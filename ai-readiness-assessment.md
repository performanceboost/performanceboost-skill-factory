# AI Readiness Assessment

## Zweck
Die meisten B2B-KMU diskutieren AI-Einsatz, bevor sie die Grundvoraussetzungen dafür erfüllen. Dieses Skill-Dokument bewertet systematisch, ob ein Unternehmen bereit ist für den produktiven AI-Einsatz — nicht als Experiment, sondern als Produktivitätshebel. Es verhindert teure Fehlinvestitionen in Tools, die an mangelnder Datenbasis, ungereiften Prozessen oder fehlendem Team-Kontext scheitern.

## Wann verwenden
- Vor jeder AI-Tool-Empfehlung oder -Implementierung — als obligatorische Voraussetzungs-Diagnose
- Wenn ein KMU fragt "Wir wollen AI einsetzen — wo fangen wir an?"
- Wenn bestehende AI-Tools nicht den erwarteten ROI liefern und die Ursache unklar ist
- Vor dem Aufbau von Automatisierungs-Workflows, die auf AI-Ausgaben angewiesen sind
- Bei der Evaluation, ob ein Unternehmen für Agentic Automation bereit ist (Vorstufe zu Skill: Agentic Automation Opportunity Scanner)

## Input

**Datenbasis**
- CRM-Datenvollständigkeit: Prozentsatz befüllter Pflichtfelder (Zielwert: >80%)
- Historische Datentiefe: Wie viele Monate/Jahre saubere, strukturierte Daten existieren
- Datenquellen-Inventar: Welche Systeme erzeugen strukturierte Daten (CRM, ERP, Marketing-Tool, Website)
- Datenkonsistenz: Gibt es eine Single Source of Truth oder mehrere konkurrierende Wahrheiten?

**Prozessreife**
- Dokumentationsgrad: Sind kritische Prozesse schriftlich definiert oder leben sie in Köpfen?
- Wiederholbarkeitsgrad: Wie viele Prozesse laufen identisch ab, unabhängig davon, wer sie ausführt?
- Fehlerquote: Werden Prozessfehler gemessen und zurückverfolgt?
- Übergabepunkte: Sind Handover-Kriterien (z.B. MQL → SQL) klar definiert?

**Team-Kapazität und -Kompetenz**
- AI-Erfahrungsstand: Wer im Team nutzt bereits welche AI-Tools produktiv?
- Verfügbare Implementation-Kapazität: Stunden pro Monat, die für AI-Projekte reserviert werden können
- Change-Readiness: Wie reagiert das Team auf neue Tools — Frühadopter oder Skeptiker?
- Technische Grundkompetenz: Kann das Team Prompts schreiben, Workflows konfigurieren, Outputs validieren?

