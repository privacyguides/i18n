---
meta_title: "متصفحات ويب تركز على الخصوصية لأنظمة أندرويد وiOS – Privacy Guides"
title: متصفحات الهواتف
icon: material/cellphone-information
description: المتصفحات التالية هي خياراتنا الموصى بها لتصفح الإنترنت بشكل عادي وغير مجهول على الهواتف المحمولة.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: توصيات لمتصفحات الهواتف التي تحافظ على الخصوصية
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Cromite
    image: /assets/img/browsers/cromite.svg
    url: https://cromite.org
    applicationCategory: Web Browser
    operatingSystem:
      - أندرويد
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: المتصفح
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>يُوفر الحماية من التهديدات التالية:</small>

- [:material-account-cash: رأسمالية المراقبة](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

هذه هي **متصفحات الويب للهواتف الذكية** والإعدادات التي نوصي بها حاليا لتصفح الإنترنت العادي (غير المجهول). إذا كنت بحاجة إلى تصفّح الإنترنت بشكل مجهول، فعليك استخدام [Tor](tor.md) بدلًا من ذلك.

## Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

يحتوي متصفح Brave على مانع مدمج للإعلانات والتتبع، بالإضافة إلى [ميزات خصوصية عديدة](https://brave.com/privacy-features)، يتم تفعيل الكثير منها بشكل تلقائي.

بما أن Brave مبني على متصفح Chromium، فستجده مألوفًا وسهل الاستخدام، ويعمل بسلاسة مع أغلب المواقع.

[:octicons-home-16: الصفحة الرئيسية](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="سياسية الخصوصية" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="الشرح التفصيلي" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### إعدادات Brave الموصى بها

متصفح Tor هو الوسيلة الوحيدة التي تتيح لك تصفح الإنترنت دون الكشف عن هويتك فعليا. عند استخدام متصفح Brave، نوصي بتغيير الإعدادات التالية لحماية خصوصيتك من أطراف معينة، لكن جميع المتصفحات الأخرى، باستثناء [متصفح Tor](tor.md#tor-browser)، يمكن تتبعها من قِبل *شخص ما* بطريقة أو بأخرى.

=== "أندرويد"

    يمكن العثور على هذه الخيارات في :material-menu: → **Settings**→ **Brave Shields & privacy**.

=== "iOS"

    يمكن العثور على هذه الخيارات في :fontawesome-solid-ellipsis: → **Settings**→ **Shields & Privacy**.

#### الإعدادات الافتراضية لـ Brave shields

يتضمّن Brave بعض وسائل الحماية من تتبّع البصمة ضمن ميزة [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) الخاصة به. من الأفضل تهيئة هذه الإعدادات [على مستوى جميع المواقع](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)، بدلاً من تعديلها لكل موقع على حدة.

يمكنك تعديل إعدادات الـ (Shields) لكل موقع على حدة حسب ما تحتاج، لكن بشكل عام ننصحك باستخدام الإعدادات التالية كبداية:

=== "أندرويد"

    <div class="annotate" markdown>

    - [x] اختر **Aggressive** تحت خيار *Block trackers & ads*
    - [x] اختر **Auto-redirect AMP pages **
    - [x] اختر **Auto-redirect tracking URLs**
    - [x] اختر **Require all connections to use HTTPS (strict)** تحت خيار *Upgrade connections to HTTPS*
    - \[x\] (اختياري) اختر **Block Scripts** (1)
    - [x] اختر **Block third-party cookies** تحت خيار *Block Cookies*
    - [x] اختر **Block Fingerprinting**
    - [x] اختر **Prevent fingerprinting via language settings**

    <details class="warning" markdown>
    <summary>استخدم قوائم الحجب الجاهزة (default filter lists)</summary>

    يتيح لك متصفح Brave اختيار قوائم حجب محتوى إضافية من خلال قائمة **Content Filtering** أو صفحة الإعدادات`brave://adblock`. ننصح بعدم استخدام هذه الميزة، وبدلا من ذلك، حافظ على قوائم الحجب الافتراضية. استخدام قوائم تصفية إضافية قد يجعل متصفحك مختلفا عن باقي مستخدمي Brave، مما يزيد من احتمالية تتبّعك. كما أنه قد يعرّضك لمخاطر أمنية أكبر، إذا وُجدت ثغرة في Brave وتم إدخال قاعدة ضارة إلى إحدى تلك القوائم.

    </details>

    - [x] اختر **Forget me when I close this site**

    </div>

    1. هذا الخيار يعطل JavaScript، مما قد يؤدي إلى تعطل العديد من المواقع أو عدم عملها بشكل صحيح. لإصلاح ذلك، يمكنك إضافة استثناءات لكل موقع على حدة، وذلك بالضغط على أيقونة الدرع (Shield) في شريط العنوان (Adress bar)، ثم إلغاء تفعيل هذا الخيار من قسم *Advanced controls*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] اختر **Aggressive** تحت خيار *Trackers & Ads Blocking*
    - [x] اختر **Strict** تخت خيار *Upgrade Connections to HTTPS*
    - [x] اختر **Auto-Redirect AMP pages**
    - [x] اختر **Auto-Redirect Tracking URLs**
    - \[x\] (اختياري) اختر **Block Scripts** (1)
    - [x] اختر **Block Fingerprinting**
    - [x] اختر **Site Tabs Closed** تحت خيار *Auto Shred*

    <details class="warning" markdown>
    <summary>استخدم قوائم الحجب الجاهزة (default filter lists)</summary>

    يتيح لك متصفح Brave اختيار قوائم حجب محتوى إضافية من خلال قائمة **Content Filtering**. ننصح بعدم استخدام هذه الميزة، وبدلا من ذلك، حافظ على قوائم الحجب الافتراضية. استخدام قوائم تصفية إضافية قد يجعل متصفحك مختلفا عن باقي مستخدمي Brave، مما يزيد من احتمالية تتبّعك. كما أنه قد يعرّضك لمخاطر أمنية أكبر، إذا وُجدت ثغرة في Brave وتم إدخال قاعدة ضارة إلى إحدى تلك القوائم.

    </details>

    </div>

    1. هذا الخيار يعطل JavaScript، مما قد يؤدي إلى تعطل العديد من المواقع أو عدم عملها بشكل صحيح. لإصلاح ذلك، يمكنك إضافة استثناءات لكل موقع على حدة، وذلك بالضغط على أيقونة الدرع (Shield) في شريط العنوان (Adress bar)، ثم إلغاء تفعيل هذا الخيار من قسم *Advanced controls*.

##### مسح بيانات التصفح (لأجهزة أندرويد فقط)

- [x] اختر **Clear data on exit**

##### حجب وسائل التواصل الاجتماعي (لأجهزة أندرويد فقط)

- [ ] ألغِ تفعيل جميع مكونات وسائل التواصل الاجتماعي

#### إعدادات إضافية للخصوصية

=== "أندرويد"

    <div class="annotate" markdown>

    - [x] اختر **Disable non-proxied UDP** تحت خيار [*WebRTC IP handling policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (إختياري) اختر **No protection** تحت خيار *Safe Browsing*  (1)
    - [ ] أزل التحديد عن **Allow sites to check if you have payment methods saved**
    - [ ] Uncheck **Javascript optimization & security** under the setting with the same name
    - [x] اختر **Close tabs on exit**
    -  [ ] أزل التحديد عن **Allow privacy-preserving product analytics (P3A)**
    - [ ] أزل التحديد عن **Automatically send diagnostic reports**
    - [ ] أزل التحديد عن **Automatically send daily usage ping to Brave**

    </div>

    1. في نسخة أندرويد من Brave، ميزة ["التصفح الآمن"](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) **لا تستخدم** بروكسي لإخفاء هويتك عند [التحقق من الروابط](https://developers.google.com/safe-browsing/v4/update-api#checking-urls)، بعكس نسخة الـ Desktop التي توفر هذا المستوى من الخصوصية. أي أن Google قد ترى عنوان IP الخاص بك وتقوم بتسجيله عند استخدام هذه الميزة. ميزة "التصفح الآمن" لا تعمل على أجهزة أندرويد التي لا تحتوي على خدمات Google Play.

=== "iOS"

    -  [ ] أزل التحديد عن **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] أزل التحديد عن **Automatically send daily usage ping to Brave**

#### Leo

يمكن العثور على هذه الخيارات في :material-menu: → **Settings** → **Leo**.

<div class="annotate" markdown>

- [ ] أزل التحديد عن *Show autocomplete suggestions in address bar** (1)

</div>

1. هذا الخيار غير متوفر في تطبيق Brave على iOS.

#### محركات البحث

يمكن العثور على هذه الخيارات في :material-menu:/:fontawesome-solid-ellipsis: → **Settings** → **Search engines**.

- [ ] أزل التحديد عن **عرض اقتراحات البحث**

#### Brave Sync

تتيح لك [Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) مزامنة بيانات التصفح الخاصة بك (مثل السجل، والإشارات المرجعية (Bookmarks)، وغيرها) والوصول إليها من جميع أجهزتك، دون الحاجة إلى إنشاء حساب، مع حمايتها باستخدام التشفير التام بين الطرفين (E2EE).

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Cromite logo](assets/img/browsers/cromite.svg){ align=right }

Cromite هو متصفح مبني على Chromium ويأتي مزودا بمانع إعلانات مدمج، وحماية من بصمة المتصفح (وهي تقنية تُستخدم لتتبعك عبر الإنترنت بناء على خصائص جهازك ومتصفحك)، بالإضافة إلى تحسينات أخرى في [الخصوصية والأمان](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). هو مشروع فرعي (fork) من متصفح Bromite، الذي لم يعد قيد التطوير.

[:octicons-home-16: الصفحة الرئيسية](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="سياسة الخصوصية" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="الشروحات التفصيلية" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### الإعدادات الموصى بها

يمكن العثور على هذه الخيارات في :material-menu: → :gear: **Settings** → **Privacy and security**.

#### بيانات التصفح

- [x] اختر **Close all open tabs on exit**

#### وضع التصفح الخفي

- [x] اختر **Open external links in incognito**

#### الأمان

- [x] اختر **Always use secure connections**

يساعد هذا في منعك من فتح مواقع لا تستخدم اتصالا مشفّرا (HTTP) عن طريق الخطأ. المواقع التي لا تدعم HTTPS أصبحت نادرة في الوقت الحالي، لذا فإن تفعيل هذا الخيار لن يؤثر كثيرًا — أو قد لا يؤثر إطلاقًا — على تصفحك اليومي.

#### إعدادات Adblock Plus

يمكن العثور على هذه الخيارات في :material-menu: → :gear: **Settings** → **Adblock Plus settings**.

يحتوي متصفح Cromite على نسخة مُعدلة من Adblock Plus، مع تفعيل EasyList تلقائيا، بالإضافة إلى إمكانية اختيار قوائم تصفية إضافية من خلال قائمة **Filter lists**.

استخدام قوائم إضافية قد يجعلك تبرز بين مستخدمي Cromite الآخرين، وقد يزيد من خطر التعرض لهجمات إذا تم إدخال قاعدة خبيثة في إحدى القوائم التي تستخدمها.

- \[x\] (اختياري) اختر **Enable anti-circumvention and snippets**

يُضيف هذا الخيار قائمة إضافية في Adblock Plus قد تُحسن من فعالية حجب المحتوى في متصفح Cromite. تنطبق هنا نفس التحذيرات بخصوص التميز عن بقية المستخدمين وزيادة احتمال التعرض لهجمات.

#### إعدادات Adblock (الإصدار القديم)

يمكن العثور على هذه الخيارات في :material-menu: → :gear: **Settings** → **Legacy Adblock settings**.

- [] ألغ تفعيل خيار التحديث التلقائي (autoupdate setting)

هذا الخيار يوقف البحث عن تحديثات لقائمة فلاتر الإعلانات (adblock filter) التابعة لـ Bromite، لأنها لم تعد مدعومة أو محدثة.

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Blink engine (the core component of Chromium) like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

في أجهزة iOS، يكون Safari هو المتصفح الأساسي المُثبت مسبقا. يتضمن Safari مجموعة من [ميزات الخصوصية](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios)، مثل [منع التتبع الذكي (Intelligent Tracking Prevention)](https://webkit.org/blog/7675/intelligent-tracking-prevention)، وعرض الصفحات في علامات تبويب (tabs) خاصة مؤقتة ومعزولة عن نشاط التصفح العادي، وحماية من بصمة المتصفح (وهي تقنية تستخدمها بعض المواقع للتعرف على جهازك من خلال خصائصه الفنية حتى بدون ملفات تعريف الارتباط "Cookies")، عن طريق إظهار إعدادات نظام موحدة لجعل الأجهزة تبدو متشابهة، إضافة إلى توليد بصمة عشوائية ( fingerprint randomization) للمزيد من الحماية، وميزة Private Relay المتوفرة فقط لمشتركي iCloud+ المدفوعين، والتي تُخفي عنوان Ip وتشفر حركة التصفح.

[:octicons-home-16: التنزيلات](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="سياسية الخصوصية" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="الشرح التفصيلي" }

</details>

</div>

### إعدادات Safari الموصى بها

يمكن العثور على خيارات الخصوصية والأمان التالية في :gear: **Settings** → **Apps** → **Safari**.

#### السماح لـ Safari بالوصول إلى

ضمن **Siri**:

- [ ] أوقف ميزة **Learn from this App**
- [ ] أوقف ميزة **Show in App**
- [ ] أوقف ميزة **Show on Home Screen**
- [ ] أوقف ميزة **Suggest App**

عند تعطيل هذا الخيار لن يستخدم Siri سجل التصفح أو نشاطك في Safari لتقديم اقتراحات أو تذكيرات.

#### بحث

- [ ] أوقف ميزة **Search Engine Suggestions**

عند تفعيل هذا الخيار، يتم إرسال كلمات البحث التي تكتبها في شريط العنوان إلى محرك البحث الذي اخترته في Safari مما قد يؤثر على خصوصيتك. عند تعطيل اقتراحات البحث، يمكنك التحكم بشكل أفضل في المعلومات التي يراها محرك البحث.

#### الملفات الشخصية

يوفر Safari ميزة إنشاء ملفات شخصية متعددة، بحيث يمكنك فصل التصفح الشخصي عن العمل أو أي استخدام آخر. جميع ملفات تعريف الارتباط (الكوكيز)، وسجل التصفح، وبيانات المواقع تكون منفصلة لكل ملف شخصي. استخدم ملفا شخصيا منفصلا لكل غرض — مثلا: واحد للتسوق، وآخر للعمل، وآخر للدراسة — لتحسين الخصوصية وتنظيم التصفح.

#### الخصوصية والأمان

- [x] Enable **Prevent Cross-Site Tracking**

هذا الخيار يقوم بتفعيل ميزة ["منع التتبع الذكي" (ITP) ](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp)في WebKit، والتي تساعد على تقليل قدرة المواقع على تتبعك عبر الإنترنت. تعمل هذه الميزة على منع التتبع من خلال الذكاء الاصطناعي الموجود على جهازك، دون إرسال بياناتك للخوادم، ما يعزز الخصوصية. تمنحك ITP (منع التتبع الذكي) حماية جيدة من معظم أساليب التتبع المنتشرة، لكنها لا تغلق جميع الطرق بالكامل، وذلك لتفادي تعطيل تجربة المستخدم على المواقع.

- [x] شغل ميزة **اRequire Face ID/Touch ID to Unlock Private Browsing**

يتيح لك هذا الخيار حماية التصفح الخاص ببصمة الإصبع، أو الوجه، أو رقم سري، حتى لا يتمكن أحد من الوصول إليه أثناء عدم استخدامك للجهاز.

- [ ] Disable **Fraudulent Website Warning**

This setting uses Google Safe Browsing (or Tencent Safe Browsing for users in mainland China or Hong Kong) to protect you while you browse. As such, your IP address may be logged by your Safe Browsing provider. Disabling this setting will disable this logging, but you might be more vulnerable to known phishing sites.

- [x] Enable **Not Secure Connection Warning**

This setting shows a warning screen if your connection to a website isn't using HTTPS. Safari will automatically try to upgrade the site to HTTPS, so you should only see this when there is no HTTPS connection available.

- [ ] Disable **Highlights**

Apple's privacy policy for Safari states:

> When visiting a webpage, Safari may send information calculated from the webpage address to Apple over OHTTP to determine if relevant highlights are available.

#### Settings for Websites

Under **Camera**

- [x] Select **Ask**

Under **Microphone**

- [x] Select **Ask**

Under **Location**

- [x] Select **Ask**

These settings ensure that websites can only access your camera, microphone, or location after you explicitly grant them access.

#### Other Privacy Settings

These options can be found in :gear: **Settings** → **Apps** → **Safari** → **Advanced**.

##### Fingerprinting Mitigations

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### Privacy Preserving Ad Measurement

- [ ] Disable **Privacy Preserving Ad Measurement**

Ad click measurement has traditionally used tracking technology that infringes on user privacy. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

The feature has little privacy concerns on its own, so while you can choose to leave it on, we consider the fact that it's automatically disabled in Private Browsing to be an indicator for disabling the feature.

#### Always-on Private Browsing

Open Safari and tap the Tabs button, located in the bottom right. Then, expand the :material-format-list-bulleted: Tab Groups list.

- [x] Select **Private**

Safari's Private Browsing mode offers additional privacy protections. Private Browsing uses a new [ephemeral](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) session for each tab, meaning tabs are isolated from one another. There are other smaller privacy benefits with Private Browsing too, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed in to sites. This may be an inconvenience.

#### iCloud Sync

Synchronization of Safari History, Tab Groups, iCloud Tabs and saved passwords are E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Go to :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] Turn on **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend setting Safari's default download location to a local folder on your device. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

### الحد الأدنى من المتطلبات

- يشترط أن يكون البرنامج قادرا على التحديث تلقائيا دون تدخل يدوي.
- يجب أن يتم تحديث محرك المتصفح بسرعة فور صدور تحديثات من المصدر الرئيسي، لضمان الأمان والأداء.
- من الضروري أن يوفر المتصفح ميزة حظر الإعلانات والمحتوى المزعج.
- أي تغييرات تُجري لتحسين الخصوصية يجب ألا تضر بسهولة أو راحة استخدام المتصفح.
