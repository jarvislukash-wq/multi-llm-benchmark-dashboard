# Wave 1 Timing Triggers — multi-llm-benchmark-dashboard

## Purpose

Doplnit k Wave 1 jednu chybějící věc:
**nejít jen podle segmentu, ale i podle správného momentu a konkrétního triggeru, který otevírá konverzaci.**

Tahle vrstva není nový routing dokument.
Je to praktický doplněk k `DISCOVERY-TRACKER.md`, `execution/WAVE1-OUTREACH-BATCH.md` a `execution/OUTREACH-PLAYBOOK.md`, aby bylo jasné:
- proč oslovit právě tenhle účet teď
- jaký konkrétní pain otevřít jako první
- kdy použít `dashboard`, `scorecard` nebo `memo` bez zbytečného přepitchování

---

## Source-of-truth note

Platí toto pořadí pravdy:
1. `DISCOVERY-TRACKER.md` drží kanonické přiřazení buyer situation, framingu a CTA
2. `execution/WAVE1-OUTREACH-BATCH.md` drží ready-to-send kombinaci kontakt + framing + CTA + artifact
3. tento dokument jen přidává **timing layer**: proč je účet relevantní právě teď a jaký opener má nejvyšší šanci otevřít reply

Tento dokument nemá měnit `buyer situation`, `framing`, `CTA` ani artifact mapping.

---

## Fresh public market signals from this pass

Tyhle signály stojí za tím, proč má timing vrstva smysl právě teď.

### 1. Public compare layer je už silný a buyer ho zná
- **Artificial Analysis** veřejně staví na tom, že pomáhá vybrat nejlepší model a provider pro konkrétní use case podle intelligence, speed a price.
- **OpenRouter Rankings** veřejně staví na usage datech z milionů uživatelů a ukazuje popularitu modelů podle use case, jazyka a tool usage.

**Implication:**
Neprodávat „lepší leaderboard“ ani popularity layer.
První věta musí otevírat **rozhodnutí v týmu**, ne samotná data.

### 2. Observability / gateway kategorie už mají jasné rozpočtové anchor body
- **Langfuse** veřejně ukazuje self-serve pricing `$29 / $199 / $2499`.
- **Helicone** veřejně ukazuje `$79 / $799 / enterprise` a silně komunikuje monitoring, gateway a alerts.

**Implication:**
Buyer už je zvyklý, že za opakovaný AI workflow nástroj se platí.
Ale platí se za **průběžný provozní nebo rozhodovací workflow**, ne za hezčí benchmark tabulku.

### 3. AI-native a AI-enabled produkty rozšiřují AI surface area
- **Notion** veřejně tlačí AI workspace, agents, enterprise search a meeting notes.
- **Graphite** veřejně tlačí AI code review a PR workflow.
- **Magic Patterns** veřejně tlačí AI prototyping pro product týmy.
- **Fintool** veřejně tlačí AI agent workflow pro equity research.

**Implication:**
Čím víc AI use casů produkt má, tím častěji vzniká problém:
- který model je nejlepší pro nový workflow
- kdy přepnout na levnější fallback
- jak rozhodnutí vysvětlit mimo engineering

---

## Trigger categories

Používat jen jako opener / priority layer. Ne jako náhradu buyer-situation labelů.

| Trigger | Kdy ho použít | Nejlepší framing | Co buyer typicky řeší | Čemu se vyhnout |
|---|---|---|---|---|
| `new_ai_surface` | firma viditelně rozšiřuje AI features nebo AI workflow | dashboard nebo scorecard | nový use case, srovnání více modelů, rychlé první rozhodnutí | nepitchovat observability platformu |
| `compare_chaos` | buyer pravděpodobně kombinuje leaderboardy, pricing tabulky a interní poznámky | dashboard | roztříštěné zdroje dat, chybí finální compare view | neprodávat raw benchmark data |
| `budget_fallback` | use case je citlivý na cenu, throughput nebo fallback | scorecard | best budget pick, safest fallback, cost ceiling | nezačínat abstraktním dashboard pitch-em |
| `stakeholder_alignment` | rozhodnutí je potřeba obhájit managementu, klientovi nebo governance vrstvě | memo | explainability, recommendation, alignment | nezačínat technickými benchmark detaily |
| `pre_llmops_gap` | tým je dost AI-native na to, aby řešil model selection, ale nepotřebuje další těžký stack | scorecard -> dashboard | lightweight decision layer před observability adopcí | nesrovnávat se přímo s Langfuse / Helicone šířkou |

