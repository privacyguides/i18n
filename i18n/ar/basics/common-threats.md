---
title: "التهديدات الشائعة"
icon: 'material/eye-outline'
description: نموذج تهديداتك يخصّك شخصيًا، ولكن هذه بعض الأشياء التي تُهم الكثير من زوار هذا الموقع.
---

بوجهٍ عام، إننا نصنف توصياتنا إلى [التهديدات](threat-modeling.md) أو الأهداف المنطبقة على معظم الناس. ==قد تولي اهتمامًا بواحدٍ من تلك الاحتمالات، أو بالقليل منها، أو بجميعها، أو قد لا تولي اهتمامًا بأيٍّ منها مطلقًا==، وتتوقف الأدوات والخدمات التي تستخدمها على أهدافك. قد تكون لديك تهديدات محددة خارج هذه الفئات كذلك، ولا بأس بهذا قَط! الجزء الهامّ هو التوصل إلى فهم للفوائد وأوجه القصور في الأدوات التي تختار استخدامها، ﻷنَّه لن تحميك أيٌّ منها تقريبًا من كلّ تهديد موجود.

<span class="pg-purple">:material-incognito: **إخفاء الهُوية**</span>
:

حجب نشاطك على الإنترنت عن هُويتك الحقيقية، حاميًا إياك من الأشخاص الذين يحاولون الكشف عن هُويتك *أنت* بالتحديد.

<span class="pg-red">:material-target-account: **الهجمات المستهدفة**</span>
:

الحماية من المخترقين أو العناصر الخبيثة الأخرى مِمَّن يحاولون الوصول إلى بياناتك أو أجهزتك *أنت* بالتحديد.

<span class="pg-viridian">:material-package-variant-closed-remove: **هجمات سلاسل الإمداد**</span>
:

عادةً ما يكون شكلًا من أشكال <span class="pg-red">:material-target-account: الهجمات المستهدفة</span> المتمحورة حول ثغرة أمنية أو ثغرة مستغلّة تقدّم إلى برمجيات سليمة إمّا مباشرةً أو من خلال تبعيّة برمجية من طرف ثالث.

<span class="pg-orange">:material-bug-outline: **الهجمات السلبية**</span>
:

الحماية من أشياء مثل البرمجيات الخبيثة، واختراقات البيانات، وهجمات أخرى تُشن ضد العديد من الأشخاص في آنٍ واحد.

<span class="pg-teal">:material-server-network: **مزوِّدو الخِدمات**</span>
:

حماية بياناتك من مزوِّدي الخِدمات (على سبيل المثال، باستخدام التشفير بين الطرفين، الذي يجعل بياناتك غير قابلة للقراءة من قِبَل الخادم).

<span class="pg-blue">:material-eye-outline: **المراقبة الجماعيّة**</span>
:

الحماية من وكالات الحكومة، ومؤسساتها، ومواقعها الإلكترونية، وخدماتها التي تعمل معًا لتعقّب أنشطتك.

<span class="pg-brown">:material-account-cash: **رأسمالية المراقبة**</span>
:

حماية نفسك من شبكات الإعلانات الكبيرة مثل Google وFacebook، وكذلك من عدد كبير من الجهات الخارجية التي تجمع البيانات.

<span class="pg-green">:material-account-search: **الظهور العلني**</span>
:

تقليل المعلومات المتاحة عنك على الإنترنت لمحركات البحث أو للعامة.

<span class="pg-blue-gray">:material-close-outline: **الرقابة**</span>
:

تجنب حجب الوصول إلى المعلومات أو التعرض للرقابة عند التعبير عن رأيك على الإنترنت.

