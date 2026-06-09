# ICP & Segment Prioritization

## Zweck
Dieses Framework definiert und priorisiert das Ideal Customer Profile (ICP) jenseits demografischer Oberflächenmerkmale. Es analysiert, welche Kundensegmente den höchsten Revenue-per-Acquisition liefern, den kürzesten Sales Cycle haben und die niedrigste Churn-Rate aufweisen — und identifiziert die spezifischen Buying Trigger und Decision Dynamics, die diese Segmente auszeichnen. Ergebnis ist nicht eine statische Zielgruppendefinition, sondern ein operationalisierbares Segment-Profil, das die gesamte Revenue Engine steuert.

## Wann verwenden
- Das Unternehmen spricht «alle B2B-Unternehmen» an — de facto niemanden
- Conversion-Rates sind tief, obwohl Leads quantitativ ausreichend sind
- Sales verbringt mehr als 30% der Zeit mit Deals, die nie zu echten Opportunities werden
- Marketing und Sales haben implizit unterschiedliche Vorstellungen vom Wunschkunden
- Neue Marktsegmente sollen erschlossen werden — ohne strukturierte Bewertung welche
- Churn-Rate ist über 10% im Jahr — häufig ein Zeichen falscher Kundenselektion an der Quelle

## Input
**Bestandskundendaten**
- Vollständige Kundenliste mit: Branche, Unternehmensgrösse (Mitarbeitende und Umsatz), Region, Akquisitionskanal, ACV (Average Contract Value), Start-Datum, aktueller Status
- CLV oder Umsatz pro Kunde der letzten 24 Monate
- Churn-Daten: Welche Kunden haben gekündigt, wann und mit welchem dokumentierten Grund?
- NPS oder CSAT-Daten, wenn vorhanden

**Sales-Prozessdaten**
- Sales-Cycle-Länge pro Segment und Deal-Grösse
- CAC pro Kanal und Segment
- Win/Loss-Daten: Welche Deals wurden gewonnen, welche verloren — und gegen wen?
- Einwand-Log aus Sales-Gesprächen

**Qualitative Eingaben**
- Gespräche oder Interviews mit 5–10 besten Kunden: Kaufmotivation, Trigger, interne Entscheidungsstruktur
- Gespräche mit 3–5 churned Kunden: Warum haben sie aufgehört?
- Sales-Team-Einschätzung: Welcher Kundentyp ist am einfachsten zu konvertieren, am anspruchsvollsten zu betreuen?

## Analyseprozess

**1. Bestandskunden-Segmentierung und Scoring**
Jeden Bestandskunden anhand von vier Dimensionen bewerten (je 1–5 Punkte):
- Revenue-Wert: ACV und CLV im Verhältnis zum Durchschnitt
- Akquisitionseffizienz: CAC und Sales-Cycle-Länge
- Retention-Qualität: Vertragslänge, Verlängerungsrate, Upsell-Geschichte
- Referenzpotenzial: Hat der Kunde aktiv weiterempfohlen oder als Referenz gedient?

Kunden in drei Cluster einteilen: Tier 1 (Top 20%, Score 16–20), Tier 2 (mittlere 50%, Score 9–15), Tier 3 (untere 30%, Score 4–8).

**2. Tier-1-Muster extrahieren**
Für Tier-1-Kunden nach gemeinsamen Merkmalen suchen — strukturiert nach drei Ebenen:
- **Firmografisch**: Branche, Grösse, Wachstumsphase, Technologie-Stack, Standort
- **Situativ**: In welcher Situation befand sich das Unternehmen vor dem Kauf? (z.B. Team-Wachstum, Digitalisierungsdruck, Compliance-Anforderung, Wettbewerbsdruck)
- **Trigger-basiert**: Welches konkrete Ereignis hat die Kaufentscheidung ausgelöst? (z.B. Führungswechsel, gescheitertes internes Projekt, Expansion in neuen Markt)

**3. Decision Dynamics kartieren**
Pro Segment die Entscheidungsstruktur dokumentieren:
- Wer ist der Wirtschaftliche Käufer (Budget-Entscheid)? Wer ist der technische Evaluator? Wer ist der Champion (interner Fürsprecher)?
- Typische Anzahl Stakeholder im Entscheidungsprozess
- Welche Einwände treten in welcher Phase auf — und von wem?
- Durchschnittliche Zeit von erstem Kontakt bis Entscheidung pro Segment

**4. Revenue-Potenzial pro Segment schätzen**
Für jedes identifizierte Segment berechnen:
- Adressierbarer Markt in der Deutschschweiz: Anzahl Unternehmen im Profil × durchschnittlicher ACV
- Erreichbarer Anteil (realistisch, nicht theoretisch) in 12 und 24 Monaten
- CLV:CAC-Ratio des Segments — Benchmark: gesund ab 3:1, exzellent ab 5:1
- Payback Period: Wie viele Monate bis CAC-Rückgewinnung durch Umsatz?

**5. Segment-Priorisierungs-Matrix**
Segmente in zwei Dimensionen bewerten:
- Y-Achse: Strategisches Potenzial (Marktgrösse × CLV:CAC)
- X-Achse: Erreichbarkeit (Kanal-Fit, bestehende Proof Points, Ressourcenaufwand)

