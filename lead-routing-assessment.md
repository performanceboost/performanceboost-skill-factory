# Lead Routing Assessment

## Zweck
Dieses Skill-Dokument bewertet systematisch, ob Leads korrekt, schnell und nachvollziehbar zu den richtigen Sales-Reps gelangen. Fehlerhafte Lead-Routing-Prozesse sind eine der am meisten unterschätzten Umsatzlecks im B2B-Vertrieb: Ein Lead, der 24 Stunden auf Bearbeitung wartet, hat statistisch eine 21-mal geringere Konversionschance als einer, der innerhalb von 5 Minuten kontaktiert wird. Das Assessment legt offen, ob technische Logik, menschliche Prozesse und Attribution übereinstimmen — oder ob Leads systematisch im Nirgendwo verschwinden.

## Wann verwenden
- Wenn Sales-Reps unterschiedlich ausgelastete Pipelines haben (einer mit 80 Leads, einer mit 8)
- Wenn MQLs generiert werden, aber keine Folgeaktivität im CRM erscheint
- Wenn das Unternehmen mehrere Produkte, Regionen oder Marktsegmente hat
- Wenn ein neues CRM eingeführt wurde oder die Sales-Organisation gewachsen ist
- Wenn Lead-Attribution im CRM-Reporting inkonsistent ist

## Input

**Aus CRM (technische Analyse):**
- Routing-Regeln im CRM dokumentiert und exportiert (HubSpot Workflows, Salesforce Assignment Rules, Pipedrive Automation)
- Durchschnittliche Zeit zwischen Lead-Erstellung und erster Aktivität je Rep (letzte 90 Tage)
- Leads ohne zugewiesenen Owner (Orphan Leads) — Anzahl und Alter
- Lead-Volumen je Rep (letzte 12 Monate) — Verteilungsgleichmässigkeit prüfen
- Attribution-Feld: Wie viele Leads haben keinen Lead-Source-Eintrag?

**Aus Prozess-Interview (Sales-Lead, Marketing-Ops, je 30 Minuten):**
- Wie wird entschieden, wer einen Lead bekommt? Ist das dokumentiert?
- Was passiert mit einem Lead ausserhalb der Arbeitszeiten?
- Gibt es SLAs für die Reaktionszeit auf MQLs? Werden sie gemessen?
- Was passiert mit einem Lead, wenn der zugewiesene Rep krank oder ausserhaus ist?

**Aus Marketing-Automation:**
- Trigger-Bedingungen für MQL-Status (Score-Schwellwert, Formular-Submission, Content-Download)
- Zeitverzögerung zwischen MQL-Trigger und CRM-Übergabe (sollte <5 Minuten sein)
- Gibt es Leads, die MQL-Status erreichen, aber nie ins CRM übergeben werden?

## Analyseprozess

1. **Routing-Logik rekonstruieren und dokumentieren**
   - Alle aktiven Routing-Regeln aus dem CRM exportieren
   - Sequenz visuell kartieren: Wann wird welche Regel ausgelöst? Gibt es Überschneidungen oder Lücken?
   - Spezifische Szenarien testen: Was passiert mit einem Lead aus dem Kanton Graubünden, der für Produkt B qualifiziert ist und ausserhalb der Bürozeiten eingeht?
   - Edge Cases identifizieren: Leads, die in keine Regel fallen (Fallback-Verhalten prüfen)

2. **Speed-to-Lead messen**
   - CRM-Zeitstempel: Lead Created → First Activity (Anruf, E-Mail, Meeting geloggt)
   - Benchmarks:
     - Best-in-Class: <5 Minuten bei automatisiertem Erstkontakt, <1 Stunde bei manuell bearbeitetem Erstkontakt
     - Akzeptabel: <4 Stunden
     - Kritisch: >24 Stunden (trifft auf einen Grossteil der Schweizer KMU zu)
   - Verteilung nach Rep: Wer antwortet schnell, wer nicht?
   - Zeitliche Muster: Schlechtere Speed-to-Lead an bestimmten Wochentagen oder Uhrzeiten?

3. **Verteilungsgleichmässigkeit prüfen**
   - Lead-Volumen je Rep last 90 Tage: Standardabweichung berechnen
   - Korrelation zwischen Lead-Volumen und Deal-Qualität: Bekommt der beste Rep auch die besten Leads?
   - Round-Robin vs. Skill-basiertes Routing: Welches System ist eingesetzt, und entspricht es der Strategie?
   - Territoriale Überschneidungen: Werden Leads für dieselbe Firma manchmal an verschiedene Reps geleitet?

4. **SLA-Compliance messen**
   - Falls SLAs dokumentiert sind: Einhaltungsquote der letzten 90 Tage berechnen
   - Falls keine SLAs: Ist-Reaktionszeiten dokumentieren und als Basis für SLA-Definition nutzen
   - Eskalationsprozess prüfen: Was passiert nach 4 Stunden ohne Reaktion auf einen MQL?

5. **Attribution-Konsistenz prüfen**
   - Quote der Leads mit vollständiger Attribution (Lead Source, Campaign, Channel) messen (Ziel: >90%)
   - Abgleich: Stimmt die CRM-Attribution mit dem Marketing-Automation-System überein?
   - Häufigste Attribution-Lücken: Direct Traffic, offline Quellen, manuelle Imports

