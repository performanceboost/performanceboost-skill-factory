# Growth Bottleneck Finder

## Zweck
Die meisten B2B-Unternehmen arbeiten gleichzeitig an zehn Wachstumsinitiativen und wundern sich, warum keine davon durchbricht. Dieser Skill identifiziert den primären Engpass im Wachstumssystem — den einen Punkt, an dem Revenue systematisch verloren geht und der alle nachgelagerten Massnahmen limitiert. Basierend auf Goldrattts Theory of Constraints, adaptiert für B2B-Revenue-Systeme: Wer den Engpass nicht kennt, optimiert am falschen Ort.

## Wann verwenden
- Wachstum stagniert trotz laufender Marketing- und Sales-Aktivitäten
- Mehrere Initiativen gleichzeitig laufen, ohne dass eine messbar wirkt
- Pipeline ist vorhanden, aber Abschlussrate oder Velocity stimmt nicht
- Neue Massnahmen werden gestartet, bevor alte Probleme gelöst sind
- Budget wird erhöht, ohne proportionalen Revenue-Anstieg zu sehen

## Input

**Funnel-Daten (CRM / Marketing Automation)**
- MQL-Volumen pro Monat (letzte 6 Monate)
- MQL → SQL Conversion Rate
- SQL → Opportunity Rate
- Opportunity → Closed Won Rate
- Durchschnittliche Sales Cycle Länge
- Pipeline Velocity (CHF pro Tag)

**Traffic und Demand-Daten**
- Website-Besucher pro Monat nach Kanal
- Lead Conversion Rate (Besucher → Lead)
- Cost-per-Lead pro Kanal
- Organische vs. bezahlte Lead-Verteilung

**Qualitative Inputs (Interview oder Workshop)**
- Wo verliert das Sales-Team Deals am häufigsten?
- Welche Einwände wiederholen sich?
- Wo bricht der Übergabeprozess Marketing → Sales ab?
- Was blockiert die aktuell grössten Deals?

## Analyseprozess

1. **Funnel-Mapping: IST-Zustand dokumentieren**
   - Alle Conversion Rates von Stufe zu Stufe quantifizieren
   - Benchmark-Vergleich anstellen: MQL→SQL Best-in-Class 35%, Branchendurchschnitt 20-25%; SQL→Close Best-in-Class 30%, Durchschnitt 15-20%
   - Stufe mit grösster Abweichung vom Benchmark markieren
   - Absoluten Revenue-Schaden berechnen: Wenn MQL→SQL bei 12% statt 25% liegt und 100 MQLs/Monat generiert werden, gehen bei CHF 15'000 ACV monatlich ca. CHF 19'500 verloren

2. **Engpass-Hypothesen formulieren**
   - Schritt 1: Ist es ein Volumen-Problem (zu wenige Leads oben im Funnel)?
   - Schritt 2: Ist es ein Qualitäts-Problem (falsche Leads, falsches ICP)?
   - Schritt 3: Ist es ein Conversion-Problem (Leads sind da, werden aber nicht gewandelt)?
   - Schritt 4: Ist es ein Retention-Problem (Kunden kommen, bleiben aber nicht)?
   - Nur eine dieser vier Stufen ist der primäre Engpass — die anderen sind nachgelagerte Symptome

3. **Engpass-Validierung durch Kreuzabgleich**
   - Qualitative Sales-Interviews gegen quantitative Funnel-Daten halten
   - Wenn Sales sagt «zu wenige Leads», aber Conversion Rate <15%: Qualitätsproblem, kein Volumen-Problem
   - Wenn Lead-Volumen hoch, aber SQL-Rate tief: ICP-Definition oder Nurturing-Lücke
   - Wenn SQL-Rate gut, aber Close Rate tief: Proposal-Qualität, Pricing, Competitive Positioning

4. **Upstream/Downstream-Analyse**
   - Für jeden vermuteten Engpass prüfen: Was verstärkt sich, wenn dieser gelöst wird?
   - Was bleibt limitiert, selbst wenn dieser gelöst wird?
   - Der echte Engpass entfaltet Hebelwirkung auf alle nachgelagerten Metriken

5. **Kosten des Engpasses quantifizieren**
   - Monthly Revenue leakage in CHF berechnen
   - Opportunity Cost bei Beibehaltung über 12 Monate
   - Damit Investitionsentscheidung fundiert begründbar

## Bewertungslogik

**Level 1 — Kein System (Kritisch)**
Keine Funnel-Metriken gemessen. Kein CRM oder nicht konsistent genutzt. Revenue-Entwicklung nicht auf Aktivitäten zurückführbar. Engpass-Analyse nicht möglich, da keine Datenbasis existiert. Sofortmassnahme: Tracking-Infrastruktur aufbauen.

