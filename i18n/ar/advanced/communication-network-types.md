---
title: "أنواع شبكات الاتصال"
icon: 'material/transit-connection-variant'
description: استعراض سريع لعدد من تصميمات الشبكات التي تعتمد عليها غالبا تطبيقات المراسلة الفورية.
---

هناك اكثر من طريقة معروفة لبناء الشبكات بهدف توصيل الرسائل بين المستخدمين. هذه الشبكات قد توفر درجات مختلفة من الخصوصية، لذلك من المهم ان تفكر في [نموذج التهديد (Threat Model)](../basics/threat-modeling.md) الخاص بك عند اختيار التطبيق الذي ستستخدمه.

[تطبيقات المراسلة الفورية (Instant Messengers) الموصى بها](../real-time-communication.md ""){.md-button} [:material-movie-open-play-outline: فيديو: حان الوقت للتوقف عن استخدام SMS، وهذه هي الاسباب](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## شبكات بخادم واحد مركزي

![رسم توضيحي للشبكات المركزية](../assets/img/layout/network-centralized.svg){ align=left }

تطبيقات المراسلة المركزية (Centralized messengers) هي التي يكون فيها كل المستخدمين على نفس الخادم، او على شبكة خوادم تديرها وتتحكم بها جهة واحدة (شركة او منظمة).

بعض تطبيقات المراسلة ذات الاستضافة الذاتية (self-hosted) تتيح لك تشغيل خادمك الخاص. الاستضافة الذاتية (Self-hosting) قد تمنحك مزيدا من ضمانات الخصوصية، مثل عدم وجود سجلات استخدام (no logs)، او تقليل الوصول الى البيانات الوصفية (metadata) (مثل معلومات عن من يتواصل مع من). في هذا النوع من تطبيقات المراسلة، الاستضافة الذاتية تعني ان الشبكة تكون منفصلة، ويجب ان ينضم كل الاطراف الى نفس الخادم لكي يتحدثوا.

**ما الذي يميزها:**

- من السهل طرح ميزات جديدة واجراء تعديلات بشكل اسرع.
- سهل الاستخدام من البداية، ويساعدك على العثور على معارفك بسرعة.
- غالبا تقدم مجموعة ميزات اوسع واكثر استقرارا، لان بناءها وتطويرها يكون ابسط ضمن نظام مركزي.
- قد تصبح مشكلات الخصوصية اقل اذا كان الخادم تحت سيطرتك وتقوم باستضافته بنفسك.

**العيوب:**

- قد ينتج عنها [ قيود على التحكم او على امكانية الوصول](https://drewdevault.com/2018/08/08/Signal.html). وقد يشمل ذلك امورا مثل:
- عدم السماح لبرامج طرف ثالث [بالاتصال بالشبكة المركزية](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165)، مع انها قد تقدم مرونة اعلى او تجربة استخدام افضل. في الغالب تجد هذه التفاصيل منصوصا عليها في بنود وشروط الاستخدام.
- نقص في الوثائق والارشادات (documentation) التي يحتاجها مطورو الطرف الثالث (third-party developers)، او عدم توفرها اساسا.
- اذا كانت الخدمة بيد جهة واحدة، فمن السهل ان تتبدل [ملكيتها](https://web.archive.org/web/20210729191953/https://blog.privacytools.io/delisting-wire)او سياسة الخصوصية او اسلوب ادارتها، ومع الوقت قد ينعكس ذلك سلبا على خصوصية المستخدمين.
- الاستضافة الذاتية ليست دائما سهلة، فهي تحتاج بعض المعرفة التقنية وجهدا في الاعداد.

## شبكات خوادم متعددة مترابطة

![شكل يوضح شبكات متعددة الخوادم](../assets/img/layout/network-decentralized.svg){ align=left }

هذا النوع من تطبيقات المراسلة يعتمد على اكثر من خادم مستقل وغير مركزي، مع امكانية ان تتواصل الخوادم مع بعضها (والبريد الالكتروني مثال واضح على ذلك). هذا النظام يسمح لمسؤول كل خادم بادارة خادمه بطريقته، وفي الوقت نفسه يبقى ضمن شبكة اتصالات اوسع.

في حالة الاستضافة الذاتية، يمكن لاعضاء خادم ضمن شبكة مترابطة التواصل مع اعضاء خوادم اخرى، لكن بعض الخوادم قد تقرر البقاء خاصة وغير مرتبطة بالخوادم الاخرى (مثل خادم داخلي لفريق في العمل).

**ما الذي يميزها:**

- يمنحك سيطرة اوسع على بياناتك اذا كنت تشغل خادمك بنفسك.
- يتيح لك اختيار الجهة التي تثق بها لحفظ بياناتك، عبر الاختيار بين عدة خوادم عامة (public servers).
- عادة يسمح بتطبيقات بديلة من طرف ثالث، يمكن ان توفر تجربة اكثر ملاءمة للجهاز، او اكثر تخصيصا، او اكثر قابلية للاستخدام للجميع.
- يمكن مراجعة برنامج الخادم وإثبات انه مطابق للكود المعلن، طالما ان لديك صلاحية الوصول للخادم، او انك تثق بمن يمتلك هذه الصلاحية (كفرد من العائلة).

**العيوب:**

- ادخال اي ميزة جديدة يتطلب جهدا اكبر، لانها تحتاج الى معيار متفق عليه واختبارات تضمن عملها بسلاسة مع كل خوادم الشبكة.
- نتيجة لما سبق، قد تلاحظ ان بعض الخصائص ناقصة او غير مستقرة او تختلف في سلوكها عن التطبيقات المركزية (centralized platforms)، مثل ارسال الرسائل اثناء عدم الاتصال او ميزة حذف الرسائل.
- قد تظل بعض المعلومات الجانبية متوفرة (مثل معرفة من يتحدث مع من)، لكن محتوى الرسائل لا يكون قابلا للاطلاع اذا تم استخدام E2EE.
- خوادم الشبكات المترابطة تتطلب غالبا ان تثق بمسؤول الخادم الذي تستخدمه. قد يدير الخادم شخص غير محترف في مجال الامن، وربما لا ينشر مستندات قياسية (standard documents) مثل سياسة الخصوصية او شروط الخدمة التي تشرح بوضوح كيف تستخدم بياناتك.
- قد يختار مدير الخادم حجب خوادم اخرى عندما تكون سببا في اساءات دون رقابة، او عندما لا تلتزم بقواعد التعامل المتفق عليها. هذا قد يمنعك من التواصل مع الاشخاص الموجودين على تلك الخوادم.

## شبكات اتصال مباشر بين الاجهزة (Peer-to-Peer Networks)

![P2P diagram](../assets/img/layout/network-distributed.svg){ align=left }

في تطبيقات المراسلة ذات الاتصال المباشر، يتم تمرير الرسالة عبر [شبكة موزعة](https://en.wikipedia.org/wiki/Distributed_networking) من العقد حتى تصل للمستلم، من غير وجود خادم مركزي لطرف ثالث.

في العادة يتم التعرف بين الاطراف عبر شبكة قائمة على [الحوسبة الموزعة (distributed computing)](https://en.wikipedia.org/wiki/Distributed_computing). امثلة على هذا: [Distributed Hash Tables](https://en.wikipedia.org/wiki/Distributed_hash_table) (DHT)، وهي تقنية تعتمد عليها بروتوكولات مثل [BitTorrent](https://en.wikipedia.org/wiki/BitTorrent_(protocol)) و [IPFS](https://en.wikipedia.org/wiki/InterPlanetary_File_System). طريقة اخرى هي شبكات المدى القصير، وفيها يتم الاتصال عبر الواي فاي او البلوتوث (مثل Briar او بروتوكول [Scuttlebutt](https://scuttlebutt.nz)للشبكات الاجتماعية).

عندما يعثر الطرف على طريق للوصول الى جهة الاتصال عبر اي من هذه الطرق، يتم بعدها تكوين اتصال مباشر بين الطرفين. مع ان الرسائل غالبا مشفرة، قد يستطيع الملاحظ استنتاج من يرسل لمن واين يوجد كل طرف.

شبكات الاتصال المباشر بين الاجهزة (P2P) لا تستخدم خوادم، لان الاطراف تتواصل فيما بينها مباشرة، لذلك لا يوجد مفهوم الاستضافة الذاتية هنا. لكن احيانا توجد خدمات اضافية تحتاج خوادم مركزية، مثل اكتشاف المستخدمين او توصيل الرسائل عندما يكون الطرف غير متصل، وهنا قد تكون الاستضافة الذاتية مفيدة.

**ما الذي يميزها:**

- Minimal information is exposed to third-parties.
- Modern P2P platforms implement E2EE by default. There are no servers that could potentially intercept and decrypt your transmissions, unlike centralized and federated models.

**العيوب:**

- Reduced feature set:
- Messages can only be sent when both peers are online, however, your client may store messages locally to wait for the contact to return online.
- Generally increases battery usage on mobile devices, because the client must stay connected to the distributed network to learn about who is online.
- Some common messenger features may not be implemented or incompletely, such as message deletion.
- Your IP address and that of the contacts you're communicating with may be exposed if you do not use the software in conjunction with a [VPN](../vpn.md) or [Tor](../tor.md). Many countries have some form of mass surveillance and/or metadata retention.

## Anonymous Routing

![Anonymous routing diagram](../assets/img/layout/network-anonymous-routing.svg){ align=left }

A messenger using [anonymous routing](https://doi.org/10.1007/978-1-4419-5906-5_628) hides either the identity of the sender, the receiver, or evidence that they have been communicating. Ideally, a messenger should hide all three.

There are [many](https://doi.org/10.1145/3182658) ways to implement anonymous routing. One of the most famous is [onion routing](https://en.wikipedia.org/wiki/Onion_routing) (i.e. [Tor](tor-overview.md)), which communicates encrypted messages through a virtual [overlay network](https://en.wikipedia.org/wiki/Overlay_network) that hides the location of each node as well as the recipient and sender of each message. The sender and recipient never interact directly and only meet through a secret rendezvous node so that there is no leak of IP addresses nor physical location. Nodes cannot decrypt messages, nor the final destination; only the recipient can. Each intermediary node can only decrypt a part that indicates where to send the still encrypted message next, until it arrives at the recipient who can fully decrypt it, hence the "onion layers."

Self-hosting a node in an anonymous routing network does not provide the host with additional privacy benefits, but rather contributes to the whole network's resilience against identification attacks for everyone's benefit.

**ما الذي يميزها:**

- Minimal to no information is exposed to other parties.
- Messages can be relayed in a decentralized manner even if one of the parties is offline.

**العيوب:**

- Slow message propagation.
- Often limited to fewer media types, mostly text, since the network is slow.
- Less reliable if nodes are selected by randomized routing, some nodes may be very far from the sender and receiver, adding latency or even failing to transmit messages if one of the nodes goes offline.
- More complex to get started, as the creation and secured backup of a cryptographic private key is required.
- Just like other decentralized platforms, adding features is more complex for developers than on a centralized platform. Hence, features may be lacking or incompletely implemented, such as offline message relaying or message deletion.
