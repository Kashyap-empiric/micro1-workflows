## MODEL D

### Model:
Codex, using gpt-5.6-rose with Extra High intelligence

### Session ID
019f9294-6935-76c2-9717-7f6d6e90e2eb

### 1. Overall task success, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
Every deliverable is here and the analysis behind it is carefully reasoned throughout. The historical-cutoff write-up explicitly names the mechanism, landing time rather than authoring time, and walks through the specific commit where that distinction matters. The architecture read is precise about the harder findings too, a dormant integration described as wired but flag-off by default, and a role check on an admin screen correctly described as client-side only. Two things keep this out of the top band. The closing handoff report itself shipped with a visibly broken link reference, small, but present in the message called "Completed." And getting there took an unprompted detour into a heavier recovery path before a live correction was needed to get it back on track. The final delivery counts check out despite that, four tracked items, four attachments, one review message, exactly matching what the closing report claims.

### 2. Task accuracy, ignoring speed, rating 1 to 7 (self-imposed ceiling 6) *
6

**Commentary:**
Pull the clock out and this holds up as careful, well-evidenced work throughout. It correctly separates a buried data model from the obvious folders, calls out indirect component reuse funneled through a wrapper, and is exact about which integration is genuinely live versus wired-but-inactive. The cutoff reasoning is laid out clearly and explicitly, naming the specific field that governs "landed on main." The one real slip is a categorization error, an app-shell strategy that wraps an existing web UI gets filed under native-bridge options, when it's really a different framework-level approach entirely. The distinction between direct and indirect component reuse is a genuinely hard one to draw, and naming it explicitly instead of collapsing it into a single reuse count is a real sign of care.

### 3. Efficiency, rating 1 to 7 (self-imposed ceiling 6) *
4

**End-to-end time (minutes):** About 25
**Wrong actions / recovery:** One real detour: after a single upload stalled, it escalated on its own to a considerably heavier operating-system-level fallback, working through window selection and permission steps, rather than just retrying the simpler path first. A live nudge redirected it back to the browser plugin, and a fresh tab was all it actually needed to fix the stall.
**Commentary:**
Most of this run moved efficiently, the source review and the doc came together in one continuous stretch. The drag is concentrated in the one upload that stalled, where the chosen recovery path reached for more complexity than the problem needed. The fix that actually worked, a fresh browser tab, is exactly what a simple first retry would have tried. Everything outside that one detour moved cleanly, the source review and the document build never needed a second pass.

### 4. Writing quality, rating 1 to 7 (self-imposed ceiling 6) *
4

**Commentary:**
The document itself reads well, a clear method-and-boundary statement up front, consistent scope, dependencies, done structure across every tracked item. Two things pull this down. The final handoff message still carries an unresolved, garbled correction line about a link that reads like leaked internal error text. And the technology-comparison section groups a fundamentally different integration strategy under a heading meant for narrower bridge choices, which would genuinely confuse a reader. The phase-by-phase scope descriptions themselves are genuinely well written, specific about what's in and out of each stage rather than reading like a generic checklist.

### 5. Instruction following, rating 1 to 7 (self-imposed ceiling 6) *
6

**Commentary:**
Every explicit rule I can check lands. It verified every required permission before writing anything, scoped the browser fallback to the one confirmed gap, never ran the app or hit a live endpoint, capped the grouped phases, attached real files, and every tracked item repeats the same not-authorized-for-release language. The duplicate-summary rule matched one existing item and created the rest correctly. The one nit: the interim status update pastes local machine file-path links into what's meant to be a clean status report. The not-authorized-for-release language repeated on every tracked item is a nice touch, making the draft status impossible to miss no matter which item someone opens first.

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (self-imposed ceiling 6) *
4

**Steering needed:** Once. It had genuinely stopped and reported clearly rather than silently thrashing, but the nudge was needed specifically because it had reached for a heavier fix on its own initiative instead of the simple retry that turned out to be all it needed.
**Additional editing before I'd use it:** Not much on the substance. I'd fix the broken link line in the handoff message myself before sending it anywhere else.
**Commentary:**
Stopping clearly and reporting exactly what succeeded and what didn't is real discipline. But the recovery path it chose on its own initiative reached for a heavier operating-system-level fallback before trying the simple retry that ended up being the actual fix, and it took a live correction to pull it back. The closing self-check also wasn't tight enough to catch a broken link sitting in its own final report. It did narrate its own reasoning clearly at each step though, so the miscalibrated choice was at least visible and easy to correct rather than hidden away.

