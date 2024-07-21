---
title: Intégrité de l'appareil
icon: material/security
description: Ces outils peuvent être utilisés pour vérifier que vos appareils ne sont pas compromis.
cover: device-integrity.webp
---

Ces outils peuvent être utilisés pour valider l'intégrité de vos appareils mobiles et vérifier s'ils présentent des indicateurs de compromission par des logiciels espions et malveillants tels que Pegasus, Predator ou KingsPawn. Cette page se concentre sur la **sécurité mobile**, car les appareils mobiles ont généralement des systèmes en lecture seule avec des configurations bien connues, de sorte que la détection de modifications malveillantes est plus facile que sur les systèmes de bureau traditionnels. Nous pourrions élargir la portée de cette page dans le futur.

<div class="admonition note" markdown>
<p class="admonition-title">Il s'agit d'un sujet avancé</p>

These tools may provide utility for certain individuals. Ils offrent des fonctionnalités dont la plupart des gens n'ont pas besoin de se préoccuper, et nécessitent souvent des connaissances techniques plus approfondies pour être utilisés efficacement.

</div>

Il est **critique** de comprendre que l'analyse de votre appareil à la recherche d'indicateurs publics de compromission n'est **pas suffisante** pour déterminer qu'un appareil est "propre" et qu'il n'est pas la cible d'un logiciel espion particulier. En vous fiant à ces outils d'analyse accessibles au public, vous risquez de passer à côté d'évolutions récentes en matière de sécurité et de vous donner un faux sentiment de sécurité.

## Conseil général

La majorité des exploits au niveau du système sur les appareils mobiles modernes - en particulier les compromissions en zéro clic - sont non persistants, ce qui signifie qu'ils ne resteront pas ou ne s'exécuteront pas automatiquement après un redémarrage. C'est pourquoi nous vous recommandons vivement de redémarrer votre appareil régulièrement. Nous recommandons à chacun de redémarrer son appareil au moins une fois par semaine, mais si les logiciels malveillants non persistants vous préoccupent particulièrement, nous recommandons, comme de nombreux experts en sécurité, de procéder à un redémarrage quotidien.

Cela signifie qu'un attaquant devrait régulièrement réinfecter votre appareil pour en conserver l'accès, bien que cela ne soit pas impossible. Le redémarrage de votre appareil ne vous protège pas non plus contre les logiciels malveillants _persistants_, mais cela est moins fréquent sur les appareils mobiles en raison des fonctions de sécurité modernes telles que le démarrage sécurisé/vérifié.

## Information post-compromission et avertissement

Si l'un des outils suivants indique une compromission potentielle par un logiciel espion tel que Pegasus, Predator ou KingsPawn, nous vous conseillons de contacter :

