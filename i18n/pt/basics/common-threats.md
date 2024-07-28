---
title: "Ameaças comuns"
icon: 'material/eye-outline'
description: Cada utilizador tem o seu modelo de ameaça, mas estes são alguns dos aspetos que interessam a muitos visitantes deste site.
---

Em termos gerais, categorizamos as nossas recomendações no tipo de [ameaças](threat-modeling.md) ou objetivos que se aplicam à maioria das pessoas. ==Pode preocupar-se com nenhuma, uma, algumas ou todas estas possibilidades==, e as ferramentas e serviços que utiliza dependem dos seus objetivos. Também pode ter ameaças específicas fora destas categorias, o que é perfeitamente normal! O que importa realmente é que compreenda as vantagens e desvantagens das ferramentas que escolher, uma vez que praticamente nenhuma delas o protegerá de todas as ameaças.

- <span class="pg-purple">:material-incognito: Anonimato</span> - Protege a sua atividade online da sua identidade real, protegendo-o de pessoas que estão a tentar descobrir *a sua * identidade.
- <span class="pg-red">:material-target-account: Ataques direcionados</span> - Estar protegido contra hackers ou outros agentes maliciosos que estão a tentar obter acesso aos *seus* dados ou dispositivos.
- <span class="pg-orange">:material-bug-outline: Ataques passivos</span> - Estar protegido contra coisas como malware, violações de dados e outros ataques que são feitos contra muitas pessoas ao mesmo tempo.
- <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span> - A vulnerability or exploit introduced into otherwise good software either directly or through a dependency from a third party.
- <span class="pg-teal">:material-server-network: Fornecedores de serviços</span> - Proteger os seus dados dos fornecedores de serviços (por exemplo, com E2EE, que torna os seus dados ilegíveis para o servidor).
- <span class="pg-blue">:material-eye-outline: Vigilância em massa</span> - Proteção contra agências governamentais, organizações, sites e serviços que trabalham em conjunto para seguir as suas atividades.
- <span class="pg-brown">:material-account-cash: Capitalismo de vigilância</span> - Proteger-se das grandes redes de marketing, como o Google e o Facebook, bem como de uma miríade de outros coletores de dados de terceiros.
- <span class="pg-green">:material-account-search: Exposição pública</span> - Limitar as informações sobre si que estão acessíveis online - para motores de busca ou para o público em geral.
- <span class="pg-blue-gray">:material-close-outline: Censura</span> - Evitar a censura ao acesso de informações ou quando nos expressamos online.

Algumas destas ameaças podem ser mais importantes para si do que outras, dependendo das suas preocupações específicas. For example, a software developer with access to valuable or critical data may be primarily concerned with <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span> and <span class="pg-red">:material-target-account: Targeted Attacks</span>. They will likely still want to protect their personal data from being swept up in <span class="pg-blue">:material-eye-outline: Mass Surveillance</span> programs. Da mesma forma, muitas pessoas podem estar principalmente preocupadas com a <span class="pg-green">:material-account-search: Exposição pública</span> dos seus dados pessoais, mas podem também importar-se com questões de segurança, como <span class="pg-orange">:material-bug-outline: Ataques passivos</span>- como o malware que afeta os seus dispositivos.

## Anonimato vs. Privacidade

<span class="pg-purple">:material-incognito: Anonimato</span>

O anonimato é muitas vezes confundido com a privacidade, mas são conceitos distintos. Enquanto a privacidade é um conjunto de escolhas que faz sobre a forma como os seus dados são utilizados e partilhados, o anonimato é a dissociação completa das suas atividades online da sua identidade real.

Os denunciantes e os jornalistas, por exemplo, podem ter um modelo de ameaça muito mais extremo, que exige o anonimato total. Não se trata apenas de esconder o que fazem, os dados que possuem e de não serem pirateados por agentes maliciosos ou governos, mas também de esconder totalmente quem são. Muitas vezes, sacrificarão qualquer tipo de conveniência se isso significar proteger o seu anonimato, privacidade ou segurança, porque as suas vidas podem depender disso. A maioria das pessoas não precisa de ir tão longe.

## Segurança e Privacidade

<span class="pg-orange">:material-bug-outline: Ataques passivos</span>

