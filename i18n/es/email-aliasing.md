---
title: Alias de correo electrónico
icon: material/email-lock
description: Un servicio de alias de correo electrónico te permite generar con facilidad una nueva dirección de correo electrónico para cada sitio web en el que te registras.
cover: email-aliasing.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-account-search: Exposición Pública](basics/common-threats.md#limiting-public-information){ .pg-green }

Un **servicio de alias de correo electrónico** te permite generar fácilmente una nueva dirección de correo electrónico para cada sitio web en el que te registres. Los alias de correo electrónico que generas son reenviados a una dirección de correo electrónico de tu elección, ocultando tanto tu dirección "principal" de correo electrónico como la identidad de tu [proveedor de correo electrónico](email.md). El verdadero alias de correo electrónico es mejor que el direccionamiento plus, comúnmente utilizado y admitido por muchos proveedores, que permite crear alias como `su nombre+[cualquiercosaaquí]@ejemplo.com`, porque los sitios web, los anunciantes y las redes de seguimiento pueden eliminar trivialmente cualquier cosa después del signo `+`. Organizaciones como la [IAB](https://en.wikipedia.org/wiki/Interactive_Advertising_Bureau) solicitan que los anunciantes [normalicen las direcciones de correo electrónico](https://shkspr.mobi/blog/2023/01/the-iab-loves-tracking-users-but-it-hates-users-tracking-them) para poder correlacionarlas y rastrearlas, sin importar las preferencias de privacidad de los usuarios.

<div class="grid cards" markdown>

- ![addy.io logo](assets/img/email-aliasing/addy.svg){ .twemoji } [addy.io](email-aliasing.md#addyio)
- ![SimpleLogin logo](assets/img/email-aliasing/simplelogin.svg){ .twemoji } [SimpleLogin](email-aliasing.md#simplelogin)

</div>

Los alias de correo electrónico también pueden servir de respaldo en caso de que tu proveedor de correo electrónico cese sus operaciones. En dicho escenario, fácilmente puedes redirigir tus alias a una nueva dirección de correo electrónico. A su vez, sin embargo, estás confiando en que tu servicio de alias continúe funcionando.

El uso de un servicio dedicado de alias de correo electrónico también tiene una cantidad de beneficios sobre un alias general en un dominio personalizado:

- Los alias se pueden activar y desactivar individualmente cuando lo necesites, evitando que los sitios web te envíen correos electrónicos al azar.
- Las respuestas son enviadas desde la dirección del alias, ocultando tu dirección real de correo electrónico.

También tienen una cantidad de beneficios sobre los servicios "temporales de correo electrónico":

- Los alias son permanentes y pueden ser activados nuevamente si necesitas recibir algo como un reseteo de la contraseña.
- Los correos electrónicos son enviados a tu buzón de confianza, en vez de ser almacenados por el proveedor de los alias.
- Los servicios de correo electrónico temporal suelen tener buzones públicos a los que puede acceder cualquiera que conozca la dirección, mientras que los alias son privados para ti.

Nuestras recomendaciones de alias de correo electrónico son proveedores que te permiten crear alias en dominios que ellos controlan, así como en tu(s) propio(s) dominio(s) personalizado(s) por una módica cuota anual. Estos pueden ser autoalojados si deseas tener el máximo control. Sin embargo, usar un dominio personalizado puede tener inconvenientes relacionados con la privacidad: Si eres la única persona usando tu dominio personalizado, tus acciones pueden ser rastreadas con facilidad a través de los sitios web, simplemente con el nombre del dominio en la dirección de correo electrónico e ignorando todo lo que se encuentre antes del signo de (@).

Usar un servicio de alias requiere confiar tus mensajes sin encriptar a tu proveedor de correo electrónico y tu proveedor de alias. Algunos proveedores mitigan esto ligeramente con el cifrado automático PGP[^1], que reduce el número de partes en las que tienes que confiar de dos a una al cifrar los correos entrantes antes de que lleguen a tu proveedor de buzón final.

### addy.io

<div class="admonition recommendation" markdown>

![addy.io logo](assets/img/email-aliasing/addy.svg){ align=right }

**addy.io** te permite crear 10 alias de dominio en un dominio compartido de forma gratuita, o alias "estándar" ilimitados.

[:octicons-home-16: Página Principal](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Politica de Privacidad" }
[:octicons-info-16:](https://addy.io/faq){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

El número de alias compartidos (finalizan en un dominio compartido como @addy.io) que puedes crear está limitado a 10 en el plan gratuito de addy.io, 50 en el plan de 1$/mes e ilimitado en el plan de 4$/mes (facturado en 3$ por un año). You can pay for these plans using [cryptocurrency](https://addy.io/help/subscribing-with-cryptocurrency) or purchase a voucher code from [ProxyStore](https://addy.io/help/voucher-codes), addy.io's official reseller.

Puedes crear un número ilimitado de alias estándar que terminen en un dominio como @[nombredeusuario].addy.io o un dominio personalizado en los planes de pago. Sin embargo, como ya se ha mencionado, esto puede ir en detrimento de la privacidad porque la gente puede relacionar trivialmente tus alias estándar basándose únicamente en el nombre de dominio. Estos son útiles cuando un dominio compartido puede estar bloqueado por un servicio. Securitum [auditó](https://addy.io/blog/addy-io-passes-independent-security-audit) addy.io en septiembre de 2023 y no [se identificaron] vulnerabilidades significativas(https://addy.io/addy-io-security-audit.pdf).

Funciones gratuitas destacables:

- [x] 10 Alias Compartidos
- [x] Alias Estándar Ilimitados
- [ ] No Hay Respuestas Salientes
- [x] 1 Buzón de Destinatario
- [x] Cifrado PGP Automático[^1]

Si cancelas tu suscripción, disfrutarás de las características de tu plan de pago hasta que finalice el ciclo de facturación. Una vez finalizado el ciclo de facturación actual, la mayoría de las funciones de pago (incluidos los dominios personalizados) se [desactivarán](https://addy.io/faq/#what-happens-if-i-have-a-subscription-but-then-cancel-it), la configuración de las cuentas de pago se restablecerá a sus valores predeterminados y se activará la función catch-all si anteriormente estaba desactivada.

### SimpleLogin

<div class="admonition recommendation" markdown>

![SimpleLogin logo](assets/img/email-aliasing/simplelogin.svg){ align=right }

**SimpleLogin** es un servicio gratuito que proporciona alias de correo electrónico en una variedad de nombres de dominio compartidos y, opcionalmente, ofrece funciones de pago como alias ilimitados y dominios personalizados.

[:octicons-home-16: Página Principal](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="Politica de Privacidad" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin fue [adquirido por Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) el 8 de abril de 2022. Si utilizas Proton Mail para tu buzón principal, SimpleLogin es una gran elección. Como ambos productos pertenecen ahora a la misma empresa, ahora sólo tienes que confiar en una única entidad. También esperamos que SimpleLogin se integre más estrechamente con las ofertas de Proton en el futuro. SimpleLogin sigue siendo compatible con el reenvío a cualquier proveedor de correo electrónico de tu elección. Securitum [auditó](https://simplelogin.io/blog/security-audit) SimpleLogin a principios de 2022 y todos los problemas [se solucionaron](https://simplelogin.io/audit2022/web.pdf).

Puedes vincular tu cuenta SimpleLogin en la configuración con tu cuenta Proton. If you have Proton Pass Plus, Proton Unlimited, or any multi-user Proton plan, you will have SimpleLogin Premium for free.

You can also purchase a voucher code for SimpleLogin Premium anonymously via their official reseller, [ProxyStore](https://simplelogin.io/faq).

Funciones gratuitas destacables:

- [x] 10 Alias Compartidos
- [x] Respuestas Ilimitadas
- [x] 1 Buzón de Destinatario
- [ ] El Cifrado PGP Automático[^1] solo está disponible en los planes de pago

Cuando finalice tu suscripción, todos los alias que hayas creado podrán seguir recibiendo y enviando mensajes de correo electrónico. Sin embargo, no puedes crear ningún alias nuevo que supere el límite del plan gratuito, ni puedes añadir un nuevo dominio, directorio o buzón.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proveedores que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), evaluamos los proveedores de correo electrónico con el mismo estándar que nuestros [criterios de proveedor de correo electrónico](email.md#criteria) donde corresponda. Sugerimos que te familiarices con esta lista antes de decidir utilizar un servicio de correo electrónico y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

[^1]: El cifrado PGP automático te permite cifrar correos electrónicos entrantes no cifrados antes de que sean enviados a tu buzón de correo, asegurándote de que tu proveedor principal de buzón nunca vea contenido de correo electrónico no cifrado.
