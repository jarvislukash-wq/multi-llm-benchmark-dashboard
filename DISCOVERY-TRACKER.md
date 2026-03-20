# Discovery Tracker - multi-llm-benchmark-dashboard

> Poznamka: nize je **wave 1 account list** pro prvni outreach. Jde o account-level targety a cilove role. `Public contact` neznamena automaticky verejne overene jmeno; presny dukaz je v `execution/WAVE1-CONTACT-VERIFICATION.md`, kde je rozlisene `person_verified` vs `account_verified`. Kde zatim verejne jmeno chybi nebo neslo spolehlive overit bez loginu, je uveden **role-based fallback** a prioritni kanal. Sloupce `Pain`, `Pricing band` a `Preferred format` jsou pracovni hypotezy pro prioritizaci outreach, ne potvrzena fakta.

## Interview tracker

| Lead | Firma | Segment | Public contact | Backup contact / role | Channel | Priorita | Stav | Pain (1-5) | Models 3+ | Pricing band | Preferred format | Framing to test | Next step |
|---|---|---|---|---|---|---|---|---:|---|---|---|---|---|
| AI Help Experience owner | Canva | SaaS s AI feature | Andreas Schuster - Head of Product, AI Help Experience | Applied AI / platform engineering lead | LinkedIn + Canva engineering / product channels | P1 | to_contact | 4 | yes | enterprise | hybrid | scorecard | send scorecard CTA for support assistant use case |
| AI tutoring platform lead | Khan Academy | SaaS s AI feature | Walt Wells - Staff Software Engineer | AI learning lead / engineering manager | LinkedIn + Khan Academy leadership / engineering channel | P1 | to_contact | 4 | yes | 149_plus | dashboard | dashboard | send demo CTA focused on quality vs cost tradeoff |
| Product prototyping founder | Magic Patterns | AI startup | Alexander Danilowicz - Co-founder | Product / GTM co-founder | LinkedIn + company site contact | P1 | to_contact | 5 | yes | 149_plus | dashboard | scorecard | send scorecard CTA for coding + product workflow |
| AI platform owner | Merck | Enterprise innovation | Walid Mehanna - Chief Data & AI Officer | AI platform / governance owner | LinkedIn + enterprise innovation contact path | P2 | to_contact | 4 | yes | enterprise | hybrid | memo | send executive CTA with governance + benchmark angle |
| Support AI operations lead | SumUp | SaaS s AI feature | Ana Casado - Head of Operations Data and AI | AI engineering / reliability lead | LinkedIn + SumUp about/jobs/contact path | P1 | to_contact | 5 | yes | enterprise | hybrid | scorecard | send scorecard CTA for support / fallback decisions |
| AI search eval owner | Dropbox | SaaS s AI feature | Josh Clemm - VP of Engineering | AI search / evaluation engineering lead | LinkedIn + Dropbox leadership / AI product path | P1 | to_contact | 5 | yes | enterprise | dashboard | dashboard | send demo CTA with internal eval merge angle |
| Workspace AI platform lead | Notion | SaaS s AI feature | Sarav Bhatia - Sr. Dir. of Engineering | AI / engineering lead | LinkedIn + Notion request-demo / product leadership path | P1 | to_contact | 5 | yes | enterprise | hybrid | dashboard | send demo CTA focused on model-selection workflow |
| AI code review owner | Graphite | AI startup | Quinten Farmer - Founder & CEO | CTO / AI engineering lead | LinkedIn + Graphite request-demo | P1 | to_contact | 5 | yes | 149_plus | dashboard | scorecard | send scorecard CTA for coding assistant wedge |
| Learning AI platform lead | Coursera | SaaS s AI feature | Winne Tam - Senior Engineering Manager *(account-verified only)* | Sophie Gao - Staff Software Engineer | LinkedIn + Coursera leadership / engineering path | P2 | research_needed | 4 | yes | enterprise | hybrid | memo | verify named contact or use role-based fallback before send |
| AI orchestration lead | Zapier | SaaS s AI feature | Mike Knoop - Co-Founder *(account-verified only)* | AI product / platform lead | LinkedIn + Zapier contact sales | P1 | research_needed | 5 | yes | enterprise | dashboard | dashboard | verify named contact or use role-based fallback before send |
| AI video workflow lead | Loom | SaaS s AI feature | Matt Granmoe - Senior Software Engineer *(account-verified only)* | AI product lead | LinkedIn + Atlassian/Loom contact path | P2 | research_needed | 4 | yes | 149_plus | report | scorecard | verify named contact or use role-based fallback before send |
| Financial AI engineering lead | Fintool | AI startup | Paul Klein IV - Founder & CEO | VP Engineering / AI platform lead | LinkedIn + company site contact | P1 | to_contact | 5 | yes | enterprise | dashboard | dashboard | send demo CTA focused on eval + routing decisions |
| Internal AI automation owner | Ramp | SaaS s AI feature | Ben Levick - Head of AI & Operations | Finance automation / AI product lead | LinkedIn + Ramp contact/demo path | P1 | to_contact | 4 | yes | enterprise | hybrid | memo | send executive CTA with productivity + cost angle |
| Applied AI engineering lead | Canva | SaaS s AI feature | Andreas Schuster - Head of Product, AI Help Experience | Applied AI / platform engineering lead | LinkedIn + Canva engineering / product channels | P2 | to_contact | 4 | yes | enterprise | dashboard | dashboard | send demo CTA focused on compare workflow |
| Reliability / fallback owner | SumUp | SaaS s AI feature | Ana Casado - Head of Operations Data and AI | AI engineering / reliability lead | LinkedIn + SumUp about/jobs/contact path | P2 | to_contact | 5 | yes | enterprise | hybrid | scorecard | send scorecard CTA for budget + fallback scorecard |

