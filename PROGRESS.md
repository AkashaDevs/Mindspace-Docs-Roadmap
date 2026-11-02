# Mindspace development progress

[Overview](README.md) · [Client inventory](CLIENT_FEATURES.md) · [Server inventory](SERVER_FEATURES.md)

## November 1 2026 - Native Task saves verified against the real API

The compiled Task UI now has a positive native parent/position save verified through actual signup/login, the normal mounted server and Mongo. Desktop and phone Chrome each use a fresh, initially empty owned database. The browser sends one minimal child/affected-parent batch, reloads and explicitly refreshes canonical Tasks; independent database checks confirm parent/mirror, positions, list/group membership and preserved authored text/completion date. Both databases are cleared afterward. No frontend Task seed or synthesized API payload is used.

Those runs exposed a startup health defect: an unmounted fallback could return 404, and HTTP 200 could incorrectly imply that a disconnected database was online. The shared HTTP probe now reads API/database status together from the mounted /api/health route, uses the configured API origin, preserves maintenance state and aborts a stalled request after five seconds. The old archived build fails the same canonical-health assertion; the new build passes both real-API journeys with 97 API responses, no HTTP failures and no page errors.

Current validation passes 2,404 client checks, 237 focused checks, release lint with zero errors and the existing 21 warnings, plus production/font/artifact audits. Native hierarchy regressions pass 8 source and 32 compiled browser cases across four compiled profiles; two source connectivity cases and 12 separate compiled isolation controls also pass. The skipped source-only isolation invocation is excluded. Earlier failed pilots and their corrected test assumptions remain recorded. The candidate freezes 2,885 client inputs, 574 server inputs and 516 build files. Existing server runtime modules are unchanged; prior 1,110 server checks are retained, not claimed as rerun.

The compiled UI reaches the owned real server through an explicit loopback forwarding bridge. Production-origin/CORS, Socket.IO/provider acceptance, physical LG V60/touch testing, real Data Table/capture/refused/lost-response journeys, clone/Trash/erasure writers, placement, larger workloads and the wider product/release phase remain open. Application source remains local and existing-user authored data is untouched.

## November 1 2026 - Native Task hierarchy uses the shared save queue

Basic and List hierarchy drags now use minimal batched reorder intent through the existing scoped queue. Changed positions, actual list/group assignment and affected parent order travel together. Hidden children in other lists/groups remain in the parent order; unrelated Task text and completion dates are preserved. The held appearance clears before the network response, so rapid moves can continue and save in order.

Real group drops reuse the existing filter-choice dialog, including cancellation without a save. Empty-group drops, refused-save reload/retry and already-committed lost-response recovery have mounted proof. The shared planner isolates position buckets by list, group and parent, and replaces repeated ancestor scans with indexed lookup. Selected/detail displays resolve current Task records.

The old mounted full-snapshot baseline fails both views as expected. The final candidate passes 2,397 client checks, 227 focused checks, release lint with zero errors and the original 21 warnings, plus production/font/artifact audits. There are 97 distinct accepted browser cases: 27 source and 70 isolated compiled, all with explicit zero-page-error observations. The 40 native hierarchy cases include source and all four compiled profiles. Data Table graph regressions use source plus compiled Chrome/tablet; adjacent List/Basic controls use source plus compiled Chrome/phone. Four additional source recovery rechecks pass with the final test helper. A transient tablet recovery-button race is preserved; the complete fresh tablet graph group supersedes that earlier profile. Saved-state assertions and production bytes remain unchanged. Earlier scope-key, test-target and obsolete-contract failures remain preserved. The frozen candidate has 2,881 client inputs, 573 unchanged server inputs and 516 build files.

Server code is unchanged; prior 1,110 server checks and native graph/reorder transaction evidence are retained rather than claimed as rerun. Browser-to-isolated-real-API proof, other graph writers, creation placement, larger workloads, physical-device acceptance, deployment and the wider product phase remain open. Application source remains local and existing-user authored data is untouched.

## November 1 2026 - Task graph recovery journeys

Data Table detach and reparent journeys now have mounted verification of minimal queued child patches, both canonical parent mirrors, and unchanged actual list/group assignment and content. Refused moves retain their exact queued intent. A committed move whose response was lost is confirmed from saved graph records without sending it again, after an explicit copy choice or recovery-save retry when an immediate reload leaves interrupted protected copies.

A known parent refusal preserves the thought and permits a corrected standalone capture. An uncertain child capture reopens read-only and repeats its exact logical identity and payload, confirming one child and its parent mirror. Legacy reciprocal links render within a finite path, can be detached for repair, and are excluded from invalid ancestor choices.

