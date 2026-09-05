---
name: mooselog-travel-routebook
description: "Plan trips with current research or transform an existing itinerary into Mooselog-style travel journal pages. Use for 小红书旅行手帐, AI 旅行规划, 国内旅行手帐, 中国风旅行攻略, illustrated map journals, citywalks, hiking journals, roadbooks, routebooks, and domestic or international travel guide pages. Supports either user-supplied routes or an AI-researched destination-and-duration brief, then produces destination-colored editorial notebook compositions with illustrated maps, schedules, practical cards, and checklists."
---

# Mooselog Travel Journal V2.6

Author: Mooselog

Create a design-rich travel journal page from the user's trip materials. Treat route information as one module inside a larger editorial notebook system, not as the entire product.

## Core Reframe

The product is **旅行手帐 / travel journal**, not merely 旅行路书 / routebook.

- Make a complete page that feels planned, collectible, and designed.
- Use the user's route, photos, map links, and notes as raw material for a journal spread.
- Let the page contain multiple information modules: title, date, weather, knowledge, goals, schedule, map, stop cards, photos, food, transport, tips, reservations, and checklist.
- Use photos as references, evidence stickers, or illustrated landmarks; do not build a dominant photo grid unless explicitly requested.
- Build strong composition first, then place content. Avoid filling boxes mechanically.

## First Response Workflow

When the user requests a travel journal, routebook, hand-drawn map, guide page, itinerary image, 小红书旅行手帐, 手帐式攻略, or similar:

1. Ask this routing question first unless the answer is already explicit: **你已经有完整行程，还是希望把目的地、天数和偏好交给 AI 检索规划？**
   - `existing-itinerary`: transform a supplied plan into a journal without silently redesigning the trip.
   - `ai-planned-trip`: research, propose, verify, and confirm an itinerary before journal production.
2. Determine trip type: domestic China or international.
3. Ask whether the journal covers the **whole trip** or a **single day**. Do not infer this when the user has not stated it.
4. Ask whether the user wants an author credit. If yes, collect the exact display name; if no, omit it.
5. Determine output format: one page for a whole trip, one page per day, cover + daily pages, or long-scroll journal.
6. Determine journal mode:
   - **Notebook guide**: schedule + map + tips; best for useful social posts.
   - **Illustrated map journal**: map panel dominates; best for citywalk or one-day trips.
   - **Photo-memory journal**: photos and notes dominate; best for emotional travel record.
   - **Hiking field journal**: route difficulty, equipment, reservation, and terrain notes dominate.
7. Determine style:
   - Use `travel-journal` as the default for hand-drawn notebook reference images.
   - Use other presets only when the user asks for a specific art direction.
8. Collect only missing inputs that materially affect the output.

Use `balanced-fast` production by default. Do not ask the user to choose a speed mode unless they explicitly care about speed, variants, or maximum polish. Read [references/efficient-production.md](references/efficient-production.md) before starting research, generating artwork, or revising an existing journal.

For `ai-planned-trip`, read [references/ai-trip-planning.md](references/ai-trip-planning.md) before asking detailed questions or researching. Do not start image generation until the user has seen and accepted the itinerary draft, unless they explicitly ask the skill to make every decision and proceed autonomously.

## Two Product Modes

### Existing Itinerary

- Preserve the user's route order, booked items, dates, notes, and supplied photo-to-stop mapping.
- Research only missing context or facts the user asks to enrich.
- Flag obvious feasibility or closure problems, but do not silently replace booked plans.
- Convert the approved source material into the journal manifest and composition workflow below.

### AI-Planned Trip

- Start from destination, duration, dates or season, departure point, traveler profile, interests, pace, transport preference, and budget band.
- Browse current primary or official sources for opening periods, closures, reservation requirements, transport feasibility, park rules, and other time-sensitive constraints.
- Create a day-by-day route with geographic clustering, realistic transit buffers, meal/rest space, weather fallback ideas, and a short reason for each stop.
- Distinguish verified facts from recommendations and estimates. Never invent exact prices, timetables, availability, coordinates, or weather.
- Present a concise itinerary draft before artwork. Ask for one confirmation covering route and major tradeoffs; then continue directly into journal production.
- After confirmation, the AI-planned route becomes the source itinerary and follows the same visual, typography, composition, and quality rules as `existing-itinerary`.

## Production Speed Modes

