# Mindspace development progress

[Overview](README.md) · [Client inventory](CLIENT_FEATURES.md) · [Server inventory](SERVER_FEATURES.md)

## October 31 2026 — Keep Task notes through interruptions

Task notes now keep an unfinished title and writing together. Closing the drawer, reloading or returning in another browser can restore the draft; uploading account recovery remains separate from saving the Task itself. Save and Clear send only the fields the user changed through the existing ordered Task save system. Discard leaves the saved Task alone.

Older saves and recovery cleanup preserve newer typing. A confirmed Task receipt finishes its local recovery checkpoint before cleanup begins. Changes to another Task field are retained, and replacing a changed field or a competing recovery copy requires review. If an uncertain save already reached the server, matching recovery can be cleared without sending the Task update again.

The drawer has compact fixed action areas and a scrollable writing area, shared voice input, and 44px controls for coarse pointers. Multiline writing retains its line breaks and spacing through save, reload and further typing. Viewport resizing preserves the draft and keeps the full action buttons visible.

Local acceptance covers 144 source-browser and 220 compiled-client checks across Chrome, Firefox, tablet Safari and phone profiles: 364 passes without retries or skips. All 2,289 client unit checks, release lint and production/font/artifact checks pass. Browser journeys use isolated API fixtures; backend source is unchanged. Deployment, physical LG V60 testing and the wider release gates remain separate. Nested Task relationships, remaining inline consumers, safe table sorting and larger-board admission remain open.

## October 31 2026 — Edit tasks without losing your place

Task titles and text details now respond immediately while typing. Enter or leaving a field sends one small update; multiline fields use Ctrl/Cmd+Enter so ordinary Enter can add a new line. Grouping by the edited field keeps the input in place while it is focused. Later edits continue through the existing ordered save system behind earlier drag saves.

Unfinished edits use the existing protected device recovery system. Failed saves, reloads and changing view tabs retain the text. Escape preserves the cancellation before cleanup, and a failed recovery save can be retried without retyping. Older confirmations keep newer typing. Separate tabs and saved values that changed elsewhere require an explicit choice before overwriting. Structured fields retain invalid JSON for correction and preserve zero and false values.

Local acceptance covers 68 source-browser and 148 compiled-client checks across desktop, Firefox, tablet and phone profiles: 216 passes without retries or skips. This combines 200 unchanged cases from the full browser matrix with 16 fresh storage/cleanup checks after a final recovery-button correction. All 2,263 client unit checks, release lint and production/font/artifact checks pass. Compiled checks also cover existing capture, completion, dates, notes, position and drag controls. Browser journeys use isolated API fixtures. Backend code is unchanged; earlier database checks remain separate evidence.

The changes are in the local preview and remain undeployed. Nested Task relationships, longer notes drafts, safe Table sorting, larger workloads, whole-move transactions and ordering across devices remain open.

## October 31 2026 — Capture tasks with a clear destination

Data Table New task and group Add task now open the shared editor before saving. Empty tables offer the same capture path. The editor shows the destination list and group, retains the selected status/priority/difficulty context and asks for a choice when a group allows several values. Changing the list clears the old group; choosing a real group uses its parent list.

Drafts retain their destination and authored details through closing, reload, account/workspace switches and account recovery. An unconfirmed save keeps its original task details and retry identity until it is resolved; Close and keep draft preserves that attempt. Reminder timing can still be reviewed. An explicit server refusal of a destination leaves the draft editable for correction.

The server validates new list/group assignments and the Group parent in the creation transaction. A confirmed retry returns the canonical task before validating a now-retired destination. Tasks remain unlimited. Broader Task relationship/update audits and the index rollout remain open.

The Task editor now keeps its header and save controls visible around one scrollable form body, including recovery messages. Phone and desktop geometry checks prevent form fields from overlapping the footer.

