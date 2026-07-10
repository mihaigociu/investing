# Valuation Worksheet — Cognizant

Keep three scenarios throughout: **Bear / Base / Bull.** Buffett's discipline, inverted for a cheap stock: here the danger isn't needing the *optimistic* case to justify the price — it's that the *bear* case (structural AI-driven decline) may be the real one, so **the reverse-DCF and the bear case get done first.**

> **Status:** populated with FY2025 actuals from `financials-actuals.md`. Do the math yourself before trusting any figure.

**Anchor numbers:** FY2025 revenue **$21.108B**, GAAP operating income **$3.389B** (16.1% margin), adjusted EPS **$5.28**, GAAP EPS **$4.56**, FCF **$2.665B**, SBC **$181M** (10-K-exact, ~0.9% of revenue), owner earnings ~**$2.48B (~$5.24/sh)**, net cash ~**$1.34B**, diluted shares ~**474M**, price **~$43** (market cap ~$20.4B, EV ~$19.0B). FY2026 guide: revenue +4–6.5% cc, adj EPS **$5.56–5.70**.

---

## 1. Normalized Owner Earnings

```
Owner Earnings = Net Income (GAAP)
               + Depreciation & Amortization
               + Other non-cash charges
               − Stock-Based Compensation        ← treat SBC as a REAL cost
               − Maintenance Capex                ← small (~1% of revenue)
               ± Normalized working-capital change
```

Easiest build for CTSH is top-down from FCF (which already nets capex and working capital), then subtract SBC:

| Line (FCF bridge, FY2025) | Bear | Base | Bull |
|------|-----:|-----:|-----:|
| Free cash flow | 2,665 | 2,665 | 2,665 |
| − Stock-based comp (10-K actual $181M) | (181) | (181) | (181) |
| ± Normalized working capital | (75) | 0 | +25 |
| **= Owner earnings ($M)** | **~2,409** | **~2,484** | **~2,509** |
| ÷ Diluted shares (M) | 474 | 474 | 474 |
| **Owner earnings / share** | **~$5.08** | **~$5.24** | **~$5.29** |

> **Punchline:** current owner earnings ~$2.4–2.5B (~$5.1–5.3/share). Against ~$43 that's **~8.2x owner earnings / ~12% owner-earnings yield.** CTSH is cheap *on today's cash flow.* Rover was ~100x+; this is the mirror image. The SBC line is small — actual 10-K SBC is only **$181M (~0.9% of revenue)**, far cleaner than Rover's ~10%-of-revenue SBC — a genuine earnings-quality point. The valuation question is entirely about the **trajectory** of these earnings, handled next.

---

## 2. Reverse DCF — *do this one FIRST; it's the most honest*

Don't forecast. Ask: **what does ~$43 already assume?**

Setup:
- Enterprise value ≈ market cap $20.4B − net cash $1.34B ≈ **$19.0B**.
- Owner earnings / FCF ≈ **$2.5–2.7B** → **EV/FCF ≈ ~7.1–7.6x** → FCF yield ≈ **~13%**.

A perpetuity is worth `FCF ÷ (discount rate − growth)`. Solve for the growth the price implies:

| Discount rate (r) | EV/FCF at $43 | Implied perpetual growth `g = r − FCF/EV` |
|---:|---:|---:|
| 9% | ~7.3x | **≈ −4.7%/yr** |
| 10% | ~7.3x | **≈ −3.7%/yr** |
| 11% | ~7.3x | **≈ −2.7%/yr** |

> **The single most important finding of this whole analysis:**
> **At ~$43, the market is pricing Cognizant's cash flow to *decline* roughly 3–5% per year, forever.** You do not need growth to make money. You need the decline to be *milder* than that — flat is a win, and any growth is a large win.
>
> That reframes the buy/wait decision entirely. The bull doesn't have to argue "AI is no threat." The bull only has to argue "the labor model won't shrink faster than ~4%/yr." The bear has to argue it will shrink *faster* — which, per the insider ("already cannibalizing," "price-squeezed"), is a live possibility, not a strawman.

