---
meta_title: "The Best Password Managers to Protect Your Privacy and Security - Privacy Guides"
title: "Pengelola Kata Sandi"
icon: material/form-textbox-password
description: Password managers allow you to securely store and manage passwords and other credentials.
cover: passwords.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Password Manager Recommendations
    url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Bitwarden
    image: /assets/img/password-management/bitwarden.svg
    url: https://bitwarden.com
    sameAs: https://en.wikipedia.org/wiki/Bitwarden
    applicationCategory: Pengelola Kata Sandi
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: 1Password
    image: /assets/img/password-management/1password.svg
    url: https://1password.com
    sameAs: https://en.wikipedia.org/wiki/1Password
    applicationCategory: Pengelola Kata Sandi
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Proton Pass
    image: /assets/img/password-management/protonpass.svg
    url: https://proton.me/pass
    applicationCategory: Pengelola Kata Sandi
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Psono
    image: /assets/img/password-management/psono.svg
    url: https://psono.com
    applicationCategory: Pengelola Kata Sandi
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassXC
    image: /assets/img/password-management/keepassxc.svg
    url: https://keepassxc.org
    sameAs: https://en.wikipedia.org/wiki/KeePassXC
    applicationCategory: Pengelola Kata Sandi
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassDX
    image: /assets/img/password-management/keepassdx.svg
    url: https://keepassdx.com
    applicationCategory: Pengelola Kata Sandi
    operatingSystem: Android
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: gopass
    image: /assets/img/password-management/gopass.svg
    url: https://gopass.pw
    applicationCategory: Pengelola Kata Sandi
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - FreeBSD
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
---

<small>Protects against the following threat(s):</small>

