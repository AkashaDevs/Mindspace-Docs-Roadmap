# Mindspace client features and roadmap

[Overview](README.md) · [Server](SERVER_FEATURES.md) · [Progress](PROGRESS.md)

Updated November 1, 2026. Checked and struck-through items have implementation and recorded development verification. Empty checkboxes remain open. New usability reports stay open even when an earlier implementation test passed. These are development statuses, not a claim about every hosted version.

## Capture and return

- [x] ~~Shared quick-entry actions for Tasks, Events, Notes, Reminders, Journal and Stats.~~
- [x] ~~Scratchpad and Captchalogue capture with details added after the thought is saved.~~
- [x] ~~Retain unfinished capture and editor drafts across navigation and interruption.~~
- [x] ~~Recover uncertain Task and Reminder creation without blindly creating another record.~~
- [x] ~~Turn a saved Note into a Task and continue to scheduling or a reminder.~~
- [x] ~~Carry the original thought time into natural-language reminder interpretation.~~
- [x] ~~Search Tasks, Notes, Goals, Events, Habits, Stats, Reminders and Daily Log writing.~~
- [x] ~~Offer bounded spelling recovery when exact search finds nothing.~~
- [x] ~~Shared record detail, archive and Trash recovery for supported record types.~~
- [x] ~~Lazy schema-by-schema Database Explorer with registered record commands.~~
- [x] ~~PWA capture shortcuts and text-share entry foundations.~~
- [ ] Verify installed-phone shortcuts, sharing and actual device capture comfort.
- [ ] Extend hands-free capture and commands through the shared action directory.
- [ ] Complete a scoped export and restore journey across supported record types.

## Navigation and shared layout

- [x] ~~Registry-driven routes, breadcrumbs, navigation, page tools and command search.~~
- [x] ~~Shared record actions and contextual commands through the switchboard.~~
- [x] ~~Fixed dashboard outer shell with a scrollable content interior.~~
- [x] ~~Compact mobile header with primary capture outside the overflow menu.~~
- [x] ~~Configurable navigation visibility and alert-focused rail badges.~~
- [x] ~~One expandable floating launcher for health and diagnostic tools.~~
- [x] ~~Visible recovery for failed page loading.~~
- [x] ~~Background refresh preserves loaded Tasks, navigation and unfinished capture.~~
  - [x] ~~Retain authored Task edits while refreshed records arrive.~~
  - [x] ~~Keep progress and retry available after closing and reopening page tools.~~
  - [x] ~~Prevent older workspace reads from undoing a confirmed workspace switch.~~
- [x] ~~Keep newer queued edits when an earlier save finishes, while respecting discarded local work.~~
- [x] ~~Open Todo list tools and Planner Page tools by default, with per-dashboard tab choices.~~
- [x] ~~Choose and reorder compact right-sidebar widgets, with a labelled phone drawer and a separate Today task view.~~
- [x] ~~Skip to dashboard content on the first Tab and browse desktop views with arrow keys.~~
- [x] ~~Show the confirmed Event title in every breadcrumb layout when opening a saved Event directly.~~
- [x] ~~Keep notification history controls and record titles visible on narrow screens.~~
- [ ] Complete longer keyboard, pointer and touch journeys across dashboard changes.
- [ ] Verify global roster refresh before workspace selection.
- [ ] Continue measured visual consistency, spacing and accessibility improvements.

## Home, Workbench and time

- [x] ~~Home and Your Day for daily tasks, events, reminders and reflection.~~
- [x] ~~Compact optional first-use capture and retrieval guide.~~
- [x] ~~Today's Agenda date controls and event/task/routine/habit filters.~~
- [x] ~~Workbench tools and a return path to the previously selected Task.~~
- [x] ~~Inspectable next-action suggestions and optional current-energy ordering.~~
- [x] ~~Break a larger Task into a concrete smaller step and continue to focus time.~~
- [x] ~~Time planning uses confirmed schedule data and retains interrupted intent.~~
- [x] ~~Header Day Circle toggle, active inset styling and pressed feedback.~~
- [ ] Confirm the original Day Circle placement problem in the affected review setup.
- [ ] Verify repeated daily use and longer interruptions beyond controlled regressions.