---

## Trigger-to-message rules

### 1. `new_ai_surface`
Použij, když veřejný web jasně ukazuje aktivní AI produktovou expanzi.

**Nejlepší opener:**
- „u vás mi to sedí hlavně na nový / rozšiřující se AI workflow“
- „jak dnes vybíráte model pro nový use case bez restartu od nuly“

**Good fit accounts in current Wave 1:**
- Notion
- Magic Patterns
- Graphite
- Fintool

### 2. `compare_chaos`
Použij, když je pravděpodobné, že tým už má benchmarky nebo eval signály, ale chybí finální decision layer.

**Nejlepší opener:**
- „nejde mi o další leaderboard, spíš o compare workflow“
- „co se změnilo proti poslednímu rozhodnutí“

**Good fit accounts in current Wave 1:**
- Khan Academy
- Dropbox
- Notion
- Zapier
- Canva

### 3. `budget_fallback`
Použij, když use case zjevně nese cost pressure nebo vysoký objem.

**Nejlepší opener:**
- „best budget pick + safest fallback“
- „kde je tradeoff kvalita vs cena vs latence“

**Good fit accounts in current Wave 1:**
- SumUp
- Canva
- Loom
- Fintool

### 4. `stakeholder_alignment`
Použij, když buyer pravděpodobně potřebuje rozhodnutí vysvětlit dál.

**Nejlepší opener:**
- „obhájit, proč je vhodný právě tenhle model“
- „podklad použitelný pro engineering i management“

**Good fit accounts in current Wave 1:**
- Merck
- Ramp
- Coursera

### 5. `pre_llmops_gap`
Použij, když tým zjevně řeší AI workflow, ale first-touch musí být lehký a konkrétní.

**Nejlepší opener:**
- „use-case scorecard místo dalšího obecného benchmarku“
- „lightweight decision layer před plným LLMOps stackem“

**Good fit accounts in current Wave 1:**
- Magic Patterns
- Loom
- Graphite

---

## Account-level trigger map for Wave 1A

| Account | Public signal from this pass | Primary trigger | Why now | Best opener angle |
|---|---|---|---|---|
| Canva | AI Help Experience ownership + support-facing AI surface | `budget_fallback` | support workflow rychle promění model choice do cost + quality tradeoffu | support scorecard: best overall / budget / fallback |
| Khan Academy | AI tutoring context je kvalitou citlivý a rozpočtově relevantní | `compare_chaos` | public benchmarky samy nestačí pro tutoring tradeoff | compare workflow pro quality vs cost |
| Magic Patterns | AI-native product prototyping platform | `pre_llmops_gap` | vysoká šance častých modelových rozhodnutí bez potřeby těžké observability vrstvy | sample scorecard pro coding + product workflow |
| Merck | AI + data science + enterprise leadership kontext | `stakeholder_alignment` | value je v obhajitelném recommendation outputu | executive memo pro governance-oriented use case |
| SumUp | operations + AI ownership, přirozený tlak na budget/fallback | `budget_fallback` | support / operations use case je citlivý na náklady a spolehlivost | scorecard pro budget ceiling + fallback |
| Notion | AI workspace, agents, enterprise search, AI meeting notes | `new_ai_surface` | široká AI surface area zvyšuje počet opakovaných model decisions | dashboard opener pro multi-model decision workflow |
| Graphite | AI code review platform | `new_ai_surface` | coding use case přirozeně vyvolává compare otázku kvalita vs rychlost vs cost | coding scorecard opener |
| Fintool | AI agent workflow pro equity research | `compare_chaos` | přesnost, cost a fallback jsou rozhodovací, ne jen observability problém | dashboard opener pro eval + routing decisions |
| Ramp | veřejný AI + operations angle | `stakeholder_alignment` | model choice je potřeba svázat s productivity a cost discipline | executive memo opener |

