# Sean from IT — Current State (3 May 2026)

<!-- Auto-synced from Notion. Last sync: 2026-05-06 05:28 UTC -->

<!-- ANCHOR -->
> **Shoreham-by-Sea, West Sussex, BN43** — Victorian mid-terrace, 3 floors
> Last updated: 1 April 2026
---
## 🟢 Current Status — 3 May 2026
- [**Sender.net**](http://sender.net/)** mailing list connected to **[**italianwithhannah.com**](http://italianwithhannah.com/)** (3 May 2026):** DNS records added in Hostinger. DKIM CNAME added with correct name `sender._domainkey` (not `@`). DMARC TXT added as `_dmarc`. Existing SPF record (`v=spf1 include:spf.titan.email ~all`) edited to merge [Sender.net](http://sender.net/) include: `v=spf1 include:spf.titan.email include:sendersrv.com ~all`. Propagation confirmed within 15–30 mins. See `## 📧 Email & Mailing List — italianwithhannah.com` section below for full how-to.
## 🟢 Current Status — 30 April 2026
- **Second Brain v3 planning session (30 Apr 2026):** Explored migration options away from Notion + public GitHub. Five options evaluated against 7 use cases: (1) Obsidian + Copidian Copilot + Obsidian Sync, (2) Obsidian + Claude Code/Cowork, (3) Notion Business + AI Agents, (4) Obsidian + Smart Connections, (5) Hybrid Notion journal + Obsidian state files. **Decision: stay on v2 for now, revisit in 1–2 months.** Obsidian is philosophically the right direction (local-first, markdown, model-agnostic, private) but mobile plugin startup times (10–15 seconds reported) make it a downgrade from current mobile workflow at 80% phone usage.
- **v3 trigger events to watch monthly:**
  - GitHub MCP connector appearing in Claude's registry — unlocks private repo reads, eliminates both Notion and public GitHub dependency
  - Obsidian mobile performance improvements — if plugin startup drops to 3–4 seconds, Obsidian becomes viable as primary
  - Obsidian Copilot project feature maturing — needs structured 20-project routing comparable to Claude Projects
- **Notion frustrations documented:** MCP server flaky, mobile app slow, databases no longer used meaningfully (only for templates), general bugginess. Kiwifruit would like to move away from Notion when a viable replacement exists.
- **Notion AI Meeting Notes plugin:** Decision to drop. Will switch Catarina therapy session recording to BlackHole + QuickTime + MacWhisper on personal MacBook Air M1. Saves subscription cost; stack already owned.
- **Mac Mini server idea:** Parked. Overkill for this problem — likely solved by a registry connector appearing. Nassy covers most home server needs already.
- **Key insight from session:** The constraint shaping the v3 decision is mobile AI chat performance. At 80% mobile usage, Notion + Claude is hard to beat today. The frustration is Notion as the storage layer, not Claude as the conversation layer. Claude Projects + MCP is one of the better chat-with-structured-data implementations available. Kiwifruit's Rightbrain experience confirms the model layer and app layer are separating — staying model-flexible is important but not urgent.
- **Hannah confirmed:** Does not use Notion and will never use it. Not a factor in platform decisions.
## 🟢 Current Status — 26 April 2026
- **Notion → GitHub sync automation live (26 Apr 2026):** GitHub Action (`notion-sync.yml`) deployed to `sb-notes/second-brain` repo. Runs nightly at 02:00 UTC (03:00 BST). Reads all 18 Second Brain v2 live state files from Notion API, converts to markdown, commits to GitHub. Skips commit if no changes. Can also be triggered manually from GitHub Actions tab. First manual run: success, 2m 8s, all 18 files synced.
- **GitHub Action secrets configured:**
  - `NOTION_TOKEN` — Notion "GitHub Sync" internal integration token, stored as org-level secret in `sb-notes` org, scoped to public repositories. Integration has access to "Second brain state files" parent page (covers all 19 projects).
  - `GH_PAT` — Fine-grained personal access token (resource owner: `sb-notes` org, repo: `sb-notes/second-brain`, permission: Contents read/write). Stored as repo-level secret in `second-brain`. Expiry: 1 year.
- **Notion integration in use:** "GitHub Sync" integration (internal connection in Kiwifruit's Notion workspace). Token retrieved and stored in GitHub this session. Access granted to "Second brain state files" teamspace page and all children.
- **Nightly sync architecture note:** The nightly sync keeps GitHub (Claude's read source) current with Notion (Claude's write destination). Without it, Claude reads stale GitHub files if Notion was updated but the repo wasn't manually pushed. The Action eliminates all manual GitHub pushes going forward. Workflow file: `.github/workflows/notion-sync.yml` in `sb-notes/second-brain`.
- **Second Brain v1 and v2 architecture documented in Notion (26 Apr 2026):** Two new pages created under "Second brain state files": (1) Second Brain v1 — Architecture & Deprecation — what v1 was, the five failure modes, deprecation decision; (2) Second Brain v2 — Architecture & Design — full design spec, session flow, data flow, trigger words, codename system, bug fixes, the nightly sync automation, all 19 projects listed.
## 🟢 Current Status — 14 April 2026
- **Wispr Flow — Android power settings note (14 Apr):** Wispr Flow icon periodically disappears from Gboard toolbar after Android power management kills background processes. Mental note from Kiwifruit: always toggle Wispr Flow off and back on again before starting a journal transcription session on Android. Battery Unrestricted fix was applied (4 Apr 2026) but may need re-checking after OS updates.
## 🟢 Current Status — 13 April 2026
- **Notion plan downgrade (13 Apr 2026):** Kiwifruit downgraded from Business to Plus plan. Rationale: Notion AI no longer used — replaced by Wispr Flow for voice input. Claude MCP integration unaffected by plan change (API-based, not tied to Notion AI). Basic integrations (Slack, Google Drive, Gmail) retained on Plus. Features lost: Notion Agent, Custom Agents, AI Meeting Notes, SAML SSO, Enterprise search, Premium integrations.
## 🟢 Current Status — 1 April 2026
- **Desk relocation (Position D):** Planned for weekend of 29–30 March 2026 — confirm whether completed
- **Shure MV7+:** Purchased via Vinted 1 Apr 2026, £149 delivered, brand new sealed. Replaces MAONO AU-PM422. Ready for use.
- **Podcast (Rightbrain Adventures in AI):** Parked until after probation review 2 April 2026
- **Technics EAH-AZ100:** Set up and confirmed as keeper. Left earbud remapped to ANC cycling. Large tips being trialled.
- **Penguin 3-in-1 mouse:** Active on Bluetooth to MacBook M5. Dongle stored in mouse base. Old Penguin listed on Vinted.
- **Hannah's Pixel 8 migration:** Complete. Giffgaff SIM ported. Post-migration caller ID / data issues escalated to Giffgaff support.
- **Carciofi's Pixel 8 — spam call filtering (2 Apr 2026):** giffgaff (O2) hides the "Filter spam calls" toggle on Pixel 8 (carrier restriction). Workaround implemented: Caller ID & Spam enabled, Call Screen (on-device AI) turned on, Should I Answer? app installed. Unknown number blocking not enabled (too aggressive). This combo silences suspected spam without vibrating.
- **Kiwifruit's Pixel 8 — Wispr Flow / Gboard integration (4 Apr 2026):** Wispr Flow icon was periodically disappearing from Gboard toolbar after restart. Root cause: Android adaptive battery / background permission stripping. Fix applied: Battery set to Unrestricted (Settings → Apps → Wispr Flow → Battery), background usage enabled, "Manage app if unused" confirmed disabled (greyed out — not applicable). Floating black overlay bubble dismissed; Gboard toolbar icon confirmed as preferred trigger. Volume button shortcut (hold both volume keys) configured as fallback if toolbar icon disappears. Accessibility icon turned off to reduce clutter.
- **Nassy (QNAP):** In loft, connected via AV1000 powerline adapters, IP 192.168.68.108. Plex running. Tailscale active (100.86.115.108). QuMagie live for Hannah. Confirm Hannah’s /Media permissions reverted to Read Only.
- **QFile photo backup:** Both Pixel 8s pointing to /Media/Photos with date-based subfolders.
- **Octopus Energy renewal:** Action required before 3 April 2026 — click “Choose Octopus 12M Fixed” in renewal email.
- **Glasses:** Cubitts Ampton Bold tortoiseshell (Vinted, £80, new without tags) — pending frame size confirmation.
---
## Journal sync — 31 March 2026
- Plex not working on the Shield TV — to be fixed; Plex works on other devices. Low priority but noted.
- Music transition plan: complete switch from YouTube Music to Plex; save Miss Rachel and Miss Apple video/audio catalogues to Nessie (NAS); then cancel YouTube Music subscription (saving ~£260/year).
- Audio recording setup task: set up QuickTime audio recording on personal MacBook Air M1 using BlackHole as virtual audio device; test and verify the workflow; transcribe via MacWhisper. Plan to purchase MacWhisper licence.
- Claude/Notion second brain system noted as functioning well — Wispr Flow → Notion → Claude → state files loop fully operational and daily journaling established.
---
Last updated: February 2026 — maintained by Oliver & Claude
This is the single source of truth for all technology, equipment, services and energy decisions in the house. Update this page whenever something changes, so future Claude threads can be pointed here instead of relying on project file storage.
---
## 👨‍👩‍👧 Household
- **Occupants:** Oliver + wife + children (moved in Sep 2025)
- **Property:** Victorian terraced house, 3 floors, Shoreham-by-Sea, West Sussex
- **Flat (let out separately):** Has Solfex thermostat + Vaillant boiler in loft — managed separately
---
## ⚡ Energy — Octopus Energy (Account: A-CEC10C86)
### Current Tariff (until 3 April 2026)
- **Tariff:** Loyal Octopus 12M Fixed (April 2025 v1)
- **Electricity unit rate:** 23.75p/kWh | Standing charge: 44.44p/day
- **Gas unit rate:** 5.61p/kWh | Standing charge: 29.59p/day
- **Meters:** Electricity smart meter 23J0437513 | Gas smart meter E6S11867532462
### Decision at Renewal (April 2026)
- **Recommended:** Octopus 12M Fixed
- Electricity: 25.83p/kWh | Gas: 5.57p/kWh | Est. monthly: £145.88
- Saves ~£100/year vs Flexible Octopus based on actual usage
- No exit fee on either option
### April 2026 Renewal — Decision Made (28 Feb 2026)
- **Action required before 3 April 2026:** Click "Choose Octopus 12M Fixed" in renewal email
- If no action taken, Octopus auto-rolls to Flexible Octopus (more expensive)
- Octopus's consumption estimates (2,972 kWh elec / 12,365 kWh gas) are **overstated** — actual 12-month usage is ~3,000 kWh elec / ~9,600 kWh gas
- Real estimated annual cost on Fixed: ~£1,480 vs ~£1,580 on Flexible
### Actual Usage Analysis (Jan 2025–Feb 2026)
Key milestones and their impact on consumption:
| Period | Context | Avg Electricity/mo | Avg Gas/mo |
| --- | --- | --- | --- |
| Jan–Feb 2025 | 2 adult lodgers in house | 343 kWh | 1,213 kWh |
| Apr–Aug 2025 | Lodgers gone, summer, 2 adults | 154 kWh | 170 kWh |
| Sep–Nov 2025 | Children moved in, old Google Nest heating | 275 kWh | 580 kWh |
| Dec 2025–Feb 2026 | Drayton Wiser TRVs + new front door | 267 kWh | 1,592 kWh |
**Key insight:** Gas use in Dec 25–Feb 26 is higher in absolute terms but this reflects the house being *properly heated room-by-room* for the first time — previously under-heated to save money. Electricity is 19% lower year-on-year (Jan 25 → Jan 26: 333 → 271 kWh) despite children now living there, confirming the Wiser's smart scheduling is working. The new front door (Jan 2026, completing full double glazing) will compound savings from next winter onwards. Octopus's annual estimate of 12,365 kWh gas is significantly overstated — actual 12-month gas usage is ~9,600–10,500 kWh.
### Milestone Timeline
- **Mar 2025:** 2 adult lodgers moved out
- **Sep 2025:** Children moved in
- **Dec 2025:** Google Nest replaced with Drayton Wiser + TRVs on all radiators → house noticeably warmer
- **Jan 2026:** New front door fitted — entire house now double glazed
---
## 📧 Email & Mailing List — [italianwithhannah.com](http://italianwithhannah.com/)
### Setup summary
- **Domain registrar / DNS:** Hostinger ([hpanel.hostinger.com](http://hpanel.hostinger.com/) → Domains → DNS / Nameservers)
- **Email provider:** Titan Email (via Hostinger) — MX records point to [mx1.titan.email](http://mx1.titan.email/) / [mx2.titan.email](http://mx2.titan.email/)
- **Mailing list platform:** [Sender.net](http://sender.net/)
### How to connect [Sender.net](http://sender.net/) to a Hostinger domain
In [Sender.net](http://sender.net/): Settings → Sender Domains → Authenticate → your domain → shows DKIM, SPF, DMARC records to add.
**DKIM (CNAME record)**
- Type: CNAME
- Name: `sender._domainkey` ⚠️ Hostinger pre-fills `@` here — change it
- Target: `dkim.sendersrv.com`
- TTL: 14400
**DMARC (TXT record)**
- Type: TXT
- Name: `_dmarc`
- Content: `v=DMARC1; p=none;`
- TTL: 14400
**SPF (TXT record — edit existing, do not add new)**
- Hostinger already has a TXT `@` record from Titan: `v=spf1 include:spf.titan.email ~all`
- Click **Edit** on that record and merge — only one SPF per domain allowed
- Updated value: `v=spf1 include:spf.titan.email include:sendersrv.com ~all`
**Verify:** Return to [Sender.net](http://sender.net/) → click **Check SPF, DKIM and DMARC records**. Propagation typically 15–30 mins on Hostinger.
---
## 🌐 Network & Connectivity
- **Broadband: BT (fibre)** — main internet connection
- **Router/Mesh: TP-Link Deco M9 Plus** — mesh WiFi across 3 floors
- **NAS: QNAP TS-251D “Nassy”** — Intel Celeron J4005, 2-bay, 8GB DDR4 RAM max. Connected to Deco M9 node via Ethernet. IP: 192.168.68.108
- **NAS Drive 1 (Primary): Seagate IronWolf 8TB** — main storage drive
- **NAS Drive 2 (Backup): WD Red Plus 8TB** (secondhand) — daily backup of IronWolf. WD is quieter — plan to swap to primary when convenient
- **VPN: Surfshark** — used across all devices. Split tunnelling managed carefully around Plex/Tailscale
- **Remote Access: Tailscale** — for remote Plex access, avoids port forwarding
- **Mobile provider (Oliver): giffgaff (O2 network)** — switched from EE, better signal in Shoreham-by-Sea
---
## 📺 Media / Entertainment
- **TV: Panasonic TX-40GX800B** (40", 4K, 2019) — mounted on long-reach arm on chimney breast
- **Streaming/Plex server: NVIDIA Shield Pro** — runs Plex Media Server, connected to NAS via network, Plex library: Plexi
- **Plex subscription: Plex Pass (Lifetime)** — enables hardware transcoding, remote streaming, Plexamp
- **Soundbar: Ultimea D80** — connected via HDMI ARC, front surrounds wired to soundbar
- **Bluetooth speakers: EarFun UBOOM** (x2, paired together) — secondary audio
---
### 🎧 Earbuds & Headphones (Oliver)
- **Earbuds (primary): Technics EAH-AZ100E** — purchased via Vinted Mar 2026, £164. Fully set up and confirmed as keeper after side-by-side testing with Bose QC Ultra Earbuds (Mar 2026). Paired via simultaneous long-press hold on both earbuds (no case button). Left earbud long press remapped to ANC cycling via Technics Audio Connect app. Sound: well-balanced, neutral, slightly warm. Call quality: consistent, picks up full voice, not muffled. Outdoor ANC: excellent. Large ear tip size being trialled for optimal fit and seal.
- **Earbuds (backup): EarFun Air Pro 4** — retained as backup.
- **Bose QC Ultra Earbuds 2nd Gen — tested and returning (Mar 2026):** Arrived as mislabelled Vinted swap. Required factory reset (30-second case button hold) to clear previous pairing. Sound: very bass-heavy, unusable at 25% volume; dynamic soundstage feel. Call quality: muffled and quiet. ANC muffles outdoors vs Technics. Slightly more comfortable out of the box. Returning via Vinted buyer protection — Technics clearly preferred for sound balance and call quality.
- **Over-ear headphones: Sony WH-1000XM4** (or equivalent) — existing NC headphones. Note: bass-heavy sound signature.
## 💻 Computers & Phones
### Pixel 8 Purchase & Migration (28 Feb 2026)
**Purchased:** Google Pixel 8 128GB Obsidian from Back Market (refurbished) - £194
- **Condition:** "Good" grade - flawless screen guaranteed, 80%+ battery health
- **Protection:** Spigen Liquid Air case £16.99 + tempered glass screen protector ~£8
- **Total cost:** ~£219 for fully protected setup
- **Previous phone:** Pixel 4a (purchased refurb June 2023 from eBay, 24.06.23)
- **Pixel 4a history:** Originally from 2020 release, ~5.5 years old hardware at retirement
- **Wife also upgrading:** Pixel 3a → Pixel 8 128GB (same Back Market deal)
**Migration checklist prepared:**
1. Recorder app files backed up to Google Drive
1. Downloads folder cleaned (old 101 Ways workspace files removed)
1. Photos verified backed up to both Google Photos + Nassy via QFile
1. App list documented for reinstallation
1. Crypto wallet recovery phrases verified in 1Password (Tangem, Ledger Live, MetaMask)
1. Google Authenticator export prepared
1. Signal backup enabled
**On arrival checks:**
- Battery health target: 85%+ (minimum acceptable: 80%)
- IMEI check via [checkmend.com](http://checkmend.com/) (£2)
- Physical inspection: screen, cameras, buttons, charging port
- Data transfer via USB-C cable (30-60 mins estimated)
**Post-migration:**
- Disable Google Photos auto-backup (moving fully to Nassy + QuMagie)
- QFile auto-upload configured for overnight NAS backup
- Keep Pixel 4a as backup during 30-day Back Market return window
- Factory reset Pixel 4a after 7+ days of confirmed Pixel 8 stability
**Key retailer comparison (Feb 2026):**
- Back Market: £194-221 (Good to Great condition)
- eBay tc-gadgets: £219.99 (confusing returns policy)
- Reboxed: £203-221
- CeX: £380-420 (Grade A/B, but 2-year warranty)
- 256GB premium: £286+ (not justified for usage with nightly NAS backups)
**Decision rationale:** Back Market £194 beat eBay by £26, with clearer returns (30 days) and same 12-month warranty. 128GB sufficient given QFile overnight backup workflow to Nassy.
- **Laptop (Oliver, personal): MacBook Air M1** — personal/home use only. Brave browser, Surfshark VPN
- **Laptop (Oliver, work): MacBook Air M5 (13-inch)** — Rightbrain work machine, work-only, no personal crossover
- **Laptop (Hannah): MacBook Air M1**
- **Phone (Oliver): Google Pixel 8** (128GB Obsidian, Back Market refurb, Feb 2026) — monochrome display mode, Brave browser, Surfshark VPN, giffgaff eSIM
- **Phone (Hannah): Google Pixel 3a** — giffgaff (O2), physical SIM only (no eSIM on 3a), migrated from EE Mar 2026. Pixel 8 upgrade via Back Market planned later in 2026
- **Tablet: Acer Iconia Tab M10 (A22001) 128GB** — video calls and toddlers
- **Recording device: Roland R-05** — choir concerts. External mic upgrade under consideration
- **Webcam: Elgato Facecam MK2** — 2K, used on MacBook Air M1
- **Standing desk: Flexispot EC-1** — loft office (moving to Position D Mar 2026)
---
## 📸 Photo Management
- **Platform:** QuMagie (QNAP) — AI photo management on Nassy
- **Workflow:** Google Photos sync to NAS nightly via QFile app (Android). Family photos pooled and shared via NAS
- **Goal:** Replace Google Photos paid storage with self-hosted NAS solution. Cut to Google free tier
- **Mobile upload app:** QFile (Google Play) — QMagie mobile upload being discontinued
---
## 🎵 Music
- **Server:** Plex / Plexamp (via Plex Pass lifetime)
- **Library location:** `/NASSY/Media/Music/` — includes `/YTM Catalog/`, `/Playlists/`, `/Uploaded Files/`
- **Source:** YouTube Music library downloaded via 4K Video Downloader, tagged in MusicBrainz Picard
- **Playlists:** Managed via Soundiiz (paid licence)
---
## 🔥 Heating & Home Systems
### 🔁 Drayton Wiser Room Thermostat — Factory Reset & Re-pair Procedure (confirmed 10 Apr 2026)
Devices paired to old Kit 1 hub and not deleted before hub replacement. This is the confirmed working method.
1. In the Wiser app, **start pairing mode first**: **+** → **Add Device** → **Room Thermostat** — get it actively searching before touching the thermostat
1. Remove **both** batteries, wait **20 seconds** — removing only one battery does not work
1. Reinsert both batteries with + and − fingers ready
1. Immediately press and hold **both + and − buttons simultaneously**
1. Keep holding for up to 20 seconds until the screen shows a **green background with a WiFi symbol** = pairing mode
1. The app should find the device within 30 seconds of the WiFi symbol appearing
> The app must be in searching mode **before** the thermostat boots — not after. The pairing window is short.
> If the WiFi symbol appears but joining fails, move physically next to the hub and retry from step 1.
---
### 🔁 Drayton Wiser TRV — Factory Reset & Re-pair Procedure (confirmed 10 Apr 2026)
This is the correct reset sequence for the Wiser Radiator Thermostat as confirmed through hands-on testing. Ignore the official documentation — the twist-and-hold method does not work reliably on these units.
1. Remove batteries, wait 10 seconds, reinsert
1. Let the TRV boot until you see **3 flashing LEDs** (red left, red centre, blue right)
1. Twist cap **right (+)** — blue light for 3 seconds — let it calibrate (valve moves)
1. Twist cap **right (+) and hold for ~15 seconds** until the centre LED flashes red **8 times** — then you see red + blue flashing with orange in the centre
1. Twist cap **left (−) for 3 seconds** — centre LED turns **solid green** = pairing mode
1. In the Wiser app: **+** → **Add Device** → **Radiator Thermostat** — device is found and paired
> Do one TRV at a time. Pair each before resetting the next.
- **Heating controller: Drayton Wiser Kit 3 (WT734R)** — upgraded from Kit 1 on 10 Apr 2026 by electrician Jamie (nephew of Paul, PJ Plumbing). Kit 3 provides 2 heating channels + 1 hot water channel.
- **Wiser Kit 3 channel wiring (as installed, 10 Apr 2026):**
  - Channel 1: Heating → radiator circuit (TRVs + room thermostats)
  - Channel 2: Hot Water → UFH pump circuit (physically wired here — confirmed by floorboard creak test)
  - Channel 3: Heating → currently assigned to kitchen room thermostat for UFH control; physical wiring to UFH pumps still on Channel 2 terminal
- **UFH architecture (main house):** Two 240V pump zones (kitchen slab, diner raised floor) both operate simultaneously as one logical zone. Previously controlled by Solfex (decommissioned, wires capped). Now on Wiser hot water channel.
- **Outstanding wiring issue (10 Apr 2026):** UFH pumps are wired to hot water terminal (Channel 2) rather than Channel 3. Hot water channel is binary on/off with no thermostat association — kitchen room thermostat on Channel 3 cannot call the UFH pumps directly. Workaround: hot water schedule covers UFH timing. Proper fix: Jamie to move UFH pump cable from hot water terminal to Channel 3 terminal + confirm boiler demand wire covers both channels independently. A motorised zone valve on the UFH circuit may also be needed for independent heat calling.
- **All 3 channel outputs confirmed identical:** 2(1)A 230V relay switches — no electrical difference between heating and hot water terminals per Drayton spec sheet.
- **Boiler (main house): Vaillant ecoTEC Plus 835 H combi** — water pressure confirmed 1.7 bar (healthy). Spanner icon showing = annual service reminder (not a fault). Chimney sweep mode accidentally triggered and cancelled 10 Apr 2026 — no settings affected.
- **Wiser devices paired to Kit 3 hub (10 Apr 2026):** Lounge room thermostat (Channel 1), kitchen room thermostat (Channel 3), lounge TRV, bedroom TRV, kids bedroom TRV, landing smart plug/repeater. Remaining TRVs to pair: loft, playroom.
- **TRV reset note:** See Wiser TRV and Room Thermostat reset procedures above — official Drayton docs unreliable; hands-on confirmed methods documented in this file.
- **Boiler (main house) — combi**
- **Underfloor heating (flat): Solfex thermostat + Vaillant ecoTEC plus 835 H combi A** — let-out flat, managed separately. F.22 (low water pressure) + F.53 (mass flow sensor) faults appeared Mar 2026, resolved by re-pressurising to 1.3 bar and resetting. Target cold pressure: 1.2–1.5 bar
- **Dishwasher: Bosch SMV69M01GB** — E09 error = heat pump/heater assembly fault
- **Baby monitor: Boifun** (Baby 3SM/6T-style) — uses BoifunCam/CloudEdge app
- **Watch (Oliver): Withings Activité Steel HR** — ScanWatch upgrade under consideration
- **Watch (previous): Garmin** (model TBC) — replaced by Withings, historical data exported from Garmin Connect
---
## 🧒 Children's Devices & Toys
### Tonies Collection (Apr 2026)
- **Toniebox:** Already owned. Children are Bunny and Fox, age 2.
- **Purchases (Apr 2026, all secondhand):**
  - Sleepy Friends Nature Sounds (green cat) — £8, Vinted, very good condition
  - Sleepy Friends Bedtime Lullabies (red cat) — £8, Vinted, very good condition. 20 tracks, ~50 mins, classic UK nursery rhymes and lullabies
  - Beatrix Potter Peter Rabbit Collection — £9, Vinted, sealed. Multi-story audiobook.
  - Tonies Sleepy Sheep Night Light — £19.50 delivered, eBay, used once. RRP £34.99. 4 dimmable brightness levels, 90 mins nature sounds + instrumental, works on/off Toniebox, 30-min sleep timer, USB-C rechargeable, up to 240hrs battery at lowest brightness. Replacing breathing bear and floor night light.
- **Approach:** Secondhand-first via Vinted/eBay. UK voices preferred. Avoid American-voiced content.
- **Wishlist:** Nursery Rhymes Tonie (target £6–8 secondhand)
### LCD Writing Tablets (Mar 2026)
- Purchased: Genialba 8.5 inch LCD Writing Tablet, 2-pack (Pink & Purple), £7.99 from Amazon UK
- Uses replaceable coin/button battery (not USB rechargeable) — deliberate choice after community research
- Purchased for the toddlers (age ~2); 8.5" confirmed as best size for under-3s per community consensus
- USB rechargeable alternatives (POPERFUN 13") were reviewed but rejected due to QC concerns in reviews
---
## 🚗 Car
- **Vehicle: Toyota Auris Estate**
- **Charging: 12V / 120W cigarette lighter** — USB-C fast charger added for Android phones
---
## 🎙️ Microphone
- **Microphone: Shure MV7+** — purchased via Vinted, 1 Apr 2026, £149 delivered
- Condition: Brand new, factory sealed, never opened (unwanted gift)
- Full contents: USB-C cable, XLR cable, desktop stand, original box
- Use case: daily meetings on MacBook M5 + fortnightly Rightbrain Adventures in AI podcast recording via OBS
- Connection: USB-C direct to MacBook M5
- Previous mic: MAONO AU-PM422 condenser (approx 5 years old) — retired
- Purchase journey: researched MV7i (John Pye auction, missed at £91 hammer/~£130 all-in), MV7+ (multiple eBay listings), settled on Vinted sealed unit as best value
## 🖱️ Peripherals
### USB-C Right-Angle Adapter (Mar 2026)
- Purchased: VCOM 240W 80Gbps USB-C right-angle adapter, 1 pair, £8.19 from Amazon UK
- Use case: MacBook Air M5 (Rightbrain work laptop) → LG 4K monitor + USB hub (mouse, headset)
- Chosen variant: 240W 80Gbps (highest spec) for bandwidth headroom with 4K display passthrough
- Brand note: VCOM mid-tier, solid aluminium build, adequate for passive adapter at this price
### Ergonomic Mouse (Mar 2026)
- Posturite Penguin Large wireless USB dongle misplaced during family visit
- Decision: purchase new **Penguin 3-in-1 Large** (wired + wireless + Bluetooth) from Posturite — ~£81–102
- Bluetooth model eliminates dongle dependency entirely
- Hand size confirmed: 20cm wrist-to-fingertip, 10cm wide palm — XL / top of Large size range
- Use case: left hand primary, partial ambidextrous switching — Penguin is the only true vertical ambidextrous mouse at this size
- MX Vertical considered but ruled out: right-hand only design, and large-hand users hit size limits
- Purchased via Rightbrain work budget
- **Old Penguin wireless-only mouse:** Listed for sale on Vinted (Mar 2026) — missing dongle, sold for parts or for buyers who have a spare dongle. Serial: LGWDWLBT2411000973, QC 2024.
- **New Penguin 3-in-1 setup decision:** Bluetooth on MacBook M5, not dongle via Ugreen USB hub. Rationale: avoids repeating dongle-loss issue; macOS BT 5.3 handles Magic Keyboard + Technics AZ100E + Penguin comfortably. Dongle stored in mouse base slot as fallback only.
- Old Penguin wireless (large, dongle-only model) listed for sale on Vinted — dongle lost, selling as parts/spares. Serial: LGWDWLBT2411009 73. QC sticker dated 2024. Collection Shoreham BN43 or post.
- New Penguin 3-in-1 received and set up Mar 2026. **Bluetooth chosen as primary connection** to MacBook Air M5 — eliminates dongle-loss risk. USB dongle stored in mouse base slot as fallback. Ugreen USB-C hub on M5 available as dongle host if BT tracking proves unreliable.
---
## 📱 Additional Devices (from legacy custom instructions)
- **Tablet:** Acer Iconia Tab M10 (A22001) 128GB — used for video calls and toddlers
- **Webcam:** Elgato Facecam MK2 2K — used on MacBook Air M1
- **Previous phone (retired):** Pixel 4a — factory reset after Pixel 8 migration
---
## 🔑 Key Principles (for Claude threads)
- **Minimum viable spend** — refurbished/secondhand preferred over new where quality holds
- **Set and forget reliability** — prefer solutions that need no ongoing maintenance once configured
- **Privacy first** — Surfshark VPN + Brave browser on all devices as standard
- **Self-hosted over cloud** — NAS as private cloud for photos, music, media
- **UK sources preferred** — giffgaff, Octopus Energy, Amazon UK, [signalchecker.co.uk](http://signalchecker.co.uk/)
- **Carrier-unlocked phones only** — Verizon/locked models incompatible with UK networks
- Firmware updates on QNAP commonly reset Plex settings — document and check after every update
---
## 📝 How to Use This Page
1. **When something changes** — update the relevant table or section directly in Notion
1. **Starting a new Claude thread** — paste the URL of this page and say "refer to my current state page"
---
Last journal sync: not yet run
## 🏠 House Layout — 53 Victoria Road (for office/studio planning)
**Property type:** Victorian mid-terrace, 3 storeys, approx 1,297 sq ft
**Orientation:** Front faces south. Rear faces north.
### Ground Floor
- Kitchen (rear/north), Dining Room/Bedroom aka Playroom (middle, west-facing window only), Living Room (front/south bay window)
### First Floor
- Two bedrooms, bathroom, utility room
### Second Floor (Loft Conversion)
- **Bedroom** — master bedroom with blue feature wall (east side), Velux in north-facing roof slope, sloped ceilings, wooden floorboards
- **Alcove / Landing** (11'1" x 5'4" / 3.4m x 1.6m) — Ollie's current home office, Position A. Flexispot EC-1 standing desk faces west toward window with Downs view. Width ~93 cm, too narrow for green screen with Elgato FaceCam MK2 wide-angle lens. Floor slopes slightly.
- **Shower Room** off the landing
### Office/Studio Layout — Decision (26 Mar 2026)
- **Decision: Position D chosen.** Desk moving to north wall of loft bedroom, facing south. Planned for weekend of 29–30 Mar 2026.
- Velux window over left shoulder provides consistent indirect natural light; no glare behind screen. Blackout blind integrated into Velux.
- Bed moving to south side of room, headboard against south wall, extending north into room. South wall section: 165 cm; bed length: 203 cm — must remain perpendicular (cannot fit sideways). North wall section: 171.5 cm.
- Dresser relocated into alcove (former Position A) as secondary standing surface for wireless headset calls with Downs view.
- Green screen: 2m+ flat wall behind desk position suits Elgato FaceCam MK2.
- **Position A retired** — 93 cm too narrow for green screen, west-facing glare/eye strain from constant brightness management.
- **Position C rejected** — noise, 2-storey carry, unstable desk.
- Flexispot EC-1 moves from alcove to Position D; flatter floor should improve stability.
## 💻 Work Laptop — [Rightbrain.ai](http://rightbrain.ai/) (6 Mar 2026)
- Ollie starting new role at [Rightbrain.ai](http://rightbrain.ai/) as Product Lead → CPO
- Offered choice of 13-inch or 15-inch MacBook Air as work laptop
- **Decision: 13-inch MacBook Air M5** chosen for portability
- Key rationale: regular travel to Newcastle by train + client visits; 13-inch better fit for train tables and meetings; community consensus from CPO/manager community confirms 13-inch preferred by travelling execs over 15-inch
- Already familiar with 13-inch form factor from personal MacBook Air M1
- **Machine separation policy:** M5 is work-only; M1 is personal/home-only. No crossover.
## 🔗 Notion MCP Cross-Workspace Architecture (28 Mar 2026)
- **Confirmed:** Notion MCP auth is scoped per-Claude-account, per-workspace. Personal Claude → personal Notion; work Claude → work Notion. No cross-workspace access.
- Tested 28 Mar 2026: Claude can only see the "Ollie" teamspace. Rightbrain workspace is not accessible from personal Claude.
- **Morning journal → Rightbrain workflow (Option B adopted):**
  - Ollie dictates morning journal into personal Notion workspace as usual
  - Personal Claude routes personal items to personal state files
  - Claude then outputs a formatted "📋 RIGHTBRAIN CLIPBOARD" text block at the end of the response, containing any work-relevant updates extracted from the journal
  - Ollie copy-pastes the clipboard block into a Rightbrain Claude conversation, which writes to Rightbrain state files in the Rightbrain Notion workspace
  - Custom instruction for clipboard extraction added to Cheryl project custom instructions (28 Mar 2026)
  - Overhead: ~30 seconds per morning session when work content is present
- **To enable direct cross-workspace access in future:** Would require reconnecting Notion MCP integration and granting access to both workspaces during OAuth flow — but this depends on Rightbrain Notion admin permitting external integrations
## 🤖 Claude Dispatch — Decision (25 Mar 2026)
- **Decision: Not adopting Dispatch at this time**
- Home setup: all files cloud-based and API-accessible (Notion, Google Drive, Gmail) — no local compute needed; existing Android → Claude mobile workflow already covers async task dispatch well enough
- Work setup: M5 is work-only machine; separation of concerns means no personal Claude Cowork session running on it
- **Future trigger for revisiting:** If Ollie begins running local LLMs or processing heavy client data dumps locally on the M5 for Rightbrain work, Dispatch would become worth evaluating at that point
---
## Journal sync — 30 April 2026 (source: "Still in Toon")
- **Public GitHub repo flagged as a bad idea:** Kiwifruit explicitly identified the current public `sb-notes/second-brain` repo as a privacy risk during a discussion with team members (Anthony, Hugo, Pete T) in Newcastle. Needs to be made private or migrated away from GitHub. 💪 FOR OLLIE: resolve this — change repo visibility to private or migrate.
- **V3 Obsidian brainstorm (transit notes):** Key insight from Pete T — most team members interact with their second brain primarily from laptop; Kiwifruit interacts mostly from phone (journal input + starting chats). This is the constraint shaping V3 decisions. Obsidian local vaults on phone + Claude reading/writing vault files = removes GitHub entirely; SyncThing + Nassy/QFile for backup. Hugo suggested Cursor as a layer for model flexibility, but Cursor is laptop-only. Trial path: Obsidian Notion export community plugin on journal DB as a test case. See Current Status (30 Apr) for full evaluated options and decision to stay on V2 for now.
---
## Journal sync — 27 April 2026 (source: "Monday")
- Second Brain V2 confirmed fully operational. Kiwifruit has written up V1 vs V2 architecture as a comparison document and saved it in Notion. Shared at work (Rightbrain) with intent to roll out as “Product Second Brain” and talk about it with the team.
- Immediate benefit observed: fewer token-limit interruptions, faster responses from Claude.
---
## Journal sync — 20–24 April 2026 (sources: "A new week", "Chilly Tuesday", "Wednesday by the sea by the sea", "Friyay")
### Second Brain v2 completion sprint
- **20 Apr:** 5 of ~17 projects done via Co-Work (Cheryl, Aloyse, Dr Quinn, Sean from IT, Shula RTM, Marty completed). Sonnet 4.6 with no extended thinking confirmed as best model for Co-Work (long but not complex tasks). Token limits causing repeated interruptions — workaround: set next project running and step away
- **21 Apr:** Bob the Builder and Aunty Jen processed this morning. Next: Degen. After Degen, Tier 1 projects all done. Then Tier 2 to follow at leisure. Note for State File Index: needs to be updated to replace v1 state file URLs with v2 live GitHub URLs for each project; also needs to document the broader set of state files per project
- **22 Apr:** Second Brain v2 nearly complete — all but 2 minor projects remaining. Plan to complete both over lunchtime today. Then: populate split state files, test whole system. Very confident this will reduce Claude response delays and improve conversation quality. Intent: roll out at work + share on podcast
- **24 Apr:** 2 small projects still to split. Writing Markdown to Notion still to do. GitHub Action to sync Notion → GitHub being planned (likely a scheduled GitHub Action). Testing and refinement after that. V2 should work until the Obsidian V3 migration (mid-term, not now)
### YouTube Music → Plex migration (ongoing)
- Still pending: metadata rewriting (YouTube Music strips metadata; Claude/Claude Code to help rewrite) + playlist import into Plex
- Goal: cancel YouTube Music Premium (~£260/year saving). Also need to save Miss Rachel + Miss Apple catalogues to Nassy before cancelling
- Fix Plex on Shield TV still outstanding (works on other devices)
### Obsidian V3 (mid-term exploration)
- Kiwifruit explored Obsidian as potential V3 for Second Brain via Perplexity session (24 Apr, late evening). Not acting on this now — committed to v2 through to testing. Will collect data points over time. Decision: mid-term consideration only; V2 system to run until a clear case exists for V3
---
## Journal sync — 1–2 March 2026
### Pixel 8 migration context
- Pixel 8 purchased (noted in 27 Feb journal) specifically to reduce IT frustrations during parenting period
- Migration from Pixel 4a in progress; 30-day Back Market return window still active
- Wife also upgrading from Pixel 3a → Pixel 8 via same Back Market deal
### Notion journal automation — set up successfully (1 Mar 2026)
- Claude journal-to-markdown pipeline set up: Ollie dictates journal notes (voice), converted to Notion entries
- Current state files in Notion now being used across multiple Claude projects via MCP
- Each Claude thread appends updates to relevant state files; index file lists all
- System described as working well — "set up Claude with current state files in Notion"
- Journal indexing project completed: 35 entries from Sept 2024 – Mar 2026 processed and routed to state files
1. **Adding new equipment** — add a row to the relevant table with make, model and any key notes
1. **Energy renewals** — update the Energy section with new tariff details each April
> 💡 This page lives in the **Home** workspace in Notion and replaces the need to store long conversation histories as project files for context.
---
## 🗂️ Notion Workspace Structure (set up 28 Feb 2026)
- **🏠 Home** page created as top-level hub for all current state files
- **Sean from IT — Current State** (this page) is the first child page
- Future current state pages to be added as sub-pages of Home: Aloyse Adoption, Aunty Jen Cooking, Bob the Builder, etc.
- State File Index (routing table) is at: [📋 State File Index v2 ](https://www.notion.so/31424a1cf0f081a186aade69d7e17878)
- Home hub page: [Second brain state files](https://www.notion.so/31324a1cf0f08174a3c4fcbeba44664f)
---
## 🗂️ Project Files Review — Updates (5 Mar 2026)
### NAS Upgrade Research (Jan 2026)
- Researched UGREEN NASync DXP2800 as potential future NAS upgrade vs alternatives (Synology DS223J, Terramaster F2-221, QNAP TS-233)
- DXP2800 has best-in-class hardware (Intel N100, 8GB DDR5, 2.5GbE) but premium price and maturing software (UGOS)
- **Current position:** No NAS upgrade planned — QNAP TS-251D still meeting needs. Filed for reference if TS-251D fails
### Withings Watch Research (Dec 2025)
- Reviewed Steel HR vs ScanWatch as Garmin replacement (charging every 5 days was pain point)
- Steel HR: ~25 days battery, £140–160 | ScanWatch: ~30 days, £210+, sapphire glass, ECG/SpO2
- ScanWatch premium is marginal benefit in practice per Reddit; Steel HR is better value for basic needs
- **Status:** Withings Activité Steel HR currently owned. ScanWatch upgrade still under consideration
### Power Bank Research (Aug 2025)
- Anker preferred over Mixx for family "set and forget" power bank; Ugreen/Baseus also credible
- Reviewed 10k/20k/26k mAh options with fast charge for Pixel 3a, 4a, 8a and tablet use
- **Purchase status:** Not confirmed as purchased in project files — check if still outstanding
  ## 🖥️ Plex / Home Network — Indirect Playback Issue (Mar 2026)
  - Shield TV showing "Indirect playback" warning in Plex — streaming via Plex relay (~2Mbps) instead of direct LAN
  - Issue triggered by shelf collapse (cat knocked everything off) — Shield lost physical Ethernet connection
  - Shield fell back to WiFi on a different Deco mesh node than QNAP (NASSY), forcing Plex through internet relay
  - NASSY wired to Entryway Deco node (IP: 192.168.68.250); Shield was no longer visible as a wired device in Deco app
  - Root cause confirmed as physical disconnection, not QNAP firmware update (though update was done twice in one day and was initial suspect)
  - **Troubleshooting steps taken:** changed Plex "Allow insecure connections" from Never → Preferred; verified Netflix worked (internet OK, LAN not); confirmed Shield missing from all Deco nodes
  - **Fix in progress:** 6× 3m Cat6 cables ordered, arriving next day — will reconnect Shield to Lounge Deco node
  - **QNAP Plex settings to configure post-reconnection (if issue persists):**
    - Network → Secure connections: Preferred
    - Enable server support for insecure connections: On (No Authentication)
    - LAN Networks: `192.168.68.0/24`
    - Treat WAN IP As LAN Bandwidth: ON
    - IPs allowed without auth: `192.168.68.0/24`
  - **Deferred:** Move NASSY upstairs with AV1000 powerline adaptors; benchmark throughput before committing to this for 4K content
  - Side issue: Ultimea surround sound also stopped — kids had switched it off at the wall (resolved)
  - Workaround active: Plex working at reduced quality via relay
  ## 📱 Hannah's Mobile Migration — EE → Giffgaff (Mar 2026)
  - Hannah migrating from EE to Giffgaff (same path as Ollie's earlier migration)
  - Giffgaff referral SIM received by post (activation code: XVWM9X) — triggers £5 payback to Ollie + £5 bonus credit to Hannah on activation
  - Hannah's current handset: **Pixel 3a** — does NOT support eSIM; physical nano SIM only
  - Physical nano SIM from referral letter used for activation
  - PAC code obtained from EE; number port in progress via Giffgaff app
  - Plan: **£10/month rolling 40GB** (no contract) — minimum viable spend
  - Pixel 3a to be upgraded to Pixel 8 (Back Market refurb) later in 2026; eSIM will be available at that point
  - Ollie previously followed identical path: EE → Giffgaff on Pixel 4a, then upgraded to Pixel 8
