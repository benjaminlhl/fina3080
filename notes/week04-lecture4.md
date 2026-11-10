# FINA 3080 — Week 4 Notes
## Lecture 4: Portfolio analysis and the Markowitz portfolio selection model

*Investment Analysis and Portfolio Management · Instructor: Chao Ying (CUHK)*

> **How to read these notes:** everything in the main text comes from the slides. Parts marked **▶ Beyond the slides** are my own explanations and worked examples. They follow the optional textbook (BKM Ch. 6–7) but were not explicitly presented in lecture.

**Today's outline**
1. Levels of the allocation decision *(recap from Lecture 3)*
2. Return and risk of the complete portfolio *(recap from Lecture 3)*
3. The Capital Allocation Line (CAL), including a borrowing rate above the risk-free rate
4. Risk tolerance and portfolio choice: the optimal y*
5. Portfolios of two risky assets
6. The optimal risky portfolio P*
7. The optimal complete portfolio C*

---

## 0. Announcements and market update (slides 2–8)

### Announcements
- **Homework 1** is posted on Blackboard and is **due Oct 16**. Team information is on Blackboard.
- You can start the homework after this lecture.

### HSI vs. S&P 500, week of Sep 21–25 (slides 4–5)
- The level correlation is **0.47**.
- **Sep 21:** an AI/chip rally and falling oil prices → **HSI and US stocks rose**.
- **Sep 23:** a **strong US PMI** → the economy is stronger than expected → **fears of a Fed hike grow** → **stocks fell**.

### A few mega-cap stocks move an entire index (slide 6)
- On Sep 21, **AMD** rose about 10% and reached a **$1 trillion** market cap. **Intel** rose 12% and **Arm** rose 17%. On Friday, **Microsoft** rose 3.7% after it unveiled new Copilot features.
- **Lesson (ties to Lecture 1):** in a **value-weighted index**, a few mega-cap stocks can move the whole index even when most other companies barely move.

### Good economic news can be bad for stocks (slides 7–8)
**The Purchasing Managers' Index (PMI)** is a survey-based measure of current business conditions.
| PMI | Meaning |
|---|---|
| **> 50** | Business activity is **expanding** |
| **= 50** | Roughly unchanged |
| **< 50** | Business activity is **contracting** |

- A higher PMI means faster expansion. It is **not** a percentage growth rate.
- **US Composite PMI = 58.4**, up from 56.0. This is the strongest reading in more than five years.
- **Chain of reasoning:** strong economy → **expectations of higher rates** → bond prices fall → **stocks fall**.

---

## 1. Levels of the allocation decision (slide 10, recap)

The investment decision happens at three levels, from the top down:
1. **Asset allocation (capital allocation):** choose the weights between the **risky portfolio** and the **risk-free asset**. This is the choice of **y**.
2. **Optimal weights within the risky assets:** stocks vs. bonds vs. other risky assets. This produces **P\***.
3. **Security selection:** choose which individual securities to hold within each class.

The **complete portfolio** is the whole thing: risky assets plus the risk-free asset.

---

## 2. Return and risk of the complete portfolio (slides 12–14, recap)

Put a fraction **y** of your wealth in the risky portfolio P and **1 − y** in the risk-free asset.

**Expected return**
$$E(r_C) = yE(r_P) + (1-y)r_f \;\;\Longrightarrow\;\; E(r_C) = r_f + y\,[E(r_P) - r_f]$$
- **r_f** is the reward for **inflation and deferred consumption**, with no risk.
- **y** is the **quantity** of risk you take on.
- **E(r_P) − r_f**, the **risk premium**, is the **price** of risk: the reward for taking it on.

**Risk**
$$\sigma_C^2 = y^2\sigma_P^2 + (1-y)^2\sigma_f^2 + 2y(1-y)\sigma_{Pf}$$
The risk-free asset has σ_f = 0 and σ_Pf = 0 by definition, so
$$\sigma_C^2 = y^2\sigma_P^2 \;\;\Longrightarrow\;\; \sigma_C = y\,\sigma_P$$

**Slide example:** E(r_P) = 15%, σ_P = 22%, r_f = 7%. Then E(r_C) = 7% + y·8% and σ_C = y·22%.

---

## 3. The Capital Allocation Line (CAL) (slides 14, 16, 22–23)

Substitute y = σ_C / σ_P into the return equation:
$$E(r_C) = r_f + \underbrace{\frac{E(r_P) - r_f}{\sigma_P}}_{S\text{ = Sharpe ratio}}\;\sigma_C$$

