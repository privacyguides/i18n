---
title: "常见威胁"
icon: '资料/视野'
description: 您的威胁模式是您自己量身定制的，但这些是本网站许多访客都关心的一些问题。
---

广义而言，可以将我们有关[威胁](threat-modeling.md) 或者适用于大多数人的目标的建议分为这几类。 ==你可能关注其中零个、 一个、 几个、 或所有这些可能性==， 你应该使用的工具和服务取决于你的目标。在这些类别之外，您可能面临其他的特定威胁，这是完全正常的！重要的是要去了解您选择的这些工具的优缺点，因为也许任何工具都不能够保护您免受所有可以想象到的威胁。

<span class="pg-purple">:material-incognito: **匿名性**</span>
:

将您的在线活动与真实身份隔离开来，保护您免受那些试图揭露*您*身份的人的侵害。

<span class="pg-red">:material-target-account: **定向攻击**</span>
:

保护您免受试图获取*您*的数据或设备访问权限的黑客或其他恶意行为者的侵害。

<span class="pg-viridian">:material-package-variant-closed-remove: **供应链攻击**</span>
:

通常是一种<span class="pg-red">:material-target-account: 定向攻击</span>形式，其核心是直接或通过第三方依赖引入到原本正常的软件中的漏洞或后门。

<span class="pg-orange">:material-bug-outline: **被动攻击**</span>
:

保护您免受恶意软件、数据泄露和其他同时针对许多人的攻击的影响。

<span class="pg-teal">:material-server-network: **服务提供商**</span>
:

保护您的数据不受服务提供商的侵害（例如，使用端到端加密，使您的数据对服务器不可读）。

<span class="pg-blue">:material-eye-outline: **大规模监控**</span>
:

保护您免受政府机构、组织、网站和服务共同追踪您的活动的影响。

<span class="pg-brown">:material-account-cash: **监控资本主义**</span>
:

保护您免受大型广告网络（如 Google 和 Facebook）以及无数其他第三方数据收集者的侵害。

<span class="pg-green">:material-account-search: **公开暴露**</span>
:

限制在网络上可访问的关于您的信息——无论是对搜索引擎还是对公众。

<span class="pg-blue-gray">:material-close-outline: **审查制度**</span>
:

避免获取信息的途径受到审查，或在网上发言时受到审查。

其中一些威胁可能比其他威胁更重要，具体取决于您的关注点。例如，可以访问有价值或关键数据的软件开发人员可能主要关注<span class="pg-viridian">:material-package-variant-closed-remove: 供应链攻击</span>和<span class="pg-red">:material-target-account: 定向攻击</span>。他们可能仍希望保护个人数据不被卷入<span class="pg-blue">:material-eye-outline: 大规模监控</span>项目中。同样，"普通人 "可能主要关心他们的个人数据的 <span class="pg-green">:material-account-search: ，公开曝光</span> ，但他们仍应警惕那些侧重于安全的问题，比如<span class="pg-orange">:material-bug-outline: ，被动攻击</span>，就像那些会影响到设备的恶意软件 。

## 匿名与隐私

<span class="pg-purple">:material-incognito: 匿名性</span>

匿名和隐私经常被混淆，但这是两个截然不同的概念。隐私是你对如何使用和分享你的数据所做的一系列选择，而匿名则是将你的在线活动与你的现实生活身份完全脱离关系。

例如，举报人和记者可能会有一个相对极端的威胁模型，需要完全匿名。这不仅是在隐藏他们所做的事情，他们有哪些数据，不被黑客或政府入侵，而且还完全隐藏他们是谁。这意味着为了保护他们的匿名性、隐私或安全，他们可以牺牲任何形式的便利，因为他们的生命可能依赖于前者。大多数普通人都不需要去这样做。

## 安全和隐私

<span class="pg-orange">:material-bug-outline: 被动攻击</span>

