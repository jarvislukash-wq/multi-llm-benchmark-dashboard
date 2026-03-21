# Sample Dashboard View — Customer Support Assistant

## Purpose

Toto je **sendable sample artifact** pro dashboard-first validation.

Neni to live produkt ani klikaci prototyp.
Je to 1-page preview toho, co ma buyer videt, kdyz nechce cist jen scorecard nebo memo, ale potrebuje rychle pochopit **decision dashboard view**.

Ma behem 2 minut ukazat:
- jak vypada compare workflow pro jeden use case
- ktery model je `best overall`, `best budget`, `best speed` a `safest fallback`
- co se zmenilo proti poslednimu rozhodnuti
- jestli buyer chce spis dashboard, scorecard nebo executive memo format

> Pozn.: cisla nize jsou **illustrative sample format**, ne live benchmark pull. Cilem je overit, jestli je tenhle dashboardovy vystup pro tym srozumitelny a uzitecny.

**Source-of-truth note:** tenhle sample artifact slouzi jen jako ukazka dashboard formatu pro validation outreach, ne jako routing rozhodnuti. Pro realny Wave 1 outreach rozhoduje, komu a s jakym framingem dashboard sample poslat, `execution/WAVE1-OUTREACH-BATCH.md` a odpovidajici personalizace ve `execution/WAVE1A-PERSONALIZED-SKELETONS.md` / `execution/WAVE1B-PERSONALIZED-SKELETONS.md`.

---

## Use case

**Use case:** customer support assistant pro SaaS

### Decision objective
Vybrat model stack, ktery udrzi:
- dobrou kvalitu odpovedi
- rozumny cost envelope
- rychlou odezvu v live supportu
- fallback pripravenost pri zmene ceny nebo vypadku

---

## Topline summary bar

| Widget | Current winner | Why it matters |
|---|---|---|
| Best overall | GPT-4.1 mini | nejvyvazenejsi kompromis kvalita / cena / latence |
| Best budget | Gemini Flash class | vysoky objem, rychlost, lepsi economics |
| Best speed | Gemini Flash class | nejbliz live-chat use case s nizkou cekaci dobou |
| Safest fallback | GPT-4.1 mini -> Gemini Flash class | jednoducha fallback logika bez tezke orchestrace |
| Best escalation lane | Claude Sonnet class | silnejsi odpovedi pro slozitejsi nebo citlivejsi dotazy |

---

## Compare table snapshot

| Model | Quality | Cost-efficiency | Latency | Fallback readiness | Risk | Overall score | Dashboard tag |
|---|---:|---:|---:|---:|---:|---:|---|
| GPT-4.1 mini | 8.5 | 7.5 | 8.0 | 8.5 | low | **8.2** | best_overall |
| Gemini Flash class | 7.5 | 8.5 | 9.0 | 8.0 | low | **8.1** | best_budget / best_speed |
| Claude Sonnet class | 9.0 | 6.0 | 7.0 | 7.5 | medium | **7.7** | escalation_lane |
| Open-weight budget class | 6.5 | 9.0 | 8.0 | 6.5 | medium_high | **7.5** | cost_floor |

---

## Recommendation widgets

### Default operating choice
**GPT-4.1 mini**
- nejbezpecnejsi start pro bezny support traffic
- dobry kompromis mezi kvalitou a economics
- jednoduse vysvetlitelne pro produkt i operations tym

### Budget / throughput lane
**Gemini Flash class**
- nejlepsi kandidat pro high-volume flow
- dava smysl tam, kde cena a rychlost vyhravaji nad maximalni kvalitou
- vhodne jako fallback nebo budget-first lane

### Escalation lane
**Claude Sonnet class**
- pro slozitejsi, citlivejsi nebo delsi konverzace
- ne jako plosny default, spis jako quality lane

---

## Change monitor preview

### What would trigger a recommendation refresh
- provider zmeni cenu o 15 %+ 
- novy model zmeni `best_budget` nebo `best_overall`
- interni eval ukaze pokles odpovedi u slozitejsich ticketu
- fallback model prestane davat economics smysl

### Example change card
- **Previous best budget:** open-weight budget class
- **Current best budget:** Gemini Flash class
- **Reason:** lepsi latency a nizsi implementation risk pri podobnem cost profilu

Tohle je cast, ktera odlisuje dashboard od jednorazove scorecard.
Neukazuje jen jedno rozhodnuti, ale i to, **co se zmenilo od minula**.

---

## Suggested operating pattern

| Role v stacku | Doporuceny model |
|---|---|
| Primary default | GPT-4.1 mini |
| Budget / speed lane | Gemini Flash class |
| Escalation lane | Claude Sonnet class |
| Cost-floor experiments | open-weight budget class |

---

## What this dashboard view is meant to answer

Za 2 minuty ma byt jasne:
1. ktery model je dnes nejlepsi default
2. jaky model drzet jako budget nebo speed variantu
3. jaky fallback ma nejmensi provozni riziko
4. co se zmenilo proti poslednimu rozhodnuti
5. jestli buyer potrebuje prubezny dashboard, nebo mu staci scorecard / memo

---

## Feedback prompt for validation

Kdybych ti poslal tenhle dashboard sample po prvnim outreachi, staci mi 3 kratke odpovedi:
1. Je tenhle dashboard view pro vas srozumitelny a uzitecny?
2. Co je pro vas cennejsi: prubezny compare dashboard, 1-page scorecard, nebo executive memo?
3. Co by musel tenhle dashboard ukazovat navic, aby mel pro vas smysl jako placeny workspace?
