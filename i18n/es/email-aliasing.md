---
title: Alias de correo electrónico
icon: material/email-lock
description: Un servicio de alias de correo electrónico te permite generar con facilidad una nueva dirección de correo electrónico para cada sitio web en el que te registras.
cover: email-aliasing.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-account-search: Public Exposure](basics/common-threats.md#limiting-public-information){ .pg-green }

An **email aliasing service** allows you to easily generate a new email address for every website you register for. Los alias de correo electrónico que generas son reenviados a una dirección de correo electrónico de tu elección, ocultando tanto tu dirección "principal" de correo electrónico como la identidad de tu [proveedor de correo electrónico](email.md). El verdadero alias de correo electrónico es mejor que el direccionamiento plus, comúnmente utilizado y admitido por muchos proveedores, que permite crear alias como `su nombre+[cualquiercosaaquí]@ejemplo.com`, porque los sitios web, los anunciantes y las redes de seguimiento pueden eliminar trivialmente cualquier cosa después del signo `+`. Organizaciones como la [IAB](https://en.wikipedia.org/wiki/Interactive_Advertising_Bureau) solicitan que los anunciantes [normalicen las direcciones de correo electrónico](https://shkspr.mobi/blog/2023/01/the-iab-loves-tracking-users-but-it-hates-users-tracking-them) para poder correlacionarlas y rastrearlas, sin importar las preferencias de privacidad de los usuarios.

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
- Temporary email services typically have public mailboxes which can be accessed by anyone who knows the address, while aliases are private to you.

Our email aliasing recommendations are providers that allow you to create aliases on domains they control, as well as on your own custom domain(s) for a modest yearly fee. Estos pueden ser autoalojados si deseas tener el máximo control. Sin embargo, usar un dominio personalizado puede tener inconvenientes relacionados con la privacidad: Si eres la única persona usando tu dominio personalizado, tus acciones pueden ser rastreadas con facilidad a través de los sitios web, simplemente con el nombre del dominio en la dirección de correo electrónico e ignorando todo lo que se encuentre antes del signo de (@).

Usar un servicio de alias requiere confiar tus mensajes sin encriptar a tu proveedor de correo electrónico y tu proveedor de alias. Some providers mitigate this slightly with automatic PGP encryption[^1], which reduces the number of parties you need to trust from two to one by encrypting incoming emails before they are delivered to your final mailbox provider.

### addy.io

<div class="admonition recommendation" markdown>

![addy.io logo](assets/img/email-aliasing/addy.svg){ align=right }

**addy.io** lets you create 10 domain aliases on a shared domain for free, or unlimited "standard" aliases.

[:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://addy.io/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

El número de alias compartidos (finalizan en un dominio compartido como @addy.io) que puedes crear está limitado a 10 en el plan gratuito de addy.io, 50 en el plan de 1$/mes e ilimitado en el plan de 4$/mes (facturado en 3$ por un año). You can create unlimited standard aliases which end in a domain like @[username].addy.io or a custom domain on paid plans. However, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. Estos son útiles cuando un dominio compartido puede estar bloqueado por un servicio. Securitum [auditó](https://addy.io/blog/addy-io-passes-independent-security-audit) addy.io en septiembre de 2023 y no [se identificaron] vulnerabilidades significativas(https://addy.io/addy-io-security-audit.pdf).

Funciones gratuitas destacables:

- [x] 10 Alias Compartidos
- [x] Alias Estándar Ilimitados
- [ ] No Hay Respuestas Salientes
- [x] 1 Buzón de Destinatario
- [x] Automatic PGP Encryption[^1]

If you cancel your subscription, you will still enjoy the features of your paid plan until the billing cycle ends. After the end of your current billing cycle, most paid features (including any custom domains) will be [deactivated](https://addy.io/faq/#what-happens-if-i-have-a-subscription-but-then-cancel-it), paid account settings will be reverted to their defaults, and catch-all will be enabled if it was previously disabled.

### SimpleLogin

<div class="admonition recommendation" markdown>

![Simplelogin logo](assets/img/email-aliasing/simplelogin.svg){ align=right }

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

Puedes vincular tu cuenta SimpleLogin en la configuración con tu cuenta Proton. If you have the Proton Unlimited plan or any multi-user Proton plan, you will have SimpleLogin Premium for free.

Funciones gratuitas destacables:

- [x] 10 Alias Compartidos
- [x] Respuestas Ilimitadas
- [x] 1 Buzón de Destinatario
- [ ] Automatic PGP Encryption[^1] is only available on paid plans

When your subscription ends, all aliases you created will still be able to receive and send emails. However, you cannot create any new aliases that would exceed the free plan limit, nor can you add a new domain, directory, or mailbox.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proveedores que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), evaluamos los proveedores de correo electrónico con el mismo estándar que nuestros [criterios de proveedor de correo electrónico](email.md#criteria) donde corresponda. Sugerimos que te familiarices con esta lista antes de decidir utilizar un servicio de correo electrónico y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

[^1]: Automatic PGP encryption allows you to encrypt non-encrypted incoming emails before they are forwarded to your mailbox, making sure your primary mailbox provider never sees unencrypted email content.
