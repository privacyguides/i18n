---
title: Panoramica Android
icon: simple/android
description: Android è un sistema operativo open-source con forti protezioni di sicurezza, il che lo rende la nostra scelta migliore per i telefoni.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Logo di Android](../assets/img/android/android.svg){ align=right }

Il **Progetto Open Source di Androd** è un sistema operativo mobile sicuro, che dispone di una forte [modalità sandbox delle app](https://source.android.com/security/app-sandbox), [Avvio Verificato](https://source.android.com/security/verifiedboot) (AVB) e di un robusto sistema di controllo delle [autorizzazioni](https://developer.android.com/guide/topics/permissions/overview).

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="Source Code" }

[Our Android Advice :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## Protezioni di Sicurezza

Key components of the Android security model include [verified boot](#verified-boot), [firmware updates](#firmware-updates), and a robust [permission system](#android-permissions). These important security features form the baseline of the minimum criteria for our [mobile phone](../mobile-phones.md) and [custom Android OS](../android/distributions.md) recommendations.

### Avvio Verificato

[**Verified Boot**](https://source.android.com/security/verifiedboot) is an important part of the Android security model. Fornisce protezione dagli attacchi di [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack), la persistenza del malware e assicura che gli aggiornamenti di sicurezza non siano rimuovibili con la [protezione da rollback](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

Android 10 e superiori si sono allontanati dalla crittografia dell'intero disco, verso una [crittografia basata sui file](https://source.android.com/security/encryption/file-based) più sicura. I tuoi dati sono crittografati utilizzando chiavi crittografiche univoche e il file del sistema operativo sono lasciati non crittografati.

L'Avvio Verificato assicura l'integrità dei file del sistema operativo, dunque impedendo a un avversario con l'accesso fisico, di manomettere o installare malware sul dispositivo. Nell'improbabile caso in cui il malware possa sfruttare altre parti del sistema e ottenere accesso privilegiato superiore, l'Avvio Verificato impedirà e ripristinerà le modifiche alla partizione di sistema, al riavvio del dispositivo.

Sfortunatamente, gli OEM devono supportare l'Avvio Verificato sulla propria distribuzione Android stock. Solo alcuni OEM, come Google, supportano la registrazione di chiavi AVB personalizzate sui propri dispositivi. Inoltre, alcuni AOSP derivati come LineageOS o /e/ OS, non supportano l'Avvio Verificato anche su hardware che lo supporta, per i sistemi operativi di terze parti. Ti consigliamo di verificare il supporto **prima** di acquistare un nuovo dispositivo. I derivati AOSP che non supportano l'Avvio Verificato **non** sono consigliati.

Inoltre, molti OEM dispongono di un'implementazione corrotta dell'Avvio Verificato, di cui devi essere consapevole, al di là del loro marketing. Ad esempio, i Fairphone 3 e 4 non sono sicuri di default, poiché il [bootloader di fabbrica si fida della chiave di firma AVB pubblica](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### Aggiornamenti del firmware

**Firmware updates** are critical for maintaining security and without them your device cannot be secure. Gli OEM stipulano accordi di supporto coi propri partner per fornire i componenti closed source per un periodo di supporto limitato. Questi sono mensilmente riportati nei [Bollettini di Sicurezza di Android](https://source.android.com/security/bulletin).

Poiché i componenti del telefono, come il processore e le tecnologie radio, si affidano a componenti closed source, gli aggiornamenti devono essere forniti dai rispettivi produttori. Dunque, è importante che tu acquisti un dispositivo entro un ciclo di supporto attivo. [Qualcomm](https://qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) support their devices for 4 years, while cheaper products often have shorter support cycles. Con l'introduzione del [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google produce ora il proprio SoC e fornirà un supporto di almeno 5 anni. Con l'introduzione della serie Pixel 8, Google ha aumentato la finestra di supporto a 7 anni.

I dispositivi EOL, non più supportati dal produttore del SoC, non possono ricevere aggiornamenti del firmware dai fornitori OEM o dai distributori di ricambi per Android. Ciò significa che i problemi di sicurezza di questi dispositivi non saranno risolti.

Fairphone, ad esempio, commercializza il proprio dispositivo Fairphone 4 con 6 anni di assistenza. Tuttavia, il SoC (Qualcomm Snapdragon 750G sul Fairphone 4), ha una data di scadenza considerevolmente più breve. Ciò significa che gli aggiornamenti di sicurezza di quel firmware da Qualcomm per il Fairphone 4 termineranno a settembre 2023, indipendentemente dal fatto che Fairphone continui a rilasciare aggiornamenti di sicurezza del software.

### Autorizzazioni di Android

[**Permissions on Android**](https://developer.android.com/guide/topics/permissions/overview) grant you control over what apps are allowed to access. Google apporta [miglioramenti](https://developer.android.com/about/versions/11/privacy/permissions) regolari al sistema di autorizzazioni, in ogni nuova versione. Tutte le app che installi sono rigorosamente [testate](https://source.android.com/security/app-sandbox), dunque, non è necessario installare alcuna app di antivirus.

Uno smartphone con la versione più recente di Android sarà sempre più sicuro di un vecchio smartphone con un antivirus a pagamento. It's better not to pay for antivirus software and to save money to buy a new smartphone such as a [Google Pixel](../mobile-phones.md#google-pixel).

Android 10:

- L'[Archiviazione Esaminata](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) ti conferisce maggiore controllo sui file e può limitare ciò che può [accedere all'archiviazione esterna](https://developer.android.com/training/data-storage#permissions). Le app possono avere una cartella specifica nell'archiviazione esterna, nonché l'abilità di memorizzarvi tipi specifici di file multimediali.
- Accesso più ristretto alla [posizione del dispositivo](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location), introducendo l'autorizzazione `ACCESS_BACKGROUND_LOCATION`. Questa impedisce alle app di accedere alla posizione quando in esecuzione in background, senza l'espressa autorizzazione dall'utente.

Android 11:

- [Autorizzazioni una tantum](https://developer.android.com/about/versions/11/privacy/permissions#one-time), che ti consentono di concedere un'autorizzazione a un'app, una singola volta.
- [Ripristino automatico delle autorizzazioni](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset), che ripristina i [permessi in esecuzione](https://developer.android.com/guide/topics/permissions/overview#runtime), concessi all'apertura dell'app.
- Autorizzazioni granulari per accedere alle funzioni relative al [ numero di telefono](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers).

Android 12:

- Un'autorizzazione per concedere soltanto la [posizione approssimativa](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- Ripristino automatico delle [app ibernate](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation).
- [Controllo dell'accesso ai dati](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing), che semplifica la determinazione di quale parte di un'app sta eseguendo un certo tipo di accesso ai dati.

Android 13:

- Un'autorizzazione per l'[accesso alle Wi-Fi nelle vicinanze](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points were a popular way for apps to track a user's location.
- Ulteriori [autorizzazioni multimediali granulari](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), a significare che puoi concedere l'accesso ai soli file immagine, video o audio.
- L'utilizzo in background dei sensori richiede adesso l'autorizzazione [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

Un'app potrebbe richiedere un'autorizzazione per una sua funzionalità specifica. Ad esempio, ogni app capace di scansionare i codici QR, richiederà l'autorizzazione all'utilizzo della fotocamera. Alcune app possono richiedere più autorizzazioni di quelle necessarie.

[Exodus](https://exodus-privacy.eu.org) può essere utile per confrontare applicazioni con scopi simili. Se un'app richiede molte autorizzazioni e contiene molti annunci e analisi, è probabilmente un brutto segno. Consigliamo di esaminare i singoli tracker e di leggerne le descrizioni piuttosto che limitarsi a **contarne il totale** e supporre che tutte le voci elencate siano uguali.

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Se un'app è prevalentemente un servizio basato su web, il tracciamento potrebbe verificarsi dal lato del server. [Facebook](https://reports.exodus-privacy.eu.org/it/reports/com.facebook.katana/latest/) mostra "nessun tracker", ma sicuramente traccia gli interessi e il comportamento degli utenti sul sito. Le app potrebbero eludere il rilevamento non utilizzando le librerie di codice standard prodotte dall'industria pubblicitaria, sebbene sia improbabile.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

Le applicazioni che rispettano la privacy come [Bitwarden](https://reports.exodus-privacy.eu.org/it/reports/com.x8bit.bitwarden/latest/) possono mostrare alcuni tracker come [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/it/trackers/49/). Questa libreria include [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) che può fornire [notifiche push](https://en.wikipedia.org/wiki/Push_technology) nelle app. Questo [è il caso] (https://fosstodon.org/@bitwarden/109636825700482007) di Bitwarden. That doesn't mean that Bitwarden is using all the analytics features that are provided by Google Firebase Analytics.

</div>

## Funzionalità per la Privacy

### Profili Utente

Multiple **user profiles** can be found in :gear: **Settings** → **System** → **Users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps. Ogni profilo è crittografato con la sua chiave crittografica e non può accedere ai dati di qualsiasi altro profilo. Anche il proprietario del dispositivo non può visualizzare i dati di altri profili, senza conoscerne la password. I profili utente multipli sono un metodo di isolamento più sicuro.

### Profilo di lavoro

[**Work Profiles**](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

Il profilo di lavoro dipende da un controllore del dispositivo per funzionare. Le funzionalità come *File Shuttle* e *blocco della ricerca dei contatti* o qualsiasi tipo di funzionalità d'isolamento, devono essere implementate dal controllore. È inoltre necessario fidarsi completamente dell'app di controllo del dispositivo, che ha pieno accesso ai dati dell'utente all'interno del profilo di lavoro.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the owner profile and work profile simultaneously.

### Private Space

**Private Space** is a feature introduced in Android 15 that adds another way of isolating individual apps. You can set up a private space in the owner profile by navigating to :gear: **Settings** → **Security & privacy** → **Private space**. Once set up, your private space resides at the bottom of the app drawer.

Like user profiles, a private space is encrypted using its own encryption key, and you have the option to set up a different unlock method. Like work profiles, you can use apps from both the owner profile and private space simultaneously. Apps launched from a private space are distinguished by an icon depicting a key within a shield.

Unlike work profiles, Private Space is a feature native to Android that does not require a third-party app to manage it. For this reason, we generally recommend using a private space over a work profile, though you can use a work profile alongside a private space.

### VPN kill switch

Android 7 e successivi supporta un kill switch VPN, disponibile senza la necessità d'installare applicazioni di terze parti. Questa funzionalità può prevenire fughe, se la VPN è disconnessa. Si trova in :gear: **Impostazioni** → **Rete e Internet** → **VPN** → :gear: → **Blocca connessioni senza VPN**.

### Interruttori globali

I dispositivi Android moderni dispongono di interruttori globali per disabilitare i servizi Bluetooth e della posizione. Android 12 ha introdotto gli interruttori per la fotocamera e il microfono. Quando non sono in uso, consigliamo di disabilitare queste funzionalità. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Servizi di Google

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play Services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.

### Programma di protezione avanzata

Se hai un account Google, ti suggeriamo di iscriverti al [Programma di protezione avanzata](https://landing.google.com/advancedprotection). È disponibile gratuitamente a costo zero per chiunque possieda due o più chiavi di sicurezza hardware con supporto a [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online). Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

Il Programma di Protezione Avanzata fornisce un migliore monitoraggio delle minacce, e consente:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](../basics/account-creation.md#sign-in-with-oauth)
- L'accesso ai dati del profilo soltanto a Google e alle app verificate di terze parti
- Scansione delle email in entrata sui profili Gmail, in cerca di tentativi di [phishing](https://en.wikipedia.org/wiki/Phishing#Email_phishing)
- Stricter [safe browser scanning](https://google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Processo di recupero più rigido per i profili con credenziali perdute

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949) such as:

- Non permette l'installazione di app al di fuori del Google Play Store, dell'app store del fornitore del sistema operativo o tramite [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Scansione automatica obbligatoria del dispositivo con [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Avviso sulle applicazioni non verificate
- Enabling ARM's hardware-based [Memory Tagging Extension (MTE)](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension) for supported apps, which lowers the likelihood of device exploits happening through memory corruption bugs

### Aggiornamenti di Sistema di Google Play

In passato, gli aggiornamenti di sicurezza di Android dovevano essere forniti dal fornitore del sistema operativo. Android è divenuto più modulare a partire da Android 10, e Google può inviare gli aggiornamenti di sicurezza push per **alcuni** componenti di sistema, tramite i Play Services privilegiati.

Se possiedi un dispositivo al termine della vita, distribuito con Android 10 o superiori e non riesci a eseguirvi nessuno dei nostri sistemi operativi, è probabile che sia meglio che ti attenga all'installazione di Android del tuo OEM (rispetto a un sistema operativo non elencato qui, come LineageOS o /e/ OS). Ciò ti consentirà di ricevere **alcune** correzioni di sicurezza da Google, senza però violare il modello di sicurezza di Android, utilizzando un derivato di Android non sicuro e incrementando la tua superficie di attacco. Consigliamo comunque di passare a un dispositivo supportato il prima possibile.

### ID pubblicitario

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248) used for targeted advertising. Disabilita questa funzionalità per limitare i dati raccolti su di te.

On Android distributions with [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **All services** → **Ads**.

- [x] Select **Delete advertising ID**

On Android distributions with privileged Google Play Services (which includes the stock installation on most devices), the setting may be in one of several locations. Controlla

- :gear: **Impostazioni** → **Google** → **Pubblicità**
- :gear: **Impostazioni** → **Privacy** → **Pubblicità**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. Altrimenti, assicurati di rinunciare e di ripristinare il tuo ID pubblicitario.

### SafetyNet e API di Play Integrity

[SafetyNet](https://developer.android.com/training/safetynet/attestation) e le [API di Play Integrity](https://developer.android.com/google/play/integrity) sono generalmente utilizzati per le [app bancarie](https://grapheneos.org/usage#banking-apps). Molte app bancarie funzioneranno bene su GrapheneOS con i servizi Play in modalità sandbox, tuttavia, alcune app non finanziarie dispongono di meccanismi anti-manomissione che potrebbero fallire. GrapheneOS supera il controllo `basicIntegrity`, ma non il controllo del certificato `ctsProfileMatch`. I dispositivi con Android 8 o successive, dispongono di supporto dell'attestazione del hardware, non superabile con chiavi trapelate o gravi vulnerabilità.

Per quanto riguarda Google Wallet, lo sconsigliamo a causa della loro [informativa sulla privacy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), che prevede che l'utente debba rinunciare se non vuole che il suo rating creditizio e le sue informazioni personali siano condivise con i servizi di marketing affiliati.
