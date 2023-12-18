---
title: Integridad del Dispositivo
icon: material/security
description: Estas herramientas pueden utilizarse para comprobar si tus dispositivos están comprometidos.
cover: device-integrity.webp
---

Estas herramientas pueden utilizarse para validar la integridad de tus dispositivos móviles y comprobar si presentan indicadores de compromiso por programas espía y maliciosos como Pegasus, Predator o KingsPawn. Esta página se centra en la **seguridad móvil**, porque los dispositivos móviles suelen tener sistemas de solo lectura con configuraciones bien conocidas, por lo que detectar modificaciones maliciosas es más fácil que en los sistemas de escritorio tradicionales. Es posible que en el futuro ampliemos el contenido de esta página.

!!! nota "Este es un tema avanzado"

```
Estas herramientas pueden resultar útiles para determinadas personas. Proporcionan funcionalidades de las que la mayoría de la gente no necesita preocuparse, y a menudo requieren conocimientos técnicos más profundos para utilizarlas con eficacia.
```

Es **crítico** entender que escanear tu dispositivo en busca de indicadores públicos de compromiso no es **suficiente** para determinar que un dispositivo está "limpio" y no es el objetivo de una herramienta de spyware en particular. Confiar en estas herramientas de escaneado de acceso público puede pasar por alto los últimos avances en materia de seguridad y darte una falsa sensación de seguridad.

## Consejo General

La mayoría de los exploits a nivel de sistema en los dispositivos móviles modernos -especialmente los de tipo zero-click- no son persistentes, lo que significa que no permanecen ni se ejecutan automáticamente tras un reinicio. Por este motivo, recomendamos encarecidamente reiniciar el dispositivo con regularidad. Recomendamos a todo el mundo que reinicie sus dispositivos una vez a la semana como mínimo, pero si el malware no persistente te preocupa especialmente, nosotros y muchos expertos en seguridad recomendamos un programa de reinicio diario.

Esto significa que un atacante tendría que reinfectar regularmente tu dispositivo para mantener el acceso, aunque cabe señalar que esto no es imposible. Reiniciar tu dispositivo tampoco te protegerá contra el malware _persistente_, pero esto es menos común en los dispositivos móviles debido a las modernas características de seguridad como el arranque seguro/verificado.

## Información Posterior al Compromiso y Descargo de Responsabilidad

Si alguna de las siguientes herramientas indica un posible compromiso por parte de programas espía como Pegasus, Predator o KingsPawn, te aconsejamos que te pongas en contacto con:

