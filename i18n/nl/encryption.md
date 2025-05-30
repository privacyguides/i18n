---
meta_title: "Recommended Encryption Software: VeraCrypt, Cryptomator, PicoCrypt, and OpenPGP - Privacy Guides"
title: "Encryptie Software"
icon: material/file-lock
description: Encryptie van gegevens is de enige manier om te controleren wie er toegang toe heeft. These tools allow you to encrypt your emails and any other files.
cover: encryption.webp
---

**Encryption** is the only secure way to control who can access your data. If you are currently not using encryption software for your hard disk, emails, or files, you should pick an option here.

## Multi-platform

The options listed here are available on multiple platforms and great for creating encrypted backups of your data.

### Cryptomator (Cloud)

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Passieve aanvallen](basics/common-threats.md#security-and-privacy ""){.pg-orange}

<div class="admonition recommendation" markdown>

![Cryptomator logo](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** is an encryption solution designed for privately saving files to any cloud [:material-server-network: Service Provider](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }, eliminating the need to trust that they won't access your files. Hiermee kunt u kluizen maken die worden opgeslagen op een virtuele schijf, waarvan de inhoud wordt gecodeerd en gesynchroniseerd met uw cloudopslagprovider.

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

Cryptomator maakt gebruik van AES-256 encryptie om zowel bestanden als bestandsnamen te versleutelen. Cryptomator kan geen metadata versleutelen, zoals tijdstempels voor toegang, wijziging en creatie, noch het aantal en de grootte van bestanden en mappen.

Cryptomator is free to use on all desktop platforms, as well as on iOS in "read only" mode. Cryptomator offers [paid](https://cryptomator.org/pricing) apps with full functionality on iOS and Android. The Android version can be purchased anonymously via [ProxyStore](https://cryptomator.org/coop/proxystore).

Sommige cryptografische bibliotheken van Cryptomator zijn [geaudit](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) door Cure53. De reikwijdte van de gecontroleerde bibliotheken omvat: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) en [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). De controle strekte zich niet uit tot [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), een bibliotheek die door Cryptomator voor iOS wordt gebruikt.

Cryptomator's documentation details its intended [security target](https://docs.cryptomator.org/en/latest/security/security-target), [security architecture](https://docs.cryptomator.org/en/latest/security/architecture), and [best practices](https://docs.cryptomator.org/en/latest/security/best-practices) for use in further detail.

### Picocrypt (Bestand)

<small>Protects against the following threat(s):</small>

- [:material-target-account: Gerichte aanvallen](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![Picocrypt logo](assets/img/encryption-software/picocrypt.svg){ align=right }

**Picocrypt** is een klein en eenvoudig encryptieprogramma dat moderne encryptie biedt. Picocrypt gebruikt het veilige XChaCha20-cijfer en de Argon2id-sleutelafleidingsfunctie om een hoog niveau van veiligheid te bieden. Het gebruikt Go's standaard x/crypto modules voor zijn versleutelingsfuncties.

[:octicons-repo-16: Repository](https://github.com/Picocrypt/Picocrypt#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/Picocrypt/Picocrypt){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/picocrypt){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-apple: macOS](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-linux: Linux](https://github.com/Picocrypt/Picocrypt/releases)

</details>

</div>

Picocrypt has been [audited](https://github.com/Picocrypt/storage/blob/main/Picocrypt.Audit.Report.pdf) by Radically Open Security in August 2024, and [most](https://github.com/Picocrypt/Picocrypt/issues/32#issuecomment-2329722740) of the issues found in the audit were subsequently fixed.

### VeraCrypt (Schijf)

<small>Protects against the following threat(s):</small>

- [:material-target-account: Gerichte aanvallen](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![VeraCrypt-logo](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![VeraCrypt-logo](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt** is een met broncode beschikbaar freeware hulpprogramma dat wordt gebruikt voor on-the-fly encryptie. Het kan een virtuele versleutelde schijf binnen een bestand maken, een partitie versleutelen of het gehele opslagapparaat versleutelen met pre-boot verificatie.

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

VeraCrypt is een vork van het beëindigde TrueCrypt-project. Volgens de ontwikkelaars zijn er beveiligingsverbeteringen doorgevoerd en zijn de problemen die bij de eerste controle van de TrueCrypt-code aan het licht zijn gekomen, aangepakt.

Bij het versleutelen met VeraCrypt heb je de keuze uit verschillende [hashfuncties](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme). Wij raden je aan **alleen** [SHA-512](https://en.wikipedia.org/wiki/SHA-512) te selecteren en vast te houden aan het [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) blokcijfer.

TrueCrypt has been [audited a number of times](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits), and VeraCrypt has also been [audited separately](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit).

## Operating System Encryption

<small>Protects against the following threat(s):</small>

- [:material-target-account: Gerichte aanvallen](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Built-in OS encryption solutions generally leverage hardware security features such as a [secure cryptoprocessor](basics/hardware.md#tpmsecure-cryptoprocessor). Therefore, we recommend using the built-in encryption solutions for your operating system. For cross-platform encryption, we still recommend [cross-platform tools](#multi-platform) for additional flexibility and to avoid vendor lock-in.

### BitLocker

<div class="admonition recommendation" markdown>

![BitLocker logo](assets/img/encryption-software/bitlocker.png){ align=right }

**BitLocker** is the full volume encryption solution bundled with Microsoft Windows that uses the Trusted Platform Module ([TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm)) for hardware-based security.

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title="Documentation" }

</details>

</div>

BitLocker is [officially supported](https://support.microsoft.com/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838) on the Pro, Enterprise, and Education editions of Windows. It can be enabled on Home editions provided that they meet the following prerequisites.

<details class="example" markdown>
<summary>Enabling BitLocker on Windows Home</summary>

To enable BitLocker on "Home" editions of Windows, you must have partitions formatted with a [GUID Partition Table](https://en.wikipedia.org/wiki/GUID_Partition_Table) and have a dedicated TPM (v1.2, 2.0+) module. You may need to [disable the non-Bitlocker "Device encryption" functionality](https://discuss.privacyguides.net/t/enabling-bitlocker-on-the-windows-11-home-edition/13303/5) (which is inferior because it sends your recovery key to Microsoft's servers) if it is enabled on your device already before following this guide.

1. Open een opdrachtprompt en controleer de indeling van de partitietabel van jouw schijf met het volgende commando. Je zou "**GPT**" moeten zien staan onder "Partition Style":

    ```powershell
    powershell Get-Disk
    ```

2. Voer dit commando uit (in een admin commando prompt) om jouw TPM versie te controleren. Je zou `2.0` of `1.2` moeten zien staan naast `SpecVersion`:

    ```powershell
    powershell Get-WmiObject -Namespace "root/cimv2/security/microsofttpm" -Class WIN32_tpm
    ```

3. Access [Advanced Startup Options](https://support.microsoft.com/windows/advanced-startup-options-including-safe-mode-b90e7808-80b5-a291-d4b8-1a1af602b617). Je moet opnieuw opstarten terwijl je op de F8-toets drukt voordat Windows start en naar de *opdrachtprompt* gaat in **Problemen oplossen** → **Geavanceerde opties** → **Opdrachtprompt**.
4. Log in met jouw admin-account en typ dit in de opdrachtprompt om de versleuteling te starten:

    ```powershell
    manage-bde -on c: -used
    ```

5. Sluit de opdrachtprompt en en start verder op naar de gewone Windows installatie.
6. Open een admin commando prompt en voer de volgende commando's uit:

    ```powershell
    manage-bde c: -protectors -add -rp -tpm
    manage-bde -protectors -enable c:
    manage-bde -protectors -get c: > %UserProfile%\Desktop\BitLocker-Recovery-Key.txt
    ```

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

     Back-up de `BitLocker-Recovery-Key.txt` op uw bureaublad naar een apart opslagapparaat. Het verlies van deze herstelcode kan leiden tot verlies van gegevens.

</div>

</details>

### FileVault

<div class="admonition recommendation" markdown>

![FileVault-logo](assets/img/encryption-software/filevault.png){ align=right }

**FileVault** is de in macOS ingebouwde oplossing voor volumeversleuteling tijdens het filteren. FileVault takes advantage of the [hardware security capabilities](os/macos-overview.md#hardware-security) present on an Apple Silicon SoC or T2 Security Chip.

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title="Documentation" }

</details>

</div>

We advise against using your iCloud account for recovery; instead, you should securely store a local recovery key on a separate storage device.

### Linux Unified Key Setup

<div class="admonition recommendation" markdown>

![LUKS-logo](assets/img/encryption-software/luks.png){ align=right }

**LUKS** is de standaard FDE-methode voor Linux. Het kan worden gebruikt om volledige volumes of partities te versleutelen, of om versleutelde containers te maken.

[:octicons-repo-16: Repository](https://gitlab.com/cryptsetup/cryptsetup#what-the-){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup){ .card-link title="Source Code" }

</details>

</div>

<details class="example" markdown>
<summary>Creating and opening encrypted containers</summary>

```bash
dd if=/dev/urandom of=/path-to-file bs=1M count=1024 status=progress
sudo cryptsetup luksFormat /path-to-file
```

#### Opening encrypted containers

We recommend opening containers and volumes with `udisksctl` as this uses [Polkit](https://en.wikipedia.org/wiki/Polkit). De meeste bestandsbeheerders, zoals die van populaire desktopomgevingen, kunnen versleutelde bestanden ontgrendelen. Tools like [udiskie](https://github.com/coldfix/udiskie) can run in the system tray and provide a helpful user interface.

```bash
udisksctl loop-setup -f /path-to-file
udisksctl unlock -b /dev/loop0
```

</details>

<div class="admonition note" markdown>
<p class="admonition-title">Remember to back up volume headers</p>

Wij raden je aan altijd [een back-up te maken van uw LUKS-headers](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) in geval van een gedeeltelijke schijfstoring. This can be done with:

```bash
cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
```

</div>

## Command-line

<small>Protects against the following threat(s):</small>

- [:material-target-account: Gerichte aanvallen](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Tools met command-line interfaces zijn handig voor het integreren van [shell scripts](https://en.wikipedia.org/wiki/Shell_script).

### Kryptor

<div class="admonition recommendation" markdown>

![Kryptor logo](assets/img/encryption-software/kryptor.png){ align=right }

**Kryptor** is een gratis en open-source programma voor het versleutelen en ondertekenen van bestanden dat gebruik maakt van moderne en veilige cryptografische algoritmen. It aims to be a better version of [age](https://github.com/FiloSottile/age) and [Minisign](https://jedisct1.github.io/minisign) to provide a simple, easier alternative to GPG.

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

![Tomb logo](assets/img/encryption-software/tomb.png){ align=right }

**Tomb** is een is een command-line shell wrapper voor LUKS. It supports steganography via [third-party tools](https://dyne.org/software/tomb/#advanced-usage).

[:octicons-home-16: Homepage](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Source Code" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title="Contribute" }

</details>

</div>

## OpenPGP

<small>Protects against the following threat(s):</small>

- [:material-target-account: Gerichte aanvallen](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Passieve aanvallen](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Dienstverleners](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

OpenPGP is soms nodig voor specifieke taken zoals het digitaal ondertekenen en versleutelen van e-mail. PGP heeft veel mogelijkheden en is [complex](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html) omdat het al heel lang bestaat. Voor taken zoals het ondertekenen of versleutelen van bestanden, raden wij de bovenstaande opties aan.

Bij het versleutelen met PGP, heb je de optie om verschillende opties te configureren in het `gpg.conf` bestand. We recommend staying with the standard options specified in the [GnuPG user FAQ](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

<div class="admonition tip" markdown>
<p class="admonition-title">Use future defaults when generating a key</p>

When [generating keys](https://gnupg.org/gph/en/manual/c14.html) we suggest using the `future-default` command as this will instruct GnuPG use modern cryptography such as [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) and [Ed25519](https://ed25519.cr.yp.to):

```bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU Privacy Guard

<div class="admonition recommendation" markdown>

![GNU Privacy Guard logo](assets/img/encryption-software/gnupg.svg){ align=right }

**GnuPG** is een GPL-gelicenseerd alternatief voor de PGP-suite van cryptografische software. GnuPG is in overeenstemming met [RFC 4880](https://tools.ietf.org/html/rfc4880), de huidige IETF-specificatie van OpenPGP. The GnuPG project has been working on an [updated draft](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh) in an attempt to modernize OpenPGP. GnuPG is een onderdeel van het GNU-softwareproject van de Free Software Foundation en heeft van de Duitse regering het belangrijke [funding](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) ontvangen.

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

![GPG4win-logo](assets/img/encryption-software/gpg4win.svg){ align=right }

**GPG4win** is een pakket voor Windows van [Intevation en g10 Code](https://gpg4win.org/impressum.html). Het bevat [diverse hulpmiddelen](https://gpg4win.org/about.html) die je kunnen helpen bij het gebruik van GPG op Microsoft Windows. Het project is in 2005 opgezet en oorspronkelijk [gefinancierd door](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography) het Bundesamt für Informationssicherheit (BSI) van Duitsland.

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
<summary>Downloads</summary>

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
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

Cure53 completed a [security audit](https://openkeychain.org/openkeychain-3-6) of OpenKeychain 3.6 in October 2015. The published audit and OpenKeychain's solutions to the issues raised in the audit can be found [here](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

### Minimum kwalificaties

- Cross-platform encryption apps must be open source.
- Apps voor bestandsversleuteling moeten ontsleuteling ondersteunen op Linux, macOS en Windows.
- Apps voor externe schijfversleuteling moeten ontsleuteling ondersteunen op Linux, macOS en Windows.
- Interne (OS) schijfversleutelingsapps moeten platformonafhankelijk zijn of ingebouwd zijn in het besturingssysteem.

### Beste geval

Onze best-case criteria geven aan wat wij zouden willen zien van het perfecte project in deze categorie. Het is mogelijk dat onze aanbevelingen geen of niet alle functies bevatten, maar degene die dat wel doen kunnen hoger gerangschikt worden dan andere op deze pagina.

- Toepassingen voor versleuteling van het besturingssysteem (FDE) moeten gebruik maken van hardwarebeveiliging zoals een TPM of Secure Enclave.
- Bestandsversleutelingsapps moeten ondersteuning van eerste of derde partijen hebben voor mobiele platforms.
