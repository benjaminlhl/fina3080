# FINA 3080 — Final Exam Review, Part 2: Lectures 5–7

*Final exam: **Dec 1, 7–9 pm, LSK LT6** · **45%** · cumulative · closed book, bring a financial calculator*

> **Where the marks probably are**
> - **Lecture 5 (CAPM)** was the last lecture on the midterm. Its ideas (β, SML, α, systematic vs. unique risk) are the **language** of Lectures 6–7, so you need it cold.
> - **Lectures 6–7 were never examined.** Expect them to carry a big share of the final:
>   - the **APT arbitrage table** (Lecture 6),
>   - **Sharpe / Jensen / information ratio** and why they rank differently (Lectures 6–7),
>   - the **t-statistic of alpha** and "how many months" (Lecture 7),
>   - **fund types, NAV, fees** and the **three forms of the EMH** (Lecture 7).
>
> Same method as Part 1: checklist from memory → formula sheet → traps → practice problems on paper → check solutions.

---

## 1. Concept checklist

### Lecture 5 — Diversification and the CAPM
- [ ] "100 Rule" (stocks % = 100 − age); MPF **DIS**: CAF ≈ 60% risky, A65F ≈ 20% risky, de-risking automatically with age.
- [ ] σ_P² = σ²/n + [(n−1)/n]ρσ² → **ρσ² (average covariance)** as n → ∞.
- [ ] A stock's contribution to a diversified portfolio's risk depends on its **covariance, not its variance**.
- [ ] Total risk = **market** (systematic, nondiversifiable) + **unique** (firm-specific, idiosyncratic, diversifiable). Know all the synonyms.
- [ ] N risky assets: global minimum-variance portfolio, efficient frontier; the 3-step process (frontier → P\* via tangent CAL → C\* via indifference curve).
- [ ] **CAPM assumptions:** borrow/lend at r_f; mean–variance optimizers; homogeneous expectations.
- [ ] Why everyone holds the **market portfolio M** (the 50/30/20 example) → **passive investing is efficient**.
- [ ] **CML** (E(r) vs. σ, through M).
- [ ] Derivation idea: equal reward-to-risk [E(r_x) − r_f]/σ_Mx = [E(r_M) − r_f]/σ_M² → **CAPM**.
- [ ] **SML** (E(r) vs. β, slope = market risk premium, β_M = 1).
- [ ] **α > 0** above the SML → underpriced → **buy**; α < 0 → **sell**; α = 0 → hold.
- [ ] Two ways to estimate β: σ_iM/σ_M², or the **slope of the excess-return regression**.
- [ ] Dow-30 evidence: β vs. return is **weak** → "CAPM doesn't work well" → multifactor models.
- [ ] Fama–French: **market, SMB, HML**.
- [ ] Barber & Odean (2000): more trading → lower **net** returns.
- [ ] Market news: weak jobs report → lower hike odds → stocks **up**; HK/US timing difference.

### Lecture 6 — APT and performance evaluation
- [ ] Multifactor model; α = 0 in equilibrium.
- [ ] APT rests on **no-arbitrage**: riskless, zero-investment profit → everyone takes an **infinite** position → prices correct.
- [ ] Implications: high β → high E(r); firm-specific risk **not rewarded**; hold diversified portfolios.
- [ ] Portfolio α and β are **weighted sums**; σ²(e_P) uses **squared** weights.
- [ ] **Factor portfolio**: β = 1 on one factor, 0 on the others, σ²(e) = 0.
- [ ] Build the **arbitrage table**: weights sum to 0, betas sum to 0, profit = alpha.
- [ ] Why it fails for a **single stock** (exposure to e_A).
- [ ] **APT vs. CAPM** (4 differences).
- [ ] Two problems in evaluating funds: **adjust for risk** and **luck vs. skill** (octopus).
- [ ] **Sharpe** (total risk; for whole portfolio), **Jensen α** (vs. CAPM; manager skill), **information ratio** α/σ(e) (manager skill). They can **rank differently**.
- [ ] **Active Share** = 0.5Σ|w_fund − w_bench|; HK example: Corr(Active Share, α) = 0.69.
- [ ] Fees: expense ratio & 12b-1 (yearly), front-end load (buy), back-end load (sell); **performance doesn't persist**; active ~0.8–1.1% vs. passive ~0.1–0.27% expense ratio.

