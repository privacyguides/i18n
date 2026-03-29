---
title: Fotoverwaltung
icon: material/image
description: Diese Fotoverwaltungs-Tools schützen deine persönlichen Fotos vor den neugierigen Blicken von Cloud-Speicheranbietern und anderen Unbefugten.
cover: photo-management.webp
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-bug-outline: Passive Angriffe](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: Dienstanbieter](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

Die meisten Cloud **Fotoverwaltungslösungen** wie Google Fotos, Flickr, und Amazon Fotos schützen nicht deine Fotos vom Anbieter selbst. Diese Optionen behalten deine persönlichen Fotos privat, während du sie trotzdem noch mit deiner Familie und vertrauten Personen teilen kannst.

## Ente Photos

<div class="admonition recommendation" markdown>

![Ente logo](assets/img/photo-management/ente.svg){ align=right }

**Ente Photos** ist ein verschlüsselter end-to-end-Backup-service für Fotos, das automatische Backups auf iOS und Android unterstützt. Ihr Code ist vollständig Open Source auf der Client-seite sowie auch auf der Serverseite. Man kann es ebenfalls [selbst hosten](https://github.com/ente-io/ente/tree/main/server#self-hosting).

Der kostenlose Plan bietet 10 GB Speicher, solange man den Dienst mindestens ein Mal im Jahr benutzt.

[:octicons-home-16: Homepage](https://ente.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ente.com/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=photos)
- [:simple-android: Android](https://ente.com/download)
- [:fontawesome-brands-windows: Windows](https://ente.com/download)
- [:simple-apple: macOS](https://ente.com/download)
- [:simple-linux: Linux](https://ente.com/download)
- [:octicons-browser-16: Web](https://web.ente.io)

</details>

</div>

The server-side source code and infrastructure which underpins Ente Photos underwent an audit by [Cure53](https://ente.com/blog/cern-audit) in October 2025. Previous audits were completed by [Cure53](https://ente.com/blog/cryptography-audit) in March 2023 and by [Fallible](https://ente.com/reports/Fallible-Audit-Report-19-04-2023.pdf) in April 2023.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu [unseren Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir dich mit dieser Liste auseinanderzusetzen bevor du ein Projekt aussuchst, und führe ebenfalls deine eigene Recherche um sicher zu sein, dass du das richtige aussuchst.

### Mindestanforderungen

- Cloud-gehostete Anbieter müssen E2EE durchsetzen.
- Muss einen kostenlosen Plan oder eine Probezeit zum Testen anbieten.
- Muss TOTP oder FIDO2-Multifaktor-Authentifizierung oder Passkey-Logins unterstützen.
- Muss eine Weboberfläche bieten, die grundlegende Dateiverwaltungsfunktionen unterstützt.
- Muss einen einfachen Export aller Dateien/Dokumente ermöglichen.
- Muss Open Source sein.

### Im besten Fall

- Sollte veröffentlichte Überprüfungen von angesehene, unabhängigen Dritten haben.
