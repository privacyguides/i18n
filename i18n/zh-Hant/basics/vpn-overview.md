---
meta_title: "VPN如何保護您的隱私？ VPN概述 - Privacy Guides"
title: VPN 簡介
icon: material/vpn
description: 虛擬私用網路將風險從您的ISP 轉移到您信任的第三方。 你應該記住這些事情。
---

Virtual Private Networks are a way of extending the end of your network to exit somewhere else in the world.

Normally, an ISP can see the flow of internet traffic entering and exiting your network termination device (i.e. modem). Encryption protocols such as HTTPS are commonly used on the internet, so they may not be able to see exactly what you're posting or reading, but they can get an idea of the [domains you request](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

Using a VPN hides even this information from your ISP, by shifting the trust you place in your network to a server somewhere else in the world. As a result, the ISP then only sees that you are connected to a VPN and nothing about the activity that you're passing through it.

!!! note "備註"

    When we refer to "Virtual Private Networks" on this website, we are usually referring to **commercial** [VPN providers](../vpn.md), who you pay a monthly fee to in exchange for routing your internet traffic securely through their public servers. There are many other forms of VPN, such as ones you host yourself or ones operated by workplaces which allow you to securely connect to internal/employee network resources, however, these VPNs are usually designed for accessing remote networks securely, rather than protecting the privacy of your internet connection.

## How does a VPN work?

VPNs encrypt your traffic between your device and a server owned by your VPN provider. From the perspective of anyone between you and the VPN server, it looks like you're connecting to the VPN server. From the perspective of anyone between the VPN server and your destination site, all they can see is the VPN server connecting to the website.

``` mermaid
flowchart LR
 763931["Your Device<div>(with VPN Client)</div>"] ===|"VPN Encryption"| 404512{"VPN Server"}
 404512 -.-|"No VPN Encryption"| 593753((("The Internet\n(Your Destination)")))
 subgraph 763931["Your Device<div>(with VPN Client)</div>"]
 end
```

Note that a VPN does not add any security or encryption to your traffic between the VPN server and your destination on the internet. To access a website securely you **must** still ensure HTTPS is in use regardless of whether you use a VPN.

## 我應該使用 VPN 嗎？

**Yes**, almost certainly. A VPN has many advantages, including:

1. **僅需**對網路連線服務商隱藏您的流量 。
1. 對 ISP 和反盜版組織隱藏您的下載（如 torrents）。
1. Hiding your IP from third-party websites and services, helping you blend in and preventing IP based tracking.
1. Allowing you to bypass geo-restrictions on certain content.

VPNs can provide *some* of the same benefits Tor provides, such as hiding your IP from the websites you visit and geographically shifting your network traffic, and good VPN providers will not cooperate with e.g. legal authorities from oppressive regimes, especially if you choose a VPN provider outside your own jurisdiction.

VPNs cannot encrypt data outside the connection between your device and the VPN server. VPN providers can also see and modify your traffic the same way your ISP could, so there is still a level of trust you are placing in them. 而且沒有方式可以驗證 VPN 提供商的“無記錄”政策是否貫徹。

## When isn't a VPN suitable?

Using a VPN in cases where you're using your [real-life or well-known identity](common-misconceptions.md#complicated-is-better) online is unlikely be useful. 這樣做可能會觸發垃圾郵件和欺詐偵測系統，例如您正試圖登入銀行網站。

It's important to remember that a VPN will not provide you with absolute anonymity, because the VPN provider itself will still see your real IP address, destination website information, and often has a money trail that can be linked directly back to you. You can't rely on "no logging" policies to protect your data from anyone who is able to protect. If you need complete safety from the network itself, consider using [Tor](../advanced/tor-overview.md) in addition to or instead of a VPN.

