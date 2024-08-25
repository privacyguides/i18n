---
meta_title: "توصیه های ایمیل خصوصی رمزگذاری شده - Privacy Guides"
title: "سرویس‌های ایمیل"
icon: material/email
description: این ارائه دهندگان ایمیل فضایی عالی برای ذخیره ایمن ایمیل‌های شما ارائه می دهند، و بسیاری از آنها رمزگذاری OpenPGP با سایر ارائه دهندگان ایمیل را ارائه می دهند.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

ایمیل عملاً برای استفاده از هر سرویس آنلاین ضروری است، اما ما آن را برای مکالمات فرد به فرد توصیه نمی کنیم. به جای استفاده از ایمیل برای تماس با افراد دیگر، از یک پیام‌رسان استفاده کنید که از محرمانگی رو به جلو (forward secrecy) پشتیبانی می‌کند.

[پیام‌رسان‌های توصیه شده](real-time-communication.md ""){.md-button}

## Recommended Providers

برای هر چیز دیگری، ما انواع ارائه دهندگان ایمیل را بر اساس مدل‌های تجاری پایدار و ویژگی‌های امنیتی و حریم خصوصی توصیه می‌کنیم. Read our [full list of criteria](#criteria) for more information.

| Provider                    | OpenPGP / WKD                          | IMAP / SMTP                                                | Zero Access Encryption                               | Anonymous Payments            |
| --------------------------- | -------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------- | ----------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Paid plans only | :material-check:{ .pg-green }                        | Cash                          |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                              | :material-information-outline:{ .pg-blue } Mail only | Cash                          |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                        | Monero & Cash via third-party |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md) to protect your privacy. Among other things, these services can help protect your real inbox from spam, prevent marketers from correlating your accounts, and encrypt all incoming messages with PGP.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

## سرویس‌های سازگار با OpenPGP

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. به عنوان مثال، یک کاربر Proton Mail می تواند یک پیام E2EE را به یک کاربر Mailbox.org ارسال کند، یا می توانید اعلان های رمزگذاری شده با OpenPGP را از سرویس های اینترنتی که از آن پشتیبانی می کنند دریافت کنید.

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

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** یک سرویس ایمیل با تمرکز بر حریم خصوصی، رمزگذاری، امنیت و سهولت استفاده است. They have been in operation since 2013. شرکت Proton AG در ژنو سوئیس قرار دارد. The Proton Mail Free plan comes with 500MB of Mail storage, which you can increase up to 1GB for free.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

