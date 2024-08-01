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
<p class="admonition-title">Observação</p>

Quando nos referimos a "Redes Privadas Virtuais" neste site, geralmente estamos nos referindo a **provedores comerciais** [de VPN](../vpn.md), aos quais você paga uma taxa mensal em troca do roteamento seguro do seu tráfego de Internet por seus servidores públicos. Há muitas outras formas de VPN, como as que você mesmo hospeda ou as operadas por locais de trabalho que permitem a conexão segura a recursos de rede interna/dos funcionários; no entanto, essas VPNs geralmente são projetadas para acessar redes remotas com segurança, em vez de proteger a privacidade da sua conexão com a Internet.

</div>

## Como funciona a VPN?

As VPNs criptografam o tráfego entre o dispositivo e um servidor de propriedade do provedor de VPN. Do ponto de vista de qualquer pessoa entre você e o servidor VPN, parece que você está se conectando ao servidor VPN. Do ponto de vista de qualquer pessoa entre o servidor VPN e o site de destino, tudo o que ela pode ver é o servidor VPN se conectando ao site.

``` mermaid

```

Observe que uma VPN não adiciona nenhuma segurança ou criptografia ao seu tráfego entre o servidor VPN e o seu destino na Internet. Para acessar um site com segurança, você ainda **deve** garantir que o HTTPS esteja em uso, independentemente de usar uma VPN.

## Devo Usar Uma VPN?

**Sim**, quase certamente. Uma VPN tem muitas vantagens, incluindo:

1. Ocultar seu tráfego **apenas** do seu provedor de serviços de Internet.
1. Ocultação de seus downloads (como torrents) de seu ISP e de organizações antipirataria.
1. Oculta seu IP de sites e serviços de terceiros, ajudando-o a se integrar e evitando o rastreamento baseado em IP.
1. Permitindo que você contorne as restrições geográficas de determinados conteúdos.

As VPNs podem oferecer *alguns* dos mesmos benefícios que o Tor, como ocultar seu IP dos sites que você visita e deslocar geograficamente seu tráfego de rede, e bons provedores de VPN não cooperarão com, por exemplo, autoridades legais de regimes opressivos, especialmente se você escolher um provedor de VPN fora de sua própria jurisdição.

VPNs não podem criptografar dados fora da conexão entre o seu dispositivo e o servidor VPN. Os provedores de VPN também podem ver e modificar o seu tráfego da mesma forma que o seu ISP, portanto, ainda há um nível de confiança que você está depositando neles. E não há nenhuma maneira de verificar as políticas de "não registro" dos provedores de VPN.

## Quando uma VPN não é apropriada?

Using a VPN in cases where you're using your [real-life or well-known identity](common-misconceptions.md#complicated-is-better) online is unlikely to be useful. Fazê-lo pode acionar sistemas de detecção de fraude e “spam”, como se você logasse no site do seu banco.

É importante lembrar que uma VPN não lhe proporcionará anonimato absoluto, pois o próprio provedor de VPN ainda verá seu endereço IP real, as informações do site de destino e, muitas vezes, tem um rastro de dinheiro que pode ser vinculado diretamente a você. Não é possível confiar em políticas de "não registro" para proteger seus dados de qualquer pessoa que possa protegê-los. Se você precisar de segurança total da própria rede, considere o uso do [Tor](../advanced/tor-overview.md), além ou em vez de uma VPN.

Você também não deve confiar em uma VPN para proteger sua conexão com um destino HTTP não criptografado. Para manter realmente privado e seguro o que você faz nos sites que visita, você precisa utilizar HTTPS. Isso manterá suas senhas, tokens de sessão e consultas protegidas do provedor de VPN e de outros adversários em potencial entre o servidor VPN e seu destino. Você deve ativar o modo somente-HTTPS em seu navegador (se for compatível) para atenuar os ataques que tentam fazer downgrade de sua conexão de HTTPS para HTTP.

## Devo usar DNS criptografado com uma VPN?

A menos que seu próprio provedor de VPN hospede os servidores de DNS criptografados, **provavelmente não**. Usar o DOH/DOT (ou qualquer outra forma de DNS criptografado) com servidores de terceiros simplesmente adicionará mais entidades nas quais confiar. Seu provedor VPN ainda pode ver quais sites você visita baseado nos seus endereços IP e outros métodos. Dito isso, pode haver algumas vantagens em ativar o DNS criptografado para habilitar outros recursos de segurança em seu navegador, como o ECH. As tecnologias de navegador que dependem do DNS encriptado no navegador são relativamente recentes e ainda não estão generalizadas, pelo que a sua relevância para o usuário em particular é um exercício que deixamos ao critério do usuário pesquisar de forma independente.

Outro motivo comum pelo qual o DNS criptografado é recomendado é que ele impede a falsificação de DNS. No entanto, seu navegador já deve estar checando por [certificados TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) com **HTTPS** e te informar sobre. Se você não está usando **HTTPS**, então um adversário pode simplesmente modificar qualquer coisa diferente das suas consultas DNS e o resultado será pouco diferente.

## Devo usar Tor *e* uma VPN?

Talvez o Tor não seja necessariamente adequado para todos, em primeiro lugar. Considere o seu [modelo de ameaça](threat-modeling.md), pois se o seu adversário não for capaz de extrair informações do seu provedor de VPN, o uso de uma VPN por si só pode fornecer proteção suficiente.

Se você usa o Tor, *provavelmente* é melhor se conectar à rede Tor através de um provedor de VPN comercial. No entanto, esse é um assunto complexo sobre o qual escrevemos mais em nossa página de [visão geral do Tor](../advanced/tor-overview.md).

