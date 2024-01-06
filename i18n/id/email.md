---
meta_title: "Encrypted Private Email Recommendations - Privacy Guides"
title: "Layanan Surel"
icon: material/email
description: Penyedia surel ini menawarkan tempat yang baik untuk menyimpan surel Anda dengan aman, dan banyak yang menawarkan enkripsi OpenPGP yang dapat dioperasikan dengan penyedia lain.
cover: email.webp
---

Surel bisa dibilang merupakan kebutuhan untuk menggunakan layanan daring apa pun, namun kami tidak merekomendasikannya untuk percakapan antar orang. Daripada menggunakan surel untuk menghubungi orang lain, pertimbangkan untuk menggunakan media pesan instan yang mendukung kerahasiaan penerusan.

[Perpesanan Instan yang Direkomendasikan](real-time-communication.md ""){.md-button}

Untuk yang lainnya, kami merekomendasikan berbagai penyedia surel yang didasarkan pada model bisnis yang berkelanjutan serta fitur keamanan dan privasi bawaan.

- [Penyedia Email yang Kompatibel dengan OpenPGP :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Penyedia Terenkripsi Lainnya :material-arrow-right-drop-circle:](#more-providers)
- [Layanan Alias Surel :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Opsi yang Dilayani Sendiri :material-arrow-right-drop-circle:](#self-hosting-email)

## Layanan yang Kompatibel dengan OpenPGP

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. Sebagai contoh, pengguna Proton Mail dapat mengirim pesan E2EE ke pengguna Mailbox.org, atau Anda dapat menerima notifikasi terenkripsi OpenPGP dari layanan internet yang mendukungnya.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ .twemoji } [Skiff Mail](email.md#skiff-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

!!! warning

    When using E2EE technology like OpenPGP your email will still have some metadata that is not encrypted in the header of the email, generally including the subject line! Baca lebih lanjut tentang [metadata surel] (basics/email-security.md#email-metadata-overview).
    
    OpenPGP juga tidak mendukung kerahasiaan Penerusan, yang berarti jika kunci privat Anda atau penerima dicuri, semua pesan sebelumnya yang dienkripsi dengan kunci tersebut akan terekspos. [Bagaimana cara melindungi kunci pribadi saya?](basics/email-security.md#bagaimana-saya-melindungi-kunci-pribadi-saya)

### Proton Mail

!!! recommendation

    ![ Proton Mail logo ]( assets/img/email/protonmail.svg){ align=right }
    
    **Proton Mail** adalah layanan surel dengan fokus pada privasi, enkripsi, keamanan, dan kemudahan penggunaan. Mereka telah beroperasi sejak **2013**. Proton AG berbasis di Genewa, Swiss. Akun dimulai dengan penyimpanan 500 MB dengan paket gratis mereka.
    
    [:octicons-home-16: Beranda](https://proton.me/mail){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Layanan Onion" }
    [:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Kebijakan Privasi" }
    [:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Dokumentasi}
    [:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Kode Sumber" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
        - [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
        - [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
        - [:simple-apple: macOS](https://proton.me/mail/bridge#download)
        - [:simple-linux: Linux](https://proton.me/mail/bridge#download)
        - [:octicons-browser-16: Web](https://mail.proton.me)

Akun gratis memiliki beberapa keterbatasan, seperti tidak dapat mencari teks tubuh dan tidak memiliki akses ke [Proton Mail Bridge](https://proton.me/mail/bridge), yang diperlukan untuk menggunakan [klien surel desktop yang direkomendasikan](email-clients.md) (misalnya Thunderbird). Akun berbayar mencakup fitur-fitur seperti Proton Mail Bridge, penyimpanan tambahan, dan dukungan domain khusus. [Surat pengesahan](https://proton.me/blog/security-audit-all-proton-apps) diberikan untuk aplikasi Proton Mail pada tanggal 9 November 2021 oleh [Securitum](https://research.securitum.com).

Jika Anda memiliki paket Proton Unlimited, Bisnis, atau Visioner, Anda juga mendapatkan [SimpleLogin](#simplelogin) Premium secara gratis.

Proton Mail memiliki laporan mogok internal yang tidak **dibagikan kepada pihak ketiga**. Ini dapat dinonaktifkan di: **Pengaturan** > **Buka Pengaturan** > **Akun** > **Keamanan dan privasi** > **Kirim laporan kemogokan**.

#### :material-check:{ .pg-green } Domain dan Alias Khusus

Pelanggan Proton Mail berbayar dapat menggunakan domain mereka sendiri dengan layanan ini atau alamat [yang mencakup semua](https://proton.me/support/catch-all). Proton Mail juga mendukung [subalamat](https://proton.me/support/creating-aliases), yang berguna bagi orang-orang yang tidak ingin membeli domain.

#### :material-check:{ .pg-green } Metode Pembayaran Pribadi

Proton Mail [menerima](https://proton.me/support/payment-options) uang tunai melalui pos selain kartu kredit/debit standar, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), dan pembayaran PayPal.

#### :material-check:{ .pg-green } Keamanan Akun

Proton Mail supports TOTP [two factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two factor authentication first.

#### :material-check:{ .pg-green } Data Security

Proton Mail has [zero-access encryption](https://proton.me/blog/zero-access-encryption) at rest for your emails and [calendars](https://proton.me/news/protoncalendar-security-model). Data secured with zero-access encryption is only accessible by you.

Certain information stored in [Proton Contacts](https://proton.me/support/proton-contacts), such as display names and email addresses, are not secured with zero-access encryption. Contact fields that support zero-access encryption, such as phone numbers, are indicated with a padlock icon.

#### :material-check:{ .pg-green } Email Encryption

Proton Mail has [integrated OpenPGP encryption](https://proton.me/support/how-to-use-pgp) in their webmail. Email ke akun Proton Mail lainnya dienkripsi secara otomatis, dan enkripsi ke alamat non-Proton Mail dengan kunci OpenPGP dapat diaktifkan dengan mudah di pengaturan akun Anda. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD, such as Skiff Mail, will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. Hal ini memungkinkan orang yang tidak menggunakan Proton Mail untuk menemukan kunci OpenPGP akun Proton Mail dengan mudah, untuk lintas-penyedia E2EE. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Account Termination

If you have a paid account and your [bill is unpaid](https://proton.me/support/delinquency) after 14 days, you won't be able to access your data. Setelah 30 hari, akun Anda akan menjadi tunggakan dan tidak akan menerima surat masuk. Anda akan terus ditagih selama periode ini.

#### :material-information-outline:{ .pg-blue } Fungsionalitas Tambahan

Proton Mail menawarkan akun "Unlimited" seharga €9,99/Bulan, yang juga memungkinkan akses ke Proton VPN selain menyediakan beberapa akun, domain, alias, dan penyimpanan 500GB.

Proton Mail tidak menawarkan fitur warisan digital.

### Skiff Mail

!!! recommendation

    ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ align=right }
    
    **Skiff Mail** is a web based email service with E2EE that began in 2020 that is based in San Francisco with developers worldwide. Accounts start with 10GB of free storage.
    
    [:octicons-home-16: Homepage](https://skiff.com/mail){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://app.skiff.com/docs/db93c237-84c2-4b2b-9588-19a7cd2cd45a#tyGksN9rkqbo2uGYASxsA6HVLjUoly/wTYK8tncTto8=){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://skiff.com/help){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/skiff-org/skiff-apps){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-android: Android](https://play.google.com/store/apps/details?id=com.skemailmobileapp&pli=1)
        - [:simple-appstore: iOS](https://apps.apple.com/us/app/skiff-mail/id1619168801)
        - [:octicons-browser-16: Web](https://app.skiff.com/mail)

Skiff has undergone a few [audits](https://skiff.com/transparency) during its development.

#### :material-check:{ .pg-green } Domain dan Alias Khusus

You can create up to 3 additional @skiff.com email aliases in addition to your primary account address on their free plan. Free accounts can add 1 [custom domain](https://skiff.com/blog/custom-domain-setup), and up to 15 custom domains on a paid plan. You can create unlimited aliases or a [catch-all](https://skiff.com/blog/catch-all-email-alias) alias on your custom domain.

#### :material-alert-outline:{ .pg-orange } Private Payment Methods

Skiff Mail accepts cryptocurrency payments via Coinbase Commerce, including Bitcoin and Ethereum, but they do not accept our recommended [cryptocurrency](cryptocurrency.md), Monero. They also accept credit card payments via Stripe.

#### :material-check:{ .pg-green } Keamanan Akun

Skiff Mail supports TOTP two-factor authentication and hardware security keys using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Data Security

Skiff Mail has zero access encryption at rest for all of your data. This means the messages and other data stored in your account are only readable by you.

#### :material-check:{ .pg-green } Email Encryption

Skiff Mail encrypts messages to other Skiff mailboxes automatically with E2EE. On December 18th, 2023, Skiff added support for PGP and automatic public key discovery via Web Key Directory (WKD). This means that emails sent to other providers which use WKD, such as Proton Mail, will be automatically encrypted with OpenPGP as well without the need to exchange public PGP keys with your contacts. New Skiff Mail accounts should have a PGP key automatically generated, while accounts from before this feature was introduced need to generate a new PGP key for their address (or upload an existing private key) in the account's address settings. Skiff Mail only has support for reading messages encrypted with PGP/MIME, not the older PGP/Inline standard. Sending messages with PGP/MIME is the [recommended approach](https://www.gnupg.org/faq/gnupg-faq.html#use_pgpmime), but may pose compatibility issues in some edge cases.

Skiff Mail also publishes the public keys of Skiff Mail accounts via HTTP from their [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This allows people who don't use Skiff Mail to find the OpenPGP keys of Skiff Mail accounts easily, for cross-provider E2EE. This only applies to email addresses ending in one of Skiff's own domains, like @skiff.com. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

Skiff does not have a "temporary inbox" or "passworded email" feature like some other providers have, so that external users without OpenPGP cannot receive or reply to messages with E2EE.

#### :material-information-outline:{ .pg-blue } Account Termination

Skiff Mail accounts do not expire, but unpaid accounts will be prompted to remove any enabled paid features (such as additional aliases) or renew their plan before the account can be used.

#### :material-information-outline:{ .pg-blue } Fungsionalitas Tambahan

Skiff additionally offers [workspace productivity features](https://discuss.privacyguides.net/t/skiff-pages-drive-productivity-tools/11758/13), but we still prefer [alternative](productivity.md) options for collaborating and file sharing at this time.

Skiff Mail does not offer a digital legacy feature.

### Mailbox.org

!!! recommendation

    ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }
    
    **Mailbox.org** is an email service with a focus on being secure, ad-free, and privately powered by 100% eco-friendly energy. Mereka telah beroperasi sejak 2014. Mailbox.org berbasis di Berlin, Jerman. Akun dimulai dengan penyimpanan 2 GB, yang dapat ditingkatkan sesuai kebutuhan.
    
    [:octicons-home-16: Beranda](https://mailbox.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Kebijakan Privasi" }
    [:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Dokumentasi}
    
    ??? unduhan
    
        - [:octicons-browser-16: Web](https://login.mailbox.org)

#### :material-check:{ .pg-green } Domain dan Alias Khusus

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain) addresses. Mailbox.org also supports [subaddressing](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } Metode Pembayaran Pribadi

Mailbox.org tidak menerima Bitcoin atau mata uang kripto lainnya sebagai karena prosesor pembayaran mereka BitPay menangguhkan operasi di Jerman. Namun, mereka menerima uang tunai melalui pos, pembayaran tunai ke rekening bank, transfer bank, kartu kredit, PayPal, dan beberapa prosesor khusus Jerman: paydirekt dan Sofortüberweisung.

#### :material-check:{ .pg-green } Keamanan Akun

Mailbox.org mendukung [autentikasi dua faktor](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) hanya untuk surel web mereka. Anda dapat menggunakan TOTP atau [YubiKey](https://en.wikipedia.org/wiki/YubiKey) melalui [YubiCloud](https://www.yubico.com/products/services-software/yubicloud). Standar web seperti [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) belum didukung.

#### :material-information-outline:{ .pg-blue } Keamanan Data

Mailbox.org memungkinkan enkripsi surat masuk menggunakan [kotak surat terenkripsi](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox). Pesan baru yang Anda terima akan segera dienkripsi dengan kunci publik Anda.

Namun, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), platform perangkat lunak yang digunakan oleh Mailbox.org, [tidak mendukung](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) enkripsi buku alamat dan kalender Anda. A [standalone option](calendar.md) may be more appropriate for that information.

#### :material-check:{ .pg-green } Email Encryption

Mailbox.org has [integrated encryption](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) on Mailbox.org's servers. Fitur ini berguna ketika penerima jarak jauh tidak memiliki OpenPGP dan tidak dapat mendekripsi salinan email di kotak surat mereka sendiri.

Mailbox.org also supports the discovery of public keys via HTTP from their [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Hal ini memungkinkan orang di luar Mailbox.org untuk menemukan kunci OpenPGP dari akun Mailbox.org dengan mudah, untuk lintas-penyedia E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Account Termination

Your account will be set to a restricted user account when your contract ends, after [30 days it will be irrevocably deleted](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Fungsionalitas Tambahan

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org). However, their webmail interface cannot be accessed via their .onion service and you may experience TLS certificate errors.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org also supports [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) in addition to standard access protocols like IMAP and POP3.

Mailbox.org memiliki fitur warisan digital untuk semua paket. You can choose whether you want any of your data to be passed to heirs providing that they apply and provide your testament. Alternatively, you can nominate a person by name and address.

## Penyedia Lainnya

These providers store your emails with zero-knowledge encryption, making them great options for keeping your stored emails secure. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

!!! recommendation

    ![Tuta logo](assets/img/email/tuta.svg){ align=right }
    
    **Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. Akun dimulai dengan penyimpanan 1GB dengan paket gratis mereka.
    
    [:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://tuta.com/faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://tuta.com/community/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
        - [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
        - [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
        - [:simple-windows11: Windows](https://tuta.com/#download)
        - [:simple-apple: macOS](https://tuta.com/#download)
        - [:simple-linux: Linux](https://tuta.com/#download)
        - [:octicons-browser-16: Web](https://app.tuta.com/)

Tuta doesn't support the [IMAP protocol](https://tuta.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/howto#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } Domain dan Alias Khusus

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/faq#custom-domain). Tuta doesn't allow for [subaddressing (plus addresses)](https://tuta.com/faq#plus), but you can use a [catch-all](https://tuta.com/howto#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Private Payment Methods

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } Keamanan Akun

Tuta supports [two factor authentication](https://tuta.com/faq#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Data Security

Tuta has [zero access encryption at rest](https://tuta.com/faq#what-encrypted) for your emails, [address book contacts](https://tuta.com/faq#encrypted-address-book), and [calendars](https://tuta.com/faq#calendar). This means the messages and other data stored in your account are only readable by you.

#### :material-information-outline:{ .pg-blue } Email Encryption

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Account Termination

Tuta will [delete inactive free accounts](https://tuta.com/faq#inactive-accounts) after six months. You can reuse a deactivated free account if you pay.

#### :material-information-outline:{ .pg-blue } Fungsionalitas Tambahan

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tuta also has a business feature called [Secure Connect](https://tuta.com/secure-connect/). This ensures customer contact to the business uses E2EE. The feature costs €240/y.

Tuta doesn't offer a digital legacy feature.

## Layanan Alias Surel

An email aliasing service allows you to easily generate a new email address for every website you register for. The email aliases you generate are then forwarded to an email address of your choosing, hiding both your "main" email address and the identity of your email provider. True email aliasing is better than plus addressing commonly used and supported by many providers, which allows you to create aliases like yourname+[anythinghere]@example.com, because websites, advertisers, and tracking networks can trivially remove anything after the + sign to know your true email address.

<div class="grid cards" markdown>

- ![addy.io logo](assets/img/email/mini/addy.svg){ .twemoji } [addy.io](email.md#addyio)
- ![SimpleLogin logo](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

Email aliasing can act as a safeguard in case your email provider ever ceases operation. In that scenario, you can easily re-route your aliases to a new email address. In turn, however, you are placing trust in the aliasing service to continue functioning.

Using a dedicated email aliasing service also has a number of benefits over a catch-all alias on a custom domain:

- Aliases can be turned on and off individually when you need them, preventing websites from emailing you randomly.
- Replies are sent from the alias address, shielding your real email address.

They also have a number of benefits over "temporary email" services:

- Aliases are permanent and can be turned on again if you need to receive something like a password reset.
- Emails are sent to your trusted mailbox rather than stored by the alias provider.
- Temporary email services typically have public mailboxes which can be accessed by anyone who knows the address, aliases are private to you.

Our email aliasing recommendations are providers that allow you to create aliases on domains they control, as well as your own custom domain(s) for a modest yearly fee. They can also be self-hosted if you want maximum control. However, using a custom domain can have privacy-related drawbacks: If you are the only person using your custom domain, your actions can be easily tracked across websites simply by looking at the domain name in the email address and ignoring everything before the at (@) sign.

Using an aliasing service requires trusting both your email provider and your aliasing provider with your unencrypted messages. Some providers mitigate this slightly with automatic PGP encryption, which reduces the number of parties you need to trust from two to one by encrypting incoming emails before they are delivered to your final mailbox provider.

### addy.io

!!! recommendation

    ![addy.io logo](assets/img/email/addy.svg#only-light){ align=right }
    ![addy.io logo](assets/img/email/addy-dark.svg#only-dark){ align=right }
    
    **addy.io** lets you create 10 domain aliases on a shared domain for free, or unlimited "standard" aliases which are less anonymous.
    
    [:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://app.addy.io/docs){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
        - [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

The number of shared aliases (which end in a shared domain like @addy.io) that you can create is limited to 10 on addy.io's free plan, 50 on their $1/month plan and unlimited on the $4/month plan (billed $3 for a year). You can create unlimited standard aliases (which end in a domain like @[username].addy.io or a custom domain on paid plans), however, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. They are useful where a shared domain might be blocked by a service. Securitum [mengaudit](https://addy.io/blog/addy-io-passes-independent-security-audit/) addy.io pada September 2023 dan tidak ada kerentanan signifikan [yang teridentifikasi](https://addy.io/addy-io-security-audit.pdf).

Notable free features:

- [x] 10 Shared Aliases
- [x] Unlimited Standard Aliases
- [ ] No Outgoing Replies
- [x] 1 Recipient Mailboxes
- [x] Automatic PGP Encryption

### SimpleLogin

!!! recommendation

    ![Simplelogin logo](assets/img/email/simplelogin.svg){ align=right }
    
    **SimpleLogin** is a free service which provides email aliases on a variety of shared domain names, and optionally provides paid features like unlimited aliases and custom domains.
    
    [:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
        - [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
        - [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

SimpleLogin was [acquired by Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) as of April 8, 2022. If you use Proton Mail for your primary mailbox, SimpleLogin is a great choice. As both products are now owned by the same company you now only have to trust a single entity. We also expect that SimpleLogin will be more tightly integrated with Proton's offerings in the future. SimpleLogin continues to support forwarding to any email provider of your choosing. Securitum [audited](https://simplelogin.io/blog/security-audit/) SimpleLogin in early 2022 and all issues [were addressed](https://simplelogin.io/audit2022/web.pdf).

You can link your SimpleLogin account in the settings with your Proton account. If you have the Proton Unlimited, Business, or Visionary Plan, you will have SimpleLogin Premium for free.

Notable free features:

- [x] 10 Shared Aliases
- [x] Unlimited Replies
- [x] 1 Recipient Mailbox

## Email Hosting Mandiri

Advanced system administrators may consider setting up their own email server. Mail servers require attention and continuous maintenance in order to keep things secure and mail delivery reliable.

### Combined software solutions

!!! recommendation

    ![Mailcow logo](assets/img/email/mailcow.svg){ align=right }
    
    **Mailcow** is a more advanced mail server perfect for those with a bit more Linux experience. It has everything you need in a Docker container: A mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.
    
    [:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

!!! recommendation

    ![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }
    
    **Mail-in-a-Box** is an automated setup script for deploying a mail server on Ubuntu. Its goal is to make it easier for people to set up their own mail server.
    
    [:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

For a more manual approach we've picked out these two articles:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [How To Run Your Own Mail Server](https://www.c0ffee.net/blog/mail-server-guide/) (August 2017)

## Kriteria

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any Email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an Email provider, and conduct your own research to ensure the Email provider you choose is the right choice for you.

### Teknologi

We regard these features as important in order to provide a safe and optimal service. You should consider whether the provider which has the features you require.

**Minimum untuk Memenuhi Syarat:**

- Encrypts email account data at rest with zero-access encryption.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**Kasus Terbaik:**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
- [Subaddressing](https://en.wikipedia.org/wiki/Email_address#Subaddressing) support.
- Catch-all or alias functionality for those who own their own domains.
- Use of standard email access protocols such as IMAP, SMTP or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.

### Privasi

Kami lebih memilih penyedia yang kami rekomendasikan untuk mengumpulkan data sesedikit mungkin.

**Minimum untuk Memenuhi Syarat:**

- Protect sender's IP address. Filter it from showing in the `Received` header field.
- Don't require personally identifiable information (PII) besides a username and a password.
- Privacy policy that meets the requirements defined by the GDPR.

**Kasus Terbaik:**

- Accepts [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Hosted in a jurisdiction with strong email privacy protection laws.

### Keamanan

Email servers deal with a lot of very sensitive data. We expect that providers will adopt best industry practices in order to protect their members.

**Minimum untuk Memenuhi Syarat:**

- Protection of webmail with 2FA, such as TOTP.
- Zero access encryption, builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) support.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://www.hardenize.com/), [testssl.sh](https://testssl.sh/), or [Qualys SSL Labs](https://www.ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLSv1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- A valid [MTA-STS](https://tools.ietf.org/html/rfc8461) and [TLS-RPT](https://tools.ietf.org/html/rfc8460) policy.
- Valid [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Valid [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) and [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996/).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) submission, assuming SMTP is used.
- Website security standards such as:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) if loading things from external domains.
- Must support viewing of [Message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Kasus Terbaik:**

- Support for hardware authentication, i.e. U2F and [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F and WebAuthn are more secure as they use a private key stored on a client-side hardware device to authenticate people, as opposed to a shared secret that is stored on the web server and on the client side when using TOTP. Furthermore, U2F and WebAuthn are more resistant to phishing as their authentication response is based on the authenticated [domain name](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), this is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Program bug-bounty dan/atau proses pengungkapan kerentanan yang terkoordinasi.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

### Kepercayaan

Anda tidak akan mempercayakan keuangan Anda pada seseorang dengan identitas palsu, jadi mengapa mempercayakan surel Anda pada mereka? Kami mewajibkan penyedia layanan yang kami rekomendasikan untuk terbuka mengenai kepemilikan atau kepemimpinan mereka. Kami juga ingin melihat laporan transparansi yang lebih sering, terutama dalam hal bagaimana permintaan pemerintah ditangani.

**Minimum untuk Memenuhi Syarat:**

- Kepemimpinan atau kepemilikan yang berhadapan dengan publik.

**Kasus Terbaik:**

- Kepemimpinan yang berhadapan dengan publik.
- Laporan transparansi yang sering.

### Pemasaran

With the email providers we recommend we like to see responsible marketing.

**Minimum untuk Memenuhi Syarat:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt-out.

Tidak boleh melakukan pemasaran yang tidak bertanggung jawab:

- Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
- Menjamin perlindungan anonimitas 100%. Ketika seseorang membuat klaim bahwa sesuatu itu 100%, itu berarti tidak ada kepastian untuk gagal. Kami tahu bahwa orang dapat dengan mudah menyamarkan nama mereka dengan beberapa cara, misalnya:

    - Menggunakan kembali informasi pribadi (akun surel, nama samaran unik, dll.) yang mereka akses tanpa perangkat lunak anonimitas (Tor, VPN, dll.)
    - [Sidik jari peramban](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Kasus Terbaik:**

- Clear and easy to read documentation. This includes things like, setting up 2FA, email clients, OpenPGP, etc.

### Fungsionalitas Tambahan

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