- The CAL is a **straight line** in (σ, E(r)) space. It starts at **F = (0, r_f)** and passes through **P = (σ_P, E(r_P))**.
- **Slope = Sharpe ratio = reward-to-variability** = S = [E(r_P) − r_f] / σ_P. In the slide example, S = 8/22 = **0.36**.

| Range of y | What it means | Where you sit on the CAL |
|---|---|---|
| **y = 0** | All risk-free | Point F |
| **0 ≤ y ≤ 1** | **Unlevered**: you lend at r_f | Between F and P: r_f ≤ E(r_C) ≤ E(r_P) and 0 ≤ σ_C ≤ σ_P |
| **y = 1** | All in the risky portfolio | Point P |
| **y > 1** | **Levered**: you borrow at r_f, i.e., **buy on margin** | Beyond P: E(r_C) > E(r_P) and σ_C > σ_P |

### When the borrowing rate is higher: r_b > r_f (slides 16, 22–23)
Brokers usually charge more to borrow than the risk-free rate.
- To the **left** of P (lending), the slope is still S = [E(r_P) − r_f] / σ_P. This is **CAL 1**.
- To the **right** of P (borrowing), the slope is **S_b = [E(r_P) − r_b] / σ_P**, which is **smaller**. This is **CAL 2**.
- So the CAL becomes **kinked at P**, i.e., at y = 1.

**How to find the optimal portfolio when r_b > r_f (exam procedure):**
1. Solve y\* with **r_f**.
2. **Case 1: y\* ≤ 1** (no borrowing). You're done, and r_b doesn't matter.
3. **Case 2: y\* > 1.** You want to borrow, so solve again with **r_b** in place of r_f. Call the result **y\*\***.
   - If **y\*\* > 1**, use y\*\*. You buy on margin and borrow at r_b.
   - If **y\*\* ≤ 1** (while y\* > 1), choose **y = 1**. You'd borrow at r_f but you can't, and at r_b you don't want to borrow. The answer is the **kink**: 100% in the risky portfolio.

### Can y\* be negative? (slide 22)
**No.** A negative y means shorting the risky portfolio. When E(r_P) > r_f, the complete portfolio would then have an expected return **below r_f** while still carrying risk. A risk-averse investor would never choose that.

---

## 4. Risk tolerance and portfolio choice: the optimal y\* (slides 18–21)

Utility (from Lecture 3) is U = E(r) − ½Aσ². Substitute the complete portfolio:
$$U_C = r_f + y\,[E(r_P) - r_f] - \tfrac{1}{2}A\,y^2\sigma_P^2$$

**Maximize over y.** The first-order condition is ∂U_C/∂y = 0:
$$[E(r_P) - r_f] - A\,y\,\sigma_P^2 = 0 \quad\Longrightarrow\quad \boxed{\,y^* = \frac{E(r_P) - r_f}{A\,\sigma_P^2}\,}$$

**Intuition:** y\* goes **up** with the risk premium and goes **down** with risk aversion A and with variance σ_P². Note that the denominator uses the **variance**, not the standard deviation.

### Worked example (slide 19): A = 4, E(r_P) = 15%, σ_P = 22%, r_f = 7%
$$y^* = \frac{0.15 - 0.07}{4 \times 0.22^2} = \frac{0.08}{4 \times 0.0484} = \frac{0.08}{0.1936} = 41.32\%$$

- E(r_C\*) = 7% + 0.4132 × 8% = **10.31%**
- σ_C\* = 0.4132 × 22% = **9.09%**
- U(y\*) = 0.07 + 0.4132(0.08) − ½(4)(0.4132²)(0.0484) = **8.65%**

> ⚠️ **Slide 21 prints E(r_C\*) = 10.28% and σ_C\* = 9.02%.** These look like rounding from reading the chart. The exact values from the formulas are 10.31% and 9.09%. The utility of **8.653%** matches exactly. On an exam, show your formula and calculation.

### Graphically (slides 20–21)
- **Utility as a function of y (slide 20):** an inverted parabola. It peaks at y\* = 0.4132 with U = 8.65%.
- **On the CAL (slide 21):** draw the **indifference curves** for A = 4. The optimal complete portfolio C\* is where the **highest indifference curve is tangent to the CAL**.
  - U = 4.653% crosses the CAL: it is reachable but **suboptimal**.
  - U = 8.653% just **touches** the CAL at C\*: this is **optimal**.
  - U = 12.653% lies above the CAL everywhere: it is **not feasible**.

