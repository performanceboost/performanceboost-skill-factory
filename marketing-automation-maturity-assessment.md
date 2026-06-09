# Marketing Automation Maturity Assessment

## Zweck
Dieses Skill-Dokument bewertet den tatsächlichen Reifegrad einer Marketing-Automation-Infrastruktur — nicht nach installierten Tools, sondern nach operativer Wirkung. Die meisten B2B-KMU unterschätzen systematisch, wo sie stehen: Sie verwechseln «wir haben HubSpot» mit «wir betreiben Marketing Automation». Das Modell legt offen, welcher Anteil der potenziellen Automatisierungsleistung heute tatsächlich genutzt wird und wo Revenue durch manuelle Lücken verloren geht.

## Wann verwenden
- Vor einem Marketing-Automation-Projekt, um den Ausgangszustand zu dokumentieren und Quick Wins zu priorisieren
- Nach einer Tool-Implementierung, wenn unklar ist, ob das System wirklich genutzt wird oder nur existiert
- Wenn MQL-Volumen stagniert trotz steigendem Werbebudget
- Wenn Sales sich über Lead-Qualität beschwert, ohne dass es eine gemeinsam definierte Qualifikationsdefinition gibt
- Bei der Vorbereitung einer CRM-Migration oder Tech-Stack-Konsolidierung

## Input

**Technische Infrastruktur**
- Welches Marketing-Automation-Tool ist im Einsatz (HubSpot, ActiveCampaign, Marketo, Brevo, Mailchimp, manuell)?
- Welches CRM ist verbunden — und ist die Verbindung bidirektional?
- Welche Datenquellen fliessen in das System (Website, Ads, Events, Webinare, CRM-Aktivitäten)?
- Gibt es ein aktives Lead-Scoring-Modell?

**Prozesse und Flows**
- Welche automatisierten Sequenzen laufen aktiv (nicht nur erstellt, sondern aktiv)?
- Gibt es eine dokumentierte MQL-Definition mit Scoring-Schwellenwert?
- Gibt es einen definierten Marketing-to-Sales-Übergabeprozess mit SLA?
- Wie viele manuelle Schritte enthält der aktuelle Lead-Follow-up-Prozess?

**Performance-Daten**
- Aktuelle MQL-Volumen pro Monat
- MQL-zu-SQL-Konversionsrate
- Durchschnittliche Zeit vom First-Touch bis MQL-Übergabe
- E-Mail-Open-Rates und Click-Through-Rates der aktiven Nurturing-Sequenzen
- Anteil der Leads, die nie kontaktiert werden («Lead Decay»)

## Analyseprozess

1. **Tool-Bestand vs. Tool-Nutzung trennen**
   - Liste alle lizenzierten Tools auf
   - Für jedes Tool: Wird es täglich/wöchentlich aktiv genutzt oder ist es primär «Datengrab»?
   - Benchmark: Best-in-Class-Unternehmen nutzen 70–80% der lizenzierten Automation-Features; typische KMU nutzen unter 30%

2. **Sequenz-Audit**
   - Alle vorhandenen E-Mail-Sequenzen und Workflows listen
   - Für jede Sequenz: Ist sie aktiv? Wann wurde sie zuletzt geändert? Hat sie einen klaren Conversion-Zweck?
   - Klassifizierung: Broadcast (kein Trigger), reaktiv (einfacher Trigger), verhaltensbasiert (mehrstufige Logik)

3. **CRM-Synchronisation prüfen**
   - Fliessen Marketing-Aktivitäten in das CRM? (E-Mail-Öffnungen, Seitenbesuche, Formular-Ausfüllungen)
   - Kann Sales die Marketing-Historie eines Leads sehen, bevor er kontaktiert?
   - Werden Deals/Opportunities-Daten zurück ins Marketing-Automation-System gespielt?

4. **Lead-Scoring-Qualität bewerten**
   - Gibt es ein Scoring-Modell? Wenn ja: enthält es demografische UND Verhaltens-Scores?
   - Ist der MQL-Schwellenwert empirisch kalibriert (basierend auf historischen Conversion-Daten) oder willkürlich gesetzt?
   - Wird Scoring aktiv für Sequenz-Trigger verwendet?

5. **Lead-Decay-Rate messen**
   - Anteil der Leads, die in den letzten 90 Tagen ins CRM eingegangen sind, aber nie eine automatisierte oder manuelle Folge-Kommunikation erhalten haben
   - Benchmark: Bei Unternehmen ohne Automation verlieren 40–60% der generierten Leads jeglichen Kontakt nach dem ersten Touch

## Bewertungslogik

**Stufe 1 — Manuell (Score 0–20/100)**
Keine Marketing-Automation-Software im Einsatz oder reine Broadcast-E-Mails ohne Trigger. Jeder Lead-Follow-up ist manuell. MQL-Definition existiert nicht formal. Typischer Schaden: Lead-Decay-Rate über 60%, Vertrieb entscheidet nach Bauchgefühl über Prioritäten.

**Stufe 2 — Reaktiv (Score 21–40/100)**
Ein Tool ist lizenziert und sendet einfache Willkommens-Sequenzen oder Formular-Bestätigungen. Kein bidirektionales CRM-Sync. Scoring fehlt oder ist nur demografisch. Lead-Decay-Rate 40–60%. MQL-Übergabe erfolgt nach Zeitintervall, nicht nach Verhalten.