قد تكون بعض هذه التهديدات أهم بالنسبة لك من غيرها، حسب مخاوفك واحتياجاتك الخاصة. على سبيل المثال، قد يكون مطور برمجيات لديه وصول إلى بيانات قيمة أو حساسة مهتما بشكل أساسي بـ <span class="pg-viridian">:material-package-variant-closed-remove: هجمات سلسلة التوريد (Supply Chain Attacks)</span> و<span class="pg-red">:material-target-account: الهجمات المستهدفة (Targeted Attacks)</span>. ومن المرجح أنهم سيظلون يرغبون في حماية بياناتهم الشخصية من أن تُجمع ضمن برامج <span class="pg-blue">:material-eye-outline: المراقبة الجماعية (Mass Surveillance)</span>. وبالمثل، قد يكون اهتمام كثير من الناس الأساسي هو <span class="pg-green">:material-account-search: الظهور العلني (Public Exposure)</span> لبياناتهم الشخصية، لكن ينبغي لهم أيضا الحذر من المشكلات المتعلقة بالأمان، مثل <span class="pg-orange">:material-bug-outline: الهجمات السلبية (Passive Attacks)</span>، كإصابة أجهزتهم ببرمجيات ضارة.

## إخفاء الهوية مقابل الخصوصية

<span class="pg-purple">:material-incognito: إخفاء الهوية</span>

غالبا ما يتم الخلط بين إخفاء الهوية والخصوصية، لكنهما مفهومان مختلفان. بينما تعني الخصوصية مجموعة الخيارات التي تتخذها بشأن كيفية استخدام بياناتك ومشاركتها، فإن إخفاء الهوية يعني فصل أنشطتك على الإنترنت تماما عن هويتك الحقيقية.

على سبيل المثال، قد يكون لدى المبلغين عن المخالفات والصحفيين نموذج تهديد (Threat Model) أكثر صرامة بكثير، ويتطلب إخفاء الهوية بشكل كامل. ولا يقتصر الأمر على إخفاء ما يفعلونه والبيانات التي لديهم، أو تجنب اختراقهم من جهات خبيثة أو حكومات، بل يشمل أيضا إخفاء هويتهم بالكامل. وغالبا ما يضحون بأي قدر من الراحة إذا كان ذلك يساعد على حماية إخفاء هويتهم أو خصوصيتهم أو أمانهم، لأن حياتهم قد تعتمد على ذلك. معظم الناس لا يحتاجون إلى الذهاب إلى هذا الحد.

## الأمان والخصوصية

<span class="pg-orange">:material-bug-outline: الهجمات السلبية</span>

غالبا ما يتم الخلط أيضا بين الأمان والخصوصية، لأنك تحتاج إلى الأمان للحصول على أي قدر من الخصوصية: فاستخدام الأدوات، حتى لو كانت مصممة لحماية الخصوصية، لا فائدة منه إذا كان بإمكان المهاجمين استغلال ثغراتها بسهولة ثم نشر بياناتك. قد تكون الخدمة آمنة جدا من الاختراق والهجمات، لكنها في الوقت نفسه *لا تحترم* خصوصيتك. أفضل مثال على ذلك هو الوثوق ببياناتك لدى Google، التي شهدت عددا قليلا من الحوادث الأمنية مقارنة بحجمها، بفضل توظيف خبراء أمان من الأفضل في المجال لحماية بنيتها التحتية. رغم أن خدمات Google آمنة جدا من ناحية الحماية، فإن كثيرا من الناس لا يعتقدون أن Google تحافظ على خصوصية بياناتهم عند استخدام خدماتها المجانية مثل Gmail وYouTube

عندما يتعلق الأمر بأمان التطبيقات، فنحن عادة لا نعرف — وأحيانا لا يمكننا أن نعرف — ما إذا كان البرنامج الذي نستخدمه ضارا، أو قد يصبح ضارا يوما ما. حتى مع أكثر المطورين موثوقية، لا يوجد عادة ما يضمن أن برامجهم خالية من ثغرة خطيرة قد يتم استغلالها لاحقا.

لتقليل الضرر الذي *قد* يسببه برنامج ضار، ينبغي استخدام أسلوب الأمان عبر العزل (ecurity by compartmentalization). على سبيل المثال، يمكن تطبيق ذلك باستخدام أجهزة كمبيوتر مختلفة لمهام مختلفة، أو استخدام أجهزة افتراضية لفصل مجموعات التطبيقات المرتبطة ببعضها، أو استخدام نظام تشغيل آمن يركز بشكل كبير على الـ sandboxing للتطبيقات والـ Mandatory Access Control.

