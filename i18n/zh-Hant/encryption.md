---
meta_title: "推薦的加密軟體： VeraCrypt, Cryptomat, PicoCrypt 和 OpenPGP - Privacy Guides"
title: "加密軟體"
icon: material/file-lock
description: 數據加密是控制誰可以訪問它的唯一方法。 這些工具允許您加密電子郵件和任何其他檔案。
cover: encryption.webp
---

**加密** 是控制誰能存取您資料的唯一安全方法。 如果您目前沒有為您的硬碟，電子郵件或檔案使用加密軟體，您應該在這裡選擇一個選項。

## 多平臺

這裡列出的選項可在多種平台上使用，非常適合為您的資料建立加密備份。

### Cryptomator（雲端）

<small>防護下列威脅：</small>

- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy ""){.pg-orange}

<div class="admonition recommendation" markdown>

![Cryptomator logo](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** 是一種加密方案，專為私密的將檔案儲存至任何雲端 [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers){ .pg-teal } 而設計，讓您無需相信他們不會存取您的檔案。 它允許您創建儲存在虛擬驅動器上的保管庫，其內容已加密並與雲端儲存供應商同步。

[:octicons-home-16: 首頁](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.cryptomator.org){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/cryptomator){ .card-link title="原始碼" }
[:octicons-heart-16:](https://cryptomator.org/donate){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.cryptomator)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1560822163)
- [:simple-android: Android](https://cryptomator.org/android)
- [:fontawesome-brands-windows: Windows](https://cryptomator.org/downloads)
- [:simple-apple: macOS](https://cryptomator.org/downloads)
- [:simple-linux: Linux](https://cryptomator.org/downloads)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.cryptomator.Cryptomator)

</details>

</div>

Cryptomator 使用 AES-256 加密來加密檔案和檔案名稱。 Cryptomator 無法加密中繼資料，例如存取、修改和創建時間戳記，也無法加密檔案和資料夾的數量和大小。

Cryptomator is free to use on all desktop platforms, as well as on iOS in "read only" mode. Cryptomator offers [paid](https://cryptomator.org/pricing) apps with full functionality on iOS and Android. The Android version can be purchased anonymously via [ProxyStore](https://cryptomator.org/coop/proxystore).

一些 Cryptomator 加密程式庫 [已被Cure53審核](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) 。 稽核程式庫的範圍包括： [cryptolib](https://github.com/cryptomator/cryptolib)、 [cryptofs](https://github.com/cryptomator/cryptofs)、 [siv-mode](https://github.com/cryptomator/siv-mode) 和 [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor)。 審計並未包含[cryptolib-swift](https://github.com/cryptomator/cryptolib-swift)它是 Cryptomator 運用在 iOS 程式庫。

Cryptomator 的文件詳細介紹它的預期[安全目標](https://docs.cryptomator.org/en/latest/security/security-target)，[安全架構](https:/ /docs.cryptomator.org/en/latest/security/architecture)和[最佳實踐](https://docs.cryptomator.org/en/latest/security/best-practices) 以供更詳細的使用。

### Picocrypt (檔案)

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![Picocrypt logo](assets/img/encryption-software/picocrypt.svg){ align=right }

**Picocrypt** 是一個小而簡單的加密工具，提供現代加密。 Picocrypt 使用安全的 XChaCha20 密碼和 Argon2id 金鑰派生功能來提供高級別的安全性。 它使用 Go 標準x/crypto 模塊作為其加密功能。

[:octicons-repo-16: 儲存庫](https://github.com/Picocrypt/Picocrypt){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/Picocrypt/Picocrypt){ .card-link title="原始碼" }
[:octicons-heart-16:](https://opencollective.com/picocrypt){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-apple: macOS](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-linux: Linux](https://github.com/Picocrypt/Picocrypt/releases)

</details>

</div>

Picocrypt 已於 2024 年 8 月接受 Radically Open Security 的[審核](https://github.com/Picocrypt/storage/blob/main/Picocrypt.Audit.Report.pdf)，審核中發現的[大部分](https://github.com/Picocrypt/Picocrypt/issues/32#issuecomment-2329722740)問題隨後都已修正。

### VeraCrypt（磁碟）

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![VeraCrypt logo](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![VeraCrypt logo](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt** 是一個開源的免費軟體實用程式，用於即時加密。 它可以在檔案中建立虛擬加密磁碟、加密分割區，或透過預先啟動驗證來加密整個儲存裝置。

[:octicons-home-16: 首頁](https://veracrypt.fr){ .md-button .md-button--primary }
[:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title="說明文件" }
[:octicons-code-16:](https://veracrypt.fr/code){ .card-link title="原始碼" }
[:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://veracrypt.fr/en/Downloads.html)
- [:simple-apple: macOS](https://veracrypt.fr/en/Downloads.html)
- [:simple-linux: Linux](https://veracrypt.fr/en/Downloads.html)

</details>

</div>

VeraCrypt是已停產的 TrueCrypt 項目的分支。 根據其開發人員的說法，已經實施了安全性改進，並解決了最初的TrueCrypt 代碼審計提出的問題。

使用 VeraCrypt 加密時，您可以選擇不同的 [雜湊函式](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme)。 我們建議您**只**選擇 [SHA-512](https://en.wikipedia.org/wiki/SHA-512)，並堅持使用 [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) 區塊加密法。

Truecrypt 已完成[多次審計](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits)，而 VeraCrypt 也曾接受 [獨立審計](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit)。

## 作業系統加密

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

作業系統內建的加密方案通常會利用硬體安全功能，例如：[安全加密協處理器](basics/hardware.md#tpmsecure-cryptoprocessor)。 因此，我們建議您使用作業系統內建的加密方案。 對於跨平台加密，我們仍建議使用 [跨平台工具](#multi-platform) ，以獲得額外的靈活性，並避免供應商鎖定。

### BitLocker

<div class="admonition recommendation" markdown>

![BitLocker 標誌](assets/img/encryption-software/bitlocker.png){ align=right }

**BitLocker** 是 Microsoft Windows 綁定的全 卷(volume) 加密方案，使用 信賴平台模組([TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm)) 提供基於硬體的安全性。

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title="說明文件" }

</details>

</div>

Windows 的專業版、企業版和教育版均[正式支援](https://support.microsoft.com/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838) BitLocker。 只要符合下列先決條件，即可在家庭版上啟用。

<details class="example" markdown>
<summary>Windows Home上啓用BitLocker</summary>

若要在 Windows 家用版啟用 BitLocker ，必須使用 [GUID 分割表](https://en.wikipedia.org/wiki/GUID_Partition_Table) 格式化的分割區，並且具有專用的TPM (v1.2, 2.0+)模組。 如果在遵循本指南之前已在裝置上啟用，則要[停用非Bitlocker「裝置加密」功能](https://discuss.privacyguides.net/t/enabling-bitlocker-on-the-windows-11-home-edition/13303/5)](因為它會將您的復原金鑰傳送到Microsoft 的伺服器)。

1. 開啟命令提示符，並使用以下命令檢查磁碟機的分區表格格式。 您應該會在“分區樣式”下方看到“**GPT**” ：

    ```powershell
    powershell Get-Disk
    ```

2. 在管理員命令提示符中執行此命令以檢查您的TPM版本。 您應該會在 `個SpecVersion`旁邊看到 `2.0` 或 `1.2` ：

    ```powershell
    powershell Get-WmiObject -Namespace "root/cimv2/security/microsofttpm" -Class WIN32_tpm
    ```

3. 造訪[進階啟動選項](https://support.microsoft.com/windows/advanced-startup-options-include-safe-mode-b90e7808-80b5-a291-d4b8-1a1af602b617)。 重新啟動時需要在 Windows 啟動前按下F8 鍵，然後進入 *命令提示字元* in **疑難排解** → **進階選項** → **命令提字元**。
4. 使用管理員帳戶登入並在命令提示符中輸入指令以開始加密：

    ```powershell
    manage-bde -on c: -used
    ```

5. 關閉命令提示符並繼續啟動正常Windows。
6. 打開 admin 命令提示符並運行以下命令：

    ```powershell
    manage-bde c: -protectors -add -rp -tpm
    manage-bde -protectors -enable c:
    manage-bde -protectors -get c: > %UserProfile%\Desktop\BitLocker-Recovery-Key.txt
    ```

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

將桌面上的「BitLocker-Recovery-Key.txt」備份到單獨的儲存裝置。 若遺失恢復代碼可能會導致資料無法回復。

</div>

</details>

### FileVault

<div class="admonition recommendation" markdown>

![FileVault logo](assets/img/encryption-software/filevault.png){ align=right }

**FileVault** 是 macOS 內建的即時磁區加密方案。 FileVault 能利用 Apple 晶片 SoC 或 T2 安全晶片上的 [硬體安全功能](os/macos-overview.md#hardware-security)。

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title="說明文件" }

</details>

</div>

我們建議您不要使用 iCloud 帳戶進行復原；相反地，您應該將本機的復原金鑰安全地儲存在獨立的儲存裝置上。

### Linux Unified Key設定

<div class="admonition recommendation" markdown>

![LUKS logo](assets/img/encryption-software/luks.png){ align=right }

**LUKS** 是 Linux 預設 FDE 方法。 它可用於加密整個磁區、分割區或建立加密容器。

[:octicons-home-16: 首頁](https://gitlab.com/cryptsetup/cryptsetup/-/blob/main/README.md){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title="說明文件" }
[:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup){ .card-link title="原始碼" }

</details>

</div>

<details class="example" markdown>
<summary>建立和開啟加密容器</summary>

```bash
dd if=/dev/urandom of=/path-to-file bs=1M count=1024 status=progress
sudo cryptsetup luksFormat /path-to-file
```

#### 開啟加密容器

建議使用 `udisksctl` 打開容器和磁碟區，因為它使用 [Polkit](https://en.wikipedia.org/wiki/Polkit)。 大多數檔案管理器，例如流行的桌面環境中包含的檔案管理器，都可以解鎖加密的檔案。 像 [udiskie](https://github.com/coldfix/udiskie) 這類工具可以在系統工作列運行並提供有用的使用者介面。

```bash
udisksctl loop-setup -f /path-to-file
udisksctl unlock -b /dev/loop0
```

</details>

<div class="admonition note" markdown>
<p class="admonition-title">記得備份磁區標頭</p>

我們建議您務必 [備份您的LUKS標頭](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) 以防部分驅動器故障。 可透過以下指令達成

```bash
cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
```

</div>

## 命令列

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

命令行界面的工具可用於集成 [shell 腳本](https://en.wikipedia.org/wiki/Shell_script)。

### Kryptor

<div class="admonition recommendation" markdown>

![Kryptor logo](assets/img/encryption-software/kryptor.png){ align=right }

**Kryptor** 是一個免費的開源文件加密和簽名工具，利用現代安全的加密算法。 它旨在成為更好版本的 [age](https://github.com/FiloSottile/age)和 [Minisign](https://jedisct1.github.io/minisign/)，提供一個簡單，更容易的 GPG 替代品。

[:octicons-home-16: 首頁](https://kryptor.co.uk){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kryptor.co.uk/features#privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://kryptor.co.uk/tutorial){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="原始碼" }
[:octicons-heart-16:](https://kryptor.co.uk/#donate){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://kryptor.co.uk)
- [:simple-apple: macOS](https://kryptor.co.uk)
- [:simple-linux: Linux](https://kryptor.co.uk)

</details>

</div>

### Tomb

<div class="admonition recommendation" markdown>

![Tomb logo](assets/img/encryption-software/tomb.png){ align=right }

**Tomb** 是 LUKS 的命令行 shell 包裝器。 它通過 [第三方工具](https://dyne.org/software/tomb/#advanced-usage) 支援隱寫。

[:octicons-home-16: 首頁](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="原始碼" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title="捐款" }

</details>

</div>

## OpenPGP

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

OpenPGP 有時需要執行特定任務，例如數位簽署和加密電子郵件。 PGP 有許多功能，但也因此而很 [複雜](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html) ，因為它已經存在很久了。 對於簽署或加密檔案等任務，我們建議您使用上述選項。

使用 PGP 加密時，您可以選擇在 `gpg.conf` 檔案中設定不同的選項。 我們建議您繼續使用 [ GnuPG 用戶常見問題集](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf)中指定的標準選項。

<div class="admonition tip" markdown>
<p class="admonition-title">在生成金鑰時使用未來的預設值</p>

當[產生金鑰](https://gnupg.org/gph/en/manual/c14.html)時，建議使用 `future-default` 指令，它將指示GnuPG 使用現代密碼學，例如 [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) 與 [Ed25519](https://ed25519.cr.yp.to) ：

```bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU Privacy Guard

<div class="admonition recommendation" markdown>

![GNU Privacy Guard logo](assets/img/encryption-software/gnupg.svg){ align=right }

**GnuPG** 是 GPL授權的加密軟體 PGP 替代品。 GnuPG 符合 [RFC 4880](https://tools.ietf.org/html/rfc4880) ，這是目前 OpenPGP 的 IETF 規範。 GnuPG 專案一直致力於 [更新](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh/) ，試圖現代化OpenPGP。 GnuPG 是自由軟體基金會GNU 軟體項目的一部分，並已收到德國政府的重大 [資助](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html)。

[:octicons-home-16: 首頁](https://gnupg.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title="說明文件" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)
- [:simple-apple: macOS](https://gpgtools.org)
- [:simple-linux: Linux](https://gnupg.org/download/index.html#binary)

</details>

</div>

### GPG4win

<div class="admonition recommendation" markdown>

![GPG4win logo](assets/img/encryption-software/gpg4win.svg){ align=right }

**GPG4win** 是 [Intevation and g10 Code](https://gpg4win.org/impressum.html) 的Windows 套件。 它包括 [各種工具](https://gpg4win.org/about.html) ，可協助您在 Microsoft Windows 上使用GPG。 該項目最初由德國聯邦信息安全辦公室（BSI）於2005年發起並 [資助](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography)。

[:octicons-home-16: 首頁](https://gpg4win.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title="說明文件" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="原始碼" }
[:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)

</details>

</div>

### GPG Suite

<div class="admonition note" markdown>
<p class="admonition-title">Note "備註"</p>

建議 [Canary Mail](email-clients.md#canary-mail-ios) 在 iOS 裝置上使用 PGP 和電子郵件。

</div>

<div class="admonition recommendation" markdown>

![GPG Suite logo](assets/img/encryption-software/gpgsuite.png){ align=right }

**GPG Suite** 為 macOS 上的 [Apple Mail](email-clients.md#apple-mail-macos) 和其他電子郵件客戶端提供 OpenPGP 支援。

我們建議看看他們的 [第一步](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email) 和 [知識庫](https://gpgtools.tenderapp.com/kb) 以取得支援。

[:octicons-home-16: 首頁](https://gpgtools.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/GPGTools){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-apple: macOS](https://gpgtools.org)

</details>

</div>

目前，GPG Suite [還沒有](https://gpgtools.com/sequoia) 適用於 macOS Sonoma 及更新版本的穩定版本。

### OpenKeychain

<div class="admonition recommendation" markdown>

![OpenKeychain logo](assets/img/encryption-software/openkeychain.svg){ align=right }

**OpenKeychain** 是 Android 版 GnuPG 的實作。 一般的郵件客戶端如 [Thunderbird](email-clients.md#thunderbird)、[FairEmail](email-clients.md#fairemail-android) 和其他 Android 應用程式都需要它來提供加密支援。

[:octicons-home-16: 首頁](https://openkeychain.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://openkeychain.org/help/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://openkeychain.org/faq){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

Cure53 於 2015 年 10 月完成對 OpenKeychain 3.6 的 [安全審核](https://openkeychain.org/openkeychain-3-6)。 已公布的審核報告以及 OpenKeychain 對於審核報告中所提出問題的解決方案，可以在 [這裡](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015) 找到。

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 跨平臺加密應用程式須為開源。
- 檔案加密應用程式必須支援 Linux、macOS 和 Windows 的解密。
- 外部磁碟加密應用程式必須支援 Linux、macOS 和 Windows 的解密。
- 作業系統內部磁碟加密應用程式必須是跨平臺或原生內建作業系統。

### 最佳情況

最佳情況標準代表我們希望在這個類別的完美項目的應具備的特性。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 作業系統(FDE)加密應用程式應使用硬體安全性，例如 TPM 或Secure Enclave。
- 檔案加密應用程式應有自己的或第三方支援行動平臺。
