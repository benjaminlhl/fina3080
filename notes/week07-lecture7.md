# FINA 3080 — Week 7 Notes
## Lecture 7: Investment funds, luck vs. skill, and the Efficient Market Hypothesis

*Investment Analysis and Portfolio Management · Instructor: Chao Ying (CUHK)*

> **How to read these notes:** everything in the main text comes from the slides. Parts marked **▶ Beyond the slides** are my own explanations and worked examples (BKM Ch. 4, 11, 24, 26).
>
> ⭐ **Not on the midterm → high priority for the final.** The title also mentions **behavioral finance**, but these slides end at the three forms of market efficiency. Behavioral finance is probably next lecture.

**Today's outline**
1. Financial intermediaries: types of funds
2. Mutual funds (and ETFs)
3. Hedge funds
4. Luck or skill? (the t-statistic of alpha)
5. Randomness and market efficiency
6. Forms of market efficiency

---

## 0. Market update (slides 2–3)
- **Oct 30:** Big Tech earnings disappoint → **US stocks fall sharply**, but **HK financial and property stocks rally → HSI rises**. (Again, HK and US don't always move together.)

---

## 1. Types of funds (slides 5–9)

A **fund** collects money from individuals and invests it in a wide range of securities.

### 1. Managed investment companies
**(i) Open-end funds = mutual funds** (e.g., the Tracker Fund)
- **Shares outstanding change**: new shares are created when investors buy and **redeemed** when they sell. They trade **daily**.
- Priced at **Net Asset Value (NAV)**:
$$\text{NAV} = \frac{\text{Market value of assets} - \text{Liabilities}}{\text{Shares outstanding}}$$

**(ii) Closed-end funds**
- **Shares outstanding don't change.** To exit you must **sell to another investor** on the market.
- So the price can be at a **premium or discount to NAV**.

### 2. Exchange-Traded Funds (ETFs)
- Similar to mutual funds; **many track indexes**.
- **Traded on stock exchanges like stocks**, throughout the day.

### 3. Hedge funds
- Like mutual funds but structured as **private partnerships** with **less regulation**.
- **Open only to wealthy or institutional investors.**

> **▶ Beyond the slides: NAV example.** A fund holds $250m of assets, has $10m of liabilities and 12m shares → NAV = 240/12 = **$20**. If a closed-end fund with this NAV trades at $18, it is at a **10% discount**: (18 − 20)/20 = −10%.

### Who owns US stocks? (slides 7–9)
- **Chart (to 2011):** households 35%, mutual funds 20%, international investors 13%, pension funds 9%, government retirement funds 8%, ETFs 4%, hedge funds 3%, other 8%. Pension and government retirement funds (17% combined) are **"large but passive."**
- **2019 (Federal Reserve):** households **37.7%**, mutual funds **21.8%**, foreign **15.1%**, ETFs **6.4%**, state/local government pensions 5.5%, private pensions 5.4%, non-financial corporations 4.2%, life insurance 1.2%, federal government pensions 0.7%, other 1.7%.
- **FT (2021):** **retail trading** now accounts for almost as much **volume** as mutual funds and hedge funds combined (over 20% of US equity volume by 2021). **High-frequency market makers** are the biggest share at about 40–50%.

---

## 2. Mutual funds and ETFs (slides 11–25)

### Size (slides 11–13)
- **Worldwide (2020):** **126,457** open-end funds with **US$63.1 trillion** of net assets: **45% equity**, 21% bond, 21% mixed/other. Almost **half** of global mutual fund assets are in the US.
- **US (2020):** 7,636 funds managing **US$23.9 trillion**; **45.7%** of households own mutual funds; families keep on average **23%** of financial assets in investment companies.
- **Hong Kong (2021):** **2,135** funds managing **US$1.68 trillion** (44% equity, 36% bond).
- **MPF (2021):** HK$1,167 billion (US$150 billion), covering **2.7 million** employees.

### ETFs (slides 14–16)
- **Growing fast**, catching up with mutual funds. Can be active or passive.
- **Key difference:** ETFs trade **like stocks** (any time during the day), while **mutual funds can only be bought or sold once a day at the close** (at NAV).
- **HK ETFs (2021):** total net assets **HK$429 billion** (US$55 billion).
- **Tracker Fund of Hong Kong (2800.HK, TraHK):**
  - Launched in **1999** after the **Asian Financial Crisis**; it **tracks the Hang Seng Index**.
  - Managed by **Hang Seng Investment Management** (previously State Street Global Advisors Asia).
  - Net assets about **HK$135 billion**.

### Fund styles (slides 17, 25)
- **Passive:** closely tracks an index.
- **Active:** has a **benchmark** index and tries to **beat** it.
- **Morningstar style box (9 styles):** market cap (**small / medium / large**) × stock type (**value / blend / growth**).

### Performance measures, Active Share, fees (slides 18–24)
Same as Lecture 6: **Sharpe, Jensen's α, information ratio**, Active Share, the HK fund example (Corr(Active Share, α) = 0.69), fees (expense ratio and 12b-1 annually; front-end load on purchase; back-end load on redemption), **performance doesn't persist**, and active expense ratios (~0.8–1.1%) are far above passive ones (~0.1–0.27%). See `week06-lecture6.md` Sections 4–5.

---

## 3. Hedge funds (slides 27, 33–34)

- **Smaller than mutual funds, but more skillful.**
- They **short sell and buy on margin**. Leverage is about **1.7–1.8** (SEC reports).
- **Strategies:** long/short equity, **market neutral**, **convertible arbitrage**, **merger arbitrage**, distressed investing, emerging markets, event-driven, fixed-income arbitrage, **global macro**.

### Fees: "2 and 20" (slide 33)
- **2%** of total asset value as a **management fee**, plus **20% of any profits** earned (the incentive or performance fee).
- **Do they beat the market, and does good performance persist?** The evidence is doubtful.

> **▶ Beyond the slides: "2 and 20" in numbers.** A $100m fund earns a 15% gross return ($15m).
> - Management fee: 2% × $100m = **$2m**.
> - Incentive fee: 20% × $15m = **$3m** (using profits before fees, as the slide words it).
> - Investors get $15m − $5m = $10m → **10% net**, versus 15% gross. Fees took a third of the profit.
> - (Some funds charge the 20% on profits **after** the management fee: 20% × $13m = $2.6m → 10.4% net. Follow whatever convention the exam question states.)

### Warren Buffett's bet (slide 34)
- In **2007**, Buffett bet **$1 million** that an **S&P 500 index fund** would beat a collection of hedge funds over **10 years**.
- **Result:** the index fund returned **7.1%** a year compounded; the basket of hedge funds chosen by **Protégé Partners** returned only **2.2%**.
- **Lesson:** fees + difficulty of beating the market → **passive wins**.

---

## 4. Luck or skill? How long must we watch a manager? (slides 28–32)

**Setup (slide 30):** regress a manager's monthly excess returns on the market's: **α = 0.2% per month**, **σ(e) = 2% per month**. How many months until we are **95% sure** that α > 0?

**Standard error of alpha (slide 31):**
$$\sigma(\alpha) \approx \frac{\sigma(e)}{\sqrt{N}}$$
**t-statistic:**
$$t(\alpha) = \frac{\alpha}{\sigma(\alpha)} = \frac{\alpha\sqrt{N}}{\sigma(e)}$$

**Solve (slide 32):** for 95% confidence, t ≥ **1.96**:
$$1.96 = \frac{0.2\sqrt{N}}{2} \;\Rightarrow\; \sqrt{N} = 19.6 \;\Rightarrow\; N = 384 \text{ months} = \mathbf{32\ years!}$$

**Shortcut:** $N = \left(\dfrac{1.96\,\sigma(e)}{\alpha}\right)^2$ — make sure α and σ(e) are in the **same units** (both monthly).

- This is **conservative**: it assumes α and σ(e) stay **constant**. If they change over time you need **even more data** and more sophisticated methods.
- **Lesson:** even a genuinely skilled manager can't be distinguished from a lucky one within a normal career. Most track records are far too short.

> **▶ Beyond the slides: link to the information ratio.** α/σ(e) is the (monthly) **information ratio**, so t = IR × √N. A manager with a higher IR is identified faster: N = (1.96/IR)².
> Example: α = 0.5%/month, σ(e) = 3% → N = (1.96 × 3/0.5)² = 11.76² ≈ **139 months (≈ 11.5 years)**. With only 60 months of data, t = 0.5√60/3 = **1.29 < 1.96** → can't reject luck.

---

## 5. Randomness and market efficiency (slides 36–39)

### Why should prices be random? (slides 36–37)
- Suppose the "true" value of a stock is **$110** but it trades at **$100**. How? The true value **isn't yet known by the market**.
- Once the information is revealed, "arbitrage" ensures the price **quickly moves to the true value**: buyers rush in, owners refuse to sell below $110, so the price **jumps** to $110.
- Therefore **stock prices only change when new information arrives**.
- New information is **unpredictable (random)** by definition → **price changes are also unpredictable (random)**.
- So, apart from a fair risk-adjusted return, **prices follow a random walk**.
- **This is the Efficient Markets Hypothesis (EMH).**

▶ Common confusion: a random walk does **not** mean prices are irrational. It means they **already** reflect all known information, so only *news* moves them.

### Responses to news (slide 38)
- **Timely** price responses to news imply efficient markets.
- In an efficient market the price **jumps immediately** at the announcement (up for good news, down for bad news) and then **stays flat**: no drift before (no leakage) and no drift after (no slow reaction).
- ▶ A **gradual drift after** the news = **under-reaction**; a jump followed by a **reversal** = **over-reaction**. Both are signs of **inefficiency** (and they're what behavioral finance tries to explain).

### Evidence: the pre-FOMC drift (slide 39)
- Average cumulative return on the S&P 500 over three-day windows around **scheduled FOMC announcements** (Sept 1994 – March 2011), vs. all other three-day windows.
- Around FOMC days the S&P rises about **0.5%**, much of it **before** the 2:15 pm statement. Non-FOMC windows average roughly **0**.
- ▶ This is the "pre-FOMC announcement drift" (Lucca & Moench, 2015): a predictable pattern that is hard to square with the EMH.

---

## 6. Forms of market efficiency (slides 41–44)

**Market efficiency is a matter of degree.** It depends on **what we count as information**. Three increasing levels:

| Form | Prices reflect… | Examples of info already in the price | So this doesn't earn abnormal returns ▶ |
|---|---|---|---|
| **Weak** | All **historical** information | Past prices, trading volume | **Technical analysis** (charts, momentum rules) |
| **Semi-strong** | All **publicly available** information (historical **plus** public) | Firm fundamentals, management, earnings, news | **Fundamental analysis** of public data |
| **Strong** | All **public and private** information (historical + public + **insider**) | Upcoming mergers and acquisitions | Even **insider** information |

**Reasoning in each case:** if the information were ever useful, investors (or for strong form, insiders and their allies) would already have traded on it, **impounding it into prices** and removing further profit opportunities.

**They are nested:** strong ⇒ semi-strong ⇒ weak. If the market is semi-strong efficient, it is also weak-form efficient. ▶ The reverse is not true.

> **▶ Beyond the slides: how each form is tested**
> - **Weak:** do past returns predict future returns? (serial correlation, momentum, filter rules)
> - **Semi-strong:** **event studies**: does the price react fully and immediately to public announcements (earnings, M&A, dividends)? Post-earnings-announcement drift is a famous violation.
> - **Strong:** do **insiders** earn abnormal returns? (They usually do → strong form generally **fails**; that's why insider trading is illegal.)
> - **Most evidence:** markets are roughly weak-form and largely semi-strong efficient, **not** strong-form efficient.

---

## 7. Formula sheet

| Concept | Formula |
|---|---|
| NAV | (Market value of assets − Liabilities) / Shares outstanding |
| Premium / discount | (Price − NAV) / NAV |
| Hedge fund fees | 2% × assets + 20% × profits |
| Standard error of α | σ(α) = σ(e)/√N |
| t-statistic of α | t = α√N / σ(e) |
| Months needed | N = (1.96 σ(e)/α)² |

---

## 8. Self-test

1. What is the difference between an open-end fund and a closed-end fund? Which can trade at a discount to NAV, and why?
2. Give two differences between an ETF and a mutual fund.
3. What are the three key features of hedge funds? Explain "2 and 20".
4. A manager has α = 0.3% per month and σ(e) = 2.5% per month. How many years of data do you need to be 95% confident the alpha is real?
5. With 10 years of data, what is the t-statistic for the manager in Q4? Is the alpha significant?
6. Why does the EMH predict that price changes follow a random walk?
7. Classify each as weak, semi-strong or strong form: (a) "Trading on a head-and-shoulders chart pattern can't beat the market." (b) "A CEO buying shares before announcing a takeover can't earn abnormal returns." (c) "Buying stocks after a good earnings announcement can't beat the market."
8. If the market is semi-strong efficient, must it also be weak-form efficient?
9. Draw the price reaction to good news in an efficient market and in one that under-reacts.
10. What was Buffett's bet and its outcome?

<details>
<summary>Answers</summary>

1. Open-end: shares are created/redeemed at NAV, so the price always equals NAV. Closed-end: fixed shares, traded between investors, so the price is set by supply and demand and can be a premium or **discount** to NAV.
2. ETFs trade on an exchange throughout the day like stocks (mutual funds only once a day at the closing NAV); ETFs are mostly index trackers; ETFs generally have lower fees ▶.
3. Private partnerships with less regulation; open only to wealthy/institutional investors; use short selling and leverage. "2 and 20" = 2% of assets per year plus 20% of profits.
4. N = (1.96 × 2.5/0.3)² = (16.33)² ≈ **267 months ≈ 22 years**.
5. t = 0.3 × √120 / 2.5 = 0.3 × 10.95 / 2.5 = **1.31 < 1.96** → not significant at 95%.
6. Prices change only when new information arrives, and new information is unpredictable by definition, so price changes are unpredictable.
7. (a) **Weak** (past prices). (b) **Strong** (private info). (c) **Semi-strong** (public info).
8. **Yes.** Public information includes historical prices and volume.
9. Efficient: a single jump at the announcement, flat before and after. Under-reaction: a smaller initial jump followed by a gradual upward drift.
10. In 2007, $1m that an S&P 500 index fund would beat a basket of hedge funds over 10 years. The index fund returned 7.1% a year vs. 2.2% for the hedge funds; Buffett won.
</details>
