# Valuation Worksheet — Rover Group

Keep three scenarios throughout: **Conservative / Base / Optimistic**. Buffett's discipline: if you need the optimistic case to justify the price, it's too expensive.

> **Status:** partially populated with actuals from `financials-actuals.md`. Blanks (`___`) remain where the number requires the DEFM14A merger proxy or your own judgment. Do the math yourself before trusting any figure.

**Anchor numbers (from `financials-actuals.md`):** FY2023E revenue ~**$231M**, Adj. EBITDA ~**$47M**, SBC ~**$22M**, capex ~**$9M**, net cash ~**$230M**, diluted shares ~**181M**, Blackstone price **$11.00** (equity ~$2.3B, EV ~$2.07B).

---

## 1. Normalized Owner Earnings

Buffett's preferred earnings measure:

```
Owner Earnings = Net Income (GAAP)
               + Depreciation & Amortization
               + Other non-cash charges
               − Stock-Based Compensation        ← treat SBC as a REAL cash-equivalent cost
               − Maintenance Capex                ← small for asset-light Rover
               ± Normalized working-capital change
```

Two ways to build it — a top-down bridge from Adjusted EBITDA is easiest with the data we have. FY2023E figures in $M:

| Line (Adj-EBITDA bridge) | Conservative | Base | Optimistic |
|------|-------------:|-----:|-----------:|
| Adjusted EBITDA (FY2023E) | 46 | 47 | 48 |
| − Stock-based comp (real cost) | (24) | (22) | (20) |
| − Capex (mostly capitalized s/w) | (9) | (9) | (8) |
| − Cash taxes (NOLs shield near-term) | (1) | (1) | (2) |
| ± Normalized working capital | 0 | +2 | +4 |
| **= Owner earnings ($M)** | **~12** | **~17** | **~22** |
| ÷ Diluted shares (M) | 181 | 181 | 181 |
| **Owner earnings / share** | **~$0.07** | **~$0.09** | **~$0.12** |

> **The punchline:** current owner earnings are ~$12–22M. Against a $2.3B equity value at $11, that's **~100–190x owner earnings**. Rover was *not* cheap on current cash flow — the entire case for $11 rests on **growth + margin expansion** (see §3). The SBC line is decisive: adding it back (as "Adjusted EBITDA" does) roughly *doubles* apparent profit. Owner earnings subtract it.

> ⚠️ The SBC line is where a soft analysis goes wrong. "Adjusted EBITDA" adds SBC back; owner earnings must subtract it. If SBC is large relative to net income, Rover's *economic* profit is much lower than the adjusted headline.

---

## 2. Discounted Cash Flow (Owner Earnings)

Assumptions:

| Input | Conservative | Base | Optimistic |
|-------|-------------|------|-----------|
| Starting owner earnings | ___ | ___ | ___ |
| Yr 1–5 growth % | ___ | ___ | ___ |
| Yr 6–10 growth % | ___ | ___ | ___ |
| Terminal growth % | 2% | 2.5% | 3% |
| Discount rate | 10% | 9% | 9% |

- Project owner earnings for 10 years at the growth rates above.
- Discount each year to present value at the discount rate.
- Terminal value = `Yr10 owner earnings × (1 + terminal g) ÷ (discount rate − terminal g)`, discounted back.
- Enterprise value = Σ PV(years) + PV(terminal). Add net cash, divide by diluted shares.

| Output | Conservative | Base | Optimistic |
|--------|-------------|------|-----------|
| PV of 10-yr cash flows | ___ | ___ | ___ |
| PV of terminal value | ___ | ___ | ___ |
| + Net cash | ___ | ___ | ___ |
| = Equity value | ___ | ___ | ___ |
| ÷ Diluted shares | ___ | ___ | ___ |
| **Intrinsic value / share** | **___** | **___** | **___** |

---

## 3. Reverse DCF — *do this one first, it's the most honest*

Instead of forecasting, ask: **what does the price already assume?**

