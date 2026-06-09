# Process Automation Assessment

## Zweck
Die meisten B2B-KMU haben erhebliche Automatisierungspotenziale in Marketing, Sales und Operations — ohne es zu wissen, weil niemand je die gesamten Prozesskosten sichtbar gemacht hat. Dieses Skill-Dokument kartiert systematisch alle repetitiven Prozesse, bewertet deren Automatisierbarkeit nach Tool-Kompatibilität und Prozessreife, und berechnet das CHF-Einsparpotenzial pro Prozess. Das Ziel ist kein Technologie-Roadmap-Dokument, sondern eine priorisierte Investitionsentscheidung: Welche Automatisierung zahlt sich in unter 6 Monaten aus?

## Wann verwenden
- Wenn ein Unternehmen sein Wachstum skalieren möchte, ohne proportional mehr Personal einzustellen
- Wenn Operations-Kosten steigen, aber die Ursache unklar ist
- Vor der Evaluation oder dem Wechsel von Automatisierungs-Tools (Make, Zapier, n8n, HubSpot Workflows)
- Wenn Marketing oder Sales "zu beschäftigt" sind für strategische Arbeit — als Diagnose, ob die Beschäftigung manuell oder systemisch ist
- Als Grundlage für ein Gespräch mit der Geschäftsleitung über Tech-Stack-Investitionen

## Input

**Marketing-Prozesse (Mindestzahl: 8 erheben)**
- Lead-Capture: Wie werden Leads aus welchen Quellen ins CRM übertragen?
- Lead-Nurturing: Werden Follow-up-Sequenzen manuell oder automatisch ausgelöst?
- Content-Produktion: Welche Content-Schritte wiederholen sich wöchentlich?
- Reporting: Wer erstellt welche Berichte, wie häufig, in welchem Tool?
- Event- und Webinar-Management: Registrierung, Erinnerungen, Follow-up — wie viel davon ist manuell?
- Social-Media-Scheduling: Welches Tool, welcher manuelle Aufwand?

**Sales-Prozesse (Mindestzahl: 8 erheben)**
- Prospect-Recherche: Wie wird ein neuer Lead vor dem Erstkontakt recherchiert?
- CRM-Datenpflege: Wie und wann werden Deals, Kontakte und Aktivitäten aktualisiert?
- Proposal-Erstellung: Wie lange dauert ein Angebot, welche Teile sind copy-paste?
- Follow-up-Management: Wer erinnert wen wie an ausstehende Antworten?
- Demo-Vorbereitung: Welche Informationen werden vor einem Demo manuell zusammengestellt?
- Onboarding-Kommunikation: Welche Mails und Tasks werden nach einem Abschluss manuell ausgelöst?

**Operations-Prozesse (Mindestzahl: 5 erheben)**
- Reporting und Dashboard-Updates: Wöchentliche/monatliche Routine-Reports
- Daten-Synchronisation: Welche Daten werden manuell zwischen Systemen kopiert?
- Rechnungsstellung und Vertragsmanagement: Wie viel davon ist manuell?
- Onboarding neuer Mitarbeitender: Welche Schritte wiederholen sich?
- Support- und Anfragen-Routing: Wie werden eingehende Anfragen zugeteilt?

**Tool-Stack-Inventar**
- Vollständige Liste aller genutzten SaaS-Tools mit Abo-Kosten/Monat
- API-Verfügbarkeit pro Tool (ja/nein) — entscheidet über Integrationsmöglichkeit
- Bestehende Automationen: Was läuft bereits automatisch, aber wird nicht bewusst wahrgenommen?

## Analyseprozess

1. **Prozess-Inventarisierung (Workshop-Format, 90 Minuten)**
   - Workshop mit je einer Person pro Abteilung (Marketing, Sales, Ops)
   - Instruktion: "Beschreibt mir eure Woche. Was macht ihr, ohne wirklich nachzudenken? Was fühlt sich wie Busywork an?"
   - Output: 20–35 identifizierte Prozesse auf Karten/Miro-Board
   - Direkt im Workshop: Zeitschätzung pro Prozess (Minuten/Instanz, Instanzen/Woche)

