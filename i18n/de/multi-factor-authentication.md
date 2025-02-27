---
title: "Multifactor Authentication"
icon: 'material/two-factor-authentication'
description: These tools assist you with securing your internet accounts with Multifactor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">Hardware Schlüssel</p>

[Hardware-Sicherheitsschlüssel-Empfehlungen](security-keys.md) wurden in eine eigene Kategorie verschoben.

</div>

**Multifactor Authentication Apps** implement a security standard adopted by the Internet Engineering Task Force (IETF) called **Time-based One-time Passwords**, or **TOTP**. Bei dieser Methode teilen Websites ein Geheimnis mit dir, das von deiner Authentifizierungs-App verwendet wird, um einen sechsstelligen Code (in der Regel) auf der Grundlage der aktuellen Uhrzeit zu generieren, den du bei der Anmeldung auf der Website zur Überprüfung eingibst. Typically, these codes are regenerated every 30 seconds, and once a new code is generated the old one becomes useless. Selbst wenn ein Hacker einen sechsstelligen Code erhält, gibt es für ihn keine Möglichkeit, diesen Code umzukehren, um das ursprüngliche Geheimnis zu erfahren, oder auf andere Weise vorherzusagen, wie zukünftige Codes aussehen könnten.

Wir empfehlen dir dringend, mobile TOTP-Apps anstelle von Desktop-Alternativen zu verwenden, da Android und iOS eine bessere Sicherheit und App-Isolierung bieten als die meisten Desktop-Betriebssysteme.

## Ente Auth

<div class="admonition recommendation" markdown>

![Ente Auth Logo](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**Ente Auth** ist eine kostenlose und quelloffene Anwendung, die TOTP-Tokens speichert und erzeugt. It can be used with an online account to back up and sync your tokens across your devices (and access them via a web interface) in a secure, end-to-end encrypted fashion. Sie kann auch offline auf einem einzigen Gerät genutzt werden, ohne dass ein Konto erforderlich ist.

[:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://help.ente.io/auth){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

## Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Aegis-Logo](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** ist eine kostenlose und quelloffene App für Android zur Verwaltung deiner 2-Schritt-Verifizierungs-Token für deine Online-Dienste. Aegis Authenticator arbeitet vollständig offline/lokal, bietet aber im Gegensatz zu vielen Alternativen die Möglichkeit, deine Token zur Sicherung zu exportieren.

[:octicons-home-16: Homepage](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title=Spenden }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

<!-- markdownlint-disable-next-line -->
## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

- Der Quellcode muss öffentlich zugänglich sein.
- Darf keine Internetverbindung erfordern.
- Die Cloud-Synchronisierung muss optional sein, und (falls verfügbar) muss die Synchronisierungsfunktion E2EE sein.
