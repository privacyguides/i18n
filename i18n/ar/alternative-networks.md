---
title: "الشبكات البديلة"
icon: material/vector-polygon
description: تتيح لك هذه الأدوات الوصول إلى شبكات أخرى غير شبكة الويب العالمية.
cover: alternative-networks.webp
---

<small>يحمي من التهديدات التالية:</small>

- [:material-server-network: مقدّمو الخدمات](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-eye-outline: المراقبة الجماعية](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }
- [:material-account-cash:رأسمالية المراقبة](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

## شبكات إخفاء الهوية

عند الحديث عن شبكات إخفاء الهوية، نود التأكيد على أن [Tor](advanced/tor-overview.md) هو خيارنا الأول. فهي شبكة إخفاء الهوية الأكثر استخداما، والأكثر خضوعا للدراسة والبحث، ويجري تطويرها باستمرار. قد يؤدي استخدام شبكات أخرى إلى تعريض [:material-incognito: هويتك المجهولة](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } للخطر بشكل أكبر، إلا إذا كنت تعرف جيدا ما تفعله.

### Tor

<div class="admonition recommendation" markdown>

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

شبكة **Tor** هي مجموعة من الخوادم التي يديرها متطوعون، وتتيح لك الاتصال بالإنترنت مجانا مع حماية خصوصيتك وتعزيز أمانك. ويمكن للأفراد والمؤسسات مشاركة المعلومات عبرها باستخدام «خدمات .onion الخفية»، وذلك دون نهك خصوصيتهم. لأن حظر حركة البيانات عبر Tor وتتبعها أمر صعب، تُعد Tor أداة فعالة لتجاوز [:material-close-outline: الرقابة](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

</div>

الطريقة التي ننصح بها للاتصال بشبكة Tor هي استخدام متصفح Tor الرسمي، وقد شرحناه بالتفصيل في صفحة مخصصة له:

[معلومات عن متصفح Tor :material-arrow-right-drop-circle:](tor.md){ .md-button .md-button--primary } [شرح مفصّل عن Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md){ .md-button }

يمكنك الاتصال بشبكة Tor باستخدام أدوات أخرى، لكن اختيار الأداة المناسبة يعتمد على Threat Model الخاص بك. إذا كنت تستخدم Tor بشكل عادي، ولا تقلق من أن يجمع مزود خدمة الإنترنت أدلة ضدك، فمن المحتمل أن يكون استخدام تطبيقات مثل [Orbot](#orbot) أو متصفحات الهاتف للاتصال بشبكة Tor مناسبا لك. استخدامك لـ Tor في حياتك اليومية لا يحميك فقط، بل يساعد في حماية الآخرين أيضا. كلما زاد عدد المستخدمين، أصبحت شبكة Tor أكثر قوة، وانخفضت قدرة مزودي الإنترنت والحكومات على تتبع الأفراد أو وصمهم باستخدامها. ساهم في كسر الصورة النمطية السلبية واجعل الخصوصية عادة طبيعية للجميع.

<div class="admonition example" markdown>
<p class="admonition-title">جربه الآن!</p>

يمكنك محاولة الاتصال بموقع _Privacy Guides_ عبر شبكة Tor على الرابط [xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion](http://www.xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion).

</div>

#### Orbot

<div class="admonition recommendation" markdown>

![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }

تطبيق Orbot هو تطبيق للهواتف يوجّه حركة الإنترنت من أي تطبيق على جهازك عبر شبكة Tor.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title="Documentation" }
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)
- [:simple-fdroid: F-Droid](https://guardianproject.info/fdroid)

</details>

</div>

كنا ننصح سابقا بتفعيل خيار _Isolate Destination Address_ في إعدادات Orbot. رغم أن هذا الإعداد قد يحسّن الخصوصية نظريًا، لأنه يفرض استخدام مسار اتصال مختلف لكل عنوان IP تتصل به، فإنه لا يقدم فائدة حقيقية لمعظم التطبيقات (خاصةً عند تصفح الويب)، وقد يؤدي إلى بطء ملحوظ في الأداء وزيادة الضغط على شبكة Tor. لم نعد ننصح بتغيير القيمة الافتراضية لهذا الإعداد، إلا إذا كنت متأكدا من حاجتك إلى ذلك.[^1]

\=== "أندرويد"

```
يمكن لـ Orbot توجيه اتصال كل تطبيق على حدة عبر شبكة Tor، إذا كان التطبيق يدعم بروكسي SOCKS أو HTTP. ويمكنه أيضا توجيه جميع اتصالات الإنترنت عبر Tor باستخدام [VpnService](https://developer.android.com/reference/android/net/VpnService)، مع إمكانية تفعيل ميزة منع الاتصال بالإنترنت عند توقف VPN من خلال :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

غالبا ما تتأخر تحديثات Orbot على Google Play ومستودع F-Droid التابع لمشروع Guardian Project، لذلك ننصحك بتنزيله مباشرة من مستودع GitHub بدلا منهما. جميع الإصدارات موقعة بالتوقيع الرقمي نفسه، لذا يُفترض أن تكون متوافقة مع بعضها.
```

\=== "iOS"

```
على iOS، يواجه Orbot بعض القيود التي قد تؤدي إلى تعطل التطبيق أو تسرب بعض البيانات. فنظام iOS لا يوفر ميزة فعالة على مستوى النظام لمنع الاتصال بالإنترنت دون VPN، مثل الموجودة في Android. كما يفرض iOS حدا مصطنعا على الذاكرة التي يمكن أن تستخدمها إضافات الشبكة، مما يجعل تشغيل Tor عبر Orbot دون تعطل أمرا صعبا. حاليا، يُعد استخدام Tor على الكمبيوتر أكثر أمانًا من استخدامه على الهاتف.
```

#### Snowflake

<div class="admonition recommendation" markdown>

![Snowflake logo](assets/img/self-contained-networks/snowflake.svg#only-light){ align=right }
![Snowflake logo](assets/img/self-contained-networks/snowflake-dark.svg#only-dark){ align=right }

يتيح لك **Snowflake** المساهمة بجزء من سرعة اتصالك بالإنترنت لدعم مشروع Tor، من خلال تشغيل بروكسي "Snowflake" داخل متصفحك.

يمكن للأشخاص الذين يخضعون للرقابة على الإنترنت استخدام بروكسي Snowflake للاتصال بشبكة Tor. يُعد Snowflake طريقة رائعة للمساهمة في دعم شبكة Tor، حتى لو لم تكن لديك الخبرة التقنية اللازمة لتشغيل Tor relay أو bridge.

[:octicons-home-16: Homepage](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

</details>

</div>

يمكنك تفعيل Snowflake في متصفحك بفتحه في تبويب آخر وتشغيله باستخدام زر التفعيل. يمكنك ترك Snowflake يعمل في الخلفية أثناء تصفح الإنترنت، لتساهم بجزء من اتصالك في دعم الشبكة. لا ننصح بتثبيت Snowflake كإضافة للمتصفح، لأن إضافة ملحقات من جهات خارجية قد تزيد من فرص تعرض متصفحك للهجمات الأمنية.

[شغل Snowflake في متصفحك :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html){ .md-button }

لا يزيد Snowflake من خصوصيتك بأي شكل، ولا يُستخدم للاتصال بشبكة Tor من خلال متصفحك الشخصي. لكن إذا كان اتصالك بالإنترنت لا يخضع للرقابة، فننصحك بتشغيل Snowflake لمساعدة الأشخاص الذين يعانون من الرقابة على الإنترنت في حماية خصوصيتهم بشكل أفضل. لا داعي للقلق بشأن المواقع التي يزورها الآخرون عبر البروكسي الخاص بك، فعنوان الـIP الذي تراه هذه المواقع سيكون عنوان عقدة الخروج (exit node) من شبكة Tor، وليس عنوانك.

تشغيل بروكسي Snowflake ينطوي على مخاطر قليلة، بل إن مخاطره أقل من تشغيل Tor relay أو bridge، اللذين لا ينطوي تشغيلهما على مخاطر كبيرة أصلا. ومع ذلك، يظل Snowflake يمرر حركة بيانات الآخرين عبر اتصالك بالإنترنت، مما قد يؤثر على استخدامك له، خاصة إذا كانت باقتك محدودة. تأكد من فهمك [لطريقة عمل Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) قبل أن تقرر تشغيل بروكسي.

### I2P (مشروع الإنترنت الخفي)

<div class="admonition recommendation" markdown>

![I2P logo](assets/img/self-contained-networks/i2p.svg#only-light){ align=right }
![I2P logo](assets/img/self-contained-networks/i2p-dark.svg#only-dark){ align=right }

طبقة **I2P** هي طبقة شبكية تشفر اتصالاتك وتوجهها عبر شبكة من أجهزة الكمبيوتر المنتشرة حول العالم. تركز I2P بشكل أساسي على إنشاء شبكة بديلة تحمي الخصوصية، بدلا من إخفاء هويتك عند استخدام الإنترنت العادي.

[:octicons-home-16: Homepage](https://geti2p.net/en){ .md-button .md-button--primary }
[:octicons-info-16:](https://geti2p.net/en/about/software){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/i2p/i2p.i2p){ .card-link title="Source Code" }
[:octicons-heart-16:](https://geti2p.net/en/get-involved){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.i2p.android)
- [:simple-android: اندرويد](https://geti2p.net/en/download#android)
- [:fontawesome-brands-windows: وندوز](https://geti2p.net/en/download#windows)
- [:simple-apple: macOS](https://geti2p.net/en/download#mac)
- [:simple-linux: لينكس](https://geti2p.net/en/download#unix)

</details>

</div>

تركز I2P بشكل أساسي على إنشاء شبكة بديلة تحمي الخصوصية، بدلا من إخفاء هوية المستخدم عند الاتصال بالإنترنت العادي. بدلًا من ذلك، يمكنك زيارة مواقع مستضافة بشكل مجهول داخل شبكة I2P نفسها. تُسمى هذه المواقع "eepsites"، وتنتهي عناوينها بالنطاق .`i2p`.

<div class="admonition example" markdown>
<p class="admonition-title">جربه الآن!</p>

يمكنك تجربة الوصول إلى موقع _Privacy Guides_ عبر شبكة I2P من خلال [privacyguides.i2p](http://privacyguides.i2p/?i2paddresshelper=fvbkmooriuqgssrjvbxu7nrwms5zyhf34r3uuppoakwwsm7ysv6q.b32.i2p).

</div>

وعلى عكس Tor، كل جهاز متصل بشبكة I2P يساعد تلقائيا في نقل بيانات المستخدمين الآخرين، بدلا من الاعتماد على متطوعين لتشغيل خوادم مخصصة لذلك. تضم شبكة Tor حوالي [10,000](https://metrics.torproject.org/networksize.html) خادم replays و bridges، مقارنة بنحو 50,000 في شبكة I2P. وهذا يعني أن بياناتك قد تسلك مسارات أكثر داخل الشبكة، مما قد يساعد على إخفاء هويتك بشكل أفضل. غالبًا ما تكون شبكة I2P أسرع من Tor، ويرجع ذلك على الأرجح إلى أن Tor تركز أكثر على الاتصال بمواقع الإنترنت العادية (clearnet)، مما يجعل حركة البيانات تمر عبر عدد محدود من عقد الخروج، وقد يؤدي ذلك إلى بطء الاتصال. يُعتبر أداء الخدمات المخفية على شبكة I2P أفضل بكثير بشكل عام مقارنةً بشبكة Tor. بينما يصعب تشغيل تطبيقات مشاركة الملفات مثل BitTorrent عبر شبكة Tor (وقد يؤدي ذلك إلى إبطاء الشبكة بشكل كبير)، فإن تشغيلها عبر I2P أسهل بكثير ويقدم أداء أفضل.

لكن طريقة عمل I2P لها بعض العيوب أيضا. اعتماد Tor على عقد خروج (exit node) مخصصة يعني أن عددا أكبر من الأشخاص يمكنهم استخدامها، حتى في الأماكن التي تكون فيها مخاطر استخدام الشبكة أعلى. كما أن الخوادم التي تنقل البيانات داخل شبكة Tor غالبا ما تكون أسرع وأكثر استقرارا، لأنها عادة لا تعمل عبر اتصالات الإنترنت المنزلية. تركز Tor أيضا بشكل أكبر على حماية الخصوصية أثناء التصفح، مثل منع تتبع المستخدم عبر بصمة المتصفح (Browser Fingerprinting)، وتوفر متصفحا مخصصا [Tor Browser](tor.md) لجعل تصفح الإنترنت مجهول الهوية قدر الإمكان. تُستخدم شبكة I2P من خلال [متصفحك العادي](desktop-browsers.md)، ورغم أنه يمكنك تعديل إعدادات المتصفح لحماية خصوصيتك بشكل أفضل، فمن المرجح أن تظل بصمة متصفحك (Browser Fingerprinting) مختلفة عن بصمات متصفحات مستخدمي I2P الآخرين، مما يجعل تمييزك عنهم أسهل.

من المرجح أن تكون شبكة Tor أكثر قدرة على تجاوز الرقابة والحجب، بفضل شبكة الـ bridges التي توفرها، وتنوع [وسائل نقل الاتصال القابلة للتبديل (pluggable transports)](https://tb-manual.torproject.org/circumvention). في المقابل، تستخدم I2P خوادم مختلفة يديرها متطوعون للاتصال بالشبكة لأول مرة، ولا تُعتبر هذه الخوادم موثوقة بالضرورة. أما Tor فتعتمد على خوادم موثوقة ومحددة مسبقا في البرنامج، مما قد يجعل حجبها أسهل.

[^1]: نوقش إعداد `IsolateDestAddr` في [القائمة البريدية لمشروع Tor](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403) و[توثيق Stream Isolation الخاص بمشروع Whonix](https://whonix.org/wiki/Stream_Isolation)، ويرى المشروعان أن استخدامه ليس خيارا مناسبًا لمعظم الناس في العادة.
