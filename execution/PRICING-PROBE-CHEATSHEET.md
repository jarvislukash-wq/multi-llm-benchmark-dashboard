# Pricing Probe Cheatsheet - Wave 1

## Purpose

Dat operatorovi kratky navod, **jak se ptat na cenu bez prestreleni a bez predstirani potvrzeneho willingness-to-pay**.

Pouzivej spolu s:
- `DISCOVERY-TRACKER.md`
- `execution/OUTREACH-LOG-TEMPLATE.md`
- `execution/WAVE1-VALIDATION-VERDICT-TEMPLATE.md`
- `COMPETITOR-PRICING-ANCHORS.md`

---

## Guardrail

Cil neni z leadu vytahnout presne euro.  
Cil je spolehlive zaradit signal do jednoho z labelu:

- `none`
- `under_39`
- `39_149`
- `149_plus`
- `enterprise`

A zaroven zapsat:
- `pro_signal = positive / neutral / negative`

---

## 3 safe questions

### 1. Artifact vs recurring workflow
Pouzij, kdyz buyer chape problem, ale jeste nemluvi o rozpoctu.

> "Je pro vas tohle spis jednorazova scorecard / memo vec, nebo opakovany team workflow, ke kteremu byste se vraceli pri zmene modelu a cen?"

**Interpretace:**
- jednorazovy artifact -> zatim spis `none` nebo `under_39`
- recurring team workflow -> kandidat na `39_149` nebo `149_plus`

### 2. Lightweight vs team-budget probe
Pouzij, kdyz buyer reaguje pozitivne na hodnotu.

> "Kdyby to realne zkratilo rucni compare a dalo vam sdilitelny vystup pro tym, je to pro vas spis lightweight self-serve nastroj, nebo uz neco z team budgetu?"

**Interpretace:**
- lightweight self-serve -> `under_39`
- team budget -> `39_149` nebo `149_plus`

### 3. Pilot vs SaaS motion
Pouzij u agentur, enterprise nebo buyeru s governance tonem.

> "Davalo by vam vetsi smysl platit za prubezny workspace, nebo spis za pilot / konkretni decision pack pro jeden use case?"

**Interpretace:**
- jednorazovy pilot / pack -> `149_plus` nebo `enterprise`, ale casto mimo self-serve
- recurring workspace -> silnejsi `39_149` / `149_plus`

---

## Fast mapping table

| Buyer signal | `price_probe` | `pro_signal` |
|---|---|---|
| "Posli to, ale budget na to nemame" | `none` | `negative` |
| "Jako maly tool bych to zkusil" | `under_39` | `neutral` |
| "Kdyby to fungovalo pro tym, nizsi stovky mesicne jsou OK" | `39_149` | `positive` |
| "Za tymovy workflow / vice lidi to klidne muze byt vic" | `149_plus` | `positive` |
| "Tohle by slo pres pilot / procurement / enterprise budget" | `enterprise` | `positive` |
| "Spis jednorazovy report nez nastroj" | ponech podle kontextu, casto `none` nebo `under_39` | vetsinou `neutral` |

---

## Segment-specific hint

### AI startup / applied AI lead
Nejdriv testuj recurring workflow.

Dobra otazka:
> "Jak casto se vam vraci model review nebo fallback rozhodnuti? Pokud opakovane, dava vam vetsi smysl scorecard workflow, nebo maly workspace?"

### AI agentura
Nejdriv testuj multi-client hodnotu.

Dobra otazka:
> "Je pro vas vetsi hodnota v jednom klientskem memo, nebo v tom mit opakovatelne scorecards napric klienty?"

### SaaS engineering lead
Nejdriv testuj team-budget framing.

Dobra otazka:
> "Kdyby to spojilo verejne benchmarky a vase interni evaly do jednoho rozhodnuti, je to pro vas spis mensi tool budget, nebo uz normalni team workflow budget?"

---

## Public anchor sanity check

Pouzivej v hlave tyto orientacni body:
- public benchmark intelligence je na trhu casto zdarma / acquisition vrstva
- low paid AI tooling muze zacinat kolem `$29-79`
- silnejsi recurring team workflow bezne zije kolem `$79-199`
- vyssi team / compliance motion skace vyrazne vys

To znamena:
- **nepretlacuj** kazdeho buyer do `149_plus`
- **nepodstrel** recurring team use case do ciste artifact pricingu, pokud buyer mluvi o pravidelnem review

---

## Logging rule

Po kazdem relevantnim signalu zapis do `execution/OUTREACH-LOG-TEMPLATE.md`:
- `price_probe`
- `pro_signal`
- 1 kratkou vetu proc

Priklad:
- `price_probe = 39_149`
- `pro_signal = positive`
- `notes = buyer sees recurring team compare value; not just one-off report`

---

## Decision rule

Pokud prvnich nekolik reply ukaze:
- prevazujici `none` / `under_39` -> wedge je mozna spis artifact / report / audit
- prevazujici `39_149` -> current Pro workspace hypothesis drzi
- caste `149_plus` / `enterprise` -> muze existovat silnejsi team / governance motion, ale az po live evidence
