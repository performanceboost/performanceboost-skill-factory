# Conversion Path Analysis

## Zweck
Dieses Skill-Dokument analysiert alle Pfade, die ein Lead vom ersten Kontaktpunkt bis zur MQL-Übergabe an Sales zurücklegt. Die meisten B2B-Unternehmen kennen ihren Cost-per-Lead — aber nicht, wo genau zwischen Lead-Generierung und Sales-Gespräch der grösste Anteil ihrer Pipeline verloren geht. Diese Analyse macht Drop-off-Punkte, Conversion-Brüche und Sub-optimale Channel-Kombinationen sichtbar und übersetzt sie in konkrete CHF-Verluste.

## Wann verwenden
- Wenn der Cost-per-MQL deutlich höher ist als erwartet, obwohl Lead-Generierungskosten stabil sind
- Wenn Marketing und Sales unterschiedliche Erklärungen für die Pipeline-Lücke haben und keine gemeinsame Datenbasis existiert
- Vor einer Entscheidung über Kanal-Budget-Allokation — um zu verstehen, welche Channels die qualitativ hochwertigsten Pfade produzieren, nicht nur die günstigsten Leads
- Nach einer Redesign- oder Funnel-Änderung, um sicherzustellen, dass Conversion-Rates nicht gesunken sind
- Wenn ABM-Kampagnen evaluiert werden und unklar ist, ob Multi-Touch-Pfade besser konvertieren als Single-Touch-Pfade

## Input

**Tracking-Infrastruktur**
- Ist GA4 korrekt eingerichtet mit Conversion-Events (Formular-Ausfüllungen, Demo-Buchungen, Content-Downloads)?
- Sind UTM-Parameter auf allen bezahlten und organischen Kanälen konsistent gesetzt?
- Gibt es CRM-Attribution (welcher Kanal/welche Kampagne ist mit jedem Lead verknüpft)?
- Ist ein Multi-Touch-Attributions-Modell aktiv, oder wird nur First-Touch oder Last-Touch gemessen?

**Funnel-Daten (letzte 90 Tage)**
- Gesamtzahl Website-Besucher pro Kanal
- Conversion-Rate Website-Besucher → Lead (nach Kanal und Landing Page)
- Conversion-Rate Lead → MQL (Gesamt und nach Lead-Quelle)
- Conversion-Rate MQL → SQL
- Conversion-Rate SQL → Opportunity (gebuchtes Gespräch oder Demo)
- Durchschnittliche Zeit zwischen jedem Übergang

**Channel-Mix-Daten**
- Welche Kanäle erzeugen Leads (LinkedIn Ads, Google Search, SEO, E-Mail, Events, Referral)?
- Anteil der Leads pro Kanal
- Cost-per-Lead pro Kanal
- MQL-Rate pro Kanal (nicht nur Lead-Volumen)
- Gibt es Multi-Touch-Daten: Welche Kanal-Kombinationen führen öfter zu Closed-Won?

**Content-Conversion-Daten**
- Welche Landing Pages oder Content-Assets generieren am meisten Leads?
- Welche haben die höchste Lead-zu-MQL-Conversion-Rate (nicht nur die höchste Anzahl Leads)?
- Welche Call-to-Actions performen am besten in welchen Funnel-Phasen?

## Analyseprozess

1. **Funnel-Visualisierung mit Volumina und Rates**
   - Jeden Funnel-Schritt mit absolutem Volumen und prozentualer Conversion-Rate dokumentieren
   - Branchen-Benchmarks einsetzen: B2B-Durchschnitt Website-zu-Lead: 1–3%; Best-in-Class: 4–7%. Lead-zu-MQL: 15–25% (durchschnittlich); Best-in-Class: 30–45%. MQL-zu-SQL: 8–15% (Durchschnitt); Best-in-Class: 30–40%
   - Jede Stufe, die unter Benchmark liegt, als «Leck» kennzeichnen

2. **Drop-off-Punkt-Identifikation**
   - Grösster absoluter Verlust: Wo gehen die meisten Leads verloren (nicht prozentual, sondern in Absolutzahlen)?
   - Grösster relativer Verlust: Wo ist die Conversion-Rate am schlechtesten im Vergleich zum Benchmark?
   - Diese zwei Punkte sind selten identisch — beide müssen adressiert werden, aber mit unterschiedlicher Priorität
   - Beispiel: Ein Trichter mit 1'000 Leads und 40% MQL-Rate verliert weniger absolut bei 10% MQL→SQL als ein Trichter mit 500 Leads und 80% MQL-Rate bei 5% MQL→SQL

