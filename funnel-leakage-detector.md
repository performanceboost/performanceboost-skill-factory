# Funnel Leakage Detector

## Zweck
Dieses Skill-Dokument identifiziert präzise, an welchen Stellen im B2B-Revenue-Funnel Deals, Leads und Pipeline-Volumen verloren gehen — und rechnet den CHF-Impact jeder Leckagestelle durch. Das Werkzeug verwandelt vage Wachstumsprobleme («wir brauchen mehr Leads») in konkrete, priorisierte Reparaturpunkte mit messbarem ROI. Die meisten B2B-Unternehmen verlieren mehr Revenue durch Leckagen als durch zu wenig Nachfrage.

## Wann verwenden
- Wenn Marketingbudget steigt, aber Pipeline-Volumen nicht proportional wächst
- Wenn Win Rate unter 20% liegt oder seit zwei Quartalen sinkt
- Wenn Sales über schlechte Lead-Qualität klagt, Marketing über mangelndes Follow-up
- Wenn Deal-Zyklen länger werden, ohne dass sich das durchschnittliche Deal-Volumen erhöht
- Vor jeder Entscheidung, das Demand-Generation-Budget zu erhöhen: Zuerst die Lecks stopfen

## Input

**Aus CRM (letzte 12 Monate, nach Quartal aufgeteilt):**
- Volumen je Funnel-Stage: MQL, SQL, Opportunity, Proposal Sent, Closed Won, Closed Lost
- Konversionsrate je Stage-Übergang
- Durchschnittliche Verweildauer (Days in Stage) je Stage
- Closed-Lost-Gründe (Kategorien und Häufigkeit)
- Deals ohne Aktivität >21 Tage («Zombie-Deals»)

**Aus Marketing-Automation:**
- Lead-Volumen je Kanal und Kampagne
- MQL-Rate je Lead-Source
- Nurturing-Engagement-Rate (E-Mail-Öffnungsrate, Klickrate auf Follow-up-Sequenzen)
- Leads, die nie kontaktiert wurden (>72 Stunden ohne Sales-Aktivität nach MQL-Status)

**Aus Interviews:**
- Warum werden Deals als «Kein Budget» eingestuft — fehlende Qualifizierung oder echter Budget-Mangel?
- Wie lange dauert die Erstellung eines Proposals durchschnittlich?
- Gibt es eine formalisierte Einwand-Behandlung — oder improvisiert jeder Rep?

## Analyseprozess

1. **Stage-Konversionsraten berechnen und benchmarken**
   - Jeden Stage-Übergang berechnen: MQL→SQL, SQL→Opportunity, Opportunity→Proposal, Proposal→Closed Won
   - Schweizer B2B-KMU-Benchmarks anwenden:
     - MQL→SQL: Best-in-Class 35%, Durchschnitt 18–22%, kritisch unter 12%
     - SQL→Opportunity: Best-in-Class 65%, Durchschnitt 45–55%, kritisch unter 35%
     - Opportunity→Closed Won (Win Rate): Best-in-Class 28–35%, Durchschnitt 18–22%, kritisch unter 12%
   - Abweichungen vom Benchmark je Stage dokumentieren

2. **CHF-Impact je Leckagestelle quantifizieren**
   - Formel: Leckage-Impact = (Ist-Rate − Benchmark-Rate) × Stage-Volumen × durchschnittlicher Deal-Wert
   - Beispiel: MQL→SQL-Rate bei 10% statt 22% bei 100 MQLs/Monat und CHF 15'000 Average Deal Value = CHF 18'000 verlorenes Pipeline-Potenzial pro Monat
   - Alle Leckagestellen in CHF/Monat und CHF/Jahr ausdrücken

3. **Timing-Leckagen identifizieren**
   - Days-in-Stage je Übergang messen
   - Kritische Schwellwerte: MQL-Reaktionszeit >4 Stunden reduziert Kontaktwahrscheinlichkeit um 80% (Harvard Business Review, bestätigt in DACH-Vertriebsstudien)
   - Deals, die länger als 2× der durchschnittlichen Deal-Dauer in einer Stage sind → Zombie-Deals
   - Zombie-Deal-Rate: kritisch wenn >15% der offenen Pipeline

4. **Closed-Lost-Analyse**
   - Closed-Lost-Gründe nach Häufigkeit und Volumen kategorisieren
   - Top-3-Verlustgründe auf ihre tatsächliche Ursache zurückführen:
     - «Kein Budget» → oft: falsche ICP-Qualifizierung oder falscher Zeitpunkt
     - «Zu teuer» → oft: fehlende Value-Kommunikation oder Vergleich mit falschen Wettbewerbern
     - «Kein Bedarf» → oft: zu frühe Übergabe von Marketing an Sales (Nurturing-Lücke)
   - Verlustgründe nach Stage kartieren: Wo im Funnel werden diese Deals verloren?

5. **Leckage-Prioritätsmatrix erstellen**
   - Zwei Achsen: CHF-Impact (hoch/tief) × Reparaturaufwand (hoch/tief)
   - Quick Wins: hoher Impact, tiefer Aufwand → sofort angehen
   - Strategische Projekte: hoher Impact, hoher Aufwand → planen
   - Deprioritisieren: tiefer Impact, hoher Aufwand → ignorieren

