# FINA 3080 — Week 6 Notes
## Lecture 6: Multifactor models, APT and portfolio performance evaluation

*Investment Analysis and Portfolio Management · Instructor: Chao Ying (CUHK)*

> **How to read these notes:** everything in the main text comes from the slides. Parts marked **▶ Beyond the slides** are my own explanations and worked examples (BKM Ch. 10 and 24).
>
> ⭐ **This lecture was not on the midterm (which covered Lectures 1–5), so expect it to be weighted heavily on the final.** The APT arbitrage table and the three performance measures are prime exam material.

**Today's outline**
1. Multifactor models and Arbitrage Pricing Theory (APT)
2. Performance evaluation overview
3. Performance measures that adjust for risk
4. Application: mutual funds

---

## 0. Announcements and market update (slides 2–4)
- Homework 1 solution and grades, and the **midterm solution**, are on Blackboard. Midterm grades will be posted before Nov 3.
- **Oct 6–9:** tech optimism → AI stocks and HK internet companies rebound.
- **Oct 14–15:** US **CPI +0.6%** → Fed-hike fears rise → US stocks fall; **HK reacts the next morning** (time zones again).
- **Oct 16:** worries about AI financing + higher oil → US tech falls.
- **Oct 22–23:** Meta reported Q3 capital expenditure of about **$34.91 billion** after the US close on Oct 21 → renewed worries about the **scale and profitability of AI spending**.

---

## 1. Multifactor models (slides 6–8, recap from Lecture 5)

**Single-factor (CAPM) model:**
$$(\tilde r_i - r_f) = \alpha_i + \beta_i(\tilde r_M - r_f) + \tilde e_i, \qquad \text{Corr}(\tilde r_M, \tilde e_i) = 0$$

**Multifactor model:**
$$r_{it} - r_f = \alpha_i + \beta_{i1}(r_{1t} - r_f) + \dots + \beta_{in}(r_{nt} - r_f) + e_{it}$$
with **α_i = 0 in equilibrium**.

**Fama–French three factors:** market excess return, **SMB** (small − big), **HML** (high − low book-to-market).

---

## 2. Arbitrage Pricing Theory (APT) (slides 9–20)

### The idea (slide 9)
- **Multifactor models are a result of the APT.**
- When there is **mispricing (α ≠ 0)**, investors can form **arbitrage strategies**.
- **Arbitrage** = **positive profit, without risk, without net investment** (same definition as Lecture 1).
- Given a riskless arbitrage, **every** investor wants to take an **infinite position**, regardless of risk aversion or wealth.
- This quickly **moves prices**, eliminates the opportunity and restores equilibrium.
- When no arbitrage opportunities exist, markets satisfy the **"no-arbitrage condition."**

### Implications (slide 10)
Take expectations of the model (E(e) = 0):
$$E(r_i) - r_f = \alpha_i + \beta_{i1}[E(r_1) - r_f] + \dots + \beta_{in}[E(r_n) - r_f]$$
- **High betas → high expected returns.**
- **High firm-specific risk → not compensated** (you can diversify it away for free).
- People should hold **diversified portfolios** → **passive investing**.

### Portfolio alpha, betas and firm-specific risk (slide 11)
"The good news is that they are all weighted sums":
$$\alpha_P = \sum w_i\alpha_i, \qquad \beta_{Pk} = \sum w_i\beta_{ik} \text{ for each factor } k$$
$$\sigma^2(e_P) = \sum w_i^2\,\sigma^2(e_i)$$
⚠️ Note the **squared** weights in the last one (firm-specific risks are uncorrelated, so no covariance terms). That's why σ²(e_P) shrinks toward zero in a large diversified portfolio.

### Factor portfolios (slide 12)
A **factor portfolio** is driven by **one factor alone**:
- **β = 1** on its own factor and **β = 0** on all the others;
- **no firm-specific risk**: σ²(e) = 0.
- There are as many factor portfolios as factors.

