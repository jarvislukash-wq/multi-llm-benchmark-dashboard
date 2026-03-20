# Wave 1 Contact Verification — multi-llm-benchmark-dashboard

## Purpose

Oddelit **account verification** od **person verification**, aby Wave 1 outreach nestal na nepresnych tvrzenich o verejne dohledanych osobach.

Tento dokument je evidence vrstva pro verejne zdroje, ne routing dokument.

**Source-of-truth note:** tenhle dokument rozhoduje jen o verification confidence (`person_verified` / `account_verified` / `source_claim_only`). Nesmí měnit `buyer situation`, `framing`, `CTA` ani artifact assignment — ty zůstávají v `DISCOVERY-TRACKER.md`, `execution/WAVE1-OUTREACH-BATCH.md` a odpovídajících Wave 1 skeletons / fallback dokumentech. Pokud je contact status slabší než dřív, mění se jen forma oslovení, ne routing logika.

---

## Verification statuses

- `person_verified` = verejny zdroj potvrzuje firmu i konkretni jmeno
- `account_verified` = verejny zdroj potvrzuje firmu / customer story, ale ne konkretni jmeno pouzite v outreachu
- `source_claim_only` = jmeno je v projektu uvedene, ale tento dokument zatim nema ulozeny verejny dukaz

---

## Verification matrix

| Company | Contact in Wave 1 | Source | Status | Notes |
|---|---|---|---|---|
| Canva | Andreas Schuster | Langfuse customers | person_verified | firma i jmeno potvrzene na verejne customer page |
| Khan Academy | Walt Wells | Langfuse customers | person_verified | firma i jmeno potvrzene na verejne customer page |
| Magic Patterns | Alexander Danilowicz | Langfuse customers | person_verified | firma i jmeno potvrzene na verejne customer page |
| Merck | Walid Mehanna | Langfuse customers | person_verified | firma i jmeno potvrzene na verejne customer page |
| SumUp | Ana Casado | Langfuse customers | person_verified | firma i jmeno potvrzene na verejne customer page |
| Dropbox | Josh Clemm | Braintrust customers | person_verified | firma i jmeno potvrzene na verejne customer page |
| Notion | Sarav Bhatia | Braintrust customers | person_verified | firma i jmeno potvrzene na verejne customer page |
| Graphite | Quinten Farmer | Braintrust customers | person_verified | firma i jmeno potvrzene na verejne customer page |
| Fintool | Paul Klein IV | Braintrust customers | person_verified | firma i jmeno potvrzene na verejne customer page |
| Ramp | Ben Levick | Notion AI page | person_verified | firma i jmeno potvrzene na verejne product page |
| Coursera | Winne Tam | Braintrust customers | account_verified | customer page potvrzuje Coursera, ale ne toto jmeno v nactenem verejnem obsahu |
| Zapier | Mike Knoop | Braintrust customers | account_verified | customer page potvrzuje Zapier, ale ne toto jmeno v nactenem verejnem obsahu |
| Loom | Matt Granmoe | Braintrust customers | account_verified | customer page potvrzuje Loom, ale ne toto jmeno v nactenem verejnem obsahu |

---

## Practical execution rule

- `person_verified` lead lze drzet jako named-contact outreach, pokud routing zustava stejny.
- `account_verified` lead se ma brat jako **account-level target s role-based fallbackem**; named contact v trackeru je jen pracovni kandidat, ne overeny fakt.
- Kdyz se objevi novy verejny dukaz pro konkretni osobu, nejdriv aktualizovat tento dokument a teprve potom zvednout confidence v batchi nebo trackeru.

---

## Current implication for Wave 1B

Wave 1B uz neni blokovany account selection, ale neni korektni ho popisovat jako plne `verified public contacts`.

Presnejsi stav:
- Dropbox = person-verified
- Coursera = account-verified
- Zapier = account-verified
- Loom = account-verified
