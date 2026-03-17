# Sample Decision Memo — Customer Support Assistant

## Purpose

Toto je **sendable sample artifact** pro executive / governance validation.

Není to live benchmark report. Je to ukázka formátu, který má během 2 minut odpovědět:
- jaký model nasadit jako default
- jaký držet jako fallback
- kde je hlavní tradeoff kvalita vs cena vs rychlost
- jestli by tým chtěl spíš memo, scorecard nebo dashboard

---

## Decision to make

**Jaký model stack zvolit pro customer support assistant v SaaS produktu?**

Rozhodnutí se týká hlavně 3 věcí:
1. kvalita odpovědi u FAQ + account dotazů
2. economics při vyšším objemu ticketů
3. bezpečný fallback při výpadku, změně ceny nebo poklesu kvality

---

## Recommendation

### Recommended operating setup
- **Primary default:** GPT-4.1 mini
- **Fallback path:** Gemini Flash class
- **Escalation lane:** Claude Sonnet class

### Why this setup
- GPT-4.1 mini dává nejlepší celkový kompromis mezi kvalitou, cenou a jednoduchostí rolloutu
- Gemini Flash class zlepšuje economics a rychlost pro high-volume flows
- Claude Sonnet class dává smysl pro složitější nebo citlivější konverzace, kde je vyšší tolerance na cenu

---

## Executive summary

### What this recommendation optimizes for
- rychlý start bez složité orchestrace
- rozumný cost envelope pro běžný support provoz
- jasně vysvětlitelný fallback model pro risk management

### What it avoids
- nasazení nejdražšího modelu jako plošného defaultu
- vendor lock-in bez připravené alternativy
- decision by hype místo decision by use case

---

## Tradeoff summary

| Option | Strength | Main tradeoff |
|---|---|---|
| GPT-4.1 mini as primary | nejlepší balance pro většinu support dotazů | nemusí být nejlevnější při extrémním objemu |
| Gemini Flash class as primary | rychlost a nízká cena | může chtít víc guardrailů u složitějších dotazů |
| Claude Sonnet class as primary | vyšší kvalita u těžších konverzací | slabší economics pro default path |
| Open-weight budget class as primary | nejnižší cost floor | vyšší implementation a quality risk |

---

## When this recommendation changes

Tahle volba se má přepočítat, pokud:
1. support workload je hlavně krátký FAQ chat s minimem edge cases
2. cost target je tvrdší než quality target
3. governance nebo data residency omezuje provider choice
4. tým má vlastní eval set, který ukáže jiný winner pro tone, policy nebo hallucination rate

---

## Suggested rollout logic

### Phase 1
- spustit GPT-4.1 mini jako primary
- držet Gemini Flash jako fallback
- Claude používat jen pro escalation / high-value cases

### Phase 2
- změřit ticket resolution quality, cost per conversation a escalation rate
- podle výsledků rozhodnout, jestli má smysl víc trafficu přesunout do budget lane

---

## Validation question

Když bys dostal takovéhle memo po prvním outreachi, co je pro tebe cennější?
1. stačí ti tenhle 1-page memo format
2. chceš radši scorecard s explicitním srovnáním modelů
3. potřebuješ spíš živý dashboard s průběžně aktualizovaným compare view
