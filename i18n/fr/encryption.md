---
meta_title: "Logiciels de chiffrement recommandés : VeraCrypt, Cryptomator, PicoCrypt et OpenPGP - Privacy Guides"
title: "Logiciels de chiffrement"
icon: material/file-lock
description: Le chiffrement des données est le seul moyen de contrôler qui peut y accéder. Ces outils vous permettent de chiffrer vos emails et tout autre de fichier.
cover: encryption.webp
---

Le chiffrement des données est le seul moyen de contrôler qui peut y accéder. Si vous n'utilisez pas actuellement de logiciel de chiffrement pour votre disque dur, vos e-mails ou vos fichiers, vous devriez choisir une option ici.

## Multi-plateforme

Les options répertoriées ici sont multiplateformes et parfaites pour créer des sauvegardes chiffrées de vos données.

### Cryptomator (Cloud)

<div class="admonition recommendation" markdown>

![Logo Cryptomator](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** est une solution de chiffrement conçue pour enregistrer vos fichiers de manière privée vers n'importe quel fournisseur de cloud. Il vous permet de créer des coffres-forts qui sont stockés sur un disque virtuel, dont le contenu est chiffré et synchronisé avec votre fournisseur de stockage cloud.

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
- [:simple-windows11: Windows](https://cryptomator.org/downloads)
- [:simple-apple: macOS](https://cryptomator.org/downloads)
- [:simple-linux: Linux](https://cryptomator.org/downloads)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.cryptomator.Cryptomator)

</details>

</div>

Cryptomator utilise le chiffrement AES-256 pour chiffrer les fichiers et les noms de fichiers. Cryptomator ne peut pas chiffrer certaines métadonnées telles que les dates et heures d'accès, de modification et de création, ni le nombre et la taille des fichiers et des dossiers.

Certaines bibliothèques cryptographiques de Cryptomator ont été [auditées](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) par Cure53. La portée des bibliothèques auditées comprend: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) et [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). L'audit ne s'est pas étendu à [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), qui est une bibliothèque utilisée par Cryptomator pour iOS.

Cryptomator's documentation details its intended [security target](https://docs.cryptomator.org/en/latest/security/security-target), [security architecture](https://docs.cryptomator.org/en/latest/security/architecture), and [best practices](https://docs.cryptomator.org/en/latest/security/best-practices) for use in further detail.

### Picocrypt (Fichier)

<div class="admonition recommendation" markdown>

![Logo de Picocrypt](assets/img/encryption-software/picocrypt.svg){ align=right }

**Picocrypt** est un outil de chiffrement léger et simple qui fournit un chiffrement moderne. Picocrypt utilise le chiffrement sécurisé XChaCha20 et la fonction de dérivation de clé Argon2id pour assurer un haut niveau de sécurité. Il utilise les modules x/crypto standards de Go pour ses fonctions de chiffrement.

[:octicons-repo-16: Dépôt](https://github.com/HACKERALERT/Picocrypt){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/HACKERALERT/Picocrypt){ .card-link title="Code source" }
[:octicons-heart-16:](https://opencollective.com/picocrypt){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-windows11: Windows](https://github.com/HACKERALERT/Picocrypt/releases)
- [:simple-apple: macOS](https://github.com/HACKERALERT/Picocrypt/releases)
- [:simple-linux: Linux](https://github.com/HACKERALERT/Picocrypt/releases)

</details>

</div>

### VeraCrypt (Disque)

<div class="admonition recommendation" markdown>

![logo VeraCrypt](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![logo VeraCrypt](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt** est un utilitaire gratuit et open source pour le chiffrement de fichiers/dossiers à la volée. Il peut créer un disque virtuel chiffré dans un fichier, chiffrer une partition ou l'ensemble du périphérique de stockage avec une authentification avant le démarrage.

[:octicons-home-16: Homepage](https://veracrypt.fr){ .md-button .md-button--primary }
[:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title=Documentation}
[:octicons-code-16:](https://veracrypt.fr/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://veracrypt.fr/en/Downloads.html)
- [:simple-apple: macOS](https://veracrypt.fr/en/Downloads.html)
- [:simple-linux: Linux](https://veracrypt.fr/en/Downloads.html)

</details>

</div>

VeraCrypt est un dérivé du projet TrueCrypt, qui a été abandonné. Selon ses développeurs, des améliorations de la sécurité ont été apportées et les problèmes soulevés par l'audit initial du code de TrueCrypt ont été résolus.

Lors du chiffrement avec VeraCrypt, vous avez la possibilité de choisir parmi différentes [fonctions de hachage](https://fr.wikipedia.org/wiki/VeraCrypt#Syst%C3%A8me_de_chiffrement). Nous vous suggérons de **seulement** sélectionner [SHA-512](https://fr.wikipedia.org/wiki/SHA-2) et de vous en tenir au [chiffrement par blocs AES](https://fr.wikipedia.org/wiki/Advanced_Encryption_Standard).

Truecrypt a été [audité un certain nombre de fois](https://fr.wikipedia.org/wiki/TrueCrypt#Audit_global_du_logiciel_en_2013) et VeraCrypt a également été [audité séparément](https://fr.wikipedia.org/wiki/VeraCrypt#Audit).

## Chiffrement complet du disque du système d'exploitation

Pour chiffrer le disque à partir duquel votre système d'exploitation démarre, nous recommandons généralement d'activer le logiciel de chiffrement fourni avec votre système d'exploitation plutôt que d'utiliser un outil tiers. En effet, les outils de chiffrement natifs de votre système d'exploitation utilisent souvent des fonctions spécifiques au système d'exploitation et au matériel, telles que le [cryptoprocesseur sécurisé](https://fr.wikipedia.org/wiki/Cryptoprocesseur_s%C3%A9curis%C3%A9) de votre appareil, pour protéger votre ordinateur contre des attaques physiques plus avancées. Pour les disques secondaires et les disques externes sur lesquels vous *ne démarrez pas*, nous recommandons toujours l'utilisation d'outils open-source tels que [VeraCrypt](#veracrypt-disk) plutôt que les outils ci-dessous, car ils offrent une flexibilité supplémentaire et vous permettent d'éviter l'enfermement dans un fournisseur.

### BitLocker

<div class="admonition recommendation" markdown>

![Logo BitLocker](assets/img/encryption-software/bitlocker.png){ align=right }

**BitLocker** est la solution de chiffrement intégral de volume fournie avec Microsoft Windows. The main reason we recommend it for encrypting your boot drive is because of its [use of TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm). ElcomSoft, a forensics company, has written about this feature in [Understanding BitLocker TPM Protection](https://blog.elcomsoft.com/2021/01/understanding-BitLocker-tpm-protection).

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title=Documentation}

</details>

</div>

BitLocker is [only supported](https://support.microsoft.com/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838) on Pro, Enterprise and Education editions of Windows. Il peut être activé sur les éditions Famille à condition qu'elles remplissent les pré-requis.

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

3. Access [Advanced Startup Options](https://support.microsoft.com/windows/advanced-startup-options-including-safe-mode-b90e7808-80b5-a291-d4b8-1a1af602b617). Vous devez redémarrer en appuyant sur la touche F8 avant que Windows ne démarre et aller dans l'*invite de commande* dans **Dépannage** → **Options avancées** → **Invite de commande**.
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

**FileVault** est la solution de chiffrement de volume à la volée intégrée à macOS. FileVault est recommandé parce qu'il [tire profit](https://support.apple.com/guide/security/volume-encryption-with-filevault-sec4c6dc1b6e/web) de capacités de sécurité matérielle présentes sur un SoC de silicium Apple ou une Puce de Sécurité T2.

[:octicons-info-16:](https://support.apple.com/fr-fr/guide/mac-help/mh11785/mac){ .card-link title=Documentation}

</details>

</div>

Nous recommandons de stocker une clé de récupération locale dans un endroit sûr plutôt que d'utiliser votre compte iCloud pour la récupération.

### Linux Unified Key Setup

<div class="admonition recommendation" markdown>

![Logo LUKS](assets/img/encryption-software/luks.png){ align=right }

**LUKS** est la méthode de chiffrement de disque par défaut pour Linux. Elle peut être utilisée pour chiffrer des volumes complets, des partitions ou créer des conteneurs chiffrés.

[:octicons-home-16: Homepage](https://gitlab.com/cryptsetup/cryptsetup/-/blob/main/README.md){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup){ .card-link title="Source Code" }

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

Les outils dotés d'une interface de ligne de commande sont utiles pour intégrer des [scripts shell](https://fr.wikipedia.org/wiki/Script_shell).

### Kryptor

<div class="admonition recommendation" markdown>

![Logo Kryptor](assets/img/encryption-software/kryptor.png){ align=right }

**Kryptor** est un outil gratuit et open source de chiffrement et de signature de fichiers qui utilise des algorithmes cryptographiques modernes et sécurisés. It aims to be a better version of [age](https://github.com/FiloSottile/age) and [Minisign](https://jedisct1.github.io/minisign) to provide a simple, easier alternative to GPG.

[:octicons-home-16: Homepage](https://kryptor.co.uk){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kryptor.co.uk/features#privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kryptor.co.uk/tutorial){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kryptor.co.uk/#donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://kryptor.co.uk)
- [:simple-apple: macOS](https://kryptor.co.uk)
- [:simple-linux: Linux](https://kryptor.co.uk)

</details>

</div>

### Tomb

<div class="admonition recommendation" markdown>

![Logo de Tomb](assets/img/encryption-software/tomb.png){ align=right }

**Tomb** est un outil pour LUKS en ligne de commande shell. It supports steganography via [third-party tools](https://dyne.org/software/tomb/#advanced-usage).

[:octicons-home-16: Homepage](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Source Code" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title=Contribute }

</details>

</div>

## OpenPGP

OpenPGP est parfois nécessaire pour des tâches spécifiques telles que la signature numérique et le chiffrage des e-mails. PGP possède de nombreuses fonctionnalités et est [complexe](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html) car il existe depuis longtemps. Pour des tâches telles que la signature ou le chiffrement des fichiers, nous suggérons les options ci-dessus.

Lorsque vous chiffrez avec PGP, vous avez la possibilité de configurer différentes options dans votre fichier `gpg.conf` . We recommend staying with the standard options specified in the [GnuPG user FAQ](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

<div class="admonition tip" markdown>
<p class="admonition-title">Utiliser future-defaults lors de la génération d'une clé</p>

When [generating keys](https://gnupg.org/gph/en/manual/c14.html) we suggest using the `future-default` command as this will instruct GnuPG use modern cryptography such as [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) and [Ed25519](https://ed25519.cr.yp.to):

```bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU Privacy Guard

<div class="admonition recommendation" markdown>

![Logo de GNU Privacy Guard](assets/img/encryption-software/gnupg.svg){ align=right }

**GnuPG** est une alternative sous licence GPL de la suite de logiciels cryptographiques PGP. GnuPG est conforme [RFC 4880](https://tools.ietf.org/html/rfc4880), qui est la spécification actuelle de l'IETF pour OpenPGP. The GnuPG project has been working on an [updated draft](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh) in an attempt to modernize OpenPGP. GnuPG fait partie du projet logiciel GNU de la Free Software Foundation et a reçu un [financement](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) majeur du gouvernement allemand.

[:octicons-home-16: Page d'accueil](https://gnupg.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
- [:simple-windows11: Windows](https://gpg4win.org/download.html)
- [:simple-apple: macOS](https://gpgtools.org)
- [:simple-linux: Linux](https://gnupg.org/download/index.html#binary)

</details>

</div>

### GPG4win

<div class="admonition recommendation" markdown>

![Logo GPG4win](assets/img/encryption-software/gpg4win.svg){ align=right }

**GPG4win** est un paquet pour Windows de [Intevation et g10 Code](https://gpg4win.org/impressum.html). Il comprend [divers outils](https://gpg4win.org/about.html) qui peuvent vous aider à utiliser GPG sous Microsoft Windows. Le projet a été lancé et initialement [financé par](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography) l'Office Fédéral allemand pour la Sécurité de l'Information (BSI) en 2005.

[:octicons-home-16: Page d'accueil](https://gpg4win.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title=Documentation}
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="Code source" }
[:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-windows11: Windows](https://gpg4win.org/download.html)

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

Nous vous recommandons de consulter leurs [Premiers pas](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email) et leur [Base de connaissances](https://gpgtools.tenderapp.com/kb) pour obtenir de l'aide.

[:octicons-home-16: Page d'accueil](https://gpgtools.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-apple: macOS](https://gpgtools.org)

</details>

</div>

### OpenKeychain

<div class="admonition recommendation" markdown>

![Logo OpenKeychain](assets/img/encryption-software/openkeychain.svg){ align=right }

**OpenKeychain** est une implémentation Android de GnuPG. It's commonly required by mail clients such as [K-9 Mail](email-clients.md#k-9-mail-android) and [FairEmail](email-clients.md#fairemail-android) and other Android apps to provide encryption support. Cure53 completed a [security audit](https://openkeychain.org/openkeychain-3-6) of OpenKeychain 3.6 in October 2015. Les détails techniques concernant l'audit et les solutions d'OpenKeychain peuvent être trouvés [ici](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).

[:octicons-home-16: Homepage](https://openkeychain.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://openkeychain.org/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://openkeychain.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

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
