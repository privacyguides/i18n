---
meta_title: "متصفحات ويب تحترم الخصوصية للحاسوب الشخصي والماك - Privacy Guides"
title: متصفحات الحاسوب المكتبي
icon: material/laptop
description: هذه المتصفحات التي تحمي الخصوصية هي ما نوصي به حاليا لتصفّح الإنترنت العادي (غير المجهول) على أجهزة الكمبيوتر.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: ترشيحات لمتصفحات تحافظ على الخصوصية (للكمبيوتر)
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://ar.wikipedia.org/wiki/%D9%81%D9%8A%D8%B1%D9%81%D9%83%D8%B3
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://ar.wikipedia.org/wiki/%D8%A8%D8%B1%D9%8A%D9%81_(%D9%85%D8%AA%D8%B5%D9%81%D8%AD_%D9%88%D9%8A%D8%A8)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>يوفّر حماية ضد المخاطر التالية:</small>

- [:material-account-cash: الاقتصاد القائم على تتبع المستخدمين](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

هذه هي متصفحات الويب المخصصة **لأجهزة الكمبيوتر المكتبي**، والإعدادات التي نوصي بها حاليًا لتصفح الإنترنت العادي (غير المجهول). نوصي باستخدام [متصفح Mullvad](#mullvad-browser) إذا كنت تهتم بالحصول على حماية قوية للخصوصية وإخفاء بصمة الجهاز (anti-fingerprinting) من اللحظة الأولى، و**[Firefox](#firefox)** لمن يتصفح الإنترنت بشكل عادي ويبحث عن بديل جيد لمتصفح Google Chrome، و**[Brave](#brave)** إذا كنت بحاجة إلى التوافق مع المتصفحات المبنية على Chromium.

إذا كنت بحاجة إلى تصفّح الإنترنت بشكل مجهول، فعليك استخدام [Tor](tor.md) بدلًا من ذلك. نقدم في هذه الصفحة بعض التوصيات الخاصة بالإعدادات، لكن يجب أن تعلم أن جميع المتصفحات — باستثناء متصفح Tor — يمكن تتبعها من قِبل *جهة ما* بطريقة أو بأخرى.

## متصفح Mullvad

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
متصفح Mullvad مبني على [متصفح Tor](tor.md#tor-browser)، لكن بدون الاتصال بشبكة Tor. يهدف هذا المتصفح إلى توفير تقنيات متصفح Tor الخاصة بـ <strong>إخفاء بصمة الجهاز</strong> لمستخدمي الـVPN، وهي من وسائل الحماية الأساسية ضد [:material-eye-outline: مراقبة الجمهور (Mass Surveillance)](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. يُطور هذا المتصفح من قِبل مشروع Tor، ويُوزع بواسطة [Mullvad](vpn.md#mullvad)، **ولا** يتطلب استخدام خدمة Mullvad VPN.

[:octicons-home-16: الصفحة الرئيسية](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="سياسة الخصوصية" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="الشرح التفصيلي" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>تحميل</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

مثل [متصفح Tor](tor.md)، صُمم متصفح Mullvad **لإخفاء بصمة الجهاز**، وذلك بجعل بصمة متصفحك متطابقة مع جميع مستخدمي Mullvad Browser. ويشمل إعدادات افتراضية وإضافات يتم ضبطها تلقائيا وفق مستويات الأمان المدمجة: *العادي*، *الأكثر أمانًا*، و*الأعلى أمانًا*.

لذلك، من الضروري عدم تعديل المتصفح بأي شكل من الأشكال، باستثناء تغيير [مستويات الأمان الافتراضية (security levels)](https://tb-manual.torproject.org/security-settings) فقط. عند تغيير مستوى الأمان (security level)، **يجب** دائمًا إعادة تشغيل المتصفح قبل متابعة استخدامه. وإلا، فقد لا تُطبَّق [إعدادات الأمان بشكل كامل](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw)، مما قد يعرّضك لخطر التتبع واستغلال الثغرات، مقارنة بما تتوقعه من مستوى الأمان الذي اخترته.

تعديل أي شيء غير مستوى الأمان يجعل متصفحك مختلفًا عن الآخرين، وهذا يلغـي فائدة استخدامه لحماية الخصوصية. إذا كنت تفضل تعديل إعدادات المتصفح بحرية، ولا تمانع إمكانية التتبع، فننصحك باستخدام [Firefox](#firefox) بدلًا منه.

### إخفاء بصمة الجهاز

**حتى بدون** استخدام [VPN](vpn.md)، يوفر متصفح Mullvad نفس مستوى الحماية من [سكربتات التتبع البسيطة (بصمة المتصفح)](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting)، تمامًا مثل المتصفحات الأخرى مثل Firefox مع [Arkenfox](#arkenfox-advanced) أو [Brave](#brave). متصفح Mullvad يوفر هذه الحماية تلقائيا، لكن ذلك يأتي على حساب بعض المرونة والراحة التي قد توفّرها المتصفحات الأخرى.

==للحصول على أقوى حماية ضد تتبّع البصمة، نوصي باستخدام متصفح Mullvad **إلى جانب** VPN==، سواء كان Mullvad أو أحد مزوّدي VPN الآخرين الذين نوصي بهم.  باستخدام VPN مع متصفح Mullvad، يصبح متصفحك وعنوان الـ IP مُشابهين لعدد كبير من المستخدمين، مما يساعدك على الاختفاء ضمن "الزحام" ويقلّل من فرص تتبّعك.  هذه الطريقة هي الوسيلة الوحيدة لتفادي أدوات التتبع المتقدمة، وهي نفس التقنية التي يعتمدها متصفح Tor لمنع التتبع.

يرجى ملاحظة أنه رغم إمكانية استخدام متصفح Mullvad مع أي مزوّد VPN، إلا أن وجود "مجموعة" من المستخدمين لتختلط بها يعتمد على أن مستخدمين آخرين على نفس الـVPN يستخدمون أيضًا متصفح Mullvad. وهذا الأمر يُرجّح أن يحدث مع Mullvad VPN أكثر من غيره من المزوّدين، خصوصًا في الفترة القريبة من إطلاق المتصفح. متصفح Mullvad لا يحتوي على VPN مدمج، ولا يتحقّق من أنك تستخدم VPN قبل بدء التصفّح، لذلك يجب إعداد اتصال الـVPN وتشغيله بشكل منفصل.

 يأتي متصفح Mullvad مزودا مسبقا بإضافتي *uBlock Origin* و*NoScript* لمتصفح الويب. رغم أننا عادةً لا ننصح بإضافة *إضافات جديدة* إلى [المتصفح](browser-extensions.md)، إلا أن الإضافات المثبّتة مسبقًا مع متصفح Mullvad يجب **عدم** حذفها أو تعديل إعداداتها الافتراضية، لأن القيام بذلك قد يجعل بصمة متصفحك مختلفة بوضوح عن باقي مستخدمي Mullvad Browser. يأتي المتصفح أيضا مزوّدا مسبقا بإضافة Mullvad Browser Extension، والتي *يمكنك* إزالتها بأمان دون أن يؤثر ذلك على بصمة المتصفح، إذا رغبت بذلك. كما أنه لا بأس في الاحتفاظ بها حتى إذا كنت لا تستخدم Mullvad VPN.

### الوضع الخفي

يعمل متصفح Mullvad في وضع التصفح الخفي بشكل دائم، أي أن سجل التصفح والكوكيز وبيانات المواقع الأخرى يتم مسحها تلقائيًا في كل مرة تغلق فيها المتصفح. سيتم الاحتفاظ بالمواقع المحفوظة (Bookmarks) وإعدادات المتصفح وإعدادات الإضافات، ولن تُحذف.

هذا الإجراء ضروري لمنع أساليب التتبع المتقدمة، لكنه يأتي على حساب بعض جوانب الراحة وبعض ميزات Firefox، مثل ميزة الحاويات متعددة الحسابات (Multi-Account Containers). تذكر أنه يمكنك دائما استخدام أكثر من متصفح. على سبيل المثال، يمكنك استخدام Firefox مع Arkenfox لتصفح بعض المواقع التي تحتاج إلى البقاء مسجّلًا فيها أو لا تعمل بشكل جيد مع متصفح Mullvad، واستخدام Mullvad Browser للتصفّح العام.

### Mullvad Leta

Mullvad Browser comes with [**Mullvad Leta**](search-engines.md#mullvad-leta) as the default search engine, which functions as a proxy to either Google or Brave search results (configurable on the Mullvad Leta homepage).

إذا كنت من مستخدمي Mullvad VPN، فهناك قدر من المخاطرة في استخدام خدمات مثل Mullvad Leta، لأنها تُقدم من نفس مزوّد خدمة الـVPN الذي تستخدمه. This is because Mullvad theoretically has access to your true IP address (via their VPN) and your search activity (via Leta); the latter is information a VPN is typically intended to separate. رغم أن Mullvad لا تجمع إلا القليل جدًا من المعلومات عن مستخدمي خدمة VPN أو Leta، فإنه من الأفضل التفكير في استخدام [محرك بحث آخر](search-engines.md) إذا كانت هذه المخاطرة تثير قلقك.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){ align=right }

Firefox يوفّر إعدادات قوية لحماية الخصوصية، مثل [الحماية المحسّنة من التتبع (Enhanced Tracking Protection)](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop)، والتي تساعد على حجب أنواع مختلفة من [أساليب التتبع](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: الصفحة الرئيسية](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="سياسية الخصوصية" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="الشرح التفصيلي" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="المساهمة" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>
- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">تنبيه</p>

عند تحميل Firefox من موقع Mozilla، يتم تضمين [رمز فريد](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) في الملف، ويرسل المتصفح هذا الرمز تلقائيًا من خلال خاصية القياس عن بُعد أو إرسال بيانات الاستخدام (Telemetry). الرمز لا يُضمَّن في النسخ التي تُحمّل من رابط إصدارات [Mozilla على FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### إعدادات Firefox الموصى بها

توجد هذه الخيارات ضمن :material-menu: → **الإعدادات**.

#### بحث

- [ ] أزل التحديد عن **عرض اقتراحات البحث**

قد لا تكون ميزة اقتراحات البحث متوفّرة في منطقتك.

اقتراحات البحث ترسل كل ما تكتبه في شريط العنوان إلى محرك البحث الافتراضي، سواء ضغطت على Enter ونفّذت البحث أو لا. عند تعطيل اقتراحات البحث، يمكنك التحكم بشكل أفضل في المعلومات التي يراها محرك البحث.

##### Firefox Suggest (متاح في الولايات المتحدة فقط)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) هي ميزة مشابهة لاقتراحات البحث، لكنها متوفرة فقط في الولايات المتحدة. نوصي بإيقاف هذه الميزة لنفس السبب الذي نوصي فيه بإيقاف اقتراحات البحث. إذا لم تظهر لك هذه الخيارات ضمن **شريط العنوان (Address Bar)**، فهذا يعني أنك لا تملك التجربة الجديدة ويمكنك تجاهل هذه التغييرات.

- [ ] أزل التحديد عن **الاقتراحات من Firefox**
- [ ] أزل التحديد عن **اقتراحات من الرعاة**

#### الخصوصية والأمان

##### حماية التتبع المتقدّمة

- فعِّل مستوى **الحماية الصارمة** في خيار حماية التتبع المتقدّمة (Enhanced Tracking Protection)

يوفّر لك هذا الإعداد الحماية من أدوات تتبّع وسائل التواصل الاجتماعي، وسكربتات بصمة المتصفح (مع ملاحظة أنه لا يحميك من *كل* أنواع التتبّع بالبصمة)، وبرمجيات التعدين الخفي (cryptominers)، وملفات تعريف الارتباط (الكوكيز) التي تتبعك عبر المواقع، وبعض أنواع المحتوى التتبّعي الأخرى. حماية التتبع المتقدّمة (ETP) توفّر حماية من العديد من التهديدات الشائعة، لكنها لا تمنع جميع أساليب التتبع، لأنها مصمّمة لتعمل دون التأثير على قابلية استخدام المواقع أو التسبّب في مشاكل أثناء التصفح.

##### مسح البيانات عند الإغلاق

إذا كنت ترغب في البقاء مسجّل الدخول في مواقع معيّنة، يمكنك إضافة استثناءات من خلال **ملفات تعريف الارتباط وبيانات المواقع (Cookies and Site Data)** ← **إدارة الاستثناءات (Manage Exceptions)**

- [x] فعِّل خيار **حذف الكوكيز وبيانات المواقع (Delete cookies and site data) عند إغلاق Firefox**

هذا الإعداد يوفّر لك الحماية من الكوكيز الدائمة، لكنه لا يحميك من الكوكيز التي يتم الحصول عليها خلال جلسة التصفح نفسها. عند تفعيل هذا الخيار، يمكنك بسهولة مسح الكوكيز الخاصة بالمتصفح بمجرد إعادة تشغيل Firefox. إذا كنت تزور موقعا بشكل متكرر وتريد البقاء مسجّل الدخول فيه، يمكنك إضافة استثناء خاص له.

##### إرسال بيانات الاستخدام

- [ ] أزل التحديد عن **السماح لـ Firefox بإرسال البيانات الفنية وبيانات التفاعل إلى Mozilla**
- [ ] قم بإيقاف خيار **السماح لـ Firefox بتجربة ميزات تجريبية (دراسات)**
- وفقا لسياسة الخصوصية الخاصة بـ Firefox من Mozilla،

وفقا لسياسة الخصوصية الخاصة بـ Firefox من Mozilla،

> يرسل Firefox بيانات تتعلّق بإصدار المتصفح واللغة المستخدمة، ونظام تشغيل الجهاز ومواصفات الجهاز، والذاكرة، ومعلومات أساسية حول الأعطال والأخطاء، بالإضافة إلى نتائج العمليات التلقائية مثل التحديثات، والحماية من المواقع الضارة، وتفعيل المنتج، إلى Mozilla. عند إرسال Firefox للبيانات، يتم تسجيل عنوان IP مؤقتا في سجلات خوادمنا.

بالإضافة إلى ذلك، تقوم خدمة حسابات Mozilla (Mozilla Accounts service) بجمع [بعض البيانات التقنية](https://mozilla.org/privacy/mozilla-accounts). إذا كنت تملك حسابًا لدى Mozilla، يمكنك تعطيل هذه الميزة أو رفض المشاركة من خلال الإعدادات:

1. افتح [إعدادات ملفك الشخصي على accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. أزل التحديد عن **جمع البيانات واستخدامها (Data Collection and Use)** ← **المساعدة في تحسين حسابات (Help improve Firefox Accounts) Firefox**

##### تفضيلات الإعلانات في المواقع

- [ ] أزل التحديد عن **السماح للمواقع بقياس الإعلانات بطريقة تحافظ على الخصوصية (privacy-preserving ad measuremen)**

مع إصدار Firefox 128، تمت إضافة ميزة جديدة تتعلق بـ[الإسناد المحافظ على الخصوصية](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA)، وقد تم [تفعيله افتراضيًا](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). تسمح PPA للمعلنين بقياس نجاح الإعلانات مباشرة من خلال المتصفح، دون الحاجة إلى أدوات التتبع التقليدية المبنية على JavaScript. نرى أن هذا السلوك لا يندرج بشكل مباشر ضمن المهام الأساسية لمتصفح المستخدم، كما أن تعطيله افتراضيًا في Arkenfox يشير إلى أنه من المناسب إبقاء هذه الميزة غير مفعّلة.

##### وضع HTTPS فقط

- فعّل **وضع HTTPS فقط لجميع النوافذ (windows)**

يساعد هذا في منعك من فتح مواقع لا تستخدم اتصالا مشفّرا (HTTP) عن طريق الخطأ. المواقع التي لا تدعم HTTPS أصبحت نادرة في الوقت الحالي، لذا فإن تفعيل هذا الخيار لن يؤثر كثيرًا — أو قد لا يؤثر إطلاقًا — على تصفحك اليومي.

##### DNS over HTTPS

إذا كنت تستخدم [ خدمة DNS over HTTPS ](dns.md):

- [x] فعِّل **أقصى حماية** واختر مزوّد DNS يناسبك

عند تفعيل "أقصى حماية"، يستخدم Firefox فقط خدمة DNS المشفّرة (DNS over HTTPS). وإذا لم يتمكّن من الاتصال بها، أو إذا قالت الخدمة إن الموقع الذي تحاول الوصول إليه غير موجود، فسيعرض المتصفح رسالة تحذير لحمايتك. هذا الخيار يمنع الشبكة (مثل الواي فاي الذي تتصل به) من التلاعب أو تقليل مستوى حماية خدمة DNS دون أن تعرف، وهو ما قد يعرّض خصوصيتك للخطر.

#### المزامنة

[فايرفوكس سينك (Firefox Sync)](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) تُمكنك من الوصول إلى بيانات التصفُّح الخاصة بك (مثل السجلّ، والإشارات المرجعيّة (Bookmarks)، وغيرهما) من جميع أجهزتك، وتَقوم بحمايتها من خلال التشفير التام بين الطرفين (E2EE).

### Arkenfox (متقدم)

<div class="admonition tip" markdown>
<p class="admonition-title">متصفح Mullvad يوفر حماية قوية ضد التتبع ببصمة المتصفح (anti-fingerprinting)</p>

يوفر متصفح Mullvad نفس مستوى الحماية من تتبع البصمة الذي يقدمه Arkenfox مباشرة دون الحاجة إلى إعدادات إضافية، كما لا يتطلّب استخدام خدمة Mullvad VPN للاستفادة من هذه الحماية. عند استخدامه مع VPN، يمكن لمتصفح Mullvad التصدي لأساليب التتبع المتقدمة التي لا يستطيع Arkenfox التعامل معها. يبقى Arkenfox خيارا أكثر مرونة، حيث يمكنك تخصيص إعداداته وإضافة استثناءات لمواقع تحتاج تسجيل الدخول الدائم إليها.

</div>

مشروع [Arkenfox](https://github.com/arkenfox/user.js) يقدّم إعدادات محسّنة ومختارة بعناية لتعزيز الخصوصية في متصفح Firefox. إذا [قررت](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) استخدام Arkenfox، فبعض [الإعدادات](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) قد تكون صارمة من وجهة نظر البعض، وقد تتسبب في عدم عمل بعض المواقع بشكل صحيح — لكن يمكنك [تعديلها بسهولة](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) لتناسب احتياجاتك.  ننصحك **بشدة** بتصفّح كامل محتوى [صفحة الويكي الخاصة بهم](https://github.com/arkenfox/user.js/wiki). يدعم Arkenfox كذلك ميزة [الحاويات](https://support.mozilla.org/kb/containers#w_for-advanced-users) في Firefox.

يركز Arkenfox على منع أساليب التتبع البسيطة، من خلال ميزة "عشوائية الرسم" (canvas randomization) — وهي تقنية تغيّر طريقة عرض الصور داخل صفحات الويب بشكل طفيف، بحيث يصعب على المواقع استخدام تلك الرسومات كوسيلة لتتبّعك — بالإضافة إلى إعدادات Firefox المدمجة لمقاومة تتبّع البصمة. على عكس Mullvad وTor، لا يسعى Arkenfox لجعل متصفحك يشبه متصفحات الآخرين، وهي الطريقة الوحيدة تقريبا لمنع التتبع المتقدم ببصمة المتصفح. تذكر أنه يمكنك دائمًا استخدام أكثر من متصفح. على سبيل المثال، يمكنك استخدام Firefox مع Arkenfox لبعض المواقع التي تثق بها أو تحتاج إلى البقاء مسجل الدخول فيها، واستخدام متصفح Mullvad لباقي استخداماتك اليومية.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

يحتوي متصفح Brave على مانع مدمج للإعلانات والتتبع، بالإضافة إلى [ميزات خصوصية عديدة](https://brave.com/privacy-features)، يتم تفعيل الكثير منها بشكل تلقائي.

بما أن Brave مبني على متصفح Chromium، فستجده مألوفًا وسهل الاستخدام، ويعمل بسلاسة مع أغلب المواقع.

[:octicons-home-16: الصفحة الرئيسية](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="سياسية الخصوصية" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="الشرح التفصيلي" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

يُضيف Brave ما يُعرف بـ [رمز إحالة (referral code)](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes) إلى اسم ملف التنزيل من موقع Brave الرسمي، ويُستخدم هذا الرمز لتتبع المصدر الذي تم تحميل المتصفح منه، مثل الرمز BRV002 في ملف باسم Brave-Browser-BRV002.pkg. يقوم برنامج التثبيت بعد ذلك بإرسال طلب إلى خادم Brave يتضمن رمز الإحالة، وذلك في نهاية عملية التثبيت. ننصحك، إذا كنت تشعر بالقلق من ذلك، أن تقوم بإعادة تسمية ملف التثبيت قبل فتحه، لتجنّب إرسال رمز الإحالة تلقائيًا إلى خوادم Brave.

</div>

### إعدادات Brave الموصى بها

توجد هذه الخيارات ضمن :material-menu: → **الإعدادات**.

#### Shields

يتضمّن Brave بعض وسائل الحماية من تتبّع البصمة ضمن ميزة [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) الخاصة به. من الأفضل تهيئة هذه الإعدادات [على مستوى جميع المواقع](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)، بدلاً من تعديلها لكل موقع على حدة.

إذا لزم الأمر، يمكنك تخفيف إعدادات Shields لمواقع معينة، لكننا نوصي بتفعيل الإعدادات التالية كإعداد افتراضي:

<div class="annotate" markdown>

اختر Aggressive (المستوى الشديد) في Trackers & ads blocking لحظر التتبع والإعلانات بفعالية أكبر

<details class="warning" markdown>
<summary>Use default filter lists</summary>

يمكنك في Brave تفعيل فلاتر حظر إضافية عبر الصفحة brave://adblock. لا نوصي باستخدام هذه الخاصية، من الأفضل الاكتفاء بالقوائم الافتراضية. استخدام قوائم تصفية إضافية قد يجعل متصفحك مختلفا عن باقي مستخدمي Brave، مما يزيد من احتمالية تتبّعك. كما أنه قد يعرّضك لمخاطر أمنية أكبر، إذا وُجدت ثغرة في Brave وتم إدخال قاعدة ضارة إلى إحدى تلك القوائم.

</details>

- [x] اختر **Strict** ضمن *Upgrade connections to HTTPS*
- [x] (إختياري) اختر **Block Scripts** (1)
- [x] فعل **Block fingerprinting**
- [x] اختر **Block third-party cookies**
- [x] فعل **Forget me when I close this site** (2)
- [] أزل التحديد عن جميع مكونات وسائل التواصل الاجتماعي

</div>

1. هذا الخيار يعطل JavaScript، مما قد يؤدي إلى تعطل العديد من المواقع أو عدم عملها بشكل صحيح. لإصلاح ذلك، يمكنك إضافة استثناءات لكل موقع على حدة، وذلك بالضغط على أيقونة الدرع (Shield) في شريط العنوان (Adress bar)، ثم إلغاء تفعيل هذا الخيار من قسم *Advanced controls*.
2. إذا كنت ترغب في البقاء مسجل الدخول في موقع معين تزوره باستمرار، يمكنك إضافة استثناء خاص لهذا الموقع بالضغط على أيقونة الدرع (Shield) في شريط العنوان (Adress bar)، ثم إلغاء تفعيل هذا الخيار من قسم *Advanced controls*.

#### الخصوصية والأمان

<div class="annotate" markdown>

- [x] Select **Don’t allow sites to use JavaScript optimization** under *Security* → *Manage JavaScript optimization & security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. عند تعطيل V8 optimizer، يتم تقليل فرص استغلال الثغرات الأمنية عن طريق إيقاف [*بعض*](https://grapheneos.social/@GrapheneOS/112708049232710156) أجزاء JavaScript Just-In-Time (JIT) compilation.

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity). ومع ذلك، فإن متصفح Brave **ليس** مقاوما لتتبع البصمة بنفس مستوى متصفح Tor، كما أن عدد مستخدمي Brave مع Tor أقل بكثير، مما يجعلك مميزًا ويسهل تتبعك. إذا كنت بحاجة إلى إخفاء هويتك بشكل قوي، ننصح باستخدام [متصفح Tor](tor.md#tor-browser).

##### جمع البيانات

-  [ ] أزل التحديد عن **Allow privacy-preserving product analytics (P3A)**
- [ ] أزل التحديد عن **Automatically send daily usage ping to Brave**
- [ ] أزل التحديد عن **Automatically send diagnostic reports**

#### Web3

ميزات Web3 في Brave قد تجعل متصفحك أكثر تميّزًا وأسهل في التتبع، وقد تزيد من احتمالات التعرّض للهجمات. ما لم تكن تستخدم أيا من هذه الميزات، يُفضل أن تقوم بتعطيلها.

- اختر **Extensions (no fallback)** ضمن *Default Ethereum wallet*
- اختر **Extensions (no fallback)** ضمن *Default Solana wallet*

#### الإضافات (قم بإيقاف كل الإضافات المدمجة غير الضرورية بالنسبة لك)

- [ ] قم بإيقاف كل الإضافات (Extensions) المدمجة غير الضرورية بالنسبة لك

#### محرك بحث

نوصي بإيقاف اقتراحات البحث (search suggestions) في Brave لنفس السبب الذي نوصي من أجله بإيقاف هذه الميزة في [Firefox](#search).

- [ ] أزل التحديد عن **عرض اقتراحات البحث**

#### نظام

<div class="annotate" markdown>

أزل التحديد عن Continue running background apps when Brave is closed لتعطيل تشغيل التطبيقات في الخلفية (1)

</div>

1. قد لا يظهر هذا الخيار في بعض الأنظمة.

#### Brave Sync

تتيح لك [Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) مزامنة بيانات التصفح الخاصة بك (مثل السجل، والإشارات المرجعية (Bookmarks)، وغيرها) والوصول إليها من جميع أجهزتك، دون الحاجة إلى إنشاء حساب، مع حمايتها باستخدام التشفير التام بين الطرفين (E2EE).

#### Brave Rewards and Wallet

تتيح لك **Brave Rewards** كسب عملة BAT (Basic Attention Token) الرقمية مقابل القيام ببعض الأنشطة داخل متصفح Brave، مثل مشاهدة الإعلانات أو دعم المواقع التي تزورها. تعتمد هذه الميزة على حساب تتم إدارته من قبل جهة خارجية (وليس من طرفك مباشرة)، كما تتطلّب التحقق من هويتك (إجراءات اعرف عميلك – KYC) من خلال عدد محدود من المزوّدين. لا نوصي باستخدام BAT كعملة رقمية خاصة، كما لا نوصي باستخدام [custodial wallet](advanced/payments.md#wallet-custody)، لذلك نُفضل تجنب هذه الميزة.

تعمل **Brave Wallet** محليا (Locally) على جهازك، لكنها لا تدعم أي عملات رقمية تركّز على الخصوصية، لذلك لا ننصح باستخدام هذه الميزة أيضا.

## المعايير

**نود أن نوضح أننا لا نتبع أيًّا من المشاريع التي نوصي بها.** نحن نعتمد على [معايير واضحة](about/criteria.md) ومجموعة شروط محددة تساعدنا في تقديم توصيات محايدة وموضوعية. قبل استخدام أي مشروع، تأكد من مراجعة هذه القائمة بعناية، وخصص بعض الوقت لإجراء بحثك الشخصي، فاختيارك الصحيح يبدأ من وعيك وفهمك لما تستخدمه.

### الحد الأدنى من المتطلبات

- يجب أن يكون البرنامج مفتوح المصدر (open-source software).
- يشترط أن يكون البرنامج قادرا على التحديث تلقائيا دون تدخل يدوي.
- يشترط أن يتلقى البرنامج تحديثات المحرك خلال 0–1 يوم من إصدارها من المشروع الأصلي (المصدر الرسمي للتطوير – upstream).
- يجب أن يكون متاحا على أنظمة Linux وmacOS وWindows.
- أي تغييرات تُجري لتحسين الخصوصية يجب ألا تضر بسهولة أو راحة استخدام المتصفح.
- يشترط حظر كوكيز الطرف الثالث (third-party cookies) تلقائيًا دون تدخل المستخدم.
- يجب أن يدعم [تجزئة الحالة (state partitioning)](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning)، وهي تقنية تفصل بيانات كل موقع عن الآخر للحد من التتبع بين المواقع.[^1]

### أحسن الاحتمالات

تمثل معاييرنا في أحسن الاحتمالات التصور المثالي لما ينبغي أن يقدمه المشروع الأفضل ضمن هذه الفئة. ليست جميع توصياتنا مُلزمة بتوفير كل هذه الميزات، لكن المشاريع التي تتوافق معها بشكل أكبر قد تُصنف في مرتبة أعلى، لأنها تقترب أكثر من المعايير التي نعتبرها نموذجا لأفضل مستوى ممكن.

- يُفضل أن يحتوي على ميزة مدمجة لحظر المحتوى (مثل الإعلانات وأدوات التتبع).
- ينبغي أن يوفر دعما لفصل الكوكيز بين المواقع المختلفة، كما هو الحال في ميزة [Multi-Account Containers](https://support.mozilla.org/kb/containers).
- يُفضل أن يدعم تطبيقات الويب القابلة للتثبيت (Progressive Web Apps)، وهي تطبيقات يمكن تشغيلها من المتصفح وتعمل وكأنها تطبيقات مستقلة على الجهاز، مثل تطبيقات الهاتف أو سطح المكتب (PC). تمكنك تطبيقات الويب القابلة للتثبيت (PWAs) من استخدام بعض المواقع كما لو كانت برامج مستقلة مثبتة على حاسوبك، دون الحاجة إلى فتح المتصفح في كل مرة. يعتبر استخدام PWAs خيارا أكثر أمانا من بعض التطبيقات المبنية على Electron، لأنها تعتمد على متصفحك وتستفيد من تحديثاته الأمنية المستمرة.
- يستحسن تجنب إضافة ميزات غير أساسية (bloatware) لا علاقة لها بالخصوصية، حتى لا تصبح عبئا غير مفيد على المتصفح.
- يُستحسن إيقاف جمع بيانات الاستخدام (telemetry) تلقائيا ما لم يوافق المستخدم صراحةً.
- يُستحسن أن يقدم المشروع خادم مزامنة مفتوح المصدر، لتمكين المستخدمين من تشغيله ذاتيا إذا رغبوا بذلك.
- يُفترض أن يعتمد بشكل افتراضي على [محرك بحث يحترم الخصوصية](search-engines.md).

[^1]: شرح Brave لهذا الموضوع مُفصل في [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state). [↩](#fnref:1){.footnote-backref}
