---
title: "Email-Clients"
icon: material/email-open
description: Diese Email-Clients sind Datenschutzfreundlich und unterstützen OpenPGP Email Verschlüsselung.
cover: email-clients.webp
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-server-network: Diensteanbieter](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-target-account: Gezielte Angriffe](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Die **Email-Clients** die wir empfehlen unterstützen [OpenPGP](encryption.md#openpgp) sowie starke Authentifizierung wie z.B. [Open Authorization (Oauth)](basics/account-creation.md#sign-in-with-oauth). OAuth lässt dich [Multi-Faktor Authentifizierung](basics/multi-factor-authentication.md) nutzen, um Kontendiebstahl zu verhindern.

<details class="warning" markdown>
<summary>Email bietet keinen Forward-Secrecy</summary>

Wenn man Ende-zu-Ende-Verschlüsselung (E2EE) wie OpenPGP benutzt, werden trotzdem [manche Metadaten](basics/email-security.md#email-metadata-overview) im Email-Header nicht verschlüsselt.

OpenPGP unterstützt ebenfalls nicht [Forward-Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), das heißt, wenn der private Schlüssel von dir oder deinem Empfänger gestohlen werden, können alle Nachrichten, die mit dem Schlüssel verschlüsselt waren, preisgeben werden: [Wie beschütze ich meine private Schlüssel?](basics/email-security.md) Wende dich an einem Medium dass Forward-Secrecy unterstützt:

[Echtzeit Kommunikation](real-time-communication.md ""){.md-button}

</details>

## Plattformübergreifend

### Thunderbird

<div class="admonition recommendation" markdown>

![Thunderbird logo](assets/img/email-clients/thunderbird.svg){ align=right }

**Thunderbird** ist ein kostenloser, plattformübergreifender Open-Source-Client für Email, Newsgroup, News Feed und Chat (XMPP, IRC, Matrix) der von der Thunderbird-Community und zuvor von der Mozilla Foundation entwickelt wurde.

[:octicons-home-16: Homepage](https://thunderbird.net){ .md-button .md-button--primary } [:octicons-eye-16:](https://mozilla.org/privacy/thunderbird){ .card-link title="Datenschutzerklärung" } [:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title="Dokumentation" } [:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.thunderbird.android)
- [:simple-github: GitHub](https://github.com/thunderbird/thunderbird-android/releases)
- [:fontawesome-brands-windows: Windows](https://thunderbird.net)
- [:simple-apple: macOS](https://thunderbird.net)
- [:simple-linux: Linux](https://thunderbird.net)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

When replying to someone on a mailing list in Thunderbird Mobile, the "reply" option may also include the mailing list. For more information see [thunderbird/thunderbird-android #3738](https://github.com/thunderbird/thunderbird-android/issues/3738).

</div>

#### Empfohlene Konfiguration

<div class="annotate" markdown>

Wir empfehlen die Änderung dieser Einstellungen, um Thunderbird Desktop mehr Privater zu machen.

Diese Optionen können unter :material-menu: → **Allgemeine Einstellungen** → **Datenschutz** gefunden werden.

##### Web Content

- [ ] Uncheck  **Remember websites and links I've visited**
- [ ] Uncheck  **Accept cookies from sites** (1)

</div>

1. You may need to keep this setting checked when you're logging in to some providers such as Gmail, or via an institution’s SSO. You should uncheck it once you log in successfully.

##### Telemetry

- [ ] Uncheck  **Allow Thunderbird to send technical and interaction data to Mozilla**

#### Thunderbird-user.js (advanced)

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js) is a set of configuration options that aims to disable as many of the web-browsing features within Thunderbird Desktop as possible in order to reduce attack surface and maintain privacy. Some of the changes are backported from the [Arkenfox project](desktop-browsers.md#arkenfox-advanced).

## Platform Specific

### Apple Mail (macOS)

<div class="admonition recommendation" markdown>

![Apple Mail logo](assets/img/email-clients/applemail.png){ align=right }

**Apple Mail** is included in macOS and can be extended to have OpenPGP support with [GPG Suite](encryption.md#gpg-suite), which adds the ability to send PGP-encrypted email.

[:octicons-home-16: Homepage](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/en-ww){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/mail){ .card-link title=Documentation}

</details>

</div>

<div class="admonition info" markdown>
<p class="admonition-title">For those using macOS Sonoma</p>

Currently, GPG Suite does [not yet](https://gpgtools.com/sonoma) have a stable release for macOS Sonoma.

</div>

Apple Mail has the ability to load remote content in the background or block it entirely and hide your IP address from senders on [macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) and [iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios).

### FairEmail (Android)

<div class="admonition recommendation" markdown>

![FairEmail logo](assets/img/email-clients/fairemail.svg){ align=right }

**FairEmail** is a minimal, open-source email app which uses open standards (IMAP, SMTP, OpenPGP) and minimizes data and battery usage.

[:octicons-home-16: Homepage](https://email.faircode.eu){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="Source Code" }
[:octicons-heart-16:](https://email.faircode.eu/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
- [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

</details>

</div>

### GNOME Evolution (GNOME)

<div class="admonition recommendation" markdown>

![Evolution logo](assets/img/email-clients/evolution.svg){ align=right }

**Evolution** is a personal information management application that provides integrated mail, calendaring, and address book functionality. Evolution has extensive [documentation](https://gnome.pages.gitlab.gnome.org/evolution/help) to help you get started.

[:octicons-home-16: Homepage](https://gitlab.gnome.org/GNOME/evolution/-/wikis/home){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.gnome.org/GNOME/evolution/-/wikis/Privacy-Policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://gnome.pages.gitlab.gnome.org/evolution/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution){ .card-link title="Source Code" }
[:octicons-heart-16:](https://gnome.org/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

</details>

</div>

### Kontact (KDE)

<div class="admonition recommendation" markdown>

![Kontact logo](assets/img/email-clients/kontact.svg){ align=right }

**Kontact** is a personal information manager (PIM) application from the [KDE](https://kde.org) project. It provides a mail client, address book, RSS client, and an organizer.

[:octicons-home-16: Homepage](https://kontact.kde.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kontact.kde.org/users){ .card-link title="Documentation" }
[:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kde.org/community/donations){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-linux: Linux](https://kontact.kde.org/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

</details>

</div>

### Mailvelope (Browser)

<div class="admonition recommendation" markdown>

![Mailvelope logo](assets/img/email-clients/mailvelope.svg){ align=right }

**Mailvelope** is a browser extension that enables the exchange of encrypted emails following the OpenPGP encryption standard.

[:octicons-home-16: Homepage](https://mailvelope.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailvelope.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mailvelope.com/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

</details>

</div>

### NeoMutt (CLI)

<div class="admonition recommendation" markdown>

![NeoMutt logo](assets/img/email-clients/mutt.svg){ align=right }

**NeoMutt** is an open-source command line email reader for Linux and BSD. It's a fork of [Mutt](https://en.wikipedia.org/wiki/Mutt_(email_client)) with added features.

NeoMutt is a text-based client that has a steep learning curve. It is, however, very customizable.

[:octicons-home-16: Homepage](https://neomutt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://neomutt.org/guide){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="Source Code" }
[:octicons-heart-16:](https://paypal.com/paypalme/russon){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: macOS](https://neomutt.org/distro)
- [:simple-linux: Linux](https://neomutt.org/distro)

</details>

</div>

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

### Mindestanforderungen

- Apps developed for open-source operating systems must be open source.
- Must not collect telemetry, or have an easy way to disable all telemetry.
- Must support OpenPGP message encryption.

### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Merkmale, aber diejenigen, die sie enthalten, werden möglicherweise höher eingestuft als andere auf dieser Seite.

- Should be open source.
- Should be cross-platform.
- Should not collect any telemetry by default.
- Should support OpenPGP natively, i.e. without extensions.
- Should support storing OpenPGP encrypted emails locally.
