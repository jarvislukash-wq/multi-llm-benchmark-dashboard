# Competitor Teardown — multi-llm-benchmark-dashboard

## Purpose

Doplnit enrichment o **konkrétní competitor read** z veřejného positioning textu hlavních hráčů.

Cíl není opsat feature list. Cíl je vyjasnit:
- co už trh dobře pokrývá
- kde je skutečná mezera
- kde je bezpečný wedge pro první verzi produktu

---

## Quick conclusion

Trh je silný ve 3 vrstvách:
1. **public benchmark intelligence**
2. **observability + evals**
3. **gateway / routing operativa**

Stále ale zůstává slabší **decision layer** pro tým, který potřebuje rychle rozhodnout:
- jaký model zvolit pro konkrétní use case
- jak obhájit tradeoff kvalita vs cena vs latence
- jak mít jednu scorecard pro engineering i management

To je nejrealističtější wedge.

---

## Public positioning snapshots

### 1. Artificial Analysis
**Veřejné positioning jádro:** nezávislá analýza AI landscape, intelligence index, speed, price, personalized model recommendation.

**Co tím jasně vlastní:**
- důvěryhodný přehled trhu
- benchmark data a metodiku
- rychlé veřejné compare napříč modely

**Co tím naopak neřeší úplně dobře:**
- interní rozhodovací workflow týmu
- collaboration kolem konkrétního use case
- merge interních evalů nebo produkčních signálů
- export rozhodnutí jako interní memo / scorecard workflow

**Implication pro nás:**
Nemá smysl soutěžit na „nejlepší veřejná benchmark data obecně". Smysl dává vzít benchmark layer jako vstup a postavit nad něj **decision workflow**.

---

### 2. Braintrust
**Veřejné positioning jádro:** AI observability platform, production traces → evals, prompt/model comparison, quality improvement per release.

**Co tím jasně vlastní:**
- observability pro AI produkty
- eval maturity workflow
- trace → dataset → eval loop
- quality/regression proces pro shipping týmy

**Co tím naopak není primárně:**
- jednoduchý market-facing cockpit pro pre-purchase model selection
- lightweight executive compare dashboard
- vendor-neutral scorecard pro „který model nasadit a proč" bez hlubší observability adopce

**Implication pro nás:**
Kdo už aktivně řeší production quality loop, může skončit u Braintrust. Náš wedge musí začínat **dřív v rozhodovacím cyklu** — ještě před plným eval/observability stackem.

---

### 3. Langfuse
**Veřejné positioning jádro:** open-source LLM engineering platform, traces, evals, prompt management, metrics.

**Co tím jasně vlastní:**
- populární open-source engineering vrstvu
- tracing a debug workflow
- developer adoption a self-hosting trust

**Co tím naopak zůstává vedle:**
- business-ready selection cockpit
- normalizované porovnání externích benchmarků, pricingu a use-case fitu
- jednoduchý doporučovací layer pro management / product ownera

**Implication pro nás:**
Langfuse je silná engineering platforma. Proti ní se nevyhrává observability šířkou. Vyhrát se dá na **jasném výstupu rozhodnutí**, ne na trace depth.

---

### 4. Helicone
**Veřejné positioning jádro:** AI gateway + LLM observability, route / debug / analyze.

**Co tím jasně vlastní:**
- provozní vrstvu kolem requestů
- routing a monitoring
- cost / usage / segments / alerts

**Co tím naopak není střed produktu:**
- strategický compare layer před rozhodnutím o model portfolio
- shareable scorecard pro use-case selection
- externí benchmark intelligence jako primární vstup

**Implication pro nás:**
Helicone řeší hlavně **run-time operativu**. Náš wedge je **decision-time workflow**.

---

### 5. OpenRouter Rankings
**Veřejné positioning jádro:** rankings podle reálného usage z milionů uživatelů, popularity, market share, use-case a language breakdowns.