## Devo acessar o Tor por meio de provedores VPN que fornecem "Nós Tor?

Você não deve usar esse recurso: A principal vantagem de usar o Tor é que você não confia no seu provedor de VPN, o que é negado quando você usa os nós do Tor hospedados pela sua VPN em vez de se conectar diretamente ao Tor a partir do seu computador.

Atualmente, o Tor suporta apenas o protocolo TCP. Os pacotes UDP (usados por [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3) e outros protocolos), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) e outros serão descartados. Para compensar isso, os provedores de VPN normalmente encaminham todos os pacotes não-TCP por meio do servidor VPN (seu primeiro salto). Esse é o caso da [ProtonVPN](https://protonvpn.com/support/tor-vpn). Além disso, ao usar essa configuração do Tor sobre VPN, você não tem controle sobre outros recursos importantes do Tor, como o [endereço de destino isolado](https://whonix.org/wiki/Stream_Isolation) (usando um circuito Tor diferente para cada domínio visitado).

O recurso deve ser visto como uma maneira *conveniente* de acessar serviços ocultos no Tor, não para permanecer anônimo. Para obter o anonimato adequado, use o [navegador Tor](../tor.md) real.

## Propriedade da VPN comercial

A maioria dos serviços de VPN é de propriedade das mesmas [poucas empresas](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies). Essas empresas obscuras administram vários serviços de VPN menores para criar a ilusão de que você tem mais opções do que realmente tem e para maximizar o lucro. Normalmente, esses provedores que alimentam a empresa de fachada têm péssimas políticas de privacidade e não se deve confiar seu tráfego de Internet a eles. Você deve ser muito rigoroso com relação ao provedor que decidir usar.

Você também deve ter cuidado com o fato de que muitos sites de avaliação de VPNs são meros veículos de publicidade abertos a quem der o maior lance. ==O Privacy guides não ganham dinheiro com recomendações de produtos externos, e nunca usam programas de afiliados.==

[Nossas Recomendações](../vpn.md ""){.md-button}

## Alternativas modernas de VPN

Recentemente, várias organizações fizeram algumas tentativas para resolver alguns problemas que as VPNs centralizadas apresentam. Essas tecnologias são relativamente novas, mas vale a pena ficar de olho no desenvolvimento do campo.

### Múltiplos Relays

Os MPRs (Multi-Party Relays) usam vários nós pertencentes a diferentes partes, de modo que nenhuma parte individual saiba quem você é e a que está se conectando. Essa é a ideia básica por trás do Tor, mas agora existem alguns serviços pagos que tentam emular esse modelo.

As MPRs buscam resolver um problema inerente às VPNs: o fato de que você precisa confiar totalmente nelas. Eles atingem esse objetivo segmentando as responsabilidades entre duas ou mais empresas diferentes. Por exemplo, o iCloud+ Private Relay da Apple roteia seu tráfego por dois servidores:

1. Em primeiro lugar, um servidor operado pela Apple.

    Esse servidor consegue ver o IP do seu dispositivo quando você se conecta a ele e tem conhecimento de suas informações de pagamento e do ID Apple vinculado à sua assinatura do iCloud. No entanto, ele não consegue ver a qual site você está se conectando.

2. Em segundo lugar, um servidor operado por uma CDN parceira, como a Cloudflare ou a Fastly.

    Esse servidor realmente faz a conexão com o site de destino, mas não tem conhecimento do seu dispositivo. O único endereço IP que ele conhece é o do servidor da Apple.

Outros MPRs administrados por empresas diferentes, como o Google ou o INVISV, operam de maneira muito semelhante. Essa proteção por segmentação só existe se você confiar que às duas empresas não farão conluio entre si para anonimizar você.

### VPNs descentralizadas

Outra tentativa de resolver os problemas com serviços de VPN centralizados são as dVPNs. Eles se baseiam na tecnologia “blockchain” e afirmam eliminar a confiança em uma única parte, distribuindo os nós entre várias pessoas diferentes. No entanto, muitas vezes uma dVPN terá como padrão um único nó, o que significa que você precisa confiar totalmente nesse nó, assim como em uma VPN tradicional. Diferentemente de uma VPN tradicional, esse único nó que pode ver todo o seu tráfego é uma pessoa aleatória, em vez de seu provedor de VPN, que pode ser auditado e tem responsabilidades legais para manter sua política de privacidade. Para solucionar esse problema, é necessário um salto múltiplo, mas isso tem um custo de estabilidade e desempenho.

Outra consideração é a responsabilidade jurídica. O nó de saída precisará lidar com problemas legais decorrentes do uso indevido da rede, uma questão com a qual a rede Tor tem lutado durante toda a sua existência. Isso desencoraja as pessoas comuns de rodar nós e o torna mais atraente para um ator malicioso com muitos recursos para hospedar um. Esse é um grande problema se o serviço for de nó único, pois o nó de saída potencialmente mal-intencionado pode ver quem você é e a que está se conectando.

Muitas dVPNs são usadas para promover uma criptomoeda em vez de oferecer o melhor serviço. Elas também tendem a ser redes menores, com menos nós, o que as torna mais vulneráveis a [ataques Sybil](https://en.wikipedia.org/wiki/Sybil_attack).

## Informações Relacionadas a VPN

- [O problema com os sites de análise de VPN e privacidade](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [Investigação de Aplicativos VPN Gratuitos](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [Proprietários Secretos de VPN revelados: 101 produtos VPN operados por apenas 23 empresas](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [Esta empresa chinesa está secretamente por trás de 24 aplicativos populares que pedem permissões perigosas](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - uma narrativa muito precária](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) por Dennis Schubert
