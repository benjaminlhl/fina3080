# FINA 3080 — Week 1 Notes
## Lecture 1: Syllabus review, course overview, securities indexes

*Investment Analysis and Portfolio Management · Instructor: Chao Ying (CUHK)*

> **How to read these notes:** everything in the main text comes from the slides. Parts marked **▶ Beyond the slides** are extra explanation and worked examples I added to fill gaps. They follow the optional textbook (BKM Ch. 1–2) but were not explicitly presented in lecture.

---

## 0. Opening example: HSI vs. S&P 500 (slides 2 and 27)

The lecture opens with a chart of the **Hang Seng Index (HSI)** and the **S&P 500** from 29 Jun to 4 Sep 2026.

- **Level correlation = 0.54.** The two indexes *usually* move in the same direction.
  - Note on the chart: this is a correlation of **price levels**, not of **returns**. The two markets also trade in different time zones, so HK often reacts to the *previous night's* US session.
- **The two markets diverged in July:**
  - **17 July:** the Philadelphia Semiconductor Index (mostly US AI and semiconductor stocks) fell more than 18%. The S&P 500 dropped sharply while the HSI kept rising, because the HSI has little exposure to US chip stocks.
- **3 Aug:** the S&P 500 jumped on news of US–Iran negotiations and Big Tech earnings that came in better than expected.
- **The latest week (31 Aug – 4 Sep):**
  - **Sep 1:** renewed US–Iran conflict raised concerns about oil prices.
  - **Sep 3:** Fed Governor Waller signalled he might support holding rates unchanged.
  - **Sep 4 (HK):** Hong Kong reacted at the open to the US rally of the previous night.
  - **Sep 4 (US):** the August payroll report surprised investors before the US open.

**Takeaway:** indexes respond to news, and markets are linked. The links are imperfect, though: sector exposure and time zones matter.

---

## 1. What is an investment? (slides 3–5)

**Definition:** an investment is a **current commitment of money (or other resources) made in the expectation of future benefits.**

The definition has two key ideas:

| Idea | Meaning |
|---|---|
| **Current vs. future** | You give something up now and get something back later. |
| **Expectation** | The future benefits are **uncertain**, so risk is unavoidable. |

### The HK$10,000 thought experiment
Suppose you wake up one day and find you are HK$10,000 richer. Should you invest it or consume it?

**The instructor's answer is to keep the same portfolio weights.**

| | Stock (50%) | Bond (30%) | Cash (20%) | Total |
|---|---|---|---|---|
| Before | $500,000 | $300,000 | $200,000 | $1,000,000 |
| After +$10,000 | $505,000 | $303,000 | $202,000 | $1,010,000 |

**Point of the example:** a small windfall does not need to change your strategy. Your asset allocation reflects your preferences (risk tolerance, horizon), so new money is allocated **in proportion** to it. The **portfolio weights**, not the dollar amounts, are what define your investment decision.

---

## 2. Course logistics (slides 7–12)

### People
- **Instructor:** Chao YING (chaoying@cuhk.edu.hk)
- **TA:** Yiwei Liang (yiweiliang@**link**.cuhk.edu.hk). Note the `link.` in the address.

### Prerequisites you should already know
Expected value, standard deviation, covariance, regression, discount rate, net present value (NPV).

> **▶ Beyond the slides: quick refresher**
> - **Expected value:** E[R] = Σ pₛ·Rₛ
> - **Variance / std. dev.:** σ² = Σ pₛ·(Rₛ − E[R])², σ = √σ²
> - **Covariance:** Cov(R₁,R₂) = Σ pₛ·(R₁ₛ − E[R₁])(R₂ₛ − E[R₂]); correlation ρ = Cov/(σ₁σ₂)
> - **NPV:** NPV = −C₀ + Σ CFₜ/(1+r)ᵗ, where r is the discount rate
> - **Regression:** Rᵢ = α + β·R_M + ε. This is the basis for "beta", which appears later in the course.

