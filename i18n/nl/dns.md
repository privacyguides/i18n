---
title: "DNS-resolvers"
icon: material/dns
description: Dit zijn enkele versleutelde DNS-providers die wij aanbevelen, ter vervanging van de standaardconfiguratie van jouw ISP.
---

Versleutelde DNS met servers van derden zou alleen moeten worden gebruikt om simpele [DNS-blokkering](https://en.wikipedia.org/wiki/DNS_blocking) te omzeilen en als je er zeker van bent dat er geen gevolgen zullen zijn. Versleutelde DNS zal je niet helpen jouw surfactiviteiten te verbergen.

[Meer informatie over DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Aanbevolen Providers

| DNS-provider                                                                    | Privacybeleid                                                                                         | Protocollen                                                   | Loggen        | ECS       | Filteren                                                                                                                                                  |
| ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- | ------------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard**](https://adguard.com/en/adguard-dns/overview.html)                 | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                                | Cleartext <br> DoH/3 <br> DoT <br> DNSCrypt | Beetje[^1]    | Nee       | Gebaseerd op server keuze. De filterlijst die wordt gebruikt, is hier te vinden. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setting-up-1.1.1.1/) | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/) | Cleartext <br> DoH/3 <br> DoT                     | Beetje[^2]    | Nee       | Gebaseerd op server keuze.                                                                                                                                |
| [**Control D**](https://controld.com/free-dns)                                  | [:octicons-link-external-24:](https://controld.com/privacy)                                           | Cleartext <br> DoH/3 <br> DoT <br> DoQ      | Optioneel[^3] | Nee       | Gebaseerd op server keuze.                                                                                                                                |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls)      | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy/)                    | DoH <br> DoT                                            | Geen[^4]      | Nee       | Gebaseerd op server keuze. De filterlijst die wordt gebruikt, is hier te vinden. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    |
| [**NextDNS**](https://www.nextdns.io)                                           | [:octicons-link-external-24:](https://www.nextdns.io/privacy)                                         | Cleartext <br> DoH/3 <br> DoT                     | Optioneel[^5] | Optioneel | Gebaseerd op server keuze.                                                                                                                                |
| [**Quad9**](https://quad9.net)                                                  | [:octicons-link-external-24:](https://quad9.net/privacy/policy/)                                      | Cleartext <br> DoH <br> DoT <br> DNSCrypt   | Beetje[^6]    | Optioneel | Gebaseerd op server keuze, malware blokkering is standaard.                                                                                               |

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaard criteria](about/criteria.md) hebben wij een duidelijke reeks eisen opgesteld om objectieve aanbevelingen te kunnen doen. We raden je aan deze lijst goed door te lezen voordat je een project kiest en je eigen onderzoek te doen om er zeker van te zijn dat het de juiste keuze voor jou is.

!!! example "Deze sectie is nieuw"

    We werken aan het vaststellen van gedefinieerde criteria voor elk deel van onze site, en dit kan onderhevig zijn aan verandering. Als je vragen hebt over onze criteria, stel ze dan [op ons forum](https://discuss.privacyguides.net/latest) en ga er niet van uit dat we iets niet in overweging hebben genomen bij het opstellen van onze aanbevelingen als het hier niet vermeld staat. Er zijn veel factoren die worden overwogen en besproken wanneer wij een project aanbevelen, en het documenteren van elke factor is een werk in uitvoering.

- Moet [DNSSEC](advanced/dns-overview.md#what-is-dnssec) ondersteunen.
- [QNAME Minimalisatie](advanced/dns-overview.md#what-is-qname-minimization).
- Toestaan dat [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) kan worden uitgeschakeld.
- Voorkeur voor [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) ondersteuning of geo-steering ondersteuning.

## Ondersteuning voor besturingssystemen

### Android

Android 9 en hoger ondersteunen DNS over TLS. De instellingen kunnen worden gevonden in: **Instellingen** &rarr; **Netwerk & internet** &rarr; **Privé-DNS**.

### Apple apparaten

De nieuwste versies van iOS, iPadOS, tvOS en macOS ondersteunen zowel DoT als DoH. Beide protocollen worden ondersteund via [configuratieprofielen](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) of via de [DNS Settings API](https://developer.apple.com/documentation/networkextension/dns_settings).

Na installatie van een configuratieprofiel of een app die gebruik maakt van de DNS Settings API, kan de DNS-configuratie worden geselecteerd. Als een VPN actief is, zal de resolutie binnen de VPN-tunnel de DNS-instellingen van het VPN gebruiken en niet je systeembrede instellingen.

#### Ondertekende Profielen

Apple biedt geen native interface voor het maken van versleutelde DNS-profielen. [Secure DNS profile creator](https://dns.notjakob.com/tool.html) is een onofficiële tool voor het maken van je eigen versleutelde DNS-profielen, echter worden deze niet ondertekend. Ondertekende profielen hebben de voorkeur; ondertekening valideert de oorsprong van een profiel en helpt de integriteit van de profielen te waarborgen. Een groen "Geverifieerd" label wordt gegeven aan ondertekende configuratieprofielen. Voor meer informatie over het ondertekenen van codes, zie [Over het ondertekenen van codes](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html). **Ondertekende profielen** worden aangeboden door [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io), en [Quad9](https://www.quad9.net/news/blog/ios-mobile-provisioning-profiles/).

!!! info

    `systemd-resolved`, die veel Linux-distributies gebruiken om hun DNS lookups te doen, [ondersteunt DoH nog niet](https://github.com/systemd/systemd/issues/8639). Als je DoH wilt gebruiken, moet je een proxy installeren zoals [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) en [configureren](https://wiki.archlinux.org/title/Dnscrypt-proxy) om alle DNS-query's van je systeem-resolver te nemen en ze over HTTPS door te sturen.

## Versleutelde DNS-proxy

Versleutelde DNS-proxy software biedt een lokale proxy voor de [onversleutelde DNS](advanced/dns-overview.md#unencrypted-dns)-resolver om naar door te sturen. Meestal wordt het gebruikt op platformen die [versleutelde DNS](advanced/dns-overview.md#what-is-encrypted-dns)niet ondersteunen.

### RethinkDNS

!!! recommendation

    ![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
    !RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }
    
    **RethinkDNS** is een open-source Android client met ondersteuning voor [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) en DNS-proxy samen met het cachen van DNS antwoorden, lokaal loggen van DNS-queries en kan ook gebruikt worden als firewall.
    
    [:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacybeleid" }
    [:octicons-info-16:](https://docs.rethinkdns.com/){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Broncode" }
    
    ??? downloads "Downloaden"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
        - [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

### dnscrypt-proxy

!!! recommendation

    ![dnscrypt-proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }
    
    **dnscrypt-proxy** is een DNS-proxy met ondersteuning voor [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), en [Geanonimiseerde DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).
    
    !!! warning "De geanonimiseerde DNS-functie anonimiseert [**niet**](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) ander netwerkverkeer."
    
    [:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Broncode" }
    [:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Bijdrage leveren }
    
    ??? downloads "Downloaden"
    
        - [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
        - [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
        - [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

## Zelf gehoste oplossingen

Een zelf gehoste DNS-oplossing is handig voor het bieden van filtering op gecontroleerde platforms, zoals Smart TV's en andere IoT-apparaten, omdat er geen client-side software nodig is.

### AdGuard Home

!!! recommendation

    ![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }
    
    **AdGuard Home** is een open-source [DNS-sinkhole](https://wikipedia.org/wiki/DNS_sinkhole) die gebruik maakt van [DNS filtering](https://www.cloudflare.com/learning/access-management/what-is-dns-filtering/) om ongewenste webinhoud, zoals advertenties, te blokkeren.
    
    AdGuard Home beschikt over een vriendelijke webinterface om inzicht te krijgen en geblokkeerde inhoud te beheren.
    
    [:octicons-home-16: Homepage](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Privacybeleid" }
    [:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Broncode" }

### Pi-hole

!!! recommendation

    ![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }
    
    **Pi-hole** is een open-source [DNS-sinkhole](https://wikipedia.org/wiki/DNS_sinkhole) die [DNS filtering](https://www.cloudflare.com/learning/access-management/what-is-dns-filtering/) gebruikt om ongewenste webinhoud, zoals advertenties, te blokkeren.
    
    Pi-hole is ontworpen om te worden gehost op een Raspberry Pi, maar het is niet beperkt tot dergelijke hardware. De software beschikt over een vriendelijke webinterface om inzicht te krijgen en geblokkeerde inhoud te beheren.
    
    [:octicons-home-16: Homepage](https://pi-hole.net/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://pi-hole.net/privacy/){ .card-link title="Privacybeleid" }
    [:octicons-info-16:](https://docs.pi-hole.net/){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Broncode" }
    [:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Bijdrage leveren }

[^1]: AdGuard slaat geaggregeerde prestatiecijfers van hun DNS-servers op, namelijk het aantal volledige verzoeken aan een bepaalde server, het aantal geblokkeerde verzoeken, en de snelheid waarmee verzoeken worden verwerkt. Zij houden ook de database bij van domeinen die in de laatste 24 uur zijn aangevraagd. "We hebben deze informatie nodig om nieuwe trackers en bedreigingen te identificeren en te blokkeren." "We houden ook bij hoe vaak bepaalde trackers geblokkeerd zijn. We hebben deze informatie nodig om verouderde regels uit onze filters te verwijderen." [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare verzamelt en bewaart alleen de beperkte DNS-querygegevens die naar de 1.1.1.1 resolver worden gestuurd. De 1.1.1.1 resolver dienst logt geen persoonsgegevens, en het grootste deel van de beperkte niet-persoonlijk identificeerbare query-gegevens wordt slechts 25 uur bewaard. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/)
[^3]: Control D logt alleen voor Premium resolvers met aangepaste DNS-profielen. Gratis resolvers loggen geen gegevens. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: De DNS-service van Mullvad is beschikbaar voor zowel abonnees als niet-abonnees van Mullvad VPN. Hun privacybeleid beweert expliciet dat zij op geen enkele manier DNS-verzoeken loggen. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy/)
[^5]: NextDNS kan inzichten en loggingfuncties bieden op een opt-in basis. Je kan retentietijden en opslaglocaties kiezen voor de logs die je wilt bewaren. Als er niet specifiek om gevraagd wordt, worden er geen gegevens gelogd. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: Quad9 verzamelt sommige gegevens ten behoeve van de monitoring van en reactie op bedreigingen. Die gegevens kunnen vervolgens opnieuw worden gemengd en gedeeld, bijvoorbeeld ten behoeve van veiligheidsonderzoek. Quad9 verzamelt of registreert geen IP-adressen of andere gegevens die zij als persoonlijk identificeerbaar beschouwen. [https://www.quad9.net/privacy/policy/](https://www.quad9.net/privacy/policy/)
