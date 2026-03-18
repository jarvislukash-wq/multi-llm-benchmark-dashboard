# Validation Runbook — multi-llm-benchmark-dashboard

## Purpose

Převést existující enrichment a validační assety do jednoho praktického plánu, podle kterého se dá během 14 dnů ověřit:
- jestli je problém dost bolestivý
- jestli funguje messaging
- jestli existuje ochota zaplatit
- jestli má projekt důvod postoupit do SPEC fáze

Tento dokument neřeší plný go-to-market. Řeší jen nejkratší cestu k rozhodnutí **pokračovat / nepokračovat / zúžit wedge**.

---

## 1. Validation goals

### Primary goals
1. Potvrdit, že AI týmy skutečně řeší chaos při výběru modelu.
2. Ověřit, že use-case scorecards jsou srozumitelnější než obecné leaderboardy.
3. Zjistit, jestli buyer vidí hodnotu ve spojení public benchmarků + interních evalů.
4. Ověřit, že existuje realistická willingness to pay v pásmu **€39–149/měs**.

### Secondary goals
- zjistit, který ICP reaguje nejlépe
- zjistit, jestli trh nejsilněji reaguje na framing `dashboard`, `scorecard` nebo `decision memo`
- vybrat první wedge pro případný SPEC

---

## 2. 14-day execution plan

| Den | Aktivita | Výstup |
|---|---|---|
| 1 | vybrat messaging variantu A/B/C pro první test | jedna primární hero message |
| 1-2 | připravit jednoduchou landing page / form | URL + CTA formulář |
| 2 | připravit outreach list 30 kontaktů | tracker s prioritou |
| 3-7 | oslovit první vlnu 15 kontaktů | reply rate + booked calls |
| 4-10 | udělat 8-10 discovery callů | interview notes + pain scores |
| 7 | vyhodnotit messaging a CTA | první conversion snapshot |
| 8-12 | druhá vlna outreach + follow-up | dalších 10-15 oslovení |
| 10-13 | poslat 3 use-case scorecards vybraným leadům | reakce na relevance scorecards |
| 14 | rozhodnutí continue / narrow / stop | stručný validation verdict |

---

## 3. Success thresholds

### Minimum bar
Projekt má důvod pokračovat, pokud během prvního validačního sprintu padne aspoň:
- **8+ relevantních odpovědí** od ICP
- **5+ discovery callů** s lidmi, kteří splní screener
- **3+ respondenti**, kteří potvrdí, že dnes výběr modelu řeší bolestivě / neefektivně
- **2+ respondenti**, kteří řeknou, že by za řešení podobného typu reálně platili nebo chtěli pilot

### Strong signal
Silný signál pro pokračování do SPEC:
- **10+ kvalifikovaných callů**
- **40 %+ respondentů** explicitně potvrdí vysokou pain level
- **3+ design-partner signály** (pilot, demo, follow-up s daty, intro do týmu)
- aspoň **1 jasně dominantní wedge** (např. AI startup CTO nebo AI agentury)

### Kill / narrow signals
Zúžit nebo stopnout, pokud nastane aspoň jedno:
- lidé problém uznávají, ale nechtějí za něj platit
- největší hodnota je jen v jednorázovém reportu, ne v produktu
- interní eval import je nutný od prvního dne a bez něj je dashboard bezcenný
- messaging nevytváří dostatek call bookingů ani po 2 iteracích

---

## 4. Metrics to track

### Funnel metrics
- landing page visits
- CTA clicks
- form submits
- submit rate
- outreach sent
- outreach replies
- positive replies
- calls booked
- calls completed

### Discovery metrics
- pain score (1-5)
- frequency of model-switching
- number of models/providers in use
- current decision workflow maturity
- strongest objection
- preferred artifact: dashboard / report / API
- `price_probe`: none / under_39 / 39_149 / 149_plus / enterprise
- `pro_signal`: positive / neutral / negative

