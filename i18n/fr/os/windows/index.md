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

This section is a work in progress, because it takes considerably more time and effort to make a Windows installation more privacy-friendly than other operating systems.

</div>

## Remarques concernant la vie privée

Microsoft Windows, particularly those versions aimed at consumers like the **Home** version often don't prioritize privacy-friendly features by [default](https://theguardian.com/technology/2015/jul/31/windows-10-microsoft-faces-criticism-over-privacy-default-settings). En conséquence, nous remarquons beaucoup plus de [collecte de données](https://en.wikipedia.org/wiki/Criticism_of_Microsoft#Telemetry_and_data_collection) que nécessaire, sans réel avertissement qu'il s'agit du comportement par défaut. Pour tenter de faire compétition à Google dans le domaine des publicités, [Cortana](https://fr.wikipedia.org/wiki/Cortana_\(assistant_personnel_intelligent\)) a inclus des identifiants uniques tels qu'un "identifiant publicitaire" afin de corréler l'utilisation et d'aider les publicitaires à cibler leurs publicités.  Au lancement, la télémétrie ne pouvait pas être désactivé dans les éditions non commerciales de Windows 10. Celle-ci ne peut toujours pas être désactivée, cependant, Microsoft a ajouté l'option de [réduire](https://extremetech.com/computing/243079-upcoming-windows-update-reduces-spying-microsoft-still-mum-data-collects) les données qui leur sont envoyées.

Windows 11 comporte un certain nombre de restrictions ou de valeurs par défaut, telles que :

- Il oblige l'utilisation d'un compte Microsoft au lieu d'un compte local.
- Il rend difficile l'accès à l'option de compte local pour les éditions \*_Pro_ et **Entreprise** de Windows.
- Il active par défaut de la collecte de données, obligeant les utilisateurs à la désactiver par eux même.
- Il intègre massivement les services Microsoft comme Bing, OneDrive et Teams, les présentant comme les seules options pour les utilisateurs, en plus de les rendre difficile à supprimer.
- Il règle Edge comme navigateur par défaut, en tout temps, et celui-ci le redevient après chaque mise à jour s'il a été changé.
- Il ajoute des fonctionnalités IA basées sur l'infonuagique dans plusieurs composantes Windows et applications Microsoft.
- Il conserve des informations sensibles inutiles par défaut. Même si ces données sont conservées localement, elles demeurent une cible pour les acteurs malveillants qui pourraient se retrouver sur votre appareil.

Microsoft utilise fréquemment sa fonction de mises à jour automatiques pour ajouter des nouvelles fonctionnalités à votre appareil et effectuer des changements dans la collecte de données qui sont activés par défaut. Some [privacy features](https://blogs.windows.com/windows-insider/2023/11/16/previewing-changes-in-windows-to-comply-with-the-digital-markets-act-in-the-european-economic-area) such as the option to _opt out_ of syncing an online Microsoft account with Windows, require you to select a country in the EEA (European Economic Area) during installation. It can be changed to your real country after Windows is installed.

## Windows Editions

Many critical privacy and security features are unfortunately locked away behind higher-cost editions of Windows, instead of being available in Windows **Home**. Some features missing from **Home** include BitLocker Drive Encryption, Hyper-V, and Windows Sandbox. In our Windows guides we will cover how to use all of these features appropriately, so having a premium edition of Windows will be necessary.

Windows **Enterprise** provides the most flexibility when it comes to configuring privacy and security settings built in to Windows. For example, they are the only editions that allow you to enable the highest level of restrictions on data sent to Microsoft via telemetry tools. Unfortunately, Enterprise is not available for retail purchase, so it may not be available to you.

The best version available for _retail_ purchase is Windows **Pro** as it has nearly all the features you'll want to use to secure your device, including BitLocker, Hyper-V, etc. The only thing missing is some of the most restrictive limitations on Microsoft's telemetry, unfortunately.

Students and teachers may be able to obtain a Windows **Education** (equivalent to Enterprise) or **Pro Education** license (equivalent to Pro) for free, including on personal devices, from their educational institution. Many schools partner with Microsoft via OnTheHub or Microsoft Azure for Education, so you can check those sites or your school's benefits page to see if you qualify. Whether or not you are able to get these licenses depends entirely on your institution. This may be the best way for many people to obtain an Enterprise-level edition of Windows for personal use. There are no additional privacy or security risks associated with using an Education license compared to the retail versions.

It is not recommended to use third party modified versions of Windows such as Windows AME. Since modified versions of Windows like Windows AME don't receive updates, security features and antivirus definitions in Windows Defender will fall behind the current threat landscape, opening you up to attacks, thus making you even less secure.

## Obtaining Windows

Currently, only Windows 11 license keys are available for purchase, but these keys will work on Windows 10 as well, so you can still purchase a Windows 11 Pro key to activate a Windows 10 install.

The official [Media Creation Tool](https://microsoft.com/software-download/windows11) is the best way to put a Windows installer on a USB flash drive. Third-party tools like Rufus or Etcher may unexpectedly modify the files, which could lead to boot issues or other troubles when installing.

This tool only lets you install a **Home** or **Pro** installation, as there are no publicly available downloads for Windows **Enterprise** edition. If you have an **Enterprise** license key, you can easily upgrade a **Pro** installation. To do this, install Windows **Pro** without entering a license key during setup, then enter your **Enterprise** key in the Settings app after completing the installation. Your **Pro** install will be upgraded to **Enterprise** automatically after entering a valid license key.

If you are installing an **Education** license then you will typically have a private download link that will be provided alongside your license key when you obtain it from your institution's benefits portal.