**We now have the real answer from the DEFM14A** (no need to guess). The plan the bankers discounted to reach ~$11 assumed:
- Revenue **CAGR ~15%** for a decade ($231M → $961M by 2033).
- **Unlevered FCF growing from $18M (2023) to $264M (2033)** — a ~**31% CAGR**.
- Adjusted EBITDA margin **doubling from ~20% to ~42%**; U.S. take rate rising from ~22% to **27.5%**.
- Discount rate (WACC) **12.5–14.5%**; perpetuity growth **4–6%**.

Even on those aggressive assumptions and that high discount rate, the banks' DCFs only reach **$11.25 / $11.41 at the very top** of their ranges (Centerview / Goldman). So:
- **$11 = the ceiling of a bullish plan.** There is essentially **zero margin of safety** — you'd be paying for flawless execution of a decade-long take-rate-and-margin expansion.
- At the **undisturbed ~$8.4**, you'd still be underwriting most of that plan, just with a small cushion.

**Judgment:** The growth/margin ramp baked into **$11 is optimistic-to-heroic** (a doubling of EBITDA margin *and* a rising take rate, with no recession allowance). A value investor demanding a margin of safety would pass at $11 and would only have been interested near Rover's **2022 lows (~$3–5)**. Rewrite in your own words after stress-testing the plan: ________________________________________.

---

## 4. Multiples Cross-Check

At $11.00/share:

| Multiple | Rover @ $11 | Wag! (PET) FY23 | Rover's own history | Verdict |
|----------|-----------:|----------------:|--------------------|---------| 
| EV / Revenue (FY23E) | **~9.0x** | **~0.9–1.0x** | ~2–5x in 2022 lows | rich |
| EV / Adj. EBITDA (FY23E) | **~44x** | n/m (~breakeven) | n/a (barely profitable earlier) | rich |
| P / FCF | **~75–100x** | n/m | ___ | rich |
| P / E (GAAP, est.) | **~100x+** | n/m (net loss) | n/a | growth multiple |

> **The ~9x vs ~1x gap** between Rover and Wag! is a market-priced *moat signal* — Rover's leadership, profitability and growth vs. Wag!'s shrinking, breakeven, net-debt business. But it also means the premium was already in the price: at ~9x sales, $11 offered **no margin of safety**. See `deal-benchmark-and-peers.md` for the full peer read.

---

## 5. Intrinsic Value Range & Buy Price

| | Value |
|---|-------|
| Intrinsic value range (low–high) | $___ – $___ |
| Point estimate (base case) | $___ |
| Margin of safety applied | ___% (suggest 30–40%: short track record) |
| **Your buy price (would buy below this)** | **$___** |

---

## 6. The "$11 Test" — grading against reality

| Question | Answer |
|----------|--------|
| Blackstone's price | **$11.00** (~$2.3B equity, ~$2.07B EV) |
| Your conservative intrinsic value | $___ (model in §2) |
| Your base intrinsic value | $___ |
| Premium $11 paid over undisturbed price | **~30%+** (undisturbed ≈ $8.4) |
| **Was $11 a bargain / fair / rich vs. intrinsic value?** | Draft: **fair-to-rich** — a growth/PE price, not a value price on current cash flow |
| Would you have bought *below* $11 during 2022–2023? At what price? | Likely yes in the **2022 lows (~$3–5)** with a margin of safety; harder to justify near $8–11 |
| What did the bankers conclude vs. yours? | **Goldman DCF $7.87–$11.41; Centerview DCF $7.40–$11.25; comps $6.55–$9.25 (rev) & $8.45–$10.25 (EBITDA)**. $11 sits at/above the top of every method — confirms "full-to-rich." See `deal-benchmark-and-peers.md`. |

> **Interpreting the result:** that a top-tier buyer paid $11 confirms Rover generates *ownable, durable* cash flows — the moat is real enough for the smart money. But Blackstone underwrites leverage, cost synergies, and a multi-year hold to a bigger exit; a public value investor demanding a margin of safety on *today's* owner earnings would not have chased $11. **The value opportunity was the 2022 fear, not the 2024 buyout.** That gap — between "great business" and "great price" — is the whole lesson.

**One-paragraph conclusion:**

> ________________________________________________________________
> ________________________________________________________________
