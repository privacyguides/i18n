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

La censure est un problème grandissant sur les plateformes de réseaux sociaux qui se produit de deux manières différentes. Premièrement, les entreprises accèdent généralement à des demandes illégitimes de censure, que ce soit de la part de gouvernements ou selon leurs propres politiques internes. Deuxièmement, elles exigent généralement de créer un compte pour accéder à du contenu cloisonné qui serait normalement accessibles à tous sur l'Internet ouvert ; ces pratiques ont pour effet de censurer dans les faits les recherches des utilisateurs soucieux de leur vie privée qui ne souhaitent pas payer le prix de leur confidentialité pour créer un compte sur ces réseaux.

Les réseaux sociaux que nous recommandons permettent de contourner la censure en fonctionnant sur un protocole ouvert et décentralisé. Ils ne nécessitent pas non plus de créer un compte pour simplement voir du contenu accessible au public.

Gardez à l'esprit qu'**aucun** réseau social n'est adapté aux communications privées et sensibles. Pour communiquer directement avec d'autres personnes, nous vous recommandons d'utiliser un service de [messagerie instantanée](real-time-communication.md) avec un chiffrement de bout-en-bout robuste et de n'utiliser les messages privés sur les réseaux sociaux que dans le but de convenir d'une plateforme sécurisée à utiliser avec vos contacts.

## Décentralisation

Les réseaux sociaux décentralisés sont basés sur une architecture fondamentalement différente des réseaux sociaux conventionnels, mais assez similaire à la structure sous-jacente des emails. Au lieu de créer un compte sur un service unique comme vous le feriez pour Facebook ou Discord, vous devez à la place choisir le serveur public et indépendant (appelé généralement instance ou "homeserver") que vous souhaitez rejoindre. Le serveur que vous choisissez de rejoindre peut découvrir et communiquer avec les autres serveurs ; cet aspect de la décentralisation s'appelle la _fédération_.

Un des gros avantages de ce modèle décentralisé est qu'il n'y a aucune autorité centrale qui peut censurer votre compte sur l'entièreté du réseau, bien qu'il soit possible que votre compte soit banni ou mis en sourdine par un serveur individuel.

Il est cependant important de rester attentif car chaque serveur est sa propre entité, avec sa propre politique de confidentialité, ses propres conditions d'utilisation et sa propre équipe d'administration et de modérateurs. Bien que beaucoup de ces serveurs soient beaucoup _moins_ restrictifs et plus respectueux de la vie privée que les plateformes traditionnelles de réseaux sociaux, certains peuvent être _plus_ restrictifs ou potentiellement _pire_ en termes de confidentialité. Généralement, le logiciel utilisé par ces réseaux sociaux ne fait pas de différence entre les administrateurs et ne limite pas leurs pouvoirs.

## Résistance à la censure

Bien que la censure ne soit pas présente au niveau du réseau entier pour un réseau social décentralisé, vous pouvez malgré tout en être victime au niveau du serveur, selon son administrateur. Les administrateurs peuvent _défédérer_ d'autres serveurs, ce qui peut limiter le contenu que vous voyez et les personnes avec qui vous interagissez.

Si vous êtes particulièrement inquiet concernant un serveur spécifique qui censure votre contenu, le contenu que vous pouvez voir, ou ce qui est visible aux autres serveurs, vous avez généralement deux options :

1. **Héberger vous-même le logiciel du réseau social.** Cette approche vous donne exactement la même résistance à la censure que n'importe quel autre site web que vous hébergez vous-même, c'est-à-dire assez élevée.

2. **Utiliser un service d'hébergement géré.** Nous n'avons pas de recommandations particulières, mais il existe un certain nombre de services d'hébergement qui vous permettent de créer un tout nouveau serveur sur votre propre nom de domaine (ou sur un sous-domaine de leur domaine, mais nous ne vous recommandons pas cette option à moins que l'enregistrement de votre propre domaine ne représente une charge trop élevée sur votre confidentialité).

   Généralement, les fournisseurs d'hébergement s'occuperont de la partie _technique_ sur serveur, mais vous laisserons totalement gérer la partie _modération_. Cela peut être une approche plus intéressante que l'auto-hébergement pour la plupart des gens puisque vous pouvez bénéficier d'un grand contrôle sur votre serveur sans vous préoccuper des problèmes techniques ou des failles de sécurité.

   Vous devriez consulter minutieusement les conditions d'utilisation et les politiques d'utilisation acceptable avant de choisir un fournisseur d'hébergement. Celles-ci laissent généralement plus de possibilités qu'un serveur hébergé classique, et sont moins susceptible d'être appliquées sans une demande explicite, mais peuvent tout de même être restrictives de façon indésirable.

