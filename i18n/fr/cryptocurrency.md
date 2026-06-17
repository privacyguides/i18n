---
meta_title: "Chaînes de blocs de crypto-monnaies privées - Privacy Guides"
description: Contrairement à la plupart des cryptomonnaies, celles-ci offrent la confidentialité des transactions par défaut. Pour cacher les détails des transactions, nous recommandons surtout Monero.
title: Crypto-monnaie
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-eye-outline: Surveillance de masse](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censure](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

Effectuer des paiements en ligne est l'un des plus grands défis en matière de protection de la vie privée. Ces crypto-monnaies garantissent par défaut la confidentialité des transactions (ce qui n'est **pas** garanti par la majorité des crypto-monnaies), à condition que vous ayez une bonne compréhension de la façon d'effectuer des paiements privés de manière efficace. Nous vous encourageons vivement à lire notre article sur les paiements avant d'effectuer tout achat :

[Effectuer des paiements privés :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

De nombreux projets de crypto-monnaies, voire la plupart, sont des escroqueries. Effectuez des transactions avec prudence, uniquement avec des projets auxquels vous faites confiance.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Logo de Monero](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** utilise une blockchain dotée de technologies renforçant la confidentialité qui masquent les transactions afin d'assurer [:material-incognito: l'anonymat](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }. Chaque transaction Monero cache le montant de la transaction, les adresses d'envoi et de réception, ainsi que la source des fonds, sans aucune difficulté, ce qui en fait un choix idéal pour les novices en matière de crypto-monnaies.

