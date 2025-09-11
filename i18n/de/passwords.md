---
meta_title: "Die besten Passwort-Manager zum Schutz deiner Privatsphäre und Sicherheit - Privacy Guides"
title: Passwort-Manager
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
    sameAs: https://de.wikipedia.org/wiki/KeePassXC
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
    name: Gopass
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

[Einführung in Passwörter :material-arrow-right-drop-circle:](basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

Integrierte Passwortmanager in Software wie Browsern und Betriebssystemen sind manchmal nicht so gut wie spezielle Passwortmanager-Software. Der Vorteil eines integrierten Passwortmanagers ist die gute Integration in die Software, aber er ist oft sehr einfach und verfügt nicht über die Datenschutz- und Sicherheitsfunktionen, die eigenständige Angebote bieten.

For example, the password manager in Microsoft Edge doesn't offer end-to-end encryption at all. Googles Passwortmanager hat [optional](https://support.google.com/accounts/answer/11350823) E2EE, und [Apples](https://support.apple.com/HT202303) bietet standardmäßig E2EE.

</div>

## Cloud-basiert

Diese Passwort-Manager synchronisieren deine Passwörter mit einem Cloud-Server, damit du von all deinen Geräten aus leicht darauf zugreifen kannst und vor Geräteverlust geschützt bist.

### Bitwarden

<div class="admonition recommendation" markdown>

![Bitwarden-Logo](assets/img/passwort-management/bitwarden.svg){ align=right }

**Bitwarden** ist ein kostenloser und quelloffener Passwort- und Passkey-Manager. Es zielt darauf ab, Passwortmanagementprobleme für Einzelpersonen, Teams und Unternehmen zu lösen. Bitwarden ist eine der besten und sichersten Lösungen, um alle deine Logins und Passwörter zu speichern und sie bequem zwischen all deinen Geräten zu synchronisieren.

[:octicons-home-16: Homepage](https://bitwarden.com/de-de/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/de-de/privacy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://bitwarden.com/de-de/help/){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1137397744)
- [:simple-github: GitHub](https://github.com/bitwarden/android/releases)
- [:fontawesome-brands-windows: Windows](https://bitwarden.com/download)
- [:simple-apple: macOS](https://bitwarden.com/download)
- [:simple-linux: Linux](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/nngceckbapebfimnlniiiahkandclblb)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)
- [:simple-safari: Safari](https://apps.apple.com/app/id1352778147)

</details>

</div>

Bitwarden verwendet standardmäßig [PBKDF2](https://bitwarden.com/help/kdf-algorithms/#pbkdf2) als Schlüsselableitungsalgorithmus (KDF). Als Alternative bietet es auch das sicherere [Argon2](https://bitwarden.com/help/kdf-algorithms/#argon2id) an. You can change your account's KDF algorithm in the web vault:

- [x] Select **Settings → Security → Keys → KDF algorithm → Argon2id**

Der serverseitige Code von Bitwarden ist [quelloffen](https://github.com/bitwarden/server). Wenn du also nicht die Bitwarden-Cloud nutzen möchtest, kannst du problemlos deinen eigenen Bitwarden-Synchronisierungsserver hosten.

### Proton Pass

<div class="admonition recommendation" markdown>

![Proton Pass Logo](assets/img/password-management/protonpass.svg){ align=right }

**Proton Pass** ist ein quelloffener, E2EE Passwort-Manager, der von Proton entwickelt wurde, dem Team hinter [Proton Mail](email.md#proton-mail). Es speichert deine Anmeldedaten sicher, erzeugt eindeutige E-Mail-Aliase und unterstützt und speichert Passkeys.

[:octicons-home-16: Homepage](https://proton.me/de/pass){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/de/pass/privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://proton.me/de/support/pass){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/protonpass){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=proton.android.pass)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6443490629)
- [:fontawesome-brands-windows: Windows](https://proton.me/pass/download)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/proton-pass)
- [:simple-googlechrome: Chrome](https://chromewebstore.google.com/detail/ghmbeldphafepmbegfdlkpapadhbakde)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/gcllgfdnfnllodcaambdaknbipemelie)
- [:octicons-browser-16: Web](https://pass.proton.me)

</details>

</div>

Mit der Übernahme von SimpleLogin im April 2022 bietet Proton eine "Hide-My-Email"-Funktion an, mit der du 10 Aliase (kostenloser Plan) oder unbegrenzte Aliase (kostenpflichtige Pläne) erstellen kannst.

Die mobilen Anwendungen und die Browsererweiterung von Proton Pass wurden im Mai und Juni 2023 von Cure53 geprüft. Das Sicherheitsanalyseunternehmen kam zu dem Schluss:

> Proton Pass Apps und Komponenten hinterlassen einen recht positiven Eindruck in Sachen Sicherheit.

Alle Probleme wurden kurz nach dem [Bericht](https://res.cloudinary.com/dbulfrlrz/images/v1707561557/wp-pme/Cure53-proton-pass-20230717/Cure53-proton-pass-20230717.pdf) angegangen und behoben.

### 1Password

<div class="admonition recommendation" markdown>

![1Password Logo](assets/img/password-management/1password.svg){ align=right }

**1Password** ist ein Passwortmanager mit einem starken Fokus auf Sicherheit und Benutzerfreundlichkeit, der es dir ermöglicht, Passwörter, Schlüssel, Kreditkarten, Softwarelizenzen und andere sensible Informationen in einem sicheren digitalen Tresor zu speichern. Dein Tresor wird auf den Servern von 1Password gegen eine [monatliche Gebühr] (https://1password.com/sign-up) gehostet.

1Password wird regelmäßig [geprüft] (https://support.1password.com/security-assessments) und bietet einen hervorragenden Kundensupport. 1Password ist ein Closed-Source-Produkt; die Sicherheit des Produkts ist jedoch in ihrem [Sicherheits-Whitepaper](https://1passwordstatic.com/files/security/1password-white-paper.pdf) ausführlich dokumentiert.

[:octicons-home-16: Homepage](https://1password.com/de){ .md-button .md-button--primary }
[:octicons-eye-16:](https://1password.com/de/legal/privacy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://support.1password.com/de/){ .card-link title="Dokumentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750)
- [:fontawesome-brands-windows: Windows](https://1password.com/downloads/windows)
- [:simple-apple: macOS](https://1password.com/downloads/mac)
- [:simple-linux: Linux](https://1password.com/downloads/linux)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/1password-x-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/aeblfdkhhhdcdjpifhhbdiojplfjncoa)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/dppgmdbiimibapkepcbdbmkaabgiofem)
- [:simple-safari: Safari](https://apps.apple.com/app/id1569813296)
- [:octicons-browser-16: Web](https://my.1password.com/signin)

</details>

</div>

Traditionell bot 1Password das beste Benutzererlebnis von Passwort-Managern für Menschen, die macOS und iOS nutzen; jedoch hat es nun Funktionsparität auf allen Plattformen erreicht. 1Password's clients boast many features geared towards families and less technical people, such as an intuitive UI for ease-of-use and navigation, as well as advanced functionality. Nahezu jede Funktion von 1Password ist in den nativen mobilen oder Desktop-Clients verfügbar.

Dein 1Password-Tresor ist sowohl mit deinem Master-Passwort als auch mit einem zufälligen 34-Zeichen-Sicherheitsschlüssel zur Verschlüsselung deiner Daten auf den Servern von 1Password gesichert. Dieser Sicherheitsschlüssel bietet einen zusätzlichen Schutz für deine Daten, da deine Daten unabhängig von deinem Master-Kennwort mit hoher Entropie gesichert sind. Viele andere Passwortmanager-Lösungen verlassen sich bei der Sicherung deiner Daten ausschließlich auf die Stärke deines Master-Passworts.

### Psono

<div class="admonition recommendation" markdown>

![Psono-Logo](assets/img/password-management/psono.svg){ align=right }

**Psono** ist ein freier und quelloffener Passwort-Manager aus Deutschland, der sich auf die Passwortverwaltung für Teams konzentriert. Psono unterstützt den sicheren Austausch von Passwörtern, Dateien, Lesezeichen und E-Mails. Alle Geheimnisse sind durch ein Master-Passwort geschützt.

[:octicons-home-16: Homepage](https://psono.com/de){ .md-button .md-button--primary }
[:octicons-eye-16:](https://psono.com/de/privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://doc.psono.com){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://gitlab.com/psono){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.psono.psono)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1545581224)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/eljmjmgjkbmpmfljlmklcfineebidmlo)
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
- Es muss ein veröffentlichtes Audit von einem angesehenen, unabhängigen Dritten vorliegen.
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

![KeePassXC Logo](assets/img/password-management/keepassxc.svg){ align=right }

**KeePassXC** ist ein Community-Fork von KeePassX, einer nativen, plattformübergreifenden Portierung von KeePass Password Safe, mit dem Ziel, es mit neuen Funktionen und Fehlerbehebungen zu erweitern und zu verbessern, um einen funktionsreichen, plattformübergreifenden und modernen Open-Source-Passwortmanager anzubieten.

[:octicons-home-16: Homepage](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://keepassxc.org/docs){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://keepassxc.org/donate){ .card-link title="Spenden" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://keepassxc.org/download/#windows)
- [:simple-apple: macOS](https://keepassxc.org/download/#mac)
- [:simple-linux: Linux](https://keepassxc.org/download/#linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/oboonakemofpalcgghocfoadofidjkkk)

</details>

</div>

KeePassXC speichert seine Exportdaten als [CSV-Dateien](https://en.wikipedia.org/wiki/Comma-separated_values). Es kann zu Datenverlusten kommen, wenn du diese Datei in einen anderen Passwortmanager importierst. Wir empfehlen dir, jeden Datensatz manuell zu überprüfen.

### KeePassDX (Android)

<div class="admonition recommendation" markdown>

![KeePassDX Logo](assets/img/password-management/keepassdx.svg){ align=right }

**KeePassDX** ist ein leichtgewichtiger Passwort-Manager für Android. Er ermöglicht das Bearbeiten von verschlüsselten Daten in einer einzelnen Datei im KeePass-Format und kann Formulare sicher ausfüllen.

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

The [pro version](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) of the app allows you to unlock cosmetic content and non-standard protocol features, but more importantly, it helps and encourages development.

### Gopass (CLI)

<div class="admonition recommendation" markdown>

![Gopass logo](assets/img/password-management/gopass.svg){ align=right }

**Gopass** is a minimal password manager for the command line written in Go. Es kann innerhalb von Skripting-Anwendungen verwendet werden und funktioniert auf allen wichtigen Desktop- und Server-Betriebssystemen.

[:octicons-home-16: Homepage](https://gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title="Spenden" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://gopass.pw/#install-windows)
- [:simple-apple: macOS](https://gopass.pw/#install-macos)
- [:simple-linux: Linux](https://gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://gopass.pw/#install-bsd)

</details>

</div>

### Kriterien

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

- Muss plattformübergreifend sein.