## Mastodon

<div class="admonition recommendation" markdown>

![Logo de Mastodon](assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** est un réseau social basé sur des protocoles open web et un logiciel libre et open-source. Il utilise un protocole décentralisé comme les emails, **:simple-activitypub: ActivityPub** : les utilisateurs peuvent exister sur différents serveurs ou différentes plateformes mais peuvent quand même communiquer entre eux.

[:octicons-home-16: Page d'Accueil](https://joinmastodon.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.joinmastodon.org){ .card-link title="Documentation" }

</div>

Il existe de nombreuses plateformes logiciel qui utilisent ActivityPub en tant que protocole dorsal (backend) de réseau social, ce qui signifie qu'elles peuvent communiquer entre elles même si elles utilisent un logiciel différent. Par exemple, PeerTube est un logiciel de publication de vidéo qui utilise ActivityPub, ce qui signifie que vous pouvez suivre des chaînes PeerTube avec un compte PeerTube, _et_ avec un compte Mastodon car celui-ci utilise aussi ActivityPub.

Nous avons choisi de recommander Mastodon en tant que plateforme principale de réseaux sociaux plutôt que d'autre logiciel ActivityPub pour les raisons suivantes :

1. Mastodon a un historique solide de mises à jour de sécurité. Dans les rares cas où des failles de sécurité majeures ont été détectées, ils ont rapidement et efficacement publié les correctifs. Historiquement, ces correctifs de sécurité ont également été rétroportés sur des branches de fonctionnalité plus anciennes. Cela peut rendre la tâche plus facile aux hébergeurs les moins expérimentés qui peuvent ne pas être à l'aise à l'idée de mettre immédiatement à jour leurs instances. Mastodon propose également un système de notifications de mise à jour intégré à leur interface web, augmentant ainsi les chances que les administrateurs des serveurs soient au courant des correctifs de sécurité disponibles pour leurs instances.

2. Mastodon convient à la plupart des types de contenus. Bien que ce soit avant tout une plateforme de microblog, Mastodon prend très bien en charge les posts plus longs, les images, les vidéos et la plupart des autres posts que vous êtes susceptible de rencontrer si vous suivez des utilisateurs qui ne sont pas sur Mastodon. Grâce à cela, vous pouvez utiliser Mastodon comme "hub central" pour vos abonnements, peu importe la plateforme qu'ils utilisent. En comparaison, si vous utilisez uniquement un compte PeerTube, vous ne pourrez suivre _que_ d'autres chaines de vidéos.

3. Mastodon dispose de contrôles assez complets en matière de protection de la vie privée. Vous pouvez limiter comment et quand sont utilisées vos données grâce à des fonctionnalités intégrées, dont certaines que nous allons aborder ci-dessous. Ils développent également de nouvelles fonctionnalités en tenant compte de la protection de la vie privée. Par exemple, alors que d'autres logiciels ActivityPub ont rapidement mis en place des "citations de post" en gérant simplement les liens vers d'autres posts avec un modal d'intégration légèrement différent, Mastodon [développe](https://blog.joinmastodon.org/2025/02/bringing-quote-posts-to-mastodon) une fonction de citation de post qui vous permettra de contrôler plus précisément les citations de vos posts.

### Choisir une instance

Afin de bénéficier un maximum de Mastodon, il est très important de choisir un serveur, ou "instance", en lien avec le type de contenu que vous souhaitez publier ou consulter. Pour le moment nous ne recommandons pas d'instance spécifique, mais vous pouvez demander de l'aide au sein de notre communauté. Nous vous recommandons cependant d'éviter d'utiliser _mastodon.social_ ou _mastodon.online_ car ces instances sont contrôlées par la même entreprise qui développe Mastodon. Du point de vue de la décentralisation, il est préférable au long terme de séparer les développeurs d'un logiciel et les hébergeurs de serveur afin qu'aucune des parties ne puisse exercer un trop grand contrôle sur le réseau entier.

### Paramètres de confidentialité recommandés

Depuis l'interface web de Mastodon, cliquez sur **Préférences** dans la barre latérale droite. Dans le panneau de contrôle de d'administration, vous trouverez ces sections dans la barre latérale gauche :

#### Profil

Ici, vous trouverez un certain nombre de réglages de confidentialité dans l'onglet **Vie privée et visibilité**. Il convient notamment de prêter attention à ces éléments :

- [ ] **Accepter automatiquement de nouveaux abonnés**. Décochez cette case si vous souhaitez maintenir votre compte privé. Cela vous permettra de passer en revue les personnes qui souhaitent suivre votre compte avant de les accepter.

  Contrairement à la plupart des plateformes de réseaux sociaux, si votre profil est privé vous toujours la _possibilité_ de publier des posts (appelés _pouets_) visible publiquement par les personnes qui ne vous suivent pas et qui peuvent également être partagés par des non-abonnés. Désactiver ce paramètre est le seul moyen d'avoir le _choix_ de publier des posts visibles du monde entier ou d'un groupe de personnes choisies.

- [ ] **Afficher les profils abonnés et suivis sur le profil**. Décocher cette case pour cacher au public votre cercle social. Il est assez rare que la liste des personnes que vous suivez présente un intérêt réel pour les autres, mais ces informations peuvent présenter un risque pour vous.

- [ ] **Afficher l'application que vous utilisez pour envoyer un message**. Décochez cette case pour éviter de révéler inutilement des informations sur votre configuration informatique personnelle.

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

- **Public** : visible par n'importe qui sur internet.
- **Non-listé** : équivalent à l'option Public ! Ne représente pas une garantie technique, simplement une demande que vous faites aux autres serveurs de cacher vos pouets.
- **Privé** : visible uniquement par vos abonnés. Si vous n'avez pas modifier vos paramètres de restriction de vos abonnés, considérez le comme équivalent à l'option Public !
- **Direct** : visible uniquement par les personnes que vous mentionnez dans le pouet. C'est la version de Mastodon des messages privés/directs, mais vous ne devriez jamais l'utiliser pour des conversations privées ou sensibles car Mastodon ne propose pas de chiffrement de bout-en-bout, comme nous l'avons mentionné plus haut.

Si vous avez modifié vos paramètres selon nos recommandations, vos pouets devraient être réglés par défaut sur **Privé** et vous ne devriez utiliser **Public** que de façon réfléchie et intentionnelle.

## Element

<div class="admonition recommendation" markdown>

![Logo de Element](assets/img/social-networks/element.svg){ align=right }

**Element** est le client phare du protocole **:simple-matrix: [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im)**, un [format ouvert](https://spec.matrix.org/latest) qui permet une communication décentralisée grâce à des groupes de discussion fédérés. Les utilisateurs peuvent communiquer entre eux même si leurs comptes sont sur des instances (homeservers) différentes.

[:octicons-home-16: Page d'Accueil](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://element.io/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Code Source" }

<details class="downloads" markdown><summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1083446067)
- [:simple-github: GitHub](https://github.com/element-hq/element-android/releases)
- [:fontawesome-brands-windows: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-browser-16: Web](https://app.element.io)

</details>

</div>

### Choisir une instance (homeserver)

Afin de profiter un maximum de Matrix, il est important de choisir une instance (serveur que vous choisissez à la création de votre compte, aussi appelé "homeserver"), qui correspond aux sujets sur lesquels vous souhaitez discuter. Nous ne recommandons pas d'instance particulière pour le moment, mais vous pouvez demander conseil dans nos communautés ou utiliser des ressources comme [_joinmatrix.org_](https://servers.joinmatrix.org). Nous vous recommandons d'éviter _matrix.org_ car cette instance est contrôlée par l'équipe de développement de Matrix. Du point de vue de la décentralisation, il est préférable au long terme de séparer les développeurs d'un logiciel et les hébergeurs de serveur afin qu'aucune des parties ne puisse exercer un trop grand contrôle sur le réseau entier.

### Paramètres de confidentialité recommandés

Depuis l'interface web ou bureau, allez à :gear: → **Tous les paramètres** pour trouver les sections suivantes :

#### Sessions

Par défaut, lorsque vous vous connectez à Element sur un nouvel appareil, le nom de la session sera automatiquement complété par le client Matrix et la plateforme que vous avez utilisés pour vous connecter. Cette information peut être visible par d'autres utilisateurs selon le client Matrix qu'ils utilisent.

Pour éviter de divulguer inutilement des informations sur votre appareil personnel, nous vous conseillons de vider le nom de session ; cela changera le nom de session en un ID de Session alphanumérique généré aléatoirement.

#### Préférences

- [ ] Décochez **Envoyer les accusés de réception**
- [ ] Décochez **Envoyer des notifications de saisie**

Vous devriez décocher ces options pour réduire les métadonnées visibles aux autres utilisateurs lorsque vous discutez dans un salon public.

#### Audio et Vidéo

- [ ] Décochez **Autoriser le pair-à-pair pour les appels en face à face**
- [ ] Décochez **Autoriser le serveur de secours d’assistance d’appel (turn.matrix.org)**

Si vous décidez d'utiliser Element pour vos communications en face à face, nous vous conseillons de désactiver ces paramètres pour éviter d'exposer votre adresse IP à l'autre personne.

#### Sécurité et vie privée

##### Gérer les intégrations (scalar.vector.im)

Un gestionnaire d'intégration Matrix connecte Matrix à des services extérieurs comme des bots, des ponts et d'autres améliorations. Element collecte des informations pour fournir ces services à ceux qui utilisent un gestionnaire d'intégration ; vous pouvez consulter leur [Politique de Confidentialité](https://element.io/integration-manager-privacy-notice) pour connaitre les informations exactes collectées par Element et comment celle-ci sont traitées.

En tant qu'utilisateur final d'une instance publique, vous pouvez décocher l'option **Activer le gestionnaire d'intégration** car elle n'influence pas la visibilité des bots ou autres services extérieurs. En tant qu'administrateur d'une instance, assurez-vous que les fonctionnalités supplémentaires proposées par des services extérieurs valent la peine de leur envoyer vos données.

##### Sessions

- [ ] (Optionnel) Décochez **Enregistrez le nom, la version et l'URL du client afin de reconnaitre les sessions plus facilement dans le gestionnaire de sessions**

Désactiver cette option peut rendre plus difficile de reconnaitre vos sessions actives si vous vous êtes connectés sur plusieurs appareils.

#### Chiffrement

- [x] (Optionnel) Cochez **Dans les salons chiffrés, envoyez des messages uniquement aux utilisateurs vérifiés**

Lorsque vous activez ce paramètre, les utilisateurs qui n'ont pas utilisé la fonctionnalité **Utilisateur Vérifié** et les appareils non vérifiés des utilisateurs vérifiés ne recevrons pas vos messages dans un salon chiffré. Vous pouvez limiter les messages que vous pouvez voir et les personnes avec qui vous interagissez.

## Critères

**Nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de nos [critères de base](about/criteria.md), nous avons élaboré un ensemble d'exigences clair nous permettant de proposer des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de faire votre choix, et de mener vos propres recherches pour vous assurer que celui-ci correspond bien à vos besoins.

- Doit être un logiciel libre et open-source.
- Doit utiliser un protocole fédératif pour communiquer avec les autres instances du logiciel de réseau social.
- Ne doit pas comporter de restrictions non techniques quant aux personnes avec lesquelles il est possible de se fédérer.
- Doit être utilisable dans un [navigateur standard](desktop-browsers.md).
- Doit rendre accessible le contenu public sans avoir à créer de compte.
- Doit permettre de limiter qui peut suivre votre profil.
- Doit vous permettre de poster du contenu visible uniquement à vos abonnés.
- Doit prendre en charge les standards et les fonctionnalités modernes de sécurité des application web (y compris [l'authentification multifactorielle](multi-factor-authentication.md)).
