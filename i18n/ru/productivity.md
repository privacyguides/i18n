---
title: "Инструменты для продуктивности"
icon: material/file-sign
description: Большинство онлайновых офисных пакетов не поддерживают E2EE, что означает, что поставщик облачных услуг имеет доступ ко всему, что вы делаете.
cover: productivity.png
---

Большинство онлайновых офисных пакетов не поддерживают E2EE, что означает, что поставщик облачных услуг имеет доступ ко всему, что вы делаете. Политика конфиденциальности может юридически защитить ваши права, но она не обеспечивает технических ограничений доступа.

## Платформы для совместной работы

### Nextcloud

!!! recommendation

    ![Логотип Nextcloud](assets/img/productivity/nextcloud.svg){ align=right }
    
    **Nextcloud** - это набор бесплатного клиент-серверного программного обеспечения с открытым исходным кодом для создания собственного сервиса хранилища файлов на приватном сервере, который вы контролируете.
    
    [:octicons-home-16: Домашняя страница](https://nextcloud.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://nextcloud.com/support/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://nextcloud.com/contribute/){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
        - [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
        - [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
        - [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
        - [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

!!! recommendation

    Мы не рекомендуем использовать [плагин E2EE](https://apps.nextcloud.com/apps/end_to_end_encryption) для Nextcloud, так как это может привести к потере данных; это очень экспериментальный продукт, который недостаточно качественен для полноценного использования. По этой причине мы не рекомендуем сторонних провайдеров Nextcloud.

### CryptPad

!!! recommendation

    ![Логотип CryptPad](assets/img/productivity/cryptpad.svg){ align=right }
    
    **CryptPad** - это приватная альтернатива популярным офисным инструментам. Все содержимое этой веб-службы шифруется сквозным шифрованием и может быть легко передано другим пользователям.
    
    [:octicons-home-16: Домашняя страница](https://cryptpad.fr){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://docs.cryptpad.fr/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=Поддержать }

### Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

!!! example "Это новый раздел"

    Мы всё еще работаем над установлением критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у вас есть вопросы по поводу наших критериев, пожалуйста, [задавайте их на нашем форуме](https://discuss.privacyguides.net/latest). Если какой-то критерий здесь не указан, это не значит, что мы его не учли. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

В целом, мы определяем платформы для совместной работы как полноценные комплексы, которые могут разумно заменить такие платформы для совместной работы, как Google Drive.

- Открытый исходный код.
- Если E2EE не используется, то файлы должны быть доступны через WebDAV.
- Имеет клиенты синхронизации для Linux, macOS и Windows.
- Поддерживает редактирование документов и электронных таблиц.
- Поддерживает совместную работу с документами в режиме реального времени.
- Поддерживает экспорт документов в стандартные форматы документов (например, ODF).

#### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Должен хранить файлы в обычной файловой системе.
- Должны либо поддерживать многофакторную аутентификацию TOTP или FIDO2, либо вход с помощью Passkey.

## Офисные пакеты

### LibreOffice

!!! recommendation

    ![Логотип LibreOffice](assets/img/productivity/libreoffice.svg){ align=right }
    
    **LibreOffice** - это бесплатный офисный пакет с открытым исходным кодом и широкими функциональными возможностями.
    
    [:octicons-home-16: Домашняя страница](https://www.libreoffice.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.libreoffice.org/about-us/privacy/privacy-policy-en/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://documentation.libreoffice.org/en/english-documentation/){ .card-link title=Документация}
    [:octicons-code-16:](https://www.libreoffice.org/about-us/source-code){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://www.libreoffice.org/donate/){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://www.libreoffice.org/download/android-and-ios/)
        - [:simple-appstore: App Store](https://www.libreoffice.org/download/android-and-ios/)
        - [:simple-windows11: Windows](https://www.libreoffice.org/download/download/)
        - [:simple-apple: macOS](https://www.libreoffice.org/download/download/)
        - [:simple-linux: Linux](https://www.libreoffice.org/download/download/)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.libreoffice.LibreOffice)

### OnlyOffice

!!! recommendation

    ![Логотип OnlyOffice](assets/img/productivity/onlyoffice.svg){ align=right }
    
    **OnlyOffice** - это облачный бесплатный офисный пакет с открытым исходным кодом и широкими функциональными возможностями, включающими интеграцию с Nextcloud.
    
    [:octicons-home-16: Домашняя страница](https://www.onlyoffice.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://help.onlyoffice.com/products/files/doceditor.aspx?fileid=5048502&doc=SXhWMEVzSEYxNlVVaXJJeUVtS0kyYk14YWdXTEFUQmRWL250NllHNUFGbz0_IjUwNDg1MDIi0){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://helpcenter.onlyoffice.com/userguides.aspx){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/ONLYOFFICE){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onlyoffice.documents)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id944896972)
        - [:simple-windows11: Windows](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-apple: macOS](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-linux: Linux](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.onlyoffice.desktopeditors)

### Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

!!! example "Это новый раздел"

    Мы всё еще работаем над установлением критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у вас есть вопросы по поводу наших критериев, пожалуйста, [задавайте их на нашем форуме](https://discuss.privacyguides.net/latest). Если какой-то критерий здесь не указан, это не значит, что мы его не учли. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

В целом, мы определяем офисные пакеты как приложения, которые могут разумно заменить Microsoft Word для большинства потребностей.

- Должны быть кроссплатформенными.
- Должны иметь открытый исходный код.
- Должны работать офлайн.
- Должны поддерживать редактирование документов, таблиц и презентаций.
- Должны экспортировать файлы в стандартные форматы документов.

## Размещение текста

### PrivateBin

!!! recommendation

    ![Логотип PrivateBin](assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** - это минималистичный онлайновый сервис размещения текста с открытым исходным кодом, где сервер не знает о вставляемых данных. Данные шифруются/дешифруются в браузере с помощью 256-битного AES. Это улучшенная версия ZeroBin. Существует [список экземпляров](https://privatebin.info/directory/).
    
    [:octicons-home-16: Домашняя страница](https://privatebin.info){ .md-button .md-button--primary }
    [:octicons-server-16:](https://privatebin.info/directory/){ .card-link title="Публичный экземпляр"}
    [:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/wiki/FAQ){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Исходный код" }

### Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Мы рекомендуем тебе ознакомиться с этим списком, прежде чем выбрать продукт, и провести собственное исследование, чтобы убедиться в правильности своего выбора.

!!! example "Это новый раздел"

    Мы пока работаем над установлением определенных критериев для каждого раздела нашего сайта, и они могут поменяться в будущем. Если у тебя есть какие-нибудь вопросы по поводу наших критериев, пожалуйста, [задавай их на нашем форуме](https://discuss.privacyguides.net/latest) и не думай, что мы не учли что-то при составлении наших рекомендаций, если это не указано здесь. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

#### Минимальные требования

- Должен быть с открытым исходным кодом.
- Должно быть реализовано сквозное шифрование "с нулевым доверием".
- Должен поддерживать файлы, защищенные паролем.


#### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Должен иметь опубликованный аудит от авторитетной, независимой третьей стороны.