### Decision metrics
- percent of calls that confirm the problem
- percent of calls that react positively to scorecards
- percent of calls asking for internal data merge
- percent of calls willing to see pilot or mockup

---

## 5. Interview scoring rubric

Po každém callu doplnit tyto 4 skóre:

| Kritérium | Skóre 1 | Skóre 3 | Skóre 5 |
|---|---|---|---|
| Problem intensity | problém je okrajový | občas nepříjemný | častý, drahý a otravný |
| Workflow chaos | mají relativně jasno | workflow je částečně roztříštěné | benchmarky/evaly/cena jsou úplný chaos |
| Purchase intent | jen zvědavost | chce follow-up | chce pilot / demo / early access |
| Scorecard fit | scorecard moc nepomáhá | zajímavé, ale ne zásadní | scorecard framing přesně sedí |

### Quick interpretation
- **16-20 bodů** = velmi silný lead
- **11-15 bodů** = relevantní, ale potřebuje další segmentaci
- **≤10 bodů** = slabý signál nebo špatný ICP

---

## 6. Recommended first wedge

Pokud není kapacita validovat vše, začít tímto pořadím:
1. **AI startup CTO / applied AI lead**
2. **AI agentura founder / delivery lead**
3. **SaaS product lead s aktivní AI feature**

### Why
- mají kratší rozhodovací cyklus
- bolest kolem model selection je u nich častější a čerstvá
- snáz popíšou cost/quality tradeoff
- vyšší šance na rychlý design-partner signal

---

## 7. Landing page test design

### Variant to test first
Začít variantou **B — engineering angle**.

### Reason
- nejkonkrétněji pojmenovává porovnání modelů
- nejméně zní jako generický analytics dashboard
- nejlépe sedí primárnímu ICP (AI engineering / CTO)

### Suggested page sections
1. Hero + CTA
2. Problem snapshot
3. 3 use-case scorecards
4. Public + internal data merge value prop
5. FAQ / objections
6. CTA form

### Suggested form fields
- work email
- role
- team size
- hlavní use case
- kolik modelů dnes testují
- chci demo / chci scorecards / chci early access

---

## 8. Decision tree after sprint

### Go
Pokračovat do SPEC, pokud:
- je potvrzený problém
- existuje aspoň jeden silný ICP segment
- lidi rozumí scorecard framingu
- objevily se signály pro placený pilot nebo ochotu platit

### Narrow
Zúžit scope, pokud:
- problém existuje, ale jen v jednom use case
- lidi chtějí spíš report nebo API než dashboard
- největší hodnota je jen v public + pricing compare bez interních dat

### Stop
Nestavět dál, pokud:
- rozhovory neukazují dost silný pain
- kupující nepovažují problém za dost důležitý
- dashboard je vnímaný jako nice-to-have bez rozpočtu

---

## 9. Phase-advance handoff recommendation

Projekt je připravený na přechod z enrichment do další fáze ve chvíli, kdy budou splněny tyto 4 body:
1. proběhne aspoň 5 kvalifikovaných interview
2. bude existovat jasně vybraný wedge ICP
3. bude rozhodnuto, zda první wedge a messaging stavět jako `dashboard`, `scorecard` nebo `decision memo / hybrid`
4. bude potvrzen minimální value proposition pro první placený pilot

Do té doby je interní enrichment dokumentace dostatečně připravená; další neznámé už jsou hlavně externí validační data.

---

## 10. Lightweight verdict capture

Jakmile bude existovat první malý balík reply/call signálů, zapsat stručný verdict do `execution/WAVE1-VALIDATION-VERDICT-TEMPLATE.md`.

Template má schválně držet jen 4 rozhodnutí:
- který segment je nejsilnější
- který framing vyhrává (`dashboard`, `scorecard`, `memo` nebo hybrid)
- jaká je první realistická placená jednotka
- jestli další vlna má znamenat `continue`, `narrow` nebo `stop`

Tím se Wave 1 nevyhodnotí jen podle reply rate, ale i podle obchodního směru pro první SPEC.

