# Mindspace development progress

[Overview](README.md) · [Client inventory](CLIENT_FEATURES.md) · [Server inventory](SERVER_FEATURES.md)

## November 7 2026 - Rename in Notes Explorer

The tree and folder listing now share an inline rename field. F2 selects the existing name, and a deliberate second mouse click starts editing. A quick double-click still opens the file.

Save with Enter, by leaving the field, or with the checkmark. Cancel with Escape or X. Shift+Enter adds a line. An unconfirmed save keeps the typed name available to retry. The local production checks cover the tablet touch cancellation race and the adjacent Explorer journeys.

## November 7 2026 - Load Notes Explorer by folder

The local Explorer opens a page of folder metadata and reads the selected file separately. It restores the last folder, open branches and selected file on the same device. The root and first folder page used 7,149 bytes in a 256-file browser fixture.

The browser and production build checks passed locally. The development directory index rollout and the broader drag/drop and rename work remain on the checklist.

## November 7 2026 - Log a Stat from any dashboard

Open the Stat form directly from the desktop header or choose Log a stat in the phone's More dashboard actions menu. The form keeps your place on the current dashboard, and unfinished input can be resumed on the same device. The dashboard shortcut strip also stays behind open dialogs.

The local production build passed 92 browser cases covering Stat capture, the Data Table, sidebar tools and modal actions.

## November 7 2026 - Compact the Stats Data Table

Search, Quick Add and paging stay within reach at phone widths. Rows adapt to the available table space when the sidebars open, and Options keeps filters, entry settings and import and export together.

The local production build passed 20 browser cases. A direct global Stat shortcut remains on the checklist.

## November 7 2026 - Keep the Stats key you type

Enter adds the typed key when the only matches are partial. An exact key still reuses its existing type. The picker also labels the plus action Create data key. The same controls work in the Data Table and global capture.

The local build passed 40 compiled browser cases, eight source cases and 2,508 client checks. The compact table and global capture discovery are the next improvements.

## November 7 2026 - Customize the right sidebar

The right sidebar starts with Today, Tasks, Notes and Stats. Use Customize tools to add, hide or reorder built-in widgets. The device remembers the layout. Today shows open tasks due on the current date, and Stats loads when its tab is opened. The phone drawer has named controls and returns focus to its launcher.

The local build passed the widget checks across four browser profiles. Compact Stats entry and table improvements remain open.

## November 7 2026 - Open relevant dashboard sidebar tools

Todo opens its list tools and Planner opens its Page tools by default. Each dashboard remembers the tab a user chooses. On phones the drawer stays closed until opened. Routes without sidebar content leave out the Page tools tab.

The local build passed 28 production browser cases, 15 source regressions and 2,503 client checks. The right-sidebar widget redesign and compact Stats controls remain open.

## November 7 2026 - Reuse loaded Planner Events

Planner uses its confirmed Event collection to build the upcoming date window. This removes the second range request from the full load. Standalone date-window callers can request overlapping Events and recurring series, then apply the exact selected dates on the client.

The local build passed 64 compiled browser checks, 2,500 client checks and 1,121 server checks. Live verification of the new backend remains open.

## November 7 2026 - Show the right dates in Planner Page tools

Upcoming Events shows later recurring occurrences and Events that continue into the selected dates. Search and sort use the loaded records. Each row shows its schedule and opens the saved Event or series. Returning from that detail keeps the originating Planner page.

The local build passed 56 compiled browser checks and 2,499 client checks. The remaining range API and live recurrence persistence checks are open.

## November 7 2026 - Schedule recurring Planner Events

The candidate saves daily, weekly, monthly and yearly Event series. The shared editor keeps the repeat schedule in an interrupted draft. Scheduler and Planner timelines show occurrences for their current date windows and link back to the saved series. The editor makes it clear that changes apply to the whole series.

The local build passed 84 compiled browser checks, 2,496 client checks and 1,120 server checks. The preview still needs the updated backend before recurrence can be enabled there.

## November 7 2026 - Keep Planner Event dates across timezones

The Planner keeps an all-day Event on its occupied dates when viewed from another timezone. The shared editor uses the Event's timezone for its clock fields. Changing the timezone on a timed Event keeps its scheduled moment. Changing it on an all-day Event keeps its dates.

