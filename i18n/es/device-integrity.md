---
title: Integridad del Dispositivo
icon: material/security
description: Estas herramientas pueden utilizarse para comprobar si tus dispositivos están comprometidos.
cover: device-integrity.webp
---

Estas herramientas pueden utilizarse para validar la integridad de tus dispositivos móviles y comprobar si presentan indicadores de compromiso por programas espía y maliciosos como Pegasus, Predator o KingsPawn. Esta página se centra en la **seguridad móvil**, porque los dispositivos móviles suelen tener sistemas de solo lectura con configuraciones bien conocidas, por lo que detectar modificaciones maliciosas es más fácil que en los sistemas de escritorio tradicionales. Es posible que en el futuro ampliemos el contenido de esta página.

<div class="admonition note" markdown>
<p class="admonition-title">Este es un tema avanzado</p>

These tools may provide utility for certain individuals. Estas proporcionan funciones de las que la mayoría de las personas no se deben preocupar y, frecuentemente, requieren un conocimiento técnico más profundo para ser usadas de la manera correcta.

</div>

Es **crítico** comprender que escanear tu dispositivo por indicadores públicos de compromiso **no es suficiente** para determinar si un dispositivo está "limpio" y no está bajo el radar de una herramienta de spyware. La confianza en estas herramientas de escaneo de acceso público puede pasar por alto los últimos avances en seguridad y proporcionarte una falsa sensación de seguridad.

## Recomendación general

La mayoría de las vulnerabilidades a nivel del sistema en dispositivos móviles modernos—en especial los del tipo cero-click—no son persistentes, significando que estas no permanecerán o se ejecutarán luego de un reinicio. Por esta razón, recomendamos encarecidamente reiniciar tu dispositivo con regularidad. Le recomendamos a todos reiniciar sus dispositivos una vez por semana como mínimo, pero si un malware no persistente es una preocupación en particular para ti, nosotros y varios expertos en seguridad recomendamos un programa de reinicio diario.

Esto significa que un atacante deberá volver a infectar tu dispositivo con regularidad para mantener el acceso, aunque es importante destacar que esto no es imposible. Reiniciar tu dispositivo tampoco te protegerá ante malware _persistente_, pero esto no es tan común en los dispositivos móviles, debido a características modernas de seguridad como el inicio seguro/verificado.

## Información y descargo posterior al compromiso

Si cualquiera de las siguientes herramientas indican un potencial compromiso de parte de programas espías como Pegasus, Predator o KingsPawn, te recomendamos contactar:

