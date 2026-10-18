---
meta_title: "추천 암호화 소프트웨어: 베라크립트, 크립토메이터, OpenPGP - 프라이버시 가이드"
title: "암호화 소프트웨어"
icon: material/file-lock
description: 데이터 암호화는 누가 데이터에 접근할 수 있는지 통제하는 유일한 방법입니다. 이 도구를 사용하면 이메일과 기타 모든 파일을 암호화할 수 있습니다.
cover: encryption.webp
---

**암호화**는 누가 데이터에 접근할 수 있는지 통제하는 유일하게 안전한 방법입니다. 현재 하드 디스크, 이메일, 파일에 암호화 소프트웨어를 사용하고 있지 않다면 여기에서 하나를 골라야 합니다.

## 멀티 플랫폼 { #multi-platform }

여기에 소개된 도구는 여러 플랫폼에서 사용할 수 있으며, 데이터의 암호화된 백업을 만드는 데 매우 적합합니다.

### 크립토메이터(클라우드) { #cryptomator-cloud }

<small>다음 위협으로부터 보호합니다:</small>

- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy ""){.pg-orange}

<div class="admonition recommendation" markdown>

![크립토메이터 로고](assets/img/encryption-software/cryptomator.svg){ align=right }

**크립토메이터**는 어떤 클라우드 [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }에든 파일을 비공개로 저장할 수 있도록 설계된 암호화 솔루션으로, 제공업체가 파일에 접근하지 않을 것이라고 신뢰할 필요를 없애 줍니다. 가상 드라이브에 저장되는 보관함을 만들 수 있으며, 보관함의 내용은 암호화되어 클라우드 스토리지 제공업체와 동기화됩니다.

