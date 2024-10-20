---
meta_title: Los mejores sistemas operativos personalizados de Android (también conocidos como Custom ROMs) - Privacy Guides
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
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://en.wikipedia.org/wiki/DivestOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: ./
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-target-account: Ataques Dirigidos](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataques Pasivos](../basics/common-threats.md#security-and-privacy){ .pg-orange }

Un **sistema operativo personalizado basado en Android** (también conocido como **ROM** personalizada) es una manera popular de alcanzar altos niveles de privacidad y seguridad en tu dispositivo. Esto contrasta con la versión "stock" de Android que viene preinstalada en tu teléfono y está profundamente integrada con los Servicios de Google Play.

Recomendamos instalar uno de estos sistemas operativos personalizados Android en tu dispositivo, listados en orden de preferencia, dependiendo de la compatibilidad de tu dispositivo con estos sistemas operativos.

## Derivados de AOSP

### GrapheneOS

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

### DivestOS

Si GrapheneOS no es compatible con tu teléfono, DivestOS es una buena alternativa. Admite una amplia variedad de teléfonos con _varios_ niveles de protecciones de seguridad y control de calidad.

<div class="admonition recommendation" markdown>

![DivestOS logo](../assets/img/android/divestos.svg){ align=right }

**DivestOS** es un soft-fork de [LineageOS](https://lineageos.org).
DivestOS hereda muchos [dispositivos compatibles](https://divestos.org/index.php?page=devices\&base=LineageOS) de LineageOS. Tiene builds firmados, haciendo posible tener [arranque verificado](../os/android-overview.md#verified-boot) en algunos dispositivos que no son Pixel. No todos los dispositivos compatibles admiten el arranque verificado u otras funciones de seguridad.

[:octicons-home-16: Página Principal](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Servicio Onion" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title="Contribuir" }

</div>

El [estado](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) de las actualizaciones de firmware en particular variará significativamente dependiendo del modelo de tu teléfono. Mientras que los errores y vulnerabilidades estándar de AOSP pueden solucionarse con actualizaciones de software estándar como las proporcionadas por DivestOS, algunas vulnerabilidades no pueden parchearse sin el apoyo del fabricante del dispositivo, lo que hace que los dispositivos al final de su vida útil sean menos seguros incluso con una ROM alternativa actualizada como DivestOS.

DivestOS dispone de [parcheo](https://gitlab.com/divested-mobile/cve_checker) automático de vulnerabilidades del kernel ([CVE](https://es.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)), menos blobs propietarios y un archivo [hosts](https://divested.dev/index.php?page=dnsbl) personalizado. Su WebView reforzado, [Mulch](https://gitlab.com/divested-mobile/mulch), permite la [integridad del flujo de control](https://en.wikipedia.org/wiki/Control-flow_integrity) para todas las arquitecturas y la [partición del estado de la red](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), y recibe actualizaciones fuera de banda.

DivestOS también incluye parches del núcleo de GrapheneOS y activa todas las funciones de seguridad del núcleo disponibles a través de [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). Todos los kernels más nuevos que la versión 3.4 incluyen [sanitización](https://lwn.net/Articles/334747) de página completa y todos los kernels compilados por Clang ~22 tienen activado [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471).

DivestOS implementa algunos parches de endurecimiento del sistema desarrollados originalmente para GrapheneOS. DivestOS 16.0 y superior implementa el cambio de permisos `INTERNET` y `SENSORS` de GrapheneOS, [asignador de memoria endurecido](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://grapheneos.org/usage#exec-spawning), Interfaz Nativa Java [constificación](https://en.wikipedia.org/wiki/Const_\(programación_informática\)), y parches de endurecimiento parciales [biónicos](https://en.wikipedia.org/wiki/Bionic_\(software\)). La versión 17.1 y superiores incluyen aleatorización completa de direcciones MAC por red, control [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html), reinicio automático y [opciones de tiempo de espera](https://grapheneos.org/features#attack-surface-reduction) Wi-Fi/Bluetooth.

DivestOS utiliza F-Droid como su tienda de aplicaciones por defecto. Normalmente [recomendamos evitar F-Droid](obtaining-apps.md#f-droid), pero hacerlo en DivestOS no es viable; los desarrolladores actualizan sus aplicaciones a través de su propio repositorio F-Droid, [DivestOS Oficial](https://divestos.org/fdroid/official). Para estas aplicaciones debes seguir usando F-Droid **con el repositorio DivestOS habilitado** para mantener esos componentes actualizados. Para otras aplicaciones, se siguen aplicando nuestros [métodos de obtención](obtaining-apps.md) recomendados.

DivestOS sustituye muchas de las conexiones de red en segundo plano de Android a los servicios de Google por servicios alternativos, como el uso de OpenEUICC para la activación de eSIM, NTP.org para la hora de red y Quad9 para DNS. Estas conexiones pueden modificarse, pero su desviación de las conexiones de red de un teléfono Android estándar podría significar que es más fácil para un adversario en tu red deducir qué sistema operativo tienes instalado en tu teléfono. Si esto te preocupa, considera la posibilidad de utilizar una [VPN de confianza](../vpn.md) y activar el [kill switch](../os/android-overview.md#vpn-killswitch) nativo de VPN para ocultar este tráfico de red de tu red local e ISP.

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
