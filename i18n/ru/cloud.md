---
meta_title: "Лучшие приватные и безопасные облачные хранилища - Privacy Guides"
title: "Облачное хранилище"
icon: material/file-cloud
description: Многие облачные хранилища требуют от вас полностью им доверять, что они не будут просматривать ваши файлы. Это приватные альтернативы!
cover: cloud.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Пассивные атаки](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Поставщики услуг](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Many **cloud storage providers** require your full trust that they will not look at your files. Альтернативы, перечисленные ниже, устраняют необходимость в доверии путем внедрения безопасного E2EE.

Если эти альтернативы не соответствуют вашим потребностям, мы предлагаем вам рассмотреть возможность использования программного обеспечения для шифрования, например, [Cryptomator](encryption.md#cryptomator-cloud) с другими облачными хранилищами. Использование Cryptomator в сочетании с **любым** облачным хранилищем (включая эти) может быть хорошей идеей для снижения риска ошибок шифрования в собственных клиентах провайдера.

<details class="admonition info" markdown>
<summary>Looking for Nextcloud?</summary>

Nextcloud is [still a recommended tool](document-collaboration.md#nextcloud) for self-hosting a file management suite, however we do not recommend third-party Nextcloud storage providers at the moment, because we do [not recommend](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) Nextcloud's built-in E2EE functionality for home users.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** is an encrypted cloud storage provider from the popular encrypted email provider [Proton Mail](email.md#proton-mail). The initial free storage is limited to 2GB, but with the completion of certain steps, additional storage can be obtained up to 5GB.

[:octicons-home-16: Homepage](https://proton.me/drive){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

The Proton Drive web application has been independently audited by Securitum in [2021](https://proton.me/community/open-source).

Proton Drive's brand new mobile clients have not yet been publicly audited by a third party.

## Tresorit

<div class="admonition recommendation" markdown>

![Логотип Tresorit](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit** - швейцарско-венгерский провайдер зашифрованных облачных хранилищ, основанный в 2011 году. Tresorit принадлежит Swiss Post, национальной почтовой службе Швейцарии.

[:octicons-home-16: Homepage](https://tresorit.com){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/id722163232)
- [:fontawesome-brands-windows: Windows](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: Linux](https://tresorit.com/download)

</details>

</div>

Компания Tresorit прошла ряд независимых аудитов безопасности:

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Compliance [Certification](https://certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Penetration Testing by Computest
    - В данном обзоре оценивалась безопасность веб-клиента Tresorit, приложения для Android, приложения для Windows и соответствующей инфраструктуры.
    - Computest обнаружил две уязвимости, которые были устранены.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - В данном обзоре был проанализирован весь исходный код Tresorit и было подтверждено, что реализация соответствует концепциям, описанным в [техническом документе](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf) Tresorit.
    - Компания Ernst & Young дополнительно протестировала веб-приложение, мобильные и настольные клиенты: "Результаты тестирования не выявили никаких отклонений от заявлений Tresorit о конфиденциальности данных."

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en) which requires passing [35 criteria](https://swiss-digital-initiative.org/criteria) related to security, privacy, and reliability.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** is a decentralized protocol and open-source platform for storage, social media, and applications. It provides a secure and private space where users can store, share, and view their photos, videos, documents, etc. Peergos secures your files with quantum-resistant end-to-end encryption and ensures all data about your files remains private. It is built on top of [IPFS (InterPlanetary File System)](https://ipfs.tech), a peer-to-peer architecture that protects against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-globe-16: Web](https://peergos.net)
- [:fontawesome-brands-windows: Windows](https://github.com/Peergos/web-ui/releases)
- [:simple-apple: macOS](https://github.com/Peergos/web-ui/releases)
- [:simple-linux: Linux](https://github.com/Peergos/web-ui/releases)

</details>

</div>

Peergos is primarily a web app, but you can self-host the server either as a local cache for your remote Peergos account, or as a standalone storage server which negates the need to register for a remote account and subscription. The Peergos server is a `.jar` file, which means the Java 17+ Runtime Environment ([OpenJDK download](https://azul.com/downloads)) should be installed on your machine to get it working.

Running a local version of Peergos alongside a registered account on their paid, hosted service allows you to access your Peergos storage without any reliance on DNS or TLS certificate authorities, and keep a copy of your data backed up to their cloud. The user experience should be the same whether you run their desktop server or just use their hosted web interface.

Peergos was [audited](https://cure53.de/pentest-report_peergos.pdf) by Cure53 in September 2019, and all found issues were subsequently fixed.

Also, the Android app is not available but it is [in the works](https://discuss.privacyguides.net/t/peergos-private-storage-sharing-social-media-and-application-platform/11825/25). The current workaround is to use the mobile [PWA](https://peergos.net) instead.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

### Минимальные требования

- Должны использовать обязательное сквозное шифрование.
- Должны иметь бесплатную версию или пробный период для тестирования.
- Must support TOTP or FIDO2 multi-factor authentication, or passkey logins.
- Должны иметь веб-интерфейс, поддерживающий основные функции управления файлами.
- Должны обеспечивать легкий экспорт всех файлов/документов.

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Clients should be open source.
- Клиенты должны быть полностью проверены независимой третьей стороной.
- Должны предлагать нативные клиенты для Linux, Android, Windows, macOS и iOS.
    - Эти клиенты должны интегрироваться с собственными инструментами ОС для сервисов облачных хранилищ, такими как интеграция приложения Files на iOS или функциональность DocumentsProvider на Android.
- Должны поддерживать простой обмен файлами с другими пользователями.
- Должны предлагать, по крайней мере, базовые функции предварительного просмотра и редактирования файлов в веб-интерфейсе.

[^1]: Соотвествие стандарту [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 относится к [системе управления информационной безопасностью](https://en.wikipedia.org/wiki/Information_security_management) компании и распространяется на продажу, разработку, обслуживание и поддержку облачных услуг.