### 7. Citation quality, rating 1 to 7 (self-imposed ceiling 6) *
6

**Commentary:**
This is thoroughly sourced. Every framework, bridge, testing, and pipeline option points to its own named vendor reference, the pipeline design lays out concrete stages rather than a vague description, and the cost math correctly separates a one-time store-registration fee from a recurring developer-program fee. The one soft spot is a device-testing cost figure built on an assumed usage split rather than a single quoted price. The four-stage pipeline breakdown adds real value too, grounding the CI/CD recommendation in an actual sequence of gates rather than a single vendor name.

### 8. GUI action correctness, rating 1 to 7 (self-imposed ceiling 6), or N/A: Not applicable to this task *
3

**Commentary:**
This is a genuinely messy interface story. A file-chooser event stalled entirely on one upload, and instead of a quick retry, it escalated into a whole separate operating-system automation path, none of which ended up fixing it. It took a live redirect back to the simple browser path, and a fresh tab resolved it immediately. That's real thrashing on a task that ultimately needed a much simpler fix. The eventual fix took only a fresh tab, which makes the earlier operating-system detour read as even more avoidable in hindsight.

---

### MODEL D

#### Logs

Worked for 22m 12s

I'll first validate every required permission and resolve the repository snapshot, then read the source before producing any artifacts. I'm using the GitHub, Google Drive/Docs, and Teams messaging skills for their connector-specific workflows; I'll use Chrome as the fallback for Jira attachments or native Google Doc tabs if those connector paths are incomplete. No app execution or live endpoint probing.

Used GitHub, Atlassian Rovo, Google Drive, and Codex Apps integrations, ran commands

The basic targets resolve: GitHub grants pull access, MBTF is visible for issue creation, the named Drive folder exists, and the Teams team has an exact match. The cutoff is 12:30 UTC; the candidate commit is 368cec4... at 11:30 UTC, with two later commits excluded. I'm checking branch ancestry and the remaining write/attachment surfaces before starting the analysis.

Used Google Drive, GitHub, Atlassian Rovo, and Codex Apps integrations

Jira's connector can create/edit MBTF issues but exposes no attachment upload action. Per your fallback instruction, I'm checking the authenticated Chrome surface for the attachment control before proceeding. The Google Docs connector does advertise native addDocumentTab, so tabs have a direct path; I'll still verify them after creation.

Used Chrome integration, ran a command

Preflight passes: Chrome is authenticated in MBTF and exposes an enabled "Add attachment" action on the existing phase seed issue; Drive folder ownership and Teams can_post_directly are confirmed. I'll now analyze the cutoff snapshot in depth, including registered routes, indirect component reuse, data model, dormant/flagged paths, and credential-shaped material. I will not treat later commits as part of the blueprint.

Ran commands

The source is deliberately small but has important build blockers: two client calls have no matching registered server endpoint, auth is fixture-grade, the push screen is flag-gated, and the Stripe return URI assumes a mobile invoice-detail route that does not exist in the web tree. I'm validating current vendor pricing for the stack comparison, then I'll translate those findings into a tabbed, source-grounded blueprint and four phase packets.

Ran a command, searched the web

I'm moving onto native Google Docs authoring. The Docs skill directs a connector-native route here because the requested tab topology is an explicit native structure; I'm reading its creation, request-safety, table, citation, chip, and final-QA guidance before the first write.

Used Google Drive integration, ran commands, searched the web

The nine-tab structure is in place and populated with native headings and lists. I'm adding the high-value native tables now, registered endpoints, complete screen/component reuse, stack options and costs, contract gaps, and secret-review locations, then I'll verify the tab tree, cells, hyperlinks, date chips, and rendered export.

Used Google Drive integration, searched the web

Connector readback confirms all nine native tabs, the complete inventory and endpoint tables, native date chips, linked vendor sources, and styled fixed-width tables. I corrected an inherited blank heading at the secret table boundary. Next I'm checking the exported rendering and preparing phase-specific attachment files from the completed tab content.

Used Google Drive integration, edited a file, ran commands

Context automatically compacted

The blueprint is populated in native tabs. I'm doing the final export-quality check now, then I'll split the relevant tabs into phase packets, update/create the four Jira phases with attachments, and send the single Engineering-channel handoff.

Ran commands

Viewed 7 images

Viewed 7 images

Viewed 7 images

Ran a command

Viewed 7 images

Edited a file, ran commands