A segurança e a privacidade também são frequentemente confundidas, uma vez que é necessária segurança para obter privacidade: A utilização de ferramentas - mesmo que sejam privadas por conceção - é inútil se puderem ser facilmente exploradas por atacantes que mais tarde divulgam os seus dados. No entanto, o inverso não é necessariamente verdadeiro: o serviço mais seguro do mundo *não é necessariamente* orientado para as questões da privacidade. O melhor exemplo disto é a confiança que depositamos na Google que, embora com uma escala muito significativa, tem tido poucos incidentes de segurança, o que consegue através do concurso de especialistas em segurança líderes do setor. Embora a Google forneça serviços muito seguros, poucas pessoas consideram os seus dados protegidos contra olhares indiscretos, sobretudo nos produtos gratuitos da Google (Gmail, YouTube, etc.)

No que diz respeito à segurança das aplicações, geralmente não sabemos (e por vezes não podemos saber) se o software que utilizamos é malicioso ou se poderá um dia tornar-se malicioso. Mesmo com os programadores mais fiáveis, geralmente não há garantia de que o seu software não tenha uma vulnerabilidade grave que possa ser explorada mais tarde.

Para minimizar os danos que um software malicioso *pode* causar, deve utilizar a segurança por compartimentação. Essa compartimentação pode ser conseguida na forma de utilização de computadores diferentes para trabalhos diferentes, utilização de máquinas virtuais para separar diferentes grupos de aplicações relacionadas ou utilização de um sistema operativo seguro com uma forte ênfase na solução de sandbox das aplicações e no controlo de acesso obrigatório.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Os sistemas operativos móveis têm geralmente uma melhor proteção das aplicações do que os sistemas operativos de secretária: as aplicações não podem obter acesso à raiz e necessitam de permissão para aceder aos recursos do sistema.

