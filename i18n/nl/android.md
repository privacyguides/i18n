---
title: "Android"
icon: 'simple/android'
description: Je kunt het besturingssysteem op jouw Android-telefoon vervangen door deze veilige en privacy respecterende alternatieven.
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Privé Android besturingssystemen
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

[:octicons-home-16:](https://source.android.com/){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentatie}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/){ .card-link title="Broncode" }

Dit zijn de Android-besturingssystemen, apparaten en apps die wij aanbevelen om de beveiliging en privacy van jouw mobiele apparaat te maximaliseren. aanbeveling

[Algemeen Android-overzicht en -aanbevelingen :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

[Waarom we GrapheneOS aanbevelen boven CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/ ""){.md-button}

## AOSP-derivaten

Wij raden je aan een van deze aangepaste Android-besturingssystemen op jouw toestel te installeren, in volgorde van voorkeur, afhankelijk van de compatibiliteit van jouw toestel met deze besturingssystemen.

!!! note

    End-of-life apparaten (zoals GrapheneOS of CalyxOS's apparaten met "uitgebreide ondersteuning") beschikken niet over volledige beveiligingspatches (firmware-updates) omdat de OEM de ondersteuning heeft stopgezet. Deze apparaten kunnen niet als volledig veilig worden beschouwd, ongeacht de geïnstalleerde software.

### GrapheneOS

!!! recommendation

    ![GrapheneOS logo](assets/img/android/grapheneos.svg#only-light){ align=right }
    ![GrapheneOS logo](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }
    
    **GrapheneOS** is de beste keuze als het gaat om privacy en veiligheid.
    
    GrapheneOS biedt extra [beveiligingsversteviging](https://en.wikipedia.org/wiki/Hardening_(computing)) en privacyverbeteringen. Het heeft een [geharde geheugentoewijzer](https://github.com/GrapheneOS/hardened_malloc), netwerk- en sensormachtigingen, en diverse andere [beveiligingskenmerken](https://grapheneos.org/features). GrapheneOS wordt ook geleverd met volledige firmware-updates en ondertekende builds, dus geverifieerd opstarten wordt volledig ondersteund.
    
    [:octicons-home-16: Homepage](https://grapheneos.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacybeleid" }
    [:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentatie}
    [:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Broncode" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Bijdragen }

GrapheneOS ondersteunt [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), die draait [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) volledig sandboxed als elke andere gewone app. Dit betekent dat je kunt profiteren van de meeste Google Play-services, zoals [pushmeldingen](https://firebase.google.com/docs/cloud-messaging/), terwijl je volledige controle hebt over hun machtigingen en toegang, en terwijl je ze bevat in een specifiek [werkprofiel](os/android-overview.md#work-profile) of [gebruikersprofiel](os/android-overview.md#user-profiles) van jouw keuze.

Google Pixel-telefoons zijn de enige apparaten die momenteel voldoen aan GrapheneOS's [hardware beveiligingseisen](https://grapheneos.org/faq#device-support).

### DivestOS

!!! recommendation

    ![DivestOS logo](assets/img/android/divestos.svg){ align=right }
    
    **DivestOS** is een soft-fork van [LineageOS](https://lineageos.org/).
    DivestOS erft veel [ondersteunde apparaten](https://divestos.org/index.php?page=devices&base=LineageOS) van LineageOS. Het heeft ondertekende builds, waardoor het mogelijk is om [geverifieerde boot](https://source.android.com/security/verifiedboot) te hebben op sommige niet-Pixel apparaten.
    
    [:octicons-home-16: Homepage](https://divestos.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Privacybeleid" }
    [:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Broncode" }
    [:octicons-heart-16:](https://divested.dev/index.php?page=donate){ .card-link title=Bijdragen }

DivestOS heeft geautomatiseerde kernel kwetsbaarheden ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [patching](https://gitlab.com/divested-mobile/cve_checker), minder propriëtaire blobs, en een aangepaste [hosts](https://divested.dev/index.php?page=dnsbl) bestand. Zijn geharde WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), maakt [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) mogelijk voor alle architecturen en [network state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning), en ontvangt out-of-band updates. DivestOS bevat ook kernelpatches van GrapheneOS en schakelt alle beschikbare kernelbeveiligingsfuncties in via [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). Alle kernels nieuwer dan versie 3.4 bevatten volledige pagina [sanitization](https://lwn.net/Articles/334747/) en alle ~22 Clang-gecompileerde kernels hebben [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) ingeschakeld.

DivestOS implementeert enkele systeemhardingspatches die oorspronkelijk voor GrapheneOS zijn ontwikkeld. DivestOS 16.0 en hoger implementeert GrapheneOS's [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) en SENSORS permission toggle, [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](android/grapheneos-vs-calyxos.md#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constification](https://en.wikipedia.org/wiki/Const_(computer_programming)), en partial [bionic](https://en.wikipedia.org/wiki/Bionic_(software)) hardening patchsets. 17.1 en hoger bevat GrapheneOS's per-netwerk volledige [MAC randomisatie](https://en.wikipedia.org/wiki/MAC_address#Randomization) optie, [`ptrace_scope`](https://www.kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) controle, en automatische reboot/Wi-Fi/Bluetooth [timeout opties](https://grapheneos.org/features).

DivestOS gebruikt F-Droid als standaard app store. Normaal gesproken raden we aan om F-Droid te vermijden vanwege de vele [beveiligingsproblemen](#f-droid). Op DivestOS is dat echter niet mogelijk; de ontwikkelaars werken hun apps bij via hun eigen F-Droid repositories ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) en [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). Wij raden aan de officiële F-Droid app uit te schakelen en [Neo Store](https://github.com/NeoApplications/Neo-Store/) te gebruiken met de DivestOS repositories ingeschakeld om die componenten up-to-date te houden. Voor andere apps gelden nog steeds onze aanbevolen methoden om ze te verkrijgen.

!!! warning

    DivestOS firmware update [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) en kwaliteitscontrole varieert tussen de apparaten die het ondersteunt. We raden nog steeds GrapheneOS aan, afhankelijk van de compatibiliteit van uw toestel. Voor andere apparaten is DivestOS een goed alternatief.
    
    Niet alle ondersteunde apparaten hebben geverifieerde boot, en sommige doen het beter dan andere.

## Android-apparaten

Wanneer je een apparaat koopt, raden wij je aan er een zo nieuw als mogelijk te kopen. De software en firmware van mobiele apparaten worden slechts een beperkte tijd ondersteund, dus door nieuw te kopen wordt die levensduur zoveel mogelijk verlengd.

Vermijd het kopen van telefoons van jouw mobiele provider. Deze hebben vaak een **vergrendelde bootloader** en bieden geen ondersteuning voor [OEM-ontgrendeling](https://source.android.com/devices/bootloader/locking_unlocking). Deze telefoonvarianten voorkomen dat je enige vorm van alternatieve Android-distributie installeert.

Wees zeer **voorzichtig** met het kopen van tweedehands telefoons van online marktplaatsen. Controleer altijd de reputatie van de verkoper. Als het apparaat is gestolen, is het mogelijk [IMEI geblacklist](https://www.gsma.com/security/resources/imei-blacklisting/) is. Er is ook een risico dat je in verband wordt gebracht met de activiteiten van de vorige eigenaar.

Nog een paar tips met betrekking tot Android toestellen en compatibiliteit van het besturingssysteem:

- Koop geen apparaten die het einde van hun levensduur hebben bereikt of bijna hebben bereikt, de fabrikant moet voor extra firmware-updates zorgen.
- Koop geen voorgeladen LineageOS of /e/ OS telefoons of Android telefoons zonder de juiste [Verified Boot](https://source.android.com/security/verifiedboot) ondersteuning en firmware updates. Deze apparaten hebben ook geen manier om te controleren of er mee geknoeid is.
- Kortom, als een toestel of Android-distributie hier niet vermeld staat, is daar waarschijnlijk een goede reden voor. Kijk op ons [forum](https://discuss.privacyguides.net/) voor meer details!

### Google Pixel

Google Pixel-telefoons zijn de **enige** toestellen die we aanraden om te kopen. Pixel-telefoons hebben een sterkere hardwarebeveiliging dan alle andere Android-toestellen die momenteel op de markt zijn, dankzij de juiste AVB-ondersteuning voor besturingssystemen van derden en Google's aangepaste [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) -beveiligingschips die functioneren als het Secure Element.

!!! recommendation

    ![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }
    
    **Google Pixel**-apparaten staan bekend om hun goede beveiliging en goede ondersteuning van [Verified Boot](https://source.android.com/security/verifiedboot), zelfs bij het installeren van aangepaste besturingssystemen.
    
    Vanaf de **Pixel 6** en **6 Pro** krijgen Pixel-apparaten minimaal 5 jaar lang gegarandeerde beveiligingsupdates, wat een veel langere levensduur garandeert dan de 2-4 jaar die concurrerende OEM's doorgaans bieden.
    
    [:material-shopping: Store](https://store.google.com/category/phones){ .md-button .md-button--primary }

Secure Elements zoals de Titan M2 zijn beperkter dan de Trusted Execution Environment van de processor die door de meeste andere telefoons gebruikt wordt, omdat ze alleen gebruikt worden voor geheimen opslag, hardware attestatie, en snelheidsbeperking van het invoeren van wachtwoorden, niet voor het draaien van "vertrouwde" programma's. Telefoons zonder een Secure Element moeten de TEE gebruiken voor *alle* van deze functies. Dat leidt tot een groter aanvalsoppervlak.

Google Pixel-telefoons gebruiken een TEE OS genaamd Trusty dat [open-source](https://source.android.com/security/trusty#whyTrusty) is, in tegenstelling tot veel andere telefoons.

De installatie van GrapheneOS op een Pixel telefoon is eenvoudig met hun [web installer](https://grapheneos.org/install/web). Als je zich niet op jouw gemak voelt om het zelf te doen en bereid bent om een beetje extra geld uit te geven, kijk dan eens naar de [NitroPhone](https://shop.nitrokey.com/shop). Deze zijn voorgeladen met GrapheneOS van het gerenommeerde bedrijf [Nitrokey](https://www.nitrokey.com/about).

Nog een paar tips voor de aanschaf van een Google Pixel:

- Als je op zoek bent naar een koopje voor een Pixel-toestel, raden wij je aan een "**a**"-model te kopen, net nadat het volgende vlaggenschip is uitgebracht. Kortingen zijn meestal beschikbaar omdat Google zal proberen om hun voorraad op te ruimen.
- Overweeg de mogelijkheden om de prijzen te verlagen en de speciale aanbiedingen van de fysieke winkels.
- Kijk naar online naar de koopjes sites in jouw land. Deze kunnen je waarschuwen voor goede uitverkopen.
- Google geeft een lijst met de [ondersteuningscyclus](https://support.google.com/nexus/answer/4457705) voor elk van hun toestellen. De prijs per dag voor een apparaat kan worden berekend als: $\text{Kosten} \over \text {Datum einde levensduur}-\text{Huidige datum}$, wat betekent dat hoe langer het apparaat wordt gebruikt, hoe lager de kosten per dag zijn.

## Algemene toepassingen

Wij bevelen op deze site een groot aantal Android-apps aan. De hier vermelde apps zijn exclusief voor Android en verbeteren of vervangen specifiek belangrijke systeemfuncties.

### Shelter

!!! recommendation

    ![Shelter logo](assets/img/android/shelter.svg){ align=right }
    
    **Shelter** is een app waarmee je gebruik kunt maken van de functie Werkprofiel van Android om apps op uw apparaat te isoleren of te dupliceren.
    
    Shelter ondersteunt het blokkeren van het zoeken naar contacten tussen profielen en het delen van bestanden tussen profielen via de standaard bestandsbeheerder ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).
    
    [:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.patreon.com/PeterCxy){ .card-link title=Bijdragen }
    
    ??? downloads "Downloaden"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.typeblog.shelter)

!!! warning

    Shelter wordt aanbevolen boven [Insular](https://secure-system.gitlab.io/Insular/) en [Island](https://github.com/oasisfeng/island) omdat het [blokkeren van contact zoeken](https://secure-system.gitlab.io/Insular/faq.html) ondersteunt.
    
    Wanneer je Shelter gebruikt, stelt je jouw volledige vertrouwen in de ontwikkelaar, aangezien Shelter optreedt als [Device Admin](https://developer.android.com/guide/topics/admin/device-admin) voor het werkprofiel en uitgebreide toegang heeft tot de gegevens die erin zijn opgeslagen.

### Auditor

!!! recommendation

    ![Auditor logo](assets/img/android/auditor.svg#only-light){ align=right }
    ![Auditor logo](assets/img/android/auditor-dark.svg#only-dark){ align=right }
    
    **Auditor** is een app die hardwarebeveiligingsfuncties gebruikt om de integriteit van het apparaat te bewaken voor [ondersteunde apparaten](https://attestation.app/about#device-support). Momenteel werkt het alleen met GrapheneOS en het standaard besturingssysteem van het toestel.
    
    [:octicons-home-16: Homepage](https://attestation.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Privacybeleid" }
    [:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentatie}
    [:octicons-code-16:](https://attestation.app/source){ .card-link title="Broncode" }
    [:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Bijdragen }
    
    ??? downloads "Downloaden"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Auditor voert attest en inbraakdetectie uit door:

- Door gebruik te maken van een [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) model tussen een *auditor* en *audittee*, stelt het paar een private sleutel op in de [hardwaregebaseerde sleutelbewaarplaats](https://source.android.com/security/keystore/) van de *auditor*.
- De *auditor* kan een ander exemplaar van de Auditor app zijn of de [Remote Attestation Service](https://attestation.app).
- De *auditor* registreert de huidige toestand en configuratie van de *auditee*.
- Mocht er met het besturingssysteem van de *auditee worden geknoeid* nadat de koppeling is voltooid, dan zal de auditor op de hoogte zijn van de verandering in de toestand en de configuraties van het apparaat.
- Je zult op de hoogte worden gebracht van de wijziging.

Er wordt geen persoonlijk identificeerbare informatie aan de attestatiedienst verstrekt. Wij raden je aan je aan te melden met een anonieme account en attestatie op afstand in te schakelen voor voortdurende controle.

Als jouw [bedreigingsmodel](basics/threat-modeling.md) privacy vereist, kunt je overwegen [Orbot](tor.md#orbot) of een VPN te gebruiken om jouw IP-adres voor de attestatiedienst te verbergen. Om er zeker van te zijn dat jouw hardware en besturingssysteem echt zijn, voert [onmiddellijk na de installatie van het apparaat en vóór elke internetverbinding een lokale attestatie uit:](https://grapheneos.org/install/web#verifying-installation).

### Secure Camera

!!! recommendation

    ![Secure camera logo](assets/img/android/secure_camera.svg#only-light){ align=right }
    ![Secure camera logo](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }
    
    **Secure Camera** is een camera-app gericht op privacy en veiligheid die afbeeldingen, video's en QR-codes kan vastleggen. De uitbreidingen van CameraX (Portret, HDR, Nachtzicht, Gezichtsretouche en Auto) worden ook ondersteund op beschikbare toestellen.
    
    [:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
    [:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Broncode" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Bijdrage leveren }
    
    ??? downloads "Downloaden"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

De belangrijkste privacyfuncties zijn:

- Automatisch verwijderen van [Exif](https://en.wikipedia.org/wiki/Exif) metadata (standaard ingeschakeld)
- Gebruik van de nieuwe [Media](https://developer.android.com/training/data-storage/shared/media) API, daarom zijn [opslagmachtigingen](https://developer.android.com/training/data-storage) niet vereist
- Microfoontoestemming niet vereist, tenzij je geluid wilt opnemen

!!! note

    Metadata worden momenteel niet verwijderd uit videobestanden, maar dat is wel de bedoeling.
    
    De metadata over de beeldoriëntatie worden niet gewist. Als je gps locatie inschakelt (in Secure camera), wordt deze **niet** verwijderd. Als je dat later wilt verwijderen moet je een externe app gebruiken zoals [ExifEraser](data-redaction.md#exiferaser).

### Secure PDF Viewer

!!! recommendation

    ![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
    ![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }
    
    **Secure PDF Viewer** is een PDF-viewer gebaseerd op [pdf.js](https://en.wikipedia.org/wiki/PDF.js) die geen rechten vereist. De PDF wordt ingevoerd in een [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_ontwikkeling)) [webview](https://developer.android.com/guide/webapps/webview). Dit betekent dat er niet direct toestemming nodig is om toegang te krijgen tot inhoud of bestanden.
    
    [Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) wordt gebruikt om af te dwingen dat de JavaScript en styling eigenschappen binnen het WebView volledig statische inhoud zijn.
    
    [:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Bijdragen }
    
    ??? downloads "Downloaden"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

## Het verkrijgen van Applicaties

### GrapheneOS App Store

De app store van GrapheneOS is beschikbaar op [GitHub](https://github. com/GrapheneOS/Apps/releases). Het ondersteunt Android 12 en hoger en is in staat om zichzelf te updaten. De app store heeft losstaande applicaties gebouwd door het GrapheneOS project, zoals de [Auditor](https://attestation.app/), [Camera](https://github.com/GrapheneOS/Camera), en [PDF-viewer](https://github.com/GrapheneOS/PdfViewer). Als je op zoek bent naar deze applicaties, raden wij je ten zeerste aan ze te halen uit de app-winkel van GrapheneOS in plaats van de Play Store, omdat de apps in hun winkel zijn ondertekend door de eigen handtekening van het GrapheneOS-project waar Google geen toegang toe heeft.

### Aurora Store

De Google Play Store vereist een Google-account om in te loggen, wat de privacy niet ten goede komt. Je kunt dit omzeilen door een alternatieve client te gebruiken, zoals Aurora Store.

!!! recommendation

    ![Aurora Store logo](assets/img/android/aurora-store.webp){ align=right }
    
    **Aurora Store** is een Google Play Store-client waarvoor geen Google-account, Google Play Services of microG nodig is om apps te downloaden.
    
    [:octicons-home-16: Homepage](https://auroraoss.com/){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Broncode" }
    
    ??? downloads "Downloaden"
    
        - [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

Met de Aurora Store kun je geen betaalde apps downloaden met hun anonieme accountfunctie. Je kunt optioneel inloggen met jouw Google-account bij de Aurora Store om apps te downloaden die je hebt gekocht, waardoor Google toegang krijgt tot de lijst van apps die je hebt geïnstalleerd, maar je profiteert nog steeds van het feit dat je niet de volledige Google Play-client en Google Play Services of microG op jouw toestel nodig hebt.

### Handmatig met RSS-meldingen

Voor apps die worden uitgebracht op platforms als GitHub en GitLab, kun je misschien een RSS-feed toevoegen aan je [nieuwsaggregator](/news-aggregators) waarmee je nieuwe releases kunt volgen.

![RSS APK](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](./assets/img/android/rss-changes-light.png#only-light) ![APK Changes](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

Op GitHub, met [Secure Camera](#secure-camera) als voorbeeld, zou je navigeren naar de [release pagina](https://github.com/GrapheneOS/Camera/releases) en `.atom` toevoegen aan de URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### Gitlab

Op GitLab, met [Aurora Store](#aurora-store) als voorbeeld, zou je naar zijn [project repository](https://gitlab.com/AuroraOSS/AuroraStore) navigeren en `/-/tags?format=atom` aan de URL toevoegen:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Verifiëren van APK vingerafdrukken

Als u APK-bestanden downloadt om handmatig te installeren, kunt je hun handtekening verifiëren met de tool [`apksigner`](https://developer.android.com/studio/command-line/apksigner), die deel uitmaakt van Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Installeer [Java JDK](https://www.oracle.com/java/technologies/downloads/).

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

5. De resulterende hashes kunnen dan worden vergeleken met een andere bron. Sommige ontwikkelaars zoals Signal [tonen de vingerafdrukken](https://signal.org/android/apk/) op hun website.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![F-Droid logo](assets/img/android/f-droid.svg){ align=right width=120px }

==We raden **momenteel niet** F-Droid aan als een manier om apps te verkrijgen.== F-Droid wordt vaak aanbevolen als alternatief voor Google Play, vooral in de privacygemeenschap. De optie om repositories van derden toe te voegen en niet beperkt te zijn tot het ecosysteem van Google heeft geleid tot de populariteit. F-Droid heeft bovendien [reproduceerbare builds](https://f-droid.org/en/docs/Reproducible_Builds/) voor sommige toepassingen en zet zich in voor vrije en open-source software. Er zijn echter [opmerkelijke problemen](https://privsec.dev/posts/android/f-droid-security-issues/) met de officiële F-Droid-client, hun kwaliteitscontrole en hoe ze pakketten bouwen, ondertekenen en leveren.

Vanwege hun proces van het bouwen van apps lopen apps in de officiële F-Droid-repository vaak achter op updates. F-Droid maintainers hergebruiken ook pakket-ID's tijdens het ondertekenen van apps met hun eigen sleutels, wat niet ideaal is omdat het F-Droid team dan het ultieme vertrouwen krijgt.

Andere populaire repositories van derden zoals [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) verlichten enkele van deze zorgen. De IzzyOnDroid repository haalt builds rechtstreeks van GitHub en is het op één na beste optie naast het direct downloaden vanaf de eigen repositories van de ontwikkelaars. Het is echter niet iets dat we kunnen aanbevelen, aangezien apps meestal [worden verwijderd](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) van die respository wanneer ze in de hoofdrepository van F-Droid terechtkomen. Hoewel dat logisch is (omdat het doel van die specifieke repository is om apps te hosten voordat ze worden geaccepteerd in de belangrijkste F-Droid-repository), kan het je achterlaten met geïnstalleerde apps die niet langer updates ontvangen.

Dat gezegd zijnde, de [F-Droid](https://f-droid.org/en/packages/) en [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) repositories zijn de thuisbasis van talloze apps, dus ze kunnen een nuttig hulpmiddel zijn om open-source apps te zoeken en te ontdekken die je vervolgens kunt downloaden via Play Store, Aurora Store, of door het verkrijgen van de APK rechtstreeks van de ontwikkelaar. Het is belangrijk om in gedachten te houden dat sommige apps in deze repositories al jaren niet zijn bijgewerkt en mogelijk afhankelijk zijn van niet-ondersteunde bibliotheken, onder andere, die een potentieel beveiligingsrisico vormen. Je moet jouw beste oordeel gebruiken bij het zoeken naar nieuwe apps via deze methode.

!!! note

    In sommige zeldzame gevallen verspreidt de ontwikkelaar van een app deze alleen via F-Droid ([Gadgetbridge](https://gadgetbridge.org/) is hier een voorbeeld van). Als je echt zo'n app nodig hebt, raden we je aan de [Neo Store](https://github.com/NeoApplications/Neo-Store/) te gebruiken in plaats van de officiële F-Droid app om hem te verkrijgen.

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

!!! example "Deze sectie is nieuw"

    We werken aan het vaststellen van gedefinieerde criteria voor elk deel van onze site, en dit kan onderhevig zijn aan verandering. Als je vragen hebt over onze criteria, stel ze dan [op ons forum](https://discuss.privacyguides.net/latest) en neem niet aan dat we iets niet in overweging hebben genomen bij het opstellen van onze aanbevelingen als het hier niet vermeld staat. Er zijn veel factoren die worden overwogen en besproken wanneer wij een project aanbevelen, en het documenteren van elke factor is een werk in uitvoering.

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
