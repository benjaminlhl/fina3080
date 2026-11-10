# FINA 3080 — Week 5 Notes
## Lecture 5: The Capital Asset Pricing Model (CAPM) and multifactor models

*Investment Analysis and Portfolio Management · Instructor: Chao Ying (CUHK)*

> **How to read these notes:** everything in the main text comes from the slides. Parts marked **▶ Beyond the slides** are my own explanations and worked examples. They follow the optional textbook (BKM Ch. 7–10) but were not explicitly presented in lecture.

**Today's outline**
1. Diversification
2. Markowitz selection with N risky assets
3. The CAPM
4. Multifactor models

---

## 0. Recap, announcements and market update (slides 2–13)

### Recap: the portfolio choice steps (slide 4)
1. Start simple: **one risky and one risk-free asset**.
2. Combine many risky securities: **(a)** two risky securities give the optimal P\*; **(b)** with 3, 4, … securities you get further **benefits of diversification** (today's lecture).
3. Combine the risky securities with the risk-free asset: **draw the CAL tangent to the set of feasible risky portfolios**.
4. Choose your own portfolio given your risk aversion: treat P\* as one risky asset and go back to step 1 to get **C\***.

### Highest utility from the Lecture 4 example (slide 8)
$$U_C = r_f + y[E(r_P) - r_f] - \tfrac{1}{2}Ay^2\sigma_P^2 = 0.05 + 0.7439(0.06) - \tfrac{1}{2}(4)(0.7439^2)(0.020164) = \mathbf{7.23\%}$$

### Announcements (slides 9, 45)
- **Midterm: Oct 20, 7–9 pm, LSK LT6. Coverage: Lectures 1 to 5.** Closed book; bring a financial calculator. A sample exam, its solution and the **formula sheet** are on Blackboard.

### Market update: bad news, higher stock prices (slides 10–13)
- **Sep 28–Oct 2:** oil above $100 and falling bond prices → higher borrowing costs → pressure on stocks.
- **Oct 2, 8:30 am ET:** a surprisingly **weak US jobs report**: payrolls up only **29k** vs. **90k** expected.
  - This sharply **lowered expectations of another Fed hike**. Reuters put the probability of a Fed pause at about **80%**.
  - **Bad news for the economy can be good news for stocks.** (This is the mirror image of Lecture 4's strong PMI.)
- **Why did HK fall while the US rose on the same Friday? Timing.**
  - The US report came out at 8:30 am New York = **8:30 pm Hong Kong**, but HK closes around **4:08 pm HKT**.
  - During HK trading: oil + high global borrowing costs → **HSI −2.60%**.
  - Four hours after HK closed: the weak jobs report → fewer hike fears → **S&P 500 +0.73%**.

---

## 1. Diversification (slides 15–20)

### Rules of thumb (slides 15–16)
- **"The 100 Rule":** % of your portfolio in stocks = **100 − your age**.
- **The MPF Default Investment Strategy (DIS)** uses two mixed-asset funds:
  - **Core Accumulation Fund (CAF):** about **60%** in higher-risk assets (mainly global equities), 40% in lower-risk assets (mainly global bonds).
  - **Age 65 Plus Fund (A65F):** about **20%** in higher-risk assets, 80% lower-risk.
  - The trustee **automatically and gradually reduces** risky exposure as the member approaches retirement age.

### How far can diversification go? (slide 17)
- Combining risky securities lowers portfolio σ **if they are not perfectly correlated**.
- **Adding more securities strengthens this**: the efficient frontier **shifts left**.

### Portfolio risk and the number of stocks (slides 18–19)
Assume **n** securities, an **equally weighted** portfolio, every stock with the **same variance σ²** and the **same correlation ρ** with every other stock:
$$\sigma_P^2 = \frac{1}{n}\sigma^2 + \frac{n-1}{n}\rho\sigma^2$$
$$\lim_{n\to\infty}\sigma_P^2 = \rho\sigma^2 = \text{average covariance}$$

- The **first term** (own variances) **disappears** as n grows.
- The **second term** (covariances) **stays**. You can't diversify it away.
- **Key message: a stock's contribution to the risk of a well-diversified portfolio depends only on its covariance, not its variance.**

**The chart (slide 19):** portfolio σ vs. number of stocks.
| ρ | Diversification potential |
|---|---|
| 1.0 | **None** (σ_P stays at σ) |
| 0.5 | Some |
| 0.15 | **High** |

The part of risk that falls away is **diversifiable ("unique") risk**; the floor it approaches is **undiversifiable ("market") risk**.

> **▶ Beyond the slides: a worked example.** σ = 40%, ρ = 0.25 (σ² = 0.16).
>
> | n | σ_P |
> |---|---|
> | 1 | 40.0% |
> | 2 | 31.6% |
> | 5 | 25.3% |
> | 10 | 22.8% |
> | 25 | 21.2% |
> | 100 | 20.3% |
> | ∞ | √(0.25 × 0.16) = **20.0%** |
>
> Most of the benefit comes from the **first 10–20 stocks**.

### Two sources of risk (slide 20)
$$\text{Total risk} = \text{Market risk} + \text{Unique risk}$$
| Market risk | Unique risk |
|---|---|
| Affects **all** stocks (macro) | Affects **one** stock (micro) |
| Also called **systematic**, systemic, **nondiversifiable**, general risk | Also called **firm-specific**, **idiosyncratic**, **nonsystematic**, **diversifiable** risk |

Learn **all the synonyms**: exam questions often use a different name from the one you memorised.

---

## 2. Markowitz selection with N risky assets (slides 22–25)

- **Two assets (Lecture 4):** the opportunity set is a single curve between D and E.
- **Three assets (slide 23):** different weights give a **cloud of points**. The data would be provided.
- **N assets (slide 24):** individual assets (X, Y, Z, …) lie **inside** the opportunity set. Its left edge is the **minimum-variance frontier**, with the **global minimum-variance portfolio** at its leftmost point. The **efficient frontier** is the part above that point.

### Three steps with a risk-free asset (slide 25)
1. **Draw the efficient frontier.**
2. **Pick P\*:** draw the CAL from F **tangent** to the efficient frontier.
3. **Pick C\*:** find where an **indifference curve** is tangent to that CAL.

---

## 3. The CAPM (slides 27–38)

### Assumptions (slide 27)
1. Investors can **borrow and lend any amount at the risk-free rate**.
2. Investors are **mean–variance optimizers**.
3. Investors have a **common world view** ("**homogeneous expectations**"): they agree on expected returns and on variances and covariances.

### The market portfolio (slides 28–29)
If everyone thinks alike, they all:
- agree on E(r), variances and covariances;
- compute the **same efficient frontier**;
- hold the **same optimal risky portfolio** (the same % in each risky security).

**That common P\* is the market portfolio, M.**

**Example (slide 29):** each investor holds 50% A, 30% B, 20% C, just in different amounts.
| Stock | Investor 1 | Investor 2 | Investor 3 | **Market** |
|---|---|---|---|---|
| A (50%) | $50 | $100 | $200 | **$350** |
| B (30%) | $30 | $60 | $120 | **$210** |
| C (20%) | $20 | $40 | $80 | **$140** |
| Sum | $100 | $200 | $400 | **$700** |

Adding up everyone's holdings gives the market, and the market has the **same 50/30/20 weights**.

### The Capital Market Line (CML) (slide 30)
- The CML is the **CAL drawn through the market portfolio M**: from F at (0, r_f) through M at (σ_M, E(r_M)).
$$\text{CML: } E(r_C) = r_f + \frac{E(r_M) - r_f}{\sigma_M}\,\sigma_C$$
- The x-axis is **total risk σ**. Only efficient portfolios (mixes of F and M) lie on it.

### CAPM implications (slide 31)
- **Everyone holds M as P\*.** M includes **all traded assets**, each held in proportion to its **market capitalization**.
- **Passive (index, "lazy") investing is efficient.**
- **Everyone's C\* is a mix of M and F.** Only the split (y) differs across investors.

### Equilibrium security returns (slides 32–34)
What is a **fair** expected return for one stock? Compare it with the benchmark everyone holds, M.
- **Stock x's reward-to-risk ratio** = its contribution to the market risk premium ÷ its contribution to market risk:
$$\frac{w_x[E(r_x) - r_f]}{w_x\sigma_{Mx}} = \frac{E(r_x) - r_f}{\sigma_{Mx}}$$
- **For the market itself:** market risk premium ÷ market variance = [E(r_M) − r_f] / σ_M². This is the **"market price of risk."**
- **In equilibrium**, prices adjust until every security offers the **same** reward-to-risk:
$$\frac{E(r_x) - r_f}{\sigma_{Mx}} = \frac{E(r_M) - r_f}{\sigma_M^2} \;\;\Longrightarrow\;\; E(r_x) - r_f = \frac{\sigma_{Mx}}{\sigma_M^2}[E(r_M) - r_f]$$

$$\boxed{\text{CAPM: } E(r_x) = r_f + \beta_x[E(r_M) - r_f], \qquad \beta_x = \frac{\sigma_{Mx}}{\sigma_M^2}}$$

### The Security Market Line (SML) (slide 35)
- The SML plots **E(r) against β** (not σ!).
- It goes through **(0, r_f)** and **M at (β = 1, E(r_M))**.
- **Slope = E(r_M) − r_f**, the **market risk premium**.
- **Every** asset (efficient or not) lies on the SML in equilibrium.

### Using the SML to pick stocks: alpha (slide 36)
The **actual** expected return A(r) (e.g., an analyst's forecast) can differ from the CAPM return. The difference is **alpha**:
$$\alpha = A(r) - E(r)_{\text{CAPM}}$$
| Alpha | Return is | Price is | Action |
|---|---|---|---|
| **α > 0** (above the SML) | too **high** | too **low** (underpriced) | **Buy** |
| **α < 0** (below the SML) | too **low** | too **high** (overpriced) | **Sell** |
| **α = 0** (on the SML) | adequate | fair | **Hold** |

**Remember:** high expected return ⇔ low current price. Price and expected return move in **opposite** directions.

### Evidence: 30 Dow stocks (slide 37)
A scatter of average excess return vs. beta. The relationship is **weak/flat**: higher-β stocks don't clearly earn more. This motivates multifactor models.

### Two ways to estimate beta (slide 38)
1. **Covariance method:** β_i = σ_iM / σ_M², with σ_iM and σ_M² from sample returns. (▶ Equivalent: β_i = ρ_iM σ_i / σ_M.)
2. **Regression of excess returns** (the "characteristic line"):
$$R_{it} = \alpha_i + \beta_i R_{Mt} + e_{it}, \qquad R_{it} = r_{it} - r_f,\; R_{Mt} = r_{Mt} - r_f$$
   **α** is the intercept, **β** is the slope, **e** is the residual.

> **▶ Beyond the slides: CML vs. SML** (a classic exam question)
>
> | | CML | SML |
> |---|---|---|
> | x-axis | **σ** (total risk) | **β** (systematic risk) |
> | Slope | Sharpe ratio of M: [E(r_M) − r_f]/σ_M | Market risk premium: E(r_M) − r_f |
> | Which assets lie on it | Only **efficient portfolios** (mixes of M and F) | **All** fairly priced assets and portfolios |
> | Used for | Asset allocation (choosing y) | Pricing individual securities (fair return, α) |
>
> **Portfolio beta** is the weighted average: β_P = Σ w_i β_i. Beta of M = 1; beta of the risk-free asset = 0.

---

## 4. Multifactor models (slides 40–44)

### The CAPM as a single-factor model (slide 40)
$$(\tilde r_i - r_f) = \alpha_i + \beta_i(\tilde r_M - r_f) + \tilde e_i$$
- **α_i:** the stock's expected excess return **if the market excess return is zero**.
- **β_i(r̃_M − r_f):** the part of the return due to **market movements** (systematic).
- **ẽ_i:** the **firm-specific** part, not due to the market. **Corr(r̃_M, ẽ_i) = 0.**

▶ This splits total variance: σ_i² = β_i²σ_M² + σ²(e_i), i.e., **systematic + firm-specific**.

### Multifactor models (slide 41)
"**The CAPM does not work well**, so we introduce…"
$$r_{it} - r_f = \alpha_i + \beta_{i1}(r_{1t} - r_f) + \dots + \beta_{in}(r_{nt} - r_f) + e_{it}$$
- r_1t − r_f, …, r_nt − r_f are the **factor excess returns**.
- β_i1, …, β_in are the **factor betas** (sensitivities).
- e_it = unanticipated firm-specific events.
- **α_i (mispricing) = 0 in equilibrium.**

### Fama–French (1993) three-factor model (slide 42)
1. **Market:** the excess return of the market index.
2. **SMB (Small Minus Big):** return on small-cap stocks − return on big-cap stocks (the **size** factor).
3. **HML (High Minus Low):** return on high book-to-market stocks − return on low book-to-market stocks (the **value** factor).

▶ $r_i - r_f = \alpha_i + \beta_{iM}(r_M - r_f) + \beta_{i,SMB}\,SMB + \beta_{i,HML}\,HML + e_i$

### Passive investment strategies (slide 43)
- **Do what the theory says:** hold a sensible mix of the **risk-free asset and index funds** (a point on the CAL), instead of trading every day and **timing the market**.
- **Why?** Few people **consistently** beat the market; stock picking and market timing are **costly**; **passive beats active**.

### "Trading is hazardous to your wealth" (slide 44)
**Barber & Odean (2000), Journal of Finance:** 78,000 US households, 1991–1996.
- **Gross** returns are about the same (~18–19%) across trading-activity groups.
- **Net** returns (after costs) **fall sharply** as trading rises: the most active group nets only about **11%**, against about **18%** for the S&P 500.
- **Lesson:** trading costs eat returns. The more you trade, the worse you do.

---

## 5. Formula sheet

| Concept | Formula |
|---|---|
| Equal-weighted n-stock variance | σ_P² = σ²/n + [(n−1)/n]ρσ² → ρσ² as n → ∞ |
| CML | E(r_C) = r_f + [(E(r_M) − r_f)/σ_M]·σ_C |
| Beta | β_i = σ_iM / σ_M² (= ρ_iMσ_i/σ_M ▶) |
| CAPM / SML | E(r_i) = r_f + β_i[E(r_M) − r_f] |
| Alpha | α = actual (forecast) return − CAPM return |
| Single-index regression | R_i = α_i + β_iR_M + e_i (excess returns) |
| Variance split ▶ | σ_i² = β_i²σ_M² + σ²(e_i) |
| Portfolio beta | β_P = Σ w_iβ_i |
| Multifactor | r_i − r_f = α_i + Σ β_ik(r_k − r_f) + e_i |

---

## 6. Self-test

1. Ten stocks, each with σ = 30%, pairwise ρ = 0.2, equally weighted. What is σ_P? What does it approach as n → ∞?
2. Name three other terms for "unique risk" and three for "market risk".
3. State the three CAPM assumptions. Why do they imply that everyone holds the market portfolio?
4. r_f = 2%, E(r_M) = 9%. Stock K has β = 1.5. What is its CAPM expected return?
5. An analyst expects K to return 11%. What is its alpha? Should you buy or sell it?
6. Cov(r_i, r_M) = 0.024 and σ_M = 20%. Find β_i.
7. A portfolio is 40% in a stock with β = 1.5 and 60% in a stock with β = 0.5. What is its beta?
8. What do SMB and HML stand for, and what do they capture?
9. What did Barber & Odean (2000) find?
10. What is the difference between the CML and the SML?

<details>
<summary>Answers</summary>

1. σ² = 0.09. σ_P² = 0.09/10 + (9/10)(0.2)(0.09) = 0.009 + 0.0162 = 0.0252 → σ_P = **15.9%**. Limit: √(0.2 × 0.09) = √0.018 = **13.4%**.
2. Unique: firm-specific, idiosyncratic, nonsystematic, diversifiable. Market: systematic, systemic, nondiversifiable, general.
3. Borrow/lend at r_f; mean–variance optimizers; homogeneous expectations. Everyone computes the same frontier and the same tangency P\*. Since all investors together must hold all the shares that exist, P\* must be the market portfolio.
4. 2% + 1.5 × 7% = **12.5%**.
5. α = 11% − 12.5% = **−1.5%** → expected return too low → price too high → **sell**.
6. β = 0.024 / 0.04 = **0.6**.
7. 0.4(1.5) + 0.6(0.5) = **0.9**.
8. SMB = Small Minus Big (size factor); HML = High Minus Low book-to-market (value factor).
9. Gross returns were similar across traders, but net returns fell sharply with trading activity; the most active households underperformed the market badly.
10. CML: E(r) vs. σ, only efficient portfolios, slope = Sharpe ratio of M. SML: E(r) vs. β, all fairly priced assets, slope = market risk premium.
</details>