## Bewertungslogik

**Fünf Leckage-Zonen mit Schweregrad:**

**Zone 1 — Top-of-Funnel-Leckage (MQL-Qualität)**
Schweregrad Rot: MQL→SQL unter 12%. Symptom: Sales lehnt >60% der Leads ab. Ursache: ICP nicht scharf genug, Lead-Scoring-Modell kalibriert Quantity über Quality.

**Zone 2 — Handover-Leckage (Marketing→Sales-Übergang)**
Schweregrad Rot: Speed-to-Lead >4 Stunden bei >20% der MQLs. Schweregrad Gelb: Keine dokumentierten Übergabe-Kriterien. Symptom: Leads fallen zwischen Zuständigkeiten durch.

**Zone 3 — Mid-Funnel-Leckage (SQL→Opportunity)**
Schweregrad Rot: SQL→Opportunity unter 35%. Symptom: Viele Erstgespräche, wenige Folgetermine. Ursache: fehlende Qualifizierungsstruktur (MEDDIC, BANT oder equivalent), kein Proposal-Prozess.

**Zone 4 — Late-Funnel-Leckage (Proposal→Close)**
Schweregrad Rot: Win Rate unter 15%. Symptom: Proposals werden erstellt, aber Entscheidungen verzögern sich oder bleiben aus. Ursache: fehlende Entscheidungsträger im Prozess, unklarer Business Case, keine Follow-up-Struktur nach Proposal.

**Zone 5 — Post-Sale-Leckage (Churn, kein Expansion)**
Schweregrad Gelb: Churn >15%/Jahr, Expansion Revenue unter 10% des Gesamtumsatzes. Symptom: CAC-Payback-Period verlängert sich, obwohl Neukundengeschäft wächst.

## Output

- Funnel-Wasserfall-Chart: Volumen und Konversionsrate je Stage mit Benchmark-Vergleich
- Leckagestellen-Ranking nach CHF-Impact/Jahr (sortiert nach Priorität)
- Leckage-Prioritätsmatrix (Impact vs. Aufwand)
- Zombie-Deal-Liste mit Handlungsempfehlung je Deal
- Closed-Lost-Analyse: Top-3-Verlustgründe mit Volumen und Massnahmen

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Speed-to-Lead messen und auf <2 Stunden reduzieren: CRM-Alert bei neuem MQL für zuständigen Rep einrichten
- Zombie-Deals identifizieren und aus aktiver Pipeline entfernen oder reaktivieren — keine Phantom-Pipeline
- Closed-Lost-Pflichtfeld im CRM einführen: kein Deal kann ohne Verlustgrund geschlossen werden
- Top-Verlustgrund analysieren: Wenn «Kein Budget» >30% der Losses, ICP-Qualifizierungskriterien sofort schärfen

**Mittelfristig (1–3 Monate)**
- Lead-Scoring-Modell auf tatsächliche MQL→SQL-Konversion kalibrieren (rückwärts validieren: welche Scores konvertieren wirklich?)
- Mid-Funnel-Qualifizierung strukturieren: Einheitliches Qualifizierungs-Framework für alle Reps einführen
- Proposal-Prozess standardisieren: Template mit Business-Case-Kalkulation, nächste Schritte explizit definiert
- Nurturing-Sequenz für «Nicht bereit»-MQLs einrichten: 4–6 E-Mails über 6 Wochen, trigger-basiert auf Engagement

**Strategisch (3–12 Monate)**
- Revenue-Attribution-Modell für alle Kanäle implementieren: jede geschlossene Opportunity hat nachverfolgbare Herkunft
- Win/Loss-Interview-Programm aufbauen: 10–15 Interviews pro Quartal, Insights fliessen in Positioning zurück
- Pipeline-Velocity als Steuerungsgrösse einführen: Geschwindigkeit des Geldflusses durch den Funnel als Frühindikator
- CS-Expansion-Playbook entwickeln: systematisches Upsell/Cross-Sell bei Bestandskunden

## Performanceboost Perspektive

Der häufigste Reflex bei stagnierendem Wachstum ist: mehr Marketingbudget. Mehr Leads oben rein. Aber wenn der Funnel leckt, beschleunigt mehr Budget nur den Verlust. Performanceboost führt den Leakage-Detector deshalb immer durch, bevor wir ein Demand-Generation-Budget empfehlen oder erhöhen.

Der überraschendste Befund in der Praxis: Die grösste Leckage liegt selten an einem einzelnen Kanal. Sie liegt am Übergang — Marketing gibt einen Lead weiter, den Sales nicht als qualifiziert betrachtet. Oder Sales öffnet einen Lead nach 48 Stunden, wenn die Kaufabsicht längst wieder abgekühlt ist. In beiden Fällen ist das Problem kein Kanal-Problem. Es ist ein Prozess-Problem. Und Prozess-Probleme löst man nicht mit mehr Budget.