- If you are a human rights defender, journalist, or from a civil society organization: [Amnesty International's Security Lab](https://securitylab.amnesty.org/contact-us)
- If a business or government device is compromised: the appropriate security liason at your enterprise, department, or agency
- Les forces de l'ordre locales

**Nous ne sommes pas en mesure de vous aider directement au-delà de ces conseils.** Nous sommes disposés à discuter de votre situation ou de vos circonstances particulières et à examiner vos résultats dans nos espaces [communautaires](https://discuss.privacyguides.net), mais il est peu probable que nous puissions vous aider au-delà de ce qui est écrit sur cette page.

Les outils présentés sur cette page sont uniquement capables de détecter les indicateurs de compromission, et non de les supprimer. Si vous craignez d'avoir été compromis, nous vous conseillons de procéder comme suit :

- Envisager le remplacement complet de l'appareil
- Envisagez de changer de numéro SIM/eSIM
- Ne pas restaurer à partir d'une sauvegarde, car cette dernière peut être compromise

Ces outils fournissent une analyse basée sur les informations auxquelles ils ont accès à partir de votre appareil et sur les indicateurs de compromission accessibles au public. Il est important de garder à l'esprit deux choses :

1. Les indicateurs de compromissions ne sont que cela : des _indicateurs_. Ils ne constituent pas un résultat définitif et peuvent parfois être des **faux positifs**. Si un indicateur de compromission est détecté, cela signifie que vous devez effectuer des recherches supplémentaires sur la menace _potentielle_.
2. Les indicateurs de compromission recherchés par ces outils sont publiés par des organismes de recherche sur les menaces, mais tous les indicateurs ne sont pas mis à la disposition du public ! Cela signifie que ces outils peuvent présenter un **faux négatif**, si votre appareil est infecté par un logiciel espion qui n'est détecté par aucun des indicateurs publics. Reliable and comprehensive digital forensic support and triage require access to non-public indicators, research, and threat intelligence.

## Outils de vérification externes

External verification tools run on your computer and scan your mobile device for forensic traces, which are helpful to identify potential compromise.

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Les indicateurs publics de compromission ne suffisent pas à déterminer qu'un appareil est "propre" et qu'il n'a pas été ciblé par un logiciel espion particulier. En se fiant uniquement aux indicateurs publics, il est possible de passer à côté de traces médico-légales récentes et de donner un faux sentiment de sécurité.

Reliable and comprehensive digital forensic support and triage require access to non-public indicators, research, and threat intelligence.

Such support is available to civil society through [Amnesty International's Security Lab](https://amnesty.org/en/tech) or [Access Now’s Digital Security Helpline](https://accessnow.org/help).

</div>

Ces outils peuvent déclencher des faux positifs. Si l'un de ces outils détecte des indicateurs de compromission, vous devez approfondir la question pour déterminer le risque réel. Certains rapports peuvent être des faux positifs basés sur des sites web que vous avez visités dans le passé, et les résultats qui datent de plusieurs années sont probablement soit des faux positifs, soit le signe d'une compromission antérieure (qui n'est plus active).

### Mobile Verification Toolkit

<div class="admonition recommendation" markdown>

![Logo MVT](assets/img/device-integrity/mvt.webp){ align=right }

Le **Mobile Verification Toolkit** (**MVT**) est une collection d'utilitaires qui simplifie et automatise le processus d'analyse des appareils mobiles à la recherche de traces potentielles de ciblage ou d'infection par des campagnes connues de logiciels espions. MVT was developed by Amnesty International and released in 2021 in the context of the [Pegasus Project](https://forbiddenstories.org/about-the-pegasus-project).

[:octicons-home-16: Homepage](https://mvt.re){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-apple: macOS](https://docs.mvt.re/en/latest/install)
- [:simple-linux: Linux](https://docs.mvt.re/en/latest/install)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

L'utilisation de MVT ne suffit pas à déterminer qu'un appareil est "propre" et qu'il n'est pas la cible d'un logiciel espion particulier.

</div>

MVT est _plus_ utile pour scanner les appareils iOS. Android stores very little diagnostic information useful to triage potential compromises, and because of this, `mvt-android` capabilities are limited as well. Par contre, les sauvegardes iTunes iOS chiffrées fournissent un sous-ensemble suffisamment important de fichiers stockés sur l'appareil pour détecter les artefacts suspects dans de nombreux cas. Ceci étant dit, MVT fournit tout de même des outils assez utiles pour l'analyse des systèmes iOS et Android.

Si vous utilisez iOS et que vous présentez un risque élevé, nous avons trois suggestions supplémentaires à vous faire :

1. Créez et conservez des sauvegardes iTunes régulières (mensuelles). Cela vous permet de trouver et de diagnostiquer les infections passées plus tard avec MVT, si de nouvelles menaces sont découvertes dans le futur.

2. Déclenchez souvent des journaux _sysdiagnose_ et sauvegardez-les en externe. Ces journaux peuvent fournir des données inestimables aux futurs enquêteurs criminalistiques si nécessaire.

   La procédure à suivre varie selon le modèle, mais vous pouvez la déclencher sur les téléphones récents en maintenant enfoncées les touches _Alimentation_ + _Volume haut_ + _Volume bas_ jusqu'à ce que vous sentiez une brève vibration. Après quelques minutes, le journal _sysdiagnose_ horodaté apparaîtra dans **Paramètres** > **Confidentialité et sécurité** > **Analytiques et améliorations** > **Données analytiques**.

3. Activer le [mode Isolement](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode).

MVT vous permet d'effectuer des analyses plus approfondies si votre appareil est jailbreaké. À moins que vous ne sachiez ce que vous faites, **ne jailbreakez pas et ne rootez pas votre appareil.** Le jailbreaking de votre appareil l'expose à des risques de sécurité considérables.

### iMazing (iOS)

<div class="admonition recommendation" markdown>

![logo iMazing](assets/img/device-integrity/imazing.png){ align=right }

**iMazing** fournit un outil gratuit d'analyse des logiciels espions pour les appareils iOS qui agit comme une interface graphique pour [MVT](#mobile-verification-toolkit). Il peut être beaucoup plus facile à utiliser que MVT, qui lui est un outil en ligne de commande conçu pour les technologues et les enquêteurs judiciaires.

[:octicons-home-16: Homepage](https://imazing.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:fontawesome-brands-windows: Windows](https://imazing.com/download)
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

![logo Auditor](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![logo Auditor](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**Auditor** est une application qui exploite les fonctions de sécurité matérielle pour assurer la surveillance de l'intégrité des appareils en validant activement l'identité d'un appareil et l'intégrité de son système d'exploitation. Actuellement, elle ne fonctionne qu'avec GrapheneOS ou le système d'exploitation de base pour les [appareils pris en charge](https://attestation.app/about#device-support).

[:octicons-home-16: Page d'accueil](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentation}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="Code source" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
- [:material-cube-outline: Magasin d'applications de GrapheneOS](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Auditor is not a scanning/analysis tool like some other tools on this page. Rather, it uses your device's hardware-backed keystore to allow you to verify the identity of your device and gain assurance that the operating system itself hasn't been tampered with or downgraded via verified boot. Cela fournit un contrôle d'intégrité très solide de l'appareil lui-même, mais qui ne permet pas nécessairement de vérifier si les applications utilisateur exécutées sur l'appareil sont malveillantes.

Auditor effectue l'attestation et la détection d'intrusion avec **deux** appareils, un _audité_ (l'appareil vérifié) et un _auditeur_ (l'appareil effectuant la vérification). The auditor can be any Android 10+ device (or a remote web service operated by [GrapheneOS](android/distributions.md#grapheneos)), while the auditee must be a specifically [supported device](https://attestation.app/about#device-support). Auditor fonctionne comme tel :

- Using a [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) model between an _auditor_ and _auditee_, the pair establish a private key in the [hardware-backed keystore](https://source.android.com/security/keystore) of the _Auditor_.
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

![logo Hypatia](assets/img/device-integrity/hypatia.svg#only-light){ align=right }
![logo Hypatia](assets/img/device-integrity/hypatia-dark.svg#only-dark){ align=right }

**Hypatia** is an open source real-time malware scanner for Android, from the developer of [DivestOS](android/distributions.md#divestos). It accesses the internet to download signature database updates, but does not upload your files or any metadata to the cloud (scans are performed entirely locally).

[:octicons-home-16: Page d'accueil](https://divestos.org/pages/our_apps#hypatia){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy#hypatia){ .card-link title="Politique de confidentialité" }
[:octicons-code-16:](https://github.com/divested-mobile/hypatia){ .card-link title="Code source" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/packages/us.spotco.malwarescanner)

</details>

</div>

Hypatia is particularly good at detecting common stalkerware: If you suspect you are a victim of stalkerware, you should [visit this page](https://stopstalkerware.org/information-for-survivors) for advice.

### iVerify Basic (iOS)

<div class="admonition recommendation" markdown>

![logo iVerify](assets/img/device-integrity/iverify.webp){ align=right }

**iVerify Basic** is an iOS app which can scan your device to check configuration settings, patch level, and other areas of security. Il vérifie également que votre appareil ne présente pas d'indicateurs de compromission par des outils de jailbreak ou des logiciels espions tels que Pegasus.

[:octicons-home-16: Homepage](https://iverify.io/products/basic){ .md-button .md-button--primary }
[:octicons-eye-16:](https://iverify.io/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://iverify.io/frequently-asked-questions#iVerify-General){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1466120520)

</details>

</div>

Previously, iVerify would scan your device for threats automatically in the background and notify you if one is found, but this is [no longer the case](https://discuss.privacyguides.net/t/iverify-basic-is-now-available-on-android/18458/11) following their rebrand of the consumer app to _iVerify Basic_ in May 2024. You can still run manual scans within the app. Automatic background scanning is now only available in iVerify's enterprise product which is unavailable to consumers.

Like all iOS apps, iVerify Basic is restricted to what it can observe about your device from within the iOS App Sandbox. Elle ne fournira pas une analyse aussi solide qu'un outil d'analyse de système complet tel que [MVT](#mobile-verification-toolkit). Sa fonction première est de détecter si votre appareil est jailbreaké, ce qu'elle fait efficacement, mais une menace hypothétique conçue _spécifiquement_ pour contourner les contrôles d'iVerify y parviendrait probablement.

iVerify Basic is **not** an "antivirus" tool, and will not detect non-system-level malware such as malicious custom keyboards or malicious Wi-Fi Sync configurations, for example.

In addition to device scanning, iVerify Basic also includes a number of additional security utilities which you may find useful, including device [reboot reminders](os/ios-overview.md#before-first-unlock), iOS update notifications (which are often faster than Apple's staggered update notification rollout), and some basic privacy and security guides.