The editor keeps an invalid timezone or a time skipped by daylight saving available for correction before saving. Scheduler moves keep the all-day Event in its named zone.

The local build passed 114 compiled browser checks and 2,491 client checks. Event recurrence remains open.

## November 7 2026 - Edit all-day Events by occupied date

The Planner now shows the last occupied date in shared editors and saved Event details. Moving the start preserves the number of calendar days through daylight-saving changes. The form leaves a backwards range open for correction.

An unsaved draft remembers the earlier clock times when a timed Event switches to all day, including after a reload. Switching back restores those times on the chosen dates. The saved Event stores its date range without the draft metadata.

The local build passed 92 compiled browser checks across desktop, tablet and phone profiles and 2,489 client checks. Named timezones and recurrence remain open.

## November 7 2026 - Keep Events in the chosen Planner

The Add event button, timeline actions and Scheduler dates now use one destination rule. Planner-only capture uses its sole active Calendar when there is one. Otherwise the form can save directly to the Planner or use a Calendar the user chooses. Changing the Calendar updates its Planner and shows that destination in the form.

A missing or conflicting focus gives the user a way back before capture. An interrupted draft keeps its chosen destination when focus changes. If its Calendar disappears, the title and dates stay in the form while the user picks a new destination or saves without a Calendar.

A recovered device draft is ready to use while its account copy uploads.

The local build passed 80 browser checks across desktop, tablet and phone profiles, plus 2,487 client checks. Broader all-day editing, time zones and recurrence remain open.

## November 7 2026 - Open and return from saved Planner Events

Open a saved Event from Today, Agenda or Scheduler, or choose View Event after capture. The detail page reads the exact Event within the active workspace, including when it falls outside the loaded Planner collection. A failed read offers Retry. An unavailable record still offers a way back.

The detail view shows one schedule line, names the Calendar and Planner when available, and keeps Reminder, edit and delete actions together. The return action restores the Planner page and Calendar focus. Scheduler also keeps the selected day and view.

The local build passed 34 current browser cases and 2,487 client checks. Broader Event authoring for all-day dates, time zones, recurrence and destination scope remains open. The app changes are available in the local preview.

## November 7 2026 - Capture an Event from the Planner calendar

Tap a date or time slot, or drag across a range, to open the same compact form as Add event. The selected date, time and focused Calendar carry into the form. The timeline now leaves space for its timed rows even when the all-day row is empty.

Typing a title and immediately closing or reloading keeps the draft, including its original date. A refused save keeps the form ready to retry. Edits update the saved Event without creating a duplicate, and closing an unchanged Event leaves no draft. A linked Reminder opens after a successful Event creation when requested.

The local candidate passed 165 browser checks across the capture, draft, layout and viewport journeys, plus 2,487 client checks and production artifact checks. Browser profiles include desktop, phone and tablet emulation. The live service has not been updated. The saved Event detail and return journey, broader date and recurrence behavior, and provider verification remain open.

## November 7 2026 - Stable startup viewport and native calendar zoom

The shared document containers now use consistent percentage widths. The compiled phone regression keeps the expected layout and visual viewport through startup, responsive-boundary changes, year navigation and Event dialog dismissal. The header and scheduler controls remain fully onscreen. Short-screen login/signup controls and long public reading retain their interior scrolling.

Planner permits vertical panning and native pinch zoom. A shared multi-pointer activation guard prevents a pinch from opening an Event form or becoming a selection, edit, drop or resize save. Fresh pointer gestures and keyboard/programmatic actions remain available. The native phone input check retains user zoom through real Tab/Enter period navigation, opens no incidental dialog and makes no Event writes. Ordinary one-finger date taps still open the selected day's form.

The final bounded validation passes 144 browser checks: 28 source and 28 compiled layout checks, 14 source and 14 compiled boundary cases, 24 compiled scheduler controls and 36 compiled capture cases. Twelve explicit profile skips reserve the two native-touch cases for the Chromium phone profile. All 2,480 client checks, release lint and production/font/artifact audits pass. There are 102 current-main compiled isolation observations and thirteen current stylesheet observations; no forbidden requests. Backend inputs remain unchanged.

