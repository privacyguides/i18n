---
meta_title: "Encrypted Private Email Recommendations - Privacy Guides"
title: "البُرُد الإلكترونية"
icon: material/email
description: توفِّر الجهات المذكورة مخزنًا آمنًا لرسائلك، والكثير منهم يدعم تعمية أوبن‌بي‌جي‌بي مع جهات أخرى.
cover: email.webp
---

حتَّى ولو كان البريد الإلكتروني حاجةً لتستخدم أيَّ خدمة إنترنت فإننا لا نوصي به للتحادث. تأمَّل استخدام خدمة اتصال مباشر تدعم السرية المستقبلية لتحادث الناس بدلًا من استخدام بريد إلكتروني.

[ما نوصي به من برامج مراسلة فورية](real-time-communication.md ""){.md-button}

خلا ذلك فنوصي بعدد من موفِّري خدمة البريد الإلكتروني، وذلك حسب استدامة نموذجات عملهم وأمنهم ومزايا الخصوصية عندهم.

- [موفِّرو خدمة البريد الإلكتروني الداعمون لأوبن‌بي‌جي‌بي :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [غيرهم من موفَّري الخدمة المعمَّاة :material-arrow-right-drop-circle:](#more-providers)
- [خدمات تكنين البُرُد الإلكترونية :material-arrow-right-drop-circle:](#email-aliasing-services)
- [خيارات الاستضافة الذاتية :material-arrow-right-drop-circle:](#self-hosting-email)

## الخدمات الداعمة لأوبن‌بي‌جي‌بي

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. فمثلًا: باستطاعة مستخدم بريد بروتون إرسال رسالة معمَّاة بين الأطراف، وكون المستقبل مستخدم Mailbox.org، أو لك استقبال إشعارات معمَّاةً بأوبن‌بي‌جي‌بي من خدمات الإنترنت الداعمة له.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using E2EE technology like OpenPGP your email will still have some metadata that is not encrypted in the header of the email, generally including the subject line! Read more about [email metadata](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support Forward secrecy, which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed. [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### بريد بروتون

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=left }

**بريد بروتون** هو خدمة بُرُد إلكترونية تركِّز في الخصوصية والتعمية والأمن واليسر. وهم يعملون منذ **٢٠١٣**. ومقرُّ بروتون أي‌جي في جنيف في سويسرا. تبدأ الحسابات عندهم لها سعة تخزين ٥٠٠ م‌بايت، وذلك حسب الاشتراك المجاني.

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

للحسابات المجانية قيود، كعجزهم عن البحث في النصوص وعدم استخدام [جسر بريد بروتون](https://proton.me/mail/bridge)، وتحتاجه إن أردت استخدام [أحد برامج البريد في سطح المكتب الموصى بها](email-clients.md) (مثل ثندربرد). لمن اشترك في حساب عند بريد بروتون مزايا، مثل جسر بريد بروتون ومساحة تخزين إضافية ودعم أسماء النطاق المخصَّصة. أعطت [سكيورتم](https://research.securitum.com) [شهادةً](https://proton.me/blog/security-audit-all-proton-apps) لتطبيقات بريد بروتون في التاسع من نوفمبر عام ٢٠٢١.

إن كان عندك اشتراك «بروتون أنلمتد» أو «بروتون بزنس» أو «فجنري بلان» فسوف تحصل على اشتراك [سمبل‌لوج‌إن](#simplelogin) مجَّانًا.

عند بريد بروتون تقارير تعطُّل داخلية **لا** يشاركونها مع أيِّ جهة خارجية. ولك تعطيلها في: **الإعدادات** > ** إذهب للإعدادات** > **الحساب** > **الأمن والخصوصية** > **أرسل تقارير التعطُّل**.

#### :material-check:{ .pg-green } النطاقات المخصَّصة والكنى

بإمكان مشتركي بريد بروتون استخدام أسماء نطاق من عندهم أو لهم استخدام عنوان [جامع](https://proton.me/support/catch-all). Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } سُبُل الدفع الخاصَّة

[يقبل](https://proton.me/support/payment-options) بريد بروتون الدفع نقدًا عن طريق البريد، ويقبل كذلك الدفع ببطاقات الائتمان والبطاقات المصرفية [وبتكوين](advanced/payments.md#other-coins-bitcoin-ethereum-etc) وبي‌بال.

#### :material-check:{ .pg-green } أمن الحساب

يدعم بريد بروتون [الاستيثاق بخطوتين عبر](https://proton.me/support/two-factor-authentication-2fa) «كلمة المرور لمرة واحدة حسب الوقت (TOTP)» [ومفاتيح أمن العتاد](https://proton.me/support/2fa-security-key) وفق معيارَي FIDO2 و U2F. ويتطلَّب استخدام مفاتيح أمن العتاد إعداد الاستيثاق بخطوتين عبر كلمة المرور لمرة واحدة حسب الوقت.

#### :material-check:{ .pg-green } أمن البيانات

عند بريد بروتون [تعمية دون أيِّ وصول](https://proton.me/blog/zero-access-encryption) لبُرُدك الإلكترونية [وتقويماتك](https://proton.me/news/protoncalendar-security-model). لا يمكن لأحد الوصول للبيانات المعمَّاة دون أيِّ وصول سواك.

بعض المعلومات المخزَّنة في [متراسلي بروتون](https://proton.me/support/proton-contacts) ليست مؤمَّنةً بتعمية دون أيِّ وصول، كالأسماء المعروضة وعناوين البُرُد الإلكترونية. تُعلَّم حقول المتراسلين الداعمة للتعمية دون أيِّ وصول بعلامة قفل، كأرقام الجوالات.

#### :material-check:{ .pg-green } تعمية البريد الإلكتروني

عند بريد بروتون [دعم مدمج لتعمية أوبن‌بي‌جي‌بي](https://proton.me/support/how-to-use-pgp) في صفحة البريد. تعمَّى الرسائل المرسلة لحسابات بريد بروتون الأخرى تلقائيًّا، ولك تمكين تعمية أوبن‌بي‌جي‌بي لعناوين البريد خارج بروتون في إعدادات حسابك. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. ويتيح هذا لمن ليس عنده بريد بروتون العثور على مفاتيح أوبن‌بي‌جي‌بي لحسابات بريد بروتون بسهولة، وذلك لتمكين التعمية بين الأطراف بين موفِّري خدمة البريد الإلكترونيِّ. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } إنهاء الحسابات

إن كان عندك حساب مدفوع [ولم تدفع الفاتورة](https://proton.me/support/delinquency) ١٤ يومًا فلن تستطيع الوصول لبياناتك. وبعد ثلاثين يوم يصبح حسابك خاملًا لا يستقبل الرسائل. وسوف يستمر إصدار الفواتير خلال هذه المدَّة.

#### :material-information-outline:{ .pg-blue } وظائف إضافية

يعرض بريد بروتون حسابًا «لا نهائيًّا» قيمته ٩٫٩٩ يورو لكلِّ شهر، ويتيح الوصول لشبكة بروتون الافتراضية الخاصَّة، واستخدام عدَّة حسابات ونطاقات وكنًى و مساحة تخزين ٥٠٠ ج‌بايت.

ليس عند بريد بروتون ميزة الإرث الرقميِّ.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=left }

**Mailbox.org** هو خدمة بريد إلكترونيٍّ تركِّز على الأمن والخلوِّ من الإعلانات، وهي تستلم طاقتها من مصادر خاصَّة ١٠٠٪ صديقة للبيئة. وهم يعملون منذ ٢٠١٤. ومقرُّهم في برلين في ألمانيا. تبدأ الحسابات ولها مساحة تخزين ٢ ج‌بايت، وتمكن زيادتها حسب الحاجة.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } النطاقات المخصَّصة والكنى

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } سُبُل الدفع الخاصَّة

لا تقبل Mailbox.org الدفع باستخدام العملات المعمَّاة، وسبب ذلك أن معالج دفعهم، بِت‌بَي، علَّق عملياته في ألمانيا. ولكنهم يقبلون الدفع نقدًا عبر البريد، ودفع النقد لحساب مصرف، والتحويل المصرفيَّ، وبطاقات الائتمان، وبَي‌بال، وبعض معالجي الدفع في ألمانيا: paydirekt و Sofortüberweisung.

#### :material-check:{ .pg-green } أمن الحساب

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). بعض معايير الوِب مثل [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) ليست مدعومةً بعد.

#### :material-information-outline:{ .pg-blue } أمن البيانات

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). تعمَّى الرسائل الواردة باستخدام مفتاحك العامِّ فورًا.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. لعلَّ [خيارًا مستقلًّا](calendar.md) أفضل لهذه المعلومات.

#### :material-check:{ .pg-green } تعمية البريد الإلكتروني

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. فائدة هذا تظهر في حال كان المستقبل ليس لديه أوبن‌بي‌جي‌بي ولا يستطيع كشف تعمية نسخة من الرسالة في صندوق بريده.

تدعم Mailbox.org اكتشاف المفتايح العامَّة باستخدام HTTP من [دليل مفاتيح الوِب (WKD)](https://wiki.gnupg.org/WKD) التابع لهم. ويتيح هذا لمن ليس عنده Mailbox.org العثور على مفاتيح أوبن‌بي‌جي‌بي لحسابات Mailbox.org بسهولة، وذلك لتمكين التعمية بين الأطراف بين موفِّري خدمة البريد الإلكترونيِّ. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } إنهاء الحسابات

يعيَّن حسابك حساب مستخدم مقيَّد عند انتهاء عقدك، وبعد [ثلاثين يوم سوف يحذف نهائيًّا](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } وظائف إضافية

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). ولكن لا يمكن الوصول لواجهة موقعهم باستخدام خدمة .onion، وقد تواجه أخطاء شهادة TLS.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. تدعم Mailbox.org [إكستشينج-أكتف‌سنك](https://en.wikipedia.org/wiki/Exchange_ActiveSync)، وكذلك تدعم معايير الوصول القياسية مثل IMAP و POP3.

عند Mailbox.org ميزة الإرث الرقميِّ لكلِّ الاشتراكات. فبوسعك اختيار ما إن أردت أن تورِّث أيَّ بيانات لك، وذلك إن سجَّل ذلك ورثاؤك وشهدت بذلك. غير ذلك فيمكنك ترشيح شخص باسمه وعنوانه.

## مقدِّموا خدمة آخرون

يخزِّن مقدمِّو الخدمة هؤلاء بُرُدك معمَّاةً تعمية دون معرفة، وهذا جاعلهم خيارات جيِّدةً لتخزِّنها فيها. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg){ align=right }

**Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. تبدأ الحسابات المجانية عندهم بمساحة تخزين ١ ج‌بايت.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/faq){ .card-link title=Documentation}
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

Tuta doesn't support the [IMAP protocol](https://tuta.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/howto#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } النطاقات المخصَّصة والكنى

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/faq#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/faq#plus), but you can use a [catch-all](https://tuta.com/howto#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } سُبُل الدفع الخاصَّة

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } أمن الحساب

Tuta supports [two factor authentication](https://tuta.com/faq#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } أمن البيانات

Tuta has [zero access encryption at rest](https://tuta.com/faq#what-encrypted) for your emails, [address book contacts](https://tuta.com/faq#encrypted-address-book), and [calendars](https://tuta.com/faq#calendar). ويعني هذا أن الرسائل والبيانات المخزَّنة في حسابك لا يقرؤها إلا أنت.

#### :material-information-outline:{ .pg-blue } Email Encryption

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } إنهاء الحسابات

Tuta will [delete inactive free accounts](https://tuta.com/faq#inactive-accounts) after six months. ولك إعادة استخدام حساب ألغي تفعليه إن دفعت.

#### :material-information-outline:{ .pg-blue } وظائف إضافية

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tuta also has a business feature called [Secure Connect](https://tuta.com/secure-connect). وهي تضمن أن اتصال العميل بعمل معمًّى بين الأطراف. يكلِّف هذا ٢٤٠ يورو لكلِّ سنة.

Tuta doesn't offer a digital legacy feature.

## خدمات تكنية البُرُد الإلكترونية

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

<div class="admonition recommendation" markdown>

![addy.io logo](assets/img/email/addy.svg#only-light){ align=right }
![addy.io logo](assets/img/email/addy-dark.svg#only-dark){ align=right }

**addy.io** lets you create 10 domain aliases on a shared domain for free, or unlimited "standard" aliases which are less anonymous.

[:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://app.addy.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

The number of shared aliases (which end in a shared domain like @addy.io) that you can create is limited to 10 on addy.io's free plan, 50 on their $1/month plan and unlimited on the $4/month plan (billed $3 for a year). You can create unlimited standard aliases (which end in a domain like @[username].addy.io or a custom domain on paid plans), however, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. They are useful where a shared domain might be blocked by a service. Securitum [audited](https://addy.io/blog/addy-io-passes-independent-security-audit) addy.io in September 2023 and no significant vulnerabilities [were identified](https://addy.io/addy-io-security-audit.pdf).

Notable free features:

- [x] 10 Shared Aliases
- [x] Unlimited Standard Aliases
- [ ] No Outgoing Replies
- [x] 1 Recipient Mailboxes
- [x] Automatic PGP Encryption

### SimpleLogin

<div class="admonition recommendation" markdown>

![Simplelogin logo](assets/img/email/simplelogin.svg){ align=right }

**SimpleLogin** is a free service which provides email aliases on a variety of shared domain names, and optionally provides paid features like unlimited aliases and custom domains.

[:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin was [acquired by Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) as of April 8, 2022. If you use Proton Mail for your primary mailbox, SimpleLogin is a great choice. As both products are now owned by the same company you now only have to trust a single entity. We also expect that SimpleLogin will be more tightly integrated with Proton's offerings in the future. SimpleLogin continues to support forwarding to any email provider of your choosing. Securitum [audited](https://simplelogin.io/blog/security-audit) SimpleLogin in early 2022 and all issues [were addressed](https://simplelogin.io/audit2022/web.pdf).

You can link your SimpleLogin account in the settings with your Proton account. If you have the Proton Unlimited, Business, or Visionary Plan, you will have SimpleLogin Premium for free.

Notable free features:

- [x] 10 Shared Aliases
- [x] Unlimited Replies
- [x] 1 Recipient Mailbox

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

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any Email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an Email provider, and conduct your own research to ensure the Email provider you choose is the right choice for you.

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