## Bewertungslogik

**Level 1 — Kein System (0–15 Punkte)**
Leads werden manuell und ad hoc verteilt. Kein dokumentierter Prozess. Reaktionszeit abhängig von Verfügbarkeit und Aufmerksamkeit des Sales-Leads. Orphan-Lead-Rate >20%. Keine Attribution. Typisch für: Ein-bis-Drei-Personen-Vertriebsteams ohne dediziertes CRM-Setup.

**Level 2 — Basisregeln (16–35 Punkte)**
Erste Routing-Regeln im CRM vorhanden, aber nicht vollständig. Round-Robin oder manuelle Zuweisung. Speed-to-Lead im Durchschnitt 4–24 Stunden. Keine SLAs. Attribution lückenhaft (50–70% Abdeckung). Edge Cases nicht abgefangen.

**Level 3 — Strukturiert (36–55 Punkte)**
Routing-Logik dokumentiert. Segmentierung nach Quelle oder Produktinteresse vorhanden. Speed-to-Lead durchschnittlich <4 Stunden. SLAs informell vereinbart. Attribution >75%. Regelmässige manuelle Überprüfung der Routing-Ergebnisse. Schweizer B2B-KMU-Durchschnitt liegt hier.

**Level 4 — Automatisiert (56–75 Punkte)**
Vollständige Routing-Automatisierung ohne manuelle Eingriffe für Standardfälle. Speed-to-Lead <1 Stunde, bei High-Intent-Leads automatisierter Erstkontakt in <5 Minuten. SLAs dokumentiert und im CRM überwacht. Attribution >90%. Eskalationslogik für unbearbeitete MQLs aktiv.

**Level 5 — Prädiktiv (76–100 Punkte)**
Skill-basiertes oder Account-basiertes Routing (richtiger Rep für richtigen Account-Typ). Lead-Score fliesst in Routing-Entscheidung ein. Real-Time-Benachrichtigung bei High-Intent-Signalen. Vollständige Attribution. SLA-Compliance >95% gemessen. A/B-Tests auf Routing-Logik (welcher Rep konvertiert welchen Lead-Typ besser?).

## Output

- Routing-Prozess-Flowchart mit identifizierten Lücken und Edge Cases
- Speed-to-Lead-Report je Rep und im Teamdurchschnitt
- Orphan-Lead-Liste (Leads ohne Owner oder ohne Aktivität >7 Tage)
- Attribution-Abdeckungsquote nach Kanal
- SLA-Compliance-Rate (sofern SLAs existieren) oder SLA-Empfehlung basierend auf Ist-Daten
- Priorisierte Massnahmenliste mit geschätztem CHF-Impact

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Orphan Leads bereinigen: Alle Leads ohne Owner sofort zuweisen, Fallback-Routing-Regel erstellen
- Speed-to-Lead-Messung aktivieren: CRM-Property oder Dashboard für «Zeit bis erste Aktivität» einrichten
- E-Mail-Alert für Sales-Rep bei neuem MQL: sofortige Benachrichtigung, kein manuelles CRM-Checken
- Pflichtfeld Lead Source: kein Lead-Import ohne Quellen-Attribution möglich

**Mittelfristig (1–3 Monate)**
- SLA-Dokument erstellen und unterzeichnen: MQL-Reaktionszeit <2 Stunden Bürozeiten, Eskalation nach 4 Stunden
- Routing-Logik nach Produkt oder Segment differenzieren, falls mehrere Produkte oder Regionen vorhanden
- Round-Robin vs. Skill-based Routing evaluieren: Welches Modell passt zur Teamstruktur?
- Ferienvertretung und Ausfall-Routing definieren: Wer bekommt Leads, wenn Rep X nicht erreichbar ist?

**Strategisch (3–12 Monate)**
- Account-based Routing einführen: Leads von bestehenden Accounts gehen direkt an den Relationship Owner
- Lead-Score als Routing-Kriterium nutzen: High-Score-Leads priorisiert oder direkt an Senior Reps
- Attribution-Modell finalisieren: Server-Side Tracking für lückenlose Herkunftsverfolgung
- Routing-Performance-Review quartalsweise: Konversionsrate nach Rep und Lead-Typ auswerten

## Performanceboost Perspektive

Routing klingt technisch. Es ist strategisch. Wer einen Lead bekommt und wie schnell, entscheidet über die Konversion — nicht nur das Messaging. In der Praxis sehen wir bei Schweizer KMU typischerweise zwei Probleme gleichzeitig: zu langsame Reaktion auf warme Leads (4–48 Stunden statt 4 Minuten) und unfaire oder unsystematische Verteilung, die bestimmte Reps systematisch benachteiligt.

Performanceboost betrachtet Routing als Teil der Revenue-Architektur — nicht als CRM-Konfigurationsaufgabe. Die Routing-Logik muss die Vertriebsstrategie abbilden: Welche Segmente sind prioritär? Welcher Rep schliesst welchen Kunden-Typ am besten ab? Was passiert mit einem Lead ausserhalb der Bürozeiten? Diese Fragen sind nicht technisch — sie sind strategisch. Wir beantworten sie zuerst, bevor wir eine einzige Automation anfassen.
