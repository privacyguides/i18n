---
title: "Choisissez Votre Matériel (Hardware)"
icon: 'material/chip'
description: Il n'y a pas que les logiciels qui sont importants pour votre vie privée, le matériel que vous utiliser quotidiennement l'est aussi.
---

Quand on parle de la protection de la vie privée, on ne réfléchit souvent pas autant au choix du matériel qu'au choix du logiciel. Vous pouvez considérer le matériel comme le pilier sur lequel vous allez construire le reste de votre setup protégeant votre vie privée.

## Choisissez un ordinateur

Les composants de vos appareils traitent et stockent toutes vos données digitales. Il est important que tous les appareils soient encore supportés par le fabricant et les développeurs afin de recevoir les mises à jour de sécurité.

### Programmes de sécurité du matériel

Certains appareils disposent d'un "programme de sécurité du matériel", issu d'une collaboration entre les fournisseurs sur les bonnes pratiques et les recommandations lors de la conception du matériel, par exemple :

- [les PCs Windows Secured-core](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure-11) répondent à des critères de sécurité plus élevés spécifiés par Microsoft. Ces protections ne s'appliquent pas qu'aux utilisateurs de Windows ; les utilisateurs d'autres systèmes d'exploitation peuvent toujours bénéficier de fonctionnalités comme la [protection DMA](https://learn.microsoft.com/en-us/windows/security/information-protection/kernel-dma-protection-for-thunderbolt) and la possiblité de toujours se méfier des certificats Microsoft.
- [Android Ready SE](https://developers.google.com/android/security/android-ready-se) est le résultat de la collaboration entre fournisseurs pour s'assurer que leurs appareils respectents les [bonnes pratiques](https://source.android.com/docs/security/best-practices/hardware) et incluent un stockage matériel résistants aux manipulations pour des éléments tels que les clés de chiffrement.
- Lorsque macOS fonctionne sur un SoC Apple, il tire parti de la [sécurité matérielle](../os/macos-overview.md#hardware-security), qui peut ne pas être disponible pour d'autre systèmes d'exploitation.
- La [sécurité de ChromeOS](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper) est la plus optimale lorsqu'il est exécuté sur un Chromebook, car il peut utiliser certaines fonctionnalités matérielles comme le [hardware root-of-trust](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper/#hardware-root-of-trust-and-verified-boot).

Même si vous n'utilisez pas ces systèmes d'exploitation, la participation à ces programmes peut indiquer que le fabricant met en place des bonnes pratiques en termes de matériel et de mises à jour.

### Système d'exploitation préinstallé

Les ordinateurs neufs sont presque toujours livrés avec Windows, à moins d'acheter un Mac ou une machine Linux spécialisée. Il est généralement conseillé d'effacer entièrement le disque et d'installer une nouvelle copie du système d'exploitation de votre choix, même si cela signifie réinstaller Windows à partir de zéro. En raison d'accords entre les fournisseurs hardware et des éditeurs de logiciels douteux, l'installation par défaut de Windows est souvent préchargée de bloatware, [adware](https://bleepingcomputer.com/news/technology/lenovo-gets-a-slap-on-the-wrist-for-superfish-adware-scandal), voire de [malware](https://zdnet.com/article/dell-poweredge-motherboards-ship-with-malware).

### Mises à jour du micrologiciel (firmware)

Le hardware présente souvent des problèmes de sécurité qui sont découverts et corrigés par des mises à jour du firmware de votre matériel.

Presque tous les composants de votre ordinateur ont besoin d'un firmware pour fonctionner, de la carte mère aux périphériques de stockage. L'idéal est que tous les composants de votre appareil soient entièrement pris en charge. Les appareils Apple, les Chromebooks, la plupart des téléphones Android et les appareils Microsoft Surface gèrent les mises à jour du firmware pour vous tant que l'appareil est pris en charge.

Si vous construisez votre propre PC, il se peut que vous deviez mettre à jour manuellement le firmware de votre carte mère en le téléchargeant directement à partir du site du fabricant d'origine. Si vous utilisez Linux, envisagez l'utilisation de l'outil intégré [`fwupd`](https://fwupd.org) qui vous permettra de vérifier et d'appliquer les mise à jour du firmware de votre carte mère.

### TPM/Cryptoprocesseur sécurisé

La plupart des ordinateurs et des téléphones sont équipés d'un TPM (ou d'un cryptoprocesseur sécurisé similaire) qui stocke en toute sécurité vos clés de chiffrement et gère d'autres fonctions liées à la sécurité. Si vous utilisez actuellement un appareil qui n'en est pas équipé, il peut être intéressant d'aquérir un nouvel ordinateur disposant de cette fonctionnalité. Certaines cartes mères d'ordinateurs de bureau et de serveurs sont dotées d'un "en-tête TPM" qui peut accueillir une petite carte accessoire contenant le TPM.

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

Les TPM virtuels sont vulnérables aux attaques par canal auxiliaire et les TPM externe, du fait qu'ils soient séparés de la CPU sur la carte mère, sont vulnérable au [sniffing](https://pulsesecurity.co.nz/articles/TPM-sniffing) lorsqu'un attaquant a accès au hardware. La solution à ce problème consiste à inclure le processeur sécurisé dans la CPU elle-même, comme c'est le cas pour les puces d'Apple et le [Pluton](https://microsoft.com/en-us/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs) de Microsoft.

</div>

### Biométrie

Beaucoup d'appareil sont équipés de lecteur d'empreinte digitale ou de fonctions de reconnaissance faciale. Ces fonctions peuvent être très pratiques mais ne sont pas parfait et sont parfois susceptibles de ne pas fonctionner. Laplupart des appareils proposent un PIN ou un mot de passe lorsque cela se produit, ce qui signifie que la sécurité de l'appareil est toujours finalement conditionnée par le mot de passe.

L'utilisation de fonction de biométrie peut empêcher quelqu'un de vous regarder taper votre mot de passe, si le "shoulder-surfing" (regarderr par dessus l'épaule) fait partie de votre modèle de menace, la biométrie peut être une bonne option.

La plupart des implémentations de l'authentification par reconnaissance faciale exigent que vous regardiez votre téléphone et ne fonctionnent qu'à une distance relativement proche, de sorte que vous n'avez pas à vous inquiéter outre mesure que quelqu'un pointe votre téléphone vers votre visage pour le déverrouiller sans votre consentement. Vous pouvez toujours désactiver les données biométriques lorsque votre téléphone est verrouillé si vous le souhaitez. Sur iOS, vous pouvez maintenir le bouton latéral et un boutton de volume pendant 3 secondes pour désactiver Face ID sur les modèles qui le permettent. Surr Android, maintenez le bouton d'alimentation et appuyez sur Verrouillage (Lockdown) dans le menu.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Certains appareils ne disposent pas du hardware adapté pour une utilisation sécurisé de la reconnaissance faciale. Il existe deux principales méthodes de reconnaissance faciale : 2D et 3D. L'authentification faciale en D utilise un projecteur de points qui permet à l'appareil de créée une carte de profondeur en 3D de votre visage. Vérifiez que votre appareil en soit doté.

</div>

Android défini trois [classes de sécurité](https://source.android.com/docs/security/features/biometric/measure#biometric-classes) pour la biométrie ; vérifiez que votre appareil est de classe 3 avant d'activer la biométrie.

### Chiffrement de l'appareil

Si votre appareil est [chiffré] (../encryption.md), vos données sont mieux protégées lorsque votre appareil est complètement éteint (et non simplement endormi), c'est-à-dire avant que vous n'ayez saisi votre clé de chiffrement ou le mot de passe de l'écran de verrouillage pour la première fois. Sur les téléphones, cet état de sécurité accrue est appelé "Before First Unlock" (BFU), et "After First Unlock" (AFU) une fois que vous avez saisi le bon mot de passe après un redémarrage ou une mise sous tension. Par rapport au BFU, l'AFU est nettement moins sécurisé contre les outils de criminalistique numérique ou autres attaques. Par conséquent, si vous craignez qu'un pirate ait un accès physique à votre appareil, vous devriez l'éteindre complètement lorsque vous ne l'utilisez pas.

Cela peut s'avérer peu pratique, il convient donc de se demander si cela en vaut la peine, mais dans tous les cas, même le mode AFU est efficace contre la plupart des menaces, à condition que vous utilisiez une clé de chiffrement forte.

## External Hardware

Les composants internes ne suffisent pas à eux seuls à se protéger contre certaines menaces. Bon nombre de ces options sont hautement situationnelles ; veuillez évaluer si elles sont vraiment nécessaires pour votre modèle de menace.

### Clés de sécurité matérielles

Les clés matérielles sont des dispositifs qui utilisent une cryptographie forte pour vous authentifier auprès d'un appareil ou d'un compte. L'idée est que, comme elles ne peuvent pas être copiées, vous pouvez les utiliser pour sécuriser des comptes de manière à ce qu'ils ne soient accessibles qu'en cas de possession physique de la clé, ce qui élimine de nombreuses attaques à distance.

[Clés matérielles recommandées :material-arrow-right-drop-circle:](../security-keys.md){ .md-button .md-button--primary } [En savoir plus sur les clés matérielles :material-arrow-right-drop-circle:](multi-factor-authentication.md#hardware-security-keys){ .md-button }

### Caméra/Microphone

Si vous ne voulez pas faire confiance aux contrôles d'autorisation de votre système d'exploitation pour empêcher l'activation de la caméra, vous pouvez acheter des bloqueurs de caméra qui empêchent physiquement la lumière d'atteindre la caméra. Vous pouvez également acheter un appareil qui n'a pas de caméra intégrée et utiliser une caméra externe que vous pouvez débrancher lorsque vous avez fini de l'utiliser. Certains appareils sont équipés de bloqueurs de caméra intégrés ou de commutateurs matériels qui déconnectent physiquement l'alimentation de la caméra.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

N'achetez que des caches de caméra adaptés à votre ordinateur portable et qui ne risquent pas d'être endommagées lorsque vous fermez le couvercle. Cacher la caméra interfère avec le réglage automatique de la luminosité et les fonctions de reconnaissance faciale.

</div>

Pour l'accès au microphone, vous devrez dans la plupart des cas vous fier aux contrôles d'autorisation intégrés à votre système d'exploitation. Vous pouvez également acheter un appareil qui n'a pas de microphone intégré et utiliser un micro externe que vous pouvez débrancher lorsque vous avez fini de l'utiliser. Certains appareils, comme [un MacBook ou un iPad](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web), sont dotés d'une déconnexion matérielle du microphone lorsque vous fermez le couvercle.

De nombreux ordinateurs disposent d'une option BIOS permettant de désactiver la caméra et le microphone. Lorsqu'il est désactivé, le matériel n'apparaît même pas en tant que périphérique sur un système démarré.

### Écrans de confidentialité

Les écrans de confidentialité sont des films que vous pouvez poser sur votre écran de manière à ce que celui ci ne soit visible que sous un certain angle. Ils peuvent être utiles si votre modèle de menace inclut que d'autres personnes regardent votre écran sans votre consentement, mais ils ne sont pas infaillibles car n'importe qui peut simplement changer d'angle de vue et voir ce qui s'affiche sur votre écran.

### Dead Man's Switches

Un dispositif de veille automatique empêche une machine de fonctionner sans la présence d'un opérateur humain. Ces dispositifs ont été conçus à l'origine comme une mesure de sécurité, mais le même concept peut être appliqué à un appareil électronique pour le verrouiller lorsque vous n'êtes pas présent.

Certains ordinateurs portables sont capables de [détecter votre présence] (https://support.microsoft.com/en-us/windows/managing-presence-sensing-settings-in-windows-11-82285c93-440c-4e15-9081-c9e38c1290bb) et de se verrouiller automatiquement lorsque vous n'êtes pas assis devant l'écran. Vous pouvez vérifier les paramètres de votre système d'exploitation pour voir si votre ordinateur prend en charge cette fonctionnalité.

Vous pouvez également vous procurer des câbles, comme [BusKill](https://buskill.in), qui verrouillent ou effacent votre ordinateur lorsque le câble est déconnecté.

### Anti-Interdiction/Evil Maid Attack

Le meilleur moyen d'éviter une attaque ciblée contre vous avant que l'appareil ne soit en votre possession est de l'acheter dans un magasin physique, plutôt que de le commander à votre adresse.

Assurez-vous que votre appareil prend en charge le démarrage sécurisé/le démarrage vérifié et qu'il est activé. Dans la mesure du possible, évitez de laisser votre appareil sans surveillance.

## Sécurisez votre réseau

### Compartmentalization

Many solutions exist that allow you to separate what you're doing on a computer, such as virtual machines and sandboxing. However, the best compartmentalization is physical separation. This is useful especially for situations where certain software requires you to bypass security features in your OS, such as with anti-cheat software bundled with many games.

For gaming, it may be useful to designate one machine as your "gaming" machine and only use it for that one task. Keep it on a separate VLAN. This may require the use of a managed switch and a router that supports segregated networks.

Most consumer routers allow you to do this by enabling a separate "guest" network that can't talk to your main network. All untrusted devices can go here, including IoT devices like your smart fridge, thermostat, TV, etc.

### Minimalism

As the saying goes, "less is more". The fewer devices you have connected to your network, the less potential attack surface you'll have and the less work it will be to make sure they all stay up-to-date.

You may find it useful to go around your home and make a list of every connected device you have to help you keep track.

### Routers

Your router handles all your network traffic and acts as your first line of defense between you and the open internet.

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

A lot of routers come with storage to put your files on so you can access them from any computer on your network. We recommend you don't use networking devices for things other than networking. In the event your router was compromised, your files would also be compromised.

</div>

The most important thing to think about with routers is keeping them up-to-date. Many modern routers will automatically install updates, but many others won't. You should check on your router's settings page for this option. That page can usually be accessed by typing `192.168.1.1` or `192.168.0.1` into the URL bar of any browser assuming you're on the same network. You can also check in the network settings of your OS for "router" or "gateway".

If your router does not support automatic updates, you will need to go to the manufacturer's site to download the updates and apply them manually.

Many consumer-grade routers aren't supported for very long. If your router isn't supported by the manufacturer anymore, you can check if it's supported by [FOSS firmware](../router.md). You can also buy routers that come with FOSS firmware installed by default; these tend to be supported longer than most routers.

Some ISPs provide a combined router/modem. It can be beneficial for security to purchase a separate router and set your ISP router/modem into modem-only mode. This way, even when your ISP-provided router is no longer getting updates, you can still get security updates and patches. It also means any problems that affect your modem won't affect your router and vice versa.
