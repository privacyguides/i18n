---
title: "常见威胁"
icon: '资料/视野'
description: 您的威胁模式是您自己量身定制的，但这些是本网站许多访客都关心的一些问题。
---

广义而言，可以将我们有关[威胁](threat-modeling.md) 或者适用于大多数人的目标的建议分为这几类。 ==你可能关注其中零个、 一个、 几个、 或所有这些可能性==， 你应该使用的工具和服务取决于你的目标。 You may have specific threats outside these categories as well, which is perfectly fine! 重要的是要去了解您选择的这些工具的优缺点，因为也许任何工具都不能够保护您免受所有可以想象到的威胁。

<span class="pg-purple">:material-incognito: **Anonymity**</span>
:

Shielding your online activity from your real identity, protecting you from people who are trying to uncover *your* identity specifically.

<span class="pg-red">:material-target-account: **Targeted Attacks**</span>
:

Being protected from hackers or other malicious actors who are trying to gain access to *your* data or devices specifically.

<span class="pg-viridian">:material-package-variant-closed-remove: **Supply Chain Attacks**</span>
:

Typically, a form of <span class="pg-red">:material-target-account: Targeted Attack</span> that centers around a vulnerability or exploit introduced into otherwise good software either directly or through a dependency from a third party.

<span class="pg-orange">:material-bug-outline: **Passive Attacks**</span>
:

Being protected from things like malware, data breaches, and other attacks that are made against many people at once.

<span class="pg-teal">:material-server-network: **Service Providers**</span>
:

Protecting your data from service providers (e.g. with E2EE, which renders your data unreadable to the server).

<span class="pg-blue">:material-eye-outline: **Mass Surveillance**</span>
:

Protection from government agencies, organizations, websites, and services which work together to track your activities.

<span class="pg-brown">:material-account-cash: **Surveillance Capitalism**</span>
:

Protecting yourself from big advertising networks, like Google and Facebook, as well as a myriad of other third-party data collectors.

<span class="pg-green">:material-account-search: **Public Exposure**</span>
:

Limiting the information about you that is accessible online—to search engines or the public.

<span class="pg-blue-gray">:material-close-outline: **Censorship**</span>
:

Avoiding censored access to information or being censored yourself when speaking online.

其中一些威胁可能比其他威胁更重要，具体取决于您的关注点。 For example, a software developer with access to valuable or critical data may be primarily concerned with <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span> and <span class="pg-red">:material-target-account: Targeted Attacks</span>. They will likely still want to protect their personal data from being swept up in <span class="pg-blue">:material-eye-outline: Mass Surveillance</span> programs. 同样，"普通人 "可能主要关心他们的个人数据的 <span class="pg-green">:material-account-search: ，公开曝光</span> ，但他们仍应警惕那些侧重于安全的问题，比如<span class="pg-orange">:material-bug-outline: ，被动攻击</span>，就像那些会影响到设备的恶意软件 。

## 匿名与隐私

<span class="pg-purple">:material-incognito: 匿名性</span>

匿名和隐私经常被混淆，但这是两个截然不同的概念。 隐私是你对如何使用和分享你的数据所做的一系列选择，而匿名则是将你的在线活动与你的现实生活身份完全脱离关系。

例如，举报人和记者可能会有一个相对极端的威胁模型，需要完全匿名。 这不仅是在隐藏他们所做的事情，他们有哪些数据，不被黑客或政府入侵，而且还完全隐藏他们是谁。 这意味着为了保护他们的匿名性、隐私或安全，他们可以牺牲任何形式的便利，因为他们的生命可能依赖于前者。 大多数普通人都不需要去这样做。

## 安全和隐私

<span class="pg-orange">:material-bug-outline: 被动攻击</span>

安全和隐私经常被混为一谈，因为你需要安全来获得任何形式的隐私。如果这些工具可以很容易地被攻击者利用并随后泄漏你的数据，那么无论再怎么看似隐私都无济于事。 然而，反之亦然；世界上最安全的服务 *不一定是* 私密的。 这方面最好的例子是将数据托付给谷歌，鉴于其规模，谷歌能够通过雇用行业领先的安全专家来保护他们的基础设施，从而最大限度地减少了安全事件。 尽管谷歌提供了非常安全的服务，但很少有人会认为他们在谷歌的免费消费者产品(Gmail、YouTube等) 中的数据是私有的。

