---
title: "Autenticación de Múltiples Factores"
icon: 'material/two-factor-authentication'
description: Estas herramientas te ayudan a proteger tus cuentas de Internet con la autenticación multifactor sin enviar tus secretos a terceros.
cover: multi-factor-authentication.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-target-account: Ataques dirigidos](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">Llaves Físicas</p>

Las [recomendaciones sobre llaves de seguridad físicas](security-keys.md) se han movido a su propia categoría.

</div>

Las **Aplicaciones de Autenticación Multifactor** aplican una norma de seguridad adoptada por el Grupo de Trabajo de Ingeniería de Internet (IETF) denominada **contraseñas de un solo uso basadas en el tiempo**, o **TOTP**. Se trata de un método en el que los sitios web comparten un secreto con usted que es utilizado por su aplicación de autenticación para generar un código de seis dígitos (normalmente) basado en la hora actual, que introduce al iniciar sesión para que el sitio web lo compruebe. Normalmente, estos códigos se regeneran cada 30 segundos, y una vez que se genera uno nuevo, el anterior queda inutilizado. Incluso si un pirata informático consigue un código de seis dígitos, no hay forma de que invierta ese código para obtener el secreto original ni de que pueda predecir cuáles serán los códigos futuros.

Recomendamos encarecidamente que utilice aplicaciones TOTP para móviles en lugar de alternativas de escritorio, ya que Android e iOS tienen mejor seguridad y aislamiento de aplicaciones que la mayoría de los sistemas operativos de escritorio.

## Ente Auth

<div class="admonition recommendation" markdown>

![Ente Auth logo](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**Ente Auth** es una aplicación gratuita y de código abierto que almacena y genera tokens TOTP. Esta permite utilizar una cuenta en línea para realizar copias de seguridad y sincronizar sus tokens entre sus dispositivos (y accesarlos por medio de una interfaz web) de una manera secura y cifrada de extremo a extremo. También se puede utilizar sin conexión a Internet en un único dispositivo sin la necesidad de una cuenta.

[:octicons-home-16: Página Principal](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://help.ente.io/auth){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

## Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** es una aplicación gratuita y de código abierto para gestionar sus tokens para la verificación de 2 pasos de sus servicios en línea. Aegis Authenticator funciona completamente sin conexión/localmente, pero incluye una opción para exportar sus tokens para respaldarlos, a diferencia de otras alternativas.

[:octicons-home-16: Página Principal](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

<!-- markdownlint-disable-next-line -->
## Criterios

**Por favor, tenga en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de decidir utilizar un proyecto y realizar su propia investigación para asegurarse de que es la elección ideal para usted.

- El código fuente debe estar a disposición del público.
- No debe requerir conexión a Internet.
- La sincronización con la nube debe ser opcional, y (si está disponible) la funcionalidad de sincronización debe ser E2EE.
