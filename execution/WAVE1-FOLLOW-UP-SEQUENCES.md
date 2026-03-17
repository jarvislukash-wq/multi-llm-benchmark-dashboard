# Wave 1 Follow-up Sequences — multi-llm-benchmark-dashboard

## Purpose

Doplnit ultra-krátké follow-up varianty pro všechny 3 hlavní framingy z Wave 1:
- `dashboard`
- `scorecard`
- `memo`

Cíl:
- druhý a třetí dotek mají být stejně ready-to-send jako first touch
- follow-up má být kratší než první zpráva
- každý follow-up má držet původní framing a CTA
- když lead nechce call, vždy nabídnout lehčí artefakt místo dalšího pitchování

---

## Rules

- Day 3 = lehké připomenutí bez tlaku
- Day 7 = poslední low-friction ping
- max 45-70 slov
- nepřidávat nové claims
- držet se stejného use-case angle jako v first touch skeletonu
- po odeslání zapsat reply quality do `execution/OUTREACH-LOG-TEMPLATE.md`

---

## 1. Dashboard framing

### Best fit
- AI startup CTO / applied AI
- SaaS engineering lead
- týmy, které pravděpodobně chtějí compare workflow nebo demo

### Day 3 follow-up
Ahoj {{first_name}}, jen se připomínám k tomu **decision dashboard** nápadu pro {{use_case}}. Pokud je call zbytečný, klidně pošlu jen 1 jednoduchou scorecard, ať je hned vidět, jestli by ten compare workflow pro vás měl hodnotu.

### Day 7 follow-up
Poslední ping — řeším teď hlavně týmy, které aktivně porovnávají víc modelů pro {{use_case}}. Kdyby bylo jednodušší mrknout nejdřív na výstup než řešit call, pošlu krátkou sample scorecard a stačí mi stručný feedback.

### CTA fallback
- primární: 20min demo call
- fallback: sample scorecard pro konkrétní use case

### Signal to log
- chce demo / workflow / compare view
- ptá se na weights, alerts nebo historické srovnání
- odmítá call, ale chce sample output

---

## 2. Scorecard framing

### Best fit
- AI agentura
- founder s nízkou tolerancí na call bez artefaktu
- týmy, kde funguje konkrétní use-case výstup

### Day 3 follow-up
Ahoj {{first_name}}, jen navazuju — pokud to je relevantní pro {{use_case}}, můžu poslat 1 ukázkovou **scorecard** bez dalšího pitchování. Zajímalo by mě jen, jestli je tenhle formát užitečný, nebo mimo.

### Day 7 follow-up
Poslední připomenutí — když mi jen pošleš use case, pošlu krátkou sample scorecard a tím to pro mě končí. Neřeším teď prodej, spíš ověřuju, jestli tenhle formát vůbec otevírá smysluplnou konverzaci.

### CTA fallback
- primární: send sample scorecard
- fallback: very short written feedback, bez callu

### Signal to log
- chce sample output
- reaguje na konkrétní use case
- mluví spíš o reportu / exportu než dashboardu

---

## 3. Memo framing

### Best fit
- enterprise AI / governance owner
- lead, který potřebuje explainability a alignment
- cost / risk / approval-heavy prostředí

### Day 3 follow-up
Ahoj {{first_name}}, krátce navazuju na ten **decision memo** koncept pro {{use_case}}. Když nebude dávat smysl call, rád pošlu 1 stránku jako sample a zajímal by mě jen stručný pohled, jestli je tenhle formát použitelný pro tým i management.

### Day 7 follow-up
Poslední ping — pokud je u vás kolem {{use_case}} důležité obhájit model choice i mimo engineering, můžu poslat krátký sample memo / scorecard. Když to teď není priorita, úplně v pohodě.

### CTA fallback
- primární: executive feedback
- fallback: 1-page sample memo / scorecard

### Signal to log
- chce executive summary
- řeší approval, governance nebo cost justification
- preferuje hybrid report + dashboard view

---

## Personalization placeholders

Do follow-upu doplnit jen 1 z těchto prvků:
- `{{use_case}}`
- jméno produktu / týmu
- veřejně dohledatelný ownership angle

Nepřidávat víc než jeden personalizační detail. Follow-up má být lehký.

---

## Recommended usage

- `dashboard` first touch bez reply -> Day 3 dashboard follow-up -> Day 7 dashboard follow-up s nabídnutou scorecard
- `scorecard` first touch bez reply -> Day 3 scorecard follow-up -> Day 7 low-friction close
- `memo` first touch bez reply -> Day 3 memo follow-up -> Day 7 executive close

---

## Exit condition

Jakmile přijde prvních 5-8 odpovědí:
- porovnat reply quality podle framingu
- zjistit, jestli follow-up otevírá víc odpovědí než first touch sám
- rozhodnout, jestli další vlna bude `dashboard-first`, `scorecard-first` nebo `hybrid`
