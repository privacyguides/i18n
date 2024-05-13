---
meta_title: "Private VPN Service Recommendations and Comparison, No Sponsors or Ads - Privacy Guides"
title: "Layanan VPN"
icon: material/vpn
description: Ini adalah layanan VPN terbaik untuk melindungi privasi dan keamanan daring Anda. Temukan penyedia di sini yang tidak memata-matai Anda.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<!-- markdownlint-disable MD024 -->

If you're looking for additional **privacy** from your ISP, on a public Wi-Fi network, or while torrenting files, a VPN may be the solution for you.

<div class="admonition danger" markdown>
<p class="admonition-title">VPNs do not provide anonymity</p>

Using a VPN will **not** keep your browsing habits anonymous, nor will it add additional security to non-secure (HTTP) traffic.

If you are looking for **anonymity**, you should use the Tor Browser. If you're looking for added **security**, you should always ensure you're connecting to websites using HTTPS. VPN bukanlah pengganti praktik keamanan yang baik.

[Download Tor](https://torproject.org){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Ikhtisar VPN Terperinci :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Penyedia yang Direkomendasikan

Our recommended providers use encryption, support WireGuard & OpenVPN, and have a no logging policy. Baca [daftar lengkap kriteria kami](#criteria) untuk informasi lebih lanjut.

| Provider              | Countries | WireGuard                     | Port Forwarding                                            | IPv6                                                     | Anonymous Payments |
| --------------------- | --------- | ----------------------------- | ---------------------------------------------------------- | -------------------------------------------------------- | ------------------ |
| [Proton](#proton-vpn) | 91+       | :material-check:{ .pg-green } | :material-information-outline:{ .pg-blue } Partial Support | :material-alert-outline:{ .pg-orange }                   | Uang Tunai         |
| [IVPN](#ivpn)         | 37+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-information-outline:{ .pg-blue } Outgoing Only | Monero, Cash       |
| [Mullvad](#mullvad)   | 41+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                            | Monero, Cash       |

### Proton VPN

<div class="admonition recommendation" markdown>

![Logo Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** adalah pesaing kuat dalam bidang VPN, dan mereka telah beroperasi sejak 2016. Proton AG berbasis di Swiss dan menawarkan tingkat gratis terbatas, serta opsi premium yang lebih berfitur.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:simple-windows11: Windows](https://protonvpn.com/download-windows)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 91 Countries

Proton VPN has [servers in 91 countries](https://protonvpn.com/vpn-servers) or [5](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/free-vpn/server).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Ini karena rute yang lebih pendek (lebih sedikit loncatan) ke tempat tujuan.
{ .annotate }

1. Last checked: 2024-04-02

Kami juga berpikir akan lebih baik untuk keamanan kunci pribadi penyedia VPN jika mereka menggunakan [server khusus](https://en.wikipedia.org/wiki/Dedicated_hosting_service), daripada solusi berbagi pakai yang lebih murah (dengan pelanggan lain) seperti [peladen pribadi virtual](https://id.wikipedia.org/wiki/Peladen_pribadi_virtual).

#### :material-check:{ .pg-green } Diaudit Secara Independen

Pada Januari 2020, Proton VPN telah menjalani audit independen oleh SEC Consult. SEC Consult menemukan beberapa kerentanan berisiko sedang dan rendah di aplikasi Proton VPN di Windows, Android, dan iOS, yang semuanya telah "diperbaiki dengan benar" oleh Proton VPN sebelum laporan diterbitkan. Tidak satu pun dari masalah yang diidentifikasi akan memberikan penyerang akses jarak jauh ke perangkat atau lalu lintas Anda. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit) and the report was [produced by Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). [Surat pengesahan ](https://proton.me/blog/security-audit-all-proton-apps) diberikan untuk aplikasi Proton VPN pada tanggal 9 November 2021 oleh [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Klien Sumber Terbuka

Proton VPN menyediakan kode sumber untuk klien desktop dan seluler mereka di [organisasi GitHub](https://github.com/ProtonVPN) mereka.

#### :material-check:{ .pg-green } Menerima Uang Tunai

Proton VPN, selain menerima kartu kredit/debit, PayPal, dan [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), juga menerima **uang tunai/mata uang lokal** sebagai bentuk pembayaran anonim.

#### :material-check:{ .pg-green } Dukungan WireGuard

Proton VPN sebagian besar mendukung protokol WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Selain itu, WireGuard bertujuan untuk menjadi lebih sederhana dan lebih berkinerja.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. On Proton VPN's Windows, macOS, iOS, Android, ChromeOS, and Android TV apps, WireGuard is the default protocol; however, [support](https://protonvpn.com/support/how-to-change-vpn-protocols) for the protocol is not present in their Linux app.

#### :material-alert-outline:{ .pg-orange } No IPv6 Support

Proton VPN's servers are only compatible with IPv4. The Proton VPN applications will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, and you will not be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The Windows app provides an easy to access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Torrent applications often support NAT-PMP natively.

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or Wireguard are blocked with various rudimentary techniques. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately it does not work very well in countries where sophisticated filters are deployed that analyze all outgoing traffic in an attempt to discover encrypted tunnels. Stealth is also not yet available on [Windows](https://github.com/ProtonVPN/win-app/issues/64) or Linux.

#### :material-check:{ .pg-green } Klien Ponsel

In addition to providing standard OpenVPN configuration files, Proton VPN has mobile clients for [App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), and [GitHub](https://github.com/ProtonVPN/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

Proton VPN clients support two factor authentication on all platforms. Proton VPN memiliki server dan pusat data mereka sendiri di Swiss, Islandia, dan Swedia. They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](tor.md#tor-browser) for this purpose.

##### :material-alert-outline:{ .pg-orange } Fitur killswitch rusak pada Mac berbasis Intel

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN killswitch. Jika Anda memerlukan fitur ini, dan Anda menggunakan Mac dengan chipset Intel, Anda sebaiknya mempertimbangkan untuk menggunakan layanan VPN lain.

### IVPN

<div class="admonition recommendation" markdown>

![Logo IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** adalah penyedia VPN premium, dan mereka telah beroperasi sejak 2009. IVPN is based in Gibraltar and does not offer a free trial.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:simple-windows11: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Countries

IVPN has [servers in 37 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Ini karena rute yang lebih pendek (lebih sedikit loncatan) ke tempat tujuan.
{ .annotate }

1. Last checked: 2024-04-02

Kami juga berpikir akan lebih baik untuk keamanan kunci pribadi penyedia VPN jika mereka menggunakan [server khusus](https://en.wikipedia.org/wiki/Dedicated_hosting_service), daripada solusi berbagi pakai yang lebih murah (dengan pelanggan lain) seperti [peladen pribadi virtual](https://id.wikipedia.org/wiki/Peladen_pribadi_virtual).

#### :material-check:{ .pg-green } Diaudit Secara Independen

IVPN telah menjalani [audit tanpa pencatatan dari Cure53](https://cure53.de/audit-report_ivpn.pdf) yang menyimpulkan bahwa klaim tanpa pencatatan dari IVPN disetujui. IVPN juga telah menyelesaikan [laporan pentest komprehensif Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) pada Januari 2020. IVPN has also said they plan to have [annual reports](https://ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Klien Sumber Terbuka

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Kode sumber dapat diperoleh dari [organisasi GitHub](https://github.com/ivpn) mereka.

#### :material-check:{ .pg-green } Menerima Uang Tunai dan Monero

Selain menerima kartu kredit/debit dan PayPal, IVPN menerima Bitcoin, **Monero** dan **uang tunai/mata uang lokal** (pada paket tahunan) sebagai bentuk pembayaran anonim.

#### :material-check:{ .pg-green } Dukungan WireGuard

IVPN mendukung protokol WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Selain itu, WireGuard bertujuan untuk menjadi lebih sederhana dan lebih berkinerja.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6 Support

IVPN allows you to [connect to services using IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Penerusan Porta Jarak Jauh

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using the [v2ray](https://v2ray.com/en/index.html) project which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. Currently this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } Klien Ponsel

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

IVPN clients support two factor authentication. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Logo Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** adalah VPN yang cepat dan murah dengan fokus serius pada transparansi dan keamanan. Mereka telah beroperasi sejak **2009**. Mullvad is based in Sweden and does not offer a free trial.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:simple-windows11: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 41 Countries

Mullvad has [servers in 41 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Ini karena rute yang lebih pendek (lebih sedikit loncatan) ke tempat tujuan.
{ .annotate }

1. Last checked: 2024-04-02

Kami juga berpikir akan lebih baik untuk keamanan kunci pribadi penyedia VPN jika mereka menggunakan [server khusus](https://en.wikipedia.org/wiki/Dedicated_hosting_service), daripada solusi berbagi pakai yang lebih murah (dengan pelanggan lain) seperti [peladen pribadi virtual](https://id.wikipedia.org/wiki/Peladen_pribadi_virtual).

#### :material-check:{ .pg-green } Diaudit Secara Independen

Klien VPN Mullvad telah diaudit oleh Cure53 dan Assured AB dalam laporan pentest [yang diterbitkan di cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). Para peneliti keamanan menyimpulkan:

> Cure53 dan Assured AB senang dengan hasil audit dan perangkat lunak ini meninggalkan kesan positif secara keseluruhan. Dengan dedikasi keamanan dari tim internal di kompleks VPN Mullvad, para penguji tidak meragukan proyek ini berada di jalur yang benar dari sudut pandang keamanan.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> Hasil dari proyek Mei-Juni 2020 yang menargetkan kompleks Mullvad ini cukup positif. [...] Keseluruhan ekosistem aplikasi yang digunakan oleh Mullvad meninggalkan kesan yang baik dan terstruktur. Struktur keseluruhan aplikasi memudahkan untuk meluncurkan patch dan perbaikan secara terstruktur. Lebih dari segalanya, temuan yang ditemukan oleh Cure53 menunjukkan pentingnya untuk terus mengaudit dan menilai ulang vektor kebocoran saat ini, untuk selalu memastikan privasi pengguna akhir. Dengan demikian, Mullvad melakukan pekerjaan yang sangat baik dalam melindungi pengguna akhir dari kebocoran PII yang umum terjadi dan risiko terkait privasi.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data) and is available on [Assured's website](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Klien Sumber Terbuka

Mullvad menyediakan kode sumber untuk klien desktop dan seluler mereka di [organisasi GitHub](https://github.com/mullvad/mullvadvpn-app) mereka.

#### :material-check:{ .pg-green } Menerima Uang Tunai dan Monero

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment, prepaid cards with redeem codes are also available. Mereka juga menerima transfer Swish dan transfer bank.

#### :material-check:{ .pg-green } Dukungan WireGuard

Mullvad mendukung protokol WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Selain itu, WireGuard bertujuan untuk menjadi lebih sederhana dan lebih berkinerja.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } Dukungan IPv6

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Penerusan Porta Jarak Jauh

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad has obfuscation an mode using [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) which may be useful in situations where VPN protocols like OpenVPN or Wireguard are blocked.

#### :material-check:{ .pg-green } Klien Ponsel

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. Klien Android juga tersedia di [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They use [ShadowSocks](https://shadowsocks.org) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Seharusnya, [Cina harus menggunakan metode yang berbeda untuk memblokir server ShadowSocks](https://github.com/net4people/bbs/issues/22).

## Kriteria

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Penting untuk dicatat bahwa menggunakan penyedia VPN tidak akan membuat Anda menjadi anonim, tetapi akan memberi Anda privasi yang lebih baik dalam situasi tertentu. VPN bukanlah alat untuk aktivitas ilegal. Jangan bergantung pada kebijakan "tanpa pencatatan".

</div>

**Harap diperhatikan bahwa kami tidak berafiliasi dengan penyedia yang kami rekomendasikan. Hal ini memungkinkan kami untuk memberikan rekomendasi yang sepenuhnya objektif.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk setiap penyedia VPN yang ingin direkomendasikan, termasuk enkripsi yang kuat, audit keamanan independen, teknologi modern, dan banyak lagi. Kami menyarankan Anda membiasakan diri dengan daftar ini sebelum memilih penyedia VPN, dan melakukan penelitian sendiri untuk memastikan penyedia VPN yang Anda pilih dapat dipercaya.

### Teknologi

Kami mewajibkan semua penyedia VPN yang kami rekomendasikan untuk menyediakan berkas konfigurasi OpenVPN untuk digunakan pada klien mana pun. **Jika** VPN menyediakan klien khusus mereka sendiri, kami memerlukan killswitch untuk memblokir kebocoran data jaringan saat terputus.

**Minimum untuk Memenuhi Syarat:**

- Dukungan untuk protokol yang kuat seperti WireGuard & OpenVPN.
- Killswitch yang terpasang pada klien.
- Dukungan multihop. Multihopping penting untuk menjaga kerahasiaan data jika terjadi kompromi pada satu node.
- Jika klien VPN tersedia, klien tersebut seharusnya [bersumber terbuka](https://id.wikipedia.org/wiki/Perangkat_lunak_sumber_terbuka), seperti perangkat lunak VPN yang umumnya sudah terpasang di dalamnya. Kami percaya bahwa ketersediaan [kode sumber](https://id.wikipedia.org/wiki/Kode_sumber) memberikan transparansi yang lebih besar tentang apa yang sebenarnya dilakukan oleh perangkat Anda.

**Kasus Terbaik:**

- Killswitch dengan opsi yang sangat mudah dikonfigurasi (aktifkan/nonaktifkan pada jaringan tertentu, saat boot, dll.)
- Klien VPN yang mudah digunakan
- Mendukung [IPv6](https://id.wikipedia.org/wiki/IPv6). Kami berharap server akan mengizinkan koneksi masuk melalui IPv6 dan memungkinkan Anda untuk mengakses layanan yang dihosting pada alamat IPv6.
- Kemampuan [penerusan porta jarak jauh](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) membantu dalam membuat koneksi ketika menggunakan perangkat lunak berbagi file P2P ([Peer-to-Peer](https://id.wikipedia.org/wiki/Peer-to-peer)) atau hosting server (misalnya, Mumble).
- Obfuscation technology which pads data packets with random data to circumvent internet censorship.

### Privasi

Kami lebih memilih penyedia yang kami rekomendasikan untuk mengumpulkan data sesedikit mungkin. Tidak mengumpulkan informasi pribadi pada saat pendaftaran, dan tidak menerima bentuk pembayaran anonim.

**Minimum untuk Memenuhi Syarat:**

- [Mata uang kripto anonim](cryptocurrency.md) **atau** opsi pembayaran tunai.
- Tidak ada informasi pribadi yang diperlukan untuk mendaftar: Hanya nama pengguna, kata sandi, dan surel.

**Kasus Terbaik:**

- Menerima beberapa opsi [pembayaran anonim](advanced/payments.md).
- Tidak ada informasi pribadi yang diterima (nama pengguna yang dibuat secara otomatis, tidak perlu surel, dll.).

### Keamanan

VPN tidak ada gunanya jika tidak bisa menyediakan keamanan yang memadai. Kami mewajibkan semua penyedia yang kami rekomendasikan untuk mematuhi standar keamanan saat ini untuk koneksi OpenVPN mereka. Secara ideal, mereka akan menggunakan skema enkripsi yang lebih tahan terhadap masa depan secara bawaan. Kami juga mewajibkan pihak ketiga yang independen untuk mengaudit keamanan penyedia layanan, secara ideal dengan cara yang sangat komprehensif dan secara berulang (tahunan).

**Minimum untuk Memenuhi Syarat:**

- Skema enkripsi yang kuat: OpenVPN dengan autentikasi SHA-256; RSA-2048 atau jabat tangan yang lebih baik; enkripsi data AES-256-GCM atau AES-256-CBC.
- Forward Secrecy.
- Audit keamanan yang dipublikasikan dari perusahaan pihak ketiga yang memiliki reputasi baik.

**Kasus Terbaik:**

- Enkripsi terkuat: RSA-4096.
- Forward Secrecy.
- Audit keamanan yang dipublikasikan secara komprehensif dari perusahaan pihak ketiga yang memiliki reputasi baik.
- Program bug-bounty dan/atau proses pengungkapan kerentanan yang terkoordinasi.

### Kepercayaan

Anda tidak akan mempercayakan keuangan Anda pada seseorang dengan identitas palsu, jadi mengapa mempercayakan data internet Anda pada mereka? Kami mewajibkan penyedia layanan yang kami rekomendasikan untuk terbuka mengenai kepemilikan atau kepemimpinan mereka. Kami juga ingin melihat laporan transparansi yang lebih sering, terutama dalam hal bagaimana permintaan pemerintah ditangani.

**Minimum untuk Memenuhi Syarat:**

- Kepemimpinan atau kepemilikan yang berhadapan dengan publik.

**Kasus Terbaik:**

- Kepemimpinan yang berhadapan dengan publik.
- Laporan transparansi yang sering.

### Pemasaran

Dengan penyedia VPN yang kami rekomendasikan, kami ingin melihat pemasaran yang bertanggung jawab.

**Minimum untuk Memenuhi Syarat:**

- Harus menyediakan analitik sendiri (yaitu, tanpa Google Analytics). Situs penyedia juga harus mematuhi [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) untuk orang-orang yang ingin menolak pelacakan.

Tidak boleh melakukan pemasaran yang tidak bertanggung jawab:

- Menjamin perlindungan anonimitas 100%. Ketika seseorang membuat klaim bahwa sesuatu itu 100%, itu berarti tidak ada kepastian untuk gagal. Kami tahu bahwa orang dapat dengan mudah menyamarkan nama mereka dengan beberapa cara, misalnya:
    - Reusing personal information (e.g., email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Sidik jari peramban](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Klaim bahwa VPN sirkuit tunggal "lebih anonim" daripada Tor, yang merupakan sirkuit tiga atau lebih loncatan yang secara teratur berubah.
- Gunakan bahasa yang bertanggung jawab: misalnya, tidak masalah untuk mengatakan bahwa VPN "terputus" atau "tidak tersambung", namun mengklaim bahwa seseorang "terpapar", "rentan", atau "terkompromi" merupakan penggunaan bahasa yang tidak perlu dan tidak benar. Sebagai contoh, orang tersebut mungkin saja menggunakan layanan penyedia VPN lain atau menggunakan Tor.

**Kasus Terbaik:**

Pemasaran yang bertanggung jawab yang mendidik dan bermanfaat bagi konsumen dapat mencakup:

- Perbandingan yang akurat dengan kapan [Tor](tor.md) harus digunakan sebagai gantinya.
- Ketersediaan situs web penyedia VPN melalui [layanan .onion](https://id.wikipedia.org/wiki/.onion)

### Fungsionalitas Tambahan

Meskipun tidak sepenuhnya merupakan persyaratan, ada beberapa faktor yang kami pertimbangkan ketika menentukan penyedia mana yang akan direkomendasikan. These include content blocking functionality, warrant canaries, multihop connections, excellent customer support, the number of allowed simultaneous connections, etc.
