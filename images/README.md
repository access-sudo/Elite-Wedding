# Images

Every image on the page is loaded from this folder. The 11 filenames below are
what `index.html` and `app.js` reference — drop a file in with the exact name
and that slot fills in. Names and extensions must match exactly (all `.jpg`).

These slots previously pointed at `readdy.ai/api/search-image?...` generator
URLs. All 11 of those now return **HTTP 404**, which is why the page shows no
images. Two were also malformed (the prompt was truncated at an apostrophe and
the query params were spliced in mid-sentence).

| # | File | Source size | Where it appears |
|---|------|-------------|------------------|
| 1 | `hero-palace-arch.jpg` | 1000 x 1400 (portrait) | Hero — palace gateway |
| 2 | `journey-baraat.jpg` | 1600 x 900 (landscape) | Journey — Baraat |
| 3 | `journey-haldi.jpg` | 1600 x 900 (landscape) | Journey — Haldi |
| 4 | `journey-mehndi.jpg` | 1600 x 900 (landscape) | Journey — Mehndi |
| 5 | `journey-decor.jpg` | 1600 x 900 (landscape) | Journey — Decor / mandap |
| 6 | `journey-catering.jpg` | 1600 x 900 (landscape) | Journey — Catering |
| 7 | `journey-entertainment.jpg` | 1600 x 900 (landscape) | Journey — Entertainment |
| 8 | `atelier-floral.jpg` | 900 x 900 (square) | Atelier — florist's hands |
| 9 | `venue-amber-courtyard.jpg` | 900 x 1200 (portrait) | Venue — Amber Courtyard |
| 10 | `venue-lake-pavilion.jpg` | 900 x 1200 (portrait) | Venue — Lake Pavilion |
| 11 | `venue-jali-hall.jpg` | 900 x 1200 (portrait) | Venue — The Jali Hall |

The source sizes are the aspect ratios the layout was designed around. A larger
file at the same ratio is fine; a different ratio will crop.

If you would rather host the images elsewhere (a CDN or an S3 bucket), replace
the `images/<name>.jpg` values in `index.html` and `app.js` with the full URLs
instead — each name appears exactly once in each file.