**Judgment to write in your own words after stress-testing:** Is a >4%/yr perpetual decline more or less likely than flat-to-slightly-growing, given (a) bookings/book-to-bill still ~1.3x, (b) headcount still growing, (c) net cash + buybacks shrinking the share count ~3%/yr — *against* (d) real AI cannibalization of billable hours and (e) eroding pricing power? ________________________________________.

---

## 3. Discounted Cash Flow — three scenarios

10-year owner-earnings DCF, discounted at **10%** (above a blue-chip rate, to price real disruption risk). Per-share adds net cash and divides by a *shrinking* share count (buybacks). Rough outputs:

| Input | Bear | Base | Bull |
|-------|------|------|------|
| Starting owner earnings ($M) | 2,484 | 2,484 | 2,484 |
| Yr 1–5 growth | **−6%** | **0%** | **+4%** |
| Yr 6–10 growth | **−4%** | **+1%** | **+4%** |
| Terminal growth | **−3%** | **+1%** | **+2.5%** |
| Discount rate | 10% | 10% | 10% |
| Buyback share shrink | ~1%/yr | ~2.5%/yr | ~3%/yr |
| **≈ Intrinsic value / share** | **~$30–35** | **~$50–55** | **~$65–75** |

**Interpretation:**
- **Bear (~$30–35):** AI structurally deflates the labor model; revenue and margin grind down; buybacks can't outrun the decline. At ~$43 you'd be *overpaying*. This is the value trap, and it is *not* a strawman — the insider evidence keeps it alive.
- **Base (~$50–55):** the turnaround holds the line at roughly flat-to-tiny-growth; AI is a wash (cannibalization offset by new AI-build demand); buybacks + dividend compound. At ~$43 you're paying ~80% of fair value — modestly undervalued, ~15–20% upside plus a 3% yield.
- **Bull (~$65–75):** the +7% 2025 growth proves durable, margins expand toward peers as AI lifts productivity, and Cognizant is a *net winner* of the AI transition (clients pay it to build their AI). ~$43 is deeply undervalued. (Matches the sell-side "$67 by 2028" case.)

The spread ($30 to $75) is enormous — which is *honest*. It reflects that the AI question is genuinely unresolved. A tight intrinsic-value estimate here would be false precision.

---

## 4. Multiples Cross-Check (at ~$43)

| Multiple | CTSH @ $43 | CTSH 10-yr median | Peers (2026) | Verdict |
|----------|-----------:|------------------:|:---|---|
| P/E (adjusted) | **~8.1x** | ~18x | ~low-teens to mid-teens | cheap, cheapest of majors |
| P/FCF | **~7.7x** | ~18x | — | ~56% below own history |
| EV/Revenue | **~0.9x** | ~2x | ~1–3x | cheap |
| EV/adj-EBIT | **~5.7x** | — | — | cheap |
| Dividend yield | **~3.0%** | ~1.5% | — | ~2x normal — paid to wait |

> Every lens says the same thing: **cheap on the past.** But "cheap vs. its own history" assumes the future rhymes with the past — the exact assumption AI puts in doubt. Multiples confirm the setup; they do not resolve it. See `peers-and-benchmark.md` for why analyst targets anchored to these historical multiples are unreliable here.

---

## 5. Intrinsic Value Range & Buy Price

| | Value |
|---|-------|
| Intrinsic value range (bear–bull) | **$30 – $75** |
| Point estimate (base case) | **~$52** |
| Margin of safety demanded | **35–40%** (narrow/eroding moat + management-honesty flag + structural, not cyclical, threat) |
| **Buy price (would buy below this)** | **~$32–34** |
| Current price | **~$43** |

**Why such a wide margin of safety?** Buffett widens the required discount when the range of outcomes is wide and the downside is structural. Here all three risk amplifiers are present: (1) the moat is narrow and eroding (volume sticky, price not); (2) management honesty/owner-orientation is flagged by the insider; (3) the threat is *structural* (AI deflating the model), not merely *cyclical* (a passing budget freeze). A cyclical dip you buy at a 20% discount; a structural threat you demand 35–40% or you pass.

**So at ~$43:** the stock is **below the base case (~$52) but above the margin-of-safety buy price (~$32–34).** In plain terms — **cheap, but not yet a margin of safety.**

---