The original viewport and pinch-policy failures are retained. Native gesture checks use a neutral input control and browser-frame-spaced two-finger events; startup layout instrumentation and scroll/zoom resets are absent from the repaired geometry journey. Application changes remain local; physical-device acceptance remains open.

The next Planner work is to unify older day-cell capture with the compact shared Event form and consistent clicked-day/date fields, verify saved Event/detail/return context, and complete broader scope/time/all-day/recurrence journeys. The full consolidation phase remains active.

## November 6 2026 - Readable compact calendar cells and contained shortcuts

Planner month cells separate week-number and day links, wrap Event times and title previews, and retain the full title in the existing editor. Crowded days use FullCalendar's native more popup; selecting one of twelve same-day Events opens the correct record. Native week/day navigation, timelines and event lists remain available without extra collection reads or writes.

The scheduler now has a consistent finite-height contract. A conflicting automatic content-height setting had disabled the library's height-based Event limits. The shared dashboard shortcut panel also hides its collapsed contents from display and keyboard navigation, expands above its toggle within a narrow screen, and labels its controls.

The bounded scope passes 123 browser checks: 24 source and 24 compiled cell/shortcut checks across four browser profiles, 24 compiled scheduler controls, 36 compiled capture checks and 15 existing draft checks. Five original phone-profile recovery skips remain. All 2,473 client checks, release lint and production/font/artifact audits pass. Backend inputs are unchanged; prior 1,118 server checks are retained. Application changes remain local.

A separate compiled phone geometry regression remains open: an initial oversized layout viewport leads to zoom/pan and header clipping after resize/dialog interactions. The shortcut repair does not resolve that symptom. Diagnostic animation-frame reads changed its timing, so that experiment is not acceptance evidence. Shared-shell investigation, saved-Event/detail/return context, scope/time/recurrence journeys, and device/provider/release acceptance continue.

## November 6 2026 - Clearer scheduler controls and date headings

The Planner scheduler now has one compact toolbar with a readable date range, one Today action and Previous/Next period controls. A grouped selector retains all eleven previously exposed layouts and makes three already-configured day/week variants reachable. Go To Date and year jumps remain in secondary controls.

The toolbar uses stable controls and native menu items. Keyboard focus stays on a period button after navigation and returns to the view selector after selection. The calendar and selector use the same view registry. Switching all fourteen layouts makes no extra Planner collection reads or writes.

Visual review found an additional built-in toolbar and month columns displaying misleading January dates. Both have explicit browser regressions: the duplicate vendor header is disabled, month/year/multi-month layouts use weekday headings, and weekly layouts retain their actual dates.

The final local candidate passes 147 browser checks: 24 source and 24 compiled scheduler cases, 36 source and 36 compiled capture cases, 15 existing draft checks, eight readiness checks and four geometry checks. Five existing Chromium-only recovery cases remain skipped in the phone profile. All 2,473 client checks, release lint and production/font/artifact checks pass. Backend bytes are unchanged; prior 1,118 server checks are retained.

A long whole-app Tab path and outer header geometry after resize/dialog transitions are tracked separately. Compact calendar-cell week numbers/event text, saved-Event navigation and return context, wider scope/time/recurrence journeys, and physical-device/provider/release acceptance remain open. Application changes remain local.

## November 6 2026 - Quicker Planner Event capture and interruption recovery

Planner now presents a labelled Add event action, with Calendar and Planner creation in a secondary menu. The hosted dialog uses the same Event form as routed creation and the shared editor. Title, timing, all-day status and Calendar are visible first; location and other details remain available in a disclosure.

Capture keeps the selected local day and loaded Calendar context. Scheduler month navigation also updates the date used by the header action. An unavailable focused Calendar produces an explanation instead of silently creating in the first Calendar. Validation stays in the dialog and failed saves retain the entered values.

Testing found that an Event typed and immediately closed could miss the autosave delay. The hosted dialog now checkpoints that close through the protected draft owner and uses the existing interruption helper for reload/background recovery. Account synchronization remains debounced. Existing cross-device conflict and confirmed-cleanup behavior is retained.

The final local candidate passes 95 browser checks: 36 source and 36 compiled capture/consumer cases across four profiles, 15 existing draft checks and eight readiness checks. Four additional settled-animation captures were checked against that same compiled build. Five existing Chromium-only recovery cases remain skipped in the phone profile. All 2,471 client checks, release lint and production/font/artifact checks pass. Backend bytes are unchanged; prior 1,118 server checks are retained.

