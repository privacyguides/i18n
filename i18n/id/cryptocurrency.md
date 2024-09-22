---
meta_title: "Private Cryptocurrency Blockchains - Privacy Guides"
description: Unlike most cryptocurrencies, these ones provide transaction privacy by default. Monero is our top choice for obfuscating transaction information.
title: Mata Uang Kripto
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Protects against the following threat(s):</small>

- [:material-eye-outline: Pengawasan Massal](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Penyensoran](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

Melakukan pembayaran secara daring adalah salah satu tantangan terbesar bagi privasi. Mata uang kripto di bawah ini menyediakan privasi transaksi secara bawaan (sesuatu yang **tidak** dijamin oleh sebagian besar mata uang kripto), asalkan Anda memiliki pemahaman yang kuat tentang cara melakukan pembayaran pribadi secara efektif. Kami sangat menyarankan Anda untuk membaca artikel ikhtisar pembayaran kami terlebih dahulu sebelum melakukan pembelian:

[Melakukan Pembayaran Pribadi :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Banyak atau bahkan sebagian besar proyek mata uang kripto adalah penipuan. Lakukan transaksi dengan hati-hati hanya dengan proyek yang Anda percayai.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** uses a blockchain with privacy-enhancing technologies that obfuscate transactions to achieve [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }. Setiap transaksi Monero menyembunyikan jumlah transaksi, alamat pengirim dan penerima, dan sumber dana tanpa ada rintangan yang harus dilewati, menjadikannya pilihan ideal untuk pemula mata uang kripto.

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribute }

</details>

</div>

Dengan Monero, pengamat luar tidak dapat menguraikan alamat yang memperdagangkan Monero, jumlah transaksi, saldo alamat, atau riwayat transaksi.

Untuk privasi yang optimal, pastikan untuk menggunakan dompet nonkustodian di mana kunci tampilan tetap berada di perangkat. Ini berarti hanya Anda yang dapat menggunakan dana Anda dan melihat transaksi yang masuk dan keluar. If you use a custodial wallet, the provider can see **everything** you do; if you use a “lightweight” wallet where the provider retains your private view key, the provider can see almost everything you do. Some noncustodial wallets include:

- [Official Monero client](https://getmonero.org/downloads) (Desktop)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, macOS)
    - Cake Wallet supports multiple cryptocurrencies. A Monero-only version of Cake Wallet for iOS and Android is available at [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

For maximum privacy (even with a noncustodial wallet), you should run your own Monero node. Using another person’s node will expose some information to them, such as the IP address that you connect to it from, the timestamps that you sync your wallet, and the transactions that you send from your wallet (though no other details about those transactions). Alternatively, you can connect to someone else’s Monero node over Tor or [I2P](alternative-networks.md#i2p-the-invisible-internet-project).

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. Public postings show that the US Department of the Treasury's Financial Crimes Enforcement Network [licensed](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) CipherTrace's "Monero Module" in late 2022.

Monero transaction graph privacy is limited by its relatively small ring signatures, especially against targeted attacks. Monero's privacy features have also been [called into question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) by some security researchers, and a number of severe vulnerabilities have been found and patched in the past, so the claims made by organizations like CipherTrace are not out of the question. While it's unlikely that Monero mass surveillance tools exist like they do for Bitcoin and others, it's certain that tracing tools assist with targeted investigations.

Ultimately, Monero is the strongest contender for a privacy-friendly cryptocurrency, but its privacy claims have **not** been definitively proven one way or the other. More time and research is needed to assess whether Monero is resilient enough to attacks to always provide adequate privacy.

## Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

- Cryptocurrency must provide private/untraceable transactions by default.
