---
title: "Introdução ao DNS"
icon: material/dns
description: Estes são alguns provedores de DNS criptografados para os quais recomendamos mudar, para substituir a configuração padrão de seu ISP.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

DNS criptografado com servidores de terceiros só deve ser usado para contornar o [bloqueio básico de DNS](https://en.wikipedia.org/wiki/DNS_blocking) quando você pode ter certeza de que não haverá nenhuma consequência. DNS criptografado não ajudará você a esconder nenhuma de suas atividades de navegação.

[Saiba mais sobre DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Provedores Recomendados

These are our favorite public DNS resolvers based on their privacy and security characteristics, and their worldwide performance. Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked you should use a dedicated DNS filtering product instead.

| Provedor de DNS                                                            | Protocolos                               | Logging / Privacy Policy | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | Filtragem                                                                                                                                                                                                                                                                                                                                                                                                                | Signed Apple Profile                                                                                                     |
| -------------------------------------------------------------------------- | ---------------------------------------- | ------------------------ | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | Cleartext   DoH/3   DoT   DoQ   DNSCrypt | Anonymized[^1]           | Anonymized                                                     | Based on server choice. As listas de filtragem usadas podem ser encontradas aqui. [**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS) as defined in [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484) packages queries in the [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) protocol and provides security with HTTPS. Support was first added in web browsers such as Firefox 60 and Chrome 83. | Yes [:octicons-link-external-24:](https://adguard.com/en/blog/encrypted-dns-ios-14.html)                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | Cleartext   DoH/3   DoT                  | Anonymized[^2]           | Não                                                            | Based on server choice.                                                                                                                                                                                                                                                                                                                                                                                                  | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846) |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | Cleartext   DoH/3   DoT   DoQ            | No[^3]                   | Não                                                            | Based on server choice.                                                                                                                                                                                                                                                                                                                                                                                                  | Yes [:octicons-link-external-24:](https://docs.controld.com/docs/macos-platform)                                         |
| [**dns0.eu**](https://dns0.eu)                                             | Cleartext   DoH/3   DoH   DoT   DoQ      | Anonymized[^4]           | Anonymized                                                     | Based on server choice.                                                                                                                                                                                                                                                                                                                                                                                                  | Yes [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                             |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | DoH   DoT                                | No[^5]                   | Não                                                            | Based on server choice. As listas de filtragem usadas podem ser encontradas aqui. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)                                                                                                                                                                                                                                                                  | Yes [:octicons-link-external-24:](https://mullvad.net/en/blog/profiles-to-configure-our-encrypted-dns-on-apple-devices)  |
| [**Quad9**](https://quad9.net)                                             | Cleartext   DoH   DoT   DNSCrypt         | Anonymized[^6]           | Opcional                                                       | Based on server choice, malware blocking by default.                                                                                                                                                                                                                                                                                                                                                                     | Yes [:octicons-link-external-24:](https://quad9.net/news/blog/ios-mobile-provisioning-profiles)                          |

## Self-Hosted DNS Filtering

Uma solução de DNS auto-hospedada é útil para fornecer filtragem em plataformas limitadas como Smart TVs e outros dispositivos IoT, já que não é necessário nenhum “software” do lado do cliente.

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

O Pi-hole foi projetado para ser hospedado em um Raspberry Pi, mas não se limita a esse "hardware". O “software” apresenta uma interface web amigável para visualizar informações e gerenciar conteúdo bloqueado.

[:octicons-home-16: Homepage](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribute }

</details>

</div>

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

AdGuard Home apresenta um painel web amigável para ver informações e gerenciar conteúdos bloqueados.

[:octicons-home-16: Homepage](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Source Code" }

</details>

</div>

## Cloud-Based DNS Filtering

These DNS filtering solutions offer a web dashboard where you can customize the blocklists to your exact needs, similarly to a Pi-hole. These services are usually easier to set up and configure than self-hosted services like the ones above, and can be used more easily across multiple networks (self-hosted solutions are typically restricted to your home/local network unless you set up a more advanced configuration).

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. In addition to their paid plans, they offer a number of preconfigured DNS resolvers you can use for free.

[:octicons-home-16: Homepage](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: Linux](https://docs.controld.com/docs/ctrld)
- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: App Store](https://apps.apple.com/app/1518799460)
- [:simple-github: GitHub](https://github.com/Control-D-Inc/ctrld/releases)

</details>

</div>

### NextDNS

<div class="admonition recommendation" markdown>

![NextDNS logo](assets/img/dns/nextdns.svg){ align=right }

**NextDNS** is a customizable DNS service which lets you block security threats, unwanted content, and advertisements on a DNS level. They offer a fully functional free plan for limited use.

[:octicons-home-16: Homepage](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)
- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)

</details>

</div>

When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether.

NextDNS's free plan is fully functional, but should not be relied upon for security or other critical filtering applications, because after 300,000 DNS queries in a month all filtering, logging, and other account-based functionality is disabled. It can still be used as a regular DNS provider after that point, so your devices will continue to function and make secure queries via DNS-over-HTTPS, just without your filter lists.

NextDNS also offers public DNS-over-HTTPS service at `https://dns.nextdns.io` and DNS-over-TLS/QUIC at `dns.nextdns.io`, which are available by default in Firefox and Chromium, and subject to their default no-logging [privacy policy](https://nextdns.io/privacy).

## Encrypted DNS Proxies

Encrypted DNS proxy software provides a local proxy for the [unencrypted DNS](advanced/dns-overview.md#unencrypted-dns) resolver to forward to. Typically, it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** is an open-source Android client that supports [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) and DNS Proxy. It also provides additional functionality such as caching DNS responses, locally logging DNS queries, and using the app as a firewall.

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

While RethinkDNS takes up the Android VPN slot, you can still use a VPN or Orbot with the app by [adding a Wireguard configuration](https://docs.rethinkdns.com/proxy/wireguard) or [manually configuring Orbot as a Proxy server](https://docs.rethinkdns.com/firewall/orbot), respectively.

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![dnscrypt-proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt-proxy** is a DNS proxy with support for [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), and [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

The anonymized DNS feature does [not](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) anonymize other network traffic.

</div>

## Criteria

**Por favor, note que não somos parceiros de nenhum dos produtos que recomendamos.** Além de [nossos requisitos básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para nos permitir fornecer recomendações objetivas. Recomendamos que você se familiarize com esta lista antes de escolher usar um produto, e que faça sua própria pesquisa para garantir que o produto escolhido é o ideal para você.

All DNS products must support:

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [Minimização QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- Anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.

Additionally, all public providers:

- Prefira suporte a [Anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) ou suporte a orientação geográfica.
- Must not log any personal data to disk
    - As noted in our footnotes, some providers collect query information for example, for purposes like security research, but in that case that data must not be associated with any PII such as IP address, etc.

[^1]: O AdGuard armazena métricas de desempenho agregadas de seus servidores DNS, ou seja, o número de solicitações completas para um determinado servidor, o número de solicitações bloqueadas, e a velocidade de processamento dos pedidos. Eles também coletam e armazenam a base de dados de domínios solicitados nas últimas 24 horas. "Precisamos desta informação para identificar e bloquear novos rastreadores e ameaças". "Também registramos quantas vezes este ou aquele rastreador foi bloqueado. Precisamos desta informação para remover regras desatualizadas dos nossos filtros". [https://adguard-dns.io/pt_br/privacy.html](https://adguard.com/en/privacy/dns.html)
[^2]: O Cloudflare coleta e armazena apenas os dados limitados de consulta de DNS que são enviados para o resolvedor 1.1.1.1. O serviço de resolução 1.1.1.1 não registra dados pessoais, e a maior parte dos limitados dados de consulta, não pessoalmente identificáveis, é armazenado por apenas 25 horas. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: ControlD somente coleta e armazena métricas para resolvedores "Premium" com perfis DNS personalizados. Resolvedores gratuitos não registram dados. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: dns0.eu collects some data for their threat intelligence feeds, to monitor for newly registered/observed/active domains and other bulk data. That data is shared with some [partners](https://docs.dns0.eu/data-feeds/introduction) for e.g. security research. They do not collect any Personally Identifiable Information. [https://dns0.eu/privacy](https://dns0.eu/privacy)
[^5]: O serviço DNS do Mullvad está disponível tanto para assinantes quanto para não assinantes do Mullvad VPN. A sua política de privacidade afirma explicitamente que não armazenam as solicitações DNS de maneira nenhuma. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^6]: Quad9 coleta alguns dados para fins de monitoramento e resposta a ameaças. Esses dados podem então ser misturados e divulgados, por exemplo, para fins de pesquisas de segurança. Quad9 não coleta ou grava endereços IP, ou outros dados que eles considerem pessoalmente identificáveis. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