The broader scheduler toolbar cleanup, saved-record/return-to-plan discovery, additional scope/recurrence journeys and physical-device/provider/release acceptance remain open. Application changes remain local.

## November 6 2026 - Linked Task fields and usable field menus

Data Table groups for stored Subtask and Prerequisite links now resolve loaded Task names and normalize plain/populated references by identity. Name filtering works locally, returns after reload and clears without fetching the collection or discarding hidden Tasks. Stored links and their order remain unchanged. Structured display metadata also stays readable without passing an object into the rendered heading.

The long field menus now use a shared native-scroll option. This repairs a phone scrolling reset that could leave later fields unreachable. Grouping and Add filter controls remain mounted after selection, so keyboard focus returns correctly and Tab reaches the new filter query.

The current local candidate passes 52 browser checks across four profiles, including compiled linked-field journeys and existing drag/hidden-task/default-select persistence checks. All 2,467 client checks, release lint and production/font/artifact checks pass. Backend bytes are unchanged; prior 1,118 server checks are retained. Failed name/heading, touch-scroll and keyboard-focus runs remain recorded.

Other structured/nested presentation, capture policies, larger workloads, Task graph writers, placement and physical-device/release acceptance remain open. Application changes remain local.

## November 6 2026 - Notes work from nested Task menus

Task notes now opens from nested Data Table rows, including grandchildren. The menu had been visible while the recursive row boundary dropped its opening handler. Both recursive boundaries now pass the existing shared notes action through to the normal drawer.

Unfinished notes survive closing and reopening. Saving changes only that Task's notes; a refused save keeps the draft through reload and retries the same patch. Parent relationships, list/group assignments, completion, tags and other Tasks stay intact.

The local candidate passes 68 current browser checks: source and compiled details across four profiles, existing compiled subtask controls, and adjacent desktop/phone notes recovery. The original missing-drawer failure is preserved. All 2,463 client checks, release lint and production/font/artifact checks pass. Backend bytes are unchanged and the prior 1,118 server checks are retained. This is fixture-based browser acceptance; application changes remain local.

Other nested/structured view projections, Task graph writers, creation placement, larger workloads and device/release acceptance remain open.

## November 6 2026 - Workspace cleanup resumes after a browser restart

If server deletion succeeds while device storage blocks cleanup, Mindspace now checks again after a fresh browser sign-in and clears the kept copy attempt. It keeps only content-free retirement metadata. Startup manifest and account-draft reads wait for the same scoped confirmation, avoiding stale requests against the deleted Workspace.

The server lookup is authenticated and read-only. It accepts at most 100 explicit Workspace IDs, returns only IDs confirmed deleted for the signed-in owner, and excludes other owners and unfinished deletions. Authored recovery content stays on the device.

The current local candidate passes 128 source/compiled browser checks across four profiles, 16 adjacent account-draft journeys, ten real API journeys, all 2,463 client checks, release lint and production/font/artifact checks. The unchanged server candidate retains 1,118 full server checks. Desktop and phone fresh-process checks start with empty sessionStorage, verify sign-in and scoped retirement, make no stale reads or new authoring, and leave their owned disposable databases empty.

Other device namespaces, account-wide erasure, remaining Task graph writers, scale, physical-device and production/provider acceptance remain open. Application changes remain local.

## November 6 2026 - Workspace deletion clears kept copy attempts

Deleting a Workspace now clears its kept Task copy attempts on the device after the server confirms the exact Workspace and owner. Only content-free retirement metadata remains. Open recovery choices and late copy responses cannot bring those details back, while other accounts and Workspaces keep their recovery data.

A failed server deletion preserves the attempt. If server deletion succeeds but device storage blocks cleanup, the mounted Workspace screen explains what remains and supports retry through the server's deletion receipt.

The current candidate passes 104 source/compiled browser checks, eight real API journeys, all 2,450 client checks, release lint and production/font/artifact checks. Desktop and phone API journeys independently confirm two Workspace Task graphs erased and six ordinary copy-recovery graphs preserved. All eight disposable databases were cleaned up. Server runtime is unchanged; the prior 1,114 server checks are retained.