Daraus ergeben sich vier Felder: Fokus-Segmente (oben rechts), Zukunfts-Segmente (oben links), Nischen (unten rechts), Deprioritisieren (unten links).

## Bewertungslogik

**ICP-Reifegrad — 5 Stufen**

| Stufe | Bezeichnung | Kriterien | Operative Konsequenz |
|-------|-------------|-----------|---------------------|
| 1 | Undefiniert | Kein dokumentiertes ICP; das Unternehmen verkauft an jeden, der kaufen will | Sales verliert Zeit mit unqualifizierten Deals; Marketing produziert nicht verwertbare Leads |
| 2 | Demografisch | ICP basiert auf Firmografik (Branche, Grösse) ohne Verhaltens- oder Trigger-Dimension | Führt zu breiten Zielgruppen ohne Resonanz; CPL hoch, Conversion tief |
| 3 | Verhaltensbasiert | ICP enthält Kaufverhalten und typische Situationsmerkmale; wird aber selten aktualisiert | Bessere Qualifizierung, aber kein systematisches Scoring oder Routing |
| 4 | Trigger-basiert | ICP definiert spezifische Kauftrigger und Decision Dynamics; Lead-Scoring und Channel-Auswahl sind darauf ausgerichtet | MQL→SQL-Rate messbar über Branchendurchschnitt (Best-in-Class: 35%+); Sales fokussiert auf beste Deals |
| 5 | Dynamisch | ICP wird quartalsweise mit echten Win/Loss-Daten aktualisiert; Segmentierung ist im CRM und in der Automation abgebildet; verschiedene Personas erhalten differenzierte Journeys | Vollständig prädiktiver Pipeline; niedrigster CAC, höchster CLV — Wachstum ist planbar |

## Output
- Priorisiertes ICP-Dokument: Tier-1-Segment mit vollständigem Firmografik-, Situations- und Trigger-Profil
- Persona-Steckbriefe pro relevantem Entscheidungstyp: Wirtschaftlicher Käufer, Champion, Evaluator
- Segment-Scoring-Modell für CRM-Integration: Welche Datenpunkte qualifizieren einen Lead als ICP-konform?
- Revenue-Potenzial-Berechnung pro Segment in CHF
- Liste der explizit deprioritisierten Segmente mit Begründung

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Top-20-Kunden nach ACV × Verlängerungsrate identifizieren und auf gemeinsame Merkmale analysieren — in einem halben Tag ergibt sich das klarste ICP-Signal
- CRM-Daten um zwei Felder ergänzen: «Kauftrigger» und «Verlustgrund» — retroperspektiv für die letzten 20 Deals ausfüllen
- Lead-Scoring-Test: Alle aktuellen Opportunities gegen das neue ICP-Profil bewerten — welche Deals sind tatsächlich qualifiziert?

**Mittelfristig (1–3 Monate)**
- 5–7 strukturierte Interviews mit Tier-1-Kunden führen: Trigger-Frage, Alternativenvergleich, Decision-Making-Prozess
- ICP in CRM als Scoring-Modell abbilden: Automatisches Lead-Rating auf Basis von Firmografik und Verhaltens-Signalen
- Marketing-Kampagnen auf Tier-1-ICP ausrichten: Alle aktiven Kampagnen auf ICP-Relevanz prüfen, nicht ICP-konforme einstellen

**Strategisch (3–12 Monate)**
- Quarterly ICP-Review einführen: Win/Loss-Daten fliessen direkt in ICP-Updates ein
- Zweites Fokus-Segment erschliessen, sobald Tier-1-Segment saturiert oder stabiles Playbook existiert
- Retention-Strategie nach Segment differenzieren: Tier-1-Kunden erhalten andere Onboarding- und Success-Journeys als Tier-2

## Performanceboost Perspektive
Das häufigste ICP-Problem in Deutschschweizer KMU ist nicht, dass kein ICP vorhanden ist — es ist, dass das ICP nie mit echten Umsatzdaten abgeglichen wurde. Ein ICP, das auf einem internen Workshop basiert und nie gegen Win/Loss-Realität gespiegelt wurde, ist eine Hypothese, keine Strategie.

Performanceboost führt jede ICP-Arbeit mit einem Datenspiegel aus dem CRM: Welche Kunden generieren den höchsten CLV, haben den kürzesten Sales Cycle und die niedrigste Churn-Rate? Diese Kunden definieren das reale ICP — nicht die Wunschkunden, sondern die Kunden, mit denen das Unternehmen nachweislich gewinnt.

Ein konkreter Erfahrungswert: Bei einem Schweizer SaaS-Unternehmen (30 Mitarbeitende) zeigte die ICP-Analyse, dass 67% des profitablen Umsatzes von 22% der Kunden stammten — alle aus einer einzigen Branche mit einem spezifischen Trigger (Compliance-Anforderung durch regulatorische Änderung). Die gesamte GTM-Energie wurde danach auf diese 22% ausgerichtet. CAC sank innerhalb von 6 Monaten um 40%, Sales-Cycle um 28 Tage.
