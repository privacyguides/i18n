---
title: نظرة عامة على macOS
icon: material/apple-finder
description: الـ macOS هو نظام تشغيل أجهزة الكمبيوتر من Apple، ويتكامل مع أجهزتها لتوفير مستوى عالٍ من الأمان.
---

نظام الـ **macOS** هو نظام تشغيل مبني على Unix، طورته Apple لأجهزة Mac. لتعزيز الخصوصية في macOS، يمكنك تعطيل ميزات الـ telemetry وتشديد إعدادات الخصوصية والأمان الحالية.

أجهزة Mac القديمة التي تعمل بمعالجات Intel وأجهزة Hackintosh لا تدعم جميع ميزات الأمان التي يوفرها macOS. لتعزيز أمان البيانات، ننصح باستخدام جهاز Mac أحدث مزوّد بمعالج [Apple Silicon](https://support.apple.com/HT211814).

## ملاحظات حول الخصوصية

هناك بعض المخاوف المهمة المتعلقة بالخصوصية في macOS التي ينبغي أن تأخذها في الاعتبار. هذه المخاوف تتعلق بنظام التشغيل نفسه، وليس بتطبيقات Apple وخدماتها الأخرى.

### قفل التنشيط

يمكن إعداد أجهزة Apple Silicon الجديدة تماما دون الاتصال بالإنترنت. لكن استعادة جهاز Mac أو إعادة تعيينه **تتطلب** الاتصال بخوادم Apple عبر الإنترنت للتحقق من حالة Activation Lock الخاصة بالجهاز.

### التحقق من إلغاء صلاحية التطبيقات

يجري macOS عمليات تحقق عبر الإنترنت عند فتح التطبيقات، للتأكد من عدم احتوائها على برمجيات خبيثة معروفة، وللتحقق مما إذا كانت شهادة توقيع المطور قد أُلغيت.

تستخدم خدمة OCSP من Apple تشفير HTTPS، لذلك لا تستطيع سوى Apple معرفة التطبيقات التي تفتحها. [نشرت](https://support.apple.com/HT202491) Apple معلومات عن سياسة تسجيل البيانات الخاصة بهذه الخدمة. [وعدت](http://lapcatsoftware.com/articles/2024/8/3.html) Apple أيضا بإضافة خيار يتيح للمستخدمين تعطيل هذا التحقق عبر الإنترنت، لكنها لم تضفه إلى macOS حتى الآن.

مع أنه [يمكنك](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private) تعطيل هذا التحقق يدويا بسهولة نسبية، فإننا لا ننصح بذلك إلا إذا كانت عمليات التحقق من إلغاء الصلاحية التي يجريها macOS ستعرض خصوصيتك لخطر كبير، لأنها تؤدي دورا مهما في منع تشغيل التطبيقات المخترقة.

## الإعدادات الموصى بها

عند إعداد جهاز Mac لأول مرة، سيكون حسابك من نوع Administrator، وله صلاحيات أعلى من حساب المستخدم العادي Standard. يحتوي macOS على عدة وسائل حماية تمنع البرمجيات الخبيثة والبرامج الأخرى من استغلال صلاحيات حساب Administrator، لذلك يعد استخدام هذا الحساب آمنا بشكل عام.

[لكن سبق اكتشاف](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass) ثغرات أمنية قابلة للاستغلال في أدوات الحماية مثل `sudo`. إذا أردت تقليل احتمال استغلال البرامج التي تشغلها لصلاحيات Administrator، يمكنك التفكير في إنشاء حساب ثانٍ من نوع Standard لاستخدامه في مهامك اليومية. ومن فوائد ذلك أيضا أنه يسهل عليك معرفة متى يحتاج أحد التطبيقات إلى صلاحيات Administrator، لأنه سيطلب منك إدخال بيانات حساب Administrator في كل مرة يحتاج فيها إلى هذه الصلاحيات.

إذا كنت تستخدم حسابا ثانيا، فليس من الضروري تسجيل الدخول إلى حساب Administrator الأصلي من شاشة تسجيل الدخول في macOS. عندما تنفذ مهمة من حساب Standard تتطلب صلاحيات Administrator، من المفترض أن يطلب منك النظام إدخال بيانات حساب Administrator لمنح الصلاحيات المطلوبة لهذه المرة فقط، دون الحاجة إلى مغادرة حساب Standard. تقدّم Apple [إرشادات](https://support.apple.com/HT203998) حول كيفية إخفاء حساب Administrator إذا كنت تفضل ظهور حساب واحد فقط على شاشة تسجيل الدخول.

### iCloud

عند استخدام خدمات Apple مثل iCloud، تُخزن معظم معلوماتك على خوادمها وتحمى بمفاتيح تشفير *تستطيع Apple الوصول إليها افتراضيا*. تُسمّي Apple هذا النظام [Standard Data Protection](https://support.apple.com/en-us/102651).

لذلك، إذا كنت تستخدم iCloud، فننصحك [ **Advanced Data Protection**](https://support.apple.com/HT212520). تشفر هذه الميزة الغالبية العظمى من بياناتك في iCloud باستخدام مفاتيح تشفير محفوظة على أجهزتك بدلا من خوادم Apple، وذلك من خلال التشفير من طرف إلى طرف (End-to-End Encryption). وبهذا تظل بياناتك محمية حتى في حال حدوث تسريب للبيانات، ولا تستطيع Apple نفسها الاطلاع عليها.

إذا أردت تثبيت التطبيقات من App Store دون تفعيل iCloud، يمكنك تسجيل الدخول إلى Apple Account من داخل App Store بدلًا من **System Settings**.

### إعدادات النظام

هناك عدة إعدادات مدمجة في النظام ينبغي مراجعتها أو تغييرها لتعزيز أمان جهازك. افتح تطبيق **Settings**:

#### البلوتوث

- [ ] أوقف تشغيل **Bluetooth** (إلا إذا كنت تستخدمه حاليا)

#### الشبكة

بحسب نوع الاتصال الذي تستخدمه، سواء **Wi-Fi** أو **Ethernet** (ويظهر بجانبه مؤشر أخضر وكلمة "connected")، اضغط على الأيقونة المناسبة.

اضغط على زر "Details" بجانب اسم شبكتك:

- [x] اختر **Rotating** ضمن إعداد **Private Wi-Fi address**

- [x] فعّل خيار **Limit IP address tracking**

##### Firewall

يمنع جدار الحماية الاتصالات غير المرغوب فيها عبر الشبكة. كلما كانت إعدادات جدار الحماية أكثر صرامة، زاد مستوى أمان جهاز Mac. لكن قد يؤدي ذلك إلى حظر بعض الخدمات. ينبغي ضبط جدار الحماية على أكثر الإعدادات صرامة دون حظر الخدمات التي تستخدمها.

- [x] فعّل خيار **Firewall**

Click the **Options** button:

- [x] Turn on **Block all incoming connections**

If this configuration is too strict, you can come back and uncheck this. However, macOS will typically prompt you to allow incoming connections for an app if the app requests it.

#### General

By default, your device name will be something like "[your name]'s iMac". Because this name is [publicly broadcast on your network](https://support.apple.com/guide/mac-help/change-computers-local-hostname-mac-mchlp2322/26/mac/26#:~:text=The%20local%20hostname%2C%20or%20local%20network%20name%2C%20is%20displayed%20at%20the%20bottom%20of%20the%20Sharing%20settings%20window.%20It%20identifies%20your%20Mac%20to%20Bonjour%2Dcompatible%20services.), you'll want to change your device name to something generic like "Mac".

Click on **About** and type your desired device name into the **Name** field.

##### Software Updates

You should automatically install all available updates to make sure your Mac has the latest security fixes.

Click the small :material-information-outline: icon next to **Automatic Updates**:

- [x] Turn on **Download new updates when available**

- [x] Turn on **Install macOS updates**

- [x] Turn on **Install Security Responses and system files**

#### Apple Intelligence & Siri

If you do not use these features on macOS, you should disable them:

- [ ] Turn off **Apple Intelligence**
- [ ] Turn off **Siri**

**[Apple Intelligence](https://apple.com/legal/privacy/data/en/intelligence-engine)** is only available if your device supports it. Apple Intelligence uses a combination of on-device processing and their [Private Cloud Compute](https://security.apple.com/blog/private-cloud-compute) for things that take more processing power than your device can provide.

To see a report of all the data sent via Apple Intelligence, you can navigate to **Privacy & Security** → **Apple Intelligence Report** and press **Export Activity** to see activity from the either the last 15 minutes or 7 days, depending on what you set it for. Similar to the **App Privacy Report** which shows you the recent permissions accessed by the apps on your phone, the Apple Intelligence Report likewise shows what is being sent to Apple's servers while using Apple Intelligence.

By default, ChatGPT integration is disabled. If you don't want ChatGPT integration anymore, you can navigate to **ChatGPT**:

- [ ] Turn off **Use ChatGPT**

You can also have it ask for confirmation every time if you leave ChatGPT integration on:

- [x] Turn on **Confirm Requests**

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

Any request made with ChatGPT will be sent to ChatGPT's servers, there is no on-device processing and no PCC like with Apple Intelligence.

</div>

#### الخصوصية والأمان

Whenever an application requests a permission, it will show up here. You can decide which applications you want to allow or deny specific permissions.

##### Location Services

You can individually allow location services per-app. If you don't need apps to use your location, turning off location services entirely is the most private option.

- [ ] عطّل خدمات الموقع **(Location Services)**

##### Analytics & Improvements

Decide whether you want to share analytics data with Apple and app developers.

##### Apple Advertising

Decide whether you want personalized ads based on your usage.

- [ ] عطّل خيار **Personalized Ads**

##### FileVault

On modern devices with a Secure Enclave (Apple T2 Security Chip, Apple Silicon), your data is always encrypted, but is decrypted automatically by a hardware key if your device doesn't detect it's been tampered with. Enabling [FileVault](../encryption.md#filevault) additionally requires your password to decrypt your data, greatly improving security, especially when powered off or before the first login after powering on.

On older Intel-based Mac computers, FileVault is the only form of disk encryption available by default, and should always be enabled.

- [x] Click **Turn On**

##### Lockdown Mode

**[Lockdown Mode](https://support.apple.com/guide/mac-help/lock-mac-targeted-a-cyberattack-ibrw66f4e191/mac)** disables some features in order to improve security. Some apps or features won't work the same way they do when it's off. For example, Javascript Just-In-Time ([JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers)) compilation and [WebAssembly](https://developer.mozilla.org/docs/WebAssembly) are disabled in Safari with Lockdown Mode enabled. We recommend enabling Lockdown Mode and seeing whether it significantly impacts daily usage.

- [x] Click **Turn On**

### تغيير عنوان MAC عشوائيا

macOS uses a randomized MAC address when [performing Wi-Fi scans](https://support.apple.com/guide/security/privacy-features-connecting-wireless-networks-secb9cb3140c/web) while disconnected from a network.

You can set your [MAC address to be randomized](https://support.apple.com/en-us/102509) per network and rotate occasionally to prevent tracking between networks and on the same network over time.

انتقل إلى **System Settings** → **Network** → **Wi-Fi** → **Details**، ثم اضبط **Private Wi-Fi address** على **Fixed** إذا كنت تريد عنوانًا ثابتًا وفريدًا للشبكة التي تتصل بها، أو على **Rotating** إذا كنت تريد أن يتغير العنوان بمرور الوقت.

فكر أيضا في تغيير اسم جهازك (hostname)، فهو معرف آخر لجهازك يُعلَن عنه على الشبكة التي تتصل بها. قد ترغب في اختيار اسم عام لجهازك، مثل "MacBook Air" أو "Laptop" أو "John's MacBook Pro" أو "iPhone"، من خلال **System Settings** → **General** → **Sharing**.

## وسائل الحماية الأمنية

يعتمد macOS على مبدأ الدفاع متعدد الطبقات (Defense in Depth)، باستخدام عدة طبقات من الحماية على مستوى البرامج والأجهزة، ولكل طبقة خصائص مختلفة. يساعد ذلك على منع اختراق أمان النظام بالكامل في حال فشل إحدى طبقات الحماية.

### أمان البرامج

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

يتيح لك macOS تثبيت التحديثات التجريبية (Beta). هذه الإصدارات غير مستقرة، وقد تجمع بيانات [telemetry إضافية](https://beta.apple.com/privacy) لأنها مخصّصة للاختبار. لهذا السبب، ننصحك بتجنب استخدام الإصدارات التجريبية من البرامج بشكل عام.

</div>

#### وحدة تخزين النظام الموقعة (Signed System Volume)

تُحمى مكوّنات macOS داخل الـ [Signed System Volume](https://support.apple.com/guide/security/signed-system-volume-security-secd698747c9/web) ومخصصة للقراءة فقط، مما يمنعك أنت والبرمجيات الخبيثة من تعديل ملفات النظام المهمة.

يتحقق النظام من سلامة وحدة تخزين النظام أثناء تشغيله، ويرفض أي بيانات لا يغطيها توقيع تشفيري صالح من Apple.

#### حماية سلامة النظام (System Integrity Protection)

يفرض macOS قيودا أمنية معينة لا يمكن تجاوزها. تُعرف هذه القيود باسم [Mandatory Access Controls](https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/1/web/1)، وهي الأساس الذي تعتمد عليه ميزات sandboxing والرقابة الأبوية (parental controls) و[System Integrity Protection](https://support.apple.com/en-us/102149) في macOS.

تجعل ميزة System Integrity Protection مواقع ملفات النظام المهمة للقراءة فقط، لحمايتها من التعديل بواسطة البرمجيات الخبيثة. وتأتي هذه الحماية إلى جانب ميزة الـ Kernel Integrity Protection المعتمدة على مكونات الجهاز، والتي تمنع تعديل نواة النظام (Kernel) أثناء وجودها في الذاكرة.

#### أمان التطبيقات

##### عزل التطبيقات (App Sandbox)

في macOS، يحدد المطور ما إذا كان التطبيق سيعمل داخل بيئة معزولة (sandbox) عند توقيعه رقميا. تساعد ميزة [App Sandbox](https://developer.apple.com/documentation/xcode/configuring-the-macos-app-sandbox) على الحماية من الثغرات الأمنية في التطبيقات التي تستخدمها، من خلال تقييد ما يمكن للمهاجم الوصول إليه إذا نجح في استغلال ثغرة في أحد هذه التطبيقات. لا تستطيع ميزة App Sandbox *وحدها* الحماية من[:material-package-variant-closed-remove: هجمات سلسلة التوريد](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} التي ينفّذها مطوّرون خبيثون. للحماية من هذه الهجمات، يجب أن تفرض جهة أخرى غير المطور نفسه استخدام sandboxing، كما هو الحال في [App Store](https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/1/web/1#:~:text=All%20apps%20from%20the%20App%20Store%20are%20sandboxed%20to%20restrict%20access%20to%20data%20stored%20by%20other%20apps.).

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

التطبيقات التي تُنزل من خارج App Store الرسمي ليست ملزَمة باستخدام sandboxing. إذا كانت الحماية من [:material-bug-outline: الهجمات السلبية (Passive attacks)](:material-bug-outline:){ .pg-orange } من أولويات الـ Threat Model الخاص بك، فقد ترغب في التحقق مما إذا كانت البرامج التي تنزّلها من خارج App Store تستخدم sandboxing، لأن المطور هو من يختار تفعيل هذه الحماية.

</div>

يمكنك التحقق مما إذا كان التطبيق يستخدم App Sandbox بعدة طرق:

يمكنك استخدام [Activity Monitor ](https://developer.apple.com/documentation/security/protecting-user-data-with-app-sandbox#Verify-that-your-app-uses-App-Sandbox)للتحقق مما إذا كانت التطبيقات قيد التشغيل تعمل داخل بيئة معزولة (sandbox).

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

كون إحدى عمليات التطبيق تعمل داخل بيئة معزولة (sandbox) لا يعني بالضرورة أن جميع عملياته معزولة.

</div>

بدلا من ذلك، يمكنك التحقق مما إذا كانت التطبيقات تستخدم sandboxing قبل تشغيلها، من خلال تنفيذ الأمر التالي في Terminal:

``` zsh
codesign -dvvv --entitlements - <path to your app>
```

إذا كان التطبيق يعمل داخل بيئة معزولة (sandbox)، فستظهر لك النتيجة التالية:

``` zsh
    [Key] com.apple.security.app-sandbox
    [Value]
        [Bool] true
```

إذا اكتشفت أن التطبيق الذي تريد تشغيله لا يستخدم sandboxing، فيمكنك عزله [بطرق](../basics/common-threats.md#security-and-privacy) أخرى، مثل استخدام الأجهزة الافتراضية (Virtual Machines) أو جهاز منفصل، أو اختيار تطبيق مشابه يستخدم sandboxing، أو تجنّب استخدام التطبيق غير المعزول تمامًا.

##### بيئة التشغيل المحصّنة (Hardened Runtime)

توفّر ميزة [Hardened Runtime](https://developer.apple.com/documentation/security/hardened_runtime) طبقة حماية إضافية للتطبيقات، تساعد على منع أنواع معيّنة من استغلال الثغرات الأمنية. تعزز هذه الميزة أمان التطبيقات ضد استغلال الثغرات الأمنية، من خلال تعطيل بعض الوظائف مثل JIT.

يمكنك التحقق مما إذا كان التطبيق يستخدم Hardened Runtime من خلال تنفيذ الأمر التالي:

``` zsh
codesign -dv <path to your app>
```

إذا كانت ميزة Hardened Runtime مفعّلة، فستظهر لك القيمة `flags=0x10000(runtime)`. ظهور `runtime` في النتيجة يعني أن ميزة Hardened Runtime مفعّلة. قد تظهر علامات أخرى، لكن ما نبحث عنه هنا هو العلامة runtime.

يمكنك إظهار عمود باسم "Restricted" في Activity Monitor، يوضّح ما إذا كانت العملية تخضع لقيود تمنع الـ injecting code فيها عبر الـ [dynamic linker](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html) في macOS. من الأفضل أن تظهر القيمة "Yes".

##### Antivirus

يأتي macOS مزوّدًا بنوعين من الحماية ضد [البرمجيات الخبيثة](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/1/web/1):

1. توفّر عملية مراجعة التطبيقات في App Store حماية تساعد على منع تشغيل البرمجيات الخبيثة من الأساس. أما التطبيقات الخارجية، فتساعد خدمة *Notarization* (المرتبطة بميزة *Gatekeeper*) على حمايتها، حيث تفحصها Apple بحثًا عن برمجيات خبيثة معروفة قبل السماح بتشغيلها. يجب أن يوقع المطوّرون التطبيقات رقميا باستخدام مفتاح توفره لهم Apple. وهذا يضمن أن البرامج التي تشغلها صادرة عن مطوّريها الحقيقيين. تتطلب عملية Notarization أيضا من المطورين تفعيل ميزة Hardened Runtime في تطبيقاتهم، مما يحد من بعض طرق استغلال الثغرات الأمنية.
2. Protection against other malware and remediation from existing malware on your system is provided by *XProtect*, a more traditional antivirus software built-in to macOS.

We recommend against installing third-party antivirus software as they typically do not have the system-level access required to properly function anyway, because of Apple's limitations on third-party apps, and because granting the high levels of access they do ask for often poses an even greater security and privacy risk to your computer.

##### النسخ الاحتياطي

macOS comes with automatic backup software called [Time Machine](https://support.apple.com/HT201250), so you can create [encrypted backups](https://support.apple.com/guide/mac-help/keep-your-time-machine-backup-disk-secure-mh21241/mac) to an external drive or a network drive in the event of corrupted/deleted files.

### Hardware Security

Many modern security features in macOS—such as modern Secure Boot, hardware-level exploit mitigation, OS integrity checks, and file-based encryption—rely on Apple Silicon, and Apple's newer hardware always has the [best security](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). We only encourage the use of Apple Silicon, and not older Intel-based Mac computers or Hackintoshes.

Some of these modern security features are available on older Intel-based Mac computers with the Apple T2 Security Chip, but that chip is susceptible to the *checkm8* exploit which could compromise its security.

If you use Bluetooth accessories such as a keyboard, we recommend that you use official Apple ones as their firmware will [automatically be updated](https://support.apple.com/en-us/120303#:~:text=Firmware%20updates%20are%20automatically%20delivered%20in%20the%20background%20while%20the%20Magic%20Keyboard%20is%20actively%20paired%20to%20a%20device%20running%20macOS%2C%20iOS%2C%20iPadOS%2C%20or%20tvOS.) for you by macOS. Using third party accessories is fine, but you should remember to install firmware updates for them regularly.

Apple's SoCs focus on [minimizing attack surface](https://support.apple.com/en-vn/guide/security/secf020d1074/web#:~:text=Security%2Dfocused%20hardware%20follows%20the%20principle%20of%20supporting%20limited%20and%20discretely%20defined%20functions%20to%20minimize%20attack%20surface.) by relegating security functions to dedicated hardware with limited functionality.

#### Boot ROM

macOS prevents malware persistence by only allowing official Apple software to run at boot time; this is known as [secure boot](https://support.apple.com/en-vn/guide/security/secac71d5623/1/web/1). Mac computers verify this with a bit of read-only memory on the SoC called the [boot ROM](https://support.apple.com/en-vn/guide/security/aside/sec5240db956/1/web/1), which is [laid down during the manufacturing of the chip](https://support.apple.com/en-vn/guide/security/secf020d1074/1/web/1#:~:text=which%20is%20laid%20down%20during%20Apple%20SoC%20fabrication).

The boot ROM forms the hardware root of trust. This ensures that malware cannot tamper with the boot process, since the boot ROM is immutable. When your Mac boots up, the boot ROM is the first thing that runs, forming the first link in the chain of trust.

Mac computers can be configured to boot in [three security modes](https://support.apple.com/guide/deployment/startup-security-dep5810e849c/web#dep32fb404e1): *Full Security*, *Reduced Security*, and *Permissive Security*, with the default setting being Full Security. You should ideally be using Full Security mode and avoid things like **[kernel extensions](https://support.apple.com/guide/deployment/system-extensions-in-macos-depa5fb8376f/web#dep51e097f45)** that force you to lower your security mode. Make sure to [check](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) that you're using Full Security mode.

#### Secure Enclave

The **[Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/web)** is a security chip built into devices with Apple Silicon which is responsible for storing and generating encryption keys for data at rest as well as Face ID and Touch ID data. It contains its own [separate boot ROM](https://support.apple.com/en-vn/guide/security/sec59b0b31ff/web#sec43006c49f).

You can think of the Secure Enclave as your device's security hub: it has an AES encryption engine and a mechanism to securely store your encryption keys, and it's separated from the rest of the system, so even if the main processor is compromised, it should still be safe.

#### Touch ID

Apple's Touch ID feature allows you to securely unlock your devices using biometrics.

Your biometric data [never leaves your device](https://www.apple.com/legal/privacy/data/en/touch-id/#:~:text=Touch%C2%A0ID%20data%20does%20not%20leave%20your%20device%2C%20and%20is%20never%20backed%20up%20to%20iCloud%20or%20anywhere%20else.); it's stored only in the Secure Enclave.

#### Hardware Microphone Disconnect

All laptops with Apple Silicon or the T2 chip feature a [hardware disconnect](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web) for the built-in microphone whenever the lid is closed. This means that there is no way for an attacker to listen to your Mac's microphone even if the operating system is compromised.

Note that the camera does not have a hardware disconnect, since its view is obscured when the lid is closed anyway.

#### Secure Camera Indicator

The built-in camera in a Mac is designed so that the camera can't turn on without the camera indicator light [also turning on](https://support.apple.com/en-us/102177#:~:text=The%20camera%20is%20engineered%20so%20that%20it%20can’t%20activate%20without%20the%20camera%20indicator%20light%20also%20turning%20on.%20This%20is%20how%20you%20can%20tell%20if%20your%20camera%20is%20on.).

#### Peripheral Processor Security

Computers have [built-in processors](https://support.apple.com/en-vn/guide/security/seca500d4f2b/1/web/1) other than the main CPU that handle things like networking, graphics, power management, etc. These processors can have insufficient security and become compromised, therefore Apple tries to minimize the need for these processors in their hardware.

When it is necessary to use one of these processors, Apple works with the vendor to ensure that the processor

- runs verified firmware from the primary CPU on startup
- has its own Secure Boot chain
- follows minimum cryptographic standards
- ensures known bad firmware is properly revoked
- has its debug interfaces disabled
- is signed with Apple's cryptographic keys

#### Direct Memory Access Protections

Apple Silicon separates each component that requires [direct memory access](https://support.apple.com/guide/security/direct-memory-access-protections-seca4960c2b5/1/web/1). For example, a Thunderbolt port can't access memory designated for the kernel.

#### Terminal Secure Keyboard Entry

Enable [Secure Keyboard Entry](https://support.apple.com/guide/terminal/use-secure-keyboard-entry-trml109/mac) to prevent other apps from detecting what you type in the terminal.
