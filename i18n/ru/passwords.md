---
meta_title: "The Best Password Managers to Protect Your Privacy and Security - Privacy Guides"
title: "Менеджеры паролей"
icon: material/form-textbox-password
description: Password managers allow you to securely store and manage passwords and other credentials.
cover: passwords.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Password Manager Recommendations
    url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Bitwarden
    image: /assets/img/password-management/bitwarden.svg
    url: https://bitwarden.com
    sameAs: https://en.wikipedia.org/wiki/Bitwarden
    applicationCategory: Менеджер паролей
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: 1Password
    image: /assets/img/password-management/1password.svg
    url: https://1password.com
    sameAs: https://en.wikipedia.org/wiki/1Password
    applicationCategory: Менеджер паролей
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Proton Pass
    image: /assets/img/password-management/protonpass.svg
    url: https://proton.me/pass
    applicationCategory: Менеджер паролей
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Psono
    image: /assets/img/password-management/psono.svg
    url: https://psono.com
    applicationCategory: Менеджер паролей
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassXC
    image: /assets/img/password-management/keepassxc.svg
    url: https://keepassxc.org
    sameAs: https://en.wikipedia.org/wiki/KeePassXC
    applicationCategory: Менеджер паролей
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassDX
    image: /assets/img/password-management/keepassdx.svg
    url: https://keepassdx.com
    applicationCategory: Менеджер паролей
    operatingSystem: Android
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Strongbox
    image: /assets/img/password-management/strongbox.svg
    url: https://strongboxsafe.com
    applicationCategory: Менеджер паролей
    operatingSystem: iOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: gopass
    image: /assets/img/password-management/gopass.svg
    url: https://gopass.pw
    applicationCategory: Менеджер паролей
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - FreeBSD
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
---

<small>Protects against the following threat(s):</small>

