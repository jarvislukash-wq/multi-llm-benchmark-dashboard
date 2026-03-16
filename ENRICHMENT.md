# Enrichment — multi-llm-benchmark-dashboard

## 1. Executive summary

Trh už má silné hráče na benchmark data, eval tooling i observability. Chybí ale jednoduchý produkt, který z toho udělá **rozhodovací systém pro výběr modelu**. To je hlavní mezera.

Nejlepší wedge:
- nezačínat jako full LLMOps platforma
- začít jako **decision dashboard** pro malé a střední AI týmy
- rychle dodat jasnou odpověď: **který model vybrat pro konkrétní use case**

## 2. Competitor matrix

| Segment | Hráči | Co dělají dobře | Kde je mezera |
|---|---|---|---|
| Public benchmark intelligence | Artificial Analysis, LMArena, OpenRouter Rankings | data, důvěra, traffic | chybí interní rozhodovací workflow a team collaboration |
| Evals / quality | Braintrust, Confident AI, Promptfoo, Evidently | evaluace kvality, regression testing | slabší executive compare layer a business recommendation |
| Observability / tracing | Langfuse, Helicone, W&B Weave | trace, latency, cost, monitoring | neřeší výběr model portfolio a external benchmark merge |
| Gateway / routing | Portkey | routing, governance, gateway | operativa, ne pre-purchase / pre-adoption decision layer |

## 3. Where the product wins

### Unique value proposition
„Nejrychlejší cesta od chaosu v modelech k obhajitelnému rozhodnutí.“

### 3 klíčové diferenciátory
1. **Use-case scoring** místo globálního ranku
2. **Mix veřejných a interních dat**
3. **Doporučení pro business rozhodnutí**, ne jen raw grafy

## 4. ICP pain points

### AI startup founder / CTO
- tým testuje více modelů, ale rozhodnutí je subjektivní
- management chce zdůvodnit cost/quality tradeoff
- po každém novém model release se rozhodování restartuje

### AI engineer / applied AI lead
- benchmarky jsou rozeseté po webu
- interní evaly žijí v notebooku, CI nebo různých nástrojích
- těžko se vysvětluje, proč zrovna tenhle model vyhrál

### AI consultant / agency
- potřebuje obhájit model stack klientovi
- chce srovnávat řešení pro různé use casy
- ocení shareable report a klientský dashboard

## 5. Pricing hypothesis

### Pricing logic
Produkt šetří hlavně:
- čas seniorních lidí při model selection
- cost overruns ze špatné volby modelu
- churn v experimentování bez evidence

### Doporučené pricing pásmo
- **€39 Starter**: low-friction vstup, solo / indie / malý tým
- **€149 Pro**: hlavní sweet spot pro startupy
- **€399 Team**: pro agentury a multi-user týmy
- **Enterprise custom**: governance, SSO, self-hosted

### Co musí Pro tier umět, aby dával smysl
- custom weighting per use case
- import interních eval výsledků
- alerts na změny price/performance
- export decision memo / report

## 6. Revenue expansion paths

1. benchmark API
2. paid research briefs / quarterly market reports
3. enterprise vendor governance module
4. procurement / routing recommendation integrations

## 7. Validation questions

### Problem interviews
1. Jak dnes vybíráte model pro nový use case?
2. Které metriky jsou při výběru nejdůležitější?
3. Kde dnes berete benchmark data?
4. Jak často měníte model kvůli ceně nebo kvalitě?
5. Co je na tom procesu nejvíc otravné nebo drahé?

### Pricing / value interviews
1. Jak drahá je špatná volba modelu ve vašem týmu?
2. Zaplatili byste za dashboard, který spojí benchmarky, cenu a vaše evaly?
3. Co by pro vás muselo být uvnitř, aby to mělo hodnotu €149/měs?
4. Chtěli byste spíš SaaS, nebo exportovatelný report / API?

## 8. Recommended next milestone

Enrichment milestone bude prakticky splněný po doplnění:
1. 10-15 customer interview target listu
2. landing page copy / messaging testu
3. mocku prvních 3 use-case scorecards

## 9. Sources used in this pass

- Artificial Analysis
- LMArena
- OpenRouter Rankings
- Braintrust
- Portkey
- Confident AI
- Helicone
- Langfuse
- Promptfoo
- Evidently AI
- W&B Weave

## 10. Verdict

Projekt má smysl hlavně tehdy, pokud zůstane úzce vymezený:
**decision intelligence pro výběr LLM**, ne další široká LLMOps platforma.

To je realistická wedge i lepší cesta k monetizaci.

## 11. Validation assets created

Navazující validační balík je v `VALIDATION-ASSETS.md` a obsahuje:
- 12 prioritizovaných interview target profilů
- landing page messaging varianty
- 3 ukázkové use-case scorecards
- seznam předpokladů a rychlých experimentů pro další krok

Tím je enrichment dokumentace dostatečně konkrétní pro přechod do externí validace.