### Example: the APT expected return (slide 13)
Two-factor model. Factor portfolios: E(r_1) = 10%, E(r_2) = 12%. r_f = 4%.
Well-diversified portfolio A (σ²(e_A) = 0): β_A1 = 0.5, β_A2 = 0.75.
$$E(r_A) = r_f + \beta_{A1}[E(r_1) - r_f] + \beta_{A2}[E(r_2) - r_f] = 4\% + 0.5(6\%) + 0.75(8\%) = \mathbf{13\%}$$

### The arbitrage (slides 14–17)
Suppose A is actually expected to return **12%**. Then **α_A = 12% − 13% = −1%**: A is **overpriced** → **sell A**.

**Recipe:**
1. **Sell** the mispriced portfolio (w_A = −1).
2. **Buy** a replicating portfolio with the **same betas** using factor portfolios: w_1 = **β_A1 = 0.5**, w_2 = **β_A2 = 0.75**.
3. Use the **risk-free asset** to make the **net investment zero**: w_f = −(0.5 + 0.75 − 1) = **−0.25** (borrow).
4. Profit = −w_A × α_A … here (−1)(−1%) = **+1%**.

| Position | Weight | β₁ | β₂ | E(r) contribution |
|---|---|---|---|---|
| A | **−1** | −0.5 | −0.75 | −12% |
| Factor portfolio 1 | **+0.5** | +0.5 | 0 | +5% (0.5 × 10%) |
| Factor portfolio 2 | **+0.75** | 0 | +0.75 | +9% (0.75 × 12%) |
| Risk-free | **−0.25** | 0 | 0 | −1% (−0.25 × 4%) |
| **Total** | **0** (no net investment) | **0** | **0** (no factor risk) | **+1%** = alpha |

**Check list for any arbitrage table:** weights sum to **0**, every β sums to **0**, and the expected return is **positive**.

**Scale it up (slide 17):** multiply every weight by 100 (e.g., −$100 in A, +$50, +$75, −$25) → profit **+100%** of the $1 unit, i.e., $1 per $100 shorted. Since it is riskless and costless, everyone scales up until the price corrects.

### What about individual securities? (slides 18–19)
If A is a **single stock** rather than a well-diversified portfolio, the same trade leaves you exposed to **−e_A**, A's **firm-specific risk**:
| Position | Weight | β₁ | β₂ | Firm-specific |
|---|---|---|---|---|
| A | −1 | −0.5 | −0.75 | **−e_A** |
| FP1, FP2, r_f | 0.5, 0.75, −0.25 | +0.5 | +0.75 | 0 |
| **Total** | 0 | 0 | 0 | **−e_A** |

So it is **not riskless** → not a true arbitrage. The APT pricing holds for **well-diversified portfolios**, not necessarily each stock.

### APT vs. CAPM (slide 20)
| | **APT** | **CAPM** |
|---|---|---|
| Applies to | **Well-diversified portfolios**; not necessarily individual stocks | **All** assets, including individual stocks |
| Mispricing | Some individual stocks **can** be mispriced (off the SML) | Every asset on the SML in equilibrium |
| Market portfolio needed? | **No.** Gets E(r)–β relation without the market portfolio (no "demand = supply" assumption) | **Yes**, relies on everyone holding M |
| Factors | Can be extended to **multiple factors** | Single factor (the market) |
| Built on | **No-arbitrage** | Mean–variance optimisation and equilibrium |

APT is **more general**.

---

## 3. Performance evaluation overview (slides 22–24)
- Markets are **not 100% efficient**: some investors earn more thanks to information or skill, **but high returns can also be luck**. The key task is to **separate luck from skill**.
- The coin-flip mailing again (143 → 72 → 36 → 18 people see a perfect record by chance).
- **Two issues when a fund earns high returns:**
  1. **Adjust for risk**: high risk → high return, so raw returns mislead.
  2. **Luck or skill?** e.g., the **octopus** (Paul) that correctly "predicted" World Cup matches.

---

## 4. Risk-adjusted performance measures (slides 26–28)

All use **averages over the evaluation period**.

