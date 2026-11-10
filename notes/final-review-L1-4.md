# FINA 3080 — Final Exam Review, Part 1: Lectures 1–4

*Final exam: **Dec 1, 7–9 pm, LSK LT6** · **45%** of the grade · **cumulative***

> **How to use this sheet**
> 1. Go through the **concept checklist** (Section 1). For each line, say the answer out loud **without looking**. Anything you can't explain → reread that week's notes (`week0X-lectureX.md`).
> 2. Learn the **formula sheet** (Section 2) well enough to rewrite it from memory.
> 3. Read the **traps** (Section 3). These are where marks usually get lost.
> 4. Do the **practice problems** (Section 4) on paper with a calculator **before** opening the solutions.
>
> Lectures 1–5 were already tested on the midterm (Lecture 5 lists the midterm coverage as "Lecture 1 to 5"), so on the final Lectures 1–4 will most likely appear as **building blocks** inside bigger questions from later lectures. The most important carry-forward skills are the **two-asset portfolio math, Sharpe ratio, y\*, and the CAL**. They are the base for everything that follows (CAPM, index models, performance evaluation).

---

## 1. Concept checklist

### Lecture 1 — Investments, LOOP, efficiency, indexes
- [ ] Definition of an **investment**: commit resources **now**, expect **uncertain future** benefits.
- [ ] The HK$10,000 example: extra wealth is invested in the **same proportions** (50/30/20) → portfolio **weights** stay the same.
- [ ] **Diversification** reduces risk (Markowitz, Nobel 1990). Higher expected return ⇔ higher risk.
- [ ] **Law of One Price**: identical assets sell for the same price, **net of transaction costs**. Big Mac (non-tradable, big gaps) vs. iPad mini (tradable, small gaps) vs. cocaine (huge costs/risk of arbitrage).
- [ ] **Arbitrage** = **zero risk, zero net investment, positive profit**. Buy low/sell high → prices **converge** → profit disappears.
- [ ] **Efficient market**: prices reflect **all available information** (HSBC $60 → $100 example).
- [ ] **Luck vs. skill**: the coin-flip mailing (143 → 72 → 36 → 18 people see a "perfect" record by pure chance).
- [ ] Why indexes exist: track average performance, **benchmark managers**, **base for derivatives**.
- [ ] Kinds of indexes: stock/bond, narrow/broad, large/small cap, general/sector, country/regional.
- [ ] **Value-weighted index** formula; it reflects **buy-and-hold** and is **unaffected by stock splits**; mega-caps dominate it.
- [ ] HSI (~80 blue chips, narrow) vs. HSCI (~500 stocks, broad, the parent universe).

### Lecture 2 — Markets, trading, margin, short selling, returns
- [ ] **Real assets** (land, buildings, machines, human capital) vs. **financial assets** (claims on real assets).
- [ ] **Direct** financing (investment banks) vs. **indirect** financing (banks, insurers, mutual funds).
- [ ] **Primary** market (new issues, IPO) vs. **secondary** market (existing securities, exchanges).
- [ ] Four **functions** of financial markets: capital allocation, consumption timing, risk management, separation of ownership and management.
- [ ] Classification tree: marketable (primitive: debt/equity; derivatives: futures/options) vs. non-marketable (loans, mortgages, insurance); securitization.
- [ ] Four secondary market types: **direct search, brokered search, dealer, auction**.
- [ ] **Bid < Ask** always. You **buy at the ask, sell at the bid**. Spread = dealer's profit.
- [ ] Auction market = centralized → only **one** bid/ask pair at any moment.
- [ ] Order types: **market**, **limit buy** (below price), **limit sell** (above price), **stop-loss sell** (below price, you **hold** the stock), **stop-loss buy** (above price, e.g., to cover a short).
- [ ] **Margin** = equity / market value. Initial vs. maintenance margin; **margin call**.
- [ ] Margin magnifies returns **up and down**: ROE = stock return / margin (no interest).
- [ ] **Short selling**: borrow → sell → buy back later. Proceeds stay in the account + collateral. Loss is **unlimited**.
- [ ] Short-selling "campaigns" (Muddy Waters, China MediaExpress).
- [ ] **HPR** = (P₁ − P₀ + D) / P₀. **Arithmetic average** of returns.
- [ ] **Expected** (forward-looking, population μ, σ²) vs. **realized** (backward-looking, sample R(r), s²).

