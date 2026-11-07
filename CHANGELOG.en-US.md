# Changelog

[Português (Brasil)](CHANGELOG.md) · [Official releases](https://github.com/FP-SOLU/afluente-releases/releases/latest)

This record describes versioned changes. Release reports retain validation evidence and limits; a fix does not certify every provider or environment.

## 0.6.5 — 2026-11-07

- The updater checks local services before closing the app. Stale records, reused PIDs, unrelated port owners, and unavailable inspections show actionable guidance with the port and conversation environment panel.
- The check does not stop processes or archive records automatically. Unresolved states require review and are not reported as confirmed cleanup.
- Added preparation feedback and protection against concurrent installation attempts.
- Shutdown waits for every resource and persistence operation even when another fails early, and concurrent quit events share one shutdown operation.
- Local shutdown diagnostics retain only fixed stage names and states. Notifications distinguish preview, browser, persistence, and execution failures.
- Added stale-record, identity, port, failed-flush, draft-preservation, and disposable-profile Electron/IPC update regressions.

## 0.6.4 — 2026-11-07

- Replaced the aggregate 4 MiB Codex transport check with incremental per-message framing, a 32 MiB message limit, and intact UTF-8 handling for images and larger responses.
- Process loss before waiter registration now fails explicitly instead of leaving a task waiting indefinitely.
- Execution details retain allowlisted failure codes and descriptions. Unknown failures are no longer attributed to OKF or the network without evidence; private error text and stderr are not stored in history.
- A confirmed terminal transient failure may continue once on the same thread. Authentication, quotas, policies, cancellation, pending decisions, and command/MCP/file-change/image-generation activity in the turn prevent automatic continuation, including completed tools.
- Fixed early notifications received before turn-start responses and late messages from previous turns.
- Added transport, recovery, persistence, and disposable-profile Electron rendering regressions.

## 0.6.3 — 2026-11-06

### Continuity and memory

- Replaced the last-four-tasks excerpt with scoped context selection and access to the complete conversation/project history.
- Added paginated search, chunked source reading, cited checkpoints, and retrieval of original files and images.
- Preserved recent steering and older choices with provenance and task status. Agent notes remain separate from human authorization and approved memory.
- Context credentials follow the session lifecycle and are revoked on completion or cancellation.

### Execution and performance

- Repetition detection uses observed progress and allows a strategy recovery before interrupting persistent repetition.
- Useful work continues beyond seven rounds; progress state is bounded and persisted.
- UI events are coalesced, concurrent history reads share requests, and hidden windows pause visual refreshes until shown again.
- New tasks wait when estimated available memory is insufficient, without cancelling existing work.
- Codex threads are reused within matching agent, project, model, and permission scopes. Cumulative usage becomes per-execution usage; identical attachments are not resent to the same thread.

### Updates and verification

- The updater checks the newest stable version again before installation and invalidates outdated intermediate downloads.
- Installation messages distinguish a newer release, verification failure, and running tasks.
- Added regressions for long history, images, isolation, restart, repetition, memory admission, sessions, and event bursts. A real-provider landing-page exercise and its observed limits are documented in the technical report.

## 0.6.2 — 2026-11-06

- Removed duplicate task-summary and delivery/evidence blocks while retaining execution details.
- Added sequential questions with back navigation, preserved answers, batch submission, and animated confirmation.
- Added official provider icons and refined session/MCP diagnostics and settings alignment.
- Added sidebar Codex/ChatGPT and Claude quotas when exposed by the provider.

## 0.6.1 — 2026-11-06

- Added explicit choices to steer the current task or queue a new request, including Claude.
- Refined chat profiles and background MCP execution.

## 0.6.0 — 2026-11-06

- Expanded the multi-provider experience, onboarding, model selection, integration diagnostics, and local tools.
- Added OKF-independent local knowledge and refined memory, usage, and configuration.

Earlier releases are listed in the [official release archive](https://github.com/FP-SOLU/afluente-releases/releases), with engineering records in `docs/`.

---
**Afluente — by FP Solutions**  
Developed and maintained by FP Solutions.
