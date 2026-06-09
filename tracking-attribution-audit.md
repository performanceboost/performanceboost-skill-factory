# Tracking & Attribution Audit

## Zweck
Dieser Skill diagnostiziert systematisch, ob die Tracking-Infrastruktur eines Unternehmens valide Daten liefert — und ob die Attribution-Logik Budgetentscheidungen unterstützt oder sabotiert. Falsche oder fehlende Attribution ist kein technisches Problem, sondern ein Revenue-Problem: Unternehmen skalieren Kanäle, die nicht konvertieren, und kürzen Budgets bei Kanälen, die tatsächlich Deals generieren. Der Audit macht diese Blindspots sichtbar und bewertet den finanziellen Schaden fehlerhafter Daten in CHF.

## Wann verwenden
- Das Marketing-Team kann nicht zuverlässig sagen, welcher Kanal welchen Teil des Pipeline-Volumens verantwortet
- Google Ads, LinkedIn Ads oder Meta Ads zeigen stark abweichende Conversion-Zahlen als das CRM
- Conversion-Tracking wurde vor mehr als 6 Monaten nicht geprüft oder angepasst
- Ein neuer Kanal wird getestet und es ist unklar, ob Conversions korrekt erfasst werden
- Das Unternehmen plant Budgetverschiebungen zwischen Kanälen und braucht verlässliche Attribution als Entscheidungsbasis

## Input

**Tracking-Infrastruktur**
- Zugang zu Google Tag Manager (Container-Konfiguration, alle Tags/Trigger/Variablen)
- Google Analytics 4 Property: Events-Liste, Conversions-Konfiguration, Data Streams
- Pixel-Setup: Meta Pixel, LinkedIn Insight Tag, ggf. weitere (TikTok, XING)
- Server-Side Tracking vorhanden: ja/nein, Plattform (z. B. stape.io, GTM Server)

**CRM & Conversion-Daten**
- CRM-System (HubSpot, Salesforce, Pipedrive): Lead-Quelle-Felder und wie sie befüllt werden
- Anzahl Leads der letzten 90 Tage nach Kanal (CRM)
- Anzahl Leads der letzten 90 Tage nach Kanal (Ads-Plattformen)
- Anzahl abgeschlossener Deals nach Ursprungskanal (letzten 12 Monate)

**Attribution-Logik**
- Welches Attribution-Modell ist in GA4 aktiv? (Last Click, Data-Driven, Linear)
- Welche Attribution nutzen die Ads-Plattformen intern?
- Gibt es ein CRM-seitiges Attribution-Feld (z. B. "Original Source" in HubSpot)?
- UTM-Namenskonvention: dokumentiert und einheitlich durchgesetzt ja/nein

**Business-Kontext**
- Durchschnittlicher Deal-Wert (CHF)
- Anzahl Deals pro Monat
- Anteil Deals, bei denen Quelle im CRM als "Unknown" oder leer eingetragen ist

## Analyseprozess

1. **Tag Manager Audit**
   - Alle aktiven Tags auflisten und gegen bekannte Conversion-Ziele abgleichen
   - Auf doppelte Tags prüfen (z. B. GA4 Event und GA4 Config mehrfach gefeuert)
   - Trigger-Logik validieren: Feuern Tags auf den richtigen Seiten/Events?
   - Staging vs. Production: werden Tags nur auf Live-Domain aktiv?

2. **GA4 Event & Conversion Audit**
   - Alle als Conversion markierten Events auflisten
   - Für jeden Conversion-Event: Stichprobe von 10 realen Conversions im Debug-Modus nachvollziehen
   - Parameter-Vollständigkeit prüfen: werden relevante Parameter (campaign, source, medium, content) übergeben?
   - Cross-Domain-Tracking: falls Subdomain oder externer Checkout, ist Konfiguration korrekt?

3. **UTM-Konsistenz-Check**
   - Alle aktiven Kampagnen-URLs auf UTM-Parameter prüfen (utm_source, utm_medium, utm_campaign, utm_content)
   - Groß-/Kleinschreibung, Trennzeichen und Namenskonventionen auf Einheitlichkeit prüfen
   - Anteil Traffic ohne UTM-Parameter aus Paid-Kanälen messen (Zielwert: unter 5 %)

4. **CRM-Plattform-Abgleich (Discrepancy Analysis)**
   - Lead-Volumina aus CRM vs. Ads-Plattformen für die letzten 90 Tage gegenüberstellen
   - Abweichung je Kanal in % berechnen: Toleranzbereich bis 15 %, kritisch ab 30 %
   - "Unknown"-Anteil im CRM-Feld "Lead Source" messen: Zielwert unter 10 %
   - Falls HubSpot: Original Source Drill-Down auf Plausibilität prüfen

5. **Attribution-Modell-Implikation**
   - Last-Click-Anteil am Budget-Reporting identifizieren
   - Für die letzten 6 Monate: wie viel Budget wurde basierend auf Last-Click-Attribution entschieden?
   - Multi-Touch-Pfade aus GA4 Conversion Paths analysieren: welche Kanäle erscheinen nur als Assist, nie als Last Click?
   - Finanziellen Schaden kalkulieren: (Anteil Budget in falsch attribuierten Kanälen) × (Avg. Deal Value) × (geschätzte Conversion-Rate-Differenz)

6. **Server-Side Tracking Bewertung**
   - Browser-seitiges vs. server-seitiges Event-Volumen vergleichen (falls vorhanden)
   - Consent-Rate messen: bei unter 70 % Opt-in-Rate ist client-seitiges Tracking strukturell unvollständig
   - Cookie-Lifetime-Problem: ITP/ETP-Impact auf Safari-User quantifizieren

