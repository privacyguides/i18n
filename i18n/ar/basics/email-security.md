---
meta_title: "لماذا لا يُعد البريد الإلكتروني الخيار الأفضل للخصوصية والأمان - Privacy Guides"
title: أمان البريد الإلكتروني
icon: material/email
description: البريد الإلكتروني غير آمن من نواحٍ عديدة، وهذه بعض الأسباب التي تجعله ليس خيارنا الأول للتواصل الآمن.
---

البريد الإلكتروني وسيلة تواصل غير آمنة عمومًا. يمكنك تحسين أمان بريدك الإلكتروني باستخدام أدوات مثل OpenPGP، التي تضيف الـ End-to-End Encryption إلى رسائلك، لكن OpenPGP لا يزال يعاني من عدة عيوب مقارنة بالتشفير في تطبيقات المراسلة الأخرى.

لذلك، يُفضل استخدام البريد الإلكتروني لتلقي الرسائل المرتبطة بالمعاملات (مثل الإشعارات، ورسائل التحقق، وإعادة تعيين كلمات المرور، وغيرها) من الخدمات التي تسجل فيها عبر الإنترنت، وليس للتواصل مع الآخرين.

## نظرة عامة على تشفير البريد الإلكتروني

الطريقة المعتادة لإضافة الـ End-to-End Encryption إلى رسائل البريد الإلكتروني بين مزودي بريد مختلفين هي استخدام OpenPGP. توجد تطبيقات مختلفة لمعيار الـ OpenPGP، وأكثرها شيوعا هما [GnuPG](../encryption.md#gnu-privacy-guard) و[OpenPGP.js](https://openpgpjs.org).

حتى إذا كنت تستخدم OpenPGP، فهو لا يدعم [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy)، ما يعني أنه إذا سُرق المفتاح الخاص بك أو بالمستلم في أي وقت، فستصبح جميع الرسائل السابقة المشفّرة به مكشوفة. لهذا السبب، نوصي باستخدام [تطبيقات المراسلة الفورية](../real-time-communication.md) التي تدعم forward secrecy بدلًا من البريد الإلكتروني للتواصل بين الأشخاص كلما أمكن ذلك.

يوجد معيار آخر شائع لدى الشركات يُسمى [S/MIME](https://en.wikipedia.org/wiki/S/MIME)، لكنه يتطلب شهادة صادرة عن [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (ولا تصدر جميع الجهات شهادات S/MIME، وغالبا ما يتطلب ذلك دفع رسوم سنوية). في بعض الحالات، يكون استخدامه أسهل من الـ PGP لأنه مدعوم في تطبيقات البريد الإلكتروني الشائعة مثل Apple Mail و[Google Workplace](https://support.google.com/a/topic/9061730) و[Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). لكن S/MIME لا يحل مشكلة عدم وجود الـ forward secrecy، كما أنه ليس أكثر أمانا من الـ PGP بشكل ملحوظ.

## ما هو معيار «Web Key Directory»؟

يتيح معيار [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) لتطبيقات البريد الإلكتروني العثور على مفتاح الـ OpenPGP الخاص بعناوين بريد إلكتروني أخرى، حتى إذا كانت مستضافة لدى مزود مختلف. ستطلب تطبيقات البريد الإلكتروني التي تدعم الـ WKD من خادم المستلم مفتاحا استنادًا إلى اسم النطاق الخاص بعنوان البريد الإلكتروني. على سبيل المثال، إذا أرسلت رسالة إلى `jonah@privacyguides.org`، فسيطلب تطبيق البريد الإلكتروني الذي تستخدمه من `privacyguides.org` مفتاح الـ OpenPGP الخاص بـ Jonah، وإذا كان لدى `privacyguides.org` مفتاح لهذا الحساب، فسيتم تشفير رسالتك تلقائيا.

In addition to the [email clients we recommend](../email-clients.md) which support WKD, some webmail providers also support WKD. يعتمد نشر مفتاحك *الخاص* في WKD ليستخدمه الآخرون على إعدادات النطاق لديك. إذا كنت تستخدم [مزود بريد إلكتروني](../email.md#openpgp-compatible-services) يدعم WKD، مثل Proton Mail أو Mailbox Mail، فيمكنه نشر مفتاح الـ OpenPGP الخاص بك على نطاقه نيابةً عنك.

إذا كنت تستخدم نطاقك الخاص، فستحتاج إلى إعداد WKD بشكل منفصل. إذا كنت تتحكم في اسم نطاقك، فيمكنك إعداد WKD بغض النظر عن مزود البريد الإلكتروني الذي تستخدمه. إحدى الطرق السهلة للقيام بذلك هي استخدام ميزة الـ "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" من خادم `keys.openpgp.org`: أضف سجل CNAME إلى النطاق الفرعي `openpgpkey` في نطاقك، واجعله يشير إلى `wkd.keys.openpgp.org`، ثم ارفع مفتاحك إلى [keys.openpgp.org](https://keys.openpgp.org). بدلا من ذلك، يمكنك [استضافة WKD بنفسك على خادم الويب الخاص بك](https://wiki.gnupg.org/WKDHosting).

إذا كنت تستخدم نطاقا مشتركًا من مزود لا يدعم الـ WKD، مثل `@gmail.com`، فلن تتمكن من مشاركة مفتاح OpenPGP مع الآخرين بهذه الطريقة.

### ما تطبيقات البريد الإلكتروني التي تدعم End-to-End Encryption؟

يمكن استخدام مزودي البريد الإلكتروني الذين يسمحون باستخدام بروتوكولات مثل IMAP وSMTP مع أي من [تطبيقات البريد الإلكتروني التي نوصي بها](../email-clients.md). اعتمادا على طريقة المصادقة (authentication)، قد يؤدي ذلك إلى تقليل الأمان إذا كان مزود البريد أو تطبيق البريد الإلكتروني لا يدعم الـ [OAuth](account-creation.md#sign-in-with-oauth) أو تطبيق bridge، لأن [المصادقة متعددة العوامل (multifactor authentication)](multi-factor-authentication.md) لا تكون ممكنة عند استخدام المصادقة بكلمة المرور فقط.

### كيف أحمي مفاتيحي الخاصة؟

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Email Metadata Overview

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as `To`, `From`, `Cc`, `Date`, and `Subject`. There are also a number of hidden headers included by many email clients and providers that can reveal information about your account.

Client software may use email metadata to show who a message is from and what time it was received. Servers may use it to determine where an email message must be sent, among [other purposes](https://en.wikipedia.org/wiki/Email#Message_header) which are not always transparent.

### Who Can View Email Metadata?

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Sometimes email servers will also use third-party services to protect against spam, which generally also have access to your messages.

### Why Can't Metadata be E2EE?

Email metadata is crucial to the most basic functionality of email (where it came from, and where it has to go). E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
