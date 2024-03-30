---
title: "Заметки"
icon: material/notebook-edit-outline
description: These encrypted note-taking apps let you keep track of your notes without giving them to a third-party.
cover: notebooks.webp
---

Сохраняйте свои заметки и дневники, не передавая их третьим лицам.

Если вы в настоящее время используете такие приложения, как Evernote, Google Keep или Microsoft OneNote, то мы предлагаем вам выбрать альтернативу с поддержкой E2EE.

## Облачные сервисы

### Standard Notes

<div class="admonition recommendation" markdown>

![Логотип Standard Notes](assets/img/notebooks/standard-notes.svg){ align=right }

**Standard Notes** - это простое и приватное приложение для заметок, которое делает ваши заметки легкими и доступными везде, где бы вы ни находились. Приложение имеет E2EE на каждой платформе и продвинутый функционал с темами и кастомными редакторами для ПК. Он также прошел [независимый аудит](https://standardnotes.com/help/2/has-standard-notes-completed-a-third-party-security-audit).

[:octicons-home-16: Homepage](https://standardnotes.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://standardnotes.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://standardnotes.com/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/standardnotes){ .card-link title="Source Code" }
[:octicons-heart-16:](https://standardnotes.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.standardnotes)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1285392450)
- [:simple-github: GitHub](https://github.com/standardnotes/app/releases)
- [:simple-windows11: Windows](https://standardnotes.com)
- [:simple-apple: macOS](https://standardnotes.com)
- [:simple-linux: Linux](https://standardnotes.com)
- [:octicons-globe-16: Web](https://app.standardnotes.com)

</details>

</div>

### Notesnook

<div class="admonition recommendation" markdown>

![Notesnook logo](assets/img/notebooks/notesnook.svg){ align=right }

**Notesnook** is a free (as in speech) & open-source note-taking app focused on user privacy & ease of use. В нем реализовано сквозное шифрование на всех платформах и мощная синхронизация, позволяющая делать заметки на ходу. You can easily import your notes from Evernote, OneNote & a lot of other apps using their [official importer](https://importer.notesnook.com).

[:octicons-home-16: Homepage](https://notesnook.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://notesnook.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.notesnook.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/streetwriters/notesnook){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/streetwriters/notesnook/blob/master/CONTRIBUTING.md){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.streetwriters.notesnook)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1544027013)
- [:simple-github: GitHub](https://github.com/streetwriters/notesnook/releases)
- [:simple-windows11: Windows](https://notesnook.com/downloads)
- [:simple-apple: macOS](https://notesnook.com/downloads)
- [:simple-linux: Linux](https://notesnook.com/downloads)
- [:simple-firefoxbrowser: Firefox](https://notesnook.com/notesnook-web-clipper)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/notesnook-web-clipper/kljhpemdlcnjohmfmkogahelkcidieaj)

</details>

</div>

Notesnook only allows local note encryption with the [private vault](https://help.notesnook.com/lock-notes-with-private-vault) feature on their pro plan, otherwise your notes are not stored encrypted on your device. Your notes are always encrypted before being synced to their servers with keys which only you have access to.

### Joplin

<div class="admonition recommendation" markdown>

![Логотип Joplin](assets/img/notebooks/joplin.svg){ align=right }

**Joplin** - это бесплатное, открытое приложение с богатой функциональностью для ведения заметок и списков задач, которое может обрабатывать большое количество заметок в формате Markdown, упорядоченных по тегам и записным книжкам. Приложение предлагает E2EE и может синхронизироваться через Nextcloud, Dropbox и др. Приложение также предлагает легкий перенос данных из Evernote и простых текстовых заметок.

[:octicons-home-16: Homepage](https://joplinapp.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://joplinapp.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://joplinapp.org/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/laurent22/joplin){ .card-link title="Source Code" }
[:octicons-heart-16:](https://joplinapp.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.cozic.joplin)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1315599797)
- [:simple-github: GitHub](https://github.com/laurent22/joplin-android/releases)
- [:simple-windows11: Windows](https://joplinapp.org/#desktop-applications)
- [:simple-apple: macOS](https://joplinapp.org/#desktop-applications)
- [:simple-linux: Linux](https://joplinapp.org/#desktop-applications)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/joplin-web-clipper)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/joplin-web-clipper/alofnhikmmkdbbbgpnglcpdollgjjfek)

</details>

</div>

Joplin does not [support](https://github.com/laurent22/joplin/issues/289) password/PIN protection for the application itself or individual notes and notebooks. Но ваши данные по-прежнему шифруются вашим секретным ключом при передаче и в месте синхронизации. Since January 2023, Joplin [supports biometrics](https://github.com/laurent22/joplin/commit/f10d9f75b055d84416053fab7e35438f598753e9) app lock for Android and iOS.

### Cryptee

<div class="admonition recommendation" markdown>

![Логотип Cryptee](./assets/img/notebooks/cryptee.svg#only-light){ align=right }
![Логотип Cryptee](./assets/img/notebooks/cryptee-dark.svg#only-dark){ align=right }

**Cryptee** - это веб-редактор документов и приложение для хранения фотографий с поддержкой E2EE и открытым исходным кодом. Cryptee - это PWA, что означает, что он работает без проблем на всех современных устройствах, не требуя нативных приложений для каждой соответствующей платформы.

[:octicons-home-16: Homepage](https://crypt.ee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://crypt.ee/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://crypt.ee/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/cryptee){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-globe-16: PWA](https://crypt.ee/download)

</details>

</div>

Cryptee предлагает 100 МБ хранилища бесплатно, а если вам нужно больше, вы можете воспользоваться платными опциями. Регистрация не требует указания электронной почты или другой персональной информации.

## Локальные сервисы

### Org-mode

<div class="admonition recommendation" markdown>

![Org-mode logo](assets/img/notebooks/org-mode.svg){ align=right }

**Org-mode** is a [major mode](https://gnu.org/software/emacs/manual/html_node/elisp/Major-Modes.html) for GNU Emacs. Org-mode предназначен для ведения заметок, to-do листов, планирования проектов и создания документов с помощью быстрой и эффективной системы работы с обычным текстом. Синхронизация возможна с помощью программ для [синхронизации файлов](file-sharing.md#синхронизация-файлов).

[:octicons-home-16: Домашняя страница](https://orgmode.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://orgmode.org/manuals.html){ .card-link title=Документация}
[:octicons-code-16:](https://git.savannah.gnu.org/cgit/emacs/org-mode.git){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://liberapay.com/bzg){ .card-link title=Поддержать }

</details>

</div>

## Критерии

**Обратите внимание, что у нас нет связей ни с одним из проектов, которые мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md)мы разработали четкий набор требований, позволяющий нам давать объективные рекомендации. Мы рекомендуем вам ознакомиться с этим списком, прежде чем выбрать программу, и провести самостоятельное исследование, чтобы убедиться, что это правильный выбор для вас.

- Clients must be open source.
- Облачная синхронизация должна использовать E2EE.
- Должна быть поддержка экспорта документов в стандартных форматах.

### В лучшем случае

- Функции локального резервного копирования/синхронизации должны поддерживать шифрование.
- Облачные платформы должны поддерживать обмен документами.