## Bewertungslogik

**Reifegrad-Modell: 5 Stufen**

**Stufe 1 — Blind (kritisch)**
Keine einheitliche UTM-Logik, über 40 % Unknown im CRM, Conversion-Tracking nicht verifiziert, Attribution-Entscheidungen basieren auf Plattform-Reports ohne CRM-Abgleich. Geschätzter CHF-Schaden: 20–40 % des Paid-Media-Budgets wird falsch alloziert.

**Stufe 2 — Fragmentiert**
Grundlegendes Tracking vorhanden, aber inkonsistent. UTM-Parameter teilweise gesetzt, 20–40 % Unknown im CRM, keine einheitliche Attribution-Logik. Plattform- und CRM-Daten werden getrennt betrachtet, kein systematischer Abgleich.

**Stufe 3 — Funktional**
Tracking läuft stabil, UTM-Konvention dokumentiert und zu 80 % eingehalten. Conversion-Events verifiziert. CRM-Unknown unter 20 %. Attribution-Modell definiert, aber noch Last-Click-dominant. Kein Server-Side Tracking.

**Stufe 4 — Verlässlich**
Vollständige UTM-Abdeckung (unter 5 % ohne Parameter), CRM-Unknown unter 10 %, regelmässige Discrepancy-Checks, Data-Driven Attribution in GA4 aktiv. Multi-Touch-Pfade werden analysiert. Server-Side Tracking in Evaluierung oder Pilotbetrieb.

**Stufe 5 — Präzise**
Server-Side Tracking aktiv, Consent-unabhängige Datenbasis, CRM-Attribution und Plattform-Attribution synchronisiert. Finanziell fundierte Budget-Allokation möglich. Attribution-Reports wöchentlich reviewed und als Entscheidungsbasis genutzt.

## Output

- **Tracking-Health-Scorecard**: je Kanal (GA4, GTM, Meta, LinkedIn, CRM) mit Status (Grün/Gelb/Rot) und konkretem Befund
- **Discrepancy-Tabelle**: Plattform-Leads vs. CRM-Leads je Kanal, letzten 90 Tage, Abweichung in %
- **UTM-Audit-Log**: Anteil Traffic mit korrekten UTM-Parametern, Fehlertypen und betroffene Kampagnen
- **Attribution-Lücken-Bericht**: welche Kanäle systematisch unter- oder überbewertet werden und warum
- **CHF-Schaden-Kalkulation**: konservative Schätzung des finanziellen Impacts falscher Attribution, basierend auf Avg. Deal Value und historischem Budget
- **Priorisierte Massnahmen-Liste**: nach Impact und Aufwand sortiert

## Empfehlungen

**Quick Wins (0–30 Tage)**
- UTM-Namenskonvention dokumentieren und in einem zentralen UTM-Builder verankern (z. B. Google Sheet mit Dropdown)
- Alle aktiven GTM-Tags im Staging-Modus verifizieren — doppelte Tags deaktivieren
- GA4 Conversion-Events im DebugView gegen 5 reale Formulareinsendungen validieren
- CRM-Feld "Lead Source" für alle Leads der letzten 30 Tage auf Vollständigkeit prüfen

**Mittelfristig (1–3 Monate)**
- Monatlichen Discrepancy-Report einführen: CRM-Leads vs. Plattform-Conversions, Abweichungen über 15 % eskalieren
- Attribution-Modell von Last Click auf Data-Driven umstellen (Voraussetzung: min. 30 Conversions/Monat je Kanal)
- Multi-Touch-Analyse in GA4 aktivieren und Kanal-Assist-Raten in Budget-Entscheidungen einbeziehen
- Server-Side Tracking evaluieren: Pilotprojekt für primären Conversion-Event (z. B. Demo-Request)

**Strategisch (3–12 Monate)**
- Server-Side Tracking vollständig implementieren — Abhängigkeit von Browser-Cookies und Consent-Raten reduzieren
- CRM-Attribution und GA4-Attribution automatisch abgleichen (via Make oder native Integrationen)
- Budget-Allokation formal an Attribution-Daten knüpfen: quartalsweise Review-Prozess mit definierten Schwellenwerten
- Revenue Attribution: Deals aus CRM rückwirkend mit Ursprungskanal verknüpfen und CLV je Kanal berechnen

## Performanceboost Perspektive

Die meisten KMU-Tracking-Audits scheitern an zwei Stellen: Sie bleiben technisch ("GTM ist konfiguriert") ohne den finanziellen Impact zu berechnen — oder sie produzieren eine Fehlerliste ohne Priorisierung. Performanceboost führt den Tracking-Audit immer mit einer konkreten CHF-Schätzung ab: Wie viel Budget wurde in den letzten 12 Monaten auf Basis fehlerhafter Attribution entschieden? Diese Zahl macht den Audit von einem technischen Pflichtübung zur Geschäftsentscheidung.

Zweiter Unterschied: Wir prüfen nicht nur, ob Tags feuern — wir prüfen, ob die Daten Budgetentscheidungen tragen können. Ein Tag kann technisch korrekt feuern und trotzdem falsche Attribution erzeugen, wenn UTM-Parameter inkonsistent gesetzt oder CRM-Felder nicht synchronisiert sind. Der Audit deckt beide Ebenen ab: technische Integrität und attributive Verlässlichkeit.
