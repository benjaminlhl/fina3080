# FINA 3080 — Week 3 Notes
## Lecture 3: Portfolio mathematics and capital allocation

*Investment Analysis and Portfolio Management · Instructor: Chao Ying (CUHK)*

> **How to read these notes:** everything in the main text comes from the slides. Parts marked **▶ Beyond the slides** are my own explanations and worked examples. They follow the optional textbook (BKM Ch. 5–6) but were not explicitly presented in lecture.

**Today's outline**
1. Value at Risk (VaR)
2. Risky and risk-free prospects, and the risk premium
3. Risk preferences and utility
4. Mean–variance analysis and indifference curves
5. Levels of the allocation decision
6. Return and risk of the complete portfolio

---

## 0. Announcements, recap and market update (slides 2–8)

### Announcements
- **Homework teams of 4–6 students.**
  - A team can mix students from both sessions (A and B).
  - Smaller teams will be combined, and students without a team will be assigned to one.
  - Email the **TA, not the instructor**, by **11:59 pm on Sep 25**.
- **Exam conflicts:** the exams are on **Oct 20** and **Dec 1** (7–9 pm). If you don't speak up by **Sep 22**, the instructors assume you can take them.
  - A makeup exam will be arranged, including for the midterm.
  - If you can't take the midterm makeup, the **final counts for 80%** (35% + 45%).
- The quiz solution and practice problems are on Blackboard.

### Recap of Lecture 2
Financial markets and the economy, how securities are traded, buying on margin, short selling, and expected vs. realized return.

### HSI vs. S&P 500, week of Sep 14–18 (slides 4–5)
- The level correlation dipped to **0.52**.
- It was **a volatile week that ended almost flat**. The sequence was:
  1. Fears about AI, an oil shock and rising borrowing costs, followed by
  2. **a Fed rate hike**, followed by
  3. relief on oil prices and a rebound in tech stocks.

### The Fed raises rates (slide 7)
| | |
|---|---|
| **Rate hike** | +25 bps, to a target range of **3.75%–4.00%** |
| **Reason** | Inflation is still elevated, and the Fed wants a faster return to its **2% target** |
| **Signal** | Policy remains restrictive; future decisions are **data-dependent** |
| **Growth** | The economy is still expanding, at a moderate pace |
| **Jobs** | The labor market remains solid |
| **Market reaction** | US stocks **fell** after the announcement |

The chart of the federal funds target rate shows several phases:
- about 5.25% in 2006–07
- near 0% after the 2008 crisis
- a rise to about 2.4% in 2019
- back near 0% in 2020
- a rapid climb to about 5.5% in 2023
- cuts in 2024–25
- **a new hike in 2026**

### Why a US decision affects Hong Kong (slide 8)
- Hong Kong runs the **Linked Exchange Rate System (LERS)**: the HKD is **pegged to the USD** within a band of **7.75–7.85**.
- Under LERS, the **HKMA** sets its **Base Rate** using a **pre-set formula** closely tied to the Fed's target range. As a result, short-term HKD interest rates tend to track US rates.
- **Result:** on **Sep 17, 2026**, after the Fed's hike, the HKMA set its **Base Rate at 4.25%**.
- **Why it matters:** higher local borrowing costs affect HK **property, banks, and overall market sentiment**.

> **▶ Beyond the slides:** under the formula, the Base Rate is the lower end of the Fed funds target range **plus 50 bps**: 3.75% + 0.50% = **4.25%**. (Strictly, it is the higher of this and an average of short-term HIBOR rates.) Hong Kong can't set its own rates independently while it keeps the peg. This is the "impossible trinity": a fixed exchange rate, free capital flows and independent monetary policy can't all coexist.

---

## 1. Value at Risk (VaR) (slides 9–13)

### What VaR is
- **Value at Risk is the cut-off for the lowest 5% of returns, i.e. the 5th percentile of the return distribution.**
- There is a **5% probability that the return will be lower than the VaR**.
- Standard deviation measures dispersion on *both* sides of the mean. VaR focuses only on the **downside tail**, which is the risk investors actually worry about.

### VaR under a normal distribution (slide 10)
$$\text{VaR}_{5\%} = \mu - 1.65 \sigma$$
**Example:** μ = 1%, σ = 2%, so VaR = 1% − 1.65 × 2% = **−2.3%**. In 5% of periods, you lose 2.3% or more.

