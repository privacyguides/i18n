---
meta_title: The Best Android Operating Systems - Privacy Guides
title: Distribuciones alternativas
description: Puedes reemplazar el sistema operativo en tu teléfono Android por estas alternativas seguras y respetuosas con la privacidad.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Private Android Operating Systems
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: ./
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-target-account: Ataques Dirigidos](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataques Pasivos](../basics/common-threats.md#security-and-privacy){ .pg-orange }

A **custom Android-based operating system** (sometimes referred to as a **custom ROM**) can be a way to achieve a higher level of privacy and security on your device. This is in contrast to the "stock" version of Android which comes with your phone from the factory, and is often deeply integrated with Google Play Services as well as other vendor software.

We recommend installing GrapheneOS if you have a Google Pixel as it provides improved security hardening and additional privacy features. The reasons we don't list other operating systems or devices are as follows:

- They often have [weaker security](index.md#install-a-custom-distribution).
- Support is frequently dropped when the maintainer loses interest or upgrades their device, which is in contrast to the predictable [support cycle](https://grapheneos.org/faq#device-lifetime) that GrapheneOS follows.
- They generally have few or no notable privacy or security improvements that make installing them worthwhile.

## GrapheneOS

<div class="admonition recommendation" markdown>

![Logo de GrapheneOS](../assets/img/android/grapheneos.svg#only-light){ align=right }
![Logo de GrapheneOS](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** es la mejor opción cuando se trata de privacidad y seguridad.

GrapheneOS proporciona [mejoras adicionales de seguridad](https://en.wikipedia.org/wiki/Hardening_\(computing\)) y privacidad. Dispone de un [asignador de memoria reforzado](https://github.com/GrapheneOS/hardened_malloc), permisos de red y sensores, y otras diversas [características de seguridad](https://grapheneos.org/features). GrapheneOS también incluye actualizaciones completas de firmware y compilaciones firmadas, por lo que el arranque verificado es totalmente compatible.

[:octicons-home-16: Página Principal](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentación}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuir }

</div>

GrapheneOS es compatible con [Google Play aislado](https://grapheneos.org/usage#sandboxed-google-play), que ejecuta los servicios de Google Play totalmente aislados como cualquier otra aplicación normal. Esto significa que puedes aprovechar la mayoría de los servicios de Google Play, como las notificaciones push, a la vez que tienes un control total sobre sus permisos y accesos, y los limitas a un [perfil de trabajo](../os/android-overview.md#work-profile) o [perfil de usuario](../os/android-overview.md#user-profiles) específico de tu elección.

Los [teléfonos Google Pixel](../mobile-phones.md#google-pixel) son los únicos dispositivos que actualmente cumplen los [requisitos de seguridad de hardware] de GrapheneOS(https://grapheneos.org/faq#future-devices).

Por defecto, Android realiza muchas conexiones de red a Google para realizar comprobaciones de conectividad DNS, para sincronizar con la hora actual de la red, para comprobar tu conectividad de red y para muchas otras tareas en segundo plano. GrapheneOS los sustituye por conexiones a servidores operados por GrapheneOS y sujetos a su política de privacidad. Esto oculta información como tu dirección IP [de Google](../basics/common-threats.md#privacy-from-service-providers), pero significa que es trivial para un administrador de tu red o ISP ver que estás haciendo conexiones a `grapheneos.network`, `grapheneos.org`, etc. y deducir qué sistema operativo estás usando.

Si quieres ocultar información como esta a un adversario de tu red o ISP, **debes** utilizar una [VPN de confianza](../vpn.md) además de cambiar la configuración de comprobación de conectividad a **Estándar (Google)**. Se puede encontrar en :gear: **Configuración** → **Red e Internet** → **Comprobaciones de conectividad a Internet**. Esta opción te permite conectarte a los servidores de Google para comprobar la conectividad, lo que, junto con el uso de una VPN, te ayuda a mezclarte con un grupo mayor de dispositivos Android.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados a ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](../about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

- Debe ser software de código abierto.
- Debe soportar el bloqueo del cargador de arranque con soporte de clave AVB personalizada.
- Debe recibir las principales actualizaciones de Android dentro de 0-1 meses desde su lanzamiento.
- Debe recibir actualizaciones de las funciones de Android (versión menor) en un plazo de 0 a 14 días desde su lanzamiento.
- Debe recibir parches de seguridad periódicos en un plazo de 0 a 5 días desde su publicación.
- No debe estar «rooteado» desde el principio.
- **No** debe habilitar Google Play Services por defecto.
- **No** debe requerir la modificación del sistema para admitir Google Play Services.
