# CRM Data Quality Check

## Zweck
Dieses Skill-Dokument liefert eine systematische Bewertung der CRM-Datenqualität entlang fünf Dimensionen: Vollständigkeit, Aktualität, Duplikatrate, Konsistenz und Verwertbarkeit. Schlechte CRM-Daten sind der unsichtbare Multiplikator aller anderen Revenue-Probleme: Automation trifft falsche Empfänger, Forecasts sind unzuverlässig, Attribution ist lückenhaft, und Personalisierung produziert peinliche Fehler. Dieser Check quantifiziert das Problem in CHF — und liefert einen priorisierten Bereinigungsplan.

## Wann verwenden
- Vor der Einführung oder Erweiterung von Marketing-Automation
- Wenn E-Mail-Kampagnen ungewöhnlich hohe Bounce- oder Unsubscribe-Raten zeigen
- Nach Migration von einem alten CRM auf ein neues System
- Wenn Reporting-Zahlen zwischen CRM, Marketing-Automation und Analytics-Tool nicht übereinstimmen
- Vor einem grossen Outreach-Programm oder einem Account-Based-Marketing-Launch
- Als Jahres-Hygiene-Check — empfohlen mindestens einmal pro Quartal

## Input

**Aus CRM (vollständiger Export aller aktiven und inaktiven Records):**
- Alle Contact-Records mit allen befüllten und leeren Feldern
- Alle Company/Account-Records mit zugehörigen Contacts
- Alle Deal-Records mit Stage, Wert, Owner, Erstellungsdatum, letzter Aktivität
- Activity-Log: E-Mails, Anrufe, Meetings — letzte 12 Monate
- Duplikat-Report des CRM-Systems (falls nativ verfügbar)

**Aus Marketing-Automation:**
- Liste aller aktiven Sequenzen und Zielgruppen-Segmente
- Bounce-Rate je Domain und E-Mail-Adresstyp
- Unsubscribe-Rate letzte 6 Monate
- Contacts ohne Marketing-Automation-Sync (Datenlücke zwischen CRM und MAP)

**Aus Team-Interview (Marketing-Ops, Sales-Ops, je 30 Minuten):**
- Wie werden neue Contacts ins CRM eingegeben? Manuell, via Import, via Formular?
- Gibt es Duplizierungsprobleme, die dem Team bekannt sind?
- Welche CRM-Felder werden für Segmentierung und Automation aktiv genutzt?
- Wann wurde die letzte gezielte Datenbereinigung durchgeführt?

## Analyseprozess

1. **Vollständigkeitsanalyse (Completeness)**
   - Die 15 umsatzrelevantesten CRM-Felder definieren (Beispiele: Vorname/Nachname, Geschäfts-E-Mail, Firma, Jobtitel, Branche, Firmengrösse, Land, Lead-Source, ICP-Kriterium, Lead-Score, letzter Kontakt, zuständiger Rep, Deal-Stage, Deal-Wert, Next-Step-Datum)
   - Vollständigkeitsquote je Feld berechnen: Anzahl befüllter Records / Total Records × 100
   - Kritische Schwellen:
     - <70% Vollständigkeit = kritisch (Automation und Segmentierung versagen hier)
     - 70–85% = akzeptabel aber verbesserungswürdig
     - >85% = gut, >95% = Best-in-Class
   - Felder mit niedriger Vollständigkeit auf Ursachen prüfen: Fehlender Pflichtfeld-Status? Kein Prozess für Datenpflege? Veraltete Importquellen?

2. **Aktualitätsanalyse (Recency)**
   - Letztes Aktivitätsdatum je Contact berechnen: Wie viele Contacts wurden in den letzten 12 Monaten kontaktiert?
   - Segmentierung nach Alter:
     - Aktiv (letzte Aktivität <6 Monate): Direkt nutzbar
     - Schlafend (6–24 Monate ohne Aktivität): Validierung empfohlen vor nächstem Outreach
     - Zombie-Contacts (>24 Monate ohne Aktivität): E-Mail-Validierung obligatorisch, Segmentierung separat
   - Typischer Befund: Schweizer KMU-CRMs enthalten im Schnitt 25–40% Records, die älter als 24 Monate ohne Aktivität sind — ein direktes Hard-Bounce-Risiko
   - Company-Records: Wie viele haben veraltete Umsatz-, Mitarbeiterzahl- oder Website-Einträge (prüfbar via Clearbit, Apollo oder LinkedIn)?

