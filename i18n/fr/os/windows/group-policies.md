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
 - Turn off the Windows Messenger Customer Experience Improvement Program: **Enabled**

Note that disabling the Windows Customer Experience Improvement Program also disables some other tracking features that can be individually controlled with Group Policy as well. We don't list them all here or disable them because this setting covers that.

#### OS Policies

 - Allow Clipboard History: **Disabled**
 - Allow Clipboard synchronization across devices: **Disabled**
 - Enables Activity Feed: **Disabled**
 - Allow publishing of User Activities: **Disabled**
 - Allow upload of User Activities: **Disabled**

#### Profils utilisateurs

 - Turn off the advertising ID: **Enabled**

### Windows Components

#### AutoPlay Policies

AutoRun and AutoPlay are features which allow Windows to run a script or perform some other task when a device is connected, sometimes avoiding security measures that involve user consent. This could allow untrusted devices to run malicious code without your knowledge. It's a security best practice to disable these features, and simply open files on your external disks manually.

 - Turn off AutoPlay: **Enabled**
 - Disallow Autoplay for nonvolume devices: **Enabled**
 - Set the default behavior for AutoRun: **Enabled**
     - Default AutoRun Behavior: **Do not execute any AutoRun commands**

#### BitLocker Drive Encryption

You may wish to re-encrypt your operating system drive after changing these settings.

 - Choose drive encryption method and cipher strength (Windows Vista, Windows Server 2008, Windows 7): **Enabled**
     - Select the encryption method: **AES-256**

Setting the cipher strength for the Windows 7 policy still applies that strength to newer versions of Windows.

##### Operating System Drives

 - Require additional authentication at startup: **Enabled**
 - Allow enhanced PINs for startup: **Enabled**

Despite the names of these policies, this doesn't _require_ you to do anything by default, but it will unlock the _option_ to have a more complex setup (such as requiring a PIN at startup in addition to the TPM) in the BitLocker setup wizard.

#### Cloud Content

 - Turn off cloud optimized content: **Enabled**
 - Turn off cloud consumer account state content: **Enabled**
 - Do not show Windows tips: **Enabled**
 - Turn off Microsoft consumer experiences: **Enabled**

#### Credential User Interface

 - Require trusted path for credential entry: **Enabled**
 - Prevent the use of security questions for local accounts: **Enabled**

#### Data Collection and Preview Builds

 - Allow Diagnostic Data: **Enabled**
     - Options: **Send required diagnostic data** (Pro Edition); or
     - Options: **Diagnostic data off** (Enterprise or Education Edition)
 - Limit Diagnostic Log Collection: **Enabled**
 - Limit Dump Collection: **Enabled**
 - Limit optional diagnostic data for Desktop Analytics: **Enabled**
     - Options: **Disable Desktop Analytics collection**
 - Do not show feedback notifications: **Enabled**

#### File Explorer

 - Turn off account-based insights, recent, favorite, and recommended files in File Explorer: **Enabled**

#### MDM

 - Disable MDM Enrollment: **Enabled**

#### OneDrive

 - Save documents to OneDrive by default: **Disabled**
 - Prevent OneDrive from generating network traffic until the user signs in to OneDrive: **Enabled**
 - Prevent the usage of OneDrive for file storage: **Enabled**

This last setting disables OneDrive on your system; make sure to change it to **Disabled** if you use OneDrive.

#### Push To Install

 - Turn off Push To Install service: **Enabled**

#### Recherche

 - Allow Cortana: **Disabled**
 - Don't search the web or display web results in Search: **Enabled**
 - Set what information is shared in Search: **Enabled**
     - Type of information: **Anonymous info**

#### Sync your settings

 - Do not sync: **Enabled**

#### Text input

 - Improve inking and typing recognition: **Disabled**

#### Windows Error Reporting

 - Do not send additional data: **Enabled**
 - Consent > Configure Default consent: **Enabled**
     - Consent level: **Always ask before sending data**
