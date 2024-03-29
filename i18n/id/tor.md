---
meta_title: "Peramban dan Jaringan Tor: Penjelajahan Web Anonim - Privacy Guides"
title: "Jaringan Tor"
icon: simple/torproject
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

![Logo Tor](assets/img/self-contained-networks/tor.svg){ align=right }

Jaringan **Tor** adalah sekelompok server yang dioperasikan secara sukarela yang memungkinkan Anda terhubung secara gratis dan meningkatkan privasi dan keamanan Anda di Internet. Individu dan organisasi juga dapat berbagi informasi melalui jaringan Tor dengan "layanan tersembunyi .onion" tanpa mengorbankan privasi mereka. Karena lalu lintas Tor sulit diblokir dan dilacak, Tor merupakan alat pengelabuan sensor yang efektif.

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

Tor bekerja dengan merutekan lalu lintas internet Anda melalui server yang dioperasikan secara sukarela, daripada membuat koneksi langsung ke situs yang Anda coba kunjungi. Hal ini mengaburkan dari mana lalu lintas berasal, dan tidak ada server di jalur koneksi yang dapat melihat jalur penuh dari mana lalu lintas berasal dan pergi, yang berarti bahkan server yang Anda gunakan untuk terhubung tidak dapat merusak anonimitas Anda.

[Ikhtisar Tor Terperinci :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Menghubungkan ke Tor

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Before connecting to Tor, please ensure you've read our [overview](advanced/tor-overview.md) on what Tor is and how to connect to it safely. We often recommend connecting to Tor through a trusted [VPN provider](vpn.md), but you have to do so **properly** to avoid decreasing your anonymity.

</div>

Ada berbagai cara untuk terhubung ke jaringan Tor dari perangkat Anda, yang paling umum digunakan adalah **Tor Browser**, sebuah fork dari Firefox yang dirancang untuk penjelajahan anonim untuk komputer desktop dan Android.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Increasing the number of people who use Tor on an everyday basis helps reduce the bad stigma of Tor, and lowers the quality of "lists of Tor users" that ISPs and governments may compile.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

### Tor Browser

<div class="admonition recommendation" markdown>

![Logo Tor Browser](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** adalah pilihan jika Anda membutuhkan anonimitas, dengan menyediakan akses ke jaringan dan jembatan Tor, dan termasuk pengaturan dan ekstensi bawaan yang secara otomatis dikonfigurasikan oleh tingkat keamanan bawaan: *Standar*, *Lebih Aman* dan *Paling Aman*.

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:simple-windows11: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Anda sebaiknya **jangan pernah** memasang ekstensi tambahan apa pun pada Tor Browser atau menyunting pengaturan `about:config`, termasuk yang kami sarankan untuk Firefox. Ekstensi browser dan pengaturan nonstandar membuat Anda menonjol dari orang lain di jaringan Tor, sehingga membuat peramban Anda lebih mudah untuk [disidik jari](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

Tor Browser dirancang untuk mencegah sidik jari, atau mengidentifikasi Anda berdasarkan konfigurasi peramban Anda. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings).

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

### Orbot

<div class="admonition recommendation" markdown>

![Logo Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** adalah VPN Tor gratis untuk ponsel pintar yang merutekan lalu lintas dari aplikasi apa pun pada perangkat Anda melalui jaringan Tor.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Kami sebelumnya merekomendasikan untuk mengaktifkan preferensi *Isolasi Alamat Tujuan* di pengaturan Orbot. Walaupun pengaturan ini secara teoritis dapat meningkatkan privasi dengan memaksakan penggunaan sirkuit yang berbeda untuk setiap alamat IP yang Anda sambungkan, pengaturan ini tidak memberikan keuntungan praktis untuk sebagian besar aplikasi (terutama penelusuran web), dapat menimbulkan dampak buruk signifikan terhadap kinerja, dan meningkatkan beban pada jaringan Tor. Kami tidak lagi menyarankan untuk menyesuaikan pengaturan ini dari nilai bawaannya kecuali jika Anda memang membutuhkannya.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tips for Android</p>

Orbot dapat memproksi aplikasi individual jika aplikasi tersebut mendukung proksi SOCKS atau HTTP. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Orbot sering kali ketinggalan versi di [repositori F-Droid] (https://guardianproject.info/fdroid) dan [Google Play] (https://play.google.com/store/apps/details?id=org.torproject.android) milik Guardian Project, jadi pertimbangkan untuk mengunduh langsung dari [repositori GitHub] (https://github.com/guardianproject/orbot/releases).

Semua versi ditandatangani menggunakan tanda tangan yang sama sehingga seharusnya kompatibel satu sama lain.

</div>

### Onion Browser

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser).

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

## Relai dan Jembatan

### Snowflake

<div class="admonition recommendation" markdown>

![Logo Snowflake](assets/img/browsers/snowflake.svg#only-light){ align=right }
![Logo Snowflake](assets/img/browsers/snowflake-gelap.svg#only-dark){ align=right }

**Snowflake** memungkinkan Anda untuk menyumbangkan bandwidth ke Proyek Tor dengan mengoperasikan "proksi Snowflake" di dalam peramban Anda.

Orang-orang yang disensor bisa menggunakan proksi Snowflake untuk menyambung ke jaringan Tor. Snowflake adalah cara yang bagus untuk berkontribusi pada jaringan bahkan jika Anda tidak memiliki pengetahuan teknis untuk menjalankan relai atau jembatan Tor.

[:octicons-home-16: Homepage](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

</details>

</div>

Anda dapat mengaktifkan Snowflake di peramban Anda dengan membukanya di tab lain dan mengaktifkan tombolnya. Anda dapat membiarkannya berjalan di latar belakang saat Anda menjelajah untuk menyumbangkan koneksi Anda. Kami tidak menyarankan untuk memasang Snowflake sebagai ekstensi peramban; menambahkan ekstensi pihak ketiga dapat meningkatkan permukaan serangan Anda.

[Jalankan Snowflake di Peramban Anda :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake tidak meningkatkan privasi Anda dengan cara apa pun, juga tidak digunakan untuk terhubung ke jaringan Tor dalam peramban pribadi Anda. Namun, jika koneksi internet Anda tidak disensor, Anda sebaiknya mempertimbangkan untuk menjalankannya untuk membantu orang-orang di jaringan yang disensor untuk mencapai privasi yang lebih baik. Tidak perlu khawatir tentang situs web mana yang diakses orang melalui proksi Anda—alamat IP penjelajahan mereka yang terlihat akan cocok dengan node keluar Tor mereka, bukan milik Anda.

Menjalankan proksi Snowflake berisiko rendah, bahkan lebih rendah daripada menjalankan relai Tor atau jembatan yang sudah tidak terlalu berisiko. Namun, itu masih memproksi lalu lintas melalui jaringan Anda yang dapat berdampak pada beberapa hal, terutama jika jaringan Anda memiliki bandwidth terbatas. Pastikan Anda memahami [cara kerja Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) sebelum memutuskan apakah akan menjalankan proksi.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
