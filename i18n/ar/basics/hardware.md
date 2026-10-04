---
title: "اختيار أجهزتك"
icon: 'material/chip'
description: البرامج ليست كل شيء؛ تعرّف على الأجهزة التي تستخدمها يوميًا وكيف تساعدك على حماية خصوصيتك.
---

عند الحديث عن الخصوصية، غالبًا ما لا نهتم بالأجهزة بقدر اهتمامنا بالبرامج التي نستخدمها. يجب اعتبار أجهزتك الأساس الذي تبني عليه بقية إعدادات الخصوصية لديك.

## اختيار جهاز كمبيوتر

تعالج المكوّنات الداخلية لأجهزتك جميع بياناتك الرقمية وتخزنها. من المهم أن تظل جميع الأجهزة مدعومة من الشركة المصنعة والمطورين، وأن تستمر في تلقي تحديثات الأمان.

### برامج الحماية على مستوى الأجهزة

تحتوي بعض الأجهزة على «برنامج لأمان الأجهزة»، وهو تعاون بين الشركات المصنعة لتطبيق أفضل الممارسات والتوصيات عند تصميم الأجهزة، على سبيل المثال:

- تستوفي أجهزة [Windows Secured-core PCs](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure-11) معايير أمان أعلى تحددها Microsoft. لا تقتصر وسائل الحماية هذه على مستخدمي Windows فقط؛ إذ يمكن لمستخدمي أنظمة التشغيل الأخرى أيضا الاستفادة من ميزات مثل [DMA protection](https://learn.microsoft.com/en-us/windows/security/information-protection/kernel-dma-protection-for-thunderbolt) وإمكانية عدم الوثوق إطلاقا بشهادات Microsoft.
- يُعد [Android Ready SE](https://developers.google.com/android/security/android-ready-se) تعاونا بين الشركات المصنّعة لضمان أن أجهزتها تتبع [أفضل الممارسات](https://source.android.com/docs/security/best-practices/hardware)، ومزوّدة بوحدة تخزين عتادية آمنة ومحمية من التلاعب، لحفظ أشياء مثل مفاتيح التشفير.
- يستفيد macOS عند تشغيله على Apple SoC من [الأمان على مستوى الأجهزة](../os/macos-overview.md#hardware-security)، وقد لا تتوفر هذه الميزات عند استخدام أنظمة تشغيل من جهات خارجية.
- يكون أمان [ChromeOS security](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper) في أفضل حالاته عند تشغيله على جهاز Chromebook، لأنه يستطيع الاستفادة من ميزات الأجهزة المتاحة، مثل [hardware root-of-trust](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper/#hardware-root-of-trust-and-verified-boot).

حتى إذا كنت لا تستخدم أنظمة التشغيل هذه، فقد تشير مشاركة الشركة المصنّعة في هذه البرامج إلى أنها تتبع أفضل الممارسات فيما يتعلق بأمان الأجهزة وتحديثاتها.

### نظام التشغيل المثبت مسبقا

تأتي أجهزة الكمبيوتر الجديدة دائما تقريبا مع Windows مثبتا مسبقا، إلا إذا اشتريت جهاز Mac أو جهازا مخصصا يعمل بنظام Linux. يُفضل عادةً مسح القرص وتثبيت نسخة جديدة من نظام التشغيل الذي تختاره، حتى لو كان ذلك يعني فقط إعادة تثبيت Windows من البداية. بسبب الاتفاقيات بين الشركات المصنعة للأجهزة وشركات البرمجيات المشبوهة، غالبا ما تأتي نسخة Windows الافتراضية محملة مسبقًا ببرامج غير ضرورية، أو [برامج إعلانية](https://bleepingcomputer.com/news/technology/lenovo-gets-a-slap-on-the-wrist-for-superfish-adware-scandal)، أو حتى [برامج ضارة](https://zdnet.com/article/dell-poweredge-motherboards-ship-with-malware).

### تحديثات الـ Firmware

غالبا ما تحتوي الأجهزة على مشكلات أمنية يتم اكتشافها وإصلاحها من خلال تحديثات الـ Firmware الخاصة بها.

تحتاج كل مكونات جهاز الكمبيوتر تقريبا إلى Firmware لكي تعمل، بدءا من اللوحة الأم وحتى وحدات التخزين. من الأفضل أن تكون جميع مكونات جهازك مدعومة بالكامل. تتولى أجهزة Apple وChromebook ومعظم هواتف Android وأجهزة Microsoft Surface تحديثات Firmware تلقائيا ما دام الجهاز لا يزال مدعوما.

إذا قمت بتجميع جهاز الكمبيوتر بنفسك، فقد تحتاج إلى تحديث Firmware الخاص باللوحة الأم (motherboard) يدويا عن طريق تنزيله من موقع الشركة المصنعة (OEM). إذا كنت تستخدم Linux، ففكر في استخدام أداة fwupd المدمجة، والتي تتيح لك التحقق من تحديثات Firmware المتاحة للوحة الأم (motherboard) وتثبيتها.

### TPM/معالج التشفير الآمن

تأتي معظم أجهزة الكمبيوتر والهواتف مزودة بـ TPM (أو معالج تشفير آمن مشابه)، والذي يخزن مفاتيح التشفير بأمان ويتولى وظائف أخرى متعلقة بالأمان. إذا كنت تستخدم حاليا جهازًا لا يحتوي على إحدى هذه الميزات، فقد يكون من الأفضل شراء جهاز كمبيوتر أحدث يدعمها. تحتوي بعض اللوحات الأم (motherboard) لأجهزة الكمبيوتر المكتبية (desktops) والخوادم على "TPM header"، يمكن توصيل لوحة صغيرة به تحتوي على TPM.

<div class="admonition Note" markdown>
<p class="admonition-title">ملحوظة</p>

تكون وحدات الـ (virtual TPM) عرضة لهجمات side-channel، بينما تكون وحدات الـ TPM الخارجية، بسبب انفصالها عن الـ CPU على اللوحة الأم (motherboard)، عرضة لـ sniffing عندما يتمكن المهاجم من الوصول فعليا إلى الجهاز. الحل لهذه المشكلة هو دمج المعالج الآمن داخل الـ CPU نفسه، كما هو الحال في شرائح Apple ومعالج [Pluton](https://microsoft.com/en-us/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs) من Microsoft.

</div>

### الـ Biometrics أو القياسات الحيوية

تأتي العديد من الأجهزة مزودة بقارئ بصمات الأصابع (fingerprint) أو بميزة التعرف على الوجه. قد تكون هذه الميزات مريحة جدا، لكنها ليست مثالية وقد تفشل أحيانا. عند حدوث ذلك، ستعود معظم الأجهزة إلى استخدام الـ PIN أو كلمة المرور، ما يعني أن أمان جهازك يظل معتمدًا على قوة كلمة مرورك.

يمكن للـBiometrics أن تمنع شخصا من مراقبتك أثناء كتابة كلمة مرورك، لذلك إذا كان التلصص على ما تكتبه جزءا من Threat Model لديك، فالـ Biometrics خيار جيد.

تتطلب معظم تقنيات التعرف على الوجه (face authentication) أن تنظر إلى هاتفك مباشرة، كما أنها لا تعمل إلا من مسافة قريبة نسبيا، لذلك لا داعي للقلق كثيرا من أن يوجه شخص ما هاتفك نحو وجهك لفتحه دون موافقتك. لا يزال بإمكانك تعطيل الـ Biometrics عندما يكون هاتفك مقفلًا إذا أردت. على iOS، يمكنك الضغط مطولا على الزر الجانبي وأحد زري مستوى الصوت لمدة 3 ثوان لتعطيل Face ID على الأجهزة التي تدعمه. على Android، اضغط مطولا على زر التشغيل، ثم اضغط على Lockdown من القائمة.

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

بعض الأجهزة لا تحتوي على المكونات اللازمة للتعرف الآمن على الوجه. هناك نوعان رئيسيان من التعرف على الوجه: ثنائي الأبعاد (2D) وثلاثي الأبعاد (3D). يستخدم التعرف على الوجه ثلاثي الأبعاد (3D) جهازا لإسقاط النقاط، ما يسمح للجهاز بإنشاء خريطة عمق ثلاثية الأبعاد لوجهك. تأكد من أن جهازك يدعم هذه الميزة.

</div>

يحدّد Android ثلاث فئات أمان للـbiometrics؛ ويُنصح بالتأكد من أن جهازك ضمن Class 3 قبل تفعيل الـbiometrics.

### التشفير على مستوى الجهاز

إذا كان جهازك [مشفرًا](../encryption.md)، تكون بياناتك أكثر أمانا عندما يكون الجهاز مغلقا بالكامل، وليس في وضع السكون فقط، أي قبل إدخال مفتاح التشفير أو كلمة مرور شاشة القفل للمرة الأولى. على الهواتف، يُشار إلى حالة الأمان الأعلى هذه باسم "Before First Unlock" (BFU)، وبعد إدخال كلمة المرور الصحيحة لأول مرة عقب إعادة التشغيل أو تشغيل الهاتف، تصبح الحالة "After First Unlock" (AFU). تُعد حالة الـ AFU أقل أمانا بكثير من الـ BFU في مواجهة أدوات التحليل الجنائي الرقمي وغيرها من أساليب الاستغلال. لذلك، إذا كنت قلقا من وصول مهاجم فعليا إلى جهازك، فمن الأفضل إيقاف تشغيله بالكامل عندما لا تستخدمه.

قد لا يكون هذا عمليا دائما، لذا فكّر فيما إذا كان يستحق ذلك. ومع ذلك، حتى وضع الـ AFU يظل فعّالًا ضد معظم التهديدات، ما دمت تستخدم مفتاح تشفير قويًا.

## المكونات الخارجية

لا يمكن للمكونات الداخلية لجهازك وحدها حمايتك من بعض التهديدات. العديد من هذه الخيارات تعتمد بشكل كبير على حالتك؛ لذا قيّم ما إذا كانت ضرورية فعلًا ضمن الـ Threat Model الخاص بك.

### مفاتيح الأمان المادية (Hardware Security Keys)

مفاتيح الأمان المادية هي أجهزة تستخدم تشفيرا قويا للتحقق من هويتك عند تسجيل الدخول إلى جهاز أو حساب. الفكرة هي أنه لا يمكن نسخ هذه المفاتيح، لذلك يمكنك استخدامها لحماية حساباتك بحيث لا يمكن الوصول إليها إلا عند امتلاك المفتاح فعليا، مما يمنع العديد من الهجمات عن بُعد.

[مفاتيح الأمان المادية الموصى بها :material-arrow-right-drop-circle:](../security-keys.md){ .md-button .md-button--primary } [اعرف المزيد عن مفاتيح الأمان المادية :material-arrow-right-drop-circle:](multi-factor-authentication.md#hardware-security-keys){ .md-button }

### الكاميرا / الميكروفون

إذا كنت لا تريد الاعتماد على إعدادات الأذونات في نظام التشغيل لمنع تشغيل الكاميرا من الأساس، يمكنك شراء أغطية للكاميرا تمنع وصول الضوء إليها فعليا. يمكنك أيضا شراء جهاز لا يحتوي على كاميرا مدمجة، واستخدام كاميرا خارجية يمكنك فصلها بعد الانتهاء من استخدامها. بعض الأجهزة تحتوي على غطاء مدمج للكاميرا أو زر فعلي يقطع عنها الكهرباء تماما.

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

يجب أن تشتري فقط أغطية كاميرا تناسب حاسوبك المحمول ولا تسبب أي ضرر عند إغلاق الشاشة. سيؤثر تغطية الكاميرا في ميزات السطوع التلقائي والمصادقة بالوجه.

</div>

بالنسبة إلى الوصول إلى الميكروفون، ستحتاج في معظم الحالات إلى الاعتماد على إعدادات الأذونات المدمجة في نظام التشغيل. بدلًا من ذلك، يمكنك شراء جهاز لا يحتوي على ميكروفون مدمج، واستخدام ميكروفون خارجي يمكنك فصله بعد الانتهاء من استخدامه. بعض الأجهزة، مثل [MacBook أو iPad](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web)، تفصل الميكروفون فعليا عند إغلاق الجهاز.

تحتوي العديد من أجهزة الكمبيوتر على خيار في الـ BIOS لتعطيل الكاميرا والميكروفون. عند تعطيلها من الـ BIOS، لن يتعرّف النظام على الكاميرا أو الميكروفون كأجهزة حتى بعد تشغيل الكمبيوتر.

### شاشات الخصوصية

شاشات الخصوصية هي طبقة يمكنك وضعها فوق شاشتك العادية، بحيث لا يمكن رؤية محتوى الشاشة إلا من زاوية محددة. هذه الشاشات مفيدة إذا كان الـ Threat Model لديك يشمل أشخاصا قد ينظرون إلى شاشتك، لكنها ليست حلا مضمونا، إذ يمكن لأي شخص تغيير زاوية النظر ورؤية ما يظهر على الشاشة.

### مفاتيح الأمان عند عدم الاستجابة

هو نظام يجعل الآلة تتوقف تلقائيا إذا لم يكن الشخص الذي يشغلها موجودا أو قادرا على التحكم بها. صممت هذه الأنظمة في الأصل كوسيلة أمان، لكن يمكن تطبيق الفكرة نفسها على الأجهزة الإلكترونية لقفلها عندما لا تكون موجودا.

تستطيع بعض أجهزة الكمبيوتر المحمولة [اكتشاف](https://support.microsoft.com/en-us/windows/managing-presence-sensing-settings-in-windows-11-82285c93-440c-4e15-9081-c9e38c1290bb) وجودك، ويمكنها قفل الجهاز تلقائيا عندما لا تكون جالسا أمام الشاشة. يجب عليك التحقق من إعدادات نظام التشغيل لمعرفة ما إذا كان جهازك يدعم هذه الميزة.

يمكنك أيضا استخدام كابلات مثل [BusKill](https://buskill.in)، والتي تقفل جهاز الكمبيوتر أو تمسح بياناته عند فصل الكابل.

### Anti-Interdiction/Evil Maid Attack

The best way to prevent a targeted attack against you before a device is in your possession is to purchase a device in a physical store, rather than ordering it to your address.

Make sure your device supports secure boot/verified boot, and you have it enabled. Try to avoid leaving your device unattended whenever possible.

### Kensington Locks

Many laptops come equipped with a [Kensington slot](https://www.kensington.com/solutions/product-category/security/?srsltid=AfmBOorQOlRnqRJOAqM-Mvl7wumed0wBdiOgktlvdidpMHNIvGfwj9VI) that can be used to secure your device with a **metal cable** that locks into the slot on your machine. These locks can be combination locks or keyed.

As with all locks, Kensington locks are vulnerable to [physical attacks](https://youtu.be/vgvCxL7dMJk) so you should mainly use them to deter petty theft. You can secure your laptop at home or even when you're out in public using a table leg or something that won't move easily.

## Secure your Network

### Compartmentalization

Many solutions exist that allow you to separate what you're doing on a computer, such as virtual machines and sandboxing. However, the best compartmentalization is physical separation. This is useful especially for situations where certain software requires you to bypass security features in your OS, such as with anti-cheat software bundled with many games.

For gaming, it may be useful to designate one machine as your "gaming" machine and only use it for that one task. Keep it on a separate VLAN. This may require the use of a managed switch and a router that supports segregated networks.

Most consumer routers allow you to do this by enabling a separate "guest" network that can't talk to your main network. All untrusted devices can go here, including IoT devices like your smart fridge, thermostat, TV, etc.

### Minimalism

As the saying goes, "less is more". The fewer devices you have connected to your network, the less potential attack surface you'll have and the less work it will be to make sure they all stay up-to-date.

You may find it useful to go around your home and make a list of every connected device you have to help you keep track.

### Routers

Your router handles all your network traffic and acts as your first line of defense between you and the open internet.

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

A lot of routers come with storage to put your files on so you can access them from any computer on your network. We recommend you don't use networking devices for things other than networking. In the event your router was compromised, your files would also be compromised.

</div>

The most important thing to think about with routers is keeping them up-to-date. Many modern routers will automatically install updates, but many others won't. You should check on your router's settings page for this option. That page can usually be accessed by typing `192.168.1.1` or `192.168.0.1` into the URL bar of any browser assuming you're on the same network. You can also check in the network settings of your OS for "router" or "gateway".

If your router does not support automatic updates, you will need to go to the manufacturer's site to download the updates and apply them manually.

Many consumer-grade routers aren't supported for very long. If your router isn't supported by the manufacturer anymore, you can check if it's supported by [FOSS firmware](../router.md). You can also buy routers that come with FOSS firmware installed by default; these tend to be supported longer than most routers.

Some ISPs provide a combined router/modem. It can be beneficial for security to purchase a separate router and set your ISP router/modem into modem-only mode. This way, even when your ISP-provided router is no longer getting updates, you can still get security updates and patches. It also means any problems that affect your modem won't affect your router and vice versa.
