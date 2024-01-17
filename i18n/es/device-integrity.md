---
title: Integridad del Dispositivo
icon: material/security
description: Estas herramientas pueden utilizarse para comprobar si tus dispositivos están comprometidos.
cover: device-integrity.webp
---

Estas herramientas pueden utilizarse para validar la integridad de tus dispositivos móviles y comprobar si presentan indicadores de compromiso por programas espía y maliciosos como Pegasus, Predator o KingsPawn. Esta página se centra en la **seguridad móvil**, porque los dispositivos móviles suelen tener sistemas de solo lectura con configuraciones bien conocidas, por lo que detectar modificaciones maliciosas es más fácil que en los sistemas de escritorio tradicionales. Es posible que en el futuro ampliemos el contenido de esta página.

<div class="admonition note" markdown>
<p class="admonition-title">This is an advanced topic</p>

Estas herramientas pueden ser útiles para determinadas personas. They provide functionality which most people do not need to worry about, and often require more in-depth technical knowledge to use effectively.

</div>

It is **critical** to understand that scanning your device for public indicators of compromise is **not sufficient** to determine that a device is "clean", and not targeted with a particular spyware tool. Reliance on these publicly-available scanning tools can miss recent security developments and give you a false sense of security.

## General Advice

The majority of system-level exploits on modern mobile devices—especially zero-click compromises—are non-persistent, meaning they will not remain or run automatically after a reboot. For this reason, we highly recommend rebooting your device regularly. We recommend everybody reboot their devices once a week at minimum, but if non-persistent malware is of particular concern for you, we and many security experts recommend a daily reboot schedule.

This means an attacker would have to regularly re-infect your device to retain access, although we'll note this is not impossible. Rebooting your device also will not protect you against _persistent_ malware, but this is less common on mobile devices due to modern security features like secure/verified boot.

## Post-Compromise Information & Disclaimer

If any of the following tools indicate a potential compromise by spyware such as Pegasus, Predator, or KingsPawn, we advise that you contact:

- If you are a human rights defender, journalist, or from a civil society organization: [Amnesty International's Security Lab](https://securitylab.amnesty.org/contact-us/)
- If a business or government device is compromised: Contact the appropriate security liason at your enterprise, department, or agency
- Local law enforcement

**We are unable to help you directly beyond this.** We are happy to discuss your specific situation or circumstances and review your results in our [community](https://discuss.privacyguides.net) spaces, but it is unlikely we can assist you beyond what is written on this page.

The tools on this page are only capable of detecting indicators of compromise, not removing them. If you are concerned about having been compromised, we advise that you:

- Consider replacing the device completely
- Consider changing your SIM/eSIM number
- Not restore from a backup, because that backup may be compromised

These tools provide analysis based on the information they have the ability to access from your device, and publicly-accessible indicators of compromise. It is important to keep in mind two things:

1. Indicators of compromise are just that: _indicators_. They are not a definitive finding, and may occasionally be **false positives**. If an indicator of compromise is detected, it means you should do additional research into the _potential_ threat.
2. The indicators of compromise these tools look for are published by threat research organizations, but not all indicators are made available to the public! This means that these tools can present a **false negative**, if your device is infected with spyware which is not detected by any of the public indicators. Reliable and comprehensive digital forensic support and triage requires access to non-public indicators, research and threat intelligence.

## External Verification Tools

External verification tools run on your computer and scan your mobile device for forensic traces which are helpful to identify potential compromise.

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Public indicators of compromise are insufficient to determine that a device is "clean", and not targeted with a particular spyware tool. Reliance on public indicators alone can miss recent forensic traces and give a false sense of security.

Reliable and comprehensive digital forensic support and triage requires access to non-public indicators, research and threat intelligence.

Such support is available to civil society through [Amnesty International's Security Lab](https://www.amnesty.org/en/tech/) or [Access Now’s Digital Security Helpline](https://www.accessnow.org/help/).

</div>

Estas herramientas pueden desencadenar falsos positivos. Si alguna de estas herramientas detecta indicadores de peligro, debes profundizar para determinar el riesgo real. Algunos informes pueden ser falsos positivos basados en sitios web que has visitado en el pasado, y los hallazgos que tienen muchos años de antigüedad probablemente sean falsos positivos o indiquen un compromiso anterior (y ya no activo).

### Mobile Verification Toolkit

<div class="admonition recommendation" markdown>

![MVT logo](assets/img/device-integrity/mvt.webp){ align=right }

**Mobile Verification Toolkit** (**MVT**) is a collection of utilities which simplifies and automates the process of scanning mobile devices for potential traces of targeting or infection by known spyware campaigns. MVT was developed by Amnesty International and released in 2021 in the context of the [Pegasus Project](https://forbiddenstories.org/about-the-pegasus-project/).

[:octicons-home-16: Homepage](https://mvt.re/){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: macOS](https://docs.mvt.re/en/latest/install/)
- [:simple-linux: Linux](https://docs.mvt.re/en/latest/install/)

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

![iMazing logo](assets/img/device-integrity/imazing.png){ align=right }

**iMazing** provides a free spyware analyzer tool for iOS devices which acts as a GUI-wrapper for [MVT](#mobile-verification-toolkit). This can be much easier to run compared to MVT itself, which is a command-line tool designed for technologists and forensic investigators.

[:octicons-home-16: Homepage](https://imazing.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

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

![Auditor logo](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![Auditor logo](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**Auditor** is an app which leverages hardware security features to provide device integrity monitoring by actively validating the identity of a device and the integrity of its operating system. Currently, it only works with GrapheneOS or the stock operating system for [supported devices](https://attestation.app/about#device-support).

[:octicons-home-16: Homepage](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentation}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

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

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El uso de estas aplicaciones no basta para determinar que un dispositivo está "limpio" y no es objetivo de una herramienta de spyware concreta.

</div>

### Hypatia (Android)

<div class="admonition recommendation" markdown>

![Hypatia logo](assets/img/device-integrity/hypatia.svg#only-light){ align=right }
![Hypatia logo](assets/img/device-integrity/hypatia-dark.svg#only-dark){ align=right }

**Hypatia** is an open source real-time malware scanner for Android, from the developer of [DivestOS](android.md#divestos). It accesses the internet to download signature database updates, but does not upload your files or any metadata to the cloud (scans are performed entirely locally).

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#hypatia){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy#hypatia){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/divested-mobile/hypatia){ .card-link title="Source Code" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: F-Droid](https://f-droid.org/packages/us.spotco.malwarescanner/)

</details>

</div>

Hypatia es especialmente bueno en la detección de stalkerware común: Si sospechas que eres víctima de stalkerware, deberías [visitar esta página](https://stopstalkerware.org/information-for-survivors/) para obtener asesoramiento.

### iVerify (iOS)

<div class="admonition recommendation" markdown>

![iVerify logo](assets/img/device-integrity/iverify.webp){ align=right }

**iVerify** is an iOS app which automatically scans your device to check configuration settings, patch level, and other areas of security. It also checks your device for indicators of compromise by jailbreak tools or spyware such as Pegasus.

[:octicons-home-16: Homepage](https://www.iverify.io/consumer){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.iverify.io/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://www.iverify.io/frequently-asked-questions#iVerify-General){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/us/app/iverify/id1466120520)

</details>

</div>

Como todas las aplicaciones de iOS, iVerify está limitada a lo que puede observar sobre tu dispositivo desde el iOS App Sandbox. No proporcionará un análisis tan sólido como una herramienta de análisis de sistema completo como [MVT](#mobile-verification-toolkit). Su función principal es detectar si tu dispositivo tiene jailbreak, para lo cual es eficaz, sin embargo, una hipotética amenaza que esté _específicamente_ diseñada para eludir las comprobaciones de iVerify probablemente lo conseguiría.

iVerify **no** es una herramienta "antivirus", y no detectará malware no relacionado con el sistema, como teclados personalizados maliciosos o configuraciones Wi-Fi Sync maliciosas, por ejemplo.

Además del escaneo del dispositivo, iVerify también incluye una serie de utilidades de seguridad adicionales que pueden resultarte útiles, como recordatorios de reinicio del dispositivo, notificaciones de actualización de iOS (que suelen ser más rápidas que el despliegue escalonado de notificaciones de actualización de Apple), algunas guías básicas de privacidad y seguridad, y una herramienta DNS sobre HTTPS que puede conectar las consultas [DNS](dns.md) de tu dispositivo de forma segura a Quad9, Cloudflare o Google.
