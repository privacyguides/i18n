---
meta_title: "Encrypted Private Email Recommendations - Privacy Guides"
title: "خزمەتگوزاری پۆستەی ئەلکتڕۆنی"
icon: material/email
description: ئەم دابینکەرانەی پۆستەی ئەلکتڕۆنی شوێنێکی نایاب پێشکەش دەکەن بۆ کۆکردنەوەی پۆستەکان بە پارێزراوی.
cover: email.webp
---

<!-- markdownlint-disable MD024 -->
پۆستەی ئەلکتڕۆنی بەتایبەتی گرنگە بۆ بەکارهێنانی هەر خزمەتگوزاریەکی سەرهێڵ، بەڵام ئێمە پێشنیاری ناکەین بۆ گفتوفۆی دوو کەسی. لەجیاتی بەکارهێنانی پۆستەی ئەلکتڕۆنی بۆ پەیوەندی کردن بە کەسانی تر، ڕەچاوی بەکارهێنانی ئامرازێکی نامەبەری دەستبەجێ بکە، کە پشتگیری لە نهێنیکردنی بەردەوام دەکات.

[نامەبەرە دەستبەجێیە پێشنیارکراوەکان](real-time-communication.md ""){.md-button}

بۆ هەموو شتێکی تر، ئێمە دابینکەری پۆستەی ئەلکتڕۆنی جۆراوجۆر پێشنیاردەکەین لەسەر بنەمای شێوازی بازرگانی پشتپێبەستراو و تایبەتمەندیەکانی پاراستن و تایبەتێێی.

