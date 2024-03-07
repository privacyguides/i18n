---
title: "Introdução ao DNS"
icon: material/dns
description: Estes são alguns provedores de DNS criptografados para os quais recomendamos mudar, para substituir a configuração padrão de seu ISP.
cover: dns.webp
---

DNS criptografado com servidores de terceiros só deve ser usado para contornar o [bloqueio básico de DNS](https://en.wikipedia.org/wiki/DNS_blocking) quando você pode ter certeza de que não haverá nenhuma consequência. DNS criptografado não ajudará você a esconder nenhuma de suas atividades de navegação.

[Saiba mais sobre DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Provedores Recomendados

| Provedor de DNS                                                                 | Política de Privacidade                                                                               | Protocolos                                                                   | Registro     | ECS      | Filtragem                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ------------ | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard**](https://adguard.com/en/adguard-dns/overview.html)                 | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                                | Cleartext <br> DoH/3 <br> DoT <br> DoQ <br> DNSCrypt | Alguns[^1]   | Yes      | Based on personal configuration. As listas de filtragem usadas podem ser encontradas aqui. [**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS) as defined in [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484) packages queries in the [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) protocol and provides security with HTTPS. Support was first added in web browsers such as Firefox 60 and Chrome 83. |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setting-up-1.1.1.1/) | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/) | Cleartext <br> DoH/3 <br> DoT                                    | Alguns[^2]   | Não      | Based on personal configuration.                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Control D**](https://controld.com/free-dns)                                  | [:octicons-link-external-24:](https://controld.com/privacy)                                           | Cleartext <br> DoH/3 <br> DoT <br> DoQ                     | Opcional[^3] | Não      | Based on personal configuration.                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls)      | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy/)                    | DoH <br> DoT                                                           | Não[^4]      | Não      | Based on personal configuration. As listas de filtragem usadas podem ser encontradas aqui. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)                                                                                                                                                                                                                                                                  |
| [**NextDNS**](https://www.nextdns.io)                                           | [:octicons-link-external-24:](https://www.nextdns.io/privacy)                                         | Cleartext <br> DoH/3 <br> DoT <br> DoQ                     | Opcional[^5] | Opcional | Based on personal configuration.                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Quad9**](https://quad9.net)                                                  | [:octicons-link-external-24:](https://quad9.net/privacy/policy/)                                      | Cleartext <br> DoH/ <br> DoT <br> DNSCrypt                 | Alguns[^6]   | Opcional | Based on personal configuration, Malware blocking by default.                                                                                                                                                                                                                                                                                                                                                                     |

### Criteria

**Por favor, note que não somos parceiros de nenhum dos produtos que recomendamos.** Além de [nossos requisitos básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para nos permitir fornecer recomendações objetivas. Recomendamos que você se familiarize com esta lista antes de escolher usar um produto, e que faça sua própria pesquisa para garantir que o produto escolhido é o ideal para você.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Estamos trabalhando para estabelecer requisitos definidos para cada seção de nosso site, e isto pode estar sujeito a mudanças. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.

</div>

- Deve suportar [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [Minimização QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- Permitir que [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) seja desativado.
- Prefira suporte a [Anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) ou suporte a orientação geográfica.

## Native Operating System Support

### Android

Android 9 e superior suportam DNS sobre TLS. As configurações podem ser encontradas em: **Configurações** &rarr; **Rede & Internet** &rarr; **DNS particular**.

### Apple Devices

As versões mais recentes do iOS, iPadOS, tvOS e macOS, suportam DoT e DoH. Ambos os protocolos são suportados nativamente através dos [perfis de configuração](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) ou através das [configurações de DNS API](https://developer.apple.com/documentation/networkextension/dns_settings).

Após a instalação de um perfil de configuração ou de um aplicativo que usa a API de configurações de DNS, a configuração de DNS pode ser selecionada. Se uma VPN estiver ativa, a resolução no túnel VPN usará as configurações de DNS da VPN e não suas configurações gerais do sistema.

#### Signed Profiles

A Apple não fornece uma interface nativa para a criação de perfis DNS criptografados. Info Perfis assinados são preferidos; a assinatura valida a origem de um perfil e ajuda a garantir a integridade dos perfis. Uma marca de "Verificado" na cor verde é dada aos perfis de configuração assinados. Para mais informações sobre assinatura de código, ver [Sobre Assinatura de Código](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html). **Perfis assinados** são oferecidos por [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io), e [Quad9](https://www.quad9.net/news/blog/ios-mobile-provisioning-profiles/).

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

`systemd-resolved`, que muitas distribuições Linux usam para fazer suas pesquisas de DNS, ainda não [suporta DoH](https://github.com/systemd/systemd/issues/8639). Se você deseja usar o DoH, você precisará instalar um proxy como [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) e [configurá-lo](https://wiki. rchlinux.org/title/Dnscrypt-proxy) para pegar todas as consultas de DNS do resolvedor do sistema e encaminhá-los por HTTPS.

</div>

## Encrypted DNS Proxies

Encrypted DNS proxy software provides a local proxy for the [unencrypted DNS](advanced/dns-overview.md#unencrypted-dns) resolver to forward to. Typically it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

obnoxious --&gt; | Yes | encryptedDNS(Use&lt;br&gt; encrypted DNS&lt;br&gt; with 3rd party)
    obnoxious --&gt; | No | ispDNS{Does ISP support&lt;br&gt; encrypted DNS?} ispDNS --&gt; | Yes | useISP(Use&lt;br&gt; encrypted DNS&lt;br&gt; with ISP)
    ispDNS --&gt; | No | nothing(Do nothing)

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![dnscrypt-proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt-proxy** is a DNS proxy with support for [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), and [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

<div class="admonition warning" markdown>
<p class="admonition-title">The anonymized DNS feature does <a href="advanced/dns-overview.md#why-shouldnt-i0-use-encrypted-dns"><strong>not</strong></a> anonymize other network traffic.</p>
</div>

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

## Soluções auto-hospedadas

Uma solução de DNS auto-hospedada é útil para fornecer filtragem em plataformas limitadas como Smart TVs e outros dispositivos IoT, já que não é necessário nenhum “software” do lado do cliente.

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** é um programa de código aberto [DNS-sinkhole](https://wikipedia.org/wiki/DNS_sinkhole) que utiliza [filtragem DNS](https://www.cloudflare.com/learning/access-management/what-is-dns-filtering/) para bloquear conteúdos web indesejados, tais como anúncios.

AdGuard Home apresenta um painel web amigável para ver informações e gerenciar conteúdos bloqueados.

[:octicons-home-16: Homepage](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Source Code" }

</details>

</div>

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** é um programa de código aberto [DNS-sinkhole](https://wikipedia.org/wiki/DNS_sinkhole) que usa [filtragem DNS](https://www.cloudflare.com/learning/access-management/what-is-dns-filtering/) para bloquear conteúdos web indesejados, como anúncios.

O Pi-hole foi projetado para ser hospedado em um Raspberry Pi, mas não se limita a esse "hardware". O “software” apresenta uma interface web amigável para visualizar informações e gerenciar conteúdo bloqueado.

[:octicons-home-16: Homepage](https://pi-hole.net/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribute }

</details>

</div>

[^1]: O AdGuard armazena métricas de desempenho agregadas de seus servidores DNS, ou seja, o número de solicitações completas para um determinado servidor, o número de solicitações bloqueadas, e a velocidade de processamento dos pedidos. Eles também coletam e armazenam a base de dados de domínios solicitados nas últimas 24 horas. "Precisamos desta informação para identificar e bloquear novos rastreadores e ameaças". "Também registramos quantas vezes este ou aquele rastreador foi bloqueado. Precisamos desta informação para remover regras desatualizadas dos nossos filtros". [https://adguard-dns.io/pt_br/privacy.html](https://adguard.com/en/privacy/dns.html)
[^2]: O Cloudflare coleta e armazena apenas os dados limitados de consulta de DNS que são enviados para o resolvedor 1.1.1.1. O serviço de resolução 1.1.1.1 não registra dados pessoais, e a maior parte dos limitados dados de consulta, não pessoalmente identificáveis, é armazenado por apenas 25 horas. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/)
[^3]: ControlD somente coleta e armazena métricas para resolvedores "Premium" com perfis DNS personalizados. Resolvedores gratuitos não registram dados. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: O serviço DNS do Mullvad está disponível tanto para assinantes quanto para não assinantes do Mullvad VPN. A sua política de privacidade afirma explicitamente que não armazenam as solicitações DNS de maneira nenhuma. [https://mullvad.net/pt/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy/)
[^5]: NextDNS can provide insights and logging features on an opt-out basis. Você pode escolher o tempo de retenção e os locais de armazenamento dos registros para quaisquer registros que você decidir manter. Se não for especificamente solicitado, nenhum dado é armazenado. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: Quad9 coleta alguns dados para fins de monitoramento e resposta a ameaças. Esses dados podem então ser misturados e divulgados, por exemplo, para fins de pesquisas de segurança. Quad9 não coleta ou grava endereços IP, ou outros dados que eles considerem pessoalmente identificáveis. [https://www.quad9.net/pt/privacy/policy/](https://www.quad9.net/privacy/policy/)
