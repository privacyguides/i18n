---
meta_title: "Software di crittografia consigliati: VeraCrypt, Cryptomator, PicoCrypt e OpenPGP - Privacy Guides"
title: "Software di Crittografia"
icon: material/file-lock
description: La crittografia dei dati è il solo modo per controllare chi possa accedervi. Questi strumenti ti consentono di crittografare le tue email e qualsiasi altro file.
cover: encryption.webp
---

La crittografia dei dati è l'unico modo per controllare chi può accedervi. Se, al momento, non stai utilizzando alcun software di crittografia per il tuo disco rigido, le tue email o file, dovresti selezionare un'opzione qui.

## Multipiattaforma

Le opzioni qui elencate sono multipiattaforma e ottime per creare backup crittografati dei tuoi dati.

### Cryptomator (Cloud)

!!! recommendation

    ![Cryptomator logo](assets/img/encryption-software/cryptomator.svg){ align=right }
    
    **Cryptomator** è una soluzione per la crittografia progettata per salvare privatamente i file di qualsiasi provider cloud. Ti consente di creare cassaforti memorizzate su un'unità virtuale, i cui contenuti sono crittografati e sincronizzati con il tuo fornitore d'archiviazione su cloud.
    
    [:octicons-home-16: Home](https://cryptomator.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://docs.cryptomator.org/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/cryptomator){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://cryptomator.org/donate/){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.cryptomator)
        - [:simple-appstore: App Store](https://apps.apple.com/it/app/cryptomator-2/id1560822163)
        - [:simple-android: Android](https://cryptomator.org/android)
        - [:simple-windows11: Windows](https://cryptomator.org/downloads)
        - [:simple-apple: macOS](https://cryptomator.org/downloads)
        - [:simple-linux: Linux](https://cryptomator.org/downloads)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.cryptomator.Cryptomator)

Cryptomator utilizza la crittografiaa AES-256 per crittografare i file e i loro nomi. Cryptomator non può crittografare i metadati come marche orarie d'accesso, modifica e creazione, né il numero e le dimensioni dei file e delle cartelle.

Alcune librerie crittografiche di Cryptomator sono state [revisionate](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) da Cure53. Alcune delle librerie sottoposte a verifica sono: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) e [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). Non è stata controllata [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), che è una libreria usata da Cryptomator per iOS.

La documentazione di Cryptomator ne descrive l'[obiettivo di sicurezza](https://docs.cryptomator.org/en/latest/security/security-target/), [architettura di sicurezza](https://docs.cryptomator.org/en/latest/security/architecture/) e le [migliori pratiche](https://docs.cryptomator.org/en/latest/security/best-practices/) previsti, per l'utilizzo.

### Picocrypt (File)

!!! recommendation

    ![Picocrypt logo](assets/img/encryption-software/picocrypt.svg){ align=right }
    
    **Picocrypt** è un strumento semplice e di piccole dimensioni che fornisce tecniche di crittografia moderna. Picocrypt utilizza il cifrario sicuro XChaCha20 e la funzione di derivazione della chiave Argon2id per fornire un alto livello di sicurezza. Utilizza i moduli standard x/crypto di Go per le sue funzionalità di sicurezza.
    
    [:octicons-repo-16: Repository](https://github.com/HACKERALERT/Picocrypt){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/HACKERALERT/Picocrypt){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://opencollective.com/picocrypt){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-windows11: Windows](https://github.com/HACKERALERT/Picocrypt/releases)
        - [:simple-apple: macOS](https://github.com/HACKERALERT/Picocrypt/releases)
        - [:simple-linux: Linux](https://github.com/HACKERALERT/Picocrypt/releases)

### VeraCrypt (Disco)

!!! recommendation

    ![Logo di VeraCrypt](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
    ![Logo di VeraCrypt](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }
    
    **VeraCrypt** è un'utility libera con sorgente disponibile, utilizzata per la crittografia al volo. Può creare un disco virtuale crittografato in un file, crittografare una partizione o crittografare l'intero dispositivo di archiviazione con l'autenticazione antecedente l'avvio.
    
    [:octicons-home-16: Home](https://veracrypt.fr){ .md-button .md-button--primary }
    [:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title=Documentazione}
    [:octicons-code-16:](https://veracrypt.fr/code/){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-windows11: Windows](https://www.veracrypt.fr/en/Downloads.html)
        - [:simple-apple: macOS](https://www.veracrypt.fr/en/Downloads.html)
        - [:simple-linux: Linux](https://www.veracrypt.fr/en/Downloads.html)

VeraCrypt è un fork del progetto abbandonato TrueCrypt. Secondo i suoi sviluppatori, sono stati implementati dei miglioramenti alla sicurezza e, i problemi sollevati dall'iniziale controllo del codice di TrueCrypt sono stati risolti.

Crittografando con VeraCrypt, puoi selezionare [funzioni di hash](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme) differenti. Ti suggeriamo di selezionare **soltanto** [SHA-512](https://en.wikipedia.org/wiki/SHA-512), e il cifrario a blocchi [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard).

Truecrypt è stato [controllato numerose volte](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits), così come VeraCrypt, [controllato separatamente](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit).

## Crittografia dell'intero disco del sistema operativo

Per crittografare l'unità da cui si avvia il sistema operativo, in genere si consiglia di attivare il software di crittografia fornito con il sistema operativo piuttosto che utilizzare uno strumento di terze parti. Questo perché gli strumenti di crittografia nativi del sistema operativo spesso utilizzano caratteristiche specifiche del sistema operativo e dell'hardware, come il [cryptoprocessor](https://it.wikipedia.org/wiki/Cryptoprocessor) nel dispositivo, per proteggere il computer da attacchi fisici più avanzati. Per le unità secondarie e le unità esterne da cui *non* si effettua l'avvio, si consiglia comunque di utilizzare strumenti open-source come [VeraCrypt](#veracrypt-disk) rispetto a quelli indicati di seguito, perché offrono una maggiore flessibilità e consentono di evitare il vendor lock-in.

### BitLocker

!!! recommendation

    ![Logo di BitLocker](assets/img/encryption-software/bitlocker.png){ align=right }
    
    **BitLocker** è il programma di crittografia completa del volume, integrato con Microsoft Windows. Il motivo principale per cui lo consigliamo per la crittografia dell'unità di avvio è il suo [utilizzo di TPM](https://docs.microsoft.com/en-us/windows/security/information-protection/tpm/how-windows-uses-the-tpm). ElcomSoft, una società di analisi forense, ha scritto su questa funzione in [Understanding BitLocker TPM Protection](https://blog.elcomsoft.com/2021/01/understanding-BitLocker-tpm-protection/).
    
    [:octicons-info-16:](https://docs.microsoft.com/en-us/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title=Documentazione}

BitLocker è [supportato soltanto](https://support.microsoft.com/en-us/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838) dalle edizioni Pro, Enterprise ed Education di Windows. Può essere abilitato sulle edizioni Home, ammesso che soddisfino i prerequisiti.

??? example "Attivare BitLocker su Windows Home"

    Per abilitare BitLocker sulle edizioni "Home" di Windows, devi avere le partizioni formattate con una [Tabella di Partizione GUID](https://it.wikipedia.org/wiki/GUID_Partition_Table) e disporre di un modulo TPM (v1.2, 2.0+) dedicato. Potrebbe essere necessario [disabilitare la funzionalità "Crittografia dispositivo" non-Bitlocker](https://discuss.privacyguides.net/t/enabling-bitlocker-on-the-windows-11-home-edition/13303/5) (che è inferiore perché invia la chiave di recupero ai server di Microsoft) se è già attiva sul dispositivo prima di seguire questa guida.

    1. Apri il prompt dei comandi e verifica il formato della tabella di partizione dell'unità, con il seguente comando. Dovresti vedere "**GPT**" elencato sotto "Stile di Partizione":

        ```
        powershell Get-Disk
        ```

    2. Esegui questo comando (nel prompt dei comandi da admin), per verificare la tua versione di TPM. Dovresti vedere `2.0` o `1.2`, elencato affianco a `SpecVersion`:

        ```
        powershell Get-WmiObject -Namespace "root/cimv2/security/microsofttpm" -Class WIN32_tpm
        ```

    3. Accedi alle [Opzioni di Avvio Avanzate](https://support.microsoft.com/it-it/windows/opzioni-di-avvio-avanzate-inclusa-la-modalit%C3%A0-provvisoria-b90e7808-80b5-a291-d4b8-1a1af602b617). Devi riavviare premendo il tasto F8, prima dell'avvio di Windows e andare nel *prompt dei comandi* in **Risoluzione dei Problemi** → **Opzioni Avanzate** → **Prompt dei Comandi**.

    4. Accedi con il tuo profilo da amministratore e digita nel prompt dei comandi questo comando, per avviare la crittografia:

        ```
        manage-bde -on c: -used
        ```

    5. Chiudi il prompt dei comandi e procedi con l'avvio regolare di Windows.

    6. Apri il prompt dei comandi con privilegi da amministratore ed esegui i seguenti comandi:

        ```
        manage-bde c: -protectors -add -rp -tpm
        manage-bde -protectors -enable c:
        manage-bde -protectors -get c: > %UserProfile%\Desktop\BitLocker-Recovery-Key.txt
        ```

        !!! tip "Suggerimento"
   
        Esegui il backup di 'BitLocker-Recovery-Key.txt' sul tuo desktop, in un dispositivo d'archiviazione separato. La perdita del codice di recupero potrebbe risultare nella perdita dei dati.

### FileVault

!!! recommendation

    ![Logo di FileVault](assets/img/encryption-software/filevault.png){ align=right }
    
    **FileVault** è la soluzione per la crittografia rapida dei volumi, integrata su macOS. FileVault è consigliata perché [sfrutta](https://support.apple.com/guide/security/volume-encryption-with-filevault-sec4c6dc1b6e/web) le funzionalità di sicurezza hardware presenti su un SoC in silicio o un Chip di Sicurezza T2 di Apple.
    
    [:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title=Documentazione}

Consigliamo di memorizzare una chiave di recupero locale in un luogo sicuro, invece di utilizzare il tuo profilo di iCloud per il recupero.

### Linux Unified Key Setup

!!! recommendation

    ![Logo di LUKS](assets/img/encryption-software/luks.png){ align=right }
    
    **LUKS** è il metodo di FDE predefinito per Linux. È utilizzabile per crittografare interi volumi, partizioni, o creare contenitori crittografati.
    
    [:octicons-home-16: Home](https://gitlab.com/cryptsetup/cryptsetup/-/blob/main/README.md){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title=Documentazione}
    [:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup/){ .card-link title="Codice Sorgente" }

??? example "Creazione e apertura di contenitori crittografati"

    ```
    dd if=/dev/urandom of=/path-to-file bs=1M count=1024 status=progress
    sudo cryptsetup luksFormat /path-to-file
    ```


    #### Apertura di contenitori crittografati
    Consigliamo di aprire contenitori e volumi con `udisksctl`, poiché utilizza [Polkit](https://it.wikipedia.org/wiki/PolicyKit). Gran parte dei gestori di file, come quelli inclusi con i popolari ambienti desktop, possono sbloccare i file crittografati. Strumenti come [udiskie](https://github.com/coldfix/udiskie) possono essere eseguiti nella barra delle applicazioni e forniscono un'utile interfaccia utente.
    ```
    udisksctl loop-setup -f /path-to-file
    udisksctl unlock -b /dev/loop0
    ```

!!! note "Ricorda di eseguire il backup delle intestazioni dei volumi"

    Consigliamo di eseguire sempre il [back up delle intestazioni LUKS](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) in caso di guasto parziale dell'unità. Ciò può essere fatto con:

    ```
    cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
    ```

## Basati sul browser

La crittografia basata sul browser può essere utile quando devi crittografare un file, ma non puoi installare software o app sul tuo dispositivo.

### hat.sh

!!! recommendation

    ![Logo di hat.sh](assets/img/encryption-software/hat-sh.png#only-light){ align=right }
    ![Logo di hat.sh](assets/img/encryption-software/hat-sh-dark.png#only-dark){ align=right }
    
    **Hat.sh** è un'applicazione web che fornisce una crittografia dei file dal lato del client nel browser. Può anche essere ospitata autonomamente ed è utile se devi crittografare un file ma non puoi installare alcun software sul tuo dispositivo, a causa di politiche organizzative.
    
    [:octicons-globe-16: Sito web](https://hat.sh){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://hat.sh/about/){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://hat.sh/about/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/sh-dv/hat.sh){ .card-link title="Codice Sorgente" }
    :octicons-heart-16:{ .card-link title="I metodi di donazione si possono trovare in fondo al sito web" }

## Riga di comando

Gli strumenti con interfacce di riga di comando sono utili per integrare gli [script della shell](https://en.wikipedia.org/wiki/Shell_script).

### Kryptor

!!! recommendation

    ![Logo di Kryptor](assets/img/encryption-software/kryptor.png){ align=right }
    
    **Kryptor** è uno strumento gratuito e open source di crittografia e firma dei file, che utilizza algoritmi crittografici moderni e sicuri. Punta a essere una versione migliorata di[age](https://github.com/FiloSottile/age) e [Minisign](https://jedisct1.github.io/minisign/) per fornire un'alternativa semplice a GPG.
    
    [:octicons-home-16: Home](https://www.kryptor.co.uk){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.kryptor.co.uk/features#privacy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://www.kryptor.co.uk/tutorial){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://www.kryptor.co.uk/#donate){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-windows11: Windows](https://www.kryptor.co.uk)
        - [:simple-apple: macOS](https://www.kryptor.co.uk)
        - [:simple-linux: Linux](https://www.kryptor.co.uk)

### Tomb

!!! recommendation

    ![Logo di Tomb](assets/img/encryption-software/tomb.png){ align=right }
    
    **Tomb** è un wrapper della shell a riga di comando, per LUKS. Supporta la steganografia tramite [strumenti di terze parti](https://github.com/dyne/Tomb#how-does-it-work).
    
    [:octicons-home-16: Pagina principale](https://www.dyne.org/software/tomb){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://www.dyne.org/donate){ .card-link title=Contribuisci }

## OpenPGP

OpenPGP è talvolta necessario per incarichi specifici, come firmare digitalmente e crittografare un'email. PGP include molte funzionalità ed è [complesso](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html), dato che è in circolazione da molto tempo. Per gli incarichi come firmare o crittografare i file, suggeriamo le opzioni precedenti.

Crittografando con PGP, puoi configurare diverse opzioni nel tuo file `gpg.config`. Ti consigliamo di attenerti con le opzioni standard specificate nelle [Domande Frequenti degli utenti di GnuPG](https://www.gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

!!! tip "Utilizzare future-default quando si genera una chiave"

    [Generando le chiavi]https://www.gnupg.org/gph/en/manual/c14.html), consigliamo di utilizzare il comando 'future-default', istruendo GnuPG a utilizzare la crittografia moderna come [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) ed [Ed25519](https://ed25519.cr.yp.to/):

    ```bash
    gpg --quick-gen-key alice@example.com future-default
    ```

### GNU Privacy Guard

!!! recommendation

    ![Logo di GNU Privacy Guard](assets/img/encryption-software/gnupg.svg){ align=right }
    
    **GnuPG** è un'alternativa con licenza GPL alla suite PGP per software crittografici. GnuPG è conforme con [RFC 4880](https://tools.ietf.org/html/rfc4880), la specifica IETF corrente di OpenPGP. Il progetto GnuPG ha lavorato a una [bozza aggiornata](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh/) nel tentativo di modernizzare OpenPGP. GnuPG fa parte del progetto Free Software Foundation di GNU ed ha ricevuto un'importante [finanziamento](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) dal governo tedesco.
    
    [:octicons-home-16: Home](https://gnupg.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title=Documentazione}
    [:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="Codice Sorgente" }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
        - [:simple-windows11: Windows](https://gpg4win.org/download.html)
        - [:simple-apple: macOS](https://gpgtools.org)
        - [:simple-linux: Linux](https://gnupg.org/download/index.html#binary)

### GPG4win

!!! recommendation

    ![Logo di GPG4win](assets/img/encryption-software/gpg4win.svg){ align=right }
    
    **GPG4win** è un pacchetto per Windows di [Intevation e g10 Code](https://gpg4win.org/impressum.html). Include [vari strumenti](https://gpg4win.org/about.html), che possono assisterti nell'utilizzo di GPG su Microsoft Windows. Il progetto è stato avviato e originariamente [finanziato dall'](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography)Ufficio Federale Tedesco per la Sicurezza delle Informazioni (BSI) nel 2005.
    
    [:octicons-home-16: Home](https://gpg4win.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title=Documentazione}
    [:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title=Contribuisci }
    
    ??? downloads "Scarica"
    
        - [:simple-windows11: Windows](https://gpg4win.org/download.html)

### GPG Suite

!!! note "Nota"

    Suggeriamo [Canary Mail](email-clients.md#canary-mail) per utilizzare PGP con le email sui dispositivi iOS.

!!! recommendation

    ![Logo di GPG Suite](assets/img/encryption-software/gpgsuite.png){ align=right }
    
    **GPG Suite** fornisce il supporto OpenPGP per [Apple Mail](email-clients.md#apple-mail) e macOS.
    
    Consigliamo di dare un'occhiata ai loro [Primi passi](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email) e alla loro [Base di Conoscenza](https://gpgtools.tenderapp.com/kb) per supporto.
    
    [:octicons-home-16: Home](https://gpgtools.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Codice Sorgente" }
    
    ??? downloads "Scarica"
    
        - [:simple-apple: macOS](https://gpgtools.org)

### OpenKeychain

!!! recommendation

    ![Logo di OpenKeychain](assets/img/encryption-software/openkeychain.svg){ align=right }
    
    **OpenKeychain** è un'implementazione Android di GnuPG. È comunementa richiesta da client mail come [K-9 Mail](email-clients.md#k-9-mail) e [FairEmail](email-clients.md#fairemail) e da altre app Android per fornire supporto alla crittografia. Cure53 ha completato un [controllo di sicurezza](https://www.openkeychain.org/openkeychain-3-6) di OpenKeychain 3.6 a ottobre 2015. I dettagli tecnici sul controllo e le soluzioni di OpenKeychain possono essere trovate [qui](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).
    
    [:octicons-home-16: Home](https://www.openkeychain.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.openkeychain.org/help/privacy-policy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://www.openkeychain.org/faq/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="Codice Sorgente" }
    
    ??? downloads "Scarica"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

### Requisiti minimi

- Le applicazioni di crittografia multipiattaforma devono essere open source.
- Le app di crittografia dei file devono supportare la decrittografia su Linux, macOS e Windows.
- Le app per la crittografia del disco esterno devono supportare la decrittografia su Linux, macOS e Windows.
- Le app di crittografia del disco interno (OS) devono essere multipiattaforma o integrate nativamente al sistema operativo.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Le app di crittografia del Sistema Operativo (FDE) dovrebbero utilizzare la sicurezza hardware, come TPM o Secure Enclave.
- Le app per la crittografia dei file dovrebbero avere supporto da prime o terze parti, per le piattaforme mobili.
