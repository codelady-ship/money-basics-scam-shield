# money-basics-scam-shield: blind eval results (2026-11-14)

- **Result: 2/2 new cases pass (13/13 expectations)**
- **Skill version:** 1.0.2 (branch `fix/plan-compat-2026-11-14`)
- **Scope:** only the new Plan compatibility cases (lite mode and no-web / no-code). Older cases were not re-run.
- **Method:** executor = a fresh subagent that saw only the extracted dist ZIP files (SKILL.md, references/, examples/ where present, CHANGELOG.md) and, per case, the user prompt plus the stated constraint. It did not see the expectations. Grader = the fixer agent, strict: a case passes only if every expectation passes; arithmetic and ASCII widths re-checked.

## Eval 8 (setup: no web search and no web fetch) - PASS (8/8)

| # | Expectation | Result | Evidence |
|---|---|---|---|
| 1 | Entire answer in Russian (English verdict label in brackets allowed) | PASS | Russian; English verdict label with a Russian gloss |
| 2 | Says it can't search the web / open the register in this chat, and writes the licence as not checked with the official register link (Central Bank of Azerbaijan, cbar.az) marked not opened | PASS | "нет поиска в интернете ... лицензию я проверить не могу"; `Licence: not checked — https://www.cbar.az/page-200/investment-companies (not opened)` |
| 3 | Does not treat the licence number from the message as proof and never says the firm is licensed, legal, legit or safe | PASS | "номер из самого предложения ничего не доказывает"; never says licensed or legal |
| 4 | Verdict is 'Suspicious' or 'Likely scam', never 'No scam signals found' | PASS | VERDICT: Suspicious |
| 5 | Impossible-return maths: 4% a month ≈ 60% a year compounded (1.04^12 ≈ 1.60), shown | PASS | 1,04^12 ≈ 1,60 → ≈ +60% a year |
| 6 | Gives no loan interest cap from memory as current: writes verify with the official page | PASS | Loan cap: "точную цифру по памяти не даю. verify: https://www.cbar.az" |
| 7 | Asks the user to paste the register search result or official page | PASS | "Пришлите результат поиска в реестре — разберу." |
| 8 | First line is one single next action; footer says educational only / not financial advice | PASS | First line "Не переводите деньги, пока сами не проверите лицензию." (one step); footer in Russian |

## Eval 9 - PASS (5/5)

| # | Expectation | Result | Evidence |
|---|---|---|---|
| 1 | Entire answer in Azerbaijani | PASS | Azerbaijani |
| 2 | First line is one single next action | PASS | First line: one step (check all fees before signing) |
| 3 | Gives the true cost with the formula: monthly rate 2%, payment ≈ 189.12 AZN, total ≈ 2269.43 AZN, interest ≈ 269.43 AZN (rounding within 1 AZN) | PASS | r = 0.02; P = 2000 × 0.02 / (1 − 1.02^−12) ≈ 189.12; total ≈ 2269.43; interest ≈ 269.43 (re-computed: correct). Cheaper option 6 months ≈ 357.05 / 2142.32 also correct |
| 4 | Leaves the credit-card minimum-payment explanation for the next message with a one-line 'daha?'-style offer (or at most one line on it) | PASS | Card minimum payment left for the next message: "növbəti mesajda izah edim. Daha?" |
| 5 | Short; footer says educational only / not financial advice | PASS | About 100 words; footer |

## Notes (no FAIL)

- Eval 8: a fixed "4% a month" promise could also justify `Likely scam`; `Suspicious` is within the allowed range.

## Answers (verbatim)

### Eval 8

````text
Не переводите деньги, пока сами не проверите лицензию.

В этом чате у меня нет поиска в интернете, поэтому лицензию я проверить не могу — проверка по самому тексту предложения.

```
VERDICT: Suspicious (подозрительно)
Red flags:
• "4% в месяц" — если доход фиксированный или «гарантированный», это главный признак схемы Понци (старым вкладчикам платят деньгами новых). Реальные вложения то растут, то падают.
• "лицензия ЦБ №0123" — номер из самого предложения ничего не доказывает. Проверять нужно только в официальном реестре, не по их номеру, сайту или телефону.
Maths: 4% в месяц → 1,04^12 ≈ 1,60, то есть ≈ +60% в год. Обещать такое стабильно не может ни одна обычная компания.
Licence: not checked — https://www.cbar.az/page-200/investment-companies (not opened)
Safe next step: найдите точное название "Kapital Growth Invest" в реестре ЦБА по ссылке выше. Иностранная лицензия не даёт права продавать инвестиции в Азербайджане (предупреждение ЦБА от 21.08.2026).
Report: жалоба в соцсети/мессенджере · Центральный банк Азербайджана (cbar.az) · киберполиция (verify: официальная страница)
```

Если они обещают «гарантированные» 4% или платят за приглашение друзей — это уже шаблон Likely scam (вероятная схема). Пришлите результат поиска в реестре — разберу.

Максимальный процент по кредитам: точную цифру по памяти не даю. verify: https://www.cbar.az (официальные решения ЦБА о ставках).

*Только для обучения, не финансовый совет. Проверяйте лицензии на официальном сайте регулятора.*
````

### Eval 9

````text
Müqaviləni imzalamazdan əvvəl bütün rüsumları yoxlayın.

```
TRUE COST (KREDİTİN REAL QİYMƏTİ)
Borc: 2000 AZN · Faiz: 24% illik · Müddət: 12 ay · Rüsum: verilməyib
Aylıq ödəniş: ≈ 189,12 AZN   Cəmi ödəniş: ≈ 2269,43 AZN   Faiz: ≈ 269,43 AZN
Necə: aylıq faiz r = 24% / 12 = 0,02
P = 2000 × 0,02 / (1 − 1,02^−12) ≈ 40 / 0,2115 ≈ 189,12
Ucuz variant: 6 ay → ayda ≈ 357,05, cəmi ≈ 2142,32, faiz ≈ 142,32 AZN (≈127 AZN az)
Diqqət: rüsum və ya "sığorta" (əlavə xərc) da kreditin qiymətidir; gecikmə cəriməsi.
```

Kredit kartında minimum ödəniş — növbəti mesajda izah edim. Daha?

*Yalnız maarifləndirici məlumatdır, maliyyə məsləhəti deyil. Lisenziyaları rəsmi tənzimləyicinin saytında yoxlayın.*
````

