# Mindspace server features and roadmap

[Overview](README.md) · [Client](CLIENT_FEATURES.md) · [Progress](PROGRESS.md)

Updated October 31, 2026. Checked and struck-through items have recorded implementation verification. Empty checkboxes remain open. Controlled database and provider-fixture tests establish development behavior; current deployment and provider acceptance are separate gates.

## Platform and access

- [x] ~~Separate Node/Express server and MongoDB/Mongoose data owners.~~
- [x] ~~Authenticated workspace-scoped routes and shared access checks.~~
- [x] ~~API/database health checks and environment-controlled capabilities.~~
- [x] ~~Token-verified, user-bound realtime socket registration.~~
- [x] ~~Shared schema, controller and service ownership for application records.~~
- [ ] Complete cross-owner retirement and background-delivery race acceptance.
- [ ] Finish intended-environment release, backup, recovery and operational checks.

## Accounts and preferences

- [x] ~~Credential signup/login, session refresh and account-bound preferences.~~
- [x] ~~Server password policy, complete-value comparison and versioned hash owner.~~
- [x] ~~Legacy credential reads without automatic credential rewriting.~~
- [x] ~~Bounded signup requests and safe diagnostic classification.~~
- [x] ~~Versioned terms/privacy acknowledgment and profile/preference persistence.~~
- [x] ~~Pending provider-signup agreement and continuation foundations.~~
- [x] ~~Temporary Guest expiry and same-account permanent conversion.~~
- [x] ~~Atomic local account cleanup and session-retirement admission foundations.~~
- [ ] Provision and verify signup-agreement storage on the rollout target.
- [ ] Complete intended-provider round trips and cached-client release acceptance.
- [ ] Complete explicit legacy credential recovery and coordinated reader deployment.
- [ ] Complete external-provider/media erasure, delayed writers and lost-result recovery.

## Core records and recovery

- [x] ~~Workspace, Task, Todo list/group, Planner/Event, Note, Goal, Habit, Stat and Daily Log owners.~~
- [x] ~~Persisted Task/group ordering and automatic matching group rules.~~
- [x] ~~Validate Task reorder list destinations, clear old group membership and retain the canonical parent of group destinations without transferring workspace ownership.~~
- [x] ~~Preserve existing finish time and progress history when completed Task moves are retried.~~
- [x] ~~Read only requested Task/group move metadata through an authorized, bounded endpoint, preserving schema defaults for older records.~~
  - [x] ~~Recover both baseline and current parent mirrors with requested Task move fields in one authorized read-only snapshot after a lost hierarchy-save response.~~
- [x] ~~Scoped Task/Reminder creation identities for duplicate-safe recovery.~~
- [x] ~~Validate new Task list/group destinations and the canonical Group parent in the creation transaction, while preserving confirmed retry/deletion recovery.~~
- [x] ~~Coordinate Task parent changes and canonical child mirrors in transactions across creation, single/bulk updates and hierarchy reorder.~~
- [x] ~~Reject cycles and unavailable or cross-workspace parents; roll graph, content and positions back together while preserving exact retry and completion behavior.~~
- [x] ~~Detach surviving children during permanent Task deletion, coordinate creation-retirement recovery, and return bounded graph confirmation/recovery metadata.~~
- [ ] Complete remaining clone, Trash and account/Workspace erasure graph-writer audits and end-to-end client graph acceptance.
- [x] ~~Shared recovery drafts with revision, capacity and retention rules.~~
- [x] ~~Task/Note/checklist conversion and follow-through foundations.~~
- [x] ~~Bounded lexical search and limited spelling recovery.~~
- [x] ~~Registered workspace cleanup and transaction-backed admission for verified writers.~~
- [x] ~~Read bounded Workspace retirement confirmations for the authenticated owner, returning IDs only and excluding unfinished or foreign deletions.~~
- [x] ~~Bulk workspace summaries.~~
- [x] ~~Account settings updates preserve unrelated categories, including concurrent distinct-category saves.~~
  - [x] ~~Persist stable Task-tab identities, presentation and one saved preset through the existing settings owner.~~
  - [x] ~~Retain bounded request validation, literal JSON values and explicit whole-settings reset.~~
- [ ] Add minimal-metadata, location-based Notes explorer reads.
  - [x] ~~Return projected note metadata with parent IDs and a stable cursor.~~
  - [x] ~~Scope selected-file reads and bound authorized folder pages and ancestor chains.~~
  - [x] ~~Persist one scoped sibling rank per reordered item and page it alongside older notes.~~
  - [ ] Install the ranked directory index on a dedicated development database and verify both cursor streams.
  - [x] ~~Persist file and folder moves in an authorized transaction, update descendant paths, and verify rollback and reload.~~
- [ ] Complete versioned export/restore coverage and unsupported-type guidance.
- [ ] Measure high-volume Stats aggregation and define complex-value chart contracts.
  - [x] ~~Accept and return typed Time Range values through authenticated Stat create, edit and list.~~

## Scheduling and notifications

