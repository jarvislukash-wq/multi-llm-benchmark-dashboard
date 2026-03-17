# Target Account Shortlist — wave 1

## Purpose

Převést obecný ICP a competitor research do **prvních 15 konkrétních target accountů** pro outreach.

Nejde o finální sales list. Jde o nejpravděpodobnější firmy, kde:
- už veřejně běží AI use case
- je pravděpodobný multi-model nebo eval workflow
- model selection může mít přímý dopad na cost, latency nebo reliability

---

**Source-of-truth note:** tenhle shortlist je jen kandidátní pool pro account selection, ne finální execution routing. Pro reálný Wave 1 outreach jsou source of truth konkrétní firmy, `buyer situation`, `framing`, `CTA` a artifact v `execution/WAVE1-OUTREACH-BATCH.md` a odpovídajících personalizacích ve `execution/WAVE1A-PERSONALIZED-SKELETONS.md` / `execution/WAVE1B-PERSONALIZED-SKELETONS.md`. Pokud se shortlist a batch rozcházejí, rozhoduje batch.

## Why these accounts

### 1. Public AI maturity signal
Firmy byly vybrané z veřejných customer / AI pages, kde je vidět aktivní práce s:
- AI observability
- evals
- AI product features
- production AI workflows

### 2. Good fit for the wedge
Projekt není obecný observability tool. Hledáme týmy, které potřebují **decision layer**:
- porovnat víc modelů
- obhájit tradeoff kvalita vs cena vs latence
- mít scorecard pro konkrétní use case

### 3. Fastest validation path
Nejrychlejší signál nedá broad SMB outreach, ale týmy, které už AI řeší naplno a mají čerstvou zkušenost s model switching nebo eval-driven development.

---

## Wave 1 segments

### Segment A — AI startup / AI-native product
Nejlepší kandidáti pro rychlou validaci dashboard wedge.

| Firma | Proč sedí | Doporučený wedge |
|---|---|---|
| Magic Patterns | AI-native produkt, rychlé experimenty, pravděpodobný tlak na kvalitu vs cost | coding / product workflow scorecard |
| Graphite | AI code review, silný coding use case | coding assistant scorecard |
| Fintool | vysoký objem AI workflows, přesnost + cost pressure | reasoning / extraction dashboard |

### Segment B — SaaS s aktivní AI feature
Silné pro validaci decision dashboardu i hybridního reportu.

| Firma | Proč sedí | Doporučený wedge |
|---|---|---|
| Canva | support/help AI a productized AI workflows | support assistant scorecard |
| Khan Academy | AI learning product, kvalita odpovědí je citlivá | tutoring / response quality scorecard |
| SumUp | support + operations AI, fallback a budget tradeoff | support + fallback scorecard |
| Dropbox | AI search / retrieval, silný eval mindset | RAG / search scorecard |
| Notion | multi-surface AI product, pravděpodobně více modelů | hybrid decision dashboard |
| Coursera | AI learning features, explainability pro stakeholdery | report + dashboard hybrid |
| Zapier | AI orchestration a mnoho use case variant | dashboard for multi-model operations |
| Loom | AI-assisted video workflows, throughput + cost | high-volume workflow scorecard |
| Ramp | internal AI automation + ops ROI thinking | executive-facing model decision memo |

### Segment C — Enterprise / governance-heavy
Pomalejší sales cyklus, ale silný signál pro enterprise pricing a governance needs.

| Firma | Proč sedí | Doporučený wedge |
|---|---|---|
| Merck | governance, compliance, enterprise AI portfolio | hybrid dashboard + report |

---

## Recommended CTA by segment

### Demo CTA
Použít pro:
- Khan Academy
- Fintool
- Dropbox
- Notion
- Zapier

Důvod: vysoká pravděpodobnost, že ocení workflow a compare view.

### Scorecard CTA
Použít pro:
- Canva
- SumUp
- Graphite
- Loom
- Magic Patterns

Důvod: nižší tření, jednodušší vstup do konverzace přes konkrétní use case.

### Executive / hybrid CTA
Použít pro:
- Merck
- Coursera
- Ramp

Důvod: tady může víc fungovat governance, ROI a decision memo framing než čistý dashboard pitch.

---

## What this shortlist should answer

Po první outreach vlně chceme vědět hlavně 4 věci:
1. reagují víc AI-native startupy, nebo AI-enabled SaaS?
2. funguje líp CTA `demo`, nebo CTA `scorecard`?
3. je silnější wedge `dashboard`, `report`, nebo `hybrid`?
4. je nejbolestivější use case `coding`, `RAG/support`, nebo `high-volume extraction`?

---

## Next operational step

1. vzít 15 accountů z `DISCOVERY-TRACKER.md`
2. dohledat 1-2 konkrétní osoby per account
3. poslat první wave podle `execution/OUTREACH-PLAYBOOK.md`
4. po odpovědích přepsat hypotézy v trackeru na reálné signály