3. **Channel-Qualitäts-Matrix**
   - Für jeden aktiven Kanal: Lead-Volumen, Cost-per-Lead, MQL-Rate, Cost-per-MQL, SQL-Rate, Cost-per-SQL
   - Häufigster Fehler: Kanäle werden nach Cost-per-Lead optimiert, obwohl ein günstigerer Lead eine 5x schlechtere MQL-Rate hat und der effektive Cost-per-SQL 3x höher ist
   - Benchmark: Google Search (high-intent Keywords) typische MQL-Rate: 25–40%; LinkedIn Ads (Content-Download): 8–15%; Kalt-E-Mail ohne Automation: 3–8%

4. **Multi-Touch-Pfad-Analyse**
   - Wenn Attributionsdaten vorhanden: Welche Kanal-Sequenzen führen zu den besten Abschlüssen?
   - Typisches Muster in B2B-KMU: First-Touch über Paid Search, Nurturing via Content/E-Mail, Closing-Trigger via direktem Outreach oder Demo-Request nach LinkedIn-Retargeting
   - Single-Touch-Attribution systematisch auf False Negatives prüfen: Kanal B bekommt keine Anerkennung, obwohl er konsistent im Pfad der besten Deals vorkommt

5. **Zeit-zu-Conversion-Analyse**
   - Durchschnittliche Zeit von First-Touch bis MQL, MQL bis SQL, SQL bis Opportunity
   - Wo entstehen «Stau-Punkte» — Phasen, in denen Leads überdurchschnittlich lange verweilen?
   - Benchmark B2B-KMU: First-Touch bis MQL: 14–45 Tage (je nach Produkt-Komplexität); MQL bis Sales-Kontakt: Best-in-Class unter 24 Stunden; typischer KMU-Durchschnitt: 3–7 Tage (jeder zusätzliche Tag reduziert Conversion um geschätzte 5–8%)

## Bewertungslogik

**Stufe 1 — Keine Messbarkeit (Score 0–20/100)**
Keine konsistente UTM-Tracking-Struktur. Conversion-Events in GA4 nicht oder falsch konfiguriert. CRM-Daten sind nicht mit Marketing-Quellen verknüpft. Entscheidungen über Kanal-Budget basieren auf Impressionen und Klicks, nicht auf Pipeline-Daten. Typischer Schaden: Budgets werden auf Kanäle konzentriert, die günstige Leads, aber schlechte MQLs produzieren — CHF-Verlust durch Fehlallokation oft 30–50% des gesamten Werbebudgets.

**Stufe 2 — Partielle Messung (Score 21–40/100)**
GA4 misst Formular-Ausfüllungen, aber keine durchgehende Funnel-Verbindung bis zum SQL. First-Touch-Attribution wird als einziges Modell genutzt. MQL-Rate nach Kanal ist unbekannt. Marketing und Sales messen unterschiedliche Dinge und können keine gemeinsame Funnel-Ansicht erstellen.

**Stufe 3 — Funnel-transparent (Score 41–60/100)**
Vollständiger Funnel von Lead bis SQL ist messbar. Channel-spezifische Conversion-Rates bekannt. Drop-off-Punkte sind identifiziert, aber noch nicht systematisch adressiert. Attribution ist primär Last-Touch oder First-Touch, Multi-Touch fehlt. MQL→SQL-Rate ist bekannt: typischerweise 10–20%.

**Stufe 4 — Optimierungs-aktiv (Score 61–80/100)**
Regelmässige Funnel-Reviews mit Channel-Performance-Vergleich. Drop-off-Punkte werden aktiv mit A/B-Tests oder gezielten Massnahmen adressiert. Multi-Touch-Attribution gibt ein realistischeres Bild der Channel-Wirkung. Zeit-zu-MQL ist bekannt und wird aktiv optimiert. MQL→SQL-Rate: 20–32%.

**Stufe 5 — Prädiktiv gesteuert (Score 81–100/100)**
Conversion-Daten fliessen zurück in Kampagnen-Optimierung (Google/LinkedIn Conversion-basiertes Bidding auf SQL-Signale, nicht nur Lead-Signale). Multi-Touch-Attributions-Modell ist kalibriert und wird für Budget-Allokations-Entscheidungen genutzt. Funnel-Velocity wird als Leading-Indicator für Monats-Pipeline genutzt. MQL→SQL-Rate: 30–42%. Cost-per-SQL: unter CHF 400–800 (je nach Segment und ACV).

