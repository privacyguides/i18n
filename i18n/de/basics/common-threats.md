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

<span class="pg-viridian">:material-package-variant-closed-remove: **Supply Chain Attacks**</span>
:

Typically a form of <span class="pg-red">:material-target-account: Targeted Attack</span> that centers around a vulnerability or exploit introduced into otherwise good software either directly or through a dependency from a third party.

<span class="pg-orange">:material-bug-outline: **Passive Angriffe**</span>
:

Schutz vor Malware, Datenleaks und anderen Angriffen, die sich gegen viele Menschen gleichzeitig richten.

<span class="pg-teal">:material-server-network: **Service Providers**</span>
:

Schutz deiner Daten vor Dienstleistern (z. B. mit E2EE, welche deine Daten für den Server unlesbar macht).

<span class="pg-blue">:material-eye-outline: **Massenüberwachung**</span>
:

Protection from government agencies, organizations, websites, and services which work together to track your activities.

<span class="pg-brown">:material-account-cash: **Überwachungskapitalismus**</span>
:

Protecting yourself from big advertising networks, like Google and Facebook, as well as a myriad of other third-party data collectors.

<span class="pg-green">:material-account-search: **Public Exposure**</span>
:

Limiting the information about you that is accessible online—to search engines or the general public.

<span class="pg-blue-gray">:material-close-outline: **Zensur**</span>
:

Avoiding censored access to information or being censored yourself when speaking online.

Einige dieser Bedrohungen können für dich wichtiger sein als andere, je nach deinen spezifischen Anliegen. Ein Softwareentwickler, der Zugang zu wertvollen oder kritischen Daten hat, könnte sich beispielsweise in erster Linie über <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain-Angriffe</span> und <span class="pg-red">:material-target-account: Targeted Attacks</span> Sorgen machen. Sie werden wahrscheinlich immer noch ihre persönlichen Daten davor schützen wollen, von <span class="pg-blue">:material-eye-outline: Massenüberwachungsprogrammen</span> erfasst zu werden. Ebenso sind viele Menschen vielleicht in erster Linie besorgt über die <span class="pg-green">:material-account-search: Öffentliche Bloßstellung</span> ihrer persönlichen Daten, sollten aber trotzdem auf sicherheitsrelevante Probleme achten, wie z. B. <span class="pg-orange">:material-bug-outline: Passive Angriffe</span> - wie Malware, die ihre Geräte befallen.

## Anonymität vs. Datenschutz

<span class="pg-purple">:material-incognito: Anonymität</span>

Anonymität wird oft mit Datenschutz in einen Topf geworfen, es sind aber unterschiedliche Konzepte. Während Datenschutz aus einer Reihe von Entscheidungen besteht, die du über die Verwendung und Weitergabe deiner Daten triffst, bedeutet Anonymität die vollständige Trennung deiner Online-Aktivitäten von deiner wirklichen Identität.

Für Whistleblower und Journalisten beispielsweise kann ein viel extremeres Bedrohungsmodell gelten, das völlige Anonymität erfordert. Das bedeutet nicht nur, dass sie verbergen, was sie tun, welche Daten sie haben und dass sie nicht von böswilligen Akteuren oder Regierungen gehackt werden, sondern auch, dass sie völlig verbergen, wer sie sind. Sie sind oft bereit, jede Art von Bequemlichkeit zu opfern, wenn es darum geht, ihre Anonymität, Privatsphäre oder Sicherheit zu schützen, weil ihr Leben davon abhängen könnte. Die meisten Menschen brauchen so weit nicht zu gehen.

## Sicherheit und Datenschutz

<span class="pg-orange">:material-bug-outline: Passive Angriffe</span>

