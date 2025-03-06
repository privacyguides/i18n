---
title: "Häufige Bedrohungen"
icon: 'material/eye-outline'
description: Deine persönliche Bedrohungsanalyse kannst nur du selber durchführen. Vielen Besuchern dieser Webseite sind aber folgende Dinge wichtig.
---

Wir ordnen unsere Empfehlungen nach [Bedrohungen](threat-modeling.md) beziehungsweise Zielen, die für die meisten Menschen gelten. ==Dich können keine, eine, einige oder alle dieser Themen betreffen==, und du solltest die von dir eingesetzten Werkzeuge und Dienste von deinen Zielen abhängig machen. Du kannst auch spezifische Bedrohungen außerhalb dieser Kategorien haben, das ist völlig in Ordnung! Wichtig ist, dass du die Vorteile und Schwächen der von dir gewählten Werkzeuge kennst, denn praktisch keines davon schützt dich vor jeder Bedrohung.

<span class="pg-purple">:material-incognito: **Anonymität**</span>
:

Schütze deine Online-Aktivitäten von deiner realen Identität, um dich vor Personen zu schützen, die gezielt versuchen *deine* Identität aufzudecken.

<span class="pg-red">:material-target-account: **Targeted Attacks**</span>
:

Schutz vor Hackern oder anderen böswilligen Akteuren, die versuchen, sich Zugang zu *deinen * Daten oder Geräten zu verschaffen.

<span class="pg-viridian">:material-package-variant-closed-remove: **Supply-Chain-Attacke**</span>
:

Typically, a form of <span class="pg-red">:material-target-account: Targeted Attack</span> that centers around a vulnerability or exploit introduced into otherwise good software either directly or through a dependency from a third party.

<span class="pg-orange">:material-bug-outline: **Passive Angriffe**</span>
:

Schutz vor Malware, Datenleaks und anderen Angriffen, die sich gegen viele Menschen gleichzeitig richten.

<span class="pg-teal">:material-server-network: **Diensteanbieter**</span>
:

Schutz deiner Daten vor Dienstleistern (z. B. mit E2EE, welche deine Daten für den Server unlesbar macht).

<span class="pg-blue">:material-eye-outline: **Massenüberwachung**</span>
:

Schutz vor Regierungsbehörden, Organisationen, Webseiten und Diensten, die zusammenarbeiten, um deine Aktivitäten zu verfolgen.

<span class="pg-brown">:material-account-cash: **Überwachungskapitalismus**</span>
:

Schutz vor großen Werbenetzwerken wie Google und Facebook sowie vor einer Vielzahl anderer Datensammler.

<span class="pg-green">:material-account-search: **Public Exposure**</span>
:

Begrenzung der Informationen über dich online—für Suchmaschinen oder die Öffentlichkeit.

<span class="pg-blue-gray">:material-close-outline: **Zensur**</span>
:

Vermeidung des zensierten Zugriffs auf Informationen oder der eigenen Zensur, wenn man sich online äußert.

Einige dieser Bedrohungen können für dich wichtiger sein als andere, je nach deinen spezifischen Anliegen. Ein Softwareentwickler, der Zugang zu wertvollen oder kritischen Daten hat, könnte sich beispielsweise in erster Linie über <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain-Angriffe</span> und <span class="pg-red">:material-target-account: Targeted Attacks</span> Sorgen machen. Sie werden wahrscheinlich immer noch ihre persönlichen Daten davor schützen wollen, von <span class="pg-blue">:material-eye-outline: Massenüberwachungsprogrammen</span> erfasst zu werden. Ebenso sind viele Menschen vielleicht in erster Linie besorgt über die <span class="pg-green">:material-account-search: Öffentliche Bloßstellung</span> ihrer persönlichen Daten, sollten aber trotzdem auf sicherheitsrelevante Probleme achten, wie z. B. <span class="pg-orange">:material-bug-outline: Passive Angriffe</span> - wie Malware, die ihre Geräte befallen.

## Anonymität vs. Datenschutz

