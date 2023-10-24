---
meta_title: "Os Melhores Gerenciadores de Senhas para Proteger sua Privacidade e Segurança — Privacy Guides"
title: "Gerenciadores de Senhas"
icon: material/form-textbox-password
description: Gerenciadores de senhas permitem que você armazene e gerencie com segurança senhas e outras credenciais.
cover: passwords.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Gerenciadores de Senhas Recomendados
    url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Bitwarden
    image: /assets/img/password-management/bitwarden.svg
    url: https://bitwarden.com
    sameAs: https://en.wikipedia.org/wiki/Bitwarden
    applicationCategory: Gerenciador de Senhas
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
    applicationCategory: Gerenciador de Senhas
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
    name: Psono
    image: /assets/img/password-management/psono.svg
    url: https://psono.com
    applicationCategory: Gerenciador de Senhas
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
    url: https://keepassxc.org/
    sameAs: https://en.wikipedia.org/wiki/KeePassXC
    applicationCategory: Gerenciador de Senhas
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
    url: https://www.keepassdx.com/
    applicationCategory: Gerenciador de Senhas
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
    url: https://strongboxsafe.com/
    applicationCategory: Gerenciador de Senhas
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
    url: https://www.gopass.pw/
    applicationCategory: Gerenciador de Senhas
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

Os gerenciadores de senhas permitem que você armazene e gerencie com segurança senhas e outras credenciais com o uso de uma senha mestra.

[Introdução às Senhas :material-arrow-right-drop-circle:](./basics/passwords-overview.md)

