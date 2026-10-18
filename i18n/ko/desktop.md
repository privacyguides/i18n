---
title: "데스크톱/PC"
icon: simple/linux
description: 리눅스 배포판은 프라이버시 보호와 소프트웨어 자유를 위해 흔히 추천됩니다.
cover: desktop.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

리눅스 배포판은 프라이버시 보호와 소프트웨어 자유를 위해 흔히 추천됩니다. 아직 리눅스를 사용하지 않는다면, 아래에서 사용해 볼 만한 배포판과 여러 리눅스 배포판에 적용할 수 있는 일반적인 프라이버시 및 보안 개선 팁을 확인해 보세요. 추천 소프트웨어 중 일부는 여러분이 선택한 리눅스 배포판용 패키지로 제공되지 않을 수 있다는 점에 유의하세요.

- [리눅스 개요 :material-arrow-right-drop-circle:](os/linux-overview.md)

## 전통적인 배포판 { #traditional-distributions }

### 페도라 리눅스 { #fedora-linux }

<div class="admonition recommendation" markdown>

![페도라 로고](assets/img/linux-desktop/fedora.svg){ align=right }

**페도라 리눅스**는 리눅스를 처음 사용하는 분들께 추천하는 데스크톱 배포판입니다. 페도라는 일반적으로 다른 배포판보다 먼저 새로운 기술(예: [웨일랜드](https://wayland.freedesktop.org), [파이프와이어](https://pipewire.org))을 도입합니다. 이러한 새로운 기술은 대개 보안, 프라이버시, 전반적인 사용성의 개선을 가져옵니다.

[:octicons-home-16: 홈페이지](https://fedoraproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs){ .card-link title="문서" }
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title="후원하기" }

</details>

</div>

페도라에는 그놈 데스크톱 환경을 사용하는 [페도라 워크스테이션](https://fedoraproject.org/workstation)과 KDE를 사용하는 [페도라 KDE 플라즈마 데스크톱](https://fedoraproject.org/kde)이라는 두 가지 주요 데스크톱 에디션이 있습니다. 지금까지는 페도라 워크스테이션이 더 인기 있고 널리 추천되어 왔지만, KDE도 점점 인기를 얻고 있으며 윈도우와 더 비슷한 사용 경험을 제공하므로 일부 사람들에게는 리눅스로 쉽게 넘어오는 데 도움이 될 수 있습니다. 두 에디션의 보안 및 프라이버시 이점은 매우 비슷하므로, 대부분 개인 취향의 문제입니다.

페도라는 세미 롤링 릴리스 주기를 따릅니다. 데스크톱 환경 같은 일부 패키지는 다음 페도라 릴리스까지 고정되지만, (커널을 포함한) 대부분의 패키지는 릴리스 기간 내내 자주 업데이트됩니다. 각 페도라 릴리스는 1년간 지원되며, 6개월마다 새 버전이 출시됩니다.

### 오픈수세 텀블위드 { #opensuse-tumbleweed }

<div class="admonition recommendation" markdown>

![오픈수세 텀블위드 로고](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**오픈수세 텀블위드**는 안정적인 롤링 릴리스 배포판입니다.

오픈수세 텀블위드는 [Btrfs](https://en.wikipedia.org/wiki/Btrfs)와 [스내퍼](https://en.opensuse.org/openSUSE:Snapper_Tutorial)를 사용하여 문제가 생겼을 때 스냅숏으로 롤백할 수 있도록 합니다.

[:octicons-home-16: 홈페이지](https://get.opensuse.org/tumbleweed){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org){ .card-link title="문서" }
[:octicons-heart-16:](https://shop.opensuse.org){ .card-link title="후원하기" }

</details>

</div>

리눅스 배포판 [평가 기준](#criteria)에서 X11을 피할 것을 권장한 것과 마찬가지로, 레거시 X11 창 시스템만 지원하는 데스크톱 환경(예: Xfce)은 피할 것을 권장합니다. 현재 KDE 플라즈마는 기본적으로 X11을 사용하지만, 웨일랜드도 지원합니다.

텀블위드는 각 업데이트가 배포판의 스냅숏으로 출시되는 롤링 릴리스 모델을 따릅니다. 시스템을 업그레이드하면 새 스냅숏이 다운로드됩니다. 각 스냅숏은 품질을 보장하기 위해 [openQA](https://openqa.opensuse.org)의 일련의 자동화된 테스트를 거칩니다.

### 아치 리눅스 { #arch-linux }

<div class="admonition recommendation" markdown>

![아치 로고](assets/img/linux-desktop/archlinux.svg){ align=right }

**아치 리눅스**는 가볍고 직접 구성하는(DIY) 배포판으로, 설치한 것만 갖추게 됩니다. 자세한 내용은 [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions)를 참고하세요.

[:octicons-home-16: 홈페이지](https://archlinux.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org){ .card-link title="문서" }
[:octicons-heart-16:](https://archlinux.org/donate){ .card-link title="후원하기" }

</details>

</div>

아치 리눅스는 롤링 릴리스 주기를 따릅니다. 정해진 릴리스 일정이 없으며 패키지가 매우 자주 업데이트됩니다.

DIY 배포판이므로 시스템을 직접 [구성하고 유지 관리해야 합니다](os/linux-overview.md#arch-based-distributions). 아치에는 설치 과정을 조금 더 쉽게 해 주는 [공식 설치 프로그램](https://wiki.archlinux.org/title/Archinstall)이 있습니다.

[아치 리눅스 패키지](https://reproducible.archlinux.org)의 상당 부분은 [재현 가능](https://reproducible-builds.org)합니다[^1].

## 원자적 배포판 { #atomic-distributions }

**원자적 배포판**(**불변 배포판**이라고도 함)은 시스템을 직접 수정하는 대신 핵심 시스템 이미지 위에 변경 사항을 겹쳐 적용하는 방식으로 패키지 설치와 업데이트를 처리하는 운영 체제입니다. 원자적 배포판의 장점으로는 향상된 안정성과 업데이트를 쉽게 롤백할 수 있는 기능이 있습니다. 자세한 내용은 [*기존 업데이트 vs 원자적 업데이트*](os/linux-overview.md#traditional-vs-atomic-updates)를 참고하세요.

### 페도라 아토믹 데스크톱 { #fedora-atomic-desktops }

<div class="admonition recommendation" markdown>

![페도라 로고](assets/img/linux-desktop/fedora.svg){ align=right }

**페도라 아토믹 데스크톱**은 `rpm-ostree` 패키지 관리자를 사용하며 컨테이너 기반 작업 흐름과 데스크톱 애플리케이션용 플랫팩에 중점을 둔 페도라 변형 배포판입니다. 이 변형 배포판은 모두 페도라 워크스테이션과 같은 릴리스 일정을 따르므로 같은 빠른 업데이트의 혜택을 받으며 업스트림과 매우 가깝게 유지됩니다.

[:octicons-home-16: 홈페이지](https://fedoraproject.org/atomic-desktops){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/emerging){ .card-link title="문서" }
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title="후원하기" }

</details>

</div>

[페도라 아토믹 데스크톱](https://fedoramagazine.org/introducing-fedora-atomic-desktops)은 선호하는 데스크톱 환경에 따라 다양한 버전으로 제공됩니다. 리눅스 배포판 [평가 기준](#criteria)에서 X11을 피할 것을 권장한 것과 마찬가지로, 레거시 X11 창 시스템만 지원하는 버전은 피할 것을 권장합니다.

이 운영 체제는 [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf) 패키지 관리자를 [`rpm-ostree`](https://coreos.github.io/rpm-ostree)라는 훨씬 진보된 대안으로 대체한다는 점에서 페도라 워크스테이션과 다릅니다. `rpm-ostree` 패키지 관리자는 시스템의 기본 이미지를 다운로드한 다음, [깃](https://en.wikipedia.org/wiki/Git)과 비슷한 커밋 트리 형태로 그 위에 패키지를 겹쳐 적용하는 방식으로 작동합니다. 시스템을 업데이트하면 새 기본 이미지가 다운로드되고, 그 새 이미지에 겹쳐 둔 패키지가 적용됩니다.

업데이트가 완료되면 시스템을 재부팅하여 새 배포본으로 전환합니다. `rpm-ostree`는 시스템의 배포본을 두 개 유지하므로, 새 배포본에 문제가 생기면 쉽게 롤백할 수 있습니다. 필요에 따라 더 많은 배포본을 고정해 둘 수도 있습니다.

이러한 배포판에서는 [플랫팩](https://flatpak.org)이 기본 패키지 설치 방법입니다. `rpm-ostree`는 컨테이너 안에 둘 수 없는 패키지를 기본 이미지 위에 겹쳐 적용하는 용도로만 사용하도록 설계되었기 때문입니다.

플랫팩의 대안으로 [Toolbx](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox)를 사용해 전통적인 페도라 환경을 흉내 내는 [포드맨](https://podman.io) 컨테이너를 만들 수도 있는데, 이는 까다로운 개발자에게 [유용한 기능](https://containertoolbx.org)입니다. 이러한 컨테이너는 호스트 운영 체제와 홈 디렉터리를 공유합니다.

### 닉스OS { #nixos }

<div class="admonition recommendation" markdown>

![닉스OS 로고](assets/img/linux-desktop/nixos.svg){ align=right }

닉스OS는 재현성과 안정성에 중점을 둔 Nix 패키지 관리자 기반의 독립 배포판입니다.

[:octicons-home-16: 홈페이지](https://nixos.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title="문서" }
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title="후원하기" }

</details>

</div>

닉스OS의 패키지 관리자는 모든 패키지의 모든 버전을 **Nix 스토어**의 서로 다른 폴더에 보관합니다. 따라서 같은 패키지의 여러 버전을 시스템에 설치할 수 있습니다. 패키지 콘텐츠가 폴더에 기록되면 해당 폴더는 읽기 전용이 됩니다.

닉스OS도 원자적 업데이트를 제공합니다. 먼저 새 시스템 세대에 필요한 패키지와 파일을 다운로드(또는 빌드)한 다음 그 세대로 전환합니다. 새 세대로 전환하는 방법은 여러 가지가 있습니다. 재부팅 후 활성화하도록 지정하거나, 실행 중에 바로 전환할 수 있습니다. 실행 중에 새 세대로 전환하되 현재 시스템 세대로 설정하지 않는 방식으로 새 세대를 *테스트*해 볼 수도 있습니다. 업데이트 과정에서 문제가 생기면 재부팅만 하면 정상 작동하던 시스템 버전으로 돌아갈 수 있습니다.

Nix 패키지 관리자는 패키지를 정의하는 데 순수 함수형 언어(이 언어의 이름도 Nix입니다)를 사용합니다.

(주요 패키지 소스인) [Nixpkgs](https://github.com/nixos/nixpkgs)는 하나의 깃허브 저장소에 담겨 있습니다. 같은 언어로 자신만의 패키지를 정의한 다음 구성에 쉽게 포함시킬 수도 있습니다.

Nix는 소스 기반 패키지 관리자입니다. 바이너리 캐시에 미리 빌드된 패키지가 없으면 Nix는 정의에 따라 소스에서 패키지를 빌드합니다. 각 패키지는 호스트 시스템과 최대한 독립된, 샌드박스화된 *순수* 환경에서 빌드됩니다. 이 방식으로 빌드된 바이너리는 재현 가능합니다[^1].

## 익명성 중심 배포판 { #anonymity-focused-distributions }

### 후닉스 { #whonix }

<div class="admonition recommendation" markdown>

![후닉스 로고](assets/img/linux-desktop/whonix.svg){ align=right }

**후닉스**는 보안 중심의 데비안 포크인 [킥시큐어](#kicksecure)를 기반으로 합니다. 인터넷에서 프라이버시, 보안, [:material-incognito: 익명성](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }을 제공하는 것을 목표로 합니다. 후닉스는 [큐브스 OS](#qubes-os)와 함께 사용하는 것이 가장 좋습니다.

[:octicons-home-16: 홈페이지](https://whonix.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="어니언 서비스" }
[:octicons-info-16:](https://whonix.org/wiki/Documentation){ .card-link title="문서" }
[:octicons-heart-16:](https://whonix.org/wiki/Donate){ .card-link title="후원하기" }

</details>

</div>

후닉스는 "워크스테이션"과 토르 "게이트웨이", 두 개의 가상 머신으로 실행하도록 설계되었습니다. 워크스테이션의 모든 통신은 반드시 토르 게이트웨이를 거쳐야 합니다. 즉, 워크스테이션이 어떤 종류의 멀웨어에 침해되더라도 실제 IP 주소는 숨겨진 채로 유지됩니다.

주요 기능으로는 토르 스트림 격리, [키 입력 익명화](https://whonix.org/wiki/Keystroke_Deanonymization#Kloak), [암호화된 스왑](https://github.com/Whonix/swap-file-creator), 강화된 메모리 할당자 등이 있습니다. 향후 버전의 후닉스에는 시스템의 모든 프로세스를 완전히 가두기 위해 [시스템 전체 앱아머 정책](https://github.com/roddhjav/apparmor.d)과 [샌드박스화된 앱 실행기](https://whonix.org/wiki/Sandbox-app-launcher)가 포함될 가능성이 높습니다.

후닉스는 [큐브스와 함께](https://whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers) 사용하는 것이 가장 좋습니다. 큐브스에서 VPN ProxyVM과 함께 후닉스를 구성하여 ISP로부터 토르 활동을 숨기는 방법에 대한 [추천 가이드](os/qubes-overview.md#connecting-to-tor-via-a-vpn)가 있습니다.

### 테일즈 { #tails }

<div class="admonition recommendation" markdown>

![테일즈 로고](assets/img/linux-desktop/tails.svg){ align=right }

**테일즈**는 모든 통신을 토르를 통해 라우팅하는 데비안 기반 라이브 운영 체제로, DVD, USB 스틱, SD 카드에 설치하여 거의 모든 컴퓨터에서 부팅할 수 있습니다. [토르](tor.md)를 사용하여 검열을 우회하면서 프라이버시와 [:material-incognito: 익명성](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }을 보호하며, 전원을 끄면 사용한 컴퓨터에 아무런 흔적도 남기지 않습니다.

[:octicons-home-16: 홈페이지](https://tails.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.net/doc/index.en.html){ .card-link title="문서" }
[:octicons-heart-16:](https://tails.net/donate){ .card-link title="후원하기" }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

테일즈는 종료할 때 [비디오 메모리](https://en.wikipedia.org/wiki/Dual-ported_video_RAM)를 [지우지 않습니다](https://gitlab.tails.boum.org/tails/tails/-/issues/5356). 테일즈를 사용한 후 컴퓨터를 재시작하면, 테일즈에서 마지막으로 표시되었던 화면이 잠깐 나타날 수 있습니다. 컴퓨터를 재시작하는 대신 종료하면, 전원이 꺼진 상태로 일정 시간이 지난 후 비디오 메모리가 자동으로 지워집니다.

</div>

테일즈는 망각성(디스크에 아무것도 기록하지 않음) 덕분에 안티 포렌식에 매우 적합하지만, 후닉스처럼 강화된 배포판은 아닙니다. 후닉스가 갖춘 많은 익명성 및 보안 기능이 없으며, 업데이트 주기도 훨씬 깁니다(6주에 한 번). 멀웨어에 침해된 테일즈 시스템은 투명 프록시를 우회할 가능성이 있어, 사용자의 익명성이 해제될 수 있습니다.

테일즈는 토르 브라우저에 [유블록 오리진](browser-extensions.md#ublock-origin)을 기본으로 포함하고 있어, 공격자가 테일즈 사용자의 핑거프린트를 식별하기 더 쉬워질 수 있습니다. [후닉스](desktop.md#whonix) 가상 머신은 유출에 더 강할 수 있지만 망각성이 없으므로, 저장 장치에서 데이터가 복구될 수 있습니다.

테일즈는 설계상 재부팅할 때마다 완전히 초기화되도록 되어 있습니다. 재부팅 사이에 일부 데이터를 저장하도록 암호화된 [영구 저장소](https://tails.net/doc/persistent_storage/index.en.html)를 구성할 수 있습니다.

## 보안 중심 배포판 { #security-focused-distributions }

<small>다음 위협으로부터 보호합니다:</small>

- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy ""){.pg-orange}

### 큐브스 OS { #qubes-os }

<div class="admonition recommendation" markdown>

![큐브스 OS 로고](assets/img/qubes/qubes_os.svg){ align=right }

**큐브스 OS**는 안전한 가상 머신(또는 "큐브")을 통해 데스크톱 컴퓨팅에 강력한 보안을 제공하도록 설계된 오픈 소스 운영 체제입니다. 큐브스는 Xen, X 윈도 시스템, 리눅스를 기반으로 합니다. 대부분의 리눅스 애플리케이션을 실행할 수 있고 대부분의 리눅스 드라이버를 사용할 수 있습니다.

[:octicons-home-16: 홈페이지](https://qubes-os.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="어니언 서비스" }
[:octicons-eye-16:](https://qubes-os.org/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://qubes-os.org/doc){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/QubesOS){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://qubes-os.org/donate){ .card-link title="후원하기" }

</details>

</div>

큐브스 OS는 하위 시스템(예: 네트워킹, USB 등)과 애플리케이션을 별도의 *큐브*에 격리하여 컴퓨터를 보호합니다. [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}의 익스플로잇으로 시스템의 한 부분이 침해되더라도, 추가적인 격리 덕분에 나머지 *큐브*와 핵심 시스템은 보호될 가능성이 높습니다.

큐브스의 작동 방식에 대한 자세한 내용은 [큐브스 OS 개요](os/qubes-overview.md) 페이지를 읽어 보세요.

### 시큐어블루 { #secureblue }

<div class="admonition recommendation" markdown>

![시큐어블루 로고](assets/img/linux-desktop/secureblue.svg){ align=right }

**시큐어블루**는 [페도라 아토믹 데스크톱](#fedora-atomic-desktops)을 기반으로 하는 보안 중심 운영 체제입니다. 알려진 취약점과 알려지지 않은 취약점 모두의 악용을 사전에 방어하기 위한 여러 [보안 기능](https://secureblue.dev/features)을 포함하며, 크로미움 기반의 강화된 웹 브라우저인 [트라이밸런트](https://github.com/secureblue/Trivalent)가 함께 제공됩니다.

[:octicons-home-16: 홈페이지](https://secureblue.dev){ .md-button .md-button--primary }
[:octicons-info-16:](https://secureblue.dev/install){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/secureblue/secureblue){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://secureblue.dev/donate){ .card-link title="후원하기" }

</div>

**트라이밸런트**는 [그래핀OS](android/distributions.md#grapheneos)의 바나듐 브라우저에서 영감을 받은, 데스크톱 리눅스용으로 강화된 시큐어블루의 크로미움입니다.

시큐어블루는 그래핀OS의 [강화된 메모리 할당자](https://github.com/GrapheneOS/hardened_malloc)도 제공하며, 이를 (플랫팩을 포함해) 전역적으로 활성화합니다.

### 킥시큐어 { #kicksecure }

대부분의 경우 데스크톱 용도로는 데비안 같은 "영원히 구식인" 배포판을 [권장하지 않지만](os/linux-overview.md#release-cycle), 킥시큐어는 일반적인 리눅스 설치 이상으로 강화된 데비안 기반 운영 체제입니다.

<div class="admonition recommendation" markdown>

![킥시큐어 로고](assets/img/linux-desktop/kicksecure.svg){ align=right }

**킥시큐어**는 아주 단순하게 말하면 데비안의 공격 표면을 크게 줄여 주는 스크립트, 구성, 패키지의 모음입니다. 기본적으로 많은 프라이버시 및 강화 권장 사항을 적용합니다. 또한 [후닉스](#whonix)의 기반 OS 역할도 합니다.

[:octicons-home-16: 홈페이지](https://kicksecure.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kicksecure.com/wiki/Privacy_Policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://kicksecure.com/wiki/Documentation){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://kicksecure.com/wiki/Donate){ .card-link title="후원하기" }

</details>

</div>

## 평가 기준 { #criteria }

자신에게 맞는 리눅스 배포판을 고르는 것은 매우 다양한 개인 취향에 달려 있으며, 이 페이지는 사용할 만한 모든 배포판을 망라한 목록이 **아닙니다**. 리눅스 개요 페이지에서 [배포판 선택하기](os/linux-overview.md#choosing-your-distribution)에 대한 더 자세한 조언을 확인할 수 있습니다. *이* 페이지의 배포판은 모두 대체로 그곳에서 다룬 지침을 따르며, 다음 기준을 모두 충족합니다:

- 자유 오픈 소스여야 합니다.
- 정기적으로 소프트웨어와 커널 업데이트를 받아야 합니다.
- 마지막 주요 릴리스가 [10년도 더 전](https://x.org/wiki/Releases)인 X11을 피해야 합니다.
    - 주목할 만한 예외는 큐브스이지만, X11에서 흔히 발생하는 [격리 문제](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation)는 가상화를 통해 피할 수 있습니다. 이 격리는 *서로 다른 큐브*(가상 머신)에서 실행되는 앱에만 적용되며, *같은* 큐브에서 실행되는 앱끼리는 서로 보호되지 않습니다.
- 설치 시 전체 디스크 암호화를 지원해야 합니다.
- 정기 릴리스를 1년 이상 고정하지 않아야 합니다.
    - 데스크톱 용도로는 "장기 지원(LTS)"이나 "안정" 배포판 릴리스를 [권장하지 않습니다](os/linux-overview.md#release-cycle).
- 다양한 하드웨어를 지원해야 합니다.
- 더 큰 프로젝트를 선호합니다.
    - 운영 체제를 유지 관리하는 것은 큰 과제이며, 소규모 프로젝트는 피할 수 있는 실수를 더 많이 저지르거나 중요한 업데이트를 지연하는 (더 나쁘게는 아예 사라지는) 경향이 있습니다. (기업의 지원이든 매우 큰 커뮤니티의 지원이든) 10년 후에도 존재할 가능성이 높은 프로젝트를 선호하며, 수작업으로 만들어지거나 관리자가 소수인 프로젝트는 피합니다.

또한 추천 프로젝트에 대한 [표준 평가 기준](about/criteria.md)도 그대로 적용됩니다. **프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.**

[^1]: 재현성이란 최종 사용자에게 제공되는 패키지와 바이너리가 소스 코드와 일치하는지 검증할 수 있는 능력을 의미하며, 잠재적인 [:material-package-variant-closed-remove: 공급망 공격](basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}에 대비하는 데 유용할 수 있습니다.