3. **Duplikatanalyse**
   - Duplikate auf zwei Ebenen prüfen: Contact-Duplikate (gleiche Person, mehrere Records) und Company-Duplikate (gleiche Firma, mehrere Records)
   - Matching-Logik anwenden: E-Mail-Adresse (eindeutig), Telefonnummer, Vor-/Nachname + Firma
   - Duplikatrate berechnen: Anzahl Duplikate / Total Records × 100
   - Benchmarks:
     - <3% = gut
     - 3–8% = akzeptabel
     - >8% = kritisch (Automation sendet doppelt, Reps kontaktieren dieselbe Person mehrfach, Reporting ist verzerrt)
   - Typischer CHF-Impact von Duplikaten: Doppelte E-Mail-Credits in Marketing-Automation (bei 10'000 Contacts und 5% Duplikatrate = 500 unnötige Kontakt-Lizenzen), Peinlichkeitsfaktor bei Kalt-Outreach («Hallo Herr Müller» — gleiche Firma, dritter Kontaktversuch)

4. **Konsistenzanalyse (Consistency)**
   - Feldformate prüfen: Telefonnummern (einheitlich mit +41 oder ohne?), Jobtitels (CEO vs. Chief Executive Officer vs. Geschäftsführer — drei verschiedene Werte für dieselbe Funktion)
   - Picklist-Felder auf unerwünschte Freitext-Einträge prüfen: Branche, Firmengrösse, Region
   - Grossschreibung und Sonderzeichen in Namen und Firmennamen validieren (Automation-Personalisierung scheitert an «herr müller» oder «MÜLLER CONSULTING AG» im Kontrast zu «Max Müller»)
   - Widersprüchliche Daten aufdecken: Contacts ohne Company-Record, Deals ohne zugehörigen Contact, Companies ohne Website

5. **Verwertbarkeitsanalyse (Usability)**
   - Segmentierbarkeit prüfen: Können die geplanten Zielgruppen aus den vorhandenen Daten tatsächlich gebildet werden?
   - Automation-Readiness: Welche der aktiven Automationen würden bei aktueller Datenlage fehlschlagen?
   - Attribution-Vollständigkeit: Wie viele Contacts haben keinen Lead-Source-Eintrag? (Ziel: <10% ohne Attribution)
   - Reporting-Konsistenz: Stimmt die Kontaktzahl im CRM mit dem Marketing-Automation-System überein?

## Bewertungslogik

**Level 1 — Datenchaos (0–20 Punkte)**
Durchschnittliche Feldvollständigkeit <60%. Duplikatrate >15%. Keine strukturierten Picklists. Mehr als 40% der Contacts älter als 24 Monate ohne Aktivität. Attribution fehlt vollständig. Automation produziert regelmässig Fehler oder erreicht falsche Personen. Reporting unbrauchbar.

**Level 2 — Basisqualität (21–40 Punkte)**
Pflichtfelder mehrheitlich befüllt (70–80% Vollständigkeit), aber keine Datenpflege-Prozesse. Duplikatrate 8–15%. Jobtitel und Branchen-Felder inkonsistent. Viele Zombie-Contacts unreflektiert in aktiven Segmenten. Automation funktioniert, trifft aber regelmässig falsche Empfänger.

**Level 3 — Strukturiert (41–60 Punkte)**
Vollständigkeitsquote der Kernfelder >80%. Duplikatrate 4–8%. Erste Datenbereinigung durchgeführt. Picklists standardisiert. Attribution für >75% der Contacts vorhanden. Regelmässige, aber manuelle Hygiene-Prozesse. Schweizer KMU-Standard bei gut geführten Marketing-Ops-Teams.

**Level 4 — Qualitätsbewusst (61–80 Punkte)**
Vollständigkeit >90% auf allen Kernfeldern. Duplikatrate <4%. Zombie-Contacts in separates Segment ausgelagert. Datenpflege-Prozesse automatisiert (z.B. regelmässige Enrichment-Läufe via Clearbit oder Clay). Attribution >90%. Reporting zwischen CRM und MAP konsistent.

**Level 5 — Daten-Excellence (81–100 Punkte)**
Vollständigkeit >95%. Duplikatrate <2%. Automatisierte Enrichment-Prozesse halten Firmengrösse, Jobtitel und Kontaktdaten aktuell. Attribution 100%. Regelmässige Qualitäts-KPIs im RevOps-Dashboard sichtbar. Datenpflege ist kein Projekt — sie ist ein kontinuierlicher Prozess.

## Output

- CRM-Qualitäts-Scorecard: Gesamtscore (0–100) nach Dimension aufgeschlüsselt
- Vollständigkeits-Heatmap: Je Feld mit Ampelfarbe und Prozentsatz
- Duplikat-Liste mit Merge-Empfehlung (priorisiert nach Relevanz der betroffenen Records)
- Zombie-Contact-Segment: Exportierbare Liste mit empfohlener Aktion (reaktivieren / validieren / archivieren)
- Inkonsistenz-Report: Felder mit Formatproblemen und Korrekturvorschlag
- CHF-Impact-Schätzung: Kosten schlechter Daten (Lizenzgebühren für Duplikate, Bounce-Kosten, entgangene Attribution)
- Priorisierter Bereinigungsplan: Was zuerst, was kann warten

## Empfehlungen

**Quick Wins (0–30 Tage)**
- Duplikate bereinigen: HubSpot Duplicate Manager, Dedupely, oder nativer Salesforce-Prozess — bei >500 Duplikaten Tool-gestützte Bereinigung, nicht manuell
- Zombie-Contacts aus aktiven Marketing-Listen entfernen: separates Segment erstellen, nicht löschen
- Pflichtfelder im CRM technisch erzwingen: Vorname, Nachname, Firma, E-Mail, Lead Source — keine Umgehung möglich
- E-Mail-Validierung für Contacts >18 Monate ohne Aktivität durchführen (Tool: Neverbounce, Zerobounce, oder nativer HubSpot-Validator) — vor dem nächsten grossen Outreach

**Mittelfristig (1–3 Monate)**
- Picklists für alle Dropdown-Felder standardisieren: Branche, Firmengrösse, Land, Region — bestehende Freitext-Werte normalisieren
- Enrichment-Prozess aufbauen: Neuen Contacts werden automatisch Firmengrösse, Branche und LinkedIn-URL angehängt (Clay, Clearbit, Apollo oder HubSpot Enrichment)
- Datenpflege-Verantwortung zuweisen: Wer ist für CRM-Datenqualität zuständig? Ohne namentliche Verantwortung keine nachhaltige Hygiene
- CRM-MAP-Sync prüfen und bereinigen: Stellen sicher, dass alle CRM-Contacts korrekt in der Marketing-Automation-Plattform gespiegelt sind

**Strategisch (3–12 Monate)**
- Kontinuierliches Enrichment einrichten: Automatischer Daten-Refresh alle 90 Tage für aktive Accounts
- CRM-Qualitäts-KPIs ins RevOps-Dashboard integrieren: Vollständigkeitsquote, Duplikatrate und Aktualität als monatliche Metriken
- Data-Governance-Policy schreiben: Wie werden neue Records erstellt? Wer darf Felder ändern? Wie werden veraltete Records archiviert?
- Rückverfolgung von Datenqualität auf Geschäftsergebnisse: Konversionsrate segmentiert nach Datenqualität des Leads — zeigt den ROI der Datenbereinigung in CHF

## Performanceboost Perspektive

Schlechte CRM-Daten sind kein technisches Problem. Sie sind ein Symptom fehlender Prozesse und fehlender Verantwortlichkeit. «Wir haben zu wenig Ressourcen, um das sauber zu halten» ist die häufigste Aussage — und meistens falsch. Was fehlt, ist ein klarer Prozess, wer bei welchem Trigger was ins CRM einträgt. Wenn das definiert ist, kostet Datenpflege weniger Zeit als die monatliche Bereinigung von Chaos.

Performanceboost empfiehlt den CRM Data Quality Check als Pflicht-Schritt vor jeder Automation oder jedem Outreach-Programm. Nicht weil Datenqualität an sich sexy ist — sondern weil jede Automation, jedes Scoring-Modell und jedes Attribution-Modell auf der Qualität der zugrunde liegenden Daten basiert. Ein Revenue-System, das auf schlechten Daten läuft, optimiert sich in die falsche Richtung. Schneller. Wir haben in der Praxis erlebt, dass eine Datenbereinigung von 2–3 Tagen die Attribution-Abdeckung von 55% auf 88% gebracht hat — und damit die Entscheidungsgrundlage für CHF 400'000 Marketingbudget fundamental verändert hat.