The normal-curve picture shows these coverage ranges:
| Range | Probability inside | Probability in each tail |
|---|---|---|
| μ ± 1σ | 68% | 16% |
| μ ± 1.65σ | 90% | **5%** (this is the VaR cut-off) |
| μ ± 2σ (more precisely 1.96σ) | 95% | 2.5% |
| μ ± 3σ (more precisely 2.58σ) | 99% | 0.5% |

### VaR from realized returns (slide 11)
If realized returns are roughly normal, r ≈ N(R(r), s²). Replace the population parameters with sample statistics:
$$\text{VaR} \approx r_A - 1.65 s$$
Here r_A is the arithmetic mean of past returns and s is their sample standard deviation.

### Non-normal returns: fat tails (slide 12)
- Realized returns often have **"fat tails"**: extreme outcomes happen more often than the normal distribution predicts. In other words, the returns are **not normal**.
- When that happens, **mean and variance no longer fully describe returns**, and the formula μ − 1.65σ **understates** the true downside.
- **VaR is still informative because, defined as a percentile, it makes no assumption about the "true" distribution.** It is simply the 5th percentile of the returns you actually observe.

### Historical VaR example (slide 13)
With **100 observations**, rank the returns from highest to lowest:

| Rank | Return | |
|---|---|---|
| 1 | +10.1% | |
| 2 | +9.8% | |
| … | … | |
| **95** | **−7.0%** | 95% of the time, returns are better than the VaR |
| **96** | **−7.2%** | 5% of the time, returns are worse than the VaR |
| 97 | −8.0% | |
| 98–100 | … | |

**The VaR cut-off can be −7%, −7.2%, or the average of the two (−7.1%).** All three are acceptable conventions.

> **▶ Beyond the slides**
> - For a **1% VaR**, use μ − 2.33σ.
> - **VaR in dollars:** a HK$1m portfolio with a 5% VaR of −2.3% has a dollar VaR of **HK$23,000**. "Over one period, there is a 5% chance of losing HK$23,000 or more."
> - **A limitation:** VaR says *where* the tail begins but not *how bad* it gets. **Expected shortfall** (also called CVaR) is the *average* return in the worst 5% of outcomes. It is the natural next step.

---

## 2. Risky vs. risk-free prospects and the risk premium (slides 14–16)

### Setup (slide 15)
You invest W = $100.

| Prospect | State | Probability | Outcome | Return |
|---|---|---|---|---|
| **Risky** | good (g) | 60% | $150 | +50% |
| | poor (p) | 40% | $80 | −20% |
| **Risk-free** (government debt) | any state | 100% | $105 | 5% |

**Statistics of the risky prospect**
$$E[r] = 0.6(50\%) + 0.4(-20\%) = 30\% - 8\% = \mathbf{22\%}$$
$$\sigma^2 = 0.6(0.50 - 0.22)^2 + 0.4(-0.20 - 0.22)^2 = 0.04704 + 0.07056 = 0.1176$$
$$\sigma = \sqrt{0.1176} = \mathbf{34\%}$$
The risk-free prospect has E[r] = 5% and σ = 0%.

### The risk premium (slide 16)
$$\text{Risk premium} \equiv E[r] - r_f = 22\% - 5\% = \mathbf{17\%}$$
**The risk premium is the return (reward) for the risk you take.** It is the extra expected return you get for bearing risk instead of holding a T-bill.

> **▶ Beyond the slides:** the **excess return** is the *realized* return minus r_f. The **risk premium** is the *expected* excess return. Only investors who are not risk-neutral need a positive risk premium before they will hold a risky asset (see §3).

---

## 3. Risk preferences and utility (slides 17–20)

### The utility score, or certainty equivalent (slide 18)
- The utility score combines three things into a **single preference score** for a security or portfolio: **risk aversion**, **expected return** and **risk**.
- It helps **predict** how an investor will invest, and helps **advise** investors on what they should do.

$$\boxed{U = E[r] - \tfrac{1}{2} A \sigma^2 = CE}$$
**A** measures the investor's **risk aversion**.

| Value of A | Investor type |
|---|---|
| A > 0 | **Risk averse.** Risk *lowers* utility. |
| A = 0 | **Risk neutral.** Only E[r] matters. |
| A < 0 | **Risk loving.** Risk *raises* utility. |

⚠️ **Units:** use decimals in the formula. For example, σ = 34% means σ² = 0.34² = 0.1156, **not** 1156.

