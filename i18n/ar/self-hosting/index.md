---
title: الاستضافة بنفسك
meta_title: "استضافة البرامج والخدمات بنفسك - Privacy Guides"
description: للقراء الذين لديهم خبرة تقنية أكبر، يمكن أن توفر استضافة البرامج والخدمات بأنفسهم خصوصية إضافية، لأنها تمنحهم تحكما كاملًا في بياناتهم.
cover: router.webp
---

<small>يحمي من التهديدات التالية:</small>

- [:material-server-network: مقدّمو الخدمات](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

يمكن أن تساعدك **استضافة** البرامج والخدمات بنفسك على تحقيق مستوى أعلى من الخصوصية من خلال السيادة الرقمية، خاصة بالاستغناء عن الاعتماد على الخوادم السحابية التي يتحكم فيها مطورو البرامج أو الشركات التي توفرها. نقصد بالاستضافة بنفسك تشغيل التطبيقات وتخزين البيانات على أجهزتك الخاصة.

تتطلب استضافة خدماتك بنفسك خبرة تقنية متقدمة وفهما عميقا للمخاطر المرتبطة بها. عندما تستضيف الخدمات بنفسك، سواء لنفسك أو للآخرين، فإنك تتحمّل مسؤوليات إضافية لم تكن مضطرا لتحملها من قبل. قد يؤدي إعداد برامج الخصوصية التي تستضيفها بنفسك بشكل غير صحيح إلى تعريض خصوصيتك لمخاطر أكبر مقارنةً باستخدام خدمة تدعم التشفير التام بين الطرفين (End-to-End Encryption)، لذلك يُفضل تجنب الاستضافة بنفسك إذا لم تكن لديك الخبرة الكافية للقيام بها.

## :material-dns: فلترة الـ DNS

<div class="grid cards" markdown>

- ![AdGuard Home logo](../assets/img/self-hosting/adguard-home.svg){ .twemoji loading=lazy } [AdGuard Home](dns-filtering.md#adguard-home)
- ![Pi-Hole logo](../assets/img/self-hosting/pi-hole.svg){ .twemoji loading=lazy } [Pi-Hole](dns-filtering.md#pi-hole)

</div>

[تعرف على المزيد :material-arrow-right-drop-circle:](dns-filtering.md)

## :material-email:خوادم البريد الإلكتروني

<div class="grid cards" markdown>

- ![Stalwart logo](../assets/img/self-hosting/stalwart.svg){ .twemoji loading=lazy } [Stalwart](email-servers.md#stalwart)
- ![Mailcow logo](../assets/img/self-hosting/mailcow.svg){ .twemoji loading=lazy } [Mailcow](email-servers.md#mailcow)
- ![Mail-in-a-Box logo](../assets/img/self-hosting/mail-in-a-box.svg){ .twemoji loading=lazy } [Mail-in-a-Box](email-servers.md#mail-in-a-box)

</div>

[تعرف على المزيد :material-arrow-right-drop-circle:](email-servers.md)

## :material-file-multiple-outline: إدارة الملفات

<div class="grid cards" markdown>

- ![PhotoPrism logo](../assets/img/self-hosting/photoprism.svg){ .twemoji loading=lazy } [PhotoPrism](file-management.md#photoprism)
- ![FreedomBox logo](../assets/img/self-hosting/freedombox.svg){ .twemoji loading=lazy } [FreedomBox](file-management.md#freedombox)
- ![Nextcloud logo](../assets/img/self-hosting/nextcloud.svg){ .twemoji loading=lazy } [Nextcloud](file-management.md#nextcloud)

</div>

[تعرف على المزيد :material-arrow-right-drop-circle:](file-management.md)

## :material-form-textbox-password: إدارة كلمات المرور

### Vaultwarden

<div class="admonition recommendation" markdown>

![Vaultwarden logo](../assets/img/self-hosting/vaultwarden.svg#only-light){ align=right }
![Vaultwarden logo](../assets/img/self-hosting/vaultwarden-dark.svg#only-dark){ align=right }

خادم **Vaultwarden** هو بديل لخادم المزامنة الخاص بـ[Bitwarden](../passwords.md#bitwarden)، مكتوب بلغة Rust ومتوافق مع تطبيقات Bitwarden الرسمية. وهو مناسب جدا للاستضافة بنفسك، خاصةً عندما لا يكون تشغيل [الخدمة الرسمية](https://github.com/bitwarden/server) التي تستهلك الكثير من موارد الجهاز خيارًا عمليًا.

[:octicons-repo-16: Repository](https://github.com/dani-garcia/vaultwarden#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title="Contribute" }

</div>

## :material-account-supervisor-circle-outline: شبكات التواصل الاجتماعي

يمكن أن تساعدك استضافة نسختك الخاصة من برنامج شبكة تواصل اجتماعي على تجاوز [الرقابة على مستوى الخادم](../social-networks.md#censorship-resistance) التي قد يفرضها مسؤول خادم عام أو فريق إدارته.

### Mastodon

<div class="admonition recommendation" markdown>

![Mastodon logo](../assets/img/social-networks/mastodon.svg){ align=right }

شبكة **Mastodon** هي شبكة تواصل اجتماعي تعتمد على بروتوكولات الويب المفتوحة وبرامج مجانية ومفتوحة المصدر. تستخدم بروتوكول:simple-activitypub: ActivityPub اللامركزي.

[:octicons-home-16:](https://joinmastodon.org){ .card-link title="Homepage" }
[:octicons-info-16:](https://docs.joinmastodon.org/admin/prerequisites){ .card-link title="Admin Documentation" }

</div>

يدعم Mastodon [التكامل مع شبكة Tor](https://docs.joinmastodon.org/admin/optional/tor) للتعامل مع الحالات الأكثر تعقيدا، مثل تعرض مزود الاستضافة نفسه للرقابة. لكن هذا قد يجعل الوصول إلى محتواك مقتصرا على الخوادم الأخرى التي تدعم Tor، كما هو الحال مع معظم الخدمات المخفية الأخرى.

يستفيد Mastodon من مجتمع كبير ونشط من المستخدمين الذين يستضيفونه بأنفسهم، كما تتوفر وثائق شاملة تشرح كيفية إدارته. بينما تتطلب العديد من المنصات الأخرى التي تستخدم ActivityPub خبرة تقنية كبيرة لتشغيلها وحل مشكلاتها، يتميّز Mastodon بإصدارات مستقرة ومختبرة جيدا. ويمكن عموما لأي شخص يعرف كيفية استخدام سطر الأوامر في Linux واتباع التعليمات خطوة بخطوة تشغيله بأمان ودون مشكلات.

### Element

<div class="admonition recommendation" markdown>

![Element logo](../assets/img/social-networks/element.svg){ align=right }

تطبيق **Element** هو التطبيق الرئيسي لبروتوكول **:simple-matrix: Matrix**، وهو معيار مفتوح يتيح التواصل بشكل لامركزي من خلال غرف دردشة مترابطة بين خوادم مختلفة.

[:octicons-home-16:](https://element.io){ .card-link title="Homepage" }
[:octicons-info-16:](https://element-hq.github.io/synapse/latest){ .card-link title="Admin Documentation" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

</div>

## :material-flip-to-front: واجهات المستخدم

يمكن أن تساعدك استضافة نسختك الخاصة من واجهة ويب على تجاوز قيود عدد الطلبات التي قد تواجهها عند استخدام النسخ العامة التي تشهد ضغطا كبيرا من المستخدمين. من المهم أيضا أن يستخدم أشخاص آخرون نسختك، حتى يصعب تمييز نشاطك عن نشاط بقية المستخدمين. يجب أن تنتبه إلى مكان وطريقة استضافة نسختك، لأن نشاط المستخدمين الآخرين سيكون مرتبطا بخادمك.

<div class="grid cards" markdown>

- ![Redlib logo](../assets/img/frontends/redlib.svg){ .lg .middle .twemoji } [**Redlib (Reddit)**](../frontends.md#redlib)

  ---

  [:octicons-info-16:](https://github.com/redlib-org/redlib#deployment){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Source Code" }

- ![Invidious logo](../assets/img/frontends/invidious.svg#only-light){ .twemoji }![Invidious logo](../assets/img/frontends/invidious-dark.svg#only-dark){ .twemoji } [**Invidious (YouTube)**](../frontends.md#invidious)

  ---

  [:octicons-home-16:](https://invidious.io){ .card-link title="Homepage" }
  [:octicons-info-16:](https://docs.invidious.io/installation){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }

- ![Piped logo](../assets/img/frontends/piped.svg){ .twemoji } [**Piped (YouTube)**](../frontends.md#piped)

  ---

  [:octicons-info-16:](https://docs.piped.video/docs/self-hosting){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }

</div>

## المزيد من الأدوات...

توفر بعض الأدوات التي نوصي بها في مقالات أخرى من الموقع خيار الاستضافة بنفسك أيضا. يمكنك التفكير في هذا الخيار إذا قرأت وثائق هذه الأدوات وكنت واثقا من قدرتك على تشغيلها بنفسك.

<div class="grid cards" markdown>

- ![Peergos logo](../assets/img/cloud/peergos.svg){ .twemoji } [**Peergos**](../cloud.md#peergos)

  ---

  [:octicons-home-16:](https://peergos.org){ .card-link title="Homepage" }
  [:octicons-info-16:](https://github.com/peergos/peergos#usage---running-locally-to-log-in-to-another-instance){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }

- ![Addy.io logo](../assets/img/email-aliasing/addy.svg){ .twemoji } [**Addy.io**](../email-aliasing.md#addyio)

  ---

  [:octicons-home-16:](https://addy.io){ .card-link title="Homepage" }
  [:octicons-info-16:](https://addy.io/self-hosting){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }

- ![SimpleLogin logo](../assets/img/email-aliasing/simplelogin.svg){ .twemoji } [**SimpleLogin**](../email-aliasing.md#simplelogin)

  ---

  [:octicons-home-16:](https://addy.io){ .card-link title="Homepage" }
  [:octicons-info-16:](https://github.com/simple-login/app#prerequisites){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }

- ![Ente logo](../assets/img/photo-management/ente.svg){ .twemoji } [**Ente Photos**](../photo-management.md#ente-photos)

  ---

  [:octicons-home-16:](https://ente.com){ .card-link title="Homepage" }
  [:octicons-info-16:](https://ente.com/help/self-hosting/){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Source Code" }

- ![CryptPad logo](../assets/img/document-collaboration/cryptpad.svg){ .twemoji } [**CryptPad**](../document-collaboration.md#cryptpad)

  ---

  [:octicons-home-16:](https://cryptpad.fr){ .card-link title="Homepage" }
  [:octicons-info-16:](https://docs.cryptpad.org/en/admin_guide/index.html){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Source Code" }

- ![Send logo](../assets/img/file-sharing-sync/send.svg){ .twemoji } [**Send**](../file-sharing.md#send)

  ---

  [:octicons-home-16:](https://send.vis.ee){ .card-link title="Homepage" }
  [:octicons-info-16:](https://github.com/timvisee/send/blob/master/docs/deployment.md){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Source Code" }

- ![LibreTranslate logo](../assets/img/language-tools/libretranslate.png){ .twemoji } [**LibreTranslate**](../language-tools.md#libretranslate)

  ---

  [:octicons-home-16:](https://libretranslate.com){ .card-link title="Homepage" }
  [:octicons-info-16:](https://docs.libretranslate.com){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/LibreTranslate/LibreTranslate){ .card-link title="Source Code" }

- ![Miniflux logo](../assets/img/news-aggregators/miniflux.svg#only-light){ .twemoji }![Miniflux logo](../assets/img/news-aggregators/miniflux-dark.svg#only-dark){ .twemoji } [**Miniflux**](../news-aggregators.md#miniflux)

  ---

  [:octicons-home-16:](https://miniflux.app){ .card-link title="Homepage" }
  [:octicons-info-16:](https://miniflux.app/docs/index.html#administration-guide){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/miniflux/v2){ .card-link title="Source Code" }

- ![Standard Notes logo](../assets/img/notebooks/standard-notes.svg){ .twemoji } [**Standard Notes**](../notebooks.md#standard-notes)

  ---

  [:octicons-home-16:](https://standardnotes.com){ .card-link title="Homepage" }
  [:octicons-info-16:](https://standardnotes.com/help/47/can-i-self-host-standard-notes){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/standardnotes){ .card-link title="Source Code" }

- ![PrivateBin logo](../assets/img/pastebins/privatebin.svg){ .twemoji } [**PrivateBin**](../pastebins.md#privatebin)

  ---

  [:octicons-home-16:](https://privatebin.info){ .card-link title="Homepage" }
  [:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/blob/master/doc/Installation.md){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Source Code" }

- ![Paaster logo](../assets/img/pastebins/paaster.svg){ .twemoji } [**Paaster**](../pastebins.md#paaster)

  ---

  [:octicons-home-16:](https://paaster.io){ .card-link title="Homepage" }
  [:octicons-info-16:](https://github.com/WardPearce/paaster#deployment){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/WardPearce/paaster){ .card-link title="Source Code" }

- ![SimpleX Chat logo](../assets/img/messengers/simplex.svg){ .twemoji } [**SimpleX Chat**](../real-time-communication.md#simplex-chat)

  ---

  [:octicons-home-16:](https://simplex.chat){ .card-link title="Homepage" }
  [:octicons-info-16:](https://simplex.chat/docs/server.html){ .card-link title="Admin Documentation" }
  [:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Source Code" }

</div>
