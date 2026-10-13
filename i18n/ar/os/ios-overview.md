---
title: نظرة عامة على iOS
icon: simple/apple
description: الـ iOS هو نظام تشغيل للهواتف المحمولة طورته Apple لأجهزة iPhone.
---

الـ **iOS** و**iPadOS** هما نظاما تشغيل مغلقا المصدر طوّرتهما Apple لأجهزة iPhone وiPad على الترتيب. إذا كان لديك جهاز محمول من Apple، يمكنك تحسين خصوصيتك من خلال تعطيل بعض ميزات telemetry المدمجة التي تجمع بيانات الاستخدام، وضبط بعض إعدادات الخصوصية والأمان الموجودة في النظام لجعل جهازك أكثر أمانا.

## ملاحظات حول الخصوصية

غالبا ما يشيد خبراء الأمان بأجهزة iOS لقوة حمايتها للبيانات واتباعها لأحدث الممارسات الأمنية الموصى بها. ومع ذلك، فإن القيود التي تفرضها Apple على نظامها، خاصةً في أجهزتها المحمولة، لا تزال تؤثر سلبا على الخصوصية بعدة طرق.

نرى عموما أن iOS يوفر لمعظم المستخدمين حماية للخصوصية والأمان أفضل من المتوسط، مقارنةً بأجهزة Android التي تعمل بنسخته الأصلية من أي شركة مصنّعة. ومع ذلك، يمكنك الحصول على مستوى أعلى من الخصوصية باستخدام [نظام Android مخصص](../android/distributions.md) مثل GrapheneOS، إذا كنت ترغب في الاستغناء تماما عن الخدمات السحابية من Apple أو Google أو كنت بحاجة إلى ذلك.

### قفل التنشيط

يجب التحقق من جميع أجهزة iOS عبر خوادم قفل التنشيط (Activation Lock) التابعة لشركة Apple عند إعدادها لأول مرة أو إعادة ضبطها، مما يعني أنك **بحاجة** إلى اتصال بالإنترنت لاستخدام جهاز iOS.

### متجر التطبيقات الإلزامي

المصدر الوحيد للتطبيقات على iOS هو متجر App Store التابع لشركة Apple، والذي يتطلب حساب Apple للوصول إليه. هذا يعني أن Apple تحتفظ بسجل لجميع التطبيقات التي تثبتها على جهازك، ويمكنها على الأرجح ربط هذه المعلومات بهويتك الحقيقية إذا أضفت وسيلة دفع إلى App Store.

### جمع بيانات الاستخدام بشكل ينتهك الخصوصية

