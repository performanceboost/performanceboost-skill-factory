# Lead Generation Diagnostic

## Zweck
Dieses Framework ist eine vollständige Diagnose der Lead-Generierungs-Infrastruktur eines B2B-Unternehmens. Es deckt systematisch auf, wo Leads verloren gehen, welche Kanäle unter- oder überinvestiert sind, wo Conversion-Pfade brechen, und ob die MQL-Definition und der Handoff zu Sales die Pipeline absichtlich einschränken. Das Ziel ist nicht eine Bestandsaufnahme — es ist die Lokalisierung des primären Hebels, der mit dem geringsten Aufwand den grössten Lead-Zuwachs erzeugt.

## Wann verwenden
- Lead-Volumen stagniert trotz konstantem oder wachsendem Budget
- Sales beschwert sich über Lead-Qualität, Marketing über Sales-Inaktivität
- Ein neues Kanal- oder Format-Investment steht zur Diskussion
- Das Unternehmen hat bisher keine strukturierte Lead-Generierung — Erstaufnahme vor dem Aufbau
- Nach einem Rebrand, einem Produkt-Pivot oder dem Eintritt in ein neues Marktsegment

## Input

**Kanal- und Kampagnen-Daten**
- Aktive Kanäle mit monatlichem Budget und Laufzeit (LinkedIn Ads, Google Ads, Meta, SEO/Organisch, Outbound, Events, Referral, Partner)
- CPL je Kanal (letzten 3 Monate, Monatsdurchschnitt)
- Lead-Volumen je Kanal (absolut, Monatsdurchschnitt)
- Kampagnen-Targeting: Geografisch, firmografisch, behavioural — wie präzise ist das ICP abgebildet?
- Ad-Creative-Rotation: Wie oft werden Creatives getestet? Wie viele Varianten laufen parallel?

**Conversion-Pfad-Daten**
- Alle Landing Pages mit URL, Traffic-Quelle, Visitor-Volumen, Formular-Conversion-Rate
- Formular-Felder je Landing Page (Anzahl und Art der abgefragten Felder)
- Thank-You-Page-Erlebnisse: Was passiert nach dem Formular-Submit?
- CTA-Typen auf der Website: Demo, Kontakt, Newsletter, Download, Assessment, Beratungsgespräch
- Mobile-Performance der Conversion-Seiten (Mobile-Conversion-Rate vs. Desktop)

**Lead-Magnet-Daten**
- Alle aktiven Lead-Magnete (Guides, Checklists, Templates, Assessments, Webinare, Tools)
- Download-/Anmelde-Zahlen je Lead-Magnet
- Lead-zu-MQL-Rate je Lead-Magnet
- Alter der Lead-Magnete: Wann zuletzt inhaltlich aktualisiert?
- ICP-Passung: Welches ICP-Segment spricht jeder Lead-Magnet an?

**MQL-Definition und Handoff-Daten**
- Schriftlich dokumentierte MQL-Kriterien (ja/nein)
- Lead-Scoring-Modell: Vorhanden? Felder und Gewichtungen dokumentiert?
- Durchschnittliche Zeit von Lead-Eingang bis MQL-Qualifizierung (in Stunden/Tagen)
- Durchschnittliche Zeit von MQL bis erstem Sales-Kontakt (in Stunden — Benchmark: unter 1 Stunde für warme MQLs)
- Feedback-Loop: Gibt Sales strukturiertes Feedback zu Lead-Qualität zurück an Marketing?
- SQL-Ablehnungsrate: Wie viele MQLs werden von Sales als unqualifiziert abgelehnt?

**Nurturing-Daten**
- Aktive E-Mail-Sequenzen: Anzahl, Länge, Trigger
- Open Rate je Sequenz (Benchmark B2B: 28–35 %)
- Reply Rate je Sequenz (Benchmark: 1.5–4 % bei Cold, 5–12 % bei Warm)
- Nurturing-Ausstieg-Rate: Wie viele Leads verlassen die Sequenz ohne Konversion?
- Retargeting: Wird Pixel-basiertes Retargeting für nicht-konvertierte Leads genutzt?

## Analyseprozess

**Schritt 1: Kanal-Effizienz-Matrix erstellen**
- Für jeden Kanal: CPL, Lead-Volumen, Lead-zu-MQL-Rate, Cost-per-MQL berechnen
- Rangierung nach Cost-per-MQL (nicht CPL) — das ist die entscheidende Metrik
- Benchmark Cost-per-MQL nach Kanal (Deutschschweiz B2B, typische Werte):
  - LinkedIn Ads: CHF 180–450 pro MQL
  - Google Search: CHF 120–320 pro MQL
  - Content/SEO (organisch): CHF 40–100 pro MQL (mit Infrastruktur-Invest)
  - Outbound (SDR-gestützt): CHF 80–200 pro MQL
  - Events/Webinare: CHF 60–150 pro MQL (Fixkosten geteilt)
- Kanäle mit Cost-per-MQL mehr als 2.5x über Benchmark sind sofortige Optimierungs-Kandidaten

