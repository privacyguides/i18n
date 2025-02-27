---
title: "Veel voorkomende bedreigingen"
icon: 'material/eye-outline'
description: Jouw dreigingsmodel is persoonlijk voor je, maar dit zijn enkele van de dingen die veel bezoekers van deze site belangrijk vinden.
---

In grote lijnen delen wij onze aanbevelingen in in deze algemene categorieën van [bedreigingen](threat-modeling.md) of doelstellingen die voor de meeste mensen gelden. ==U kunt zich bezighouden met geen, een, enkele, of al deze mogelijkheden==, en de instrumenten en diensten die je gebruikt hangen af van wat jouw doelstellingen zijn. You may have specific threats outside these categories as well, which is perfectly fine! Het belangrijkste is dat je inzicht krijgt in de voordelen en tekortkomingen van de middelen die je gebruikt, want vrijwel geen enkel middel beschermt je tegen elke denkbare bedreiging.

<span class="pg-purple">:material-incognito: **Anonymity**</span>
:

Shielding your online activity from your real identity, protecting you from people who are trying to uncover *your* identity specifically.

<span class="pg-red">:material-target-account: **Targeted Attacks**</span>
:

Being protected from hackers or other malicious actors who are trying to gain access to *your* data or devices specifically.

<span class="pg-viridian">:material-package-variant-closed-remove: **Supply Chain Attacks**</span>
:

Typically, a form of <span class="pg-red">:material-target-account: Targeted Attack</span> that centers around a vulnerability or exploit introduced into otherwise good software either directly or through a dependency from a third party.

<span class="pg-orange">:material-bug-outline: **Passive Attacks**</span>
:

Being protected from things like malware, data breaches, and other attacks that are made against many people at once.

<span class="pg-teal">:material-server-network: **Service Providers**</span>
:

Protecting your data from service providers (e.g. with E2EE, which renders your data unreadable to the server).

<span class="pg-blue">:material-eye-outline: **Mass Surveillance**</span>
:

Protection from government agencies, organizations, websites, and services which work together to track your activities.

<span class="pg-brown">:material-account-cash: **Surveillance Capitalism**</span>
:

Protecting yourself from big advertising networks, like Google and Facebook, as well as a myriad of other third-party data collectors.

<span class="pg-green">:material-account-search: **Public Exposure**</span>
:

Limiting the information about you that is accessible online—to search engines or the public.

<span class="pg-blue-gray">:material-close-outline: **Censorship**</span>
:

Avoiding censored access to information or being censored yourself when speaking online.

Sommige van deze bedreigingen kunnen zwaarder wegen dan andere, afhankelijk van jouw specifieke zorgen. For example, a software developer with access to valuable or critical data may be primarily concerned with <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span> and <span class="pg-red">:material-target-account: Targeted Attacks</span>. They will likely still want to protect their personal data from being swept up in <span class="pg-blue">:material-eye-outline: Mass Surveillance</span> programs. Op dezelfde manier is de "gemiddelde consument" misschien in de eerste plaats bezorgd over <span class="pg-green">:material-account-search: Public Exposure</span> van zijn persoonsgegevens, maar moet hij toch op zijn hoede zijn voor op beveiliging gerichte zaken zoals <span class="pg-orange">:material-bug-outline: Passive Attacks</span> zoals malware die zijn apparaten aantast.

## Anonimiteit versus privacy

<span class="pg-purple">:material-incognito: Anonimiteit</span>

Anonimiteit wordt vaak verward met privacy, maar het is een apart concept. Terwijl privacy een reeks keuzes is die je maakt over hoe jouw gegevens worden gebruikt en gedeeld, is anonimiteit het volledig loskoppelen van jouw online activiteiten van jouw echte identiteit.

Voor klokkenluiders en journalisten, bijvoorbeeld, kan een veel extremer bedreigingsmodel gelden, dat volledige anonimiteit vereist. Dat is niet alleen verbergen wat zij doen, welke gegevens zij hebben, en niet gehackt worden door hackers of overheden, maar ook volledig verbergen wie zij zijn. Zij zullen elke vorm van gemak opofferen als dat betekent dat hun anonimiteit, privacy of veiligheid wordt beschermd, want hun leven kan ervan afhangen. De meeste gewone mensen hoeven niet zo ver te gaan.

## Veiligheid en privacy

<span class="pg-orange">:material-bug-outline: Passieve aanvallen</span>

