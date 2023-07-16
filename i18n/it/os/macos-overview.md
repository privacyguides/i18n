---
title: Panoramica di macOS
icon: material/apple-finder
description: macOS è il sistema operativo desktop di Apple che opera con il loro hardware, fornendo grande sicurezza.
---

**macOS** è un sistema operativo Unix sviluppato da Apple per i propri computer Mac. Per migliorare la privacy su macOS, puoi disabilitare le funzionalità di telemetria e rafforzare le impostazioni di privacy e sicurezza esistenti.

I più datati Mac e Hackintosh basati su Intel non supportano tutte le funzionalità di sicurezza offerte da macOS. Per migliorare la sicurezza dei dati, consigliamo di utilizzare un Mac più recente, con [Apple Silicon](https://support.apple.com/en-us/HT211814).

## Note sulla Privacy

Esistono alcune notevoli preoccupazioni sulla privacy con macOS, che dovremmo considerare. Queste sono relative allo stesso sistema operativo, e non ad altri servizi e app di Apple.

### Blocco di Attivazione

I nuovissimi dispositivi di Apple silicon sono configurabili senza una connessione a Internet. Tuttavia, recuperare o ripristinare il tuo Mac **richiederà** una connessione a Internet, affinché i server di Apple possano verificarlo rispetto al database del Blocco di Attivazione, dei dispositivi perduti o rubati.

### Controlli di Revoca dell'App

macOS esegue controlli online quando apri un'app, per verificare che questa non contenga malware noti e se il certificato di firma dello sviluppatore è stato revocato.

Precedentemente, questi controlli erano eseguiti tramite un protocollo crittografato OCSP, le cui informazioni sulle app che esegui sulla tua rete, sarebbero potute trapelare. Apple ha aggiornato il proprio servizio OCSP per utilizzare la crittografia HTTPS nel 2021 e ha [pubblicato le informazioni](https://support.apple.com/HT202491) sulla propria politica di registrazione per questo servizio. Inoltre, hanno promesso di aggiungere un meccanismo per consentire alle persone di disattivare questo controllo online, sebbene questo non sia stato aggiunto a macOS fino a luglio 2023.

Sebbene [puoi](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private/) disattivare manualmente questo controllo in maniera relativamente facile, consigliamo di non farlo, a meno che non sia molto compromesso dai controlli di revoca eseguiti da macOS, poiché svolgono un ruolo importante nell'assicurarsi che le app compromesse siano bloccate dall'esecuzione.

## Configurazione consigliata

Il tuo profilo, quando configuri per la prima volta Mac, sarà un profilo Amministratore, avente privilegi maggiori di un profilo utente Standard. macOS presenta numerose protezioni che impediscono a malware e altri programmi di abusare dei tuoi privilegi da Amministratore, così che l'utilizzo di questo profilo sia, in generale, sicuro.

Tuttavia, exploit nelle utility protettive, come `sudo`, sono stati [scoperti in passato](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass/). Se desideri evitare la possibilità che i programmi che esegui abusino dei tuoi privilegi da Amministratore, potresti considerare di creare un secondo profilo utente Standard, da utilizzare per le operazioni quotidiane. Ciò presenta l'ulteriore beneficio di rendere più ovvio quando un'app necessita dell'accesso da amministratore, poiché ti richiederà le credenziali ogni volta.

Se utilizzi un secondo profilo, non è rigorosamente necessario connettersi al tuo profilo da Amministratore originale, dalla schermata d'accesso di macOS. Quando stai facendo qualcosa da utente Standard che richieda le autorizzazioni da Amministratore, il sistema dovrebbe richiederti l'autenticazione, dove puoi inserire le tue credenziali da Amministratore, pur essendo un utente Standard, una tantum. Apple fornisce [supporto](https://support.apple.com/HT203998) per nascondere il tuo profilo da Amministratore, se preferisci visualizzare un singolo profilo sulla tua schermata di accesso.

Altrimenti, puoi utilizzare un'utility come [macOS Enterprise Privileges](https://github.com/SAP/macOS-enterprise-privileges) per intensificare su richiesta i diritti da Amministratore, ma ciò potrebbe essere vulnerabile ad alcuni exploit non ancora scoperti, come tutte le protezioni basate su software.

### iCloud

Gran parte delle preoccupazioni su privacy e sicurezza con i prodotti di Apple sono relative ai loro *servizi su cloud*, non al loro hardware o software. Quando utilizzi i servizi di Apple come iCloud, gran parte delle tue informazioni sono memorizzate sui loro server e protetti dalle chiavi *cui Apple ha accesso* di default. Questo livello d'accesso è stato occasionalmente abusato dalle autorità per aggirare il fatto che i tuoi dati sono altrimenti crittografati in sicurezza sul tuo dispositivo e, ovviamente, Apple è vulnerabile alle violazioni di dati, come ogni altra azienda.

Dunque, se utilizzi iCloud, dovresti [abilitare la **Protezione Avanzata dei Dati**](https://support.apple.com/HT212520). Questa, crittografa praticamente tutti i tuoi dati di iCloud con chiavi memorizzate sui tuoi dispositivi (crittografia end-to-end), piuttosto che sui server di Apple, così che i tuoi dati di iCloud siano protetti nel caso di una violazione di dati, e altrimenti nascosti da Apple.

### Impostazioni di Sistema

Esistono numerose impostazioni integrate che dovresti confermare o modificare per proteggere il tuo sistema. Apri l'app delle **Impostazioni**:

#### Bluetooth

- [ ] Rimuovi la spunta da **Bluetooth** (a meno che tu non lo stia utilizzando al momento)

#### Rete

A seconda del fatto che tu stia utilizzando la **Wi-Fi** o il cavo **Ethernet** (denotato da un puntino verde e la parola "connesso"), clicca sull'icona corrispondente.

Clicca sul pulsante dei "Dettagli" affianco al nome della tua rete:

- [x] Spunta **Limita monitoraggio indirizzo IP**

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

#### Privacy & Sicurezza

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

##### Sicurezza

Le app dall'Apple Store sono soggette a linee guida di sicurezza più rigide, come un sandboxing più rigido. Se le sole app che necessiti sono disponibili dall'App Store, cambia l'impostazione **Consenti applicazioni scaricate da** ad **App Store**, per impedire l'esecuzione accidentale di altre app. Questa è una buona opzione, in particolare se stai configurando una macchina per altri utenti meno tecnici, come bambini.

Inoltre, se scegli di consentire le applicazioni da sviluppatori identificati, sii cauto sulle app che esegui e da dove le ottieni.

##### FileVault

Sui dispositivi moderni con una Zona Franca Sicura (Chip di Sicurezza Apple T2, Apple silicon), i tuoi dati sono sempre crittografati, ma sono automaticamente decrittografati da una chiave hardware, se il tuo dispositivo non rileva di esser stato manomesso. Abilitare FileVault richiede inoltre la tua password per decrittografare i tuoi dati, migliorando ampiamente la sicurezza, specialmente quando spento o prima del primo accesso all'accensione.

Sui vecchi computer Mac basati su Intel, FileVault è la sola forma di crittografia del disco disponibile di default, e dovrebbe sempre essere abilitata.

- [x] Clicca su **Attiva**

##### Modalità Lockdown

La [Modalità Lockdown](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) disabilita alcune funzionalità per poter migliorare la sicurezza. Alcune app o funzionalità non funzioneranno allo stesso modo di quanto sono disattivate, ad esempio, [JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers/) e [WASM](https://developer.mozilla.org/en-US/docs/WebAssembly) sono disabilitate su Safari, con la Modalità di Lockdown abilitata. Consigliamo di abilitare la Modalità di Lockdown e di scoprire se impatta significativamente sul tuo utilizzo: è facile convivere con molte delle modifiche che effettua.

- [x] Clicca su **Attiva**

### Randomizzazione dell'indirizzo MAC

A differenza di iOS, macOS non ti dà un'opzione per rendere casuale il tuo indirizzo MAC nelle impostazioni, quindi, dovrai farlo con un comando o uno script.

Apri il tuo Terminale e inserisci questo comando per casualizzare il tuo indirizzo MAC:

``` zsh
openssl rand -hex 6 | sed 's/\(..\)/\1:/g; s/.$//' | xargs sudo ifconfig en1 ether 
```

en1 è il nome dell'interfaccia per cui stai modificando l'indirizzo MAC. Questo potrebbe non essere quello corretto su ogni Mac, quindi, per verificare, puoi tenere premuto il tasto opzioni e cliccare sul simbolo della Wi-Fi nella parte superiore destra della tua schermata.

Questo sarà ripristinato al riavvio.

## Protezioni di Sicurezza

macOS utilizza la difesa approfondita, affidandosi a svariati livelli di protezioni basati su software e hardware, con proprietà differenti. Ciò assicura che un fallimento su un livello, non comprometta la sicurezza generale del sistema.

### Sicurezza del Software

!!! warning "Attenzione"

    macOS ti consente di installare gli aggiornamenti beta. Questi sono instabili e potrebbero comportare un'ulteriore telemetria, essendo per scopi di test. Per questo, ti consigliamo di evitare i software in beta, in generale.

#### Volume di Sistema Firmato

i componenti di sistema di macOS sono protetti in un volume di sistema firmato di sola lettura, a significare che né tu né un malware possiate alterare importanti file di sistema.

Il volume di sistema è verificato mentre in esecuzione e qualsiasi dato non sia firmato con una firma crittografica valida da Apple, sarà rifiutato.

#### Protezione dell'Integrità di Sistema

macOS imposta certe limitazioni di sicurezza, che non sono sovrascrivibili. Queste, sono dette Controlli d'Accesso Obbligatori e formano la base del sandbox, controllo genitori e Protezione dell'Integrità di Sistema su macOS.

La Protezione dell'Integrità di Sistema rende le posizioni dei file di sola lettura, per proteggere dalla modifica da parte di codice dannoso. Questa si aggiunge alla Protezione dell'Integrità del Kernel basata sul hardware, che evita che il kernel sia modificata in memoria.

#### Sicurezza delle Applicazioni

##### App Sandbox

Le app di macOS scaricate dall'App Store devono essere testate utilizzando [App Sandbox](https://developer.apple.com/documentation/security/app_sandbox).

!!! warning "Attenzione"

    I software scaricati al di fuori dell'App Store ufficiale non devono essere testate. Dovresti evitare i software non provenienti dall'App Store, il più possibile.

##### Antivirus

macOS presenta due forme di difesa dai malware:

1. In primo luogo, la protezione dal lancio di malware è fornita dal processo di revisione dell'App Store per le applicazioni presenti su di esso, o *Notarizzazione* (parte di *Gatekeeper*), un procedimento in cui le app di terze parti sono scansionate in cerca di malware noti da Apple, prima di poter essere eseguite.
2. La protezione da altri malware e rimedi da malware esistenti sul tuo sistema è fornita da *XProtect*, un software antivirus più tradizionale, integrato su macOS.

Sconsigliamo di installare software antivirus di terze parti, poiché, tipicamente, non hanno accesso a livello di sistema, necessario per funzionare propriamente, a causa di limitazioni di Apple sulle app di terze parti, e poiché garantire gli alti livelli d'accesso da essi richiesti, causa spesso un rischio sulla sicurezza e privacy maggiore al tuo computer.

##### Backups

macOS presenta un software di backup automatico chiamato [Time Machine](https://support.apple.com/HT201250), così, puoi creare dei backup crittografati su un'unità esterna o di rete, nel caso di file corrotti/eliminati.

### Sicurezza Hardware

Molte funzionalità di sicurezza moderne su macOS, come Avvio Sicuro, la mitigazione degli exploit a livello hardware, i controlli d'integrità dell'OS e la crittografia basata sui file, si affidano ad Apple silicon e i più nuovi hardware di Apple hanno sempre la [migliore sicurezza](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). Incoraggiamo esclusivamente l'utilizzo di Apple silicon, e non dei precedenti computer Mac o Hackintosh basati su Intel.

Alcune di queste funzionalità di sicurezza moderne sono disponibili sui vecchi computer Mac basati su Intel con il Chip di Sicurezza Apple T2 ma, tale chip, è suscettivile all'exploit *checkm8*, che potrebbe comprometterne la sicurezza.

Se utilizzi accessori Bluetooth come una tastiera, consigliamo di utilizzarne di ufficiali di Apple, poiché il loro firmware sarà automaticamente aggiornato per te da macOS. Utilizzare accessori di terze parti va bene, ma dovresti ricordarti di installarne regolarmente gli aggiornamenti del firmware.

I Sistemi su Chip di Apple mirano a minimizzare la superficie di attacco relegando le funzioni di sicurezza ad hardware dedicato con funzionalità limitate.

#### ROM di Avvio

macOS impedisce la persistenza dei malware, consntendo soltanto ai software Apple ufficiali di essere eseguiti all'avvio; ciò è noto come avvio di sicurezza. I computer Mac verificano ciò con un po' di memoria di sola lettura sul Sistema su Chip, detta ROM di avvio, stabilita durante la produzione del chip.

La ROM di avvio forma la radice di fiducia del hardware. Ciò assicura che i malware non possano manomettere il processo di avvio. Quando il tuo Mac si avvia, la ROM di avvio è la prima cosa eseguita, formando il primo collegamento nella catena di fiducia.

I computer Mac sono configurabili per avviarsi in tre modalità di sicurezza: *Sicurezza Completa*, *Sicurezza Ridotta* e *Sicurezza Permissiva*, dove la prima è l'impostazione predefinita. Idealmente, dovresti utilizzare la modalità di Sicurezza Completa ed evitare cose come le **estensioni del Kernel**, che ti forzano a ridurre la tua modalità di sicurezza. Assicurati di [verificare](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) di star utilizzando la modalità di Sicurezza Completa.

#### Secure Enclave

Secure Enclave è un chip di sicurezza integrato nei dispositivi con Apple silicon, responsabile della memorizzazione e generazione delle chiavi crittografiche per i dati inattivi, nonché per i dati di Face ID e Touch ID. Contiene la propria ROM di avvio separata.

Puoi pensare a Secure Enclave come un hub di sicurezza del tuo dispositivo: include un motore crittografico AES e un meccanismo per memorizzare in sicurezza le tue chiavi crittografiche, ed è separato dal resto del sistema quindi, anche se il processore principale è compromesso, dovrebbe ancora essere sicuro.

#### Touch ID

La funzionalità Touch ID di Apple ti consente di sbloccare in sicurezza i tuoi dispositivi, utilizzando fattori biometrici.

I tuoi dati biometrici non abbandonano mai il tuo dispositivo; sono memorizzati soltanto nel Secure Enclave.

#### Disconnessione del Microfono Hardware

Tutti i portatili con Apple silicon o il chip T2, includono una disconnessione hardware per il microfono integrato, alla chiusura dello schermo. Ciò significa che non vi è modo per un utente malevolo, di ascoltare dal microfono del tuo Mac, anche se il sistema operativo è compromesso.

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

Apple silicon separa ogni componente che richieda l'accesso diretto alla memoria. Ad esempio, una porta di Thunderbolt non può accedere alla memoria designata per il Kernel.

## Fonti

- [Sicurezza della Piattaforma di Apple](https://support.apple.com/guide/security/welcome/web)
