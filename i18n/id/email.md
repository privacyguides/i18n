---
meta_title: "Rekomendasi Email Pribadi Terenkripsi - Privacy Guides"
title: Layanan Email
icon: material/email
description: Penyedia email ini menawarkan tempat yang baik untuk menyimpan email Anda dengan aman, dan banyak yang menawarkan enkripsi OpenPGP yang dapat dioperasikan dengan penyedia lain.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Melindungi dari ancaman(s) berikut ini:</small>

- [:material-server-network: Penyedia Layanan](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Email bisa dibilang merupakan kebutuhan untuk menggunakan layanan daring apa pun, namun kami tidak merekomendasikannya untuk percakapan antar orang. Daripada menggunakan email untuk menghubungi orang lain, pertimbangkan untuk menggunakan media pesan instan yang mendukung kerahasiaan penerusan.

[Pengirim Pesan Instan yang Direkomendasikan](real-time-communication.md ""){.md-button}

## Penyedia yang Direkomendasikan

Untuk yang lainnya, kami merekomendasikan berbagai penyedia surel yang didasarkan pada model bisnis yang berkelanjutan serta fitur keamanan dan privasi bawaan. Baca [daftar lengkap kriteria](#criteria) kami untuk informasi lebih lanjut.

| Penyedia                      | OpenPGP / WKD                          | IMAP / SMTP                                                     | Zero-Access Encryption                                | Metode Pembayaran Anonim                         |
| ----------------------------- | -------------------------------------- | --------------------------------------------------------------- | ----------------------------------------------------- | ------------------------------------------------ |
| [Proton Mail](#proton-mail)   | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Hanya paket berbayar | :material-check:{ .pg-green }                         | Uang Tunai                                       |
| [MailBox Mail](#mailbox-mail) | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                   | :material-information-outline:{ .pg-blue } Hanya mail | Uang Tunai                                       |
| [Tuta](#tuta)                 | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                          | :material-check:{ .pg-green }                         | Monero <br>Uang tunai melalui pihak ketiga |

Selain (atau sebagai pengganti) penyedia email yang direkomendasikan di sini, Anda mungkin ingin mempertimbangkan [layanan aliasing email](email-aliasing.md#recommended-providers) khusus untuk melindungi privasi Anda. Di antaranya, layanan-layanan ini dapat membantu melindungi kotak masuk asli Anda dari spam, mencegah para pemasar menghubungkan akun-akun Anda, dan mengenkripsi semua pesan yang masuk dengan PGP.

- [Informasi Lebih Lanjut :material-arrow-right-drop-circle:](email-aliasing.md)

## Layanan yang Kompatibel dengan OpenPGP

Penyedia layanan ini secara native mendukung enkripsi/dekripsi OpenPGP dan [standar Web Key Directory (WKD)](basics/email-security.md#what-is-the-web-key-directory-standard), yang memungkinkan email terenkripsi ujung ke ujung yang bersifat penyedia-agnostik. Sebagai contoh, pengguna Proton Mail dapat mengirim pesan E2EE ke pengguna Mailbox Mail, atau Anda dapat mengirim notifikasi terenkripsi OpenPGP dari layanan internet yang mendukungnya.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](#proton-mail)
- ![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ .twemoji } [Mailbox Mail](#mailbox-mail)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Peringatan</p>

Ketika menggunakan teknologi E2EE seperti OpenPGP, email Anda akan tetap memiliki beberapa metadata yang tidak terenkripsi di header email, umumnya termasuk baris subjek! Baca lebih lanjut tentang [metadata email](basics/email-security.md#email-metadata-overview).

OpenPGP juga tidak mendukung forward secrecy, yang berarti jika kunci privat Anda atau penerima pesan dicuri, semua pesan sebelumnya yang dienkripsi dengan kunci tersebut akan terekspos.

- [Bagaimana cara melindungi kunci pribadi saya?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** adalah layanan email dengan fokus pada privasi, enkripsi, keamanan, dan kemudahan penggunaan. Mereka telah beroperasi sejak tahun 2013. Proton AG berbasis di Geneva, Switzerland.

Paket Proton Free hadir dengan penyimpanan Mail sebesar 500 MB, yang dapat Anda tingkatkan hingga 1 GB secara gratis.

[:octicons-home-16: Halaman Utama](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Layanan Onion" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="Kebijakan Privasi" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="Dokumentasi" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Kode Sumber" }

<details class="downloads" markdown>
<summary>Unduhan</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Akun gratis memiliki beberapa keterbatasan, seperti tidak dapat mencari teks di body email dan tidak memiliki akses ke [Proton Mail Bridge](https://proton.me/mail/bridge), yang diperlukan untuk menggunakan [klien email desktop yang direkomendasikan](email-clients.md) (misalnya Thunderbird). Akun berbayar mencakup fitur-fitur seperti Proton Mail Bridge, penyimpanan tambahan, dan dukungan domain khusus. Jika Anda memiliki paket Proton Unlimited atau paket Proton multi-user, Anda juga mendapatkan [SimpleLogin](email-aliasing.md#simplelogin) Premium secara gratis.

[Surat pengesahan](https://proton.me/blog/security-audit-all-proton-apps) diberikan untuk aplikasi Proton Mail pada tanggal 9 November 2021 oleh [Securitum](https://research.securitum.com).

Proton Mail memiliki laporan crash internal yang **tidak** dibagikan dengan pihak ketiga. Hal ini dapat dinonaktifkan di aplikasi web: :gear: → **All Settings** → **Account** → **Security and privacy** → **Privacy and data collection**.

#### :material-check:{ .pg-green } Domain dan Alias Khusus

Pelanggan Proton Mail berbayar dapat menggunakan domain mereka sendiri dengan layanan ini atau alamat [catch-all](https://proton.me/support/catch-all). Proton Mail juga mendukung [sub-addressing](https://proton.me/support/creating-aliases), yang berguna bagi orang-orang yang tidak ingin membeli domain.

#### :material-check:{ .pg-green } Metode Pembayaran Pribadi

Proton Mail [menerima](https://proton.me/support/payment-options)**tunai** melalui pos selain kartu kredit/debit standar, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), dan PayPal.

#### :material-check:{ .pg-green } Keamanan Akun

Proton Mail mendukung [two-factor authentication](https://proton.me/support/two-factor-authentication-2fa) TOTP dan [kunci keamanan perangkat keras](https://proton.me/support/2fa-security-key) menggunakan standar FIDO2 atau U2F. Penggunaan kunci keamanan perangkat keras memerlukan pengaturan TOTP two-factor authentication terlebih dahulu.

#### :material-check:{ .pg-green } Keamanan Data

Proton Mail memiliki [zero-access encryption](https://proton.me/blog/zero-access-encryption) untuk email dan [kalender](https://proton.me/news/protoncalendar-security-model) Anda. Data yang diamankan dengan zero-access encryption hanya dapat diakses oleh Anda.

Informasi tertentu yang disimpan di [Proton Contacts](https://proton.me/support/proton-contacts), seperti nama tampilan dan alamat email, tidak diamankan dengan zero-access encryption. Bidang kontak yang mendukung zero-access encryption, seperti nomor telepon, ditunjukkan dengan ikon gembok.

#### :material-check:{ .pg-green } Enkripsi Email

Proton Mail telah [mengintegrasikan enkripsi OpenPGP](https://proton.me/support/how-to-use-pgp) di webmail mereka. Email ke akun Proton Mail lainnya dienkripsi secara otomatis, dan enkripsi ke alamat non-Proton Mail dengan kunci OpenPGP dapat diaktifkan dengan mudah di pengaturan akun Anda. Proton juga mendukung external key discovery otomatis dengan WKD. Ini berarti bahwa email yang dikirim ke penyedia lain yang menggunakan WKD akan secara otomatis dienkripsi dengan OpenPGP juga, tanpa perlu secara manual menukar kunci PGP publik dengan kontak Anda. Mereka juga memungkinkan Anda untuk [mengenkripsi pesan ke alamat non-Proton Mail tanpa OpenPGP](https://proton.me/support/password-protected-emails), tanpa perlu mendaftar untuk akun Proton Mail.

Proton Mail juga mempublikasikan kunci publik akun Proton melalui HTTP dari WKD mereka. Hal ini memungkinkan orang yang tidak menggunakan Proton Mail untuk menemukan kunci OpenPGP akun Proton Mail dengan mudah untuk E2EE lintas penyedia. Ini hanya berlaku untuk alamat email yang diakhiri dengan salah satu domain Proton, seperti `@proton.me`. Jika Anda menggunakan domain khusus, Anda harus [mengonfigurasi WKD](basics/email-security.md#what-is-the-web-key-directory-standard) secara terpisah.

#### :material-information-outline:{ .pg-blue } Penghentian Akun

Jika Anda memiliki akun berbayar dan [tagihan Anda belum dibayar](https://proton.me/support/delinquency) setelah 14 hari, Anda tidak akan dapat mengakses data Anda. Setelah 30 hari, akun Anda akan menunggak dan tidak akan menerima email masuk. Anda akan terus ditagih selama periode ini. Proton akan [menghapus akun gratis yang tidak aktif](https://proton.me/support/inactive-accounts) setelah satu tahun. Anda **tidak dapat** menggunakan kembali alamat email dari akun yang telah dinonaktifkan.

#### :material-information-outline:{ .pg-blue } Fungsionalitas Tambahan

Paket [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) Proton Mail juga memungkinkan akses ke layanan Proton lainnya selain menyediakan beberapa domain khusus, alias hide-my-email tanpa batas, dan penyimpanan 500 GB.

### MailBox Mail

<div class="admonition recommendation" markdown>

![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ align=right }

**Mailbox Mail** adalah layanan email yang berfokus pada keamanan, bebas iklan, dan didukung oleh 100% energi ramah lingkungan. Mereka telah beroperasi sejak tahun 2014. Mailbox Mail berbasis di Berlin, Germany.

Akun dimulai dengan penyimpanan hingga 2 GB, yang dapat ditingkatkan sesuai kebutuhan.

[:octicons-home-16: Halaman Utama](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Kebijakan Privasi" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Dokumentasi" }

<details class="downloads" markdown>
<summary>Unduhan</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Domain dan Alias Khusus

Mailbox Mail memungkinkan Anda menggunakan domain Anda sendiri, dan mereka mendukung alamat [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name). Mailbox Mail juga mendukung [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), yang berguna jika Anda tidak ingin membeli domain.

#### :material-check:{ .pg-green } Metode Pembayaran Pribadi

Mailbox Mail tidak menerima mata uang kripto apa pun karena prosesor pembayaran mereka, BitPay menangguhkan operasinya di German. Namun, mereka menerima **uang tunai** melalui pos, pembayaran **tunai** ke rekening bank, transfer bank, kartu kredit, PayPal, dan beberapa prosesor khusus German: Paydirekt dan Sofortüberweisung.

#### :material-check:{ .pg-green } Keamanan Akun

MailBox Mail mendukung [two-factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) hanya untuk webmail mereka. Anda dapat menggunakan TOTP atau [YubiKey](security-keys.md#yubikey) melalui [YubiCloud](https://yubico.com/products/services-software/yubicloud). Standar web seperti [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) belum didukung.

#### :material-information-outline:{ .pg-blue } Keamanan Data

Mailbox Mail memungkinkan enkripsi email masuk menggunakan [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Pesan baru yang Anda terima akan segera dienkripsi dengan kunci publik Anda.

Namun, [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), platform perangkat lunak yang digunakan oleh Mailbox Mail, [tidak mendukung](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) enkripsi buku alamat dan kalender Anda. [Opsi mandiri](calendar.md) mungkin lebih tepat untuk data tersebut.

#### :material-check:{ .pg-green } Enkripsi Email

Mailbox Mail telah [mengintegrasikan enkripsi](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) di webmail mereka, yang menyederhanakan pengiriman pesan ke orang-orang dengan kunci OpenPGP publik. Mereka juga memungkinkan [penerimaan jarak jauh untuk mendekripsi email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) di server Mailbox Mail. Fitur ini berguna ketika penerima jarak jauh tidak memiliki OpenPGP dan tidak dapat mendekripsi salinan email di kotak surat mereka sendiri.

Mailbox Mail juga mendukung discovery kunci publik melalui HTTP dari WKD mereka. Hal ini memungkinkan orang di luar Mailbox Mail untuk menemukan kunci OpenPGP dari akun Mailbox Mail dengan mudah untuk E2EE lintas penyedia. Ini hanya berlaku untuk alamat email yang berakhiran dengan salah satu domain Mailbox Mail sendiri, seperti `@mailbox.org`. Jika Anda menggunakan domain khusus, Anda harus [mengonfigurasi WKD](basics/email-security.md#what-is-the-web-key-directory-standard) secara terpisah.

#### :material-information-outline:{ .pg-blue } Penghentian Akun

Akun Anda diatur ke akun pengguna terbatas ketika kontrak Anda berakhir. Data ini akan dihapus secara permanen setelah [30 hari](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Fungsionalitas Tambahan

Anda dapat mengakses akun Mailbox Mail Anda melalui IMAP/SMTP menggunakan layanan [.onion](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Namun, antarmuka webmail mereka tidak dapat diakses melalui layanan .onion mereka, dan Anda mungkin mangalami kesalahan sertifikat TLS.

Semua akun dilengkapi penyimpanan awan terbatas yang [dapat dienkripsi](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox Mail juga menawarkan alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), yang memberlakukan enkripsi TLS pada koneksi antara server email, jika tidak, pesan tidak akan terkirim sama sekali. Mailbox Mail juga mendukung [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) selain protokol akses standar seperti IMAP dan POP3.

Mailbox Mail memiliki fitur warisan digital untuk semua paket. Anda dapat memilih apakah Anda ingin data Anda diwariskan kepada ahli waris, asalkan mereka mengajukan permohonan dan memberikan surat wasiat Anda. Sebagai alternatif, Anda dapat menominasikan seseorang berdasarkan nama dan alamat.

## Penyedia Lainnya

Penyedia ini menyimpan email Anda dengan zero-knowledge encryption, menjadikannya pilihan yang bagus untuk menjaga email yang tersimpan tetap aman. Namun, mereka tidak mendukung standar enkripsi yang dapat dioperasikan untuk komunikasi E2EE antara penyedia yang berbeda.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (sebelumnya bernama *Tutanota*) adalah layanan email berfokus pada keamanan dan privasi melalui penggunaan enkripsi. Tuta telah beroperasi sejak tahun 2011 dan berbasis di Hanover, Germany.

Akun gratis dimulai dengan penyimpanan 1 GB.

:octicons-home-16: Halaman Utama](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Kebijakan Privasi" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="Dokumentasi" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Kode Sumber" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="Kontribusi" }

<details class="downloads" markdown>
<summary>Unduhan</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta tidak mendukung [protokol IMAP](https://tuta.com/support#imap) atau penggunaan [klien email](email-clients.md) pihak ketiga, dan Anda juga tidak dapat menambahkan [akun email eksternal](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) ke aplikasi Tuta. [Impor email](https://github.com/tutao/tutanota/issues/630) saat ini juga tidak didukung, meskipun hal ini [akan diubah](https://tuta.com/blog/kickoff-import). Email dapat diekspor satu per satu [atau dengan pemilihan massal](https://tuta.com/support#generalMail) per folder, yang mungkin merepotkan jika Anda memiliki banyak folder.

#### :material-check:{ .pg-green } Domain dan Alias Khusus

Akun Tuta berbayar dapat menggunakan 15 atau 30 alias tergantung pada paket mereka dan alias tak terbatas pada [domain kustom](https://tuta.com/support#custom-domain). Tuta tidak mengizinkan [sub-addressing (plus addresses)](https://tuta.com/support#plus), tetapi Anda bisa menggunakan [catch-all](https://tuta.com/support#settings-global) dengan domain kustom.

#### :material-information-outline:{ .pg-blue } Metode Pembayaran Pribadi

Tuta hanya menerima kartu kredit dan PayPal secara langsung, namun [**mata uang kripto**](cryptocurrency.md) dapat digunakan untuk membeli kartu hadiah melalui [kemitraan](https://tuta.com/support/#cryptocurrency) dengan ProxyStore.

#### :material-check:{ .pg-green } Keamanan Akun

Tuta mendukung [two-factor authentication](https://tuta.com/support#2fa) dengan TOTP atau U2F.

#### :material-check:{ .pg-green } Keamanan Data

Tuta memiliki [zero-access encryption](https://tuta.com/support#what-encrypted) untuk email Anda, [kontak buku alamat](https://tuta.com/support#encrypted-address-book), dan [kalender](https://tuta.com/support#calendar). Ini berarti pesan dan data lain yang tersimpan di akun Anda hanya dapat dibaca oleh Anda.

#### :material-information-outline:{ .pg-blue } Enkripsi Email

Tuta [tidak menggunakan OpenPGP](https://tuta.com/support/#pgp). Akun Tuta hanya bisa menerima email terenkripsi dari akun non-Tuta ketika dikirim melalui [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Penghentian Akun

Tuta akan [menghapus akun gratis yang tidak aktif](https://tuta.com/support#inactive-accounts) setelah enam bulan. Anda dapat menggunakan kembali akun gratis yang telah dinonaktifkan jika Anda membayar.

#### :material-information-outline:{ .pg-blue } Fungsionalitas Tambahan

Tuta menawarkan versi bisnis [Tuta untuk organisasi nirlaba](https://tuta.com/blog/secure-email-for-non-profit) secara gratis atau dengan diskon besar.

## Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan penyedia yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk setiap penyedia email yang ingin direkomendasikan, termasuk menerapkan praktik terbaik industri, teknologi modern, dan banyak lagi. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih penyedia email, dan melakukan penelitian sendiri untuk memastikan penyedia email yang Anda pilih adalah pilihan yang tepat untuk Anda.

### Teknologi

Kami menganggap fitur-fitur ini penting untuk memberikan layanan yang aman dan optimal. Anda harus mempertimbangkan apakah penyedia memiliki fitur yang Anda butuhkan.

**Minimum untuk Memenuhi Syarat:**

- Harus mengenkripsi data akun email saat tidak aktif dengan zero-access encryption.
- Harus mampu mengekspor email sebagai [Mbox](https://en.wikipedia.org/wiki/Mbox) atau .EML individual dengan standar [RFC5322](https://datatracker.ietf.org/doc/rfc5322).
- Izinkan pengguna untuk menggunakan [nama domain](https://en.wikipedia.org/wiki/Domain_name) mereka sendiri. Nama domain khusus penting bagi pengguna karena memungkinkan mereka untuk mempertahankan keagenan meraka dari layanan, jika layanan berubah menjadi buruk atau diakuisisi oleh perusahaan lain yang tidak memprioritaskan privasi.
- Harus beroperasi pada infrastruktur milik sendiri, yaitu tidak dibangun di atas penyedia layanan email pihak ketiga.

**Kasus Terbaik:**

- Harus mengenkripsi semua data akun (kontak, kalender, dll.) saat tidak digunakan dengan zero-access encryption.
- Harus menyediakan enkripsi E2EE/PGP webmail yang terintegrasi sebagai kenyamanan.
- Harus mendukung WKD untuk memungkinkan penemuan kunci OpenPGP publik yang lebih baik melalui HTTP. Pengguna GnuPG dapat memperoleh kunci dengan perintah `gpg --locate-key example_user@example.com`.
- Dukungan untuk temporary mailbox untuk pengguna eksternal. Ini berguna ketika Anda ingin mengirim email terenkripsi tanpa mengirimkan salinan yang sebenarnya kepada penerima. Email ini biasanya memiliki masa berlaku terbatas dan kemudian dihapus secara otomatis. Mereka juga tidak mengharuskan penerima untuk mengonfigurasi kriptografi apa pun seperti OpenPGP.
- Harus mendukung [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Harus mengizinkan pengguna untuk menggunakan [nama domain](https://en.wikipedia.org/wiki/Domain_name) mereka sendiri. Nama domain khusus penting bagi pengguna karena memungkinkan mereka untuk mempertahankan keagenan mereka dari layanan, jika layanan berubah menjadi buruk atau diakuisisi oleh perusahaan lain yang tidak memprioritaskan privasi.
- Fungsionalitas catch-all atau alias bagi mereka yang menggunakan domain sendiri.
- Sebaiknya gunakan protokol akses email standar seperti IMAP, SMTP, atau [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Protokol akses standar memastikan pelanggan dapat dengan mudah mengunduh semua email mereka, jika mereka ingin beralih ke penyedia lain.
- Layanan penyedia email harus tersedia melalui [layanan onion](https://en.wikipedia.org/wiki/.onion).

### Privasi

Kami lebih memilih penyedia yang kami rekomendasikan untuk mengumpulkan data sesedikit mungkin.

**Minimum untuk Memenuhi Syarat:**

- Harus melindungi alamat IP pengirim, yang dapat berupa penyaringan agar tidak ditampilkan di bidang header `Received`.
- Tidak boleh meminta informasi identitas pribadi (PII) selain nama pengguna dan kata sandi.
- Kebijakan privasi harus memenuhi persyaratan yang ditentukan oleh GDPR.

**Kasus Terbaik:**

- Harus menerima [opsi pembayaran anonim](advanced/payments.md) ([mata uang kripto](cryptocurrency.md), uang tunai, kartu hadiah, dll.)
- Harus di-host di yuridiksi dengan undang-undang perlindungan privasi email yang kuat.

### Keamanan

Server email berurusan dengan banyak data yang sangat sensitif. Kami berharap penyedia layanan akan mengadopsi praktik terbaik industri untuk melindungi pelanggan mereka.

**Minimum untuk Memenuhi Syarat:**

- Perlindungan webmail dengan 2FA, seperti [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, yang dibangun di atas enkripsi saat tidak digunakan. Penyedia tidak memiliki kunci dekripsi untuk data yang mereka miliki. Hal ini mencegah karyawan nakal membocorkan data yang mereka miliki atau musuh jarak jauh merilis data yang telah mereka curi dengan mendapatkan akses tidak sah ke server.
- Dukungan [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Tidak ada kesalahan atau kerentanan TLS saat diprofilkan oleh alat-alat seperti [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), atau [Qualys SSL Labs](https://ssllabs.com/ssltest); ini termasuk kesalahan terkait sertifikat dan parameter DH yang lemah, seperti yang menyebabkan [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Preferensi rangkaian server (opsional pada TLS 1.3) untuk rangkaian sandi yang kuat yang mendukung forward secrecy dan enkripsi yang diautentikasi.
- Kebijakan [MTA-STS](https://tools.ietf.org/html/rfc8461) dan [TLS-RPT](https://tools.ietf.org/html/rfc8460) yang masih berlaku.
- Catatan [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) yang valid.
- Catatan [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) dan [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) yang valid.
- Harus memiliki catatan dan kebijakan [DMARC](https://en.wikipedia.org/wiki/DMARC) yang tepat atau menggunakan [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) untuk otentikasi. Jika autentikasi DMARC digunakan, kebijakan harus diatur untuk `reject` atau `quarantine`.
- Preferensi paket server TLS 1.2 atau yang lebih baru dan paket untuk [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- Pengiriman [SMTPS](https://en.wikipedia.org/wiki/SMTPS), dengan asumsi menggunakan SMTP.
- Standar keamanan situs web seperti:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) jika memuat sesuatu dari domain eksternal.
- Harus mendukung tampilan [message header](https://en.wikipedia.org/wiki/Email#Message_header), karena ini adalah fitur forensik yang penting untuk menentukan apakah sebuah email merupakan upaya phishing.

**Kasus Terbaik:**

- Harus mendukung autentikasi perangkat keras, yaitu. E2F dan [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) sebagai tambahan untuk dukungan DANE.
- Harus mengimplementasikan [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), yang berguna bagi orang-orang yang mengirim ke milis [RFC8617](https://tools.ietf.org/html/rfc8617).
- Audit keamanan yang dipublikasikan dari perusahaan pihak ketiga yang memiliki reputasi baik.
- Program bug-bounty dan/atau proses pengungkapan kerentanan yang terkoordinasi.
- Standar keamanan situs web seperti:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Kepercayaan

Anda tidak akan mempercayakan keuangan Anda kepada seseorang dengan identitas palsu, jadi mengapa mempercayakan email Anda kepada mereka? Kami mewajibkan penyedia layanan yang kami rekomendasikan untuk terbuka mengenai kepemilikan atau kepemimpinan mereka. Kami juga ingin melihat laporan transparansi yang lebih sering, terutama dalam hal bagaimana permintaan pemerintah ditangani.

**Minimum untuk Memenuhi Syarat:**

- Kepemimpinan atau kepemilikan yang berhadapan dengan publik.

**Kasus Terbaik:**

- Laporan transparansi yang sering.

### Pemasaran

Dengan penyedia email yang kami rekomendasikan, kami ingin melihat pemasaran yang bertanggung jawab.

**Minimum untuk Memenuhi Syarat:**

- Harus meng-host analitik sendiri (tidak ada Google Analytics, Adobe Analytics, dll.).
- Tidak boleh melakukan pemasaran yang tidak bertanggung jawab, yang dapat mencakup hal-hal berikut:
    - Klaim "enkripsi yang tidak dapat dipecahkan." Enkripsi harus digunakan dengan tujuan agar tidak menjadi rahasia di masa depan ketika teknologi untuk memecahkannya sudah ada.
    - Jaminan perlindungan enonimitas 100%. Ketika seseorang membuat klaim bahwa sesuatu adalah 100%, itu berarti bahwa tidak ada kepastian untuk kegagalan. Kami tahu bahwa orang dapat dengan mudah menghilangkan nama mereka dengan beberapa cara, misalnya.:
        - Menggunakan kembali informasi pribadi, misalnya (akun email, nama samaran unik, dll.) yang mereka akses tanpa perangkat lunak anonimitas seperti Tor
        - [Sidik jari peramban](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Kasus Terbaik:**

- Dokumentasi yang jelas dan mudah dibaca untuk tugas-tugas seperti menyiapkan 2FA, klien email, OpenPGP, dll.

### Fungsionalitas Tambahan

Meskipun tidak sepenuhnya persyaratan, ada beberapa faktor kenyamanan atau privasi lain yang kami pertimbangkan ketika menentukan penyedia mana yang akan direkomendasikan.