- [دابینکەرانی پۆستەی ئەلکتڕۆنی گونجاو لەگەڵOpenPGP :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [دابینکەرانی تری شفرکراو:material-arrow-right-drop-circle:](#more-providers)
- [هەڵبژاردنەکانی سەرپەرشتی-خودی :material-arrow-right-drop-circle:](#self-hosting-email)

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md) to protect your privacy. Among other things, these services can help protect your real inbox from spam, prevent marketers from correlating your accounts, and encrypt all incoming messages with PGP.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

## خزمەتگوزاریەکانی گونجاون لەگەڵ OpenPGP

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. بۆ نموونە: بەکارهێنەرێکی Proton Mail دەتوانێت پەیامێکی E2EE بنێرێت بۆ بەکارهێنەرێکی Mailbox.org، یان دەتوانیت ئاگادارکردنەوەی OpenPGP-شفرکراوت پێ بگات لەڕێی ئەو خزمەتگوزاریانەی پشتگیری دەکەن.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using E2EE technology like OpenPGP your email will still have some metadata that is not encrypted in the header of the email, generally including the subject line! Read more about [email metadata](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support Forward secrecy, which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed. [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![لۆگۆی Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** خزمەتگوزاریەکی پۆستەی ئەلکتڕۆنیە، کە سەرنجی هەبوونی تایبەتێتی، شفرکردن، پارێزراوی، وە ئاسان لە بەکارهێنان دروست کراوە. ئەوان لە **2013**ـەوە لە کاردان. Proton AG is based in Genève, Switzerland. Accounts start with 500 MB storage with their free plan.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

هەژمارە بەخۆڕایەکان هەندێک سنووریان هەیە، وەک نەتوانینی گەڕان لەناو دەقی نامە و مافی نەبوونی بەکارهێنانی [Proton Mail Bridge](https://proton.me/mail/bridge)، کە پێویستە بۆ بەکارهێنانی[ ڕاژەخوازە پێشنیارکراوەکانی سەر کۆمپیوتەر](email-clients.md) (نـم. Thunderbird). هەژمارە پارەدراوەکان هەندێک تایبەتمەندی لەخۆدەگرن وەک Proton Mail Bridge، کۆگای زیادە، و پشتگیری دۆمەینە تایبەتەکان. [نامەیەکی تاقیکردنەوە](https://proton.me/blog/security-audit-all-proton-apps) بە مەبەستی لایەنگری بۆ کاربەرنامەکانی Proton Mail پێشکەشکرا لە 9ـی تشرینی دووەمی(نۆڤێمبەری) ساڵی 2021 لەلایەن [Securitum](https://research.securitum.com).

If you have the Proton Unlimited, Business, Family, or Visionary Plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail ڕاپۆرتی تێکچوونە ناوخۆییەکانی هەیە، کە ئەوان هاوبەشی **ناکەن** لەگەڵ لایەنە سێیەمەکان. ئەمە دەتوانێ لە ناچالاک بکرێت لە: **Settings** > **Go to Settings** > **Account** > **Security and privacy** > **Send crash reports**.

#### :material-check:{ .pg-green } دۆمەینە تایبەتیەکان و نازناوەکان

بەژداربووانی Proton Mail دەتوانن دۆمەینی خۆیان بەکاربێنن لەگەل خزمەتگوزاریەکە یان <a href=https://proton.me/support/catch-all>هەموو نامەیەک بگرنەوە</a>. Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green }شێوازی پارەدانی نهێنی

Proton Mail پارەی نەخت [وەردەگرێت](https://proton.me/support/payment-options) لەڕێگای پۆستە, لەگەڵ شێوازە باوەکانی تری پارەدان وەک [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc)، credit/debit card، و Paypal.

#### :material-check:{ .pg-green }پارێزراوێتی هەژمار

Proton Mail supports TOTP [two factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two factor authentication first.

#### :material-check:{ .pg-green }پارێزراوێتی زانیاری

Proton Mail تەکنەلۆژیای [شفرکردن و تێپەڕبوونی-ئەستەمی](https://proton.me/blog/zero-access-encryption) بەکاردێنێت بۆ پۆستە ئەلکتڕۆنیەکان و [ڕۆژ ژمێرەکانت](https://proton.me/news/protoncalendar-security-model). زانیارەکانی، کە بە تەکنەلۆژیای شفرەکردن و تێپەربوونی-ئەستەمی پارێزگاریان لێکراوە تەنهیا تۆو دەستت پێیان دەگات.

هەندێک زانیاری کە هەڵگیراون لەناو [ Proton Contacts](https://proton.me/support/proton-contacts)، وەک ناوە پیشاندراوەکان و ناونیشانی پۆستە ئەلکتڕۆنیەکان، ئەوائەوانە پارێزگاریان لێ نەکراوە بە تەکنەلۆژیای شفرکردن و تێپەڕبوونی-ئەستەمی. ئەو خانانەی Contacts کە پشتگیری لە شفرکردن و تێپەڕبوونی-ئەستەمی دەکەن، بەشێوەی وێنەیەکی بچووکراوەی قفڵ نیشان دەدرێن.

#### :material-check:{ .pg-green } شفرکردنی پۆستەی ئەلکتڕۆنی

Proton Mail [شفرکردنی OpenPGP زیادکردووە](https://proton.me/support/how-to-use-pgp) بۆ ماڵپەری پۆستەی ئەلکتڕۆنییەکەیان. پۆستەی ئەلکتڕۆنی نێوان هەژمارەکانی Proton Mail خۆکارانە شفرکراوە، بەڵام شفرکردن لە نێوان Proton Mail و پۆستەی ئەلکتڕۆنی تر شفردەکرێن بە ئاسانی لەڕێگەی کلیلی OpenPGP، کە لە ڕێکخستنەکانی هەژمارەکەت هەیە. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. ئەمەڕێگە ئەو کەسانە دەدات کە Proton Mail بەکار ناهێنن بۆئەوەی کلیکە گشتیەکانی هەژماری Proton Mail بە ئاسانی بدۆزنەوە. تا ببێتە هۆی گونجاندن لەگەڵ دابینکەرانی تری E2EE. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } لەناوبردنی هەژمار

ئەگەر هەژمارێکی پارەدراوت هەبێت وە [پارەی پسوولەکەت نەدابێت](https://proton.me/support/delinquency) دوای 14 ڕۆژ، ئەوا ناتوانیت دەستت بگات بە زانیاریەکانت. دوای 30 ڕۆژ، هەژمارەکەت دەبێتە نایاسایی و هیچ نامایەکی ترت بۆ نایەت. لەم ماوەیەدا بەردەوام دەبیت لە وەرگرتنی پسوولە. Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address on a deactivated account.

#### :material-information-outline:{ .pg-blue } کرداری زیادە

Proton Mail هەژمارێکی "Unlimited" پێشکەش دەکات لەبەرامبەر €9.99 بۆ یەک مانگ، کە توانای بەکارهێنانی Proton VPN چالاک دەکات جگە لە پێشکەشکردنی زیاتر لە هەژمارێک، دۆمەینێک، نازناوێک، وە 500G بۆ کۆکردنەوە.

Poton Mail کرداری میراتی دیجیتاڵی پێشکەش ناکات.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox** خزمەتگوزاریەکی پۆستەی ئەلکتڕۆنیە کە جەخت لە هەبوونی سەلامەتی و بێ بەرامبەری تایبەتێتی و کارکردن بە وزەیەکی %100ـی هاوڕێی ژینگە. ئەوان لە **2014**ـەوە لە کاردان. Mailbox.org دەکەوێتە بەرلین، لە ئەڵمانیا. هەژمارەکان دەستپێدەکەن لە 2GB بۆ هەڵگرتن، کە دەتوانرێت زیاد بکرێت بەپێی پێویست.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } دۆمەینە تایبەتیەکان و نازناوەکان

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green }شێوازی پارەدانی نهێنی

Mailbox.org هیچ جۆرە دراوێکی دیجیتاڵی قبوڵ ناکات بەهۆی ڕاگرتنی کارەکانی شێوازی پارەدانەکەیان BitPay لە ئەڵمانیا. However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green }پارێزراوێتی هەژمار

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). شیوازە باوەکانی وەک [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) هێشتا پشتگیری نەکراون.

#### :material-information-outline:{ .pg-blue }پارێزراوێتی زانیاری

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). نامە نوێکانی کە تۆ وەریدەگری ڕاستەوخۆ بە کلیلی گشتیت شفر دەکرێن.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. [بژاردەیەکی سەربەخۆ](calendar.md) لەوانەیە گونجاوتر بێت بۆ ئەم زانیاریە.

#### :material-check:{ .pg-green } شفرکردنی پۆستەی ئەلکتڕۆنی

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. ئەم تایبەتمەندیە بەسوودە کاتێک وەرگر لە دوورەوە OpenPGPـی نییە و ناتوانێت شفرەکە لەسەر لەبەرگیراوەیەکی پۆستەکە لاببات لە سندووقی پۆستەکانی خۆیدا.

هەروەها Mailbox.org پشتگیری دۆزینەوەی کلیلە گشتیەکان دەکات لە HTTPــەوە لە ڕێگای [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). ئەمە ڕێگە بە کەسانی دەرەوەی Mailbox.org دەدات کە کلیلەکانی OpenPGP بۆ هەژمارەکانی Mailbox.org بە ئاسانی بدۆزنەوە، تا ببێتە هۆی گونجاندن لەگەڵ دابینکەرانی تری E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } لەناوبردنی هەژمار

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } کرداری زیادە

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). هەرچۆنێک بێت، ناتوانیت لە ڕێگەی ڕووکاری ماڵپەڕی پۆستەی ئەلکتڕۆنییەکەیان خزمەتگوزاری .onian بەکاربهێنیت وە لەوانەیە ڕووبەڕووی هەڵەی بڕوانامەی TLS ببیتەوە.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org also supports [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) in addition to standard access protocols like IMAP and POP3.

Mailbox.org has a digital legacy feature for all plans. You can choose whether you want any of your data to be passed to heirs providing that they apply and provide your testament. Alternatively, you can nominate a person by name and address.

## More Providers

These providers store your emails with zero-knowledge encryption, making them great options for keeping your stored emails secure. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg){ align=right }

**Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. Accounts start with 1GB storage with their free plan.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:simple-windows11: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta doesn't support the [IMAP protocol](https://tuta.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } دۆمەینە تایبەتیەکان و نازناوەکان

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Private Payment Methods

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green }پارێزراوێتی هەژمار

Tuta supports [two factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green }پارێزراوێتی زانیاری

Tuta has [zero access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). This means the messages and other data stored in your account are only readable by you.

#### :material-information-outline:{ .pg-blue } Email Encryption

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } لەناوبردنی هەژمار

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. You can reuse a deactivated free account if you pay.

#### :material-information-outline:{ .pg-blue } کرداری زیادە

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tuta doesn't offer a digital legacy feature.

## Self-Hosting Email

Advanced system administrators may consider setting up their own email server. Mail servers require attention and continuous maintenance in order to keep things secure and mail delivery reliable.

### Combined software solutions

<div class="admonition recommendation" markdown>

![Mailcow logo](assets/img/email/mailcow.svg){ align=right }

**Mailcow** is a more advanced mail server perfect for those with a bit more Linux experience. It has everything you need in a Docker container: A mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** is an automated setup script for deploying a mail server on Ubuntu. Its goal is to make it easier for people to set up their own mail server.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>

For a more manual approach we've picked out these two articles:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## Criteria

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### Technology

We regard these features as important in order to provide a safe and optimal service. You should consider whether the provider which has the features you require.

**Minimum to Qualify:**

- Encrypts email account data at rest with zero-access encryption.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**Best Case:**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
- Catch-all or alias functionality for those who own their own domains.
- Use of standard email access protocols such as IMAP, SMTP or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.

### Privacy

We prefer our recommended providers to collect as little data as possible.

**Minimum to Qualify:**

- Protect sender's IP address. Filter it from showing in the `Received` header field.
- Don't require personally identifiable information (PII) besides a username and a password.
- Privacy policy that meets the requirements defined by the GDPR.

**Best Case:**

- Accepts [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Hosted in a jurisdiction with strong email privacy protection laws.

### Security

Email servers deal with a lot of very sensitive data. We expect that providers will adopt best industry practices in order to protect their members.

**Minimum to Qualify:**

- Protection of webmail with 2FA, such as TOTP.
- Zero access encryption, builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) support.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLSv1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- A valid [MTA-STS](https://tools.ietf.org/html/rfc8461) and [TLS-RPT](https://tools.ietf.org/html/rfc8460) policy.
- Valid [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Valid [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) and [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) submission, assuming SMTP is used.
- Website security standards such as:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) if loading things from external domains.
- Must support viewing of [Message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Best Case:**

- Support for hardware authentication, i.e. U2F and [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F and WebAuthn are more secure as they use a private key stored on a client-side hardware device to authenticate people, as opposed to a shared secret that is stored on the web server and on the client side when using TOTP. Furthermore, U2F and WebAuthn are more resistant to phishing as their authentication response is based on the authenticated [domain name](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), this is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Trust

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**Minimum to Qualify:**

- Public-facing leadership or ownership.

**Best Case:**

- Public-facing leadership.
- Frequent transparency reports.

### Marketing

With the email providers we recommend we like to see responsible marketing.

**Minimum to Qualify:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt-out.

Must not have any marketing which is irresponsible:

- Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
- Making guarantees of protecting anonymity 100%. When someone makes a claim that something is 100% it means there is no certainty for failure. We know people can quite easily deanonymize themselves in a number of ways, e.g.:

    - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Best Case:**

- Clear and easy to read documentation. This includes things like, setting up 2FA, email clients, OpenPGP, etc.

### Additional Functionality

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
