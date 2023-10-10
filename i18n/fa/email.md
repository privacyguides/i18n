---
meta_title: "توصیه های ایمیل خصوصی رمزگذاری شده - Privacy Guides"
title: "سرویس‌های ایمیل"
icon: material/email
description: این ارائه دهندگان ایمیل فضایی عالی برای ذخیره ایمن ایمیل‌های شما ارائه می دهند، و بسیاری از آنها رمزگذاری OpenPGP با سایر ارائه دهندگان ایمیل را ارائه می دهند.
cover: email.png
---

ایمیل عملاً برای استفاده از هر سرویس آنلاین ضروری است، اما ما آن را برای مکالمات فرد به فرد توصیه نمی کنیم. به جای استفاده از ایمیل برای تماس با افراد دیگر، از یک پیام‌رسان استفاده کنید که از محرمانگی رو به جلو (forward secrecy) پشتیبانی می‌کند.

[پیام‌رسان‌های توصیه شده](real-time-communication.md ""){.md-button}

برای هر چیز دیگری، ما انواع ارائه دهندگان ایمیل را بر اساس مدل‌های تجاری پایدار و ویژگی‌های امنیتی و حریم خصوصی توصیه می‌کنیم.

- [ارائه دهندگان ایمیل سازگار با OpenPGP :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [سایر ارائه دهندگان ایمیل رمزگذاری شده :material-arrow-right-drop-circle:](#more-providers)
- [سرویس های نام مستعار ایمیل (Email Aliasing) :material-arrow-right-drop-circle:](#email-aliasing-services)
- [گزینه های خود میزبانی (Self-Hosted) :material-arrow-right-drop-circle:](#self-hosting-email)

## سرویس‌های سازگار با OpenPGP

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. به عنوان مثال، یک کاربر Proton Mail می تواند یک پیام E2EE را به یک کاربر Mailbox.org ارسال کند، یا می توانید اعلان های رمزگذاری شده با OpenPGP را از سرویس های اینترنتی که از آن پشتیبانی می کنند دریافت کنید.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

!!! هشدار

    هنگام استفاده از فناوری E2EE مانند OpenPGP، ایمیل همچنان دارای برخی فراداده است که در header ایمیل رمزگذاری نشده است. بیشتر بخوانید در مورد [فراداده ایمیل](basics/email-security.md#email-metadata-overview).
    
    OpenPGP همچنین از Forward secrecy پشتیبانی نمی کند، به این معنی که اگر کلید خصوصی شما یا گیرنده به سرقت رفته باشد، همه پیام های قبلی رمزگذاری شده با آن قابل بازگشایی خواهد بود. [چگونه از کلید خصوصی خود محافظت کنم؟](basics/email-security.md#how-do-i-protect-my-private-keys)

### Proton Mail

!!! recommendation

    ![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }
    
    **Proton Mail** یک سرویس ایمیل با تمرکز بر حریم خصوصی، رمزگذاری، امنیت و سهولت استفاده است. آن‌ها از **2013** شروع به کار کرده‌اند. شرکت Proton AG در ژنو سوئیس قرار دارد. طرح رایگان شامل ۵۰۰ مگابایت فضای ذخیره‌سازی است.
    
    [:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }
    
    ؟؟؟ دانلودها
    
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
        - [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
        - [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
        - [:simple-apple: macOS](https://proton.me/mail/bridge#download)
        - [:simple-linux: Linux](https://proton.me/mail/bridge#download)
        - [:octicons-browser-16: Web](https://mail.proton.me)

حساب‌های رایگان دارای محدودیت‌هایی هستند، مانند عدم امکان جستجوی متن اصلی و عدم دسترسی به [Proton Mail Bridge](https://proton.me/mail/bridge)، که برای استفاده از [نرم افزار ایمیل دسک‌تاپ (ویندوزی) توصیه‌شده](email-clients.md) لازم است (به عنوان مثال. Thunderbird). حساب‌های پولی شامل ویژگی‌هایی مانند Proton Mail Bridge، فضای ذخیره‌سازی اضافی و پشتیبانی از دامنه سفارشی است. A [letter of attestation](https://proton.me/blog/security-audit-all-proton-apps) was provided for Proton Mail's apps on 9th November 2021 by [Securitum](https://research.securitum.com).

اگر حسابUnlimited یا Business یا Visionary دارید، [SimpleLogin](#simplelogin) پولی را نیز به صورت رایگان دریافت می کنید.

Proton Mail گزارش‌های خرابی داخلی دارد که اطلاعات آن را با اشخاص ثالث به اشتراک **نمی‌گذارد**. This can be disabled in: **Settings** > **Go to Settings** > **Account** > **Security and privacy** > **Send crash reports**.

#### :material-check:{ .pg-green } Custom Domains and Aliases

مشترکین Proton Mail پولی می توانند از دامنه خود با این سرویس یا آدرس [catch-all](https://proton.me/support/catch-all) استفاده کنند. Proton Mail همچنین از [subaddressing](https://proton.me/support/creating-aliases) پشتیبانی می‌کند که برای افرادی که نمی‌خواهند دامنه بخرند مفید است.

#### :material-check:{ .pg-green } روش های پرداخت خصوصی

Proton Mail پول نقد از طریق پست، کارت اعتباری/دبیت استاندارد، [Bitcoin](advanced/payments.md# other-coins-bitcoin-ethereum-etc) و پرداخت های PayPal را [می‌پذیرد](https://proton.me/support/payment-options).

#### :material-check:{ .pg-green } امنیت حساب

Proton Mail از TOTP [احراز هویت دو عاملی](https://proton.me/support/two-factor-authentication-2fa) و [کلیدهای امنیتی سخت افزاری](https://proton.me/support TOTP/2fa-security-key) با استفاده از استانداردهای FIDO2 یا U2F پشتیبانی می‌کند. استفاده از کلید امنیتی سخت افزاری نیازمند راه‌اندازی احراز هویت دو عاملی TOTP است.

#### :material-check:{ .pg-green } امنیت داده

Proton Mail دارای [رمزگذاری بدون دسترسی](https://proton.me/blog/zero-access-encryption) برای سرویس ایمیل‌ و [تقویم](https://proton.me/news/protoncalendar-security-model) است. داده های ایمن شده با رمزگذاری دسترسی صفر فقط توسط شما قابل دسترسی است.

برخی از اطلاعات ذخیره شده در [Proton Contacts](https://proton.me/support/proton-contacts)، مانند نام‌های نمایشی و آدرس‌های ایمیل، با رمزگذاری دسترسی صفر ایمن نمی‌شوند. فیلدهای مخاطبین که از رمزگذاری دسترسی صفر پشتیبانی می کنند، مانند شماره تلفن، با نماد قفل نشان مشخص می شوند.

#### :material-check:{ .pg-green } رمزگذاری ایمیل

Proton Mail دارای [رمزگذاری OpenPGP یکپارچه](https://proton.me/support/how-to-use-pgp) در ایمیل خود است. ایمیل‌های سایر حساب‌های Proton Mail به‌طور خودکار رمزگذاری می‌شوند و رمزگذاری آدرس‌های ایمیل غیر پروتون با کلید OpenPGP به راحتی در تنظیمات حساب شما فعال می‌شود. آنها همچنین به شما این امکان را می‌دهند که [پیام‌های ارسال شده به آدرس‌های ایمیل غیر پروتون را رمزگذاری کنید](https://proton.me/support/password-protected-emails) بدون اینکه نیازی به ثبت نام حساب Proton Mail یا استفاده از نرم‌افزاری مانند OpenPGP باشد.

Proton Mail همچنین از کشف کلیدهای عمومی از طریق HTTP از [دایرکتوری کلیدهای وب (WKD)](https://wiki.gnupg.org/WKD) پشتیبانی می کند. این قابلیت به افرادی که از سرویس Proton Mail استفاده نمی‌کنند اجازه می‌دهد تا کلیدهای OpenPGP حساب‌های Proton Mail را برای رمزگذاری E2EE سرویس‌های دیگر به راحتی پیدا کنند. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } بستن حساب

اگر یک حساب پولی دارید و [صورتحساب شما پس از 14 روز پرداخت نشده است](https://proton.me/support/delinquency)، نمی‌توانید به داده‌های خود دسترسی داشته باشید. پس از 30 روز، حساب شما معلق می‌شود و نامه های دریافتی را دریافت نمی‌کند. در این مدت صورتحساب شما ادامه خواهد داشت.

#### :material-information-outline:{ .pg-blue } عملکردهای دیگر

Proton Mail یک حساب "نامحدود" یا Unlimited به مبلغ 9.99 یورو در ماه ارائه می‌دهد که علاوه بر ارائه چندین حساب، دامنه، نام مستعار و 500 گیگابایت فضای ذخیره سازی، دسترسی به Proton VPN را نیز امکان پذیر می‌کند.

Proton Mail امکان به ارث بردن اطلاعات برای وراث را ندارد.

### Mailbox.org

!!! recommendation

    ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }
    
    **Mailbox.org** یک سرویس ایمیل با تمرکز بر ایمن بودن، بدون آگهی و خصوصی بودن با مصرف انرژی 100% سازگار با محیط زیست است. آنها از سال 2014 شروع به کار کرده‌اند. Mailbox.org در برلین آلمان مستقر است. حساب‌ها با ۲ گیگابایت فضای ذخیره‌سازی شروع می‌شوند که در صورت نیاز می‌توان آن را ارتقا داد.
    
    [:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}
    
    ???     - [:octicons-browser-16: Web](https://login.mailbox.org)

#### :material-check:{ .pg-green } دامنه ها و نام های مستعار (Aliases) سفارشی

Mailbox.org به شما امکان می‌دهد از دامنه خود استفاده کنید و آدرس های [catch-all](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain) را پشتیبانی می‌کند. Mailbox.org همچنین از [subaddressing](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+do+I+use+it) پشتیبانی می کند. اگر نمی‌خواهید دامنه بخرید این قابلیت مفید است.

#### :material-check:{ .pg-green } روش های پرداخت خصوصی

به دلیل تعلیق پرداخت‌یار BitPay در آلمان، Mailbox.org هیچ ارز دیجیتالی را نمی‌پذیرد. با این حال، آنها پول نقد از طریق پست، پرداخت نقدی به حساب بانکی، انتقال بانکی، کارت اعتباری، پی پال و چند پرداخت‌یار خاص آلمانی paydirekt و Sofortüberweisung را می پذیرند.

#### :material-check:{ .pg-green } امنیت حساب

Mailbox.org [تأیید هویت دو عاملی (2FA)](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) را فقط برای ایمیل وب خود پشتیبانی می کند. می توانید از TOTP یا [YubiKey](https://en.wikipedia.org/wiki/YubiKey) از طریق [YubiCloud](https://www.yubico.com/products/services-software/yubicloud) استفاده کنید. استانداردهای وب مانند [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) هنوز پشتیبانی نمی‌شوند.

#### :material-information-outline:{ .pg-blue } امنیت داده

Mailbox.org امکان رمزگذاری نامه های دریافتی را با استفاده از [صندوق پستی رمزگذاری شده](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox) خود می دهد. پیام های جدیدی که دریافت می‌کنید بلافاصله با کلید عمومی شما رمزگذاری می‌شوند.

با این حال، [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange)، پلتفرم نرم‌افزاری که Mailbox.org از آن استفاده می‌کند،

مخاطبین (Contacts) و تقویم را رمزگذاری نمی‌کند. A [standalone option](calendar.md) may be more appropriate for that information.</p> 



#### :material-check:{ .pg-green } رمزگذاری ایمیل

Mailbox.org دارای [رمزگذاری یکپارچه](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) در ایمیل وب خود است که ارسال پیام به افراد دارای کلیدهای عمومی OpenPGP را ساده می کند. آنها همچنین به [گیرندگان راه دور اجازه رمزگشایی ایمیل](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) در سرورهای Mailbox.org را می‌دهند. این ویژگی زمانی مفید است که گیرنده امکان استفاده از OpenPGP را ندارد و نمی تواند یک کپی از ایمیل را در صندوق پستی خود رمزگشایی کند.

Mailbox.org همچنین از کشف کلیدهای عمومی از طریق HTTP از [دایرکتوری کلیدهای وب (WKD)](https://wiki.gnupg.org/WKD) پشتیبانی می کند. این قابلیت به افرادی که از سرویس Mailbox.org استفاده نمی‌کنند اجازه می‌دهد تا کلیدهای OpenPGP حساب‌های Mailbox.org را برای رمزگذاری E2EE سرویس‌های دیگر به راحتی پیدا کنند. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.



#### :material-information-outline:{ .pg-blue } بستن حساب

پس از پایان اشتراک، حساب شما محدود می شود. پس از [30 روز به صورت غیر قابل برگشت](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract) حذف می شود.



#### :material-information-outline:{ .pg-blue } عملکردهای دیگر

با استفاده از [سرویس onion](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org) می‌توانید به حساب Mailbox.org خود از طریق IMAP/SMTP دسترسی پیدا کنید. با این حال، رابط وب ایمیل از طریق سرویس .onion آنها قابل دسترسی نیست و ممکن است با خطاهای گواهی TLS مواجه شوید.

همه حساب‌ها دارای فضای ذخیره‌سازی ابری محدودی هستند که [قابل رمزگذاری](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive) است. Mailbox.org همچنین نام مستعار (Alias) [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely) را ارائه می دهد که رمزگذاری TLS را در اتصال بین سرورهای ایمیل اعمال می کند، در غیر این صورت پیام به هیچ وجه ارسال نخواهد شد. Mailbox.org همچنین از [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) علاوه بر پروتکل‌های دسترسی استاندارد مانند IMAP و POP3 پشتیبانی می‌کند.

Mailbox.org امکان به ارث بردن اطلاعات برای همه طرح‌هایش را دارد. می‌توانید انتخاب کنید که آیا می‌خواهید کدام یک از داده‌هایتان به وراث داده شود، مشروط بر اینکه آنها درخواست دهند و وصیت شما را ارائه دهند. همچنین می‌توانید فردی را با نام و آدرس معرفی کنید.



## سرویس دهندگان بیشتر

این ارائه دهندگان ایمیل های شما را با رمزگذاری دانش صفر (zero-knowledge encryption) ذخیره می کنند که آنها را گزینه‌های خوبی برای ایمن نگه داشتن ایمیل های شما می‌کند. با این حال، آنها از استانداردهای رمزگذاری E2EE بین ارائه دهندگان مختلف ایمیل پشتیبانی نمی‌کنند.

<div class="grid cards" markdown>

- ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ .twemoji } [Skiff Mail](email.md#skiff-mail)
- ![Tutanota logo](assets/img/email/tutanota.svg){ .twemoji } [Tutanota](email.md#tutanota)

</div>

### Skiff Mail

!!! recommendation

    ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ align=right }
    
    **Skiff Mail** یک سرویس ایمیل مبتنی بر وب با E2EE است که در سال 2020 آغاز شد و در سانفرانسیسکو مستقر است و توسعه دهندگان آن در سرتاسر جهان هستند. حساب‌ها با 10 گیگابایت فضای ذخیره‌سازی رایگان شروع می‌شوند.
    
    [:octicons-home-16: Homepage](https://skiff.com/mail){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://app.skiff.com/docs/db93c237-84c2-4b2b-9588-19a7cd2cd45a#tyGksN9rkqbo2uGYASxsA6HVLjUoly/wTYK8tncTto8=){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://skiff.com/help){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/skiff-org/skiff-apps){ .card-link title="Source Code" }
    
    ???     - [:simple-android: Android](https://play.google.com/store/apps/details?id=com.skemailmobileapp&pli=1)
        - [:simple-appstore: iOS](https://apps.apple.com/us/app/skiff-mail/id1619168801)
        - [:octicons-browser-16: Web](https://app.skiff.com/mail)
    

Skiff در طول توسعه خود تحت چند [ممیزی (Audit)](https://skiff.com/transparency) قرار گرفته است.



#### :material-check:{ .pg-green } دامنه ها و نام های مستعار (Aliases) سفارشی

در طرح رایگان، می توانید تا 3 نام مستعار ایمیل @skiff.com علاوه بر آدرس حساب اصلی خود ایجاد کنید. حساب‌های رایگان می‌توانند 1 [دامنه سفارشی (custom domain)](https://skiff.com/blog/custom-domain-setup) و حساب‌های پولی می‌توانند حداکثر 15 دامنه سفارشی را اضافه کنند. می توانید نام های مستعار (Alias) نامحدود یا قابلیت [catch-all](https://skiff.com/blog/catch-all-email-alias) را در دامنه سفارشی خود ایجاد کنید.



#### :material-alert-outline:{ .pg-orange } روش های پرداخت خصوصی

Skiff Mail پرداخت‌های رمزارز از جمله بیت‌کوین و اتریوم را از طریق Coinbase Commerce می‌پذیرد، اما آنها [رمزارز](cryptocurrency.md) پیشنهادی ما، Monero را نمی‌پذیرند. آنها همچنین پرداخت های کارت اعتباری را از طریق Stripe می پذیرند.



#### :material-check:{ .pg-green } امنیت حساب

Skiff Mail از احراز هویت دو مرحله ای TOTP و کلیدهای امنیتی سخت افزاری با استفاده از استانداردهای FIDO2 یا U2F پشتیبانی می کند. استفاده از کلید امنیتی سخت افزاری نیازمند راه‌اندازی احراز هویت دو مرحله ای TOTP است.



#### :material-check:{ .pg-green } امنیت داده

Skiff Mail رمزگذاری دسترسی صفر (zero access) در حالت استراحت (at rest) را برای همه داده‌های شما دارد. این بدان معناست که پیام ها و سایر داده های ذخیره شده در حساب شما فقط توسط شما قابل خواندن است.



#### :material-information-outline:{ .pg-blue } رمزگذاری ایمیل

Skiff Mail از OpenPGP استفاده نمی کند. ایمیل‌ها فقط با رمزگذاری انتها به انتها E2EE برای سایر کاربران Skiff Mail رمزگذاری می‌شوند. Skiff مانند برخی از ارائه دهندگان دیگر ویژگی «صندوق ورودی موقت» یا «رمز بر روی ایمیل» ندارد، به طوری که کاربران خارج از skiff نمی توانند پیام ها را با E2EE دریافت کنند یا به آن‌ها پاسخ دهند.



#### :material-information-outline:{ .pg-blue } بستن حساب

حساب‌های Skiff Mail منقضی نمی‌شوند، اما از حساب‌های پولی پرداخت‌نشده خواسته می‌شود تا همه ویژگی‌های پولی (مانند نام‌های مستعار اضافی) را حذف کنند یا طرح پولی خود را قبل از استفاده تمدید کنند.



#### :material-information-outline:{ .pg-blue } عملکردهای دیگر

Skiff همچنین [ویژگی‌های بهره‌وری فضای کاری](https://discuss.privacyguides.net/t/skiff-pages-drive-productivity-tools/11758/13) را ارائه می دهد، اما ما همچنان <a href را ترجیح می دهیم گزینه های ="productivity.md">جایگزین</a> برای همکاری و اشتراک‌گذاری فایل را ترجیح می‌دهیم.

Skiff Mail امکان به ارث بردن اطلاعات برای وراث را ندارد.



### Tutanota

!!! recommendation

    ![Tutanota logo](assets/img/email/tutanota.svg){ align=right }
    
    **Tutanota** یک سرویس ایمیل با تمرکز بر امنیت و حفظ حریم خصوصی از طریق استفاده از رمزگذاری است. Tutanota از **2011** فعال بوده و در هانوفر آلمان مستقر است. طرح رایگان شامل ۱ گیگابایت فضای ذخیره‌سازی است.
    
    [:octicons-home-16: Homepage](https://tutanota.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://tutanota.com/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://tutanota.com/faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://tutanota.com/community/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
        - [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
        - [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
        - [:simple-windows11: Windows](https://tutanota.com/#download)
        - [:simple-apple: macOS](https://tutanota.com/#download)
        - [:simple-linux: Linux](https://tutanota.com/#download)
        - [:octicons-browser-16: Web](https://mail.tutanota.com/)
    

Tutanota doesn't support the [IMAP protocol](https://tutanota.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tutanota app. Neither [Email import](https://github.com/tutao/tutanota/issues/630) or [subfolders](https://github.com/tutao/tutanota/issues/927) are currently supported, though this is [due to be changed](https://tutanota.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tutanota.com/howto#generalMail) per folder, which may be inconvenient if you have many folders.



#### :material-check:{ .pg-green } Custom Domains and Aliases

Paid Tutanota accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tutanota.com/faq#custom-domain). Tutanota doesn't allow for [subaddressing (plus addresses)](https://tutanota.com/faq#plus), but you can use a [catch-all](https://tutanota.com/howto#settings-global) with a custom domain.



#### :material-information-outline:{ .pg-blue } روش های پرداخت خصوصی

Tutanota only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tutanota.com/faq/#cryptocurrency) with Proxystore.



#### :material-check:{ .pg-green } امنیت حساب

Tutanota supports [two factor authentication](https://tutanota.com/faq#2fa) with either TOTP or U2F.



#### :material-check:{ .pg-green } امنیت داده

Tutanota has [zero access encryption at rest](https://tutanota.com/faq#what-encrypted) for your emails, [address book contacts](https://tutanota.com/faq#encrypted-address-book), and [calendars](https://tutanota.com/faq#calendar). این بدان معناست که پیام ها و سایر داده های ذخیره شده در حساب شما فقط توسط شما قابل خواندن است.



#### :material-information-outline:{ .pg-blue } رمزگذاری ایمیل

Tutanota [does not use OpenPGP](https://www.tutanota.com/faq/#pgp). Tutanota accounts can only receive encrypted emails from non-Tutanota email accounts when sent via a [temporary Tutanota mailbox](https://www.tutanota.com/howto/#encrypted-email-external).



#### :material-information-outline:{ .pg-blue } بستن حساب

Tutanota will [delete inactive free accounts](https://tutanota.com/faq#inactive-accounts) after six months. You can reuse a deactivated free account if you pay.



#### :material-information-outline:{ .pg-blue } Additional Functionality

Tutanota offers the business version of [Tutanota to non-profit organizations](https://tutanota.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tutanota also has a business feature called [Secure Connect](https://tutanota.com/secure-connect/). This ensures customer contact to the business uses E2EE. The feature costs €240/y.

Tutanota doesn't offer a digital legacy feature.



## Email Aliasing Services

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
    

The number of shared aliases (which end in a shared domain like @addy.io) that you can create is limited to 10 on addy.io's free plan, 50 on their $1/month plan and unlimited on the $4/month plan (billed $3 for a year). You can create unlimited standard aliases (which end in a domain like @[username].addy.io or a custom domain on paid plans), however, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. They are useful where a shared domain might be blocked by a service. Securitum [audited](https://addy.io/blog/addy-io-passes-independent-security-audit/) addy.io in September 2023 and no significant vulnerabilities [were identified](https://addy.io/addy-io-security-audit.pdf).

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



## خودمیزبانی ایمیل (Self-Hosting)

ادمین‌های سیستم پیشرفته ممکن است راه اندازی سرور ایمیل خود را در نظر بگیرند. سرورهای ایمیل برای ایمن نگه داشتن چیزها و قابل اعتماد بودن تحویل ایمیل نیاز به توجه و نگهداری مداوم دارند.



### راه‌حل های نرم‌افزاری ترکیبی

!!! recommendation

    ![Mailcow logo](assets/img/email/mailcow.svg){ align=right }
    
     **Mailcow** سرور ایمیل پیشرفته‌تری است که برای کسانی که تجربه لینوکس به نسبت بالایی دارند عالی است. هر آنچه را که در یک Docker Container نیاز دارید را شامل می‌شود: سرور ایمیل با پشتیبانی از DKIM، آنتی ویروس و نظارت بر هرزنامه، webmail و ActiveSync با SOGo، و مدیریت مبتنی بر وب با پشتیبانی 2FA.
    
    [:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }
    

!!! توصیه شده

    ![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }
    
    **Mail-in-a-Box** یک اسکریپت تنظیم خودکار برای پیاده‌سازی یک سرور ایمیل در اوبونتو است. هدف آن این است که راه اندازی سرور ایمیل شخصی را برای افراد آسان‌تر کند.
    
    [:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }
    

برای یک رویکرد دستی‌تر، این دو مقاله را انتخاب کرده‌ایم:

- [راه اندازی سرور ایمیل با OpenSMTPD ،Dovecot و Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (سال ۲۰۱۹)
- [چگونه سرور ایمیل خود را اجرا کنید](https://www.c0ffee.net/blog/mail-server-guide/) (اوت 2017)



## معیار

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any Email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an Email provider, and conduct your own research to ensure the Email provider you choose is the right choice for you.



### فناوری

We regard these features as important in order to provide a safe and optimal service. You should consider whether the provider which has the features you require.

**حداقل شرایط صلاحیت:**

- Encrypts email account data at rest with zero-access encryption.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**بهترین شرایط:**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
- [Subaddressing](https://en.wikipedia.org/wiki/Email_address#Subaddressing) support.
- Catch-all or alias functionality for those who own their own domains.
- Use of standard email access protocols such as IMAP, SMTP or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.



### حریم خصوصی

We prefer our recommended providers to collect as little data as possible.

**حداقل شرایط صلاحیت:**

- Protect sender's IP address. Filter it from showing in the `Received` header field.
- Don't require personally identifiable information (PII) besides a username and a password.
- Privacy policy that meets the requirements defined by the GDPR.

**بهترین شرایط:**

- Accepts [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Hosted in a jurisdiction with strong email privacy protection laws.



### Security

Email servers deal with a lot of very sensitive data. We expect that providers will adopt best industry practices in order to protect their members.

**Minimum to Qualify:**

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

**Best Case:**

- Support for hardware authentication, i.e. U2F and [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F and WebAuthn are more secure as they use a private key stored on a client-side hardware device to authenticate people, as opposed to a shared secret that is stored on the web server and on the client side when using TOTP. Furthermore, U2F and WebAuthn are more resistant to phishing as their authentication response is based on the authenticated [domain name](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), this is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.
- Website security standards such as: 
      - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)



### اعتماد

شما به شخصی با هویت تقلبی برای امور مالی اعتماد نمی‌کنید، پس چرا با ایمیل‌تان به آنها اعتماد کنید؟ ما از ارائه‌دهندگانی که توصیه می‌کنیم می‌خواهیم که درباره مالکیت یا رهبری خود به صورت عمومی اطلاع رسانی کنند. همچنین، ما علاقه‌مندیم که گزارش‌های شفافیت متناوب ببینیم، به ویژه در ارتباط با روش برخورد با درخواست‌های دولتی.

**حداقل شرایط صلاحیت:**

- رهبری یا مالکیت قابل رویت توسط عموم.

**بهترین شرایط:**

- رهبری قابل رویت عمومی.
- گزارش‌های شفافیت متناوب.



### تبلیغات و بازاریابی

با ارائه‌دهندگان ایمیلی که ما توصیه می‌کنیم، ما علاقه‌مند به بازاریابی مسئولانه هستیم.

**حداقل شرایط صلاحیت:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt-out.

نباید هیچ گونه بازاریابی نامسئولانه انجام شود:

- Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
- Making guarantees of protecting anonymity 100%. When someone makes a claim that something is 100% it means there is no certainty for failure. We know people can quite easily deanonymize themselves in a number of ways, e.g.:
  
      - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**بهترین شرایط:**

- Clear and easy to read documentation. This includes things like, setting up 2FA, email clients, OpenPGP, etc.



### قابلیت‌های اضافی

با اینکه این موارد الزامی نیستند، اما در انتخاب ارائه‌دهندگانی که توصیه ‌می‌کنیم، به عواملی مانند راحتی و حفظ حریم خصوصی نیز توجه می‌کنیم.