واجهت Apple في السابق مشكلات في فصل بيانات telemetry التي تجمعها على iOS عن حسابات Apple بشكل صحيح. في عام [2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings)، تبين أن Apple كانت ترسل تسجيلات Siri إلى خوادمها ليراجعها موظفون لدى شركات خارجية يدويا، وكان بعضها يحتوي على معلومات شديدة السرية. ورغم أن Apple أوقفت هذا البرنامج مؤقتا بعد [انتشار التقارير عنه](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana)، فإنها أضافت بعد بضعة أشهر، في تحديث لاحق لنظام iOS، خيارًا يتيح للمستخدمين [**منع**](https://theguardian.com/technology/2019/oct/30/apple-lets-users-opt-out-of-having-siri-conversations-recorded) رفع محادثاتهم مع Siri. علاوة على ذلك، في عام 2021، [عدلت Apple](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance) طريقة عمل Siri بحيث تعالج التسجيلات الصوتية على الجهاز نفسه بدلًا من إرسالها إلى خوادمها.

وفي الآونة الأخيرة، تبين أن Apple ترسل بيانات تحليل الاستخدام حتى عند [تعطيل مشاركة هذه البيانات في iOS](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558). ويبدو أنه يمكن بسهولة [ربط](https://twitter.com/mysk_co/status/1594515229915979776) هذه البيانات بمعرفات فريدة لحسابات iCloud، رغم أن Apple تقول إنها منفصلة عن حسابات Apple.

### حركة مرور الإنترنت خارج اتصالات VPN النشطة

تنص سياسة الخصوصية لدى Apple [فيما يتعلق بخدمات VPN](https://apple.com/legal/privacy/data/en/vpns) على ما يلي:

> حتى عند تشغيل VPN، قد تمر بعض اتصالات الإنترنت الضرورية لخدمات النظام الأساسية خارج اتصال VPN، حتى يتمكن جهازك من العمل بشكل صحيح.

## الإعدادات الموصى بها

**ملاحظة:** يفترض هذا الدليل أنك تستخدم أحدث إصدار من iOS.

### iCloud

ترتبط معظم المخاوف المتعلقة بالخصوصية والأمان في منتجات Apple بخدماتها السحابية، وليس بأجهزتها أو برامجها. عندما تستخدم خدمات Apple مثل iCloud، تُخزن معظم معلوماتك على خوادم الشركة، وتُحمى بمفاتيح تشفير تستطيع Apple الوصول إليها بشكل افتراضي. يمكنك الاطلاع على [وثائق Apple](https://support.apple.com/HT202303) لمعرفة الخدمات التي تستخدم End-to-End Encryption. أي بيانات يُذكر أنها مشفرة "in transit" أو "on server" تعني أن Apple قد تتمكن من الوصول إليها دون إذنك. استغلت جهات إنفاذ القانون هذه الإمكانية أحيانا للوصول إلى بياناتك رغم أنها مشفّرة بشكل آمن على جهازك. وبالطبع، فإن Apple معرّضة أيضًا لاختراقات البيانات مثل أي شركة أخرى.

لذلك، إذا كنت تستخدم iCloud، فمن الأفضل [تفعيل **Advanced Data Protection.**](https://support.apple.com/HT212520) تعمل هذه الميزة على تشفير جميع بياناتك تقريبا على iCloud باستخدام مفاتيح تشفير مخزنة على أجهزتك بدلا من خوادم Apple، وذلك من خلال End-to-End Encryption. وبهذا، تظل بياناتك محمية حتى في حال حدوث اختراق للبيانات، ولا تستطيع Apple الاطلاع عليها.

رغم أن التشفير الذي تستخدمه ميزة Advanced Data Protection قوي، [فإنه ليس بمستوى *قوة* التشفير](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) الذي توفره بعض[ الخدمات السحابية](../cloud.md) الأخرى، خاصةً فيما يتعلق بـ iCloud Drive. ننصح بشدة بتفعيل Advanced Data Protection إذا كنت تستخدم iCloud، لكننا ننصحك أيضا بالتفكير في استخدام خدمة بديلة [تهتم بالخصوصية](../tools.md) بشكل أكبر. ومع ذلك، فمن غير المرجح أن تؤثر هذه الاختلافات في التشفير على معظم المستخدمين.

يمكنك أيضا حماية بياناتك عن طريق تقليل البيانات التي تزامنها مع iCloud من الأساس. في أعلى تطبيق **الإعدادات**، سيظهر اسمك وصورتك الشخصية إذا كنت قد سجلت الدخول إلى iCloud. اضغط عليه، ثم اختر **iCloud**، وأوقف المزامنة لأي خدمات لا تريد مزامنتها مع iCloud. قد تظهر بعض تطبيقات الجهات الخارجية ضمن قائمة **Show All** إذا كانت تزامن بياناتها مع iCloud، ويمكنك إيقاف مزامنتها من هنا.

#### iCloud+

يتضمن الاشتراك المدفوع في **iCloud+** (بأي خطة تخزين على iCloud) بعض الميزات التي تساعد على حماية خصوصيتك. رغم أن هذه الميزات قد تكون مناسبة لمستخدمي iCloud الحاليين، فإننا لا ننصح بالاشتراك في iCloud+ من أجلها فقط، بدلا من استخدام [VPN](../vpn.md) وخدمة مستقلة لإنشاء [عناوين بريد إلكتروني](../email-aliasing.md) بديلة.

الـ [**Private Relay**](https://apple.com/legal/privacy/data/en/icloud-relay) هي خدمة Proxy تمرر جميع اتصالات Safari، واستعلامات DNS، والاتصالات غير المشفرة على جهازك عبر خادمين: أحدهما تابع لشركة Apple، والآخر تابع لشركة خارجية (مثل Akamai وCloudflare وFastly). من الناحية النظرية، يفترض أن يمنع هذا أي جهة مشاركة في الخدمة، بما فيها Apple، من معرفة جميع المواقع التي تزورها أثناء استخدامك لها. على عكس VPN، لا تحمي خدمة Private Relay الاتصالات المشفرة بالفعل.

خدمة **Hide My Email** هي خدمة من Apple لإنشاء عناوين بريد إلكتروني بديلة. يمكنك إنشاء عنوان بريد إلكتروني بديل مجانا عند استخدام *Sign In With Apple* على موقع أو تطبيق، أو إنشاء عدد غير محدود من العناوين البديلة وقتما تشاء من خلال اشتراك مدفوع في iCloud+. تتميز خدمة Hide My Email باستخدام نطاق `@icloud.com` لعناوين البريد الإلكتروني البديلة، مما يجعل احتمال حظرها أقل مقارنة بخدمات أخرى. لكنها لا توفر بعض الميزات الموجودة في الخدمات المستقلة، مثل تشفير PGP التلقائي أو دعم صناديق بريد متعددة.

#### الوسائط والمشتريات

في أعلى تطبيق **الإعدادات**، سيظهر اسمك وصورتك الشخصية إذا كنت قد سجلت الدخول إلى حساب Apple. اضغط عليه، ثم اختر **الوسائط والمشتريات (Media & Purchases)** ← **عرض الحساب (View Account)**.

- [ ] **أوقف التوصيات المخصصة (Personalized Recommendations)**

#### Find My

خدمة **Find My** هي خدمة تتيح لك تتبّع أجهزة Apple الخاصة بك ومشاركة موقعك مع أصدقائك وعائلتك. وتتيح لك أيضا مسح بيانات جهازك عن بُعد في حال سرقته، لمنع السارق من الوصول إلى بياناتك. تكون [بيانات موقعك في Find My](https://apple.com/legal/privacy/data/en/find-my) محمية بتشفير End-to-End Encryption في الحالات التالية:

- عندما تشارك موقعك مع أحد أفراد عائلتك أو أصدقائك، ويستخدم كلاكما iOS 17 أو إصدارا أحدث.
- عندما يكون جهازك غير متصل بالإنترنت، ويتم تحديد موقعه عبر شبكة Find My.

لا تكون بيانات موقعك محمية بتشفير End-to-End Encryption عندما يكون جهازك متصلا بالإنترنت وتستخدم Find My iPhone لتحديد موقعه عن بُعد. عليك أن تقرر ما إذا كانت مزايا الحماية من السرقة التي توفرها ميزة Activation Lock تستحق هذه التنازلات.

في أعلى تطبيق **الإعدادات**، سيظهر اسمك وصورتك الشخصية إذا كنت قد سجلت الدخول إلى حساب Apple. اضغط عليه، ثم اختر **Find My**. يمكنك من هنا اختيار تفعيل ميزات تحديد الموقع في Find My أو إيقافها.

### الاعدادات

يمكنك العثور على العديد من الإعدادات الأخرى المتعلقة بالخصوصية في تطبيق **الإعدادات**.

#### وضع الطيران

يؤدي تفعيل **وضع الطيران** إلى منع هاتفك من الاتصال بأبراج شبكات المحمول. سيظل بإمكانك الاتصال بشبكات Wi-Fi واستخدام Bluetooth، لذا يمكنك تفعيل وضع الطيران عندما تكون متصلًا بشبكة Wi-Fi.

#### Wi-Fi

يمكنك تفعيل ميزة استخدام [عناوين أجهزة عشوائية](https://support.apple.com/en-us/102509#triswitch) لحمايتك من التتبع عبر شبكات Wi-Fi المختلفة، وكذلك عند الاتصال بالشبكة نفسها على مدار الوقت. في الشبكة التي تتصل بها حاليا، اضغط على زر :material-information: التالي:

- [x] اضبط **Private Wi-Fi Address** على **Fixed** أو **Rotating**

يمكنك أيضًا تفعيل خيار **Limit IP Address Tracking**. This is similar to iCloud Private Relay but only affects connections to "known trackers." Because it only affects connections to potentially malicious servers, this setting is probably fine to leave enabled, but if you don't want *any* traffic to be routed through Apple's servers, you should turn it off.

#### Bluetooth

**Bluetooth** should be disabled when you aren't using it as it increases your attack surface. Disabling Bluetooth (or Wi-Fi) via the Control Center only disables it temporarily: you must switch it off in Settings for disabling it to remain effective.

- [ ] Turn off **Bluetooth**

Note that Bluetooth is automatically turned on after every system update.

#### General

Your iPhone's device name will by default contain your first name, and this will be visible to anyone on networks you connect to. You should change this to something more generic, like "iPhone." Select **About** → **Name** and enter the device name you prefer.

It is important to install software updates frequently to get the latest security fixes. You can enable automatic updates to keep your phone up-to-date without needing to constantly check for updates. Select **Software Update** → **Automatic Updates**:

- [x] Turn on **Automatically Install**

**AirDrop** is commonly used to easily share files, but it represents a significant privacy risk. The AirDrop protocol constantly broadcasts your personal information to your surroundings, with [very weak](https://usenix.org/system/files/sec21-heinrich.pdf) security protections. Your identity can easily be discovered by attackers even with limited resources, and the Chinese government has [openly acknowledged](https://arstechnica.com/security/2024/01/hackers-can-id-unique-apple-airdrop-users-chinese-authorities-claim-to-do-just-that) using such techniques to identify AirDrop users in public since 2022.

- [x] Select **AirDrop** → **Receiving Off**

**AirPlay** lets you seamlessly stream content from your iPhone to a TV; however, you might not always want this. Select **AirPlay & Continuity** → **Automatically AirPlay**:

- [x] Select **Never** or **Ask**

**Background App Refresh** allows your apps to refresh their content while you're not using them. This may cause them to make unwanted connections. Turning this off can also save battery life, but may affect an app's ability to receive updated information, particularly weather and messaging apps.

Select **Background App Refresh** and switch off any apps you don't want to continue refreshing in the background. If you don't want any apps to refresh in the background, you can select **Background App Refresh** again and turn it **Off**.

#### Apple Intelligence & Siri

This is available if your device supports **[Apple Intelligence](https://support.apple.com/guide/iphone/apple-intelligence-and-privacy-iphe3f499e0e/ios)**. Apple Intelligence uses a combination of on-device processing and their **[Private Cloud Compute](https://security.apple.com/blog/private-cloud-compute)** for things that take more processing power than your device can provide.

To see a report of all the requests made to Apple's servers, you can navigate to **Privacy & Security** → **Apple Intelligence Report** and press **Export Activity** to see activity from the either the last 15 minutes or 7 days, depending on what you set it for. Similar to the **App Privacy Report** which shows you the recent permissions accessed by the apps on your phone, the Apple Intelligence Report likewise shows what is being sent to Apple's servers while using Apple Intelligence.

Apple Intelligence can integrate with [ChatGPT](https://support.apple.com/guide/iphone/use-chatgpt-with-apple-intelligence-iph00fd3c8c2/ios). If you want ChatGPT integration, you can navigate to **ChatGPT** and press **Set Up**. If you want to disable it, go to the same place:

- [ ] Turn off **Use ChatGPT**

You can also have it ask for confirmation every time if you leave ChatGPT integration on:

- [x] Turn on **Confirm Requests**

If you don't want anyone to be able to control your phone with Siri when it is locked, you can turn that off here.

- [ ] Turn off **Allow Siri When Locked**

#### Face ID/Touch ID & Passcode

Setting a strong password on your phone is the most important step you can take for physical device security. You'll have to make trade-offs here between security and convenience: A longer password will be annoying to type in every time, but a shorter password or PIN will be easier to guess. Setting up Face ID or Touch ID along with a strong password can be a good compromise between usability and security.

Select **Turn Passcode On** or **Change Passcode** → **Passcode Options** → **Custom Alphanumeric Code**. Make sure that you create a [secure password](../basics/passwords-overview.md).

If you wish to use Face ID or Touch ID, you can go ahead and set it up now. Your phone will use the password you set up earlier as a fallback in case your biometric verification fails. Biometric unlock methods are primarily a convenience, although they do stop surveillance cameras or people over your shoulder from watching you input your passcode.

If you use biometrics, you should know how to turn them off quickly in an emergency. Holding down the [side button](https://support.apple.com/en-us/105103) and *either* volume button until you see the Slide to Power Off slider will disable biometrics, requiring your passcode to unlock. Your passcode will be required after your device restarts.

You can similarly disable biometrics by pressing the side button five times, or for devices with Touch ID, you can hold down the side button and nothing else. Make sure you try this in advance, so you know which method works for your device.

**Stolen Device Protection** adds additional security intended to protect your personal data if your device is stolen while unlocked. If you enable both biometric authentication and the [Find My](#find-my) iPhone feature, we recommend enabling this protection:

- [x] Turn on **Stolen Device Protection**

After enabling Stolen Device Protection, [certain actions](https://support.apple.com/HT212510) will require biometric authentication without a password fallback (in the event that a shoulder surfer has obtained your PIN), such as using password autofill, accessing payment information, and disabling Lost Mode. It also adds a security delay to certain actions performed away from your home or another "familiar location," such as requiring a 1-hour timer to reset your Apple Account password or sign out of your Apple Account. This delay is intended to give you time to enable Lost Mode and secure your account before a thief can reset your device.

**Allow Access When Locked** presents options for what you can allow when your phone is locked. Pick and choose which feature you want to disable to prevent unauthorized access if someone gets their hands on your phone. The more of these options you disable, the less someone without your password can do, but the less convenient it will be for you.

iPhones are already resistant to brute-force attacks by making you wait long periods of time after multiple failed attempts; however, there have historically been exploits to get around this. To be extra safe, you can set your phone to wipe itself after 10 failed passcode attempts.

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

With this setting enabled, someone could intentionally wipe your phone by entering the wrong password many times. Make sure you have proper backups and only enable this setting if you feel comfortable with it.

</div>

- [x] Turn on **Erase Data**

#### الخصوصية والأمان

**Location Services** allows you to use features like Find My and Maps. If you don't need these features, you can disable Location Services. Alternatively, you can review and pick which apps can use your location here. Select **Location Services**:

- [ ] Turn off **Location Services**

A purple arrow will appear next to an app in these settings that has used your location recently, while a gray arrow indicates that your location has been accessed within the last 24 hours. If you decide to leave Location Services on, Apple will use it for System Services by default. You can review and pick which services can use your location here. However, if you don't want to submit location analytics to Apple, which they use to improve Apple Maps, you can disable this here as well. Select **System Services**:

- [ ] Turn off **iPhone Analytics**
- [ ] Turn off **Routing & Traffic**
- [ ] Turn off **Improve Maps**

You can decide to allow apps to request to **track** you here. Disabling this disallows all apps from tracking you with your phone's advertising ID. Select **Tracking**:

- [ ] Turn off **Allow Apps to Request to Track**

This is disabled by default and cannot be changed for users under 18.

You should turn off **Research Sensor & Usage Data** if you don't wish to participate in studies. Select **Research Sensor & Usage Data**:

- [ ] Turn off **Sensor & Usage Data Collection**

**[Safety Check](https://support.apple.com/guide/personal-safety/safety-check-iphone-ios-16-ips2aad835e1/1.0/web/1.0)** allows you to quickly view and revoke certain people and apps that might have permission to access your data. Here, you can perform an **Emergency Reset**, immediately resetting permissions for all people and apps which might have access to device resources. You can also **Manage Sharing & Access**, which allows you to review and customize who and what has access to your device and account resources. If you're in an abusive situation, read Apple's [Personal Safety User Guide](https://support.apple.com/guide/personal-safety/welcome/web) for guidance on what you should do.

You should disable analytics if you don't wish to send usage data to Apple. Select **Analytics & Improvements** and unselect the type(s) of analytics that you don't want to send to Apple.

Disable **Personalized Ads** if you don't want targeted ads. Select **Apple Advertising**:

- [ ] Turn off **Personalized Ads**

**App Privacy Report** is a built-in tool that allows you to see which permissions your apps are using. Select **App Privacy Report**:

- [x] Select **Turn On App Privacy Report**

Set wired accessories to ask for permission when you connect them. Select **Wired Accessories**:

- [x] Select **Always Ask** or **Ask for New Accessories**

**[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode)** is a security setting you can enable to make your phone more resistant to attacks. Be aware that certain apps and features [won't work](https://support.apple.com/HT212650) as they do normally.

- [x] Select **Turn On Lockdown Mode**

## Additional Advice

### E2EE Calls

Normal phone calls made with the Phone app through your carrier are not E2EE. Both FaceTime Video and FaceTime Audio calls are E2EE. Alternatively, you can use [another app](../real-time-communication.md) like Signal for E2EE calls.

### Encrypted iMessage

The [color of the message bubble](https://support.apple.com/en-us/104972) in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates the other party is using either the outdated SMS and MMS protocols or RCS. RCS on iOS is **not** E2EE. Currently, the only way to have E2EE in Messages is for both parties to be using iMessage on Apple devices.

If either you or your messaging partner have iCloud Backup enabled without Advanced Data Protection, the encryption key will be stored on Apple's servers, meaning they can access your messages.

By default, you trust Apple's identity servers that you're messaging the right person. To defend yourself from a potentially malicious server, you can enable **[Contact Key Verification](https://support.apple.com/en-us/118246)**. At the top of the **Settings** app where your name is, select it, then go to **Contact Key Verification**.

- [x] Turn on **Verification in iMessage**

Both you and your contacts need to enable Contact Key Verification and follow Apple's [instructions](https://support.apple.com/en-us/118246#verify) for the security assurances mentioned above to take effect.

### Photo Permissions

When an app prompts you for access to your device's photo library, iOS provides you with options to limit what an app can access.

Rather than allow an app to access all the photos on your device, you can allow it to only access whichever photos you choose by tapping the "Select Photos..." option in the permission dialog. You can change photo access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Photos**.

![Photo Permissions](../assets/img/ios/photo-permissions-light.png#only-light) ![Photo Permissions](../assets/img/ios/photo-permissions-dark.png#only-dark)

**Add Photos Only** is a permission that only gives an app the ability to download photos to the photo library. Not all apps which request photo library access provide this option.

![Private Access](../assets/img/ios/private-access-light.png#only-light) ![Private Access](../assets/img/ios/private-access-dark.png#only-dark)

Some apps also support **Private Access**, which functions similarly to the **Limited Access** permission. However, photos shared to apps using Private Access include their location by default. We recommend unchecking this setting if you do not [remove photo metadata](../data-redaction.md) beforehand.

### Contact Permissions

Similarly, rather than allow an app to access all the contacts saved on your device, you can allow it to only access whichever contacts you choose. You can change contact access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Contacts**.

![Contact Permissions](../assets/img/ios/contact-permissions-light.png#only-light) ![Contact Permissions](../assets/img/ios/contact-permissions-dark.png#only-dark)

### Require Biometrics and Hide Apps

iOS offers the ability to lock most apps behind Touch ID/Face ID or your passcode, which can be useful for protecting sensitive content in apps which do not provide the option themselves. You can lock an app by long-pressing on it and selecting **Require Face ID/Touch ID**. Any app locked in this way requires biometric authentication whenever opening it or accessing its contents in other apps. Also, notification previews for locked apps will not be shown.

In addition to locking apps behind biometrics, you can also hide apps so that they don't appear on the Home Screen, App Library, the app list in **Settings**, etc. While hiding apps may be useful in situations where you have to hand your unlocked phone to someone else, the concealment provided by the feature is not absolute, as a hidden app is still visible in some places such as the battery usage list. Moreover, one notable trade off of hiding an app is that you will not receive any of its notifications.

You can hide an app by long-pressing on it and selecting **Require Face ID/Touch ID** → **Hide and Require Face ID/Touch ID**. Note that pre-installed Apple apps, as well as the default web browser and email app, cannot be hidden. Hidden apps reside in a **Hidden** folder at the bottom of the App Library, which can be unlocked using biometrics. This folder appears in the App Library whether you hid any apps or not, which provides you a degree of plausible deniability.

### Guided Access

Sometimes you might want to hand your phone to someone to make a call or do a specific task, but you don't want them to have full access to your phone. In these cases, you can quickly enable **[Guided Access](https://support.apple.com/guide/iphone/lock-iphone-to-one-app-iph7fad0d10/ios)** to lock the phone to one specific app until you authenticate.

<div class="admonition warning" markdown>
<p class="admonition-title">تنوية</p>

Guided Access isn't foolproof, as it's possible you could leak data unintentionally or the feature could be bypassed. You should only use Guided Access for situations where you casually hand your phone to someone to use. You should not use it as a tool to protect against advanced adversaries.

</div>

### Redacting Elements in Images

If you need to hide information in a photo, you can use Apple's built-in editing tools to do so.

You can use the [Clean Up](https://support.apple.com/en-us/121429) feature on supported devices to pixelate faces or remove objects from images.

- Open the **Photos** app and tap the photo you have selected for redaction
- Tap the :material-tune:
- Tap the button labeled **Clean Up**
- Draw a circle around whatever you want to redact. Faces will be pixelated, and it will attempt to delete anything else.

Our warning [against blurring text](../data-redaction.md) also applies here, so we recommend to instead add a black shape with 100% opacity over it. In addition to redacting text, you can also black out any face or object using the **Photos** app.

<div class="annotate" markdown>

- Tap the image you have selected for redaction
- Tap the :material-tune: → :material-dots-horizontal: (1) → Markup → :material-plus:
- Select **Add Shape** and choose the square or circle
- On the toolbar, tap the circle and choose black as the color for filling in the shape. You can also move the shape and increase its size as you see fit.

</div>

1. This may not appear on certain iPhone models.

**Don't** use the highlighter to obfuscate information, as its opacity is not quite 100%.

### Avoid Jailbreaking

Jailbreaking an iPhone undermines its security and makes you vulnerable. Running untrusted, third-party software could cause your device to be infected with malware.

### iOS Betas

Apple always makes beta versions of iOS available early for those that wish to help find and report bugs. We don't recommend installing beta software on your phone. Beta releases are potentially unstable and could have undiscovered security vulnerabilities.

## Security Highlights

### Before First Unlock

If your threat model includes [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} that involve forensic tools, and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. The state *after* a reboot but *before* unlocking your device is referred to as "Before First Unlock" (BFU), and when your device is in that state it makes it [significantly more difficult](https://belkasoft.com/checkm8_glossary) for forensic tools to exploit vulnerabilities to access your data. This BFU state allows you to receive notifications for calls, texts, and alarms, but most of the data on your device is still encrypted and inaccessible. This can be impractical, so consider whether these trade-offs make sense for your situation.

iPhones [automatically reboot](https://support.apple.com/guide/security/protecting-user-data-in-the-face-of-attack-secf5549a4f5/1/web/1#:~:text=On%20an%20iPhone%20or%20iPad%20with%20iOS%2018%20and%20iPadOS%2018%20or%20later%2C%20a%20new%20security%20protection%20will%20restart%20devices%20if%20they%20remain%20locked%20for%20a%20prolonged%20period%20of%20time.) if they're not unlocked after a period of time.

### MTE

The iPhone 17 line and later offer a security enhancement called [Memory Tagging Extension](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension) (MTE), which makes it significantly harder for an attacker to exploit memory corruption vulnerabilities. This always-on protection depends on hardware support, so it's not available for older devices.

For more details on Apple's implementation of MTE, read the [blog post](https://security.apple.com/blog/memory-integrity-enforcement) published by Apple Security Research. We also cover Apple's implementation of MTE and how it compares to Android's implementation in the Google Pixel 8 series and later in our [own article](https://www.privacyguides.org/posts/2025/09/20/memory-integrity-enforcement-changes-the-game-on-ios).
