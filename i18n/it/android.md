---
meta_title: "Consigli su Android: GrapheneOS e DivestOS - Privacy Guides"
title: "Android"
icon: 'simple/android'
description: Puoi sostituire il sistema operativo sul tuo telefono Android con queste alternative sicure e rispettose della privacy.
cover: android.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Sistemi operativi Android privati
    url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://it.wikipedia.org/wiki/Android
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
    sameAs: https://it.wikipedia.org/wiki/Google_Pixel
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
    name: Fotocamera Sicura
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Visualizzatore PDF Sicuro
    applicationCategory: Utilities
    operatingSystem: Android
---

![Logo di Android](assets/img/android/android.svg){ align=right }

Il **Progetto Open Source di Android** è un sistema operativo mobile e open source sviluppato da Google, utilizzato da gran parte dei dispositivi mobili al mondo. Gran parte dei telefonini venduti con Android sono modificati per includere integrazioni e app invasive come Google Play Services, quindi, puoi migliorare significativamente la tua privacy sul tuo dispositivo mobile, sostituendo l'installazione predefinita del tuo telefono con una versione di Android priva di tali funzionalità invasive.

[:octicons-home-16:](https://source.android.com/){ .card-link title=Home }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentazione}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/){ .card-link title="Codice Sorgente" }

Questi sono i sistemi operativi, i dispositivi e le app Android che consigliamo, per massimizzare la sicurezza e la privacy del tuo dispositivo mobile. Per scoprire di più su Android:

[Panoramica generale di Android :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## Derivati di AOSP

Consigliamo di installare uno di questi sistemi operativi personalizzati di Android sul tuo dispositivo, elencati per preferenza, a seconda della compatibilità del tuo dispositivo con essi.

!!! note "Nota"

    I dispositivi al termine della propria vita (come i dispositivi a "supporto esteso" di GrapheneOS o CalyxOS), non hanno correzioni di sicurezza complete (aggiornamenti del firmware), a causa dell'interruzione del supporto dall'OEM. Questi dispositivi non sono considerabili interamente sicuri, indipendentemente dal software installato.

### GrapheneOS

!!! recommendation

    ![Logo di GrapheneOS](assets/img/android/grapheneos.svg#only-light){ align=right }
    ![Logo di GrapheneOS](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }
    
    **GrapheneOS** è la scelta migliore per quanto riguarda privacy e sicurezza.
    
    GrapheneOS fornisce maggiore [sicurezza] (https://it.wikipedia.org/wiki/Hardening) e miglioramenti della privacy. Dispone di un [allocatore di memoria rafforzato](https://github.com/GrapheneOS/hardened_malloc), autorizzazioni di rete e dei sensori e varie altre [funzionalità di sicurezza](https://grapheneos.org/features). Inoltre, dispone di aggiornamenti completi del firmware e build firmate, quindi, l'avvio verificato è pienamente supportato.
    
    [:octicons-home-16: Home](https://grapheneos.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentazione}
    [:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuisci }

GrapheneOS supporta [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), che esegue [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) in piena modalità sandbox, come ogni altra app regolare. Ciò significa che puoi sfruttare gran parte dei Google Play Services, come le [notifiche push](https://firebase.google.com/docs/cloud-messaging/), pur avendo il pieno controllo sui suoi accessi e autorizzazioni, e contenendoli in un [profilo di lavoro](os/android-overview.md#work-profile) o [profilo dell'utente](os/android-overview.md#user-profiles) specifico e di tua scelta.

I telefoni Google Pixel sono i soli dispositivi che, al momento, soddisfano i [requisiti di sicurezza hardware](https://grapheneos.org/faq#device-support) di GrapheneOS.

[Perché consigliamo GrapheneOS, rispetto a CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/ ""){.md-button}

### DivestOS

!!! recommendation

    ![Logo di DivestOS](assets/img/android/divestos.svg){ align=right }
    
    **DivestOS** è una biforcazione morbida di [LineageOS](https://lineageos.org/).
    DivestOS eredita molti [dispositivi supportati](https://divestos.org/index.php?page=devices&base=LineageOS) da LineageOS. Dispone di build firmate, rendendo possibile l'[avvio verificato](https://source.android.com/security/verifiedboot) su alcuni dispositivi non Pixel.
    
    [:octicons-home-16: Home](https://divestos.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Servizio Onion" }
    [:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribuisci }

DivestOS offre [correzioni](https://gitlab.com/divested-mobile/cve_checker) automatizzate delle vulnerabilità del kernel (CVE), minori blob proprietari e un file degli [host](https://divested.dev/index.php?page=dnsbl) personalizzato. La sua WebView rafforzata, [Mulch](https://gitlab.com/divested-mobile/mulch), consente la [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) per tutte le architetture e il [partizionamento dello stato di rete](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning), ricevendo aggiornamenti fuori programma. Inoltre, DivestOS include delle correzioni del kernel da GrapheneOS e consente tutte le funzionalità di sicurezza del kernel disponibili, tramite il [rafforzamento di defconfig](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). Tutti i kernel più recenti della versione 3.4 includono la [sanificazione](https://lwn.net/Articles/334747/) completa delle pagine e tutti i circa 22 kernel compilati in Cleng, dispongono di [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471).

DivestOS implementa alcune correzioni di rafforzamento del sistema, sviluppate in origine per GrapheneOS. DivestOS 16.0 e superiori implementano l'interruttore delle autorizzazioni [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) e SENSORS, l'[allocatore di memoria rafforzato](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constificato](https://en.wikipedia.org/wiki/Const_(computer_programming)) e serie di correzioni di rafforzamento [bionico](https://en.wikipedia.org/wiki/Bionic_(software)). Le versioni 17.1 e superiori presentano l'opzione di [casualizzazione del MAC](https://en.wikipedia.org/wiki/MAC_address#Randomization) completa per rete di GrapheneOS, il controllo di [`ptrace_scope`](https://www.kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) e le [opzioni di timeout](https://grapheneos.org/features) di riavvio/Wi-Fi/Bluetooth automatiche.

DivestOS utilizza F-Droid come app store predefinito. Normalmente [consigliamo di evitare F-Droid](#f-droid), ma su DivestOS non è possibile farlo; gli sviluppatori aggiornano le loro applicazioni tramite i propri repository di F-Droid ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) e [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). Consigliamo di disabilitare l'applicazione ufficiale F-Droid e di utilizzare [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic/) **con i repository di DivestOS abilitati** per mantenere questi componenti aggiornati. Per le altre app, sono ancora validi i nostri metodi consigliati per ottenerle.

!!! warning

    Lo [stato](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) di aggiornamento del firmware di DivestOS e il controllo della qualiità variano tra i dispositivi supportati. Continuiamo a consigliare GrapheneOS a seconda della compatibilità con il tuo dispositivo. Per altri dispositivi, DivestOS è una buona alternativa.
    
    Non tutti i dispositivi supportati dispongono dell'avvio verificato e, alcuni, lo eseguono meglio di altri.

## Dispositivi Android

Acquistando un dispositivo, consigliamo di prenderne uno il più recente possibile. Il software e il firmware dei dispositivi mobili sono supportati esclusivamente per un periodo di tempo limitato, quindi, l'acquisto di prodotti nuovi ne estende la durata il più possibile.

Evita di acquistare telefoni dagli operatori di rete mobile. Questi, spesso, dispongono di un **bootloader bloccato** e non supportano lo [sblocco dell'OEM](https://source.android.com/devices/bootloader/locking_unlocking). Queste varianti ti impediranno di installare alcun tipo di distribuzione alternativa di Android.

Presta molta **attenzione** all'acquisto di telefoni di seconda mano dai mercati online. Controlla sempre la reputazione del venditore. Se il dispositivo è rubato, c'è la possibilità che [l'IMEI sia bloccato](https://www.gsma.com/security/resources/imei-blacklisting/). Esiste anche il rischio di essere associati all'attività del proprietario precedente.

Altri consigli sui dispositivi Android e sulla compatibilità del sistema operativo:

- Non acquistare dispositivi che hanno raggiunto o sono prossimi al termine della propria vita, gli aggiornamenti del firmware aggiuntivi devono essere forniti dal produttore.
- Non acquistare telefoni con LineageOS o /e/ OS preinstallati o qualsiasi dispositivo Android privo dell'adeguato supporto all'[Avvio Verificato](https://source.android.com/security/verifiedboot) e degli aggiornamenti del firmware. Inoltre, questi dispositivi non ti consentono di verificare se sono stati manomessi.
- In breve, se un dispositivo o una distribuzione Android non sono elencati qui, probabilmente c'è una buona ragione. Visita il nostro [forum](https://discuss.privacyguides.net/) per ulteriori dettagli!

### Google Pixel

I telefoni Google Pixel sono i **soli** dispositivi che consigliamo di acquistare. I telefoni Pixel presentano una maggiore sicurezza hardware rispetto agli altri dispositivi Android al momento presenti sul mercato, grazie all'adeguato supporto ai sistemi operativi di terze parti e ai chip di sicurezza personalizzati '[Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) di Google, che fungono da Secure Element.

!!! recommendation

    ![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }
    
    I dispositivi **Google Pixel** sono noti per avere una buona sicurezza e per supportare adeguatamente l'[Avvio Verificato](https://source.android.com/docs/security/features/verifiedboot?hl=it), anche installando sistemi operativi personalizzati.
    
    A partire da **Pixel 8** e **8 Pro**, i dispositivi Pixel riceveranno un minimo di 7 anni di aggiornamenti di sicurezza garantiti, assicurando una durata molto maggiore, rispetto a 2-5 anni tipicamente offerti dagli OEM concorrenti.
    
    [:material-shopping: Store](https://store.google.com/category/phones){ .md-button .md-button--primary }

Gli Elementi Sicuri come Titan M2 sono più limitati dell'Ambiente d'Esecuzione Attendibile del processore, utilizzato da gran parte degli altri dispositivi, essendo utilizzati soltanto per l'archiviazione segreta, l'attestazione del hardware e la limitazione della frequenza, non per eseguire i programmi "attendibili". I telefoni privi di un Elemento Sicuro, devono utilizzare TEE per *tutte* queste funzionalità, risultando in una maggiore superficie di attacco.

I telefoni Google Pixel utilizzano un SO TEE detto Trusty, che è [open source](https://source.android.com/security/trusty#whyTrusty), a differenza di molti altri dispositivi.

L'installazione di GrapheneOS su un telefono Pixel è facile grazie all'[installatore web](https://grapheneos.org/install/web). Se non ti senti a tuo agio a farlo da solo e desideri spendere un po' di denaro in più, consulta il [NitroPhone](https://shop.nitrokey.com/shop), preinstallato con GrapheneOS dalla rispettabile azienda [Nitrokey](https://www.nitrokey.com/about).

Altri suggerimenti per l'acquisto di un Google Pixel:

- Se vuoi fare un affare con un dispositivo Pixel, ti consigliamo di acquistare un modello "**A**", poco dopo l'uscita del modello top di gamma successivo. Solitamente, gli sconti, sono disponibili perché Google cercerà di smaltire le scorte.
- Considera le opzioni di sconto e offerte speciali, nei negozi fisici.
- Consulta le community di sconti online nel tuo paese. Possono segnalarti le vendite più convenienti.
- Google fornisce un elenco che mostra il [ciclo di supporto](https://support.google.com/nexus/answer/4457705) per ognuno dei propri dispositivi. Il prezzo giornaliero di un dispositivo è calcolabile come: $\text{Cost} \over \text {EOL Date}-\text{Current Date}$, a significare che maggiore è l'utilizzo del dispositivo, minore è il costo giornaliero.

## App generali

Consigliamo un'ampia gamma di app di Android, tramite questo sito. Le app qui elencate sono esclusive di Android e migliorano o sostituiscono nello specifico delle funzionalità fondamentali di sistema.

### Shelter

!!! recommendation

    ![Logo di Shelter](assets/img/android/shelter.svg){ align=right }
    
    **Shelter** è un'app che ti aiuta a sfruttare la funzionalità del Profilo di Lavoro di Android per isolare o duplicare le app sul tuo dispositivo.
    
    Shelter supporta il blocco della ricerca dei contatti tra profili e la condivisione di file tra profili tramite il gestore dei file predefinito ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).
    
    [:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://www.patreon.com/PeterCxy){ .card-link title=Contribuisci }

!!! warning "Attenzione"

    Shelter è consigliato rispetto a [Insular](https://secure-system.gitlab.io/Insular/) e [Island](https://github.com/oasisfeng/island), poiché supporta il [blocco della ricerca dei contatti](https://secure-system.gitlab.io/Insular/faq.html).
    
    Utilizzando Shelter, ti affidi interamente al suo sviluppatore, poiché Shelter agisce da [Admin del Dispositivo](https://developer.android.com/guide/topics/admin/device-admin?hl=it) per creare il Profilo di Lavoro, e ha ampio accesso ai dati memorizzati nel Profilo di Lavoro.

### Auditor

!!! recommendation

    ![Logo di Auditor](assets/img/android/auditor.svg#only-light){ align=right }
    ![Logo di Auditor](assets/img/android/auditor-dark.svg#only-dark){ align=right }
    
    **Auditor * * è un'app che sfrutta le funzionalità di sicurezza hardware per fornire il monitoraggio dell'integrità del dispositivo, convalidando attivamente l'identità di un dispositivo e l'integrità del suo sistema operativo. Al momento, funziona soltanto con GrapheneOS o con il sistema operativo di fabbrica per i [dispositivi supportati](https://attestation.app/about#device-support).
    
    [:octicons-home-16: Home](https://attestation.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentazione}
    [:octicons-code-16:](https://attestation.app/source){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribuisci }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Auditor esegue l'attestazione e il rilevamento delle intrusioni:

- Utilizzando un modello di [Fiducia Al Primo Utilizzo (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) tra un *revisore* e un *revisionato*, la coppia stabilisce una chiave privata nel [keystore del hardware](https://source.android.com/security/keystore/) del *Revisore*.
- Il *revisore* può essere un'altra istanza dell'app Auditor o del [Servizio di Attestazione Remoto](https://attestation.app).
- Il *revisore* registra lo stato corrente e la configurazione del *revisionato*.
- In caso di manomissione del sistema operativo del *revisore* in seguito al completamento dell'associazione, il revisore sarà a conoscenza della modifica allo stato e le configurazioni del dispositivo.
- Sarai avvisato della modifica.

Nessun'informazione personalmente identificabile è inviata al servizio d'attestazione. Ti consigliamo di iscriverti con un profilo anonimo e di consentire l'attestazione da remoto per il monitoraggio continuo.

Se il tuo [modello di minaccia](basics/threat-modeling.md) richiede la privacy, potresti considerare l'utilizzo di [Orbot](tor.md#orbot) o di una VPN per nascondere il tuo indirizzo IP dal servizio d'attestazione. Per assicurarti che il tuo hardware e sistema operativo siano autentici, [esegui l'attestazione locale](https://grapheneos.org/install/web#verifying-installation) immediatamente dopo l'installazione del dispositivo e prima di qualsiasi connessione a Internet.

### Fotocamera Sicura

!!! recommendation

    ![Logo di Secure Camera](assets/img/android/secure_camera.svg#only-light){ align=right }
    ![Logo di Secure camera](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }
    
     **Secure Camera** è un'app per fotocamera incentrata sulla privacy e la sicurezza che può catturare immagini, video e codici QR. Le estensioni del fornitore di CameraX (Ritratto, HDR, Notte, Ritocco del Viso e Automatica) sono supportate anche sui dispositivi disponibili.
    
    [:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
    [:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuisci }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Le principali funzionalità di privacy includono:

- Rimozione automatica dei metadati [Exif](https://en.wikipedia.org/wiki/Exif) (abilitata di default)
- Utilizzo della nuova API [Media](https://developer.android.com/training/data-storage/shared/media), dunque le [autorizzazioni d'archiviazione](https://developer.android.com/training/data-storage) non sono necessarie
- L'autorizzazione del microfono non è necessaria a meno che tu non voglia registrare dei suoni

!!! note "Nota"

    I metadati non sono al momento eliminati dai file video, ma la funzionalità è in fase di sviluppo.
    
    I metadati sull'orientamento dell'immagine non vengono eliminati. Se abiliti la posizione (su Secure Camera), nemmeno questa **sarà** eliminata. Se desideri eliminarla in seguito, dovrai utilizzare un'app esterna come [ExifEraser](data-redaction.md#exiferaser).

### Visualizzatore PDF Sicuro

!!! recommendation

    ![Logo di Secure PDF Viewer](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
    ![Logo di Secure PDF Viewer](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }
    
    **Secure PDF Viewer** è un visualizzatore di PDF basato su [pdf.js](https://it.wikipedia.org/wiki/PDF.js), che non richiede alcuna autorizzazione. Il PDF viene inserito in una [webview](https://developer.android.com/guide/webapps/webview) [in modalità sandbox](https://it.wikipedia.org/wiki/Sandbox). Ciò significa che non richiede direttamente l'autorizzazione all'accesso dei contenuti o dei file.
    
    La [Politica sulla Sicurezza dei Contenuti](https://en.wikipedia.org/wiki/Content_Security_Policy) è utilizzata per imporre che le proprietà JavaScript e di stile nella WebView siano contenuti interamente statici.
    
    [:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

## Ottenere le Applicazioni

### Obtainium

!!! recommendation

    ![Logo di Obtainium](assets/img/android/obtainium.svg){ align=right }
    
    **Obtainium** è un gestore di app che ti consente di installare e aggiornare le app direttamente dalla pagina di rilascio dello sviluppatore (es. GitHub, GitLab, il sito web dello sviluppatore, ecc.), piuttosto che un app store/repository di app centralizzato. Supporta gli aggiornamenti automatici in background su Android 12 e versioni successive.
    
    [:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribuisci}
    
    ??? downloads "Scarica"
    
        - [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

Obtainium ti consente di scaricare file di installazione APK da un'ampia varietà di fonti, ed è compito tuo assicurarti che tali fonti e applicazioni siano legittime. Ad esempio, utilizzare Obtainium per installare Signal dalla [pagina APK di Signal](https://signal.org/android/apk/) dovrebbe andare bene, ma l'installazione da repository APK di terze parti come Aptoide o APKPure potrebbe comportare ulteriori rischi. Il rischio di installare un *aggiornamento* dannoso è minore, poiché Android stesso verifica che tutti gli aggiornamenti delle app siano firmati dallo stesso sviluppatore dell'app esistente sul tuo telefono prima di installarli.

### App Store di GrapheneOS

L'app store di GrapheneOS è disponibile su [GitHub](https://github.com/GrapheneOS/Apps/releases). Supporta Android 12 e versioni successive ed è in grado di aggiornarsi da solo. L'app store contiene applicazioni indipendenti basate sul progetto di GrapheneOS, come [Auditor](https://attestation.app/), [Fotocamera](https://github.com/GrapheneOS/Camera) e [Visualizzatore PDF](https://github.com/GrapheneOS/PdfViewer). Se stai cercando queste app, consigliamo vivamente di ottenere l'app store di GrapheneOS del Play Store, poiché le app sul loro store sono firmate dalla firma dello stesso progetto di GrapheneOS, a cui Google non ha accesso.

### Aurora Store

Il Google Play Store richiede un profilo Google per l'accesso, il che non è un bene per la privacy. Puoi aggirare tale problema utilizzando un client alternativo, come Aurora Store.

!!! consiglio

    ![Logo di Aurora Store](assets/img/android/aurora-store.webp){ align=right }
    
    **Aurora Store** è un client di Google Play Store che non richiede un profilo di Google, Google Play Services o microG per scaricare le app.
    
    [:octicons-home-16: Pagina Principale](https://auroraoss.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Politica sulla Privacy" }
    [:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Codice Sorgente" }
    
    ??? downloads
    
        - [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

Aurora Store non consente di scaricare app a pagamento con la propria funzione del profilo anonimo. Facoltativamente, puoi accedere con il tuo profilo di Google all'Aurora Store per scaricare le app acquistate, consentendo l'accesso all'elenco delle app installate a Google e, tuttavia, beneficiando del fatto di non richiedere il client completo di Google Play e Google Play Services o microG sul tuo dispositivo.

### Manualmente con le notifiche RSS

Per le app rilasciate sulle piattaforme come GitHub e GitLab, potresti aggiungere un feed SS al tuo [aggregatore di notizie](/news-aggregators), che ti aiuterà a tenere traccia delle nuove versioni.

![APK di RSS](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![Modifiche APK](./assets/img/android/rss-changes-light.png#only-light) ![Modifiche APK](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

Su GitHub, utilizzando come esempio [Secure Camera](#secure-camera), dovresti navigare alla sua [pagina di rilascio](https://github.com/GrapheneOS/Camera/releases) e aggiungere `.atom` all'URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

Su GitLab, utilizzando come esempio [Aurora Store](#aurora-store), dovresti navigare al suo [repository del progetto](https://gitlab.com/AuroraOSS/AuroraStore) e aggiunge `/-/tags?format=atom` all'URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Verifica delle impronte digitali degli APK

Se scarichi i file APK da installare manualmente, puoi verificarne la firma con lo strumento [`apksigner`](https://developer.android.com/studio/command-line/apksigner), parte degli [strumenti di creazione](https://developer.android.com/studio/releases/build-tools) di Android.

1. Installa [Java JDK](https://www.oracle.com/java/technologies/downloads/).

2. Scarica gli [strumenti della riga di comando di Android Studio](https://developer.android.com/studio#command-tools).

3. Estrai l'archivio scaricato:

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. Esegui il comando di verifica della firma:

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. Gli hash risultanti possono poi esser confrontati con un'altra fonte. Alcuni sviluppatori, come per Signal, [mostrano le impronte digitali](https://signal.org/android/apk/) sul proprio sito web.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![Logo di F-Droid](assets/img/android/f-droid.svg){ align=right width=120px }

==Consigliamo F-Droid solo come mezzo per ottenere le applicazioni che non possono essere ottenute con i mezzi riportati sopra.== F-Droid è spesso raccomandato come alternativa a Google Play, in particolare nella community della privacy. La possibilità di aggiungere repository di terze parti e di non essere confinati a Google, ne ha determinato la popolarità. F-Droid dispone inoltre di [build riproducibili](https://f-droid.org/en/docs/Reproducible_Builds/) per alcune applicazioni ed è dedicato a software liberi e open source. Tuttavia, il modo in cui F-Droid costruisce, firma e consegna i pacchetti presenta alcuni aspetti negativi legati alla sicurezza:

A causa del loro processo di creazione delle app, quelle presenti nel repository ufficiale di F-Droid sono spesso in ritardo con gli aggiornamenti. Inoltre, i manutentori di F-Droid riutilizzano gli ID dei pacchetti firmando le app con le proprie chiavi, il che non è ideale, poiché conferisce al team di F-Droid la massima fiducia. Inoltre, i requisiti per l'inclusione di un'applicazione nel repo ufficiale di F-Droid sono meno rigidi rispetto ad altri app store come Google Play, il che significa che F-Droid tende ad ospitare molte applicazioni più vecchie, non mantenute o che comunque non soddisfano più [i standard moderni di sicurezza](https://developer.android.com/google/play/requirements/target-sdk).

Altri repository popolari di terze parti per F-Droid, come [IzzyOnDroid](https://apt.izzysoft.de/fdroid/), alleviano alcune di queste preoccupazioni. Il repository IzzyOnDroid estrae le build direttamente da GitHub ed è la seconda scelta migliore dopo i repository degli sviluppatori. Tuttavia, non è un'opzione che possiamo consigliare pienamente, poiché le applicazioni vengono tipicamente [rimosse](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) da questo repository se in seguito vengono aggiunte al repository principale di F-Droid. Sebbene ciò abbia senso (dato che l'obiettivo di questo particolare repository è ospitare le app prima che vengano accettate nel repository principale di F-Droid), ti può lasciare con le app installate senza ricevere più aggiornamenti.

Detto questo, i repository [F-Droid](https://f-droid.org/en/packages/) e [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) ospitano innumerevoli applicazioni, quindi possono essere uno strumento utile per cercare e scoprire applicazioni open source che si possono poi scaricare attraverso altri mezzi come Play Store, Aurora Store o ottenendo l'APK direttamente dallo sviluppatore. Quando cerchi nuove applicazioni attraverso questo metodo, dovresti usare il tuo miglior giudizio e tenere d'occhio la frequenza con cui l'applicazione viene aggiornata. Le applicazioni obsolete possono fare affidamento su librerie non supportate, tra le altre cose, comportando un potenziale rischio per la sicurezza.

!!! note "F-Droid Basic"

    In alcuni rari casi, lo sviluppatore di un'app la distribuirà soltanto tramite F-Droid, ([Gadgetbridge](https://gadgetbridge.org/) ne è un esempio). Se hai davvero bisogno di un'applicazione del genere, ti consigliamo di utilizzare il nuovo client [F-Droid Basic](https://f-droid.org/it/packages/org.fdroid.basic/) invece dell'applicazione originale F-Droid per ottenerla. F-Droid Basic può eseguire aggiornamenti incustoditi senza estensioni privilegiate o root, inoltre ha un set di funzionalità ridotto (limitando la superficie di attacco).

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

### Sistemi Operativi

- Deve essere un software open source.
- Deve supportare il blocco del bootloader con supporto alla chiave AVB personalizzato.
- Deve ricevere gli aggiornamenti principali di Android entro 0-1 mesi dalla pubblicazione.
- Deve ricevere gli aggiornamenti delle funzionalità Android (versione minore) entro 0-14 giorni dalla pubblicazione.
- Deve ricevere regolarmente le correzioni di sicurezza entro 0-5 giorni dalla pubblicazione.
- **Non** deve essere preconfigurato con il "root".
- **Non** deve abilitare Google Play Services di default.
- **Non** deve richiedere la modifica del sistema per supportare Google Play Services.

### Dispositivi

- Deve supportare almeno uno dei sistemi operativi personalizzati consigliati.
- Al momento, deve essere venduto nuovo nei negozi.
- Deve ricevere un minimo di 5 anni di aggiornamenti di sicurezza.
- Deve disporre di un hardware Secure Element dedicato.

### Applicazioni

- Le applicazioni su questa pagina non devono essere applicabili ad alcuna altra categoria di software presente sul sito.
- Le applicazioni generali dovrebbero estendere o sostituire le funzionalità di base del sistema.
- Le applicazioni dovrebbero ricevere aggiornamenti e manutenzione regolari.