- [:material-target-account: Serangan Bertarget](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Serangan Pasif](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Penyedia Layanan](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

**Password managers** allow you to securely store and manage passwords and other credentials with the use of a master password.

[Pengantar Kata Sandi :material-arrow-right-drop-circle:](./basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

Pengelola kata sandi bawaan pada perangkat lunak seperti peramban dan sistem operasi terkadang tidak sebaik perangkat lunak pengelola kata sandi khusus. The advantage of a built-in password manager is good integration with the software, but it can often be very simple and lack privacy and security features that standalone offerings have.

Sebagai contoh, pengelola kata sandi di Microsoft Edge sama sekali tidak menawarkan E2EE. Google's password manager has [optional](https://support.google.com/accounts/answer/11350823) E2EE, and [Apple's](https://support.apple.com/HT202303) offers E2EE by default.

</div>

## Aplikasi berbasis cloud

Pengelola kata sandi ini menyinkronkan kata sandi Anda ke server cloud untuk kemudahan akses dari semua perangkat Anda dan keamanan terhadap kehilangan perangkat.

### Bitwarden

<div class="admonition recommendation" markdown>

![Bitwarden logo](assets/img/password-management/bitwarden.svg){ align=right }

**Bitwarden** is a free and open-source password and passkey manager. Ini bertujuan untuk memecahkan masalah manajemen kata sandi untuk individu, tim, dan organisasi bisnis. Bitwarden merupakan salah satu solusi terbaik dan teraman untuk menyimpan semua login dan kata sandi Anda sekaligus menjaganya agar tetap tersinkronisasi dengan mudah di antara semua perangkat Anda.

[:octicons-home-16: Homepage](https://bitwarden.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://bitwarden.com/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1137397744)
- [:simple-github: GitHub](https://github.com/bitwarden/android/releases)
- [:fontawesome-brands-windows: Windows](https://bitwarden.com/download)
- [:simple-apple: macOS](https://bitwarden.com/download)
- [:simple-linux: Linux](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/bitwarden-free-password-m/nngceckbapebfimnlniiiahkandclblb)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)
- [:simple-safari: Safari](https://apps.apple.com/us/app/bitwarden/id1352778147)

</details>

</div>

Bitwarden uses [PBKDF2](https://bitwarden.com/help/kdf-algorithms/#pbkdf2) as its key derivation function (KDF) algorithm by default. It also offers [Argon2](https://bitwarden.com/help/kdf-algorithms/#argon2id), which is more secure, as an alternative. You can change your account's KDF algorithm in the web vault.

- [x] Select **Settings > Security > Keys > KDF algorithm > Argon2id**

Kode sisi server Bitwarden [bersumber terbuka](https://github.com/bitwarden/server), jadi jika Anda tidak ingin menggunakan "awan" Bitwarden, Anda dapat dengan mudah meng-hos server sinkronisasi Bitwarden Anda sendiri.

**Vaultwarden** is an alternative implementation of Bitwarden's sync server written in Rust and compatible with official Bitwarden clients, perfect for self-hosted deployment where running the resource-heavy official service might not be ideal. Jika Anda ingin meng-host Bitwarden di server Anda sendiri, Gunakanlah Vaultwarden dan bukan kode server resmi Bitwarden.

[:octicons-repo-16: Vaultwarden Repository](https://github.com/dani-garcia/vaultwarden ""){.md-button} [:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title="Contribute" }

### Proton Pass

<div class="admonition recommendation" markdown>

![Proton Pass logo](assets/img/password-management/protonpass.svg){ align=right }

**Proton Pass** is an open-source, end-to-end encrypted password manager developed by Proton, the team behind [Proton Mail](email.md#proton-mail). It securely stores your login credentials, generates unique email aliases, and supports and stores passkeys.

[:octicons-home-16: Homepage](https://proton.me/pass){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/pass/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/pass){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/protonpass){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=proton.android.pass)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/proton-pass-password-manager/id6443490629)
- [:fontawesome-brands-windows: Windows](https://proton.me/pass/download)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/proton-pass)
- [:simple-googlechrome: Chrome](https://chromewebstore.google.com/detail/proton-pass-free-password/ghmbeldphafepmbegfdlkpapadhbakde)
- [:fontawesome-brands-edge: Edge](https://chromewebstore.google.com/detail/proton-pass-free-password/ghmbeldphafepmbegfdlkpapadhbakde)
- [:octicons-browser-16: Web](https://pass.proton.me)

</details>

</div>

With the acquisition of SimpleLogin in April 2022, Proton has offered a "hide-my-email" feature that lets you create 10 aliases (free plan) or unlimited aliases (paid plans).

The Proton Pass mobile apps and browser extension underwent an audit performed by Cure53 throughout May and June 2023. The security analysis company concluded:

> Proton Pass apps and components leave a rather positive impression in terms of security.

All issues were addressed and fixed shortly after the [report](https://res.cloudinary.com/dbulfrlrz/images/v1707561557/wp-pme/Cure53-proton-pass-20230717/Cure53-proton-pass-20230717.pdf).

### 1Password

<div class="admonition recommendation" markdown>

![1Password logo](assets/img/password-management/1password.svg){ align=right }

**1Password** is a password manager with a strong focus on security and ease-of-use that allows you to store passwords, passkeys, credit cards, software licenses, and any other sensitive information in a secure digital vault. Your vault is hosted on 1Password's servers for a [monthly fee](https://1password.com/sign-up). 1Password is [audited](https://support.1password.com/security-assessments) on a regular basis and provides exceptional customer support. 1Password memiliki sumber yang tertutup; namun, keamanan produk didokumentasikan secara menyeluruh dalam [laporan resmi keamanan] (https://1passwordstatic.com/files/security/1password-white-paper.pdf) mereka.

[:octicons-home-16: Homepage](https://1password.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://1password.com/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.1password.com){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750)
- [:fontawesome-brands-windows: Windows](https://1password.com/downloads/windows)
- [:simple-apple: macOS](https://1password.com/downloads/mac)
- [:simple-linux: Linux](https://1password.com/downloads/linux)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/1password-x-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/1password-%E2%80%93-password-mana/aeblfdkhhhdcdjpifhhbdiojplfjncoa)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/dppgmdbiimibapkepcbdbmkaabgiofem)
- [:simple-safari: Safari](https://apps.apple.com/us/app/1password-for-safari/id1569813296)
- [:octicons-browser-16: Web](https://my.1password.com/signin)

</details>

</div>

Traditionally, 1Password has offered the best password manager user experience for people using macOS and iOS; however, it has now achieved feature parity across all platforms. 1Password's clients boast many features geared towards families and less technical people, such as an intuitive UI for ease of use and navigation, as well as advanced functionality. Notably, nearly every feature of 1Password is available within its native mobile or desktop clients.

Brankas 1Password Anda diamankan dengan kata sandi utama dan kunci keamanan 34 karakter yang diacak untuk mengenkripsi data Anda di server mereka. Kunci keamanan ini menambahkan lapisan perlindungan pada data Anda karena data Anda diamankan dengan entropi yang tinggi terlepas dari kata sandi utama Anda. Banyak solusi pengelola kata sandi lainnya yang sepenuhnya bergantung pada kekuatan kata sandi utama Anda untuk mengamankan data Anda.

### Psono

<div class="admonition recommendation" markdown>

![Logo Psono](assets/img/password-management/psono.svg){ align=right }

**Psono** adalah pengelola kata sandi gratis dan bersumber terbuka dari Jerman, dengan fokus pada pengelolaan kata sandi untuk tim. Psono mendukung berbagi kata sandi, file, penanda, dan email dengan aman. Semua rahasia dilindungi oleh kata sandi utama.

[:octicons-home-16: Homepage](https://psono.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://doc.psono.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.com/psono){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.psono.psono)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1545581224)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/psonopw-password-manager/eljmjmgjkbmpmfljlmklcfineebidmlo)
- [:simple-docker: Docker Hub](https://hub.docker.com/r/psono/psono-client)

</details>

</div>

Psono menyediakan dokumentasi ekstensif untuk produk mereka. Klien web untuk Psono bisa di-host sendiri; sebagai alternatif, Anda bisa memilih Edisi Komunitas lengkap atau Edisi Enterprise dengan fitur tambahan.

In April 2024, Psono added [support for passkeys](https://psono.com/blog/psono-introduces-passkeys) for the browser extension only.

### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

#### Persyaratan Minimum

- Harus menggunakan E2EE yang kuat, berbasis standar/modern.
- Harus memiliki praktik enkripsi dan keamanan yang terdokumentasi secara menyeluruh.
- Must have a published audit from a reputable, independent third party.
- Semua telemetri yang tidak penting harus bersifat opsional.
- Tidak boleh mengumpulkan PII lebih banyak daripada yang diperlukan untuk tujuan penagihan.

#### Kasus Terbaik

Kriteria kasus terbaik kami mewakili apa yang ingin kami lihat dari proyek yang sempurna dalam kategori ini. Rekomendasi kami mungkin tidak menyertakan salah satu atau semua fungsi ini, tetapi rekomendasi yang menyertakan fungsi ini mungkin memiliki peringkat yang lebih tinggi daripada yang lain di halaman ini.

- Telemetri harus bersifat opsional (dinonaktifkan secara default) atau tidak dikumpulkan sama sekali.
- Harus bersumber terbuka dan dapat dihos sendiri.

## Penyimpanan Lokal

Opsi ini memungkinkan Anda untuk mengelola basis data kata sandi terenkripsi secara lokal.

### KeePassXC

<div class="admonition recommendation" markdown>

![KeePassXC logo](assets/img/password-management/keepassxc.svg){ align=right }

**KeePassXC** is a community fork of KeePassX, a native cross-platform port of KeePass Password Safe, with the goal of extending and improving it with new features and bug fixes to provide a feature-rich, cross-platform, and modern open-source password manager.

[:octicons-home-16: Homepage](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://keepassxc.org/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassxc.org/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://keepassxc.org/download/#windows)
- [:simple-apple: macOS](https://keepassxc.org/download/#mac)
- [:simple-linux: Linux](https://keepassxc.org/download/#linux)
- [:simple-flathub: Flatpak](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/keepassxc-browser/oboonakemofpalcgghocfoadofidjkkk)

</details>

</div>

KeePassXC menyimpan data ekspornya sebagai file [CSV](https://en.wikipedia.org/wiki/Comma-separated_values). You may encounter data loss if you import this file into another password manager. Kami menyarankan Anda memeriksa setiap catatan secara manual.

### KeePassDX (Android)

<div class="admonition recommendation" markdown>

![KeePassDX logo](assets/img/password-management/keepassdx.svg){ align=right }

**KeePassDX** is a lightweight password manager for Android; it allows for editing encrypted data in a single file in KeePass format and can fill in forms securely. The [pro version](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) of the app allows you to unlock cosmetic content and non-standard protocol features, but more importantly, it helps and encourages development.

[:octicons-home-16: Homepage](https://keepassdx.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassdx.com/#donation){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
- [:simple-github: GitHub](https://github.com/Kunzisoft/KeePassDX/releases)

</details>

</div>

### gopass (CLI)

<div class="admonition recommendation" markdown>

![gopass logo](assets/img/password-management/gopass.svg){ align=right }

**gopass** is a minimal password manager for the command line written in Go. It can be used within scripting applications and works on all major desktop and server operating systems.

[:octicons-home-16: Homepage](https://gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://gopass.pw/#install-windows)
- [:simple-apple: macOS](https://gopass.pw/#install-macos)
- [:simple-linux: Linux](https://gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://gopass.pw/#install-bsd)

</details>

</div>

### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

- Harus lintas platform.
