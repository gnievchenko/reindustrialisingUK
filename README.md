# Paying for Power

**Industrial electricity prices in the United Kingdom, Germany and China, 2010–2025 — what Britain's are made of, and why.**

📄 **Read the study:** *(link goes here once GitHub Pages is switched on)*

> **Status: draft for review.** Figures may change. The register stamp in the article footer (`@ D72/Q103/S220`) identifies exactly which version of the underlying workbook the published numbers come from.

---

## What this is

A comparative study of what energy-intensive industry actually pays for electricity in three countries, built bottom-up from published tariffs, levies, network charging schedules and wholesale market data rather than from headline survey averages alone — and then reconciled against those survey averages, with the gap between the two treated as a finding rather than an error.

The study has two jobs, in order: **diagnose** why UK industrial electricity is priced as it is relative to Germany and China, then **prescribe** measures that would improve UK competitiveness. The prescription follows the diagnosis, not the other way round.

## The main findings

**British industrial electricity is expensive, but by 2025 the popular explanation is largely out of date for the firms it is supposed to be about.** For a fully-relieved energy-intensive user, UK levies are exactly zero, and pure network charges have converged with Germany's — about $5.5/MWh against $7.9. On an all-in basis at the large baseload archetype, Britain has crossed over: roughly $133/MWh against Germany's $141.

**The remaining British disadvantage sits in wholesale power, not in the policy stack.** British wholesale prices track the short-run marginal cost of gas generation almost identically at annual resolution; in Germany gas sets a *ceiling* rather than the marginal price, and in China coal contracts anchor the price. That is a merit-order difference, not a hub-price difference — Britain and Germany buy gas at nearly the same price.

**Relief is narrow.** Roughly 85% of British industrial electricity volume carries no exemption at all, so the relieved case above is a minority experience. And at the medium archetype — a 20 GWh two-shift site — the ranking reverses: Britain is far more expensive than Germany, because such a site qualifies for German network relief nowhere near as easily as commentary assumes.

The study also tests, and declines to support, several popular remedies — including the claim that restarting North Sea production or building nuclear would lower industrial prices.

## Contents

| Path | What it is |
|---|---|
| `paying_for_power_article.html` | The study. Single file, no dependencies, 14 interactive figures drawn as inline SVG. Open it directly in a browser. |
| `industrial_electricity_master.xlsx` | The master workbook — the single source of truth for every number in the article. |
| `data/*.csv` | Plain-text extracts of the load-bearing sheets, so changes are visible in diffs. |

## How to check the numbers

Every figure in the article resolves to a cell in the workbook, and every input resolves to a registered source. Three sheets carry that trail:

**`decisions`** — every methodological choice, numbered `D1`…`D72`, each with the reasoning and the date it was signed off. Where a choice could have gone another way, the alternative is recorded.

**`qc`** — every quality-control finding, numbered `Q1`…`Q104`, including the ones that are still open and the ones that turned out to be my own errors. Findings are not removed once resolved.

**`sources`** — every primary source, numbered `S1`…`S220`, with the URL and the retrieval date.

Charts in the article have a **"View data"** control beneath them that opens the underlying series as a table, so no figure has to be read off an axis.

## Method, in brief

Prices are built as a stack — wholesale energy, network and system charges, levies and taxes including generation-capital recovery, and (for the UK) a measured supplier cost-and-margin block — for two archetypal sites in each country, at two relief states. All prices are stated in real 2025 US dollars at Federal Reserve annual-average exchange rates, excluding VAT, and include energy taxes as actually borne on both the observed and modelled sides.

The modelled stacks are then reconciled against published survey averages (DESNZ QEP for the UK, Eurostat for Germany, provincial tariff schedules for China). The residual between the two is decomposed rather than assumed away; most of it turns out to be procurement vintage — British industrial users buying forward at prices struck in earlier, more expensive years.

## Corrections

Corrections are welcome and will be made as dated commits rather than silent edits. If a number looks wrong, the fastest way to show it is to name the workbook cell or the register entry it comes from. Open an issue.

One limitation is known and flagged rather than hidden: the stage-7 network projections for 2028/29 onward still rest on a superseded RIIO-ET3 draft determination, rescaled by published chain factors (logged as `Q98`/`Q99`); no figure in the article depends on them. The grid-utilisation claim itself is tested in the article's section 10, and the evidence base behind that section is banked in the workbook at `stage7_network` rows 71–96 (`D72`).

## Licence

Text, charts and analysis: [CC BY 4.0](LICENSE). Underlying data is drawn from public sources, each individually cited in the `sources` sheet and subject to its own terms.