Beveiliging en privacy worden vaak door elkaar gehaald, omdat je beveiliging nodig hebt om enige schijn van privacy te krijgen: Hulpmiddelen gebruiken die privé lijken, is zinloos als ze gemakkelijk door aanvallers kunnen worden misbruikt om jouw gegevens later vrij te geven. Het omgekeerde is echter niet noodzakelijk waar; de veiligste dienst ter wereld *is niet noodzakelijk* privé. Het beste voorbeeld hiervan is het toevertrouwen van gegevens aan Google, dat, gezien zijn omvang, minimale veiligheidsincidenten heeft gekend door vooraanstaande beveiligingsexperts in te zetten om zijn infrastructuur te beveiligen. Hoewel Google een zeer veilige dienst aanbiedt, zouden maar weinigen hun gegevens als privé beschouwen in de gratis consumentenproducten van Google (Gmail, YouTube, enz.).

Wat de beveiliging van toepassingen betreft, weten we over het algemeen niet (en kunnen we soms niet) weten of de software die we gebruiken kwaadaardig is, of dat op een dag zou kunnen worden. Zelfs bij de meest betrouwbare ontwikkelaars is er meestal geen garantie dat hun software geen ernstige kwetsbaarheid bevat die later kan worden uitgebuit.

Om de potentiële schade van kwaadaardige software tot een minimum te beperken, moet u beveiliging door compartimentering toepassen. Dit kan in de vorm van het gebruik van verschillende computers voor verschillende taken, het gebruik van virtuele machines om verschillende groepen van gerelateerde toepassingen te scheiden, of het gebruik van een veilig besturingssysteem met een sterke nadruk op sandboxing van toepassingen en verplichte toegangscontrole.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Mobiele besturingssystemen zijn over het algemeen veiliger dan desktopbesturingssystemen als het gaat om sandboxing van toepassingen.

Apps kunnen geen root-toegang krijgen en hebben alleen toegang tot systeembronnen die je hen verleent. ChromeOS has similar sandboxing capabilities to Android, and macOS has full system permission control (and developers can opt in to sandboxing for applications). Chrome OS heeft vergelijkbare sandboxing-eigenschappen als Android, en macOS heeft volledige controle over systeemtoestemmingen en opt-in (voor ontwikkelaars) sandboxing voor applicaties, maar deze besturingssystemen geven wel identificerende informatie door aan hun respectieve OEM's. Linux heeft de neiging geen informatie door te geven aan systeemverkopers, maar het heeft een slechte bescherming tegen exploits en kwaadaardige apps. This can be mitigated somewhat with specialized distributions which make significant use of virtual machines or containers, such as [Qubes OS](../desktop.md#qubes-os).

</div>

## Attacks against Specific Individuals

<span class="pg-red">:material-target-account: Gerichte aanvallen</span>

Gerichte aanvallen tegen een specifieke gebruiker zijn moeilijker aan te pakken. Gangbare aanvalsmethoden zijn het verzenden van schadelijke documenten via e-mails, het uitbuiten van kwetsbaarheden in de browser en het besturingssysteem, en fysieke aanvallen. Als dit voor je een punt van zorg is, moet je mogelijk meer geavanceerde strategieën ter beperking van bedreigingen toepassen.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

**Webbrowsers**, **e-mailclients**, en **kantoorapplicaties** voeren standaard onvertrouwde code uit die je door derden wordt toegestuurd. Het draaien van meerdere virtuele machines om toepassingen als deze te scheiden van uw hostsysteem en van elkaar is een techniek die je kunt gebruiken om te voorkomen dat een exploit in deze toepassingen de rest van jouw systeem aantast. Technologieën als Qubes OS of Microsoft Defender Application Guard op Windows bieden bijvoorbeeld handige methoden om dit naadloos te doen.

</div>