安全和隐私经常被混为一谈，因为你需要安全来获得任何形式的隐私。如果这些工具可以很容易地被攻击者利用并随后泄漏你的数据，那么无论再怎么看似隐私都无济于事。然而，反之亦然；世界上最安全的服务 *不一定是* 私密的。这方面最好的例子是将数据托付给谷歌，鉴于其规模，谷歌能够通过雇用行业领先的安全专家来保护他们的基础设施，从而最大限度地减少了安全事件。尽管谷歌提供了非常安全的服务，但很少有人会认为他们在谷歌的免费消费者产品(Gmail、YouTube等) 中的数据是私有的。

当涉及到应用程序安全时，我们通常不知道（有时甚至无法知道）我们使用的软件是否是恶意的，或者在未来的某一天会不会变成恶意的。即使是最值得信赖的开发人员，通常也不能保证他们的软件没有可能在以后被利用的严重漏洞。

为了最大限度地减少恶意软件可能造成的损害，您应该采用隔离方式进行安全防护。这可以是使用不同的计算机进行不同的工作，使用虚拟机来分离不同的相关应用程序组，或者使用一个安全的操作系统，重点是要有应用程序沙盒和强制性的访问控制。

<div class="admonition tip" markdown>
<p class="admonition-title">提示</p>

在应用程序沙盒方面，移动操作系统通常比桌面操作系统更安全。