### Materials
- **Optional textbook:** Bodie, Kane & Marcus (BKM), *Investments*, 12th ed. Readings are listed in the syllabus, and all are optional.
- **Slides** are posted on Blackboard (https://blackboard.cuhk.edu.hk/) **at least 24 hours before** each lecture. There are two versions: one **before** the lecture and one **after**, with additional slides.

### Grading

| Component | Weight | Details |
|---|---|---|
| Homework | **15%** | 2 group assignments, 4–6 students per group (groups formed after add/drop) |
| Peer evaluation | **5%** | You evaluate your teammates at the end of the semester |
| Midterm exam | **35%** | **Oct 20, 7–9 pm, LSK LT6** (no class that day) |
| Final exam (cumulative) | **45%** | **Dec 1, 7–9 pm, LSK LT6** (no class that day) |
| Participation | bonus* | Only upgrades your grade, never downgrades it. Decided by the instructor, who adds up to "5% of your final exam score". |

⚠️ **Exam conflicts** had to be reported to the TA by **Tuesday, September 22**.

---

## 3. Course overview: what FINA 3080 is about (slides 6, 13–22)

**The goal is to learn how to invest wisely in an uncertain environment. The course is *not* about predicting the future.**

It covers four fundamental areas:
1. Asset classes and financial markets
2. **Money allocation:** how to split money across assets
3. **Asset pricing:** how to find the fair price of a security
4. **Portfolio evaluation:** how to judge portfolio managers

### 3.1 Money allocation (slide 14)
- Allocate money across different assets and securities.
- **The risk–return relationship:** a higher expected return comes with higher risk.
- The course is **not** about getting rich quickly. Gambling is the fastest way to get rich, and it is also the fastest way to lose.
- **Use diversification to reduce risk** ("don't put all your eggs in one basket"). The idea is linked to **Harry Markowitz** (Nobel 1990), the founder of modern portfolio theory.

> **▶ Beyond the slides: why diversification works**
> For two assets with weights w₁ and w₂:
> σ²ₚ = w₁²σ₁² + w₂²σ₂² + 2w₁w₂ρσ₁σ₂
> When ρ < 1, the portfolio's σ is **less than** the weighted average of the individual σ's. You lower risk without giving up expected return. This is the foundation of the money-allocation part of the course.

### 3.2 Asset pricing: the Law of One Price (slides 15–19)
- The main question is how to determine the **fair price** of a security.
- **Key concept: the Law of One Price (LOOP).** Identical goods or assets should sell for the same price everywhere, after converting currencies and **net of transaction costs**.
- Associated names: **William Sharpe** (Nobel 1990, CAPM) and **Eugene Fama** (Nobel 2013, efficient markets).

#### Example 1: the Big Mac Index (Jan 2022, in USD)
| Switzerland | US (base) | Europe | UK | Singapore | Thailand | China | Japan | Vietnam | Philippines | Malaysia | Indonesia | Russia |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| $6.94 | $5.81 | $5.08 | $4.74 | $4.33 | $4.06 | $3.63 | $3.59 | $2.98 | $2.85 | $2.40 | $2.36 | $1.86 |

- **Does this violate the LOOP?** On the surface it does: the same burger costs nearly 4× more in Switzerland than in Russia.
- **Can you profit from it?** No. You can't buy Big Macs in Moscow and ship them to Zurich. Transport costs, perishability and local costs (wages, rent) eat up the difference.
- **Slide's key point:** "Price difference is close to transaction cost." Once trading costs are counted, buying low and selling high is not profitable.

#### Example 2: Big Mac Index vs. iPad mini ("Mini Mac") Index (slide 17)
- Measured by the **Big Mac**, many currencies look 20–70% under- or overvalued against the USD (Russia and Malaysia are extreme cases).
- Measured by the **iPad mini**, most deviations are within **0 to −20%**.
- **Why the difference?** An iPad is a **highly tradable** good: it is easy to ship and identical everywhere. Arbitrage pressure keeps its prices close together. A Big Mac is not tradable, so its price gaps can persist.
- **Lesson:** the LOOP holds more tightly when trading is cheaper and easier.

#### Example 3: wholesale prices of cocaine, per kg (UNODC, 2019)
- Colombia **$1,500**, Mexico $12k, El Salvador $29k, Australia $152k, Algeria $167k, Jordan $169k, **Kuwait $214k**.
- That is a gap of more than 100×. "Transaction costs" here include enormous **legal risk** and barriers to transport.
- **Lesson:** large price gaps can persist when the costs or risks of arbitrage are high. LOOP is a statement about prices *net of* trading frictions.

#### Arbitrage (slide 19)
- **A violation of the LOOP is an arbitrage opportunity.**
- **Arbitrage** is a "free lunch": a **zero-risk, zero-net-investment** strategy that still generates profits.
- **How do you profit?** Buy low and sell high at the same time.
- **What happens next?** Traders buy the cheap asset, which pushes its price up, and sell the expensive one, which pushes its price down. **Prices converge and arbitrage profits disappear.**

> **▶ Beyond the slides: a numerical arbitrage example**
> Suppose a stock trades at HK$50 in Hong Kong and at the equivalent of HK$52 in London, with HK$0.50 per share in total transaction costs.
> Buy in HK at 50, sell in London at 52, and you earn 52 − 50 − 0.50 = **HK$1.50 per share** with no risk and no net capital.
> As everyone does this, the HK price rises and the London price falls until the gap is ≤ HK$0.50. At that point no profitable arbitrage remains.

### 3.3 Market efficiency (slide 20)
**Example:** HSBC trades at $60, and you somehow know its "true" value is $100.
- **What should you do?** Buy HSBC.
- **What happens?** You and everyone with the same information keep buying until **HSBC's price rises to $100**.

**Efficient market:** prices **reflect all available information.** Once information is public, trading quickly builds it into the price, so the information no longer earns an easy profit.

> **▶ Beyond the slides: the three forms of the Efficient Market Hypothesis (Fama)** (covered in detail later)
> - **Weak form:** prices reflect all past price and volume data, so technical analysis doesn't work.
> - **Semi-strong form:** prices reflect all *public* information, so fundamental analysis of public data doesn't work.
> - **Strong form:** prices reflect *all* information, including private information, so even insiders can't beat the market.

### 3.4 Portfolio evaluation: luck or skill? (slides 21–22)
- Financial markets are **not 100% efficient.**
  - Some investors *can* earn higher returns thanks to better information or skill.
  - High returns could also be due to **luck**.
- **The central problem is to separate luck from skill.**

**The fund-manager puzzle:** how could a fund manager *always* give some investors "accurate" predictions in order to attract them?

**The coin-flip demonstration (slide 22):** the class has 143 students, identified by student ID.
1. Tell **half** the class "the market will go **up**" and the other half "it will go **down**".
2. Suppose the market goes down. Discard the 71 who received the wrong call. **72** people have now seen a correct prediction.
3. Split those 72 again: 36 get "up" and 36 get "down". The market goes down, so **36** people have now seen 2 correct calls in a row.
4. Split again: 18 get "up" and 18 get "down". After this round, **18** people have seen **3 out of 3** correct predictions.

To those 18 people the "manager" looks like a genius, but every prediction was a **coin flip**.

> **▶ Beyond the slides: why this matters**
> - Starting with N people, after k rounds about N/2ᵏ people have seen a perfect record. With 10,000 people and 5 rounds, about 312 people see 5 correct calls in a row by pure chance.
> - The same logic applies to the *industry*. With thousands of funds, some will have outstanding track records by luck alone. This is called **survivorship bias** or **selection bias**: we only notice the winners.
> - Later in the course we will use statistical tools (alpha, t-statistics, Sharpe ratio) to test whether performance is *significantly* better than luck.

---

## 4. Securities indexes (slides 23–26)

### Why use indexes?
1. To **track** how securities are doing on average (a market barometer)
2. To **compare** the performance of managers (a benchmark)
3. To serve as the **base for derivatives** (index futures, options, ETFs)

### Kinds of indexes

| Dimension | Example | vs. | Example |
|---|---|---|---|
| Asset class | **Stocks:** DJI, HSI | vs. | **Bonds:** Barclays Capital, Merrill Lynch indexes |
| Breadth | **Narrow:** DJI (30 stocks), HSI | vs. | **Broad:** S&P 500, HSCI |
| Size | **Large cap:** DJI, HSI | vs. | **Small cap:** S&P 600 |
| Coverage | **General:** DJI, HSI | vs. | **Sectoral:** HSI-Finance |
| Geography | **Country:** DJI, HSI | vs. | **Regional:** MSCI indexes |

### Value-weighted indexes (slide 25)
A value-weighted index is the **average return of the index stocks, weighted by market value (market capitalization).**

Examples:
- **Hang Seng Index:** 82 large HK stocks
- **S&P 500**

**Formula:** the index compares today's total market cap with its initial level.

$$
I_t^V = \frac{\sum_{i=1}^{N} Q_{it} \times P_{it}}{\sum_{i=1}^{N} Q_{i0} \times P_{i0}} \times 100
$$

- Qᵢₜ is the number of shares of stock *i* outstanding at time *t*.
- Pᵢₜ is the price of stock *i* at time *t*.
- The base period (t = 0) is set to 100.

**Properties:**
- It reflects a **buy-and-hold strategy**: holding every stock in proportion to its market cap. You don't need to rebalance when prices move.
- It is **unaffected by stock splits**, because a split changes Q and P in offsetting ways and market cap stays the same.
- Weights are proportional to **market cap**, so big companies dominate the index.

> **▶ Beyond the slides: worked example**
>
> | Stock | Q₀ | P₀ | Cap₀ | P₁ | Cap₁ |
> |---|---|---|---|---|---|
> | A | 100 | $10 | $1,000 | $12 | $1,200 |
> | B | 50 | $40 | $2,000 | $38 | $1,900 |
> | **Total** | | | **$3,000** | | **$3,100** |
>
> I₁ = 3,100 / 3,000 × 100 = **103.33**, so the index rose 3.33%.
> - A rose 20% and B fell 5%, but B is twice A's size. The weighted return is (1/3)(20%) + (2/3)(−5%) = **3.33%**, which matches.
> - **Split check:** if B splits 2-for-1, it has 100 shares at $19, and its cap is still $1,900. The index doesn't change. ✔
>
> **Contrast: a price-weighted index (e.g., the Dow Jones Industrial Average).**
> A price-weighted index is the simple average of prices: (12 + 38)/2 vs. (10 + 40)/2 gives 25/25, so 0% change. High-*priced* stocks dominate regardless of company size. Splits change the average price, so the divisor must be adjusted after every split.
>
> **Equal-weighted index:** a simple average of returns, (20% − 5%)/2 = 7.5%. To keep weights equal, you must rebalance continuously.

### HSI vs. Hang Seng Composite Index (HSCI) (slide 26)

| Feature | Hang Seng Index (HSI) | Hang Seng Composite Index (HSCI) |
|---|---|---|
| Number of stocks | ~80 (select group) | ~500 (much broader) |
| Coverage | Top large-cap companies | Large, mid and small cap |
| Scope | Narrow ("blue-chip" segment) | Broad ("entire market" of eligible stocks) |
| Purpose | Main benchmark and barometer of the HK economy | Comprehensive market gauge; underlying universe for other indexes |
| Representativeness | Major, influential companies | Overall listed equity market |
| Relationship | Constituents are largely a **subset** of the largest HSCI companies | The **parent universe** from which the HSI and other indexes are derived |

---

## 5. Quick review questions (self-test)

1. What two features distinguish an investment from consumption?
2. You receive a HK$20,000 bonus and hold 60/30/10 stock/bond/cash out of $500,000 of wealth. How much goes into each asset class if you keep your weights?
3. Define arbitrage. Why does it disappear quickly in liquid financial markets?
4. Why does the iPad mini index show much smaller "currency misvaluations" than the Big Mac index?
5. Wholesale cocaine is about 140× more expensive in Kuwait than in Colombia. Does this disprove the LOOP? Explain.
6. HSBC trades at $60 and you know its true value is $100. What do you do, and what happens to the price? What does this imply about efficient markets?
7. A newsletter has correctly called the market direction 6 months in a row. Why might that be meaningless?
8. Two stocks: X has 200 shares at $5 → $6; Y has 100 shares at $30 → $27. Compute the value-weighted index at t = 1 (base 100). What happens if X does a 2-for-1 split?
9. Give three reasons we construct securities indexes.
10. How is the HSI related to the HSCI?

<details>
<summary>Answers</summary>

1. Sacrificing resources **now** for **uncertain** future benefits (the current-vs-future trade-off and expectation/uncertainty).
2. Total $520,000 → Stock $312,000, Bond $156,000, Cash $52,000. The additions are +$12,000, +$6,000 and +$2,000.
3. A zero-risk, zero-net-investment strategy with a positive profit. When everyone buys low and sells high, prices converge and the gap closes.
4. iPads are cheap to ship and identical worldwide, so arbitrage keeps prices aligned. Big Macs are not tradable.
5. No. The LOOP holds *net of transaction costs*, and here those costs include huge legal risk and smuggling costs.
6. Buy. Buying pressure pushes the price to $100. In an efficient market, prices reflect all available information, so such gaps don't persist.
7. With enough newsletters, some will hit 6/6 by luck alone (1/64 chance each). This is selection bias, and you need to separate luck from skill.
8. Cap₀ = 1,000 + 3,000 = 4,000. Cap₁ = 1,200 + 2,700 = 3,900. I₁ = **97.5**. The split doesn't change the index (400 shares × $3 = $1,200).
9. To track average performance, to benchmark managers, and to serve as the underlying for derivatives.
10. The HSCI is the broad parent universe (~500 stocks). The HSI (~80 blue chips) is largely a subset of the largest HSCI constituents.
</details>

---

## 6. One-paragraph summary

FINA 3080 teaches how to invest sensibly under uncertainty, not how to forecast. An investment trades certain resources today for uncertain benefits later, and allocation decisions are about **weights**. The course has four pillars:
- **Money allocation:** the risk–return trade-off and diversification (Markowitz).
- **Asset pricing:** the Law of One Price and arbitrage (Sharpe, Fama). Price gaps persist only when trading costs or risks are high.
- **Market efficiency:** prices reflect available information.
- **Portfolio evaluation:** separating luck from skill. The coin-flip demonstration shows how a "perfect" track record can be pure luck.

Indexes such as the value-weighted HSI and S&P 500 measure the market, benchmark managers and serve as the underlying for derivatives. A value-weighted index equals a buy-and-hold market-cap portfolio and is unaffected by stock splits.
