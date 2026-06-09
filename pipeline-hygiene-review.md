# Pipeline Hygiene Review

## Zweck
Eine volle Pipeline und eine saubere Pipeline sind zwei verschiedene Dinge. Die meisten CRM-Systeme sind Friedhöfe: Deals, die seit Monaten nicht bewegt wurden, Close Dates, die automatisch um 30 Tage verschoben werden, und Opportunities, deren letzter Kontakt ein unbeantwortes E-Mail vor sechs Wochen war. Dieser Skill diagnostiziert Qualität und Realismus der bestehenden Opportunity-Pipeline: Stale Deals, Stage-Klumpen, fehlende Next Steps, unrealistische Close Dates und die daraus resultierenden Forecasting-Verzerrungen — mit direkter Quantifizierung des CHF-Schadens durch Phantom-Pipeline.

## Wann verwenden
- Forecast weicht regelmässig um mehr als 20% vom tatsächlichen Ergebnis ab
- Pipeline-Volumen wächst, aber Abschlüsse nehmen nicht proportional zu
- Vertriebsleitung hat das Gefühl, dass die «guten Deals» im CRM versteckt sind
- Vor einem Quartals-End-Push: Realistische Pipeline-Einschätzung statt Wunschdenken
- Nach Wachstumsphase oder Merger: Pipeline aus mehreren Quellen zusammengeführt, Qualität unklar
- Management oder Investoren fordern verlässlichere Revenue-Prognosen

## Input

**CRM-Rohdaten (vollständiger Export)**
- Alle offenen Opportunities: Stage, Deal Value, Close Date (aktuell und ursprünglich), Erstelldatum, Letzte Aktivität
- Aktivitäts-Log je Opportunity: Art, Datum, Ersteller
- Stage-History: Wann wurde die Opportunity in welche Stage gesetzt?
- Zuständiger Rep
- Alle Felder, die als Qualifikationskriterien definiert sind (Budget, Authority, Need, Timeline)

**Prozess-Referenz**
- Offizielle Stage-Definitionen und typische Verweildauer je Stage
- Definition «Stale Deal» des Unternehmens (falls vorhanden)
- Forecast-Kategorien und deren Kriterien (Commit, Best Case, Pipeline)

## Analyseprozess

1. **Stale Deal Identifikation**
   - Definition anwenden: Kein Aktivitäts-Log seit mehr als 2× der durchschnittlichen Stage-Verweildauer = Stale
   - In Abwesenheit einer Unternehmensdefinition: Stale = keine Aktivität seit 21 Tagen (transaktionaler B2B) bzw. 45 Tagen (komplexer B2B)
   - Segmentierung: Stale nach Stage, nach Rep, nach Alter (21–45 Tage / 45–90 Tage / 90+ Tage)
   - Berechnung Phantom Pipeline: Summe aller Stale Deals in CHF — dieser Betrag ist aus dem Forecast zu entfernen
   - Benchmark: Best-in-Class: unter 10% der Pipeline-Summe sind Stale Deals. Red Flag: über 25%

2. **Stage-Klumpen analysieren**
   - Welche Stage hat unverhältnismässig viele Deals (über 35% aller offenen Opportunities)?
   - «Stage Stacking» ist ein Warnsignal: Reps parken Deals in einer Stage, weil der nächste Schritt unklar ist oder Arbeit bedeutet
   - Häufigste Klumpen-Stage: «Proposal Sent» oder «Angebot versendet» — Deal wurde übergeben, aber niemand verfolgt aktiv
   - Identifikation ob Klumpen strukturell (Prozess-Gap) oder verhaltensbedingt (Rep-spezifisch) ist

3. **Next-Step-Qualität bewerten**
   - Wie viele offene Deals haben einen dokumentierten, datierten Next Step?
   - Best-in-Class: 90%+ aller Deals in Stage 2+ haben einen konkreten Next Step mit Datum
   - Differenzierung: «Nachfassen» ist kein Next Step. «Demo mit CFO am 15.03.» ist ein Next Step
   - Berechnung: Deals ohne dokumentierten Next Step × durchschnittlichem Deal Value = ungesteuertes Pipeline-Volumen

4. **Close Date Realismus testen**
   - Analyse der Close Date Historie: Wie oft wurde das Close Date je Opportunity verschoben? Wie weit?
   - Deals mit mehr als 2 Verschiebungen: Wahrscheinlichkeitskorrektur auf maximal 20% — unabhängig von der Stage
   - «Date Pushing Pattern»: Monatliche Analyse, ob Close Dates systematisch Richtung Quartalsende clustern (Aktivitäts-Illusion kurz vor QE)
   - Realismus-Check: Kann der Deal in der verbleibenden Zeit bis zum Close Date realistisch abgeschlossen werden? Minimum-Aktivitäten prüfen

5. **Qualifikationsvollständigkeit prüfen**
   - Für alle Deals ab Stage 2: Sind Budget, Authority, Need, Timeline dokumentiert?
   - Unvollständig qualifizierte Deals in Stage 3+ sind ein kritisches Forecasting-Risiko
   - Berechnung: «Unqualifizierte Late-Stage Deals» × Deal Value = Forecasting-Risikosumme
   - Best-in-Class: 85%+ der Stage-3-Deals sind vollständig qualifiziert

6. **Rep-spezifische Muster identifizieren**
   - Gibt es Reps mit systematisch höherem Anteil an Stale Deals?
   - Gibt es Reps, die Close Dates häufiger verschieben als andere?
   - Gibt es Reps mit Stage-Klumpen in spezifischen Stages? (Coaching-Implikation)
   - Wichtig: Rep-Daten nur für Coaching nutzen, nie öffentlich vergleichen ohne Kontext

