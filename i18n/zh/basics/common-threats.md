---
title: "常见威胁"
icon: '资料/视野'
description: Your threat model is personal to you, but these are some of the things many visitors to this site care about.
---

广义而言，可以将我们有关[威胁](threat-modeling.md) 或者适用于大多数人的目标的建议分为这几类。 ==你可能关注其中零个、 一个、 几个、 或所有这些可能性==， 你应该使用的工具和服务取决于你的目标。 你可能也有这些类别之外的特定威胁，这完全可以！ 重要的是要去了解您选择的这些工具的优缺点，因为也许任何工具都不能够保护您免受所有可以想象到的威胁。

- <span class="pg-purple">:material-incognito: 匿名性</span> - 隔离你的线上活动和你的真实身份, 特别是要保护 *你的* 身份不被人揭露。
- <span class="pg-red">:material-target-account: 定向攻击</span> -防御专业黑客或恶意代理人获得，特别是 *你的* 数据或设备的访问权。
- <span class="pg-orange">:material-bug-outline: 被动攻击</span> - 防御诸如恶意软件、数据泄露和其他一些同时针对许多人的攻击。
- <span class="pg-teal">:material-server-network: 服务供应商</span> - 保护您的数据不受服务供应商的影响，例如，通过端到端加密使您的数据无法被服务器读取。
- <span class="pg-blue">:material-eye-outline: 大规模监控</span> - 防止政府机构、组织、网站和服务联合起来共同追踪你的活动。
- <span class="pg-brown">:material-account-cash: 监视资本主义</span> - 保护自己不受谷歌和Facebook等大型广告网络以及其他无数第三方数据收集者的影响
- <span class="pg-green">:material-account-search: 公开曝光</span> - 限制搜索引擎或一般公众在线访问到关于你的信息的能力。
- <span class="pg-blue-gray">:material-close-outline: 审查</span> - 避免信息的获取受到审查或者在网上的发言被审查。

其中一些威胁可能比其他威胁更重要，具体取决于您的关注点。 例如，一个能接触到有价值或关键数据的软件开发者可能主要关注 <span class="pg-red">:material-target-account: 定向攻击</span>，但除此之外，他们可能仍然希望保护自己的个人数据不被卷进 <span class="pg-blue">:material-eye-outline: 大规模监控</span> 计划。 同样，"普通人 "可能主要关心他们的个人数据的 <span class="pg-green">:material-account-search: ，公开曝光</span> ，但他们仍应警惕那些侧重于安全的问题，比如<span class="pg-orange">:material-bug-outline: ，被动攻击</span>，就像那些会影响到设备的恶意软件 。

## 匿名与隐私

<span class="pg-purple">:material-incognito: 匿名性</span>

匿名和隐私经常被混淆，但这是两个截然不同的概念。 隐私是你对如何使用和分享你的数据所做的一系列选择，而匿名则是将你的在线活动与你的现实生活身份完全脱离关系。

例如，举报人和记者可能会有一个相对极端的威胁模型，需要完全匿名。 这不仅是在隐藏他们所做的事情，他们有哪些数据，不被黑客或政府入侵，而且还完全隐藏他们是谁。 这意味着为了保护他们的匿名性、隐私或安全，他们可以牺牲任何形式的便利，因为他们的生命可能依赖于前者。 大多数普通人都不需要去这样做。

## 安全和隐私

<span class="pg-orange">:material-bug-outline: 被动攻击</span>

安全和隐私经常被混为一谈，因为你需要安全来获得任何形式的隐私。如果这些工具可以很容易地被攻击者利用并随后泄漏你的数据，那么无论再怎么看似隐私都无济于事。 然而，反之亦然；世界上最安全的服务 *不一定是* 私密的。 这方面最好的例子是将数据托付给谷歌，鉴于其规模，谷歌能够通过雇用行业领先的安全专家来保护他们的基础设施，从而最大限度地减少了安全事件。 尽管谷歌提供了非常安全的服务，但很少有人会认为他们在谷歌的免费消费者产品(Gmail、YouTube等) 中的数据是私有的。

