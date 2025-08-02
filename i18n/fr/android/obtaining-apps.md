---
title: "Obtenir des applications"
description: Nous recommandons ces méthodes pour obtenir des applications sur Android sans interagir avec les services Google Play.
---

Il existe de nombreuses façons d'obtenir des applications Android en privé, même à partir du Play Store, sans interagir avec les services Google Play. Nous recommandons les méthodes suivantes pour obtenir des applications sur Android, par ordre de préférence.

## Obtainium

<div class="admonition recommendation" markdown>

![Logo Obtainium](../assets/img/android/obtainium.svg){ align=right }

**Obtainium** est un gestionnaire d'applications qui permet d'installer et de mettre à jour des applications directement à partir de la page de publication du développeur (c.-à-d. GitHub, GitLab, le site web du développeur, etc.), plutôt que depuis un dépôt/magasin d'application centralisé. Il prend en charge les mises à jour automatique en arrrière plan sur Android 12 et versions ultérieures.

[:octicons-repo-16: Dépôt](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Code source" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium permet de télécharger les fichiers d'installation APK à partir d'une grande variété de sources, et c'est à vous de vous assurer que ces sources et ces applications sont authentiques. Par exemple, installer Signal depuis [Page d'accueil de l'APK de Signal] (https://signal.org/android/apk) ne devrait pas poser de problèmes, mais l'installer depuis des dépôts d'APK tiers comme Aptoide ou APKPure peut présenter des risques supplémentaires. Le risque d'installer une _mise à jour_ malveillante est plus faible car Android vérifie lui-même que toutes les mises à jour d'application sont signées du même développeur que les applications existantes sur votre téléphone avant de les installer.

## Magasin d'applications de GrapheneOS

Le magasin d'applications de GrapheneOS est disponible sur [GitHub](https://github.com/GrapheneOS/Apps/releases). Il prend en charge Android 12 et les versions ultérieures et peut se mettre à jour lui-même. Le magasin d'applications contient des applications autonomes créées par le projet GrapheneOS, telles que [Auditor](../device-integrity.md#auditor-android), [Camera](general-apps.md#secure-camera) et [PDF Viewer](general-apps.md#secure-pdf-viewer). Si vous souhaitez installer ces appllications, nous recommandons vivement de les télécharger depuis le magasin d'application GrapheneOS plutôt que depuis le Play Store, car les applications de leur magasin sont signées par la signature du projet GrapheneOS, à laquelle Google n'a pas accès.

## Aurora Store

Le Google Play Store nécessite un compte Google pour se connecter, ce qui n'est pas optimal en termes de confidentialité. Pour contourner le problème, vous pouver utiliser un client alternatif comme Aurora Store.

<div class="admonition recommendation" markdown>

![Aurora Store logo](../assets/img/android/aurora-store.webp){ align=right }

**Aurora Store** est un client du Google Play Store qui peut télécharrger des applications sans compte Google, ni les Google Play Services, ni microG.

[:octicons-home-16: Page d'accueil](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Politique de confidentialité" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Il n'est pas possible de télécharger des applications payantes avec la fonction compte anonyme". Il est possible d'éventuellement se connecter sur Aurora Store avec un compte Google pour télécharger des applications déjà achetées, cela donne cependant accès à Google à la liste des applications installées. Cependant, vous bénéficiez toujours de l'avantage de ne pas avoir besoin du client Google Play complet ni des Google Play Services ou de microG sur votre appareil.

## Manuellement avec les notifications RSS

Pour les applications publiées sur des plateformes telles que GitHub et GitLab, vous pouvez ajouter un flux RSS à votre [aggrégateur d'actualités](../news-aggregators.md) qui vous permet de suivre les nouvelles versions.

![RSS APK](../assets/img/android/rss-apk-light.png#only-light) ![RSS APK](../assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](../assets/img/android/rss-changes-light.png#only-light) ![APK Changes](../assets/img/android/rss-changes-dark.png#only-dark)

### GitHub

Sur GitHub, en utilisant [Secure Camera](general-apps.md#secure-camera) comme exemple, vous naviguerez vers sa [page de publication](https://github.com/GrapheneOS/Camera/releases) et ajouterez `.atom` à l'URL :

`https://github.com/GrapheneOS/Camera/releases.atom`

### GitLab

Sur GitLab, en utilisant [Aurora Store](#aurora-store) comme exemple, vous naviguerez vers [le dépôt du projet](https://gitlab.com/AuroraOSS/AuroraStore) et ajouterez `/-/tags?format=atom` à l'URL :

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

### Vérifier les empreintes numériques des APK

Lorsque vous téléchargez des fichiers APK à installer manuellement, vous pouvez vérifier leur signature avec l'outil [`apksigner`](https://developer.android.com/studio/command-line/apksigner), qui fait partie des [build-tools](https://developer.android.com/studio/releases/build-tools) d'Android.

1. Installer [Java JDK](https://oracle.com/java/technologies/downloads).

2. Télécharger les [outils de ligne de commande Android Studio] (https://developer.android.com/studio#command-tools).

3. Extraire l'archive téléchargée :

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. Exécuter la commande de vérification de la signature :

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. Les hashs qui en résultent peuvent ensuite être comparés à une autre source. Certains développeurs comme Signal [montrent les empreintes numériques] (https://signal.org/android/apk) sur leur site web.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

## F-Droid

![F-Droid logo](../assets/img/android/f-droid.svg){ align=right width=120px }

\==Nous recommandons F-Droid uniquement lorsque les applications ne peuvent pas être obtenues par les moyens ci-dessus.== F-Droid est souvent recommandé comme alternative à Google Play, en particulier dans la communauté de la protection de la vie privée. Sa popularité vient de la possibilité d''ajouter des dépôts tier et de ne pas être limité au jardin clos de Google. F-Droid propose également des [versions reproductibles](https://f-droid.org/en/docs/Reproducible_Builds) pour certaines applications et est dédié aux logiciels libres et open-source. Cependant, la façon dont F-Droid construit, signe et livre les paquets présente quelques inconvénients liés à la sécurité :

En raison de leur processus de création, les applications du dépôt _officiel_ F-Droid sont souvent en retard sur les mises à jour. L'équipe de maintenance de F-Droid réutilise également les identifiants des paquets tout en signant les applications avec leurs propres clés, ce qui n'est pas idéal car cela implique de faire totalement confiance à l'équipe F-Droid. De plus, pour qu'une application soit incluse dans le dépôt officiel F-Droid, les conditions requises sont moins strictes que pour d'autres magasins comme le Play Store. Cela signifie que F-Droid propose beaucoup plus d'applications vieilles, non maintenues, ou qui ne répondent plus aux [standards modernes de sécurité](https://developer.android.com/google/play/requirements/target-sdk).

D'autres dépôts populaire sur F-Droid, comme [IzzyOnDroid](https://apt.izzysoft.de/fdroid) atténuent certains de ces problèmes. Le dépôt IzzyOnDroid récupère les builds directement depuis les forges (GitHub, GitLab, etc.) c'est ce qui se rapproche le plus des propres dépôts des développeurs. Il donne également accès à des [builds reproductibles](https://android.izzysoft.de/articles/named/iod-rbs-mirrors-clients) de centaines d'applications et font vérifier par des développeurs la reproductibilité des APKs signés par des développeurs. De plus, l'équipe de IzzyOnDroid procède à une [analyse de sécurité complémentaires](https://android.izzysoft.de/articles/named/iod-scan-apkchecks) des applications hébergées sur le répertoire, qui conduisent généralement à des [discussions](https://github.com/gouravkhunger/QuotesApp/issues/22) entre eux et les développeurs en vue d'améliorer la protection de la vie privée des applications. Dans [certaines circomstances](https://gitlab.com/IzzyOnDroid/repo#are-apps-removed-from-the-repo--and-when-does-that-happen), une application peut parfois être retirée du dépôt IzzyOnDroid.

Les dépôts [F-Droid](https://f-droid.org/en/packages) et [IzzyOnDroid](https://apt.izzysoft.de/fdroid) hébergent un grand nombre d'applications et peuvent permettre de chercher et découvrir des applications open-source qu'il est possible de télécharger ensuite par d'autres moyens comme le Play Store, Aurora Store ou en obtenant l'APK directement auprès du développeur. Vous devez faire preuve de discernement lorsque vous recherchez de nouvelles applications par cette méthode, et surveiller la fréquence des mises à jour de l'application. Des applications obsolètes peuvent, entre autre, s'appuyer sur des bibliothèques non maintenues, ce qui peut constituer un risque pour la sécurité.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

Dans de rares cas, le développeur d'une application ne la distribue que par l'intermédiaire de F-Droid ([Gadgetbridge](../health-and-wellness.md#gadgetbridge) en est un exemple). Si vous avez vraiment besoin d'une telle application, nous vous recommandons d'utiliser le client plus récent [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) au lieu de l'application F-Droid originale pour l'obtenir. F-Droid Basic peut effectuer des mises à jour en arrière-plan, sans autorisations privilégiées ou root, et possède un ensemble de fonctionnalités réduit (limitant ainsi les possiblités d'attaque).

</div>
