# Wave 1 Outreach Batch - multi-llm-benchmark-dashboard

## Purpose

Prevest shortlist do **ready-to-send batch** rozdeleneho podle realne testovaneho framingu a CTA:
- `dashboard` + `demo`
- `scorecard` + `sample scorecard`
- `memo` + `executive feedback`

Tento dokument je schvalne prakticky: kdo je nejlepsi prvni kontakt, pres jaky kanal jit, jaky framing ma dostat, jaky 1. message angle poslat a jaky artifact poslat jako prvni nebo fallback.

Zdroj pravdy pro rozdeleni je `DISCOVERY-TRACKER.md`.

## Source-of-truth note

Tento batch je operacni vyber pro odeslani, ne primarni misto pro rozhodovani o buyer routing logice.

Plati toto poradi pravdy:
1. `ENRICHMENT.md` drzi market context, ICP a buyer-situation definice
2. `DISCOVERY-TRACKER.md` drzi kanonicke prirazeni firem ke framingu, CTA a buyer situaci
3. `execution/WAVE1-ARTIFACT-MAPPING.md` drzi kanonicke prirazeni primary/fallback artifactu
4. tento batch jen sklada ready-to-send kombinace kontakt + kanal + framing + CTA pro Wave 1

Kdyz se zmeni routing, CTA nebo artifact mapping, nejdriv aktualizovat kanonicky zdroj a az potom tento batch. Tento dokument nema sam menit buyer-situation definice ani prepisovat canonical framing assignment.

---

## Batch A - dashboard framing + demo CTA

Pouzit tam, kde cekame vyssi engineering ownership a zajem o compare workflow. Buyer situation: lead uz ma evaly nebo traces, ale chybi finalni rozhodnuti.

| Firma | Primary contact | Backup | Kanal | Buyer situation | Use case angle | Framing | CTA | Primary artifact | Fallback artifact |
|---|---|---|---|---|---|---|---|---|---|
| Khan Academy | Walt Wells - Staff Software Engineer | AI learning lead | LinkedIn | ma evaly nebo quality signals, ale chybi finalni rozhodnuti | tutoring quality vs cost | dashboard | ask for 20min demo call | SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md |
| Dropbox | Josh Clemm - VP of Engineering | AI search / evaluation lead | LinkedIn | ma evaly nebo quality signals, ale chybi finalni rozhodnuti | AI search eval merge | dashboard | ask for 20min demo call | SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md |
| Notion | Sarav Bhatia - Sr. Dir. of Engineering | AI / engineering lead | LinkedIn + request demo | ma evaly nebo quality signals, ale chybi finalni rozhodnuti | multi-model decision workflow | dashboard | ask for 20min demo call | SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md |
| Zapier | Mike Knoop - Co-Founder | AI product / platform lead | LinkedIn + contact sales | ma evaly nebo quality signals, ale chybi finalni rozhodnuti | multi-model operations | dashboard | ask for 20min demo call | SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md |
| Fintool | Paul Klein IV - Founder & CEO | VP Engineering / AI platform lead | LinkedIn + company site | ma evaly nebo routing signals, ale chybi finalni rozhodnuti | eval + routing decisions | dashboard | ask for 20min demo call | SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md |
| Canva | Andreas Schuster - Head of Product, AI Help Experience | Applied AI lead | LinkedIn | ma evaly nebo support quality signals, ale chybi finalni rozhodnuti | support assistant compare workflow | dashboard | ask for 20min demo call | SAMPLE-DASHBOARD-SUPPORT-ASSISTANT.md | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md |

### Dashboard message skeleton

Ahoj {{first_name}},

resim validation pro **decision dashboard**, ktery srovna GPT / Claude / Gemini a dalsi modely podle konkretniho use case - kvalita, cena, latence a fallback v jednom compare view.

U vas mi to dava smysl hlavne pro **{{use_case}}**, kde se model choice rychle propisuje do kvality i nakladu.

Nejde mi o dalsi leaderboard. Spis o workflow, kde tym behem par minut vidi:
- best overall
- best budget pick
- safest fallback
- co se zmenilo proti poslednimu rozhodnuti

Daval by ti smysl kratky 20min call? Kdyz ne, poslu klidne i jednu scorecard pro vas use case a staci strucny feedback.

---

## Batch B - scorecard framing + sample CTA

