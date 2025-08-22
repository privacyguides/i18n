---
title: "Introduction à Tor"
icon: 'simple/torproject'
description: Tor est un réseau décentralisé, gratuit, conçu pour utiliser Internet avec le plus de confidentialité possible.
---

![Logo Tor](../assets/img/self-contained-networks/tor.svg){ align=right }

[**Tor**](../alternative-networks.md#tor) est un réseau décentralisé, gratuit, conçu pour utiliser Internet avec le plus de confidentialité possible. S'il est utilisé correctement, le réseau permet une navigation et des communications privées et anonymes. Parce que le trafic Tor est difficile à bloquer et à tracer, Tor est un outil efficace pour contourner la censure.

[:material-movie-open-play-outline: Vidéo : Pourquoi utiliser Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

Tor fonctionne en acheminant votre trafic Internet via des serveurs gérés par des bénévoles, au lieu d'établir une connexion directe avec le site que vous essayez de visiter. Cela permet de masquer la provenance du trafic, et aucun serveur sur le chemin de la connexion n'est en mesure de voir le chemin complet de la provenance et de la destination du trafic, ce qui signifie que même les serveurs que vous utilisez pour vous connecter ne peuvent pas briser votre anonymat.

[:octicons-home-16:](https://torproject.org){ .card-link title="Page d'accueil" }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Service onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Code source" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribuer }

## Se connecter en toute sécurité à Tor

Avant de vous connecter à Tor, vous devriez soigneusement réfléchir à ce que vous cherchez à accomplir en utilisant Tor, et à qui vous essayez de cacher votre activité sur le réseau.

Si vous vivez dans un pays libre, que vous accédez à du contenu banal via Tor, que vous n'êtes pas inquiété que votre FAI ou adminisateur de réseau local sachent que vous utilisz Tor, et que vous voulez aider à [déstigmatiser](https://2019.www.torproject.org/about/torusers.html.en) l'utilisation de Tor, vous pouvez vous connecter sans inquiétude à Tor directement via des moyens standards comme [Tor Browser](../tor.md) .

Si vous avez la possibilité d'accéder à un fournisseur de VPN de confiance et que **l'un** des éléments suivants est vrai, vous devriez presque certainement vous connecter à Tor par le biais d'un VPN :

- Vous utilisez déjà un [fournisseur VPN de confiance](../vpn.md)
- Votre modèle de menace inclut un adversaire capable d'extraire des informations de votre FAI
- Votre modèle de menace inclut votre FAI lui-même en tant qu'adversaire
- Votre modèle de menace inclut les administrateurs de réseaux locaux avant votre FAI en tant qu'adversaire

Parce que nous [recommandons généralement](../basics/vpn-overview.md) déjà que la grande majorité des gens utilisent un fournisseur de VPN de confiance pour diverses raisons, la recommandation suivante concernant la connexion à Tor via un VPN s'applique probablement à vous. <mark>Il n'est pas nécessaire de désactiver votre VPN avant de vous connecter à Tor</mark>, comme certaines ressources en ligne pourraient vous le faire croire.

En vous connectant directement à Tor, vous vous distinguerez auprès des administrateurs de réseaux locaux ou de votre FAI. La détection et la corrélation de ce trafic [ont été effectuées](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax) dans le passé par des administrateurs de réseau pour identifier et désanonymiser des utilisateurs spécifiques de Tor sur leur réseau. D'un autre côté, se connecter à un VPN est presque toujours moins suspect, parce que les fournisseurs de VPN commerciaux sont utilisés par les consommateurs de tous les jours pour une variété de tâches courantes telles que contourner les géo-restrictions, même dans les pays avec de lourdes restrictions d'Internet.

Par conséquent, vous devriez faire un effort pour cacher votre adresse IP **avant** de vous connecter au réseau Tor. Vous pouvez le faire simplement en vous connectant à un VPN (par le biais d'un client installé sur votre ordinateur) puis en accédant à [Tor](../tor.md) normalement (par exemple, via Tor Browser). Cela crée une chaîne de connexion comme celle-ci :

- [x] Vous → VPN → Tor → Internet

Du point de vue de votre FAI, il semble que vous accédez à un VPN normalement (avec la protection associée que cela vous fourni). Du point de vue de votre VPN, il peut voir que vous vous connectez au réseau Tor, mais rien sur les sites web auxquels vous accédez. Du point de vue de Tor, vous vous connectez normalement, mais dans le cas improbable d'une compromission du réseau Tor, seule l'IP de votre VPN serait exposée, et votre VPN devrait être compromis *également* pour vous désanonymiser.

Il ne s'agit **pas** d'un moyen de contournement de la censure, car si Tor est bloqué par votre FAI, votre VPN le sera probablement aussi. Cette recommandation vise plutôt à faire en sorte que votre trafic se fonde mieux dans le trafic banal des utilisateurs de VPN, et à vous fournir un certain niveau de déni plausible en masquant à votre FAI le fait que vous vous connectez à Tor.

---

Nous **déconseillons fortement** de combiner Tor avec un VPN de toute autre manière. Ne configurez pas votre connexion d'une manière qui ressemble à l'une des suivantes :

- Vous → Tor → VPN → Internet
- Vous → VPN → Tor → VPN → Internet
- Toute autre configuration

Certains fournisseurs de VPN et d'autres documentations recommandent parfois ces **mauvaises** configurations pour échapper à des bannissements de Tor (c'est-à-dire, aux bannissements des noeuds de sortie par les sites web). [Normalement](https://support.torproject.org/#about_change-paths), Tor change fréquemment le chemin de votre circuit à travers le réseau. Lorsque vous choisissez un VPN comme *destination* permanente (en vous connectant à un serveur VPN *après* Tor), vous éliminez cet avantage et nuisez considérablement à votre anonymat.

Il est difficile de mettre en place de mauvaises configurations comme celles-ci par accident, parce qu'elles impliquent généralement soit la mise en place de paramètres de proxy personnalisés dans le Navigateur Tor, soit la mise en place de paramètres de proxy personnalisés dans votre client VPN qui achemine votre trafic VPN à travers le Navigateur Tor. Tant que vous évitez ces configurations autres que celles par défaut, tout va bien.

---

<div class="admonition info" markdown>
<p class="admonition-title">Capture d'empreinte numérique VPN/SSH</p>

Le Tor Project [mentionne](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) que *théoriquement* l'utilisation d'un VPN pour cacher à votre FAI les activités Tor n'est pas forcément infaillible. Les VPNs se sont révélés vulnérables à la capture d'empreinte numérique du trafic des sites web (fingerprinting), un adversaire pouvant toujours deviner quel site web est visité, car tous les sites web ont des schémas de trafic spécifiques.

Il n'est donc pas déraisonnable de penser que le trafic Tor chiffré caché par un VPN pourrait également être détecté par des méthodes similaires. Il n'existe aucun document de recherche sur ce sujet, et nous considérons toujours que les avantages de l'utilisation d'un VPN l'emportent largement sur ces risques, mais il s'agit d'un élément à garder à l'esprit.

Si vous pensez toujours que les transports enfichables (ponts) offrent une protection supplémentaire contre la capture d'empreinte numérique du trafic de site web qu'un VPN n'offre pas, vous avez toujours la possibilité d'utiliser un pont **et** un VPN en même temps.

</div>

Pour déterminer si vous devez d'abord utiliser un VPN pour vous connecter au réseau Tor, il vous faudra faire preuve de bon sens et connaître les politiques de votre gouvernement et de votre FAI relatives à ce à quoi vous vous connectez. Cependant, dans la plupart des cas, il est préférable que vous soyez vu comme connecté à un réseau VPN commercial plutôt que directement au réseau Tor. Si les fournisseurs de VPN sont censurés dans votre région, vous pouvez également envisager d'utiliser des transports enfichables Tor (par exemple Snowflake ou les ponts meek) comme alternative, mais l'utilisation de ces ponts peut susciter plus de suspicion que les tunnels WireGuard/OpenVPN standard.

## Ce que Tor n'est pas

Dans tous les cas, le réseau Tor n'est pas un outil parfait en ce qui concerne la protection de la vie privée et présent un certain nombre d'inconvénients qu'il convient d'examiner attentivement. Ces éléments ne doivent pas vous décourager d'utiliser Tor s'il est adapté à vos besoins, mais ils doivent être pris en compte lors du choix de la solution la plus appropriée pour vous.

### Tor n'est pas un VPN gratuit

La sortie de l'application mobile *Orbot* a conduit de nombreuses personnes à décrire Tor comme un "VPN gratuit" pour tout le trafic de votre appareil. Cependant, traiter Tor de cette manière présente certains dangers par rapport à un VPN classique.

Contrairement aux nœuds de sortie de Tor, les fournisseurs de VPN ne sont généralement pas *activement* [malveillants](#caveats). Les nœuds de sortie Tor pouvant être créés par n'importe qui, ils constituent des points névralgiques pour l'enregistrement et la modification du réseau. En 2020, de nombreux nœuds de sortie de Tor ont été documentés comme rétrogradant le trafic HTTPS en HTTP afin de [détourner des transactions de crypto-monnaies](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). D'autres attaques de nœuds de sortie, telles que le remplacement de téléchargements par des logiciels malveillants via des canaux non chiffrés, ont également été observées. Le protocole HTTPS atténue ces menaces dans une certaine mesure.

Comme nous l'avons déjà mentionné, Tor est également facilement identifiable sur le réseau. Contrairement à un véritable fournisseur de VPN, l'utilisation de Tor vous fera passer pour une personne qui tente probablement d'échapper aux autorités. Dans un monde parfait, Tor serait considéré par les administrateurs réseaux et les autorités comme un outils aux multiples usages (comme les VPNs), mais en réalité Tor est plutôt perçu comme bien moins légitime que les VPNs commerciaux. Ainsi, l'utilisation d'un vrai VPN vous permet un déni plausible, par exemple "Je l'utilisais juste pour regarder Netflix", etc.

### L'utilisation de Tor n'est pas indétectable

**Même si vous utilisez des ponts et des transports enfichables,** le Projet Tor ne fournit aucun outil pour cacher à votre FAI le fait que vous utilisez Tor. Même l'utilisation de "transports enfichables" obscurcis ou de ponts non publics ne permet pas de dissimuler le fait que l'on utilise un canal de communication privé. Les transports enfichables les plus populaires comme obfs4 (qui obscurcit votre trafic pour "ne ressembler à rien") et meek (qui utilise le domain fronting pour camoufler votre trafic) peuvent être [détectés](https://hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) avec des techniques d'analyse du trafic assez classiques. Snowflake présente des problèmes similaires et peut être [facilement détecté](https://hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) *avant* même qu'une connexion Tor ne soit établie.

Il existe des transport enfichables autres que ces trois-là, mais ils reposent généralement sur la sécurité par l'obscurité pour échapper à la détection. Ils ne sont pas impossibles à détecter - ils sont simplement utilisés par si peu de personnes qu'il ne vaut pas la peine de construire des détecteurs spécifiques. Il ne faut pas s'y fier si vous êtes spécifiquement surveillé.

Il est essentiel de comprendre la différence entre contourner la censure et échapper à la détection. Il est plus facile d'accomplir la première solution en raison des nombreuses limitations réelles de ce que les censeurs de réseau peuvent faire en masse, mais ces techniques ne cachent pas le fait que vous -*spécifiquement* - utilisez Tor à une personne intéressée qui surveille votre réseau.

### Le Navigateur Tor n'est pas le navigateur le plus *sûr*

L'anonymat est souvent en contradiction avec la sécurité : l'anonymat de Tor exige que chaque utilisateur soit identique, ce qui crée une monoculture (les mêmes bugs sont présents chez tous les utilisateurs du navigateur Tor). En matière de cybersécurité, les monocultures sont généralement considérées comme mauvaises : la sécurité par la diversité (qui fait défaut à Tor) permet une segmentation naturelle en limitant les vulnérabilités à des groupes plus restreints, et est donc généralement souhaitable, mais cette diversité est également moins bonne pour l'anonymat.

En outre, le Navigateur Tor est basé sur les versions Extended Support Release de Firefox, qui ne reçoivent des correctifs que pour les vulnérabilités considérées comme *Critique* et *Élevée* (et non pour celles *Moyenne* et *Faible*). Cela signifie que les attaquants pourraient (par exemple) :

1. Rechercher les nouvelles vulnérabilités Critique/Élevée dans les versions nightly ou bêta de Firefox, puis vérifier si elles sont exploitables dans le navigateur Tor (cette période de vulnérabilité peut durer des semaines).
2. Enchaîner *plusieurs * vulnérabilités Moyenne/Faible jusqu'à ce qu'ils obtiennent le niveau d'accès qu'ils recherchent (cette période de vulnérabilité peut durer des mois ou plus).

Les personnes exposées aux vulnérabilités des navigateurs devraient envisager des protections supplémentaires pour se défendre contre les exploits du Navigateur Tor, comme l'utilisation de Whonix dans [Qubes](../os/qubes-overview.md) pour contenir votre navigation Tor dans une machine virtuelle sécurisée et la protéger contre les fuites.

## Création de chemins vers les services de surface

Les "services de surface" sont des sites web auxquels vous pouvez accéder avec n'importe quel navigateur, comme [privacyguides.org](https://www.privacyguides.org). Tor vous permet de vous connecter à ces sites web de manière anonyme en acheminant votre trafic via un réseau composé de milliers de serveurs gérés par des bénévoles et appelés nœuds (ou relais).

Chaque fois que vous [vous connectez à Tor](../tor.md), il choisit trois nœuds pour construire un chemin vers Internet - ce chemin est appelé "circuit"

<figure markdown>
  ![Chemin Tor montrant votre appareil se connectant à un noeud d'entrée, un noeud central et un noeud de sortie avant d'atteindre le site web de destination](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Chemin Tor montrant votre appareil se connectant à un noeud d'entrée, un noeud central et un noeud de sortie avant d'atteindre le site web de destination](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Chemin du circuit Tor</figcaption>
</figure>

Chacun de ces nœuds a sa propre fonction:

### Le nœud d'entrée

Le noeud d'entrée, souvent appelé le noeud de garde, est le premier noeud auquel votre client Tor se connecte. Le nœud d'entrée est capable de voir votre adresse IP, mais il est incapable de voir à quoi vous vous connectez.

Contrairement aux autres nœuds, le client Tor choisira aléatoirement un nœud d'entrée et restera avec lui pendant deux à trois mois pour vous protéger de certaines attaques.[^1]

### Le nœud central

Le noeud central est le second noeud auquel votre client Tor se connecte. Il peut voir de quel nœud provient le trafic - le nœud d'entrée - et vers quel nœud il se dirige ensuite. Le nœud central ne peut pas voir votre adresse IP ou le domaine auquel vous vous connectez.

Pour chaque nouveau circuit, le nœud central est choisi au hasard parmi tous les nœuds Tor disponibles.

### Le nœud de sortie

Le nœud de sortie est le point où votre trafic web quitte le réseau Tor et est transféré vers la destination souhaitée. Le nœud de sortie ne peut pas voir votre adresse IP, mais il sait à quel site il se connecte.

Le noeud de sortie sera choisi au hasard parmi tous les noeuds Tor disponibles et exécutés avec une balise "relais de sortie".[^2]

## Création de chemins vers les services onion

Les "services onion" (également communément appelés "services cachés") sont des sites web auxquels on ne peut accéder qu'au moyen du navigateur Tor. Ces sites web ont un long nom de domaine généré de manière aléatoire et se terminant par `.onion`.

La connexion à un service onion dans Tor fonctionne de manière très similaire à la connexion à un service de surface, mais votre trafic est acheminé à travers un total de **six nœuds** avant d'atteindre le serveur de destination. Cependant, comme auparavant, seuls trois de ces nœuds contribuent à *votre* anonymat, les trois autres nœuds protègent *l'anonymat du Service Onion*, en cachant la véritable IP et la localisation du site web de la même manière que le navigateur Tor cache les vôtres.

<figure style="width:100%" markdown>
  ![Chemin Tor montrant votre trafic acheminé à travers vos trois noeuds Tor plus trois noeuds Tor supplémentaires qui cachent l'identité du site web](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Chemin Tor montrant votre trafic acheminé à travers vos trois noeuds Tor plus trois noeuds Tor supplémentaires qui cachent l'identité du site web](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Chemin du circuit Tor avec des services onion. Les nœuds de la zone <span class="pg-blue">bleue</span> appartiennent à votre navigateur, tandis que les nœuds de la zone <span class="pg-red">rouge</span> appartiennent au serveur, de sorte que leur identité vous est cachée.</figcaption>
</figure>

## Chiffrement

Tor chiffre chaque paquet (un bloc de données transmises) trois fois avec les clefs du nœud de sortie, du nœud central, et du nœud d'entrée, dans cet ordre.

Une fois que Tor a construit un circuit, la transmission des données se fait comme suit:

1. Premièrement: lorsque le paquet arrive au nœud d'entrée, la première couche de chiffrement est supprimée. Dans ce paquet chiffré, le nœud d'entrée trouvera un autre paquet chiffré avec l'adresse du nœud central. Le nœud d'entrée transmet ensuite le paquet au nœud central.

2. Deuxièmement : lorsque le nœud central reçoit le paquet du nœud d'entrée, il supprime lui aussi une couche de chiffrement avec sa clé, et trouve cette fois un paquet chiffré avec l'adresse du nœud de sortie. Le nœud central transmet ensuite le paquet au nœud de sortie.

3. Enfin, lorsque le nœud de sortie reçoit son paquet, il supprime la dernière couche de chiffrement avec sa clé. Le nœud de sortie verra l'adresse de destination et transmettra le paquet à cette adresse.

Vous trouverez ci-dessous un autre schéma illustrant le processus. Chaque nœud supprime sa propre couche de chiffrement, et lorsque le serveur de destination renvoie les données, le même processus se déroule entièrement en sens inverse. Par exemple, le nœud de sortie ne sait pas qui vous êtes, mais il sait de quel nœud il provient. Il ajoute donc sa propre couche de chiffrement et renvoie le message.

<figure markdown>
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Envoyer et recevoir des données à travers le réseau Tor</figcaption>
</figure>

Tor nous permet de nous connecter à un serveur sans que personne ne connaisse le chemin entier. Le nœud d'entrée sait qui vous êtes, mais pas où vous allez; le nœud central ne sait pas qui vous êtes ni où vous allez; et le nœud de sortie sait où vous allez, mais pas qui vous êtes. Comme le nœud de sortie est celui qui établit la connexion finale, le serveur de destination ne connaîtra jamais votre adresse IP.

## Mises en garde 

Bien que Tor offre de solides garanties de confidentialité, il faut être conscient que Tor n'est pas parfait:

- Tor ne vous protège jamais contre le risque de vous exposer par erreur, par exemple si vous partagez trop d'informations sur votre identité réelle.
- Les nœuds de sortie de Tor peuvent **modifier** le trafic non chiffré qui passe par eux. Cela signifie que le trafic non chiffré, tel que le trafic HTTP ordinaire, peut être modifié par un nœud de sortie malveillant. Ne téléchargez **jamais** des fichiers à partir d'un site web non chiffré `http://` via Tor, et assurez-vous que votre navigateur est configuré de manière à toujours mettre à niveau le trafic HTTP vers HTTPS.
- Les nœuds de sortie de Tor peuvent également surveiller le trafic qui passe par eux. Le trafic non chiffré qui contient des informations personnellement identifiables peut vous désanonymiser jusqu'à ce nœud de sortie. Encore une fois, nous recommandons de n'utiliser que HTTPS via Tor.
- Des adversaires puissants capables de surveiller passivement *tout* le trafic réseau du monde entier ("Global Passive Adversaries") ne sont **pas** une chose contre laquelle Tor vous protège (et l'utilisation de Tor [avec un VPN](#safely-connecting-to-tor) ne change rien à ce fait).
- Des adversaires bien financés ayant la capacité d'observer passivement *la plupart* du trafic réseau du monde ont encore une *chance* de désanonymiser les utilisateurs de Tor au moyen d'une analyse avancée du trafic.

Si vous souhaitez utiliser Tor pour naviguer sur le web, nous ne recommandons que le Navigateur Tor **officiel** - il est conçu pour empêcher la capture d'empreintes numériques.

- [Navigateur Tor :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Protections offertes par les ponts

Les ponts Tor sont généralement présentés comme une méthode alternative pour cacher l'utilisation de Tor à un FAI, au lieu d'un VPN (que nous suggérons d'utiliser si possible). Il faut savoir que si les ponts permettent de contourner la censure de manière adéquate, il ne s'agit que d'un avantage *transitoire*. Ils ne vous protègent pas de manière adéquate contre le fait que votre FAI découvre que vous vous êtes connecté à Tor dans le *passé* grâce à l'analyse historique des journaux de trafic.

Pour illustrer ce point, considérez le scénario suivant : vous vous connectez à Tor via un pont et votre FAI ne le détecte pas parce qu'il n'effectue pas d'analyse sophistiquée de votre trafic et que les choses fonctionnent donc comme prévu. Quatre mois se sont écoulés et l'IP de votre pont a été rendue publique. Il s'agit d'un phénomène très courant avec les ponts, qui sont découverts et bloqués relativement souvent, mais pas immédiatement.

Votre FAI veut identifier les utilisateurs de Tor il y a 4 mois, et avec leurs journaux de métadonnées limités, ils peuvent voir que vous vous êtes connecté à une adresse IP qui s'est révélée plus tard être un pont Tor. Vous n'avez pratiquement aucune autre excuse pour établir une telle connexion, de sorte que le FAI peut affirmer avec une très grande certitude que vous étiez un utilisateur de Tor à ce moment-là.

Comparez cela à notre scénario recommandé, dans lequel vous vous connectez à Tor par le biais d'un VPN. Supposons que 4 mois plus tard, votre FAI souhaite à nouveau identifier toute personne ayant utilisé Tor il y a 4 mois. Leurs journaux peuvent très certainement identifier votre trafic il y a quatre mois, mais tout ce qu'ils pourraient voir, c'est que vous vous êtes connecté à l'adresse IP d'un VPN. En effet, la plupart des FAI ne conservent sur de longues périodes que les métadonnées et non le contenu intégral du trafic que vous effectuez. Le stockage de l'intégralité de vos données de trafic nécessiterait une quantité massive d'espace de stockage que la quasi-totalité des adversaires ne possèdent pas.

Comme il est presque certain que votre FAI ne capture pas toutes les données au niveau des paquets et les stocke indéfiniment, il n'a aucun moyen de déterminer à quoi vous vous êtes connecté avec ce VPN *après* coup avec une technique avancée telle que l'inspection approfondie des paquets, et vous avez donc un déni plausible.

Par conséquent, les ponts sont les plus utiles pour contourner la censure sur Internet *dans l'immédiat*, mais elles ne remplacent pas **tous** les avantages que l'utilisation d'un VPN avec Tor peut apporter. Encore une fois, il ne s'agit pas d'un conseil *contre* l'utilisation des ponts Tor, vous devez simplement être conscient de ces limitations lorsque vous prenez votre décision. Dans certains cas, les ponts peuvent être la *seule* option (si tous les fournisseurs de VPN sont bloqués, par exemple), vous pouvez donc toujours les utiliser dans ces circonstances en gardant cette limitation à l'esprit.

Si vous pensez qu'un pont peut vous aider à vous défendre contre la capture d'empreinte numérique ou d'autres analyses avancées du réseau plus que ne le fait déjà le tunnel chiffré d'un VPN, vous avez toujours la possibilité d'utiliser un pont en conjonction avec un VPN. Ainsi, vous restez protégé par les techniques d'obscurcissement du transport enfichable, même si un adversaire parvient à avoir un certain niveau de visibilité dans votre tunnel VPN. Si vous décidez de suivre cette voie, nous vous recommandons de vous connecter à un pont obfs4 derrière votre VPN pour une protection optimale contre la capture d'empreintes numériques, plutôt qu'à meek ou Snowflake.

Il est [possible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) que le transport enfichable [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) actuellement à l'essai puisse atténuer certains de ces problèmes. Nous continuerons à suivre l'évolution de cette technologie.

## Ressources supplémentaires

- [Manuel d'utilisation du navigateur Tor](https://tb-manual.torproject.org)
- [Comment fonctionne Tor - Computerphile](https://youtube.com/watch?v=QRYzre4bf7I) <small>(YouTube)</small>
- [Les Services Onions de Tor - Computerphile](https://youtube.com/watch?v=lVcbq_a5N9I)<small>(YouTube)</small>

[^1]: Le premier relais de votre circuit est appelé "garde d'entrée" ou "garde". Il s'agit d'un relais rapide et stable qui reste le premier de votre circuit pendant 2 à 3 mois afin de vous protéger contre une attaque connue de rupture d'anonymat. Le reste de votre circuit change avec chaque nouveau site web que vous visitez, et tous ensemble ces relais fournissent les protections complètes de Tor en matière de vie privée. Pour en savoir plus sur le fonctionnement des relais de garde, consultez cet [article de blog](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) et ce [document](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) sur les gardes d'entrée. ([https://support.torproject.org/tbb/tbb-2](https://support.torproject.org/tbb/tbb-2))

[^2]: Balise de relai: une (dis-)qualification spéciale des relais pour les positions de circuit (par exemple, "Guard", "Exit", "BadExit"), les propriétés de circuit (par exemple, "Fast", "Stable") ou les rôles (par exemple, "Authority", "HSDir"), tels qu'attribués par les autorités de l'annuaire et définis plus précisément dans la spécification du protocole de l'annuaire. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html#relay-flag))
