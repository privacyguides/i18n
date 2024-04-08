---
title: "Resolvedores de DNS"
icon: material/dns
description: Estos son algunos proveedores de DNS cifrado a los que recomendamos cambiar para reemplazar la configuración por defecto de tu proveedor de servicios de internet.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

Un DNS encriptado con servidores de terceros solo debe utilizarse para evitar el [bloqueo de DNS básico](https://en.wikipedia.org/wiki/DNS_blocking) cuándo puedas estar seguro de que no habrá ningunas consecuencias. Un DNS encriptado no te ayudará a esconder ninguna de tu actividad en línea.

[Aprende más sobre DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Proveedores Recomendados

Estos son nuestros resolvedores de DNS públicos favoritos en función de sus características de privacidad y seguridad, y de su rendimiento en todo el mundo. Algunos de estos servicios ofrecen un bloqueo básico a nivel de DNS de malware o rastreadores en función del servidor que elijas, pero si quieres poder ver y personalizar lo que se bloquea, deberías utilizar en su lugar un producto de filtrado DNS dedicado.

| Proveedor de DNS                                                           | Política de Privacidad                                                                               | Protocolos                               | Registro     | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | Filtrado                                                                                                                                                         | Signed Apple Profile                                                                                                     |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------- | ------------ | -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext   DoH/3   DoT   DoQ   DNSCrypt | Algún[^1]    | Anonymized                                                     | Based on server choice. La lista de filtros siendo utilizada se puede encontrar aquí. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS)   | Yes [:octicons-link-external-24:](https://adguard.com/en/blog/encrypted-dns-ios-14.html)                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Cleartext   DoH/3   DoT                  | Algún[^2]    | No                                                             | Based on server choice.                                                                                                                                          | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846) |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Cleartext   DoH/3   DoT   DoQ            | Opcional[^3] | No                                                             | Based on server choice.                                                                                                                                          | Yes [:octicons-link-external-24:](https://docs.controld.com/docs/macos-platform)                                         |
| [**dns0.eu**](https://dns0.eu)                                             | [:octicons-link-external-24:](https://dns0.eu/privacy)                                               | Cleartext   DoH/3   DoH   DoT   DoQ      | No           | Anonymized                                                     | Based on server choice.                                                                                                                                          | Yes [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                             |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH   DoT                                | No[^4]       | No                                                             | Based on server choice. La lista de filtro que se está utilizando se puede encontrar aquí. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock) | Yes [:octicons-link-external-24:](https://mullvad.net/en/blog/profiles-to-configure-our-encrypted-dns-on-apple-devices)  |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Cleartext   DoH   DoT   DNSCrypt         | Some[^5]     | Opcional                                                       | Based on server choice, malware blocking by default.                                                                                                             | Yes [:octicons-link-external-24:](https://quad9.net/news/blog/ios-mobile-provisioning-profiles)                          |

## Self-Hosted DNS Filtering

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

[:octicons-home-16: Página de Inicio](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Politica de privacidad" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Código fuente" }

</details>

</div>

## Cloud-Based DNS Filtering

These DNS filtering solutions offer a web dashboard where you can customize the blocklists to your exact needs, similarly to a Pi-hole. These services are usually easier to set up and configure than self-hosted services like the ones above, and can be used more easily across multiple networks (self-hosted solutions are typically restricted to your home/local network unless you set up a more advanced configuration).

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** es un servicio DNS personalizable que permite bloquear amenazas de seguridad, contenidos no deseados y publicidad a nivel de DNS. Además de sus planes de pago, ofrecen una serie de resolvedores DNS preconfigurados que puedes utilizar gratuitamente.

[:octicons-home-16: Página Principal](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-windows11: Windows](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: Linux](https://docs.controld.com/docs/ctrld)
- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: App Store](https://apps.apple.com/app/1518799460)
- [:simple-github: GitHub](https://github.com/Control-D-Inc/ctrld/releases/tag/v1.3.5)

</details>

</div>

### NextDNS

<div class="admonition recommendation" markdown>

![NextDNS logo](assets/img/dns/nextdns.svg){ align=right }

 **NextDNS** es un servicio DNS personalizable que te permite bloquear amenazas de seguridad, contenidos no deseados y publicidad a nivel DNS. Ofrecen un plan gratuito totalmente funcional para uso limitado.

[:octicons-home-16: Página Principal](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-windows11: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)
- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)

</details>

</div>

Cuando se utiliza con una cuenta, NextDNS habilitará las funciones de información y registro de forma predeterminada (ya que algunas funciones lo requieren). Puedes elegir los tiempos de retención y las ubicaciones de almacenamiento de los registros que desees conservar.

El plan gratuito de NextDNS es totalmente funcional, pero no se debe confiar en él para aplicaciones de seguridad u otras aplicaciones de filtrado críticas, ya que después de 300.000 consultas DNS en un mes se deshabilitan todas las funciones de filtrado, registro y otras funciones basadas en la cuenta. Se puede seguir utilizando como un proveedor DNS normal después de ese punto, por lo que sus dispositivos seguirán funcionando y haciendo consultas seguras a través de DNS-sobre-HTTPS, solo que sin sus listas de filtros.

NextDNS también ofrece el servicio público DNS-sobre-HTTPS en `https://dns.nextdns.io` y DNS-sobre-TLS/QUIC en `dns.nextdns.io`, que están disponibles por defecto en Firefox y Chromium, y sujetos a su [política de privacidad](https://nextdns.io/privacy) de no-logging por defecto.

## Proxies DNS Cifrados

El software de proxy de DNS encriptado proporciona un proxy local para que el resolver DNS [no encriptado](advanced/dns-overview.md#unencrypted-dns) lo reenvíe. Normalmente, se utiliza en plataformas que no soportan [DNS cifrado](advanced/dns-overview.md#what-is-encrypted-dns) de forma nativa.

### RethinkDNS

<div class="admonition recommendation" markdown>

![Logo de RethinkDNS](assets/img/android/rethinkdns.svg#only-light){ align=right }
![Logo de RethinkDNS](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** es un cliente Android de código abierto que soporta [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) y DNS Proxy junto con el almacenamiento en caché de las respuestas DNS, el registro local de las consultas DNS y también se puede utilizar como cortafuegos.

[:octicons-home-16: Página Principal](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![logo dnscrypt-proxy](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt-proxy** es un proxy DNS con soporte para [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), y [DNS Anonimizado](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

<div class="admonition warning" markdown>
<p class="admonition-title">La función DNS anonimizado <a href="advanced/dns-overview.md#why-shouldnt-i0-use-encrypted-dns"><strong>no</strong></a> anonimiza otro tráfico de red.</p>
</div>

[:octicons-repo-16: Repositorio](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

## Criterios

**Ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten proporcionar recomendaciones objetivas. Te sugerimos que te familiarices con esta lista antes de elegir usar un proyecto, y que lleves a cabo tu propia investigación para asegurarte de que es la elección correcta para ti.

### Requisitos Mínimos

- [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [Minimización QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- Anonimizar [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) o desactivarlo por defecto.
- Preferir soporte [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) o soporte de dirección geográfica.

[^1]: AdGuard almacena métricas de rendimiento agregadas de sus servidores DNS, es decir, el número de solicitudes completas a un servidor en particular, el número de solicitudes bloqueadas, y la velocidad de procesamiento de solicitudes. También guardan y almacenan la base de datos de dominios solicitados dentro de las últimas 24 horas. "Necesitamos esta información para identificar y bloquear nuevos rastreadores y amenazas". "También registramos cuántas veces se ha bloqueado tal o cual rastreador. Necesitamos esta información para eliminar normas obsoletas de nuestros filtros". [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare recopila y almacena únicamente los datos de consulta DNS limitados que se envían al resolver 1.1.1.1. El servicio de resolución 1.1.1.1 no registra datos personales, y el grueso de los limitados datos de consulta no identificables personalmente se almacena solo durante 25 horas. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: El Control D solo registra los resolvers Premium con perfiles DNS personalizados. Los resolvers libres no registran datos. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: El servicio DNS de Mullvad está disponible tanto para suscriptores como para no suscriptores de Mullvad VPN. Su política de privacidad afirma explícitamente que no registran solicitudes DNS de ninguna manera. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: Quad9 recopila algunos datos con fines de monitorización y respuesta ante amenazas. Esos datos pueden remezclarse y compartirse, por ejemplo, con fines de investigación sobre seguridad. Quad9 no colecciona ni registra direcciones IP ni otros datos que consideren personalmente identificables. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
