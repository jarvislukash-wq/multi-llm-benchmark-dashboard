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
- **€149 Pro**: hlavní pricing hypotéza pro startupy (čeká na live willingness-to-pay potvrzení)
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
3. Co by pro vás muselo být uvnitř, aby to pro vás mělo hodnotu v pásmu kolem €149/měs?
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

## 10.1 Competitor teardown addendum

Detailní competitor teardown z veřejného positioning textu je nově v `COMPETITOR-TEARDOWN.md`.

Hlavní závěr z tohoto passu:
- nesoutěžit na čistém leaderboardu ani observability šířce
- držet wedge jako **decision layer** nad benchmarky, pricingem a interními signály
- první placenou hodnotu balit jako **scorecard / decision workspace**, ne jako těžkou LLMOps platformu

Nejrelevantnější referenční hráči pro positioning v tomto passu:
- Artificial Analysis — public benchmark intelligence
- Braintrust — observability + eval maturity
- Langfuse — open-source LLM engineering platform
- Helicone — gateway + observability
- OpenRouter Rankings — usage/popularity signal

## 11. Validation assets created

Navazující validační balík je v `VALIDATION-ASSETS.md` a obsahuje:
- 12 prioritizovaných interview target profilů
- landing page messaging varianty
- 3 ukázkové use-case scorecards
- seznam předpokladů a rychlých experimentů pro další krok

Tím je enrichment dokumentace dostatečně konkrétní pro přechod do externí validace.

Navazující execution vrstva je rozepsaná v `VALIDATION-RUNBOOK.md` (14denní plán, success thresholds, decision tree) a `DISCOVERY-TRACKER.md` (šablona evidence interview a landing page testu).


## 13. Buyer decision matrix vs alternatives

Malý doplněk k positioning wedge: buyer nepotřebuje jen vědět, že existuje mezera na trhu. Potřebuje být zřejmé, **kdy sáhne po tomto produktu místo existujících alternativ**.

| Buyer situace | Co dnes typicky použije | Proč to nestačí | Proč vyhraje multi-llm-benchmark-dashboard |
|---|---|---|---|
| Chci rychle porovnat modely pro nový use case | Artificial Analysis / OpenRouter / vlastní spreadsheet | veřejná data nejsou navázaná na konkrétní use-case váhy a týmové rozhodnutí | use-case scorecard + recommendation output v jednom |
| Už mám traces a evaly, ale rozhodnutí je pořád roztříštěné | Langfuse / Braintrust / Helicone | observability ukazuje provoz, ne finální doporučení pro business tradeoff | decision layer nad interními i veřejnými signály |
| Potřebuju klientovi nebo managementu obhájit volbu modelu | slides / docs / ad-hoc memo | ruční výstup je pomalý, neauditovatelný a opakuje se od nuly | shareable memo/scorecard export se stejnou logikou jako dashboard |
| Řeším rozpočet a fallback model, ne jen top quality | leaderboardy nebo provider pitch | leaderboard neukazuje cost ceiling, fallback ani budget-safe variantu | best overall / best budget / safest fallback v jedné vrstvě |
| Chci lightweight nástroj před nasazením plného LLMOps stacku | nic / spreadsheet | tým zůstává v chaosu a rozhodování je subjektivní | low-friction wedge ještě před observability adopcí |

### Packaging implication

Tohle podporuje 3 produktové balíčky, které jdou po stejné bolesti z různých stran:
- **scorecard-first** pro low-friction vstup a outbound
- **dashboard-first** pro týmy s opakovaným compare workflow
- **memo export** pro enterprise / governance / client-facing obhajobu

Hlavní závěr: produkt nemá prodávat „víc dat“. Má prodávat **rychlejší a obhajitelné rozhodnutí**.

## 12. Segment prioritization and pricing implication

Detailní ICP + pricing prioritizace je nově v `SEGMENT-PRICING-MATRIX.md`.

Hlavní závěr z tohoto passu:
- nejsilnější první komerční wedge je **AI startup / applied AI tým**
- nejnižší tření má **scorecard-first vstup** s následným upsellem na dashboard / workspace
- hlavní pricing hypothesis pro první reálný produktový sweet spot zůstává **€149 Pro**, ale zatím bez potvrzeného live buyer signálu
- agentury jsou silný druhý segment hlavně pro **shareable scorecard / memo** a pozdější **€399 Team** plán
- enterprise zůstává zajímavý spíš jako pozdější memo/governance motion než jako první self-serve wedge

Praktický dopad pro validaci:
- ve Wave 1 nevyhodnocovat jen reply rate, ale i to, jestli buyer reaguje spíš na **scorecard workflow** nebo na **dashboard workspace**
- sledovat, jestli startupy a agentury reagují rychleji než SaaS engineering týmy
- explicitně testovat, zda je první placená jednotka předplatné workspace, nebo opakovaný scorecard / memo workflow

## 12. Messaging framing test

Další konkrétní enrichment krok je nově zapsaný v `execution/MESSAGING-FRAMING-TEST.md`.

Smysl tohoto passu:
- netestovat jen CTA `demo` vs `scorecards`
- explicitně otestovat i mentální model produktu: `decision dashboard` vs `use-case scorecard` vs `decision memo / executive hybrid`
- propsat framing do outreach i discovery trackeru, aby po prvních odpovědích šlo rozhodnout, jestli stavět dashboard-first, scorecard-first nebo hybrid

Tím se enrichment posunul z obecného positioning do konkrétního validačního experimentu.
