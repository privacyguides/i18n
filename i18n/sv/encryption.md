---
meta_title: "Recommended Encryption Software: VeraCrypt, Cryptomator, PicoCrypt, and OpenPGP - Privacy Guides"
title: "Programvara för kryptering"
icon: material/file-lock
description: Kryptering av data är det enda sättet att kontrollera vem som har tillgång till dem. These tools allow you to encrypt your emails and any other files.
cover: encryption.webp
---

**Encryption** is the only secure way to control who can access your data. If you are currently not using encryption software for your hard disk, emails, or files, you should pick an option here.

## Multiplattform

The options listed here are available on multiple platforms and great for creating encrypted backups of your data.

### Cryptomator (moln)

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Passiva attacker](basics/common-threats.md#security-and-privacy ""){.pg-orange}

<div class="admonition recommendation" markdown>

![Cryptomator logo](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** is an encryption solution designed for privately saving files to any cloud [:material-server-network: Service Provider](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }, eliminating the need to trust that they won't access your files. Det låter dig skapa valv som lagras på en virtuell enhet, vars innehåll krypteras och synkroniseras med din molnlagringsleverantör.

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

Cryptomator använder AES-256-kryptering för att kryptera både filer och filnamn. Cryptomator kan inte kryptera metadata som åtkomst, ändring och skapande tidsstämplar, eller antalet och storleken på filer och mappar.

Cryptomator is free to use on all desktop platforms, as well as on iOS in "read only" mode. Cryptomator offers [paid](https://cryptomator.org/pricing) apps with full functionality on iOS and Android. The Android version can be purchased anonymously via [ProxyStore](https://cryptomator.org/coop/proxystore).

Vissa kryptografiska bibliotek från Cryptomator har granskats [av Cure53](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44). De granskade biblioteken omfattar följande: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) och [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). Granskningen omfattade inte [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), som är ett bibliotek som används av Cryptomator för iOS.

Cryptomator's documentation details its intended [security target](https://docs.cryptomator.org/en/latest/security/security-target), [security architecture](https://docs.cryptomator.org/en/latest/security/architecture), and [best practices](https://docs.cryptomator.org/en/latest/security/best-practices) for use in further detail.

### Picocrypt (Fil)

<small>Protects against the following threat(s):</small>

- [:material-target-account: Riktade attacker](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![Picocrypt-logotyp](assets/img/encryption-software/picocrypt.svg){ align=right }

**Picocrypt** är ett litet och enkelt krypteringsverktyg som tillhandahåller modern kryptering. Picocrypt använder den säkra XChaCha20-chiffern och Argon2id-nyckelderivatfunktionen för att ge en hög säkerhetsnivå. Det använder Go standard x/crypto moduler för sina krypteringsfunktioner.

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

### VeraCrypt (disk)

<small>Protects against the following threat(s):</small>

- [:material-target-account: Riktade attacker](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![VeraCrypt logo](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![VeraCrypt logo](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt** är ett källkod-tillgängligt freeware-verktyg som används för on-the-fly kryptering. Det kan skapa en virtuell krypterad disk i en fil, kryptera en partition eller kryptera hela lagringsenheten med autentisering före start.

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

VeraCrypt är en gaffel i det nedlagda TrueCrypt-projektet. Enligt utvecklarna har säkerhetsförbättringar genomförts och problem som togs upp vid den första TrueCrypt-kodgranskningen har åtgärdats.

När du krypterar med VeraCrypt kan du välja mellan olika hashfunktioner [](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme). Vi föreslår att du **endast** väljer [SHA-512](https://en.wikipedia.org/wiki/SHA-512) och håller dig till [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) blockchiffer.

TrueCrypt has been [audited a number of times](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits), and VeraCrypt has also been [audited separately](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit).

## Operating System Encryption

<small>Protects against the following threat(s):</small>

- [:material-target-account: Riktade attacker](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

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

1. Öppna en kommandotolk och kontrollera enhetens partitionstabellformat med följande kommando. Du bör se "**GPT**" listad under "Partition Style":

    ```powershell
    powershell Get-Disk
    ```

2. Kör det här kommandot (i en administratörskommandotolk) för att kontrollera din TPM-version. Du bör se `2.0` eller `1.2` bredvid `SpecVersion`:

    ```powershell
    powershell Get-WmiObject -Namespace "root/cimv2/security/microsofttpm" -Class WIN32_tpm
    ```

3. Access [Advanced Startup Options](https://support.microsoft.com/windows/advanced-startup-options-including-safe-mode-b90e7808-80b5-a291-d4b8-1a1af602b617). Du måste starta om och samtidigt trycka på F8-tangenten innan Windows startar och gå in i kommandotolken ** i **Felsökning** → **Avancerade alternativ** → **Kommandotolk**.
4. Logga in med ditt administratörskonto och skriv detta i kommandotolken för att starta kryptering:

    ```powershell
    manage-bde -on c: -used
    ```

5. Stäng kommandotolken och fortsätt att starta upp till vanligt Windows.
6. Öppna en administratörskommandotolk och kör följande kommandon:

    ```powershell
    manage-bde c: -protectors -add -rp -tpm
    manage-bde -protectors -enable c:
    manage-bde -protectors -get c: > %UserProfile%\Desktop\BitLocker-Recovery-Key.txt
    ```

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Säkerhetskopiera `BitLocker-Recovery-Key.txt` på skrivbordet till en separat lagringsenhet. Förlust av denna återställningskod kan leda till förlust av data.

</div>

</details>

### FileVault

<div class="admonition recommendation" markdown>

![FileVaults logotyp](assets/img/encryption-software/filevault.png){ align=right }

**FileVault** är en lösning för volymkryptering i farten som är inbyggd i macOS. FileVault takes advantage of the [hardware security capabilities](os/macos-overview.md#hardware-security) present on an Apple Silicon SoC or T2 Security Chip.

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title="Documentation" }

</details>

</div>

We advise against using your iCloud account for recovery; instead, you should securely store a local recovery key on a separate storage device.

### Linux Unified Key Setup

<div class="admonition recommendation" markdown>

![LUKS-logotyp](assets/img/encryption-software/luks.png){ align=right }

**LUKS** är standardmetoden för FDE för Linux. Den kan användas för att kryptera hela volymer, partitioner eller skapa krypterade behållare.

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

We recommend opening containers and volumes with `udisksctl` as this uses [Polkit](https://en.wikipedia.org/wiki/Polkit). De flesta filhanterare, t. ex. de som ingår i populära skrivbordsmiljöer, kan låsa upp krypterade filer. Tools like [udiskie](https://github.com/coldfix/udiskie) can run in the system tray and provide a helpful user interface.

```bash
udisksctl loop-setup -f /path-to-file
udisksctl unlock -b /dev/loop0
```

</details>

<div class="admonition note" markdown>
<p class="admonition-title">Remember to back up volume headers</p>

Vi rekommenderar att du alltid [säkerhetskopierar dina LUKS-rubriker] (https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) om en del av enheten skulle gå sönder. This can be done with:

```bash
cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
```

</div>

## Kommandorad

<small>Protects against the following threat(s):</small>

- [:material-target-account: Riktade attacker](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Verktyg med kommandoradsgränssnitt är användbara för att integrera [skalskript](https://en.wikipedia.org/wiki/Shell_script).

### Kryptor

<div class="admonition recommendation" markdown>

![Kryptor-logotyp](assets/img/encryption-software/kryptor.png){ align=right }

** Kryptor** är ett gratis och öppet källkodsverktyg för filkryptering och signering som använder moderna och säkra kryptografiska algoritmer. It aims to be a better version of [age](https://github.com/FiloSottile/age) and [Minisign](https://jedisct1.github.io/minisign) to provide a simple, easier alternative to GPG.

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

![Tomb-logotyp](assets/img/encryption-software/tomb.png){ align=right }

* * Tomb * * är ett kommandoradsskal för LUKS. It supports steganography via [third-party tools](https://dyne.org/software/tomb/#advanced-usage).

[:octicons-home-16: Homepage](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Source Code" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title="Contribute" }

</details>

</div>

## OpenPGP

<small>Protects against the following threat(s):</small>

- [:material-target-account: Riktade attacker](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Passiva attacker](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Tjänsteleverantörer](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

OpenPGP behövs ibland för specifika uppgifter som digital signering och kryptering av e-post. PGP har många funktioner och är [komplext](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html) eftersom det har funnits länge. För uppgifter som signering eller kryptering av filer föreslår vi ovanstående alternativ.

Vid kryptering med PGP har du möjlighet att konfigurera olika alternativ i din `gpg.conf` -fil. We recommend staying with the standard options specified in the [GnuPG user FAQ](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

<div class="admonition tip" markdown>
<p class="admonition-title">Use future defaults when generating a key</p>

When [generating keys](https://gnupg.org/gph/en/manual/c14.html) we suggest using the `future-default` command as this will instruct GnuPG use modern cryptography such as [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) and [Ed25519](https://ed25519.cr.yp.to):

```bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU Privacy Guard

<div class="admonition recommendation" markdown>

![GNU Privacy Guard-logotypen](assets/img/encryption-software/gnupg.svg){ align=right }

**GnuPG * * är ett GPL-licensierat alternativ till PGP-paketet med kryptografisk programvara. GnuPG är kompatibel med [RFC 4880](https://tools.ietf.org/html/rfc4880), som är den aktuella IETF-specifikationen för OpenPGP. The GnuPG project has been working on an [updated draft](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh) in an attempt to modernize OpenPGP. GnuPG är en del av Free Software Foundations GNU-programvaruprojekt och har fått stora [funding](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) från den tyska regeringen.

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

![GPG4win-logotyp](assets/img/enkrypteringsprogram/gpg4win.svg){ align=right }

**GPG4win** är ett paket för Windows från [Intevation and g10 Code] (https://gpg4win.org/impressum.html). Den innehåller [olika verktyg] (https://gpg4win.org/about.html) som kan hjälpa dig att använda GPG i Microsoft Windows. Projektet initierades och finansierades ursprungligen [av](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography) Tysklands federala kontor för informationssäkerhet (BSI) 2005.

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

## Kriterier

**Observera att vi inte är knutna till något av de projekt som vi rekommenderar.** Förutom [våra standardkriterier](about/criteria.md)har vi utvecklat en tydlig uppsättning krav som gör det möjligt för oss att ge objektiva rekommendationer. Vi föreslår att du bekantar dig med den här listan innan du väljer att använda ett projekt, och att du gör din egen forskning för att se till att det är rätt val för dig.

### Minimikrav

- Cross-platform encryption apps must be open source.
- File encryption apps must support decryption on Linux, macOS, and Windows.
- External disk encryption apps must support decryption on Linux, macOS, and Windows.
- Internal (OS) disk encryption apps must be cross-platform or built in to the operating system natively.

### Bästa fall

Våra kriterier för bästa fall representerar vad vi skulle vilja se av det perfekta projektet i denna kategori. Våra rekommendationer kanske inte innehåller alla eller några av dessa funktioner, men de som gör det kan vara högre rankade än andra på den här sidan.

- Operating System (FDE) encryption apps should utilize hardware security such as a TPM or Secure Enclave.
- File encryption apps should have first- or third-party support for mobile platforms.
