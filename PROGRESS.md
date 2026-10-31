# Mindspace development progress

[Overview](README.md) · [Client inventory](CLIENT_FEATURES.md) · [Server inventory](SERVER_FEATURES.md)

## October 31 2026

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