### Lecture 3 — VaR, risk premium, utility, indifference, CAL
- [ ] **VaR** = 5th percentile of the return distribution. Normal: μ − 1.65σ. Historical: rank the returns and take the cut-off (either neighbour or their average).
- [ ] **Fat tails** → normal VaR **understates** risk; historical VaR makes **no distribution assumption**.
- [ ] **Risk premium** = E[r] − r_f (the reward for bearing risk).
- [ ] **Utility** U = E[r] − ½Aσ² = **certainty equivalent**. Invest in the risky asset iff U > r_f.
- [ ] A > 0 risk averse (upward-sloping indifference curves); A = 0 risk neutral (flat); A < 0 risk loving (downward).
- [ ] **Mean–variance criterion**: for risk-averse investors, **northwest** is better. Northeast/southwest moves are ambiguous (they depend on A).
- [ ] **Lotteries**: same σ, different **skewness** → mean–variance can't explain them.
- [ ] Three **levels** of allocation: capital allocation (y), asset allocation within risky (P\*), security selection.
- [ ] Complete portfolio: E(r_C) = r_f + y[E(r_P) − r_f], σ_C = yσ_P; the CAL; the **Sharpe ratio**.
- [ ] US Fed hike → HK follows because of the **Linked Exchange Rate System** (7.75–7.85 peg).

### Lecture 4 — Markowitz
- [ ] **y\* = [E(r_P) − r_f] / (Aσ_P²)**, derived from the first-order condition. y\* is never negative.
- [ ] **r_b > r_f**: kinked CAL. Procedure y\* → y\*\* → possibly the corner y = 1.
- [ ] Optimum = **tangency of the indifference curve and the CAL**.
- [ ] Two-asset E(r_P) and σ_P²; **covariance = ρσσ**.
- [ ] ρ = 1 → no diversification benefit; ρ < 1 → σ_P below the weighted average; ρ = −1 → zero-risk portfolio possible.
- [ ] **Minimum-variance portfolio**; **efficient frontier** = part of the opportunity set above it.
- [ ] **P\*** = tangency portfolio = **maximum Sharpe ratio**; same for every investor (**separation**).
- [ ] C\* breakdown: (1 − y\*) risk-free, y\*·w_D\* bonds, y\*·w_E\* stocks.
- [ ] PMI > 50 expansion; "good news can be bad for stocks" (strong economy → rate fears).

---

## 2. Master formula sheet (Lectures 1–4)

| Topic | Formula | Notes |
|---|---|---|
| Value-weighted index | I_t = Σ(Q_it·P_it) / Σ(Q_i0·P_i0) × 100 | Unaffected by splits |
| Margin (long) | (MV − Loan) / MV | |
| Margin-call price (long) | P = Loan / [N(1 − M)] | M = maintenance margin |
| Margin (short) | (Assets − N·P) / (N·P) | Assets = sale proceeds + collateral |
| Margin-call price (short) | P = Assets / [N(1 + M)] | |
| Levered ROE | (End equity − Start equity) / Start equity | = r / margin with no interest |
| HPR | (P_t − P_{t−1} + D_t) / P_{t−1} | |
| Arithmetic mean | Σr_t / n | |
| Geometric mean ▶ | [Π(1 + r_t)]^{1/n} − 1 | ≤ arithmetic |
| Scenario E[r] | Σ p(s)·r(s) | |
| Scenario variance | Σ p(s)·[r(s) − E[r]]² | |
| Sample variance ▶ | Σ(r_t − r̄)² / (n − 1) | |
| VaR (5%, normal) | μ − 1.65σ | 1%: μ − 2.33σ ▶ |
| Risk premium | E[r] − r_f | |
| Utility / CE | U = E[r] − ½Aσ² | Use **decimals** |
| Indifference curve | E[r] = U + ½Aσ² | |
| Complete portfolio | E(r_C) = r_f + y[E(r_P) − r_f], σ_C = yσ_P | |
| Sharpe ratio | S = [E(r_P) − r_f] / σ_P | Slope of the CAL |
| CAL | E(r_C) = r_f + S·σ_C | |
| Optimal y | y\* = [E(r_P) − r_f] / (Aσ_P²) | |
| Two-asset return | w_D E(r_D) + w_E E(r_E) | |
| Two-asset variance | w_D²σ_D² + w_E²σ_E² + 2w_Dw_E ρσ_Dσ_E | |
| Min-variance weight ▶ | w_E = (σ_D² − σ_DE)/(σ_D² + σ_E² − 2σ_DE) | |
| Tangency weight ▶ | w_D\* = (R_Dσ_E² − R_Eσ_DE) / [R_Dσ_E² + R_Eσ_D² − (R_D + R_E)σ_DE] | R = excess return |

