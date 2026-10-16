# Battery demand & end-of-life materials, 2020–2050

An interactive, self-contained scenario suite for the battery age: demand, materials,
carbon debt, and the infrastructure networks beneath it all. No build step, no
dependencies, no tracking — plain HTML with inline SVG charts.

**View it:** open `index.html` in any browser, or enable GitHub Pages
(Settings → Pages → deploy from branch, root) and the repo serves automatically at
`https://<user>.github.io/<repo>/`.

## Pages

| File | What it shows |
|---|---|
| `index.html` | The master model: three scenarios (consensus / accelerated EoL / Doubling Down), demand by EV & BESS segment, chemistry, materials in Mt, mine-supply balance, plants & investment, gap table. Year slider + scenario + Global/China/ROW toggles. |
| `non-passenger-vs-us-eu.html` | The argument in one chart: global non-passenger EV battery volume (GWh) vs the entire US+EU EV market, isolated at 2030 / 2035 / 2040. |
| `pack-volume-by-sector.html` | Stacked columns: battery pack volume (TWh) by transport sub-sector — from 3 kWh 2/3-wheeler packs to MWh-class marine tug swap packs — 2020–2050. |
| `battery-network.html` | The unmodelled layer: swap stations, spare-pack float, charging energy, backup/resilience fleet, recovery plants and collection depots. |
| `data/model.json` | Every scenario table, mix, intensity and derived-metric rule behind the pages. |

## The three scenarios

| Scenario | 2030 | 2035 | 2040 | 2050 | Core logic |
|---|---|---|---|---|---|
| Analyst consensus | 4.6 TWh | 7.6 | 11.5 | 17.5 | Flat extrapolation; has under-reported demand every year since 2020 |
| Accelerated EoL | 7.0 TWh | 13 | 23 | 38 | Larger packs, data-centre deep DoD, deeper cycling, harsher asset use, 3C & small-format fleet — 2030–2040 is the S-curve |
| Doubling Down | 9.5 TWh | 19 | 34 | 55 | All of the above plus 15th FYP circular economy → 16th FYP fast-track: 50% of materials from recovery by 2035; coal/oil/gas applied energy replaced; diesel out |

## Model logic (short form)

- **Demand is non-linear** — the steep section of the S-curve is 2030–2040.
- **EoL accelerates faster than installs** — deeper DoD and harsher use compress asset life.
- **The materials deficit is the order book** — even consensus runs ~5 Mt short by 2030; the gap is the build programme, not a ceiling.
- **Alternative storage in the stationary layer** (Na-ion, vanadium flow, pumped hydro, CAES) frees lithium for transport.
- **The network is unmodelled everywhere else** — charging, swapping, backup and disposal are the roads-and-traffic-lights of this transition; every node is a measurement point.

Key evidence anchors: Ember EV Sales Tracker (Oct 2026: $20bn oil displaced in six months
post-Hormuz; +45% BEV growth ex-US/China; 49/56 countries at record share), IEA Global EV
Outlook 2026 (1-in-4 trucks electric in China), field observation along China
corridors (Pinglu Canal–Huzhou marine swaps, Ningbo/Qingdao port fleets, Yiwu consumables
belt, Tianjin–Ningde BYD/CATL/CRRG).

## Files

```
index.html                      master scenario model
non-passenger-vs-us-eu.html     non-passenger GWh vs US+EU benchmark
pack-volume-by-sector.html      pack volume by transport sub-sector
battery-network.html            charging / swapping / backup / disposal networks
data/model.json                 full model tables and rules
```


## Challenge this model

This repository is published as a deliberate challenge to consensus forecasting.
Cetacea's position: analyst models have under-reported battery demand every year since
2020 because they price the fossil-era transition — linear, policy-pushed, US/EU-centred —
onto an era that is structural, price-driven, consumer-pulled, and majority non-Western.
We would rather be corrected in public than politely ignored.

**Where to hit us hardest** — the five assumptions we most want sector specialists to counter:

1. **The swapping float (3×).** Swapped segments carry ~3× pack volume in circulation
   (in service / waiting / charging). Based on 2/3W and taxi fleet ratios in China and
   East Africa. *If you operate swap networks: what is the real station-to-vehicle ratio?*
2. **Doubling Down recovery share (50% of materials by 2035).** Assumes the 15th FYP
   circular-economy rollout feeds a 16th FYP fast-track. *Metallurgists and plant
   engineers: is 50% recovery share physically achievable by 2035 — feedstock quality,
   chemistry limits, build speed?*
3. **EoL acceleration.** Harsher use (deep DoD, high cycle counts, V2G, twin-shoulder
   cycling) compresses asset life 20–60% vs consensus. *Fleet operators and battery
   warranty teams: what are your actual retirement curves?*
4. **Materials intensity and mine supply.** Blended kt/GWh glide paths and the
   existing-plus-committed mine supply series. *Geologists and cost curve analysts:
   where is the supply number wrong — too optimistic or too pessimistic?*
5. **The US+EU benchmark.** ~280 GWh (2026) growing ~12%/yr. *Market analysts: is EU
   growth + US stall the right shape, or does US policy reversal change it?*

Open an issue — data beats adjectives, but both are welcome. Every accepted correction
lands in `data/model.json` with a changelog entry and a named credit in the README.

## Changelog

- **v1.0 (Oct 2026)** — initial release: three scenarios through 2050, materials balance
  vs mine supply, non-passenger benchmark, network model. Evidence anchors: Ember EV
  Sales Tracker Oct 2026, IEA Global EV Outlook 2026, field observation China corridors.

## Caveats

Illustrative house-view modelling for discussion — not investment advice, not a consensus
forecast. Materials scope is five key metals (lithium LCE, nickel, cobalt, copper,
graphite). Re-verify against current market data before external use.

## License

CC BY 4.0 — reuse with attribution.
