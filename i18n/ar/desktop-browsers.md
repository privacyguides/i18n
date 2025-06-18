---
meta_title: "متصفحات ويب تحترم الخصوصية للحاسوب الشخصي والماك - Privacy Guides"
title: "متصفحات الحاسوب المكتبي"
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

يأتي متصفح Mullvad مزوّدًا بمحرك البحث [**Mullvad Leta**](https://leta.mullvad.net) كخيار افتراضي، وهو يعمل كوسيط (proxy) لعرض نتائج البحث من Google أو Brave، ويمكنك اختيار المحرك الذي تفضّله من الصفحة الرئيسية لـ Mullvad Leta

إذا كنت من مستخدمي Mullvad VPN، فهناك قدر من المخاطرة في استخدام خدمات مثل Mullvad Leta، لأنها تُقدم من نفس مزوّد خدمة الـVPN الذي تستخدمه. وذلك لأن Mullvad يمكنها نظريا الوصول إلى عنوان IP الحقيقي الخاص بك (من خلال خدمة الـVPN)، وكذلك إلى نشاطك في البحث (عبر Leta)، وهي معلومات يُفترض أن تظل منفصلة عن بعضها عند استخدام VPN. رغم أن Mullvad لا تجمع إلا القليل جدًا من المعلومات عن مستخدمي خدمة VPN أو Leta، فإنه من الأفضل التفكير في استخدام [محرك بحث آخر](search-engines.md) إذا كانت هذه المخاطرة تثير قلقك.

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

If you use a [DNS over HTTPS provider](dns.md):

- [x] Select **Max Protection** and choose a suitable provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (advanced)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

</div>

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember that you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave is built upon the Chromium web browser project, so it should feel familiar and have minimal website compatibility issues.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

</div>

### Recommended Brave Configuration

توجد هذه الخيارات ضمن :material-menu: → **الإعدادات**.

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Shields' options can be downgraded on a per-site basis as needed, but by default we recommend setting the following:

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option disables JavaScript, which will break a lot of sites. To fix them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

#### Privacy and security

<div class="annotate" markdown>

- [x] Select **Don't allow sites to use the V8 optimizer** under *Security* → *Manage V8 security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Disabling the V8 optimizer reduces your attack surface by disabling [*some*](https://grapheneos.social/@GrapheneOS/112708049232710156) parts of JavaScript Just-In-Time (JIT) compilation.

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### Search engine

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] أزل التحديد عن **عرض اقتراحات البحث**

#### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running background apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

### Minimum Requirements

- Must be open-source software.
- Must support automatic updates.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Best-Case

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps (PWAs). PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