Sicherheit und Datenschutz werden auch oft verwechselt, weil man Sicherheit braucht, um überhaupt einen Anschein von Datenschutz zu erhalten: Der Einsatz von Tools - selbst wenn sie von vornherein privat sind - ist sinnlos, wenn sie leicht von Angreifern ausgenutzt werden können, die später Ihre Daten veröffentlichen. Das Gegenteil ist jedoch nicht unbedingt der Fall: Der sicherste Dienst der Welt *ist nicht unbedingt* privat. Das beste Beispiel hierfür ist das Anvertrauen von Daten an Google, das in Anbetracht seiner Größe nur wenige Sicherheitsvorfälle zu verzeichnen hatte, weil es branchenführende Sicherheitsexperten mit der Sicherung seiner Infrastruktur beschäftigt. Obwohl Google sehr sichere Dienste anbietet, würden nur sehr wenige Menschen ihre Daten in den kostenlosen Verbraucherprodukten von Google (Gmail, YouTube usw.) als privat betrachten

When it comes to application security, we generally don't (and sometimes can't) know if the software we use is malicious, or might one day become malicious. Even with the most trustworthy developers, there's generally no guarantee that their software doesn't have a serious vulnerability that could later be exploited.

To minimize the damage that a malicious piece of software *could* do, you should employ security by compartmentalization. For example, this could come in the form of using different computers for different jobs, using virtual machines to separate different groups of related applications, or using a secure operating system with a strong focus on application sandboxing and mandatory access control.

<div class="admonition tip" markdown>
<p class="admonition-title">Tipp</p>

Mobile operating systems generally have better application sandboxing than desktop operating systems: Apps can't obtain root access, and require permission for access to system resources.

