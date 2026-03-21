# Wave 1 First-5 Send Packet — multi-llm-benchmark-dashboard

## Purpose

Posledni prakticky bridge mezi `WAVE1-LIVE-EVIDENCE-BOARD.md` a realnym odeslanim prvnich 5 zprav.

Tenhle packet nedela novy routing ani novy research.
Dela jen 3 veci:
- drzi **presne poradi** prvnich 5 leadu
- sklada k nim **copy-paste first-touch text** na jednom miste
- predvyplnuje **minimalni log radky**, aby se po odeslani jen doplnil datum, kanal a status

Cil:
- zkratit live execution z vice souboru na jeden packet
- snizit sanci, ze se pri prvnim sendu rozbije trigger / framing / artifact pairing
- dostat projekt co nejbliz k prvni reply evidence bez dalsi dokumentacni smycky

---

## Source-of-truth note

Plati toto poradi pravdy:
1. `execution/WAVE1-LIVE-EVIDENCE-BOARD.md` = canonical send order
2. `execution/WAVE1-OUTREACH-BATCH.md` = canonical framing + CTA + artifact routing
3. tento packet = canonical wording pro first-live-send subset, kdyz se posila presne tohle first-5 poradi
4. `execution/OUTREACH-LOG-TEMPLATE.md` = canonical evidence labels po sendu a reply
5. `execution/WAVE1A-PERSONALIZED-SKELETONS.md` a dalsi skeletony = sirsi wording pro zbytek Wave 1 mimo tenhle first-5 subset

Kdyz se zmeni routing, neprepisovat ho tady jako prvni.

---

## First-5 send order

| Order | Company | Contact | Verification | Trigger | Framing | CTA | Primary artifact | Fallback artifact |
|---|---|---|---|---|---|---|---|---|
| 1 | SumUp | Ana Casado | person_verified | budget_fallback | scorecard | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` |
| 2 | Magic Patterns | Alexander Danilowicz | person_verified | pre_llmops_gap | scorecard | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` |
| 3 | Canva | Andreas Schuster | person_verified | budget_fallback | scorecard | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` |
| 4 | Graphite | Quinten Farmer | person_verified | new_ai_surface | scorecard | send sample scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` |
| 5 | Notion | Sarav Bhatia | person_verified | new_ai_surface | dashboard | ask for 20min demo call | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` |

---

## Operator rules for this packet

- nic nevymyslet mimo canonical wording nize
- `scorecard` leadum neposilat dashboard-first wording
- `dashboard` leadum nenutit scorecard jako primary pitch; scorecard je fallback asset pri odmitnuti callu
- po odeslani okamzite propsat radek do logu nize
- do notes zapsat presne:
  - `trigger_used: ...`
  - `trigger_confirmed: unclear`
  - `trigger_shift: none`

---

## 1) SumUp — Ana Casado

- **Channel:** LinkedIn
- **Trigger:** `budget_fallback`
- **Framing:** `scorecard`
- **CTA:** `send sample scorecard`
- **Sent artifact:** `scorecard`
- **Primary artifact file:** `execution/SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
- **Fallback artifact file:** `execution/SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md`

### Copy-paste first touch
Ahoj Ano,

ověřuju, jestli týmy kolem operations a AI chtějí **use-case scorecards** pro výběr LLM modelu místo dalšího obecného benchmarku.

U SumUp mi to sedí hlavně na **support + fallback** rozhodování, kde je důležitý poměr kvalita odpovědi, náklady a spolehlivá budget varianta.

V jednom scorecard výstupu by bylo vidět:
- best overall model
- best budget variantu
- safest fallback
- kde je tradeoff kvalita vs cena vs latence

Jestli chceš, pošlu 1 ukázkovou scorecard pro support workflow a stačí mi krátký feedback, jestli je to pro vás užitečný formát.

---

## 2) Magic Patterns — Alexander Danilowicz

- **Channel:** LinkedIn + company site
- **Trigger:** `pre_llmops_gap`
- **Framing:** `scorecard`
- **CTA:** `send sample scorecard`
- **Sent artifact:** `scorecard`
- **Primary artifact file:** `execution/SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
- **Fallback artifact file:** `execution/SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md`

### Copy-paste first touch
Ahoj Alexander,

ověřuju, jestli AI-native týmy chtějí **use-case scorecards** pro výběr LLM modelu místo obecného leaderboardu.

U Magic Patterns mi to sedí hlavně na **coding + product workflow**, kde se často řeší, jestli je důležitější top kvalita, rychlost nebo rozumný cost-performance.

Scorecard má ukázat v jednom výstupu:
- best overall
- best budget pick
- safest fallback
- kde je tradeoff kvalita vs cena vs latence

Jestli chceš, pošlu 1 ukázkovou scorecard právě pro tenhle typ workflow. Stačí mi pak stručný feedback, jestli by to pro vás bylo užitečné, nebo mimo.

---

## 3) Canva — Andreas Schuster

- **Channel:** LinkedIn
- **Trigger:** `budget_fallback`
- **Framing:** `scorecard`
- **CTA:** `send sample scorecard`
- **Sent artifact:** `scorecard`
- **Primary artifact file:** `execution/SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
- **Fallback artifact file:** `execution/SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md`

### Copy-paste first touch
Ahoj Andreas,

ověřuju, jestli AI týmy chtějí **use-case scorecards** pro výběr LLM modelu místo dalšího obecného leaderboardu.

U Canvy mi to sedí hlavně na **support assistant / AI Help Experience** workflow, kde je důležitý poměr kvalita odpovědi, náklady a spolehlivá budget varianta.

