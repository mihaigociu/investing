# Data Sources & Gathering Checklist — Cognizant

Everything you need to run the analysis in `value-investing-analysis-plan.md`. Cognizant is an actively traded large-cap, so data is abundant — the discipline is to prefer **primary filings** (SEC EDGAR, IR) over secondary aggregators, and to **verify any figure before trusting it.**

## Primary source: SEC EDGAR

- **EDGAR company page:** https://www.sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0001058290&type=10-K
- Cognizant's **CIK is `0001058290`**. Machine-readable filing index (JSON): `https://data.sec.gov/submissions/CIK0001058290.json`

> **⚠️ Access tip (important):** SEC.gov **blocks automated fetchers that don't declare a User-Agent** (HTTP 403). Browser access works fine; for scripted access, send a User-Agent with a contact email:
> ```bash
> curl -s -A "Research your.name@example.com" \
>   "https://data.sec.gov/submissions/CIK0001058290.json" -o ctsh.json
> ```

### Filings to pull (in priority order)

| Filing | Why you need it |
|--------|----------------|
| **10-K (FY2023, FY2024, FY2025)** | Audited annuals: full financials, risk factors (read the AI and competition risk factors closely), MD&A, segment detail, headcount, attrition. The backbone. |
| **10-Q (recent quarters)** | Quarterly trend, bookings, book-to-bill, constant-currency growth, margin trajectory — the leading indicators of whether the AI headwind is showing up in the numbers yet. |
| **Q4/full-year 2025 press release (8-K exhibit 99)** | FY2025 actuals + FY2026 guidance. Already extracted into `financials-actuals.md`. |
| **DEF 14A (annual proxy)** | Executive compensation, incentive metrics, insider ownership. **High priority** given the "management extracting" concern — check whether comp is tied to per-share value/ROIC or to revenue/adjusted metrics, and what the top team is actually paid vs. the workforce. |
| **Earnings-call transcripts (4–6, 2024–2026)** | Management candor on the AI threat *to their own model*, pricing commentary, and whether growth is organic or FX/M&A. |
| **Forms 3/4/5** | Insider buying/selling — are executives buying at these lows, or only selling vested stock? |

## Secondary / supporting sources

- **Company IR site:** https://investors.cognizant.com — press releases, quarterly decks, the annual report.
- **Earnings-call transcripts** — Motley Fool, Seeking Alpha, or the IR archive.
- **Peer filings & commentary** — the AI-disruption thesis is a *sector* story; you must read the peers:
  - **Accenture (ACN)** — the bellwether; its June-2026 guidance cut triggered the sector selloff. Its commentary on bookings, consulting demand, and GenAI is the single best external read on industry direction.
  - **TCS, Infosys (INFY), Wipro (WIT), HCLTech** — Indian majors; same labor-arbitrage model, down ~50% from peaks in 2026. Their results and margin/pricing commentary corroborate or contradict the CTSH story.
  - **IBM, Capgemini, Genpact** — adjacent comparables.
- **Sector/industry views** — JPMorgan, Morgan Stanley, and other sell-side sector notes on IT services (treat price targets skeptically — see below).
- **Macro/industry data** — enterprise IT spending forecasts (Gartner/IDC), for the demand-runway and cyclicality questions.

> **Handle analyst price targets with care.** Several services (e.g., GuruFocus "GF Value" ~$84, sell-side "$67 by 2028" cases) show intrinsic estimates far above ~$43. Many are anchored to *pre-disruption* multiples (~18x) and mechanically look cheap. The reverse-DCF in `valuation-worksheet.md` is a more honest tool — it tells you what the price assumes rather than asserting what it "should" be.

## Data-gathering checklist (build one table)

Fill one column per fiscal year (2023, 2024, 2025) plus a "normalized" column.

**Top line & KPIs**
- [ ] Revenue; revenue growth % (reported **and** constant currency)
- [ ] Organic vs. acquired vs. FX decomposition of growth
- [ ] Bookings (TTM total contract value) and **book-to-bill ratio**
- [ ] Segment revenue & growth (Health Sciences, Financial Services, Products & Resources, CMT)
- [ ] Geographic mix (North America / Europe / Rest of World)

**Profitability**
- [ ] GAAP operating margin; **adjusted** operating margin (and the size of the adjustment)
- [ ] GAAP net income; GAAP diluted EPS; **adjusted** diluted EPS
- [ ] Stock-based compensation ($ and % of revenue)
- [ ] Effective tax rate (watch for one-off tax items distorting GAAP EPS)

**Cash & capital**
- [ ] Operating cash flow
- [ ] Capex (should be small — ~1–1.5% of revenue)
- [ ] Free cash flow and **FCF conversion** (FCF ÷ net income)
- [ ] Owner earnings (compute per worksheet: FCF − SBC ± normalization)
- [ ] Cash & short-term investments; total debt; **net cash**
- [ ] Shares outstanding (diluted); buybacks executed ($ and avg price)
- [ ] Dividends paid; payout ratio
- [ ] Acquisitions ($ spent, what was bought, and how it's performed)

**People (the labor model)**
- [ ] Headcount (total and delivery)
- [ ] Voluntary attrition (TTM)
- [ ] Utilization (if disclosed)
- [ ] Revenue per employee (a rough productivity gauge — watch whether AI lifts it)

**Returns**
- [ ] ROE
- [ ] ROIC (and ROIC excluding excess cash / adjusting for goodwill)

**For the buy/wait decision**
- [ ] Current price, 52-week range, YTD move
- [ ] Market cap, net cash, enterprise value
- [ ] P/E (GAAP & adjusted), P/FCF, EV/Revenue, EV/adj-EBIT, dividend yield — **vs. CTSH's own 10-year medians** and **vs. peers**
- [ ] Reverse-DCF implied growth/decline at the current price (the key number)
