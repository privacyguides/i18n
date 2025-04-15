---
meta_title: "Recommended Encryption Software: VeraCrypt, Cryptomator, PicoCrypt, and OpenPGP - Privacy Guides"
title: "Encryption Software"
icon: material/file-lock
description: Encryption of data is the only way to control who can access it. These tools allow you to encrypt your emails and any other files.
cover: encryption.webp
---

**Encryption** is the only secure way to control who can access your data. If you are currently not using encryption software for your hard disk, emails, or files, you should pick an option here.

## Multi-platform

The options listed here are available on multiple platforms and great for creating encrypted backups of your data.

### Cryptomator (Cloud)

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-bug-outline: Pasif Saldırılar](basics/common-threats.md#security-and-privacy ""){.pg-orange}

<div class="admonition recommendation" markdown>

![Cryptomator logo](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** is an encryption solution designed for privately saving files to any cloud [:material-server-network: Service Provider](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }, eliminating the need to trust that they won't access your files. It allows you to create vaults that are stored on a virtual drive, the contents of which are encrypted and synced with your cloud storage provider.

[:octicons-home-16: Ana Sayfa](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.cryptomator.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/cryptomator){ .card-link title="Source Code" }
[:octicons-heart-16:](https://cryptomator.org/donate){ .card-link title=Contribute }???

<details class="downloads" markdown>
indirmeler

 - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onlyoffice.documents)
 - [:simple-appstore: App Store](https://apps.apple.com/app/id944896972)
 - [:simple-windows11: Windows](https://www.onlyoffice.com/download-desktop.aspx)
 - [:simple-apple: macOS](https://www.onlyoffice.com/download-desktop.aspx)
 - [:simple-linux: Linux](https://www.onlyoffice.com/download-desktop.aspx)
 - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.onlyoffice.desktopeditors)

</details>

</div>

Cryptomator hem dosyaları hem de dosya adlarını şifrelemek için AES-256 şifreleme kullanır. Cryptomator erişim, değişiklik ve oluşturma zaman damgaları gibi meta verileri ya da dosya ve klasörlerin sayısını ve boyutunu şifreleyemez.

Cryptomator tüm masaüstü platformlarında ve iOS'ta "salt okunur" modda ücretsiz olarak kullanılabilir. Cryptomator, iOS ve Android'de tam işlevselliğe sahip [ücretli](https://cryptomator.org/pricing) uygulamalar sunar. Android sürümü [ProxyStore](https://cryptomator.org/coop/proxystore) üzerinden anonim olarak satın alınabilir.

Bazı Cryptomator kriptografik kütüphaneleri Cure53 tarafından [denetlenmiştir](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44). Denetlenen kütüphanelerin kapsamı şunları içerir: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) ve [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). Denetim, iOS için Cryptomator tarafından kullanılan bir kütüphane olan [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift)'i kapsamamıştır.

Cryptomator'ın dokümantasyonu, amaçlanan [güvenlik hedefini](https://docs.cryptomator.org/en/latest/security/security-target), [güvenlik mimarisini](https://docs.cryptomator.org/en/latest/security/architecture) ve kullanım için [en iyi uygulamaları](https://docs.cryptomator.org/en/latest/security/best-practices) daha ayrıntılı olarak açıklamaktadır.

### Picocrypt (Dosya)

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-target-account: Hedefli Saldırılar](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![Picocrypt logosu](assets/img/encryption-software/picocrypt.svg){ align=right }

**Picocrypt** modern şifreleme sağlayan küçük ve basit bir şifreleme aracıdır. Picocrypt, yüksek düzeyde güvenlik sağlamak için güvenli XChaCha20 şifresini ve Argon2id anahtar türetme işlevini kullanır. Şifreleme özellikleri için Go'nun standart x/crypto modüllerini kullanır.

[:octicons-repo-16: Repository](https://github.com/Picocrypt/Picocrypt){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/Picocrypt/Picocrypt){ .card-link title="Documentation" }
[:octicons-heart-16:](https://opencollective.com/picocrypt){ .card-link title="Kaynak Kod" }

<details class="downloads" markdown>
<summary>İndirmeler</summary>
- [:fontawesome-brands-windows: Windows](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-apple: macOS](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-linux: Linux](https://github.com/Picocrypt/Picocrypt/releases)
- [ Web)

</details>

</div>

Picocrypt, Ağustos 2024'te Radically Open Security tarafından [denetlenmiş](https://github.com/Picocrypt/storage/blob/main/Picocrypt.Audit.Report.pdf) ve denetimde bulunan sorunların [çoğu](https://github.com/Picocrypt/Picocrypt/issues/32#issuecomment-2329722740) daha sonra düzeltilmiştir.

### VeraCrypt (Disk)

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-target-account: Hedefli Saldırılar](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![VeraCrypt logosu](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![VeraCrypt logosu](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt**, anında şifreleme için kullanılan, kaynak olarak kullanılabilen ücretsiz bir yardımcı programdır. Bir dosya içinde sanal bir şifreli disk oluşturabilir, bir bölümü şifreleyebilir veya önyükleme öncesi kimlik doğrulaması ile tüm depolama aygıtını şifreleyebilir.

[:octicons-home-16: Homepage](https://veracrypt.fr){ .md-button .md-button--primary }[:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title="Public Instances"}
[:octicons-code-16:](https://veracrypt.fr/code){ .card-link title=Documentation}
[:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title="Source Code" }
[](){ .card-link title=Contribute" }

<details class="downloads" markdown>
<summary>İndirmeler</summary>
- [:fontawesome-brands-windows: Windows](https://veracrypt.fr/en/Downloads.html)
- [:simple-apple: macOS](https://veracrypt.fr/en/Downloads.html)
- [:simple-linux: Linux](https://veracrypt.fr/en/Downloads.html)
- [ Web)

</details>

</div>

VeraCrypt, durdurulan TrueCrypt projesinin bir çatalıdır. Geliştiricilerine göre, güvenlik iyileştirmeleri uygulanmış ve ilk TrueCrypt kod denetiminde ortaya çıkan sorunlar ele alınmıştır.

VeraCrypt ile şifreleme yaparken, farklı [hash fonksiyonları](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme) arasından seçim yapma seçeneğiniz vardır. **Yalnızca** [SHA-512](https://en.wikipedia.org/wiki/SHA-512) 'yi seçmenizi ve [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) blok şifresine bağlı kalmanızı öneririz.

TrueCrypt [birçok kez denetlenmiştir](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits) ve VeraCrypt de [ayrıca denetlenmiştir](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit).

## İşletim Sistemi Şifreleme

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-target-account: Hedefli Saldırılar](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Yerleşik işletim sistemi şifreleme çözümleri genellikle [güvenli](basics/hardware.md#tpmsecure-cryptoprocessor) bir [kripto işlemci](basics/hardware.md#tpmsecure-cryptoprocessor) gibi donanım güvenliği özelliklerinden yararlanır. Bu nedenle, işletim sisteminiz için yerleşik şifreleme çözümlerini kullanmanızı öneririz. Platformlar arası şifreleme için, daha fazla esneklik sağlamak ve satıcı kilitlenmesini önlemek için yine de platformlar [arası araçları](#multi-platform) öneriyoruz.

### BitLocker

<div class="admonition recommendation" markdown>

![BitLocker logosu](assets/img/encryption-software/bitlocker.png){ align=right }

**BitLocker**, donanım tabanlı güvenlik için Güvenilir Platform Modülünü ([TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm)) kullanan Microsoft Windows ile birlikte gelen tam birim şifreleme çözümüdür.

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title="Documentation" }

</details>

</div>

BitLocker, Windows'un Pro, Enterprise ve Education sürümlerinde [resmi olarak desteklenmektedir](https://support.microsoft.com/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838). Aşağıdaki önkoşulları karşılamaları koşuluyla Ev sürümlerinde etkinleştirilebilir.

<details class="example" markdown>
<summary>Windows Home'da BitLocker'ı Etkinleştirme</summary>

Windows'un "Home" sürümlerinde BitLocker'ı etkinleştirmek için [GUID Bölümleme Tablosu](https://en.wikipedia.org/wiki/GUID_Partition_Table) ile biçimlendirilmiş bölümlere ve özel bir TPM (v1.2, 2.0+) modülüne sahip olmanız gerekir. Bu kılavuzu izlemeden önce cihazınızda zaten etkinse [, Bitlocker olmayan "Cihaz şifreleme" işlevini](https://discuss.privacyguides.net/t/enabling-bitlocker-on-the-windows-11-home-edition/13303/5) (kurtarma anahtarınızı Microsoft'un sunucularına gönderdiği için daha düşüktür) devre dışı bırakmanız gerekebilir.

1. Bir komut istemi açın ve aşağıdaki komutla sürücünüzün bölümleme tablosu biçimini kontrol edin. "Bölümleme Stili" altında**"GPT**"nin listelendiğini görmelisiniz:

    ```powershell
    powershell Get-Disk
    ```

2. TPM sürümünüzü kontrol etmek için bu komutu çalıştırın (bir yönetici komut isteminde). `SpecVersion`'ın yanında listelenen `2.0` veya `1.2` 'yi görmelisiniz:

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
<p class="admonition-title">Tip</p>

Backup `BitLocker-Recovery-Key.txt` on your Desktop to a separate storage device. Loss of this recovery code may result in loss of data.

</div>

</details>

### FileVault

<div class="admonition recommendation" markdown>

![FileVault logo](assets/img/encryption-software/filevault.png){ align=right }

**FileVault** is the on-the-fly volume encryption solution built into macOS. FileVault takes advantage of the [hardware security capabilities](os/macos-overview.md#hardware-security) present on an Apple Silicon SoC or T2 Security Chip.

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title="Documentation" }

</details>

</div>

We advise against using your iCloud account for recovery; instead, you should securely store a local recovery key on a separate storage device.

### Linux Unified Key Setup

<div class="admonition recommendation" markdown>

![LUKS logo](assets/img/encryption-software/luks.png){ align=right }

**LUKS** is the default FDE method for Linux. It can be used to encrypt full volumes, partitions, or create encrypted containers.

[:octicons-home-16: Homepage](https://gitlab.com/cryptsetup/cryptsetup/-/blob/main/README.md){ .md-button .md-button--primary }
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

We recommend opening containers and volumes with `udisksctl` as this uses [Polkit](https://en.wikipedia.org/wiki/Polkit). Most file managers, such as those included with popular desktop environments, can unlock encrypted files. Tools like [udiskie](https://github.com/coldfix/udiskie) can run in the system tray and provide a helpful user interface.

```bash
udisksctl loop-setup -f /path-to-file
udisksctl unlock -b /dev/loop0
```

</details>

<div class="admonition note" markdown>
<p class="admonition-title">Remember to back up volume headers</p>

We recommend you always [back up your LUKS headers](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) in case of partial drive failure. This can be done with:

```bash
cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
```

</div>

## Command-line

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-target-account: Hedefli Saldırılar](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Tools with command-line interfaces are useful for integrating [shell scripts](https://en.wikipedia.org/wiki/Shell_script).

### Kryptor

<div class="admonition recommendation" markdown>

![Kryptor logo](assets/img/encryption-software/kryptor.png){ align=right }

**Kryptor** is a free and open-source file encryption and signing tool that makes use of modern and secure cryptographic algorithms. It aims to be a better version of [age](https://github.com/FiloSottile/age) and [Minisign](https://jedisct1.github.io/minisign) to provide a simple, easier alternative to GPG.

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

**Tomb** is a command-line shell wrapper for LUKS. It supports steganography via [third-party tools](https://dyne.org/software/tomb/#advanced-usage).

[:octicons-home-16: Homepage](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Source Code" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title="Contribute" }

</details>

</div>

## OpenPGP

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-target-account: Hedefli Saldırılar](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Pasif Saldırılar](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

OpenPGP is sometimes needed for specific tasks such as digitally signing and encrypting email. PGP has many features and is [complex](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html) as it has been around a long time. For tasks such as signing or encrypting files, we suggest the above options.

When encrypting with PGP, you have the option to configure different options in your `gpg.conf` file. We recommend staying with the standard options specified in the [GnuPG user FAQ](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

<div class="admonition tip" markdown>
<p class="admonition-title">Bir anahtar oluştururken gelecekteki varsayılanları kullanın</p>

Anahtar üretirken](https://gnupg.org/gph/en/manual/c14.html) `future-default` komutunu kullanmanızı öneririz, çünkü bu GnuPG'ye [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) ve [Ed25519](https://ed25519.cr.yp.to) gibi modern kriptografiyi kullanması talimatını verecektir:

``bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU Gizlilik Koruması

<div class="admonition recommendation" markdown>

![GNU Privacy Guard logosu](assets/img/encryption-software/gnupg.svg){ align=right }

**GnuPG** PGP kriptografik yazılım paketine GPL lisanslı bir alternatiftir. GnuPG, OpenPGP'nin mevcut IETF spesifikasyonu olan [RFC 4880](https://tools.ietf.org/html/rfc4880) ile uyumludur. GnuPG projesi OpenPGP'yi modernize etmek amacıyla bir [güncellenmiş taslak](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh) üzerinde çalışmaktadır. GnuPG, Özgür Yazılım Vakfı'nın GNU yazılım projesinin bir parçasıdır ve Alman hükümetinden büyük [fon](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) almıştır.

[:octicons-home-16: Ana Sayfa](https://gnupg.org){ .md-button .md-button--primary }[:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="Source Code" }
[](){ .card-link title=Contribute" }

<details class="downloads" markdown>
<summary>İndirmeler</summary>
- [:simple-googleplay: Windows](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
- [:fontawesome-brands-windows: macOS](https://gpg4win.org/download.html)
- [:simple-apple: Linux](https://gpgtools.org)
- [ Web)

</details>

</div>

### GPG4win

<div class="admonition recommendation" markdown>

![GPG4win logosu](assets/img/encryption-software/gpg4win.svg){ align=right }

**GPG4win** [Intevation ve g10 Code](https://gpg4win.org/impressum.html) tarafından Windows için geliştirilmiş bir pakettir. Microsoft Windows üzerinde GPG kullanmanıza yardımcı olabilecek [çeşitli araçlar](https://gpg4win.org/about.html) içerir. Proje 2005 yılında Almanya'nın Federal Bilgi Güvenliği Ofisi (BSI) tarafından başlatılmış ve başlangıçta [finanse edilmiştir](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography).

[:octicons-home-16: Ana Sayfa](https://gpg4win.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title=Documentation}
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="Source Code" }
[:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title=Contribute }???

<details class="downloads" markdown>
<summary>İndirmeler</summary>

- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)

</details>

</div>

### GPG Paketi

<div class="admonition recommendation" markdown>

![GPG Suite logosu](assets/img/encryption-software/gpgsuite.png){ align=right }

**GPG Suite**, [Apple Mail](email-clients.md#apple-mail-macos) ve macOS üzerindeki diğer e-posta istemcileri için OpenPGP desteği sağlar.

Destek için [İlk adımlar](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email) ve [Bilgi Bankası](https://gpgtools.tenderapp.com/kb) adreslerine göz atmanızı öneririz.

[:octicons-home-16: Ana Sayfa](https://gpgtools.org){ .md-button .md-button--primary }[:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Source Code" }
[](){ .card-link title=Contribute" }

<details class="downloads" markdown>
<summary>İndirmeler</summary>

- [:simple-apple: Flathub](https://gpgtools.org)

</details>

</div>

Şu anda, GPG Suite'in macOS Sonoma ve sonrası için [henüz](https://gpgtools.com/sequoia) kararlı bir sürümü bulunmamaktadır.

### OpenKeychain

<div class="admonition recommendation" markdown>

![OpenKeychain logosu](assets/img/encryption-software/openkeychain.svg){ align=right }

**OpenKeychain** Android için bir GnuPG uygulamasıdır. Genellikle [Thunderbird](email-clients.md#thunderbird), [FairEmail](email-clients.md#fairemail-android) gibi posta istemcileri ve diğer Android uygulamaları tarafından şifreleme desteği sağlamak için gereklidir.

[:octicons-home-16: Ana Sayfa](https://openkeychain.org){ .md-button .md-button--primary }[:octicons-eye-16:](https://openkeychain.org/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://openkeychain.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="Source Code" }
[](){ .card-link title=Contribute" }

<details class="downloads" markdown>
<summary>İndirmeler</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

Cure53, OpenKeychain 3.6'nın [güvenlik denetimini](https://openkeychain.org/openkeychain-3-6) Ekim 2015'te tamamlamıştır. Yayınlanan denetime ve OpenKeychain'in denetimde ortaya konan sorunlara yönelik çözümlerine [buradan](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015) ulaşabilirsiniz.

## Kriter

**Lütfen önerdiğimiz projelerin hiçbirine bağlı olmadığımızı unutmayın.** [standart kriterlerimize](about/criteria.md)ek olarak, objektif tavsiyelerde bulunabilmemiz için bir takım gereklilikler geliştirdik. Bir projeyi kullanmayı seçmeden önce bu listeye aşina olmanızı ve sizin için doğru seçim olduğundan emin olmak için kendi araştırmanızı yapmanızı öneririz.

### Asgari Nitelikler

- Platformlar arası şifreleme uygulamaları açık kaynak kodlu olmalıdır.
- Dosya şifreleme uygulamaları Linux, macOS ve Windows'ta şifre çözmeyi desteklemelidir.
- Harici disk şifreleme uygulamaları Linux, macOS ve Windows'ta şifre çözmeyi desteklemelidir.
- Dahili (OS) disk şifreleme uygulamaları çapraz platformlu olmalı veya işletim sisteminde yerel olarak yerleşik olmalıdır.

### En İyi Durum

En iyi durum kriterlerimiz, bu kategorideki mükemmel bir projede görmek istediklerimizi temsil etmektedir. Önerilerimiz bu işlevlerden herhangi birini veya tamamını içermeyebilir, ancak içerenler bu sayfada diğerlerinden daha üst sıralarda yer alabilir.

- İşletim Sistemi (FDE) şifreleme uygulamaları TPM veya Secure Enclave gibi donanım güvenliği kullanmalıdır.
- Dosya şifreleme uygulamaları mobil platformlar için birinci veya üçüncü taraf desteğine sahip olmalıdır.
