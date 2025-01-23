---
title: Panoramica su iOS
icon: simple/apple
description: iOS è un sistema operativo mobile sviluppato da Apple per l'iPhone.
---

**iOS** e **iPadOS** sono sistemi operativi mobili proprietari sviluppati da Apple per i propri prodotti, iPhone e iPad, rispettivamente. Se possiedi un dispositivo mobile Apple, puoi incrementare la tua privacy disabilitando alcune funzionalità di telemetria integrate e rafforzando alcune impostazioni per la privacy e la sicurezza, integrate sul sistema.

## Note sulla Privacy

iOS devices are frequently praised by security experts for their robust data protection and adherence to modern best practices. Tuttavia, le restrizioni dell'ecosistema di Apple, in particolare per quanto riguarda i dispositivi mobili, ostacolano ancora la privacy in diversi modi.

Generalmente, consideriamo che iOS fornisca protezioni della privacy e della sicurezza migliori della media per gran parte delle persone, rispetto ai dispositivi Android di fabbrica da qualsiasi produttore. However, you can achieve even higher standards of privacy with a [custom Android operating system](../android/distributions.md) like GrapheneOS, if you want or need to be completely independent of Apple or Google's cloud services.

### Blocco di Attivazione

Tutti i dispositivi iOS devono essere confrontati con i server di Activation Lock di Apple, quando configurati inizialmente o ripristinati, a significare che è **necessaria** una connessione a Internet per utilizzare un dispositivo iOS.

### App Store Obbligatorio

The only source for apps on iOS is Apple's App Store, which requires an Apple Account to access. Ciò significa che Apple detiene un registro di qualsiasi app tu installi sul tuo dispositivo e, probabilmente, potrebbe collegare tali informazioni alla tua identità reale, se fornisci un metodo di pagamento all'App Store.

### Telemetria Invadente

