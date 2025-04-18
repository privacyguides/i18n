---
title: Introduction à Android
icon: simple/android
description: Android est un système d'exploitation open source doté de solides protections de sécurité, ce qui en fait notre premier choix pour les téléphones.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Logo d'Android](../assets/img/android/android.svg){ align=right }

**Android Open Source Project** est un système d'exploitation mobile sécurisé doté d'un solide [sandboxing d'application](https://source.android.com/security/app-sandbox), d'un [démarrage vérifié](https://source.android.com/security/verifiedboot) (AVB), et d'un solide système de contrôle des [autorisations](https://developer.android.com/guide/topics/permissions/overview).

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="Source Code" }

[Our Android Advice :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## Protections de sécurité

Key components of the Android security model include [verified boot](#verified-boot), [firmware updates](#firmware-updates), and a robust [permission system](#android-permissions). These important security features form the baseline of the minimum criteria for our [mobile phone](../mobile-phones.md) and [custom Android OS](../android/distributions.md) recommendations.

### Démarrage vérifié

[**Verified Boot**](https://source.android.com/security/verifiedboot) is an important part of the Android security model. Il fournit une protection contre les attaques de type [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack), la persistance de logiciels malveillants et garantit que les mises à jour de sécurité ne peuvent pas être rétrogradées grâce au [rollback protection](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

Les versions supérieures à Android 10 ont abandonné le chiffrement complet du disque au profit d'un chiffrement plus souple [basé sur les fichiers](https://source.android.com/security/encryption/file-based). Vos données sont chiffrées à l'aide de clés de chiffrement propres à chaque utilisateur, tandis que les fichiers du système d'exploitation ne sont pas chiffrés.

Le Démarrage Vérifié garantit l'intégrité des fichiers du système d'exploitation, empêchant un adversaire disposant d'un accès physique d'altérer ou d'installer des logiciels malveillants sur l'appareil. Dans le cas improbable où un logiciel malveillant parviendrait à exploiter d'autres parties du système et à obtenir un accès privilégié, le Démarrage Vérifié empêchera et annulera toutes modifications apportées à la partition système lors du redémarrage de l'appareil.

Malheureusement, les fabricants sont tenus de prendre en charge le Démarrage Vérifié uniquement sur leurs distributions Android d'origine. Seuls quelques fabricants OEM, tels que Google, prennent en charge l'enrolement de clés AVB personnalisées sur leurs appareils. De plus, certaines ROM dérivées d'AOSP tels que LineageOS ou /e/ OS ne prennent pas en charge le Démarrage Vérifié, même si le matériel peut le prendre en charge. Nous vous recommandons de vérifier le support de cette fonctionnalité **avant** d'acheter un nouvel appareil. Les dérivés d'AOSP qui ne prennent pas en charge le Démarrage Vérifié ne sont **pas** recommandés.

De nombreux contructeurs ont également une implémentation défectueuse du Démarrage Vérifié dont vous devez être conscient au-delà de leur marketing. Par exemple, les Fairphone 3 et 4 ne sont pas sécurisés par défaut, car le [chargeur d'amorçage d'origine fait confiance à la clé de signature AVB publique](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### Mises à jour du micrologiciel

**Firmware updates** are critical for maintaining security and without them your device cannot be secure. Les fabriquants ont conclu des accords de prise de en charge avec leurs partenaires pour fournir les mises à jour des composants closed-source pendant une période limitée. Celles-ci sont détaillées dans les [Bulletins de Sécurité Android](https://source.android.com/security/bulletin) mensuels.

Comme les composants du téléphone, tels que le processeur et les technologies radio, reposent sur des composants closed-source, les mises à jour doivent être fournies par leur fabricants respectifs. Par conséquent, il est important que vous achetiez un appareil qui reçoit activement des mises à jours. [Qualcomm](https://qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) support their devices for 4 years, while cheaper products often have shorter support cycles. Avec l'introduction du [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google fabrique maintenant son propre SoC et fournira un minimum de 5 ans de mises à jour. Avec l'introduction de la série Pixel 8, Google a porté cette intervalle de prise en charge à 7 ans.

Les appareils qui ne sont plus pris en charge par le fabricant du SoC ne peuvent pas recevoir de mises à jour du micrologiciel de la part des fabricants ou des distributeurs. Cela signifie que les problèmes de sécurité de ces appareils ne seront pas corrigés.

Fairphone, par exemple, commercialise son appareil Fairphone 4 comme bénéficiant de 6 ans de mises à jour. Cependant, le SoC (Qualcomm Snapdragon 750G sur le Fairphone 4) a une date de fin de vie (EOL) beaucoup plus courte. Cela signifie que les mises à jour de sécurité du micrologiciel de Qualcomm pour le Fairphone 4 prendront fin en septembre 2023, que Fairphone continue ou non à publier des mises à jour de sécurité logicielle.

### Autorisations d'Android

[**Permissions on Android**](https://developer.android.com/guide/topics/permissions/overview) grant you control over what apps are allowed to access. Google apporte régulièrement des [améliorations](https://developer.android.com/about/versions/11/privacy/permissions) sur le système d'autorisations à chaque nouvelle version d'Android. Toutes les applications que vous installez sont strictement [isolées](https://source.android.com/security/app-sandbox), il n'est donc pas nécessaire d'installer des applications antivirus.

Un smartphone équipé de la dernière version d'Android sera toujours plus sûr qu'un vieux smartphone équipé d'un antivirus que vous avez payé. It's better not to pay for antivirus software and to save money to buy a new smartphone such as a [Google Pixel](../mobile-phones.md#google-pixel).

Android 10 :

- [Scoped Storage](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) vous donne plus de contrôle sur vos fichiers et peut limiter les applications qui peuvent [accéder au stockage externe](https://developer.android.com/training/data-storage#permissions). Les applications peuvent avoir un répertoire spécifique dans le stockage externe ainsi que la possibilité d'y stocker des types de médias spécifiques.
- Un acès plus strict à la [localisation de l'appareil](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location) en introduisant l'autorisation `ACCESS_BACKGROUND_LOCATION` . Cela empêche les applications d'accéder à la localisation lorsqu'elles fonctionnent en arrière-plan sans l'autorisation expresse de l'utilisateur.

Android 11 :

- [Autorisations uniques](https://developer.android.com/about/versions/11/privacy/permissions#one-time) qui vous permettent d'accorder une autorisation à une application une seule fois.
- [Réinitialisation automatique des autorisations](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset), qui réinitialise [les autorisations d'exécution](https://developer.android.com/guide/topics/permissions/overview#runtime) accordées lors de l'ouverture de l'application.
- Autorisations granulaires pour accéder aux fonctions liées au [numéro de téléphone](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers).

Android 12 :

- Une autorisation pour accorder uniquement la [localisation approximative](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- Réinitialisation automatique des [applications en hibernation](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation).
- [Audit de l'accès aux données](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing) qui permet de déterminer plus facilement quelle partie d'une application effectue un type spécifique d'accès aux données.

Android 13 :

- Une autorisation pour un [accès aux wifi à proximité](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points were a popular way for apps to track a user's location.
- Des [autorisations plus granulaires pour les médias](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), ce qui signifie que vous pouvez accorder l'accès uniquement aux images, aux vidéos ou aux fichiers audio.
- L'utilisation de capteurs en arrière-plan nécessite désormais l'autorisation [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

Une application peut demander une autorisation pour une fonction spécifique qu'elle possède. Par exemple, toute application permettant de scanner des codes QR nécessitera l'autorisation de l'appareil photo. Certaines applications peuvent demander plus d'autorisations qu'elles n'en ont besoin.

[Exodus](https://exodus-privacy.eu.org) peut être utile pour comparer des applications ayant des objectifs similaires. Si une application nécessite de nombreuses autorisations et comporte beaucoup de traqueurs publicitaires et d'analytiques, c'est probablement un mauvais signe. Nous vous recommandons d'examiner les différents traqueurs et de lire leur description plutôt que de vous contenter de **compter leur nombre** et de supposer que tous les éléments énumérés sont égaux.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Si une application est principalement un service web, le suivi peut se faire du côté du serveur. [Facebook](https://reports.exodus-privacy.eu.org/fr/reports/com.facebook.katana/latest/) n'affiche "aucun traqueur" mais piste certainement les intérêts et le comportement des utilisateurs sur le site. Les applications peuvent échapper à la détection en n'utilisant pas les bibliothèques de code standard produites par l'industrie de la publicité, bien que cela soit peu probable.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Des applications respectueuses de la vie privée telles que [Bitwarden](https://reports.exodus-privacy.eu.org/fr/reports/com.x8bit.bitwarden/latest) peuvent afficher certains traqueurs tels que [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/fr/trackers/49). Cette bibliothèque comprend [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) qui peut fournir des [notifications push](https://fr.wikipedia.org/wiki/Server_push) dans les applications. C'est [le cas](https://fosstodon.org/@bitwarden/109636825700482007) avec Bitwarden. That doesn't mean that Bitwarden is using all the analytics features that are provided by Google Firebase Analytics.

</div>

## Fonctionnalités de protection de la vie privée

### Profils utilisateurs

Multiple **user profiles** can be found in :gear: **Settings** → **System** → **Users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps. Chaque profil est chiffré à l'aide de sa propre clé de chiffrement et ne peut accéder aux données d'aucun autre profil. Même le propriétaire de l'appareil ne peut pas voir les données des autres profils sans connaître leur mot de passe. Les profils d'utilisateurs multiples est une méthode d'isolement plus sécurisée.

### Profil professionnel

[**Work Profiles**](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

Le profil professionnel dépend d'un gestionnaire d'appareil pour fonctionner. Les fonctionnalités telles que la *Navigation de Fichiers* et le *blocage de la recherche de contacts* ou tout autre type de fonctionnalités d'isolation doivent être implémentées par le gestionnaire. Vous devez également faire entièrement confiance à l'application de gestionnaire d'appareil, car elle a un accès total à vos données au sein du profil professionnel.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the owner profile and work profile simultaneously.

### Private Space

**Private Space** is a feature introduced in Android 15 that adds another way of isolating individual apps. You can set up a private space in the owner profile by navigating to :gear: **Settings** → **Security & privacy** → **Private space**. Once set up, your private space resides at the bottom of the app drawer.

Like user profiles, a private space is encrypted using its own encryption key, and you have the option to set up a different unlock method. Like work profiles, you can use apps from both the owner profile and private space simultaneously. Apps launched from a private space are distinguished by an icon depicting a key within a shield.

Unlike work profiles, Private Space is a feature native to Android that does not require a third-party app to manage it. For this reason, we generally recommend using a private space over a work profile, though you can use a work profile alongside a private space.

### VPN kill switch

Android 7 et plus prennent en charge un arrêt d'urgence du VPN et il est disponible sans qu'il soit nécessaire d'installer des applications tierces. Cette fonction permet d'éviter les fuites si le VPN est déconnecté. Il se trouve dans :gear: **Paramètres** → **Réseau & internet** → **VPN** → :gear: → **Bloquer les connexions sans VPN**.

### Boutons à bascule globaux

Les appareils Android modernes disposent de boutons à bascule permettant de désactiver les services Bluetooth et de localisation. Android 12 a introduit des boutons à bascule pour l'appareil photo et le microphone. Lorsque vous n'utilisez pas ces fonctions, nous vous recommandons de les désactiver. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Services Google

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play Services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.

### Programme de Protection Avancé

Si vous avez un compte Google, nous vous suggérons de vous inscrire au [Programme de Protection Avancée](https://landing.google.com/advancedprotection). Il est disponible gratuitement pour toute personne possédant au moins deux clés de sécurité physiques qui prennent en charge le protocole [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online). Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

Le Programme de Protection Avancée offre une surveillance accrue des menaces et permet :

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](../basics/account-creation.md#sign-in-with-oauth)
- Seul Google et les applications tierces vérifiées peuvent accéder aux données du compte
- Une analyse des e-mails entrants sur les comptes Gmail pour détecter les tentatives de [hameçonnage](https://en.wikipedia.org/wiki/Phishing#Email_phishing)
- Une [analyse plus stricte de la sécurité du navigateur](https://google.com/chrome/privacy/whitepaper.html#malware) avec Google Chrome
- Un processus de récupération plus strict pour les comptes ayant perdu leurs informations d'identification

 Si vous utilisez des services Google Play non sandboxés (courants sur les systèmes d'exploitation d'origine), le Programme de Protection Avancée est également accompagné d'[avantages supplémentaires](https://support.google.com/accounts/answer/9764949) tels que :

- Ne pas autoriser l'installation d'applications en dehors du Google Play Store, de la boutique d'applications du fournisseur du système d'exploitation ou via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Analyse automatique obligatoire des appareils avec [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Avertissement concernant les applications non vérifiées

### Mise à jour du système avec Google Play

Dans le passé, les mises à jour de sécurité d'Android devaient être envoyées par le fournisseur du système d'exploitation. Android est devenu plus modulaire à partir d'Android 10, et Google peut envoyer des mises à jour de sécurité pour **certains** composants du système via les services Google Play privilégiés.

Si vous avez un appareil sous Android 10 minimum qui n'est plus supporté et que vous ne pouvez pas installer l'un des systèmes d'exploitation que nous recommandons sur votre appareil, vous feriez mieux de vous en tenir à votre installation Android d'origine (par opposition à un système d'exploitation non répertorié ici, tel que LineageOS ou /e/ OS). Cela vous permettra de recevoir **certains** correctifs de sécurité de Google, sans enfreindre le modèle de sécurité Android en utilisant par exemple un dérivé d'Android non sécurisé et augmentant votre surface d'attaque. Nous vous recommanderions néanmoins de passer à un appareil qui est toujours supporté dès que possible.

### L'Identifiant publicitaire

Tous les appareils sur lesquels les Google Play Services sont installés génèrent automatiquement un [identifiant publicitaire](https://support.google.com/googleplay/android-developer/answer/6048248) utilisé pour la publicité ciblée. Désactivez cette fonctionnalité pour limiter les données collectées à votre sujet.

On Android distributions with [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **All services** → **Ads**.

- [x] Select **Delete advertising ID**

On Android distributions with privileged Google Play Services (which includes the stock installation on most devices), the setting may be in one of several locations. Vérifiez:

- :gear: **Paramètres** → **Google** → **Annonces**
- :gear: **Paramètres** → **Confidentialité** → **Annonces**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. Si ce n'est pas le cas, veillez à refuser la personnalisation des publicités puis à réinitialiser votre identifiant publicitaire.

### SafetyNet et Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) et les [API Play Integrity](https://developer.android.com/google/play/integrity) sont généralement utilisés pour des [applications bancaires](https://grapheneos.org/usage#banking-apps). De nombreuses applications bancaires fonctionneront sans problème sur GrapheneOS avec les services Google Play en sandbox, mais certaines applications non financières ont leurs propres mécanismes anti-tampering rudimentaires qui peuvent échouer. GrapheneOS passe le contrôle `basicIntegrity`, mais pas le contrôle de certification `ctsProfileMatch`. Les appareils équipés d'Android 8 ou d'une version ultérieure sont dotés d'un système d'attestation matérielle qui ne peut être contourné qu'en cas de fuite de clés ou de vulnérabilité grave.

Quant à Google Wallet, nous ne le recommandons pas en raison de sa [politique de confidentialité](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), qui stipule que vous devez manuellement refuser si vous ne voulez pas que votre note de crédit et vos informations personnelles soient partagées avec des services de marketing affiliés.