حساب‌های رایگان دارای محدودیت‌هایی هستند، مانند عدم امکان جستجوی متن اصلی و عدم دسترسی به [Proton Mail Bridge](https://proton.me/mail/bridge)، که برای استفاده از [نرم افزار ایمیل دسک‌تاپ (ویندوزی) توصیه‌شده](email-clients.md) لازم است (به عنوان مثال. Thunderbird). حساب‌های پولی شامل ویژگی‌هایی مانند Proton Mail Bridge، فضای ذخیره‌سازی اضافی و پشتیبانی از دامنه سفارشی است. A [letter of attestation](https://proton.me/blog/security-audit-all-proton-apps) was provided for Proton Mail's apps on 9th November 2021 by [Securitum](https://research.securitum.com).

If you have the Proton Unlimited plan or any multi-user Proton plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail has internal crash reports that are **not** shared with third parties. This can be disabled in the web app: :gear: → **All Settings** → **Account** → **Security and privacy** → **Privacy and data collection**.

#### :material-check:{ .pg-green } Custom Domains and Aliases

مشترکین Proton Mail پولی می توانند از دامنه خود با این سرویس یا آدرس [catch-all](https://proton.me/support/catch-all) استفاده کنند. Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } روش های پرداخت خصوصی

Proton Mail پول نقد از طریق پست، کارت اعتباری/دبیت استاندارد، [Bitcoin](advanced/payments.md# other-coins-bitcoin-ethereum-etc) و پرداخت های PayPal را [می‌پذیرد](https://proton.me/support/payment-options).

#### :material-check:{ .pg-green } امنیت حساب

Proton Mail از TOTP [احراز هویت دو عاملی](https://proton.me/support/two-factor-authentication-2fa) و [کلیدهای امنیتی سخت افزاری](https://proton.me/support TOTP/2fa-security-key) با استفاده از استانداردهای FIDO2 یا U2F پشتیبانی می‌کند. استفاده از کلید امنیتی سخت افزاری نیازمند راه‌اندازی احراز هویت دو عاملی TOTP است.

#### :material-check:{ .pg-green } امنیت داده

Proton Mail دارای [رمزگذاری بدون دسترسی](https://proton.me/blog/zero-access-encryption) برای سرویس ایمیل‌ و [تقویم](https://proton.me/news/protoncalendar-security-model) است. داده های ایمن شده با رمزگذاری دسترسی صفر فقط توسط شما قابل دسترسی است.

برخی از اطلاعات ذخیره شده در [Proton Contacts](https://proton.me/support/proton-contacts)، مانند نام‌های نمایشی و آدرس‌های ایمیل، با رمزگذاری دسترسی صفر ایمن نمی‌شوند. فیلدهای مخاطبین که از رمزگذاری دسترسی صفر پشتیبانی می کنند، مانند شماره تلفن، با نماد قفل نشان مشخص می شوند.

#### :material-check:{ .pg-green } رمزگذاری ایمیل

Proton Mail دارای [رمزگذاری OpenPGP یکپارچه](https://proton.me/support/how-to-use-pgp) در ایمیل خود است. ایمیل‌های سایر حساب‌های Proton Mail به‌طور خودکار رمزگذاری می‌شوند و رمزگذاری آدرس‌های ایمیل غیر پروتون با کلید OpenPGP به راحتی در تنظیمات حساب شما فعال می‌شود. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. این قابلیت به افرادی که از سرویس Proton Mail استفاده نمی‌کنند اجازه می‌دهد تا کلیدهای OpenPGP حساب‌های Proton Mail را برای رمزگذاری E2EE سرویس‌های دیگر به راحتی پیدا کنند. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } بستن حساب

اگر یک حساب پولی دارید و [صورتحساب شما پس از 14 روز پرداخت نشده است](https://proton.me/support/delinquency)، نمی‌توانید به داده‌های خود دسترسی داشته باشید. پس از 30 روز، حساب شما معلق می‌شود و نامه های دریافتی را دریافت نمی‌کند. در این مدت صورتحساب شما ادامه خواهد داشت. Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address of a deactivated account.

#### :material-information-outline:{ .pg-blue } عملکردهای دیگر

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500GB of storage.

Proton Mail امکان به ارث بردن اطلاعات برای وراث را ندارد.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** یک سرویس ایمیل با تمرکز بر ایمن بودن، بدون آگهی و خصوصی بودن با مصرف انرژی 100% سازگار با محیط زیست است. آنها از سال 2014 شروع به کار کرده‌اند. Mailbox.org در برلین آلمان مستقر است. Accounts start with up to 2GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } دامنه ها و نام های مستعار (Aliases) سفارشی

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } روش های پرداخت خصوصی

به دلیل تعلیق پرداخت‌یار BitPay در آلمان، Mailbox.org هیچ ارز دیجیتالی را نمی‌پذیرد. However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } امنیت حساب

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). استانداردهای وب مانند [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) هنوز پشتیبانی نمی‌شوند.

#### :material-information-outline:{ .pg-blue } امنیت داده

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). پیام های جدیدی که دریافت می‌کنید بلافاصله با کلید عمومی شما رمزگذاری می‌شوند.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. A [standalone option](calendar.md) may be more appropriate for that information.

#### :material-check:{ .pg-green } رمزگذاری ایمیل

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. این ویژگی زمانی مفید است که گیرنده امکان استفاده از OpenPGP را ندارد و نمی تواند یک کپی از ایمیل را در صندوق پستی خود رمزگشایی کند.

Mailbox.org همچنین از کشف کلیدهای عمومی از طریق HTTP از [دایرکتوری کلیدهای وب (WKD)](https://wiki.gnupg.org/WKD) پشتیبانی می کند. این قابلیت به افرادی که از سرویس Mailbox.org استفاده نمی‌کنند اجازه می‌دهد تا کلیدهای OpenPGP حساب‌های Mailbox.org را برای رمزگذاری E2EE سرویس‌های دیگر به راحتی پیدا کنند. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } بستن حساب

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } عملکردهای دیگر

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). با این حال، رابط وب ایمیل از طریق سرویس .onion آنها قابل دسترسی نیست و ممکن است با خطاهای گواهی TLS مواجه شوید.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org همچنین از [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) علاوه بر پروتکل‌های دسترسی استاندارد مانند IMAP و POP3 پشتیبانی می‌کند.

Mailbox.org امکان به ارث بردن اطلاعات برای همه طرح‌هایش را دارد. می‌توانید انتخاب کنید که آیا می‌خواهید کدام یک از داده‌هایتان به وراث داده شود، مشروط بر اینکه آنها درخواست دهند و وصیت شما را ارائه دهند. همچنین می‌توانید فردی را با نام و آدرس معرفی کنید.

## سرویس دهندگان بیشتر

این ارائه دهندگان ایمیل های شما را با رمزگذاری دانش صفر (zero-knowledge encryption) ذخیره می کنند که آنها را گزینه‌های خوبی برای ایمن نگه داشتن ایمیل های شما می‌کند. با این حال، آنها از استانداردهای رمزگذاری E2EE بین ارائه دهندگان مختلف ایمیل پشتیبانی نمی‌کنند.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since 2011 and is based in Hanover, Germany. Free accounts start with 1GB of storage.

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
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta doesn't support the [IMAP protocol](https://tuta.com/support#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } دامنه ها و نام های مستعار (Aliases) سفارشی

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } روش های پرداخت خصوصی

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } امنیت حساب

