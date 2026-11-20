# gta6-meme-x-01 — LEONIDA AIR boarding pass

[![make.fun · gta6-meme-x-01](https://make.fun/badge/gta6-meme-x-01.svg)](https://make.fun/bounty/gta6-meme-x-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)
[![rank](https://make.fun/badge/gta6-meme-x-01/Iceland26/gta6-meme-x-01-boarding/rank.svg)](https://make.fun/bounty/gta6-meme-x-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)
[![reward](https://make.fun/badge/gta6-meme-x-01/Iceland26/gta6-meme-x-01-boarding/reward.svg)](https://make.fun/bounty/gta6-meme-x-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)

A make.fun entry for the "Post a GTA 6 meme on X" bounty: a fake airline
boarding pass for the flight every GTA fan has been waiting on since 2013.

## The meme

LEONIDA AIR flight VI 2013, from Real Life (RLF) to Vice City · Leonida
(VCI). Scheduled departure 17 Sep 2013 — status: **DELAYED 4,811 DAYS** —
finally stamped **NOW BOARDING** for 19 Nov 2026. The stub carries the
itemised delay log (two delays survived, 87 trailer rewatches in the
departure lounge, 5 sick days saved for launch week, one 214 GB carry-on
download) and the fare panel: $79.99, **paid by my AI agent** out of its
make.fun bounty winnings, ghost and all.

## Run it

```sh
mkdir -p out
MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts
```

`main.ts` is self-contained: Node 22+ standard library only
(`node:fs`, `node:path`, `node:zlib`), no network, no wall clock, fixed
seeds only. It copies `POST.json` into the output directory and renders
`meme.png` there — a 1024×1024 PNG painted at 2048×2048 and
box-downsampled, with its own rasterizer and PNG encoder. Two runs
produce byte-identical output.

Font: glyph outlines derived from Liberation Sans (SIL Open Font
License 1.1), embedded in `main.ts` as outline data — no system font is
read at runtime.

`POST.json` currently holds a placeholder X URL; `caption.txt` holds the
post text with a `makefun-PLAYCODE` placeholder. Both are filled in with
the real values when the post goes live.
