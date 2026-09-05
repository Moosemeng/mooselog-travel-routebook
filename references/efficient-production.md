# Efficient Production

Use this reference for every new journal and revision. The goal is to reduce waiting and image-generation retries without lowering the final quality bar.

## Default Pipeline

Use `balanced-fast` unless the user explicitly requests a rough preview or multiple art directions.

1. **Batch intake**: ask one compact group of missing questions. Reuse all answers already present in the thread.
2. **One research pass**: search official/current sources in batches, resolve feasibility, and stop once the route can be responsibly planned.
3. **Freeze content**: create one journal manifest with exact copy, map labels, page count, ratio, and author credit. For AI-planned trips, obtain route confirmation before artwork.
4. **Validate density cheaply**: for dense whole-trip or multi-page outputs, make a deterministic wireframe or calculate card/text bounds before image generation.
5. **Generate text-free art once**: create one base per approved page with blank text-safe cards and compact label pockets. Never ask the image model to render final Chinese body copy.
6. **Render text locally**: use bundled fonts and a reusable script to place all exact copy, labels, accents, and the author credit.
7. **QA once, repair narrowly**: inspect at full page and phone scale. Fix copy/layout locally. Regenerate only an artwork layer that truly fails.

## Project Bundle

When saving outputs, keep reusable stages together when practical:

```text
trip-journal/
  manifest.json or manifest.md
  sources.md                 # only when research was needed
  style-brief.md             # optional for multi-page consistency
  base/                      # text-free approved artwork
  render_journal.py          # deterministic typography/layout
  preview/                   # optional wireframe or pilot
  final/
```

Do not require every file for a tiny one-off image. The invariant is to preserve enough state that text revisions do not trigger image generation.

## Research Efficiency

- Search multiple related official questions in one batch rather than one stop at a time.
- Research critical constraints first: closures, reservations, schedules, transport, and route feasibility.
- Do not research decorative trivia until the itinerary is viable.
- Reuse sources already gathered in the same task. Recheck only facts that changed, are live, or are newly relevant.
- Keep recommendations concise and stop browsing when more sources would not change the route or journal copy.

## Multi-Page Efficiency

- Do not generate every page before the visual system is approved.
- Validate one representative pilot page or shared style brief first when the user has not approved the art direction.
- After approval, generate independent text-free page bases in parallel when tooling permits.
- Reuse palette, route treatment, paper system, icon language, typography scale, and label style across pages.
- Use one shared render helper and page-specific manifests rather than rewriting typography logic for every page.

## Preview Modes

### Quick Preview

Use when the user asks to see structure quickly or content is still changing.

- No expensive final illustration.
- Show zones, card sizes, text hierarchy, route order, and approximate landmark positions.
- Clearly call it a layout preview, not final artwork.

### Balanced Fast

Use by default.

- At most one normal artwork generation per approved page before QA.
- Permit one targeted artwork retry only when the base violates a hard requirement such as wrong composition, missing landmark system, unusable text zones, or incorrect visual identity.
- Typography corrections never consume the artwork retry.

### Studio

Use only when the user requests variants or explicitly wants maximum polish.

- Define the difference between variants before generation.
- Keep the selected base and discard no approved work during copy revisions.

## Revision Router

Determine the smallest invalid layer:

| User change | Action |
|---|---|
| Wording, date, time, price note | Update manifest and local render |
| Font size, card position, text contrast | Update local render |
| Map label name or route-line color | Update local render when separate; otherwise edit only map overlay |
| Author credit | Update local render |
| Replace one photo sticker | Replace that asset or local region |
| Add/remove a stop without changing overall geography | Update manifest and map overlay; preserve base if space allows |
| Route topology or destination changes | Regenerate affected base page |
| User rejects the entire visual style | Generate a new base after clarifying the new direction |

## Hard Efficiency Rules

- Never browse again merely to restate already verified information.
- Never regenerate a whole journal for a text overlap.
- Never generate final art before route/page-count confirmation in AI-planned mode.
- Never create multiple visual variants by default.
- Never serialize independent file reads, research queries, or page renders when they can run together.
- Do not sacrifice the typography, collision, source, or mobile-legibility quality gates for speed.
