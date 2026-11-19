# The World in One Day — Wednesday 18 November 2026

Newspaper-style poster summing up the world news of Wednesday 18 November
2026, built from scratch for make.fun competition `news-image-20261118`.

## The image

`entry.png` — 1024×1024. A front page:

- **Masthead** — "THE WORLD IN ONE DAY", dated Wednesday 18 November 2026.
- **Three leads** — the Xi–Putin talks and Thursday's first-ever
  Trump–Xi–Putin trilateral in Shenzhen; fire exchanged across the Gulf
  (U.S. strike on Qeshm Island, Iranian drones at Kuwait and Bahrain,
  third U.S. carrier in the region); Anthropic's $81.3bn IPO, the largest
  debut in history.
- **World map** — a hand-drawn map with 12 numbered markers and a legend.
- **Eight sections, 36 stories + 3 leads = 39 stories** — Europe, Middle
  East, Africa, Asia-Pacific, Americas, Economy & Markets, Climate &
  Science, Sport & Culture.
- **The day in numbers** — $81.3bn IPO, 141 drones in a night, €45bn EU
  loan for Ukraine, gold $3,728, 145 km/h cyclone gusts, 5 IPL titles for
  Dhoni, $190.4m Van Gogh.

All 39 stories were researched fresh from reporting dated 18 November 2026
(Reuters, AP, AFP, BBC, Al Jazeera, The New York Times, CNN, NDTV and
others). Nothing is copied from the 17 November entry; this build was
written entirely fresh.

## How it was made

`poster.html` is the poster (HTML + CSS + inline SVG map). It was rendered
to `entry.png` with headless desktop Chrome at 1024×1024. `main.ts` copies
the shipped `entry.png` to the output directory using a path resolved from
`import.meta.url`, so it works from any working directory and both grader
runs produce byte-identical output.

## Verify

```sh
mkdir -p /tmp/out1 /tmp/out2
cd /tmp && MAKEFUN_OUTPUT_DIR=/tmp/out1 node /path/to/repo/main.ts
cd /tmp && MAKEFUN_OUTPUT_DIR=/tmp/out2 node /path/to/repo/main.ts
sha256sum /tmp/out1/entry.png /tmp/out2/entry.png   # must match
```

## License

MIT — see `LICENSE`.
