---
meta_title: "Les meilleures messageries instantanées privées - Privacy Guides"
title: "Communication en temps réel"
icon: material/chat-processing
description: Les autres messageries instantanées mettent toutes vos conversations privées à la disposition de la société qui les gère.
cover: real-time-communication.webp
---

Voici nos recommandations pour de la communication en temps réel chiffrée.

[Types de réseaux de communication :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## Messageries instantanées chiffrées

Ces messageries sont idéales pour sécuriser vos communications sensibles.

### Signal

<div class="admonition recommendation" markdown>

![Logo de Signal](assets/img/messengers/signal.svg){ align=right }

**Signal** est une application mobile développée par Signal Messenger LLC. L'application fournit une messagerie instantanée et des appels sécurisés avec le protocole Signal, un protocole de chiffrement extrêmement sécurisé qui prend en charge la confidentialité persistante[^1] et la sécurité post-compromission.[^2]

[:octicons-home-16: Page d'accueil](https://signal.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://support.signal.org/hc/en-us){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Code source" }
[:octicons-heart-16:](https://signal.org/donate/){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk/)
- [:simple-windows11: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal demande votre numéro de téléphone pour l'enregistrement, mais vous devriez créer un nom d'utilisateur pour cacher votre numéro de téléphone à vos contacts :

1. Dans Signal, ouvrez les paramètres de l'application et appuyez sur votre profil en haut.
2. Appuyez sur **Nom d'utilisateur** et choisissez **Continuer** sur l'écran "Configurez votre nom d'utilisateur Signal".
3. Entrez un nom d'utilisateur. Your username will always be paired with a unique set of digits to keep your username unique and prevent people from guessing it, for example if you enter "John" your username might end up being `@john.35`.
4. Go back to the main app settings page and select **Privacy**.
5. Select **Phone Number**
6. Change the **Who Can See My Number** setting to: **Nobody**

You can optionally change the **Who Can Find Me By Number** setting to **Nobody** as well, if you want to prevent people who already have your phone number from discovering your Signal account/username.

Contact lists on Signal are encrypted using your Signal PIN and the server does not have access to them. Les profils personnels sont également chiffrés et ne sont partagés qu'avec les contacts qui vous ajoutent. Signal supports [private groups](https://signal.org/blog/signal-private-group-system/), where the server has no record of your group memberships, group titles, group avatars, or group attributes. Signal expose un minimum de métadonnées lorsque l'option [Expéditeur Scellé](https://signal.org/blog/sealed-sender/) est activée. L'adresse de l'expéditeur est chiffrée avec le corps du message, et seule l'adresse du destinataire est visible par le serveur. Expéditeur Scellé est uniquement activé pour les personnes de votre liste de contacts, mais peut être activé pour tous les destinataires avec le risque accru de recevoir du spam.

Le protocole a fait l'objet d'un [audit](https://eprint.iacr.org/2016/1013.pdf) indépendant en 2016. La spécification du protocole Signal se trouve dans leur [documentation](https://signal.org/docs/).

Nous avons quelques conseils supplémentaires pour configurer et renforcer votre installation Signal :

[Configuration et renforcement de Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening/)

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Logo Simplex](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat est une messagerie instantanée décentralisée qui ne dépend d'aucun identifiant unique tel qu'un numéro de téléphone ou un nom d'utilisateur. Les utilisateurs de SimpleX Chat peuvent scanner un code QR ou cliquer sur un lien d'invitation pour participer à des conversations de groupe.

[:octicons-home-16: Page d'accueil](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/simplex-chat/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:simple-windows11: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX Chat [a été audité](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) par Trail of Bits en Octobre 2022.

SimpleX Chat prend en charge les fonctionnalités de base des conversations de groupe, des messages directs et de l'édition de messages et du markdown. Les appels audio et vidéo E2EE sont également pris en charge. Vos données peuvent être exportées et importées sur un autre appareil, car il n'y a pas de serveur central où elles sont sauvegardées.

### Briar

<div class="admonition recommendation" markdown>

![Logo Briar](assets/img/messengers/briar.svg){ align=right }

**Briar** est une messagerie instantanée chiffrée qui se [connecte](https://briarproject.org/how-it-works/) à d'autres clients par le réseau Tor. Briar peut également se connecter par Wi-Fi ou Bluetooth lorsqu'il se trouve à proximité. Le mode de maillage local de Briar peut être utile lorsque la disponibilité d’internet pose problème.

[:octicons-home-16: Page d'accueil](https://briarproject.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy/){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Code source" }
[:octicons-heart-16:](https://briarproject.org/){ .card-link title="Les options de dons sont listées en bas de la page d'accueil" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:simple-windows11: Windows](https://briarproject.org/download-briar-desktop/)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop/)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Pour ajouter un contact sur Briar, vous devez d'abord vous ajouter tous les deux. Vous pouvez soit échanger des liens `briar://` soit scanner le QR code d'un contact s'il se trouve à proximité.

Le logiciel client a été indépendamment [audité](https://briarproject.org/news/2017-beta-released-security-audit/) et le protocole de routage anonyme utilise le réseau Tor qui a également été audité.

Briar a un [cahier des charges](https://code.briarproject.org/briar/briar-spec) entièrement publié.

Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## Autres options

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

These messengers do not have forward secrecy[^1], and while they fulfill certain needs that our previous recommendations may not, we do not recommend them for long-term or sensitive communications. Toute compromission de la clé parmi les destinataires du message affecterait la confidentialité de **toutes** les communications passées.

</div>

### Element

<div class="admonition recommendation" markdown>

![Logo d'Element](assets/img/messengers/element.svg){ align=right }

**Element** est le [client](https://matrix.org/ecosystem/clients/) de référence pour le protocole [Matrix](https://matrix.org/docs/guides/introduction), un [standard ouvert](https://matrix.org/docs/spec) pour la communication décentralisée sécurisée en temps réel.

Les messages et les fichiers partagés dans les salons privés (ceux qui nécessitent une invitation) sont par défaut E2EE, tout comme les appels vocaux et vidéo individuels.

[:octicons-home-16: Page d'accueil](https://element.io/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/vector-im){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/vector/id1083446067)
- [:simple-github: GitHub](https://github.com/vector-im/element-android/releases)
- [:simple-windows11: Windows](https://element.io/get-started)
- [:simple-apple: macOS](https://element.io/get-started)
- [:simple-linux: Linux](https://element.io/get-started)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

Les photos de profil, les réactions et les surnoms ne sont pas chiffrés.

Les appels vocaux et vidéo de groupe ne sont [pas](https://github.com/vector-im/element-web/issues/12878) E2EE, et utilisent Jitsi, mais cela devrait changer avec [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401). Les appels de groupe n'ont [pas d'authentification](https://github.com/vector-im/element-web/issues/13074) actuellement, ce qui signifie que les participants ne faisant pas partie de la salle peuvent également se joindre aux appels. Nous vous recommandons de ne pas utiliser cette fonctionnalité pour les réunions privées.

The Matrix protocol itself [theoretically supports forward secrecy](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], however this is [not currently supported in Element](https://github.com/vector-im/element-web/issues/7101) due to it breaking some aspects of the user experience such as key backups and shared message history.

Le protocole a fait l'objet d'un [audit](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) indépendant en 2016. La spécification du protocole Matrix se trouve dans leur [documentation](https://spec.matrix.org/latest/). Le [cliquet cryptographique Olm](https://matrix.org/docs/matrix-concepts/end-to-end-encryption/) utilisé par Matrix est une implémentation de l'[algorithme à double cliquet](https://signal.org/docs/specifications/doubleratchet/) de Signal.

### Session

<div class="admonition recommendation" markdown>

![Logo de Session](assets/img/messengers/session.svg){ align=right }

**Session** est une messagerie décentralisée axée sur les communications privées, sécurisées et anonymes. Session prend en charge les messages directs, les discussions de groupe et les appels vocaux.

Session utilise le réseau décentralisé [Oxen Service Node Network](https://oxen.io/) pour stocker et acheminer les messages. Chaque message chiffré est acheminé via trois nœuds dans le Oxen Service Node Network, ce qui rend pratiquement impossible pour les nœuds de compiler des informations significatives sur ceux qui utilisent le réseau.

[:octicons-home-16: Page d'accueil](https://getsession.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:simple-windows11: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

Session permet l'E2EE dans les chats individuels ou des groupes fermés pouvant compter jusqu'à 100 membres. Les groupes ouverts n'ont aucune restriction sur le nombre de membres, mais sont ouverts par conception.

Session was previously based on Signal Protocol before replacing it with their own in December 2020. Session Protocol does [not](https://getsession.org/blog/session-protocol-technical-information) support forward secrecy.[^1]

Oxen requested an independent audit for Session in March 2020. The audit [concluded](https://getsession.org/session-code-audit) in April 2021, “The overall security level of this application is good and makes it usable for privacy-concerned people.”

Session has a [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) describing the technical details of the app and protocol.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

<div class="admonition example" markdown>
<p class="admonition-title">Cette section est nouvelle</p>

Nous travaillons à l'établissement de critères définis pour chaque section de notre site, et celles-ci peuvent être sujet à changement. Si vous avez des questions sur nos critères, veuillez [poser la question sur notre forum](https://discuss.privacyguides.net/latest) et ne supposez pas que nous n'avons pas pris en compte un élément dans nos recommandations s'il ne figure pas dans la liste. De nombreux facteurs sont pris en compte et discutés lorsque nous recommandons un projet, et la documentation de chacun d'entre eux est en cours.

</div>

- Has open-source clients.
- Does not require sharing personal identifiers (phone numbers or emails in particular) with contacts.
- Uses E2EE for private messages by default.
- Supports E2EE for all messages.
- Has been independently audited.

### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Supports Forward Secrecy[^1]
- Supports Future Secrecy (Post-Compromise Security)[^2]
- Has open-source servers.
- Decentralized, i.e. [federated or P2P](advanced/communication-network-types.md).
- Uses E2EE for all messages by default.
- Supports Linux, macOS, Windows, Android, and iOS.

[^1]: [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future Secrecy (or Post-Compromise Security) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties, since they lose access as soon as a key exchange occurs that is not intercepted.
