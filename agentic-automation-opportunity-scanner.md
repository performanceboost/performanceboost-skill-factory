# Agentic Automation Opportunity Scanner

## Zweck
Autonome AI-Agents können repetitive, mehrstufige Prozesse ohne menschliche Eingriffe ausführen — von der Prospect-Recherche über CRM-Updates bis zur Meeting-Vorbereitung. Dieses Skill-Dokument identifiziert systematisch, welche Prozesse in der Revenue Engine eines B2B-KMU für Agentic Automation geeignet sind, und priorisiert sie nach realistischem Aufwand-/Impact-Verhältnis. Es verhindert, dass Unternehmen autonome Agents auf den falschen Prozessen aufsetzen — denn ein Agent auf einem schlecht definierten Prozess macht Fehler schneller, nicht langsamer.

## Wann verwenden
- Wenn das AI-Readiness-Assessment Level 3 oder höher ergibt (Voraussetzung)
- Wenn SDRs oder Account Executives mehr als 40% ihrer Zeit mit manueller Recherche und CRM-Pflege verbringen
- Wenn Prospect-Listen unvollständig sind und das Enrichment-Budget für manuelle Arbeit zu hoch ist
- Wenn Marketing-Automationen bereits laufen, aber die Übergabe zu Sales noch manuell erfolgt
- Als Grundlage für den Aufbau eines Clay-Workflows oder einer Make/n8n-Automatisierungs-Architektur

## Input

**Prozess-Inventar (aus bestehendem oder neu erstelltem Process-Mapping)**
- Liste der 15 häufigsten Aufgaben in Sales, Marketing und Operations
- Zeitaufwand pro Aufgabe: Minuten/Durchführung × Durchführungen/Woche = Stunden/Woche
- Wer führt die Aufgabe aus? (Rolle, Seniorität, Stundensatz als Proxy für CHF-Wert)
- Welche Tools sind involviert? (Input-System, Output-System, Übergabe-Mechanismus)

**Daten- und Trigger-Qualität**
- Existieren klare Trigger-Events für den Start des Prozesses? (z.B. neuer Lead im CRM, Formular-Einreichung, Stellenausschreibung online)
- Sind die Entscheidungsregeln innerhalb des Prozesses explizit und regelbasiert, oder erfordern sie Kontexturteil?
- Ist der erwartete Output klar definiert und validierbar?

**Tool-Stack-Inventar**
- CRM: HubSpot / Salesforce / Pipedrive (mit API-Zugang ja/nein)
- Enrichment-Tools: Clay, Apollo, Clearbit, LinkedIn Sales Navigator
- Automation-Layer: Make, Zapier, n8n
- Kommunikations-Tools: E-Mail-Client, LinkedIn, Slack
- AI-Layer: GPT-4, Claude, Gemini (mit API-Schlüssel ja/nein)

## Analyseprozess

1. **Prozess-Taxonomie erstellen**
   - Klassifiziere jeden identifizierten Prozess in eine von fünf Kategorien:
     - **Research & Enrichment**: Prospect-Recherche, Firmendaten anreichern, News-Monitoring
     - **Qualifizierung & Routing**: Lead-Scoring, MQL-Determination, Zuweisung zu Vertriebsmitarbeitenden
     - **Outreach & Sequencing**: Erstkontakt vorbereiten, Follow-up-Timing bestimmen, Sequenz-Personalisierung
     - **CRM-Hygiene & Updates**: Deal-Status pflegen, Kontaktdaten aktualisieren, Aktivitäten loggen
     - **Reporting & Insights**: Wöchentliche Reports zusammenstellen, Pipeline-Zusammenfassungen, Meeting-Briefings
   - Jede Kategorie hat unterschiedliche Reife-Anforderungen für Agentic Automation

