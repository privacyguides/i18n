---
title: "Почтовые клиенты"
icon: material/email-open
description: Эти почтовые клиенты соблюдают конфиденциальность и поддерживают шифрование электронной почты OpenPGP.
cover: email-clients.webp
---

Наш список рекомендаций содержит только почтовые клиенты, которые поддерживают [OpenPGP](/encryption/#openpgp) и безопасную аутентификацию (например, [OAuth](https://ru.wikipedia.org/wiki/OAuth)). OAuth позволяет использовать [многофакторную аутентификацию](basics/multi-factor-authentication.md) и предотвратить кражу учетных записей.

??? warning "Электронная почта не обеспечивает прямую секретность"

    При использовании технологии сквозного шифрования (E2EE), например OpenPGP, электронная почта все равно будет содержать [некоторые метаданные](email.md#email-metadata-overview), которые не зашифрованы в заголовке письма.
    
    OpenPGP также не поддерживает прямую секретность](https://ru.wikipedia.org/wiki/Perfect_forward_secrecy), что означает: если ваш приватный ключ или приватный ключ получателя будет украден, то все предыдущие сообщения, зашифрованные с его помощью, будут раскрыты: [Как защитить мои приватные ключи?](basics/email-security.md) Рассмотрите возможность использования среды, обеспечивающей прямую секретность:
    
    [Связь в реальном времени](real-time-communication.md){ .md-button }

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

    ![Логотип FairEmail](assets/img/email-clients/fairemail.svg){ align=right }
    
    **FairEmail** - это небольшое приложение электронной почты с открытым исходным кодом, использующее открытые стандарты (IMAP, SMTP, OpenPGP) с низким потреблением данных и заряда батареи.
    
    [:octicons-home-16: Домашняя страница](https://email.faircode.eu){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://email.faircode.eu/donate/){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
        - [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

### GNOME Evolution (GNOME)

!!! recommendation

    ![Логотип Evolution](assets/img/email-clients/evolution.svg){ align=right }
    
    **Evolution** — это приложение для управления персональной информацией, которое обеспечивает интегрированную почту, календарь и функциональность адресной книги. Evolution имеет подробную [документацию](https://help.gnome.org/users/evolution/stable/), чтобы помочь вам начать работу.
    
    [:octicons-home-16: Домашняя страница](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://help.gnome.org/users/evolution/stable/){ .card-link title=Документация}
    [:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution/){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://www.gnome.org/donate/){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

### K-9 Mail (Android)

!!! recommendation

    ![логотип K-9 Mail](assets/img/email-clients/k9mail.svg){ align=right }
    
    **K-9 Mail** — это независимое почтовое приложение, которое поддерживает как POP3, так и IMAP, но поддерживает только push-почту для IMAP.
    
    В будущем, K-9 Mail станет [официальным](https://k9mail.app/2022/06/13/K-9-Mail-and-Thunderbird.html) клиентом Thunderbird для Android.
    
    [:octicons-home-16: Homepage](https://k9mail.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://k9mail.app/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://docs.k9mail.app/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/thundernest/k-9){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://k9mail.app/contribute){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
        - [:simple-github: GitHub](https://github.com/thundernest/k-9/releases)

!!! warning "Осторожно"

    Когда вы отвечаете кому-то на письмо, отправленное сразу нескольким людям, поле с получателем может также содержать несколько адресов. Более подробную информацию можно найти тут [thundernest/k-9 #3738](https://github.com/thundernest/k-9/issues/3738).

### Kontact (KDE)

!!! recommendation

    ![Логотип Kontact](assets/img/email-clients/kontact.svg){ align=right }
    
    **Kontact** - это менеджер персональной информации от проекта [KDE](https://kde.org). Он предоставляет почтовый клиент, адресную книгу, органайзер и клиент RSS.
    
    [:octicons-home-16: Домашняя страница](https://kontact.kde.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://kontact.kde.org/users/){ .card-link title=Документация}
    [:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://kde.org/community/donations/){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-linux: Linux](https://kontact.kde.org/download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

### Mailvelope (Браузер)

!!! recommendation

    ![Логотип Mailvelope](assets/img/email-clients/mailvelope.svg){ align=right }
    
    **Mailvelope** - это расширение для браузера, позволяющее обмениваться зашифрованными электронными письмами в соответствии со стандартом шифрования OpenPGP.
    
    [:octicons-home-16: Домашняя страница](https://www.mailvelope.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mailvelope.com/en/privacy-policy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://mailvelope.com/faq){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

### NeoMutt (Командная строка)

!!! recommendation

    ![Логотип NeoMutt](assets/img/email-clients/mutt.svg){ align=right }
    
    **NeoMutt** - это читалка почты (или MUA) для командной строки с открытым исходным кодом для Linux и BSD. Это форк [Mutt](https://en.wikipedia.org/wiki/Mutt_(email_client)) с добавленными возможностями.
    
    Neomut - это текстовый клиент, которым сложно научиться пользоваться. Тем не менее он очень кастомизируемый.
    
    [:octicons-home-16: Домашняя страница](https://neomutt.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://neomutt.org/guide/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://www.paypal.com/paypalme/russon/){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-apple: macOS](https://neomutt.org/distro)
        - [:simple-linux: Linux](https://neomutt.org/distro)

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

!!! example "Это новый раздел"

    Мы всё еще работаем над установлением критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у вас есть вопросы по поводу наших критериев, пожалуйста, [задавайте их на нашем форуме](https://discuss.privacyguides.net/latest). Если какой-то критерий здесь не указан, это не значит, что мы его не учли. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

### Минимальные требования

- Apps developed for open-source operating systems must be open source.
- Не должны собирать телеметрию или должен быть простой способ её отключить.
- Должны поддерживать шифрование сообщений OpenPGP.

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Should be open source.
- Должны быть кроссплатформенными.
- По умолчанию не должны собирать телеметрию.
- Должны нативно поддерживать OpenPGP, т.е. без расширений.
- Должны поддерживать локальное хранение писем, зашифрованных OpenPGP.
