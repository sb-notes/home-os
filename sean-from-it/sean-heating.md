---
project: sean
file: sean-heating
tier: warm
schema_version: 2
last_updated: 2026-04-20
token_budget: 2000
---

# Sean from IT — Heating, Home Systems & Energy

## Boiler — Main House

- **Model:** Vaillant ecoTEC Plus 835 H combi
- Water pressure confirmed 1.7 bar (healthy)
- Spanner icon showing = annual service reminder, not a fault
- Chimney sweep mode accidentally triggered and cancelled 10 Apr 2026 — no settings affected

## Drayton Wiser Kit 3 (upgraded 10 Apr 2026)

- **Model:** Wiser Kit 3 (WT734R) — upgraded from Kit 1 by electrician Jamie (nephew of Paul, PJ Plumbing)
- **Provides:** 2 heating channels + 1 hot water channel

### Channel wiring (as installed 10 Apr 2026)

| Channel | Assignment | Physical wiring |
|---|---|---|
| Channel 1 | Heating | Radiator circuit (TRVs + room thermostats) |
| Channel 2 | Hot Water | UFH pump circuit (physically wired here — confirmed by floorboard creak test) |
| Channel 3 | Heating | Kitchen room thermostat for UFH control; physical wiring to UFH pumps still on Channel 2 terminal |

### Outstanding wiring issue

UFH pumps are wired to the hot water terminal (Channel 2) rather than Channel 3. Hot water channel is binary on/off with no thermostat association — kitchen room thermostat on Channel 3 cannot call the UFH pumps directly.

**Workaround:** Hot water schedule covers UFH timing.

**Proper fix (Jamie return visit needed):** Move UFH pump cable from hot water terminal to Channel 3 terminal; confirm boiler demand wire covers both channels independently; assess motorised zone valve on UFH circuit for independent heat calling.

**Note:** All 3 channel outputs confirmed identical — 2(1)A 230V relay switches; no electrical difference between heating and hot water terminals per Drayton spec sheet.

### Devices paired to Kit 3 hub (10 Apr 2026)

- Lounge room thermostat (Channel 1)
- Kitchen room thermostat (Channel 3)
- Lounge TRV
- Bedroom TRV
- Kids bedroom TRV
- Landing smart plug / repeater

**Still to pair:** Loft TRV, Playroom TRV

---

## Wiser Room Thermostat — Factory Reset & Re-pair Procedure

**Confirmed working 10 Apr 2026.** Devices paired to old Kit 1 hub and not deleted before hub replacement.

1. In the Wiser app, **start pairing mode first**: + → Add Device → Room Thermostat — get it actively searching before touching the thermostat
2. Remove **both** batteries, wait **20 seconds** (removing only one battery does not work)
3. Reinsert both batteries with + and − fingers ready
4. Immediately press and hold **both + and − buttons simultaneously**
5. Keep holding for up to 20 seconds until screen shows **green background with WiFi symbol** = pairing mode
6. App should find device within 30 seconds of WiFi symbol appearing

> The app must be in searching mode **before** the thermostat boots — not after. The pairing window is short. If the WiFi symbol appears but joining fails, move physically next to the hub and retry from step 1.

---

## Wiser TRV — Factory Reset & Re-pair Procedure

**Confirmed working 10 Apr 2026.** Official Drayton documentation is unreliable — use this method.

1. Remove batteries, wait 10 seconds, reinsert
2. Let TRV boot until you see **3 flashing LEDs** (red left, red centre, blue right)
3. Twist cap **right (+)** — blue light for 3 seconds — let it calibrate (valve moves)
4. Twist cap **right (+) and hold for ~15 seconds** until centre LED flashes red **8 times** — then red + blue flashing with orange in centre
5. Twist cap **left (−) for 3 seconds** — centre LED turns **solid green** = pairing mode
6. In the Wiser app: + → Add Device → Radiator Thermostat — device found and paired

> Do one TRV at a time. Pair each before resetting the next.

---

## Underfloor Heating (Main House)

Two 240V pump zones (kitchen slab, diner raised floor) — operate simultaneously as one logical zone. Previously controlled by Solfex (decommissioned, wires capped). Now on Wiser hot water channel. See wiring issue above.

---

## Let-out Flat Systems

- **Boiler:** Vaillant ecoTEC Plus 835 H combi A — managed separately
- **Heating controller:** Solfex thermostat
- **Fault history (Mar 2026):** F.22 (low water pressure) + F.53 (mass flow sensor) — resolved by re-pressurising to 1.3 bar and resetting. Target cold pressure: 1.2–1.5 bar

---

## Other Home Systems

- **Baby monitor:** Boifun (Baby 3SM/6T-style) — uses BoifunCam/CloudEdge app
- **Dishwasher:** Bosch SMV69M01GB — E09 error = heat pump/heater assembly fault

---

## Octopus Energy (Account: A-CEC10C86)

### April 2026 renewal — completed

Renewed to Octopus 12M Fixed before 3 Apr 2026 deadline.

- **Current tariff (Fixed 12M):** Electricity 25.83p/kWh; Gas 5.57p/kWh; est. monthly £145.88
- Saves ~£100/year vs Flexible Octopus based on actual usage
- No exit fee on either option

### Previous tariff (until 3 Apr 2026)

- Loyal Octopus 12M Fixed (April 2025 v1)
- Electricity: 23.75p/kWh | Standing charge: 44.44p/day
- Gas: 5.61p/kWh | Standing charge: 29.59p/day

### Meters

- Electricity smart meter: 23J0437513
- Gas smart meter: E6S11867532462

### Actual usage analysis

| Period | Context | Avg electricity/month | Avg gas/month |
|---|---|---|---|
| Jan–Feb 2025 | 2 adult lodgers | 343 kWh | 1,213 kWh |
| Apr–Aug 2025 | Lodgers gone, summer, 2 adults | 154 kWh | 170 kWh |
| Sep–Nov 2025 | Children moved in, old Google Nest | 275 kWh | 580 kWh |
| Dec 2025–Feb 2026 | Drayton Wiser TRVs + new front door | 267 kWh | 1,592 kWh |

**Key insight:** Gas higher in winter 2025–26 reflects the house being properly heated room-by-room for the first time. Electricity 19% lower year-on-year (Jan 25→Jan 26: 333→271 kWh) despite children now in house — Wiser smart scheduling working. New front door (Jan 2026) completed full double glazing; will compound savings from next winter. Actual 12-month gas usage ~9,600–10,500 kWh; Octopus estimate of 12,365 kWh overstated.

### Milestones affecting usage

- Mar 2025: 2 adult lodgers moved out
- Sep 2025: Bunny and Fox moved in
- Dec 2025: Google Nest replaced with Drayton Wiser + TRVs on all radiators
- Jan 2026: New front door fitted — entire house now double glazed
