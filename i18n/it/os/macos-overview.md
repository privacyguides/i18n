---
title: Panoramica di macOS
icon: material/apple-finder
description: macOS è il sistema operativo desktop di Apple che opera con il loro hardware, fornendo grande sicurezza.
---

**macOS** è un sistema operativo Unix sviluppato da Apple per i propri computer Mac. Per migliorare la privacy su macOS, puoi disabilitare le funzionalità di telemetria e rafforzare le impostazioni di privacy e sicurezza esistenti.

I più datati Mac e Hackintosh basati su Intel non supportano tutte le funzionalità di sicurezza offerte da macOS. To enhance data security, we recommend using a newer Mac with [Apple Silicon](https://support.apple.com/HT211814).

## Note sulla Privacy

Esistono alcune notevoli preoccupazioni sulla privacy con macOS, che dovremmo considerare. Queste sono relative allo stesso sistema operativo, e non ad altri servizi e app di Apple.

### Blocco di Attivazione

Brand-new Apple Silicon devices can be set up without an internet connection. Tuttavia, recuperare o ripristinare il tuo Mac **richiederà** una connessione a Internet, affinché i server di Apple possano verificarlo rispetto al database del Blocco di Attivazione, dei dispositivi perduti o rubati.

### Controlli di Revoca dell'App

macOS esegue controlli online quando apri un'app, per verificare che questa non contenga malware noti e se il certificato di firma dello sviluppatore è stato revocato.

Apple's OCSP service uses HTTPS encryption, so only they are able to see which apps you open. They've [posted information](https://support.apple.com/HT202491) about their logging policy for this service. They additionally [promised](http://lapcatsoftware.com/articles/2024/8/3.html) to add a mechanism for people to opt-out of this online check, but this has not been added to macOS.

While you [can](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private) manually opt out of this check relatively easily, we recommend against doing so unless you would be badly compromised by the revocation checks performed by macOS, because they serve an important role in ensuring compromised apps are blocked from running.

## Configurazione consigliata

Il tuo profilo, quando configuri per la prima volta Mac, sarà un profilo Amministratore, avente privilegi maggiori di un profilo utente Standard. macOS presenta numerose protezioni che impediscono a malware e altri programmi di abusare dei tuoi privilegi da Amministratore, così che l'utilizzo di questo profilo sia, in generale, sicuro.

However, exploits in protective utilities like `sudo` have been [discovered in the past](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass). Se desideri evitare la possibilità che i programmi che esegui abusino dei tuoi privilegi da Amministratore, potresti considerare di creare un secondo profilo utente Standard, da utilizzare per le operazioni quotidiane. Ciò presenta l'ulteriore beneficio di rendere più ovvio quando un'app necessita dell'accesso da amministratore, poiché ti richiederà le credenziali ogni volta.

Se utilizzi un secondo profilo, non è rigorosamente necessario connettersi al tuo profilo da Amministratore originale, dalla schermata d'accesso di macOS. Quando stai facendo qualcosa da utente Standard che richieda le autorizzazioni da Amministratore, il sistema dovrebbe richiederti l'autenticazione, dove puoi inserire le tue credenziali da Amministratore, pur essendo un utente Standard, una tantum. Apple fornisce [supporto](https://support.apple.com/HT203998) per nascondere il tuo profilo da Amministratore, se preferisci visualizzare un singolo profilo sulla tua schermata di accesso.

### iCloud

Quando utilizzi i servizi di Apple come iCloud, gran parte delle tue informazioni sono memorizzate sui loro server e protetti dalle chiavi *cui Apple ha accesso* di default. This is called [Standard Data Protection](https://support.apple.com/en-us/102651) by Apple.

Dunque, se utilizzi iCloud, dovresti [abilitare la **Protezione Avanzata dei Dati**](https://support.apple.com/HT212520). Questa, crittografa praticamente tutti i tuoi dati di iCloud con chiavi memorizzate sui tuoi dispositivi (crittografia end-to-end), piuttosto che sui server di Apple, così che i tuoi dati di iCloud siano protetti nel caso di una violazione di dati, e altrimenti nascosti da Apple.

If you want to be able to install apps from the App Store but don't want to enable iCloud, you can sign in to your Apple Account from the App Store instead of **System Settings**.

### Impostazioni di Sistema

Esistono numerose impostazioni integrate che dovresti confermare o modificare per proteggere il tuo sistema. Apri l'app delle **Impostazioni**:

#### Bluetooth

- [ ] Rimuovi la spunta da **Bluetooth** (a meno che tu non lo stia utilizzando al momento)

#### Rete

A seconda del fatto che tu stia utilizzando la **Wi-Fi** o il cavo **Ethernet** (denotato da un puntino verde e la parola "connesso"), clicca sull'icona corrispondente.

Clicca sul pulsante dei "Dettagli" affianco al nome della tua rete:

- [x] Select **Rotating** under **Private Wi-Fi address**

- [x] Check **Limit IP address tracking**

##### Firewall

Il tuo firewall blocca le connessioni di rete indesiderate. Più le impostazioni del tuo firewall sono rigide, più il tuo Mac è sicuro. Tuttavia, alcuni servizi verranno bloccati. Dovresti configurare il tuo firewall affinché sia il più rigido possibile, senza i servizi di blocco che utilizzi.

- [x] Spunta **Firewall**

Clicca sul pulsante **Opzioni**:

- [x] Spunta **Blocca tutte le connessioni in entrata**

Se questa configurazione è troppo rigida, puoi tornare qui e rimuovere la spunta. Tuttavia, macOS, tipicamente, ti richiederà di consentire le connessioni in entrata per un'app, se tale app lo richiede.

#### Generali

Di default, il nome del tuo dispositivo sarà simile a "iMac di [tuo nome]". Poiché questo nome è trasmesso pubblicamente sulla tua rete, vorrai modificarlo a qualcosa di generico, come "Mac".

Clicca su **Informazioni** e digita il nome desiderato del tuo dispositivo, nel campo **Nome**.

##### Aggiornamenti software

Dovresti installare automaticamente tutti gli aggiornamenti disponibili, per assicurarti che il tuo Mac abbia le correzioni di sicurezza più recenti.

Clicca sulla piccola icona :material-information-outline:, affianco ad **Aggiornamenti Automatici**:

- [x] Spunta **Controlla aggiornamenti**

- [x] Spunta **Scarica nuovi aggiornamenti quando disponibili**

- [x] Spunta **Installa aggiornamenti di macOS**

- [x] Spunta **Installa aggiornamenti delle applicazioni dall'Apple Store**

- [x] Spunta **Installa Risposte di Sicurezza e file di sistema**

#### Privacy e sicurezza

Ogni volta che un'applicazione richiede un'autorizzazione, apparirà qui. Puoi decidere a quali applicazioni desideri consentire o negare dei permessi specifici.

##### Servizi di Posizione

Puoi consentire individualmente i servizi di posizione, per ogni app. Se non necessiti che le app utilizzino la tua posizione, disattivare interamente i servizi di posizione è l'opzione più privata.

- [ ] Rimuovi la spunta da **Servizi di Posizione**

##### Analisi e Miglioramenti

Decidi se desideri condividere i dati analitici con Apple e gli sviluppatori.

- [ ] Rimuovi la spunta da **Condividi Analisi Mac**

- [ ] Rimuovi la spunta da **Migliora Siri e Dettatura**

- [ ] Rimuovi la spunta da **Condividi con gli sviluppatori dell'app**

- [ ] Rimuovi la spunta da **Condividi Analisi iCloud** (visibile se sei connesso a iCloud)

##### Pubblicità di Apple

Decidi se desideri annunci personalizzati secondo il tuo utilizzo.

- [ ] Rimuovi la spunta da **Annunci Personalizzati**

##### FileVault

On modern devices with a Secure Enclave (Apple T2 Security Chip, Apple Silicon), your data is always encrypted, but is decrypted automatically by a hardware key if your device doesn't detect it's been tampered with. Enabling [FileVault](../encryption.md#filevault) additionally requires your password to decrypt your data, greatly improving security, especially when powered off or before the first login after powering on.

Sui vecchi computer Mac basati su Intel, FileVault è la sola forma di crittografia del disco disponibile di default, e dovrebbe sempre essere abilitata.

- [x] Clicca **Attiva**

##### Modalità Lockdown

La [Modalità Lockdown](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) disabilita alcune funzionalità per poter migliorare la sicurezza. Some apps or features won't work the same way they do when it's off, for example, [JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers) and [WASM](https://developer.mozilla.org/docs/WebAssembly) are disabled in Safari with Lockdown Mode enabled. Consigliamo di abilitare la Modalità di Lockdown e di scoprire se impatta significativamente sul tuo utilizzo: è facile convivere con molte delle modifiche che effettua.

- [x] Clicca **Attiva**

### Randomizzazione dell'indirizzo MAC

macOS uses a randomized MAC address when performing Wi-Fi scans while disconnected from a network.

You can set your MAC address to be randomized per network and rotate occasionally to prevent tracking between networks and on the same network over time.

Go to **System Settings** → **Network** → **Wi-Fi** → **Details** and set **Private Wi-Fi address** to either **Fixed** if you want a fixed but unique address for the network you're connected to, or **Rotating** if you want it to change over time.

Consider changing your hostname as well, which is another device identifier that's broadcast on the network you're connected to. You may wish to set your hostname to something generic like "MacBook Air", "Laptop", "John's MacBook Pro", or "iPhone" in **System Settings** → **General** → **Sharing**. Alcuni [script per la privacy](https://github.com/sunknudsen/privacy-guides/tree/master/how-to-spoof-mac-address-and-hostname-automatically-at-boot-on-macos#guide) consentono di generare facilmente hostname con nomi casuali.

## Protezioni di Sicurezza

macOS utilizza la difesa approfondita, affidandosi a svariati livelli di protezioni basati su software e hardware, con proprietà differenti. Ciò assicura che un fallimento su un livello, non comprometta la sicurezza generale del sistema.

### Sicurezza del Software

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

macOS ti consente di installare gli aggiornamenti beta. Questi sono instabili e potrebbero comportare un'ulteriore telemetria, essendo per scopi di test. Per questo, ti consigliamo di evitare i software in beta, in generale.

</div>

#### Volume di Sistema Firmato

i componenti di sistema di macOS sono protetti in un volume di sistema firmato di sola lettura, a significare che né tu né un malware possiate alterare importanti file di sistema.

Il volume di sistema è verificato mentre in esecuzione e qualsiasi dato non sia firmato con una firma crittografica valida da Apple, sarà rifiutato.

#### Protezione dell'Integrità di Sistema

macOS imposta certe limitazioni di sicurezza, che non sono sovrascrivibili. Queste, sono dette Controlli d'Accesso Obbligatori e formano la base del sandbox, controllo genitori e Protezione dell'Integrità di Sistema su macOS.

La Protezione dell'Integrità di Sistema rende le posizioni dei file di sola lettura, per proteggere dalla modifica da parte di codice dannoso. Questa si aggiunge alla Protezione dell'Integrità del Kernel basata sul hardware, che evita che il kernel sia modificata in memoria.

#### Sicurezza delle Applicazioni

##### Sandbox delle App

On macOS, whether an app is sandboxed is determined by the developer when they sign it. The App Sandbox protects against vulnerabilities in the apps you run by limiting what a malicious actor can access in the event that the app is exploited. The App Sandbox *alone* can't protect against [:material-package-variant-closed-remove: Supply Chain Attacks](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} by malicious developers. For that, sandboxing needs to be enforced by someone other than the developer themselves, as it is on the App Store.

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

I software scaricati al di fuori dell'App Store ufficiale non devono essere testate. If your threat model prioritizes defending against [:material-bug-outline: Passive Attacks](../basics/common-threats.md#security-and-privacy){ .pg-orange }, then you may want to check if the software you download outside the App Store is sandboxed, which is up to the developer to *opt in*.

</div>

You can check if an app uses the App Sandbox in a few ways:

You can check if apps that are already running are sandboxed using the [Activity Monitor](https://developer.apple.com/documentation/security/protecting-user-data-with-app-sandbox#Verify-that-your-app-uses-App-Sandbox).

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Just because one of an app's processes is sandboxed doesn't mean they all are.

</div>

Alternatively, you can check apps before you run them by running this command in the terminal:

``` zsh
% codesign -dvvv --entitlements - <path to your app>
```

If an app is sandboxed, you should see the following output:

``` zsh
    [Key] com.apple.security.app-sandbox
    [Value]
        [Bool] true
```

If you find that the app you want to run is not sandboxed, then you may employ methods of [compartmentalization](../basics/common-threats.md#security-and-privacy) such as virtual machines or separate devices, use a similar app that is sandboxed, or choose to not use the non-sandboxed app altogether.

##### Hardened Runtime

The [Hardened Runtime](https://developer.apple.com/documentation/security/hardened_runtime) is an extra form of protection for apps that prevents certain classes of exploits. It improves the security of apps against exploitation by disabling certain features like JIT.

You can check if an app uses the Hardened Runtime using this command:

``` zsh
codesign --display --verbose /path/to/bundle.app
```

If Hardened Runtime is enabled, you will see `flags=0x10000(runtime)`. The `runtime` output means Hardened Runtime is enabled. There might be other flags, but the runtime flag is what we're looking for here.

You can enable a column in Activity Monitor called "Restricted" which is a flag that prevents programs from injecting code via macOS's [dynamic linker](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html). Ideally, this should say "Yes".

##### Antivirus

macOS presenta due forme di difesa dai malware:

1. In primo luogo, la protezione dal lancio di malware è fornita dal processo di revisione dell'App Store per le applicazioni presenti su di esso, o *Notarizzazione* (parte di *Gatekeeper*), un procedimento in cui le app di terze parti sono scansionate in cerca di malware noti da Apple, prima di poter essere eseguite. Apps are required to be signed by the developers using a key given to them by Apple. This ensures that you are running software from the real developers. Notarization also requires that developers enable the Hardened Runtime for their apps, which limits methods of exploitation.
2. La protezione da altri malware e rimedi da malware esistenti sul tuo sistema è fornita da *XProtect*, un software antivirus più tradizionale, integrato su macOS.

We recommend against installing third-party antivirus software as they typically do not have the system-level access required to properly function anyway, because of Apple's limitations on third-party apps, and because granting the high levels of access they do ask for often poses an even greater security and privacy risk to your computer.

##### Backup

macOS comes with automatic backup software called [Time Machine](https://support.apple.com/HT201250), so you can create encrypted backups to an external drive or a network drive in the event of corrupted/deleted files.

### Sicurezza Hardware

Many modern security features in macOS—such as modern Secure Boot, hardware-level exploit mitigation, OS integrity checks, and file-based encryption—rely on Apple Silicon, and Apple's newer hardware always has the [best security](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). We only encourage the use of Apple Silicon, and not older Intel-based Mac computers or Hackintoshes.

Alcune di queste funzionalità di sicurezza moderne sono disponibili sui vecchi computer Mac con processore Intel con l'Apple T2 Security Chip, ma questo chip è suscettibile all'exploit *checkm8* che potrebbe comprometterne la sicurezza.

Se utilizzi accessori Bluetooth come una tastiera, consigliamo di utilizzarne di ufficiali di Apple, poiché il loro firmware sarà automaticamente aggiornato per te da macOS. Utilizzare accessori di terze parti va bene, ma dovresti ricordarti di installarne regolarmente gli aggiornamenti del firmware.

I Sistemi su Chip di Apple mirano a minimizzare la superficie di attacco relegando le funzioni di sicurezza ad hardware dedicato con funzionalità limitate.

#### ROM di Avvio

macOS impedisce la persistenza dei malware, consentendo soltanto ai software Apple ufficiali di essere eseguiti all'avvio; ciò è noto come avvio di sicurezza. I computer Mac verificano ciò con un po' di memoria di sola lettura sul Sistema su Chip, detta ROM di avvio, stabilita durante la produzione del chip.

La ROM di avvio forma la radice di fiducia del hardware. Ciò assicura che i malware non possano manomettere il processo di avvio. Quando il tuo Mac si avvia, la ROM di avvio è la prima cosa eseguita, formando il primo collegamento nella catena di fiducia.

I computer Mac sono configurabili per avviarsi in tre modalità di sicurezza: *Sicurezza Completa*, *Sicurezza Ridotta* e *Sicurezza Permissiva*, dove la prima è l'impostazione predefinita. Idealmente, dovresti utilizzare la modalità di Sicurezza Completa ed evitare cose come le **estensioni del Kernel**, che ti forzano a ridurre la tua modalità di sicurezza. Assicurati di [verificare](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) di star utilizzando la modalità di Sicurezza Completa.

#### Secure Enclave

The Secure Enclave is a security chip built into devices with Apple Silicon which is responsible for storing and generating encryption keys for data at rest as well as Face ID and Touch ID data. Contiene la propria ROM di avvio separata.

Puoi pensare a Secure Enclave come un hub di sicurezza del tuo dispositivo: include un motore crittografico AES e un meccanismo per memorizzare in sicurezza le tue chiavi crittografiche, ed è separato dal resto del sistema quindi, anche se il processore principale è compromesso, dovrebbe ancora essere sicuro.

#### Touch ID

La funzionalità Touch ID di Apple ti consente di sbloccare in sicurezza i tuoi dispositivi, utilizzando fattori biometrici.

I tuoi dati biometrici non abbandonano mai il tuo dispositivo; sono memorizzati soltanto nel Secure Enclave.

#### Disconnessione del Microfono Hardware

All laptops with Apple Silicon or the T2 chip feature a hardware disconnect for the built-in microphone whenever the lid is closed. Ciò significa che non vi è modo per un utente malevolo, di ascoltare dal microfono del tuo Mac, anche se il sistema operativo è compromesso.

Nota che la fotocamera non presenta una disconnessione hardware, poiché la sua inquadratura è comunque oscurata, alla chiusura dello schermo.

#### Sicurezza del Processore Periferico

I computer integrano processori differenti dalla CPU principale, che gestiscono cose come rete, grafica, gestione dei consumi, etc. Questi processori possono avere una sicurezza insufficiente ed essere compromessi, dunque, Apple prova a minimizzarne l'esigenza nel proprio hardware.

Quando è necessario utilizzare uno di tali processori, Apple opera da fornitore per assicurarsi che il processore

- esegua il firmware verificato dalla CPU principale all'avvio
- abbia la propria catena di Avvio Sicuro
- segua standard crittografici minimi
- assicuri che i firmware malevoli siano revocati adeguatamente
- abbia le interfacce di debug disabilitate
- sia firmato con chiavi crittografiche di Apple

#### Protezioni di Accesso Diretto alla Memoria

Apple Silicon separates each component that requires direct memory access. Ad esempio, una porta di Thunderbolt non può accedere alla memoria designata per il Kernel.

## Fonti

- [Sicurezza della Piattaforma di Apple](https://support.apple.com/guide/security/welcome/web)
