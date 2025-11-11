---
title: "Powszechne zagrożenia"
icon: 'material/eye-outline'
description: Model zagrożeń jest dla każdego indywidualny, ale oto kilka kwestii, które interesują wielu odwiedzających tę stronę.
---

Ogólnie rzecz biorąc, dzielimy nasze zalecenia według [zagrożeń](threat-modeling.md) lub celów, które dotyczą większości osób. ==Może nie dotyczyć Cię żadne, jedno, kilka lub wszystkie z tych zagrożeń== — narzędzia i usługi, których używasz, zależą od twoich celów. Możesz mieć też konkretne zagrożenia wykraczające poza te kategorie, i to jest całkowicie w porządku! Najważniejsze jest zrozumienie korzyści i ograniczeń narzędzi, które wybierasz, ponieważ praktycznie żadne z nich nie ochroni cię przed wszystkimi zagrożeniami.

<span class="pg-purple">:material-incognito: **Anonimowość**</span>
:

Chronienie aktywności w sieci przed ujawnieniem Twojej prawdziwej tożsamości, zabezpieczając cię przed osobami, które w szczególności próbują poznać *Twoją* tożsamość.

<span class="pg-red">:material-target-account: **Ataki ukierunkowane**</span>
:

Ochrona przed hakerami lub innymi cyberprzestępcami, którzy próbują uzyskać dostęp do *Twoich* danych lub urządzeń w sposób wymierzony.

<span class="pg-viridian">:material-package-variant-closed-remove: **Ataki na łańcuch dostaw**</span>
:

Zwykle przyjmuję formę <span class="pg-red">:material-target-account: Ataku ukierunkowanego</span>, która koncentruje się wokół luki lub błędu w zabezpieczeniach wprowadzonego do pozornie dobrego oprogramowania — bezpośrednio lub przez zależność od strony trzeciej.

<span class="pg-orange">:material-bug-outline: **Ataki pasywne**</span>
:

Ochrona przed takimi zagrożeniami jak złośliwe oprogramowanie, wycieki danych i innymi atakami wymierzonymi przeciwko wielu osobom jednocześnie.

<span class="pg-teal">:material-server-network: **Dostawcy usług**</span>
:

Ochrona Twoich danych przed dostawcami usług (np. za pomocą E2EE, które sprawia, że twoje dane są nieczytelne dla serwera).

<span class="pg-blue">:material-eye-outline: **Masowa inwigilacja**</span>
:

Ochrona przed agencjami rządowymi, organizacjami, stronami i usługami, które współpracują, by śledzić Twoje działania.

<span class="pg-brown">:material-account-cash: **Kapitalizm inwigilacji**</span>
:

Ochrona przed dużymi sieciami reklamowymi, takimi jak Google i Facebook, oraz przed wieloma innymi zbieraczami danych stron trzecich.

<span class="pg-green">:material-account-search: **Publiczna ekspozycja**</span>
:

Ograniczanie dostępnych o Tobie informacji w sieci — dla wyszukiwarek lub ogółu.

<span class="pg-blue-gray">:material-close-outline: **Cenzura**</span>
:

Unikanie cenzurowanego dostępu do informacji lub sytuacji, w których Twoje wypowiedzi online są cenzurowane.

Niektóre z tych zagrożeń mogą być dla Ciebie ważniejsze niż inne, w zależności od Twoich obaw. Na przykład programista mający dostęp do wartościowych lub krytycznych danych może przede wszystkim martwić się o <span class="pg-viridian">:material-package-variant-closed-remove: Ataki na łańcuch dostaw</span> i <span class="pg-red">:material-target-account: Ataki ukierunkowane</span>. Prawdopodobnie nadal będzie chciał chronić swoje dane osobowe przed wciągnięciem ich w programy <span class="pg-blue">:material-eye-outline: Masowej inwigilacji</span>. Podobnie wiele osób może przede wszystkim obawiać się <span class="pg-green">:material-account-search: Publicznej ekspozycji</span> swoich danych osobowych, ale i tak powinny być one czujne w kwestiach związanych z bezpieczeństwem, takich jak <span class="pg-orange">:material-bug-outline: Ataki pasywne</span> — na przykład złośliwe oprogramowanie atakujące ich urządzenia.

