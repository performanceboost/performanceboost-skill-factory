# Workflow Opportunity Scanner

## Zweck
Dieses Skill-Dokument identifiziert systematisch alle manuellen Prozesse in Marketing und Sales, die heute Zeit fressen, Fehler produzieren oder Revenue-Lücken erzeugen — und priorisiert sie nach dem konkreten ROI einer Automatisierung. Die meisten Automatisierungs-Projekte scheitern, weil sie mit «was ist technisch möglich» beginnen, statt mit «was kostet uns die aktuelle Manualität am meisten». Dieser Scanner kehrt die Logik um: zuerst der Schaden, dann die Lösung.

## Wann verwenden
- Vor der Einführung oder Erweiterung eines Automation-Tech-Stacks, um die Prioritätenliste zu definieren
- Wenn Marketing- oder Sales-Teams «zu wenig Zeit» haben, ohne dass der Zeitaufwand strukturiert erfasst wurde
- Bei der Vorbereitung eines RevOps-Projekts als Input für die Prozess-Architektur
- Wenn ein neues CRM oder Automation-Tool eingeführt wird und entschieden werden muss, welche Workflows zuerst gebaut werden
- Nach einem Team-Wachstum, um zu prüfen, ob manuelle Prozesse skalierbar sind oder Bottlenecks erzeugen

## Input

**Prozess-Inventar (durch strukturierte Interviews oder Prozess-Dokumentation)**
- Liste aller regelmässigen Marketing-Tasks (täglich, wöchentlich, monatlich) und ihr ungefährer Zeitaufwand
- Liste aller regelmässigen Sales-Tasks mit Zeitaufwand
- Alle Punkte, an denen Daten manuell von einem System ins andere übertragen werden
- Alle Prozesse, die aktuell durch «ich erinnere mich» oder «ich prüfe das gelegentlich» gesteuert werden

**Fehlerquellen-Dokumentation**
- Wo werden Leads nicht kontaktiert, weil jemand vergessen hat?
- Wo werden falsche Daten in CRM-Felder eingetragen, weil keine Validierung existiert?
- Wo verlieren Leads ihren Status, weil kein automatischer Übergang definiert ist?

**System-Landschaft**
- Welche Tools sind vorhanden und wie sind sie heute verbunden (oder nicht verbunden)?
- Wo existieren manuelle Exports/Imports zwischen Systemen?
- Welche Tools haben API-Zugänge oder native Integrationen, die noch nicht genutzt werden?

**Team-Zeiterfassung**
- Wie viele Stunden pro Woche verbringen Marketing- und Sales-Mitarbeitende mit administrativen Aufgaben ohne direkten Revenue-Beitrag?

## Analyseprozess

1. **Prozess-Inventar erstellen (Time-Value-Mapping)**
   - Alle genannten manuellen Prozesse in eine Tabelle aufnehmen
   - Für jeden Prozess: Frequenz × Zeitaufwand pro Ausführung = monatlicher Zeitaufwand in Stunden
   - Kosten monetarisieren: Stundensatz der ausführenden Person × monatliche Stunden = CHF-Aufwand pro Prozess pro Monat
   - Benchmark: Typischer B2B-KMU-Vertriebsmitarbeitende verbringt 25–35% der Arbeitszeit mit administrativen Aufgaben statt mit Verkaufsgesprächen

2. **Fehlerkosten-Analyse**
   - Für jeden fehleranfälligen Prozess: Was ist der Worst-Case-Schaden pro Fehler?
   - Lead-Nicht-Kontaktierung: durchschnittlicher Lead-Wert × geschätzte Conversion-Rate = verlorener Pipeline-Wert
   - Falsche CRM-Daten: Leads, die falsch segmentiert werden, erhalten falschen Content → schlechtere Conversion-Rates
   - Doppelerfassungen und Datenfehler verlangsamen Reporting → falsche Entscheidungen

