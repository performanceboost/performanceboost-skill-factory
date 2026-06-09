# Dashboard Effectiveness Assessment

## Zweck
Dieser Skill bewertet, ob bestehende Dashboards tatsächlich bessere Entscheidungen ermöglichen — oder ob sie primär als Reporting-Artefakt existieren, das niemand aktiv nutzt. Ein Dashboard ist nur dann wertvoll, wenn es die richtige Person, mit der richtigen Metrik, zum richtigen Zeitpunkt, zu einer konkreten Handlung führt. Die meisten B2B-KMU haben entweder zu viele Dashboards (Datengrab-Problem) oder zu wenige (Blindflug-Problem). Dieser Skill findet heraus, welches Szenario zutrifft und was die messbaren Konsequenzen sind.

## Wann verwenden
- Dashboards existieren, aber werden in Weekly-Meetings nicht als Entscheidungsgrundlage genutzt
- Verschiedene Teams berichten unterschiedliche Zahlen für dieselbe Metrik
- Ein neues Dashboard-Tool wird evaluiert oder eingeführt
- Das Reporting kostet erhebliche Stunden pro Monat, der Nutzen ist aber unklar
- Nach einer Tracking-Umstellung: sichergestellt werden soll, dass neue Daten korrekt visualisiert werden

## Input

**Dashboard-Inventar**
- Vollständige Liste aller aktiven Dashboards (Name, Tool, primärer Nutzer, Update-Frequenz)
- Screenshots oder Zugang zu den 3–5 meistgenutzten Dashboards
- Wer hat die Dashboards erstellt? Wer sollte sie nutzen?

**Nutzungsverhalten**
- Wie oft werden die wichtigsten Dashboards pro Woche geöffnet? (Schätzung des primären Nutzers)
- In welchen Meetings werden Dashboards aktiv verwendet — und von wem?
- Wann wurde das letzte Mal eine Entscheidung aufgrund eines Dashboard-Insights getroffen? (konkret benennen)
- Gibt es Dashboards, die seit mehr als 30 Tagen niemand geöffnet hat?

**Metriken-Konfiguration**
- Welche Metriken sind in den primären Dashboards enthalten? (vollständige Liste)
- Sind Zielwerte (Targets) für die wichtigsten Metriken hinterlegt?
- Welche Metriken wurden in den letzten 6 Monaten aus Dashboards entfernt oder hinzugefügt?

**Technische Basis**
- Welche Datenquellen speisen die Dashboards (GA4, CRM, Ads-Plattformen, ERP, Manuell)?
- Welche Daten werden manuell aktualisiert vs. automatisch synchronisiert?
- Aktuellster Datenstand pro Dashboard (Latenz in Stunden/Tagen)

## Analyseprozess

1. **Dashboard-Inventarisierung und Klassifikation**
   - Alle Dashboards in drei Kategorien einteilen: Operative Dashboards (tägliche/wöchentliche Steuerung), Strategische Dashboards (monatliche/quartalsweise Reviews), Vanity Dashboards (niemand nutzt sie aktiv, keine Handlung folgt)
   - Anteil Vanity Dashboards am Gesamtbestand messen: Zielwert unter 20 %
   - Doppelungen identifizieren: werden dieselben Metriken in mehreren Dashboards unterschiedlich berechnet?

2. **Entscheidungs-Rückwärtsanalyse**
   - Für die letzten 3 Monate: 5 konkrete Entscheidungen im Marketing/Sales auflisten
   - Je Entscheidung: Welche Daten wurden genutzt? Aus welchem Dashboard? Oder aus keinem?
   - Wenn mehr als 60 % der Entscheidungen ohne aktive Dashboard-Nutzung getroffen wurden: strukturelles Nutzungsproblem

3. **Metrik-Relevanz-Check**
   - Jeden Metrik-Wert in den primären Dashboards gegen folgende Kriterien prüfen:
     - Handlungsrelevanz: führt eine Veränderung dieser Metrik zu einer konkreten Massnahme?
     - Revenue-Verbindung: lässt sich die Metrik direkt oder indirekt mit Pipeline oder Umsatz verknüpfen?
     - Kontrollierbarkeit: kann das Team diese Metrik durch eigene Entscheidungen beeinflussen?
   - Metriken, die alle drei Kriterien nicht erfüllen: Vanity Metric

4. **Aktualitäts- und Latenz-Bewertung**
   - Datenverzögerung je Dashboard messen: wann wurden die Daten zuletzt aktualisiert?
   - Latenz-Toleranz je Dashboard-Typ: Operativ max. 24 Stunden, Strategisch max. 7 Tage
   - Anteil manuell befüllter Felder vs. automatisch synchronisierter Daten: Zielwert unter 15 % manuell

5. **Nutzer-Adoption-Interview**
   - Mit 3–5 primären Dashboard-Nutzern je ein strukturiertes 15-Minuten-Gespräch führen
   - Fragen: Welches Dashboard öffnest du täglich? Was fehlte dir letzte Woche? Welche Zahl kennst du auswendig?
   - Fragen: Gab es eine Situation, in der du ein Dashboard öffnen wolltest, aber die Daten nicht vertraut hast?
   - Vertrauen in Datenbasis bewerten: wenn mehr als ein Nutzer Datenkvalität als Problem nennt, ist das ein kritischer Befund

6. **Alert- und Anomalie-System prüfen**
   - Existieren proaktive Alerts (z. B. wenn CPL um 30 % steigt, wenn MQL-Volumen unter Schwellenwert fällt)?
   - Wenn keine Alerts existieren: Dashboard ist reaktiv, nicht operativ — wird nur geöffnet, wenn man ohnehin schon weiss, dass etwas nicht stimmt

