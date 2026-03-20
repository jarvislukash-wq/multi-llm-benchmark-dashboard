# Messaging Framing Test — multi-llm-benchmark-dashboard

## Goal

Ověřit, který framing nejlépe otevírá konverzaci a vede ke kvalifikovanému zájmu:
- **decision dashboard**
- **use-case scorecard**
- **decision memo / executive hybrid**

Nejde o finální branding. Jde o rychlý test, jaký mentální model buyer chápe nejrychleji.

---

**Source-of-truth note:** tenhle framing test slouží pro hypotézy a vyhodnocení, ne jako samostatný routing dokument. Pro reálný Wave 1 outreach se `framing`, `CTA` a posílaný artefakt přebírají bez reinterpretace z `execution/WAVE1-OUTREACH-BATCH.md` a odpovídajících personalizací ve `execution/WAVE1A-PERSONALIZED-SKELETONS.md` / `execution/WAVE1B-PERSONALIZED-SKELETONS.md`.
Stejně tak tenhle dokument neslouží ke změně `buyer situation`; ta zůstává source-of-truth v trackeru a navazujících Wave 1 execution artefaktech.

## The 3 framings

| Framing | Short promise | Best fit | Main risk |
|---|---|---|---|
| Decision dashboard | jedno místo pro výběr modelu podle kvality, ceny, latence a fallbacku | AI startupy, engineering-heavy týmy | může znít jako další analytics tool |
| Use-case scorecard | rychlé srovnání modelů pro konkrétní use case | vytížení operátoři, consultative sale, agentury | může znít moc staticky / jednorázově |
| Decision memo / executive hybrid | obhajitelný výběr modelu pro tým a management | governance, enterprise, cost owners | může vypadat spíš jako služba než SaaS |

---

## Working hypotheses

### H1 — decision dashboard
Nejlépe zafunguje u týmů, které už mají interní evaly nebo aktivně porovnávají více modelů.

**Signal, že funguje:**
- lead chce demo nebo live compare view
- ptá se na weights, alerts, historical compare
- zajímá ho dashboard / workspace formát

### H2 — use-case scorecard
Nejlépe zafunguje jako low-friction vstup u leadů, kteří nechtějí call bez konkrétního artefaktu.

**Signal, že funguje:**
- lead chce poslat sample output
- reaguje na konkrétní use case
- ptá se na report/share/export místo plné platformy

### H3 — decision memo / executive hybrid
Nejlépe zafunguje tam, kde je důležitá explainability, governance a cost justification.

**Signal, že funguje:**
- lead chce executive summary
- řeší approval proces nebo vendor governance
- zajímá ho hybrid report + dashboard

---

## Suggested segment mapping

| Segment | Primary framing | Secondary framing | Avoid as first touch |
|---|---|---|---|
| AI startup CTO / applied AI lead | decision dashboard | use-case scorecard | executive memo |
| AI agentura founder / delivery lead | use-case scorecard | decision dashboard | pure executive memo |
| SaaS engineering lead | decision dashboard | use-case scorecard | executive memo |
| Enterprise AI / governance owner | decision memo / executive hybrid | decision dashboard | pure scorecard-only pitch |

---

## Copy angles to test

### A. Decision dashboard
**Headline angle:**
Vyber správný LLM model rychleji než ve spreadsheetu, leaderboardu a observability toolu dohromady.

**1-line explanation:**
Jedno compare workflow pro kvalitu, cenu, latenci a fallback podle konkrétního use case.

**Primary CTA:**
Rezervovat demo

### B. Use-case scorecard
**Headline angle:**
Získej jasné srovnání modelů pro svůj use case bez dalšího benchmark chaosu.

**1-line explanation:**
Scorecard ukáže best overall, best budget a safest fallback pro konkrétní workflow.

**Primary CTA:**
Poslat ukázkovou scorecard

### C. Decision memo / executive hybrid
**Headline angle:**
Obhaj výběr LLM modelu před týmem i managementem.

**1-line explanation:**
Lehký decision layer mezi veřejnými benchmarky, interními evaly a business rozhodnutím.

**Primary CTA:**
Poslat decision memo

---

## Measurement plan

### Per lead / conversation track
- segment
- framing sent
- CTA used
- response type: none / reply / call / sample request
- preferred framing: dashboard / scorecard / memo / hybrid
- strongest objection
- exact phrase they used pro hodnotu

### Per landing page variant track
- hero framing variant
- CTA click rate
- form submit rate
- selected intent
- share of qualified leads (3+ models / real decision owner)

---

## Minimum success bar

Po první vlně chceme vidět aspoň:
- **5+ odpovědí** napříč framingy
- **3+ kvalifikované reakce**, kde lead explicitně potvrdí problém
- **1 zřetelně silnější framing** podle reply quality, ne jen počtu odpovědí

### Strong signal
- decision dashboard vyhrává, pokud lidi chtějí workflow / compare / alerts
- scorecard vyhrává, pokud sample artefakt otevírá většinu callů
- memo/hybrid vyhrává, pokud enterprise leady chtějí obhajobu a interní alignment

---

## Recommended test order

### Wave 1
- AI startup / SaaS engineering: **dashboard vs scorecard**
- enterprise / governance: **memo vs dashboard**

### Wave 2
- držet vítězný framing pro dominantní segment
- u runner-up framingu ověřit, jestli není silný jen pro jiný ICP

---

## Interview prompts tied to framing

### If dashboard framing was sent
- Chybí vám dnes spíš compare workflow, nebo data samotná?
- Chtěl bys to řešit jako dashboard, nebo spíš export/report?

### If scorecard framing was sent
- Je pro tebe scorecard užitečný artefakt, nebo je to jen vstup do deeper workflow?
- Chtěl bys scorecard jednorázově, nebo průběžně aktualizovanou?

### If memo framing was sent
- Potřebujete spíš recommendation pro management, nebo operativní nástroj pro tým?
- Kdo musí u vás model choice schválit nebo obhájit?

---

## Decision after first validation pass

Po prvních odpovědích rozhodnout 3 věci:
1. který framing otevírá nejvíc kvalitních rozhovorů
2. který segment reaguje s nejvyšší bolestí
3. jestli první produkt má být **dashboard-first**, **scorecard-first** nebo **hybrid dashboard + memo**
