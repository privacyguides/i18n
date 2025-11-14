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

La biométrie peut empêcher quelqu’un d’observer la saisie de votre mot de passe. Si l’observation directe fait partie de votre modèle de menace, la biométrie est une bonne option.

La plupart des implémentations de l'authentification par reconnaissance faciale exigent que vous regardiez votre téléphone et ne fonctionnent qu'à une distance relativement proche, de sorte que vous n'avez pas à vous inquiéter outre mesure que quelqu'un pointe votre téléphone vers votre visage pour le déverrouiller sans votre consentement. Vous pouvez toujours désactiver les données biométriques lorsque votre téléphone est verrouillé si vous le souhaitez. Sur iOS, vous pouvez maintenir le bouton latéral et un bouton de volume enfoncés pendant 3 secondes pour désactiver Face ID sur les modèles qui le prennent en charge. Sur Android, maintenez le bouton d’alimentation enfoncé et appuyez sur **Verrouillage** dans le menu.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Certains appareils ne disposent pas du hardware adapté pour une utilisation sécurisé de la reconnaissance faciale. Il existe deux principales méthodes de reconnaissance faciale : 2D et 3D. L'authentification faciale en D utilise un projecteur de points qui permet à l'appareil de créée une carte de profondeur en 3D de votre visage. Vérifiez que votre appareil en soit doté.

</div>

