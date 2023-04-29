---
title: "DNS 리졸버"
icon: material/dns
description: ISP 기본 구성을 대체하여 전환할 용도로 권장하는 암호화 DNS 제공 업체 목록입니다.
cover: dns.png
---

제3자 서버를 사용하는 암호화 DNS는 기본적인 [DNS 차단](https://en.wikipedia.org/wiki/DNS_blocking)을 우회하는 용도로만, 그리고 아무런 문제가 발생하지 않을 것이라고 확신할 수 있는 경우에만 사용해야 합니다. 암호화 DNS는 여러분의 브라우저 탐색 활동을 숨기는 데에 전혀 도움이 되지 않습니다.

[DNS 자세히 알아보기 :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## 권장 제공 업체

| DNS 제공 업체                                                                       | 프라이버시 정책                                                                                              | 프로토콜                                                   | 로그 보관   | ECS   | 필터링                                                                                                               |
| ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------ | ------- | ----- | ----------------------------------------------------------------------------------------------------------------- |
| [**AdGuard**](https://adguard.com/en/adguard-dns/overview.html)                 | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                                | 평문 <br> DoH/3 <br> DoT <br> DNSCrypt | 일부[^1]  | No    | 개인 설정에 따라 달라집니다. 필터 목록은 여기에서 확인할 수 있습니다. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setting-up-1.1.1.1/) | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/) | 평문 <br> DoH/3 <br> DoT                     | 일부[^2]  | No    | 개인 설정에 따라 달라집니다.                                                                                                  |
| [**Control D**](https://controld.com/free-dns)                                  | [:octicons-link-external-24:](https://controld.com/privacy)                                           | 평문 <br> DoH/3 <br> DoT <br> DoQ      | 선택적[^3] | No    | 개인 설정에 따라 달라집니다.                                                                                                  |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls)      | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy/)                    | DoH <br> DoT                                     | 없음[^4]  | No    | 개인 설정에 따라 달라집니다. 필터 목록은 여기에서 확인할 수 있습니다. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    |
| [**NextDNS**](https://www.nextdns.io)                                           | [:octicons-link-external-24:](https://www.nextdns.io/privacy)                                         | 평문 <br> DoH/3 <br> DoT                     | 선택적[^5] | 선택 사항 | 개인 설정에 따라 달라집니다.                                                                                                  |
| [**Quad9**](https://quad9.net)                                                  | [:octicons-link-external-24:](https://quad9.net/privacy/policy/)                                      | 평문 <br> DoH <br> DoT <br> DNSCrypt   | 일부[^6]  | 선택 사항 | 개인 설정에 따라 달라지지만, 멀웨어는 기본적으로 차단됩니다.                                                                                |

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

!!! example "이 단락은 최근에 만들어졌습니다"

    Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec)를 지원해야 합니다.
- [QNAME 최소화](advanced/dns-overview.md#what-is-qname-minimization)를 지원해야 합니다.
- [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) 비활성화를 지원해야 합니다.
- Prefer [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) support or geo-steering support.

## Native Operating System Support

### Android

Android 9 이상 버전은 DNS over TLS를 지원합니다. 해당 설정은 **설정** &rarr; **네트워크 및 인터넷** &rarr; **비공개 DNS**에서 확인할 수 있습니다.

### Apple 기기

iOS, iPadOS, tvOS, macOS 최신 버전은 DoT, DoH를 모두 지원합니다. 두 프로토콜 모두 [구성 프로필](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web)이나 [DNS 설정 API](https://developer.apple.com/documentation/networkextension/dns_settings)를 통해 운영 체제에서 기본으로 지원합니다.

구성 프로필이나, DNS 설정 API를 사용하는 앱을 설치하고 나면 DNS 구성에서 선택 가능합니다. VPN이 활성화되어 있는 경우, VPN 연결 내 DNS 요청은 시스템 전체 설정이 아닌 VPN의 DNS 설정을 사용합니다.

#### Signed Profiles

Apple does not provide a native interface for creating encrypted DNS profiles. [Secure DNS profile creator](https://dns.notjakob.com/tool.html) is an unofficial tool for creating your own encrypted DNS profiles, however they will not be signed. Signed profiles are preferred; signing validates a profile's origin and helps to ensure the integrity of the profiles. A green "Verified" label is given to signed configuration profiles. For more information on code signing, see [About Code Signing](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html). **Signed profiles** are offered by [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io), and [Quad9](https://www.quad9.net/news/blog/ios-mobile-provisioning-profiles/).

!!! info "정보"

    많은 Linux 배포판에서 DNS 조회에 사용하는 `systemd-resolved`는 아직 [DoH를 지원하지 않습니다](https://github.com/systemd/systemd/issues/8639). DoH를 사용하려는 경우, [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) 등의 프록시를 설치 및 [설정하여](https://wiki.archlinux.org/title/Dnscrypt-proxy), 시스템 리졸버에서 모든 DNS 요청을 가져와 HTTPS로 전달하도록 해야 합니다.

## 암호화 DNS 프록시

Encrypted DNS proxy software provides a local proxy for the [unencrypted DNS](advanced/dns-overview.md#unencrypted-dns) resolver to forward to. Typically it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

!!! recommendation

    ![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
    ![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }
    
    **RethinkDNS** is an open-source Android client supporting [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) and DNS Proxy along with caching DNS responses, locally logging DNS queries and can be used as a firewall too.
    
    [:octicons-home-16: 홈페이지](https://rethinkdns.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://docs.rethinkdns.com/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
        - [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

### dnscrypt-proxy

!!! recommendation

    ![dnscrypt-proxy 로고](assets/img/dns/dnscrypt-proxy.svg){ align=right }
    
    **dnscrypt-proxy**는 [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [익명화 DNS(Anonymized DNS)](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS)를 지원하는 DNS 프록시입니다.
    
    !!! warning "익명화 DNS(Anonymized DNS)는 여타 네트워크 트래픽까지 익명화하지 [**않습니다**](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns)."
    
    [:octicons-repo-16: 저장소](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
        - [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
        - [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

## 자체 호스팅 솔루션

자체 호스팅 DNS 솔루션은 클라이언트 측 소프트웨어가 필요하지 않기 때문에, 스마트 TV 및 기타 IoT 기기처럼 통제된 플랫폼에서 필터링을 적용하기에 유용합니다.

### AdGuard Home

!!! recommendation

    ![AdGuard Home 로고](assets/img/dns/adguard-home.svg){ align=right }
    
    **AdGuard Home**은 [DNS 필터링](https://www.cloudflare.com/learning/access-management/what-is-dns-filtering/)을 사용하여 광고 등의 원치 않는 웹 콘텐츠를 차단하는 오픈 소스[DNS 싱크홀](https://wikipedia.org/wiki/DNS_sinkhole)입니다.
    
    세련된 웹 인터페이스를 통해 쉽고 빠른 분석 및 차단 콘텐츠 관리가 가능합니다.
    
    [:octicons-home-16: 홈페이지](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="소스 코드" }

### Pi-hole

!!! recommendation

    ![Pi-hole 로고](assets/img/dns/pi-hole.svg){ align=right }
    
    **Pi-hole**은 [DNS 필터링](https://www.cloudflare.com/learning/access-management/what-is-dns-filtering/)을 사용하여 광고 등의 원치 않는 웹 콘텐츠를 차단하는 오픈 소스 [DNS 싱크홀](https://wikipedia.org/wiki/DNS_sinkhole)입니다.
    
    Pi-hole은 라즈베리 파이에서 호스팅되도록 설계되었지만, 그 외 하드웨어에서도 사용할 수 있습니다. 친절한 웹 인터페이스를 통해 쉽고 빠른 분석 및 차단 콘텐츠 관리가 가능합니다.
    
    [:octicons-home-16: 홈페이지](https://pi-hole.net/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://pi-hole.net/privacy/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://docs.pi-hole.net/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=기부 }

[^1]: AdGuard stores aggregated performance metrics of their DNS servers, namely the number of complete requests to a particular server, the number of blocked requests, and the speed of processing requests. They also keep and store the database of domains requested in within last 24 hours. "We need this information to identify and block new trackers and threats." "We also log how many times this or that tracker has been blocked. We need this information to remove outdated rules from our filters." [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare collects and stores only the limited DNS query data that is sent to the 1.1.1.1 resolver. The 1.1.1.1 resolver service does not log personal data, and the bulk of the limited non-personally identifiable query data is stored only for 25 hours. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/)
[^3]: Control D only logs for Premium resolvers with custom DNS profiles. Free resolvers do not log data. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: Mullvad's DNS service is available to both subscribers and non-subscribers of Mullvad VPN. Their privacy policy explicitly claims they do not log DNS requests in any way. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy/)
[^5]: NextDNS can provide insights and logging features on an opt-in basis. You can choose retention times and log storage locations for any logs you choose to keep. If it's not specifically requested, no data is logged. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: Quad9 collects some data for the purposes of threat monitoring and response. That data may then be remixed and shared, such as for the purpose of security research. Quad9 does not collect or record IP addresses or other data they deem personally identifiable. [https://www.quad9.net/privacy/policy/](https://www.quad9.net/privacy/policy/)
