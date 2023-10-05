---
meta_title: "As melhores aplicações de mensagens instantâneas com foco na privacidade - Privacy Guides"
title: "Comunicação em tempo real"
icon: material/chat-processing
description: Outras aplicações de mensagens instantâneas disponibilizam todas as suas conversas privadas à empresa que as gere.
cover: real-time-communication.png
---

Estas são as nossas recomendações para comunicação encriptada em tempo real.

[Tipos de redes de comunicação :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## Aplicações de mensagens encriptadas

Estas aplicações de mensagens são ótimas para proteger as suas comunicações sensíveis.

### Signal

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Signal](assets/img/messengers/signal.svg){ align=right }
    
    **Signal** é uma aplicação para dispositivos móveis desenvolvida pela Signal Messenger LLC. A aplicação permite o envio de mensagens instantâneas, bem como chamadas de voz e vídeo.
    
    Todas as comunicações são E2EE. As listas de contactos são encriptadas utilizando o PIN do Signal e o servidor não tem acesso a elas. Os perfis pessoais também são encriptados e apenas são partilhados com os contactos com quem conversa.
    
    [:octicons-home-16: Homepage](https://signal.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://support.signal.org/hc/en-us){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/signalapp){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://signal.org/donate/){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
        - [:simple-android: Android](https://signal.org/android/apk/)
        - [:simple-windows11: Windows](https://signal.org/download/windows)
        - [:simple-apple: macOS](https://signal.org/download/macos)
        - [:simple-linux: Linux](https://signal.org/download/linux)

O Signal suporta [grupos privados](https://signal.org/blog/signal-private-group-system/). O servidor não tem qualquer registo dos grupos a que pertence, títulos de grupo, avatares de grupo ou atributos de grupo. O Signal tem metadados mínimos quando se ativa o[Sealed Sender](https://signal.org/blog/sealed-sender/). O endereço do remetente é encriptado juntamente com o corpo da mensagem e apenas o endereço do destinatário é visível para o servidor. O Sealed Sender só está ativado para as pessoas da sua lista de contactos, mas pode ser ativado para todos os destinatários, com o risco acrescido de poder receber spam. O Signal requer o seu número de telefone como identificador pessoal.

O protocolo foi objeto de uma [auditoria](https://eprint.iacr.org/2016/1013.pdf) independente em 2016. A especificação do protocolo Signal pode ser encontrada na sua [documentação](https://signal.org/docs/).

Temos algumas dicas adicionais sobre como configurar e fortalecer a sua instalação do Signal:

[Configuração e robustecimento do Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening/)

### SimpleX Chat

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Simplex](assets/img/messengers/simplex.svg){ align=right }
    
    O **SimpleX** Chat é uma aplicação descentralizada de mensagens instantâneas e não depende de quaisquer identificadores únicos, tais como números de telefone ou nomes de utilizador. Os utilizadores do SimpleX Chat podem fazer scan a um código QR ou clicar numa ligação de convite para participar em conversas de grupo.
    
    [:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Código-fonte" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/simplex-chat/id1605771084)
        - [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
        - [:simple-windows11: Windows](https://simplex.chat/downloads/#desktop-app)
        - [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
        - [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

O SimpleX Chat [foi auditado](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) por Trail of Bits, em outubro de 2022.

SimpleX Chat supports basic group chatting functionality, direct messaging, and editing of messages and markdown. Chamadas de áudio e vídeo E2EE também são suportadas. Os seus dados podem ser exportados e importados para outro dispositivo, dado não existirem servidores centrais com cópias de segurança.

### Briar

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Briar](assets/img/messengers/briar.svg){ align=right }
    
    O **Briar** é uma aplicação de mensagens instantâneas encriptada que [connects](https://briarproject.org/how-it-works/) a outros clientes, usando a rede Tor. O Briar pode ligar-se através de Wi-Fi ou Bluetooth. O modo de rede local do Briar pode ser útil, quando não estiver garantida a disponibilidade da Internet.
    
    [:octicons-home-16: Homepage](https://briarproject.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://briarproject.org/privacy-policy/){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentação}
    [:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://briarproject.org/){ .card-link title="As opções de donativos estão listadas na parte inferior da página inicial" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
        - [:simple-windows11: Windows](https://briarproject.org/download-briar-desktop/)
        - [:simple-linux: Linux](https://briarproject.org/download-briar-desktop/)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

Para adicionar um contacto no Briar, é necessário que você e o contacto se adicionem mutuamente. Pode trocar links `briar://` ou digitalizar o código QR de um contacto, se este estiver próximo.

O software cliente foi [auditado de forma independente](https://briarproject.org/news/2017-beta-released-security-audit/), e o protocolo de encaminhamento anónimo utiliza a rede Tor, que também foi auditada.

O Briar publicou na íntegra a sua [especificação](https://code.briarproject.org/briar/briar-spec).

O Briar suporta Forward Secrecy, através do Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) e do [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md).

## Opções adicionais

!!! aviso

    Estas aplicações de mensagens instantâneas não têm [Forward Secrecy] (https://en.wikipedia.org/wiki/Forward_secrecy) e, embora satisfaçam certas necessidades que as nossas recomendações anteriores não podem satisfazer, não os recomendamos para comunicações de longo prazo ou sensíveis. Qualquer comprometimento da chave entre os destinatários da mensagem afetará a confidencialidade de **todas** as comunicações anteriores.

### Element

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Element](assets/img/messengers/element.svg){ align=right }
    
    **Element** é o cliente de referência para o protocolo [Matrix](https://matrix.org/docs/guides/introduction), uma [norma aberta](https://matrix.org/docs/spec) para comunicação segura e descentralizada, em tempo real.
    
    As mensagens e os ficheiros partilhados em salas privadas (que requerem um convite) são, por defeito, E2EE, tal como as chamadas de voz e de vídeo, de um para um.
    
    [:octicons-home-16: Homepage](https://element.io/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://element.io/privacy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://element.io/help){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/vetor-im){ .card-link title="Código-fonte" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
        - [:simple-appstore: App Store](https://apps.apple.com/app/vector/id1083446067)
        - [:simple-github: GitHub](https://github.com/vector-im/element-android/releases)
        - [:simple-windows11: Windows](https://element.io/get-started)
        - [:simple-apple: macOS](https://element.io/get-started)
        - [:simple-linux: Linux](https://element.io/get-started)
        - [:octicons-globe-16: Web](https://app.element.io)

As imagens de perfil, as reações e os nicknames não são encriptados.

As chamadas de voz e vídeo em grupo [não são](https://github.com/vector-im/element-web/issues/12878) E2EE e utilizam Jitsi, mas espera-se que esta situação se altere com o [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401). Atualmente, as chamadas de grupo [não têm autenticação](https://github.com/vector-im/element-web/issues/13074), o que significa que os participantes que não estão na sala também podem juntar-se às chamadas. Recomendamos que não utilize esta funcionalidade para reuniões privadas.

O próprio protocolo Matrix [suporta teoricamente o PFS](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy), no entanto, este [não é atualmente suportado no Element](https://github.com/vector-im/element-web/issues/7101) devido aos problemas que provoca em alguns aspetos da experiência do utilizador, como as cópias de segurança de chaves e o histórico de mensagens partilhadas.

O protocolo foi objeto de uma [auditoria independente](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) em 2016. A especificação do protocolo Matrix pode ser encontrada na sua [documentação](https://spec.matrix.org/latest/). O [Olm](https://matrix.org/docs/projects/other/olm) criptográfico utilizado pelo Matrix é uma implementação do algoritmo [Double Ratchet da Signal](https://signal.org/docs/specifications/doubleratchet/).

### Session

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Session](assets/img/messengers/session.svg){ align=right }
    
    **Session** é uma aplicação descentralizada de mensagens instantâneas com foco em comunicações privadas, seguras e anónimas. A sessão oferece suporte para mensagens diretas, conversas de grupo e chamadas de voz.
    
    O Session utiliza a rede descentralizada [Oxen Service Node Network] (https://oxen.io/) para armazenar e encaminhar mensagens. Cada mensagem encriptada é encaminhada através de três nós na Oxen Service Node Network, tornando virtualmente impossível que os nós compilem informação significativa sobre aqueles que utilizam a rede.
    
    [:octicons-home-16: Homepage](https://getsession.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Código-fonte" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
        - [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
        - [:simple-windows11: Windows](https://getsession.org/download)
        - [:simple-apple: macOS](https://getsession.org/download)
        - [:simple-linux: Linux](https://getsession.org/download)

O Session permite E2EE em conversas individuais ou em grupos fechados com um máximo de 100 membros. Os grupos abertos não têm restrições quanto ao número de membros, mas são abertos por definição.

O Session [não](https://getsession.org/blog/session-protocol-technical-information) suporta PFS, que é quando um sistema de encriptação altera automática e frequentemente as chaves que utiliza para encriptar e desencriptar informações, de modo a que, se a chave mais recente for comprometida, exponha uma parte reduzida de informações sensíveis.

A Oxen solicitou uma auditoria independente para o Session, em março de 2020. Em abril de 2021, a auditoria [concluiu](https://getsession.org/session-code-audit): "O nível geral de segurança desta aplicação é bom e torna-a utilizável por pessoas preocupadas com a privacidade."

O Session tem um [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) que descreve os aspetos técnicos da aplicação e do protocolo.

## Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

!!! exemplo "Esta secção é nova"

    Estamos a trabalhar no sentido de estabelecer critérios para cada secção do nosso site, o que pode originar alterações. Se tiver alguma dúvida sobre os critérios utilizados, por favor [pergunte no nosso fórum] (https://discuss.privacyguides.net/latest) e não parta do princípio de que algo foi excluído das nossas recomendações, caso não esteja listado aqui. São muitos os fatores considerados e discutidos quando recomendamos um projeto, e documentar cada um deles é um trabalho em curso.

- Deve ter clientes de código aberto.
- Deve utilizar o E2EE para mensagens privadas por defeito.
- Deve suportar E2EE para todas as mensagens.
- Deve ter sido objeto de uma auditoria independente.

### Melhor caso

Os nossos melhores critérios representam o que gostaríamos de ver num projeto perfeito desta categoria. As nossas recomendações podem não incluir todas as funcionalidades, mas incluem as que, na nossa opinião, têm um impacto mais elevado.

- Deve ter o Forward Secrecy.
- Deve ter servidores de código aberto.
- Deve ser descentralizado, ou seja, federado ou P2P.
- Deve utilizar o E2EE para todas as mensagens por defeito.
- Deve ser compatível com Linux, macOS, Windows, Android e iOS.