**Stufe 3 — Strukturiert (Score 41–60/100)**
Mehrere aktive Sequenzen für unterschiedliche Buyer-Journey-Phasen. Grundlegendes Lead-Scoring vorhanden. CRM-Verbindung besteht, ist aber primär einseitig (Marketing → CRM). MQL-Definition ist dokumentiert. Lead-Decay-Rate 20–40%. Nurturing-Content ist generisch, nicht nach ICP-Segment differenziert.

**Stufe 4 — Verhaltensbasiert (Score 61–80/100)**
Automatisierung reagiert auf spezifische Verhaltens-Signale (Seitenbesuche, Content-Downloads, E-Mail-Klicks auf bestimmte Topics). Bidirektionales CRM-Sync aktiv. Scoring-Modell enthält beide Dimensionen (fit + engagement). Sales erhält automatisierte Alert-Notifications bei Score-Schwellenwerten. Lead-Decay-Rate unter 20%.

**Stufe 5 — Prädiktiv & Revenue-integriert (Score 81–100/100)**
Scoring-Modell ist empirisch kalibriert und wird quartalsweise mit Conversion-Daten abgeglichen. Segmentierung ist dynamisch und ICP-basiert. Revenue-Daten (Deal-Grösse, Produkt, Segment) fliessen zurück und steuern Nurturing-Logik. Pipeline-Velocity-Metriken sind in Automation-Entscheidungen integriert. MQL→SQL-Rate: 30–40% (Branchenbest-in-Class); typischer KMU-Durchschnitt: 8–15%.

## Output

- Reifegrad-Score (0–100) mit Einordnung in die 5 Stufen
- Feature-Nutzungs-Matrix: Welche Automation-Funktionen sind lizenziert vs. aktiv genutzt vs. nicht vorhanden
- Lead-Decay-Analyse: Quantifizierung verlorener Leads pro Quartal in Anzahl und geschätztem Pipeline-Verlust (CHF)
- Priorisierte Lücken-Liste nach Impact (Revenue-Relevanz × Implementierungsaufwand)
- CRM-Synchronisations-Bewertung: Welche Datenpunkte fehlen im Bidirektional-Sync
- Benchmark-Vergleich: Aktuelle Metriken vs. Branchenbenchmarks für Unternehmensgrösse und Sektor

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Alle «schlafenden» Leads der letzten 90 Tage identifizieren und Re-Engagement-Sequenz aktivieren (typischer Recovery: 5–12% der totgeglaubten Leads)
- Formular-Bestätigungs-E-Mails auf mehrstufige Willkommens-Sequenz (3 E-Mails, 7 Tage) upgraden — kostet null neue Leads, erhöht die Aktivierungsrate
- MQL-Definition schriftlich fixieren: Minimum Scoring-Dimensionen, Schwellenwert, Übergabe-SLA

**Mittelfristig (1–3 Monate)**
- Bidirektionales CRM-Sync einrichten: Sales-Aktivitäten (E-Mails, Calls, Deal-Stage-Updates) fliessen zurück in Automation-Scoring
- Lead-Scoring-Modell mit Verhaltens-Dimension ergänzen: Website-Engagement, Content-Affinität, E-Mail-Klick-Muster
- Segmentierte Nurturing-Sequenzen nach ICP-Tier erstellen (mindestens 2 Segmente: Enterprise-fit vs. SME-fit)

**Strategisch (3–12 Monate)**
- Scoring-Kalibrierung: Historische Wins/Losses analysieren und rückwirkend mit Scoring-Daten abgleichen — MQL-Schwellenwert empirisch justieren
- Pipeline-Velocity-Integration: Nurturing-Intensität an Deal-Stage koppeln (Leads in aktiven Deals bekommen andere Sequenzen als kalte Kontakte)
- Reporting-Dashboard aufbauen: Weekly Automation-Health-Check mit MQL-Volumen, Decay-Rate, Sequenz-Performance, SQL-Conversion

## Performanceboost Perspektive

Die grösste Fehlinvestition in Marketing Automation ist nicht das falsche Tool — es ist das richtige Tool, das falsch betrieben wird. Wir erleben regelmässig Situationen, in denen KMU CHF 800–2'000 pro Monat für HubSpot oder ActiveCampaign ausgeben und de facto Broadcast-E-Mail-Software betreiben. Der Reifegrad liegt bei Stufe 2, die Lizenzkosten entsprechen Stufe 4.

Unser Einstieg ist immer das Audit, bevor die erste Empfehlung ausgesprochen wird. Das Maturity-Assessment gibt uns in 2–3 Stunden ein klares Bild, welche drei bis fünf Interventionen den grössten Revenue-Impact haben. Wir optimieren bestehende Infrastruktur, bevor wir neue empfehlen — weil der grösste Hebel fast immer in der Nutzungstiefe liegt, nicht im Tool-Wechsel. Wenn das Scoring-Modell stimmt und der CRM-Sync bidirektional läuft, steigen MQL→SQL-Raten in unseren Projekten typischerweise um 40–80% — ohne zusätzliches Werbebudget.
