# Outreach Log Template — multi-llm-benchmark-dashboard

## Purpose

Jednoduchý log pro první validační vlnu, aby šlo po odeslání rychle vyhodnotit:
- který framing funguje líp
- které CTA získává kvalitnější odpovědi
- který segment má nejvyšší pain a purchase intent
- který artifact byl reálně poslaný a který artifact lead reálně vytáhl v první odpovědi

Držet to schválně lehké. Žádný CRM overkill.

---

## Status values
- drafted
- sent
- follow_up_1
- follow_up_2
- replied
- booked
- completed
- disqualified

## Reply quality values
- none
- weak
- relevant
- high_intent

## Preferred artifact values
- dashboard
- scorecard
- memo
- report
- API
- hybrid
- unknown

## Suggested columns

| Date | Company | Contact | Segment | Framing | CTA | Channel | Status | Sent artifact | First reply artifact | Reply quality | Preferred artifact | Pain (1-5) | WTP band | Next step | Notes / exact phrasing |
|---|---|---|---|---|---|---|---|---|---|---|---|---:|---|---|---|
| YYYY-MM-DD | Canva | Andreas Schuster | SaaS s AI feature | dashboard | demo | LinkedIn | drafted | dashboard | unknown | none | unknown | 4 | enterprise | send first message | |
| YYYY-MM-DD | Khan Academy | Walt Wells | SaaS s AI feature | dashboard | demo | LinkedIn | drafted | dashboard | unknown | none | unknown | 4 | 149_plus | send first message | |
| YYYY-MM-DD | Magic Patterns | Alexander Danilowicz | AI startup | scorecard | sample scorecard | LinkedIn | drafted | scorecard | unknown | none | unknown | 5 | 149_plus | send first message | |
| YYYY-MM-DD | Merck | Walid Mehanna | Enterprise innovation | memo | executive feedback | LinkedIn | drafted | memo | unknown | none | unknown | 4 | enterprise | send first message | |
| YYYY-MM-DD | SumUp | Ana Casado | SaaS s AI feature | scorecard | sample scorecard | LinkedIn | drafted | scorecard | unknown | none | unknown | 5 | enterprise | send first message | |

---

## How to use after each touch

### After send
Zapsat jen:
- date
- status = sent
- framing
- CTA
- channel
- sent artifact = co šlo ven jako první skutečný asset

**Poznámka pro execution:** `framing`, `CTA` a `sent artifact` se mají opsat z finálního Wave 1 routingu bez vlastní reinterpretace — source of truth je `WAVE1-OUTREACH-BATCH.md` a konkrétní personalizace ve `WAVE1A-PERSONALIZED-SKELETONS.md` / `WAVE1B-PERSONALIZED-SKELETONS.md`. Do logu se až po odeslání doplňuje jen skutečný kanál a případná odchylka, ne nový routing.

### After reply
Dopsat:
- reply quality
- first reply artifact = který artifact lead výslovně zmínil nebo otevřel jako první
- preferred artifact
- 1 přesnou větu nebo frázi, kterou lead použil
- strongest objection nebo requested next step

### After call
Dopsat navíc:
- pain (1-5)
- WTP band
- jestli chtějí pilot / sample / intro / nic

---

## Minimum analysis after first wave

Po první vlně stačí sečíst 5 věcí:
1. počet odpovědí podle framingu
2. počet kvalitních odpovědí podle CTA
3. které firmy chtějí dashboard vs scorecard vs memo
4. který sent artifact přinesl nejvíc reply quality
5. které exact phrasing se opakuje napříč odpověďmi

To stačí pro rozhodnutí, jestli je silnější:
- dashboard-first
- scorecard-first
- hybrid dashboard + memo