V jednom scorecard výstupu by bylo vidět:
- best overall model
- best budget variantu
- safest fallback
- kde je tradeoff kvalita vs cena vs latence

Jestli chceš, pošlu 1 ukázkovou scorecard pro support workflow a stačí mi krátký feedback, jestli je to pro vás užitečný formát.

---

## 4) Graphite — Quinten Farmer

- **Channel:** LinkedIn + request demo
- **Trigger:** `new_ai_surface`
- **Framing:** `scorecard`
- **CTA:** `send sample scorecard`
- **Sent artifact:** `scorecard`
- **Primary artifact file:** `execution/SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
- **Fallback artifact file:** `execution/SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md`

### Copy-paste first touch
Ahoj Quintene,

overuju, jestli AI týmy chtějí **use-case scorecards** pro výběr LLM modelu místo dalšího obecného leaderboardu.

U Graphite mi to sedí hlavně na **coding assistant / code review workflow**, kde se často řeší, jestli je důležitější top kvalita návrhu, rychlá odezva nebo rozumný cost-performance.

V jedné scorecard by bylo vidět:
- best overall model
- best budget pick
- safest fallback
- kde je tradeoff kvalita vs cena vs latence

Jestli chceš, pošlu 1 ukázkovou scorecard právě pro coding assistant use case. Stačí mi pak stručný feedback, jestli je to pro vás užitečný formát, nebo mimo.

---

## 5) Notion — Sarav Bhatia

- **Channel:** LinkedIn + request demo
- **Trigger:** `new_ai_surface`
- **Framing:** `dashboard`
- **CTA:** `ask for 20min demo call`
- **Sent artifact:** `dashboard`
- **Primary artifact file:** `execution/SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
- **Fallback artifact file:** `execution/SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md`

### Copy-paste first touch
Ahoj Sarave,

ověřuju zájem o jednoduchý **decision dashboard** pro týmy, které porovnávají více LLM modelů podle konkrétního use case — kvalita, cena, latence a fallback v jednom compare workflow.

U Notionu mi to sedí hlavně na **multi-model decision workflow**, kde se model choice může rychle propsat do kvality feature i provozních nákladů.

Nejde mi o další leaderboard. Spíš o pohled, kde tým rychle vidí:
- best overall model
- budget variantu
- bezpečný fallback
- co se změnilo proti poslednímu rozhodnutí

Dával by ti smysl krátký 20min call? Když ne, klidně pošlu i sample scorecard pro workspace AI use case a stačí stručný feedback.

---

## Prefilled outreach log rows

Tyhle radky po odeslani zkopirovat do `execution/OUTREACH-LOG-TEMPLATE.md` a jen doplnit datum / skutecny kanal / stav.

| Date | Company | Contact | Segment | Buyer situation | Framing | CTA | Channel | Status | Sent artifact | First reply artifact | Reply quality | Preferred artifact | Status quo | Status-quo break | Pain (1-5) | Pricing band | Price probe | Pro signal | Next step | Notes / exact phrasing |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---:|---|---|---|---|---|
| YYYY-MM-DD | SumUp | Ana Casado | SaaS s AI feature | budget ceiling a fallback rozhodnuti | scorecard | sample scorecard | LinkedIn | drafted | scorecard | unknown | none | unknown | spreadsheet | speed | 5 | enterprise | none | neutral | send first message | trigger_used: budget_fallback; trigger_confirmed: unclear; trigger_shift: none |
| YYYY-MM-DD | Magic Patterns | Alexander Danilowicz | AI startup | lightweight vrstva pred plnym LLMOps stackem | scorecard | sample scorecard | LinkedIn + company site | drafted | scorecard | unknown | none | unknown | spreadsheet | speed | 5 | 149_plus | none | neutral | send first message | trigger_used: pre_llmops_gap; trigger_confirmed: unclear; trigger_shift: none |
| YYYY-MM-DD | Canva | Andreas Schuster | SaaS s AI feature | rychle porovnat modely pro support use case | scorecard | sample scorecard | LinkedIn | drafted | scorecard | unknown | none | unknown | unclear | unclear | 4 | enterprise | none | neutral | send first message | trigger_used: budget_fallback; trigger_confirmed: unclear; trigger_shift: none |
| YYYY-MM-DD | Graphite | Quinten Farmer | AI startup | rychle porovnava modely pro novy use case | scorecard | sample scorecard | LinkedIn + request demo | drafted | scorecard | unknown | none | unknown | unclear | unclear | 5 | 149_plus | none | neutral | send first message | trigger_used: new_ai_surface; trigger_confirmed: unclear; trigger_shift: none |
| YYYY-MM-DD | Notion | Sarav Bhatia | SaaS s AI feature | ma evaly nebo quality signaly, ale chybi finalni decision layer | dashboard | demo | LinkedIn + request demo | drafted | dashboard | unknown | none | unknown | provider_native | refreshability | 5 | enterprise | none | neutral | send first message | trigger_used: new_ai_surface; trigger_confirmed: unclear; trigger_shift: none |

---

## Done definition for this packet

Packet splnil ucel, pokud operator bez otevirani dalsich souboru zvladne:
1. videt presne poradi first-5
2. zkopirovat first-touch wording
3. vedet jaky artifact patri ke kteremu leadu
4. po odeslani hned zapsat canonical evidence radek

Pokud ani po tomhle live send neprobehne, dalsi poctivy krok uz neni dalsi docs expansion, ale skutecne odeslani nebo explicitni rozhodnuti, proc se send odklada.
