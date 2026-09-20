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

الاتصال مباشرةً بشبكة Tor سيجعل استخدامك لها واضحًا لمسؤولي الشبكة المحلية أو لمزوّد خدمة الإنترنت (ISP). Detecting and correlating this traffic [has been done](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax) in the past by network administrators to identify and deanonymize specific Tor users on their network. في المقابل، يكون الاتصال بخدمة VPN أقل إثارة للشك في معظم الحالات، لأن خدمات الـ VPN التجارية يستخدمها الناس بشكل عادي لأغراض كثيرة، مثل تجاوز القيود الجغرافية على المحتوى، حتى في البلدان التي تفرض قيودًا شديدة على الإنترنت.

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

من الصعب أن تصل إلى مثل هذه الإعدادات الخاطئة عن طريق الخطأ، لأنها تتطلب عادةً ضبط إعدادات Proxy مخصّصة داخل متصفح Tor، أو داخل تطبيق الـ VPN بحيث يتم تمرير اتصال الـ VPN عبر متصفح Tor. As long as you avoid these non-default configurations, you're probably fine.

---

<div class="admonition info" markdown>
<p class="admonition-title">بصمات VPN/SSH</p>

يشير مشروع Tor إلى أنه من الناحية النظرية، قد لا يكون استخدام VPN لإخفاء نشاطك على Tor عن مزوّد خدمة الإنترنت (ISP) حلًا مضمونًا بالكامل. قد يتمكن من يراقب اتصال الـ VPN من تخمين الموقع الذي تزوره من شكل حركة البيانات، لأن لكل موقع نمطًا مميزًا في طريقة إرسال واستقبال البيانات.

لذلك، من الممكن أن يتم التعرف أيضا على حركة Tor المشفرة والمخفية داخل اتصال VPN باستخدام طرق مشابهة. لا توجد أبحاث منشورة حول هذا الأمر حتى الآن، وما زلنا نرى أن فوائد استخدام VPN أكبر بكثير من هذه المخاطر، لكن من الجيد أن تضع هذا الاحتمال في الحسبان.

If you still believe that pluggable transports (bridges) provide additional protection against website traffic fingerprinting that a VPN does not, you always have the option to use a bridge **and** a VPN in conjunction.

</div>

تحديد ما إذا كان من الأفضل أن تتصل أولا بخدمة VPN قبل استخدام Tor يعتمد على تقديرك للموقف، ومعرفتك بسياسات حكومتك ومزوّد خدمة الإنترنت (ISP) تجاه نوع الاتصالات التي تستخدمها. ومع ذلك، نؤكد مرة أخرى أنه في معظم الحالات، من الأفضل أن يبدو اتصالك وكأنك تستخدم شبكة VPN تجارية بدلًا من الاتصال مباشرةً بشبكة Tor. إذا كانت خدمات الـ VPN محجوبة في منطقتك، فيمكنك استخدام وسائل النقل القابلة للتمويه (Pluggable Transports) في Tor، مثل الجسور (Bridges) من نوع Snowflake أو meek، كبديل. لكن استخدام هذه الجسور قد يلفت الانتباه أكثر من اتصالات WireGuard أو OpenVPN العادية.

## ما ليس عليه Tor

شبكة Tor ليست أداة مثالية لحماية الخصوصية في جميع الحالات، ولديها عدد من العيوب التي ينبغي أخذها بعين الاعتبار بعناية. لا ينبغي أن تمنعك هذه الأمور من استخدام Tor إذا كان مناسبا لاحتياجاتك، لكنها تظل نقاطا مهمة يجب التفكير فيها عند تحديد الحل الأنسب لك.

### شبكة Tor ليس شبكة VPN مجانية

أدى إصدار تطبيق *Orbot* للهواتف المحمولة إلى وصف كثير من الناس لشبكة Tor بأنها «VPN مجاني» لكل حركة المرور على جهازك. لكن استخدام Tor بهذه الطريقة ينطوي على بعض المخاطر مقارنةً بخدمة الـ VPN التقليدية.