▶ = not on the slides (textbook), but useful.

---

## 3. Common traps (where people lose marks)

1. **Percent vs. decimal in utility.** U = 0.22 − ½(3)(0.34)² = 0.0466. **Do not** compute 22 − ½(3)(34)² = −1712. Always use decimals in U and y\*.
2. **y\* uses variance, not σ.** y\* = 0.08 / (4 × **0.0484**), not 4 × 0.22.
3. **Covariance vs. correlation.** If the question gives ρ, multiply: σ_DE = ρσ_Dσ_E. Don't put ρ straight into the variance formula.
4. **Don't forget the factor 2** in the cross term 2w_Dw_Eσ_DE.
5. **Portfolio σ is not the weighted average of σ's** (unless ρ = 1). Portfolio E(r) **is** always the weighted average.
6. **Short margin-call price uses (1 + M)**; long uses (1 − M). Short "assets" = proceeds **plus** collateral.
7. **Levered ROE is measured on your own equity**, and loan interest comes **out** of the gain.
8. **Bid/ask from your side:** you buy at the (higher) ask and sell at the (lower) bid.
9. **Stop-loss sell vs. limit sell:** stop-loss sell triggers when the price **falls** (protects a long position); limit sell triggers when the price **rises** (takes profit).
10. **Historical VaR rank:** 5% of n observations. With n = 100, the cut-off is between the 95th and 96th best (= 5th and 6th worst). Any of the two, or their average, is accepted.
11. **r_b > r_f:** only recompute if y\* > 1. If y\* > 1 but y\*\* ≤ 1, the answer is **y = 1**, not y\*\*.
12. **Complete portfolio weights** must add to 100%: risk-free + y\*·w_D\* + y\*·w_E\*.
13. **The min-variance portfolio is not the optimal risky portfolio.** P\* maximizes the **Sharpe ratio**.
14. **Expected vs. realized:** μ, σ² = population (forward-looking); r̄, s² = sample (backward-looking).
15. **Lecture 4 slide 21 rounding:** exact E(r_C\*) = 10.31%, σ_C\* = 9.09% (the slide prints 10.28%/9.02%). Trust your formula and show working.

---

## 4. Practice problems (exam style)

All of these are new problems, different from the self-tests in the weekly notes. Answers are in Section 5.

**P1. Value-weighted index.** An index has two stocks and a base value of 100.
| Stock | Shares | P₀ | P₁ |
|---|---|---|---|
| A | 100 | $10 | $12 |
| B | 50 | $40 | $38 |

(a) Compute the index at t = 1. (b) What is the index return, and how does it compare with the simple average of the two stock returns? Why? (c) Stock A then has a 2-for-1 split. What happens to the index?

**P2. Margin with interest.** You buy 400 shares at $50 with 60% initial margin. Maintenance margin is 30%. The broker charges 5% interest per year on the loan.
(a) How much do you borrow? (b) Below what price do you get a margin call (ignore interest)? (c) One year later the price is $55 and the stock paid a $1 dividend. What is your return on equity? (d) Compare with the unlevered return.