Pouzit tam, kde chceme nizsi treni a konkretni use-case vstup do konverzace. Buyer situation: buyer rychle porovnava modely pro novy use case, resi budget ceiling nebo hleda lightweight vrstvu pred plnym LLMOps stackem.

| Firma | Primary contact | Backup | Kanal | Buyer situation | Use case angle | Framing | CTA | Primary artifact | Fallback artifact |
|---|---|---|---|---|---|---|---|---|---|
| Magic Patterns | Alexander Danilowicz - Co-founder | product / GTM co-founder | LinkedIn + company site | rychle porovnava modely pro novy use case | coding + product workflow | scorecard | send sample scorecard | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md | SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md |
| SumUp | Ana Casado - Head of Operations Data and AI | AI reliability lead | LinkedIn | resi budget ceiling a fallback model | support + fallback scorecard | scorecard | send sample scorecard | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md | SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md |
| Graphite | Quinten Farmer - Founder & CEO | CTO / AI engineering lead | LinkedIn + request demo | rychle porovnava modely pro novy use case | coding assistant wedge | scorecard | send sample scorecard | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md | SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md |
| Loom | Matt Granmoe - Senior Software Engineer | AI product lead | LinkedIn + Atlassian path | hleda lightweight vrstvu pred plnym LLMOps stackem | high-volume AI workflow | scorecard | send sample scorecard | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md | SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md |
| Canva | Andreas Schuster - Head of Product, AI Help Experience | Applied AI lead | LinkedIn | rychle porovnava modely pro novy use case | support assistant scorecard | scorecard | send sample scorecard | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md | SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md |
| SumUp | Ana Casado - Head of Operations Data and AI | AI reliability lead | LinkedIn | resi budget ceiling a fallback model | budget + fallback scorecard | scorecard | send sample scorecard | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md | SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md |

### Scorecard message skeleton

Ahoj {{first_name}},

overuju, jestli AI tymy chteji **use-case scorecards** pro vyber LLM modelu misto obecneho leaderboardu.

U vas mi to sedi hlavne na **{{use_case}}**.

Myslenka je jednoducha: vzit verejne benchmarky, pricing a pripadne interni eval signaly a ukazat v jedne scorecard:
- best overall
- best budget
- safest fallback
- kde je tradeoff kvalita vs cena vs latence

Jestli chces, poslu 1 ukazkovou scorecard pro vas use case. Staci mi pak kratky feedback, jestli je to uzitecne nebo mimo.

---

## Batch C - memo framing + executive feedback CTA

Pouzit tam, kde je silnejsi governance, ROI a explainability angle. Buyer situation: buyer potrebuje obhajit volbu modelu pred managementem nebo klientem.

| Firma | Primary contact | Backup | Kanal | Buyer situation | Use case angle | Framing | CTA | Primary artifact | Fallback artifact |
|---|---|---|---|---|---|---|---|---|---|
| Merck | Walid Mehanna - Chief Data & AI Officer | AI platform / governance owner | LinkedIn | potrebuje obhajit volbu modelu pred managementem nebo klientem | governance + benchmark memo | memo | ask for executive feedback | SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md |
| Coursera | Winne Tam - Senior Engineering Manager | Sophie Gao - Staff Software Engineer | LinkedIn + leadership path | potrebuje obhajit volbu modelu pred managementem nebo klientem | explainable model choice for learning tools | memo | ask for executive feedback | SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md |
| Ramp | Ben Levick - Head of AI & Operations | finance automation / AI product lead | LinkedIn + demo/contact path | potrebuje obhajit volbu modelu pred managementem nebo klientem | productivity + cost memo | memo | ask for executive feedback | SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md | SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md |

### Memo message skeleton

Ahoj {{first_name}},

resim validation pro lehky **decision memo layer** nad LLM stackem - neco mezi executive memo a engineering dashboardem.

Cil: aby slo obhajit, **proc je pro konkretni use case nejlepsi prave tenhle model**, a to podle kvality, ceny, latence a fallback strategie.

Mluvim hlavne s tymy, ktere uz AI provozuji ve vetsim meritku a musi delat opakovana rozhodnuti kolem model selection nebo governance.

Kdyby to bylo relevantni, rad poslu 1 ukazkovy decision memo / scorecard pro vas use case, nebo dame kratky 20min call.

