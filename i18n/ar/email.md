---
meta_title: "توصيات Privacy Guides لاستخدام بريد إلكتروني مشفر يحافظ على الخصوصية"
title: "البُرُد الإلكترونية"
icon: material/email
description: توفِّر الجهات المذكورة مخزنًا آمنًا لرسائلك، والكثير منهم يدعم تعمية أوبن‌بي‌جي‌بي مع جهات أخرى.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>يوفر الحماية من التهديدات التالية:</small>

- [:material-server-network: مزودو الخدمات](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

حتَّى ولو كان البريد الإلكتروني حاجةً لتستخدم أيَّ خدمة إنترنت فإننا لا نوصي به للتحادث. تأمَّل استخدام خدمة اتصال مباشر تدعم السرية المستقبلية لتحادث الناس بدلًا من استخدام بريد إلكتروني.

[ما نوصي به من برامج مراسلة فورية](real-time-communication.md ""){.md-button}

## موفرو الخدمة الموصى بهم

خلا ذلك فنوصي بعدد من موفِّري خدمة البريد الإلكتروني، وذلك حسب استدامة نموذجات عملهم وأمنهم ومزايا الخصوصية عندهم. للمزيد من المعلومات، اطلع على [قائمة المعايير](#criteria).

| مزوّد                       | OpenPGP / WKD                          | IMAP / SMTP                                               | تشفير يمنع وصول المزود إلى البيانات                   | وسائل الدفع بدون هوية                                  |
| --------------------------- | -------------------------------------- | --------------------------------------------------------- | ----------------------------------------------------- | ------------------------------------------------------ |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } خطط مدفوعة فقط | :material-check:{ .pg-green }                         | نقداً                                                  |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                             | :material-information-outline:{ .pg-blue } البريد فقط | نقداً                                                  |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                    | :material-check:{ .pg-green }                         | مونيرو (Monero) <br> دفع نقدي من خلال وسيط خارجي |

الإضافة إلى (أو بدلا من) مزود البريد الإلكتروني الموصى به هنا، قد ترغب في استخدام [خدمة مخصصة لإخفاء البريد الإلكتروني](email-aliasing.md#recommended-providers) (email aliasing) لحماية خصوصيتك. من بين فوائد هذه الخدمات أنها تساعد في حماية بريدك الحقيقي من الرسائل المزعجة، وتمنع جهات التسويق من ربط حساباتك ببعضها، كما يمكنها تشفير جميع الرسائل الواردة باستخدام PGP.

- [المزيد من المعلومات :material-arrow-right-drop-circle:](email-aliasing.md)

## الخدمات الداعمة لـ OpenPGP

تدعم هذه الخدمات بشكل مدمج تشفير وفك تشفير OpenPGP، بالإضافة إلى معيار [Web Key Directory (WKD)](basics/email-security.md#what-is-the-web-key-directory-standard)، مما يتيح إرسال واستقبال رسائل بريد إلكتروني مشفرة بالكامل من الطرف إلى الطرف، دون الاعتماد على مزود خدمة معين. فمثلًا: باستطاعة مستخدم بريد بروتون إرسال رسالة معمَّاة بين الأطراف، وكون المستقبل مستخدم Mailbox.org، أو لك استقبال إشعارات معمَّاةً بأوبن‌بي‌جي‌بي من خدمات الإنترنت الداعمة له.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

عند استخدام تقنيات التشفير التام بين الطرفين (E2EE) مثل OpenPGP، سيظل هناك بعض البيانات الوصفية (metadata) غير مشفرة في رأس الرسالة، وغالبا ما يشمل ذلك سطر العنوان (subject)! اقرأ المزيد عن [بيانات البريد الإلكتروني الوصفية (metadata)](basics/email-security.md#email-metadata-overview).

لا يدعم OpenPGP خاصية (forward secrecy)، أي أنه إذا تمكن أحد من الحصول على المفتاح الخاص بك أو بمستلم الرسالة لاحقا، فسيكون بإمكانه فك تشفير جميع الرسائل القديمة التي تم إرسالها باستخدام ذلك المفتاح.

- [كيف أحمي مفاتيحي الخاصة (private keys)؟](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=left }

**بريد بروتون** هو خدمة بُرُد إلكترونية تركِّز في الخصوصية والتعمية والأمن واليسر. بدأت خدمتهم منذ عام 2013. تقع شركة Proton AG في جنيف، سويسرا.

توفر خطة Proton المجانية سعة تخزين للبريد تصل إلى 500 ميجابايت، ويمكنك زيادتها مجانا حتى 1 جيجابايت.

[:octicons-home-16: الصفحة الرئيسية](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="سياسة الخصوصية" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="لشرح التفصيلي" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

الحسابات المجانية لديها بعض القيود، مثل عدم القدرة على البحث داخل محتوى الرسائل، وعدم إمكانية استخدام أداة [Proton Mail Bridge](https://proton.me/mail/bridge)، التي تُستخدم لربط بريد Proton مع [برامج البريد على الكمبيوتر](email-clients.md) مثل Thunderbird. لمن اشترك في حساب عند بريد بروتون مزايا، مثل جسر بريد بروتون ومساحة تخزين إضافية ودعم أسماء النطاق المخصَّصة. إذا كنت مشتركا في خطة Proton Unlimited أو أي خطة متعددة المستخدمين من Proton، فستحصل أيضا على [SimpleLogin](email-aliasing.md#simplelogin) Premium مجانا، وهي خدمة تساعدك على إنشاء عناوين بريد إلكتروني مستعارة لحماية خصوصيتك وتجنب الرسائل المزعجة.

أعطت [سكيورتم](https://research.securitum.com) [شهادةً](https://proton.me/blog/security-audit-all-proton-apps) لتطبيقات بريد بروتون في التاسع من نوفمبر عام ٢٠٢١.

بريد Proton Mail يحتوي على تقارير أعطال داخلية (internal crash reports) **لا** تتم مشاركتها مع أي جهة خارجية. يمكنك إيقاف هذا الخيار من خلال تطبيق الويب::gear: → **جميع الإعدادات (All Settings)** → **الحساب (Account)** → **الأمان والخصوصية (Security and privacy)** → **الخصوصية وجمع البيانات (Privacy and data collection)**.

#### :material-check:{ .pg-green } النطاقات المخصَّصة والكنى

بإمكان مشتركي بريد بروتون استخدام أسماء نطاق من عندهم أو لهم استخدام عنوان [جامع](https://proton.me/support/catch-all). يدعم Proton Mail أيضًا ما يُعرف بـ[العناوين الإضافية](https://proton.me/support/creating-aliases) (sub-addressing)، وهي ميزة تتيح لك إنشاء عناوين فرعية مرتبطة ببريدك الأساسي دون الحاجة إلى شراء نطاق خاص. على سبيل المثال، يمكنك استخدام عنوان مثل username+shopping@proton.me لتسجيله في مواقع التسوق، وسيتم توجيه الرسائل إلى بريدك الرئيسي نفسه.

#### :material-check:{ .pg-green } سُبُل الدفع الخاصَّة

يقبل Proton Mail [الدفع](https://proton.me/support/payment-options) **نقدًا عبر البريد** (عن طريق إرسال المبلغ ورقيًا إلى عنوانهم البريدي)، بالإضافة إلى وسائل الدفع المعتادة مثل بطاقات الـ credit/debit، [البيتكوين](advanced/payments.md#other-coins-bitcoin-ethereum-etc)، وPayPal.

#### :material-check:{ .pg-green } أمن الحساب

يدعم Proton Mail المصادقة الثنائية (TOTP) [two-factor authentication](https://proton.me/support/two-factor-authentication-2fa)، بالإضافة إلى [مفاتيح أمان مادية (hardware security keys)](https://proton.me/support/2fa-security-key) تعمل وفقًا لمعايير FIDO2 أو U2F، مثل مفاتيح YubiKey أو SoloKey. يتطلب استخدام الـ hardware security key تفعيل المصادقة الثنائية (TOTP) أولًا.

#### :material-check:{ .pg-green } أمن البيانات

عند بريد بروتون [تعمية دون أيِّ وصول](https://proton.me/blog/zero-access-encryption) لبُرُدك الإلكترونية [وتقويماتك](https://proton.me/news/protoncalendar-security-model). البيانات المحمية بتشفير بدون وصول (zero-access encryption) لا يمكن لأي أحد الوصول إليها سوى أنت.

ليست كل البيانات في Proton Contacts مشفّرة بالكامل؛ فمثلاً، الـ display names وعناوين البريد تظل قابلة للوصول من قِبل مزود الخدمة لأنها لا تخضع لتشفير بدون وصول. الحقول في جهات الاتصال التي تدعم التشفير بدون وصول — مثل أرقام الهاتف — يتم تمييزها بأيقونة قفل.

#### :material-check:{ .pg-green } تشفير البريد الإلكتروني

يحتوي Proton Mail على [دعم مدمج لتشفير OpenPGP](https://proton.me/support/how-to-use-pgp) داخل واجهة البريد على الويب، مما يسهّل إرسال واستقبال رسائل مشفّرة دون الحاجة إلى إعدادات خارجية. يتم تشفير الرسائل المرسلة إلى حسابات Proton Mail الأخرى تلقائيا. كما يمكن تفعيل التشفير عند إرسال رسائل إلى عناوين خارجية تدعم OpenPGP بسهولة من خلال إعدادات الحساب. يدعم Proton أيضا ميزة البحث التلقائي عن المفاتيح العامة (public keys) الخاصة بمستلمي البريد باستخدام معيار WKD (Web Key Directory). هذا يعني أنك تستطيع إرسال رسائل مشفرة تلقائيا إلى مستخدمين في خدمات بريد أخرى تدعم WKD، دون الحاجة لمشاركة مفاتيح التشفير يدويا مع أي شخص. يتيح لك Proton أيضا [تشفير الرسائل المرسلة إلى عناوين بريد خارجية (غير Proton Mail) بدون استخدام OpenPGP](https://proton.me/support/password-protected-emails)، ودون أن يحتاج المستلم إلى إنشاء حساب في Proton Mail. يتم ذلك من خلال حماية الرسالة بكلمة مرور تختارها أنت، وتشاركها مع المستلم بطريقة آمنة.

ينشر Proton Mail أيضا الـ public keys لحساباته عبر بروتوكول HTTP من خلال نظام WKD (Web Key Directory)، مما يسهّل على الآخرين العثور على مفاتيح التشفير الخاصة بك عند إرسال رسائل مشفّرة إليك. وبفضل هذه الميزة، يمكن لأي شخص يستخدم خدمة بريد مختلفة العثور على مفتاح التشفير الخاص بك في Proton Mail بسهولة، وإرسال رسائل مشفّرة إليك دون خطوات معقّدة، باستخدام التشفير التام بين الطرفين (E2EE). ينطبق هذا فقط على عناوين البريد التي تنتهي بأحد نطاقات Proton الخاصة، مثل `@proton.me`. إذا كنت تستخدم نطاقا مخصصًا (أي عنوان بريد إلكتروني ينتهي باسم نطاقك الخاص بدلًا من ‎@proton.me)، فستحتاج إلى [إعداد WKD](basics/email-security.md#what-is-the-web-key-directory-standard) يدويا بشكل منفصل.

#### :material-information-outline:{ .pg-blue } إنهاء الحسابات

إن كان عندك حساب مدفوع [ولم تدفع الفاتورة](https://proton.me/support/delinquency) ١٤ يومًا فلن تستطيع الوصول لبياناتك. وبعد ثلاثين يوم يصبح حسابك خاملًا لا يستقبل الرسائل. وسوف يستمر إصدار الفواتير خلال هذه المدَّة. سيقوم Proton [بحذف الحسابات المجانية غير النشطة](https://proton.me/support/inactive-accounts) بعد مرور عام من عدم استخدامها. إذا تم إلغاء تفعيل حسابك، **فلن تتمكن** من استخدام نفس عنوان البريد الإلكتروني مرة أخرى.

#### :material-information-outline:{ .pg-blue } وظائف إضافية

تمنحك خطة [Proton Unlimited](https://proton.me/support/proton-plans#proton-unlimited) إمكانية الوصول إلى باقي خدمات Proton، بالإضافة إلى دعم عدة نطاقات مخصصة، وإنشاء عدد غير محدود من عناوين "أخفي بريدي (hide-my-email)" (وهي عناوين مستعارة تُستخدم لحماية بريدك الحقيقي)، إلى جانب 500 جيجابايت من سعة التخزين.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

خدمة Mailbox.org هي خدمة بريد إلكتروني تركز على الأمان، خالية من الإعلانات، وتعمل بالكامل باستخدام طاقة صديقة للبيئة بنسبة 100٪. وهم يعملون منذ ٢٠١٤. ومقرُّهم في برلين في ألمانيا.

تبدأ الحسابات بسعة تخزين تصل إلى 2 جيجابايت، ويمكن زيادتها حسب الحاجة.

:octicons-home-16: الصفحة الرئيسية](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="سياسة الخصوصية" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="شرح تفصيلي" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } النطاقات المخصَّصة والكنى

تتيح لك Mailbox.org استخدام نطاقك الخاص، كما تدعم عناوين [Catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name)، وهي عناوين تستقبل أي رسالة تُرسل إلى أي اسم ضمن نطاقك، حتى لو لم يكن العنوان مُعرّفًا مسبقًا. تدعم Mailbox.org أيضا ميزة [العناوين الإضافية (sub-addressing)](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it)، وهي مفيدة إذا كنت لا ترغب في شراء نطاق خاص، حيث يمكنك إنشاء عناوين فرعية مرتبطة ببريدك الأساسي لاستخدامها لأغراض مختلفة (مثل: username+news@mailbox.org).

#### :material-check:{ .pg-green } وسائل الدفع الخاصة

خدمة Mailbox.org لا تقبل العملات الرقمية حاليا بسبب توقف مزود الدفع BitPay عن العمل في ألمانيا. ومع ذلك، فإنهم يقبلون الدفع **نقدًا** عبر البريد، أو **نقدًا** عبر إيداع في حساب بنكي، بالإضافة إلى التحويل البنكي، وبطاقات الائتمان، وPayPal، وعدد من وسائل الدفع الخاصة بألمانيا مثل Paydirekt وSofortüberweisung.

#### :material-check:{ .pg-green } أمن الحساب

تدعم Mailbox.org ميزة [المصادقة الثنائية (two-factor authentication)](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa)، ولكنها متوفرة فقط عند استخدام البريد من خلال الموقع (webmail)، ولا تعمل عند استخدام تطبيقات خارجية مثل Thunderbird أو Outlook. يمكنك استخدام المصادقة الثنائية إما عبر TOTP أو من خلال [YubiKey](https://en.wikipedia.org/wiki/YubiKey) باستخدام خدمة [YubiCloud](https://yubico.com/products/services-software/yubicloud). لم يتم دعم معايير الويب مثل [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) حتى الآن، وهي تقنية حديثة تتيح تسجيل الدخول بشكل آمن بدون الحاجة إلى كلمات مرور.

#### :material-information-outline:{ .pg-blue } أمن البيانات

تتيح Mailbox.org تشفير الرسائل الواردة باستخدام ميزة [صندوق البريد المشفر (encrypted mailbox)](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox) الخاص بها. تعمَّى الرسائل الواردة باستخدام مفتاحك العامِّ فورًا.

ومع أن Mailbox.org توفّر صندوق بريد مشفّر، إلا أن المنصة التي تعتمد عليها [(Open-Xchange) ](https://en.wikipedia.org/wiki/Open-Xchange)[لا تدعم](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) تشفير جهات الاتصال والتقويم، مما يعني أن هذه البيانات لا تتم حمايتها بالتشفير الكامل مثل الرسائل. إذا كنت ترغب في حماية تقويمك وجهات اتصالك بتشفير كامل، فمن الأفضل استخدام [خدمة منفصلة](calendar.md) مخصصة لذلك.

#### :material-check:{ .pg-green } تشفير البريد الإلكتروني

توفر Mailbox.org [تشفيرا مدمجا ](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard)داخل واجهة البريد على المتصفح، ما يسهل إرسال رسائل مشفرة إلى الأشخاص الذين يستخدمون مفاتيح OpenPGP، دون الحاجة إلى إعدادات معقّدة. يمكنك إرسال رسائل مشفّرة حتى [إلى أشخاص لا يستخدمون PGP](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp)، حيث يمكنهم فك تشفير الرسالة عبر صفحة خاصة على موقع Mailbox.org، باستخدام كلمة مرور تقوم بمشاركتها معهم بشكل آمن. فائدة هذا تظهر في حال كان المستقبل ليس لديه أوبن‌بي‌جي‌بي ولا يستطيع كشف تعمية نسخة من الرسالة في صندوق بريده.

تدعم Mailbox.org أيضا العثور على الـ public keys عبر بروتوكول HTTP من خلال نظام WKD (Web Key Directory)، مما يسهل على الآخرين إرسال رسائل مشفّرة إليك دون الحاجة لتبادل المفاتيح يدويا. يساعد هذا الأشخاص الذين لا يستخدمون Mailbox.org في العثور بسهولة على مفاتيح OpenPGP الخاصة بمستخدمي Mailbox.org، مما يسهّل إرسال رسائل مشفّرة بتشفير تام بين الطرفين (E2EE) حتى بين خدمات بريد مختلفة. هذا ينطبق فقط على عناوين البريد الإلكتروني التي تنتهي بأحد نطاقات Mailbox.org، مثل `@mailbox.org`، ولا يشمل العناوين المخصصة التي تستخدم نطاقك الخاص. إذا كنت تستخدم نطاقا مخصصًا (أي عنوان بريد إلكتروني ينتهي باسم نطاقك الخاص بدلًا من ‎@proton.me)، فستحتاج إلى [إعداد WKD](basics/email-security.md#what-is-the-web-key-directory-standard) يدويا بشكل منفصل.

#### :material-information-outline:{ .pg-blue } إنهاء الحسابات

سيتم تحويل حسابك إلى حساب محدود الصلاحيات عند انتهاء الاشتراك. سيتم حذف الحساب بشكل نهائي ولا يمكن استعادته بعد [30 يومًا](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract) من انتهاء الاشتراك.

#### :material-information-outline:{ .pg-blue } وظائف إضافية

يمكنك الوصول إلى حسابك في Mailbox.org عبر IMAP/SMTP باستخدام [خدمة ‎.onion الخاصة بهم](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org)، وذلك من خلال شبكة Tor لتأمين الاتصال وإخفاء الهوية. واجهة البريد على الموقع لا تعمل بالكامل عند الدخول عبر شبكة Tor باستخدام عنوان ‎.onion، وقد تظهر رسائل تحذير تتعلّق بشهادة الأمان عند محاولة الاتصال.

تأتي جميع الحسابات بسعة تخزين سحابي محدودة، ويمكنك [تشفير الملفات](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive) داخلها مباشرة من خلال واجهة Mailbox.org لحماية خصوصيتك، دون الحاجة إلى أدوات خارجية. توفر Mailbox.org عنوانا خاصا وهو [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely)، يمكنك استخدامه بدلًا من عنوانك العادي إذا كنت تريد إرسال الرسائل فقط عندما يكون الاتصال بين خوادم البريد مشفّرا بالكامل (TLS). وإذا لم يكن التشفير متاحا، فلن تُرسل الرسالة حفاظا على الأمان. تدعم Mailbox.org [إكستشينج-أكتف‌سنك](https://en.wikipedia.org/wiki/Exchange_ActiveSync)، وكذلك تدعم معايير الوصول القياسية مثل IMAP و POP3.

عند Mailbox.org ميزة الإرث الرقميِّ لكلِّ الاشتراكات. يمكنك اختيار ما إذا كنت ترغب في تمرير أي من بياناتك إلى الورثة، بشرط أن يتقدموا بطلب رسمي ويُقدموا وصيتك القانونية. غير ذلك فيمكنك ترشيح شخص باسمه وعنوانه.

## مقدِّموا خدمة آخرون

يخزِّن مقدمِّو الخدمة هؤلاء بُرُدك معمَّاةً تعمية دون معرفة، وهذا جاعلهم خيارات جيِّدةً لتخزِّنها فيها. لكنهم لا يدعمون التشفير التام بين الطرفين (E2EE) عند إرسال الرسائل إلى مستخدمين في خدمات بريد إلكتروني أخرى.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

خدمة Tuta (التي كانت تُعرف سابقا باسم Tutanota) هي خدمة بريد إلكتروني تركز على الأمان والخصوصية من خلال استخدام التشفير. تعمل Tuta منذ عام 2011، وتتخذ من هانوفر في ألمانيا مقرا لها.

تبدأ الحسابات المجانية بسعة تخزين تبلغ 1 جيجابايت.

[:octicons-home-16: الصفحة الرئيسية](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="سياسة الخصوصية" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="الشروحات التفصيلية" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="المساهمة" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

لا يمكنك استخدام Tuta مع [تطبيقات البريد الأخرى](email-clients.md) مثل Outlook أو Thunderbird، لأنها لا تدعم [بروتوكول IMAP](https://tuta.com/support#imap). كما لا يمكنك [إضافة حسابات بريد ](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647)من خدمات أخرى داخل تطبيق Tuta – يمكنك استخدام الخدمة فقط من خلال تطبيقها أو موقعها الرسمي. ميزة [استيراد الرسائل الإلكترونية (Email import)](https://github.com/tutao/tutanota/issues/630) غير مدعومة حاليا، لكن من المخطط [توفيرها لاحقًا](https://tuta.com/blog/kickoff-import). يمكنك تصدير الرسائل [يدويا واحدة تلو الأخرى أو دفعة لكل مجلد](https://tuta.com/support#generalMail)، لكن هذه الطريقة قد تكون مرهقة إذا كان بريدك منظما في عدد كبير من المجلدات.

#### :material-check:{ .pg-green } النطاقات المخصَّصة والكنى

يمكن لمستخدمي الخطط المدفوعة في Tuta إنشاء 15 أو 30 عنوانا مستعارا (alias) حسب الخطة المختارة، مع إمكانية إنشاء عدد غير محدود من العناوين المستعارة عند استخدام [نطاق مخصص](https://tuta.com/support#custom-domain). لا تدعم Tuta ميزة [العناوين الفرعية](https://tuta.com/support#plus) (sub-addressing) مثل استخدام عنوان من نوع username+shopping@tuta.com، ولكن إذا كنت تستخدم نطاقك الخاص، يمكنك تفعيل ميزة [catch-all](https://tuta.com/support#settings-global)، التي تتيح استقبال جميع الرسائل الموجّهة إلى أي عنوان ضمن نطاقك (مثل أي_اسم@yourdomain.com) داخل بريدك الرئيسي.

#### :material-information-outline:{ .pg-blue } سُبُل الدفع الخاصَّة

تدعم Tuta الدفع المباشر عبر بطاقات الائتمان وPayPal فقط، ولكن يمكن استخدام [**العملات الرقمية**](cryptocurrency.md) لشراء بطاقات هدايا من خلال شراكتهم مع [ProxyStore](https://tuta.com/support/#cryptocurrency).

#### :material-check:{ .pg-green } أمن الحساب

تدعم Tuta ميزة [المصادقة الثنائية](https://tuta.com/support#2fa) باستخدام إما رموز TOTP (مثل تطبيق Authy أو Google Authenticator) أو مفاتيح أمان U2F (مثل YubiKey).

#### :material-check:{ .pg-green } أمن البيانات

تقوم Tuta بتشفير رسائلك، [وجهات اتصالك](https://tuta.com/support#encrypted-address-book)، [وتقويمك](https://tuta.com/support#calendar) باستخدام ما يُعرف بـ ["تشفير بدون وصول" (zero-access encryption)، وهو نظام يضمن أن لا أحد—حتى فريق Tuta نفسه—يمكنه الوصول إلى محتوى بياناتك، مما يعني أن البيانات لا يمكن قراءتها إلا من قبلك أنت فقط.](https://tuta.com/support#what-encrypted). ويعني هذا أن الرسائل والبيانات المخزَّنة في حسابك لا يقرؤها إلا أنت.

#### :material-information-outline:{ .pg-blue } تشفير البريد الإلكتروني

لا تستخدم Tuta بروتوكول [OpenPGP](https://tuta.com/support/#pgp). لا يمكن لحسابات Tuta استقبال رسائل مشفرة من بريد إلكتروني خارجي (غير تابع لـ Tuta)، إلا إذا تم إرسال الرسالة من خلال [صندوق Tuta المؤقت (temporary Tuta mailbox)](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } إنهاء الحسابات

ستقوم Tuta بـ[حذف الحسابات المجانية غير النشطة](https://tuta.com/support#inactive-accounts) بعد مرور ستة أشهر. ولك إعادة استخدام حساب ألغي تفعليه إن دفعت.

#### :material-information-outline:{ .pg-blue } وظائف إضافية

خدمة Tuta توفر النسخة المخصّصة للأعمال [للمؤسسات غير الربحية](https://tuta.com/blog/secure-email-for-non-profit) مجانا أو بسعر منخفض جدًا.

## المعايير

**مهم: نحن لا نتبع أي شركة من الشركات التي نرشّحها.** إلى جانب [المعايير الأساسية لدينا](about/criteria.md)، وضعنا شروطًا واضحة يجب أن يلتزم بها أي مزوّد بريد إلكتروني ليتم ترشيحه، مثل استخدام أحدث التقنيات واتباع أفضل ممارسات الأمان. ننصحك بالاطلاع على هذه القائمة قبل اختيار مزود بريد إلكتروني، والقيام ببحثك الخاص للتأكد من أن الخيار الذي تختاره هو الأنسب لك.

### تكنولوجي

هذه الميزات مهمة لتقديم خدمة تحمي خصوصيتك وتعمل بأفضل شكل ممكن. تأكد أن المزود يقدم الميزات التي تناسب احتياجاتك.

**الحد الأدنى لترشيح الخدمة:**

- يجب أن يتم تشفير بيانات حساب البريد الإلكتروني أثناء التخزين باستخدام تشفير يمنع حتى مزود الخدمة من الوصول إليها (تشفير بدون وصول "Zero-access encryption").
- يجب أن يوفر إمكانية تصدير (exporting) الرسائل بصيغة [MBOX](https://en.wikipedia.org/wiki/Mbox) أو ملفات .EML فردية وفقًا لمعيار [RFC5322](https://datatracker.ietf.org/doc/rfc5322).
- يجب أن تتيح الخدمة للمستخدمين إمكانية استخدام [اسم النطاق الخاص بهم](https://en.wikipedia.org/wiki/Domain_name). استخدام أسماء النطاقات المخصصة مهم للمستخدمين، لأنه يمنحهم استقلالية عن مزود الخدمة، في حال تدهورت الخدمة أو تم الاستحواذ عليها من قبل شركة لا تهتم بالخصوصية.
- يجب أن تعمل الخدمة على بنية تحتية مملوكة لها بالكامل، أي دون الاعتماد على مزودي خدمات بريد إلكتروني خارجيين.

**أحسن الاحتمالات:**

- يُفضّل أن يتمّ تشفير جميع بيانات الحساب (مثل جهات الاتصال، والتقويم، وغيرها) أثناء التخزين باستخدام تشفير يمنع مزوّد الخدمة من الوصول إليها (تشفير بدون وصول "Zero-access encryption").
- يُستحسن أن يكون التشفير القوي (مثل E2EE أو PGP) مدمجا داخل موقع البريد نفسه، حتى يتمكّن المستخدم من إرسال رسائل آمنة بسهولة.
- يُفضل أن تدعم الخدمة ميزة WKD لتسهيل العثور على مفاتيح OpenPGP العامة عبر بروتوكول HTTP. إذا كانت خدمة البريد تدعم ميزة WKD، يمكن لمستخدمي GnuPG الحصول على مفتاح التشفير العام لأي عنوان بريد باستخدام الأمر: `gpg --locate-key example_user@example.com`.
- إمكانية إرسال رسائل مشفرة إلى مستلمين ليس لديهم حساب، عبر صندوق بريد مؤقّت وآمن. تكون هذه الميزة مفيدة عندما تريد إرسال رسالة مشفّرة دون إرسال نسخة فعلية إلى بريد المستلم، بل يطّلع عليها من خلال رابط آمن. عادةً ما تبقى هذه الرسائل متاحة لفترة قصيرة فقط، ثم تُحذف تلقائيًا من الصندوق المؤقّت. ولا يحتاج المستلم إلى إعداد أي أدوات تشفير معقدة مثل OpenPGP لقراءة الرسالة.
- يُفضل أن تدعم الخدمة ميزة [العناوين الفرعية (sub-addressing)](https://en.wikipedia.org/wiki/Email_address#Sub-addressing)، والتي تتيح للمستخدم إضافة علامات مميّزة إلى بريده الإلكتروني (مثل username+shopping@example.com) لتنظيم الرسائل أو تصفيتها بسهولة.
- يجب أن تتيح الخدمة للمستخدمين إمكانية استخدام [اسم النطاق الخاص بهم](https://en.wikipedia.org/wiki/Domain_name)، مثل example.com، بدلاً من الاعتماد فقط على نطاق الخدمة (مثل user@tuta.com). هذه الميزة تمنح المستخدم تحكمًا أكبر في هويته الرقمية، وتُسهّل عليه نقل بريده إلى خدمة أخرى في المستقبل دون تغيير عنوانه. استخدام أسماء النطاقات المخصصة مهم للمستخدمين، لأنه يمنحهم استقلالية عن مزود الخدمة، في حال تدهورت الخدمة أو تم الاستحواذ عليها من قبل شركة لا تهتم بالخصوصية.
- دعم ميزة "Catch-all" أو "الأسماء المستعارة" (alias) للمستخدمين الذين يستخدمون نطاقهم الخاص.
- يُفضل أن تدعم الخدمة بروتوكولات الوصول إلى البريد الإلكتروني المعتمدة مثل IMAP وSMTP أو [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol)، وذلك حتى يتمكن المستخدم من استخدام تطبيقات البريد المختلفة لإرسال واستقبال الرسائل بسهولة. هذه البروتوكولات تتيح ربط البريد بخدمات أو تطبيقات خارجية بطريقة مرنة وآمنة. تضمن بروتوكولات الوصول القياسية (Standard access protocols) أن يتمكن المستخدمون من تنزيل كل رسائل بريدهم بسهولة، إذا قرروا الانتقال إلى مزود خدمة آخر.
- يُفضل أن تكون خدمات مزود البريد الإلكتروني متاحة من خلال [خدمة .onion](https://en.wikipedia.org/wiki/.onion)، وذلك لتوفير طبقة إضافية من الخصوصية وإخفاء الهوية عند الوصول إلى البريد، خاصة في البيئات التي تُقيد فيها حرية الوصول إلى الإنترنت.

### الخصوصية

نُفضل أن يجمع مزودو البريد الذين نوصي بهم أقل قدر ممكن من البيانات عن المستخدمين.

**أقل المتطلبات لترشيح الخدمة:**

- يجب أن تحمي الخدمة عنوان IP الخاص بالمرسِل، وذلك مثلا عبر إزالته أو حجبه من معلومات الرسالة التقنية (مثل حقل `Received`) التي يمكن أن تكشف عن موقع المرسِل أو جهازه.
- يجب أن تتيح الخدمة إنشاء حساب باستخدام اسم مستخدم وكلمة مرور فقط، دون الحاجة إلى تقديم معلومات شخصية مثل الاسم أو رقم الهاتف (PII).
- يجب أن تكون سياسة الخصوصية متوافقة مع متطلبات اللائحة العامة لحماية البيانات (GDPR)، والتي تضمن الشفافية في كيفية جمع البيانات واستخدامها.

**أحسن الاحتمالات:**

- يُفضل أن تدعم الخدمة [خيارات الدفع المجهولة](advanced/payments.md) مثل [العملات الرقمية](cryptocurrency.md)، أو الدفع نقدًا، أو باستخدام بطاقات الهدايا، وذلك لحماية هوية المستخدم عند الاشتراك
- يُفضل أن تكون الخدمة مستضافة في دولة تُطبق قوانين صارمة تحمي خصوصية البريد الإلكتروني.

### الأمان

خوادم البريد الإلكتروني تخزن وتُمرر بيانات شخصية مهمة، مثل الرسائل الخاصة والمرفقات، مما يجعل حمايتها أمرا ضروريا. من المهم أن يتبع مزودو الخدمة أعلى معايير الأمان المتعارف عليها، لضمان حماية بيانات المستخدمين وخصوصيتهم.

**أقل المتطلبات لترشيح الخدمة:**

- تأمين واجهة البريد عبر المتصفح (Webmail) باستخدام المصادقة الثنائية (2FA)، مثل [رموز TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp) المؤقتة.
- تشفير بدون وصول (Zero-access encryption)، وهو امتداد لتشفير البيانات أثناء التخزين (encryption at rest)، ويضمن أن حتى مزود الخدمة لا يمكنه الوصول إلى محتوى بياناتك، لأنه لا يمتلك مفاتيح فك التشفير. مزود الخدمة لا يمتلك مفاتيح فك التشفير الخاصة بالبيانات التي يحتفظ بها. هذا يمنع أي موظف سيئ النية من تسريب البيانات التي يمكنه الوصول إليها، أو أي جهة خارجية من كشف البيانات حتى لو تمكّنت من اختراق الخادم، لأن البيانات تكون مشفرة ولا يمكن قراءتها دون المفاتيح.
- دعم [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)، وهي تقنية تهدف إلى حماية نظام أسماء النطاقات (DNS) من التلاعب، من خلال التحقق من أن البيانات المستلمة من خوادم DNS أصلية ولم يتم تعديلها.
- ألا تظهر أي أخطاء أو ثغرات في بروتوكول TLS عند فحص الخدمة باستخدام أدوات مثل [Hardenize](https://hardenize.com)، أو [testssl.sh](https://testssl.sh)، أو [Qualys SSL Labs](https://ssllabs.com/ssltest). ويشمل ذلك خلو الخدمة من أخطاء في الشهادات الأمنية أو استخدام معايير تشفير ضعيفة (مثل مفاتيح DH غير الآمنة) والتي تسببت سابقا في ثغرات أمنية مثل [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- يفضّل أن يستخدم الخادم مجموعات تشفير قوية (cipher suites) تُعطي أولوية للأمان، وتدعم خصائص مثل forward secrecy والتشفير الموثوق (authenticated encryption).
- يجب أن تطبق الخدمة سياسة [MTA-STS](https://tools.ietf.org/html/rfc8461) و[TLS-RPT](https://tools.ietf.org/html/rfc8460) بشكل صحيح، لضمان تشفير الرسائل بين الخوادم، واكتشاف أي مشاكل أو محاولات لاعتراض الاتصال.
- يجب أن تدعم الخدمة سجلات [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities)الصالحة، وهي وسيلة لتعزيز أمان البريد الإلكتروني عبر التأكد من صحة الشهادات المستخدمة في التشفير، وتقليل خطر التلاعب أو التصيّد.
- يجب أن تدعم الخدمة سجلات [SPF ](https://en.wikipedia.org/wiki/Sender_Policy_Framework)و[DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) بشكل صحيح، لحماية البريد من التزييف والانتحال، وضمان أن الرسائل لم يتم التلاعب بها أثناء الإرسال.
- يجب أن تلتزم الخدمة بسياسة [DMARC](https://en.wikipedia.org/wiki/DMARC) فعالة لمنع انتحال البريد الإلكتروني، أو أن تستخدم [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) للتحقق من موثوقية الرسائل في حال إعادة توجيهها. إذا كانت خدمة البريد تستخدم مصادقة DMARC (DMARC authentication)، فيجب أن تكون السياسة مهيأة على `reject` (رفض) أو `quarantine` (عزل)، وذلك لضمان التعامل الصارم مع الرسائل غير الموثوقة ومنع انتحال الهوية.
- يُفضل أن تَستخدم الخدمة بروتوكول TLS 1.2 أو إصدارا أحدث، وأن تضع خطة للتوافق مع [RFC8996](https://datatracker.ietf.org/doc/rfc8996)، وهو المعيار الذي ينص على إيقاف استخدام الإصدارات القديمة والضعيفة من TLS مثل 1.0 و1.1، بهدف تحسين الأمان.
- دعم إرسال البريد عبر [SMTPS](https://en.wikipedia.org/wiki/SMTPS) (نسخة مشفرة من بروتوكول SMTP)، وذلك في حال استخدام SMTP.
- معايير أمان المواقع الإلكترونية مثل:
    - [سياسة النقل (Transpoort) الآمن الصارم عبر HTTPS](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - دعم ميزة [Subresource Integrity (SRI)](https://en.wikipedia.org/wiki/Subresource_Integrity) عند تحميل ملفات من نطاقات خارجية (external domains)، وهي آلية تتيح التحقق من أن الملفات لم يتم التلاعب بها أثناء تحميلها من مصادر خارجية، مما يعزز أمان الموقع.
- يجب أن تتيح الخدمة عرض الـ [Message Headers](https://en.wikipedia.org/wiki/Email#Message_header) ، لأنها تعد ميزة أساسية في تحليل البريد الإلكتروني، وتساعد في الكشف عن محاولات التصيّد أو التزوير من خلال تتبع مصدر الرسالة والمسارات التي مرت بها.

**أحسن الاحتمالات:**

- يُفضل أن تدعم الخدمة المصادقة باستخدام أجهزة مادية (hardware authentication)، مثل: U2F و[WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- يجب أن تدعم الخدمة [سجل CAA في DNS](https://tools.ietf.org/html/rfc6844)، إلى جانب دعم DANE، لحماية النطاق من الشهادات المزوّرة أو غير المصرح بها.
- يُفضّل أن تدعم الخدمة ميزة [ARC (سلسلة الاستلام الموثقة)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain)، وهي مفيدة خصوصا للمستخدمين الذين يرسلون رسائل إلى القوائم البريدية (mailing lists)، حيث تُمكن من الحفاظ على معلومات المصادقة عند إعادة توجيه الرسائل، وذلك وفقًا لمعيار [RFC8617](https://tools.ietf.org/html/rfc8617).
- يُستحسن أن تنشر الخدمة نتائج تدقيق أمني أجراه طرف ثالث موثوق، لإثبات التزامها بأعلى معايير الأمان والشفافية.
- برامج مكافآت الإبلاغ عن الثغرات (Bug Bounty)، أو وجود آلية منظمة للإفصاح عن الثغرات الأمنية والتعامل معها بشكل مسؤول.
- معايير أمان المواقع الإلكترونية مثل:
    - [سياسة أمان المحتوى (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### الثقة

لن تثق بأموالك مع شخص يستخدم هوية مزيفة، فلماذا تثق ببريدك الإلكتروني؟ يجب أن يكون مزودو الخدمة الذين نرشحهم شفافين بشأن من يملك ويدير الخدمة، لأن الثقة تبدأ من الوضوح. نرغب في أن تُصدر الخدمة تقارير شفافية دورية توضح عدد ونوع الطلبات الحكومية التي تتلقاها، وكيف تتعامل معها، لضمان الوضوح والثقة.

**الحد الأدنى لترشيح الخدمة:**

- فريق إداري أو مالك معروف ومُعلن بشكل علني.

**أحسن الاحتمالات:**

- تقارير شفافية دورية.

### التسويق

نحرص على أن يتبع مزودو البريد الذين نرشحهم أساليب تسويقية مسؤولة، لا تضلل المستخدمين ولا تبالغ في وعود الخصوصية.

**الحد الأدنى لترشيح الخدمة:**

- يجب أن تستضيف الخدمة أدوات التحليلات الخاصة بها داخليًا (دون استخدام أدوات خارجية مثل Google Analytics أو Adobe Analytics، ألخ.).
- يجب ألا تستخدم الخدمة أي أساليب تسويقية غير مسؤولة، والتي قد تشمل ما يلي:
    - ادعاءات بأن "التشفير غير قابل للاختراق". يجب استخدام التشفير مع الأخذ في الاعتبار أن سريته قد لا تدوم في المستقبل، خاصة مع تطور التقنيات التي قد تُمكن من كسره.
    - ضمانات بحماية الهوية بشكل كامل بنسبة 100٪. عندما يدعي أحدهم أن شيئا ما مضمون بنسبة 100٪، فهذا يعني ضمنا أنه لا يمكن أن يفشل أبدا — وهو أمر غير واقعي. نعلم أن المستخدمين قد يفصحون عن هويتهم دون قصد بطرق متعددة، مثلا.:
        - إعادة استخدام بيانات شخصية (مثل البريد أو الاسم المستعار) سبق استخدامها بدون أدوات إخفاء الهوية مثل Tor، مما يسهل الربط بين الهوية الحقيقية والنشاط
        - [بصمة المتصفح](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**أحسن الاحتمالات:**

- توثيق واضح وسهل القراءة لخطوات مثل إعداد المصادقة الثنائية (2FA)، وتوصيل البريد الإلكتروني ببرامج خارجية، واستخدام OpenPGP، وغيرها.

### ميزات إضافية

رغم أن هذه ليست شروطا أساسية، إلا أننا أخذنا بعين الاعتبار بعض الجوانب الإضافية التي تسهم في تحسين الخصوصية أو سهولة الاستخدام عند تقييم مزودي البريد الإلكتروني الذين نوصي بهم.