**Strategische Klarheit**
- Priorisierte Wachstumsziele für die nächsten 12 Monate
- Identifizierte Engpässe im Revenue-System (Wo verliert das Unternehmen Deals/Zeit/Geld?)
- Budget-Rahmen für AI-Tools und Implementierung (Orientierung: CHF 500–5'000/Monat)

## Analyseprozess

1. **Datenbasis-Audit**
   - CRM-Export: Zähle befüllte vs. leere Felder für die Top-10 Kontakt- und Deal-Felder
   - Prüfe Datenkonsistenz: Gibt es doppelte Kontakte, inkonsistente Firmennamen, fehlende Umsatzdaten?
   - Bewerte Historien-Tiefe: Weniger als 6 Monate saubere Daten = AI-Modelle trainieren auf Rauschen
   - Identifiziere, welche Daten bereits in maschinenlesbarem Format vorliegen vs. in PDFs, E-Mails oder Köpfen

2. **Prozess-Mapping**
   - Liste die 10 zeitaufwändigsten wiederkehrenden Aufgaben in Marketing, Sales und Operations auf
   - Bewerte jede nach: Wie oft pro Woche? Wie viele Minuten? Wie hoch die Fehlerrate?
   - Markiere welche davon regelbasiert (deterministisch) vs. urteilsabhängig (probabilistisch) sind
   - Regelbasierte Prozesse mit >2 Stunden/Woche Aufwand: direkte Automatisierungs-Kandidaten

3. **Team-Readiness-Interview**
   - Befrage je eine Person aus Marketing, Sales und Operations (15 Minuten pro Person)
   - Kernfragen: Welche Tools nutzt du täglich? Wo verlierst du am meisten Zeit an sinnloser Arbeit? Was würdest du nie an eine Maschine delegieren?
   - Identifiziere AI-Champions (Frühadopter) und Skeptiker — beide sind wichtige Informationsquellen

4. **Use-Case-Prä-Screening**
   - Mappe identifizierte Prozesse gegen bekannte AI-Use-Case-Kategorien: Inhaltserstellung, Datenanreicherung, Klassifizierung, Zusammenfassung, Personalisierung, Routing
   - Bewerte pro Use Case: Datenverfügbarkeit (0–3), Prozessklarheit (0–3), Business Impact (0–3)
   - Use Cases mit Score ≥7/9 sind Quick-Win-Kandidaten

5. **Risiko-Assessment**
   - Identifiziere regulatorische Einschränkungen (DSGVO, Finanzregulierung, Berufsgeheimnis)
   - Prüfe Tool-Kompatibilität: Welche bestehenden Systeme haben native AI-Features vs. benötigen externe Integration?
   - Bewerte Abhängigkeits-Risiko: Wie kritisch ist ein Prozess, wenn das AI-Tool ausfällt?

## Bewertungslogik

**Level 1 — AI-Blind (Score 0–20%)**
Keine strukturierten Daten, keine dokumentierten Prozesse, kein Team-Wissen über AI. AI-Investitionen würden an der Basis scheitern. Priorität: Daten- und Prozess-Fundament aufbauen, bevor jedes AI-Gespräch stattfindet. Typische Situation: Handwerksbetrieb mit Excel-basierter Kundenverwaltung.

**Level 2 — AI-Neugierig (Score 21–40%)**
Einzelne Mitarbeitende nutzen ChatGPT sporadisch, aber kein systematischer Einsatz. CRM vorhanden, aber lückenhaft befüllt. Prozesse teilweise dokumentiert. Quick Wins möglich, aber ohne Fundament-Arbeit kaum skalierbar. Typische Situation: 15-Personen-Agentur, die GPT für Textentwürfe nutzt.

**Level 3 — AI-Experimentierend (Score 41–60%)**
Mehrere Tools im Einsatz (Copilot, ChatGPT, vereinzelt Clay), aber unkoordiniert. Daten sauber in einem Kernsystem, Prozesse dokumentiert für Hauptpfade. AI-Projekte starten und stagnieren mangels Ownership. Typische Situation: B2B-SaaS mit 30 MA, HubSpot in Betrieb, aber kein Revenue Operations Framework.

**Level 4 — AI-Systematisch (Score 61–80%)**
AI in mehreren Prozessen produktiv integriert, messbare Zeitersparnis dokumentiert, dediziertes AI-Budget. Daten konsistent, Prozesse klar. Bereit für Agentic Automation in definierten Bereichen. Typische Situation: Scale-up mit RevOps-Funktion, Clay für Prospecting, HubSpot-Automationen aktiv.

**Level 5 — AI-Nativ (Score 81–100%)**
AI durchzieht die gesamte Revenue Engine. Entscheidungen werden durch AI-Insights informiert, nicht nur beschleunigt. Feedback-Loops zwischen AI-Outputs und Geschäftsergebnissen etabliert. Weniger als 5% aller B2B-KMU in der Deutschschweiz haben dieses Niveau erreicht.

## Output

- **AI-Readiness-Score** (0–100%) mit Aufschlüsselung nach vier Dimensionen: Daten, Prozesse, Team, Strategie
- **Kurzfristige Quick-Win-Liste**: 3–5 konkrete Use Cases mit Aufwandsschätzung (Stunden) und erwarteter Zeitersparnis (Stunden/Monat)
- **Datenlücken-Report**: Welche Daten fehlen oder sind unstrukturiert — mit konkretem Sanierungsplan
- **Risikomatrix**: Use Cases nach Implementierungsrisiko und Business Impact (2x2)
- **Tool-Gap-Analyse**: Welche AI-Tools sind bereits im Stack, was fehlt, was überlappt
- **Roadmap-Empfehlung**: 90-Tage-Plan mit priorisierten Initiativen

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Einen AI-Champion benennen: eine Person mit 2–4 Stunden/Woche Kapazität für AI-Experimente
- CRM-Datensanierung starten: Pflichtfelder für die Top-200 Kontakte vollständig befüllen (Grundvoraussetzung für alle nachgelagerten AI-Use-Cases)
- ChatGPT oder Claude für interne Dokumente einführen: Gesprächszusammenfassungen, E-Mail-Entwürfe, Research-Zusammenfassungen — messbare Zeitersparnis ohne Datenrisiko
- Einen einzigen regelbasierten Prozess mit >3 Stunden/Woche-Aufwand identifizieren und mit Make.com oder Zapier automatisieren

**Mittelfristig (1–3 Monate)**
- Datenbankqualität auf >80% Vollständigkeit in Kern-CRM-Feldern bringen
- AI-gestützte Lead-Anreicherung implementieren (Clay + Apollo-Kombination): Ziel 85%+ E-Mail-Abdeckung auf Prospecting-Listen
- Erstes AI-Personalisierungsexperiment in E-Mail-Sequenzen aufsetzen: A/B-Test zwischen generischer und AI-personalisierter Version — Benchmark: +15–25% Reply Rate
- Content-Produktion mit AI-Assist beschleunigen: Nicht AI schreibt, AI strukturiert und entwirft — menschliche Redaktion finalisiert

**Strategisch (3–12 Monate)**
- AI-Ops-Funktion aufbauen: Klare Ownership für AI-Tool-Governance, Prompt-Bibliothek, Output-Qualitätskontrolle
- Revenue Intelligence einführen: AI-gestützte Deal-Analyse (Gong/Chorus oder HubSpot AI) — Ziel: Win/Loss-Muster erkennen, nicht nur dokumentieren
- Predictive Scoring implementieren: AI-basiertes Lead-Scoring auf historischen CRM-Daten — Voraussetzung: min. 500 abgeschlossene Deals als Trainingsbasis
- Agentic Workflows in Betrieb nehmen: Autonome Research- und Enrichment-Agents für Prospecting (Vorstufe: Agentic Automation Opportunity Scanner)

## Performanceboost Perspektive

Wir starten kein AI-Projekt ohne dieses Assessment. Der häufigste Fehler, den wir bei KMU sehen: CHF 15'000 in ein AI-Tool investiert, das auf schlechten Daten trainiert wird und schlechte Outputs produziert — dann heisst es "AI funktioniert bei uns nicht." Das ist kein AI-Problem. Das ist ein Fundament-Problem.

Unser spezifischer Ansatz: Wir verbinden das AI-Readiness-Assessment direkt mit dem Revenue-System-Audit. AI-Readiness wird nie isoliert bewertet — immer in Bezug auf den konkreten Engpass im Revenue-System. Ein Unternehmen mit Pipeline-Problem bekommt eine andere AI-Prioritätenliste als eines mit Retention-Problem. Wir liefern keine generischen "AI-Roadmaps" — wir zeigen, welche AI-Investition in den nächsten 90 Tagen den grössten Hebel auf die Umsatzzahl hat. Und wir nennen die Zahl in CHF, nicht in Effizienz-Punkten.
