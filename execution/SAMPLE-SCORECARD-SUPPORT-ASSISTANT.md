# Sample Scorecard — Customer Support Assistant

## Purpose

Toto je **sendable sample artifact** pro validační outreach.

Je schválně krátký a čitelný pro 2 publika najednou:
- AI / engineering lead
- product nebo operations owner

> Pozn.: skóre a čísla níže jsou **illustrative sample format**, ne live benchmark pull. Cíl je ověřit, jestli je tenhle výstup pro tým užitečný.

---

## Use case

**Use case:** customer support assistant pro SaaS

### Co tým typicky řeší
- kvalita odpovědí na FAQ + account otázky
- rozumná cena při větším objemu ticketů
- nízká latence v live chatu
- bezpečný fallback při výpadku nebo zdražení primárního modelu

---

## Decision weights

| Faktor | Váha |
|---|---:|
| Quality / answer usefulness | 35% |
| Cost per production volume | 25% |
| Latency / responsiveness | 20% |
| Fallback readiness | 10% |
| Implementation risk | 10% |

---

## Shortlist snapshot

| Model | Quality | Cost-efficiency | Latency | Fallback fit | Overall sample score | Best role |
|---|---:|---:|---:|---:|---:|---|
| GPT-4.1 mini | 8.5 | 7.5 | 8.0 | 8.0 | **8.1** | balanced primary |
| Claude Sonnet class | 9.0 | 6.0 | 7.0 | 7.5 | **7.7** | high-quality escalation |
| Gemini Flash class | 7.5 | 8.5 | 9.0 | 8.0 | **8.1** | speed / budget-heavy flows |
| Open-weight budget class | 6.5 | 9.0 | 8.0 | 6.5 | **7.5** | cost floor / internal batch work |

---

## Recommendation view

### 1) Best overall
**GPT-4.1 mini**
- nejvyváženější kombinace kvality, ceny a latence
- vhodné jako default pro většinu support dotazů
- nejsnazší start pro tým, který chce rychlé rozhodnutí bez složité orchestrace

### 2) Best budget / speed pick
**Gemini Flash class**
- dává smysl tam, kde je důležitá rychlost a vysoký objem
- dobrý kandidát pro první draft odpovědi nebo low-risk support flows
- tradeoff: může chtít víc guardrailů u složitějších dotazů

### 3) Best quality escalation lane
**Claude Sonnet class**
- vhodné pro složité nebo citlivější konverzace
- dobrý jako druhá vrstva pro escalation path
- tradeoff: horší economics jako plošný default

### 4) Best cost floor
**Open-weight budget class**
- zajímavé pro interní summarization, tagging nebo batch enrichment
- méně vhodné jako jediný customer-facing default bez silných eval guardrailů

---

## Suggested deployment pattern

### Lean rollout
- **Primary:** GPT-4.1 mini
- **Fallback:** Gemini Flash class
- **Escalation:** Claude Sonnet class

Proč:
- jednoduché na vysvětlení i rollout
- pokrývá quality + speed + fallback
- nevyžaduje složitý routing hned v první fázi

---

## What changes the recommendation

Doporučení se rychle změní, pokud:
1. support workload je hlavně krátký FAQ chat a ne knowledge-heavy řešení
2. cena má vyšší prioritu než quality
3. tým už má vlastní eval set a ví, že konkrétní provider sedí líp na jejich tone / policy požadavky
4. governance nebo data residency omezuje provider choice

---

## What this artifact is meant to answer

Za 2 minuty má být jasné:
- který model nasadit jako default
- který držet jako fallback
- kde je největší tradeoff kvalita vs cena vs rychlost
- jestli tým spíš potřebuje **dashboard**, **scorecard**, nebo **decision memo** format

---

## Feedback prompt for validation

Kdybych ti tohle poslal po prvním outreachi, stačí mi 3 krátké odpovědi:
1. Je tenhle formát pro váš tým užitečný, nebo ne?
2. Chybí ti víc dashboard view, nebo naopak stačí 1-page scorecard?
3. Za co bys platil spíš: live compare dashboard, pravidelné scorecards, nebo executive memo export?
