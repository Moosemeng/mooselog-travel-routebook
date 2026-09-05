# Input Brief

Use this reference when collecting materials for a Mooselog travel journal.

## Minimal Questions

Ask the fewest questions needed to start:

1. Do you already have a complete itinerary, or should AI research and plan it from the destination, duration, and preferences?
2. Is this a domestic China trip or an international trip?
3. Should the journal cover the whole trip or one specific day? Ask this explicitly unless the user has already answered it.
4. Should the image show an author credit? If yes, what exact display name should be used?
5. Should the output be one page for the trip, one page per day, a cover plus daily pages, or a long-scroll journal?
6. For an existing itinerary: what is the ordered itinerary, and which photos belong to which stop or day?
7. For AI planning: what are the destination, departure point, dates/season, days, traveler profile, interests, pace, transport, budget, and booked lodging constraints?
8. What platform or ratio is needed, and should Mooselog recommend the journal mode?

## Journal Inputs

Required:

- Trip title or working title.
- Day labels or route sections.
- Stop names and route order.
- Photos, sketches, screenshots, or visual references.
- Map links, coordinates, or a rough route description.

Strongly recommended:

- Date or season.
- Time range for each stop.
- Transport between stops.
- Weather or weather placeholder.
- Goals checklist.
- Food list, photo checklist, packing list, or reservation checklist.
- Practical tips, warnings, tickets, parking, opening hours, or booking notes.
- Desired tone: cute, elegant, vintage, field journal, playful, minimal, dense guide, etc.
- For domestic China: local region, season, and any verified cultural or craft references the user wants emphasized or avoided.

## Domestic China Trips

Accept Gaode, Baidu, Apple Maps, Google Maps, screenshots, place names, or coordinates. If exact coordinates are missing, build a symbolic journal map and avoid claiming turn-by-turn accuracy.

Do not ask the user to design the Chinese visual language from scratch. Recommend a regional visual dialect from the destination and let the user override it. Ask a cultural clarification only when a specific religious, ethnic, heritage, official, or politically sensitive symbol would materially affect the output.

## International Trips

Accept Google Maps links, copied pins, place names, coordinates, or user-written route order. If map links exist, include them as small map/pin cards, QR placeholders, or source notes inside the journal page.

## Journal Manifest Template

```text
Planning source: existing-itinerary | ai-planned-trip
Trip type:
Trip scope: whole-trip | single-day
Author credit: none | exact display name
Output format:
Journal mode:
Platform/ratio:
Title:
Date/day labels:
Language:
Tone:
Weather:
Knowledge/info cards:
Goals/checklist:
Food/check-in list:
Transport guide:
Tips:
Map links / coordinates:

Days:
1. Day label:
   Theme:
   Hero visual:
   Stops:
     1. Time:
        Name:
        Photo:
        Map link/coordinate:
        Action/reason:
        Transport:
        Tags:
        Reservation/cost:
        Note:
```

## Platform Ratios

- Xiaohongshu single page: 3:4 vertical by default.
- Xiaohongshu carousel: one 3:4 page per day or section.
- Xiaohongshu long image: tall vertical, use only when the user asks for long-scroll.
- Instagram feed: 4:5 vertical.
- Instagram story/Reels cover: 9:16 vertical.
- Poster/zine: 3:5 vertical.
- Square summary: 1:1.

When unknown and the user writes Chinese, use Xiaohongshu 3:4 vertical.

## Missing Information Rules

- Do not invent exact weather, prices, opening hours, booking windows, coordinates, or transport schedules.
- Use placeholders or "出发前确认" when exact details are unavailable.
- If the user asks Codex to research, browse current official sources for time-sensitive facts.
- If only photos are supplied, infer visual mood and ask for stop names/order before making a guide-heavy page.
