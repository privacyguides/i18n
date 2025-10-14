---
meta_title: "Logiciels de chiffrement recommandés : VeraCrypt, Cryptomator, and OpenPGP - Privacy Guides"
title: "Logiciels de chiffrement"
icon: material/file-lock
description: Le chiffrement des données est le seul moyen de contrôler qui peut y accéder. Ces outils vous permettent de chiffrer vos emails et tout autre de fichier.
cover: encryption.webp
---

Le **chiffrement** est le seul moyen fiable de contrôler qui peu accéder à vos données. Voici nos recommandations de logiciel de chiffrement pour les personnes souhaitant chiffrer leur disque dur, mail ou fichiers.

## Multi-plateforme

Nos recommandations sont disponibles sur plusieurs plateformes et permettent de créer des sauvegardes chiffrées de toutes vos données.

### Cryptomator (Cloud)

<small>Protège contre les menaces suivantes :</small>

- [:material-bug-outline: Attaques passives](basics/common-threats.md#security-and-privacy ""){.pg-orange}

<div class="admonition recommendation" markdown>

![Logo de Cryptomator](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** est une solution de chiffrement pensée pour chiffrer vos fichiers sauvegardés dans n'importe quel [:material-server-network: Fournisseur de Service](basics/common-threats.md#privacy-from-service-providers){ .pg-teal } cloud, éliminant ainsi le besoin de s'assurer qu'il n'accède pas à vos fichiers. Il vous permet de créer des coffres-forts qui sont stockés sur un disque virtuel, dont le contenu est chiffré et synchronisé avec votre fournisseur de stockage cloud.

[:octicons-home-16: Page d'Accueil](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://docs.cryptomator.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/cryptomator){ .card-link title="Code Source" }
[:octicons-heart-16:](https://cryptomator.org/donate){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.cryptomator)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1560822163)
- [:simple-android: Android](https://cryptomator.org/android)
- [:fontawesome-brands-windows: Windows](https://cryptomator.org/downloads)
- [:simple-apple: macOS](https://cryptomator.org/downloads)
- [:simple-linux: Linux](https://cryptomator.org/downloads)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.cryptomator.Cryptomator)

</details>

</div>

Cryptomator utilise le chiffrement AES-256 pour chiffrer les fichiers et les noms de fichiers. Cryptomator ne peut pas chiffrer certaines métadonnées telles que les dates et heures d'accès, de modification et de création, ni le nombre et la taille des fichiers et des dossiers.

Cryptomator est gratuit sur toutes les plateformes de bureau, ainsi que sur iOS en mode "lecture seule". Les autres fonctionnalités de l'application sur iOS ainsi que l'application Android sont [payantes](https://cryptomator.org/pricing). La version Android peut être achetée anonymement avec [ProxyStore](https://cryptomator.org/coop/proxystore).

Certaines bibliothèques cryptographiques de Cryptomator ont été [auditées](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) par Cure53. La portée des bibliothèques auditées comprend: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) et [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). L'audit ne s'est pas étendu à [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), qui est une bibliothèque utilisée par Cryptomator pour iOS.

La documentation de Cryptomator décris en détails [ses objectifs de sécurité](https://docs.cryptomator.org/en/latest/security/security-target),[son architecture](https://docs.cryptomator.org/en/latest/security/architecture), et [les bonnes pratiques](https://docs.cryptomator.org/en/latest/security/best-practices) à adopter pour une utilisation optimale.

### VeraCrypt (Disque)

<small>Protège contre les menaces suivantes :</small>

- [:material-target-account: Attaques ciblées](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![logo VeraCrypt](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![logo VeraCrypt](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt** est un utilitaire gratuit et open source pour le chiffrement de fichiers/dossiers à la volée. Il peut créer un disque virtuel chiffré dans un fichier, chiffrer une partition ou l'ensemble du périphérique de stockage avec une authentification avant le démarrage.

[:octicons-home-16: Page d'Accueil](https://veracrypt.fr){ .md-button .md-button--primary }
[:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://veracrypt.fr/code){ .card-link title="Code Source" }
[:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:fontawesome-brands-windows: Windows](https://veracrypt.fr/en/Downloads.html)
- [:simple-apple: macOS](https://veracrypt.fr/en/Downloads.html)
- [:simple-linux: Linux](https://veracrypt.fr/en/Downloads.html)

</details>

</div>

VeraCrypt est un dérivé du projet TrueCrypt, qui a été abandonné. Selon ses développeurs, des améliorations de la sécurité ont été apportées et les problèmes soulevés par l'audit initial du code de TrueCrypt ont été résolus.

Lors du chiffrement avec VeraCrypt, vous avez la possibilité de choisir parmi différentes [fonctions de hachage](https://fr.wikipedia.org/wiki/VeraCrypt#Syst%C3%A8me_de_chiffrement). Nous vous suggérons de **seulement** sélectionner [SHA-512](https://fr.wikipedia.org/wiki/SHA-2) et de vous en tenir au [chiffrement par blocs AES](https://fr.wikipedia.org/wiki/Advanced_Encryption_Standard).

TrueCrypt a été [audité plusieurs fois](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits), et VeraCrypt a également été [audité séparément](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit).

## Chiffrement du système d'exploitation

<small>Protège contre les menaces suivantes :</small>

- [:material-target-account: Attaques ciblées](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Les solutions de chiffrement intégrées au système d'exploitation s'appuient généralement sur les fonctionnalités de sécurité du hardware, comme un [cryptoprocesseur sécurisé](basics/hardware.md#tpmsecure-cryptoprocessor). C'est pourquoi nous vous recommandons d'utiliser les solutions de chiffrement intégrées à votre système d'exploitation. Pour un chiffrement multiplateforme, nous recommandons toujours [des outils multiplateformes](#multi-platform) pour plus de flexibilité, et éviter le verrouillage des fournisseurs.

### BitLocker

<div class="admonition recommendation" markdown>

![Logo de BitLocker](assets/img/encryption-software/bitlocker.png){ align=right }

**BitLocker** est l'outil de chiffrement fourni avec Microsoft Windows, il utilise le module de plateforme sécurisée ([TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm)) pour la sécurité hardware.

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title="Documentation" }

</details>

</div>

BitLocker est [officiellement disponible](https://support.microsoft.com/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838) sur les éditions Pro, Entreprise et Education de Windows. Il est possible de l'activer sur les éditions Home qui répondent aux critères suivants.

<details class="example" markdown>
<summary>Activer BitLocker dans Windows Famille</summary>

Pour activer BitLocker sur les éditions "Famille" de Windows, vous devez formater vos partitions avec une [Table de Partitionnement GUID](https://en.wikipedia.org/wiki/GUID_Partition_Table) et disposer d'un module TPM dédié (v1.2, 2.0+). Il se peut que vous deviez [désactiver la fonctionnalité "Chiffrement de l'appareil" non-Bitlocker](https://discuss.privacyguides.net/t/enabling-bitlocker-on-the-windows-11-home-edition/13303/5) (qui est inférieure car elle envoie votre clé de récupération aux serveurs de Microsoft) si elle est déjà activée sur votre appareil avant de suivre ce guide.

1. Ouvrez une invite de commande et vérifiez le format de la table de partition de votre disque à l'aide de la commande suivante. Vous devriez voir "**GPT**" listé sous "Style de partition" :

    ```powershell
    powershell Get-Disk
    ```

2. Exécutez cette commande (dans une invite de commande administrateur) pour vérifier la version de votre TPM. Vous devriez voir `2.0` ou `1.2` listé à côté de `SpecVersion`:

    ```powershell
    powershell Get-WmiObject -Namespace "root/cimv2/security/microsofttpm" -Class WIN32_tpm
    ```

3. Accèdez aux [Options de démarrage avancées](https://support.microsoft.com/windows/advanced-startup-options-including-safe-mode-b90e7808-80b5-a291-d4b8-1a1af602b617). Vous devez redémarrer en appuyant sur la touche F8 avant que Windows ne démarre et aller dans l'*invite de commande* dans **Dépannage** → **Options avancées** → **Invite de commande**.
4. Connectez-vous avec votre compte administrateur et tapez ceci dans l'invite de commande pour lancer le chiffrement:

    ```powershell
    manage-bde -on c: -used
    ```

5. Fermez l'invite de commande et continuez le démarrage vers Windows normalement.
6. Ouvrez une invite de commande administrateur et exécutez les commandes suivantes:

    ```powershell
    manage-bde c: -protectors -add -rp -tpm
    manage-bde -protectors -enable c:
    manage-bde -protectors -get c: > %UserProfile%\Desktop\BitLocker-Recovery-Key.txt
    ```

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

    Sauvegardez le fichier `BitLocker-Recovery-Key.txt` de votre ordinateur de bureau sur un périphérique de stockage distinct. La perte de ce code de récupération peut entraîner la perte de données.

</div>

</details>

### FileVault

<div class="admonition recommendation" markdown>

![Logo FileVault](assets/img/encryption-software/filevault.png){ align=right }

**FileVault** est la solution de chiffrement de volume à la volée intégrée à macOS. FileVault utilise les [fonctionnalités de sécurité hardware](os/macos-overview.md#hardware-security) de Apple Silicon SoC ou de T2 Security Chip.

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title="Documentation" }

</details>

</div>

Nous vous recommandons d'éviter d'utiliser votre compte iCloud pour récupérer vos données ; à la place, vous pouvez stocker une clé de récupération localement et de façon sécurisée dans un périphérique de stockage externe.

### Linux Unified Key Setup

<div class="admonition recommendation" markdown>

![Logo LUKS](assets/img/encryption-software/luks.png){ align=right }

**LUKS** est la méthode de chiffrement de disque par défaut pour Linux. Elle peut être utilisée pour chiffrer des volumes complets, des partitions ou créer des conteneurs chiffrés.

[:octicons-repo-16: Dépôt](https://gitlab.com/cryptsetup/cryptsetup#what-the-){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup){ .card-link title="Code Source" }

</details>

</div>

<details class="example" markdown>
<summary>Créer et ouvrir des conteneurs chiffrés</summary>

```bash
dd if=/dev/urandom of=/chemin-vers-fichier bs=1M count=1024 status=progress
sudo cryptsetup luksFormat /chemin-vers-fichier
```

#### Ouvrir des conteneurs chiffrés

Nous recommandons d'ouvrir les conteneurs et les volumes avec `udisksctl` car cela utilise [Polkit](https://en.wikipedia.org/wiki/Polkit). La plupart des gestionnaires de fichiers, tels que ceux inclus dans les environnements de bureau les plus courants, peuvent déverrouiller les fichiers chiffrés. Des outils tels que [udiskie](https://github.com/coldfix/udiskie) peuvent s'exécuter dans la barre d'état système et fournir une interface utilisateur pratique.

```bash
udisksctl loop-setup -f /chemin-vers-fichier
udisksctl unlock -b /dev/loop0
```

</details>

<div class="admonition note" markdown>
<p class="admonition-title">N'oubliez pas de sauvegarder les en-têtes de volume</p>

Nous vous recommandons de toujours [sauvegarder vos en-têtes LUKS](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) en cas de panne partielle du lecteur. Cela peut être fait avec :

```bash
cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
````

</div>

## Ligne de commande

<small>Protège des menaces suivantes :</small>

- [:material-target-account: Attaques ciblées](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Les outils dotés d'une interface de ligne de commande sont utiles pour intégrer des [scripts shell](https://fr.wikipedia.org/wiki/Script_shell).

### Kryptor

<div class="admonition recommendation" markdown>

![Logo Kryptor](assets/img/encryption-software/kryptor.png){ align=right }

**Kryptor** est un outil gratuit et open source de chiffrement et de signature de fichiers qui utilise des algorithmes cryptographiques modernes et sécurisés. Il se veut être une meilleure version de [age](https://github.com/FiloSottile/age) et [Minisign](https://jedisct1.github.io/minisign) en tant qu'alternative plus simple à GPG.

[:octicons-home-16: Page d'Accueil](https://kryptor.co.uk){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kryptor.co.uk/features#privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://kryptor.co.uk/tutorial){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="Code Source" }
[:octicons-heart-16:](https://kryptor.co.uk/#donate){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:fontawesome-brands-windows: Windows](https://kryptor.co.uk)
- [:simple-apple: macOS](https://kryptor.co.uk)
- [:simple-linux: Linux](https://kryptor.co.uk)

</details>

</div>

### Tomb

<div class="admonition recommendation" markdown>

![Logo de Tomb](assets/img/encryption-software/tomb.png){ align=right }

**Tomb** est un outil pour LUKS en ligne de commande shell. Il permet d'avoir recours à la stéganographie via des [outils tiers](https://dyne.org/software/tomb/#advanced-usage).

[:octicons-home-16: Page d'Accueil](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Code Source" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title="Contribuer" }

</details>

</div>

## OpenPGP

<small>Protège contre les menaces suivantes :</small>

- [:material-target-account: Attaques ciblées](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Attaques passives](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fournisseurs de service](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

OpenPGP est parfois nécessaire pour des tâches spécifiques telles que la signature numérique et le chiffrage des e-mails. PGP possède de nombreuses fonctionnalités et est [complexe](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html) car il existe depuis longtemps. Pour des tâches telles que la signature ou le chiffrement des fichiers, nous suggérons les options ci-dessus.

Lorsque vous chiffrez avec PGP, vous avez la possibilité de configurer différentes options dans votre fichier `gpg.conf` . Nous vous recommandons de garder les options de base précisées dans la [FAQ utilisateurs GnuPG](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

<div class="admonition tip" markdown>
<p class="admonition-title">Utiliser future-defaults lors de la génération d'une clé</p>

Lorsque vous [générez une clef](https://gnupg.org/gph/en/manual/c14.html), nous vous recommandons d'utiliser la commande `future-default` afin d'indiquer à GnuPG d'utiliser des outils de cryoptographie modernes tels que [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) et [Ed25519](https://ed25519.cr.yp.to) :

```bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU Privacy Guard

<div class="admonition recommendation" markdown>

![Logo de GNU Privacy Guard](assets/img/encryption-software/gnupg.svg){ align=right }

**GnuPG** est une alternative sous licence GPL de la suite de logiciels cryptographiques PGP. GnuPG est conforme [RFC 4880](https://tools.ietf.org/html/rfc4880), qui est la spécification actuelle de l'IETF pour OpenPGP. Le projet GnuPG travaille actuellement sur une [nouvelle ébauche](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh) dans le but de moderniser OpenPGP. GnuPG fait partie du projet logiciel GNU de la Free Software Foundation et a reçu un [financement](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) majeur du gouvernement allemand.

[:octicons-home-16: Page d'Accueil](https://gnupg.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)
- [:simple-apple: macOS](https://gpgtools.org)
- [:simple-linux: Linux](https://gnupg.org/download/index.html#binary)

</details>

</div>

### GPG4win

<div class="admonition recommendation" markdown>

![Logo GPG4win](assets/img/encryption-software/gpg4win.svg){ align=right }

**GPG4win** est un paquet pour Windows de [Intevation et g10 Code](https://gpg4win.org/impressum.html). Il comprend [divers outils](https://gpg4win.org/about.html) qui peuvent vous aider à utiliser GPG sous Microsoft Windows. Le projet a été lancé et initialement [financé par](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography) l'Office Fédéral allemand pour la Sécurité de l'Information (BSI) en 2005.

[:octicons-home-16: Page d'Accueil](https://gpg4win.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="Code Source" }
[:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)

</details>

</div>

### GPG Suite

<div class="admonition recommendation" markdown>

![Logo de GPG Suite](assets/img/encryption-software/gpgsuite.png){ align=right }

**GPG Suite** permet d'utiliser OpenPGP avec [Apple Mail](email-clients.md#apple-mail-macos) et d'autre clients mail sur macOS.

Vous pouvez consulter leurs articles [Premiers Pas](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email)(fr) et [Base de connaissance](https://gpgtools.tenderapp.com/kb)(eng) en cas de difficulté.

[:octicons-home-16: Page d'Accueil](https://gpgtools.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-apple: macOS](https://gpgtools.org)

</details>

</div>

PGP Suite n'a [pas encore](https://gpgtools.com/sequoia) sorti de version stable pour macOS Sonoma et les versions ultérieures.

### OpenKeychain

<div class="admonition recommendation" markdown>

![Logo de OpenKeychain](assets/img/encryption-software/openkeychain.svg){ align=right }

**OpenKeyChain** est une implémentation de GnuPGP pour Android. Elle est généralement requise par les clients mail comme [Thunderbird](email-clients.md#thunderbird), [FairMail](email-clients.md#fairemail-android), et d'autres applications Android pour permettre d'utiliser les fonctions de chiffrement.

[:octicons-home-16: Page d'Accueil](https://openkeychain.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://openkeychain.org/help/privacy-policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://openkeychain.org/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

OpenKeychain 3.6 a été entièrement [audité](https://openkeychain.org/openkeychain-3-6) par Cure53 en octobre 2015. Vous pouvez trouver le rapport d'audit ainsi que les solutions mises en place par OpenKeyChain pour palier aux failles de sécurité [ici](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Qualifications minimales

- Les applications de chiffrement multiplateforme doivent être open-source.
- Les applications de chiffrement de fichiers doivent prendre en charge le déchiffrement sur Linux, macOS et Windows.
- Les applications de chiffrement de disques externes doivent prendre en charge le déchiffrement sur Linux, macOS et Windows.
- Les applications de chiffrement de disques internes (OS) doivent être multiplateforme ou intégrées nativement au système d'exploitation.

### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Les applications de chiffrement du système d'exploitation (FDE) devraient utiliser une sécurité matérielle telle qu'un TPM ou Secure Enclave.
- Les applications de chiffrement de fichiers devraient bénéficier d'une prise en charge native ou tierce pour les plateformes mobiles.
