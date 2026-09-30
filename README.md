# MG4 Urban – Software Improvement Proposals

Interactive prototype that demonstrates ten owner-reported issues and proposed enhancements for the **MG4 Urban** (Brazilian market) infotainment system, instrument cluster and MG app.

**Live demo:** https://arthur-lzrs.github.io/mg4urban-improvements/

> Independent owner proposal prepared for MG's software development and improvement team. It is not an official MG product. Implementation feasibility and hardware compatibility require assessment by MG; no specific software release is assumed.

## What the prototype shows

The layout reproduces the current head unit (home screens, Settings, Energy, bottom bar) and the instrument cluster, then applies each proposal on top of it.

| # | Proposal | Where to try it |
|---|----------|-----------------|
| 1 | Overall infotainment responsiveness | Any screen – compare *Current* (simulated delay, no feedback) vs *Proposed* |
| 2 | Automatic light/dark color scheme by headlight status | Settings › General + "Headlights on" toggle |
| 3 | Wireless charging on/off control | Settings › General + "Phone on wireless pad" toggle |
| 4 | Customizable main screens and bottom bar | Home › Customize (drag, remove, add, restore default) |
| 5 | MG Pilot profiles + quick access button | Bottom bar: tap to apply, press and hold to choose |
| 6 | Adjustable instrument cluster font size | Settings › Instrument cluster, then the *Instrument cluster* tab |
| 7 | Native voice assistant in Brazilian Portuguese | Settings › Voice – tap a sample command |
| 8 | Brazilian Portuguese interface translation | Select item 8 – labels switch to PT-BR (current vs proposed) |
| 9 | Expanded audio equalization | Settings › Sound (10 bands, presets, save custom) |
| 10 | Vehicle sharing between separate MG app accounts | *MG app* tab – two phones side by side |

### Controls

- **Left panel** – the ten items with issue, impact, proposed improvement, technical consideration and "how to try it". Clicking an item opens the related screen.
- **Infotainment / Instrument cluster / MG app** – switches the simulated display.
- **Version: Proposed / Current** – toggles between the proposal and a representation of today's software.
- **Improvement markers** – amber numbered badges on every changed element.
- **Simulation bar** – headlights, phone on wireless pad and vehicle speed.

## Notes

- Built for desktop browsers (latest Chrome, Edge, Safari or Firefox).
- Vehicle artwork is simplified vector illustration. The "Current" screens for the voice assistant and equalizer are representations, not captures.
- Suggested Brazilian Portuguese wording (item 8) is an example for evaluation.
- `index.html` is fully self-contained (no build step, no external dependencies at runtime besides web fonts).

## Publishing on GitHub Pages

1. Push these files to the `main` branch of `arthur-lzrs/mg4urban-improvements`.
2. In the repository, go to **Settings › Pages** and set **Source** to **GitHub Actions**.
3. The workflow in `.github/workflows/pages.yml` deploys automatically on every push to `main` (it can also be run manually from the *Actions* tab).

Alternative without Actions: **Settings › Pages › Deploy from a branch**, branch `main`, folder `/ (root)`.

## Repository structure

```
.
├── index.html                 # Self-contained interactive prototype
├── 404.html                   # Redirects unknown paths to the prototype
├── .nojekyll                  # Serve files as-is (no Jekyll processing)
├── .github/workflows/pages.yml
└── README.md
```

## Author

Arthur – MG4 Urban owner, Brazil · 30 September 2026
