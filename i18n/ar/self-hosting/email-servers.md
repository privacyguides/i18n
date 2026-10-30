---
title: خوادم البريد الإلكتروني
meta_title: "استضافة البريد الإلكتروني بنفسك - Privacy Guides"
icon: material/email
description: للقراء الذين لديهم خبرة تقنية أكبر، يمكن أن توفر استضافة البريد الإلكتروني بأنفسهم خصوصية إضافية، لأنها تمنحهم تحكما أكبر في بياناتهم.
cover: email.webp
---

<small>يحمي من التهديدات التالية:</small>

- [:material-server-network: مقدّمو الخدمات](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

يمكن لمسؤولي الأنظمة ذوي الخبرة المتقدمة التفكير في إعداد خادم بريد إلكتروني خاص بهم. تحتاج خوادم البريد الإلكتروني إلى متابعة وصيانة مستمرة للحفاظ على أمانها وضمان وصول الرسائل بشكل موثوق. بالإضافة إلى الحلول المتكاملة التالية، اخترنا بعض المقالات التي تشرح كيفية إعداد خادم بريد إلكتروني يدويًا:

- [إعداد خادم بريد إلكتروني باستخدام OpenSMTPD وDovecot وRspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd)(2019)
- [كيفية تشغيل خادم بريد إلكتروني خاص بك](https://www.c0ffee.net/blog/mail-server-guide)(أغسطس 2017)

## Stalwart

<div class="admonition recommendation" markdown>

![Stalwart logo](../assets/img/self-hosting/stalwart.svg){ align=right }

خادم Stalwart هو خادم بريد إلكتروني حديث نسبيا، مكتوب بلغة Rust، ويدعم بروتوكول JMAP بالإضافة إلى البروتوكولات التقليدية IMAP وPOP3 وSMTP. يوفر خيارات كثيرة لتخصيص الإعدادات، كما يأتي بإعدادات افتراضية مناسبة من حيث الأمان والميزات، مما يجعله سهل الاستخدام من البداية. يوفر واجهة لإدارته عبر الويب تدعم المصادقة الثنائية (2FA) باستخدام TOTP، ويتيح لك إضافة مفتاح PGP العام الخاص بك لتشفير جميع الرسائل الواردة.

[:octicons-home-16: Homepage](https://stalw.art){ .md-button .md-button--primary }
[:octicons-info-16:](https://stalw.art/docs/get-started){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/stalwartlabs){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/stalwartlabs){ .card-link title="Contribute" }

</div>

تتميز [طريقة تطبيق PGP](https://stalw.art/docs/encryption/overview) في Stalwart عن باقي حلول استضافة البريد الإلكتروني التي نوصي بها، وتتيح لك تشغيل خادم بريد إلكتروني خاص بك تُخزن فيه الرسائل بشكل مشفر، مما يقلل من خطر وصول أشخاص غير مصرح لهم إلى رسائلك. إذا أعددت أيضا Web Key Directory ‏(WKD) على نطاقك، واستخدمت برنامج بريد إلكتروني يدعم الـPGP وWKD لتشفير الرسائل الصادرة (مثل Thunderbird)، فهذه أسهل طريقة للحصول على توافق مع التشفير التام بين الطرفين (E2EE) عند استضافة بريدك الإلكتروني بنفسك، مما يتيح لك التواصل بشكل مشفر مع جميع مستخدمي [Proton Mail](../email.md#proton-mail).

لا يتضمن Stalwart واجهة مدمجة لاستخدام البريد الإلكتروني عبر الويب، لذلك ستحتاج إلى استخدام [برنامج بريد إلكتروني مستقل](../email-clients.md) أو استضافة واجهة بريد إلكتروني مفتوحة المصدر بنفسك، مثل تطبيق Mail من Nextcloud.

نستخدم Stalwart لإدارة بريدنا الإلكتروني الداخلي في Privacy Guides.

## Mailcow

<div class="admonition recommendation" markdown>

![Mailcow logo](../assets/img/self-hosting/mailcow.svg){ align=right }

خادم Mailcow هو خادم بريد إلكتروني متقدم، ومناسب جدا لمن لديهم خبرة في استخدام Linux. يوفر كل ما تحتاج إليه داخل حاوية Docker: خادم بريد إلكتروني يدعم DKIM، وحماية من الفيروسات والرسائل المزعجة، وواجهة لاستخدام البريد الإلكتروني عبر الويب مع دعم ActiveSync من خلال SOGo، بالإضافة إلى واجهة إدارة عبر الويب تدعم المصادقة الثنائية (2FA).

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="Contribute" }

</div>

## Mail-in-a-Box

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](../assets/img/self-hosting/mail-in-a-box.svg){ align=right }

سكربت Mail-in-a-Box هو سكربت يُسهل إعداد وتشغيل خادم بريد إلكتروني على Ubuntu بشكل تلقائي. يهدف إلى تسهيل إعداد خادم بريد إلكتروني خاص بك.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>