- If you are a human rights defender, journalist, or from a civil society organization: [Amnesty International's Security Lab](https://securitylab.amnesty.org/contact-us)
- Si un dispositivo empresarial o gubernamental es comprometido: Contacte al responsable de seguridad de tu empresa, departamento o agencia
- Cuerpos locales de seguridad

**No somos capaces de ayudarte directamente más allá de esto.** Estamos encantados de discutir tu situación o circunstancia en específico y revisar tus resultados en nuestros espacios [comunitarios](https://discuss.privacyguides.net), pero es poco probable que podamos ayudarte más allá de lo escrito en esta página.

Las herramientas en esta página únicamente son capaces de detectar indicadores de compromisos, no en removerlos. Si estás preocupado sobre estar comprometido, te sugerimos:

- Considerar reemplazar el dispositivo en su totalidad
- Considerar cambiar tu número SIM/eSIM
- No restaurar una copia de seguridad, porque dicho respaldo podría estar comprometido

Estas herramientas proporcionan un análisis basado en la información de tu dispositivo que son capaces de acceder, además de los indicadores públicos de compromiso. Es importante tomar en cuenta dos cosas:

1. Los indicadores de compromiso son solo eso: _indicadores_. No son un hallazgo definitivo y, ocasionalmente, pueden ser **falsos positivos**. Si un indicador de compromiso es detectado, esto significa que deberías realizar una investigación adicional sobre la _potencial_ amenaza.
2. ¡Los indicadores de compromiso buscados por estas herramientas son publicados por organizaciones de investigación de amenazas, pero no todos los indicadores son públicos! Esto significa que estas herramientas pueden presentar un **falso negativo**, si tu dispositivo está infectado con programas de espionaje que no son detectados por cualquiera de los indicadores públicos. Un soporte forense digital confiable y completo requiere el acceso a indicadores privados, investigación e inteligencia de amenazas.

## Herramientas externas de verificación

Las herramientas externas de verificación se pueden ejecutar en tu computadora y escanean tu dispositivo móvil por rastros forenses que son útiles para identificar potenciales compromisos.

<div class="admonition danger" markdown>
<p class="admonition-title">Peligro</p>

Los indicadores públicos de compromiso son insuficientes para determinar si un dispositivo está "limpio" y no está bajo el radar de una herramienta de espionaje en específico. La confianza en indicadores públicos puede pasar por alto los más recientes rastros forenses y proporcionar una falsa sensación de seguridad.

Un soporte forense digital confiable y completo requiere el acceso a indicadores privados, investigación e inteligencia de amenazas.

Such support is available to civil society through [Amnesty International's Security Lab](https://amnesty.org/en/tech) or [Access Now’s Digital Security Helpline](https://accessnow.org/help).

</div>

Estas herramientas pueden desencadenar falsos positivos. Si alguna de estas herramientas detecta indicadores de peligro, debes profundizar para determinar el riesgo real. Algunos informes pueden ser falsos positivos basados en sitios web que has visitado en el pasado, y los hallazgos que tienen muchos años de antigüedad probablemente sean falsos positivos o indiquen un compromiso anterior (y ya no activo).

### Mobile Verification Toolkit

<div class="admonition recommendation" markdown>

![Logo de MVT](assets/img/device-integrity/mvt.webp){ align=right }

**Mobile Verification Toolkit** (**MVT**) es una colección de herramientas que simplifican y automatizan el proceso de escanear dispositivos móviles en busca de potenciales rastros de ataques o infecciones por campañas conocidas de espionaje. MVT was developed by Amnesty International and released in 2021 in the context of the [Pegasus Project](https://forbiddenstories.org/about-the-pegasus-project).

[:octicons-home-16: Homepage](https://mvt.re){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-apple: macOS](https://docs.mvt.re/en/latest/install)
- [:simple-linux: Linux](https://docs.mvt.re/en/latest/install)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El uso de MVT no es suficiente para determinar que un dispositivo está "limpio" y no es objetivo de una herramienta espía concreta.

</div>

MVT es _más_ útil para escanear dispositivos iOS. Android almacena muy poca información de diagnóstico útil para triar posibles compromisos, y debido a esto las capacidades de `mvt-android` también son limitadas. Por otro lado, las copias de seguridad cifradas de iTunes para iOS proporcionan un subconjunto de archivos almacenados en el dispositivo lo suficientemente grande como para detectar artefactos sospechosos en muchos casos. Dicho esto, MVT sigue proporcionando herramientas bastante útiles para el análisis tanto de iOS como de Android.

Si utilizas iOS y estás en situación de alto riesgo, tenemos tres sugerencias adicionales para ti:

1. Crea y mantén copias de seguridad periódicas (mensuales) de iTunes. Esto te permite encontrar y diagnosticar infecciones pasadas más tarde con MVT, si se descubren nuevas amenazas en el futuro.

2. Activa los registros de _sysdiagnose_ a menudo y respáldalos externamente. Estos registros pueden proporcionar datos muy valiosos a futuros investigadores forenses en caso necesario.

   El proceso para hacerlo varía según el modelo, pero puedes activarlo en los teléfonos más nuevos manteniendo pulsados _Apagar_ + _Subir volumen_ + _Bajar volumen_ hasta que sientas una breve vibración. Transcurridos unos minutos, el registro _sysdiagnose_ con fecha y hora aparecerá en **Configuración** > **Privacidad y seguridad** > **Análisis y Mejoras** > **Datos de Análisis**.

3. Activa eñ [Modo de Bloqueo](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode).

MVT te permite realizar escaneos/análisis más profundos si tu dispositivo tiene jailbreak. A menos que sepas lo que estás haciendo, **no hagas jailbreak ni root a tu dispositivo.** Hacer jailbreak a tu dispositivo lo expone a considerables riesgos de seguridad.

### iMazing (iOS)

<div class="admonition recommendation" markdown>

![logo de iMazing](assets/img/device-integrity/imazing.png){ align=right }

**iMazing** proporciona una herramienta gratuita para el análisis de programas de espionaje, disponible para dispositivos iOS, que actúa como una interfaz gráfica para [MVT](#mobile-verification-toolkit). Esta puede ser más fácil de ejecutar, a comparación del propio MVT, que es una herramienta de línea de comandos diseñada para tecnólogos e investigadores forenses.

[:octicons-home-16: Homepage](https://imazing.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-windows11: Windows](https://imazing.com/download)
- [:simple-apple: macOS](https://imazing.com/download)

</details>

</div>

iMazing automatiza y te guía de forma interactiva a través del proceso de uso de [MVT](#mobile-verification-toolkit) para escanear tu dispositivo en busca de indicadores de compromiso de acceso público publicados por varios investigadores de amenazas. Toda la información y advertencias que se aplican a MVT se aplican también a esta herramienta, por lo que te sugerimos que te familiarices también con las notas sobre MVT de las secciones anteriores.

## Verificación en el Dispositivo

Se trata de aplicaciones que puedes instalar y que comprueban el dispositivo y el sistema operativo en busca de signos de manipulación y validan la identidad del dispositivo.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El uso de estas aplicaciones no basta para determinar que un dispositivo está "limpio" y no es objetivo de una herramienta de spyware concreta.

</div>

### Auditor (Android)

<div class="admonition recommendation" markdown>

![Logo de Auditor](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![Logo de Auditor](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**Auditor** es una aplicación que aprovecha las funciones de seguridad del hardware para proporcionar un monitoreo de la integridad del dispositivo, al validar de manera activa la identidad de este y la integridad del sistema operativo. Actualmente, esta sólo funciona con GrapheneOS o el sistema operativo en limpio para los [dispositivos compatibles](https://attestation.app/about#device-support).

[:octicons-home-16: Página principal](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Política de privacidad" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title="Documentación"}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="Código fuente" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title="Contribuir"}

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Auditor no es una herramienta de escaneo/análisis como otras herramientas de esta página, sino que utiliza el almacén de claves respaldado por hardware de tu dispositivo para permitirte verificar la identidad de tu dispositivo y asegurarte de que el propio sistema operativo no ha sido manipulado o degradado a través de un arranque verificado. Esto proporciona una comprobación muy sólida de la integridad del propio dispositivo, pero no comprueba necesariamente si las aplicaciones a nivel de usuario que se ejecutan en el dispositivo son maliciosas.

El auditor realiza la atestación y la detección de intrusiones con **dos** dispositivos, uno _auditado_ (el dispositivo que se verifica) y un _auditor_ (el dispositivo que realiza la verificación). El auditor puede ser cualquier dispositivo Android 10+ (o un servicio web remoto operado por [GrapheneOS](android.md#grapheneos)), mientras que el auditado debe ser específicamente un [dispositivo soportado](https://attestation.app/about#device-support). Auditor funciona así:

- Using a [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) model between an _auditor_ and _auditee_, the pair establish a private key in the [hardware-backed keystore](https://source.android.com/security/keystore) of the _Auditor_.
- El _auditor_ puede ser otra instancia de la aplicación Auditor o el [Servicio de Certificación a Distancia](https://attestation.app).
- El _auditor_ registra el estado actual y la configuración del _auditado_.
- En caso de que se produzca una manipulación del sistema operativo del _auditado_ una vez completado el emparejamiento, el auditor será consciente del cambio en el estado y las configuraciones del dispositivo.
- Se te avisará del cambio.

Es importante señalar que Auditor solo puede detectar eficazmente cambios **después** del emparejamiento inicial, no necesariamente durante o antes debido a su modelo TOFU. Para asegurarte de que el hardware y el sistema operativo son auténticos, [realiza una atestación local](https://grapheneos.org/install/web#verifying-installation) inmediatamente después de instalar el dispositivo y antes de cualquier conexión a Internet.

No se envía información personal identificable al servicio de certificación. Recomendamos que te registres con una cuenta anónima y actives la atestación remota para una supervisión continua.

Si tu [modelo de amenaza](basics/threat-modeling.md) requiere privacidad, podrías considerar utilizar [Orbot](tor.md#orbot) o una VPN para ocultar tu dirección IP al servicio de atestación.

## Escáneres en el Dispositivo

Se trata de aplicaciones que puedes instalar en tu dispositivo y que lo escanean en busca de señales de peligro.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El uso de estas aplicaciones no basta para determinar que un dispositivo está "limpio" y no es objetivo de una herramienta de spyware concreta.

</div>

### Hypatia (Android)

<div class="admonition recommendation" markdown>

![Logo de Hypatia](assets/img/device-integrity/hypatia.svg#only-light){ align=right }
![Logo de Hypatia](assets/img/device-integrity/hypatia-dark.svg#only-dark){ align=right }

**Hypatia** es un escáner de malware en tiempo real para Android, creado por el desarrollador de [DivestOS](android.md#divestos). Este accede al Internet para descargar actualizaciones de la base de datos de firmas, pero no sube tus archivos o cualquier metadato a la nube (los escaneos son realizados de manera local).

[:octicons-home-16: Página principal](https://divestos.org/pages/our_apps#hypatia){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy#hypatia){ .card-link title="Política de privacidad" }
[:octicons-code-16:](https://github.com/divested-mobile/hypatia){ .card-link title="Código fuente" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title="Contribuir"}

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-android: F-Droid](https://f-droid.org/packages/us.spotco.malwarescanner)

</details>

</div>

Hypatia is particularly good at detecting common stalkerware: If you suspect you are a victim of stalkerware, you should [visit this page](https://stopstalkerware.org/information-for-survivors) for advice.

### iVerify (iOS)

<div class="admonition recommendation" markdown>

![logo de iVerify](assets/img/device-integrity/iverify.webp){ align=right }

**iVerify** es una aplicación para iOS que escanea de manera automática tu dispositivo para revisar los ajustes de la configuración, el nivel de parche y otras áreas de seguridad. Esta también revisa tu dispositivo por indicadores de compromiso de herramientas de jailbreak o programas de espionaje como Pegasus.

[:octicons-home-16: Homepage](https://iverify.io/consumer){ .md-button .md-button--primary }
[:octicons-eye-16:](https://iverify.io/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://iverify.io/frequently-asked-questions#iVerify-General){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1466120520)

</details>

</div>

Como todas las aplicaciones de iOS, iVerify está limitada a lo que puede observar sobre tu dispositivo desde el iOS App Sandbox. No proporcionará un análisis tan sólido como una herramienta de análisis de sistema completo como [MVT](#mobile-verification-toolkit). Su función principal es detectar si tu dispositivo tiene jailbreak, para lo cual es eficaz, sin embargo, una hipotética amenaza que esté _específicamente_ diseñada para eludir las comprobaciones de iVerify probablemente lo conseguiría.

iVerify **no** es una herramienta "antivirus", y no detectará malware no relacionado con el sistema, como teclados personalizados maliciosos o configuraciones Wi-Fi Sync maliciosas, por ejemplo.

Además del escaneo del dispositivo, iVerify también incluye una serie de utilidades de seguridad adicionales que pueden resultarte útiles, como recordatorios de reinicio del dispositivo, notificaciones de actualización de iOS (que suelen ser más rápidas que el despliegue escalonado de notificaciones de actualización de Apple), algunas guías básicas de privacidad y seguridad, y una herramienta DNS sobre HTTPS que puede conectar las consultas [DNS](dns.md) de tu dispositivo de forma segura a Quad9, Cloudflare o Google.
