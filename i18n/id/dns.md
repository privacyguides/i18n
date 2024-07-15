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

These are our favorite public DNS resolvers based on their privacy and security characteristics, and their worldwide performance. Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked you should use a dedicated DNS filtering product instead.

| Penyedia DNS                                                               | Protokol                                 | Logging / Privacy Policy | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | Pemfilteran                                                                                                                                            | Signed Apple Profile                                                                                                     |
| -------------------------------------------------------------------------- | ---------------------------------------- | ------------------------ | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | Cleartext   DoH/3   DoT   DoQ   DNSCrypt | Anonymized[^1]           | Anonymized                                                     | Based on server choice. Daftar filter yang digunakan dapat ditemukan di sini. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) | Yes [:octicons-link-external-24:](https://adguard.com/en/blog/encrypted-dns-ios-14.html)                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | Cleartext   DoH/3   DoT                  | Anonymized[^2]           | Tidak                                                          | Based on server choice.                                                                                                                                | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846) |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | Cleartext   DoH/3   DoT   DoQ            | No[^3]                   | Tidak                                                          | Based on server choice.                                                                                                                                | Yes [:octicons-link-external-24:](https://docs.controld.com/docs/macos-platform)                                         |
| [**dns0.eu**](https://dns0.eu)                                             | Cleartext   DoH/3   DoH   DoT   DoQ      | Anonymized[^4]           | Anonymized                                                     | Based on server choice.                                                                                                                                | Yes [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                             |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | DoH   DoT                                | No[^5]                   | Tidak                                                          | Based on server choice. Daftar filter yang digunakan dapat ditemukan di sini. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    | Yes [:octicons-link-external-24:](https://mullvad.net/en/blog/profiles-to-configure-our-encrypted-dns-on-apple-devices)  |
| [**Quad9**](https://quad9.net)                                             | Cleartext   DoH   DoT   DNSCrypt         | Anonymized[^6]           | Opsional                                                       | Based on server choice, malware blocking by default.                                                                                                   | Yes [:octicons-link-external-24:](https://quad9.net/news/blog/ios-mobile-provisioning-profiles)                          |

## Self-Hosted DNS Filtering

Solusi DNS yang dihosting sendiri berguna untuk menyediakan penyaringan pada platform terkontrol, seperti Smart TV dan perangkat IoT lainnya, karena tidak ada perangkat lunak di sisi klien yang diperlukan.

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

## Cloud-Based DNS Filtering

These DNS filtering solutions offer a web dashboard where you can customize the blocklists to your exact needs, similarly to a Pi-hole. These services are usually easier to set up and configure than self-hosted services like the ones above, and can be used more easily across multiple networks (self-hosted solutions are typically restricted to your home/local network unless you set up a more advanced configuration).

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. In addition to their paid plans, they offer a number of preconfigured DNS resolvers you can use for free.

[:octicons-home-16: Homepage](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: Linux](https://docs.controld.com/docs/ctrld)
- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: App Store](https://apps.apple.com/app/1518799460)
- [:simple-github: GitHub](https://github.com/Control-D-Inc/ctrld/releases)

</details>

</div>

### NextDNS

<div class="admonition recommendation" markdown>

![NextDNS logo](assets/img/dns/nextdns.svg){ align=right }

**NextDNS** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. They offer a fully functional free plan for limited use.

[:octicons-home-16: Homepage](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)
- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)

</details>

</div>

When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether.

NextDNS's free plan is fully functional, but should not be relied upon for security or other critical filtering applications, because after 300,000 DNS queries in a month all filtering, logging, and other account-based functionality is disabled. It can still be used as a regular DNS provider after that point, so your devices will continue to function and make secure queries via DNS-over-HTTPS, just without your filter lists.

NextDNS also offers public DNS-over-HTTPS service at `https://dns.nextdns.io` and DNS-over-TLS/QUIC at `dns.nextdns.io`, which are available by default in Firefox and Chromium, and subject to their default no-logging [privacy policy](https://nextdns.io/privacy).

## DNS Proxy yang Terenkripsi

Perangkat lunak proxy DNS terenkripsi menyediakan proxy lokal untuk [DNS tidak terenkripsi](advanced/dns-overview.md#unencrypted-dns) resolver untuk diteruskan. Typically, it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** is an open-source Android client that supports [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) and DNS Proxy. It also provides additional functionality such as caching DNS responses, locally logging DNS queries, and using the app as a firewall.

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

While RethinkDNS takes up the Android VPN slot, you can still use a VPN or Orbot with the app by [adding a Wireguard configuration](https://docs.rethinkdns.com/proxy/wireguard) or [manually configuring Orbot as a Proxy server](https://docs.rethinkdns.com/firewall/orbot), respectively.

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![dnscrypt-proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt-proxy** is a DNS proxy with support for [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), and [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

The anonymized DNS feature does [not](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) anonymize other network traffic.

</div>

## Kriteria

**Harap dicatat bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami menyarankan agar Anda mengenal lebih lanjut daftar di bawah ini sebelum memutuskan untuk menggunakan project tertentu. Selalu lakukan riset sendiri untuk memastikan bahwa project tersebut adalah pilihan yang tepat untuk Anda.

All DNS products must support:

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [Minimalisasi QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- Anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.

Additionally, all public providers:

- Dukungan [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) atau geo-steering lebih disukai.
- Must not log any personal data to disk
    - As noted in our footnotes, some providers collect query information for example, for purposes like security research, but in that case that data must not be associated with any PII such as IP address, etc.

[^1]: AdGuard menyimpan informasi kinerja dari server DNS mereka, seperti informasi request kepada server tertentu, jumlah request yang terblokir dan informasi mengenai kecepatan request ketika sedang diproses. Mereka juga menyimpan database domain yang diminta dalam waktu 24 jam terakhir. "Kami membutuhkan informasi ini untuk mengidentifikasi dan memblokir pelacak dan ancaman baru." "Kami juga mencatat berapa kali pelacak telah diblokir. Kami membutuhkan informasi ini untuk menghapus aturan lama dari filter kami." [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare hanya mengumpulkan dan menyimpan data permintaan DNS terbatas yang dikirim ke resolver 1.1.1.1. Layanan resolver 1.1.1.1 tidak mencatat data pribadi, dan sebagian besar data yang tidak dapat diidentifikasi secara pribadi hanya disimpan selama 25 jam. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D hanya mencatat untuk resolver Premium dengan profil DNS khusus. Resolver gratis tidak mencatat data. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: dns0.eu collects some data for their threat intelligence feeds, to monitor for newly registered/observed/active domains and other bulk data. That data is shared with some [partners](https://docs.dns0.eu/data-feeds/introduction) for e.g. security research. They do not collect any Personally Identifiable Information. [https://dns0.eu/privacy](https://dns0.eu/privacy)
[^5]: Layanan DNS Mullvad tersedia untuk pelanggan dan non-pelanggan Mullvad VPN. Kebijakan privasi mereka secara eksplisit mengklaim bahwa mereka tidak mencatat permintaan DNS dengan cara apa pun. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^6]: Quad9 mengumpulkan beberapa data untuk tujuan pemantauan dan tanggapan ancaman. Data nantinya diacak dan dibagikan untuk tujuan penelitian keamanan. Quad9 tidak mengumpulkan atau mencatat alamat IP atau data lain yang mereka anggap dapat diidentifikasi secara pribadi. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