### Lecture 7 — Funds, luck vs. skill, EMH
- [ ] **Open-end** (mutual) funds: shares created/redeemed, priced at **NAV**, trade once a day at the close.
- [ ] **Closed-end** funds: fixed shares, **premium or discount** to NAV.
- [ ] **ETFs**: like mutual funds, mostly index trackers, **trade like stocks** all day. Tracker Fund 2800.HK (1999, tracks HSI).
- [ ] **Hedge funds**: private partnerships, less regulation, wealthy/institutional only, **short + leverage** (1.7–1.8), strategies list, **"2 and 20"**.
- [ ] Who owns US stocks: households largest, then mutual funds; pension funds "large but passive"; retail trading volume rising.
- [ ] Buffett's bet: S&P 500 fund **7.1%** vs. hedge funds **2.2%** a year over 10 years.
- [ ] **σ(α) = σ(e)/√N**, **t = α√N/σ(e)**, need t ≥ 1.96 → **384 months = 32 years** in the slide example.
- [ ] EMH: prices move only on **new (random) information** → **random walk**; immediate, complete response to news.
- [ ] Pre-FOMC drift evidence.
- [ ] **Weak** (historical) ⊂ **semi-strong** (all public) ⊂ **strong** (public + private) efficiency, with examples.

---

## 2. Formula sheet (Lectures 5–7)

| Topic | Formula |
|---|---|
| n-stock diversification | σ_P² = σ²/n + [(n−1)/n]ρσ² → ρσ² |
| CML | E(r_C) = r_f + [(E(r_M) − r_f)/σ_M]σ_C |
| Beta | β_i = σ_iM/σ_M² = ρ_iMσ_i/σ_M ▶ |
| CAPM / SML | E(r_i) = r_f + β_i[E(r_M) − r_f] |
| Alpha | α = forecast (or actual average) return − CAPM return |
| Single-index model | r_i − r_f = α_i + β_i(r_M − r_f) + e_i |
| Variance split ▶ | σ_i² = β_i²σ_M² + σ²(e_i) |
| Multifactor / APT | E(r_P) = r_f + Σβ_Pk[E(r_k) − r_f] |
| Portfolio α, β | Σw_iα_i, Σw_iβ_ik |
| Portfolio residual variance | Σw_i²σ²(e_i) |
| Arbitrage risk-free weight | −(Σβ − 1) when short 1 unit of the asset and long β_k of each factor portfolio |
| Sharpe | (r̄_P − r̄_f)/σ_P |
| Jensen's α | r̄_P − [r̄_f + β_P(r̄_M − r̄_f)] |
| Information ratio | α_P/σ(e_P) |
| Treynor ▶ | (r̄_P − r̄_f)/β_P |
| Active Share | 0.5Σ|w_j,i − w_b,i| |
| NAV | (Assets − Liabilities)/Shares |
| t-stat of α | α√N/σ(e); N = (1.96σ(e)/α)² |

---

## 3. Common traps

