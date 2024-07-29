---
meta_title: "Chaînes de blocs de crypto-monnaies privées - Privacy Guides"
title: Crypto-monnaie
icon: material/bank-circle
cover: cryptocurrency.webp
---

Effectuer des paiements en ligne est l'un des plus grands défis en matière de protection de la vie privée. Ces crypto-monnaies garantissent par défaut la confidentialité des transactions (ce qui n'est **pas** garanti par la majorité des crypto-monnaies), à condition que vous ayez une bonne compréhension de la façon d'effectuer des paiements privés de manière efficace. Nous vous encourageons vivement à lire notre article sur les paiements avant d'effectuer tout achat :

[Effectuer des paiements privés :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

De nombreux projets de crypto-monnaies, voire la plupart, sont des escroqueries. Effectuez des transactions avec prudence, uniquement avec des projets auxquels vous faites confiance.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Logo Monero](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** utilise une chaîne de blocs avec des technologies de protection de la vie privée qui obscurcissent les transactions afin d'obtenir un anonymat. Chaque transaction Monero cache le montant de la transaction, les adresses d'envoi et de réception, ainsi que la source des fonds, sans aucune difficulté, ce qui en fait un choix idéal pour les novices en matière de crypto-monnaies.

[:octicons-home-16: Page d'accueil](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Code source" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribuer }

</details>

</div>

Avec Monero, les observateurs extérieurs ne peuvent pas déchiffrer les adresses qui échangent des Monero, les montants des transactions, les soldes des adresses ou l'historique des transactions.

Pour une confidentialité optimale, assurez-vous d'utiliser un portefeuille non dépositaire, où la clé d'affichage reste sur l'appareil. Cela signifie que vous êtes le seul à pouvoir dépenser vos fonds et à voir les transactions entrantes et sortantes. Si vous utilisez un portefeuille dépositaire, le fournisseur peut voir **tout** ce que vous faites ; si vous utilisez un portefeuille "léger" dans lequel le fournisseur conserve votre clé d'affichage privée, il peut voir presque tout ce que vous faites. Parmi les portefeuilles non dépositaires, on peut citer :

- [le client Monero officiel](https://getmonero.org/downloads) (bureau)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, macOS)
    - Cake Wallet prend en charge plusieurs crypto-monnaies. Une version de Cake Wallet réservée aux utilisateurs de Monero est disponible pour iOS et Android sur [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (bureau)
- [Monerujo](https://monerujo.io) (Android)

Pour une confidentialité maximale (même avec un portefeuille non dépositaire), vous devriez utiliser votre propre nœud Monero. L'utilisation du nœud d'une autre personne expose certaines informations, telles que l'adresse IP à partir de laquelle vous vous connectez, les heures auxquelles vous synchronisez votre portefeuille et les transactions que vous envoyez à partir de votre portefeuille (mais pas d'autres détails sur ces transactions). Vous pouvez également vous connecter au nœud Monero de quelqu'un d'autre via Tor ou [I2P](alternative-networks.md#i2p-the-invisible-internet-project).

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. Des publications publiques montrent que le Financial Crimes Enforcement Network du département du Trésor américain [a accordé une licence à](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) CipherTrace pour son "module Monero" à la fin de l'année 2022.

La confidentialité du graphe des transactions Monero est limitée par son cercle de signatures relativement petit, en particulier contre les attaques ciblées. Les caractéristiques de confidentialité de Monero ont également été [remises en question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) par certains chercheurs en sécurité, et un certain nombre de vulnérabilités graves ont été trouvées et corrigées dans le passé, de sorte que les affirmations faites par des organisations comme CipherTrace ne sont pas hors de question. S'il est peu probable qu'il existe des outils de surveillance de masse de Monero comme il en existe pour le Bitcoin et d'autres, il est certain que les outils de traçage facilitent les enquêtes ciblées.

En fin de compte, Monero est la crypto-monnaie la plus respectueuse de la vie privée, mais ses revendications en matière de confidentialité **n'ont pas** été prouvées de manière définitive. Plus de temps et de recherche sont nécessaires pour évaluer si le Monero est suffisamment résistant aux attaques pour toujours offrir une protection adéquate de la vie privée.

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- La crypto-monnaie doit offrir des transactions privées/intraçables par défaut.
