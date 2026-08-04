## MODEL C

### Model:
Codex, using gpt-5.6-cyan with High intelligence

### Session ID
019f8e86-cde3-7883-aa8c-4e6e3d587e35

### 1. Overall task success, rating 1 to 7 (self-imposed ceiling 6) *
4

**Commentary:**
Every deliverable landed, and the run's own honesty about never visually checking the rendered document is worth more than a false claim of having verified it. Real architectural findings back this up, a data model tracked into a non-obvious location, a dormant integration correctly kept off the active list. But the historical-cutoff write-up never shows why the harder excluded commit is actually excluded, just states the outcome. And reaching a finished state took two rounds of live help, one a genuine dead end this run could not resolve on its own, needing an outside fix before it could actually finish. The four tracked items are also internally consistent with the document itself, matching phase to attachment correctly across the board.

### 2. Task accuracy, ignoring speed, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
The architecture read is genuinely strong on the harder findings: a data model tracked down outside the obvious folders, a dormant integration correctly kept separate from the live ones, an admin screen's role check correctly identified as client-side only. But the historical-cutoff reasoning doesn't hold up the same way, it states which commits are excluded without ever showing the mechanism. The framework recommendation has the same gap, labeled inferred but never tied to one specific piece of code. The dual authentication write-up is precise too, treating the current and the deprecated flow as two separate generations rather than folding the old one into a footnote.

### 3. Efficiency, rating 1 to 7 (self-imposed ceiling 6) *
4

**End-to-end time (minutes):** About 40
**Wrong actions / recovery:** One real detour: it dropped down to driving the upload dialog at the operating-system level after the browser path failed, and that attempt didn't end up being what fixed anything either. It did recover, but only after a tool permission got changed by someone outside the run.
**Commentary:**
Most of this run moved at a good clip, the code inventory, doc, and work items came together without wasted motion. The drag is concentrated almost entirely in one spot: a single upload step that stalled twice and needed a person to fix a setting it couldn't touch itself. That's exactly the kind of thrashing pattern that should pull this down, even though the analysis work itself never meandered. The recovery once it did land was clean, the very next attempt succeeded and the run picked back up exactly where it left off rather than re-doing earlier steps.

### 4. Writing quality, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
Both the narration and the finished artifacts read well, short status lines, real headings and tables instead of flat paragraphs, and a synthesis view pulling the phase-by-phase detail into one timeline that wasn't strictly asked for but genuinely helps. Two things pull this down. A couple of the work-item descriptions and their matching doc sections use close to identical phrasing, reading copied rather than freshly written. And the closing narration leans on the same stock transition phrases, repeated across nearly every update. The Teams message in particular is well calibrated for its audience, stating what changed without padding it out with detail that belongs in the document.

### 5. Instruction following, rating 1 to 7 (self-imposed ceiling 6) *
5

**Commentary:**
Most of the explicit rules land cleanly: the duplicate-summary rule applied exactly as written, credential material pointed at by file and line, everything left in the not-started state. Where this comes up short is the same historical-cutoff constraint, which needs the reasoning actually shown rather than an answer simply stated, and the run never demonstrates it. It also flagged more credential-shaped locations than the obvious ones, which reads as either thorough or slightly over-eager, and nothing settles which. The static-review boundary is respected throughout too, nothing in the record suggests the application was ever run or an endpoint contacted.

### 6. Collaboration, autonomy, and verification, rating 1 to 7 (self-imposed ceiling 6) *
4

**Steering needed:** Twice, and for different reasons. The first came right after it correctly refused to guess between two ambiguous duplicates and paused instead, which was good judgment rather than a mistake needing correction. The second was real, it had stalled on the upload step and needed outside help.
**Additional editing before I'd use it:** Some. I'd want to personally click through the finished doc and the four work items, confirm the cutoff-exclusion reasoning myself, and check the rendering the run's own closing note admits was never inspected.
**Commentary:**
Pausing rather than guessing on the ambiguous duplicate is good judgment. But the upload failure that followed wasn't something this run could resolve on its own, it took someone outside changing a permission by hand. The verification it ran before sending the review message was genuine, an actual re-query, but it stopped at structure and never confirmed how the finished document renders. That re-query specifically checked attachment count and status per item rather than relying on a general sense that things looked fine.

### 7. Citation quality, rating 1 to 7 (self-imposed ceiling 6) *
6

