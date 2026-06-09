# AI Use Case Discovery

## Zweck
Die meisten AI-Use-Case-Gespräche in KMU scheitern an zwei Extremen: entweder zu abstrakt ("Wir wollen AI für alles einsetzen") oder zu eng ("Wir brauchen einen Chatbot"). Dieses Skill-Dokument strukturiert einen Workshop-Prozess, der konkrete, priorisierte AI-Use-Cases entlang der gesamten Revenue Engine aufdeckt — von der ersten Idee über die Feasibility-Prüfung bis zum belastbaren Business Case. Es produziert keine Ideen-Liste, sondern eine Entscheidungsgrundlage.

## Wann verwenden
- Als strukturierter Workshop mit Entscheider und Teamleads (Dauer: 3–4 Stunden)
- Wenn ein Unternehmen AI "angehen" möchte, aber nicht weiss wo
- Nach einem AI-Readiness-Assessment (Level 2 oder höher) als nächster Schritt
- Wenn bestehende AI-Investitionen keinen klaren ROI zeigen und eine Neubewertung nötig ist
- Wenn ein neues Service-Angebot oder Produkt gebaut wird und AI-Komponenten evaluiert werden

## Input

**Vorbereitung (wird 48h vor Workshop versandt)**
- Ausgefüllte Revenue-Engpass-Karte: Wo verliert das Unternehmen aktuell am meisten Deals/Zeit/Geld? (5 Minuten Ausfüllen, max. 10 Punkte)
- Tool-Inventar: Vollständige Liste aller eingesetzten Software-Tools mit Hauptnutzung
- KPI-Snapshot: Aktuelle Werte für 5 Kernkennzahlen (Lead-Volumen, MQL→SQL-Rate, Durchschnittliche Deal-Dauer, Churn-Rate, CAC)
- Team-Readiness-Selbsteinschätzung: Wer im Team hat bereits AI-Tools produktiv genutzt? (Namen und Tools)

**Workshop-Teilnehmende (obligatorisch)**
- Geschäftsleitung oder Entscheidungsträger/in (Budget- und Strategie-Kontext)
- Marketing-Verantwortliche/r (Nachfrage und Lead-Generation-Perspektive)
- Sales-Verantwortliche/r (Pipeline- und Conversion-Perspektive)
- Optional: Operations oder Customer Success (Retention-Perspektive)

## Analyseprozess

### Phase 1: Revenue-Engine-Mapping (45 Minuten)

1. **Visualisierung der gesamten Revenue Engine auf einem Board**
   - Zeichne den vollständigen Weg von Erstkontakt bis zu erneutertem Kauf: Awareness → Lead → MQL → SQL → Proposal → Closed Won → Onboarding → Retention → Expansion
   - Für jeden Schritt: Aktuelle Konversionsrate und durchschnittliche Dauer
   - Beispiel-Benchmark-Referenzwerte für B2B-KMU in der DACH-Region:
     - MQL→SQL-Rate Best-in-Class: 35% (Branchendurchschnitt: 12–18%)
     - SQL→Closed-Won-Rate Best-in-Class: 30% (Branchendurchschnitt: 15–22%)
     - Lead-to-Close-Zyklus B2B-SaaS: 45–90 Tage (KMU unter CHF 50k ACV)
   - Markiere für jeden Schritt: Wie viel menschliche Arbeit steckt drin? (hoch/mittel/tief)

2. **Engpass-Identifizierung**
   - Frage an jede Person: "Wo verliert ihr am meisten Deals, die ihr eigentlich gewinnen solltet?"
   - Frage: "Welcher Schritt dauert am längsten und warum?"
   - Frage: "Wo verbringt euer Team Zeit, die direkt auf dem Ergebnis keinen Einfluss hat?"
   - Markiere die drei grössten Engpässe auf der Revenue-Engine-Karte

### Phase 2: AI-Opportunity-Brainstorming (60 Minuten)

