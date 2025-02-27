---
title: "Tor 개요"
icon: 'simple/torproject'
description: Tor는 무료로 이용 가능한 탈중앙화 네트워크입니다. 최대한 프라이버시를 보호하면서 인터넷을 이용할 수 있도록 설계되었습니다.
---

![Tor 로고](../assets/img/self-contained-networks/tor.svg){ align=right }

[**Tor**](../alternative-networks.md#tor) is a free to use, decentralized network designed for using the internet with as much privacy as possible. Tor 네트워크를 올바르게 사용하면 비공개 및 익명 웹 탐색과 커뮤니케이션이 가능합니다. Tor 트래픽은 차단 및 추적이 어렵기 때문에 검열 우회에 효과적입니다.

Tor works by routing your internet traffic through volunteer-operated servers, instead of making a direct connection to the site you're trying to visit. 이러한 방식을 통해 트래픽의 출처를 알 수 없게 만들고, 연결 경로상의 서버 또한 트래픽의 전체 경로는 볼 수 없으므로, 연결에 사용한 서버조차도 여러분의 익명성을 깨트릴 수 없습니다.

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

## Clearnet 서비스 경로 구축 방식

클리어넷(Clearnet) 서비스란, 모든 브라우저로 접근 가능한 웹사이트(예시: [privacyguides.org](https://www.privacyguides.org))를 말합니다. 클리어넷 서비스의 동의어로 '표면 웹(Surface Web)'이 쓰이기도 합니다. Tor는 '노드'(혹은 '릴레이')라고 하는 자원 봉사 운영 서버 수천 개로 구성된 네트워크를 통해 트래픽을 라우팅하여, 웹사이트를 익명으로 연결할 수 있도록 합니다.

여러분이 [Tor에 연결할](../tor.md) 때마다 3개의 노드가 선택되어 인터넷 연결 경로를 구축합니다. 이 경로를 '우회로(Circuit)'라고 합니다.

<figure markdown>
  ![여러분의 기기가 목적지 웹사이트에 도달하기까지 거쳐가는 입구 노드, 중간 노드, 출구 노드를 나타내는 Tor 경로](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![여러분의 기기가 목적지 웹사이트에 도달하기까지 거쳐가는 입구 노드, 중간 노드, 출구 노드를 나타내는 Tor 경로](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Tor 우회 경로</figcaption>
</figure>

노드는 각각 다른 역할을 가지고 있습니다.

### 입구 노드

입구 노드(Entry Node)는 Tor 클라이언트가 연결되는 첫 번째 노드입니다. 진입 노드/가드 노드(Guard Node)라고 불리기도 합니다. 입구 노드는 사용자의 IP 주소를 볼 수 있으나, 사용자가 어디에 연결하는지는 알 수 없습니다.

다른 노드와 달리, Tor 클라이언트는 여러분을 특정 공격으로부터 보호하기 위해 무작위로 입구 노드를 선택하여 2~3개월간 해당 노드를 유지합니다.

### 중간 노드

중간 노드(Middle Node)는 Tor 클라이언트가 연결되는 두 번째 노드입니다. 중간 노드는 트래픽이 어디서 왔는지, 즉 어떤 입구 노드에서 왔는지, 그리고 다음으로는 어떤 노드로 가는지 알 수 있습니다. 중간 노드는 사용자의 IP 주소 혹은 사용자가 연결하고자 하는 도메인은 알 수 없습니다.

중간 노드는 우회로를 새로 생성할 때마다 사용 가능한 모든 Tor 노드 중에서 무작위로 선택됩니다.

### 출구 노드

출구 노드(Exit Node)는 웹 트래픽이 Tor 네트워크를 벗어나, 사용자가 원하는 목적지로 전달되는 지점입니다. 출구 노드는 사용자의 IP 주소를 볼 수 없으나, 어떤 사이트에 연결하고 있는지는 알 수 있습니다.

출구 노드는 출구 릴레이 플래그로 실행된 모든 사용 가능한 Tor 노드 중에서 무작위로 선택됩니다.

## Onion 서비스 경로 구축 방식

'Onion 서비스'('Hidden 서비스'라고도 불립니다)는 Tor 브라우저로만 접근 가능한 웹사이트입니다. Onion 서비스 도메인은 랜덤으로 생성된 긴 문자열로 되어있으며, `.onion`으로 끝납니다.

Tor에서 Onion 서비스로의 연결은 클리어넷 서비스 연결과 매우 유사하게 작동하지만, 트래픽은 목적지 서버에 도달하기 전에 총 **6개**의 노드를 거쳐 라우팅됩니다. 단, 앞선 내용과 마찬가지로 *사용자의 익명성*에 기여하는 노드는 이 중 3개 뿐이며, 나머지 노드 3개는 *Onion 서비스의 익명성*을 보호합니다. 즉, Tor 브라우저가 사용자의 IP와 주소를 숨기는 것과 동일한 방식으로 웹사이트의 실제 IP와 주소를 숨깁니다.

<figure style="width:100%" markdown>
  ![3개의 Tor 노드에 더해 웹사이트 신원을 숨기는 3개의 Tor 노드를 추가로 거쳐가는 트래픽을 나타내는 Tor 경로](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![3개의 Tor 노드에 더해 웹사이트 신원을 숨기는 3개의 Tor 노드를 추가로 거쳐가는 트래픽을 나타내는 Tor 경로](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Onion 서비스 Tor 우회 경로 <span class="pg-blue">파란색</span> 테두리 내 노드는 사용자 브라우저에 해당하며, <span class="pg-red">빨간색</span> 테두리 내 노드는 서버에 해당합니다. 이리하여 서버의 신원은 노출되지 않습니다.</figcaption>
</figure>

## 암호화

Tor는 각 패킷(전송되는 데이터 덩어리)을 출구, 중간, 입구 노드 순서대로 키를 3 번 암호화합니다.

Tor 우회로가 구축되고 나면 데이터 전송은 다음과 같이 이루어집니다:

1. 먼저, 패킷이 입구 노드에 도착하면 첫 번째 암호화 레이어가 제거됩니다. 입구 노드는 해당 암호화 패킷에서 중간 노드 주소가 포함된 또 다른 암호화 패킷을 찾습니다. 이후, 입구 노드는 중간 노드로 패킷을 전송합니다.

2. 다음으로, 중간 노드가 입구 노드로부터 패킷을 수신하면 마찬가지로 키를 이용해 암호화 레이어를 제거합니다. 이번에는 출구 노드 주소가 포함된 암호화 패킷을 찾습니다. 이후, 중간 노드는 출구 노드로 패킷을 전송합니다.

3. 마지막으로, 출구 노드가 패킷을 수신하면 해당 키로 마지막 암호화 레이어를 제거합니다. 출구 노드는 목적지 주소를 확인하고 해당 주소로 패킷을 전송합니다.

다음은 이 과정을 다이어그램으로 나타낸 것입니다. 각 노드는 해당 노드의 암호화 레이어를 제거하며, 목적지 서버가 데이터를 반환할 경우 이와 동일한 과정이 정반대로 진행됩니다. 예를 들어, 출구 노드는 사용자가 누구인지는 알 수 없으나 어떤 노드에서 전송해왔는지는 알고 있으므로 자체 암호화 레이어를 추가하여 전송합니다.

<figure markdown>
  ![Tor 암호화](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor 암호화](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Tor 네트워크를 통한 데이터 송수신</figcaption>
</figure>

Tor를 이용하면 단일 주체에게 전체 경로를 노출하지 않고도 서버에 연결 가능합니다. 입구 노드는 사용자가 누구인지는 알지만 목적지는 알 수 없고, 중간 노드는 사용자와 목적지 모두 알 수 없으며, 출구 노드는 목적지는 알지만 사용자가 누구인지는 알 수 없습니다. 최종 연결이 생성되는 지점은 출구 노드이므로, 목적지 서버는 사용자의 IP 주소를 절대 알 수 없습니다.

## 주의 사항

Tor는 강력한 프라이버시를 보장하지만, 완벽하지는 않습니다:

- Tor never protects you from exposing yourself by mistake, such as if you share too much information about your real identity.
- Tor exit nodes can **modify** unencrypted traffic which passes through them. This means traffic which is not encrypted, such as plain HTTP traffic, can be changed by a malicious exit node. **Never** download files from an unencrypted `http://` website over Tor, and ensure your browser is set to always upgrade HTTP traffic to HTTPS.
- Tor 출구 노드가 직접 트래픽을 모니터링하고 있을 수도 있습니다. Unencrypted traffic which contains personally identifiable information can deanonymize you to that exit node. Again, we recommend only using HTTPS over Tor.
- Powerful adversaries with the capability to passively watch *all* network traffic around the globe ("Global Passive Adversaries") are **not** something that Tor protects you against (and using Tor [with a VPN](#safely-connecting-to-tor) doesn't change this fact).
- Well-funded adversaries with the capability to passively watch *most* network traffic around the globe still have a *chance* of deanonymizing Tor users by means of advanced traffic analysis.

웹 탐색 용도로 Tor를 이용하고자 하실 경우, 핑거프린팅을 방지하도록 설계된 **공식** Tor 브라우저만 사용하실 것을 권장드립니다.

- [Tor 브라우저 :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Protections provided by bridges

Tor bridges are commonly touted as an alternative method to hiding Tor usage from an ISP, instead of a VPN (as we suggest using if possible). Something to consider is that while bridges may provide adequate censorship circumvention, this is only a *transient* benefit. They do not adequately protect you from your ISP discovering you connected to Tor in the *past* with historical traffic log analysis.

To illustrate this point, consider the following scenario: You connect to Tor via a bridge, and your ISP doesn’t detect it because they are not doing sophisticated analysis of your traffic, so things are working as intended. Now, 4 months go by, and the IP of your bridge has been made public. This is a very common occurrence with bridges, they are discovered and blocked relatively frequently, just not immediately.

Your ISP wants to identify Tor users 4 months ago, and with their limited metadata logging they can see that you connected to an IP address which was later revealed to be a Tor bridge. You have virtually no other excuse to be making such a connection, so the ISP can say with very high confidence that you were a Tor user at that time.

Contrast this with our recommended scenario, where you connect to Tor via a VPN. Say that 4 months later your ISP again wants to identify anybody who used Tor 4 months ago. Their logs almost certainly can identify your traffic 4 months ago, but all they would likely be able to see is that you connected to a VPN’s IP address. This is because most ISPs only retain metadata over long periods of time, not the full contents of the traffic you request. Storing the entirety of your traffic data would require a massive quantity of storage which nearly all threat actors wouldn't possess.

Because your ISP almost certainly is not capturing all packet-level data and storing it forever, they have no way of determining what you connected to with that VPN *after* the fact with an advanced technique like deep packet inspection, and therefore you have plausible deniability.

Therefore, bridges provide the most benefit when circumventing internet censorship *in the moment*, but they are not an adequate substitute for **all** the benefits that using a VPN alongside Tor can provide. Again, this is not advice *against* using Tor bridges, you should just be aware of these limitations while making your decision. In some cases bridges may be the *only* option (if all VPN providers are blocked, for instance), so you can still use them in those circumstances with this limitation in mind.

If you think that a bridge can aid in defending against fingerprinting or other advanced network analysis more than a VPN's encrypted tunnel already can, you always have the option to use a bridge in conjunction with a VPN as well. That way you are still protected by the pluggable transport's obfuscation techniques even if an adversary gains some level of visibility into your VPN tunnel. If you decide to go this route, we recommend connecting to an obfs4 bridge behind your VPN for optimal fingerprinting protection, rather than meek or Snowflake.

It is [possible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) that the [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) pluggable transport currently being trialed may mitigate some of these concerns. We will continue to keep an eye on that technology as it develops.

## 추가 자료

- [Tor 브라우저 사용자 설명서](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://youtube.com/watch?v=QRYzre4bf7I) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://youtube.com/watch?v=lVcbq_a5N9I) <small>(YouTube)</small>

[^1]: 우회로의 첫 번째 릴레이는 'Entry Guard' 혹은 'Guard'라고 합니다. 알려진 익명성 침해 공격으로부터 보호하기 위해, 우회로에서 첫 번째 릴레이로 2~3개월간 유지되는 빠르고 안정적인 릴레이입니다. 우회로의 나머지 경로는 새로운 웹사이트를 방문할 때마다 변경되며, 이러한 릴레이가 모두 모여 Tor의 완벽한 프라이버시 보호를 제공합니다. 보다 자세한 가드 릴레이 작동 방식 설명은 [이 블로그 포스트](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters)와 [이 논문](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf)을 참고해 주세요. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2))

[^2]: '릴레이 플래그'란 우회로 위치(Guard, Exit, BadExit 등), 우회로 속성(Fast, Stable 등), 역할(Authority, HSDir 등) 같은 릴레이의 특수 자격을 말합니다. 이는 Directory Authority에 의해 할당되며, Directory Protocol 사양에 추가로 정의되어 있습니다. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