**Commentary:**
Grounding here works on two fronts. Code-derived claims, architecture notes, data model gaps, the secrets review, are all tied to specific files and line numbers instead of vague assertions. The technology comparison is sourced the same way, each option pointing to its own reference, backed by a decision matrix and a computed monthly cost. The one thing short of flawless: one cost figure is a rough estimate built on an assumed usage number, and the linked pages are general pricing or FAQ pages rather than specific plan-tier docs. The decision matrix format itself adds real value, turning the sourcing into something scannable rather than requiring a reader to piece the comparison together from paragraphs.

### 8. GUI action correctness, rating 1 to 7 (self-imposed ceiling 6), or N/A: Not applicable to this task *
3

**Commentary:**
Most of this run was connector-driven with no real interface to judge, but the one place it did have to drive a UI is where it struggled most. The browser-based upload path failed to even open a file picker. It then tried the operating-system level, selecting the window directly, and that didn't pan out either. It did eventually land in the right final state, but the path there was enough thrashing that I can't call this higher than a 3. Neither failed attempt produced a clear diagnostic on its own, it took an outside party recognizing the actual permission problem before the run could even understand what to fix.

---

### MODEL C

#### Logs

Worked for 4m 52s

I'll start with the access gate and stop immediately if any required capability fails. I'm using the GitHub, Google Docs/Drive, Atlassian, Teams message, and Chrome-control skills because this job spans those systems and explicitly requires Chrome fallback for Jira attachments or document tabs. I'll verify access first, then resolve the historical commit and read the code without running it or calling live endpoints.

The required connector surfaces are present. The Google Docs connector advertises native tab creation directly; Jira's connector does not expose attachment uploads, so the Chrome fallback is required for that specific step. I'm now checking the named project/folder/channel and the Jira issue UI before creating anything.

Used Google Drive, GitHub, Atlassian Rovo, Chrome, Codex Apps, and the browser, ran commands

The duplicate-safety check has hit a hard stop before any write: MBTF already contains two separate "Foundation and auth" issues, MBTF-75 and MBTF-76. That is the foundational phase named in the requested breakdown, and your rule says to stop when an exact summary has more than one match. I'm closing the read-only browser checks and will leave the repository, Drive, Jira, and Teams unchanged.

Used Chrome integration

Stopped before creating anything because Jira contains two exact matches for the foundational phase:
MBTF-75 - "Foundation and auth"
MBTF-76 - "Foundation and auth"
Your rerun rule requires stopping when more than one exact match exists. No Google Doc, Jira updates or attachments, or Teams post were made.
The GitHub repository was readable, and the named Jira project, Drive folder, Teams team/channel, and authenticated Jira Chrome session were reachable. Full attachment and document-tab write validation was not attempted after the duplicate stop.

4:05 PM

delete one and then continue

4:07 PM

Worked for 24m 43s

I'll delete the newer duplicate, MBTF-76, preserve the older MBTF-75 as the canonical "Foundation and auth" issue, and then resume the original workflow. I'm continuing with the Jira/Chrome, GitHub, Google Docs/Drive, and Teams workflows; the deletion is the only extra write beyond your original request.

Used Chrome and Atlassian Rovo integrations, ran commands

MBTF-76 is deleted and the exact-summary check now returns only MBTF-75. I'm moving into the code review next: resolving the historical main-branch commit, then reading its route and server files without executing the app or contacting any application endpoint.

Used GitHub integration

The historical cut is resolved to 368cec4aff9f293a2564eb6c35f3d9045b343c2c (committed 17:00 IST). GitHub confirms it is the main-branch merge base and that the next two main commits landed after the 18:00 IST cutoff. I'm now pulling the 34 files from that exact commit for a file-by-file inventory.

Used GitHub integration, searched the web

The code inventory is complete. The architecture is small but deliberately mixed: six Next screens, one /api health handler, Express routers plus a dynamic manifest, two live auth generations, Prisma/PostgreSQL models, active Stripe/PostHog, dormant Sentry, and feature-gated push UI. I also found credential-shaped material; I'll reference only file and line locations in the required secrets-review tab, never copy the values. The Google Docs workflow is now guiding the native-tab and table construction.

Used Google Drive integration, searched the web

Native tabs are in place and all nine tab bodies have been written. The first date-chip batch was rejected atomically because Google Docs does not accept the en-IN chip locale; no content changed. The Docs workflow's validation prevented a partial write, and I'm retrying with the supported en locale.

Used Google Drive integration

The blueprint is now a nine-tab native Google Doc with real title/heading styles, native bullet/numbered lists, native date chips, seven linked pricing sources, and a formatted comparison table. I'm exporting it for Jira attachments next, then I'll upsert the four phase issues and keep each in To Do.

