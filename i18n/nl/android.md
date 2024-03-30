---
meta_title: "Android Recommendations: GrapheneOS and DivestOS - Privacy Guides"
title: "Android"
icon: 'simple/android'
description: You can replace the operating system on your Android phone with these secure and privacy-respecting alternatives.
cover: android.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Private Android Operating Systems
    url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://en.wikipedia.org/wiki/Android_(operating_system)
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://en.wikipedia.org/wiki/DivestOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": Product
    name: Pixel
    brand:
      "@type": Brand
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://en.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Review
      author:
        "@type": Organization
        name: Privacy Guides
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Auditor
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilities
    operatingSystem: Android
---

![Android logo](assets/img/android/android.svg){ align=right }

Het **Android Open Source Project** is een open-source mobiel besturingssysteem onder leiding van Google dat de meerderheid van de mobiele apparaten van de wereld aandrijft. De meeste telefoons die met Android worden verkocht zijn aangepast om invasieve integraties en apps zoals Google Play Services op te nemen, dus je kunt jouw privacy op jouw mobiele apparaat aanzienlijk verbeteren door de standaardinstallatie van jouw telefoon te vervangen door een versie van Android zonder deze invasieve functies.

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject){ .card-link title="Source Code" }

Dit zijn de Android-besturingssystemen, apparaten en apps die wij aanbevelen om de beveiliging en privacy van jouw mobiele apparaat te maximaliseren. aanbeveling

