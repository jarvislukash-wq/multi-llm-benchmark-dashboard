# Smoke Test Landing Page — multi-llm-benchmark-dashboard

## Goal

Připravit jednoduchou 1stránkovou landing page pro první validační sprint.

Primární úkol stránky není "prodat produkt". Má ověřit 3 věci:
1. jestli messaging varianty **B** rezonuje s primárním ICP
2. jestli lidi chtějí vidět demo / scorecards / early access
3. jestli problém působí dost urgentně na rezervaci callu nebo zanechání kontaktu

---

## Primary audience

- AI startup CTO
- Applied AI lead
- Engineering lead řešící 3+ modelů
- AI agentura founder / delivery lead

---

## Recommended page structure

1. Hero
2. Problem snapshot
3. 3 use-case scorecards preview
4. Why existing tools are not enough
5. CTA form
6. FAQ / objections
7. Final CTA

---

## Full page copy

### Hero

**Eyebrow**
For teams choosing between GPT, Claude, Gemini and other LLMs

**Headline**
Porovnej LLM modely podle reálného use case, ne podle hype.

**Subheadline**
Decision dashboard pro týmy, které potřebují obhájit nejlepší model podle kvality, ceny, latence a fallback strategie.

**Primary CTA**
Rezervovat demo

**Secondary CTA**
Poslat ukázkové scorecards

**Microcopy under CTA**
Pro týmy, které aktivně testují 3+ modelů nebo providerů.

---

### Problem section

**Section headline**
Problém není nedostatek benchmarků. Problém je roztříštěné rozhodování.

**Body copy**
Benchmark leaderboard je na jednom webu. Pricing na stránkách providerů. Latence v observability nástroji. Vlastní evaly v notebooku, CI nebo interním dashboardu.

Výsledek:
- výběr modelu se opakuje od nuly
- těžko se vysvětluje, proč vyhrál právě tenhle model
- fallback a budget varianta se řeší pozdě
- po každém novém release se decision workflow rozpadne znovu

---

### Solution section

**Section headline**
Jedna scorecard pro každé důležité rozhodnutí o modelu.

**Body copy**
Multi-LLM Benchmark Dashboard spojuje veřejné benchmarky, pricing a interní eval signály do jednoho compare workflow.

Pro každý use case ukáže:
- best overall
- best budget pick
- best speed pick
- safest fallback
- strongest coding / reasoning option

---

### Use-case scorecards preview

#### 1. RAG support assistant
**What matters:** groundedness, latency, cena za konverzaci, hallucination risk

#### 2. AI coding assistant
**What matters:** code task quality, tool-use fit, long-context reliability, price per workflow

#### 3. High-volume extraction
**What matters:** cost per successful task, schema adherence, throughput, multilingual reliability

**Section microcopy**
Každý tým má jiné priority. Proto nestačí jeden globální rank.

---

### Why not existing tools

**Section headline**
Proč nestačí leaderboard nebo observability tool

| Varianta | Co dává | Co chybí |
|---|---|---|
| Public leaderboard | rychlý přehled trhu | neodpoví, co je nejlepší pro tvůj use case |
| Observability tool | interní cost/latency data | chybí širší compare a externí benchmark kontext |
| Ruční spreadsheet | flexibilita | neškáluje, rychle zastarává |

**Bridge statement**
Tady vzniká decision layer mezi veřejným benchmarkem a interní realitou týmu.

---

### CTA form

**Form headline**
Chceš rychleji rozhodnout, který model nasadit?

**Fields**
- Work email
- Role
- Company
- Team size
- Main AI use case
- Kolik modelů dnes aktivně testujete? (1-2 / 3-5 / 6+)
- Co chceš vidět? (demo / scorecards / early access)

**Primary button**
Chci demo / scorecards

**Qualification note**
Prioritně bereme týmy, které aktivně porovnávají 3+ modelů nebo providerů.

---

### FAQ / objections

#### Nestačí nám Artificial Analysis nebo LMArena?
Jsou skvělé pro veřejný přehled. Neřeší ale rozhodnutí podle konkrétního use case ani propojení s interními evaly a produkční realitou.

#### To už přece umí Langfuse / Helicone.
Tyhle nástroje dobře řeší observability a tracing. Tohle je decision dashboard pro model selection, ne další trace viewer.

#### Co když ještě nemáme interní eval data?
První hodnota může vzniknout už nad veřejnými benchmarky, pricingem a use-case scorecards. Interní data jen zvyšují přesnost doporučení.

#### Je to dashboard, report nebo API?
To právě validujeme. Landing page má zjistit, který formát kupující chtějí nejdřív.

---

### Final CTA

**Headline**
Přestaň vybírat LLM modely podle dojmu.

**Subheadline**
Pošli svůj use case a ukažeme ti, jak by vypadala scorecard pro tvoje rozhodnutí.

**Button**
Chci ukázkovou scorecard

---

## Event tracking plan

### Must-track events
- page_view
- hero_primary_cta_click
- hero_secondary_cta_click
- scorecard_section_view
- form_start
- form_submit
- selected_intent_demo
- selected_intent_scorecards
- selected_intent_early_access

### Success snapshot for first pass
- 50+ relevant visits
- 10 %+ CTA click rate
- 5 %+ form submit rate
- 3+ kvalifikované leady z prvních návštěv

---

## Smoke test checklist

- [ ] publish as simple no-code page or static page
- [ ] connect form to lightweight collection flow
- [ ] send first traffic from direct outreach
- [ ] tag replies by ICP segment
- [ ] compare demo CTA vs scorecards CTA
- [ ] review objections after first 10 conversations

---

## Recommended decision after first 2 weeks

### Keep pushing current page if
- CTA konverze je zdravá
- leady odpovídají na use-case framing
- lidi chápou rozdíl proti leaderboards / observability tools

### Adjust messaging if
- response je jen na "benchmark" ale ne na "decision dashboard"
- většina leadů chce spíš report nebo audit než produkt
- lidé bez interních evalů nevnímají hodnotu

### Narrow wedge if
- nejlépe reaguje jen jeden use case nebo jeden segment
- typicky coding assistant nebo AI agentury
