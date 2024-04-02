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
    name: Strongbox
    image: /assets/img/password-management/strongbox.svg
    url: https://strongboxsafe.com
    applicationCategory: Pengelola Kata Sandi
    operatingSystem: iOS
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

Pengelola kata sandi memungkinkan Anda menyimpan dan mengelola kata sandi dan kredensial lainnya dengan aman dengan menggunakan kata sandi utama.

[Pengantar Kata Sandi :material-arrow-right-drop-circle:](./basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

Pengelola kata sandi bawaan pada perangkat lunak seperti peramban dan sistem operasi terkadang tidak sebaik perangkat lunak pengelola kata sandi khusus. Keuntungan dari pengelola kata sandi bawaan adalah integrasi yang baik dengan perangkat lunak, tetapi sering kali sangat sederhana dan tidak memiliki fitur privasi dan keamanan seperti yang dimiliki oleh penawaran mandiri.

Sebagai contoh, pengelola kata sandi di Microsoft Edge sama sekali tidak menawarkan E2EE. Google's password manager has [optional](https://support.google.com/accounts/answer/11350823) E2EE, and [Apple's](https://support.apple.com/HT202303) offers E2EE by default.

</div>

## Aplikasi berbasis cloud

Pengelola kata sandi ini menyinkronkan kata sandi Anda ke server cloud untuk kemudahan akses dari semua perangkat Anda dan keamanan terhadap kehilangan perangkat.

### Bitwarden

<div class="admonition recommendation" markdown>

![Logo Bitwarden](assets/img/password-management/bitwarden.svg){ align=right }

**Bitwarden** adalah sebuah pengelola kata sandi yang gratis dan bersumber terbuka. Ini bertujuan untuk memecahkan masalah manajemen kata sandi untuk individu, tim, dan organisasi bisnis. Bitwarden merupakan salah satu solusi terbaik dan teraman untuk menyimpan semua login dan kata sandi Anda sekaligus menjaganya agar tetap tersinkronisasi dengan mudah di antara semua perangkat Anda.

[:octicons-home-16: Homepage](https://bitwarden.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://bitwarden.com/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1137397744)
- [:simple-github: GitHub](https://github.com/bitwarden/mobile/releases)
- [:simple-windows11: Windows](https://bitwarden.com/download)
- [:simple-linux: Linux](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/bitwarden-free-password-m/nngceckbapebfimnlniiiahkandclblb)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)

</details>

</div>

Bitwarden also features [Bitwarden Send](https://bitwarden.com/products/send), which allows you to share text and files securely with [end-to-end encryption](https://bitwarden.com/help/send-encryption). [Kata sandi](https://bitwarden.com/help/send-privacy/#send-passwords) dapat diminta bersama dengan tautan kirim. Bitwarden Send juga memiliki fitur [penghapusan otomatis](https://bitwarden.com/help/send-lifespan).

Anda memerlukan [Paket Premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) untuk dapat berbagi file. Paket yang gratis hanya bisa berbagi teks saja.

Kode sisi server Bitwarden [bersumber terbuka](https://github.com/bitwarden/server), jadi jika Anda tidak ingin menggunakan "awan" Bitwarden, Anda dapat dengan mudah meng-hos server sinkronisasi Bitwarden Anda sendiri.

**Vaultwarden** adalah implementasi alternatif dari server sinkronisasi Bitwarden yang ditulis dalam Rust dan kompatibel dengan klien Bitwarden resmi, sempurna untuk penerapan yang dihosting sendiri di mana menjalankan layanan resmi yang penuh sumber daya mungkin tidak ideal. Jika Anda ingin meng-host Bitwarden di server Anda sendiri, Gunakanlah Vaultwarden dan bukan kode server resmi Bitwarden.

[:octicons-repo-16: Repositori Vaultwarden](https://github.com/dani-garcia/vaultwarden ""){.md-button} [:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title=Dokumentasi}
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Kode Sumber" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title=Kontribusi }

### 1Password

<div class="admonition recommendation" markdown>

![Logo 1Password](assets/img/password-management/1password.svg){ align=right }

**1Password** adalah pengelola kata sandi dengan fokus yang kuat pada keamanan dan kemudahan penggunaan, yang memungkinkan Anda menyimpan kata sandi, kartu kredit, lisensi perangkat lunak, dan informasi sensitif lainnya dalam brankas digital yang aman. Your vault is hosted on 1Password's servers for a [monthly fee](https://1password.com/sign-up). 1Password is [audited](https://support.1password.com/security-assessments) on a regular basis and provides exceptional customer support. 1Password memiliki sumber yang tertutup; namun, keamanan produk didokumentasikan secara menyeluruh dalam [laporan resmi keamanan] (https://1passwordstatic.com/files/security/1password-white-paper.pdf) mereka.

[:octicons-home-16: Homepage](https://1password.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://1password.com/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.1password.com){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750)
- [:simple-windows11: Windows](https://1password.com/downloads/windows)
- [:simple-apple: macOS](https://1password.com/downloads/mac)
- [:simple-linux: Linux](https://1password.com/downloads/linux)

</details>

</div>

Secara tradisional, **1Password** telah menawarkan pengalaman pengguna pengelola kata sandi terbaik untuk orang-orang yang menggunakan macOS dan iOS; namun, kini telah mencapai kesamaan fitur di semua platform. Aplikasi ini memiliki banyak fitur yang ditujukan untuk keluarga dan orang yang kurang teknis, serta fungsionalitas yang canggih.

Brankas 1Password Anda diamankan dengan kata sandi utama dan kunci keamanan 34 karakter yang diacak untuk mengenkripsi data Anda di server mereka. Kunci keamanan ini menambahkan lapisan perlindungan pada data Anda karena data Anda diamankan dengan entropi yang tinggi terlepas dari kata sandi utama Anda. Banyak solusi pengelola kata sandi lainnya yang sepenuhnya bergantung pada kekuatan kata sandi utama Anda untuk mengamankan data Anda.

Satu keunggulan yang dimiliki 1Password dibandingkan Bitwarden adalah dukungan kelas satu untuk klien asli. Sementara Bitwarden mendelegasikan banyak tugas, terutama fitur manajemen akun, pada antarmuka brankas web mereka, 1Password membuat hampir semua fitur tersedia dalam klien seluler atau desktop aslinya. Klien-klien 1Password juga memiliki UI yang lebih intuitif, yang membuatnya lebih mudah digunakan dan dinavigasi.

### Psono

<div class="admonition recommendation" markdown>

![Logo Psono](assets/img/password-management/psono.svg){ align=right }

**Psono** adalah pengelola kata sandi gratis dan bersumber terbuka dari Jerman, dengan fokus pada pengelolaan kata sandi untuk tim. Psono mendukung berbagi kata sandi, file, penanda, dan email dengan aman. Semua rahasia dilindungi oleh kata sandi utama.

[:octicons-home-16: Homepage](https://psono.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://doc.psono.com){ .card-link title=Documentation}
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

### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

#### Persyaratan Minimum

- Harus menggunakan E2EE yang kuat, berbasis standar/modern.
- Harus memiliki praktik enkripsi dan keamanan yang terdokumentasi secara menyeluruh.
- Harus memiliki audit yang dipublikasikan dari pihak ketiga yang memiliki reputasi baik dan independen.
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

![Logo KeePassXC](assets/img/pengelolaan kata sandi/keepassxc.svg){ align=right }

**KeePassXC** adalah sebuah fork komunitas dari KeePassX, sebuah port lintas platform asli dari KeePass Password Safe, dengan tujuan untuk memperluas dan memperbaikinya dengan fitur-fitur baru dan perbaikan bug untuk menyediakan sebuah pengelola kata sandi yang kaya akan fitur, lintas platform, dan modern bersumber terbuka.

[:octicons-home-16: Homepage](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://keepassxc.org/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassxc.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://keepassxc.org/download/#windows)
- [:simple-apple: macOS](https://keepassxc.org/download/#mac)
- [:simple-linux: Linux](https://keepassxc.org/download/#linux)
- [:simple-flathub: Flatpak](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/keepassxc-browser/oboonakemofpalcgghocfoadofidjkkk)

</details>

</div>

KeePassXC menyimpan data ekspornya sebagai file [CSV](https://en.wikipedia.org/wiki/Comma-separated_values). Hal ini dapat menyebabkan hilangnya data jika Anda mengimpor file ini ke pengelola kata sandi lain. Kami menyarankan Anda memeriksa setiap catatan secara manual.

### KeePassDX (Android)

<div class="admonition recommendation" markdown>

![Logo KeePassDX](assets/img/pengelolaan kata sandi/keepassdx.svg){ align=right }

**KeePassDX** adalah pengelola kata sandi yang ringan untuk Android, memungkinkan pengeditan data terenkripsi dalam satu file dalam format KeePass dan dapat mengisi formulir dengan cara yang aman. [Contributor Pro] (https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) memungkinkan untuk membuka konten kosmetik dan fitur protokol non-standar, tetapi yang lebih penting lagi, ini membantu dan mendorong pengembangan.

[:octicons-home-16: Homepage](https://keepassdx.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassdx.com/#donation){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
- [:simple-github: GitHub](https://github.com/Kunzisoft/KeePassDX/releases)

</details>

</div>

### Strongbox (iOS & macOS)

<div class="admonition recommendation" markdown>

![Logo Strongbox](assets/img/password-management/strongbox.svg){ align=right }

**Strongbox** adalah pengelola kata sandi sumber terbuka untuk iOS dan macOS. Mendukung format KeePass dan Password Safe, Strongbox bisa digunakan bersamaan dengan pengelola kata sandi lainnya, seperti KeePassXC, pada platform non-Apple. By employing a [freemium model](https://strongboxsafe.com/pricing), Strongbox offers most features under its free tier with more convenience-oriented [features](https://strongboxsafe.com/comparison)—such as biometric authentication—locked behind a subscription or perpetual license.

[:octicons-home-16: Homepage](https://strongboxsafe.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://strongboxsafe.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://strongboxsafe.com/getting-started){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/strongbox-password-safe/Strongbox){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/strongbox-password-safe/Strongbox#supporting-development){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id897283731)

</details>

</div>

Additionally, there is an offline-only version offered: [Strongbox Zero](https://apps.apple.com/app/id1581589638). Versi ini sudah diminimalkan dalam upaya untuk mengurangi permukaan serangan.

### Baris perintah

Produk-produk ini adalah pengelola kata sandi minimal yang dapat digunakan dalam aplikasi skrip.

#### gopass

<div class="admonition recommendation" markdown>

![logo gopass](assets/img/password-management/gopass.svg){ align=right }

**gopass** adalah pengelola kata sandi untuk baris perintah yang ditulis dalam Go. Aplikasi ini bekerja pada semua sistem operasi desktop dan server utama (Linux, macOS, BSD, Windows).

[:octicons-home-16: Homepage](https://gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://gopass.pw/#install-windows)
- [:simple-apple: macOS](https://gopass.pw/#install-macos)
- [:simple-linux: Linux](https://gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://gopass.pw/#install-bsd)

</details>

</div>

<!-- markdownlint-disable-next-line -->
### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

- Harus lintas platform.
