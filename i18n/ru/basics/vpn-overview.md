---
meta_title: "How Do VPNs Protect Your Privacy? Our VPN Overview - Privacy Guides"
title: Обзор VPN
icon: material/vpn
description: Virtual Private Networks shift risk away from your ISP to a third-party you trust. You should keep these things in mind.
---

Виртуальные частные сети позволяют перенести выход вашей сети в любую точку мира.

[:material-movie-open-play-outline: Нужен ли вам VPN?](https://www.privacyguides.org/videos/2024/12/12/do-you-need-a-vpn ""){.md-button}

Обычно провайдер может видеть поток интернет-трафика, входящего и выходящего сетевого устройства (т.е. модема). В интернете широко используются протоколы шифрования, такие как HTTPS, поэтому интернет-провайдеры не могут видеть, что именно Вы публикуете или читаете, но они могут получить представление о [посещаемых вами доменах](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

VPN скрывает даже эту информацию от Вашего провайдера, перенося точку выхода на сервер в другой точке мира. В результате провайдер видит только то, что Вы подключены к VPN, и не знает, что Вы делаете через VPN.

<div class="admonition note" markdown>
<p class="admonition-title">Примечание</p>

When we refer to "Virtual Private Networks" on this website, we are usually referring to **commercial** [VPN providers](../vpn.md), who you pay a monthly fee to in exchange for routing your internet traffic securely through their public servers. There are many other forms of VPN, such as ones you host yourself or ones operated by workplaces which allow you to securely connect to internal/employee network resources, however, these VPNs are usually designed for accessing remote networks securely, rather than protecting the privacy of your internet connection.

</div>

## Как работает VPN?

VPNs encrypt your traffic between your device and a server owned by your VPN provider. From the perspective of anyone between you and the VPN server, it looks like you're connecting to the VPN server. From the perspective of anyone between the VPN server and your destination site, all they can see is the VPN server connecting to the website.

``` mermaid
flowchart LR
 763931["Ваше устройство<div>(клиент VPN)</div>"] ===|"Шифрование VPN"| 404512{"Сервер VPN"}
 404512 -.-|"Без шифрования VPN"| 593753(("Интернет<div>(Пункт назначения)</div>"))
 subgraph 763931["Ваше устройство<div>(Клиент VPN)</div>"]
 end
```

Note that a VPN does not add any security or encryption to your traffic between the VPN server and your destination on the internet. To access a website securely you **must** still ensure HTTPS is in use regardless of whether you use a VPN.

## Следует ли мне использовать VPN?

**Да**, почти наверняка. VPN позволяет:

1. Скрывать ваш трафик **только** от вашего интернет-провайдера.
1. Скрывать ваши загрузки (например, торренты) от провайдера и антипиратских организаций.
1. Скрывать ваш IP от сторонних веб-сайтов и служб, маскируясь и предотвращая отслеживание по IP.
1. Обходить гео-ограничения на определённый контент.

VPNs can provide *some* of the same benefits Tor provides, such as hiding your IP from the websites you visit and geographically shifting your network traffic, and good VPN providers will not cooperate with e.g. legal authorities from oppressive regimes, especially if you choose a VPN provider outside your own jurisdiction.

VPNs cannot encrypt data outside the connection between your device and the VPN server. VPN providers can also see and modify your traffic the same way your ISP could, so there is still a level of trust you are placing in them. И нет никакого способа проверить политику VPN-провайдера "без ведения логов".

## Когда не стоит использовать VPN?

Using a VPN in cases where you're using your [real-life or well-known identity](common-misconceptions.md#complicated-is-better) online is unlikely to be useful. Это может привести к срабатыванию систем обнаружения спама и мошенничества, например, если вы зашли на сайт своего банка.

It's important to remember that a VPN will not provide you with absolute anonymity because the VPN provider itself will still have access to your real IP address, destination website information, and often a money trail that can be linked directly back to you. "No logging" policies are merely a promise; if you need complete safety from the network itself, consider using [Tor](../advanced/tor-overview.md) in addition to or instead of a VPN.

You also should not trust a VPN to secure your connection to an unencrypted, HTTP destination. Чтобы сохранить конфиденциальность и безопасность того, что вы делаете на посещаемых вами сайтах, необходимо использовать HTTPS. This will keep your passwords, session tokens, and queries safe from the VPN provider and other potential adversaries in between the VPN server and your destination. You should enable HTTPS-only mode in your browser (if it's supported) to mitigate attacks which try to downgrade your connection from HTTPS to HTTP.

## Нужно ли мне использовать зашифрованный DNS вместе с VPN?

Unless your VPN provider hosts the encrypted DNS servers themselves, **probably not**. Using DOH/DOT (or any other form of encrypted DNS) with third-party servers will simply add more entities to trust. Ваш провайдер VPN все еще может видеть, какие сайты вы посещаете, основываясь на IP-адресах и других методах. All this being said, there may be some advantages to enabling encrypted DNS in order to enable other security features in your browser, such as ECH. Browser technologies which are reliant on in-browser encrypted DNS are relatively new and not yet widespread, so whether they are relevant to you in particular is an exercise we will leave to you to research independently.

Another common reason encrypted DNS is recommended is that it prevents DNS spoofing. Однако ваш браузер уже должен проверять наличие [TLS сертификатов](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) с **HTTPS** и предупреждать вас об этом. Если вы не используете **HTTPS**, то злоумышленник все равно может просто модифицировать что угодно, кроме ваших DNS-запросов, и конечный результат будет немного отличаться.

## Следует ли мне использовать Tor *и* VPN?

Maybe, Tor is not necessarily suitable for everybody in the first place. Consider your [threat model](threat-modeling.md), because if your adversary is not capable of extracting information from your VPN provider, using a VPN alone may provide enough protection.

If you do use Tor then you are *probably* best off connecting to the Tor network via a commercial VPN provider. However, this is a complex subject which we've written more about on our [Tor overview](../advanced/tor-overview.md) page.

## Should I access Tor through VPN providers that provide "Tor nodes"?

You should not use that feature: The primary advantage of using Tor is that you do not trust your VPN provider, which is negated when you use Tor nodes hosted by your VPN instead of connecting directly to Tor from your computer.

Currently, Tor only supports the TCP protocol. UDP (used by [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3), and other protocols), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol), and other packets will be dropped. Чтобы компенсировать это, провайдеры VPN обычно направляют все пакеты, не относящиеся к TCP, через свой VPN-сервер (первый путь вашего трафика). This is the case with [ProtonVPN](https://protonvpn.com/support/tor-vpn). Additionally, when using this Tor over VPN setup, you do not have control over other important Tor features such as [Isolated Destination Address](https://whonix.org/wiki/Stream_Isolation) (using a different Tor circuit for every domain you visit).

The feature should be viewed as a *convenient* way to access hidden services on Tor, not to stay anonymous. For proper anonymity, use the actual [Tor Browser](../tor.md).

## Commercial VPN Ownership

Most VPN services are owned by the same [few companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies). These shady companies run lots of smaller VPN services to create the illusion that you have more choice than you actually do and to maximize profit. Typically, these providers that feed into their shell company have terrible privacy policies and shouldn't be trusted with your internet traffic. You should be very strict about which provider you decide to use.

You should also be wary that many VPN review sites are merely advertising vehicles open to the highest bidder. ==Privacy Guides does not make money from recommending external products, and never uses affiliate programs.==

[Our VPN Recommendations](../vpn.md ""){.md-button}

## Modern VPN Alternatives

Recently, some attempts have been made by various organizations to address some issues which centralized VPNs have. These technologies are relatively new, but worth keeping an eye on as the field develops.

### Multi-Party Relays

Multi-Party Relays (MPRs) use multiple nodes owned by different parties, such that no individual party knows both who you are and what you're connecting to. This is the basic idea behind Tor, but now there are some paid services that try to emulate this model.

MPRs seek to solve a problem inherent to VPNs: the fact that you must trust them completely. They accomplish this goal by segmenting the responsibilities between two or more different companies.

One example of a commercially available MPR is Apple's iCloud+ Private Relay, which routes your traffic through two servers:

1. Firstly, a server operated by Apple.

    This server is able to see your device's IP when you connect to it, and has knowledge of your payment information and Apple ID tied to your iCloud subscription. However, it is unable to see what website you are connecting to.

2. Secondly, a server operated by a partner CDN, such as Cloudflare or Fastly.

    This server actually makes the connection to your destination website, but has no knowledge of your device. The only IP address it knows about is Apple's server's.

Other MPRs run by different companies operate in a very similar manner. This protection by segmentation only exists if you trust the two companies to not collude with each other to deanonymize you.

### Decentralized VPNs

Another attempt at solving the issues with centralized VPN services are dVPNs. These are based on blockchain technology and claim to eliminate trust in a single party by distributing the nodes across lots of different people. However, many times a dVPN will default to a single node, meaning you need to trust that node completely, just like a traditional VPN. Unlike a traditional VPN, this one node that can see all your traffic is a random person instead of your VPN provider that can be audited and has legal responsibilities to uphold their privacy policy. Multi-hop is needed to solve this, but that comes with a stability and performance cost.

Another consideration is legal liability. The exit node will need to deal with legal problems from misuse of the network, an issue that the Tor network has contended with for its entire existence. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

Many dVPNs are used to push a cryptocurrency rather than to make the best service. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## Больше информации о VPN

- [The Trouble with VPN and Privacy Review Sites](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [Free VPN App Investigation](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [Hidden VPN owners unveiled: 101 VPN products run by just 23 companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [This Chinese company is secretly behind 24 popular apps seeking dangerous permissions](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - a Very Precarious Narrative](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) by Dennis Schubert