## Tasks

- [x] ~~TodoList → TodoListGroup → Task hierarchy and retained list selection across views.~~
- [x] ~~Kanban, List, Detailed, Table and Calendar presentations of shared data.~~
- [x] ~~Filter loaded Tasks by list without discarding other lists' records.~~
- [x] ~~Indexed Task lookup and shared group projection foundations.~~
- [x] ~~Task/group drag and drop with persisted ordering and failure recovery.~~
- [x] ~~Preserve hidden column positions and newer Task edits when column saves finish.~~
- [x] ~~Keep rapid Task and column saves in order through the shared queue owner while rendering moves immediately.~~
- [x] ~~Saved custom groups show all matching Tasks in their own list.~~
  - [x] ~~Keep manual membership and overlapping card occurrences distinct.~~
  - [x] ~~Persist filter rules and identify legacy rules requiring review.~~
- [x] ~~Kanban zoom from 25% to 200% with stepped buttons and slider.~~
- [x] ~~Drop space below Add Task and collapsed, fit-height and full-height columns.~~
- [x] ~~Configurable tabs with add, close, rename, pin, reorder and move actions.~~
  - [x] ~~Save and restore one account-backed tab preset.~~
  - [x] ~~Open several instances of a view type with stable identities and individual names.~~
  - [x] ~~Keep Kanban zoom and hidden groups independent for each tab.~~
  - [x] ~~Recover the saved arrangement from the account without relying on browser settings.~~
  - [x] ~~Keep tabs after failed or unconfirmed saves and preserve newer local changes during a delayed save.~~
- [x] ~~Virtualized variable-height Task table with bounded mounted rows.~~
- [x] ~~Shared reminder actions, due-time controls and recoverable edits.~~
- [x] ~~Retain unconfirmed queued Task/group batch updates for retry, including ungrouping and automatic-group drop fields.~~
- [x] ~~Show confirmed queued Task and column changes immediately after Retry while preserving newer edits.~~
- [x] ~~Recover refused or partially saved direct Task and column moves through Sync Queue during the current session, preserving newer edits and flagging conflicts.~~
- [x] ~~Recover pending Task and column moves from a protected device copy after reload, for the original account and workspace, with explicit Retry and fresh server checks.~~
- [x] ~~Keep the remaining tasks from one drag together in Sync Queue, with review when any position or parent changes.~~
- [x] ~~Retry overlapping pending drags as one order after reload and hold related tasks together when a saved position conflicts.~~
- [x] ~~Recover unsaved task and column moves in a fresh browser signed into the same account and workspace.~~
- [x] ~~Keep nearby drags in large Kanban columns to the tasks whose positions change, including sparse saved positions.~~
- [x] ~~Clear an already confirmed recovery row when another retry write fails, retaining only refused or conflicted work.~~
- [x] ~~Wait for exact recovery-copy confirmation before queued Retry, with clear progress and failure feedback while preserving independent drafts.~~
- [ ] Verify whole-move transactions, ordering across devices and remaining drag adapters.
- [ ] Clarify opening Tasks, choosing a view, opening list tools and selecting a list filter.
  - [x] ~~Expose Lists beside the tabs using the existing desktop tools and mobile left drawer.~~
  - [x] ~~Reorder saved Todo Lists with pointer, keyboard and touch while keeping the active list selected.~~
  - [x] ~~Reveal the selected Task tab on direct entry, reload and resize, with a readable mobile navigation row that preserves focus and loaded Tasks.~~
  - [x] ~~Keep Basic search and capture visible in compact phone controls, with discoverable active filters, retained drafts and compact writable empty groups.~~
  - [x] ~~Keep loaded Task records and shared list selection while switching views.~~
