# Validation Assets — multi-llm-benchmark-dashboard

## Goal

Převést enrichment z obecné tržní analýzy do konkrétních validačních materiálů, které se dají použít pro:
- 10-15 customer discovery rozhovorů
- landing page smoke test
- první messaging test podle use case
- otestování, jestli se z painu a evaluace dá dojít k realistickému placenému pilotu nebo rozumnému cenovému pásmu

---

## 1. ICP interview target list

Cíl: nemluvit obecně s "AI lidmi", ale s lidmi, kteří reálně rozhodují o výběru modelů, rozpočtu nebo evaluacích.

| # | Segment | Role | Velikost týmu | Proč je relevantní | Hlavní otázka k ověření |
|---|---|---|---:|---|---|
| 1 | AI startup | CTO / cofounder | 3-10 | nese odpovědnost za cost-quality tradeoff | Jak dnes obhajujete volbu modelu před byznysem? |
| 2 | AI startup | Applied AI lead | 2-8 | řeší evaluace a model switching | Co vás nejvíc brzdí při porovnání 3+ modelů? |
| 3 | SaaS s AI feature | Product lead | 5-20 | potřebuje rozhodnutí bez hlubokého ML backgroundu | Jak se dnes rozhoduje mezi kvalitou, cenou a rychlostí? |
| 4 | AI agentura | Founder | 2-15 | vybírá modely pro více klientů | Kolikrát měsíčně musíte klientovi vysvětlovat model stack? |
| 5 | AI agentura | Delivery lead | 3-12 | potřebuje opakovatelné scorecards | Chybí vám opakovatelný compare framework? |
| 6 | Enterprise innovation | AI product manager | 5-25 | potřebuje decision memo a governance | Jak dnes dokumentujete doporučení modelu? |
| 7 | Enterprise innovation | Procurement / platform owner | 5-30 | zajímá ho vendor risk a náklady | Co by musel dashboard ukázat, aby pomohl s procurementem? |
| 8 | LLMOps tým | AI engineer | 2-10 | má interní latency/cost data | Kde dnes kombinujete interní a veřejná data? |
| 9 | RAG produkt | Head of engineering | 4-15 | řeší relevance, cenu a fallbacky | Jak často měníte model kvůli horším reálným výsledkům? |
| 10 | Support automation | Product owner | 3-12 | potřebuje stabilitu a budget control | Jak poznáte, že je "budget model" ještě dost dobrý? |
| 11 | Coding assistant tým | Tech lead | 3-10 | srovnává code-heavy modely | Podle čeho rozhodujete mezi benchmarkem a UX v produkci? |
| 12 | Data extraction workflow | Ops/automation lead | 2-8 | řeší vysoký objem a cenu za task | Jak měříte cost per successful task? |

### Prioritní pořadí outreach

1. AI startup CTO / applied AI lead
2. AI agentura founder / delivery lead
3. SaaS product lead s aktivní AI feature
4. Enterprise innovation / governance role

### Interview screener

Respondent je vhodný, pokud platí aspoň 3 z 5:
- používá nebo testuje 3+ modelů / providerů
- dělá rozhodnutí mezi kvalitou, cenou a latencí
- má vlastní evaly nebo produkční usage data
- během posledních 90 dnů měnil nebo zvažoval změnu modelu
- rozhoduje o rozpočtu nebo doporučuje model stack dál v organizaci

### Interview script outline (20-25 min)

1. Kontext produktu a use case (3 min)
2. Jak dnes vybírá model (5 min)
3. Jaké zdroje dat používá (4 min)
4. Kde je největší pain / slepé místo (5 min)
5. Reakce na koncept decision dashboardu (4 min)
6. Ochota platit / alternativy / další krok (4 min)

---

## 2. Landing page messaging pack

### Hero variant A — executive angle

**Headline:**
Vyber správný LLM model bez chaosu v benchmarcích.

**Subheadline:**
Jedno místo, kde spojíš benchmarky, cenu, latenci a vlastní evaly do jasného doporučení pro konkrétní use case.

**Primary CTA:**
Chci early access

**Secondary CTA:**
Ukázat scorecards

### Hero variant B — engineering angle

**Headline:**
Porovnej GPT, Claude, Gemini a další podle reálného use case.

**Subheadline:**
Ne leaderboard pro všechny. Decision dashboard pro týmy, které potřebují obhájit nejlepší model podle kvality, nákladů a rychlosti.

**Primary CTA:**
Rezervovat demo

### Hero variant C — agency / consultant angle

**Headline:**
Přestaň klientům doporučovat modely podle dojmu.

**Subheadline:**
Vytvoř shareable scorecards pro support, RAG, coding i extraction a ukaž jasný důvod, proč tenhle model vyhrál.

**Primary CTA:**
Chci 3 ukázkové scorecards

### 3 value bullets above the fold

- Srovnání modelů podle use case, ne podle hype.
- Cena, latence a kvalita v jedné scorecard.
- Shareable doporučení pro tým i management.

### Problem section copy

Dnes máš benchmarky v jednom tabu, pricing na stránkách providerů, latency v observability nástroji a interní evaly v notebooku nebo CI. Výsledek je jednoduchý: výběr modelu trvá dlouho, těžko se obhajuje a často se opakuje od nuly při každém novém release.

