# CAC_post3 — Where the World Cup Actually Lives

Calcio AC post #03. A geographic / economic read of every WC 2026 squad — which clubs, which leagues, and which continents actually run the tournament.

## Headline findings
- **Manchester City** sends 19 players to WC 2026 — more than any other club
- **Big-5 European leagues** (England, Spain, Italy, Germany, France) account for **~43%** of the entire tournament
- **Saudi Pro League** is the **6th-biggest supplier** — ahead of MLS, Eredivisie, Liga MX, Brasileirão
- **~66%** of all WC 2026 players play their club football in Europe
- **Netherlands**: 26 players, almost none in Eredivisie · **Senegal**: 26 players, none in Senegal · **Qatar**: 92% home-based

## Structure
```
CAC_post3/
├── data/                       # source CSV + enriched data.json
│   ├── wc2026_squads.csv
│   └── data.json
├── web/
│   ├── index.html              # interactive dashboard (Plotly)
│   ├── slides.html             # 9-slide carousel + HD export
│   └── logo.svg
├── images/                     # exported slide PNGs go here
├── index.html                  # redirect to /web/
└── README.md
```

## Live site
Once GitHub Pages is enabled (Settings → Pages → branch `main`, root `/`):
`https://calcio-ac.github.io/CAC_post3/`

## Interactive dashboard features
- 4 KPI tiles · sortable top-N clubs (filterable by continent)
- Top leagues bar chart with Big-5 highlight
- Continent share pie
- **Pick-a-country**: see where any of the 48 nations' players actually play
- **Home vs Abroad** ranking — every nation, sorted by % of squad in domestic league
- **Pick-a-club**: see who plays for any of the top 30 clubs
- Methodology box at the bottom explaining attribution rules

## Slide deck (9 slides, 1080×1350)
1. COVER — "Where the World Cup actually lives"
2. **5 CLUBS RUN THE WORLD** — top 10 club bar chart
3. **5 LEAGUES, HALF THE WORLD CUP** — Big-5 = 43%
4. **BY CONTINENT** — table + top club in each
5. **THE SAUDI PROJECT** — 6th-biggest supplier
6. **HOME vs ABROAD** — Qatar 92% / Senegal 0%
7. **WHERE EXPORTERS PLAY** — Morocco → France, Senegal → England, etc.
8. **HOW WE COUNT** — methodology slide (the Barça press-release discrepancy explained)
9. **CTA** — link to interactive site + calcioac.com

HD export: per-slide ⬇ DOWNLOAD HD (2x = 2160×2700) and ⬇ DOWNLOAD ALL.

## Methodology
- **Club attribution**: each player is credited to their **parent club** at squad announcement. Loanees go to the parent club, not the loan club (the rule FIFA uses).
- **Reserves merged**: B-teams roll up to the senior team (per user request — e.g. `Barcelona B` → `Barcelona`).
- **League = club country**, covering all divisions combined.
- **Continent = club continent**, not the national team's.
- **Mapping coverage**: ~97% of players are tagged with a club country. The ~3% remainder are spelling variants that don't affect any of the top-10 rankings.
- **Source**: FBref / FIFA roster + manual normalization.

## Palette / font
`#0277B6` Europe · `#D90429` accent / Saudi · `#09D69F` highlight · `#FFD166` BG · Courier New everywhere.