- [ ] Finish measured list-toggle and drag pickup responsiveness on representative data.
  - [x] ~~Show Kanban Task and column grips with labeled keyboard move controls.~~
  - [x] ~~Keep Task editing available during a column save and retry the same column batch after interruption.~~
  - [x] ~~Save the actual drop position in Basic and List and keep a newer drag active while an earlier save finishes.~~
  - [x] ~~Defer collapsed Kanban card details and scheduling options until opened.~~
  - [x] ~~Confirm a saved Task defer and open review for its linked reminders.~~
  - [ ] Recheck zoomed dragging, long boards and interactions after extended use.
  - [ ] Meet practical keyboard and physical-phone acceptance alongside browser tests.
- [ ] Support several independently configured instances of the same view type.
  - [x] ~~Stable repeated instances, account preset and independent Kanban presentation.~~
  - [x] ~~Keep Calendar dates, display mode, selected-day focus and applied filters independent in each tab and the account preset.~~
  - [x] ~~Apply Calendar text filters to retained Tasks locally, with removal restoring the matching list data.~~
  - [x] ~~Keep primary Calendar actions and date controls visible as the available width changes.~~
  - [x] ~~Independent Table group expansion and Detailed grouping, sorting, filters and group disclosure through refresh and reload.~~
  - [x] ~~Per-tab Data Table filters, selected grouping and task-order direction, with responsive row-detail expansion and real layout choices.~~
  - [x] ~~Keep working tabs through ordinary reloads and restore saved presentation from the account preset.~~
  - [x] ~~Sort the top-level rows in each Table tab using loaded Tasks; retain field and direction through reload and account presets.~~
  - [x] ~~Keep automatic sorting separate from Manual order drag, cancel held drags on view changes and preserve the existing batch save.~~
  - [x] ~~Apply top-level Table text filters locally, retaining hidden Tasks and independent tab preferences through reload and account presets.~~
  - [x] ~~Preserve hidden Task positions and real list/group membership through filtered drag, queued Retry and reload.~~
  - [x] ~~Show matching Table counts and a clear way to recover when filters hide every row.~~
  - [x] ~~Keep sorted-row controls usable and avoid repeating large collection sorts when a row expands.~~
  - [x] ~~Data Table drag saving and recovery preserve hidden Tasks, typed grouping, canonical list/group membership and ascending, descending or loaded order.~~
    - [x] ~~Keep later Task edits behind earlier saves without blocking input, preserving newer fields when move replies arrive.~~
  - [ ] Audit List, Basic, Gantt and other nested view settings.
    - [x] ~~Keep Basic search and applied category/text filters independent in each tab, through reload and account presets, using retained Tasks.~~
    - [x] ~~Provide Clear filters recovery and advance active due-date filters when the local day changes.~~
    - [x] ~~Keep List/Basic row details and subtask expansion independent, alongside Basic group collapse preferences.~~
    - [x] ~~Refresh Basic saved/automatic groups from current Task fields and render structured tags through the shared normalizer.~~
    - [x] ~~Preserve full native row-move batches and reload order; retire held drags on tab/list/filter/scope changes while allowing dispatched saves to finish.~~
    - [x] ~~Open List details explicitly without shifting controls on focus; use the existing details dialog on narrow screens.~~
    - [x] ~~Keep Basic search, filters and actions inside the dashboard across narrow and wide layouts.~~
    - [x] ~~Group Basic Tasks by saved groups, status, priority, difficulty, tags, assignee, due date or completion through shared projections.~~
    - [x] ~~Retain each Basic tab's grouping through reload and account presets; update due-date groups when the day changes.~~
    - [x] ~~Save supported field-group drops through the shared queue and Retry, preserving actual list/group membership and subtask relationships.~~
    - [x] ~~Capture Tasks with explicit field-group defaults and create saved groups through the existing confirmed page save owners.~~
    - [x] ~~Cancel released touch holds across menus so a quick selection cannot open a delayed context menu.~~
    - [ ] Finish remaining Gantt/nested projections and larger preset/workload acceptance.
