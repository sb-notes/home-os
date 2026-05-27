# Lavender Thorn — Current State (2 May 2026)

<!-- Auto-synced from Notion. Last sync: 2026-05-27 06:18 UTC -->

<!-- ANCHOR -->
---
## Update — 9 May 2026 (source: weekly wrap-up clarification)
### Session cadence
- **4th Wednesday of each month, 7:30pm.**
- Next session: **Wednesday 27 May 2026, 7:30pm.**
---
**Project:** Lavender Thorn HBN Advisory
**Topic:** Consulting client (HBN Advisory)
**Last updated:** 4 April 2026
---
## Engagement Overview
- Advisory is pro bono; Ollie is Product Strategist
- Cadence: started fortnightly, now **monthly** calls (moved to evening slot 19:30 once Ollie started new role at RightBrain)
- Co-founders: **Paul** (product/business) and **Matt** (software engineer); third collaborator **Marius** mentioned in Slack channel
- Team comms: Slack channel "perfumist" (Paul, Matt, Marius)
- Video calls: switched from Google Meet to **Jitsi** due to audio issues
- Sessions DB and Actions DB in Notion, mirroring DataBoots setup
## Platform & Product
- **URL:** [lavender-thorn.co.uk](http://lavender-thorn.co.uk/) (current); .app domain used originally under Perfumista name
- **Core mechanic:** LLM-powered perfume discovery platform; users find fragrances via celebrity, mood, scent type, budget, house, occasion inputs; monetises via affiliate links
- **Tech stack:** Claude for the LLM recommender (~3p/conversation); Claude Code for coding; Gemini for copy generation, synthesis, and image generation; Google's SERP API for search; custom stealth scraping engine for celebrity news and retailer data
- **Database:** ~50,000 perfumes known; ~300 currently saleable via Amazon; heading toward 9,000 purchasable once broader affiliate catalogues are integrated
- **Taxonomy:** refined to 40 accords and 465 notes
- **Data sourcing:** shifted from Amazon-only to direct scraping of ~100 Shopify perfume shops and perfume houses for higher-quality notes, accords, pricing, and sale data
- **Price tracking:** real-time price tracker across Shopify shops; automated sale detection (30%+ discounts)
- **Content engine:** "Stalker" — celebrity news engine that scrapes web for celebrity/perfume news, then Gemini synthesises into editorial articles; automated Instagram video/image content pipeline for social
- **Site features shipped (as of Session 5, Feb 2026):** AI chat assistant, celebrity discovery pages with JSON-LD schema markup, perfume house pages with AI-generated scent forest imagery, launches calendar, browse by notes/accords/mood/budget, cross-linked perfume detail pages, budget-tier browsing, mobile-first design
- **Perfume Chemist Studio (currently disabled):** reverse-engineer perfumes, see ingredient costs from chemical suppliers on Shopify, compliance checking, cost optimisation, house DNA comparison tool showing brand signature notes and accords; recommended to put behind paywall or beta programme
- **MCP server:** proof-of-concept built for Shopify's agentic purchase framework; agent can search DB for price drops, perfume compositions, and make purchase recommendations; potential 5% commission on agent-mediated purchases
- **ML R&D (Matt):** building a machine learning model for semantic perfume search based on user language (how people talk about perfumes) rather than house descriptions; discovered database of scientific papers on scent that could support published research / thought leadership
## Brand & Naming
- **Original name:** Perfumista — abandoned because [perfumista.co.uk](http://perfumista.co.uk/) is an active UK business (~429 Trustpilot reviews, ~$5M revenue)
- **Current name:** Lavender Thorn — AI-generated (ChatGPT); discovered to trace back to surnames of a real married couple who make perfumes; [lavenderthorn.com](http://lavenderthorn.com/) domain is owned by them
- **Brand perception problem:** "Lavender Thorn" skews too traditional / "granny lavender" for the 24–34 target audience
- **Recommended rebrand:** lean into AI-forward identity; top candidate **Perfuma** (coined, short, legally defensible, clean namespace); [Perfuma.ai](http://perfuma.ai/) available at ~£88/year on Hostinger; [Perfumer.ai](http://perfumer.ai/) available at ~£137/year; [parfuma.com](http://parfuma.com/) taken (Belgian luxury perfumery); [perfuma.com](http://perfuma.com/) availability unconfirmed — flagged as urgent to check
- **Pre-commit checks needed:** (1) [perfuma.com](http://perfuma.com/) domain availability/pricing, (2) UKIPO trademark search Class 35 + Class 44, (3) Companies House search for "Perfuma"
- **Paul and Matt currently in disagreement** over naming direction
- **Visual identity direction:** stronger, bolder, modern; Frozen/Pixar-inspired typography with whimsical but modern aesthetic; commission via Upwork/Fiverr/99designs (~£90 budget suggested)
- **Broader strategic context:** name needs to work both as consumer-facing perfume discovery platform AND as MCP server for scent/perfume data
- **PR angle:** "World's first AI-powered perfume house" — inspired by Mackmyra (Swedish AI-powered whiskey distillery that got Forbes coverage)
- **Male version planned:** "Leatherthorn for Cologne" — text-only plan, not yet built
## ICP & Personas
- **Evolution:** Session 1 focused on "Last Minute Larry" (men buying perfume last-minute for female partners); by Session 5 pivoted to young women buying for themselves after early Search Console data showed celebrity-driven impressions dominating
- **Primary ICP (current):** 24–34 year old women who buy perfume for themselves, follow celebrities, spend on fashion; personality/celebrity-driven purchase behaviour
- **Secondary ICP:** "Tech Girls" — growing demographic graduating from CS programmes who may respond positively to AI-forward positioning
- **Legacy persona:** "Last Minute Larry" — man in 20s–60s buying perfume as a last-minute gift for female partner; nervous about buying perfume, starts with what's on her dresser; values: fast delivery (Amazon Prime), cheap, de-risked ("similar to what she already wears"), good returns; key triggers: Valentine's Day, anniversary, birthday, Christmas, Mother's Day
- **Key ICP insight:** embrace AI positioning with target audience rather than hiding it; lean into authenticity and capability
## Growth & Marketing Strategy
- **SEO & content:** blog launched with AI-generated content (Gemini); weekly cadence recommended; Google Search Console showing impressions (70+ as of Feb 2026), overwhelmingly celebrity-related; sitemap trimmed to purchasable perfumes only after crawler gave up on 10K pages; need to thread Google Trends search phrases and top-selling perfume names into generated page copy for intent capture
- **Celebrity content as primary growth lever:** early data strongly indicates "celebrity → what they wear → buy" is the top-of-funnel path; celebrity pages with schema/JSON-LD markup; editorial-style content enriched with sourced context
- **"Sniping" strategy:** when big brands launch with massive budgets, create cheaper-alternative content to capture demand spillover; "Le Intent" by Zadig identified as a test case
- **Newsletter / mailing list:** set up with 400 emails/month free tier; triggers: price drops, new releases, "biggest movers"; VIP price alerts as potential paid tier; exit-intent popup recommended over inline-only signup; personalisation planned via session-to-user linking after signup
- **Influencer / brand face strategy:** partner with influencer who brings existing audience; offer equity (no cash available); target unpaid YouTube/TikTok perfume reviewers, actors, musicians with business sense; Paul's brother and niece Isla may have agent network connections; add "Work with us" section to site
- **Referral mechanic:** refer-a-friend discussed (Dropbox model); could offer share of affiliate fee as discount
- **Social channels:** TikTok and Snapchat likely primary channels for 24–34 female ICP; need to research where top perfume brands are placing promotional spend
- **Content ideas:** perfume vs. AI blind testing with reviewers; sample discovery programme (£6 across 10 sites vs £60 for bottles); celebrity/launch/trend editorial
- **Competitor analysis:** closest competitors are celebrity magazine-style curated perfume sites (Vogue Beauty etc.); no direct AI-powered competitor identified; recommended teardown of Debenhams perfume page + 3–5 Awin network perfume sellers for common UX patterns
## Monetisation & Revenue Models
- **Current:** Amazon affiliate links (only); zero conversions as of Session 1 (Jan 2026)
- **Next affiliate target:** Debenhams — application held until site quality is polished; Awin affiliate network has 5 perfume sellers, one with ~9,000 perfumes
- **Affiliate strategy evolution:** moving away from Amazon-only toward Debenhams and other UK e-commerce affiliate programmes; multi-retailer buy/price comparison planned
- **MCP / agentic commerce:** proof-of-concept MCP server for Shopify; 5% commission potential; positions the platform for agentic purchase flows
- **Other revenue models discussed:** (1) AI-powered perfume house creating scents that fill market gaps, (2) samples at 99p + postage, (3) white-label platform for influencer-branded perfume lines, (4) VIP price alerts as paid subscription tier, (5) direct-to-house affiliate referral traffic for better terms
- **B2B opportunity:** chemist studio tools have value to actual perfume manufacturers and amateur perfumer community (comparable to model railway enthusiast spend ~£4K/year)
## Key Metrics & Traction
- As of Session 1 (Jan 2026): ~10 conversations, zero conversions, negligible traffic
- As of Session 5 (Feb 2026): 70+ Google Search Console impressions, upward trend, all celebrity-related
- Google crawler initially gave up after crawling only 2 pages; sitemap trimmed and content quality improved to encourage re-indexing
- No meaningful revenue yet
## Analytics & Instrumentation
- Google Search Console / Webmaster Tools active
- Some tracking on buy/purchase button click flow
- Need to instrument: page landings, journey entry points, buy clicks, email signups, session tracking for personalisation
- Weekly analytics review cadence recommended
- Mixpanel or Google Analytics / Data Studio discussed as options
## Competitive Landscape
- No direct AI-powered perfume discovery competitor identified
- Closest: celebrity magazine curated perfume editorial sites (Vogue Beauty, similar)
- Competitors are image-heavy, magazine-style, with longer editorial articles
- Debenhams has ~100 celebrity perfumes; Awin network has broader catalogues
- Key differentiator: only platform aggregating all perfume house data in one place with better UX; data depth is significant first-mover advantage (cloneable but hard to replicate quickly)
- [perfumista.co.uk](http://perfumista.co.uk/) is the incumbent in the "Perfumista" name space (~429 Trustpilot reviews, ~$5M revenue)
## Notion Advisory Structure
- Sessions DB: Lavender Thorne Sessions (entries named Session N: title (YYYY-MM-DD))
- Actions DB: Lavender Thorne Actions (linked to Sessions, GTD statuses)
- Both DBs embedded on the Lavender Thorne HBN advisory page
- Legacy session pages migrated as DB entries (21 Mar 2026)
- Structure mirrors DataBoots advisory setup
## Session Log
- **Session 7 (27 Apr 2026):** Working on site revisions Matt was planning. Naming still unresolved (Paul and Matt not yet aligned). Paul stepping back — has some paid work in; Matt stepping up. Communication and agreement between the two remains a challenge; things tend not to move without Kiwifruit facilitating. Advised pivot framing: away from twenty-something fangirl persona; toward tech bros and "last-minute Larry" (male, happy to buy perfume online, wants it tomorrow). Core strategic issues discussed: (1) people may prefer to smell perfume before buying — samples as "sale before the sale"; Kiwifruit to raise £5–10 sample entry point next session as list-builder + user research mechanism. (2) Language for male audience: cologne not perfume; brand must flex for both without defaulting to one. Paul generated a full animated AI mascot series. 8,000 impressions/month via Google Search but zero clickthrough — need a compelling hook. **Uncle Sniff concept surfaced:** Dog in a lab coat (a Labrador, doing lab tests and teardowns with the paw). Strapline: "Smell better for less using science." Mascot-led viral content that cuts through without an influencer budget. Possible comparison site angle with affiliate links to purchase. Key enduring advice: "Be something to someone rather than nothing to everyone." Shoreham Tech note: Paul Collingwood and Matt both flagged as likely pre-launch drinks attendees for Shoreham Tech.
- **Session 7 follow-up (28–29 Apr):** Uncle Sniff idea elaborated further. If brand moves to Uncle Sniff, mascot is a Labrador in a lab coat with lab tests. Scratch-and-sniff sample sheets as a product: "Here you are wanting CK1 but here are three cheaper ones that smell really good. Here’s your scratch-and-sniff sheet." Ordering of samples and testers identified as a key mechanic to explore for next session.
- **Session 1 (29 Jan 2026):** Diagnostic session; Perfumista status, acquisition/activation/retention framing, SEO + blog + mailing list recommended, "Last Minute Larry" persona coined, "sniping" launches strategy, brand name concerns raised
- **Session 2 (12 Feb 2026):** Rebrand to Lavender Thorn; blog + mailing list shipped; ~1000 perfume pages generated; Google Trends + bestseller mapping for SEO; analytics instrumentation recommended; click-first UX over chat-first
- **Session 3 (26 Feb 2026):** Major redesign demo; ICP pivot to young women (24F); celebrity-driven impressions validated; perfume houses + launches + budget browsing shipped; mobile-first; newsletter strategy; competitor analysis approach; Mackmyra whiskey inspiration; focus on perfume before adjacent markets
- **Session 4 (25 Mar 2026):** Data infrastructure shift to direct house scraping; price tracker + sale detection + automated social content; MCP server PoC; chemist studio demo; brand crisis (domain + perception); rebrand to AI-forward name recommended; influencer/brand face strategy; revenue model diversification discussed
---
Last state file sync: 4 April 2026
