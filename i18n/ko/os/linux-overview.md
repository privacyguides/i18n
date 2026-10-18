---
title: 리눅스 개요
icon: simple/linux
description: 리눅스는 오픈 소스이자 프라이버시 중심의 대안 데스크톱 운영 체제이지만, 모든 배포판이 똑같지는 않습니다.
---

**리눅스**는 오픈 소스이자 프라이버시 중심의 대안 데스크톱 운영 체제입니다. 주류 운영 체제의 만연한 원격 측정과 기타 프라이버시 침해 기술에 맞서, 데스크톱 리눅스는 컴퓨터를 처음부터 끝까지 완전히 통제하고 싶은 사람들에게 확실한 선택지로 남아 있습니다.

이 웹사이트에서 "리눅스"라는 용어는 일반적으로 **데스크톱** 리눅스 배포판을 가리킵니다. 크롬OS, 안드로이드, 큐브스 OS처럼 리눅스 커널을 사용하는 다른 운영 체제는 이 페이지에서 다루지 않습니다.

[프라이버시 가이드의 리눅스 추천 :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## 보안 참고 사항 { #security-notes }

리눅스에는 알아 두어야 할 몇 가지 주목할 만한 보안 문제가 있습니다. 이러한 단점에도 불구하고, 데스크톱 리눅스 배포판은 다음을 원하는 대부분의 사람에게 여전히 훌륭한 선택입니다:

- 독점 운영 체제에 흔히 딸려 오는 원격 측정 피하기
- [소프트웨어 자유](https://gnu.org/philosophy/free-sw.en.html#four-freedoms) 유지하기
- [후닉스](../desktop.md#whonix)나 [테일즈](../desktop.md#tails) 같은 프라이버시 중심 시스템 사용하기

### 오픈 소스 보안 { #open-source-security }

리눅스와 기타 오픈 소스 소프트웨어가 단지 소스 코드가 공개되어 있다는 이유만으로 본질적으로 안전하다는 것은 [흔한 오해](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure)입니다. 커뮤니티 검증이 정기적으로 이루어질 것이라는 기대가 있지만, 항상 [그런 것은 아닙니다](https://seirdy.one/posts/2022/02/02/floss-security).

실제로 배포판의 보안은 프로젝트 활동, 개발자 경험, 코드 리뷰의 엄격함, 그리고 수년간 손대지 않았을 수 있는 코드베이스의 특정 부분에 얼마나 자주 관심을 기울이는지 등 여러 요인에 따라 달라집니다.

### 부족한 보안 기능 { #missing-security-features }

현재 데스크톱 리눅스는 특정 보안 기능 면에서 macOS나 안드로이드 같은 대안보다 [뒤처져 있습니다](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9). 향후 이러한 부분이 개선되기를 바랍니다.

- 리눅스의 **자체 검사 부팅**은 애플의 [보안 부팅](https://support.apple.com/guide/security/secac71d5623/web)이나 안드로이드의 [자체 검사 부팅](https://source.android.com/security/verifiedboot) 같은 대안만큼 견고하지 않습니다. 자체 검사 부팅은 멀웨어에 의한 지속적인 변조와 [이블 메이드 공격](https://en.wikipedia.org/wiki/Evil_Maid_attack)을 막아 주지만, 가장 발전된 배포판에서도 여전히 [대부분 사용할 수 없습니다](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- 리눅스에서는 플랫팩 같은 컨테이너화된 앱이나 파이어자일 같은 샌드박싱 솔루션을 사용하더라도 앱에 대한 **강력한 샌드박싱**이 매우 부족합니다. 플랫팩은 지금까지 리눅스에서 가장 유망한 샌드박싱 유틸리티이지만, 여전히 여러 면에서 부족하며 대부분의 앱이 샌드박스를 손쉽게 우회할 수 있는 [안전하지 않은 기본값](https://flatkill.org/2020)을 허용합니다.

또한 리눅스는 윈도우의 임의 코드 가드(Arbitrary Code Guard)나 macOS의 강화된 런타임처럼 다른 운영 체제에서는 이제 표준이 된 [익스플로잇 완화 기법](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations)의 구현에서도 뒤처져 있습니다. 게다가 대부분의 리눅스 프로그램과 리눅스 자체는 메모리 안전하지 않은 언어로 작성되어 있습니다. 메모리 손상 버그는 수정되어 CVE가 할당된 [취약점의 대부분](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code)을 차지합니다. 이는 윈도우와 macOS도 마찬가지이지만, 이들은 각각 러스트와 스위프트 같은 메모리 안전 언어를 빠르게 도입하고 있습니다.

## 배포판 선택하기 { #choosing-your-distribution }

모든 리눅스 배포판이 똑같지는 않습니다. 프라이버시 가이드의 [리눅스 추천 페이지](../desktop.md)가 어떤 배포판을 사용해야 하는지에 대한 권위 있는 출처를 의도한 것은 아니지만, 추천 항목은 다음 지침을 따르고 *있습니다*. 배포판을 선택할 때 염두에 두어야 할 몇 가지 사항은 다음과 같습니다:

### 릴리스 주기 { #release-cycle }

안정적인 업스트림 소프트웨어 릴리스에 가깝게 유지되는 배포판, 흔히 롤링 릴리스 배포판이라고 하는 배포판을 선택할 것을 강력히 권장합니다. 릴리스 주기가 고정된 배포판은 패키지 버전을 업데이트하지 않아 보안 업데이트가 뒤처지는 경우가 많기 때문입니다.

[데비안](https://debian.org/security/faq#handling)처럼 릴리스가 고정된 배포판에서는 패키지 관리자가 업스트림 개발자가 출시한 "다음 버전"으로 소프트웨어를 올리는 대신, 취약점을 수정하는 패치를 백포트할 것으로 기대됩니다. 일부 보안 수정 사항(특히 덜 알려진 소프트웨어의 경우)은 [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)를 아예 [받지 못하므로](https://arxiv.org/abs/2105.14565), 이러한 패치 모델에서는 배포판에 반영되지 않습니다. 그 결과 사소한 보안 수정 사항이 다음 주요 릴리스까지 보류되는 경우가 있습니다.

패키지를 보류하고 임시 패치를 적용하는 것은 개발자가 의도한 소프트웨어 작동 방식에서 벗어나므로 좋은 생각이 아니라고 봅니다. [리처드 브라운](https://rootco.de/aboutme)이 이에 관해 발표한 자료가 있습니다:

- [정기 릴리스는 틀렸다, 살고 싶다면 롤링하라](https://youtu.be/i8c0mg_mS7U) <small>(유튜브)</small>

### 기존 업데이트 vs 원자적 업데이트 { #traditional-vs-atomic-updates }

기존에는 리눅스 배포판이 원하는 패키지를 순차적으로 업데이트하는 방식으로 업데이트되었습니다. 페도라, 아치 리눅스, 데비안 기반 배포판에서 사용하는 것과 같은 기존 업데이트 방식은 업데이트 중에 오류가 발생하면 안정성이 떨어질 수 있습니다.

반면 원자적 업데이트를 사용하는 배포판은 업데이트를 완전히 적용하거나 아예 적용하지 않습니다. 원자적 배포판에서는 업데이트 중에 (정전 등으로) 오류가 발생하면 시스템에 아무것도 변경되지 않습니다.

원자적 업데이트 방식은 이 모델을 통해 안정성을 확보할 수 있으며, 실버블루와 닉스OS 같은 [배포판](../desktop.md#atomic-distributions)에서 사용됩니다. [아담 샤말리크](https://twitter.com/adsamalik)가 `rpm-ostree`가 실버블루에서 어떻게 작동하는지에 대해 발표했습니다:

- [페도라 실버블루를 사용해 보자 — 불변 데스크톱 OS! - 아담 샤말리크](https://youtu.be/-hpV5l-gJnQ) <small>(유튜브)</small>

### "보안 중심" 배포판 { #security-focused-distributions }

"보안 중심" 배포판과 "침투 테스트" 배포판을 혼동하는 경우가 많습니다. "가장 안전한 리눅스 배포판"을 간단히 검색하면 칼리 리눅스, 블랙아치, 패럿 OS 같은 결과가 나오는 경우가 많습니다. 이러한 배포판은 다른 시스템을 테스트하는 도구를 묶어 놓은 공격용 침투 테스트 배포판입니다. 일상적인 사용을 위한 "추가 보안"이나 방어적 완화 기능은 포함되어 있지 않습니다.

### 아치 기반 배포판 { #arch-based-distributions }

아치 및 아치 기반 배포판은 정기적인 [시스템 유지 관리](https://wiki.archlinux.org/title/System_maintenance)가 필요하므로 (배포판에 관계없이) 리눅스 입문자에게는 권장하지 않습니다. 아치에는 기반 소프트웨어 선택을 위한 배포판 업데이트 메커니즘이 없습니다. 따라서 최신 동향을 계속 파악하고, 새로운 기술이 기존 방식을 대체할 때 직접 도입해야 합니다.

안전한 시스템을 위해서는 [강제적 접근 제어](#mandatory-access-control) 시스템 도입, [커널 모듈](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) 블랙리스트 설정, 부팅 매개변수 강화, [sysctl](https://en.wikipedia.org/wiki/Sysctl) 매개변수 조작, [Polkit](https://en.wikipedia.org/wiki/Polkit) 같은 필요한 구성 요소 파악 등 시스템의 보안을 제대로 설정할 수 있는 충분한 리눅스 지식도 갖추고 있어야 합니다.

아치를 "더 쉽게 사용"할 수 있도록 설계된 아치 기반 파생 배포판은 기본 시스템을 약화시키면서 잘못된 보안 관행을 부추기는 경우가 많으므로 권장하지 않습니다. 이러한 관행에는 아치 공식 채널보다 업데이트가 덜 자주 이루어지는 다운스트림 저장소에 오래된 패키지를 포함하는 것 등이 있습니다. 게다가 이러한 배포판은 대개 아치 사용자 저장소(AUR)와 관련된 위험을 사용자에게 제대로 알려 주지 않습니다.

[아치 사용자 저장소(AUR)](https://wiki.archlinux.org/title/Arch_User_Repository)를 사용하는 사람이라면 누구나 해당 서비스에서 다운로드하는 PKGBUILD(패키지를 빌드하는 레시피)를 **반드시** 직접 검토할 수 있어야 합니다. AUR 패키지는 커뮤니티가 만든 콘텐츠로 어떤 식으로도 검증되지 않으므로 소프트웨어 [:material-package-variant-closed-remove: 공급망 공격](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}에 취약하며, 실제로 [과거에](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository) 이런 공격이 있었고 최근에는 [1500개의 패키지](https://discuss.privacyguides.net/t/around-1-500-aur-packages-compromised-with-rootkit-like-malware/38517)가 침해되기도 했습니다.

AUR은 항상 최소한으로만 사용해야 하며, 여러 페이지에서 충분한 경고 없이 [AUR 헬퍼](https://wiki.archlinux.org/title/AUR_helpers)를 무작정 사용하라는 잘못된 조언이 많습니다. 데비안 기반 배포판의 서드파티 개인 패키지 저장소(PPA)나 페도라의 커뮤니티 프로젝트(COPR)를 사용할 때에도 비슷한 경고가 적용됩니다.

리눅스 경험이 있고 아치 기반 배포판을 사용하고 싶다면, 메인라인 아치 리눅스가 **유일하게** 권장되는 선택지입니다.

### 리눅스-리브레 커널과 "자유(Libre)" 배포판 { #linux-libre-kernel-and-libre-distributions }

리눅스-리브레 커널은 [보안 완화 기능을 제거](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released)하고 취약한 마이크로코드에 대한 [커널 경고를 억제](https://news.ycombinator.com/item?id=29674846)하므로 사용하지 **않을** 것을 권장합니다.

### 강제적 접근 제어 { #mandatory-access-control }

강제적 접근 제어는 앱이나 시스템 서비스 같은 시스템의 일부를 가두는 데 도움이 되는 추가 보안 제어 기능입니다. 리눅스 배포판에서 흔히 볼 수 있는 두 가지 강제적 접근 제어 형태는 [SELinux](https://github.com/SELinuxProject)와 [앱아머](https://apparmor.net)입니다. 페도라와 텀블위드는 기본적으로 SELinux를 사용하며, 텀블위드는 설치 프로그램에서 대신 앱아머를 선택할 수 있는 옵션을 제공합니다.

[페도라](https://docs.fedoraproject.org/en-US/quick-docs/selinux-getting-started)의 SELinux는 기본적으로 리눅스 컨테이너, 가상 머신, 서비스 데몬을 가둡니다. 앱아머는 snap 데몬이 [파이어폭스](https://snapcraft.io/firefox)처럼 [엄격한](https://snapcraft.io/docs/snap-confinement) 격리가 적용된 snap을 [샌드박싱](https://snapcraft.io/docs/security-sandboxing)하는 데 사용됩니다. 페도라에서는 [ConfinedUsers](https://fedoraproject.org/wiki/SIGs/ConfinedUsers) 특별 관심 그룹을 통해 시스템의 더 많은 부분을 가두려는 커뮤니티 차원의 노력이 진행되고 있습니다.

## 일반 권장 사항 { #general-recommendations }

### 드라이브 암호화 { #drive-encryption }

대부분의 리눅스 배포판에는 설치 프로그램에 [LUKS](../encryption.md#linux-unified-key-setup) FDE를 활성화하는 옵션이 있습니다. 설치 시 이 옵션을 설정하지 않았다면, 암호화는 [디스크 파티션 분할](https://en.wikipedia.org/wiki/Disk_partitioning) 이후, [파일 시스템](https://en.wikipedia.org/wiki/File_system) 포맷 이전에 적용되므로 데이터를 백업하고 다시 설치해야 합니다. 저장 장치를 안전하게 지우는 것도 권장합니다:

- [안전한 데이터 삭제 :material-arrow-right-drop-circle:](https://www.privacyguides.org/articles/2022/05/25/secure-data-erasure/)

### 스왑 { #swap }

잠재적으로 민감한 메모리 데이터가 영구 저장소에 기록되지 않도록 (그리고 성능 향상을 위해) 기존 스왑 파일이나 파티션 대신 [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator)을 사용하는 것을 고려해 보세요. 페도라 기반 배포판은 [기본적으로 ZRAM을 사용](https://fedoraproject.org/wiki/Changes/SwapOnZRAM)합니다.

디스크 절전(최대 절전 모드) 기능이 필요하다면 여전히 기존 스왑 파일이나 파티션을 사용해야 합니다. 이러한 위협 중 일부를 완화하려면 영구 저장 장치에 있는 스왑 공간을 최소한 [암호화](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption)해 두세요.

### 독점 펌웨어(마이크로코드 업데이트) { #proprietary-firmware-microcode-updates }

일부 리눅스 배포판([리눅스-리브레](https://en.wikipedia.org/wiki/Linux-libre) 기반이나 직접 구성하는 배포판 등)에는 심각한 보안 취약점을 패치하는 독점 [마이크로코드](https://en.wikipedia.org/wiki/Microcode) 업데이트가 포함되어 있지 않습니다. 이러한 취약점의 대표적인 예로는 [스펙터](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [멜트다운](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [포어섀도](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)) 및 기타 [하드웨어 취약점](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html)이 있습니다.

마이크로코드 업데이트에는 소프트웨어만으로는 완전히 완화할 수 없는 CPU의 중요한 보안 패치가 포함되어 있으므로, 설치할 것을 **강력히 권장**합니다. 페도라와 오픈수세는 모두 기본적으로 마이크로코드 업데이트를 적용합니다.

### 업데이트 { #updates }

대부분의 리눅스 배포판은 업데이트를 자동으로 설치하거나 설치하라고 알려 줍니다. 취약점이 발견되었을 때 소프트웨어가 패치되도록 OS를 최신 상태로 유지하는 것이 중요합니다.

일부 배포판(특히 고급 사용자를 대상으로 하는 배포판)은 최소한의 구성으로 제공되어 사용자가 직접 처리하기를 기대합니다(예: 아치나 데비안). 이러한 배포판에서는 중요한 보안 업데이트를 받으려면 "패키지 관리자"(`apt`, `pacman`, `dnf` 등)를 수동으로 실행해야 합니다.

또한 일부 배포판은 펌웨어 업데이트를 자동으로 다운로드하지 않습니다. 이를 위해서는 [`fwupd`](https://wiki.archlinux.org/title/Fwupd)를 설치해야 합니다.

### 권한 제어 { #permission-controls }

[웨일랜드](https://wayland.freedesktop.org) 디스플레이 프로토콜을 지원하는 데스크톱 환경은 X11만 지원하는 환경보다 [더 안전합니다](https://lwn.net/Articles/589147). 또한 *일반적으로* **플랫팩**으로 받은 애플리케이션처럼 샌드박스 처리된 애플리케이션을 설치하여 사용할 것을 권장합니다. 플랫팩은 [`security-context-v1`](https://github.com/flatpak/flatpak/pull/4920) 프로토콜과 D-Bus 프로토콜 필터링 기능을 지원하므로, 권한 제어를 통해 앱을 샌드박싱하기 위한 목적으로 앱을 올바르게 식별할 수 있습니다.[^1] 반대로 샌드박스 밖의 애플리케이션은 [포털 권한 저장소를 덮어쓰거나](https://invent.kde.org/plasma/xdg-desktop-portal-kde/-/issues/7#note_1112260) [권한 있는 웨일랜드 프로토콜을 이용하는](https://github.com/swaywm/sway/pull/7648#issuecomment-2507730794) 방식으로 화면 캡처 같은 권한 있는 작업을 자유롭게 수행할 수 있습니다.

## 프라이버시 설정 조정 { #privacy-tweaks }

### MAC 주소 무작위화 { #mac-address-randomization }

많은 데스크톱 리눅스 배포판(페도라, 오픈수세 등)에는 이더넷과 와이파이 설정을 구성하는 [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager)가 포함되어 있습니다.

NetworkManager를 사용할 때 [MAC 주소](https://en.wikipedia.org/wiki/MAC_address)를 무작위화할 수 있습니다. 이렇게 하면 연결된 네트워크에서 특정 기기를 추적하기 어려워지므로 와이파이 네트워크에서 프라이버시가 조금 더 보호됩니다. 하지만 익명성을 제공하지는 [**않습니다**](https://papers.mathyvanhoef.com/wisec2016.pdf).

터미널에서 `/etc/NetworkManager/conf.d/00-macrandomize.conf` 파일을 새로 만들고 다음 내용을 추가하세요:

```text
[device]
wifi.scan-rand-mac-address=yes

[connection]
wifi.cloned-mac-address=random
ethernet.cloned-mac-address=random
```

그런 다음 NetworkManager를 재시작하세요:

```sh
systemctl restart NetworkManager
```

선택적으로 연결 매개변수를 `random`에서 `stable`로 바꾸면 *네트워크마다* 무작위 MAC 주소가 할당되지만, 나중에 같은 네트워크에 다시 연결할 때는 같은 주소가 유지됩니다. `random`을 사용하면 *연결할 때마다* 무작위 MAC 주소가 할당됩니다. 이는 캡티브 포털이 있는 네트워크나 고정 DHCP 할당을 사용하는 네트워크에서 바람직할 수 있지만, 여러 번 연결하는 단일 네트워크 운영자에게 더 쉽게 식별될 수 있다는 단점이 있습니다.

[systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components)를 사용한다면 [RFC 7844(DHCP 클라이언트용 익명성 프로필)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=)를 활성화하는 [`MACAddressPolicy=random`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=)을 설정해야 합니다.

MAC 주소 무작위화는 주로 와이파이 연결에서 유용합니다. 이더넷 연결에서는 네트워크 관리자가 (네트워크 스위치에서 연결된 포트를 확인하는 등) 다른 방법으로 기기를 쉽게 식별할 수 있으므로, MAC 주소를 무작위화해도 이점이 거의 (또는 전혀) 없습니다. 와이파이 MAC 주소 무작위화는 와이파이 펌웨어의 지원 여부에 따라 달라집니다.

### 기타 식별자 { #other-identifiers }

주의해야 할 다른 시스템 식별자도 있습니다. 이것이 여러분의 [위협 모델](../basics/threat-modeling.md)에 해당하는지 생각해 보세요:

- **호스트 이름:** 시스템의 호스트 이름은 연결하는 네트워크와 공유됩니다. 호스트 이름에 이름이나 운영 체제 같은 식별 가능한 단어를 넣지 말고, 일반적인 용어나 무작위 문자열을 사용하세요.
- **사용자 이름:** 마찬가지로 사용자 이름은 시스템 전반에서 다양하게 사용됩니다. 실명 대신 "user" 같은 일반적인 용어를 사용하는 것을 고려해 보세요.

### 시스템 집계 { #system-counting }

페도라 프로젝트는 고유 ID 대신 [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) 변수를 사용하여 미러에 접속하는 고유 시스템의 수를 [집계](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting)합니다. 페도라는 이를 통해 부하를 파악하고 필요한 곳에 업데이트용 서버를 더 잘 배치합니다.

이 [옵션](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo)은 현재 기본적으로 꺼져 있습니다. 향후 활성화될 경우에 대비해 `/etc/dnf/dnf.conf`에 `countme=false`를 추가할 것을 권장합니다. 실버블루처럼 `rpm-ostree`를 사용하는 시스템에서는 [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) 타이머를 마스킹하여 `countme` 옵션을 비활성화합니다.

오픈수세도 시스템을 집계하는 데 [고유 ID](https://en.opensuse.org/openSUSE:Statistics)를 사용하며, `/var/lib/zypp/AnonymousUniqueId` 파일을 비워서 비활성화할 수 있습니다.

[^1]: 이를 통해 웨일랜드 컴포지터가 클라이언트에 대한 식별 정보를 얻을 수 있는 신뢰할 수 있는 방법이 제공됩니다. 그러면 컴포지터는 필요에 따라 보안 정책을 적용할 수 있습니다. [https://github.com/flatpak/flatpak/commit/f0e626a4b60439f211f06d35df74b675a9ef42f4](https://github.com/flatpak/flatpak/commit/f0e626a4b60439f211f06d35df74b675a9ef42f4)
