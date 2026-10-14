# FINA 3080 — Week 2 Notes
## Lecture 2: Two determinants of investment decisions — return and risk

*Investment Analysis and Portfolio Management · Instructor: Chao Ying (CUHK)*

> **How to read these notes:** everything in the main text comes from the slides. Parts marked **▶ Beyond the slides** are my own explanations and worked examples. They follow the optional textbook (BKM Ch. 1, 3, 5) but were not explicitly presented in lecture.

**Today's outline**
1. Financial markets and the economy
2. How securities are traded
3. Buying on margin
4. Short selling
5. Expected vs. realized return and risk

---

## 0. Announcements and market update (slides 2–5)

### Announcements
- If you haven't done the **Lecture 1 quiz** on Blackboard, finish it. The solution has been posted.
- Send questions to **both** the instructor (chaoying@cuhk.edu.hk) **and** the TA (yiweiliang@**link**.cuhk.edu.hk).

### HSI vs. S&P 500, week of Sep 7–11 (slides 3–4)
- The level correlation is still **0.54**.
- **Sep 7:** the US cash market was closed for Labor Day, so the chart carries forward the Sep 4 S&P 500 close.
- **Sep 7–10:** the Middle East conflict intensified and **oil rose above $100**. Both indexes drifted down.
- **Sep 11:** news of a possible Iran–Gulf deal on **shipping through the Strait of Hormuz** pushed oil down from about $110. Both indexes bounced.

**Takeaway:** a shared macro shock (oil and geopolitics) moves both markets *in the same direction*. Compare the July divergence from Lecture 1, which was a sector-specific shock to US chip stocks.

### HSI constituents, top 50 (slide 5)
This slide links back to the **value-weighted** HSI from Lecture 1. The weights are proportional to market cap, so a handful of giants dominate the index.

| Rank | Stock | Industry | Share type | Weight |
|---|---|---|---|---|
| 1 | HSBC Holdings (0005) | Financials | HK Ordinary | 8.78% |
| 2 | Tencent (0700) | IT | Other HK-listed Mainland Co. | 8.61% |
| 3 | AIA (1299) | Financials | HK Ordinary | 7.45% |
| 4 | Alibaba (9988) | IT | Other HK-listed Mainland Co. | 6.94% |
| 5 | Meituan (3690) | IT | Other HK-listed Mainland Co. | 4.86% |
| 6 | CCB (0939) | Financials | H Share | 4.67% |
| 7 | **China Mobile (0941)** *(underlined on the slide)* | Telecom | **Red Chip** | 3.71% |
| 8 | HKEX (0388) | Financials | HK Ordinary | 3.19% |

- The top 5 stocks make up about **36.6%** of the index, and the top 8 about **48%**.
- The index is dominated by **Financials** and **IT**.

> **▶ Beyond the slides: HK share types**
> - **HK Ordinary:** companies incorporated in Hong Kong or overseas, with mainly non-mainland business (e.g. HSBC, AIA, HKEX).
> - **H Share:** companies **incorporated in mainland China** and listed in Hong Kong (e.g. CCB, ICBC, Ping An).
> - **Red Chip:** companies incorporated **outside** the mainland but **controlled by mainland state-owned entities** (e.g. China Mobile, CNOOC).
> - **Other HK-listed Mainland Co.:** privately owned mainland businesses, usually incorporated offshore in places like the Cayman Islands (e.g. Tencent, Alibaba, Meituan, Xiaomi).

---

## 1. Financial markets and the economy (slides 6–12)

### Real assets vs. financial assets
| | **Real assets** | **Financial assets** |
|---|---|---|
| What they are | Assets used to **produce goods and services** | **Claims on real assets** (or on the income they generate) |
| Examples | Land, buildings, machines, **human capital (knowledge)** | Stocks, bonds, loans, derivatives |
| Productive? | Yes, they determine an economy's wealth | They **do not contribute directly** to productive capacity |

> **▶ Beyond the slides:** financial assets net out across the whole economy, because my asset (a bond) is your liability. What is left is real assets, so a society's wealth is its real assets. Financial assets decide **who owns** those real assets and the income they produce.

### How funds flow through the economy (slide 8)
- **Business sector:** has "ideas, no money". This is the **demand for money**.
- **Household sector:** has "money, no ideas". This is the **supply of money**.
- **Government:** sets fiscal policy and the rules.

