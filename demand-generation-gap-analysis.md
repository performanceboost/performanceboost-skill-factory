# Demand Generation Gap Analysis

## Zweck
Dieses Framework berechnet die präzise Lücke zwischen dem aktuellen Lead-Volumen und dem Pipeline-Input, der für das definierte Umsatzziel tatsächlich benötigt wird. Es deckt auf, wo in der Demand-Generation-Maschine Volumen, Qualität oder Konversion verloren geht — und quantifiziert den CHF-Schaden pro Schwachstelle. Wer diese Analyse nicht macht, optimiert ins Leere: mehr Budget in Kanäle, die das eigentliche Problem nicht lösen.

## Wann verwenden
- Das Quartalsziel wird verfehlt, aber unklar ist, ob das Problem Volumen, Qualität oder Konversion ist
- Ein neues Umsatzziel wurde gesetzt und der dafür benötigte Pipeline-Input wurde nie rückwärts berechnet
- Mehrere Demand-Gen-Kanäle laufen parallel, aber der Beitrag jedes Kanals zum tatsächlichen Revenue ist unbekannt
- Die Marketing-zu-Sales-Übergabe erzeugt Reibung und gegenseitige Schuldzuweisungen
- Budget-Entscheide für den nächsten Zyklus stehen an und eine Priorisierung fehlt

## Input

**Umsatz- und Pipeline-Daten (aus CRM)**
- Revenue-Ziel aktuelles Quartal/Jahr (CHF)
- Durchschnittlicher Deal-Wert (Average Contract Value, ACV) in CHF
- Historische Win-Rate (Anzahl Deals gewonnen / Anzahl Opportunities gesamt)
- Durchschnittliche Sales-Cycle-Länge in Tagen
- Aktuelle Pipeline-Grösse und Stage-Verteilung

**Lead- und Conversion-Daten (Marketing + CRM)**
- Anzahl MQLs pro Monat (letzten 3 Monate)
- MQL-zu-SQL-Conversion-Rate
- SQL-zu-Opportunity-Rate
- Opportunity-zu-Close-Rate
- Lead-Volumen pro Kanal (Paid, Organic, Outbound, Events, Referral)

**Kanal-Performance-Daten**
- Cost-per-Lead (CPL) pro Kanal
- Cost-per-MQL pro Kanal
- Cost-per-Opportunity pro Kanal
- Budget-Verteilung pro Kanal (CHF/Monat)

**Content- und Conversion-Daten**
- Anzahl aktiver Lead-Magnete und deren Conversion-Raten
- Landing-Page-Conversion-Raten (Besucher zu Lead)
- E-Mail-Sequenz-Performance (Open Rate, Reply Rate, Booked Meetings)

## Analyseprozess

**Schritt 1: Rückwärts-Kalkulation des benötigten Pipeline-Inputs**
- Ziel-Revenue ÷ ACV = Anzahl benötigter gewonnener Deals
- Benötigte Deals ÷ Win-Rate = Anzahl benötigter Opportunities
- Benötigte Opportunities ÷ SQL-zu-Opportunity-Rate = Anzahl benötigter SQLs
- Benötigte SQLs ÷ MQL-zu-SQL-Rate = Anzahl benötigter MQLs
- Benötigte MQLs ÷ Lead-zu-MQL-Rate = Anzahl benötigter Leads (Total)
- Ergebnis: Der tatsächliche monatliche Lead-Bedarf als harte Zahl

**Schritt 2: Ist-Volumen vs. Soll-Volumen je Funnel-Stage**
- Aktuelles Monatsdurchschnitt MQLs den berechneten Soll-MQLs gegenüberstellen
- Gap in absoluten Zahlen und als Prozent ausweisen
- Gap auf CHF-Basis monetarisieren: Gap-MQLs × CPO × Win-Rate × ACV = entgangener Revenue
- Prüfen ob der Gap primär ein Volumen-, ein Qualitäts- oder ein Konversionsproblem ist

**Schritt 3: Kanal-Beitrag und Effizienz-Analyse**
- Für jeden Kanal: Anteil am Lead-Volumen, Anteil am MQL-Volumen, Anteil am gewonnenen Revenue
- Verhältnis berechnen: Kanal-Budget-Anteil vs. Revenue-Beitrags-Anteil
- Kanäle in vier Quadranten einteilen: Hoher Beitrag/hohe Effizienz (skalieren), Hoher Beitrag/niedrige Effizienz (optimieren), Niedriger Beitrag/hohe Effizienz (investieren), Niedriger Beitrag/niedrige Effizienz (stoppen)
- CPO (Cost per Opportunity) als Primär-Metrik je Kanal berechnen

**Schritt 4: Konversions-Engpass-Lokalisierung**
- Jede Funnel-Stage gegen Benchmarks prüfen:
  - Lead-zu-MQL: Best-in-Class 25–35 %, schwach unter 10 %
  - MQL-zu-SQL: Best-in-Class 35–50 %, schwach unter 15 %
  - SQL-zu-Opportunity: Best-in-Class 60–75 %, schwach unter 30 %
  - Opportunity-zu-Close: Best-in-Class 25–35 % (B2B SaaS), schwach unter 12 %
- Die Stage mit der grössten Abweichung vom Benchmark ist der primäre Hebel

**Schritt 5: Content- und Conversion-Path-Effizienz**
- Welche Lead-Magnete generieren MQLs, welche nur Kontakte?
- Landing-Page-Conversion-Rate unter 2 % signalisiert Copy- oder Offer-Problem
- Formular-Abandon-Rate über 60 % signalisiert Friction-Problem
- E-Mail-Nurturing: Reply Rate unter 1 % signalisiert Relevanz-Problem

## Bewertungslogik