Used Google Drive and Atlassian Rovo integrations, edited files

The four Jira phase issues are now in place: MBTF-75 was updated, and three new To Do tasks were created. I've also prepared four attachment files containing the relevant tab extracts, with secret values excluded. The Chrome attachment fallback is the remaining Jira step.

Used Chrome integration, ran commands

Context automatically compacted

The duplicate is gone. I'm finishing the four attachment uploads now, then I'll re-verify the Jira set and document structure before sending the single Teams announcement.

Used Chrome integration, ran commands

Chrome can reach Jira, but the extension's file-chooser bridge isn't firing. I'm switching to the Windows UI for the upload step so the native file dialog can complete the attachments without changing the issue scope.

Initialize Windows upload control
Select Chrome window
Inspect Chrome upload window

Deleted duplicate MBTF-76, then stopped at the attachment prerequisite.
Chrome's file-chooser bridge did not open, and the Windows fallback ended because it could not confidently verify the active browser URL. Therefore:
Jira attachments were not uploaded.
The Teams announcement was not sent.
Existing issues remain in To Do.
The Google Doc blueprint and Jira work already created remain in place.
To enable file upload, go to chrome://extensions in Chrome, click Details under the ChatGPT Chrome Extension, and enable "Allow access to file URLs." See here for details.

Edited 4 files, +149/-0
Review changes
jira-attachments/Mobile Build Blueprint - Core screens.md +39/-0
jira-attachments/Mobile Build Blueprint - Foundation and auth.md +39/-0
jira-attachments/Mobile Build Blueprint - Notifications and analytics.md +37/-0
(1 more file)

4:31 PM

continue

4:33 PM

Worked for 9m 15s

I'll retry the Jira uploads first. If all four attachments verify, I'll run the duplicate/status and document checks, then send the one Teams post as the final external action.

Used Chrome integration, ran commands

The upload path is working now; the foundation file is saved on MBTF-75. I'm applying the same verified sequence to the other three phase issues.

Used Chrome and Atlassian Rovo integrations, ran commands

Searched Jira issues using JQL

All four Jira files are attached and connector-readback confirms one exact issue per summary, one attachment each, and To Do on every issue. I'm doing the document's final native-tab readback now.

Used Google Drive and Codex Apps integrations, ran commands
Ran Get-Content '...google-docs\SKILL.md' | Select-Object -First 180
Ran Get-Content '...google-docs\SKILL.md' | Select-Object -Skip 180 -First 180
Ran Get-Content '...google-docs\SKILL.md' | Select-Object -Skip 360

Got document
Listed 2 folder items
Listed 2 folder items
Microsoft Teams resolve team
Microsoft Teams resolve channel
Microsoft Teams validate write target

The blueprint has passed its final connector checks: nine native tabs, exact historical SHA, pricing source links/table, all six sprint references, and no copied secret values. I'm sending the single Engineering-channel review post now.

Used Chrome and Codex Apps integrations
Microsoft Teams send channel message
Close attachment workspace

Completed.
Mobile Build Blueprint - webapp-main, with nine native tabs.
Historical commit: 368cec4aff9f293a2564eb6c35f3d9045b343c2c.
Jira: MBTF-75, MBTF-78, MBTF-79, and MBTF-80.
Each issue has its relevant blueprint extract attached and remains To Do.
Duplicate MBTF-76 was deleted; each exact summary now has one match.
Teams review post sent.
No application code or live application endpoints were executed. Native document structure was verified; rendered PDF visual QA was unavailable.

#### Output

--- Teams message, "Testing Client Workflows" team, "Engineering" channel ---
The Mobile Build Blueprint for webapp-main is ready for review:
https://docs.google.com/document/d/1eE4UPBAvEE3PD1O413bKodfrLhAzV6mgmn-alQ-Lv7M
Jira issues created or updated: MBTF-75, MBTF-78, MBTF-79, MBTF-80.

--- Google Doc "Mobile Build Blueprint - webapp-main", Overview tab ---
Mobile Build Blueprint - webapp-main

Resolved source snapshot
Commit SHA: 368cec4aff9f293a2564eb6c35f3d9045b343c2c
Historical source cut-off: Jul 10, 2026 at 18:00 IST (12:30 UTC). The selected commit landed at 17:00 IST and is the main-branch merge base before two later commits.
Method: static code review only. The app was not run and no live application endpoint was contacted.
Prepared: Jul 23, 2026.

