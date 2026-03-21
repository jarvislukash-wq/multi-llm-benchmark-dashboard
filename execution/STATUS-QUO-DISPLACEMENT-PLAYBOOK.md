# Status-Quo Displacement Playbook — multi-llm-benchmark-dashboard

## Purpose

Prevest competitor a hidden-competitor poznatky do jedne prakticke vrstvy pro Wave 1.

Tenhle dokument neresi novy ICP ani novy pricing.
Resi jednu konkretni vec:
**co presne musi produkt porazit v prvnich reply a calls, aby buyer nezustal u dnesniho workflow.**

Nejvetsi konkurence v prvnim nakupnim momentu casto neni dalsi SaaS.
Je to:
- spreadsheet / Notion tabulka
- slides / interni memo
- provider-native compare
- observability / eval stack bez finalni decision vrstvy

---

## Fresh public anchors from this pass

Z verejnych stranek je porad zretelne:

- **Artificial Analysis** vlastni public compare: intelligence, speed, price, recommendation.
- **OpenRouter Rankings** vlastni popularity a usage signal.
- **Langfuse** vlastni traces, evals, prompt management a metrics.
- **Helicone** vlastni gateway, routing, debug a analyze vrstvu.
- **Braintrust** vlastni trace -> eval -> quality loop.

### Practical implication

Nesmi se prodavat:
- dalsi leaderboard
- dalsi trace viewer
- dalsi gateway
- dalsi "AI analytics" bez decision outputu

Musi se prodavat:
- rychlejsi rozhodnuti
- sdilitelny vystup
- opakovatelny refresh po zmene modelu, ceny nebo fallbacku

---

## Status-quo map

| Status quo | Proc u nej buyer zustava | Kde se decision rozbije | Co musi produkt vyhrat | Nejlepsi framing | Nejlepsi CTA |
|---|---|---|---|---|---|
| `spreadsheet` | nulove naklady, rychly start, plna kontrola | rychle zastara, vahy nejsou jednotne, tezko se sdili | `speed` | `scorecard` | send sample scorecard |
| `memo` | jde snadno preposlat managementu nebo klientovi | pri kazde zmene modelu se dela znovu | `shareable_output` | `memo` | ask for executive feedback |
| `provider_native` | buyer uz je uvnitr jednoho providera | chybi cross-vendor compare, fallback a neutralita | `refreshability` | `dashboard` | ask for 20min demo call |
| `mixed` | tym kombinuje benchmarky, pricing, traces a poznamky | nikdo nema finalni source of truth | `mixed` | `dashboard` -> `memo` fallback | ask for 20min demo call |
| `unclear` | buyer jeste nepojmenoval dnesni workflow | neni jasne, co realne pouziva | nejdriv diagnostika, ne pitch | `scorecard` default | send sample scorecard |

---

## Discovery routing by status quo

### 1. Kdyz buyer zije ve `spreadsheet`

**Signal:**
- "mame tabulku"
- "porovnavame si to rucne"
- "mame to v Notionu"

**Nejkratsi value promise:**
- rychlejsi prvni rozhodnuti
- jednotne vahy pro use case
- best overall / budget / fallback bez rucniho prepisovani

**Co nerikat:**
- "mame vic dat"
- "mame lepsi leaderboard"

**Co rict:**
- "zajima me hlavne, jestli vam dnes chybi rychly compare vystup bez rucniho skladani tabulky"

**Best next asset:**
- scorecard

---

### 2. Kdyz buyer zije v `memo`

**Signal:**
- "delame deck pro management"
- "piseme doporuceni klientovi"
- "stejne to nakonec skonci ve slidich"

**Nejkratsi value promise:**
- shareable output bez rucniho prepisu
- decision rationale pro engineering i management
- snadny refresh pri zmene modelu nebo ceny

**Co nerikat:**
- technicke benchmark detaily jako prvni vec

**Co rict:**
- "overuju, jestli je pro vas dulezitejsi samotne compare, nebo spis rychly podklad, ktery jde hned poslat dal"

**Best next asset:**
- memo

---

### 3. Kdyz buyer zije v `provider_native`

**Signal:**
- "koukame na provider dashboard"
- "porovnavame to u OpenAI / Anthropic / provideru"
- "resime to uvnitr jednoho stacku"

