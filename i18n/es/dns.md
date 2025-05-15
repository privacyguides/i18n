---
title: "Servidores DNS"
icon: material/dns
description: We recommend choosing these encrypted DNS providers to replace your ISP's default configuration.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protégete contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Un DNS cifrado con servidores de terceros solo debe utilizarse para evitar el [bloqueo de DNS básico](https://en.wikipedia.org/wiki/DNS_blocking) cuándo puedas estar seguro de que no habrá ningunas consecuencias. Un DNS cifrado no te ayudará a esconder ninguna de tu actividad en línea.

[Aprende más sobre DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Proveedores Recomendados

Estos son nuestros resolvedores de DNS públicos favoritos en función de sus características de privacidad y seguridad, y de su rendimiento en todo el mundo. Some of these services offer basic DNS-level blocking of malware or trackers depending on the server you choose, but if you want to be able to see and customize what is blocked, you should use a dedicated DNS filtering product instead.

| Proveedor de DNS                                                           | Protocolos                                                               | Logs / Política de Privacidad | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | Filtrado                                                                                                                                                            | Perfil de Apple firmado                                                                                                                                                                                                     |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ----------------------------- | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | Cleartext <br>DoH/3 <br>DoT <br>DoQ <br>DNSCrypt | Anónimo[^1]                   | Anónimo                                                        | Basado en la elección del servidor. La lista de filtros utilizada se puede encontrar aquí. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) | Sí [:octicons-link-external-24:](https://adguard-dns.io/en/blog/encrypted-dns-ios-14.html)                                                                                                                                  |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | Cleartext <br>DoH/3 <br>DoT                                  | Anonymized[^2]                | No                                                             | Basado en la elección del servidor.                                                                                                                                 | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846)                                                                                                    |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | Cleartext <br>DoH/3 <br>DoT <br>DoQ                    | No[^3]                        | No                                                             | Basado en la elección del servidor.                                                                                                                                 | Yes <br>[:simple-apple: iOS](https://docs.controld.com/docs/ios-platform) <br>[:material-apple-finder: macOS](https://docs.controld.com/docs/macos-platform#manual-setup-profile)                               |
| [**DNS0.eu**](https://dns0.eu)                                             | Cleartext <br>DoH/3 <br>DoH <br>DoT <br>DoQ      | Anonymized[^4]                | Anónimo                                                        | Basado en la elección del servidor.                                                                                                                                 | Sí [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                                                                                                                                 |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | DoH <br>DoT                                                        | No[^5]                        | No                                                             | Basado en la elección del servidor. La lista de filtros utilizada se puede encontrar aquí. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    | Yes [:octicons-link-external-24:](https://github.com/mullvad/encrypted-dns-profiles)                                                                                                                                        |
| [**Quad9**](https://quad9.net)                                             | Cleartext <br>DoH <br>DoT <br>DNSCrypt                 | Anonymized[^6]                | Opcional                                                       | Basado en la elección del servidor. Malware blocking is included by default.                                                                                        | Yes <br>[:simple-apple: iOS](https://docs.quad9.net/Setup_Guides/iOS/iOS_14_and_later_(Encrypted)) <br>[:material-apple-finder: macOS](https://docs.quad9.net/Setup_Guides/MacOS/Big_Sur_and_later_(Encrypted)) |

## Servidor DNS autoalojado

Una solución DNS autoalojada es útil para proporcionar filtrado en plataformas controladas, como Smart TV y otros dispositivos IoT, ya que no se necesita software del lado del cliente.

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** es un [DNS-sinkhole](https://es.wikipedia.org/wiki/DNS_sinkhole) de código abierto que utiliza [filtrado DNS](https://cloudflare.com/learning/access-management/what-is-dns-filtering) para bloquear contenidos web no deseados, como la publicidad.

Pi-hole está diseñado para alojarse en una Raspberry Pi, pero no se limita a dicho hardware. El software cuenta con una interfaz web fácil de usar para ver los datos y gestionar los contenidos bloqueados.

[:octicons-home-16: Página Principal](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribuir }

</details>

</div>

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** es un [DNS-sinkhole](https://es.wikipedia.org/wiki/DNS_sinkhole) de código abierto que utiliza [filtrado DNS](https://cloudflare.com/learning/access-management/what-is-dns-filtering) para bloquear contenidos web no deseados, como la publicidad.

AdGuard Home cuenta con una interfaz web pulida para ver información y gestionar el contenido bloqueado.

[:octicons-home-16: Página Principal](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Politica de privacidad" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Código fuente" }inicio

</details>

</div>

## Filtrado DNS basado en la nube

These DNS filtering solutions offer a web dashboard where you can customize the block lists to your exact needs, similarly to a Pi-hole. Estos servicios suelen ser más fáciles de instalar y configurar que los autoalojados, como los anterioriores, y pueden utilizarse más fácilmente en múltiples redes (las soluciones autoalojadas suelen estar restringidas a su red doméstica/local, a menos que se establezca una configuración más avanzada).

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** es un servicio DNS personalizable que permite bloquear amenazas de seguridad, contenidos no deseados y publicidad a nivel de DNS. Además de sus planes de pago, ofrecen una serie de resolvedores DNS preconfigurados que puedes utilizar gratuitamente.

[:octicons-home-16: Homepage](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: App Store](https://apps.apple.com/app/1518799460)
- [:simple-github: GitHub](https://github.com/Control-D-Inc/ctrld/releases)
- [:fontawesome-brands-windows: Windows](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: Linux](https://docs.controld.com/docs/ctrld)

</details>

</div>

### NextDNS

<div class="admonition recommendation" markdown>

![NextDNS logo](assets/img/dns/nextdns.svg){ align=right }

 **NextDNS** es un servicio DNS personalizable que te permite bloquear amenazas de seguridad, contenidos no deseados y publicidad a nivel DNS. Ofrecen un plan gratuito totalmente funcional para uso limitado.

[:octicons-home-16: Homepage](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)
- [:fontawesome-brands-windows: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)

</details>

</div>

Cuando se utiliza con una cuenta, NextDNS habilitará las funciones de información y registro de forma predeterminada (ya que algunas funciones lo requieren). Puedes elegir los tiempos de retención y las ubicaciones de almacenamiento de los registros que desees conservar.

NextDNS's free plan is fully functional, but should not be relied upon for security or other critical filtering applications, because after 300,000 DNS queries in a month all filtering, logging, and other account-based functionality are disabled. It can still be used as a regular DNS provider after that point, so your devices will continue to function and make secure queries via DNS-over-HTTPS (DoH), just without your filter lists.

NextDNS also offers a public DoH service at `https://dns.nextdns.io` and DNS-over-TLS/QUIC (DoT/DoQ) at `dns.nextdns.io`, which are available by default in Firefox and Chromium, and subject to their default, no-logging [privacy policy](https://nextdns.io/privacy).

## Proxies DNS Cifrados

El software de proxy de DNS cifrado proporciona un proxy local para que el servidor DNS [no cifrado](advanced/dns-overview.md#unencrypted-dns) lo reenvíe. Normalmente, se utiliza en plataformas que no soportan [DNS cifrado](advanced/dns-overview.md#what-is-encrypted-dns) de forma nativa.

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** is an open-source Android client that supports [DoH](advanced/dns-overview.md#dns-over-https-doh), [DoT](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) and DNS Proxy. También proporciona funciones adicionales, como el almacenamiento en caché de las respuestas DNS, el registro local de las consultas DNS y el uso de la aplicación como cortafuegos.

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Descargas</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

While RethinkDNS takes up the Android VPN slot, you can still use a VPN or Orbot with the app by [adding a WireGuard configuration](https://docs.rethinkdns.com/proxy/wireguard) or [manually configuring Orbot as a Proxy server](https://docs.rethinkdns.com/firewall/orbot), respectively.

### DNSCrypt-Proxy

<div class="admonition recommendation" markdown>

![DNSCrypt-Proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**DNSCrypt-Proxy** is a DNS proxy with support for [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DoH](advanced/dns-overview.md#dns-over-https-doh), and [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Descargas</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

La función de DNS anónimo [no](advanced/dns-overview.md#por-que-no-deberia-utilizar-un-dns-cifrado) hace anónimo otro tráfico de red.

</div>

## Criterios

**Ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten proporcionar recomendaciones objetivas. Te sugerimos que te familiarices con esta lista antes de elegir usar un proyecto, y que lleves a cabo tu propia investigación para asegurarte de que es la elección correcta para ti.

All DNS products...

- Must support [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- Must support [QNAME Minimization](advanced/dns-overview.md#what-is-qname-minimization).
- Must anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.

Additionally, all public providers...

- Must not log any personal data to disk.
    - As noted in the footnotes, some providers collect query information for purposes like security research, but in that case the data must not be associated with any PII such as IP address, etc.
- Should support [anycast](https://en.wikipedia.org/wiki/Anycast) or geo-steering.

[^1]: AdGuard almacena métricas de rendimiento agregadas de sus servidores DNS, es decir, el número de solicitudes completas a un servidor en particular, el número de solicitudes bloqueadas, y la velocidad de procesamiento de solicitudes. They also keep and store the database of domains requested within the last 24 hours.

    > We need this information to identify and block new trackers and threats. We also log how many times this or that tracker has been blocked. We need this information to remove outdated rules from our filters.

    AdGuard DNS: [*Privacy Policy*](https://adguard-dns.io/en/privacy.html) [^2]: Cloudflare collects and stores only the limited DNS query data that is sent to the 1.1.1.1 resolver. The 1.1.1.1 resolver service does not log personal data, and the bulk of the limited non-personally identifiable query data is stored only for 25 hours.

    1.1.1.1 Public DNS Resolver: [*Cloudflare’s commitment to privacy*](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) [^3]: Control D only logs specific account data for Premium resolvers with custom DNS profiles. Free resolvers do not retain any data.

    Control D: [*Privacy Policy*](https://controld.com/privacy) [^4]: DNS0.eu collects some data for their threat intelligence feeds to monitor for newly registered/observed/active domains and other bulk data. Esos datos se comparten con algunos [socios](https://docs.dns0.eu/data-feeds/introduction) para, por ejemplo, investigaciones de seguridad. They do not collect any personally identifiable information.

    DNS0.eu: [*Privacy Policy*](https://dns0.eu/privacy) [^5]: Mullvad's DNS service is available to both subscribers and non-subscribers of Mullvad VPN. Su política de privacidad afirma explícitamente que no registran solicitudes DNS de ninguna manera.

    Mullvad: [*No-logging of user activity policy*](https://mullvad.net/en/help/no-logging-data-policy) [^6]: Quad9 collects some data for the purposes of threat monitoring and response. That data may then be remixed and shared for purposes like furthering their security research. Quad9 no colecciona ni registra direcciones IP ni otros datos que consideren personalmente identificables.

    Quad9: [*Data and Privacy Policy*](https://quad9.net/privacy/policy)
