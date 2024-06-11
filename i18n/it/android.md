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
    sameAs: https://it.wikipedia.org/wiki/GrapheneOS
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

![Logo di Android](assets/img/android/android.svg){ align=right }

Il **Progetto Open Source di Android** è un sistema operativo mobile e open source sviluppato da Google, utilizzato da gran parte dei dispositivi mobili al mondo. Gran parte dei telefonini venduti con Android sono modificati per includere integrazioni e app invasive come Google Play Services, quindi, puoi migliorare significativamente la tua privacy sul tuo dispositivo mobile, sostituendo l'installazione predefinita del tuo telefono con una versione di Android priva di tali funzionalità invasive.

[:octicons-home-16:](https://source.android.com){ .card-link title=Pagina Principale }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentazione}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject){ .card-link title="Codice Sorgente" }

Questi sono i sistemi operativi, i dispositivi e le app Android che consigliamo, per massimizzare la sicurezza e la privacy del tuo dispositivo mobile. Per scoprire di più su Android:

[Panoramica generale di Android :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## Derivati di AOSP

Consigliamo di installare uno di questi sistemi operativi personalizzati di Android sul tuo dispositivo, elencati per preferenza, a seconda della compatibilità del tuo dispositivo con essi.

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

End-of-life devices (such as GrapheneOS's or CalyxOS's "extended support" devices) do not have full security patches (firmware updates) due to the OEM discontinuing support. Questi dispositivi non sono considerabili interamente sicuri, indipendentemente dal software installato.

</div>

### GrapheneOS

<div class="admonition recommendation" markdown>

![Logo di GrapheneOS](assets/img/android/grapheneos.svg#only-light){ align=right }
![Logo di GrapheneOS](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** è la scelta migliore per quanto riguarda privacy e sicurezza.

GrapheneOS fornisce maggiore [sicurezza] (https://it.wikipedia.org/wiki/Hardening) e miglioramenti della privacy. Dispone di un [allocatore di memoria rafforzato](https://github.com/GrapheneOS/hardened_malloc), autorizzazioni di rete e dei sensori e varie altre [funzionalità di sicurezza](https://grapheneos.org/features). Inoltre, dispone di aggiornamenti completi del firmware e build firmate, quindi, l'avvio verificato è pienamente supportato.

[:octicons-home-16: Pagina Principale](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentazione}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuisci }

</div>

GrapheneOS supporta [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), che esegue [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) in piena modalità sandbox, come ogni altra app regolare. Ciò significa che puoi sfruttare la maggior parte dei Google Play Services, come le [notifiche push](https://firebase.google.com/docs/cloud-messaging), offrendoti il pieno controllo delle autorizzazioni e dell'accesso, contenendoli in un [profilo di lavoro](os/android-overview.md#work-profile) specifico o in un [profilo utente](os/android-overview.md#user-profiles) di tua scelta.

I telefoni Google Pixel sono gli unici dispositivi che attualmente soddisfano i [requisiti di sicurezza hardware](https://grapheneos.org/faq#future-devices) di GrapheneOS.

[Perché consigliamo GrapheneOS, rispetto a CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos ""){.md-button}

### DivestOS

<div class="admonition recommendation" markdown>

![Logo di DivestOS](assets/img/android/divestos.svg){ align=right }

**DivestOS** è un soft-fork di [LineageOS](https://lineageos.org).
DivestOS eredita molti [dispositivi supportati](https://divestos.org/index.php?page=devices&base=LineageOS) da LineageOS. Dispone di build firmate, rendendo possibile l'[avvio verificato](https://source.android.com/docs/security/features/verifiedboot?hl=it) su alcuni dispositivi non Pixel.

[:octicons-home-16: Home](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Servizio Onion" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribuisci }

</div>

DivestOS offre [correzioni](https://gitlab.com/divested-mobile/cve_checker) automatizzate delle vulnerabilità del kernel (CVE), minori blob proprietari e un file degli [host](https://divested.dev/index.php?page=dnsbl) personalizzato. Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates. Inoltre, DivestOS include delle correzioni del kernel da GrapheneOS e consente tutte le funzionalità di sicurezza del kernel disponibili, tramite il [rafforzamento di defconfig](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

DivestOS implementa alcune correzioni di rafforzamento del sistema, sviluppate in origine per GrapheneOS. DivestOS 16.0 e superiori implementano l'interruttore delle autorizzazioni [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) e SENSORS, l'[allocatore di memoria rafforzato](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constificato](https://en.wikipedia.org/wiki/Const_(computer_programming)) e serie di correzioni di rafforzamento [bionico](https://en.wikipedia.org/wiki/Bionic_(software)). 17.1 and higher features GrapheneOS's per-network full [MAC randomization](https://en.wikipedia.org/wiki/MAC_address#Randomization) option, [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, and automatic reboot/Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features).

DivestOS utilizza F-Droid come app store predefinito. Normalmente [consigliamo di evitare F-Droid](#f-droid), ma su DivestOS non è possibile farlo; gli sviluppatori aggiornano le loro applicazioni tramite i propri repository di F-Droid ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) e [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). Consigliamo di disabilitare l'applicazione ufficiale F-Droid e di utilizzare [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) **con i repository DivestOS abilitati** per mantenere aggiornati questi componenti. Per le altre app, sono ancora validi i nostri metodi consigliati per ottenerle.

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Lo [stato](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) di aggiornamento del firmware di DivestOS e il controllo della qualiità variano tra i dispositivi supportati. Continuiamo a consigliare GrapheneOS a seconda della compatibilità con il tuo dispositivo. Per altri dispositivi, DivestOS è una buona alternativa.

Non tutti i dispositivi supportati dispongono dell'avvio verificato e, alcuni, lo eseguono meglio di altri.

</div>

## Dispositivi Android

Acquistando un dispositivo, consigliamo di prenderne uno il più recente possibile. Il software e il firmware dei dispositivi mobili sono supportati esclusivamente per un periodo di tempo limitato, quindi, l'acquisto di prodotti nuovi ne estende la durata il più possibile.

Evita di acquistare telefoni dagli operatori di rete mobile. Questi, spesso, dispongono di un **bootloader bloccato** e non supportano lo [sblocco dell'OEM](https://source.android.com/devices/bootloader/locking_unlocking). Queste varianti ti impediranno di installare alcun tipo di distribuzione alternativa di Android.

Presta molta **attenzione** all'acquisto di telefoni di seconda mano dai mercati online. Controlla sempre la reputazione del venditore. Se il dispositivo è stato rubato, c'è la possibilità che venga inserito nel [database IMEI](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). Esiste anche il rischio di essere associati all'attività del proprietario precedente.

Altri consigli sui dispositivi Android e sulla compatibilità del sistema operativo:

- Non acquistare dispositivi che hanno raggiunto o sono prossimi al termine della propria vita, gli aggiornamenti del firmware aggiuntivi devono essere forniti dal produttore.
- Non acquistare telefoni con LineageOS o /e/ OS preinstallati o qualsiasi dispositivo Android privo dell'adeguato supporto all'[Avvio Verificato](https://source.android.com/security/verifiedboot) e degli aggiornamenti del firmware. Inoltre, questi dispositivi non ti consentono di verificare se sono stati manomessi.
- In breve, se un dispositivo o una distribuzione Android non sono elencati qui, probabilmente c'è una buona ragione. Dai un'occhiata al nostro [forum](https://discuss.privacyguides.net) per trovare i dettagli!

### Google Pixel

I telefoni Google Pixel sono i **soli** dispositivi che consigliamo di acquistare. I telefoni Pixel presentano una maggiore sicurezza hardware rispetto agli altri dispositivi Android al momento presenti sul mercato, grazie all'adeguato supporto ai sistemi operativi di terze parti e ai chip di sicurezza personalizzati '[Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) di Google, che fungono da Secure Element.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

I dispositivi **Google Pixel** sono noti per avere una buona sicurezza e per supportare adeguatamente l'[Avvio Verificato](https://source.android.com/docs/security/features/verifiedboot?hl=it), anche installando sistemi operativi personalizzati.

A partire da **Pixel 8** e **8 Pro**, i dispositivi Pixel riceveranno un minimo di 7 anni di aggiornamenti di sicurezza garantiti, assicurando una durata molto maggiore, rispetto a 2-5 anni tipicamente offerti dagli OEM concorrenti.

[:material-shopping: Store](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

Gli Elementi Sicuri come Titan M2 sono più limitati dell'Ambiente d'Esecuzione Attendibile del processore, utilizzato da gran parte degli altri dispositivi, essendo utilizzati soltanto per l'archiviazione segreta, l'attestazione del hardware e la limitazione della frequenza, non per eseguire i programmi "attendibili". I telefoni privi di un Elemento Sicuro, devono utilizzare TEE per *tutte* queste funzionalità, risultando in una maggiore superficie di attacco.

I telefoni Google Pixel utilizzano un SO TEE detto Trusty, che è [open source](https://source.android.com/security/trusty#whyTrusty), a differenza di molti altri dispositivi.

L'installazione di GrapheneOS su un telefono Pixel è facile grazie all'[installatore web](https://grapheneos.org/install/web). If you don't feel comfortable doing it yourself and are willing to spend a bit of extra money, check out the [NitroPhone](https://shop.nitrokey.com/shop) as they come preloaded with GrapheneOS from the reputable [Nitrokey](https://nitrokey.com/about) company.

Altri suggerimenti per l'acquisto di un Google Pixel:

- Se vuoi fare un affare con un dispositivo Pixel, ti consigliamo di acquistare un modello "**A**", poco dopo l'uscita del modello top di gamma successivo. Solitamente, gli sconti, sono disponibili perché Google cercerà di smaltire le scorte.
- Considera le opzioni di sconto e offerte speciali, nei negozi fisici.
- Consulta le community di sconti online nel tuo paese. Possono segnalarti le vendite più convenienti.
- Google provides a list showing the [support cycle](https://support.google.com/nexus/answer/4457705) for each one of their devices. The price per day for a device can be calculated as: <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext>Cost</mtext> <mrow> <mtext>End of Life Date</mtext> <mo>−</mo> <mtext>Current Date</mtext> </mrow> </mfrac> </math> , meaning that the longer use of the device the lower cost per day.
- Se il Pixel non è disponibile nella tua regione, il [NitroPhone](https://shop.nitrokey.com/shop) può essere spedito a livello globale.

## App generali

Consigliamo un'ampia gamma di app di Android, tramite questo sito. Le app qui elencate sono esclusive di Android e migliorano o sostituiscono nello specifico delle funzionalità fondamentali di sistema.

### Shelter

<div class="admonition recommendation" markdown>

![Logo di Shelter](assets/img/android/shelter.svg){ align=right }

**Shelter** è un'app che ti aiuta a sfruttare la funzionalità del Profilo di Lavoro di Android per isolare o duplicare le app sul tuo dispositivo.

Shelter supporta il blocco della ricerca dei contatti tra profili e la condivisione di file tra profili tramite il gestore dei file predefinito ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Contribuisci }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Shelter è consigliato rispetto a [Insular](https://secure-system.gitlab.io/Insular) e [Island](https://github.com/oasisfeng/island) poiché supporta il [blocco della ricerca dei contatti](https://secure-system.gitlab.io/Insular/faq.html).

Utilizzando Shelter, ti affidi interamente al suo sviluppatore, poiché Shelter agisce da [Admin del Dispositivo](https://developer.android.com/guide/topics/admin/device-admin?hl=it) per creare il Profilo di Lavoro, e ha ampio accesso ai dati memorizzati nel Profilo di Lavoro.

</div>

### Secure Camera

<div class="admonition recommendation" markdown>

![Logo di Secure Camera](assets/img/android/secure_camera.svg#only-light){ align=right }
![Logo di Secure camera](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

 **Secure Camera** è un'app per fotocamera incentrata sulla privacy e la sicurezza che può catturare immagini, video e codici QR. Le estensioni del fornitore di CameraX (Ritratto, HDR, Notte, Ritocco del Viso e Automatica) sono supportate anche sui dispositivi disponibili.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Le principali funzionalità di privacy includono:

- Rimozione automatica dei metadati [Exif](https://en.wikipedia.org/wiki/Exif) (abilitata di default)
- Utilizzo della nuova API [Media](https://developer.android.com/training/data-storage/shared/media), dunque le [autorizzazioni d'archiviazione](https://developer.android.com/training/data-storage) non sono necessarie
- L'autorizzazione del microfono non è necessaria a meno che tu non voglia registrare dei suoni

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

I metadati non sono al momento eliminati dai file video, ma la funzionalità è in fase di sviluppo.

I metadati sull'orientamento dell'immagine non vengono eliminati. Se abiliti la posizione (su Secure Camera), nemmeno questa **sarà** eliminata. Se desideri eliminarla in seguito, dovrai utilizzare un'applicazione esterna come [ExifEraser] (data-redaction.md#exiferaser-android).

</div>

### Secure PDF Viewer

<div class="admonition recommendation" markdown>

![Logo di Secure PDF Viewer](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Logo di Secure PDF Viewer](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** è un visualizzatore di PDF basato su [pdf.js](https://it.wikipedia.org/wiki/PDF.js), che non richiede alcuna autorizzazione. Il PDF viene inserito in una [webview](https://developer.android.com/guide/webapps/webview) [in modalità sandbox](https://it.wikipedia.org/wiki/Sandbox). Ciò significa che non richiede direttamente l'autorizzazione all'accesso dei contenuti o dei file.

La [Politica sulla Sicurezza dei Contenuti](https://en.wikipedia.org/wiki/Content_Security_Policy) è utilizzata per imporre che le proprietà JavaScript e di stile nella WebView siano contenuti interamente statici.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Ottenere le Applicazioni

### Obtainium

<div class="admonition recommendation" markdown>

![Logo di Obtainium](assets/img/android/obtainium.svg){ align=right }

**Obtainium** è un gestore di app che ti consente di installare e aggiornare le app direttamente dalla pagina di rilascio dello sviluppatore (es. GitHub, GitLab, il sito web dello sviluppatore, ecc.), piuttosto che un app store/repository di app centralizzato. Supporta gli aggiornamenti automatici in background su Android 12 e versioni successive.

[:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium ti consente di scaricare file di installazione APK da un'ampia varietà di fonti, ed è compito tuo assicurarti che tali fonti e applicazioni siano legittime. For example, using Obtainium to install Signal from [Signal's APK landing page](https://signal.org/android/apk) should be fine, but installing from third-party APK repositories like Aptoide or APKPure may pose additional risks. Il rischio di installare un *aggiornamento* dannoso è minore, poiché Android stesso verifica che tutti gli aggiornamenti delle app siano firmati dallo stesso sviluppatore dell'app esistente sul tuo telefono prima di installarli.

### App Store di GrapheneOS

L'app store di GrapheneOS è disponibile su [GitHub](https://github.com/GrapheneOS/Apps/releases). Supporta Android 12 e versioni successive ed è in grado di aggiornarsi da solo. The app store has standalone applications built by the GrapheneOS project such as the [Auditor](https://attestation.app), [Camera](https://github.com/GrapheneOS/Camera), and [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). Se stai cercando queste app, consigliamo vivamente di ottenere l'app store di GrapheneOS del Play Store, poiché le app sul loro store sono firmate dalla firma dello stesso progetto di GrapheneOS, a cui Google non ha accesso.

### Aurora Store

Il Google Play Store richiede un profilo Google per l'accesso, il che non è un bene per la privacy. Puoi aggirare tale problema utilizzando un client alternativo, come Aurora Store.

<div class="admonition recommendation" markdown>

![Logo di Aurora Store](assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** è un client di Google Play Store che non richiede un profilo di Google, Google Play Services o microG per scaricare le app.

[:octicons-home-16: Pagina Principale](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Politica sulla Privacy" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Codice Sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Aurora Store non consente di scaricare app a pagamento con la propria funzione del profilo anonimo. Puoi facoltativamente accedere con il tuo account Google all'Aurora Store per scaricare le applicazioni acquistate, il che consente a Google di accedere all'elenco delle applicazioni da te installate. Tuttavia, benefici del vantaggio di non richiedere il client Google Play completo e i Google Play Services o microG sul tuo dispositivo.

### Manualmente con le notifiche RSS

Per le app rilasciate su piattaforme come GitHub e GitLab, potresti aggiungere un feed RSS al tuo [aggregatore di notizie](news-aggregators.md), che ti aiuterà a tener traccia delle nuove versioni.

![APK di RSS](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![Modifiche APK](./assets/img/android/rss-changes-light.png#only-light) ![Modifiche APK](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

Su GitHub, utilizzando come esempio [Secure Camera](#secure-camera), dovresti navigare alla sua [pagina di rilascio](https://github.com/GrapheneOS/Camera/releases) e aggiungere `.atom` all'URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

Su GitLab, utilizzando come esempio [Aurora Store](#aurora-store), dovresti navigare al suo [repository del progetto](https://gitlab.com/AuroraOSS/AuroraStore) e aggiunge `/-/tags?format=atom` all'URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Verifica delle impronte digitali degli APK

Se scarichi i file APK da installare manualmente, puoi verificarne la firma con lo strumento [`apksigner`](https://developer.android.com/studio/command-line/apksigner), parte degli [strumenti di creazione](https://developer.android.com/studio/releases/build-tools) di Android.

1. Installa [Java JDK](https://oracle.com/java/technologies/downloads).

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

5. Gli hash risultanti possono poi esser confrontati con un'altra fonte. Some developers such as Signal [show the fingerprints](https://signal.org/android/apk) on their website.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![Logo di F-Droid](assets/img/android/f-droid.svg){ align=right width=120px }

==Consigliamo F-Droid solo come mezzo per ottenere le applicazioni che non possono essere ottenute con i mezzi riportati sopra.== F-Droid è spesso raccomandato come alternativa a Google Play, in particolare nella community della privacy. La possibilità di aggiungere repository di terze parti e di non essere confinati a Google, ne ha determinato la popolarità. F-Droid additionally has [reproducible builds](https://f-droid.org/en/docs/Reproducible_Builds) for some applications and is dedicated to free and open-source software. Tuttavia, il modo in cui F-Droid costruisce, firma e consegna i pacchetti presenta alcuni aspetti negativi legati alla sicurezza:

A causa del loro processo di creazione delle app, quelle presenti nel repository ufficiale di F-Droid sono spesso in ritardo con gli aggiornamenti. Inoltre, i manutentori di F-Droid riutilizzano gli ID dei pacchetti firmando le app con le proprie chiavi, il che non è ideale, poiché conferisce al team di F-Droid la massima fiducia. Inoltre, i requisiti per l'inclusione di un'applicazione nel repo ufficiale di F-Droid sono meno rigidi rispetto ad altri app store come Google Play, il che significa che F-Droid tende ad ospitare molte applicazioni più vecchie, non mantenute o che comunque non soddisfano più [i standard moderni di sicurezza](https://developer.android.com/google/play/requirements/target-sdk).

Other popular third-party repositories for F-Droid such as [IzzyOnDroid](https://apt.izzysoft.de/fdroid) alleviate some of these concerns. Il repository IzzyOnDroid estrae le build direttamente da GitHub ed è la seconda scelta migliore dopo i repository degli sviluppatori. Tuttavia, non è un'opzione che possiamo consigliare pienamente, poiché le applicazioni vengono tipicamente [rimosse](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) da questo repository se in seguito vengono aggiunte al repository principale di F-Droid. Sebbene ciò abbia senso (dato che l'obiettivo di questo particolare repository è ospitare le app prima che vengano accettate nel repository principale di F-Droid), ti può lasciare con le app installate senza ricevere più aggiornamenti.

Detto ciò, i repository di [F-Droid](https://f-droid.org/en/packages) e [IzzyOnDroid](https://apt.izzysoft.de/fdroid) ospitano innumerevoli applicazioni, quindi possono essere uno strumento utile per cercare e scoprire applicazioni open-source che puoi scaricare attraverso altri mezzi come Play Store, Aurora Store o ottenendo l'APK direttamente dallo sviluppatore. Quando cerchi nuove applicazioni attraverso questo metodo, dovresti usare il tuo miglior giudizio e tenere d'occhio la frequenza con cui l'applicazione viene aggiornata. Le applicazioni obsolete possono fare affidamento su librerie non supportate, tra le altre cose, comportando un potenziale rischio per la sicurezza.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

In alcuni casi rari, lo sviluppatore di un'applicazione la distribuisce solo attraverso F-Droid ([Gadgetbridge](https://gadgetbridge.org) ne è un esempio). Se hai davvero bisogno di un'applicazione del genere, ti consigliamo di utilizzare il nuovo client [F-Droid Basic](https://f-droid.org/it/packages/org.fdroid.basic/) invece dell'applicazione originale F-Droid per ottenerla. F-Droid Basic supporta gli aggiornamenti automatici in background senza estensione privilegiata o root e ha un set di funzionalità ridotto (che limita la superficie di attacco).

</div>

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

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
