---
title: "Tor概述"
icon: 'simple/torproject'
description: Tor是一个免费使用的去中心化网络，专为尽量隐私地使用互联网而设计。
---

![Tor logo](../assets/img/self-contained-networks/tor.svg){ align=right }

[**Tor**](../alternative-networks.md#tor) is a free to use, decentralized network designed for using the internet with as much privacy as possible. 如果使用得当，该网络可以实现隐私且匿名地浏览和通信。 由于Tor流量难以阻止和跟踪，因此Tor是一种有效的审查规避工具。

[:material-movie-open-play-outline: Video: Why You Need Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor/ ""){.md-button}

Tor works by routing your internet traffic through volunteer-operated servers, instead of making a direct connection to the site you're trying to visit. 这会混淆流量的来源，并且连接路径中的任何服务器都无法看到流量来自和流向的完整路径，这意味着即使您用于连接的服务器也无法打破您的匿名性。

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

## Safely Connecting to Tor

Before connecting to Tor, you should carefully consider what you're looking to accomplish by using Tor in the first place, and who you're trying to hide your network activity from.

If you live in a free country, are accessing mundane content via Tor, aren't worried about your ISP or local network administrators having the knowledge that you're using Tor, and want to help [destigmatize](https://2019.www.torproject.org/about/torusers.html.en) Tor usage, you can likely connect to Tor directly via standard means like [Tor Browser](../tor.md) without worry.

If you have the ability to access a trusted VPN provider and **any** of the following are true, you almost certainly should connect to Tor through a VPN:

- You already use a [trusted VPN provider](../vpn.md)
- Your threat model includes an adversary which is capable of extracting information from your ISP
- Your threat model includes your ISP itself as an adversary
- Your threat model includes local network administrators before your ISP as an adversary

Because we already [generally recommend](../basics/vpn-overview.md) that the vast majority of people use a trusted VPN provider for a variety of reasons, the following recommendation about connecting to Tor via a VPN likely applies to you. <mark>There is no need to disable your VPN before connecting to Tor</mark>, as some online resources would lead you to believe.

Connecting directly to Tor will make your connection stand out to any local network administrators or your ISP. Detecting and correlating this traffic [has been done](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax) in the past by network administrators to identify and deanonymize specific Tor users on their network. On the other hand, connecting to a VPN is almost always less suspicious, because commercial VPN providers are used by everyday consumers for a variety of mundane tasks like bypassing geo-restrictions, even in countries with heavy internet restrictions.

Therefore, you should make an effort to hide your IP address **before** connecting to the Tor network. You can do this by simply connecting to a VPN (through a client installed on your computer) and then accessing [Tor](../tor.md) as normal, through Tor Browser for example. This creates a connection chain like:

- [x] You → VPN → Tor → Internet

From your ISP's perspective, it looks like you're accessing a VPN normally (with the associated cover that provides you). From your VPN's perspective, they can see that you are connecting to the Tor network, but nothing about what websites you're accessing. From Tor's perspective, you're connecting normally, but in the unlikely event of some sort of Tor network compromise, only your VPN's IP would be exposed, and your VPN would *additionally* have to be compromised to deanonymize you.

This is **not** censorship circumvention advice, because if Tor is blocked entirely by your ISP, your VPN likely is as well. Rather, this recommendation aims to make your traffic blend in better with commonplace VPN user traffic, and provide you with some level of plausible deniability by obscuring the fact that you're connecting to Tor from your ISP.

---

We **very strongly discourage** combining Tor with a VPN in any other manner. Do not configure your connection in a way which resembles any of the following:

- You → Tor → VPN → Internet
- You → VPN → Tor → VPN → Internet
- Any other configuration

Some VPN providers and other publications will occasionally recommend these **bad** configurations to evade Tor bans (exit nodes being blocked by websites) in some places. [Normally](https://support.torproject.org/#about_change-paths), Tor frequently changes your circuit path through the network. When you choose a permanent *destination* VPN (connecting to a VPN server *after* Tor), you're eliminating this advantage and drastically harming your anonymity.

Setting up bad configurations like these is difficult to do accidentally, because it usually involves either setting up custom proxy settings inside Tor Browser, or setting up custom proxy settings inside your VPN client which routes your VPN traffic through the Tor Browser. As long as you avoid these non-default configurations, you're probably fine.

---

<div class="admonition info" markdown>
<p class="admonition-title">VPN/SSH Fingerprinting</p>

The Tor Project [notes](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) that *theoretically* using a VPN to hide Tor activities from your ISP may not be foolproof. VPNs have been found to be vulnerable to website traffic fingerprinting, where an adversary can still guess what website is being visited, because all websites have specific traffic patterns.

Therefore, it's not unreasonable to believe that encrypted Tor traffic hidden by a VPN could also be detected via similar methods. There are no research papers on this subject, and we still consider the benefits of using a VPN to far outweigh these risks, but it is something to keep in mind.

If you still believe that pluggable transports (bridges) provide additional protection against website traffic fingerprinting that a VPN does not, you always have the option to use a bridge **and** a VPN in conjunction.

</div>

Determining whether you should first use a VPN to connect to the Tor network will require some common sense and knowledge of your own government's and ISP's policies relating to what you're connecting to. However, again in most cases you will be better off being seen as connecting to a commercial VPN network than directly to the Tor network. If VPN providers are censored in your area, then you can also consider using Tor pluggable transports (e.g. Snowflake or meek bridges) as an alternative, but using these bridges may arouse more suspicion than standard WireGuard/OpenVPN tunnels.

## What Tor is Not

The Tor network is not the perfect privacy protection tool in all cases, and has a number of drawbacks which should be carefully considered. These things should not discourage you from using Tor if it is appropriate for your needs, but they are still things to think about when deciding which solution is most appropriate for you.

### Tor is not a free VPN

The release of the *Orbot* mobile app has lead many people to describe Tor as a "free VPN" for all of your device traffic. However, treating Tor like this poses some dangers compared to a typical VPN.

Unlike Tor exit nodes, VPN providers are usually not *actively* [malicious](#caveats). Because Tor exit nodes can be created by anybody, they are hotspots for network logging and modification. In 2020, many Tor exit nodes were documented to be downgrading HTTPS traffic to HTTP in order to [hijack cryptocurrency transactions](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). Other exit node attacks such as replacing downloads via unencrypted channels with malware have also been observed. HTTPS does mitigate these threats to an extent.

As we've alluded to already, Tor is also easily identifiable on the network. Unlike an actual VPN provider, using Tor will make you stick out as a person likely attempting to evade authorities. In a perfect world, Tor would be seen by network administrators and authorities as a tool with many uses (like how VPNs are viewed), but in reality the perception of Tor is still far less legitimate than the perception of commercial VPNs, so using a real VPN provides you with plausible deniability, e.g. "I was just using it to watch Netflix," etc.

### Tor usage is not undetectable

**Even if you use bridges and pluggable transports,** the Tor Project provides no tools to hide the fact that you are using Tor from your ISP. Even using obfuscated "pluggable transports" or non-public bridges do not hide the fact that you are using a private communications channel. The most popular pluggable transports like obfs4 (which obfuscates your traffic to "look like nothing") and meek (which uses domain fronting to camouflage your traffic) can be [detected](https://hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) with fairly standard traffic analysis techniques. Snowflake has similar issues, and can be [easily detected](https://hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) *before* a Tor connection is even established.

Pluggable transports other than these three do exist, but typically rely on security through obscurity to evade detection. They aren't impossible to detect, they are just used by so few people that it's not worth the effort building detectors for them. They shouldn't be relied upon if you specifically are being monitored.

It is critical to understand the difference between bypassing censorship and evading detection. It is easier to accomplish the former because of the many real-world limitations on what network censors can realistically do en masse, but these techniques do not hide the fact that you—*specifically* you—are using Tor from an interested party monitoring your network.

### Tor Browser is not the most *secure* browser

Anonymity can often be at odds with security: Tor's anonymity requires every user to be identical, which creates a monoculture (the same bugs are present across all Tor Browser users). As a cybersecurity rule of thumb, monocultures are generally regarded as bad: Security through diversity (which Tor lacks) provides natural segmentation by limiting vulnerabilities to smaller groups, and is therefore usually desirable, but this diversity is also less good for anonymity.

Additionally, Tor Browser is based on Firefox's Extended Support Release builds, which only receives patches for vulnerabilities considered *Critical* and *High* (not *Medium* and *Low*). This means that attackers could (for example):

1. Look for new Critical/High vulnerabilities in Firefox nightly or beta builds, then check if they are exploitable in Tor Browser (this vulnerability period can last weeks).
2. Chain *multiple* Medium/Low vulnerabilities together until they get the level of access they're looking for (this vulnerability period can last months or longer).

Those at risk of browser vulnerabilities should consider additional protections to defend against Tor Browser exploits, such as using Whonix in [Qubes](../os/qubes-overview.md) to contain your Tor browsing in a secure VM and protect against leaks.

## 建立通往公开网络服务的链路

公开网络服务是您可以使用任何浏览器访问的网站，例如 [privacyguides.org](https://www.privacyguides.org)。 Tor的工作原理是通过一个由数千个志愿者运行的服务器（称为节点或中继）组成的网络路由您的流量。

每次你连接到 [Tor](../tor.md)，它都会选择三个节点来建立一条通往互联网的路径——这条路径被称为“链路”。

<figure markdown>
  ![显示您的设备在到达目的地网站前连接到入口节点、中间节点和出口节点的 Tor 链路](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![显示您的设备在到达目的地网站前连接到入口节点、中间节点和出口节点的 Tor 链路](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Tor 链路</figcaption>
</figure>

每个节点都有自己的功能：

### 入口节点

入口节点，通常被称为守护节点，是你的Tor客户端连接到的第一个节点。 入口节点能够看到你的IP地址，但它无法看到你正在连接什么。

与其他节点不同，Tor客户端会随机选择一个入口节点并坚持两到三个月，以保护你免受某些攻击。[^1]

### 中间节点

中间节点是你的Tor客户端连接的第二个节点。 它可以看到流量来自哪个节点--入口节点--以及它接下来要去哪个节点。 中间节点不能，看到你的IP地址或你正在连接的域。

对于每个新线路，在所有可用的Tor节点中随机选择中间节点。

### 出口节点

出口节点是你的网络流量离开Tor网络并被转发到待达目的地的地方。 出口节点无法看到你的IP地址，但它确实知道正在连接到哪个网站。

出口节点将从运行有出口中继标志的所有可用Tor节点中随机选择。[^2]

## 建立通往暗网网络服务的链路

暗网服务是只能通过 Tor 浏览器访问的网站。 这些网站有一个以 `.onion` 结尾的随机生成的长域名。

在 Tor 中连接到暗网服务的工作原理与连接到公网服务非常相似，但在到达目的地服务器之前，你的流量会经过**六个**节点。 不过，和前面一样，这些节点中只有三个有助于*你*的匿名性，其他三个节点保护*暗网服务*的匿名性，隐藏网站的真实 IP 和位置，就像 Tor 浏览器隐藏你的网站一样。

<figure style="width:100%" markdown>
  ![显示您的流量通过三个 Tor 节点以及另外三个隐藏暗网服务身份的 Tor 节点的 Tor 链路](.../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![显示您的流量通过三个 Tor 节点以及另外三个隐藏暗网服务身份的 Tor 节点的 Tor 链路](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>使用暗网服务的 Tor 链路。 <span class="pg-blue">蓝色</span> 方框中的节点属于您的浏览器，而 <span class="pg-red">红色</span> 方框中的节点属于服务器，因此它们的身份对您是隐藏的。</figcaption>
</figure>

## 加密

Tor用出口、中间和入口节点的密钥对每个数据包（一个传输的数据块）进行三次加密--按顺序进行。

一旦Tor建立了一个电路，数据传输就会按以下方式进行。

1. 首先：当数据包到达入口节点时，第一层的加密被移除。 在这个加密的数据包中，入口节点会发现另一个带有中间节点地址的加密数据包。 然后，入口节点将把数据包转发给中间节点。

2. 第二：当中间节点收到来自入口节点的数据包时，它也会用自己的密钥去掉一层加密，这时会发现一个带有出口节点地址的加密数据包。 然后，中间节点将把数据包转发给出口节点。

3. 最后：当出口节点收到其数据包时，它将用其密钥去除最后一层加密。 出口节点将看到目标地址并将数据包转发到该地址。

下面是一个显示该过程的替代图。 每个节点都会移除自己的加密层，而当目的地服务器返回数据时，同样的过程会完全反向发生。 例如，出口节点不知道你是谁，但它知道它来自哪个节点，因此它添加了自己的加密层并将其发送回来。

<figure markdown>
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Sending and receiving data through the Tor Network</figcaption>
</figure>

通过使用Tor，我们可以在没有任何一方知道整个线路的情况下连接到一个服务器。 入口节点知道你是谁，但不知道你要去哪里；中间节点不知道你是谁，也不知道你要去哪里；而出口节点知道你要去哪里，但不知道你是谁。 因为出口节点是进行最终连接的，目标服务器永远不会知道你的IP地址。

## Caveats (注意)

尽管Tor确实提供了强有力的隐私保障，但您必须意识到Tor并不完美：

- Tor never protects you from exposing yourself by mistake, such as if you share too much information about your real identity.
- Tor exit nodes can **modify** unencrypted traffic which passes through them. This means traffic which is not encrypted, such as plain HTTP traffic, can be changed by a malicious exit node. **Never** download files from an unencrypted `http://` website over Tor, and ensure your browser is set to always upgrade HTTP traffic to HTTPS.
- Tor出口节点也可以监控通过它们的流量。 Unencrypted traffic which contains personally identifiable information can deanonymize you to that exit node. Again, we recommend only using HTTPS over Tor.
- Powerful adversaries with the capability to passively watch *all* network traffic around the globe ("Global Passive Adversaries") are **not** something that Tor protects you against (and using Tor [with a VPN](#safely-connecting-to-tor) doesn't change this fact).
- Well-funded adversaries with the capability to passively watch *most* network traffic around the globe still have a *chance* of deanonymizing Tor users by means of advanced traffic analysis.

如果您希望使用Tor浏览网页，我们只建议使用 **官方** Tor浏览器，该浏览器旨在防止指纹。

- [Tor浏览器 :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Protections provided by bridges

Tor bridges are commonly touted as an alternative method to hiding Tor usage from an ISP, instead of a VPN (as we suggest using if possible). Something to consider is that while bridges may provide adequate censorship circumvention, this is only a *transient* benefit. They do not adequately protect you from your ISP discovering you connected to Tor in the *past* with historical traffic log analysis.

To illustrate this point, consider the following scenario: You connect to Tor via a bridge, and your ISP doesn’t detect it because they are not doing sophisticated analysis of your traffic, so things are working as intended. Now, 4 months go by, and the IP of your bridge has been made public. This is a very common occurrence with bridges, they are discovered and blocked relatively frequently, just not immediately.

Your ISP wants to identify Tor users 4 months ago, and with their limited metadata logging they can see that you connected to an IP address which was later revealed to be a Tor bridge. You have virtually no other excuse to be making such a connection, so the ISP can say with very high confidence that you were a Tor user at that time.

Contrast this with our recommended scenario, where you connect to Tor via a VPN. Say that 4 months later your ISP again wants to identify anybody who used Tor 4 months ago. Their logs almost certainly can identify your traffic 4 months ago, but all they would likely be able to see is that you connected to a VPN’s IP address. This is because most ISPs only retain metadata over long periods of time, not the full contents of the traffic you request. Storing the entirety of your traffic data would require a massive quantity of storage which nearly all threat actors wouldn't possess.

Because your ISP almost certainly is not capturing all packet-level data and storing it forever, they have no way of determining what you connected to with that VPN *after* the fact with an advanced technique like deep packet inspection, and therefore you have plausible deniability.

Therefore, bridges provide the most benefit when circumventing internet censorship *in the moment*, but they are not an adequate substitute for **all** the benefits that using a VPN alongside Tor can provide. Again, this is not advice *against* using Tor bridges, you should just be aware of these limitations while making your decision. In some cases bridges may be the *only* option (if all VPN providers are blocked, for instance), so you can still use them in those circumstances with this limitation in mind.

If you think that a bridge can aid in defending against fingerprinting or other advanced network analysis more than a VPN's encrypted tunnel already can, you always have the option to use a bridge in conjunction with a VPN as well. That way you are still protected by the pluggable transport's obfuscation techniques even if an adversary gains some level of visibility into your VPN tunnel. If you decide to go this route, we recommend connecting to an obfs4 bridge behind your VPN for optimal fingerprinting protection, rather than meek or Snowflake.

It is [possible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) that the [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) pluggable transport currently being trialed may mitigate some of these concerns. We will continue to keep an eye on that technology as it develops.

## 其它资源

- [Tor浏览器用户手册](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://youtube.com/watch?v=QRYzre4bf7I) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://youtube.com/watch?v=lVcbq_a5N9I) <small>(YouTube)</small>

[^1]: 您线路上的第一个中继称为“入口警卫“或“警卫”。 它是一个快速而稳定的中继，会在2-3个月内持续作为你的线路的第一个中继，以防止已知的破坏匿名性的攻击。 你的线路其余部分会随着你访问的每个新网站而改变，所有这些中继器一起提供Tor的全部隐私保护。 关于警卫中继器如何工作的更多信息，请参阅这篇 [博文](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) 和 [关于入口警卫的论文](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf)。 ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2))

[^2]: 中继标志：由目录权限分配并在目录协议规范中进一步定义的线路位置（例如， “Guard”、“Exit”、“BadExit” ）、线路属性（例如， “Fast”、“Stable” ）或角色（例如， “Authority”、“HSDir” ）的中继的特殊（ dis- ）限定。 ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