### The certainty equivalent (slide 19)
- The **certainty equivalent** is the hypothetical **risk-free return that would make you indifferent** between the risk-free prospect and the risky one.
- **Decision rule:** compare U with the actual risk-free rate. If U > r_f, choose the risky prospect. If U < r_f, choose the risk-free one.
- Because **different people have different risk aversions (A)**, the same risky prospect has a **different certainty equivalent for each person**.

### Utility and investment choice (slide 20)
Take E[r] = 22%, σ = 34% and R_F = 5%. Then U = 22% − ½ × A × 0.1156.

| A | U | Compared with R_F = 5% | Choice |
|---|---|---|---|
| 1 | 22% − 5.78% ≈ **16%** | > 5% | **Risky** prospect |
| 2 | 22% − 11.56% ≈ **10%** | > 5% | **Risky** prospect |
| 3 | 22% − 17.34% ≈ **4.7%** (the slide shows 4%) | < 5% | **Risk-free** prospect |

**The moral: different investors make different choices.**

> **▶ Beyond the slides: the break-even A**
> The investor is indifferent when 0.22 − ½A(0.1156) = 0.05, which gives A = 0.17 / 0.0578 ≈ **2.94**. Anyone with A below 2.94 takes the risky prospect, and anyone above 2.94 takes the T-bill.

---

## 4. Mean–variance analysis and indifference curves (slides 21–27)

### Utility indifference
An **indifference curve** is the set of (σ, E[r]) combinations that are **equally agreeable** to a given investor, meaning they give the **same utility U**. Rearranging the utility formula:
$$E[r] = U + \tfrac{1}{2}A\sigma^2$$

The three slides fix **U = 2%** and vary σ:

| σ | **Risk averse** (A = 4) | **Risk neutral** (A = 0) | **Risk loving** (A = −4) |
|---|---|---|---|
| 0% | 2.0% | 2.0% | 2.0% |
| 5% | 2.5% | 2.0% | 1.5% |
| 10% | 4.0% | 2.0% | 0.0% |
| 15% | 6.5% | 2.0% | −2.5% |
| **Shape** | Upward-sloping and convex | Flat | Downward-sloping |
| **Meaning** | Demands **more** return as risk rises | Demands **neither more nor less** | Demands **less** return as risk rises |

(Check one entry: for A = 4 and σ = 10%, E[r] = 2% + ½ × 4 × 0.01 = 2% + 2% = 4%.)

**On the combined chart (slide 25):**
- **Along one curve**, every point gives the *same utility*. For example, on the A = 4 curve, (σ ≈ 11%, E[r] ≈ 4.5%) and (12.5%, 5.1%) are equally good.
- **At the same σ** (say 10%), the three investors need very different returns to reach U = 2%: 4%, 2% and 0% respectively.
- **Curves higher up and to the left** represent higher utility for a risk-averse investor.

### The mean–variance criterion (slide 26)
Start from a portfolio P at (σ_P, E[r_P]). Which directions are **better**?

| Direction | Risk-averse investor | Risk-neutral investor | Risk-loving investor |
|---|---|---|---|
| **North** (higher E[r], same σ) | better | **better** | better |
| **Northwest** (higher E[r], lower σ) | **better** | better | ambiguous |
| **Northeast** (higher E[r], higher σ) | ambiguous | better | **better** |
| **South** | worse | **worse** | worse |
| **Southeast** (lower E[r], higher σ) | **worse** | worse | ambiguous |
| **Southwest** (lower E[r], lower σ) | ambiguous | worse | **worse** |

(The slide highlights the bold cell in each row as the "defining" direction for each type.)

> **▶ Beyond the slides: the formal criterion for risk-averse investors**
> Portfolio A **dominates** portfolio B if E[r_A] ≥ E[r_B] **and** σ_A ≤ σ_B, with at least one inequality strict. Moving northwest is always an improvement. A northeast or southwest move can't be ranked without knowing A.

### Lotteries: a puzzle for mean–variance analysis (slide 27)
Compare two games:
1. **Mark Six:** pay HK$10 for a small chance of winning HK$100m.
2. **"Reverse" Mark Six:** receive HK$10, but with a small chance you must pay HK$100m.