- [ ] Recheck table density and timestamp input presentation in the visual pass.
  - [x] ~~Fit the Data Table due-date editor to its available width and keep dates and times editable in either order.~~
  - [x] ~~Create Tasks from the Table header, a group or an empty workspace through the shared editor, with explicit destinations and protected drafts.~~
  - [x] ~~Open the current saved Task from compact feedback even when filters hide it, retaining the selected filters, list and tab.~~
  - [x] ~~Keep newer loaded Task fields and one visible record when retrying a creation whose original response was lost.~~
  - [x] ~~Compact Data Table actions, readable task titles/labels and date editing with Save, Cancel and Clear.~~
  - [x] ~~Confirmed completion, minimal notes edits and position commands through the shared move queue.~~
  - [x] ~~Create from empty Data Tables and actual list/group or status/priority/difficulty contexts through the shared Task editor, with explicit destination controls and group-rule choices.~~
  - [x] ~~Keep capture drafts and the original unconfirmed save through close/reload; retry with one stable creation identity, keep uncertain details read-only and allow correction after an explicit destination refusal.~~
  - [x] ~~Keep Task editor header and save controls visible around one scrollable form body, with phone-sized controls and viewport/overlap checks.~~
  - [x] ~~Type Task titles and multiline details without a server request per character; commit on Enter or leaving the field and keep focus stable while grouping changes.~~
  - [x] ~~Keep unfinished field edits on the current device through refused saves, reloads and view changes, preserving newer typing while older saves finish.~~
  - [x] ~~Review competing tab copies or changed saved values before overwriting; retry storage/cleanup failures and retain invalid structured text for correction.~~
  - [x] ~~Keep unfinished Task titles and notes on the device across closing and reloads; recover uploaded account drafts in a fresh browser.~~
  - [x] ~~Save or clear only authored Task fields, preserve multiline literal text, and retain newer typing while older saves or recovery cleanup finish.~~
  - [x] ~~Review competing recovery copies or changed saved fields, discard a local edit without changing the Task, and finish matching recovery cleanup without replaying an update.~~
  - [x] ~~Keep compact Task notes actions visible around a scrollable writing area, with shared dictation and touch-sized controls.~~
  - [x] ~~Preserve literal tags, entities and whitespace in plain-text editor drafts, commits and saves using format-aware normalization.~~
  - [x] ~~Render plain-text previews as text and keep rich HTML previews on the shared sanitizer, including read-only and live modes.~~
  - [x] ~~Keep expanded Task details focused on description, subtasks and useful fields, with labeled pin state, compact sections and access to the full editor.~~
  - [x] ~~Keep the exact Task copy attempt on the device before sending, explicitly check refused or uncertain copies after reload, and join repeated clicks while a copy is pending.~~
  - [x] ~~Recover a real committed child-copy response after reload by replaying the same key and payload on desktop and phone, preserving one copy and one parent update.~~
  - [x] ~~Retire old clone work across account/workspace changes while allowing a fresh explicit recovery check before an old response arrives.~~
  - [x] ~~Keep old copy-recovery actions bound to their original attempt so they cannot create an accidental second copy or interfere with newer work.~~
  - [x] ~~Restore the same saved copy from Trash, or explicitly create a replacement with the kept details after confirmed permanent deletion.~~
  - [x] ~~Erase kept Task copy attempts after confirmed Workspace deletion, block late copy work, preserve other scopes and offer explicit retry if device cleanup fails.~~
  - [x] ~~Resume blocked Workspace copy-attempt cleanup after a full browser restart, and hold dependent reads until authenticated scoped confirmation.~~
  - [ ] Verify removal of device-kept copy attempts through scoped local-data erasure.
  - [ ] Finish nested relationships and audit remaining inline/shared plain-text consumers.
    - [x] ~~Group stored Subtask/Prerequisite reference arrays by identity and filter using loaded Task names, keeping stored links, order and hidden Tasks intact.~~
    - [x] ~~Reach long Data Table field menus by touch and keyboard, retaining focus through grouping changes and into a newly added filter query.~~
    - [x] ~~Open nested Task notes in the shared drawer, retain unfinished text and retry refused saves without changing relationships or other Task fields.~~
    - [x] ~~Open Data Table subtask capture in the canonical editor with the actual parent/list/group prefilled, without saving a sentinel or blank Task.~~
    - [x] ~~Attach an existing Task from Data Table through one minimal queued child-parent patch while retaining its actual list, group and position.~~
    - [x] ~~Create a child through the canonical editor and resume independent parent-specific drafts after reload, parent movement or parent removal, including account-only long-context drafts.~~
    - [x] ~~Preserve the current thought before switching drafts, checkpoint rapid page interruptions through the protected draft owner, and recover a lost reparent response with direct Retry without repeating the move.~~
    - [x] ~~Resolve divergent device and account Task drafts with explicit choices, and resume confirmed child cleanup without creating the Task twice.~~
    - [x] ~~Retire account work during a scope-changing draft switch while preserving the original device copy, including an explicit device-only retry when its checkpoint fails.~~
    - [x] ~~Show compact device/account draft text comparisons before choosing a recovery copy.~~
    - [x] ~~Resolve a competing device draft after account/workspace retirement through explicit local choices while account work stays stopped.~~
    - [x] ~~Keep draft selection responsive through pending device saves and avoid repeated blank or unchanged account autosaves while preserving explicit clears.~~
    - [x] ~~Verify mounted detach/reparent with both parent mirrors, minimal queued patches and unchanged actual list/group membership.~~
    - [x] ~~Recover refused or lost Task-graph and child-create responses through explicit copy choices and exact replay, confirming one saved result.~~
    - [x] ~~Render and repair legacy circular Task links within a finite path and prevent invalid ancestor choices.~~
    - [x] ~~Move native List/Basic hierarchy drags onto minimal shared queue batches while retaining affected parent order.~~
    - [x] ~~Preserve hidden children and real list/group assignment without sending unrelated Task text or completion dates in hierarchy moves.~~
    - [x] ~~Recover refused or lost native hierarchy saves and queue rapid moves in order while releasing the held appearance before confirmation.~~
    - [ ] Verify graph UI journeys against an isolated real API and audit remaining clone/Trash/account-erasure graph writers.
      - [x] ~~Verify a compiled native parent/position move through real login, mounted APIs, reload and independent Mongo inspection on desktop and phone layouts.~~
      - [x] ~~Verify Data Table attach, reparent and detach through real APIs, canonical parent receipts, reload and independent Mongo preservation checks on desktop and phone.~~
      - [x] ~~Resume an interrupted child thought after editor close/reload and create exactly one linked Task through the real API on desktop and phone.~~
      - [x] ~~Recover a deliberately lost committed child-create response by replaying the exact key and payload, confirming one Task and parent link on desktop and phone.~~
      - [x] ~~Keep a thought after the real server refuses its unavailable parent, then correct and save it once on desktop and phone.~~
      - [x] ~~Retain a real refused reparent in the shared queue and retry the same minimal change after reload on desktop and phone.~~
      - [x] ~~Confirm a saved detach after its response is lost without sending a second move on desktop and phone.~~
      - [x] ~~Recover both parent lists after a saved reparent response is lost without sending a second move on desktop and phone.~~
      - [x] ~~Use one fresh-copy contract for Task clone actions, resetting completion, Done status, progress and completion dates while preserving reusable context and intended parent.~~
      - [x] ~~Clone parents and completed children through full/nested Data Table row menus and Basic context actions, preserving originals and saved relationships on desktop and phone.~~
      - [x] ~~Use one bounded canonical HTTP health request at the configured API origin, preserving explicit database and maintenance state without unmounted fallbacks.~~
    - [x] ~~Publish related Task graph confirmations through shared mutation services without a full collection reload, preserving newer fields and retired scopes.~~
    - [x] ~~Provide minimal parent/mirror move payloads, protected recovery contracts and version-aware queue rollback baselines; retain pending intent across related confirmations.~~
