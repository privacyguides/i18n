---
title: 파일 공유 및 동기화
icon: material/share-variant
description: 기기 간에, 친구나 가족과, 또는 온라인에서 익명으로 프라이버시를 지키며 파일을 공유하는 방법을 알아보세요.
cover: file-sharing.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

기기 간에, 친구나 가족과, 또는 온라인에서 익명으로 프라이버시를 지키며 파일을 공유하는 방법을 알아보세요.

## 파일 공유 { #file-sharing }

이미 [프로톤 드라이브](cloud.md#proton-drive)[^1]를 사용하고 있거나 [비트워든](passwords.md#bitwarden) 프리미엄[^2] 구독이 있다면, 각각이 제공하는 파일 공유 기능을 사용해 보세요. 두 기능 모두 종단 간 암호화를 사용합니다. 그렇지 않다면 여기에 소개된 독립형 도구를 사용해 공유하는 파일을 원격 서버가 읽을 수 없도록 할 수 있습니다.

### 센드 { #send }

<div class="admonition recommendation" markdown>

![센드 로고](assets/img/file-sharing-sync/send.svg){ align=right }

**센드**는 중단된 모질라의 파이어폭스 센드 서비스를 포크한 것으로, 링크를 통해 다른 사람에게 파일을 보낼 수 있습니다. 파일은 기기에서 암호화되므로 서버가 읽을 수 없으며, 원하는 경우 비밀번호로 보호할 수도 있습니다. 센드의 관리자는 [공개 인스턴스](https://send.vis.ee)를 호스팅하고 있습니다. 다른 공개 인스턴스를 사용하거나, 센드를 직접 호스팅할 수도 있습니다.

[:octicons-home-16: 홈페이지](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="공개 인스턴스"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title="후원하기" }

</details>

</div>

센드는 웹 인터페이스나 [ffsend](https://github.com/timvisee/ffsend) CLI를 통해 사용할 수 있습니다. 명령줄에 익숙하고 파일을 자주 보낸다면, 자바스크립트 기반 암호화를 피하기 위해 CLI 클라이언트를 사용할 것을 권장합니다. `--host` 플래그를 지정하여 특정 서버를 사용할 수 있습니다:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### 어니언셰어 { #onionshare }

<div class="admonition recommendation" markdown>

![어니언셰어 로고](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**어니언셰어**는 어떤 크기의 파일이든 안전하고 [:material-incognito: 익명으로](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } 공유할 수 있게 해 주는 오픈 소스 도구입니다. 토르 어니언 서비스로 접근할 수 있는 웹 서버를 실행하고, 추측할 수 없는 URL을 수신자와 공유하여 파일을 다운로드하거나 보낼 수 있게 하는 방식으로 작동합니다.

[:octicons-home-16: 홈페이지](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="어니언 서비스" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: 리눅스](https://onionshare.org/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/org.onionshare.OnionShare)

</details>

</div>

어니언셰어는 [:material-close-outline: 검열](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}을 우회하기 위해 [토르 브리지](https://docs.onionshare.org/2.6.2/en/tor.html#automatic-censorship-circumvention)를 통해 연결하는 옵션을 제공합니다.

### 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

- 복호화된 데이터를 원격 서버에 저장해서는 안 됩니다.
- 오픈 소스 소프트웨어여야 합니다.
- 리눅스, macOS, 윈도우용 클라이언트가 있거나, 웹 인터페이스가 있어야 합니다.

## 파일 동기화 { #file-sync }

### 싱크싱(P2P) { #syncthing-p2p }

<div class="admonition recommendation" markdown>

![싱크싱 로고](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**싱크싱**은 오픈 소스 P2P 방식의 지속적 파일 동기화 유틸리티입니다. 로컬 네트워크나 인터넷을 통해 두 대 이상의 기기 간에 파일을 동기화하는 데 사용됩니다. 싱크싱은 중앙 서버를 사용하지 않으며, [블록 교환 프로토콜(Block Exchange Protocol)](https://docs.syncthing.net/specs/bep-v1.html#bep-v1)을 사용해 기기 간에 데이터를 전송합니다. 모든 데이터는 TLS로 암호화됩니다.

[:octicons-home-16: 홈페이지](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title="문서"}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: 리눅스](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

### 평가 기준 { #criteria_1 }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

#### 최소 요구 사항 { #minimum-requirements }

- 제3자의 원격/클라우드 서버가 필요하지 않아야 합니다.
- 오픈 소스 소프트웨어여야 합니다.
- 리눅스, macOS, 윈도우용 클라이언트가 있거나, 웹 인터페이스가 있어야 합니다.

#### 우대 사항 { #best-case }

우대 사항은 이 카테고리에서 완벽한 프로젝트라면 갖추었으면 하는 사항을 나타냅니다. 추천 항목에 이 기능 중 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- 최소한 문서 미리 보기를 지원하는 iOS 및 안드로이드용 모바일 클라이언트가 있는 것이 좋습니다.
- iOS와 안드로이드에서 사진 백업을 지원하고, 선택적으로 안드로이드에서 파일/폴더 동기화를 지원하는 것이 좋습니다.

[^1]: 프로톤 드라이브에서는 공유 가능한 공개 링크를 생성하거나 지정된 이메일 주소로 고유 링크를 보내 [파일이나 폴더를 공유](https://proton.me/support/drive-shareable-link)할 수 있습니다. 공개 링크는 비밀번호로 보호하고, 만료일을 설정하고, 완전히 취소할 수 있으며, 이메일로 공유한 링크는 사용자 지정 권한을 설정하고 마찬가지로 취소할 수 있습니다. 프로톤 드라이브의 [개인정보 처리방침](https://proton.me/drive/privacy-policy)에 따르면 파일 내용, 파일 및 폴더 이름, 미리 보기 이미지는 종단 간 암호화됩니다.
[^2]: [프리미엄](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) 구독을 이용하면 [비트워든 센드](https://bitwarden.com/products/send)로 [종단 간 암호화](https://bitwarden.com/help/send-encryption)를 적용해 파일과 텍스트를 안전하게 공유할 수 있습니다. 센드 링크와 함께 [비밀번호](https://bitwarden.com/help/send-privacy/#send-passwords)를 요구하도록 설정할 수 있습니다. 비트워든 센드에는 [자동 삭제](https://bitwarden.com/help/send-lifespan) 기능도 있습니다.