Tab guide
- Architecture - stack, active and dormant modules, endpoint map, auth generations, and integrations.
- Screen Inventory - every code-defined screen and reusable component, including reuse counts.
- Mobile Stack - build-ready framework, native bridge, testing, and CI/CD options with current published pricing.
- User Flow - inferred screen-to-screen journeys, with code-backed API and deep-link transitions.
- Data Model & API Gaps - Prisma entities, client/server contract mismatches, and mobile data implications.
- Risks & Open Questions - ranked implementation risks and decisions that must be resolved during refinement.
- Secrets found (review) - file-and-line references only; credential values are intentionally omitted.
- Delivery Plan - four dependent phases across Sprints 1 through 6, ready to mirror into Jira.

--- Google Doc, Delivery Plan tab ---
Delivery Plan

Phase sequencing

Foundation and auth - Sprints 1-2
- Scope: Expo/React Native scaffold, navigation shell, typed networking, secure token storage, JWT login/refresh contract, route guards, environment separation, secret remediation, and legacy-auth decision.
- Done: Android and iOS development builds sign in through the reconciled API, persist/clear credentials securely, gate admin routes, handle expiry, and pass unit/integration tests without embedded credentials.
- Dependencies: none; this phase unblocks all mobile feature work.

Core screens - Sprints 2-4
- Scope: Login, Dashboard, Invoices list/detail/checkout handoff, Settings, Admin reports guard, reusable native design primitives, loading/empty/error states, and reconciled settings/invoice contracts.
- Done: traced web capabilities are represented as tested native screens; invoice data is API-backed; CTAs navigate; settings persist; role behavior is enforced by both client routing and server policy.
- Dependencies: Foundation and auth.

Notifications and analytics - Sprints 4-5
- Scope: notification preferences, push installation registration, feature-flag behavior, APNs/FCM bridge, PostHog event plan, Sentry activation, Stripe checkout deep links, and privacy/consent controls.
- Done: opt-in preferences persist; push tokens register by environment; success/cancel links reconcile checkout; analytics and errors are validated without sensitive payloads; disabled flags fail safely.
- Dependencies: Foundation and auth; Core screens for end-to-end journeys.

Testing and release - Sprints 5-6
- Scope: unit/component/API-contract coverage, Maestro critical flows, optional BrowserStack device matrix, EAS or Codemagic pipeline, signing, store metadata, staged rollout, observability checks, rollback, and runbook.
- Done: CI builds both platforms from a clean checkout, required tests gate merges, release candidates install on representative devices, store submissions are reproducible, and launch/rollback ownership is documented.
- Dependencies: all preceding phases.

Sprint map
- Sprint 1 - repository and app foundation; auth contract and secret remediation.
- Sprint 2 - auth completion, navigation, shared primitives, and first Dashboard/Login slice.
- Sprint 3 - invoices and settings data flows.
- Sprint 4 - remaining core screens, admin policy, checkout handoff, and notification foundations.
- Sprint 5 - push, analytics, observability, deep-link hardening, and broad test automation.
- Sprint 6 - device matrix, release pipeline, store submission rehearsal, rollout, and runbook.

--- Google Doc, Secrets found (review) tab ---
Secrets found (review)

Handling rule
Values are intentionally omitted. Review and rotate or remove any credential-like material; confirm whether each entry is a fixture, placeholder, or active secret before mobile work begins.

Locations
- .env.example lines 1-3 - credential/key placeholders are present.
- src/config/cloud.ts line 2 - credential-shaped access identifier is committed.
- src/services/notifications.ts line 3 - encoded bootstrap/proof material is committed.
- server/routes/auth.ts line 8 - private signing-key fallback is embedded.
- server/routes/auth.ts line 12 - token-shaped refresh response is embedded.
- server/middleware/requireAuth.ts line 7 - public verification-key fallback is embedded.
- server/auth/legacySession.ts line 6 - legacy cookie-key fallback is embedded.

Required remediation before mobile builds
- Remove committed secret material and invalidate any value that may have been active.
- Replace fallback credentials with startup validation that fails closed outside an explicit local-test environment.
- Store mobile build and runtime secrets in scoped CI/CD environments; separate development, preview, and production.
- Add secret scanning and history scanning to pull-request and release gates.

--- Google Doc, Mobile Stack tab ---
Mobile Stack