- [ ] Finish remaining text/Markdown/JSON import/export and subtask/sidebar drag workflows.

## Planner and routines

- [x] ~~Planner, Calendar and Event records with day and scheduling views.~~
- [x] ~~Calendar visibility filters use retained data.~~
- [x] ~~Shared Event entry and Task-to-Time scheduling actions.~~
- [x] ~~Routine, focus, day, week and cycle planning foundations.~~
- [x] ~~Reduce Planner toolbar clutter and clarify primary actions.~~
  - [x] ~~Use one scheduler toolbar with truthful period/day headings, stable keyboard focus and a grouped selector for all 14 supported layouts.~~
  - [x] ~~Make Add event the primary header action, keeping Calendar and Planner creation in a secondary menu.~~
- [x] ~~Provide an obvious compact quick-add Event form with progressive detail.~~
  - [x] ~~Preserve a freshly typed Event on immediate close or reload, and retain details through refused-save retry and confirmed cleanup.~~
- [x] ~~Improve compact calendar-cell spacing and preserve native overflow access and Event actions.~~
  - [x] ~~Wrap time/title previews and separate week/date links at narrow widths and enlarged text.~~
- [x] ~~Hide collapsed dashboard shortcuts and keep their expanded panel within narrow screens.~~
- [x] ~~Resolve compiled phone viewport zoom/pan after startup, resizing and dialogs.~~
  - [x] ~~Keep native pinch zoom available without accidental Event activation, while preserving fresh taps and keyboard navigation.~~
