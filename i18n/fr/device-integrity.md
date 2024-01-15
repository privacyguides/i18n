---
title: Intégrité de l'appareil
icon: material/security
description: Ces outils peuvent être utilisés pour vérifier que vos appareils ne sont pas compromis.
cover: device-integrity.webp
---

Ces outils peuvent être utilisés pour valider l'intégrité de vos appareils mobiles et vérifier s'ils présentent des indicateurs de compromission par des logiciels espions et malveillants tels que Pegasus, Predator ou KingsPawn. Cette page se concentre sur la **sécurité mobile**, car les appareils mobiles ont généralement des systèmes en lecture seule avec des configurations bien connues, de sorte que la détection de modifications malveillantes est plus facile que sur les systèmes de bureau traditionnels. Nous pourrions élargir la portée de cette page dans le futur.

<div class="admonition note" markdown>
<p class="admonition-title">This is an advanced topic</p>

Ces outils peuvent être utiles à certaines personnes. They provide functionality which most people do not need to worry about, and often require more in-depth technical knowledge to use effectively.

</div>

It is **critical** to understand that scanning your device for public indicators of compromise is **not sufficient** to determine that a device is "clean", and not targeted with a particular spyware tool. Reliance on these publicly-available scanning tools can miss recent security developments and give you a false sense of security.

## General Advice

The majority of system-level exploits on modern mobile devices—especially zero-click compromises—are non-persistent, meaning they will not remain or run automatically after a reboot. For this reason, we highly recommend rebooting your device regularly. We recommend everybody reboot their devices once a week at minimum, but if non-persistent malware is of particular concern for you, we and many security experts recommend a daily reboot schedule.

This means an attacker would have to regularly re-infect your device to retain access, although we'll note this is not impossible. Rebooting your device also will not protect you against _persistent_ malware, but this is less common on mobile devices due to modern security features like secure/verified boot.

## Post-Compromise Information & Disclaimer

If any of the following tools indicate a potential compromise by spyware such as Pegasus, Predator, or KingsPawn, we advise that you contact:

