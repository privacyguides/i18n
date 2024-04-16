---
title: "常见误区"
icon: 'material/robot-confused'
description: 隐私并不是一个简单明了的话题，而且很容易被市场宣传和其他虚假信息所迷惑。
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Is open-source software inherently secure?
        acceptedAnswer:
          "@type": Answer
          text: |
            源代码是否可用以及软件的许可方式本身并不会对其安全性产生任何影响。 开源软件有可能比专有软件更安全，但不能保证一定如此。 在评估软件时，应逐一查看每个软件的声誉和安全性。
      - 
        "@type": Question
        name: 将信任转给另一家服务提供商能否提高隐私保护？
        acceptedAnswer:
          "@type": Answer
          text: |
            在讨论像VPN这样的解决方案时，我们经常谈到 "转移信任"（它将你对ISP的信任转移到VPN供应商身上）。 虽然这可以保护你的浏览数据不被 ISP 知晓，但你选择的 VPN 供应商仍然可以访问你的浏览数据。你的数据并不是全方位保护的。
      - 
        "@type": Question
        name: 注重隐私的解决方案一定可信吗？
        acceptedAnswer:
          "@type": Answer
          text: |
            仅仅关注一个工具或供应商的隐私政策和营销，会让你看不到它的弱点。 当你在寻找一个更私人的解决方案时，你应该确定根本的问题是什么，并为这个问题找到技术解决方案。 例如，您可能希望避免使用Google云端硬盘，因为它允许Google访问您的所有数据。 这种情况下的根本问题是缺乏端对端加密，所以你应该确保你切换到的供应商确实实现了端对端加密，或者使用一个工具（如 Cryptomator），在任何云供应商上使用端对端加密。 转换到一个 "注重隐私 "的供应商（不实施E2EE）并不能解决你的问题：它只是将信任从谷歌转移到该供应商。
      - 
        "@type": Question
        name: 我的威胁模型应该有多复杂？
        acceptedAnswer:
          "@type": Answer
          text: |
            我们经常看到人们描述的隐私威胁模型过于复杂。 通常情况下，这些解决方案包括许多不同的电子邮件账户或有许多移动部件和条件的复杂设置等问题。 答案的问题通常是“达到 × 的最佳方式是什么？”。
            为自己寻找 "最佳 "解决方案并不一定意味着你要追求一个有几十种条件的无懈可击的解决方案——这些解决方案往往难以现实地发挥作用。 正如我们之前所讨论的，安全往往是以便利为代价的。
---

## “开源软件始终是安全的”或“专有软件更安全”

这些神话源于一些偏见，但软件产品的来源和许可并不以任何方式内在地影响其安全性。 ==开源软件 *有可能* 比专有软件更安全, 但对于这一点没有绝对保证。== 在你评估软件时，需要去逐一检查每个工具的声誉和安全性。

</em> 开源软件 *，可以由第三方进行审计，而且通常比专有的同类软件对潜在的漏洞更加透明。 它还允许你审查代码并禁用你自己发现的任何可疑功能。 然而， *，除非你这样做*，否则不能保证代码曾经被评估过，特别是对于较小的软件项目。 The open development process has also sometimes been exploited to introduce new vulnerabilities known as <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>, which are discussed further in our [Common Threats](common-threats.md) page.[^1]</p>

从另一个角度看，专利软件的透明度较低，但这并不意味着它不安全。 主要的专利软件项目可以由内部和第三方机构进行审计，而独立的安全研究人员仍然可以通过逆向工程等技术找到漏洞。

为了避免决策出现偏差， *，你要评估你所使用的软件的隐私和安全标准，这一点至关重要*。

## "转移信任可以增加隐私"

在讨论像VPN这样的解决方案时，我们经常谈到 "转移信任"（它将你对ISP的信任转移到VPN供应商身上）。 虽然这可以保护你的浏览数据不被你的ISP *，特别是*，但你选择的VPN供应商仍然可以访问你的浏览数据。你的数据并不是完全不受各方保护的。 这意味着：

1. 在选择将信任转移给一个供应商时，你必须谨慎行事。
2. 你仍然应该使用其他技术，如E2EE，来完全保护你的数据。 仅仅是不信任一个供应商而信任另一个供应商，并不能保证你的数据安全。

## "以隐私为重点的解决方案本质上是值得信赖的"

仅仅关注一个工具或供应商的隐私政策和营销，会让你看不到它的弱点。 当你在寻找一个更私人的解决方案时，你应该确定根本的问题是什么，并为这个问题找到技术解决方案。 例如，您可能希望避免使用Google云端硬盘，因为它允许Google访问您的所有数据。 这种情况下的根本问题是缺乏E2EE，所以你应该确保你切换到的供应商确实实现了E2EE，或者使用一个工具（如 [Cryptomator](../encryption.md#cryptomator-cloud)），在任何云供应商上提供E2EE。 转换到一个 "注重隐私 "的供应商（不实施E2EE）并不能解决你的问题：它只是将信任从谷歌转移到该供应商。

你所选择的供应商的隐私政策和商业惯例是非常重要的，但应该被认为是次要的，因为对你的隐私的技术保证。当信任一个供应商根本不是一个要求时，你不应该把信任转移到另一个供应商身上。

## "复杂的是更好的"

我们经常看到人们描述的隐私威胁模型过于复杂。 通常情况下，这些解决方案包括许多不同的电子邮件账户或有许多移动部件和条件的复杂设置等问题。 答案通常是“做 *×*的最佳方式是什么？”。

为自己寻找 "最佳 "解决方案并不一定意味着你要追求一个有几十种条件的无懈可击的解决方案——这些解决方案往往难以现实地发挥作用。 正如我们之前所讨论的，安全往往是以便利为代价的。 下面，我们提供一些提示。

1. ==行动需要服务于一个特定的目的：==思考如何用最少的行动完成你想要的东西。
2. ==消除人类的失败点：==我们会失败，会累，会忘记事情。 为了维护安全，避免依赖你必须记住的手动条件和流程。
3. ==为你的意图使用正确的保护水平。==我们经常看到所谓的执法或防传唤解决方案的建议。 这些往往需要专业知识，通常不是人们想要的。 如果你可以通过一个简单的疏忽轻易地去掉匿名，那么为匿名建立一个复杂的威胁模型就没有意义。

那么，如何看待这个问题？

最清晰的威胁模型之一是，部分人*，知道你是谁* ，而另一部分人不知道。 总有一些情况下你必须申报你的合法姓名，也有一些情况下你不需要这样做。

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Tip</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](https://getmonero.org). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added a obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
