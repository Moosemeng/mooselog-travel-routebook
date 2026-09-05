# Typography

Use this reference before producing any travel-journal image containing text.

## Bundled Font

Use only the bundled Noto Sans SC files for Chinese and Latin text:

- `assets/fonts/NotoSansSC-Regular.ttf`
- `assets/fonts/NotoSansSC-Bold.ttf`

For a cute rounded Latin map title or small decorative Latin display text, use:

- `assets/fonts/Fredoka-SemiBold.ttf`

The accompanying `assets/fonts/OFL-NotoSansSC.txt` is the SIL Open Font License 1.1 from the official Google Fonts Noto Sans SC package. Preserve the license whenever redistributing the font files.

The accompanying `assets/fonts/OFL-Fredoka.txt` is the SIL Open Font License 1.1 from the official Google Fonts Fredoka package. Preserve it whenever redistributing Fredoka.

## Rules

- Resolve font paths relative to the skill directory; do not depend on macOS, Windows, or Linux system fonts.
- Use Bold for titles, day tabs, section labels, and map labels. Use Regular for body text, times, subtitles, and notes.
- Use Noto Sans SC for all Chinese, body copy, times, labels, and mixed-language strings.
- Use Fredoka only for short Latin display text such as `DOLOMITES MAP`; do not use it as a Chinese fallback.
- Verify every requested glyph renders. Treat missing-glyph squares as a blocking export failure.
- Do not describe a font as commercially usable without a bundled license or an authoritative license source.
- The OFL permits use and embedding in commercial outputs subject to its terms; this instruction is operational guidance, not legal advice.
