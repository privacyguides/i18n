---
title: "Client Email"
icon: material/email-open
description: Questi client di posta elettronica rispettano la privacy e supportano la crittografia OpenPGP.
cover: email-clients.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Fornitori di Servizi](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-target-account: Attacchi Mirati](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

The **email clients** we recommend support both [OpenPGP](encryption.md#openpgp) and strong authentication such as [Open Authorization (OAuth)](basics/account-creation.md#sign-in-with-oauth). OAuth allows you to use [Multi-Factor Authentication](basics/multi-factor-authentication.md) to prevent account theft.

<details class="warning" markdown>
<summary>L'email non fornisce la forward secrecy</summary>

When using end-to-end encryption (E2EE) technology like OpenPGP, email will still have [some metadata](basics/email-security.md#email-metadata-overview) that is not encrypted in the header of the email.

OpenPGP non supporta inoltre la [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), il che significa che se la tua chiave privata o quella del destinatario viene rubata, tutti i messaggi precedenti crittografati con essa saranno esposti: [Come posso proteggere le mie chiavi private?](basics/email-security.md) Considera la possibilità di utilizzare un mezzo di comunicazione che garantisca la forward secrecy:

[Comunicazione in tempo reale](real-time-communication.md ""){.md-button}

</details>

## Multipiattaforma

### Thunderbird

<div class="admonition recommendation" markdown>

![Logo Thunderbird](assets/img/email-clients/thunderbird.svg){ align=right }

**Thunderbird** è un client di posta elettronica, newsgroup, news feed e chat (XMPP, IRC, Matrix) gratuito, open-source e multipiattaforma, sviluppato dalla communityThunderbird e precedentemente dalla Mozilla Foundation.

[:octicons-home-16: Homepage](https://thunderbird.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/thunderbird){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title="Documentation" }
[:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Source Code" }

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
<p class="admonition-title">Avviso</p>

When replying to someone on a mailing list in Thunderbird Mobile, the "reply" option may also include the mailing list. For more information see [thunderbird/thunderbird-android #3738](https://github.com/thunderbird/thunderbird-android/issues/3738).

</div>

#### Configurazione consigliata

<div class="annotate" markdown>

We recommend changing some of these settings to make Thunderbird Desktop a little more private.

These options can be found in :material-menu: → **Settings** → **Privacy & Security**.

##### Web Content

- [ ] Uncheck  **Remember websites and links I've visited**
- [ ] Uncheck  **Accept cookies from sites** (1)

</div>

1. You may need to keep this setting checked when you're logging in to some providers such as Gmail, or via an institution’s SSO. You should uncheck it once you log in successfully.

##### Telemetry

- [ ] Uncheck  **Allow Thunderbird to send technical and interaction data to Mozilla**

#### Thunderbird-user.js (avanzato)

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js) is a set of configuration options that aims to disable as many of the web-browsing features within Thunderbird Desktop as possible in order to reduce attack surface and maintain privacy. Some of the changes are backported from the [Arkenfox project](desktop-browsers.md#arkenfox-advanced).

## Specifiche della Piattaforma

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

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

### Requisiti minimi

- Apps developed for open-source operating systems must be open source.
- Must not collect telemetry, or have an easy way to disable all telemetry.
- Must support OpenPGP message encryption.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Should be open source.
- Should be cross-platform.
- Should not collect any telemetry by default.
- Should support OpenPGP natively, i.e. without extensions.
- Should support storing OpenPGP encrypted emails locally.