- `quick-preview`: build a deterministic wireframe or typography-first preview without final illustration. Use for validating content density, page count, and layout direction.
- `balanced-fast` (default): freeze content, generate one text-free artwork base per approved page, add all typography deterministically, and run one visual QA pass.
- `studio`: allow one or two art-direction variants or additional illustration refinement when the user explicitly prioritizes exploration over speed.

Never use repeated full-image generation to fix copy, fonts, labels, card padding, or minor spacing. Re-render those changes locally on the approved base artwork.

After identifying the trip type, branch immediately:

- For `domestic-china`, read [references/china-travel-visual-system.md](references/china-travel-visual-system.md) and treat it as the flagship design path.
- For `international`, use destination-local visual evidence and the international identity rules in this file. Do not reuse a generic European notebook treatment.
- For both paths, read [references/adaptive-color-system.md](references/adaptive-color-system.md) before choosing any background, paper, card, map, or route color.

Read [references/input-brief.md](references/input-brief.md) when collecting materials. Read [references/travel-journal-system.md](references/travel-journal-system.md) before creating any hand-drawn notebook, travel journal, or reference-image-inspired page. Read [references/typography.md](references/typography.md) before producing any image that contains text. Read [references/style-presets.md](references/style-presets.md) before choosing a secondary style. Read [references/quality-gate.md](references/quality-gate.md) before final delivery.

## Domestic And International Branches

Do not treat domestic and international journals as one template with only a flag difference.

### Domestic China

- Make domestic China the most culturally specific and design-rich default path.
- Select a Chinese page architecture and regional visual dialect from [references/china-travel-visual-system.md](references/china-travel-visual-system.md).
- Use Chinese elements as composition, map grammar, title structure, paper treatment, and information hierarchy, not as random decorative stickers.
- Require destination-specific evidence and avoid generic antique-yellow "Chinese style".
- Omit the country flag by default.

### International

- Derive the visual language from the destination's own landscape, architecture, print culture, transport, and season.
- Use the destination-country flag quietly unless the user opts out.
- Avoid applying Chinese motifs to international trips unless the user explicitly requests a cross-cultural treatment.

## Default Style Menu

Offer these presets by default:

1. `travel-journal` - design-rich notebook travel journal with title, schedule, illustrated map, cards, lists, and tips.
2. `illustrated-map-journal` - map-forward journal spread with large hand-drawn route map and stop callouts.
3. `hiking-field-journal` - trail-focused page with map, distance, duration, difficulty, gear, reservation, and safety notes.
4. `photo-memory-journal` - scrapbook-like travel memory page with stronger photo presence.
5. `minimal-guide-card` - cleaner guide card when legibility is more important than decoration.
6. `gathered-zine` - artful photo-and-paper collage when the user wants an editorial poster.
7. `vintage-postcard` - nostalgic postcard/archive travel page.
8. `watercolor-travel` - soft illustrated travel page.

The old `handbook-map`, `sticker-journal`, `cute-comic`, and `minimal-map` labels remain valid aliases, but map them into the V2.0 journal system:

- `handbook-map` -> `travel-journal` or `illustrated-map-journal`
- `sticker-journal` -> `photo-memory-journal`
- `cute-comic` -> `travel-journal` with cute stickers and rounded illustration
- `minimal-map` -> `minimal-guide-card`

## Input Contract

Represent the user's materials as a journal manifest:

```text
Planning source: existing-itinerary | ai-planned-trip
Trip type: domestic-china | international
Trip scope: whole-trip | single-day
Author credit: none | exact display name
Output format: one-page | one-page-per-day | cover-plus-days | long-scroll
Journal mode: notebook-guide | illustrated-map-journal | photo-memory-journal | hiking-field-journal
Platform/ratio: xiaohongshu-3:4 | instagram-4:5 | vertical-3:5 | square-1:1 | custom
Style: travel-journal | illustrated-map-journal | hiking-field-journal | photo-memory-journal | custom
Title:
Date/day label:
Language:
Weather:
Knowledge card:
Today goals:
Food/check-in list:
Transport guide:
Tips:
Map links / coordinates:

AI planning preferences (ai-planned-trip only):
  Destination or candidate region:
  Departure point:
  Dates/season and number of days:
  Travelers and mobility constraints:
  Interests and must-do items:
  Pace: relaxed | balanced | intensive
  Transport preference:
  Budget band:
  Lodging status or preferred bases:
  Avoidances / dietary needs:

Stops:
  1. time:
     name:
     photo:
     map link or coordinate:
     action/reason:
     transport:
     tags:
     reservation/cost:
     note:
```

