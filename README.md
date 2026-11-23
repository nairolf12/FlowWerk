# flowWerk · Website

Statische Website für sumFlow – gehostet via GitHub Pages unter flow-werk.de

## Dateien
```
index.html              ← Startseite flowWerk
sumflow.html            ← Produktseite sumFlow (finflow.html leitet hierher)
beispiele/              ← Beispiel-PDFs als Bilder für sumflow.html
changelog.html          ← Versionshistorie (gestylt)
datenschutz.html        ← Datenschutzerklärung
404.html                ← Fehlerseite
favicon.svg             ← Browser-Icon
og-image.png            ← Social-Media-Vorschaubild
robots.txt              ← Crawler-Steuerung
sitemap.xml             ← SEO-Sitemap
CNAME                   ← flow-werk.de
CHANGELOG.md            ← Website-Changelog (nicht der Produkt-Changelog)
downloads/              ← Installer
```

## Neue Version veröffentlichen
1. Installer nach `downloads/` hochladen, dabei mit Versionsnummer benennen:
   `sumFlow-Installer-X.Y.Z.dmg` und `sumFlow-Setup-X.Y.Z.exe`
   (die Build-Skripte erzeugen sie ohne Nummer). Alte Installer löschen
2. In `sumflow.html` den `V`-Block anpassen (v, date, dlMac, dlWin) **und**
   `softwareVersion` / `datePublished` im JSON-LD
3. `changelog.html` ergänzen (Text wortgleich aus der `CHANGELOG.md` des
   App-Projekts), Badge „Aktuelle Version" auf den neuen Eintrag verschieben
4. `lastmod` in `sitemap.xml` für die geänderten Seiten setzen
5. Committen → GitHub Pages deployt automatisch

## Sales Button aktivieren/deaktivieren
1. In `sumflow.html`: `const SALES_ENABLED=false;` auf `true` setzen
2. Im JSON-LD `availability` von `OutOfStock` auf `InStock` ändern
3. Committen

## Kontakt
info@flow-werk.de · flow-werk.de · flowWerk · Florian Haußmann
