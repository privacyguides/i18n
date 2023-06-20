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

O SimpleX Chat [foi auditado](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) por Trail of Bits, em outubro de 2022.

Atualmente, o SimpleX Chat apenas disponibiliza clientes para Android e iOS. São suportadas as funcionalidades básicas de conversação em grupo, mensagens diretas, edição de mensagens e markdown. E2EE Audio and Video calls are also supported.

Your data can be exported, and imported onto another device, as there are no central servers where this is backed up.

### Briar

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![logótipo Briar](/assets/img/messengers/briar.svg){ align=right }
    
    **Briar** é um mensageiro instantâneo encriptado que [connects](https://briarproject.org/how-it-works/) para outros clientes que utilizam a Rede Tor. Briar também pode se conectar via Wi-Fi ou Bluetooth quando em proximidade local. O modo de rede local do Briar pode ser útil quando a disponibilidade da Internet é um problema.
    
    [Visite briarproject.org](https://briarproject.org/){ .md-button .md-button--primary }
    
    **Downloads***
    - [:fontawesome-brands-android: Android](https://f-droid.org/packages/org.briarproject.briar.android)
    - [:fontawesome-brands-google-play: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
    - [:fontawesome-brands-git: Source](https://code.briarproject.org/briar/briar) downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
        - [:simple-windows11: Windows](https://briarproject.org/download-briar-desktop/)
        - [:simple-linux: Linux](https://briarproject.org/download-briar-desktop/)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

To add a contact on Briar, you must both add each other first. You can either exchange `briar://` links or scan a contact’s QR code if they are nearby.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit/), and the anonymous routing protocol uses the Tor network which has also been audited.

Briar has a fully [published specification](https://code.briarproject.org/briar/briar-spec).

Briar supports perfect forward secrecy by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## Tipos de Redes de Comunicação

!!! Recomendamos que você verifique o [documentação](https://developers.yubico.com/SSH/) de Yubico sobre como configurar isso.

    These messengers do not have Perfect [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) (PFS), and while they fulfill certain needs that our previous recommendations may not, we do not recommend them for long-term or sensitive communications. [Visite getession.org](https://getsession.org/){ .md-button .md-button--primary }
    
    **Downloads***
    - [:fontawesome-brands-windows: Windows](https://getsession.org/windows)
    - [:fontawesome-brands-apple: macOS](https://getsession.org/mac)
    - [:fontawesome-brands-app-store-ios: App Store](https://apps.apple.com/app/id1470168868)
    - [:fontawesome-brands-linux: Linux](https://www.getession.org/linux)
    - [:fontawesome-brands-android: Android](https://fdroid.getsession.org/)
    - [:fontawesome-brands-google-play: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
    - [:pg-f-droid: F-Droid](https://fdroid.getsession.org)
    - [:fontawesome-brands-github: Source](https://github.com/oxen-io/session-desktop)

### Element

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Element logo](assets/img/messengers/element.svg){ align=right }
    
    **Element** is the reference client for the [Matrix](https://matrix.org/docs/guides/introduction) protocol, an [open standard](https://matrix.org/docs/spec) for secure decentralized real-time communication.
    
    Messages and files shared in private rooms (those which require an invite) are by default E2EE as are one to one voice and video calls.
    
    [:octicons-home-16: Homepage](https://element.io/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/vector-im){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
        - [:simple-appstore: App Store](https://apps.apple.com/app/vector/id1083446067)
        - [:simple-github: GitHub](https://github.com/vector-im/element-android/releases)
        - [:simple-windows11: Windows](https://element.io/get-started)
        - [:simple-apple: macOS](https://element.io/get-started)
        - [:simple-linux: Linux](https://element.io/get-started)
        - [:octicons-globe-16: Web](https://app.element.io)

Profile pictures, reactions, and nicknames are not encrypted.

Group voice and video calls are [not](https://github.com/vector-im/element-web/issues/12878) E2EE, and use Jitsi, but this is expected to change with [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401). Group calls have [no authentication](https://github.com/vector-im/element-web/issues/13074) currently, meaning that non-room participants can also join the calls. We recommend that you do not use this feature for private meetings.

The Matrix protocol itself [theoretically supports PFS](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy), however this is [not currently supported in Element](https://github.com/vector-im/element-web/issues/7101) due to it breaking some aspects of the user experience such as key backups and shared message history.

The protocol was independently [audited](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) in 2016. The specification for the Matrix protocol can be found in their [documentation](https://spec.matrix.org/latest/). The [Olm](https://matrix.org/docs/projects/other/olm) cryptographic ratchet used by Matrix is an implementation of Signal’s [Double Ratchet algorithm](https://signal.org/docs/specifications/doubleratchet/).

### Session

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Session logo](assets/img/messengers/session.svg){ align=right }
    
    **Session** is a decentralized messenger with a focus on private, secure, and anonymous communications. Session offers support for direct messages, group chats, and voice calls.
    
    Session uses the decentralized [Oxen Service Node Network](https://oxen.io/) to store and route messages. Every encrypted message is routed through three nodes in the Oxen Service Node Network, making it virtually impossible for the nodes to compile meaningful information on those using the network.
    
    [:octicons-home-16: Homepage](https://getsession.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
        - [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
        - [:simple-windows11: Windows](https://getsession.org/download)
        - [:simple-apple: macOS](https://getsession.org/download)
        - [:simple-linux: Linux](https://getsession.org/download)

Session allows for E2EE in one-on-one chats or closed groups which allow for up to 100 members. Open groups have no restriction on the number of members, but are open by design.

Session does [not](https://getsession.org/blog/session-protocol-technical-information) support PFS, which is when an encryption system automatically and frequently changes the keys it uses to encrypt and decrypt information, such that if the latest key is compromised it exposes a smaller portion of sensitive information.

Oxen requested an independent audit for Session in March of 2020. The audit [concluded](https://getsession.org/session-code-audit) in April of 2021, “The overall security level of this application is good and makes it usable for privacy-concerned people.”

Session has a [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) describing the technicals of the app and protocol.

## Framadate

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! Considere o auto-hospedagem para mitigar esta ameaça.

    ![logo PrivateBin](/assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** é um pastebin online minimalista e de código aberto onde o servidor tem zero conhecimento de dados colados. Os dados são criptografados/descriptografados no navegador usando AES de 256 bits. Psono suporta compartilhamento seguro de senhas, arquivos, marcadores e e-mails.

- Must have open-source clients.
- Must use E2EE for private messages by default.
- Must support E2EE for all messages.
- Must have been independently audited.

### Best-Case

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Should have Perfect Forward Secrecy.
- Should have open-source servers.
- Should be decentralized, i.e. federated or P2P.
- Should use E2EE for all messages by default.
- Should support Linux, macOS, Windows, Android, and iOS.
