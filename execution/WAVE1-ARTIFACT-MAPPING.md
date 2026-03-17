# Wave 1 Artifact Mapping — multi-llm-benchmark-dashboard

## Purpose

Explicitně propojit **konkrétní Wave 1 kontakty** s tím, jaký artifact mají dostat jako první a jaký jako fallback.

Cíl: ať je hned jasné,
- co poslat komu
- jaký framing tím testujeme
- jaký backup artifact použít, když lead nechce call

---

## Mapping rules

| Framing | Primary artifact | Fallback artifact | Kdy použít |
|---|---|---|---|
| dashboard | `execution/SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `execution/SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | když chceme otevřít demo call, ale mít po ruce lehký sample |
| scorecard | `execution/SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `execution/SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | když chceme low-friction vstup přes konkrétní sample |
| memo | `execution/SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | `execution/SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | když lead spíš řeší explainability, governance nebo executive alignment |

---

## Wave 1A — highest confidence contacts

| Company | Contact | Framing | Primary artifact to send | Fallback artifact | Why this pairing |
|---|---|---|---|---|---|
| Canva | Andreas Schuster | dashboard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | support assistant use case je nejblíž hotové scorecard; memo je vhodný second step pro product ownera |
| Khan Academy | Walt Wells | dashboard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | scorecard je nejrychlejší konkrétní ukázka kvalita vs cost tradeoffu |
| Magic Patterns | Alexander Danilowicz | scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | AI-native founder segment má dostat sample-first wedge |
| Merck | Walid Mehanna | memo | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | governance-heavy kontakt spíš ocení recommendation framing než čistý compare sheet |
| SumUp | Ana Casado | scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | operations + support use case sedí na konkrétní scorecard artefakt |
| Notion | Sarav Bhatia | dashboard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | dashboard-first outreach může při odmítnutí callu hned přepnout na scorecard |
| Graphite | Quinten Farmer | scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | founder v coding segmentu dostane nejdřív nízkotřecí sample |
| Fintool | Paul Klein IV | dashboard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | scorecard funguje jako concrete leave-behind k dashboard pitchi |
| Ramp | Ben Levick | memo | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | ops + cost discipline angle sedí na executive memo |

---

## Wave 1B — verified public contacts

| Company | Contact | Framing | Primary artifact to send | Fallback artifact | Why this pairing |
|---|---|---|---|---|---|
| Dropbox | Josh Clemm | dashboard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | dashboard-first, ale sample scorecard je nejrychlejší asset po prvním doteku |
| Coursera | Winne Tam | memo | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | learning/product alignment se lépe vysvětluje přes memo |
| Zapier | Mike Knoop | dashboard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | orchestration-heavy kontakt může chtít workflow call, scorecard je dobrý backup |
| Loom | Matt Granmoe | scorecard | `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md` | `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md` | high-volume workflow segment lépe otevře konkrétní scorecard než memo |

---

## Practical send logic

### If first touch is `dashboard`
1. poslat dashboard-first message
2. pokud lead nechce call, nabídnout nebo poslat `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
3. pokud se ptá na recommendation nebo obhajobu volby, přepnout na memo

### If first touch is `scorecard`
1. poslat sample-first message
2. jako první artifact použít `SAMPLE-SCORECARD-SUPPORT-ASSISTANT.md`
3. pokud lead řeší stakeholder alignment, přepnout na memo

### If first touch is `memo`
1. poslat executive-first message
2. jako první artifact použít `SAMPLE-DECISION-MEMO-SUPPORT-ASSISTANT.md`
3. pokud lead chce víc operativní compare view, poslat scorecard jako doplněk

---

## Next after send

Po prvních reálných odpovědích doplnit do outreach logu navíc:
- který artifact byl skutečně poslaný
- jestli reply quality byla vyšší po scorecard nebo po memo
- jestli support-assistant sample stačil, nebo lead chtěl use-case-specific variantu