[:octicons-home-16: 홈페이지](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://docs.cryptomator.org){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/cryptomator){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://cryptomator.org/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=org.cryptomator)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1560822163)
- [:simple-android: 안드로이드](https://cryptomator.org/android)
- [:fontawesome-brands-windows: 윈도우](https://cryptomator.org/downloads)
- [:simple-apple: macOS](https://cryptomator.org/downloads)
- [:simple-linux: 리눅스](https://cryptomator.org/downloads)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.cryptomator.Cryptomator)

</details>

</div>

크립토메이터는 AES-256 암호화를 사용하여 파일과 파일 이름을 모두 암호화합니다. 크립토메이터는 접근, 수정, 생성 타임스탬프 같은 메타데이터나 파일 및 폴더의 개수와 크기는 암호화할 수 없습니다.

크립토메이터는 모든 데스크톱 플랫폼과 iOS의 "읽기 전용" 모드에서 무료로 사용할 수 있습니다. 크립토메이터는 iOS와 안드로이드에서 모든 기능을 갖춘 [유료](https://cryptomator.org/pricing) 앱을 제공합니다. 안드로이드 버전은 [프록시스토어](https://cryptomator.org/coop/proxystore)를 통해 익명으로 구매할 수 있습니다.

일부 크립토메이터 암호화 라이브러리는 Cure53의 [감사](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44)를 받았습니다. 감사 대상 라이브러리는 [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode), [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor)입니다. iOS용 크립토메이터에서 사용하는 라이브러리인 [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift)는 감사 대상에 포함되지 않았습니다.

크립토메이터 문서에는 의도된 [보안 목표](https://docs.cryptomator.org/en/latest/security/security-target), [보안 아키텍처](https://docs.cryptomator.org/en/latest/security/architecture), 사용 시 [모범 사례](https://docs.cryptomator.org/en/latest/security/best-practices)가 더 자세히 설명되어 있습니다.

### 베라크립트(디스크) { #veracrypt-disk }

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![베라크립트 로고](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![베라크립트 로고](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**베라크립트**는 실시간 암호화에 사용되는 소스 공개 프리웨어 유틸리티입니다. 파일 안에 가상 암호화 디스크를 만들거나, 파티션을 암호화하거나, 부팅 전 인증으로 저장 장치 전체를 암호화할 수 있습니다.

[:octicons-home-16: 홈페이지](https://veracrypt.fr){ .md-button .md-button--primary }
[:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title="문서" }
[:octicons-code-16:](https://veracrypt.fr/code){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://veracrypt.fr/en/Downloads.html)
- [:simple-apple: macOS](https://veracrypt.fr/en/Downloads.html)
- [:simple-linux: 리눅스](https://veracrypt.fr/en/Downloads.html)

</details>

</div>

베라크립트는 중단된 트루크립트 프로젝트의 포크입니다. 개발자에 따르면 보안이 개선되었으며, 초기 트루크립트 코드 감사에서 제기된 문제도 해결되었습니다.

베라크립트로 암호화할 때는 다양한 [해시 함수](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme) 중에서 선택할 수 있습니다. [SHA-512](https://en.wikipedia.org/wiki/SHA-512)**만** 선택하고 [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) 블록 암호를 사용할 것을 권장합니다.

트루크립트는 [여러 차례 감사](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits)를 받았으며, 베라크립트도 [별도로 감사](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit)를 받았습니다.

## 운영 체제 암호화 { #operating-system-encryption }

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

OS에 내장된 암호화 솔루션은 일반적으로 [보안 암호 프로세서](basics/hardware.md#tpmsecure-cryptoprocessor) 같은 하드웨어 보안 기능을 활용합니다. 따라서 운영 체제에 내장된 암호화 솔루션을 사용할 것을 권장합니다. 크로스 플랫폼 암호화에는 유연성을 높이고 공급업체 종속을 피하기 위해 여전히 [크로스 플랫폼 도구](#multi-platform)를 권장합니다.

<details class="warning" markdown>

<summary>사용하지 않을 때는 기기를 종료하세요.</summary>

사용하지 않을 때 기기의 전원을 끄면 메모리에 암호화 키가 남지 않으므로 FDE 방식의 공격 표면이 최소화되어 가장 높은 수준의 보안을 제공합니다.

</details>

### 비트로커 { #bitlocker }

<div class="admonition recommendation" markdown>

![비트로커 로고](assets/img/encryption-software/bitlocker.png){ align=right }

**비트로커**는 마이크로소프트 윈도우에 포함된 전체 볼륨 암호화 솔루션으로, 하드웨어 기반 보안을 위해 신뢰 플랫폼 모듈([TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm))을 사용합니다.

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title="문서" }

</details>

</div>

비트로커는 윈도우 프로, 엔터프라이즈, 에듀케이션 에디션에서 [공식 지원](https://support.microsoft.com/en-us/windows/bitlocker-overview-44c0c61c-989d-4a69-8822-b95cd49b1bbf)됩니다. 홈 에디션은 자동 [장치 암호화](https://support.microsoft.com/en-us/windows/device-encryption-in-windows-cf7e2b6f-3e70-4882-9532-18633605b7df)만 지원하며, 특정 하드웨어 요구 사항을 충족해야 합니다. 홈 에디션을 사용하고 있다면 [프로로 업그레이드](https://support.microsoft.com/en-us/windows/upgrade-windows-home-to-windows-pro-ef34d520-e73f-3198-c525-d1a218cc2818)할 것을 권장하며, 윈도우를 다시 설치하거나 파일을 잃지 않고도 업그레이드할 수 있습니다.

프로 이상의 에디션은 더 안전한 부팅 전 [TPM+PIN](https://learn.microsoft.com/en-us/windows/security/operating-system-security/data-protection/bitlocker/faq#what-is-the-difference-between-a-tpm-owner-password--recovery-password--recovery-key--pin--enhanced-pin--and-startup-key) 기능도 지원하며, 이는 해당 [그룹 정책](os/windows/group-policies.md#bitlocker-drive-encryption) 설정으로 구성합니다. PIN은 입력 횟수가 제한되며, 누군가 무차별 대입으로 접근을 시도하면 TPM이 패닉 상태가 되어 암호화 키에 대한 접근을 영구적으로 또는 일정 시간 동안 차단합니다.

</details>

### FileVault

<div class="admonition recommendation" markdown>

![FileVault 로고](assets/img/encryption-software/filevault.png){ align=right }

**FileVault**는 macOS에 내장된 실시간 볼륨 암호화 솔루션입니다. FileVault는 애플 실리콘 SoC나 T2 보안 칩에 있는 [하드웨어 보안 기능](os/macos-overview.md#hardware-security)을 활용합니다.

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title="문서" }

</details>

</div>

복구에 아이클라우드 계정을 사용하는 것은 권장하지 않으며, 대신 별도의 저장 장치에 로컬 복구 키를 안전하게 보관해야 합니다.

### 리눅스 통합 키 설정 { #linux-unified-key-setup }

<div class="admonition recommendation" markdown>

![LUKS 로고](assets/img/encryption-software/luks.png){ align=right }

**LUKS**는 리눅스의 기본 FDE 방식입니다. 전체 볼륨이나 파티션을 암호화하거나 암호화된 컨테이너를 만드는 데 사용할 수 있습니다.

[:octicons-repo-16: 저장소](https://gitlab.com/cryptsetup/cryptsetup#what-the-){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title="문서" }
[:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup){ .card-link title="소스 코드" }

</details>

</div>

<details class="example" markdown>
<summary>암호화된 컨테이너 만들고 열기</summary>

```bash
dd if=/dev/urandom of=/path-to-file bs=1M count=1024 status=progress
sudo cryptsetup luksFormat /path-to-file
```

#### 암호화된 컨테이너 열기 { #opening-encrypted-containers }

[Polkit](https://en.wikipedia.org/wiki/Polkit)을 사용하는 `udisksctl`로 컨테이너와 볼륨을 여는 것을 권장합니다. 널리 쓰이는 데스크톱 환경에 포함된 파일 관리자 등 대부분의 파일 관리자는 암호화된 파일의 잠금을 해제할 수 있습니다. [udiskie](https://github.com/coldfix/udiskie) 같은 도구는 시스템 트레이에서 실행되어 유용한 사용자 인터페이스를 제공합니다.

```bash
udisksctl loop-setup -f /path-to-file
udisksctl unlock -b /dev/loop0
```

</details>

<div class="admonition note" markdown>
<p class="admonition-title">볼륨 헤더를 백업해 두세요</p>

드라이브 일부가 고장 날 경우에 대비해 항상 [LUKS 헤더를 백업](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore)해 둘 것을 권장합니다. 다음 명령으로 백업할 수 있습니다:

```bash
cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
```

</div>

## 명령줄 { #command-line }

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

명령줄 인터페이스를 갖춘 도구는 [셸 스크립트](https://en.wikipedia.org/wiki/Shell_script)에 통합하는 데 유용합니다.

### 크립터 { #kryptor }

<div class="admonition recommendation" markdown>

![크립터 로고](assets/img/encryption-software/kryptor.png){ align=right }

**크립터**는 현대적이고 안전한 암호화 알고리즘을 사용하는 자유 오픈 소스 파일 암호화 및 서명 도구입니다. [age](https://github.com/FiloSottile/age)와 [미니사인](https://jedisct1.github.io/minisign)을 개선한 버전을 목표로 하며, GPG를 대체할 수 있는 간단하고 더 쉬운 도구를 제공합니다.

[:octicons-home-16: 홈페이지](https://kryptor.co.uk){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kryptor.co.uk/features#privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://kryptor.co.uk/tutorial){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://kryptor.co.uk/#donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://kryptor.co.uk)
- [:simple-apple: macOS](https://kryptor.co.uk)
- [:simple-linux: 리눅스](https://kryptor.co.uk)

</details>

</div>

### 툼 { #tomb }

<div class="admonition recommendation" markdown>

![툼 로고](assets/img/encryption-software/tomb.png){ align=right }

**툼**은 LUKS용 명령줄 셸 래퍼입니다. [서드파티 도구](https://dyne.org/software/tomb/#advanced-usage)를 통해 스테가노그래피를 지원합니다.

[:octicons-home-16: 홈페이지](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title="후원하기" }

</details>

</div>

## OpenPGP

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

OpenPGP는 이메일에 디지털 서명을 하고 암호화하는 것과 같은 특정 작업에 필요할 때가 있습니다. PGP는 오랫동안 사용되어 왔기 때문에 기능이 많고 [복잡](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html)합니다. 파일 서명이나 암호화 같은 작업에는 위의 선택지를 추천합니다.

PGP로 암호화할 때는 `gpg.conf` 파일에서 다양한 옵션을 구성할 수 있습니다. [GnuPG 사용자 FAQ](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf)에 명시된 표준 옵션을 유지할 것을 권장합니다.

<div class="admonition tip" markdown>
<p class="admonition-title">키를 생성할 때 향후 기본값(future-default) 사용하기</p>

[키를 생성](https://gnupg.org/gph/en/manual/c14.html)할 때는 `future-default` 명령을 사용할 것을 권장합니다. 이 명령은 GnuPG가 [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History)와 [Ed25519](https://ed25519.cr.yp.to) 같은 최신 암호 기술을 사용하도록 지시합니다:

```bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU 프라이버시 가드 { #gnu-privacy-guard }

<div class="admonition recommendation" markdown>

![GNU 프라이버시 가드 로고](assets/img/encryption-software/gnupg.svg){ align=right }

**GnuPG**는 GPL 라이선스로 제공되는 PGP 암호화 소프트웨어 제품군의 대안입니다. GnuPG는 현재 OpenPGP의 IETF 사양인 [RFC 4880](https://tools.ietf.org/html/rfc4880)을 준수합니다. GnuPG 프로젝트는 OpenPGP를 현대화하기 위해 [개정 초안](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh) 작업을 진행해 왔습니다. GnuPG는 자유 소프트웨어 재단의 GNU 소프트웨어 프로젝트에 속하며, 독일 정부로부터 상당한 [자금 지원](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html)을 받았습니다.

[:octicons-home-16: 홈페이지](https://gnupg.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title="문서" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
- [:fontawesome-brands-windows: 윈도우](https://gpg4win.org/download.html)
- [:simple-apple: macOS](https://gpgtools.org)
- [:simple-linux: 리눅스](https://gnupg.org/download/index.html#binary)

</details>

</div>

### GPG4win

<div class="admonition recommendation" markdown>

![GPG4win 로고](assets/img/encryption-software/gpg4win.svg){ align=right }

**GPG4win**은 [인테베이션과 g10 Code](https://gpg4win.org/impressum.html)가 만든 윈도우용 패키지입니다. 마이크로소프트 윈도우에서 GPG를 사용하는 데 도움이 되는 [다양한 도구](https://gpg4win.org/about.html)가 포함되어 있습니다. 이 프로젝트는 2005년 독일 연방정보보안청(BSI)이 시작했으며, 처음에는 BSI의 [자금 지원](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography)을 받았습니다.

[:octicons-home-16: 홈페이지](https://gpg4win.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title="문서" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://gpg4win.org/download.html)

</details>

</div>

### GPG 스위트 { #gpg-suite }

<div class="admonition recommendation" markdown>

![GPG 스위트 로고](assets/img/encryption-software/gpgsuite.png){ align=right }

**GPG 스위트**는 macOS의 [애플 메일](email-clients.md#apple-mail-macos) 및 기타 이메일 클라이언트에 OpenPGP 지원을 제공합니다.

지원이 필요하다면 [첫 단계](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email)와 [지식 베이스](https://gpgtools.tenderapp.com/kb)를 살펴볼 것을 권장합니다.

[:octicons-home-16: 홈페이지](https://gpgtools.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/GPGTools){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-apple: macOS](https://gpgtools.org)

</details>

</div>

현재 GPG 스위트는 macOS 소노마 이후 버전용 안정 릴리스가 [아직](https://gpgtools.com/sequoia) 없습니다.

### 오픈키체인 { #openkeychain }

<div class="admonition recommendation" markdown>

![오픈키체인 로고](assets/img/encryption-software/openkeychain.svg){ align=right }

**오픈키체인**은 안드로이드용 GnuPG 구현체입니다. [썬더버드](email-clients.md#thunderbird), [페어이메일](email-clients.md#fairemail-android) 같은 메일 클라이언트와 기타 안드로이드 앱에서 암호화 지원을 위해 흔히 필요합니다.

[:octicons-home-16: 홈페이지](https://openkeychain.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://openkeychain.org/help/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://openkeychain.org/faq){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

Cure53은 2015년 10월 오픈키체인 3.6에 대한 [보안 감사](https://openkeychain.org/openkeychain-3-6)를 완료했습니다. 공개된 감사 보고서와 감사에서 제기된 문제에 대한 오픈키체인의 해결책은 [여기](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015)에서 확인할 수 있습니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

### 최소 요구 사항 { #minimum-qualifications }

- 크로스 플랫폼 암호화 앱은 오픈 소스여야 합니다.
- 파일 암호화 앱은 리눅스, macOS, 윈도우에서 복호화를 지원해야 합니다.
- 외장 디스크 암호화 앱은 리눅스, macOS, 윈도우에서 복호화를 지원해야 합니다.
- 내장(OS) 디스크 암호화 앱은 크로스 플랫폼이거나 운영 체제에 기본으로 내장되어 있어야 합니다.

### 우대 사항 { #best-case }

우대 사항은 이 카테고리에서 완벽한 프로젝트라면 갖추었으면 하는 사항을 나타냅니다. 추천 항목에 이 기능 중 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- 운영 체제(FDE) 암호화 앱은 TPM이나 Secure Enclave 같은 하드웨어 보안을 활용하는 것이 좋습니다.
- 파일 암호화 앱은 모바일 플랫폼에 대한 자체 또는 서드파티 지원이 있는 것이 좋습니다.