3. **Automatisierbarkeits-Prüfung**
   - Für jeden Prozess: Ist er regelbasiert (klare If-Then-Logik) oder erfordert er Judgement?
   - Regelbasiert + hoher Zeitaufwand = idealer Automatisierungs-Kandidat
   - Judgement-basiert = menschliche Entscheidung bleibt, aber Vorbereitung kann automatisiert werden
   - Tool-Match: Welches vorhandene oder sinnvolle Tool würde diesen Prozess automatisieren (Make/Zapier, HubSpot Workflows, CRM-native Automation, Clay)?

4. **ROI-Berechnung pro Kandidat**
   - Implementierungsaufwand (einmalig in Stunden oder CHF)
   - Monatliche Zeitersparnis nach Automatisierung (in CHF)
   - Break-even-Berechnung: Wann hat sich die Investition amortisiert?
   - Revenue-Impact: Führt die Automatisierung zu höherer Pipeline-Velocity, besserer Lead-Qualifikation oder schnellerer Reaktionszeit?
   - Benchmark: ROI-positive Automatisierungen in B2B-KMU amortisieren sich durchschnittlich in 6–14 Wochen

5. **Priorisierungs-Matrix aufbauen**
   - Zwei Dimensionen: Business-Impact (Zeit + Revenue + Fehlerreduktion) und Implementierungs-Aufwand (Komplexität + Abhängigkeiten)
   - Vier Quadranten:
     - Quick Wins: Hoher Impact, tiefer Aufwand — sofort umsetzen
     - Grosse Projekte: Hoher Impact, hoher Aufwand — mit Meilenstein-Plan angehen
     - Fill-ins: Tiefer Impact, tiefer Aufwand — wenn Kapazität vorhanden
     - Nicht umsetzen: Tiefer Impact, hoher Aufwand — explizit priorisieren

## Bewertungslogik

**Stufe 1 — Keine Automation (Score 0–20/100)**
Alle Prozesse sind manuell. Kein aktives Automation-Tool ausser E-Mail-Client. Datentransfers erfolgen via Copy-Paste oder manuelle CSV-Exports. Typischer versteckter Kostenfaktor: CHF 3'000–8'000 pro Monat in administrativem Aufwand pro Mitarbeitenden im Revenue-Team.

**Stufe 2 — Punktuelle Automation (Score 21–40/100)**
Einzelne Prozesse sind automatisiert (z.B. Formular-zu-CRM-Sync), aber die meisten Übergaben zwischen Systemen sind noch manuell. Automation ist reaktiv entstanden, nicht strategisch geplant. Zap-/Make-Flows sind unstrukturiert und schwer wartbar.

**Stufe 3 — Prozess-selektive Automation (Score 41–60/100)**
Die wichtigsten Marketing-Automation-Flows laufen (Lead-Eintritt, Sequenz-Trigger, MQL-Übergabe). Sales-seitige Automation ist jedoch schwach. Reporting ist noch grossteils manuell. Zeitersparnis gegenüber Stufe 1: typischerweise 40–60% der ursprünglichen Admin-Stunden.

**Stufe 4 — Revenue-Process-Automation (Score 61–80/100)**
Marketing- und Sales-Prozesse sind in einem kohärenten Automation-System verbunden. CRM-Updates triggern Marketing-Aktionen und vice versa. Reporting läuft automatisch. Manuelle Arbeit konzentriert sich auf Judgement-Aufgaben, nicht auf Dateneingabe. Restaufwand: unter 10% des ursprünglichen Admin-Zeitaufwands.

**Stufe 5 — Adaptive Automation (Score 81–100/100)**
Workflows sind nicht nur regelbasiert, sondern KI-assistiert: Enrichment läuft automatisch via Clay/Apollo, Lead-Scoring wird durch ML-Modelle verfeinert, Content-Personalisierung erfolgt dynamisch. Neue Prozesse werden standardmässig auf Automatisierbarkeit geprüft, bevor manuelle Execution entschieden wird. Reporting ist Echtzeit-fähig.

