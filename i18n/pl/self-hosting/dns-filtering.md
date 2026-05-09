---
title: DNS Filtering
meta_title: "Self-Hosting DNS Solutions - Privacy Guides"
icon: materiał/dns
description: For our more technical readers, self-hosting a DNS solution can provide filtering for devices not covered by cloud-based DNS solutions.
cover: dns.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-server-network: Service Providers](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: Surveillance Capitalism](../basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

**Self-hosting DNS** is useful for providing [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) on controlled platforms, such as smart TVs and other IoT devices, as no client-side software is needed. Keep in mind that the DNS solutions below are typically restricted to your home or local network unless you set up a more advanced configuration.

## DNS Sinkholes

[**DNS sinkholes**](https://en.wikipedia.org/wiki/DNS_sinkhole) use DNS filtering to block unwanted web content such as advertisements.

### Pi-Hole

<div class="admonition recommendation" markdown>

![Logo Paster](../assets/img/self-hosting/pi-hole.svg){ align=right }

**Pi-hole** is an open-source DNS sinkhole which features a friendly web interface to view insights and manage blocked content. Pi-hole is designed to be hosted on a Raspberry Pi, but it is not limited to such hardware.

[:octicons-home-16: Strona główna](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title="Wesprzyj" }

</div>

### AdGuard Home

<div class="admonition recommendation" markdown>

![Logo AdGuard Home](../assets/img/self-hosting/adguard-home.svg){ align=right }

**AdGuard Home** is an open-source DNS sinkhole which features a polished web interface to view insights and manage blocked content.

[:octicons-home-16: Strona główna](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Kod źródłowy" }

</div>