The exported tabs render cleanly across all 28 pages, including the tables and source links. I've made four fresh, phase-specific PDF packets from this exact export; next I'm applying the exact-summary duplicate guard in MBTF before any Jira write.

Used Atlassian Rovo integration

The exact-summary guard found one existing Foundation issue and no matches for the other three. MBTF-90 was updated in place; MBTF-91 through 93 were created, all in To Do. I'm using Chrome for the connector's attachment gap and will verify Jira's attachment metadata before the Teams post.

Used Chrome and Atlassian Rovo integrations, ran commands

The first packet is confirmed in Jira. The second chooser timed out during the browser interaction, so I'm reconnecting and using the browser's upload-recovery path before proceeding; I won't send the handoff until every attachment is confirmed.

Used Chrome integration

Chrome's chooser event worked for MBTF-90 but is not firing on MBTF-91, even through the underlying file input. I'm going to use the Windows app-control skill for the native picker fallback that Chrome's upload guidance permits, while keeping the target narrowly limited to the generated phase packet.

Ran a command
Read Windows control guidance
Find native file picker
Locate Chrome window
Ran a command
Open work Chrome window
Requested permission
Retry Chrome window state
Select Jira browser tab
Recheck Chrome tab state
Select Jira tab
Observe Chrome focus
use chrome plug in

11:14 AM

Used Chrome integration

Understood, I'll stay in the Chrome plugin for the remaining Jira uploads. I'm dropping the Windows app-control fallback and will retry from a fresh Jira page state, then verify each attachment through Jira before sending Teams.

Used Chrome and Atlassian Rovo integrations

I stopped at the attachment failure, so this is not a completed handoff.
The native-tabbed Google Doc was created in the Mobile Build - Test Fixture Drive folder. It records the resolved snapshot as 368cec4aff9f293a2564eb6c35f3d9045b343c2c, the latest main-branch commit landed at or before 10 July 2026, 18:00 IST. I did not run the app or call its endpoints.

Jira phase | Result | Status | Attachment
MBTF-90, Foundation and auth | Exact-summary match updated in place | To Do | PDF attached and verified
MBTF-91, Core invoices and navigation | Created | To Do | Missing
MBTF-92, Notifications and observability | Created | To Do | Missing
MBTF-93, Verification and release readiness | Created | To Do | Missing

Correction: the MBTF-93 link is here.
The Chrome plugin successfully uploaded MBTF-90's 176,202-byte phase packet. On MBTF-91, Jira's Add attachment menu was reachable, but Chrome repeatedly timed out waiting for its file-chooser event, including after a fresh page load and a retry through the file input. No second upload was confirmed. The prepared packets are available locally as three local PDF file links.
I did not send the Microsoft Teams post, because the attachment requirement is incomplete and you asked me to stop on a half-broken setup. I also made no status transitions or other notifications. Please bring the kept MBTF-91 Jira tab to the foreground in Chrome and tell me to retry; I'll continue with the Chrome plugin, verify all three attachments, and only then send the one Engineering-channel post.

Edited 2 files, +60/-0
.codex-staging/build_current_phase_packets.py +59/-0
.codex-staging/current-blueprint.pdf.b64 +1/-0

11:16 AM

try again. use chrome plugin

11:16 AM

Worked for 3m 9s

I'll retry the remaining uploads through the Chrome plugin, verify them in Jira, and then send the one Engineering-channel handoff if all three succeed.

Used Chrome integration, ran commands

The fresh Chrome tab fixed the chooser problem. MBTF-91 now shows its PDF in Jira's Attachments section. I'm applying the same active-tab path to MBTF-92 and MBTF-93.

Used Chrome and Atlassian Rovo integrations

All four Jira issues now have their phase-specific PDF attachment, and Jira metadata confirms they remain in To Do. I'm using the Teams message skill to send the single requested review announcement to the exact Engineering channel.

Used Codex Apps integration, ran a command

Completed.
The Mobile Build Blueprint - webapp-main is in the Mobile Build - Test Fixture Drive folder with nine native tabs: Overview, Architecture, Screen Inventory, Mobile Stack, User Flow, Data & API Contracts, Risks & Open Questions, Secrets found (review), and Delivery Plan.
The resolved main-branch snapshot is 368cec4aff9f293a2564eb6c35f3d9045b343c2c, landed at 17:00 IST on 10 July 2026. The later 18:30 and 19:00 IST commits were excluded. The review was static; I did not run the app or contact its endpoints.

