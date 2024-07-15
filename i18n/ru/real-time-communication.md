---
meta_title: "The Best Private Instant Messengers - Privacy Guides"
title: "Мессенджеры"
icon: material/chat-processing
description: Other instant messengers make all of your private conversations available to the company that runs them.
cover: real-time-communication.webp
---

Это наши рекомендации по зашифрованному общению в режиме реального времени.

[Типы коммуникационных сетей :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## Зашифрованные мессенджеры

Эти мессенджеры отлично подходят для защиты конфиденциальных сообщений.

### Signal

<div class="admonition recommendation" markdown>

![Signal logo](assets/img/messengers/signal.svg){ align=right }

**Signal** - мобильное приложение, разработанное Signal Messenger LLC. The app provides instant messaging and calls secured with the Signal Protocol, an extremely secure encryption protocol which supports forward secrecy[^1] and post-compromise security.[^2]

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
3. Enter a username. Your username will always be paired with a unique set of digits to keep your username unique and prevent people from guessing it, for example if you enter "John" your username might end up being `@john.35`.
4. Go back to the main app settings page and select **Privacy**.
5. Select **Phone Number**
6. Change the **Who Can See My Number** setting to: **Nobody**

You can optionally change the **Who Can Find Me By Number** setting to **Nobody** as well, if you want to prevent people who already have your phone number from discovering your Signal account/username.

Contact lists on Signal are encrypted using your Signal PIN and the server does not have access to them. Личные профили также шифруются и предоставляются только тем контактам, с которыми вы переписываетесь. Signal supports [private groups](https://signal.org/blog/signal-private-group-system), where the server has no record of your group memberships, group titles, group avatars, or group attributes. Signal has minimal metadata when [Sealed Sender](https://signal.org/blog/sealed-sender) is enabled. Адрес отправителя шифруется вместе с текстом сообщения, серверу виден только адрес получателя. Функция запечатанного отправителя включена только для людей из вашего списка контактов, но может быть включена для всех получателей с повышенным риском получения спама.

Протокол прошел независимый [аудит](https://eprint.iacr.org/2016/1013.pdf) в 2016 году. The specification for the Signal protocol can be found in their [documentation](https://signal.org/docs).

У нас есть несколько дополнительных советов по настройке и улучшению безопасности вашей установки Signal:

[Настройка и усиление безопасности Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Логотип Simplex](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat - это децентрализованный мессенджер, который не зависит от каких-либо уникальных идентификаторов, таких как номера телефонов или имена пользователей. Пользователи SimpleX Chat могут сканировать QR-код или открыть ссылку-приглашение для участия в групповых беседах.

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

SimpleX Chat [прошел аудит](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) от компании Trail of Bits в октябре 2022 года.

SimpleX Chat supports basic group chatting functionality, direct messaging, and editing of messages and markdown. Также поддерживаются аудио- и видеозвонки, зашифрованные E2EE. Ваши данные можно экспортировать и импортировать на другое устройство, так как центральных серверов, где хранятся резервные копии, нет.

### Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works) to other clients using the Tor Network. Briar также может передавать сообщения через Wi-Fi или Bluetooth, если получатель находится в непосредственной близости. Режим локальной сети Briar может быть полезен, когда Вы не имеете доступа к Интернету.

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

Чтобы добавить контакт в Briar, вы оба должны сначала добавить друг друга. Вы можете либо обмениваться ссылками `briar://`, либо сканировать QR-код контакта, если он находится поблизости.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit), and the anonymous routing protocol uses the Tor network which has also been audited.

Briar имеет полностью [опубликованную документацию](https://code.briarproject.org/briar/briar-spec).

Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## Дополнительные варианты

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

These messengers do not have forward secrecy[^1], and while they fulfill certain needs that our previous recommendations may not, we do not recommend them for long-term or sensitive communications. Любая компрометация ключа среди получателей сообщений повлияет на конфиденциальность **всех** прошлых сообщений.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** is the reference [client](https://matrix.org/ecosystem/clients) for the [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im) protocol, an [open standard](https://spec.matrix.org/latest) for secure decentralized real-time communication.

Сообщения, файлы, голосовые и видео звонки между двумя людьми, которые обмениваются ими в приватных комнатах (для которых требуется приглашение), по умолчанию являются E2EE.

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

Фотографии профиля, реакции и никнеймы не зашифрованы.

Групповые голосовые и видео звонки [не](https://github.com/vector-im/element-web/issues/12878) зашифрованы E2EE, а используют Jitsi. Ожидается, что это изменится с [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401). Групповые звонки в настоящее время [не имеют аутентификации](https://github.com/vector-im/element-web/issues/13074), что означает, что к звонкам могут присоединяться и не входящие в комнату участники. Мы рекомендуем вам не использовать эту функцию для приватных созвонов.

The Matrix protocol itself [theoretically supports forward secrecy](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], however this is [not currently supported in Element](https://github.com/vector-im/element-web/issues/7101) due to it breaking some aspects of the user experience such as key backups and shared message history.

Протокол прошел независимый [аудит](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) в 2016 году. The specification for the Matrix protocol can be found in their [documentation](https://spec.matrix.org/latest). The [Olm cryptographic ratchet](https://matrix.org/docs/matrix-concepts/end-to-end-encryption) used by Matrix is an implementation of Signal’s [Double Ratchet algorithm](https://signal.org/docs/specifications/doubleratchet).

### Session

<div class="admonition recommendation" markdown>

![Логотип Session](assets/img/messengers/session.svg){ align=right }

**Session** - это децентрализованный мессенджер, ориентированный на приватные, безопасные и анонимные коммуникации. Session предлагает поддержку обычных чатов, групповых чатов и голосовых вызовов.

Session uses the decentralized [Oxen Service Node Network](https://oxen.io) to store and route messages. Каждое зашифрованное сообщение проходит через три узла в сети Oxen Service Node Network, что делает практически невозможным для узлов собрать значимую информацию о тех, кто пользуется сетью.

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

Сессия использует E2EE в чатах один на один или в закрытых группах, в которых могут участвовать до 100 человек. Открытые группы не имеют ограничений по количеству участников, но являются открытыми по своей сути.

Session was previously based on Signal Protocol before replacing it with their own in December 2020. Session Protocol does [not](https://getsession.org/blog/session-protocol-technical-information) support forward secrecy.[^1]

Oxen requested an independent audit for Session in March 2020. The audit [concluded](https://getsession.org/session-code-audit) in April 2021, “The overall security level of this application is good and makes it usable for privacy-concerned people.”

Session has a [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) describing the technical details of the app and protocol.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

### Минимальные требования к сервисам

- Has open-source clients.
- Does not require sharing personal identifiers (phone numbers or emails in particular) with contacts.
- Uses E2EE for private messages by default.
- Supports E2EE for all messages.
- Has been independently audited.

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Supports Forward Secrecy[^1]
- Supports Future Secrecy (Post-Compromise Security)[^2]
- Has open-source servers.
- Decentralized, i.e. [federated or P2P](advanced/communication-network-types.md).
- Uses E2EE for all messages by default.
- Supports Linux, macOS, Windows, Android, and iOS.

[^1]: [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future Secrecy (or Post-Compromise Security) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties, since they lose access as soon as a key exchange occurs that is not intercepted.
