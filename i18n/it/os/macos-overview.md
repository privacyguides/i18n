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

- [ ] Turn off **Bluetooth** (unless you are currently using it)

#### Rete

A seconda del fatto che tu stia utilizzando la **Wi-Fi** o il cavo **Ethernet** (denotato da un puntino verde e la parola "connesso"), clicca sull'icona corrispondente.

Clicca sul pulsante dei "Dettagli" affianco al nome della tua rete:

- [x] Select **Rotating** under **Private Wi-Fi address**

- [x] Turn on **Limit IP address tracking**

##### Firewall

Il tuo firewall blocca le connessioni di rete indesiderate. Più le impostazioni del tuo firewall sono rigide, più il tuo Mac è sicuro. Tuttavia, alcuni servizi verranno bloccati. Dovresti configurare il tuo firewall affinché sia il più rigido possibile, senza i servizi di blocco che utilizzi.

- [x] Turn on **Firewall**

Clicca sul pulsante **Opzioni**:

- [x] Turn on **Block all incoming connections**

Se questa configurazione è troppo rigida, puoi tornare qui e rimuovere la spunta. Tuttavia, macOS, tipicamente, ti richiederà di consentire le connessioni in entrata per un'app, se tale app lo richiede.

#### Generali

Di default, il nome del tuo dispositivo sarà simile a "iMac di [tuo nome]". Because this name is [publicly broadcast on your network](https://support.apple.com/guide/mac-help/change-computers-local-hostname-mac-mchlp2322/26/mac/26#:~:text=The%20local%20hostname%2C%20or%20local%20network%20name%2C%20is%20displayed%20at%20the%20bottom%20of%20the%20Sharing%20settings%20window.%20It%20identifies%20your%20Mac%20to%20Bonjour%2Dcompatible%20services.), you'll want to change your device name to something generic like "Mac".

Clicca su **Informazioni** e digita il nome desiderato del tuo dispositivo, nel campo **Nome**.

##### Aggiornamenti software

Dovresti installare automaticamente tutti gli aggiornamenti disponibili, per assicurarti che il tuo Mac abbia le correzioni di sicurezza più recenti.

Clicca sulla piccola icona :material-information-outline:, affianco ad **Aggiornamenti Automatici**:

- [x] Turn on **Download new updates when available**

- [x] Turn on **Install macOS updates**

- [x] Turn on **Install Security Responses and system files**

#### Apple Intelligence & Siri

If you do not use these features on macOS, you should disable them:

- [ ] Turn off **Apple Intelligence**
- [ ] Disattiva **Siri**

**[Apple Intelligence](https://apple.com/legal/privacy/data/en/intelligence-engine)** is only available if your device supports it. Apple Intelligence uses a combination of on-device processing and their [Private Cloud Compute](https://security.apple.com/blog/private-cloud-compute) for things that take more processing power than your device can provide.

To see a report of all the data sent via Apple Intelligence, you can navigate to **Privacy & Security** → **Apple Intelligence Report** and press **Export Activity** to see activity from the either the last 15 minutes or 7 days, depending on what you set it for. Similar to the **App Privacy Report** which shows you the recent permissions accessed by the apps on your phone, the Apple Intelligence Report likewise shows what is being sent to Apple's servers while using Apple Intelligence.

By default, ChatGPT integration is disabled. If you don't want ChatGPT integration anymore, you can navigate to **ChatGPT**:

- [ ] Turn off **Use ChatGPT**

You can also have it ask for confirmation every time if you leave ChatGPT integration on:

- [x] Turn on **Confirm Requests**

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Any request made with ChatGPT will be sent to ChatGPT's servers, there is no on-device processing and no PCC like with Apple Intelligence.

</div>

#### Privacy e sicurezza

Ogni volta che un'applicazione richiede un'autorizzazione, apparirà qui. Puoi decidere a quali applicazioni desideri consentire o negare dei permessi specifici.

##### Servizi di Posizione

Puoi consentire individualmente i servizi di posizione, per ogni app. Se non necessiti che le app utilizzino la tua posizione, disattivare interamente i servizi di posizione è l'opzione più privata.

- [ ] Disattiva i **Servizi di Posizione**

##### Analisi e Miglioramenti

Decide whether you want to share analytics data with Apple and app developers.

##### Pubblicità di Apple

Decidi se desideri annunci personalizzati secondo il tuo utilizzo.

- [ ] Disattiva gli **Annunci Personalizzati**

##### FileVault

On modern devices with a Secure Enclave (Apple T2 Security Chip, Apple Silicon), your data is always encrypted, but is decrypted automatically by a hardware key if your device doesn't detect it's been tampered with. Enabling [FileVault](../encryption.md#filevault) additionally requires your password to decrypt your data, greatly improving security, especially when powered off or before the first login after powering on.

Sui vecchi computer Mac basati su Intel, FileVault è la sola forma di crittografia del disco disponibile di default, e dovrebbe sempre essere abilitata.

- [x] Clicca **Attiva**

##### Modalità Lockdown

**[Lockdown Mode](https://support.apple.com/guide/mac-help/lock-mac-targeted-a-cyberattack-ibrw66f4e191/mac)** disables some features in order to improve security. Some apps or features won't work the same way they do when it's off. For example, Javascript Just-In-Time ([JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers)) compilation and [WebAssembly](https://developer.mozilla.org/docs/WebAssembly) are disabled in Safari with Lockdown Mode enabled. We recommend enabling Lockdown Mode and seeing whether it significantly impacts daily usage.

- [x] Clicca **Attiva**

### Randomizzazione dell'indirizzo MAC

macOS uses a randomized MAC address when [performing Wi-Fi scans](https://support.apple.com/guide/security/privacy-features-connecting-wireless-networks-secb9cb3140c/web) while disconnected from a network.

You can set your [MAC address to be randomized](https://support.apple.com/en-us/102509) per network and rotate occasionally to prevent tracking between networks and on the same network over time.

Go to **System Settings** → **Network** → **Wi-Fi** → **Details** and set **Private Wi-Fi address** to either **Fixed** if you want a fixed but unique address for the network you're connected to, or **Rotating** if you want it to change over time.

Consider changing your hostname as well, which is another device identifier that's broadcast on the network you're connected to. You may wish to set your hostname to something generic like "MacBook Air", "Laptop", "John's MacBook Pro", or "iPhone" in **System Settings** → **General** → **Sharing**.

## Protezioni di Sicurezza

macOS utilizza la difesa approfondita, affidandosi a svariati livelli di protezioni basati su software e hardware, con proprietà differenti. Ciò assicura che un fallimento su un livello, non comprometta la sicurezza generale del sistema.

### Sicurezza del Software

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

macOS ti consente di installare gli aggiornamenti beta. These are unstable and may come with [extra telemetry](https://beta.apple.com/privacy) since they're for testing purposes. Per questo, ti consigliamo di evitare i software in beta, in generale.

</div>

#### Volume di Sistema Firmato

macOS's system components are protected in a read-only [signed system volume](https://support.apple.com/guide/security/signed-system-volume-security-secd698747c9/web), meaning that neither you nor malware can alter important system files.

Il volume di sistema è verificato mentre in esecuzione e qualsiasi dato non sia firmato con una firma crittografica valida da Apple, sarà rifiutato.

#### Protezione dell'Integrità di Sistema

macOS imposta certe limitazioni di sicurezza, che non sono sovrascrivibili. These are called [Mandatory Access Controls](https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/1/web/1), and they form the basis of the sandbox, parental controls, and [System Integrity Protection](https://support.apple.com/en-us/102149) on macOS.

La Protezione dell'Integrità di Sistema rende le posizioni dei file di sola lettura, per proteggere dalla modifica da parte di codice dannoso. Questa si aggiunge alla Protezione dell'Integrità del Kernel basata sul hardware, che evita che il kernel sia modificata in memoria.

#### Sicurezza delle Applicazioni

##### Sandbox delle App

On macOS, whether an app is sandboxed is determined by the developer when they sign it. The [App Sandbox](https://developer.apple.com/documentation/xcode/configuring-the-macos-app-sandbox) protects against vulnerabilities in the apps you run by limiting what a malicious actor can access in the event that the app is exploited. The App Sandbox *alone* can't protect against [:material-package-variant-closed-remove: Supply Chain Attacks](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} by malicious developers. For that, sandboxing needs to be enforced by someone other than the developer themselves, as it is on the [App Store](https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/1/web/1#:~:text=All%20apps%20from%20the%20App%20Store%20are%20sandboxed%20to%20restrict%20access%20to%20data%20stored%20by%20other%20apps.).

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
codesign -dvvv --entitlements - <path to your app>
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
codesign -dv <path to your app>
```

If Hardened Runtime is enabled, you will see `flags=0x10000(runtime)`. The `runtime` output means Hardened Runtime is enabled. There might be other flags, but the runtime flag is what we're looking for here.

You can enable a column in Activity Monitor called "Restricted" which is a flag that prevents programs from injecting code via macOS's [dynamic linker](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html). Ideally, this should say "Yes".

##### Antivirus

macOS comes with two forms of [malware defense](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/1/web/1):

1. In primo luogo, la protezione dal lancio di malware è fornita dal processo di revisione dell'App Store per le applicazioni presenti su di esso, o *Notarizzazione* (parte di *Gatekeeper*), un procedimento in cui le app di terze parti sono scansionate in cerca di malware noti da Apple, prima di poter essere eseguite. Apps are required to be signed by the developers using a key given to them by Apple. This ensures that you are running software from the real developers. Notarization also requires that developers enable the Hardened Runtime for their apps, which limits methods of exploitation.
2. La protezione da altri malware e rimedi da malware esistenti sul tuo sistema è fornita da *XProtect*, un software antivirus più tradizionale, integrato su macOS.

We recommend against installing third-party antivirus software as they typically do not have the system-level access required to properly function anyway, because of Apple's limitations on third-party apps, and because granting the high levels of access they do ask for often poses an even greater security and privacy risk to your computer.

##### Backup

macOS comes with automatic backup software called [Time Machine](https://support.apple.com/HT201250), so you can create [encrypted backups](https://support.apple.com/guide/mac-help/keep-your-time-machine-backup-disk-secure-mh21241/mac) to an external drive or a network drive in the event of corrupted/deleted files.

### Sicurezza Hardware

Many modern security features in macOS—such as modern Secure Boot, hardware-level exploit mitigation, OS integrity checks, and file-based encryption—rely on Apple Silicon, and Apple's newer hardware always has the [best security](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). We only encourage the use of Apple Silicon, and not older Intel-based Mac computers or Hackintoshes.

Alcune di queste funzionalità di sicurezza moderne sono disponibili sui vecchi computer Mac con processore Intel con l'Apple T2 Security Chip, ma questo chip è suscettibile all'exploit *checkm8* che potrebbe comprometterne la sicurezza.

If you use Bluetooth accessories such as a keyboard, we recommend that you use official Apple ones as their firmware will [automatically be updated](https://support.apple.com/en-us/120303#:~:text=Firmware%20updates%20are%20automatically%20delivered%20in%20the%20background%20while%20the%20Magic%20Keyboard%20is%20actively%20paired%20to%20a%20device%20running%20macOS%2C%20iOS%2C%20iPadOS%2C%20or%20tvOS.) for you by macOS. Utilizzare accessori di terze parti va bene, ma dovresti ricordarti di installarne regolarmente gli aggiornamenti del firmware.

Apple's SoCs focus on [minimizing attack surface](https://support.apple.com/en-vn/guide/security/secf020d1074/web#:~:text=Security%2Dfocused%20hardware%20follows%20the%20principle%20of%20supporting%20limited%20and%20discretely%20defined%20functions%20to%20minimize%20attack%20surface.) by relegating security functions to dedicated hardware with limited functionality.

#### ROM di Avvio

macOS prevents malware persistence by only allowing official Apple software to run at boot time; this is known as [secure boot](https://support.apple.com/en-vn/guide/security/secac71d5623/1/web/1). Mac computers verify this with a bit of read-only memory on the SoC called the [boot ROM](https://support.apple.com/en-vn/guide/security/aside/sec5240db956/1/web/1), which is [laid down during the manufacturing of the chip](https://support.apple.com/en-vn/guide/security/secf020d1074/1/web/1#:~:text=which%20is%20laid%20down%20during%20Apple%20SoC%20fabrication).

La ROM di avvio forma la radice di fiducia del hardware. This ensures that malware cannot tamper with the boot process, since the boot ROM is immutable. Quando il tuo Mac si avvia, la ROM di avvio è la prima cosa eseguita, formando il primo collegamento nella catena di fiducia.

Mac computers can be configured to boot in [three security modes](https://support.apple.com/guide/deployment/startup-security-dep5810e849c/web#dep32fb404e1): *Full Security*, *Reduced Security*, and *Permissive Security*, with the default setting being Full Security. You should ideally be using Full Security mode and avoid things like **[kernel extensions](https://support.apple.com/guide/deployment/system-extensions-in-macos-depa5fb8376f/web#dep51e097f45)** that force you to lower your security mode. Assicurati di [verificare](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) di star utilizzando la modalità di Sicurezza Completa.

#### Secure Enclave

The **[Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/web)** is a security chip built into devices with Apple Silicon which is responsible for storing and generating encryption keys for data at rest as well as Face ID and Touch ID data. It contains its own [separate boot ROM](https://support.apple.com/en-vn/guide/security/sec59b0b31ff/web#sec43006c49f).

Puoi pensare a Secure Enclave come un hub di sicurezza del tuo dispositivo: include un motore crittografico AES e un meccanismo per memorizzare in sicurezza le tue chiavi crittografiche, ed è separato dal resto del sistema quindi, anche se il processore principale è compromesso, dovrebbe ancora essere sicuro.

#### Touch ID

La funzionalità Touch ID di Apple ti consente di sbloccare in sicurezza i tuoi dispositivi, utilizzando fattori biometrici.

Your biometric data [never leaves your device](https://www.apple.com/legal/privacy/data/en/touch-id/#:~:text=Touch%C2%A0ID%20data%20does%20not%20leave%20your%20device%2C%20and%20is%20never%20backed%20up%20to%20iCloud%20or%20anywhere%20else.); it's stored only in the Secure Enclave.

#### Disconnessione del Microfono Hardware

All laptops with Apple Silicon or the T2 chip feature a [hardware disconnect](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web) for the built-in microphone whenever the lid is closed. Ciò significa che non vi è modo per un utente malevolo, di ascoltare dal microfono del tuo Mac, anche se il sistema operativo è compromesso.

Nota che la fotocamera non presenta una disconnessione hardware, poiché la sua inquadratura è comunque oscurata, alla chiusura dello schermo.

#### Secure Camera Indicator

The built-in camera in a Mac is designed so that the camera can't turn on without the camera indicator light [also turning on](https://support.apple.com/en-us/102177#:~:text=The%20camera%20is%20engineered%20so%20that%20it%20can’t%20activate%20without%20the%20camera%20indicator%20light%20also%20turning%20on.%20This%20is%20how%20you%20can%20tell%20if%20your%20camera%20is%20on.).

#### Sicurezza del Processore Periferico

Computers have [built-in processors](https://support.apple.com/en-vn/guide/security/seca500d4f2b/1/web/1) other than the main CPU that handle things like networking, graphics, power management, etc. Questi processori possono avere una sicurezza insufficiente ed essere compromessi, dunque, Apple prova a minimizzarne l'esigenza nel proprio hardware.

Quando è necessario utilizzare uno di tali processori, Apple opera da fornitore per assicurarsi che il processore

- esegua il firmware verificato dalla CPU principale all'avvio
- abbia la propria catena di Avvio Sicuro
- segua standard crittografici minimi
- assicuri che i firmware malevoli siano revocati adeguatamente
- abbia le interfacce di debug disabilitate
- sia firmato con chiavi crittografiche di Apple

#### Protezioni di Accesso Diretto alla Memoria

Apple Silicon separates each component that requires [direct memory access](https://support.apple.com/guide/security/direct-memory-access-protections-seca4960c2b5/1/web/1). Ad esempio, una porta di Thunderbolt non può accedere alla memoria designata per il Kernel.

#### Terminal Secure Keyboard Entry

Enable [Secure Keyboard Entry](https://support.apple.com/guide/terminal/use-secure-keyboard-entry-trml109/mac) to prevent other apps from detecting what you type in the terminal.
