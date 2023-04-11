---
title: VPN-overzicht
icon: material/vpn
description: Virtual Private Networks verleggen het risico van jouw ISP naar een derde partij die je vertrouwt. Je moet deze dingen in gedachten houden.
---

Virtual Private Networks zijn een manier om het einde van jouw netwerk uit te breiden tot een uitgang ergens anders in de wereld. Een ISP kan de stroom van internetverkeer zien dat jouw netwerkaansluitapparaat (d.w.z. modem) binnenkomt en verlaat.

Encryptieprotocollen zoals HTTPS worden algemeen gebruikt op het internet, zodat zij misschien niet precies kunnen zien wat je post of leest, maar zij kunnen wel een idee krijgen van de [domeinen die je opvraagt](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

Een VPN kan helpen omdat het vertrouwen kan verschuiven naar een server ergens anders in de wereld. Het resultaat is dat de ISP dan alleen ziet dat je verbonden bent met een VPN en niets over de activiteit die je erin doorgeeft.

## Moet ik een VPN gebruiken?

**Ja**, tenzij je Tor al gebruikt. Een VPN doet twee dingen: het verschuift de risico's van jouw Internet Service Provider naar zichzelf en het verbergt jouw IP voor een dienst van derden.

VPN's kunnen geen gegevens versleutelen buiten de verbinding tussen jouw toestel en de VPN-server. VPN providers kunnen jouw verkeer zien en wijzigen op dezelfde manier als jouw ISP dat kan. En er is geen enkele manier om het "no logging" beleid van een VPN provider te verifiëren.

Zij verbergen echter wel jouw werkelijke IP-adres voor een dienst van derden, op voorwaarde dat er geen IP-lekken zijn. Ze helpen je op te gaan in anderen en IP-gebaseerde opsporing te beperken.

## Wanneer zou ik geen VPN moeten gebruiken?

Het gebruik van een VPN in gevallen waarin je jouw [bekende identiteit](common-threats.md#common-misconceptions) gebruikt, is waarschijnlijk niet nuttig.

Dit kan spam- en fraudedetectiesystemen alarmeren, zoals wanneer je zou inloggen op de website van uw bank.

## Hoe zit het met encryptie?

De encryptie die door VPN-aanbieders wordt aangeboden, bevindt zich tussen jouw apparaten en hun servers. Het garandeert dat deze specifieke link veilig is. Dit is een stap verder dan het gebruik van onversleutelde proxies, waarbij een tegenstander op het netwerk de communicatie tussen jouw apparaten en deze proxies kan onderscheppen en wijzigen. De versleuteling tussen jouw apps of browsers en de dienstverleners wordt echter niet door deze versleuteling afgehandeld.

Om wat je doet op de websites die je bezoekt privé en veilig te houden, moet je HTTPS gebruiken. Dit houdt jouw wachtwoorden, sessietokens en zoekopdrachten veilig voor de VPN-provider. Overweeg om "HTTPS everywhere" in jouw browser in te schakelen om downgrade-aanvallen zoals [SSL Strip](https://www.blackhat.com/presentations/bh-dc-09/Marlinspike/BlackHat-DC-09-Marlinspike-Defeating-SSL.pdf)tegen te gaan.

## Moet ik versleutelde DNS gebruiken met een VPN?

Tenzij jouw VPN-provider de versleuteldeDNS-servers host, **nee**. Het gebruik van DOH/DOT (of een andere vorm van versleutelde DNS) met servers van derden zal gewoon meer entiteiten toevoegen om te vertrouwen en doet **absoluut niets** om jouw privacy/veiligheid te verbeteren. Jouw VPN-provider kan nog steeds zien welke websites je bezoekt op basis van de IP-adressen en andere methoden. In plaats van alleen jouw VPN-provider te vertrouwen, vertrouwt je nu zowel de VPN-provider als de DNS-provider.

Een veelgehoorde reden om versleutelde DNS aan te bevelen is dat het helpt tegen DNS spoofing. Jouw browser zou echter al moeten controleren op [TLS-certificaten](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) met **HTTPS** en je daarvoor moeten waarschuwen. Als je **HTTPS** niet gebruikt, dan kan een tegenstander nog steeds gewoon iets anders dan jouw DNS-query's wijzigen en zal het eindresultaat weinig anders zijn.

Niet onnodig te zeggen, **dat je geen versleutelde DNS moet gebruiken met Tor**. Dit zou al jouw DNS-verzoeken via één enkel circuit leiden en de gecodeerde DNS-provider in staat stellen je te deanonimiseren.

## Moet ik Tor *gebruiken en* een VPN?

Door een VPN met Tor te gebruiken, creëer je in wezen een permanent toegangsknooppunt, vaak met een geldspoor eraan vast. Dit levert je geen enkel extra voordeel op, terwijl het aanvalsoppervlak van jouw verbinding drastisch wordt vergroot. Als je je Tor gebruik wilt verbergen voor je ISP of je overheid, dan heeft Tor daar een ingebouwde oplossing voor: Tor bridges. [Lees meer over Tor bridges en waarom het gebruik van een VPN niet nodig is](../advanced/tor-overview.md).

## Wat als ik anonimiteit nodig heb?

VPN's kunnen geen anonimiteit bieden. Jouw VPN-provider ziet nog steeds jouw echte IP-adres, en heeft vaak een geldspoor dat direct naar u kan worden teruggeleid. Je kunt niet vertrouwen op een "no logging"-beleid om jouw gegevens te beschermen. Gebruik in plaats daarvan [Tor](https://www.torproject.org/).

## Hoe zit het met VPN providers die Tor nodes aanbieden?

Gebruik die functie niet. Het punt van het gebruik van Tor is dat je je VPN provider niet vertrouwt. Momenteel ondersteunt Tor alleen het [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) protocol. [UDP](https://en.wikipedia.org/wiki/User_Datagram_Protocol) (gebruikt in [WebRTC](https://en.wikipedia.org/wiki/WebRTC) voor het delen van spraak en video, het nieuwe [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3) protocol, enz.), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) en andere pakketten zullen worden gedropt. Om dit te compenseren, routeren VPN-aanbieders gewoonlijk alle niet-TCP-pakketten via hun VPN-server (je eerste hop). Dit is het geval met [ProtonVPN](https://protonvpn.com/support/tor-vpn/). Bovendien, wanneer je deze Tor over VPN setup gebruikt, heb je geen controle over andere belangrijke Tor functies zoals [Isolated Destination Address](https://www.whonix.org/wiki/Stream_Isolation) (een ander Tor circuit gebruiken voor elk domein dat je bezoekt).

De functie moet gezien worden als een handige manier om toegang te krijgen tot het Tor Netwerk, niet om anoniem te blijven. Gebruik voor echte anonimiteit de Tor Browser, TorSocks of een Tor gateway.

## Wanneer zijn VPN's nuttig?

Een VPN kan nog steeds nuttig zijn voor je in een aantal scenario's, zoals:

1. Het verbergen van jouw verkeer van **is alleen** jouw Internet Service Provider.
1. Het verbergen van je downloads (zoals torrents) voor je ISP en anti-piraterij organisaties.
1. Het verbergen van jouw IP-adres voor websites en diensten van derden, zodat IP-gebaseerde tracering wordt voorkomen.

Voor dit soort situaties, of als je een andere dwingende reden hebt, zijn de VPN-providers die we hierboven hebben opgesomd volgens ons de meest betrouwbare. Het gebruik van een VPN-provider betekent echter nog steeds dat je *vertrouwt op* de provider. In vrijwel elk ander scenario zou je een veilige **"by-design"** tool zoals Tor moeten gebruiken.

## Bronnen en verdere lectuur

1. [VPN - a Very Precarious Narrative](https://schub.io/blog/2019/04/08/very-precarious-narrative.html) door Dennis Schubert
1. [Tor Netwerk Overzicht](../advanced/tor-overview.md)
1. [IVPN Privacy Gidsen](https://www.ivpn.net/privacy-guides)
1. ["Heb ik een VPN nodig?"](https://www.doineedavpn.com), een tool ontwikkeld door IVPN om agressieve VPN-marketing uit te dagen door mensen te helpen beslissen of een VPN geschikt is voor hen.

## Verwante VPN-informatie

- [Het probleem met VPN- en privacybeoordelingssites](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites/)
- [Gratis VPN-app onderzoek](https://www.top10vpn.com/free-vpn-app-investigation/)
- [Verborgen VPN-eigenaars onthuld: 101 VPN-producten van slechts 23 bedrijven](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/)
- [Dit Chinese bedrijf zit in het geheim achter 24 populaire apps die gevaarlijke toestemmingen zoeken](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions/)
