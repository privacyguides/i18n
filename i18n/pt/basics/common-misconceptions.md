---
title: "Equívocos Comuns"
icon: 'material/robot-confused'
description: A privacidade não é um tema simples, e é fácil ser apanhado por alegações de marketing e outras desinformações.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Is open-source software inherently secure?
        acceptedAnswer:
          "@type": Answer
          text: |
            O facto de o código-fonte estar ou não disponível e a forma como o software é licenciado não afetam de forma alguma a sua segurança. O software de código aberto tem potencial para ser mais seguro do que o software proprietário, mas não há nenhuma garantia de que seja esse o caso. Ao avaliar o software, deve ter em conta a reputação e a segurança de cada ferramenta numa base individual.
      - 
        "@type": Question
        name: Pode a transferência de confiança para outro fornecedor aumentar a privacidade?
        acceptedAnswer:
          "@type": Answer
          text: |
            Falamos muito de "transferência de confiança" quando discutimos soluções como as VPN (que transferem a confiança que deposita no seu ISP para o fornecedor de VPN). Embora isto proteja especificamente os seus dados de navegação do seu ISP, o fornecedor de VPN que escolher continua a ter acesso aos seus dados de navegação: os seus dados não estão completamente protegidos de todas as partes.
      - 
        "@type": Question
        name: São as soluções centradas na privacidade intrinsecamente fiáveis?
        acceptedAnswer:
          "@type": Answer
          text: |
            Concentrar-se apenas nas políticas de privacidade e no marketing de uma ferramenta ou fornecedor pode cegá-lo para os seus pontos fracos. Quando procura uma solução mais privada, deve determinar qual é o problema subjacente e encontrar soluções técnicas para esse problema. Por exemplo, pode querer evitar o Google Drive, que dá ao Google acesso a todos os seus dados. O problema subjacente neste caso é a falta de E2EE, pelo que deve certificar-se de que o fornecedor para o qual muda implementa efetivamente o E2EE, ou utilizar uma ferramenta (como o Cryptomator) que fornece E2EE em qualquer fornecedor de serviços em nuvem. Mudar para um fornecedor "centrado na privacidade" (que não implementa o E2EE) não resolve o seu problema: apenas transfere a confiança da Google para esse fornecedor.
      - 
        "@type": Question
        name: Quão complicado deve ser o meu modelo de ameaça?
        acceptedAnswer:
          "@type": Answer
          text: |
            É frequente vermos pessoas a descrever modelos de ameaças à privacidade que são demasiado complexos. Muitas vezes, estas soluções incluem problemas como muitas contas de correio eletrónico diferentes ou configurações complicadas com muitas partes móveis e condições. As respostas são geralmente respostas a "Qual é a melhor forma de fazer X?"
            Encontrar a "melhor" solução para si não significa necessariamente que está à procura de uma solução infalível com dezenas de condições — estas soluções são muitas vezes difíceis de trabalhar de forma realista. Tal como referimos anteriormente, a segurança tem muitas vezes um custo em termos de conveniência.
---

## "O software de código aberto é sempre seguro" ou "O software proprietário é mais seguro"

Estes mitos têm origem numa série de preconceitos, mas o facto de o código-fonte estar ou não disponível e como o software é licenciado não afetam de forma alguma a sua segurança. ==O software de código aberto tem o *potencial* de ser mais seguro do que o software proprietário, mas não há qualquer garantia de que seja esse o caso.== Ao avaliar o software, deve analisar a reputação e a segurança de cada ferramenta numa base individual.

O software de código aberto *pode* ser auditado por terceiros e é frequentemente mais transparente relativamente a potenciais vulnerabilidades do que as contrapartes proprietárias. Permite-lhe também rever o código e desativar qualquer funcionalidade suspeita que encontre. No entanto, *a menos que o faça*, não há garantia de que o código tenha sido alguma vez avaliado, especialmente em projetos de software menores. The open development process has also sometimes been exploited to introduce new vulnerabilities known as <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>, which are discussed further in our [Common Threats](common-threats.md) page.[^1]

