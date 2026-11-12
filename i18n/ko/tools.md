---
meta_title: "광고 없는 프라이버시 도구/서비스 추천 - 프라이버시 가이드"
title: "프라이버시 도구"
icon: material/tools
hide:
  - toc
description: 프라이버시 가이드 커뮤니티가 추천하는 프라이버시 도구, 서비스, 소프트웨어, 하드웨어의 전체 목록입니다.
---

특정 문제를 해결할 도구를 찾고 있다면, 아래에서 저희가 추천하는 다양한 하드웨어 및 소프트웨어를 살펴보세요. 추천 도구는 주로 보안 기능을 기준으로 선정하며, 탈중앙화 및 오픈 소스 도구도 우선적으로 고려합니다. 전 세계적인 대규모 감시 프로그램으로부터의 보호, 빅테크 기업 회피, 공격 완화 등 다양한 위협 모델에 적용할 수 있지만, 무엇이 여러분에게 가장 적합한지는 여러분만이 판단할 수 있습니다.

<div class="grid" markdown>

<div markdown>
[VPN 제공업체](vpn.md){ .md-button }
[비밀번호 관리자](passwords.md){ .md-button }
[이메일 제공업체](email.md){ .md-button }
[브라우저 확장 프로그램](browser-extensions.md){ .md-button }
[DNS 서버](dns.md){ .md-button }
[이메일 별칭 서비스](email-aliasing.md){ .md-button }
[사진 관리 도구](photo-management.md){ .md-button }
</div>

</div>

<div markdown>

<div class="admonition info" markdown>

[자체 호스팅 추천](self-hosting/index.md)은 별도 카테고리로 이동했습니다.

</div>

</div>

여러분에게 가장 적합한 프라이버시 도구와 대체 프로그램을 찾는 데 도움이 필요하다면, 프라이버시 가이드 [포럼](https://discuss.privacyguides.net)이나 [매트릭스](https://matrix.to/#/#privacyguides:matrix.org) 커뮤니티에서 토론을 시작해 보세요!

각 프로젝트에 대한 자세한 내용, 선정 이유, 추가 팁과 요령을 알고 싶다면 각 섹션의 "자세히 알아보기" 링크를 클릭하거나, 추천 항목 자체를 클릭하여 해당 페이지의 섹션으로 바로 이동하세요.

<div class="grid" markdown>

<div markdown>
- [x] **광고 없는 추천**
- [x] **잦은 업데이트**
- [x] **독자의 신뢰**
</div>

<div markdown>
- [x] **완전한 편집 독립성**
- [x] **오픈 소스 기여**
- [x] **언론인의 신뢰**
</div>

</div>

## 프라이버시 웹 브라우저 { #private-web-browsers }

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/images/browsers/tor.svg){ align=left }

**Tor Browser** (Desktop & Android) is the top choice if you need anonymity, as it provides you with access to the **Tor** network, a group of volunteer-operated servers that allows you to connect for free and improve your privacy and security on the Internet. 개인과 단체는 ".onion 히든 서비스"를 통해 프라이버시를 침해받지 않고 토르 네트워크에서 정보를 공유할 수도 있습니다. 토르 트래픽은 차단하고 추적하기 어렵기 때문에, 토르는 효과적인 검열 우회 도구입니다.

[전체 리뷰 읽기 :material-arrow-right-drop-circle:](tor.md){ .md-button .md-button--primary }

</div>

<div class="grid cards" markdown>

