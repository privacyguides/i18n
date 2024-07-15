---
meta_title: "Recommended Encryption Software: VeraCrypt, Cryptomator, PicoCrypt, and OpenPGP - Privacy Guides"
title: "Encryptie Software"
icon: material/file-lock
description: Encryptie van gegevens is de enige manier om te controleren wie er toegang toe heeft. These tools allow you to encrypt your emails and any other files.
cover: encryption.webp
---

Encryptie van gegevens is de enige manier om te controleren wie er toegang toe heeft. Als je momenteel geen encryptiesoftware gebruikt voor jouw harde schijf, e-mails of bestanden, moet je hier een optie kiezen.

## Multi-platform

De hier genoemde opties zijn multiplatform en zeer geschikt voor het maken van versleutelde back-ups van jouw gegevens.

### Cryptomator (Cloud)

<div class="admonition recommendation" markdown>

![Cryptomator logo](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** is een encryptie-oplossing die is ontworpen voor het privé opslaan van bestanden bij elke cloudprovider. Hiermee kunt u kluizen maken die worden opgeslagen op een virtuele schijf, waarvan de inhoud wordt gecodeerd en gesynchroniseerd met uw cloudopslagprovider.

[:octicons-home-16: Homepage](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.cryptomator.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/cryptomator){ .card-link title="Source Code" }
[:octicons-heart-16:](https://cryptomator.org/donate){ .card-link title=Contribute }

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

Sommige cryptografische bibliotheken van Cryptomator zijn [geaudit](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) door Cure53. De reikwijdte van de gecontroleerde bibliotheken omvat: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) en [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). De controle strekte zich niet uit tot [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), een bibliotheek die door Cryptomator voor iOS wordt gebruikt.

Cryptomator's documentation details its intended [security target](https://docs.cryptomator.org/en/latest/security/security-target), [security architecture](https://docs.cryptomator.org/en/latest/security/architecture), and [best practices](https://docs.cryptomator.org/en/latest/security/best-practices) for use in further detail.

### Picocrypt (Bestand)

<div class="admonition recommendation" markdown>

![Picocrypt logo](assets/img/encryption-software/picocrypt.svg){ align=right }

**Picocrypt** is een klein en eenvoudig encryptieprogramma dat moderne encryptie biedt. Picocrypt gebruikt het veilige XChaCha20-cijfer en de Argon2id-sleutelafleidingsfunctie om een hoog niveau van veiligheid te bieden. Het gebruikt Go's standaard x/crypto modules voor zijn versleutelingsfuncties.

[:octicons-repo-16: Repository](https://github.com/Picocrypt/Picocrypt){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/Picocrypt/Picocrypt){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/picocrypt){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-apple: macOS](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-linux: Linux](https://github.com/Picocrypt/Picocrypt/releases)

</details>

</div>

### VeraCrypt (Schijf)

<div class="admonition recommendation" markdown>

![VeraCrypt-logo](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![VeraCrypt-logo](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt** is een met broncode beschikbaar freeware hulpprogramma dat wordt gebruikt voor on-the-fly encryptie. Het kan een virtuele versleutelde schijf binnen een bestand maken, een partitie versleutelen of het gehele opslagapparaat versleutelen met pre-boot verificatie.

[:octicons-home-16: Homepage](https://veracrypt.fr){ .md-button .md-button--primary }
[:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title=Documentation}
[:octicons-code-16:](https://veracrypt.fr/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://veracrypt.fr/en/Downloads.html)
- [:simple-apple: macOS](https://veracrypt.fr/en/Downloads.html)
- [:simple-linux: Linux](https://veracrypt.fr/en/Downloads.html)

</details>

</div>

VeraCrypt is een vork van het beëindigde TrueCrypt-project. Volgens de ontwikkelaars zijn er beveiligingsverbeteringen doorgevoerd en zijn de problemen die bij de eerste controle van de TrueCrypt-code aan het licht zijn gekomen, aangepakt.

Bij het versleutelen met VeraCrypt heb je de keuze uit verschillende [hashfuncties](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme). Wij raden je aan **alleen** [SHA-512](https://en.wikipedia.org/wiki/SHA-512) te selecteren en vast te houden aan het [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) blokcijfer.

Truecrypt is [een aantal keer gecontroleerd](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits), en VeraCrypt is ook [apart gecontroleerd](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit).

## OS Volledige Schijfversleuteling

For encrypting the drive your operating system boots from, we generally recommend enabling the encryption software that comes with your operating system rather than using a third-party tool. This is because your operating system's native encryption tools often make use of OS and hardware-specific features like the [secure cryptoprocessor](https://en.wikipedia.org/wiki/Secure_cryptoprocessor) in your device to protect your computer against more advanced physical attacks. For secondary drives and external drives which you *don't* boot from, we still recommend using open-source tools like [VeraCrypt](#veracrypt-disk) over the tools below, because they offer additional flexibility and let you avoid vendor lock-in.

### BitLocker

<div class="admonition recommendation" markdown>

![BitLocker-logo](assets/img/encryption-software/bitlocker.png){ align=right }

**BitLocker** is de oplossing voor volledige volume-encryptie die met Microsoft Windows wordt meegeleverd. The main reason we recommend it for encrypting your boot drive is because of its [use of TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm). ElcomSoft, a forensics company, has written about this feature in [Understanding BitLocker TPM Protection](https://blog.elcomsoft.com/2021/01/understanding-BitLocker-tpm-protection).

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title=Documentation}

</details>

</div>

BitLocker is [only supported](https://support.microsoft.com/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838) on Pro, Enterprise and Education editions of Windows. Het kan worden ingeschakeld op Home-edities, mits deze aan de voorwaarden voldoen.

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

**FileVault** is de in macOS ingebouwde oplossing voor volumeversleuteling tijdens het filteren. FileVault wordt aanbevolen omdat het [leverages](https://support.apple.com/guide/security/volume-encryption-with-filevault-sec4c6dc1b6e/web) hardware beveiligingsmogelijkheden biedt die aanwezig zijn op een Apple silicium SoC of T2 Security Chip.

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title=Documentatie}

</details>

</div>

Wij raden je aan een lokale herstelsleutel op een veilige plaats op te slaan in plaats van uw iCloud-account te gebruiken voor herstel.

### Linux Unified Key Setup

<div class="admonition recommendation" markdown>

![LUKS-logo](assets/img/encryption-software/luks.png){ align=right }

**LUKS** is de standaard FDE-methode voor Linux. Het kan worden gebruikt om volledige volumes of partities te versleutelen, of om versleutelde containers te maken.

[:octicons-home-16: Homepage](https://gitlab.com/cryptsetup/cryptsetup/-/blob/main/README.md){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title=Documentation}
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

Tools met command-line interfaces zijn handig voor het integreren van [shell scripts](https://en.wikipedia.org/wiki/Shell_script).

### Kryptor

<div class="admonition recommendation" markdown>

![Kryptor logo](assets/img/encryption-software/kryptor.png){ align=right }

**Kryptor** is een gratis en open-source programma voor het versleutelen en ondertekenen van bestanden dat gebruik maakt van moderne en veilige cryptografische algoritmen. It aims to be a better version of [age](https://github.com/FiloSottile/age) and [Minisign](https://jedisct1.github.io/minisign) to provide a simple, easier alternative to GPG.

[:octicons-home-16: Homepage](https://kryptor.co.uk){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kryptor.co.uk/features#privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kryptor.co.uk/tutorial){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kryptor.co.uk/#donate){ .card-link title=Contribute }

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
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Source Code" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title=Contribute }

</details>

</div>

## OpenPGP

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
[:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title=Documentation}
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
[:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title=Documentation}
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="Source Code" }
[:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)

</details>

</div>

### GPG Suite

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

We suggest [Canary Mail](email-clients.md#canary-mail-ios) for using PGP with email on iOS devices.

</div>

<div class="admonition recommendation" markdown>

![GPG Suite logo](assets/img/encryption-software/gpgsuite.png){ align=right }

**GPG Suite** provides OpenPGP support for [Apple Mail](email-clients.md#apple-mail-macos) and macOS.

Wij raden aan een kijkje te nemen in hun [Eerste stappen pagina](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email) en [Kennisbank](https://gpgtools.tenderapp.com/kb) voor ondersteuning.

[:octicons-home-16: Homepage](https://gpgtools.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: macOS](https://gpgtools.org)

</details>

</div>

### OpenKeychain

<div class="admonition recommendation" markdown>

![OpenKeychain-logo](assets/img/encryption-software/openkeychain.svg){ align=right }

**OpenKeychain** is een Android implementatie van GnuPG. It's commonly required by mail clients such as [K-9 Mail](email-clients.md#k-9-mail-android) and [FairEmail](email-clients.md#fairemail-android) and other Android apps to provide encryption support. Cure53 completed a [security audit](https://openkeychain.org/openkeychain-3-6) of OpenKeychain 3.6 in October 2015. Technische details over de audit en OpenKeychain's oplossingen zijn te vinden op [here](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).

[:octicons-home-16: Homepage](https://openkeychain.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://openkeychain.org/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://openkeychain.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

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
