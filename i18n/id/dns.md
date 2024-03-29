---
title: "Penyelesai DNS"
icon: material/dns
description: Berikut ini adalah beberapa penyedia DNS terenkripsi yang kami sarankan yang bisa digunakan untuk menggantikan konfigurasi bawaan ISP Anda.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

DNS terenkripsi dengan server pihak ketiga sebaiknya hanya digunakan untuk mengatasi pemblokiran [DNS dasar](https://en.wikipedia.org/wiki/DNS_blocking) ketika Anda yakin tidak akan ada konsekuensi apa pun. DNS yang terenkripsi tidak akan membantu menyembunyikan aktivitas penjelajahan Anda.

[Pelajari lebih lanjut tentang DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Penyedia yang Direkomendasikan

| Penyedia DNS                                                               | Kebijakan Privasi                                                                                    | Protokol                                                                     | Pencatatan Log | ECS      | Pemfilteran                                                                                                                                                     |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | -------------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard**](https://adguard.com/en/adguard-dns/overview.html)            | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext <br> DoH/3 <br> DoT <br> DoQ <br> DNSCrypt | Beberapa[^1]   | Yes      | Berdasarkan konfigurasi pribadi. Daftar filter yang digunakan dapat ditemukan di sini. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Teks biasa <br> DoH/3 <br> DoT                                   | Beberapa[^2]   | Tidak    | Berdasarkan konfigurasi pribadi.                                                                                                                                |
| [**Control D**](https://controld.com/free-dns)                             | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Teks biasa <br> DoH/3 <br> DoT <br> DoQ                    | Opsional[^3]   | Tidak    | Berdasarkan konfigurasi pribadi.                                                                                                                                |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH <br> DoT                                                           | Tidak[^4]      | Tidak    | Berdasarkan konfigurasi pribadi. Daftar filter yang digunakan dapat ditemukan di sini. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    |
| [**NextDNS**](https://nextdns.io)                                          | [:octicons-link-external-24:](https://nextdns.io/privacy)                                            | Teks biasa <br> DoH/3 <br> DoT <br> DoQ                    | Opsional[^5]   | Opsional | Berdasarkan konfigurasi pribadi.                                                                                                                                |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Teks biasa <br> DoH <br> DoT <br> DNSCrypt                 | Beberapa[^6]   | Opsional | Berdasarkan konfigurasi personal, Malware terblokir secara default.                                                                                             |

### Kriteria

**Harap dicatat bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami menyarankan agar Anda mengenal lebih lanjut daftar di bawah ini sebelum memutuskan untuk menggunakan project tertentu. Selalu lakukan riset sendiri untuk memastikan bahwa project tersebut adalah pilihan yang tepat untuk Anda.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Kami sedang berupaya menetapkan kriteria yang ditentukan untuk setiap bagian dari situs kami, dan hal ini dapat berubah sewaktu-waktu. Jika Anda memiliki pertanyaan tentang kriteria kami, silakan [tanyakan di forum kami](https://discuss.privacyguides.net/latest) dan jangan berasumsi bahwa kami tidak mempertimbangkan sesuatu saat membuat rekomendasi jika tidak tercantum di sini. Ada banyak faktor yang dipertimbangkan dan didiskusikan saat kami merekomendasikan sebuah proyek, dan mendokumentasikan setiap faktor tersebut merupakan pekerjaan yang sedang berjalan.

</div>

- Harus mendukung [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [Minimalisasi QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- Mengizinkan [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) untuk dinonaktifkan.
- Dukungan [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) atau geo-steering lebih disukai.

## Dukungan Sistem Operasi

### Android

Android 9 ke atas mendukung DNS melalui TLS. Pengaturan dapat ditemukan di: **Pengaturan** &rarr; **Jaringan & Internet** &rarr; **DNS Pribadi**.

### Perangkat Apple

Versi terbaru iOS, iPadOS, tvOS, dan macOS, mendukung DoT dan DoH. Kedua protokol didukung secara default melalui [profil konfigurasi](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) atau melalui [API Pengaturan DNS](https://developer.apple.com/documentation/networkextension/dns_settings).

Setelah pemasangan profil konfigurasi atau aplikasi yang menggunakan API Pengaturan DNS, konfigurasi DNS dapat dipilih. Jika VPN aktif, pengaturan DNS dalam VPN akan digunakan untuk menentukan resolusi, bukan pengaturan DNS sistem Anda secara keseluruhan.

#### Profil yang Ditandatangani

Apple tidak menyediakan antarmuka asli untuk membuat profil DNS terenkripsi. [Pembuat profil DNS aman](https://dns.notjakob.com/tool.html) adalah alat tidak resmi untuk membuat profil DNS terenkripsi Anda sendiri, namun profil tersebut tidak akan ditandatangani. Profil yang ditandatangani lebih disukai; penandatanganan memvalidasi asal profil dan membantu memastikan integritas profil. Label "Terverifikasi" berwarna hijau diberikan pada profil konfigurasi yang telah ditandatangani. Untuk informasi lebih lanjut tentang penandatanganan kode, lihat [Tentang Penandatanganan Kode](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html). **Signed profiles** are offered by [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io), and [Quad9](https://quad9.net/news/blog/ios-mobile-provisioning-profiles).

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

`systemd-resolved`, yang digunakan banyak distribusi Linux untuk melakukan pencarian DNS, belum [mendukung DoH](https://github.com/systemd/systemd/issues/8639). Jika Anda ingin menggunakan DoH, Anda perlu menginstal proxy seperti [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) dan [konfigurasikan] (https://wiki.archlinux.org/title/Dnscrypt-proxy) untuk mengambil semua permintaan DNS dari resolver sistem Anda dan meneruskannya melalui HTTPS.

</div>

## DNS Proxy yang Terenkripsi

Perangkat lunak proxy DNS terenkripsi menyediakan proxy lokal untuk [DNS tidak terenkripsi](advanced/dns-overview.md#unencrypted-dns) resolver untuk diteruskan. Biasanya digunakan pada platform yang tidak mendukung [DNS terenkripsi](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo ]( assets/img/android/rethinkdns.svg#only-light ){ align=right }
![RethinkDNS logo ]( assets/img/android/rethinkdns-dark.svg#only-dark ){ align=right }

** RethinkDNS ** adalah klien Android sumber terbuka yang mendukung [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) dan Proksi DNS bersama dengan tanggapan DNS cache, pencatatan permintaan DNS lokal dan dapat digunakan sebagai tembok api juga.

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![dnscrypt - proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt - proxy ** adalah proxy DNS dengan dukungan untuk [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), dan [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonimized-DNS).

<div class="admonition warning" markdown>
<p class="admonition-title">The anonymized DNS feature does <a href="advanced/dns-overview.md#why-shouldnt-i0-use-encrypted-dns"><strong>not</strong></a> anonymize other network traffic.</p>
</div>

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

## Solusi Self-hosting

Solusi DNS yang dihosting sendiri berguna untuk menyediakan penyaringan pada platform terkontrol, seperti Smart TV dan perangkat IoT lainnya, karena tidak ada perangkat lunak di sisi klien yang diperlukan.

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

AdGuard Home memiliki antarmuka web yang dipoles untuk melihat wawasan dan mengelola konten yang diblokir.

[:octicons-home-16: Beranda](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Kebijakan Privasi" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Dokumentasi}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Kode Sumber" }

</details>

</div>

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

Pi-hole dirancang untuk dihosting di Raspberry Pi, tetapi tidak terbatas pada perangkat keras tersebut. Perangkat lunak ini memiliki antarmuka web yang ramah untuk melihat analisis dan mengelola konten yang diblokir.

[:octicons-home-16: Homepage](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribute }

</details>

</div>

[^1]: AdGuard menyimpan informasi kinerja dari server DNS mereka, seperti informasi request kepada server tertentu, jumlah request yang terblokir dan informasi mengenai kecepatan request ketika sedang diproses. Mereka juga menyimpan database domain yang diminta dalam waktu 24 jam terakhir. "Kami membutuhkan informasi ini untuk mengidentifikasi dan memblokir pelacak dan ancaman baru." "Kami juga mencatat berapa kali pelacak telah diblokir. Kami membutuhkan informasi ini untuk menghapus aturan lama dari filter kami." [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare hanya mengumpulkan dan menyimpan data permintaan DNS terbatas yang dikirim ke resolver 1.1.1.1. Layanan resolver 1.1.1.1 tidak mencatat data pribadi, dan sebagian besar data yang tidak dapat diidentifikasi secara pribadi hanya disimpan selama 25 jam. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D hanya mencatat untuk resolver Premium dengan profil DNS khusus. Resolver gratis tidak mencatat data. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: Layanan DNS Mullvad tersedia untuk pelanggan dan non-pelanggan Mullvad VPN. Kebijakan privasi mereka secara eksplisit mengklaim bahwa mereka tidak mencatat permintaan DNS dengan cara apa pun. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether. If used without an account, no data is logged. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: Quad9 mengumpulkan beberapa data untuk tujuan pemantauan dan tanggapan ancaman. Data nantinya diacak dan dibagikan untuk tujuan penelitian keamanan. Quad9 tidak mengumpulkan atau mencatat alamat IP atau data lain yang mereka anggap dapat diidentifikasi secara pribadi. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
