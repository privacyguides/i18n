---
title: "Почтовые клиенты"
icon: material/email-open
description: Эти почтовые клиенты соблюдают конфиденциальность и поддерживают шифрование электронной почты OpenPGP.
cover: email-clients.png
---

Наш список рекомендаций содержит только почтовые клиенты, которые поддерживают [OpenPGP](/encryption/#openpgp) и безопасную аутентификацию (например, [OAuth](https://ru.wikipedia.org/wiki/OAuth)). OAuth позволяет использовать [многофакторную аутентификацию](/multi-factor-authentication) и предотвратить кражу учетных записей.

??? warning "Email does not provide forward secrecy"

    When using end-to-end encryption (E2EE) technology like OpenPGP, email will still have [some metadata](email.md#email-metadata-overview) that is not encrypted in the header of the email.
    
    OpenPGP also does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed: [How do I protect my private keys?](basics/email-security.md) Consider using a medium that provides forward secrecy:
    
    [Real-time Communication](real-time-communication.md){ .md-button }

## Кросс-платформенные приложения

### Thunderbird

!!! recommendation

    ![Логотип Thunderbird](assets/img/email-clients/thunderbird.svg){ align=right }
    
    **Thunderbird** - бесплатный кроссплатформенный клиент электронной почты, новостных лент и чатов (XMPP, IRC, Twitter) с открытым исходным кодом, разработанный сообществом Thunderbird, а ранее - Mozilla Foundation.
    
    [:octicons-home-16: Домашняя страница](https://www.thunderbird.net){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/thunderbird){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title=Документация}
    [:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-windows11: Windows](https://www.thunderbird.net)
        - [:simple-apple: macOS](https://www.thunderbird.net)
        - [:simple-linux: Linux](https://www.thunderbird.net)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

#### Рекомендованные настройки

Мы рекомендуем изменить некоторые из этих настроек, чтобы сделать Thunderbird более приватным.

Эти параметры можно найти в разделе :material-menu: → **Настройки** → **Приватность и защита**.

##### Содержимое веб-сайтов

- [ ] Убрать галочку  **Помнить посещённые мной веб-сайты и ссылки**
- [ ] Убрать галочку  **Принимать куки с сайтов**

##### Сбор и использование данных Thunderbird

- [ ] Убрать галочку  **Разрешить Thunderbird отправлять технические данные и данные взаимодействия в Mozilla**

#### Thunderbird-user.js (продвинутый)

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js), представляет собой набор конфигурации, цель которых - отключить как можно больше функций веб-браузинга в Thunderbird, чтобы уменьшить поверхность атаки и сохранить конфиденциальность. Некоторые изменения перенесены из [проекта Arkenfox](https://github.com/arkenfox/user.js).

## Конкретные платформы

### Почта Apple (macOS)

!!! recommendation

    ![Логотип Apple Mail](assets/img/email-clients/applemail.png){ align=right }
    
    **Почта Apple** входит в состав macOS и может быть расширен поддержкой OpenPGP с помощью [GPG Suite](encryption.md#gpg-suite), что добавляет возможность отправлять зашифрованную PGP электронную почту.
    
    [:octicons-home-16: Домашняя страница](https://support.apple.com/ru-ru/guide/mail/welcome/mac){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/ru/legal/privacy/ru/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://support.apple.com/ru-ru/mail){ .card-link title=Документация}

Почта Apple имеет возможность загружать удаленный контент в фоновом режиме или полностью блокировать его и скрывать ваш IP-адрес от отправителей на [macOS](https://support.apple.com/ru-ru/guide/mail/mlhl03be2866/mac) и [iOS](https://support.apple.com/ru-ru/guide/iphone/iphf084865c7/ios).

### Canary Mail (iOS)

!!! recommendation

    ![Логотип Canary Mail](assets/img/email-clients/canarymail.svg){ align=right }
    
    **Canary Mail** - это платный почтовый клиент, разработанный для обеспечения сквозного шифрования с такими функциями безопасности, как биометрическая блокировка приложений.
    
    [:octicons-home-16: Домашняя страница](https://canarymail.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://canarymail.io/privacy.html){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://canarymail.zendesk.com/){ .card-link title=Документация}
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.canarymail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1236045954)
        - [:simple-windows11: Windows](https://canarymail.io/downloads.html)

!!! warning "Осторожно"

    Canary Mail только недавно выпустила клиенты для Windows и Android. Мы считаем, что они не настолько стабильные, как клиенты для iOS и Mac.

Canary Mail имеет закрытый исходный код. Мы рекомендуем его из-за небольшого выбора почтовых клиентов на iOS, поддерживающих PGP E2EE.

### FairEmail (Android)

!!! recommendation

    ![Логотип Mailvelope](assets/img/email-clients/mailvelope.svg){ align=right }
    
    **Mailvelope** - браузерное расширение, позволяющее обмениваться зашифрованными письмами по стандарту OpenPGP.
    
    [Перейти на mailvelope.com](https://www.mailvelope.com){ .md-button .md-button--primary } [Политика конфиденциальности](https://www.mailvelope.com/en/privacy-policy){ .md-button }
    
    **Скачать**
    - [:fontawesome-brands-firefox: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
    - [:fontawesome-brands-chrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
    - [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)
    - [:fontawesome-brands-github: Исходный код](https://github.com/mailvelope/mailvelope) [Перейти на kontact.kde.org](https://kontact.kde.org){ .md-button .md-button--primary } [Политика конфиденциальности](https://kde.org/privacypolicy-apps){ .md-button }

### GNOME Evolution (GNOME)

!!! recommendation

    ![K-9 Mail logo](assets/img/email-clients/k9mail.svg){ align=right }
    
    **K-9 Mail** - независимое почтовое приложение, которое поддерживает и POP3, и IMAP (только push). [Перейти на k9mail.app](https://k9mail.app){ .md-button .md-button--primary } [Политика конфиденциальности](https://k9mail.app/privacy){ .md-button }
    
    downloads
     - [:fontawesome-brands-firefox: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
    - [:fontawesome-brands-chrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
    - [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)
    - [:fontawesome-brands-github: Исходный код](https://github.com/mailvelope/mailvelope) downloads
    
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

### K-9 Mail (Android)

!!! recommendation

    ![FairEmail logo](assets/img/email-clients/fairemail.svg){ align=right }
    
    **FairEmail** — минимальное почтовое приложение с открытым исходным ходом, использующее открытые стандарты (IMAP, SMTP, OpenPGP) с малым потреблением памяти и заряда батареи.
    
    [Перейти на email.faircode.eu](https://email.faircode.eu){ .md-button .md-button--primary } [Политика конфиденциальности](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .md-button }
    
    downloads
    
        - [:fontawesome-brands-google-play: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
        - [:pg-f-droid: F-Droid](https://f-droid.org/packages/com.fsck.k9/)
        - [:fontawesome-brands-github: Исходный код](https://github.com/k9mail) downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
        - [:simple-github: GitHub](https://github.com/k9mail/k-9/releases)

!!! note

    ![Canary Mail logo](assets/img/email-clients/canarymail.svg){ align=right }
    
    **Canary Mail** - платный почтовый клиент, разработанный для обеспечения сквозного шифрования с использованием таких функций, как биометрическая блокировка и т.д. [Перейти на canarymail.io](https://canarymail.io){ .md-button .md-button--primary } [Политика конфиденциальности](https://canarymail.io/privacy.html){ .md-button }

### Kontact (KDE)

!!! recommendation

    ![Kontact logo](assets/img/email-clients/kontact.svg){ align=right }
    
    **Kontact** is a personal information manager (PIM) application from the [KDE](https://kde.org) project. It provides a mail client, address book, organizer and RSS client.
    
    [:octicons-home-16: Homepage](https://kontact.kde.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://kontact.kde.org/users/){ .card-link title=Documentation}
    [:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://kde.org/community/donations/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-linux: Linux](https://kontact.kde.org/download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

### Mailvelope (Browser)

!!! recommendation

    ![Mailvelope logo](assets/img/email-clients/mailvelope.svg){ align=right }
    
    **Mailvelope** is a browser extension that enables the exchange of encrypted emails following the OpenPGP encryption standard.
    
    [:octicons-home-16: Homepage](https://www.mailvelope.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mailvelope.com/en/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mailvelope.com/faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

### NeoMutt (CLI)

!!! recommendation

    ![NeoMutt logo](assets/img/email-clients/mutt.svg){ align=right }
    
    **NeoMutt** is an open-source command line mail reader (or MUA) for Linux and BSD. It's a fork of [Mutt](https://en.wikipedia.org/wiki/Mutt_(email_client)) with added features.
    
    NeoMutt is a text-based client that has a steep learning curve. It is however, very customizable.
    
    [:octicons-home-16: Homepage](https://neomutt.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://neomutt.org/guide/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.paypal.com/paypalme/russon/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-apple: macOS](https://neomutt.org/distro)
        - [:simple-linux: Linux](https://neomutt.org/distro)

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! Для уменьшения этой угрозы рассмотрите возможность самостоятельного хостинга.

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. Мы учитываем и обсуждаем много факторов, перед тем как рекомендовать какой-то проект, и документирование каждого из них ещё не завершено.

### Минимальные требования

- Apps developed for open-source operating systems must be open-source.
- Must not collect telemetry, or have an easy way to disable all telemetry.
- Must support OpenPGP message encryption.

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Should be open-source.
- Should be cross-platform.
- Should not collect any telemetry by default.
- Should support OpenPGP natively, i.e. without extensions.
- Should support storing OpenPGP encrypted emails locally.