There are two channels between them:
1. **Direct financing** (arranged through **investment banks**). Households give funds directly to businesses and receive claims such as stocks and bonds.
2. **Indirect financing** (through **intermediaries** such as banks, insurers and mutual funds). Households give funds to the intermediary and get a claim on the intermediary, such as a deposit, a policy or fund units. The intermediary then gives funds to businesses and receives claims on them.

### Primary vs. secondary markets (slide 9)
- **Primary market:** **new issues** of securities, such as IPOs and new bond issues. This is the financing process from slide 8, and the firm receives the money.
- **Secondary market:** **existing** securities are bought and sold between investors, for example on stock exchanges. The firm receives nothing directly.

### Four functions of financial markets (slides 10–11)
1. **Allocating capital.** Firms "grow now, pay later" by issuing stocks and bonds. Capital flows to the most promising ideas.
2. **Timing consumption.**
   - Save now and spend later, by investing.
   - Buy now and pay at a different time, by selling past investments or borrowing.
3. **Managing risk.** You can **manage** risk through diversification, **share** it through insurance, or **hedge** it with derivatives.
4. **Separating ownership from management.**
   - Owners don't need to run the firm. They can buy or sell stocks and bonds instead of hiring and firing managers.
   - Firm managers should pursue strategies that **enhance shareholder value**.

> **▶ Beyond the slides:** point 4 creates the **agency problem**: managers may pursue their own interests rather than shareholders'. Mechanisms that address it include the board of directors, pay linked to stock price, takeover threats, and shareholders simply selling, which pushes the price down.

### Classification tree of financial assets (slide 12)
```
Financial Assets
├── Marketable (tradable)
│   ├── Primitive securities — claims on real assets
│   │   ├── Debt: bills, notes, bonds
│   │   └── Equity: stocks
│   ├── Derivative securities — value depends on other assets
│   │   ├── Futures
│   │   └── Options
│   └── Securitized claims — package non-marketable assets into marketable portfolios
│        (e.g. mortgage-backed securities)
└── Non-marketable
    ├── Debt: loans, mortgages, insurance policies  ──► (can be securitized)
    └── Equity: net worth (personal wealth net of debt)
```

---

## 2. How securities are traded (slides 13–19)

### Four types of secondary markets (slide 14)
These are ordered from least to most organized:

| Type | How buyers and sellers meet | Example |
|---|---|---|
| **1. Direct search** | Buyers and sellers find each other themselves | Used **books**, garage sales |
| **2. Brokered search** | A **broker** matches buyers and sellers for a commission | **Real estate** (houses) |
| **3. Dealer markets** | A **dealer** holds an inventory and trades on their own account. You **buy at the ask** and **sell at the bid** | **Foreign exchange**, most bonds |
| **4. Auction markets** | All traders meet in one integrated, centralized place | **Stock exchanges** |

Market authorities (regulators) oversee all four.

### Bid vs. ask (slides 15–16)
- **Bid price:** the **highest** price a buyer will pay. This is the price you get when you **sell**.
- **Ask price:** the **lowest** price at which a seller will sell. This is the price you pay when you **buy**.
- **The ask is always higher than the bid.**
- **Bid–ask spread = ask − bid.** It is the dealer's (market maker's) compensation and a **transaction cost** for investors.
- **Example:** a dealer buys at $100.00 (bid) and sells at $100.05 (ask), so the spread of **$0.05 per share** is the dealer's profit.

### Exchange rates: airport vs. HSBC bank (slide 17)
Both quotes are in HKD. The airport quotes per 100 units, and HSBC quotes per 1 unit.

| Currency | Airport: they buy (your bid) | Airport: they sell (your ask) | HSBC bid | HSBC ask |
|---|---|---|---|---|
| USD | 7.3398 | 8.1931 | 7.8091 | 7.8852 |
| EUR | 8.2877 | 9.3025 | 8.8516 | 9.0389 |
| JPY | 0.0670 | 0.0750 | 0.07029 | 0.07177 |
| GBP | 9.8787 | 11.1459 | 10.1690 | 10.4420 |

**Is there an arbitrage opportunity?**

