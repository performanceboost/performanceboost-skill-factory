# Lifecycle Stage Audit

## Zweck
Dieses Skill-Dokument bewertet die Definition, Konsistenz und Datenqualität der Lifecycle-Stages im CRM. Falsch konfigurierte oder inkonsistent genutzte Stages sind der Hauptgrund für unzuverlässige Pipeline-Berichte und manipulierbare Forecasts. Ein Lifecycle Stage Audit deckt auf: Zombie-Deals (die Pipeline aufblähen, ohne Abschlusschance), falsch klassifizierte Leads (die falsches Reporting erzeugen) und Stage-Progressions-Probleme (die Entscheidungen verzögern oder verhindern).

## Wann verwenden
- Wenn Forecast-Zahlen regelmässig nicht mit dem tatsächlichen Abschluss übereinstimmen
- Wenn Marketing und Sales unterschiedliche Zahlen für dieselbe Pipeline-Stufe berichten
- Wenn Deals im CRM monatelang in derselben Stage verbleiben, ohne Aktivität
- Wenn ein neues Lead-Scoring-Modell oder ein neues CRM eingeführt wurde
- Wenn das Unternehmen eine Due Diligence vorbereitet und saubere Pipeline-Daten benötigt

## Input

**Aus CRM (vollständiger Daten-Export):**
- Alle aktiven Deals mit Stage, Erstellungsdatum, letzter Aktivität, Eigentümer und Deal-Wert
- Stage-History aller Deals der letzten 24 Monate (Stage-Wechsel mit Zeitstempel)
- Anzahl Deals je Stage, segmentiert nach Rep und Quartal
- Alle Lifecycle-Stage-Definitionen wie im CRM konfiguriert (Felder, Automatisierungen, Trigger)

**Aus Interviews (Sales-Lead, Marketing-Ops, je 45 Minuten):**
- Wie wird entschieden, wann ein Deal von einer Stage in die nächste verschoben wird?
- Gibt es formale Kriterien — oder entscheidet jeder Rep selbst?
- Wie wird ein Stagnations-Deal behandelt? Wann wird er als verloren eingestuft?
- Sind Lifecycle-Stage-Definitionen schriftlich dokumentiert und allen Reps bekannt?

**Aus Dokumentation:**
- Schriftliche Definition von MQL, SQL, Opportunity, Proposal Sent, Closed Won/Lost — falls vorhanden
- Sales Playbook oder Qualifizierungsframework (MEDDIC, BANT, SPICED oder eigenes)
- CRM-Konfigurationsprotokoll: Wann wurden Stages zuletzt geändert?

## Analyseprozess

1. **Stage-Definitionen auditieren**
   - Alle CRM-Stages auflisten und auf Vollständigkeit prüfen: Haben alle Stages eine schriftliche Eintrittsbedingung?
   - Eintrittskriterien für jede Stage von mindestens 3 Reps unabhängig abfragen — stimmen die Antworten überein?
   - Kritische Prüfung: Sind die Definitionen verhaltensbasiert (was hat der Lead getan?) oder intentionsbasiert (was glaubt der Rep)? Verhaltensbasiert = reproduzierbar; intentionsbasiert = subjektiv und manipulierbar.
   - Übergang Opportunity → Proposal: Ist «Proposal Sent» ein tatsächlicher Stage oder wird es manchmal mit «Verbal Commitment» gleichgesetzt?

2. **Stage-Progressions-Analyse**
   - Durchschnittliche Verweildauer (Days in Stage) je Stage berechnen — letzte 4 Quartale
   - Benchmarks für Schweizer B2B-KMU (Median, abhängig von Produktkomplexität):
     - MQL → SQL: 1–5 Tage (länger = Routing-Problem oder fehlende Nurturing-Sequenz)
     - SQL → Opportunity: 3–14 Tage (länger = Qualifizierungsschwäche)
     - Opportunity → Proposal: 7–21 Tage (länger = interne Prozessbremse)
     - Proposal → Close: 14–45 Tage (länger = fehlende Entscheidungsträger oder Budget-Problem)
   - Stage-Rückwärtsbewegungen identifizieren: Deals, die von Opportunity zurück zu SQL degradiert wurden — wie häufig? Warum?
   - Übersprungene Stages: Deals, die von MQL direkt zu Closed Won sprangen — valide oder Datenproblem?

3. **Zombie-Deal-Identifikation**
   - Definition Zombie-Deal: Offen, letzte Aktivität >30 Tage, kein geplanter nächster Schritt
   - Zombie-Deal-Rate berechnen: Anzahl Zombies / Total offene Deals × 100
   - Kritisch: >15% Zombie-Rate verzerrt Forecast und Conversion-Metriken erheblich
   - Verteilung nach Rep: Welcher Rep hat die höchste Zombie-Konzentration? Oft ein Coaching-Signal.
   - CHF-Wert der Zombie-Pipeline berechnen: Typischer Befund in Schweizer KMU — 20–40% der ausgewiesenen Pipeline ist in Wirklichkeit nicht aktiv verfolgbar

4. **Falschklassifizierungen erkennen**
   - Deals, die als «Opportunity» geführt werden, aber kein Budget bestätigt haben (BANT-Check)
   - Leads, die als «MQL» gelten, aber keinen Lead-Score über dem Schwellwert aufweisen
   - «Closed Lost»-Deals ohne Verlustgrund: Datenqualitätslücke und Forecasting-Blindstelle
   - Deals, die nur «Closed Won» wurden, weil der Rep den Stage manuell ohne echten Abschluss gesetzt hat (Kontrolle durch Rechnungsvergleich, falls möglich)

