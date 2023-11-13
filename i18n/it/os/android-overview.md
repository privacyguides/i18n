---
title: Panoramica Android
icon: simple/android
description: Android è un sistema operativo open source con forti protezioni per la sicurezza, il che lo rende la nostra scelta migliore, per la telefonia.
---

![Logo di Android](../assets/img/android/android.svg){ align=right }

Il **Progetto Open Source di Androd** è un sistema operativo mobile sicuro, che dispone di una forte [modalità sandbox delle app](https://source.android.com/security/app-sandbox), [Avvio Verificato](https://source.android.com/security/verifiedboot) (AVB) e di un robusto sistema di controllo delle [autorizzazioni](https://developer.android.com/guide/topics/permissions/overview).

## I nostri consigli

### Scegliere una distribuzione di Android

When you buy an Android phone, the default operating system comes bundled with apps and functionality that are not part of the Android Open Source Project. Many of these apps—even apps like the dialer which provide basic system functionality—require invasive integrations with Google Play Services, which in turn asks for privileges to access your files, contacts storage, call logs, SMS messages, location, camera, microphone, and numerous other things on your device in order for those basic system apps and many other apps to function in the first place. Frameworks like Google Play Services increase the attack surface of your device and are the source of various privacy concerns with Android.

Questo problema potrebbe essere risolto utilizzando una distribuzione modificata di Android che non preveda un'integrazione così invasiva. Purtroppo, molte distribuzioni di Android personalizzate spesso violano il modello di sicurezza di Android, non supportando funzioni di sicurezza critiche come AVB, protezione rollback, aggiornamenti del firmware e così via. Alcune distribuzioni forniscono anche build [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) che espongono root tramite [ADB](https://developer.android.com/studio/command-line/adb) e richiedono politiche SELinux [più permissive](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) per ospitare le funzionalità di debug, con conseguente ulteriore aumento della superficie di attacco e indebolimento del modello di sicurezza.

Idealmente, quando si sceglie una distribuzione modificata di Android, bisogna assicurarsi che rispetti il modello di sicurezza Android. Come minimo, la distribuzione dovrebbe avere build di produzione, supporto per AVB, protezione dal rollback, aggiornamenti tempestivi del firmware e del sistema operativo e SELinux in [modalità enforcing](https://source.android.com/security/selinux/concepts#enforcement_levels). Tutte le distribuzioni di Android da noi consigliate soddisfano questi criteri.

[Le nostre raccomandazioni per il sistema Android :material-arrow-right-drop-circle:](../android.md ""){.md-button}

### Evitare il rooting

Il [rooting](https://it.wikipedia.org/wiki/Rooting) dei telefoni Android può diminuire notevolmente la sicurezza in quanto indebolisce nel complesso il [modello di sicurezza di Android](https://it.wikipedia.org/wiki/Android#Privacy_e_sicurezza). Ciò può ridurre la privacy in caso di exploit assistito dalla sicurezza ridotta. I metodi di rooting comuni richiedono la manomissione diretta della partizione d'avvio, rendendo impossibile l'esecuzione corretta dell'Avvio Verificato. Le app che richiedono root, inoltre, modificheranno la partizione di sistema, a significare che l'Avvio Verificato dovrebbe rimanere disabilitato. Esporre il root direttamente nell'interfaccia utente, inoltre, incrementa la [superficie d'attacco](https://en.wikipedia.org/wiki/Attack_surface) del tuo dispositivo e potrebbe favorire le vulnerabilità d'[intensificazione del privilegio](https://en.wikipedia.org/wiki/Privilege_escalation) e aggiramenti della politica di SELinux.

I blocchi di annunci, che modificano il [file degli host](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) e i firewall (AFWall+) che richiedono l'accesso persistente al root, sono pericolosi e non dovrebbero essere utilizzati. Inoltre, sono il modo errato per risolvere i loro scopi. Per il blocco degli annunci, piuttosto, suggeriamo soluzioni di blocco dei server [DNS](../dns.md) crittografati o una [VPN](../vpn.md). RethingDNS, TrackerControl e AdAway in modalità non di root, occuperanno lo slot della VPN (utilizzando una VPN di loopback locale), impedendoti di utilizzare i servizi di miglioramento della privacy, come Orbot o un vero server VPN.

AFWall+ opera secondo l'approccio di [filtraggio dei pacchetti](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) e potrebbe essere aggirabile in certe situazioni.

Non crediamo che i sacrifici di sicurezza effettuati dal rooting di un telefono, valgano i discutibili benefici della privacy di tali app.

### Installare Aggiornamenti

È importante non utilizzare una versione di Android arrivata al [termine della sua vita](https://endoflife.date/android). Le più recenti versioni di Android non soltanto ricevono gli aggiornamenti di sicurezza per il sistema operativo, ma anche importanti aggiornamenti di miglioramento della privacy.

Ad esempio, [prima di Android 10](https://developer.android.com/about/versions/10/privacy/changes), qualsiasi app avente l'autorizzazionee [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) poteva accedere a numeri di serie univoci e sensibili del tuo telefono, quali l'[IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), il [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), o l'[IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity) della tua scheda SIM; mentre ora soltanto le app di sistema possono farlo. Le app di sistema sono fornite soltanto dall'OEM o dalla distribuzione di Android.

### Condividere Media

Puoi evitare di consentire a molte app l'autorizzazione d'accesso ai tuoi file multimediali, con le funzionalità di condivisione integrate di Android. Molte applicazioni ti consentono di "condividere" un file con esse, tramite caricamento dello stesso.

Ad esempio, se desideri pubblicare un'immagine su Discord, puoi aprire il tuo gestore di file o galleria e condividerla con l'app di Discord, invece di concedere a Discord l'accesso completo ai tuoi file multimediali e foto.

## Protezioni di Sicurezza

### Avvio Verificato

L'[Avvio Verificato](https://source.android.com/security/verifiedboot) è una parte importante del modello di sicurezza di Android. Fornisce protezione dagli attacchi di [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack), la persistenza del malware e assicura che gli aggiornamenti di sicurezza non siano rimuovibili con la [protezione da rollback](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

Android 10 e superiori si sono allontanati dalla crittografia dell'intero disco, verso una [crittografia basata sui file](https://source.android.com/security/encryption/file-based) più sicura. I tuoi dati sono crittografati utilizzando chiavi crittografiche univoce e il file del sistema operativo sono lasciati non crittografati.

L'Avvio Verificato assicurare l'integrità dei file del sistema operativo, dunque impedendo a un avversario con l'accesso fisico, di manomettere o installare malware sul dispositivo. Nell'improbabile caso in cui il malware possa sfruttare altre parti del sistema e ottenere accesso privilegiato superiore, l'Avvio Verificato impedirà e ripristinerà le modifiche alla partizione di sistema, al riavvio del dispositivo.

Sfortunatamente, gli OEM devono supportare l'Avvio Verificato sulla propria distribuzione Android stock. Solo alcuni OEM, come Google, supportano la registrazione di chiavi AVB personalizzate sui propri dispositivi. Inoltre, alcuni AOSP derivati come LineageOS o /e/ OS, non supportano l'Avvio Verificato anche su hardware che lo supporta, per i sistemi operativi di terze parti. Ti consigliamo di verificare il supporto **prima** di acquistare un nuovo dispositivo. I derivati AOSP che non supportano l'Avvio Verificto **non** sono consigliati.

Inoltre, molti OEM dispongono di un'implementazione corrotta dell'Avvio Verificato, di cui devi essere consapevole, al di là del loro marketing. Ad esempio, i Fairphone 3 e 4 non sono sicuri di default, poiché il [bootloader di fabbrica si fida della chiave di firma AVB pubblica](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). Ciò invalida l'avvio verificato su un dispositivo di fabbrica Fairphone, poiché il sistema avvierà i sistempi operativi Android alternativi (come /e/) [senza alcun avviso](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) sull'utilizzo del sistema operativo personalizzato.

### Aggiornamenti del firmware

Gli aggiornamenti del firmware sono fondamentali per mantenere la sicurezza e, senza di essi, il tuo dispositivo non può essere sicuro. Gli OEM stipulano accordi di supporto coi propri partner per fornire i componenti closed-source per un periodo di supporto limitato. Questi sono mensilmente riportati nei [Bollettini di Sicurezza di Android](https://source.android.com/security/bulletin).

Poiché i componenti del telefono, come il processore e le tecnologie radio, si affidano a componenti closed-source, gli aggiornamenti devono essere forniti dai rispettivi produttori. Dunque, è importante che tu acquisti un dispositivo entro un ciclo di supporto attivo. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) e [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) supportano i propri dispositivi per 4 anni, mentre i prodotti più economici prevedono spesso cicli di supporto più brevi. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

I dispositivi EOL, non più supportati dal produttore del SoC, non possono ricevere aggiornamenti del firmware dai fornitori OEM o dai distributori di ricambi per Android. Ciò significa che i problemi di sicurezza di questi dispositivi non saranno risolti.

Fairphone, for example, markets their Fairphone 4 device as receiving 6 years of support. Tuttavia, il SoC (Qualcomm Snapdragon 750G sul Fairphone 4), ha una data di scadenza considerevolmente più breve. Ciò significa che gli aggiornamenti di sicurezza di quel firmware da Qualcomm per il Fairphone 4 termineranno a settembre 2023, indipendentemente dal fatto che Fairphone continui a rilasciare aggiornamenti di sicurezza del software.

### Autorizzazioni di Android

[Le autorizzazioni su Android](https://developer.android.com/guide/topics/permissions/overview) ti garantiscono il controllo su quali app hanno accesso. Google apporta [miglioramenti](https://developer.android.com/about/versions/11/privacy/permissions) regolari al sistema di autorizzazioni, in ogni nuova versione. Tutte le app che installi sono rigorosamente [testate](https://source.android.com/security/app-sandbox), dunque, non è necessario installare alcuna app di antivirus.

Uno smartphone con la versione più recente di Android sarà sempre più sicuro di un vecchio smartphone con un antivirus a pagamento. È meglio non pagare un software antivirus e risparmiare soldi per acquistare un nuovo smartphone, come un Google Pixel.

Android 10:

- L'[Archiviazione Esaminata](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) ti conferisce maggiore controllo sui file e può limitare ciò che può [accedere all'archiviazione esterna](https://developer.android.com/training/data-storage#permissions). Le app possono avere una cartella specifica nell'archiviazione esterna, nonché l'abilità di memorizzarvi tipi specifici di file multimediali.
- Accesso più ristretto alla [posizione del dispositivo](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location), introducendo l'autorizzazione `ACCESS_BACKGROUND_LOCATION`. Questa impedisce alle app di accedere alla posizione quando in esecuzione in background, senza l'espressa autorizzazione dall'utente.

Android 11:

- [Autorizzazioni una tantum](https://developer.android.com/about/versions/11/privacy/permissions#one-time), che ti consentono di concedere un'autorizzazione a un'app, una singola volta.
- [Ripristino automatico delle autorizzazioni](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset), che ripristina i [permessi in esecuzione](https://developer.android.com/guide/topics/permissions/overview#runtime), concessi all'apertura dell'app.
- Autorizzazioni granulari pre accedere alle funzionalità correlate al [numero telefonico](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers).

Android 12:

- Un'autorizzazione per concedere soltanto la [posizione approssimativa](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- Ripristino automatico delle [app ibernate](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation).
- [Controllo dell'accesso ai dati](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing), che semplifica la determinazione di quale parte di un'app sta eseguendo un certo tipo di accesso ai dati.

Android 13:

- A permission for [nearby Wi-Fi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points was a popular way for apps to track a user's location.
- Ulteriori [autorizzazioni multimediali granulari](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), a significare che puoi concedere l'accesso aai soli filee immagine, video o audio.
- L'utilizzo in background dei sensori richiede adesso l'autorizzazione [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

Un'app potrebbe richiedere un'autorizzazione per una sua funzionalità specifica. Ad esempio, ogni app capace di scansionare i codici QR, richiederà l'autorizzazione all'utilizzo della fotocamera. Alcune app possono richiedere più autorizzazioni di quelle necessarie.

[Exodus](https://exodus-privacy.eu.org/) può essere utile se devi confrontare app con scopi simili. Se un'app richiede molte autorizzazioni e contiene molti annunci e analisi, è probabilmente un brutto segno. Consigliamo di esaminare i singoli tracker e di leggerne le descrizioni piuttosto che limitarsi a **contarne il totale** e supporre che tutte le voci elencate siano uguali.

!!! warning

    Se un'app è prevalentemente un servizio basato su web, il tracciamento potrebbe verificarsi dal lato del server. [Facebook](https://reports.exodus-privacy.eu.org/it/reports/com.facebook.katana/latest/) mostra "nessun tracciatore", ma traccia sicuramente gli interessi e comportamenti degli utenti sul sito. Le app potrebbero eludere il rilevamento non utilizzando le librerie di codice standard prodotte dall'industria pubblicitaria, sebbene sia improbabile.

!!! note "Nota"

    Le app che rispettano la privacy come [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/) potrebbero mostrare dei tracciatori come [Google Firebase Analytics](https://reports.exodus.privacy.eu.org/en/trackers/49/). Questa libreria include [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) che può fornire [notifiche push](https://en.wikipedia.org/wiki/Push_technology) nelle app. Questo [è il caso] (https://fosstodon.org/@bitwarden/109636825700482007) di Bitwarden. Ciò non significa che Bitwarden sta utilizzando tutte le funzionalità analitiche fornite da Google Firebase Analytics.

## Funzionalità per la Privacy

### Profili Utente

I profili utente multipli si trovano in **Impostazioni** → **Sistema** → **Utenti multipli** e sono il metodo più semplice per isolare in Android.

Con i profili utente, puoi imporre limitazioni a un profilo specifico, come: effettuare chiamate, utilizzare gli SMS o installare app sul dispositivo. Ogni profilo è crittografato con la sua chiave crittografica e non può accedere ai dati di qualsiasi altro profilo. Anche il proprietario del dispositivo non può visualizzare i dati di altri profili, senza conoscerne la password. I profili utente multipli sono un metodo di isolamento più sicuro.

### Profilo di lavoro

I [Profili di Lavoro](https://support.google.com/work/android/answer/6191949) sono un altro metodo per isolare le singole app e potrebbe essere più comodo dei profili utente separati.

Un'app di **controllo del dispositivo**, come [Shelter](../android.md#shelter), è necessaria per creare un Profilo di Lavoro senza un MDM imprenditoriale, a meno che tu non stia utilizzando un OS personalizzato di Android che ne includa uno.

Il profilo di lavoro dipende da un controllore del dispositivo per funzionare. Le funzionalità come *File Shuttle* e *blocco della ricerca dei contatti* o qualsiasi tipo di funzionalità d'isolamento, devono essere implementate dal controllore. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

Questo metodo, generalmente, è meno sicuro di un profilo utente secondario; tuttavia, ti consente la comodità di eseguire le app nei profili lavorativi e personali, simultaneamente.

### Interruttore d'Emergenza per VPN

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. Questa funzionalità può prevenire fughe, se la VPN è disconnessa. Si trova in :gear: **Impostazioni** → **Rete e Internet** → **VPN** → :gear: → **Blocca connessioni senza VPN**.

### Interruttori globali

I dispositivi Androiid moderni dispongono di interruttori globali per disabilitare i servizi Bluetooth e della posizione. Android 12 ha introdotto gli interruttori per la fotocamera e il microfono. Quando non sono iin uso, consigliamo di disabilitare queste funzionalità. Le app non possono utilizzare le funzionalità disabilitate (anche se la singola autorizzazione è concessa), finché non sono riabilitate.

## Servizi di Google

Se utilizzi un dispositivo provvisto dei servizi di Google, il tuo sistema operativo di fabbrica o un sistema operativo che mette in sicurezza Google Play Services, come GrapheneOS, esistono numerose modifiche aggiuntive che puoi effettuare per migliorare la tua privacy. Comunque, consigliamo di evitare interamente i servizi di Google, o di limitare Google Play Services a un profilo dell'utente/di lavoro specifico, combinando un controllore del dispositivo come *Shelter*, con il Google Play di GrapheneOS.

### Programma di protezione avanzata

Se possiedi un profilo Google, ti suggeriamo di iscriverti al [Programma di Protezione Avanzata](https://landing.google.com/advancedprotection/). È disponibile gratuitamente a costo zero per chiunque possieda due o più chiavi di sicurezza hardware con supporto a [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online).

Il Programma di Protezione Avanzata fornisce un migliore monitoraggio delle minacce, e consente:

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- L'accesso ai dati del profilo soltanto a Google e alle app verificate di terze parti
- Scansione delle email in entrata sui profili Gmail, in cerca di tentativi di [phishing](https://en.wikipedia.org/wiki/Phishing#Email_phishing)
- [Scansione del browser sicura](https://www.google.com/chrome/privacy/whitepaper.html#malware) e più rigida, con Google Chrome
- Processo di recupero più rigido per i profili con credenziali perdute

 Se utilizzi Google Play Services non 'sandboxed' (comune sui sistemi operativi di fabbrica), il Programma di Protezione Avanzata fornisce anche dei [benefici aggiuntivi](https://support.google.com/accounts/answer/9764949?hl=en), come:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Scansione del dispositivo automatica e obbligatoria con [Play Protect](https://support.google.com/googleplay/answer/2812853?hl=en#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Avviso sulle applicazioni non verificate

### Aggiornamenti di Sistema di Google Play

In passato, gli aggiornamenti di sicurezza di Android dovevano essere forniti dal fornitore del sistema operativo. Android è divenuto più modulare a partire da Android 10, e Google può inviare gli aggiornamenti di sicurezza push per **alcuni** componenti di sistema, tramite i Play Services privilegiati.

Se possiedi un dispositivo al termine della vita, distribuito con Android 10 o superiori e non riesci a eseguirvi nessuno dei nostri sistemi operativi, è probabile che sia meglio che ti attenga all'installazione di Android del tuo OEM (rispetto a un sistema operativo non elencato qui, come LineageOS o /e/ OS). Ciò ti consentirà di ricevere **alcune** correzioni di sicurezza da Google, senza però violare il modello di sicurezza di Android, utilizzando un derivato di Android non sicuro e incrementando la tua superficie di attacco. Consigliamo comunque di passare a un dispositivo supportato il prima possibile.

### ID pubblicitario

Tutti i dispositivi con Google Play Services installata automaticamente, generano un [ID pubblicitario](https://support.google.com/googleplay/android-developer/answer/6048248?hl=en), utilizzando per la pubblicità mirata. Disabilita questa funzionalità per limitare i dati raccolti su di te.

Sulle distribuzioni Android con [Google Play in modalità sandbox](https://grapheneos.org/usage#sandboxed-google-play), vai su :gear: **Impostazioni** → **App** → **Sandboxed Google Play** → **Impostazioni di Google** → **Pubblicità** e seleziona *Elimina ID pubblicitario*.

Sulle distribuzioni di Android con Google Play Services privilegiati (come gli OS di fabbrica), l'impostazione potrebbe trovarsi in una delle seguenti, svariate posizioni. Controlla

- :gear: **Impostazioni** → **Google** → **Pubblicità**
- :gear: **Impostazioni** → **Privacy** → **Pubblicità**

Potrai eliminare il tuo ID pubblicitario o *Rinunciare agli annunci basati sugli interessi*, a seconda delle distribuzioni OEM di Android. L'opzione di eliminare l'ID pubblicitario, se presente, è preferibile. Altrimenti, assicurati di rinunciare e di ripristinare il tuo ID pubblicitario.

### SafetyNet e API di Play Integrity

[SafetyNet](https://developer.android.com/training/safetynet/attestation) e le [API di Play Integrity](https://developer.android.com/google/play/integrity) sono generalmente utilizzati per le [app bancarie](https://grapheneos.org/usage#banking-apps). Molte app bancarie funzioneranno bene su GrapheneOS con i servizi Play in modalità sandbox, tuttavia, alcune app non finanziarie dispongono di meccanismi anti-manomissione che potrebbero fallire. GrapheneOS supera il controllo `basicIntegrity`, ma non il controllo del certificato `ctsProfileMatch`. I dispositivi con Android 8 o successive, dispongono di supporto dell'attestazione del hardware, non superabile con chiavi trapelate o gravi vulnerabilità.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
