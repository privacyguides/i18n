---
meta_title: "The Best Password Managers to Protect Your Privacy and Security - Privacy Guides"
title: "Wachtwoord managers"
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
    applicationCategory: Wachtwoord Manager
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
    applicationCategory: Wachtwoord Manager
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
    applicationCategory: Wachtwoord Manager
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
    applicationCategory: Wachtwoord Manager
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
    applicationCategory: Wachtwoord Manager
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
    applicationCategory: Wachtwoord Manager
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
    applicationCategory: Wachtwoord Manager
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

Met wachtwoord Managers kunt je wachtwoorden en andere geheimen veilig opslaan en beheren met behulp van een hoofdwachtwoord.

[Uitleg over wachtwoorden :material-arrow-right-drop-circle:](./basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

Ingebouwde wachtwoord managers in software zoals browsers en besturingssystemen zijn soms niet zo goed als speciale software voor wachtwoordbeheer. Het voordeel van een ingebouwde wachtwoord manager is een goede integratie met de software, maar het kan vaak erg eenvoudig zijn en mist privacy- en beveiligingsfuncties die aanbiedingen van derden wel hebben.

De wachtwoord manager in Microsoft Edge biedt bijvoorbeeld helemaal geen E2EE. Google's password manager has [optional](https://support.google.com/accounts/answer/11350823) E2EE, and [Apple's](https://support.apple.com/HT202303) offers E2EE by default.

</div>

## Cloud-gebaseerd

Deze wachtwoordbeheerders synchroniseren jouw wachtwoorden met een cloudserver voor gemakkelijke toegang vanaf al jouw apparaten en veiligheid tegen verlies van apparaten.

### Bitwarden

<div class="admonition recommendation" markdown>

![Bitwarden logo](assets/img/password-management/bitwarden.svg){ align=right }

**Bitwarden** is een gratis en open-source wachtwoord manager. Het is gericht op het oplossen van problemen op het gebied van wachtwoordbeheer voor individuen, teams en bedrijfsorganisaties. Bitwarden is een van de makkelijkste en veiligste oplossingen om al jouw logins en wachtwoorden op te slaan terwijl ze gemakkelijk gesynchroniseerd blijven tussen al jouw apparaten.

[:octicons-home-16: Homepage](https://bitwarden.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://bitwarden.com/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1137397744)
- [:simple-github: GitHub](https://github.com/bitwarden/mobile/releases)
- [:simple-windows11: Windows](https://bitwarden.com/download)
- [:simple-linux: Linux](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/bitwarden-free-password-m/nngceckbapebfimnlniiiahkandclblb)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)

</details>

</div>

Bitwarden also features [Bitwarden Send](https://bitwarden.com/products/send), which allows you to share text and files securely with [end-to-end encryption](https://bitwarden.com/help/send-encryption). Een [wachtwoord](https://bitwarden.com/help/send-privacy/#send-passwords) kan nodig zijn samen met de verzendlink. Bitwarden Send beschikt ook over [automatische verwijdering](https://bitwarden.com/help/send-lifespan).

U hebt het [Premium Plan](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) nodig om bestanden te kunnen delen. Het gratis plan staat alleen het delen van tekst toe.

Bitwarden's server-side code is [open source](https://github.com/bitwarden/server), so if you don't want to use the Bitwarden cloud, you can easily host your own Bitwarden sync server.

**Vaultwarden** is een alternatieve implementatie van de sync-server van Bitwarden, geschreven in Rust en compatibel met de officiële Bitwarden-clients, perfect voor zelf-hosting waar het draaien van de officiële resource-heavy service misschien niet ideaal is. Als je Bitwarden zelf wilt hosten op jouw eigen server, wil je vrijwel zeker Vaultwarden gebruiken in plaats van de officiële servercode van Bitwarden.

[:octicons-repo-16: Vaultwarden Repository](https://github.com/dani-garcia/vaultwarden ""){.md-button} [:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title=Documentatie}
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Broncode" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title=Bijdragen}

### 1Password

<div class="admonition recommendation" markdown>

![1Password logo](assets/img/password-management/1password.svg){ align=right }

**1Password** is een wachtwoordmanager met een sterke focus op veiligheid en gebruiksgemak, waarmee je wachtwoorden, creditcards, softwarelicenties en andere gevoelige informatie kunt opslaan in een veilige digitale kluis. Your vault is hosted on 1Password's servers for a [monthly fee](https://1password.com/sign-up). 1Password is [audited](https://support.1password.com/security-assessments) on a regular basis and provides exceptional customer support. 1Password is closed source; de beveiliging van het product is echter grondig gedocumenteerd in hun [security white paper](https://1passwordstatic.com/files/security/1password-white-paper.pdf).

[:octicons-home-16: Homepage](https://1password.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://1password.com/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.1password.com){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750)
- [:simple-windows11: Windows](https://1password.com/downloads/windows)
- [:simple-apple: macOS](https://1password.com/downloads/mac)
- [:simple-linux: Linux](https://1password.com/downloads/linux)

</details>

</div>

Traditioneel biedt **1Password** de beste wachtwoordmanager-gebruikerservaring voor mensen die macOS en iOS gebruiken; het ondersteunt nu echter alle functies op alle platforms. Het heeft veel functies die gericht zijn op gezinnen en minder technische mensen, maar ook geavanceerde functionaliteit.

Uw 1Password-kluis is beveiligd met zowel jouw hoofdwachtwoord als een gerandomiseerde beveiligingssleutel van 34 tekens om jouw gegevens op hun servers te versleutelen. Deze beveiligingssleutel voegt een beschermingslaag toe aan jouw gegevens omdat jouw gegevens worden beveiligd met een hoge entropie, ongeacht jouw hoofdwachtwoord. Veel andere oplossingen voor wachtwoordbeheer zijn volledig afhankelijk van de sterkte van jouw hoofdwachtwoord om jouw gegevens te beveiligen.

Een voordeel van 1Password ten opzichte van Bitwarden is de eersteklas ondersteuning voor native clients. Terwijl Bitwarden veel taken, vooral accountbeheerfuncties, naar hun webkluisinterface verwijst, maakt 1Password bijna elke functie beschikbaar binnen zijn native mobiele of desktop clients. De clients van 1Password hebben ook een meer intuïtieve UI, waardoor ze gemakkelijker te gebruiken en te navigeren zijn.

### Psono

<div class="admonition recommendation" markdown>

![Psono logo](assets/img/password-management/psono.svg){ align=right }

**Psono** is een gratis en open-source wachtwoordmanager uit Duitsland, met een focus op wachtwoordbeheer voor teams. Psono ondersteunt het veilig delen van wachtwoorden, bestanden, bladwijzers en e-mails. Alle geheimen worden beschermd door een hoofdwachtwoord.

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

Psono biedt uitgebreide documentatie voor hun product. De web-client voor Psono kunt je zelf hosten; als alternatief kunt je kiezen voor de volledige Community Edition of de Enterprise Edition met extra mogelijkheden.

### Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

#### Minimale vereisten

- Moet gebruik maken van sterke, op standaarden gebaseerde/moderne E2EE.
- Moet beschikken over grondig gedocumenteerde encryptie- en beveiligingspraktijken.
- Moet een gepubliceerde audit hebben van een gerenommeerde, onafhankelijke derde partij.
- Alle niet-essentiële telemetrie moet optioneel zijn.
- Mag niet meer PII verzamelen dan nodig is voor factureringsdoeleinden.

#### Beste geval

Onze best-case criteria geven aan wat wij zouden willen zien van het perfecte project in deze categorie. Het is mogelijk dat onze aanbevelingen geen of niet alle functies bevatten, maar degene die dat wel doen kunnen hoger gerangschikt worden dan andere op deze pagina.

- Telemetrie moet opt-in zijn (standaard uitgeschakeld) of helemaal niet worden verzameld.
- Should be open source and reasonably self-hostable.

## Lokale opslag

Met deze opties kunt je een versleutelde wachtwoorddatabase lokaal beheren.

### KeePassXC

<div class="admonition recommendation" markdown>

![KeePassXC logo](assets/img/password-management/keepassxc.svg){ align=right }

**KeePassXC** is een community fork van KeePassX, een native cross-platform port van KeePass Password Safe, met als doel het uit te breiden en te verbeteren met nieuwe functies en bugfixes om een feature-rijke, cross-platform en moderne open-source password manager te bieden.

[:octicons-home-16: Homepage](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://keepassxc.org/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassxc.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://keepassxc.org/download/#windows)
- [:simple-apple: macOS](https://keepassxc.org/download/#mac)
- [:simple-linux: Linux](https://keepassxc.org/download/#linux)
- [:simple-flathub: Flatpak](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/keepassxc-browser/oboonakemofpalcgghocfoadofidjkkk)

</details>

</div>

KeePassXC slaat zijn exportgegevens op als [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) bestanden. Dit kan gegevensverlies betekenen als je dit bestand importeert in een andere wachtwoordmanager. Wij adviseren je om elke registratie handmatig te controleren.

### KeePassDX (Android)

<div class="admonition recommendation" markdown>

![KeePassDX logo](assets/img/password-management/keepassdx.svg){ align=right }

**KeePassDX** is een lichtgewicht wachtwoordmanager voor Android, waarmee versleutelde gegevens in een enkel bestand in KeePass-formaat kunnen worden bewerkt en de formulieren op een veilige manier kunnen worden ingevuld. [Contributor Pro](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) maakt het mogelijk om cosmetische inhoud en niet-standaard protocolfuncties vrij te spelen, maar belangrijker nog, het helpt en stimuleert de ontwikkeling.

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

### Strongbox (iOS & macOS)

<div class="admonition recommendation" markdown>

![Strongbox logo](assets/img/password-management/strongbox.svg){ align=right }

**Strongbox** is een native, open-source wachtwoordmanager voor iOS en macOS. Strongbox ondersteunt zowel KeePass als Password Safe formaten en kan worden gebruikt in combinatie met andere wachtwoordmanagers, zoals KeePassXC, op niet-Apple platforms. By employing a [freemium model](https://strongboxsafe.com/pricing), Strongbox offers most features under its free tier with more convenience-oriented [features](https://strongboxsafe.com/comparison)—such as biometric authentication—locked behind a subscription or perpetual license.

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

Additionally, there is an offline-only version offered: [Strongbox Zero](https://apps.apple.com/app/id1581589638). Deze versie is uitgekleed in een poging het aanvalsoppervlak te verkleinen.

### Command-line

Deze producten zijn minimale wachtwoordmanagers die kunnen worden gebruikt binnen scriptingtoepassingen.

#### gopass

<div class="admonition recommendation" markdown>

![gopass logo](assets/img/password-management/gopass.svg){ align=right }

**gopass** is een wachtwoordmanager voor de commandoregel geschreven in Go. Het werkt op alle belangrijke desktop- en serverbesturingssystemen (Linux, macOS, BSD, Windows).

[:octicons-home-16: Homepage](https://gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://gopass.pw/#install-windows)
- [:simple-apple: macOS](https://gopass.pw/#install-macos)
- [:simple-linux: Linux](https://gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://gopass.pw/#install-bsd)

</details>

</div>

### Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

- Moet cross-platform zijn.