## Anonimowość a prywatność

<span class="pg-purple">:material-incognito: Anonimowość</span>

Anonimowość jest często mylona z prywatnością, ale są to różne pojęcia. Prywatność to zestaw wyborów dotyczących tego, jak Twoje dane są używane i udostępniane, natomiast anonimowość to całkowite oddzielenie Twoich działań w sieci od Twojej prawdziwej tożsamości.

Na przykład sygnaliści i dziennikarze mogą mieć znacznie bardziej ekstremalny model zagrożeń, który wymaga całkowitej anonimowości. Chodzi nie tylko o ukrycie tego, co robią, jakimi danymi dysponują i o ochronę przed atakami cyberprzestępców czy państw, ale też o pełne ukrycie, kim są. Często rezygnują z jakiejkolwiek wygody, jeśli pozwala to chronić ich anonimowość, prywatność lub bezpieczeństwo, ponieważ od tego może zależeć ich życie. Większość osób nie musi iść aż tak daleko.

## Bezpieczeństwo a prywatność

<span class="pg-orange">:material-bug-outline: Ataki pasywne</span>

Bezpieczeństwo i prywatność też bywają często mylone, ponieważ potrzebujesz bezpieczeństwa, by w ogóle mieć choćby namiastkę prywatności: korzystanie z narzędzi — nawet zaprojektowanych z myślą o prywatności — jest bezcelowe, jeśli mogą zostać łatwo wykorzystane przez atakujących, którzy później ujawnią Twoje dane. Jednak odwrotność niekoniecznie jest prawdziwa: najbezpieczniejsza usługa na świecie *niekoniecznie* jest prywatna. Najlepszym przykładem jest powierzenie danych firmie Google, która, biorąc pod uwagę swoją skalę, miała stosunkowo niewiele incydentów bezpieczeństwa, bo zatrudnia wiodących w branży ekspertów, by zabezpieczać swoją infrastrukturę. Mimo że Google dostarcza bardzo bezpieczne usługi, niewiele osób uznałoby swoje dane za prywatne w darmowych produktach konsumenckich Google (Gmail, YouTube itp.).

Jeśli chodzi o bezpieczeństwo aplikacji, zwykle nie wiemy (a czasem nie możemy wiedzieć), czy oprogramowanie, z którego korzystamy, jest złośliwe lub czy pewnego dnia nie stanie się złośliwe. Nawet przy najbardziej godnych zaufania deweloperach nie ma zwykle gwarancji, że ich oprogramowanie nie zawiera poważnej luki, którą można by później wykorzystać.

Aby zminimalizować szkody, jakie złośliwe oprogramowanie *mogłoby* wyrządzić, warto stosować zasadę zabezpieczeń przez szufladkowanie (ang. *compartmentalization*). Na przykład może to oznaczać używanie różnych komputerów do różnych zadań, korzystanie z maszyn wirtualnych do izolowania grup powiązanych aplikacji albo użycie bezpiecznego systemu operacyjnego silnie stawiającego na mechanizm piaskownicy aplikacji i obowiązkową kontrolę dostępu.

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

Mobilne systemy operacyjne zazwyczaj oferują lepszy mechanizm piaskownicy aplikacji niż systemy na komputery stacjonarne: aplikacje nie mogą uzyskać uprawnień root i wymagają zezwoleń na dostęp do zasobów systemowych.

