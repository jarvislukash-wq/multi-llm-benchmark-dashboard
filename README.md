# multi-llm-benchmark-dashboard

Created on 2026-03-12
Type: commercial
Phase: enrichment

## Idea

Dashboard pro týmy, které porovnávají více LLM modelů napříč benchmarky, cenou, latencí a reálným provozem. Cíl není jen ukazovat veřejné leaderboardy, ale dát produktovým a AI engineering týmům jedno místo pro rozhodnutí: **který model nasadit pro konkrétní use case a proč**.

## Problem

Dnes jsou data rozbitá mezi několik zdrojů:
- veřejné benchmark leaderboardy
- provider pricing pages
- API usage a latency interně v týmu
- eval výsledky z CI / experimentů

Výsledek:
- těžké porovnání modelů podle konkrétního use case
- rozhodování podle dojmu nebo Twitter hype
- drahé přepínání modelů bez jasného ROI

## Target customer / ICP

### Primární ICP
- AI startupy a product týmy s 2-20 vývojáři
- staví chatboty, copilots, agenty, RAG workflow nebo coding assistants
- používají 3+ modelů / providerů
- řeší tradeoff: kvalita vs cena vs latence

### Sekundární ICP
- AI konzultanti a agentury
- enterprise innovation týmy
- open-source benchmark maintainers / research teams

## Market landscape

### Přímé a blízké alternativy

| Produkt | Co řeší | Silná stránka | Slabina vůči tomuto nápadu |
|---|---|---|---|
| Artificial Analysis | veřejné benchmarky, cena, rychlost | důvěryhodné nezávislé leaderboardy | chybí workflow pro interní rozhodování týmu a vlastní eval data |
| LMArena | crowd preference ranking | silný brand a community signal | neřeší enterprise náklady, observability ani interní benchmarky |
| OpenRouter Rankings | usage-based popularita modelů | reálná usage data trhu | popularity != fitness pro konkrétní produkt |
| Braintrust | evals + tracing + observability | silné napojení na produkční kvalitu | není to market-facing benchmark cockpit napříč veřejnými + interními zdroji |
| Langfuse | tracing, evals, prompt management | open-source a oblíbené u AI engineering týmů | fokus je observability, ne benchmark intelligence layer |
| W&B Weave | traces, evals, monitoring | silný dev ecosystem | širší platforma, slabší jednoduchý executive compare use case |
| Confident AI | evals, observability, red teaming | quality workflow | více QA/evals než business rozhodování o model portfolio |
| Portkey / Helicone | gateway + observability + routing | provozní data, cost control | neřeší benchmark intelligence v dashboard-first podobě |
| Promptfoo / Evidently | testování, evals, bezpečnost | kvalitní eval tooling | spíš framework / testing vrstva než decision dashboard |

### Co z trhu plyne

1. **Leaderboardy existují**, ale jsou hlavně veřejné a generické.
2. **Observability nástroje existují**, ale soustředí se na trace/debugging, ne na výběr modelu pro business rozhodnutí.
3. **Mezera je v decision layeru**: spojit veřejné benchmarky, ceníky, interní evaly a produkční usage do jedné scorecard.

## Positioning

### Jednou větou
**„Jeden cockpit pro výběr správného LLM modelu podle kvality, ceny, latence a fitu pro konkrétní use case.“**

### Co to není
- není to další obecný observability stack
- není to jen další leaderboard mirror
- není to pure eval framework pro vývojáře

### Co to je
- decision dashboard pro AI product / engineering leady
- bridge mezi veřejným benchmark světem a interní realitou týmu

## Competitive advantages

1. **Use-case scorecards místo obecných leaderboards**  
   Např. support bot, coding assistant, extraction, RAG QA.

2. **Spojení veřejných + interních dat**  
   Artificial Analysis / LMArena / OpenRouter + vlastní evals + production telemetry.

3. **Business-ready rozhodnutí**  
   „Best quality“, „best cost-performance“, „safe fallback“, „EU budget pick“.

4. **Executive + engineering view v jednom**  
   CTO vidí náklady a riziko, AI engineer vidí benchmark detail a experiment historii.

5. **Vendor-neutral positioning**  
   Narozdíl od provider-specific dashboardů má produkt motivaci porovnávat férově.

