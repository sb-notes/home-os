# Cheryl v2 — Operator Review Pack

Everything built, everything pending, and the manual steps you need to run to ship this. Read once end-to-end before pushing.

## Files built (11 total)

All files in `/mnt/outputs/`. Shape matches the Dr Quinn canonical reference.

| File | Tier | Budget | Purpose |
|---|---|---|---|
| `cheryl-live.md` | live | 600 | Always-on snapshot, scope statement, top open actions, table of contents |
| `cheryl-emdr.md` | warm | 1200 | EMDR framework, resourcing content, container visualisation, processing thread, Gina anchor |
| `cheryl-emdr-prep.md` | warm | 400 | Next-session prep pointer; Worst Memories List stays private in Notion only |
| `cheryl-patterns.md` | warm | 1200 | Overwhelm, career anxiety, scarcity, rest-deserving, accepting-help, provider identity, crisis ideation flag |
| `cheryl-catarina.md` | warm | 1400 | `therapist-c` session history (intro, 1, 2, 3, 3b, 4), therapist pipeline, ASGSF funding notes |
| `cheryl-self-care.md` | warm | 900 | Morning walk, yoga, float, fascia, choir, guitar, sleep, peer support, self-compassion |
| `cheryl-anger.md` | warm | 1200 | Current state, Apr 2026 incidents, Mar 2026 cluster, triggers, physical forms, trajectory, resolution practices |
| `cheryl-family.md` | warm | 900 | Parents, sister, grandparents (both sides), intergenerational chain, NZ childhood, homesickness |
| `cheryl-hannah.md` | warm | 900 | "Oh Ollie" thread, repair patterns, division of labour, supportive threads, intimacy, Carciofi's health worry |
| `cheryl-archive.md` | cold | — | Therapist pipeline, 5yo-inner-child framing, Gina action, Feb–Mar family visit, NZ reframe, v1 CI boilerplate |
| `cheryl-changelog.md` | changelog | — | Seed entry for v2 migration |

Plus `cheryl-custom-instructions.md` — the paste block for the Cheryl Claude project.

## Codename map — additions to push to private map

Add to the private codename map at `https://www.notion.so/34524a1cf0f08003be18fdd0936dc819`:

- **`therapist-c`** → Catarina Rato (EMDR / somatic therapist)
- **`somatic-therapist-1`** → Sarah (fascia release bodyworker)
- **`stepfather-1`** → Steve (Carciofi's stepfather) — already in Dr Quinn map; confirm or dedupe
- **`stepmother-1`** → Jane (Carciofi's mother) — already in Dr Quinn map; confirm or dedupe

Third-party names appearing in Cheryl files that stayed as real names (low-sensitivity peers / mentors, no ongoing clinical role, no safeguarding implication): Gina (deceased mentor, Melbourne); Josh (Forever Dads peer); Jess (yoga supply teacher); Fran (yoga teacher); Pete T (colleague, one walk-and-talk). Flag if you want any of these codenamed — default is leave as-is.

Names deliberately **not** written to public mirror: Kiwifruit's real parents (named as Mum / Lynn / Dad); Kiwifruit's sister (Sam); Kiwifruit's niece (Hazel); Ollie's dad's 80th, mum's email language — these are geographic / relational markers that make the family identifiable. Currently the files contain first names for Mum (Lynn) and sister (Sam) and niece (Hazel). **Decision needed:** codename the family-of-origin trio or leave as first names only?

Proposed: `mother-1` (Mum / Lynn), `sister-1` (Sam), `niece-1` (Hazel), `father-1` (Dad). Role-plus-counter per the scheme. If approved, run find-and-replace before push.

## State File Index — additions

Edit at `https://www.notion.so/State-File-Index-updated-1-Apr-2026-31424a1cf0f081a186aade69d7e17878`.

New entries (Cheryl-owned):

- **Emotional life / inner work / therapy / EMDR** → Cheryl
- **Anger log and anger-pattern work** → Cheryl (`cheryl-anger.md`)
- **`therapist-c` sessions and homework** → Cheryl (`cheryl-catarina.md`)
- **Worst Memories List (private)** → Cheryl (pointer only in `cheryl-emdr-prep.md`; full list stays in private Notion)
- **Intergenerational trauma map / family of origin (clinical)** → Cheryl (`cheryl-family.md`)
- **Marriage / couple dynamics (relational layer)** → Cheryl (`cheryl-hannah.md`)
- **Self-care infrastructure for emotional regulation** → Cheryl (`cheryl-self-care.md`)

Cross-project disambiguations to reinforce in the index:

- Goal-setting and career accountability → **Marty**, not Cheryl
- Physical health (including Carciofi's smoking, physical symptoms) → **Dr Quinn**, not Cheryl
- Parenting and adoption (including children's behaviour, LMFM protocol) → **Aloyse**, not Cheryl
- Property / financial admin → **Rosie Rentals / Degen**, not Cheryl

## Mode-entry phrases for the future Cheryl Skill

Five phrases locked — do not build the Skill yet, but note for the separate Skill-building session:

1. **"journal"** — reflective playback of recent journal content; mirror language, widen feelings, no advice
2. **"playback"** — synonym of "journal" for when Kiwifruit wants to hear himself back
3. **"therapy"** — pull `cheryl-catarina.md` + `cheryl-emdr-prep.md`; orient toward the next session
4. **"session prep"** — stronger form of "therapy"; generate pre-session brief (may delegate to `catarina-report` skill)
5. **"weekly review"** — synthesise across all warm files; surface patterns, shifts, open threads

## Items flagged for separate sessions

- **Update Skill** (cross-project) — referenced in all v2 custom instructions but not yet built. Covers: review conversation, route to tiers, apply codenames at write time, append to changelog. Rightbrain work-extract carries forward as a post-update step (was at the end of the v1 Cheryl routine).
- **Cheryl Skill** — mode-entry routing per the 5 phrases above. Flagged in custom instructions as "pending."
- **Notion → GitHub sync** — still manual push by operator. Not blocking.

## Manual steps — operator runs these in order

1. **Review** all 11 files in `/mnt/outputs/` for anything that doesn't ring true — tone, codenames, scope.
2. **Decide** on the family-of-origin codename question (Lynn / Sam / Hazel above).
3. **Scrub** any Gina surname, Melbourne group names, or other identifying detail I may have missed — I deliberately kept Gina's first name only.
4. **Apply** codename decisions via find-and-replace.
5. **Push** all 11 files to `github.com/sb-notes/second-brain/cheryl/` on the `main` branch.
6. **Update** the Cheryl Claude project's custom instructions using `cheryl-custom-instructions.md` (replace entire contents; v1 is backed up in Notion).
7. **Update** the private codename map with the `therapist-c` / `somatic-therapist-1` / family-trio additions.
8. **Update** the State File Index (use the editable duplicate) with the entries above.
9. **Test** with a fresh Cheryl thread — suggested query: *"What's the state of EMDR prep going into Thursday's session?"* — should fetch `cheryl-live.md`, recognise EMDR topic, fetch `cheryl-emdr.md` and `cheryl-emdr-prep.md`, answer reflecting Memory 18 as first target and 17 April as the active-processing start.
10. **Sign off** and move to Sean from IT as the next pilot.

## Known trade-offs in the split

- **Family / Hannah as two files** — you signed off on the split. Keeps each file at a respectable token budget (~900 each) and lets `cheryl-hannah.md` be fetched independently for couple-dynamic conversations. Cost: a small amount of duplication on intergenerational threads where the couple-layer and family-of-origin layer meet.
- **EMDR prep as a separate tiny file** — deliberately small (400 tokens). Purpose: it's the only pointer to the private Worst Memories List, and keeping it separate means the pointer is obvious. Could merge into `cheryl-emdr.md` if you prefer a lighter file count.
- **Anger as a dedicated file** — you signed off on separate. Rationale: anger is a distinct clinical thread with its own log shape (incidents, triggers, resolution), and it's the most-frequently-fetched topic likely. Lives alongside `cheryl-patterns.md` which holds the broader pattern constellation.
- **Catarina file carries the therapist-pipeline history** — the Feb–March shortlist and ASGSF research. Could move to archive as "resolved," but kept warm because the ASGSF assessment action is still outstanding and Simon Arthur-Smith remains a live budget fallback if £70/week becomes unsustainable.

## Token budget summary

Live: 600. Warm (8 files): 8100 combined, but never all loaded at once — typical fetch will be live + 1–2 warm = ~2000 tokens. Archive and changelog: load on explicit request only. Total shape matches Dr Quinn closely.
