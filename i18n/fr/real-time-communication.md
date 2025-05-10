---
meta_title: "Les meilleures messageries instantanées privées - Privacy Guides"
title: "Communication en temps réel"
icon: material/chat-processing
description: Encrypted messengers like Signal and SimpleX keep your sensitive communications secure from prying eyes.
cover: real-time-communication.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Attaques passives](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fournisseurs de service](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: Surveillance de masse](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our recommendations for encrypted **real-time communication**. These come in the form of many [types of communication networks](./advanced/communication-network-types.md).

[:material-movie-open-play-outline: Video: It's time to stop using SMS](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why/ ""){.md-button}

## Messageries instantanées chiffrées

Ces messageries sont idéales pour sécuriser vos communications sensibles.

### Signal

<div class="admonition recommendation" markdown>

![Logo de Signal](assets/img/messengers/signal.svg){ align=right }

**Signal** est une application mobile développée par Signal Messenger LLC. The app provides instant messaging and calls secured with the Signal Protocol, an extremely secure encryption protocol which supports forward secrecy[^1] and post-compromise security.[^2]

[:octicons-home-16: Homepage](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-github: GitHub](https://github.com/signalapp/Signal-Android/releases)
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

#### Molly (Android)

If you use Android and your threat model requires protecting against [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} you may consider using this alternative app, which features a number of security and usability improvements, to access the Signal network.

<div class="admonition recommendation" markdown>

![Molly logo](assets/img/messengers/molly.svg){ align=right }

**Molly** is an alternative Signal client for Android which allows you to encrypt the local database with a passphrase at rest, to have unused RAM data securely shredded, to route your connection via Tor, and [more](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features). It also has usability improvements including scheduled backups, automatic locking, [UnifiedPush](https://unifiedpush.org) support, and the ability to use your Android phone as a linked device instead of the primary device for a Signal account.

[:octicons-home-16: Homepage](https://molly.im){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/mollyim/mollyim-android/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mollyim/mollyim-android){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/mollyim){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-fdroid: F-Droid](https://molly.im/fdroid)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/im.molly.app)
- [:simple-github: GitHub](https://github.com/mollyim/mollyim-android/releases)

</details>

</div>

Molly is updated every two weeks to include the latest features and bug fixes from Signal. The exception is security issues, which are patched as soon as possible. That said, you should be aware that there might be a slight delay compared to upstream, which may affect actions such as [migrating from Signal to Molly](https://github.com/mollyim/mollyim-android/wiki/Migrating-From-Signal#migrating-from-signal).

Note that you are trusting multiple parties by using Molly, as you now need to trust the Signal team *and* the Molly team to deliver safe and timely updates.

There is a version of Molly called **Molly-FOSS** which removes proprietary code like the Google services used by both Signal and Molly, at the expense of some features like battery-saving push notifications via Google Play Services. You can regain push notifications without Google Play Services in either version of Molly with [UnifiedPush](https://unifiedpush.org), but it requires running a separate program called [Mollysocket](https://github.com/mollyim/mollysocket) on another device to function. Mollysocket can either be self-hosted on a separate computer or server (VPS), or alternatively a public Mollysocket instance can be used ([step-by-step tutorial, in German](https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy)).

All versions of Molly provide the same security improvements.

Molly and Molly-FOSS support [reproducible builds](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds), meaning it's possible to confirm that the compiled APKs match the source code.

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX Chat** is an instant messenger that doesn't depend on any unique identifiers such as phone numbers or usernames. Its decentralized network makes SimpleX Chat an effective tool against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplex.chat/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://simplex.chat/docs/simplex.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Source Code" }

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

SimpleX provides direct messaging, group chats, and E2EE calls secured with the [SimpleX Messaging Protocol](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md), which uses double ratchet encryption with quantum resistance. Additionally, SimpleX Chat provides metadata protection by using unidirectional ["simplex queues"](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md#simplex-queue) to deliver messages.

To participate in conversations on SimpleX Chat, you must scan a QR code or click an invite link. This allows you to verify a contact out-of-band, which protects against man-in-the-middle attacks by network providers. Your data can be exported and imported onto another device, as there are no central servers where this is backed up.

You can find a full list of the privacy and security [features](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations) implemented in SimpleX Chat on the app's repository.

SimpleX Chat was independently audited in [July 2024](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits) and in [October 2022](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website).

### Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works) to other clients using the Tor Network, making it an effective tool at circumventing [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar peut également se connecter par Wi-Fi ou Bluetooth lorsqu'il se trouve à proximité. Le mode de maillage local de Briar peut être utile lorsque la disponibilité d’internet pose problème.

[:octicons-home-16: Homepage](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title="Documentation" }
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

To add a contact on Briar, you must both add each other first. You can either exchange `briar://` links or scan a contact’s QR code if they are nearby.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit), and the anonymous routing protocol uses the Tor network which has also been audited.

Briar has a fully [published specification](https://code.briarproject.org/briar/briar-spec).

Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## Autres options

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Ces messageries instantanées ne disposent pas de la confidentialité persistante[^1] et, bien qu'ils répondent à certains cas d'utilisation que nos recommandations précédentes ne permettent pas, nous ne les recommandons pas pour les communications sensibles ou long terme. Toute compromission de la clé parmi les destinataires du message affecterait la confidentialité de **toutes** les communications passées.

</div>

### Session

<div class="admonition recommendation" markdown>

![Logo de Session](assets/img/messengers/session.svg){ align=right }

**Session** est une messagerie décentralisée axée sur les communications privées, sécurisées et anonymes. Session prend en charge les messages directs, les discussions de groupe et les appels vocaux.

Session uses the decentralized [Oxen Service Node Network](https://oxen.io) to store and route messages. Chaque message chiffré est acheminé via trois nœuds dans le Oxen Service Node Network, ce qui rend pratiquement impossible pour les nœuds de compiler des informations significatives sur ceux qui utilisent le réseau.

[:octicons-home-16: Homepage](https://getsession.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title="Documentation" }
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

Session allows for E2EE in one-on-one chats or closed groups which allow for up to 100 members. It is also possible to [set up](https://docs.oxen.io/oxen-docs/products-built-on-oxen/session/guides/open-group-setup) or join open groups which can host thousands of members, but messages in these open groups are **not** end-to-end encrypted between participants.

Session was previously based on Signal Protocol before replacing it with their own in December 2020. Session Protocol does [not](https://getsession.org/blog/session-protocol-technical-information) support forward secrecy.[^1]

Oxen requested an independent audit for Session in March 2020. The audit [concluded](https://getsession.org/session-code-audit) in April 2021:

> The overall security level of this application is good and makes it usable for privacy-concerned people.

Session has a [white paper](https://arxiv.org/pdf/2002.04609.pdf) describing the technical details of the app and protocol.

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

- Supports forward secrecy[^1]
- Prend en charge la confidentialité future (sécurité post-compromission)[^2]
- Dispose de serveurs open-source.
- Décentralisé, c'est-à-dire [fédéré ou P2P](advanced/communication-network-types.md).
- Utilise E2EE par défaut pour tous les messages.
- Prend en charge Linux, macOS, Windows, Android et iOS.

[^1]: [Forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: La confidentialité future (ou sécurité post-compromission) est une fonction qui empêche un attaquant de déchiffrer les **futurs** messages après avoir compromis une clé privée, à moins qu'il ne compromette également d'autres clés de session futures. Cela oblige en réalité l'attaquant à intercepter toutes les communications entre les parties, puisqu'il perd l'accès dès qu'un échange de clés non intercepté se produit.
