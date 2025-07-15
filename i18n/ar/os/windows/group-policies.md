---
title: إعدادات الـ Group Policy
description: دليل سريع لتهيئة إعدادات Group Policy لجعل Windows أكثر احتراما لخصوصيتك.
---

بعيدا عن تعديل الـ Registry نفسه، يُعد الـ **Local Group Policy Editor** أقوى وسيلة مضمنة لتغيير العديد من جوانب نظامك دون تثبيت أي أدوات طرف ثالث (third-party tools). يتطلب تغيير هذه الإعدادات نسخة [Pro Edition](index.md#windows-editions) أو إصدار أعلى.

يُستحسن ضبط هذه الإعدادات على نسخة (installation) جديدة تماما لنظام  Windows. يمكن تطبيق هذه الإعدادات على نسخة Windows الحالية، ولكن قد ينتج عن ذلك سلوك غير متوقع، ويتم ذلك على مسؤوليتك الخاصة.

يوجد مع كل إعداد في group policy editor شرح مُرفق يوضح بدقة وظيفته، وعادة ما يكون هذا الشرح تفصيليا. يرجى الانتباه إلى الشروحات المرفقة أثناء إجراء التغييرات، حتى تعرف بالضبط ما نوصي به هنا. لقد شرحنا أيضا بعض اختياراتنا أدناه عندما يكون الشرح المُرفق مع Windows غير كاف.

## Administrative Templates

يمكنك العثور على هذه الإعدادات بفتح gpedit.msc والانتقال إلى **Local Computer Policy** > **Computer Configuration** > **Administrative Templates** في الشريط الجانبي الأيسر (the left sidebar). العناوين في هذه الصفحة تمثل الـ الـ folders و subfolders ضمن الـ Administrative Templates، بينما تمثل الـ  bullet points السياسات الفردية (السياسات الفردية هنا تعني كل “Policy” مستقلة ضمن الـ Administrative Templates، يمكنك ضبطها "تمكينها أو تعطيلها أو تعديل إعداداتها" بشكل منفرد.).

لتغيير أي إعداد في Group Policy، انقر عليه نقرا مزدوجا واختر Enabled أو Disabled من أعلى النافذة التي تظهر، وذلك حسب التوصيات أدناه. قد تحتوي بعض سياسات الـ Group Policy على إعدادات إضافية قابلة للتعديل، وإذا توافرت مثل هذه الإعدادات فسنوضح أدناه الخيارات الملائمة التي نوصي بها.

### نظام

#### Device Guard

- يجب ضبط إعداد “Turn On Virtualization Based Security” على **Enabled**
    - اضبط خيار Platform Security Level على **Secure Boot and DMA Protection**
    - اضبط إعداد Secure Launch Configuration على **Enabled**

#### Internet Communication Management

- اضبط إعداد Turn off Windows Customer Experience Improvement Program على **Enabled**
- اضبط إعداد Turn off Windows Error Reporting على **Enabled**
- اضبط إعداد Turn off the Windows Messenger Customer Experience Improvement Program على **Enabled**

يرجى ملاحظة أن تعطيل Windows Customer Experience Improvement Program يؤدي أيضا إلى تعطيل بعض ميزات التتبع الأخرى، والتي يمكن التحكم بها بشكل منفصل من خلال Group Policy أيضا. لا نحتاج إلى ذكر أو تعطيل كل ميزة تتبع بشكل منفصل، لأن تعطيل Windows Customer Experience Improvement Program يؤدي تلقائيا إلى إيقاف هذه الميزات.

#### OS Policies

- اضبط إعداد Allow Clipboard History على **Disabled**
- اضبط إعداد Allow Clipboard synchronization across devices على **Disabled**
- اضبط إعداد Enables Activity Feed على **Disabled**
- اضبط إعداد Allow publishing of User Activities على **Disabled**
- اضبط إعداد Allow upload of User Activities على **Disabled**

#### User Profiles

- اضبط إعداد Turn off the advertising ID على **Enabled**

### Windows Components

#### AutoPlay Policies

تُعد AutoRun و AutoPlay ميزتان في Windows تقومان بتشغيل شيء تلقائيا (مثل برنامج أو ملف) عند توصيل جهاز خارجي مثل فلاشة USB.المشكلة أن هذا التشغيل التلقائي قد يتجاوز بعض خطوات الأمان، لأنه لا يطلب إذن المستخدم أولًا. لذلك يُفضل إيقاف هذه الميزات لتعزيز الخصوصية والحماية. قد يسمح ذلك للأجهزة غير الموثوقة بتشغيل تعليمات خبيثة (malicious code) دون علمك. لأجل حماية جهازك، يُنصح بأن توقف ميزتي AutoRun وAutoPlay،
وأن تقوم أنت بنفسك بفتح الملفات من الفلاشة أو القرص الخارجي، بدل أن يفتحها Windows تلقائيا دون إذنك.

- اضبط إعداد Turn off AutoPlay على **Enabled**
- اضبط إعداد Disallow Autoplay for nonvolume devices على **Enabled**
- اضبط إعداد Set the default behavior for AutoRun على **Enabled**
    - اضبط خيار Default AutoRun Behavior على **Do not execute any AutoRun commands**

#### BitLocker Drive Encryption

قد ترغب في إعادة تشفير الـ operating system drive بعد تغيير هذه الإعدادات.

- اضبط إعداد Choose drive encryption method and cipher strength (Windows Vista, Windows Server 2008, Windows 7) على **Enabled**
    - اضبط خيار Select the encryption method على **AES-256**

تحديدك لـ Aes-256 في سياسة Windows 7 سيجعل النظام يستخدم Aes-256 حتى في النسخ الأحدث.

##### Operating System Drives

- اضبط إعداد Require additional authentication at startup على **Enabled**
- اضبط إعداد Allow enhanced PINs for startup على **Enabled**

هذه السياسات لا **تجبرك** على استخدام PIN أو إعدادات معينة.
لكن لما تفعلها، يظهر لك **خيار**جديد أثناء إعداد BitLocker يسمح لك باختيار حماية إضافية، مثل إنك تطلب PIN عند تشغيل الجهاز، مع الاعتماد على TPM.

#### Cloud Content

- Turn off cloud optimized content: **Enabled**
- Turn off cloud consumer account state content: **Enabled**
- Do not show Windows tips: **Enabled**
- Turn off Microsoft consumer experiences: **Enabled**

#### Credential User Interface

- Require trusted path for credential entry: **Enabled**
- Prevent the use of security questions for local accounts: **Enabled**

#### Data Collection and Preview Builds

- Allow Diagnostic Data: **Enabled**
    - Options: **Send required diagnostic data** (Pro Edition); or
    - Options: **Diagnostic data off** (Enterprise or Education Edition)
- Limit Diagnostic Log Collection: **Enabled**
- Limit Dump Collection: **Enabled**
- Limit optional diagnostic data for Desktop Analytics: **Enabled**
    - Options: **Disable Desktop Analytics collection**
- Do not show feedback notifications: **Enabled**

#### File Explorer

- Turn off account-based insights, recent, favorite, and recommended files in File Explorer: **Enabled**

#### MDM

- Disable MDM Enrollment: **Enabled**

#### OneDrive

- Save documents to OneDrive by default: **Disabled**
- Prevent OneDrive from generating network traffic until the user signs in to OneDrive: **Enabled**
- Prevent the usage of OneDrive for file storage: **Enabled**

This last setting disables OneDrive on your system; make sure to change it to **Disabled** if you use OneDrive.

#### Push To Install

- Turn off Push To Install service: **Enabled**

#### بحث

- Allow Cortana: **Disabled**
- Don't search the web or display web results in Search: **Enabled**
- Set what information is shared in Search: **Enabled**
    - Type of information: **Anonymous info**

#### Sync your settings

- Do not sync: **Enabled**

#### Text input

- Improve inking and typing recognition: **Disabled**

#### Windows Error Reporting

- Do not send additional data: **Enabled**
- Consent > Configure Default consent: **Enabled**
    - Consent level: **Always ask before sending data**
