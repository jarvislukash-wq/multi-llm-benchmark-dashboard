# Wave 1 Outreach Batch - multi-llm-benchmark-dashboard

## Purpose

Prevest shortlist do **ready-to-send batch** rozdeleneho podle realne testovaneho framingu a CTA:
- `dashboard` + `demo`
- `scorecard` + `sample scorecard`
- `memo` + `executive feedback`

Tento dokument je schvalne prakticky: kdo je nejlepsi prvni kontakt, pres jaky kanal jit, jaky framing ma dostat a jaky 1. message angle poslat.

Zdroj pravdy pro rozdeleni je `DISCOVERY-TRACKER.md`.

---

## Batch A - dashboard framing + demo CTA

Pouzit tam, kde cekame vyssi engineering ownership a zajem o compare workflow.

| Firma | Primary contact | Backup | Kanal | Use case angle | Framing | CTA |
|---|---|---|---|---|---|---|
| Khan Academy | Walt Wells - Staff Software Engineer | AI learning lead | LinkedIn | tutoring quality vs cost | dashboard | ask for 20min demo call |
| Dropbox | Josh Clemm - VP of Engineering | AI search / evaluation lead | LinkedIn | AI search eval merge | dashboard | ask for 20min demo call |
| Notion | Sarav Bhatia - Sr. Dir. of Engineering | AI / engineering lead | LinkedIn + request demo | multi-model decision workflow | dashboard | ask for 20min demo call |
| Zapier | Mike Knoop - Co-Founder | AI product / platform lead | LinkedIn + contact sales | multi-model operations | dashboard | ask for 20min demo call |
| Fintool | Paul Klein IV - Founder & CEO | VP Engineering / AI platform lead | LinkedIn + company site | eval + routing decisions | dashboard | ask for 20min demo call |
| Canva | Andreas Schuster - Head of Product, AI Help Experience | Applied AI lead | LinkedIn | support assistant compare workflow | dashboard | ask for 20min demo call |

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

Pouzit tam, kde chceme nizsi treni a konkretni use-case vstup do konverzace.

| Firma | Primary contact | Backup | Kanal | Use case angle | Framing | CTA |
|---|---|---|---|---|---|---|
| Magic Patterns | Alexander Danilowicz - Co-founder | product / GTM co-founder | LinkedIn + company site | coding + product workflow | scorecard | send sample scorecard |
| SumUp | Ana Casado - Head of Operations Data and AI | AI reliability lead | LinkedIn | support + fallback scorecard | scorecard | send sample scorecard |
| Graphite | Quinten Farmer - Founder & CEO | CTO / AI engineering lead | LinkedIn + request demo | coding assistant wedge | scorecard | send sample scorecard |
| Loom | Matt Granmoe - Senior Software Engineer | AI product lead | LinkedIn + Atlassian path | high-volume AI workflow | scorecard | send sample scorecard |
| Canva | Andreas Schuster - Head of Product, AI Help Experience | Applied AI lead | LinkedIn | support assistant scorecard | scorecard | send sample scorecard |
| SumUp | Ana Casado - Head of Operations Data and AI | AI reliability lead | LinkedIn | budget + fallback scorecard | scorecard | send sample scorecard |

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

Pouzit tam, kde je silnejsi governance, ROI a explainability angle.

| Firma | Primary contact | Backup | Kanal | Use case angle | Framing | CTA |
|---|---|---|---|---|---|---|
| Merck | Walid Mehanna - Chief Data & AI Officer | AI platform / governance owner | LinkedIn | governance + benchmark memo | memo | ask for executive feedback |
| Coursera | Winne Tam - Senior Engineering Manager | Sophie Gao - Staff Software Engineer | LinkedIn + leadership path | explainable model choice for learning tools | memo | ask for executive feedback |
| Ramp | Ben Levick - Head of AI & Operations | finance automation / AI product lead | LinkedIn + demo/contact path | productivity + cost memo | memo | ask for executive feedback |

### Memo message skeleton

Ahoj {{first_name}},

resim validation pro lehky **decision memo layer** nad LLM stackem - neco mezi executive memo a engineering dashboardem.

Cil: aby slo obhajit, **proc je pro konkretni use case nejlepsi prave tenhle model**, a to podle kvality, ceny, latence a fallback strategie.

Mluvim hlavne s tymy, ktere uz AI provozuji ve vetsim meritku a musi delat opakovana rozhodnuti kolem model selection nebo governance.

Kdyby to bylo relevantni, rad poslu 1 ukazkovy decision memo / scorecard pro vas use case, nebo dame kratky 20min call.

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

### Wave 1A - highest confidence contacts
1. Canva - Andreas Schuster
2. Khan Academy - Walt Wells
3. Magic Patterns - Alexander Danilowicz
4. Merck - Walid Mehanna
5. SumUp - Ana Casado
6. Notion - Sarav Bhatia
7. Graphite - Quinten Farmer
8. Fintool - Paul Klein IV
9. Ramp - Ben Levick

### Wave 1B - now verified public contacts
1. Dropbox - Josh Clemm
2. Coursera - Winne Tam / Sophie Gao
3. Zapier - Mike Knoop
4. Loom - Matt Granmoe

Duvod: exact company match jsem dohledal primo z verejnych Braintrust customer story stranek, takze batch uz neni blokovany jmennou verifikaci.

---

## Operational notes

- **Nejvyssi confidence verejne osoby** pochazi z Langfuse customer page, Braintrust customer page a Notion AI page.
- Kde je named contact z customer story, je mozne poslat personalizovany outreach hned.
- Kdyz jmeno chybi, stale je mozne spustit account-based outreach pres role + firmu bez blokace cele vlny.
- Nejrychlejsi dalsi krok po tomto batchi: spustit outreach na Wave 1A a parallelne otestovat reply quality po framingu `dashboard` vs `scorecard` vs `memo`.