There are 48 fresh local browser checks: 16 source and 32 isolated compiled cases across Chrome, Firefox, tablet Safari and mobile Chrome. They include the eight new graph journeys and existing capture/draft regressions. All report zero page errors. Earlier failed test assumptions, tablet copy-choice and recovery-save omissions, and Firefox cleanup failures are preserved separately. The complete fresh tablet group replaces the earlier tablet profile; the failed whole run is retained. Test syntax and two controlled-fixture unit checks pass. Application/server sources and all 516 compiled files are byte-identical to the previous verified checkpoint; its 2,388 client and 1,110 server checks, release lint/build and native API evidence are retained rather than claimed as rerun.

Native hierarchy drags still need migration from full-snapshot bulk updates to the shared minimal queued path, including parent-order intent. Other graph writers, browser-to-real-isolated-API proof, creation placement, larger workloads, physical-device acceptance, deployment and the wider product phase remain open. Application source remains local and existing-user authored data is untouched.

## November 1 2026 - Draft comparison and responsive local recovery

Task draft conflict notices now show compact previews of both copies' titles, descriptions and notes before the user chooses. Authored markup remains literal text. The comparison uses the already loaded drafts and the existing recovery notice.

Both local choices now finish if another tab saves a competing copy during an account/workspace change. They stay bound to the original device identity without restarting retired account work. Choosing an unfinished draft during a protected device save now queues the selection rather than dropping it. Untouched blank captures and unchanged drafts no longer send recurring autosaves; explicitly clearing an earlier thought is still protected.

Local verification passes 2,388 client checks, release lint with no errors or added warnings, and production/font/artifact audits. The 116 accepted browser cases comprise 22 source and 94 isolated production-build cases. Comparison, conflict choice, confirmed cleanup and idle-save behavior pass across four profiles; synchronous scope/local-writer and pending-save cases use the source harness. Eight final compiled comparison/picker screenshots were reviewed. The earlier tablet cleanup failure now passes. A browser-cleanup error required a fresh complete Firefox group, which passed; the failed run is preserved. Server sources are unchanged, retaining the previous 1,110 server checks and native graph/reorder evidence.

Mounted detach/reparent/refusal and uncertain child creation, legacy cycles, native hierarchy migration, other graph writers and browser-to-real-isolated-API proof remain open. Creation placement, larger workloads, physical-device acceptance, deployment and the wider product phase remain open. Application source remains local; existing-user authored data is untouched.

## November 1 2026 - Draft choices and interrupted saves

The unfinished Task draft picker preserves different device and account copies until the user chooses one. Both choosing the account version and keeping the device version are verified. Reopening a confirmed child Task's recovery copy finishes cleanup without creating another Task.

An account or workspace change during a draft switch now retires the old account work immediately, even if the user returns to the same IDs before the page renders again. Mindspace finishes protecting the original device copy and closes the interrupted editor. If that device checkpoint fails, its explicit retry stays on the device and does not restart the retired account save. Reopening the protected draft starts a fresh owner.

Local verification passes 2,381 client checks, release lint with no errors or added warnings, and production/font/artifact audits. The 106 current browser cases comprise 16 source and 90 isolated production-build cases. Both conflict choices and confirmed cleanup pass on four profiles; the three synchronous scope/device-storage cases use the source browser harness. Eight compiled conflict/picker screenshots were reviewed. Server sources remain unchanged, retaining the prior 1,110 server checks and native graph/reorder evidence.

Scope retirement combined with a competing local writer still needs a dedicated check. Mounted detach/reparent/refusal and uncertain child creation, legacy cycles, native hierarchy migration, other graph writers and browser-to-real-isolated-API proof remain open. Larger workloads, physical-device acceptance, deployment and the wider product phase also remain open. Application source remains local; existing-user authored data is untouched.

## November 1 2026 - Return to unfinished child thoughts

Child capture now has a compact Unfinished task drafts picker in the existing editor. A unique unfinished child thought returns when its parent has moved between lists. If the parent has disappeared, New task provides a return path and the existing parent field can make the thought a standalone Task. Switching drafts saves the current thought first. Each copy keeps its original device and account identity, including older long account keys; the picker does not merge or overwrite independent copies. The protected draft owner also checkpoints a rapid page interruption before the normal autosave delay.

Direct Retry now reads canonical graph state for a failed hierarchy move even without reloading the page. If the server already committed the move, the queue restores both parent mirrors and settles without sending another move.

Local verification passes 2,381 client checks, release lint with no errors or added warnings, and production/font/artifact audits. The 88 current browser cases include 40 child-capture/draft/Retry journeys, 12 initial subtask controls, 12 graph-confirmation cases and 24 existing capture/queue regressions. Of these, 78 run against the isolated production build. The new journeys cover Chromium, Firefox, tablet Safari and phone Chrome; four compiled draft-picker screenshots were reviewed. Server sources are unchanged from the prior checkpoint, retaining the earlier 1,110 server checks and native graph/reorder evidence.

