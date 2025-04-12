---
meta_title: "Mengapa Surel Bukan Pilihan Terbaik untuk Privasi dan Keamanan - Privacy Guides"
title: Keamanan Surel
icon: material/email
description: Surel pada dasarnya tidak aman dalam banyak hal, dan ini adalah beberapa alasan mengapa surel bukanlah pilihan utama kami untuk komunikasi yang aman.
---

Surel adalah bentuk komunikasi yang tidak aman secara bawaan. Anda bisa meningkatkan keamanan surel Anda dengan alat seperti OpenPGP, yang menambahkan Enkripsi End-to-End pada pesan Anda, tetapi OpenPGP masih memiliki sejumlah kekurangan dibandingkan dengan enkripsi pada aplikasi perpesanan lainnya, dan beberapa data surel tidak pernah bisa dienkripsi secara inheren karena bagaimana surel dirancang.

Akibatnya, surel paling baik digunakan untuk menerima surel transaksional (pemberitahuan, surel verifikasi, pengaturan ulang kata sandi, dll.) dari layanan yang Anda daftarkan secara daring, bukan untuk berkomunikasi dengan orang lain.

## Ikhtisar Enkripsi Surel

Cara standar untuk menambahkan E2EE ke surel antara penyedia surel yang berbeda adalah dengan menggunakan OpenPGP. Ada beberapa implementasi yang berbeda dari standar OpenPGP, yang paling umum adalah [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard) dan [OpenPGP.js](https://openpgpjs.org).

Ada standar lain yang populer di kalangan bisnis yang disebut [S/MIME](https://en.wikipedia.org/wiki/S/MIME), namun standar ini membutuhkan sertifikat yang dikeluarkan dari [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (tidak semua dari mereka mengeluarkan sertifikat S/MIME). It has support in [Google Workplace](https://support.google.com/a/topic/9061730) and [Outlook for Web or Exchange Server 2016, 2019](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480).

Bahkan jika Anda menggunakan OpenPGP, ini tidak mendukung [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), yang berarti jika kunci privat Anda atau penerima dicuri, semua pesan sebelumnya yang dienkripsi dengan kunci tersebut akan terekspos. Inilah sebabnya mengapa kami merekomendasikan [instant messenger](../real-time-communication.md) yang menerapkan kerahasiaan ke depan melalui email untuk komunikasi orang-ke-orang bila memungkinkan.

## Apa itu standar Direktori Kunci Web?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Klien surel yang mendukung WKD akan meminta server penerima untuk mendapatkan kunci berdasarkan nama domain alamat surel. Sebagai contoh, jika Anda mengirim surel ke `jonah@privacyguides.org`, klien surel Anda akan meminta `privacyguides.org` untuk mendapatkan kunci OpenPGP Jonah, dan jika `privacyguides.org` memiliki kunci untuk akun tersebut, pesan Anda akan dienkripsi secara otomatis.

Selain [klien surel yang kami rekomendasikan](../email-clients.md), yang mendukung WKD, beberapa penyedia surel berabasis web juga mendukung WKD. Apakah kunci *Anda* diterbitkan ke WKD untuk digunakan orang lain tergantung pada konfigurasi domain Anda. Jika Anda menggunakan [penyedia surel](../email.md#openpgp-compatible-services) yang mendukung WKD, seperti Proton Mail atau Mailbox.org, mereka dapat mempublikasikan kunci OpenPGP Anda ke domain mereka untuk Anda.

Jika Anda menggunakan domain khusus Anda sendiri, Anda perlu mengonfigurasikan WKD secara terpisah. Jika Anda mengontrol nama domain Anda, Anda bisa menyiapkan WKD terlepas dari apa pun penyedia surel Anda. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from keys.openpgp.org, by setting a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then uploading your key to [keys.openpgp.org](https://keys.openpgp.org). Sebagai alternatif, Anda dapat [meng-host sendiri WKD di server web Anda sendiri](https://wiki.gnupg.org/WKDHosting).

Jika Anda menggunakan domain bersama dari penyedia yang tidak mendukung WKD, seperti @gmail.com, Anda tidak akan dapat berbagi kunci OpenPGP dengan orang lain melalui metode ini.

### Klien Email Apa yang Mendukung E2EE?

Penyedia email yang memungkinkan Anda menggunakan protokol akses standar seperti IMAP dan SMTP dapat digunakan dengan salah satu klien email [yang kami rekomendasikan](../email-clients.md). Depending on the authentication method, this may lead to the decrease security if either the provider or the email client does not support OATH or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### Bagaimana Cara Melindungi Kunci Pribadi Saya?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Email Metadata Overview

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as: `To`, `From`, `Cc`, `Date`, `Subject`. Ada juga sejumlah header tersembunyi yang disertakan oleh banyak klien dan penyedia email yang dapat mengungkapkan informasi tentang akun Anda.

Perangkat lunak klien dapat menggunakan metadata email untuk menunjukkan dari siapa pesan itu berasal dan jam berapa diterima. Servers may use it to determine where an email message must be sent, among [other purposes](https://en.wikipedia.org/wiki/Email#Message_header) which are not always transparent.

### Siapa yang Dapat Melihat Metadata Email?

Metadata email dilindungi dari pengamat luar dengan [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS) melindunginya dari pengamat luar, tetapi masih dapat dilihat oleh perangkat lunak klien email Anda (atau webmail) dan server mana pun yang meneruskan pesan dari Anda ke penerima mana pun, termasuk penyedia email Anda. Terkadang server email juga akan menggunakan layanan pihak ketiga untuk melindungi dari spam, yang umumnya juga memiliki akses ke pesan Anda.

### Mengapa Metadata tidak bisa menjadi E2EE?

Email metadata is crucial to the most basic functionality of email (where it came from, and where it has to go). E2EE pada awalnya tidak dibangun ke dalam protokol email, melainkan membutuhkan perangkat lunak tambahan seperti OpenPGP. Karena pesan OpenPGP masih harus bekerja dengan penyedia email tradisional, ia tidak dapat mengenkripsi metadata email, hanya isi pesan itu sendiri. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, the subject lines, when you're emailing, etc.
