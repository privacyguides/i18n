---
meta_title: "암호화 소프트웨어 권장 목록: VeraCrypt, Cryptomator, PicoCrypt, OpenPGP - Privacy Guides"
title: "암호화 소프트웨어"
icon: material/file-lock
description: 데이터 암호화는 데이터에 접근 가능한 사람을 통제하는 유일한 방법입니다. 암호화 툴로 이메일이나 각종 파일을 암호화하세요.
cover: encryption.png
---

데이터 암호화는 데이터에 접근 가능한 사람을 통제하는 유일한 방법입니다. 만약 아직 하드 디스크, 이메일, 파일들을 암호화하지 않았다면 여기에 있는 프로그램을 사용하는것을 추천합니다.

## Multi-platform

여기에 나열된 프로그램들은 다양한 플랫폼에서 사용이 가능하며 암호화된 데이터 백업등을 생성하는데에 사용할 수 닜습니다.

### Cryptomator (클라우드)

!!! recommendation

    ![Cryptomator 로고](assets/img/encryption-software/cryptomator.svg){ align=right }
    **Cryptomator**는 다양한 클라우드와 호환되도록 설계된 파일 암호화 솔루션입니다. 가상 드라이브에 Vault라고 불리는 파일 저장소를 생성할 수 있고, 여기에 저장된 파일들은 암호화되며 자동으로 클라우드와 동기화됩니다.
    
    [:octicons-home-16: 홈페이지](https://cryptomator.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://docs.cryptomator.org/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/cryptomator){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://cryptomator.org/donate/){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.cryptomator)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/cryptomator-2/id1560822163)
        - [:simple-android: Android](https://cryptomator.org/android)
        - [:simple-windows11: Windows](https://cryptomator.org/downloads)
        - [:simple-apple: macOS](https://cryptomator.org/downloads)
        - [:simple-linux: Linux](https://cryptomator.org/downloads)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.cryptomator.Cryptomator)

Cryptomator uses AES-256 encryption to encrypt both files and filenames. Cryptomator cannot encrypt metadata such as access, modification, and creation timestamps, nor the number and size of files and folders.

Some Cryptomator cryptographic libraries have been [audited](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) by Cure53. The scope of the audited libraries includes: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) and [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). The audit did not extend to [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), which is a library used by Cryptomator for iOS.

Cryptomator's documentation details its intended [security target](https://docs.cryptomator.org/en/latest/security/security-target/), [security architecture](https://docs.cryptomator.org/en/latest/security/architecture/), and [best practices](https://docs.cryptomator.org/en/latest/security/best-practices/) for use in further detail.

### Picocrypt (파일)

!!! recommendation

    ![Picocrypt logo](assets/img/encryption-software/picocrypt.svg){ align=right }
    
    **Picocrypt** is a small and simple encryption tool that provides modern encryption. Picocrypt uses the secure XChaCha20 cipher and the Argon2id key derivation function to provide a high level of security. It uses Go's standard x/crypto modules for its encryption features.
    
    [:octicons-repo-16: 저장소](https://github.com/HACKERALERT/Picocrypt){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/HACKERALERT/Picocrypt){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://opencollective.com/picocrypt){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-windows11: Windows](https://github.com/HACKERALERT/Picocrypt/releases)
        - [:simple-apple: macOS](https://github.com/HACKERALERT/Picocrypt/releases)
        - [:simple-linux: Linux](https://github.com/HACKERALERT/Picocrypt/releases)

### VeraCrypt (디스크)

!!! recommendation

    ![VeraCrypt logo](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
    ![VeraCrypt logo](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }
    
    **VeraCrypt** is a source-available freeware utility used for on-the-fly encryption. It can create a virtual encrypted disk within a file, encrypt a partition, or encrypt the entire storage device with pre-boot authentication.
    
    [:octicons-home-16: 홈페이지](https://veracrypt.fr){ .md-button .md-button--primary }
    [:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title=문서}
    [:octicons-code-16:](https://veracrypt.fr/code/){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-windows11: Windows](https://www.veracrypt.fr/en/Downloads.html)
        - [:simple-apple: macOS](https://www.veracrypt.fr/en/Downloads.html)
        - [:simple-linux: Linux](https://www.veracrypt.fr/en/Downloads.html)

VeraCrypt is a fork of the discontinued TrueCrypt project. According to its developers, security improvements have been implemented and issues raised by the initial TrueCrypt code audit have been addressed.

When encrypting with VeraCrypt, you have the option to select from different [hash functions](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme). We suggest you **only** select [SHA-512](https://en.wikipedia.org/wiki/SHA-512) and stick to the [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) block cipher.

Truecrypt는 [여러 차례 감사 받은 이력이 있으며](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits), VeraCrypt 또한 [별도 감사](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit)를 받았습니다.

## OS 전체 디스크 암호화

현대 운영 체제에는 [FDE(Full Disk Encryption, 전체 디스크 암호화)](https://ko.wikipedia.org/wiki/%EB%94%94%EC%8A%A4%ED%81%AC_%EC%95%94%ED%98%B8%ED%99%94) 기능이 내장되어 있습니다. 훗날에는 [보안 암호화 프로세서(Secure Cryptoprocessor)](https://en.wikipedia.org/wiki/Secure_cryptoprocessor)도 기본적으로 탑재될 것입니다.

### BitLocker

!!! recommendation

    ![BitLocker logo](assets/img/encryption-software/bitlocker.png){ align=right }
    
    **BitLocker** is the full volume encryption solution bundled with Microsoft Windows. The main reason we recommend it is because of its [use of TPM](https://docs.microsoft.com/en-us/windows/security/information-protection/tpm/how-windows-uses-the-tpm). [ElcomSoft](https://en.wikipedia.org/wiki/ElcomSoft), a forensics company, has written about it in [Understanding BitLocker TPM Protection](https://blog.elcomsoft.com/2021/01/understanding-BitLocker-tpm-protection/).
    
    [:octicons-info-16:](https://learn.microsoft.com/ko-kr/windows/security/information-protection/bitlocker/bitlocker-overview){ .card-link title=문서}

BitLocker is [only supported](https://support.microsoft.com/en-us/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838) on Pro, Enterprise and Education editions of Windows. It can be enabled on Home editions provided that they meet the prerequisites.

??? example "Windows Home에서 BitLocker를 활성화하는 방법"

    To enable BitLocker on "Home" editions of Windows, you must have partitions formatted with a [GUID Partition Table](https://en.wikipedia.org/wiki/GUID_Partition_Table) and have a dedicated TPM (v1.2, 2.0+) module.

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

        !!! tip "도움말"
   
        데스크톱의 `BitLocker-Recovery-Key.txt`를 별도 저장 장치에 백업하세요. 해당 복구 코드를 분실하면 데이터를 잃어버리게 될 수 있습니다.

### FileVault

!!! recommendation

    ![FileVault 로고](assets/img/encryption-software/filevault.png){ align=right }
    
    **FileVault**는 macOS에 기본 내장된, 즉시 사용 가능한 볼륨 암호화 솔루션입니다. FileVault is recommended because it [leverages](https://support.apple.com/guide/security/volume-encryption-with-filevault-sec4c6dc1b6e/web) hardware security capabilities present on an Apple silicon SoC or T2 Security Chip.
    
    [:octicons-info-16:](https://support.apple.com/ko-kr/guide/mac-help/mh11785/mac){ .card-link title=문서}

저희는 복구 수단으로 iCloud 계정을 사용하는 것보다는 로컬 복구 키를 안전한 곳에 보관해둘 것을 권장드립니다.

### Linux Unified Key Setup

!!! recommendation

    ![LUKS 로고](assets/img/encryption-software/luks.png){ align=right }
    
    **LUKS**는 Linux에서 기본으로 사용하는 FDE 방식입니다. 전체 볼륨, 파티션을 암호화하거나 암호화 컨테이너를 만들 수 있습니다.
    
    [:octicons-home-16: 홈페이지](https://gitlab.com/cryptsetup/cryptsetup/-/blob/main/README.md){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title=문서}
    [:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup/){ .card-link title="소스 코드" }

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

## 브라우저 기반

Browser-based encryption can be useful when you need to encrypt a file but cannot install software or apps on your device.

### hat.sh

!!! recommendation

    ![hat.sh logo](assets/img/encryption-software/hat-sh.png#only-light){ align=right }
    ![hat.sh logo](assets/img/encryption-software/hat-sh-dark.png#only-dark){ align=right }
    
    **Hat.sh** is a web application that provides secure client-side file encryption in your browser. It can also be self-hosted and is useful if you need to encrypt a file but cannot install any software on your device due to organizational policies.
    
    [:octicons-globe-16: 웹사이트](https://hat.sh){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://hat.sh/about/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://hat.sh/about/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/sh-dv/hat.sh){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://github.com/sh-dv/hat.sh#donations){ .card-link title="기부 방법은 홈페이지 하단에서 확인하실 수 있습니다" }

## 커맨드라인

커맨드라인 인터페이스가 존재하는 툴은 [Shell 스크립트](https://ko.wikipedia.org/wiki/%EC%85%B8_%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8)에 통합하는 용도로 유용합니다.

### Kryptor

!!! recommendation

    ![Kryptor 로고](assets/img/encryption-software/kryptor.png){ align=right }
    
    **Kryptor**는 현대적이고 안전한 암호화 알고리즘을 사용하는 무료 오픈 소스 툴로, 파일 암호화 및 서명 기능을 제공합니다. [age](https://github.com/FiloSottile/age)와 [Minisign](https://jedisct1.github.io/minisign/)을 개선하여 GPG를 대체할 수 있는 쉽고 간편한 대안을 제공하는 것을 목표로 합니다.
    
    [:octicons-home-16: 홈페이지](https://www.kryptor.co.uk){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.kryptor.co.uk/features#privacy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://www.kryptor.co.uk/tutorial){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://www.kryptor.co.uk/#donate){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-windows11: Windows](https://www.kryptor.co.uk)
        - [:simple-apple: macOS](https://www.kryptor.co.uk)
        - [:simple-linux: Linux](https://www.kryptor.co.uk)

### Tomb

!!! recommendation

    ![Tomb 로고](assets/img/encryption-software/tomb.png){ align=right }
    
    **Tomb**는 LUKS의 커맨드라인 Shell 래퍼(Wrapper)입니다. [외부 툴](https://github.com/dyne/Tomb#how-does-it-work)을 통해 스테가노그래피(Steganography)를 지원합니다.
    
    [:octicons-home-16: 홈페이지](https://www.dyne.org/software/tomb){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://www.dyne.org/donate){ .card-link title=기부 }

## OpenPGP

OpenPGP is sometimes needed for specific tasks such as digitally signing and encrypting email. PGP has many features and is [complex](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html) as it has been around a long time. For tasks such as signing or encrypting files, we suggest the above options.

When encrypting with PGP, you have the option to configure different options in your `gpg.conf` file. We recommend staying with the standard options specified in the [GnuPG user FAQ](https://www.gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

!!! tip "Use future defaults when generating a key"

    When [generating keys](https://www.gnupg.org/gph/en/manual/c14.html) we suggest using the `future-default` command as this will instruct GnuPG use modern cryptography such as [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) and [Ed25519](https://ed25519.cr.yp.to/):

    ```bash
    gpg --quick-gen-key alice@example.com future-default
    ```

### GNU Privacy Guard

!!! recommendation

    ![GNU Privacy Guard logo](assets/img/encryption-software/gnupg.svg){ align=right }
    
    **GnuPG** is a GPL-licensed alternative to the PGP suite of cryptographic software. GnuPG is compliant with [RFC 4880](https://tools.ietf.org/html/rfc4880), which is the current IETF specification of OpenPGP. The GnuPG project has been working on an [updated draft](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh/) in an attempt to modernize OpenPGP. GnuPG is a part of the Free Software Foundation's GNU software project and has received major [funding](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) from the German government.
    
    [:octicons-home-16: 홈페이지](https://gnupg.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title=문서}
    [:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
        - [:simple-windows11: Windows](https://gpg4win.org/download.html)
        - [:simple-apple: macOS](https://gpgtools.org)
        - [:simple-linux: Linux](https://gnupg.org/download/index.html#binary)

### GPG4win

!!! recommendation

    ![GPG4win logo](assets/img/encryption-software/gpg4win.svg){ align=right }
    
    **GPG4win** is a package for Windows from [Intevation and g10 Code](https://gpg4win.org/impressum.html). It includes [various tools](https://gpg4win.org/about.html) that can assist you in using GPG on Microsoft Windows. The project was initiated and originally [funded by](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography) Germany's Federal Office for Information Security (BSI) in 2005.
    
    [:octicons-home-16: 홈페이지](https://gpg4win.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title=문서}
    [:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-windows11: Windows](https://gpg4win.org/download.html)

### GPG Suite

!!! note

    We suggest [Canary Mail](email-clients.md#canary-mail) for using PGP with email on iOS devices.

!!! recommendation

    ![GPG Suite logo](assets/img/encryption-software/gpgsuite.png){ align=right }
    
    **GPG Suite** provides OpenPGP support for [Apple Mail](email-clients.md#apple-mail) and macOS.
    
    We recommend taking a look at their [First steps](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email) and [Knowledge base](https://gpgtools.tenderapp.com/kb) for support.
    
    [:octicons-home-16: 홈페이지](https://gpgtools.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/GPGTools){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-apple: macOS](https://gpgtools.org)

### OpenKeychain

!!! recommendation

    ![OpenKeychain logo](assets/img/encryption-software/openkeychain.svg){ align=right }
    
    **OpenKeychain** is an Android implementation of GnuPG. It's commonly required by mail clients such as [K-9 Mail](email-clients.md#k-9-mail) and [FairEmail](email-clients.md#fairemail) and other Android apps to provide encryption support. Cure53 completed a [security audit](https://www.openkeychain.org/openkeychain-3-6) of OpenKeychain 3.6 in October 2015. Technical details about the audit and OpenKeychain's solutions can be found [here](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).
    
    [:octicons-home-16: 홈페이지](https://www.openkeychain.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.openkeychain.org/help/privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://www.openkeychain.org/faq/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

!!! example "이 단락은 최근에 만들어졌습니다"

    Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

### 최소 요구 사항

- Cross-platform encryption apps must be open-source.
- File encryption apps must support decryption on Linux, macOS, and Windows.
- External disk encryption apps must support decryption on Linux, macOS, and Windows.
- Internal (OS) disk encryption apps must be cross-platform or built in to the operating system natively.

### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- Operating System (FDE) encryption apps should utilize hardware security such as a TPM or Secure Enclave.
- File encryption apps should have first- or third-party support for mobile platforms.
