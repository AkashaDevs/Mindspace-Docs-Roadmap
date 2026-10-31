# Mindspace development progress

[Overview](README.md) · [Client inventory](CLIENT_FEATURES.md) · [Server inventory](SERVER_FEATURES.md)

## October 31 2026 — Safe completion replay

Retrying an already completed Task move now preserves its existing finish time and avoids artificial progress events while still saving position and criteria changes. Reopening clears the finish time; completing again gets a new server time. The mutation keeps schema validation and workspace authorization, including when its state condition changes during the write.

Development acceptance includes all 1,036 server unit tests, 34 focused contracts and 14 authenticated checks against an isolated disposable database, with zero test residue. Six concurrent completed replays preserve time and progress counts. The authorization check exercises completion criteria across workspaces. Frontend source/build are unchanged; earlier browser evidence remains recorded separately. The local preview has been restarted to load this fix.

Direct drag failure capture, protected persistence and explicit retry through reload remain open, along with the older adapter, larger workloads and whole-move transactions. Hosted application deployment remains a separate gate.

## October 31 2026 — Task save ordering and retry feedback

Repeated Task and column moves now save in order through the shared update-queue owner. The board still responds immediately while a previous request is pending. Task reorder and group batch routes share execution order for the captured account and workspace, whether called by a drag or the background queue. Switching workspace retires waiting requests, including a switch away and back.

Confirmed queued Task and column saves also update the visible board immediately after Retry. Partial responses update confirmed records while preserving other loaded data. A late response preserves newer Task edits and does not publish into a retired workspace.

The original rapid-move cases restored obsolete positions after reload when an earlier save was delayed. Retry also cleared the queue without showing the confirmed changes. Latest local acceptance covers 96 source-browser and 88 compiled-browser cases across four profiles: 184 passes without retries or skips. All 2,116 client unit tests, release lint, production, font and artifact checks pass. This change adds no server code; earlier isolated database persistence checks remain recorded separately.

Retained retry for partially saved direct moves, transactions for a whole move, coordination across devices, larger aggregate workloads and the older basic-list adapter remain open. Application deployment and physical-device acceptance remain separate.

## October 31 2026 — Task column ordering

Moving a visible column now includes affected hidden columns in the saved order and preserves other Todo lists. Column saves send only position changes. A failed column save keeps Task edits completed while it was running. Responses to earlier column saves cannot restore data after a workspace change. Partial saves retain confirmed positions and show a message for the remaining work. Moving the first column beside Uncategorized leaves the logical order unchanged and makes no save request.

Local acceptance covers 64 source-browser cases, 52 compiled regressions and 16 compiled column cases: 132 passes across four profiles without retries or skips. All 2,105 client unit tests, release lint, production, font and artifact checks pass. The public inventory records local development verification; application deployment and physical-device acceptance remain separate.

Rapid repeated direct moves, retry for partially saved direct moves, transactions for a whole move, larger aggregate workloads and the older basic-list drag adapter remain open.

## October 31 2026 — Queued save recovery

Background queued saves retain edits made while an earlier save is running. Discarded local queue entries stay removed. Queued Task and group batches also retain unconfirmed items after partial responses, allowing an explicit retry to send only the remaining work. Task reorder payloads preserve ungrouping and the fields required by automatic groups; the server controls completion timestamps.

Development acceptance includes 96 browser cases across four profiles, all 2,099 client unit tests, 21 focused server tests and ten checks against an isolated disposable database. The browser evidence captures the initial batch, refused retry and successful retry. Production, font and artifact checks pass. These are local development results; hosted deployment and physical-device acceptance remain separate.

Whole-move transactions, rapid repeated direct drags, hidden-column ordering and remaining Task adapters stay open. Task dragging continues through its existing immediate batch routes.

## October 31 2026 — Task Calendar views

Each Calendar tab now retains its own month, timeline date, month/day mode, selected-day focus and applied text filters. The existing account preset restores those settings. Text filters now affect the visible Tasks within the selected Todo list; changing or removing a rule uses the already loaded records. Switching between mounted Calendar tabs also retains unfinished filter input.

Date navigation handles month-end choices, leap years and local calendar days. Date selectors and primary actions wrap to fit the available space, keeping Day, Add Filter and Add Task visible on smaller screens. Filter chips and the editor stay within their container.

Local acceptance covers 52 source-browser and 52 isolated compiled-client cases across Chromium, Firefox, tablet Safari and mobile Chrome profiles: 104 passes without retries or skips. All 2,088 client unit tests, release lint, production, font and artifact checks pass. Compiled desktop and mobile images were reviewed. This slice changes no server functionality; the earlier server settings proof remains a separate result.

Table/Detailed expansion and sorting, DataTable filters/grouping, other nested settings, broader Task drag and long-session responsiveness, and compact table controls remain open. Browser profiles do not establish physical-device performance. These results describe local implementation; application deployment and provider acceptance remain separate.