Phase | Sprint span | Jira result | Attachment | Status
Foundation and auth | 1-2 | MBTF-90 updated in place | 176,202-byte PDF | To Do
Core invoices and navigation | 2-4 | MBTF-91 created | 142,003-byte PDF | To Do
Notifications and observability | 4-5 | MBTF-92 created | 182,543-byte PDF | To Do
Verification and release readiness | 5-6 | MBTF-93 created | 148,235-byte PDF | To Do

The correct MBTF-91 link is MBTF-91. Chrome successfully uploaded the remaining phase packets, and Jira metadata confirmed all four PDFs and statuses.
The blueprint recommends React Native with Expo development builds, a typed and hardened API boundary, secure session storage, and native deep-link/payment/push contracts. It calls out the fixture-grade authentication, settings-route mismatch, missing push-installation handler, relative API addressing, Stripe callback gaps, and client-only admin authorization as build blockers. Inferences are labeled, and credential-shaped findings are recorded only by file and line without values. The Mobile Stack tab weighs named alternatives and published pricing from Expo, Codemagic, BrowserStack, and Firebase Test Lab.
Finally, I actually sent the requested Engineering-channel Teams post linking the doc and listing MBTF-90 through 93. No issues were transitioned, and no other notification was sent.

#### Output

--- Teams message, "Testing Client Workflows" team, "Engineering" channel ---
The Mobile Build Blueprint - webapp-main is ready for review.
Jira phase issues created or updated: MBTF-90, MBTF-91, MBTF-92, and MBTF-93. Each has its relevant blueprint-tab PDF packet attached and remains in To Do as a draft.

--- Google Doc "Mobile Build Blueprint - webapp-main", Overview tab ---
Mobile Build Blueprint - webapp-main
Code-only mobile build draft

Resolved snapshot
Repository: kashyapempiricinfotech-sys/webapp-main, main branch.
Exact cutoff commit: 368cec4aff9f293a2564eb6c35f3d9045b343c2c
Cutoff: Jul 10, 2026 at 18:00 IST (12:30 UTC). The resolved commit landed at 17:00 IST.
Resolution used committer/landing time on main, not author time.
The later legacy-session change has an author time before the cutoff but a committer time of 19:00 IST; the experimental scanner commit landed at 18:30 IST. Both are excluded. No scanner files or later cookie hardening are treated as part of this snapshot.

Method and boundary
Static source review only: tree, package manifest, app pages, /api, server registration and route manifest, middleware, services, integrations, component barrel/HOC, and buried Prisma schema. No app was run and no application endpoint was contacted. Code facts carry file traces; proposed behavior is labeled (inferred). This repository identifies itself as a disposable fixture and says not to deploy it (README.md).
Recommended direction (inferred): build a React Native/Expo client around a versioned, hardened API contract; rewrite DOM UI as native components; preserve useful TypeScript domain types only after separating them from web assumptions. Resolve authentication, endpoint drift, deep links, push installation, and authorization before feature parity.

Tab guide
- Architecture - runtime stack, registration, business modules, auth generations, integrations, and endpoint inventory.
- Screen Inventory - all six cutoff pages and four reusable component/HOC definitions, with direct and indirect reuse counts.
- Mobile Stack - framework, native bridge, test, and CI/CD alternatives with named tiers, assumptions, current vendor prices, and a recommendation.
- User Flow - code-observed and proposed screen-to-screen movement, with missing transitions called out.
- Data & API Contracts - Prisma/TypeScript model, endpoint contract drift, and mobile contract decisions.
- Risks & Open Questions - prioritized blockers, decisions, owners to assign, and verification gates.
- Secrets found (review) - credential-shaped and fixture auth material locations only, no values reproduced.
- Delivery Plan - four dependency-ordered phases spanning Sprint 1 through Sprint 6 and acceptance gates.

Decision status
Draft for engineering review. No Jira phase is authorized to leave To Do, and this blueprint does not authorize production deployment.

--- Google Doc, Mobile Stack tab ---
Mobile Stack
Decision comparison, cost assumptions, and build pipeline

Recommendation (inferred)
Use React Native with Expo development builds, a typed API client, secure token storage, native deep linking, and a server-owned payment/push contract. Existing React/TypeScript domain types reduce language/context switching, but DOM components and Next pages are not drop-in React Native UI.

