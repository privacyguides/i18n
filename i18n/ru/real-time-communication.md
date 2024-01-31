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

**Signal** - мобильное приложение, разработанное Signal Messenger LLC. Приложение обеспечивает мгновенный обмен сообщениями, а также голосовые и видеозвонки.

Все коммуникации осуществляются в режиме E2EE. Списки контактов шифруются с помощью вашего PIN-кода входа в систему, и сервер не имеет к ним доступа. Личные профили также шифруются и предоставляются только тем контактам, с которыми вы переписываетесь.

[:octicons-home-16: Homepage](https://signal.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org/hc/en-us){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk/)
- [:simple-windows11: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Сигнал поддерживает [приватные группы](https://signal.org/blog/signal-private-group-system/). На сервере нет записей о вашем членстве в группах, названиях групп, аватарах групп или атрибутах групп. Сигнал имеет минимальные метаданные, если включена функция [запечатанного отправителя](https://signal.org/blog/sealed-sender/). Адрес отправителя шифруется вместе с текстом сообщения, серверу виден только адрес получателя. Функция запечатанного отправителя включена только для людей из вашего списка контактов, но может быть включена для всех получателей с повышенным риском получения спама. Signal требует ваш номер телефона в качестве персонального идентификатора.

Протокол прошел независимый [аудит](https://eprint.iacr.org/2016/1013.pdf) в 2016 году. Спецификацию протокола Signal можно найти в их [документации](https://signal.org/docs/).

У нас есть несколько дополнительных советов по настройке и улучшению безопасности вашей установки Signal:

[Настройка и усиление безопасности Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening/)

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
- [:simple-appstore: App Store](https://apps.apple.com/us/app/simplex-chat/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:simple-windows11: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX Chat [прошел аудит](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) от компании Trail of Bits в октябре 2022 года.

SimpleX Chat supports basic group chatting functionality, direct messaging, and editing of messages and markdown. Также поддерживаются аудио- и видеозвонки, зашифрованные E2EE. Ваши данные можно экспортировать и импортировать на другое устройство, так как центральных серверов, где хранятся резервные копии, нет.

### Briar

<div class="admonition recommendation" markdown>

![Логотип Briar](assets/img/messengers/briar.svg){ align=right }

**Briar** - это зашифрованный мессенджер, который [соединяется с ](https://briarproject.org/how-it-works/) другими клиентам с помощью сети Tor. Briar также может передавать сообщения через Wi-Fi или Bluetooth, если получатель находится в непосредственной близости. Режим локальной сети Briar может быть полезен, когда Вы не имеете доступа к Интернету.

[:octicons-home-16: Homepage](https://briarproject.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://briarproject.org/){ .card-link title="Donation options are listed on the bottom of the homepage" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:simple-windows11: Windows](https://briarproject.org/download-briar-desktop/)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop/)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Чтобы добавить контакт в Briar, вы оба должны сначала добавить друг друга. Вы можете либо обмениваться ссылками `briar://`, либо сканировать QR-код контакта, если он находится поблизости.

Клиентское программное обеспечение прошло независимый [аудит](https://briarproject.org/news/2017-beta-released-security-audit/); протокол анонимной маршрутизации использует сеть Tor, который также был проверен в прошлом.

Briar имеет полностью [опубликованную документацию](https://code.briarproject.org/briar/briar-spec).

Briar поддерживает прямую секретность пересылки, используя протоколы Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) и [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md).

## Дополнительные варианты

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Хотя эти мессенджеры и проходят по определённым критериям, они не поддерживают [прямую секретность](https://ru.wikipedia.org/wiki/Perfect_forward_secrecy), поэтому мы не рекомендуем их для длительных или конфиденциальных коммуникаций. Любая компрометация ключа среди получателей сообщений повлияет на конфиденциальность **всех** прошлых сообщений.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** is the reference [client](https://matrix.org/ecosystem/clients/) for the [Matrix](https://matrix.org/docs/guides/introduction) protocol, an [open standard](https://matrix.org/docs/spec) for secure decentralized real-time communication.

Сообщения, файлы, голосовые и видео звонки между двумя людьми, которые обмениваются ими в приватных комнатах (для которых требуется приглашение), по умолчанию являются E2EE.

[:octicons-home-16: Homepage](https://element.io/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/vector-im){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/vector/id1083446067)
- [:simple-github: GitHub](https://github.com/vector-im/element-android/releases)
- [:simple-windows11: Windows](https://element.io/get-started)
- [:simple-apple: macOS](https://element.io/get-started)
- [:simple-linux: Linux](https://element.io/get-started)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

Фотографии профиля, реакции и никнеймы не зашифрованы.

Групповые голосовые и видео звонки [не](https://github.com/vector-im/element-web/issues/12878) зашифрованы E2EE, а используют Jitsi. Ожидается, что это изменится с [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401). Групповые звонки в настоящее время [не имеют аутентификации](https://github.com/vector-im/element-web/issues/13074), что означает, что к звонкам могут присоединяться и не входящие в комнату участники. Мы рекомендуем вам не использовать эту функцию для приватных созвонов.

Сам протокол Matrix [теоретически поддерживает PFS](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy), однако он [в настоящее время не поддерживается в Element](https://github.com/vector-im/element-web/issues/7101) из-за того, что это нарушает некоторые аспекты работы пользователей, такие как резервное копирование ключей и общая история сообщений.

Протокол прошел независимый [аудит](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) в 2016 году. Спецификацию протокола Matrix можно найти в их [документации](https://spec.matrix.org/latest/). The [Olm cryptographic ratchet](https://matrix.org/docs/matrix-concepts/end-to-end-encryption/) used by Matrix is an implementation of Signal’s [Double Ratchet algorithm](https://signal.org/docs/specifications/doubleratchet/).

### Session

<div class="admonition recommendation" markdown>

![Логотип Session](assets/img/messengers/session.svg){ align=right }

**Session** - это децентрализованный мессенджер, ориентированный на приватные, безопасные и анонимные коммуникации. Session предлагает поддержку обычных чатов, групповых чатов и голосовых вызовов.

Session использует децентрализованную [Oxen Service Node Network](https://oxen.io/) для хранения и маршрутизации сообщений. Каждое зашифрованное сообщение проходит через три узла в сети Oxen Service Node Network, что делает практически невозможным для узлов собрать значимую информацию о тех, кто пользуется сетью.

[:octicons-home-16: Homepage](https://getsession.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:simple-windows11: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

Сессия использует E2EE в чатах один на один или в закрытых группах, в которых могут участвовать до 100 человек. Открытые группы не имеют ограничений по количеству участников, но являются открытыми по своей сути.

Session [не](https://getsession.org/blog/session-protocol-technical-information) поддерживает прямую секретность. При прямой секретности система шифрования автоматически и часто меняет ключи шифрования, так что в случае взлома последнего ключа обнажается меньшая часть конфиденциальной информации.

Оксен запросил независимый аудит для Session в марте 2020 года. Аудит [заключил](https://getsession.org/session-code-audit) в апреле 2021 года: "Общий уровень безопасности этого приложения хороший и делает его пригодным для использования людьми, заботящимися о конфиденциальности."

У Session есть [whitepaper](https://arxiv.org/pdf/2002.04609.pdf), описывающий технические особенности приложения и протокола.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Мы всё еще работаем над установлением критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у вас есть вопросы по поводу наших критериев, пожалуйста, [задавайте их на нашем форуме](https://discuss.privacyguides.net/latest). Если какой-то критерий здесь не указан, это не значит, что мы его не учли. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

</div>

- Должны иметь приложения с открытым исходным кодом.
- Должны по умолчанию использовать E2EE для личных сообщений.
- Должны поддерживать E2EE для всех сообщений.
- Должен быть проведен независимый аудит.

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Должны поддерживать прямую секретность.
- Должны иметь серверы с открытым исходным кодом.
- Должны быть децентрализованными, т.е. федеративными или P2P.
- Должны по умолчанию использовать E2EE для всех сообщений.
- Должны поддерживать Linux, macOS, Windows, Android и iOS.
