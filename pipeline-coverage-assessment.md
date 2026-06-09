# Pipeline Coverage Assessment

## Zweck
Dieses Framework bewertet, ob die aktuell vorhandene Pipeline ausreicht, um die Quartalsziele zu erreichen — bevor das Quartal endet und es zu spät ist. Es analysiert nicht nur die Coverage Ratio als Rohdatum, sondern gewichtet Pipeline-Qualität, Stage-Verteilung und historische Konversionsraten, um eine realistische Zielerreichungswahrscheinlichkeit zu berechnen. Ein Coverage Ratio von 3x kann trügerisch sein, wenn 70 % der Pipeline in frühen Stages steckt oder die Win-Rate historisch bei 8 % liegt.

## Wann verwenden
- Sechs bis acht Wochen vor Quartalsende zur Frühwarnung
- Nach einem schwachen Vorquartal zur Ursachenanalyse
- Bei der Budgetplanung für den nächsten Zyklus
- Wenn Sales und Marketing unterschiedliche Einschätzungen zur Pipeline-Gesundheit haben
- Vor einem Board-Meeting oder Investoren-Update, das Pipeline-Prognosen erfordert

## Input

**Pipeline-Daten aus CRM (Stichtag definieren)**
- Gesamtvolumen der aktiven Pipeline in CHF (alle offenen Opportunities)
- Aufschlüsselung nach Deal-Stage (z. B. Prospecting, Qualified, Proposal, Negotiation, Verbal Commit)
- Anzahl Deals je Stage
- Durchschnittlicher Deal-Wert je Stage
- Datum des letzten Aktivitäts-Updates je Deal
- Expected-Close-Date-Verteilung (aktuelles Quartal vs. Folgeperioden)

**Historische Performance-Daten (min. 4 Quartale)**
- Win-Rate gesamt und nach Deal-Grösse (klein/mittel/gross)
- Stage-zu-Stage-Konversionsraten
- Durchschnittliche Verweildauer je Stage
- Slippage-Rate: Deals, die das Quartal nicht wie geplant geclosed wurden
- Durchschnittliche Sales-Cycle-Länge nach Segment

**Ziel- und Kontextdaten**
- Umsatzziel aktuelles Quartal in CHF
- Bereits gebuchter/gesicherter Revenue (Closed Won YTD)
- Offenes Ziel (Revenue-Ziel minus bereits gebuchter Revenue)
- Restlaufzeit des Quartals in Wochen

## Analyseprozess

**Schritt 1: Rohe Coverage Ratio berechnen**
- Coverage Ratio = Gesamte aktive Pipeline (CHF) ÷ Offenes Quartalsziel (CHF)
- Benchmark: Best-in-Class B2B = 3x–4x; Minimum funktional = 2.5x; unter 2x = kritisch
- Wichtig: Die rohe Coverage Ratio ist ein Ausgangspunkt, kein Urteil. Sie ignoriert Qualität und Timing.

**Schritt 2: Quality-gewichtete Pipeline berechnen**
- Jeden Deal mit der historischen Stage-Konversionsrate gewichten:
  - Prospecting/Discovery: 10–15 % Gewichtung
  - Qualified/Needs Analysis: 25–35 % Gewichtung
  - Proposal/Demo: 45–55 % Gewichtung
  - Negotiation: 65–80 % Gewichtung
  - Verbal Commit: 85–95 % Gewichtung
- Quality-gewichtete Pipeline = Summe aller (Deal-Wert × Stage-Gewichtung)
- Ratio neu berechnen: Quality-gewichtete Pipeline ÷ Offenes Ziel
- Typischer Befund: Rohe Coverage 3.2x → Quality-gewichtet 1.4x. Der Unterschied ist der Risikoindikator.

**Schritt 3: Timing-Filter anwenden**
- Nur Deals berücksichtigen, deren Expected-Close-Date im aktuellen Quartal liegt
- Slippage-Bereinigung: Historische Slippage-Rate vom Timing-gefilterten Volumen abziehen
  - Beispiel: 25 % der Deals slippten in den letzten 4 Quartalen → bereinigtes Volumen × 0.75
- Ergänzend prüfen: Welche Deals wurden in den letzten 14 Tagen nicht aktualisiert? (Zombie-Deals)
- Zombie-Deal-Indikator: Kein Aktivitäts-Update seit 14+ Tagen und Close-Date im laufenden Quartal → Wert auf 0 setzen für konservative Prognose

**Schritt 4: Stage-Konzentrations-Risiko analysieren**
- Wie verteilt sich die Pipeline über die Stages?
- Gesundes Verhältnis (von oben nach unten): 15 % / 20 % / 30 % / 25 % / 10 %
- Warnsignal: Mehr als 50 % der Pipeline-Volume in Stage 1–2 bei weniger als 8 Wochen Restlaufzeit
- Warnsignal: Mehr als 40 % der Deals in einer einzelnen Stage (Klumpenrisiko)
- Warnsignal: Weniger als 15 % in Negotiation/Verbal-Commit-Stage

**Schritt 5: Szenario-Modellierung**
- Konservatives Szenario: Quality-gewichtet, slippage-bereinigt, Zombie-Deals ausgeschlossen
- Basis-Szenario: Quality-gewichtet, durchschnittliche Slippage
- Optimistisches Szenario: Rohe Pipeline × historische Win-Rate ohne weitere Bereinigung
- Zielerreichungswahrscheinlichkeit je Szenario als Prozentzahl und CHF-Delta ausweisen

## Bewertungslogik

**Reifegrad-Modell: Pipeline Coverage Health (5 Stufen)**

