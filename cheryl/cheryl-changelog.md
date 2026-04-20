---
project: cheryl
file: cheryl-changelog
tier: changelog
schema_version: 2
last_updated: 2026-04-19
---

# Cheryl — Changelog

Append-only chronological log of meaningful changes to the Cheryl state files. Newest entries at the top. One to two lines per entry, stating what changed and why. Loaded only on explicit request — not loaded during normal Q&A or update cycles.

<!-- APPEND_ANCHOR -->

### Update: 19 Apr 2026
v2 architecture migration: monolithic Cheryl state file split into live, eight warm files (emdr, emdr-prep, patterns, catarina, self-care, anger, family, hannah), cold archive, and this changelog. Scope sharpened to *listener, collector, and prep assistant* — not goal-setter, not EMDR practitioner. Third-party codename `therapist-c` applied throughout; `somatic-therapist-1` used for Sarah (fascia). Worst Memories List retained in private Notion only with pointer in `cheryl-emdr-prep.md`. Schema version 2 in effect.
