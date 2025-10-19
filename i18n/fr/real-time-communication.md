---
meta_title: "Les meilleures messageries instantanées privées - Privacy Guides"
title: Communication en temps réel
icon: material/chat-processing
description: Les messageries chiffrées telles que Signal et SimpleX protègent vos communications sensibles des regards indiscrets.
cover: real-time-communication.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-bug-outline: Attaques passives](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fournisseurs de service](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: Surveillance de masse](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Ces recommandations pour une **communication** chiffrée **en temps réel** sont très utiles pour sécuriser vos communications sensibles. Ces messageries instantanées se présentent sous la forme de nombreux [types de réseaux de communication](advanced/communication-network-types.md).

[:material-movie-open-play-outline: Vidéo : Il est temps d'arrêter d'utiliser les SMS](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## Signal

<div class="admonition recommendation" markdown>

![Logo de Signal](assets/img/messengers/signal.svg){ align=right }

**Signal** est une application mobile développée par Signal Messenger LLC. L'application fournit un service de communication instantanée et d'appels sécurisés avec le protocole Signal, un chiffrement êxtremement robuste compatible avec la confidentialité persistante (forward secrecy)[^1] et la sécurité post-compromission.[^2]

[:octicons-home-16: Page d'Accueil](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://support.signal.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Code Source" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-github: GitHub](https://github.com/signalapp/Signal-Android/releases)
- [:simple-android: Android](https://signal.org/android/apk)
- [:fontawesome-brands-windows: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal a besoin de votre numéro de téléphone pour créer un compte, vous devriez donc choisir un nom d'utilisateur afin de le cacher :

1. Dans Signal, ouvrez les paramètres de l'application et appuyez sur votre profil en haut.
2. Appuyez sur **Nom d'utilisateur** et choisissez **Continuer** sur l'écran "Configurez votre nom d'utilisateur Signal".
3. Entrez un nom d'utilisateur. Votre nom d'utilisateur sera toujours associé à un ensemble de chiffre afin qu'il soit unique et pour empêcher d'autres personnes de le deviner. Par exemple si vous utiliser "Jean" comme nom d'utilisateur, celui-ci pourra devenir `@Jean35`. Par défaut, seulement deux chiffres sont associés à votre nom d'utilisateur lorsque vous le créer, mais vous pouvez en ajouter si vous le souhaitez (dans la limite de 32 caractères.
4. Retournez à la page principale des paramètres de l'application et sélectionnez **Confidentialité**.
5. Sélectionnez **Numéro de Téléphone**.
6. Définissez le paramètre **Qui peut voir mon numéro** sur **Personne**.
7. (Optionnel) Si vous souhaitez que les personnes ayant déjà votre numéro de téléphone ne puissent pas l'utiliser pour vous trouver sur Signal, définissez le paramètre **Qui peut me trouver grâce à mon numéro** sur **Personne**

Voici quelques conseils supplémentaires pour paramétrer votre Signal :

[Configuration et Renforcement de Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

Les listes de contacts sur Signal sont chiffrées avec votre PIN Signal et leur serveurs n'y ont pas accès. Votre profil est également chiffré et n'est partagé qu'avec les contacts avec lesquels vous discutez.

Signal permet de créer des [groupes privés](https://signal.org/blog/signal-private-group-system), qui permettent de ne laisser aucune trace ni des membres, ni des titres, avatars ou attributs du groupe dans leur serveur. Lorsque [Expéditeurs scellés](https://signal.org/blog/sealed-sender) est activé, Signal minimise le plus possible les métadonnées. L'adresse de l'expéditeur est chiffrée en plus du contenu du message, et seule l'adresse du destinataire est visible du serveur. L'option Expéditeurs scellés est activée uniquement pour les personnes dans votre liste de contact mais peut être activée pour tous les destinataires, bien que cela augmente le risque de recevoir du spam.

Le protocole a été [audité](https://eprint.iacr.org/2016/1013.pdf) par un tiers indépendant en 2016. Les spécificités du protocole Signal peuvent être trouvées dans leur [documentation](https://signal.org/docs).

### Molly (Android)

Si vous êtes sous Android et que votre modèle de menace vous expose à des [:material-target-account: Attaques Ciblées](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}, cette application peut vous permettre d'utiliser le réseau de Signal tout en apportant des améliorations de sécurité et d'ergonomie.

<div class="admonition recommendation" markdown>

![Logo de Molly](assets/img/messengers/molly.svg){ align=right }

**Molly** est un client alternatif de Signal pour Android qui vous permet de chiffrer la base de données locale avec une phrase de passe après la mise en veille afin de détruire de façon sécurisée les données de RAM non utilisées, de faire passer votre connexion par Tor, [et bien d'autres](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features). Elle permet également de programmer une sauvegarde automatique, de verrouiller l'application automatiquement et d'avoir la possibilité d'utiliser votre téléphone Android comme appareil lié plutôt que comme appareil principal pour un compte Signal.

[:octicons-home-16: Page d'Accueil](https://molly.im){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Plitique de Confidentialité" }
[:octicons-info-16:](https://github.com/mollyim/mollyim-android/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mollyim/mollyim-android){ .card-link title="Code Source" }
[:octicons-heart-16:](https://opencollective.com/mollyim){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-fdroid: F-Droid](https://molly.im/fdroid)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/im.molly.app)
- [:simple-github: GitHub](https://github.com/mollyim/mollyim-android/releases)

</details>

</div>

Molly est mise à jour toutes les deux semaines afin d'inclure les dernières fonctionnalités et les corrections de bug de Signal. Les mis à jour de sécurité sont quant à elles mise à disposition le plus vite possible. Il peut parfois il y avoir un petit délai, ce qui peut affecter certaines actions, comme la [migration de Signal à Molly](https://github.com/mollyim/mollyim-android/wiki/Migrating-From-Signal#migrating-from-signal).

Lorsque vous utilisez Molly, vous faites confiance à plusieurs intermédiaires pour vous fournir rapidement des mises à jour sécurisées, à savoir l'équipe de Signal *et* l'équipe de Molly.

**Molly-FOSS** est une version de Molly qui retire tout le code propriétaire utilisé par Signal et Molly comme les services Google, au prix de certaines fonctionnalités (les notifications push économisant la batterie via les services Google Play). Vous pouvez paramétrer les notifications push sans les services Google dans les deux versions de Molly avec [UnifiedPush](https://unifiedpush.org). Cette méthode d'envoi de notifications nécessite l'accès à un serveur [MollySocket](https://github.com/mollyim/mollysocket), mais vous pouvez choisir une instance publique de MollySocket.[^3]

Les deux versions de Molly possèdent les mêmes améliorations de sécurité et sont compatibles avec les [builds reproductibles](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds), ce qui vous permet de confirmer que les APKs correspondent au code source.

## SimpleX Chat

<div class="admonition recommendation" markdown>

![Logo de SimpleX Chat](assets/img/messengers/simplex.svg){ align=right }

**SimpleX Chat** est un service de messagerie instantanée qui ne dépend pas d'identifiant unique comme un numéro de téléphone ou un nom d'utilisateur. Son réseau décentralisé en fait un outil efficace contre la [:material-close-outline: Censure](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16: Page d'Accueil](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplex.chat/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://simplex.chat/docs/simplex.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:fontawesome-brands-windows: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)
- [:simple-flathub: Flathub](https://flathub.org/en/apps/chat.simplex.simplex)

</details>

</div>

SimpleX Chat permet d'envoyer des messages, de créer des conversations de groupes et de passer des appels chiffrés de bout-en-bout sécurisés avec le [Protocle SimpleX Messaging](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md), qui utilise un chiffrement à double ratchets résistant aux attaques quantiques. De plus, SimpleX protège les métadonnées en utilisant des ["simplex queues"](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md#simplex-queue) unidirectionnelles pour l'envoi des messages.

Pour participer à des conversations dans SimpleX Chat, vous devez scanner un QR code ou cliquer sur un lien d'invitation. Cela vous permet de vérifier un contact hors bande (out-of-band), ce qui vous protège des attaques man-in-the-middle des fournisseurs de réseaux. Vos données peuvent être exportées et importées sur un autre appareil et il n'existe aucune sauvegarde sur un serveur central.

Vous pouvez trouver la liste complète des [fonctionnalités](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations) de confidentialité et de sécurité mises en place par SimpleX Chat dans le dépôt de l'application.

SimpleX Chat a été audité par un organisme indépendant en [juillet 2024](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits) et en [octobre 2022](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website).

## Briar

<div class="admonition recommendation" markdown>

![Logo de Briar](assets/img/messengers/briar.svg){ align=right }

**Briar** est une messagerie instantanée qui [se connecte](https://briarproject.org/how-it-works) to aux autres clients en utilisant le [réseau Tor](alternative-networks.md#tor), ce qui en fait un outil efficace pour contourner la [:material-close-outline: Censure](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar peut également se connecter par Wi-Fi ou Bluetooth lorsqu'il se trouve à proximité. Le mode de maillage local de Briar peut être utile lorsque la disponibilité d’internet pose problème.

[:octicons-home-16: Page d'Accueil](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title="Documentation" }
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Code Source" }
[:octicons-heart-16:](https://code.briarproject.org/briar/briar#donate){ .card-link title="Contribuer" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Pour ajouter un contact sur Briar, vous devez vous ajouter mutuellement. You can either exchange `briar://` links or scan a contact’s QR code if they are nearby.

Briar has a fully [published specification](https://code.briarproject.org/briar/briar-spec). Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit), and the anonymous routing protocol uses the Tor network which has also been audited.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Must have open-source clients.
- Must not require sharing personal identifiers (particularly phone numbers or emails) with contacts.
- Must use E2EE for private messages by default.
- Must support E2EE for all messages.
- Must support forward secrecy[^1]
- Doit disposer d'un audit publié par une tierce partie indépendante et réputée.

### Critères optimaux

Nos critères optimaux représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de ces fonctionnalités, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Should support future secrecy (post-compromise security)[^2]
- Should have open-source servers.
- Should use a decentralized network, i.e. [federated or P2P](advanced/communication-network-types.md).
- Should use E2EE for all messages by default.
- Should support Linux, macOS, Windows, Android, and iOS.
[^3]: You may refer to this step-by-step tutorial in German on how to set up UnifiedPush as the notification provider for Molly: [https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy](https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy).

[^1]: [Forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future secrecy (or [post-compromise security](https://eprint.iacr.org/2016/221.pdf)) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties since they lose access as soon as a key exchange occurs that is not intercepted.
