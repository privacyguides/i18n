---
title: Paramètres de stratégie de groupe
description: Un guide rapide pour configurer la stratégie de groupe afin de rendre Windows un peu plus respectueux de la vie privée.
---

En dehors de la modification du registre lui-même, **l'éditeur de stratégie de groupe** est le moyen le plus efficace de modifier de nombreux aspects de votre système sans installer d'outils tiers. La modification de ces paramètres nécessite [Pro Edition] (index.md#windows-editions) ou une version plus récente.

Ces paramètres doivent être définis lors d'une nouvelle installation de Windows. Les paramétrer sur votre installation existante devrait fonctionner, mais peut introduire des comportements imprévisibles.

Tous ces paramètres sont accompagnés d'une explication dans l'éditeur de stratégie de groupe, qui explique exactement ce qu'ils font, généralement de manière très détaillée. Veuillez prêter attention à ces descriptions au fur et à mesure que vous apportez des modifications, afin que vous sachiez exactement ce que nous recommandons ici. Nous avons également expliqué certains de nos choix ci-dessous lorsque l'explication fournie avec Windows est inadéquate.

## Modèles Administratifs

Vous pouvez trouver ces paramètres en ouvrant `gpedit.msc` et en naviguant vers **Politique de l'ordinateur** > **Configuration de l'ordinateur** > **Modèles Administratifs** dans la barre latérale gauche. Les en-têtes de cette page correspondent aux dossiers/sous-dossiers dans les Modèles Administratifs, et les puce correspondent à des règles individuelles.

Pour modifier une stratégie de groupe, double-cliquez dessus et sélectionnez Activé ou Désactivé en haut de la fenêtre qui s'affiche en fonction des recommandations ci-dessous. Certaines stratégies de groupe comportent des paramètres supplémentaires qui peuvent être configurés. Dans ce cas, les paramètres appropriés sont également indiqués ci-dessous.

### Système

#### Device Guard

- Activer la sécurité basée sur la virtualisation : **Activé**
  - Niveau de sécurité de la plate-forme : **Secure Boot and DMA Protection** (démarrage sécurisé et protection DMA)
  - Configuration du lancement sécurisé : **Activé**

#### Gestion des communications Internet

- Désactiver le programme d'amélioration de l'expérience client de Windows : **Activé**
- Désactiver le rapport d'erreurs de Windows : **Activé**
- Désactiver le programme d'amélioration de l'expérience client de Windows : **Activé**

Notez que la désactivation du programme d'amélioration de l'expérience client Windows désactive également d'autres fonctions de suivi qui peuvent être contrôlées individuellement à l'aide de la stratégie de groupe. Ils ne sont pas listés ici car ils sont désactivés en même temps que le programme d'amélioration de l'expérience client.

#### Politiques du système d'exploitation

- Autoriser l'historique du presse-papiers : **Désactivé**
- Autoriser la synchronisation du presse-papiers entre les appareils : **Désactivé**
- Activer le flux d'activité : **Désactivé**
- Autoriser la publication des activités de l'utilisateur : **Désactivé**
- Autoriser le téléversement des activités de l'utilisateur : **Désactivé**

#### Profils utilisateurs

- Désactiver l'identifiant publicitaire : **Activé**

### Composants Windows

#### Configuration d'AutoPlay

AutoRun et AutoPlay sont des fonctions qui permettent à Windows d'exécuter un script ou une autre tâche lorsqu'un appareil est connecté, ce qui permet parfois d'éviter les mesures de sécurité qui impliquent le consentement de l'utilisateur. Cela peut permettre à des périphériques non fiables d'exécuter un code malveillant à votre insu. Il est préférable de désactiver ces fonctionnalités et d'ouvrir manuellement les fichiers sur vos disques externes.

- Désactiver AutoPlay : **Activé**
- Interdire la lecture automatique pour les appareils sans volume : **Activé**
- Définit le comportement par défaut pour AutoRun: **Activé**
  - Comportement de AutoRun par défaut : \*\*N'exécutez aucune commande AutoRun \*\*

#### Chiffrement du disque BitLocker

Il est préférable de chiffrer à nouveau le disque de votre système d'exploitation après avoir modifié ces paramètres.

- Choisissez la méthode de chiffrement du lecteur et la force du chiffrement (Windows Vista, Windows Server 2008, Windows 7) : **Activé**
  - Sélectionnez la méthode de chiffrement : **AES-256**

Le fait de définir la force de chiffrement pour la politique de Windows 7 permet de l'appliquer aux nouvelles versions de Windows.

##### Disques du système d'exploitation

- Exiger une authentification supplémentaire au démarrage : **Activé**
- Autoriser les codes PIN améliorés pour le démarrage : **Activé**

Malgré les noms de ces réglages, cela ne vous _oblige_ pas de faire quoi que ce soit par défaut, mais débloquera l'_option_ pour avoir une configuration plus complexe (comme la nécessité d'un code PIN au démarrage en plus de la TPM) dans l'assistant de configuration de BitLocker.

#### Contenu du Cloud

- Désactiver le contenu optimisé pour le cloud : **Activé**
- Désactiver le contenu de l'état du compte utilisateur cloud : **Activé**
- Ne pas afficher les conseils Windows : **Activé**
- Désactiver les expériences utilisateur de Microsoft : **Activé**

#### Interface utilisateur d'authentification

- Exiger un chemin de confiance pour l'entrée des identifiants : **Activé**
- Empêcher l'utilisation de questions de sécurité pour les comptes locaux : **Activé**

#### Collecte de données et aperçu des compilations

- Autoriser les données de diagnostic : **Activé**
  - Options : **Envoyer les données de diagnostic nécessaires** (édition Pro) ; ou
  - Options : **Données de diagnostic désactivées** (Edition Entreprise ou Education)
- Limiter la collecte des journaux de diagnostic : **Activé**
- Limiter Dump Collection : **Activé**
- Limiter les données de diagnostic optionnelles pour Desktop Analytics : **Activé**
  - Options : **Désactiver la collecte de données Desktop Analytics**
- Ne pas afficher les notifications : **Activé**

#### Explorateur de Fichiers

- Désactiver les aperçus basés sur le compte, les fichiers récents, favoris et recommandés dans l'explorateur de fichiers : **Activé**

#### MDM

- Désactiver l'inscription MDM : **Activé**

#### OneDrive

- Enregistrer les documents sur OneDrive par défaut : **Désactivé**
- Empêcher OneDrive de générer du trafic jusqu'à ce que l'utilisateur se connecte à OneDrive : **Activé**
- Empêcher l'utilisation de OneDrive pour le stockage de fichiers : **Activé**

Ce dernier paramètre désactive OneDrive sur votre système ; veillez à le modifier en **Désactivé** si vous utilisez OneDrive.

#### Push To Install

- Désactiver le service Push To Install : **Activé**

#### Recherche

- Autoriser Cortana : **Désactivé**
- Ne pas rechercher sur le Web ou afficher les résultats web dans Search : **Activé**
- Définissez les informations partagées dans Search : **Activé**
  - Type d'information : **Informations anonymes**

#### Synchroniser vos paramètres

- Ne pas synchroniser : **Activé**

#### Saisie de texte

- Améliorer la reconnaissance d'encre numérique et de saisie : **Désactivé**

#### Rapport d'erreurs Windows

- Ne pas envoyer de données supplémentaires : **Activé**
- Consentement > Configurer Consentement par défaut : **Activé**
  - Niveau de consentement : **Toujours demander avant d'envoyer des données**
