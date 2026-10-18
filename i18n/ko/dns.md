---
title: DNS 리졸버
icon: material/dns
description: ISP의 기본 설정을 대체할 암호화된 DNS 제공업체로 다음을 추천합니다.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

제3자 서버를 이용한 암호화된 **DNS**는 아무런 불이익이 없을 것이 확실할 때 기본적인 [DNS 차단](https://en.wikipedia.org/wiki/DNS_blocking)을 우회하는 용도로만 사용해야 합니다. 암호화된 DNS는 브라우징 활동을 숨기는 데 전혀 도움이 되지 않습니다.

[DNS 자세히 알아보기 :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## 추천 제공업체 { #recommended-providers }

다음은 프라이버시 및 보안 특성과 전 세계적인 성능을 기준으로 프라이버시 가이드가 가장 선호하는 공개 DNS 리졸버입니다. 이 서비스 중 일부는 선택한 서버에 따라 멀웨어나 추적기에 대한 기본적인 DNS 수준 차단을 제공하지만, 무엇이 차단되는지 확인하고 직접 설정하고 싶다면 전용 DNS 필터링 제품을 사용해야 합니다.

| DNS 제공업체                                                       | 프로토콜                                                              | 로깅 / 개인정보 처리방침 | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | 필터링                                                                                                                        | 서명된 애플 프로필                                                                                                                                                                                                                |
| -------------------------------------------------------------- | ----------------------------------------------------------------- | -------------- | -------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**애드가드 공개 DNS**](https://adguard-dns.io/en/public-dns.html)   | 평문 <br>DoH/3 <br>DoT <br>DoQ <br>DNSCrypt | 익명화[^1]        | 익명화                                                            | 서버 선택에 따라 다름. 사용되는 필터 목록은 여기에서 확인할 수 있습니다. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardSDNSFilter) | 예 [:octicons-link-external-24:](https://adguard-dns.io/en/blog/encrypted-dns-ios-14.html)                                                                                                                                 |
| [**클라우드플레어**](https://developers.cloudflare.com/1.1.1.1/setup) | 평문 <br>DoH/3 <br>DoT                                  | 익명화[^2]        | 아니요                                                            | 서버 선택에 따라 다름.                                                                                                              | 아니요 [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846)                                                                                                 |
| [**컨트롤 D 무료 DNS**](https://controld.com/free-dns)              | 평문 <br>DoH/3 <br>DoT <br>DoQ                    | 아니요[^3]        | 아니요                                                            | 서버 선택에 따라 다름.                                                                                                              | 예 <br>[:simple-apple: iOS](https://docs.controld.com/docs/ios-platform) <br>[:material-apple-finder: macOS](https://docs.controld.com/docs/macos-platform#manual-setup-profile)                               |
| [**쿼드9**](https://quad9.net)                                   | 평문 <br>DoH/3 <br>DoT <br>DoQ <br>DNSCrypt | 익명화[^4]        | 선택 사항                                                          | 서버 선택에 따라 다름. 멀웨어 차단이 기본으로 포함되어 있습니다.                                                                                      | 예 <br>[:simple-apple: iOS](https://docs.quad9.net/Setup_Guides/iOS/iOS_14_and_later_(Encrypted)) <br>[:material-apple-finder: macOS](https://docs.quad9.net/Setup_Guides/MacOS/Big_Sur_and_later_(Encrypted)) |

## 클라우드 기반 DNS 필터링 { #cloud-based-dns-filtering }

이러한 DNS 필터링 솔루션은 필요에 맞게 차단 목록을 세밀하게 설정할 수 있는 웹 대시보드를 제공합니다. 이러한 서비스는 여러 네트워크에서 쉽게 사용할 수 있습니다.

### 컨트롤 D { #control-d }

<div class="admonition recommendation" markdown>

![컨트롤 D 로고](assets/img/dns/control-d.svg){ align=right }

**컨트롤 D**는 DNS 수준에서 보안 위협, 원치 않는 콘텐츠, 광고를 차단할 수 있는 맞춤형 DNS 서비스입니다.

유료 요금제 외에도 무료로 사용할 수 있는 사전 구성된 DNS 리졸버를 여러 개 제공합니다.

[:octicons-home-16: 홈페이지](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/1518799460)
- [:simple-github: 깃허브](https://github.com/Control-D-Inc/ctrld/releases)
- [:fontawesome-brands-windows: 윈도우](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: 리눅스](https://docs.controld.com/docs/ctrld)

</details>

</div>

### 넥스트DNS { #nextdns }

<div class="admonition recommendation" markdown>

![넥스트DNS 로고](assets/img/dns/nextdns.svg){ align=right }

**넥스트DNS**는 DNS 수준에서 보안 위협, 원치 않는 콘텐츠, 광고를 차단할 수 있는 맞춤형 DNS 서비스입니다.

사용량이 제한된, 모든 기능을 갖춘 무료 요금제를 제공합니다.

[:octicons-home-16: 홈페이지](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: 깃허브](https://github.com/nextdns/nextdns/releases)
- [:fontawesome-brands-windows: 윈도우](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: 리눅스](https://github.com/nextdns/nextdns/wiki)

</details>

</div>

넥스트DNS를 계정과 함께 사용하면 (일부 기능에 필요하기 때문에) 인사이트 및 로깅 기능이 기본으로 활성화됩니다. 보관하기로 선택한 로그의 보존 기간과 저장 위치를 선택하거나, 로그를 아예 비활성화할 수 있습니다.

넥스트DNS의 무료 요금제는 모든 기능을 갖추고 있지만, 한 달에 DNS 쿼리가 300,000건을 넘으면 모든 필터링, 로깅 및 기타 계정 기반 기능이 비활성화되므로 보안이나 기타 중요한 필터링 용도로 의존해서는 안 됩니다. 그 이후에도 일반 DNS 제공업체로는 계속 사용할 수 있으므로, 필터 목록만 적용되지 않을 뿐 기기는 계속 작동하며 DNS-over-HTTPS(DoH)를 통해 안전한 쿼리를 보냅니다.

넥스트DNS는 `https://dns.nextdns.io`에서 공개 DoH 서비스를, `dns.nextdns.io`에서 DNS-over-TLS/QUIC(DoT/DoQ)을 제공합니다. 이 서비스는 파이어폭스와 크로미움에서 기본으로 사용할 수 있으며, 로그를 남기지 않는 기본 [개인정보 처리방침](https://nextdns.io/privacy)이 적용됩니다.

## 암호화된 DNS 프록시 { #encrypted-dns-proxies }

암호화된 DNS 프록시 소프트웨어는 [암호화되지 않은 DNS](advanced/dns-overview.md#unencrypted-dns) 리졸버가 요청을 전달할 수 있는 로컬 프록시를 제공합니다. 일반적으로 [암호화된 DNS](advanced/dns-overview.md#what-is-encrypted-dns)를 기본 지원하지 않는 플랫폼에서 사용됩니다.

### 리싱크DNS { #rethinkdns }

<div class="admonition recommendation" markdown>

![리싱크DNS 로고](assets/img/android/rethinkdns.svg#only-light){ align=right }
![리싱크DNS 로고](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**리싱크DNS**는 [DoH](advanced/dns-overview.md#dns-over-https-doh), [DoT](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt), DNS 프록시를 지원하는 오픈 소스 안드로이드 클라이언트입니다. 또한 DNS 응답 캐싱, DNS 쿼리 로컬 기록, 앱을 방화벽으로 사용하는 기능 등 추가 기능도 제공합니다.

[:octicons-home-16: 홈페이지](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: 깃허브](https://github.com/celzero/rethink-app/releases)

</details>

</div>

리싱크DNS는 안드로이드의 VPN 슬롯을 차지하지만, 각각 [와이어가드 구성을 추가](https://docs.rethinkdns.com/proxy/wireguard)하거나 [오봇을 프록시 서버로 수동 구성](https://docs.rethinkdns.com/firewall/orbot)하여 이 앱과 함께 VPN이나 오봇을 사용할 수 있습니다.

### DNSCrypt-Proxy

<div class="admonition recommendation" markdown>

![DNSCrypt-Proxy 로고](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**DNSCrypt-Proxy**는 [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DoH](advanced/dns-overview.md#dns-over-https-doh), [익명화된 DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS)를 지원하는 DNS 프록시입니다.

[:octicons-repo-16: 저장소](https://github.com/DNSCrypt/dnscrypt-proxy#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: 리눅스](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

익명화된 DNS 기능은 다른 네트워크 트래픽을 익명화하지 [않습니다](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

</div>

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

모든 DNS 제품은...

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec)을 지원해야 합니다.
- [QNAME 최소화](advanced/dns-overview.md#what-is-qname-minimization)를 지원해야 합니다.
- [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs)를 익명화하거나 기본적으로 비활성화해야 합니다.

또한 모든 공개 제공업체는...

- 개인 데이터를 디스크에 기록해서는 안 됩니다.
    - 각주에 언급했듯이 일부 제공업체는 보안 연구 같은 목적으로 쿼리 정보를 수집하지만, 이 경우에도 해당 데이터는 IP 주소 같은 개인 식별 정보(PII)와 연결되어서는 안 됩니다.
- [애니캐스트](https://en.wikipedia.org/wiki/Anycast) 또는 지역 기반 라우팅(geo-steering)을 지원하는 것이 좋습니다.

[^1]: 애드가드는 특정 서버에 대한 완료된 요청 수, 차단된 요청 수, 요청 처리 속도 등 DNS 서버의 집계된 성능 지표를 저장합니다. 또한 지난 24시간 동안 요청된 도메인의 데이터베이스도 보관하고 저장합니다.

    > 새로운 추적기와 위협을 식별하고 차단하려면 이 정보가 필요합니다. 또한 특정 추적기가 몇 번 차단되었는지도 기록합니다. 필터에서 오래된 규칙을 제거하려면 이 정보가 필요합니다.

    애드가드 DNS: [*개인정보 처리방침*](https://adguard-dns.io/en/privacy.html) [^2]: 클라우드플레어는 1.1.1.1 리졸버로 전송되는 제한된 DNS 쿼리 데이터만 수집하고 저장합니다. 1.1.1.1 리졸버 서비스는 개인 데이터를 기록하지 않으며, 개인을 식별할 수 없는 제한된 쿼리 데이터의 대부분은 25시간 동안만 저장됩니다.

    1.1.1.1 공개 DNS 리졸버: [*프라이버시에 대한 클라우드플레어의 약속*](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) [^3]: 컨트롤 D는 사용자 지정 DNS 프로필이 있는 프리미엄 리졸버에 대해서만 특정 계정 데이터를 기록합니다. 무료 리졸버는 어떠한 데이터도 보관하지 않습니다.

    컨트롤 D: [*개인정보 처리방침*](https://controld.com/privacy) [^4]: 쿼드9는 위협 모니터링 및 대응을 위해 일부 데이터를 수집합니다. 이 데이터는 이후 보안 연구 발전 등의 목적으로 가공되어 공유될 수 있습니다. 쿼드9는 IP 주소나 개인 식별 정보로 간주되는 기타 데이터를 수집하거나 기록하지 않습니다.

    쿼드9: [*데이터 및 개인정보 처리방침*](https://quad9.net/privacy/policy)
