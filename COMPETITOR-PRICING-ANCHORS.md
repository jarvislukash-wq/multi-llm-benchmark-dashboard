# Competitor Pricing Anchors - multi-llm-benchmark-dashboard

## Purpose

Prevest pricing hypotezy z intuice na aktualni verejne anchor body, aby dalsi Wave 1 pricing probes nestaly jen na dojmu.

**Capture date:** 2026-03-21  
**Source mode:** public pricing / homepage pages pres `browser_fetch`

---

## Quick takeaway

Trh kolem LLM tooling ukazuje 3 opakujici se vzory:

1. **Public benchmark / compare layer byva zdarma** nebo aspon funguje jako top-of-funnel.
2. **Prvni placeny team workflow** typicky zacina v low-hundreds USD mesicne, kdyz produkt resi opakovanou praci tymu.
3. **Vyssi team / enterprise tier** skace nahoru az ve chvili, kdy pribude collaboration, compliance, historie, exporty nebo governance.

To podporuje soucasny wedge:
- free sample scorecard jako acquisition
- Starter kolem ~EUR39 jako low-friction self-serve hypoteza
- Pro workspace kolem ~EUR99-149 jako hlavni testovany sweet spot
- Team od ~EUR399 az kdyz je uvnitr realny multi-workspace / shareable workflow

---

## Public anchor snapshots

| Produkt | Verejny pricing snapshot | Co je placene jadro | Implication pro nas |
|---|---|---|---|
| Artificial Analysis | homepage stavi na public intelligence, speed, price a personalized recommendation; zadny zjevny self-serve SaaS ceník na homepage | benchmark intelligence jako acquisition / trust layer | buyer bude cekat, ze zakladni compare a benchmark orientace nejsou hlavni placena hodnota |
| Langfuse | Free / **$29 Core** / **$199 Pro** / **$2499 Enterprise** | tracing, evals, historie, rate limits, teams, compliance | low-end paid AI tooling muze zacinat nizko, ale silnejsi team workflow si bez problemu rika o ~$199 |
| Helicone | Free / **$79 Pro** / **$799 Team** / Enterprise custom | alerts, reports, HQL, collaboration, compliance | vyrazny cenovy skok prichazi az s team/compliance vrstvou; ne jen za samotna data |

---

## What buyers are really paying for

### Artificial Analysis pattern
Buyer neplati za samotny fakt, ze existuje benchmark tabulka. Plati spis neprime pres trust, research distribution a recommendation value.

**Implication:**
Pokud by produkt nabizel jen hezci leaderboard, bude cenove i strategicky slaby.

### Langfuse pattern
Paid plan je obhajitelny tehdy, kdyz produkt sedi v opakovanem workflow tymu:
- delsi historie
- vyssi limity
- collaboration
- governance / compliance

**Implication:**
`multi-llm-benchmark-dashboard` musi prodavat opakovane rozhodovaci workflow, ne jednorazovy compare.

### Helicone pattern
Silnejsi pricing drzi hlavne vrstva:
- alerts / reports
- team collaboration
- organizace / compliance
- vyssi provozni jistota

**Implication:**
Vyssi tier u nas ma smysl jen pokud zahrne:
- sdilene workspace
- historii rozhodnuti
- opakovane scorecard refreshy
- exporty pro stakeholdery / klienty
- pripadne private connectors

---

## Packaging implications for this project

### 1. Free layer musi zustat silna
Nejlogictejsi free vstup je dal:
- sample scorecard
- lightweight compare preview
- pripadne public use-case scorecard page

Bez toho bude outbound tezsi, protoze public benchmark expectation je na trhu uz normalni.

### 2. Pro workspace kolem ~EUR99-149 porad dava smysl
Tento range je stale rozumny, protoze:
- je nad low-end utility pricingem
- je pod robustnejsi observability platformou typu Langfuse Pro
- sedi na buyer value: rychlejsi a obhajitelne model selection rozhodnuti

Tahle cena ale musi byt navazana na **opakovany team workflow**, ne jen na jednorazovy artifact.

### 3. Team tier od ~EUR399 je obhajitelny jen s jasnym scope
Aby mel Team tier smysl, musi byt zretelne minimalne 2-3 z techto hodnot:
- multi-workspace / vice klientu / vice use-case scorecards
- sdileni napric tymem
- historie a refresh porovnani
- exporty a stakeholder-ready memo/reporting
- alerts na zmeny ceny / vykonu / doporuceni

Bez toho je `~EUR399+` moc agresivni.

### 4. Paid pilot muze byt mezikrok pred SaaS subscription
Pro agentury nebo enterprise muze byt prvni placena jednotka spis:
- placeny scorecard / memo workflow
- decision review pilot
- custom benchmark pack

Ne vsichni musi skocit rovnou do recurring workspace pricingu.

---

## Recommended validation language

Pri validaci neprodavat cenu jako hotovou vec. Lepsi framing:
- "Kdyby to nahradilo rucni compare a dalo tymu sdilitelnou scorecard, je to pro vas spis lightweight self-serve vec, team budget, nebo enterprise / pilot motion?"
- "Je pro vas cennejsi jednorazovy artifact, nebo opakovany workspace s refreshi a alerty?"
- "Kdyby to usetrilo opakovane model review, je to spis pod EUR39, v pasmu team budgetu EUR39-149, nebo az vyssi nastrojova kategorie?"

---

## Validation implications

Wave 1 by mela potvrdit hlavne tyto 4 veci:

1. Jestli free scorecard opravdu otevira dalsi konverzaci.
2. Jestli buyer chce spis jednorazovy artifact, nebo recurring workspace.
3. Jestli `EUR99-149` pusobi jako realisticky team budget anchor.
4. Jestli vyssi `~EUR399+` tier dava smysl jen agenturam / multi-workspace buyerum.

---

## Recommended next step

Pricing hypoteza uz ma dostatecny verejny anchor. Dalsi poctivy krok neni dalsi pricing research, ale **pouzit tyto anchor body pri prvnich live price probes ve Wave 1**.