3. **Strukturiertes Brainstorming nach Use-Case-Kategorien**
   - Für jede der 6 AI-Kategorien 5–10 Minuten Brainstorming (Stille Einzelarbeit → Teilen → Cluster):

   **Kategorie 1: Inhaltserstellung und -personalisierung**
   - Trigger-Fragen: "Welche Inhalte erstellt ihr regelmässig, die sich inhaltlich kaum unterscheiden?" "Wo personalisiert ihr manuell?"
   - Typische Use Cases: AI-personalisierte Kalt-E-Mails, automatische Angebots-Zusammenfassungen, Case-Study-Drafts, Social-Media-Post-Varianten

   **Kategorie 2: Recherche und Datenanreicherung**
   - Trigger-Fragen: "Was recherchiert ihr vor einem Kundengespräch?" "Welche Informationen fehlen euch häufig im CRM?"
   - Typische Use Cases: Prospect-Intelligence vor Demo, Firmen-News-Monitoring, Technologie-Stack-Erkennung, Entscheidungsträger-Mapping

   **Kategorie 3: Klassifizierung und Routing**
   - Trigger-Fragen: "Wie entscheidet ihr, ob ein Lead gut genug für Sales ist?" "Wie priorisiert Sales die Pipeline?"
   - Typische Use Cases: AI-Lead-Scoring, Intent-Klassifizierung eingehender Anfragen, Support-Ticket-Kategorisierung, Churn-Risk-Scoring

   **Kategorie 4: Zusammenfassung und Synthese**
   - Trigger-Fragen: "Was müsst ihr manuell zusammenfassen?" "Welche Meetings hätten bessere Follow-ups verdient?"
   - Typische Use Cases: Call-Zusammenfassungen mit Next-Steps, E-Mail-Thread-Synthesen, Pipeline-Review-Briefings, Win/Loss-Analyse-Destillation

   **Kategorie 5: Conversation und Assistenz**
   - Trigger-Fragen: "Welche Fragen bekommt ihr immer wieder?" "Wo wartet ein Kunde auf eine Antwort, die standardisierbar wäre?"
   - Typische Use Cases: Website-Chatbot für Qualifizierung, interner AI-Assistent für Einwand-Handling, FAQ-Bot für Support

   **Kategorie 6: Prognose und Analyse**
   - Trigger-Fragen: "Welche Entscheidungen trefft ihr regelmässig, bei denen ihr euch auf Gefühl stützt statt auf Daten?" "Was würdet ihr analysieren, wenn ihr die Zeit hättet?"
   - Typische Use Cases: Pipeline-Forecast auf Basis historischer Patterns, Churn-Vorhersage, Kanal-Attribution-Modell, Preisoptimierung

4. **Clustering und Konsolidierung**
   - Alle Ideen auf Karten — doppelte zusammenführen, thematisch clustern
   - Ziel: 15–25 konkrete Use Cases als Input für Phase 3

### Phase 3: Feasibility-Filter (45 Minuten)

5. **Schnell-Screening mit drei K.O.-Kriterien**
   - **K.O. 1 — Datenverfügbarkeit**: Existieren die notwendigen Inputdaten strukturiert im System? Wenn nein: Auf "Bedingt möglich" verschieben
   - **K.O. 2 — Regulatorische Machbarkeit**: Sind DSGVO, Finanzregulierung oder Berufsgeheimnis-Anforderungen ein Hindernis? Wenn ja: Rechtsprüfung vor Umsetzung
   - **K.O. 3 — Menschliche Substitution vs. Augmentation**: Ersetzt der Use Case menschliches Urteil an einer kritischen Stelle, oder verstärkt er es? Substituierende Use Cases erfordern höheres Oversight — nicht verboten, aber aufwändiger
   - Nach K.O.-Filter: Typischerweise 8–15 Use Cases verbleiben

6. **Effort/Impact-Bewertung**
   - Jeder verbleibende Use Case erhält zwei Scores (je 1–5):
   - **Impact-Score**: Direkte Auswirkung auf eine der drei Messgrössen: Umsatz, Kosten, Kundenzufriedenheit
     - 1 = kein messbarer Impact
     - 3 = messbarer Impact auf eine Messgrösse, CHF 5'000–20'000/Jahr
     - 5 = messbarer Impact auf mehrere Messgrössen, >CHF 20'000/Jahr oder strategisch differenzierend
   - **Implementierungsaufwand-Score**: Gesamtaufwand für Umsetzung (Tools, Daten, Zeit, Risiko)
     - 1 = 1–5 Tage, no-code Tools, bestehende Daten
     - 3 = 2–6 Wochen, einige Integrationen, Datenaufbereitung nötig
     - 5 = >3 Monate, Custom Development, neue Dateninfrastruktur
   - Priorisierungs-Score = Impact ÷ Aufwand

### Phase 4: Business-Case-Entwicklung (45 Minuten — für Top-3)

7. **Für die drei Use Cases mit höchstem Priorisierungs-Score: vollständiger Business Case**

   **Struktur Business Case (je Use Case):**
   - **Problem-Statement**: Welchen spezifischen Engpass löst dieser Use Case?
   - **Lösungs-Skizze**: Welche Tools, welche Daten, welcher Prozess?
   - **Erwarteter Impact (CHF)**: Konservative und optimistische Schätzung, mit Annahmen
   - **Implementierungsplan**: 3–5 konkrete Schritte, Timeline, Verantwortliche
   - **Erfolgsmetriken**: Wie messen wir, ob es funktioniert? (Metric, Baseline, Zielwert, Messdatum)
   - **Risiken und Mitigationen**: Was kann schiefgehen, und wie verhindern wir es?

## Bewertungslogik

**Level 1 — Keine validierten Use Cases (0 Use Cases mit Score ≥3)**
Brainstorming hat keine konkret umsetzbaren Use Cases ergeben. Ursache: fehlendes Daten-Fundament oder Prozesse zu unklar. Rückkehr zu AI-Readiness-Assessment und Process Automation Assessment.

**Level 2 — Einzelne Quick-Win-Use-Cases (1–3 Use Cases mit Score 3–4)**
Ein bis drei schnell umsetzbare Use Cases identifiziert. Erwarteter CHF-Impact: CHF 5'000–20'000/Jahr. Pilotprojekt empfohlen, um AI-Erfahrung aufzubauen.