**Co tím jasně vlastní:**
- behaviorální market signal
- popularity a adoption layer
- velmi dobrý top-of-funnel compare input

**Co tím naopak neřeší:**
- jestli je model nejlepší pro konkrétní produktový use case
- interní business constraints týmu
- explainable recommendation pro konkrétní organizaci

**Implication pro nás:**
Popularity je silný signál, ale není to rozhodnutí. OpenRouter je vhodný vstup do scorecard, ne finální odpověď.

---

## Market map

| Vrstva | Co už trh umí dobře | Reprezentanti | Kde je mezera |
|---|---|---|---|
| Public benchmark layer | nezávislý compare, price/speed/intelligence přehled | Artificial Analysis, OpenRouter, LMArena | chybí týmový decision workflow |
| Evals / observability | traces, scoring, regression, prompt compare | Braintrust, Langfuse, Confident AI, W&B Weave | chybí jednoduchý executive recommendation layer |
| Gateway / routing | request routing, governance, monitoring | Helicone, Portkey | neřeší pre-adoption model selection |
| Decision layer | částečně ručně ve spreadsheetu / slides | interní ad-hoc workflow | **tady je prostor pro produkt** |

---

## Where the wedge is strongest

### Best initial wedge
**Use-case model selection workspace** pro týmy, které:
- aktivně testují **3+ modelů / providerů**
- řeší tradeoff **quality / cost / latency**
- potřebují rozhodnutí vysvětlit dál v týmu
- ještě nechtějí nasazovat těžší observability stack jako první krok

### Nejlepší první buyer
1. AI startup CTO / applied AI lead
2. AI agentura founder / delivery lead
3. Product / engineering lead v SaaS s aktivní AI feature

### Proč právě tento wedge
- kratší rozhodovací cyklus
- silnější akutní pain
- vyšší šance na manual-first workflow a pilot
- menší riziko, že buyer čeká enterprise-grade observability od dne 1

---

## Anti-positioning

Aby produkt nezapadl mezi existující kategorie, měl by se aktivně vymezit:

### Nejsme
- další observability tool
- další public leaderboard
- další LLM gateway
- další eval framework pro ML specialisty

### Jsme
- **decision cockpit pro výběr modelu podle use case**
- **scorecard layer mezi benchmarky a interní realitou týmu**
- **shareable recommendation workflow pro engineering i business**

---

## Product packaging implications

### Co musí být v MVP
- model catalog nad veřejnými zdroji
- use-case weighting
- scorecard output: best overall / best budget / safest fallback
- shareable report nebo memo export

### Co naopak není nutné v MVP
- plná tracing platforma
- vlastní gateway
- heavy eval orchestration
- enterprise governance suite

### Důležitý packaging insight
První testovaná placená hodnota pravděpodobně nebude „dashboard jako takový", ale:
- rychlejší rozhodnutí
- méně chaosu při model review
- obhajitelný výstup pro tým / klienta / management

To nahrává balení typu:
- **free compare / scorecard preview** jako acquisition
- **pricing hypotéza: low-end self-serve monitor kolem ~€39** pro solo / early teams, pokud buyer ocení průběžný compare workflow
- **pricing hypotéza: Pro workspace v pásmu €99–149** jako hlavní testovaný candidate paid tier
- **pricing hypotéza: Team plan od ~€399** jako pozdější testovaný tier pro sdílení, alerts, exporty a historii rozhodnutí

---

## What would make this fail

Projekt bude slabý, pokud sklouzne do jedné z těchto pastí:

1. **Příliš široká observability ambice**
   - Braintrust / Langfuse / Helicone už mají silný náskok.

2. **Pouhý leaderboard wrapper**
   - veřejné benchmarky samy o sobě jsou snadno kopírovatelné.

3. **Bez use-case framingu**
   - bez scorecard vrstvy mizí hlavní diferenciace.

