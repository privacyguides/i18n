---
title: Sur Android
icon: simple/android
description: Android est un système d'exploitation open source doté de solides protections de sécurité, ce qui en fait notre premier choix pour les téléphones.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Logo d'Android](../assets/img/android/android.svg){ align=right }

**Android Open Source Project** est un système d'exploitation mobile sécurisé doté d'un solide [sandboxing d'application](https://source.android.com/security/app-sandbox), d'un [démarrage vérifié](https://source.android.com/security/verifiedboot) (AVB), et d'un solide système de contrôle des [autorisations](https://developer.android.com/guide/topics/permissions/overview).

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="Source Code" }

[Nos conseils sur Android :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## Protections de sécurité

Les éléments clés du modèle de sécurité d'Android sont le [démarrage vérifié](#verified-boot), les [mises à jour du micrologiciel](#firmware-updates) et un [système d'autorisation](#android-permissions) robuste. Ces fonctionnalités de sécurité importantes forment la ligne de base des critères minimums pour nos recommandations [de téléphone mobile](../mobile-phones.md) et [de systèmes d'exploitation Android alternatifs](../android/distributions.md).

### Démarrage vérifié

Le [**Démarrage vérifié**](https://source.android.com/security/verifiedboot) est un élément important du modèle de sécurité d'Android. Il fournit une protection contre les attaques de type [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack), la persistance de logiciels malveillants et garantit que les mises à jour de sécurité ne peuvent pas être rétrogradées grâce au [rollback protection](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

Les versions supérieures à Android 10 ont abandonné le chiffrement complet du disque au profit d'un chiffrement plus souple [basé sur les fichiers](https://source.android.com/security/encryption/file-based). Vos données sont chiffrées à l'aide de clés de chiffrement propres à chaque utilisateur, tandis que les fichiers du système d'exploitation ne sont pas chiffrés.

Le Démarrage Vérifié garantit l'intégrité des fichiers du système d'exploitation, empêchant un adversaire disposant d'un accès physique d'altérer ou d'installer des logiciels malveillants sur l'appareil. Dans le cas improbable où un logiciel malveillant parviendrait à exploiter d'autres parties du système et à obtenir un accès privilégié, le Démarrage Vérifié empêchera et annulera toutes modifications apportées à la partition système lors du redémarrage de l'appareil.

Malheureusement, les fabricants sont tenus de prendre en charge le Démarrage Vérifié uniquement sur leurs distributions Android d'origine. Seuls quelques fabricants OEM, tels que Google, prennent en charge l'enrolement de clés AVB personnalisées sur leurs appareils. De plus, certaines ROM dérivées d'AOSP tels que LineageOS ou /e/ OS ne prennent pas en charge le Démarrage Vérifié, même si le matériel peut le prendre en charge. Nous vous recommandons de vérifier le support de cette fonctionnalité **avant** d'acheter un nouvel appareil. Les dérivés d'AOSP qui ne prennent pas en charge le Démarrage Vérifié ne sont **pas** recommandés.

De nombreux contructeurs ont également une implémentation défectueuse du Démarrage Vérifié dont vous devez être conscient au-delà de leur marketing. Par exemple, les Fairphone 3 et 4 ne sont pas sécurisés par défaut, car le [chargeur d'amorçage d'origine fait confiance à la clé de signature AVB publique](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). Cela contourne le Démarrage Vérifié sur un appareil Fairphone d'origine, car le système démarrera des systèmes d'exploitation Android alternatifs tels que (comme /e/) [sans aucun avertissement](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) sur l'utilisation d'un système d'exploitation personnalisé.

### Mises à jour du micrologiciel

Les **mises à jour du firmware** sont essentielles au maintien de la sécurité de votre appareil. Les fabriquants ont conclu des accords de prise de en charge avec leurs partenaires pour fournir les mises à jour des composants closed-source pendant une période limitée. Celles-ci sont détaillées dans les [Bulletins de Sécurité Android](https://source.android.com/security/bulletin) mensuels.

Comme les composants du téléphone, tels que le processeur et les technologies radio, reposent sur des composants closed-source, les mises à jour doivent être fournies par leur fabricants respectifs. Par conséquent, il est important que vous achetiez un appareil qui reçoit activement des mises à jours. [Qualcomm](https://qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) et [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) prennent en charge leurs appareils pendant 4 ans, alors que les produits moins chers ont souvent des prises en charge plus courts. Avec l'introduction du [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google fabrique maintenant son propre SoC et fournira un minimum de 5 ans de mises à jour. Avec l'introduction de la série Pixel 8, Google a porté cette intervalle de prise en charge à 7 ans.

Les appareils qui ne sont plus pris en charge par le fabricant du SoC ne peuvent pas recevoir de mises à jour du micrologiciel de la part des fabricants ou des distributeurs. Cela signifie que les problèmes de sécurité de ces appareils ne seront pas corrigés.

Fairphone, par exemple, commercialise son appareil Fairphone 4 comme bénéficiant de 6 ans de mises à jour. Cependant, le SoC (Qualcomm Snapdragon 750G sur le Fairphone 4) a une date de fin de vie (EOL) beaucoup plus courte. Cela signifie que les mises à jour de sécurité du micrologiciel de Qualcomm pour le Fairphone 4 prendront fin en septembre 2023, que Fairphone continue ou non à publier des mises à jour de sécurité logicielle.

### Autorisations d'Android

Les [**autorisations sur Android**](https://developer.android.com/guide/topics/permissions/overview) vous permettent de contrôler ce que les applications ont le droit d'accéder. Google apporte régulièrement des [améliorations](https://developer.android.com/about/versions/11/privacy/permissions) sur le système d'autorisations à chaque nouvelle version d'Android. Toutes les applications que vous installez sont strictement [isolées](https://source.android.com/security/app-sandbox), il n'est donc pas nécessaire d'installer des applications antivirus.

Un smartphone équipé de la dernière version d'Android sera toujours plus sûr qu'un vieux smartphone équipé d'un antivirus que vous avez payé. Il est préférable de ne pas payer pour un logiciel antivirus et d'économiser pour acheter un nouveau smartphone, comme un [Google Pixel](../mobile-phones.md#google-pixel).

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

- Une autorisation pour un [accès aux wifi à proximité](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). Les applications utilisaient couramment les adresses MAC des points d'accès Wi-Fi situés à proximités pour suivre la localisation d'un utilisateur.
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

Des applications respectueuses de la vie privée telles que [Bitwarden](https://reports.exodus-privacy.eu.org/fr/reports/com.x8bit.bitwarden/latest) peuvent afficher certains traqueurs tels que [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/fr/trackers/49). Cette bibliothèque comprend [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) qui peut fournir des [notifications push](https://fr.wikipedia.org/wiki/Server_push) dans les applications. C'est [le cas](https://fosstodon.org/@bitwarden/109636825700482007) avec Bitwarden. Cela ne signifie pas que Bitwarden utilise toutes les fonctionnalités d'analyse fournies par Google Firebase Analytics.

</div>

## Fonctionnalités de protection de la vie privée

### Profils utilisateurs

Les **profils d'utilisateurs** multiples se trouvent dans :gear: **Paramètres** → **Système** → **Utilisateurs** et constituent le moyen le plus simple d'isoler dans Android.

Avec les profils d'utilisateur, vous pouvez imposer des restrictions à un profil spécifique, par exemple : passer des appels, utiliser des SMS ou installer des applications sur l'appareil. Chaque profil est chiffré à l'aide de sa propre clé de chiffrement et ne peut accéder aux données d'aucun autre profil. Même le propriétaire de l'appareil ne peut pas voir les données des autres profils sans connaître leur mot de passe. Les profils d'utilisateurs multiples est une méthode d'isolement plus sécurisée.

### Profil professionnel

Les [**Profils Professionnels**](https://support.google.com/work/android/answer/6191949) sont une autre façon d'isoler des applications de manière individuelles et peuvent s'avérer plus pratiques que des profils d'utilisateur séparés.

Une application de **gestionnaire d'appareil** telle que [Shelter](../android/general-apps.md#shelter) est nécessaire pour créer un profil professionnel sans MDM d'entreprise, à moins que vous n'utilisiez un système d'exploitation Android personnalisé qui en comprend une.

Le profil professionnel dépend d'un gestionnaire d'appareil pour fonctionner. Les fonctionnalités telles que la *Navigation de Fichiers* et le *blocage de la recherche de contacts* ou tout autre type de fonctionnalités d'isolation doivent être implémentées par le gestionnaire. Vous devez également faire entièrement confiance à l'application de gestionnaire d'appareil, car elle a un accès total à vos données au sein du profil professionnel.

Cette méthode est généralement moins sécurisée qu'un profil utilisateur secondaire, mais elle vous permet d'exécuter simultanément des applications dans les profils professionnel et personnel.

### L'espace privé

L'**espace privé** est une fonctionnalité introduite dans Android 15 qui ajoute un autre moyen d'isoler individuellement des applications. Vous pouvez configurer un espace privé dans le profil du propriétaire en accédant à :gear: **Paramètres** → **Sécurité & Confidentialité** → **Espace privé**. Une fois configuré, votre espace privé se trouve en bas du tiroir d'applications.

Comme les profils d'utilisateur, un espace privé est chiffré à l'aide de sa propre clé de chiffrement, et vous avez la possibilité de configurer une méthode de déverrouillage différente. Comme pour les profils professionnels, vous pouvez utiliser simultanément les applications du profil propriétaire et de l'espace privé. Les applications lancées à partir d'un espace privé se distinguent par une icône représentant une clé dans un bouclier.

Contrairement aux profils professionnels, l'Espace Privé est une fonctionnalité native d'Android qui ne nécessite pas d'application tierce pour la gérer. C'est pourquoi nous recommandons d'utiliser un espace privé plutôt qu'un profil professionnel, bien que vous puissiez utiliser un profil professionnel en même temps qu'un espace privé.

### Arrêt d'urgence VPN

Android 7 et plus prennent en charge un arrêt d'urgence du VPN et il est disponible sans qu'il soit nécessaire d'installer des applications tierces. Cette fonction permet d'éviter les fuites si le VPN est déconnecté. Il se trouve dans :gear: **Paramètres** → **Réseau & internet** → **VPN** → :gear: → **Bloquer les connexions sans VPN**.

### Boutons à bascule globaux

Les appareils Android modernes disposent de boutons à bascule permettant de désactiver les services Bluetooth et de localisation. Android 12 a introduit des boutons à bascule pour l'appareil photo et le microphone. Lorsque vous n'utilisez pas ces fonctions, nous vous recommandons de les désactiver. Les applications ne peuvent pas utiliser les fonctions désactivées (même si elles ont reçu une autorisation individuelle) jusqu'à ce qu'elles soient réactivées.

## Services Google

Si vous utilisez un appareil doté des services Google, qu'il s'agisse de votre système d'exploitation d'origine ou d'un système d'exploitation qui intègre les services Google Play sandboxed en toute sécurité, comme GrapheneOS, vous pouvez apporter un certain nombre de modifications supplémentaires pour améliorer votre confidentialité. Nous recommandons toujours d'éviter complètement les services Google ou de limiter les services Google Play à un profil utilisateur/professionnel spécifique en combinant un contrôleur d'appareil comme *Shelter* avec le Sandboxed Google Play de GrapheneOS.

### Programme de Protection Avancé

Si vous avez un compte Google, nous vous suggérons de vous inscrire au [Programme de Protection Avancée](https://landing.google.com/advancedprotection). Il est disponible gratuitement pour toute personne possédant au moins deux clés de sécurité physiques qui prennent en charge le protocole [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online). Vous pouvez également utiliser des [clés d'accès](https://fidoalliance.org/passkeys).

Le Programme de Protection Avancée offre une surveillance accrue des menaces et permet :

- Une authentification à deux facteurs plus stricte ; par exemple, l'utilisation de [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **est obligatoire** et doit interdire l'utilisation de [SMS OTP](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) et [OAuth](../basics/account-creation.md#sign-in-with-oauth)
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

Sur les distributions Android avec [Google Play sandboxé](https://grapheneos.org/usage#sandboxed-google-play), allez à :gear: **Paramètres** → **Applications** → **Google Play sandboxé** → **Paramètres Google** → **Tous les services** → **Publicités**.

- [x] Sélectionnez **Supprimer l'ID publicitaire**

Sur les distributions Android avec des services Google Play privilégiés (comme le système d'exploitation Android d'origine), le paramètre peut se trouver à différents endroits. Vérifiez:

- :gear: **Paramètres** → **Google** → **Annonces**
- :gear: **Paramètres** → **Confidentialité** → **Annonces**

Selon les distributions OEM d'Android, vous aurez la possibilité de supprimer votre identifiant publicitaire ou de *refuser les publicités basées sur les centres d'intérêt*. Il est préférable de supprimer l'identifiant publicitaire lorsque cela est possible. Si ce n'est pas le cas, veillez à refuser la personnalisation des publicités puis à réinitialiser votre identifiant publicitaire.

### SafetyNet et Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) et les [API Play Integrity](https://developer.android.com/google/play/integrity) sont généralement utilisés pour des [applications bancaires](https://grapheneos.org/usage#banking-apps). De nombreuses applications bancaires fonctionneront sans problème sur GrapheneOS avec les services Google Play en sandbox, mais certaines applications non financières ont leurs propres mécanismes anti-tampering rudimentaires qui peuvent échouer. GrapheneOS passe le contrôle `basicIntegrity`, mais pas le contrôle de certification `ctsProfileMatch`. Les appareils équipés d'Android 8 ou d'une version ultérieure sont dotés d'un système d'attestation matérielle qui ne peut être contourné qu'en cas de fuite de clés ou de vulnérabilité grave.

Quant à Google Wallet, nous ne le recommandons pas en raison de sa [politique de confidentialité](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), qui stipule que vous devez manuellement refuser si vous ne voulez pas que votre note de crédit et vos informations personnelles soient partagées avec des services de marketing affiliés.
