---
meta_title: "Peramban Web yang Menghargai Privasi untuk PC dan Mac - Privacy Guides"
title: Peramban Desktop
icon: material/laptop
description: Peramban yang melindungki privasi inilah yang saat ini kami rekomendasikan untuk penjelajahan internet standar/non-anonim pada sistem desktop.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Rekomendasi Peramban Desktop Pribadi
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://id.wikipedia.org/wiki/Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://id.wikipedia.org/wiki/Brave_(peramban_web)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Melindungi dari ancaman(s) berikut ini:</small>

- [:material-account-cash: Kapitalisme Pengawasan](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Berikut ini adalah **peramban web desktop** yang kami rekomendasikan saat ini dan konfigurasi untuk penjelajahan standar/non-anonim. Kami merekomendasikan [Mullvad Browser](#mullvad-browser) jika Anda berfokus pada perlindungan privasi yang kuat dan anti-fingerprinting otomatis, [Firefox](#firefox) bagi para penjelajah internet biasa yang mencari alternatif yang baik untuk Google Chrome, dan [Brave](#brave) jika Anda membutuhkan kompatibilitas peramban Chromium.

Jika Anda perlu menjelajah internet secara anonim, Anda sebaiknya menggunakan [Tor](tor.md). Kami memberikan beberapa rekomendasi konfigurasi di halaman ini, tetapi semua browser selain Tor Browser akan dapat dilacak oleh * seseorang* dengan berbagai cara.

## Browser Mullvad

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** adalah versi dari [Tor Browser](tor.md#tor-browser) dengan integrasi jaringan Tor yang telah dihilangkan. Ini bertujuan untuk menyediakan teknolog peramban anti-fingerprinting Tor Browser kepada pengguna VPN, yang merupakan perlindungan utama terhadap [:material-eye-outline: Pengawasan Massal](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. VPN ini dikembangkan oleh Tor Project dan didistribusikan oleh [Mullvad](vpn.md#mullvad), dan **tidak** memerlukan penggunaan VPN Mullvad.

[:octicons-home-16: Halaman Utama](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Kebijakan Privasi" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Dokumentasi" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Kode Sumber" }

<details class="downloads" markdown>
<summary>Unduhan</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Seperti [Tor Browser](tor.md), Mullvad Browser dirancang untuk mencegah fingerprinting dengan membuat fingerprinting Anda identik dengan semua pengguna Mullvad Browser lainnya, dan ini mencakup pengaturan default dan ekstensi yang secara otomatis dikonfigurasi oleh tingkat keamanan default *Standar*, *Lebih Aman* dan *Paling Aman*.

Oleh karena itu, sangat penting bagi Anda untuk tidak memodifikasi peramban sama sekali di luar penyesuaian [tingkat keamanan](https://tb-manual.torproject.org/security-settings) default. Saat menyesuaikan tingkat keamanan, Anda **harus** selalu memulai ulang peramban sebelum melanjutkan penggunaannya. Jika tidak, [pengaturan keamanan mungkin tidak sepenuhnya diterapkan](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), sehingga Anda berada pada risiko fingerprinting dan eksploitasi yang lebih tinggi daripada yang Anda harapkan berdasarkan pengaturan yang dipilih.

Modifikasi selain menyesuaikan pengaturan ini akan membuat fingerprint Anda menjadi unik, sehingga mengalahkan tujuan penggunaan browser ini. Jika Anda ingin mengonfigurasi peramban Anda dengan lebih banyak dan fingerprint bukan menjadi masalah bagi Anda, kami sarankan [Firefox](#firefox) sebagai gantinya.

### Anti-Fingerprinting

**Tanpa** menggunakan [VPN](vpn.md), Mullvad Browser memberikan perlindungan yang sama terhadap [skrip pencocokan fingerprint](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) seperti browser pribadi lainnya seperti Firefox+[Arkenfox](#arkenfox-advanced) atau [Brave](#brave). Mullvad Browser menyediakan perlindungan tersebut secara bawaan, dengan mengorbankan sedikit fleksibilitas dan kenyamanan yang dapat diberikan oleh browser pribadi lainnya.

==Untuk perlindungan anti-fingerprinting yang paling kuat, kami sarankan untuk menggunakan Mullvad Browser bersama **dengan** VPN==, baik itu Mullvad atau penyedia VPN lain yang direkomendasikan. Saat menggunakan VPN dengan Mullvad Browser, Anda akan berbagi fingerprint dan alamat IP dengan pengguna lain, memberikan Anda "kerumunan" untuk berbaur. Strategi ini merupakan satu-satunya cara untuk menggagalkan skrip pelacakan tingkat lanjut, dan merupakan teknik anti-fingerprinting yang sama dengan yang digunakan oleh Tor Browser.

Perlu dicatat bahwa meskipun Anda dapat menggunakan Mullvad Browser dengan penyedia VPN mana pun, orang lain dalam VPN tersebut juga harus menggunakan Mullvad Browser agar "kerumunan" ini terbentuk, hal ini lebih mungkin terjadi pada Mullvad VPN dibandingkan dengan penyedia lainnya, terutama menjelang peluncuran Mullvad Browser. Mullvad Browser tidak memiliki konektivitas VPN bawaan, dan juga tidak memeriksa apakah Anda menggunakan VPN sebelum menjelajah; koneksi VPN Anda harus dikonfigurasikan dan dikelola secara terpisah.

Mullvad Browser hadir dengan ekstensi peramban *uBlock Origin* dan *NoScript* yang sudah diinstal sebelumnya. Meskipun kami biasanya tidak menyarankan untuk *menambahkan* [ekstensi peramban](browser-extensions.md), ekstensi yang sudah terpasang dengan peramban ini **tidak boleh** dihapus atau dikonfigurasi di luar nilai defaultnya, karena hal itu akan membuat fingerprint Anda berbeda dengan pengguna Mullvad Browser lainnya. Browser ini juga telah terpasang dengan Ekstensi Mullvad Browser, yang *dapat* dihapus dengan aman tanpa mempengaruhi fingerprint peramban Anda jika Anda menginginkannya, tetapi juga aman untuk tetap dipertahankan bahkan jika Anda tidak menggunakan Mullvad VPN.

### Mode Penjelajahan Pribadi

Mullvad Browser beroperasi dalam mode penjelajahan pribadi permanen, yang mana riwayat, cookies, dan data situs lainnya akan selalu dihapus setiap kali browser ditutup. Bookmark, pengaturan browser, dan pengaturan ekstensi Anda akan tetap dipertahankan.

Hal ini diperlukan untuk mencegah bentuk pelacakan tingkat lanjut, tetapi harus mengorbankan kenyamanan dan beberapa fitur Firefox seperti Multi-Account Containers. Ingatlah bahwa Anda selalu dapat menggunakan beberapa browser lain. Misalnya Anda dapat mempertimbangkan untuk menggunakan Firefox+Arkenfox untuk beberapa situs yang ingin Anda tetap masuk atau yang tidak berfungsi dengan baik di Mullvad Browser. Lalu menggunakan Mullvad Browser untuk penjelajahan umum.

### Mullvad Leta

Mullvad Browser dilengkapi dengan [**Mullvad Leta**](search-engines.md#mullvad-leta) sebagai mesin pencari default, yang berfungsi sebagai proteksi untuk hasil pencarian Google atau Brave (dapat dikonfigurasi di beranda Mullvad Leta).

Jika Anda adalah pengguna VPN Mullvad, ada beberapa risiko dalam menggunakan layanan seperti Mullvad Leta yang ditawarkan oleh penyedia VPN Anda sendiri. Ini karena Mullvad secara teoritis memiliki akses ke alamat IP Anda yang sebenarnya (melalui VPN mereka) dan aktifitas pencarian Anda (melalui Leta); yang terakhir ini adalah informasi yang biasanya dimaksudkan untuk dipisahkan oleh VPN. Meskipun mullvad mengumpulkan sangat sedikit informasi tentang pelanggan VPN mereka atau pengguna Leta, Anda sebaiknya mempertimbangkan [mesin pencari](search-engines.md) yang berbeda jika risiko ini menjadi perhatian Anda.

## Firefox

<div class="admonition recommendation" markdown>

![Logo Firefox](assets/img/browsers/firefox.svg){ align=right }

**Firefox** menyediakan pengaturan privasi yang kuat seperti [Perlindungan Pelacakan yang Ditingkatkan](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), yang dapat membantu memblokir berbagai [jenis pelacakan](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Halaman Utama](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Kebijakan Privasi" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Dokumentasi }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Kode Sumber }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Kontribusi" }

<details class="downloads" markdown>
<summary>Unduhan</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Peringatan</p>

Firefox menyertakan [token unduhan](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) unik dalam unduhan dari situs web Mozilla dan menggunakan telemetry di Firefox untuk mengirimkan token tersebut. Token ini **tidak** disertakan dalam rilis dari [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Konfigurasi Firefox yang Direkomendasikan

Opsi ini dapat ditemukan di :material-menu: → **Pengaturan**.

#### Search

- [ ] Hapus centang **Show search suggestions**

Fitur saran pencarian mungkin tidak tersedia di wilayah Anda.

Saran pencarian mengirimkan semua yang Anda ketik di bilah alamat ke mesin pencarian default, terlepas dari apakah Anda mengirimkan pencarian yang sebenarnya. Dengan menonaktifkan saran pencarian, Anda dapat mengontrol data yang Anda kirimkan ke penyedia mesin pencari dengan lebih tepat.

##### Firefox Suggest (hanya di AS)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) adalah fitur yang mirip dengan saran pencarian yang hanya tersedia di AS. Kami sarankan untuk menonaktifkannya karena alasan yang sama dengan menonaktifkan saran pencarian. Jika Anda tidak melihat opsi-opsi ini di bawah tajuk **Address Bar**, Anda tidak memiliki "new experience" dan dapat mengabaikan perubahan ini.

- [ ] Hapus centang **Suggestions from Firefox**
- [ ] Hapus centang **Suggestions from sponsors**

#### Privasi & Keamanan

##### Perlindungan Pelacakan yang Ditingkatkan

- [x] Pilih **Strict** Enhanced Tracking Protection

Ini melindungi Anda dengan memblokir pelacak media sosial, skrip fingerprinting (perhatikan bahwa ini tidak melindungi Anda dari *semua* fingerprinting), cryptominers, cross-site tracking cookies, dan beberapa konten pelacakan lainnya. ETP melindungi dari banyak ancaman umum, tetapi tidak memblokir semua jalan pelacakan karena dirancang untuk memiliki dampak minimal atau bahkan tidak berdampak pada kegunaan situs.

##### Sanitize on Close

Jika Anda ingin tetap masuk ke situs tertentu, Anda dapat mengizinkan pengecualian di **Cookies and Site Data**→**Manage Exception...**

- [x] Centang **Delete cookies and site data when Firefox is closed**

Ini melindungi Anda dari cookie yang persisten, tetapi tidak melindungi Anda dari cookie yang diperoleh selama satu sesi penjelajahan. Ketika ini diaktifkan, Anda dapat dengan mudah membersihkan cookie peramban Anda hanya dengan memulai ulang Firefox. Anda dapat mengatur pengecualian per situs, jika Anda ingin tetap masuk ke situs tertentu yang sering Anda kunjungi.

##### Telemetry

- [ ] Hapus centang **Allow Firefox to send technical and interaction data to Mozilla**
- [ ] Hapus centang **Allow Firefox to install and run studies**
- [ ] Hapus centang **Allow Firefox to send backlogged crash reports on your behalf**

Menurut kebijakan privasi Mozilla untuk Firefox,

> Firefox mengrimkan data tentang versi dan bahas Firefox Anda; sistem operasi perangkat dan konfigurasi perangkat keras; memori, informasi dasar tentang kerusakan dan kesalahan; hasil dari proses otomatis seperti pembaruan, penelusuran aman, dan aktivasi kepada kami. Ketika Firefox mengrimkan data kepada kami, alamat IP Anda dikumpulkan untuk sementara sebagai bagian dari log server kami.

Selain itu, layanan Akun Mozilla mengumpulkan [beberapa data teknis](https://mozilla.org/privacy/mozilla-accounts). Jika Anda menggunakan Akun Mozilla, Anda dapat memilih untuk tidak ikut serta:

1. Buka [pengaturan profil Anda di accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Hapus centang pada **Data Collection and Use**>**Help improve Firefox Accounts**

##### Preferensi Iklan Situs Web

- [ ] Hapus centang **Allow websites to perform privacy-preserving ad measurement**

Dengan rilis Firefox 128, pengaturan baru untuk [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) telah ditambahkan dan [diaktifkan secara default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA memungkinkan pengiklan untuk menggunakan browser web Anda untuk mengukur efektivitas kampanye web, alih-alih menggunakan pelacakan berbasis JavaScript tradisional. Kami menganggap perilaku ini berada di luar cakupan tanggung jawab agen pengguna, dan fakta bahwa fitur ini dinonaktifkan secara default di Arkenfox merupakan indikator tambahan untuk menonaktifkan fitur ini.

##### Mode HTTPS-Only

- [x] Pilih **Enable HTTPS-Only Mode in all windows**

Hal ini mencegah Anda secara tidak sengaja tersambung ke situs web dalam HTTP teks biasa. Situs-situs tanpa HTTPS sudah jarang ditemukan saat ini, jadi hal ini seharusnya hanya berdampak kecil atau bahkan tidak berdampak sama sekali pada penjelajahan Anda sehari-hari.

##### DNS over HTTPS

Jika Anda menggunakan [DNS over HTTPS provider](dns.md):

- [x] Pilih **Max Protection** dan pilih penyedia yang sesuai

Max Protection memberlakukan penggunaan DNS over HTTPS, dan peringatan keamanan akan muncul jika Firefox tidak dapat tersambung ke secure DNS resolver Anda, atau jika secure DNS resolver Anda mengatakan bahwa catatan untuk domain yang Anda coba akses tidak ada. Ini akan menghentikan jaringan yang Anda sambungkan untuk secara diam-diam menurunkan keamanan DNS anda.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) memungkinkan data penjelajahan Anda (riwayat, penanda, dll.) dapat diakses di semua perangkat dan melindunginya dengan E2EE.

### Arkenfox (lanjutan)

<div class="admonition tip" markdown>
<p class="admonition-title">Gunakan Mullvad Browser untuk anti-fingerprinting tingkat lanjut</p>

[Mullvad Browser](#mullvad-browser) menyediakan proteksi anti-fingerprinting yang sama dengan Arkenfox, dan tidak memerlukan penggunaan Mullvad VPN untuk mendapatkan manfaat dari proteksi ini. Ditambah dengan VPN, Mullvad Browser bisa menggagalkan skrip pelacakan yang lebih canggih yang tidak bisa dilakukan oleh Arkenfox. Arkenfox masih memiliki keunggulan karena jauh lebih fleksibel, dan mengizinkan pengecualian per situs untuk situs web yang harus Anda masuki.

</div>

[Proyek Arkenfox](https://github.com/arkenfox/user.js) menyediakan seperangkat opsi yang dipertimbangkan dengan cermat untuk Firefox. Jika Anda [memutuskan](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) untuk menggunakan Arkenfox, [beberapa opsi](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) secara subyektif sangat ketat dan/atau dapat menyebabkan beberapa situs web tidak berfungsi dengan baik—yang dapat Anda [ubah dengan mudah](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) untuk memenuhi kebutuhan Anda. Kami **sangat menyarankan untuk** membaca [wiki](https://github.com/arkenfox/user.js/wiki) lengkap mereka. Arkenfox juga memungkinkan dukungan [kontainer](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox hanya bertujuan untuk menggagalkan skrip pelacakan dasar atau naif melalui pengacakan kanvas dan pengaturan konfigurasi resistensi fingerprint bawaan Firefox. Browser ini tidak bertujuan untuk membuat browser Anda berbaur dengan kerumunan besar pengguna Arkenfox lainnya dengan cara yang sama seperti yang dilakukan oleh Mullvad Browser atau Tor Browser, yang merupakan satu-satunya cara untuk menggagalkan skrip pelacakan fingerprint tingkat lanjut. Ingatlah bahwa Anda selalu dapat menggunakan beberapa browser, misalnya, Anda dapat mempertimbangkan untuk menggunakan Firefox-Arkenfox untuk beberapa situs yang Anda ingin tetap masuk atau percayai, dan Mullvad Browser untuk penjelajahan umum.

## Brave

<div class="admonition recommendation annotate" markdown>

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

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave menambahkan "[kode rujukan](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" pada nama berkas dalam unduhan dari situs web Brave, yang digunakan untuk melacak dari sumber mana peramban tersebut diunduh, misalnya `BRV002` dalam unduhan yang bernama `Brave-Browser-BRV002.pkg`. Penginstal kemudian akan melakukan ping ke server Brave dengan kode rujukan di akhir proses instalasi. Jika Anda khawatir tentang hal ini, Anda dapat mengganti nama berkas penginstal sebelum membukanya.

</div>

### Konfigurasi Brave yang Direkomendasikan

Opsi ini dapat ditemukan di :material-menu: → **Pengaturan**.

#### Shields

Brave menyertakan beberapa langkah anti-fingerprinting dalam fitur [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Kami menyarankan untuk mengonfigurasi opsi-opsi ini [secara global](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) di semua halaman yang Anda kunjungi.

Opsi Shields dapat diturunkan pada basis per situs sesuai kebutuhan, tetapi secara default kami sarankan untuk mengatur yang berikut ini:

<div class="annotate" markdown>

- [x] Pilih **Aggressive** di bawah "Trackers & and blocking"

<details class="warning" markdown>
<summary>Gunakan daftar filter default</summary>

Brave memungkinkan Anda untuk memilih filter konten tambahan di dalam halaman `brave://adblock` internal. Kami menyarankan agar Anda tidak menggunakan fitur ini; sebagai gantinya, pertahankan daftar filter default. Menggunakan daftar tambahan akan membuat Anda terlihat berbeda dari pengguna Brave lainnya dan juga dapat meningkatkan permukaan serangan jika ada eksploitasi di Brave dan aturan berbahaya ditambahkan ke salah satu daftar yang Anda gunakan.

</details>

- [x] Pilih **Strict** di bawah *Upgrade connections to HTTPS*
- [x] (Opsional) Pilih **Block Scripts** (1)
- [x] Centang **Block fingerprinting**
- [x] Pilih **Block third-party cookies**
- [x] Centang **Forget me when I close this site** (2)
- [ ] Hapus centang pada semua komponen media sosial

</div>

1. Opsi ini menonaktifkan JavaScript, yang akan merusak banyak situs. Untuk memperbaikinya, Anda dapat mengatur pengecualian per situs dengan mengklik ikon perisai pada bilah alamat dan menghapus centang pada pengaturan ini di bawah *Advance controls*.
2. Jika Anda ingin tetap masuk ke situs tertentu yang sering Anda kunjungi, Anda dapat mengatur pengecualian per situs dengan mengklik ikon perisai di bilah alamat dan mengahapus centang pada pengaturan ini dibawah *Advanced controls*.

#### Privacy and security

<div class="annotate" markdown>

- [x] Pilih **Don’t allow sites to use JavaScript optimization** di bawah *Security* → *Manage JavaScript optimization & security* (1)
- [x] Pilih **Automatically remove permissions from unused sites** di bawah *Sites and Shields Settings*
- [x] Pilih **Disable non-proxied UDP** di bawah [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Hapus centang **Use Google services for push messaging**
- [x] Pilih **Auto-redirect AMP pages**
- [x] Pilih **Auto-redirect tracking URLs**
- [x] Pilih **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Menonaktifkan pengoptimal V8 mengurangi permukaan serangan Anda dengan menonaktifkan [*beberapa*](https://grapheneos.social/@GrapheneOS/112708049232710156) bagian dari kompilasi JavaScript Just-In-Time (JIT).

##### Tow windows

[**Private window dengan Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) memungkinkan Anda untuk merutekan lalu lintas Anda melalui jaringan Tor di Private Windows dan mengakses layanan .onion, yang mungkin berguna dalam beberapa kasus. Namun, Brave **tidak** tahan terhadap fingerprinting seperti halnya Tor Browser, dan jauh lebih sedikit orang yang menggunakan Brave dengan Tor, jadi Anda akan lebih menonjol. Jika model ancaman Anda membutuhkan anonimitas yang kuat, gunakan [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Hapus centang **Allow privacy-preserving product analytics (P3A)**
- [ ] Hapus centang **Automatically send daily usage ping to Brave**
- [ ] Hapus centang **Automatically send diagnostic reports**

#### Web3

Fitur Web3 Brave berpotensi manambah fingerprinting browser Anda dan permukaan serangan. Kecuali jika Anda menggunakan salah satu fitur ini, fitur-fitur tersebut harus dinonaktifkan.

- Pilih **Extensions (no fallback)** di bawah *Default Ethereum wallet*
- Pilih **Extensions (no fallback)** di bawah *Default Solana wallet*

#### Ekstensi

- [ ] Hapus centang semua ekstensi bawaan yang tidak Anda gunakan

#### Mesin pencari

Kami menyarankan untuk menonaktifkan saran pencarian di Brave untuk alasan yang sama dengan menonaktifkan fitur ini di [Firefox](#search).

- [ ] Hapus centang **Show search suggestions**

#### Sistem

<div class="annotate" markdown>

- [ ] Hapus centang **Continue running background apps when Brave is closed** untuk menonaktifkan aplikasi latar belakang (1)

</div>

1. Opsi ini tidak ada pada semua platform.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

### Persyaratan Minimum

- Harus berupa perangkat lunak sumber terbuka.
- Must support automatic updates.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Kasus Terbaik

Kriteria kasus terbaik kami mewakili apa yang ingin kami lihat dari proyek yang sempurna dalam kategori ini. Rekomendasi kami mungkin tidak menyertakan salah satu atau semua fungsi ini, tetapi rekomendasi yang menyertakan fungsi ini mungkin memiliki peringkat yang lebih tinggi daripada yang lain di halaman ini.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps (PWAs). PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
