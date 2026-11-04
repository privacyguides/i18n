---
title: إضافات المتصفح (Browser Extensions)
icon: material/puzzle-outline
description: يمكن لهذه الإضافات تحسين تجربة تصفحك وحماية خصوصيتك.
cover: browser-extensions.webp
---

<small>يحمي من التهديدات التالية:</small>

- [:material-account-cash:رأسمالية المراقبة](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

بشكل عام، ننصح بتقليل عدد إضافات المتصفح قدر الإمكان لتقليل الـ attack surface. تملك هذه الإضافات صلاحيات واسعة داخل متصفحك، وتتطلب منك الثقة بمطوريها، وقد [تجعل تمييزك عن غيرك أسهل](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)، و[تُضعف](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) عزل المواقع التي تتصفحها عن بعضها.

ومع ذلك، توفر بعض الإضافات ميزات قد تفوق فوائدها هذه العيوب في بعض الحالات، خاصة عندما يتعلق الأمر بـ[حظر المحتوى](basics/common-threats.md#mass-surveillance-programs).

لا تثبت إضافات لا تحتاج إليها حاليا، أو إضافات تؤدي وظائف موجودة بالفعل في متصفحك. على سبيل المثال، لا يحتاج مستخدمو [Brave](desktop-browsers.md#brave) إلى تثبيت uBlock Origin، لأن Brave Shields يوفر بالفعل الوظائف نفسها.

## أدوات حظر المحتوى

### uBlock Origin

<div class="admonition recommendation" markdown>

![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ align=right }

أداة uBlock Origin أداة مشهورة  لحظر المحتوى، ويمكنها مساعدتك في حظر الإعلانات وأدوات التتبع والبرامج النصية المستخدمة في الـ Browser Fingerprinting.

[:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)
- [:fontawesome-brands-opera: أوبرا](https://addons.opera.com/en/extensions/details/ublock/)

</details>

</div>

ننصح بالرجوع إلى [دليل المطور](https://github.com/gorhill/uBlock/wiki/Blocking-mode) واختيار أحد «أوضاع التشغيل». قد تؤدي إضافة المزيد من قوائم التصفية إلى إبطاء الأداء، و[زيادة فرص استغلال الثغرات الأمنية](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

إليك بعض [قوائم التصفية](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) الأخرى التي قد ترغب في إضافتها:

- [x] انتقل إلى **Privacy** > **AdGuard URL Tracking Protection** وتأكد من تفعيلها
- أضف [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

### uBlock Origin Lite

تتوفر أيضًا نسخة أخف من إضافة uBlock Origin باسم «Lite»، لكنها تقدم ميزات أقل مقارنةً بالنسخة الأصلية. ومع ذلك، تتميز ببعض المزايا التي لا تتوفر في النسخة الكاملة، لذا قد يكون من الأفضل اختيارها إذا...

- ...كنت لا ترغب في منح أي إضافة صلاحيات كاملة «لقراءة بيانات المواقع الإلكترونية وتعديلها»، حتى لو كانت إضافة موثوقة مثل uBlock Origin
- ...كنت تريد أداة لحظر المحتوى تستهلك موارد أقل من الذاكرة والمعالج (CPU)[^1]
- ...كان متصفحك يدعم فقط الإضافات التي تستخدم Manifest V3. وهذا هو الحال مع متصفح Chrome[^2].

<div class="admonition recommendation" markdown>

![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ align=right }

أداة uBlock Origin Lite هي أداة لحظر المحتوى متوافقة مع Manifest V3. مقارنةً بإضافة _uBlock Origin_ الأصلية، لا تحتاج هذه الإضافة إلى صلاحيات واسعة «لقراءة البيانات وتعديلها» حتى تعمل، مما يقلّل من خطر تعرّض متصفحك لـ[:material-bug-outline: هجمات سلبية](basics/common-threats.md#security-and-privacy){ .pg-orange } في حال إضافة قاعدة ضارة إلى إحدى قوائم التصفية.

[:octicons-repo-16: Repository](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uBlockOrigin/uBOL-home/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/cimighlppcgcoapaliogpjjdehbnofhn)
- [:simple-safari: Safari](https://apps.apple.com/app/id6745342698)

</details>

</div>

لا ننصح باستخدام هذا الإصدار من uBlock Origin إلا إذا كنت لا ترغب في إضافة قوائم تصفية غير الموجودة بشكل افتراضي، ولا تحتاج إلى ميزات متقدمة مثل [dynamic filtering](https://github.com/gorhill/ublock/wiki/dynamic-filtering:-quick-guide) وأداة لتسجيل الـ (network logger). تعود هذه القيود إلى طريقة تصميم Manifest V3، خاصةً أنه يفرض حدا أقصى لعدد قواعد التصفية، ويقيد قدرة الإضافات على جلب موارد من مصادر خارجية.[^3]

يوفر هذا الإصدار ثلاثة مستويات لحظر المحتوى: يعمل مستوى الـ "Basic" دون الحاجة إلى صلاحيات خاصة لعرض محتوى المواقع وتعديله، بينما يحتاج مستويا "Optimal" و"Complete" إلى هذه الصلاحيات الواسعة، لكنهما يوفران حظرا أفضل للمحتوى بفضل قواعد إضافية لإخفاء العناصر غير المرغوب فيها على صفحات الويب، وإمكانية حقن أكواد JavaScript صغيرة (scriptlets).

إذا اخترت "Optimal" أو "Complete" كوضع التصفية الافتراضي، فستطلب الإضافة صلاحية قراءة محتوى جميع المواقع التي تزورها وتعديله. ومع ذلك، يمكنك اختيار "Optimal" أو "Complete" لكل موقع على حدة، عن طريق تحريك شريط التمرير في النافذة المنبثقة للإضافة أثناء زيارة الموقع. عندها، ستطلب الإضافة صلاحية قراءة محتوى هذا الموقع وتعديله فقط. لذلك، إذا أردت الاستفادة من uBlock Origin Lite دون منحها صلاحيات إضافية، فمن الأفضل ترك الوضع الافتراضي على "Basic"، واختيار مستوى حظر أعلى فقط للمواقع التي لا يكون فيها هذا المستوى كافيا.

لا تُحدث قوائم الحظر في uBlock Origin Lite إلا عند صدور تحديث جديد للإضافة من متجر المتصفح، ولا يمكنك تحديث هذه القوائم وقتما تشاء. توفر Google [مراجعة سريعة](https://developer.chrome.com/docs/webstore/skip-review) لتحديثات قوائم التصفية، لذلك تصلك هذه التحديثات عادةً مع كل إصدار جديد من uBlock Origin Lite، والذي كان يصدر كل يومين إلى 7 أيام. لكن التحديثات تقتصر على ما يُعرف باسم «[القواعد الآمنة](https://developer.chrome.com/docs/extensions/reference/api/declarativeNetRequest#safe_rules)»، لذلك قد لا تُحدث القوائم التي تستخدم تقنيات متقدمة بنفس السرعة.

### AdGuard

ننصح مستخدمي iOS باستخدام [Safari](mobile-browsers.md#safari-ios)، لكن للأسف، الإصدار الوحيد من uBlock Origin الذي يدعمه هو Lite. لحسن الحظ، يوفر AdGuard بديلا مناسبًا:

<div class="admonition recommendation" markdown>

![AdGuard logo](assets/img/browsers/adguard.svg){ align=right }

اضافة AdGuard for iOS إضافة مجانية ومفتوحة المصدر لحظر المحتوى في Safari، وتستخدم واجهة [Content Blocker API](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker) المدمجة في المتصفح.

[:octicons-home-16: Homepage](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1047223162)

</details>

</div>

Additional filter lists do slow things down and may increase your attack surface, so only apply what you need. AdGuard for iOS has some premium features; however, standard Safari content blocking is free of charge.

## Criteria

- Must not replicate built-in browser or OS functionality.
- Must directly impact user privacy, i.e. must not simply provide information.

[^1]: uBlock Origin Lite _itself_ will consume no resources, because it uses newer APIs which make the browser process the filter lists natively, instead of running JavaScript code within the extension to handle the filtering. However, this resource advantage is only [theoretical](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-(FAQ)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo), because it's possible that standard uBlock Origin's filtering code is more efficient than your browser's native filtering code. This has not yet been benchmarked.

[^2]: [Brave](https://brave.com/blog/brave-shields-manifest-v3/) and [Opera](https://xcancel.com/Opera_Security/status/2066543496001888753) have committed to maintain MV2 support for as long as they're able to.

[^3]: This is starting to change, as MV3 extensions can now request to use scripts. This has enabled [AdGuard](https://adguard.com/en/blog/adguard-browser-extension-v5-2.html) to propose to import custom filters list by the url, as opposed to having to manually paste the rules, as is the case with uBOL.