## Output

- Funnel-Visualisierung mit allen Stufen, Volumina, Conversion-Rates und Benchmark-Abweichungen
- Drop-off-Punkt-Ranking: Priorisierte Liste der grössten Verlust-Punkte nach absolutem und relativem Impact
- Channel-Qualitäts-Matrix: Jeder Kanal mit Cost-per-Lead, MQL-Rate, Cost-per-MQL, SQL-Rate, Cost-per-SQL
- Quantifizierter Verlust pro Drop-off-Punkt in CHF (auf Basis durchschnittlichem Deal-Wert und Conversion-Wahrscheinlichkeit)
- Attribution-Assessment: Wie zuverlässig sind die vorliegenden Daten und welche Blind Spots bestehen?
- Priorisierte Optimierungs-Agenda: Die drei Massnahmen mit dem höchsten Einzel-Impact auf Pipeline-Volumen

## Empfehlungen

**Quick Wins (0–30 Tage)**
- UTM-Parameter-Konsistenz sicherstellen: Alle aktiven Paid-Kampagnen auf korrektes UTM-Tagging prüfen — ohne diesen Schritt sind alle weiteren Analysen unzuverlässig
- GA4 Conversion-Events überprüfen: Werden Formular-Ausfüllungen, Demo-Buchungen und Content-Downloads als separate Conversion-Events getrackt?
- CRM-Quellenfeld ausfüllen: Alle neuen Leads erhalten zwingend eine dokumentierte Lead-Quelle — ab sofort, auch rückwirkend schätzen für bestehende Pipeline

**Mittelfristig (1–3 Monate)**
- Channel-Qualitäts-Matrix aufbauen und in monatliches Marketing-Meeting integrieren: Nicht Cost-per-Lead, sondern Cost-per-MQL als primäre Steuerungsgrösse
- MQL-zu-Sales-Kontakt-Zeit messen und SLA definieren: Best Practice ist unter 4 Stunden für hochscorende MQLs — jede Stunde Verzögerung kostet messbar Conversion-Rate
- Erstes Multi-Touch-Attributions-Modell einrichten (HubSpot oder GA4 nativer Multi-Touch): Nicht um perfekte Daten zu haben, sondern um systematische First-Touch-Blind-Spots zu reduzieren

**Strategisch (3–12 Monate)**
- Conversion-basiertes Bidding auf SQL-Signale aufbauen: Google und LinkedIn können auf «qualifiziertes Gespräch» optimieren statt auf «Formular-Ausfüllung» — setzt saubere CRM-GA4-Verbindung voraus
- Funnel-Velocity-Dashboard einrichten: Wöchentliche Ansicht auf Time-in-Stage pro Funnel-Stufe als Leading-Indicator für monatliche Pipeline-Prognose
- Multi-Touch-Analyse ausweiten: Welche First-Touch/Last-Touch-Kanal-Kombinationen führen statistisch zu den grössten Deals? Budget-Allokation folgt dieser Erkenntnis

## Performanceboost Perspektive

Conversion Path Analysis ist für uns keine Reporting-Aufgabe — es ist eine Diagnose-Pflicht vor jeder Budget-Empfehlung. Wir haben wiederholt gesehen, wie B2B-KMU monatlich CHF 5'000–12'000 in LinkedIn-Kampagnen investieren, die günstige Leads produzieren und gleichzeitig die schlechteste MQL-Rate aller Kanäle haben — und niemand hat die kanalspezifischen Conversion-Rates gemessen.

Unser Unterschied: Wir verknüpfen Marketing-Daten zwingend mit CRM-Daten, bevor wir Kanal-Empfehlungen aussprechen. Und wir messen nicht nur Leads — wir messen Pipeline-Wert. Ein Kanal, der CHF 50 pro Lead kostet und 40% MQL-Rate hat, ist fast immer besser als ein Kanal mit CHF 20 pro Lead und 8% MQL-Rate. Diese Rechnung zu machen ist keine Rocket Science — aber sie wird in der Mehrzahl der KMU-Marketing-Teams nicht gemacht. Wir machen sie im ersten Monat jedes Engagements.