> **▶ Beyond the slides:** the indifference curve is E(r) = U + ½Aσ². It is **convex** (curving upward) for a risk-averse investor because each extra unit of σ needs more and more extra return. A more risk-averse investor (larger A) has steeper curves, so their tangency point is **closer to F**, with a smaller y\*.

---

## 5. Portfolios of two risky assets (slides 25–29)

**Setup:** a bond fund **D** and a stock fund **E**.
| | D (bonds) | E (stocks) |
|---|---|---|
| E(r) | 8% | 13% |
| σ | 12% | 20% |

**Formulas** (w_D + w_E = 1):
$$E(r_P) = w_D E(r_D) + w_E E(r_E)$$
$$\sigma_P^2 = w_D^2\sigma_D^2 + w_E^2\sigma_E^2 + 2w_Dw_E\,\sigma_{DE}, \qquad \sigma_{DE} = \rho_{DE}\,\sigma_D\,\sigma_E$$
$$\sigma_P = \left[w_D^2\sigma_D^2 + w_E^2\sigma_E^2 + 2w_Dw_E\,\rho_{DE}\,\sigma_D\sigma_E\right]^{1/2}$$

**Key fact:** the **expected return** is always a **weighted average**. The **risk** is a weighted average **only when ρ = 1**. When ρ < 1, the portfolio σ is **less than** the weighted average of the σ's. **That is the benefit of diversification.**

### Portfolio σ_P for different weights and correlations (slide 28)
| w_D | w_E | E(r_P) | σ_P (ρ = 1) | σ_P (ρ = 0.3) | σ_P (ρ = 0) | σ_P (ρ = −1) |
|---|---|---|---|---|---|---|
| 0.0 | 1.0 | 13.0% | 20% | 20% | 20% | 20% |
| 0.2 | 0.8 | 12.0% | 18% | 17% | 16% | 14% |
| 0.4 | 0.6 | 11.0% | 17% | 14% | 13% | 7% |
| 0.5 | 0.5 | 10.5% | 16% | 13% | 12% | 4% |
| 0.6 | 0.4 | 10.0% | 15% | 12% | 11% | **1%** |
| 0.8 | 0.2 | 9.0% | 14% | 11% | 10% | 6% |
| 1.0 | 0.0 | 8.0% | 12% | 12% | 12% | 12% |

(The slide also has rows for w_D = 0.1, 0.3, 0.7 and 0.9. The slide rounds E(r_P), so 10.5% appears as "11%".)

### σ_P vs. weight in stocks (slide 29)
- **ρ = 1:** σ_P is a **straight line** between 12% and 20%. There is **no diversification benefit**.
- **ρ < 1:** the curve **bows downward**. The lower ρ is, the bigger the bow.
- **ρ = −1:** σ_P hits **zero**. You can build a **perfect hedge**.
- **Minimum-variance points** shown on the chart:
  | ρ | w_E (min variance) | σ_min | E(r) at min variance |
  |---|---|---|---|
  | 0.3 | **0.18** | **11.45%** | 8.9% |
  | 0 | **0.26** | **10.29%** | 9.3% |
  | −1 | **0.38** (= 0.375) | **0%** | 9.9% |

> **▶ Beyond the slides: the minimum-variance weight formula** (gives all the numbers above)
> $$w_E^{min} = \frac{\sigma_D^2 - \sigma_{DE}}{\sigma_D^2 + \sigma_E^2 - 2\sigma_{DE}}, \qquad w_D^{min} = 1 - w_E^{min}$$
> Check for ρ = 0.3: σ_DE = 0.3(0.12)(0.20) = 0.0072, so w_E = (0.0144 − 0.0072)/(0.0144 + 0.04 − 0.0144) = 0.0072/0.04 = **0.18** ✓.
> For **ρ = −1**: w_E = σ_D/(σ_D + σ_E) = 0.12/0.32 = **0.375**, which gives σ = 0.

---

## 6. The optimal risky portfolio P\* (slides 31–33)

### The portfolio opportunity set (slide 31)
- Plot every combination of D and E in (σ, E(r)) space. This curve is the **portfolio opportunity set**: all possible risky portfolios.
- **ρ = 1:** a straight line from D to E.
- **ρ < 1:** a curve that bows **to the left**, toward lower risk.
- **ρ = −1:** two straight lines that meet the **vertical axis** (σ = 0).