**Schritt 2: Conversion-Pfad-Audit**
- Jede Landing Page gegen Conversion-Rate-Benchmarks prüfen:
  - Paid-Traffic-Landing-Page: unter 8 % = problematisch; Best-in-Class: 18–25 %
  - Organischer Traffic (Blog-CTA): unter 1 % = normal; über 3 % = gut
  - Gated-Content-Seiten: unter 15 % = Offer- oder Copy-Problem
- Formular-Längen-Analyse: Jedes zusätzliche Pflichtfeld reduziert Conversion um 5–15 %
  - Mehr als 5 Felder für ersten Kontakt: Conversion-Killer, ausser bei BOFU-Assets
- Mobile-Gap: Wenn Mobile-Conversion mehr als 40 % unter Desktop liegt → technisches Problem
- Klickpfad-Analyse: Woher kommen Leads, die zu SQLs werden? Rückwärts vom CRM tracing

**Schritt 3: Lead-Magnet-Wirksamkeit bewerten**
- Lead-Magnet-Performance-Score berechnen: (Lead-Volumen × MQL-Rate) ÷ Produktionskosten
- Generische Lead-Magnete erkennen: Titel wie "Der ultimative Guide zu X" ohne ICP-Spezifität haben typisch niedrige MQL-Raten (unter 5 %)
- Spezifische Lead-Magnete erkennen: Tools, Assessments, Branchen-spezifische Benchmarks, ROI-Rechner — typisch höhere MQL-Raten (15–35 %)
- Veraltete Lead-Magnete: Über 24 Monate ohne Update in der Deutschschweiz oft inhaltlich überholt — Vertrauensverlust bei qualifizierten Leads

**Schritt 4: MQL-Definition und Handoff-Qualität diagnostizieren**
- SQL-Ablehnungsrate als Qualitäts-Indikator:
  - Unter 10 % Ablehnung: MQL-Definition möglicherweise zu streng (zu wenig Volumen)
  - 10–25 % Ablehnung: Normaler Range für gesunden Scoring-Prozess
  - Über 40 % Ablehnung: MQL-Definition fehlt, ist unklar oder wird nicht durchgesetzt
- Reaktionszeit Marketing-zu-Sales messen: Lead-Reaktionszeit-Studie (Harvard Business Review) zeigt: Kontaktaufnahme in den ersten 5 Minuten = 9x höhere Konversionswahrscheinlichkeit vs. 10 Minuten; in der ersten Stunde = 60x höher vs. 24 Stunden
- Feedback-Loop-Qualität: Wenn Sales kein strukturiertes Feedback gibt, optimiert Marketing ins Leere

**Schritt 5: Nurturing-Infrastruktur bewerten**
- Sequenz-Mapping: Welche Leads gehen in welche Sequenz? Gibt es Lücken (Leads ohne Sequenz)?
- Segmentierung: Werden Nurturing-Sequenzen nach Segment, Kaufbereitschaft oder Verhalten differenziert oder läuft alles in eine generische Sequenz?
- Timing-Prüfung: E-Mail-Sequenzen, die länger als 6 Monate laufen ohne Reaktions-Trigger, verschwenden Kapazität
- Retargeting-Gap: Mehr als 97 % der Website-Besucher konvertieren nicht beim ersten Besuch — Retargeting ohne Pixel ist strukturelles Lead-Verlust

## Bewertungslogik

**Reifegrad-Modell: Lead Generation Infrastructure (5 Stufen)**

**Stufe 1 — Zufällig (keine Struktur, kein System)**
Leads entstehen durch Empfehlungen, Netzwerk oder seltene Inbound-Anfragen. Kein aktiver Kanal, keine Landing Page optimiert auf Conversion, kein CRM-Tracking. Lead-Generierung ist Zufall, nicht Prozess. CHF-Schaden: nicht quantifizierbar, aber jedes verpasste Lead ist verpasster Pipeline-Aufbau.

**Stufe 2 — Experimentell (Kanäle vorhanden, aber unverbunden)**
Mehrere Kanäle aktiv, aber jeder läuft in Isolation. Kein einheitliches Tracking, CPL wird je Kanal separat gemessen, Cost-per-MQL unbekannt. MQL-Definition mündlich vorhanden, nicht im CRM abgebildet. Nurturing = gelegentliche Newsletter. Typische Aussage: "Wir machen LinkedIn Ads, aber wir wissen nicht, ob es was bringt."

**Stufe 3 — Funktional (Messung aktiv, Optimierung fehlt)**
CPL und Lead-Volumen je Kanal bekannt. Landing Pages mit Formular-Tracking. MQL-Definition dokumentiert. Basis-Nurturing vorhanden. Aber: Cost-per-MQL nicht als primäre Metrik genutzt. Lead-Magnete generisch. Handoff-Prozess informal. Reaktionszeiten nicht gemessen. Lead-zu-MQL-Rate unter 12 %.

**Stufe 4 — Optimiert (datengetrieben, systematisch)**
Cost-per-MQL ist primäre Kanal-Metrik. Conversion-Pfade werden A/B-getestet. ICP-spezifische Lead-Magnete mit messbaren MQL-Raten. Lead-Scoring im CRM implementiert. Handoff-SLA definiert (z. B. Sales-Erstkontakt innerhalb 1 Stunde). SQL-Ablehnungsrate unter 25 %. Lead-zu-MQL-Rate 18–30 %.