## Output

- Workflow-Opportunity-Register: Vollständige Liste aller identifizierten Automatisierungs-Kandidaten mit CHF-Aufwand (Ist-Zustand), ROI-Schätzung und Priorisierungseinordnung
- Quick-Win-Shortlist: Die Top 3–5 Automatisierungen mit dem besten Aufwand-Impact-Verhältnis und sofort umsetzbarem Implementierungsplan
- Priorisierungs-Matrix (2×2 Quadrant) mit allen Kandidaten
- Tool-Empfehlung pro Automatisierung: Welches vorhandene oder zu ergänzende Tool ist der richtige Fit
- Quantifizierter Gesamtschaden der aktuellen Manualität in CHF/Monat
- Monatliches Einspar-Potenzial nach vollständiger Umsetzung der Quick Wins

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Lead-zu-CRM-Sync automatisieren, falls noch nicht vorhanden: Jede manuelle Dateneingabe ist ein Fehlervektor und Zeitfresser — typische Zeitersparnis: 2–4 Stunden/Woche im Team
- Interne Benachrichtigungen automatisieren: Sales-Alert bei MQL-Schwellenwert, Notification bei hochpriorisiertem Website-Besuch — kostet weniger als 2 Stunden Setup in HubSpot oder Make
- Report-Erstellung automatisieren: Weekly KPI-Dashboard via Looker Studio oder HubSpot-Report, der sich selbst versendet — typische Einsparung: 1–3 Stunden/Woche

**Mittelfristig (1–3 Monate)**
- Sales-to-Marketing-Feedback-Loop automatisieren: Wenn ein Deal als «Closed Lost» markiert wird, triggert eine Automatisierung einen Re-Nurturing-Flow oder sendet einen strukturierten Feedback-Request
- Lead-Enrichment automatisieren: Neue CRM-Kontakte werden automatisch mit Firmendaten angereichert (Apollo, Clearbit oder Clay-Workflow) — Qualität der Lead-Segmentierung steigt messbar
- Proposal/Angebots-Tracking automatisieren: Wenn ein Angebot länger als X Tage ohne Reaktion ist, triggert ein Follow-up-Task oder eine automatisierte Sequenz

**Strategisch (3–12 Monate)**
- End-to-End Revenue-Process-Automatisierung: Alle Touchpoints von First-Touch bis Closed-Won in einem zusammenhängenden Automation-System verbinden — kein Lead fällt mehr durch Systemlücken
- KI-gestützte Enrichment-Pipeline aufbauen (Clay-Workflow): Automatische Recherche von Trigger-Events, Jobtitel-Wechsel, Funding-Runden, Technologie-Nutzung — Sales-Prioritäten werden nicht mehr manuell entschieden, sondern durch Signal-Score generiert
- Automation-Governance einführen: Quartalsweises Review aller aktiven Workflows auf Performance, Aktualität und Verbesserungspotenzial

## Performanceboost Perspektive

Der Workflow Opportunity Scanner ist einer der schnellsten ROI-Nachweise, die wir in Projekten liefern. In jedem Onboarding-Assessment quantifizieren wir den versteckten Kosten-Berg der Manualität — und die Zahl überrascht Geschäftsführer regelmässig: CHF 5'000–15'000 pro Monat in direktem Zeitaufwand, der durch strukturierte Automation eliminierbarer Overhead ist.

Unser Grundsatz: Automation soll Revenue-Teams Zeit für echte Arbeit zurückgeben — Gespräche, strategische Entscheidungen, Beziehungspflege. Wir sind keine Automatisierungs-Enthusiasten. Wir automatisieren nur, wenn der ROI in weniger als 3 Monaten messbar ist. Jede Empfehlung aus dem Scanner enthält eine konkrete Break-even-Rechnung. Kein «das wird langfristig wertvoll» ohne CHF-Zahl dahinter.