> **▶ Beyond the slides: worked answer**
> To make money from arbitrage you need **one dealer's bid to be higher than another dealer's ask**. Then you could buy from one and sell to the other at a profit.
> - USD: the airport bid (7.34) is below HSBC's ask (7.885), so you can't buy at HSBC and sell at the airport.
> - USD: HSBC's bid (7.809) is below the airport ask (8.193), so you can't buy at the airport and sell at HSBC.
> - The other currencies work the same way, so **there is no arbitrage**.
> - The **airport spread is much wider**: for USD it is about 11% of the price, versus about 1% at HSBC. Airport customers are a captive market with high search costs, so the dealer can charge more. The airport's bid–ask range *contains* the bank's range.

### Auction markets (slide 18)
- An auction market is **centralized**, so at any point in time you see only **one** set of bid and ask prices: the best bid and the best ask across all orders.
- **Example:** HSBC (0005.HK) on 15 Dec 2021 at 13:27 had **bid 45.050 and ask 45.100**, with a last price of 45.100. The spread was one tick (HK$0.05).
- Contrast this with a dealer market, where each dealer (the airport, each bank) posts its own bid and ask.

### Stock order types (slide 19)
Assume the current **bid is $49** and the **ask is $51**.

**1. Market orders: buy or sell immediately at the prevailing price.**
- A **market sell** executes at the **bid**, $49.
- A **market buy** executes at the **ask**, $51.

**2. Price-contingent orders: buy or sell only if a condition is met.**

| Order | Condition | Who uses it | Purpose |
|---|---|---|---|
| **Limit buy** at $47 | Executes only if the price **hits or falls below** $47 | Someone who doesn't hold the stock | Buy cheaply |
| **Stop-loss sell** at $47 | Executes when the price **falls to** $47 | Someone who already holds the stock | Limit losses on a long position |
| **Limit sell** at $53 | Executes only if the price **hits or rises above** $53 | Someone who already holds the stock | Sell at a good price |
| **Stop-loss buy** (stop-buy) at $53 | Executes when the price **rises to** $53 | Someone who doesn't hold the stock (usually a short seller) | Limit losses on a short position |

- On the slide's price line, a price of 48 or 52 means **no order executes**. A price of 46 means the buy-limit and stop-loss sell **execute**, and 54 means the sell-limit and stop-buy **execute**.
- **Memory rule:** limit and stop-loss **buy** orders are for people who **don't hold** the stock. Limit and stop-loss **sell** orders are for people who **already hold** it.

> **▶ Beyond the slides: limit orders vs. stop orders**
> - A **limit** order sets the *worst acceptable price*. It is triggered when the price moves in your **favor**.
> - A **stop** order is triggered when the price moves **against** you. It then becomes a market order, so in a fast-falling market it may fill well below the stop price.

---

## 3. Buying on margin (slides 20–27)

### Motivation: the Ant Group IPO, Nov 2020 (slide 21)
- The instructor applied for Ant Group shares at **HK$80 per share**. Because the IPO was heavily oversubscribed, he was allocated only **50 shares** ($4,000).
- His bank debit was **HK$808,061.60**. **How many shares did he apply for?**

> **▶ Beyond the slides: worked answer**
> A board lot of 50 shares × $80 = $4,000. Add the 1% brokerage fee, the 0.0027% SFC levy and the 0.005% trading fee, and one lot costs $4,000 × 1.010077 = **$4,040.31**.
> $808,061.60 ÷ $4,040.31 = **200 lots = 10,000 shares**. He received only 50 shares, or **0.5%** of what he applied for.

- **The question:** IPO shares are allocated **in proportion** to the application. How could he get more shares? In other words, how could he get **more money**?
- **Answer:** borrow. In practice, brokers offer **IPO margin financing**, which lets you apply for many times your own cash. This leads into **buying on margin**.
- (The Ant IPO was suspended at the last minute and all the money was refunded.)

### Definitions (slide 22)
- **What is it?** You **borrow funds** from a broker to buy a security.
- **Why?** To **leverage** a bet that the price will **rise**.
- **Margin** is the percentage funded by the investor; the rest is a loan from the broker.

$$\text{Margin} = \frac{\text{Account equity}}{\text{Account market value}} = \frac{\text{Market value} - \text{Loan}}{\text{Market value}}$$

- **Initial margin:** the investor funding required at the start.
- **Maintenance margin:** the minimum margin required after that.
- **Margin call:** issued when the margin falls below the maintenance margin. You must **add funds**, or the broker **sells the margined security**.

