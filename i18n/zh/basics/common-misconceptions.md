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

</em> 开源软件 *，可以由第三方进行审计，而且通常比专有的同类软件对潜在的漏洞更加透明。 它还允许你审查代码并禁用你自己发现的任何可疑功能。 然而， *，除非你这样做*，否则不能保证代码曾经被评估过，特别是对于较小的软件项目。 开放的开发过程有时也被利用，甚至在大型项目中引入新的漏洞。[^1]</p>

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

网购时，使用[快递柜](https://en.wikipedia.org/wiki/Parcel_locker)可以帮助你保持实际住址的隐私。

</div>

2. **未知身份** -未知身份可能是您经常使用的稳定化名。 它不是匿名的，因为它没有变化。 如果你是一个网络社区的一部分，你可能希望保留一个别人知道的角色。 这个化名不是匿名的，因为如果监测的时间足够长，关于主人的细节可以揭示进一步的信息，如他们的写作方式，他们对感兴趣的话题的一般知识，等等。

你可能希望为此使用VPN，以掩盖你的IP地址。 Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](https://getmonero.org). 采用altcoin转移也可能有助于掩盖你的货币来源。 通常情况下，交易所需要完成KYC（了解你的客户），然后才允许你将法币兑换成任何种类的加密货币。 当地见面会选项也可能是一种解决方案;然而，这些往往更昂贵，有时也需要KYC。

3. **匿名身份** - 即使有经验，匿名身份也很难长期维持。 它们应该是短期和短命的身份，定期轮换。

使用Tor可以帮助解决这个问题。 还值得注意的是，通过异步通信可以实现更大的匿名性。实时通信容易受到打字模式的分析（即超过一段文字，在论坛上分发，通过电子邮件等）。

[^1]: 其中一个明显的例子是 [2021年明尼苏达大学的研究人员将三个漏洞引入了Linux内核开发项目的事件](https://cse.umn.edu/cs/linux-incident)。
