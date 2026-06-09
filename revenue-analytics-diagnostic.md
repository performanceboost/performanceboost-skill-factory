# Revenue Analytics Diagnostic

## Zweck
Dieser Skill prüft, ob die bestehende Reporting-Infrastruktur in der Lage ist, die drei zentralen Revenue-Fragen eines B2B-Unternehmens zu beantworten: Welcher Kanal bringt profitable Kunden (nicht nur Leads)? Wo verlieren wir Deals und warum? Wie hoch ist unser echter Customer Lifetime Value je Segment? Die meisten KMU können keine dieser Fragen mit Daten beantworten — sie können nur Kampagnenleistung messen, keine Revenue-Intelligenz ableiten. Dieser Skill zeigt die Lücke und quantifiziert den Wachstumsschaden.

## Wann verwenden
- Das Unternehmen skaliert Paid Media, aber es ist unklar, welche Kanäle profitable Kunden bringen — nicht nur günstige Leads
- Win/Loss-Analysen existieren nicht oder basieren auf subjektivem Vertriebsfeedback
- CLV/LTV wird entweder nicht gemessen oder einheitlich für alle Kunden berechnet, ohne Segmentierung
- Das Unternehmen plant einen neuen Kanal oder ein neues Segment und braucht historische Revenue-Daten zur Priorisierung
- Marketing und Sales streiten über Lead-Qualität, aber es gibt keine gemeinsame Datenbasis zur Klärung

## Input

**CRM-Daten (letzten 12 Monate)**
- Alle abgeschlossenen Deals: Betrag (CHF), Ursprungskanal, Branche, Unternehmensgrösse, Ansprechpartner-Titel
- Alle verlorenen Deals: Betrag, letzter Stage, Verlustgrund (falls erfasst), Wettbewerber (falls erfasst)
- Durchschnittliche Sales-Cycle-Länge je Kanal und Segment
- Churn-Daten falls SaaS/Subscription: wann gekündigt, Segment, Nutzungsdaten falls vorhanden

**Marketing-Daten**
- Lead-Volumen je Kanal (letzten 12 Monate)
- Marketing-Budget je Kanal (letzten 12 Monate, in CHF)
- MQL-Definitionen: wie ist ein MQL definiert? Wer hat die Definition festgelegt? Wann zuletzt aktualisiert?
- Conversion-Rates je Funnel-Stage: Lead → MQL → SQL → Opportunity → Deal

**Finanzielle Grunddaten**
- Durchschnittlicher Jahresumsatz je Kunde (ARR oder einmalig, je nach Modell)
- Durchschnittliche Vertragslaufzeit (Monate)
- Bekannte Churn-Rate (falls Subscription)
- Deckungsbeitrag oder Bruttomarge je Produktlinie (falls verfügbar)

**Technische Infrastruktur**
- CRM-System und Version
- Ist Kanaldaten-Attribution im CRM-Deal-Objekt vorhanden? (Feld "Original Source", "Deal Source" o. ä.)
- Gibt es eine Verbindung zwischen Marketing-Automatisierung und CRM für vollständige Touchpoint-Historien?

## Analyseprozess

1. **Revenue-by-Channel-Analyse**
   - Alle abgeschlossenen Deals der letzten 12 Monate nach Ursprungskanal segmentieren
   - Je Kanal berechnen: Anzahl Deals, Gesamtumsatz CHF, durchschnittlicher Deal Value, Customer Acquisition Cost (CAC)
   - CAC je Kanal = (Kanal-Budget + anteiliger Overhead) ÷ Anzahl Deals aus diesem Kanal
   - CAC/LTV-Ratio je Kanal berechnen: Zielwert 1:3 oder besser; unter 1:2 ist strukturell unprofitabel
   - Häufiger Befund: LinkedIn generiert weniger Leads, aber höhere Deal Values und bessere CAC/LTV-Ratios als Google Display