### Worked example: X Corp (slides 23–25)
**Setup:** price $70, N = 1,000 shares, initial margin 50%, maintenance margin M = 40%.

| Assets | | Liabilities and equity | |
|---|---|---|---|
| Stock | $70,000 | Loan | $35,000 |
| | | Equity | $35,000 |

**The price falls to $60:**
$$\text{Margin} = \frac{60{,}000 - 35{,}000}{60{,}000} = 41.67\% > 40\% \Rightarrow \textbf{no margin call}$$
The stock is now worth $60,000 and equity is $25,000. **The loan doesn't change, so the whole loss comes out of your equity.**

**At what price P is there a margin call?** Solve
$$\frac{NP - \text{Loan}}{NP} = M \;\;\Rightarrow\;\; \boxed{P = \frac{\text{Loan}}{N(1-M)}}$$
$$P = \frac{35{,}000}{1{,}000 \times (1 - 0.4)} = \$58.33$$
At $58.33 the stock is worth $58,333 and equity is $23,333, so margin is 40%. *(This ignores interest and dividends.)*

> **▶ Beyond the slides: how much cash does a margin call require?**
> Suppose the price falls to $50. Stock = $50,000 and equity = $15,000, so margin = 30% < 40%.
> To get back to 40% you need equity of 0.4 × 50,000 = $20,000, which means depositing **$5,000** of cash. The cash pays down the loan to $30,000, giving (50,000 − 30,000)/50,000 = 40% ✔.

### Leverage magnifies returns (slide 26)
| | No margin (100%) | 50% margin |
|---|---|---|
| Starting equity | $35,000 | $35,000 |
| Shares | 500 | 1,000 |
| Starting value (at $70) | $35,000 | $70,000 |
| Ending value (at $60) | $30,000 | $60,000 |
| Ending equity | $30,000 | $25,000 |
| **ROE** | **−5,000/35,000 = −14%** | **−10,000/35,000 = −29%** |

- With 50% margin, the ROE is **exactly twice** the stock's return, because leverage = 1/margin = 2.
- **Margin buying magnifies returns in both directions.**

> **▶ Beyond the slides: the general formula, including interest**
> $$\text{ROE} = \frac{r_{\text{stock}} \times \text{Value}_0 - \text{Interest}}{\text{Equity}_0} = r_{\text{stock}} \times \frac{1}{\text{margin}} - \frac{\text{Loan} \times r_{\text{loan}}}{\text{Equity}_0}$$
> Example: suppose the price rises 20% (from $70 to $84) and the loan rate is 9%. The unlevered ROE is +20%. The levered ROE is (14,000 − 3,150)/35,000 = **+31%**. If the price falls 20%, the levered ROE is (−14,000 − 3,150)/35,000 = **−49%**.

### Margin rules in the US and HK (slide 27)
- **US:** the initial margin is **50%** under **Regulation T** (Federal Reserve).
- **HK:** it **varies by broker and by stock**. For example, a broker may lend more against blue chips and nothing against small or volatile stocks. See the HSBC securities margin and POEMS margin-ratio pages.

---

## 4. Short selling (slides 28–34)

### Definitions (slide 29)
- **What is it?** You **borrow a security** from a broker and then **sell** it.
- **Why?** To bet that the price will **fall**.
- **The logic is to sell now at a high price and buy later at a low price.** This reverses the usual "long" logic of buying now and selling later.
- **Covering a short position** means buying the shorted security back to return it to the lender.
- **Rules:**
  - You must post **collateral**, usually liquid assets such as T-bills.
  - The **proceeds** of the short sale must stay **in the account**; you cannot spend them.
  - There is a **margin requirement**, and you are subject to margin calls.

### Worked example: stock Y (slides 30–32)
**Setup:** price $100, N = 1,000 shares shorted, initial margin 50% (equity ÷ short value), maintenance margin M = 30%.

**Initial position**
| Assets | | Liabilities and equity | |
|---|---|---|---|
| Cash (proceeds of the short sale) | $100,000 | Short position (stock owed) | $100,000 |
| T-bills (collateral) | $50,000 | **Equity (your own capital)** | $50,000 |

**The price falls to $70 and you cover:**
- You buy back 1,000 shares at $70 = $70,000.
- **Profit = $100,000 − $70,000 = $30,000.**
- Ending position: assets $150,000, short liability $70,000, **equity $80,000**.

