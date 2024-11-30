---
title: Apps beschaffen
description: We recommend these methods for obtaining applications on Android without interacting with Google Play Services.
---

Es gibt viele Möglichkeiten, Android-Apps privat zu beziehen, auch aus dem Play Store, ohne mit Google Play Services zu interagieren. Wir empfehlen die folgenden Methoden, um Anwendungen für Android zu erhalten, aufgelistet in der Reihenfolge ihrer Präferenz.

## Obtainium

<div class="admonition recommendation" markdown>

![Obtainium Logo](../assets/img/android/obtainium.svg){ align=right }

**Obtainium** ist ein App-Manager, der es dir erlaubt, Apps direkt von der Veröffentlichungsseite des Entwicklers (z. B. GitHub, GitLab, die Website des Entwicklers usw.) zu installieren und zu aktualisieren, anstatt von einem zentralisierten App-Store oder Repository. Es unterstützt automatische Hintergrundupdates auf Android 12 und höher.

[:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Spenden }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium ermöglicht es dir, APK-Installationsdateien von einer Vielzahl von Quellen herunterzuladen. Es liegt an dir, sicherzustellen, dass diese Quellen und Apps legitim sind. Die Verwendung von Obtainium zur Installation von Signal von [Signal's APK Seite](https://signal.org/android/apk) sollte beispielsweise problemlos möglich sein, aber die Installation von APK-Repositories von Drittanbietern wie Aptoide oder APKPure kann zusätzliche Risiken bergen. Das Risiko, ein bösartiges _Update_ zu installieren, ist geringer, da Android selbst überprüft, ob alle App-Updates vom gleichen Entwickler signiert sind wie die vorhandene App auf deinem Handy, bevor sie installiert werden.

## GrapheneOS App Store

Der App-Store von GrapheneOS ist auf [GitHub](https://github.com/GrapheneOS/Apps/releases) verfügbar. Er unterstützt Android 12 und höher und kann sich selbst aktualisieren. Der App-Store enthält eigenständige Anwendungen, die vom GrapheneOS-Projekt entwickelt wurden, z. B. [Auditor](../device-integrity.md#auditor-android), [Camera](general-apps.md#secure-camera) und [PDF Viewer](general-apps.md#secure-pdf-viewer). Wenn du nach diesen Anwendungen suchst, empfehlen wir dringend, sie aus dem App Store von GrapheneOS zu beziehen, anstatt aus dem Play Store, da die Apps in ihrem Store mit der eigenen Signatur des GrapheneOS-Projekts signiert sind, auf die Google keinen Zugriff hat.

## Aurora Store

Der Google Play Store erfordert ein Google-Konto, um sich anzumelden, was der Privatsphäre nicht gerade zuträglich ist. Du kannst dies umgehen, indem du einen alternativen Client wie den Aurora Store verwendest.

<div class="admonition recommendation" markdown>

![Aurora Store Logo](../assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** ist ein Client für den Google Play Store, der kein Google-Konto, Google Play-Dienste oder microG benötigt, um Apps herunterzuladen.

[:octicons-home-16: Homepage](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Datenschutzrichtlinie" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Der Aurora Store erlaubt es dir nicht, kostenpflichtige Apps mit der anonymen Kontofunktion herunterzuladen. Du kannst dich optional mit deinem Google-Konto im Aurora Store anmelden, um Apps herunterzuladen, die du gekauft hast. Das bedeutet jedoch, dass Google Zugriff auf die Liste der Apps, die du installiert hast, bekommt. Dennoch profitierst du davon, dass du nicht den vollständigen Google Play-Client und Google Play-Dienste oder microG auf deinem Gerät benötigst.

## Manuell mit RSS-Benachrichtigungen

Für Apps, die auf Plattformen wie GitHub und GitLab veröffentlicht werden, kannst du möglicherweise einen RSS-Feed zu deinem [News-Aggregator](../news-aggregators.md) hinzufügen, der dir hilft, neue Veröffentlichungen zu verfolgen.

![RSS APK](../assets/img/android/rss-apk-light.png#only-light) ![RSS APK](../assets/img/android/rss-apk-dark.png#only-dark) ![APK-Änderungen](../assets/img/android/rss-changes-light.png#only-light) ![APK-Änderungen](../assets/img/android/rss-changes-dark.png#only-dark)

### GitHub

Auf GitHub würdest du, beispielsweise bei [Secure Camera](general-apps.md#secure-camera), auf dessen [Releases-Seite](https://github.com/GrapheneOS/Camera/releases) gehen und `.atom` an die URL anhängen:

`https://github.com/GrapheneOS/Camera/releases.atom`

### GitLab

Auf GitLab, nehmen wir [Aurora Store](#aurora-store) als Beispiel, würdest du zum [Projekt Repository](https://gitlab.com/AuroraOSS/AuroraStore) gehen und `/-/tags?format=atom` an die URL anhängen:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

### APK-Fingerabdrücke verifizieren

Wenn du APK-Dateien herunterlädst, um sie manuell zu installieren, kannst du ihre Signatur mit dem Tool [`apksigner`](https://developer.android.com/studio/command-line/apksigner) überprüfen, welches Teil von Android [build-tools](https://developer.android.com/studio/releases/build-tools) ist.

1. Installiere das [Java JDK](https://oracle.com/java/technologies/downloads).

2. Lade die [Android Studio command line tools](https://developer.android.com/studio#command-tools) herunter.

3. Entpacke das heruntergeladene Archiv:

   ```bash
   unzip commandlinetools-*.zip
   cd cmdline-tools
   ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
   ```

4. Führe den Befehl zur Signaturüberprüfung aus:

   ```bash
   ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
   ```

5. Die resultierenden Hashes können dann mit einer anderen Quelle verglichen werden. Einige Entwickler wie Signal [zeigen die Fingerabdrücke](https://signal.org/android/apk) auf ihrer Website.

   ```bash
   Signer #1 certificate DN: CN=GrapheneOS
   Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
   Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
   Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
   ```

## F-Droid

![F-Droid Logo](../assets/img/android/f-droid.svg){ align=right width=120px }

\==Wir empfehlen F-Droid nur, um Apps zu erhalten, die auf den oben genannten Wegen nicht erhältlich sind.== F-Droid wird oft als Alternative zu Google Play empfohlen, insbesondere in der Privacy-Community. Die Möglichkeit, Repositories von Drittanbietern hinzuzufügen und nicht auf den „Walled Garden“ von Google beschränkt zu sein, hat zu seiner Popularität geführt. F-Droid bietet außerdem [reproduzierbare Builds](https://f-droid.org/en/docs/Reproducible_Builds) für einige Anwendungen und widmet sich freier und quelloffener Software. Die Art und Weise, wie F-Droid Pakete erstellt, signiert und ausliefert, birgt jedoch einige sicherheitsrelevante Nachteile:

Aufgrund des Prozesses zur Erstellung von Apps hinken die Apps im _offiziellen_ F-Droid-Repository oft bei Updates hinterher. Auch verwenden die F-Droid-Maintainer wiederholt Paket-IDs, während sie Apps mit ihren eigenen Schlüsseln signieren, was nicht ideal ist, da es dem F-Droid-Team ultimatives Vertrauen gewährt. Darüber hinaus sind die Anforderungen für eine App, die in das offizielle F-Droid-Repository aufgenommen werden soll, weniger streng als bei anderen App-Stores wie Google Play. Dies bedeutet, dass F-Droid tendenziell viel mehr Apps hostet, die älter sind, nicht gewartet werden oder anderweitig nicht mehr den [modernen Sicherheitsstandards](https://developer.android.com/google/play/requirements/target-sdk) entsprechen.

Andere beliebte Repositories von Drittanbietern für F-Droid wie [IzzyOnDroid](https://apt.izzysoft.de/fdroid) mildern einige dieser Bedenken. The IzzyOnDroid repository pulls builds directly from code forges (GitHub, GitLab, etc.) and is the next best thing to the developers' own repositories. They also offer [reproducible builds](https://android.izzysoft.de/articles/named/iod-rbs-mirrors-clients) for hundreds of applications and have developers who verify the reproducibility of developer-signed APKs. Furthermore, the IzzyOnDroid team conducts [additional security scans](https://android.izzysoft.de/articles/named/iod-scan-apkchecks) of apps housed in the repo, which usually result in [deliberations](https://github.com/gouravkhunger/QuotesApp/issues/22) between them and app developers toward privacy improvements in their apps. Note that apps may be removed from the IzzyOnDroid repo in [certain circumstances](https://gitlab.com/IzzyOnDroid/repo#are-apps-removed-from-the-repo--and-when-does-that-happen).

The [F-Droid](https://f-droid.org/en/packages) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid) repositories are home to countless apps, so they can be useful places to search for and discover open-source apps that you can then download through other means such as the Play Store, Aurora Store, or by getting the APK directly from the developer. You should use your best judgment when looking for new apps via this method, and keep an eye on how frequently the app is updated. Veraltete Apps können sich unter anderem auf nicht unterstützte Bibliotheken verlassen, was ein potenzielles Sicherheitsrisiko darstellt.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

In einigen seltenen Fällen wird der Entwickler einer App diese nur über F-Droid veröffentlichen ([Gadgetbridge](https://gadgetbridge.org) ist ein Beispiel dafür). Wenn du wirklich eine solche App brauchst, empfehlen wir den neueren [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) Client anstelle der ursprünglichen F-Droid App zu verwenden. F-Droid Basic unterstützt automatische Hintergrundaktualisierungen ohne privilegierte Zugriffsrechte oder Root und hat einen reduzierten Funktionsumfang (Begrenzung der Angriffsfläche).

</div>