- [:material-target-account: Целевые атаки](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Пассивные атаки](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Поставщики услуг](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

**Password managers** allow you to securely store and manage passwords and other credentials with the use of a master password.

[Введение в безопасные пароли :material-arrow-right-drop-circle:](./basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">Инфо.</p>

Встроенные менеджеры паролей, например в браузерах и операционных системах, иногда не так хороши, как специализированные программы для управления паролями. Преимуществом встроенных менеджеров паролей является хорошая интеграция с программным обеспечением, но зачастую они могут быть очень простыми и не иметь функций конфиденциальности и безопасности, которыми обладают отдельные программы.

Например, менеджер паролей в Microsoft Edge вообще не поддерживает E2EE. Google's password manager has [optional](https://support.google.com/accounts/answer/11350823) E2EE, and [Apple's](https://support.apple.com/HT202303) offers E2EE by default.

</div>

## Облачные сервисы

Эти менеджеры паролей синхронизируют ваши пароли с облаком для легкого доступа со всех ваших устройств и их безопасности в случае потери устройства.

### Bitwarden

<div class="admonition recommendation" markdown>

![Bitwarden logo](assets/img/password-management/bitwarden.svg){ align=right }

**Bitwarden** is a free and open-source password and passkey manager. Он направлен на решение проблем управления паролями для отдельных лиц, команд и организаций. Bitwarden - одно из лучших и самых безопасных решений для хранения всех ваших логинов и паролей с удобной синхронизацией данных между всеми вашими устройствами.

[:octicons-home-16: Homepage](https://bitwarden.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://bitwarden.com/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1137397744)
- [:simple-github: GitHub](https://github.com/bitwarden/mobile/releases)
- [:fontawesome-brands-windows: Windows](https://bitwarden.com/download)
- [:simple-linux: Linux](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/bitwarden-free-password-m/nngceckbapebfimnlniiiahkandclblb)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)
- [:simple-safari: Safari](https://apps.apple.com/us/app/bitwarden/id1352778147)

</details>

</div>

Bitwarden uses [PBKDF2](https://bitwarden.com/help/kdf-algorithms/#pbkdf2) as its key derivation function (KDF) algorithm by default. It also offers [Argon2](https://bitwarden.com/help/kdf-algorithms/#argon2id), which is more secure, as an alternative. You can change your account's KDF algorithm in the web vault.

- [x] Select **Settings > Security > Keys > KDF algorithm > Argon2id**

Bitwarden also features [Bitwarden Send](https://bitwarden.com/products/send), which allows you to share text and files securely with [end-to-end encryption](https://bitwarden.com/help/send-encryption). Отправленные через Bitwarden Send данные можно защитить [паролем](https://bitwarden.com/help/send-privacy/#send-passwords). Bitwarden Send также имеет функцию [автоматического удаления данных](https://bitwarden.com/help/send-lifespan).

Чтобы иметь возможность обмениваться файлами, вам необходима [Премиум-подписка](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans). Бесплатный план позволяет обмениваться только текстом.

Bitwarden's server-side code is [open source](https://github.com/bitwarden/server), so if you don't want to use the Bitwarden cloud, you can easily host your own Bitwarden sync server.

**Vaultwarden** is an alternative implementation of Bitwarden's sync server written in Rust and compatible with official Bitwarden clients, perfect for self-hosted deployment where running the resource-heavy official service might not be ideal. Если вы хотите самостоятельно развернуть Bitwarden на своем сервере, скорее всего, вам стоит использовать Vaultwarden вместо официального сервера Bitwarden.

[:octicons-repo-16: Репозиторий Vaultwarden](https://github.com/dani-garcia/vaultwarden ""){.md-button} [:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title=Документация}
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title=Поддержать }

### Proton Pass

<div class="admonition recommendation" markdown>

![Proton Pass logo](assets/img/password-management/protonpass.svg){ align=right }

**Proton Pass** is an open-source, end-to-end encrypted password manager developed by Proton, the team behind [Proton Mail](email.md#proton-mail). It securely stores your login credentials, generates unique email aliases, and supports and stores passkeys.

[:octicons-home-16: Homepage](https://proton.me/pass){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/pass/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/pass){ .card-link title="Documentation"}
[:octicons-code-16:](https://github.com/protonpass){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=proton.android.pass)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/proton-pass-password-manager/id6443490629)
- [:fontawesome-brands-windows: Windows](https://proton.me/pass/download)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/proton-pass)
- [:simple-googlechrome: Chrome](https://chromewebstore.google.com/detail/proton-pass-free-password/ghmbeldphafepmbegfdlkpapadhbakde)
- [:fontawesome-brands-edge: Edge](https://chromewebstore.google.com/detail/proton-pass-free-password/ghmbeldphafepmbegfdlkpapadhbakde)
- [:octicons-browser-16: Web](https://pass.proton.me)

</details>

</div>

With the acquisition of SimpleLogin in April 2022, Proton has offered a "hide-my-email" feature that lets you create 10 aliases (free plan) or unlimited aliases (paid plans).

Proton Pass currently doesn't have any "master password" functionality, which means that your vault is protected with the password for your Proton account and any of their supported [two factor authentication](basics/multi-factor-authentication.md) methods.

The Proton Pass mobile apps and browser extension underwent an audit performed by Cure53 throughout May and June of 2023. The security analysis company concluded:

> Proton Pass apps and components leave a rather positive impression in terms of security.

All issues were addressed and fixed shortly after the [report](https://res.cloudinary.com/dbulfrlrz/images/v1707561557/wp-pme/Cure53-proton-pass-20230717/Cure53-proton-pass-20230717.pdf).

### 1Password

<div class="admonition recommendation" markdown>

![1Password logo](assets/img/password-management/1password.svg){ align=right }

**1Password** is a password manager with a strong focus on security and ease-of-use, which allows you to store passwords, passkeys, credit cards, software licenses, and any other sensitive information in a secure digital vault. Your vault is hosted on 1Password's servers for a [monthly fee](https://1password.com/sign-up). 1Password is [audited](https://support.1password.com/security-assessments) on a regular basis and provides exceptional customer support. 1Password имеет закрытый исходный код, но безопасность продукта подробно описана в их [технической документации по безопасности](https://1passwordstatic.com/files/security/1password-white-paper.pdf).

[:octicons-home-16: Homepage](https://1password.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://1password.com/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.1password.com){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750)
- [:fontawesome-brands-windows: Windows](https://1password.com/downloads/windows)
- [:simple-apple: macOS](https://1password.com/downloads/mac)
- [:simple-linux: Linux](https://1password.com/downloads/linux)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/1password-x-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/1password-%E2%80%93-password-mana/aeblfdkhhhdcdjpifhhbdiojplfjncoa)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/dppgmdbiimibapkepcbdbmkaabgiofem)
- [:simple-safari: Safari](https://apps.apple.com/us/app/1password-for-safari/id1569813296)
- [:octicons-browser-16: Web](https://my.1password.com/signin)

</details>

</div>

Traditionally, 1Password has offered the best password manager user experience for people using macOS and iOS; however, it has now achieved feature-parity across all platforms. 1Password's clients boast many features geared towards families and less technical people, such as an intuitive UI for ease of use and navigation, as well as advanced functionality. Notably, nearly every feature of 1Password is available within its native mobile or desktop clients.

Ваше хранилище 1Password защищено одновременно мастер-паролем и случайным 34-символьным ключом безопасности для шифрования данных на серверах. Этот ключ добавляет вашим данным дополнительную защиту: они зашифрованы с высокой энтропией независимо от безопасности вашего мастер-пароля. Многие другие решения для управления паролями полностью полагаются на безопасность мастер-пароля для защиты ваших данных.

### Psono

<div class="admonition recommendation" markdown>

![Логотип Psono](assets/img/password-management/psono.svg){ align=right }

**Psono** - это свободный менеджер паролей с открытым исходным кодом из Германии, ориентированный на управление паролями для команд. Psono поддерживает безопасный обмен паролями, файлами, ссылками и электронной почтой. Вся секретная информация защищена мастер-паролем.

[:octicons-home-16: Homepage](https://psono.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://doc.psono.com){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.com/psono){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.psono.psono)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1545581224)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/psonopw-password-manager/eljmjmgjkbmpmfljlmklcfineebidmlo)
- [:simple-docker: Docker Hub](https://hub.docker.com/r/psono/psono-client)

</details>

</div>

Psono предоставляет подробную документацию по своему продукту. Веб-клиент для Psono может быть развернут самостоятельно; в качестве альтернативы вы можете приобрести полную версию Community Edition или Enterprise Edition с дополнительными возможностями.

In April 2024, Psono added [support for passkeys](https://psono.com/blog/psono-introduces-passkeys) for the browser extension only.

### Критерии

**Обратите внимание, что у нас нет связей ни с одним из проектов, которые мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md)мы разработали четкий набор требований, позволяющий нам давать объективные рекомендации. Мы рекомендуем вам ознакомиться с этим списком, прежде чем выбрать программу, и провести самостоятельное исследование, чтобы убедиться, что это правильный выбор для вас.

#### Минимальные требования к сервисам

- Должны использовать сильное, современное/стандартизированное E2EE.
- Должны иметь тщательно документированные методы шифрования и обеспечения безопасности.
- Должен иметь опубликованный аудит от авторитетной, независимой третьей стороны.
- Вся телеметрия, не критичная для работы сервиса, должна быть необязательной.
- Не должны собирать больше ПД, чем необходимо для проведения оплаты.

#### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Телеметрия должна собираться по желанию (отключена по умолчанию) или не собираться вообще.
- Should be open source and reasonably self-hostable.

## Локальные сервисы

Эти программы позволяют управлять зашифрованной базой паролей локально.

### KeePassXC

<div class="admonition recommendation" markdown>

![KeePassXC logo](assets/img/password-management/keepassxc.svg){ align=right }

**KeePassXC** is a community fork of KeePassX, a native cross-platform port of KeePass Password Safe, with the goal of extending and improving it with new features and bugfixes to provide a feature-rich, cross-platform, and modern open-source password manager.

[:octicons-home-16: Homepage](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://keepassxc.org/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassxc.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://keepassxc.org/download/#windows)
- [:simple-apple: macOS](https://keepassxc.org/download/#mac)
- [:simple-linux: Linux](https://keepassxc.org/download/#linux)
- [:simple-flathub: Flatpak](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/keepassxc-browser/oboonakemofpalcgghocfoadofidjkkk)

</details>

</div>

KeePassXC хранит экспортированные данные в виде [CSV](https://ru.wikipedia.org/wiki/CSV) файлов. При импортировании этого файла в другой менеджер паролей, вы можете потерять часть данных. Мы советуем вам проверять каждую запись вручную.

### KeePassDX (Android)

<div class="admonition recommendation" markdown>

![KeePassDX logo](assets/img/password-management/keepassdx.svg){ align=right }

**KeePassDX** is a lightweight password manager for Android; it allows for editing encrypted data in a single file in KeePass format and can fill in forms in a secure way. The [pro version](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) of the app allows you to unlock cosmetic content and non-standard protocol features, but more importantly, it helps and encourages development.

[:octicons-home-16: Homepage](https://keepassdx.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassdx.com/#donation){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
- [:simple-github: GitHub](https://github.com/Kunzisoft/KeePassDX/releases)

</details>

</div>

### Strongbox (iOS и macOS)

<div class="admonition recommendation" markdown>

![Strongbox logo](assets/img/password-management/strongbox.svg){ align=right }

**Strongbox** is a native password manager for iOS and macOS. Он поддерживает форматы KeePass и Password Safe, поэтому может быть использован совместно с другими менеджерами паролей, например KeePassXC, на устройствах не от Apple. By employing a [freemium model](https://strongboxsafe.com/pricing), Strongbox offers most features under its free tier, with more convenience-oriented [features](https://strongboxsafe.com/comparison)—such as biometric authentication—locked behind a subscription or perpetual license.

[:octicons-home-16: Homepage](https://strongboxsafe.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://strongboxsafe.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://strongboxsafe.com/getting-started){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/strongbox-password-safe/Strongbox){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/strongbox-password-safe/Strongbox#supporting-development){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id897283731)

</details>

</div>

Additionally, there is an offline-only version offered: [Strongbox Zero](https://apps.apple.com/app/id1581589638). Эта версия урезана, чтобы уменьшить площадь атаки.

### gopass (CLI)

<div class="admonition recommendation" markdown>

![gopass logo](assets/img/password-management/gopass.svg){ align=right }

**gopass** is a minimal password manager for the command line written in Go. It can be used within scripting applications and works on all major desktop and server operating systems (Linux, macOS, BSD, Windows).

[:octicons-home-16: Homepage](https://gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://gopass.pw/#install-windows)
- [:simple-apple: macOS](https://gopass.pw/#install-macos)
- [:simple-linux: Linux](https://gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://gopass.pw/#install-bsd)

</details>

</div>

<!-- markdownlint-disable-next-line -->
### Критерии

**Обратите внимание, что у нас нет связей ни с одним из проектов, которые мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md)мы разработали четкий набор требований, позволяющий нам давать объективные рекомендации. Мы рекомендуем вам ознакомиться с этим списком, прежде чем выбрать программу, и провести самостоятельное исследование, чтобы убедиться, что это правильный выбор для вас.

- Программа должна быть кроссплатформенной.
