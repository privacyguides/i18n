---
title: Introduction à Android
icon: simple/android
description: Android est un système d'exploitation open source doté de solides protections de sécurité, ce qui en fait notre premier choix pour les téléphones.
---

![Logo d'Android](../assets/img/android/android.svg){ align=right }

**Android Open Source Project** est un système d'exploitation mobile sécurisé doté d'un solide [sandboxing d'application](https://source.android.com/security/app-sandbox), d'un [démarrage vérifié](https://source.android.com/security/verifiedboot) (AVB), et d'un solide système de contrôle des [autorisations](https://developer.android.com/guide/topics/permissions/overview).

## Nos conseils

### Choisir une distribution Android

Lorsque vous achetez un téléphone Android, le système d'exploitation par défaut est livré avec des applications et des fonctionnalités qui ne font pas partie de l'Android Open-Source Project. Un grand nombre de ces applications - même des applications comme l'app Téléphone qui fournissent des fonctions système de base - nécessitent des intégrations invasives avec les services Google Play, qui demandent à leur tour des privilèges pour accéder à vos fichiers, au stockage de vos contacts, aux journaux d'appels, aux messages SMS, à la localisation, à l'appareil photo, au microphone et à de nombreux autres éléments de votre appareil afin que ces applications systèmes de base et beaucoup d'autres applications puissent simplement fonctionner. Les environnements tels que les services Google Play augmentent la surface d'attaque de votre appareil et sont à l'origine de divers problèmes de confidentialité liés à Android.

Ce problème pourrait être résolu en utilisant une distribution Android qui n'est pas fournie avec une intégration de ces applications invasives. Malheureusement, de nombreuses distributions d'Android enfreignent souvent le modèle de sécurité d'Android en ne prenant pas en charge les fonctions de sécurité essentielles telles que l'AVB, le rollback protection, les mises à jour du firmware, etc. Certaines distributions fournissent également des builds [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) qui permettent le root via [ADB](https://developer.android.com/studio/command-line/adb) et nécessitent [des politiques SELinux plus permissives](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) pour prendre en compte les fonctionnalités de débogage, ce qui augmente encore plus la surface d'attaque et affaiblit grandement le modèle de sécurité.

Idéalement, lorsque vous choisissez une distribution Android, vous devez vous assurer qu'elle respecte le modèle de sécurité Android. Au minimum, la distribution doit disposer de builds de production, d'un support pour AVB, d'une rollback protection, de mises à jour dans les meilleurs délais du firmware et du système d'exploitation, et de SELinux en [mode enforcing](https://source.android.com/security/selinux/concepts#enforcement_levels). Toutes les distributions Android que nous recommandons répondent à ces critères.

[Nos recommandations de distributions Android :material-arrow-right-drop-circle:](../android.md ""){.md-button}

### Éviter le rootage

[Le rootage](https://en.wikipedia.org/wiki/Rooting_(Android)) des téléphones Android peut diminuer la sécurité de manière significative car il affaiblit complétement le modèle de sécurité d'[Android](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy). Cela peut nuire à la protection de la vie privée en cas d'exploitation facilitée par la diminution de la sécurité. Les méthodes courantes de rootage impliquent une modification directe de la partition de démarrage, ce qui rend impossible l'exécution du Démarrage Vérifié. Apps that require root will also modify the system partition, meaning that Verified Boot would have to remain disabled. Le fait que le root soit exposé directement dans l'interface utilisateur augmente également la [surface d'attaque](https://en.wikipedia.org/wiki/Attack_surface) de votre appareil et peut contribuer aux vulnérabilités [d'élévation de privilèges](https://en.wikipedia.org/wiki/Privilege_escalation) et aux contournements de la politique SELinux.

Les bloqueurs de contenu, qui modifient le [fichier hosts](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) et les pare-feu (AFWall+ ) qui requièrent un accès root de manière persistante sont dangereux et ne doivent pas être utilisés. Ils ne sont pas non plus la bonne façon de résoudre les problèmes auxquels ils sont destinés. For content blocking, we suggest encrypted [DNS](../dns.md) or content blocking functionality provided by a VPN instead. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy enhancing services such as [Orbot](../tor.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+ fonctionne sur le [filtrage des paquets](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) et peut être contourné dans certaines situations.

Nous ne pensons pas que les sacrifices de sécurité en rootant un smartphone valent les avantages discutables de ces applications en matière de vie privée.

### Installer les mises à jour

Il est important de ne pas utiliser une version d'Android [en fin de vie](https://endoflife.date/android). Newer versions of Android receive not only security updates for the operating system but also important privacy enhancing updates too.

Par exemple, [avant Android 10](https://developer.android.com/about/versions/10/privacy/changes) toute application disposant de l'autorisation [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) pouvait accéder aux numéros de série sensibles et uniques de votre téléphone, tels que l'[IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), le [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), ou l'[IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity) de votre carte SIM ; alors qu'aujourd'hui, il doit s'agir d'applications système pour le faire. Les applications système sont uniquement fournies par le fabricant ou la distribution Android.

### Partager des médias

Vous pouvez éviter de donner à de nombreuses applications l'autorisation d'accéder à vos médias grâce aux fonctions de partage intégrées d'Android. De nombreuses applications vous permettent de "partager" un fichier avec elles pour l'envoi de médias.

Par exemple, si vous souhaitez publier une photo sur Discord, vous pouvez ouvrir votre gestionnaire de fichiers ou votre galerie et partager cette photo avec l'application Discord, au lieu d'accorder à Discord un accès complet à vos médias et photos.

## Protections de sécurité

### Démarrage vérifié

Le [Démarrage vérifié](https://source.android.com/security/verifiedboot) est un élément important du modèle de sécurité d'Android. Il fournit une protection contre les attaques de type [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack), la persistance de logiciels malveillants et garantit que les mises à jour de sécurité ne peuvent pas être rétrogradées grâce au [rollback protection](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

Les versions supérieures à Android 10 ont abandonné le chiffrement complet du disque au profit d'un chiffrement plus souple [basé sur les fichiers](https://source.android.com/security/encryption/file-based). Vos données sont chiffrées à l'aide de clés de chiffrement propres à chaque utilisateur, tandis que les fichiers du système d'exploitation ne sont pas chiffrés.

Le Démarrage Vérifié garantit l'intégrité des fichiers du système d'exploitation, empêchant un adversaire disposant d'un accès physique d'altérer ou d'installer des logiciels malveillants sur l'appareil. Dans le cas improbable où un logiciel malveillant parviendrait à exploiter d'autres parties du système et à obtenir un accès privilégié, le Démarrage Vérifié empêchera et annulera toutes modifications apportées à la partition système lors du redémarrage de l'appareil.

Malheureusement, les fabricants sont tenus de prendre en charge le Démarrage Vérifié uniquement sur leurs distributions Android d'origine. Seuls quelques fabricants OEM, tels que Google, prennent en charge l'enrolement de clés AVB personnalisées sur leurs appareils. De plus, certaines ROM dérivées d'AOSP tels que LineageOS ou /e/ OS ne prennent pas en charge le Démarrage Vérifié, même si le matériel peut le prendre en charge. Nous vous recommandons de vérifier le support de cette fonctionnalité **avant** d'acheter un nouvel appareil. Les dérivés d'AOSP qui ne prennent pas en charge le Démarrage Vérifié ne sont **pas** recommandés.

De nombreux contructeurs ont également une implémentation défectueuse du Démarrage Vérifié dont vous devez être conscient au-delà de leur marketing. Par exemple, les Fairphone 3 et 4 ne sont pas sécurisés par défaut, car le [chargeur d'amorçage d'origine fait confiance à la clé de signature AVB publique](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### Mises à jour du micrologiciel

Les mises à jour du micrologiciel sont essentielles au maintien de la sécurité. Sans elles, votre appareil ne peut être sécurisé. Les fabriquants ont conclu des accords de prise de en charge avec leurs partenaires pour fournir les mises à jour des composants closed-source pendant une période limitée. Celles-ci sont détaillées dans les [Bulletins de Sécurité Android](https://source.android.com/security/bulletin) mensuels.

Comme les composants du téléphone, tels que le processeur et les technologies radio, reposent sur des composants closed-source, les mises à jour doivent être fournies par leur fabricants respectifs. Par conséquent, il est important que vous achetiez un appareil qui reçoit activement des mises à jours. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) et [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) prennent en charge leurs appareils pendant quatre ans, alors que les produits moins chers ont souvent des cycles de prises en charge plus courts. Avec l'introduction du [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google fabrique maintenant son propre SoC et fournira un minimum de 5 ans de mises à jour. Avec l'introduction de la série Pixel 8, Google a porté cette intervalle de prise en charge à 7 ans.

Les appareils qui ne sont plus pris en charge par le fabricant du SoC ne peuvent pas recevoir de mises à jour du micrologiciel de la part des fabricants ou des distributeurs. Cela signifie que les problèmes de sécurité de ces appareils ne seront pas corrigés.

Fairphone, par exemple, commercialise son appareil Fairphone 4 comme bénéficiant de 6 ans de mises à jour. Cependant, le SoC (Qualcomm Snapdragon 750G sur le Fairphone 4) a une date de fin de vie (EOL) beaucoup plus courte. Cela signifie que les mises à jour de sécurité du micrologiciel de Qualcomm pour le Fairphone 4 prendront fin en septembre 2023, que Fairphone continue ou non à publier des mises à jour de sécurité logicielle.

### Autorisations d'Android

Les [autorisations sur Android](https://developer.android.com/guide/topics/permissions/overview) vous permettent de contrôler ce que les applications ont le droit d'accéder. Google apporte régulièrement des [améliorations](https://developer.android.com/about/versions/11/privacy/permissions) sur le système d'autorisations à chaque nouvelle version d'Android. Toutes les applications que vous installez sont strictement [isolées](https://source.android.com/security/app-sandbox), il n'est donc pas nécessaire d'installer des applications antivirus.

Un smartphone équipé de la dernière version d'Android sera toujours plus sûr qu'un vieux smartphone équipé d'un antivirus que vous avez payé. Il est préférable de ne pas payer pour un logiciel antivirus et d'économiser pour acheter un nouveau smartphone, comme un Google Pixel.

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

Des applications respectueuses de la vie privée telles que [Bitwarden](https://reports.exodus-privacy.eu.org/fr/reports/com.x8bit.bitwarden/latest) peuvent afficher certains traqueurs tels que [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/fr/trackers/49). Cette bibliothèque comprend [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) qui peut fournir des [notifications push](https://fr.wikipedia.org/wiki/Server_push) dans les applications. C'est [le cas](https://fosstodon.org/@bitwarden/109636825700482007) avec Bitwarden. Cela ne signifie pas que Bitwarden utilise toutes les fonctionnalités d'analyse fournies par Google Firebase Analytics.

</div>

## Fonctionnalités de protection de la vie privée

### Profils utilisateurs

Les profils d'utilisateurs multiples se trouvent dans **Paramètres** → **Système** → **Utilisateurs multiples** et constituent le moyen le plus simple d'isoler dans Android.

Avec les profils d'utilisateur, vous pouvez imposer des restrictions à un profil spécifique, par exemple : passer des appels, utiliser des SMS ou installer des applications sur l'appareil. Chaque profil est chiffré à l'aide de sa propre clé de chiffrement et ne peut accéder aux données d'aucun autre profil. Même le propriétaire de l'appareil ne peut pas voir les données des autres profils sans connaître leur mot de passe. Les profils d'utilisateurs multiples est une méthode d'isolement plus sécurisée.

### Profil professionnel

Les [Profils Professionnels](https://support.google.com/work/android/answer/6191949?hl=fr) sont une autre façon d'isoler des applications de manière individuelles et peuvent s'avérer plus pratiques que des profils d'utilisateur séparés.

Une application de **gestionnaire d'appareil** telle que [Shelter](../android.md#shelter) est nécessaire pour créer un profil professionnel sans MDM d'entreprise, à moins que vous n'utilisiez un système d'exploitation Android personnalisé qui en comprend une.

Le profil professionnel dépend d'un gestionnaire d'appareil pour fonctionner. Les fonctionnalités telles que la *Navigation de Fichiers* et le *blocage de la recherche de contacts* ou tout autre type de fonctionnalités d'isolation doivent être implémentées par le gestionnaire. Vous devez également faire entièrement confiance à l'application de gestionnaire d'appareil, car elle a un accès total à vos données au sein du profil professionnel.

Cette méthode est généralement moins sûre qu'un profil utilisateur secondaire, mais elle vous permet d'exécuter simultanément des applications dans les profils professionnel et personnel.

### Arrêt d'urgence VPN

Android 7 et plus prennent en charge un arrêt d'urgence du VPN et il est disponible sans qu'il soit nécessaire d'installer des applications tierces. Cette fonction permet d'éviter les fuites si le VPN est déconnecté. Il se trouve dans :gear: **Paramètres** → **Réseau & internet** → **VPN** → :gear: → **Bloquer les connexions sans VPN**.

### Boutons à bascule globaux

Les appareils Android modernes disposent de boutons à bascule permettant de désactiver les services Bluetooth et de localisation. Android 12 a introduit des boutons à bascule pour l'appareil photo et le microphone. Lorsque vous n'utilisez pas ces fonctions, nous vous recommandons de les désactiver. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Services Google

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. Nous recommandons toujours d'éviter complètement les services Google ou de limiter les services Google Play à un profil utilisateur/professionnel spécifique en combinant un contrôleur d'appareil comme *Shelter* avec le Sandboxed Google Play de GrapheneOS.

### Programme de Protection Avancé

Si vous avez un compte Google, nous vous suggérons de vous inscrire au [Programme de Protection Avancée](https://landing.google.com/advancedprotection). Il est disponible gratuitement pour toute personne possédant au moins deux clés de sécurité physiques qui prennent en charge le protocole [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online). Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

Le Programme de Protection Avancée offre une surveillance accrue des menaces et permet :

- Une authentification à deux facteurs plus stricte; par exemple, seul [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **doit** être utilisé et toute autre type de double autentification tels que [SMS OTP](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) et [OAuth](https://en.wikipedia.org/wiki/OAuth) sont bloqués
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

Sur les distributions Android avec [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), allez dans :gear: **Paramètres** → **Applications** → **Sandboxed Google Play** → **Paramètres Google** → **Annonces**, et sélectionnez *Supprimer l'ID publicitaire*.

Sur les distributions Android avec des services Google Play privilégiés (comme les systèmes d'exploitation d'origines), le paramètre peut se trouver à plusieurs endroits. Vérifiez:

- :gear: **Paramètres** → **Google** → **Annonces**
- :gear: **Paramètres** → **Confidentialité** → **Annonces**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. Si ce n'est pas le cas, veillez à refuser la personnalisation des publicités puis à réinitialiser votre identifiant publicitaire.

### SafetyNet et Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) et les [API Play Integrity](https://developer.android.com/google/play/integrity) sont généralement utilisés pour des [applications bancaires](https://grapheneos.org/usage#banking-apps). De nombreuses applications bancaires fonctionneront sans problème sur GrapheneOS avec les services Google Play en sandbox, mais certaines applications non financières ont leurs propres mécanismes anti-tampering rudimentaires qui peuvent échouer. GrapheneOS passe le contrôle `basicIntegrity`, mais pas le contrôle de certification `ctsProfileMatch`. Les appareils équipés d'Android 8 ou d'une version ultérieure sont dotés d'un système d'attestation matérielle qui ne peut être contourné qu'en cas de fuite de clés ou de vulnérabilité grave.

Quant à Google Wallet, nous ne le recommandons pas en raison de sa [politique de confidentialité](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), qui stipule que vous devez manuellement refuser si vous ne voulez pas que votre note de crédit et vos informations personnelles soient partagées avec des services de marketing affiliés.
