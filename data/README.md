# The Playfield dataset

The course's shared dataset: a fictional indie-game storefront. **All 20 games,
300 reviews, and docs are invented** — no real games, studios, or people. (That's
deliberate: it makes the Day-1 hallucination demo work, avoids licensing issues,
and lets the course control what's discoverable in the data.)

## Files

### `games.csv` — the catalog (20 rows)

| column | type | notes |
|--------|------|-------|
| `game_id` | str | `g01`…`g20`, joins to reviews and docs |
| `title` | str | |
| `genre` | str | |
| `price_eur` | float | `0.00` = free-to-play |
| `release_year` | int | 2022–2026 |
| `developer` | str | fictional studio |

### `reviews.csv` — player reviews (300 rows, 15 per game)

| column | type | notes |
|--------|------|-------|
| `review_id` | str | `r001`…`r300` |
| `game_id` | str | FK → `games.csv` |
| `author` | str | fictional handle |
| `hours_played` | float | correlated with tone |
| `recommended` | bool | the "thumb" — sometimes contradicts the text 🙃 |
| `helpful_votes` | int | |
| `date` | str | `YYYY-MM-DD`, consistent with release years and patch timelines |
| `review_text` | str | messy on purpose: typos, slang, Pros/Cons layouts, sarcasm, a few Romanian reviews (without diacritics, as nature intended) |

### `docs/` — the Day-3 RAG corpus (40 markdown files)

Per game: `gNN-description.md` (store page: pitch, features, system requirements)
and `gNN-patch-notes.md` (dated, versioned entries, newest first). Patch notes are
**timeline-consistent with the reviews** — complaints predate fixes, and post-fix
reviews reference them — so questions like *"did they fix the save bug?"* have
real answers.

### `shards/` — generation source

`reviews.csv` is built from these JSONL shards by `python tools/build_dataset.py`
(validates schema and timelines, shuffles deterministically, assigns ids).
Edit shards → re-run the script. Don't edit `reviews.csv` directly.

## For instructors

The per-game complaint clusters are *designed*, with varied wording so semantic
search must work by meaning. The answer key lives in
`instructor/dataset-ground-truth.md` — it doubles as the Day-5 eval seed.
