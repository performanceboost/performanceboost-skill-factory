# Revenue Operations Maturity Assessment

## Zweck
Dieses Skill-Dokument liefert ein strukturiertes Fünfstufenmodell zur Bewertung der RevOps-Reife eines B2B-Unternehmens. Es deckt auf, wo Prozesse, Daten, Technologie, Team-Alignment und Forecasting-Fähigkeit den Umsatz bremsen — und quantifiziert den CHF-Impact jeder Lücke. Das Modell funktioniert als Einstiegsdiagnostik vor jedem RevOps-Engagement und als jährliches Benchmark-Instrument.

## Wann verwenden
- Vor Beginn eines RevOps-Engagements zur Baseline-Bestimmung
- Wenn Marketing und Sales trotz gemeinsamer Ziele unterschiedliche Kennzahlen berichten
- Wenn Forecasting-Abweichungen regelmässig über ±25% liegen
- Wenn das Unternehmen einen CRM-Wechsel oder Tech-Stack-Erweiterung plant
- Wenn Wachstumsstagnation herrscht, aber keine eindeutige Ursache identifiziert ist

## Input

**Aus CRM-System (direkter Datenzugriff oder Export):**
- Anzahl offener Deals nach Stage, Alter und Eigentümer
- Konversionsraten je Funnel-Stage (letzte 12 Monate)
- Datenvollständigkeit zentraler Felder (ICP-Kriterien, Deal-Wert, Expected Close Date)
- Anzahl Duplikate und verwaister Records

**Aus Interviews (Marketing-/Sales-/CS-Lead, je 45 Minuten):**
- Definition von MQL, SQL, Opportunity — stimmt sie zwischen den Teams überein?
- Beschreibung des aktuellen Übergabeprozesses Marketing → Sales
- Wie werden Forecast-Zahlen erstellt? Intuition oder datenbasiert?
- Welche Dashboards werden wöchentlich tatsächlich genutzt?

**Aus Dokumentation:**
- Vorhandene SLAs zwischen Marketing und Sales
- Tech-Stack-Übersicht (CRM, Automation, Analytics, Integration)
- Letzter Revenue-Forecast vs. tatsächliches Ergebnis (Quartal)

## Analyseprozess

1. **Prozess-Mapping**
   - Lead-to-Revenue-Prozess vollständig dokumentieren: Wo beginnt, wo endet jede Phase?
   - Übergabe-Kriterien schriftlich festhalten und mit der gelebten Realität abgleichen
   - Identifizieren: Wo gibt es keine definierten Kriterien — reine Bauchentscheidungen?

2. **Daten-Inventar**
   - Vollständigkeitsquote der 10 wichtigsten CRM-Felder messen (Ziel: >85%)
   - Duplikatrate bestimmen (akzeptabel: <3%)
   - Aktualität prüfen: Wie viele Deals wurden >30 Tage nicht angefasst?
   - Attribution prüfen: Wie viele Deals haben keinen zugewiesenen Lead-Source?

3. **Tech-Stack-Audit**
   - Systemlandschaft kartieren: CRM, Automation, Analytics, Integrations
   - Doppelerfassungen und manuelle Datentransfers identifizieren
   - Lizenznutzung vs. tatsächliche Nutzung vergleichen

4. **Alignment-Check**
   - Marketing und Sales unabhängig voneinander dieselben Definitionen abfragen
   - Divergenzen in MQL/SQL-Definition, Pipeline-Metriken und Erfolgsverständnis dokumentieren
   - Shared Dashboards: Existieren sie? Werden sie genutzt?

5. **Forecasting-Analyse**
   - Forecast-Methode dokumentieren: Stage-basiert, historische Konversion, AI-gestützt?
   - Abweichung Forecast vs. Actual letzte 4 Quartale berechnen
   - Daten-Inputs für den Forecast auf Vollständigkeit prüfen

## Bewertungslogik

**Level 1 — Reaktiv (0–20 Punkte)**
Kein definierter Revenue-Prozess. Marketing und Sales operieren in Silos. CRM wird als Kontaktliste verwendet, nicht als Pipeline-Tool. Forecasting basiert auf Schätzungen. Keine geteilten Metriken. Typisches Symptom: Sales beschwert sich über Lead-Qualität, Marketing über fehlende Rückmeldung.

**Level 2 — Aufbauend (21–40 Punkte)**
Erste Prozesse definiert, aber nicht dokumentiert oder konsequent gelebt. CRM-Nutzung inkonsistent. MQL/SQL-Definitionen existieren auf dem Papier, werden aber unterschiedlich interpretiert. Forecasting ist Stage-basiert, ignoriert historische Konversionsraten. Datenqualität unter 70% Vollständigkeit.