Android défini trois [classes de sécurité](https://source.android.com/docs/security/features/biometric/measure#biometric-classes) pour la biométrie ; vérifiez que votre appareil est de classe 3 avant d'activer la biométrie.

### Chiffrement de l'appareil

Si votre appareil est [chiffré] (../encryption.md), vos données sont mieux protégées lorsque votre appareil est complètement éteint (et non simplement endormi), c'est-à-dire avant que vous n'ayez saisi votre clé de chiffrement ou le mot de passe de l'écran de verrouillage pour la première fois. Sur les téléphones, cet état de sécurité accrue est appelé "Before First Unlock" (BFU), et "After First Unlock" (AFU) une fois que vous avez saisi le bon mot de passe après un redémarrage ou une mise sous tension. Par rapport au BFU, l'AFU est nettement moins sécurisé contre les outils de criminalistique numérique ou autres attaques. Par conséquent, si vous craignez qu'un pirate ait un accès physique à votre appareil, vous devriez l'éteindre complètement lorsque vous ne l'utilisez pas.

Cela peut s'avérer peu pratique, il convient donc de se demander si cela en vaut la peine, mais dans tous les cas, même le mode AFU est efficace contre la plupart des menaces, à condition que vous utilisiez une clé de chiffrement forte.

## Périphériques externes

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

### Dispositif de veille automatique (Dead Man's Switches)

Un dispositif de veille automatique empêche une machine de fonctionner sans la présence d'un opérateur humain. Ces dispositifs ont été conçus à l'origine comme une mesure de sécurité, mais le même concept peut être appliqué à un appareil électronique pour le verrouiller lorsque vous n'êtes pas présent.

Certains ordinateurs portables sont capables de [détecter votre présence] (https://support.microsoft.com/en-us/windows/managing-presence-sensing-settings-in-windows-11-82285c93-440c-4e15-9081-c9e38c1290bb) et de se verrouiller automatiquement lorsque vous n'êtes pas assis devant l'écran. Vous pouvez vérifier les paramètres de votre système d'exploitation pour voir si votre ordinateur prend en charge cette fonctionnalité.

Vous pouvez également vous procurer des câbles, comme [BusKill](https://buskill.in), qui verrouillent ou effacent votre ordinateur lorsque le câble est déconnecté.

### Anti-interdiction/Evil Maid Attack

Le meilleur moyen d'éviter une attaque ciblée contre vous avant que l'appareil ne soit en votre possession est de l'acheter dans un magasin physique, plutôt que de le commander à votre adresse.

Assurez-vous que votre appareil prend en charge le démarrage sécurisé/le démarrage vérifié et qu'il est activé. Dans la mesure du possible, évitez de laisser votre appareil sans surveillance.

### Verrous Kensington

De nombreux ordinateurs sont équipés d'une [encoche de sécurité Kensington](https://www.kensington.com/solutions/product-category/security/?srsltid=AfmBOorQOlRnqRJOAqM-Mvl7wumed0wBdiOgktlvdidpMHNIvGfwj9VI) qui peut être utilisée pour sécuriser votre appareil en insérant un **câble en métal** dans l'encoche de votre appareil. Ces verrous peuvent être à combinaison ou à clef.

Comme pour tous les verrous, les verrous Kensington sont vulnérables aux [attaques physiques](https://youtu.be/vgvCxL7dMJk), vous devriez donc l'utiliser uniquement pour prévenir les petits vols. Vous pouvez sécuriser votre ordinateur portable chez vous, ou même en public, en utilisant un pied de table ou autre objet qui ne peux pas être déplacé facilement.

## Sécurisez votre réseau

### Compartimentation

Il existe de nombreuses solutions qui vous permettent de séparer ce que vous faites sur un ordinateur, comme les machines virtuelles et le sandboxing. Cependant, le meilleur moyen de compartimentation est la séparation physique. Elle est particulièrement utile dans les cas où certains logiciels vous demandent de contourner les fonctionnalités de sécurité de votre système d'exploitation, comme avec des logiciels anti-triche intégrés à de nombreux jeux.

Pour les jeux, il peut être utile de désigner une machine comme machine de "jeu" et de ne l'utiliser uniquement pour cette tâche. Gardez-le sur un VLAN séparé. Cela peut nécessiter l’utilisation d’un switch administrable et d’un routeur prenant en charge des réseaux séparés.

La plupart des routeurs grand public vous permettent de le faire en activant un réseau "invité" distinct qui ne peut pas communiquer avec votre réseau principal. Vous pouvez y connecter tous vos appareils non fiables, y compris les appareils IoT comme votre réfrigérateur intelligent, votre thermostat, votre téléviseur, etc.

### Minimalisme

Comme le dit l'adage, "less is more" ("moins c'est plus"). Moins vous avez d'appareils connectés à votre réseau, moins vous avez de surface d'attaque potentielle et moins il vous faudra veiller à ce qu'ils soient tous mis à jour.

Il peut être utile de faire le tour de votre maison et de dresser une liste de tous vos appareils connectés pour vous aider à les surveiller.

### Routeurs

Votre routeur gère l'ensemble de votre trafic réseau et constitue la première ligne de défense entre vous et internet.

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

De nombreux routeurs sont équipés d'un espace de stockage pour vos fichiers afin que vous puissiez y accéder à partir de n'importe quel appareil connecté à votre réseau. Nous vous recommandons de ne pas utiliser les dispositifs de mise en réseau à d'autres fins que la mise en réseau. Dans le cas où votre routeur était compromis, vos fichiers le seraient également.

</div>

Il est absolument essentiel de maintenir votre routeur à jour. La plupart des routeurs modernes installent automatiquement les mises à jour, mais tous ne le font pas. Vous devez vérifier cette option sur la page des paramètres de votre routeur. Cette page est généralement accessible en tapant `192.168.1.1` ou `192.168.0.1` dans la barre URL de n'importe quel navigateur, à condition que vous soyez sur le même réseau. Vous pouvez également vérifier dans les paramètres réseau de votre système d'exploitation la présence d'un "routeur" ou "passerelle".

Si votre routeur ne prend pas en charge les mises à jour automatiques, vous devrez vous rendre sur le site du fabricant pour télécharger les mises à jour et les appliquer manuellement.

Beaucoup routeurs grand public ne sont pas pris en charge très longtemps. Si votre routeur n'est plus pris en charge par le fabricant, vous pouvez vérifier s'il est pris en charge par [un firmware FOSS] (../router.md). Vous pouvez également acheter des routeurs dont le micrologiciel FOSS est installé par défaut ; ces routeurs sont généralement pris en charge plus longtemps que la plupart des routeurs.

Certains FAI fournissent un routeur/modem combiné. Pour des raisons de sécurité, il peut être préférable d'acheter un routeur séparé et de mettre le routeur/modem de votre fournisseur d'accès en mode modem uniquement. De cette façon, même lorsque votre routeur fourni par votre FAI ne reçoit plus de mises à jour, vous pouvez toujours obtenir des mises à jour de sécurité et des patch. Cela signifie également que tout problème affectant votre modem n'affectera pas votre routeur et vice versa.