Framework alternatives
React Native + Expo: retains React/TypeScript mental model and can extract domain contracts; Expo provides routing and native modules. It still requires native UI rewrites and disciplined SDK upgrades. The framework is free/open source; EAS is optional. Priced tier: Expo Free, $0/month framework/EAS entry tier; paid CI is compared separately.
Flutter: cohesive Dart/widget rendering and strong cross-platform consistency, but the TypeScript/React fixture gains less direct code reuse and the team takes a language/tooling transition. Priced tier: Flutter open-source BSD SDK, $0/month license; no vendor paid SDK tier.

Native bridge alternatives
Expo SDK + Expo Modules API (recommended, inferred): use maintained modules for secure storage, notifications, linking/browser, and custom Swift/Kotlin modules when a required SDK is not covered. Priced tier: Expo framework/SDK open source, $0/month license; optional EAS Production is budgeted in CI/CD, not double-counted.
Capacitor native runtime: wraps web UI in a WebView and offers native plugins/custom plugins, potentially preserving more DOM. It does not resolve this fixture's relative API/proxy, auth, or missing endpoint contracts, and a web-first shell may compromise native navigation/accessibility expectations (inferred). Priced tier: Capacitor open-source runtime, $0/month license.

Testing alternatives and strategy
Keep TypeScript contract/unit tests and component tests in CI; add deterministic end-to-end journeys for login, expired-token recovery, invoice list, checkout callback, preferences, flag-off/on notifications, and admin denial (inferred). Maestro CLI is an open-source YAML flow authoring option; device execution cost is separate. Existing Vitest is declared, but no mobile test suite exists at the cutoff.

Cloud option A: BrowserStack App Automate Device Cloud, one parallel test, $199/month equivalent billed annually. Predictable subscription, broad iOS/Android coverage, but annual commitment and parallelism costs apply.
Cloud option B: Firebase Test Lab Blaze pay-as-you-go. Above daily no-cost time, physical devices are $5/device-hour and virtual devices $1/device-hour, billed by rounded minute. Illustrative upper-bound: 20 physical device-hours plus 10 virtual device-hours in a month, about $110 before credits/daily no-cost allowances.

CI/CD alternatives
EAS Production (recommended initial route, inferred): $199/month plus additional usage, with $225 build credit, two included concurrencies and 50K EAS Update MAUs.
Codemagic Team Pay-as-you-go: $0 base/month; macOS M2 $0.095/minute, Linux/Windows $0.045/minute, one included concurrency; extra concurrency $49/month. At 1,000 M2 minutes and 500 Linux minutes, estimate $117.50/month before tax and extra concurrency.

Pipeline design (inferred)
1. Pull request: secret scan, lockfile/dependency review, lint, TypeScript, unit/component tests, API contract tests against mocks, and an unsigned development build.
2. Merge to main: reproducible iOS/Android development or preview builds, signed only through managed CI secrets; run smoke/E2E on simulators and a real-device matrix.
3. Release candidate: version/build-number policy, changelog, privacy/permission review, deep-link/payment/push tests, crash and analytics validation with non-production keys, and accessibility and offline/error-state checks.
4. Manual approval gate: upload to TestFlight and Play internal/closed testing, signed only through non-production keys, staged rollout plan and rollback/runbook. No production submission is authorized by this draft.

Cost envelope and sources
Pricing checked Jul 24, 2026. Selected illustrative recurring envelope: EAS Production $199 + BrowserStack Device Cloud $199 annual-billed equivalent + Apple Developer Program $99/year (about $8.25/month amortized), about $406.25/month. Google Play registration is $25 once, not monthly. Taxes, EAS overage, backend hosting, payment processing, analytics/error volume, devices, labor, and support are excluded. This is a planning estimate, not a quote.

Vendor sources: Expo pricing, Codemagic pricing, BrowserStack pricing, Firebase Test Lab pricing, React Native framework guidance, Flutter architecture, Expo Modules API, Capacitor runtime, Maestro CLI, Apple Developer Program, Google Play Console.

