---
meta_title: "Como As VPNs Protegem Sua Privacidade? Nossa Visão Geral Sobre VPN — Privacy Guides"
title: VPN Overview
icon: material/vpn
description: As Redes Privadas Virtuais transferem o risco do seu ISP para um terceiro em quem você confia. Você deve ter isso em mente.
---

Redes Privadas Virtuais são uma forma de estender o fim da sua conexão para sair de outro lugar do mundo. Um provedor de serviços de internet (ISP) pode ver o fluxo de tráfego da Internet que entra e sai do seu dispositivo de terminação de rede (por exemplo, o modem).

Protocolos de criptografia, como o HTTPS, são frequentemente usados na Internet, de modo que eles não consigam ver exatamente o que você está postando ou lendo, mas eles podem ter uma ideia dos [domínios que você solicita](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

Uma VPN pode ajudar, visto que transfere a confiança para um servidor em outro lugar do mundo. Como resultado, seu provedor de Internet só vê que você está conectado a uma VPN e nada sobre a atividade que você está transmitindo através dela.

## Devo Usar Uma VPN?

**Sim**, a menos que você já esteja usando o Tor. Uma VPN faz duas coisas: transfere os riscos do seu Provedor de Serviços de Internet para você mesmo e oculta seu IP de um serviço de terceiros.

VPNs não podem criptografar dados fora da conexão entre o seu dispositivo e o servidor VPN. Provedores de VPN podem ver e modificar seu tráfego da mesma forma que seu provedor de internet pode. E não há nenhuma maneira de verificar as políticas de "não registro" dos provedores de VPN.

No entanto, eles ocultam seu IP real de um serviço de terceiros, desde que não haja vazamentos de IP. They help you blend in with others and mitigate IP based tracking.

## Quando não deveria usar uma VPN?

Using a VPN in cases where you're using your [known identity](common-threats.md#common-misconceptions) is unlikely be useful.

Doing so may trigger spam and fraud detection systems, such as if you were to log into your bank's website.

## E Quanto à Criptografia?

Encryption offered by VPN providers are between your devices and their servers. It guarantees that this specific link is secure. This is a step up from using unencrypted proxies where an adversary on the network can intercept the communications between your devices and said proxies and modify them. However, encryption between your apps or browsers with the service providers are not handled by this encryption.

In order to keep what you actually do on the websites you visit private and secure, you must use HTTPS. This will keep your passwords, session tokens, and queries safe from the VPN provider. Consider enabling "HTTPS everywhere" in your browser to mitigate downgrade attacks like [SSL Strip](https://www.blackhat.com/presentations/bh-dc-09/Marlinspike/BlackHat-DC-09-Marlinspike-Defeating-SSL.pdf).

## Devo usar DNS criptografado com uma VPN?

Unless your VPN provider hosts the encrypted DNS servers, **no**. Using DOH/DOT (or any other form of encrypted DNS) with third-party servers will simply add more entities to trust and does **absolutely nothing** to improve your privacy/security. Your VPN provider can still see which websites you visit based on the IP addresses and other methods. Instead of just trusting your VPN provider, you are now trusting both the VPN provider and the DNS provider.

A common reason to recommend encrypted DNS is that it helps against DNS spoofing. However, your browser should already be checking for [TLS certificates](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) with **HTTPS** and warn you about it. If you are not using **HTTPS**, then an adversary can still just modify anything other than your DNS queries and the end result will be little different.

Needless to say, **you shouldn't use encrypted DNS with Tor**. This would direct all of your DNS requests through a single circuit and would allow the encrypted DNS provider to deanonymize you.

## Devo usar Tor *e* uma VPN?

By using a VPN with Tor, you're creating essentially a permanent entry node, often with a money trail attached. This provides zero additional benefits to you, while increasing the attack surface of your connection dramatically. If you wish to hide your Tor usage from your ISP or your government, Tor has a built-in solution for that: Tor bridges. [Read more about Tor bridges and why using a VPN is not necessary](../advanced/tor-overview.md).

## E se eu precisar de anonimato?

As VPNs não podem fornecer anonimato. Your VPN provider will still see your real IP address, and often has a money trail that can be linked directly back to you. You cannot rely on "no logging" policies to protect your data. Use [Tor](https://www.torproject.org/) em vez disso.

## E os provedores de VPN que fornecem nós Tor?

Não use esse recurso. The point of using Tor is that you do not trust your VPN provider. Currently Tor only supports the [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) protocol. [UDP](https://en.wikipedia.org/wiki/User_Datagram_Protocol) (used in [WebRTC](https://en.wikipedia.org/wiki/WebRTC) for voice and video sharing, the new [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3) protocol, etc.), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) and other packets will be dropped. To compensate for this, VPN providers typically will route all non-TCP packets through their VPN server (your first hop). This is the case with [ProtonVPN](https://protonvpn.com/support/tor-vpn/). Additionally, when using this Tor over VPN setup, you do not have control over other important Tor features such as [Isolated Destination Address](https://www.whonix.org/wiki/Stream_Isolation) (using a different Tor circuit for every domain you visit).

The feature should be viewed as a convenient way to access the Tor Network, not to stay anonymous. For proper anonymity, use the Tor Browser, TorSocks, or a Tor gateway.

## Quando VPNs são úteis?

A VPN may still be useful to you in a variety of scenarios, such as:

1. Hiding your traffic from **only** your Internet Service Provider.
1. Hiding your downloads (such as torrents) from your ISP and anti-piracy organizations.
1. Hiding your IP from third-party websites and services, preventing IP based tracking.

For situations like these, or if you have another compelling reason, the VPN providers we listed above are who we think are the most trustworthy. However, using a VPN provider still means you're *trusting* the provider. In pretty much any other scenario you should be using a secure**-by-design** tool such as Tor.

## Fontes e Leituras Adicionais

1. [VPN - a Very Precarious Narrative](https://schub.io/blog/2019/04/08/very-precarious-narrative.html) by Dennis Schubert
1. [Tor Network Overview](../advanced/tor-overview.md)
1. [IVPN Privacy Guides](https://www.ivpn.net/privacy-guides)
1. ["Do I need a VPN?"](https://www.doineedavpn.com), a tool developed by IVPN to challenge aggressive VPN marketing by helping individuals decide if a VPN is right for them.

## Informações Relacionadas a VPN

- [The Trouble with VPN and Privacy Review Sites](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites/)
- [Investigação de Aplicativos VPN Gratuitos](https://www.top10vpn.com/free-vpn-app-investigation/)
- [Proprietários Secretos de VPN revelados: 101 produtos VPN operados por apenas 23 empresas](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/)
- [Esta empresa chinesa está secretamente por trás de 24 aplicativos populares que pedem permissões perigosas](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions/)