Recommended baseline (inferred)
Use Expo with React Native and TypeScript, Expo Router, Expo Modules API, Maestro CLI, and EAS Production. This preserves the codebase's React/TypeScript skills and service-layer concepts while replacing DOM components with native primitives. Estimated platform/tooling base: about $199/month before optional real-device testing, store fees, and usage overages.

Cross-platform framework options
- Expo + React Native (recommended, inferred): Expo open-source framework, $0/month. Fit: closest skill and type-system match to Next/React/TypeScript; Expo Router can mirror route groups. Trade-off: existing HTML elements and Next server components are not directly reusable, so screens and navigation must be rebuilt with native primitives. Source: Expo FAQ.
- Flutter: Flutter open-source SDK, $0/month. Fit: strong native rendering and consistent cross-platform UI. Trade-off: requires a Dart rewrite of screens, services, types, and test assets, yielding less direct reuse from this React/TypeScript repository. Source: Flutter FAQ.

Native bridge options
- Expo Modules API (recommended, inferred): Expo open-source tooling, $0/month. Fit: Swift/Kotlin modules with low boilerplate, New Architecture support, and comparable performance to TurboModules. Best for push installation, secure storage, and payment/deep-link hooks. Trade-off: adds an Expo package dependency. Source: Expo Modules API overview.
- React Native TurboModules: React Native open-source architecture, $0/month. Fit: lower-level path and preferable when C++ access is required. Trade-off: more code generation and native build complexity than Expo Modules for this app's modest bridge needs. Source: Expo Modules API overview.

Testing tool options
- Maestro CLI (recommended first layer): open-source CLI, $0/month. Fit: cross-platform YAML flows for login, invoice, settings, deep-link, and feature-flag journeys; suitable for emulator/simulator CI. Trade-off: local device management remains the team's responsibility and real-device coverage is not included. Source: Maestro CLI overview.
- BrowserStack Device Cloud: Device Cloud, $199/month billed annually for one parallel test. Fit: real iOS/Android coverage and device-specific payment, biometric, locale, and interruption scenarios. Trade-off: material recurring cost and a one-parallel bottleneck at the priced tier. Source: BrowserStack pricing.

CI/CD pipeline options
- Expo EAS Production (recommended for launch): Production, $199/month plus additional usage. Includes $225 build credit, two concurrencies, 50K update MAUs, and priority support. Fit: lowest integration burden for Expo builds, signing, store submission, updates, and workflows. Source: Expo pricing.
- Codemagic Teams Pay as you go: Teams Pay as you go, rough monthly cost about $95/month for an assumed 1,000 macOS M2 build minutes at $0.095/minute; actual cost varies with usage. Fit: vendor-neutral mobile CI/CD with macOS, Linux, Windows, team members, and 60-day artifacts. Trade-off: pipeline, credentials, and update distribution need more assembly than EAS. Source: Codemagic pricing.

Cost envelope (inferred)
- Build-ready baseline: Expo/React Native $0 + Expo Modules $0 + Maestro CLI $0 + EAS Production $199 = about $199/month.
- With BrowserStack Device Cloud: about $398/month before EAS overages, taxes, Apple/Google developer fees, and observability usage.
- Lower-cost pilot: EAS Starter is $19/month with $45 build credit, but it lacks the Production tier's two concurrencies and larger team allowances, suitable only for the first implementation spike.

Current published pricing sources
Expo FAQ, Flutter FAQ, Expo Modules API overview, Maestro CLI overview, BrowserStack pricing, Expo pricing, Codemagic pricing (seven linked sources).

Decision matrix
Category | Option/tier | Monthly cost | Decision signal
Framework | Expo + React Native, open source | $0 | Recommended: highest React/TypeScript fit
Framework | Flutter, open source | $0 | Strong UI, full Dart rewrite
Native bridge | Expo Modules API, open source | $0 | Recommended: low boilerplate
Native bridge | TurboModules, open source | $0 | Use when C++ or lower-level access is required
Testing | Maestro CLI, open source | $0 | Recommended first automation layer
Testing | BrowserStack Device Cloud | $199/mo billed annually | Add real-device coverage
CI/CD | EAS Production | $199/mo + usage | Recommended for Expo launch
CI/CD | Codemagic Teams Pay as you go | about $95/mo at 1,000 M2 min | Vendor-neutral alternative

--- Jira MBTF-75, "Foundation and auth" ---
Status: To Do
Reporter: Kashyap Empiric / Assignee: Unassigned

Description
Phase goal
Create the cross-platform foundation and replace the fixture-grade authentication path with a buildable mobile security model.

Sprint span
Sprints 1-2.