**Stufe 5 — Skalierbar (Predictable Lead Engine)**
Lead-Generierung ist ein planbares System: Budgeterhöhung um X % = prognostizierbarer MQL-Anstieg um Y %. Kanal-Mix nach ICP-Segment differenziert. Lead-Magnete werden quartalsweise nach MQL-Rate priorisiert und bereinigt. Feedback-Loop zwischen Sales und Marketing formalisiert (monatliches Review mit Qualitäts-Score). Lead-zu-MQL-Rate über 30 %. Retargeting aktiv und segmentiert.

## Output

- **Kanal-Effizienz-Tabelle**: Alle aktiven Kanäle mit CPL, Cost-per-MQL, Lead-Volumen, MQL-Rate und Budget-Anteil
- **Conversion-Pfad-Audit-Tabelle**: Alle Landing Pages mit Conversion-Rate, Traffic-Quelle und Benchmark-Vergleich
- **Lead-Magnet-Wirksamkeits-Ranking**: Alle Assets nach Performance-Score (Volumen × MQL-Rate ÷ Kosten)
- **Handoff-Qualitäts-Bewertung**: MQL-Definition, SQL-Ablehnungsrate, Reaktionszeit-Messung
- **Primärer Hebel**: Eine benannte Schwachstelle mit grösster Hebelwirkung auf MQL-Volumen oder -Qualität
- **Reifegrad-Einordnung**: Stufe 1–5 mit konkreter Begründung je Diagnose-Dimension

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Cost-per-MQL je Kanal berechnen — nur diese Zahl zeigt, wo Budget falsch allokiert ist
- Den schwächsten Conversion-Pfad identifizieren (tiefste Conversion-Rate, höchster Traffic) und Formular auf maximal 3 Felder reduzieren
- MQL-Definition schriftlich fixieren und im CRM als Stage implementieren — eine Seite, kein Konzept
- Handoff-Reaktionszeit messen: CRM-Report, Zeit zwischen MQL-Qualifizierung und erstem Sales-Aktivitäts-Log

**Mittelfristig (1–3 Monate)**
- Einen neuen, ICP-spezifischen Lead-Magneten entwickeln: Assessment, ROI-Rechner oder Branchen-Benchmark-Report — keine generischen Guides
- Lead-Scoring-Modell im CRM implementieren: Mindestens 3 demografische und 3 behavioristische Scoring-Felder
- Nurturing-Sequenz für das grösste Drop-off-Segment aufbauen (Leads ohne Reaktion nach Erstdownload)
- Retargeting-Pixel auf allen relevanten Seiten implementieren und erste Retargeting-Kampagne für MOFU-Publikum aufsetzen

**Strategisch (3–12 Monate)**
- Kanal-Portfolio nach ICP-Segment differenzieren: Verschiedene Kanäle für verschiedene Buyer-Profile statt ein einziger Mix für alle
- Feedback-Loop formalisieren: Monatliches Marketing-Sales-Alignment-Meeting mit SQL-Ablehnungsrate und Lead-Qualitäts-Score als Agenda-Pflichtpunkte
- Lead-Generierungs-Dashboard aufbauen: Cost-per-MQL, Lead-zu-MQL-Rate, Handoff-Reaktionszeit und Nurturing-Effizienz als Echtzeit-Ansicht
- Ziel Reifegrad Stufe 4–5: Lead Engine ist planbar — Budget-Input korreliert nachweislich mit MQL-Output

## Performanceboost Perspektive

Das häufigste Muster, das wir bei KMUs in der Deutschschweiz sehen: LinkedIn Ads laufen, Google Ads laufen, ein paar Blog-Artikel existieren — aber kein einziges System ist verbunden. Der LinkedIn-Lead landet in einem Formular, das drei Wochen kein Follow-up erhält. Der organische Besucher findet keinen relevanten nächsten Schritt. Der Outbound-Kontakt bekommt eine generische E-Mail-Sequenz, die für alle Branchen gleich klingt.

Performanceboost diagnostiziert Lead-Generierung nicht als Kanal-Problem, sondern als System-Problem. Bevor wir Budget-Empfehlungen machen, prüfen wir die Conversion-Pfade: Wenn eine LinkedIn-Kampagne auf eine Landing Page schickt, die 3 % Conversion-Rate hat, ist das Kanal-Problem sekundär — das Conversion-Problem muss zuerst gelöst werden. Verdopplung des Ad-Budgets bei 3 % Conversion verdoppelt nur die Kosten.

Unsere Erfahrung: In 70 % der Erst-Diagnosen liegt der grösste Hebel nicht im Kanal-Mix, sondern im Handoff. Leads, die 48 Stunden auf Sales-Kontakt warten, konvertieren um 60–80 % schlechter als Leads, die in der ersten Stunde kontaktiert werden. Das kostet kein zusätzliches Budget — es kostet Prozess-Disziplin. Den zu installieren ist oft der schnellste Weg zu mehr qualifizierter Pipeline.
