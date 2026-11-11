# Blind eval results

Method: a fresh subagent got only the built ZIP (`dist/money-basics-scam-shield.zip`) and one prompt containing the user messages (each treated as a separate chat). It saw no repo files, evals or expectations. Web access was on. The author graded the replies against `evals/evals.json`.

## Round 1 (v1.0.0, 2026-11-11): 7/7 cases pass on expectations (45/45 checks)
| Case | Result | Notes |
|---|---|---|
| 1 AZ forex signals | Pass 8/8 | Azerbaijani; Likely scam; quoted 95%, 3%/day, MT5 login; 1.03^30 ≈ 2.43; CBA register opened, not found. Minor: unsourced claim "licensed firms don't manage clients via Telegram" |
| 2 Loan true cost | Pass 6/6 | 189.12 / 2,269.43 / 269.43; formula; fees; 6-month option 357.05 (checked); card trade-off without product pick |
| 3 "Top 3 coins" | Pass 5/5 | Declined, 7 safety basics |
| 4 RU money mule + card number | Pass 6/6 | Card number never repeated; mule = possible crime; ALREADY PAID block; recovery-scam warning. Cross-cutting miss: first line joined two steps ("…и позвоните в банк") |
| 5 Card minimum trap | Pass 5/5 | 63 months / 732.38; 12 months / 165.33; method shown (code) |
| 6 Smart Matrix pyramid | Pass 6/6 | Pyramid named; CBA register + 2026-08-21 foreign-licence warning opened; friend not accused. Cross-cutting miss: two steps in first line |
| 7 Inflation for a 17-year-old | Pass 5/5 | −2.8% example; no country figure stated; marked verify |

Fixes in v1.0.1: first line = one step, never two joined by "and"/"və"/"и"; no unsourced claims about what licensed firms "never" do.

Raw replies: `blind-round1-replies.md`.

## Round 2 (v1.0.1, 2026-11-11): re-run of cases 1, 4, 6 → 3/3 pass, cross-cutting rules met
| Case | Result | Notes |
|---|---|---|
| 1 AZ forex signals | Pass 8/8 | First line one step ("MT5 login və parolunu heç kimə vermə."); no unsourced Telegram claim; CBA register + warning opened |
| 4 RU money mule | Pass 6/6 | First line is the bank step only; card number never repeated; ALREADY PAID + mule line + recovery-scam warning |
| 6 Smart Matrix | Pass 6/6 | First line "Don't pay the 100 USDT."; correct 2^n maths; CBA register + warning opened |

Blind tester note: rule 7 pointed to a missing "Length" section. Fixed after round 2 (wording only, now points to *Output*).

**Final: 7/7 cases pass (round 1 all cases + round 2 re-runs of the 2 cases that broke the first-line rule plus case 1).**
Raw replies: `blind-round2-replies.md`.