### Status values
- to_contact
- contacted
- replied
- booked
- completed
- disqualified
- follow_up
- research_needed

### Preferred format values
- dashboard
- report
- API
- hybrid

### Pricing band values
- none
- under_39
- 39_149
- 149_plus
- enterprise

---

## Public contact evidence

Zdroj pravdy pro confidence level je `execution/WAVE1-CONTACT-VERIFICATION.md`. Nize uvedene zdroje ukazuji puvod account poolu; ne vsechny automaticky potvrzuji i named contact.


- **Langfuse customer stories:**
  - Canva - Andreas Schuster, Head of Product, AI Help Experience
  - Khan Academy - Walt Wells, Staff Software Engineer
  - Magic Patterns - Alexander Danilowicz, Co-founder
  - Merck - Walid Mehanna, Chief Data & AI Officer
  - SumUp - Ana Casado, Head of Operations Data and AI
- **Braintrust customers / stories:**
  - Dropbox - Josh Clemm, VP of Engineering
  - Notion - Sarav Bhatia, Sr. Dir. of Engineering
  - Graphite - Quinten Farmer, Founder & CEO
  - Coursera - Winne Tam, Senior Engineering Manager; Sophie Gao, Staff Software Engineer
  - Zapier - Mike Knoop, Co-Founder
  - Loom - Matt Granmoe, Senior Software Engineer
  - Fintool - Paul Klein IV, Founder & CEO
- **Notion AI page:**
  - Ramp - Ben Levick, Head of AI & Operations

---

## Landing page tracker

| Date | Variant | Channel | Visits | CTA clicks | Form submits | Submit rate | Notes |
|---|---|---|---:|---:|---:|---:|---|
| YYYY-MM-DD | B | outreach / organic / social | 0 | 0 | 0 | 0 % | |

---

## Interview notes template

### Lead
- Name:
- Company:
- Role:
- Segment:
- Date:

### Context
- Main AI use case:
- Number of models/providers used:
- Who decides model choice:

### Current workflow
- How they choose models today:
- Where benchmark data comes from:
- Whether they use internal evals:

### Pain points
- Biggest frustration:
- Last painful model-switch decision:
- What is hard to explain internally:

### Reaction to concept
- Framing shown: dashboard / scorecard / memo
- Response to framing:
- Response to use-case scorecards:
- Response to public + internal data merge:
- Strongest objection:

### Commercial signal
- Would they pay:
- Expected format:
- Price reaction:
- Interest in pilot/demo:

### Scoring
- Problem intensity (1-5):
- Workflow chaos (1-5):
- Purchase intent (1-5):
- Scorecard fit (1-5):
- Total:

### Next step
- Follow-up action:
- Owner:
- Deadline:
