# Changelog

## v1.2 (2026-04-04)

### Fixes
- Fixed ৰ্র conjunct: removed asamira_bng from rphf (repha) lookup so ৰ forms ba-conjuncts, not repha
- Fixed হ্ন conjunct: added lookup 83 to psts feature for Bengali script
- Fixed ষ্য, দ্য, শ্য, স্য, ন্য, হ্য: removed all _ya_trad ligatures for standard Bengali য-phala rendering
- Fixed anudatta positioning: added anudattadeva to MarkToBase lookup 11 for proper positioning on Bengali consonant bases and conjuncts
- Fixed anudatta under র-phala: adjusted Mark1 anchor for proper clearance
- Conditional anudatta y-positioning: deeper when below-base matras (ু ূ ৃ) are present
- Added em dash (U+2014) and en dash (U+2013) from FreeSerif source

### Improvements
- Udatta and double svarita scaled 1.8x wider + 1.4x taller for better visibility
- Anudatta thickened for better visibility
- Udatta x-position tuned to -358 for optimal centering
- GPOS mark anchors raised to y=920 to clear ি ী ৈ ৌ matras above
- Line metrics increased (ascent: 1600, descent: -500) for Vedic mark headroom

## v1.0 (2026-03-30)

### Features
- Full Bengali Unicode coverage (95 codepoints, 1925 glyphs)
- ba/va distinction: ৰ (U+09F0) for ba (ब), ব (U+09AC) for va (व)
- ৰ forms identical conjuncts to ব via cloned GSUB rules
- 40+ conjuncts via OpenType GSUB (akhn, blwf, blws, cjct, half, pref, pres, pstf, psts, rphf)
- 16 Vedic accent marks including udatta (U+0951), anudatta (U+0952), double svarita (U+1CDA)
- GPOS mark positioning (mark, mkmk, blwm, dist, kern)
- Based on GNU FreeSerif, licensed GPL v3 with Font Exception