- [x] ~~Use the compact Event form for day taps, timed slots and dragged date ranges, keeping the selected date and focused Calendar.~~
  - [x] ~~Preserve interrupted drafts and retry, edit the saved Event without duplicating it, and open a linked Reminder after confirmed creation.~~
- [x] ~~Open saved Event details from Today, Agenda, Scheduler and confirmed capture, with a clear return to the original Planner view.~~
- [x] ~~Keep the chosen Planner and Calendar consistent across Event capture and draft recovery.~~
- [x] ~~Show the last occupied day and preserve the Event range during all-day editing.~~
- [x] ~~Keep all-day Event dates across timezones and edit timed Events in their named zone.~~
- [x] ~~Author and recover recurring Planner Events, and show their occurrences in Scheduler and Planner timelines.~~
- [x] ~~Show recurring and overlapping Events in the Planner upcoming list for the selected dates.~~
- [x] ~~Reuse loaded Planner Events and support overlapping and recurring candidates for standalone date windows.~~
- [ ] Verify the updated running backend for recurrence and date windows, and review remaining day detail.
- [ ] Verify external calendar providers and read/write behavior before claiming full integration.

## Notes and Journal

- [x] ~~Hierarchical Notes explorer, note editing and Scratchpad capture.~~
- [x] ~~Compact collapsible Captchalogue that retains its draft.~~
- [x] ~~Clearer capture and note containers with restrained borders and shadows.~~
- [x] ~~Journal grid, larger grid and list views with formatted Markdown previews.~~
- [x] ~~Journal date navigation and recent-entry sidebar.~~
- [x] ~~Keep floating Daily Log drafts tied to the day they were started, including across timezone changes.~~
- [x] ~~Load the Notes explorer by location and minimal metadata.~~
  - [x] ~~Fetch the selected file separately and page folder metadata.~~
  - [x] ~~Restore the last folder, expanded branches and selected file on the same device within the workspace.~~
  - [x] ~~Keep folder and file loading, empty and retry states local to the Explorer.~~
- [ ] Add familiar explorer reorganization and inline rename interactions.
  - [x] ~~Move files and folders between folders by desktop drag or a keyboard and touch picker, with confirmed feedback and retry.~~
  - [x] ~~Persist manual order within a folder using desktop row-edge drops or the Before and After picker.~~
  - [x] ~~Start inline rename with F2, a deliberate second mouse click or the row menu and select the existing name.~~
  - [x] ~~Save with Enter, blur or the checkmark. Cancel with X or Escape. Use Shift+Enter for a newline.~~
- [ ] Recheck editor switching, wider layouts and compact file details.
- [ ] Finish supported note imports and grouped sticky-note workflows.

## Reminders and notifications

