---
meta_title: "Peramban dan Jaringan Tor: Penjelajahan Web Anonim - Privacy Guides"
title: "Jaringan Tor"
icon: simple/torproject
description: Protect your internet browsing from prying eyes by using the Tor network, a secure network which circumvents censorship.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
    image: /assets/img/browsers/tor.svg
    url: https://www.torproject.org
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

[:octicons-home-16:](https://www.torproject.org){ .card-link title="Laman Beranda" }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Layanan Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Dokumentasi}
[:octicons-code-16:](https://gitweb.torproject.org/tor.git){ .card-link title="Kode Sumber" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Berkontribusi }

Tor bekerja dengan merutekan lalu lintas internet Anda melalui server yang dioperasikan secara sukarela, daripada membuat koneksi langsung ke situs yang Anda coba kunjungi. Hal ini mengaburkan dari mana lalu lintas berasal, dan tidak ada server di jalur koneksi yang dapat melihat jalur penuh dari mana lalu lintas berasal dan pergi, yang berarti bahkan server yang Anda gunakan untuk terhubung tidak dapat merusak anonimitas Anda.

[Ikhtisar Tor Terperinci :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Menghubungkan ke Tor

Ada berbagai cara untuk terhubung ke jaringan Tor dari perangkat Anda, yang paling umum digunakan adalah **Tor Browser**, sebuah fork dari Firefox yang dirancang untuk penjelajahan anonim untuk komputer desktop dan Android. Selain aplikasi yang tercantum di bawah ini, ada juga sistem operasi yang dirancang khusus untuk terhubung ke jaringan Tor seperti [Whonix](desktop.md#whonix) di [Qubes OS](desktop.md#qubes-os), yang menyediakan keamanan dan perlindungan yang lebih besar daripada Tor Browser standar.

### Tor Browser

!!! recommendation

    ![Logo Tor Browser](assets/img/browsers/tor.svg){ align=right }
    
    **Tor Browser** adalah pilihan jika Anda membutuhkan anonimitas, dengan menyediakan akses ke jaringan dan jembatan Tor, dan termasuk pengaturan dan ekstensi bawaan yang secara otomatis dikonfigurasikan oleh tingkat keamanan bawaan: *Standar*, *Lebih Aman* dan *Paling Aman*.
    
    [:octicons-home-16: Beranda](https://www.torproject.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Layanan Onion" }
    [:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Dokumentasi }
    [:octicons-code-16:](https://gitweb.torproject.org/tor-browser.git/){ .card-link title="Kode Sumber" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Berkontribusi }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
        - [:simple-android: Android](https://www.torproject.org/download/#android)
        - [:simple-windows11: Windows](https://www.torproject.org/download/)
        - [:simple-apple: macOS](https://www.torproject.org/download/)
        - [:simple-linux: Linux](https://www.torproject.org/download/)

!!! danger

    Anda sebaiknya **jangan pernah** memasang ekstensi tambahan apa pun pada Tor Browser atau menyunting pengaturan `about:config`, termasuk yang kami sarankan untuk Firefox. Ekstensi browser dan pengaturan nonstandar membuat Anda menonjol dari orang lain di jaringan Tor, sehingga membuat peramban Anda lebih mudah untuk [disidik jari](https://support.torproject.org/glossary/browser-fingerprinting).

Tor Browser dirancang untuk mencegah sidik jari, atau mengidentifikasi Anda berdasarkan konfigurasi peramban Anda. Oleh karena itu, sangat penting bagi Anda untuk tidak **tidak** memodifikasi peramban di luar [tingkat keamanan](https://tb-manual.torproject.org/security-settings/) bawaan.

### Orbot

!!! recommendation

    ![Logo Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }
    
    **Orbot** adalah VPN Tor gratis untuk ponsel pintar yang merutekan lalu lintas dari aplikasi apa pun pada perangkat Anda melalui jaringan Tor.
    
    [:octicons-home-16: Beranda](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Kebijakan Privasi" }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Dokumentasi}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title="Kode Sumber" }
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Berkontribusi }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

We previously recommended enabling the *Isolate Destination Address* preference in Orbot settings. While this setting can theoretically improve privacy by enforcing the use of a different circuit for each IP address you connect to, it doesn't provide a practical advantage for most applications (especially web browsing), can come with a significant performance penalty, and increases the load on the Tor network. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

!!! tip "Tips untuk Android"

    Orbot dapat memproksi aplikasi individual jika aplikasi tersebut mendukung proksi SOCKS atau HTTP. Ini juga dapat memproksi semua koneksi jaringan Anda menggunakan [VpnService](https://developer.android.com/reference/android/net/VpnService) dan dapat digunakan dengan killswitch VPN di :gear: **Pengaturan** → **Jaringan & internet** → **VPN** → :gear: → **Blokir koneksi tanpa VPN**.
    
    Orbot sering kali ketinggalan versi di [repositori F-Droid] (https://guardianproject.info/fdroid) dan [Google Play] (https://play.google.com/store/apps/details?id=org.torproject.android) milik Guardian Project, jadi pertimbangkan untuk mengunduh langsung dari [repositori GitHub] (https://github.com/guardianproject/orbot/releases).
    
    Semua versi ditandatangani menggunakan tanda tangan yang sama sehingga seharusnya kompatibel satu sama lain.

### Onion Browser

!!! recommendation

    ![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }
    
    **Onion Browser** adalah peramban bersumber terbuka yang memungkinkan Anda menjelajah web secara anonim melalui jaringan Tor di perangkat-perangkat iOS, dan didukung oleh [Tor Project](https://support.torproject.org/glossary/onion-browser/).
    
    [:octicons-home-16: Beranda](https://strongboxsafe.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://strongboxsafe.com/privacy/){ .card-link title="Kebijakan Privasi" }
    [:octicons-info-16:](https://onionbrowser.com/faqs/){ .card-link title=Dokumentasi}
    [:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Kode Sumber" }
    [:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Kontribusi }
    
    ??? unduhan
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

## Relai dan Jembatan

### Snowflake

!!! rekomendasi

    ![Logo Snowflake](assets/img/browsers/snowflake.svg#only-light){ align=right }
    ![Logo Snowflake](assets/img/browsers/snowflake-gelap.svg#only-dark){ align=right }
    
    **Snowflake** memungkinkan Anda untuk menyumbangkan bandwidth ke Proyek Tor dengan mengoperasikan "proksi Snowflake" di dalam peramban Anda.
    
    Orang-orang yang disensor bisa menggunakan proksi Snowflake untuk menyambung ke jaringan Tor. Snowflake adalah cara yang bagus untuk berkontribusi pada jaringan bahkan jika Anda tidak memiliki pengetahuan teknis untuk menjalankan relai atau jembatan Tor.
    
    [:octicons-home-16: Homepage](https://snowflake.torproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitweb.torproject.org/pluggable-transports/snowflake.git/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

You can enable Snowflake in your browser by opening it in another tab and turning the switch on. You can leave it running in the background while you browse to contribute your connection. We don't recommend installing Snowflake as a browser extension; adding third-party extensions can increase your attack surface.

[Run Snowflake in your Browser :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake tidak meningkatkan privasi Anda dengan cara apa pun, dan tidak juga tidak digunakan untuk terhubung ke jaringan Tor dalam peramban pribadi Anda. Namun, jika koneksi internet Anda tidak disensor, Anda sebaiknya mempertimbangkan untuk menjalankannya untuk membantu orang-orang di jaringan yang disensor mencapai privasi yang lebih baik. Tidak perlu khawatir tentang situs web mana yang diakses orang melalui proksi Anda—alamat IP penjelajahan mereka yang terlihat akan cocok dengan node keluar Tor mereka, bukan milik Anda.

Menjalankan proxy Snowflake berisiko rendah, bahkan lebih rendah daripada menjalankan Tor relay atau bridge yang sudah tidak terlalu berisiko. Namun, itu masih memproksi lalu lintas melalui jaringan Anda yang dapat berdampak pada beberapa hal, terutama jika jaringan Anda memiliki bandwidth terbatas. Pastikan Anda memahami [cara kerja Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) sebelum memutuskan apakah akan menjalankan proksi.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://www.whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