**P3. Short selling.** You short 500 shares at $80. Initial margin is 50% (posted in T-bills); maintenance margin is 25%.
(a) Above what price do you get a margin call? (b) The price falls to $60 and you cover. The stock paid a $2 dividend while you were short. What is your profit and your return on equity?

**P4. Order types.** A stock's bid is $99.90 and ask is $100.10. Which order would you use in each case, and at about what price would it be executed?
(a) You want to buy right now. (b) You own the stock and want to sell automatically if it falls to $95. (c) You own the stock and want to sell if it rises to $110. (d) You are short and want protection if the price rises to $105.

**P5. Returns.** A stock returns +15%, −10% and +8% over three years.
(a) Arithmetic average? (b) ▶ Geometric average? (c) Which one tells you the actual growth of $1?

**P6. Prospect, risk premium, utility.** You invest $100 today. With probability 70% it is worth $125 in a year; with probability 30% it is worth $85. r_f = 4%.
(a) E[r], σ, and the risk premium. (b) Utility for A = 3. Does this investor invest? (c) What is the **largest** A at which an investor would still choose the risky prospect?

**P7. VaR.** (a) Monthly returns are normal with μ = 1% and σ = 4%. Find the 5% VaR and the dollar VaR on HK$500,000. (b) You have 40 monthly observations. The five worst, in order, are −12%, −9%, −7%, −6%, −5.5%. What is the 5% historical VaR?

**P8. Complete portfolio and the kinked CAL.** E(r_P) = 14%, σ_P = 25%, r_f = 4%.
(a) Sharpe ratio. (b) For A = 3: y\*, E(r_C), σ_C, and U. (c) For A = 1.5: y\*. (d) Still A = 1.5, but you can borrow only at r_b = 6%. What do you do? (e) Same, with r_b = 4.5%.

**P9. Full Markowitz problem.** Two risky funds and a T-bill:
| | Bond fund D | Stock fund E |
|---|---|---|
| E(r) | 6% | 12% |
| σ | 10% | 30% |

ρ_DE = 0, r_f = 3%, A = 5, wealth = $100,000.
(a) E(r) and σ of a 50/50 portfolio. (b) The minimum-variance portfolio: weights, E(r), σ. (c) The tangency weights are w_D\* = 75%, w_E\* = 25% (check with the formula if you like). Find E(r_P\*), σ_P\*, and its Sharpe ratio. Compare with the Sharpe ratios of D and E alone. (d) y\*, and the dollar amount in T-bills, D and E. (e) E(r_C\*), σ_C\*, U. (f) Compare C\* with the minimum-variance portfolio from (b). What do you notice?

**P10. Conceptual short answers.**
(a) Explain why two investors with different A hold the same P\*.
(b) Why can't y\* be negative?
(c) Why does the HSI index react strongly to a few stocks like Tencent or HSBC?
(d) A fund manager has beaten the market 5 years in a row. Is that evidence of skill?
(e) Why might a strong PMI report make stocks fall?
(f) Give one reason the Big Mac price gap is not an arbitrage opportunity.
(g) True or false: "Adding a stock with higher σ than every stock you already own always raises portfolio risk." Explain.

---

## 5. Solutions

<details>
<summary><b>P1</b></summary>

(a) Base value = 100×10 + 50×40 = 3,000. Value at t = 1 = 100×12 + 50×38 = 1,200 + 1,900 = 3,100.
I₁ = 3,100 / 3,000 × 100 = **103.33**.
(b) Index return = **3.33%**. Simple average = (20% + (−5%))/2 = **7.5%**. They differ because the index is **value-weighted**: B is 2/3 of the starting value, so its −5% counts twice as much as A's +20%. Check: (1/3)(20%) + (2/3)(−5%) = 3.33% ✓.
(c) After the split, A has 200 shares at $6, worth $1,200 → total value unchanged → index stays **103.33**. Value-weighted indexes are **unaffected by splits**.
</details>

<details>
<summary><b>P2</b></summary>