### Finding P\*: the highest Sharpe ratio (slide 32)
- Add the risk-free asset F (r_f = **5%**). Any CAL you can draw runs from F to some point on the opportunity set.
- **The best CAL is the steepest one.** It is **tangent** to the opportunity set. The tangency point is the **optimal risky portfolio P\***.
- P\* is the risky portfolio with the **highest reward-to-variability (Sharpe) ratio**.

**Slide numbers (ρ = 0.3):**
| Portfolio | E(r) | σ | Sharpe ratio |
|---|---|---|---|
| **A** = minimum-variance portfolio | 8.9% | 11.45% | (8.9 − 5)/11.45 = **0.34** |
| **P\*** = tangency portfolio | 11.0% | 14.20% | (11 − 5)/14.2 = **0.42** |

So **CAL(P\*)** is steeper than **CAL(A)**. **A is not optimal**, even though it has the lowest risk.

### The efficient frontier (slide 33)
- The **efficient frontier** of risky assets is the part of the opportunity set **above the minimum-variance portfolio A**.
- Portfolios **below A** are **inefficient**: some other portfolio has the same σ and a higher E(r).

### Separation (important idea)
- **Every investor**, whatever their A, uses the **same P\*** because P\* depends only on E(r), σ, ρ and r_f.
- **Risk aversion only affects y\***, i.e., how far along CAL(P\*) the investor sits.

> **▶ Beyond the slides: the tangency weight formula for two risky assets**
> The slide says P\*'s weights will be **provided in the homework and the exam**. Just in case, here is the formula, using excess returns R_D = E(r_D) − r_f and R_E = E(r_E) − r_f:
> $$w_D^* = \frac{R_D\,\sigma_E^2 - R_E\,\sigma_{DE}}{R_D\,\sigma_E^2 + R_E\,\sigma_D^2 - (R_D + R_E)\,\sigma_{DE}}, \qquad w_E^* = 1 - w_D^*$$
> Check with the slide: R_D = 0.03, R_E = 0.08, σ_DE = 0.0072:
> numerator = 0.03(0.04) − 0.08(0.0072) = 0.000624
> denominator = 0.0012 + 0.08(0.0144) − 0.11(0.0072) = 0.00156
> w_D\* = 0.000624 / 0.00156 = **0.40** ✓, so w_E\* = **0.60**.

---

## 7. The optimal complete portfolio C\* (slides 35–37)

**Recipe:** treat P\* as **one risky asset**, then use the y\* formula from Section 4.

**Step 1: describe P\*** (w_D\* = 40%, w_E\* = 60%, ρ = 0.3, r_f = 5%)
$$E(r_{P^*}) = 0.4(8\%) + 0.6(13\%) = 11\%$$
$$\sigma_{P^*}^2 = 0.4^2(0.12^2) + 0.6^2(0.20^2) + 2(0.4)(0.6)(0.0072) = 0.002304 + 0.0144 + 0.003456 = 0.02016$$
σ_P\* = **14.2%**. (The slide writes the variance as 2.0164%, a small rounding difference.)

**Step 2: find y\*** (A = 4)
$$y^* = \frac{0.11 - 0.05}{4 \times 0.020164} = \frac{0.06}{0.080656} = 74.39\%$$

**Step 3: break the complete portfolio down** (slide 37)
| Holding | Calculation | Weight in complete portfolio |
|---|---|---|
| Risk-free | 1 − 0.7439 | **25.61%** |
| Bonds (D) | 0.40 × 74.39% | **29.76%** |
| Stocks (E) | 0.60 × 74.39% | **44.63%** |
| **Total** | | **100%** |

**Step 4: return and risk of C\*** (slide 35)
- E(r_C\*) = 5% + 0.7439 × 6% = **9.46%**
- σ_C\* = 0.7439 × 14.2% = **10.56%**

**Graph (slide 35):** C\* is where the A = 4 indifference curve is tangent to **CAL(P\*)**, at (10.56%, 9.46%).

---

## 8. The whole Markowitz procedure in one view

1. **Inputs:** E(r), σ for each risky asset, the correlations/covariances, and r_f.
2. **Opportunity set:** plot all risky combinations. The **efficient frontier** is the part above the minimum-variance portfolio.
3. **P\*:** find the tangency portfolio with the **maximum Sharpe ratio**. This is the same for everyone.
4. **y\* = [E(r_P\*) − r_f] / (Aσ²_P\*)**: this is personal and depends on A.
5. **Final holdings:** (1 − y\*) in risk-free; y\* × w_i\* in each risky asset i.
6. If **r_b > r_f** and y\* > 1, recheck with r_b (Section 3).

---

## 9. Formula sheet

