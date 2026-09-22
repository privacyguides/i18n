---
title: "نظرة عامة على Tor"
icon: 'simple/torproject'
description: Tor هي شبكة مجانية ولا مركزية، صُممت لاستخدام الإنترنت بأكبر قدر ممكن من الخصوصية.
---

![شعار تور](../assets/img/self-contained-networks/tor.svg){ align=right }

[**شبكة Tor**](../alternative-networks.md#tor) هي شبكة مجانية ولا مركزية، صُمِّمت لاستخدام الإنترنت بأكبر قدر ممكن من الخصوصية. عند استخدام الشبكة بشكل صحيح، تتيح لك تصفح الإنترنت والتواصل بخصوصية ومن دون الكشف عن هويتك. فكون اتصالات تور صعبة الحظر والتتبع يجعل تور أداةً فعَّالةً لتجاوز الرقابة.

[:material-movie-open-play-outline: فيديو: لماذا تحتاج إلى Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

تعمل Tor من خلال تمرير حركة الإنترنت الخاصة بك عبر خوادم يديرها متطوعون، بدلا من الاتصال مباشرة بالموقع الذي تريد زيارته. يلبِّس هذا أصل الاتصال، وليس بوسع أي خادم في سبيل الاتصال رؤيته من بدايته لمقصده، مما يعني أن حتى الخوادم المستخدمة للاتصال لا تنتهك مجهوليتك.

[:octicons-home-16:](https://torproject.org){ .card-link title=الصفحة الرئيسية }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="خدمة Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=التوثيق }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="الكود المصدري" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=المساهمة }

## الاتصال بشبكة Tor بأمان

قبل الاتصال بشبكة Tor، فكر جيدا في الهدف الذي تريد تحقيقه من استخدامها، وفي الجهة التي تريد إخفاء نشاطك على الشبكة عنها.

إذا كنت تعيش في بلد يتمتع بحرية الإنترنت، وتستخدم Tor للوصول إلى محتوى عادي، ولا تمانع أن يعرف مزوّد خدمة الإنترنت أو مسؤولو الشبكة المحلية أنك تستخدم Tor، كما ترغب في المساعدة على [إزالة الوصمة المرتبطة باستخدام Tor](https://2019.www.torproject.org/about/torusers.html.en)، فيمكنك غالبًا الاتصال بشبكة Tor مباشرةً بالطرق المعتادة، مثل استخدام [متصفح Tor](../tor.md)، دون قلق.

إذا كان بإمكانك استخدام خدمة VPN موثوقة، وكان **أي** مما يلي ينطبق عليك، فمن الأفضل على الأرجح الاتصال بشبكة Tor عبر VPN:

- أنت تستخدم بالفعل [خدمة VPN موثوقة](../vpn.md)
- يتضمّن نموذج التهديدات (Threat Model) الخاص بك جهة قد تتمكّن من الحصول على معلومات عن نشاطك من مزوّد خدمة الإنترنت (ISP).
- يتضمّن نموذج التهديدات (Threat Model) الخاص بك مزوّد خدمة الإنترنت (ISP) نفسه كجهة قد تتجسّس على نشاطك أو تحاول تتبّعه
- يتضمّن نموذج التهديدات (Threat Model) الخاص بك مسؤولي الشبكة المحلية، الذين تمرّ اتصالاتك عبر شبكتهم قبل الوصول إلى مزوّد خدمة الإنترنت (ISP)، كجهة قد تحاول مراقبة نشاطك أو تتبّعه

وبما أننا [نوصي عموما](../basics/vpn-overview.md) بأن يستخدم معظم الناس خدمة VPN موثوقة لأسباب متعددة، فمن المرجّح أن تنطبق عليك أيضًا التوصية التالية بالاتصال بشبكة Tor عبر VPN. <mark>لا تحتاج إلى إيقاف تشغيل الـ VPN قبل الاتصال بشبكة Tor</mark>، رغم أن بعض المصادر على الإنترنت قد توحي لك بعكس ذلك.

الاتصال مباشرةً بشبكة Tor سيجعل استخدامك لها واضحًا لمسؤولي الشبكة المحلية أو لمزوّد خدمة الإنترنت (ISP). سبق أن استخدم مسؤولو بعض الشبكات [رصد هذا النوع من حركة الإنترنت وربطه بنشاط المستخدمين](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax) للتعرّف على مستخدمين محددين لشبكة Tor وكشف هوياتهم. في المقابل، يكون الاتصال بخدمة VPN أقل إثارة للشك في معظم الحالات، لأن خدمات الـ VPN التجارية يستخدمها الناس بشكل عادي لأغراض كثيرة، مثل تجاوز القيود الجغرافية على المحتوى، حتى في البلدان التي تفرض قيودًا شديدة على الإنترنت.

لذلك، من الأفضل أن تحاول إخفاء عنوان IP الخاص بك **قبل** الاتصال بشبكة Tor. يمكنك فعل ذلك ببساطة عن طريق الاتصال بخدمة VPN أولًا، باستخدام تطبيق مثبت على جهازك، ثم استخدام [Tor](../tor.md) كالمعتاد، مثلًا من خلال متصفح Tor. وبذلك يصبح مسار اتصالك كالتالي:

- [x] أنت ← VPN ← Tor ← الإنترنت

من وجهة نظر مزوّد خدمة الإنترنت (ISP)، سيبدو الأمر وكأنك تستخدم VPN بشكل عادي، وهذا يساعد على إخفاء حقيقة أنك تستخدم Tor. من وجهة نظر مزوّد خدمة الـ VPN، يمكنه معرفة أنك تتصل بشبكة Tor، لكنه لا يستطيع معرفة المواقع التي تزورها من خلالها. ومن وجهة نظر شبكة Tor، فأنت تتصل بها بشكل طبيعي. وحتى في الحالة غير المحتملة التي تتعرّض فيها شبكة Tor للاختراق، فلن ينكشف سوى عنوان IP الخاص بالـ VPN، وسيكون من الضروري *أيضًا* اختراق خدمة الـ VPN نفسها حتى يمكن كشف هويتك.

هذه **ليست** نصيحة لتجاوز الحجب، لأنه إذا كان مزوّد خدمة الإنترنت (ISP) يحجب Tor بالكامل، فمن المحتمل أن يحجب الـ VPN أيضًا. بل تهدف هذه التوصية إلى جعل حركة الإنترنت الخاصة بك تبدو أكثر شبهًا بحركة مستخدمي الـ VPN العاديين، ومنحك قدرًا من إمكانية الإنكار المعقول، وذلك بإخفاء حقيقة اتصالك بشبكة Tor عن مزوّد خدمة الإنترنت (ISP).

---

نحن **نحذر بشدة** من الجمع بين Tor وVPN بأي طريقة أخرى. لا تضبط اتصالك بطريقة تشبه أيًا من الأشكال التالية:

- أنت ← VPN ← Tor ← الإنترنت
- أنت ← VPN ← Tor ← VPN ← الإنترنت
- أي إعداد آخر

توصي بعض خدمات الـ VPN وبعض المصادر أحيانًا بهذه الإعدادات **السيئة** لتجاوز حظر Tor في بعض الأماكن، مثل حظر المواقع لعُقد الخروج (Exit Nodes). [عادة](https://support.torproject.org/#about_change-paths)، يغيّر Tor بشكل متكرر مسار اتصالك عبر الشبكة. عندما تستخدم VPN كـ *وجهة ثابتة* بعد Tor، أي تتصل بخادم VPN *بعد* المرور عبر شبكة Tor، فأنت تلغي هذه الميزة وتُضعف إخفاء هويتك بشكل كبير.

من الصعب أن تصل إلى مثل هذه الإعدادات الخاطئة عن طريق الخطأ، لأنها تتطلب عادةً ضبط إعدادات Proxy مخصّصة داخل متصفح Tor، أو داخل تطبيق الـ VPN بحيث يتم تمرير اتصال الـ VPN عبر متصفح Tor. من غير المحتمل أن تستخدم هذه الإعدادات الخاطئة عن طريق الخطأ، لأنها تتطلب عادةً إعداد Proxy مخصّص داخل متصفح Tor، أو إعداد Proxy داخل تطبيق الـ VPN لتمرير اتصال الـ VPN عبر متصفح Tor.

---

<div class="admonition info" markdown>
<p class="admonition-title">بصمات VPN/SSH</p>

يشير مشروع Tor إلى أنه من الناحية النظرية، قد لا يكون استخدام VPN لإخفاء نشاطك على Tor عن مزوّد خدمة الإنترنت (ISP) حلًا مضمونًا بالكامل. قد يتمكن من يراقب اتصال الـ VPN من تخمين الموقع الذي تزوره من شكل حركة البيانات، لأن لكل موقع نمطًا مميزًا في طريقة إرسال واستقبال البيانات.

لذلك، من الممكن أن يتم التعرف أيضا على حركة Tor المشفرة والمخفية داخل اتصال VPN باستخدام طرق مشابهة. لا توجد أبحاث منشورة حول هذا الأمر حتى الآن، وما زلنا نرى أن فوائد استخدام VPN أكبر بكثير من هذه المخاطر، لكن من الجيد أن تضع هذا الاحتمال في الحسبان.

إذا كنت لا تزال ترى أن وسائل النقل القابلة للتمويه (Pluggable Transports) أو الجسور (Bridges) توفّر حماية إضافية من تحليل بصمة حركة المواقع لا يوفّرها الـ VPN، فيمكنك استخدام Bridge وVPN معًا.

</div>

تحديد ما إذا كان من الأفضل أن تتصل أولا بخدمة VPN قبل استخدام Tor يعتمد على تقديرك للموقف، ومعرفتك بسياسات حكومتك ومزوّد خدمة الإنترنت (ISP) تجاه نوع الاتصالات التي تستخدمها. ومع ذلك، نؤكد مرة أخرى أنه في معظم الحالات، من الأفضل أن يبدو اتصالك وكأنك تستخدم شبكة VPN تجارية بدلًا من الاتصال مباشرةً بشبكة Tor. إذا كانت خدمات الـ VPN محجوبة في منطقتك، فيمكنك استخدام وسائل النقل القابلة للتمويه (Pluggable Transports) في Tor، مثل الجسور (Bridges) من نوع Snowflake أو meek، كبديل. لكن استخدام هذه الجسور قد يلفت الانتباه أكثر من اتصالات WireGuard أو OpenVPN العادية.

## ما ليس عليه Tor

شبكة Tor ليست أداة مثالية لحماية الخصوصية في جميع الحالات، ولديها عدد من العيوب التي ينبغي أخذها بعين الاعتبار بعناية. لا ينبغي أن تمنعك هذه الأمور من استخدام Tor إذا كان مناسبا لاحتياجاتك، لكنها تظل نقاطا مهمة يجب التفكير فيها عند تحديد الحل الأنسب لك.

### شبكة Tor ليس شبكة VPN مجانية

أدى إصدار تطبيق *Orbot* للهواتف المحمولة إلى وصف كثير من الناس لشبكة Tor بأنها «VPN مجاني» لكل حركة المرور على جهازك. لكن استخدام Tor بهذه الطريقة ينطوي على بعض المخاطر مقارنةً بخدمة الـ VPN التقليدية.

على عكس عُقد الخروج (Exit Nodes) في Tor، فإن مزودي خدمات الـ VPN لا يكونون *عادةً* جهات [خبيثة](#caveats) تتعمد الإضرار بالمستخدمين. لأن أي شخص يمكنه إنشاء عُقد خروج (Exit Nodes) في Tor، فقد تُستخدم هذه العُقد لمراقبة حركة الإنترنت أو التلاعب بها. في عام 2020، تم توثيق العديد من عُقد الخروج (Exit Nodes) في Tor وهي تُحوِّل اتصالات HTTPS إلى HTTP بهدف [اختطاف معاملات العملات الرقمية](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). كما تم رصد هجمات أخرى عبر عُقد الخروج (Exit Nodes)، مثل استبدال الملفات التي يتم تنزيلها عبر اتصالات غير مشفّرة ببرامج ضارة. يساعد HTTPS في تقليل هذه المخاطر إلى حدٍّ ما.

وكما ذكرنا سابقًا، يمكن أيضًا التعرّف بسهولة على استخدام Tor من خلال الشبكة. على عكس استخدام خدمة VPN عادية، فإن استخدام Tor قد يجعلك أكثر لفتًا للانتباه على الشبكة، وقد يُنظر إليك على أنك تحاول تجنّب مراقبة السلطات. في عالم مثالي، كان من المفترض أن ينظر مسؤولو الشبكات والسلطات إلى Tor على أنه أداة لها استخدامات عديدة، مثلما يُنظر إلى خدمات VPN. لكن في الواقع، لا يزال Tor يُنظر إليه على أنه أقل شرعية وموثوقية بكثير من خدمات VPN التجارية. لذلك، يمنحك استخدام VPN عادي إمكانية تقديم تفسير مقبول لاستخدامك له، مثل: «كنت أستخدمه فقط لمشاهدة Netflix»، وما إلى ذلك.

### استخدام Tor ليس مخفيًا تمامًا عن الاكتشاف

**حتى إذا كنت تستخدم الجسور (Bridges) ووسائل النقل القابلة للتوصيل (Pluggable Transports)،** فإن مشروع Tor لا يوفّر أدوات تخفي عن مزود خدمة الإنترنت (ISP) حقيقة أنك تستخدم Tor. حتى استخدام وسائل النقل المُموّهة (Pluggable Transports) أو الجسور غير العامة (non-public bridges) لا يُخفي حقيقة أنك تستخدم قناة اتصال خاصة (private communications channel). يمكن [اكتشاف](https://hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) أشهر وسائل النقل القابلة للتوصيل (Pluggable Transports)، مثل obfs4 الذي يُموّه حركة الإنترنت لتبدو وكأنها بلا نمط واضح، وmeek الذي يستخدم تقنية Domain Fronting لإخفاء حركة الإنترنت، وذلك باستخدام أساليب تحليل حركة الشبكة الشائعة نسبيًا. ويواجه Snowflake مشكلات مشابهة، إذ يمكن [اكتشافه بسهولة](https://hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) حتى *قبل* إنشاء اتصال Tor من الأساس.

توجد وسائل نقل قابلة للتوصيل (Pluggable Transports) أخرى غير هذه الثلاثة، لكنها تعتمد غالبًا على صعوبة معرفة كيفية عملها لتجنّب اكتشافها. هذا لا يعني أنه من المستحيل اكتشافها، بل إن عدد مستخدميها قليل جدًا لدرجة أن تطوير أدوات مخصصة لاكتشافها لا يستحق الجهد عادةً. لا ينبغي الاعتماد عليها إذا كنت أنت تحديدا تحت المراقبة.

من المهم جدا فهم الفرق بين تجاوز الرقابة وتجنّب اكتشاف استخدامك لـ Tor. تجاوز الرقابة أسهل، لأن الجهات التي تراقب الشبكات لا تستطيع عمليًا منع كل شيء على نطاق واسع. لكن هذه الطرق لا تُخفي عن جهة تراقب شبكتك أنك أنت *بالتحديد* تستخدم Tor.

### متصفح Tor ليس المتصفح الأكثر *أمانًا*

قد تتعارض إخفاء الهوية أحيانا مع الأمان. يحقق Tor إخفاء الهوية بجعل جميع المستخدمين يبدون متشابهين، مما يخلق بيئة رقمية موحّدة تتشارك فيها جميع النسخ نفس نقاط الضعف. في الأمن السيبراني، تُعدّ البيئات الموحّدة عمومًا مصدرًا للمخاطر. الأمان من خلال التنوع يوفر عزلا طبيعيا، لأنه يحد من تأثير أي ثغرة بحيث يقتصر على شريحة أصغر من المستخدمين. ورغم أن هذا التنوع مفيد للأمان من ناحية البنية، فإنه يضعف إخفاء هوية المستخدمين بطبيعته، لأنه يجعل تتبّع كل مستخدم أسهل.

بالإضافة إلى ذلك، يعتمد متصفح Tor على إصدارات Firefox Extended Support Release، والتي لا تتلقى تحديثات أمنية إلا للثغرات المصنفة على أنها *Critical* و*High*، وليس *Medium* و*Low*. هذا يعني أن المهاجمين يمكنهم، على سبيل المثال:

1. البحث عن ثغرات Critical أو High جديدة في إصدارات Firefox Nightly أو Beta، ثم التحقق مما إذا كان يمكن استغلالها في Tor Browser. وقد تستمر هذه الفترة التي تكون فيها الثغرة قابلة للاستغلال لعدة أسابيع.
2. دمج *عدة* ثغرات من نوع Medium أو Low معًا، حتى يحصل المهاجم على مستوى الوصول الذي يريده. وقد تستمر فترة قابلية الاستغلال هذه لعدة أشهر أو أكثر.

ينبغي لمن قد يكونون عرضة لثغرات المتصفح التفكير في وسائل حماية إضافية ضد استغلال ثغرات Tor Browser، مثل استخدام Whonix داخل [Qubes](../os/qubes-overview.md) لعزل تصفح Tor داخل آلة افتراضية آمنة والحماية من تسريب البيانات.

## بناء مسار Tor للوصول إلى مواقع الإنترنت العادية

مصطلح "Clearnet services" يقصد به المواقع التي يمكنك الوصول إليها باستخدام أي متصفح، مثل [privacyguides.org](https://www.privacyguides.org). يتيح لك Tor الاتصال بهذه المواقع دون كشف هويتك، وذلك عبر تمرير اتصالك من خلال شبكة تضم آلاف الخوادم التي يديرها متطوعون، وتُسمى nodes أو relays.

في كل مرة [تتصل فيها بشبكة Tor](../tor.md)، يختار Tor ثلاث nodes لبناء مسار إلى الإنترنت، ويُسمّى هذا المسار "circuit".

<figure markdown>
  ![مسار Tor يوضّح اتصال جهازك بـ entry node ثم middle node ثم exit node قبل الوصول إلى الموقع المطلوب](../assets/img/how-tor-works/tor-path.svg#only-light)
![مسار Tor يوضّح اتصال جهازك بـ entry node ثم middle node ثم exit node قبل الوصول إلى الموقع المطلوب](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)

<figcaption>مسار Tor circuit</figcaption>
</figure>

كل node من هذه الـ nodes لها وظيفة خاصة بها:

### عقدة الدخول (Entry Node)

عقدة الدخول (Entry Node)، والتي تُسمّى غالبًا Guard Node، هي أول node يتصل بها Tor client لديك. يمكن لعقدة الدخول (Entry Node) رؤية عنوان IP الخاص بك، لكنها لا تستطيع معرفة الموقع أو الخدمة التي تتصل بها.

على عكس باقي الـ nodes، يختار Tor client عقدة دخول (Entry Node) بشكل عشوائي ويستمر في استخدامها لمدة تتراوح بين شهرين وثلاثة أشهر، وذلك لحمايتك من بعض أنواع الهجمات.[^1]

### العقدة الوسطى (Middle Node)

العقدة الوسطى (Middle Node) هي ثاني node يتصل بها Tor client لديك. يمكنها معرفة الـ node التي جاءت منها حركة البيانات، وهي عقدة الدخول (Entry Node)، وكذلك الـ node التي ستنتقل إليها بعد ذلك. لكن العقدة الوسطى (Middle Node) لا يمكنها رؤية عنوان IP الخاص بك أو اسم النطاق الذي تتصل به.

مع كل circuit جديد، يتم اختيار العقدة الوسطى (Middle Node) بشكل عشوائي من بين جميع Tor nodes المتاحة.

### عقدة الخروج (Exit Node)

عقدة الخروج (Exit Node) هي النقطة التي تغادر عندها حركة الإنترنت الخاصة بك شبكة Tor، ثم يتم توجيهها إلى الوجهة التي تريد الوصول إليها. لا تستطيع عقدة الخروج (Exit Node) رؤية عنوان IP الخاص بك، لكنها تعرف الموقع الذي تتصل به.

يتم اختيار عقدة الخروج (Exit Node) بشكل عشوائي من بين جميع Tor nodes المتاحة التي تعمل بعلامة exit relay.[^2]

## بناء المسار إلى خدمات Onion

"خدمات Onion" (ويشار إليها أيضا باسم "الخدمات المخفية") هي مواقع لا يمكن الوصول إليها إلا باستخدام Tor Browser. تستخدم هذه المواقع أسماء نطاق طويلة يتم إنشاؤها عشوائيًا، وتنتهي بـ `.onion`.

يعمل الاتصال بخدمة Onion عبر Tor بشكل مشابه جدًا للاتصال بخدمة Clearnet، لكن حركة البيانات الخاصة بك تمر عبر **ست** nodes إجمالًا قبل الوصول إلى الخادم المطلوب. لكن كما سبق، ثلاث فقط من هذه الـ nodes تساهم في إخفاء *هويتك* أنت، بينما تحمي الـ nodes الثلاث الأخرى *هوية خدمة Onion*، من خلال إخفاء عنوان IP الحقيقي للموقع وموقعه الجغرافي، بالطريقة نفسها التي يخفي بها Tor Browser عنوانك وموقعك.

<figure style="width:100%" markdown>
  ![مسار Tor يوضح مرور حركة البيانات الخاصة بك عبر ثلاث Tor nodes، بالإضافة إلى ثلاث Tor nodes أخرى تُخفي هوية الموقع](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
![مسار Tor يوضّح مرور حركة البيانات الخاصة بك عبر ثلاث Tor nodes، بالإضافة إلى ثلاث Tor nodes أخرى تُخفي هوية الموقع](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)

<figcaption>مسار Tor circuit عند استخدام خدمات Onion. الـ nodes الموجودة داخل الإطار <span class="pg-blue">الأزرق</span> تتبع متصفحك، بينما الـ nodes الموجودة داخل الإطار <span class="pg-red">الأحمر</span> تتبع الخادم، ولذلك تظل هويته مخفية عنك.</figcaption>
</figure>

## التشفير (Encryption)

يقوم Tor بتشفير كل packet (وهي كتلة من البيانات التي يتم إرسالها) ثلاث مرات، باستخدام مفاتيح عقدة الخروج (Exit Node)، ثم العقدة الوسطى (Middle Node)، ثم عقدة الدخول (Entry Node)، بهذا الترتيب.

بعد أن ينشئ Tor الـ circuit، يتم نقل البيانات بالشكل التالي:

1. أولا: عندما تصل الـ packet إلى عقدة الدخول (Entry Node)، تتم إزالة طبقة التشفير الأولى. داخل الـ packet المشفّرة، تجد عقدة الدخول (Entry Node) packet أخرى ما زالت مشفّرة، ومعها عنوان العقدة الوسطى (Middle Node) التي يجب إرسالها إليها. بعد ذلك، ترسل عقدة الدخول (Entry Node) الـ packet إلى العقدة الوسطى (Middle Node).

2. ثانيا: عندما تستقبل العقدة الوسطى (Middle Node) الـ packet من عقدة الدخول (Entry Node)، تزيل هي أيضا طبقة من التشفير باستخدام مفتاحها. بعدها تجد بداخلها packet أخرى ما زالت مشفّرة، ومعها عنوان عقدة الخروج (Exit Node) التي يجب إرسالها إليها. بعد ذلك، ترسل العقدة الوسطى (Middle Node) الـ packet إلى عقدة الخروج (Exit Node).

3. أخيرًا: عندما تستقبل عقدة الخروج (Exit Node) الـ packet، تزيل آخر طبقة من التشفير باستخدام مفتاحها. بعد ذلك، ترى عقدة الخروج (Exit Node) عنوان الوجهة، ثم ترسل الـ packet إلى هذا العنوان.

فيما يلي رسم توضيحي آخر يشرح هذه العملية. تزيل كل node طبقة التشفير الخاصة بها، وعندما يرسل خادم الوجهة (destination server) البيانات مرة أخرى، تحدث العملية نفسها بالكامل ولكن بالترتيب العكسي. على سبيل المثال، لا تعرف عقدة الخروج (Exit Node) من أنت، لكنها تعرف الـ node التي جاءت منها البيانات، لذلك تضيف طبقة التشفير الخاصة بها ثم ترسل البيانات إليها مرة أخرى.

<figure markdown>
  ![تشفير Tor](../assets/img/how-tor-works/tor-encryption.svg#only-light)
![تشفير Tor](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)

<figcaption>إرسال واستقبال البيانات عبر شبكة Tor</figcaption>
</figure>

يتيح لنا Tor الاتصال بخادم دون أن يعرف أي طرف بمفرده المسار الكامل للاتصال. تعرف عقدة الدخول (Entry Node) من أنت، لكنها لا تعرف إلى أين تتجه. أما العقدة الوسطى (Middle Node) فلا تعرف من أنت ولا إلى أين تتجه. بينما تعرف عقدة الخروج (Exit Node) إلى أين تتجه، لكنها لا تعرف من أنت. ولأن عقدة الخروج (Exit Node) هي التي تنشئ الاتصال النهائي، فلن يعرف خادم الوجهة (destination server) عنوان IP الخاص بك.

## ملاحظات مهمة

على الرغم من أن Tor يوفر ضمانات قوية للخصوصية، فمن المهم أن نكون على دراية بأن Tor ليس مثاليا:

- متصفح Tor لا يحميك من كشف هويتك بالخطأ، مثل أن تشارك معلومات كثيرة جدا عن هويتك الحقيقية.
- يمكن لـ Tor exit nodes أن **تُعدّل** الـ traffic غير المشفّر الذي يمر من خلالها. This means traffic which is not encrypted, such as plain HTTP traffic, can be changed by a malicious exit node. **Never** download files from an unencrypted `http://` website over Tor, and ensure your browser is set to always upgrade HTTP traffic to HTTPS.
- Tor exit nodes can also monitor traffic that passes through them. Unencrypted traffic which contains personally identifiable information can deanonymize you to that exit node. Again, we recommend only using HTTPS over Tor.
- Powerful adversaries with the capability to passively watch *all* network traffic around the globe ("Global Passive Adversaries") are **not** something that Tor protects you against (and using Tor [with a VPN](#safely-connecting-to-tor) doesn't change this fact).
- Well-funded adversaries with the capability to passively watch *most* network traffic around the globe still have a *chance* of deanonymizing Tor users by means of advanced traffic analysis.

If you wish to use Tor for browsing the web, we only recommend the **official** Tor Browser—it is designed to prevent fingerprinting.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Protections provided by bridges

Tor bridges are commonly touted as an alternative method to hiding Tor usage from an ISP, instead of a VPN (as we suggest using if possible). Something to consider is that while bridges may provide adequate censorship circumvention, this is only a *transient* benefit. They do not adequately protect you from your ISP discovering you connected to Tor in the *past* with historical traffic log analysis.

To illustrate this point, consider the following scenario: You connect to Tor via a bridge, and your ISP doesn’t detect it because they are not doing sophisticated analysis of your traffic, so things are working as intended. Now, 4 months go by, and the IP of your bridge has been made public. This is a very common occurrence with bridges; they are discovered and blocked relatively frequently, just not immediately.

Your ISP wants to identify Tor users 4 months ago, and with their limited metadata logging they can see that you connected to an IP address which was later revealed to be a Tor bridge. You have virtually no other excuse to be making such a connection, so the ISP can say with very high confidence that you were a Tor user at that time.

Contrast this with our recommended scenario, where you connect to Tor via a VPN. Say that 4 months later your ISP again wants to identify anybody who used Tor 4 months ago. Their logs almost certainly can identify your traffic 4 months ago, but all they would likely be able to see is that you connected to a VPN’s IP address. This is because most ISPs only retain metadata over long periods of time, not the full contents of the traffic you request. Storing the entirety of your traffic data would require a massive quantity of storage which nearly all threat actors wouldn't possess.

Because your ISP almost certainly is not capturing all packet-level data and storing it forever, they have no way of determining what you connected to with that VPN *after* the fact with an advanced technique like deep packet inspection, and therefore you have plausible deniability.

Therefore, bridges provide the most benefit when circumventing internet censorship *in the moment*, but they are not an adequate substitute for **all** the benefits that using a VPN alongside Tor can provide. Again, this is not advice *against* using Tor bridges—you should just be aware of these limitations while making your decision. In some cases bridges may be the *only* option (if all VPN providers are blocked, for instance), so you can still use them in those circumstances with this limitation in mind.

If you think that a bridge can aid in defending against fingerprinting or other advanced network analysis more than a VPN's encrypted tunnel already can, you always have the option to use a bridge in conjunction with a VPN as well. That way you are still protected by the pluggable transport's obfuscation techniques even if an adversary gains some level of visibility into your VPN tunnel. If you decide to go this route, we recommend connecting to an obfs4 bridge behind your VPN for optimal fingerprinting protection, rather than meek or Snowflake.

It is [possible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) that the [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) pluggable transport currently being trialed may mitigate some of these concerns. We will continue to keep an eye on that technology as it develops.

## Additional Resources

- [Tor Browser User Manual](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://youtube.com/watch?v=QRYzre4bf7I) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://youtube.com/watch?v=lVcbq_a5N9I) <small>(YouTube)</small>

[^1]: The first relay in your circuit is called an "entry guard" or "guard". It is a fast and stable relay that remains the first one in your circuit for 2-3 months in order to protect against a known anonymity-breaking attack. The rest of your circuit changes with every new website you visit, and all together these relays provide the full privacy protections of Tor. For more information on how guard relays work, see this [blog post](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) and [paper](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) on entry guards. ([https://support.torproject.org/tbb/tbb-2](https://support.torproject.org/tbb/tbb-2))

[^2]: Relay flag: a special (dis-)qualification of relays for circuit positions (for example, "Guard", "Exit", "BadExit"), circuit properties (for example, "Fast", "Stable"), or roles (for example, "Authority", "HSDir"), as assigned by the directory authorities and further defined in the directory protocol specification. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html#relay-flag))
