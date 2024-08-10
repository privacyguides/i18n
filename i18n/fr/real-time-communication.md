---
meta_title: "Les meilleures messageries instantanées privées - Privacy Guides"
title: "Communication en temps réel"
icon: material/chat-processing
description: Les autres messageries instantanées mettent toutes vos conversations privées à la disposition de la société qui les gère.
cover: real-time-communication.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Attaques passives](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fournisseurs de service](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: Surveillance de masse](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our recommendations for encrypted **real-time communication**.

[Types de réseaux de communication :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## Messageries instantanées chiffrées

Ces messageries sont idéales pour sécuriser vos communications sensibles.

### Signal

<div class="admonition recommendation" markdown>

![Logo de Signal](assets/img/messengers/signal.svg){ align=right }

**Signal** est une application mobile développée par Signal Messenger LLC. The app provides instant messaging and calls secured with the Signal Protocol, an extremely secure encryption protocol which supports forward secrecy[^1] and post-compromise security.[^2]

[:octicons-home-16: Homepage](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk)
- [:fontawesome-brands-windows: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal demande votre numéro de téléphone pour l'enregistrement, mais vous devriez créer un nom d'utilisateur pour cacher votre numéro de téléphone à vos contacts :

1. Dans Signal, ouvrez les paramètres de l'application et appuyez sur votre profil en haut.
2. Appuyez sur **Nom d'utilisateur** et choisissez **Continuer** sur l'écran "Configurez votre nom d'utilisateur Signal".
3. Entrez un nom d'utilisateur. Votre nom d'utilisateur sera toujours combiné avec un ensemble unique de chiffres afin que votre nom d'utilisateur reste unique et que personne ne puisse le deviner. Par exemple, si vous entrez "John", votre nom d'utilisateur pourrait être `@john.35`. By default, only 2 digits are paired with your username when you create it, but you can add more digits until you reach the username length limit (32 characters).
4. Retournez à la page principale des paramètres de l'application et sélectionnez **Confidentialité**.
5. Sélectionnez **Numéro de téléphone**
6. Modifiez le paramètre **Qui peut voir mon numéro** et mettre : **Personne**

Vous pouvez également modifier le paramètre **Qui peut me retrouver grâce à mon numéro de téléphone** et mettre **Personne** si vous souhaitez empêcher les personnes qui possèdent déjà votre numéro de téléphone de trouver votre compte/nom d'utilisateur Signal.

La liste des contacts sur Signal est chiffrée à l'aide de votre code PIN Signal et le serveur n'y a pas accès. Votre profil est également chiffré et n'est partagé qu'avec les contacts avec lesquels vous discutez. Signal supports [private groups](https://signal.org/blog/signal-private-group-system), where the server has no record of your group memberships, group titles, group avatars, or group attributes. Signal has minimal metadata when [Sealed Sender](https://signal.org/blog/sealed-sender) is enabled. L'adresse de l'expéditeur est chiffrée avec le corps du message, et seule l'adresse du destinataire est visible par le serveur. Expéditeur Scellé est uniquement activé pour les personnes de votre liste de contacts, mais peut être activé pour tous les destinataires avec le risque accru de recevoir du spam.

Le protocole a fait l'objet d'un [audit](https://eprint.iacr.org/2016/1013.pdf) indépendant en 2016. The specification for the Signal protocol can be found in their [documentation](https://signal.org/docs).

Nous avons quelques conseils supplémentaires pour configurer et renforcer votre installation Signal :

[Configuration et renforcement de Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat is an instant messenger that doesn't depend on any unique identifiers such as phone numbers or usernames. Its decentralized network makes SimpleX Chat an effective tool against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Les utilisateurs de SimpleX Chat peuvent scanner un code QR ou cliquer sur un lien d'invitation pour participer à des conversations de groupe.

[:octicons-home-16: Page d'accueil](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:fontawesome-brands-windows: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX Chat [a été audité](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) par Trail of Bits en Octobre 2022.

SimpleX Chat prend en charge les fonctionnalités de base des conversations de groupe, des messages directs et de l'édition de messages et du markdown. Les appels audio et vidéo E2EE sont également pris en charge. Vos données peuvent être exportées et importées sur un autre appareil, car il n'y a pas de serveur central où elles sont sauvegardées.

### Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works) to other clients using the Tor Network, making it an effective tool at circumventing [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar peut également se connecter par Wi-Fi ou Bluetooth lorsqu'il se trouve à proximité. Le mode de maillage local de Briar peut être utile lorsque la disponibilité d’internet pose problème.

[:octicons-home-16: Homepage](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://briarproject.org){ .card-link title="Donation options are listed on the bottom of the homepage" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Pour ajouter un contact sur Briar, vous devez d'abord vous ajouter tous les deux. Vous pouvez soit échanger des liens `briar://` soit scanner le QR code d'un contact s'il se trouve à proximité.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit), and the anonymous routing protocol uses the Tor network which has also been audited.

Briar a un [cahier des charges](https://code.briarproject.org/briar/briar-spec) entièrement publié.

Briar prend en charge la confidentialité persistante[^1] en utilisant le protocole [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) et [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) de Bramble.

## Autres options

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Ces messageries instantanées ne disposent pas de la confidentialité persistante[^1] et, bien qu'ils répondent à certains cas d'utilisation que nos recommandations précédentes ne permettent pas, nous ne les recommandons pas pour les communications sensibles ou long terme. Toute compromission de la clé parmi les destinataires du message affecterait la confidentialité de **toutes** les communications passées.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** is the reference [client](https://matrix.org/ecosystem/clients) for the [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im) protocol, an [open standard](https://spec.matrix.org/latest) for secure decentralized real-time communication.

Les messages et les fichiers partagés dans les salons privés (ceux qui nécessitent une invitation) sont par défaut E2EE, tout comme les appels vocaux et vidéo individuels.

[:octicons-home-16: Homepage](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1083446067)
- [:simple-github: GitHub](https://github.com/element-hq/element-android/releases)
- [:fontawesome-brands-windows: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

Les photos de profil, les réactions et les surnoms ne sont pas chiffrés.

Les appels vocaux et vidéo de groupe ne sont [pas](https://github.com/vector-im/element-web/issues/12878) E2EE, et utilisent Jitsi, mais cela devrait changer avec [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401). Les appels de groupe n'ont [pas d'authentification](https://github.com/vector-im/element-web/issues/13074) actuellement, ce qui signifie que les participants ne faisant pas partie de la salle peuvent également se joindre aux appels. Nous vous recommandons de ne pas utiliser cette fonctionnalité pour les réunions privées.

Le protocole Matrix lui-même [prend théoriquement en charge la confidentialité persistante](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], mais elle [n'est pas prise en charge par Element pour le moment](https://github.com/vector-im/element-web/issues/7101) car elle rompt certains aspects de l'expérience utilisateur tels que la sauvegarde des clés et l'historique des messages partagés.

Le protocole a fait l'objet d'un [audit](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) indépendant en 2016. The specification for the Matrix protocol can be found in their [documentation](https://spec.matrix.org/latest). The [Olm cryptographic ratchet](https://matrix.org/docs/matrix-concepts/end-to-end-encryption) used by Matrix is an implementation of Signal’s [Double Ratchet algorithm](https://signal.org/docs/specifications/doubleratchet).

### Session

<div class="admonition recommendation" markdown>

![Logo de Session](assets/img/messengers/session.svg){ align=right }

**Session** est une messagerie décentralisée axée sur les communications privées, sécurisées et anonymes. Session prend en charge les messages directs, les discussions de groupe et les appels vocaux.

Session uses the decentralized [Oxen Service Node Network](https://oxen.io) to store and route messages. Chaque message chiffré est acheminé via trois nœuds dans le Oxen Service Node Network, ce qui rend pratiquement impossible pour les nœuds de compiler des informations significatives sur ceux qui utilisent le réseau.

[:octicons-home-16: Homepage](https://getsession.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:fontawesome-brands-windows: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

Session permet le E2EE dans les chats individuels ou des groupes fermés pouvant compter jusqu'à 100 membres. Les groupes ouverts n'ont aucune restriction sur le nombre de membres, mais sont ouverts par conception.

Session était auparavant basée sur le protocole Signal avant d'être remplacée par son propre protocole en décembre 2020. Le protocole de Session ne prend [pas](https://getsession.org/blog/session-protocol-technical-information) en charge la confidentialité persistante.[^1]

Oxen a demandé un audit indépendant pour Session en mars 2020. L'audit [s'est conclu](https://getsession.org/session-code-audit) en avril 2021 : "Le niveau de sécurité global de cette application est bon et la rend utilisable pour les personnes soucieuses de la protection de leur vie privée."

Session a un [livre blanc](https://arxiv.org/pdf/2002.04609.pdf) décrivant les spécifications techniques de l'application et du protocole.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Dispose de clients open-source.
- Ne nécessite pas le partage d'identifiants personnels (numéros de téléphone ou e-mails spécifiquement) avec les contacts.
- Utilise par défaut E2EE pour les messages privés.
- Prend en charge E2EE pour tous les messages.
- A fait l'objet d'un audit indépendant.

### Dans le meilleur des cas

Nos critères de cas idéal représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de cette fonctionnalité, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Prend en charge la confidentialité persistante[^1]
- Prend en charge la confidentialité future (sécurité post-compromission)[^2]
- Dispose de serveurs open-source.
- Décentralisé, c'est-à-dire [fédéré ou P2P](advanced/communication-network-types.md).
- Utilise E2EE par défaut pour tous les messages.
- Prend en charge Linux, macOS, Windows, Android et iOS.

[^1]: La [confidentialité persistante](https://en.wikipedia.org/wiki/Forward_secrecy) est un système de rotation très fréquente des clés, de sorte que si la clé de chiffrement actuelle est compromise, elle n'expose pas également les messages **antérieurs**.
[^2]: La confidentialité future (ou sécurité post-compromission) est une fonction qui empêche un attaquant de déchiffrer les **futurs** messages après avoir compromis une clé privée, à moins qu'il ne compromette également d'autres clés de session futures. Cela oblige en réalité l'attaquant à intercepter toutes les communications entre les parties, puisqu'il perd l'accès dès qu'un échange de clés non intercepté se produit.