(a) Position = 400 × $50 = $20,000. Equity = 60% = $12,000. **Loan = $8,000**.
(b) P = Loan / [N(1 − M)] = 8,000 / (400 × 0.7) = **$28.57**.
(c) End value of stock = 400 × 55 = $22,000, plus dividends 400 × $1 = $400 → $22,400. Repay loan with interest 8,000 × 1.05 = $8,400. End equity = **$14,000**.
ROE = (14,000 − 12,000) / 12,000 = **16.67%**.
(d) Unlevered return = (55 − 50 + 1)/50 = **12%**. Leverage raised the return, but by less than 12%/0.6 = 20%, because the 5% interest cost reduced it.
</details>

<details>
<summary><b>P3</b></summary>

(a) Proceeds = 500 × 80 = $40,000. Collateral = 50% × 40,000 = $20,000. Assets = **$60,000**.
P = 60,000 / [500 × (1 + 0.25)] = **$96**.
(b) Profit on price = 500 × (80 − 60) = $10,000. The short seller **pays** the dividend to the lender: 500 × 2 = $1,000. Profit = **$9,000**.
ROE = 9,000 / 20,000 = **45%**. (The dividend payment is ▶ textbook detail; the slides ignore dividends.)
</details>

<details>
<summary><b>P4</b></summary>

(a) **Market buy** → executed at the **ask, $100.10**.
(b) **Stop-loss sell** at $95 → becomes a market sell when the price hits $95.
(c) **Limit sell** at $110 → executes only at $110 or higher.
(d) **Stop-loss buy** at $105 → buys back (covers the short) if the price rises to $105.
</details>

<details>
<summary><b>P5</b></summary>

(a) (15 − 10 + 8)/3 = **4.33%**.
(b) (1.15 × 0.90 × 1.08)^{1/3} − 1 = (1.1178)^{1/3} − 1 = **3.78%**.
(c) The **geometric** average: $1 grows to 1.0378³ = $1.1178. The arithmetic average overstates growth when returns are volatile.
</details>

<details>
<summary><b>P6</b></summary>

(a) Returns: +25% (p = 0.7), −15% (p = 0.3).
E[r] = 0.7(25%) + 0.3(−15%) = 17.5% − 4.5% = **13%**.
σ² = 0.7(0.25 − 0.13)² + 0.3(−0.15 − 0.13)² = 0.7(0.0144) + 0.3(0.0784) = 0.01008 + 0.02352 = **0.0336** → σ = **18.33%**.
Risk premium = 13% − 4% = **9%**.
(b) U = 0.13 − ½(3)(0.0336) = 0.13 − 0.0504 = **7.96%** > 4% → **invest** in the risky prospect.
(c) Set U = r_f: 0.13 − ½A(0.0336) = 0.04 → A = 0.09 / 0.0168 = **5.36**. Any investor with A < 5.36 prefers the risky prospect.
</details>

<details>
<summary><b>P7</b></summary>

