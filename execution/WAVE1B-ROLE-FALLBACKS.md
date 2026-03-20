# Wave 1B Role-Based Fallbacks — multi-llm-benchmark-dashboard

## Purpose

Odblokovat Wave 1B u firem, kde je **account fit veřejně potvrzený**, ale konkrétní named contact není v aktuálně uloženém veřejném důkazu potvrzený jako `person_verified`.

Tento dokument neřeší nový routing. Jen převádí existující Wave 1 assignment do bezpečné account-level varianty:
- bez přehnaného tvrzení o veřejně ověřeném jménu
- bez blokace celé vlny
- se stejným framingem, CTA a artifact mappingem jako v `execution/WAVE1-OUTREACH-BATCH.md`

---

## Source-of-truth note

Plati toto poradi pravdy:
1. `execution/WAVE1-CONTACT-VERIFICATION.md` drzi verification confidence
2. `DISCOVERY-TRACKER.md` drzi kanonicky Wave 1 routing a next step
3. `execution/WAVE1-OUTREACH-BATCH.md` drzi finalni framing, CTA a artifact assignment
4. tento dokument jen pridava bezpečny **role-based fallback**, kdyz named contact neni public-person-verified

---

## When to use role-based fallback

Pouzit jen kdyz plati vsechny 3 body:
- firma je `account_verified`
- named contact neni verejne dolozeny v ulozenem dukazu
- nechceme cekat na dalsi manualni research, aby se Wave 1 neposouvala

Nepouzivat u `person_verified` leadu — tam zustava named-contact outreach.

---

## Lead 1 — Coursera

- **Verification status:** account_verified
- **Canonical framing:** memo
- **Canonical CTA:** executive feedback
- **Primary artifact:** `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md`
- **Fallback artifact:** `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
- **Role-based fallback target:** AI engineering manager / learning AI platform lead / AI product lead
- **Buyer situation:** potrebuje obhajit volbu modelu pred managementem nebo klientem
- **Safe channel:** LinkedIn role search + Coursera engineering / leadership path

### Role-based skeleton
Ahoj,

řeším validation pro lehký **decision memo layer** nad LLM stackem — něco mezi executive memem a engineering dashboardem.

U týmů jako Coursera mě zajímá hlavně to, jestli dává smysl formát, který pomůže obhájit **volbu modelu pro learning-oriented AI features** podle kvality, ceny, latence a fallback strategie.

Nejde mi o další leaderboard. Spíš o stručný podklad, který je použitelný pro engineering i management.

Když to dává smysl, rád pošlu 1 ukázkový decision memo / scorecard a zajímal by mě jen krátký feedback, jestli je tenhle formát užitečný.

### Execution note
- neodkazovat na konkrétní jméno, dokud není `person_verified`
- držet learning / explainability angle

---

## Lead 2 — Zapier

- **Verification status:** account_verified
- **Canonical framing:** dashboard
- **Canonical CTA:** 20min demo call
- **Primary artifact:** `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
- **Fallback artifact:** `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md`
- **Role-based fallback target:** AI product lead / AI platform lead / orchestration lead
- **Buyer situation:** ma evaly nebo quality signaly, ale chybi finalni rozhodnuti
- **Safe channel:** LinkedIn role search + Zapier contact/demo path

### Role-based skeleton
Ahoj,

řeším validation pro **decision dashboard**, který porovnává GPT / Claude / Gemini a další modely podle konkrétního use case — kvalita, cena, latence a fallback v jednom workflow.

U týmů jako Zapier mě zajímá hlavně, jestli dává smysl compare view pro **multi-model operations**, kde je těžké rychle rozhodnout, který model je nejlepší overall, který je budget varianta a který je bezpečný fallback.

Nejde mi o další leaderboard. Spíš o workflow, kde tým rychle vidí tradeoff a změny proti poslednímu rozhodnutí.

Když nebude dávat smysl call, klidně pošlu i sample scorecard pro podobný orchestration workflow a stačí stručný feedback.

### Execution note
- nepsat `Mike` ani jiný named-contact wording
- držet dashboard framing bez spekulací o interní architektuře

---

## Lead 3 — Loom

- **Verification status:** account_verified
- **Canonical framing:** scorecard
- **Canonical CTA:** send sample scorecard
- **Primary artifact:** `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
- **Fallback artifact:** `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md`
- **Role-based fallback target:** AI product lead / AI workflow owner / engineering lead
- **Buyer situation:** hleda lightweight vrstvu pred plnym LLMOps stackem
- **Safe channel:** LinkedIn role search + Atlassian/Loom contact path

### Role-based skeleton
Ahoj,

ověřuju, jestli týmy chtějí **use-case scorecards** pro výběr LLM modelu místo dalšího obecného benchmarku.

U týmů jako Loom mě zajímá hlavně, jestli je užitečný konkrétní scorecard výstup pro **high-volume AI workflow**, kde je důležitý poměr kvalita výstupu, rychlost a rozumný cost-performance.

V jedné scorecard by bylo vidět:
- best overall model
- best budget pick
- safest fallback
- kde je tradeoff kvalita vs cena vs latence

Když budeš chtít, pošlu 1 ukázkovou scorecard pro tenhle typ workflow a stačí mi krátký feedback, jestli je to užitečný formát, nebo mimo.

### Execution note
- nepoužívat named-contact oslovení
- držet low-friction scorecard-first vstup

---

## Operational rule

Pro `account_verified` firmy platí:
- named contact muze zustat v trackeru jako working candidate
- prvni bezpecny send se ale muze opřít o role-based fallback bez cekani na dalsi proof
- do outreach logu zapsat, ze slo o `role_based_fallback`
- pokud se pozdeji objevi `person_verified` proof, vratit se ke jmenné personalizaci

---

## Minimum success condition

Tento fallback je dostatecny, pokud umozni:
- neposouvat Wave 1B kvuli chybejicimu jmennemu dukazu
- zachovat stejny framing test `dashboard` vs `scorecard` vs `memo`
- nezavest do outreachi nepresny named-contact claim
