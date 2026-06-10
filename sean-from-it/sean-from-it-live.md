# Sean from IT — Current State (6 Jun 2026)

<!-- Auto-synced from Notion. Last sync: 2026-06-10 06:22 UTC -->

---
## Weekly triage — 6 June 2026
- Rows reviewed: 2
- Addressed (pattern, fix proposed): 1
- Accepted (one-off): 0
- Won't fix (stale): 0
- Still open (needs input): 1
### Proposed skill fixes
- journal-indexer-v2 — update Severity enum to minor/friction/blocker; add Home to valid Project field values
### Rows still open
- weekly-wrap-up: live state files inaccessible in automated Cowork run — workaround deployed in v2.0; three fix paths proposed (lightweight summary files, MCP pagination, GitHub pre-seeding). Needs owner decision before closing.
### Failed updates
- (none)
---
## Indexer run — 6 June 2026 04:30
- Entries indexed: 6 (Journal Sunday 31 May, Journal Monday 1 Jun, Journal Tuesday 2 Jun, Journal Wednesday 3 Jun, Journal Thursday 4 Jun, Journal Friday 5 Jun)
- State files updated: Cheryl, Aloyse, Dr Quinn, Marty, Shula RTM, Bob the Builder, Degen, Sean from IT, Shoreham Tech Live
- Dedup skips: 0
- Deferred LOW routes: 0
- Rotation: Sean from IT (stale May syncs moved to archive ✔); Marty (21–29 May ✔); Shula (22–29 May ✔); Degen (21–28 May ✔); Cheryl/Aloyse/Dr Quinn deferred (cap-zone, >15K chars — logged to Health Log)
- Friction items logged: 2 (cap-zone rotation deferred; skill file Severity values mismatch)
- Pre-flight issues: none
---
## Journal sync — 1–5 Jun 2026 (sources: "Journal Monday" 1 Jun, "Journal Wednesday" 3 Jun, "Journal Friday" 5 Jun)
### Home OS v2.1 — confirmed working (1 Jun)
- All automations confirmed running post v2.1 upgrade:
  - Weekly indexer: Saturday morning ✔
  - Weekly wrap-up: auto-generated ✔
  - Sunday news briefing: emailed to Kiwifruit and Carciofi ✔
  - State file rotation: archive pages in place for all live files ✔
