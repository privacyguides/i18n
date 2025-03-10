---
title: "Introduction aux DNS"
icon: material/dns
description: Le Système de Nom de Domaine est le "répertoire téléphonique de l'internet", qui aide votre navigateur à trouver le site web qu'il recherche.
---

The [Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System) is the 'phone book of the Internet'. Le DNS traduit les noms de domaine en adresses IP afin que les navigateurs et autres services puissent charger les ressources de l'internet, grâce à un réseau décentralisé de serveurs.

## Qu'est-ce que le DNS ?

Lorsque vous visitez un site web, une adresse numérique est renvoyée. Par exemple, lorsque vous visitez `privacyguides.org`, l'adresse `192.98.54.105` est renvoyée.

Le DNS existe depuis [les premiers jours](https://fr.wikipedia.org/wiki/Domain_Name_System#Histoire) de l'Internet. Les demandes DNS faites à destination et en provenance des serveurs DNS sont généralement **non** chiffrées. Dans un environnement résidentiel, un client se voit attribuer des serveurs par le FAI via [DHCP](https://fr.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol).

Les demandes DNS non chiffrées peuvent être facilement **surveillées** et **modifiées** en transit. Dans certaines régions du monde, les fournisseurs d'accès à Internet reçoivent l'ordre de procéder à un [ filtrage DNS primitif](https://en.wikipedia.org/wiki/DNS_blocking). Lorsque vous demandez l'adresse IP d'un domaine bloqué, le serveur peut ne pas répondre ou répondre avec une adresse IP différente. Le protocole DNS n'étant pas chiffré, le FAI (ou tout opérateur de réseau) peut utiliser [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) pour surveiller les demandes. Les FAI peuvent également bloquer des requêtes sur la base de caractéristiques communes, quel que soit le serveur DNS utilisé.

Ci-dessous, nous discutons et fournissons un tutoriel pour prouver ce qu'un observateur extérieur peut voir en utilisant un DNS normal non chiffré et un [DNS chiffré](#what-is-encrypted-dns).

### DNS non chiffré

1. En utilisant [`tshark`](https://wireshark.org/docs/man-pages/tshark.html) (qui fait partie du projet [Wireshark](https://en.wikipedia.org/wiki/Wireshark) ), nous pouvons surveiller et enregistrer le flux de paquets Internet. Cette commande enregistre les paquets qui répondent aux règles spécifiées :

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. We can then use [`dig`](https://en.wikipedia.org/wiki/Dig_(command)) (Linux, macOS, etc.) or [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) (Windows) to send the DNS lookup to both servers. Les logiciels tels que les navigateurs web effectuent ces recherches automatiquement, à moins qu'ils ne soient configurés pour utiliser un DNS chiffré.

    === "Linux, macOS"

        ```
        dig +noall +answer privacyguides.org @1.1.1.1
        dig +noall +answer privacyguides.org @8.8.8.8
        ```
    === "Windows"

        ```
        nslookup privacyguides.org 1.1.1.1
        nslookup privacyguides.org 8.8.8.8
        ```

3. Next, we want to [analyze](https://wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs) the results:

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

Si vous exécutez la commande Wireshark ci-dessus, le volet supérieur affiche les "[trames](https://en.wikipedia.org/wiki/Ethernet_frame)", et le volet inférieur affiche toutes les données relatives à la trame sélectionnée. Les solutions de filtrage et de surveillance d'entreprise (telles que celles achetées par les gouvernements) peuvent effectuer ce processus automatiquement, sans interaction humaine, et peuvent agréger ces trames pour produire des données statistiques utiles à l'observateur du réseau.

| N° | Temps    | Source    | Destination | Protocole | Longueur | Info                                                                   |
| -- | -------- | --------- | ----------- | --------- | -------- | ---------------------------------------------------------------------- |
| 1  | 0.000000 | 192.0.2.1 | 1.1.1.1     | DNS       | 104      | Standard query 0x58ba A privacyguides.org OPT                          |
| 2  | 0.293395 | 1.1.1.1   | 192.0.2.1   | DNS       | 108      | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3  | 1.682109 | 192.0.2.1 | 8.8.8.8     | DNS       | 104      | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4  | 2.154698 | 8.8.8.8   | 192.0.2.1   | DNS       | 108      | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

Un observateur pourrait modifier n'importe lequel de ces paquets.

## Qu'est-ce qu'un "DNS chiffré" ?

Les DNS cryptés peuvent se référer à un certain nombre de protocoles, les plus courants étant [DNSCrypt](#dnscrypt), [DNS sur TLS](#dns-over-tls-dot), et [DNS sur HTTPS](#dns-over-https-doh).

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) était l'une des premières méthodes de chiffrement des requêtes DNS. DNSCrypt opère sur le port 443 et fonctionne avec les protocoles de transport TCP ou UDP. DNSCrypt has never been submitted to the [Internet Engineering Task Force (IETF)](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force) nor has it gone through the [Request for Comments (RFC)](https://en.wikipedia.org/wiki/Request_for_Comments) process, so it has not been used widely outside a few [implementations](https://dnscrypt.info/implementations). En conséquence, il a été largement remplacé par le plus populaire [DNS sur HTTPS](#dns-over-https-doh).

### DNS sur TLS (DoT)

[**DNS sur TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS) est une autre méthode de chiffrement des communications DNS qui est définie dans [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858). La prise en charge a été mise en œuvre pour la première fois dans Android 9, iOS 14 et sous Linux dans [systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) dans la version 237. Ces dernières années, l'industrie a délaissé DoT au profit de DoH, car DoT est un [protocole complexe](https://dnscrypt.info/faq) dont la conformité au RFC varie d'une implémentation à l'autre. Le DoT fonctionne également sur un port dédié 853 qui peut être facilement bloqué par des pare-feu restrictifs.

### DNS sur HTTPS (DoH)

[**DNS sur HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS)Le DNS over HTTPS, tel que défini dans la [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484), intègre les requêtes dans le protocole [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) et assure la sécurité avec HTTPS. La prise en charge a d'abord été ajoutée dans les navigateurs web tels que Firefox 60 et Chrome 83.

L'implémentation native de DoH est apparue dans iOS 14, macOS 11, Microsoft Windows et Android 13 (cependant, elle ne sera pas activée [par défaut](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144)). Sous Linux la prise en charge sera assurée par [l'implémentation](https://github.com/systemd/systemd/issues/8639) dans systemd donc [l'installation de logiciels tiers est encore nécessaire](../dns.md#encrypted-dns-proxies).

### Prise en charge native des systèmes d'exploitation

#### Android

Android 9 et supérieur prennent en charge DNS via TLS. Les paramètres peuvent être trouvés dans : **Paramètres** &rarr; **Réseau & Internet** &rarr; **DNS Privé**.

#### Appareils Apple

Les dernières versions d'iOS, iPadOS, tvOS et macOS prennent en charge à la fois DoT et DoH. Les deux protocoles sont pris en charge nativement par l'intermédiaire des [profils de configuration](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) ou par l'intermédiaire de [l'API de Paramètres DNS](https://developer.apple.com/documentation/networkextension/dns_settings).

Après l'installation d'un profil de configuration ou d'une application qui utilise l'API des Paramètres DNS, la configuration DNS peut être sélectionnée. Si un VPN est actif, la résolution au sein du tunnel VPN utilisera les paramètres DNS du VPN et non les paramètres de votre système.

Apple ne fournit pas d'interface native pour la création de profils DNS chiffrés. Le [créateur de profil DNS Sécurisé](https://dns.notjakob.com/tool.html) est un outil non officiel permettant de créer vos propres profils DNS chiffrés, mais ils ne seront pas signés. Les profils signés sont préférables ; la signature valide l'origine d'un profil et contribue à garantir l'intégrité des profils. Un label vert "Vérifié" est attribué aux profils de configuration signés. Pour plus d'informations sur la signature de code, voir [A propos de la signature de code](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html).

#### Linux

`systemd-resolved`, que de nombreuses distributions Linux utilisent pour effectuer leurs recherches DNS, ne prend pas encore [en charge DoH](https://github.com/systemd/systemd/issues/8639). Si vous souhaitez utiliser le DNS-over-HTTPS, vous devez installer un proxy tel que [dnscrypt-proxy](../dns.md#dnscrypt-proxy) et le [configurer](https://wiki.archlinux.org/title/Dnscrypt-proxy) pour qu'il prenne toutes les requêtes DNS de votre résolveur système et les transmette via HTTPS.

## Que peut voir un tiers ?

Dans cet exemple, nous allons enregistrer ce qui se passe lorsque nous faisons une requête DoH :

1. Tout d'abord, lancez `tshark`:

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https and host 1.1.1.1
    ```

2. Deuxièmement, faites une requête avec `curl`:

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. Après avoir fait la demande, nous pouvons arrêter la capture de paquets avec <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Analyze the results in Wireshark:

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

Nous pouvons voir l'[établissement de la connexion](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) et la [poignée de main TLS](https://cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake) qui se produit avec toute connexion chiffrée. Lorsque l'on regarde les paquets de "données d'application" qui suivent, aucun d'entre eux ne contient le domaine que nous avons demandé ou l'adresse IP renvoyée.

## Pourquoi **ne devrais-je pas** utiliser un DNS chiffré ?

Dans les endroits où il existe un filtrage (ou une censure) de l'Internet, la visite de ressources interdites peut avoir ses propres conséquences que vous devez prendre en compte dans votre [modèle de menace](../basics/threat-modeling.md). Nous ne suggérons **pas** l'utilisation de DNS chiffrés à cette fin. Utilisez plutôt [Tor](../advanced/tor-overview.md) ou un [VPN](../vpn.md). Si vous utilisez un VPN, vous devez utiliser les serveurs DNS de votre VPN. En utilisant un VPN, vous lui confiez déjà toute votre activité réseau.

Lorsque nous effectuons une recherche DNS, c'est généralement parce que nous voulons accéder à une ressource. Nous examinerons ci-dessous certaines des méthodes susceptibles de divulguer vos activités de navigation, même lorsque vous utilisez un DNS chiffré :

### Adresse IP

Le moyen le plus simple de déterminer l'activité de navigation est de regarder les adresses IP auxquelles vos appareils accèdent. Par exemple, si l'observateur sait que `privacyguides.org` est à `198.98.54.105`, et que votre appareil demande des données à `198.98.54.105`, il y a de fortes chances que vous visitiez Privacy Guides.

Cette méthode n'est utile que lorsque l'adresse IP appartient à un serveur qui n'héberge que quelques sites web. It's also not very useful if the site is hosted on a shared platform (e.g. GitHub Pages, Cloudflare Pages, Netlify, WordPress, Blogger, etc.). Il n'est pas non plus très utile si le serveur est hébergé derrière un [proxy inverse](https://fr.wikipedia.org/wiki/Proxy_inverse), ce qui est très courant actuellement sur Internet.

### Server Name Indication (SNI)

Server Name Indication is typically used when an IP address hosts many websites. Il peut s'agir d'un service comme Cloudflare, ou d'une autre protection contre les [attaques par déni de service](https://fr.wikipedia.org/wiki/Attaque_par_déni_de_service).

1. Recommencez à capturer avec `tshark`. We've added a filter with our IP address, so you don't capture many packets:

    ```bash
    tshark -w /tmp/pg.pcap port 443 et hôte 198.98.54.105
    ```

2. Ensuite, nous visitons [https://privacyguides.org](https://privacyguides.org).

3. Après avoir visité le site web, nous voulons arrêter la capture de paquets avec <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Ensuite, nous voulons analyser les résultats :

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    Nous verrons l'établissement de la connexion, suivi du TLS handshake pour le site web Privacy Guides. Au niveau de l'image 5, vous verrez un "Client Hello".

5. Développez le triangle &#9656; à côté de chaque champ :

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer : Handshake Protocol : Client Hello
        ▸ Handshake Protocol : Client Hello
          ▸ Extension : server_name (len=22)
            ▸ Server Name Indication extension
    ```

6. Nous pouvons voir la valeur SNI qui révèle le site web que nous visitons. La commande `tshark` peut vous donner directement la valeur pour tous les paquets contenant une valeur SNI :

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

Cela signifie que même si nous utilisons des serveurs "DNS chiffrés", le domaine sera probablement divulgué par le SNI. Le protocole [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) intègre le protocole [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello), qui empêche ce type de fuite.

Les gouvernements, en particulier la [Chine](https://zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni) et la [Russie](https://zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni), ont déjà [commencé à le bloquer](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) ou ont exprimé le souhait de le faire. Récemment, la Russie [a commencé à bloquer les sites web étrangers](https://github.com/net4people/bbs/issues/108) qui utilisent le standard [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3). En effet, le protocole [QUIC](https://fr.wikipedia.org/wiki/QUIC) qui fait partie de HTTP/3 exige que `ClientHello` soit également chiffré.

### Online Certificate Status Protocol (OCSP)

Une autre façon dont votre navigateur peut divulguer vos activités de navigation est avec [l'Online Certificate Status Protocol](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol) (protocole de vérification de certificat en ligne). Lors de la visite d'un site Web HTTPS, le navigateur peut vérifier si le [certificat](https://fr.wikipedia.org/wiki/Certificat_%C3%A9lectronique) du site Web a été révoqué. Cela se fait généralement via le protocole HTTP, ce qui signifie qu'il **n'est pas** chiffré.

La requête OCSP contient le certificat "[serial number](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)", qui est unique. Il est envoyé au "OCSP responder" afin de vérifier son statut.

Nous pouvons simuler ce que ferait un navigateur en utilisant la commande [`openssl`](https://fr.wikipedia.org/wiki/OpenSSL).

1. Obtenez le certificat du serveur et utilisez [`sed`](https://fr.wikipedia.org/wiki/Stream_Editor) pour ne garder que la partie importante et l'écrire dans un fichier :

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. Obtenez le certificat intermédiaire. Les [Autorités de certification](https://fr.wikipedia.org/wiki/Autorité_de_certification) (CA) ne signent normalement pas directement un certificat ; elles utilisent ce que l'on appelle un certificat "intermédiaire".

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```

3. Le premier certificat dans `pg_and_intermediate.cert` est en fait le certificat du serveur de l'étape 1. Nous pouvons utiliser à nouveau `sed` pour tout supprimer jusqu'à la première instance de END :

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```

4. Obtenir le répondeur OCSP pour le certificat du serveur :

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```

    Notre certificat montre le répondeur du certificat Lets Encrypt. Si nous voulons voir tous les détails du certificat, nous pouvons utiliser :

    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```

5. Démarrer la capture de paquets :

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```

6. Faites la demande OCSP :

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```

7. Ouvrez la capture :

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```

    Il y aura deux paquets avec le protocole "OCSP" : un "Demande" et un "Réponse". Pour la "Demande", nous pouvons voir le "numéro de série" en développant le triangle &#9656; à côté de chaque champ :

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```

    Pour la "Réponse", nous pouvons également voir le "numéro de série" :

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ responseBytes
        ▸ BasicOCSPResponse
          ▸ tbsResponseData
            ▸ responses: 1 item
              ▸ SingleResponse
                ▸ certID
                  serialNumber
    ```

8. Ou utilisez `tshark` pour filtrer les paquets du numéro de série :

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```

Si l'observateur du réseau dispose du certificat public, qui est accessible au public, il peut faire correspondre le numéro de série à ce certificat et donc déterminer le site que vous visitez à partir de celui-ci. Le processus peut être automatisé et permet d'associer des adresses IP à des numéros de série. Il est également possible de vérifier les journaux de [Certificate Transparency](https://en.wikipedia.org/wiki/Certificate_Transparency) (en anlais) pour le numéro de série.

## Devrais-je utiliser un DNS chiffré ?

Nous avons créé cet organigramme pour décrire quand vous *devriez* utiliser des DNS chiffrés:

``` mermaid
graph TB
    Start[Démarrage] --> anonymous{Essayez-vous<br>d'être<br>anonyme ?}
    anonymous--> | Oui | tor(Utilisez Tor)
    anonymous --> | Non | censorship{Essayez-vous<br>d'eviter la<br>censure ?}
    censorship --> | Oui | vpnOrTor(Utilisez un<br>VPN ou Tor)
    censorship --> | Non | privacy{Essayez-vous de<br>protéger votre vie<br>privée du FAI ?}
    privacy --> | Oui | vpnOrTor
    privacy --> | Non | obnoxious{Votre<br>FAI fait des<br> redirections<br> nuisibles ?}
    obnoxious --> | Oui | encryptedDNS(Utilisez un<br>DNS chiffré<br>tiers)
    obnoxious --> | Non | ispDNS{Votre<br>FAI supporte<br>les DNS<br>chiffrés ?}
    ispDNS --> | Oui | useISP(Utilisez le<br>DNS chiffré<br>de votre FAI)
    ispDNS --> | Non | nothing(Ne faites rien)
```

Encrypted DNS with a third party should only be used to get around redirects and basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences, or you're interested in a provider that does some rudimentary filtering.

[Liste des serveurs DNS recommandés](../dns.md ""){.md-button}

## Qu'est-ce que le DNSSEC ?

[Domain Name System Security Extensions](https://fr.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (extension de SECurité du Système de Nom de Domaine) est une fonctionnalité du DNS qui authentifie les réponses aux recherches de noms de domaine. Il ne fournit pas de protection de la vie privée pour ces recherches, mais empêche les attaquants de manipuler ou d'empoisonner les réponses aux requêtes DNS.

En d'autres termes, le DNSSEC signe numériquement les données afin de garantir leur validité. Afin de garantir une recherche sécurisée, la signature a lieu à chaque niveau du processus de consultation du DNS. Par conséquent, toutes les réponses du DNS sont fiables.

Le processus de signature DNSSEC est similaire à celui d'une personne qui signe un document juridique avec un stylo ; cette personne signe avec une signature unique que personne d'autre ne peut créer, et un expert judiciaire peut examiner cette signature et vérifier que le document a été signé par cette personne. Ces signatures numériques garantissent que les données n'ont pas été altérées.

DNSSEC met en œuvre une politique de signature numérique hiérarchique à travers toutes les couches du DNS. Par exemple, dans le cas d'une consultation de `privacyguides.org`, un serveur DNS racine signe une clé pour le serveur de noms `.org`, et le serveur de noms `.org` signe ensuite une clé pour le serveur de noms faisant autorité `privacyguides.org`.

<small>Adapté de [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) par Google et [DNSSEC : An Introduction](https://blog.cloudflare.com/dnssec-an-introduction) par Cloudflare, tous deux sous licence [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).</small>

## Qu'est-ce que la minimisation QNAME ?

Un QNAME est un "nom qualifié", par exemple `discuss.privacyguides.net`. Auparavant, lors de la résolution d'un nom de domaine, le résolveur DNS demandait à chaque serveur de la chaîne de fournir toutes les informations dont il disposait au sujet de votre requête complète. Dans l'exemple ci-dessous, votre demande pour trouver l'adresse IP de `discuss.privacyguides.net` est demandée à tous les fournisseurs de serveurs DNS :

| Serveur                   | Question posée                                         | Réponse                                                  |
| ------------------------- | ------------------------------------------------------ | -------------------------------------------------------- |
| Serveur racine            | Quelle est l'adresse IP de discuss.privacyguides.net ? | Je ne sais pas, demandez au serveur de .net...           |
| Serveur .net              | Quelle est l'adresse IP de discuss.privacyguides.net ? | Je ne sais pas, demandez au serveur de Privacy Guides... |
| Serveur de Privacy Guides | Quelle est l'adresse IP de discuss.privacyguides.net ? | 5.161.195.190!                                           |

Grâce à la "minimisation QNAME", votre résolveur DNS demande juste assez d'informations pour trouver le serveur suivant dans la chaîne. Dans cet exemple, le serveur racine ne reçoit que les informations nécessaires pour trouver le serveur de noms approprié pour le TLD .net, et ainsi de suite, sans jamais connaître le domaine complet que vous essayez de visiter :

| Serveur                   | Question posée                                             | Réponse                                |
| ------------------------- | ---------------------------------------------------------- | -------------------------------------- |
| Serveur racine            | Quel est le serveur de noms pour .net ?                    | *Fournit le serveur .net*              |
| Serveur .net              | Quel est le serveur de noms de privacyguides.net ?         | *Fournit le serveur de Privacy Guides* |
| Serveur de Privacy Guides | Quel est le serveur de noms de discuss.privacyguides.net ? | Ce serveur !                           |
| Serveur de Privacy Guides | Quelle est l'adresse IP de discuss.privacyguides.net ?     | 5.161.195.190                          |

Bien que ce processus puisse être légèrement plus inefficace, dans cet exemple ni les serveurs de noms de la racine centrale ni les serveurs de noms du TLD ne reçoivent jamais d'informations sur votre requête *complète*, ce qui réduit la quantité d'informations transmises sur vos habitudes de navigation. Une description technique plus détaillée est définie dans [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## Qu'est-ce que le sous-réseau client EDNS (ECS) ?

Le [EDNS Client Subnet](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) est une méthode permettant à un résolveur DNS récursif de spécifier un [sous-réseau](https://fr.wikipedia.org/wiki/Sous-réseau) pour l'hôte ou le [client](https://fr.wikipedia.org/wiki/Client_(informatique)) qui effectue la requête DNS.

Il est destiné à "accélérer" la transmission des données en donnant au client une réponse qui appartient à un serveur proche de lui, comme un [réseau de diffusion de contenu](https://fr.wikipedia.org/wiki/Réseau_de_diffusion_de_contenu), souvent utilisé pour la diffusion de vidéos en continu et pour servir des applications Web JavaScript.

Cette fonction a un coût en termes de confidentialité, car elle fournit au serveur DNS des informations sur la localisation du client, généralement votre réseau IP. Par exemple, si votre adresse IP est `198.51.100.32`, le fournisseur DNS peut partager `198.51.100.0/24` avec le serveur faisant autorité. Certains fournisseurs de DNS rendent ces données anonymes en fournissant une autre adresse IP qui est approximativement proche de votre emplacement.

Si vous avez installé `dig`, vous pouvez tester si votre fournisseur DNS transmet les informations EDNS aux serveurs de noms DNS à l'aide de la commande suivante :

```bash
dig +nocmd -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```

Notez que cette commande contactera Google pour le test et renverra votre IP ainsi que les informations de sous-réseau du client EDNS. Si vous souhaitez tester un autre résolveur DNS, vous pouvez spécifier son IP, pour tester `9.9.9.11` par exemple :

```bash
dig +nocmd @9.9.9.11 -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```

Si les résultats comprennent un deuxième enregistrement TXT edns0-client-subnet (comme indiqué ci-dessous), votre serveur DNS transmet des informations EDNS. L'IP ou le réseau indiqué ci-dessous est l'information précise qui a été communiquée à Google par votre fournisseur de DNS.

```text
o-o.myaddr.l.google.com. 60 IN TXT "198.51.100.32"
o-o.myaddr.l.google.com. 60 IN TXT "edns0-client-subnet 198.51.100.0/24"
;; Query time: 64 msec
;; SERVER: 9.9.9.11#53(9.9.9.11)
;; WHEN: Wed Mar 13 10:23:08 CDT 2024
;; MSG SIZE  rcvd: 130
```
