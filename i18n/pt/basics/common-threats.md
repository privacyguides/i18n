---
title: "Ameaças comuns"
icon: 'material/eye-outline'
description: Cada utilizador tem o seu modelo de ameaça, mas estes são alguns dos aspetos que interessam a muitos visitantes deste site.
---

Em termos gerais, categorizamos as nossas recomendações no tipo de [ameaças](threat-modeling.md) ou objetivos que se aplicam à maioria das pessoas. ==Pode preocupar-se com nenhuma, uma, algumas ou todas estas possibilidades==, e as ferramentas e serviços que utiliza dependem dos seus objetivos. Também pode ter ameaças específicas fora destas categorias, o que é perfeitamente normal! O que importa realmente é que compreenda as vantagens e desvantagens das ferramentas que escolher, uma vez que praticamente nenhuma delas o protegerá de todas as ameaças.

- <span class="pg-purple">:material-incognito: Anonimato</span> - Protege a sua atividade online da sua identidade real, protegendo-o de pessoas que estão a tentar descobrir *a sua * identidade.
- <span class="pg-red">:material-target-account: Ataques direcionados</span> - Estar protegido contra hackers ou outros agentes maliciosos que estão a tentar obter acesso aos *seus* dados ou dispositivos.
- <span class="pg-orange">:material-bug-outline: Ataques passivos</span> - Estar protegido contra coisas como malware, violações de dados e outros ataques que são feitos contra muitas pessoas ao mesmo tempo.
- <span class="pg-teal">:material-server-network: Fornecedores de serviços</span> - Proteger os seus dados dos fornecedores de serviços (por exemplo, com E2EE, que torna os seus dados ilegíveis para o servidor).
- <span class="pg-blue">:material-eye-outline: Vigilância em massa</span> - Proteção contra agências governamentais, organizações, sites e serviços que trabalham em conjunto para seguir as suas atividades.
- <span class="pg-brown">:material-account-cash: Capitalismo de vigilância</span> - Proteger-se das grandes redes de marketing, como o Google e o Facebook, bem como de uma miríade de outros coletores de dados de terceiros.
- <span class="pg-green">:material-account-search: Exposição pública</span> - Limitar as informações sobre si que estão acessíveis online - para motores de busca ou para o público em geral.
- <span class="pg-blue-gray">:material-close-outline: Censura</span> - Evitar a censura ao acesso de informações ou quando nos expressamos online.

Algumas destas ameaças podem ser mais importantes para si do que outras, dependendo das suas preocupações específicas. Por exemplo, um programador de software com acesso a dados valiosos ou críticos pode estar principalmente preocupado com <span class="pg-red">:material-target-account: Ataques direcionados</span>, mas provavelmente quererá também proteger os seus dados pessoais de serem apanhados em programas de <span class="pg-blue">:material-eye-outline: Vigilância em massa</span>. Da mesma forma, muitas pessoas podem estar principalmente preocupadas com a <span class="pg-green">:material-account-search: Exposição pública</span> dos seus dados pessoais, mas podem também importar-se com questões de segurança, como <span class="pg-orange">:material-bug-outline: Ataques passivos</span>- como o malware que afeta os seus dispositivos.

## Anonimato vs. Privacidade

<span class="pg-purple">:material-incognito: Anonimato</span>

O anonimato é muitas vezes confundido com a privacidade, mas são conceitos distintos. Enquanto a privacidade é um conjunto de escolhas que faz sobre a forma como os seus dados são utilizados e partilhados, o anonimato é a dissociação completa das suas atividades online da sua identidade real.

Os denunciantes e os jornalistas, por exemplo, podem ter um modelo de ameaça muito mais extremo, que exige o anonimato total. Não se trata apenas de esconder o que fazem, os dados que possuem e de não serem pirateados por agentes maliciosos ou governos, mas também de esconder totalmente quem são. Muitas vezes, sacrificarão qualquer tipo de conveniência se isso significar proteger o seu anonimato, privacidade ou segurança, porque as suas vidas podem depender disso. A maioria das pessoas não precisa de ir tão longe.

