# finFlow · Produktwebsite

Statische Website für finFlow – gehostet via GitHub Pages unter flow-werk.de

## Dateien
```
index.html              ← Hauptseite
changelog.html          ← Versionshistorie (gestylt)
datenschutz.html        ← Datenschutzerklärung
404.html                ← Fehlerseite
favicon.svg             ← Browser-Icon
og-image.png            ← Social-Media-Vorschaubild
robots.txt              ← Crawler-Steuerung
sitemap.xml             ← SEO-Sitemap
CNAME                   ← flow-werk.de
CHANGELOG.md            ← Quelldatei für changelog.html
downloads/              ← Installer
```

## Neue Version veröffentlichen
1. Neue Installer in `downloads/` ersetzen
2. `V`-Block in `index.html` aktualisieren (v, dlMac, dlWin, date) (Zeile 313)
3. `CHANGELOG.md` und `changelog.html` aktualisieren
4. Committen → GitHub Pages deployt automatisch

## Sales Button aktivieren/deaktivieren
1. const SALES_ENABLED=false; // <-- auf true setzen, um den Kaufen-Button wieder zu aktivieren (Zeile 611)

## Kontakt
info@flow-werk.de · flow-werk.de · FlowWerk · Florian Haußmann