## October 31 2026 — Task tabs and list tools

Task tabs can now hold several instances of the same view type. Each has its own name, pin and position, and Kanban instances keep separate zoom and hidden-group settings. Keyboard selection and browser history retain the selected instance. The account preset restores after browser settings are removed; failed or unconfirmed saves keep the tabs available for retry, and a delayed save does not replace newer local changes.

A visible Lists control opens the existing list tools on desktop and the left drawer on mobile. Selecting a list and switching views preserve loaded Task records without fetching the collections again. Partial settings saves now preserve unrelated preferences and concurrent distinct-category updates; explicit reset remains available. A disposable development-account probe verified the real save/reload/reset path and canonical/legacy agreement.

Local acceptance includes 32 Task-instance source-browser cases, 32 isolated compiled-client cases, 20 retained interaction checks, eight compiled list-switch cases and four source context-stability checks: 96 passes without retries or skips. All 2,083 client and 1,028 server unit tests pass, along with release lint, production, font and artifact checks. The 20/160-Tasks-per-list Chromium benchmark remains within its existing 300/600ms limits; these measurements do not establish universal responsiveness or physical-phone performance.

Remaining Task work includes independent dates/modes, expansion, sorting and filter settings for the other lenses, broader drag and long-session responsiveness, and compact header/table presentation. Planner quick Event capture follows in the visible-work sequence. These results describe local implementation; application deployment and provider acceptance remain separate.

## October 28 2026

Header notifications now open their own detail view. An explicit related-item button preserves the direct path to the associated Note, Task or other source. Both the header and details lead to the full history table through guarded navigation.

Details read the authorized record, offer inline retry after failure and keep history available when a notification is missing. Opening status changes after server confirmation, rather than showing an optimistic or stale label. Development remounts share the pending read. The summary uses readable labels instead of raw document identifiers.

The development acceptance covers 32 source-browser cases, 32 isolated compiled-client cases and 17 retained source/snooze/history/capture checks. Three existing profile skips belong to the older Chromium-only Quick Jot test; its active case now also checks both new navigation actions with an unsaved thought. All 2,080 client unit tests and 22 focused server authorization tests pass. Production, font and artifact checks pass. These are local development results; deployment and actual device/provider delivery remain separate.

Next are the Task view/list journey, remaining perceived lag, independent view tabs and compact Planner Event capture. Broader notification presentation and production-scale history/data handling remain open.

## October 26 2026

The roadmap now separates client features from server capabilities, marks verified implementation with checked and struck-through items, and leaves unfinished work open. The next delivery pass puts visible navigation, Task, Planner, notification and dashboard improvements first.

Recent verified development work:

- Background refresh retains loaded Tasks, navigation and Scratchpad capture. Retry survives closing and reopening page tools; old workspace reads cannot undo a confirmed switch.
- Unfinished Task edits retain authored changes while refreshed records arrive. Newly recovered edits apply changed fields to fresh records.
- Virtualized Task tables keep a bounded row window. The original 480-occurrence traversal passes across Chromium, Firefox, tablet Safari and mobile Chrome profiles without scroll-triggered data reads.
- Stat capture stays available while secondary controls load. Sidebar saves and edits use confirmed records and preserve optional context.
- Signup animation and CAPTCHA lifetime corrections retain usable inputs and recovery under controlled slow/failure conditions.

The latest refresh slice passed 84 source-browser and 48 compiled-client cases. The client unit suite passed 2,079 tests. These results describe the tested development candidate. Phone browser profiles do not certify a physical device, and provider fixtures do not certify a current deployment.

The interview feedback stays open where journeys remain unclear or responsiveness feels poor. Task list switching and dragging need further practical acceptance. Orion, Notes loading and richer charting are not declared finished.

## October 19 2026

- Added configurable Task tabs and a saved preset, Kanban zoom/column heights, retained list selection, compact Notes capture and Journal layouts with Markdown previews.
- Persisted automatic Task-group rules and distinguished overlapping card occurrences.
- Added database-backed Todo list/group capacity, usage feedback and recoverable creation with controlled independent-backend database proof.
- Extended billing/payment and observed subscription history, retaining separate rollout and provider acceptance gates.

## Earlier foundations

The core Task, Planner, Notes, Habit, Goal, Reminder, Journal, Stats, workspace, account and shared-action systems are implemented. Earlier candidates have hosted Stripe sandbox evidence for renewal, payment recovery, cancellation, downgrade and cleanup. That history supports current release checks rather than certifying all new work as deployed.

The inventories carry forward useful unfinished roadmap requests. Superseded implementation details and unrelated personal notes are removed from the public presentation. Offline-only operation and content encryption remain investigations.