### Sharpe measure (reward-to-variability) (slide 26)
$$S_P = \frac{\bar r_P - \bar r_f}{\sigma_P}$$
- Excess return per unit of **total risk**.
- Use to evaluate **complete investment strategies** (e.g., your **whole** portfolio) or **diversified** portfolios.

### Jensen measure (alpha) (slide 27)
$$\alpha_P = \bar r_P - [\bar r_f + \beta_P(\bar r_M - \bar r_f)]$$
- The average return **above or below the CAPM prediction** (the term in brackets).
- Use to evaluate portfolios or securities, or to **gauge a manager's skill**.

### Information ratio (appraisal ratio) (slide 28)
$$I_P = \frac{\alpha_P}{\sigma(e_P)}$$
- α_P = Jensen's alpha; σ(e_P) = **non-systematic** (residual, firm-specific) risk.
- The return of the manager's **active portfolio** (the part not explained by the CAPM) divided by the **risk of that active portfolio**.
- Use to **gauge a manager's skill**.

**⚠️ The three measures can give different rankings** (slide 28). Know *why*: Sharpe penalises total risk, Jensen ignores risk size beyond β, IR scales alpha by the unsystematic risk taken to get it.

> **▶ Beyond the slides: which measure when?**
> | Situation | Use |
> |---|---|
> | The fund is your **entire** wealth | **Sharpe** (total risk is what you bear) |
> | The fund is **one of many** holdings in a diversified portfolio | **Jensen's α** (or Treynor = (r̄_P − r̄_f)/β_P, which uses only systematic risk) |
> | You want to combine an **active** fund with a passive index | **Information ratio** |
>
> **Treynor measure** T_P = (r̄_P − r̄_f)/β_P isn't on the slides, but it's the natural fourth measure in BKM Ch. 24.

### ▶ Worked example
r_f = 3%, market: r̄_M = 10%, σ_M = 18%.
| | r̄ | σ | β | σ(e) |
|---|---|---|---|---|
| Fund X | 14% | 25% | 1.2 | 8% |
| Fund Y | 10% | 15% | 0.7 | 5% |

| | Sharpe | Jensen α | Information ratio |
|---|---|---|---|
| X | 11/25 = **0.440** | 14 − (3 + 1.2 × 7) = **2.6%** | 2.6/8 = **0.325** |
| Y | 7/15 = **0.467** | 10 − (3 + 0.7 × 7) = **2.1%** | 2.1/5 = **0.420** |
| Market | 7/18 = 0.389 | 0 | — |

**Rankings differ:** Y wins on Sharpe and IR, X wins on Jensen's α. Both beat the market on all measures.

---

## 5. Application: mutual funds (slides 30–33)

### Active Share (slide 30)
$$\text{Active Share}_j = 0.5\sum_{i=1}^{N}\left|w_{j,i} - w_{b,i}\right|$$
- w_j,i = weight of stock i in fund j; w_b,i = weight in the **benchmark**; N counts every stock in either (a weight can be 0).
- **0** = the fund is identical to the benchmark (pure index). **1** = no overlap at all.
- The 0.5 is there because every over-weight is matched by an under-weight; without it you'd double count.

**Results with the HSI as benchmark (slide 31):**
| Fund | Active Share | Jensen's α |
|---|---|---|
| AIG Hong Kong Equity | 0.394 | 2.05% |
| BOCHK Investment Funds | 0.231 | 2.00% |
| Manulife Dragon Growth | 0.282 | 2.13% |
| **Schroder ISF HK Equity A** | **0.433** | **3.06%** |