For international trips, accept Google Maps links, coordinates, copied pins, or route notes. If exact coordinates are missing, build a symbolic illustrated map and label it as a designed journal map, not turn-by-turn navigation.

For domestic China trips, accept Gaode/Baidu/Apple/Google links. When no coordinates are supplied, build a narrative hand-drawn map using route order and user notes.

## Composition Workflow

1. Extract content atoms once and freeze them in a journal manifest: title, date, stops, times, route, map links, photos, facts, tips, warnings, food, transport, goals, and checklist items.
2. Choose the page architecture before generating artwork. For dense or multi-page work, create a fast typography-first wireframe or one representative pilot page.
3. Generate the illustration layer without readable text. Reserve explicit quiet rectangles for every text module and compact label pocket.
4. Add titles, labels, body copy, and author credit with bundled fonts in a deterministic local render layer.
5. Run collision, glyph, dimensions, and mobile-legibility checks. Fix typography locally; regenerate artwork only when the illustration itself is wrong.

Recommended architecture components:
   - Header strip or torn paper title block.
   - Info card row.
   - Schedule/timeline column.
   - Illustrated map panel.
   - Stop callouts.
   - Bottom utility cards.
   - Optional footer note.
6. Assign visual hierarchy:
   - Title and day marker are the entry point.
   - Map panel carries movement.
   - Timeline carries exact order.
   - Cards carry practical context.
   - Photos/illustrations support place identity.
7. Convert photos into small framed evidence cards, cutout stickers, or simplified landmarks. Use at most 1-3 dominant photo/illustration moments per page.
8. Use a designed map field: pale map texture, schematic streets/trails, dotted route line, arrows, pins, and labels.
9. Use a coherent sticker/icon system. Icons must communicate real content, not decorate randomly.
10. Use varied card sizes and alignments. Avoid a rigid equal-card grid unless the user asks for a clean template.
11. Check mobile legibility and thumbnail hierarchy before final delivery.

## Classic Split Layout Contract

When the user asks for a left-right notebook layout, treat the split as a hard content boundary rather than a loose visual suggestion.

- Use roughly 42-48% of the page for the left information column and 52-58% for the right map column.
- Keep the complete information system on the left: title/date, weather, local knowledge, key information, itinerary grouped by day, wish/check-in list, and transport guide.
- Keep the right side map-only: illustrated terrain, route line, arrows, numbered pins, landmark illustrations, and short stop labels.
- Do not place utility cards, long paragraphs, checklists, or photo frames inside the map column.
- Do not let any landmark illustration, route segment, flag, or decorative mark enter a text-safe rectangle.
- Use an explicit collision pass: every text block must have an opaque or sufficiently quiet background and at least 12 px of internal breathing room at Xiaohongshu 1242 x 1656 scale.
- When the illustrated map already contains quiet paper label pockets, write directly into those pockets instead of drawing larger overlay cards.
- Default map labels to only the Chinese and/or English place name. Add times, notes, or tags only when the user explicitly requests them.
- Keep map label fills and borders close to the map paper color. Use one restrained border/route color unless multiple colors carry necessary route meaning.

## Editable Content Loop

Keep content separate from layout so the user can repeatedly refine individual modules without rebuilding the visual system.

- Store title, weather, knowledge, key information, day itineraries, wish list, transport guide, and map labels as editable content fields.
- After a draft, accept targeted changes such as "只改天气卡", "压缩 Day 2", or "替换愿望清单第 3 项".
- Preserve approved layout, palette, map artwork, and typography when only content changes.
- Reflow and collision-check the changed module before export.
- Classify every revision before acting:
  - Copy, font, label, card, spacing, author, or color-token change -> deterministic re-render only.
  - One landmark or local map-region change -> edit or regenerate only that artwork region when possible.
  - New visual direction, changed route topology, or unusable base artwork -> regenerate the affected base page.
- Keep approved base artwork and render scripts. Never discard them merely because the final PNG needs a content update.

## Palette Coupling

Sample the left information palette from the illustrated map.

- Derive card fills, border swatches, day tabs, and checklist accents from terrain gray, alpine green, lake blue, muted ochre, and paper beige.
- Use low-chroma tints for card fills and slightly darker versions for borders.
- Keep the route and map labels visually restrained; avoid assigning every stop a different saturated color.

## Adaptive Destination Color