## Bewertungslogik

**Reifegrad-Modell: 5 Stufen**

**Stufe 1 — Datengrab**
Dashboards existieren, werden aber nicht regelmässig geöffnet. Metriken sind nicht mit Zielwerten verknüpft. Entscheidungen werden auf Basis von Gefühl oder Plattform-Reports getroffen, nicht auf Basis zentraler Dashboards. Daten sind 3+ Tage alt. Über 50 % der Metriken sind Vanity Metrics.

**Stufe 2 — Reporting-Artefakt**
Dashboards werden für monatliche Management-Berichte erstellt, aber nicht für operative Entscheidungen genutzt. Datenqualität wird von Nutzern angezweifelt. Kein einheitlicher Datensatz: verschiedene Abteilungen berichten verschiedene Zahlen.

**Stufe 3 — Grundfunktional**
Primäre Dashboards werden wöchentlich geöffnet. Wichtigste Metriken mit Zielwerten hinterlegt. Datenquelle für die meisten Metriken automatisch synchronisiert. Noch keine proaktiven Alerts. Entscheidungen werden gelegentlich durch Dashboards informiert.

**Stufe 4 — Entscheidungsunterstützend**
Dashboards sind fester Bestandteil von Weekly-Meetings. Metriken sind nach Audience segmentiert (CEO sieht Strategisches, Performance Marketer sieht Operatives). Proaktive Alerts für kritische Metriken aktiv. Datenbasis wird von Nutzern vertraut. Latenz operativer Dashboards unter 24 Stunden.

**Stufe 5 — Entscheidungsinfrastruktur**
Jedes Dashboard hat einen definierten Entscheidungsbereich und primären Nutzer. Anomalie-Detection aktiv. Dashboards werden vor Budgetentscheidungen als Pflicht-Input genutzt. Metriken werden quartalsweise reviewed und angepasst. Daten aus allen relevanten Systemen in einem einheitlichen Datenmodell konsolidiert.

## Output

- **Dashboard-Inventar-Klassifikation**: Operativ / Strategisch / Vanity je Dashboard, inkl. Empfehlung (behalten, konsolidieren, löschen)
- **Metrik-Audit-Tabelle**: je Metrik — Handlungsrelevanz, Revenue-Verbindung, Kontrollierbarkeit (Ja/Nein je Kriterium)
- **Nutzungs-Heatmap**: wer nutzt welches Dashboard, wie oft, mit welcher Konsequenz
- **Latenz-Report**: Datenverzögerung je System, Anteil manueller Updates
- **Vertrauens-Score**: auf Basis der Nutzer-Interviews, 1–5, mit konkreten Zitaten als Evidenz
- **Entscheidungsrelevanz-Score**: Anteil der letzten 10 Entscheidungen, die durch ein Dashboard informiert wurden

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Alle Dashboards mit letztem Öffnungsdatum auflisten — alles unter 30 Tagen ohne aktiven Nutzer archivieren
- Für die 3 wichtigsten Metriken im primären Dashboard Zielwerte eintragen (absoluter Zielwert, nicht nur Richtung)
- Wöchentliches Dashboard-Review in ein bestehendes Meeting einbetten — 10 Minuten, strukturierte Agenda: Abweichung von Zielwert, Ursache, Massnahme

**Mittelfristig (1–3 Monate)**
- Dashboard-Architektur nach Audience segmentieren: ein operatives Dashboard pro Funktion (Marketing, Sales), ein strategisches Dashboard für Geschäftsführung
- Proaktive Alerts für die 3 kritischsten Metriken einrichten (z. B. CPL +30 %, MQL-Volumen -20 %, Pipeline-Velocity -15 %)
- Alle manuell befüllten Felder auf automatische Synchronisation migrieren — Zeitaufwand für Reporting-Erstellung messen und als Baseline dokumentieren

**Strategisch (3–12 Monate)**
- Einheitliches Datenmodell definieren: wie werden Metriken unternehmensweit berechnet? Verbindliches Glossar erstellen
- Quartalsweise Metrik-Review einführen: sind die gemessenen KPIs noch die richtigen? Wachstumsphase und Strategie können Metrik-Prioritäten verschieben
- Dashboard-Nutzung als Proxy für Datenkultur messen: Anteil Entscheidungen mit Daten-Backing als eigene Metrik tracken

## Performanceboost Perspektive

Das häufigste Dashboard-Problem bei B2B-KMU ist nicht fehlende Technologie — es ist fehlende Handlungsorientierung. Dashboards werden gebaut, weil "man Daten haben sollte", nicht weil eine konkrete Entscheidungsfrage besteht. Performanceboost beginnt jeden Dashboard-Aufbau mit einer einzigen Frage: Welche Entscheidung soll dieses Dashboard in den nächsten 4 Wochen informieren? Wenn diese Frage nicht beantwortet werden kann, wird kein Dashboard gebaut.

Zweites Differenzierungsmerkmal: Wir trennen konsequent zwischen Metriken für das Managementreporting und Metriken für operative Steuerung. Viele KMU bauen ein Dashboard für beide Zwecke — und es funktioniert für keinen. Ein CEO braucht Pipeline-Velocity, CAC-Trend und Win-Rate. Ein Performance Marketer braucht CPL je Kampagne, Conversion Rate je Landing Page und Impression Share je Keyword. Wir bauen beide separat, mit separaten Update-Frequenzen und separaten Alert-Logiken.
