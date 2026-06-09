# Content-to-Pipeline Audit

## Zweck
Dieses Framework misst, welcher Content tatsächlich zu Pipeline und Revenue beiträgt — und welcher Content nur Traffic, Vanity-Metriken oder Kontaktvolumen ohne Konversion generiert. Es verbindet Content-Metriken (Visits, Downloads, Engagement) mit CRM-Daten (MQLs, SQLs, Opportunities, Closed Won) für eine Attribution, die auf CHF-Basis entschieden werden kann. Ohne diese Verbindung wird Content-Budget nach Gefühl verteilt: meistgelesene Artikel werden weitergeschrieben, obwohl sie keinen einzigen Deal beeinflusst haben.

## Wann verwenden
- Content-Ausgaben (Zeit oder CHF) sollen gegenüber der Geschäftsführung gerechtfertigt werden
- Das Content-Volumen wächst, aber die MQL-Zahlen stagnieren
- Entscheid steht an, welche Content-Formate oder -Themen priorisiert oder eingestellt werden sollen
- Sales beschwert sich, dass Marketing-Content im Vertrieb nicht nutzbar ist
- Eine neue Content-Strategie soll auf der Basis bestehender Performance entwickelt werden

## Input

**Analytics-Daten (GA4, HubSpot, Similarweb)**
- Seitenaufrufe und eindeutige Besucher je Content-Asset (letzten 6 Monate)
- Durchschnittliche Verweildauer je Asset
- Absprungrate je Asset
- Klickpfad: Von welchem Content-Asset wird zu welcher Conversion-Page navigiert?
- Scroll-Tiefe bei Long-Form-Content (wenn verfügbar)
- Download-Zahlen je Lead-Magnet (Guide, Checklist, Assessment, Template)

**Lead-Generierungs-Daten (CRM + Marketing Automation)**
- Anzahl Formular-Ausfüllungen je Landing Page / Lead-Magnet
- Conversion-Rate Besucher → Lead je Asset
- First-Touch-Attribution: Welcher Content war der erste Berührungspunkt eines Kontakts?
- Last-Touch-Attribution: Welcher Content unmittelbar vor MQL-Qualifizierung konsumiert?
- Multi-Touch: Welche Content-Assets erscheinen in mehr als 30 % der Conversion-Pfade von MQLs?

**Pipeline- und Revenue-Daten (CRM)**
- Anzahl MQLs, die einen spezifischen Content konsumiert haben
- Anzahl SQLs, Opportunities und Closed-Won-Deals je Content-Asset (via Multi-Touch-Attribution)
- Pipeline-Wert (CHF) beeinflusst durch Content-Asset
- Content-assisted Revenue: Deals, bei denen Content mind. einen Touchpoint hatte

**Content-Kosten-Daten**
- Produktionskosten je Asset (interne Stunden × Stundensatz + externe Kosten in CHF)
- Distributions-/Promotion-Kosten (Paid Social, Newsletter, SEO-Optimierung)
- Gesamt-Content-Budget aktuell (CHF/Monat)

## Analyseprozess

**Schritt 1: Content-Inventar erstellen und klassifizieren**
- Alle aktiven Content-Assets erfassen: Blogartikel, Whitepapers, Guides, Webinare, Case Studies, Templates, Assessments, Videos, Podcast-Episoden
- Je Asset klassifizieren nach: Funnel-Stage (TOFU/MOFU/BOFU), Format, Thema/Cluster, Produktionsdatum
- Assets über 18 Monate ohne Update separat kennzeichnen (potenzielle Dead-Weight-Assets)
- Ergebnis: Inventar-Tabelle mit ~5–8 Metadaten-Feldern je Asset

**Schritt 2: Traffic-zu-Lead-Konversion je Asset messen**
- Conversion-Rate = Leads aus Asset ÷ Unique Visitors je Asset
- Benchmarks:
  - TOFU-Blog-Artikel: 0.5–2 % (primär Awareness, niedrige Conversion erwartet)
  - MOFU-Guides/Whitepapers: 5–15 % (Gated Content mit Formular)
  - BOFU-Case Studies/Demo-Seiten: 8–20 % (hohe Kaufbereitschaft)
  - Landing Pages für Paid Traffic: 10–25 % (optimiert auf Conversion)