- **The two games have the same standard deviation.** They are mirror images of each other.
- Most people happily play Game 1 and would refuse Game 2. Mean–variance analysis can't explain this, because the variance is identical.
- **The explanation is that lottery payoffs are not normally distributed.** Game 1 has a long right tail (positive skewness) and Game 2 has a long left tail (negative skewness). People like positive skewness and dislike negative skewness, so mean and variance are not enough.

> **▶ Beyond the slides:** this links back to VaR. Game 2's 5% VaR looks harmless, because the disaster happens much less than 5% of the time, yet the loss could be HK$100m. Tail measures and skewness matter when returns are far from normal.

---

## 5. Levels of the allocation decision (slides 28–29)

```
Complete Portfolio
├── Risky Assets  ──┐                       ┐
│   ├── Stocks      │  Security selection   │
│   ├── Bonds       │  (optimal weights     │  Asset allocation
│   └── Others      ┘   WITHIN risky assets)│  (optimal weights between
└── Risk-free Assets                        ┘   risky and risk-free assets)
```

- **Asset allocation** (also called **capital allocation**): how to split money between the **risky portfolio** and **risk-free assets**. This is the choice of y.
- **Security selection**: the optimal weights **within** the risky assets, across stocks, bonds and other assets.
- This lecture covers the **first** decision: we take the risky portfolio P as given and choose how much to put in it. Later lectures cover how to build P.

---

## 6. Return and risk of the complete portfolio (slides 30–33)

**Notation:** y is the fraction of wealth in the risky portfolio P, and (1 − y) is the fraction in the risk-free asset F.

### Expected return (slide 31)
$$E(r_C) = y E(r_P) + (1-y) r_f$$
$$\Rightarrow\; E(r_C) = r_f + y [E(r_P) - r_f]$$
The second form has three parts:
- **r_f** is the risk-free return: the reward for **inflation and deferred consumption, without risk**.
- **y** is the risk weight: the **quantity** of risk you take.
- **[E(r_P) − r_f]** is the **risk premium**: the reward for taking risk, or the **price** of risk.

### Risk (slide 32)
$$\sigma_C^2 = y^2\sigma_P^2 + (1-y)^2\sigma_f^2 + 2y(1-y)\sigma_{Pf}$$
**By definition σ_f = 0 and σ_Pf = 0**, because the risk-free rate doesn't vary. So:
$$\sigma_C^2 = y^2\sigma_P^2 \;\Rightarrow\; \boxed{\sigma_C = y \sigma_P}$$

**Example:** E(r_P) = 15%, σ_P = 22% and r_f = 7%.
1. E(r_C) = 7% + y × 8%
2. σ_C = y × 22%

### The Capital Allocation Line (CAL) (slide 33)
Combine the two equations by substituting y = σ_C / σ_P:
$$E(r_C) = r_f + \underbrace{\frac{E(r_P) - r_f}{\sigma_P}}_{S} \sigma_C$$
- The CAL is a **straight line** from F at (0, r_f) through P at (σ_P, E(r_P)).
- **Its slope is the Sharpe ratio**, also called the **reward-to-variability ratio**:
$$S = \frac{E(r_P) - r_f}{\sigma_P} = \frac{8\%}{22\%} \approx 0.36$$
  The Sharpe ratio is the extra expected return per unit of risk.

| Region | y | Return | Risk | Meaning |
|---|---|---|---|---|
| At F | y = 0 | E(r_C) = r_f | σ_C = 0 | All in the risk-free asset |
| **Unlevered** | 0 ≤ y ≤ 1 | r_f ≤ E(r_C) ≤ E(r_P) | 0 ≤ σ_C ≤ σ_P | Lending at r_f |
| At P | y = 1 | E(r_C) = E(r_P) | σ_C = σ_P | All in P |
| **Levered** (margin buying) | y > 1 | E(r_C) > E(r_P) | σ_C > σ_P | Borrowing at r_f to buy more of P |