**Level 3 — Strukturiert (41–60 Punkte)**
Prozesse dokumentiert und mehrheitlich eingehalten. CRM als zentrales System etabliert. Marketing-to-Sales-Handover mit definierten Kriterien. Forecasting nutzt Konversionsdaten, aber noch keine Velocity-Metriken. Regelmässige Pipeline-Reviews vorhanden. Schweizer KMU-Benchmark: Mehrzahl der wachsenden Mid-Market-Unternehmen befinden sich hier.

**Level 4 — Skalierend (61–80 Punkte)**
Vollständige Funnel-Transparenz. Shared Dashboards aktiv genutzt. Attribution funktioniert für alle wesentlichen Kanäle. Pipeline Velocity wird gemessen und als Steuerungsgrösse verwendet. CAC und LTV sind bekannt und werden in Entscheidungen einbezogen. SLAs zwischen Marketing und Sales schriftlich vereinbart und eingehalten.

**Level 5 — Prädiktiv (81–100 Punkte)**
Forecasting-Genauigkeit >90% (Abweichung <10%). AI-gestützte Lead-Scoring-Modelle aktiv. Vollautomatischer Datenfuss von Erstberührung bis Abschluss. Churn-Prognosen vorhanden. Revenue-Planung direkt aus CRM-Daten abgeleitet. CS, Marketing und Sales unter einem gemeinsamen Revenue-Ziel vereint. Typisch für: Schweizer B2B-SaaS-Unternehmen ab 50 Mitarbeitenden mit dediziertem RevOps-Team.

**Punktevergabe je Dimension (je 20 Punkte max.):**
- Prozesse & Dokumentation
- Datenqualität & CRM-Hygiene
- Tech-Stack-Integration
- Team-Alignment & Shared Metrics
- Forecasting-Fähigkeit

## Output

- RevOps-Maturity-Score (0–100) mit Einordnung auf Fünf-Stufen-Skala
- Heatmap: Welche Dimension zieht den Gesamtscore am stärksten runter?
- Top-3-Lücken mit quantifiziertem CHF-Impact (z.B. «Fehlende Attribution → CHF 85'000 nicht zuordenbare Pipeline»)
- Benchmark-Vergleich: Position im Schweizer B2B-KMU-Markt
- Priorisierte Massnahmenliste nach ROI-Impact

## Empfehlungen

**Quick Wins (0–30 Tage)**
- CRM-Pflichtfelder definieren und technisch erzwingen (ICP-Kriterien, Lead Source, Deal Value)
- MQL/SQL-Definition in einem gemeinsamen Dokument schriftlich festhalten — mit Unterschriften beider Teams
- Wöchentliches Pipeline-Review einführen (45 Minuten, strukturierte Agenda)
- Duplikate im CRM bereinigen (Tool: HubSpot Duplicate Manager, Dedupely, oder nativer Salesforce-Prozess)

**Mittelfristig (1–3 Monate)**
- Shared Revenue-Dashboard aufbauen: Pipeline Velocity, MQL→SQL-Rate, CAC, Win Rate
- SLA zwischen Marketing und Sales formulieren: Reaktionszeit auf MQLs (Ziel: <4 Stunden), Follow-up-Frequenz
- Attribution-Modell implementieren: Multi-Touch für Top-of-Funnel, Last-Touch für Abschluss-Attribution
- Forecasting-Prozess von Stage-basiert auf historische Konversionsraten umstellen

**Strategisch (3–12 Monate)**
- Lead-Scoring-Modell auf Basis echte Konversionsdaten kalibrieren (nicht auf Annahmen)
- CS in Revenue-Metriken integrieren: NRR, Expansion Revenue, Churn-Rate als RevOps-Kennzahlen
- Predictive Forecasting einführen: Pipeline Velocity x historische Win Rate x Seasonalität
- Quarterly Business Reviews (QBRs) auf RevOps-Daten basieren — keine Bauchgefühl-Präsentationen

## Performanceboost Perspektive

Die meisten Schweizer KMU landen beim ersten Assessment auf Level 2 oder 3 — nicht weil ihnen die Ambition fehlt, sondern weil «Prozess» und «System» nie gleichzeitig aufgebaut wurden. Marketing hat Automation aufgesetzt, Sales führt ein CRM, aber die beiden Systeme sprechen nicht miteinander. Das Ergebnis: Zwei Wahrheiten über dieselbe Pipeline.

Performanceboost beginnt RevOps-Engagements immer mit diesem Assessment — nicht als Formalität, sondern als Diagnoseinstrument, das die erste Investitionsentscheidung bestimmt. Ein Unternehmen auf Level 2 braucht keine prädiktive Analytics; es braucht zuerst saubere Daten und gemeinsame Definitionen. Die Assessment-Ergebnisse bestimmen direkt, welche der vier Phasen (Audit → Architektur → Implementierung → Optimierung) wie viel Zeit bekommt. Kein Standard-Paket. Kein Überverkaufen von Komplexität, die das Unternehmen noch nicht tragen kann.
