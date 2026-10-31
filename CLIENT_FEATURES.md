# Mindspace client features and roadmap

[Overview](README.md) · [Server](SERVER_FEATURES.md) · [Progress](PROGRESS.md)

Updated October 31, 2026. Checked and struck-through items have implementation and recorded development verification. Empty checkboxes remain open. New usability reports stay open even when an earlier implementation test passed. These are development statuses, not a claim about every hosted version.

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
- [ ] Make dashboard-specific left-sidebar tools easy to discover and select.
- [ ] Redesign the right sidebar around useful compact widgets and designed tabs.
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
- [ ] Clarify opening Tasks, choosing a view, opening list tools and selecting a list filter.
  - [x] ~~Expose Lists beside the tabs using the existing desktop tools and mobile left drawer.~~
  - [x] ~~Keep loaded Task records and shared list selection while switching views.~~
- [ ] Finish measured list-toggle and drag pickup responsiveness on representative data.
  - [ ] Recheck zoomed dragging, long boards and interactions after extended use.
  - [ ] Meet practical keyboard and physical-phone acceptance alongside browser tests.
- [ ] Support several independently configured instances of the same view type.
  - [x] ~~Stable repeated instances, account preset and independent Kanban presentation.~~
  - [x] ~~Keep Calendar dates, display mode, selected-day focus and applied filters independent in each tab and the account preset.~~
  - [x] ~~Apply Calendar text filters to retained Tasks locally, with removal restoring the matching list data.~~
  - [x] ~~Keep primary Calendar actions and date controls visible as the available width changes.~~
  - [ ] Persist Table/Detailed expansion and sorting, DataTable filters/grouping, and remaining nested options at their current owners.
- [ ] Recheck table density and timestamp input presentation in the visual pass.
- [ ] Finish remaining text/Markdown/JSON import/export and subtask/sidebar drag workflows.

## Planner and routines

- [x] ~~Planner, Calendar and Event records with day and scheduling views.~~
- [x] ~~Calendar visibility filters use retained data.~~
- [x] ~~Shared Event entry and Task-to-Time scheduling actions.~~
- [x] ~~Routine, focus, day, week and cycle planning foundations.~~
- [ ] Reduce Planner toolbar clutter and clarify primary actions.
- [ ] Provide an obvious compact quick-add Event form with progressive detail.
- [ ] Recheck date selection, day detail and return-to-plan journeys.
- [ ] Verify external calendar providers and read/write behavior before claiming full integration.

## Notes and Journal

- [x] ~~Hierarchical Notes explorer, note editing and Scratchpad capture.~~
- [x] ~~Compact collapsible Captchalogue that retains its draft.~~
- [x] ~~Clearer capture and note containers with restrained borders and shadows.~~
- [x] ~~Journal grid, larger grid and list views with formatted Markdown previews.~~
- [x] ~~Journal date navigation and recent-entry sidebar.~~
- [ ] Load the Notes explorer by location and minimal metadata.
  - [ ] Fetch note bodies on opening and folder contents only when needed.
  - [ ] Restore the last folder, expanded hierarchy and selected record.
  - [ ] Keep loading, empty, retry and missing-record states understandable.
- [ ] Add familiar explorer reorganization and inline rename interactions.
  - [ ] Drag/drop files and folders with safe move feedback.
  - [ ] Rename from the keyboard or delayed second click, selecting the existing name.
  - [ ] Save with Enter, blur or checkmark; cancel with X; allow Shift+Enter for newline.
- [ ] Recheck editor switching, wider layouts and compact file details.
- [ ] Finish supported note imports and grouped sticky-note workflows.

## Reminders and notifications

- [x] ~~One-off and flexible recurrence, including selected weekdays and multi-week rules.~~
- [x] ~~Fast capture followed by later timing, context and delivery enrichment.~~
- [x] ~~Linked Reminder actions from Tasks, Notes, Goals and Daily Logs.~~
- [x] ~~Manage several reminders for one source without hiding separate identities.~~
- [x] ~~In-app notifications, snooze and channel/device settings foundations.~~
- [x] ~~Engagement-aware pacing foundations with inspectable timing context.~~
- [x] ~~Connect header entries to their own notification details and full history table.~~
  - [x] ~~Keep an explicit one-action related-item destination alongside notification details.~~
  - [x] ~~Read scoped canonical records, show confirmed opening status and offer inline retry or history when a notification is unavailable.~~
  - [x] ~~Preserve an unfinished Quick Jot thought when detail/history navigation is declined.~~
  - [ ] Complete return journeys from deleted or unavailable related source items.
- [ ] Unify reminder, delivery-status and history presentation.
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
- [ ] Make continuous lines deliberate and readable across missing samples.
- [ ] Restore and verify new data-key creation from the data table.
- [ ] Improve control density and discovery of existing global Stat entry.
- [ ] Add practical chart range navigation inspired by financial charts.
- [ ] Design complex-value charts, trend lines and useful analysis.

## Orion AI

- [ ] Restore agentic Insights and its entry through shared capability/action owners.
- [ ] Explain the Recommendations model, selected data and instructions.
- [ ] Add basic chat with clear scope and data controls.
- [ ] Add speech-to-command navigation using the existing command directory.
  - [ ] Show the interpreted action prominently before selection or spoken confirmation.
- [ ] Turn captured ideas into Tasks, Events or Captchalogue notes.
- [ ] Offer optional categorization, elaboration and research of a captured idea.
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
  - [ ] Verify select initialization and repeatable-array entry in migrated consumers.
- [ ] Recheck shared update-queue batching, deduplication and clear failure feedback in retained consumers.
- [ ] Prepare Fluxkit UI: inventory, package boundary, examples and release checks.
- [ ] Publish the reviewed Fluxkit UI package with installation/compatibility guidance.

## Future investigations

- [ ] Evaluate contextual suggestions and user-controlled completion feedback.
- [ ] Evaluate a local-only edition, backups and closed-app reminder constraints.
- [ ] Evaluate end-to-end encryption of user content with usable search and recovery.

These investigations do not promise offline synchronization or integrations that have not been verified.
