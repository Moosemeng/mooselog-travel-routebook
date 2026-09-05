# Mooselog Travel Routebook

`mooselog-travel-routebook` is an open-source Codex skill for planning trips and turning itineraries into design-rich travel journal pages, illustrated route maps, and Xiaohongshu-ready guides.

Created and maintained by **Mooselog**.

## Features

- Two workflows: transform an existing itinerary or let AI research and plan a trip.
- Distinct visual systems for domestic China and international travel.
- Whole-trip, single-day, daily-page, cover-plus-days, and long-scroll formats.
- Destination-derived palettes instead of a fixed vintage-paper color.
- Illustrated map, notebook guide, hiking journal, and photo-memory modes.
- A fast production pipeline that separates text-free artwork from deterministic typography.
- Mobile-legibility and collision checks for social-media exports.
- Bundled commercially usable fonts with their original licenses.

## Install

Clone the repository into your Codex skills directory:

```bash
git clone https://github.com/Moosemeng/mooselog-travel-routebook.git \
  ~/.codex/skills/mooselog-travel-routebook
```

Restart Codex if the skill is not discovered immediately. Invoke it with:

```text
$mooselog-travel-routebook
```

You can also ask naturally, for example:

```text
帮我把这份杭州三日行程做成一张小红书3:4旅行手帐。
```

## How It Works

The skill first asks whether you already have an itinerary or want AI to research one. It then collects only the missing trip scope, format, style, route, author credit, and practical information.

Its default `balanced-fast` workflow freezes the approved content, generates one text-free illustration base, adds exact copy with bundled fonts, and performs a visual quality check. Copy and layout revisions can therefore be rendered locally without regenerating the artwork.

## Repository Structure

```text
mooselog-travel-routebook/
|-- SKILL.md
|-- agents/openai.yaml
|-- references/
`-- assets/fonts/
```

## Fonts

The bundled font files are distributed under the SIL Open Font License 1.1:

- Fredoka SemiBold: see `assets/fonts/OFL-Fredoka.txt`
- Noto Sans SC Regular/Bold: see `assets/fonts/OFL-NotoSansSC.txt`

The skill instructions and other original repository content are licensed under MIT. The font files remain under their respective SIL OFL terms.

## Contributing

Issues and pull requests are welcome. When proposing a visual-system change, include the destination type, page ratio, expected information density, and a description of the layout problem it solves. Do not submit private travel photos, personal map history, booking details, or third-party assets without redistribution rights.

## License

Copyright (c) 2026 Mooselog. Released under the [MIT License](LICENSE), except for bundled fonts covered by their accompanying SIL OFL license files.