**At what price P is there a margin call?** Solve
$$\frac{\text{Assets} - NP}{NP} = M \;\;\Rightarrow\;\; \boxed{P = \frac{\text{Assets}}{N(1+M)}}$$
$$P = \frac{150{,}000}{1{,}000 \times 1.3} = \$115.38$$
At $115.38 the short position is worth $115,385 and equity is $34,615, so margin is 30%. *(This ignores interest and dividends.)*

> **▶ Beyond the slides**
> - **Return on equity** in the $70 case is 30,000 / 50,000 = **+60%**, because the stock fell by 30%.
> - **The loss is unlimited.** A stock can fall at most to $0, which caps a short seller's gain at $100,000. But it can rise without limit, so losses have no ceiling. That's why short positions face margin calls when the price **rises**.
> - **Dividends:** a short seller must pay the lender any dividends paid while the position is open.
> - **Comparing the two margin-call formulas:** for a long position, P = Loan / [N(1 − M)], and the call is triggered when the price **falls**. For a short position, P = Assets / [N(1 + M)], and the call is triggered when the price **rises**.

### Who are the short sellers? (slide 33)
- To make money from shorting, you need **negative information** about the company.
- In recent years, arbitrageurs have launched **"short-sale campaigns"** in which they *make* the bad news public. They first take a short position, then publish a research report.
- **Example: Muddy Waters vs. China MediaExpress (CCME), 2011.** Muddy Waters published "irrefutable evidence that CCME is a substantial fraud". CCME was **delisted in May 2011**.

### Buying on margin vs. short selling (slide 34)
| | **Buying on margin** | **Short selling** |
|---|---|---|
| What you borrow | **Money** | **Stocks** |
| Your bet | The price will rise | The price will fall |
| Returns | Magnified returns | Opposite to a long position |
| How your equity is used | Funds M% of the purchase; you borrow the other (1 − M) | Serves as collateral; the lender keeps it in the account |
| Margin-call risk | The stock price **falls** a lot | The stock price **rises** a lot |

---

## 5. Expected vs. realized return and risk (slides 35–41)

### Motivation: badminton (slides 37–38)
- **Korea Open 2024, men's singles quarter-final:** **Shi Yu Qi** (China, BWF world #1, seeded 1st, leading the head-to-head 6–4) against **Lee Cheuk Yiu** (Hong Kong, BWF #15).
- **What we expected:** Shi was the clear favourite.
- **What happened:** **Lee won 2–0 (21–13, 21–15).**
- **Lesson:** the **expected** outcome, based on the distribution of likely outcomes, differs from the **realized** outcome, which is a single draw from that distribution. One upset doesn't mean the expectation was wrong. Investment returns work the same way.

### Holding-period return (HPR) (slide 39)
$$r_t = \frac{P_t - P_{t-1} + Div_t}{P_{t-1}}$$
The return has two parts: the **capital gain** (Pₜ − Pₜ₋₁) and the **dividend yield** (Divₜ). Both are divided by the **starting** price.

**Example:** P₀ = 50, P₁ = 53, P₂ = 54, D₁ = D₂ = 2.
$$r_1 = \frac{53 - 50 + 2}{50} = 10\%, \qquad r_2 = \frac{54 - 53 + 2}{53} = 5.66\%$$

### Arithmetic average return (slide 40)
$$r_A = \sum_{t=1}^{n}\frac{r_t}{n} = \frac{r_1 + r_2 + \dots + r_n}{n} = \frac{10\% + 5.66\%}{2} = 7.83\%$$
- This is a **backward-looking** return, because it uses historical price data.
- **What about future returns?** That question leads to expected returns.

> **▶ Beyond the slides: the geometric average return** (coming in later lectures)
> $$r_G = \left[(1+r_1)(1+r_2)\cdots(1+r_n)\right]^{1/n} - 1 = \sqrt{1.10 \times 1.0566} - 1 = 7.81\%$$
> - The geometric average is the constant per-period return that gives the same final wealth.
> - It is always **less than or equal to** the arithmetic average. The gap grows with volatility: for example, +50% followed by −50% gives an arithmetic average of 0% but a geometric average of −13.4%.
> - **Sample variance** of realized returns: s² = Σ(rₜ − r̄)² / (n − 1).

