---
meta_title: "Como as VPNs protegem sua privacidade? Nossa Visão Geral Sobre VPN — Privacy Guides"
title: Visão geral da VPN
icon: material/vpn
description: As Redes Privadas Virtuais transferem o risco do seu ISP para um terceiro em quem você confia. Você deve ter isso em mente.
---

Redes Privadas Virtuais são uma maneira de estender o fim da sua rede para sair de outro lugar do mundo.

Normalmente um provedor de serviços de internet (ISP) pode ver o fluxo de tráfego da Internet que entra e sai do seu dispositivo de rede (por exemplo, o modem). Protocolos de criptografia, como o HTTPS, são comumente usados na Internet, portanto, talvez eles não consigam ver exatamente o que você está postando ou lendo, mas podem ter uma ideia dos [domínios que você solicita](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

Usar uma VPN esconde mesmo essa informação do seu ISP, mudando a confiança depositada em sua rede para um servidor em outro lugar do mundo. Como resultado, o ISP só vê que você está conectado a uma VPN e nada sobre a atividade que está passando por ela.

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Quando nos referimos a "Redes Privadas Virtuais" neste site, geralmente estamos nos referindo a **provedores comerciais** [de VPN](../vpn.md), aos quais você paga uma taxa mensal em troca do roteamento seguro do seu tráfego de Internet por seus servidores públicos. Há muitas outras formas de VPN, como as que você mesmo hospeda ou as operadas por locais de trabalho que permitem a conexão segura a recursos de rede interna/dos funcionários; no entanto, essas VPNs geralmente são projetadas para acessar redes remotas com segurança, em vez de proteger a privacidade da sua conexão com a Internet.

</div>

## Como funciona a VPN?

As VPNs criptografam o tráfego entre o dispositivo e um servidor de propriedade do provedor de VPN. Do ponto de vista de qualquer pessoa entre você e o servidor VPN, parece que você está se conectando ao servidor VPN. Do ponto de vista de qualquer pessoa entre o servidor VPN e o site de destino, tudo o que ela pode ver é o servidor VPN se conectando ao site.

``` mermaid
flowchart LR
 763931["Your Device<div>(with VPN Client)</div>"] ===|"VPN Encryption"| 404512{"VPN Server"}
 404512 -.-|"No VPN Encryption"| 593753((("The Internet\n(Your Destination)")))
 subgraph 763931["Your Device<div>(with VPN Client)</div>"]
 end
```

Observe que uma VPN não adiciona nenhuma segurança ou criptografia ao seu tráfego entre o servidor VPN e o seu destino na Internet. Para acessar um site com segurança, você ainda **deve** garantir que o HTTPS esteja em uso, independentemente de usar uma VPN.

## Devo Usar Uma VPN?

**Sim**, quase com certeza. Uma VPN tem muitas vantagens, incluindo:

1. Ocultar seu tráfego **apenas** do seu provedor de serviços de Internet.
1. Ocultação de seus downloads (como torrents) de seu ISP e de organizações antipirataria.
1. Oculta seu IP de sites e serviços de terceiros, ajudando-o a se integrar e evitando o rastreamento baseado em IP.
1. Permitindo que você contorne as restrições geográficas de determinados conteúdos.

As VPNs podem oferecer *alguns* dos mesmos benefícios que o Tor, como ocultar seu IP dos sites que você visita e deslocar geograficamente seu tráfego de rede, e bons provedores de VPN não cooperarão com, por exemplo, autoridades legais de regimes opressivos, especialmente se você escolher um provedor de VPN fora de sua própria jurisdição.

VPNs não podem criptografar dados fora da conexão entre o seu dispositivo e o servidor VPN. Os provedores de VPN também podem ver e modificar o seu tráfego da mesma forma que o seu ISP, portanto, ainda há um nível de confiança que você está depositando neles. E não há nenhuma maneira de verificar as políticas de "não registro" dos provedores de VPN.

## Quando uma VPN não é apropriada?

É pouco provável que a utilização de uma VPN seja útil nos casos em que utiliza a sua [identidade](common-threats.md#common-misconceptions). Fazê-lo pode acionar sistemas de detecção de fraude e “spam”, como se você logasse no site do seu banco.

É importante lembrar que uma VPN não lhe proporcionará anonimato absoluto, pois o próprio provedor de VPN ainda verá seu endereço IP real, as informações do site de destino e, muitas vezes, tem um rastro de dinheiro que pode ser vinculado diretamente a você. Não é possível confiar em políticas de "não registro" para proteger seus dados de qualquer pessoa que possa protegê-los. Se você precisar de segurança total da própria rede, considere o uso do [Tor](../advanced/tor-overview.md), além ou em vez de uma VPN.

Você também não deve confiar em uma VPN para proteger sua conexão com um destino HTTP não criptografado. Para manter realmente privado e seguro o que você faz nos sites que visita, você precisa utilizar HTTPS. Isso manterá suas senhas, tokens de sessão e consultas protegidas do provedor de VPN e de outros adversários em potencial entre o servidor VPN e seu destino. Você deve ativar o modo somente-HTTPS em seu navegador (se for compatível) para atenuar os ataques que tentam fazer downgrade de sua conexão de HTTPS para HTTP.

## Devo usar DNS criptografado com uma VPN?

A menos que seu próprio provedor de VPN hospede os servidores de DNS criptografados, **provavelmente não**. Usar o DOH/DOT (ou qualquer outra forma de DNS criptografado) com servidores de terceiros simplesmente adicionará mais entidades nas quais confiar. Seu provedor VPN ainda pode ver quais sites você visita baseado nos seus endereços IP e outros métodos. Dito isso, pode haver algumas vantagens em ativar o DNS criptografado para habilitar outros recursos de segurança em seu navegador, como o ECH. Browser technologies which are reliant on in-browser encrypted DNS are relatively new and not yet widespread, so whether they are relevant to you in particular is an exercise we will leave to you to research independently.

Another common reason encrypted DNS is recommended is that it prevents DNS spoofing. No entanto, seu navegador já deve estar checando por [certificados TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) com **HTTPS** e te informar sobre. Se você não está usando **HTTPS**, então um adversário pode simplesmente modificar qualquer coisa diferente das suas consultas DNS e o resultado será pouco diferente.

## Devo usar Tor *e* uma VPN?

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

Another consideration is legal liability. The exit node will need to deal with legal problems from misuse of the network, an issue that the Tor network has contended with for its entire existence. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

Many dVPNs are used to push a cryptocurrency rather than to make the best service. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## Informações Relacionadas a VPN

- [The Trouble with VPN and Privacy Review Sites](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [Investigação de Aplicativos VPN Gratuitos](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [Proprietários Secretos de VPN revelados: 101 produtos VPN operados por apenas 23 empresas](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [Esta empresa chinesa está secretamente por trás de 24 aplicativos populares que pedem permissões perigosas](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - a Very Precarious Narrative](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) by Dennis Schubert