当涉及到应用程序安全时，我们通常不知道（有时甚至无法知道）我们使用的软件是否是恶意的，或者在未来的某一天会不会变成恶意的。 即使是最值得信赖的开发人员，通常也不能保证他们的软件没有可能在以后被利用的严重漏洞。

为了最大限度地减少恶意软件可能造成的损害，您应该采用隔离方式进行安全防护。 这可以是使用不同的计算机进行不同的工作，使用虚拟机来分离不同的相关应用程序组，或者使用一个安全的操作系统，重点是要有应用程序沙盒和强制性的访问控制。

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

在应用程序沙盒方面，移动操作系统通常比桌面操作系统更安全。

应用程序无法获得根访问权限，只能访问您授予它们访问权限的系统资源。 ChromeOS has similar sandboxing capabilities to Android, and macOS has full system permission control (and developers can opt in to sandboxing for applications). ChromeOS具有与安卓类似的沙盒属性，而macOS具有完整的系统权限控制和（针对开发者）可选的应用程序沙盒，然而这些操作系统的确会将识别信息传输给各自的OEM。 Linux倾向于不向系统供应商提交信息，但它对漏洞和恶意应用程序的保护很差。 This can be mitigated somewhat with specialized distributions which make significant use of virtual machines or containers, such as [Qubes OS](../desktop.md#qubes-os).

</div>

## Attacks against Specific Individuals

<span class="pg-red">:material-target-account: 定向攻击</span>

针对特定用户的有针对性的攻击更加难以处理。 常见的攻击途径包括通过电子邮件发送恶意文件，利用浏览器和操作系统的漏洞，以及物理攻击。 如果您担心这一点，则可能需要采用更高级的威胁缓解策略。

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

**网络浏览器**、**电子邮件客户端**和**办公应用程序**在设计上通常都运行源自第三方的不可信代码。 运行多个虚拟机来将此类应用程序从主机系统中分离出来，以及彼此分离，是您可以使用的一种技术，以避免这些应用程序中的漏洞被利用，危及系统的其余部分。 例如，Qubes OS或Windows上的Microsoft Defender Application Guard等技术提供了无缝执行此操作的便捷方法。

</div>

If you are concerned about **physical attacks** you should use an operating system with a secure verified boot implementation, such as Android, iOS, macOS, or [Windows (with TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). 你还应该确保你的驱动器是加密的，并且操作系统使用TPM或安全 [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) 或 [Element](https://developers.google.com/android/security/android-ready-se) ，以限制输入加密口令的重试速率。 你应该避免与你不信任的人分享你的电脑，因为大多数桌面操作系统没有按用户单独加密数据。

## Attacks against Certain Organizations

<span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>

Supply chain attacks are frequently a form of <span class="pg-red">:material-target-account: Targeted Attack</span> towards businesses, governments, and activists, although they can end up compromising the public at large as well.

<div class="admonition example" markdown>
<p class="admonition-title">Example</p>

A notable example of this occurred in 2017 when M.E.Doc, a popular accounting software in Ukraine, was infected with the *NotPetya* virus, subsequently infecting people who downloaded that software with ransomware. NotPetya itself was a ransomware attack which impacted 2000+ companies in various countries, and was based on the *EternalBlue* exploit developed by the NSA to attack Windows computers over the network.

</div>

There are few ways in which this type of attack might be carried out:

1. A contributor or employee might first work their way into a position of power within a project or organization, and then abuse that position by adding malicious code.
2. A developer may be coerced by an outside party to add malicious code.
3. An individual or group might identify a third party software dependency (also known as a library) and work to infiltrate it with the above two methods, knowing that it will be used by "downstream" software developers.

These sorts of attacks can require a lot of time and preparation to perform and are risky because they can be detected, particularly in open source projects if they are popular and have outside interest. Unfortunately they're also one of the most dangerous as they are very hard to mitigate entirely. We would encourage readers to only use software which has a good reputation and makes an effort to reduce risk by:

1. Only adopting popular software that has been around for a while. The more interest in a project, the greater likelihood that external parties will notice malicious changes. A malicious actor will also need to spend more time gaining community trust with meaningful contributions.
2. Finding software which releases binaries with widely-used, trusted build infrastructure platforms, as opposed to developer workstations or self-hosted servers. Some systems like GitHub Actions let you inspect the build script that runs publicly for extra confidence. This lessens the likelihood that malware on a developer's machine could infect their packages, and gives confidence that the binaries produced are in fact produced correctly.
3. Looking for code signing on individual source code commits and releases, which creates an auditable trail of who did what. For example: Was the malicious code in the software repository? Which developer added it? Was it added during the build process?
4. Checking whether the source code has meaningful commit messages (such as [conventional commits](https://conventionalcommits.org)) which explain what each change is supposed to accomplish. Clear messages can make it easier for outsiders to the project to verify, audit, and find bugs.
5. Noting the number of contributors or maintainers a program has. A lone developer may be more susceptible to being coerced into adding malicious code by an external party, or to negligently enabling undesirable behavior. This may very well mean software developed by "Big Tech" has more scrutiny than a lone developer who doesn't answer to anyone.

## Privacy from Service Providers

<span class="pg-teal">:material-server-network: 服务提供商</span>

我们生活在一个几乎所有东西都与互联网相连的世界里。 我们的 "私人 "信息、电子邮件、社交互动通常存储在某个服务器上。 通常，当您向某人发送消息时，该消息会存储在服务器上，当您的朋友想要阅读该消息时，服务器会将其显示给他们。

这样做的明显问题是，服务提供商（或入侵服务器的黑客）可以随时随地查看你的 "私人 "对话，而你却对此一无所知。 这适用于许多常见服务，如短信、Telegram、Discord等。

值得庆幸的是，可以通过在发送到服务器之前就对您与收件人之间的通信进行端到端加密来缓解此问题。 只要服务提供者不能获得任何一方的私钥，就能保证你的信息的保密性。

<div class="admonition note" markdown>
<p class="admonition-title">Note on Web-based Encryption</p>

在实践中，不同的端到端加密实现的有效性各不相同。 [Signal](../real-time-communication.md＃signal)这类应用程序在您的设备本地运行，并且应用程序副本在不同的安装下保持相同。 如果服务提供商在他们的应用程序中设置后门，试图窃取你的私钥，这可以在未来通过逆向工程检测出来。

On the other hand, web-based E2EE implementations, such as Proton Mail's web app or Bitwarden's *Web Vault*, rely on the server dynamically serving JavaScript code to the browser to handle cryptography. 一个恶意的服务器可以针对一个特定的用户，向他们发送恶意的JavaScript代码来窃取他们的加密密钥，而用户是很难注意到这样的事情的。 即使用户注意到有人试图窃取他们的密钥，也很难证明是提供商试图这样做，因为服务器可以选择向不同的用户提供不同的网络客户端。

因此，当依赖端到端加密时，你应该尽可能选择使用本地应用程序而不是网络客户端。

</div>

即使有端对端加密，服务提供商仍然可以根据 **元数据**，对你进行剖析，而这些元数据通常不受保护。 While the service provider can't read your messages, they can still observe important things, such as whom you're talking to, how often you message them, and when you're typically active. 对元数据的保护是相当不常见的，如果你关心这一点，应该密切关注你所使用的软件的技术文档，看看是否有任何元数据最小化或保护。

## 大规模监控计划

<span class="pg-blue">:material-eye-outline: 大规模监控</span>

大规模监控是指对许多或所有特定人群进行监控的工作。 它通常是指像[Edward Snowden在2013披露](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present))的那一类政府项目。

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France, you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

政府经常为大规模监控项目辩护，认为这是打击恐怖主义和防止犯罪的必要手段。 However, as breaches of human rights, they're most often used to disproportionately target minority groups and political dissidents, among others.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

In the face of Edward Snowden's disclosures of government programs such as [PRISM](https://en.wikipedia.org/wiki/PRISM) and [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), intelligence officials also admitted that the NSA had for years been secretly collecting records about virtually every American’s phone calls — who’s calling whom, when those calls are made, and how long they last. 你应该考虑你的对手能观察到网络的哪些方面，以及你的行动是否有合理的可否认性。

</div>

尽管美国的大规模监控越来越多，但政府发现，像第215条这样的大规模监控计划在阻止实际犯罪或恐怖主义阴谋方面 "没有什么独特的价值"，其努力主要是重复联邦调查局自己的目标监控计划。[^2]

Online, you can be tracked via a variety of methods, including but not limited to:

- 你的IP地址
- 浏览器 Cookie
- 你提交给网站的数据
- 你的浏览器或设备指纹
- 支付方式的关联

If you're concerned about mass surveillance programs, you can use strategies like compartmentalizing your online identities, blending in with other users, or, whenever possible, simply avoiding giving out identifying information.

## Surveillance as a Business Model

<span class="pg-brown">:material-account-cash: 监视资本主义</span>

> 监视资本主义是一种以获取个人数据和将个人数据商品化为核心，从而以此营利的经济体系。[^2]

确保您的数据私密性的最佳方法是首先不要将其放在外面。 删除你在网上发现的关于自己的信息是你为了恢复隐私可以采取的最佳初步措施之一。 使用内容拦截器等工具来限制对其服务器的网络请求，并阅读你使用的服务的隐私政策，可以帮助你避免许多基本的对手（尽管它不能完全防止跟踪）。[^4]

Additionally, even companies outside the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. 例如，如果您的帐户具有“隐私模式” ，请启用此功能以确保您的帐户不会被搜索引擎索引，并且不会被未经您事先审核的人查看。 对企业数据收集最有力的保护是尽可能地加密或混淆你的数据，使不同的供应商难以将数据相互关联并建立你的档案。

## 限制公共信息

<span class="pg-green">:material-account-search: 公开曝光</span>

保持数据私密性的最佳方法是首先不要将其公开。 删除你在网上发现的不需要的信息是你可以采取的最好的第一步，以重新获得你的隐私。

- [查看我们的账户删除指南 :material-arrow-right-drop-circle:](account-deletion.md)

极权主义政府、网络管理员和服务提供商都可以在不同程度上进行在线审查，以控制用户的言论和用户可以获得的信息。 这些过滤互联网的行为将永远与言论自由的理想不相容。

随着Twitter和Facebook等平台对公众需求、市场压力和政府机构的压力做出让步，企业平台的审查制度也越来越普遍。 政府可以向企业隐蔽，例如白宫 [要求删除](https://www.nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) 某个挑衅性的YouTube视频；也可以是公开的，例如中国政府要求企业遵守严格的审查制度。

## 避免审查

<span class="pg-blue-gray">:material-close-outline: 审查</span>

包括极权主义政府、网络管理员和服务提供商在内的行为者都可以（在不同程度上）进行网上审查。 这些控制通讯和限制获取信息的努力，总是与言论自由的人权不相容。[^5]

企业平台的审查制度越来越普遍，因为像Twitter和Facebook这样的平台屈服于公众需求、市场压力和政府机构的压力。 Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

关注审查制度威胁的人可以使用像 [Tor](../advanced/tor-overview.md) 这样的技术来规避审查制度，并支持像 [Matrix](../real-time-communication.md#element)这样的抗审查通信平台，该平台没有一个可以任意关闭账户的集中式账户管理机构。

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

虽然逃避审查本身很容易，但隐藏你正在做的事实可能非常有问题。

你应该考虑你的对手可以观察到网络的哪些方面，以及你的行动是否有合理的可否认性。 例如，使用[加密DNS](.../advanced/dns-overview.md#what-is-encrypted-dns)可以帮助你绕过初级的、基于DNS的审查系统，但它不能真正向ISP隐藏你正在访问的内容。 VPN或Tor可以帮助向网络管理员隐藏你正在访问的内容，但不能隐藏你首先在使用这些网络。 可插拔的传输工具（如Obfs4proxy、Meek或Shadowsocks）可以帮助你逃避阻挡普通VPN协议或Tor的防火墙，但你的规避尝试仍然可以被探测或[深度包检查](https://en.wikipedia.org/wiki/Deep_packet_inspection)等方法发现。

</div>

你必须始终考虑试图绕过审查制度的风险，潜在的后果，以及你的对手可能有多复杂。 你应该谨慎地选择软件，并有一个备份计划，以防被发现。

[^1]: 美国隐私和公民自由监督委员会。 [关于根据第215条进行的电话记录计划的报告](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^2]: 维基百科： [监控资本主义](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^3]: 维基百科。 [*监视资本主义*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. 你还应该采用其他缓解技术。
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