> **▶ Beyond the slides: worked points on the CAL** (with r_f = 7%, E(r_P) = 15%, σ_P = 22%)
>
> | y | E(r_C) = 7% + 8%·y | σ_C = 22%·y | Note |
> |---|---|---|---|
> | 0 | 7% | 0% | T-bills only |
> | 0.5 | 11% | 11% | Half in P, half in T-bills |
> | 1 | 15% | 22% | All in P |
> | 1.5 | 19% | 33% | Borrow 50% of wealth and invest 150% in P |
>
> Every point has the same Sharpe ratio, 0.36: for example, (11 − 7)/11 = (19 − 7)/33 = 0.36.
>
> **The kinked CAL:** in practice, individuals borrow at a rate **higher** than r_f (say 9%). The levered part then has a smaller slope, (15 − 9)/22 = 0.27, so the CAL bends at P.
>
> **Preview: choosing the best y.** Maximize U = r_f + y[E(r_P) − r_f] − ½A y²σ_P². This gives
> $$y^* = \frac{E(r_P) - r_f}{A \sigma_P^2}$$
> For A = 4: y* = 0.08 / (4 × 0.0484) = **0.41**, so put 41% in P and 59% in T-bills. A less risk-averse investor with A = 1.5 gets y* = 1.10 and borrows. Graphically, y* is where an indifference curve is **tangent** to the CAL.

---

## 7. Formula sheet

| Concept | Formula |
|---|---|
| VaR (5%, normal) | μ − 1.65σ, or r_A − 1.65s using sample data |
| Historical VaR | The 5th-percentile ranked return |
| Expected return | E[r] = Σ p(s)·r(s) |
| Variance | σ² = Σ p(s)·[r(s) − E[r]]² |
| Risk premium | E[r] − r_f |
| Utility / certainty equivalent | U = E[r] − ½Aσ² |
| Indifference curve | E[r] = U + ½Aσ² |
| Complete portfolio return | E(r_C) = r_f + y[E(r_P) − r_f] |
| Complete portfolio risk | σ_C = yσ_P |
| Sharpe ratio (slope of the CAL) | S = [E(r_P) − r_f] / σ_P |
| CAL | E(r_C) = r_f + S·σ_C |

---

## 8. Self-test

1. Monthly returns have μ = 1.5% and σ = 4%. Compute the 5% VaR assuming normality.
2. You have 200 ranked return observations. Which rank(s) define the 5% historical VaR?
3. Why does μ − 1.65σ understate downside risk when returns have fat tails?
4. A stock pays +40% with probability 0.5 and −10% with probability 0.5. The risk-free rate is 4%. Compute E[r], σ and the risk premium.
5. For the stock in Q4, find U for A = 2 and A = 6. Which investor holds the stock?
6. Draw (or describe) the indifference curves of risk-averse, risk-neutral and risk-loving investors. Which way do they slope?
7. Portfolio X has E[r] = 10% and σ = 15%. Portfolio Y has E[r] = 12% and σ = 20%. Can a risk-averse investor rank them without knowing A? What about a risk-neutral investor?
8. Why can't mean–variance analysis explain why people buy lottery tickets?
9. r_f = 3%, E(r_P) = 11% and σ_P = 20%. You put 70% in P. Compute E(r_C), σ_C and the Sharpe ratio.
10. In Q9, what y gives σ_C = 30%? Is that position levered or unlevered?
11. In Q9, what is the optimal y* for an investor with A = 2.5?

<details>
<summary>Answers</summary>

1. VaR = 1.5% − 1.65 × 4% = **−5.1%**.
2. 5% of 200 = 10, so the cut-off lies between ranks **190 and 191**. Use either return or their average.
3. Extreme losses are more frequent than the normal distribution assumes, so the true 5th percentile lies further left.
4. E[r] = 0.5(40) + 0.5(−10) = **15%**. σ² = 0.5(0.25)² + 0.5(−0.25)² = 0.0625, so σ = **25%**. Risk premium = 15% − 4% = **11%**.
5. With A = 2: U = 0.15 − 0.0625 = **8.75%** > 4%, so this investor holds the stock. With A = 6: U = 0.15 − 0.1875 = **−3.75%** < 4%, so this investor holds T-bills.
6. Risk-averse curves slope **upward** and are convex. Risk-neutral curves are **flat**. Risk-loving curves slope **downward**.
7. Risk-averse investor: **no**, because Y has more return *and* more risk (a northeast move), so it depends on A. Risk-neutral investor: **yes, Y is better**, because only E[r] matters.
8. Lottery payoffs are highly skewed and not normal. A lottery and its mirror image have the same variance, yet people prefer the positively skewed one. Mean and variance miss skewness.
9. E(r_C) = 3% + 0.7 × 8% = **8.6%**. σ_C = 0.7 × 20% = **14%**. S = 8/20 = **0.40**.
10. y = 30/20 = **1.5**. That is **levered**: you borrow 50% of your wealth at r_f.
11. y* = 0.08 / (2.5 × 0.04) = **0.8**.
</details>