2. **Agent-Fähigkeits-Matching**
   - Prüfe jeden Prozess gegen fünf Kriterien (je 0–2 Punkte):
     - **Trigger-Klarheit**: Gibt es einen eindeutigen, maschinenlesbaren Auslöser? (0 = unklar, 1 = teilweise, 2 = eindeutig)
     - **Regelbasierheit**: Sind alle Entscheidungen im Prozess regelbasiert, ohne Ausnahme-Urteil? (0 = oft Urteil, 1 = gemischt, 2 = vollständig regelbasiert)
     - **Datenqualität**: Sind Input-Daten strukturiert und verlässlich? (0 = lückenhaft, 1 = teilweise, 2 = vollständig)
     - **Output-Validierbarkeit**: Kann ein Mensch den Agent-Output in <30 Sekunden validieren? (0 = nein, 1 = mit Aufwand, 2 = trivial)
     - **Fehlertoleranz**: Was passiert bei einem falschen Output? (0 = kritisch, 1 = korrigierbar, 2 = kein Schaden)
   - Maximaler Score: 10 Punkte. Score ≥7: Agent-Ready. Score 4–6: Prozess erst optimieren, dann automatisieren. Score <4: kein Agent-Kandidat.

3. **CHF-Impact-Kalkulation**
   - Zeitersparnis pro Woche (Stunden) × Stundensatz der ausführenden Person (CHF) × 52 Wochen = **Jahres-CHF-Wert der Automatisierung**
   - Beispiel-Benchmarks aus der Praxis:
     - Manuelle Prospect-Recherche (SDR, 45 Min./Prospect, CHF 80/h): Bei 20 Prospects/Woche = CHF 62'400/Jahr Zeitwert
     - CRM-Update nach Kundengespräch (AE, 15 Min./Gespräch, CHF 120/h): Bei 15 Gesprächen/Woche = CHF 14'040/Jahr
     - Wöchentlicher Pipeline-Report (Marketing, 2h/Woche, CHF 90/h): CHF 9'360/Jahr
   - Implementierungsaufwand schätzen: Einfache Agents (Make/Zapier + 1 AI-Step) = 4–8h Setup. Komplexe Multi-Step-Agents (Clay-Workflow + CRM-Integration + AI) = 20–60h Setup.
   - ROI-Schwelle: Amortisation in <6 Monaten als Mindestkriterium für Empfehlung

4. **Sequenzierungs-Analyse**
   - Identifiziere Prozesse, die voneinander abhängen — Agents können als Kette gebaut werden
   - Beispiel-Kette: [Trigger: Neuer Inbound-Lead] → [Agent 1: Firmendaten anreichern via Clay] → [Agent 2: ICP-Score berechnen] → [Agent 3: Personalisierte Erstmail entwurf erstellen] → [Human Checkpoint: Mail freigeben] → [Agent 4: CRM-Deal anlegen und Aktivität loggen]
   - Identifiziere notwendige Human Checkpoints (Qualitätsgates, die ein Agent nicht ersetzen soll)

5. **Risiko-Priorisierung**
   - Für jeden Agent-Kandidaten: Was ist das schlimmste plausible Failure-Szenario?
   - Klassifiziere: **Low Risk** (falscher CRM-Eintrag, leicht korrigierbar), **Medium Risk** (falsch personalisierte Mail geht raus), **High Risk** (falscher Deal-Abschluss, DSGVO-Verletzung)
   - High-Risk-Prozesse werden nicht automatisiert ohne Human-in-the-Loop-Architektur

## Bewertungslogik

**Level 1 — Keine Agent-Kandidaten (Durchschnitt-Score <3)**
Prozesse zu undefiniert oder Daten zu lückenhaft. AI-Agents würden Chaos schneller reproduzieren. Priorität: Prozess-Dokumentation und Datensanierung (3–6 Monate) bevor Agents gebaut werden.

**Level 2 — Einzelne Einfach-Agents möglich (Score 4–5 für 1–2 Prozesse)**
Ein bis zwei gut definierte Prozesse eignen sich für einfache Automatisierung (Zapier/Make ohne komplexe AI-Logik). Geeignet als Pilotprojekt für Team-Akzeptanz. Typisch: automatisches CRM-Logging von E-Mail-Aktivitäten.

**Level 3 — Multi-Step-Agents realistisch (Score ≥7 für 3–5 Prozesse)**
Mehrere Prozesse erfüllen die Agent-Kriterien. Erste vollständige Automation-Kette kann gebaut werden. Hauptkandidat: Research-to-Outreach-Pipeline für Prospecting. Erwartete Zeitersparnis: 5–10 Stunden/Woche für das Sales-Team.