(a) VaR = 1% − 1.65 × 4% = **−5.6%**. Dollar VaR = 5.6% × 500,000 = **HK$28,000**: in 5% of months, you lose HK$28,000 or more.
(b) 5% × 40 = 2 observations lie in the tail. The cut-off is between the 2nd worst (−9%) and the 3rd worst (−7%). VaR = **−9%, −7%, or the average −8%** (all accepted by the slide's convention).
</details>

<details>
<summary><b>P8</b></summary>

(a) S = (14 − 4)/25 = **0.40**.
(b) y\* = 0.10 / (3 × 0.0625) = **0.5333**.
E(r_C) = 4% + 0.5333 × 10% = **9.33%**. σ_C = 0.5333 × 25% = **13.33%**.
U = 0.0933 − ½(3)(0.1333²) = 0.0933 − 0.0267 = **6.67%**.
(c) y\* = 0.10 / (1.5 × 0.0625) = **1.0667** → wants to borrow.
(d) y\*\* = (0.14 − 0.06) / (1.5 × 0.0625) = 0.08/0.09375 = **0.853 < 1**. Wants to borrow at 4% but not at 6% → **y = 1**: 100% in P, no borrowing, no lending (the kink).
(e) y\*\* = (0.14 − 0.045) / 0.09375 = **1.013 > 1** → borrow at 4.5% and put **101.3%** in P.
</details>

<details>
<summary><b>P9</b></summary>

Useful numbers: σ_D² = 0.01, σ_E² = 0.09, σ_DE = 0 (since ρ = 0).

(a) E(r) = 0.5(6%) + 0.5(12%) = **9%**. σ² = 0.25(0.01) + 0.25(0.09) = 0.025 → σ = **15.81%**.

(b) w_E = (0.01 − 0)/(0.01 + 0.09 − 0) = **0.10**, w_D = **0.90**.
E(r) = 0.9(6%) + 0.1(12%) = **6.6%**. σ² = 0.81(0.01) + 0.01(0.09) = 0.009 → σ = **9.49%**.

(c) Tangency check: R_D = 0.03, R_E = 0.09.
w_D\* = (0.03 × 0.09 − 0) / (0.03 × 0.09 + 0.09 × 0.01 − 0) = 0.0027/0.0036 = **0.75** ✓.
E(r_P\*) = 0.75(6%) + 0.25(12%) = **7.5%**.
σ²_P\* = 0.5625(0.01) + 0.0625(0.09) = 0.005625 + 0.005625 = **0.01125** → σ = **10.61%**.
S_P\* = (7.5 − 3)/10.61 = **0.424**. Compare: S_D = (6 − 3)/10 = 0.30 and S_E = (12 − 3)/30 = 0.30. Diversification raises the Sharpe ratio above **either** asset alone.

(d) y\* = (0.075 − 0.03) / (5 × 0.01125) = 0.045 / 0.05625 = **0.80**.
- T-bills: 20% → **$20,000**
- Bond fund: 0.80 × 75% = 60% → **$60,000**
- Stock fund: 0.80 × 25% = 20% → **$20,000**

(e) E(r_C\*) = 3% + 0.8 × 4.5% = **6.6%**. σ_C\* = 0.8 × 10.61% = **8.49%**.
U = 0.066 − ½(5)(0.01125 × 0.64) = 0.066 − 0.018 = **4.8%** (> r_f = 3%).

(f) C\* has the **same expected return (6.6%)** as the minimum-variance portfolio but **lower risk (8.49% vs. 9.49%)**. Mixing the max-Sharpe portfolio P\* with T-bills beats every risky-only portfolio, even the minimum-variance one. That is why the CAL through P\* dominates.
</details>

<details>
<summary><b>P10</b></summary>

(a) P\* depends only on asset expected returns, risks, correlations and r_f, which are the same for everyone. It maximizes the slope of the CAL. A only decides **where on the CAL** you sit (y\*). This is the **separation** property.
(b) If E(r_P) > r_f, a negative y gives E(r_C) < r_f while still carrying risk. A risk-averse investor would do better holding only the risk-free asset.
(c) The HSI is **value-weighted**, so the largest market-cap stocks have the biggest weights (Lecture 4 slide 6: "a few mega-caps move the whole index").
(d) Not necessarily. Among many managers, some will have 5 good years by **luck** alone (with 1,000 managers flipping coins, about 1000/2⁵ ≈ 31 would). We need to **separate luck from skill**.
(e) Strong economy → markets expect the Fed to **raise rates** → higher discount rates/borrowing costs → bond **and** stock prices fall.
(f) A Big Mac is not tradable: shipping and perishability costs exceed the price gap. The LOOP holds **net of transaction costs**.
(g) **False.** What matters is the **covariance** with the existing portfolio. A high-σ asset with low or negative correlation can **reduce** portfolio risk (for example, with ρ = −1 you can even reach zero risk).
</details>

---

## 6. Coming next

Part 2 (`final-review-L5-7.md`) covers **Lectures 5–7**: CAPM, APT, performance evaluation, funds and the EMH. Lectures 6–7 were not on the midterm, so they get the most emphasis.