Account-wide device cleanup, other draft namespaces and returning after a full app restart while device cleanup remains blocked are still open. Application changes remain local.

## November 6 2026 - Clear recovery choices for Task copies

An old copy error message now stays bound to the attempt that produced it. If that attempt has already been handled, its button cannot silently create another task or act on a newer pending copy.

If the server finds the saved copy in Trash, recovery offers to restore and check that same copy. If the copy was permanently deleted, recovery offers an explicit replacement using the kept details. Cancelling keeps the attempt for later; creating a replacement retains its new identity before sending it.

Eighty focused source/compiled browser checks and six real API journeys pass. The real journeys cover restoration, cancelled and accepted replacement, and response loss on desktop and phone. Independent database checks confirm one active copy, unchanged originals and parent links, and cleanup of all six disposable databases. All 2,437 client and 1,114 server checks, release lint and the production build pass. Eight recovery screens were reviewed.

Device-kept intent erasure, remaining graph writers, scale, physical LG V60 checks and release work remain open. These application changes are local; this update publishes documentation only.

## November 6 2026 - Real copy replay and scope retirement

Desktop and phone journeys now verify copy recovery through the real mounted API and Mongo. Each deliberately loses a committed creation response, reloads and explicitly checks the same saved copy. The retry uses the same payload/key and receives the existing copy. Independent checks confirm one copy, one parent update, preserved originals and cleanup of both owned databases.

Scope checks found another responsiveness issue: a fresh recovery click could keep waiting on an old request after an account/workspace round trip. The shared runner now joins pending work only while its lease remains current. A fresh explicit check can use the retained key while the retired response is still held; the old response cannot publish or clear the newer work.

Twenty-four mounted source checks across four browser profiles cover retirement at the device checkpoint, while the response is held and during a recovery choice. Sixteen current compiled clone checks, two current real-API replay journeys, all 2,424 client checks, release lint and production/font/artifact checks pass. The current API journeys observed 127 responses, including two committed 201 responses deliberately withheld and two delivered 200 replays. Earlier nonclone regressions and unchanged UI frame reviews are retained.

The broader clone item remains open. Stale retry feedback must stay bound to its original saved attempt after cleanup, and saved copies in Trash or permanently deleted copies need explicit recovery choices. Wider erasure, placement, scale, physical LG V60/provider/release work also remains open. Application changes remain local.

## November 6 2026 - Safer Task copy recovery

Task copy actions now keep their exact payload and replay key on the current device before sending a request. A refused or uncertain save keeps that attempt. After reload, choosing Clone again offers an explicit check of the same saved copy, with an option to keep it for later. Repeated clicks during a pending copy join that operation; a deliberate later copy gets a fresh key after confirmation.

The UI and global default actions share the recovery service, existing protected scoped draft transactions, confirmation dialog and canonical Task receipt owners. Eight source browser checks and 68 compiled checks across four profiles pass, including exact replay, refused-save cancellation/retry, deliberate new copies, held clicks and existing editing/subtask controls. All 2,423 client checks, release lint and production/font/artifact checks pass. Four recovery dialogs were reviewed.

The current real-API compatibility journey also passes: three ordinary copies use three distinct keys, preserve the originals and parent relationships through reload, and pass independent Mongo checks. Its owned database is cleared. That journey does not yet prove real response-loss replay; the lost-response cases above use isolated browser fixtures.

The wider clone recovery item remains open for mounted account/workspace retirement and actual API/Mongo replay after a lost response. Trash/restore, erasure including the new local recovery records, placement, scale and physical-device/provider/release work also remain open. Application changes remain local.

## November 6 2026 - Clearer expanded Task details

Expanded Data Table rows now put description and subtask actions first. Internal user/list/relationship IDs, mirror arrays and raw system settings no longer appear as everyday editable fields. Categories and tags show readable labels with access to the existing Task editor, and the pin switch has an explicit label and controlled saved state. Minute estimates are available alongside the other useful Task fields.

Details use the existing per-view layout preferences. Narrow screens keep a readable single column; wider layouts retain their two-column, three-column and adaptive choices. Grouping and filters still use the complete field registry. Existing inline draft and queued-save owners remain in place.