- Home OS is now applying all learnings from Rightbrain Product OS (skills upgrade, pruning, self-healing, scheduled triage)
- Carciofi now using Claude / Home OS — Dr Quinn and Aloyse active; Kiwifruit validated this as worth it
### GitHub repo — privacy review flagged (3 Jun)
- Kiwifruit wants to analyse whether GitHub is still needed or whether Home OS can run on Notion alone
- Assessment: Notion MCP may now be stable enough; rotation + archive + weekly triage means lighter live files; self-healing mechanisms in place
- Strong urge to make the public `sb-notes/second-brain` repo **private** (privacy concern first flagged Newcastle Apr 2026)
- Also noted: GitHub now has new personal access token type (annual rotation) — worth revisiting if keeping GitHub
- Plan: investigate over the weekend of 6–7 Jun; if it makes sense, make private
### SumUp — payment setup (31 May)
- Local artist (sells watercolours/oils roadside) doesn’t take card payments; Kiwifruit wants to buy a painting for Carciofi’s birthday
- Research done: SumUp identified as the right solution
- SumUp set up on Kiwifruit’s phone so he can take payments if needed
- Plan: next time Kiwifruit sees the artist, offer to help him set it up
- Also: SumUp can be used for Art with Hannah, Italian with Hannah, and Coming to Terms book sales — to show Carciofi how it works and offer to set it up
### Product OS — Notion as state file store concerns (5 Jun)
- Key realisation: much of the Kiwifruit’s Product OS build has been working around Notion’s shortcomings as a state file store
- Next upgrade to Product OS very likely to move state files off Notion (possibly Obsidian vault, synced to phone app)
- This will have implications for Home OS too — worth monitoring
## Session update — 2 June 2026
- **Shula RTM naming fix resolved:** `shula-rtm/shula-rtm-live.md` content migrated into `shula-rtm/shula-live.md` via Claude Code. Orphaned file deleted. Pushed to `sb-notes/home-os` main (commit from 2 Jun 2026, using freshest indexer sync 06:51 UTC). Indexer will now read `shula-live.md` cleanly.
- **home-os-weekly-triage skill updated to v1.1:** Stage 1 rewritten — `notion-fetch` on DB page returns schema only, not rows. Now uses 3-pass `notion-search` to surface open rows. Updated in scheduled task, Indexer project [SKILL.md](http://skill.md/), and Notion skill library.
---
## Weekly triage — 2 June 2026
- Rows reviewed: 0
- Addressed (pattern, fix proposed): 0
- Accepted (one-off): 0
- Won't fix (stale): 0
- Still open (needs input): 0
### Proposed skill fixes
- (none)
### Rows still open
- (none)
### Failed updates
- (none)
---
## Weekly triage — 31 May 2026
- Rows reviewed: 0
- Addressed (pattern, fix proposed): 0
- Accepted (one-off): 0
- Won't fix (stale): 0
- Still open (needs input): 0
### Proposed skill fixes
- (none)
### Rows still open
- (none)
### Failed updates
- (none)
### Notes
- Sean from IT was over ~12K char cap at triage time. Rotation performed this session — page now trimmed. Archived syncs moved to sean-from-it-archive.
- structural_drift Health Log row `2026-05-31 — home-os-weekly-triage — sean-cap-exceeded` closed as addressed.
---
## Home OS v2.1 upgrade session — 31 May 2026
### What was done
- Renamed: Home hub → "🧠 Home OS — State Files"; State File Index → "📋 Home OS — State File Index v2.1"
- State File Index callout updated: "Second Brain v2" → "Home OS v2.1"; Archive Registry ID and Health Log DB ID added
- Health Log DB confirmed: collection `6bd25f74-c9db-42a3-a66d-0db5dda4149c`, page `1d454956-af8b-47f3-aa74-b28be43b144f`
- Archive pages created for all 9 Tier 1 state files (see IDs below)
- Archive Registry created: `37124a1cf0f081eaa84bead4c8d70bbc`
- journal-indexer-v2 scheduled skill updated to v2.2: Health Log DB IDs confirmed, Rotate ENABLED, codename table expanded (20+ additions, Catarina → Origano), friction schema aligned to real DB fields, schedule corrected to 04:30
- home-os-weekly-triage skill created: scheduled Saturday 09:00; four-stage loop (fetch open Health Log rows, triage, update, close-out to Sean from IT)
- [home-os-weekly-triage-SKILL.md](http://home-os-weekly-triage-skill.md/) written to Indexer project folder
- Skill library DB updated: journal-indexer-v2 entry updated to v2.2; home-os-weekly-triage v1.0 entry created
### Archive page IDs created this session
- aloyse-archive: `37124a1cf0f08177b6ebd6adca50eae5`
- cheryl-archive: `37124a1cf0f08192b57bf93f8e3c4de4`
- dr-quinn-archive: `37124a1cf0f081fa9a23c86644d34259`
- marty-archive: `37124a1cf0f0810392a2eb563b505606`
- rosie-rentals-archive: `37124a1cf0f081c7816ffe0d1f59cdc6`
- shula-archive: `37124a1cf0f08158a2a7cc6931a685a2`
- sean-from-it-archive: `37124a1cf0f0813bae04eee90cde65bc`
- degen-archive: `37124a1cf0f0816583c1e5e9aed174cb`
- jamesbot-archive: `37124a1cf0f081fa9d4ad8d266a1b751`
### Friction observed
- Sean from IT file at 49.7KB (well over 15K cap) — rotation urgently needed on next indexer run
- Product OS Skill Library ID (35843123...) is Rightbrain workspace — inaccessible from personal MCP; correct library is `eb19ab66-c12e-4ea6-b72b-03dd7071ac44`
- Coaching scheduled task currently disabled — not changed this session
### Gotchas for skill updates
- Catarina codename was `therapist-c` in indexer v2.0/v2.1 skill library entry and scheduled skill; corrected to `Origano` in v2.2
- `Origano` was already correct in weekly-wrap-up v1.1 and weekly-coaching v1.1 — no change needed there
- Health Log DB schema: field is `Type` (not `Category`), `Status` values are `open/addressed/accepted/wont_fix` (not `Open/Resolved/Parked`), `Workaround` field exists, no `Logged by` field
---
## Indexer run — 30 May 2026 06:00
- Entries indexed: 10 (Journal Thursday 21 May, Journal Friyay 22 May, Journal Saturday 23 May, Journal Sunday 24 May, Journal monday 25 May, Journal Tuesday 26 May, Journal weds 27 May, Journal Thursday 28 May, Journal Friday 29 May, Journal Saturday 30 May)
- State files updated: Cheryl, Aloyse, Dr Quinn, Marty, Shula RTM, Rosie Rentals, Secret Adopters, Bob the Builder, Degen, Augmented, Sean from IT
- Dedup skips: Journal Thursday 21 May → Cheryl (skip, covered by 15–22 May sync); Journal Thursday 21 May → Dr Quinn (skip); Journal Friyay 22 May → Cheryl (skip); Journal Friyay 22 May → Dr Quinn (skip); Journal Sunday 24 May → Aloyse (skip, 24 May already synced)
- Deferred LOW routes: 0
- Friction items logged: 1 (see below)
- Pre-flight issues: Health Log DB ID was still a placeholder — friction logged to this file instead
## Indexer friction — 30 May 2026
- **Category:** missing_infrastructure
- **Severity:** friction
- **Description:** Health Log DB ID remains the placeholder string `[HOME-HEALTH-LOG-DB-ID — confirm before Saturday run]` in the skill file. Friction items from this run logged here instead. Action needed: confirm the Health Log DB ID and update the skill file before next run.
- **Suggested fix:** Locate or create the Home Health Log DB in Notion; copy its collection ID into the skill file replacing the placeholder.
---
- **UseBean USB-C to USB-C Right Angle 100W 2M, USB 3.2 Gen 2x2 (20Gbps)** — x2, £7.99 each, Amazon UK, Prime delivery Friday 29 May
- **Cable 1 (monitor):** Mac Port 2 → LG 27" monitor. Replaces original 2020 LG monitor cable. Supports 4K DP Alt Mode + 100W PD.
- **Cable 2 (webcam):** Mac Port 1 → Elgato Facecam MK2. USB 3.2 should shift webcam from USB 2.0 (480Mbps) to USB 3.0/3.2 mode — confirm by checking device name changes from `Elgato Facecam MK2 (USB2)` to `Elgato Facecam MK2 (USB3)` in Google Meet camera selector after swap.
---
## Newsboy weekly briefing — skill & schedule setup — 31 May 2026
- **ollie-weekly-briefing skill v3** created and saved to Newsboy project folder
- Section order restructured: AI & Agentic Tech moved to section 5; Spiritual & Energetic Update moved to section 6 (last)
- Source requirement added: every story/bullet must now end with `Source: [Name](URL)`
- Email delivery added: briefing auto-emails to [hannahandollieuk@gmail.com](mailto:hannahandollieuk@gmail.com) after each run; subject `🌍 Weekly Briefing — [date]`
- Scheduled task created: `ollie-sunday-briefing` — runs every Sunday at 06:00
- Action required: run the scheduled task manually once ("Run Now" in Scheduled sidebar) to pre-approve tool permissions before first automated run
---
> 📂 **Archived syncs:** Journal syncs and status updates from 1 March – 10 May 2026 have been moved to [sean-from-it-archive](https://www.notion.so/37124a1cf0f0813bae04eee90cde65bc). Rotated 31 May 2026.
---
Last updated: 31 May 2026 — maintained by Kiwifruit & Claude
This is the single source of truth for all technology, equipment, services and energy decisions in the house. Update this page whenever something changes, so future Claude threads can be pointed here instead of relying on project file storage.
---
## 👨‍👩‍👧 Household
- **Occupants:** Oliver + wife + children (moved in Sep 2025)
- **Property:** Victorian terraced house, 3 floors, Shoreham-by-Sea, West Sussex
- **Flat (let out separately):** Has Solfex thermostat + Vaillant boiler in loft — managed separately
---
## ⚡ Energy — Octopus Energy (Account: A-CEC10C86)
### Current Tariff
- **Tariff:** Octopus 12M Fixed (renewed April 2026)
- **Electricity:** 25.83p/kWh | Standing charge: 44.44p/day
- **Gas:** 5.57p/kWh | Standing charge: 29.59p/day
- **Meters:** Electricity smart meter 23J0437513 | Gas smart meter E6S11867532462
- **Est. monthly:** £145.88 | Saves ~£100/year vs Flexible Octopus
- **No exit fee**
### Actual Usage (Jan 2025–Feb 2026)
| Period | Context | Avg Elec/mo | Avg Gas/mo |
| --- | --- | --- | --- |
| Jan–Feb 2025 | 2 adult lodgers | 343 kWh | 1,213 kWh |
| Apr–Aug 2025 | Lodgers gone, summer | 154 kWh | 170 kWh |
| Sep–Nov 2025 | Children moved in, Google Nest | 275 kWh | 580 kWh |
| Dec 2025–Feb 2026 | Wiser TRVs + new front door | 267 kWh | 1,592 kWh |
**Key insight:** Actual 12-month gas ~9,600–10,500 kWh (Octopus estimate of 12,365 kWh is overstated). Electricity 19% lower YoY despite children moving in — Wiser smart scheduling confirmed working.
---
## 📧 Email & Mailing List — [italianwithhannah.com](http://italianwithhannah.com/)
### Setup summary
- **Domain registrar / DNS:** Hostinger ([hpanel.hostinger.com](http://hpanel.hostinger.com/) → Domains → DNS / Nameservers)
- **Email provider:** Titan Email (via Hostinger) — MX records point to [mx1.titan.email](http://mx1.titan.email/) / [mx2.titan.email](http://mx2.titan.email/)
- **Mailing list platform:** [Sender.net](http://sender.net/)
### How to connect [Sender.net](http://sender.net/) to a Hostinger domain
In [Sender.net](http://sender.net/): Settings → Sender Domains → Authenticate → your domain → shows DKIM, SPF, DMARC records to add.
**DKIM (CNAME record)**
- Type: CNAME | Name: `sender._domainkey` ⚠️ Hostinger pre-fills `@` here — change it
- Target: `dkim.sendersrv.com` | TTL: 14400
**DMARC (TXT record)**
- Type: TXT | Name: `_dmarc` | Content: `v=DMARC1; p=none;` | TTL: 14400
**SPF (TXT record — edit existing, do not add new)**
- Edit existing Titan record: `v=spf1 include:spf.titan.email ~all`
- Merged value: `v=spf1 include:spf.titan.email include:sendersrv.com ~all`
**Verify:** Return to [Sender.net](http://sender.net/) → click **Check SPF, DKIM and DMARC records**. Propagation typically 15–30 mins on Hostinger.
---
## 🌐 Network & Connectivity
- **Broadband: BT (fibre)** — main internet connection
- **Router/Mesh: TP-Link Deco M9 Plus** — mesh WiFi across 3 floors
- **NAS: QNAP TS-251D "Nassy"** — Intel Celeron J4005, 2-bay, 8GB DDR4 RAM max. Connected to Deco M9 node via Ethernet. IP: 192.168.68.108
- **NAS Drive 1 (Primary): Seagate IronWolf 8TB** — main storage drive
- **NAS Drive 2 (Backup): WD Red Plus 8TB** (secondhand) — daily backup of IronWolf
- **VPN: Surfshark** — used across all devices. Split tunnelling managed carefully around Plex/Tailscale
- **Remote Access: Tailscale** — for remote Plex access, avoids port forwarding. Nassy IP: 100.86.115.108
- **Mobile provider (Oliver): giffgaff (O2 network)** — switched from EE, better signal in Shoreham-by-Sea
---
## 📺 Media / Entertainment
- **TV: Panasonic TX-40GX800B** (40", 4K, 2019) — mounted on long-reach arm on chimney breast
- **Streaming/Plex server: NVIDIA Shield Pro** — runs Plex Media Server, connected to NAS via network, Plex library: Plexi
- **Plex subscription: Plex Pass (Lifetime)** — enables hardware transcoding, remote streaming, Plexamp
- **Soundbar: Ultimea D80** — connected via HDMI ARC, front surrounds wired to soundbar
- **Bluetooth speakers: EarFun UBOOM** (x2, paired together) — secondary audio
- **Plex status:** Not working on any device (server unplugged — Carciofi moved things in studio). Fix: restart Plex Media Server via web browser console; then fix Shield TV access issue.
- **YouTube Music migration:** Still pending — cancel to save ~£260/year. Also need to save Miss Rachel + Miss Apple catalogues to Nassy first.
---
### 🎧 Earbuds & Headphones (Oliver)
- **Earbuds (primary): Technics EAH-AZ100E** — purchased via Vinted Mar 2026, £164. Confirmed keeper. Left earbud long press remapped to ANC cycling. Sound: well-balanced, neutral, slightly warm. Call quality: consistent. Outdoor ANC: excellent.
- **Earbuds (backup): EarFun Air Pro 4** — retained as backup.
- **Over-ear headphones: Sony WH-1000XM4** — existing NC headphones. Bass-heavy sound signature.
---
## 💻 Computers & Phones
- **Laptop (Oliver, personal): MacBook Air M1** — personal/home use only. Brave browser, Surfshark VPN
- **Laptop (Oliver, work): MacBook Air M5 (13-inch)** — Rightbrain work machine, work-only, no personal crossover. Decision: 13-inch for portability (train travel to Newcastle).
- **Laptop (Hannah): MacBook Air M1**
- **Phone (Oliver): Google Pixel 8** (128GB Obsidian, Back Market refurb, Feb 2026, £194) — monochrome display mode, Brave browser, Surfshark VPN, giffgaff eSIM
- **Phone (Hannah): Google Pixel 3a** — giffgaff (O2), physical SIM only (no eSIM on 3a), migrated from EE Mar 2026. Pixel 8 upgrade via Back Market planned later in 2026
- **Tablet: Acer Iconia Tab M10 (A22001) 128GB** — video calls and toddlers
- **Recording device: Roland R-05** — choir concerts
- **Webcam: Elgato Facecam MK2** — 2K. Mount: Neewer 11" Articulating Magic Arm Clamp Mount (May 2026), clamped to Invision monitor arm post on Flexispot EC-1 (loft). Camera mounted upside-down — Flip applied via Elgato Camera Hub; Elgato Virtual Camera selected as source in Google Meet/Brave. See Journal sync 27 May 2026 for full procedure.
- **Microphone: Shure MV7+** — purchased via Vinted, 1 Apr 2026, £149 delivered. Brand new, sealed. USB-C direct to MacBook M5. Previous mic: MAONO AU-PM422 (retired).
- **Standing desk: Flexispot EC-1** — loft office, Position D (north wall of loft bedroom, facing south, moved Mar/Apr 2026)
### Peripherals
- **USB-C right-angle adapter:** VCOM 240W 80Gbps, 1 pair, £8.19 — MacBook Air M5 → LG 4K monitor + USB hub
- **Ergonomic mouse: Posturite Penguin 3-in-1 Large** — Bluetooth primary on MacBook M5. Dongle stored in mouse base slot as fallback.
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
---
### 🔁 Drayton Wiser TRV — Factory Reset & Re-pair Procedure (confirmed 10 Apr 2026)
This is the correct reset sequence. Ignore the official documentation — the twist-and-hold method does not work reliably.
1. Remove batteries, wait 10 seconds, reinsert
1. Let the TRV boot until you see **3 flashing LEDs** (red left, red centre, blue right)
1. Twist cap **right (+)** — blue light for 3 seconds — let it calibrate (valve moves)
1. Twist cap **right (+) and hold for ~15 seconds** until the centre LED flashes red **8 times**
1. Twist cap **left (−) for 3 seconds** — centre LED turns **solid green** = pairing mode
1. In the Wiser app: **+** → **Add Device** → **Radiator Thermostat**
> Do one TRV at a time. Pair each before resetting the next.
- **Heating controller: Drayton Wiser Kit 3 (WT734R)** — upgraded from Kit 1 on 10 Apr 2026. Kit 3 provides 2 heating channels + 1 hot water channel.
- **Channel wiring:** Ch1: Heating (radiators/TRVs) | Ch2: Hot Water (UFH pump circuit) | Ch3: Kitchen room thermostat for UFH control
- **Outstanding wiring issue:** UFH pumps wired to Ch2 terminal; kitchen thermostat on Ch3 cannot call UFH directly. Workaround: hot water schedule covers UFH timing. Fix: Jamie to move UFH pump cable from Ch2 to Ch3.
- **Boiler (main house): Vaillant ecoTEC Plus 835 H combi** — water pressure 1.7 bar (healthy). Spanner icon = annual service reminder (not a fault).
- **Wiser devices paired (10 Apr 2026):** Lounge room thermostat (Ch1), kitchen room thermostat (Ch3), lounge TRV, bedroom TRV, kids bedroom TRV, landing smart plug/repeater. Remaining to pair: loft, playroom.
- **Boiler (flat): Solfex thermostat + Vaillant ecoTEC plus 835 H combi A** — let-out flat. F.22 + F.53 faults (Mar 2026) resolved by re-pressurising to 1.3 bar. Target cold pressure: 1.2–1.5 bar.
- **Dishwasher: Bosch SMV69M01GB** — E09 error = heat pump/heater assembly fault
- **Baby monitor: Boifun** (Baby 3SM/6T-style) — uses BoifunCam/CloudEdge app
---
## 🧒 Children's Devices & Toys
### Tonies Collection (Apr 2026)
- **Toniebox:** Already owned. Children are Bunny and Fox, age 2.
- Purchases (Apr 2026, all secondhand): Sleepy Friends Nature Sounds (£8), Sleepy Friends Bedtime Lullabies (£8), Beatrix Potter Peter Rabbit Collection (£9, sealed), Tonies Sleepy Sheep Night Light (£19.50 — 4 dimmable levels, 90 mins nature sounds, USB-C rechargeable)
- Approach: Secondhand-first via Vinted/eBay. UK voices preferred. Avoid American-voiced content.
### LCD Writing Tablets (Mar 2026)
- Genialba 8.5 inch LCD Writing Tablet, 2-pack (Pink & Purple), £7.99 — replaceable coin battery (not USB rechargeable, deliberate)
---
## 🚗 Car
- **Vehicle: Toyota Auris Estate**
- **Charging: 12V / 120W cigarette lighter** — USB-C fast charger added for Android phones
---
## 🏠 House Layout — 53 Victoria Road
**Property type:** Victorian mid-terrace, 3 storeys, approx 1,297 sq ft. Front faces south. Rear faces north.
**Ground Floor:** Kitchen (rear/north), Playroom/Dining Room (middle), Living Room (front/south bay window)
**First Floor:** Two bedrooms, bathroom, utility room
**Second Floor (Loft):** Master bedroom with blue feature wall; loft conversion with Velux (north-facing). **Office: Position D** — desk on north wall facing south. Velux over left shoulder (indirect natural light). Position A (alcove, 93cm wide) retired — too narrow for green screen.
---
## 💻 Work & Claude Architecture Notes
- [**Rightbrain.ai**](http://rightbrain.ai/)** role:** Kiwifruit is Product Lead → CPO (started Mar 2026). Work machine M5 is work-only.
- **Notion MCP:** Auth is scoped per-Claude-account, per-workspace. Personal Claude → personal Notion; work Claude → work Notion. No cross-workspace access.
- **Morning journal → Rightbrain workflow (Option B):** Ollie dictates morning journal → personal Claude routes to personal state files → outputs a "📋 RIGHTBRAIN CLIPBOARD" block → Ollie copy-pastes into Rightbrain Claude conversation. Overhead: ~30 seconds per morning session.
- **GitHub repo privacy:** Public `sb-notes/second-brain` repo flagged as a privacy risk (Apr 2026, Newcastle). Action needed: change to private or migrate.
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
1. **When something changes** — update the relevant section directly in Notion
1. **Starting a new Claude thread** — paste the URL of this page and say "refer to my current state page"
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
