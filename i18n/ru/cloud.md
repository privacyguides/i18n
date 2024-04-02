---
meta_title: "Лучшие приватные и безопасные облачные хранилища - Privacy Guides"
title: "Облачное хранилище"
icon: material/file-cloud
description: Многие облачные хранилища требуют от вас полностью им доверять, что они не будут просматривать ваши файлы. Это приватные альтернативы!
cover: cloud.webp
---

Многие облачные хранилища требуют от вас полностью им доверять, что они не будут просматривать ваши файлы. Альтернативы, перечисленные ниже, устраняют необходимость в доверии путем внедрения безопасного E2EE.

Если эти альтернативы не соответствуют вашим потребностям, мы предлагаем вам рассмотреть возможность использования программного обеспечения для шифрования, например, [Cryptomator](encryption.md#cryptomator-cloud) с другими облачными хранилищами. Использование Cryptomator в сочетании с **любым** облачным хранилищем (включая эти) может быть хорошей идеей для снижения риска ошибок шифрования в собственных клиентах провайдера.

<details class="TYPE" markdown>
<summary>Looking for Nextcloud?</summary>

Nextcloud is [still a recommended tool](productivity.md) for self-hosting a file management suite, however we do not recommend third-party Nextcloud storage providers at the moment, because we do [not recommend](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) Nextcloud's built-in E2EE functionality for home users.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Логотип Proton Drive](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** - швейцарское зашифрованное облачных хранилищ от популярного провайдера зашифрованной электронной почты [Proton Mail](email.md#proton-mail).

[:octicons-home-16: Homepage](https://proton.me/drive){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:simple-windows11: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

Веб-приложение Proton Drive прошло независимый аудит компании Securitum в [2021 году](https://proton.me/blog/security-audit-all-proton-apps), полные подробности не были предоставлены, но в аттестационном письме Securitum говорится:

> Аудиторы выявили две уязвимости низкой степени серьезности. Кроме того, были представлены пять общих рекомендаций. В то же время мы подтверждаем, что в ходе теста на проникновение не было выявлено никаких важных проблем с безопасностью.

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
- [:simple-windows11: Windows](https://tresorit.com/download)
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

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://www.efd.admin.ch/efd/en/home/digitalisierung/swiss-digital-initiative.html) which requires passing [35 criteria](https://digitaltrust-label.swiss/criteria) related to security, privacy, and reliability.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

### Минимальные требования

- Должны использовать обязательное сквозное шифрование.
- Должны иметь бесплатную версию или пробный период для тестирования.
- Должны поддерживать многофакторную аутентификацию TOTP или FIDO2, а также вход с помощью Passkey.
- Должны иметь веб-интерфейс, поддерживающий основные функции управления файлами.
- Должны обеспечивать легкий экспорт всех файлов/документов.
- Должно использоваться стандартное, проверенное шифрование.

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Clients should be open source.
- Клиенты должны быть полностью проверены независимой третьей стороной.
- Должны предлагать нативные клиенты для Linux, Android, Windows, macOS и iOS.
    - Эти клиенты должны интегрироваться с собственными инструментами ОС для сервисов облачных хранилищ, такими как интеграция приложения Files на iOS или функциональность DocumentsProvider на Android.
- Должны поддерживать простой обмен файлами с другими пользователями.
- Должны предлагать, по крайней мере, базовые функции предварительного просмотра и редактирования файлов в веб-интерфейсе.

[^1]: Соотвествие стандарту [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 относится к [системе управления информационной безопасностью](https://en.wikipedia.org/wiki/Information_security_management) компании и распространяется на продажу, разработку, обслуживание и поддержку облачных услуг.
