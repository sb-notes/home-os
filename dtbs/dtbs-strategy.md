---
tier: warm
project: Boots
topic: strategy
updated: 2026-04-21
---

# Boots — Strategy & Context

---

## About Boots

- **Company:** Boots
- **Size:** ~10 people (bootstrapped; ~2 years old)
- **Location:** UK
- **Founder/CEO:** Fern
- **Origin:** Fern previously built and led the data migration wing at a data consultancy (InterZeta), growing it from 2 people to ~60% of company value. That company was acquired by a large enterprise (Oct 2024). Fern left post-acquisition to found Boots in a startup environment.
- **Model:** Data quality and migration assessment consultancy that built its own platform. Platform now selling in its own right.

---

## The Platform

Boots built assessment tooling because they needed it for their own consultancy work. It has evolved into a standalone SaaS platform for data migration readiness assessment.

**Core capabilities:**

**Stage 1 — Database Forensics and Automated Rules**
- AI-driven statistical analysis and database profiling
- Automatic discovery of schema relationships (primary/foreign keys, even when not formally defined)
- Entity clustering: groups tables representing customer data and defines entity structures automatically
- Automated SQL-based data quality rule generation (structural patterns, conditional requirements — not just null checks)
- Speed: replaces what would typically require ~100 days of consultancy (e.g. 3 people for a month) with rapid automated assessment
- Impact measurement: quantifies the proportion of customers affected by errors without lengthy consultancy

**Stage 2 — Living Data Quality as a Service**
- Drift monitoring: detects data quality degradation over time (not just point-in-time snapshots)
- Continuous analysis: system acts as a living data analyst — monitors, detects new quality issues, adapts as business changes
- Smart prioritisation: one customer with 10,000 errors (low priority) vs. one error affecting 10,000 customers (high priority)
- Cleansing recommendations: suggests approaches; allows testing in a playground before applying to production

**Stage 3 — Data Modelling (aspirational)**
- Long-term vision; not near-term
- Would use accumulated drift analysis context to move into predictive modelling

**Agentic AI PoC (in development, Mar 2026):**
- AI agent queries Boots' semantic system context to generate full dashboards (charts, measures) on demand in a conversational interface
- Vision: lightweight consultancy layer where clients perform ad-hoc analysis without large analyst teams
- Scaling solution: as license base grows, AI agent reduces need for "data consultant account managers"

**Tech:** Heavy use of AI including traditional ML (SVCs, LGB models, n-rank); not just LLMs. Generates reusable, human-readable SQL procedures. GPT-4 used for development.

**Deployment:** Azure instance per client; connects via credentials to client database; runs analysis; delivers reports.

---

## Strategic Positioning — Core Anchor

**"Snowballing Data Pain in transformation"**

Organisations commit to major transformation programmes without truly understanding the data those programmes depend on. This creates hidden risk: migration failure, operational disruption, delays, unexpected tech debt. Existing data quality approaches are too slow and fragmented for transformation at pace. Boots makes data understanding immediate and structured — so organisations can change systems with confidence instead of assumptions.

This "why" emerged from Fern's conversation with Cedar (CEO of Trellis) in Feb 2026 and was crystallised in an email exchange. Ollie had been leading Fern toward the same framing independently. It's now the agreed strategic anchor.

**Vision of winning:**
- Structured Data Understanding becomes a standard early phase of transformation programmes
- Transformation leaders treat unknown data state as unacceptable risk
- Platform routinely used to assess readiness before migration or design begins
- Consultancies recommend the approach as standard practice
- Multiple concurrent programmes running the platform
- "So good you can't go back" customer retention

---

## Pricing & Service Model

**Tiered engagement:**
1. Free 30-minute programme health check / risk assessment call (top of funnel)
2. £12,000 data quality assessment for single system — 5-day engagement (health check product)
3. £50,000 annual license (with option to offset assessment cost against license fee)
4. Managed services

**Health Check as beachhead:** Six-week snapshot bundle (platform implementation + consultancy days) priced at roughly the cost of one week of programme delay — easy to say yes to.

**Upsell pathway:** Snapshot → ongoing license for metrics tracking → consultancy for data cleansing → full migration governance.

---

## Market & Competitive Position

**Target sector:** Housing associations and local authorities (UK). Expansion planned into other heavily regulated sectors (public sector, energy, NHS) where compliance drives data quality needs.

**NEC partnership:** Boots established a partnership with NEC (the leading social housing management software provider) in Oct 2025. NEC's product is strong but implementation is slow; Boots cuts through complexity and works directly with clients. Currently positioned as the only NEC migration partner in the housing technology space — "UK's only NEC migration partner for housing associations" is a defensible claim.

**Competitive advantage:**
- No known competitors offering equivalent governance tooling
- Platform delivers insights "two orders of magnitude" faster than traditional approaches
- Removes personal blame from difficult findings: "It's not them saying this is going to go wrong — it's the tool saying it's going to go wrong"
- Estimated 12–18 month head start if productionised effectively
- Existing consultancies struggle to communicate data issues without tooling — creates political standoffs that Boots resolves
- Can enter mid-transformation programmes — previously a market closed to consultancies

**Key market dynamics:**
- Data quality sector: 17.5% CAGR globally, driven by AI adoption
- Most transformation programmes are delayed; data risk is widely underestimated
- Housing associations are not data-literate organisations — existing tools are too technical
- Many are now on second phases of transformation after initial breakdowns

---

## GTM & Sales

**Primary channel:** Housing sector conferences and direct relationships via NEC network.

**Housing Technologies conference (Mar 2026):** Fern secured both a main stage speaking slot and a 3x3 booth. Results were exceptional — no direct competitors present; Boots positioned as complementary partner to all vendors. Data quality message strongly validated by both suppliers and clients. Immediate traction: 3 client contacts post-conference, 2 SOWs drafted within one week.

**Key clients:**
- **L&Q:** Anchor client. Unhealthy engagement — significant scope creep, unreasonable expectations; Fern unable to say no due to revenue dependency. Needs managing.
- **Northern Partnership Homes:** Mid-transformation (migrating from Open Housing to new platform); health check focused on source data quality; low-cost snapshot agreed to minimise client risk.
- **Friday call (post-Mar 21):** NEC-recommended, full migration programme at L&Q scale — potential second anchor client.

**Pipeline:** Conservative target: 1 additional anchor client + smaller full-license sales by year-end. Strong potential for 10–20 clients if pipeline is systematised.

**Sales ops:** Fern is sole sales resource; leads managed via spreadsheet. CRM urgently needed. Transcription → AI → CRM automation discussed.

**Partnership strategy:** Blocked until proven across 10+ clients and multiple major housing platform providers (NEC + 2–3 others).

---

## External Relationships

- **Cedar** (CEO, Trellis): Strategic advisor who helped Fern articulate the "strategic why." Introduced by Ollie (Session 1). Experienced in bootstrapping and dual consultancy/software tracks. Follow-up meetings ongoing.
- **Rightbrain (Ollie's employer):** Flagged as potentially relevant for Boots' sales automation needs (target market: service businesses, lead gen, rev ops).

---

## Advisory Infrastructure

- **Session cadence:** Monthly, evening slot (moved from fortnightly when Ollie started new role at Rightbrain)
- **Session format shift (from Session 4):** Challenges and concerns first, rather than updates
- **Notion:** Sessions DB and Actions DB maintained on advisory page
- **Next session:** 15 April 2026, evening
