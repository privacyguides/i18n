---
title: Alias de correo electrónico
icon: material/email-lock
description: Un servicio de alias de correo electrónico te permite generar con facilidad una nueva dirección de correo electrónico para cada sitio web en el que te registras.
cover: email-aliasing.webp
---

Un servicio de alias de correo electrónico te permite generar con facilidad una nueva dirección de correo electrónico para cada sitio web en el que te registras. Los alias de correo electrónico que generas son reenviados a una dirección de correo electrónico de tu elección, ocultando tanto tu dirección "principal" de correo electrónico y la identidad de tu [proveedor de correo electrónico](email.md). True email aliasing is better than plus addressing commonly used and supported by many providers, which allows you to create aliases like `yourname+[anythinghere]@example.com`, because websites, advertisers, and tracking networks can trivially remove anything after the `+` sign. Organizaciones como la [IAB](https://en.wikipedia.org/wiki/Interactive_Advertising_Bureau) solicitan que los anunciantes [normalicen las direcciones de correo electrónico](https://shkspr.mobi/blog/2023/01/the-iab-loves-tracking-users-but-it-hates-users-tracking-them) para poder correlacionarlas y rastrearlas, sin importar las preferencias de privacidad de los usuarios.

<div class="grid cards" markdown>

- ![addy.io logo](assets/img/email-aliasing/addy.svg){ .twemoji } [addy.io](email.md#addyio)
- ![SimpleLogin logo](assets/img/email-aliasing/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

Los alias de correo electrónico también pueden servir de respaldo en caso de que tu proveedor de correo electrónico cese sus operaciones. En dicho escenario, fácilmente puedes redirigir tus alias a una nueva dirección de correo electrónico. A su vez, sin embargo, estás confiando en que tu servicio de alias continúe funcionando.

El uso de un servicio dedicado de alias de correo electrónico también tiene una cantidad de beneficios sobre un alias general en un dominio personalizado:

- Los alias se pueden activar y desactivar individualmente cuando lo necesites, evitando que los sitios web te envíen correos electrónicos al azar.
- Las respuestas son enviadas desde la dirección del alias, ocultando tu dirección real de correo electrónico.

También tienen una cantidad de beneficios sobre los servicios "temporales de correo electrónico":

- Los alias son permanentes y pueden ser activados nuevamente si necesitas recibir algo como un reseteo de la contraseña.
- Los correos electrónicos son enviados a tu buzón de confianza, en vez de ser almacenados por el proveedor de los alias.
- Los servicios temporales de correo electrónico por lo general tienen buzones públicos a los que puede acceder cualquier persona que conozca la dirección, los alias son privados para ti.

Nuestras recomendaciones para la generación de alias de correo electrónico son proveedores que te permiten crear alias en los dominios que controlan, al igual que tu propio dominio(s) por una cómoda tarifa anual. Estos pueden ser autoalojados si deseas tener el máximo control. Sin embargo, usar un dominio personalizado puede tener inconvenientes relacionados con la privacidad: Si eres la única persona usando tu dominio personalizado, tus acciones pueden ser rastreadas con facilidad a través de los sitios web, simplemente con el nombre del dominio en la dirección de correo electrónico e ignorando todo lo que se encuentre antes del signo de (@).

Usar un servicio de alias requiere confiar tus mensajes sin encriptar a tu proveedor de correo electrónico y tu proveedor de alias. Algunos proveedores mitigan esto ligeramente con el uso de la Encriptación Automática de PGP, que reduce la cantidad de partes en las que necesitas confiar de dos a una, al encriptar tus correos electrónicos entrantes antes de que sean entregados al buzón de tu proveedor final.

### addy.io

<div class="admonition recommendation" markdown>

![addy.io logo](assets/img/email-aliasing/addy.svg){ align=right }

**addy.io** lets you create 10 domain aliases on a shared domain for free, or unlimited "standard" aliases which are less anonymous.

[:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://app.addy.io/docs){ .card-link title=Documentation}
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

The number of shared aliases (which end in a shared domain like @addy.io) that you can create is limited to 10 on addy.io's free plan, 50 on their $1/month plan and unlimited on the $4/month plan (billed $3 for a year). You can create unlimited standard aliases (which end in a domain like @[username].addy.io or a custom domain on paid plans), however, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. They are useful where a shared domain might be blocked by a service. Securitum [audited](https://addy.io/blog/addy-io-passes-independent-security-audit) addy.io in September 2023 and no significant vulnerabilities [were identified](https://addy.io/addy-io-security-audit.pdf).

Notable free features:

- [x] 10 Shared Aliases
- [x] Unlimited Standard Aliases
- [ ] No Outgoing Replies
- [x] 1 Recipient Mailbox
- [x] Automatic PGP Encryption

### SimpleLogin

<div class="admonition recommendation" markdown>

![Simplelogin logo](assets/img/email-aliasing/simplelogin.svg){ align=right }

**SimpleLogin** is a free service which provides email aliases on a variety of shared domain names, and optionally provides paid features like unlimited aliases and custom domains.

[:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

</details>

</div>

SimpleLogin was [acquired by Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) as of April 8, 2022. If you use Proton Mail for your primary mailbox, SimpleLogin is a great choice. As both products are now owned by the same company you now only have to trust a single entity. We also expect that SimpleLogin will be more tightly integrated with Proton's offerings in the future. SimpleLogin continues to support forwarding to any email provider of your choosing. Securitum [audited](https://simplelogin.io/blog/security-audit) SimpleLogin in early 2022 and all issues [were addressed](https://simplelogin.io/audit2022/web.pdf).

You can link your SimpleLogin account in the settings with your Proton account. If you have the Proton Unlimited, Business, or Visionary Plan, you will have SimpleLogin Premium for free.

Notable free features:

- [x] 10 Shared Aliases
- [x] Unlimited Replies
- [x] 1 Recipient Mailbox
- [ ] Automatic PGP Encryption is only available on paid plans

## Criterios

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we evaluate email aliasing providers to the same standard as our regular [email provider criteria](email.md#criteria) where applicable. We suggest you familiarize yourself with this list before choosing an email service, and conduct your own research to ensure the provider you choose is the right choice for you.

\*[Automatic PGP Encryption]: Allows you to encrypt non-encrypted incoming emails before they are forwarded to your mailbox, making sure your primary mailbox provider never sees unencrypted email content.
