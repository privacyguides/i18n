---
title: Aperçu de Windows
icon: material/microsoft-windows
description: Microsoft Windows est un système d'exploitation populaire qui est, de base, configuré de façon très non confidentielle. Notre guide propose certaines modifications que vous pouvez faire, sans changer de système d'exploitation.
---

**Microsoft Windows** est un OS communément livré par défaut avec de nombreux PC. Ce guide vise à vous offrir certaines façons d'améliorer votre confidentialité et à réduire le montant de télémétrie et de données stockées par défaut en désactivant certaines fonctions inutiles. Au fil du temps, Microsoft a ajouté beaucoup de fonctionnalités à l'OS qui dépendent parfois de services cloud. Ces fonctionnalités nécessitent souvent certains types de [données optionnelles](https://privacy.microsoft.com/data-collection-windows) qui sont parfois envoyées à des serveurs distants pour être traitées.

L'exemple le plus récent s'appelle "Retrouver", qui fait partie de l'ensemble de fonctionnalités de Copilote IA. "Retrouver" réalise périodiquement des captures d'écrans de tout ce que vous avez vu sur votre PC pour ensuite vous le montrer à une date ultérieure. Ces fonctionnalités "utiles" créent des métadonnées considérables, qui peuvent ensuite être analysées de manière judicieuse. Dans la plupart des cas, l'historique de navigation est suffisant et cette fonctionnalité peut donc être désactivée en toute sécurité. L'inquiétude principale avec Retrouver est que les données stockées localement sont décryptées lors de l'ouverture de votre appareil, ce qui veut dire qu'il est une cible facile pour un acteur malveillant si votre appareil devenait infecté avec un logiciel malveillant. Retrouver ne supprimera pas les informations sensibles telles que les mots de passes ou les informations financières de la base de données, mais il protège contre la prise de captures d'écran de contenu ayant un droit d'auteur protégé par la gestion des droits numériques (GDN).

Malheureusement, cette fonctionnalité a été ajoutée sans considérer les impacts qu'elle pourrait avoir en étant activée par défaut ([elle est maintenant désactivée par défaut)](https://wired.com/story/microsoft-recall-off-default-security-concerns). Toutefois, ce n'est pas un cas isolé. Un autre exemple serait la fois où Microsoft a [activé les sauvegardes automatiques à OneDrive](https://neowin.net/news/windows-11-is-now-automatically-enabling-onedrive-folder-backup-without-asking-permission) sur les nouvelles installations Windows 11 sans demander de permission.

Vous pouvez améliorer votre confidentialité et votre sécurité sur Windows, sans télécharger de logiciel tiers, en utilisant ces guides :

- Installation initiale (à venir)
- [Paramètres de stratégie de groupe](group-policies.md)
- Paramètres de confidentialité (à venir)
- Isolation d'applications (à venir)
- Renforcement de la sécurité (à venir)

<div class="admonition example" markdown>
<p class="admonition-title">Cette section est nouvelle</p>

Cette section est en cours d'élaboration, car il faut beaucoup plus de temps et d'efforts pour rendre une installation Windows plus respectueuse de la vie privée que pour d'autres systèmes d'exploitation.

</div>

## Remarques concernant la vie privée

Microsoft Windows, en particulier les versions destinées aux consommateurs comme la version **Home**, ne donne souvent pas la priorité aux fonctions respectueuses de la vie privée par [défaut](https://theguardian.com/technology/2015/jul/31/windows-10-microsoft-faces-criticism-over-privacy-default-settings). En conséquence, nous remarquons beaucoup plus de [collecte de données](https://en.wikipedia.org/wiki/Criticism_of_Microsoft#Telemetry_and_data_collection) que nécessaire, sans réel avertissement qu'il s'agit du comportement par défaut. Pour tenter de faire compétition à Google dans le domaine des publicités, [Cortana](https://fr.wikipedia.org/wiki/Cortana_\(assistant_personnel_intelligent\)) a inclus des identifiants uniques tels qu'un "identifiant publicitaire" afin de corréler l'utilisation et d'aider les publicitaires à cibler leurs publicités.  Au lancement, la télémétrie ne pouvait pas être désactivé dans les éditions non commerciales de Windows 10. Celle-ci ne peut toujours pas être désactivée, cependant, Microsoft a ajouté l'option de [réduire](https://extremetech.com/computing/243079-upcoming-windows-update-reduces-spying-microsoft-still-mum-data-collects) les données qui leur sont envoyées.

Windows 11 comporte un certain nombre de restrictions ou de valeurs par défaut, telles que :

- Il oblige l'utilisation d'un compte Microsoft au lieu d'un compte local.
- Il rend difficile l'accès à l'option de compte local pour les éditions \*_Pro_ et **Entreprise** de Windows.
- Il active par défaut de la collecte de données, obligeant les utilisateurs à la désactiver par eux même.
- Il intègre massivement les services Microsoft comme Bing, OneDrive et Teams, les présentant comme les seules options pour les utilisateurs, en plus de les rendre difficile à supprimer.
- Il règle Edge comme navigateur par défaut, en tout temps, et celui-ci le redevient après chaque mise à jour s'il a été changé.
- Il ajoute des fonctionnalités IA basées sur l'infonuagique dans plusieurs composantes Windows et applications Microsoft.
- Il conserve des informations sensibles inutiles par défaut. Même si ces données sont conservées localement, elles demeurent une cible pour les acteurs malveillants qui pourraient se retrouver sur votre appareil.

Microsoft utilise fréquemment sa fonction de mises à jour automatiques pour ajouter des nouvelles fonctionnalités à votre appareil et effectuer des changements dans la collecte de données qui sont activés par défaut. Certaines [fonctions de protection de la vie privée](https://blogs.windows.com/windows-insider/2023/11/16/previewing-changes-in-windows-to-comply-with-the-digital-markets-act-in-the-european-economic-area), telles que la possibilité de _ne pas_ synchroniser un compte Microsoft en ligne avec Windows, exigent que vous sélectionniez un pays de l'EEE (Espace Economique Européen) lors de l'installation. Le pays peut être modifié après l'installation de Windows.

## Éditions Windows

De nombreuses fonctionnalités essentielles de confidentialité et de sécurité sont malheureusement bloquées derrière des éditions plus coûteuses de Windows, au lieu d'être disponibles dans Windows **Home**. Les fonctionnalités absentes de **Home** comprennent notamment le chiffrement de BitLocker Drive, Hyper-V et Windows Sandbox. Dans nos guides Windows, nous aborderons comment utiliser toutes ces fonctionnalités correctement, avoir une version premium de Windows sera donc nécessaire.

Windows **Entreprise** offre la plus grande flexibilité concernant la configuration des paramètres de confidentialité et de sécurité intégrés à Windows. C'est par exemple la seule édition vous permet d'activer le plus haut niveau de restrictions concernant les données envoyées à Microsoft via des outils de télémétrie. Malheureusement, Enterprise n'est pas disponible à la vente pour les particuliers, il se peut donc que vous ne puissiez pas en bénéficier.

La meilleure version disponible à l'achat _pour les particuliers_ est Windows **Pro**, car elle possède presque toutes les fonctionnalités nécessaires pour sécuriser votre appareil, y compris BitLocker, Hyper-V, etc. La seule fonctionnalité manquante est malheureusement celle permettant les limitations les plus restrictives de la télémétrie de Microsoft.

Les étudiants et les enseignants peuvent parfois obtenir auprès de leur établissement d'enseignement une licence Windows **Education** (équivalent à Enterprise) ou **Pro Education** (équivalent à Pro) gratuitement, y compris sur des appareils personnels. De nombreuses écoles travaillent en partenariat avec Microsoft via OnTheHub ou Microsoft Azure for Education. Vous pouvez donc consulter ces sites ou le site web de votre école pour savoir si vous êtes éligible. L'obtention de ces licences dépend entièrement de votre établissement. C'est probablement le meilleur moyen d'obtenir une édition de Windows au niveau de Windows Entreprise pour un usage personnel. L'utilisation d'une licence Éducation ne présente aucun risque supplémentaire en termes de confidentialité ou de sécurité par rapport aux versions commerciales.

Il n'est pas recommandé d'utiliser des versions modifiées de Windows, telles que Windows AME. Étant donné que les versions modifiées de Windows, comme Windows AME, ne reçoivent pas de mises à jour, les fonctions de sécurité et les définitions antivirus de Windows Defender ne sont donc pas adaptées aux menaces actuelles, ce qui vous expose à des attaques et rend votre appareil encore plus vulnérable.

## Obtenir Windows

Actuellement, seules les clés de licence Windows 11 sont disponibles à l'achat, mais ces clés fonctionneront également sur Windows 10. Vous pouvez donc toujours acheter une clé Windows 11 Pro pour activer une installation Windows 10.

L'outil officiel [Media Creation Tool] (https://microsoft.com/software-download/windows11) est le meilleur moyen d'installer un programme d'installation de Windows sur une clé USB. Des outils tiers tels que Rufus ou Etcher peuvent modifier les fichiers de manière inattendue, ce qui peut entraîner des problèmes de démarrage ou d'autres problèmes lors de l'installation.

Cet outil vous permet seulement d'installer une installation **Home** ou **Pro** car il n'y a pas de téléchargements publics disponibles pour l'édition Windows **Entreprise**. Si vous disposez d'une clé de licence **Enterprise**, vous pouvez facilement mettre à niveau une installation **Pro**. Pour cela, installez Windows **Pro** sans entrer de clé de licence pendant l'installation, saisissez alors votre clé **Entreprise** dans l'application Paramètres après avoir terminé l'installation. Votre installation **Pro** sera automatiquement mise à niveau vers **Enterprise** après avoir saisi une clé de licence valide.

Si vous installez une licence **Education**, vous disposerez généralement d'un lien de téléchargement privé qui vous sera fourni avec votre clé de licence lorsque vous l'obtiendrez via votre institution.
