---
meta_title: "كيف تحمي الشبكات الافتراضية الخاصة خصوصيتك؟ مراجعتنا حول الشبكة الافتراضية الخاصة - دليل الخصوصية"
title: مراجعة حول الشبكة الافتراضية الخاصة
icon: material/vpn
description: تعمل الشبكات الخاصة الافتراضية على تحويل المخاطر بعيدًا عن مزود خدمة الإنترنت الخاص بك إلى جهة خارجية تثق بها. ينبغي لك أن تبقي هذه الأمور في ذهنك.
---

الشبكات الخاصة الافتراضية هي طريقة لتوسيع نهاية شبكتك للخروج في مكان آخر في العالم.

[:material-movie-open-play-outline: Video: Do you need a VPN?](https://www.privacyguides.org/videos/2024/12/12/do-you-need-a-vpn ""){.md-button}

في العادة، يستطيع مزود خدمة الإنترنت رؤية تدفق حركة الإنترنت الداخلة والخارجة من جهاز إنهاء الشبكة (أي المودم). Encryption protocols such as HTTPS are commonly used on the internet, so they may not be able to see exactly what you're posting or reading, but they can get an idea of the [domains you request](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

يؤدي استخدام الشبكة الخاصة الافتراضية إلى إخفاء هذه المعلومات عن مزود خدمة الإنترنت الخاص بك، وذلك عن طريق تحويل الثقة التي تضعها في شبكتك إلى خادم في مكان آخر من العالم. ونتيجة لذلك، يرى مزود خدمة الإنترنت فقط أنك متصل بشبكة خاصة افتراضية ولا يرى أي شيء عن النشاط الذي تقوم به عبرها.

<div class="admonition note" markdown>
<p class="admonition-title">ملاحظة</p>

عندما نشير إلى "الشبكات الخاصة الافتراضية" على هذا الموقع، فإننا نشير عادةً إلى المزودين **التجاريين** لخدمات الشبكة الافتراضية الخاصة (../vpn.md)، الذين تدفع لهم رسوماً شهرية مقابل توجيه حركة المرور على الإنترنت بشكل آمن عبر خوادمهم العامة. هناك العديد من الأشكال الأخرى للشبكات الخاصة الافتراضية، مثل تلك التي تستضيفها بنفسك أو تلك التي يتم تشغيلها بواسطة أماكن العمل والتي تسمح لك بالاتصال بشكل آمن بموارد الشبكة الداخلية/الخاصة بالموظفين، ومع ذلك، عادةً ما يتم تصميم الشبكات الخاصة الافتراضية هذه للوصول إلى الشبكات البعيدة بشكل آمن، بدلاً من حماية خصوصية اتصالك بالإنترنت.

</div>

## كيف تعمل الشبكة الافتراضية الخاصة؟

تقوم الشبكات الخاصة الافتراضية بتشفير حركة المرور بين جهازك وخادم مملوك من قِبَل مزودي هذه الشبكات لك. من وجهة نظر أي شخص يكون بينك وبين خادم الشبكات الخاصة الافتراضية، فإنه يبدو له الأمر كما لو كنت متصلاً بخادم هذه الشبكات. من وجهة نظر أي شخص يكون بين خادم الشبكات الخاصة الافتراضية والموقع النهائي، كُل ما يمكن رؤيته هو خادم هذه الشبكات متصلاً بموقع الويب.

``` mermaid
flowchart LR
 763931["Your Device<div>(with VPN Client)</div>"] ===|"VPN Encryption"| 404512{"VPN Server"}
 404512 -.-|"No VPN Encryption"| 593753(("The Internet<div>(Your Destination)</div>"))
 subgraph 763931["Your Device<div>(with VPN Client)</div>"]
 end
```

لاحظ أن الشبكات الخاصة الافتراضية لا تضيف أي أمان أو تشفير إلى حركة المرور بين خادم هذه الشبكات والموقع النهائي على الإنترنت. To access a website securely you **must** still ensure HTTPS is in use regardless of whether you use a VPN.

## هل يجب عليَّ استخدام شبكة خاصة افتراضية؟

**Yes**, almost certainly. تتمتع الشبكة الخاصة الافتراضية بالعديد من المزايا، بما في ذلك:

1. Hiding your traffic from **only** your Internet Service Provider.
1. إخفاء التنزيلات الخاصة بك (مثل التورنت) عن مزود خدمة الإنترنت والمنظمات المناهضة للقرصنة.
1. يساعدك إخفاء عنوان IP الخاص بك عن مواقع الويب والخدمات التابعة لجهات خارجية على التخفي ومنع التتبع القائم على عنوان IP.
1. يتيح لك تجاوز القيود الجغرافية على محتوى معين.

VPNs can provide *some* of the same benefits Tor provides, such as hiding your IP from the websites you visit and geographically shifting your network traffic, and good VPN providers will not cooperate with e.g. legal authorities from oppressive regimes, especially if you choose a VPN provider outside your own jurisdiction.

لا يمكن للشبكات الخاصة الافتراضية تشفير البيانات خارج الاتصال بين جهازك وخادم هذه الشبكات. يمكن لمزودي الشبكات الخاصة الافتراضية أيضاً رؤية حركة المرور الخاصة بك وتعديلها بنفس الطريقة التي يمكن أن يقوم بها مزود خدمة الإنترنت الخاص، لذلك لا يزال هناك مستوى من الثقة التي تضعها فيهم. ولا توجد طريقة بأي شَكلٍ من الأشكال للتحقق من سياسات "تسجيل البيانات" أو "التعقب" الخاصة مزود الشبكة الخاصة الافتراضية.

## متى لا تكون الشبكات الخاصة الافتراضية مناسبة؟

Using a VPN in cases where you're using your [real-life or well-known identity](common-misconceptions.md#complicated-is-better) online is unlikely to be useful. قد يؤدي القيام بذلك إلى تشغيل أنظمة اكتشاف البريد العشوائي والاحتيال، مثلما إذا كنت ستسجل الدخول إلى موقع الويب الخاص بالبنك الذي تتعامل معه.

من المهم أن تتذكر أن الشبكات الخاصة الافتراضية لن توفر لك إخفاء هُوِيَّة مطلق لأن مزود هذه الشبكات نفسه سيظل لديه إمكانية الوصول إلى عنوان IP الحقيقي الخاص بك، ومعلومات الموقع النهائي، وغالباً أيضاً إلى مساراً مالياً يمكن ربطه بك مباشرةً. "No logging" policies are merely a promise; if you need complete safety from the network itself, consider using [Tor](../advanced/tor-overview.md) in addition to or instead of a VPN.

يجب أيضاً ألّا تثق في الشبكة الخاصة الافتراضية لتأمين اتصالك بوجهة HTTP غير مشفرة. من أجل الحفاظ على خصوصية وأمن ما تقوم به على مواقع الويب التي تزورها، يجب عليك استخدام HTTPS. سيؤدي هذا إلى الحفاظ على كلمات المرور والرموز المميزة للجلسة والاستعلامات في مأمن من مزود الشبكة الخاصة الافتراضية وغيره من الأعداء المحتملين بين خادم هذه الشبكة والموقع النهائي. يجب تمكين وضع "الاتصال فقط عبر HTTPS" في متصفحك (إذا كان مدعوماً) للتخفيف من الهجمات التي تحاول تخفيض مستوى أمان اتصالك من HTTPS إلى HTTP.

## هل يجب علي استخدام نظام أسماء النطاقات المشفر مع الشبكة الافتراضية الخاصة؟

Unless your VPN provider hosts the encrypted DNS servers themselves, **probably not**. إن استخدام DoH/DOT (أو أي شكل آخر من أشكال نظام أسماء النطاقات المشفر) مع خوادم خارجية سيضيف ببساطة المزيد من الكيانات التي بحاجة أن تثق بها. لا يزال بإمكان مزود الشبكة الخاصة الافتراضية الخاص بك معرفة مواقع الويب التي تزورها بناءً على عناوين IP وطرق أخرى. بعد كل هذا، قد تكون هناك بعض المزايا لتمكين نظام أسماء النطاقات المشفر من أجل تمكين ميزات الأمان الأخرى في متصفحك، مثل: ECH. إن تقنيات المتصفح الداخلية التي تعتمد على نظام أسماء النطاقات المشفر جديدة نسبياً وغير منتشرة على نطاق واسع حتى الآن، لذا سواء إذا كانت ذات صلة بك على وجه الخصوص فهي مهمة سنتركها لك للبحث فيها بشكل مستقل.

سبب شائع آخر لتوصية استخدام نظام أسماء نطاقات مشفر هو أنه يمنع انتحال النظام. However, your browser should already be checking for [TLS certificates](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) with **HTTPS** and warn you about it. If you are not using **HTTPS**, then an adversary can still just modify anything other than your DNS queries and the end result will be little different.

## Should I use Tor *and* a VPN?

ربما شبكة Tor ليست مناسبة للجميع في المقام الأول. Consider your [threat model](threat-modeling.md), because if your adversary is not capable of extracting information from your VPN provider, using a VPN alone may provide enough protection.

If you do use Tor then you are *probably* best off connecting to the Tor network via a commercial VPN provider. However, this is a complex subject which we've written more about on our [Tor overview](../advanced/tor-overview.md) page.

## هل يجب عليّ الوصول إلى شبكة Tor بواسطة موفري شبكات خاصة افتراضية الذين يوفرون "عقد Tor"؟

لا يجب عليك استخدام هذه الميزة: الميزة الأساسية لاستخدام شبكة Tor هي أنك لا تثق بمزود الشبكة الخاصة الافتراضية الخاص بك، وهو ما ينفي عندما تستخدم عقد شبكة Tor المستضافة بواسطة هذه الشبكة الافتراضية بدلاً من الاتصال مباشرة بشبكة Tor من جهاز الكمبيوتر الخاص بك.

تدعم شبكة Tor حالياً فقط TCP. UDP (used by [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3), and other protocols), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol), and other packets will be dropped. يقوم مزودو الشبكة الخاصة الافتراضية عادةً للتعويض عن ذلك بتوجيه جميع الحزم غير التابعة لـ TCP عبر خادم شبكتهم الخاصة الافتراضية (قفزتك الأولى). This is the case with [ProtonVPN](https://protonvpn.com/support/tor-vpn). Additionally, when using this Tor over VPN setup, you do not have control over other important Tor features such as [Isolated Destination Address](https://whonix.org/wiki/Stream_Isolation) (using a different Tor circuit for every domain you visit).

The feature should be viewed as a *convenient* way to access hidden services on Tor, not to stay anonymous. For proper anonymity, use the actual [Tor Browser](../tor.md).

## ملكية الشبكة الخاصة الافتراضية التجارية

Most VPN services are owned by the same [few companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies). تدير هذه الشركات المشبوهة الكثير من خِدْمَات الشبكات الخاصة الافتراضية الأصغر حجماً لخلق الوهم بأن لديك خيارات أكثر مما لديك فعلاً ولتعظيم الربح. عادةً، يكون لدى هؤلاء المزودين الذين يغذّون شركتهم الوهمية سياسات خصوصية سيئة للغاية ولا ينبغي الوثوق بهم فيما يتعلق بحركة المرور على الإنترنت الخاصة بك. يجب أن تكون صارماً للغاية بشأن مقدم الخدمة الذي تقرر استخدامه.

يجب عليك أيضاً أن تكون حذراً من أن العديد من مواقع مراجعة الشبكات الخاصة الافتراضية هي مجرد حملات إعلانية لأعلى المستويات. ==Privacy Guides does not make money from recommending external products, and never uses affiliate programs.==

[توصياتنا بشأن الشبكات الخاصة الافتراضية](../vpn.md ""){.md-button}

## بدائل شبكات خاصة افتراضية حديثة

قامت العديد من المنظمات في الآونة الأخيرة بمحاولات لمعالجة بعض المشكلات التي تواجهها الشبكات الخاصة الافتراضية المركزية. تعتبر هذه التقنيات جديدة نسبياً، ولكنها تستحق المتابعة مع تطور المجال.

### ترحيلات متعددة الأطراف

تستخدم تقنية الترحيل متعددة الأطراف (MPRs) عُقَداً متعددة مملوكة لأطراف مختلفة، بحيث لا يعرف أي طرف مَنْ أنت وما الذي تتصل به. هذه هي الفكرة الأساسية وراء شبكة Tor، ولكن هناك الآن بعض الخِدْمَات المدفوعة التي تحاول محاكاة هذا النموذج.

تسعى عُقد الترحيل هذه إلى حل مشكلة متأصلة في الشبكات الخاصة الافتراضية وهي حقيقة أنه يجب عليك الثقة بهذه الشبكات الافتراضية بشكل كامل. تحقق هذه الاعتمادات الهدف عبر تقسيم المسؤوليات بين شركتين مختلفتين أو أكثر.

من الأمثلة على MPR المتوفرة تجارياً هو iCloud+ Private Relay من شركة أبل الذي يوجه حركة المرور الخاصة بك عبر خادمين:

1. الأول هو خادم تديره شركة آبل.

    يتمكن هذا الخادم من رؤية عنوان IP الخاص بجهازك عند الاتصال به، ولديه معرفة بمعلومات الدفع الخاصة بك ومُعرّف أبل المرتبط باشتراكك في iCloud. ومع ذلك، فهو غير قادر على رؤية الموقع الذي تتصل به.

2. أما الخادم الثاني يتم تشغيله بواسطة شبكة توصيل المحتوى CDN شريكة، مثل Cloudflare أو Fastly.

    يقوم هذا الخادم في الواقع بإجراء الاتصال بموقع الويب الخاص بك، ولكنه لا يملك أي معرفة بجهازك. عنوان IP الوحيد الذي يعرفه هو عنوان خادم أبل.

تعمل العُقد الأخرى بواسطة شركات أخرى تديرها بطريقة مماثلة للغاية. لا تتحقق هذه الحماية عبر التجزئة إلا إذا كنت تثق في أن الشركتين لن تتواطآ مع بعضهما البعض في إخفاء هويتك.

### Decentralized VPNs

Another attempt at solving the issues with centralized VPN services are dVPNs. These are based on blockchain technology and claim to eliminate trust in a single party by distributing the nodes across lots of different people. However, many times a dVPN will default to a single node, meaning you need to trust that node completely, just like a traditional VPN. Unlike a traditional VPN, this one node that can see all your traffic is a random person instead of your VPN provider that can be audited and has legal responsibilities to uphold their privacy policy. Multi-hop is needed to solve this, but that comes with a stability and performance cost.

Another consideration is legal liability. The exit node will need to deal with legal problems from misuse of the network, an issue that the Tor network has contended with for its entire existence. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

Many dVPNs are used to push a cryptocurrency rather than to make the best service. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## Related VPN Information

- [The Trouble with VPN and Privacy Review Sites](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [Free VPN App Investigation](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [Hidden VPN owners unveiled: 101 VPN products run by just 23 companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [This Chinese company is secretly behind 24 popular apps seeking dangerous permissions](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - a Very Precarious Narrative](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) by Dennis Schubert
