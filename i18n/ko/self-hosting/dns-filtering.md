---
title: DNS 필터링
meta_title: "자체 호스팅 DNS 솔루션 - 프라이버시 가이드"
icon: material/dns
description: 기술적인 지식이 있는 독자라면 DNS 솔루션을 자체 호스팅하여 클라우드 기반 DNS 솔루션이 적용되지 않는 기기에도 필터링을 제공할 수 있습니다.
cover: dns.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-server-network: 서비스 제공업체](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: 감시 자본주의](../basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

**DNS 자체 호스팅**은 클라이언트 측 소프트웨어가 필요하지 않으므로, 스마트 TV나 기타 IoT 기기처럼 통제된 플랫폼에서 [DNS 필터링](https://cloudflare.com/learning/access-management/what-is-dns-filtering)을 제공하는 데 유용합니다. 더 고급 구성을 설정하지 않는 한, 아래의 DNS 솔루션은 일반적으로 가정이나 로컬 네트워크에서만 사용할 수 있다는 점에 유의하세요.

## DNS 싱크홀 { #dns-sinkholes }

[**DNS 싱크홀**](https://en.wikipedia.org/wiki/DNS_sinkhole)은 DNS 필터링을 사용하여 광고 같은 원치 않는 웹 콘텐츠를 차단합니다.

### 파이홀 { #pi-hole }

<div class="admonition recommendation" markdown>

![파이홀 로고](../assets/img/self-hosting/pi-hole.svg){ align=right }

**파이홀**은 통계를 확인하고 차단된 콘텐츠를 관리할 수 있는 친숙한 웹 인터페이스를 갖춘 오픈 소스 DNS 싱크홀입니다. 파이홀은 라즈베리 파이에서 호스팅되도록 설계되었지만, 다른 하드웨어에서도 사용할 수 있습니다.

[:octicons-home-16: 홈페이지](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title="후원하기" }

</div>

### 애드가드 홈 { #adguard-home }

<div class="admonition recommendation" markdown>

![애드가드 홈 로고](../assets/img/self-hosting/adguard-home.svg){ align=right }

**애드가드 홈**은 통계를 확인하고 차단된 콘텐츠를 관리할 수 있는 세련된 웹 인터페이스를 갖춘 오픈 소스 DNS 싱크홀입니다.

[:octicons-home-16: 홈페이지](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="소스 코드" }

</div>