<span class="pg-purple">:material-incognito: Anonymität</span>

Anonymität wird oft mit Datenschutz in einen Topf geworfen, es sind aber unterschiedliche Konzepte. Während Datenschutz aus einer Reihe von Entscheidungen besteht, die du über die Verwendung und Weitergabe deiner Daten triffst, bedeutet Anonymität die vollständige Trennung deiner Online-Aktivitäten von deiner wirklichen Identität.

Für Whistleblower und Journalisten beispielsweise kann ein viel extremeres Bedrohungsmodell gelten, das völlige Anonymität erfordert. Das bedeutet nicht nur, dass sie verbergen, was sie tun, welche Daten sie haben und dass sie nicht von böswilligen Akteuren oder Regierungen gehackt werden, sondern auch, dass sie völlig verbergen, wer sie sind. Sie sind oft bereit, jede Art von Bequemlichkeit zu opfern, wenn es darum geht, ihre Anonymität, Privatsphäre oder Sicherheit zu schützen, weil ihr Leben davon abhängen könnte. Die meisten Menschen brauchen so weit nicht zu gehen.

## Sicherheit und Datenschutz

<span class="pg-orange">:material-bug-outline: Passive Angriffe</span>

Sicherheit und Datenschutz werden auch oft verwechselt, weil man Sicherheit braucht, um überhaupt einen Anschein von Datenschutz zu erhalten: Der Einsatz von Tools - selbst wenn sie von vornherein privat sind - ist sinnlos, wenn sie leicht von Angreifern ausgenutzt werden können, die später Ihre Daten veröffentlichen. Das Gegenteil ist jedoch nicht unbedingt der Fall: Der sicherste Dienst der Welt *ist nicht unbedingt* privat. Das beste Beispiel hierfür ist das Anvertrauen von Daten an Google, das in Anbetracht seiner Größe nur wenige Sicherheitsvorfälle zu verzeichnen hatte, weil es branchenführende Sicherheitsexperten mit der Sicherung seiner Infrastruktur beschäftigt. Obwohl Google sehr sichere Dienste anbietet, würden nur sehr wenige Menschen ihre Daten in den kostenlosen Verbraucherprodukten von Google (Gmail, YouTube usw.) als privat betrachten

Wenn es um die Sicherheit von Anwendungen geht, wissen wir in der Regel nicht (und können auch manchmal gar nicht wissen), ob die von uns verwendete Software bösartig ist oder eines Tages bösartig werden könnte. Selbst bei den vertrauenswürdigsten Entwicklern gibt es im Allgemeinen keine Garantie dafür, dass ihre Software nicht eine schwerwiegende Sicherheitslücke aufweist, die später ausgenutzt werden könnte.

Um den Schaden, den eine bösartige Software anrichten *könnte*, zu minimieren, solltest du Sicherheit durch Kompartimentalisierung (Abschottung/Isolierung bestimmter Bereiche) einsetzen. Dies kann zum Beispiel durch die Verwendung verschiedener Computer für verschiedene Aufgaben, durch die Verwendung virtueller Maschinen zur Trennung verschiedener Gruppen zusammengehöriger Anwendungen oder durch die Verwendung eines sicheren Betriebssystems mit Schwerpunkt auf Anwendungs-Sandboxing und obligatorischer Zugriffskontrolle geschehen.

<div class="admonition tip" markdown>
<p class="admonition-title">Tipp</p>

Mobile Betriebssysteme verfügen im Allgemeinen über eine bessere Sandbox für Anwendungen als Desktop-Betriebssysteme: Apps können keinen Root-Zugriff erhalten und benötigen eine Genehmigung für den Zugriff auf Systemressourcen.

