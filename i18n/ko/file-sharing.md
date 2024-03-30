---
title: "파일 공유 및 동기화"
icon: material/share-variant
description: 기기 간에, 친구 및 가족과, 혹은 익명으로 온라인 상에서 파일을 개인적으로 공유하는 방법을 알아보세요.
cover: file-sharing.webp
---

기기 간에, 친구 및 가족과, 혹은 익명으로 온라인 상에서 파일을 개인적으로 공유하는 방법을 알아보세요.

## 파일 공유

### Send

<div class="admonition recommendation" markdown>

![Send 로고](assets/img/file-sharing-sync/send.svg){ align=right }

**Send**는 Mozilla가 중단했던 Firefox Send 서비스를 포크한 프로젝트입니다. 링크를 통해 다른 사람에게 파일을 전송할 수 있습니다. 파일은 기기에서 암호화되기 때문에 서버에서는 읽을 수 없으며, 원하는 경우 비밀번호로 보호할 수도 있습니다. The maintainer of Send hosts a [public instance](https://send.vis.ee). 다른 공개 인스턴스를 사용할 수도 있으며, 여러분이 직접 Send를 호스팅하는 것도 가능합니다.

[:octicons-home-16: 홈페이지](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="공개 인스턴스"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=문서}
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=기부 }

</details>

</div>

Send는 Send 웹 인터페이스나 [ffsend](https://github.com/timvisee/ffsend) CLI로 이용할 수 있습니다. CLI가 친숙하고 파일을 자주 전송하는 분이시라면, (JavaScript 기반 암호화를 피할 수 있기 때문에) CLI 클라이언트를 사용하실 것을 권장드립니다. `--host` 플래그를 명시하여 특정 서버를 사용할 수 있습니다.

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![OnionShare 로고](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare**는 파일 크기에 관계 없이 안전하게 익명으로 공유할 수 있는 오픈 소스 툴입니다. Tor Onion 서비스로 접근 가능한 웹 서버를 실행하고, 추론 불가능한 URL을 수신자와 공유하여 파일을 다운로드하거나 전송하는 방식으로 작동합니다.

[:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)

</details>

</div>

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

- 복호화된 데이터가 원격 서버에 저장되어서는 안 됩니다.
- 오픈 소스 소프트웨어여야 합니다.
- Linux, macOS, Windows 클라이언트를 제공하거나, 웹 인터페이스가 존재해야 합니다.

## FreedomBox

<div class="admonition recommendation" markdown>

![FreedomBox 로고](assets/img/file-sharing-sync/freedombox.svg){ align=right }

**FreedomBox**는 [SBC(Single Board Computer)](https://ko.wikipedia.org/wiki/%EB%8B%A8%EC%9D%BC_%EB%B3%B4%EB%93%9C_%EC%BB%B4%ED%93%A8%ED%84%B0)에서 구동되도록 설계된 운영체제입니다. 자체 호스팅 서버 애플리케이션을 간편하게 설정할 수 있도록 하는 것이 FreedomBox의 목표입니다.

[:octicons-home-16: Homepage](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=Documentation}
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Source Code" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title=Contribute }

</details>

</div>

## 파일 동기화

### Nextcloud (클라이언트-서버 방식)

<div class="admonition recommendation" markdown>

![Nextcloud 로고](assets/img/productivity/nextcloud.svg){ align=right }

**Nextcloud**는 사용자가 관리하는 개인 서버에서 자기만의 파일 호스팅 서비스를 구축할 수 있는 무료 오픈 소스 클라이언트-서버 소프트웨어 제품군입니다.

[:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Privacy Guides는 Nextcloud용 [E2EE 앱](https://apps.nextcloud.com/apps/end_to_end_encryption)을 사용하는 것을 권장드리지 않습니다. 데이터 손실이 발생할 수 있고, 실험적인 성향이 강하며, 실사용할 만한 품질이 아니기 때문입니다.

</div>

### Syncthing (P2P 방식)

<div class="admonition recommendation" markdown>

![Syncthing 로고](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing**은 P2P 방식으로 작동하는 지속적 파일 동기화 오픈 소스 유틸리티입니다. 로컬 네트워크나 인터넷을 통해 두 개 이상의 장치 간에 파일을 동기화하는 용도로 사용됩니다. Syncthing은 중앙 서버를 사용하지 않으며, [Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1)을 이용해 기기 간에 데이터를 전송합니다. 모든 데이터는 TLS를 이용해 암호화됩니다.

[:octicons-home-16: Homepage](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="Source Code" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nutomic.syncthingandroid)
- [:simple-windows11: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

#### 최소 요구 사항

- 제3자 원격/클라우드 서버가 필요하지 않아야 합니다.
- 오픈 소스 소프트웨어여야 합니다.
- Linux, macOS, Windows 클라이언트를 제공하거나, 웹 인터페이스가 존재해야 합니다.

#### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- 최소한 문서 미리 보기 기능을 지원하는 iOS, Android 모바일 클라이언트가 존재해야 합니다.
- iOS, Android에서 사진 백업을 지원해야 하며, (선택적으로) Android에서는 파일/폴더 동기화를 지원해야 합니다.
