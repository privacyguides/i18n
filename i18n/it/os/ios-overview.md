---
title: Panoramica su iOS
icon: simple/apple
description: iOS è un sistema operativo mobile sviluppato da Apple per l'iPhone.
---

**iOS** e **iPadOS** sono sistemi operativi mobili proprietari sviluppati da Apple per i propri prodotti, iPhone e iPad, rispettivamente. Se possiedi un dispositivo mobile Apple, puoi incrementare la tua privacy disabilitando alcune funzionalità di telemetria integrate e rafforzando alcune impostazioni per la privacy e la sicurezza, integrate sul sistema.

## Note sulla Privacy

iOS devices are frequently praised by security experts for their robust data protection and adherence to modern best practices. Tuttavia, le restrizioni dell'ecosistema di Apple, in particolare per quanto riguarda i dispositivi mobili, ostacolano ancora la privacy in diversi modi.

Generalmente, consideriamo che iOS fornisca protezioni della privacy e della sicurezza migliori della media per gran parte delle persone, rispetto ai dispositivi Android di fabbrica da qualsiasi produttore. However, you can achieve even higher standards of privacy with a [custom Android operating system](../android/distributions.md#aosp-derivatives) like GrapheneOS, if you want or need to be completely independent of Apple or Google's cloud services.

### Blocco di Attivazione

Tutti i dispositivi iOS devono essere confrontati con i server di Activation Lock di Apple, quando configurati inizialmente o ripristinati, a significare che è **necessaria** una connessione a Internet per utilizzare un dispositivo iOS.

### App Store Obbligatorio

La sola fonte di app su iOS è l'App Store di Apple, che richiede un Apple ID per accedervi. Ciò significa che Apple detiene un registro di qualsiasi app tu installi sul tuo dispositivo e, probabilmente, potrebbe collegare tali informazioni alla tua identità reale, se fornisci un metodo di pagamento all'App Store.

### Telemetria Invadente

Apple ha storicamente avuto problemi con l'adeguata anonimizzazione della propria telemetria, su iOS. [In 2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), Apple was found to transmit Siri recordings—some containing highly confidential information—to their servers for manual review by third-party contractors. While they temporarily stopped that program after that practice was [widely reported on](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), the problem wasn't completely resolved [until 2021](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance).

Di recente, si è scoperto che Apple [trasmette dati analitici anche quando la condivisione degli stessi è disattivata](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) su iOS, e questi dati [sembrano](https://twitter.com/mysk_co/status/1594515229915979776) essere facilmente collegabili agli identificativi univoci dell'account iCloud, nonostante siano presumibilmente anonimi.

## Configurazione consigliata

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

In cima all'app delle **Impostazioni**, visualizzerai il tuo nome e la tua foto di profilo, se hai un Apple ID. Selezionalo, quindi seleziona **Media e Acquisti** > **Visualizza Profilo**.

- [ ] Disattiva i **Consigli Personalizzati**

#### Find My

**Find My** è un servizio che ti consente di tracciare i tuoi dispositivi Apple e di condividere la tua posizione con i tuoi amici e la tua famiglia. Inoltre, ti consente di svuotare da remoto il tuo dispositivo, in caso di furto, impedendo ai ladri di accedere ai tuoi dati. Your Find My [location data is E2EE](https://apple.com/legal/privacy/data/en/find-my) when:

- Your location is shared with a family member or friend, and you both use iOS 17 or greater.
- Il tuo dispositivo è offline ed è individuato dalla Rete di Find My.

I tuoi dati sulla posizione non sono E2EE quando il tuo dispositivo è online e utilizzi Find My iPhone da remoto, per individuare il tuo dispositivo. Dovrai decidere se mantenere questi compromessi valga i vantaggi antifurto del Blocco di Attivazione.

In cima all'app delle **Impostazioni**, visualizzerai il tuo nome e la tua foto di profilo, se hai un Apple ID. Selezionalo, quindi seleziona **Find My**. Qui puoi scegliere se abilitare o disabilitare le funzionalità di posizione di Find My.

### Settings

Molte altre impostazioni correlate alla privacy si possono trovare nell'app delle **Impostazioni**.

#### Modalità Aereo

Abilitare la **Modalità Aereo** impedisce al tuo telefono di contattare le torri cellulari. Potrai comunque connetterti alla Wi-Fi e al Bluetooth, quindi, ogni volta che sei connesso alla Wi-Fi, potrai attivare quest'impostazione.

#### Wi-Fi

Puoi abilitare la randomizzazione dell'indirizzo hardware per proteggerti dal tracciamento sulle reti Wi-Fi. Sulla rete a cui sei attualmente connesso, premi il pulsante :material-information::

- [x] Attiva l'**Indirizzo Wi-Fi Privato**

Inoltre, puoi **Limitare il Tracciamento dell'Indirizzo IP**. Ciò somiglia alla Trasmissione Privata di iCloud, ma riguarda soltanto le connessioni ai "tracciatori noti." Poiché riguarda soltanto le connessioni a server potenzialmente dannosi, quest'impostazione può tranquillamente esser lasciata abilitata, ma se desideri che *qualsiasi* traffico non sia indirizzato attraverso i server di Apple, dovresti disattivarla.

#### Bluetooth

Il **Bluetooth** dovrebbe essere disabilitato quando non lo stai utilizzando, poiché incrementa la superficie d'attacco. Disabilitare il Bluetooth (o la Wi-Fi) tramite il Centro di Controllo, lo disabilita soltanto temporaneamente: devi disattivarlo nelle Impostazioni, affinché ciò resti effettivo.

- [ ] Disattiva il **Bluetooth**

#### Generali

Il nome del tuo dispositivo iPhone conterrà di default il tuo nome e, questo, sarà visibile a chiunque, sulle reti cui ti connetti. Dovresti modificarlo in qualcosa di più generico, come "iPhone." Seleziona **Informazioni su** > **Nome** e inserisci il nome del dispositivo che preferisci.

È importante installare frequentemente gli **Aggiornamenti Software**, per ottenere le più recenti correzioni di sicurezza. Puoi abilitare gli **Aggiornamenti Automatici** per mantenere aggiornato il tuo telefono, senza dover controllare costantemente la presenza di aggiornamenti. Seleziona **Aggiornamenti Software** > **Aggiornamenti Automatici**:

- [x] Attiva **Scarica Aggiornamenti iOS**
- [x] Attiva **Installa Aggiornamenti iOS**
- [x] Attiva **Risposte di Sicurezza e File di Sistema**

**AirDrop** ti consente di trasferire facilmente file, ma può consentire a sconosciuti di inviarti file indesiderati.

- [x] Seleziona **AirDrop** > **Ricezione disattivata**

**AirPlay** ti consente di trasmettere facilmente i contenuti dal tuo iPhone a una TV; tuttavia, potresti non desiderarlo fare sempre. Seleziona **AirPlay e Scambio** > **AirPlay a TV automatico**:

- [x] Seleziona **Mai** o **Chiedi**

**Background App Refresh** consente alle tue app di aggiornare i propri contenuti, mentre non le stai utilizzando. Ciò potrebbe causare che si creino connessioni indesiderate. Disattivare quest'opzione può anche far risparmiare batteria, ma potrebbe influire sulle capacità dell'app di ricevere informazioni aggiornate, in particolare alle app meteorologiche e di messaggistica.

Seleziona **Background App Refresh** e disattiva qualsiasi app non desideri continui ad aggiornarsi in background. Se desideri che nessuna app si aggiorni in background, puoi selezionare **Background App Refresh** e **disattivarla**.

#### Siri e Ricerca

Se non desideri che qualcuno possa controllare il tuo telefono con Siri, quando è bloccato, puoi disattivarlo qui.

- [ ] Disattiva **Consenti Siri Quando Bloccato**

#### Face ID/Touch ID e Passcode

Impostare una password forte sul tuo telefono è il passo più importante che puoi intraprendere per la sicurezza fisica del dispositivo. In questo caso dovrai trovare un compromesso tra la sicurezza e la comodità: una password più lunga sarà noiosa da digitare ogni volta, ma una password o un PIN più breve sarà più facile da indovinare. Configurare Face ID o TouchID insieme a una password forte, può costituire un buon compromesso tra utilizzabilità e sicurezza.

Seleziona **Attiva Passcode** o **Modifica Passcode** > **Opzioni Passcode** > **Codice Alfanumerico Personalizzato**. Make sure that you create a [secure password](../basics/passwords-overview.md).

Se desideri utilizzare Face ID o Touch ID, puoi ora procedere alla configurazione. Il tuo telefono utilizzerà la password configurata in precedenza come ripiego, nel caso in cui la tua verifica biometrica dovesse fallire. I metodi biometrici di sblocco sono principalmente una comodità, sebbene impediscano alle telecamere di sicurezza o alle persone alle tue spalle di guardarti inserire il tuo codice d'accesso.

Se utilizzi la biometria, dovresti sapere come disattivarla rapidamente in caso d'emergenza. Tenere premuto il tasto laterale o di accensione e *uno dei* tasti del volume, finché non visualizzi il cursore Scorri per Spegnere, disabiliterà la biometria, richiedendo il codice d'accesso per sbloccare. Inoltre, il tuo codice di sicurezza sarà richiesto al riavvio del dispositivo.

Su alcuni dispositivi precedenti, potresti dover premere cinque volte il tasto di accensione per disabilitare la biometria o, per i dispositivi con Touch ID, potresti dover soltanto tenere premuto il tasto d'accensione e nient'altro. Assicurati di provare in anticipo, così da sapere quale metodo funziona per il tuo dispositivo.

**Stolen Device Protection** is a new feature in iOS 17.3 which adds additional security intended to protect your personal data if your device is stolen while unlocked. Se utilizzi la biometria e la funzione Trova il mio dispositivo nelle impostazioni dell'ID Apple, si consiglia di attivare questa nuova protezione:

- [x] Seleziona **Attiva la protezione**

After enabling Stolen Device Protection, [certain actions](https://support.apple.com/HT212510) will require biometric authentication without a password fallback (in the event that a shoulder surfer has obtained your PIN), such as using password autofill, accessing payment information, and disabling Lost Mode. It also adds a security delay to certain actions performed away from your home or another "familiar location," such as requiring a 1-hour timer to reset your Apple ID password or sign out of your Apple ID. Questo ritardo ha lo scopo di dare all'utente il tempo di attivare la Modalità smarrito e di proteggere il proprio account prima che un ladro possa resettare il dispositivo.

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

Disabilita gli **Annunci Personalizzati**, se non desideri ricevere annunci mirati. Select **Apple Advertising**:

- [ ] Disattiva gli **Annunci Personalizzati**

**App Privacy Report** è uno strumento integrato che ti consente di visualizzare quale autorizzazioni sono in uso dalle tue app. Seleziona **Rapporto sulla Privacy dell'App**:

- [x] Seleziona **Attiva Rapporto sulla Privacy delle App**

La [Modalità Lockdown](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) è un'impostazione di sicurezza che puoi abilitare per rendere il tuo telefono più resistente agli attacchi. Be aware that certain apps and features [won't work](https://support.apple.com/HT212650) as they do normally.

- [x] Seleziona **Attiva Modalità Lockdown**

## Ulteriori Consigli

### Chiamate E2EE

Le normali telefonate effettuate con l'app Telefono tramite il proprio operatore, non sono E2EE. Le chiamate di FaceTime Video e FaceTime Audio sono E2EE, o puoi utilizzare un'[altra app](../real-time-communication.md) come Signal.

### Evita il Jailbreaking

Il Jailbreak di un iPhone ne mina la sicurezza e ti rende vulnerabile. Eseguire software non affidabili e di terze parti, potrebbe causare l'infezione del tuo dispositivo da malware.

### iMessage Crittografata

Il colore della bolla del messaggio nell'app dei Messaggi indica se i tuoi messaggi sono E2EE o no. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates the other party is using the outdated SMS and MMS protocols. Al momento, il solo modo per ottenere l'E2EE sui Messaggi è che entrambe le parti utilizzino iMessage sui dispositivi Apple.

Se tu o il tuo partner di messaggistica avete abilitato iCloud Backup senza la Protezione Avanzata dei Dati, la chiave crittografica sarà memorizzata sui server di Apple, a significare che potrà accedere ai tuoi messaggi. Inoltre, lo scambio di chiavi di iMessage non è sicuro quanto le implementazioni alternative, come Signal (che ti consente di visualizzare la chiave del destinatario e di verificare tramite Codice QR), quindi non ci si dovrebbe affidare per le comunicazioni particolarmente sensibili.

### Oscuramento di Volti/Informazioni

Se devi nascondere informazioni in un foto, puoi utilizzare gli strumenti integrati di Apple per farlo. Apri la foto che desideri modificare, premi su modifica nell'angolo superiore destro dello schermo, quindi premi il simbolo del pennarello in alto a destra. Premi il più in basso a destra alla schermata, quindi, premi l'icona del rettangolo. Ora, puoi posizionare un rettangolo in qualsiasi punto dell'immagine. Assicurati di premere l'icona della forma in basso a sinistra e di selezionare il rettangolo riempito. **Non** utilizzare l'evidenziatore per offuscare le informazioni, poiché la sua opacità non è al 100%.

### Beta di iOS

Apple rende sempre disponibili per versioni beta di iOS in anticipo, per coloro che desiderano aiutare a trovare e segnalare i bug. Sconsigliamo di installare il software in beta sul tuo telefono. Le versioni beta sono potenzialmente instabili e potrebbero presentare vulnerabilità di sicurezza non ancora scoperte.

## Punti Salienti della Sicurezza

### Prima del Primo Sblocco

If your threat model includes forensic tools, and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. Lo stato *successivo* a un riavvio, ma *antecedente* allo sblocco del tuo dispositivo è noto come "Prima del Primo Sblocco" (BFU) e, quando il tuo dispositivo è in tale stato, rende [significativamente più difficile](https://belkasoft.com/checkm8_glossary), per gli strumenti forensi, di sfruttare vulnerabilità per accedere ai tuoi dati. Questo stato BFU ti consente di ricevere notifiche per le chiamate, i messaggi e le sveglie, ma gran parte dei dati sul tuo dispositivo sono ancora crittografati e inaccessibili. Ciò può essere poco pratico, quindi, considera se tali compromessi hanno senso per la tua situazione.
