# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

Content project (not application code) for the **Keep Moving Forward (KMF)** book series — short motivational "tagline" entries (title + short body + expanded story) grouped into 8 category books, plus tooling to generate social-media quote images from that content. The only executable code is three Python scripts in `scripts/`.

## Commands

Python 3 with Pillow (`PIL`) is required for image generation; no `requirements.txt` — install with `pip install Pillow` if missing.

```bash
# Generate one social image (1080x1080 PNG)
python3 scripts/generate_social_image.py --tagline "Done Beats Perfect" --body "..." \
  --template 1 --scheme dark --category motivation --out-dir KMF-motivate/tagline-images --prefix "01"

# Batch-generate all images for one book (parses that book's new-taglines-{category}.md)
python3 scripts/batch_tagline_images.py --book focus
python3 scripts/batch_tagline_images.py --book focus --skip-existing   # only fill in missing PNGs

# Batch-generate for every KMF book (not the master archive)
python3 scripts/batch_tagline_images.py --all

# Generate for the master archive file instead of a per-book file
python3 scripts/batch_tagline_images.py --book master

# QA check the legacy 101-entry Motivation book layout
python3 scripts/verify_motivation_book.py
```

`--template` is 1–3 (border style) and `--scheme` is `light` / `dark` / `tan`; both are randomized per entry when omitted.

There is no build, lint, or test suite beyond `verify_motivation_book.py` — that script only validates `new-taglines/motivation/new-taglines-motivation.md` and its story files (a legacy layout; see below), not the current per-book KMF-* folders.

## Content architecture

### Two content layers, one entry

Every idea in this project exists at two levels, kept in sync by number:

| Layer | Where | Contains |
|-------|-------|----------|
| **Short entry** | `KMF-{category}/new-taglines-{category}.md` | `## NN. Title - category`, italic *Tagline* (3–6 words), 1–2 sentence body |
| **Expanded story** | `KMF-{category}/taglines-stories/NN-slug.md` | Same title/tagline/body, plus `## Category`, `## Theme`, `## The idea`, `## Story` (150–300 words), `## Takeaway` |

The master cross-book archive lives at `new-taglines/new-taglines.md` (all entries) with its own `new-taglines/taglines-stories/` flat copy. When adding or editing an entry, **update the master archive and the category book together** — they must stay in sync.

Rendered social images (1080×1080 PNGs, named `NN-slug.png`) live in each book's `tagline-images/` folder, generated from the short entry file by `scripts/batch_tagline_images.py`.

### Category vs Theme — do not conflate

- **Category** = which book (shelf): `motivation`, `discipline`, `resilience`, `ownership`, `growth`, `mindset`, `peace`, `focus` (slug on the entry heading and `## Category` in the story file). One category per entry, answering that book's fixed reader question (e.g. motivation → "How do I get started when I don't feel like it?").
- **Theme** = which chapter *inside* that book — a narrower lens on the same reader question (e.g. Motivation's themes: Beat Perfection, Shrink The Start, Move Through Fear, Act Before Ready, Build Momentum). Recorded in `## Theme` in the story file and as `<!-- theme: ... -->` / chapter headers in the book's markdown file.

Full category→theme tables and the PAR/CAR (Problem/Challenge → Action → Result) copywriting method are documented in `new-taglines/newtagline-instructions.md`; the long-form story rules (section-by-section format, the 12 "story shapes" to rotate through, length targets, legal/originality rules) are in `new-taglines/taglines-stories-instructions.md`. **Read those two files before writing or editing taglines, bodies, or stories** — they are the style guide, not just reference.

### Known layout quirk

The instructions docs describe entries living under `new-taglines/{category}/`, but in practice each book's live files are at the **repo root** as `KMF-{category}/` (e.g. `KMF-motivate/`, `KMF-peace/`). `new-taglines/motivation/` is an empty leftover from the earlier nested layout — treat `KMF-*/` at the root as the current source of truth for per-book content, and `new-taglines/new-taglines.md` as the cross-book master.

### Other reference material

- `real-life.md` — bank of real/composite personal-experience story material, tagged by life domain and mapped to the (legacy) Motivation chapter numbering, to pull from when writing a `## Story` section.
- `start-moving-story-pilot.md` — worked example assigning distinct story shapes to Chapter 1 entries; use as a model when varying story structure across a chapter.
- `motivation-book-101-outline.md` — historical outline/merge log for an earlier 101-entry single-book version of Motivation (superseded by the ~12–13-entries-per-book, 8-category structure above, but kept for the merge/reframe decisions it documents).
- `100waystaglines/` — earlier, unrelated 100-chapter tagline draft (pre-KMF structure).
- `frame-samples/` — sample renders of the border **templates** used by `generate_social_image.py`, for visually picking a style.

## Workflow when adding a new tagline

1. Add the short entry to `new-taglines/new-taglines.md` (master archive).
2. Add the same entry to `KMF-{category}/new-taglines-{category}.md` under the correct theme chapter.
3. Create the expanded story in `KMF-{category}/taglines-stories/NN-slug.md` following the section layout in `taglines-stories-instructions.md` (pick a story shape not used in the adjacent entry).
4. Generate the social image with `scripts/generate_social_image.py` or `scripts/batch_tagline_images.py --book {category}`.
5. No author name, book title, or chapter-source references belong in any public-facing content (tagline, body, story) — see the "Legal / originality" section of `newtagline-instructions.md`.
