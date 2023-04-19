---
title: "일반적인 오해"
icon: 'material/robot-confused'
description: 프라이버시는 결코 간단하지 않고, 마케팅성 주장이나 기타 잘못된 정보에 현혹되기 쉽습니다.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: 오픈 소스 소포트웨어는 본질적으로 안전한가요?
        acceptedAnswer:
          "@type": Answer
          text: |
            소스 코드의 공개 여부와 라이선스 방식은 본질적으로 보안에 어떠한 영향도 미치지 않습니다. 오픈 소스 소프트웨어는 독점 소프트웨어보다 더 안전할 가능성이 있지만, 반드시 그렇다는 보장은 없습니다. 소프트웨어를 평가할 때는 평판과 보안을 개별적으로 살펴봐야 합니다.
      - 
        "@type": Question
        name: 다른 제공업체로 신뢰하는 대상을 변경함으로써 프라이버시를 강화할 수 있나요?
        acceptedAnswer:
          "@type": Answer
          text: |
            VPN과 같은 솔루션들에 대해 논의할 때 "신뢰하는 대상을 변경한다"는 말이 자주 나옵니다. (VPN은 ISP로부터 VPN 제공자로 신뢰 대상을 바꿉니다) 이는 ISP로부터 브라우징 데이터를 보호하지만, 당신이 선택한 VPN 제공자는 이 브라우징 데이터에 접근할 수 있습니다. 즉, 데이터가 모든 이로부터 보호되는 것이 아닙니다.
      - 
        "@type": Question
        name: 프라이버시 중점 솔루션은 본질적으로 신뢰할 수 있나요?
        acceptedAnswer:
          "@type": Answer
          text: |
            제품 또는 서비스의 개인정보 보호정책과 마케팅에만 집중하게 되면 해당 솔루션들의 약점들을 놓칠 수 있습니다. When you're looking for a more private solution, you should determine what the underlying problem is and find technical solutions to that problem. For example, you may want to avoid Google Drive, which gives Google access to all of your data. The underlying problem in this case is lack of E2EE, so you should make sure that the provider you switch to actually implements E2EE, or use a tool (like Cryptomator) which provides E2EE on any cloud provider. Switching to a "privacy-focused" provider (that doesn't implement E2EE) doesn't solve your problem: it just shifts trust from Google to that provider.
      - 
        "@type": Question
        name: How complicated should my threat model be?
        acceptedAnswer:
          "@type": Answer
          text: |
            We often see people describing privacy threat models that are overly complex. Often, these solutions include problems like many different email accounts or complicated setups with lots of moving parts and conditions. The replies are usually answers to "What is the best way to do X?"
            Finding the "best" solution for yourself doesn't necessarily mean you are after an infallible solution with dozens of conditions—these solutions are often difficult to work with realistically. As we discussed previously, security often comes at the cost of convenience.
---

## "Open-source software is always secure" or "Proprietary software is more secure"

These myths stem from a number of prejudices, but whether the source code is available and how software is licensed does not inherently affect its security in any way. ==Open-source software has the *potential* to be more secure than proprietary software, but there is absolutely no guarantee this is the case.== When you evaluate software, you should look at the reputation and security of each tool on an individual basis.

Open-source software *can* be audited by third-parties, and is often more transparent about potential vulnerabilities than proprietary counterparts. It also allows you to review the code and disable any suspicious functionality you find yourself. However, *unless you do so*, there is no guarantee that code has ever been evaluated, especially with smaller software projects. The open development process has also sometimes been exploited to introduce new vulnerabilities into even large projects.[^1]

On the flip side, proprietary software is less transparent, but that doesn't imply that it's not secure. Major proprietary software projects can be audited internally and by third-party agencies, and independent security researchers can still find vulnerabilities with techniques like reverse engineering.

To avoid biased decisions, it's *vital* that you evaluate the privacy and security standards of the software you use.

## "신뢰하는 대상을 바꾸면 프라이버시를 강화할 수 있다"

VPN과 같은 솔루션들에 대해 논의할 때 "신뢰하는 대상을 변경한다"는 말이 자주 나옵니다. (VPN은 ISP로부터 VPN 제공자로 신뢰 대상을 바꿉니다) 이는 ISP로부터 브라우징 데이터를 보호하지만, 당신이 선택한 VPN 제공자는 이 브라우징 데이터에 접근할 수 있습니다. 즉, 데이터가 모든 이로부터 보호되는 것이 아닙니다. 따라서:

1. 새로 신뢰할 제공업체를 신중하게 선택해야 합니다.
2. 종단간 암호화와 같은 기타 기술을 같이 이용해서 데이터를 지켜야 합니다. 기존 제공업체 대신 다른 업체를 신뢰하는 것만으로는 데이터 보호라고 보기 어렵습니다.

## "프라이버시를 중점으로 둔 솔루션은 본질적으로 신뢰할 수 있다"

제품 또는 서비스의 개인정보 보호정책과 마케팅에만 집중하게 되면 해당 솔루션들의 약점들을 놓칠 수 있습니다. When you're looking for a more private solution, you should determine what the underlying problem is and find technical solutions to that problem. For example, you may want to avoid Google Drive, which gives Google access to all of your data. The underlying problem in this case is lack of E2EE, so you should make sure that the provider you switch to actually implements E2EE, or use a tool (like [Cryptomator](../encryption.md#cryptomator-cloud)) which provides E2EE on any cloud provider. Switching to a "privacy-focused" provider (that doesn't implement E2EE) doesn't solve your problem: it just shifts trust from Google to that provider.

The privacy policies and business practices of providers you choose are very important, but should be considered secondary to technical guarantees of your privacy: You shouldn't shift trust to another provider when trusting a provider isn't a requirement at all.

## "복잡할수록 좋다"

We often see people describing privacy threat models that are overly complex. Often, these solutions include problems like many different email accounts or complicated setups with lots of moving parts and conditions. The replies are usually answers to "What is the best way to do *X*?"

Finding the "best" solution for yourself doesn't necessarily mean you are after an infallible solution with dozens of conditions—these solutions are often difficult to work with realistically. As we discussed previously, security often comes at the cost of convenience. Below, we provide some tips:

1. ==Actions need to serve a particular purpose:== think about how to do what you want with the fewest actions.
2. ==Remove human failure points:== We fail, get tired, and forget things. To maintain security, avoid relying on manual conditions and processes that you have to remember.
3. ==Use the right level of protection for what you intend.== We often see recommendations of so-called law-enforcement or subpoena-proof solutions. These often require specialist knowledge and generally aren't what people want. There's no point in building an intricate threat model for anonymity if you can be easily de-anonymized by a simple oversight.

So, how might this look?

One of the clearest threat models is one where people *know who you are* and one where they do not. There will always be situations where you must declare your legal name and there are others where you don't need to.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    !!! tip
   
        When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](https://www.getmonero.org/). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: One notable example of this is the [2021 incident in which University of Minnesota researchers introduced three vulnerabilities into the Linux kernel development project](https://cse.umn.edu/cs/linux-incident).