!!! info

    Gerenciadores de senhas que vêm de fábrica em aplicativos como navegadores e sistemas operacionais às vezes não são tão bons quanto um aplicativo exclusivo para gerenciamento de senhas. A vantagem de um gerenciador de senhas interno é a boa integração com o programa, mas, em geral, ele pode ser muito simples e não ter os recursos de privacidade e segurança que as ofertas autônomas têm.
    
    Por exemplo, o gerenciador de senhas do Microsoft Edge não oferece em absoluto o E2EE. O gerenciador de senhas do Google tem [optional](https://support.google.com/accounts/answer/11350823) E2EE, e [Apple's](https://support.apple.com/en-us/HT202303) oferece E2EE por padrão.

## Baseado na nuvem

Esses gerenciadores de senhas sincronizam suas senhas com um servidor em nuvem para facilitar o acesso a partir de todos os seus dispositivos e proteger contra a perda de dispositivos.

### Bitwarden

!!! recommendation

    ![Bitwarden logo](assets/img/password-management/bitwarden.svg){ align=right }
    
    **Bitwarden** is a free and open-source password manager. It aims to solve password management problems for individuals, teams, and business organizations. Bitwarden is among the best and safest solutions to store all of your logins and passwords while conveniently keeping them synced between all of your devices.
    
    [:octicons-home-16: Homepage](https://bitwarden.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://bitwarden.com/help/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
        - [:simple-appstore: App Store](https://apps.apple.com/app/bitwarden-password-manager/id1137397744)
        - [:simple-github: GitHub](https://github.com/bitwarden/mobile/releases)
        - [:simple-windows11: Windows](https://bitwarden.com/download)
        - [:simple-linux: Linux](https://bitwarden.com/download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/bitwarden-free-password-m/nngceckbapebfimnlniiiahkandclblb)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)

Bitwarden also features [Bitwarden Send](https://bitwarden.com/products/send/), which allows you to share text and files securely with [end-to-end encryption](https://bitwarden.com/help/send-encryption). A [password](https://bitwarden.com/help/send-privacy/#send-passwords) can be required along with the send link. Bitwarden Send also features [automatic deletion](https://bitwarden.com/help/send-lifespan).

You need the [Premium Plan](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) to be able to share files. The free plan only allows text sharing.

Bitwarden's server-side code is [open source](https://github.com/bitwarden/server), so if you don't want to use the Bitwarden cloud, you can easily host your own Bitwarden sync server.

**Vaultwarden** é uma implementação alternativa do servidor de sincronização do Bitwarden, escrito em Rust e compatível com os clientes oficiais do Bitwarden, perfeito para a implementação auto-hospedada em que a execução do serviço oficial com muitos recursos pode não ser ideal. Se você deseja hospedar o Bitwarden em seu próprio servidor, é quase certo que queira usar o Vaultwarden em vez do código de servidor oficial do Bitwarden.

[:octicons-repo-16: Vaultwarden Repository](https://github.com/dani-garcia/vaultwarden ""){.md-button} [:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title=Contribute }

### 1Password

!!! recommendation

    ![1Password logo](assets/img/password-management/1password.svg){ align=right }
    
    **1Password** is a password manager with a strong focus on security and ease-of-use, which allows you to store passwords, credit cards, software licenses, and any other sensitive information in a secure digital vault. Your vault is hosted on 1Password's servers for a [monthly fee](https://1password.com/sign-up/). 1Password is [audited](https://support.1password.com/security-assessments/) on a regular basis and provides exceptional customer support. 1Password is closed source; however, the security of the product is thoroughly documented in their [security white paper](https://1passwordstatic.com/files/security/1password-white-paper.pdf).
    
    [:octicons-home-16: Homepage](https://1password.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://1password.com/legal/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.1password.com/){ .card-link title=Documentation}
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750?mt=8)
        - [:simple-windows11: Windows](https://1password.com/downloads/windows/)
        - [:simple-apple: macOS](https://1password.com/downloads/mac/)
        - [:simple-linux: Linux](https://1password.com/downloads/linux/)

Tradicionalmente, o **1Password** oferece a melhor experiência de usuário de gerenciador de senhas para pessoas que usam macOS e iOS; no entanto, agora ele atingiu a igualdade de recursos em todas as plataformas. Ele apresenta muitos recursos voltados para famílias e pessoas menos técnicas, bem como funcionalidades avançadas.

Seu cofre do 1Password é protegido com sua senha mestra e uma chave de segurança aleatória de 34 caracteres para criptografar seus dados nos servidores. Essa chave de segurança adiciona uma camada de proteção aos seus dados porque eles são protegidos com alta entropia, independentemente da sua senha mestra. Muitas outras soluções de gerenciador de senhas dependem totalmente da força de sua senha mestra para proteger seus dados.

Uma vantagem do 1Password sobre o Bitwarden é seu suporte de primeira classe dos clientes nativos. Enquanto o Bitwarden reserva muitas funções, especialmente os recursos de gerenciamento de contas, para sua interface de cofre do site, o 1Password disponibiliza quase todos os recursos em seus clientes nativos para celular ou desktop. Os clientes do 1Password também têm uma interface de usuário mais intuitiva, o que os torna mais fáceis de usar e navegar.

### Psono

!!! recommendation

    ![Psono logo](assets/img/password-management/psono.svg){ align=right }
    
    **Psono** is a free and open-source password manager from Germany, with a focus on password management for teams. Psono supports secure sharing of passwords, files, bookmarks, and emails. All secrets are protected by a master password.
    
    [:octicons-home-16: Homepage](https://psono.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://doc.psono.com){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.com/psono){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.psono.psono)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/psono-password-manager/id1545581224)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/psonopw-password-manager/eljmjmgjkbmpmfljlmklcfineebidmlo)
        - [:simple-docker: Docker Hub](https://hub.docker.com/r/psono/psono-client)

Psono fornece uma extensa documentação para seu produto. The web-client for Psono can be self-hosted; alternatively, you can choose the full Community Edition or the Enterprise Edition with additional features.

### Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! example "This section is new"

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.

#### Minimum Requirements

- Must utilize strong, standards-based/modern E2EE.
- Deve ter práticas de criptografia e segurança totalmente documentadas.
- Deve ter uma auditoria publicada por um terceiro independente e de boa reputação.
- Toda telemetria não essencial deve ser opcional.
- Não deve coletar mais PII (dados pessoais identificáveis) do que o necessário para fins de faturamento.

#### Melhor Caso

Nosso critério de melhor caso representa o que gostaríamos de ver em um projeto perfeito nessa categoria. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Telemetry should be opt-in (disabled by default) or not collected at all.
- Should be open source and reasonably self-hostable.

## Local Storage

These options allow you to manage an encrypted password database locally.

### KeePassXC

!!! recommendation

    ![KeePassXC logo](assets/img/password-management/keepassxc.svg){ align=right }
    
    **KeePassXC** is a community fork of KeePassX, a native cross-platform port of KeePass Password Safe, with the goal to extend and improve it with new features and bugfixes to provide a feature-rich, cross-platform and modern open-source password manager.
    
    [:octicons-home-16: Homepage](https://keepassxc.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://keepassxc.org/docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://keepassxc.org/donate/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://keepassxc.org/download/#windows)
        - [:simple-apple: macOS](https://keepassxc.org/download/#mac)
        - [:simple-linux: Linux](https://keepassxc.org/download/#linux)
        - [:simple-flathub: Flatpak](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/keepassxc-browser/oboonakemofpalcgghocfoadofidjkkk)

KeePassXC stores its export data as [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) files. This may mean data loss if you import this file into another password manager. We advise you check each record manually.

### KeePassDX (Android)

!!! recommendation

    ![KeePassDX logo](assets/img/password-management/keepassdx.svg){ align=right }
    
    **KeePassDX** is a lightweight password manager for Android, allows editing encrypted data in a single file in KeePass format and can fill in the forms in a secure way. [Contributor Pro](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) allows unlocking cosmetic content and non-standard protocol features, but more importantly, it helps and encourages development.
    
    [:octicons-home-16: Homepage](https://www.keepassdx.com){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.keepassdx.com/#donation){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
        - [:simple-github: GitHub](https://github.com/Kunzisoft/KeePassDX/releases)

### Strongbox (iOS & macOS)

!!! recommendation

    ![Strongbox logo](assets/img/password-management/strongbox.svg){ align=right }
    
    **Strongbox** is a native, open-source password manager for iOS and macOS. Supporting both KeePass and Password Safe formats, Strongbox can be used in tandem with other password managers, like KeePassXC, on non-Apple platforms. By employing a [freemium model](https://strongboxsafe.com/pricing/), Strongbox offers most features under its free tier with more convenience-oriented [features](https://strongboxsafe.com/comparison/)—such as biometric authentication—locked behind a subscription or perpetual license.
    
    [:octicons-home-16: Homepage](https://strongboxsafe.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://strongboxsafe.com/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://strongboxsafe.com/getting-started/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/strongbox-password-safe/Strongbox){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://github.com/strongbox-password-safe/Strongbox#supporting-development){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/strongbox-keepass-pwsafe/id897283731)

Additionally, there is an offline-only version offered: [Strongbox Zero](https://apps.apple.com/app/strongbox-keepass-pwsafe/id1581589638). This version is stripped down in an attempt to reduce attack surface.

### Command-line

These products are minimal password managers that can be used within scripting applications.

#### gopass

!!! recommendation

    ![gopass logo](assets/img/password-management/gopass.svg){ align=right }
    
    **gopass** is a password manager for the command line written in Go. It works on all major desktop and server operating systems (Linux, macOS, BSD, Windows).
    
    [:octicons-home-16: Homepage](https://www.gopass.pw){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://www.gopass.pw/#install-windows)
        - [:simple-apple: macOS](https://www.gopass.pw/#install-macos)
        - [:simple-linux: Linux](https://www.gopass.pw/#install-linux)
        - [:simple-freebsd: FreeBSD](https://www.gopass.pw/#install-bsd)

### Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! example "This section is new"

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.

- Must be cross-platform.
