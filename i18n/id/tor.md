---
meta_title: "Peramban dan Jaringan Tor: Penjelajahan Web Anonim - Privacy Guides"
title: "Tor Browser"
icon: simple/torbrowser
description: Lindungi penjelajahan internet Anda dari pengintaian dengan menggunakan jaringan Tor, sebuah jaringan aman yang dapat menghindari penyensoran.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://en.wikipedia.org/wiki/Tor_(network)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Melindungi dari ancaman(s) berikut ini:</small>

- [:material-account-cash: Kapitalisme Pengawasan](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Pengawasan Massal](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Penyensoran](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** adalah sekelompok server yang dioperasikan secara sukarela yang memungkinkan Anda terhubung secara gratis dan meningkatkan privasi dan keamanan Anda di Internet. Individu dan organisasi juga dapat berbagi informasi melalui jaringan Tor dengan ".onion layanan tersembunyi " tanpa mengorbankan privasi mereka. Karena lalu lintas Tor sulit diblokir dan dilacak, Tor merupakan alat pengelabuan sensor yang efektif.

[Ikhtisar Tor Terperinci :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary}[:material-movie-open-play-outline: Video: Mengapa Anda Membutuhkan Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Sebelum menyambung ke Tor, pastikan Anda telah membaca [ikhtisar](advanced/tor-overview.md) tentang apa itu Tor dan bagaimana menyambung ke Tor dengan aman. Kami sering menyarankan untuk menyambung ke Tor melalui [penyedia VPN](vpn.md) terpercaya, tetapi Anda harus melakukannya **dengan benar** untuk menghindari berkurangnya anonimitas Anda.

</div>

Ada berbagai cara untuk terhubung ke jaringan Tor dari perangkat Anda, yang paling umum digunakan adalah **Tor Browser**, sebuah fork dari Firefox yang dirancang untuk penjelajahan [:material-incognito: anonim](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} untuk komputer desktop dan Android.

Beberapa dari aplikasi ini lebih baik daripada yang lain; menentukan pilihan tergantung pada model ancaman Anda. Jika Anda adalah pengguna Tor biasa yang tidak khawatir tentang ISP Anda mengumpulkan bukti melawan Anda, menggunakan aplikasi peramban seluler seperti [Onion Browser](#onion-browser-ios) untuk mengakses jaringan Tor mungkin tidak masalah. Meningkatkan jumlah orang yang menggunakan Tor setiap hari membantu mengurangi stigma buruk Tor, dan menurunkan kualitas "daftar pengguna Tor" yang mungkin disusun oleh ISP dan pemerintah.

Jika anonimitas yang lebih lengkap adalah yang terpenting dalam situasi Anda, Anda sebaiknya **hanya** menggunakan klien Tor browser desktop, idealnya dalam konfigurasi [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Peramban seluler lebih jarang digunakan pada Tor (lebih mudah fingerprinting), dan konfigurasi lainnya tidak diuji secara ketat terhadap deanonimisasi.

## Tor Browser

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** adalah pilihan jika Anda membutuhkan anonimitas, dengan menyediakan akses ke jaringan dan jembatan Tor, dan termasuk pengaturan dan ekstensi bawaan yang secara otomatis dikonfigurasi oleh tingkat keamanan bawaan: *Standard*, *Safer* dan *Safest*.

[:octicons-home-16: Halaman Utama](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Layanan Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="Dokumentasi" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Kode Sumber" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="Berkontribusi" }

<details class="downloads" markdown>
<summary>Unduhan</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Bahaya</p>

Anda sebaiknya **jangan pernah** memasang ekstensi tambahan apa pun pada Tor Browser atau menyunting pengaturan `about:config`, termasuk yang kami sarankan untuk Firefox. Ekstensi browser dan pengaturan nonstandar membuat Anda menonjol dari orang lain di jaringan Tor, sehingga membuat peramban Anda lebih mudah untuk [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

Tor Browser dirancang untuk mencegah fingerprinting, atau mengidentifikasi Anda berdasarkan konfigurasi peramban Anda. Oleh karena itu, sangat penting bagi Anda untuk **tidak** memodifikasi peramban di luar [tingkat keamanan](https://tb-manual.torproject.org/security-settings) bawaan. Saat menyesuaikan tingkat keamanan, Anda **harus** selalu memulai ulang peramban sebelum melanjutkan penggunaannya. Jika tidak, [pengaturan keamanan mungkin tidak sepenuhnya diterapkan](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), sehingga Anda berada pada risiko fingerprinting dan eksploitasi yang lebih tinggi daripada yang Anda harapkan berdasarkan pengaturan yang dipilih.

Selain aplikasi yang terancam di bawah ini, ada juga sistem operasi yang dirancang khusus untuk terhubung ke jaringan Tor seperti [Whonix](desktop.md#whonix) di [Qubes OS](desktop.md#qubes-os), yang menyediakan keamanan dan perlindungan yang lebih besar daripada Tor Browser standar.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** adalah peramban bersumber terbuka yang memungkinkan Anda menjelajah web secara anonim melalui jaringan Tor di perangkat-perangkat iOS, dan didukung oleh [Tor Project](https://support.torproject.org/glossary/onion-browser).

[:material-star-box: Baca ulasan Onion Browser terbaru kami.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: Halaman Utama](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Kebijakan Privasi" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title="Dokumentasi" }
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Kode Sumber" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="Berkontribusi" }

<details class="downloads" markdown>
<summary>Unduhan</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser tidak menyediakan tingkat perlindungan privasi yang sama seperti Tor Browser pada platform desktop. Untuk penggunaan biasa, ini merupakan cara yang sangat baik untuk mengakses layanan tersembunyi, tetapi jika Anda khawatir akan dilacar atau dipantau oleh musuh tingkat lanjut, Anda sebaiknya tidak mengandalkan ini sebagai alat anonimitas.

[Khususnya](https://github.com/privacyguides/privacyguides.org/issues/2929), Onion Browser tidak *menjamin* semua permintaan melalui Tor. Ketika menggunakan versi bawaan Tor, [IP asli Anda **akan** dibocorkan melalui WebRTC dan streaming audio/video](https://onionbrowser.com/faqs) karena keterbatasan WebKit. *Lebih aman* menggunakan Onion Browser bersama [Orbot](alternative-networks.md#orbot), tetapi ini masih memiliki beberapa keterbatasan pada iOS.
