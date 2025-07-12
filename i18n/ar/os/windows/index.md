---
title: نظرة عامة على Windows
icon: مواد متعلقة بنظام Microsoft Windows
description: Microsoft Windows هو نظام تشغيل شائع، لكنه يفتقر إلى الخصوصية بشكل كبير في إعداداته الافتراضية. يقدم هذا الشرح خطوات لتحسين مستوى الخصوصية في جهازك دون الحاجة إلى تغيير نظام التشغيل.
---

**Microsoft Windows** هو نظام تشغيل شائع، ويأتي مُثبتا مسبقا على العديد من أجهزة الحاسوب بشكل افتراضي. الخطوات التالية تهدف إلى تحسين الخصوصية وتقليل جمع البيانات التلقائي والمعلومات التي يُخزنها النظام، من خلال تعطيل بعض الميزات غير الضرورية. مع مرور الوقت، تضيف Microsoft ميزات جديدة إلى نظام التشغيل، والتي تعتمد أحيانا على خدمات سحابية (cloud-based services). بعض هذه الميزات تعتمد على جمع [بيانات إضافية](https://privacy.microsoft.com/data-collection-windows) من جهازك،
وغالبا ما يتم إرسال هذه البيانات إلى خوادم مايكروسوفت عبر الإنترنت لمعالجتها هناك.

من أحدث الأمثلة على ذلك ميزة تُسمى Recall، وهي جزء من مجموعة ميزات الذكاء الاصطناعي Copilot. ميزة Recall تقوم بتصوير الشاشة تلقائيا على فترات منتظمة، لتسجل كل ما تراه أو تستخدمه على جهازك، بحيث يمكنك البحث فيه أو استرجاعه لاحقا. هذه الميزات "المفيدة" تقوم بإنشاء كمية كبيرة من الـ (Metadata)، والتي يمكن تحليلها لاحقا لأغراض التحقيق الجنائي الرقمي. في أغلب الحالات، يُعتبر سجل التصفح العادي كافيا،
ويمكن تعطيل ميزة Recall دون أي ضرر أو تأثير على استخدام الجهاز. المشكلة الرئيسية في ميزة Recall هي أن كل المعلومات التي تحفظها تُخزَن داخل الجهاز نفسه، وتكون غير مشفَرة بمجرد تشغيل الجهاز، وهذا يعني أنه لو أصيب جهازك بفيروس أو برنامج تجسس، يمكن بسهولة سرقة هذه المعلومات. ميزة Recall لا تقوم بإخفاء المعلومات الحساسة مثل كلمات المرور المنسوخة أو البيانات المالية من قاعدة البيانات، لكنها في المقابل تمنع تصوير المحتوى المحمي بحقوق النشر باستخدام تقنيات الحماية (DRM).

للأسف، تمت إضافة هذه الميزة دون التفكير الكافي في آثارها على الخصوصية، خاصة وأنها كانت مفعلة بشكل افتراضي. (وهو ما لم يعد الحال عليه الآنhttps://wired.com/story/microsoft-recall-off-default-security-concerns، بعد أن قررت مايكروسوفت إيقاف تفعيلها افتراضيا بسبب المخاوف الأمنية). لكن هذه الميزة ليست حالة استثنائية. (أي أنها ليست المثال الوحيد على ميزات تفتقر إلى الخصوصية). مثال آخر هو أن Microsoft قامت تلقائيا بتفعيل ميزة [النسخ الاحتياطي للمجلدات إلى OneDrive](https://neowin.net/news/windows-11-is-now-automatically-enabling-onedrive-folder-backup-without-asking-permission) في بعض تثبيتات Windows 11 الجديدة، دون طلب إذن من المستخدم.

يمكنك تعزيز خصوصيتك وأمانك على نظام Windows دون الحاجة إلى تحميل أي أدوات خارجية، وذلك من خلال الخطوات التالية:

- تهيئة Windows بعد التثبيت (سيتم توفيره قريبا)
- [Group Policy Settings](group-policies.md)
- إعدادات الخصوصية (قريبا)
- عزل التطبيقات "Application Sandboxing" (قريبا)
- تشديد إعدادات الأمان (سيتم توفيره قريبا)

<div class="admonition example" markdown>
<p class="admonition-title">هذا القسم جديد</p>

هذا القسم لا يزال قيد العمل، لأن جعل نظام Windows أكثر احتراما للخصوصية يتطلب وقتا وجهدا أكبر مقارنة بأنظمة التشغيل الأخرى.

</div>

## ملاحظات حول الخصوصية

نظام Microsoft Windows – وخاصة الإصدارات الموجهة للمستخدمين العاديين مثل نسخة Home – غالبا ما لا تعطي الأولوية لخيارات تحافظ على الخصوصية [بشكل افتراضي](https://theguardian.com/technology/2015/jul/31/windows-10-microsoft-faces-criticism-over-privacy-default-settings). ونتيجة لذلك، نشهد غالبا [جمعا للبيانات](https://en.wikipedia.org/wiki/Criticism_of_Microsoft#Telemetry_and_data_collection) أكثر مما هو ضروري، وذلك دون أي تنبيه واضح بأن هذا هو السلوك الافتراضي للنظام. في محاولة من مايكروسوفت لمنافسة Google في مجال الإعلانات،
قامت بإدخال ميزات في [Cortana](https://en.wikipedia.org/wiki/Cortana_(virtual_assistant) مثل الـ (Advertising ID)، وذلك بهدف تتبع الاستخدام ومساعدة المعلنين في تقديم إعلانات موجهة.  عند إطلاق Windows 10، لم يكن من الممكن إيقاف جمع البيانات التلقائي (Telemetry) في الإصدارات المخصصة للمستخدمين العاديين،
مثل نسخة Home وPro، بل كان ذلك متاحا فقط في الإصدارات الموجهة للشركات (Enterprise). وحتى الآن، لا يمكن إيقاف جمع البيانات بالكامل، لكن مايكروسوفت أضافت خيارا يسمح [بتقليل](https://extremetech.com/computing/243079-upcoming-windows-update-reduces-spying-microsoft-still-mum-data-collects) كمية البيانات التي يتم إرسالها إليها.

في نظام Windows 11، هناك عدد من القيود أو الإعدادات الافتراضية التي قد تؤثر على الخصوصية، مثل:

- إجبار المستخدم على استخدام حساب Microsoft بدلا من إنشاء Local account.
- جعل خيارات إنشاء Local account أكثر صعوبة في الإصدارات **Pro \*\* و**Enterprise\*\*من Windows، مما يوجه المستخدمين نحو استخدام حساب Microsoft.
- تفعيل جميع خيارات جمع البيانات بشكل افتراضي، مما يجبر المستخدم على إيقافها يدويا (opt out) إذا أراد حماية خصوصيته.
- دمج خدمات Microsoft مثل Bing وOneDrive وTeams بعمق داخل النظام،
  بطريقة يصعب إزالتها، وغالبا ما تُعرض للمستخدم على أنها الخيار الوحيد المتاح.
- يقوم Windows بتعيين Microsoft Edge كالمتصفح الأساسي تلقائيا،
  وحتى إذا غير المستخدم المتصفح الافتراضي (مثل Chrome أو Firefox)،
  قد يعيد النظام استخدام Edge من جديد بدون إذن أو تنبيه واضح.
- إضافة ميزات ذكاء اصطناعي تعتمد على الـ cloud إلى العديد من أجزاء نظام Windows وتطبيقات Microsoft المختلفة.
- تخزين بيانات حساسة دون حاجة حقيقية لذلك. حتى البيانات التي يتم تخزينها على جهازك فقط ولا تُرسل إلى Microsoft،
  تبقى معرضة للخطر إذا أصيب جهازك بفيروس أو برنامج تجسس.

كثيرا ما تستخدم Microsoft ميزة التحديثات التلقائية لإضافة وظائف (features) جديدة إلى جهازك، وأحيانا لإجراء تعديلات تجمع بياناتك وتكون مفعلة بشكل افتراضي دون تنبيه واضح. Some [privacy features](https://blogs.windows.com/windows-insider/2023/11/16/previewing-changes-in-windows-to-comply-with-the-digital-markets-act-in-the-european-economic-area) such as the option to _opt out_ of syncing an online Microsoft account with Windows, require you to select a country in the EEA (European Economic Area) during installation. It can be changed to your real country after Windows is installed.

## Windows Editions

Many critical privacy and security features are unfortunately locked away behind higher-cost editions of Windows, instead of being available in Windows **Home**. Some features missing from **Home** include BitLocker Drive Encryption, Hyper-V, and Windows Sandbox. In our Windows guides we will cover how to use all of these features appropriately, so having a premium edition of Windows will be necessary.

Windows **Enterprise** provides the most flexibility when it comes to configuring privacy and security settings built in to Windows. For example, they are the only editions that allow you to enable the highest level of restrictions on data sent to Microsoft via telemetry tools. Unfortunately, Enterprise is not available for retail purchase, so it may not be available to you.

The best version available for _retail_ purchase is Windows **Pro** as it has nearly all the features you'll want to use to secure your device, including BitLocker, Hyper-V, etc. The only thing missing is some of the most restrictive limitations on Microsoft's telemetry, unfortunately.

Students and teachers may be able to obtain a Windows **Education** (equivalent to Enterprise) or **Pro Education** license (equivalent to Pro) for free, including on personal devices, from their educational institution. Many schools partner with Microsoft via OnTheHub or Microsoft Azure for Education, so you can check those sites or your school's benefits page to see if you qualify. Whether or not you are able to get these licenses depends entirely on your institution. This may be the best way for many people to obtain an Enterprise-level edition of Windows for personal use. There are no additional privacy or security risks associated with using an Education license compared to the retail versions.

It is not recommended to use third party modified versions of Windows such as Windows AME. Since modified versions of Windows like Windows AME don't receive updates, security features and antivirus definitions in Windows Defender will fall behind the current threat landscape, opening you up to attacks, thus making you even less secure.

## Obtaining Windows

Currently, only Windows 11 license keys are available for purchase, but these keys will work on Windows 10 as well, so you can still purchase a Windows 11 Pro key to activate a Windows 10 install.

The official [Media Creation Tool](https://microsoft.com/software-download/windows11) is the best way to put a Windows installer on a USB flash drive. Third-party tools like Rufus or Etcher may unexpectedly modify the files, which could lead to boot issues or other troubles when installing.

This tool only lets you install a **Home** or **Pro** installation, as there are no publicly available downloads for Windows **Enterprise** edition. If you have an **Enterprise** license key, you can easily upgrade a **Pro** installation. To do this, install Windows **Pro** without entering a license key during setup, then enter your **Enterprise** key in the Settings app after completing the installation. Your **Pro** install will be upgraded to **Enterprise** automatically after entering a valid license key.

If you are installing an **Education** license then you will typically have a private download link that will be provided alongside your license key when you obtain it from your institution's benefits portal.
