---
title: "Najczęstsze błędne przekonania"
icon: 'material/robot-confused'
description: Prywatność nie jest prostym tematem — łatwo dać się zwieść hasłom marketingowym i dezinformacji.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Czy oprogramowanie open-source jest z definicji bezpieczne?
        acceptedAnswer:
          "@type": Answer
          text: |
            Dostępność kodu źródłowego i sposób licencjonowania same w sobie nie wpływają bezpośrednio na bezpieczeństwo. Oprogramowanie open-source może być bezpieczniejsze od zamkniętego, ale nie ma żadnej gwarancji, że tak będzie. Oceniając program, warto rozpatrywać reputację i poziom bezpieczeństwa każdego narzędzia indywidualnie.
      - 
        "@type": Question
        name: Czy przeniesienie zaufania na innego dostawcę może zwiększyć prywatność?
        acceptedAnswer:
          "@type": Answer
          text: |
            Często mówimy o „przenoszeniu zaufania” przy rozwiązaniach takich jak VPN (które przenoszą zaufanie, jakie pokładasz w swoim dostawcy usług internetowych, na dostawcę VPN). Choć chroni to Twoje dane przeglądania przed ISP, wybrany dostawca VPN nadal ma do nich dostęp — Twoje dane nie są więc całkowicie zabezpieczone przed wszystkimi podmiotami.
      - 
        "@type": Question
        name: Czy rozwiązania nastawione na prywatność są z natury godne zaufania?
        acceptedAnswer:
          "@type": Answer
          text: |
            Skupianie się wyłącznie na politykach prywatności i marketingu danego narzędzia lub dostawcy może zaślepić Cię na ich słabości. Szukając bardziej prywatnego rozwiązania, najpierw ustal, jaki jest podstawowy problem, i dobierz techniczne środki do jego rozwiązania. Na przykład możesz chcieć unikać Dysku Google, ponieważ daje on Google dostęp do wszystkich Twoich danych. Zasadniczym problemem w tym przypadku jest brak szyfrowania end-to-end (E2EE), więc upewnij się, że wybrany dostawca, na którego się przenosisz, rzeczywiście implementuje E2EE, albo użyj narzędzia (np. Cryptomator), które zapewnia E2EE niezależnie od chmury. Przejście na „dostawcę skoncentrowanego na prywatności”, który nie wdraża E2EE, nie rozwiązuje problemu — jedynie przenosi zaufanie z Google na tego dostawcę.
      - 
        "@type": Question
        name: Jak skomplikowany powinien być mój model zagrożeń?
        acceptedAnswer:
          "@type": Answer
          text: |
            Często widzimy, że ludzie opisują modele zagrożeń dotyczące prywatności, które są przesadnie skomplikowane. Zwykle obejmują one np. wiele różnych kont e-mail lub skomplikowane konfiguracje z wieloma ruchomymi elementami i warunkami. Odpowiedzi są zazwyczaj odpowiedziami na pytania typu „Jaki jest najlepszy sposób na X?”.
            Znalezienie „najlepszego” rozwiązania nie musi oznaczać dążenia do nieomylnego systemu z dziesiątkami warunków — takie rozwiązania często są trudne w praktycznym użyciu. Jak już wspomniano, bezpieczeństwo często idzie kosztem wygody.
---

## „Oprogramowanie open-source jest zawsze bezpieczne” albo „Oprogramowanie własnościowe jest bezpieczniejsze”

These myths stem from a number of prejudices, but whether the source code is available and how software is licensed does not inherently affect its security in any way. ==Open-source software has the *potential* to be more secure than proprietary software, but there is absolutely no guarantee this is the case.== When you evaluate software, you should look at the reputation and security of each tool on an individual basis.

Open-source software *can* be audited by third-parties, and is often more transparent about potential vulnerabilities than proprietary counterparts. It also allows you to review the code and disable any suspicious functionality you find yourself. However, *unless you do so*, there is no guarantee that code has ever been evaluated, especially with smaller software projects. The open development process has also sometimes been exploited to introduce new vulnerabilities known as [:material-package-variant-closed-remove: Supply Chain Attacks](common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, which are discussed further in our [Common Threats](common-threats.md) page.[^1]

On the flip side, proprietary software is less transparent, but that doesn't imply that it's not secure. Major proprietary software projects can be audited internally and by third-party agencies, and independent security researchers can still find vulnerabilities with techniques like reverse engineering.

To avoid biased decisions, it's *vital* that you evaluate the privacy and security standards of the software you use.

## "Shifting trust can increase privacy"

Często mówimy o „przenoszeniu zaufania” przy rozwiązaniach takich jak VPN (które przenoszą zaufanie, jakie pokładasz w swoim dostawcy usług internetowych, na dostawcę VPN). While this protects your browsing data from your ISP *specifically*, the VPN provider you choose still has access to your browsing data: Your data isn't completely secured from all parties. This means that:

1. You must exercise caution when choosing a provider to shift trust to.
2. You should still use other techniques, like E2EE, to protect your data completely. Merely distrusting one provider to trust another is not securing your data.

## "Privacy-focused solutions are inherently trustworthy"

Skupianie się wyłącznie na politykach prywatności i marketingu danego narzędzia lub dostawcy może zaślepić Cię na ich słabości. Szukając bardziej prywatnego rozwiązania, najpierw ustal, jaki jest podstawowy problem, i dobierz techniczne środki do jego rozwiązania. Na przykład możesz chcieć unikać Dysku Google, ponieważ daje on Google dostęp do wszystkich Twoich danych. The underlying problem in this case is lack of E2EE, so you should make sure that the provider you switch to actually implements E2EE, or use a tool (like [Cryptomator](../encryption.md#cryptomator-cloud)) which provides E2EE on any cloud provider. Przejście na „dostawcę skoncentrowanego na prywatności”, który nie wdraża E2EE, nie rozwiązuje problemu — jedynie przenosi zaufanie z Google na tego dostawcę.

The privacy policies and business practices of providers you choose are very important, but should be considered secondary to technical guarantees of your privacy: You shouldn't shift trust to another provider when trusting a provider isn't a requirement at all.

## "Complicated is better"

Często widzimy, że ludzie opisują modele zagrożeń dotyczące prywatności, które są przesadnie skomplikowane. Often, these solutions include problems like multiple email accounts or complicated setups with lots of moving parts and conditions. The replies are usually answers to "What is the best way to do *X*?"

Znalezienie „najlepszego” rozwiązania nie musi oznaczać dążenia do nieomylnego systemu z dziesiątkami warunków — takie rozwiązania często są trudne w praktycznym użyciu. Jak już wspomniano, bezpieczeństwo często idzie kosztem wygody. Below, we provide some tips:

1. ==Actions need to serve a particular purpose:== think about how to do what you want with the fewest actions.
2. ==Remove human failure points:== We fail, get tired, and forget things. To maintain security, avoid relying on manual conditions and processes that you have to remember.
3. ==Use the right level of protection for what you intend.== We often see recommendations of so-called law-enforcement or subpoena-proof solutions. These often require specialist knowledge and generally aren't what people want. There's no point in building an intricate threat model for anonymity if you can be easily deanonymized by a simple oversight.

So, how might this look?

One of the clearest threat models is one where people *know who you are* and one where they do not. There will always be situations where you must declare your legal name and there are others where you don't need to.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Porada</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](../cryptocurrency.md#monero). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added an obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
