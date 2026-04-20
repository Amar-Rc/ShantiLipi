# ShantiLipi শান্তিলিপি

Bengali font for Vedic text typesetting with full svara mark support.

## v1.4 Features

- Full Bengali Unicode coverage (95 codepoints)
- ba/va distinction: ৰ (U+09F0) for ব (ba), ব (U+09AC) for va
- 40+ conjuncts including ন্ত্র, স্ম, স্প, স্ফ, হ্ন
- 16 Vedic accent marks (udatta, anudatta, double svarita, etc.)
- Smart anudatta positioning (adjusts above/below matras)
- Em and en dashes

## Installation

- **Mac**: Double-click the .ttf → "Install Font"
- **Windows**: Right-click → "Install"
- **Linux**: Copy to `~/.fonts/` → `fc-cache -fv`

## XeLaTeX Usage

```latex
\usepackage{fontspec}
\setmainfont{ShantiLipi}
```

Type Vedic marks after base characters:
- ॑ U+0951 = udatta
- ॒ U+0952 = anudatta
- ᳚ U+1CDA = double svarita

## License

GNU GPL v3 with Font Exception. Based on GNU FreeSerif.