[:octicons-home-16: Page d'accueil](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Code source" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribuer }

</details>

</div>

Avec Monero, les observateurs extérieurs ne peuvent pas déchiffrer les adresses qui échangent des Monero, les montants des transactions, les soldes des adresses ou l'historique des transactions.

<details class="info" markdown>
<summary>La résistance de Monero à la surveillance de masse</summary>

 Des publications publiques montrent que le Financial Crimes Enforcement Network du département du Trésor américain [a accordé une licence à](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) CipherTrace pour son "module Monero" à la fin de l'année 2022.</p> 

La confidentialité du graphe des transactions Monero est limitée par son cercle de signatures relativement petit, en particulier contre les attaques ciblées. Les caractéristiques de confidentialité de Monero ont également été [remises en question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) par certains chercheurs en sécurité, et un certain nombre de vulnérabilités graves ont été trouvées et corrigées dans le passé, de sorte que les affirmations faites par des organisations comme CipherTrace ne sont pas hors de question. S'il est peu probable qu'il existe des outils de surveillance de masse de Monero comme il en existe pour le Bitcoin et d'autres, il est certain que les outils de traçage facilitent les enquêtes ciblées.

En fin de compte, Monero est la crypto-monnaie la plus respectueuse de la vie privée, mais ses revendications en matière de confidentialité **n'ont pas** été prouvées de manière définitive. Plus de temps et de recherche sont nécessaires pour évaluer si le Monero est suffisamment résistant aux attaques pour toujours offrir une protection adéquate de la vie privée.

</details>



### Portefeuilles Monero

Pour une confidentialité optimale, veillez à utiliser un portefeuille autogardé, dans lequel la [clé de consultation](https://getmonero.org/resources/moneropedia/viewkey.html) reste stockée sur l'appareil. Cela signifie que vous êtes le seul à pouvoir dépenser vos fonds et à voir les transactions entrantes et sortantes. Si vous utilisez un portefeuille gardé (custodial), le prestataire peut voir **tout ce que** vous faites ; si vous utilisez un portefeuille « léger » où le fournisseur conserve votre clé d’audit (view key), celui-ci peut voir presque tout ce que vous faites (mais ne peut pas dépenser vos fonds). Voici quelques exemples de portefeuilles autogardés dans lesquels la clé de consultation ne quitte jamais votre appareil :

- [le client Monero officiel](https://getmonero.org/downloads) (bureau)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, Bureau) 
      - Cake Wallet prend en charge plusieurs crypto-monnaies. Une version de Cake Wallet réservée aux utilisateurs de Monero est disponible pour iOS et Android sur [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (bureau)
- [Monerujo](https://monerujo.io) (Android)



### Nœuds Monero

Pour bénéficier d'une confidentialité maximale (même avec un portefeuille en gestion propre), il est recommandé d'exécuter votre propre nœud Monero, appelé « [démon Monero](https://docs.getmonero.org/interacting/monerod-reference) », qui est inclus dans le [portefeuille en ligne de commande](https://getmonero.org/downloads/#cli). L'utilisation du nœud d'une autre personne expose certaines informations, telles que l'adresse IP à partir de laquelle vous vous connectez, les heures auxquelles vous synchronisez votre portefeuille et les transactions que vous envoyez à partir de votre portefeuille (mais pas d'autres détails sur ces transactions). Vous pouvez également vous connecter au nœud Monero d'un autre utilisateur via [Tor](alternative-networks.md#tor), [I2P](alternative-networks.md#i2p-the-invisible-internet-project) ou un [VPN](vpn.md).



### Acheter du Monero

[Quelques conseils pour obtenir des Monero](advanced/payments.md#acquisition ""){.md-button}

Il existe de nombreuses places d'échange centralisées (CEX) ainsi que des plateformes P2P sur lesquelles vous pouvez acheter et vendre du Monero. Certaines d'entre elles exigent que vous fournissiez des informations d'identité (KYC) afin de respecter la réglementation en matière de lutte contre le blanchiment d'argent. Cependant, en raison des caractéristiques de confidentialité de Monero, la seule chose connue du vendeur est *que* vous avez acheté du Monero, mais pas la quantité que vous possédez ni l'endroit où vous le dépensez (après qu'il a quitté la bourse). Voici quelques sites fiables où acheter du Monero :

- [Kraken](https://kraken.com): une plateforme d'échange centralisée (CEX) très connue. L'inscription et la vérification d'identité (KYC) sont obligatoires. Les paiements par carte bancaire et les virements bancaires sont acceptés. Veillez à ne pas laisser vos Monero nouvellement achetés sur la plateforme Kraken après l'achat ; transférez-les vers un portefeuille autogardé. Monero n'est pas disponible dans toutes les juridictions où Kraken exerce ses activités.[^1]
- [Cake Wallet](https://cakewallet.com): un portefeuille multiplateforme autogardé pour Monero et d'autres cryptomonnaies. Vous pouvez acheter des Monero directement dans l'application par carte bancaire ou virement bancaire (via des prestataires tiers tels que [Guardarian](https://guardarian.com) ou [DFX](https://dfx.swiss)).[^2] La procédure KYC n'est généralement pas requise, mais cela dépend de votre pays et du montant de votre achat. Dans les pays où il n'est pas possible d'acheter directement du Monero, vous pouvez également passer par un prestataire intégré à Cake Wallet pour acheter d'abord une autre cryptomonnaie, telle que le Bitcoin, le Bitcoin Cash ou le Litecoin, puis l'échanger contre du Monero directement depuis l'application. 
      - [Monero.com](https://monero.com) est un site partenaire sur lequel vous pouvez acheter du Monero et d'autres cryptomonnaies sans avoir à télécharger d'application. Les fonds seront simplement transférés vers l'adresse de portefeuille de votre choix.
- [RetoSwap](https://retoswap.com) (anciennement Haveno-Reto) est une plateforme d'échange P2P décentralisée (DEX) permettant la gestion autonome de ses actifs, basée sur le projet [Haveno](https://haveno.exchange) et disponible sous Linux, Windows et macOS. Le Monero peut être acheté et vendu en toute confidentialité, car la plupart des contreparties n'exigent pas de vérification d'identité (KYC), les transactions s'effectuent directement entre les utilisateurs (P2P) et toutes les connexions transitent par le réseau Tor. Il est possible d'acheter des Monero par virement bancaire, via PayPal, voire en espèces (lors d'un rendez-vous en personne ou par envoi postal). Des arbitres peuvent intervenir pour régler les litiges entre l'acheteur et le vendeur, mais soyez prudent lorsque vous communiquez vos coordonnées bancaires ou d'autres informations sensibles à votre contrepartie commerciale. La réalisation d'opérations sur certains comptes peut constituer une violation des conditions générales d'utilisation de ces comptes.



## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- La crypto-monnaie doit offrir des transactions privées/intraçables par défaut.

<div class="admonition tip" markdown>
<p class="admonition-title">Avertissement</p>

Le contenu présenté ici ne constitue pas un conseil juridique ou financier. Nous ne cautionnons ni n'encourageons les activités illicites, et nous ne cautionnons ni n'encourageons quoi que ce soit qui contrevienne aux conditions d'utilisations du service d'une entreprise. Vérifiez auprès d'un professionnel la conformité de ces recommandations aux règlementations en vigueur dans votre région. [Voir tous les avertissements](about/notices.md).

</div>

[^1]:    
    Vous pouvez consulter les pages suivantes pour obtenir des informations à jour sur les pays dans lesquels Kraken **n'** autorise **pas** l'achat de Monero : « [Où Kraken est-il agréé ou réglementé ? »](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) et « [Prise en charge de Monero (XMR) en Europe](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe) ».


[^2]:    
    Vous pouvez consulter les pages suivantes pour obtenir des informations à jour sur les pays dans lesquels Cake Wallet et Monero.com **n'** autorisent **que** l'achat direct de Monero (via des prestataires tiers) : « [Quels sont les pays desservis par DFX ? »](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) et « [Quels sont les pays/régions pris en charge ? » (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
