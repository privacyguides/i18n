---
meta_title: "Recommended Encryption Software: VeraCrypt, Cryptomator, and OpenPGP - Privacy Guides"
title: "Software di crittografia"
icon: material/file-lock
description: La crittografia dei dati è l'unico modo per controllare chi può accedervi. Questi strumenti ti consentono di crittografare le tue email e qualsiasi altro file.
cover: encryption.webp
---

**Encryption** is the only secure way to control who can access your data. If you are currently not using encryption software for your hard disk, emails, or files, you should pick an option here.

## Multipiattaforma

The options listed here are available on multiple platforms and great for creating encrypted backups of your data.

### Cryptomator (Cloud)

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Attacchi Passivi](basics/common-threats.md#security-and-privacy ""){.pg-orange}

<div class="admonition recommendation" markdown>

![Cryptomator logo](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** is an encryption solution designed for privately saving files to any cloud [:material-server-network: Service Provider](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }, eliminating the need to trust that they won't access your files. Ti consente di creare cassaforti memorizzate su un'unità virtuale, i cui contenuti sono crittografati e sincronizzati con il tuo fornitore d'archiviazione su cloud.

[:octicons-home-16: Homepage](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.cryptomator.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/cryptomator){ .card-link title="Source Code" }
[:octicons-heart-16:](https://cryptomator.org/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.cryptomator)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1560822163)
- [:simple-android: Android](https://cryptomator.org/android)
- [:fontawesome-brands-windows: Windows](https://cryptomator.org/downloads)
- [:simple-apple: macOS](https://cryptomator.org/downloads)
- [:simple-linux: Linux](https://cryptomator.org/downloads)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.cryptomator.Cryptomator)

</details>

</div>

Cryptomator utilizza la crittografiaa AES-256 per crittografare i file e i loro nomi. Cryptomator non può crittografare i metadati come marche orarie d'accesso, modifica e creazione, né il numero e le dimensioni dei file e delle cartelle.

Cryptomator is free to use on all desktop platforms, as well as on iOS in "read only" mode. Cryptomator offers [paid](https://cryptomator.org/pricing) apps with full functionality on iOS and Android. The Android version can be purchased anonymously via [ProxyStore](https://cryptomator.org/coop/proxystore).

Alcune librerie crittografiche di Cryptomator sono state [revisionate](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) da Cure53. Alcune delle librerie sottoposte a verifica sono: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) e [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). Non è stata controllata [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), che è una libreria usata da Cryptomator per iOS.

Cryptomator's documentation details its intended [security target](https://docs.cryptomator.org/en/latest/security/security-target), [security architecture](https://docs.cryptomator.org/en/latest/security/architecture), and [best practices](https://docs.cryptomator.org/en/latest/security/best-practices) for use in further detail.

### VeraCrypt (Disco)

<small>Protects against the following threat(s):</small>

- [:material-target-account: Attacchi Mirati](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![Logo di VeraCrypt](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![Logo di VeraCrypt](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt** è un'utility libera con sorgente disponibile, utilizzata per la crittografia al volo. Può creare un disco virtuale crittografato in un file, crittografare una partizione o crittografare l'intero dispositivo di archiviazione con l'autenticazione antecedente l'avvio.

[:octicons-home-16: Homepage](https://veracrypt.fr){ .md-button .md-button--primary }
[:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://veracrypt.fr/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://veracrypt.fr/en/Downloads.html)
- [:simple-apple: macOS](https://veracrypt.fr/en/Downloads.html)
- [:simple-linux: Linux](https://veracrypt.fr/en/Downloads.html)

</details>

</div>

VeraCrypt è un fork del progetto abbandonato TrueCrypt. Secondo i suoi sviluppatori, sono stati implementati dei miglioramenti alla sicurezza e, i problemi sollevati dall'iniziale controllo del codice di TrueCrypt sono stati risolti.

Crittografando con VeraCrypt, puoi selezionare [funzioni di hash](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme) differenti. Ti suggeriamo di selezionare **soltanto** [SHA-512](https://en.wikipedia.org/wiki/SHA-512), e il cifrario a blocchi [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard).

TrueCrypt has been [audited a number of times](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits), and VeraCrypt has also been [audited separately](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit).

## Operating System Encryption

<small>Protects against the following threat(s):</small>

- [:material-target-account: Attacchi Mirati](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Built-in OS encryption solutions generally leverage hardware security features such as a [secure cryptoprocessor](basics/hardware.md#tpmsecure-cryptoprocessor). Therefore, we recommend using the built-in encryption solutions for your operating system. For cross-platform encryption, we still recommend [cross-platform tools](#multi-platform) for additional flexibility and to avoid vendor lock-in.

<details class="warning" markdown>

<summary>Shut devices down when not in use.</summary>

Powering off your devices when they’re not in use provides the highest level of security, as it minimizes the attack surface of your FDE method by ensuring no encryption keys remain in memory.

</details>

### BitLocker

<div class="admonition recommendation" markdown>

![BitLocker logo](assets/img/encryption-software/bitlocker.png){ align=right }

**BitLocker** is the full volume encryption solution bundled with Microsoft Windows that uses the Trusted Platform Module ([TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm)) for hardware-based security.

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title="Documentation" }

</details>

</div>

BitLocker is [officially supported](https://support.microsoft.com/en-us/windows/bitlocker-overview-44c0c61c-989d-4a69-8822-b95cd49b1bbf) on the Pro, Enterprise, and Education editions of Windows. The Home edition only supports automatic [Device Encryption](https://support.microsoft.com/en-us/windows/device-encryption-in-windows-cf7e2b6f-3e70-4882-9532-18633605b7df) and must meet specific hardware requirements. If you’re using the Home edition, we recommend [upgrading to Pro](https://support.microsoft.com/en-us/windows/upgrade-windows-home-to-windows-pro-ef34d520-e73f-3198-c525-d1a218cc2818), which can be done without reinstalling Windows or losing your files.

Pro and higher editions also support the more secure pre-boot [TPM+PIN](https://learn.microsoft.com/en-us/windows/security/operating-system-security/data-protection/bitlocker/faq#what-is-the-difference-between-a-tpm-owner-password--recovery-password--recovery-key--pin--enhanced-pin--and-startup-key) feature, configured through the appropriate [group policy](os/windows/group-policies.md#bitlocker-drive-encryption) settings. The PIN is rate limited and the TPM will panic and lock access to the encryption key either permanently or for a period of time if someone attempts to brute force access.

</details>

### FileVault

<div class="admonition recommendation" markdown>

![Logo di FileVault](assets/img/encryption-software/filevault.png){ align=right }

**FileVault** è la soluzione per la crittografia rapida dei volumi, integrata su macOS. FileVault takes advantage of the [hardware security capabilities](os/macos-overview.md#hardware-security) present on an Apple Silicon SoC or T2 Security Chip.

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title="Documentation" }

</details>

</div>

We advise against using your iCloud account for recovery; instead, you should securely store a local recovery key on a separate storage device.

### Linux Unified Key Setup

<div class="admonition recommendation" markdown>

![Logo di LUKS](assets/img/encryption-software/luks.png){ align=right }

**LUKS** è il metodo di FDE predefinito per Linux. È utilizzabile per crittografare interi volumi, partizioni, o creare contenitori crittografati.

[:octicons-repo-16: Repository](https://gitlab.com/cryptsetup/cryptsetup#what-the-){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup){ .card-link title="Source Code" }

</details>

</div>

<details class="example" markdown>
<summary>Creazione e apertura di container cifrati</summary>

```bash
dd if=/dev/urandom of=/path-to-file bs=1M count=1024 status=progress
sudo cryptsetup luksFormat /path-to-file
```

#### Apertura di container cifrati

Consigliamo l'apertura di container e volumi con `udisksctl` poiché utilizza [Polkit](https://en.wikipedia.org/wiki/Polkit). Gran parte dei gestori di file, come quelli inclusi con i popolari ambienti desktop, possono sbloccare i file crittografati. Strumenti come [udiskie](https://github.com/coldfix/udiskie) possono essere eseguiti nella barra delle applicazioni e fornire un'utile interfaccia utente.

```bash
udisksctl loop-setup -f /path-to-file
udisksctl unlock -b /dev/loop0
```

</details>

<div class="admonition note" markdown>
<p class="admonition-title">Ricorda di eseguire il backup delle intestazioni del volume</p>

Consigliamo di eseguire sempre il [back up delle intestazioni LUKS](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) in caso di guasto parziale dell'unità. Questo può essere fatto con:

```bash
cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
```

</div>

## Riga di comando

<small>Protects against the following threat(s):</small>

- [:material-target-account: Attacchi Mirati](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Gli strumenti con interfacce di riga di comando sono utili per integrare gli [script della shell](https://en.wikipedia.org/wiki/Shell_script).

### Kryptor

<div class="admonition recommendation" markdown>

![Logo di Kryptor](assets/img/encryption-software/kryptor.png){ align=right }

**Kryptor** è uno strumento gratuito e open source di crittografia e firma dei file, che utilizza algoritmi crittografici moderni e sicuri. It aims to be a better version of [age](https://github.com/FiloSottile/age) and [Minisign](https://jedisct1.github.io/minisign) to provide a simple, easier alternative to GPG.

[:octicons-home-16: Homepage](https://kryptor.co.uk){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kryptor.co.uk/features#privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kryptor.co.uk/tutorial){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kryptor.co.uk/#donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://kryptor.co.uk)
- [:simple-apple: macOS](https://kryptor.co.uk)
- [:simple-linux: Linux](https://kryptor.co.uk)

</details>

</div>

### Tomb

<div class="admonition recommendation" markdown>

![Logo di Tomb](assets/img/encryption-software/tomb.png){ align=right }

**Tomb** è un wrapper della shell a riga di comando, per LUKS. It supports steganography via [third-party tools](https://dyne.org/software/tomb/#advanced-usage).

[:octicons-home-16: Homepage](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Source Code" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title="Contribute" }

</details>

</div>

## OpenPGP

<small>Protects against the following threat(s):</small>

- [:material-target-account: Attacchi Mirati](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Attacchi Passivi](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fornitori di Servizi](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

OpenPGP è talvolta necessario per incarichi specifici, come firmare digitalmente e crittografare un'email. PGP include molte funzionalità ed è [complesso](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html), dato che è in circolazione da molto tempo. Per gli incarichi come firmare o crittografare i file, suggeriamo le opzioni precedenti.

Crittografando con PGP, puoi configurare diverse opzioni nel tuo file `gpg.config`. We recommend staying with the standard options specified in the [GnuPG user FAQ](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

<div class="admonition tip" markdown>
<p class="admonition-title">Utilizzare le impostazioni predefinite future quando si genera una chiave</p>

When [generating keys](https://gnupg.org/gph/en/manual/c14.html) we suggest using the `future-default` command as this will instruct GnuPG use modern cryptography such as [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) and [Ed25519](https://ed25519.cr.yp.to):

```bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU Privacy Guard

<div class="admonition recommendation" markdown>

![Logo di GNU Privacy Guard](assets/img/encryption-software/gnupg.svg){ align=right }

**GnuPG** è un'alternativa con licenza GPL alla suite PGP per software crittografici. GnuPG è conforme con [RFC 4880](https://tools.ietf.org/html/rfc4880), la specifica IETF corrente di OpenPGP. The GnuPG project has been working on an [updated draft](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh) in an attempt to modernize OpenPGP. GnuPG fa parte del progetto Free Software Foundation di GNU ed ha ricevuto un'importante [finanziamento](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) dal governo tedesco.

[:octicons-home-16: Homepage](https://gnupg.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)
- [:simple-apple: macOS](https://gpgtools.org)
- [:simple-linux: Linux](https://gnupg.org/download/index.html#binary)

</details>

</div>

### GPG4win

<div class="admonition recommendation" markdown>

![Logo di GPG4win](assets/img/encryption-software/gpg4win.svg){ align=right }

**GPG4win** è un pacchetto per Windows di [Intevation e g10 Code](https://gpg4win.org/impressum.html). Include [vari strumenti](https://gpg4win.org/about.html), che possono assisterti nell'utilizzo di GPG su Microsoft Windows. Il progetto è stato avviato e originariamente [finanziato dall'](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography)Ufficio Federale Tedesco per la Sicurezza delle Informazioni (BSI) nel 2005.

[:octicons-home-16: Homepage](https://gpg4win.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="Source Code" }
[:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)

</details>

</div>

### GPG Suite

<div class="admonition recommendation" markdown>

![GPG Suite logo](assets/img/encryption-software/gpgsuite.png){ align=right }

**GPG Suite** provides OpenPGP support for [Apple Mail](email-clients.md#apple-mail-macos) and other email clients on macOS.

We recommend taking a look at their [First steps](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email) and [Knowledge Base](https://gpgtools.tenderapp.com/kb) for support.

[:octicons-home-16: Homepage](https://gpgtools.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-apple: macOS](https://gpgtools.org)

</details>

</div>

Currently, GPG Suite does [not yet](https://gpgtools.com/sequoia) have a stable release for macOS Sonoma and later.

### OpenKeychain

<div class="admonition recommendation" markdown>

![OpenKeychain logo](assets/img/encryption-software/openkeychain.svg){ align=right }

**OpenKeychain** is an implementation of GnuPG for Android. It's commonly required by mail clients such as [Thunderbird](email-clients.md#thunderbird), [FairEmail](email-clients.md#fairemail-android), and other Android apps to provide encryption support.

[:octicons-home-16: Homepage](https://openkeychain.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://openkeychain.org/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://openkeychain.org/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

Cure53 completed a [security audit](https://openkeychain.org/openkeychain-3-6) of OpenKeychain 3.6 in October 2015. The published audit and OpenKeychain's solutions to the issues raised in the audit can be found [here](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

### Requisiti minimi

- Le applicazioni di crittografia multipiattaforma devono essere open source.
- Le app di crittografia dei file devono supportare la decrittografia su Linux, macOS e Windows.
- Le app per la crittografia del disco esterno devono supportare la decrittografia su Linux, macOS e Windows.
- Le app di crittografia del disco interno (OS) devono essere multipiattaforma o integrate nativamente al sistema operativo.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Le app di crittografia del Sistema Operativo (FDE) dovrebbero utilizzare la sicurezza hardware, come TPM o Secure Enclave.
- Le app per la crittografia dei file dovrebbero avere supporto da prime o terze parti, per le piattaforme mobili.