Systemy na komputery stacjonarne zwykle pozostają w tyle w kwestii piaskownic. ChromeOS ma podobne możliwości piaskownicy do Androida, a macOS zapewnia pełną kontrolę uprawnień systemowych (deweloperzy mogą opcjonalnie włączyć piaskownicę dla aplikacji). Jednak systemy te przekazują informacje identyfikujące do swoich producentów OEM. Linux zwykle nie wysyła danych do dostawców systemu, lecz gorzej chroni przed exploitami i złośliwymi aplikacjami. Można to częściowo złagodzić, korzystając ze specjalistycznych dystrybucji, które w dużym stopniu opierają się na maszynach wirtualnych lub kontenerach, takich jak [Qubes OS](../desktop.md#qubes-os).

</div>

## Attacks against Specific Individuals

<span class="pg-red">:material-target-account: Targeted Attacks</span>

Targeted attacks against a specific person are more problematic to deal with. Common attacks include sending malicious documents via email, exploiting vulnerabilities (e.g. in browsers and operating systems), and physical attacks. If this is a concern for you, you should employ more advanced threat mitigation strategies.

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

By design, **web browsers**, **email clients**, and **office applications** typically run untrusted code, sent to you from third parties. Running multiple virtual machines—to separate applications like these from your host system, as well as each other—is one technique you can use to mitigate the chance of an exploit in these applications compromising the rest of your system. For example, technologies like Qubes OS or Microsoft Defender Application Guard on Windows provide convenient methods to do this.

</div>

If you are concerned about **physical attacks** you should use an operating system with a secure verified boot implementation, such as Android, iOS, macOS, or [Windows (with TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). You should also make sure that your drive is encrypted, and that the operating system uses a TPM or Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) or [Element](https://developers.google.com/android/security/android-ready-se) to rate limit attempts to enter the encryption passphrase. You should avoid sharing your computer with people you don't trust, because most desktop operating systems don't encrypt data separately per-user.

## Attacks against Certain Organizations

<span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>

Supply chain attacks are frequently a form of <span class="pg-red">:material-target-account: Targeted Attack</span> towards businesses, governments, and activists, although they can end up compromising the public at large as well.

<div class="admonition example" markdown>
<p class="admonition-title">Przykład</p>

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

<span class="pg-teal">:material-server-network: Service Providers</span>

We live in a world where almost everything is connected to the internet. Our "private" messages, emails, and social interactions are typically stored on a server, somewhere. Generally, when you send someone a message it's stored on a server, and when your friend wants to read the message the server will show it to them.

The obvious problem with this is that the service provider (or a hacker who has compromised the server) can access your conversations whenever and however they want, without you ever knowing. This applies to many common services, like SMS messaging, Telegram, and Discord.

Thankfully, E2EE can alleviate this issue by encrypting communications between you and your desired recipients before they are even sent to the server. The confidentiality of your messages is guaranteed, assuming the service provider doesn't have access to the private keys of either party.

<div class="admonition note" markdown>
<p class="admonition-title">Note on Web-based Encryption</p>

In practice, the effectiveness of different E2EE implementations varies. Applications, such as [Signal](../real-time-communication.md#signal), run natively on your device, and every copy of the application is the same across different installations. If the service provider were to introduce a [backdoor](https://en.wikipedia.org/wiki/Backdoor_(computing)) in their application—in an attempt to steal your private keys—it could later be detected with [reverse engineering](https://en.wikipedia.org/wiki/Reverse_engineering).

On the other hand, web-based E2EE implementations, such as Proton Mail's web app or Bitwarden's *Web Vault*, rely on the server dynamically serving JavaScript code to the browser to handle cryptography. A malicious server can target you and send you malicious JavaScript code to steal your encryption key (and it would be extremely hard to notice). Because the server can choose to serve different web clients to different people—even if you noticed the attack—it would be incredibly hard to prove the provider's guilt.

Therefore, you should use native applications over web clients whenever possible.

</div>

Even with E2EE, service providers can still profile you based on **metadata**, which typically isn't protected. While the service provider can't read your messages, they can still observe important things, such as whom you're talking to, how often you message them, and when you're typically active. Protection of metadata is fairly uncommon, and—if it's within your [threat model](threat-modeling.md)—you should pay close attention to the technical documentation of the software you're using to see if there's any metadata minimization or protection at all.

## Mass Surveillance Programs

<span class="pg-blue">:material-eye-outline: Masowa inwigilacja</span>

Mass surveillance is the intricate effort to monitor the "behavior, many activities, or information" of an entire (or substantial fraction of a) population.[^1] It often refers to government programs, such as the ones [disclosed by Edward Snowden in 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). However, it can also be carried out by corporations, either on behalf of government agencies or by their own initiative.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France, you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

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

## Surveillance as a Business Model

<span class="pg-brown">:material-account-cash: Kapitalizm inwigilacji</span>

> Surveillance capitalism is an economic system centered around the capture and commodification of personal data for the core purpose of profit-making.[^3]

For many people, tracking and surveillance by private corporations is a growing concern. Pervasive ad networks, such as those operated by Google and Facebook, span the internet far beyond just the sites they control, tracking your actions along the way. Using tools like content blockers to limit network requests to their servers, and reading the privacy policies of the services you use can help you avoid many basic adversaries (although it can't completely prevent tracking).[^4]

Additionally, even companies outside the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. You can't automatically assume your data is safe just because the service you're using doesn't fall within the typical AdTech or tracking business model. The strongest protection against corporate data collection is to encrypt or obfuscate your data whenever possible, making it difficult for different providers to correlate data with each other and build a profile on you.

## Limiting Public Information

<span class="pg-green">:material-account-search: Public Exposure</span>

The best way to keep your data private is simply not making it public in the first place. Deleting unwanted information you find about yourself online is one of the best first steps you can take to regain your privacy.

- [View our guide on account deletion :material-arrow-right-drop-circle:](account-deletion.md)

On sites where you do share information, checking the privacy settings of your account to limit how widely that data is spread is very important. For example, enable "private mode" on your accounts if given the option: This ensures that your account isn't being indexed by search engines, and that it can't be viewed without your permission.

If you've already submitted your real information to sites which shouldn't have it, consider using disinformation tactics, like submitting fictitious information related to that online identity. This makes your real information indistinguishable from the false information.

## Avoiding Censorship

<span class="pg-blue-gray">:material-close-outline: Cenzura</span>

Censorship online can be carried out (to varying degrees) by actors including totalitarian governments, network administrators, and service providers. These efforts to control communication and restrict access to information will always be incompatible with the human right to Freedom of Expression.[^5]

Censorship on corporate platforms is increasingly common, as platforms like Twitter and Facebook give in to public demand, market pressures, and pressures from government agencies. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

People concerned with the threat of censorship can use technologies like [Tor](../advanced/tor-overview.md) to circumvent it, and support censorship-resistant communication platforms like [Matrix](../social-networks.md#element), which doesn't have a centralized account authority that can close accounts arbitrarily.

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

While evading censorship itself can be easy, hiding the fact that you are doing it can be very problematic.

You should consider which aspects of the network your adversary can observe, and whether you have plausible deniability for your actions. For example, using [encrypted DNS](../advanced/dns-overview.md#what-is-encrypted-dns) can help you bypass rudimentary, DNS-based censorship systems, but it can't truly hide what you are visiting from your ISP. A VPN or Tor can help hide what you are visiting from network administrators, but can't hide that you're using those networks in the first place. Pluggable transports (such as Obfs4proxy, Meek, or Shadowsocks) can help you evade firewalls that block common VPN protocols or Tor, but your circumvention attempts can still be detected by methods like probing or [deep packet inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection).

</div>

You must always consider the risks of trying to bypass censorship, the potential consequences, and how sophisticated your adversary may be. You should be cautious with your software selection, and have a backup plan in case you are caught.

[^1]: Wikipedia: [*Mass Surveillance*](https://en.wikipedia.org/wiki/Mass_surveillance) and [*Surveillance*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: United States Privacy and Civil Liberties Oversight Board: [*Report on the Telephone Records Program Conducted under Section 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. You should also employ other mitigation techniques.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