Desktop-Betriebssysteme hinken im Allgemeinen bei ordnungsgemäßen Sandboxing-Technik hinterher. ChromeOS verfügt über ähnliche Sandboxing-Funktionen wie Android, und macOS bietet eine vollständige Kontrolle der Systemberechtigungen (und Entwickler können sich für Sandboxing von Anwendungen entscheiden). Allerdings übermitteln diese Betriebssysteme identifizierende Informationen an ihre jeweiligen OEMs. Linux tendiert dazu, keine Informationen an Systemanbieter weiterzugeben, bietet aber nur einen geringen Schutz gegen Exploits und bösartige Anwendungen. Dies kann mit spezialisierten Distributionen, die in erheblichem Umfang virtuelle Maschinen oder Container verwenden, wie [Qubes OS](../desktop.md#qubes-os), etwas abgemildert werden.

</div>

## Angriffe auf bestimmte Personen

<span class="pg-red">:material-target-account: Targeted Attacks</span>

Gezielte Angriffe auf eine bestimmte Person sind schwieriger zu bewältigen. Zu den üblichen Angriffen gehören das Versenden bösartiger Dokumente per E-Mail, das Ausnutzen von Sicherheitslücken (z. B. in Browsern und Betriebssystemen) und physische Angriffe. Wenn dies für dich eine Gefahr darstellt, solltest du fortschrittlichere Strategien zur Bedrohungsabwehr einsetzen.

<div class="admonition tip" markdown>
<p class="admonition-title">Tipp</p>

In **Webbrowsern**, **E-Mail-Clients** und **Büroanwendungen** wird in der Regel nicht vertrauenswürdiger Code ausgeführt, der dir von Dritten übermittelt wird. Der Einsatz mehrerer virtueller Maschinen — um Anwendungen wie diese von deinem Hostsystem und voneinander zu trennen - ist eine Technik, mit der du die Gefahr verringern kannst, dass ein Exploit in diesen Anwendungen den Rest deines Systems gefährdet. Beispielsweise bieten Technologien wie Qubes OS oder Microsoft Defender Application Guard unter Windows bequeme Methoden, dies zu tun.

</div>

Wenn du dir Sorgen über **physische Angriffe** machst, solltest du ein Betriebssystem mit einer sicheren verifizierten Boot-Implementierung verwenden, wie Android, iOS, macOS oder [Windows (mit TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). Du solltest auch sicherstellen, dass dein Laufwerk verschlüsselt ist und dass das Betriebssystem ein TPM oder Secure-[Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) oder -[Element](https://developers.google.com/android/security/android-ready-se) verwendet, um die Versuche zur Eingabe der Verschlüsselungspassphrase zu begrenzen. Du solltest es auch vermeiden, deinen Computer mit Personen zu teilen, denen du nicht vertraust, da die meisten Desktop-Betriebssysteme die Daten nicht separat pro Benutzer verschlüsseln.

## Angriffe auf bestimmte Organisationen

<span class="pg-viridian">:material-package-variant-closed-remove: Supply-Chain-Attacke</span>

Supply chain attacks are frequently a form of <span class="pg-red">:material-target-account: Targeted Attack</span> towards businesses, governments, and activists, although they can end up compromising the public at large as well.

<div class="admonition example" markdown>
<p class="admonition-title">Beispiel</p>

Ein bemerkenswertes Beispiel hierfür ereignete sich 2017, als M.E.Doc, eine in der Ukraine beliebte Buchhaltungssoftware, mit dem Virus *NotPetya* infiziert wurde und anschließend Personen, die diese Software heruntergeladen hatten, mit Ransomware infizierte. NotPetya selbst war ein Ransomware-Angriff, der mehr als 2000 Unternehmen in verschiedenen Ländern betraf und auf dem von der NSA entwickelten Exploit *EternalBlue* basierte, um Windows-Computer über das Netzwerk anzugreifen.

</div>

Es gibt ein paar Möglichkeiten, wie ein solcher Angriff durchgeführt werden kann:

1. Ein mitwirkende oder angestellte Person könnte sich zunächst eine Machtposition innerhalb eines Projekts oder einer Organisation erarbeiten und diese dann missbrauchen, indem er bösartigen Code einfügt.
2. Ein Entwickler kann von einer außenstehenden Partei gezwungen werden, bösartigen Code hinzuzufügen.
3. Eine Einzelperson oder eine Gruppe könnte eine Software-Abhängigkeit von Dritten (auch als Bibliothek bekannt) identifizieren und mit den beiden oben genannten Methoden infiltrieren, da sie weiß, dass sie von „downstream“ Software-Entwicklern verwendet wird.

Diese Art von Angriffen kann viel Zeit und Vorbereitung erfordern und ist riskant, weil sie entdeckt werden kann, insbesondere bei Open-Source-Projekten, wenn sie populär sind und Interesse von außen haben. Leider gehören sie auch zu den gefährlichsten, da sie nur sehr schwer vollständig zu entschärfen sind. Wir empfehlen der Leserschaft, nur Software zu verwenden, die einen guten Ruf hat und sich bemüht, das Risiko zu minimieren, indem:

1. Nur populäre Software verwendet wird, die schon seit einiger Zeit existiert. Je mehr Interesse an einem Projekt besteht, desto höher ist die Wahrscheinlichkeit, dass externe Parteien bösartige Änderungen bemerken. Ein bösartiger Akteur muss auch mehr Zeit aufwenden, um das Vertrauen der Community durch sinnvolle Beiträge zu gewinnen.
2. Software verwendet wird, die Binaries mit weit verbreiteten, vertrauenswürdigen Build-Infrastruktur-Plattformen veröffentlicht, anstatt auf Entwickler-Workstations oder selbst gehosteten Servern. Einige Systeme wie GitHub Actions ermöglichen es, das Build-Skript öffentlich zu überprüfen, um zusätzliches Vertrauen zu gewinnen. Dies verringert die Wahrscheinlichkeit, dass Malware auf einem Entwickler-Rechner die Pakete infizieren kann, und gibt die Gewissheit, dass die produzierten Binaries tatsächlich korrekt produziert wurden.
3. Nach Code-Signierung auf individuellen Quellcode-Commits und -Releases gesucht wird, die eine überprüfbare Spur davon erstellen, wer was getan hat. Zum Beispiel: War der bösartige Code im Software-Repository? Welcher Entwickler hat ihn hinzugefügt? Wurde er während des Build-Prozesses hinzugefügt?
4. Überprüft wird, ob der Quellcode sinnvolle Commit-Messages (wie [konventionelle Commits](https://conventionalcommits.org)) enthält, die erklären, was jede Änderung erreichen soll. Klare Messages können es Außenstehenden erleichtern, das Projekt zu überprüfen, zu auditen und Fehler zu finden.
5. Die Anzahl der Mitwirkenden oder Maintainer eines Programms beachtet wird. Ein einzelner Entwickler ist möglicherweise anfälliger dafür, von einer externen Partei dazu gezwungen zu werden, bösartigen Code hinzuzufügen, oder fahrlässig unerwünschtes Verhalten zu ermöglichen. Dies kann sehr wohl bedeuten, dass Software, die von „Big Tech“ entwickelt wird, einer genaueren Prüfung unterzogen wird als ein einzelner Entwickler, der niemandem Rechenschaft schuldet.

## Privatsphäre vor Dienstanbietern

<span class="pg-teal">:material-server-network: Diensteanbieter</span>

Wir leben in einer Welt, in der fast alles mit dem Internet verbunden ist. Unsere „privaten“ Nachrichten, E-Mails und sozialen Interaktionen werden meist irgendwo auf einem Server gespeichert. Wenn du jemandem eine Nachricht schickst, wird diese in der Regel auf einem Server gespeichert, und wenn dein Freund die Nachricht lesen möchte, zeigt der Server sie ihm an.

Das offensichtliche Problem dabei ist, dass der Dienstanbieter (oder ein Hacker, der in den Server eingedrungen ist) auf deine Unterhaltungen zugreifen kann, wann und wie er will, ohne dass du es je erfährst. Dies gilt für viele gängige Dienste wie SMS-Nachrichten, Telegram und Discord.

Glücklicherweise kann E2EE dieses Problem lindern, indem es die Kommunikation zwischen dir und den gewünschten Empfängern verschlüsselt, bevor sie überhaupt an den Server gesendet wird. Die Vertraulichkeit deiner Nachrichten ist gewährleistet, vorausgesetzt, der Dienstanbieter hat keinen Zugang zu den privaten Schlüsseln der beiden Parteien.

<div class="admonition note" markdown>
<p class="admonition-title">Hinweis zur webbasierten Verschlüsselung</p>

In der Praxis ist die Effektivität der verschiedenen E2EE-Implementierungen unterschiedlich. Anwendungen wie [Signal](../real-time-communication.md#signal) werden nativ auf deinem Gerät ausgeführt, und jede Kopie der Anwendung ist bei verschiedenen Installationen identisch. Wenn ein solcher Dienstanbieter eine [Hintertür](https://de.wikipedia.org/wiki/Backdoor) in seine Anwendung einbauen würde, um deine privaten Schlüssel zu stehlen, könnte dies später mit [Reverse Engineering](https://de.wikipedia.org/wiki/Reverse_engineering) entdeckt werden.

Auf der anderen Seite, bei webbasierten E2EE-Implementierungen, wie der Webanwendung von Proton Mail oder dem *Web Vault* von Bitwarden muss der Server dem Browser dynamisch JavaScript-Code zur Verfügung stellen, um die Kryptografie zu handhaben. Ein bösartiger Server kann dich ins Visier nehmen und dir bösartigen JavaScript-Code senden, um deine Verschlüsselungscode zu stehlen (und das wäre extrem schwer zu bemerken). Da der Server verschiedene Web-Clients für verschiedene Personen bereitstellen kann, wäre es - selbst wenn du den Angriff bemerkst -, unglaublich schwierig, die Schuld des Anbieters zu beweisen.

Daher solltest du, wann immer möglich, native Anwendungen anstelle von Webclients verwenden.

</div>

Selbst mit E2EE können Dienstanbieter immer noch Profile von dir auf der Grundlage von **Metadaten** erstellen, die normalerweise nicht geschützt sind. While the service provider can't read your messages, they can still observe important things, such as whom you're talking to, how often you message them, and when you're typically active. Der Schutz von Metadaten ist eher unüblich, und wenn es in deinem [Bedrohungsmodell](threat-modeling.md) vorkommt, solltest du die technische Dokumentation der Software, die du verwendest, genau prüfen, um zu sehen, ob es eine Minimierung oder einen Schutz von Metadaten gibt.

## Massenüberwachungsprogramme

<span class="pg-blue">:material-eye-outline: Massenüberwachung</span>

Unter Massenüberwachung versteht man die aufwändige Überwachung des "Verhaltens, vieler Aktivitäten oder Informationen" einer gesamten Bevölkerung (oder eines wesentlichen Teils davon).[^1] Der Begriff bezieht sich häufig auf Regierungsprogramme, wie die [von Edward Snowden im Jahr 2013 enthüllten](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)) Programme. Sie kann aber auch von Unternehmen durchgeführt werden, entweder im Auftrag von Regierungsbehörden oder auf eigene Initiative.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas der Überwachung</p>

Wenn du mehr über Überwachungsmethoden und deren Umsetzung in US-Städten erfahren möchtest, kannst du die den [Atlas of Surveillance](https://atlasofsurveillance.org) der [Electronic Frontier Foundation](https://eff.org) ansehen.

Für Frankreich kannst du einen Blick auf die [Technopolice Website](https://technopolice.fr/villes) werfen, die von dem gemeinnützigen Verein La Quadrature du Net betrieben wird.

</div>

Regierungen rechtfertigen Massenüberwachungsprogramme oft als notwendige Mittel zur Terrorismus- und Verbrechensbekämpfung. Als Menschenrechtsverletzungen werden sie jedoch am häufigsten eingesetzt, um Minderheiten und politische Dissidenten unverhältnismäßig hart zu treffen.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">Die Datenschutz-Lektion von 9/11: Massenüberwachung ist nicht der richtige Weg (englisch)</a></em></p>

In the face of Edward Snowden's disclosures of government programs such as [PRISM](https://en.wikipedia.org/wiki/PRISM) and [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), intelligence officials also admitted that the NSA had for years been secretly collecting records about virtually every American’s phone calls — who’s calling whom, when those calls are made, and how long they last. Diese Art von Informationen, die von der NSA Tag für Tag gesammelt werden, können unglaublich heikle Details über das Leben und die Verbindungen von Menschen offenbaren, z. B. ob sie einen Pfarrer:in, einen Abtreibungsanbieter, eine:n Suchtberater:in oder eine Selbstmord-Hotline angerufen haben.

</div>

Trotz der zunehmenden Massenüberwachung in den Vereinigten Staaten hat die Regierung festgestellt, dass Massenüberwachungsprogramme wie Section 215 im Hinblick auf die Verhinderung tatsächlicher Verbrechen oder terroristischer Anschläge "wenig einzigartigen Wert" haben, wobei die Bemühungen weitgehend die eigenen gezielten Überwachungsprogramme des FBI duplizieren.[^2]

Online kannst du über eine Vielzahl von Methoden verfolgt werden, einschließlich, aber nicht beschränkt auf:

- Deine IP-Adresse
- Browser-Cookies
- Die Daten, die du an Websites übermittelst
- Dein Browser- oder Gerät-Fingerabdruck
- Korrelation von Zahlungen

Wenn du über Massenüberwachungsprogramme besorgt bist, kannst du Strategien anwenden, wie z. B. deine Online-Identitäten abzuschotten, dich unter andere Benutzer zu mischen oder, wann immer möglich, einfach zu vermeiden, identifizierende Informationen preiszugeben.

## Überwachung als Geschäftsmodell

<span class="pg-brown">:material-account-cash: Überwachungskapitalismus</span>

> Der Überwachungskapitalismus ist ein Wirtschaftssystem, in dessen Mittelpunkt die Erfassung und Vermarktung personenbezogener Daten mit dem Hauptziel der Gewinnerzielung steht.[^3]

Für viele Menschen ist die Verfolgung und Überwachung durch private Unternehmen eine wachsende Sorge. Weit verbreitete Werbenetzwerke, wie die von Google und Facebook betriebenen, umspannen das Internet weit über die von ihnen kontrollierten Websites hinaus und verfolgen dabei deine Handlungen. Der Einsatz von Tools wie Content-Blockern zur Begrenzung der Netzwerkanfragen an ihre Server und das Lesen der Datenschutzrichtlinien der von dir genutzten Dienste kann dir helfen, viele einfache Angriffe zu vermeiden (auch wenn dies das Tracking nicht vollständig verhindern kann).[^4]

Additionally, even companies outside the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. Du kannst nicht automatisch annehmen, dass deine Daten sicher sind, nur weil der Dienst, den du verwendest, nicht zum typischen AdTech- oder Tracking-Geschäftsmodell gehört. Der stärkste Schutz vor der Datensammlung durch Unternehmen ist es, deine Daten zu verschlüsseln oder zu verschleiern, wann immer möglich, um es verschiedenen Anbietern schwer zu machen, Daten miteinander zu korrelieren und ein Profil über dich zu erstellen.

## Einschränkung der öffentlichen Information

<span class="pg-green">:material-account-search: Public Exposure</span>

Der beste Weg, deine Daten privat zu halten, besteht darin, sie gar nicht erst öffentlich zu machen. Das Löschen unerwünschter Informationen über dich online ist einer der besten ersten Schritte, die du unternehmen kannst, um deine Privatsphäre wiederzuerlangen.

- [Siehe unseren Leitfaden zur Kontolöschung :material-arrow-right-drop-circle:](account-deletion.md)

Auf Websites, auf denen du Informationen weitergibst, ist es sehr wichtig, die Datenschutzeinstellungen deines Kontos zu überprüfen, um die Verbreitung dieser Daten zu begrenzen. Aktiviere zum Beispiel den „privaten Modus“ für deine Konten, wenn du die Möglichkeit dazu hast: Dadurch wird sichergestellt, dass dein Konto nicht von Suchmaschinen indiziert wird und nicht ohne deine Zustimmung eingesehen werden kann.

Wenn du deine echten Daten bereits an Websites weitergegeben haben, die sie nicht haben sollten, solltest du eine Desinformationstaktik in Erwägung ziehen, wie z. B. die Weitergabe von fiktiven Informationen im Zusammenhang mit dieser Online-Identität. Dadurch sind deine echten Informationen nicht mehr von den falschen Informationen zu unterscheiden.

## Vermeidung von Zensur

<span class="pg-blue-gray">:material-close-outline: Zensur</span>

Zensur im Internet kann (in unterschiedlichem Ausmaß) von Akteuren wie totalitären Regierungen, Netzwerkadministratoren und Dienstleistern durchgeführt werden. Diese Bemühungen, die Kommunikation zu kontrollieren und den Zugang zu Informationen einzuschränken, sind immer unvereinbar mit dem Menschenrecht auf Meinungsfreiheit.[^5]

Zensur auf unternehmerisch Plattformen ist zunehmend häufiger anzutreffen, da Plattformen wie Twitter und Facebook auf öffentlichen Druck, Marktdruck und Druck von Regierungsbehörden reagieren. Regierungsdruck kann sich in verdeckten Anfragen an Unternehmen äußern, wie zum Beispiel die Bitte des Weißen Hauses, ein provokatives YouTube-Video [zu entfernen](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html), oder offen, wie die chinesische Regierung, die Unternehmen auffordert, einem strengen Zensurregime zu folgen.

Personen, die sich Sorgen um Zensur machen, können Technologien wie [Tor](../advanced/tor-overview.md) nutzen, um diese zu umgehen, und Zensur-resistente Kommunikationsplattformen wie [Matrix](../real-time-communication.md#element) unterstützen, die keine zentralisierte Kontrollinstanz haben, die Konten willkürlich schließen kann.

<div class="admonition tip" markdown>
<p class="admonition-title">Tipp</p>

Während das Umgehen von Zensur selbst einfach sein kann, kann es sehr problematisch sein, die Tatsache zu verbergen, dass man es tut.

Du solltest berücksichtigen, welche Aspekte des Netzwerks dein Gegner beobachten kann und ob dir eine glaubhafte Abstreitbarkeit (plausible deniability) für deine Handlungen möglich ist. Zum Beispiel kann die Verwendung von [verschlüsseltem DNS](../advanced/dns-overview.md#what-is-encrypted-dns) dir helfen, primitive, DNS-basierte Zensursysteme zu umgehen, aber es kann nicht wirklich vor deinem Internetanbieter verbergen, welche Seiten du besuchst. Ein VPN oder Tor kann dabei helfen, vor den Netzwerkadministratoren zu verbergen, was du besuchst, aber es kann nicht verbergen, dass du diese Netzwerke überhaupt benutzen. Pluggable Transporte (wie Obfs4proxy, Meek oder Shadowsocks) können dir helfen, Firewalls zu umgehen, die gängige VPN-Protokolle oder Tor blockieren, aber deine Umgehungsversuche können immer noch durch Methoden wie Sondierung oder [Deep Packet Inspection](https://de.wikipedia.org/wiki/Deep_Packet_Inspection) entdeckt werden.

</div>

Du musst immer die Risiken berücksichtigen, die mit dem Umgehen von Zensur verbunden sind, die möglichen Konsequenzen und den Grad der Raffinesse deines Gegners. Du solltest vorsichtig bei der Auswahl deiner Software sein und einen Notfallplan haben, falls du erwischt wirst.

[^1]: Wikipedia: [*Massenüberwachungen*](https://en.wikipedia.org/wiki/Mass_surveillance) und [*Überwachung*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: United States Privacy and Civil Liberties Oversight Board: [*Report on the Telephone Records Program Conducted under Section 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. You should also employ other mitigation techniques.
[^5]: Vereinte Nationen: [*Allgemeine Erklärung der Menschenrechte*](https://un.org/en/about-us/universal-declaration-of-human-rights).