**Stufe 1 — Blind (keine systematische Pipeline-Analyse)**
Pipeline-Zahlen existieren im CRM, werden aber nicht systematisch zur Prognose genutzt. Forecasts basieren auf Sales-Aussagen. Slippage wird nicht gemessen. Quartalsüberraschungen sind die Norm. Typisches Symptom: "Wir dachten, wir schaffen es."

**Stufe 2 — Reaktiv (Coverage Ratio bekannt, aber ungewichtet)**
Coverage Ratio wird berechnet und kommuniziert, aber nicht qualitätsgewichtet. Stage-Verteilung wird nicht analysiert. Zombie-Deals inflationieren die Pipeline. Prognose-Genauigkeit unter 60 %.

**Stufe 3 — Funktional (Quality-Gewichtung vorhanden, Slippage ignoriert)**
Stage-Gewichtung wird angewendet. Aber historische Slippage-Rate fliesst nicht ein. Timing-Filter fehlt oder ist unzuverlässig. Forecasts liegen ±25 % neben dem tatsächlichen Ergebnis. Monatliches Pipeline-Review findet statt, aber ohne Standard-Format.

**Stufe 4 — Präzise (vollständig bereinigtes Forecasting)**
Quality-gewichtete, slippage-bereinigte, timing-gefilterte Pipeline ist Standard. Zombie-Deal-Definition im CRM verankert. Szenario-Modellierung für Quartalsende läuft wöchentlich. Prognose-Genauigkeit über 75 %. Sales-Führung und Marketing arbeiten mit identischen Zahlen.

**Stufe 5 — Prädiktiv (Pipeline-Gaps werden 6–8 Wochen früh erkannt)**
Frühwarnsystem aktiv: Wenn die bereingte Coverage unter 2.5x fällt, wird automatisch eine Demand-Gen-Eskalation ausgelöst. Forecasting-Modell hat weniger als ±10 % Abweichung über 6 Quartale. Pipeline-Gesundheit wird als Leading Indicator für Revenue-Planung genutzt, nicht als Lagging Indicator.

## Output

- **Coverage Dashboard**: Rohe Ratio, Quality-gewichtete Ratio, Slippage-bereinigte Ratio — drei Zahlen nebeneinander
- **Stage-Verteilungs-Heatmap**: Visualisierung der Pipeline-Konzentration mit Warnsignal-Markierung
- **Szenario-Tabelle**: Konservativ / Basis / Optimistisch mit CHF-Wert und Zielerreichungs-Prozent
- **Zombie-Deal-Liste**: Alle Deals ohne Aktivität seit 14+ Tagen mit Empfehlung (reaktivieren oder abschreiben)
- **Gap-Aktion**: Wenn konservatives Szenario unter 85 % Zielerreichung liegt — konkreter Aktionsplan mit Volumenbedarf

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Zombie-Deals identifizieren und innerhalb von 5 Werktagen reaktivieren oder aus aktiver Pipeline entfernen
- Expected-Close-Dates auf Plausibilität prüfen — alle Deals mit Close-Date "Ende Quartal" ohne konkreten nächsten Schritt auf nächstes Quartal verschieben
- Wöchentliches Pipeline-Review mit Stage-Verteilung und bereinigter Coverage Ratio als 30-Minuten-Standard einführen
- Slippage-Rate der letzten 4 Quartale berechnen und dokumentieren

**Mittelfristig (1–3 Monate)**
- Quality-Gewichtung nach historischen Stage-Konversionen im CRM als Feld implementieren
- Slippage-Prognose automatisieren: CRM berechnet automatisch slippage-bereinigte Coverage
- Deal-Hygiene-Standards definieren: Was muss pro Stage vorhanden sein (Kontaktperson, Budget, Timeline, nächster Schritt)?
- Frühwarnsystem einrichten: Alert wenn bereinigte Coverage unter 2.5x fällt

**Strategisch (3–12 Monate)**
- Prognose-Genauigkeit als KPI einführen und quartalsweise tracken (Ziel: ±15 % Abweichung)
- Pipeline-Coverage-Ziel rückwärts aus Demand-Gen-Kapazität und Sales-Cycle-Länge ableiten
- Segmentierte Coverage-Analyse aufbauen: Coverage nach Segment, Grösse und Kanal trennen — ein einziger Coverage-Wert verdeckt kritische Muster
- Integration mit Demand Generation Gap Analysis (siehe separates Framework): Wenn Coverage fällt, automatisch Lead-Bedarf berechnen

## Performanceboost Perspektive

Eine Coverage Ratio von 3x fühlt sich sicher an — bis man die Zahlen bereinigt. Wir erleben regelmässig, dass KMUs in der Deutschschweiz eine nominelle Pipeline von CHF 1.2 Mio. ausweisen, aber nach Quality-Gewichtung und Slippage-Bereinigung bleibt ein realistischer Wert von CHF 380'000 übrig. Bei einem Quartalsziel von CHF 500'000 ist das nicht 2.4x Coverage — das ist ein Defizit von CHF 120'000, das noch sechs Wochen verborgen bleibt.

Performanceboost baut das Coverage Assessment als Standard ins monatliche Reporting ein — nicht als Quartals-Exercise, sondern als Frühwarnsystem. Der entscheidende Unterschied zu internen Einschätzungen: Wir trennen die emotionale Bewertung eines Deals ("der kommt bestimmt") von der datenbasierten Stage-Gewichtung. Wenn ein Deal seit 21 Tagen keinen nächsten Schritt hat, zählt er in unserer Kalkulation nicht als Coverage. Das ist unbequem — und präzise. Prognose-Genauigkeit über ±15 % ist für uns kein akademisches Ziel, sondern die Voraussetzung für sinnvolle Budget- und Ressourcenentscheide.
