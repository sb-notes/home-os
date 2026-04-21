---
tier: warm
project: Violet
topic: strategy
updated: 2026-04-21
---

# Violet — Strategy & Context

---

## About Violet

- **Company:** Violet (codenamed; real name withheld)
- **URL:** the platform's .co.uk domain
- **Size:** 2 co-founders + 1 collaborator
- **Location:** UK
- **Co-founders:** Reed (product/business lead) and Slate (software engineer)
- **Third collaborator:** Moss (Slack)
- **Model:** LLM-powered perfume discovery platform; monetises via affiliate links
- **Advisory:** Pro bono product strategy; monthly calls

---

## The Platform

An AI-powered perfume discovery platform. Users find fragrances via celebrity, mood, scent type, budget, perfume house, or occasion inputs. The platform then surfaces matching perfumes and monetises via affiliate links to e-commerce retailers.

**Tech stack:**
- LLM recommender (Claude; ~3p/conversation)
- Coding assistant (Claude Code)
- Copy/synthesis/image generation (Gemini)
- Search (Google SERP API)
- Custom stealth scraping engine (celebrity news + retailer data)

**Database:**
- ~50,000 perfumes known
- ~300 currently saleable via Amazon
- Heading toward ~9,000 purchasable once broader affiliate catalogues integrated
- Taxonomy: 40 accords, 465 notes
- Data sourcing shifted from Amazon-only to direct scraping of ~100 Shopify perfume shops and perfume houses

**Key features shipped (as of Session 4, Mar 2026):**
- AI chat assistant
- Celebrity discovery pages (JSON-LD schema markup)
- Perfume house pages with AI-generated scent forest imagery
- Launches calendar
- Browse by notes / accords / mood / budget
- Cross-linked perfume detail pages
- Mobile-first design
- Real-time price tracker (sale detection at 30%+ discount)
- Automated social content pipeline (Instagram video/image)
- "Stalker" celebrity news engine (scrapes web → Gemini synthesises editorial articles)

**In development / disabled:**
- Perfume Chemist Studio — reverse-engineer perfumes, ingredient costs, compliance checking, cost optimisation, house DNA comparison. Recommended: put behind paywall or beta programme. B2B value to perfume manufacturers and amateur perfumers.
- ML model (Slate) — semantic perfume search based on user language rather than house descriptions; scientific paper database discovered, potential for published research / thought leadership
- MCP server PoC — agent can search DB for price drops, compositions, make purchase recommendations; 5% commission potential on agent-mediated purchases

---

## Brand & Naming

**The problem:** the current brand name reads as traditional / "granny lavender" to the 24–34 target audience. The .com domain for the current name is owned by a real married couple who make perfumes — further complicating the position.

**Recommended rebrand:** lean into AI-forward identity.

**Top candidate: Perfuma**
- Coined, short, memorable
- Legally defensible (no obvious conflicts found so far)
- Clean namespace
- .ai domain available (~£88/year on Hostinger)
- Perfumer.ai available (~£137/year)
- parfuma.com taken (Belgian luxury perfumery)
- perfuma.com availability unconfirmed — **urgent to check**

**Pre-commit checks outstanding:**
1. perfuma.com — availability and pricing
2. UKIPO trademark — Class 35 (retail/online services) + Class 44 (beauty/fragrance advisory)
3. Companies House — search for "Perfuma"

**Status:** Reed and Slate in disagreement over naming direction. Unresolved.

**Visual identity direction:** stronger, bolder, modern; Frozen/Pixar-inspired typography with whimsical but modern aesthetic. Commission via Upwork/Fiverr/99designs (~£90 budget).

**PR angle:** "World's first AI-powered perfume house" — inspired by Mackmyra (Swedish AI whiskey distillery; got Forbes coverage). Name needs to work for both consumer-facing discovery platform AND MCP server for scent/perfume data.

**Male version planned:** "Leatherthorn for Cologne" — text-only plan, not yet built.

---

## ICP & Personas

