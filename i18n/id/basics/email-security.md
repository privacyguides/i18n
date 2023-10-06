---
meta_title: "Why Email Isn't the Best Choice for Privacy and Security - Privacy Guides"
title: Keamanan Email
icon: material/email
description: Email pada dasarnya tidak aman dalam banyak hal, dan ini adalah beberapa alasan mengapa email bukanlah pilihan utama kami untuk komunikasi yang aman.
---

Email adalah bentuk komunikasi yang tidak aman secara default. Anda bisa meningkatkan keamanan email Anda dengan alat seperti OpenPGP, yang menambahkan Enkripsi End-to-End pada pesan Anda, tetapi OpenPGP masih memiliki sejumlah kekurangan dibandingkan dengan enkripsi pada aplikasi perpesanan lainnya, dan beberapa data email tidak pernah bisa dienkripsi secara inheren karena bagaimana email dirancang.

Akibatnya, email paling baik digunakan untuk menerima email transaksional (seperti pemberitahuan, email verifikasi, pengaturan ulang kata sandi, dll.) dari layanan yang Anda daftarkan secara online, bukan untuk berkomunikasi dengan orang lain.

## Email Encryption Overview

Cara standar untuk menambahkan E2EE ke email antara penyedia email yang berbeda adalah dengan menggunakan OpenPGP. Ada beberapa implementasi yang berbeda dari standar OpenPGP, yang paling umum adalah [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard) dan [OpenPGP.js](https://openpgpjs.org).

Ada standar lain yang populer di kalangan bisnis yang disebut [S/MIME](https://en.wikipedia.org/wiki/S/MIME), namun standar ini membutuhkan sertifikat yang dikeluarkan dari [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (tidak semua dari mereka mengeluarkan sertifikat S/MIME). Ini memiliki dukungan di [Google Workplace](https://support.google.com/a/topic/9061730?hl=en&ref_topic=9061731) dan [Outlook untuk Web atau Exchange Server 2016, 2019](https://support.office.com/en-us/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480).

Bahkan jika Anda menggunakan OpenPGP, ia tidak mendukung kerahasiaan [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), yang berarti jika kunci privat Anda atau penerima dicuri, semua pesan sebelumnya yang dienkripsi dengan kunci tersebut akan terekspos. Inilah sebabnya mengapa kami merekomendasikan [instant messenger](../real-time-communication.md) yang menerapkan kerahasiaan ke depan melalui email untuk komunikasi orang-ke-orang bila memungkinkan.

## What is the Web Key Directory standard?

The Web Key Directory (WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Email clients which support WKD will ask the recipient's server for a key based on the email address' domain name. For example, if you emailed `jonah@privacyguides.org`, your email client would ask `privacyguides.org` for Jonah's OpenPGP key, and if `privacyguides.org` has a key for that account, your message would be automatically encrypted.

In addition to the [email clients we recommend](../email-clients.md) which support WKD, some webmail providers also support WKD. Whether *your own* key is published to WKD for others to use depends on your domain configuration. If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox.org, they can publish your OpenPGP key on their domain for you.

If you use your own custom domain, you will need to configure WKD separately. If you control your domain name, you can set up WKD regardless of your email provider. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from keys.openpgp.org, by setting a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then uploading your key to [keys.openpgp.org](https://keys.openpgp.org/). Alternatively, you can [self-host WKD on your own web server](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like @gmail.com, you won't be able to share your OpenPGP key with others via this method.

### Klien Email Apa yang Mendukung E2EE?

Penyedia email yang memungkinkan Anda menggunakan protokol akses standar seperti IMAP dan SMTP dapat digunakan dengan salah satu klien email [yang kami rekomendasikan](../email-clients.md). Tergantung pada metode otentikasi, ini dapat menyebabkan penurunan keamanan jika baik penyedia atau klien email tidak mendukung SUMPAH atau aplikasi jembatan sebagai [otentikasi multi-faktor](multi-factor-authentication.md) tidak mungkin dengan otentikasi kata sandi biasa.

### Bagaimana Cara Melindungi Kunci Pribadi Saya?

A smartcard (such as a [YubiKey](https://support.yubico.com/hc/en-us/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](https://www.nitrokey.com)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. Pesan tersebut kemudian didekripsi oleh smartcard dan konten yang telah didekripsi dikirim kembali ke perangkat.

It is advantageous for the decryption to occur on the smartcard to avoid possibly exposing your private key to a compromised device.

## Email Metadata Overview

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as: `To`, `From`, `Cc`, `Date`, `Subject`. Ada juga sejumlah header tersembunyi yang disertakan oleh banyak klien dan penyedia email yang dapat mengungkapkan informasi tentang akun Anda.

Perangkat lunak klien dapat menggunakan metadata email untuk menunjukkan dari siapa pesan itu berasal dan jam berapa diterima. Servers may use it to determine where an email message must be sent, among [other purposes](https://en.wikipedia.org/wiki/Email#Message_header) which are not always transparent.

### Siapa yang Dapat Melihat Metadata Email?

Metadata email dilindungi dari pengamat luar dengan [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS) melindunginya dari pengamat luar, tetapi masih dapat dilihat oleh perangkat lunak klien email Anda (atau webmail) dan server mana pun yang meneruskan pesan dari Anda ke penerima mana pun, termasuk penyedia email Anda. Terkadang server email juga akan menggunakan layanan pihak ketiga untuk melindungi dari spam, yang umumnya juga memiliki akses ke pesan Anda.

### Mengapa Metadata tidak bisa menjadi E2EE?

Email metadata is crucial to the most basic functionality of email (where it came from, and where it has to go). E2EE pada awalnya tidak dibangun ke dalam protokol email, melainkan membutuhkan perangkat lunak tambahan seperti OpenPGP. Karena pesan OpenPGP masih harus bekerja dengan penyedia email tradisional, ia tidak dapat mengenkripsi metadata email, hanya isi pesan itu sendiri. Itu berarti bahwa bahkan ketika menggunakan OpenPGP, pengamat luar dapat melihat banyak informasi tentang pesan Anda, seperti siapa yang Anda kirimi email, baris subjek, ketika Anda mengirim email, dll.