| Concept | Formula |
|---|---|
| Complete portfolio return | E(r_C) = r_f + y[E(r_P) − r_f] |
| Complete portfolio risk | σ_C = y·σ_P |
| CAL | E(r_C) = r_f + S·σ_C |
| Sharpe ratio (slope of CAL) | S = [E(r_P) − r_f] / σ_P |
| Utility of complete portfolio | U_C = r_f + y[E(r_P) − r_f] − ½Ay²σ_P² |
| Optimal allocation | **y\* = [E(r_P) − r_f] / (Aσ_P²)** |
| Two-asset expected return | E(r_P) = w_D E(r_D) + w_E E(r_E) |
| Two-asset variance | σ_P² = w_D²σ_D² + w_E²σ_E² + 2w_Dw_Eρσ_Dσ_E |
| Covariance ↔ correlation | σ_DE = ρ_DE σ_D σ_E |
| Min-variance weight ▶ | w_E = (σ_D² − σ_DE)/(σ_D² + σ_E² − 2σ_DE) |
| Zero-risk hedge (ρ = −1) ▶ | w_E = σ_D/(σ_D + σ_E) |
| Tangency weight ▶ | w_D\* = (R_Dσ_E² − R_Eσ_DE)/(R_Dσ_E² + R_Eσ_D² − (R_D+R_E)σ_DE) |

---

## 10. Self-test

1. E(r_P) = 12%, σ_P = 20%, r_f = 4%, A = 2. Find y\*, E(r_C) and σ_C.
2. In Q1, change A to 1. What is y\*? If the borrowing rate is r_b = 7%, what should the investor do?
3. Why is the denominator of y\* the **variance** σ_P² rather than σ_P?
4. Two assets: σ_1 = 10%, σ_2 = 30%, ρ = −1. What weights give a zero-risk portfolio?
5. True or false: with ρ = 1 there is no diversification benefit.
6. Why is the minimum-variance portfolio not the optimal risky portfolio?
7. Do two investors with different A hold different risky portfolios P\*? Explain.
8. P\* = 30% D and 70% E, and y\* = 0.6. Give the weights of the complete portfolio.

<details>
<summary>Answers</summary>

1. y\* = 0.08 / (2 × 0.04) = **1.0**, so 100% in P. E(r_C) = **12%** and σ_C = **20%**.
2. y\* = 0.08 / (1 × 0.04) = **2.0**. Recheck with r_b: y\*\* = (0.12 − 0.07) / (1 × 0.04) = **1.25 > 1**. So the investor borrows at 7% and holds **125%** in P. If y\*\* had come out ≤ 1, the answer would be y = 1.
3. Utility subtracts ½Aσ_C² = ½Ay²σ_P². The penalty grows with the **square** of y, so the first-order condition gives Ayσ_P². Intuitively, doubling σ_P makes the risk penalty four times as large.
4. w_1 = σ_2/(σ_1 + σ_2) = 30/40 = **75%** and w_2 = **25%**. Check: σ = |0.75(10%) − 0.25(30%)| = 0.
5. **True.** σ_P is just the weighted average of the σ's, a straight line.
6. P\* maximizes the **Sharpe ratio**. Combined with the risk-free asset, it gives the **steepest CAL**, which beats every other risky portfolio at every level of risk. The minimum-variance portfolio has lower risk but a lower Sharpe ratio (0.34 vs. 0.42 in the slide example).
7. **No.** P\* depends only on asset inputs and r_f, so everyone holds the same P\*. Risk aversion affects only y\*: the split between P\* and the risk-free asset.
8. Risk-free = **40%**, D = 0.3 × 0.6 = **18%**, E = 0.7 × 0.6 = **42%**.
</details>

---

## 11. One-paragraph summary

Investing happens at three levels: risky vs. risk-free (y), weights within risky assets (P\*), and security selection. Mixing a risky portfolio with the risk-free asset gives a straight-line **CAL** whose slope is the **Sharpe ratio**. A higher borrowing rate kinks the CAL at P. The investor's best point is **y\* = [E(r_P) − r_f]/(Aσ_P²)**, where an indifference curve is tangent to the CAL. With two risky assets, expected return is a weighted average but risk falls **below** the weighted average whenever ρ < 1. That is diversification, and it reaches zero risk when ρ = −1. Among all risky portfolios, the **tangency portfolio P\*** has the highest Sharpe ratio and is **the same for every investor**. Each investor then picks their own y\* along CAL(P\*), so C\* = (1 − y\*) risk-free + y\* × P\*.