## Bewertungslogik

**Stufe 1 — Unkontrollierte Pipeline**
Mehr als 35% Stale Deals. Kein dokumentierter Next Step in über 60% der Opportunities. Close Dates systematisch verschoben. Forecast-Abweichung über 40%. CRM ist faktisch unbrauchbar für Entscheidungen. Vertriebsleitung vertraut CRM nicht und arbeitet mit eigenen Listen.

**Stufe 2 — Teilweise erfasst, wenig verlässlich**
Stale Deals 25–35%. Next Steps in etwa 40% der Deals vorhanden. Close Date Shifting ohne System. Forecast-Abweichung 25–40%. Stage-Klumpen sichtbar aber nicht adressiert. CRM-Daten werden «als Anhaltspunkt» genutzt.

**Stufe 3 — Grundhygiene etabliert**
Stale Deals 15–25%. Next Steps in 60% der Deals. Close Dates werden sporadisch bereinigt. Forecast-Abweichung 15–25%. Erste Hygiene-Reviews finden statt, aber nicht systematisch.

**Stufe 4 — Saubere, steuerbare Pipeline**
Stale Deals unter 15%. Next Steps in 80%+ der Deals mit Datum. Close Date Shifting selten und begründet. Forecast-Abweichung unter 15%. Wöchentlicher Pipeline Review als Standard. Stage-Klumpen werden aktiv aufgelöst.

**Stufe 5 — Pipeline als Entscheidungsinstrument**
Stale Deals unter 5%. 90%+ der Stage-2+-Deals vollständig qualifiziert mit Next Steps. Forecast-Abweichung unter 10%. Automatische Hygiene-Alerts im CRM. Pipeline wird von Vertrieb und Management gleichermassen als verlässliche Grundlage für Entscheidungen genutzt.

## Output

- **Pipeline-Bereinigungsliste**: Alle Stale Deals mit Empfehlung (aktivieren, Stage zurücksetzen, schliessen) und verantwortlichem Rep
- **Phantom-Pipeline-Betrag**: CHF-Summe, die aus dem Forecast zu entfernen ist — «echte Pipeline» vs. «CRM-Pipeline»
- **Stage-Klumpen-Report**: Identifikation der problematischen Stage(s) mit struktureller Erklärung
- **Next-Step-Coverage-Rate**: Prozentualer Anteil mit dokumentiertem Next Step, segmentiert nach Rep und Stage
- **Close-Date-Realismus-Score**: Anteil unrealistischer Close Dates mit CHF-Bewertung
- **Forecasting-Korrektur**: Bereinigter Forecast-Wert nach Anwendung der Hygiene-Filter
- **Maturity Level Einschätzung**: Stufe 1–5 mit quantifizierten Auswirkungen auf Revenue

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Alle Deals ohne Aktivität seit 45+ Tagen: Rep kontaktiert Prospect mit klarer Ja/Nein-Frage — Deal aktivieren oder schliessen. Keine «offenen» Leichen im CRM
- «Keine Aktivität seit X Tagen»-Alert im CRM aktivieren (HubSpot, Salesforce, Pipedrive — alle haben diese Funktion, kaum jemand nutzt sie)
- Close Dates aller Deals im laufenden Quartal manuell verifizieren: Realistisch oder Wunschdenken?

**Mittelfristig (1–3 Monate)**
- Wöchentlicher Pipeline Review institutionalisieren: 30-minütige Struktur, nicht Statusrunde — jeder Deal der Woche mit Last Activity, Next Step, Close Date
- CRM-Pflichtfeld «Next Step mit Datum» für Stage 2+ einführen: kein Advancement ohne dokumentierten Next Step
- Deal-Score-Modell implementieren: Automatische Gewichtung basierend auf Qualifikationsvollständigkeit, Aktivitätsfrequenz und Close Date History

**Strategisch (3–12 Monate)**
- Automatisiertes Pipeline-Hygiene-Scoring aufbauen: Weekly automatischer Bericht mit Hygiene-Score je Rep
- Forecasting-Kategorien (Commit / Best Case / Pipeline) mit objektiven Criteria hinterlegen — nicht Rep-Schätzung, sondern Stage + Qualifikation + Aktivität
- Win/Loss-Daten zur Kalibrierung nutzen: Welche Pipeline-Signale korrelieren mit tatsächlichem Abschluss?

## Performanceboost Perspektive

Performanceboost führt Pipeline Hygiene Reviews regelmässig bei neuen Klienten durch — und die Erkenntnis ist konsistent: Die durchschnittliche Deutschschweizer KMU-Pipeline hat 30–40% Phantom Deals. Das bedeutet: Der Vertriebsleiter glaubt, er hat CHF 800'000 Pipeline. Tatsächlich steuerbar sind CHF 480'000 bis 560'000.

Der gefährlichste Phantom Deal ist nicht der offensichtlich stale Deal — er ist der Deal, den der Rep «im Gefühl hat». CRM zeigt Stage 3, letzte Aktivität vor 6 Wochen, aber der Rep sagt «Der kommt noch, ich kenne den.» In 70% dieser Fälle kommt er nicht.

Performanceboost nutzt eine einfache, aber wirkungsvolle Methode zur Pipeline-Bereinigung: den «Ehrlichen Forecast». Jeder Rep bewertet seine eigenen Deals nach drei Fragen — Hat der Prospect in den letzten 30 Tagen aktiv geantwortet? Gibt es einen vereinbarten Next Step? Weiss ich, wer die Kaufentscheidung trifft? Drei Ja = im Forecast. Weniger als drei = Watch List. Diese Methode ist nicht glamourös, aber sie reduziert Forecast-Abweichungen in der Regel innerhalb eines Quartals von 30%+ auf unter 15%.