- [x] ~~One-off and flexible recurrence, including selected weekdays and multi-week rules.~~
- [x] ~~Fast capture followed by later timing, context and delivery enrichment.~~
- [x] ~~Linked Reminder actions from Tasks, Notes, Goals and Daily Logs.~~
- [x] ~~Create a linked record from inside a Reminder while keeping its draft, and attach it after a confirmed save.~~
- [x] ~~Manage several reminders for one source without hiding separate identities.~~
- [x] ~~In-app notifications, snooze and channel/device settings foundations.~~
- [x] ~~Engagement-aware pacing foundations with inspectable timing context.~~
- [x] ~~Connect header entries to their own notification details and full history table.~~
  - [x] ~~Keep an explicit one-action related-item destination alongside notification details.~~
  - [x] ~~Read scoped canonical records, show confirmed opening status and offer inline retry or history when a notification is unavailable.~~
  - [x] ~~Preserve an unfinished Quick Jot thought when detail/history navigation is declined.~~
  - [ ] Complete return journeys from deleted or unavailable related source items.
- [ ] Unify reminder, delivery-status and history presentation.
  - [x] ~~Page Notification History cards and return from details to the same page and filters.~~
  - [x] ~~Read the Notification History inbox in scoped cursor pages and preserve the exact unread badge.~~
  - [x] ~~Load 12 header notifications at a time with exact tab counts, retry and a restore path.~~
  - [x] ~~Page the Notifications Board and its rated deliveries while preserving the Table filters and sort.~~
  - [x] ~~Load Notifications Table pages with global filters, sort and retryable inline edits.~~
  - [x] ~~Use scoped Reminder timing evidence on the dashboard, in the editor and in the record summary.~~
  - [x] ~~Open the exact notification from Today’s Agenda and the Time timeline.~~
  - [x] ~~Verify the matching mobile Setup probe and recover its receipt after reload.~~
  - [x] ~~Read Home notification rows for the selected day and calendar markers for the browsed month.~~
  - [x] ~~Read scoped notifications for Time, the Day Circle and schedule availability.~~
  - [x] ~~Use scoped notification reads for Messages refresh, Archive and Database Explorer.~~
  - [x] ~~Keep Reminder capture and Notification history available during refresh and retry.~~
  - [x] ~~Recover unscheduled Reminders from Home, with an inline retry when the Reminder read fails.~~
  - [x] ~~Page archived notifications in Trash and open full summaries on demand.~~
- [ ] Complete real-device delivery and repeated-use pacing acceptance.

## Habits, Goals and Stats

- [x] ~~Habit definitions, check-ins and table/calendar/timeline views.~~
- [x] ~~Virtualized Habit days with overscan and eviction using loaded activity.~~
- [x] ~~Goal progress, related records and linked reminders.~~
- [x] ~~Typed timestamped Stats, data keys and shared global entry.~~
- [x] ~~Confirmed sidebar Stat saves/edits, including optional context.~~
- [x] ~~Deferred secondary Stat controls keep primary capture immediately available.~~
- [x] ~~Request-gated Narrative signed tallies and timestamped annotations.~~
- [ ] Verify persisted statistical Insights presentations alongside the Orion restoration.
- [ ] Reduce granular hourly and large-range chart latency.
  - [x] ~~Build ordinary hourly lines from recorded periods and avoid drawing a dot for every point in long ranges.~~
  - [x] ~~Draw hourly Count and Sum lines from the edges of empty stretches while keeping exact hourly values available for inspection.~~
  - [x] ~~Draw hourly Bar and Area charts with fewer points while keeping time spacing, zero values and missing-data gaps.~~
- [x] ~~Connect recorded periods on the line chart with spacing based on elapsed time.~~
- [x] ~~Create the typed Stats key from the Data Table or global capture, with an explicit plus action and exact history matches.~~
- [x] ~~Keep the Stats Data Table compact with visible Search, Quick Add and paging at phone widths.~~
- [x] ~~Log a Stat from any dashboard through the header and resume an unfinished Stat on the same device.~~
- [ ] Add practical chart range navigation inspired by financial charts.
  - [x] ~~Choose common or custom chart dates, keep custom dates through a refresh, and fit the main controls above the chart on phones.~~
- [ ] Design complex-value charts, trend lines and useful analysis.
  - [x] ~~Chart same-day Time Range values in minutes and select numeric fields inside saved objects and arrays.~~