Tuta supports [two factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } امنیت داده

Tuta has [zero access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). این بدان معناست که پیام ها و سایر داده های ذخیره شده در حساب شما فقط توسط شما قابل خواندن است.

#### :material-information-outline:{ .pg-blue } رمزگذاری ایمیل

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } بستن حساب

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. You can reuse a deactivated free account if you pay.

#### :material-information-outline:{ .pg-blue } عملکردهای دیگر

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

Tuta doesn't offer a digital legacy feature.

## خودمیزبانی ایمیل (Self-Hosting)

ادمین‌های سیستم پیشرفته ممکن است راه اندازی سرور ایمیل خود را در نظر بگیرند. سرورهای ایمیل برای ایمن نگه داشتن چیزها و قابل اعتماد بودن تحویل ایمیل نیاز به توجه و نگهداری مداوم دارند.

### راه‌حل های نرم‌افزاری ترکیبی

<div class="admonition recommendation" markdown>

![Mailcow logo](assets/img/email/mailcow.svg){ align=right }

 **Mailcow** سرور ایمیل پیشرفته‌تری است که برای کسانی که تجربه لینوکس به نسبت بالایی دارند عالی است. It has everything you need in a Docker container: a mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** یک اسکریپت تنظیم خودکار برای پیاده‌سازی یک سرور ایمیل در اوبونتو است. هدف آن این است که راه اندازی سرور ایمیل شخصی را برای افراد آسان‌تر کند.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>

برای یک رویکرد دستی‌تر، این دو مقاله را انتخاب کرده‌ایم:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## معیار

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### فناوری

We regard these features as important in order to provide a safe and optimal service. You should consider whether the provider which has the features you require.

**حداقل شرایط صلاحیت:**

- Encrypts email account data at rest with zero-access encryption.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**بهترین شرایط:**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
- Catch-all or alias functionality for those who use their own domains.
- Use of standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.

### حریم خصوصی

We prefer our recommended providers to collect as little data as possible.

**Minimum to Qualify:**

- Protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Don't require personally identifiable information (PII) besides a username and a password.
- Privacy policy that meets the requirements defined by the GDPR.

**Best Case:**

- Accepts [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Hosted in a jurisdiction with strong email privacy protection laws.

### Security

Email servers deal with a lot of very sensitive data. We expect that providers will adopt best industry practices in order to protect their customers.

**حداقل شرایط صلاحیت:**

- Protection of webmail with 2FA, such as TOTP.
- Zero access encryption, which builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
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
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**بهترین شرایط:**

- Support for hardware authentication, i.e. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable third-party firm.
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### اعتماد

شما به شخصی با هویت تقلبی برای امور مالی اعتماد نمی‌کنید، پس چرا با ایمیل‌تان به آنها اعتماد کنید؟ ما از ارائه‌دهندگانی که توصیه می‌کنیم می‌خواهیم که درباره مالکیت یا رهبری خود به صورت عمومی اطلاع رسانی کنند. همچنین، ما علاقه‌مندیم که گزارش‌های شفافیت متناوب ببینیم، به ویژه در ارتباط با روش برخورد با درخواست‌های دولتی.

**Minimum to Qualify:**

- رهبری یا مالکیت قابل رویت توسط عموم.

**بهترین شرایط:**

- گزارش‌های شفافیت متناوب.

### تبلیغات و بازاریابی

With the email providers we recommend, we like to see responsible marketing.

**حداقل شرایط صلاحیت:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt out.

Must not have any irresponsible marketing, which can include the following:

- Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
- Making guarantees of protecting anonymity 100%. When someone makes a claim that something is 100% it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:

    - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Best Case:**

- Clear and easy to read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### قابلیت‌های اضافی

با اینکه این موارد الزامی نیستند، اما در انتخاب ارائه‌دهندگانی که توصیه ‌می‌کنیم، به عواملی مانند راحتی و حفظ حریم خصوصی نیز توجه می‌کنیم.
