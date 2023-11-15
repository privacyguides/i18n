---
title: "Introduction à Tor"
icon: 'simple/torproject'
description: Tor est un réseau décentralisé, gratuit, conçu pour utiliser Internet avec le plus de confidentialité possible.
---

Tor est un réseau décentralisé, gratuit, conçu pour utiliser Internet avec le plus de confidentialité possible. S'il est utilisé correctement, le réseau permet une navigation et des communications privées et anonymes.

## Se connecter en toute sécurité à Tor

Avant de vous connecter à [Tor](../tor.md), vous devriez soigneusement réfléchir à ce que vous cherchez à accomplir en utilisant Tor, et à qui vous essayez de cacher votre activité sur le réseau.

Si vous vivez dans un pays libre, que vous accédez à du contenu banal via Tor, que vous ne craignez pas que votre FAI ou vos administrateurs de réseau local sachent que vous utilisez Tor, et que vous voulez aider [à déstigmatiser](https://2019.www.torproject.org/about/torusers.html.en) l'utilisation de Tor, vous pouvez probablement vous connecter à Tor directement via des moyens standards comme le [Navigateur Tor](../tor.md) sans inquiétude.

Si vous avez la possibilité d'accéder à un fournisseur de VPN de confiance et que **l'un** des éléments suivants est vrai, vous devriez presque certainement vous connecter à Tor par le biais d'un VPN :

- Vous utilisez déjà un [fournisseur VPN de confiance](../vpn.md)
- Votre modèle de menace inclut un adversaire capable d'extraire des informations de votre FAI
- Votre modèle de menace inclut votre FAI lui-même en tant qu'adversaire
- Votre modèle de menace inclut les administrateurs de réseaux locaux avant votre FAI en tant qu'adversaire

Parce que nous [recommandons généralement](../basics/vpn-overview.md) déjà que la grande majorité des gens utilisent un fournisseur de VPN de confiance pour diverses raisons, la recommandation suivante concernant la connexion à Tor via un VPN s'applique probablement à vous. <mark>Il n'est pas nécessaire de désactiver votre VPN avant de vous connecter à Tor</mark>, comme certaines ressources en ligne pourraient vous le faire croire.

En vous connectant directement à Tor, vous vous distinguerez auprès des administrateurs de réseaux locaux ou de votre FAI. La détection et la corrélation de ce trafic [ont été effectuées](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax/) dans le passé par des administrateurs de réseau pour identifier et désanonymiser des utilisateurs spécifiques de Tor sur leur réseau. D'un autre côté, se connecter à un VPN est presque toujours moins suspect, parce que les fournisseurs de VPN commerciaux sont utilisés par les consommateurs de tous les jours pour une variété de tâches courantes telles que contourner les géo-restrictions, même dans les pays avec de lourdes restrictions d'Internet.

Par conséquent, vous devriez faire un effort pour cacher votre adresse IP **avant** de vous connecter au réseau Tor. Vous pouvez le faire simplement en vous connectant à un VPN (par le biais d'un client installé sur votre ordinateur) et en accédant à [Tor](../tor.md) comme d'habitude, par exemple via le Navigateur Tor. Cela crée une chaîne de connexion comme :

- [x] Vous → VPN → Tor → Internet

Du point de vue de votre FAI, il semble que vous accédez à un VPN normalement (avec la protection associée que cela vous fourni). Du point de vue de votre VPN, il peut voir que vous vous connectez au réseau Tor, mais rien sur les sites web auxquels vous accédez. Du point de vue de Tor, vous vous connectez normalement, mais dans le cas improbable d'une compromission du réseau Tor, seule l'IP de votre VPN serait exposée, et votre VPN devrait être compromis *également* pour vous désanonymiser.

Il ne s'agit **pas** de conseils de contournement de la censure, car si Tor est entièrement bloqué par votre FAI, votre VPN le sera probablement aussi. Cette recommandation vise plutôt à faire en sorte que votre trafic se fonde mieux dans le trafic banal des utilisateurs de VPN, et à vous fournir un certain niveau de déni plausible en masquant à votre FAI le fait que vous vous connectez à Tor.

---

Nous **déconseillons fortement** de combiner Tor avec un VPN de toute autre manière. Ne configurez pas votre connexion d'une manière qui ressemble à l'une des suivantes :

- Vous → Tor → VPN → Internet
- Vous → VPN → Tor → VPN → Internet
- Toute autre configuration

Certains fournisseurs de VPN et d'autres publications recommandent parfois ces **mauvaises configurations** pour éviter les interdictions de Tor (les nœuds de sortie étant bloqués par des sites web) dans certains endroits. [Normalement](https://support.torproject.org/#about_change-paths), Tor change fréquemment le chemin de votre circuit à travers le réseau. Lorsque vous choisissez un VPN comme *destination* permanente (en vous connectant à un serveur VPN *après* Tor), vous éliminez cet avantage et nuisez considérablement à votre anonymat.

Il est difficile de mettre en place de mauvaises configurations comme celles-ci par accident, parce qu'elles impliquent généralement soit la mise en place de paramètres de proxy personnalisés dans le Navigateur Tor, soit la mise en place de paramètres de proxy personnalisés dans votre client VPN qui achemine votre trafic VPN à travers le Navigateur Tor. Tant que vous évitez ces configurations autres que celles par défaut, tout va bien.

---

!!! info "Empreinte numérique VPN/SSH"

    Le Tor Project [mentionne](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) que *théoriquement* l'utilisation d'un VPN pour cacher à votre FAI les activités Tor n'est pas forcément infaillible. Les VPNs se sont révélés vulnérables à la prise d'empreinte numérique du trafic des sites web, un adversaire pouvant toujours deviner quel site web est visité, car tous les sites web ont des schémas de trafic spécifiques.
    
    Il n'est donc pas déraisonnable de penser que le trafic Tor chiffré caché par un VPN pourrait également être détecté par des méthodes similaires. Il n'existe aucun document de recherche sur ce sujet, et nous considérons toujours que les avantages de l'utilisation d'un VPN l'emportent largement sur ces risques, mais il s'agit d'un élément à garder à l'esprit.
    
    Si vous pensez toujours que les transports enfichables (ponts) offrent une protection supplémentaire contre la prise d'empreinte numérique du trafic de site web qu'un VPN n'offre pas, vous avez toujours la possibilité d'utiliser un pont **et** un VPN en même temps.

Pour déterminer si vous devez d'abord utiliser un VPN pour vous connecter au réseau Tor, il vous faudra faire preuve de bon sens et connaître les politiques de votre gouvernement et de votre FAI relatives à ce à quoi vous vous connectez. Cependant, encore une fois et dans la plupart des cas, il est préférable que vous soyez vu comme connecté à un réseau VPN commercial plutôt que directement au réseau Tor. Si les fournisseurs de VPN sont censurés dans votre région, vous pouvez également envisager d'utiliser des transports enfichables Tor (par exemple les ponts Snowflake ou meek) comme alternative, mais l'utilisation de ces ponts peut susciter plus de suspicion que les tunnels WireGuard/OpenVPN standard.

## Ce que Tor n'est pas

Le réseau Tor n'est pas l'outil de protection de la vie privée idéal dans tous les cas et présente un certain nombre d'inconvénients qu'il convient d'examiner attentivement. Ces éléments ne doivent pas vous décourager d'utiliser Tor s'il est adapté à vos besoins, mais ils doivent être pris en compte lors du choix de la solution la plus appropriée pour vous.

### Tor n'est pas un VPN gratuit

La sortie de l'application mobile *Orbot* a conduit de nombreuses personnes à décrire Tor comme un "VPN gratuit" pour tout le trafic de votre appareil. Cependant, traiter Tor de cette manière présente certains dangers par rapport à un VPN classique.

Contrairement aux nœuds de sortie de Tor, les fournisseurs de VPN ne sont généralement pas *activement* [malveillants](#caveats). Les nœuds de sortie Tor pouvant être créés par n'importe qui, ils constituent des points névralgiques pour l'enregistrement et la modification du réseau. En 2020, de nombreux nœuds de sortie de Tor ont été documentés comme rétrogradant le trafic HTTPS en HTTP afin de [détourner des transactions de crypto-monnaies](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). D'autres attaques de nœuds de sortie, telles que le remplacement de téléchargements par des logiciels malveillants via des canaux non chiffrés, ont également été observées. Le protocole HTTPS atténue ces menaces dans une certaine mesure.

Comme nous l'avons déjà mentionné, Tor est également facilement identifiable sur le réseau. Contrairement à un véritable fournisseur de VPN, l'utilisation de Tor vous fera passer pour une personne qui tente probablement d'échapper aux autorités. Dans un monde parfait, Tor serait perçu par les administrateurs réseau et les autorités comme un outil aux multiples usages (comme les VPNs), mais dans la réalité, la perception de Tor est encore bien moins légitime que celle des VPNs commerciaux, de sorte que l'utilisation d'un vrai VPN vous permet d'opposer un démenti plausible, par exemple "Je l'utilisais juste pour regarder Netflix", etc.

### L'utilisation de Tor n'est pas indétectable

**Même si vous utilisez des ponts et des transports enfichables,** le Tor Project ne fournit aucun outil pour cacher à votre FAI le fait que vous utilisez Tor. Même l'utilisation de "transports enfichables" obscurcis ou de ponts non publics ne permet pas de dissimuler le fait que l'on utilise un canal de communication privé. Les transports enfichables les plus populaires comme obfs4 (qui obscurcit votre trafic pour "ne ressembler à rien") et meek (qui utilise le domain fronting pour camoufler votre trafic) peuvent être [détectés](https://www.hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) avec des techniques d'analyse du trafic assez classiques. Snowflake présente des problèmes similaires et peut être [facilement détecté](https://www.hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) *avant même* qu'une connexion Tor ne soit établie.

Il existe des transport enfichables autres que ces trois-là, mais ils reposent généralement sur la sécurité par l'obscurité pour échapper à la détection. Ils ne sont pas impossibles à détecter, ils sont simplement utilisés par si peu de personnes que cela ne vaut pas la peine de construire des détecteurs pour eux. Il ne faut pas s'y fier si vous êtes spécifiquement surveillé.

Il est essentiel de comprendre la différence entre contourner la censure et échapper à la détection. Il est plus facile d'accomplir la première solution en raison des nombreuses limitations réelles de ce que les censeurs de réseau peuvent faire en masse, mais ces techniques ne cachent pas le fait que vous -*spécifiquement* - utilisez Tor à une personne intéressée qui surveille votre réseau.

### Le Navigateur Tor n'est pas le navigateur le plus *sûr*

L'anonymat est souvent en contradiction avec la sécurité : L'anonymat de Tor exige que chaque utilisateur soit identique, ce qui crée une monoculture (les mêmes bugs sont présents chez tous les utilisateurs du navigateur Tor). En matière de cybersécurité, les monocultures sont généralement considérées comme mauvaises : la sécurité par la diversité (qui fait défaut à Tor) permet une segmentation naturelle en limitant les vulnérabilités à des groupes plus restreints, et est donc généralement souhaitable, mais cette diversité est également moins bonne pour l'anonymat.

En outre, le Navigateur Tor est basé sur les versions Extended Support Release de Firefox, qui ne reçoivent des correctifs que pour les vulnérabilités considérées comme *Critique* et *Élevée* (et non pour celles *Moyenne* et *Faible*). Cela signifie que les attaquants pourraient (par exemple) :

1. Rechercher les nouvelles vulnérabilités Critique/Élevée dans les versions nightly ou bêta de Firefox, puis vérifier si elles sont exploitables dans le navigateur Tor (cette période de vulnérabilité peut durer des semaines).
2. Enchaîner *plusieurs * vulnérabilités Moyenne/Faible jusqu'à ce qu'ils obtiennent le niveau d'accès qu'ils recherchent (cette période de vulnérabilité peut durer des mois ou plus).

Les personnes exposées aux vulnérabilités des navigateurs devraient envisager des protections supplémentaires pour se défendre contre les exploits du Navigateur Tor, comme l'utilisation de Whonix dans [Qubes](../os/qubes-overview.md) pour contenir votre navigation Tor dans une VM sécurisée et la protéger contre les fuites.

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

La connexion à un service onion dans Tor fonctionne de manière très similaire à la connexion à un service de surface, mais votre trafic est acheminé à travers un total de **six nœuds** avant d'atteindre le serveur de destination. Cependant, comme auparavant, seuls trois de ces nœuds contribuent à *votre* anonymat, les trois autres nœuds protègent *l'anonymat du service onion*, en cachant la véritable IP et la localisation du site web de la même manière que le navigateur Tor cache les vôtres.

<figure style="width:100%" markdown>
  ![Chemin Tor montrant votre trafic acheminé à travers vos trois noeuds Tor plus trois noeuds Tor supplémentaires qui cachent l'identité du site web](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Chemin Tor montrant votre trafic acheminé à travers vos trois noeuds Tor plus trois noeuds Tor supplémentaires qui cachent l'identité du site web](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Chemin du circuit Tor avec des services onion. Les nœuds de la zone <span class="pg-blue">bleue</span> appartiennent à votre navigateur, tandis que les nœuds de la zone <span class="pg-red">rouge</span> appartiennent au serveur, de sorte que leur identité vous est cachée.</figcaption>
</figure>

## Chiffrement

Tor chiffre chaque paquet (un bloc de données transmises) trois fois avec les clés du nœud de sortie, du nœud central, et du nœud d'entrée, dans cet ordre.

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
- Les nœuds de sortie de Tor peuvent également surveiller le trafic qui passe par eux. Le trafic non chiffré qui contient des informations personnellement identifiables peut vous désanonymiser jusqu'à ce nœud de sortie. Again, we recommend only using HTTPS over Tor.
- Powerful adversaries with the capability to passively watch *all* network traffic around the globe ("Global Passive Adversaries") are **not** something that Tor protects you against (and using Tor [with a VPN](#safely-connecting-to-tor) doesn't change this fact).
- Well-funded adversaries with the capability to passively watch *most* network traffic around the globe still have a *chance* of deanonymizing Tor users by means of advanced traffic analysis.

Si vous souhaitez utiliser Tor pour naviguer sur le web, nous ne recommandons que le navigateur Tor **officiel** - il est conçu pour empêcher la prise d'empreintes numériques.

- [Navigateur Tor :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Protections provided by bridges

Tor bridges are commonly touted as an alternative method to hiding Tor usage from an ISP, instead of a VPN (as we suggest using if possible). Something to consider is that while bridges may provide adequate censorship circumvention, this is only a *transient* benefit. They do not adequately protect you from your ISP discovering you connected to Tor in the *past* with historical traffic log analysis.

To illustrate this point, consider the following scenario: You connect to Tor via a bridge, and your ISP doesn’t detect it because they are not doing sophisticated analysis of your traffic, so things are working as intended. Now, 4 months go by, and the IP of your bridge has been made public. This is a very common occurrence with bridges, they are discovered and blocked relatively frequently, just not immediately.

Your ISP wants to identify Tor users 4 months ago, and with their limited metadata logging they can see that you connected to an IP address which was later revealed to be a Tor bridge. You have virtually no other excuse to be making such a connection, so the ISP can say with very high confidence that you were a Tor user at that time.

Contrast this with our recommended scenario, where you connect to Tor via a VPN. Say that 4 months later your ISP again wants to identify anybody who used Tor 4 months ago. Their logs almost certainly can identify your traffic 4 months ago, but all they would likely be able to see is that you connected to a VPN’s IP address. This is because most ISPs only retain metadata over long periods of time, not the full contents of the traffic you request. Storing the entirety of your traffic data would require a massive quantity of storage which nearly all threat actors wouldn't possess.

Because your ISP almost certainly is not capturing all packet-level data and storing it forever, they have no way of determining what you connected to with that VPN *after* the fact with an advanced technique like deep packet inspection, and therefore you have plausible deniability.

Therefore, bridges provide the most benefit when circumventing internet censorship *in the moment*, but they are not an adequate substitute for **all** the benefits that using a VPN alongside Tor can provide. Again, this is not advice *against* using Tor bridges, you should just be aware of these limitations while making your decision. In some cases bridges may be the *only* option (if all VPN providers are blocked, for instance), so you can still use them in those circumstances with this limitation in mind.

If you think that a bridge can aid in defending against fingerprinting or other advanced network analysis more than a VPN's encrypted tunnel already can, you always have the option to use a bridge in conjunction with a VPN as well. That way you are still protected by the pluggable transport's obfuscation techniques even if an adversary gains some level of visibility into your VPN tunnel. If you decide to go this route, we recommend connecting to an obfs4 bridge behind your VPN for optimal fingerprinting protection, rather than meek or Snowflake.

It is [possible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) that the [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) pluggable transport currently being trialed may mitigate some of these concerns. We will continue to keep an eye on that technology as it develops.

## Ressources supplémentaires

- [Manuel d'utilisation du navigateur Tor](https://tb-manual.torproject.org)
- [Comment Tor fonctionne - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Services onion Tor - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: Le premier relais de votre circuit est appelé "garde d'entrée" ou "garde". Il s'agit d'un relais rapide et stable qui reste le premier de votre circuit pendant 2 à 3 mois afin de vous protéger contre une attaque connue de rupture d'anonymat. Le reste de votre circuit change avec chaque nouveau site web que vous visitez, et tous ensemble ces relais fournissent les protections complètes de Tor en matière de vie privée. Pour en savoir plus sur le fonctionnement des relais de garde, consultez cet [article de blog](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) et ce [document](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) sur les gardes d'entrée. ([https://support.torproject.org/fr/tbb/tbb-2/](https://support.torproject.org/fr/tbb/tbb-2/))

[^2]: Balise de relai: une (dis-)qualification spéciale des relais pour les positions de circuit (par exemple, "Guard", "Exit", "BadExit"), les propriétés de circuit (par exemple, "Fast", "Stable") ou les rôles (par exemple, "Authority", "HSDir"), tels qu'attribués par les autorités de l'annuaire et définis plus précisément dans la spécification du protocole de l'annuaire. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