<div class="admonition tip" markdown>
<p class="admonition-title">نصيحة</p>

توفر أنظمة تشغيل الهواتف عادة الـ sandboxing أفضل للتطبيقات مقارنة بأنظمة تشغيل الكمبيوتر: فلا يمكن للتطبيقات الحصول على صلاحيات الـ root، وتحتاج إلى إذن للوصول إلى موارد النظام.

أنظمة تشغيل الكمبيوتر عادة أضعف من ناحية الـ sandboxing المناسب. يتمتع ChromeOS بإمكانات الـ sandboxing مشابهة لـ Android، بينما يوفر macOS تحكما كاملًا في أذونات النظام (ويمكن للمطورين اختيار استخدام الـ sandboxing لتطبيقاتهم). لكن هذه الأنظمة ترسل معلومات يمكن استخدامها للتعرف عليك إلى الشركات المصنعة لأجهزتها. يميل Linux إلى عدم إرسال معلومات إلى مزودي النظام (system vendors)، لكنه يوفر حماية ضعيفة ضد استغلال الثغرات والتطبيقات الضارة. يمكن تقليل هذه المخاطر إلى حدٍ ما باستخدام توزيعات متخصصة تعتمد بشكل كبير على الأجهزة الافتراضية (virtual machines) أو الحاويات (containers)، مثل [Qubes OS](../desktop.md#qubes-os).

</div>

## هجمات تستهدف أفرادا محددين

<span class="pg-red">:material-target-account: الهجمات المستهدفة</span>

يصعب التعامل مع الهجمات التي تستهدف شخصا محددا بشكل أكبر. تشمل الهجمات الشائعة إرسال مستندات ضارة عبر البريد الإلكتروني، واستغلال الثغرات (مثل الثغرات الموجودة في المتصفحات وأنظمة التشغيل) والهجمات التي تتطلب وصولًا فعليا إلى الجهاز. إذا كان هذا الأمر يشكل مصدر قلق لك، فينبغي استخدام استراتيجيات أكثر تقدما للحد من التهديدات.

<div class="admonition tip" markdown>
<p class="admonition-title">نصيحة</p>

بحكم تصميمها، تقوم **متصفحات الويب** و**برامج البريد الإلكتروني** و**التطبيقات المكتبية (office applications)** عادةً بتشغيل تعليمات برمجية غير موثوقة تُرسل إليك من جهات خارجية. تشغيل عدة أجهزة افتراضية (virtual machines)—لفصل تطبيقات كهذه عن نظامك المضيف وعن بعضها البعض—هو أحد الأساليب التي يمكنك استخدامها لتقليل احتمال أن يؤدي استغلال ثغرة في هذه التطبيقات إلى اختراق بقية نظامك. على سبيل المثال، توفر تقنيات مثل Qubes OS أو Microsoft Defender Application Guard على Windows طرقًا سهلة لتنفيذ ذلك.

</div>

إذا كنت قلقا بشأن **الهجمات التي تتطلب وصولا فعليا إلى الجهاز**، فينبغي استخدام نظام تشغيل يدعم إقلاعا آمنا ومتحققًا منه ((secure verified boot))، مثل Android أو iOS أو macOS أو [Windows (مع TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). كما ينبغي التأكد من أن محرك الأقراص (drive) لديك مُشفر، وأن نظام التشغيل يستخدم TPM أو Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) أو [Element](https://developers.google.com/android/security/android-ready-se) للحد من عدد محاولات إدخال الـ encryption passphrase. يجب تجنب مشاركة جهاز الكمبيوتر مع أشخاص لا تثق بهم، لأن معظم أنظمة تشغيل سطح المكتب (desktop operating systems) لا تشفّر بيانات كل مستخدم بشكل منفصل.

## هجمات تستهدف مؤسسات معيّنة

<span class="pg-viridian">:material-package-variant-closed-remove: هجمات سلسلة التوريد (Supply Chain Attacks)</span>

تكون هجمات سلسلة التوريد (Supply Chain Attacks) غالبا نوعا من <span class="pg-red">:material-target-account: الهجمات المستهدفة (Targeted Attack)</span> ضد الشركات والحكومات والناشطين، لكنها قد تؤدي أيضا إلى اختراق عامة الناس.

<div class="admonition example" markdown>
<p class="admonition-title">مثال</p>

حدث مثال بارز على ذلك في عام 2017، عندما أُصيب برنامج المحاسبة الشهير M.E.Doc في أوكرانيا بفيروس NotPetya، مما أدى لاحقًا إلى إصابة الأشخاص الذين نزّلوا ذلك البرنامج ببرمجية فدية. كان NotPetya نفسه هجوما ببرمجية فدية أثّر على أكثر من 2000 شركة في دول مختلفة، واعتمد على ثغرة EternalBlue التي طورتها NSA لمهاجمة أجهزة Windows عبر الشبكة.

</div>

هناك عدة طرق يمكن من خلالها تنفيذ هذا النوع من الهجمات:

1. قد يعمل أحد المساهمين أو الموظفين أولا على الوصول إلى منصب ذي صلاحيات داخل مشروع أو مؤسسة، ثم يسيء استخدام هذا المنصب بإضافة تعليمات برمجية ضارة.
2. قد تُجبر جهة خارجية أحد المطورين على إضافة تعليمات برمجية ضارة.
3. An individual or group might identify a third party software dependency (also known as a library) and work to infiltrate it with the above two methods, knowing that it will be used by "downstream" software developers.

These sorts of attacks can require a lot of time and preparation to perform and are risky because they can be detected, particularly in open source projects if they are popular and have outside interest. Unfortunately they're also one of the most dangerous as they are very hard to mitigate entirely. We would encourage readers to only use software which has a good reputation and makes an effort to reduce risk by:

1. Only adopting popular software that has been around for a while. The more interest in a project, the greater likelihood that external parties will notice malicious changes. A malicious actor will also need to spend more time gaining community trust with meaningful contributions.
2. Finding software which releases binaries with widely-used, trusted build infrastructure platforms, as opposed to developer workstations or self-hosted servers. Some systems like GitHub Actions let you inspect the build script that runs publicly for extra confidence. This lessens the likelihood that malware on a developer's machine could infect their packages, and gives confidence that the binaries produced are in fact produced correctly.
3. Looking for code signing on individual source code commits and releases, which creates an auditable trail of who did what. For example: Was the malicious code in the software repository? Which developer added it? Was it added during the build process?
4. Checking whether the source code has meaningful commit messages (such as [conventional commits](https://conventionalcommits.org)) which explain what each change is supposed to accomplish. Clear messages can make it easier for outsiders to the project to verify, audit, and find bugs.
5. Noting the number of contributors or maintainers a program has. A lone developer may be more susceptible to being coerced into adding malicious code by an external party, or to negligently enabling undesirable behavior. This may very well mean software developed by "Big Tech" has more scrutiny than a lone developer who doesn't answer to anyone.

## Privacy from Service Providers

<span class="pg-teal">:material-server-network: Service Providers</span>

We live in a world where almost everything is connected to the internet. Our "private" messages, emails, and social interactions are typically stored on a server, somewhere. Generally, when you send someone a message it's stored on a server, and when your friend wants to read the message the server will show it to them.

The obvious problem with this is that the service provider (or a hacker who has compromised the server) can access your conversations whenever and however they want, without you ever knowing. This applies to many common services, like SMS messaging, Telegram, and Discord.

Thankfully, E2EE can alleviate this issue by encrypting communications between you and your desired recipients before they are even sent to the server. The confidentiality of your messages is guaranteed, assuming the service provider doesn't have access to the private keys of either party.

<div class="admonition note" markdown>
<p class="admonition-title">Note on Web-based Encryption</p>

In practice, the effectiveness of different E2EE implementations varies. Applications, such as [Signal](../real-time-communication.md#signal), run natively on your device, and every copy of the application is the same across different installations. If the service provider were to introduce a [backdoor](https://en.wikipedia.org/wiki/Backdoor_(computing)) in their application—in an attempt to steal your private keys—it could later be detected with [reverse engineering](https://en.wikipedia.org/wiki/Reverse_engineering).

On the other hand, web-based E2EE implementations, such as Proton Mail's web app or Bitwarden's *Web Vault*, rely on the server dynamically serving JavaScript code to the browser to handle cryptography. A malicious server can target you and send you malicious JavaScript code to steal your encryption key (and it would be extremely hard to notice). Because the server can choose to serve different web clients to different people—even if you noticed the attack—it would be incredibly hard to prove the provider's guilt.

Therefore, you should use native applications over web clients whenever possible.

</div>

Even with E2EE, service providers can still profile you based on **metadata**, which typically isn't protected. While the service provider can't read your messages, they can still observe important things, such as whom you're talking to, how often you message them, and when you're typically active. Protection of metadata is fairly uncommon, and—if it's within your [threat model](threat-modeling.md)—you should pay close attention to the technical documentation of the software you're using to see if there's any metadata minimization or protection at all.

## Mass Surveillance Programs

<span class="pg-blue">:material-eye-outline: Mass Surveillance</span>

Mass surveillance is the intricate effort to monitor the "behavior, many activities, or information" of an entire (or substantial fraction of a) population.[^1] It often refers to government programs, such as the ones [disclosed by Edward Snowden in 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). However, it can also be carried out by corporations, either on behalf of government agencies or by their own initiative.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

إذا كنت تريد معرفة المزيد عن أساليب المراقبة وكيفية استخدامها في مدينتك، يمكنك أيضا الاطلاع على [Atlas of Surveillance](https://atlasofsurveillance.org) من [Electronic Frontier Foundation](https://eff.org).

في فرنسا، يمكنك الاطلاع على موقع [Technopolice](https://technopolice.fr/villes) الذي تديره الجمعية غير الربحية La Quadrature du Net.

</div>

غالبا ما تبرر الحكومات برامج المراقبة الجماعية بأنها ضرورية لمكافحة الإرهاب ومنع الجريمة. لكن هذه البرامج، بما تنطوي عليه من انتهاكات لحقوق الإنسان، تُستخدم غالبا لاستهداف الأقليات والمعارضين السياسيين بشكل غير متناسب، إلى جانب فئات أخرى.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">درس الخصوصية من أحداث 11 سبتمبر: المراقبة الجماعية ليست الطريق الصحيح للمضي قدما</a></em></p>

في أعقاب كشف إدوارد سنودن عن برامج حكومية مثل [PRISM](https://en.wikipedia.org/wiki/PRISM) و[Upstream](https://en.wikipedia.org/wiki/Upstream_collection)، أقر مسؤولو الاستخبارات أيضا بأن NSA كانت تجمع سرا ولسنوات سجلات تتعلق بمكالمات كل أمريكي تقريبا — من يتصل بمن، ومتى تُجرى هذه المكالمات، ومدة استمرارها. عندما تجمع NSA هذا النوع من المعلومات يوما بعد يوم، فقد يكشف تفاصيل شديدة الحساسية عن حياة الأشخاص وعلاقاتهم، مثل ما إذا كانوا قد اتصلوا بقس، أو بجهة تقدم خدمات الإجهاض، أو بمستشار لعلاج الإدمان، أو بخط مساعدة للوقاية من الانتحار.

</div>

رغم تزايد المراقبة الجماعية في الولايات المتحدة، وجدت الحكومة أن برامج المراقبة الجماعية مثل Section 215 كانت ذات «قيمة إضافية محدودة جدا» في منع الجرائم الفعلية أو المخططات الإرهابية، إذ كانت هذه الجهود تكرّر إلى حد كبير برامج المراقبة المستهدفة الخاصة بـ FBI.[^2]

على الإنترنت، يمكن تتبّعك بطرق مختلفة، منها على سبيل المثال لا الحصر:

- عنوان IP الخاص بك
- ملفات تعريف الارتباط في المتصفح (Cookies)
- البيانات التي ترسلها إلى مواقع الويب
- بصمة متصفحك أو جهازك
- ربط طرق الدفع ببعضها

إذا كنت قلقا بشأن برامج المراقبة الجماعية، فيمكنك استخدام أساليب مثل فصل هوياتك على الإنترنت عن بعضها، والاندماج بين المستخدمين الآخرين، أو ببساطة تجنب تقديم معلومات تكشف هويتك كلما أمكن.

## المراقبة كوسيلة لتحقيق الأرباح

<span class="pg-brown">:material-account-cash: رأسمالية المراقبة</span>

> رأسمالية المراقبة هي نظام اقتصادي يقوم على جمع البيانات الشخصية وتحويلها إلى سلعة، بهدف أساسي هو تحقيق الأرباح.[^3]

بالنسبة لكثير من الناس، أصبح التتبع والمراقبة من قِبل الشركات الخاصة مصدر قلق متزايد. تمتد شبكات الإعلانات واسعة الانتشار، مثل تلك التي تديرها Google وFacebook، عبر الإنترنت إلى ما هو أبعد بكثير من المواقع التي تسيطر عليها، وتتابع نشاطك أثناء تنقلك بين المواقع. استخدام أدوات مثل أدوات حظر المحتوى (content blockers) للحد من طلبات الشبكة المرسلة إلى خوادمهم، وقراءة سياسات الخصوصية للخدمات التي تستخدمها، يمكن أن يساعدك على تجنب العديد من الجهات التي تحاول تتبعك بطرق بسيطة (لكن لا يمكنه منع التتبّع بالكامل).[^4]

بالإضافة إلى ذلك، حتى الشركات التي لا تعمل في مجال *AdTech* أو التتبع يمكنها مشاركة معلوماتك مع [وسطاء البيانات](https://en.wikipedia.org/wiki/Information_broker) (مثل Cambridge Analytica أو Experian أو Datalogix) أو مع جهات أخرى. لا يمكنك افتراض أن بياناتك آمنة لمجرد أن الخدمة التي تستخدمها لا تعتمد نموذج أعمال AdTech أو التتبع المعتاد. أقوى وسيلة للحماية من جمع الشركات لبياناتك هي تشفير بياناتك أو إخفاء معالمها كلما أمكن، بحيث يصعب على الجهات المختلفة ربط هذه البيانات ببعضها وبناء ملف شخصي عنك.

## الحد من المعلومات المتاحة للعامة

<span class="pg-green">:material-account-search: الظهور العلني</span>

أفضل طريقة للحفاظ على خصوصية بياناتك هي ببساطة عدم نشرها للعامة من الأساس. حذف المعلومات غير المرغوب فيها التي تجدها عن نفسك على الإنترنت هو من أفضل الخطوات الأولى التي يمكنك اتخاذها لاستعادة خصوصيتك.

- [اطلع على دليلنا لحذف الحسابات :material-arrow-right-drop-circle:](account-deletion.md)

في المواقع التي تشارك فيها معلوماتك، من المهم جدا مراجعة إعدادات الخصوصية في حسابك للحد من مدى انتشار هذه البيانات. على سبيل المثال، فعل "private mode" في حساباتك إذا كان هذا الخيار متاحا: يضمن ذلك عدم فهرسة حسابك بواسطة محركات البحث، وعدم إمكانية الاطلاع عليه دون إذنك.

إذا كنت قد قدمت بالفعل معلوماتك الحقيقية إلى مواقع لا ينبغي أن تمتلكها، ففكر في استخدام أساليب التضليل، مثل تقديم معلومات وهمية مرتبطة بتلك الهوية على الإنترنت. هذا يجعل من الصعب التمييز بين معلوماتك الحقيقية والمعلومات الزائفة.

## تجنب الرقابة

<span class="pg-blue-gray">:material-close-outline: الرقابة</span>

يمكن فرض الرقابة على الإنترنت بدرجات متفاوتة من قِبل جهات تشمل الحكومات الشمولية، ومسؤولي الشبكات، ومقدمي الخدمات. تتعارض محاولات التحكم في التواصل ومنع الوصول إلى المعلومات مع حق الإنسان في حرية التعبير.[^5]

أصبحت الرقابة على منصات الشركات أكثر شيوعا، إذ تستجيب منصات مثل X (تويتر سابقًا) وFacebook لضغوط الرأي العام والسوق والجهات الحكومية. يمكن أن تكون ضغوط الحكومات على الشركات سرية، مثل [طلب البيت الأبيض إزالة](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) مقطع فيديو مثير للجدل من YouTube، أو علنية، مثل مطالبة الحكومة الصينية الشركات بالالتزام بنظام رقابة صارم.

يمكن للأشخاص القلقين من خطر الرقابة استخدام تقنيات مثل [Tor](../advanced/tor-overview.md) لتجاوزها، ودعم منصات تواصل مقاومة للرقابة مثل [Matrix](../social-networks.md#element)، التي لا توجد فيها جهة مركزية تتحكم بالحسابات ويمكنها إغلاقها بشكل تعسفي.

<div class="admonition tip" markdown>
<p class="admonition-title">نصيحة</p>

بينما قد يكون تجاوز الرقابة نفسها أمرا سهلا، فإن إخفاء حقيقة أنك تفعل ذلك قد يكون صعبا جدا.

يجب أن تفكر في ما يستطيع خصمك مراقبته من نشاطك على الشبكة، وما إذا كان بإمكانك إنكار قيامك بهذه الأفعال بشكل مقنع. على سبيل المثال، يمكن أن يساعدك استخدام [DNS المشفر](../advanced/dns-overview.md#what-is-encrypted-dns) في تجاوز أنظمة الرقابة البسيطة المعتمدة على الـ DNS، لكنه لا يستطيع إخفاء المواقع التي تزورها فعليا عن مزود خدمة الإنترنت (ISP). يمكن أن يساعد VPN أو Tor في إخفاء المواقع التي تزورها عن مسؤولي الشبكة، لكنهما لا يستطيعان إخفاء حقيقة أنك تستخدم VPN أو Tor من الأساس. يمكن أن تساعدك الـ Pluggable Transports (مثل Obfs4proxy أو Meek أو Shadowsocks) في تجاوز جدران الحماية (firewalls) التي تحظر بروتوكولات الـ VPN الشائعة أو Tor، لكن قد تظل محاولاتك لتجاوز الرقابة قابلة للاكتشاف باستخدام أساليب مثل probing أو [الفحص العميق للحزم (deep packet inspection)](https://en.wikipedia.org/wiki/Deep_packet_inspection).

</div>

يجب أن تضع دائما في اعتبارك مخاطر محاولة تجاوز الرقابة، والعواقب المحتملة، ومدى تطور قدرات خصمك. يجب أن تكون حذرا عند اختيار البرامج التي تستخدمها، وأن تكون لديك خطة بديلة في حال تم اكتشافك.

[^1]: Wikipedia: [*المراقبة الجماعية*](https://en.wikipedia.org/wiki/Mass_surveillance) و[*المراقبة*](https://en.wikipedia.org/wiki/Surveillance). [↩](#fnref:1){.footnote-backref}
[^2]: United States Privacy and Civil Liberties Oversight Board: [*Report on the Telephone Records Program Conducted under Section 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[حصر الأشياء الضارة (Enumerating badness)](https://ranum.com/security/computer_security/editorials/dumb)" (أي "إعداد قائمة بكل الأشياء الضارة التي نعرفها")، كما تفعل العديد من أدوات حظر المحتوى وبرامج مكافحة الفيروسات، لا يحميك بشكل كاف من التهديدات الجديدة وغير المعروفة، لأنها لم تُضف بعد إلى قائمة التصفية. يجب أيضًا استخدام أساليب أخرى للحد من المخاطر.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
