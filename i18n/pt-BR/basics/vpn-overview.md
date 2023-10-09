---
meta_title: "Como As VPNs Protegem Sua Privacidade? Nossa Visão Geral Sobre VPN — Privacy Guides"
title: Visão geral da VPN
icon: material/vpn
description: As Redes Privadas Virtuais transferem o risco do seu ISP para um terceiro em quem você confia. Você deve ter isso em mente.
---

Redes Privadas Virtuais são uma forma de estender o fim da sua conexão para sair de outro lugar do mundo. Um provedor de serviços de internet (ISP) pode ver o fluxo de tráfego da Internet que entra e sai do seu dispositivo de terminação de rede (por exemplo, o modem).

Protocolos de criptografia, como o HTTPS, são frequentemente usados na Internet, de modo que eles não consigam ver exatamente o que você está postando ou lendo, mas eles podem ter uma ideia dos [domínios que você solicita](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

Uma VPN pode ajudar, visto que transfere a confiança para um servidor em outro lugar do mundo. Como resultado, seu provedor de Internet só vê que você está conectado a uma VPN e nada sobre a atividade que você está transmitindo através dela.

## Devo Usar Uma VPN?

**Sim**, a menos que você já esteja usando o Tor. Uma VPN faz duas coisas: transfere os riscos do seu Provedor de Serviços de Internet para você mesmo e oculta seu IP de um serviço de terceiros.

VPNs não podem criptografar dados fora da conexão entre o seu dispositivo e o servidor VPN. Provedores de VPN podem ver e modificar seu tráfego da mesma forma que seu provedor de internet pode. E não há nenhuma maneira de verificar as políticas de "não registro" dos provedores de VPN.

No entanto, eles ocultam seu IP real de um serviço de terceiros, desde que não haja vazamentos de IP. Ajudam a misturar-se com os outros e a diminuir o rastreio baseado no IP.

## Quando não deveria usar uma VPN?

Using a VPN in cases where you're using your [known identity](common-misconceptions.md#complicated-is-better) is unlikely be useful.

Fazê-lo pode acionar sistemas de detecção de fraude e “spam”, como se você logasse no site do seu banco.

## E Quanto à Criptografia?

A criptografia oferecida por provedores de VPN está presente entre seus dispositivos e os servidores deles. Isso garante que esse link específico entre cliente-servidor é seguro. Isso já é um avanço em relação a utilizar “proxies” descriptografados onde um adversário na rede pode interceptar as comunicações entre seus dispositivos e os respectivos “proxies”, modificando-as. No entanto, a criptografia entre seus aplicativos e navegadores com os provedores de serviço não é tratada por essa criptografia.

Para manter realmente privado e seguro o que você faz nos sites que visita, você precisa utilizar HTTPS. Isso irá manter suas senhas, “tokens” de seção, e consultas seguras do seu provedor de VPN. Considere habilitar a opção “HTTPS automático” no seu navegador para mitigar ataques de “downgrade” como o [SSL Strip](https://www.blackhat.com/presentations/bh-dc-09/Marlinspike/BlackHat-DC-09-Marlinspike-Defeating-SSL.pdf).

## Devo usar DNS criptografado com uma VPN?

A menos que seu próprio provedor de VPN hospede os servidores de DNS criptografados, **não**. Usar “DOH/DOT” (ou qualquer outra forma de DNS criptografado) com um servidor terceiro irá simplesmente adicionar mais entidades para confiar e não faz **absolutamente nada** para melhorar sua privacidade/segurança. Seu provedor VPN ainda pode ver quais sites você visita baseado nos seus endereços IP e outros métodos. Ao invés de confiar apenas no seu provedor VPN, você agora estará confiando nele e no provedor DNS escolhido.

Uma razão comum para recomendar DNS criptografado é que ajuda contra a falsificação de DNS (ou “DNS spoofing”). No entanto, seu navegador já deve estar checando por [certificados TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) com **HTTPS** e te informar sobre. Se você não está usando **HTTPS**, então um adversário pode simplesmente modificar qualquer coisa diferente das suas consultas DNS e o resultado será pouco diferente.

Needless to say, **you shouldn't use encrypted DNS with Tor**. This would direct all of your DNS requests through a single circuit and would allow the encrypted DNS provider to deanonymize you.

## Devo usar Tor *e* uma VPN?

Ao usar uma VPN com Tor, você cria essencialmente um node de entrada permanente, geralmente com um rastro de dinheiro anexado. Isso não oferece nenhum benefício adicional para você, enquanto aumenta drasticamente a superfície de ataque da sua conexão. Se você deseja ocultar o uso do Tor do seu ISP ou do governo, o Tor tem uma solução integrada para isso: Tor bridges. [Leia mais sobre Tor bridges e por que não é necessário usar uma VPN](../advanced/tor-overview.md).

## E se eu precisar de anonimato?

As VPNs não podem fornecer anonimato. Seu provedor de VPN ainda verá seu endereço IP real e geralmente possui um rastro de dinheiro que pode ser vinculado diretamente a você. Você não pode confiar em políticas de “no logging” para proteger seus dados. Use [Tor](https://www.torproject.org/) em vez disso.

## E os provedores de VPN que fornecem nós Tor?

Não use esse recurso. O objetivo de usar o Tor é que você não confia no seu provedor de VPN. Currently Tor only supports the [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) protocol. [UDP](https://en.wikipedia.org/wiki/User_Datagram_Protocol) (used in [WebRTC](https://en.wikipedia.org/wiki/WebRTC) for voice and video sharing, the new [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3) protocol, etc.), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) and other packets will be dropped. To compensate for this, VPN providers typically will route all non-TCP packets through their VPN server (your first hop). This is the case with [ProtonVPN](https://protonvpn.com/support/tor-vpn/). Additionally, when using this Tor over VPN setup, you do not have control over other important Tor features such as [Isolated Destination Address](https://www.whonix.org/wiki/Stream_Isolation) (using a different Tor circuit for every domain you visit).

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