当涉及到应用程序安全时，我们通常不知道（有时甚至无法知道）我们使用的软件是否是恶意的，或者在未来的某一天会不会变成恶意的。 即使是最值得信赖的开发人员，通常也不能保证他们的软件没有可能在以后被利用的严重漏洞。

为了最大限度地减少恶意软件可能造成的损害，您应该采用隔离方式进行安全防护。 这可以是使用不同的计算机进行不同的工作，使用虚拟机来分离不同的相关应用程序组，或者使用一个安全的操作系统，重点是要有应用程序沙盒和强制性的访问控制。

!!! tip

    在应用程序沙盒方面，移动操作系统通常比桌面操作系统更安全。
    
    应用程序无法获得根访问权限，只能访问您授予它们访问权限的系统资源。 桌面操作系统在成熟的沙箱方面通常比较落后。 ChromeOS具有与安卓类似的沙盒属性，而macOS具有完整的系统权限控制和（针对开发者）可选的应用程序沙盒，然而这些操作系统的确会将识别信息传输给各自的OEM。 Linux倾向于不向系统供应商提交信息，但它对漏洞和恶意应用程序的保护很差。 这一点可以通过大量使用虚拟机或容器的专门发行版（如Qubes OS）得到一定程度的缓解。

<span class="pg-red">:material-target-account: 定向攻击</span>

针对特定用户的有针对性的攻击更加难以处理。 常见的攻击途径包括通过电子邮件发送恶意文件，利用浏览器和操作系统的漏洞，以及物理攻击。 如果您担心这一点，则可能需要采用更高级的威胁缓解策略。

!!! tip

    **网络浏览器**、**电子邮件客户端**和**办公应用程序**在设计上通常都运行源自第三方的不可信代码。 运行多个虚拟机来将此类应用程序从主机系统中分离出来，以及彼此分离，是您可以使用的一种技术，以避免这些应用程序中的漏洞被利用，危及系统的其余部分。 例如，Qubes OS或Windows上的Microsoft Defender Application Guard等技术提供了无缝执行此操作的便捷方法。

如果你担心 **物理攻击** ，你应该使用具有安全验证启动实现的操作系统，如Android、iOS、macOS、 [Windows（带TPM）](https://docs.microsoft.com/en-us/windows/security/information-protection/secure-the-windows-10-boot-process)。 你还应该确保你的驱动器是加密的，并且操作系统使用TPM或安全 [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) 或 [Element](https://developers.google.com/android/security/android-ready-se) ，以限制输入加密口令的重试速率。 你应该避免与你不信任的人分享你的电脑，因为大多数桌面操作系统没有按用户单独加密数据。

## 来自服务提供商的隐私

<span class="pg-teal">:material-server-network: 服务提供商</span>

我们生活在一个几乎所有东西都与互联网相连的世界里。 我们的 "私人 "信息、电子邮件、社交互动通常存储在某个服务器上。 通常，当您向某人发送消息时，该消息会存储在服务器上，当您的朋友想要阅读该消息时，服务器会将其显示给他们。

这样做的明显问题是，服务提供商（或入侵服务器的黑客）可以随时随地查看你的 "私人 "对话，而你却对此一无所知。 这适用于许多常见服务，如短信、Telegram、Discord等。

值得庆幸的是，可以通过在发送到服务器之前就对您与收件人之间的通信进行端到端加密来缓解此问题。 只要服务提供者不能获得任何一方的私钥，就能保证你的信息的保密性。

!!! 注释“关于基于web的加密的说明”

    在实践中，不同的端到端加密实现的有效性各不相同。 [Signal](../real-time-communication.md＃signal)这类应用程序在您的设备本地运行，并且应用程序副本在不同的安装下保持相同。 如果服务提供商在他们的应用程序中设置后门，试图窃取你的私钥，这可以在未来通过逆向工程检测出来。
    
    另一方面，基于Web的端到端加密实现（如Proton Mail的webmail或Bitwarden的web vault）依赖于服务器动态地向浏览器提供JavaScript代码来处理加密操作。 一个恶意的服务器可以针对一个特定的用户，向他们发送恶意的JavaScript代码来窃取他们的加密密钥，而用户是很难注意到这样的事情的。 即使用户注意到有人试图窃取他们的密钥，也很难证明是提供商试图这样做，因为服务器可以选择向不同的用户提供不同的网络客户端。
    
    因此，当依赖端到端加密时，你应该尽可能选择使用本地应用程序而不是网络客户端。

即使有端对端加密，服务提供商仍然可以根据 **元数据**，对你进行剖析，而这些元数据通常不受保护。 虽然服务提供商无法阅读您的消息以查看您所说的内容，但他们仍然可以观察到您正在与谁通话、您给他们发送消息的频率以及您通常活跃的时间等情况。 对元数据的保护是相当不常见的，如果你关心这一点，应该密切关注你所使用的软件的技术文档，看看是否有任何元数据最小化或保护。

## 大规模监控计划

<span class="pg-blue">:material-eye-outline: 大规模监控</span>

大规模监控是指对许多或所有特定人群进行监控的工作。 它通常是指像[Edward Snowden在2013披露](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present))的那一类政府项目。

