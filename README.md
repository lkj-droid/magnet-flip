# Magnet Flip

A free magnetic chain puzzle game that plays in the browser: tap a tile to flip it and
its four neighbours, complete a row or column of one colour to snap it away, and chain
the drop for bonus moves.

**Play: https://lkj-droid.github.io/magnet-flip/**

- **Daily Challenge** — one board per day, generated from the UTC date, identical for every
  player in the world, resetting at 00:00 UTC. Finish a run and share your score and an emoji
  map of your board. Play on consecutive days to build a **day streak**.
- **Classic Run** — a fresh random board every time, 20 moves to start, no clock.

No download, no sign-up, no cookies, no analytics, no advertising and no network requests
once the page has loaded. Scores are kept in your own browser's local storage.

The board is drawn as a physical toy: an enamel N/S magnet in each carved well of a cream
lacquer tray, resting on a dark green felt table. Every light in the interface comes from the
same top-left source — rim highlights on the top edge, shadows below, one specular sweep on
each magnet. The game's own artwork, drawn in canvas and CSS; no image files, fonts or
libraries are fetched.

## Contents of this repository

| File | What it is |
| --- | --- |
| `index.html` | The whole game — markup, styles and script in one page |
| `favicon.svg` | The enamel magnet mark |
| `og-cover.png` | 1200×630 social preview card |
| `robots.txt` | Crawler rules |
| `sitemap.xml` | Sitemap for search engines |

## How it works

- 5×5 grid of blue **N** and red **S** enamel magnets.
- A tap flips the chosen tile plus the ones above, below, left and right (three at a corner).
- A full row or column of one colour clears; tiles fall, new tiles drop in from the top, and a
  drop that completes another line chains. A chain runs the board hot — the frame glows, the
  score turns gold and a chain tag appears under the board until it cools (gold from ×3 up).
- Score is `100 × (lines cleared)² × chain step`. A clear pays +2 moves (+3 more on a chain
  step), capped at 30 moves.

## Running locally

Open `index.html` in a browser — it has no build step and no dependencies. For a realistic
check you can also serve the folder:

```sh
python3 -m http.server 8000
# then open http://localhost:8000/
```

## Credits

Original code and artwork. No third-party assets, fonts, libraries or trademarks are used.

## Licence

© 2026 Magnet Flip. All rights reserved.