[Algemeen Android-overzicht en -aanbevelingen :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## AOSP-derivaten

Wij raden je aan een van deze aangepaste Android-besturingssystemen op jouw toestel te installeren, in volgorde van voorkeur, afhankelijk van de compatibiliteit van jouw toestel met deze besturingssystemen.

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

End-of-life apparaten (zoals GrapheneOS of CalyxOS's apparaten met "uitgebreide ondersteuning") beschikken niet over volledige beveiligingspatches (firmware-updates) omdat de OEM de ondersteuning heeft stopgezet. Deze apparaten kunnen niet als volledig veilig worden beschouwd, ongeacht de geïnstalleerde software.

</div>

### GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS logo](assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS logo](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** is de beste keuze als het gaat om privacy en veiligheid.

GrapheneOS biedt extra [beveiligingsversteviging](https://en.wikipedia.org/wiki/Hardening_(computing)) en privacyverbeteringen. Het heeft een [geharde geheugentoewijzer](https://github.com/GrapheneOS/hardened_malloc), netwerk- en sensormachtigingen, en diverse andere [beveiligingskenmerken](https://grapheneos.org/features). GrapheneOS wordt ook geleverd met volledige firmware-updates en ondertekende builds, dus geverifieerd opstarten wordt volledig ondersteund.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

</div>

GrapheneOS ondersteunt [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), die draait [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) volledig sandboxed als elke andere gewone app. This means you can take advantage of most Google Play Services, such as [push notifications](https://firebase.google.com/docs/cloud-messaging), while giving you full control over their permissions and access, and while containing them to a specific [work profile](os/android-overview.md#work-profile) or [user profile](os/android-overview.md#user-profiles) of your choice.

Google Pixel-telefoons zijn de enige apparaten die momenteel voldoen aan GrapheneOS's [hardware beveiligingseisen](https://grapheneos.org/faq#device-support).

[Waarom we GrapheneOS aanbevelen boven CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos ""){.md-button}

### DivestOS

<div class="admonition recommendation" markdown>

![DivestOS logo](assets/img/android/divestos.svg){ align=right }

**DivestOS** is a soft-fork of [LineageOS](https://lineageos.org).
DivestOS inherits many [supported devices](https://divestos.org/index.php?page=devices&base=LineageOS) from LineageOS. Het heeft ondertekende builds, waardoor het mogelijk is om [geverifieerde boot](https://source.android.com/security/verifiedboot) te hebben op sommige niet-Pixel apparaten.

[:octicons-home-16: Homepage](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Source Code" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribute }

</div>

DivestOS heeft geautomatiseerde kernel kwetsbaarheden ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [patching](https://gitlab.com/divested-mobile/cve_checker), minder propriëtaire blobs, en een aangepaste [hosts](https://divested.dev/index.php?page=dnsbl) bestand. Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates. DivestOS bevat ook kernelpatches van GrapheneOS en schakelt alle beschikbare kernelbeveiligingsfuncties in via [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

DivestOS implementeert enkele systeemhardingspatches die oorspronkelijk voor GrapheneOS zijn ontwikkeld. DivestOS 16.0 and higher implements GrapheneOS's [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) and SENSORS permission toggle, [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constification](https://en.wikipedia.org/wiki/Const_(computer_programming)), and partial [bionic](https://en.wikipedia.org/wiki/Bionic_(software)) hardening patchsets. 17.1 and higher features GrapheneOS's per-network full [MAC randomization](https://en.wikipedia.org/wiki/MAC_address#Randomization) option, [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, and automatic reboot/Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features).

DivestOS gebruikt F-Droid als standaard app store. We normally [recommend avoiding F-Droid](#f-droid), but doing so on DivestOS isn't viable; the developers update their apps via their own F-Droid repositories ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) and [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). We recommend disabling the official F-Droid app and using [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) **with the DivestOS repositories enabled** to keep those components up to date. Voor andere apps gelden nog steeds onze aanbevolen methoden om ze te verkrijgen.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

DivestOS firmware update [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) en kwaliteitscontrole varieert tussen de apparaten die het ondersteunt. We raden nog steeds GrapheneOS aan, afhankelijk van de compatibiliteit van uw toestel. Voor andere apparaten is DivestOS een goed alternatief.

Niet alle ondersteunde apparaten hebben geverifieerde boot, en sommige doen het beter dan andere.

</div>

## Android-apparaten

Wanneer je een apparaat koopt, raden wij je aan er een zo nieuw als mogelijk te kopen. De software en firmware van mobiele apparaten worden slechts een beperkte tijd ondersteund, dus door nieuw te kopen wordt die levensduur zoveel mogelijk verlengd.

Vermijd het kopen van telefoons van jouw mobiele provider. Deze hebben vaak een **vergrendelde bootloader** en bieden geen ondersteuning voor [OEM-ontgrendeling](https://source.android.com/devices/bootloader/locking_unlocking). Deze telefoonvarianten voorkomen dat je enige vorm van alternatieve Android-distributie installeert.

Wees zeer **voorzichtig** met het kopen van tweedehands telefoons van online marktplaatsen. Controleer altijd de reputatie van de verkoper. If the device is stolen, there's a possibility of it being entered in the [IMEI database](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). Er is ook een risico dat je in verband wordt gebracht met de activiteiten van de vorige eigenaar.

Nog een paar tips met betrekking tot Android toestellen en compatibiliteit van het besturingssysteem:

- Koop geen apparaten die het einde van hun levensduur hebben bereikt of bijna hebben bereikt, de fabrikant moet voor extra firmware-updates zorgen.
- Koop geen voorgeladen LineageOS of /e/ OS telefoons of Android telefoons zonder de juiste [Verified Boot](https://source.android.com/security/verifiedboot) ondersteuning en firmware updates. Deze apparaten hebben ook geen manier om te controleren of er mee geknoeid is.
- Kortom, als een toestel of Android-distributie hier niet vermeld staat, is daar waarschijnlijk een goede reden voor. Check out our [forum](https://discuss.privacyguides.net) to find details!

### Google Pixel

Google Pixel-telefoons zijn de **enige** toestellen die we aanraden om te kopen. Pixel-telefoons hebben een sterkere hardwarebeveiliging dan alle andere Android-toestellen die momenteel op de markt zijn, dankzij de juiste AVB-ondersteuning voor besturingssystemen van derden en Google's aangepaste [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) -beveiligingschips die functioneren als het Secure Element.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

**Google Pixel**-apparaten staan bekend om hun goede beveiliging en goede ondersteuning van [Verified Boot](https://source.android.com/security/verifiedboot), zelfs bij het installeren van aangepaste besturingssystemen.

Beginning with the **Pixel 8** and **8 Pro**, Pixel devices receive a minimum of 7 years of guaranteed security updates, ensuring a much longer lifespan compared to the 2-5 years competing OEMs typically offer.

[:material-shopping: Store](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

Secure Elements zoals de Titan M2 zijn beperkter dan de Trusted Execution Environment van de processor die door de meeste andere telefoons gebruikt wordt, omdat ze alleen gebruikt worden voor geheimen opslag, hardware attestatie, en snelheidsbeperking van het invoeren van wachtwoorden, niet voor het draaien van "vertrouwde" programma's. Telefoons zonder een Secure Element moeten de TEE gebruiken voor *alle* van deze functies. Dat leidt tot een groter aanvalsoppervlak.

Google Pixel phones use a TEE OS called Trusty which is [open source](https://source.android.com/security/trusty#whyTrusty), unlike many other phones.

De installatie van GrapheneOS op een Pixel telefoon is eenvoudig met hun [web installer](https://grapheneos.org/install/web). If you don't feel comfortable doing it yourself and are willing to spend a bit of extra money, check out the [NitroPhone](https://shop.nitrokey.com/shop) as they come preloaded with GrapheneOS from the reputable [Nitrokey](https://nitrokey.com/about) company.

Nog een paar tips voor de aanschaf van een Google Pixel:

- Als je op zoek bent naar een koopje voor een Pixel-toestel, raden wij je aan een "**a**"-model te kopen, net nadat het volgende vlaggenschip is uitgebracht. Kortingen zijn meestal beschikbaar omdat Google zal proberen om hun voorraad op te ruimen.
- Overweeg de mogelijkheden om de prijzen te verlagen en de speciale aanbiedingen van de fysieke winkels.
- Kijk naar online naar de koopjes sites in jouw land. Deze kunnen je waarschuwen voor goede uitverkopen.
- Google geeft een lijst met de [ondersteuningscyclus](https://support.google.com/nexus/answer/4457705) voor elk van hun toestellen. De prijs per dag voor een apparaat kan worden berekend als: $\text{Kosten} \over \text {Datum einde levensduur}-\text{Huidige datum}$, wat betekent dat hoe langer het apparaat wordt gebruikt, hoe lager de kosten per dag zijn.
- If the Pixel is unavailable in your region, the [NitroPhone](https://shop.nitrokey.com/shop) can be shipped globally.

## Algemene toepassingen

Wij bevelen op deze site een groot aantal Android-apps aan. De hier vermelde apps zijn exclusief voor Android en verbeteren of vervangen specifiek belangrijke systeemfuncties.

### Shelter

<div class="admonition recommendation" markdown>

![Shelter logo](assets/img/android/shelter.svg){ align=right }

**Shelter** is een app waarmee je gebruik kunt maken van de functie Werkprofiel van Android om apps op uw apparaat te isoleren of te dupliceren.

Shelter ondersteunt het blokkeren van het zoeken naar contacten tussen profielen en het delen van bestanden tussen profielen via de standaard bestandsbeheerder ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Source Code" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Contribute }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Shelter is recommended over [Insular](https://secure-system.gitlab.io/Insular) and [Island](https://github.com/oasisfeng/island) as it supports [contact search blocking](https://secure-system.gitlab.io/Insular/faq.html).

Wanneer je Shelter gebruikt, stelt je jouw volledige vertrouwen in de ontwikkelaar, aangezien Shelter optreedt als [Device Admin](https://developer.android.com/guide/topics/admin/device-admin) voor het werkprofiel en uitgebreide toegang heeft tot de gegevens die erin zijn opgeslagen.

</div>

### Secure Camera

<div class="admonition recommendation" markdown>

![Secure camera logo](assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure camera logo](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** is een camera-app gericht op privacy en veiligheid die afbeeldingen, video's en QR-codes kan vastleggen. De uitbreidingen van CameraX (Portret, HDR, Nachtzicht, Gezichtsretouche en Auto) worden ook ondersteund op beschikbare toestellen.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

De belangrijkste privacyfuncties zijn:

- Automatisch verwijderen van [Exif](https://en.wikipedia.org/wiki/Exif) metadata (standaard ingeschakeld)
- Gebruik van de nieuwe [Media](https://developer.android.com/training/data-storage/shared/media) API, daarom zijn [opslagmachtigingen](https://developer.android.com/training/data-storage) niet vereist
- Microfoontoestemming niet vereist, tenzij je geluid wilt opnemen

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Metadata worden momenteel niet verwijderd uit videobestanden, maar dat is wel de bedoeling.

De metadata over de beeldoriëntatie worden niet gewist. Als je gps locatie inschakelt (in Secure camera), wordt deze **niet** verwijderd. Als je dat later wilt verwijderen moet je een externe app gebruiken zoals [ExifEraser](data-redaction.md#exiferaser).

</div>

### Secure PDF Viewer

<div class="admonition recommendation" markdown>

![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** is een PDF-viewer gebaseerd op [pdf.js](https://en.wikipedia.org/wiki/PDF.js) die geen rechten vereist. De PDF wordt ingevoerd in een [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_ontwikkeling)) [webview](https://developer.android.com/guide/webapps/webview). Dit betekent dat er niet direct toestemming nodig is om toegang te krijgen tot inhoud of bestanden.

[Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) wordt gebruikt om af te dwingen dat de JavaScript en styling eigenschappen binnen het WebView volledig statische inhoud zijn.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Het verkrijgen van Applicaties

### Obtainium

<div class="admonition recommendation" markdown>

![Obtainium logo](assets/img/android/obtainium.svg){ align=right }

**Obtainium** is an app manager which allows you to install and update apps directly from the developer's own releases page (i.e. GitHub, GitLab, the developer's website, etc.), rather than a centralized app store/repository. It supports automatic background updates on Android 12 and higher.

[:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium allows you to download APK installer files from a wide variety of sources, and it is up to you to ensure those sources and apps are legitimate. For example, using Obtainium to install Signal from [Signal's APK landing page](https://signal.org/android/apk) should be fine, but installing from third-party APK repositories like Aptoide or APKPure may pose additional risks. The risk of installing a malicious *update* is lower, because Android itself verifies that all app updates are signed by the same developer as the existing app on your phone before installing them.

### GrapheneOS App Store

De app store van GrapheneOS is beschikbaar op [GitHub](https://github. com/GrapheneOS/Apps/releases). Het ondersteunt Android 12 en hoger en is in staat om zichzelf te updaten. The app store has standalone applications built by the GrapheneOS project such as the [Auditor](https://attestation.app), [Camera](https://github.com/GrapheneOS/Camera), and [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). Als je op zoek bent naar deze applicaties, raden wij je ten zeerste aan ze te halen uit de app-winkel van GrapheneOS in plaats van de Play Store, omdat de apps in hun winkel zijn ondertekend door de eigen handtekening van het GrapheneOS-project waar Google geen toegang toe heeft.

### Aurora Store

De Google Play Store vereist een Google-account om in te loggen, wat de privacy niet ten goede komt. Je kunt dit omzeilen door een alternatieve client te gebruiken, zoals Aurora Store.

<div class="admonition recommendation" markdown>

![Aurora Store logo](assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** is een Google Play Store-client waarvoor geen Google-account, Google Play Services of microG nodig is om apps te downloaden.

[:octicons-home-16: Homepage](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Met de Aurora Store kun je geen betaalde apps downloaden met hun anonieme accountfunctie. Je kunt optioneel inloggen met jouw Google-account bij de Aurora Store om apps te downloaden die je hebt gekocht, waardoor Google toegang krijgt tot de lijst van apps die je hebt geïnstalleerd, maar je profiteert nog steeds van het feit dat je niet de volledige Google Play-client en Google Play Services of microG op jouw toestel nodig hebt.

### Handmatig met RSS-meldingen

For apps that are released on platforms like GitHub and GitLab, you may be able to add an RSS feed to your [news aggregator](news-aggregators.md) that will help you keep track of new releases.

![RSS APK](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](./assets/img/android/rss-changes-light.png#only-light) ![APK Changes](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

Op GitHub, met [Secure Camera](#secure-camera) als voorbeeld, zou je navigeren naar de [release pagina](https://github.com/GrapheneOS/Camera/releases) en `.atom` toevoegen aan de URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### Gitlab

Op GitLab, met [Aurora Store](#aurora-store) als voorbeeld, zou je naar zijn [project repository](https://gitlab.com/AuroraOSS/AuroraStore) navigeren en `/-/tags?format=atom` aan de URL toevoegen:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Verifiëren van APK vingerafdrukken

Als u APK-bestanden downloadt om handmatig te installeren, kunt je hun handtekening verifiëren met de tool [`apksigner`](https://developer.android.com/studio/command-line/apksigner), die deel uitmaakt van Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Install [Java JDK](https://oracle.com/java/technologies/downloads).

2. Download de [Android Studio command line tools](https://developer.android.com/studio#command-tools).

3. Pak het gedownloade archief uit:

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. Voer het handtekening verificatie commando uit:

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. De resulterende hashes kunnen dan worden vergeleken met een andere bron. Some developers such as Signal [show the fingerprints](https://signal.org/android/apk) on their website.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![F-Droid logo](assets/img/android/f-droid.svg){ align=right width=120px }

==We only recommend F-Droid as a way to obtain apps which cannot be obtained via the means above.== F-Droid is often recommended as an alternative to Google Play, particularly in the privacy community. De optie om repositories van derden toe te voegen en niet beperkt te zijn tot het ecosysteem van Google heeft geleid tot de populariteit. F-Droid additionally has [reproducible builds](https://f-droid.org/en/docs/Reproducible_Builds) for some applications and is dedicated to free and open-source software. However, there are some security-related downsides to how F-Droid builds, signs, and delivers packages:

Vanwege hun proces van het bouwen van apps lopen apps in de officiële F-Droid-repository vaak achter op updates. F-Droid maintainers hergebruiken ook pakket-ID's tijdens het ondertekenen van apps met hun eigen sleutels, wat niet ideaal is omdat het F-Droid team dan het ultieme vertrouwen krijgt. Additionally, the requirements for an app to be included in the official F-Droid repo are less strict than other app stores like Google Play, meaning that F-Droid tends to host a lot more apps which are older, unmaintained, or otherwise no longer meet [modern security standards](https://developer.android.com/google/play/requirements/target-sdk).

Other popular third-party repositories for F-Droid such as [IzzyOnDroid](https://apt.izzysoft.de/fdroid) alleviate some of these concerns. De IzzyOnDroid repository haalt builds rechtstreeks van GitHub en is het op één na beste optie naast het direct downloaden vanaf de eigen repositories van de ontwikkelaars. However, it is not something that we can fully recommend, as apps are typically [removed](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) from that repository if they are later added to the main F-Droid repository. Hoewel dat logisch is (omdat het doel van die specifieke repository is om apps te hosten voordat ze worden geaccepteerd in de belangrijkste F-Droid-repository), kan het je achterlaten met geïnstalleerde apps die niet langer updates ontvangen.

That said, the [F-Droid](https://f-droid.org/en/packages) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid) repositories are home to countless apps, so they can be a useful tool to search for and discover open-source apps that you can then download through other means such as the Play Store, Aurora Store, or by getting the APK directly from the developer. You should use your best judgement when looking for new apps via this method, and keep an eye on how frequently the app is updated. Outdated apps may rely on unsupported libraries, among other things, posing a potential security risk.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

In some rare cases, the developer of an app will only distribute it through F-Droid ([Gadgetbridge](https://gadgetbridge.org) is one example of this). If you really need an app like that, we recommend using the newer [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) client instead of the original F-Droid app to obtain it. F-Droid Basic can do unattended updates without privileged extension or root, and has a reduced feature set (limiting attack surface).

</div>

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

### Besturingssystemen

- Moet open-source software zijn.
- Moet bootloadervergrendeling met aangepaste AVB-sleutel ondersteunen.
- Moet belangrijke Android-updates ontvangen binnen 0-1 maanden na de release.
- Moet binnen 0-14 dagen na release Android feature updates (minor versie) ontvangen.
- Moet regelmatige beveiligingspatches ontvangen binnen 0-5 dagen na vrijgave.
- Moet **niet** standaard "geroot" zijn uit de doos.
- Moet **niet** standaard Google Play Services inschakelen.
- Moet **niet** systeemaanpassing vereisen om Google Play Services te ondersteunen.

### Apparaten

- Moet ten minste één van onze aanbevolen aangepaste besturingssystemen ondersteunen.
- Moet momenteel nieuw in de winkel worden verkocht.
- Moet minimaal 5 jaar beveiligingsupdates ontvangen.
- Moet beschikken over speciale hardware voor secure elements.

### Applicaties

- Toepassingen op deze pagina mogen niet van toepassing zijn op andere softwarecategorieën op de site.
- Algemene toepassingen moeten de kernfunctionaliteit van het systeem uitbreiden of vervangen.
- Toepassingen moeten regelmatig worden bijgewerkt en onderhouden.