## 6. The Live Decision — Buy Now, Wait, or Avoid?

This replaces Rover's retrospective "$11 test" with the real, forward question.

| Question | Answer |
|----------|--------|
| Is CTSH cheap on current cash flow? | **Yes** — ~8x FCF, ~13% owner-earnings yield, net cash, ~3% dividend, buying back ~3%/yr. |
| Does ~$43 offer a *margin of safety*? | **Not a wide one.** It's below base-case fair value (~$52) but above the ~$32–34 buy price a narrow/eroding moat + management flag demand. |
| What does the price already assume? | **~3–5%/yr perpetual decline.** You win unless the business declines faster than that. |
| Does the insider evidence make faster decline likely? | **It's a live risk.** "Already cannibalizing" billable hours + "price-squeezed" pushes toward the bear case; but bookings ~1.3x and growing headcount push back. |
| Is the drop fundamental or technical/sentiment? | **Mostly sector + sentiment + forced index-removal selling** — which argues part of it is overshoot (opportunity), but the peers are cheap for a *shared real reason* (caution). |

### The verdict: **WAIT / buy only small — do not back up the truck at $43.**

The reverse-DCF says a lot of bad news is already in the price, so this is *not* an expensive stock and *not* an obvious "sell/avoid." But three things stop it from being a full-size buy today: the moat is narrow and eroding, you (the insider) don't trust management's orientation, and the thesis-defining variable (does AI turn slowing growth into real decline?) is *unresolved* — and your own inside read leans toward the risk being real. Waiting is cheap (you forgo ~3% yield), and the downside scenario (low $30s) is live.

### A staged / tranche plan (act on *price* OR *evidence*, whichever comes first)

| Tranche | Trigger | Rationale |
|---|---|---|
| **Starter (~1/4 position)** | Optional, now, ~$43 | Only if you want skin in the game; sized so a fall to the low $30s doesn't hurt and lets you average down. Skip it entirely if you'd rather wait for confirmation. |
| **Add (~1/2 position)** | Price into **low $30s** (near/below the ~$32–34 buy price and the ~$37 52-wk low) **OR** 2–3 quarters of *stable organic revenue + stable pricing + book-to-bill ≥1.0* | Either the price gives you the margin of safety, or the fundamentals demonstrably survive the AI transition and de-risk the thesis. |
| **Full position** | Both a sub-$35 price *and* evidence the revenue line is holding | Buy aggressively only when cheap *and* de-risked — you rarely get both, so be patient. |

### Evidence that would flip WAIT → BUY (watch these quarterly)
- Organic constant-currency revenue **stays positive** through 2026–2027 (the AI headwind *not* winning).
- **Book-to-bill stays ≥1.0** and bookings growth holds.
- **Revenue-per-employee rising** while headcount flattens — sign AI is lifting productivity/margin rather than gutting revenue.
- Pricing/margin **stable or expanding** (not the "grind down" of "price-squeezed").
- Management candor on the AI threat improves; insider buying appears on Form 4; comp re-aligned to per-share value.

### Evidence that would flip WAIT → AVOID (get out of the way)
- Organic revenue turns to **sustained decline**; book-to-bill falls below 1.0.
- **Headcount shrinks while revenue falls faster** (deflation winning, not productivity).
- Margins compress despite cost cuts (pricing power gone).
- Attrition of top talent spikes (the "grumbling but staying" tips over).
- Buyback funded by balance-sheet stretch, or capital allocation turns self-serving.

**One-paragraph conclusion (write your own):**

> ________________________________________________________________
> ________________________________________________________________

---

## 7. A note on *your* specific situation (concentration risk)

You are a Cognizant **employee**, likely with CTSH exposure already (RSUs/ESPP) and — most importantly — your **salary** depends on the same company. Buying more stock **doubles down** the same risk: if the AI-disruption bear case plays out, your equity *and* your job/pay are hit together. A pure valuation buy/wait call ignores this; your personal risk management should not. Even if the analysis said "buy," prudent position-sizing for you is **smaller** than for an outside investor, precisely because you are already long Cognizant through your paycheck. That argument reinforces the "wait / buy only small" verdict independent of the stock analysis itself.
