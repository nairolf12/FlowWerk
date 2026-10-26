# flow-werk.de – Website-Changelog

Änderungen an der Website selbst (Design, Struktur, Deployment). Die
funktionalen Änderungen der Software finFlow stehen ausschließlich in
`changelog.html`.

---

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
