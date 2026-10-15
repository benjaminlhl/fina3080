# FINA 3080 — Week 4 Notes
## Lecture 4: Portfolio analyses and the Markowitz portfolio selection model

*Investment Analysis and Portfolio Management · Instructor: Chao Ying (CUHK)*

> **How to read these notes:** everything in the main text comes from the slides. Parts marked **▶ Beyond the slides** are my own explanations and worked examples. They follow the optional textbook (BKM Ch. 6–7) but were not explicitly presented in lecture.

**Today's outline**
1. Levels of the allocation decision
2. Return and risk of the complete portfolio
3. The Capital Allocation Line (CAL)
4. Risk tolerance and portfolio choice
5. Portfolios of two risky assets
6. The optimal risky portfolio
7. The optimal complete portfolio

---

## 0. Recap, announcements and market update (slides 2–8)

### Recap of Lecture 3
Value at Risk (VaR); risky and risk-free prospects and the risk premium; risk preferences and utility; mean–variance analysis and indifference curves.

### Announcements
- **Homework 1** is on Blackboard and is **due Oct 16**.
- Team information is on Blackboard, so check which team you are in.
- You can start the homework after this lecture.

### HSI vs. S&P 500, week of Sep 21–25 (slides 4–5)
- The level correlation fell to **0.47** (it was 0.54 in weeks 1–2 and 0.52 in week 3).
- **Sep 21:** an AI and chip rally plus falling oil prices pushed **both** the HSI and US stocks up.
- **Sep 23:** a strong US PMI (Purchasing Managers' Index) showed the economy was stronger than expected. That raised worries about **another Fed hike**, and stocks fell.
- By the end of the week the S&P 500 had recovered, but the HSI kept drifting lower.

### A few mega-cap stocks move an entire index (slide 6)
- On Sep 21, **AMD** rose about 10% and reached a **$1 trillion** market cap. **Intel** rose 12% and **Arm** rose 17% as AI stocks rallied.
- On Friday, **Microsoft** rose 3.7% after unveiling new Copilot coding and agentic-AI features.
- **Takeaway:** in a value-weighted index, a handful of giants can move the whole index even if most companies barely move. This links back to the index-weighting material in Lecture 1.

### Good economic news can be bad for stocks (slides 7–8)
**PMI:** a survey-based indicator of current business conditions.

| PMI | Meaning |
|---|---|
| > 50 | Business activity is **expanding** |
| = 50 | Roughly unchanged |
| < 50 | Business activity is **contracting** |

A higher number means **faster** expansion. It is **not** a percentage growth rate.

S&P Global's US Composite PMI came in at **58.4**, up from 56.0. That was the strongest reading in more than five years.

**The chain:** strong economy → markets expect higher rates → bond prices fall → stocks fall.

> **▶ Beyond the slides — why higher rates hurt stocks.** A stock's price is the present value of its future cash flows. A higher interest rate raises the discount rate, so the same cash flows are worth less today. Growth stocks, whose cash flows lie far in the future, are hit hardest. In CAL terms, a higher r_f also lowers the Sharpe ratio of stocks unless their expected return rises by the same amount.

---

## 1. Levels of the allocation decision (slide 10)

Building a portfolio involves two decisions:

| Level | Decision | Today's tool |
|---|---|---|
| **Asset allocation** (capital allocation) | How much to put in risky assets vs. risk-free assets: the weight **y** | The CAL and the investor's utility |
| **Security selection** | Within the risky part, how much to put in stocks, bonds and other assets | The Markowitz model: the **optimal risky portfolio P\*** |

The result is the **complete portfolio C**: risky assets plus risk-free assets.

---

## 2. Return and risk of the complete portfolio (slides 12–13)

### Expected return (slide 12)
$$E(r_C) = yE(r_P) + (1-y)r_f = r_f + y[E(r_P) - r_f]$$

| Part | Meaning |
|---|---|
| r_f | **Risk-free return**: a reward for inflation and for delaying consumption, with no risk |
| y | **Risk weight**: the *quantity* of risk you take |
| E(r_P) − r_f | **Risk premium**: the reward for taking risk (the *price* of risk) |

### Risk (slide 13)
$$\sigma_C^2 = y^2\sigma_P^2 + (1-y)^2\sigma_f^2 + 2y(1-y)\sigma_{Pf}$$

By definition **σ_f = 0** and **σ_Pf = 0**, so:
$$\sigma_C^2 = y^2\sigma_P^2 \quad\Rightarrow\quad \sigma_C = y\,\sigma_P$$

> **▶ Beyond the slides — why σ_f and σ_Pf are zero.** The risk-free return is a **constant**: a T-bill pays the same r_f in every scenario. A constant never deviates from its mean, so its variance is 0. Covariance multiplies the deviations of the two returns, and one of them is always 0, so the covariance with *any* asset is 0. (This is risk-free in **nominal** terms over the holding period; inflation risk is ignored.)

**Running example:** E(r_P) = 15%, σ_P = 22%, r_f = 7%. Then
1. E(r_C) = 7% + y × 8%
2. σ_C = y × 22%

---

## 3. The Capital Allocation Line (slides 14–16)

### Possible complete portfolios (slide 14)
Combining E(r_C) and σ_C gives a straight line from F (the risk-free asset) through P:

$$E(r_C) = r_f + \underbrace{\frac{E(r_P) - r_f}{\sigma_P}}_{S}\,\sigma_C$$

- **S** is the **Sharpe ratio**, or reward-to-variability ratio. In the example, S = 8/22 = **0.36**.
- σ_P is the **quantity of risk** and E(r_P) − r_f = 8% is the **risk premium**.

| Region | y | Return | Risk |
|---|---|---|---|
| **Unlevered** | 0 ≤ y ≤ 1 | r_f ≤ E(r_C) ≤ E(r_P) | 0 ≤ σ_C ≤ σ_P |
| **Levered** (buying on margin) | y > 1 | E(r_C) > E(r_P) | σ_C > σ_P |

> **▶ Beyond the slides — points on the example CAL.**
>
> | y | E(r_C) | σ_C | What you do |
> |---|---|---|---|
> | 0 | 7% | 0% | All in T-bills (point F) |
> | 0.5 | 11% | 11% | Half in P, half in T-bills |
> | 1 | 15% | 22% | All in P |
> | 1.5 | 19% | 33% | Borrow 50% of your wealth and put 150% in P |
>
> Every point has the same Sharpe ratio of 0.36. Mixing in T-bills or borrowing changes **how much** risk you take, not the **reward per unit of risk**.

### When the borrowing rate is higher (slide 16)
Individuals usually borrow at **r_b > r_f**. To the right of P, the slope becomes
$$S_b = \frac{E(r_P) - r_b}{\sigma_P} < S$$
so the CAL **bends (kinks) at P**: it is flatter in the levered region.

---

## 4. Risk tolerance and asset allocation (slides 18–23)

### Setting up the problem (slide 18)
Plug E(r_C) and σ_C into the utility function U = E(r_C) − ½Aσ_C²:
$$U_C = r_f + y[E(r_P) - r_f] - \tfrac12 A\,y^2\sigma_P^2$$

### Finding the optimal y (slide 19)
Set the derivative to zero (first-order condition):
$$\frac{\partial U_C}{\partial y} = [E(r_P) - r_f] - A\,y\,\sigma_P^2 = 0$$
$$\boxed{y^* = \frac{E(r_P) - r_f}{A\,\sigma_P^2}}$$

**Example (A = 4):** y* = (0.15 − 0.07) / [4 × (0.22)²] = 0.08 / 0.1936 = **41.32%**

### Graphically (slides 20–21)
- **Slide 20:** plot U against y. The curve is an upside-down parabola with its peak at **y* = 0.4132**, where **U(y*) = 8.65%**.
- **Slide 21:** on the CAL, the optimal portfolio **C\*** is where an indifference curve (A = 4) is **tangent** to the CAL.
  - E(r_C*) ≈ **10.3%** and σ_C* ≈ **9.1%**. (The slide shows 10.28% and 9.02%; using y* = 0.4132 exactly gives 7% + 0.4132 × 8% = 10.31% and 0.4132 × 22% = 9.09%. The difference is just rounding.)
  - Three indifference curves are drawn:
    - U = 4.65%: **suboptimal**. It crosses the CAL, so you can do better.
    - U = 8.65%: **optimal**. It just touches the CAL at C\*.
    - U = 12.65%: **unfeasible**. It lies entirely above the CAL, so no portfolio reaches it.

> **▶ Beyond the slides — what y\* tells you.**
> - A **higher risk premium** → a bigger y\*.
> - **More risk (σ_P)** → a smaller y\*. σ_P is squared, so this effect is strong.
> - **More risk aversion (A)** → a smaller y\*.
> - In the example, an investor with A = 1.5 gets y\* = 0.08 / (1.5 × 0.0484) = 1.10 and would **borrow** to hold 110% in P.

### More details about the CAL (slides 22–23)

**Can y\* be below zero?** No. The complete portfolio's expected return would then be **below r_f**, so the investor is better off in T-bills.

**What if r_b > r_f?**
1. First solve for y\* using **r_f**.
2. **Case 1: y\* ≤ 1** (unlevered). The borrowing rate doesn't matter. Keep y\*.
3. **Case 2: y\* > 1** (you want to borrow). Replace r_f with **r_b** and solve again. Call the answer **y\*\***.
   - If **y\*\* > 1**: you still want to borrow at r_b, so use y\*\*.
   - If **y\*\* < 1** (while y\* > 1): you'd borrow at r_f but not at r_b. The best you can do is **y = 1**: put everything in P and borrow nothing. This is the kink point on slide 23.

> **▶ Beyond the slides — the r_b example.** With E(r_P) = 15%, σ_P = 22%, r_f = 7% and A = 1.5: y\* = 1.10 > 1. If r_b = 9%, y\*\* = (0.15 − 0.09) / (1.5 × 0.0484) = 0.83 < 1. So this investor holds **y = 1**, 100% in P.

---

## 5. Portfolios of two risky assets (slides 25–29)

### Setup (slide 25)
| | Bond fund (D) | Stock fund (E) |
|---|---|---|
| E(r) | 8% | 13% |
| σ | 12% | 20% |

### Formulas (slide 26)
With weights w_D + w_E = 1:
$$E(r_P) = w_D E(r_D) + w_E E(r_E)$$
$$\sigma_P^2 = w_D^2\sigma_D^2 + w_E^2\sigma_E^2 + 2w_Dw_E\sigma_{DE}$$
$$\sigma_P = \left[w_D^2\sigma_D^2 + w_E^2\sigma_E^2 + 2w_Dw_E\,\rho_{DE}\,\sigma_D\sigma_E\right]^{1/2}$$

where σ_DE = ρ_DE σ_D σ_E is the covariance and ρ_DE the correlation.

### Portfolio risk vs. security risk (slides 27–28)
Vary the weights from all stock to all bonds, for correlations ρ = 1, 0.3, 0 and −1:

| w_D | w_E | E(r_P) | σ_P (ρ = 1) | σ_P (ρ = 0.3) | σ_P (ρ = 0) | σ_P (ρ = −1) |
|---|---|---|---|---|---|---|
| 0.0 | 1.0 | 13% | 20% | 20% | 20% | 20% |
| 0.1 | 0.9 | 13% | 19% | 18% | 18% | 17% |
| 0.2 | 0.8 | 12% | 18% | 17% | 16% | 14% |
| 0.3 | 0.7 | 12% | 18% | 15% | 14% | 10% |
| 0.4 | 0.6 | 11% | 17% | 14% | 13% | 7% |
| 0.5 | 0.5 | 11% | 16% | 13% | 12% | 4% |
| 0.6 | 0.4 | 10% | 15% | 12% | 11% | 1% |
| 0.7 | 0.3 | 10% | 14% | 12% | 10% | 2% |
| 0.8 | 0.2 | 9% | 14% | 11% | 10% | 6% |
| 0.9 | 0.1 | 9% | 13% | 12% | 11% | 9% |
| 1.0 | 0.0 | 8% | 12% | 12% | 12% | 12% |

**Key points:**
- **E(r_P) does not depend on ρ.** It is just the weighted average of the two returns.
- **σ_P does depend on ρ.** With **ρ = 1**, σ_P is the weighted average of the two σ's, so there is **no diversification benefit**.
- With **ρ < 1**, σ_P is **less** than the weighted average. Diversification reduces risk.
- With **ρ = −1**, the two assets can **fully hedge** each other, and σ_P can reach 0.
- With ρ = 0.3, a mix like 80/20 (11%) is **less risky than the bond fund alone** (12%).

### Risk vs. weight in stocks (slide 29)
Plotting σ_P against w_E (allowing short positions from −0.5 to 1.5) shows each curve's **minimum-variance** point:

| ρ | w_E at minimum variance | Minimum σ_P |
|---|---|---|
| 0.3 | 0.18 | 11.45% |
| 0 | 0.26 | 10.3% |
| −1 | 0.38 | 0% |

> **▶ Beyond the slides — the minimum-variance weight.** Setting dσ_P²/dw_E = 0 gives
> $$w_E^{\min} = \frac{\sigma_D^2 - \sigma_{DE}}{\sigma_D^2 + \sigma_E^2 - 2\sigma_{DE}}, \qquad w_D^{\min} = 1 - w_E^{\min}$$
> For ρ = 0.3: σ_DE = 0.3 × 0.12 × 0.20 = 0.0072, so w_E = (0.0144 − 0.0072) / (0.0144 + 0.04 − 0.0144) = **0.18**.
> For ρ = −1 this simplifies to w_E = σ_D / (σ_D + σ_E) = 0.12 / 0.32 = **0.375**.

---

## 6. The optimal risky portfolio (slides 31–33)

### The portfolio opportunity set (slide 31)
Plot E(r_P) against σ_P for every mix of D and E. For each ρ you get a curve: the **portfolio opportunity set**, meaning all possible risky portfolios.
- **ρ = 1:** a straight line from D to E.
- **ρ < 1:** the curve bulges **to the left** (less risk for the same return). The lower ρ, the bigger the bulge.
- **ρ = −1:** two straight lines that meet at σ = 0.

### Finding P\* (slide 32)
Now add a risk-free asset with **r_f = 5%**. You can draw a CAL from F to **any** risky portfolio. The best one is the CAL with the **highest Sharpe ratio**: the line that is **tangent** to the opportunity set. The tangency point is the **optimal risky portfolio P\***.

| Portfolio | E(r) | σ | Sharpe ratio |
|---|---|---|---|
| A (minimum variance, ρ = 0.3) | 8.9% | 11.45% | (8.9 − 5) / 11.45 = **0.34** |
| **P\*** (tangency) | 11% | 14.2% | (11 − 5) / 14.2 = **0.42** |

CAL(A) is **not optimal**: CAL(P\*) gives more return for every level of risk.

### The efficient frontier (slide 33)
Only the part of the opportunity set **above the minimum-variance portfolio A** is worth holding. That upper part is the **efficient frontier**. Any point below A is beaten by a point directly above it, with the same risk and a higher return.

> **▶ Beyond the slides — the tangency formula.** With two risky assets and excess returns R_D = E(r_D) − r_f and R_E = E(r_E) − r_f:
> $$w_D^* = \frac{R_D\sigma_E^2 - R_E\sigma_{DE}}{R_D\sigma_E^2 + R_E\sigma_D^2 - (R_D + R_E)\sigma_{DE}}, \qquad w_E^* = 1 - w_D^*$$
> Here R_D = 3%, R_E = 8%, σ_DE = 0.0072:
> w_D\* = (0.03 × 0.04 − 0.08 × 0.0072) / (0.03 × 0.04 + 0.08 × 0.0144 − 0.11 × 0.0072) = 0.000624 / 0.00156 = **0.40**.
> The slides say the P\* weights will be **provided** in the homework and exam, so you don't need to memorize this.

---

## 7. The optimal complete portfolio (slides 35–37)

### The three-step recipe
1. **Find P\*** (given: w_D\* = 40% in bonds, w_E\* = 60% in stocks).
2. **Treat P\* as one risky asset** and compute its return and risk:
   - E(r_P\*) = 0.4 × 8% + 0.6 × 13% = **11%**
   - σ_P\*² = 0.4² × 0.0144 + 0.6² × 0.04 + 2 × 0.4 × 0.6 × 0.0072 ≈ **2.016%** (σ_P\* ≈ 14.2%)
3. **Choose y\*** using the investor's A (A = 4):
   - y\* = (0.11 − 0.05) / (4 × 0.020164) = 0.06 / 0.080656 = **74.39%**

On the graph (slide 35), C\* sits on CAL(P\*) where the A = 4 indifference curve touches it: E(r_C\*) = 5% + 0.7439 × 6% ≈ **9.46%** and σ_C\* = 0.7439 × 14.2% ≈ **10.56%**.

### Final weights (slide 37)
| Asset | Weight in the complete portfolio |
|---|---|
| Risk-free asset | 1 − 0.7439 = **25.61%** |
| Bonds | 40% × 74.39% = **29.76%** |
| Stocks | 60% × 74.39% = **44.63%** |
| **Total** | **100%** |

> **▶ Beyond the slides — the separation property.** Every investor, whatever their A, holds the **same risky portfolio P\***, because P\* depends only on the assets' returns, risks and correlations, not on preferences. Investors differ only in **y\***, i.e. how they split money between P\* and T-bills. A more risk-averse investor (higher A) holds less of P\*; a less risk-averse one holds more, possibly borrowing. For example, with A = 2: y\* = 0.06 / (2 × 0.02016) ≈ 1.49, so this investor borrows about 49% of their wealth and holds roughly 59.5% bonds and 89.3% stocks.

---

## 8. Formula sheet

| Concept | Formula |
|---|---|
| Complete portfolio return | E(r_C) = r_f + y[E(r_P) − r_f] |
| Complete portfolio risk | σ_C = yσ_P |
| Sharpe ratio | S = [E(r_P) − r_f] / σ_P |
| CAL | E(r_C) = r_f + S·σ_C |
| Levered slope with r_b > r_f | S_b = [E(r_P) − r_b] / σ_P |
| Utility of the complete portfolio | U_C = r_f + y[E(r_P) − r_f] − ½Ay²σ_P² |
| Optimal allocation | y\* = [E(r_P) − r_f] / (Aσ_P²) |
| Two-asset return | E(r_P) = w_D E(r_D) + w_E E(r_E) |
| Two-asset variance | σ_P² = w_D²σ_D² + w_E²σ_E² + 2w_Dw_Eρ_DEσ_Dσ_E |
| Covariance | σ_DE = ρ_DE σ_D σ_E |
| Minimum-variance weight | w_E = (σ_D² − σ_DE) / (σ_D² + σ_E² − 2σ_DE) |

---

## 9. Self-test

1. r_f = 4%, E(r_P) = 12%, σ_P = 25%, A = 3. Find y\*, E(r_C), σ_C and the investor's utility.
2. Same as Q1 but A = 1. Find y\*. If the borrowing rate is r_b = 6%, what should the investor do?
3. Asset 1 has E = 6% and σ = 10%. Asset 2 has E = 14% and σ = 30%. With ρ = 0, compute E(r_P) and σ_P for a 50/50 portfolio.
4. Same assets with ρ = −1. Which weights give a zero-risk portfolio, and what is its return?
5. Why does diversification reduce risk unless ρ = 1?
6. r_f = 3%. Portfolio X has E = 9% and σ = 12%; portfolio Y has E = 12% and σ = 20%. Which should you combine with T-bills, and why?
7. Using the lecture's P\* (E = 11%, σ² = 2.016%, r_f = 5%), find y\* and the bond, stock and risk-free weights for A = 2.
8. Why is the part of the opportunity set below the minimum-variance portfolio never chosen?
9. What does it mean for an indifference curve to be "unfeasible"?

<details>
<summary>Answers</summary>

1. y\* = 0.08 / (3 × 0.0625) = **0.427**. E(r_C) = 4% + 0.427 × 8% = **7.41%**. σ_C = 0.427 × 25% = **10.67%**. U = 7.41% − 1.5 × (0.1067)² = **5.71%** (above r_f = 4%, as it must be).
2. y\* = 0.08 / 0.0625 = **1.28**, so the investor wants to borrow. At r_b: y\*\* = (0.12 − 0.06) / 0.0625 = **0.96** < 1. So hold **y = 1**: everything in P, no borrowing.
3. E(r_P) = **10%**. σ_P = √(0.25 × 0.01 + 0.25 × 0.09) = √0.025 = **15.81%**, below the 20% weighted average of the two σ's.
4. w_2 = σ_1 / (σ_1 + σ_2) = 10/40 = **25%** in asset 2 and 75% in asset 1. Return = 0.75 × 6% + 0.25 × 14% = **8%**, with zero risk.
5. The covariance term 2w_1w_2ρσ_1σ_2 is smaller when ρ < 1, so σ_P falls below the weighted average of the two σ's. With ρ = 1, σ_P equals that weighted average, so there is no reduction.
6. Sharpe(X) = 6/12 = **0.50**; Sharpe(Y) = 9/20 = **0.45**. Choose **X**: its CAL is steeper, so it gives more return for every level of risk. You can lever X up if you want more risk.
7. y\* = 0.06 / (2 × 0.02016) = **1.49**. Bonds = 0.4 × 1.49 = **59.5%**, stocks = 0.6 × 1.49 = **89.3%**, risk-free = 1 − 1.49 = **−48.8%** (borrowing).
8. For every portfolio below it, there is one directly above it on the frontier with the **same risk and a higher return**, so a rational investor never holds the lower one.
9. It lies entirely above the CAL, so **no** available portfolio gives that much utility.
</details>