1. **CML vs. SML.** CML: x-axis **σ**, only efficient portfolios. SML: x-axis **β**, every asset. Don't plot a single stock on the CML.
2. **SML slope is E(r_M) − r_f**, **not** the Sharpe ratio. The CML's slope is the Sharpe ratio of M.
3. **Alpha sign → action.** Positive α = return too **high** = price too **low** = **buy**. Students often flip this.
4. **Beta from correlation:** β = ρσ_i/σ_M, not ρσ_M/σ_i, and not σ_iM/σ_M (forgot to square).
5. **Diversification limit is ρσ²**, a **variance**. Take the square root for σ.
6. **Residual variance of a portfolio uses w²**, but α and β use plain w.
7. **Arbitrage table:** the risk-free weight is whatever makes **total weight = 0**. If you're short the mispriced asset (−1) and long Σβ in factor portfolios, r_f weight = 1 − Σβ. Always show that weights **and** each β column sum to zero.
8. **Arbitrage only works for well-diversified portfolios.** For a single stock, say you're left with firm-specific risk.
9. **Which performance measure?** Whole portfolio → Sharpe. One of many funds → Jensen (or Treynor). Manager's active skill → information ratio.
10. **A positive α does not guarantee a better Sharpe ratio than the market** (see P5, fund C).
11. **t-stat units:** α and σ(e) must be in the **same period** (both monthly or both annual); N is then in that period.
12. **EMH form ordering:** strong ⇒ semi-strong ⇒ weak. Insider info = **strong**; public announcements/fundamentals = **semi-strong**; charts/past prices = **weak**.
13. **Open vs. closed-end:** only **closed-end** funds trade at a premium/discount; open-end funds transact **at NAV**.
14. **ETF vs. mutual fund trading:** ETFs trade intraday; mutual funds once a day at the closing NAV.
15. **"Bad news is good news":** weak jobs data → fewer rate hikes → stocks up. Strong PMI/CPI → more hikes → stocks down.

---

## 4. Practice problems (exam style)

**P1. Diversification.** Every stock has σ = 50%, and every pair has ρ = 0.3.
(a) σ of an equally weighted portfolio of 4 stocks. (b) The limit as n → ∞. (c) What fraction of the 4-stock portfolio's variance is still diversifiable?

**P2. CAPM, SML and alpha.** r_f = 4%, E(r_M) = 11%, σ_M = 20%.
| Stock | β | Analyst's forecast |
|---|---|---|
| P | 0.8 | 10.0% |
| Q | 1.3 | 12.5% |
| R | 1.0 | 11.0% |

(a) CAPM expected return and α of each stock. Buy, sell or hold?
(b) Beta and CAPM expected return of a portfolio with 50% P, 30% Q, 20% R.
(c) An investor with A = 3.5 holds only M and T-bills. Find y\*, E(r_C) and σ_C. On which line does this portfolio lie?

**P3. Beta and risk decomposition.** A stock has σ = 30% and correlation 0.6 with the market. σ_M = 20%.
(a) β. (b) Systematic variance, firm-specific variance and σ(e). (c) What fraction of total risk is systematic?

**P4. APT arbitrage.** Two-factor model. Factor portfolios: E(r_1) = 8%, E(r_2) = 6%. r_f = 2%. Well-diversified portfolio C has β_1 = 0.8, β_2 = 1.5 and expected return 10%.
(a) Fair APT return of C, and its α. (b) Build the arbitrage table (per $1 of C). (c) Profit if you short $1 million of C. (d) Would this be riskless if C were a single stock?

**P5. Performance evaluation.** r_f = 2%; market: r̄_M = 9%, σ_M = 16%.
| Fund | r̄ | σ | β | σ(e) |
|---|---|---|---|---|
| A | 12% | 22% | 1.3 | 9% |
| B | 10% | 14% | 0.8 | 6% |
| C | 15% | 30% | 1.5 | 15% |

(a) Sharpe, Jensen's α and information ratio for each fund (and the market's Sharpe). (b) Rank the funds on each measure. (c) Which would you pick if it were your **only** investment? If you add it to an already diversified portfolio? (d) ▶ Treynor measures. (e) Comment on fund C.

**P6. Luck or skill.** A manager's estimated alpha is 3% a year with σ(e) = 6% a year.
(a) How many years of data are needed for 95% confidence? (b) With 5 years of data, what is t? Conclusion?

**P7. Active Share.** Benchmark: S1 40%, S2 30%, S3 20%, S4 10%. Fund: S1 30%, S2 30%, S4 20%, S5 20%. Find the Active Share.

**P8. Funds.** (a) A closed-end fund has $500m of assets, $20m of liabilities and 30m shares. It trades at $14.40. Find NAV and the premium/discount. (b) Could an open-end fund with the same portfolio trade at $14.40? (c) A hedge fund with $200m earns 12% gross. Fees are "2 and 20" (20% on gross profit). What net return do investors get?

