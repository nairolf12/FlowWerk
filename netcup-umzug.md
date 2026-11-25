# flow-werk.de bei netcup (Umzug 25.11.2026)

Ersetzt alle Angaben zu „GitHub Pages" und „IONOS" in `website-stand.md`.

## Stand

- **Domain und Website liegen bei netcup**, Webhosting 1000 NUE (Hosting256805,
  a9829), Standort Nürnberg. `flow-werk.de` ist die Inklusiv-Domain des Pakets.
  Der Inklusiv-Slot ist damit belegt — nicht für eine andere Domain verwenden.
- Domain per Auth-Code von IONOS umgezogen. DNS über netcup **CloudDNS**
  (Nameserver `netcup.firstns.cc` usw.). DNSSEC noch aus.
- Webserver `a9829.netcup.net`, IPv4 `159.195.152.41`, IPv6
  `2a03:4000:6d:427f::25:6805`. Mailserver `mx982b.netcup.net` / `mail.flow-werk.de`
  (`159.195.152.43`).
- Let's Encrypt für `flow-werk.de` + `www` (HTTP-Validierung). **Kein Wildcard** —
  das braucht einen `_acme-challenge`-TXT-Eintrag, den Plesk bei CloudDNS nicht
  selbst setzen kann.
- Postfach `info@flow-werk.de` bei netcup (WCP/Plesk, „Auto-Login MAIL").
- AV-Vertrag mit netcup abgeschlossen (Besucher, Kunden, Interessenten,
  Lieferanten; Namen, Kontakt, Verkehrs- und Vertragsdaten, E-Mail-Inhalte;
  keine besonderen Kategorien).
- Getestet am 25.11.: HTTPS, Weiterleitungen, 404-Seite, Downloads, Mail ein/aus.

## DNS-Zone (CloudDNS)

Website: `@` A/AAAA auf den Webserver, `www` CNAME `flow-werk.de`, dazu netcups
Standard `*` A/AAAA, `mail`, `autoconfig`, `db`.
Mail: `@` MX 10 `mail.flow-werk.de` und MX 50 `mx982b.netcup.net` (doppelt,
harmlos), SPF `v=spf1 mx a include:_spf.webhosting.systems ~all`,
`key1`/`key2._domainkey` CNAME auf `….webhosting.systems`,
`_dmarc` `v=DMARC1; p=none; rua=mailto:info@flow-werk.de`.
**Resend** (Versanddienst, Konto „vereine_spassvogel_6d"): `resend._domainkey`
TXT, `send` MX `feedback-smtp.eu-west-1.amazonses.com`, `send` TXT
`v=spf1 include:amazonses.com ~all`. Domain dort verifiziert.

## Dateien auf dem Server

Webroot `httpdocs`. Inhalt = Repo ohne `CNAME`, `README.md`, `CHANGELOG.md`.
Installer liegen direkt in `httpdocs/downloads/`, nicht mehr im Repo nötig.

`.htaccess` (neu, lokal mit Apache getestet): alles auf `https://flow-werk.de`
ohne www (301), `finflow.html` → `sumflow.html` (301), `ErrorDocument 404`,
Punktdateien gesperrt, kein Verzeichnislisting, `.dmg`/`.exe` als Download,
Caching (woff2 1 Jahr, Bilder 1 Monat, HTML 0), Sicherheits-Header inkl. HSTS
1 Jahr.

`404.html` nutzt jetzt absolute Pfade (`/fonts/…`, `/favicon.svg`), sonst fehlt
in Unterordnern die Schrift. Beide Datenschutzerklärungen nennen netcup
(Karlsruhe, Server Nürnberg, Logfiles, AV-Vertrag, Mail bei netcup) statt GitHub.

Veröffentlichen ab jetzt: geänderte Dateien per SFTP oder WCP-Dateimanager nach
`httpdocs`. Kein Auto-Deploy mehr per `git push`. Optional später: GitHub Action
mit SSH-Upload.

## Offen

- Alte Mails aus dem IONOS-Postfach per IMAP ins netcup-Postfach ziehen.
- GitHub Pages abschalten: Settings › Pages Custom Domain entfernen, `CNAME`
  löschen. `.htaccess`, `404.html` und beide Datenschutzerklärungen ins Repo.
- IONOS-Vertrag kündigen, erst wenn im alten Postfach nichts mehr ankommt.
- Datenschutzerklärung: Resend fehlt. Ergänzen, sobald klar ist, wofür Resend
  genutzt wird (z. B. Versand der Lizenzschlüssel).
- Nach ein paar stabilen Tagen: DNSSEC im CCP einschalten.
- Resend „Move to Forge" erst danach angehen.
- Verkaufsargument für `websites.html`: Die eigene Seite liegt jetzt selbst bei
  einem deutschen Anbieter — passt zum Hosting-Modell für Kunden.