You also should not trust a VPN to secure your connection to an unencrypted, HTTP destination. 為了保持所瀏覽網站活動的私密和安全，您必須使用 HTTPS。 This will keep your passwords, session tokens, and queries safe from the VPN provider and other potential adversaries in between the VPN server and your destination. You should enable HTTPS-only mode in your browser (if it's supported) to mitigate attacks which try to downgrade your connection from HTTPS to HTTP.

## 我應該將加密 DNS 與 VPN 一起使用嗎？

Unless your VPN provider hosts the encrypted DNS servers themselves, **probably not**. Using DOH/DOT (or any other form of encrypted DNS) with third-party servers will simply add more entities to trust. 您的 VPN 提供商仍可以根據 IP 地址和其他方法查看您訪問的網站。 All this being said, there may be some advantages to enabling encrypted DNS in order to enable other security features in your browser, such as ECH. Browser technologies which are reliant on in-browser encrypted DNS are relatively new and not yet widespread, so whether they are relevant to you in particular is an exercise we will leave to you to research independently.

Another common reason encrypted DNS is recommended is that it prevents DNS spoofing. 您的瀏覽器應該已經檢查了 [TLS 憑證](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) 和 **HTTPS** ，並警告您。 如果沒用 **HTTPS**，則對手可以修改您的 DNS 查詢之外的任何東西，最終結果將沒太大差異。

## 我應該*同時* 使用 Tor 與 VPN 嗎？

Maybe, Tor is not necessarily suitable for everybody in the first place. Consider your [threat model](threat-modeling.md), because if your adversary is not capable of extracting information from your VPN provider, using a VPN alone may provide enough protection.

If you do use Tor then you are *probably* best off connecting to the Tor network via a commercial VPN provider. However, this is a complex subject which we've written more about on our [Tor overview](../advanced/tor-overview.md) page.

## Should I access Tor through VPN providers that provide "Tor nodes"?

You should not use that feature: The primary advantage of using Tor is that you do not trust your VPN provider, which is negated when you use Tor nodes hosted by your VPN instead of connecting directly to Tor from your computer.

Currently, Tor only supports the TCP protocol. UDP (used by [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3), and other protocols), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol), and other packets will be dropped. 為了彌補這一點， VPN 提供商通常會引導全部的non-TCP 封包通過他們的 VPN 伺服器（您的第一個跳）。 [ProtonVPN ](https://protonvpn.com/support/tor-vpn/)的情況就是如此。 此外，使用此 Tor over VPN 設定時，您無法控制 Tor 其他重要的功能，例如 [隔離目標位址](https://www.whonix.org/wiki/Stream_Isolation) （為您訪問不同網域使用不同的Tor 迴路）。

The feature should be viewed as a *convenient* way to access hidden services on Tor, not to stay anonymous. For proper anonymity, use the actual [Tor Browser](../tor.md).

## Commercial VPN Ownership

Most VPN services are owned by the same [few companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/). These shady companies run lots of smaller VPN services to create the illusion that you have more choice than you actually do and to maximize profit. Typically, these providers that feed into their shell company have terrible privacy policies and shouldn't be trusted with your internet traffic. You should be very strict about which provider you decide to use.

You should also be wary that many VPN review sites are merely advertising vehicles open to the highest bidder. ==Privacy Guides does not make money from recommending external products, and never uses affiliate programs.==

[Our VPN Recommendations](../vpn.md ""){.md-button}

## Modern VPN Alternatives

Recently, some attempts have been made by various organizations to address some issues which centralized VPNs have. These technologies are relatively new, but worth keeping an eye on as the field develops.

### Multi-Party Relays

Multi-Party Relays (MPRs) use multiple nodes owned by different parties, such that no individual party knows both who you are and what you're connecting to. This is the basic idea behind Tor, but now there are some paid services that try to emulate this model.

MPRs seek to solve a problem inherent to VPNs: the fact that you must trust them completely. They accomplish this goal by segmenting the responsibilities between two or more different companies. For example, Apple's iCloud+ Private Relay routes your traffic through two servers:

1. Firstly, a server operated by Apple.

    This server is able to see your device's IP when you connect to it, and has knowledge of your payment information and Apple ID tied to your iCloud subscription. However, it is unable to see what website you are connecting to.

2. Secondly, a server operated by a partner CDN, such as Cloudflare or Fastly.

    This server actually makes the connection to your destination website, but has no knowledge of your device. The only IP address it knows about is Apple's server's.

Other MPRs run by different companies like Google or INVISV operate in a very similar manner. This protection by segmentation only exists if you trust the two companies to not collude with each other to deanonymize you.

### Decentralized VPNs

Another attempt at solving the issues with centralized VPN services are dVPNs. These are based on blockchain technology and claim to eliminate trust in a single party by distributing the nodes across lots of different people. However, many times a dVPN will default to a single node, meaning you need to trust that node completely, just like a traditional VPN. Unlike a traditional VPN, this one node that can see all your traffic is a random person instead of your VPN provider that can be audited and has legal responsibilities to uphold their privacy policy. Multi-hop is needed to solve this, but that comes with a stability and performance cost.

Another consideration is legal liability. The exit node will need to deal with legal problems from misuse of the network, an issue that the Tor network has contended with for its entire existence. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

Many dVPNs are used to push a cryptocurrency rather than to make the best service. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## VPN 相關資訊

- [VPN 問題和隱私評論網站](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites/)
- [免費 VPN 應用程式調查](https://www.top10vpn.com/free-vpn-app-investigation/)
- [揭露隱身的 VPN 擁有者：由 23 家公司運營101款 VPN 產品](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/)
- [這家中國公司祕密支持24個尋求危險權限的流行應用程序](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions/)
- [VPN - a Very Precarious Narrative](https://schub.io/blog/2019/04/08/very-precarious-narrative.html) by Dennis Schubert