- Never use sand, cream, sepia, kraft, or vintage beige as an automatic journal background.
- Derive the page ground and palette from user photos first, then destination landscape, season, weather, architecture, and time of day.
- Use tactile grain on any hue; paper texture does not require yellow paper.
- For example, use alpine green and limestone gray for summer Dolomites, not desert beige; use poplar gold, canyon red, and lake blue for autumn Ejina.
- Follow [references/adaptive-color-system.md](references/adaptive-color-system.md) and document the palette rationale internally before rendering.

## Controlled Asymmetry

When the map side is richly hand-drawn, keep the information side structured but not mechanically aligned.

- Stagger small cards by 4-16 px, vary card heights, and allow subtle rotations around 0.5-1.5 degrees.
- Use tape, clipped notes, layered paper edges, watercolor swatches, and offset day tabs to create notebook rhythm.
- Keep one stable structural anchor, usually the itinerary panel, while smaller support modules behave like collected paper notes.
- Preserve text baselines, internal padding, and collision safety. "Slightly messy" must not mean overlapping copy or reduced readability.
- Avoid three equal cards aligned to one rigid row when a hand-made journal effect is requested.

## Author Credit

Ask whether the user wants an author credit on every new journal unless the answer is already known.

- If yes, use the exact display name supplied by the user.
- Place the credit quietly in the lower-right corner by default, such as `Journal by <name>` or the requested wording.
- Use a small paper strip, pencil underline, stamp, or low-contrast signature treatment.
- Do not infer an author name from the skill author or account name.
- If the user says no, omit the credit completely.

## Complex Hand-Drawn Standard

"Complex hand-drawn" means semantic illustration, not merely jittered borders or wobbly lines.

- Transform reference photos into recognizable watercolor, colored-pencil, ink, or gouache landmark illustrations.
- Replace photographic lighting and pixel detail with simplified shapes, layered washes, pencil hatching, and selective ink contours.
- A realistic photo with a hand-drawn frame does not satisfy this mode.
- Build a coherent illustrated landscape system across all stops: mountains, vegetation, architecture, transport, water, and terrain marks must share one medium and palette.
- Generate or draw map artwork without text first, then add route labels in a separate deterministic layout layer.
- Keep each landmark in its own visual island and reserve dedicated label pockets beside it. Never place text directly over high-detail imagery.

## International Identity Marker

For international trips, include the destination country's flag unless the user opts out.

- Prefer a low-opacity flag watermark or paper wash in the upper-right map area.
- Keep opacity around 6-14% so the flag reads as provenance, not branding.
- Place the flag behind map artwork and outside primary label contrast zones.
- Do not add an author mark unless the user confirms it in the author-credit question.

## Design Direction From Reference

When the user provides a notebook-map reference like the Kawagoe example, learn the structure rather than copying the subject:

- Split the page into an information half and a route-map half.
- Use a bold hand-lettered title area with day/date tags.
- Use compact top cards for weather, knowledge, and goals.
- Use a vertical schedule with colored numbered markers.
- Use a large hand-drawn map area with colored dotted route paths, arrows, pins, stop cards, and local landmarks.
- Use bottom cards for food, check-in list, transport guide, and tips.
- Keep the page dense but charming: every module should have a purpose.
- Prefer watercolor, colored-pencil, ink outlines, paper grain, tape, folds, stamps, small icons, and notebook binding details.

## Output Defaults

Return final images when image generation or visual tooling is available. Otherwise return a production-ready prompt plus a clean journal manifest.

By default, include:

- the final image or prompt;
- a concise rationale in Chinese when the user is speaking Chinese;
- any important uncertainty, such as unverified weather, exact prices, reservations, or opening times.

Do not include a long prompt unless the user asks. Add an image credit only when the user confirms it. Keep skill authorship visible here: **Mooselog Travel Journal by Mooselog**.

## Hard Avoids

Avoid treating the page as a photo collage, oversized photo grids, generic stickers unrelated to the itinerary, raw map screenshots pasted as design, rigid equal boxes, flat dashboard aesthetics, tiny unreadable text, fake exact map precision, invented coordinates/prices/opening times, decoration that does not carry information, route pins without a matching schedule, photographic landmark cards in complex-hand-drawn mode, text placed directly on detailed imagery, map illustrations that cross label or callout safe zones, one sand-colored background for every destination, domestic pages that merely remove the international flag, generic antique-yellow Chinese styling, random dragons/lanterns/clouds/seals, and culturally inaccurate or mixed regional motifs.
