---
title: Incidents
permalink: /incidents/
---

# Incidents

Security, privacy and availability incidents on the Lynctera platform, and what we did about them. An entry appears here once the incident is resolved and its internal review is complete; the internal record holds the full timeline, root cause and telemetry.

Severity follows our incident response plan: **P0** active exploitation, **P1** high risk without proven exploitation, **P2** outages and degraded controls, **P3** low-risk events. To report a security concern, email help@yellowbe.io.

See also the [changelog](./) for what has shipped.

## 2026-07-24 — Document categories from one client's template applied to other libraries

**Severity:** P2 Medium · **Status:** Resolved
**Customer impact:** Four customer libraries showed incorrect category labels for a period. No customer's documents were visible to any other customer, and no data was lost.
**Duration:** Present from 6 May 2026; found and corrected on 24 July 2026

A document-classification template built for one client was set as the platform default, so documents in four other libraries were categorised and labelled with that client's categories. Each customer's documents stayed in that customer's own isolated database throughout; the effect was incorrect labels and the exposure of one client's category names to other users. The default was replaced with a neutral template, the affected libraries were reset and re-classified, and a build-time check now prevents any client-specific template from becoming the default.

## 2026-06-23 — Internal alert delivery interruption

**Severity:** P2 Medium · **Status:** Resolved
**Customer impact:** None. Customer-facing services were unaffected; internal alert notifications to one team channel were delayed.
**Duration:** 23 June to 14 July 2026, and 21 July to 11 August 2026

A connector that Microsoft had retired sat behind our team's alert channel and began rejecting messages, so operational alerts stopped arriving in that channel while continuing to arrive by email. A second, shorter interruption followed a credential rotation. Both affected internal monitoring only; no customer service, data or commitment was affected. Alert delivery now uses a supported channel with an independent alert on delivery failure, and the notifier refreshes its credentials automatically.

## 2026-06-05 — Administrator account outage

**Severity:** P1 High · **Status:** Resolved
**Customer impact:** None. The platform, customer sign-in and customer data were unaffected.
**Duration:** About two hours to restore primary access

During routine clean-up of a retired directory, an operator-assisted tool ran a bulk account deletion against the wrong Microsoft 365 directory, removing our internal staff accounts. Customer-facing services run on separate identities and kept working, and the customer sign-in directory is separate and was not touched. Accounts were recreated and mailboxes restored within about two hours with Microsoft support; some internal chat history was lost. We now require explicit confirmation of the target directory before any destructive identity operation, handle identity changes read-only first and one account at a time, and are adding audit-log export and alerting for bulk account deletions.

---

_Generated from the incident register. Last updated 2026-09-22._
