---
meta_title: "Empfohlene Verschlüsselungssoftware: VeraCrypt, Cryptomator, PicoCrypt und OpenPGP - Privacy Guides"
title: "Verschlüsselungssoftware"
icon: material/file-lock
description: Die Verschlüsselung von Daten ist die einzige Möglichkeit zu kontrollieren, wer darauf zugreifen kann. Mit diesen Tools kannst du deine E-Mails und alle anderen Dateien verschlüsseln.
cover: encryption.webp
---

**Verschlüsselung** ist der einzige sichere Weg, um zu kontrollieren, wer auf deine Daten zugreifen kann. Wenn du derzeit keine Verschlüsselungssoftware für deine Festplatte, E-Mails oder Dateien verwendest, solltest du hier eine Option auswählen.

## Multi-Plattform

Die hier aufgeführten Optionen sind plattformübergreifend und eignen sich hervorragend für die Erstellung verschlüsselter Backups deiner Daten.

### Cryptomator (Cloud)

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-bug-outline: Passive Angriffe](basics/common-threats.md#security-and-privacy ""){.pg-orange}

<div class="admonition recommendation" markdown>

![Cryptomator Logo](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** ist eine Verschlüsselungslösung, die für private Speicherung von Dateien bei einem beliebigen [:material-server-network: Dienstanbieter](basics/common-threats.md#privacy-from-service-providers){ .pg-teal } entwickelt wurde. So musst du nicht mehr darauf vertrauen, dass dieser nicht auf deine Dateien zugreift. Es erlaubt dir Tresore zu erstellen, die auf einem virtuellen Laufwerk gespeichert sind, deren Inhalt verschlüsselt und mit deinem Cloud-Anbieter synchronisiert wird.

[:octicons-home-16: Homepage](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://docs.cryptomator.org){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/cryptomator){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://cryptomator.org/donate){ .card-link title="Spenden" }

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

Cryptomator verwendet AES-256-Verschlüsselung, um sowohl Dateien als auch Dateinamen zu verschlüsseln. Cryptomator kann weder Metadaten wie Zugriffs-, Änderungs- und Erstellungszeitstempel, noch die Anzahl und Größe von Dateien und Ordnern verschlüsseln.

Cryptomator is free to use on all desktop platforms, as well as on iOS in "read only" mode. Cryptomator offers [paid](https://cryptomator.org/pricing) apps with full functionality on iOS and Android. The Android version can be purchased anonymously via [ProxyStore](https://cryptomator.org/coop/proxystore).

Einige kryptografische Bibliotheken von Cryptomator sind von Cure53 [geprüft](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) worden. Die geprüften Bibliotheken umfasst: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) und [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). Das Audit wurde erstreckte sich nicht auf [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), eine Bibliothek, die von Cryptomator für iOS verwendet wird.

In der Dokumentation von Cryptomator werden die angestrebten [Sicherheitsziele](https://docs.cryptomator.org/en/latest/security/security-target), die [Sicherheitsarchitektur](https://docs.cryptomator.org/en/latest/security/architecture) und die [Best Practices](https://docs.cryptomator.org/en/latest/security/best-practices) für den Einsatz im Detail beschrieben.

### Picocrypt (Dateien)

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![Picocrypt-Logo](assets/img/verschluesselungs-software/picocrypt.svg){ align=right }

**Picocrypt** ist ein kleines und simples Verschlüsselungstool, das moderne Verschlüsselung bietet. Picocrypt verwendet die sichere XChaCha20-Chiffre und die Argon2id-Schlüsselableitungsfunktion, um ein hohes Maß an Sicherheit zu gewährleisten. Es verwendet Go's Standard x/crypto Module für seine Verschlüsselungsfunktionen.

[:octicons-repo-16: Repository](https://github.com/Picocrypt/Picocrypt){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/Picocrypt/Picocrypt){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://opencollective.com/picocrypt){ .card-link title="Spenden" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-apple: macOS](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-linux: Linux](https://github.com/Picocrypt/Picocrypt/releases)

</details>

</div>

Picocrypt wurde im August 2024 von Radically Open Security [geprüft](https://github.com/Picocrypt/storage/blob/main/Picocrypt.Audit.Report.pdf), und [die meisten](https://github.com/Picocrypt/Picocrypt/issues/32#issuecomment-2329722740) der bei der Prüfung festgestellten Probleme wurden anschließend behoben.

### VeraCrypt (Festplatte)

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![VeraCrypt Logo](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![VeraCrypt Logo](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt** ist ein quelloffenes, Freeware-Programm, das zur On-The-Fly Verschlüsselung verwendet wird. Es kann eine virtuelle verschlüsselte Festplatte innerhalb einer Datei erstellen, eine Partition verschlüsseln oder das gesamte Laufwerk mit einer Pre-Boot Authentifizierung verschlüsseln.

[:octicons-home-16: Homepage](https://veracrypt.fr){ .md-button .md-button--primary }
[:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://veracrypt.fr/code){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title="Spenden" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://veracrypt.fr/en/Downloads.html)
- [:simple-apple: macOS](https://veracrypt.fr/en/Downloads.html)
- [:simple-linux: Linux](https://veracrypt.fr/en/Downloads.html)

</details>

</div>

VeraCrypt ist eine Fork des eingestellten TrueCrypt-Projekts. Nach Angaben der Entwickler wurden Sicherheitsverbesserungen vorgenommen und Probleme, die bei der ersten Überprüfung des TrueCrypt-Codes aufgetreten waren, behoben.

Beim Verschlüsseln mit VeraCrypt hast du die Möglichkeit, zwischen verschiedenen [Hash-Funktionen](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme) zu wählen. Wir empfehlen dir **nur** [SHA-512](https://en.wikipedia.org/wiki/SHA-512) auszuwählen und beim [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard)-Blockchiffre zu bleiben.

TrueCrypt wurde bereits [mehrfach geprüft](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits), und auch VeraCrypt wurde einem [separaten Audit](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit) unterzogen.

## Operating System Encryption

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Built-in OS encryption solutions generally leverage hardware security features such as a [secure cryptoprocessor](basics/hardware.md#tpmsecure-cryptoprocessor). Therefore, we recommend using the built-in encryption solutions for your operating system. For cross-platform encryption, we still recommend [cross-platform tools](#multi-platform) for additional flexibility and to avoid vendor lock-in.

### BitLocker

<div class="admonition recommendation" markdown>

![BitLocker logo](assets/img/encryption-software/bitlocker.png){ align=right }

**BitLocker** is the full volume encryption solution bundled with Microsoft Windows that uses the Trusted Platform Module ([TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm)) for hardware-based security.

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title="Dokumentation" }

</details>

</div>

BitLocker is [officially supported](https://support.microsoft.com/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838) on the Pro, Enterprise, and Education editions of Windows. It can be enabled on Home editions provided that they meet the following prerequisites.

<details class="example" markdown>
<summary>Aktivieren von BitLocker unter Windows Home</summary>

To enable BitLocker on "Home" editions of Windows, you must have partitions formatted with a [GUID Partition Table](https://en.wikipedia.org/wiki/GUID_Partition_Table) and have a dedicated TPM (v1.2, 2.0+) module. You may need to [disable the non-Bitlocker "Device encryption" functionality](https://discuss.privacyguides.net/t/enabling-bitlocker-on-the-windows-11-home-edition/13303/5) (which is inferior because it sends your recovery key to Microsoft's servers) if it is enabled on your device already before following this guide.

1. Open a command prompt and check your drive's partition table format with the following command. You should see "**GPT**" listed under "Partition Style":

    ```powershell
    powershell Get-Disk
    ```

2. Run this command (in an admin command prompt) to check your TPM version. You should see `2.0` or `1.2` listed next to `SpecVersion`:

    ```powershell
    powershell Get-WmiObject -Namespace "root/cimv2/security/microsofttpm" -Class WIN32_tpm
    ```

3. Access [Advanced Startup Options](https://support.microsoft.com/windows/advanced-startup-options-including-safe-mode-b90e7808-80b5-a291-d4b8-1a1af602b617). You need to reboot while pressing the F8 key before Windows starts and go into the *command prompt* in **Troubleshoot** → **Advanced Options** → **Command Prompt**.
4. Login with your admin account and type this in the command prompt to start encryption:

    ```powershell
    manage-bde -on c: -used
    ```

5. Close the command prompt and continue booting to regular Windows.
6. Open an admin command prompt and run the following commands:

    ```powershell
    manage-bde c: -protectors -add -rp -tpm
    manage-bde -protectors -enable c:
    manage-bde -protectors -get c: > %UserProfile%\Desktop\BitLocker-Recovery-Key.txt
    ```

<div class="admonition tip" markdown>
<p class="admonition-title">Tipp</p>

Sichere die Datei `BitLocker-Recovery-Key.txt` auf deinem Desktop auf einem separaten Speichergerät. Der Verlust dieses Wiederherstellungscodes kann zu Datenverlust führen.

</div>

</details>

### FileVault

<div class="admonition recommendation" markdown>

![FileVault Logo](assets/img/encryption-software/filevault.png){ align=right }

**FileVault** ist die in macOS eingebaute "on-the-fly"-Verschlüsselungslösung. FileVault takes advantage of the [hardware security capabilities](os/macos-overview.md#hardware-security) present on an Apple Silicon SoC or T2 Security Chip.

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title="Dokumentation" }

</details>

</div>

We advise against using your iCloud account for recovery; instead, you should securely store a local recovery key on a separate storage device.

### Linux Unified Key Setup

<div class="admonition recommendation" markdown>

![LUKS-Logo](assets/img/encryption-software/luks.png){ align=right }

**LUKS** ist die Standard-FDE-Methode für Linux. Es kann zur Verschlüsselung ganzer Volumes, Partitionen oder zur Erstellung verschlüsselter Container verwendet werden.

[:octicons-home-16: Homepage](https://gitlab.com/cryptsetup/cryptsetup/-/blob/main/README.md){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup){ .card-link title="Quellcode" }

</details>

</div>

<details class="example" markdown>
<summary>Verschlüsselte Container erstellen und öffnen</summary>

```bash
dd if=/dev/urandom of=/path-to-file bs=1M count=1024 status=progress
sudo cryptsetup luksFormat /path-to-file
```

#### Verschlüsselte Container öffnen

We recommend opening containers and volumes with `udisksctl` as this uses [Polkit](https://en.wikipedia.org/wiki/Polkit). Most file managers, such as those included with popular desktop environments, can unlock encrypted files. Tools like [udiskie](https://github.com/coldfix/udiskie) can run in the system tray and provide a helpful user interface.

```bash
udisksctl loop-setup -f /path-to-file
udisksctl unlock -b /dev/loop0
```

</details>

<div class="admonition note" markdown>
<p class="admonition-title">Denke daran, den Volume-Header zu sichern</p>

Wir empfehlen dir, im Falle eines teilweisen Laufwerksausfalls immer [eine Sicherungskopie deines LUKS-Header](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) zu erstellen. Dies kann wie folgt durchgeführt werden:

```bash
cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
```

</div>

## Kommandozeile

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Werkzeuge mit Befehlszeilenschnittstellen sind nützlich für die Integration von [Shell-Skripten](https://de.wikipedia.org/wiki/Shellskript).

### Kryptor

<div class="admonition recommendation" markdown>

![Kryptor Logo](assets/img/encryption-software/kryptor.png){ align=right }

**Kryptor** ist ein kostenloses und quelloffenes Tool zur Dateiverschlüsselung und -signierung, das moderne und sichere kryptografische Algorithmen verwendet. Es soll eine bessere Version von [age](https://github.com/FiloSottile/age) und [Minisign](https://jedisct1.github.io/minisign) sein und eine einfache, leichtere Alternative zu GPG darstellen.

[:octicons-home-16: Homepage](https://kryptor.co.uk){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kryptor.co.uk/features#privacy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://kryptor.co.uk/tutorial){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://kryptor.co.uk/#donate){ .card-link title="Unterstützen" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://kryptor.co.uk)
- [:simple-apple: macOS](https://kryptor.co.uk)
- [:simple-linux: Linux](https://kryptor.co.uk)

</details>

</div>

### Tomb

<div class="admonition recommendation" markdown>

![Tomb-Logo](assets/img/verschlüsselungssoftware/tomb.png){ align=right }

**Tomb** ist ein Kommandozeilen-Shell-Wrapper für LUKS. Es unterstützt Steganografie über [Drittanbieter-Tools] (https://dyne.org/software/tomb/#advanced-usage).

[:octicons-home-16: Homepage](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title="Spenden" }

</details>

</div>

## OpenPGP

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Passive Angriffe](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Diensteanbieter](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

OpenPGP wird manchmal für spezielle Aufgaben benötigt, z. B. zum digitalen Signieren und Verschlüsseln von E-Mails. PGP hat viele Funktionen und ist [komplex](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html), da es schon lange existiert. Wenn du Dateien signieren oder verschlüsseln willst, empfehlen wir die oben genannten Optionen.

Beim Verschlüsseln mit PGP hast du die Möglichkeit, verschiedene Optionen in deiner `gpg.conf`-Datei zu konfigurieren. Wir empfehlen, die in der [GnuPG-Benutzer-FAQ](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf) angegebenen Standardoptionen beizubehalten.

<div class="admonition tip" markdown>
<p class="admonition-title">Verwende Future-Defaults, wenn du Schlüssel generierst</p>

Bei der [Schlüsselgenerierung](https://gnupg.org/gph/en/manual/c14.html) empfehlen wir die Verwendung des Befehls `future-default`, da dies GnuPG anweist, moderne Kryptographie wie [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) und [Ed25519](https://ed25519.cr.yp.to) zu verwenden:

```bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU Privacy Guard

<div class="admonition recommendation" markdown>

![GNU Privacy Guard logo](assets/img/encryption-software/gnupg.svg){ align=right }

**GnuPG** ist eine GPL-lizensierte Alternative zur PGP-Suite von Verschlüsselungssoftware. GnuPG ist [RFC 4880](https://tools.ietf.org/html/rfc4880) komfort, was die aktuelle IETF Spezifikation von OpenPGP ist. Das GnuPG-Projekt hat an einem [aktualisierten Entwurf](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh) gearbeitet, um OpenPGP zu modernisieren. GnuPG ist Teil des GNU-Softwareprojekts der Free Software Foundation und wurde von der deutschen Regierung maßgeblich [gefördert](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html).

[:octicons-home-16: Homepage](https://gnupg.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="Quellcode" }

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

![GPG4win Logo](assets/img/encryption-software/gpg4win.svg){ align=right }

**GPG4win** ist ein Paket für Windows von [Intevation und g10 Code](https://gpg4win.org/impressum-de.html). Es beinhaltet [verschiedene Tools](https://gpg4win.org/about-de.html), die dir bei der Verwendung von GPG unter Microsoft Windows helfen können. Das Projekt wurde 2005 [initiiert und ursprünglich finanziert](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography) vom deutschen Bundesamt für Sicherheit in der Informationstechnik (BSI).

[:octicons-home-16: Homepage](https://gpg4win.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title="Unterstützen" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download-de.html)

</details>

</div>

### GPG Suite

<div class="admonition recommendation" markdown>

![GPG Suite logo](assets/img/encryption-software/gpgsuite.png){ align=right }

**GPG Suite** provides OpenPGP support for [Apple Mail](email-clients.md#apple-mail-macos) and other email clients on macOS.

Wir empfehlen, einen Blick auf die [Ersten Schritte](https://gpgtools.tenderapp.com/kb/how-to/erste-schritte-gpgtools-einrichten-einen-schlssel-erstellen-deine-erste-verschlsselte-mail) und die [Wissensdatenbank](https://gpgtools.tenderapp.com/kb) zu werfen, um Unterstützung zu erhalten.

[:octicons-home-16: Homepage](https://gpgtools.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Quellcode" }

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
[:octicons-eye-16:](https://openkeychain.org/help/privacy-policy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://openkeychain.org/faq){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

Cure53 completed a [security audit](https://openkeychain.org/openkeychain-3-6) of OpenKeychain 3.6 in October 2015. The published audit and OpenKeychain's solutions to the issues raised in the audit can be found [here](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

### Mindestanforderungen

- Plattformübergreifende Verschlüsselungsanwendungen müssen quelloffen sein.
- Anwendungen zur Dateiverschlüsselung müssen die Entschlüsselung unter Linux, macOS und Windows unterstützen.
- Anwendungen zur Verschlüsselung externer Festplatten müssen die Entschlüsselung unter Linux, macOS und Windows unterstützen.
- Internal (OS) disk encryption apps must be cross-platform or built in to the operating system natively.

### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Merkmale, aber diejenigen, die sie enthalten, werden möglicherweise höher eingestuft als andere auf dieser Seite.

- Operating System (FDE) encryption apps should utilize hardware security such as a TPM or Secure Enclave.
- File encryption apps should have first- or third-party support for mobile platforms.
