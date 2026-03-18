# Segment + Pricing Matrix — multi-llm-benchmark-dashboard

## Purpose

Doplnit enrichment o jednu praktickou věc, která zatím chyběla v plně explicitní podobě:
**který ICP testovat jako první, s jakým artifactem a v jakém pricing balení**.

Nejde o finální pricing. Jde o rozhodovací podklad před externí validací, aby Wave 1 neověřovala jen messaging, ale i:
- který segment má největší pain
- kde je nejkratší cesta k placenému pilotu
- jestli první placený wedge má být scorecard-first, dashboard-first nebo memo-first

---

## Scoring model

Každý segment je hodnocený 1-5. Vyšší = lepší pro první komerční wedge.

| Kritérium | Váha | Co znamená |
|---|---:|---|
| Pain intensity | 30 % | jak bolestivý a častý je model-selection problém |
| Speed to decision | 20 % | jak rychle se dostaneme k relevantní odpovědi nebo callu |
| Willingness to pay | 20 % | pravděpodobnost rozpočtu pro placený pilot / SaaS |
| Distribution fit | 15 % | jak dobře sedí outbound + scorecard/demo flow |
| Product simplicity | 15 % | jak málo enterprise/ops komplexity je potřeba v první verzi |

**Interpretace:**
- **4.2-5.0** = nejlepší první wedge
- **3.5-4.1** = silný druhý segment
- **pod 3.5** = validovat později nebo jen opportunisticky

---

## Segment scorecard

| Segment | Pain | Speed | WTP | Distribution | Simplicity | Weighted score |
|---|---:|---:|---:|---:|---:|---:|
| AI startup CTO / applied AI lead | 5 | 5 | 4 | 4 | 4 | **4.55** |
| AI agentura founder / delivery lead | 4 | 4 | 4 | 5 | 4 | **4.15** |
| SaaS engineering lead s aktivní AI feature | 5 | 3 | 4 | 3 | 3 | **3.85** |
| Enterprise AI / governance owner | 4 | 2 | 5 | 2 | 2 | **3.15** |

### Ranking
1. **AI startup CTO / applied AI lead**
2. **AI agentura founder / delivery lead**
3. **SaaS engineering lead s aktivní AI feature**
4. **Enterprise AI / governance owner**

---

## 1. AI startup CTO / applied AI lead

### Why this segment ranks #1
- často testuje 3+ modelů a providerů
- rozhodnutí se dějí rychle a opakovaně
- problém je čerstvý: cost vs quality vs latency vs fallback
- menší interní politika než v enterprise
- vysoká šance na konkrétní feedback místo obecného „zajímavé"

### What they most likely buy first
- **scorecard-first vstup**
- následně **dashboard / workspace** pokud řeší opakované compare workflow

### Best first offer
- sample scorecard pro konkrétní use case
- navazující 20min demo nad decision workflow

### Pricing hypothesis
- **€39 Starter** pro solo / malý tým jako low-friction vstup
- **€149 Pro** jako hlavní pricing test / packaging hypotéza pro tým, který chce custom weights + interní eval import + history; zatím nejde o potvrzený willingness-to-pay signál

### Main risk
- část startupů bude chtít vše řešit ve spreadsheetu nebo interně
- pokud produkt zní moc enterprise, adoption spadne

### What to validate
- stačí scorecard jako wedge, nebo chtějí rovnou dashboard?
- je €149/měs vnímané jako rozumné proti času seniorních lidí?

---

## 2. AI agentura founder / delivery lead

### Why this segment ranks #2
- opakovaně obhajuje model stack klientům
- scorecard a memo artefakty mají okamžitou hodnotu
- buyer chápe hodnotu shareable outputu rychleji než interní SaaS tým
- dobrý fit na report + dashboard hybrid

### What they most likely buy first
- **scorecard / memo-first balení**
- až později team workspace nebo white-label varianta

### Best first offer
- klientsky sdílitelná scorecard
- export decision memo pro support / coding / extraction use case

### Pricing hypothesis
- **€149 Pro** jako testovaný Pro-level price point pokud jde o interní agenturní workflow; zatím ne jako potvrzený buyer signál
- **€399 Team** pokud chtějí více workspace, historii a sdílení napříč klienty
- potenciál pro white-label nebo consulting add-on

### Main risk
- část poptávky může být spíš po službě než po produktu
- mohou chtít více use-case-specific šablon hned od začátku

### What to validate
- chtějí průběžný dashboard, nebo jim reálně stačí exportovatelný artifact?
- kolik klientských workflow musí řešit měsíčně, aby SaaS dával smysl?

---

## 3. SaaS engineering lead s aktivní AI feature