## Segurança e Privacidade

<span class="pg-orange">:material-bug-outline: Ataques passivos</span>

A segurança e a privacidade também são frequentemente confundidas, uma vez que é necessária segurança para obter privacidade: A utilização de ferramentas - mesmo que sejam privadas por conceção - é inútil se puderem ser facilmente exploradas por atacantes que mais tarde divulgam os seus dados. No entanto, o inverso não é necessariamente verdadeiro: o serviço mais seguro do mundo *não é necessariamente* orientado para as questões da privacidade. O melhor exemplo disto é a confiança que depositamos na Google que, embora com uma escala muito significativa, tem tido poucos incidentes de segurança, o que consegue através do concurso de especialistas em segurança líderes do setor. Embora a Google forneça serviços muito seguros, poucas pessoas consideram os seus dados protegidos contra olhares indiscretos, sobretudo nos produtos gratuitos da Google (Gmail, YouTube, etc.)

No que diz respeito à segurança das aplicações, geralmente não sabemos (e por vezes não podemos saber) se o software que utilizamos é malicioso ou se poderá um dia tornar-se malicioso. Mesmo com os programadores mais fiáveis, geralmente não há garantia de que o seu software não tenha uma vulnerabilidade grave que possa ser explorada mais tarde.

Para minimizar os danos que um software malicioso *pode* causar, deve utilizar a segurança por compartimentação. Essa compartimentação pode ser conseguida na forma de utilização de computadores diferentes para trabalhos diferentes, utilização de máquinas virtuais para separar diferentes grupos de aplicações relacionadas ou utilização de um sistema operativo seguro com uma forte ênfase na solução de sandbox das aplicações e no controlo de acesso obrigatório.

