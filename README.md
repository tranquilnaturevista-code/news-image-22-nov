# The World in One Day — Sunday 22 November 2026

[![News Image](https://make.fun/badge/news-image-20261122.svg)](https://make.fun/bounty/news-image-20261122)
[![Rank](https://make.fun/badge/news-image-20261122/tranquilnaturevista-code/news-image-22-nov/rank.svg)](https://make.fun/bounty/news-image-20261122)
[![Reward](https://make.fun/badge/news-image-20261122/tranquilnaturevista-code/news-image-22-nov/reward.svg)](https://make.fun/bounty/news-image-20261122)

Entry for the [make.fun bounty “Sum up 22 November's world news in one
image”](https://make.fun/bounty/news-image-20261122): a one-page newspaper
front page for **Sunday 22 November 2026**, drawn programmatically with
Pillow. The masthead and the date are the largest type on the page, the
lead story is the COP31 climate talks in Antalya, and six more stories
cover Ukraine, the Gulf, the Baltic, Mexico, world trade, and Hong Kong —
plus a ticker of four further stories along the bottom.

## How it works

- `render_frontpage.py` draws the page (1024×1024, PNG) from the story
  list below and saves it as `entry.png`. It uses no network, no
  randomness, and no timestamps: two runs produce byte-identical output.
- `main.py` is the entry program. It verifies that `entry.png` is a whole
  PNG within the competition limits (at most 1024×1024 pixels, at most
  1 MiB) and copies it byte for byte to `/output/entry.png`, so the page
  the judge sees is exactly the page laid out here.

## Stories in the image

- **COP31 nears a final deal (lead).** After days deadlocked over fossil
  fuels, climate talks in Antalya, Turkey, put a new package to nearly
  200 nations, with a plenary due to approve it on Sunday morning.
  (Reuters, 22 November 2026)
- **Overnight barrage batters Ukraine.** Russia fires hundreds of drones
  and dozens of missiles overnight into Sunday; Poland scrambles jets.
  (Times of India / Reuters, 22 November 2026)
- **Tankers hit off Oman as Gulf tensions surge.** Bahrain investigates a
  Patriot interceptor crash amid reports of Iranian drone attacks, while
  Trump seeks a lasting nuclear deal with Iran. (Times of India, 22
  November 2026)
- **Drones hit Russian ship in the Baltic.** Finland tightens security in
  the Gulf of Finland and says Ukraine was likely behind the attack.
  (Times of India, 22 November 2026)
- **Cartel boss “El Chapo Isidro” arrested.** The FBI most-wanted drug
  lord is seized in a shoot-out; 11 are killed in the violence that
  follows in Sinaloa. (Times of India, 22 November 2026)
- **EU and Indonesia sign landmark trade deal.** A decade of negotiations
  ends: 98.5% of tariffs to go, saving exporters about €600m a year.
  (European Commission / Reuters, 21–22 November 2026)
- **Hong Kong votes for Election Committee.** Some 5,700 voters choose the
  powerful body that picks the city's leader. (22 November 2026 news
  digest)
- **Also today:** tech shares slide; former Brazilian president Jair
  Bolsonaro is in intensive care; Zelensky calls the Crimean Bridge
  strikes “a fair response”; the FBI probes a hack of its crime database.
  (BBC, Times of India, 22 November 2026)

Where outlets disagreed on casualty figures, the image states no figure
rather than guessing one. All stories are events that happened, or were
first reported, on 22 November 2026.

## Reproduce

```sh
python3 render_frontpage.py   # writes entry.png (deterministic)
python3 main.py               # writes /output/entry.png
```

Python 3.13, Pillow, and the DejaVu fonts are all that is needed to
render; `main.py` itself needs only the standard library.