**Level 4 — Agent-Portfolio ausbaufähig (Score ≥7 für 6–10 Prozesse)**
Eine koordinierte Agent-Architektur ist sinnvoll. Verschiedene Agents teilen Daten und Trigger. Dediziertes Ops-Budget für Agent-Wartung und -Optimierung notwendig (ca. CHF 500–1'500/Monat intern).

**Level 5 — Autonome Revenue-Engine-Komponenten (Score ≥7 für >10 Prozesse)**
Large parts der Revenue Engine laufen mit minimaler manueller Intervention. Menschliche Arbeit konzentriert sich auf Urteil, Beziehung und Strategie. Weniger als 3% aller B2B-KMU in der Schweiz haben dieses Niveau.

## Output

- **Agent-Opportunity-Register**: Tabellarische Übersicht aller Prozesse mit Score, CHF-Wert, Implementierungsaufwand und Risiko-Klassifizierung
- **Top-3-Prioritätenliste**: Die drei Agent-Kandidaten mit dem besten Aufwand/Impact-Verhältnis und ROI <6 Monate
- **Architektur-Skizze**: Welche Tools für welchen Agent — Tool-Stack je Kandidat
- **Human-Checkpoint-Karte**: Wo müssen Menschen im Agent-Workflow eingreifen — und warum
- **Quick-Win-Agent-Spezifikation**: Für den #1-Kandidaten: vollständige Prozessbeschreibung, Trigger, Steps, Output, Validierungslogik

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Einen Einfach-Agent implementieren: CRM-Aktivitäts-Logging via Make (Trigger: E-Mail gesendet → CRM-Aktivität anlegen). Setup: 2–3 Stunden. Ziel: Team an Agent-Konzept gewöhnen
- Clay-Trial für Prospect-Enrichment starten: Manuell aufgebaute Liste von 50 Prospects durch Clay-Workflow anreichern und Zeitersparnis messen (Benchmark: 80% Zeitreduktion vs. manuelle Recherche)
- Jeden SDR bitten, eine Woche lang zu tracken: Wie viele Minuten pro Tag für CRM-Pflege, Recherche, und Report-Erstellung? Baseline für ROI-Berechnung

**Mittelfristig (1–3 Monate)**
- Research-to-Outreach-Agent aufbauen: [Trigger: ICP-Unternehmen auf LinkedIn oder G2] → [Clay: Firmendaten + Kontaktdaten anreichern] → [AI: Personalisierungs-Snippet generieren] → [CRM: Kontakt anlegen + Sequenz starten]
- CRM-Hygiene-Agent implementieren: Automatisches Erkennen und Zusammenführen doppelter Kontakte, automatisches Updaten von Firmen-Informationen via Clearbit-API
- Meeting-Briefing-Agent pilotieren: 30 Minuten vor jedem Kundengespräch automatisch: letzte 3 Aktivitäten, offene Deal-Stage, letzte News des Unternehmens — als Slack-Nachricht an AE

**Strategisch (3–12 Monate)**
- End-to-End-Inbound-Agent: Von Formular-Einreichung bis personalisierter Erstkontakt in <5 Minuten, ohne menschliche Intervention bis zum Human Checkpoint
- Churn-Frühwarnsystem: Agent überwacht CRM-Signale (Rückgang Login-Aktivität, ausgebliebene Renewal-Kommunikation) und eskaliert proaktiv an Customer Success
- Competitive Intelligence Agent: Automatisches Monitoring von Mitbewerber-Stellenausschreibungen, Pricing-Änderungen und G2-Reviews — wöchentlicher Briefing-Report für Sales

## Performanceboost Perspektive

Wir bauen keine Agents auf Prozessen, die noch nicht funktionieren. Das ist der häufigste Fehler: Ein Unternehmen automatisiert einen broken Prozess — und hat dann einen broken Prozess, der 10x schneller Fehler produziert. Unsere Reihenfolge ist fix: Prozess definieren → Prozess manuell testen → Prozess automatisieren → Agent mit Human Checkpoint testen → Agent in Produktion.

Unser spezifischer Hebel bei KMU: Wir starten mit dem Prospecting-Agent, weil er den direktesten CHF-Impact auf die Pipeline hat und in 3–4 Wochen implementierbar ist. Clay + GPT-4 + HubSpot-Integration — dieser Stack liefert bei unseren Kunden regelmässig 8–12 Stunden Zeitersparnis pro SDR pro Woche. Das sind bei einem CHF 90'000-Jahresgehalt CHF 20'000–30'000 Jahreswert aus einem einzigen Agent. Das ist die Zahl, die wir dem Geschäftsführer zeigen — nicht die Workflow-Architektur.