Option comparison table:
Category/option | Fit and trade-off | Tier/rough monthly cost
Framework: React Native + Expo | React/TS alignment, native UI rewrite, recommended (inferred) | Expo Free/OSS: $0, optional EAS separate
Framework: Flutter | Cohesive Dart widgets, lower direct reuse here (inferred) | Open-source BSD SDK: $0 license
Bridge: Expo SDK + Modules | Maintained modules and custom Swift/Kotlin, dev builds, recommended (inferred) | Expo OSS SDK: $0 license
Bridge: Capacitor | WebView/DOM reuse and plugins, web-shell trade-offs (inferred) | Open-source runtime: $0 license
Testing: BrowserStack App Automate | Broad real-device automation, annual commitment, 1 parallel | Device Cloud: $199/mo equivalent, billed annually
Testing: Firebase Test Lab | Usage-shaped device matrix, quota/coverage planning | Blaze: illustrative under $110 for 20 physical + 10 virtual hours before free allowances
CI/CD: Expo EAS | Integrated build/submit/update, credits and overage, recommended (inferred) | Production: $199/mo + usage, $225 credit
CI/CD: Codemagic | Cross-framework usage billing, explicit signing/control | Team PAYG: about $117.50 for 1,000 M2 + 500 Linux min

--- Google Doc, Delivery Plan tab ---
Delivery Plan
Four draft phases across Sprint 1-Sprint 6

Planning assumptions (inferred)
Sprint numbers express sequencing, not committed calendar dates or Jira Sprint field membership. An issue spanning multiple sprints remains one phase issue; the description carries its span. Dependencies are explicit. All phase issues remain To Do until review.

Phase 1 - Foundation and auth | Sprint 1-2
Establish Expo/React Native workspace, environment/base URL, typed contract/mocks, navigation shell, secure storage, identity redesign, JWT/refresh lifecycle, legacy-session migration decision, secret remediation, CI baseline, and deep-link skeleton. Depends on security/API decisions. Done: reviewed contract and threat model, no fixture credentials/defaults in mobile, mocked login/restore/logout/401 flow tested, builds reproducible, secrets scan and type/unit gates passing. Sources: Architecture, Data & API Contracts, Risks & Open Questions, Secrets found (review), Mobile Stack.

Phase 2 - Core invoices and navigation | Sprint 2-4
Implement authenticated Dashboard, Invoices list, native InvoiceCard/CTA/shell, detail route, loading/empty/error/offline states, typed pagination/ownership contract, checkout launch and verified return/reconciliation. Depends on Phase 1 identity, base URL and API contract. Done: iOS/Android journeys cover login, dashboard, list, detail, checkout success/cancel and 401 recovery against controlled environments/mocks; accessibility and analytics hooks reviewed. Sources: Screen Inventory, User Flow, Architecture, Data & API Contracts.

Phase 3 - Notifications and observability | Sprint 4-5
Align preference endpoint, implement installation API/server token lifecycle, permission/consent UX and feature flag, APNs/FCM delivery contract, PostHog taxonomy/privacy, Sentry mobile/server release setup, dashboards and alert ownership. Depends on Phase 1 auth and Phase 2 shell/contracts. Done: flag-off safe, opt-in/denial/revoke/token rotation and preference persistence tested, no PII leakage, events/errors verified with non-production configuration, rollout gate approved. Sources: Architecture, User Flow, Data & API Contracts, Risks & Open Questions, Mobile Stack.

Phase 4 - Verification and release readiness | Sprint 5-6
Complete unit/component/contract/E2E and real-device matrix, security/accessibility/performance/offline/deep-link/payment/push regression, signing, privacy, store metadata, beta distribution, staged rollout and rollback runbook. Depends on prior phases and resolved P0/P1 decisions. Done: release candidate passes agreed quality gates on supported iOS/Android devices, artifacts/provenance and TestFlight/Play test-track evidence exist, approval/rollback ownership is recorded, and no production release occurs under this draft. Sources: Mobile Stack, User Flow, Risks & Open Questions, Delivery Plan.

Dependency path
Foundation/auth, then core navigation/invoices, then notifications/observability, then verification/release readiness. Phase 2 can begin contract/UI work during Sprint 2 after Phase 1 interfaces stabilize; Phase 3 follows the authenticated shell; Phase 4 overlaps late integration but cannot close before all gates pass (inferred).

--- Jira MBTF-90, "Foundation and auth" ---
Status: To Do
Phase 1 - Foundation and auth
Sprint span: Sprint 1-Sprint 2. This is the earliest dependency-bearing phase. Sprint numbers express sequencing and the span is intentionally recorded in the description because one phase crosses sprint boundaries.
Blueprint: [link]. The attached PDF packet contains the relevant native tabs: Overview, Architecture, Mobile Stack, Data & API Contracts, Risks & Open Questions, Secrets found (review), and Delivery Plan.