**Level 3 — Mehrere priorisierte Use Cases (4–7 Use Cases, davon ≥2 mit Score ≥4)**
Ein solider Portfolio-Ansatz möglich. Erwarteter aggregierter CHF-Impact: CHF 20'000–60'000/Jahr. Dedizierte Implementation-Kapazität empfohlen: 1–2 Personen mit 30% Zeitanteil über 6 Monate.

**Level 4 — Strategisches AI-Portfolio (8+ Use Cases, davon ≥3 mit Score ≥4)**
AI kann in mehreren Revenue-Engine-Stufen gleichzeitig eingesetzt werden. Erwarteter aggregierter CHF-Impact: CHF 50'000–150'000/Jahr. Dedizierter AI-Projektlead empfohlen.

**Level 5 — AI als Wettbewerbsvorteil (>10 Use Cases mit differenzierendem strategischen Impact)**
AI verändert nicht nur Prozesseffizienz, sondern das Geschäftsmodell: personalisierte Produkte, prädiktive Services, skalierbare Beratungsqualität. Selten bei KMU unter 50 MA erreichbar ohne intensive externe Unterstützung.

## Output

- **Use-Case-Register**: Vollständige Tabelle aller identifizierten Use Cases mit Impact-Score, Aufwand-Score, Priorisierungs-Score und Status
- **Priorisierungs-Matrix**: Visuelle Impact/Effort-Darstellung aller Use Cases
- **Top-3-Business-Cases**: Vollständig ausgearbeitete Business Cases mit CHF-Impact, Implementierungsplan und Erfolgsmetriken
- **Quick-Win-Liste**: Use Cases, die in unter 2 Wochen mit bestehendem Stack umsetzbar sind
- **Strategische AI-Roadmap**: 12-Monats-Plan mit Implementierungssequenz und Budget-Bedarf
- **Entscheidungs-Empfehlung**: Klare Empfehlung für ersten Schritt — Was, wer, bis wann, mit welchem Budget?

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Den Use Case mit höchstem Priorisierungs-Score und niedrigstem Aufwand-Score sofort starten — als Lernprojekt mit definiertem Enddatum (4 Wochen)
- Erfolgsmetriken vor Beginn definieren und dokumentieren: Baseline messen, Zielwert setzen, Messdatum festlegen
- Intern kommunizieren, was getestet wird und warum — AI-Projekte scheitern häufig an mangelndem Team-Buy-in, nicht an der Technologie

**Mittelfristig (1–3 Monate)**
- Top-3-Business-Cases sequenziell umsetzen (nicht parallel — parallele Projekte ohne dedizierten Ops-Lead scheitern häufiger)
- Learnings aus Pilotprojekt dokumentieren und in nächste Projekte einfliessen lassen
- Monatliches AI-Review: Was funktioniert, was nicht, was skalieren wir?
- Prompt-Bibliothek aufbauen: Alle validierten AI-Prompts und Workflow-Konfigurationen dokumentieren — institutionelles Wissen statt Einzelpersonen-Know-how

**Strategisch (3–12 Monate)**
- AI-Use-Case-Discovery jährlich wiederholen: Der beste Zeitpunkt für den zweiten Workshop ist 6 Monate nach dem ersten — dann gibt es echte Learnings als Input
- AI-Kompetenz intern aufbauen: Mindestens eine Person mit vertieftem AI-Ops-Know-how (Prompt Engineering, Workflow-Design, Output-Qualitätskontrolle)
- AI-Governance-Regeln definieren: Welche Daten dürfen in welche AI-Tools? DSGVO-konforme Nutzungsrichtlinien schriftlich festhalten
- Wettbewerbs-Monitoring: Welche AI-Capabilities entwickeln direkte Mitbewerber? Ist AI dabei, die Wettbewerbslandschaft in der Branche zu verschieben?

## Performanceboost Perspektive

Wir führen keine AI-Use-Case-Workshops durch, ohne vorher die Revenue-Engine-Karte des Unternehmens gezeichnet zu haben. Der Fehler, den wir immer wieder bei anderen Beratern sehen: Use Cases werden bottom-up aus Tool-Features abgeleitet — "HubSpot hat jetzt AI, was machen wir damit?" Wir arbeiten top-down: wo verliert dieses Unternehmen konkret Umsatz, und kann AI an diesem Punkt helfen?

Der meistübersehene Use Case in B2B-KMU ist Speed-to-Lead: Die durchschnittliche Reaktionszeit auf einen eingehenden Lead in Schweizer KMU beträgt über 24 Stunden. Best-in-Class liegt bei unter 5 Minuten. Ein AI-gestützter Qualifizierungs- und Routing-Agent, der innerhalb von 3 Minuten auf einen neuen Lead reagiert, eine erste Qualifizierungs-Mail sendet und den Sales-Rep mit einem vollständigen Briefing benachrichtigt — das ist kein Technologie-Experiment. Das ist ein messbarer Umsatzhebel, der sich in unter 4 Wochen implementieren lässt.
