# Outreach Playbook — multi-llm-benchmark-dashboard

## Goal

Převést existující validation assets do první outreach vlny bez dalšího vymýšlení.

Cíl první vlny:
- oslovit **15 kvalifikovaných leadů**
- získat **5+ odpovědí**
- domluvit **3+ discovery calls**
- ověřit, jestli lépe funguje CTA **demo** nebo **scorecards**

---

## Wave 1 target mix (15 leads)

### P1 — AI startup
- 5× CTO / cofounder
- 3× Applied AI lead / founding engineer

### P2 — AI agentura
- 3× founder / delivery lead

### P3 — SaaS with active AI feature
- 2× product lead
- 2× engineering lead

---

## Qualification rules

Lead je vhodný, pokud sedí aspoň 3 z 5:
- tým používá nebo testuje 3+ modelů / providerů
- řeší cost-quality-latency tradeoff
- v posledních 90 dnech měnil model nebo fallback
- používá evaly, prompt tests nebo produkční telemetry
- někdo v roli rozhoduje o stacku nebo rozpočtu

---

## Framing assignment rules

Neotestujeme jen CTA. Každému leadovi přiřadíme i hlavní framing produktu.

| Segment | Primary framing | Secondary framing | Default CTA |
|---|---|---|---|
| AI startup CTO / applied AI | decision dashboard | use-case scorecard | demo |
| AI agentura founder / delivery | use-case scorecard | decision dashboard | scorecard |
| SaaS engineering lead | decision dashboard | use-case scorecard | demo |
| Enterprise AI / governance | decision memo / executive hybrid | decision dashboard | executive feedback |

### What to log after each send
- framing sent: dashboard / scorecard / memo
- CTA used: demo / scorecard / executive feedback
- primary artifact chosen before send
- fallback artifact prepared before send
- sent artifact = co opravdu odeslo jako prvni asset
- reply quality: none / weak / relevant / high-intent
- preferred artifact mentioned by lead


### Buyer-situation routing for outreach

Pouzij stejnou routing logiku jako v `execution/SMOKE-TEST-LANDING-PAGE.md`, aby lead dostal stejny framing v outboundu i po prokliku na landing.

