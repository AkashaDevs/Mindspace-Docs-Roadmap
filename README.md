# Mindspace

Mindspace brings tasks, calendars, notes, habits, goals and reminders into one workspace. It is being built by a developer with ADHD around a familiar problem: a thought is easy to lose, and a planning system is easy to stop using when life gets busy.

The aim is to make a small action easy: capture a thought, find it again, give it a time or reminder, and pick up where you left off. More detailed controls are available when you need them.

## What you can do

- Capture a note or task from shared quick-entry tools, then organize it later.
- See the same tasks through board, list, table and calendar views.
- Plan events and focus time alongside tasks and routines.
- Set one-off and recurring reminders, including selected weekdays and multi-week patterns.
- Track habits, keep a journal and record measurements over time.
- Return to unfinished work with saved drafts, recovery actions and searchable records.

## Features and roadmap

| Area | Feature inventory and remaining work |
| --- | --- |
| Client | [Dashboards, capture, navigation and interface](CLIENT_FEATURES.md) |
| Server | [Accounts, data, scheduling, billing and service limits](SERVER_FEATURES.md) |
| Progress | [Dated development updates and verification scope](PROGRESS.md) |

The inventories use **checked, struck-through items for implemented work with recorded verification**, and empty checkboxes for remaining work. A working foundation and a later improvement can both appear: having a Task board does not mean its drag performance or navigation is finished.

**Current status: active pre-1.0 development.** The inventories describe the development candidate reviewed on October 26, 2026. A checked item does not mean that change is already deployed to every hosted version. Current deployment and provider acceptance remain separate release gates. Paid enrollment and some integrations remain gated.

## Current focus

The next delivery pass prioritizes changes people can see and use immediately:

1. Bring the public feature lists up to date for both client and server.
2. Make the Task dashboard easier to enter, choose a view and filter by list; improve responsiveness.
3. Simplify Planner controls and make adding an event easy to find.
4. Make notification entries lead somewhere useful, with a clear route to history.
5. Improve sidebar context, compact controls and consistency between dashboards.

Deeper work on Notes loading, Orion AI, charting, forms and backend release readiness follows in separate, verifiable slices. Reliability and protection of user data remain release requirements throughout.

## Project structure

Mindspace has separate React/Vite client and Node/Express/MongoDB server projects. This public repository provides a combined product roadmap; implementation is maintained in separate client and server repositories. The client presents records and actions, while the server owns access, scheduling, subscription state and service limits.

Billing uses Stripe-hosted Checkout and the customer portal. Mindspace does not need to collect raw card numbers or security codes to provide subscriptions. The server inventory distinguishes implemented billing flows from the remaining provider, infrastructure and release checks.

Offline-only operation is being considered as a possible future edition. It is not a current feature or a commitment to a release date.