### Why this segment ranks #3
- problém je reálný a často drahý
- fit na dashboard je silný
- ale cesta k odpovědi bývá pomalejší než u startupů
- vyšší šance, že už mají Langfuse / Braintrust / vlastní tooling a musí se jasně vysvětlit rozdíl

### What they most likely buy first
- **dashboard-first**
- scorecard jako leave-behind po prvním callu

### Best first offer
- demo compare workflow
- ukázka propojení public benchmarků + interních eval signálů

### Pricing hypothesis
- **€149 Pro** jako testovaný výchozí Pro price point
- **€399 Team** u více uživatelů nebo pravidelného decision review procesu

### Main risk
- bez interního data merge může být produkt vnímaný jako "jen hezčí compare"
- sales motion je pomalejší a product expectations vyšší

### What to validate
- jak silně trvají na interním eval importu od dne 1?
- stačí lightweight dashboard, nebo čekají hlubší observability funkce?

---

## 4. Enterprise AI / governance owner

### Why this segment ranks #4
- rozpočet může být nejvyšší
- governance a explainability pain je reálný
- ale první prodej je pomalý, politický a vyžaduje větší důvěru
- vysoké riziko, že první požadavek bude memo/report, ne self-serve produkt

### What they most likely buy first
- **memo / executive hybrid**
- teprve později dashboard nebo private workspace

### Best first offer
- decision memo pro model governance
- pilot s jedním use casem a stakeholder alignment výstupem

### Pricing hypothesis
- enterprise custom
- možný placený pilot místo self-serve pricingu

### Main risk
- dlouhý cyklus a scope creep
- early-stage produkt může působit příliš úzce nebo naopak nedostatečně enterprise-ready

### What to validate
- chtějí opakované decision workflow, nebo jen jednorázové recommendation memo?
- je enterprise angle vhodný už teď, nebo až po potvrzení u menších týmů?

---

## Packaging recommendation

### Best first package
**Scorecard-first entry -> dashboard upsell**

Proč:
- nejnižší tření v outboundu
- lze poslat bez nutnosti callu
- rychleji ukáže hodnotu než abstraktní „dashboard"
- přirozeně otevírá otázku, jestli tým potřebuje opakovaný workspace

### Product packaging ladder
1. **Free / manual sample scorecard**
   - acquisition a discovery vstup
2. **€39 Starter**
   - self-serve scorecards + watchlist + základní compare
3. **€149 Pro**
   - hlavní pricing test / packaging hypotéza pro startupy a menší AI týmy, zatím bez potvrzeného live buyer signálu
4. **€399 Team**
   - agentury, více workspace, historie, sdílení, exporty
5. **Enterprise custom**
   - governance, SSO, self-hosted, private connectors

---

## Pricing experiments to run in validation

| Experiment | Komu | Co přesně ověřit | Success signal |
|---|---|---|---|
| Sample scorecard -> paid follow-up | startup / agentura | jestli bezplatný sample otevírá placený workspace | lead chce další scorecard nebo recurring workflow |
| €39 self-serve probe | solo / malý tým | jestli existuje low-friction self-serve zájem | lead řekne, že by to zkusil bez callu |
| €149 team workspace probe | startup / SaaS tým | jestli je to realistický sweet spot | lead potvrdí, že by to řešil z team budgetu |
| €399 multi-workspace probe | agentura | jestli sdílení napříč klienty zvyšuje hodnotu | lead chce více klientských scorecards / historii |
| paid pilot / enterprise memo probe | enterprise | jestli je vhodnější pilot než self-serve SaaS | lead chce governance-oriented paid trial |

---

## Practical implication for Wave 1

Wave 1 nemá sbírat jen reply rate. Má zodpovědět i 3 obchodní otázky:
1. **Je nejsilnější první buyer startup, agentura nebo SaaS tým?**
2. **Otevírá konverzaci lépe scorecard-first než dashboard-first?**
3. **Je první placená jednotka dashboard subscription, nebo opakovaný scorecard / memo workflow?**

Proto je správné držet:
- startupy a agentury jako hlavní prioritní learning source
- SaaS týmy jako druhou validaci dashboard wedge
- enterprise jen opportunisticky, ne jako hlavní early wedge

---

## Recommendation

Pokud bych měl z dnešních enrichment dat vybrat jediný první komerční wedge, je to:

**AI startup / applied AI tým + scorecard-first vstup + případný upsell na testovaný €149 decision workspace.**

Druhý nejlogičtější wedge:

**AI agentura + shareable scorecard / memo + upsell na €399 multi-workspace team plan.**

Tohle je zatím nejčistší kombinace:
- krátký feedback loop
- vysoká srozumitelnost hodnoty
- nejmenší produktové riziko
- rozumná cesta k placenému pilotu