### Primary ICP (current)
**24–34 year old women buying perfume for themselves**
- Follow celebrities; spend on fashion
- Personality/celebrity-driven purchase behaviour
- Reached via TikTok, Snapchat, Instagram
- Respond positively to AI-forward positioning (lean in, don't hide it)

### Secondary ICP
**"Tech Girls"**
- Growing demographic graduating from CS programmes
- May respond strongly to AI-forward identity

### Legacy persona — Last Minute Larry
- Man in 20s–60s buying perfume last-minute as a gift for a female partner
- Nervous about buying perfume; starts with what's on her dresser
- Values: fast delivery (Amazon Prime), cheap, de-risked ("similar to what she already wears"), good returns
- Key triggers: Valentine's Day, anniversary, birthday, Christmas, Mother's Day
- Deprioritised after Session 3 based on Search Console data

---

## Growth & Marketing Strategy

### SEO & content
- Blog launched with AI-generated content (Gemini); weekly cadence recommended
- Google Search Console: 70+ impressions as of Feb 2026, overwhelmingly celebrity-related
- Sitemap trimmed to purchasable perfumes only (crawler had given up on 10K pages)
- Thread Google Trends search phrases + top-selling perfume names into generated page copy for intent capture

### Celebrity content as primary growth lever
- Early data strongly indicates "celebrity → what they wear → buy" is the key top-of-funnel path
- Celebrity pages with schema/JSON-LD markup
- Editorial-style content enriched with sourced context
- Stalker engine automates this at scale

### "Sniping" strategy
- When big brands launch with massive budgets, create cheaper-alternative content to capture demand spillover
- "Le Intent" by Zadig identified as a test case

### Newsletter / mailing list
- 400 emails/month free tier set up
- Triggers: price drops, new releases, "biggest movers"
- VIP price alerts as potential paid tier
- Exit-intent popup recommended (over inline-only signup)
- Personalisation planned via session-to-user linking after signup

### Influencer / brand face strategy
- Partner with influencer who brings existing audience; offer equity (no cash available)
- Target: unpaid YouTube/TikTok perfume reviewers, actors, musicians with business sense
- Reed's brother and niece Isla may have agent network connections
- Add "Work with us" section to site

### Referral mechanic
- Refer-a-friend (Dropbox model); offer share of affiliate fee as discount

### Social channels
- TikTok and Snapchat likely primary for 24–34 female ICP
- Research where top perfume brands place promotional spend

### Content ideas
- Perfume vs. AI blind testing with reviewers
- Sample discovery programme (£6 across 10 sites vs £60 for bottles)
- Celebrity/launch/trend editorial

---

## Monetisation & Revenue Models

### Current
- Amazon affiliate links only
- Zero conversions as of Session 1 (Jan 2026)

### Next affiliate targets
- **Debenhams** — application held until site quality polished; ~100 celebrity perfumes
- **Awin network** — 5 perfume sellers; one has ~9,000 perfumes

### Other revenue models discussed
1. AI-powered perfume house — create scents that fill market gaps
2. Samples at 99p + postage
3. White-label platform for influencer-branded perfume lines
4. VIP price alerts as paid subscription tier
5. Direct-to-house affiliate referral traffic for better terms
6. B2B — Chemist Studio tools for actual perfume manufacturers and amateur perfumers
7. MCP / agentic commerce — 5% commission on agent-mediated purchases

---

## Competitive Landscape

- No direct AI-powered perfume discovery competitor identified
- Closest: celebrity magazine curated perfume editorial (Vogue Beauty etc.)
- Competitors: image-heavy, magazine-style, longer editorial
- Debenhams: ~100 celebrity perfumes
- Awin network: broader catalogues
- Key differentiator: only platform aggregating all perfume house data in one place with better UX; data depth is significant first-mover advantage (cloneable but hard to replicate quickly)

---

## Analytics & Instrumentation

- Google Search Console / Webmaster Tools: active
- Some tracking on buy/purchase button click flow
- **Gaps:** page landings, journey entry points, buy clicks, email signups, session tracking for personalisation
- Weekly analytics review cadence recommended
- Mixpanel or Google Analytics / Data Studio discussed as options