## Orion AI

- [ ] Restore agentic Insights and its entry through shared capability/action owners.
  - [x] ~~Show Reflect AI availability, lookback and data disclosure, and preserve results during retry.~~
- [ ] Explain the Recommendations model, selected data and instructions.
- [x] ~~Add basic chat with provider disclosure, opt-in recent messages, and a recoverable composer.~~
- [ ] Add speech-to-command navigation using the existing command directory.
  - [x] ~~Show the interpreted destination before selection or spoken confirmation.~~
- [x] ~~Draft a Task, Event or Captchalogue note in Orion and review it in its editor before saving.~~
  - [x] ~~Preview a spoken draft request and confirm it with a separate utterance or button.~~
- [x] ~~Offer optional categorization, elaboration and research of a captured idea.~~
  - [x] ~~Preview a saved excerpt, generate an outline and review it as a separate Note.~~
  - [x] ~~Review the exact web query, follow inline citations and save research as a separate Note.~~
  - [x] ~~Offer optional Orion category and tag review after Captchalogue saves a note.~~
- [ ] Evaluate other uses by whether they reduce effort in an existing journey.

## Accounts, workspaces and first visit

- [x] ~~Login/signup, profile and persistent account preferences.~~
- [x] ~~Username suggestions, display-name autofill and required/password feedback.~~
- [x] ~~Readable auth containers and bounded animated backgrounds.~~
- [x] ~~Shared CAPTCHA lifetime, expiry and refusal recovery.~~
- [x] ~~Confirmed sign-in enters the dashboard before optional hydration finishes.~~
- [x] ~~Guest lifecycle and same-account conversion foundations.~~
- [x] ~~Workspace icon/emoji choices, bounded logo input and image-crop foundations.~~
- [x] ~~Bulk workspace summaries, placeholders and compact/expanded details.~~
- [x] ~~Server-capability-driven billing availability and account history interfaces.~~
- [ ] Complete intended-origin provider and signup-consent rollout checks.
- [ ] Recheck landing-page language and replace dense explanation with small useful demos.
- [ ] Complete mounted account erasure and uncertain-result recovery.
- [ ] Provide a real support destination before enabling submission.

## Shared forms and reusable UI

- [x] ~~Shared input, form, dialog, confirmation, draft and action infrastructure.~~
- [ ] Streamline form configuration for data types, input variants and validation.
  - [ ] Configure size, placement, grouping, appearance and behavior consistently.
  - [ ] Use generated forms where a bespoke form does not serve a specific need.
  - [x] ~~Verify generated Planner row append, removal, select state and failed-save retry.~~
  - [x] ~~Verify the shared field configuration and late reference options in Planner Details.~~
  - [x] ~~Use the shared generator in Journal Quick entry and verify editable Planner links and draft recovery.~~
  - [x] ~~Validate generated repeatable Planner fields and preserve older Habit data during edits.~~
  - [x] ~~Recover unfinished Planner edits after reload and save just the fields that changed.~~
  - [x] ~~Recover unfinished Event edits after reload, retry a failed save, and keep unrelated server changes.~~
  - [x] ~~Recover the latest new Event or Planner draft after an immediate reload.~~
  - [x] ~~Share Todo list editing across the context menu and sidebar with draft recovery and confirmed filter updates.~~
  - [x] ~~Jump to a Journal date and open its entry or start writing for that day, with draft recovery.~~
  - [ ] Verify select initialization and repeatable-array entry in migrated consumers.
- [ ] Recheck shared update-queue batching, deduplication and clear failure feedback in retained consumers.
- [ ] Prepare Fluxkit UI: inventory, package boundary, examples and release checks.
- [ ] Publish the reviewed Fluxkit UI package with installation/compatibility guidance.

## Future investigations

- [ ] Evaluate contextual suggestions and user-controlled completion feedback.
- [ ] Evaluate a local-only edition, backups and closed-app reminder constraints.
- [ ] Evaluate end-to-end encryption of user content with usable search and recovery.

These investigations do not promise offline synchronization or integrations that have not been verified.