Por outro lado, o software proprietário é menos transparente, mas isso não significa que não seja seguro. Os principais projetos de software proprietário podem ser auditados internamente e por agências terceiras, e os investigadores de segurança independentes podem ainda encontrar vulnerabilidades com técnicas como a engenharia inversa.

Para evitar decisões tendenciosas, é *vital* que avalie as normas de privacidade e segurança do software que utiliza.

## "A mudança de confiança pode aumentar a privacidade"

Falamos muito de "transferência de confiança" quando discutimos soluções como as VPN (que transferem a confiança que deposita no seu ISP para o fornecedor de VPN). Embora isto *especificamente* proteja os seus dados de navegação do seu ISP, o fornecedor de VPN que escolher continua a ter acesso aos seus dados de navegação: os seus dados não estão completamente protegidos de todas as partes. Isto significa que:

1. Deve exercitar cuidado ao escolher um provedor para mudar confiança.
2. Deve ainda utilizar outras técnicas, como a E2EE, para proteger completamente os seus dados. O simples facto de desconfiar de um fornecedor para confiar noutro não protege os seus dados.

## "As soluções centradas na privacidade são inerentemente fiáveis"

Concentrar-se apenas nas políticas de privacidade e no marketing de uma ferramenta ou fornecedor pode cegá-lo para os seus pontos fracos. Quando procura uma solução mais privada, deve determinar qual é o problema subjacente e encontrar soluções técnicas para esse problema. Por exemplo, pode querer evitar o Google Drive, que dá ao Google acesso a todos os seus dados. O problema subjacente neste caso é a falta de E2EE, pelo que deve certificar-se de que o fornecedor para o qual muda implementa efetivamente o E2EE, ou utilizar uma ferramenta (como o [Cryptomator](../encryption.md#cryptomator-cloud)) que fornece E2EE em qualquer fornecedor de serviços em nuvem. Mudar para um fornecedor "centrado na privacidade" (que não implementa o E2EE) não resolve o seu problema: apenas transfere a confiança da Google para esse fornecedor.

As políticas de privacidade e as práticas comerciais dos fornecedores que escolher são muito importantes, mas devem ser consideradas secundárias relativamente às garantias técnicas da sua privacidade: não se deve transferir a confiança para outro fornecedor quando a confiança num fornecedor não é de todo um requisito.

## "Complicado é melhor"

É frequente vermos pessoas a descrever modelos de ameaças à privacidade que são demasiado complexos. Muitas vezes, estas soluções incluem problemas como muitas contas de correio eletrónico diferentes ou configurações complicadas com muitas partes móveis e condições. As respostas são geralmente respostas a "Qual é a melhor maneira de fazer *X*?"

Encontrar a "melhor" solução para si não significa necessariamente que está à procura de uma solução infalível com dezenas de condições — estas soluções são muitas vezes difíceis de trabalhar de forma realista. Tal como referimos anteriormente, a segurança tem muitas vezes um custo em termos de conveniência. Em seguida, apresentamos alguns conselhos:

1. ==As ações têm de servir um determinado objetivo:== pense em como fazer o que pretende com o menor número de ações.
2. ==Remova os pontos de falha humanos:== Falhamos, cansamo-nos e esquecemo-nos de coisas. Para manter a segurança, evite depender de condições e processos manuais dos quais tem de se lembrar.
3. ==Utilize o nível de proteção adequado para o que pretende== É frequente vermos recomendações das chamadas soluções à prova de intimação ou de aplicação da lei. Estes requerem frequentemente conhecimentos especializados e não são geralmente o que as pessoas querem. Não adianta criar um modelo de ameaças complexo para o anonimato se pode ser facilmente desanonimizado por um simples descuido.

Então, o que isto pode parecer?

Um dos modelos de ameaça mais claros é aquele no qual as pessoas *sabem quem é* e aquele em que não sabem. Haverá sempre situações em que tem de declarar o seu nome legal e outras em que não precisa de o fazer.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Tip</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](https://getmonero.org). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added a obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://www.cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