2. **Funnel-Leak-Analyse**
   - Vollständige Conversion-Rate je Stage für die letzten 12 Monate berechnen
   - Benchmarks B2B SaaS Deutschschweiz: Lead → MQL 20–35 %, MQL → SQL 25–40 %, SQL → Opportunity 50–70 %, Opportunity → Deal 25–40 %
   - Stages mit unter 50 % der Benchmark-Rate identifizieren: das ist der primäre Leak-Punkt
   - Stagespezifische Analyse: bei welchen Deals verlieren wir in welcher Stage — nach Kanal, Segment, Unternehmensgrösse?

3. **Win/Loss-Qualitäts-Audit**
   - Anteil verlorener Deals mit dokumentiertem Verlustgrund im CRM messen: Zielwert über 70 %
   - Verlustgründe kategorisieren: Preis, Wettbewerber, kein Budget, kein Bedarf, Timing, kein Entscheider erreicht
   - Falls unter 40 % der Verluste dokumentiert sind: keine valide Win/Loss-Analyse möglich — strukturelles CRM-Hygiene-Problem
   - Top-3-Verlustgründe identifizieren und gegen Positionierung und Messaging abgleichen

4. **CLV-Segmentierungsanalyse**
   - CLV je Kundensegment berechnen: CLV = (Avg. Jahresumsatz × Bruttomarge) × (1 ÷ Churn-Rate)
   - Segmentierungskriterien: Branche, Unternehmensgrösse, Ursprungskanal, Produkt/Service-Linie
   - Höchsten CLV-Segment identifizieren: wie viel % des Marketing-Budgets fliesst in dieses Segment?
   - Typischer Befund: das Segment mit dem höchsten CLV erhält nicht proportional mehr Budget als der Durchschnitt

5. **Attribution-Gap-Analyse**
   - Anteil Deals mit leerem oder "Unknown"-Ursprungskanal im CRM messen
   - Hochrechnung: bei 20 % Unknown-Deals und CHF 500'000 Jahresumsatz sind CHF 100'000 Revenue nicht zuordenbar
   - Dark-Funnel-Schätzung: welche Touchpoints (LinkedIn-Organisch, Empfehlung, Event) werden systematisch nicht erfasst?

6. **Pipeline-Velocity-Berechnung**
   - Pipeline Velocity = (Anzahl Opportunities × Avg. Deal Value × Win Rate) ÷ Sales Cycle Länge (Tage)
   - Monatliche Pipeline-Velocity für die letzten 6 Monate berechnen
   - Trend: steigt oder fällt Pipeline Velocity? Welche Variable treibt die Veränderung?
   - Pipeline Velocity je Kanal vergleichen: welcher Kanal produziert die schnellsten, profitabelsten Deals?

## Bewertungslogik

**Reifegrad-Modell: 5 Stufen**

**Stufe 1 — Revenue Blind**
Keine Kanal-Attribution im CRM. Win/Loss-Dokumentation unter 20 %. CLV wird nicht berechnet. Marketing- und Sales-Daten existieren in getrennten Systemen ohne Verbindung. Budgetentscheidungen basieren auf Plattform-Metriken (Klicks, Impressionen), nicht auf Revenue-Daten. Typisch für Unternehmen unter CHF 2 Mio. Jahresumsatz ohne dediziertes Marketing.

**Stufe 2 — Kanal-Awareness**
Grundlegende Kanal-Attribution vorhanden, aber lückenhaft (30–50 % Unknown). Funnel-Conversion-Rates bekannt, aber nicht segmentiert. Kein CLV-Modell. Win/Loss-Dokumentation 20–50 %. Budgetentscheidungen teilweise datengeleitet, aber primär durch Mediapläne der Agenturen getrieben.

**Stufe 3 — Funnel-Sichtbarkeit**
Vollständige Funnel-Daten mit Conversion-Rates je Stage. Kanal-Attribution über 70 % vollständig. CLV als Einzelwert berechnet (aber nicht segmentiert). Win/Loss-Dokumentation über 60 %. Pipeline-Velocity bekannt und wird monatlich gemessen.

**Stufe 4 — Revenue Intelligence**
CAC und CLV je Kanal und Segment berechnet. CAC/LTV-Ratio als Budget-Entscheidungskriterium aktiv genutzt. Win/Loss-Analyse strukturiert und wird in Positionierungs-Reviews eingespeist. Pipeline-Velocity-Trend wird monatlich zur Forecast-Kalibrierung genutzt. Dark-Funnel partiell erfasst.

