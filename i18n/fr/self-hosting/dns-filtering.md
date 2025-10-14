---
title: Filtrage DNS
meta_title: "Solutions de DNS autohébergées - Privacy Guides"
icon: material/dns
description: Pour nos lecteurs les plus avancés, autohéberger un DNS peut permettre de mettre en place un filtrage pour les appareils non pris en charge par les solutions DNS basées sur le cloud.
cover: dns.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-server-network: Fournisseurs de services](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: Capitalisme de Surveillance](../basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

**Un DNS autohébergé** peut servir à mettre en place un [filtrage DNS](https://cloudflare.com/learning/access-management/what-is-dns-filtering) sur des appareils tels que les télévisions intelligentes ou autres objets IoT (ou IdO, Internet des Objets), car il ne nécessite aucun logiciel client-side. Les solutions DNS suivantes sont généralement limitées à l'espace de votre maison ou réseau local à moins de paramétrer une configuration plus avancée.

## Gouffre DNS (DNS Sinkholes)

[**Un gouffre DNS**](https://en.wikipedia.org/wiki/DNS_sinkhole) utilise le filtrage DNS pour bloquer du contenu indésirable tel que les publicités.

### Pi-Hole

<div class="admonition recommendation" markdown>

![Logo de Pi-hole](../assets/img/self-hosting/pi-hole.svg){ align=right }

**Pi-Hole** est un gouffre DNS open-source avec une interface web simple qui affiche les informations utiles du gouffre DNS et vous permet de gérer le contenu bloqué. Pi-hole est conçu pour être hébergé sur un Raspberry Pi, mais il n'est pas limité à ce type de matériel.

[:octicons-home-16: Page d'Acceuil](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Code Source" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title="Contribuer" }

</div>

### AdGuard Home

<div class="admonition recommendation" markdown>

![Logo de AdGuard Home](../assets/img/self-hosting/adguard-home.svg){ align=right }

**AdGuard Home** est un gouffre DNS open-source une interface web sophistiquée qui affiche les informations utiles du gouffre DNS et vous permet de gérer le contenu bloqué.

[:octicons-home-16: Page d'Acceuil](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Code Source" }

</div>
