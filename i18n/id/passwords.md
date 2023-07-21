---
meta_title: "Pengelola Kata Sandi Terbaik untuk Melindungi Privasi dan Keamanan Anda - Privacy Guides"
title: "Pengelola Kata Sandi"
icon: material/form-textbox-password
description: Pengelola kata sandi memungkinkan Anda menyimpan dan mengelola kata sandi dan kredensial lainnya dengan aman.
cover: passwords.png
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Rekomendasi Pengelola Kata Sandi
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
    url: https://keepassxc.org/
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
    url: https://www.keepassdx.com/
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
    url: https://strongboxsafe.com/
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
    url: https://www.gopass.pw/
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

!!! info

    Pengelola kata sandi bawaan pada perangkat lunak seperti peramban dan sistem operasi terkadang tidak sebaik perangkat lunak pengelola kata sandi khusus. Keuntungan dari pengelola kata sandi bawaan adalah integrasi yang baik dengan perangkat lunak, tetapi sering kali sangat sederhana dan tidak memiliki fitur privasi dan keamanan seperti yang dimiliki oleh penawaran mandiri.
    
    Sebagai contoh, pengelola kata sandi di Microsoft Edge sama sekali tidak menawarkan E2EE. Pengelola kata sandi Google memiliki [optional](https://support.google.com/accounts/answer/11350823) E2EE, dan [Apple] (https://support.apple.com/en-us/HT202303) menawarkan E2EE secara default.

## Aplikasi berbasis cloud

Pengelola kata sandi ini menyinkronkan kata sandi Anda ke server cloud untuk kemudahan akses dari semua perangkat Anda dan keamanan terhadap kehilangan perangkat.

### Bitwarden

!!! recommendation

    ![Logo Bitwarden](assets/img/password-management/bitwarden.svg){ align=right }
    
    **Bitwarden** adalah sebuah pengelola kata sandi yang gratis dan bersumber terbuka. Ini bertujuan untuk memecahkan masalah manajemen kata sandi untuk individu, tim, dan organisasi bisnis. Bitwarden merupakan salah satu solusi terbaik dan teraman untuk menyimpan semua login dan kata sandi Anda sekaligus menjaganya agar tetap tersinkronisasi dengan mudah di antara semua perangkat Anda.
    
    [:octicons-home-16: Homepage](https://bitwarden.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Kebijakan Privasi" }
    [:octicons-info-16:](https://bitwarden.com/help/){ .card-link title=Dokumentasi}
    [:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Kode Sumber" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
        - [:simple-appstore: App Store](https://apps.apple.com/app/bitwarden-password-manager/id1137397744)
        - [:simple-github: GitHub](https://github.com/bitwarden/mobile/releases)
        - [:simple-windows11: Windows](https://bitwarden.com/download)
        - [:simple-linux: Linux](https://bitwarden.com/download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/bitwarden-free-password-m/nngceckbapebfimnlniiiahkandclblb)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)

Bitwarden juga memiliki fitur [Bitwarden Send](https://bitwarden.com/products/send/), yang memungkinkan Anda untuk berbagi teks dan file dengan aman dengan [ enkripsi end-to-end](https://bitwarden.com/help/send-encryption). [Kata sandi](https://bitwarden.com/help/send-privacy/#send-passwords) dapat diminta bersama dengan tautan kirim. Bitwarden Send juga memiliki fitur [penghapusan otomatis](https://bitwarden.com/help/send-lifespan).

Anda memerlukan [Paket Premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) untuk dapat berbagi file. Paket yang gratis hanya bisa berbagi teks saja.

Kode sisi server Bitwarden adalah [open-source](https://github.com/bitwarden/server), jadi jika Anda tidak ingin menggunakan cloud Bitwarden, Anda dapat dengan mudah meng-host server sinkronisasi Bitwarden Anda sendiri.

**Vaultwarden** adalah implementasi alternatif dari server sinkronisasi Bitwarden yang ditulis dalam Rust dan kompatibel dengan klien Bitwarden resmi, sempurna untuk penerapan yang dihosting sendiri di mana menjalankan layanan resmi yang penuh sumber daya mungkin tidak ideal. Jika Anda ingin meng-host Bitwarden di server Anda sendiri, Gunakanlah Vaultwarden dan bukan kode server resmi Bitwarden.

[:octicons-repo-16: Repositori Vaultwarden](https://github.com/dani-garcia/vaultwarden ""){.md-button} [:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title=Dokumentasi}
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Kode Sumber" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title=Kontribusi }

### 1Password

!!! recommendation

    ![Logo 1Password](assets/img/password-management/1password.svg){ align=right }
    
    **1Password** adalah pengelola kata sandi dengan fokus yang kuat pada keamanan dan kemudahan penggunaan, yang memungkinkan Anda menyimpan kata sandi, kartu kredit, lisensi perangkat lunak, dan informasi sensitif lainnya dalam brankas digital yang aman. Brankas Anda di-host di server 1Password dengan biaya [biaya bulanan] (https://1password.com/sign-up/). 1Password sudah [teraudit](https://support.1password.com/security-assessments/) secara teratur dan menyediakan dukungan pelanggan yang bagus. 1Password is closed source; however, the security of the product is thoroughly documented in their [security white paper](https://1passwordstatic.com/files/security/1password-white-paper.pdf).
    
    [:octicons-home-16: Homepage](https://1password.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://1password.com/legal/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.1password.com/){ .card-link title=Documentation}
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750?mt=8)
        - [:simple-windows11: Windows](https://1password.com/downloads/windows/)
        - [:simple-apple: macOS](https://1password.com/downloads/mac/)
        - [:simple-linux: Linux](https://1password.com/downloads/linux/)

Traditionally, **1Password** has offered the best password manager user experience for people using macOS and iOS; however, it has now achieved feature-parity across all platforms. It boasts many features geared towards families and less technical people, as well as advanced functionality.

Your 1Password vault is secured with both your master password and a randomized 34-character security key to encrypt your data on their servers. This security key adds a layer of protection to your data because your data is secured with high entropy regardless of your master password. Many other password manager solutions are entirely reliant on the strength of your master password to secure your data.

One advantage 1Password has over Bitwarden is its first-class support for native clients. While Bitwarden relegates many duties, especially account management features, to their web vault interface, 1Password makes nearly every feature available within its native mobile or desktop clients. 1Password's clients also have a more intuitive UI, which makes them easier to use and navigate.

### Psono

!!! recommendation

    ![Psono logo](assets/img/password-management/psono.svg){ align=right }
    
    **Psono** is a free and open-source password manager from Germany, with a focus on password management for teams. Psono supports secure sharing of passwords, files, bookmarks, and emails. All secrets are protected by a master password.
    
    [:octicons-home-16: Homepage](https://psono.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://doc.psono.com){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.com/psono){ .card-link title="Source Code" }
    
    ??? unduhan
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.psono.psono)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/psono-password-manager/id1545581224)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/psonopw-password-manager/eljmjmgjkbmpmfljlmklcfineebidmlo)
        - [:simple-docker: Docker Hub](https://hub.docker.com/r/psono/psono-client)

Psono menyediakan dokumentasi ekstensif untuk produk mereka. Klien web untuk Psono bisa di-host sendiri; sebagai alternatif, Anda bisa memilih Edisi Komunitas lengkap atau Edisi Enterprise dengan fitur tambahan.

### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

!!! contoh "Bagian ini baru"

    Kami sedang berupaya menetapkan kriteria yang jelas untuk setiap bagian dari situs kami, dan hal ini dapat berubah sewaktu-waktu. Jika Anda memiliki pertanyaan mengenai kriteria kami, silakan [tanyakan di forum](https://discuss.privacyguides.net/latest) dan jangan berasumsi bahwa kami tidak mempertimbangkan sesuatu saat membuat rekomendasi jika tidak tercantum di sini. Ada banyak faktor yang dipertimbangkan dan didiskusikan saat kami merekomendasikan sebuah proyek, dan mendokumentasikan setiap faktor tersebut merupakan sebuah pekerjaan yang sedang berjalan.

#### Persyaratan Minimum

- Harus menggunakan E2EE yang kuat, berbasis standar/modern.
- Harus memiliki praktik enkripsi dan keamanan yang terdokumentasi secara menyeluruh.
- Harus memiliki audit yang dipublikasikan dari pihak ketiga yang memiliki reputasi baik dan independen.
- Semua telemetri yang tidak penting harus bersifat opsional.
- Tidak boleh mengumpulkan PII lebih banyak daripada yang diperlukan untuk tujuan penagihan.

#### Kasus Terbaik

Kriteria kasus terbaik kami mewakili apa yang ingin kami lihat dari proyek yang sempurna dalam kategori ini. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Telemetry should be opt-in (disabled by default) or not collected at all.
- Should be open-source and reasonably self-hostable.

## Local Storage

These options allow you to manage an encrypted password database locally.

### KeePassXC

!!! recommendation

    ![KeePassXC logo](assets/img/password-management/keepassxc.svg){ align=right }
    
    **KeePassXC** is a community fork of KeePassX, a native cross-platform port of KeePass Password Safe, with the goal to extend and improve it with new features and bugfixes to provide a feature-rich, cross-platform and modern open-source password manager.
    
    [:octicons-home-16: Homepage](https://keepassxc.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://keepassxc.org/docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://keepassxc.org/donate/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://keepassxc.org/download/#windows)
        - [:simple-apple: macOS](https://keepassxc.org/download/#mac)
        - [:simple-linux: Linux](https://keepassxc.org/download/#linux)
        - [:simple-flathub: Flatpak](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/keepassxc-browser/oboonakemofpalcgghocfoadofidjkkk)

KeePassXC stores its export data as [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) files. This may mean data loss if you import this file into another password manager. We advise you check each record manually.

### KeePassDX (Android)

!!! recommendation

    ![KeePassDX logo](assets/img/password-management/keepassdx.svg){ align=right }
    
    **KeePassDX** is a lightweight password manager for Android, allows editing encrypted data in a single file in KeePass format and can fill in the forms in a secure way. [Contributor Pro](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) allows unlocking cosmetic content and non-standard protocol features, but more importantly, it helps and encourages development.
    
    [:octicons-home-16: Homepage](https://www.keepassdx.com){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.keepassdx.com/#donation){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
        - [:simple-github: GitHub](https://github.com/Kunzisoft/KeePassDX/releases)

### Strongbox (iOS & macOS)

!!! recommendation

    ![Strongbox logo](assets/img/password-management/strongbox.svg){ align=right }
    
    **Strongbox** is a native, open-source password manager for iOS and macOS. Supporting both KeePass and Password Safe formats, Strongbox can be used in tandem with other password managers, like KeePassXC, on non-Apple platforms. By employing a [freemium model](https://strongboxsafe.com/pricing/), Strongbox offers most features under its free tier with more convenience-oriented [features](https://strongboxsafe.com/comparison/)—such as biometric authentication—locked behind a subscription or perpetual license.
    
    [:octicons-home-16: Homepage](https://strongboxsafe.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://strongboxsafe.com/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://strongboxsafe.com/getting-started/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/strongbox-password-safe/Strongbox){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://github.com/strongbox-password-safe/Strongbox#supporting-development){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/strongbox-keepass-pwsafe/id897283731)

Additionally, there is an offline-only version offered: [Strongbox Zero](https://apps.apple.com/app/strongbox-keepass-pwsafe/id1581589638). This version is stripped down in an attempt to reduce attack surface.

### Baris perintah

These products are minimal password managers that can be used within scripting applications.

#### gopass

!!! recommendation

    ![gopass logo](assets/img/password-management/gopass.svg){ align=right }
    
    **gopass** is a password manager for the command line written in Go. It works on all major desktop and server operating systems (Linux, macOS, BSD, Windows).
    
    [:octicons-home-16: Homepage](https://www.gopass.pw){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://www.gopass.pw/#install-windows)
        - [:simple-apple: macOS](https://www.gopass.pw/#install-macos)
        - [:simple-linux: Linux](https://www.gopass.pw/#install-linux)
        - [:simple-freebsd: FreeBSD](https://www.gopass.pw/#install-bsd)

### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

!!! contoh "Bagian ini baru"

    Kami sedang berupaya menetapkan kriteria yang jelas untuk setiap bagian dari situs kami, dan hal ini dapat berubah sewaktu-waktu. Jika Anda memiliki pertanyaan mengenai kriteria kami, silakan [tanyakan di forum](https://discuss.privacyguides.net/latest) dan jangan berasumsi bahwa kami tidak mempertimbangkan sesuatu saat membuat rekomendasi jika tidak tercantum di sini. Ada banyak faktor yang dipertimbangkan dan didiskusikan saat kami merekomendasikan sebuah proyek, dan mendokumentasikan setiap faktor tersebut merupakan sebuah pekerjaan yang sedang berjalan.

- Must be cross-platform.