Mounted detach/reparent/refusal and uncertain child-creation journeys, legacy cycles, concurrent-copy/scope-retirement picker races, native hierarchy migration and other graph-writer audits remain open. Browser-to-real-isolated-API proof, larger workload admission, physical-device checks, deployment and the wider product phase also remain open. Application source remains local; existing-user authored data is untouched.

## November 1 2026 - First subtask controls through shared saves

Data Table's Add New Task entry now opens the existing canonical editor with the actual parent, list and group prefilled. It no longer writes the literal new into a parent mirror. Attaching an existing Task sends one minimal queued child-parent change, preserving that Task's list, group and position. The subtask panel has aligned action headers, a clear empty state and shared relationship choices. The page-level parent-change callback uses the existing save/recovery owner.

Interrupted hierarchy recovery also checks both parents. The bounded authorized endpoint returns requested move fields and graph-only metadata from one read-only snapshot. An already committed reparent can restore both mirrors and settle its queued intent without replaying another write. Ordinary move reads retain their existing fast path.

Local verification passes 2,369 client and 1,110 server checks, release lint and production/font/artifact audits. The 60 current browser cases comprise 24 initial subtask-control cases across four profiles, 12 graph-confirmation cases and 24 existing queue/capture regressions: 14 source and 46 isolated production-build cases. Exact minimal attachment requests, parent prefill and viewport containment pass; four deliberate compiled capture screenshots were reviewed. Native probes pass 14 graph scenarios and 29 reorder compatibility checks, with both owned databases cleared. The development preview was refreshed and its API/database health verified.

This closes the initial capture-launch and attachment defects. Actual child submission and parent-specific draft journeys, mounted detach/reparent/refusal/uncertain recovery, legacy cycles and native hierarchy migration remain open, together with other graph-writer audits. Larger workloads, physical-device checks, deployment and the wider product phase remain open. Application source remains local; existing-user authored data is untouched.

## November 1 2026 - Dependable Task relationship saves

Task relationship APIs now coordinate children and both parent mirrors in the existing transaction owner. They reject cycles and unavailable or cross-workspace parents, and roll accompanying content and positions back together on failure. Creation retries, completed-task finish times and no-op versions stay stable. Permanent deletion detaches surviving children while coordinating the existing creation-retirement receipt; injected failure rolls both back.

The shared client save services now publish related graph confirmations without reloading every Task. Newer text and pending graph intent survive late responses, and older full responses cannot restore stale relationships. Shared move payloads and protected recovery copies can retain parent/mirror intent. Version-aware queue baselines preserve a newer related confirmation when a pending move fails, without consuming that pending revision.

Local acceptance covers 2,356 client and 1,107 server checks, release lint and production/font/artifact audits. The 48 current browser cases include 24 graph-receipt cases across four profiles and 24 existing queue/capture regressions: 14 source and 34 isolated production-build cases. Two older regression tests require development modules and are verified in source. Native API probes pass 13 graph scenarios and 29 existing reorder checks in owned disposable databases; both databases are cleared. Browser transport fixtures remain distinct from the real database API probes.

Native hierarchy callers and visible subtask capture/attach/detach controls still need migration to the shared path. Parent-specific drafts, legacy-cycle rendering, remaining clone/Trash/erasure writers and actual graph UI-to-API acceptance remain open. Creation placement, larger/zoomed workloads, physical-device checks, deployment and the wider product phase remain open. Application source is local and existing-user data is untouched.

## November 1 2026 - Basic grouping that changes the view

Basic's grouping menu now renders saved groups, status, priority, difficulty, tags, assignee, due date and completion. Grouping belongs to each view tab and survives reload and account presets. Date groups follow the current day, and filters keep using loaded Tasks.

Dragging between supported field groups saves through the existing scoped queue, including explicit Retry after a refused save. Actual list/group membership and subtask parent/order references stay intact. Other grouping lenses explain their available actions. Quick touch selections also cancel their context-menu holds across portals, while intentional holds retain their behavior. Tasks can be added with supported group defaults, and Create Group now waits for a confirmed save through the shared page owner.

Local acceptance covers 202 distinct browser cases (72 source and 130 production-build), including four-profile grouping journeys and existing capture/view/layout regressions. All 2,335 client unit checks, release lint and production/font/artifact audits pass. Production-build requests are isolated to the intended compiled app; desktop and phone screenshots were reviewed. Browser API fixtures and pure server settings-bound checks are separate from live database/provider acceptance.