**P9. EMH.** Which form of the EMH (if any) is contradicted by each finding?
(a) Stocks that rose most over the past 6 months keep outperforming over the next 6 months.
(b) Corporate insiders earn abnormal returns trading their own company's stock.
(c) Prices keep drifting up for 60 days after good earnings announcements.
(d) The S&P 500 rises on average in the 24 hours **before** scheduled FOMC announcements.

**P10. Short answers.**
(a) Why is firm-specific risk not rewarded with higher expected returns?
(b) Give two reasons passive investing tends to beat active investing.
(c) If everyone indexed passively, would markets stay efficient? ▶
(d) Why did HK fall while the US rose on Oct 2?
(e) The 4 HK funds in Lecture 6 all had positive alpha. Should you invest in the one with the highest alpha? Give two caveats.

---

## 5. Solutions

<details>
<summary><b>P1</b></summary>

σ² = 0.25.
(a) σ_P² = 0.25/4 + (3/4)(0.3)(0.25) = 0.0625 + 0.05625 = 0.11875 → σ_P = **34.5%**.
(b) ρσ² = 0.3 × 0.25 = 0.075 → σ = **27.4%**.
(c) (0.11875 − 0.075)/0.11875 = **36.8%** of the variance can still be diversified away.
</details>

<details>
<summary><b>P2</b></summary>

(a) Market risk premium = 7%.
| Stock | CAPM E(r) | α | Action |
|---|---|---|---|
| P | 4 + 0.8(7) = **9.6%** | 10 − 9.6 = **+0.4%** | Underpriced → **buy** |
| Q | 4 + 1.3(7) = **13.1%** | 12.5 − 13.1 = **−0.6%** | Overpriced → **sell** |
| R | 4 + 1.0(7) = **11.0%** | **0** | Fairly priced → **hold** |

(b) β_P = 0.5(0.8) + 0.3(1.3) + 0.2(1.0) = **0.99**. CAPM E(r) = 4 + 0.99(7) = **10.93%**.
(c) y\* = 0.07 / (3.5 × 0.04) = **0.5**. E(r_C) = 4 + 0.5(7) = **7.5%**; σ_C = 0.5(20%) = **10%**. It lies on the **CML** (and, with β = 0.5, also on the SML: 4 + 0.5 × 7 = 7.5% ✓).
</details>

<details>
<summary><b>P3</b></summary>

(a) β = ρσ_i/σ_M = 0.6 × 0.30/0.20 = **0.9**.
(b) Systematic = β²σ_M² = 0.81 × 0.04 = **0.0324**. Total = 0.09. Firm-specific = 0.09 − 0.0324 = **0.0576** → σ(e) = **24%**.
(c) 0.0324/0.09 = **36%** (= ρ²). The other 64% is diversifiable.
</details>

<details>
<summary><b>P4</b></summary>

(a) Fair E(r_C) = 2 + 0.8(6) + 1.5(4) = 2 + 4.8 + 6 = **12.8%**. α = 10 − 12.8 = **−2.8%** → overpriced → **sell C**.
(b)
| Position | Weight | β₁ | β₂ | E(r) |
|---|---|---|---|---|
| C | −1 | −0.8 | −1.5 | −10% |
| FP1 | +0.8 | +0.8 | 0 | +6.4% |
| FP2 | +1.5 | 0 | +1.5 | +9% |
| r_f | −1.3 | 0 | 0 | −2.6% |
| **Total** | **0** | **0** | **0** | **+2.8%** |
r_f weight = −(0.8 + 1.5 − 1) = −1.3 (borrow).
(c) 2.8% × $1,000,000 = **$28,000**, with no risk and no net investment.
(d) **No.** You'd be short C's firm-specific risk (−e_C), so the profit isn't guaranteed.
</details>

<details>
<summary><b>P5</b></summary>