- Si eres un defensor de los derechos humanos, periodista o perteneces a una organización de la sociedad civil: [Laboratorio de Seguridad de Amnistía Internacional](https://securitylab.amnesty.org/contact-us/)
- Si un dispositivo empresarial o gubernamental se ve comprometido: Ponte en contacto con el responsable de seguridad de tu empresa, departamento o agencia
- Fuerzas y cuerpos de seguridad locales

**No podemos ayudarte directamente más allá de esto.** Estamos encantados de discutir tu situación específica o circunstancias y de revisar tus resultados en nuestros espacios de [community](https\://discuss. rivacyguides.net), pero es poco probable que podamos ayudarte más allá de lo que está escrito en esta página.

Las herramientas de esta página solo son capaces de detectar indicadores de compromiso, no de eliminarlos. Si te preocupa haber sido comprometido, te aconsejamos que:

- Considera la posibilidad de sustituir el dispositivo por completo
- Considera cambiar tu número SIM/eSIM
- No restaures a partir de una copia de seguridad, porque esa copia puede estar comprometida

Estas herramientas ofrecen análisis basados en la información a la que pueden acceder desde tu dispositivo, así como indicadores de compromiso de acceso público. Es importante tener en cuenta dos cosas:

1. Los indicadores de compromiso son solo eso: _indicadores_. No son un hallazgo definitivo, y ocasionalmente pueden ser **falsos positivos**. Si se detecta un indicador de compromiso, significa que debes realizar una investigación adicional sobre la amenaza _potencial_.
2. Los indicadores de peligro que buscan estas herramientas son publicados por organizaciones de investigación de amenazas, ¡pero no todos los indicadores se ponen a disposición del público! Esto significa que estas herramientas pueden presentar un **falso negativo**, si tu dispositivo está infectado con spyware que no es detectado por ninguno de los indicadores públicos. Un apoyo y triaje forense digital fiable y completo requiere acceso a indicadores no públicos, investigación e inteligencia sobre amenazas.

## Herramientas de Verificación Externas

Las herramientas de verificación externas se ejecutan en el ordenador y escanean el dispositivo móvil en busca de rastros forenses que resulten útiles para identificar un posible compromiso.

!!! danger "Peligro"

```
Los indicadores públicos de compromiso son insuficientes para determinar que un dispositivo está "limpio" y no es el objetivo de una herramienta espía concreta. Confiar únicamente en indicadores públicos puede pasar por alto rastros forenses recientes y dar una falsa sensación de seguridad.

Un apoyo y un triaje forenses digitales fiables y completos requieren acceso a indicadores no públicos, investigación e inteligencia sobre amenazas.

Este tipo de apoyo está disponible para la sociedad civil a través de [Laboratorio de Seguridad de Amnistía Internacional](https://www.amnesty.org/es/tech/) o [Línea de Ayuda de Seguridad Digital de Access Now](https://www.accessnow.org/help/).
```

Estas herramientas pueden desencadenar falsos positivos. Si alguna de estas herramientas detecta indicadores de peligro, debes profundizar para determinar el riesgo real. Algunos informes pueden ser falsos positivos basados en sitios web que has visitado en el pasado, y los hallazgos que tienen muchos años de antigüedad probablemente sean falsos positivos o indiquen un compromiso anterior (y ya no activo).

### Mobile Verification Toolkit

!!! recommendation "Recomendación"

```
![MVT logo](assets/img/device-integrity/mvt.webp){ align=right }

**Mobile Verification Toolkit** (**MVT**) es una colección de utilidades que simplifica y automatiza el proceso de escaneo de dispositivos móviles en busca de posibles rastros de ataques o infecciones por campañas de spyware conocidas. MVT fue desarrollado por Amnistía Internacional y publicado en 2021 en el contexto del [Proyecto Pegasus](https://forbiddenstories.org/about-the-pegasus-project/).

[:octicons-home-16: Página Principal](https://mvt.re/){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Código Fuente" }

??? downloads "Descargas"

    - [:simple-apple: macOS](https://docs.mvt.re/en/latest/install/)
    - [:simple-linux: Linux](https://docs.mvt.re/en/latest/install/)
```

!!! warning "Advertencia"

```
El uso de MVT no es suficiente para determinar que un dispositivo está "limpio" y no es objetivo de una herramienta espía concreta.
```

MVT es _más_ útil para escanear dispositivos iOS. Android almacena muy poca información de diagnóstico útil para triar posibles compromisos, y debido a esto las capacidades de `mvt-android` también son limitadas. Por otro lado, las copias de seguridad cifradas de iTunes para iOS proporcionan un subconjunto de archivos almacenados en el dispositivo lo suficientemente grande como para detectar artefactos sospechosos en muchos casos. Dicho esto, MVT sigue proporcionando herramientas bastante útiles para el análisis tanto de iOS como de Android.

Si utilizas iOS y estás en situación de alto riesgo, tenemos tres sugerencias adicionales para ti:

1. Crea y mantén copias de seguridad periódicas (mensuales) de iTunes. Esto te permite encontrar y diagnosticar infecciones pasadas más tarde con MVT, si se descubren nuevas amenazas en el futuro.

2. Activa los registros de _sysdiagnose_ a menudo y respáldalos externamente. Estos registros pueden proporcionar datos muy valiosos a futuros investigadores forenses en caso necesario.

   El proceso para hacerlo varía según el modelo, pero puedes activarlo en los teléfonos más nuevos manteniendo pulsados _Apagar_ + _Subir volumen_ + _Bajar volumen_ hasta que sientas una breve vibración. Transcurridos unos minutos, el registro _sysdiagnose_ con fecha y hora aparecerá en **Configuración** > **Privacidad y seguridad** > **Análisis y Mejoras** > **Datos de Análisis**.

3. Activa eñ [Modo de Bloqueo](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode).

MVT te permite realizar escaneos/análisis más profundos si tu dispositivo tiene jailbreak. A menos que sepas lo que estás haciendo, **no hagas jailbreak ni root a tu dispositivo.** Hacer jailbreak a tu dispositivo lo expone a considerables riesgos de seguridad.

### iMazing (iOS)

!!! recommendation "Recomendación"

```
![iMazing logo](assets/img/device-integrity/imazing.png){ align=right }

**iMazing** proporciona una herramienta gratuita de análisis de spyware para dispositivos iOS que actúa como un GUI-wrapper para [MVT](#mobile-verification-toolkit). Esto puede ser mucho más fácil de ejecutar en comparación con el propio MVT, que es una herramienta de línea de comandos diseñada para tecnólogos e investigadores forenses.

[:octicons-home-16: Página Principal](https://imazing.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title=Documentación}

??? downloads "Descargas"

    - [:simple-windows11: Windows](https://imazing.com/download)
    - [:simple-apple: macOS](https://imazing.com/download)
```

iMazing automatiza y te guía de forma interactiva a través del proceso de uso de [MVT](#mobile-verification-toolkit) para escanear tu dispositivo en busca de indicadores de compromiso de acceso público publicados por varios investigadores de amenazas. Toda la información y advertencias que se aplican a MVT se aplican también a esta herramienta, por lo que te sugerimos que te familiarices también con las notas sobre MVT de las secciones anteriores.

## Verificación en el Dispositivo

Se trata de aplicaciones que puedes instalar y que comprueban el dispositivo y el sistema operativo en busca de signos de manipulación y validan la identidad del dispositivo.

!!! warning "Advertencia"

```
El uso de estas aplicaciones no basta para determinar que un dispositivo está "limpio" y no es objetivo de una herramienta de spyware concreta.
```

### Auditor (Android)

!!! recommendation "Recomendación"

```
![Auditor logo](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![Auditor logo](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**Auditor** es una aplicación que aprovecha las características de seguridad del hardware para supervisar la integridad del dispositivo validando activamente la identidad de un dispositivo y la integridad de su sistema operativo. Actualmente, solo funciona con GrapheneOS o con el sistema operativo original de [dispositivos compatibles](https://attestation.app/about#device-support).

[:octicons-home-16: Página Principal](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentación}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribuir }

??? downloads "Descargas"

    - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
    - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
    - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)
```

Auditor no es una herramienta de escaneo/análisis como otras herramientas de esta página, sino que utiliza el almacén de claves respaldado por hardware de tu dispositivo para permitirte verificar la identidad de tu dispositivo y asegurarte de que el propio sistema operativo no ha sido manipulado o degradado a través de un arranque verificado. Esto proporciona una comprobación muy sólida de la integridad del propio dispositivo, pero no comprueba necesariamente si las aplicaciones a nivel de usuario que se ejecutan en el dispositivo son maliciosas.

El auditor realiza la atestación y la detección de intrusiones con **dos** dispositivos, uno _auditado_ (el dispositivo que se verifica) y un _auditor_ (el dispositivo que realiza la verificación). El auditor puede ser cualquier dispositivo Android 10+ (o un servicio web remoto operado por [GrapheneOS](android.md#grapheneos)), mientras que el auditado debe ser específicamente un [dispositivo soportado](https://attestation.app/about#device-support). Auditor funciona así:

- Utilizando un modelo [Confiar en el Primer Uso (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) entre un _auditor_ y un _auditado_, la pareja establece una clave privada en el [almacén de claves respaldado por hardware](https://source.android.com/security/keystore/) de _Auditor_.
- El _auditor_ puede ser otra instancia de la aplicación Auditor o el [Servicio de Certificación a Distancia](https://attestation.app).
- El _auditor_ registra el estado actual y la configuración del _auditado_.
- En caso de que se produzca una manipulación del sistema operativo del _auditado_ una vez completado el emparejamiento, el auditor será consciente del cambio en el estado y las configuraciones del dispositivo.
- Se te avisará del cambio.

Es importante señalar que Auditor solo puede detectar eficazmente cambios **después** del emparejamiento inicial, no necesariamente durante o antes debido a su modelo TOFU. Para asegurarte de que el hardware y el sistema operativo son auténticos, [realiza una atestación local](https://grapheneos.org/install/web#verifying-installation) inmediatamente después de instalar el dispositivo y antes de cualquier conexión a Internet.

No se envía información personal identificable al servicio de certificación. Recomendamos que te registres con una cuenta anónima y actives la atestación remota para una supervisión continua.

Si tu [modelo de amenaza](basics/threat-modeling.md) requiere privacidad, podrías considerar utilizar [Orbot](tor.md#orbot) o una VPN para ocultar tu dirección IP al servicio de atestación.

## Escáneres en el Dispositivo

Se trata de aplicaciones que puedes instalar en tu dispositivo y que lo escanean en busca de señales de peligro.

!!! warning "Advertencia"

```
El uso de estas aplicaciones no basta para determinar que un dispositivo está "limpio" y no es objetivo de una herramienta de spyware concreta.
```

### Hypatia (Android)

!!! recommendation "Recomendación"

```
![Hypatia logo](assets/img/device-integrity/hypatia.svg#only-light){ align=right }
![Hypatia logo](assets/img/device-integrity/hypatia-dark.svg#only-dark){ align=right }

**Hypatia** es un escáner de malware en tiempo real de código abierto para Android, del desarrollador de [DivestOS](android.md#divestos). Accede a Internet para descargar actualizaciones de la base de datos de firmas, pero no sube tus archivos ni ningún metadato a la nube (los escaneos se realizan de forma totalmente local).

[:octicons-home-16: Página Principal](https://divestos.org/pages/our_apps#hypatia){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy#hypatia){ .card-link title="Política de Privacidad" }
[:octicons-code-16:](https://github.com/divested-mobile/hypatia){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribuir }

??? downloads "Descargas"

    - [:simple-android: F-Droid](https://f-droid.org/packages/us.spotco.malwarescanner/)
```

Hypatia es especialmente bueno en la detección de stalkerware común: Si sospechas que eres víctima de stalkerware, deberías [visitar esta página](https://stopstalkerware.org/information-for-survivors/) para obtener asesoramiento.

### iVerify (iOS)

!!! recommendation "Recomendación"

```
![iVerify logo](assets/img/device-integrity/iverify.webp){ align=right }

**iVerify** es una aplicación para iOS que escanea automáticamente tu dispositivo para comprobar los ajustes de configuración, el nivel de parches y otras áreas de seguridad. También comprueba tu dispositivo en busca de indicadores de compromiso por parte de herramientas de jailbreak o spyware como Pegasus.

[:octicons-home-16: Página Principal](https://www.iverify.io/consumer){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.iverify.io/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://www.iverify.io/frequently-asked-questions#iVerify-General){ .card-link title=Documentación}

??? downloads "Descargas"

    - [:simple-appstore: App Store](https://apps.apple.com/us/app/iverify/id1466120520)
```

Como todas las aplicaciones de iOS, iVerify está limitada a lo que puede observar sobre tu dispositivo desde el iOS App Sandbox. No proporcionará un análisis tan sólido como una herramienta de análisis de sistema completo como [MVT](#mobile-verification-toolkit). Su función principal es detectar si tu dispositivo tiene jailbreak, para lo cual es eficaz, sin embargo, una hipotética amenaza que esté _específicamente_ diseñada para eludir las comprobaciones de iVerify probablemente lo conseguiría.

iVerify **no** es una herramienta "antivirus", y no detectará malware no relacionado con el sistema, como teclados personalizados maliciosos o configuraciones Wi-Fi Sync maliciosas, por ejemplo.

Además del escaneo del dispositivo, iVerify también incluye una serie de utilidades de seguridad adicionales que pueden resultarte útiles, como recordatorios de reinicio del dispositivo, notificaciones de actualización de iOS (que suelen ser más rápidas que el despliegue escalonado de notificaciones de actualización de Apple), algunas guías básicas de privacidad y seguridad, y una herramienta DNS sobre HTTPS que puede conectar las consultas [DNS](dns.md) de tu dispositivo de forma segura a Quad9, Cloudflare o Google.