**Nejkratsi value promise:**
- neutralni cross-vendor compare
- budget pick vedle safest fallback
- refresh po release nebo pricing zmene

**Co nerikat:**
- "nahradime vam observability"
- "udelame vam routing"

**Co rict:**
- "nejde mi o dalsi trace nebo gateway vrstvu; zajima me, jestli vam dnes chybi neutralni finalni decision layer napric providery"

**Best next asset:**
- dashboard

---

### 4. Kdyz buyer zije v `mixed`

**Signal:**
- "bereme benchmarky zvenku, cost z observability a zbytek rucne"
- "mame to rozsekane mezi vic nastroju"

**Nejkratsi value promise:**
- jedna scorecard / dashboard nad roztříštěnými signály
- auditovatelny compare output
- mene restartu od nuly pri kazdem novem modelu

**Co nerikat:**
- ze nahradime vsechny jejich nastroje

**Co rict:**
- "zajima me, jestli je dnes nejvetsi problem samotne mereni, nebo spis finalni rozhodnuti a sdilitelny vystup"

**Best next asset:**
- dashboard, pripadne memo fallback podle stakeholder angle

---

## Objection handling by status quo

| Status quo | Nejpravdepodobnejsi objection | Bezpecna odpoved |
|---|---|---|
| `spreadsheet` | "tohle uz si zvladneme udelat sami" | "to verim — overuju hlavne, jestli je rucni compare dost rychly a opakovatelny i pri dalsi zmene modelu" |
| `memo` | "tohle je spis sluzba nez produkt" | "to je fer — zajima me prave, jestli se to u vas lame u jednorazoveho doporuceni, nebo u opakovaneho workflow" |
| `provider_native` | "tohle uz vidime u providera" | "jasne — pointa neni dalsi provider view, ale neutralni compare a fallback napric vendory" |
| `mixed` | "uz mame Langfuse / Braintrust / vlastni evaly" | "prave to me zajima — jestli vam i s nimi chybi finalni recommendation vrstva" |
| `unclear` | "zatim jen koukame" | "v pohode — staci mi vedet, jestli dnes rozhodujete spis v tabulce, memu nebo provider view" |

---

## What to log after each real conversation

Do `execution/OUTREACH-LOG-TEMPLATE.md` po reply nebo call vzdy doplnit:

- `status_quo`
- `status_quo_break`
- jednu presnou vetu, ktera to potvrzuje
- jestli buyer chtel `dashboard`, `scorecard` nebo `memo`

### Minimal forced questions

Kdyz to buyer prirozene nerekl, staci 3 kratke otazky:
1. "Jak to dnes porovnavate — spis tabulka, memo, nebo provider-native view?"
2. "Co je na tom nejvic pomale nebo otravne?"
3. "Co by pro vas bylo cennejsi: rychlejsi compare, sdilitelny vystup, nebo refresh po zmene modelu?"

---

## Practical win conditions for Wave 1

Prvni vlna nema dokazat, ze produkt porazi vsechny kategorie.
Ma dokazat, ze umi porazit aspon jeden status quo opakovane.

### Nejsilnejsi prve targety
1. `spreadsheet` -> vyhrat na `speed`
2. `provider_native` -> vyhrat na `refreshability`
3. `memo` -> vyhrat na `shareable_output`

### Slabsi prvni target
- `mixed`, pokud buyer nedokaze pojmenovat hlavni bolest

---

## Decision rule after first 5+ replies

Vyhodnotit ne jen reply rate a framing, ale i tohle:

1. Ktery `status_quo` se objevuje nejcasteji
2. Ktery `status_quo_break` se opakuje nejcasteji
3. Ktery artifact nejlip vytlacuje dnesni workflow
4. Ktery exact phrase buyer sam pouziva pri popisu dnesni bolesti

Pokud se bude opakovat stejna kombinace, dalsi vlna outreach ma byt rizena uz i podle toho:
- `spreadsheet + speed`
- `provider_native + refreshability`
- `memo + shareable_output`

---

## Guardrail

Tenhle playbook nema rozsirovat scope produktu.
Naopak ho ma drzet uzce:
- decision layer
- use-case compare
- shareable output
- refreshable recommendation

Jakmile messaging sklouzne do "monitoringu", "gateway", "full eval platform" nebo "lepsiho leaderboardu", buyer se vraci na pudu silnejsich existujicich kategorii.