Final local acceptance includes 51 source-browser and 118 compiled-client checks, 2,223 client and 1,057 server unit checks, release lint and production/font/artifact checks. A separate real disposable-database probe passes 29 checks and leaves no records behind. Browser journeys use isolated API fixtures. Desktop and phone editor captures were reviewed.

The local preview is refreshed; application source remains local and undeployed. Nested relationships, inline editing/drafts, safe Table sorting and larger workloads remain on the active phase list.

## October 31 2026 — More room for tasks and clearer controls

Data Table rows now give task titles room to be read. Expansion, dragging, completion and reminders stay beside the task; pinning, notes, deletion and position commands are in More. Fields that do not fit remain in expandable details. Dates open a compact editor with Save, Cancel and Clear, and a refused save keeps the edit available. Status and other choice fields use readable labels, including older saved status names.

Completion updates the matching status and remains confirmed by the server. Notes edits send only changed fields, so they do not resend an older drag position. Up, down and position commands use the same save/recovery owner as dragging and update neighboring positions. Ordinary task confirmation now updates local records once.

Development acceptance covers 104 source-browser cases and 48 fresh compiled-client cases across four profiles: 152 passes without retries or skips. The source count combines 92 unchanged passing cases and 12 rechecks after the label refinement. All 2,207 client unit checks, release lint and production/font/artifact checks pass. Desktop and phone captures were reviewed. Backend code is unchanged; earlier server/database evidence is retained separately.

The preview has these changes; application source remains local and undeployed. Data Table creation with the shared editor, nested relationships, inline editing/drafts, safe Table sorting and larger workloads remain open.

## October 31 2026 — Reliable Data Table moves and later edits

Data Table dragging now shares the existing ordered save and recovery system with the other Task views. Moves retain hidden Tasks, save the displayed order and update the real list/group relationships. Status and real group/list drops change the intended fields; ambiguous group rules offer a choice, and Cancel leaves the task alone. Other property groups remain available for browsing and within-group reordering. Failed or partly saved moves recover after reload with explicit Retry.

Later task edits wait behind an earlier save while the input stays usable. An older response preserves newer field changes. The row Edit button opens its existing details instead of submitting an unchanged task. The server now validates list-only destinations and clears old group membership; a real group still determines its parent list.

Development acceptance covers 156 source-browser and 80 compiled-client cases across four profiles: 236 passes without retries or skips. All 2,202 client and 1,052 server unit checks pass, along with release lint and production/font/artifact checks. A separate real disposable-database probe passes 24 checks and leaves no records behind. Source acceptance combines 148 retained cases with eight driver rechecks; compiled acceptance combines 76 retained cases with four pointer-state rechecks. Browser journeys use isolated API fixtures; they remain distinct from database acceptance.

The local preview has been refreshed. Application source remains local and undeployed. Safe Table sorting, the compact action/date strip, completion/create/nested controls, larger workloads, whole-move transactions and ordering across devices remain open. Tasks remain unlimited.

## October 31 2026 — Independent Task views and usable details

Table group disclosure, Detailed grouping/filtering/sorting and Data Table options now belong to each view tab. Opening another tab keeps the shared Tasks loaded and leaves the first tab's choices intact. Detailed grouping changes the displayed groups and counts. Row details have working layout choices, fit the visible area and recover safely during loading; phone fields use a single column. Ordinary reloads retain current account-bound presentation, with the saved preset available from the account.

Current development acceptance includes 100 compiled Task/preset cases across four browser profiles and eight Settings journeys, all without retries or skips. All 2,187 client unit tests, release lint and production/font/artifact checks pass. Earlier 100 source Task cases are retained separately; the initial wider source run contained a stale reset-test failure and 12 desktop-only skips. Account-preset browser journeys use isolated API fixtures; the backend is unchanged.

The application changes are local and have not been deployed. Safe Table sorting, the older Data Table drag-saving path, other nested settings, representative latency and larger workloads remain open.

## October 31 2026 — Clear recovery progress before Retry