Apple has historically had problems with properly disassociating their telemetry from Apple Accounts on iOS. In [2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), Apple was found to transmit Siri recordings—some containing highly confidential information—to their servers for manual review by third-party contractors. Though Apple temporarily stopped that program after that practice was [widely reported on](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), the company rolled out a switch to [**opt out** of uploading conversations with Siri](https://theguardian.com/technology/2019/oct/30/apple-lets-users-opt-out-of-having-siri-conversations-recorded) a few months later in the succeeding iOS update. Moreover, in 2021, [Apple reworked Siri](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance) so that it processes voice recordings locally rather than sending it to their servers.

More recently, Apple has been found to transmit analytics [even when analytics sharing is disabled](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) on iOS, and this data [appears](https://twitter.com/mysk_co/status/1594515229915979776) to be easily linked to unique iCloud account identifiers despite supposedly being decoupled from Apple Accounts.

### Traffic Outside Active VPN Connections

Apple's [privacy policy regarding VPNs](https://apple.com/legal/privacy/data/en/vpns) states:

> Even when a VPN is active, some traffic that is necessary for essential system services will take place outside the VPN so that your device can function properly.

## Configurazione consigliata

**Note:** This guide assumes that you're running the latest version of iOS.

### iCloud

Gran parte delle preoccupazioni su privacy e sicurezza con i prodotti di Apple sono correlate ai loro servizi su cloud, non al loro hardware o software. Quando utilizzi i servizi di Apple come iCloud, gran parte delle tue informazioni sono archiviate sui loro server e protette con chiavi, cui Apple ha accesso di default. Puoi consultare la [documentazione di Apple](https://support.apple.com/HT202303) per le informazioni su quali servizi sono crittografati end-to-end. Qualsiasi cosa sia elencata come "in transito" o "sul server", indica che è possibile, per Apple, accedere a tali dati senza la tua autorizzazione. Questo livello d'accesso è stato occasionalmente abusato dalle autorità per aggirare il fatto che i tuoi dati sono altrimenti crittografati in sicurezza sul tuo dispositivo e, ovviamente, Apple è vulnerabile alle violazioni di dati, come ogni altra azienda.

Dunque, se utilizzi iCloud, dovresti [abilitare la **Protezione Avanzata dei Dati**](https://support.apple.com/HT212520). Questa, crittografa praticamente tutti i tuoi dati di iCloud con chiavi memorizzate sui tuoi dispositivi (crittografia end-to-end), piuttosto che sui server di Apple, così che i tuoi dati di iCloud siano protetti nel caso di una violazione di dati, e altrimenti nascosti da Apple.

La crittografa utilizzata dalla Protezione Avanzata dei Dati, sebbene forte, [non è *altrettanto* robusta](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4), quanto quella offerta da altri [servizi su cloud](../cloud.md), in particolare per quanto riguarda iCloud Drive. Sebbene incoraggiamo vivamente all'utilizzo della Protezione Avanzata dei Dati se utilizzi iCloud, suggeriremmo anche di considerare di trovare un'alternativa a iCloud, da un [fornitore del servizio più orientato alla privacy](../tools.md), sebbene sia improbabile che, gran parte delle persone, sarebbero influenzate da queste stranezze crittografiche.

Inoltre, in primo luogo, puoi proteggere i tuoi dati limitando ciò che sincronizzi su iCloud. In cima all'app delle **Impostazioni**, visualizzerai il tuo nome e la tua foto di profilo, se sei iscritto su iCloud. Selezionalo, poi **iCloud**, quindi disattiva gli interruttori per qualsiasi servizio tu desideri non sia sincronizzato con iCloud. Potresti visualizzare delle app di terze parti, elencate in **Mostra tutto**, se si sincronizzano con iCloud, che potrai disabilitare da qui.

#### iCloud+

Un abbonamento a pagamento a **iCloud+** (con qualsiasi piano di archiviazione su iCloud), fornisce alcune funzionalità di protezione della privacy. While these may provide adequate service for current iCloud customers, we wouldn't recommend purchasing an iCloud+ plan over a [VPN](../vpn.md) and [standalone email aliasing service](../email-aliasing.md) just for these features alone.

[**Private Relay**](https://apple.com/legal/privacy/data/en/icloud-relay) is a proxy service which relays all of your Safari traffic, your DNS queries, and unencrypted traffic on your device through two servers: one owned by Apple and one owned by a third-party provider (including Akamai, Cloudflare, and Fastly). In teoria, ciò dovrebbe impedire a qualsiasi singolo fornitore nella catena, Apple inclusa, dall'avere una piena visibilità di quali siti web visiti mentre sei connesso. Unlike a VPN, Private Relay does not protect traffic that's already encrypted.

**Hide My Email** è il servizio di alias email di Apple. Puoi creare un alias email gratuitamente quando *Accedi Con Apple* su un sito web o un'app, o generarne di illimitati su richiesta, con un piano iCloud+ a pagamento. Hide My Email ha il vantaggio di utilizzare il dominio `@icloud.com` per i propri alias, riducendo la probabilità di essere bloccato rispetto ad altri servizi di alias email, ma non offrendo le funzionalità offerte dai servizi indipendenti, come la crittografia PGP automatica o il supporto a più caselle.

#### Media e Acquisti

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. Select that, then select **Media & Purchases** → **View Account**.

- [ ] Disattiva i **Consigli Personalizzati**

#### Find My

**Find My** è un servizio che ti consente di tracciare i tuoi dispositivi Apple e di condividere la tua posizione con i tuoi amici e la tua famiglia. Inoltre, ti consente di svuotare da remoto il tuo dispositivo, in caso di furto, impedendo ai ladri di accedere ai tuoi dati. Your Find My [location data is E2EE](https://apple.com/legal/privacy/data/en/find-my) when:

- Your location is shared with a family member or friend, and you both use iOS 17 or greater.
- Il tuo dispositivo è offline ed è individuato dalla Rete di Find My.

I tuoi dati sulla posizione non sono E2EE quando il tuo dispositivo è online e utilizzi Find My iPhone da remoto, per individuare il tuo dispositivo. Dovrai decidere se mantenere questi compromessi valga i vantaggi antifurto del Blocco di Attivazione.

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. Selezionalo, quindi seleziona **Find My**. Qui puoi scegliere se abilitare o disabilitare le funzionalità di posizione di Find My.

### Settings

Molte altre impostazioni correlate alla privacy si possono trovare nell'app delle **Impostazioni**.

#### Modalità Aereo

Abilitare la **Modalità Aereo** impedisce al tuo telefono di contattare le torri cellulari. Potrai comunque connetterti alla Wi-Fi e al Bluetooth, quindi, ogni volta che sei connesso alla Wi-Fi, potrai attivare quest'impostazione.

#### Wi-Fi

You can enable [hardware address randomization](https://support.apple.com/en-us/102509#triswitch) to protect you from tracking across Wi-Fi networks, and on the same network over time. On the network you are currently connected to, tap the :material-information: button:

- [x] Set **Private Wi-Fi Address** to **Fixed** or **Rotating**

Inoltre, puoi **Limitare il Tracciamento dell'Indirizzo IP**. Ciò somiglia alla Trasmissione Privata di iCloud, ma riguarda soltanto le connessioni ai "tracciatori noti." Poiché riguarda soltanto le connessioni a server potenzialmente dannosi, quest'impostazione può tranquillamente esser lasciata abilitata, ma se desideri che *qualsiasi* traffico non sia indirizzato attraverso i server di Apple, dovresti disattivarla.

#### Bluetooth

Il **Bluetooth** dovrebbe essere disabilitato quando non lo stai utilizzando, poiché incrementa la superficie d'attacco. Disabilitare il Bluetooth (o la Wi-Fi) tramite il Centro di Controllo, lo disabilita soltanto temporaneamente: devi disattivarlo nelle Impostazioni, affinché ciò resti effettivo.

- [ ] Disattiva il **Bluetooth**

Note that Bluetooth is automatically turned on after every system update.

#### Generali

Il nome del tuo dispositivo iPhone conterrà di default il tuo nome e, questo, sarà visibile a chiunque, sulle reti cui ti connetti. Dovresti modificarlo in qualcosa di più generico, come "iPhone." Select **About** → **Name** and enter the device name you prefer.

È importante installare frequentemente gli **Aggiornamenti Software**, per ottenere le più recenti correzioni di sicurezza. Puoi abilitare gli **Aggiornamenti Automatici** per mantenere aggiornato il tuo telefono, senza dover controllare costantemente la presenza di aggiornamenti. Select **Software Update** → **Automatic Updates**:

- [x] Attiva **Scarica Aggiornamenti iOS**
- [x] Attiva **Installa Aggiornamenti iOS**
- [x] Attiva **Risposte di Sicurezza e File di Sistema**

**AirDrop** is commonly used to easily share files, but it represents a significant privacy risk. The AirDrop protocol constantly broadcasts your personal information to your surroundings, with [very weak](https://www.usenix.org/system/files/sec21-heinrich.pdf) security protections. Your identity can easily be discovered by attackers even with limited resources, and the Chinese government has [openly acknowledged](https://arstechnica.com/security/2024/01/hackers-can-id-unique-apple-airdrop-users-chinese-authorities-claim-to-do-just-that/) using such techniques to identify AirDrop users in public since 2022.

- [x] Select **AirDrop** → **Receiving Off**

**AirPlay** ti consente di trasmettere facilmente i contenuti dal tuo iPhone a una TV; tuttavia, potresti non desiderarlo fare sempre. Select **AirPlay & Continuity** → **Automatically AirPlay**:

- [x] Seleziona **Mai** o **Chiedi**

**Background App Refresh** consente alle tue app di aggiornare i propri contenuti, mentre non le stai utilizzando. Ciò potrebbe causare che si creino connessioni indesiderate. Turning this off can also save battery life, but may affect an app's ability to receive updated information, particularly weather and messaging apps.

Seleziona **Background App Refresh** e disattiva qualsiasi app non desideri continui ad aggiornarsi in background. Se desideri che nessuna app si aggiorni in background, puoi selezionare **Background App Refresh** e **disattivarla**.

#### Siri e Ricerca

Se non desideri che qualcuno possa controllare il tuo telefono con Siri, quando è bloccato, puoi disattivarlo qui.

- [ ] Disattiva **Consenti Siri Quando Bloccato**

#### Face ID/Touch ID e Passcode

Impostare una password forte sul tuo telefono è il passo più importante che puoi intraprendere per la sicurezza fisica del dispositivo. In questo caso dovrai trovare un compromesso tra la sicurezza e la comodità: una password più lunga sarà noiosa da digitare ogni volta, ma una password o un PIN più breve sarà più facile da indovinare. Configurare Face ID o TouchID insieme a una password forte, può costituire un buon compromesso tra utilizzabilità e sicurezza.

Select **Turn Passcode On** or **Change Passcode** → **Passcode Options** → **Custom Alphanumeric Code**. Make sure that you create a [secure password](../basics/passwords-overview.md).

Se desideri utilizzare Face ID o Touch ID, puoi ora procedere alla configurazione. Il tuo telefono utilizzerà la password configurata in precedenza come ripiego, nel caso in cui la tua verifica biometrica dovesse fallire. I metodi biometrici di sblocco sono principalmente una comodità, sebbene impediscano alle telecamere di sicurezza o alle persone alle tue spalle di guardarti inserire il tuo codice d'accesso.

Se utilizzi la biometria, dovresti sapere come disattivarla rapidamente in caso d'emergenza. Tenere premuto il tasto laterale o di accensione e *uno dei* tasti del volume, finché non visualizzi il cursore Scorri per Spegnere, disabiliterà la biometria, richiedendo il codice d'accesso per sbloccare. Inoltre, il tuo codice di sicurezza sarà richiesto al riavvio del dispositivo.

On some older devices, you may have to press the power button five times to disable biometrics instead, or for devices with Touch ID, you may just have to hold down the power button and nothing else. Assicurati di provare in anticipo, così da sapere quale metodo funziona per il tuo dispositivo.

**Stolen Device Protection** adds additional security intended to protect your personal data if your device is stolen while unlocked. If you use biometrics and the Find My Device feature in your Apple Account settings, we recommend enabling this new protection:

- [x] Seleziona **Attiva la protezione**

After enabling Stolen Device Protection, [certain actions](https://support.apple.com/HT212510) will require biometric authentication without a password fallback (in the event that a shoulder surfer has obtained your PIN), such as using password autofill, accessing payment information, and disabling Lost Mode. It also adds a security delay to certain actions performed away from your home or another "familiar location," such as requiring a 1-hour timer to reset your Apple Account password or sign out of your Apple Account. Questo ritardo ha lo scopo di dare all'utente il tempo di attivare la Modalità smarrito e di proteggere il proprio account prima che un ladro possa resettare il dispositivo.

**Consenti Accesso Da Bloccato** ti offre delle opzioni per consentire l'accesso quando il telefono è bloccato. Più di queste opzioni disabiliti, minori saranno le azioni disponibili a qualcuno senza la tua password, ma meno comodo sarà per te. Seleziona e scegli quali di queste non desideri siano accessibili a qualcuno, qualora dovesse impossessarsi del tuo telefono.

- [ ] Disattiva **Oggi e Ricerca**
- [ ] Disattiva **Centro Notifiche**
- [ ] Disattiva **Centro di Controllo**
- [ ] Disattiva **Widget del Blocco Schermo**
- [ ] Disattiva **Siri**
- [ ] Disattiva **Rispondi con Messaggio**
- [ ] Disattiva **Controllo Home**
- [ ] Disattiva il **Portafoglio**
- [ ] Disattiva **Richiama Chiamate Perse**
- [ ] Disattiva gli **Accessori USB**

Gli iPhone sono già resistenti agli attacchi di forza bruta, facendoti attendere abbastanza a lungo dopo più tentativi falliti; tuttavia, storicamente, sono esistiti degli exploit per aggirare tale problema. Per una maggiore sicurezza, puoi impostare il tuo telefono perché si ripristini da solo, dopo 10 tentativi falliti di inserimento del codice d'accesso.

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Con quest'impostazione abilitata, qualcuno potrebbe ripristinare intenzionalmente il tuo telefono, inserendo molte volte la password errata. Assicurati di avere dei backup adeguati e di abilitare quest'impostazione soltanto se ti senti a tuo agio nel farlo.

</div>

- [x] Attiva **Cancella Dati**

#### Privacy e sicurezza

I **Servizi di Posizione** ti consentono di utilizzare funzionalità come Find My e Maps. Se non necessiti di queste funzionalità, puoi disabilitare i Servizi di Posizione. Altrimenti, puoi revisionare e selezionare quali app possono utilizzare la tua posizione. Seleziona i **Servizi di Posizione**:

- [ ] Disattiva i **Servizi di Posizione**

A purple arrow will appear next to an app in these settings that has used your location recently, while a gray arrow indicates that your location has been accessed within the last 24 hours. If you decide to leave Location Services on, Apple will use it for System Services by default. You can review and pick which services can use your location here. However, if you don't want to submit location analytics to Apple, which they use to improve Apple Maps, you can disable this here as well. Select **System Services**:

- [ ] Turn off **iPhone Analytics**
- [ ] Turn off **Routing & Traffic**
- [ ] Turn off **Improve Maps**

Puoi decidere di consentire alle app di richiedere di **tracciarti**, qui. Disabilitarlo impedisce a tutte le app di tracciarti, con l'ID pubblicitario del tuo telefono. Seleziona **Tracciamento**:

- [ ] Disattiva **Consenti alle App di Richiedere di Tracciare**

This is disabled by default and cannot be changed for users under 18.

Dovresti disattivare **Sensore di Ricerca e Dati di Utilizzo** se non desideri partecipare agli studi. Seleziona **Sensore di Ricerca e Dati di Utilizzo**:

- [ ] Disattiva **Raccolta dei Dati del Sensore e di Utilizzo**

**Safety Check** ti consente di visualizzare rapidamente e di revocare certe persone e certe app, che potrebbero avere l'autorizzazione ad accedere ai tuoi dati. Here you can perform an **Emergency Reset**, immediately resetting permissions for all people and apps which might have access to device resources. You can also **Manage Sharing & Access** which allows you to go through and customize who and what has access to your device and account resources.

Dovresti disabilitare le analisi se non desideri inviare i dati di utilizzo ad Apple. Seleziona **Analisi e Miglioramenti**:

- [ ] Disattiva **Condividi Analisi iPhone** o **Condividi Analisi iPhone e Watch**
- [ ] Disattiva **Condividi Analisi di iCloud**
- [ ] Disattiva **Migliora Fitness+**
- [ ] Disattiva **Migliora Sicurezza**
- [ ] Disattiva **Migliora Siri e Dettatura**
- [ ] Turn off **Improve Assistive Voice Features**
- [ ] Turn off **Improve AR Location Accuracy**

Disabilita gli **Annunci Personalizzati**, se non desideri ricevere annunci mirati. Select **Apple Advertising**:

- [ ] Disattiva gli **Annunci Personalizzati**

**App Privacy Report** è uno strumento integrato che ti consente di visualizzare quale autorizzazioni sono in uso dalle tue app. Seleziona **Rapporto sulla Privacy dell'App**:

- [x] Seleziona **Attiva Rapporto sulla Privacy delle App**

La [Modalità Lockdown](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) è un'impostazione di sicurezza che puoi abilitare per rendere il tuo telefono più resistente agli attacchi. Be aware that certain apps and features [won't work](https://support.apple.com/HT212650) as they do normally.

- [x] Seleziona **Attiva Modalità Lockdown**

## Ulteriori Consigli

### Chiamate E2EE

Le normali telefonate effettuate con l'app Telefono tramite il proprio operatore, non sono E2EE. Both FaceTime Video and FaceTime Audio calls are E2EE. Alternatively, you can use [another app](../real-time-communication.md) like Signal for E2EE calls.

### iMessage Crittografata

The [color of the message bubble](https://support.apple.com/en-us/104972) in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates the other party is using either the outdated SMS and MMS protocols or RCS. RCS on iOS is **not** E2EE. Currently, the only way to have E2EE in Messages is for both parties to be using iMessage on Apple devices.

Se tu o il tuo partner di messaggistica avete abilitato iCloud Backup senza la Protezione Avanzata dei Dati, la chiave crittografica sarà memorizzata sui server di Apple, a significare che potrà accedere ai tuoi messaggi. Additionally, iMessage's key exchange is not as secure as alternative implementations like Signal's (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Photo Permissions

When an app prompts you for access to your device's photo library, iOS provides you with options to limit what an app can access.

Rather than allow an app to access all the photos on your device, you can allow it to only access whichever photos you choose by tapping the "Select Photos..." option in the permission dialog. You can change photo access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Photos**.

![Photo Permissions](../assets/img/ios/photo-permissions-light.png#only-light) ![Photo Permissions](../assets/img/ios/photo-permissions-dark.png#only-dark)

**Add Photos Only** is a permission that only gives an app the ability to download photos to the photo library. Not all apps which request photo library access provide this option.

![Private Access](../assets/img/ios/private-access-light.png#only-light) ![Private Access](../assets/img/ios/private-access-dark.png#only-dark)

Some apps also support **Private Access**, which functions similarly to the **Limited Access** permission. However, photos shared to apps using Private Access include their location by default. We recommend unchecking this setting if you do not [remove photo metadata](../data-redaction.md) beforehand.

### Contact Permissions

Similarly, rather than allow an app to access all the contacts saved on your device, you can allow it to only access whichever contacts you choose. You can change contact access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Contacts**.

![Contact Permissions](../assets/img/ios/contact-permissions-light.png#only-light) ![Contact Permissions](../assets/img/ios/contact-permissions-dark.png#only-dark)

### Require Biometrics and Hide Apps

iOS offers the ability to lock most apps behind Touch ID/Face ID or your passcode, which can be useful for protecting sensitive content in apps which do not provide the option themselves. You can lock an app by long-pressing on it and selecting **Require Face ID/Touch ID**. Any app locked in this way requires biometric authentication whenever opening it or accessing its contents in other apps. Also, notification previews for locked apps will not be shown.

In addition to locking apps behind biometrics, you can also hide apps so that they don't appear on the Home Screen, App Library, the app list in **Settings**, etc. While hiding apps may be useful in situations where you have to hand your unlocked phone to someone else, the concealment provided by the feature is not absolute, as a hidden app is still visible in some places such as the battery usage list. Moreover, one notable tradeoff of hiding an app is that you will not receive any of its notifications.

You can hide an app by long-pressing on it and selecting **Require Face ID/Touch ID** → **Hide and Require Face ID/Touch ID**. Note that pre-installed Apple apps, as well as the default web browser and email app, cannot be hidden. Hidden apps reside in a **Hidden** folder at the bottom of the App Library, which can be unlocked using biometrics. This folder appears in the App Library whether you hid any apps or not, which provides you a degree of plausible deniability.

### Redacting Elements in Images

If you need to hide information in a photo, you can use Apple's built-in editing tools to do so.

If your device supports it, you can use the [Clean Up](https://support.apple.com/en-us/121429) feature to pixelate faces or remove objects from images.

- Open the **Photos** app and tap the photo you have selected for redaction
- Tap the :material-tune: (at the bottom of the screen)
- Tap the button labeled **Clean Up**
- Draw a circle around whatever you want to redact. Faces will be pixelated and it will attempt to delete anything else.

Our warning [against blurring text](../data-redaction.md) also applies here, so we recommend to instead add a black shape with 100% opacity over it. In addition to redacting text, you can also black out any face or object using the **Photos** app.

- Tap the image you have selected for redaction
- Tap the :material-tune: (at the bottom of the screen) → markup symbol (top right) → plus icon at the bottom right
- Select **Add Shape** and choose the square or circle
- On the toolbar, tap the circle (left-most option) and choose black as the color for filling in the shape. You can also move the shape and increase its size as you see fit.

**Don't** use the highlighter to obfuscate information, as its opacity is not quite 100%.

### Evita il Jailbreaking

Il Jailbreak di un iPhone ne mina la sicurezza e ti rende vulnerabile. Eseguire software non affidabili e di terze parti, potrebbe causare l'infezione del tuo dispositivo da malware.

### Beta di iOS

Apple rende sempre disponibili per versioni beta di iOS in anticipo, per coloro che desiderano aiutare a trovare e segnalare i bug. Sconsigliamo di installare il software in beta sul tuo telefono. Le versioni beta sono potenzialmente instabili e potrebbero presentare vulnerabilità di sicurezza non ancora scoperte.

## Punti Salienti della Sicurezza

### Prima del Primo Sblocco

If your threat model includes [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} that involve forensic tools, and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. Lo stato *successivo* a un riavvio, ma *antecedente* allo sblocco del tuo dispositivo è noto come "Prima del Primo Sblocco" (BFU) e, quando il tuo dispositivo è in tale stato, rende [significativamente più difficile](https://belkasoft.com/checkm8_glossary), per gli strumenti forensi, di sfruttare vulnerabilità per accedere ai tuoi dati. Questo stato BFU ti consente di ricevere notifiche per le chiamate, i messaggi e le sveglie, ma gran parte dei dati sul tuo dispositivo sono ancora crittografati e inaccessibili. Ciò può essere poco pratico, quindi, considera se tali compromessi hanno senso per la tua situazione.