**Reifegrad-Modell: Demand Generation Fitness (5 Stufen)**

**Stufe 1 — Reaktiv (kein System)**
Keine definierte MQL-Definition, kein CRM-Tracking, Lead-Volumen abhängig von Zufalls-Inbound oder sporadischen Kampagnen. Gap-Berechnung nicht möglich mangels Datenbasis. CHF-Schaden: nicht quantifizierbar, aber strukturell erheblich.

**Stufe 2 — Fragmentiert (Inseln ohne Verbindung)**
Einzelne Kanäle laufen, aber ohne Attribution. CPL bekannt, CPO unbekannt. MQL-Definition existiert aber nicht im CRM abgebildet. Kanal-Performance wird nicht gegenübergestellt. Typisches Symptom: "Wir generieren Leads, aber Sales ist unzufrieden."

**Stufe 3 — Funktional (Messung vorhanden, Optimierung fehlt)**
Funnel-Metriken dokumentiert, Coverage-Gap berechenbar. Kanal-Beiträge bekannt. Konversionsraten werden jedoch nicht systematisch verbessert. Budget-Entscheide noch teilweise auf Bauchgefühl basiert. Lead-zu-MQL-Rate unter 15 %.

**Stufe 4 — Optimiert (datengetrieben, Gap aktiv geschlossen)**
Monatliche Gap-Analyse als Standard. Kanal-Budget wird auf Basis von CPO, nicht CPL allokiert. Konversionspfade werden A/B-getestet. MQL-zu-SQL-Rate über 25 %. Sales und Marketing einigen sich monatlich auf gemeinsame Pipeline-Ziele.

**Stufe 5 — Prädiktiv (Pipeline wird geplant, nicht gehofft)**
Demand-Gen-Output ist planbar auf Quartalsbasis. Forecasting-Modell vorhanden. Lead-Bedarf wird automatisch gegen Revenue-Ziel berechnet. Neue Kanäle werden mit definierten KPIs getestet, bevor sie skaliert werden. MQL-zu-SQL-Rate über 35 %, CPO sinkt QoQ.

## Output

- **Gap-Tabelle**: Ist vs. Soll je Funnel-Stage (Leads, MQLs, SQLs, Opportunities) mit CHF-Monetarisierung des Gaps
- **Kanal-Effizienz-Matrix**: Vier-Quadranten-Darstellung aller aktiven Kanäle nach Beitrag und Effizienz
- **Primärer Engpass**: Eine benannte Stage im Funnel mit grösster Hebelwirkung
- **Reifegrad-Einordnung**: Stufe 1–5 mit konkreter Begründung
- **Budget-Umverteilungs-Empfehlung**: Welche Kanäle mehr, welche weniger Budget erhalten sollten — mit Begründung

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Gap-Zahl berechnen und ins CRM-Dashboard integrieren — ab sofort monatlich sichtbar
- Den schwächsten Konversionspunkt im Funnel identifizieren und isoliert testen (z. B. Formular verkürzen, CTA-Text ändern)
- Kanal mit höchstem CPO und niedrigstem Revenue-Beitrag pausieren oder Budget halbieren
- MQL-Definition zwischen Marketing und Sales schriftlich fixieren — eine A4-Seite, kein 20-seitiges Konzept

**Mittelfristig (1–3 Monate)**
- Attribution-Modell einrichten: Welcher Kanal hat welchen Deal beeinflusst? (First-Touch, Last-Touch, Multi-Touch)
- CPO als primäre Budget-Allokations-Metrik einführen, CPL als sekundäre Metrik behandeln
- Lead-Nurturing-Sequenzen für die Stage mit höchstem Drop-off aufbauen
- Monatliches Pipeline-Review zwischen Marketing und Sales mit gemeinsamer Gap-Analyse einführen

**Strategisch (3–12 Monate)**
- Prädiktives Forecasting-Modell aufbauen: Lead-Bedarf wird automatisch aus Revenue-Ziel berechnet
- Kanal-Portfolio diversifizieren: Kein einzelner Kanal sollte mehr als 40 % des MQL-Volumens liefern
- Content-Attribution vollständig in CRM integrieren: Welcher Content-Asset hat welche MQL-Konversion beeinflusst?
- Demand-Gen-Reife von Stufe 3 auf Stufe 4–5 entwickeln mit definierten Meilensteinen pro Quartal

## Performanceboost Perspektive

Die meisten B2B-KMUs in der Deutschschweiz haben kein Budget-Problem — sie haben ein Zurechnungs-Problem. Budgets werden auf Kanäle verteilt, die sich gut anfühlen, nicht auf Kanäle, deren CPO bekannt ist. Performanceboost startet jedes Engagement mit der Rückwärts-Kalkulation aus Schritt 1: Revenue-Ziel zu Lead-Bedarf. Diese Zahl — der monatlich benötigte MQL-Input — ist der Anker für alles Folgende. Ohne diese Zahl ist Budget-Allokation Spekulation.

Wir messen nicht Klicks und Impressionen. Wir messen Cost-per-Opportunity und den Anteil jedes Kanals am tatsächlich gewonnenen Revenue in CHF. Das erfordert eine saubere CRM-Integration, klare MQL/SQL-Definitionen und Attribution, die nicht im Marketing-Tool steckenbleibt, sondern bis zum Dealabschluss durchzieht. In der Praxis bedeutet das oft: Wir finden in den ersten vier Wochen einen Kanal, der 30–40 % des Budgets verbraucht, aber weniger als 10 % des Revenues liefert — und ein anderer Kanal läuft unterfinanziert, obwohl er 3x effizienter ist. Den Gap zu berechnen ist nicht das Ziel. Das Ziel ist, ihn mit dem richtigen Mitteleinsatz zu schliessen.
