# Wave 1 Outreach Batch - multi-llm-benchmark-dashboard

## Purpose

Prevest shortlist do **ready-to-send batch** rozdeleneho podle CTA:
- `demo`
- `scorecard`
- `executive-hybrid`

Tento dokument je schvalne prakticky: kdo je nejlepsi prvni kontakt, pres jaky kanal jit a jaky 1. message angle poslat.

---

## Batch A - demo CTA

Pouzit tam, kde cekame vyssi engineering ownership a zajem o compare workflow.

| Firma | Primary contact | Backup | Kanal | Use case angle | CTA |
|---|---|---|---|---|---|
| Khan Academy | Walt Wells - Staff Software Engineer | AI learning lead | LinkedIn | tutoring quality vs cost | ask for 20min demo call |
| Dropbox | AI search / evaluation lead *(name pending verification)* | Luis Hector Chavez - CTO *(company match pending)* | LinkedIn | AI search eval merge | ask for 20min demo call |
| Notion | Sarav Bhatia - Sr. Dir. of Engineering | AI / engineering lead | LinkedIn + request demo | multi-model decision workflow | ask for 20min demo call |
| Zapier | AI product / platform lead *(name pending verification)* | Mohsen Sardari - VP Engineering *(company match pending)* | LinkedIn + contact sales | multi-model operations | ask for 20min demo call |
| Fintool | Paul Klein IV - Founder & CEO | VP Engineering / AI platform lead | LinkedIn + company site | eval + routing decisions | ask for 20min demo call |
| Canva | Andreas Schuster - Head of Product, AI Help Experience | Applied AI lead | LinkedIn | support assistant compare workflow | ask for 20min demo call |

### Demo message skeleton

Ahoj {{first_name}},

resim validation pro decision dashboard, ktery srovna GPT / Claude / Gemini a dalsi modely podle konkretniho use case - kvalita, cena, latence a fallback v jedne scorecard.

U vas mi to dava smysl hlavne pro **{{use_case}}**, kde se model choice rychle propisuje do kvality i nakladu.

Nejde mi o dalsi leaderboard. Spis o workflow, kde tym behem par minut vidi:
- best overall
- best budget pick
- safest fallback
- co se zmenilo proti poslednimu rozhodnuti

Daval by ti smysl kratky 20min call? Kdyz ne, poslu klidne i jednu scorecard pro vas use case a staci strucny feedback.

---

## Batch B - scorecard CTA

Pouzit tam, kde chceme nizsi treni a konkretni use-case vstup do konverzace.

| Firma | Primary contact | Backup | Kanal | Use case angle | CTA |
|---|---|---|---|---|---|
| Magic Patterns | Alexander Danilowicz - Co-founder | product / GTM co-founder | LinkedIn + company site | coding + product workflow | send sample scorecard |
| SumUp | Ana Casado - Head of Operations Data and AI | AI reliability lead | LinkedIn | support + fallback scorecard | send sample scorecard |
| Graphite | Quinten Farmer - Founder & CEO | CTO / AI engineering lead | LinkedIn + request demo | coding assistant wedge | send sample scorecard |
| Loom | AI product lead *(name pending verification)* | Allen Kleiner - AI Engineering Lead *(company match pending)* | LinkedIn + Atlassian path | high-volume AI workflow | send sample scorecard |
| Coursera | Mustafa Furniturewala - CTO | Josh Clemm - VP Engineering *(company match pending)* | LinkedIn + leadership path | explainable model choice for learning tools | send sample scorecard |
| Canva | Andreas Schuster - Head of Product, AI Help Experience | Applied AI lead | LinkedIn | support assistant scorecard | send sample scorecard |
| SumUp | Ana Casado - Head of Operations Data and AI | AI reliability lead | LinkedIn | budget + fallback scorecard | send sample scorecard |

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

## Batch C - executive-hybrid CTA

Pouzit tam, kde je silnejsi governance, ROI a explainability angle.

| Firma | Primary contact | Backup | Kanal | Use case angle | CTA |
|---|---|---|---|---|---|
| Merck | Walid Mehanna - Chief Data & AI Officer | AI platform / governance owner | LinkedIn | governance + benchmark memo | ask for executive feedback |
| Ramp | Ben Levick - Head of AI & Operations | finance automation / AI product lead | LinkedIn + demo/contact path | productivity + cost memo | ask for executive feedback |

### Executive-hybrid message skeleton

Ahoj {{first_name}},

resim validation pro lehky decision layer nad LLM stackem - neco mezi executive memo a engineering dashboardem.

Cil: aby slo obhajit, **proc je pro konkretni use case nejlepsi prave tenhle model**, a to podle kvality, ceny, latence a fallback strategie.

Mluvim hlavne s tymy, ktere uz AI provozuji ve vetsim meritku a musi delat opakovana rozhodnuti kolem model selection nebo governance.

Kdyby to bylo relevantni, rad poslu 1 ukazkovy decision memo / scorecard pro vas use case, nebo dame kratky 20min call.

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

### Wave 1B - send after one more verification pass
1. Dropbox
2. Coursera
3. Zapier
4. Loom

Duvod: firmy jsou spravne vybrane, ale u konkretniho jmena chci jeste jednou overit exact company match z verejneho zdroje.

---

## Operational notes

- **Nejvyssi confidence verejne osoby** pochazi z Langfuse customer page, Braintrust customer page a Notion AI page.
- Kde je `company match pending`, neposilat personalizovany outreach na jmeno bez dalsiho overeni.
- Kdyz jmeno chybi, stale je mozne spustit account-based outreach pres role + firmu bez blokace cele vlny.
- Nejrychlejsi dalsi krok po tomto batchi: doplnit 4 zbyvajici jmena a rovnou otestovat reply rate `demo` vs `scorecard`.
