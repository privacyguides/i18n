---
title: "Visão geral do Tor"
icon: 'simple/torproject'
description: Tor é uma rede descentralizada e de utilização gratuita, concebida para utilizar a Internet com o máximo de privacidade possível.
---

Tor é uma rede descentralizada e de utilização gratuita, concebida para utilizar a Internet com o máximo de privacidade possível. Se utilizada corretamente, a rede permite a navegação e as comunicações privadas e anónimas.

## Construção de caminhos para os serviços Clearnet

Os "serviços Clearnet" são sites a que pode aceder com qualquer browser, como é o caso do [privacyguides.org](https://www.privacyguides.org). O Tor permite-lhe ligar-se a estes sites de forma anónima, encaminhando o seu tráfego através de uma rede composta por milhares de servidores geridos por voluntários, chamados nós (ou relés).

Sempre que [se liga ao Tor](../tor.md), este escolhe três nós para construir um caminho para a Internet - este caminho chama-se "circuito"

<figure markdown>
  ![Caminho do Tor que mostra o seu dispositivo a ligar-se a um nó de entrada, a um nó intermédio e a um nó de saída antes de chegar ao site de destino](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Caminho do Tor que mostra o seu dispositivo a ligar-se a um nó de entrada, a um nó intermédio e a um nó de saída antes de chegar ao site de destino](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Caminho do circuito do Tor</figcaption>
</figure>

Cada um destes nós tem a sua própria função:

### O nó de entrada

O nó de entrada, muitas vezes chamado de nó de guarda, é o primeiro nó ao qual seu cliente Tor se conecta. O nó de entrada consegue ver o seu endereço IP, mas não consegue ver a que é que se está a ligar.

Ao contrário dos outros nós, o cliente Tor seleciona aleatoriamente um nó de entrada e usa-o durante dois a três meses para o proteger de certos ataques.[^1]

### O nó intermédio

O nó intermédio é o segundo nó ao qual o seu cliente Tor se conecta. Pode ver de que nó veio o tráfego - o nó de entrada - e para que nó se dirige a seguir. O nó intermédio não pode ver o seu endereço IP ou o domínio ao qual se está a ligar.

Para cada novo circuito, o nó intermédio é selecionado aleatoriamente de entre todos os nós Tor disponíveis.

### O nó de saída

O nó de saída é o ponto em que o seu tráfego web deixa a rede Tor e é encaminhado para o seu destino final. O nó de saída não consegue ver o seu endereço IP, mas sabe a que site se está a ligar.

O nó de saída é escolhido aleatoriamente de entre todos os nós Tor disponíveis que possuam um sinalizador de retransmissão de saída.[^2]

## Criação de caminhos para os serviços Onion

Os "Serviços Onion" (também vulgarmente designados por "serviços ocultos") são sites que só podem ser acedidos através do Tor. Estes sites têm um nome de domínio longo que é gerado aleatoriamente e que termina em `.onion`.

A ligação a um serviço Onion no Tor funciona de forma muito semelhante à ligação a um serviço clearnet, mas o seu tráfego é encaminhado através de um total de **seis** nós, antes de chegar ao servidor de destino. No entanto, tal como antes, apenas três desses nós contribuem para *o seu* anonimato. Os restantes três nós protegem o anonimato* do Onion Service*, ocultando o verdadeiro IP e a localização do site, da mesma forma que o browser Tor oculta o seu.

<figure style="width:100%" markdown>
  ![Caminho do Tor que mostra o seu tráfego sendo encaminhado através dos três nós Tor, mais os três nós Tor adicionais que escondem a identidade do site](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Caminho do Tor que mostra o seu tráfego sendo encaminhado através dos três nós Tor, mais os três nós Tor adicionais que escondem a identidade do site](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Caminho do circuito Tor com Serviços Onion. Os nós na vedação <span class="pg-blue">azul</span> pertencem ao seu browser, enquanto os nós na vedação <span class="pg-red">vermelha</span> pertencem ao servidor, pelo que a sua identidade está oculta.</figcaption>
</figure>

## Encriptação

O Tor encripta três vezes cada um dos pacotes (blocos de dados transmitidos) com as chaves do nó de saída, do nó intermédio e do nó de entrada - por esta ordem.

Uma vez estabelecido o circuito pelo Tor, a transmissão de dados é efetuada da seguinte forma:

1. Primeiro: quando o pacote chega ao nó de entrada, a primeira camada de encriptação é removida. Neste pacote encriptado, o nó de entrada encontrará outro pacote encriptado com o endereço do nó intermédio. O nó de entrada reencaminha então o pacote para o nó intermédio.

2. Em seguida: quando o nó intermédio recebe o pacote do nó de entrada, também ele remove uma camada de encriptação com a sua chave e, desta vez, encontra um pacote encriptado com o endereço do nó de saída. O nó intermédio reencaminha então o pacote para o nó de saída.

3. Por último: quando o nó de saída recebe o seu pacote, remove a última camada de encriptação com a sua chave. O nó de saída verá o endereço de destino e encaminhará o pacote para esse endereço.

Segue-se um diagrama alternativo que mostra o processo. Cada nó remove a sua própria camada de encriptação e, quando o servidor de destino devolve os dados, o mesmo processo acontece totalmente ao contrário. Por exemplo, o nó de saída não sabe quem é o utilizador, mas sabe de que nó veio a mensagem, pelo que adiciona a sua própria camada de encriptação e envia-a de volta.

<figure markdown>
  ![Encriptação Tor](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Encriptação Tor](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Enviar e receber dados através da Rede Tor</figcaption>
</figure>

O Tor permite-nos ligar a um servidor sem que alguma das partes conheça todo o caminho. O nó de entrada sabe quem é o utilizador, mas não sabe para onde vai; o nó intermédio não sabe quem é o utilizador nem para onde vai; e o nó de saída sabe para onde vai, mas não sabe quem é o utilizador. Uma vez que o nó de saída é o que estabelece a ligação final, o servidor de destino nunca saberá o seu endereço IP.

## Ressalvas

Embora o Tor ofereça fortes garantias de privacidade, é preciso estar ciente de que ele não é perfeito:

- Adversários bem financiados, com a capacidade de observar passivamente a maior parte do tráfego de rede em todo o mundo, têm a possibilidade de desanonimizar os utilizadores do Tor através de uma análise de tráfego avançada. O Tor também não o protege de se expor inadvertidamente, como quando partilha demasiadas informações sobre a sua verdadeira identidade.
- Os nós de saída do Tor também podem monitorizar o tráfego que passa por eles. Isto significa que o tráfego que não está encriptado, como o tráfego HTTP simples, pode ser registado e monitorizado. Se esse tráfego contiver informações de identificação pessoal, pode retirar o anonimato do utilizador para esse nó de saída. Assim, recomendamos a utilização de HTTPS sobre Tor sempre que possível.

Se pretender utilizar o Tor para navegar na Web, recomendamos apenas o browser Tor **oficial** - foi concebido para evitar a recolha de impressões digitais.

- [Browser Tor :material-arrow-right-drop-circle:](../tor.md#tor-browser)

## Recursos Adicionais

- [Manual do utilizador do Tor](https://tb-manual.torproject.org)
- [Como funciona o Tor - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Serviços Onion Tor - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: O primeiro relé no seu circuito chama-se "guarda de entrada" ou "guarda". Trata-se de um retransmissor rápido e estável que permanece o primeiro no seu circuito durante 2-3 meses, a fim de o proteger contra um ataque conhecido de quebra de anonimato. O resto do seu circuito muda a cada novo site que visita e, em conjunto, estes relés fornecem todas as proteções de privacidade do Tor. Para obter mais informações sobre o funcionamento dos relés de proteção, consulte esta [publicação no blogue](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) e o [documento](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) sobre proteções de entrada. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2/))

[^2]: Flag do relé: uma (des)qualificação especial de relés para posições de circuito (por exemplo, "Guard", "Exit", "BadExit"), propriedades de circuito (por exemplo, "Fast", "Stable"), ou funções (por exemplo, "Authority", "HSDir"), tal como atribuídas pelas autoridades de diretório e definidas mais pormenorizadamente na especificação do protocolo de diretório. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