5. **CRM-Automation-Konsistenz prüfen**
   - Welche Stage-Wechsel werden automatisch ausgelöst (Formular-Submission, Meeting gebucht)? Funktionieren diese Trigger wie erwartet?
   - Gibt es Stage-Automationen, die sich gegenseitig überschreiben?
   - Lifecycle-Stage im Contact-Record vs. Deal-Record: Stimmen sie überein oder widersprechen sie sich?

## Bewertungslogik

**Level 1 — Unstrukturiert**
Keine schriftlichen Stage-Definitionen. Reps setzen Stages nach persönlichem Verständnis. Zombie-Rate >30%. Keine Stage-History verfügbar. Forecasting basiert auf Deal-Anzahl, nicht auf Konversionswahrscheinlichkeit. Pipeline-Zahlen sind Meinungen, keine Fakten.

**Level 2 — Inkonsistent**
Definitionen existieren, werden aber nicht einheitlich angewendet. Deutliche Diskrepanz zwischen Reps in Stage-Zeitstempeln. Zombie-Rate 15–30%. Rückwärtsbewegungen häufig, aber undokumentiert. Closed-Lost-Gründe fehlen in >40% der Fälle.

**Level 3 — Strukturiert**
Stage-Definitionen schriftlich und mehrheitlich bekannt. Zombie-Rate 8–15%. Stage-Progressions-Zeiten im akzeptablen Bereich. Closed-Lost-Pflichtfeld vorhanden, aber nicht immer präzise ausgefüllt. Forecast basiert auf Stage-Wahrscheinlichkeiten. Schweizer KMU-Standard: Gut geführte Teams befinden sich hier.

**Level 4 — Konsistent**
Verhaltensbasierte Stage-Kriterien, die von allen Reps gleichwertig angewendet werden. Zombie-Rate <8%. Regelmässige Pipeline-Review-Meetings mit Stage-Überprüfung. Attribution vollständig. Rückwärtsbewegungen dokumentiert und analysiert. Win/Loss-Analyse systematisch.

**Level 5 — Prädiktiv**
AI-gestütztes Stage-Scoring: CRM berechnet automatisch Abschlusswahrscheinlichkeit basierend auf Verhaltens- und historischen Daten. Zombie-Deals werden automatisch markiert und eskaliert. Stage-Progressions-Anomalien lösen automatische Coaching-Alerts aus. Forecasting-Genauigkeit >90%. Deal-Zyklen sind vorhersehbar auf ±10%.

## Output

- Stage-Definitionsdokument: IST-Zustand mit Lücken und Widersprüchen
- Stage-Progressions-Report: Days in Stage je Stage, Reps im Vergleich
- Zombie-Deal-Liste mit Massnahmenvorschlag (reaktivieren, verlieren, eskalieren)
- Falschklassifizierungs-Report: Deals, die ihren Stage nicht erfüllen — nach Rep und Stage
- Forecast-Korrekturfaktor: Bereinigtes Pipeline-Volumen nach Zombie-Abzug (in CHF)
- Stage-Definitions-Template: Vorlage für überarbeitete, verhaltensbasierte Eintrittskriterien

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Zombie-Deals sofort aus aktiver Pipeline entfernen: Neuer Stage «On Hold» oder direkt «Closed Lost» mit Reaktivierungsplan
- Closed-Lost-Pflichtfeld technisch erzwingen: kein Deal kann ohne Verlustgrund geschlossen werden
- Stage-Definitionen in einem gemeinsamen Dokument für alle Reps sichtbar machen (Notion, Confluence, HubSpot Knowledge Base)
- Pipeline-Review-Meeting einführen: wöchentlich, 30 Minuten, Fokus auf Stage-Bewegungen und nächste Schritte

**Mittelfristig (1–3 Monate)**
- Verhaltensbasierte Stage-Kriterien gemeinsam mit dem Sales-Team entwickeln: Was muss bewiesen sein, damit ein Deal vorwärtsbewegt wird?
- Stage-Automationen aufbauen: Meeting gebucht = automatisch SQL, Proposal gesendet = automatisch nächster Stage
- Rückwärtsbewegungen systematisch dokumentieren und analysieren: Welche Stages werden am häufigsten zurückgesetzt? Das ist ein Trainingsbedarf-Signal.
- Win/Loss-Tracking aktivieren: Top-3-Gründe je Quartal automatisch aggregieren

**Strategisch (3–12 Monate)**
- Deal-Scoring-Modell auf historischen Konversionsdaten basieren: Welche Faktoren (Segment, Deal-Grösse, Lead-Quelle) korrelieren mit Abschluss?
- Predictive Forecasting einführen: Kombination aus Stage-Wahrscheinlichkeit und historischer Konversionsrate je Stage
- Quarterly Stage-Audit institutionalisieren: Sind die Definitionen noch passend zur Vertriebsstrategie?

## Performanceboost Perspektive

Ein aufgeblähtes Pipeline-Reporting ist keine Kleinigkeit — es ist eine Entscheidungsgefahr. Wenn 30% der ausgewiesenen Pipeline Zombie-Deals sind, überinvestiert das Unternehmen in Sales-Ressourcen, die keine echte Chance mehr haben, und unterinvestiert in Marketing, weil der Funnel «voll» aussieht.

Performanceboost führt diesen Audit immer durch, bevor wir Pipeline-Velocity oder Conversion-Optimierungen empfehlen. Denn ohne saubere Stage-Daten optimiert man Scheinzahlen. Unser Ansatz: Stage-Definitionen gemeinsam mit dem Sales-Team entwickeln — nicht für sie aufschreiben. Nur was das Team selbst definiert hat, wird auch konsistent angewendet. Das ist keine Frage der Technologie. Es ist eine Frage des gemeinsamen Verständnisses.