2. **Automatisierbarkeits-Bewertung**
   - Jeder Prozess wird gegen drei Dimensionen bewertet:

   **Dimension A: Prozessklarheit (1–5)**
   1 = Prozess lebt in Köpfen, keine klaren Regeln
   3 = Prozess ist dokumentiert, aber mit Ausnahmen
   5 = Prozess ist vollständig regelbasiert, keine Ausnahmen

   **Dimension B: Technische Umsetzbarkeit (1–5)**
   1 = Beteiligte Tools haben keine API oder Automation-Support
   3 = Teilweise API-Unterstützung, manuelle Schritte unvermeidbar
   5 = Alle beteiligten Tools haben native Integration oder API

   **Dimension C: Datenverfügbarkeit (1–5)**
   1 = Input-Daten unstrukturiert oder unvollständig
   3 = Daten vorhanden, aber in verschiedenen Systemen
   5 = Alle Input-Daten strukturiert, in einem System, aktuell

   - **Automatisierbarkeits-Score** = (A + B + C) / 15 × 100%
   - Score ≥70%: Direkter Automatisierungs-Kandidat
   - Score 40–69%: Bedingt automatisierbar nach Vorbereitung (Prozess klären oder Daten sanieren)
   - Score <40%: Kein Automatisierungs-Kandidat in den nächsten 6 Monaten

3. **CHF-Einsparpotenzial-Kalkulation**
   - Formel: (Minuten/Instanz × Instanzen/Woche × 52) / 60 × Stundensatz (CHF) = **Jahres-CHF-Einsparpotenzial**
   - Stundensatz-Referenzwerte (Deutschschweiz):
     - Junior Marketing/Sales: CHF 60–75/h
     - Senior Marketing/Sales: CHF 90–120/h
     - Geschäftsleitung: CHF 150–250/h
   - Zusätzlich: **Fehlerkosten schätzen** — wie häufig passieren Fehler im manuellen Prozess, und was kosten sie? (Verlorener Deal, doppelter Versand, falscher Empfänger)
   - Implementierungskosten schätzen:
     - Einfache Automation (Zapier/Make, 1–3 Schritte): CHF 500–1'500 einmalig
     - Mittlere Automation (Multi-Step, CRM-Integration): CHF 2'000–6'000 einmalig
     - Komplexe Automation (AI-Layer, mehrere Systeme, Testing): CHF 6'000–15'000 einmalig
   - ROI-Berechnung: Jahres-CHF-Einsparpotenzial ÷ Implementierungskosten = **Amortisationsdauer (Monate)**

4. **Priorisierungs-Matrix erstellen**
   - Alle Kandidaten in einer 2×2-Matrix platzieren:
     - X-Achse: CHF-Einsparpotenzial/Jahr (niedrig vs. hoch)
     - Y-Achse: Automatisierbarkeits-Score (niedrig vs. hoch)
   - Quadrant 1 (oben rechts): **Priorität 1 — jetzt umsetzen** — hoch automatisierbar, hohes Einsparpotenzial
   - Quadrant 2 (oben links): **Priorität 2 — Quick Wins** — hoch automatisierbar, mittleres Potenzial
   - Quadrant 3 (unten rechts): **Priorität 3 — nach Vorbereitung** — grosses Potenzial, aber Fundament fehlt
   - Quadrant 4 (unten links): **Deprioritisiert** — kleines Potenzial, schwer automatisierbar

5. **Tool-Gap-Analyse**
   - Identifiziere, welche Automationen mit dem bestehenden Stack möglich sind
   - Identifiziere, welche Automationen zusätzliche Tools erfordern
   - Berechne: Tool-Zusatzkosten (CHF/Monat) vs. Einsparpotenzial — Break-even-Punkt?
   - Identifiziere redundante Tools im Stack (gezahlt, aber nicht genutzt oder überlappend)

## Bewertungslogik

**Level 1 — Manuell-Betrieb (0–20% automatisiert)**
Fast alle Prozesse laufen manuell. Wachstum erfordert proportional mehr Personal. Fehlerrate hoch. CHF-Einsparpotenzial typischerweise CHF 50'000–150'000/Jahr, aber noch nicht realisierbar mangels Prozessklarheit. Sofortiger Fokus: Prozesse dokumentieren und Top-3-Kandidaten identifizieren.

**Level 2 — Teilautomatisiert (21–40% automatisiert)**
Einzelne Automationen existieren (z.B. automatische Bestätigungs-Mails), aber die meisten Prozesse sind noch manuell. Häufig: Insellösungen ohne Verbindung untereinander. CHF-Einsparpotenzial: CHF 30'000–80'000/Jahr.

**Level 3 — Kernsystem automatisiert (41–60% automatisiert)**
Die wichtigsten Marketing-Automationen laufen (Lead-Nurturing, Follow-up-Sequenzen). Sales pflegt CRM, aber noch weitgehend manuell. Reporting teilweise automatisiert. CHF-Einsparpotenzial in verbleibenden Prozessen: CHF 20'000–50'000/Jahr.

