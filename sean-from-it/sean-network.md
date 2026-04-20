---
project: sean
file: sean-network
tier: warm
schema_version: 2
last_updated: 2026-04-20
token_budget: 1000
---

# Sean from IT — Network & Connectivity

## Broadband

- **Provider:** BT (fibre) — main internet connection

## Mesh WiFi

- **Router/Mesh:** TP-Link Deco M9 Plus — covers all 3 floors
- NAS (Nassy) connected to a Deco M9 node via Ethernet

## NAS — Nassy (QNAP TS-251D)

- **Hardware:** Intel Celeron J4005, 2-bay, 8GB DDR4 RAM (max)
- **IP (local):** 192.168.68.108
- **Tailscale IP:** 100.86.115.108
- **Location:** Loft, connected via AV1000 powerline adapters
- **Drive 1 (primary):** Seagate IronWolf 8TB — main storage
- **Drive 2 (backup):** WD Red Plus 8TB (secondhand) — daily backup of IronWolf. WD is quieter; plan to swap to primary when convenient
- **Key note:** Firmware updates on QNAP commonly reset Plex settings — check and document after every update

### NAS folder structure (relevant paths)

- `/Media/Photos/` — QFile auto-upload target (both Pixel 8s, date-based subfolders)
- `/Media/Music/` — Plex music library (`/YTM Catalog/`, `/Playlists/`, `/Uploaded Files/`)
- `/Media/` — Carciofi has QuMagie access; permissions confirmed Read Only (Apr 2026)

### NAS services running

- **Plex Media Server** — served from Nassy; transcoding via Shield Pro
- **Tailscale** — remote access; avoids port forwarding
- **QuMagie** — AI photo management; live for Carciofi (Hannah's family photo access)
- **QFile** — mobile photo upload app (Google Play); QMagie mobile upload being discontinued

## VPN

- **Surfshark** — active across all devices. Split tunnelling managed carefully around Plex and Tailscale

## Remote access

- **Tailscale** — preferred method for remote Plex access

## Mobile

- **Kiwifruit's provider:** giffgaff (O2 network) — switched from EE; better signal in Shoreham-by-Sea BN43
- **Carciofi's provider:** giffgaff (O2 network) — Giffgaff SIM ported after Pixel 8 migration (Mar 2026)
- **Carciofi's Pixel 8 — spam call filtering (2 Apr 2026):** giffgaff (O2) hides "Filter spam calls" toggle on Pixel 8 (carrier restriction). Workaround: Caller ID & Spam enabled, Call Screen (on-device AI) on, Should I Answer? app installed. Unknown number blocking not enabled (too aggressive). Combo silences suspected spam without vibrating.

## NAS upgrade research (filed, no action planned)

Researched UGREEN NASync DXP2800 as potential future NAS upgrade vs Synology DS223J, Terramaster F2-221, QNAP TS-233. DXP2800 has best-in-class hardware (Intel N100, 8GB DDR5, 2.5GbE) but premium price and maturing software (UGOS). **Current position:** no upgrade planned — QNAP TS-251D meeting needs. Filed for reference if TS-251D fails.
