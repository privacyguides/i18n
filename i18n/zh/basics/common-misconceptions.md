---
title: "常见误区"
icon: 'material/robot-confused'
description: Privacy isn't a straightforward topic, and it's easy to get caught up in marketing claims and other disinformation.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Is open source software inherently secure?
        acceptedAnswer:
          "@type": Answer
          text: |
            Whether the source code is available and how software is licensed does not inherently affect its security in any way. Open-source software has the potential to be more secure than proprietary software, but there is absolutely no guarantee this is the case. When you evaluate software, you should look at the reputation and security of each tool on an individual basis.
      - 
        "@type": Question
        name: Can shifting trust to another provider increase privacy?
        acceptedAnswer:
          "@type": Answer
          text: |
            在讨论像VPN这样的解决方案时，我们经常谈到 "转移信任"（它将你对ISP的信任转移到VPN供应商身上）。 While this protects your browsing data from your ISP specifically, the VPN provider you choose still has access to your browsing data: Your data isn't completely secured from all parties.
      - 
        "@type": Question
        name: Are privacy-focused solutions inherently trustworthy?
        acceptedAnswer:
          "@type": Answer
          text: |
            仅仅关注一个工具或供应商的隐私政策和营销，会让你看不到它的弱点。 当你在寻找一个更私人的解决方案时，你应该确定根本的问题是什么，并为这个问题找到技术解决方案。 例如，您可能希望避免使用Google云端硬盘，因为它允许Google访问您的所有数据。 The underlying problem in this case is lack of E2EE, so you should make sure that the provider you switch to actually implements E2EE, or use a tool (like Cryptomator) which provides E2EE on any cloud provider. 转换到一个 "注重隐私 "的供应商（不实施E2EE）并不能解决你的问题：它只是将信任从谷歌转移到该供应商。
      - 
        "@type": Question
        name: How complicated should my threat model be?
        acceptedAnswer:
          "@type": Answer
          text: |
            我们经常看到人们描述的隐私威胁模型过于复杂。 通常情况下，这些解决方案包括许多不同的电子邮件账户或有许多移动部件和条件的复杂设置等问题。 The replies are usually answers to "What is the best way to do X?"
            为自己寻找 "最佳 "解决方案并不一定意味着你要追求一个有几十种条件的无懈可击的解决方案--这些解决方案往往难以现实地发挥作用。 正如我们之前所讨论的，安全往往是以便利为代价的。
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

为自己寻找 "最佳 "解决方案并不一定意味着你要追求一个有几十种条件的无懈可击的解决方案--这些解决方案往往难以现实地发挥作用。 正如我们之前所讨论的，安全往往是以便利为代价的。 下面，我们提供一些提示。

1. ==行动需要服务于一个特定的目的：==思考如何用最少的行动完成你想要的东西。
2. ==消除人类的失败点：==我们会失败，会累，会忘记事情。 为了维护安全，避免依赖你必须记住的手动条件和流程。
3. ==为你的意图使用正确的保护水平。==我们经常看到所谓的执法或防传唤解决方案的建议。 这些往往需要专业知识，通常不是人们想要的。 如果你可以通过一个简单的疏忽轻易地去掉匿名，那么为匿名建立一个复杂的威胁模型就没有意义。

那么，如何看待这个问题？

最清晰的威胁模型之一是，部分人*，知道你是谁* ，而另一部分人不知道。 总有一些情况下你必须申报你的合法姓名，也有一些情况下你不需要这样做。

1. **已知身份** - 已知身份是用于必须申报姓名的事情。 有许多法律文件和合同都需要合法身份。 这可能包括开设银行账户、签署房产租赁合同、获得护照、进口物品时的海关申报，或以其他方式与你的政府打交道。 这些东西通常会导致信用卡、信用等级检查、账户号码，以及可能的实际地址等凭证。

    我们不建议使用VPN或Tor来做这些事情，因为你的身份已经通过其他方式被了解。

    !!! tip
   
        网购时，使用[快递柜](https://en.wikipedia.org/wiki/Parcel_locker)可以帮助你保持实际住址的隐私。

2. **未知身份** -未知身份可能是您经常使用的稳定化名。 它不是匿名的，因为它没有变化。 如果你是一个网络社区的一部分，你可能希望保留一个别人知道的角色。 这个化名不是匿名的，因为如果监测的时间足够长，关于主人的细节可以揭示进一步的信息，如他们的写作方式，他们对感兴趣的话题的一般知识，等等。

    你可能希望为此使用VPN，以掩盖你的IP地址。 金融交易更难掩盖。你可以考虑使用匿名的加密货币，如 [Monero](https://www.getmonero.org/)。 采用altcoin转移也可能有助于掩盖你的货币来源。 通常情况下，交易所需要完成KYC（了解你的客户），然后才允许你将法币兑换成任何种类的加密货币。 当地见面会选项也可能是一种解决方案;然而，这些往往更昂贵，有时也需要KYC。

3. **匿名身份** - 即使有经验，匿名身份也很难长期维持。 它们应该是短期和短命的身份，定期轮换。

    使用Tor可以帮助解决这个问题。 还值得注意的是，通过异步通信可以实现更大的匿名性。实时通信容易受到打字模式的分析（即超过一段文字，在论坛上分发，通过电子邮件等）。

[^1]: 其中一个明显的例子是 [2021年明尼苏达大学的研究人员将三个漏洞引入了Linux内核开发项目的事件](https://cse.umn.edu/cs/linux-incident)。
