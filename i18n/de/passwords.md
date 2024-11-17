---
meta_title: "Die besten Passwort-Manager zum Schutz deiner Privatsphäre und Sicherheit - Privacy Guides"
title: "Passwort-Manager"
icon: material/form-textbox-password
description: Mit Passwortmanagern kannst du Passwörter und andere Anmeldeinformationen sicher speichern und verwalten.
cover: passwords.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Empfehlungen für Passwort-Manager
    url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Bitwarden
    image: /assets/img/password-management/bitwarden.svg
    url: https://bitwarden.com/de-de/
    sameAs: https://en.wikipedia.org/wiki/Bitwarden
    applicationCategory: Passwort-Manager
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
    url: https://1password.com/de
    sameAs: https://de.wikipedia.org/wiki/1Password
    applicationCategory: Passwort-Manager
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
    url: https://proton.me/de/pass
    applicationCategory: Passwort-Manager
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
    url: https://psono.com/de
    applicationCategory: Passwort-Manager
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
    applicationCategory: Passwort-Manager
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
    applicationCategory: Passwort-Manager
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
    url: https://strongboxsafe.com/de/
    applicationCategory: Passwort-Manager
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
    applicationCategory: Passwort-Manager
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

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Passive Angriffe](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Diensteanbieter](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

**Passwort-Manager** ermöglichen die sichere Speicherung und Verwaltung von Passwörtern und anderen Anmeldeinformationen unter Verwendung eines Master-Passworts.

[Einführung in Passwörter :material-arrow-right-drop-circle:](./basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

Integrierte Passwortmanager in Software wie Browsern und Betriebssystemen sind manchmal nicht so gut wie spezielle Passwortmanager-Software. The advantage of a built-in password manager is good integration with the software, but it can often be very simple and lack privacy and security features that standalone offerings have.

Der Passwort-Manager in Microsoft Edge bietet zum Beispiel überhaupt kein E2EE. Googles Passwortmanager hat [optional](https://support.google.com/accounts/answer/11350823) E2EE, und [Apples](https://support.apple.com/HT202303) bietet standardmäßig E2EE.

</div>

## Cloud-basiert

Diese Passwort-Manager synchronisieren deine Passwörter mit einem Cloud-Server, damit du von all deinen Geräten aus leicht darauf zugreifen kannst und vor Geräteverlust geschützt bist.

### Bitwarden

<div class="admonition recommendation" markdown>

![Bitwarden-Logo](assets/img/passwort-management/bitwarden.svg){ align=right }

**Bitwarden** ist ein kostenloser und quelloffener Passwort- und Passkey-Manager. Es zielt darauf ab, Passwortmanagementprobleme für Einzelpersonen, Teams und Unternehmen zu lösen. Bitwarden ist eine der besten und sichersten Lösungen, um alle deine Logins und Passwörter zu speichern und sie bequem zwischen all deinen Geräten zu synchronisieren.

[:octicons-home-16: Homepage](https://bitwarden.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://bitwarden.com/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1137397744)
- [:simple-github: GitHub](https://github.com/bitwarden/android/releases)
- [:fontawesome-brands-windows: Windows](https://bitwarden.com/download)
- [:simple-linux: Linux](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/bitwarden-free-password-m/nngceckbapebfimnlniiiahkandclblb)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)
- [:simple-safari: Safari](https://apps.apple.com/us/app/bitwarden/id1352778147)

</details>

</div>

Bitwarden verwendet standardmäßig [PBKDF2](https://bitwarden.com/help/kdf-algorithms/#pbkdf2) als Schlüsselableitungsalgorithmus (KDF). Als Alternative bietet es auch das sicherere [Argon2](https://bitwarden.com/help/kdf-algorithms/#argon2id) an. Du kannst den KDF-Algorithmus deines Kontos im Web-Tresor ändern.

- [x] Wähle **Einstellungen > Sicherheit > Schlüssel > KDF-Algorithmus > Argon2id**

Der serverseitige Code von Bitwarden ist [quelloffen](https://github.com/bitwarden/server). Wenn du also nicht die Bitwarden-Cloud nutzen möchtest, kannst du problemlos deinen eigenen Bitwarden-Synchronisierungsserver hosten.

**Vaultwarden** ist eine alternative Implementierung des Sync-Servers von Bitwarden, die in Rust geschrieben wurde und mit den offiziellen Bitwarden-Clients kompatibel ist. Sie eignet sich perfekt für den selbstgehosteten Einsatz, wenn der ressourcenintensive offizielle Dienst nicht ideal ist. Wenn du Bitwarden auf deinem eigenen Server hosten willst, wirst du mit ziemlicher Sicherheit lieber Vaultwarden als den offiziellen Servercode von Bitwarden verwenden wollen.

[:octicons-repo-16: Vaultwarden Repository](https://github.com/dani-garcia/vaultwarden ""){.md-button} [:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title="Contribute" }

### Proton Pass

<div class="admonition recommendation" markdown>

![Proton Pass Logo](assets/img/password-management/protonpass.svg){ align=right }

**Proton Pass** ist ein quelloffener, E2EE Passwort-Manager, der von Proton entwickelt wurde, dem Team hinter [Proton Mail](email.md#proton-mail). Es speichert deine Anmeldedaten sicher, erzeugt eindeutige E-Mail-Aliase und unterstützt und speichert Passkeys.

[:octicons-home-16: Homepage](https://proton.me/pass){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/pass/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/pass){ .card-link title="Documentation" }
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

Mit der Übernahme von SimpleLogin im April 2022 bietet Proton eine "Hide-My-Email"-Funktion an, mit der du 10 Aliase (kostenloser Plan) oder unbegrenzte Aliase (kostenpflichtige Pläne) erstellen kannst.

Die mobilen Anwendungen und die Browsererweiterung von Proton Pass wurden im Mai und Juni 2023 von Cure53 geprüft. Das Sicherheitsanalyseunternehmen kam zu dem Schluss:

> Proton Pass Apps und Komponenten hinterlassen einen recht positiven Eindruck in Sachen Sicherheit.

Alle Probleme wurden kurz nach dem [Bericht](https://res.cloudinary.com/dbulfrlrz/images/v1707561557/wp-pme/Cure53-proton-pass-20230717/Cure53-proton-pass-20230717.pdf) angegangen und behoben.

### 1Password

<div class="admonition recommendation" markdown>

![1Password logo](assets/img/password-management/1password.svg){ align=right }

**1Password** is a password manager with a strong focus on security and ease-of-use that allows you to store passwords, passkeys, credit cards, software licenses, and any other sensitive information in a secure digital vault. Dein Tresor wird auf den Servern von 1Password gegen eine [monatliche Gebühr] (https://1password.com/sign-up) gehostet. 1Password wird regelmäßig [geprüft] (https://support.1password.com/security-assessments) und bietet einen hervorragenden Kundensupport. 1Password ist ein Closed-Source-Produkt; die Sicherheit des Produkts ist jedoch in ihrem [Sicherheits-Whitepaper](https://1passwordstatic.com/files/security/1password-white-paper.pdf) ausführlich dokumentiert.

[:octicons-home-16: Homepage](https://1password.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://1password.com/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.1password.com){ .card-link title="Documentation" }

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

Traditionally, 1Password has offered the best password manager user experience for people using macOS and iOS; however, it has now achieved feature parity across all platforms. Die Clients von 1Password verfügen über viele Funktionen, die sich an Familien und technisch weniger versierte Personen richten, wie z. B. eine intuitive Benutzeroberfläche für einfache Bedienung und Navigation sowie erweiterte Funktionen. Nahezu jede Funktion von 1Password ist in den nativen mobilen oder Desktop-Clients verfügbar.

Dein 1Password-Tresor ist sowohl mit deinem Master-Passwort als auch mit einem zufälligen 34-Zeichen-Sicherheitsschlüssel zur Verschlüsselung deiner Daten auf den Servern von 1Password gesichert. Dieser Sicherheitsschlüssel bietet einen zusätzlichen Schutz für deine Daten, da deine Daten unabhängig von deinem Master-Kennwort mit hoher Entropie gesichert sind. Viele andere Passwortmanager-Lösungen verlassen sich bei der Sicherung deiner Daten ausschließlich auf die Stärke deines Master-Passworts.

### Psono

<div class="admonition recommendation" markdown>

![Psono-Logo](assets/img/password-management/psono.svg){ align=right }

**Psono** ist ein freier und quelloffener Passwort-Manager aus Deutschland, der sich auf die Passwortverwaltung für Teams konzentriert. Psono unterstützt den sicheren Austausch von Passwörtern, Dateien, Lesezeichen und E-Mails. Alle Geheimnisse sind durch ein Master-Passwort geschützt.

[:octicons-home-16: Homepage](https://psono.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://doc.psono.com){ .card-link title="Documentation" }
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

Psono bietet eine umfangreiche Dokumentation für sein Produkt. Der Web-Client für Psono kann selbst gehostet werden; alternativ kannst du die vollständige Community Edition oder die Enterprise Edition mit zusätzlichen Funktionen wählen.

Im April 2024 fügte Psono [Unterstützung für Passkeys](https://psono.com/blog/psono-introduces-passkeys) nur für die Browsererweiterung hinzu.

### Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

#### Mindestanforderungen

- Muss starke, standardbasierte/moderne E2EE verwenden.
- Muss gründlich dokumentierte Verschlüsselungs- und Sicherheitspraktiken haben.
- Must have a published audit from a reputable, independent third party.
- Alle nicht wesentlichen Telemetriedaten müssen optional sein.
- Es dürfen nicht mehr personenbezogene Daten erhoben werden, als für die Rechnungsstellung erforderlich sind.

#### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Merkmale, aber diejenigen, die sie enthalten, werden möglicherweise höher eingestuft als andere auf dieser Seite.

- Telemetrie sollte auf Wunsch erfolgen (standardmäßig deaktiviert) oder überhaupt nicht erfasst werden.
- Es sollte quelloffen sein und sich in einem angemessenen Rahmen selbst hosten lassen.

## Lokaler Speicher

Mit diesen Optionen kannst du eine verschlüsselte Kennwortdatenbank lokal verwalten.

### KeePassXC

<div class="admonition recommendation" markdown>

![KeePassXC-Logo](assets/img/password-management/keepassxc.svg){ align=right }

**KeePassXC** ist ein Community-Fork von KeePassX, einer nativen, plattformübergreifenden Portierung von KeePass Password Safe, mit dem Ziel, es mit neuen Funktionen und Fehlerbehebungen zu erweitern und zu verbessern, um einen funktionsreichen, plattformübergreifenden und modernen Open-Source-Passwortmanager anzubieten.

[:octicons-home-16: Homepage](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://keepassxc.org/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassxc.org/donate){ .card-link title="Contribute" }

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

KeePassXC speichert seine Exportdaten als [CSV-Dateien](https://en.wikipedia.org/wiki/Comma-separated_values). You may encounter data loss if you import this file into another password manager. Wir empfehlen dir, jeden Datensatz manuell zu überprüfen.

### KeePassDX (Android)

<div class="admonition recommendation" markdown>

![KeePassDX-Logo](assets/img/password-management/keepassdx.svg){ align=right }

**KeePassDX** ist ein leichtgewichtiger Passwort-Manager für Android; er ermöglicht die Bearbeitung verschlüsselter Daten in einer einzigen Datei im KeePass-Format und kann Formulare auf sichere Weise ausfüllen. Die [Pro-Version](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) der App ermöglicht es dir, kosmetische Inhalte und nicht standardmäßige Protokollfunktionen freizuschalten, aber noch wichtiger ist, dass sie die Entwicklung unterstützt und fördert.

[:octicons-home-16: Homepage](https://keepassdx.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassdx.com/#donation){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
- [:simple-github: GitHub](https://github.com/Kunzisoft/KeePassDX/releases)

</details>

</div>

### Strongbox (iOS & macOS)

<div class="admonition recommendation" markdown>

![Strongbox-Logo](assets/img/password-management/strongbox.svg){ align=right }

**Strongbox** ist ein nativer Passwortmanager für iOS und macOS. Strongbox unterstützt sowohl das KeePass- als auch das Password Safe-Format und kann zusammen mit anderen Passwortmanagern wie KeePassXC auf Nicht-Apple-Plattformen verwendet werden. Durch den Einsatz eines [Freemium-Modells](https://strongboxsafe.com/pricing) bietet Strongbox die meisten Funktionen im Rahmen seines kostenlosen Angebots an, wobei komfortablere [Funktionen](https://strongboxsafe.com/comparison) - wie biometrische Authentifizierung - hinter einem Abonnement oder einer unbefristeten Lizenz verschlossen sind.

[:octicons-home-16: Homepage](https://strongboxsafe.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://strongboxsafe.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://strongboxsafe.com/getting-started){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/strongbox-password-safe/Strongbox){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/strongbox-password-safe/Strongbox#supporting-development){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id897283731)

</details>

</div>

Additionally, Strongbox offers an offline-only version: [Strongbox Zero](https://apps.apple.com/app/id1581589638). Diese Version ist abgespeckt, um die Angriffsfläche zu verringern.

### gopass (CLI)

<div class="admonition recommendation" markdown>

![gopass Logo](assets/img/password-management/gopass.svg){ align=right }

**gopass** ist ein minimaler, in Go geschriebener Passwortmanager für die Kommandozeile. It can be used within scripting applications and works on all major desktop and server operating systems.

[:octicons-home-16: Homepage](https://gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://gopass.pw/#install-windows)
- [:simple-apple: macOS](https://gopass.pw/#install-macos)
- [:simple-linux: Linux](https://gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://gopass.pw/#install-bsd)

</details>

</div>

### Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

- Muss plattformübergreifend sein.
