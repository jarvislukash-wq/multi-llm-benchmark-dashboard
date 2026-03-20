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

## Framing variants to test

Landing page už nemá testovat jen CTA `demo` vs `scorecards`, ale i hlavní mentální model produktu.

### Variant D — decision dashboard
- **Headline:** Vyber správný LLM model rychleji než ve spreadsheetu, leaderboardu a observability toolu dohromady.
- **Subheadline:** Decision dashboard pro týmy, které potřebují porovnat kvalitu, cenu, latenci a fallback podle konkrétního use case.
- **Primary CTA:** Rezervovat demo

### Variant S — use-case scorecard
- **Headline:** Získej jasné srovnání modelů pro svůj use case bez dalšího benchmark chaosu.
- **Subheadline:** Use-case scorecards ukážou best overall, best budget a safest fallback pro konkrétní workflow.
- **Primary CTA:** Poslat ukázkové scorecards

### Variant M — decision memo / executive hybrid
- **Headline:** Obhaj výběr LLM modelu před týmem i managementem.
- **Subheadline:** Lehký decision layer, který spojí veřejné benchmarky, pricing a interní eval signály do obhajitelného doporučení.
- **Primary CTA:** Poslat decision memo

### Recommended test order
1. AI startup / engineering traffic: testovat `D` vs `S`
2. Enterprise / governance traffic: testovat `M` vs `D`
3. Nesrovnávat všechny 3 varianty najednou na malém trafficu

---

## Source-of-truth note

Tento dokument je vychozi source of truth pro landing page framing varianty (`D`, `S`, `M`), jejich doporuceny test order a defaultni CTA mapovani pro smoke test. Buyer situace a positioning logika se odvozuji z buyer decision matrix v `ENRICHMENT.md`; `execution/MESSAGING-FRAMING-TEST.md` muze doplnit experimentni hypotézy, ale nema prepisovat nazvy framingu ani vychozi CTA bez vedome upravy tohoto dokumentu.

## Buyer-situation routing for landing variants

Aby landing test navazoval na buyer decision matrix v `ENRICHMENT.md`, pouzij pro traffic a outreach tento jednoduchy routing:

| Buyer situace | Nejvhodnejsi landing framing | Proc | Doporuceny CTA |
|---|---|---|---|
| Tym rychle porovnava modely pro novy use case | Variant S - use-case scorecard | nejrychleji ukaze konkretni rozhodnuti bez tezkeho setupu | Poslat ukazkove scorecards |
| Tym uz ma evaly nebo traces, ale chybi finalni rozhodnuti | Variant D - decision dashboard | lepe sedi na opakovane compare workflow a decision layer | Rezervovat demo |
| Buyer potrebuje obhajit volbu modelu pred managementem nebo klientem | Variant M - decision memo | nejsilnejsi governance a explainability angle | Poslat decision memo |
| Buyer resi rozpoctovy strop a fallback model | Variant S - use-case scorecard | scorecard nejlip ukaze best budget a safest fallback vedle sebe | Poslat ukazkove scorecards |
| Buyer hleda lightweight nastroj pred plnym LLMOps stackem | Variant S -> az pak D | nizkotrieni vstup pres scorecard, dashboard az po potvrzeni zajmu | Poslat ukazkove scorecards |

Prakticke pravidlo: kdyz si nejsi jisty, zacni `S`. `D` pouzij az tam, kde buyer uz premysli v opakovanem team workflow. `M` posilej jen tam, kde je zjevny executive, governance nebo client-facing angle.

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

### Hidden status-quo competitors

**Section headline**
Ve skutečnosti nesoutěžíš jen s benchmark nástroji

V prvním nákupním momentu tenhle produkt často nesoutěží s jiným SaaS. Soutěží s tím, co tým používá už dnes:

| Status quo alternativa | Proč ji tým drží | Kde selhává | Co musí landing page slíbit |
|---|---|---|---|
| Spreadsheet / Notion tabulka | nulové pořizovací náklady, rychlý start | ruční compare rychle zastará a nejde dobře sdílet | rychlejší první rozhodnutí než ruční compare |
| Slides / interní memo | snadno se pošle managementu nebo klientovi | při každé změně modelu nebo ceny se přepisuje od nuly | sdílitelný výstup bez ručního přepisování do slidů |
| Provider-native playground / dashboard | tým už je uvnitř konkrétního providera | neukáže férový cross-vendor tradeoff ani fallback variantu | opakovatelný refresh po změně modelu nebo ceny |

**Decision implication**
Jestli landing page neukáže rychlost prvního rozhodnutí, sdílitelný výstup a opakovatelný refresh, buyer zůstane u status quo i bez nákupu dalšího nástroje.

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

#### Je to decision dashboard, scorecard nebo decision memo?
To právě validujeme. Landing page má zjistit, který framing kupující chtějí vidět nejdřív.

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
- selected_framing_dashboard
- selected_framing_scorecard
- selected_framing_memo

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
