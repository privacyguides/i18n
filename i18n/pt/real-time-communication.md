---
meta_title: "The Best Private Instant Messengers - Privacy Guides"
title: "Comunicação em tempo real"
icon: material/chat-processing
description: Encrypted messengers like Signal and SimpleX keep your sensitive communications secure from prying eyes.
cover: real-time-communication.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Ataques passivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fornecedores de serviços](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: Vigilância em massa](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: Capitalismo de vigilância](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our recommendations for encrypted **real-time communication**.

[Tipos de redes de comunicação :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## Aplicações de mensagens encriptadas

Estas aplicações de mensagens são ótimas para proteger as suas comunicações sensíveis.

### Signal

<div class="admonition recommendation" markdown>

![Logótipo Signal](assets/img/messengers/signal.svg){ align=right }

**Signal** é uma aplicação para dispositivos móveis desenvolvida pela Signal Messenger LLC. The app provides instant messaging and calls secured with the Signal Protocol, an extremely secure encryption protocol which supports forward secrecy[^1] and post-compromise security.[^2]

[:octicons-home-16: Homepage](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk)
- [:fontawesome-brands-windows: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal requires your phone number for registration, however you should create a username to hide your phone number from your contacts:

1. In Signal, open the app's settings and tap your account profile at the top.
2. Tap **Username** and choose **Continue** on the "Set up your Signal username" screen.
3. Enter a username. Your username will always be paired with a unique set of digits to keep your username unique and prevent people from guessing it, for example if you enter "John" your username might end up being `@john.35`. By default, only 2 digits are paired with your username when you create it, but you can add more digits until you reach the username length limit (32 characters).
4. Go back to the main app settings page and select **Privacy**.
5. Select **Phone Number**
6. Change the **Who Can See My Number** setting to: **Nobody**

You can optionally change the **Who Can Find Me By Number** setting to **Nobody** as well, if you want to prevent people who already have your phone number from discovering your Signal account/username.

Contact lists on Signal are encrypted using your Signal PIN and the server does not have access to them. Os perfis pessoais também são encriptados e apenas são partilhados com os contactos com quem conversa. Signal supports [private groups](https://signal.org/blog/signal-private-group-system), where the server has no record of your group memberships, group titles, group avatars, or group attributes. Signal has minimal metadata when [Sealed Sender](https://signal.org/blog/sealed-sender) is enabled. O endereço do remetente é encriptado juntamente com o corpo da mensagem e apenas o endereço do destinatário é visível para o servidor. O Sealed Sender só está ativado para as pessoas da sua lista de contactos, mas pode ser ativado para todos os destinatários, com o risco acrescido de poder receber spam.

O protocolo foi objeto de uma [auditoria](https://eprint.iacr.org/2016/1013.pdf) independente em 2016. The specification for the Signal protocol can be found in their [documentation](https://signal.org/docs).

Temos algumas dicas adicionais sobre como configurar e fortalecer a sua instalação do Signal:

[Configuração e robustecimento do Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

#### Molly (Android)

If you use Android and your threat model requires protecting against [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} you may consider using this alternative app, which features a number of security and usability improvements, to access the Signal network.

<div class="admonition recommendation" markdown>

![Molly logo](assets/img/messengers/molly.svg){ align=right }

**Molly** is an alternative Signal client for Android which allows you to encrypt the local database with a passphrase at rest, to have unused RAM data securely shredded, to route your connection via Tor, and [more](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features). It also has usability improvements including scheduled backups, automatic locking, and the ability to use your Android phone as a linked device instead of the primary device for a Signal account.

[:octicons-home-16: Homepage](https://molly.im){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/mollyim/mollyim-android/wiki){ .card-link title="Documentation"}
[:octicons-code-16:](https://github.com/mollyim/mollyim-android){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/mollyim){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-fdroid: F-Droid](https://molly.im/fdroid)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/im.molly.app)
- [:simple-github: GitHub](https://github.com/mollyim/mollyim-android/releases)

</details>

</div>

Molly is updated every two weeks to include the latest features and bug fixes from Signal. The exception is security issues, which are patched as soon as possible. That said, you should be aware that there might be a slight delay compared to upstream, which may affect actions such as [migrating from Signal to Molly](https://github.com/mollyim/mollyim-android/wiki/Migrating-From-Signal#migrating-from-signal).

Note that you are trusting multiple parties by using Molly, as you now need to trust the Signal team *and* the Molly team to deliver safe and timely updates.

There is a version of Molly called **Molly-FOSS** which removes proprietary code like the Google services used by both Signal and Molly, at the expense of some features like battery-saving push notifications via Google Play Services.

There is also a version called [**Molly-UP**](https://github.com/mollyim/mollyim-android#unifiedpush) which is based on Molly-FOSS and adds support for push notifications with [UnifiedPush](https://unifiedpush.org/), an open source alternative to the push notifications provided by Google Play Services, but it requires running a separate program called [Mollysocket](https://github.com/mollyim/mollysocket) to function. Mollysocket can either be self-hosted on a separate computer or server (VPS), or alternatively a public Mollysocket instance can be used ([step-by-step tutorial, in German](https://www.kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy/)).

All three versions of Molly provide the same security improvements.

Molly and Molly-FOSS support [reproducible builds](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds), meaning it's possible to confirm that the compiled APKs match the source code.

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat is an instant messenger that doesn't depend on any unique identifiers such as phone numbers or usernames. Its decentralized network makes SimpleX Chat an effective tool against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Os utilizadores do SimpleX Chat podem fazer scan a um código QR ou clicar numa ligação de convite para participar em conversas de grupo.

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:fontawesome-brands-windows: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

O SimpleX Chat [foi auditado](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) por Trail of Bits, em outubro de 2022.

SimpleX Chat supports basic group chatting functionality, direct messaging, and editing of messages and markdown. Chamadas de áudio e vídeo E2EE também são suportadas. Your data can be exported and imported onto another device, as there are no central servers where this is backed up.

### Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works) to other clients using the Tor Network, making it an effective tool at circumventing [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. O Briar pode ligar-se através de Wi-Fi ou Bluetooth. O modo de rede local do Briar pode ser útil, quando não estiver garantida a disponibilidade da Internet.

[:octicons-home-16: Homepage](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://briarproject.org){ .card-link title="Donation options are listed on the bottom of the homepage" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Para adicionar um contacto no Briar, é necessário que você e o contacto se adicionem mutuamente. Pode trocar links `briar://` ou digitalizar o código QR de um contacto, se este estiver próximo.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit), and the anonymous routing protocol uses the Tor network which has also been audited.

O Briar publicou na íntegra a sua [especificação](https://code.briarproject.org/briar/briar-spec).

Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## Opções adicionais

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

These messengers do not have forward secrecy[^1], and while they fulfill certain needs that our previous recommendations may not, we do not recommend them for long-term or sensitive communications. Qualquer comprometimento da chave entre os destinatários da mensagem afetará a confidencialidade de **todas** as comunicações anteriores.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** is the flagship client for the [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im) protocol, an [open standard](https://spec.matrix.org/latest) for secure decentralized real-time communication.

Messages and files shared in private rooms (those which require an invite) are by default E2EE, as are one-to-one voice and video calls.

[:octicons-home-16: Homepage](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1083446067)
- [:simple-github: GitHub](https://github.com/element-hq/element-android/releases)
- [:fontawesome-brands-windows: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

As imagens de perfil, as reações e os nicknames não são encriptados.

Group voice and video calls are [not](https://github.com/vector-im/element-web/issues/12878) E2EE and use Jitsi, but this is expected to change with [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401). Atualmente, as chamadas de grupo [não têm autenticação](https://github.com/vector-im/element-web/issues/13074), o que significa que os participantes que não estão na sala também podem juntar-se às chamadas. Recomendamos que não utilize esta funcionalidade para reuniões privadas.

The Matrix protocol itself [theoretically supports forward secrecy](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], however this is [not currently supported in Element](https://github.com/vector-im/element-web/issues/7101) due to it breaking some aspects of the user experience such as key backups and shared message history.

O protocolo foi objeto de uma [auditoria independente](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) em 2016. The specification for the Matrix protocol can be found in their [documentation](https://spec.matrix.org/latest). The [Olm cryptographic ratchet](https://matrix.org/docs/matrix-concepts/end-to-end-encryption) used by Matrix is an implementation of Signal’s [Double Ratchet algorithm](https://signal.org/docs/specifications/doubleratchet).

### Session

<div class="admonition recommendation" markdown>

![Logótipo Session](assets/img/messengers/session.svg){ align=right }

**Session** é uma aplicação descentralizada de mensagens instantâneas com foco em comunicações privadas, seguras e anónimas. A sessão oferece suporte para mensagens diretas, conversas de grupo e chamadas de voz.

Session uses the decentralized [Oxen Service Node Network](https://oxen.io) to store and route messages. Cada mensagem encriptada é encaminhada através de três nós na Oxen Service Node Network, tornando virtualmente impossível que os nós compilem informação significativa sobre aqueles que utilizam a rede.

[:octicons-home-16: Homepage](https://getsession.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:fontawesome-brands-windows: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

O Session permite E2EE em conversas individuais ou em grupos fechados com um máximo de 100 membros. Os grupos abertos não têm restrições quanto ao número de membros, mas são abertos por definição.

Session was previously based on Signal Protocol before replacing it with their own in December 2020. Session Protocol does [not](https://getsession.org/blog/session-protocol-technical-information) support forward secrecy.[^1]

Oxen requested an independent audit for Session in March 2020. The audit [concluded](https://getsession.org/session-code-audit) in April 2021:

> The overall security level of this application is good and makes it usable for privacy-concerned people.

Session has a [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) describing the technical details of the app and protocol.

## Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

### Requisitos mínimos

- Has open-source clients.
- Does not require sharing personal identifiers (phone numbers or emails in particular) with contacts.
- Uses E2EE for private messages by default.
- Supports E2EE for all messages.
- Has been independently audited.

### Melhor caso

Os nossos melhores critérios representam o que gostaríamos de ver num projeto perfeito desta categoria. As nossas recomendações podem não incluir todas as funcionalidades, mas incluem as que, na nossa opinião, têm um impacto mais elevado.

- Supports forward secrecy[^1]
- Supports Future Secrecy (Post-Compromise Security)[^2]
- Has open-source servers.
- Decentralized, i.e. [federated or P2P](advanced/communication-network-types.md).
- Uses E2EE for all messages by default.
- Supports Linux, macOS, Windows, Android, and iOS.

[^1]: [Forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future Secrecy (or Post-Compromise Security) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties, since they lose access as soon as a key exchange occurs that is not intercepted.