!!! dica

    Os sistemas operativos móveis têm geralmente uma melhor proteção das aplicações do que os sistemas operativos de secretária: as aplicações não podem obter acesso à raiz e necessitam de permissão para aceder aos recursos do sistema.
    
    Os sistemas operativos para desktop deixam a desejar no que diz respeito a uma adequada proteção. O ChromeOS tem capacidades de sandbox semelhantes às do Android e o macOS tem controlo total das permissões do sistema (e os programadores podem optar pela sandbox para as aplicações). No entanto, estes sistemas operativos transmitem informações de identificação aos respectivos OEMs. O Linux tende a não enviar informações aos fornecedores de sistemas, mas tem uma fraca proteção contra exploits e aplicações maliciosas. Isto pode ser mitigado de alguma forma com distribuições especializadas que fazem uso significativo de máquinas virtuais ou contentores, como o [Qubes OS](../../desktop/#qubes-os).

<span class="pg-red">:material-target-account: Ataques direcionados</span>

Os ataques direcionados contra uma pessoa específica são mais problemáticos de tratar. Os ataques mais comuns incluem o envio de documentos maliciosos por e-mail, a exploração de vulnerabilidades (por exemplo, em navegadores e sistemas operativos) e ataques físicos. Se isto for uma preocupação para si, deve utilizar estratégias de mitigação de ameaças mais avançadas.

!!! dica

    Por definição, os **browsers**, os **clientes de e-mail** e as **suites de escritório** executam normalmente código não fiável, enviado por terceiros. Executar várias máquinas virtuais - para separar aplicações como estas do seu sistema anfitrião, bem como umas das outras - é uma técnica que pode utilizar para reduzir a possibilidade de uma exploração nestas aplicações poder comprometer o resto do seu sistema. Por exemplo, tecnologias como o Qubes OS ou o Microsoft Defender Application Guard no Windows fornecem métodos convenientes para o fazer.

Se estiver preocupado com **ataques físicos** deve utilizar um sistema operativo com uma implementação de arranque seguro verificado, como o Android, iOS, macOS ou [Windows (com TPM)](https://docs.microsoft.com/en-us/windows/security/information-protection/secure-the-windows-10-boot-process). Deve também certificar-se de que a sua unidade está encriptada e que o sistema operativo utiliza um TPM, Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) ou [Element](https://developers.google.com/android/security/android-ready-se) para limitar as tentativas de introdução da frase-chave de encriptação. Deve evitar partilhar o seu computador com pessoas em quem não confia, uma vez que a maioria dos sistemas operativos de computador de secretária não encripta os dados separadamente por utilizador.

## Privacidade dos prestadores de serviços

<span class="pg-teal">:material-server-network: Fornecedores de serviços</span>

Vivemos num mundo em que quase tudo está ligado à Internet. As nossas mensagens "privadas", e-mails e interações sociais são normalmente armazenadas num servidor, em qualquer parte do mundo. Geralmente, quando envia uma mensagem a alguém, esta é armazenada num servidor e, quando o seu amigo quer ler a mensagem, o servidor mostra-a.

Há um problema óbvio devido ao facto do fornecedor de serviços (ou um hacker que tenha comprometido o servidor) poder aceder às conversas quando e como quiser, sem que o utilizador alguma vez o saiba. Isto aplica-se a muitos serviços comuns, como as mensagens SMS, o Telegram e o Discord.

Felizmente, a E2EE pode aliviar este problema, através da encriptação das comunicações entre si e os seus destinatários, antes mesmo de serem enviadas para o servidor. A confidencialidade das suas mensagens é garantida, assumindo que o fornecedor de serviços não tem acesso às chaves privadas de nenhuma das partes.

!!! nota "Nota sobre a encriptação baseada na Web"

    Na prática, a eficácia das diferentes implementações E2EE varia. As aplicações, como o [Signal](../real-time-communication.md#signal), são executadas nativamente no seu dispositivo e todas as cópias da aplicação são as mesmas em diferentes instalações. Se o fornecedor de serviços introduzisse um [backdoor](https://en.wikipedia.org/wiki/Backdoor_(computing)) na sua aplicação - numa tentativa de roubar as suas chaves privadas - esse facto poderia mais tarde ser detetado através de [engenharia inversa] (https://en.wikipedia.org/wiki/Reverse_engineering).
    
    Por outro lado, as implementações E2EE baseadas na Web, como o webmail do Proton Mail ou o *Web Vault* da Bitwarden, dependem do servidor que fornece dinamicamente código JavaScript ao browser para tratar da criptografia. Um servidor malicioso pode visá-lo e enviar-lhe código JavaScript malicioso para roubar a sua chave de encriptação (e seria extremamente difícil de notar). Uma vez que o servidor pode optar por servir clientes Web diferentes a pessoas diferentes - mesmo que se tenha apercebido do ataque - seria incrivelmente difícil provar a culpa do fornecedor.
    
    Por conseguinte, sempre que possível, deve utilizar aplicações nativas em vez de clientes Web.

Mesmo com a E2EE, os fornecedores de serviços podem ainda traçar o seu perfil com base nos **metadados**, que normalmente não estão protegidos. Embora o fornecedor de serviços não possa ler as suas mensagens, pode observar coisas importantes, como com quem está a falar, com que frequência lhes envia mensagens e quando está normalmente ativo. A proteção de metadados é bastante invulgar e, se estiver incluída no seu [modelo de ameaças](threat-modeling.md), deve prestar muita atenção à documentação técnica do software que está a utilizar, de forma a verificar se existe alguma minimização ou proteção de metadados.

## Programas de vigilância em massa

<span class="pg-blue">:material-eye-outline: Vigilância em massa</span>

A vigilância em massa é o esforço intrincado para monitorizar o "comportamento, atividades ou informações" de toda uma população (ou de uma sua fração substancial).[^1] Refere-se frequentemente a programas governamentais, como os [ revelados por Edward Snowden em 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). No entanto, também pode ser efetuada por empresas, quer em nome de agências governamentais, quer por sua própria iniciativa.

!!! resumo "Atlas da Vigilância"

    Se quiser saber mais sobre os métodos de vigilância e a forma como são aplicados na sua cidade, pode consultar o [Atlas da Vigilância] (https://atlasofsurveillance.org/) da [Electronic Frontier Foundation] (https://www.eff.org/).
    
    Em França, pode consultar o [site Technolopolice] (https://technopolice.fr/villes/), mantido pela associação sem fins lucrativos La Quadrature du Net.

Os governos justificam frequentemente os programas de vigilância em massa como meios necessários para combater o terrorismo e prevenir a criminalidade. No entanto, e violando os direitos humanos, é mais frequentemente utilizado para atingir de forma desproporcionada grupos minoritários e dissidentes políticos, entre outros.

!!! quote "ACLU: [*A lição de privacidade do 11 de setembro: A vigilância em massa não é o caminho a seguir*](https://www.aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward)"

    Perante [as revelações de Edward Snowden sobre programas governamentais como [PRISM](https://en.wikipedia.org/wiki/PRISM) e [Upstream](https://en.wikipedia.org/wiki/Upstream_collection)], os funcionários dos serviços secretos também admitiram que a NSA recolhia secretamente, há anos, registos sobre praticamente todas as chamadas telefónicas dos americanos - quem liga a quem, quando são feitas e quanto tempo duram. Este tipo de informação, quando recolhida pela NSA dia após dia, pode revelar pormenores incrivelmente sensíveis sobre a vida e as associações das pessoas, como por exemplo, se telefonaram a um pastor, a um fornecedor de abortos, a um conselheiro de toxicodependência ou a uma linha de apoio ao suicídio.

Apesar da crescente vigilância em massa nos Estados Unidos, o governo concluiu que os programas de vigilância em massa, como a Secção 215, têm tido "pouco valor único" no que diz respeito a impedir crimes reais ou conspirações terroristas, com esforços que duplicam em grande parte os programas de vigilância direcionada do próprio FBI.[^2]

Enquanto online, pode ser seguido através de uma variedade de métodos:

- O seu endereço IP
- Cookies do browser
- Os dados que submete a sites
- A impressão digital do seu browser ou dispositivo
- Correlação dos métodos de pagamento

\[Esta não é uma lista exaustiva].

Se estiver preocupado com os programas de vigilância em massa, pode utilizar estratégias como compartimentar as suas identidades online, misturar-se com outros utilizadores ou, sempre que possível, simplesmente evitar fornecer informações de identificação.

<span class="pg-brown">:material-account-cash: Capitalismo de vigilância</span>

> O capitalismo de vigilância é um sistema económico centrado na captura e mercantilização de dados pessoais, com o objetivo principal de gerar lucro.[^3]

Para muitas pessoas, a localização e vigilância por parte de empresas privadas é uma preocupação crescente. As redes de marketing omnipresentes, como as operadas pela Google e pelo Facebook, abrangem a Internet muito para além dos sites que controlam, acompanhando todas as suas ações ao longo da sua jornada de navegação. A utilização de ferramentas tais como bloqueadores de conteúdos para limitar os pedidos de rede aos seus servidores, bem como a leitura das políticas de privacidade dos serviços que utiliza, pode ajudá-lo a evitar muitos adversários básicos (embora não possa impedir completamente o rastreio).[^4]

Além disso, mesmo as empresas que não pertencem à *AdTech* ou à indústria de rastreio podem partilhar as suas informações com [corretores de dados](https://en.wikipedia.org/wiki/Information_broker) (como a Cambridge Analytica, a Experian ou a Datalogix) ou outras partes. Não pode assumir que os seus dados estão seguros só porque o serviço que está a utilizar não se enquadra no modelo de negócio típico da AdTech ou do rastreio. A proteção mais forte contra a recolha de dados empresariais é encriptar ou ofuscar os seus dados sempre que possível, dificultando a correlação entre os dados de diferentes fornecedores e a criação de um perfil sobre si.

## Limitação da informação pública

<span class="pg-green">:material-account-search: Exposição pública</span>

A melhor forma de manter os seus dados privados é simplesmente não os tornar públicos. A eliminação de informações indesejadas que encontra online é um dos melhores primeiros passos que pode dar para recuperar a sua privacidade.

- [Veja o nosso guia sobre a eliminação de contas :material-arrow-right-drop-circle:](account-deletion.md)

Nos sites onde partilha informações, é muito importante verificar as definições de privacidade da sua conta, de forma a limitar a divulgação desses dados. Por exemplo, ative o "modo privado" nas suas contas, se tiver essa opção: assim, garante que a sua conta não está a ser indexada pelos motores de busca e que não pode ser visualizada sem a sua autorização.

Se já submeteu as suas informações reais a sites que não as deveriam ter, considere a possibilidade de utilizar táticas de desinformação, como submeter informações fictícias relacionadas com essa identidade online. Isso torna as suas informações reais indistinguíveis das falsas.

## Evitar a Censura

<span class="pg-blue-gray">:material-close-outline: Censura</span>

A censura online pode ser realizada (em diferentes graus) por diversos atores, incluindo governos totalitários, administradores de redes e prestadores de serviços. Estes esforços para controlar a comunicação e restringir o acesso à informação serão sempre incompatíveis com o direito humano à liberdade de expressão.[^5]

A censura nas plataformas corporativas é cada vez mais comum, uma vez que plataformas como o Twitter e o Facebook cedem à procura pública, às pressões do mercado e às pressões das agências governamentais. As pressões do governo podem ser solicitações dissimuladas a empresas, como no caso em que a Casa Branca [solicitou a retirada](https://www.nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) de um vídeo provocador do YouTube, ou, de forma evidente, quando o Governo chinês exige que as empresas respeitem um regime rigoroso de censura.

As pessoas que se preocupam com a ameaça da censura podem usar tecnologias como o [Tor](../advanced/tor-overview.md) para contorná-la, e utilizar plataformas de comunicação resistentes à censura, como o [Matrix](../real-time-communication.md#element), que não tem uma autoridade de conta centralizada que pode fechar as contas arbitrariamente.

!!! dica

    Enquanto evitar a censura em si pode ser fácil, esconder esse facto pode ser muito problemático.
    
    Deve considerar quais os aspetos da rede que o seu adversário pode observar e se tem negação plausível das suas ações. Por exemplo, usar [DNS criptografado](../advanced/dns-overview.md#what-is-encrypted-dns) pode ajudá-lo a contornar sistemas rudimentares de censura baseados em DNS, mas não pode realmente esconder as suas atividades online do seu ISP. Uma VPN ou o Tor podem ajudar a esconder o que está a visitar dos administradores de rede, mas não pode esconder o facto de estar a usar essas redes. Transportes conectáveis (como Obfs4proxy, Meek ou Shadowsocks) podem ajudá-lo a evitar firewalls que bloqueiam protocolos VPN comuns ou Tor, mas as suas tentativas de contornar o problema podem ser detetadas através de métodos como sondagem ou [inspeção profunda de pacotes](https://en. wikipedia.org/wiki/Deep_packet_inspection).

Deve sempre considerar os riscos de tentar contornar a censura, as possíveis consequências e o quão sofisticado o seu adversário pode ser. Deve ser cauteloso com a sua seleção de software e ter um plano de backup, caso seja apanhado.

[^1]: Wikipedia: [*Vigilância em massa*](https://en.wikipedia.org/wiki/Mass_surveillance) e [*Vigilância*](https: //en.wikipedia.org/wiki/Surveillance).
[^2]: Conselho de Supervisão de Privacidade e Liberdades Civis dos Estados Unidos: [*Relatório sobre o Programa de Registos Telefónicos Conduzido ao abrigo da Secção 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Capitalismo de vigilância<*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerar maldades](https://www.ranum.com/security/computer_security/editorials/dumb/)" (ou "listar todas as coisas más que conhecemos"), como muitos bloqueadores de anúncios e programas antivírus, não o protegem adequadamente contra novas ameaças ou ameaças desconhecidas, dado estas aindam não terem sido adicionadas à lista de filtros. Deve empregar outras técnicas de mitigação.
[^5]: Nações Unidas: [*Declaração Universal dos Direitos Humanos *](https://www.un.org/en/about-us/universal-declaration-of-human-rights).