Seventy-two compiled browser checks pass across Chrome, Firefox, tablet Safari and mobile Chrome, covering controls, independent layouts, grouping, filters, subtask capture, attachment and minimal field updates. A phone source regression also passes. All 2,417 client checks, release lint and production/font/artifact checks pass, and four final screenshots were reviewed. This client presentation slice uses isolated browser fixtures; the earlier real-API/Mongo evidence is retained, not claimed as rerun.

The full goal is restored after the desktop app reinstall. Application source remains local. Clone interruption/refusal/replay, Trash/restore and erasure writers, placement, larger workloads, physical LG V60 testing and the rest of the consolidation phase remain open.

## November 3 2026 - Fresh Task copies and Data Table clone actions

Task copies now share one fresh-task contract. Copying a completed task clears completion, Done status, progress and completion dates while keeping its description, list, group and intended parent. A copied parent starts with an empty child list; it does not borrow the original parent's children. The original records and relationships stay intact.

Data Table now offers Clone Task in both full and nested row menus. Those actions, Basic/List context actions and the existing sidebar actions use the same confirmed-save owner; the global command's default service uses the shared copy builder. Confirmed local insertion is tied to the account and workspace that started the action. Direct desktop/phone proof covers the full and nested Data Table menus and Basic context menu, including switching views without another Task collection fetch, refresh and reload.

Seven real-API journeys pass against the current compiled app, including clone, native-save, Data Table, exact child-create replay, refused move and lost-reparent recovery. All seven owned databases are cleared. Independent Mongo checks confirm three fresh copies per clone journey, reset fields, correct parent mirrors and preserved original content, completion, date, list, group and position. Thirty-two fresh compiled native regression cases also pass across four browser profiles. The current API journeys observed 378 actual responses, one expected refusal and two deliberately withheld committed responses.

All 2,413 client checks, 35 focused checks, release lint and production/font/artifact checks pass. Four settled desktop/phone screenshots were reviewed. Earlier failed runs remain failed; test-only reporting now preserves initial disposable ownership and cleanup diagnostics through shutdown failures. The production server is unchanged, with its earlier 1,110 checks retained rather than claimed as rerun.

Application source remains local. Remaining Task work includes compact meaningful expanded details, clone interruption/recovery, Trash/restore and erasure graph writers, creation placement and larger workloads. Physical LG V60/touch, production-origin/CORS, providers and the wider phase remain open.

## November 2 2026 - Real refused saves and lost Task moves verified

A refused child-task save keeps the original thought available to correct. When its parent becomes unavailable after the form opens, the real server rejects that placement; choosing a valid placement saves the thought once under the same capture identity. A refused reparent similarly keeps its exact change in the shared queue. After reload, Retry checks current server state and saves the same minimal change, preserving the task's list, group, content, completion and date.

Desktop and phone checks also let the server commit a detach or reparent before deliberately withholding its response in the owned test bridge. Recovery reads the canonical task and both affected parents, confirms the saved result and clears the queue without sending another move. Independent Mongo checks confirm one task and the correct parent lists, with no second version increment from recovery.

Nine current real-API journeys pass, including native-save compatibility. All nine initially empty owned databases are cleared. There are 406 actual API responses, four expected server refusals, four deliberately lost committed responses and nine zero-page-error observations. Four focused safeguards pass for the private fixture control, which accepts only fixed actions in its owned database and is never mounted in the app.

Only test/probe code changed; the compiled app and production server remain unchanged. Earlier positive Data Table, interrupted capture and exact child-create replay proofs remain retained, alongside 2,411 client checks, 1,110 server checks, 70 UI browser cases and twelve isolation controls; those earlier suites are not claimed as rerun. These checks complete this bounded local API recovery item. Other graph writers, creation placement, larger workloads, production-origin/CORS, providers, physical LG V60/touch and the wider phase remain open. Application source remains local.

## November 2 2026 - Real Task graph and capture recovery verified

Data Table attach, reparent and detach now have desktop/phone proof through real login, the normal mounted API and Mongo. Each journey sends three minimal child-parent patches, receives the canonical parent updates, reloads and explicitly refreshes Tasks. Independent database checks confirm both parent mirrors and preserved title, description, completion date, list, group and position.