### Expected vs. realized returns (slide 41)
| | **Expected return μ and expected risk σ²** | **Realized return R(r) and realized risk s²** |
|---|---|---|
| Direction | **Forward**-looking | **Backward**-looking |
| Meaning | What *should* happen on average | What *did* happen on average |
| Requires | Knowledge of the **distribution** of returns | Analysis of **sample** returns to learn the distribution |
| Type | **Population parameters** | **Sample statistics** |

- **How they connect:** past returns give sample statistics R(r) and s². In the present we analyse these to **estimate** the distribution's parameters μ and σ² for future returns. Realized returns are usually used to **extrapolate** expected returns and risk.

> **▶ Beyond the slides: expected return from scenarios**
> $$E[r] = \sum_s p(s)\, r(s), \qquad \sigma^2 = \sum_s p(s)\,[r(s) - E[r]]^2$$
> Example: a boom (p = 0.3) gives +30%, a normal year (p = 0.5) gives +10%, and a recession (p = 0.2) gives −20%.
> E[r] = 0.09 + 0.05 − 0.04 = **10%**
> σ² = 0.3(0.20)² + 0.5(0)² + 0.2(−0.30)² = 0.012 + 0.018 = 0.030, so **σ = 17.3%**.

---

## 6. Formula sheet

| Concept | Formula |
|---|---|
| Margin (long position) | (MV − Loan) / MV |
| Margin-call price (long) | P = Loan / [N(1 − M)] |
| Margin (short position) | (Assets − N·P) / (N·P) |
| Margin-call price (short) | P = Assets / [N(1 + M)] |
| Levered ROE (no interest) | r_stock / margin |
| Holding-period return | (Pₜ − Pₜ₋₁ + Divₜ) / Pₜ₋₁ |
| Arithmetic average | Σrₜ / n |
| Bid–ask spread | Ask − Bid (you buy at the ask, sell at the bid) |

---

## 7. Self-test

1. Is a share of HSBC a real asset or a financial asset? What about HSBC's headquarters building?
2. Name the four functions of financial markets.
3. A firm's IPO happens in the ___ market. Trading of that firm's shares on HKEX the next day happens in the ___ market.
4. A dealer quotes bid 7.80 and ask 7.90. What do you pay to buy, and what do you get when you sell? What is the spread?
5. A stock trades at bid $49 and ask $51. You hold the stock and want protection if it falls below $45. Which order do you use?
6. You buy 500 shares at $40 with 60% initial margin and a 35% maintenance margin. (a) What is the loan? (b) At what price do you receive a margin call?
7. In Q6, the price rises to $48. What is your ROE, ignoring interest?
8. You short 2,000 shares at $50 with 50% initial margin and 25% maintenance margin. At what price do you receive a margin call?
9. Why is the potential loss on a short sale unlimited?
10. P₀ = 20, P₁ = 22, D₁ = 1, P₂ = 21, D₂ = 1. Compute r₁, r₂ and the arithmetic average.
11. What is the difference between μ and the sample mean of past returns?

<details>
<summary>Answers</summary>

1. The share is a financial asset, because it is a claim. The building is a real asset.
2. Allocating capital, timing consumption, managing risk, and separating ownership from management.
3. Primary; secondary.
4. You pay 7.90 (the ask) to buy and get 7.80 (the bid) when you sell. The spread is 0.10.
5. A **stop-loss sell** order at $45.
6. (a) Value = $20,000. Equity = 60% × $20,000 = $12,000, so the **loan is $8,000**. (b) P = 8,000 / [500 × (1 − 0.35)] = **$24.62**.
7. The gain is 500 × $8 = $4,000. ROE = 4,000 / 12,000 = **33.3%**, which is the stock's 20% return ÷ 0.6.
8. Assets = $100,000 in proceeds + $50,000 of collateral = $150,000. P = 150,000 / (2,000 × 1.25) = **$60**.
9. The price can rise without any limit, and you must buy the shares back at whatever the price is.
10. r₁ = (22 − 20 + 1)/20 = **15%**. r₂ = (21 − 22 + 1)/22 = **0%**. The arithmetic average is **7.5%**.
11. μ is the forward-looking **population** parameter of the return distribution. The sample mean is a backward-looking **estimate** of μ computed from realized returns.
</details>