على عكس عُقد الخروج (Exit Nodes) في Tor، فإن مزودي خدمات الـ VPN لا يكونون *عادةً* جهات [خبيثة](#caveats) تتعمد الإضرار بالمستخدمين. لأن أي شخص يمكنه إنشاء عُقد خروج (Exit Nodes) في Tor، فقد تُستخدم هذه العُقد لمراقبة حركة الإنترنت أو التلاعب بها. In 2020, many Tor exit nodes were documented to be downgrading HTTPS traffic to HTTP in order to [hijack cryptocurrency transactions](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). Other exit node attacks such as replacing downloads via unencrypted channels with malware have also been observed. HTTPS does mitigate these threats to an extent.

As we've alluded to already, Tor is also easily identifiable on the network. Unlike an actual VPN provider, using Tor will make you stick out as a person likely attempting to evade authorities. In a perfect world, Tor would be seen by network administrators and authorities as a tool with many uses (like how VPNs are viewed), but in reality the perception of Tor is still far less legitimate than the perception of commercial VPNs. As such, using a real VPN provides you with plausible deniability, e.g. "I was just using it to watch Netflix," etc.

### Tor usage is not undetectable

**Even if you use bridges and pluggable transports,** the Tor Project doesn't provide any tools to hide the fact that you are using Tor from your ISP. Even using obfuscated "pluggable transports" or non-public bridges do not hide the fact that you are using a private communications channel. The most popular pluggable transports like obfs4 (which obfuscates your traffic to "look like nothing") and meek (which uses domain fronting to camouflage your traffic) can be [detected](https://hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) with fairly standard traffic analysis techniques. Snowflake has similar issues, and can be [easily detected](https://hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) *before* a Tor connection is even established.

Pluggable transports other than these three do exist, but typically rely on security through obscurity to evade detection. They aren't impossible to detect—they are just used by so few people that it's not worth the effort building detectors for them. They shouldn't be relied upon if you specifically are being monitored.

It is critical to understand the difference between bypassing censorship and evading detection. It is easier to accomplish the former because of the many real-world limitations on what network censors can realistically do en masse, but these techniques do not hide the fact that you—*specifically* you—are using Tor from an interested party monitoring your network.

### Tor Browser is not the most *secure* browser

Anonymity can often be at odds with security. Tor achieves anonymity by ensuring every user appears identical, creating a digital monoculture where the same vulnerabilities exist across all installations. In cybersecurity, monocultures are generally considered a risk. Security through diversity provides natural segmentation by limiting the impact of an exploit to a smaller segment of users. While such diversity is structurally desirable for security, it inherently compromises user anonymity by making individuals trackable.

Additionally, Tor Browser is based on Firefox's Extended Support Release builds, which only receives patches for vulnerabilities considered *Critical* and *High* (not *Medium* and *Low*). This means that attackers could (for example):

1. Look for new Critical/High vulnerabilities in Firefox nightly or beta builds, then check if they are exploitable in Tor Browser (this vulnerability period can last weeks).
2. Chain *multiple* Medium/Low vulnerabilities together until they get the level of access they're looking for (this vulnerability period can last months or longer).

Those at risk of browser vulnerabilities should consider additional protections to defend against Tor Browser exploits, such as using Whonix in [Qubes](../os/qubes-overview.md) to contain your Tor browsing in a secure virtual machine and protect against leaks.

## Path Building to Clearnet Services

"Clearnet services" are websites which you can access with any browser, like [privacyguides.org](https://www.privacyguides.org). Tor lets you connect to these websites anonymously by routing your traffic through a network comprised of thousands of volunteer-run servers called nodes (or relays).

Every time you [connect to Tor](../tor.md), it will choose three nodes to build a path to the internet—this path is called a "circuit."

<figure markdown>
  ![Tor path showing your device connecting to an entry node, middle node, and exit node before reaching the destination website](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Tor path showing your device connecting to an entry node, middle node, and exit node before reaching the destination website](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Tor circuit pathway</figcaption>
</figure>

Each of these nodes has its own function:

### The Entry Node

The entry node, often called the guard node, is the first node to which your Tor client connects. The entry node is able to see your IP address, however it is unable to see what you are connecting to.

Unlike the other nodes, the Tor client will randomly select an entry node and stick with it for two to three months to protect you from certain attacks.[^1]

### The Middle Node

The middle node is the second node to which your Tor client connects. It can see which node the traffic came from—the entry node—and to which node it goes to next. The middle node cannot, see your IP address or the domain you are connecting to.

For each new circuit, the middle node is randomly selected out of all available Tor nodes.

### The Exit Node

The exit node is the point in which your web traffic leaves the Tor network and is forwarded to your desired destination. The exit node is unable to see your IP address, but it does know what site it's connecting to.

The exit node will be chosen at random from all available Tor nodes ran with an exit relay flag.[^2]

## Path Building to Onion Services

"Onion Services" (also commonly referred to as "hidden services") are websites which can only be accessed by the Tor browser. These websites have a long randomly generated domain name ending with `.onion`.

Connecting to an Onion Service in Tor works very similarly to connecting to a clearnet service, but your traffic is routed through a total of **six** nodes before reaching the destination server. Just like before, however, only three of these nodes are contributing to *your* anonymity, the other three nodes protect *the Onion Service's* anonymity, hiding the website's true IP and location in the same manner that Tor Browser is hiding yours.

<figure style="width:100%" markdown>
  ![Tor path showing your traffic being routed through your three Tor nodes plus three additional Tor nodes which hide the website's identity](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Tor path showing your traffic being routed through your three Tor nodes plus three additional Tor nodes which hide the website's identity](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Tor circuit pathway with Onion Services. Nodes in the <span class="pg-blue">blue</span> fence belong to your browser, while nodes in the <span class="pg-red">red</span> fence belong to the server, so their identity is hidden from you.</figcaption>
</figure>

## Encryption

Tor encrypts each packet (a block of transmitted data) three times with the keys from the exit, middle, and entry node in that order.

Once Tor has built a circuit, data transmission is done as follows:

1. Firstly: When the packet arrives at the entry node, the first layer of encryption is removed. In this encrypted packet, the entry node will find another encrypted packet with the middle node’s address. The entry node will then forward the packet to the middle node.

2. Secondly: When the middle node receives the packet from the entry node, it too will remove a layer of encryption with its key, and this time finds an encrypted packet with the exit node's address. The middle node will then forward the packet to the exit node.

3. Lastly: When the exit node receives its packet, it will remove the last layer of encryption with its key. The exit node will see the destination address and forward the packet to that address.

Below is an alternative diagram showing the process. Each node removes its own layer of encryption, and when the destination server returns data, the same process happens entirely in reverse. For example, the exit node does not know who you are, but it does know which node it came from, and so it adds its own layer of encryption and sends it back.

<figure markdown>
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Sending and receiving data through the Tor Network</figcaption>
</figure>

Tor allows us to connect to a server without any single party knowing the entire path. The entry node knows who you are, but not where you are going; the middle node doesn’t know who you are or where you are going; and the exit node knows where you are going, but not who you are. Because the exit node is what makes the final connection, the destination server will never know your IP address.

## Caveats

Though Tor does provide strong privacy guarantees, one must be aware that Tor is not perfect:

- Tor never protects you from exposing yourself by mistake, such as if you share too much information about your real identity.
- Tor exit nodes can **modify** unencrypted traffic which passes through them. This means traffic which is not encrypted, such as plain HTTP traffic, can be changed by a malicious exit node. **Never** download files from an unencrypted `http://` website over Tor, and ensure your browser is set to always upgrade HTTP traffic to HTTPS.
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