- [x] ~~Shared scheduler and Reminder service owners.~~
- [x] ~~One-off, weekday, compound-duration and multi-week recurrence contracts.~~
- [x] ~~Source-linked Reminder lifecycle and uncertain-creation recovery.~~
- [x] ~~In-app/realtime plus capability-gated email and device-push paths.~~
- [x] ~~Snooze, interaction tracking and delivery-status foundations.~~
- [x] ~~Engagement-aware pacing and subject-interaction foundations.~~
- [x] ~~Server-owned notification entitlement checks.~~
- [ ] Reconcile notification detail, source and history contracts with the revised UI.
- [ ] Audit history pagination, retention, indexes and payload size for production scale.
- [ ] Verify queued delivery against retirement at execution time.
- [ ] Complete device, timezone, long-interruption and repeated-use acceptance.
- [ ] Install and verify required pacing indexes and schedule maintenance on intended targets.

## Billing and payment information

Stripe is the provider. Hosted Checkout and the customer portal collect/manage payment details. The application boundary excludes raw card numbers and security codes. Infrastructure encryption and access still need verification; this is not a claim of end-to-end encryption of all Mindspace data.

- [x] ~~Server-selected pricing and hosted Stripe Checkout.~~
- [x] ~~Account-bound hosted portal for subscription and payment-detail management.~~
- [x] ~~Signed raw-body webhooks and provider-confirmed reconciliation.~~
- [x] ~~Public-safe billing capabilities instead of client-invented plan state.~~
- [x] ~~Bounded request contracts rejecting unsupported raw payment fields.~~
- [x] ~~Authorized invoice/payment history and safe hosted document/receipt links.~~
  - [x] ~~Scoped paging and verified recorded-customer discovery.~~
  - [x] ~~Cross-account refusal and retained history during retry.~~
- [x] ~~Separate observed subscription history and duplicate-event handling.~~
  - [x] ~~Provider-source lineage, replacement ordering and fenced reads.~~
- [x] ~~Saved Checkout recovery and persistent account-closing admission.~~
- [x] ~~Provider-first erasure and local cleanup foundations.~~
- [x] ~~Hosted lifecycle sandbox proof for an earlier recorded release candidate.~~
- [ ] Re-prove hosted billing and history on the intended current candidate.
  - [ ] Verify interruption, renewal, failure/recovery, cancellation and resumption.
  - [ ] Verify paid-period access, downgrade and preserved existing records.
  - [ ] Verify erasure, concurrent provider changes and zero-residue cleanup.
- [ ] Complete account-wide historical coverage including undiscovered legacy provider records.
- [ ] Install/verify customer-claim and subscription-history storage/index requirements.
- [ ] Verify deployed HTTPS, database/backup encryption, access and retention.
- [ ] Complete deferred subscription producers before enabling them.
- [ ] Make a separate launch decision before enabling paid enrollment or Hero benefits.

Legacy direct-card payment and custom payment-method APIs are deliberately unavailable. Hosted operations replace that approach; unavailable endpoints are not counted as finished payment features.

## Subscription capabilities and limits

Approved policy: **Tasks are unlimited**. Free allows **3 Todo lists per workspace and 8 groups per list**. Pro currently allows **25 lists per workspace and 200 groups per list**, with a later deliberate switch to unlimited capacity possible through configuration.

- [x] ~~Shared plan catalog, effective-plan resolver and safe capabilities.~~
- [x] ~~Server-enforced owned-workspace capacity.~~
- [x] ~~Registered Todo list/group capacity policies and guarded mutations.~~
- [x] ~~Database-backed atomic capacity with independent-backend contention proof.~~
- [x] ~~Duplicate-safe container creation and interrupted/lost-response recovery.~~
- [x] ~~Authenticated usage snapshots and retained drafts after refusal.~~
- [x] ~~Provider-confirmed paid delivery and delinquency/expiry fail closure.~~
- [ ] Complete the feature and mutation coverage matrix for release.
  - [ ] Cover create, bulk, import, clone, restore, transfer, conversion and jobs.
  - [ ] Define charged ownership, capacity release, downgrade and retry per allowance.
- [ ] Select and enforce remaining published allowances through registered adapters.
  - [ ] Resolve tags, categories, editor seats and storage policy before advertising enforcement.
  - [ ] Account for actual upload bytes, replacement and deletion where enabled.
- [ ] Extend canonical usage feedback to every retained limited action.
- [ ] Verify transactions and indexes on intended development before rollout.
- [ ] Complete final-candidate adversarial, multi-instance and lifecycle acceptance.

Frontend visibility is guidance. The server remains authoritative for enforced capabilities and allowances.

## Orion AI and future services

- [ ] Audit existing generation providers, prompts and selected data.
- [ ] Restore agentic generation through explicit capabilities and account authorization.
- [ ] Explain model, context, retention and instructions in the client.
- [ ] Add bounded confirmed Task, Event and Note tool contracts for chat/voice.
- [ ] Add optional classification, elaboration and research with minimal necessary data.
- [ ] Define cost/rate limits, cancellation and useful failure recovery.
- [ ] Evaluate offline architecture and content encryption as separate future scopes.

## Release and maintainability

- [x] ~~Focused unit, mounted-browser and disposable-database regression tooling.~~
- [x] ~~Separate build/deployment and public-safe capability configuration.~~
- [x] ~~Explicit audit/provision tools instead of request-time production index creation.~~
- [ ] Finish paired retention/index rollout, current provider proof and recovery gates.
- [ ] Preserve security, isolation and data safety throughout visual improvements.
- [ ] Document any server-independent contracts needed by the Fluxkit UI package.