| Buyer situace | Poslat jako primary framing | CTA | Primary artifact |
|---|---|---|---|
| Buyer rychle porovnava modely pro novy use case | scorecard | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` |
| Buyer uz ma evaly nebo traces, ale chybi finalni rozhodnuti | dashboard | 20min demo call | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` |
| Buyer potrebuje obhajit volbu modelu pred managementem nebo klientem | memo | executive feedback | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` |
| Buyer resi budget ceiling a fallback model | scorecard | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` |
| Buyer hleda lightweight vrstvu pred plnym LLMOps stackem | scorecard -> dashboard az po reply | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` |

Prakticke pravidlo: kdyz si nejsi jisty, zacni `scorecard`. `dashboard` pouzij hlavne tam, kde lead uz premysli v opakovanem compare workflow. `memo` drz jen pro executive, governance nebo client-facing situace.

Poznamka pro execution: `WAVE1A-PERSONALIZED-SKELETONS.md` a `WAVE1B-PERSONALIZED-SKELETONS.md` uz tenhle buyer-situation routing plne prebiraji. Pri personalizaci tedy nemen buyer framing mimo zapsanou situaci ve Wave batchi, jen dopln kontext o firme a kontaktu.

**Source-of-truth note:** Tento playbook je operator guide pro Wave 1 execution. Finalni routing rozhodnuti pro konkretni leady zustavaji v `execution/WAVE1-OUTREACH-BATCH.md`; personalizace ve `WAVE1A`/`WAVE1B` je pouze provadi do textu, neprepisuje.

---

## Outreach angle by segment

### 1. AI startup CTO
**Pain angle:** chaos v model selection a obhajoba před byznysem

**Message goal:** dostat 20min call nebo zájem o scorecard

**Template**
Ahoj {{first_name}},

řeším teď validation pro jednoduchý dashboard, který srovná GPT / Claude / Gemini a další modely podle konkrétního use case — kvalita, cena, latence a fallback v jedné scorecard.

Mluvím hlavně s týmy, které aktivně testují 3+ modelů a musí obhájit, proč nasadily právě tenhle.

Sedí na vás něco z toho?
- výběr modelu se opakuje od nuly při každém novém release
- benchmarky, pricing a interní evaly jsou roztříštěné
- je těžké vysvětlit managementu cost vs quality tradeoff

Kdyby jo, stačil by mi krátký 20min call. Když nebudeš chtít call, můžu poslat i ukázkovou scorecard pro váš use case.

---

### 2. Applied AI lead / engineer
**Pain angle:** benchmark chaos + interní evaluace bez jednoho compare view

**Template**
Ahoj {{first_name}},

ověřuju, jestli AI týmy chtějí decision dashboard pro výběr LLM modelů podle use case, ne jen další leaderboard.

Myšlenka je jednoduchá: spojit veřejné benchmarky, pricing a interní eval signály do jedné scorecard a ukázat třeba best overall / best budget / safest fallback.

Zajímá mě, jak dnes u vás porovnáváte 3+ modelů a co je na tom nejvíc opruz.

Dal bys 20 minut? Případně pošlu 1 ukázkovou scorecard a stačí mi krátký feedback.

---

### 3. AI agentura founder / delivery lead
**Pain angle:** opakované vysvětlování model stacku klientům

**Template**
Ahoj {{first_name}},

řeším validation pro nástroj, který pomůže agenturám obhájit výběr LLM modelu klientovi pomocí sdílitelných scorecards.

Typicky pro use casy jako support bot, RAG, coding nebo extraction:
- co je nejlepší overall
- co je nejlepší budget varianta
- co je bezpečný fallback

Dává mi smysl mluvit hlavně s lidmi, kteří tohle řeší opakovaně napříč klienty.

Kdyby to bylo relevantní, rád pošlu ukázkovou scorecard nebo dáme 20min call.

---

## Follow-up cadence

Tento playbook drzi jen timing. Kanonicke Day 3 / Day 7 texty podle `dashboard`, `scorecard` a `memo` framingu jsou v `execution/WAVE1-FOLLOW-UP-SEQUENCES.md`.

### Day 0
- poslat first touch podle `execution/WAVE1-OUTREACH-BATCH.md` a odpovidajiciho personalized skeletonu

### Day 3
- poslat framing-specific follow-up z `execution/WAVE1-FOLLOW-UP-SEQUENCES.md`
- kdyz lead nechce call, nabidnout tam definovany fallback artifact

### Day 7
- poslat posledni low-friction follow-up z `execution/WAVE1-FOLLOW-UP-SEQUENCES.md`
- uz nevymyslet novy messaging mimo kanonickou follow-up sekvenci

---

## Call booking objective

Na callu nepotřebujeme pitchovat produkt. Potřebujeme zjistit:
1. jak dnes vybírají model
2. jak drahý je špatný výběr
3. jestli jim dává smysl use-case scorecard
4. jestli chtějí dashboard, report nebo API
5. jestli by za to zaplatili nebo šli do pilotu

---

## Manual ops checklist

- [ ] vybrat 15 leadů podle prioritního mixu
- [ ] každý lead zapsat do `DISCOVERY-TRACKER.md`
- [ ] tagnout segment a prioritu P1/P2/P3
- [ ] před odesláním potvrdit `Primary artifact` a `Fallback artifact` podle `execution/WAVE1-OUTREACH-BATCH.md`
- [ ] poslat první vlnu se 2 CTA variantami: demo vs scorecards
- [ ] po odeslání okamžitě zapsat `Sent artifact` do `execution/OUTREACH-LOG-TEMPLATE.md`
- [ ] po každé odpovědi zapsat objection, preferred artifact a další krok
- [ ] po každém callu vyplnit scoring rubric z `VALIDATION-RUNBOOK.md`

---

## Messaging test to compare

### Variant 1 — Demo CTA
Pro leady s vyšším purchase intentem a engineering ownership.

### Variant 2 — Scorecard CTA
Pro vytížené leady nebo consultative segment, kde je nižší tření.

### What to learn
- který framing získá nejkvalitnější odpovědi
- který CTA získá víc odpovědí
- který segment reaguje nejrychleji
- kde je problém nejbolestivější

---

## Exit criteria for wave 1

Wave 1 je úspěšná, pokud z 15 leadů padne aspoň:
- 5 odpovědí
- 3 discovery calls
- 2 potvrzené high-pain leady
- 1 jasný signál preferovaného formátu: dashboard / report / API / hybrid

Pokud ne, upravit messaging nebo zúžit ICP dřív, než se dělá další asset work.