!!! 摘要“监测地图”

    如果你想了解更多关于监视方法以及它们在你的城市是如何实施的，你也可以看看[电子前沿基金会](https://atlasofsurveillance.org/)的[监视地图]。
    
    In France you can take a look at the [Technolopolice website](https://technopolice.fr/villes/) maintained by the non-profit association La Quadrature du Net.

政府经常为大规模监控项目辩护，认为这是打击恐怖主义和防止犯罪的必要手段。 然而，它侵犯人权，最常被用来不成比例地针对少数群体和持不同政见者等。

!!! 引用 "美国公民自由联盟。 [*9/11的隐私教训。大规模监控不是前进的方向*](https://www.aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward)"

    面对[爱德华-斯诺登披露的政府项目，如 [PRISM]（https://en.wikipedia.org/wiki/PRISM）和 [Upstream]（https://en.wikipedia.org/wiki/Upstream_collection）]，情报官员也承认，国家安全局多年来一直在秘密收集几乎每个美国人的电话记录--谁在给谁打电话，这些电话是什么时候打的，以及它们持续多长时间。 你应该考虑你的对手能观察到网络的哪些方面，以及你的行动是否有合理的可否认性。

尽管美国的大规模监控越来越多，但政府发现，像第215条这样的大规模监控计划在阻止实际犯罪或恐怖主义阴谋方面 "没有什么独特的价值"，其努力主要是重复联邦调查局自己的目标监控计划。[^2]

尽管美国的大规模监控越来越多，但政府发现，像第215条这样的大规模监控计划在阻止实际犯罪或恐怖主义阴谋方面 "没有什么独特的价值"，这份工作基本上只是在重复联邦调查局本身的目标监控计划。[^1]

- 你的IP地址
- 浏览器 Cookie
- 你提交给网站的数据
- 你的浏览器或设备指纹
- 支付方式的关联

\ [此列表并非详尽无遗]。

如果你担心大规模的监控项目，你可以使用一些策略，比如将你的在线身份进行分隔，与其他用户混在一起，或者尽可能地避免提供身份信息。

<span class="pg-brown">:material-account-cash: 监视资本主义</span>

> 监视资本主义是一种以获取个人数据和将个人数据商品化为核心，从而以此营利的经济体系。[^2]

确保您的数据私密性的最佳方法是首先不要将其放在外面。 删除你在网上发现的关于自己的信息是你为了恢复隐私可以采取的最佳初步措施之一。 使用内容拦截器等工具来限制对其服务器的网络请求，并阅读你使用的服务的隐私政策，可以帮助你避免许多基本的对手（尽管它不能完全防止跟踪）。[^4]

在你分享信息的网站上，检查你账户的隐私设置以限制该数据的传播范围是非常重要的。 例如，如果您的帐户具有“隐私模式” ，请启用此功能以确保您的帐户不会被搜索引擎索引，并且不会被未经您事先审核的人查看。 对企业数据收集最有力的保护是尽可能地加密或混淆你的数据，使不同的供应商难以将数据相互关联并建立你的档案。

## 限制公共信息

<span class="pg-green">:material-account-search: 公开曝光</span>

保持数据私密性的最佳方法是首先不要将其公开。 删除你在网上发现的不需要的信息是你可以采取的最好的第一步，以重新获得你的隐私。

- [查看我们的账户删除指南 :material-arrow-right-drop-circle:](account-deletion.md)

极权主义政府、网络管理员和服务提供商都可以在不同程度上进行在线审查，以控制用户的言论和用户可以获得的信息。 这些过滤互联网的行为将永远与言论自由的理想不相容。

随着Twitter和Facebook等平台对公众需求、市场压力和政府机构的压力做出让步，企业平台的审查制度也越来越普遍。 政府可以向企业隐蔽，例如白宫 [要求删除](https://www.nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) 某个挑衅性的YouTube视频；也可以是公开的，例如中国政府要求企业遵守严格的审查制度。

## 避免审查

<span class="pg-blue-gray">:material-close-outline: 审查</span>

包括极权主义政府、网络管理员和服务提供商在内的行为者都可以（在不同程度上）进行网上审查。 这些控制通讯和限制获取信息的努力，总是与言论自由的人权不相容。[^5]

企业平台的审查制度越来越普遍，因为像Twitter和Facebook这样的平台屈服于公众需求、市场压力和政府机构的压力。 政府可以向企业隐蔽，例如白宫 [要求删除](https://www.nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) 某个挑衅性的YouTube视频；也可以是公开的，例如中国政府要求企业遵守严格的审查制度。

关注审查制度威胁的人可以使用像 [Tor](../advanced/tor-overview.md) 这样的技术来规避审查制度，并支持像 [Matrix](../real-time-communication.md#element)这样的抗审查通信平台，该平台没有一个可以任意关闭账户的集中式账户管理机构。

!!! tip

    虽然逃避审查本身很容易，但隐藏你正在做的事实可能非常有问题。
    
    你应该考虑你的对手可以观察到网络的哪些方面，以及你的行动是否有合理的可否认性。 例如，使用[加密DNS](.../advanced/dns-overview.md#what-is-encrypted-dns)可以帮助你绕过初级的、基于DNS的审查系统，但它不能真正向ISP隐藏你正在访问的内容。 VPN或Tor可以帮助向网络管理员隐藏你正在访问的内容，但不能隐藏你首先在使用这些网络。 可插拔的传输工具（如Obfs4proxy、Meek或Shadowsocks）可以帮助你逃避阻挡普通VPN协议或Tor的防火墙，但你的规避尝试仍然可以被探测或[深度包检查](https://en.wikipedia.org/wiki/Deep_packet_inspection)等方法发现。

你必须始终考虑试图绕过审查制度的风险，潜在的后果，以及你的对手可能有多复杂。 你应该谨慎地选择软件，并有一个备份计划，以防被发现。

[^1]: 美国隐私和公民自由监督委员会。 [关于根据第215条进行的电话记录计划的报告](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^2]: 维基百科： [监控资本主义](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^3]: 维基百科。 [*监视资本主义*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[列举坏事](https://www.ranum.com/security/computer_security/editorials/dumb/)"（或 "列出我们知道的所有坏事"），正如许多广告拦截器和防病毒程序所做的那样，无法充分保护你免受新的和未知的威胁，因为它们还没有被添加到过滤器列表中。 你还应该采用其他缓解技术。
[^5]: 联合国。 [*世界人权宣言》*](https://www.un.org/en/about-us/universal-declaration-of-human-rights)。
