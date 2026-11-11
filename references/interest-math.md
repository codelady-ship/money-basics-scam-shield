# Interest maths (show the user the steps)

Always ask whether a rate is **per year** or **per month** (or per day). Microloans often quote per day; cards per year.

## Symbols
- L = amount borrowed · n = number of monthly payments
- Yearly nominal rate (APR) → monthly rate r = APR / 12 (as a decimal: 24% → 0.02)

## 1. Equal monthly payment (annuity loan)
P = L × r / (1 − (1 + r)^−n)
Total paid = P × n · Interest = P × n − L

**Example:** 2,000 at 24% a year for 12 months. r = 0.02.
P = 2000 × 0.02 / (1 − 1.02^−12) ≈ **189.12** a month. Total ≈ 2,269.43. Interest ≈ **269.43**.
If r = 0: P = L / n.

## 2. Fees and add-ons
Upfront fee or "insurance" you pay also counts as cost. Total cost = interest + all fees. If a fee is taken from the loan (you receive less), the real rate is higher than the stated one: you pay interest on money you never got. Say this in one line; don't compute an "effective APR" unless you can run code — then mark it ≈.

## 3. Credit card: the minimum-payment trap
Each month: balance × (1 + r), then subtract the payment. Simulate month by month (with code if possible).
**Example:** 1,000 at 30% a year (r = 0.025), no new spending.
- Paying the minimum (5% of balance, at least 20): ≈ **63 months**, total ≈ 1,732, interest ≈ **732**.
- Paying a fixed 100 a month: ≈ **12 months**, total ≈ 1,165, interest ≈ **165**.
Minimum-payment rules differ by bank: use the user's card terms; if unknown, say "example assumption".
Grace period: if the full statement balance is paid by the due date, purchases often have no interest — check the card's own terms. Cash withdrawals usually have a fee and interest from day one (check terms).

## 4. Per-day rates (microloans, "daily profit")
Simple daily interest: L × d × days. Example: 500 at 1% a day for 30 days → 500 × 0.01 × 30 = **150** interest. As a yearly rate: 1% × 365 = **365% a year** (simple).

## 5. Compound growth (savings or impossible promises)
Future value = amount × (1 + rate per period)^periods.
3% a day for 30 days: 1.03^30 ≈ 2.43. 10% a month for 12 months: 1.1^12 ≈ 3.14.

## 6. Inflation and real return
Real return ≈ (1 + nominal) / (1 + inflation) − 1.
Example: savings 5% a year, inflation 8% → 1.05 / 1.08 − 1 ≈ **−2.8%**: money buys less after a year.
Use the official inflation figure (statistics office or central bank) **opened now** with "as of"; otherwise use the user's number or write "verify".

## 7. Foreign-currency loans
If income is in AZN (or som, tenge, naira…) and the loan is in USD/EUR, a currency fall raises every payment in local money. Example: 100 USD payment; if the rate moves from 1.70 to 2.00, the payment goes from 170 to 200 in local money (+17.6%). Rates only from the central bank page opened now, or the user's numbers.

## Rounding
Round money to 2 decimals and mark with ≈ when computed by hand. If a result looks odd, recheck rate units (year vs month vs day) first.
