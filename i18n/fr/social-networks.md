---
title: Réseaux sociaux
icon: material/account-supervisor-circle-outline
description: Trouvez un nouveau réseau social qui ne fouille pas dans vos données et qui ne monétise pas votre profil.
cover: social-networks.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-close-outline: Censure](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }
- [:material-account-cash: Capitalisme de Surveillance](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Ces **réseaux sociaux** respectueux de la vie privée vous permettent de participer à des communautés en ligne sans donner votre nom complet, votre numéro de téléphone ou autre informations personnelles habituellement demandées par les entreprises de la tech.

La censure de deux manières différentes est un problème grandissant sur les plateformes de réseaux sociaux. Premièrement, les entreprises accèdent généralement à des demandes illégitimes de censure, que ce soit de la part de gouvernements ou selon leur propres politiques internes. Deuxièmement, elles exigent généralement de créer un compte pour accéder à du contenu cloisonné qui serait normalement accessibles à tous sur l'Internet ouvert ; ces pratiques ont pour effet de censurer dans les faits les recherches des utilisateurs soucieux de leur vie privée qui ne souhaitent pas payer le prix de leur confidentialité pour créer un compte sur ces réseaux.

Les réseaux sociaux que nous recommandons permettent de contourner la censure en fonctionnant sur un protocole ouvert et décentralisé. Ils permettent également de visualiser le contenu public sans créer de compte.

Gardez à l'esprit qu'**aucun** réseau social n'est adapté aux communications privées et sensibles. Pour communiquer directement avec d'autres personnes, nous vous recommandons d'utiliser un service de [messagerie instantanée](real-time-communication.md) avec un chiffrement de bout-en-bout robuste et de n'utiliser les messages privés sur les réseaux sociaux que dans le but de convenir d'une plateforme sécurisée à utiliser avec vos contacts.

## Décentralisation

Les réseaux sociaux décentralisés sont basés sur une architecture fondamentalement différente des réseaux sociaux conventionnels, mais assez similaire à la structure sous-jacente des emails. Au lieu de créer un compte sur un service unique comme vous le feriez pour Facebook ou Discord, vous devez à la place choisir un serveur public et indépendant à rejoindre. Le serveur que vous choisissez de rejoindre peut découvrir et communiquer avec les autres serveurs ; cet aspect de la décentralisation s'appelle la _fédération_.

Un des gros avantages de ce modèle décentralisé est qu'il n'y a aucune autorité centrale qui peut censurer votre compte sur l'entièreté du réseau, bien qu'il soit possible que votre compte soit banni ou mis en sourdine par un serveur individuel.

L'inconvénient de ce modèle décentralisé est que chaque serveur est sa propre entité, avec sa propre politique de confidentialité, ses propres conditions d'utilisation et sa propre équipe d'administration et de modérateurs. Bien que beaucoup de ces serveurs soient beaucoup _moins_ restrictifs et plus respectueux de la vie privée que les plateformes traditionnelles de réseaux sociaux, certains peuvent être _plus_ restrictifs ou potentiellement _pire_ en termes de confidentialité. Généralement, le logiciel utilisé par ces réseaux sociaux ne fait pas de différence entre ces administrateurs et ne limite pas leur pouvoirs.

## Résistance à la censure

Bien que la censure ne soit pas présente au niveau du réseau entier pour un réseau social décentralisé, vous pouvez malgré tout en être victime au niveau du serveur, selon l'administrateur de ce serveur. Les administrateurs peuvent _défédérer_ d'autres serveurs, ce qui peut limiter le contenu que vous voyez et les personnes avec qui vous interagissez.

Si vous êtes particulièrement inquiet concernant un serveur spécifique qui censure votre contenu, le contenu que vous pouvez voir, ou qui est visible aux autres serveurs, vous avez généralement deux options :

1. **Héberger vous-même le logiciel du réseau social.** Cette approche vous donne exactement la même résistance à la censure que n'importe quel autre site web que vous hébergez vous-même, c'est-à-dire assez élevée.

2. **Utiliser un service d'hébergement géré.** Nous n'avons pas de recommandations particulières, mais il existe un certain nombre de services d'hébergement qui vous permettent de créer un tout nouveau serveur sur votre propre nom de domaine (ou sur un sous-domaine de leur domaine, mais nous ne vous recommandons pas cette option à moins que l'enregistrement de votre propre domaine ne représente une charge trop élevée sur votre confidentialité).

   Généralement, les fournisseurs d'hébergement s'occuperont de la partie _technique_ sur serveur, mais vous laisserons totalement gérer la partie _modération_. Cela peut être une approche plus intéressante que l'auto-hébergement pour la plupart des gens puisque vous pouvez bénéficier d'un grand contrôle sur votre serveur sans vous préoccuper des problèmes techniques ou des failles de sécurité.

   Vous devriez consulter minutieusement les conditions d'utilisation et les politiques d'utilisation acceptable avant de choisir un fournisseur d'hébergement. Elles laissent généralement plus de possibilités qu'un serveur hébergé classique, et sont moins susceptible d'être appliquées sans une demande, mais peuvent tout de même être restrictives de manière indésirable.