Os sistemas operativos para desktop deixam a desejar no que diz respeito a uma adequada proteção. O ChromeOS tem capacidades de sandbox semelhantes às do Android e o macOS tem controlo total das permissões do sistema (e os programadores podem optar pela sandbox para as aplicações). No entanto, estes sistemas operativos transmitem informações de identificação aos respectivos OEMs. O Linux tende a não enviar informações aos fornecedores de sistemas, mas tem uma fraca proteção contra exploits e aplicações maliciosas. This can be mitigated somewhat with specialized distributions which make significant use of virtual machines or containers, such as [Qubes OS](../desktop.md#qubes-os).

</div>

<span class="pg-red">:material-target-account: Ataques direcionados</span>

Os ataques direcionados contra uma pessoa específica são mais problemáticos de tratar. Os ataques mais comuns incluem o envio de documentos maliciosos por e-mail, a exploração de vulnerabilidades (por exemplo, em navegadores e sistemas operativos) e ataques físicos. Se isto for uma preocupação para si, deve utilizar estratégias de mitigação de ameaças mais avançadas.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Por definição, os **browsers**, os **clientes de e-mail** e as **suites de escritório** executam normalmente código não fiável, enviado por terceiros. Executar várias máquinas virtuais - para separar aplicações como estas do seu sistema anfitrião, bem como umas das outras - é uma técnica que pode utilizar para reduzir a possibilidade de uma exploração nestas aplicações poder comprometer o resto do seu sistema. Por exemplo, tecnologias como o Qubes OS ou o Microsoft Defender Application Guard no Windows fornecem métodos convenientes para o fazer.

</div>

If you are concerned about **physical attacks** you should use an operating system with a secure verified boot implementation, such as Android, iOS, macOS, or [Windows (with TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). Deve também certificar-se de que a sua unidade está encriptada e que o sistema operativo utiliza um TPM, Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) ou [Element](https://developers.google.com/android/security/android-ready-se) para limitar as tentativas de introdução da frase-chave de encriptação. Deve evitar partilhar o seu computador com pessoas em quem não confia, uma vez que a maioria dos sistemas operativos de computador de secretária não encripta os dados separadamente por utilizador.

<span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>

Supply chain attacks are frequently a form of <span class="pg-red">:material-target-account: Targeted Attack</span> towards businesses, governments, and activists, although they can end up compromising the public at large as well.

<div class="admonition example" markdown>
<p class="admonition-title">Example</p>

A notable example of this occurred in 2017 when M.E.Doc, a popular accounting software in Ukraine, was infected with the *NotPetya* virus, subsequently infecting people who downloaded that software with ransomware. NotPetya itself was a ransomware attack which impacted 2000+ companies in various countries, and was based on the *EternalBlue* exploit developed by the NSA to attack Windows computers over the network.

</div>

There are few ways in which this type of attack might be carried out:

1. A contributor or employee might work their way into a position of power within a project or organization, then abuse that position by adding malicious code.
2. A developer may be coerced by an outside party to add malicious code.
3. An individual or group might identify a third party software dependency (also known as a library) and work to infiltrate it with the above two methods, knowing that it will be used by "downstream" software developers.

These sorts of attacks can require a lot of time and preparation to perform and are risky because they can be detected, particularly in open source projects if they are popular and have outside interest. Unfortunately they're also one of the most dangerous as they are very hard to mitigate entirely. We would encourage readers only use software which has a good reputation and makes an effort to reduce risk by:

1. Only adopting popular software that has been around for a while. The more interest in a project the greater likelihood that external parties will notice malicious changes. A malicious actor will also need to spend more time gaining community trust with meaningful contributions.
2. Finding software which releases binaries with widely-used, trusted build infrastructure platforms, as opposed to developer workstations or self-hosted servers. Some systems like GitHub Actions let you inspect the build script that runs publicly for extra confidence. This lessens the likelihood that malware on a developer's machine could infect their packages, and gives confidence that the binaries produced are in fact produced correctly.
3. Looking for code signing on individual source code commits and releases, which creates an auditable trail of who did what. For example: Was the malicious code in the software repository? Which developer added it? Was it added during the build process?
4. Checking whether the source code has meaningful commit messages (such as [conventional commits](https://conventionalcommits.org)) which explain what the change is supposed to accomplish. Clear messages can make it easier for outsiders to the project to verify, audit, and find bugs.
5. Noting the number of contributors or maintainers a program has. A lone developer may be more susceptible to being coerced into adding malicious code by an external party, or to negligently enable undesirable behavior. This may very well mean software developed by "Big Tech" has more scrutiny than a lone developer who doesn't answer to anyone.

## Privacidade dos prestadores de serviços

<span class="pg-teal">:material-server-network: Fornecedores de serviços</span>

Vivemos num mundo em que quase tudo está ligado à Internet. As nossas mensagens "privadas", e-mails e interações sociais são normalmente armazenadas num servidor, em qualquer parte do mundo. Geralmente, quando envia uma mensagem a alguém, esta é armazenada num servidor e, quando o seu amigo quer ler a mensagem, o servidor mostra-a.

Há um problema óbvio devido ao facto do fornecedor de serviços (ou um hacker que tenha comprometido o servidor) poder aceder às conversas quando e como quiser, sem que o utilizador alguma vez o saiba. Isto aplica-se a muitos serviços comuns, como as mensagens SMS, o Telegram e o Discord.

Felizmente, a E2EE pode aliviar este problema, através da encriptação das comunicações entre si e os seus destinatários, antes mesmo de serem enviadas para o servidor. A confidencialidade das suas mensagens é garantida, assumindo que o fornecedor de serviços não tem acesso às chaves privadas de nenhuma das partes.

<div class="admonition note" markdown>
<p class="admonition-title">Note on Web-based Encryption</p>

Na prática, a eficácia das diferentes implementações E2EE varia. As aplicações, como o [Signal](../real-time-communication.md#signal), são executadas nativamente no seu dispositivo e todas as cópias da aplicação são as mesmas em diferentes instalações. Se o fornecedor de serviços introduzisse um [backdoor](https://en.wikipedia.org/wiki/Backdoor_(computing)) na sua aplicação - numa tentativa de roubar as suas chaves privadas - esse facto poderia mais tarde ser detetado através de [engenharia inversa] (https://en.wikipedia.org/wiki/Reverse_engineering).

Por outro lado, as implementações E2EE baseadas na Web, como o webmail do Proton Mail ou o *Web Vault* da Bitwarden, dependem do servidor que fornece dinamicamente código JavaScript ao browser para tratar da criptografia. Um servidor malicioso pode visá-lo e enviar-lhe código JavaScript malicioso para roubar a sua chave de encriptação (e seria extremamente difícil de notar). Uma vez que o servidor pode optar por servir clientes Web diferentes a pessoas diferentes - mesmo que se tenha apercebido do ataque - seria incrivelmente difícil provar a culpa do fornecedor.

Por conseguinte, sempre que possível, deve utilizar aplicações nativas em vez de clientes Web.

</div>

Mesmo com a E2EE, os fornecedores de serviços podem ainda traçar o seu perfil com base nos **metadados**, que normalmente não estão protegidos. Embora o fornecedor de serviços não possa ler as suas mensagens, pode observar coisas importantes, como com quem está a falar, com que frequência lhes envia mensagens e quando está normalmente ativo. A proteção de metadados é bastante invulgar e, se estiver incluída no seu [modelo de ameaças](threat-modeling.md), deve prestar muita atenção à documentação técnica do software que está a utilizar, de forma a verificar se existe alguma minimização ou proteção de metadados.

## Programas de vigilância em massa

<span class="pg-blue">:material-eye-outline: Vigilância em massa</span>

A vigilância em massa é o esforço intrincado para monitorizar o "comportamento, atividades ou informações" de toda uma população (ou de uma sua fração substancial).[^1] Refere-se frequentemente a programas governamentais, como os [ revelados por Edward Snowden em 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). No entanto, também pode ser efetuada por empresas, quer em nome de agências governamentais, quer por sua própria iniciativa.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

Os governos justificam frequentemente os programas de vigilância em massa como meios necessários para combater o terrorismo e prevenir a criminalidade. No entanto, e violando os direitos humanos, é mais frequentemente utilizado para atingir de forma desproporcionada grupos minoritários e dissidentes políticos, entre outros.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

In the face of Edward Snowden's disclosures of government programs such as [PRISM](https://en.wikipedia.org/wiki/PRISM) and [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), intelligence officials also admitted that the NSA had for years been secretly collecting records about virtually every American’s phone calls — who’s calling whom, when those calls are made, and how long they last. Este tipo de informação, quando recolhida pela NSA dia após dia, pode revelar pormenores incrivelmente sensíveis sobre a vida e as associações das pessoas, como por exemplo, se telefonaram a um pastor, a um fornecedor de abortos, a um conselheiro de toxicodependência ou a uma linha de apoio ao suicídio.

</div>

Apesar da crescente vigilância em massa nos Estados Unidos, o governo concluiu que os programas de vigilância em massa, como a Secção 215, têm tido "pouco valor único" no que diz respeito a impedir crimes reais ou conspirações terroristas, com esforços que duplicam em grande parte os programas de vigilância direcionada do próprio FBI.[^2]

Enquanto online, pode ser seguido através de uma variedade de métodos:

- O seu endereço IP
- Cookies do browser
- Os dados que submete a sites
- A impressão digital do seu browser ou dispositivo
- Correlação dos métodos de pagamento

\[Esta não é uma lista exaustiva].

If you're concerned about mass surveillance programs, you can use strategies like compartmentalizing your online identities, blending in with other users, or, whenever possible, simply avoiding giving out identifying information.

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

A censura nas plataformas corporativas é cada vez mais comum, uma vez que plataformas como o Twitter e o Facebook cedem à procura pública, às pressões do mercado e às pressões das agências governamentais. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

As pessoas que se preocupam com a ameaça da censura podem usar tecnologias como o [Tor](../advanced/tor-overview.md) para contorná-la, e utilizar plataformas de comunicação resistentes à censura, como o [Matrix](../real-time-communication.md#element), que não tem uma autoridade de conta centralizada que pode fechar as contas arbitrariamente.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Enquanto evitar a censura em si pode ser fácil, esconder esse facto pode ser muito problemático.

Deve considerar quais os aspetos da rede que o seu adversário pode observar e se tem negação plausível das suas ações. Por exemplo, usar [DNS criptografado](../advanced/dns-overview.md#what-is-encrypted-dns) pode ajudá-lo a contornar sistemas rudimentares de censura baseados em DNS, mas não pode realmente esconder as suas atividades online do seu ISP. Uma VPN ou o Tor podem ajudar a esconder o que está a visitar dos administradores de rede, mas não pode esconder o facto de estar a usar essas redes. Transportes conectáveis (como Obfs4proxy, Meek ou Shadowsocks) podem ajudá-lo a evitar firewalls que bloqueiam protocolos VPN comuns ou Tor, mas as suas tentativas de contornar o problema podem ser detetadas através de métodos como sondagem ou [inspeção profunda de pacotes](https://en. wikipedia.org/wiki/Deep_packet_inspection).

</div>

Deve sempre considerar os riscos de tentar contornar a censura, as possíveis consequências e o quão sofisticado o seu adversário pode ser. Deve ser cauteloso com a sua seleção de software e ter um plano de backup, caso seja apanhado.

[^1]: Wikipedia: [*Vigilância em massa*](https://en.wikipedia.org/wiki/Mass_surveillance) e [*Vigilância*](https: //en.wikipedia.org/wiki/Surveillance).
[^2]: Conselho de Supervisão de Privacidade e Liberdades Civis dos Estados Unidos: [*Relatório sobre o Programa de Registos Telefónicos Conduzido ao abrigo da Secção 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Capitalismo de vigilância<*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. Deve empregar outras técnicas de mitigação.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
