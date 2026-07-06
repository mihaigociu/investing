# Data Sources & Gathering Checklist — Rover Group

Everything you need to run the analysis in `value-investing-analysis-plan.md`. Rover is delisted, but **all public-era filings remain permanently available on SEC EDGAR** — this is the primary, authoritative source. Use filings over secondary sites; verify any figure before trusting it.

## Primary source: SEC EDGAR

- **EDGAR company page:** https://www.sec.gov/edgar/browse/?CIK=1826018
- Rover Group's **CIK is `0001826018`**. Machine-readable filing index (JSON): `https://data.sec.gov/submissions/CIK0001826018.json`

> **⚠️ Access tip (important):** SEC.gov **blocks automated fetchers that don't declare a User-Agent** (you'll get HTTP 403). Browser access works fine; for scripted access, send a User-Agent with a contact email. Example that works:
> ```bash
> curl -s -A "Research your.name@example.com" \
>   "https://www.sec.gov/Archives/edgar/data/1826018/000162828024001811/rover-definitiveproxystate.htm" -o proxy.htm
> ```
> The DEFM14A used for this analysis: accession `0001628280-24-001811`. The management projections and both banks' fairness-opinion ranges have already been extracted into `deal-benchmark-and-peers.md`.

### Filings to pull (in priority order)

| Filing | Why you need it |
|--------|----------------|
| **10-K (FY2021, FY2022, FY2023)** | Audited annuals: full financials, risk factors, MD&A, segment/KPI disclosures (GBV, take rate, bookings). The backbone. |
| **10-Q (all quarters)** | Quarterly trend + seasonality; most recent operating picture before the deal. |
| **S-4 / proxy from 2021 SPAC merger** | Rover went public via SPAC (Nebula Caravel Acquisition Corp / True Wind Capital). Contains original projections, historical financials, deal terms, warrant structure. |
| **DEFM14A + 8-K (Blackstone deal)** | Merger proxy for the take-private. Contains the **board's fairness opinion, the banker's valuation analyses (DCF, comparable companies, precedent transactions), and management projections** — a *goldmine* for the "$11 test." Announced 29 Nov 2023; closed 27 Feb 2024. |
| **DEF 14A (annual proxy)** | Executive comp, incentive structure, insider ownership — for Phase 3. |
| **Forms 3/4/5** | Insider buying/selling. |

> **Tip:** The merger proxy's fairness-opinion section is the single most useful document for the case study — it shows exactly how Rover's own advisors valued the company and justified $11. Read it *after* forming your own view, so it doesn't anchor you.

## Secondary / supporting sources

- **Earnings-call transcripts** — Motley Fool, Seeking Alpha, or the company's IR archive (via Wayback Machine: `web.archive.org` → `investors.rover.com`). Pull 4–6 across 2022–2023 for management candor (Phase 3).
- **Press releases** — Rover blog press archive and GlobeNewswire for the deal announcement and quarterly results.
- **Wayback Machine** — Rover's investor-relations pages are gone post-delisting; retrieve them via archive.org.
- **Industry / TAM data** — American Pet Products Association (APPA), pet-care market reports, for Phase 1 TAM and Phase 6 secular-tailwind claims.
- **Competitor filings** — **Wag! (Nasdaq: PET)** is a directly comparable public marketplace; **Care.com** (pre-buyout) filings; use for peer multiples and moat comparison.

## Data-gathering checklist (build one spreadsheet)

Fill one column per fiscal year (2021, 2022, 2023) plus a "normalized" column.

**Top line & marketplace KPIs**
- [ ] Gross Booking Value (GBV)
- [ ] Bookings / active bookings count
- [ ] Blended take rate (Revenue ÷ GBV)
- [ ] Revenue
- [ ] Revenue growth % and GBV growth %
- [ ] Repeat-booking rate / retention (if disclosed)

**Profitability**
- [ ] Gross / contribution margin ($ and %)
- [ ] Sales & marketing as % of revenue
- [ ] Adjusted EBITDA + margin
- [ ] GAAP operating income
- [ ] GAAP net income (note the inflection to profitability)
- [ ] Stock-based compensation ($ and % of revenue)

**Cash & capital**
- [ ] Operating cash flow
- [ ] Capex (should be small — asset-light)
- [ ] Free cash flow
- [ ] Owner earnings (compute per worksheet)
- [ ] Cash & equivalents
- [ ] Total debt / net cash
- [ ] Shares outstanding (basic and *fully diluted*, incl. warrants)
- [ ] Buybacks executed ($ and avg price)
- [ ] Acquisitions ($ spent, what was bought)

**Returns**
- [ ] ROE
- [ ] ROIC (and ROIC excluding excess cash)

**For the "$11 test"**
- [ ] Undisturbed share price before 29 Nov 2023 announcement
- [ ] Implied equity value and enterprise value at $11.00
- [ ] EV/Revenue, EV/EBITDA, P/FCF at $11
- [ ] The banker's DCF range and comps from the merger proxy