- Assets mit Conversion-Rate unter 50 % des Benchmarks sind Optimierungs-Kandidaten

**Schritt 3: Lead-zu-MQL-Qualität je Content-Source messen**
- MQL-Rate = MQLs aus Content-Source ÷ Leads aus Content-Source
- Differenz zwischen Content-Quellen aufdecken: Ein Guide kann 200 Leads und 8 MQLs liefern (4 %), ein Case Study 15 Leads und 9 MQLs (60 %)
- Content mit hoher Lead- aber niedriger MQL-Rate signalisiert: falsches Publikum angezogen oder Lead-Magnet zu generisch
- Content mit niedriger Lead- aber hoher MQL-Rate signalisiert: unterschätztes Asset mit qualifizierterem Publikum

**Schritt 4: Pipeline-Attribution berechnen**
- Multi-Touch-Attribution implementieren (empfohlen: Linear oder Time-Decay für B2B)
- Je Asset: Pipeline-Wert (CHF) = Summe der anteiligen Opportunity-Werte aller Deals, in denen das Asset einen Touchpoint hatte
- Content-ROI je Asset = Pipeline-Wert ÷ Produktionskosten
- Benchmark Best-in-Class: Content-ROI > 10x (d. h. CHF 500 Produktionskosten → CHF 5'000+ Pipeline-Wert)
- Assets unter 3x ROI sind Abschreibungs-Kandidaten, es sei denn, sie erfüllen eine strategische Awareness-Funktion

**Schritt 5: Content-Gap-Analyse nach Funnel-Stage und ICP-Segment**
- Für welche Funnel-Stage existiert zu wenig Content? (Häufigster Befund: MOFU unterversorgt)
- Für welches ICP-Segment fehlen spezifische Assets? (z. B. Use Cases für Branchen-Cluster)
- Welche Einwände oder Fragen von Sales sind nicht durch Content abgedeckt?
- Battle-Card- und Proposal-Template-Lücken separat auflisten

## Bewertungslogik

**Reifegrad-Modell: Content-to-Pipeline Reife (5 Stufen)**

**Stufe 1 — Dekorativ (Content ohne Messung)**
Content wird produziert und veröffentlicht. Erfolg wird an Pageviews oder "gutes Feedback" gemessen. Kein Formular-Tracking, keine Lead-Attribution, keine CRM-Verbindung. Content-Budget ist de facto ein Reputations-Budget ohne Accountability.

**Stufe 2 — Vanity-getrieben (Reach-Metriken dominieren)**
Pageviews, Social Shares und Newsletter-Abonnenten werden gemessen. Lead-Generierung wird über Formular-Submits verfolgt, aber nicht nach MQL-Qualität differenziert. Attribution endet beim ersten Touchpoint. Typische Fehleraussage: "Unser meistgelesener Artikel ist unser bester Content."

**Stufe 3 — Lead-Attribution vorhanden (First-Touch, kein Multi-Touch)**
Content-zu-Lead-Attribution ist aktiv. First-Touch-Source im CRM vorhanden. Aber Multi-Touch-Attribution fehlt — Beiträge in der Mitte des Funnels sind unsichtbar. MQL-Rate je Content-Source noch nicht berechnet. 40–60 % des Content-Portfolios liefert messbar Leads, Rest ungemessen.

**Stufe 4 — Pipeline-Attribution (Multi-Touch, CHF-basiert)**
Multi-Touch-Attribution aktiv. Pipeline-Wert je Asset berechenbar. Content-ROI wird quartalsweise ausgewertet. Budget-Entscheide basieren auf Attribution-Daten. 20–30 % des Content-Portfolios liefert über 80 % des content-assisted Revenue (80/20 sichtbar und genutzt).

**Stufe 5 — Predictive Content (Attribution steuert Produktion)**
Content-Produktion wird durch Attribution-Daten gesteuert: Formate, Themen und Funnel-Stage werden nach ROI priorisiert. Content-Gap-Analyse ist quarterl Standard. Sales nutzt MOFU/BOFU-Content aktiv in Deals. Content-ROI Best Assets über 15x. Content-Portfolio wird aktiv bereinigt — tote Assets werden depubliziert oder konsolidiert.

## Output

- **Content-Performance-Matrix**: Alle Assets nach Traffic, Conversion-Rate, MQL-Rate, Pipeline-Wert (CHF) und Content-ROI
- **Top-10-Pipeline-Treiber**: Die zehn Assets mit höchstem anteiligem Pipeline-Wert
- **Bottom-10-Dead-Weight**: Assets mit hohem Produktionsaufwand aber unter 1x Content-ROI
- **Funnel-Coverage-Map**: Welche Stages und ICP-Segmente sind über- oder unterversorgt
- **Content-Gap-Liste**: Priorisierte Liste fehlender Assets (nach Pipeline-Hebelwirkung geordnet)
- **Budget-Umverteilungs-Empfehlung**: Aktuelle vs. empfohlene Budget-Allokation nach Content-Typ und Funnel-Stage

## Empfehlungen

**Quick Wins (0–30 Tage)**
- GA4-Formular-Tracking und CRM-Source-Felder prüfen und bereinigen — ohne saubere Datenbasis ist jede Attribution unbrauchbar
- Die drei bestperformenden MOFU-Assets identifizieren und in Sales-Enablement-Prozess integrieren
- Dead-Weight-Assets (unter 100 Visits, 0 Leads in 6 Monaten) auf No-Index setzen oder konsolidieren
- Conversion-Rate der drei meistbesuchten TOFU-Assets prüfen — wenn unter 0.5 %, CTA und Offer überarbeiten

**Mittelfristig (1–3 Monate)**
- Multi-Touch-Attribution einrichten (HubSpot Attribution Reports oder Looker Studio mit CRM-Verbindung)
- Content-ROI-Berechnung je Asset als quartalsweisen Standard einführen
- MOFU-Gap schliessen: Mindestens zwei neue Assets für die häufigsten ICP-Einwände produzieren
- Case Studies für Top-3-ICP-Segmente strukturiert aufbauen — mit konkreten Kennzahlen und Branchen-Kontext

**Strategisch (3–12 Monate)**
- Content-Produktion vollständig attributions-gesteuert: Jedes neue Asset muss eine Pipeline-Hypothese haben
- Content-Cluster-Strategie implementieren: Thematische Autorität in 3–4 Kernthemen aufbauen statt Content-Streuung
- Sales-Content-Bibliothek aufbauen: Battle Cards, Proposal Templates, Einwand-Guides — nach Segment und Stage
- Content-Performance-Dashboard als Standard im monatlichen Marketing-Review verankern

## Performanceboost Perspektive

Das Hauptproblem bei Content in Schweizer KMUs ist nicht mangelnde Kreativität — es ist fehlende Verbindung. Blogartikel leben in WordPress, Leads im CRM, Deals in einer Excel-Tabelle, und niemand hat je die drei Systeme verbunden. Die Konsequenz: Budgets werden in Content investiert, der Traffic bringt aber keine Pipeline, während die zwei Assets, die tatsächlich Deals beeinflussen, zufällig entstanden sind und nie bewusst skaliert wurden.

Performanceboost trennt Content rigoros in zwei Kategorien: Demand Capture Content (für Menschen, die bereits suchen — SEO, Case Studies, Vergleichsseiten) und Demand Creation Content (für Menschen, die noch nicht suchen — Thought Leadership, Diagnose-Tools, Kategorien-Guides). Beide haben unterschiedliche ROI-Horizonte und sollten nicht mit denselben Metriken gemessen werden. Was wir nicht akzeptieren: Content-Budgets ohne Attribution-Infrastruktur. Wer nicht messen kann, welcher Content zu Deals beiträgt, hat kein Content-Marketing — er hat Content-Produktion als Selbstzweck.
