---
meta_title: "Рекомендуемые программы для шифрования: VeraCrypt, Cryptomator, PicoCrypt и OpenPGP - Privacy Guides"
title: "Программы для шифрования"
icon: material/file-lock
description: Шифрование данных - единственный способ контролировать доступ к ним. Эти программы позволяют шифровать электронную почту и любые другие файлы.
cover: encryption.png
---

Шифрование данных - единственный способ контролировать доступ к ним. Если вы еще не используете какие-либо инструменты шифрования диска, электронной почты или файлов, то вы можете выбрать один из них тут.

## Мультиплатформенные приложения

Перечисленные здесь программы являются многоплатформенными и отлично подходят для создания зашифрованных резервных копий ваших данных.

### Cryptomator (Облако)

!!! recommendation

    ![Логотип Cryptomator](assets/img/encryption-software/cryptomator.svg){ align=right }
    
    **Cryptomator** - это программа для шифрования, разработанная для приватного хранения файлов в любом облачном хранилище. Программа может создавать хранилища в виртуальном диске, содержимое которых зашифровано и синхронизировано с твоим облачным хранилищем.
    
    [:octicons-home-16: Домашняя страница](https://cryptomator.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://docs.cryptomator.org/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/cryptomator){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://cryptomator.org/donate/){ .card-link title=Поддержать }
    
    ??? скачать
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.cryptomator)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/cryptomator-2/id1560822163)
        - [:simple-android: Android](https://cryptomator.org/android)
        - [:simple-windows11: Windows](https://cryptomator.org/downloads)
        - [:simple-apple: macOS](https://cryptomator.org/downloads)
        - [:simple-linux: Linux](https://cryptomator.org/downloads)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.cryptomator.Cryptomator)

Cryptomator использует шифрование AES-256 для шифрования как файлов, так и их имён. Cryptomator не может зашифровать метаданные, такие как: время создания, изменения и доступа к файлу, количество и размер файлов и папок.

Cure53 провёл [аудит](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) некоторых криптографических библиотек Cryptomator. Эти библиотеки включают в себя [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) и [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). Аудит не проходила [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), которая сейчас используется в iOS.

В документации Cryptomator подробно описаны его предполагаемые [цели безопасности](https://docs.cryptomator.org/en/latest/security/security-target/), [архитектура безопасности](https://docs.cryptomator.org/en/latest/security/architecture/), и [лучшие практики](https://docs.cryptomator.org/en/latest/security/best-practices/) для использования.

### Picocrypt (Файлы)

!!! recommendation

    ![Логотип Picocrypt](assets/img/encryption-software/picocrypt.svg){ align=right }
    
    **Picocrypt** - это маленькая и простая программа, предоставляющая современное шифрование. Picocrypt использует безопасный шифр XChaCha20 и функцию формирования ключа Argon2id для обеспечения высокого уровня безопасности. Для функций шифрования он использует стандартные модули Go x/crypto.
    
    [:octicons-repo-16: Репозиторий](https://github.com/HACKERALERT/Picocrypt){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/HACKERALERT/Picocrypt){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://opencollective.com/picocrypt){ .card-link title=Поддержать }
    
    ??? скачать
    
        - [:simple-windows11: Windows](https://github.com/HACKERALERT/Picocrypt/releases)
        - [:simple-apple: macOS](https://github.com/HACKERALERT/Picocrypt/releases)
        - [:simple-linux: Linux](https://github.com/HACKERALERT/Picocrypt/releases)

### VeraCrypt (Диск)

!!! recommendation

    ![Логотип VeraCrypt](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
    ![Логотип VeraCrypt](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }
    
    **VeraCrypt** - это свободно распространяемая утилита с исходным кодом, используемая для шифрования "на лету". Программа может создавать виртуальный зашифрованный диск в файле, зашифровать логический раздел или даже зашифровать все устройство с предзагрузочной аутентификацией.
    
    [:octicons-home-16: Домашняя страница](https://veracrypt.fr){ .md-button .md-button--primary }
    [:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title=Документация}
    [:octicons-code-16:](https://veracrypt.fr/code/){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title=Поддержать }
    
    ??? скачать
    
        - [:simple-windows11: Windows](https://www.veracrypt.fr/en/Downloads.html)
        - [:simple-apple: macOS](https://www.veracrypt.fr/en/Downloads.html)
        - [:simple-linux: Linux](https://www.veracrypt.fr/en/Downloads.html)

VeraCrypt - это форк, прекратившего свое существование, проекта TrueCrypt. По словам разработчиков, были реализованы улучшения безопасности и решены проблемы, найденные в ходе первоначального аудита кода TrueCrypt.

При шифровании с помощью VeraCrypt ты можешь выбрать различные [хэш-функции](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme). Мы настоятельно рекомендуем выбрать **только** [SHA-512](https://en.wikipedia.org/wiki/SHA-512) и блочное шифрование по алгоритму [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard).

Аудит Truecrypt проводился [несколько раз](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits). Veracrypt [проходил](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit) аудит уже отдельно.

## Шифрование всего диска

Современные ОС включают в себя [шифрование диска](https://en.wikipedia.org/wiki/Disk_encryption) и используют [безопасный криптопроцессор](https://en.wikipedia.org/wiki/Secure_cryptoprocessor).

### BitLocker

!!! recommendation

    ![Логотип BitLocker](assets/img/encryption-software/bitlocker.png){ align=right }
    
    **BitLocker** - решение для полного шифрования диска в Microsoft Windows. Основная причина, по которой мы рекомендуем его, заключается в [использовании доверенного платформенного модуля (TPM)](https://docs.microsoft.com/en-us/windows/security/information-protection/tpm/how-windows-uses-the-tpm). [ElcomSoft](https://ru.wikipedia.org/wiki/ElcomSoft), криминалистическая компания, написала об этом в [Understanding BitLocker TPM Protection](https://blog.elcomsoft.com/2021/01/understanding-BitLocker-tpm-protection/).
    
    [:octicons-info-16:](https://docs.microsoft.com/en-us/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title=Документация}

BitLocker [поддерживается только](https://support.microsoft.com/en-us/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838) в Pro, Enterprise и Education версиях Windows. Эту функцию можно включить и в Home версии при соответствии условиям.

??? пример «Включение BitLocker на Windows Home»

    Чтобы включить BitLocker в "Домашних" редакциях Windows, необходимо, чтобы разделы были отформатированы с помощью [GUID Partition Table](https://en.wikipedia.org/wiki/GUID_Partition_Table) и имели выделенный модуль TPM (v1.2, 2.0+).

    1. Open a command prompt and check your drive's partition table format with the following command. You should see "**GPT**" listed under "Partition Style":

        ```
        powershell Get-Disk
        ```

    2. Run this command (in an admin command prompt) to check your TPM version. You should see `2.0` or `1.2` listed next to `SpecVersion`:

        ```
        powershell Get-WmiObject -Namespace "root/cimv2/security/microsofttpm" -Class WIN32_tpm
        ```

    3. Access [Advanced Startup Options](https://support.microsoft.com/en-us/windows/advanced-startup-options-including-safe-mode-b90e7808-80b5-a291-d4b8-1a1af602b617). You need to reboot while pressing the F8 key before Windows starts and go into the *command prompt* in **Troubleshoot** → **Advanced Options** → **Command Prompt**.

    4. Login with your admin account and type this in the command prompt to start encryption:

        ```
        manage-bde -on c: -used
        ```

    5. Close the command prompt and continue booting to regular Windows.

    6. Open an admin command prompt and run the following commands:

        ```
        manage-bde c: -protectors -add -rp -tpm
        manage-bde -protectors -enable c:
        manage-bde -protectors -get c: > %UserProfile%\Desktop\BitLocker-Recovery-Key.txt
        ```

        !!! tip
   
        Backup `BitLocker-Recovery-Key.txt` on your Desktop to a separate storage device. Loss of this recovery code may result in loss of data.

### FileVault

!!! recommendation

    ![Логотип FileVault](assets/img/encryption-software/filevault.png){ align=right }
    
    **FileVault** - это решение для шифрования томов "на лету", встроенное в macOS. FileVault is recommended because it [leverages](https://support.apple.com/guide/security/volume-encryption-with-filevault-sec4c6dc1b6e/web) hardware security capabilities present on an Apple silicon SoC or T2 Security Chip.
    
    [Перейти на support.apple.com](https://support.apple.com/en-us/HT204837){ .md-button .md-button--primary }

We recommend storing a local recovery key in a secure place as opposed to using your iCloud account for recovery.

### Linux Unified Key Setup (LUKS)

!!! recommendation

    ![LUKS logo](assets/img/encryption-software/luks.png){ align=right }
    
    **LUKS** is the default FDE method for Linux. It can be used to encrypt full volumes, partitions, or create encrypted containers.
    
    [:octicons-home-16: Homepage](https://gitlab.com/cryptsetup/cryptsetup/-/blob/main/README.md){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup/){ .card-link title="Source Code" }

??? example "Creating and opening encrypted containers"

    ```
    dd if=/dev/urandom of=/path-to-file bs=1M count=1024 status=progress
    sudo cryptsetup luksFormat /path-to-file
    ```


    #### Opening encrypted containers
    We recommend opening containers and volumes with `udisksctl` as this uses [Polkit](https://en.wikipedia.org/wiki/Polkit). Most file managers, such as those included with popular desktop environments, can unlock encrypted files. Tools like [udiskie](https://github.com/coldfix/udiskie) can run in the system tray and provide a helpful user interface.
    ```
    udisksctl loop-setup -f /path-to-file
    udisksctl unlock -b /dev/loop0
    ```

!!! note "Remember to back up volume headers"

    We recommend you always [back up your LUKS headers](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) in case of partial drive failure. This can be done with:

    ```
    cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
    ```

## Шифрование через браузер

Шифрование через браузер может быть полезным, если вам нужно зашифровать файл, но вы не можете установить программу для шифрования на свое устройство.

### hat.sh

!!! recommendation

    ![Логотип hat.sh](assets/img/encryption-software/hat-sh.png#only-light){ align=right }
    ![Логотип hat.sh](assets/img/encryption-software/hat-sh-dark.png#only-dark){ align=right }
    
    **Hat.sh** - это сайт, который безопасно зашифровывает данные через браузер. Сайт может быть полезен, если вам нужно зашифровать файл, но вы не можете установить какое-либо программное обеспечение на свое устройство из-за политики организации.
    
    [Перейти на hat.sh](https://hat.sh){ .md-button .md-button--primary }

## Шифрование через командную строку

Инструменты с интерфейсом командной строки полезны для интеграции [сценариев оболочки](https://en.wikipedia.org/wiki/Shell_script).

### Kryptor

!!! recommendation

    ![Логотип Kryptor](assets/img/encryption-software/kryptor.png){ align=right }
    
    **Kryptor** - это бесплатный инструмент для шифрования и подписи файлов с открытым исходным кодом, использующий современные и безопасные криптографические алгоритмы. Его цель - стать улучшенной версией [age](https://github.com/FiloSottile/age) и [Minisign](https://jedisct1.github.io/minisign/), чтобы обеспечить простую, удобную для пользователя альтернативу GPG.
    
    [Перейти на kryptor.co.uk](https://www.kryptor.co.uk){ .md-button .md-button--primary } [Политика конфиденциальности](https://www.kryptor.co.uk/features#privacy){ .md-button } downloads
    
        - [:fontawesome-brands-windows: Windows](https://www.kryptor.co.uk)
        - [:fontawesome-brands-apple: macOS](https://www.kryptor.co.uk)
        - [:fontawesome-brands-linux: Linux](https://www.kryptor.co.uk)
        - [:fontawesome-brands-github: Исходный код](https://github.com/samuel-lucas6/Kryptor)

### Tomb

!!! recommendation

    ![Логотип Tomb](assets/img/encryption-software/tomb.png){ align=right }
    
    **Tomb** - это оболочка командной строки для LUKS. Он поддерживает стеганографию с помощью [сторонних инструментов] (https://github.com/dyne/Tomb#how-does-it-work).
    
    [Перейти на dyne.org](https://www.dyne.org/software/tomb){ .md-button .md-button--primary }

## OpenPGP

OpenPGP is sometimes needed for specific tasks such as digitally signing and encrypting email. PGP имеет множество функций и является [сложным](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html) , поскольку существует уже долгое время. Для таких задач, как подписание или шифрование файлов, мы предлагаем использовать вышеуказанные варианты.

When encrypting with PGP, you have the option to configure different options in your `gpg.conf` file. Мы рекомендуем придерживаться стандартных опций, указанных в FAQ пользователя GnuPG [](https://www.gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

!!! совет "Использовать будущие значения по умолчанию при генерации ключа"

    When [generating keys](https://www.gnupg.org/gph/en/manual/c14.html) we suggest using the `future-default` command as this will instruct GnuPG use modern cryptography such as [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) and [Ed25519](https://ed25519.cr.yp.to/):

    ```bash
    gpg --quick-gen-key alice@example.com future-default
    ```

### GNU Privacy Guard

!!! recommendation

    ![Логотип GNU Privacy Guard](assets/img/encryption-software/gnupg.svg){ align=right }
    
    **GnuPG** - это GPL-альтернатива криптографическому пакету PGP. GnuPG совместим с [RFC 4880] (https://tools.ietf.org/html/rfc4880), который является текущей спецификацией IETF для OpenPGP. Проект GnuPG работает над [обновленным проектом](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh/) в попытке улучшить OpenPGP. GnuPG является частью фонда свободного программного обеспечения GNU и получил крупное [финансирование](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) от правительства Германии.
    
    [Перейти на gnupg.org](https://gnupg.org){ .md-button .md-button--primary } [Политика конфиденциальности](https://gnupg.org/privacy-policy.html){ .md-button }
     downloads
    
        - [:fontawesome-brands-windows: Windows](download.html)
        - [:fontawesome-brands-apple: macOS](https://gpgtools.org)
        - [:fontawesome-brands-linux: Linux](https://gnupg.org/download/index.html#binary)
        - [:fontawesome-brands-google-play: Flatpak](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
        - [:fontawesome-brands-git: Исходный код](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git)

### GPG4win

!!! recommendation

    ![GPG4win logo](assets/img/encryption-software/gpg4win.svg){ align=right }
    
    **GPG4win** is a package for Windows from [Intevation and g10 Code](https://gpg4win.org/impressum.html). It includes [various tools](https://gpg4win.org/about.html) that can assist you in using GPG on Microsoft Windows. The project was initiated and originally [funded by](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography) Germany's Federal Office for Information Security (BSI) in 2005.
    
    [Перейти на gpg4win.org](https://gpg4win.org){ .md-button .md-button--primary } [Privacy Policy](https://gpg4win.org/privacy-policy.html){ .md-button } downloads
    
        - [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)
        - [:fontawesome-brands-git: Исходный код](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary)

### GPG Suite

!!! note

    We suggest [Canary Mail](email-clients.md#canary-mail) for using PGP with email on iOS devices.

!!! recommendation

    ![GPG Suite logo](assets/img/encryption-software/gpgsuite.png){ align=right }
    
    **GPG Suite** provides OpenPGP support for [Apple Mail](email-clients.md#apple-mail) and macOS.
    
    We recommend taking a look at their [First steps](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email) and [Knowledge base](https://gpgtools.tenderapp.com/kb) for support.
    
    [:octicons-home-16: Homepage](https://gpgtools.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-apple: macOS](https://gpgtools.org)

### OpenKeychain

!!! recommendation

    ![Логотип OpenKeychain](assets/img/encryption-software/openkeychain.svg){ align=right }
    
    **OpenKeychain** - это Android-реализация GnuPG. It's commonly required by mail clients such as [K-9 Mail](email-clients.md#k-9-mail) and [FairEmail](email-clients.md#fairemail) and other Android apps to provide encryption support. Cure53 completed a [security audit](https://www.openkeychain.org/openkeychain-3-6) of OpenKeychain 3.6 in October 2015. Technical details about the audit and OpenKeychain's solutions can be found [here](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).
    
    [Перейти на openkeychain.org](https://www.openkeychain.org){ .md-button .md-button--primary } [Политика конфиденциальности](https://www.openkeychain.org/help/privacy-policy){ .md-button } downloads
    
        - [:fontawesome-brands-google-play: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
        - [:pg-f-droid: F-Droid](https://f-droid.org/packages/org.sufficientlysecure.keychain/)
        - [:fontawesome-brands-git: Исходный код](https://github.com/open-keychain/open-keychain)

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! Для уменьшения этой угрозы рассмотрите возможность самостоятельного хостинга.

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. Мы учитываем и обсуждаем много факторов, перед тем как рекомендовать какой-то проект, и документирование каждого из них ещё не завершено.

### Минимальные требования

- Cross-platform encryption apps must be open-source.
- File encryption apps must support decryption on Linux, macOS, and Windows.
- External disk encryption apps must support decryption on Linux, macOS, and Windows.
- Internal (OS) disk encryption apps must be cross-platform or built in to the operating system natively.

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Operating System (FDE) encryption apps should utilize hardware security such as a TPM or Secure Enclave.
- File encryption apps should have first- or third-party support for mobile platforms.