**Level 4 — Revenue Engine mehrheitlich automatisiert (61–80% automatisiert)**
Marketing- und Sales-Prozesse sind grösstenteils automatisiert. Manuelle Eingriffe nur für Ausnahmen und Urteilsentscheide. Reporting läuft automatisch. Fokus: Optimierung bestehender Automationen und Ausweitung auf komplexere Prozesse.

**Level 5 — Automation-First-Betrieb (>80% automatisiert)**
Das Unternehmen wächst ohne proportional steigenden operativen Aufwand. Team-Zeit konzentriert sich auf Strategie, Beziehung und Kreativität. Wenige KMU in der Deutschschweiz erreichen dieses Niveau — es erfordert 2–3 Jahre konsequente Automatisierungs-Investition.

## Output

- **Prozess-Inventar-Tabelle**: Alle erhobenen Prozesse mit Zeitaufwand, Automatisierbarkeits-Score und CHF-Einsparpotenzial
- **Priorisierungs-Matrix**: Visuelle 2×2-Darstellung aller Automatisierungs-Kandidaten
- **Top-5-Automatisierungen mit Business Case**: Für jede: Prozessbeschreibung, Tool-Vorschlag, Implementierungsaufwand, CHF-Einsparpotenzial, Amortisationsdauer
- **Tool-Gap-Report**: Fehlende Tools, redundante Tools, Integrations-Empfehlungen
- **Gesamt-CHF-Einsparpotenzial**: Über alle identifizierten Automationen aggregiert — mit realistischem 12-Monats-Realisierungspotenzial
- **90-Tage-Automatisierungs-Roadmap**: Priorisierte Implementierungsreihenfolge mit klaren Meilensteinen

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Einen Automation-Sprint starten: Die #1-Automatisierung aus der Priorisierungs-Matrix in 1–2 Wochen umsetzen — Ziel ist ein sichtbarer Zeitgewinn für das Team als Motivationsanker
- Make.com oder Zapier-Zugang einrichten: Kostenlos oder CHF 29/Monat — ermöglicht 90% aller einfachen Automationen ohne Entwicklerkosten
- Sofort starten: Lead-Benachrichtigung bei Formular-Einreichung automatisieren (Trigger: HubSpot-Formular → Slack-Nachricht an Sales → CRM-Eintrag anlegen) — Setup: 45 Minuten, Zeitersparnis: 30–60 Minuten/Tag

**Mittelfristig (1–3 Monate)**
- CRM-Datenpflege-Automation: Automatisches Logging von E-Mail-Aktivitäten, Call-Zusammenfassungen (AI-gestützt via Gong oder HubSpot AI) und Deal-Stage-Übergänge
- Marketing-Reporting-Automation: Wöchentlicher Report aus GA4 + HubSpot automatisch an Geschäftsleitung — spart typischerweise 2–4 Stunden/Woche für Marketing
- Proposal-Erstellungs-Automation: Template-basierte Angebote mit dynamischen Feldern aus CRM — Zeitreduktion von 60–90 Minuten auf 10–15 Minuten pro Angebot

**Strategisch (3–12 Monate)**
- End-to-End-Lead-to-Revenue-Automation aufbauen: Von Lead-Capture über Nurturing, Qualifizierung, Handover und Onboarding — jeder Schritt automatisch getriggert, menschliche Eingriffe nur bei definierten Ausnahmen
- Predictive Operations: AI-gestützte Vorhersage, welche Deals diese Woche Attention brauchen, basierend auf CRM-Daten und Aktivitäts-Patterns
- Kosten-Controlling der Automation-Stack: Vierteljährliches Audit aller Automation-Tools — was wird genutzt, was kann gekündigt werden?

## Performanceboost Perspektive

Wir führen das Process Automation Assessment nicht als IT-Projekt durch — wir führen es als Revenue-Analyse durch. Die Frage ist nie "Welche Prozesse können wir automatisieren?" Die Frage ist immer: "Welche manuellen Prozesse kosten uns Pipeline, Deals oder Kunden?" Das sind die Prozesse, die sofort angegangen werden.

Konkret: Bei einem unserer Kunden (B2B-SaaS, 30 MA) hat das Assessment ergeben, dass SDRs 11 Stunden pro Woche für Prospect-Recherche und CRM-Pflege aufwandten. Amortisation der Automatisierung in 2,3 Monaten. Aber noch wichtiger: Die 11 Stunden wurden in aktive Outreach-Zeit umgewandelt — was die Anzahl der wöchentlichen Erstkontakte von 40 auf 90 erhöhte, bei gleichem Team. Das ist der Multiplikator-Effekt, den wir mit Automatisierung suchen: nicht Kosten sparen, sondern Kapazität für wachstumsrelevante Aktivität freimachen.