Desktop operating systems generally lag behind on proper sandboxing. ChromeOS has similar sandboxing capabilities to Android, and macOS has full system permission control (and developers can opt-in to sandboxing for applications). However, these operating systems do transmit identifying information to their respective OEMs. Linux tends to not submit information to system vendors, but it has poor protection against exploits and malicious apps. This can be mitigated somewhat with specialized distributions which make significant use of virtual machines or containers, such as [Qubes OS](../desktop.md#qubes-os).

</div>

## Attacks against Specific Individuals

<span class="pg-red">:material-target-account: Targeted Attacks</span>

Targeted attacks against a specific person are more problematic to deal with. Common attacks include sending malicious documents via email, exploiting vulnerabilities (e.g. in browsers and operating systems), and physical attacks. If this is a concern for you, you should employ more advanced threat mitigation strategies.

<div class="admonition tip" markdown>
<p class="admonition-title">Tipp</p>

In **Webbrowsern**, **E-Mail-Clients** und **Büroanwendungen** wird in der Regel nicht vertrauenswürdiger Code ausgeführt, der dir von Dritten übermittelt wird. Der Einsatz mehrerer virtueller Maschinen — um Anwendungen wie diese von deinem Hostsystem und voneinander zu trennen - ist eine Technik, mit der du die Gefahr verringern kannst, dass ein Exploit in diesen Anwendungen den Rest deines Systems gefährdet. Beispielsweise bieten Technologien wie Qubes OS oder Microsoft Defender Application Guard unter Windows bequeme Methoden, dies zu tun.

</div>

If you are concerned about **physical attacks** you should use an operating system with a secure verified boot implementation, such as Android, iOS, macOS, or [Windows (with TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). You should also make sure that your drive is encrypted, and that the operating system uses a TPM or Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) or [Element](https://developers.google.com/android/security/android-ready-se) to rate limit attempts to enter the encryption passphrase. You should avoid sharing your computer with people you don't trust, because most desktop operating systems don't encrypt data separately per-user.

## Angriffe auf bestimmte Organisationen

<span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>

Supply chain attacks are frequently a form of <span class="pg-red">:material-target-account: Targeted Attack</span> towards businesses, governments, and activists, although they can end up compromising the public at large as well.

<div class="admonition example" markdown>
<p class="admonition-title">Beispiel</p>

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

## Privatsphäre vor Dienstanbietern

<span class="pg-teal">:material-server-network: Diensteanbieter</span>

Wir leben in einer Welt, in der fast alles mit dem Internet verbunden ist. Unsere „privaten“ Nachrichten, E-Mails und sozialen Interaktionen werden in der Regel irgendwo auf einem Server gespeichert. Generally, when you send someone a message it's stored on a server, and when your friend wants to read the message the server will show it to them.

Das offensichtliche Problem dabei ist, dass der Dienstanbieter (oder ein Hacker, der in den Server eingedrungen ist) auf deine Unterhaltungen zugreifen kann, wann und wie er will, ohne dass du es je erfährst. Dies gilt für viele gängige Dienste wie SMS-Nachrichten, Telegram und Discord.

Glücklicherweise kann E2EE dieses Problem lindern, indem es die Kommunikation zwischen dir und den gewünschten Empfängern verschlüsselt, bevor sie überhaupt an den Server gesendet wird. Die Vertraulichkeit deiner Nachrichten ist gewährleistet, vorausgesetzt, der Dienstanbieter hat keinen Zugang zu den privaten Schlüsseln der beiden Parteien.

<div class="admonition note" markdown>
<p class="admonition-title">Hinweis zur webbasierten Verschlüsselung</p>

In practice, the effectiveness of different E2EE implementations varies. Applications, such as [Signal](../real-time-communication.md#signal), run natively on your device, and every copy of the application is the same across different installations. If the service provider were to introduce a [backdoor](https://en.wikipedia.org/wiki/Backdoor_(computing)) in their application—in an attempt to steal your private keys—it could later be detected with [reverse engineering](https://en.wikipedia.org/wiki/Reverse_engineering).

On the other hand, web-based E2EE implementations, such as Proton Mail's web app or Bitwarden's *Web Vault*, rely on the server dynamically serving JavaScript code to the browser to handle cryptography. A malicious server can target you and send you malicious JavaScript code to steal your encryption key (and it would be extremely hard to notice). Because the server can choose to serve different web clients to different people—even if you noticed the attack—it would be incredibly hard to prove the provider's guilt.

Therefore, you should use native applications over web clients whenever possible.

</div>

Even with E2EE, service providers can still profile you based on **metadata**, which typically isn't protected. While the service provider can't read your messages, they can still observe important things, such as who you're talking to, how often you message them, and when you're typically active. Protection of metadata is fairly uncommon, and—if it's within your [threat model](threat-modeling.md)—you should pay close attention to the technical documentation of the software you're using to see if there's any metadata minimization or protection at all.

## Massenüberwachungsprogramme

<span class="pg-blue">:material-eye-outline: Massenüberwachung</span>

Mass surveillance is the intricate effort to monitor the "behavior, many activities, or information" of an entire (or substantial fraction of a) population.[^1] It often refers to government programs, such as the ones [disclosed by Edward Snowden in 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). However, it can also be carried out by corporations, either on behalf of government agencies or by their own initiative.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas der Überwachung</p>

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

Governments often justify mass surveillance programs as necessary means to combat terrorism and prevent crime. However, as breaches of human rights, they're most often used to disproportionately target minority groups and political dissidents, among others.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

In the face of Edward Snowden's disclosures of government programs such as [PRISM](https://en.wikipedia.org/wiki/PRISM) and [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), intelligence officials also admitted that the NSA had for years been secretly collecting records about virtually every American’s phone calls — who’s calling whom, when those calls are made, and how long they last. This kind of information, when amassed by the NSA day after day, can reveal incredibly sensitive details about people’s lives and associations, such as whether they have called a pastor, an abortion provider, an addiction counselor, or a suicide hotline.

</div>

Despite growing mass surveillance in the United States, the government has found that mass surveillance programs like Section 215 have had "little unique value" with respect to stopping actual crimes or terrorist plots, with efforts largely duplicating the FBI's own targeted surveillance programs.[^2]

Online, you can be tracked via a variety of methods, including but not limited to:

- Your IP address
- Browser cookies
- The data you submit to websites
- Your browser or device fingerprint
- Payment method correlation

If you're concerned about mass surveillance programs, you can use strategies like compartmentalizing your online identities, blending in with other users, or, whenever possible, simply avoiding giving out identifying information.

## Überwachung als Geschäftsmodell

<span class="pg-brown">:material-account-cash: Surveillance Capitalism</span>

> Der Überwachungskapitalismus ist ein Wirtschaftssystem, in dessen Mittelpunkt die Erfassung und Vermarktung personenbezogener Daten mit dem Hauptziel der Gewinnerzielung steht.[^3]

Für viele Menschen ist die Verfolgung und Überwachung durch private Unternehmen eine wachsende Sorge. Weit verbreitete Werbenetzwerke, wie die von Google und Facebook betriebenen, umspannen das Internet weit über die von ihnen kontrollierten Websites hinaus und verfolgen dabei deine Handlungen. Using tools like content blockers to limit network requests to their servers, and reading the privacy policies of the services you use can help you avoid many basic adversaries (although it can't completely prevent tracking).[^4]

Additionally, even companies outside of the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. You can't automatically assume your data is safe just because the service you're using doesn't fall within the typical AdTech or tracking business model. The strongest protection against corporate data collection is to encrypt or obfuscate your data whenever possible, making it difficult for different providers to correlate data with each other and build a profile on you.

## Einschränkung der öffentlichen Information

<span class="pg-green">:material-account-search: Public Exposure</span>

Der beste Weg, deine Daten privat zu halten, besteht darin, sie gar nicht erst öffentlich zu machen. Das Löschen unerwünschter Informationen über dich online ist einer der besten ersten Schritte, die du unternehmen kannst, um deine Privatsphäre wiederzuerlangen.

- [Siehe unseren Leitfaden zur Kontolöschung :material-arrow-right-drop-circle:](account-deletion.md)

On sites where you do share information, checking the privacy settings of your account to limit how widely that data is spread is very important. For example, enable "private mode" on your accounts if given the option: This ensures that your account isn't being indexed by search engines, and that it can't be viewed without your permission.

If you've already submitted your real information to sites which shouldn't have it, consider using disinformation tactics, like submitting fictitious information related to that online identity. This makes your real information indistinguishable from the false information.

## Vermeidung von Zensur

<span class="pg-blue-gray">:material-close-outline: Zensur</span>

Censorship online can be carried out (to varying degrees) by actors including totalitarian governments, network administrators, and service providers. These efforts to control communication and restrict access to information will always be incompatible with the human right to Freedom of Expression.[^5]

Censorship on corporate platforms is increasingly common, as platforms like Twitter and Facebook give in to public demand, market pressures, and pressures from government agencies. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

People concerned with the threat of censorship can use technologies like [Tor](../advanced/tor-overview.md) to circumvent it, and support censorship-resistant communication platforms like [Matrix](../real-time-communication.md#element), which doesn't have a centralized account authority that can close accounts arbitrarily.

<div class="admonition tip" markdown>
<p class="admonition-title">Tipp</p>

While evading censorship itself can be easy, hiding the fact that you are doing it can be very problematic.

You should consider which aspects of the network your adversary can observe, and whether you have plausible deniability for your actions. For example, using [encrypted DNS](../advanced/dns-overview.md#what-is-encrypted-dns) can help you bypass rudimentary, DNS-based censorship systems, but it can't truly hide what you are visiting from your ISP. A VPN or Tor can help hide what you are visiting from network administrators, but can't hide that you're using those networks in the first place. Pluggable transports (such as Obfs4proxy, Meek, or Shadowsocks) can help you evade firewalls that block common VPN protocols or Tor, but your circumvention attempts can still be detected by methods like probing or [deep packet inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection).

</div>

You must always consider the risks of trying to bypass censorship, the potential consequences, and how sophisticated your adversary may be. You should be cautious with your software selection, and have a backup plan in case you are caught.

[^1]: Wikipedia: [*Massenüberwachungen*](https://en.wikipedia.org/wiki/Mass_surveillance) und [*Überwachung*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: United States Privacy and Civil Liberties Oversight Board: [*Report on the Telephone Records Program Conducted under Section 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. You should also employ other mitigation techniques.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
