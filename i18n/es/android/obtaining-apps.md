---
title: Obtener Aplicaciones
description: Recomendamos estos métodos para obtener aplicaciones en Android sin interactuar con los Servicios de Google Play.
---

Hay varias formas para obtener aplicaciones de Android de una manera privada, incluso desde Google Play Store, sin interactuar con los Servicios de Google Play. Recomendamos los siguientes métodos de obtener aplicaciones en Android, listados en orden de preferencia.

## Obtainium

<div class="admonition recommendation" markdown>

![Logo de Obtainium](../assets/img/android/obtainium.svg){ align=right }

**Obtainium** es un gestor de aplicaciones que permite instalar y actualizar aplicaciones, directamente desde la propia página de lanzamientos del desarrollador (por ejemplo, GitHub, GitLab, el sitio web del desarrollador, etc.), en vez de una tienda o repositorio centralizado. Es compatible con las actualizaciones automáticas en segundo plano en Android 12 y versiones superiores.

[:octicons-repo-16: Repositorio](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Código fuente" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium te permite descargar los archivos instaladores APK desde una amplia variedad de fuentes, y depende de ti asegurarte que esas fuentes y aplicaciones son legítimas. Por ejemplo, utilizar Obtainium para instalar Signal desde la [página de Signal](https://signal.org/android/apk) puede estar bien, pero realizar la instalación desde repositorios de terceros como Aptoide o APKPure puede generar riesgos adicionales. El riesgo de instalar una _actualización_ maliciosa es bajo, porque Android verifica que todas las actualizaciones se encuentran firmadas por el mismo desarrollador de la aplicación existente en tu teléfono antes de instalarla.

## Tienda de aplicaciones de GrapheneOS

La tienda de aplicaciones de GrapheneOS está disponible en [GitHub](https://github.com/GrapheneOS/Apps/releases). Es compatible con Android 12 y superiores, y es capaz de actualizarse por si misma. La tienda de aplicaciones tiene aplicaciones independientes creadas por el proyecto GrapheneOS, como [Auditor](../device-integrity.md#auditor-android), [Cámara](general-apps.md#secure-camera) y [Lector PDF](general-apps.md#secure-pdf-viewer). Si estás buscando estas aplicaciones, te recomendamos obtenerlas desde la tienda de aplicaciones de GrapheneOS en vez de la Play Store, porque las aplicaciones en su propia tienda se encuentran firmadas con las propias firmas del proyecto GrapheneOS, que no pueden ser accesadas por Google.

## Aurora Store

Google Play Store requiere una cuenta de Google para iniciar sesión, algo poco ideal para la privacidad. Puedes evitar esto usando un cliente alternativo como Aurora Store.

<div class="admonition recommendation" markdown>

![logo de Aurora Store](../assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** es un cliente de Google Play Store que no requiere una cuenta de Google, los Servicios de Google Play o microG para la descarga de aplicaciones.

[:octicons-home-16: Página principal](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Política de privacidad" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Código fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Aurora Store no permite descargar aplicaciones de pago con su función de cuenta anónima. Opcionalmente, puedes iniciar sesión con tu cuenta de Google en Aurora Store para descargar las aplicaciones que has comprado, lo que permite a Google accesar al listado de aplicaciones instaladas. Sin embargo, todavía te beneficias de no requerir el cliente completo de Google Play, además de los servicios de Google Play o microG en tu dispositivo.

## Manualmente con notificaciones RSS

Para las aplicaciones que son publicadas en plataformas como GitHub y GitLab, puedes añadir un canal RSS a tu [agregador de noticias](../news-aggregators.md) que te ayudará a rastrear los nuevos lanzamientos.

![RSS APK](../assets/img/android/rss-apk-light.png#only-light) ![RSS APK](../assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](../assets/img/android/rss-changes-light.png#only-light) ![APK Changes](../assets/img/android/rss-changes-dark.png#only-dark)

### GitHub

En GitHub, usando [Secure Camera](general-apps.md#secure-camera) como un ejemplo, puedes dirigirte a su [página de lanzamientos](https://github.com/GrapheneOS/Camera/releases) y añadir `.atom` a la URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

### GitLab

En GitLab, usando [Aurora Store](#aurora-store) como ejemplo, navegarías a su [repositorio de proyecto](https://gitlab.com/AuroraOSS/AuroraStore) y añadirías `/-/tags?format=atom` a la URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

### Verificación de Huellas Digitales APK

Si descarga archivos APK para instalarlos manualmente, puedes verificar su firma con la herramienta [`apksigner`](https://developer.android.com/studio/command-line/apksigner), que forma parte de [build-tools](https://developer.android.com/studio/releases/build-tools) de Android.

1. Instala [Java JDK](https://oracle.com/java/technologies/downloads).

2. Descarga las [Herramientas de línea de comandos de Android Studio](https://developer.android.com/studio#command-tools).

3. Extrae el archivo descargado:

   ```bash
   unzip commandlinetools-*.zip
   cd cmdline-tools
   ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
   ```

4. Ejecuta el comando de verificación de firma:

   ```bash
   ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
   ```

5. Los hashes resultantes pueden compararse con otra fuente. Algunos desarrolladores como Signal [muestran las huellas digitales](https://signal.org/android/apk) en su sitio web.

   ```bash
   Signer #1 certificate DN: CN=GrapheneOS
   Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
   Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
   Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
   ```

## F-Droid

![F-Droid logo](../assets/img/android/f-droid.svg){ align=right width=120px }

\==We only recommend F-Droid as a way to obtain apps which cannot be obtained via the means above.== F-Droid is often recommended as an alternative to Google Play, particularly within the privacy community. The option to add third-party repositories and not be confined to Google's walled garden has led to its popularity. F-Droid additionally has [reproducible builds](https://f-droid.org/en/docs/Reproducible_Builds) for some applications and is dedicated to free and open-source software. However, there are some security-related downsides to how F-Droid builds, signs, and delivers packages:

Due to their process of building apps, apps in the _official_ F-Droid repository often fall behind on updates. F-Droid maintainers also reuse package IDs while signing apps with their own keys, which is not ideal as it gives the F-Droid team ultimate trust. Additionally, the requirements for an app to be included in the official F-Droid repo are less strict than other app stores like Google Play, meaning that F-Droid tends to host a lot more apps which are older, unmaintained, or otherwise no longer meet [modern security standards](https://developer.android.com/google/play/requirements/target-sdk).

Other popular third-party repositories for F-Droid such as [IzzyOnDroid](https://apt.izzysoft.de/fdroid) alleviate some of these concerns. The IzzyOnDroid repository pulls builds directly from GitHub and is the next best thing to the developers' own repositories. However, it is not something that we can fully recommend, as apps are typically [removed](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) from that repository if they are later added to the main F-Droid repository. While that makes sense (since the goal of that particular repository is to host apps before they're accepted into the main F-Droid repository), it can leave you with installed apps which no longer receive updates.

That said, the [F-Droid](https://f-droid.org/en/packages) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid) repositories are home to countless apps, so they can be a useful tool to search for and discover open-source apps that you can then download through other means such as the Play Store, Aurora Store, or by getting the APK directly from the developer. You should use your best judgement when looking for new apps via this method, and keep an eye on how frequently the app is updated. Outdated apps may rely on unsupported libraries, among other things, posing a potential security risk.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

In some rare cases, the developer of an app will only distribute it through F-Droid ([Gadgetbridge](https://gadgetbridge.org) is one example of this). If you really need an app like that, we recommend using the newer [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) client instead of the original F-Droid app to obtain it. F-Droid Basic supports automatic background updates without privileged extension or root, and has a reduced feature set (limiting attack surface).

</div>