**Stufe 5 — Predictive Revenue**
Segmentiertes CLV-Modell mit Churn-Prädiktoren. Multi-Touch-Attribution mit Revenue-Rückwärtsattribution (welcher erste Touchpoint produzierte die profitabelsten Kunden?). Automatisierter Forecast basierend auf Pipeline-Velocity und historischen Win-Rates. Marketing-Budget-Allokation wird quartalsweise basierend auf CAC/LTV-Ratio je Segment angepasst.

## Output

- **Revenue-by-Channel-Tabelle**: Umsatz CHF, Deals, Avg. Deal Value, CAC, CLV, CAC/LTV-Ratio je Kanal
- **Funnel-Leak-Report**: Conversion-Rates je Stage vs. Benchmarks, primärer Leak-Punkt identifiziert
- **Win/Loss-Analyse**: Top-3-Verlustgründe, Anteil dokumentierter Verluste, Messaging-Implikationen
- **CLV-Segmentierungstabelle**: CLV je Segment mit Budget-Allokation-Empfehlung
- **Pipeline-Velocity-Trend**: monatlich, letzten 6 Monate, mit Treiber-Analyse
- **Revenue-Lücken-Quantifizierung**: CHF-Schätzung des Impacts, falls primäre Lücken geschlossen würden

## Empfehlungen

**Quick Wins (0–30 Tage)**
- CRM-Pflichtfeld für Verlustgrund einführen: alle Deals ab sofort nicht ohne dokumentierten Verlustgrund schliessen
- Kanaldaten-Attribution in allen neuen Deals als Pflichtfeld setzen — historische Daten bereinigen soweit rückwirkend möglich
- CAC je Kanal für die letzten 12 Monate berechnen: Google Sheet reicht als Startpunkt, kein BI-Tool notwendig

**Mittelfristig (1–3 Monate)**
- CLV-Modell für die 3 wichtigsten Kundensegmente aufbauen: Daten aus CRM + Finanzbuchhaltung
- Monatlichen Revenue-Analytics-Review einführen: CAC/LTV je Kanal, Pipeline-Velocity-Trend, Top-Verlustgründe
- Marketing-to-Sales Übergabedefinition (MQL-Kriterien) anhand der Funnel-Leak-Analyse validieren oder anpassen

**Strategisch (3–12 Monate)**
- Budget-Allokation formal an CAC/LTV-Ratio knüpfen: Kanal mit Ratio unter 1:2 wird nicht skaliert, über 1:4 wird priorisiert
- Win/Loss-Analyse in quartalsweise Positioning-Reviews einbetten: Verlustmuster fliessen in Messaging und ICP-Definition zurück
- Predictive Forecasting einführen: Pipeline-Velocity-Modell als Grundlage für Umsatzprognosen ersetzen manuelle Sales-Schätzungen

## Performanceboost Perspektive

Wir sehen bei fast jedem B2B-KMU dasselbe Muster: Das Marketing optimiert auf Cost-per-Lead, der Vertrieb beklagt Lead-Qualität, und niemand kann mit Zahlen belegen, welcher Kanal tatsächlich profitable Kunden produziert. Die Debatte bleibt subjektiv, weil die Dateninfrastruktur für eine objektive Antwort fehlt.

Performanceboost verknüpft deshalb von Beginn an Marketing-Daten (Kanal, Kampagne, Budget) mit CRM-Daten (Deal-Value, Churn, Upsell) — und berechnet CAC und CLV nicht als theoretische Grössen, sondern als reale Entscheidungsparameter für die nächste Budgetrunde. Konkret: In einem typischen Engagement zeigt die erste Revenue-Analytics-Auswertung, dass einer der Top-3-Paid-Kanäle einen CAC/LTV-Ratio unter 1:1,5 hat — strukturell unprofitabel. Diese Erkenntnis ist in keinem Plattform-Report sichtbar, weil Plattformen nur ihre eigene Effizienz messen, nie den Revenue-Impact.
