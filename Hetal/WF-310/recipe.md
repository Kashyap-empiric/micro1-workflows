# Retrieval Recipe

Fixture product: LumenDesk, a fictional SaaS support operations platform. All corpus text, queries, rankings, and support policies in this repository are invented test data.

## BM25

- Lowercase all text.
- Extract maximal `[a-z0-9]+` tokens and drop tokens of length 1.
- Do not stem and do not remove stopwords.
- Okapi parameters: `k1 = 1.5` and `b = 0.75`.
- Compute document frequency over all 154 chunks.
- Use `idf(term) = ln(1 + (N - df + 0.5) / (df + 0.5))`.
- Score query terms with `idf * (tf * (k1 + 1)) / (tf + k1 * (1 - b + b * doc_length / average_doc_length))`.
- Rank by score descending and then chunk ID ascending for an exact score tie.

## Dense fallback

A real sentence embedding model could not be run in this environment: no API credential or callable embedding endpoint was available, and `sentence-transformers`, `transformers`, `torch`, and `scikit-learn` were not installed. The fixture therefore uses the prompt's permitted deterministic TF-IDF cosine fallback. BM25/dense complementarity is weaker than it would be with a sentence-transformer.

- Normalize with the same lowercase alphanumeric tokenization.
- Add every overlapping sequence of three adjacent tokens as a `phrase:` feature.
- Add one `alias:` feature for each token in the following deterministic support-domain synonym groups:
  - `ai_draft`: `assistant`, `confidence`, `machine`, `suggested`, `suggestion`, `written`
  - `late_reactivation`: `arrive`, `closed`, `finished`, `inbound`, `reopens`, `wrote`
  - `agent_handoff`: `hands`, `inherits`, `moves`, `ownership`, `responsibility`
  - `plan_reduction`: `cheaper`, `downgrade`, `historical`, `tier`
  - `concurrent_edit`: `conflicting`, `coworkers`, `edits`, `nearly`, `overwrite`, `simultaneously`
  - `omnichannel`: `channel`, `continuous`, `normalizes`, `places`, `social`, `timeline`
  - `import_suppression`: `automations`, `bulk`, `loaded`, `silent`, `skip`, `skipped`, `usual`
  - `consumption_forecast`: `campaign`, `capacity`, `credits`, `forecast`, `forecasts`, `predicted`
  - `deleted_inbox`: `correspondence`, `deleted`, `destination`, `fallback`, `inbox`, `removed`
  - `redaction`: `evidence`, `masking`, `private`, `redaction`, `sensitive`, `transcript`
  - `index_lag`: `absent`, `checkpoint`, `index`, `lookup`, `stale`
  - `spam_learning`: `classification`, `classifications`, `junk`, `mistaken`, `retroactively`, `safe`, `spam`
- Use sublinear term frequency `1 + ln(count)`.
- Use smoothed IDF `ln((1 + N) / (1 + df)) + 1`, computed over all 154 chunks.
- L2-normalize document and query vectors and rank by cosine similarity.
- Rank by score descending and then chunk ID ascending for an exact score tie.

## Reciprocal Rank Fusion

- Use `k = 60`.
- For weight `alpha`, score a chunk as `alpha * 1/(k + BM25 rank) + (1 - alpha) * 1/(k + dense rank)`.
- Use 0 for a side where the chunk is absent from that retriever's recorded top 10.
- Sweep `alpha` from 0.0 through 1.0 in steps of 0.1 and break exact fused-score ties by ascending chunk ID.

## Authoring validation

- Six hybrid-only queries were accepted only when the truth ranked from 8 through 10 for both standalone retrievers and appeared in fused top 5 at the unique best sweep weight.
- Six boundary queries were accepted only with the truth exactly at BM25 rank 5 or 6, including at least three of each.
- Four split-signal dual-truth queries were accepted only when BM25 top 5 found the first acceptable chunk but not the second, while dense top 5 found the second but not the first.
- Six disputed queries were accepted only when both candidate chunks appeared in the union of the two recorded top-10 lists.
- The full 0.0 through 1.0 RRF sweep was checked to have one unique best alpha, but its value is intentionally not included here.
- Query rows were interleaved with deterministic shuffle seed `20260721`; authoring categories are not written to the log.
- Revision passes required for the hybrid-only and disputed queries: 7.

## Fixture counts

- Corpus chunks: 154.
- Exact-match-friendly chunks: 18.
- Conceptual or paraphrase-friendly chunks: 17.
- Coherent near-duplicate decoy pairs: 6.
- Stale or duplicate chunks: 4 across 2 replacement pairs.
- Queries: 84.
- BM25-friendly queries: 12.
- Pure paraphrase queries: 12.
- Two-acceptable-ground-truth queries: 12.
- Clean split-signal dual-truth queries: 4.
- Computed hybrid-only queries: 6.
- Rank-5/rank-6 boundary queries: 6.
- Content-gap queries: 8.
- Disputed-ground-truth queries: 6.
- Near-duplicate-intent queries: 8.