In scope
- Expo/React Native TypeScript scaffold and navigation shell.
- Typed API client, environment separation, and secure device storage.
- Reconciled JWT login and refresh contract, expiry handling, sign-out, and route guards.
- Client and server admin authorization behavior.
- Credential remediation and CI secret boundaries.
- Decision and migration plan for the live legacy cookie-session endpoints.

Dependencies
None. This phase unblocks all later mobile work.

Done means
- Android and iOS development builds install from a clean checkout.
- Login, refresh, expiry, and logout work against the reconciled contract.
- Credentials are stored securely and no credential value is embedded in source.
- User/admin routes are guarded and server authorization is test-covered.
- The legacy-auth support or retirement decision is documented and actionable.

Relevant blueprint tabs
Overview; Architecture; Mobile Stack; Data Model & API Gaps; Secrets found (review); Delivery Plan.

Attachment: Mobile Build Blueprint - Foundation and auth.md

Source blueprint
Mobile Build Blueprint - webapp-main
Source commit: 368cec4aff9f293a2564eb6c35f3d9045b343c2c

Keep this issue in To Do until the draft is reviewed.

--- Jira MBTF-75 attachment file, "Mobile Build Blueprint - Foundation and auth.md" ---
# Mobile Build Blueprint - Foundation and auth

Source Google Doc: [link]
Source commit: 368cec4aff9f293a2564eb6c35f3d9045b343c2c
Relevant native tabs: Overview; Architecture; Mobile Stack; Data Model & API Gaps; Secrets found (review); Delivery Plan.

## Overview
The reviewed snapshot is the latest main-branch commit at or before 10 July 2026, 18:00 IST. Static review only; the app was not run and no live application endpoints were called.

## Architecture
- Next.js 15.4, React 19.1, TypeScript 5.8, Express 5.1, Prisma/PostgreSQL, Vitest.
- Current JWT flow: /api/auth/login, /api/auth/refresh, and Bearer verification in server/middleware/requireAuth.ts.
- Legacy cookie-session endpoints remain mounted at /api/legacy/profile and /api/legacy/logout.
- Role assignment is fixture-grade and the Admin reports page performs only a component-level role check.

## Mobile Stack
- Recommended (inferred): Expo + React Native + TypeScript, Expo Router, Expo Modules API.
- Framework cost: Expo open-source tier, $0/month; Flutter open-source SDK, $0/month.
- Bridge cost: Expo Modules API or React Native TurboModules, both open-source at $0/month.
- Recommended launch CI/CD: EAS Production, $199/month plus usage.

## Data Model & API Gaps
- Models: User, Invoice, NotificationSetting in packages/data/prisma/schema.prisma.
- PUT /api/settings and POST /api/notifications/installations are called by clients but not registered by the server.
- JWT refresh returns a fixed fixture token; persistence is not wired to Prisma.

## Secrets found (review)
Values intentionally omitted. Review .env.example lines 1-3, src/config/cloud.ts line 2, src/services/notifications.ts line 3, server/routes/auth.ts lines 8 and 12, server/middleware/requireAuth.ts line 7, and server/auth/legacySession.ts line 6.

--- Jira MBTF-80, "Testing and release" ---
Status: To Do
Reporter: Kashyap Empiric / Assignee: Unassigned

Description
Phase goal
Make both mobile platforms reproducibly testable, signable, distributable, observable, and reversible.

Sprint span
Sprints 5-6.

In scope
- Unit, component, and API-contract coverage.
- Maestro critical-flow automation and optional BrowserStack real-device matrix.
- EAS Production or Codemagic pipeline, signing, environment promotion, and artifact retention.
- Store metadata, privacy declarations, staged rollout, launch monitoring, rollback, and runbook.
- Final secret and dependency scanning gates.

Dependencies
Foundation and auth; Core screens; Notifications and analytics.

Done means
- CI produces signed Android and iOS release candidates from a clean checkout.
- Required tests gate merges and release promotion.
- Critical journeys pass on representative OS/device combinations.
- Store submissions and environment promotion are reproducible.
- Launch, monitoring, rollback, and incident ownership are documented and rehearsed.

Relevant blueprint tabs
Mobile Stack; User Flow; Risks & Open Questions; Secrets found (review); Delivery Plan.

Attachment: Mobile Build Blueprint - Testing and release.md

Source blueprint
Mobile Build Blueprint - webapp-main
Source commit: 368cec4aff9f293a2564eb6c35f3d9045b343c2c

Keep this issue in To Do until the draft is reviewed.

