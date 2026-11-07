---
title: 자체 호스팅
meta_title: "자체 호스팅 소프트웨어 및 서비스 - 프라이버시 가이드"
description: 기술적인 지식이 있는 독자라면 소프트웨어와 서비스를 자체 호스팅하여 데이터를 최대한 통제함으로써 프라이버시를 추가로 보장받을 수 있습니다.
cover: router.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-server-network: 서비스 제공업체](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

소프트웨어와 서비스를 **자체 호스팅**하는 것은 디지털 주권, 특히 제품 개발자나 공급업체가 통제하는 클라우드 서버로부터의 독립을 통해 더 높은 수준의 프라이버시를 달성하는 방법이 될 수 있습니다. 여기서 자체 호스팅이란 자신의 하드웨어에서 애플리케이션과 데이터를 호스팅하는 것을 의미합니다.

자체 호스팅에는 고급 기술 지식과 관련 위험에 대한 깊은 이해가 필요합니다. 자신과 다른 사람들을 위한 호스트가 되면, 그렇지 않았다면 지지 않았을 책임을 지게 됩니다. 프라이버시 소프트웨어를 잘못 자체 호스팅하면 종단 간 암호화 서비스 제공업체 등을 사용하는 것보다 오히려 상황이 나빠질 수 있으므로, 아직 익숙하지 않다면 피하는 것이 좋습니다.

## :material-dns: DNS 필터링 { #dns-filtering }

<div class="grid cards" markdown>

- ![AdGuard Home logo](../assets/images/self-hosting/adguard-home.svg){ .twemoji loading=lazy } [AdGuard Home](dns-filtering.md#adguard-home)
- ![Pi-Hole logo](../assets/images/self-hosting/pi-hole.svg){ .twemoji loading=lazy } [Pi-Hole](dns-filtering.md#pi-hole)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](dns-filtering.md)

## :material-email: 이메일 서버 { #email-servers }

<div class="grid cards" markdown>

- ![Stalwart logo](../assets/images/self-hosting/stalwart.svg){ .twemoji loading=lazy } [Stalwart](email-servers.md#stalwart)
- ![Mailcow logo](../assets/images/self-hosting/mailcow.svg){ .twemoji loading=lazy } [Mailcow](email-servers.md#mailcow)
- ![Mail-in-a-Box logo](../assets/images/self-hosting/mail-in-a-box.svg){ .twemoji loading=lazy } [Mail-in-a-Box](email-servers.md#mail-in-a-box)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](email-servers.md)

## :material-file-multiple-outline: 파일 관리 { #file-management }

<div class="grid cards" markdown>

- ![PhotoPrism logo](../assets/images/self-hosting/photoprism.svg){ .twemoji loading=lazy } [PhotoPrism](file-management.md#photoprism)
- ![FreedomBox logo](../assets/images/self-hosting/freedombox.svg){ .twemoji loading=lazy } [FreedomBox](file-management.md#freedombox)
- ![Nextcloud logo](../assets/images/self-hosting/nextcloud.svg){ .twemoji loading=lazy } [Nextcloud](file-management.md#nextcloud)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](file-management.md)

## :material-form-textbox-password: 비밀번호 관리 { #password-management }

### 볼트워든 { #vaultwarden }

<div class="admonition recommendation" markdown>

![Vaultwarden logo](../assets/images/self-hosting/vaultwarden.svg#only-light){ align=right }
![Vaultwarden logo](../assets/images/self-hosting/vaultwarden-dark.svg#only-dark){ align=right }

**볼트워든**은 러스트로 작성된 [비트워든](../passwords.md#bitwarden) 동기화 서버의 대체 구현체로, 공식 비트워든 클라이언트와 호환되며 리소스를 많이 사용하는 [공식 서비스](https://github.com/bitwarden/server)를 실행하기 부담스러운 자체 호스팅 환경에 적합합니다.

[:octicons-repo-16: 저장소](https://github.com/dani-garcia/vaultwarden#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title="후원하기" }

</div>

## :material-account-supervisor-circle-outline: 소셜 네트워크 { #social-networks }

소셜 네트워크 소프트웨어의 인스턴스를 직접 자체 호스팅하면 공개 서버 관리자나 관리팀에 의한 잠재적인 [서버 수준의 검열](../social-networks.md#censorship-resistance)을 피하는 데 도움이 됩니다.

### 마스토돈 { #mastodon }

<div class="admonition recommendation" markdown>

![Mastodon logo](../assets/images/social-networks/mastodon.svg){ align=right }

**마스토돈**은 개방형 웹 프로토콜과 자유 오픈 소스 소프트웨어를 기반으로 하는 소셜 네트워크입니다. 탈중앙화 **:simple-activitypub: 액티비티펍** 프로토콜을 사용합니다.

[:octicons-home-16:](https://joinmastodon.org){ .card-link title="홈페이지" }
[:octicons-info-16:](https://docs.joinmastodon.org/admin/prerequisites){ .card-link title="관리자 문서" }

</div>

마스토돈은 호스팅 제공업체조차 검열 대상이 되는 더 극단적인 상황을 위해 [토르 네트워크와 통합](https://docs.joinmastodon.org/admin/optional/tor)할 수 있지만, 이 경우 (대부분의 다른 히든 서비스처럼) 토르와 통합된 다른 서버만 여러분의 콘텐츠에 접근할 수 있게 될 수 있습니다.

마스토돈은 크고 활발한 자체 호스팅 커뮤니티의 혜택을 크게 받고 있으며, 관리 방법도 포괄적으로 문서화되어 있습니다. 다른 많은 액티비티펍 플랫폼은 운영하고 문제를 해결하는 데 상당한 기술 지식이 필요할 수 있지만, 마스토돈은 매우 안정적이고 검증된 릴리스를 제공하며, 리눅스 명령줄을 사용할 줄 알고 단계별 안내를 따를 수 있는 사람이라면 일반적으로 문제없이 안전하게 운영할 수 있습니다.

### 엘리먼트 { #element }

<div class="admonition recommendation" markdown>

![Element logo](../assets/images/social-networks/element.svg){ align=right }

**엘리먼트**는 연합된 대화방을 통해 탈중앙화된 통신을 가능하게 하는 개방형 표준인 **:simple-matrix: 매트릭스** 프로토콜의 대표 클라이언트입니다.

[:octicons-home-16:](https://element.io){ .card-link title="홈페이지" }
[:octicons-info-16:](https://element-hq.github.io/synapse/latest){ .card-link title="관리자 문서" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="소스 코드" }

</div>

## :material-flip-to-front: 프런트엔드 { #frontends }

웹 기반 프런트엔드의 인스턴스를 직접 자체 호스팅하면 트래픽이 많은 공개 인스턴스에서 겪을 수 있는 속도 제한을 피하는 데 도움이 됩니다. 다른 사용자들 사이에 섞이려면 다른 사람들도 여러분의 인스턴스를 함께 사용하는 것이 중요합니다. 다른 사람들의 사용 내역이 여러분의 호스팅과 연결되므로, 어디서 어떻게 호스팅하는지에 주의해야 합니다.

<div class="grid cards" markdown>

- ![Redlib logo](../assets/images/frontends/redlib.svg){ .lg .middle .twemoji } [**Redlib (Reddit)**](../frontends.md#redlib)

  ---

  [:octicons-info-16:](https://github.com/redlib-org/redlib#deployment){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="소스 코드" }

- ![Invidious logo](../assets/images/frontends/invidious.svg#only-light){ .twemoji }![Invidious logo](../assets/images/frontends/invidious-dark.svg#only-dark){ .twemoji } [**Invidious (YouTube)**](../frontends.md#invidious)

  ---

  [:octicons-home-16:](https://invidious.io){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://docs.invidious.io/installation){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="소스 코드" }

- ![Piped logo](../assets/images/frontends/piped.svg){ .twemoji } [**Piped (YouTube)**](../frontends.md#piped)

  ---

  [:octicons-info-16:](https://docs.piped.video/docs/self-hosting){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="소스 코드" }

</div>

## 더 많은 도구... { #more-tools }

웹사이트의 다른 카테고리에서 추천하는 도구 중에도 자체 호스팅 옵션을 제공하는 것이 있으므로, 문서를 읽어 본 후 소프트웨어를 호스팅할 자신이 있다면 고려해 볼 수 있습니다.

<div class="grid cards" markdown>

- ![Peergos logo](../assets/images/cloud/peergos.svg){ .twemoji } [**Peergos**](../cloud.md#peergos)

  ---

  [:octicons-home-16:](https://peergos.org){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://github.com/peergos/peergos#usage---running-locally-to-log-in-to-another-instance){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="소스 코드" }

- ![Addy.io logo](../assets/images/email-aliasing/addy.svg){ .twemoji } [**Addy.io**](../email-aliasing.md#addyio)

  ---

  [:octicons-home-16:](https://addy.io){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://addy.io/self-hosting){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="소스 코드" }

- ![SimpleLogin logo](../assets/images/email-aliasing/simplelogin.svg){ .twemoji } [**SimpleLogin**](../email-aliasing.md#simplelogin)

  ---

  [:octicons-home-16:](https://addy.io){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://github.com/simple-login/app#prerequisites){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/simple-login){ .card-link title="소스 코드" }

- ![Ente logo](../assets/images/photo-management/ente.svg){ .twemoji } [**Ente Photos**](../photo-management.md#ente-photos)

  ---

  [:octicons-home-16:](https://ente.com){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://ente.com/help/self-hosting/){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="소스 코드" }

- ![CryptPad logo](../assets/images/document-collaboration/cryptpad.svg){ .twemoji } [**CryptPad**](../document-collaboration.md#cryptpad)

  ---

  [:octicons-home-16:](https://cryptpad.fr){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://docs.cryptpad.org/en/admin_guide/index.html){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="소스 코드" }

- ![Send logo](../assets/images/file-sharing-sync/send.svg){ .twemoji } [**Send**](../file-sharing.md#send)

  ---

  [:octicons-home-16:](https://send.vis.ee){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://github.com/timvisee/send/blob/master/docs/deployment.md){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="소스 코드" }

- ![LibreTranslate logo](../assets/images/language-tools/libretranslate.png){ .twemoji } [**LibreTranslate**](../language-tools.md#libretranslate)

  ---

  [:octicons-home-16:](https://libretranslate.com){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://docs.libretranslate.com){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/LibreTranslate/LibreTranslate){ .card-link title="소스 코드" }

- ![Miniflux logo](../assets/images/news-aggregators/miniflux.svg#only-light){ .twemoji }![Miniflux logo](../assets/images/news-aggregators/miniflux-dark.svg#only-dark){ .twemoji } [**Miniflux**](../news-aggregators.md#miniflux)

  ---

  [:octicons-home-16:](https://miniflux.app){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://miniflux.app/docs/index.html#administration-guide){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/miniflux/v2){ .card-link title="소스 코드" }

- ![Standard Notes logo](../assets/images/notebooks/standard-notes.svg){ .twemoji } [**Standard Notes**](../notebooks.md#standard-notes)

  ---

  [:octicons-home-16:](https://standardnotes.com){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://standardnotes.com/help/47/can-i-self-host-standard-notes){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/standardnotes){ .card-link title="소스 코드" }

- ![PrivateBin logo](../assets/images/pastebins/privatebin.svg){ .twemoji } [**PrivateBin**](../pastebins.md#privatebin)

  ---

  [:octicons-home-16:](https://privatebin.info){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/blob/master/doc/Installation.md){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="소스 코드" }

- ![Paaster logo](../assets/images/pastebins/paaster.svg){ .twemoji } [**Paaster**](../pastebins.md#paaster)

  ---

  [:octicons-home-16:](https://paaster.io){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://github.com/WardPearce/paaster#deployment){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/WardPearce/paaster){ .card-link title="소스 코드" }

- ![SimpleX Chat logo](../assets/images/messengers/simplex.svg){ .twemoji } [**SimpleX Chat**](../real-time-communication.md#simplex-chat)

  ---

  [:octicons-home-16:](https://simplex.chat){ .card-link title="홈페이지" }
  [:octicons-info-16:](https://simplex.chat/docs/server.html){ .card-link title="관리자 문서" }
  [:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="소스 코드" }

</div>
