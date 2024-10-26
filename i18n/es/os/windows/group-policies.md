---
title: Configuración de las Directivas de Grupo
description: Una guía rápida para configurar las Directivas de Grupo para que Windows respete un poco más la privacidad.
---

Aparte de modificar el propio registro, el **Editor de Directivas de Grupo Local** es la forma más potente de cambiar muchos aspectos del sistema sin instalar herramientas de terceros. Para cambiar estos ajustes se requiere la [Edición Pro](index.md#windows-editions) o superior.

Estos ajustes deben establecerse en una nueva instalación de Windows. Configurarlos en tu instalación existente debería funcionar, pero puede introducir un comportamiento impredecible y lo haces bajo tu propio riesgo.

Todas estas configuraciones tienen una explicación adjunta en el Editor de Directivas de Grupo que explica exactamente lo que hacen, normalmente con gran detalle. Por favor, presta atención a esas descripciones cuando hagas cambios, para que sepas exactamente lo que estamos recomendando aquí. We've also explained some of our choices below whenever the explanation included with Windows is inadequate.

## Administrative Templates

You can find these settings by opening `gpedit.msc` and navigating to **Local Computer Policy** > **Computer Configuration** > **Administrative Templates** in the left sidebar. The headers on this page correspond to folders/subfolders within Administrative Templates, and the bullet points correspond to individual policies.

To change any group policy, double click it and select Enabled or Disabled at the top of the window that appears depending on the recommendations below. Some group policies have additional settings that can be configured, and if that's the case the appropriate settings are noted below as well.

### Sistema

#### Device Guard

- Turn On Virtualization Based Security: **Enabled**
  - Platform Security Level: **Secure Boot and DMA Protection**
  - Secure Launch Configuration: **Enabled**

#### Internet Communication Management

- Turn off Windows Customer Experience Improvement Program: **Enabled**
- Turn off Windows Error Reporting: **Enabled**
- Turn off the Windows Messenger Customer Experience Improvement Program: **Enabled**

Note that disabling the Windows Customer Experience Improvement Program also disables some other tracking features that can be individually controlled with Group Policy as well. We don't list them all here or disable them because this setting covers that.

#### OS Policies

- Allow Clipboard History: **Disabled**
- Allow Clipboard synchronization across devices: **Disabled**
- Enables Activity Feed: **Disabled**
- Allow publishing of User Activities: **Disabled**
- Allow upload of User Activities: **Disabled**

#### Perfiles de usuario

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

Despite the names of these policies, this doesn't _require_ you to do anything by default, but it will unlock the _option_ to have a more complex setup (such as requiring a PIN at startup in addition to the TPM) in the Bitlocker setup wizard.

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

#### Buscar

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