Scope
- Establish the React Native/Expo development-build workspace, environment separation, HTTPS API base URL, typed/versioned contract, mocks, navigation shell, secure token storage, deep-link skeleton, and reproducible iOS/Android CI baseline.
- Replace fixture-grade login and refresh behavior with a reviewed identity and authorization design: real credential/identity-provider validation, signing and key management, issuer/audience/expiry validation, refresh rotation and revocation, controlled 401 retry/logout, and server-side role/ownership enforcement.
- Decide migration or retirement of the registered legacy cookie-session path; do not extend it into mobile without an explicit reviewed compatibility plan.
- Resolve the client/server contract drift and missing API boundaries before dependent feature implementation, including canonical preferences path, request headers/error envelope, environment routing, and generated typed client.
- Security-review credential-shaped and fixture material at the locations recorded in the blueprint; assess exposure and rotate/revoke/remove where appropriate. Do not copy any credential value into Jira, chat, build output, or mobile defaults.
- Add secret scanning, dependency/lockfile review, lint, TypeScript, unit/contract tests, and unsigned development-build gates.

Dependencies and handoff
Security, identity, API, and product owners must approve the contract and threat model. Phase 2 can start contract/UI work in Sprint 2 only after stable interfaces and authentication boundaries are agreed. Phases 3 and 4 depend on this foundation.

Definition of done
- Reviewed identity, authorization, refresh, legacy-session, API versioning, environment, and threat-model decisions are recorded and owned.
- No fixture credential, fallback key, static token, or demo default is carried into the mobile client or production configuration; security findings are privately assessed and remediation tracked.
- Mocked login, secure restore, expiry, one controlled refresh/retry, logout, and invalid-token/401 paths pass on iOS and Android.
- A canonical typed API contract and error model exist, with contract tests covering authentication and the initial protected boundary.
- Reproducible development builds and CI secret-scan, type, lint, unit, and contract gates pass.
- Deep-link and navigation skeletons are validated without production payment or push enablement.

Draft control: Keep this issue in To Do pending review. This phase does not authorize deployment or production release.
Attachments: 1 file.

--- Jira MBTF-91, "Core invoices and navigation" ---
Status: To Do
Phase 2 - Core invoices and navigation
Sprint span: Sprint 2-Sprint 4. Contract and shell work can begin late in Sprint 2 after Phase 1 interfaces stabilize; feature completion follows the approved identity and API foundation.
Blueprint: [link]. The attached PDF packet contains Overview, Architecture, Screen Inventory, User Flow, Data & API Contracts, and Delivery Plan.

Scope
- Implement the authenticated native shell and Dashboard, Invoices list, native InvoiceCard and accessible CTA primitives, invoice detail route, and explicit loading, empty, error, offline, and retry states.
- Replace demo card/list assumptions with a reviewed, typed, paginated invoice contract, ownership/role authorization, currency/status validation, and server-originated state.
- Wire Dashboard, Invoices, and detail navigation and define whether invoice creation is in MVP; the cutoff CTA labels do not themselves implement navigation.
- Implement server-owned Stripe Checkout launch and verified success/cancel app or universal-link return, callback validation, idempotency, ownership/amount checks, and webhook/status reconciliation. Do not trust client-supplied amount or callback state.
- Carry accessibility and reviewed analytics hooks through shared native components; define safe 401 recovery against the Phase 1 session lifecycle.
- Decide the server-authorized Admin Reports branch and MVP boundary before exposing any report data; a client role check alone is not an authorization control.

Dependencies
Depends on Phase 1's reviewed identity, secure session, HTTPS base URL, typed API/error model, and deep-link skeleton. Payment and product owners must resolve checkout policy and invoice-detail/create scope. Phase 3 consumes the authenticated shell and contract conventions.

Definition of done
1. iOS and Android controlled-environment or mock journeys cover login, Dashboard, invoice list, detail, checkout launch, success/cancel return, including expired-session/401 recovery.
2. List/detail ownership, pagination, status/currency validation, empty/error/offline states, and retry behavior have contract and component tests.
3. Deep links are verified for cold and warm starts; callback state and server reconciliation are tested without production payment credentials.
4. Shared shell, card, and CTA meet agreed accessibility and telemetry conventions.
5. Admin data is absent from mobile or protected by a reviewed server-side role/tenant/ownership policy and tested denial path.
6. Product signs off the invoice creation and MVP boundaries; no unwired demo CTA is presented as a working capability.

Draft control: Keep in To Do. This issue does not authorize production payment or release.
Attachments: 1 file.

