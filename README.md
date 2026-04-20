# ShantiLipi শান্তিলিপি

A Bengali font designed for **Vedic text typesetting** with full svara (accent) mark support.

## Features

- **Full Bengali Unicode coverage** — 95 Bengali codepoints, 1925 glyphs total
- **ba/va distinction** — ৰ (U+09F0) for ब (ba) vs ব (U+09AC) for व (va), critical for Sanskrit-in-Bengali
- **40+ conjuncts** via OpenType GSUB — ত্র, ক্ষ, ব্র, ন্দ্র, স্ব, জ্ঞ, হ্ন, and more
- **16 Vedic accent marks** including:
  - **Udatta** (U+0951) — single vertical stroke above matra line
  - **Anudatta** (U+0952) — horizontal stroke below baseline
  - **Double Svarita** (U+1CDA) — double vertical stroke above matra line
  - Karshana, Shara, Prenkha, Triple Svarita, and more
- **Matra-aware accent positioning** — udatta clears ি ী ৈ ৌ above; anudatta clears ু ূ ৃ and র-phala below
- **Em dash (—) and en dash (–)** included
- **Installable** on Mac, Windows, Linux

## The ব/ৰ Distinction

In traditional Sanskrit-in-Bengali typesetting, ब (ba) and व (va) are distinct phonemes:

| Glyph | Unicode | Represents | Sanskrit | Example |
|-------|---------|-----------|----------|---------|
| ব | U+09AC | va (व) | varuna | বরুণ (varuṇa) |
| ৰ | U+09F0 | ba (ब) | brahma | ৰ্রহ্ম (brahma) |

ৰ forms conjuncts identically to ব — so ৰ্র renders the same conjunct shape as ব্র.

## Installation

**Mac**: Double-click `ShantiLipi-Regular.ttf` → Click "Install Font"

**Windows**: Right-click `ShantiLipi-Regular.ttf` → "Install" or "Install for all users"

**Linux**: Copy to `~/.fonts/` or `/usr/share/fonts/truetype/shantilipi/` then run `fc-cache -fv`

## Features

- Full Bengali Unicode coverage (95 codepoints)
- ba/va distinction: ৰ (U+09F0) for ব (ba), ব (U+09AC) for va
- 40+ conjuncts including ন্ত্র, স্ম, স্প, স্ফ, হ্ন
- 16 Vedic accent marks (udatta, anudatta, double svarita, etc.)
- Smart anudatta positioning (adjusts above/below matras)
- Em and en dashes

## Usage with XeLaTeX

```latex
\documentclass{article}
\usepackage{fontspec}
\usepackage{polyglossia}
\setdefaultlanguage{bengali}
\setmainfont{ShantiLipi}

\begin{document}

% ব = va (व), ৰ = ba (ब)
ওঁ শং নো মিত্রঃ শং বরুণঃ।
ইন্দ্রো ৰৃহস্পতিঃ।
নমো ৰ্রহ্মণে।

% Vedic marks — place after the base character:
% U+0951 ॑ = udatta
% U+0952 ॒ = anudatta
% U+1CDA ᳚ = double svarita

শ॑ং নো॑ মি॑ত্রঃ    % udatta on শ, নো, মি
ন॒মো               % anudatta on ন

\end{document}
```

## Typing Special Characters

| Character | Unicode | Mac (Hex Input) | Windows | Purpose |
|-----------|---------|-----------------|---------|---------|
| ৰ | U+09F0 | Opt+09F0 | 09F0 Alt+X | ba (ब) |
| ॑ | U+0951 | Opt+0951 | 0951 Alt+X | udatta |
| ॒ | U+0952 | Opt+0952 | 0952 Alt+X | anudatta |
| ᳚ | U+1CDA | Opt+1CDA | 1CDA Alt+X | double svarita |

## Vedic Accent Marks

| Mark | Unicode | Position | Description |
|------|---------|----------|-------------|
| ॑ | U+0951 | Above | Udatta — single vertical stroke above matra line |
| ॒ | U+0952 | Below | Anudatta — horizontal stroke below baseline |
| ᳚ | U+1CDA | Above | Double Svarita — two vertical strokes above matra line |

Plus 13 additional Vedic tone marks from the Unicode Vedic Extensions block (U+1CD0–U+1CFF).

## Technical Details

| Property | Value |
|----------|-------|
| Font format | TrueType (.ttf) |
| Version | 1.2 |
| Glyphs | 1925 |
| Bengali codepoints | 95 |
| Vedic marks | 16 |
| GSUB features | akhn, blwf, blws, cjct, half, hlig, pref, pres, pstf, psts, rphf |
| GPOS features | blwm, dist, kern, mark, mkmk |
| File size | ~449 KB |

## License

ShantiLipi is derived from [GNU FreeSerif](https://www.gnu.org/software/freefont/) and is released under the **GNU General Public License v3** with the **Font Exception**.

- You can **freely use** this font in any document
- You can **distribute** documents using this font without the GPL applying to the document
- If you **modify the font itself**, you must release modifications under the same GPL license
- See [LICENSE](LICENSE) for full terms

## Credits

- **Base font**: GNU FreeSerif by Primoz Peterlin, Steve White, and contributors
- **Vedic modifications**: ShantiLipi Project

## Contributing

Contributions welcome! Areas that could use help:
- Refining glyph outlines to match traditional woodblock/letterpress Bengali aesthetic
- Testing across different rendering engines and platforms
- Hinting for better screen rendering at small sizes
- Building an OFL-licensed version (using Noto Sans Bengali base) for Google Fonts submission

