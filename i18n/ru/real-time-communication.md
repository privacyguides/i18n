---
meta_title: "Лучшие приватные мессенджеры - Privacy Guides"
title: Мессенджеры
icon: material/chat-processing
description: Encrypted messengers like Signal and SimpleX keep your sensitive communications secure from prying eyes.
cover: real-time-communication.webp
---

<small>Защищает от следующих угроз:</small>

- [:material-bug-outline: Пассивные атаки](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Поставщики услуг](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: Массовое наблюдение](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Эти рекомендации по шифрованию **связи в режиме реального времени** отлично подходят для защиты конфиденциальных сообщений. Эти мессенджеры представлены в виде множества [типов коммуникационных сетей](advanced/communication-network-types.md).

[:material-movie-open-play-outline: Видео: Пора прекратить использовать СМС](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## Signal

<div class="admonition recommendation" markdown>

![Signal logo](assets/img/messengers/signal.svg){ align=right }

**Signal** — мобильное приложение, разработанное Signal Messenger LLC. Приложение обеспечивает обмен мгновенными сообщениями и звонками, защищенными протоколом Signal — чрезвычайно надежным протоколом шифрования, который поддерживает прямую секретность[^1] и защиту после компрометации.[^2]

[:octicons-home-16: Главная](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Политика конфиденциальности"}
[:octicons-info-16:](https://support.signal.org){ .card-link title="Документация" }
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title="Поддержать" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-github: GitHub](https://github.com/signalapp/Signal-Android/releases)
- [:simple-android: Android](https://signal.org/android/apk)
- [:fontawesome-brands-windows: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Для регистрации Signal требует номер телефона, однако Вам следует создать имя пользователя, чтобы скрыть свой номер телефона от контактов:

1. Откройте настройки приложения и нажмите на Ваш профиль вверху.
2. Нажмите **Имя пользователя** и выберите **Продолжить** на экране "Настройка имени пользователя Signal".
3. Введите имя пользователя. Ваше имя пользователя всегда будет сопровождаться уникальным набором цифр, чтобы сохранить уникальность Вашего имени и предотвратить возможность угадать его. Например, если Вы введете "John", Ваше имя пользователя в итоге может стать `@john.35`. По умолчанию при создании имени пользователя к нему добавляются только 2 цифры, но Вы можете добавить больше, пока не достигнете максимальной длины имени пользователя (32 символа).
4. Вернитесь на главную страницу настроек и нажмите **Конфиденциальность**.
5. Нажмите **Номер телефона**.
6. Измените **Кто может видеть мой номер** на **Никто**.
7. (Необязательно) Измените **Кто может найти меня по номеру** на **Никто**, если Вы хотите, чтобы люди, у которых уже есть Ваш номер телефона, не смогли обнаружить Вашу учетную запись/имя пользователя Signal.

У нас есть несколько дополнительных советов по настройке и улучшению безопасности Signal:

[Настройка и улучшение безопасности Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

В Signal списки контактов шифруются с помощью Вашего Signal PIN-кода, и сервер не имеет к ним доступа. Личные профили также шифруются и передаются только тем контактам, с которыми Вы переписываетесь.

Signal supports [private groups](https://signal.org/blog/signal-private-group-system), where the server has no record of your group memberships, group titles, group avatars, or group attributes. Signal has minimal metadata when [Sealed Sender](https://signal.org/blog/sealed-sender) is enabled. The sender address is encrypted along with the message body, and only the recipient address is visible to the server. Sealed Sender is only enabled for people in your contacts list, but can be enabled for all recipients with the increased risk of receiving spam.

The protocol was independently [audited](https://eprint.iacr.org/2016/1013.pdf) in 2016. The specification for the Signal protocol can be found in their [documentation](https://signal.org/docs).

### Molly (Android)

If you use Android and your threat model requires protecting against [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} you may consider using this alternative app, which features a number of security and usability improvements, to access the Signal network.

<div class="admonition recommendation" markdown>

![Molly logo](assets/img/messengers/molly.svg){ align=right }

**Molly** is an alternative Signal client for Android which allows you to encrypt the local database with a passphrase at rest, to have unused RAM data securely shredded, to route your connection via Tor, and [more](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features). It also has usability improvements including scheduled backups, automatic locking, and the ability to use your Android phone as a linked device instead of the primary device for a Signal account.

[:octicons-home-16: Homepage](https://molly.im){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/mollyim/mollyim-android/wiki){ .card-link title="Documentation" }
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

**Molly-FOSS** is a version of Molly which removes proprietary code like the Google services used by both Signal and Molly at the expense of some features (like battery-saving push notifications via Google Play Services). You can set up push notifications without Google Play Services in either version of Molly with [UnifiedPush](https://unifiedpush.org). Using this notification delivery method requires access to a [MollySocket](https://github.com/mollyim/mollysocket) server, but you can choose a public MollySocket instance for this.[^3]

Both versions of Molly provide the same security improvements and support [reproducible builds](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds), meaning it's possible to confirm that the compiled APKs match the source code.

## SimpleX Chat

<div class="admonition recommendation" markdown>

![SimpleX Chat logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX Chat** is an instant messenger that doesn't depend on any unique identifiers such as phone numbers or usernames. Its decentralized network makes SimpleX Chat an effective tool against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16: Главная](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplex.chat/privacy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://simplex.chat/docs/simplex.html){ .card-link title="Документация" }
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Исходный код" }

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

SimpleX Chat provides direct messaging, group chats, and E2EE calls secured with the [SimpleX Messaging Protocol](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md), which uses double ratchet encryption with quantum resistance. Additionally, SimpleX Chat provides metadata protection by using unidirectional ["simplex queues"](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md#simplex-queue) to deliver messages.

To participate in conversations on SimpleX Chat, you must scan a QR code or click an invite link. This allows you to verify a contact out-of-band, which protects against man-in-the-middle attacks by network providers. Your data can be exported and imported onto another device, as there are no central servers where this is backed up.

You can find a full list of the privacy and security [features](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations) implemented in SimpleX Chat in the app's repository.

SimpleX Chat was independently audited in [July 2024](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits) and in [October 2022](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website).

## Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works) to other clients using the [Tor network](alternative-networks.md#tor), making it an effective tool at circumventing [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar также может передавать сообщения через Wi-Fi или Bluetooth, если получатель находится в непосредственной близости. Режим локальной сети Briar может быть полезен, когда Вы не имеете доступа к Интернету.

[:octicons-home-16: Главная](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title="Документация" }
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://code.briarproject.org/briar/briar#donate){ .card-link title="Поддержать" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Чтобы добавить контакт в Briar, вы должны сначала добавить друг друга. Вы можете либо обменяться ссылками `briar://`, либо отсканировать QR-код контакта, если он находится поблизости.

Briar has a fully [published specification](https://code.briarproject.org/briar/briar-spec). Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

Клиентское ПО прошло независимый [аудит](https://briarproject.org/news/2017-beta-released-security-audit); протокол анонимной маршрутизации использует сеть Tor, который также был проверен в прошлом.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

### Минимальные требования к сервисам

- Должны иметь приложения с открытым исходным кодом.
- Не должны требовать передачи контактам личных идентификаторов (особенно номера телефона или адреса электронной почты).
- Должны по умолчанию использовать E2EE для личных сообщений.
- Должны поддерживать E2EE для всех сообщений.
- Должны поддерживать прямую секретность[^1].
- Должны иметь опубликованный аудит от авторитетной, независимой сторонней организации.

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Должны поддерживать будущую секретность (защиту после компрометации) [^2].
- Должны иметь серверы с открытым исходным кодом.
- Должны использовать децентрализованную сеть, т.е. [федеративную или P2P](advanced/communication-network-types.md).
- Должны по умолчанию использовать E2EE для всех сообщений.
- Должны поддерживать Linux, macOS, Windows, Android и iOS.
[^3]: You may refer to this step-by-step tutorial in German on how to set up UnifiedPush as the notification provider for Molly: [https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy](https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy).

[^1]: [Forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future secrecy (or [post-compromise security](https://eprint.iacr.org/2016/221.pdf)) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties since they lose access as soon as a key exchange occurs that is not intercepted.
