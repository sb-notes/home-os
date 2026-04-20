---
project: sean
file: sean-tools
tier: warm
schema_version: 2
last_updated: 2026-04-20
token_budget: 1000
---

# Sean from IT — Tools, Workflows & Setup

## Key Principles

- **Minimum viable spend** — refurbished/secondhand preferred over new where quality holds
- **Set and forget reliability** — prefer solutions needing no ongoing maintenance once configured
- **Privacy first** — Surfshark VPN + Brave browser on all devices as standard
- **Self-hosted over cloud** — NAS as private cloud for photos, music, media
- **UK sources preferred** — giffgaff, Octopus Energy, Amazon UK, signalchecker.co.uk
- **Carrier-unlocked phones only** — Verizon/locked models incompatible with UK networks
- **QNAP firmware updates** commonly reset Plex settings — document and check after every update

## Wispr Flow

- **Platform:** Voice dictation app, used on Android (Pixel 8) and Mac
- **Primary use:** Daily morning journal dictation → Notion → Claude state files
- **Gboard integration:** Toolbar icon is the preferred trigger. See `sean-devices.md` for full Pixel 8 setup, battery fix, and volume button fallback.
- **Workflow:** Wispr Flow → Notion entries → Claude journal indexer → state files updated

## Notion MCP Cross-Workspace Architecture (28 Mar 2026)

- **Confirmed:** Notion MCP auth is scoped per-Claude-account, per-workspace. Personal Claude → personal Notion; work Claude → work Notion. No cross-workspace access.
- Tested 28 Mar 2026: personal Claude can only see the "Ollie" teamspace; Rightbrain workspace not accessible.

### Rightbrain clipboard workflow (Option B — adopted)

Ollie dictates morning journal into personal Notion workspace as usual. Personal Claude routes personal items to personal state files. Claude outputs a formatted "📋 RIGHTBRAIN CLIPBOARD" text block at end of response containing any work-relevant updates. Ollie copy-pastes the clipboard block into a Rightbrain Claude conversation, which writes to Rightbrain state files in the Rightbrain Notion workspace. Custom instruction for clipboard extraction added to Cheryl project (28 Mar 2026). Overhead: ~30 seconds per morning session when work content is present.

To enable direct cross-workspace access in future: would require reconnecting Notion MCP integration and granting access to both workspaces during OAuth flow — depends on Rightbrain Notion admin permitting external integrations.

## Claude Dispatch — Decision (25 Mar 2026)

**Decision: Not adopting Dispatch at this time.**

- Home setup: all files cloud-based and API-accessible (Notion, Google Drive, Gmail) — no local compute needed; existing Android → Claude mobile workflow already covers async task dispatch
- Work setup: M5 is work-only; separation of concerns means no personal Claude Cowork session running on it
- **Future trigger for revisiting:** If Kiwifruit begins running local LLMs or processing heavy client data dumps locally on the M5, Dispatch would become worth evaluating then

## Notion Plan (downgraded 13 Apr 2026)

- Downgraded from Business to Plus plan
- Rationale: Notion AI no longer used — replaced by Wispr Flow for voice input
- Claude MCP integration unaffected (API-based, not tied to Notion AI)
- Features retained on Plus: Basic integrations (Slack, Google Drive, Gmail)
- Features lost: Notion Agent, Custom Agents, AI Meeting Notes, SAML SSO, Enterprise search, Premium integrations

## House Layout — 53 Victoria Road

**Property:** Victorian mid-terrace, 3 storeys, ~1,297 sq ft. Front faces south, rear faces north.

### Ground Floor
Kitchen (rear/north), Dining Room/Playroom (middle, west-facing), Living Room (front/south bay window)

### First Floor
Two bedrooms, bathroom, utility room

### Second Floor (Loft Conversion)
- **Master bedroom** — blue feature wall (east), Velux in north-facing roof slope, sloped ceilings, wooden floorboards
- **Alcove/Landing** (3.4m × 1.6m, ~93cm wide) — Kiwifruit's former home office (Position A). Too narrow for green screen with Elgato FaceCam MK2 wide-angle lens. Floor slopes slightly. Dresser now relocated here as secondary standing surface for wireless headset calls.
- **Shower room** off landing

### Desk position decision (26 Mar 2026)

**Position D chosen.** Desk on north wall of loft bedroom, facing south. Planned for weekend 29–30 Mar 2026 — confirm complete.

- Velux over left shoulder: consistent indirect natural light, no glare. Blackout blind integrated.
- Green screen: 2m+ flat wall behind desk suits Elgato FaceCam MK2
- North wall section: 171.5 cm; south wall section: 165 cm
- Bed moving to south side, headboard against south wall (203 cm bed, must remain perpendicular)
- Position A retired (93 cm too narrow, west-facing glare)
- Position C rejected (noise, 2-storey carry, unstable desk)