--- Jira MBTF-92, "Notifications and observability" ---
Status: To Do
Phase 3 - Notifications and observability
Sprint span: Sprint 4-Sprint 5. This follows the authenticated shell and stable API conventions from Phases 1-2.
Blueprint: [link]. The attached PDF packet contains Overview, Architecture, Mobile Stack, User Flow, Data & API Contracts, Risks & Open Questions, and Delivery Plan.

Scope
- Align the reminder-preference client and server on one canonical versioned route/schema. The cutoff client targets a different path from the registered preference handler.
- Design and implement the authenticated push-installation API and server token lifecycle: registration, platform/provider mapping, rotation, deletion, consent state, failure handling, and APNs/FCM delivery ownership. The cutoff client installation target has no registered handler.
- Build permission education, OS permission, opt-in/denial/revocation, preferences, and feature-flag-safe Notifications Center UX. Keep the feature disabled until contract, consent, delivery, and rollback gates are reviewed.
- Define mobile/server PostHog SDK placement, consent and event taxonomy, PII minimization, environment keys, sampling, dashboards, and ownership. The cutoff browser SDK startup placement and exported event call-site gap require review.
- Define Sentry mobile/server projects, release and source-map handling, privacy/sampling, alert ownership, and non-production verification. The cutoff integration is wired but flag-dormant by default.

Dependencies
Depends on Phase 1 authentication, environment and contract decisions and Phase 2 shell/navigation. Security, privacy, notification, analytics, and observability owners must approve provider, consent, retention, and alert policies. Phase 4 verifies the resulting behavior on a device matrix.

Definition of done
1. Preference persistence uses the approved canonical contract and passes client/server contract tests.
2. Installation, token rotation/deletion, opt-in, denial, revocation, delivery failure, and feature-off paths pass on supported iOS/Android devices or controlled test infrastructure.
3. No push feature is enabled by default before consent, authenticated server delivery, monitoring, rollback, and ownership gates are approved.
4. Event and error telemetry are verified with non-production configuration; no unapproved PII or secret is emitted.
5. Dashboards, alerts, sampling, release/source-map policy, privacy disclosures, and accountable owners are documented and tested.
6. Rollout and disablement gates are approved for the later release-readiness phase.

Draft control: Keep in To Do; no production notification or analytics rollout is authorized.
Attachments: 1 file.

--- Jira MBTF-93, "Verification and release readiness" ---
Status: To Do
Phase 4 - Verification and release readiness
Sprint span: Sprint 5-Sprint 6. Verification can overlap late integration, but this phase cannot close until the prior phase gates and P0/P1 decisions are resolved.
Blueprint: [link]. The attached PDF packet contains Overview, Mobile Stack, User Flow, Risks & Open Questions, and Delivery Plan.

Scope
- Complete unit, component, typed-contract, end-to-end, simulator/emulator, and real-device coverage across the agreed iOS/Android support matrix.
- Exercise authentication expiry/refresh/logout, invoice list/detail states, checkout success/cancel and cold/warm deep links, preference persistence, push permission/token lifecycle, feature-off behavior, admin denial, network/offline/error recovery, and telemetry privacy.
- Run security, dependency and secret-scan, accessibility, performance, localization/region, transport, and release-configuration checks.
- Establish signing and managed CI secrets, version/build-number and artifact-provenance policy, source maps, privacy/store metadata, TestFlight and Play internal/closed-test evidence, monitoring, approval, and rollback runbook.
- Re-price build/device usage against actual expected minutes, device-hours, MAUs, and concurrency; the blueprint cost envelope is illustrative and excludes overage, taxes, backend, labor, and other variable services.

Dependencies
Depends on Phases 1-3, approved identity/API/payment/notification/analytics/privacy decisions, and named product, security, release, and operational owners. The draft does not grant permission to submit to production stores.

Definition of done
1. Agreed quality gates pass on the supported real-device and OS matrix, with reproducible artifacts and traceable test evidence.
2. Authentication, payment/deep-link, push, offline/error, authorization denial, accessibility, performance, security, and privacy regressions pass or have explicitly accepted, owned exceptions.
3. Signing, CI secret handling, versioning, provenance, source maps, store disclosures, beta-track evidence, monitoring, staged rollout, and rollback procedures are reviewed.
4. Release and rollback approvers and operational alert owners are recorded; budget assumptions are refreshed from measured usage.
5. No production deployment, store submission, or feature rollout occurs under this draft. A separate explicit approval is required.

Draft control: Keep in To Do pending review and authorization.
Attachments: 1 file.