**Level 2 — Symptomwahrnehmung (Schwach)**
Team weiss, dass etwas nicht funktioniert, aber nicht wo. Funnel-Daten teilweise vorhanden, aber nicht systematisch analysiert. Entscheidungen basieren auf Gefühl oder lautester Stimme im Raum. Typisch bei Unternehmen mit <10 Sales-Mitarbeitenden ohne dediziertes RevOps.

**Level 3 — Engpass identifiziert, aber falsch priorisiert (Mittel)**
Funnel-Daten vorhanden. Ein Engpass wird adressiert, aber es ist nicht der primäre. Klassisches Beispiel: Unternehmen erhöht Werbebudget, obwohl das eigentliche Problem im MQL→SQL-Übergang liegt. Ressourcen werden suboptimal eingesetzt.

**Level 4 — Engpass klar, Lösung in Arbeit (Gut)**
Der primäre Engpass ist datenbasiert identifiziert und priorisiert. Massnahmen laufen, werden gemessen. Andere Initiativen werden bewusst zurückgestellt. Typische Verbesserung: 25-40% Pipeline-Steigerung innerhalb von 90 Tagen nach korrekter Engpass-Lösung.

**Level 5 — Systematisches Engpass-Management (Exzellent)**
Engpass-Review ist fester Bestandteil des monatlichen Revenue-Meetings. Wenn ein Engpass gelöst wird, verschiebt sich der nächste Engpass automatisch und wird identifiziert. Continuous Improvement als Betriebsmodus. Best-in-Class-Unternehmen wechseln den primären Engpass alle 2-4 Quartale.

## Output

- Engpass-Diagnose-Karte: Primärer Engpass mit Datenbelegung und CHF-Quantifizierung
- Funnel-Heatmap: Alle Conversion Rates visualisiert mit Benchmark-Abweichungen markiert
- Priorisierte Hypothesen-Liste: Top 3 Engpass-Kandidaten mit Wahrscheinlichkeit und Evidenz
- Revenue Leakage Berechnung: Monatlicher und jährlicher Schaden des identifizierten Engpasses in CHF
- Fokus-Empfehlung: Eine klare Handlungsempfehlung — nicht drei, nicht fünf

## Empfehlungen

**Quick Wins (0-30 Tage)**
- Funnel-Dashboard in CRM aufbauen: alle Conversion Rates auf einem Blick, täglich aktuell
- Sales-Interview-Runde (3-5 Gespräche à 30 Minuten) zur Validierung der Datenhypothesen
- MQL-Definition schriftlich fixieren und zwischen Marketing und Sales alignment herstellen — dieser Schritt allein verbessert MQL→SQL-Rate typischerweise um 8-12 Prozentpunkte
- Revenue Leakage Berechnung präsentieren, um interne Priorisierungsdiskussionen zu beenden

**Mittelfristig (1-3 Monate)**
- Engpass-spezifische Massnahmen umsetzen (nicht alles gleichzeitig)
- Wenn Volumen-Engpass: Demand-Generation-Programm starten, ICP-gerechte Kanäle aktivieren
- Wenn Qualitäts-Engpass: Lead Scoring implementieren, ICP-Definition verschärfen, irrelevante Leads aus dem Funnel entfernen
- Wenn Conversion-Engpass: Sales Enablement-Materialien überarbeiten, Übergabeprozess strukturieren
- Monatliches Engpass-Review einführen

**Strategisch (3-12 Monate)**
- Revenue Operations Struktur aufbauen, die Engpass-Erkennung automatisiert
- Forecasting-Modell entwickeln, das Pipeline-Velocity und Engpass-Position berücksichtigt
- Engpass-Logik in OKR-Planung integrieren: Quarterly Goals immer am aktuellen primären Engpass ausrichten
- Wenn primärer Engpass gelöst: systematisch nächsten Engpass identifizieren und adressieren

## Performanceboost Perspektive

Der häufigste Fehler, den wir bei KMU in der Deutschschweiz sehen: Das Unternehmen hat ein Conversion-Problem bei SQL→Close, aber investiert in mehr LinkedIn Ads. Das Ergebnis ist ein teurerer Funnel mit derselben schlechten Abschlussrate.

Unser Ansatz beginnt immer mit der Engpass-Frage, bevor wir eine einzige Massnahme empfehlen. In der initialen Diagnose (3-4 Wochen) quantifizieren wir jeden Funnel-Schritt und berechnen den CHF-Schaden pro Engpass — nicht abstrakt, sondern in konkreten Zahlen, die Geschäftsführer für Investitionsentscheidungen brauchen.

Das, was uns unterscheidet: Wir lehnen es ab, an einem Funnel-Schritt zu arbeiten, bevor der Engpass identifiziert ist. «Mehr Aktivität» ist keine Strategie. Der primäre Engpass bekommt 80% der Ressourcen — alles andere wartet. Diese Disziplin ist unbequem, aber sie ist der Grund, warum Wachstum mit uns planbar wird.
