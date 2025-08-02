---
title: "Android"
description: Notre conseil pour remplacer les fonctionnalités par défaut d'Android qui sont invasives de la vie privée.
icon: 'simple/android'
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Recommandations pour Android
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://fr.wikipedia.org/wiki/Android
---

![logo Android](../assets/img/android/android.svg){ align=right }

Le **Android Open Source Project** (AOSP) est un système d'exploitation mobile open-source dirigé par Google, utilisé par la majorité des appareils mobiles dans le monde. La plupart des téléphones vendu avec Android sont modifiés pour inclure des intégrations et applications invasives de la vie privée comme les Services Google Play, ainsi vous pouvez significativement améliorer votre confidentialité sur votre appareil mobile en remplaçant l'installation par défaut de votre téléphone avec une version d'android sans fonctionnalité intrusive.

[Vue d'ensemble d'Android :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## Nos conseils

### Remplacez les Services Google

Il y a de nombreuses méthodes pour obtenir des applications tout en évitant d'utiliser Google Play. Dès que c'est possible, essayez d'utiliser une de ces méthodes avant d'installer vos applications depuis une source non confidentielle :

[Obtenir des applications :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

Il existe également de nombreuses alternatives aux applications préinstallées, comme l'application de l'appareil photo. En plus des applications Android recommandées sur ce site, nous avons créée une liste d'applications système utilitaires spécifiques à Android qui pourraient vous être utiles.

[Recommandation d'applications génériques :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### Installer une distribution alternative

Lorsque vous achetez un téléphone Android, le système d'exploitation par défaut est livré avec des applications et des fonctionnalités qui ne font pas partie de l'Android Open-Source Project. Un grand nombre de ces applications - même des applications comme l'app Téléphone qui fournissent des fonctions système de base - nécessitent des intégrations invasives avec les services Google Play, qui demandent à leur tour des privilèges pour accéder à vos fichiers, au stockage de vos contacts, aux journaux d'appels, aux messages SMS, à la localisation, à l'appareil photo, au microphone et à de nombreux autres éléments de votre appareil afin que ces applications systèmes de base et beaucoup d'autres applications puissent simplement fonctionner. Les environnements tels que les services Google Play augmentent la surface d'attaque de votre appareil et sont à l'origine de divers problèmes de confidentialité liés à Android.

Ce problème peut être résolu en utilisant une distibution alternative d'Android, communément appellée _custom ROM_, qui n'inclue pas une intégration d'applications aussi invasive. Malheureusement, de nombreuses distributions d'Android enfreignent souvent le modèle de sécurité d'Android en ne prenant pas en charge les fonctions de sécurité essentielles telles que l'AVB, le rollback protection, les mises à jour du firmware, etc. Certaines distributions proposent également des versions [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) qui exposent l'utilisateur root via [ADB](https://developer.android.com/studio/command-line/adb) et nécessitent des politiques SELinux [plus permissives](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) pour prendre en compte les fonctions de débogage, ce qui augmente encore la surface d'attaque et affaiblit le modèle de sécurité.

Idéalement, lorsque vous choisissez une distribution Android, vous devez vous assurer qu'elle respecte le modèle de sécurité Android. Au minimum, la distibution doit disposer de builds de production, d'un support pour AVB, d'une protection rollback, de mises à jour rapides et régulières du firmware et du système d'exploitation et de SELinux en [mode renforcé](https://source.android.com/security/selinux/concepts#enforcement_levels). Toutes les distributions d'Android recommandées ici répondent à ces critères :

[Distributions recommandées :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### Eviter le Root

[Root](https://en.wikipedia.org/wiki/Rooting_\(Android\)) un téléphone Android peut sévèrement impacter la sécurité car cela affaibli le [modèle de sécurité Android](https://en.wikipedia.org/wiki/Android_\(operating_system\)#Security_and_privacy). Cela peut nuire à la protection de la vie privée en cas d'exploitation facilitée par la diminution de la sécurité. Les méthodes courantes de rootage impliquent une modification directe de la partition de démarrage, ce qui rend impossible l'exécution du Démarrage Vérifié. Les applications qui requièrent un Andoird rooté peuvent également modifier la partition du système, ce qui signifie que le Démarrage Vérifié devra rester désactivé. Le fait que le root soit exposé directement dans l'interface utilisateur augmente également la surface d'attaque de votre appareil et peut contribuer aux vulnérabilités [d'élévation de privilèges](https://en.wikipedia.org/wiki/Privilege_escalation) et aux contournements de la politique SELinux.

Les bloqueurs de contenu qui modifient le [fichier hosts](https://en.wikipedia.org/wiki/Hosts_\(file\)) (comme AdAway) et les pare-feu qui exigent un accès root permanent (comme AFWall+) sont dangereux et ne doivent pas être utilisés. Ils ne sont pas non plus la bonne façon de résoudre les problèmes qu'ils sont censés adresser. Pour bloquer du contenu, nous suggérons un [DNS](../dns.md) chiffré ou un VPN avec une fonctionnalité de blocage de contenu. TrackerControl et AdAway en mode non-root occuperont l'emplacement VPN (en utilisant un VPN looback local), empêchant ainsi l'utilisation de service de protection de la vie privée comme [Orbot](../alternative-networks.md#orbot) or ou [un vrai service VPN](../vpn.md).

AFWall+ fonctionne selon l'approche du [filtrage de paquets](https://en.wikipedia.org/wiki/Firewall_\(computing\)#Packet_filter) et peut être contourné dans certaines situations.

Nous ne pensons pas que les sacrifices de sécurité en rootant un smartphone valent les avantages discutables de ces applications en matière de vie privée.

### Installez les mises à jour régulièrement

Il est important de ne pas utiliser une version d'Android en [fin de vie](https://endoflife.date/android). Les versions plus récentes d'Android reçoivent non seulement des mises à jour de sécurité pour le système d'exploitation, mais aussi d'importantes améliorations de la confidentialité.

Par exemple, [avant Android 10](https://developer.android.com/about/versions/10/privacy/changes) n'importe quelle application avec l'autorisation [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) pouvait accéder aux numéros de séries sensible et unique de votre téléphone comme le [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), ou vos cartes SIM [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); alors qu'aujoud'hui il faut être une application système pour le faire. Les applications système sont uniquement fournies par le fabricant ou la distribution Android.

### Utilisez les fonctionnalités de partage intégrées

Vous pouvez éviter de donner à de nombreuses applications l'autorisation d'accéder à vos médias grâce aux fonctions de partage intégrées d'Android. De nombreuses applications vous permettent de "partager" un fichier avec elles pour l'envoi de médias.

Par exemple, si vous souhaitez publier une photo sur Discord, vous pouvez ouvrir votre gestionnaire de fichiers ou votre galerie et partager cette photo avec l'application Discord, au lieu d'accorder à Discord un accès complet à vos médias et photos.
