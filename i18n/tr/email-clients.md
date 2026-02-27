---
title: "E-posta İstemcileri"
icon: material/email-open
description: Bu e-posta istemcileri gizliliğinize saygı duyar ve OpenPGP e-posta şifrelemesini destekler.
cover: email-clients.webp
---

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-server-network: Hizmet Sunucular](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-target-account: Hedefli Saldırılar](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Önerdiğimiz **e-posta istemcileri** hem [OpenPGP'yi](encryption.md#openpgp) hem de [Açık Kimlik Doğrulamayı (OAuth)](basics/account-creation.md#sign-in-with-oauth) destekler. OAuth, hesap çalınmalarına karşı [Çok Aşamalı Kimlik Doğrulaması](basics/multi-factor-authentication.md) kullanmanıza olanak tanır.

<details class="warning" markdown>
<summary>E-posta ileriye dönük gizlilik sağlamaz</summary>

OpenPGP gibi bir uçtan uca şifreleme (E2EE) teknolojisi kullanıldığında, e-postaların başlık kısmında şifrelenmemiş [bazı metaveriler](basics/email-security.md#email-metadata-overview) bulunmaya devam edecektir.

OpenPGP de [ileriye dönük gizliliği](https://tr.wikipedia.org/wiki/İleri_gizlilik) desteklemez. Sizin veya alıcının özel anahtarı herhangi bir zamanda ele geçirilirse, önceden o anahtarla şifrelenmiş tüm mesajlar açığa çıkacaktır: [Özel anahtarlarımı nasıl koruyabilirim?](basics/email-security.md) İleriye dönük gizlilik sağlayan bir iletişim ortamı kullanmayı düşünün:

[Gerçek Zamanlı İletişim](real-time-communication.md ""){.md-button}

</details>

## Çok Platformlu

### Thunderbird

<div class="admonition recommendation" markdown>

![Thunderbird logo](assets/img/email-clients/thunderbird.svg){ align=right }

**Thunderbird**, günümüzde Thunderbird topluluğu tarafından, daha önce de Mozilla Vakfı tarafından geliştirilen, özgür, açık kaynaklı, çok platformlu bir e-posta, haber grubu, RSS akışı ve sohbet (XMPP, IRC, Matrix) istemcisidir.

[:octicons-home-16: Ana Sayfa](https://thunderbird.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/thunderbird){ .card-link title="Gizlilik Politikası" }
[:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title="Dokümantasyon" }
[:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Kaynak Kodu" }

<details class="downloads" markdown>
<summary>İndirmeler</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.thunderbird.android)
- [:simple-github: GitHub](https://github.com/thunderbird/thunderbird-android/releases)
- [:fontawesome-brands-windows: Windows](https://thunderbird.net)
- [:simple-apple: macOS](https://thunderbird.net)
- [:simple-linux: Linux](https://thunderbird.net)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Uyarı</p>

Thunderbird mobil uygulamasında bir e-posta listesindeki birisine yanıt verirken, "Yanıtla" seçeneği e-posta listesini de içerebilir. Daha fazla bilgi için [thunderbird/thunderbird-android #3738](https://github.com/thunderbird/thunderbird-android/issues/3738).

</div>

#### Önerilen Yapılandırma

<div class="annotate" markdown>

Thunderbird masaüstü uygulamasını biraz daha gizlilik dostu hâle getirmek için bazı ayarları değiştirmenizi öneririz.

Bu seçenekler :material-menu: → **Ayarlar** → Gizlilik ve Güvenlik sekmesinden bulunabilir.

##### Web İçeriği

- [ ] **Ziyaret ettiğim bağlantıları ve web sitelerini hatırla** seçeneğini kapatın.
- [ ] **Web sitelerinden çerezlere izin ver** seçeneğini kapatın (1)

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

## Kriter

**Lütfen önerdiğimiz projelerin hiçbirine bağlı olmadığımızı unutmayın.** [standart kriterlerimize](about/criteria.md) ek olarak, objektif tavsiyelerde bulunabilmemiz için bir takım gereklilikler geliştirdik. Bir projeyi kullanmayı seçmeden önce bu listeye aşina olmanızı ve sizin için doğru seçim olduğundan emin olmak için kendi araştırmanızı yapmanızı öneririz.

### Asgari Nitelikler

- Apps developed for open-source operating systems must be open source.
- Must not collect telemetry, or have an easy way to disable all telemetry.
- Must support OpenPGP message encryption.

### En İyi Durum

En iyi durum kriterlerimiz, bu kategorideki mükemmel bir projede görmek istediklerimizi temsil etmektedir. Önerilerimiz bu işlevlerden herhangi birini veya tamamını içermeyebilir, ancak içerenler bu sayfada diğerlerinden daha üst sıralarda yer alabilir.

- Should be open source.
- Should be cross-platform.
- Should not collect any telemetry by default.
- Should support OpenPGP natively, i.e. without extensions.
- Should support storing OpenPGP encrypted emails locally.
