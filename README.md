# Money Basics & Scam Shield

Free Claude skill (SKILL.md) that teaches money basics in plain words and checks money offers for scam signs. Built for students, beginners and young professionals, especially in Azerbaijan, Central Asia and Africa. Answers in the user's language, phone-short.

**Educational only. Not financial advice.** It never picks stocks, coins, brokers or lenders, and never asks for bank logins, card or ID numbers.

## What it does
- **Explain:** interest, APR, credit cards, loans, microloans, BNPL, overdraft, credit history, inflation, emergency fund, saving vs investing vs gambling.
- **True cost:** monthly payment, total paid and interest for a loan or card, with the formula shown; credit-card minimum-payment trap; per-day microloan rates.
- **Offer check:** Ponzi, pyramids, forex/crypto "signals", copy-trading, fake trading platforms, crypto doubling, romance-investment, loan apps, money-mule "jobs", recovery scams → verdict (`Likely scam` / `Suspicious` / `No scam signals found`), quoted red flags, impossible-return maths, licence check on the official regulator register, report route.
- **Already paid / shared:** ordered recovery steps and a recovery-scam warning.

## Where it stops
- No personal investment, tax or legal advice. Tax and legal figures only from official pages opened in the session, with a date, or marked "verify".
- Licence checks and official figures need web access; without it the best verdict is `Suspicious` and links are marked "not opened".
- Doesn't contact, pay, invest or report for you. Never accuses named people.

## Files
- `SKILL.md` — the skill.
- `references/` — scam patterns, interest maths, money basics, official registers by country.
- `evals/evals.json` — 7 test cases. `tests/` — blind eval results.
- `scripts/build-agensi-zip.ps1` — builds `dist/money-basics-scam-shield.zip` (SKILL.md + references + CHANGELOG only).
- `LISTING.md` — Agensi listing texts.

## Install
Copy the folder into your skills directory (e.g. `~/.claude/skills/money-basics-scam-shield/`), or upload the ZIP in Claude → Settings → Capabilities → Skills.

## Related (optional)
- Scholarship & Visa Scam Checker (free) — study-abroad scams.
- Student Budget Planner (free) — monthly plan for stipend, rent and currency.

## License
MIT © 2026 Codelady Abroad
