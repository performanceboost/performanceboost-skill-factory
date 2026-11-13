# MarTech Stack Inventory

## Zweck
Dieses Skill-Dokument liefert eine vollständige Inventur des MarTech-Stacks, also aller Programme, mit denen ein Unternehmen Kunden gewinnt und betreut: CRM, Website und Formulare, E-Mail und Newsletter, Werbekonten, Tracking, Reporting, Automatisierung und die Tabellen dazwischen. Ergebnis ist eine Liste mit Kosten, Nutzung, Verantwortlichen und Datenflüssen sowie ein Entscheid pro Tool: behalten, ersetzen, abschaffen oder fehlt. Die Inventur ist die Grundlage für weniger Lizenzen, weniger Handarbeit und jeden späteren Einsatz von KI.

## Wann verwenden
- Wenn die Lizenzkosten steigen und niemand genau weiss, welche Tools noch gebraucht werden
- Wenn Daten von Hand zwischen Systemen kopiert werden
- Wenn Zahlen aus CRM, Website-Analyse und Werbekonten nicht übereinstimmen
- Vor der Einführung eines neuen CRM, einer Marketing-Automatisierung oder von KI-Agenten
- Nach einem Wechsel in der Geschäftsleitung oder im Marketing, wenn Wissen über Tools verloren gegangen ist
- Als jährliche Überprüfung, idealerweise vor der Budgetplanung

## Input

**Aus Buchhaltung und Kreditkartenabrechnungen (letzte 12 Monate):**
- Alle wiederkehrenden Zahlungen an Software-Anbieter
- Jahres- und Monatsabos, Anzahl Lizenzen, Kündigungsfristen

**Aus den Tools selbst:**
- Liste der Benutzerkonten und letzte Anmeldung (meist in den Admin-Einstellungen)
- Aktive Schnittstellen und Automatisierungen
- Welche Personendaten im Tool gespeichert sind und wo der Anbieter sie speichert

**Aus kurzen Gesprächen mit Marketing, Vertrieb und Geschäftsleitung (je 20–30 Minuten):**
- Welche Tools nutzen Sie täglich, welche selten, welche nie?
- Wo kopieren Sie Daten von Hand von einem System ins andere?
- Welche Auswertung fehlt Ihnen heute?
- Welche Tools wurden eingeführt, aber nie richtig genutzt?

## Analyseprozess

1. **Alle Tools erfassen**
   - Pro Tool eine Zeile: Name, Zweck in einem Satz, Kosten pro Jahr, Kündigungsfrist, Anzahl Lizenzen, verantwortliche Person
   - Auch kostenlose Tools und Tabellen aufnehmen, wenn darin Kundendaten liegen
   - Tools ohne verantwortliche Person markieren

2. **Nutzung prüfen**
   - Anzahl Lizenzen mit Anzahl aktiver Nutzerinnen und Nutzer vergleichen (Anmeldung in den letzten 90 Tagen)
   - Ungenutzte Lizenzen und Tools ohne Anmeldung seit über 90 Tagen markieren
   - Kosten pro aktiver Person berechnen: Jahreskosten / aktive Nutzer

3. **Überschneidungen finden**
   - Funktionen gruppieren: Kontakte speichern, E-Mails versenden, Formulare, Termine, Auswertungen, Automatisierung
   - Pro Funktion zählen, wie viele Tools sie abdecken
   - Funktionen markieren, die in einem bereits bezahlten Tool vorhanden sind, aber über ein zweites Tool genutzt werden

4. **Datenflüsse aufzeichnen**
   - Den Weg einer neuen Anfrage vom ersten Kontakt bis zur Offerte aufzeichnen
   - Jede Stelle markieren, an der Daten von Hand übertragen werden, mit geschätzter Häufigkeit pro Monat
   - Festhalten, welches System für Kundendaten führend ist (falls keines: als Lücke markieren)

5. **Datenschutz prüfen**
   - Pro Tool: Welche Personendaten liegen darin, wo speichert der Anbieter sie (Schweiz, EU, andere Länder)?
   - Prüfen, ob alle Tools mit Personendaten in der Datenschutzerklärung aufgeführt sind
   - Hinweis: Diese Prüfung ersetzt keine Rechtsberatung

6. **Lizenz prüfen (bei Open-Source-Tools)**
   - Lizenzdatei des Projekts lesen, nicht nur die Angabe in Tool-Verzeichnissen
   - Prüfen, ob die Lizenz Einschränkungen für die kommerzielle Nutzung enthält

## Bewertungslogik

Jedes Tool erhält einen von vier Entscheiden:

| Entscheid | Kriterien |
|---|---|
| **Behalten** | Klarer Zweck, verantwortliche Person, wird genutzt, Daten fliessen automatisch |
| **Ersetzen** | Zweck nötig, aber Tool passt nicht zu den Abläufen, ist nicht verbunden oder zu teuer pro aktiver Person |
| **Abschaffen** | Keine Nutzung seit über 90 Tagen, Funktion bereits in einem anderen Tool vorhanden, oder kein Zweck mehr |
| **Fehlt** | Funktion wird gebraucht, ist aber nicht abgedeckt (z. B. kein führendes System für Kundendaten) |

Zusätzlich wird der Stack als Ganzes eingestuft:

**Stufe 1 — Wildwuchs**
Kein Überblick über Tools und Kosten. Kein führendes System für Kundendaten. Daten werden regelmässig von Hand übertragen. Mehrere Tools ohne verantwortliche Person.

**Stufe 2 — Überblick**
Tools und Kosten sind bekannt. Überschneidungen und ungenutzte Lizenzen sind identifiziert, aber noch nicht bereinigt. Einzelne Verbindungen bestehen.

**Stufe 3 — Verbunden**
Ein führendes System für Kundendaten. Die wichtigsten Abläufe (Anfrage, Newsletter, Auftrag) laufen ohne Abtippen. Jedes Tool hat eine verantwortliche Person.

**Stufe 4 — Gesteuert**
Neue Tools werden vor dem Kauf geprüft. Kosten werden jährlich überprüft. Verbindungen melden Fehler. Grundlage für den Einsatz von KI-Agenten ist vorhanden.

## Output

- Tool-Liste mit Zweck, Kosten pro Jahr, Lizenzen, aktiven Nutzern, Verantwortlichen und Entscheid
- Übersicht der Überschneidungen pro Funktion
- Skizze der Datenflüsse mit allen Stellen, an denen von Hand übertragen wird
- Liste der Tools mit Personendaten und Speicherort
- Jährliche Kosten heute und nach Umsetzung der Entscheide
- Einstufung des Stacks (Stufe 1–4) und die nächsten drei Schritte

## Empfehlungen

**Sofort (0–30 Tage)**
- Ungenutzte Lizenzen reduzieren, Kündigungsfristen in den Kalender eintragen
- Für jedes Tool eine verantwortliche Person festlegen
- Vor jeder Kündigung die Daten exportieren

**Mittelfristig (1–3 Monate)**
- Ein führendes System für Kundendaten festlegen, meist das CRM
- Den häufigsten Ablauf (meist die Website-Anfrage) ohne Abtippen ins CRM führen
- Doppelte Funktionen zusammenführen, zuerst dort, wo die meisten Daten liegen

**Strategisch (3–12 Monate)**
- Regel einführen: neue Tools nur nach Prüfung von Zweck, Verbindung, Datenschutz und Kosten
- Jährliche Inventur vor der Budgetplanung
- Erst auf dieser Grundlage KI-Anwendungen und KI-Agenten einführen