- If you are a human rights defender, journalist, or from a civil society organization: [Amnesty International's Security Lab](https://securitylab.amnesty.org/contact-us/)
- If a business or government device is compromised: Contact the appropriate security liason at your enterprise, department, or agency
- Local law enforcement

**We are unable to help you directly beyond this.** We are happy to discuss your specific situation or circumstances and review your results in our [community](https://discuss.privacyguides.net) spaces, but it is unlikely we can assist you beyond what is written on this page.

The tools on this page are only capable of detecting indicators of compromise, not removing them. If you are concerned about having been compromised, we advise that you:

- Consider replacing the device completely
- Consider changing your SIM/eSIM number
- Not restore from a backup, because that backup may be compromised

These tools provide analysis based on the information they have the ability to access from your device, and publicly-accessible indicators of compromise. It is important to keep in mind two things:

1. Indicators of compromise are just that: _indicators_. They are not a definitive finding, and may occasionally be **false positives**. If an indicator of compromise is detected, it means you should do additional research into the _potential_ threat.
2. The indicators of compromise these tools look for are published by threat research organizations, but not all indicators are made available to the public! This means that these tools can present a **false negative**, if your device is infected with spyware which is not detected by any of the public indicators. Reliable and comprehensive digital forensic support and triage requires access to non-public indicators, research and threat intelligence.

## External Verification Tools

External verification tools run on your computer and scan your mobile device for forensic traces which are helpful to identify potential compromise.

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Public indicators of compromise are insufficient to determine that a device is "clean", and not targeted with a particular spyware tool. Reliance on public indicators alone can miss recent forensic traces and give a false sense of security.

Reliable and comprehensive digital forensic support and triage requires access to non-public indicators, research and threat intelligence.

Such support is available to civil society through [Amnesty International's Security Lab](https://www.amnesty.org/en/tech/) or [Access Now’s Digital Security Helpline](https://www.accessnow.org/help/).

</div>

Ces outils peuvent déclencher des faux positifs. Si l'un de ces outils détecte des indicateurs de compromission, vous devez approfondir la question pour déterminer le risque réel. Certains rapports peuvent être des faux positifs basés sur des sites web que vous avez visités dans le passé, et les résultats qui datent de plusieurs années sont probablement soit des faux positifs, soit le signe d'une compromission antérieure (qui n'est plus active).

### Mobile Verification Toolkit

<div class="admonition recommendation" markdown>

![MVT logo](assets/img/device-integrity/mvt.webp){ align=right }

**Mobile Verification Toolkit** (**MVT**) is a collection of utilities which simplifies and automates the process of scanning mobile devices for potential traces of targeting or infection by known spyware campaigns. MVT was developed by Amnesty International and released in 2021 in the context of the [Pegasus Project](https://forbiddenstories.org/about-the-pegasus-project/).

[:octicons-home-16: Homepage](https://mvt.re/){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-apple: macOS](https://docs.mvt.re/en/latest/install/)
- [:simple-linux: Linux](https://docs.mvt.re/en/latest/install/)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

L'utilisation de MVT ne suffit pas à déterminer qu'un appareil est "propre" et qu'il n'est pas la cible d'un logiciel espion particulier.

</div>

MVT est _plus_ utile pour scanner les appareils iOS. Android stocke très peu d'informations de diagnostic utiles pour trier les compromissions potentielles, et pour cette raison, les capacités de `mvt-android` sont également limitées. Par contre, les sauvegardes iTunes iOS chiffrées fournissent un sous-ensemble suffisamment important de fichiers stockés sur l'appareil pour détecter les artefacts suspects dans de nombreux cas. Ceci étant dit, MVT fournit tout de même des outils assez utiles pour l'analyse des systèmes iOS et Android.

Si vous utilisez iOS et que vous présentez un risque élevé, nous avons trois suggestions supplémentaires à vous faire :

1. Créez et conservez des sauvegardes iTunes régulières (mensuelles). Cela vous permet de trouver et de diagnostiquer les infections passées plus tard avec MVT, si de nouvelles menaces sont découvertes dans le futur.

2. Déclenchez souvent des journaux _sysdiagnose_ et sauvegardez-les en externe. Ces journaux peuvent fournir des données inestimables aux futurs enquêteurs criminalistiques si nécessaire.

   La procédure à suivre varie selon le modèle, mais vous pouvez la déclencher sur les téléphones récents en maintenant enfoncées les touches _Alimentation_ + _Volume haut_ + _Volume bas_ jusqu'à ce que vous sentiez une brève vibration. Après quelques minutes, le journal _sysdiagnose_ horodaté apparaîtra dans **Paramètres** > **Confidentialité et sécurité** > **Analytiques et améliorations** > **Données analytiques**.

3. Activer le [mode Isolement](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode).

MVT vous permet d'effectuer des analyses plus approfondies si votre appareil est jailbreaké. À moins que vous ne sachiez ce que vous faites, **ne jailbreakez pas et ne rootez pas votre appareil.** Le jailbreaking de votre appareil l'expose à des risques de sécurité considérables.

### iMazing (iOS)

<div class="admonition recommendation" markdown>

![iMazing logo](assets/img/device-integrity/imazing.png){ align=right }

**iMazing** provides a free spyware analyzer tool for iOS devices which acts as a GUI-wrapper for [MVT](#mobile-verification-toolkit). This can be much easier to run compared to MVT itself, which is a command-line tool designed for technologists and forensic investigators.

[:octicons-home-16: Homepage](https://imazing.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-windows11: Windows](https://imazing.com/download)
- [:simple-apple: macOS](https://imazing.com/download)

</details>

</div>

iMazing automatise et vous guide de manière interactive tout au long du processus d'utilisation de [MVT](#mobile-verification-toolkit) pour analyser votre appareil à la recherche d'indicateurs de compromission accessibles au public et publiés par divers chercheurs en menaces. Toutes les informations et tous les avertissements qui s'appliquent à MVT s'appliquent également à cet outil. Nous vous conseillons donc de vous familiariser également avec les notes sur MVT dans les sections ci-dessus.

## Vérification sur l'appareil

Il s'agit d'applications que vous pouvez installer et qui vérifient que votre appareil et votre système d'exploitation ne présentent pas de signes d'altération et qui valident l'identité de votre appareil.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

L'utilisation de ces applications ne suffit pas à déterminer qu'un appareil est "propre" et qu'il n'est pas la cible d'un logiciel espion particulier.

</div>

### Auditor (Android)

<div class="admonition recommendation" markdown>

![Auditor logo](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![Auditor logo](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**Auditor** is an app which leverages hardware security features to provide device integrity monitoring by actively validating the identity of a device and the integrity of its operating system. Currently, it only works with GrapheneOS or the stock operating system for [supported devices](https://attestation.app/about#device-support).

[:octicons-home-16: Homepage](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentation}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Auditor n'est pas un outil de scan/analyse comme d'autres outils sur cette page, mais il utilise le magasin de clés s'appuyant sur le materiel de votre appareil pour vous permettre de vérifier l'identité de votre appareil et de vous assurer que le système d'exploitation lui-même n'a pas été altéré ou dégradé par le biais d'un démarrage vérifié. Cela fournit un contrôle d'intégrité très solide de l'appareil lui-même, mais qui ne permet pas nécessairement de vérifier si les applications utilisateur exécutées sur l'appareil sont malveillantes.

Auditor effectue l'attestation et la détection d'intrusion avec **deux** appareils, un _audité_ (l'appareil vérifié) et un _auditeur_ (l'appareil effectuant la vérification). L'auditeur peut être n'importe quel appareil Android 10+ (ou un service web distant géré par [GrapheneOS](android.md#grapheneos)), tandis que l'audité doit être un [appareil pris en charge](https://attestation.app/about#device-support) spécifique. Auditor fonctionne comme tel :

- En utilisant un modèle de [confiance à la première utilisation (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) entre un _auditeur_ et un _audité_, la paire établit une clé privée dans le [magasin de clés s'appuyant sur le matériel](https://source.android.com/security/keystore/) de l'_auditeur_.
- L'_auditeur_ peut être une autre instance de l'application Auditor ou le [service d'attestation à distance](https://attestation.app).
- L'_auditeur_ enregistre l'état et la configuration actuels de l'_audité_.
- Si le système d'exploitation de l'_audité_ est altéré après l'appairage, l'auditeur sera informé de la modification de l'état et de la configuration de l'appareil.
- Vous serez alerté de ce changement.

Il est important de noter que l'auditeur ne peut détecter efficacement les changements _qu'après_ l'appairage initial, et pas nécessairement pendant ou avant, en raison de son modèle TOFU. Pour vous assurer que votre matériel et votre système d'exploitation sont authentiques, [effectuez une attestation locale](https://grapheneos.org/install/web#verifying-installation) immédiatement après l'installation de l'appareil et avant toute connexion à l'internet.

Aucune donnée à charactère personnel n'est soumise au service d'attestation. Nous vous recommandons de vous inscrire avec un compte anonyme et d'activer l'attestation à distance pour un contrôle continu.

Si votre [modèle de menace](basics/threat-modeling.md) nécessite une certaine confidentialité, vous pouvez envisager d'utiliser [Orbot](tor.md#orbot) ou un VPN pour cacher votre adresse IP au service d'attestation.

## Scanners embarqués

Il s'agit d'applications que vous pouvez installer sur votre appareil et qui l'analysent pour détecter des signes de compromission.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

L'utilisation de ces applications ne suffit pas à déterminer qu'un appareil est "propre" et qu'il n'est pas la cible d'un logiciel espion particulier.

</div>

### Hypatia (Android)

<div class="admonition recommendation" markdown>

![Hypatia logo](assets/img/device-integrity/hypatia.svg#only-light){ align=right }
![Hypatia logo](assets/img/device-integrity/hypatia-dark.svg#only-dark){ align=right }

**Hypatia** is an open source real-time malware scanner for Android, from the developer of [DivestOS](android.md#divestos). It accesses the internet to download signature database updates, but does not upload your files or any metadata to the cloud (scans are performed entirely locally).

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#hypatia){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy#hypatia){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/divested-mobile/hypatia){ .card-link title="Source Code" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-android: F-Droid](https://f-droid.org/packages/us.spotco.malwarescanner/)

</details>

</div>

Hypatia est particulièrement efficace pour détecter les logiciels de harcèlement : si vous pensez être victime d'un logiciel de harcèlement, vous devriez [visiter cette page](https://stopstalkerware.org/information-for-survivors/) pour obtenir des conseils.

### iVerify (iOS)

<div class="admonition recommendation" markdown>

![iVerify logo](assets/img/device-integrity/iverify.webp){ align=right }

**iVerify** is an iOS app which automatically scans your device to check configuration settings, patch level, and other areas of security. It also checks your device for indicators of compromise by jailbreak tools or spyware such as Pegasus.

[:octicons-home-16: Homepage](https://www.iverify.io/consumer){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.iverify.io/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://www.iverify.io/frequently-asked-questions#iVerify-General){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-appstore: App Store](https://apps.apple.com/us/app/iverify/id1466120520)

</details>

</div>

Comme toutes les applications iOS, iVerify est limité à ce qu'il peut observer sur votre appareil depuis l'iOS App Sandbox. Elle ne fournira pas une analyse aussi solide qu'un outil d'analyse de système complet tel que [MVT](#mobile-verification-toolkit). Sa fonction première est de détecter si votre appareil est jailbreaké, ce qu'elle fait efficacement, mais une menace hypothétique conçue _spécifiquement_ pour contourner les contrôles d'iVerify y parviendrait probablement.

iVerify n'est **pas** un outil "antivirus" et ne détectera pas les logiciels malveillants non liés au système, tels que les claviers personnalisés malveillants ou les synchronisations de configurations Wi-Fi malveillantes, par exemple.

Outre l'analyse de l'appareil, iVerify comprend également un certain nombre d'utilitaires de sécurité supplémentaires qui peuvent s'avérer utiles, notamment des rappels de redémarrage de l'appareil, des notifications de mise à jour iOS (qui sont souvent plus rapides que les notifications de mise à jour échelonnées d'Apple), des guides de base sur la confidentialité et la sécurité, et un outil DNS over HTTPS qui peut connecter les requêtes [DNS](dns.md) de votre appareil de manière sécurisée à Quad9, Cloudflare, ou Google.
