---
title: "Tor Overzicht"
icon: 'simple/torproject'
description: Tor is een gratis te gebruiken, gedecentraliseerd netwerk dat is ontworpen om het internet met zoveel mogelijk privacy te gebruiken.
---

Tor is een gratis te gebruiken, gedecentraliseerd netwerk dat is ontworpen om het internet met zoveel mogelijk privacy te gebruiken. Bij correct gebruik maakt het netwerk privé en anoniem browsen en communicatie mogelijk.

## Opbouw van het pad naar Clearnet diensten

"Clearnet diensten" zijn websites die je met elke browser kunt bezoeken, zoals [privacyguides.org](https://www.privacyguides.org). Met Tor kun je anoniem verbinding maken met deze websites door je verkeer door een netwerk te leiden dat bestaat uit duizenden vrijwillig gerunde servers die nodes (of relays) worden genoemd.

Telkens wanneer je [verbinding maakt met Tor](../tor.md), zal het drie nodes kiezen om een pad naar het internet te bouwen; dit pad wordt een "circuit" genoemd

<figure markdown>
  Tor-pad waarop jouw apparaat verbinding maakt met een ingangsknooppunt, middelste knooppunt en uitgangsknooppunt voordat de website van bestemming wordt bereikt](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Tor-pad waarop jouw apparaat verbinding maakt met een ingangsknooppunt, middelste knooppunt en uitgangsknooppunt voordat de website van bestemming wordt bereikt](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Tor-circuitroute</figcaption>
</figure>

Elk van deze knooppunten heeft zijn eigen functie:

### De Entry Node

De entry node, vaak de guard node genoemd, is het eerste knooppunt waarmee uw Tor-client verbinding maakt. De entry node kan uw IP-adres zien, maar het kan niet zien waarmee u verbinding maakt.

In tegenstelling tot de andere nodes, zal de Tor client willekeurig een entry node kiezen en deze twee tot drie maanden aanhouden om je te beschermen tegen bepaalde aanvallen.[^1]

### De Middle Node

De Middle node is het tweede knooppunt waarmee je Tor client verbinding maakt. Het kan zien van welk knooppunt het verkeer afkomstig is - de entry node - en naar welk knooppunt het vervolgens gaat. De middle node kan jouw IP-adres of het domein waarmee je verbinding maakt niet zien.

Voor elk nieuw circuit wordt de middle node willekeurig gekozen uit alle beschikbare Tor-knooppunten.

### De Exit Node

De exit node is het punt waar je webverkeer het Tor netwerk verlaat en wordt doorgestuurd naar de gewenste bestemming. De exit node kan jouw IP-adres niet zien, maar weet wel met welke site hij verbinding maakt.

De exit node wordt willekeurig gekozen uit alle beschikbare Tor-knooppunten met een exit-relaisvlag.[^2]

## Opbouw van het pad naar onion diensten

"Onion Services" (ook wel "verborgen diensten" genoemd) zijn websites die alleen toegankelijk zijn via de Tor-browser. Deze websites hebben een lange willekeurig gegenereerde domeinnaam die eindigt op `.onion`.

Verbinden met een Onion Service in Tor werkt ongeveer hetzelfde als verbinden met een clearnet service, maar je verkeer wordt door een totaal van **zes** nodes geleid voordat het de bestemmingsserver bereikt. Net als voorheen dragen echter slechts drie van deze knooppunten bij tot *jouw* anonimiteit, de andere drie knooppunten beschermen *de Onion Service's* anonimiteit, door het ware IP en de locatie van de website te verbergen op dezelfde manier als Tor Browser die van jou verbergt.

<figure style="width:100%" markdown>
  Tor-pad dat ujouw verkeer via uw drie Tor-knooppunten leidt plus drie extra Tor-knooppunten die de identiteit van de website verbergen](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Tor pad dat jouw verkeer toont dat door uw drie Tor nodes wordt geleid plus drie extra Tor nodes die de identiteit van de website verbergen](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Tor circuit pad met Onion Services. </span></span> Knooppunten in het blauwe <span class="pg-blue">hek behoren tot jouw browser, terwijl knooppunten in het rode <span class="pg-red">hek tot de server behoren, zodat hun identiteit voor jou verborgen blijft.</figcaption>
</figure>

## Encryptie

Tor versleutelt elk netwerk pakket ( in een blok verzonden gegevens) drie keer met de sleutels van het Exit-, middle- en entry node- in die volgorde.

Zodra Tor een circuit heeft gebouwd, verloopt de gegevensoverdracht als volgt:

1. Ten eerste: wanneer het pakket bij het entry node aankomt, wordt de eerste encryptielaag verwijderd. In dit versleutelde pakket vindt de entry een ander versleuteld pakket met het adres van de middle node. De entry node stuurt het pakket dan door naar de middle node.

2. Ten tweede: wanneer de middle node het pakket van de entr node ontvangt, verwijdert het ook een versleutelingslaag met zijn sleutel, en vindt ditmaal een versleuteld pakket met het adres van de exit node. De middle node stuurt het pakket dan door naar de exit node.

3. Ten slotte: wanneer de exit node zijn pakket ontvangt, verwijdert het de laatste versleutelingslaag met zijn sleutel. De exit node ziet hierna bestemmingsadres en stuurt het pakket door naar dat adres.

Hieronder staat een alternatief schema dat het proces weergeeft. Elke node verwijdert zijn eigen versleutelings laag, en wanneer de bestemmings server gegevens terugstuurt, gebeurt hetzelfde proces volledig in omgekeerde richting. Zo weet de exit node niet wie je bent, maar wel van welk knooppunt het afkomstig is, en dus voegt het zijn eigen versleutelings laag toe en stuurt het het terug.

<figure markdown>
  Tor encryption](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Gegevens verzenden en ontvangen via het Tor Netwerk</figcaption>
</figure>

Met Tor kunnen we verbinding maken met een server zonder dat een enkele partij het hele pad kent. De entry node weet wie je bent, maar niet waar je naartoe gaat; De middle node weet niet wie je bent of waar je naartoe gaat; en de exit node weet waar je naartoe gaat, maar niet wie je bent. Omdat de exit node de uiteindelijke verbinding maakt, zal de bestemmingsserver nooit jouw IP-adres kennen.

## Opmerkingen

Hoewel Tor sterke privacygaranties biedt, moet men beseffen dat Tor niet perfect is:

- Goed gefinancierde tegenstanders met de mogelijkheid om passief het meeste netwerkverkeer over de hele wereld te bekijken, hebben een kans om Tor-gebruikers te deanonimiseren door middel van geavanceerde verkeersanalyse. Tor beschermt je ook niet tegen het per ongeluk blootstellen van jezelf, bijvoorbeeld als je te veel informatie over je echte identiteit deelt.
- Tor exit nodes kunnen ook het verkeer controleren dat via hen verloopt. Dit betekent dat verkeer dat niet versleuteld is, zoals gewoon HTTP-verkeer, kan worden geregistreerd en gecontroleerd. Als dergelijk verkeer persoonlijk identificeerbare informatie bevat, kan het u deanonimiseren tot dat exit-knooppunt. Daarom raden wij aan waar mogelijk HTTPS over Tor te gebruiken.

Als je Tor wilt gebruiken om op het web te surfen, raden we alleen de **officiële** Tor Browser aan - deze is ontworpen om vingerafdrukken te voorkomen.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

## Extra bronnen

- [Tor Browser Gebruikershandleiding](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: De entry node in jouw circuit wordt een "bewaker" of "Guard" genoemd. Het is een snel en stabiel node dat gedurende 2-3 maanden de eerste blijft in jouw circuit, ter bescherming tegen een bekende anonimiteitsdoorbrekende aanval. De rest van je circuit verandert bij elke nieuwe website die je bezoekt, en alles bij elkaar bieden deze relays de volledige privacybescherming van Tor. Voor meer informatie over de werking van guard nodes, zie deze [blogpost](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) en [paper](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) over inloopbeveiliging. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2/))

[^2]: Relaysvlag: een speciale (dis-)kwalificatie van relais voor circuitposities (bijvoorbeeld "Guard", "Exit", "BadExit"), circuiteigenschappen (bijvoorbeeld "Fast", "Stable"), of rollen (bijvoorbeeld "Authority", "HSDir"), zoals toegewezen door de directory-autoriteiten en nader gedefinieerd in de specificatie van het directory-protocol. ([https://metrics.torproject.org/glossary.html/](https://metrics.torproject.org/glossary.html))