If you are concerned about **physical attacks** you should use an operating system with a secure verified boot implementation, such as Android, iOS, macOS, or [Windows (with TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). Je moet er ook voor zorgen dat jouw schijf versleuteld is, en dat het besturingssysteem een TPM of Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) of [Element](https://developers.google.com/android/security/android-ready-se) gebruikt voor het beperken van de snelheid waarmee pogingen worden gedaan om de wachtwoordzin voor de versleuteling in te voeren. Je moet voorkomen dat je jouw computer deelt met mensen die je niet vertrouwt, omdat de meeste desktopbesturingssystemen gegevens niet afzonderlijk per gebruiker versleutelen.

## Attacks against Certain Organizations

<span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>

Supply chain attacks are frequently a form of <span class="pg-red">:material-target-account: Targeted Attack</span> towards businesses, governments, and activists, although they can end up compromising the public at large as well.

<div class="admonition example" markdown>
<p class="admonition-title">Example</p>

A notable example of this occurred in 2017 when M.E.Doc, a popular accounting software in Ukraine, was infected with the *NotPetya* virus, subsequently infecting people who downloaded that software with ransomware. NotPetya itself was a ransomware attack which impacted 2000+ companies in various countries, and was based on the *EternalBlue* exploit developed by the NSA to attack Windows computers over the network.

</div>

There are few ways in which this type of attack might be carried out:

1. A contributor or employee might first work their way into a position of power within a project or organization, and then abuse that position by adding malicious code.
2. A developer may be coerced by an outside party to add malicious code.
3. An individual or group might identify a third party software dependency (also known as a library) and work to infiltrate it with the above two methods, knowing that it will be used by "downstream" software developers.

These sorts of attacks can require a lot of time and preparation to perform and are risky because they can be detected, particularly in open source projects if they are popular and have outside interest. Unfortunately they're also one of the most dangerous as they are very hard to mitigate entirely. We would encourage readers to only use software which has a good reputation and makes an effort to reduce risk by:

1. Only adopting popular software that has been around for a while. The more interest in a project, the greater likelihood that external parties will notice malicious changes. A malicious actor will also need to spend more time gaining community trust with meaningful contributions.
2. Finding software which releases binaries with widely-used, trusted build infrastructure platforms, as opposed to developer workstations or self-hosted servers. Some systems like GitHub Actions let you inspect the build script that runs publicly for extra confidence. This lessens the likelihood that malware on a developer's machine could infect their packages, and gives confidence that the binaries produced are in fact produced correctly.
3. Looking for code signing on individual source code commits and releases, which creates an auditable trail of who did what. For example: Was the malicious code in the software repository? Which developer added it? Was it added during the build process?
4. Checking whether the source code has meaningful commit messages (such as [conventional commits](https://conventionalcommits.org)) which explain what each change is supposed to accomplish. Clear messages can make it easier for outsiders to the project to verify, audit, and find bugs.
5. Noting the number of contributors or maintainers a program has. A lone developer may be more susceptible to being coerced into adding malicious code by an external party, or to negligently enabling undesirable behavior. This may very well mean software developed by "Big Tech" has more scrutiny than a lone developer who doesn't answer to anyone.

## Privacy from Service Providers

<span class="pg-teal">:material-server-network: Dienstverleners</span>

Wij leven in een wereld waarin bijna alles met het internet is verbonden. Onze "privé"-berichten, e-mails, sociale interacties worden gewoonlijk ergens op een server opgeslagen. Wanneer je iemand een bericht stuurt, wordt dat bericht opgeslagen op een server en wanneer jouw vriend het bericht wil lezen, zal de server het hem tonen.

Het voor de hand liggende probleem hierbij is dat de dienstverlener (of een hacker die de server heeft gecompromitteerd) in jouw "privé"-gesprekken kan kijken wanneer en hoe hij maar wil, zonder dat je het ooit te weten komt. Dit geldt voor veel gangbare diensten zoals SMS-berichten, Telegram, Discord, enzovoort.

Gelukkig kan end-to-end encryptie dit probleem verlichten door de communicatie tussen jou en de gewenste ontvangers te versleutelen voordat ze zelfs maar naar de server worden verzonden. De vertrouwelijkheid van jouw berichten is gewaarborgd, zolang de dienstverlener geen toegang heeft tot de particuliere sleutels van beide partijen.

<div class="admonition note" markdown>
<p class="admonition-title">Note on Web-based Encryption</p>

In de praktijk varieert de doeltreffendheid van verschillende implementaties van end-to-end encryptie. Toepassingen zoals [Signal](../real-time-communication.md#signal) draaien op het toestel zelf, en elke kopie van de toepassing is hetzelfde voor verschillende installaties. Als de dienstverlener een backdoor in zijn applicatie zou aanbrengen om te proberen jouw privé-sleutels te stelen, zou dat later met reverse engineering kunnen worden opgespoord.

On the other hand, web-based E2EE implementations, such as Proton Mail's web app or Bitwarden's *Web Vault*, rely on the server dynamically serving JavaScript code to the browser to handle cryptography. Een kwaadwillende server zou zich op een specifieke gebruiker kunnen richten en hem kwaadwillige JavaScript-code sturen om zijn encryptiesleutel te stelen, en het zou uiterst moeilijk zijn voor de gebruiker om zoiets ooit op te merken. Zelfs als de gebruiker de poging om zijn sleutel te stelen opmerkt, zou het ongelooflijk moeilijk zijn om te bewijzen dat het de provider is die dit probeert, omdat de server ervoor kan kiezen om verschillende webclients aan verschillende gebruikers aan te bieden.

Wanneer je vertrouwt op end-to-end encryptie, moet je daarom waar mogelijk native applicaties verkiezen boven web clients.

</div>

Zelfs met end-to-end encryptie kunnen dienstverleners je nog steeds profileren op basis van **metadata**, die doorgaans niet beschermd zijn. While the service provider can't read your messages, they can still observe important things, such as whom you're talking to, how often you message them, and when you're typically active. Bescherming van metadata is tamelijk ongewoon, en je zou goed moeten opletten in de technische documentatie van de software die je gebruikt om te zien of er überhaupt sprake is van minimalisering of bescherming van metadata, als dat voor je een punt van zorg is.

## Programma's voor massatoezicht

<span class="pg-blue">:material-eye-outline: Massabewaking</span>

Massasurveillance is een poging om een groot deel van of een gehele bevolking te surveilleren. Het verwijst vaak naar overheidsprogramma's, zoals de programma's [die in 2013 door Edward Snowden werden onthuld](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)).

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France, you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

Regeringen rechtvaardigen massasurveillanceprogramma's vaak als noodzakelijke middelen om terrorisme te bestrijden en misdaad te voorkomen. However, as breaches of human rights, they're most often used to disproportionately target minority groups and political dissidents, among others.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

In the face of Edward Snowden's disclosures of government programs such as [PRISM](https://en.wikipedia.org/wiki/PRISM) and [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), intelligence officials also admitted that the NSA had for years been secretly collecting records about virtually every American’s phone calls — who’s calling whom, when those calls are made, and how long they last. Je moet nagaan welke aspecten van het netwerk jouw tegenstander kan waarnemen, en of je jouw acties kunt ontkennen.

</div>

Ondanks de toenemende massasurveillance in de Verenigde Staten heeft de regering vastgesteld dat massasurveillanceprogramma's zoals Section 215 "weinig unieke waarde" hebben gehad wat betreft het stoppen van daadwerkelijke misdaden of terroristische complotten, waarbij de inspanningen grotendeels de eigen gerichte surveillanceprogramma's van de FBI dupliceren.[^2]

Online, you can be tracked via a variety of methods, including but not limited to:

- Jouw IP-adres
- Browser cookies
- Gegevens die je aan websites verstrekt
- Jouw browser of apparaat vingerafdruk
- Correlatie van betalingsmethodes

If you're concerned about mass surveillance programs, you can use strategies like compartmentalizing your online identities, blending in with other users, or, whenever possible, simply avoiding giving out identifying information.

## Surveillance as a Business Model

<span class="pg-brown">:material-account-cash: Surveillance kapitalisme</span>

> Het surveillance kapitalisme is een economisch systeem dat draait om het vastleggen en verhandelen van persoonsgegevens met als hoofddoel het maken van winst.[^2]

De beste manier om ervoor te zorgen dat jouw gegevens privé blijven, is ze in de eerste plaats gewoon niet openbaar te maken. Het verwijderen van informatie die je online over jezelf vindt, is een van de beste eerste stappen die je kunt nemen om jouw privacy terug te krijgen. Het gebruik van hulpmiddelen zoals content blockers om netwerkverzoeken aan hun servers te beperken, en het lezen van het privacybeleid van de diensten die je gebruikt, kunnen je helpen veel laag hangend fruit te vermijden, maar kunnen je nooit volledig beschermen tegen alle tracking.[^4]

Additionally, even companies outside the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. Als jouw accounts bijvoorbeeld een "privémodus" hebben, schakel deze dan in om ervoor te zorgen dat jouw account niet wordt geïndexeerd door zoekmachines en niet kan worden bekeken door mensen die je niet van tevoren vertrouwd. De sterkste bescherming tegen het verzamelen van bedrijfsgegevens is om jouw gegevens waar mogelijk te versleutelen of te verdoezelen, waardoor het voor verschillende providers moeilijk wordt om gegevens met elkaar te correleren en een profiel op je op te bouwen.

## Beperking van publieke informatie

<span class="pg-green">:material-account-search: Publiekelijke bekendheid</span>

De beste manier om ervoor te zorgen dat jouw gegevens privé blijven, is ze in de eerste plaats gewoon niet openbaar te maken. Het verwijderen van ongewenste informatie die je online over jezelf vindt, is een van de beste eerste stappen die je kunt nemen om jouw privacy te terug te winnen.

- [Bekijk onze gids over het verwijderen van accounts :material-arrow-right-drop-circle:](account-deletion.md)

Online-censuur kan in verschillende mate worden uitgeoefend door actoren zoals totalitaire regeringen, netwerkbeheerders en dienstverleners die de meningsuiting van hun gebruikers en de informatie waartoe zij toegang hebben, willen controleren. Deze pogingen om het internet te filteren zullen altijd onverenigbaar zijn met de idealen van vrije meningsuiting.

Censuur op bedrijfsplatforms komt steeds vaker voor nu platforms als Twitter en Facebook toegeven aan de vraag van het publiek, de druk van de markt en de druk van overheidsinstanties. Overheidsdruk kan bestaan uit heimelijke verzoeken aan bedrijven, zoals het verzoek van het Witte Huis [om een provocerende YouTube-video uit de lucht te halen ](https://www.nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html), of uit openlijke, zoals de Chinese regering die van bedrijven eist dat zij zich houden aan een streng censuurregime.

## Censuur vermijden

<span class="pg-blue-gray">:material-close-outline: Censuur</span>

Censuur online kan (in verschillende mate) worden uitgeoefend door actoren zoals totalitaire regeringen, netwerkbeheerders en dienstverleners. Deze pogingen om de communicatie te controleren en de toegang tot informatie te beperken zullen altijd onverenigbaar zijn met het mensenrecht op vrijheid van meningsuiting.[^5]

Censuur op bedrijfsplatforms komt steeds vaker voor, nu platforms als Twitter en Facebook toegeven aan de vraag van het publiek, de druk van de markt en de druk van overheidsinstanties. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

Mensen die bezorgd zijn over de dreiging van censuur kunnen technologieën als [Tor](../advanced/tor-overview.md) gebruiken om die te omzeilen, en steun verlenen aan censuurbestendige communicatieplatforms als [Matrix](../real-time-communication.md#element), dat geen gecentraliseerde accountautoriteit heeft die willekeurig accounts kan sluiten.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Het ontwijken van censuur kan gemakkelijk zijn, maar het verbergen van het feit dat je het doet kan heel moeilijk zijn.

Je zou moeten overwegen welke aspecten van het netwerk je tegenstander kan waarnemen en of je plausibele ontkenningsmogelijkheden voor je actie hebt. Het gebruik van [versleutelde DNS](../advanced/dns-overview.md#what-is-encrypted-dns) kan je bijvoorbeeld helpen om rudimentaire, DNS-gebaseerde censuursystemen te omzeilen, maar het kan niet echt verbergen wat je bezoekt bij je ISP. Een VPN of Tor kan helpen verbergen wat je bezoekt voor netwerkbeheerders, maar je kunt niet verbergen dat je deze netwerken als gebruikt. Pluggable transports (zoals Obfs4proxy, Meek of Shadowsocks) kunnen je helpen firewalls te omzeilen die gangbare VPN-protocollen of Tor blokkeren, maar jouw pogingen tot omzeiling kunnen nog steeds worden ontdekt door methoden als probing of [deep packet inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection).

</div>

Je moet altijd rekening houden met de risico 's van het proberen om censuur te omzeilen, de mogelijke gevolgen en hoe geavanceerd je tegenstander kan zijn. Je moet voorzichtig zijn met jouw software selectie, en een back-up plan hebben voor het geval je betrapt wordt.

[^1]: United States Privacy and Civil Liberties Oversight Board: [Rapport over het telefoongegevens programma, uitgevoerd onder Section 215](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^2]: Wikipedia: [Surveillance kapitalisme](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^3]: Wikipedia: [*Surveillancekapitalisme*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. Je moet ook andere mitigatietechnieken gebruiken.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