---

## Buyer-situation routing shortcut

Pouzij batch podle buyer situace bez dalsi interpretace:
- `dashboard` batch = lead uz ma evaly, traces nebo compare workflow, ale chybi finalni rozhodnuti
- `scorecard` batch = lead rychle porovnava modely pro novy use case, resi budget/fallback nebo chce lightweight vrstvu
- `memo` batch = lead potrebuje rozhodnuti obhajit pred managementem, klientem nebo governance vrstvou

Kdyz je signal smiseny, zacni `scorecard`, priprav `memo` jako fallback pro executive follow-up a `dashboard` nech pro leady s jasnym opakovaným compare workflow.

---

## Consistency check against tracker

Wave 1 batch ma byt konzistentni s `DISCOVERY-TRACKER.md` v techto bodech:
- `dashboard` leady maji dostat dashboard-first message a demo CTA
- `scorecard` leady maji dostat scorecard-first message a sample CTA
- `memo` leady maji dostat executive / memo-first message
- duplicity typu `Canva` a `SumUp` jsou zamerne - testuje se jina zprava pro jiny use-case angle

Pokud se tracker zmeni, nejdriv aktualizovat tracker a teprve potom tento batch.

---

## Send order recommendation

### Canonical first-5 live send order

Pokud se posila prvni realna vlna bez dalsi reinterpretace, drzet tento canonical subset:
1. SumUp - Ana Casado
2. Magic Patterns - Alexander Danilowicz
3. Canva - Andreas Schuster
4. Graphite - Quinten Farmer
5. Notion - Sarav Bhatia

Tento subset je zamerne sladěny s:
- `execution/WAVE1-LIVE-EVIDENCE-BOARD.md`
- `execution/WAVE1-FIRST5-SEND-PACKET.md`
- `execution/WAVE1-TIMING-TRIGGERS.md`
- `execution/WAVE1A-PERSONALIZED-SKELETONS.md`

Poznamka: `Canva` je v tomto first-5 subsetu vedena pres `scorecard`, ne pres sirsi `dashboard` variantu. Duvod je rychlejsi `budget_fallback` reply signal v prvni mikro-vlne.

### Remaining Wave 1A queue after first-5
6. Khan Academy - Walt Wells
7. Merck - Walid Mehanna
8. Fintool - Paul Klein IV
9. Ramp - Ben Levick

### Wave 1B - verified accounts, mixed contact confidence
1. Dropbox - Josh Clemm
2. Coursera - Winne Tam / Sophie Gao
3. Zapier - Mike Knoop
4. Loom - Matt Granmoe

Duvod: verejne customer pages potvrzuji Wave 1B account fit, ale ne u vsech firem potvrzuji i konkretni named contact. Batch tedy neni blokovany account selection, ale ma mixed contact confidence a musi se ridit `execution/WAVE1-CONTACT-VERIFICATION.md`.

---

## Pricing signal handoff for Wave 1

Po kazde relevantni reply nebo call z teto vlny zapis pricing signal do `execution/OUTREACH-LOG-TEMPLATE.md` bez vlastniho preznacovani. Pouzij presne tyto hodnoty, aby batch, log a verdict vrstva mely stejnou slovni zasobu end-to-end:
- `price_probe = none / under_39 / 39_149 / 149_plus / enterprise`
- `pro_signal = positive / neutral / negative`
- 1 presnou vetu nebo frazi, ktera pricing signal potvrzuje

Wave 1 batch nema zavadet zadne alternativni pricing labely. Pokud buyer rekne napriklad, ze chce jen jednorazovy audit nebo free artifact, routuj to do `price_probe` a `pro_signal` podle log template misto volneho slovniho popisu.

---

## Operational notes

- **Nejvyssi confidence verejne osoby** jsou rozlisene v `execution/WAVE1-CONTACT-VERIFICATION.md` na `person_verified` vs `account_verified` podle verejneho dukazu.
- Kde je named contact z customer story, je mozne poslat personalizovany outreach hned.
- Kdyz jmeno chybi, stale je mozne spustit account-based outreach pres role + firmu bez blokace cele vlny.
- Nejrychlejsi dalsi krok po tomto batchi: spustit outreach na Wave 1A a parallelne otestovat reply quality po framingu `dashboard` vs `scorecard` vs `memo`.