Child capture also passes after the editor is closed and the page reloaded: the original thought resumes, creates once with its parent/list/group context and appears immediately without a collection reload. A separate test lets the real server commit a child, then deliberately drops that response in the loopback forwarding bridge. After interruption, replaying the exact creation key and body receives the existing Task. Both desktop and phone retain one saved child and one parent link; replay does not advance the committed parent/child versions again.

Seven real-API journeys pass, including native-save compatibility, with seven cleared owned databases, seven zero-page-error observations and 492 actual API responses without HTTP failures. Two committed responses were intentionally not delivered to exercise recovery. The seven journeys make only fourteen Task collection reads: initial loading plus explicit canonical refresh. Twelve separate compiled isolation controls pass across four profiles, including guards that keep response dropping opt-in. No Task store seed or synthesized API response is used in the real journeys.

Only test/probe code changed. The same production artifact and existing 2,411 client checks, 1,110 server checks and 70 UI browser cases are retained, not claimed as rerun. The failed first independent capture check assumed null for a field the seed leaves unset; it remains failed, and final probes require exact original-field/version preservation. Application source remains local. Actual server-refused saves, lost move-response recovery, other graph writers, creation placement, larger workloads, production-origin/CORS, providers, physical LG V60/touch and the wider phase remain open.

## November 1 2026 - Compact Basic Task controls on phones

The Basic phone toolbar now measures about 115 pixels rather than 235 at the reviewed width. Search and Add Task stay visible; grouping and advanced filters open from a labeled button with an active-filter count. Each tab retains its own disclosure choice, filters and unfinished filter text. Fields stay mounted while hidden, and opening the panel reuses the existing compiled filter state. Desktop/tablet filter actions and capture share one row. Empty writable groups combine their message and Add task action while keeping the existing drop zone. The simple List lens keeps its toolbar-free presentation.

Current validation passes 2,411 client checks, release lint with zero errors and the existing 21 warnings, and production/font/artifact audits. There are 70 current browser cases: 16 source and 54 compiled, including four-profile compact controls and native queued-drag regressions, plus two fresh real-API desktop/phone saves with independent Mongo confirmation and cleared owned databases. Four source/compiled desktop, tablet and phone screenshots were reviewed.

The earlier broad 86-case run remains failed at 80/86; six older journeys needed explicit open-panel steps before using now-collapsed controls. Their original data, draft and fit/hit assertions are unchanged, and fresh source/compiled rechecks pass. A tablet failure against an introduced blanket height cap is retained; the final check measures desktop/tablet action-row alignment directly while preserving strict phone height limits. These narrower current checks do not turn the old broad run into a pass.

The frozen candidate has 2,890 client inputs, 574 unchanged server inputs and 516 build files. Existing server runtime is unchanged; prior server checks are retained, not rerun. Application changes remain local. Broader real Task capture/refusal/lost-response recovery, clone/Trash/erasure writers, placement, larger workloads, physical LG V60/touch and the wider product/release phase remain open.

## November 1 2026 - Selected Task tabs stay visible on phones

Opening Basic directly could show the Kanban label because the correctly selected Basic tab was entirely clipped inside the horizontal strip. The tab owner now reveals the active chip when selection, arrangement or available width changes, while preserving manual scrolling and keyboard focus. A reusable ContentHeader option gives Task navigation its own row on mobile; desktop retains one row. This keeps the selected label readable even at 320 pixels without refetching or discarding loaded Tasks.

The old compiled baseline fails the visibility check. An initial reveal-only attempt exposed insufficient room at 320 pixels; that failed run is preserved. The final candidate passes 6 source and 12 compiled tab-continuity cases, including direct entry, reload, resize, focus/data retention, close and preset restore. All 32 compiled native drag/recovery regressions pass across four browser profiles. Two fresh desktop/phone journeys also save through real login/mounted APIs, confirm Mongo state after reload and clear their owned databases; 98 API responses have no HTTP errors. Four source/compiled phone screenshots were reviewed.

Current checks: 2,408 full client checks, 241 focused checks, zero lint errors with the existing 21 warnings, and production/font/artifact audits. The frozen candidate has 2,887 client inputs, 574 unchanged server inputs and 516 build files. Prior 1,110 server checks are retained, not rerun. Application changes remain local. Phone filter-toolbar/empty-group density, broader real Task capture/refusal/recovery, other graph writers, physical LG V60 testing and the wider product/release phase remain open.

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