### Solution section copy

Multi-LLM Benchmark Dashboard spojuje veřejné benchmarky, pricing, interní evaly a produkční signály do jednoho dashboardu. Každý use case dostane vlastní váhy a výsledkem je jasné doporučení:
- best overall
- best budget pick
- best speed pick
- safest fallback
- strongest coding / reasoning option

### Feature blocks

#### 1. Use-case scorecards
Každý use case má vlastní priority. Support bot nechce totéž co coding assistant.

#### 2. Public + internal data merge
Veřejné leaderboardy bez interní reality nestačí. Tady se skládají dohromady.

#### 3. Decision-ready outputs
Exportovatelný report pro CTO, product lead i klienta.

### Social proof placeholders

- "Ušetřili jsme dny rozhodování při každém model review."
- "Konečně jsme měli jeden podklad pro engineering i management."
- "Pomohlo nám to obhájit přechod na levnější fallback model."

### CTA section

**Headline:**
Chceš vědět, který model je nejlepší pro tvůj konkrétní use case?

**CTA:**
Přidej se do early access a pošli svůj use case.

### Objections to test

- „Tohle už řeší Langfuse / Helicone.“
- „Veřejné benchmarky si umíme přečíst sami.“
- „Bez našich interních dat to pro nás nemá hodnotu.“
- „Spíš chceme API nebo report než další dashboard.“

---

## 3. Use-case scorecards

Níže jsou 3 ukázkové scorecards pro messaging i discovery. Nejsou to finální benchmark výsledky, ale struktura, podle které má kupující přemýšlet.

### Scorecard A — RAG support assistant

**Buyer:** AI product lead / support automation owner

**Primární cíl:**
Dobrá odpověď na zákaznický dotaz při kontrolovaných nákladech a nízké latenci.

**Top decision metrics:**
- answer quality / groundedness — 35 %
- latency — 20 %
- price per 1k conversations — 20 %
- hallucination risk — 15 %
- context handling — 10 %

**What winning looks like:**
- spolehlivé odpovědi nad interním baseline
- přijatelná rychlost pro live support
- možnost levnějšího fallback modelu

**Decision outputs to show:**
- best overall support model
- best budget support model
- safest fallback

**Why this scorecard matters:**
Support týmy často nechtějí absolutně nejlepší model, ale nejlepší poměr kvalita / rychlost / cena.

### Scorecard B — AI coding assistant

**Buyer:** CTO / engineering lead

**Primární cíl:**
Vybrat model pro code generation, debugging a refactoring bez zbytečného přepalování rozpočtu.

**Top decision metrics:**
- code task quality — 40 %
- tool use / function calling fit — 15 %
- latency — 10 %
- price per engineering seat / workflow — 15 %
- long-context reliability — 10 %
- consistency across tasks — 10 %

**What winning looks like:**
- vysoká úspěšnost na interních coding tasks
- rozumná rychlost v IDE / CI workflow
- jasný fallback pro levnější operace

**Decision outputs to show:**
- best coding quality
- best cost-performance for daily usage
- best long-context option

**Why this scorecard matters:**
U coding týmů dává smysl testovat, jestli produkt zkrátí čas evaluace natolik, že vznikne realistický placený pilot nebo rozumné cenové pásmo; zatím to ale není potvrzený WTP signál.

### Scorecard C — High-volume extraction / classification

**Buyer:** ops lead / automation owner / consultant

**Primární cíl:**
Zpracovat vysoký objem dokumentů nebo ticketů s dobrým cost-per-successful-task.

**Top decision metrics:**
- extraction accuracy — 30 %
- cost per 10k tasks — 30 %
- latency / throughput — 20 %
- schema adherence / structured output reliability — 15 %
- multilingual performance — 5 %

**What winning looks like:**
- stabilní structured outputs
- nízká cena při vysokém objemu
- dostatečná přesnost bez nutnosti premium modelu všude

**Decision outputs to show:**
- cheapest viable model
- best cost-performance
- premium quality option for edge cases

**Why this scorecard matters:**
Tady se nejrychleji projeví ekonomická hodnota produktu, protože špatná volba modelu okamžitě násobí náklady objemem.

---

## 4. What to validate first

### Must-validate assumptions

1. Kupující opravdu chtějí use-case scorecards, ne jen obecný leaderboard.
2. Největší hodnota je v decision support, ne v observability detailu.
3. Pricing pásmo kolem **€149/měs** je potřeba teprve potvrdit jako realistický sweet spot pro AI startupy a agentury; zatím je to testovaná hypotéza, ne potvrzený willingness-to-pay signál.
4. Interní eval import výrazně zvyšuje perceived value.

### Fast experiments

1. Landing page se 3 CTA variantami
2. 10-15 discovery callů podle prioritních ICP
3. Ručně připravený scorecard/report pro 3 design partners
4. Test ceny: free report vs **€39 self-serve** vs **testovaný workspace v pásmu €99-149**

---

## 5. Enrichment milestone status

Po tomto dokumentu je enrichment prakticky připravený na uzavření. Chybí už hlavně reálná validace venku:
- domluvit první rozhovory
- pustit landing page smoke test
- získat reakce na 3 use-case scorecards
