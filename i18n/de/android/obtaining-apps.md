---
title: Apps beschaffen
---

Es gibt viele Möglichkeiten, Android-Apps privat zu beziehen, auch aus dem Play Store, ohne mit Google Play Services zu interagieren. Wir empfehlen die folgenden Methoden, um Anwendungen für Android zu erhalten, aufgelistet in der Reihenfolge ihrer Präferenz.

## Obtainium

<div class="admonition recommendation" markdown>

![Obtainium Logo](../assets/img/android/obtainium.svg){ align=right }

**Obtainium** ist ein App-Manager, der es dir erlaubt, Apps direkt von der Veröffentlichungsseite des Entwicklers (z. B. GitHub, GitLab, die Website des Entwicklers usw.) zu installieren und zu aktualisieren, anstatt von einem zentralisierten App-Store oder Repository. Es unterstützt automatische Hintergrundupdates auf Android 12 und höher.

[:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium ermöglicht es dir, APK-Installationsdateien aus einer Vielzahl von Quellen herunterzuladen, und es liegt an dir, sicherzustellen, dass diese Quellen und Apps legitim sind. Die Verwendung von Obtainium zur Installation von Signal von [Signal's APK Seite] (https://signal.org/android/apk) sollte beispielsweise problemlos möglich sein, aber die Installation von APK-Repositories von Drittanbietern wie Aptoide oder APKPure kann zusätzliche Risiken bergen. Das Risiko, ein bösartiges _Update_ zu installieren, ist geringer, da Android selbst überprüft, ob alle App-Updates vom gleichen Entwickler signiert sind wie die vorhandene App auf deinem Handy, bevor sie installiert werden.

## GrapheneOS App Store

Der App-Store von GrapheneOS ist auf [GitHub](https://github.com/GrapheneOS/Apps/releases) verfügbar. Er unterstützt Android 12 und höher und kann sich selbst aktualisieren. Der App-Store enthält eigenständige Anwendungen, die vom GrapheneOS-Projekt entwickelt wurden, z. B. [Auditor](../device-integrity.md#auditor-android), [Camera](general-apps.md#secure-camera) und [PDF Viewer](general-apps.md#secure-pdf-viewer). Wenn du nach diesen Anwendungen suchst, empfehlen wir dringend, sie aus dem App Store von GrapheneOS zu beziehen, anstatt aus dem Play Store, da die Apps in ihrem Store mit der eigenen Signatur des GrapheneOS-Projekts signiert sind, auf die Google keinen Zugriff hat.

## Aurora Store

Der Google Play Store erfordert ein Google-Konto, um sich anzumelden, was der Privatsphäre nicht gerade zuträglich ist. Du kannst dies umgehen, indem du einen alternativen Client wie den Aurora Store verwendest.

<div class="admonition recommendation" markdown>

![Aurora Store Logo](../assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** is a Google Play Store client which does not require a Google account, Google Play Services, or microG to download apps.

[:octicons-home-16: Homepage](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Aurora Store does not allow you to download paid apps with their anonymous account feature. You can optionally log in with your Google account with Aurora Store to download apps you have purchased, which does give access to the list of apps you've installed to Google. However, you still benefit from not requiring the full Google Play client and Google Play Services or microG on your device.

## Manuell mit RSS-Benachrichtigungen

For apps that are released on platforms like GitHub and GitLab, you may be able to add an RSS feed to your [news aggregator](../news-aggregators.md) that will help you keep track of new releases.

![RSS APK](../assets/img/android/rss-apk-light.png#only-light) ![RSS APK](../assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](../assets/img/android/rss-changes-light.png#only-light) ![APK Changes](../assets/img/android/rss-changes-dark.png#only-dark)

### GitHub

On GitHub, using [Secure Camera](general-apps.md#secure-camera) as an example, you would navigate to its [releases page](https://github.com/GrapheneOS/Camera/releases) and append `.atom` to the URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

### GitLab

On GitLab, using [Aurora Store](#aurora-store) as an example, you would navigate to its [project repository](https://gitlab.com/AuroraOSS/AuroraStore) and append `/-/tags?format=atom` to the URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

### Verifying APK Fingerprints

If you download APK files to install manually, you can verify their signature with the [`apksigner`](https://developer.android.com/studio/command-line/apksigner) tool, which is a part of Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Install [Java JDK](https://oracle.com/java/technologies/downloads).

2. Download the [Android Studio command line tools](https://developer.android.com/studio#command-tools).

3. Extract the downloaded archive:

   ```bash
   unzip commandlinetools-*.zip
   cd cmdline-tools
   ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
   ```

4. Run the signature verification command:

   ```bash
   ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
   ```

5. The resulting hashes can then be compared with another source. Some developers such as Signal [show the fingerprints](https://signal.org/android/apk) on their website.

   ```bash
   Signer #1 certificate DN: CN=GrapheneOS
   Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
   Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
   Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
   ```

## F-Droid

![F-Droid Logo](../assets/img/android/f-droid.svg){ align=right width=120px }

\==We only recommend F-Droid as a way to obtain apps which cannot be obtained via the means above.== F-Droid is often recommended as an alternative to Google Play, particularly within the privacy community. The option to add third-party repositories and not be confined to Google's walled garden has led to its popularity. F-Droid additionally has [reproducible builds](https://f-droid.org/en/docs/Reproducible_Builds) for some applications and is dedicated to free and open-source software. However, there are some security-related downsides to how F-Droid builds, signs, and delivers packages:

Due to their process of building apps, apps in the _official_ F-Droid repository often fall behind on updates. F-Droid maintainers also reuse package IDs while signing apps with their own keys, which is not ideal as it gives the F-Droid team ultimate trust. Additionally, the requirements for an app to be included in the official F-Droid repo are less strict than other app stores like Google Play, meaning that F-Droid tends to host a lot more apps which are older, unmaintained, or otherwise no longer meet [modern security standards](https://developer.android.com/google/play/requirements/target-sdk).

Other popular third-party repositories for F-Droid such as [IzzyOnDroid](https://apt.izzysoft.de/fdroid) alleviate some of these concerns. The IzzyOnDroid repository pulls builds directly from GitHub and is the next best thing to the developers' own repositories. However, it is not something that we can fully recommend, as apps are typically [removed](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) from that repository if they are later added to the main F-Droid repository. While that makes sense (since the goal of that particular repository is to host apps before they're accepted into the main F-Droid repository), it can leave you with installed apps which no longer receive updates.

That said, the [F-Droid](https://f-droid.org/en/packages) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid) repositories are home to countless apps, so they can be a useful tool to search for and discover open-source apps that you can then download through other means such as the Play Store, Aurora Store, or by getting the APK directly from the developer. You should use your best judgement when looking for new apps via this method, and keep an eye on how frequently the app is updated. Outdated apps may rely on unsupported libraries, among other things, posing a potential security risk.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

In some rare cases, the developer of an app will only distribute it through F-Droid ([Gadgetbridge](https://gadgetbridge.org) is one example of this). If you really need an app like that, we recommend using the newer [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) client instead of the original F-Droid app to obtain it. F-Droid Basic supports automatic background updates without privileged extension or root, and has a reduced feature set (limiting attack surface).

</div>
