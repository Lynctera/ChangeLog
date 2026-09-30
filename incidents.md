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

---

_Generated from the incident register. Last updated 2026-09-30._
