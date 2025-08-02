---
title: "Solucionadores DNS"
icon: material/dns
description: Te recomendamos que elijas estos proveedores de DNS cifrado para sustituir la configuración predeterminada de tu ISP.
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

Estos son nuestros solucionadores de DNS públicos favoritos en función de sus características de privacidad y seguridad, y de su rendimiento en todo el mundo. Algunos de estos servicios ofrecen un bloqueo básico a nivel de DNS de malware o rastreadores en función del servidor que elijas, pero si quieres poder ver y personalizar lo que se bloquea, deberías utilizar en su lugar un producto de filtrado DNS dedicado.

| Proveedor de DNS                                                           | Protocolos                                                                    | Logs / Política de Privacidad | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | Filtrado                                                                                                                                                                   | Perfil de Apple firmado                                                                                                                                                                                                    |
| -------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard Public DNS**](https://adguard-dns.io/en/public-dns.html)        | Texto en claro <br>DoH/3 <br>DoT <br>DoQ <br>DNSCrypt | Anónimo[^1]                   | Anónimo                                                        | Basado en la elección del servidor. La lista de filtros utilizada se puede encontrar aquí. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardSDNSFilter) | Sí [:octicons-link-external-24:](https://adguard-dns.io/en/blog/encrypted-dns-ios-14.html)                                                                                                                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | Texto en claro <br>DoH/3 <br>DoT                                  | Anónimo[^2]                   | No                                                             | Basado en la elección del servidor.                                                                                                                                        | No [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846)                                                                                                   |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | Texto en claro <br>DoH/3 <br>DoT <br>DoQ                    | No[^3]                        | No                                                             | Basado en la elección del servidor.                                                                                                                                        | Sí <br>[:simple-apple: iOS](https://docs.controld.com/docs/ios-platform) <br>[:material-apple-finder: macOS](https://docs.controld.com/docs/macos-platform#manual-setup-profile)                               |
| [**DNS0.eu**](https://dns0.eu)                                             | Texto en claro <br>DoH/3 <br>DoH <br>DoT <br>DoQ      | Anónimo[^4]                   | Anónimo                                                        | Basado en la elección del servidor.                                                                                                                                        | Sí [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                                                                                                                                |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | DoH <br>DoT                                                             | No[^5]                        | No                                                             | Basado en la elección del servidor. La lista de filtros utilizada se puede encontrar aquí. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)           | Sí [:octicons-link-external-24:](https://github.com/mullvad/encrypted-dns-profiles)                                                                                                                                        |
| [**Quad9**](https://quad9.net)                                             | Texto en claro <br>DoH <br>DoT <br>DNSCrypt                 | Anónimo[^6]                   | Opcional                                                       | Basado en la elección del servidor. El bloqueo de malware está incluido por defecto.                                                                                       | Sí <br>[:simple-apple: iOS](https://docs.quad9.net/Setup_Guides/iOS/iOS_14_and_later_(Encrypted)) <br>[:material-apple-finder: macOS](https://docs.quad9.net/Setup_Guides/MacOS/Big_Sur_and_later_(Encrypted)) |

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
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Política de privacidad" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Código fuente" }inicio

</details>

</div>

## Filtrado DNS basado en la nube

Estas soluciones de filtrado DNS ofrecen un panel web en el que puedes personalizar las listas de bloqueo según tus necesidades exactas, de forma similar a un Pi-hole. Estos servicios suelen ser más fáciles de instalar y configurar que los autoalojados, como los anterioriores, y pueden utilizarse más fácilmente en múltiples redes (las soluciones autoalojadas suelen estar restringidas a su red doméstica/local, a menos que se establezca una configuración más avanzada).

### Control D

<div class="admonition recommendation" markdown>

![Control D logo](assets/img/dns/control-d.svg){ align=right }

**Control D** es un servicio DNS personalizable que permite bloquear amenazas de seguridad, contenidos no deseados y publicidad a nivel de DNS. Además de sus planes de pago, ofrecen una serie de solucionadores DNS preconfigurados que puedes utilizar gratuitamente.

[:octicons-home-16: Página Principal](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

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

[:octicons-home-16: Página Principal](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)
- [:fontawesome-brands-windows: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)

</details>

</div>

Cuando se utiliza con una cuenta, NextDNS habilitará las funciones de información y registro de forma predeterminada (ya que algunas funciones lo requieren). Puedes elegir los tiempos de retención y las ubicaciones de almacenamiento de los registros que desees conservar.

El plan gratuito de NextDNS es totalmente funcional, pero no se debe confiar en él para aplicaciones de seguridad u otras aplicaciones de filtrado críticas, ya que después de 300.000 consultas DNS en un mes se desactivan todas las funciones de filtrado, registro y otras funciones basadas en la cuenta. Se puede seguir utilizando como un proveedor DNS normal después de ese punto, por lo que tus dispositivos seguirán funcionando y haciendo consultas seguras a través de DNS sobre HTTPS (DoH), solo que sin tus listas de filtros.

NextDNS también ofrece un servicio DoH público en `https://dns.nextdns.io` y DNS sobre TLS/QUIC (DoT/DoQ) en `dns.nextdns.io`, que están disponibles por defecto en Firefox y Chromium, y sujetos a su [política de privacidad](https://nextdns.io/privacy) por defecto, sin registro.

## Proxies DNS Cifrados

El software de proxy de DNS cifrado proporciona un proxy local para que el solucionador DNS [no cifrado](advanced/dns-overview.md#unencrypted-dns) lo reenvíe. Normalmente, se utiliza en plataformas que no soportan [DNS cifrado](advanced/dns-overview.md#what-is-encrypted-dns) de forma nativa.

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** es un cliente Android de código abierto que soporta [DoH](advanced/dns-overview.md#dns-over-https-doh), [DoT](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) y Proxy DNS. También proporciona funciones adicionales, como el almacenamiento en caché de las respuestas DNS, el registro local de las consultas DNS y el uso de la aplicación como cortafuegos.

[:octicons-home-16: Página Principal](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Descargas</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

Aunque RethinkDNS ocupa el espacio VPN de Android, puedes seguir utilizando una VPN u Orbot con la aplicación [añadiendo una configuración de WireGuard](https://docs.rethinkdns.com/proxy/wireguard) o [configurando manualmente Orbot como servidor Proxy](https://docs.rethinkdns.com/firewall/orbot), respectivamente.

### DNSCrypt-Proxy

<div class="admonition recommendation" markdown>

![DNSCrypt-Proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**DNSCrypt-Proxy** es un proxy DNS compatible con [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DoH](advanced/dns-overview.md#dns-over-https-doh), y [DNS Anónimo](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

[:octicons-repo-16: Repositorio](https://github.com/DNSCrypt/dnscrypt-proxy#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title="Contribuir " }

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

Todos los productos DNS...

- Deben admitir [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- Debe admitir la [Minimización de QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- Deben anonimizar [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) o desactivarlo por defecto.

Además, todos los proveedores públicos...

- No deben registrar datos personales en el disco.
    - Como se indica en las notas a pie de página, algunos proveedores recopilan información de consulta con fines como la investigación de seguridad, pero en ese caso los datos no deben asociarse a ninguna PII, como la dirección IP, etc.
- Deberían admitir [anycast](https://en.wikipedia.org/wiki/Anycast) o geo-steering.

[^1]: AdGuard almacena métricas de rendimiento agregadas de sus servidores DNS, es decir, el número de solicitudes completas a un servidor en particular, el número de solicitudes bloqueadas, y la velocidad de procesamiento de solicitudes. También guarda y almacena la base de datos de dominios solicitados en las últimas 24 horas.

    > Necesitamos esta información para identificar y bloquear nuevos rastreadores y amenazas. También registramos cuántas veces se ha bloqueado tal o cual rastreador. Necesitamos esta información para eliminar reglas obsoletas de nuestros filtros.

    AdGuard DNS: [*Política de Privacidad*](https://adguard-dns.io/en/privacy.html) [^2]: Cloudflare recopila y almacena únicamente los datos de consulta DNS limitados que se envían al solucionador 1.1.1.1. El servicio de resolución 1.1.1.1 no registra datos personales, y el grueso de los limitados datos de consulta no identificables personalmente se almacena solo durante 25 horas.

    1.1.1.1 Solucionador de DNS Público: [*El compromiso de Cloudflare con la privacidad*](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) [^3]: Control D solo registra datos específicos de la cuenta para los solucionadores Premium con perfiles DNS personalizados. Los solucionadores gratuitos no conservan ningún dato.

    Control D: [*Política de Privacidad*](https://controld.com/privacy) [^4]: DNS0.eu recoge algunos datos para sus fuentes de inteligencia de amenazas para monitorizar dominios recién registrados/observados/activos y otros datos masivos. Esos datos se comparten con algunos [socios](https://docs.dns0.eu/data-feeds/introduction) para, por ejemplo, investigaciones de seguridad. No recopilan información personal identificable.

    DNS0.eu: [*Política de Privacidad*](https://dns0.eu/privacy) [^5]: El servicio DNS de Mullvad está disponible tanto para suscriptores como para no suscriptores de Mullvad VPN. Su política de privacidad afirma explícitamente que no registran solicitudes DNS de ninguna manera.

    Mullvad: [*Política de no registro de la actividad de los usuarios*](https://mullvad.net/en/help/no-logging-data-policy) [^6]: Quad9 recopila algunos datos con fines de supervisión y respuesta ante amenazas. Esos datos pueden remezclarse y compartirse con fines como el fomento de sus investigaciones de seguridad. Quad9 no colecciona ni registra direcciones IP ni otros datos que consideren personalmente identificables.

    Quad9: [*Política de Datos y Privacidad*](https://quad9.net/privacy/policy)
