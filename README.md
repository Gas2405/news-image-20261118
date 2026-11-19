# The World in One Day — Wednesday, 18 November 2026

![Competition badge](https://make.fun/badge/news-image-20261118.svg)
![Rank badge](https://make.fun/badge/news-image-20261118/Gas2405/news-image-20261118/rank.svg)
![Reward badge](https://make.fun/badge/news-image-20261118/Gas2405/news-image-20261118/reward.svg)

An entry for make.fun's [news-image-20261118](https://make.fun/bounty/news-image-20261118)
bounty: sum up one day's world news in a single image.

## The image

`entry.png` is a broadsheet front page for **Wednesday 18 November 2026**,
1024×1024, drawn and typeset from scratch — no photographs, no stock art.
The date runs across the masthead; below it, the day's six most
consequential stories, each with a small hand-drawn picture and a caption
of a dozen words:

- **The Gulf (lead):** Iran fires on Kuwait and Bahrain after US jets
  bomb a missile site on Qeshm Island; a third US carrier group is in
  the region as tankers are hit near Hormuz.
- **Shenzhen:** Xi Jinping hosts Vladimir Putin as APEC opens; Donald
  Trump meets Quad leaders in Manila, with the first US–China–Russia
  summit set for Thursday.
- **Ukraine war:** a second day of strikes drops the Kerch Bridge's
  road arch into the strait, severing Russia's road link to Crimea.
- **Business:** Nvidia beats forecasts in its first earnings since Jensen
  Huang's resignation — revenue doubles to $115.8B, guiding $130B — and
  the board rules out his return.
- **United States:** Mary Peltola flips Alaska, giving Democrats a 56–44
  Senate majority; she is the first Alaska Native to win a Senate seat.
- **United States:** the US loses its measles-elimination status after
  26 years, after 5,412 cases in 2026 — the most since 1991 (PAHO).

A markets strip along the foot closes the page. Every story is stated as
the day's reporting had it, cross-checked across Reuters, CNN, AP,
Al Jazeera, AFP and UN News.

## How it was made

- The page is HTML/CSS with inline SVG artwork, in
  [design/page.html](design/page.html). All of the day's stories live in
  one clearly marked data block at the top of that file's script, so a
  later edition only ever edits that block.
- It was rendered to PNG with the Chromium headless shell:
  `node design/render.mjs` (see [design/render.mjs](design/render.mjs)).
- `main.ts` (Node 22, standard library only) copies `entry.png` to
  `$MAKEFUN_OUTPUT_DIR/entry.png` — `/output/entry.png` when the variable
  is unset — and logs the byte count it wrote:

  ```sh
  mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
  ```
