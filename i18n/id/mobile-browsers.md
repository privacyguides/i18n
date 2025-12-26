---
meta_title: "Peramban Web yang Menghargai Privasi untuk Android dan iOS - Privacy Guides"
title: Peramban Seluler
icon: material/cellphone-information
description: Peramban-peramban inilah yang saat ini kami rekomendasikan untuk penjelajahan internet standar/non-anonim di ponsel Anda.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Rekomendasi Peramban Seluler Pribadi
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Cromite
    image: /assets/img/browsers/cromite.svg
    url: https://cromite.org
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Melindungi dari ancaman(s) berikut ini:</small>

- [:material-account-cash: Kapitalisme Pengawasan](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Berikut ini adalah peramban **web seluler** yang kami rekomendasikan saat ini dan konfigurasi untuk penjelajahan internet standar/non-anonim. Jika Anda perlu menjelajah internet secara anonim, Anda sebaiknya menggunakan [Tor](tor.md) sebagai gantinya.

## Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** menyertakan pemblokir konten bawaan dan [fitur privasi](https://brave.com/privacy-features), yang sebagian besar diaktifkan secara default.

Brave dibuat berdasarkan proyek peramban web Chromium, sehingga seharusnya terasa familier dan memiliki masalah kompatibilitas situs web yang minimal.

[:octicons-home-16: Halaman Utama](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Kebijakan Privasi" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Dokumentasi" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Kode Sumber" }

<details class="downloads" markdown>
<summary>Unduhan</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### Konfigurasi Brave yang Direkomendasikan

Tor Browser adalah satu-satunya cara untuk benar-benar menjelajah internet secara anonim. Ketika Anda menggunakan Brave, kami sarankan untuk mengubah pengaturan berikut ini untuk melindungi privasi Anda dari pihak-pihak tertentu, tetapi semua peramban selain [Tor Browser](tor.md#tor-browser) akan dapat dilacak oleh *seseorang* dalam beberapa hal.

=== "Android"

    Opsi ini dapat ditemukan di :material-menu: → **Settings** → **Brave Shields & privacy**.

=== "iOS"

    Opsi ini dapat ditemukan di :fontawesome-solid-ellipsis: → **Settings** → **Shields & Privacy**.

#### Default global Brave Shield

Brave menyertakan beberapa langkah anti-fingerprinting dalam fitur [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Kami menyarankan untuk mengonfigurasi opsi-opsi ini [secara global](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) di semua halaman yang Anda kunjungi.

Opsi Shields dapat diturunkan pada basis per situs sesuai kebutuhan, tetapi secara default kami sarankan untuk mengatur yang berikut ini:

=== "Android"

    <div class="annotate" markdown>

    - [x] Pilih **Aggressive** di bawah *Block trackers & ads*
    - [x] Pilih **Auto-redirect AMP pages**
    - [x] Pilih **Auto-redirect tracking URLs**
    - [x] Pilih **Require all connections to use HTTPS (strict)** di bawah *Upgrade connections to HTTPS*
    - \[x\] (Opsional) Pilih **Block Scripts** (1)
    - [x] Pilih **Block third-party cookies** di bawah *Block Cookies*
    - [x] Pilih **Block Fingerprinting**
    - [x] Pilih **Prevent fingerprinting via language settings**

    <details class="warning" markdown>
    <summary>Menggunakan daftar filter default</summary>

    Brave memungkinkan Anda untuk memilih filter konten tambahan di dalam menu **Content Filtering** atau halaman internal `brave://adblock`. Kami menyampaikan agar Anda tidak menggunakan fitur ini; sebagai gantinya, pertahankan daftar filter default. Menggunakan daftar tambahan akan membuat Anda terlihat berbeda dari pengguna Brave lainnya dan juga dapat meningkatkan permukaan serangan jika ada eksploitasi di Brave dan aturan berbahaya ditambahkan ke salah satu daftar yang Anda gunakan.

    </details>

    - [x] Pilih **Forget me when I close this site**

    </div>

    1. Opsi ini menonaktifkan JavaScript, yang akan merusak banyak situs. Untuk membatalkannya, Anda dapat menetapkan pengecualian per situs dengan mengetuk ikon Perisai di bilah alamat dan menghapus centang pada pengaturan ini di bawah *Advanced controls*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Pilih **Aggresive** di bawah *Trackers & Ads Blocking*
    - [x] Pilih **Strict** di bawah *Upgrade Connections to HTTPS*
    - [x] Pilih **Auto-Redirect AMP pages**
    - [x] Pilih **Auto-Redirect Tracking URLs**
    - \[x\] (Opsional) Pilih **Block Scripts** (1)
    - [x] Pilih **Block Fingerprinting**
    - [x] Pilih **Site Tabs Closed** di bawah *Auto Shred*

    <details class="warning" markdown>
    <summary>Menggunakan daftar filter default</summary>

    Brave memungkinkan Anda untuk memilih filter konten tambahan dalam menu **Content Filtering**. Kami menyampaikan agar Anda tidak menggunakan fitur ini; sebagai gantinya, pertahankan daftar filter default. Menggunakan daftar tambahan akan membuat Anda terlihat berbeda dari pengguna Brave lainnya dan juga dapat meningkatkan permukaan serangan jika ada eksploitasi di Brave dan aturan berbahaya ditambahkan ke salah satu daftar yang Anda gunakan.

    </details>

    </div>

    1. Opsi ini menonaktifkan JavaScript, yang akan merusak banyak situs. Untuk membatalkannya, Anda dapat menetapkan pengecualian per situs dengan mengetuk ikon Perisai di bilah alamat dan menghapus centang pada pengaturan ini di bawah *Advanced controls*.

##### Menghapus data penelusuran (hanya untuk Android)

- [x] Pilih **Clear data on exit**

##### Pemblokiran Media Sosial (khusus Android)

- [ ] Hapus centang pada semua komponen media sosial

#### Pengaturan privasi lainnya

=== "Android"

    <div class="annotate" markdown>

    - [x] Pilih **Disable non-proxied UDP** di bawah [*WebTPC IP handling policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Opsional) Pilih **No protection** di bawah *Safe Browsing* (1)
    - [ ] Hapus centang **Allow sites to check if you have payment methods saved**
    - [ ] Hapus centang **Javascript optimization & security** di bawah pengaturan dengan nama yang sama
    - [x] Pilih **Close tabs on exit**
    - [ ] Hapus centang **Allow privacy-preserving product analytics (P3A)**
    - [ ] Hapus centang **Automatically send diagnostic reports**
    - [ ] Hapus centang **Automatically send daily usage ping to Brave**

    </div>

    1. [Implementasi Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) Brave di Android **tidak** menggunakan proxy [permintaan jaringan Safe Browsing](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) seperti versi desktopnya. Ini berarti alamat IP Anda dapat dilihat (dan dicatat) oleh Google. Perhatikan bahwa Safe Browsing tidak tersedia untuk perangkat Android tanpa Layanan Google Play.

=== "iOS"

    - [ ] Hapus centang **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] Hapus centang **Automatically send daily usage ping to Brave**

#### Leo

Opsi ini dapat ditambahkan di :material-menu: → **Settings** → **Leo**.

<div class="annotate" markdown>

- [ ] Hapus centang **Show autocomplete suggestions in address bar** (1)

</div>

1. Opsi ini tidak ada di aplikasi iOS Brave.

#### Mesin pencari

Opsi ini dapat ditemukan di :material-menu:/:fontawesome-solid-ellipsis: → **Settings** → **Search engines**.

- [ ] Hapus centang **Show search suggestions**

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) memungkinkan data penjelajahan Anda (riwayat, penanda, dll.) dapat diakses di semua perangkat Anda tanpa memerlukan akun dan melindunginya dengan E2EE.

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Cromite logo](assets/img/browsers/cromite.svg){ align=right }

**Cromite** adalah peramban berbasis Chromium dengan pemblokiran iklan bawaan, perlindungan fingerprinting dan [peningkatan privasi dan keamanan](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). Ini adalah cabang dari peramban **Bromite**.

[:octicons-home-16: Halaman Utama](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Kebijakan Privasi" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Dokumentasi" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Kode Sumber" }

<details class="downloads" markdown>
<summary>Unduhan</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Konfigurasi yang Disarankan

Opsi ini dapat ditemukan di :material-menu: → :gear: **Settings** → **Privacy and security**.

#### Data Penjelajahan

- [x] Pilih **Close all open tabs on exit**

#### Mode Incognito

- [x] Pilih **Open external links in incognito**

#### Keamanan

- [x] Pilih **Always use secure connections**

Hal ini mencegah Anda secara tidak sengaja tersambung ke situs web dalam HTTP teks biasa. HTTP sangat jarang digunakan saat ini, jadi hal ini seharusnya hanya berdampak kecil atau bahkan tidak berdampak sama sekali pada penjelajahan Anda sehari-hari.

#### Pengaturan Adblock Plus

Opsi-opsi ini dapat ditemukan di :material-menu: → :gear: **Settings** → **Adblock Plus settings**.

Cromite berisi versi khusus Adblock Plus dengan EasyList yang diaktifkan secara default, serta opsi untuk memilih lebih banyak daftar filter di dalam menu **Filter lists**.

Menggunakan daftar tambahan akan membuat Anda terlihat berbeda dari pengguna Cromite lainnya dan juga dapat meningkatkan permukaan serangan jika aturan berbahaya ditambahkan ke salah satu daftar yang Anda gunakan.

- \[x\] (Opsional) Pilih **Enable anti-circumvention and snippets**

Pengaturan ini menambahkan daftar Adblock Plus tambahan yang dapat meningkatkan efektivitas pemblokiran konten Cromite. Peringatan mengenai keunggulan dan potensi peningkatan permukaan serangan berlaku.

#### Pengaruran Adblock lama

Opsi ini dapat ditemukan di :material-menu: → :gear: **Settings** → **Legacy Adblock settings**.

- [ ] Hapus centang pada autoupdate setting

Ini menonaktifkan pemeriksaan pembaruan untuk filter adblock Bromite yang tidak dipelihara.

## Safari (iOS)

Di iOS, aplikasi apa pun yang dapat menjelajahi web [dibatasi](https://developer.apple.com/app-store/review/guidelines) untuk menggunakan [kerangka kerja WebKit](https://developer.apple.com/documentation/webkit) yang disediakan Apple, sehingga peramban seperti [Brave](#brave) tidak menggunakan mesin Blink (komponen inti Chromium) seperti mitranya di sistem operasi lain.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** adalah peramban default di iOS. Ini termasuk [fitur privasi](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) seperti [Pencegahan Pelacakan Cerdas](https://webkit.org/blog/7675/intelligent-tracking-prevention), tab Penjelajahan Pribadi yang terisolasi dan bersifat sementara, perlindungan fingerprinting (dengan menyajikan versi sederhana dari konfigurasi sistem ke situs web, sehingga lebih banyak perangkat yang terlihat sama), dan pengacakan fingerprint, serta Private Relay untuk mereka yang berlangganan iCloud+ berbayar.

[:octicons-home-16: Halaman Utama](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Kebijakan Privasi" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="Dokumentasi" }

</details>

</div>

### Konfigurasi Safari yang Direkomendasikan

Opsi terkait privasi/keamanan berikut ini dapat ditemukan di :gear: **Settings** → **Apps** → **Safari**.

#### Allow Safari to Access

Dibawah **Siri**:

- [ ] Nonaktifkan **Learn from this App**
- [ ] Nonaktifkan **Show in App**
- [ ] Nonaktifkan **Show on Home Screen**
- [ ] Nonaktifkan **Suggest App**

Hal ini mencegah Siri menggunakan konten dari Safari untuk saran Siri.

#### Search

- [ ] Nonaktifkan **Search Engine Suggestions**

Pengaturan ini mengirimkan apa pun yang Anda ketik di bilah alamat ke mesin pencari yang diatur di Safari. Dengan menonaktifkan saran pencarian, Anda dapat mengontrol data yang Anda kirimkan ke penyedia mesin pencari dengan lebih tepat.

#### Proflles

Safari memungkinkan Anda untuk memisahkan penjelajahan dengan profil yang berbeda. Semua cookie, riwayat, dan data situs web Anda terpisah untuk setiap profil. Anda harus menggunakan profil yang berbeda untuk tujuan yang berbeda, misalnya Belajar, Kerja, atau Sekolah.

#### Privasi & Keamanan

- [x] Aktifkan **Prevent Cross-Site Tracking**

Hal ini memungkinkan [Perlindungan Pelacakan Cerdas](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) Webkit. Fitur ini membantu melindungi dari pelacakan yang tidak diinginkan dengan menggunakan pembelajaran mesin pada perangkat untuk menghentikan pelacak. ITP melindungi dari banyak ancaman umum, tetapi tidak memblokir semua jalan pelacakan karena dirancang untuk tidak mengganggu kegunaan situs web.

- [x] Aktifkan **Require Face ID/Touch ID to Unlock Private Browsing**

Pengaturan ini memungkinkan Anda untuk mengunci tab pribadi Anda di belakang biometrik/PIN ketika tidak digunakan.

- [ ] Nonaktifkan **Fraudulent Website Warning**

Pengaturan ini menggunakan Google Safe Browsing (atau Tencent Safe Browsing untuk pengguna di Tiongkok atau Hong Kong) untuk melindungi Anda saat menjelajah. Dengan demikian, alamat IP Anda mungkin dicatat oleh penyedia Safe Browsing Anda. Menonaktifkan pengaturan ini akan menonaktifkan logging, tetapi Anda mungkin akan lebih rentan terhadap situs-situs phishing yang dikenal.

- [x] Aktifkan **Not Secure Connection Warning**

Pengaturan ini menampilkan layar peringatan jika koneksi Anda ke situs web tidak menggunakan HTTPS. Safari akan secara otomatis mencoba meningkatkan situs ke HTTPS, jadi Anda hanya akan melihat ini ketika tidak ada koneksi HTTPS yang tersedia.

- [ ] Nonaktifkan **Highlights**

Kebijakan privasi Apple untuk Safari menyatakan:

> Saat mengunjungi halaman web, Safari dapat mengirimkan informasi yang dihitung dari alamat halaman web ke Apple melalui OHTTP untuk menentukan apakah sorotan yang relevan tersedia.

#### Pengaturan untuk Situs Web

Di bawah **Camera**

- [x] Pilih **Ask**

Di bawa **Microphone**

- [x] Pilih **Ask**

Di bawah **Location**

- [x] Pilih **Ask**

Pengaturan ini memastikan bahwa situs web hanya dapat mengakses kamera, mikrofon, atau lokasi Anda setelah Anda secara eksplisit memberikan akses kepada mereka.

#### Pengaturan Privasi Lainnya

Opsi ini dapat ditemukan di :gear: **Settings** → **Apps** → **Safari** → **Advanced**.

##### Mitigasi Fingerprinting

Pengaturan **Advanced Tracking and Fingerprinting Protection** akan mengacak nilai tertentu sehingga fingerprinting Anda akan lebih sulit:

- [x] Pilih **All Browsing** atau **Private Browsing**

##### Privacy Preserving Ad Measurement

- [ ] Nonaktifkan **Privacy Preserving Ad Measurement**

Pengukuran klik iklan secara tradisional menggunakan teknologi pelacakan yang melanggar privasi pengguna. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) adalah fitur WebKit dan standar web yang bertujuan untuk memungkinkan pengiklan mengukur efektivitas kampanye web tanpa mengorbankan privasi pengguna.

Fitur ini memiliki sedikit masalah privasi, jadi meskipun Anda dapat memilih untuk membiarkannya aktif, kami menganggap fakta bahwa fitur ini dinonaktifkan secara otomatis di Private Browsing sebagai indikator untuk menonaktifkan fitur tersebut.

#### Always-on Private Browsing

Buka Safari dan ketuk tombol Tab, yang terletak di kanan bawah. Kemudian, perluas daftar :material-format-list-bulleted: Tab Groups.

- [x] Pilih **Private**

Mode Safari Private Browsing menawarkan perlindungan privasi tambahan. Private Browsing menggunakan sesi [ephemeral](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) untuk setiap tab, yang berarti tab-tab tersebut terpisah satu sama lain. Ada juga manfaat privasi lain yang lebih kecil dengan Private Browsing, seperti tidak mengirimkan alamat halaman web ke Apple saat menggunakan fitur terjemahan Safari.

Harap diperhatikan bahwa Private Browsing tidak menyimpan cookie dan data situs web, sehingga Anda tidak dapat tetap masuk ke situs. Hal ini mungkin merepotkan.

#### iCloud Sync

Sinkronisasi Riwayat Safari, Group Tab, iCloud Tab dan kata sandi yang disimpan adalah E2EE. Namun demikian, secara default, bookmark [tidak](https://support.apple.com/HT202303) digunakan. Apple dapat mendekripsi dan mengaksesnya sesuai dengan [kebijakan privasi](https://apple.com/legal/privacy/en-ww) mereka.

Anda dapat mengaktifkan E2EE untuk penanda dan unduhan Safari dengan mengaktifkan [Advanced Data Protection](https://support.apple.com/HT212520). Buka :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] Aktifkan **Advanced Data Protection**

Jika Anda menggunakan iCloud dengan Advanced Data Protection dinonaktifkan, kami juga menyarankan untuk mengatur lokasi unduhan default Safari ke folder lokal di perangkat Anda. Opsi ini dapat ditemukan di :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

### Persyaratan Minimum

- Harus mendukung pembaruan otomatis.
- Harus menerima pembaruan mesin dari rilis hulu dengan cepat.
- Harus mendukung pemblokiran konten.
- Perubahan apa pun yang diperlukan untuk membuat permban lebih menghargai privasi tidak boleh berdampak negatif pada pengalaman pengguna.
