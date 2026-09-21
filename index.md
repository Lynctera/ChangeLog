# Changelog

All notable changes to this project will be documented in this file.

This project follows the [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) format and [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.3.0] - 2026-09-21

Platform work promoted to production between 21 July and 21 September 2026, grouped by theme. The period carried 469 feature changes, 1,248 fixes, 16 performance changes and 65 refactors, promoted to production in reviewed batches after a soak period on the development environment.

### Added
- Inbox intelligence for connected mailboxes: a daily brief, a commitment ledger showing what a mailbox owes and is waiting on, searchable mail history, and an interaction map of where the load comes from.
- Reply drafting that draws on pre-computed thread summaries and commitments, and proposes meeting times from the owner's calendar. Drafts can be produced for messages the platform has not yet ingested by reading them from the live mailbox.
- Mailbox health monitoring that warns when the mail provider refuses reads and clears on the next success, with a daily full-mailbox reconciliation.
- A mail access audit covering every surface that reads or exports mail content, with an operations access-log page.
- Email filter rules that can test recipients, body, attachment names and attachment presence, including regular-expression matching; category synchronisation now follows category renames.
- Document extraction records per-field confidence and source, routes low-confidence fields to human review, and meters billed pages on every extraction path. Extraction results held by the analysis service are deleted once persisted.
- Research artefacts carry numbered citations with a sources panel; web evidence is gathered through a shared, consent-gated web knowledge source.
- Personal AI memory: a per-user style card that shapes drafting and is attributed in answers, visible and manageable in the portal.
- A knowledge agent that learns a library's corpus from the tenant's own data; matter background is available to case and precedent chat.
- Precedent library improvements: two-stage document-type resolution, body-text search, effective dates surfaced to the model, and reconcile/fix tooling.
- AI-led interviews: session recovery after a connection gap, timeouts for abandoned interviews, a record-and-transcribe fallback, and respondent data redaction once the retention window expires.
- Relationship graph: entity merging and connection search, freshness refresh on ingest, and a verification stage.
- Process workspace guardrails: per-tenant spend ceilings, concurrency caps for document assessments, and cancellation of background runs when a tenant's persistence path trips.
- Outlook add-in: feedback on an answer is stored with the excerpt and the sources that were shown.
- External data through governed MCP servers with bring-your-own-key subscriptions; tool arguments are validated against pinned schemas before leaving the platform.
- The reconciliation daily review runs as a governed workflow with a conditional human-approval gate.
- Classification analytics: a review queue as the first ground truth, a taxonomy coverage view, and proposed sub-categories for oversized buckets.
- Public demo-request form with server-side lead capture and notification.

### Changed
- Portal design system tokenised (type and elevation scales) so a brand can be skinned without code changes; refreshed inbox views.
- AI calls moved to the Responses API surface, with strict JSON schemas where the provider supports them, prompt caching, and per-turn reasoning-effort control.
- Skills became a governed AI-definition family alongside agents and processes, propagating from the template to every tenant.
- Almagest AI public site redesigned: landing page, How It Works and team pages.

### Fixed
- Over a thousand reliability, correctness and data-accuracy fixes across the portal, email listener, process workspace, tracking and AI framework, found through expanded automated testing, nightly regression runs and a live end-to-end suite on a scratch tenant.

### Security
- A single HTML escaper across the portal; every listed dynamic-HTML site is escaped, and a scanner keeps them escaped.
- User-uploaded files never render as active content on the portal origin; rendered markdown makes no remote fetches.
- Tenant-bound key checks on every keyed HTTP function; tenant binding requires an active mapping, with the domain-based fallback removed.
- Platform identity headers are trusted only when written by the platform; email-claim trust is checked on every email-keyed path before caching.
- The mailbox onboarding cookie can no longer choose a directory or a mailbox; a retired brand's open self-signup was closed.
- Production configuration is checked for any key still pointing at a non-production resource.
- Tool-call approvals are recorded in the ISO 42001 decision audit; SOC 2 evidence is now generated from live configuration.

### Performance
- Session sharding and claim-at-enqueue for document assessments, a configurable per-tenant hot window before execution-log offload, and sixteen targeted performance changes.

## [0.2.0] - 2026-07-21

A catch-up summary of platform work since the 0.1.0 scaffold, grouped by theme.

### Added
- AI-assisted reconciliation engine with automated matching and a human review step for exceptions.
- Due diligence, RFP/vendor-evaluation, and investment-readiness scoring — all built on one configurable analysis engine.
- AI-led interviews for structured data collection.
- Conversational AI assistant that answers questions by searching an organization's documents and knowledge base.
- Document intake and classification pipeline for incoming files.
- Securities and market data enrichment sourced from public filings.
- Platform credits and usage-based billing.
- Searchable knowledge base with training content.
- Configurable, no-code workflow engine for multi-step business processes.

### Changed
- Rebuilt client portal with a refreshed design system and a redesigned home dashboard.
- Improved email intelligence and categorization accuracy.

### Fixed
- Numerous reliability, performance, and data-accuracy fixes from expanded internal testing.

### Security
- Ongoing work toward SOC 2, ISO 27001, and ISO 42001 alignment.

## [0.1.0] - 2025-10-20

### Added
- Initial public changelog scaffold.

