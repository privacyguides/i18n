---
title: "Инструменты продуктивности"
icon: material/file-sign
description: Большинство онлайновых офисных пакетов не поддерживают E2EE, что означает, что поставщик облачных услуг имеет доступ ко всему, что вы делаете.
cover: productivity.webp
---

<!-- markdownlint-disable MD024 -->
Большинство онлайновых офисных пакетов не поддерживают E2EE, что означает, что поставщик облачных услуг имеет доступ ко всему, что вы делаете. Политика конфиденциальности может юридически защитить ваши права, но она не обеспечивает технических ограничений доступа.

## Платформы для совместной работы

### Nextcloud

<div class="admonition recommendation" markdown>

![Логотип Nextcloud](assets/img/productivity/nextcloud.svg){ align=right }

**Nextcloud** - это набор бесплатного клиент-серверного программного обеспечения с открытым исходным кодом для создания собственного сервиса хранилища файлов на приватном сервере, который вы контролируете.

[:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Мы не рекомендуем использовать [плагин E2EE](https://apps.nextcloud.com/apps/end_to_end_encryption) для Nextcloud, так как это может привести к потере данных; это очень экспериментальный продукт, который недостаточно качественен для полноценного использования. По этой причине мы не рекомендуем сторонних провайдеров Nextcloud.

</div>

### CryptPad

<div class="admonition recommendation" markdown>

![Логотип CryptPad](assets/img/productivity/cryptpad.svg){ align=right }

**CryptPad** - это приватная альтернатива популярным офисным инструментам. Все содержимое этой веб-службы шифруется сквозным шифрованием и может быть легко передано другим пользователям.

[:octicons-home-16: Homepage](https://cryptpad.fr){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.cryptpad.fr){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=Contribute }

</details>

</div>

### Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

#### Минимальные требования

В целом, мы определяем платформы для совместной работы как полноценные комплексы, которые могут разумно заменить такие платформы для совместной работы, как Google Drive.

- Open source.
- Если E2EE не используется, то файлы должны быть доступны через WebDAV.
- Имеет клиенты синхронизации для Linux, macOS и Windows.
- Поддерживает редактирование документов и электронных таблиц.
- Поддерживает совместную работу с документами в режиме реального времени.
- Поддерживает экспорт документов в стандартные форматы документов (например, ODF).

#### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Должен хранить файлы в обычной файловой системе.
- Should support TOTP or FIDO2 multi-factor authentication support, or passkey logins.

## Офисные пакеты

### LibreOffice

<div class="admonition recommendation" markdown>

![Логотип LibreOffice](assets/img/productivity/libreoffice.svg){ align=right }

**LibreOffice** - это бесплатный офисный пакет с открытым исходным кодом и широкими функциональными возможностями.

[:octicons-home-16: Homepage](https://libreoffice.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://libreoffice.org/about-us/privacy/privacy-policy-en){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://documentation.libreoffice.org/en/english-documentation){ .card-link title=Documentation}
[:octicons-code-16:](https://libreoffice.org/about-us/source-code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://libreoffice.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://libreoffice.org/download/android-and-ios)
- [:simple-appstore: App Store](https://libreoffice.org/download/android-and-ios)
- [:fontawesome-brands-windows: Windows](https://libreoffice.org/download/download)
- [:simple-apple: macOS](https://libreoffice.org/download/download)
- [:simple-linux: Linux](https://libreoffice.org/download/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.libreoffice.LibreOffice)

</details>

</div>

### OnlyOffice

<div class="admonition recommendation" markdown>

![Логотип OnlyOffice](assets/img/productivity/onlyoffice.svg){ align=right }

**OnlyOffice** - это облачный бесплатный офисный пакет с открытым исходным кодом и широкими функциональными возможностями, включающими интеграцию с Nextcloud.

[:octicons-home-16: Homepage](https://onlyoffice.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://help.onlyoffice.com/products/files/doceditor.aspx?fileid=5048502&doc=SXhWMEVzSEYxNlVVaXJJeUVtS0kyYk14YWdXTEFUQmRWL250NllHNUFGbz0_IjUwNDg1MDIi0){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://helpcenter.onlyoffice.com/userguides.aspx){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ONLYOFFICE){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onlyoffice.documents)
- [:simple-appstore: App Store](https://apps.apple.com/app/id944896972)
- [:fontawesome-brands-windows: Windows](https://onlyoffice.com/download-desktop.aspx)
- [:simple-apple: macOS](https://onlyoffice.com/download-desktop.aspx)
- [:simple-linux: Linux](https://onlyoffice.com/download-desktop.aspx)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.onlyoffice.desktopeditors)

</details>

</div>

### Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

В целом, мы определяем офисные пакеты как приложения, которые могут разумно заменить Microsoft Word для большинства потребностей.

- Должны быть кроссплатформенными.
- Должны иметь открытый исходный код.
- Должны работать офлайн.
- Должны поддерживать редактирование документов, таблиц и презентаций.
- Должны экспортировать файлы в стандартные форматы документов.

## Размещение текста

### PrivateBin

<div class="admonition recommendation" markdown>

![Логотип PrivateBin](assets/img/productivity/privatebin.svg){ align=right }

**PrivateBin** - это минималистичный онлайновый сервис размещения текста с открытым исходным кодом, где сервер не знает о вставляемых данных. Данные шифруются/дешифруются в браузере с помощью 256-битного AES. Это улучшенная версия ZeroBin.

[:octicons-home-16: Homepage](https://privatebin.info){ .md-button .md-button--primary }
[:octicons-server-16:](https://privatebin.info/directory){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/wiki/FAQ){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Source Code" }

</div>

### Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Мы рекомендуем тебе ознакомиться с этим списком, прежде чем выбрать продукт, и провести собственное исследование, чтобы убедиться в правильности своего выбора.

#### Минимальные требования к сервисам

- Исходный код проекта должен быть открыт.
- Должно быть реализовано сквозное шифрование "с нулевым доверием".
- Должен поддерживать файлы, защищенные паролем.

#### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Должен иметь опубликованный аудит от авторитетной, независимой третьей стороны.

## Language services

### LanguageTool

<div class="admonition recommendation" markdown>

![LanguageTool logo](assets/img/productivity/languagetool.svg#only-light){ align=right }
![LanguageTool logo](assets/img/productivity/languagetool-dark.svg#only-dark){ align=right }

**LanguageTool** is a multilingual grammar, style and spell checker that supports more than 20 languages. The software is [self-hostable](https://dev.languagetool.org/http-server), and the extensions do not send your input text to their server.

  LanguageTool offers integration with a variety of [office suites](https://languagetool.org/services#text_editors) and [email clients](https://languagetool.org/services#mail_clients).

[:octicons-home-16: Homepage](https://languagetool.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://languagetool.org/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://languagetooler.freshdesk.com/en/support/solutions){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/languagetool-org){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1534275760)
- [:fontawesome-brands-windows: Windows](https://languagetool.org/windows-desktop)
- [:simple-apple: macOS](https://languagetool.org/mac-desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/languagetool)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/grammar-and-spell-checker/oldceeleldhonbafppcapldpdifcinji)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/hfjadhjooeceemgojogkhlppanjkbobc)
- [:simple-safari: Safari](https://apps.apple.com/app/id1534275760)

</details>

</div>

### Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

- Исходный код проекта должен быть открыт.
- Must be possible to self-host.