Backend code is unchanged. Broader hierarchy transactions, creation placement/index allocation, larger and zoomed workloads, physical LG V60 checks, deployment and the remaining product phase stay open.

## November 1 2026 - Keep List and Basic views ready to resume

Basic's toolbar now wraps its search, filters and actions within the dashboard. Search, applied filters and group collapse belong to each view tab. List and Basic keep separate detail/subtask expansion through reload and account presets. Filters use retained Tasks, provide a clear way back from empty results, and follow the local day for due dates.

Basic groups now render current saved Task values, including automatic group membership. Structured tags use the shared normalizer. List details open through an explicit action, keeping controls stable during focus and drag pickup; narrow screens use the existing details dialog.

Dragging rows saves the complete position batch and retains list/group membership after reload. A held drag ends when its view or filter context changes; a save already sent can still finish. Local acceptance covers 224 distinct source and production-build browser cases across four profiles, all 2,314 client unit checks, release lint and production/font/artifact audits. Browser journeys use isolated API fixtures; current preset payloads also pass the unchanged pure server settings bounds.

Basic's grouping selector and typed drops, nested relationships, larger workloads, physical LG V60 checks, deployment and the wider phase remain open. Backend code is unchanged; earlier database evidence remains separate.

## November 1 2026 - Capture a Task and find it again

The Table header and group buttons now open the shared new-Task editor with the intended destination. Empty workspaces can capture a first Task without creating a list. Group defaults and required choices use the same editor, and existing Task edits remain ordinary updates.

A compact saved-Task message provides Open task even when the current filters hide the new record. It opens the latest saved values without changing the selected filters, list or view. Drafts survive closing and reloading; uncertain saves retry their original request. If a refresh already loaded a newer version of that Task, the retry preserves it and avoids a duplicate row.

Local acceptance covers 248 distinct source and production-build browser cases across four profiles, all 2,306 client unit checks, release lint and production/font/artifact checks. Existing filtered dragging still saves complete position batches and retains failed batches for Retry. Browser journeys use isolated API fixtures. Backend code is unchanged; physical LG V60 checks, deployment, remaining Task projections and relationships, and the wider phase stay open.

## November 1 2026 - Filter a Task table without losing hidden tasks

Table filters now use the Tasks already loaded in the browser. Each tab keeps its own filters through reload and account presets. Matching counts and Clear filters explain how to return when nothing matches; removing filters restores the retained Tasks.

Dragging filtered rows preserves hidden neighbours, saved positions and actual list/group membership. Failed saves retain their complete batch for Retry. Reload checks confirm the saved order and membership. Changing a filter cancels a held drag while allowing an already sent save to finish. Sorted rows keep their ordinary controls usable, and expanding a row avoids sorting the collection again.

Local acceptance covers 320 distinct source and production-build browser cases across four profiles and all 2,302 client unit checks, plus release lint and production/font/artifact checks. Browser journeys use isolated API fixtures. Backend code is unchanged; earlier database evidence remains separate. A separate check reproduced a Table creation problem, which is next for repair. Physical LG V60 checks, deployment, remaining Task views and the wider phase stay open.

## November 1 2026 - Sort a Task table without changing saved order

Each Table tab now offers field and direction controls for its top-level rows using Tasks already loaded in the browser. Changing sort does not fetch or rewrite Tasks. Tabs retain separate preferences through reload and account presets, and an explicit refresh re-sorts updated saved values.

Manual order returns to positional drag reordering. Automatic sorting explains that mode and prevents ambiguous top-level positional drops; changing the tab, list or sort cancels a held drag. Manual drops retain the existing ordered batch save, including affected neighboring positions and intact list/group membership after reload.

Local validation covers 216 distinct source and production-build browser cases across four profiles, covering sorting and existing Task regressions. All 2,297 client unit checks, release lint and production/font/artifact checks pass. Browser journeys use isolated API fixtures. Backend code is unchanged; application deployment, physical phone checks, remaining Task views and the wider phase stay separate.

## October 31 2026 — Keep literal writing as text

The shared editor was treating literal tags, entities and whitespace-only text as empty HTML. Those entries now remain text through drafting, committing and saving. The real Task notes journey preserves them through closing, reloading, saving and further typing.

Read-only and live text previews show literal text with its spacing. Rich HTML previews retain their formatting through the existing sanitizer. Switching the editor's configured format re-evaluates the content using the appropriate rules.

Local validation passes 184 product-browser checks across source and compiled clients, plus 12 source-only component probes, across four browser profiles. All 2,295 client unit checks, release lint and production/font/artifact checks pass. Browser product journeys use isolated API fixtures. Backend code is unchanged, and the component probe is excluded from the production artifact. Deployment, physical phone checks and the wider phase remain separate.

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
