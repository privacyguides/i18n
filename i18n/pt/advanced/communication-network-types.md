---
title: "Tipos de redes de comunicação"
icon: 'material/transit-connection-variant'
description: Uma visão geral sobre as várias arquiteturas de rede normalmente utilizadas por aplicações de mensagens instantâneas.
---

Existem várias arquiteturas de rede normalmente utilizadas para transmitir mensagens entre pessoas. Estas redes podem fornecer diferentes garantias de privacidade, pelo que vale a pena considerar o seu modelo de ameaça [](../basics/threat-modeling.md) ao decidir qual a aplicação a utilizar.

[Aplicações de mensagens instantâneas recomendadas](../real-time-communication.md ""){.md-button}

## Redes centralizadas

![Diagrama de redes centralizadas](../assets/img/layout/network-centralized.svg){ align=left }

As aplicações de mensagens instantâneas centralizadas são aquelas em que todos os participantes se encontram no mesmo servidor ou rede de servidores, controlados pela mesma organização.

Algumas aplicações de mensagens instantâneas permitem-lhe a opção de auto-hospedagem, possibilitando que sejam instaladas no seu próprio servidor. A auto-hospedagem pode oferecer garantias de privacidade adicionais, como a ausência de registos de utilização ou o acesso limitado a metadados (dados sobre quem fala com quem). As aplicações de mensagens instantâneas centralizadas auto-hospedadas são isoladas, havendo a necessidade de terem que estar todos a utilizar o mesmo servidor, para que seja possível a comunicação.

**Vantagens:**

- Novas funcionalidades e alterações podem ser implementadas mais rapidamente.
- Facilidade de utilização e facilidade em encontrar contactos.
- Ecossistema amadurecido e estável, devido à facilidade de desenvolvimento de um software centralizado.
- Reduzidos problemas de privacidade, devido à confiança depositada na configuração do servidor.

**Desvantagens:**