(a)
| | Sharpe | Jensen α | IR | ▶ Treynor |
|---|---|---|---|---|
| A | 10/22 = **0.455** | 12 − (2 + 1.3 × 7) = **0.9%** | 0.9/9 = **0.100** | 10/1.3 = 7.69 |
| B | 8/14 = **0.571** | 10 − (2 + 0.8 × 7) = **2.4%** | 2.4/6 = **0.400** | 8/0.8 = 10.0 |
| C | 13/30 = **0.433** | 15 − (2 + 1.5 × 7) = **2.5%** | 2.5/15 = **0.167** | 13/1.5 = 8.67 |
| Market | 7/16 = **0.4375** | 0 | — | 7.0 |

(b) Sharpe: **B > A > C**. Jensen: **C > B > A**. IR: **B > C > A**. (Treynor: B > C > A.) The rankings differ.
(c) Only investment → **Sharpe → B**. Adding to a diversified portfolio → **Jensen (or Treynor)**: Jensen picks C narrowly over B; Treynor picks B. For pure manager skill (IR), B.
(e) C has the **highest alpha**, yet its Sharpe ratio (0.433) is **below the market's (0.4375)**: its large firm-specific risk (σ(e) = 15%) makes it a poor stand-alone holding, even though it beats the CAPM.
</details>

<details>
<summary><b>P6</b></summary>

(a) N = (1.96 × 6/3)² = 3.92² = **15.4 years**.
(b) t = 3√5/6 = **1.12 < 1.96** → can't reject that the alpha is luck.
</details>

<details>
<summary><b>P7</b></summary>

|differences|: S1 0.10, S2 0, S3 0.20, S4 0.10, S5 0.20 → sum = 0.60. Active Share = **0.30**.
</details>

<details>
<summary><b>P8</b></summary>

(a) NAV = (500 − 20)/30 = **$16**. Discount = (14.40 − 16)/16 = **−10%**.
(b) **No.** Open-end funds are bought and redeemed **at NAV** ($16); only closed-end funds trade away from NAV.
(c) Gross profit = 12% × 200 = $24m. Management fee = 2% × 200 = $4m. Incentive fee = 20% × 24 = $4.8m. Net = 24 − 8.8 = $15.2m → **7.6%**.
</details>

<details>
<summary><b>P9</b></summary>

(a) Past prices predict returns (momentum) → contradicts **weak** form (and therefore semi-strong and strong).
(b) Private information earns profits → contradicts **strong** form only.
(c) Slow reaction to public news (post-earnings drift) → contradicts **semi-strong** form (and strong).
(d) A predictable pattern around **publicly scheduled** events → contradicts **semi-strong** form (some argue it's a risk premium, but it's hard to square with efficiency).
</details>

<details>
<summary><b>P10</b></summary>

(a) It can be diversified away **at no cost**. In equilibrium (CAPM/APT), investors are only paid for risk they **can't** avoid: systematic/factor risk.
(b) Few managers **consistently** beat the market (and it's hard to tell skill from luck); active management is **costly**: higher expense ratios, loads, trading costs (Barber & Odean; Buffett's bet).
(c) ▶ No. Someone must trade on information to keep prices efficient. Passive investors free-ride on active ones; if everyone were passive, mispricing would appear and active investing would become profitable again (the Grossman–Stiglitz paradox).
(d) **Timing.** The weak US jobs report came at 8:30 pm HKT, after HK closed (≈4:08 pm). During HK hours, oil and borrowing costs pushed the HSI down 2.6%; the US then rose 0.73% on lower Fed-hike odds.
(e) (1) **Luck vs. skill**: alphas of 2–3% need decades of data to be statistically significant. (2) **Performance doesn't persist**, and (3) **fees** (loads, expense ratios) reduce what you actually earn. Also the sample is only four funds.
</details>

---

## 6. Coming next
Upload the remaining lectures (8 onward, likely starting with **behavioral finance**) and any **practice problems / past papers / sample final**, and they'll be added as Part 3 along with weekly notes. Past papers are especially useful for matching the instructor's style.
