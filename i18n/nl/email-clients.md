---
title: "Email clients"
icon: material/email-open
description: These email clients are privacy-respecting and support OpenPGP email encryption.
cover: email-clients.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Dienstverleners](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-target-account: Gerichte aanvallen](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

The **email clients** we recommend support both [OpenPGP](encryption.md#openpgp) and strong authentication such as [Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth). OAuth allows you to use [Multi-Factor Authentication](basics/multi-factor-authentication.md) to prevent account theft.

<details class="warning" markdown>
<summary>Email does not provide forward secrecy</summary>

When using end-to-end encryption (E2EE) technology like OpenPGP, email will still have [some metadata](basics/email-security.md#email-metadata-overview) that is not encrypted in the header of the email.

OpenPGP also does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed: [How do I protect my private keys?](basics/email-security.md) Consider using a medium that provides forward secrecy:

[Real-time Communication](real-time-communication.md ""){.md-button}

</details>

## Cross-Platform

### Thunderbird

<div class="admonition recommendation" markdown>

![Thunderbird logo](assets/img/email-clients/thunderbird.svg){ align=right }

**Thunderbird** is a free, open-source, cross-platform email, newsgroup, news feed, and chat (XMPP, IRC, Matrix) client developed by the Thunderbird community, and previously by the Mozilla Foundation.

[:octicons-home-16: Homepage](https://thunderbird.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/thunderbird){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title="Documentation" }
[:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://thunderbird.net)
- [:simple-apple: macOS](https://thunderbird.net)
- [:simple-linux: Linux](https://thunderbird.net)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

</details>

</div>

#### Aanbevolen configuratie

We raden aan om sommige van deze instellingen te wijzigen om Thunderbird een beetje meer privé te maken.

Deze opties zijn te vinden in :material-menu: → **Instellingen** → **Privacy & Beveiliging**.

##### Web Content

- [ ] Deselecteer  **Onthoud websites en links die ik heb bezocht**
- [ ] Deselecteer  **Accepteer cookies van sites**

##### Telemetrie

- [ ] Deselecteer  **Toestaan dat Thunderbird technische en interactiegegevens naar Mozilla stuurt**

#### Thunderbird-user.js (geavanceerd)

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js) is a set of configuration options that aims to disable as many of the web-browsing features within Thunderbird as possible in order to reduce attack surface and maintain privacy. Some of the changes are backported from the [Arkenfox project](desktop-browsers.md#arkenfox-advanced).

## Platform specifiek

### Apple Mail (macOS)

<div class="admonition recommendation" markdown>

![Apple Mail-logo](assets/img/email-clients/applemail.png){ align=right }

**Apple Mail** is opgenomen in macOS en kan worden uitgebreid met OpenPGP-ondersteuning met [GPG Suite](/encryption/#gpg-suite), waarmee de mogelijkheid wordt toegevoegd om versleutelde e-mail te versturen.

[:octicons-home-16: Homepage](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/en-ww){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/mail){ .card-link title=Documentation}

</details>

</div>

Apple Mail heeft de mogelijkheid om inhoud op afstand op de achtergrond te laden of volledig te blokkeren en jouw IP-adres te verbergen voor afzenders op [macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) en [iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios).

### Canary Mail (iOS)

<div class="admonition recommendation" markdown>

![Canary Mail-logo](assets/img/email-clients/canarymail.svg){ align=right }

**Canary Mail** is een betaalde e-mailclient die is ontworpen om end-to-end versleuteling naadloos te laten verlopen met beveiligingsfuncties zoals een biometrische app-vergrendeling.

[:octicons-home-16: Homepage](https://canarymail.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://canarymail.io/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://canarymail.io/help){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.canarymail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1155470386)
- [:fontawesome-brands-windows: Windows](https://canarymail.io/downloads.html)
- [:simple-apple: macOS](https://apps.apple.com/app/id1236045954)

</details>

</div>

<details class="warning" markdown>
<summary>Warning</summary>

Canary Mail heeft pas onlangs een Windows- en Android-client uitgebracht, hoewel die volgens ons niet zo stabiel zijn als hun iOS- en Mac-tegenhangers.

</details>

Canary Mail is closed-source. We raden het aan omdat er maar weinig keuzes zijn voor e-mailclients op iOS die PGP E2EE ondersteunen.

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

### Gnome evolutie (Gnome)

<div class="admonition recommendation" markdown>

![Evolution logo](assets/img/email-clients/evolution.svg){ align=right }

**Evolution** is een applicatie voor het beheer van persoonlijke informatie die geïntegreerde mail-, agenda- en adresboekfuncties biedt. Evolution has extensive [documentation](https://help.gnome.org/users/evolution/stable) to help you get started.

[:octicons-home-16: Homepage](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
[:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.gnome.org/users/evolution/stable){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution){ .card-link title="Source Code" }
[:octicons-heart-16:](https://gnome.org/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

</details>

</div>

### K-9 Mail (Android)

<div class="admonition recommendation" markdown>

![K-9 Mail logo](assets/img/email-clients/k9mail.svg){ align=right }

**K-9 Mail** is een onafhankelijke mail-applicatie die zowel POP3 als IMAP mailboxen ondersteunt, maar alleen push mail voor IMAP ondersteunt.

In de toekomst zal K-9 Mail de [officieel gemerkte](https://k9mail.app/2022/06/13/K-9-Mail-and-Thunderbird.html) Thunderbird client voor Android zijn.

[:octicons-home-16: Homepage](https://k9mail.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://k9mail.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.k9mail.app){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/thundernest/k-9){ .card-link title="Source Code" }
[:octicons-heart-16:](https://k9mail.app/contribute){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
- [:simple-github: GitHub](https://github.com/thundernest/k-9/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When replying to someone on a mailing list, the "reply" option may also include the mailing list. Zie voor meer informatie [thundernest/k-9 #3738](https://github.com/thundernest/k-9/issues/3738).

</div>

### Kontact (KDE)

<div class="admonition recommendation" markdown>

![Kontact logo](assets/img/email-clients/kontact.svg){ align=right }

**Kontact** is een persoonlijke informatiemanager (PIM) applicatie van het [KDE](https://kde.org) project. It provides a mail client, address book, RSS client, and an organizer.

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

**Mailvelope** is een browser extensie die de uitwisseling van versleutelde e-mails mogelijk maakt volgens de OpenPGP encryptie standaard.

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

**NeoMutt** is an open-source command line email reader for Linux and BSD. Het is een vork van [Mutt](https://en.wikipedia.org/wiki/Mutt_(email_client)) met toegevoegde mogelijkheden.

NeoMutt is een tekst-gebaseerde client die een steile leercurve heeft. It is, however, very customizable.

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

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

### Minimum kwalificaties

- Apps developed for open-source operating systems must be open source.
- Mag geen telemetrie verzamelen, of een gemakkelijke manier hebben om alle telemetrie uit te schakelen.
- Moet OpenPGP-berichtversleuteling ondersteunen.

### Beste geval

Onze best-case criteria geven aan wat wij zouden willen zien van het perfecte project in deze categorie. Het is mogelijk dat onze aanbevelingen geen of niet alle functies bevatten, maar degene die dat wel doen kunnen hoger gerangschikt worden dan andere op deze pagina.

- Should be open source.
- Moet cross-platform zijn.
- Verzamelt standaard geen telemetrie.
- Moet OpenPGP native ondersteunen, dat wil zeggen zonder extensies.
- Moet ondersteuning bieden voor het lokaal opslaan van OpenPGP-versleutelde e-mails.
