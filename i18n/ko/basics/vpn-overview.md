---
meta_title: "How Do VPNs Protect Your Privacy? Our VPN Overview - Privacy Guides"
title: VPN 개요
icon: 자료/Vpn
description: Virtual Private Networks shift risk away from your ISP to a third-party you trust. 이러한 사항을 염두해 두셔야 합니다.
---

Virtual Private Networks are a way of extending the end of your network to exit somewhere else in the world.

Normally, an ISP can see the flow of internet traffic entering and exiting your network termination device (i.e. modem). Encryption protocols such as HTTPS are commonly used on the internet, so they may not be able to see exactly what you're posting or reading, but they can get an idea of the [domains you request](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

Using a VPN hides even this information from your ISP, by shifting the trust you place in your network to a server somewhere else in the world. As a result, the ISP then only sees that you are connected to a VPN and nothing about the activity that you're passing through it.

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

When we refer to "Virtual Private Networks" on this website, we are usually referring to **commercial** [VPN providers](../vpn.md), who you pay a monthly fee to in exchange for routing your internet traffic securely through their public servers. There are many other forms of VPN, such as ones you host yourself or ones operated by workplaces which allow you to securely connect to internal/employee network resources, however, these VPNs are usually designed for accessing remote networks securely, rather than protecting the privacy of your internet connection.

</div>

## VPN은 어떻게 작동하나요?

VPNs encrypt your traffic between your device and a server owned by your VPN provider. From the perspective of anyone between you and the VPN server, it looks like you're connecting to the VPN server. From the perspective of anyone between the VPN server and your destination site, all they can see is the VPN server connecting to the website.

``` mermaid
flowchart LR
 763931["Your Device<div>(with VPN Client)</div>"] ===|"VPN Encryption"| 404512{"VPN Server"}
 404512 -.-|"No VPN Encryption"| 593753((("The Internet\n(Your Destination)")))
 subgraph 763931["Your Device<div>(with VPN Client)</div>"]
 end
```

Note that a VPN does not add any security or encryption to your traffic between the VPN server and your destination on the internet. To access a website securely you **must** still ensure HTTPS is in use regardless of whether you use a VPN.

## VPN을 사용해야 하나요?

**Yes**, almost certainly. A VPN has many advantages, including:

1. Hiding your traffic from **only** your Internet Service Provider.
1. Hiding your downloads (such as torrents) from your ISP and anti-piracy organizations.
1. Hiding your IP from third-party websites and services, helping you blend in and preventing IP based tracking.
1. Allowing you to bypass geo-restrictions on certain content.

VPNs can provide *some* of the same benefits Tor provides, such as hiding your IP from the websites you visit and geographically shifting your network traffic, and good VPN providers will not cooperate with e.g. legal authorities from oppressive regimes, especially if you choose a VPN provider outside your own jurisdiction.

VPNs cannot encrypt data outside the connection between your device and the VPN server. VPN providers can also see and modify your traffic the same way your ISP could, so there is still a level of trust you are placing in them. And there is no way to verify a VPN provider's "no logging" policies in any way.

## When isn't a VPN suitable?

Using a VPN in cases where you're using your [real-life or well-known identity](common-misconceptions.md#complicated-is-better) online is unlikely to be useful. Doing so may trigger spam and fraud detection systems, such as if you were to log into your bank's website.

It's important to remember that a VPN will not provide you with absolute anonymity, because the VPN provider itself will still see your real IP address, destination website information, and often has a money trail that can be linked directly back to you. You can't rely on "no logging" policies to protect your data from anyone who is able to protect. If you need complete safety from the network itself, consider using [Tor](../advanced/tor-overview.md) in addition to or instead of a VPN.

You also should not trust a VPN to secure your connection to an unencrypted, HTTP destination. In order to keep what you actually do on the websites you visit private and secure, you must use HTTPS. This will keep your passwords, session tokens, and queries safe from the VPN provider and other potential adversaries in between the VPN server and your destination. You should enable HTTPS-only mode in your browser (if it's supported) to mitigate attacks which try to downgrade your connection from HTTPS to HTTP.

## Should I use encrypted DNS with a VPN?

Unless your VPN provider hosts the encrypted DNS servers themselves, **probably not**. Using DOH/DOT (or any other form of encrypted DNS) with third-party servers will simply add more entities to trust. Your VPN provider can still see which websites you visit based on the IP addresses and other methods. All this being said, there may be some advantages to enabling encrypted DNS in order to enable other security features in your browser, such as ECH. Browser technologies which are reliant on in-browser encrypted DNS are relatively new and not yet widespread, so whether they are relevant to you in particular is an exercise we will leave to you to research independently.

Another common reason encrypted DNS is recommended is that it prevents DNS spoofing. However, your browser should already be checking for [TLS certificates](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) with **HTTPS** and warn you about it. If you are not using **HTTPS**, then an adversary can still just modify anything other than your DNS queries and the end result will be little different.

## Tor를 사용할 때에도 VPN을 사용해야 하나요?

Maybe, Tor is not necessarily suitable for everybody in the first place. Consider your [threat model](threat-modeling.md), because if your adversary is not capable of extracting information from your VPN provider, using a VPN alone may provide enough protection.

If you do use Tor then you are *probably* best off connecting to the Tor network via a commercial VPN provider. However, this is a complex subject which we've written more about on our [Tor overview](../advanced/tor-overview.md) page.

## Should I access Tor through VPN providers that provide "Tor nodes"?

You should not use that feature: The primary advantage of using Tor is that you do not trust your VPN provider, which is negated when you use Tor nodes hosted by your VPN instead of connecting directly to Tor from your computer.

Currently, Tor only supports the TCP protocol. UDP (used by [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3), and other protocols), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol), and other packets will be dropped. To compensate for this, VPN providers typically will route all non-TCP packets through their VPN server (your first hop). This is the case with [ProtonVPN](https://protonvpn.com/support/tor-vpn). Additionally, when using this Tor over VPN setup, you do not have control over other important Tor features such as [Isolated Destination Address](https://whonix.org/wiki/Stream_Isolation) (using a different Tor circuit for every domain you visit).

The feature should be viewed as a *convenient* way to access hidden services on Tor, not to stay anonymous. For proper anonymity, use the actual [Tor Browser](../tor.md).

## Commercial VPN Ownership

Most VPN services are owned by the same [few companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies). These shady companies run lots of smaller VPN services to create the illusion that you have more choice than you actually do and to maximize profit. Typically, these providers that feed into their shell company have terrible privacy policies and shouldn't be trusted with your internet traffic. You should be very strict about which provider you decide to use.

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

Another consideration is legal liability. 출구 노드는 네트워크 오용으로 인한 법적 문제를 해결해야 하며, 이는 Tor 네트워크가 존재해온 내내 논란이 되어온 문제입니다. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

많은 dVPN이 최고의 서비스를 제공하기보다는 암호화폐를 홍보하는 데 사용됩니다. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## VPN 관련 추가 정보

- [(영문) VPN 및 프라이버시 리뷰 사이트의 문제점](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [(영문) 무료 VPN 앱 조사 내용](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [(영문) 드러나지 않았던 VPN 운영의 실체: 단 23개의 회사가 101개 VPN 제품을 운영하고 있습니다](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [(영문) 인기 앱 24개에 파고들어 위험한 권한을 요구하고 있는 어떤 중국 회사](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - a Very Precarious Narrative](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) by Dennis Schubert