## Revenue model hypothesis

### SaaS tiers

| Tier | Cena | Pro koho | Co obsahuje |
|---|---:|---|---|
| Starter | €39/měs | solo builder / malý tým | 3 use-case scorecards, 5 model watchlists, weekly refresh |
| Pro | €149/měs | AI startup tým | custom weights, interní eval import, alerts, team workspace |
| Team | €399/měs | větší AI tým / agentura | více workspace, role, API, historical comparison |
| Enterprise | custom | enterprise | SSO, self-hosted, private connectors, SLA |

### Další monetizace
- placené benchmark snapshots / reports
- consulting onboarding pro model governance
- API access pro interní procurement nebo routing tools
- white-label benchmark portal pro agentury / consultancies

## Demand signals

- Artificial Analysis ukazuje silnou poptávku po nezávislém srovnání modelů.
- OpenRouter Rankings potvrzuje, že trh aktivně porovnává modely podle usage, ne jen podle marketingu.
- Braintrust, Langfuse, Confident AI a W&B dokazují, že firmy už platí za eval/observability vrstvu.
- Rychlé tempo releasů modelů zvyšuje decision fatigue: leaderboard z minulého měsíce často nestačí.
- AI týmy potřebují obhájit volbu modelu před managementem: kvalita, cena, fallback, vendor risk.

## Risks

1. veřejná benchmark data jsou částečně komodita
2. některé platformy můžou přidat compare dashboardy samy
3. bez interních dat importů je produkt snadno kopírovatelný
4. maintenance cost benchmark zdrojů může růst

## Recommended MVP

### MVP scope
1. Import 3 veřejných zdrojů:
   - Artificial Analysis
   - OpenRouter rankings
   - jeden community signal source / manual ingest
2. Normalizovaný model catalog
3. Compare dashboard pro 10-20 nejrelevantnějších modelů
4. Váhy podle use case:
   - quality
   - price
   - latency
   - context window
   - tool use / coding fit
5. Jednoduché recommendation views:
   - best overall
   - best budget
   - best speed
   - best coding
   - best fallback
6. Export shareable decision reportu

### MVP wedge
Začít bez těžké observability integrace. Nejdřív vyřešit **„jak si rychle vybrat model“**, teprve potom přidat interní trace/eval connectors.

## Go-to-market hypothesis

### Nejpravděpodobnější první kanály
- content / SEO na long-tail dotazy typu „best LLM for RAG“, „Claude vs Gemini vs GPT cost quality"
- LinkedIn / X publikované benchmark breakdowny
- free interactive compare page jako acquisition funnel
- outreach na AI startup founders a AI engineers

### Fast validation plan
1. udělat landing page s 3 use-case scorecards
2. oslovit 15-20 AI týmů a zjistit, jak dnes volí modely
3. ověřit willingness to pay za:
   - interní compare workspace
   - alerts při změně rankings / pricing
   - export pro decision review

## Concrete next step

Další konkrétní krok po dokončeném enrichment základu:
**spustit 10-15 customer discovery rozhovorů a landing page smoke test nad validačním balíkem ve `VALIDATION-ASSETS.md`.**

Praktický execution podklad je teď připravený v:
- `VALIDATION-RUNBOOK.md` — 14denní plán, success thresholds a decision tree
- `DISCOVERY-TRACKER.md` — šablona pro interview a smoke test evidenci
- `execution/SMOKE-TEST-LANDING-PAGE.md` — kompletní 1stránková landing page copy, event tracking a smoke-test checklist
- `execution/OUTREACH-PLAYBOOK.md` — první outreach vlna pro 15 leadů, segmentové message templates a follow-up cadence
- `execution/TARGET-ACCOUNT-SHORTLIST.md` — konkrétní wave 1 account shortlist a CTA doporučení pro outreach
- `execution/WAVE1-OUTREACH-BATCH.md` — ready-to-send wave 1 batch rozdělený na demo / scorecard / executive-hybrid CTA
- `COMPETITOR-TEARDOWN.md` — konkrétní competitor read a positioning wedge proti Artificial Analysis / Braintrust / Langfuse / Helicone / OpenRouter
