# flow-werk.de – Website-Changelog

Änderungen an der Website selbst (Design, Struktur, Deployment). Die
funktionalen Änderungen der Software sumFlow stehen ausschließlich in
`changelog.html`.

---

## 2026-11-13 (3)

- `links.html` auf denselben variablen Schriftschnitt umgestellt wie die
  übrigen Seiten. Die drei statischen Dateien `fonts/manrope-latin-400-`,
  `-600-` und `-700-normal.woff2` werden nicht mehr gebraucht und müssen im
  Repo gelöscht werden — das Entpacken des Pakets entfernt sie nicht
- Im Ordner `fonts/` liegen damit genau zwei Schriftdateien und der Lizenztext

## 2026-11-13 (2)

- **Schriftart lokal eingebunden.** Manrope lag bisher bei Google Fonts; bei
  jedem Seitenaufruf ging die IP-Adresse der Besucher dorthin. Jetzt liefert
  der eigene Server die Schrift aus (`fonts/`, variabler woff2-Schnitt für die
  Strichstärken 200–800, SIL Open Font License). Betrifft alle acht Seiten;
  die `preconnect`- und Stylesheet-Verweise auf fonts.googleapis.com und
  fonts.gstatic.com sind ersatzlos entfallen
- Beide Datenschutzerklärungen: Absatz zur Schriftauslieferung ergänzt. Die
  Aussage „keine eingebetteten Drittdienste" stimmt damit jetzt auch

## 2026-11-13

- Neue Seite `websites.html`: Website-Erstellung als eigene Dienstleistung —
  Leistungen (Neubau, Überarbeitung, Pflege und Hosting), Arbeitsweise, Ablauf
  in vier Schritten, ein Abschnitt „wofür ich der Richtige bin und wofür nicht",
  Preise auf Anfrage, Kontakt per E-Mail mit vorbereitetem Betreff
- Startseite: neuer Abschnitt `#websites` unter dem Produktraster mit Verweis
  auf die neue Seite, dazu Einträge in Navigation und Fußzeile
- Startseite: Meta-Description erweitert, `knowsAbout` und `makesOffer` in den
  strukturierten Daten ergänzt
- `sitemap.xml` um `websites.html` erweitert

## 2026-11-11

- Beide Produkt-Screenshots gegen Aufnahmen aus sumFlow 3.7.0 getauscht
  (`screenshot-dashboard.png`, `screenshot-belege.png`)
- Kundennamen in beiden Screenshots durch Musternamen ersetzt, Kennzahlen
  im Dashboard durch Musterwerte — passend zur Mini-Vorschau in Kachel 01
  (Offen 2.430 €, Überfällig 480 €, Umsatz 11.840 €)

## 2026-11-06

- **Produkt umbenannt: finFlow heißt ab Version 3.7.0 sumFlow.** Alle Seiten,
  Titel, Meta-Angaben, strukturierten Daten und Schriftzüge umgestellt
- Produktseite liegt jetzt unter `sumflow.html`; unter `finflow.html` steht
  eine Weiterleitungsseite (Meta-Refresh, JavaScript und `canonical` auf die
  neue Adresse), damit alte Links und Lesezeichen weiter funktionieren
- `changelog.html`: Eintrag zu 3.7.0 ergänzt, Badge verschoben; Einträge bis
  3.6.2.2 nennen weiterhin finFlow, weil sie unter diesem Namen erschienen
  sind — dazu ein Hinweis unter der Überschrift
- `sumflow.html`: Version 3.7.0, Downloadpfade auf `sumFlow-Installer-3.7.0.dmg`
  und `sumFlow-Setup-3.7.0.exe`, `softwareVersion` und `datePublished` im
  JSON-LD nachgezogen
- `sitemap.xml` auf die neue Adresse umgestellt

## 2026-10-26

- `finflow.html`: Versionsbadge, Downloadlinks und strukturierte Daten auf
  finFlow 3.6.2.2 aktualisiert
- `changelog.html`: Versionen 3.6.2, 3.6.2.1 und 3.6.2.2 nachgetragen
- Suchmaschinen-Grundlagen ergänzt: `canonical`-Tags auf allen indexierbaren
  Seiten, `lastmod` in der Sitemap, fehlende Meta-Descriptions nachgetragen
- Strukturierte Daten als JSON-LD: `Organization` + `WebSite` auf der
  Startseite, `SoftwareApplication` (inkl. Preis und Systemvoraussetzungen)
  auf der finFlow-Seite
- `finflow.html`: Open-Graph- und Favicon-Angaben ergänzt (fehlten dort)
- `404.html`: auf `noindex` gesetzt
- **Impressum korrigiert**: Die Straße war in `finflow.html` zweimal als
  „Haldestraße" statt „Haldenstraße" hinterlegt (`pubStreet` und
  Muster-Widerrufsformular) — betraf Impressum, Datenschutzhinweis und AGB
  auf der Produktseite
- `index.html`: `og:image` auf absolute URL umgestellt (relative Pfade werden
  von manchen Diensten beim Teilen nicht aufgelöst), Bildmaße ergänzt
- Neues `logo-512.png` (quadratisches Primärlogo) als `logo` in den
  strukturierten Daten statt des 1200×630-Banners
- Produktabschnitt: Das nachgebaute Fenster „Rechnungsübersicht" ist entfernt —
  diese Ansicht gibt es in finFlow nicht. An seiner Stelle steht jetzt ein
  echter Screenshot der Ansicht „Belege & E-Rechnungen"
  (`screenshot-belege.png`), das zugehörige Attrappen-CSS wurde entfernt
- JSON-LD: beide Screenshots als `screenshot` hinterlegt
- `screenshot-dashboard.png` erneuert: zeigt jetzt die Oberfläche nach dem
  Rebrand. Die Kundennamen sind durch Musterdaten ersetzt (auf einer
  öffentlichen Seite haben echte Kundennamen nichts verloren), die
  macOS-Titelleiste ist abgeschnitten, weil die Seite einen eigenen
  Fensterrahmen zeichnet

## 2026-09-22 (2)

- Startseite neu gestaltet: Glasoberflächen, cursorgeführte Lichtreflexe und
  3D-Neigung auf den Produktkarten, animiertes Wellen-Logo, Scroll-Reveals
- Startseite um zwei Abschnitte ergänzt: Markensektion mit den vier CI-Werten
  und ein Kontaktabschluss
- `finflow.html` und `changelog.html` auf dieselbe Designsprache gehoben,
  Footer dort auf Graphite Navy umgestellt
- Datenschutzseiten: seitliches Scrollen auf schmalen Bildschirmen behoben

## 2026-09-22

- Website auf die neue flowWerk Corporate Identity umgestellt: Farben,
  Wellen-Logo, Manrope-Schrift und Layout auf allen Seiten (`index.html`,
  `finflow.html`, `changelog.html`, `404.html`, `datenschutz.html`,
  `datenschutz-flowwerk.html`) erneuert
- `favicon.svg` und `og-image.png` neu erstellt (neues Logo/CI)
- Ungenutzte alte Logo-Assets (`assets_*.png`) entfernt
- `finflow.html`: Versionsbadge und Downloadlinks auf 3.6.1 aktualisiert
- `changelog.html`: fehlende Versionen 3.5.1–3.6.1 nachgetragen