Task and column Retry now waits for the restored recovery copy to finish loading or saving. Progress and recovery-save failures explain why it is unavailable. The queue guard and visible controls use the same readiness rule, published before the controls appear. Once the exact copy is confirmed, Retry can update the pending intent without creating an unnecessary choice between older copies. Genuine independent drafts retain their protection, and immediate drag saves keep their responsive path.

Development acceptance covers 152 source-browser and 120 compiled-client cases across four profiles: 272 passes without retries or skips. All 2,172 client unit tests, 88 focused contracts, release lint and production/font/artifact checks pass. Actual browser storage locks are held across two reload stages for Tasks and columns, including refused saves and conflicts. Ordinary retry journeys need no extra copy choices or recovery-save clicks. Server source and checkpoint format are unchanged; earlier database checks remain separate evidence.

The preview is healthy. Application deployment, physical-device acceptance, independent Table/Detailed/Data Table settings, representative responsiveness and larger aggregate workloads remain open.

## October 31 2026 — Task retry confirmations

When Retry finds that a move is already saved, that row now leaves Sync Queue even if another row's write fails. Only the remaining change stays queued, with a refused save and a server conflict kept distinct. Reload and another successful Retry preserve the saved order without resending the confirmed row.

Development acceptance covers 136 source-browser and 104 compiled-client cases across four profiles: 240 passes without retries or skips. All 2,164 client unit tests, 80 focused contracts, release lint and production/font/artifact checks pass. Captured writes shrink from two rows to one, and only that remaining row is checked on the next return. Server source is unchanged; earlier database checks remain separate evidence. Application deployment and physical-device acceptance remain open.

Very fast repeated reloads can still require an unnecessary recovery-copy choice, and an early Retry can appear available before recovery persistence has settled. The verified journey completes any visible copy/save steps first. Reducing those prompts and aligning button readiness remain open work, alongside independent view settings, representative latency, larger batches and cross-device recovery.

## October 31 2026 — Task move recovery after reload

Unsaved Task and column moves now have a protected copy on the device. Returning to the original account and workspace restores the pending changes for explicit Retry. Retry checks only the affected server records first; it can recognize a fully saved uncertain move without writing again. A delayed check cannot send an obsolete move or replace a newer record. Competing tabs keep separate recovery copies until the user chooses, and storage failures stay visible and retryable.

The server metadata read is limited to 500 requested IDs, checks workspace access and excludes record bodies. It applies the same schema defaults as ordinary reads, so older records do not create false conflicts. No stored data is migrated.

Local acceptance covers 180 source-browser and 164 compiled-client cases across four profiles: 344 passes without retries or skips. All 2,146 client and 1,042 server unit tests, 19 isolated database/API checks with zero residue, release lint and production/font/artifact checks pass. The preview has been refreshed to load the new endpoint.

Pending recovery copies remain on this device. A mixed-result follow-up remains: when a canonical check confirms one row but another write fails, the confirmed row is still labelled failed even though it is not sent again. Larger batches, the older basic-list adapter, whole-move transactions, ordering across devices, application deployment and physical-device acceptance remain open.

## October 31 2026 — Direct drag retry

Refused or partially saved Task and column moves now retain only their unconfirmed changes in the existing Sync Queue. Retry updates the board using confirmed records. A late response cannot consume a newer move, and a failed later move rolls back to the last confirmed save. Newer confirmed titles survive retry; a conflicting position stays queued for review while an unaffected row can save.

Local acceptance includes 128 source-browser and 112 compiled-client cases across four profiles: 240 passes without retries or skips. All 2,127 client unit tests, 34 focused contracts, release lint and production/font/artifact checks pass. Captured writes confirm that only unconfirmed rows are retried. The batch endpoints and server source are unchanged; earlier isolated database results remain separate evidence.

This recovery currently lasts for the open session. Protected recovery through reload and account/workspace return, the older basic-list adapter, larger aggregate workloads and whole-move/cross-device concurrency remain open. Application deployment and physical-device acceptance remain separate gates.

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