- **All four outperformed the HSI.**
- **Corr(Active Share, Jensen's α) = 0.69**: the more active funds had higher alpha **in this sample**.

> **▶ Beyond the slides: worked Active Share**
> Benchmark: A 50%, B 30%, C 20%. Fund: A 40%, B 20%, D 40% (no C).
> |differences| = |0.4 − 0.5| + |0.2 − 0.3| + |0 − 0.2| + |0.4 − 0| = 0.1 + 0.1 + 0.2 + 0.4 = 0.8 → Active Share = **0.40**.

### Fees and performance (slide 32)
- **Expense ratio / distribution (12b-1) fee:** paid **every year**.
- **Front-end load / purchase fee:** paid when you **buy**.
- **Back-end load / redemption fee:** paid when you **sell**.
- These can be 0% for some funds but **5% or more** for some active funds.
- **Good performance may not persist.** Past alpha ≠ future alpha; the data show future performance is usually **not** as good.

### Active vs. passive (slide 33)
Expense ratios of equity mutual funds worldwide, 2000–2017:
- **Actively managed:** about 1.06% → **0.78%**.
- **Passively managed:** about 0.27% → **0.09%**.
- Passive funds are **far cheaper**, and the gap compounds every year.

---

## 6. Formula sheet

| Concept | Formula |
|---|---|
| APT expected return | E(r_P) = r_f + Σ β_Pk[E(r_k) − r_f] |
| Portfolio alpha / beta | α_P = Σw_iα_i; β_Pk = Σw_iβ_ik |
| Portfolio residual variance | σ²(e_P) = Σw_i²σ²(e_i) |
| Arbitrage weights | Sell 1 of A; buy β_A1 of FP1, …, β_An of FPn; risk-free = −(Σβ − 1) |
| Sharpe | (r̄_P − r̄_f)/σ_P |
| Jensen's α | r̄_P − [r̄_f + β_P(r̄_M − r̄_f)] |
| Information ratio | α_P / σ(e_P) |
| Treynor ▶ | (r̄_P − r̄_f)/β_P |
| Active Share | 0.5 Σ|w_j,i − w_b,i| |

---

## 7. Self-test

1. Factor portfolios: E(r_1) = 9%, E(r_2) = 7%. r_f = 3%. Well-diversified portfolio B has β_1 = 1.2, β_2 = 0.4. What should E(r_B) be?
2. B is expected to return 12%. What is its alpha? Write out the full arbitrage table.
3. Why does the same trade not work as a pure arbitrage if B is a single stock?
4. Give three differences between the APT and the CAPM.
5. A fund has r̄ = 12%, σ = 20%, β = 0.9, σ(e) = 6%. r_f = 2%, r̄_M = 10%. Compute its Sharpe, Jensen α and information ratio.
6. Which measure would you use for a fund that is your only investment? For one fund among many?
7. A portfolio holds 50 stocks equally, each with σ(e) = 30%. What is σ(e_P)?

<details>
<summary>Answers</summary>

1. 3% + 1.2(6%) + 0.4(4%) = 3 + 7.2 + 1.6 = **11.8%**.
2. α = 12% − 11.8% = **+0.2%** → B is **underpriced** → **buy** B.
   | Position | Weight | β₁ | β₂ | E(r) |
   |---|---|---|---|---|
   | B | +1 | +1.2 | +0.4 | +12% |
   | FP1 | −1.2 | −1.2 | 0 | −10.8% |
   | FP2 | −0.4 | 0 | −0.4 | −2.8% |
   | r_f | +0.6 | 0 | 0 | +1.8% |
   | **Total** | **0** | **0** | **0** | **+0.2%** |
   Risk-free weight = −(1 − 1.2 − 0.4) = +0.6 (you **lend**).
3. Long B leaves you exposed to e_B, B's firm-specific risk, so the position is not riskless.
4. APT holds for well-diversified portfolios (individual stocks can be mispriced); it doesn't need the market portfolio; it allows many factors; it rests on no-arbitrage instead of everyone holding M.
5. Sharpe = 10/20 = **0.50**. α = 12 − (2 + 0.9 × 8) = 12 − 9.2 = **2.8%**. IR = 2.8/6 = **0.467**.
6. Only investment → **Sharpe** (total risk). One of many → **Jensen's α** (or Treynor), since firm-specific risk diversifies away.
7. σ²(e_P) = Σ(1/50)²(0.09) = 50 × (1/2500)(0.09) = 0.0018 → σ(e_P) = **4.24%**.
</details>