---

## Account-level trigger map for Wave 1B

| Account | Public signal from this pass | Primary trigger | Why now | Best opener angle |
|---|---|---|---|---|
| Dropbox | AI/search/eval fit z customer story contextu | `compare_chaos` | pravděpodobně mají signály, ale ne nutně sdílitelný decision layer | dashboard compare workflow |
| Coursera | learning-oriented AI feature context | `stakeholder_alignment` | learning workflow často potřebuje vysvětlit tradeoff i netechnickým stakeholderům | memo / executive feedback |
| Zapier | orchestration-heavy AI operations context | `compare_chaos` | více use casů a providerů zvyšuje decision fatigue | dashboard pro multi-model operations |
| Loom | AI-assisted workflow + throughput angle | `pre_llmops_gap` | low-friction sample má větší šanci než široký platform pitch | scorecard pro high-volume workflow |

---

## Practical send priority rule

Když není kapacita poslat vše najednou, prioritizuj účty podle této logiky:

### Priority 1 — nejvyšší šance na konkrétní reply
1. `budget_fallback`
2. `pre_llmops_gap`
3. `compare_chaos`
4. `stakeholder_alignment`

### Why
- `budget_fallback` a `pre_llmops_gap` typicky otevírají nejkratší a nejkonkrétnější odpověď
- `compare_chaos` je silný, ale buyer může chtít delší vysvětlení rozdílu proti observability tools
- `stakeholder_alignment` je relevantní, ale reply cycle bývá pomalejší

### Recommended first 5 by trigger practicality
1. SumUp — `budget_fallback`
2. Magic Patterns — `pre_llmops_gap`
3. Canva — `budget_fallback`
4. Graphite — `new_ai_surface`
5. Notion — `new_ai_surface`

Tohle není nový canonical send order. Je to praktická zkratka pro situaci, kdy chceme nejdřív nasbírat reply quality z nejkonkrétnějších openerů.

---

## Trigger-aware objection handling

| Trigger | Nejpravděpodobnější objection | Co říct místo přepitchování |
|---|---|---|
| `new_ai_surface` | „tohle si změříme sami“ | „dává smysl — zajímá mě hlavně, jestli vám dnes chybí sdílitelný compare output, ne samotná data“ |
| `compare_chaos` | „už máme Langfuse / Braintrust / vlastní evaly“ | „právě to mě zajímá — jestli vám i s nimi chybí finální model decision layer“ |
| `budget_fallback` | „stačí nám levnější model a hotovo“ | „rozumím — pointa je vidět, kdy levnější model ještě stačí a kdy už ne“ |
| `stakeholder_alignment` | „tohle je spíš interní deck než produkt“ | „to je fér — ověřuju právě, jestli se to láme u jednorázového memo, nebo u opakovaného workflow“ |
| `pre_llmops_gap` | „nechceme další tool“ | „právě proto testuju scorecard-first vstup místo plné platformy“ |

---

## What to log after live sends

Do `execution/OUTREACH-LOG-TEMPLATE.md` nezavádět novou taxonomii, pokud to není nutné.

Stačí do `Notes / exact phrasing` dopsat:
- jaký trigger byl skutečně použit jako opener
- jestli buyer na ten trigger navázal
- jestli bylo potřeba trigger změnit v follow-upu

Praktický formát poznámky:
- `trigger_used: budget_fallback`
- `trigger_confirmed: yes / no / unclear`
- `trigger_shift: none / dashboard / scorecard / memo`

---

## Decision rule after first replies

Po prvních 5+ odpovědích nevyhodnocovat jen segment a framing.
Vyhodnotit i tohle:
1. který trigger otevírá nejrychleji reply
2. který trigger vede ke kvalitnějším odpovědím než jen „zajímavé“
3. kde buyer sám zopakuje stejný pain vlastním jazykem

Pokud se to bude opakovat, další vlna má být řízená už nejen podle segmentu, ale i podle vítězného triggeru.