- ![Mullvad Browser logo](assets/images/browsers/mullvad_browser.svg){ .lg .middle .twemoji } **Mullvad Browser**

    ---

    **Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed, aimed at providing Tor Browser's anti-fingerprinting browser technologies to VPN users.

    - [Read Full Review :material-arrow-right-drop-circle:](desktop-browsers.md#mullvad-browser)

- ![Firefox logo](assets/images/browsers/firefox.svg){ .lg .middle .twemoji } **Firefox**

    ---

    **Firefox** is a great Chromium alternative which provides strong privacy settings such as [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), which can help block various [types of tracking](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

    - [Read Full Review :material-arrow-right-drop-circle:](desktop-browsers.md#firefox)

- ![Brave logo](assets/images/browsers/brave.svg){ .lg .middle .twemoji } **Brave Browser**

    ---

    **Brave** is a private-by-default browser based on Chromium, so it should feel familiar and have minimal website compatibility issues.

    - [Brave 데스크톱 리뷰 :material-arrow-right-drop-circle:](desktop-browsers.md#brave)
    - [Brave 모바일 리뷰 :material-arrow-right-drop-circle:](mobile-browsers.md#brave)

- ![Safari 로고](assets/images/browsers/safari.svg){ .lg .middle .twemoji } **Safari (iOS)**

    ---

    [지문 추적 방지](https://webkit.org/blog/15697/private-browsing-2-0) 기능과 기본 제공되는 추적기 차단 기능 덕분에 **Safari**를 권장합니다. 또한 비공개 브라우징 모드에서 쿠키를 분리하여 탭 간 추적을 방지합니다.

    - [전체 리뷰 읽기 :material-arrow-right-drop-circle:](mobile-browsers.md#safari-ios)

</div>

<div class="grid" markdown>

<div markdown>
### 브라우저 확장 프로그램 { #browser-extensions }

<div class="grid cards" markdown>

- ![uBlock Origin 로고](assets/images/browsers/ublock_origin.svg){ .twemoji loading=lazy } [uBlock Origin](browser-extensions.md#ublock-origin)
- ![uBlock Origin Lite 로고](assets/images/browsers/ublock_origin_lite.svg){ .twemoji loading=lazy } [uBlock Origin Lite](browser-extensions.md#ublock-origin-lite)
- ![AdGuard 로고](assets/images/browsers/adguard.svg){ .twemoji loading=lazy } [iOS용 AdGuard](browser-extensions.md#adguard)

</div>

</div>

<div markdown>
### 더 많은 토르 네트워크 도구 { #more-tor-network-tools }

<div class="grid cards" markdown>

- ![Onion Browser 로고](assets/images/self-contained-networks/onion_browser.svg){ .twemoji loading=lazy } [Onion Browser (iOS용 Tor)](tor.md#onion-browser-ios)

</div>

</div>

</div>

## 프라이버시 VPN 제공업체 TOP 3 { #top-3-private-vpn-providers }

<details class="danger" markdown>
<summary>VPN은 익명성을 제공하지 않습니다</summary>

VPN을 사용해도 브라우징 습관이 익명으로 유지되지 **않으며**, 안전하지 않은(HTTP) 트래픽에 보안이 추가되지도 않습니다.

**익명성**이 필요하다면 토르 브라우저를 사용해야 합니다.

**보안**을 강화하고 싶다면 항상 HTTPS로 웹사이트에 연결하고 있는지 확인해야 합니다. VPN은 올바른 보안 관행을 대체하지 못합니다.

[자세히 알아보기 :material-arrow-right-drop-circle:](vpn.md)

</details>

<div class="grid cards" markdown>

- ![Proton VPN 로고](assets/images/vpn/protonvpn.svg){ .lg .middle .twemoji } **Proton VPN**

    ---

    - [x] **112개국 이상**
    - [x] WireGuard 지원
    - [x] 현금 결제
    - [x] 부분 포트 포워딩 지원
    - [ ] IPv6 미지원

    [전체 리뷰 읽기 :material-arrow-right-drop-circle:](vpn.md#proton-vpn)

- ![IVPN 로고](assets/images/vpn/mini/ivpn.svg){ .lg .middle .twemoji } **IVPN**

    ---

    - [x] **37개국 이상**
    - [x] WireGuard 지원
    - [x] 모네로 및 현금 결제
    - [ ] 포트 포워딩 미지원
    - [ ] IPv6 미지원

    [전체 리뷰 읽기 :material-arrow-right-drop-circle:](vpn.md#ivpn)

- ![Mullvad 로고](assets/images/vpn/mullvad.svg){ .lg .middle .twemoji } **Mullvad**

    ---

    - [x] **49개국 이상**
    - [x] WireGuard 지원
    - [x] 모네로 및 현금 결제
    - [ ] 포트 포워딩 미지원
    - [x] IPv6 지원

    [전체 리뷰 읽기 :material-arrow-right-drop-circle:](vpn.md#mullvad)

</div>

## 프라이버시 이메일 제공업체 TOP 3 { #top-3-private-email-providers }

<div class="grid cards" markdown>

- ![Proton Mail 로고](assets/images/email/protonmail.svg){ .lg .middle .twemoji } **Proton Mail**

    ---

    프로톤 메일은 개인정보 보호, 암호화, 보안 및 사용 편의성에 중점을 둔 이메일 서비스입니다. 2013년부터 운영되고 있습니다. 프로톤 AG는 스위스 제네바에 본사를 두고 있습니다. 프로톤 메일 무료 요금제는 500MB의 메일 저장 공간을 제공하며, 무료로 최대 1GB까지 늘릴 수 있습니다.

    [전체 리뷰 읽기 :material-arrow-right-drop-circle:](email.md#proton-mail)

- ![Mailbox Mail 로고](assets/images/email/mailbox-mail.svg){ .lg .middle .twemoji } **Mailbox Mail**

    ---

    Mailbox Mail(구 *Mailbox.org*)은 보안과 광고 없음에 중점을 두고, 100% 친환경 에너지로 운영되는 이메일 서비스입니다. 2014년부터 운영되고 있습니다. 메일박스 메일은 독일 베를린에 기반을 두고 있습니다. 계정은 최대 2GB의 저장 공간으로 시작하며, 필요에 따라 업그레이드할 수 있습니다.

    [전체 리뷰 읽기 :material-arrow-right-drop-circle:](email.md#mailbox-mail)

- ![Tuta 로고](assets/images/email/tuta.svg#only-light){ .lg .middle .twemoji }![Tuta 로고](assets/images/email/tuta-dark.svg#only-dark){ .lg .middle .twemoji } **Tuta**

    ---

    투타(구 *Tutanota*)는 암호화를 통해 보안과 개인정보 보호에 중점을 둔 이메일 서비스입니다. 투타는 2011년부터 운영되고 있으며, 독일 하노버에 기반을 두고 있습니다. 무료 계정은 1GB의 저장 공간으로 시작합니다.

    [전체 리뷰 읽기 :material-arrow-right-drop-circle:](email.md#tuta)

</div>

<div class="grid" markdown>

<div markdown>
### 이메일 별칭 서비스 { #email-aliasing-services }

<div class="grid cards" markdown>

- ![Addy.io 로고](assets/images/email-aliasing/addy.svg){ .twemoji loading=lazy } [Addy.io](email-aliasing.md#addyio)
- ![SimpleLogin 로고](assets/images/email-aliasing/simplelogin.svg){ .twemoji loading=lazy } [SimpleLogin](email-aliasing.md#simplelogin)

</div>

</div>

</div>

### 안전한 이메일 클라이언트 { #secure-email-clients }

<div class="grid cards" markdown>

- ![Thunderbird 로고](assets/images/email-clients/thunderbird.svg){ .twemoji loading=lazy } [Thunderbird](email-clients.md#thunderbird)
- ![Apple Mail 로고](assets/images/email-clients/applemail.png){ .twemoji loading=lazy } [Apple Mail (macOS)](email-clients.md#apple-mail-macos)
- ![FairEmail 로고](assets/images/email-clients/fairemail.svg){ .twemoji loading=lazy } [FairEmail (Android)](email-clients.md#fairemail-android)
- ![GNOME Evolution 로고](assets/images/email-clients/evolution.svg){ .twemoji loading=lazy } [GNOME Evolution (Linux)](email-clients.md#gnome-evolution-gnome)
- ![Kontact 로고](assets/images/email-clients/kontact.svg){ .twemoji loading=lazy } [Kontact (Linux)](email-clients.md#kontact-kde)
- ![Mailvelope 로고](assets/images/email-clients/mailvelope.svg){ .twemoji loading=lazy } [Mailvelope (표준 웹메일용 PGP)](email-clients.md#mailvelope-browser)
- ![NeoMutt 로고](assets/images/email-clients/mutt.svg){ .twemoji loading=lazy } [NeoMutt (CLI)](email-clients.md#neomutt-cli)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](email-clients.md)

## 더 많은 프라이버시 서비스 제공업체 { #more-private-service-providers }

### 클라우드 스토리지 { #cloud-storage }

<div class="grid cards" markdown>

- ![프로톤 드라이브 로고](assets/images/cloud/protondrive.svg){ .twemoji loading=lazy } [프로톤 드라이브](cloud.md#proton-drive)
- ![트레소릿 로고](assets/images/cloud/tresorit.svg){ .twemoji loading=lazy } [트레소릿](cloud.md#tresorit)
- ![피어고스 로고](assets/images/cloud/peergos.svg){ .twemoji loading=lazy } [피어고스](cloud.md#peergos)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](cloud.md)

### 데이터 삭제 서비스 { #data-removal-services }

<div class="grid cards" markdown>

- ![EasyOptOuts 로고](assets/images/data-broker-removals/easyoptouts.svg){ .twemoji loading=lazy } [EasyOptOuts](data-broker-removals.md#easyoptouts-paid)
- ![Google 로고](assets/images/data-broker-removals/google.svg){ .twemoji loading=lazy } [Google *당신에 관한 검색 결과*](data-broker-removals.md#google-results-about-you-free)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](data-broker-removals.md)

### DNS

#### DNS 제공업체 { #dns-providers }

다양한 기준에 따라 [쿼드9](https://quad9.net) 등 여러 암호화된 DNS 서버를 [추천](dns.md#recommended-providers)합니다. 제공업체를 선택하기 전에 DNS에 관한 페이지를 읽어 볼 것을 권장합니다. 많은 경우 대체 DNS 제공업체를 사용하는 것은 권장하지 않습니다.

[자세히 알아보기 :material-arrow-right-drop-circle:](dns.md)

#### 암호화된 DNS 프록시 { #encrypted-dns-proxies }

<div class="grid cards" markdown>

- ![RethinkDNS logo](assets/images/android/rethinkdns.svg#only-light){ .twemoji loading=lazy }![RethinkDNS logo](assets/images/android/rethinkdns-dark.svg#only-dark){ .twemoji loading=lazy } [RethinkDNS](dns.md#rethinkdns)
- ![DNSCrypt-Proxy logo](assets/images/dns/dnscrypt-proxy.svg){ .twemoji loading=lazy } [DNSCrypt-Proxy](dns.md#dnscrypt-proxy)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](dns.md#encrypted-dns-proxies)

### 금융 서비스 { #financial-services }

#### 결제 마스킹 서비스 { #payment-masking-services }

<div class="grid cards" markdown>

- ![Privacy.com logo](assets/images/financial-services/privacy_com.svg#only-light){ .twemoji loading=lazy }![Privacy.com logo](assets/images/financial-services/privacy_com-dark.svg#only-dark){ .twemoji loading=lazy } [Privacy.com](financial-services.md#privacycom-us)
- ![MySudo logo](assets/images/financial-services/mysudo.svg#only-light){ .twemoji loading=lazy }![MySudo logo](assets/images/financial-services/mysudo-dark.svg#only-dark){ .twemoji loading=lazy } [MySudo](financial-services.md#mysudo-us-paid)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](financial-services.md#payment-masking-services)

#### 온라인 기프트 카드 마켓플레이스 { #online-gift-card-marketplaces }

<div class="grid cards" markdown>

- ![Coincards logo](assets/images/financial-services/coincards.svg){ .twemoji loading=lazy } [Coincards](financial-services.md#coincards)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](financial-services.md#gift-card-marketplaces)

### 사진 관리 { #photo-management }

<div class="grid cards" markdown>

- ![Ente logo](assets/images/photo-management/ente.svg){ .twemoji loading=lazy } [Ente Photos](photo-management.md#ente-photos)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](photo-management.md)

### 검색 엔진 { #search-engines }

<div class="grid cards" markdown>

- ![Brave Search logo](assets/images/search-engines/brave-search.svg){ .twemoji loading=lazy } [Brave Search](search-engines.md#brave-search)
- ![DuckDuckGo logo](assets/images/search-engines/duckduckgo.svg){ .twemoji loading=lazy } [DuckDuckGo](search-engines.md#duckduckgo)
- ![SearXNG logo](assets/images/search-engines/searxng.svg){ .twemoji loading=lazy } [SearXNG](search-engines.md#searxng)
- ![Startpage logo](assets/images/search-engines/startpage.svg#only-light){ .twemoji loading=lazy }![Startpage logo](assets/images/search-engines/startpage-dark.svg#only-dark){ .twemoji loading=lazy } [Startpage](search-engines.md#startpage)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](search-engines.md)

## 소프트웨어 { #software }

### AI 채팅 { #ai-chat }

<div class="grid cards" markdown>

- ![Kobold logo](assets/images/ai-chat/kobold.png){ .twemoji loading=lazy } [Kobold.cpp](ai-chat.md#koboldcpp)
- ![Llamafile logo](assets/images/ai-chat/llamafile.webp){ .twemoji loading=lazy } [Llamafile](ai-chat.md#llamafile)
- ![Ollama logo](assets/images/ai-chat/ollama.png){ .twemoji loading=lazy } [Ollama (CLI)](ai-chat.md#ollama-cli)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](ai-chat.md)

### 캘린더 동기화 { #calendar-sync }

<div class="grid cards" markdown>

- ![Tuta logo](assets/images/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/images/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](calendar.md#tuta)
- ![Proton Calendar logo](assets/images/calendar/proton-calendar.svg){ .twemoji loading=lazy } [Proton Calendar](calendar.md#proton-calendar)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](calendar.md)

### 암호화폐 { #cryptocurrency }

<div class="grid cards" markdown>

- ![Monero logo](assets/images/cryptocurrency/monero.svg){ .twemoji loading=lazy } [Monero](cryptocurrency.md#monero)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](cryptocurrency.md)

### 데이터 및 메타데이터 가리기 { #data-and-metadata-redaction }

<div class="grid cards" markdown>

- ![MAT2 logo](assets/images/data-redaction/mat2.svg){ .twemoji loading=lazy } [MAT2](data-redaction.md#mat2)
- ![Metadata Cleaner](assets/images/data-redaction/metadatacleaner.svg){ .twemoji loading-lazy } [Metadata Cleaner](data-redaction.md#metadata-cleaner)
- ![ExifEraser logo](assets/images/data-redaction/exiferaser.svg){ .twemoji loading=lazy } [ExifEraser (Android)](data-redaction.md#exiferaser-android)
- ![ExifTool logo](assets/images/data-redaction/exiftool.png){ .twemoji loading=lazy } [ExifTool (CLI)](data-redaction.md#exiftool-cli)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](data-redaction.md)

### 문서 협업 { #document-collaboration }

<div class="grid cards" markdown>

- ![CryptPad logo](assets/images/document-collaboration/cryptpad.svg){ .twemoji loading=lazy } [CryptPad](document-collaboration.md#cryptpad)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](document-collaboration.md)

### 암호화 소프트웨어 { #encryption-software }

<details class="info" markdown>
<summary>운영 체제 암호화</summary>

OS 드라이브를 암호화할 때는 윈도우의 **비트로커**, macOS의 **FileVault**, 리눅스의 **LUKS**처럼 일반적으로 운영 체제가 제공하는 암호화 도구를 사용할 것을 권장합니다. 이러한 도구는 운영 체제에 포함되어 있으며 [보안 암호 프로세서](basics/hardware.md/#tpmsecure-cryptoprocessor) 같은 하드웨어 암호화 요소를 활용합니다.

[자세히 알아보기 :material-arrow-right-drop-circle:](encryption.md#operating-system-encryption)

</details>

#### 크로스 플랫폼 도구 { #cross-platform-tools }

<div class="grid cards" markdown>

- ![Cryptomator logo](assets/images/encryption-software/cryptomator.svg){ .twemoji loading=lazy } [Cryptomator](encryption.md#cryptomator-cloud)
- ![VeraCrypt logo](assets/images/encryption-software/veracrypt.svg#only-light){ .twemoji loading=lazy }![VeraCrypt logo](assets/images/encryption-software/veracrypt-dark.svg#only-dark){ .twemoji loading=lazy } [VeraCrypt (FDE)](encryption.md#veracrypt-disk)
- ![Kryptor logo](assets/images/encryption-software/kryptor.png){ .twemoji loading=lazy } [Kryptor](encryption.md#kryptor)
- ![Tomb logo](assets/images/encryption-software/tomb.png){ .twemoji loading=lazy } [Tomb](encryption.md#tomb)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](encryption.md)

#### OpenPGP 클라이언트 { #openpgp-clients }

<div class="grid cards" markdown>

- ![GnuPG logo](assets/images/encryption-software/gnupg.svg){ .twemoji loading=lazy } [GnuPG](encryption.md#gnu-privacy-guard)
- ![GPG4Win logo](assets/images/encryption-software/gpg4win.svg){ .twemoji loading=lazy } [GPG4Win (Windows)](encryption.md#gpg4win)
- ![GPG Suite logo](assets/images/encryption-software/gpgsuite.png){ .twemoji loading=lazy } [GPG Suite (macOS)](encryption.md#gpg-suite)
- ![OpenKeychain logo](assets/images/encryption-software/openkeychain.svg){ .twemoji loading=lazy } [OpenKeychain](encryption.md#openkeychain)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](encryption.md#openpgp)

### 파일 공유 및 동기화 { #file-sharing-and-sync }

<div class="grid cards" markdown>

- ![Send logo](assets/images/file-sharing-sync/send.svg){ .twemoji loading=lazy } [Send](file-sharing.md#send)
- ![OnionShare logo](assets/images/file-sharing-sync/onionshare.svg){ .twemoji loading=lazy } [OnionShare](file-sharing.md#onionshare)
- ![Syncthing logo](assets/images/file-sharing-sync/syncthing.svg){ .twemoji loading=lazy } [Syncthing](file-sharing.md#syncthing-p2p)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](file-sharing.md)

### 프런트엔드 { #frontends }

<div class="grid cards" markdown>

- ![Redlib logo](assets/images/frontends/redlib.svg){ .twemoji loading=lazy } [Redlib (Reddit, Web)](frontends.md#redlib)
- ![FreeTube logo](assets/images/frontends/freetube.svg){ .twemoji loading=lazy } [FreeTube (YouTube, Desktop)](frontends.md#freetube)
- ![LibreTube logo](assets/images/frontends/libretube.svg#only-light){ .twemoji loading=lazy }![LibreTube logo](assets/images/frontends/libretube-dark.svg#only-dark){ .twemoji loading=lazy } [LibreTube (YouTube, Android)](frontends.md#libretube-android)
- ![NewPipe logo](assets/images/frontends/newpipe.svg){ .twemoji loading=lazy } [NewPipe (YouTube, Android)](frontends.md#newpipe-android)
- ![Invidious logo](assets/images/frontends/invidious.svg#only-light){ .twemoji loading=lazy }![Invidious logo](assets/images/frontends/invidious-dark.svg#only-dark){ .twemoji loading=lazy } [Invidious (YouTube, Web)](frontends.md#invidious)
- ![Piped logo](assets/images/frontends/piped.svg){ .twemoji loading=lazy } [Piped (YouTube, Web)](frontends.md#piped)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](frontends.md)

### 건강 및 웰니스 앱 { #health-and-wellness-apps }

<div class="grid cards" markdown>

- ![Drip logo](assets/images/health-and-wellness/drip.png){ .twemoji loading=lazy } [Drip](health-and-wellness.md#drip)
- ![Euki logo](assets/images/health-and-wellness/euki.svg){ .twemoji loading=lazy } [Euki](health-and-wellness.md#euki)
- ![Apple Health logo](assets/images/health-and-wellness/apple-health.webp#only-light){ .twemoji loading=lazy } ![Apple Health logo](assets/images/health-and-wellness/apple-health-dark.webp#only-dark){ .twemoji loading=lazy } [Apple Health](health-and-wellness.md#apple-health)
- ![Apple Fitness logo](assets/images/health-and-wellness/apple-fitness.webp){ .twemoji loading=lazy } [Apple Fitness](health-and-wellness.md#apple-fitness)
- ![Gadgetbridge logo](assets/images/health-and-wellness/gadgetbridge.svg#only-light){ .twemoji loading=lazy }![Gadgetbridge logo](assets/images/health-and-wellness/gadgetbridge-dark.svg#only-dark){ .twemoji loading=lazy } [Gadgetbridge](health-and-wellness.md#gadgetbridge)
- ![Apple Health logo](assets/images/health-and-wellness/apple-health.webp#only-light){ .twemoji loading=lazy } ![Apple Health logo](assets/images/health-and-wellness/apple-health-dark.webp#only-dark){ .twemoji loading=lazy } [Apple Health Records](health-and-wellness.md#apple-health-records)
- ![CommonHealth logo](assets/images/health-and-wellness/commonhealth.png){ .twemoji loading=lazy } [CommonHealth](health-and-wellness.md#commonhealth)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](health-and-wellness.md)

### 언어 도구 { #language-tools }

<div class="grid cards" markdown>

- ![LibreTranslate logo](assets/images/language-tools/libretranslate.png){ .twemoji } [LibreTranslate](language-tools.md#libretranslate)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](language-tools.md)

### 지도 및 내비게이션 앱 { #maps-and-navigation-apps }

<div class="grid cards" markdown>

- ![Organic Maps logo](assets/images/maps/organic-maps.svg){ .twemoji loading=lazy } [Organic Maps](maps.md#organic-maps)
- ![OsmAnd logo](assets/images/maps/osmand.svg){ .twemoji loading=lazy } [OsmAnd](maps.md#osmand)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](maps.md)

### 다중 인증 도구 { #multi-factor-authentication-tools }

**참고:** [하드웨어 보안 키](#security-keys)는 별도 카테고리로 이동했습니다.

<div class="grid cards" markdown>

- ![Ente Auth logo](assets/images/multi-factor-authentication/ente-auth.svg){ .twemoji loading=lazy } [Ente Auth](multi-factor-authentication.md#ente-auth)
- ![Aegis logo](assets/images/multi-factor-authentication/aegis.png){ .twemoji loading=lazy } [Aegis Authenticator (Android)](multi-factor-authentication.md#aegis-authenticator-android)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](multi-factor-authentication.md)

### 뉴스 애그리게이터 { #news-aggregators }

<div class="grid cards" markdown>

- ![Akregator logo](assets/images/news-aggregators/akregator.svg){ .twemoji loading=lazy } [Akregator](news-aggregators.md#akregator)
- ![NewsFlash logo](assets/images/news-aggregators/newsflash.png){ .twemoji loading=lazy } [NewsFlash](news-aggregators.md#newsflash)
- ![Feeder logo](assets/images/news-aggregators/feeder.png){ .twemoji} [Feeder (Android)](news-aggregators.md#feeder)
- ![Miniflux logo](assets/images/news-aggregators/miniflux.svg#only-light){ .twemoji loading=lazy }![Miniflux logo](assets/images/news-aggregators/miniflux-dark.svg#only-dark){ .twemoji loading=lazy } [Miniflux](news-aggregators.md#miniflux)
- ![NetNewsWire logo](assets/images/news-aggregators/netnewswire.png){ .twemoji loading=lazy } [NetNewsWire](news-aggregators.md#netnewswire)
- ![Newsboat logo](assets/images/news-aggregators/newsboat.svg){ .twemoji loading=lazy } [Newsboat](news-aggregators.md#newsboat)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](news-aggregators.md)

### 노트 { #notebooks }

<div class="grid cards" markdown>

- ![Standard Notes logo](assets/images/notebooks/standard-notes.svg){ .twemoji loading=lazy } [Standard Notes](notebooks.md#standard-notes)
- ![Notesnook logo](assets/images/notebooks/notesnook.svg){ .twemoji loading=lazy } [Notesnook](notebooks.md#notesnook)
- ![Joplin logo](assets/images/notebooks/joplin.svg){ .twemoji loading=lazy } [Joplin](notebooks.md#joplin)
- ![Cryptee logo](assets/images/notebooks/cryptee.svg#only-light){ .twemoji loading=lazy }![Cryptee logo](assets/images/notebooks/cryptee-dark.svg#only-dark){ .twemoji loading=lazy } [Cryptee](notebooks.md#cryptee)
- ![Org-mode logo](assets/images/notebooks/org-mode.svg){ .twemoji loading=lazy } [Org-mode](notebooks.md#org-mode)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](notebooks.md)

### 오피스 제품군 { #office-suites }

<div class="grid cards" markdown>

- ![LibreOffice logo](assets/images/office-suites/libreoffice.svg){ .twemoji loading=lazy } [LibreOffice](office-suites.md#libreoffice)
- ![OnlyOffice logo](assets/images/office-suites/onlyoffice.svg){ .twemoji loading=lazy } [OnlyOffice](office-suites.md#onlyoffice)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](office-suites.md)

### 비밀번호 관리자 { #password-managers }

<div class="grid cards" markdown>

- ![Bitwarden logo](assets/images/password-management/bitwarden.svg){ .twemoji loading=lazy } [Bitwarden](passwords.md#bitwarden)
- ![Proton Pass logo](assets/images/password-management/protonpass.svg){ .twemoji loading=lazy } [Proton Pass](passwords.md#proton-pass)
- ![1Password logo](assets/images/password-management/1password.svg){ .twemoji loading=lazy } [1Password](passwords.md#1password)
- ![Psono logo](assets/images/password-management/psono.svg){ .twemoji loading=lazy } [Psono](passwords.md#psono)
- ![KeePassXC logo](assets/images/password-management/keepassxc.svg){ .twemoji loading=lazy } [KeePassXC](passwords.md#keepassxc)
- ![KeePassDX logo](assets/images/password-management/keepassdx.svg){ .twemoji loading=lazy } [KeePassDX (Android)](passwords.md#keepassdx-android)
- ![KeePassium logo](assets/images/password-management/keepassium.svg){ .twemoji loading=lazy } [KeePassium (iOS & macOS)](passwords.md#keepassium-ios-macos)
- ![Gopass logo](assets/images/password-management/gopass.svg){ .twemoji loading=lazy } [Gopass (CLI)](passwords.md#gopass-cli)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](passwords.md)

### 페이스트빈 { #pastebins }

<div class="grid cards" markdown>

- ![PrivateBin logo](assets/images/pastebins/privatebin.svg){ .twemoji loading=lazy } [PrivateBin](pastebins.md#privatebin)
- ![Paaster logo](assets/images/pastebins/paaster.svg){ .twemoji loading=lazy } [Paaster](pastebins.md#paaster)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](pastebins.md)

### 실시간 커뮤니케이션 { #real-time-communication }

<div class="grid cards" markdown>

- ![Signal logo](assets/images/messengers/signal.svg){ .twemoji loading=lazy } [Signal](real-time-communication.md#signal)
- ![Briar logo](assets/images/messengers/briar.svg){ .twemoji loading=lazy } [Briar](real-time-communication.md#briar)
- ![SimpleX Chat logo](assets/images/messengers/simplex.svg){ .twemoji loading=lazy } [SimpleX Chat](real-time-communication.md#simplex-chat)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](real-time-communication.md)

### 소셜 네트워크 { #social-networks }

<div class="grid cards" markdown>

- ![Mastodon logo](assets/images/social-networks/mastodon.svg){ .twemoji loading=lazy } [Mastodon](social-networks.md#mastodon)
- ![Element logo](assets/images/social-networks/element.svg){ .twemoji loading=lazy } [Element](social-networks.md#element)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](social-networks.md)

## 하드웨어 { #hardware }

### 보안 키 { #security-keys }

<div class="grid cards" markdown>

- ![Yubico logo](assets/images/security-keys/mini/yubico.svg){ .twemoji loading=lazy } [Yubico Security Key](security-keys.md#yubico-security-key)
- ![Yubico logo](assets/images/security-keys/mini/yubico.svg){ .twemoji loading=lazy } [YubiKey](security-keys.md#yubikey)
- ![Nitrokey](assets/images/security-keys/mini/nitrokey.svg){ .twemoji loading=lazy } [Nitrokey](security-keys.md#nitrokey)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](security-keys.md)

### 휴대폰 { #mobile-phones }

<div class="grid cards" markdown>

- ![Google Pixel 6](assets/images/android/google-pixel.png){ .twemoji loading=lazy } [Google Pixel](mobile-phones.md#google-pixel)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](mobile-phones.md)

## 운영 체제 { #operating-systems }

### 모바일 { #mobile }

#### 커스텀 안드로이드 운영 체제 { #custom-android-operating-systems }

<div class="grid cards" markdown>

- ![GrapheneOS logo](assets/images/android/grapheneos.svg#only-light){ .twemoji loading=lazy }![GrapheneOS logo](assets/images/android/grapheneos-dark.svg#only-dark){ .twemoji loading=lazy } [GrapheneOS](android/distributions.md#grapheneos)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](android/distributions.md)

#### 안드로이드 앱 { #android-apps }

<div class="grid cards" markdown>

- ![Shelter logo](assets/images/android/mini/shelter.svg){ .twemoji loading=lazy } [Shelter (Work Profiles)](android/general-apps.md#shelter)
- ![Secure Camera logo](assets/images/android/secure_camera.svg#only-light){ .twemoji loading=lazy }![Secure Camera logo](assets/images/android/secure_camera-dark.svg#only-dark){ .twemoji loading=lazy } [Secure Camera](android/general-apps.md#secure-camera)
- ![Secure PDF Viewer logo](assets/images/android/secure_pdf_viewer.svg#only-light){ .twemoji loading=lazy }![Secure PDF Viewer logo](assets/images/android/secure_pdf_viewer-dark.svg#only-dark){ .twemoji loading=lazy } [Secure PDF Viewer](android/general-apps.md#secure-pdf-viewer)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](android/general-apps.md)

#### 안드로이드 앱을 받는 방법 { #ways-to-obtain-android-apps }

<div class="grid cards" markdown>

- ![Obtainium logo](assets/images/android/obtainium.svg){ .twemoji loading=lazy } [Obtainium (App Manager)](android/obtaining-apps.md#obtainium)
- ![Aurora Store logo](assets/images/android/aurora-store.webp){ .twemoji loading=lazy } [Aurora Store (Google Play Client)](android/obtaining-apps.md#aurora-store)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](android/obtaining-apps.md)

### 데스크톱/PC { #desktoppc }

<div class="grid cards" markdown>

- ![Qubes OS logo](assets/images/qubes/qubes_os.svg){ .twemoji loading=lazy } [Qubes OS (Xen VM Distribution)](desktop.md#qubes-os)
- ![Fedora logo](assets/images/linux-desktop/fedora.svg){ .twemoji loading=lazy } [Fedora Linux](desktop.md#fedora-linux)
- ![openSUSE Tumbleweed logo](assets/images/linux-desktop/opensuse-tumbleweed.svg){ .twemoji loading=lazy } [openSUSE Tumbleweed](desktop.md#opensuse-tumbleweed)
- ![Arch logo](assets/images/linux-desktop/archlinux.svg){ .twemoji loading=lazy } [Arch Linux](desktop.md#arch-linux)
- ![Fedora logo](assets/images/linux-desktop/fedora.svg){ .twemoji loading=lazy } [Fedora Atomic Desktops](desktop.md#fedora-atomic-desktops)
- ![NixOS logo](assets/images/linux-desktop/nixos.svg){ .twemoji loading=lazy } [NixOS](desktop.md#nixos)
- ![Whonix logo](assets/images/linux-desktop/whonix.svg){ .twemoji loading=lazy } [Whonix (Tor)](desktop.md#whonix)
- ![Tails logo](assets/images/linux-desktop/tails.svg){ .twemoji loading=lazy } [Tails (Live Boot)](desktop.md#tails)
- ![Secureblue logo](assets/images/linux-desktop/secureblue.svg){ .twemoji loading=lazy } [Secureblue](desktop.md#secureblue)
- ![Kicksecure logo](assets/images/linux-desktop/kicksecure.svg){ .twemoji loading=lazy } [Kicksecure](desktop.md#kicksecure)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](desktop.md)

### 라우터 펌웨어 { #router-firmware }

<div class="grid cards" markdown>

- ![OpenWrt logo](assets/images/router/openwrt.svg#only-light){ .twemoji loading=lazy }![OpenWrt logo](assets/images/router/openwrt-dark.svg#only-dark){ .twemoji loading=lazy } [OpenWrt](router.md#openwrt)
- ![OPNsense logo](assets/images/router/opnsense.svg){ .twemoji loading=lazy } [OPNsense](router.md#opnsense)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](router.md)

## 고급 도구 { #advanced-tools }

이 도구는 특정 개인에게 유용할 수 있습니다. 대부분의 사람은 신경 쓸 필요가 없는 기능을 제공하며, 효과적으로 활용하려면 보다 깊은 기술 지식이 필요한 경우가 많습니다.

### 대체 네트워크 { #alternative-networks }

<div class="grid cards" markdown>

- ![I2P logo](assets/images/self-contained-networks/i2p.svg#only-light){ .twemoji loading=lazy } ![I2P logo](assets/images/self-contained-networks/i2p-dark.svg#only-dark){ .twemoji loading=lazy } [I2P](alternative-networks.md#i2p-the-invisible-internet-project)
- ![Tor logo](assets/images/self-contained-networks/tor.svg){ .twemoji loading=lazy } [Tor](alternative-networks.md#tor)
- ![Orbot logo](assets/images/self-contained-networks/orbot.svg){ .twemoji loading=lazy } [Orbot (Mobile Tor Proxy)](alternative-networks.md#orbot)
- ![Snowflake logo](assets/images/self-contained-networks/snowflake.svg#only-light){ .twemoji loading=lazy }![Snowflake logo](assets/images/self-contained-networks/snowflake-dark.svg#only-dark){ .twemoji loading=lazy } [Snowflake](alternative-networks.md#snowflake)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](alternative-networks.md)

### 기기 무결성 검증 { #device-integrity-verification }

<div class="grid cards" markdown>

- ![MVT logo](assets/images/device-integrity/mvt.webp#only-light){ .twemoji loading=lazy }![MVT logo](assets/images/device-integrity/mvt-dark.png#only-dark){ .twemoji loading=lazy } [Mobile Verification Toolkit](device-integrity.md#mobile-verification-toolkit)
- ![iMazing logo](assets/images/device-integrity/imazing.png){ .twemoji loading=lazy } [iMazing (iOS)](device-integrity.md#imazing-ios)
- ![Auditor logo](assets/images/device-integrity/auditor.svg#only-light){ .twemoji loading=lazy }![Auditor logo](assets/images/device-integrity/auditor-dark.svg#only-dark){ .twemoji loading=lazy } [Auditor (Android)](device-integrity.md#auditor-android)

</div>

[자세히 알아보기 :material-arrow-right-drop-circle:](device-integrity.md)