## Mastodon

<div class="admonition recommendation" markdown>

![Logo de Mastodon](assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** est un réseau social basé sur des protocoles open web et un logiciel libre et open-source. Il utilise un protocole décentralisé comme les emails, **:simple-activitypub: ActivityPub** : les utilisateurs peuvent exister sur différents serveurs ou différentes plateformes mais peuvent quand même communiquer entre eux.

[:octicons-home-16: Page d'Accueil](https://joinmastodon.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.joinmastodon.org){ .card-link title="Documentation" }

</div>

Il existe de nombreuses plateformes logiciel qui utilisent ActivityPub en tant que protocole dorsal (backend) de réseau social, ce qui signifie qu'elles peuvent communiquer entre elles même si elles utilisent un logiciel différent. Par exemple, PeerTube est un logiciel de publication de vidéo qui utilise ActivityPub, ce qui signifie que vous pouvez suivre des chaînes PeerTube soit avec un compte PeerTube, _soit_ avec un compte Mastodon car celui-ci utilise aussi ActivityPub.

Nous avons choisi de recommander Mastodon en tant que plateforme principale de réseaux sociaux plutôt que d'autre logiciel ActivityPub pour les raisons suivantes :

1. Mastodon a un historique solide de mises à jour de sécurité. Dans les rares cas où des failles de sécurité majeures ont été détectées, ils ont rapidement et efficacement publié les correctifs. Historiquement, ces correctifs de sécurité ont également été rétroportés dans les branches les plus anciennes. Cela peut rendre la tâche plus facile aux hébergeurs les moins expérimentés qui peuvent ne pas être à l'aise à l'idée de mettre immédiatement à jour leurs instances. Mastodon propose également un système de notifications de mise à jour intégré à leur interface web, augmentant ainsi les chances que les administrateurs des serveurs soient au courant des correctifs de sécurité disponibles pour leurs instances.

2. Mastodon convient à la plupart des types de contenus. Bien que ce soit avant tout une plateforme de microblog, Mastodon prend très bien en charge les posts plus longs, les images, les vidéos et la plupart des autres posts que vous êtes susceptible de rencontrer si vous suivez des utilisateurs qui ne sont pas sur Mastodon. Grâce à cela, vous pouvez utiliser Mastodon comme "hub central" pour vos abonnements, peu importe la plateforme qu'ils utilisent. En comparaison, si vous utilisez uniquement un compte PeerTube, vous ne pourrez suivre _que_ d'autres chaines de vidéos.

3. Mastodon dispose de contrôles assez complets en matière de protection de la vie privée. Vous pouvez limiter comment et quand sont utilisées vos données grâce à des fonctionnalités intégrées, dont certaines que nous allons aborder ci-dessous. Ils développent également de nouvelles fonctionnalités en tenant compte de la protection de la vie privée. Par exemple, alors que d'autres logiciels ActivityPub ont rapidement mis en place des "citations de post" en gérant simplement les liens vers d'autres posts avec un modal d'intégration légèrement différent, Mastodon [développe](https://blog.joinmastodon.org/2025/02/bringing-quote-posts-to-mastodon) une fonction de citation de post qui vous permettra de contrôler plus précisément les citations de vos posts.

### Choisir une instance

Afin de bénéficier un maximum de Mastodon, il est très important de choisir un serveur, ou "instance", en lien avec le type de contenu que vous souhaitez publier ou consulter. Pour le moment nous ne recommandons pas d'instance spécifique, mais vous pouvez demander de l'aide au sein de notre communauté. Nous vous recommandons cependant d'éviter d'utiliser _mastodon.social_ ou _mastodon.online_ car ces instances sont contrôlées par la même entreprise qui développe Mastodon. Du point de vue de la décentralisation, il est préférable au long terme de séparer les développeurs d'un logiciel et les hébergeurs de serveur afin qu'aucune des parties ne puisse exercer un trop grand contrôle sur le réseau entier.

### Paramètres de confidentialité recommandés

Depuis l'interface web de Mastodon, cliquez sur le lien **Administration** dans la barre latérale droite. Dans le panneau de contrôle de d'administration, vous trouverez ces sections dans la barre latérale gauche :

#### Profile public

Ici, vous trouverez un certain nombre de réglages de confidentialité dans l'onglet **confidentialité et visibilité** (**privacy and reach**). Il convient notamment de prêter attention à ces éléments :

- [ ] **Accepter automatique de nouveaux followers**. Décochez cette case si vous souhaitez maintenir votre compte privé. Cela vous permettra de passer en revue les personnes qui souhaitent suivre votre compte avant de les accepter.

  Contrairement à la plupart des plateformes de réseaux sociaux, si votre profil est privé vous toujours la _possibilité_ de publier des posts (appelés _pouets_) visible publiquement par les personnes qui ne vous suivent pas et qui peuvent également être partagés par des non-abonnés. Désactiver ce paramètre est le seul moyen d'avoir le _choix_ de publier des posts visibles du monde entier ou d'un groupe de personnes choisies.

- [ ] **Montrer les abonnements et les abonnés sur le profil**. Décocher cette case pour cacher au public votre cercle social. Il est assez rare que la liste des personnes que vous suivez présente un intérêt réel pour les autres, mais ces informations peuvent présenter un risque pour vous.

- [ ] **Afficher l'application que vous utilisez pour envoyer un pouet**. Décochez cette case pour éviter de révéler inutilement des informations sur votre configuration informatique personnelle.

Les autres paramètres de confidentialité sur cette page devraient être passés en revue, cependant ceux-ci ne sont **pas** des paramètres techniques mais des simples demandes. Par exemple, si vous choisissez sur cette page de cacher votre profil des moteurs de recherche, **rien** n'empêchera un moteur de recherche de lire votre profil. Vous demandez simplement aux index des moteurs de recherche de ne pas partager votre contenu à leurs utilisateurs.

Vous devriez malgré tout faire ces demandes car elles peuvent vous aider à réduire simplement votre empreinte numérique. Cependant, vous de ne devriez pas _compter dessus_. La seule façon efficace de cacher vos pouets des moteurs de recherche est de paramètre leur visibilité sur non-public (abonnés uniquement) _et_ de limiter qui peut suivre votre compte.

#### Préférences

Vous devriez configurer vos paramètres de **confidentialité des pouets** sur : **Privé - Visible uniquement des abonnés**.

Ce paramètre change uniquement vos réglages par défaut pour éviter les erreurs. Vous pouvez toujours ajuster le niveau de visibilité lorsque vous écrivez un nouveau pouet.

#### Suppression automatique des pouets

- [x] Cochez la case **Supprimer automatiquement les vieux pouets**.

Les paramètres par défaut de cette option sont correctes, les pouets que vous publiez seront supprimés après 2 semaines, à mois que vous ne les mettiez en favoris (étoile). Cela vous permet de contrôler facilement quels posts sont permanents ou éphémères. De nombreux paramètres concernant la durée et le moment de conservation des messages peuvent toutefois être ajustés ici pour répondre à vos propres besoins.

Il est assez rare que des posts plus vieux que quelques semaines soient lus ou pertinents. Ces anciens messages sont souvent ignorés parce qu'ils sont difficiles à traiter en masse, mais ils peuvent constituer un profil assez complet sur vous au fil du temps. Vous devriez toujours vous efforcer de publier du contenu éphémère par défaut, et ne conserver les articles plus longtemps que de manière très intentionnelle.

### Poster du contenu

Lorsque vous écrivez un pouet, vous aurez la possibilité de choisir parmi les paramètres de visibilité suivants :

- **Public**, which publishes your content to anyone on the internet.
- **Quiet public**, which you should consider equivalent to publicly posting! This is not a technical guarantee, but merely a request you are making to other servers to hide your post from some feeds.
- **Followers**, which publishes your content only to your followers. If you did not follow our recommendation of restricting your followers, you should consider this equivalent to publicly posting!
- **Specific people**, which only shares the post with people who are specifically mentioned within the post. This is Mastodon's version of direct messages, but should never be relied on for private communications as we covered earlier since Mastodon has no E2EE.

If you used our recommended configuration settings above, you should be posting to **Followers** by default, and only posting to **Public** on an intentional and case-by-case basis.

## Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/social-networks/element.svg){ align=right }

**Element** is the flagship client for the **:simple-matrix: [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im)** protocol, an [open standard](https://spec.matrix.org/latest) that enables decentralized communication by way of federated chat rooms. Users can exist on different homeservers but still communicate with each other.

[:octicons-home-16: Homepage](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

<details class="downloads" markdown><summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1083446067)
- [:simple-github: GitHub](https://github.com/element-hq/element-android/releases)
- [:fontawesome-brands-windows: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-browser-16: Web](https://app.element.io)

</details>

</div>

### Choosing a Homeserver

To benefit the most from Matrix, it is critical to choose a homeserver which is well aligned with the subject(s) you want to chat about. We do not currently recommend any specific homeservers, but you may find advice within our communities or third-party resources like [_joinmatrix.org_](https://servers.joinmatrix.org). We recommend avoiding _matrix.org_ because they are operated by the same company which develops Matrix itself. Du point de vue de la décentralisation, il est préférable au long terme de séparer les développeurs d'un logiciel et les hébergeurs de serveur afin qu'aucune des parties ne puisse exercer un trop grand contrôle sur le réseau entier.

### Paramètres de confidentialité recommandés

From Element's web or desktop app, go to :gear: → **All settings** to find these sections:

#### Sessions

By default, when you log in to Element on a new device, the session name will be automatically populated with the Matrix client and platform you used for login. This information may be visible to other users depending on the Matrix client they use.

To prevent revealing information about your personal device to others unnecessarily, consider emptying the session name; this will change the session name to the randomly generated alphanumeric Session ID instead.

#### Préférences

- [ ] Décochez **Envoyer des accusés de réception**
- [ ] Uncheck **Send typing notifications**

You should uncheck these options to reduce the exposure of metadata to other users when chatting in a public room.

#### Voice & Video

- [ ] Uncheck **Allow Peer-to-Peer for 1:1 calls**
- [ ] Uncheck **Allow fallback call assist server (turn.matrix.org)**

If you do decide to use Element for one-to-one communication, we recommend unchecking these settings to prevent the exposure of your IP address to the other party.

#### Security & Privacy

##### Manage integrations (scalar.vector.im)

A Matrix integration manager connects Matrix to third-party services such as bots, bridges, and other enhancements. Element collects information to provide these services to those using an integration manager; you can review its detailed [Privacy Notice](https://element.io/integration-manager-privacy-notice) for the exact information Element collects and the ways it uses such information.

As an end user on a public homeserver, you can consider unchecking the **Enable the integration manager** option, which does not affect the visibility of bots or other third-party services. As a homeserver administrator, consider whether the additional parties with which you share your data are worth the extra functionality.

##### Sessions

- [ ] (Optional) Uncheck **Record the client name, version, and url to recognize sessions for easily in session manager**

Unchecking this option may make it more diffcult to discern your active sessions if you logged in to your Matrix account on multiple devices.

#### Chiffrement

- [x] (Optional) Check **In encrypted rooms, only send messages to verified users**

With this setting enabled, unverified users (i.e., those who have not used the **Verify User** function) and unverified devices of verified users will not receive your messages in a room with encryption enabled. This may limit the messages you can view and the people you can interact with.

## Critères

**Nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de nos [critères de base](about/criteria.md), nous avons élaboré un ensemble d'exigences clair nous permettant de proposer des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de faire votre choix, et de mener vos propres recherches pour vous assurer que celui-ci correspond bien à vos besoins.

- Must be free and open-source software.
- Must use a federated protocol to communicate with other instances of the social networking software.
- Must not have non-technical restrictions on who can be federated with.
- Must be usable within a standard [web browser](desktop-browsers.md).
- Must make public content accessible to visitors without an account.
- Must allow you to limit who can follow your profile.
- Must allow you to post content visible only to your followers.
- Must support modern web application security standards/features (including [multifactor authentication](multi-factor-authentication.md)).