应用程序无法获得根访问权限，只能访问您授予它们访问权限的系统资源。 ChromeOS 具有与 Android 类似的沙盒功能，macOS 具有完整的系统权限控制（开发者可以选择让应用程序加入沙盒）。 ChromeOS具有与安卓类似的沙盒属性，而macOS具有完整的系统权限控制和（针对开发者）可选的应用程序沙盒，然而这些操作系统的确会将识别信息传输给各自的OEM。 Linux倾向于不向系统供应商提交信息，但它对漏洞和恶意应用程序的保护很差。这可以通过大量使用虚拟机或容器的专用发行版（例如 [Qubes OS](../desktop.md#qubes-os)）在一定程度上得到缓解。

</div>

## 针对特定个人的攻击

<span class="pg-red">:material-target-account: 定向攻击</span>

针对特定用户的有针对性的攻击更加难以处理。常见的攻击途径包括通过电子邮件发送恶意文件，利用浏览器和操作系统的漏洞，以及物理攻击。如果您担心这一点，则可能需要采用更高级的威胁缓解策略。

<div class="admonition tip" markdown>
<p class="admonition-title">提示</p>

**网络浏览器**、**电子邮件客户端**和**办公应用程序**在设计上通常都运行源自第三方的不可信代码。运行多个虚拟机来将此类应用程序从主机系统中分离出来，以及彼此分离，是您可以使用的一种技术，以避免这些应用程序中的漏洞被利用，危及系统的其余部分。例如，Qubes OS或Windows上的Microsoft Defender Application Guard等技术提供了无缝执行此操作的便捷方法。

</div>

如果您担心**物理攻击**，您应该使用实现了安全验证启动的操作系统，如 Android、iOS、macOS 或 [Windows（带 TPM）](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process)。你还应该确保你的驱动器是加密的，并且操作系统使用TPM或安全 [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) 或 [Element](https://developers.google.com/android/security/android-ready-se) ，以限制输入加密口令的重试速率。你应该避免与你不信任的人分享你的电脑，因为大多数桌面操作系统没有按用户单独加密数据。

## 针对特定组织的攻击

<span class="pg-viridian">:material-package-variant-closed-remove: 供应链攻击</span>

供应链攻击通常是一种针对企业、政府和活动人士的<span class="pg-red">:material-target-account: 定向攻击</span>，尽管它们最终也可能危及广大公众。

<div class="admonition example" markdown>
<p class="admonition-title">示例</p>

这方面的一个著名例子发生在 2017 年，当时乌克兰一款流行的会计软件 M.E.Doc 感染了 *NotPetya* 病毒，随后导致下载该软件的人感染了勒索软件。 NotPetya 本身就是一次勒索软件攻击，影响了多个国家的 2000 多家公司，它是基于美国国家安全局（NSA）开发的用于通过网络攻击 Windows 计算机的 *永恒之蓝（EternalBlue）* 漏洞利用程序。

</div>

此类攻击可能有以下几种实施方式：

1. 贡献者或员工可能首先在项目或组织中获得权力地位，然后滥用该地位添加恶意代码。
2. 开发人员可能被外部强迫添加恶意代码。
3. 个人或团体可能会找到一个第三方软件依赖项（也称为库），并在知道它将被“下游”软件开发人员使用的情况下，努力用上述两种方法渗透它。

这类攻击可能需要大量的时间和准备才能执行，并且存在风险，因为它们可能会被发现，特别是在流行的并且有外部关注的开源项目中。不幸的是，它们也是最危险的攻击之一，因为很难完全防范。我们鼓励读者仅使用声誉良好并致力于通过以下方式降低风险的软件：

1. 只采用那些已经存在了一段时间且受欢迎的软件。对项目的关注越多，外部发现恶意更改的可能性就越大。恶意行为者也需要花更多的时间，通过有意义的贡献来获得社区信任。
2. 寻找使用广泛使用且受信任的构建基础架构平台（而不是开发人员工作站或自托管服务器）发布二进制文件的软件。像 GitHub Actions 这样的系统可以让您检查公开运行的构建脚本，以获得额外的信心。这降低了开发者机器上的恶意软件感染其包的可能性，并使人们确信生成的二进制文件确实是正确生成的。
3. 寻找单个源代码提交和发布的代码签名，这创建了一个谁做了什么的审计跟踪。例如：恶意代码在软件仓库中吗？哪个开发人员添加了它？它是在构建过程中添加的吗？
4. 检查源代码是否具有有意义的提交消息（例如[约定式提交](https://conventionalcommits.org)），解释每次更改旨在完成什么。清晰的消息可以使项目外部人员更容易验证、审计和发现错误。
5. 注意程序拥有的贡献者或维护者的数量。孤立的开发人员可能更容易被外部强迫添加恶意代码，或者因疏忽而启用不良行为。这很可能意味着“大型科技公司”开发的软件比不需要向任何人负责的独立开发者受到更多的审查。

## 免受服务提供商窥探的隐私

<span class="pg-teal">:material-server-network: 服务提供商</span>

我们生活在一个几乎所有东西都与互联网相连的世界里。我们的 "私人 "信息、电子邮件、社交互动通常存储在某个服务器上。通常，当您向某人发送消息时，该消息会存储在服务器上，当您的朋友想要阅读该消息时，服务器会将其显示给他们。

这样做的明显问题是，服务提供商（或入侵服务器的黑客）可以随时随地查看你的 "私人 "对话，而你却对此一无所知。这适用于许多常见服务，如短信、Telegram、Discord等。

值得庆幸的是，可以通过在发送到服务器之前就对您与收件人之间的通信进行端到端加密来缓解此问题。只要服务提供者不能获得任何一方的私钥，就能保证你的信息的保密性。

<div class="admonition note" markdown>
<p class="admonition-title">关于基于 Web 的加密的说明</p>

在实践中，不同的端到端加密实现的有效性各不相同。 [Signal](../real-time-communication.md＃signal)这类应用程序在您的设备本地运行，并且应用程序副本在不同的安装下保持相同。如果服务提供商在他们的应用程序中设置后门，试图窃取你的私钥，这可以在未来通过逆向工程检测出来。

另一方面，基于 Web 的端到端加密实现（例如 Proton Mail 的网页应用或 Bitwarden 的 *网页密码库*）依赖于服务器动态地向浏览器提供 JavaScript 代码来处理密码学。一个恶意的服务器可以针对一个特定的用户，向他们发送恶意的JavaScript代码来窃取他们的加密密钥，而用户是很难注意到这样的事情的。即使用户注意到有人试图窃取他们的密钥，也很难证明是提供商试图这样做，因为服务器可以选择向不同的用户提供不同的网络客户端。

因此，当依赖端到端加密时，你应该尽可能选择使用本地应用程序而不是网络客户端。

</div>

即使有端对端加密，服务提供商仍然可以根据 **元数据**，对你进行剖析，而这些元数据通常不受保护。虽然服务提供商无法阅读您的消息，但他们仍然可以观察到重要信息，例如您在与谁交谈、您向他们发送消息的频率以及您通常活跃的时间。对元数据的保护是相当不常见的，如果你关心这一点，应该密切关注你所使用的软件的技术文档，看看是否有任何元数据最小化或保护。

## 大规模监控计划

<span class="pg-blue">:material-eye-outline: 大规模监控</span>

大规模监控是指对许多或所有特定人群进行监控的工作。它通常是指像[Edward Snowden在2013披露](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present))的那一类政府项目。

<div class="admonition abstract" markdown>
<p class="admonition-title">监控图集 (Atlas of Surveillance)</p>

如果您想了解有关监控方法以及它们在您所在城市如何实施的更多信息，还可以查看由[电子前哨基金会 (Electronic Frontier Foundation)](https://eff.org) 制作的[监控图集 (Atlas of Surveillance)](https://atlasofsurveillance.org)。

在法国，您可以查看由非营利协会 La Quadrature du Net 维护的 [Technopolice 网站](https://technopolice.fr/villes)。

</div>

政府经常为大规模监控项目辩护，认为这是打击恐怖主义和防止犯罪的必要手段。然而，作为侵犯人权的行为，它们最常被不成比例地用于针对少数群体和持不同政见者等。

<div class="admonition quote" markdown>
<p class="admonition-title">美国公民自由联盟 (ACLU)：<em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">9/11 的隐私教训：大规模监控不是出路</a></em></p>

面对爱德华·斯诺登披露的 [棱镜 (PRISM)](https://en.wikipedia.org/wiki/PRISM) 和 [上游 (Upstream)](https://en.wikipedia.org/wiki/Upstream_collection) 等政府计划，情报官员也承认，美国国家安全局 (NSA) 多年来一直在秘密收集几乎所有美国人的电话记录——谁给谁打电话，打电话的时间，以及通话持续了多长时间。你应该考虑你的对手能观察到网络的哪些方面，以及你的行动是否有合理的可否认性。

</div>

尽管美国的大规模监控越来越多，但政府发现，像第215条这样的大规模监控计划在阻止实际犯罪或恐怖主义阴谋方面 "没有什么独特的价值"，其努力主要是重复联邦调查局自己的目标监控计划。[^2]

在网上，人们可以通过多种方法追踪您，包括但不限于：

- 你的IP地址
- 浏览器 Cookie
- 你提交给网站的数据
- 你的浏览器或设备指纹
- 支付方式的关联

如果您担心大规模监控项目，您可以使用一些策略，比如隔离您的在线身份，混入其他用户中，或者尽可能地避免泄露身份信息。

## 监控即商业模式

<span class="pg-brown">:material-account-cash: 监视资本主义</span>

> 监视资本主义是一种以获取个人数据和将个人数据商品化为核心，从而以此营利的经济体系。[^2]

确保您的数据私密性的最佳方法是首先不要将其放在外面。删除你在网上发现的关于自己的信息是你为了恢复隐私可以采取的最佳初步措施之一。使用内容拦截器等工具来限制对其服务器的网络请求，并阅读你使用的服务的隐私政策，可以帮助你避免许多基本的对手（尽管它不能完全防止跟踪）。[^4]

此外，即使是*广告技术*或追踪行业之外的公司，也可能与[数据代理商](https://en.wikipedia.org/wiki/Information_broker)（如剑桥分析、益博睿或 Datalogix）或其他方共享您的信息。例如，如果您的帐户具有“隐私模式” ，请启用此功能以确保您的帐户不会被搜索引擎索引，并且不会被未经您事先审核的人查看。对企业数据收集最有力的保护是尽可能地加密或混淆你的数据，使不同的供应商难以将数据相互关联并建立你的档案。

## 限制公共信息

<span class="pg-green">:material-account-search: 公开曝光</span>

保持数据私密性的最佳方法是首先不要将其公开。删除你在网上发现的不需要的信息是你可以采取的最好的第一步，以重新获得你的隐私。

- [查看我们的账户删除指南 :material-arrow-right-drop-circle:](account-deletion.md)

极权主义政府、网络管理员和服务提供商都可以在不同程度上进行在线审查，以控制用户的言论和用户可以获得的信息。这些过滤互联网的行为将永远与言论自由的理想不相容。

随着Twitter和Facebook等平台对公众需求、市场压力和政府机构的压力做出让步，企业平台的审查制度也越来越普遍。政府可以向企业隐蔽，例如白宫 [要求删除](https://www.nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) 某个挑衅性的YouTube视频；也可以是公开的，例如中国政府要求企业遵守严格的审查制度。

## 避免审查

<span class="pg-blue-gray">:material-close-outline: 审查</span>

包括极权主义政府、网络管理员和服务提供商在内的行为者都可以（在不同程度上）进行网上审查。这些控制通讯和限制获取信息的努力，总是与言论自由的人权不相容。[^5]

企业平台的审查制度越来越普遍，因为像Twitter和Facebook这样的平台屈服于公众需求、市场压力和政府机构的压力。政府压力可能是向企业发出的暗中请求，例如白宫[要求下架](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html)具有挑衅性的 YouTube 视频；也可以是公开的，例如中国政府要求企业遵守严格的审查制度。

担心审查制度威胁的人可以使用[Tor](../advanced/tor-overview.md)等技术来规避它，并支持像[Matrix](../social-networks.md#element)这样抗审查的通信平台，它没有可以任意关闭帐户的中央帐户授权机构。

<div class="admonition tip" markdown>
<p class="admonition-title">提示</p>

虽然逃避审查本身很容易，但隐藏你正在做的事实可能非常有问题。

你应该考虑你的对手可以观察到网络的哪些方面，以及你的行动是否有合理的可否认性。例如，使用[加密DNS](.../advanced/dns-overview.md#what-is-encrypted-dns)可以帮助你绕过初级的、基于DNS的审查系统，但它不能真正向ISP隐藏你正在访问的内容。 VPN或Tor可以帮助向网络管理员隐藏你正在访问的内容，但不能隐藏你首先在使用这些网络。可插拔的传输工具（如Obfs4proxy、Meek或Shadowsocks）可以帮助你逃避阻挡普通VPN协议或Tor的防火墙，但你的规避尝试仍然可以被探测或[深度包检查](https://en.wikipedia.org/wiki/Deep_packet_inspection)等方法发现。

</div>

你必须始终考虑试图绕过审查制度的风险，潜在的后果，以及你的对手可能有多复杂。你应该谨慎地选择软件，并有一个备份计划，以防被发现。

[^1]: 美国隐私和公民自由监督委员会。 [关于根据第215条进行的电话记录计划的报告](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^2]: 维基百科： [监控资本主义](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^3]: 维基百科。 [*监视资本主义*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: 正如许多内容拦截器和防病毒程序所做的那样，“[列举恶劣事物](https://ranum.com/security/computer_security/editorials/dumb)”（或“列出我们所知道的所有坏东西”），无法充分保护您免受新的和未知的威胁，因为它们尚未被添加到过滤器列表中。你还应该采用其他缓解技术。
[^5]: 联合国：[*世界人权宣言*](https://un.org/en/about-us/universal-declaration-of-human-rights)。