- Pode incluir [controlo ou acesso restrito](https://drewdevault.com/2018/08/08/Signal.html). Ou seja:
- Estar [impedida a ligação de clientes de terceiros](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165) à rede centralizada, o que poderia permitir uma maior personalização ou uma melhor experiência. Frequentemente definido nos Termos e Condições de utilização.
- Documentação deficiente ou inexistente para os programadores terceiros.
- A [propriedade](https://web.archive.org/web/20210729191953/https://blog.privacytools.io/delisting-wire/), a política de privacidade e gestão do serviço podem mudar facilmente quando uma única entidade os controla, podendo ficar assim, mais tarde, comprometido o serviço.
- A auto-hospedagem requer esforço e conhecimento para a configuração do serviço.

## Redes Federadas

![Diagrama de redes federadas](../assets/img/layout/network-decentralized.svg){ align=left }

As aplicações de mensagens instantâneas federadas utilizam vários servidores independentes e descentralizados que podem comunicar entre si (o e-mail é um exemplo de um serviço federado). A federação permite que os administradores de sistemas controlem o seu próprio servidor e continuem a fazer parte de uma rede de comunicações maior.

Numa solução auto-hospedada, os membros de um servidor federado podem descobrir e comunicar com membros de outros servidores, embora alguns servidores possam optar por permanecer privados, não sendo federados (por exemplo, servidor de equipa de trabalho).

**Vantagens:**

- Permite um maior controlo sobre os seus próprios dados, devido a estes residirem no seu próprio servidor.
- Permite-lhe escolher a quem confiar os seus dados, escolhendo entre vários servidores "públicos".
- Não raras vezes, permite clientes de terceiros que podem proporcionar uma experiência mais nativa, personalizada ou acessível.
- É possível verificar se o software do servidor corresponde ao código-fonte público, assumindo que tem acesso ao servidor ou que confia na pessoa que o tem (por exemplo, um membro da família).

**Desvantagens:**

- A adição de novas funcionalidades é mais complexa, uma vez que estas funcionalidades têm de ser normalizadas e testadas para garantir que funcionam com todos os servidores da rede.
- Devido ao ponto anterior, as funcionalidades podem não estar disponíveis, incompletas ou funcionar de formas inesperadas em comparação com as plataformas centralizadas, como a transmissão de mensagens quando offline ou a eliminação de mensagens.
- Podem estar disponíveis alguns metadados (por exemplo, informações como "quem está a falar com quem", mas não o conteúdo real da mensagem, se for utilizado o E2EE).
- Os servidores federados geralmente requerem grande confiança no administrador do servidor. Podem ser amadores, ou não ser "profissionais de segurança", e podem não fornecer documentos padrão, como uma política de privacidade ou termos de serviço, informações importantes para saber como serão utilizados os dados.
- Por vezes, os administradores de servidores optam por bloquear outros servidores que são uma fonte de abuso não moderado ou que quebram as regras gerais de comportamento comummente aceites. Isso tornará mais difícil a comunicação com os membros desses servidores.

## Redes peer-to-peer

![Diagrama P2P](../assets/img/layout/network-distributed.svg){ align=left }

As aplicações de mensagens instantâneas P2P ligam-se a uma [rede distribuída](https://en.wikipedia.org/wiki/Distributed_networking) de nós para retransmitir a mensagem ao destinatário, sem utilizar um servidor de terceiros.

Os clientes (peers) comunicam através da utilização de uma rede de [computação distribuída](https://en.wikipedia.org/wiki/Distributed_computing). Exemplos do atrás dito incluem [Distributed Hash Tables](https://en.wikipedia.org/wiki/Distributed_hash_table) (DHT), utilizadas por [torrents](https://en.wikipedia.org/wiki/BitTorrent_(protocol)) e [IPFS](https://en.wikipedia.org/wiki/InterPlanetary_File_System), por exemplo. Outra abordagem é a das redes de proximidade, em que uma ligação é estabelecida através de WiFi ou Bluetooth (por exemplo, Briar ou o protocolo de rede social [Scuttlebutt](https://www.scuttlebutt.nz)).

Uma vez que um peer tenha encontrado uma rota para o seu contacto através de qualquer um destes métodos, é estabelecida uma ligação direta entre eles. Embora as mensagens sejam normalmente encriptadas, um observador pode ainda assim deduzir a localização e a identidade do remetente e do destinatário.

As redes P2P não utilizam servidores, uma vez que os peers comunicam diretamente entre si e, por conseguinte, não podem ser auto-hospedados. No entanto, alguns serviços adicionais podem depender de servidores centralizados, como a descoberta de utilizadores ou a retransmissão de mensagens offline, que podem beneficiar de auto-hospedagem.

**Vantagens:**

- O número de informações expostas a terceiros é mínimo.
- As plataformas P2P modernas implementam o E2EE por defeito. Não existem servidores que possam potencialmente intercetar e desencriptar as suas transmissões, ao contrário dos modelos centralizados e federados.

**Desvantagens:**

- Conjunto de funcionalidades reduzido:
- As mensagens só podem ser enviadas quando ambos os peers estão online, no entanto, o seu cliente pode armazenar mensagens localmente para aguardar que o contacto volte a estar online.
- Geralmente, aumenta a utilização da bateria em dispositivos móveis, porque o cliente tem de permanecer ligado à rede distribuída para saber quem está online.
- Algumas funcionalidades comuns das mensagens instantâneas podem não estar implementadas ou estar incompletas, como a eliminação de mensagens.
- O seu endereço IP e o dos contactos com quem está a comunicar podem ser expostos se não utilizar o software em conjunto com uma [VPN](../vpn.md) ou o [Tor](../tor.md). Muitos países possuem formas de vigilância em massa e/ou de retenção de metadados.

## Encaminhamento anónimo

![Diagrama de encaminhamento anónimo](../assets/img/layout/network-anonymous-routing.svg){ align=left }

Uma aplicação de mensagens instantâneas que utilize o [encaminhamento anónimo](https://doi.org/10.1007/978-1-4419-5906-5_628) oculta a identidade do remetente, do destinatário ou a prova de que estão a comunicar. Idealmente, a aplicação deve esconder os três.

Existem [muitas](https://doi.org/10.1145/3182658) formas diferentes de implementar o encaminhamento anónimo. Um dos mais famosos é o [onion routing](https://en.wikipedia.org/wiki/Onion_routing) (ou seja, [Tor](tor-overview.md)), que comunica mensagens encriptadas através de uma rede virtual [sobreposta](https://en.wikipedia.org/wiki/Overlay_network), que oculta a localização de cada nó, bem como o destinatário e o remetente de cada mensagem. O remetente e o destinatário nunca interagem diretamente e só se encontram através de um nó de encontro secreto, para que não haja fuga de endereços IP nem de localização física. Os nós não podem decifrar as mensagens, nem o destino final; só o destinatário o pode fazer. Cada nó intermediário só pode decifrar uma parte que indica para onde deve ser enviada a mensagem, ainda encriptada, até chegar ao destinatário, que a pode decifrar completamente. Daí o nome "camadas de cebola"

A auto-hospedagem de um nó numa rede de encaminhamento anónima não proporciona ao anfitrião benefícios adicionais em termos de privacidade, mas contribui para a resiliência de toda a rede contra ataques de identificação, para benefício de todos.

**Vantagens:**

- As informações expostas a terceiros são mínimas, ou mesmo nenhumas.
- As mensagens podem ser retransmitidas de forma descentralizada, mesmo que uma das partes esteja offline.

**Desvantagens:**

- Propagação lenta de mensagens.
- Muitas vezes limitado a diferentes tipos de suportes. Usado principalmente para texto apenas, uma vez que a rede é lenta.
- Menos fiável, se os nós forem selecionados por encaminhamento aleatório, uma vez que alguns deles podem estar muito longe do emissor e do recetor, aumentando a latência ou mesmo deixando de transmitir mensagens se um dos nós ficar offline.
- O arranque é mais complexo, uma vez que é necessário criar e salvaguardar uma chave privada criptográfica.
- Tal como noutras plataformas descentralizadas, adicionar funcionalidades torna-se mais complexo para os programadores, ao contrário do que acontece numa plataforma centralizada. Assim, podem faltar funcionalidades ou estas podem estar implementadas de forma incompleta, como são exemplo a retransmissão de mensagens offline ou a eliminação de mensagens.
