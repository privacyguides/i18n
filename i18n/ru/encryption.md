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
    
    ??? downloads "Скачать"
    
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
    
    ??? downloads "Скачать"
    
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
    
    ??? downloads "Скачать"
    
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

??? example "Включение BitLocker на Windows Home"

    Чтобы включить BitLocker в "Домашних" редакциях Windows, необходимо, чтобы разделы были отформатированы с помощью [GUID Partition Table](https://en.wikipedia.org/wiki/GUID_Partition_Table) и имели выделенный модуль TPM (v1.2, 2.0+).

    1. Откройте командную строку и проверьте формат таблицы разделов диска с помощью следующей команды. Вы должны увидеть "**GPT**" в разделе "Стиль раздела":

        ```
        powershell Get-Disk
        ```

    2. Выполните эту команду (в командной строке от имени администратора), чтобы проверить версию вашего TPM. Вы должны увидеть `2.0` или `1.2`, перечисленные рядом с `SpecVersion`:

        ```
        powershell Get-WmiObject -Namespace "root/cimv2/security/microsofttpm" -Class WIN32_tpm
        ```

    3. Откройте [дополнительные параметры запуска](https://support.microsoft.com/en-us/windows/advanced-startup-options-including-safe-mode-b90e7808-80b5-a291-d4b8-1a1af602b617). Необходимо перезагрузиться, нажав клавишу F8 до запуска Windows, и перейти в *командную строку* в разделе **Устранение неполадок** → **Дополнительные параметры** → **Командная строка**.

    4. Войдите под учетной записью администратора и введите следующее для запуска шифрования:

        ```
        manage-bde -on c: -used
        ```

    5. Закройте командную строку и продолжите обычную загрузку в Windows.

    6. Откройте командную строку от имени администратора и выполните следующие команды:

        ```
        manage-bde c: -protectors -add -rp -tpm
        manage-bde -protectors -enable c:
        manage-bde -protectors -get c: > %UserProfile%\Desktop\BitLocker-Recovery-Key.txt
        ```

        !!! tip "Совет"
   
        Создайте резервную копию файла `BitLocker-Recovery-Key.txt` с рабочего стола на отдельном устройстве хранения данных. Потеря этого кода восстановления может привести к потере данных.

### FileVault

!!! recommendation

    ![Логотип FileVault](assets/img/encryption-software/filevault.png){ align=right }
    
    **FileVault** - это решение для шифрования томов "на лету", встроенное в macOS. FileVault рекомендуется, поскольку он [использует](https://support.apple.com/guide/security/volume-encryption-with-filevault-sec4c6dc1b6e/web) аппаратные возможности безопасности, представленные в SoC процессорах Apple или чипе безопасности T2.
    
    [:octicons-info-16:](https://support.apple.com/ru-ru/guide/mac-help/mh11785/mac){ .card-link title=Документация}

Мы рекомендуем хранить локальный ключ восстановления в надежном месте, а не использовать для восстановления учетную запись iCloud.

### Linux Unified Key Setup (LUKS)

!!! recommendation

    ![Логотип LUKS](assets/img/encryption-software/luks.png){ align=right }
    
    **LUKS** - это стандартный метод FDE для Linux. Его можно использовать для шифрования полных томов, разделов или создания зашифрованных контейнеров.
    
    [:octicons-home-16: Домашняя страница](https://gitlab.com/cryptsetup/cryptsetup/-/blob/main/README.md){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title=Документация}
    [:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup/){ .card-link title="Исходный код" }

??? example "Создание и открытие зашифрованного контейнера"

    ```
    dd if=/dev/urandom of=/path-to-file bs=1M count=1024 status=progress
    sudo cryptsetup luksFormat /path-to-file
    ```


    #### Открытие зашифрованных контейнеров
    Мы рекомендуем открывать контейнеры и тома с помощью `udisksctl`, так как при этом используется [Polkit](https://en.wikipedia.org/wiki/Polkit). Большинство файловых менеджеров, например, входящих в состав популярных настольных сред, могут разблокировать зашифрованные файлы. Такие инструменты, как [udiskie](https://github.com/coldfix/udiskie), могут запускаться в системном трее и предоставлять полезный пользовательский интерфейс.
    ```
    udisksctl loop-setup -f /path-to-file
    udisksctl unlock -b /dev/loop0
    ```

!!! note "Не забывайте создавать резервные копии заголовков томов"

    Мы рекомендуем всегда [создавать резервные копии заголовков LUKS](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) на случай частичного отказа диска. Это можно сделать с помощью:

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
    
    [:octicons-globe-16: Сайт](https://hat.sh){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://hat.sh/about/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://hat.sh/about/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/sh-dv/hat.sh){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://github.com/sh-dv/hat.sh#donations){ .card-link title="Способы донатов можно найти внизу сайта" }

## Шифрование через командную строку

Инструменты с интерфейсом командной строки полезны для интеграции [shell scripts](https://en.wikipedia.org/wiki/Shell_script).

### Kryptor

!!! recommendation

    ![Логотип Kryptor](assets/img/encryption-software/kryptor.png){ align=right }
    
    **Kryptor** - это бесплатный инструмент для шифрования и подписи файлов с открытым исходным кодом, использующий современные и безопасные криптографические алгоритмы. Его цель - стать улучшенной версией [age](https://github.com/FiloSottile/age) и [Minisign](https://jedisct1.github.io/minisign/), чтобы обеспечить простую, удобную для пользователя альтернативу GPG.
    
    [:octicons-home-16: Домашняя страница](https://www.kryptor.co.uk){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.kryptor.co.uk/features#privacy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://www.kryptor.co.uk/tutorial){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://www.kryptor.co.uk/#donate){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-windows11: Windows](https://www.kryptor.co.uk)
        - [:simple-apple: macOS](https://www.kryptor.co.uk)
        - [:simple-linux: Linux](https://www.kryptor.co.uk)

### Tomb

!!! recommendation

    ![Логотип Tomb](assets/img/encryption-software/tomb.png){ align=right }
    
    **Tomb** - это оболочка командной строки для LUKS. Он поддерживает стеганографию с помощью [сторонних инструментов] (https://github.com/dyne/Tomb#how-does-it-work).
    
    [:octicons-home-16: Домашняя страница](https://www.dyne.org/software/tomb){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://www.dyne.org/donate){ .card-link title=Поддержать}

## OpenPGP

OpenPGP иногда необходим для решения специфических задач, таких как цифровая подпись и шифрование электронной почты. PGP имеет множество функций и является [комплексным](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html), поскольку существует уже долгое время. Для таких задач, как подписание или шифрование файлов, мы предлагаем использовать вышеуказанные варианты.

При шифровании с помощью PGP у вас есть возможность настроить различные параметры в файле `gpg.conf`. Мы рекомендуем придерживаться стандартных опций, указанных в [FAQ пользователя GnuPG](https://www.gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

!!! tip "Используйте future defaults при генерации ключа"

    При [генерации ключей] (https://www.gnupg.org/gph/en/manual/c14.html) мы рекомендуем использовать команду `future-default`, так как это позволит GnuPG использовать современную криптографию, такую как [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) и [Ed25519](https://ed25519.cr.yp.to/):

    ```bash
    gpg --quick-gen-key alice@example.com future-default
    ```

### GNU Privacy Guard

!!! recommendation

    ![Логотип GNU Privacy Guard](assets/img/encryption-software/gnupg.svg){ align=right }
    
    **GnuPG** - это GPL-альтернатива криптографическому пакету PGP. GnuPG совместим с [RFC 4880] (https://tools.ietf.org/html/rfc4880), который является текущей спецификацией IETF для OpenPGP. Проект GnuPG работает над [обновленным проектом](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh/) в попытке улучшить OpenPGP. GnuPG является частью фонда свободного программного обеспечения GNU и получил крупное [финансирование](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) от правительства Германии.
    
    [:octicons-home-16: Домашняя страница](https://gnupg.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title=Документация}
    [:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
        - [:simple-windows11: Windows](https://gpg4win.org/download.html)
        - [:simple-apple: macOS](https://gpgtools.org)
        - [:simple-linux: Linux](https://gnupg.org/download/index.html#binary)

### GPG4win

!!! recommendation

    ![Логотип GPG4win](assets/img/encryption-software/gpg4win.svg){ align=right }
    
    **GPG4win** - это пакет для Windows от [Intevation и g10 Code](https://gpg4win.org/impressum.html). Он включает в себя [различные инструменты](https://gpg4win.org/about.html), которые могут помочь вам в использовании GPG в Microsoft Windows. Проект был инициирован и первоначально [финансировался](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography) федеральным управлением по информационной безопасности Германии (BSI) в 2005 году.
    
    [:octicons-home-16: Домашняя страница](https://gpg4win.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title=Документация}
    [:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-windows11: Windows](https://gpg4win.org/download.html)

### GPG Suite

!!! note "Примечание"

    Мы рекомендуем [Canary Mail](email-clients/#canary-mail) для использования PGP с электронной почтой на устройствах с iOS.

!!! recommendation

    ![Логотип GPG Suite](assets/img/encryption-software/gpgsuite.png){ align=right }
    
    **GPG Suite** обеспечивает поддержку OpenPGP для [Apple Mail](email-clients.md#apple-mail) и macOS.
    
    Мы рекомендуем ознакомиться с их [первыми шагами](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email) и [базой знаний](https://gpgtools.tenderapp.com/kb) для получения поддержки.
    
    [:octicons-home-16: Домашняя страница](https://gpgtools.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-apple: macOS](https://gpgtools.org)

### OpenKeychain

!!! recommendation

    ![Логотип OpenKeychain](assets/img/encryption-software/openkeychain.svg){ align=right }
    
    **OpenKeychain** - это Android-реализация GnuPG. Он обычно требуется почтовым клиентам, таким как [K-9 Mail](email-clients.md#k-9-mail) и [FairEmail](email-clients.md#fairemail), а также другим приложениям для Android для обеспечения поддержки шифрования. Компания Cure53 завершила [аудит безопасности](https://www.openkeychain.org/openkeychain-3-6) OpenKeychain 3.6 в октябре 2015 года. Технические подробности об аудите и решениях OpenKeychain можно найти на сайте [здесь](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).
    
    [:octicons-home-16: Домашняя страница](https://www.openkeychain.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.openkeychain.org/help/privacy-policy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://www.openkeychain.org/faq/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

!!! example "Это новый раздел"

    Мы всё еще работаем над установлением критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у вас есть вопросы по поводу наших критериев, пожалуйста, [задавайте их на нашем форуме](https://discuss.privacyguides.net/latest). Если какой-то критерий здесь не указан, это не значит, что мы его не учли. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

### Минимальные требования

- Кросс-платформенные приложения для шифрования должны быть с открытым исходным кодом.
- Приложения для шифрования файлов должны поддерживать дешифрование на Linux, macOS и Windows.
- Приложения для шифрования внешних дисков должны поддерживать дешифрование в Linux, macOS и Windows.
- Приложения для шифрования всего диска должны быть кроссплатформенными или встроенными в операционную систему.

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Приложения для шифрования операционной системы (FDE) должны использовать аппаратную защиту, такую как TPM или Secure Enclave.
- Приложения для шифрования файлов должны иметь поддержку мобильных платформ.