4. **Bez shareable outputu**
   - pokud nejde doporučení snadno přeposlat nebo obhájit, klesá business hodnota.

---

## Pricing anchor snapshots

Aby pricing hypotéza nezůstala jen teoretická, je dobré držet i rychlý veřejný anchor z blízkých kategorií.

| Produkt | Veřejný pricing snapshot | Packaging lesson pro nás |
|---|---|---|
| Langfuse | Free / **$29 Core** / **$199 Pro** / **$2499 Enterprise** | AI tooling trh snese self-serve team tier kolem low-hundreds USD měsíčně, pokud je produkt napojený na opakovaný workflow. |
| Helicone | Free / **$79 Pro** / **$799 Team** / Enterprise | Monitoring / gateway vrstva je ochotná prodávat výrazně výš, ale až když nese provozní a týmovou hodnotu. |
| Artificial Analysis | veřejný compare a recommendation obsah funguje jako top-of-funnel zdarma | Free intelligence layer může být silný acquisition kanál, placená hodnota musí začínat až u team decision workflow nebo exportu. |

### Pricing implication

Z těchto anchorů plyne praktická věc:
- nízký vstup dává smysl jako **free compare / sample scorecard**
- hlavní placený sweet spot pro tým může realisticky sedět v **testovaném pásmu cca €79-199/měs**
- vyšší tier dává smysl až se sdílením, historií, alerty nebo multi-workspace režimem

To podporuje původní hypotézu, že první komerční wedge nemá být enterprise-heavy, ale **scorecard-first / decision-workspace-first** pro malé až střední AI týmy.

## Hidden competitors and status-quo substitutes

Největší konkurence nemusí být další SaaS. Často je to prostě "uděláme si to ručně".

| Status quo alternativa | Proč ji buyer používá | Kde selhává | Implication pro nás |
|---|---|---|---|
| Spreadsheet / Notion tabulka | nulové pořizovací náklady, plná kontrola | rychle zastará, chybí jednotné score weights a audit trail | produkt musí být rychlejší než ruční compare už v prvním use case |
| Slides / interní memo | snadno se sdílí s managementem nebo klientem | vzniká ručně, nejde snadno refreshnout po změně modelu nebo ceny | memo export musí být defaultní output, ne až enterprise add-on |
| Provider-native playground / dashboard | buyer už je v nástroji providera | neporovnává férově cross-vendor tradeoff a většinou neřeší fallbacky | vendor-neutral compare je klíčová součást positioning wedge |
| Ad-hoc eval skripty | technický tým má pocit, že si vše změří sám | výstupy jsou roztříštěné a těžko sdílené mimo engineering | scorecard musí spojit engineering signály a business rozhodnutí |

### Practical takeaway

Produkt nevyhrává tím, že přidá další data. Vyhrává tím, že porazí ruční workflow ve 3 věcech:
- rychlost prvního rozhodnutí
- snadné sdílení výstupu
- opakovatelný refresh po změně modelu, benchmarku nebo ceny

---

## Recommended positioning draft

### One-liner
Vyber správný LLM model pro konkrétní use case pomocí jedné scorecard nad benchmarky, cenou, latencí a interními signály.

### 3 short bullets
- Use-case scorecards místo obecných leaderboardů
- Veřejná + interní data v jednom rozhodnutí
- Doporučení, které pochopí engineering i management

---

## Recommended next enrichment-to-validation bridge

Po competitor teardownu už další práce nemá být další obecný research. Další smysluplný krok je:

1. otestovat, jestli buyer víc reaguje na framing **decision dashboard** nebo **scorecard / memo**
2. zjistit, jestli první testovaná placená forma má být **dashboard**, **report**, nebo **hybrid**
3. z prvních odpovědí vytáhnout, jestli je silnější wedge:
   - AI startup multi-model selection
   - AI agenturní client-facing scorecards
   - SaaS fallback / budget governance
