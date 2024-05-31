---
title: "일반적인 오해"
icon: 'material/robot-confused'
description: 프라이버시는 단순한 주제가 아닙니다. 홍보성 문구나 여타 잘못된 정보에 현혹당하지 않도록 조심해야 합니다.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: 오픈 소스 소프트웨어는 본질적으로 안전한가요?
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
            제품 또는 서비스의 개인정보 보호정책과 마케팅에만 집중하게 되면 해당 솔루션들의 약점들을 놓칠 수 있습니다. 솔루션을 찾을 때에는 우선 근본적인 문제가 무엇인지를 파악한 후, 그 문제에 대응하는 기술적인 해결책을 찾는 방향으로 나아가야 합니다. 예시로, 자신의 데이터를 Google에게 넘겨줄 수 있다는 이유로 Google Drive를 피하고 싶을 수 있습니다. 여기서의 근본적인 문제는 종단간 암호화가 없다는 것입니다. 따라서 새로운 서비스 제공자를 선택할 경우, 그 제공자가 종단간 암호화를 도입했는지 확인하거나, 종단간 암호화를 직접 도입할 수 있게 해주는 프로그램를 사용할 수 있습니다. 예시로는 Cryptomator가 있습니다. 프라이버시에 중점을 두었다고 광고하지만 종단간 암호화를 도입하지 않은 제공자는 이 문제의 해결책이 될 수 없습니다. 이는 그저 Google에서 해당 제공자로 신뢰 대상을 변경할 뿐입니다.
      - 
        "@type": Question
        name: 위협 모델은 얼마나 복잡하게 만들어야 하나요?
        acceptedAnswer:
          "@type": Answer
          text: |
            가끔 과도하게 복잡한 위협 모델을 가진 사람들을 볼 수 있습니다. 이런 솔루션들은 너무 많은 이메일 계정들이나 복잡한 설정과 같은 문제점을 지니고 있을 수 있습니다. 이런 질문의 답변들은 대부분 "X를 수행하는 최선의 방법"과 같습니다.
            자신에게 최고인 솔루션은 수십가지의 조건하에서도 작동하는 것을 가리키는 것이 아닙니다. 이런 솔루션들은 대개 현실적으로 사용하기 어렵습니다. 앞서 설명한 것과 같이, 보안과 편의성은 서로 반대되는 관계를 가집니다.
---

## "오픈 소스 소프트웨어는 항상 안전하다" 혹은 "독점 소프트웨어가 더 안전하다"

이런 오해는 여러 편견에서 비롯된 것입니다. 소스 코드 공개 여부이나 라이선스 방식 자체는 보안에 어떠한 영향도 미치지 않습니다. ==오픈 소스 소프트웨어는 독점 소프트웨어보다 보안이 뛰어날 *가능성*이 존재하지만, 반드시 그러하리라는 보장은 없습니다.== 특정 소프트웨어를 평가할 때는 해당 소프트웨어의 평판과 보안을 개별적으로 판단해야 합니다.

오픈 소스 소프트웨어는 제3자로부터 검증(감사)받는 것이 *가능하고*, 잠재적인 취약점을 취급하는 데에 있어서 독점 소프트웨어보다 투명하게 이루어지는 경우가 많습니다. 하고자 한다면 자신이 직접 코드를 검토할 수도 있으며, 의심스러운 기능은 비활성화 하는 것도 가능합니다. 하지만 이론상 가능한 것과는 별개로 (특히 소규모 소프트웨어 프로젝트일수록) 해당 코드가 검증되었다는 보장은 없습니다. The open development process has also sometimes been exploited to introduce new vulnerabilities known as <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>, which are discussed further in our [Common Threats](common-threats.md) page.[^1]

반면 독점 소프트웨어는 투명성이 상대적으로 떨어지지만, 그렇다고 해서 안전하지 않다는 뜻은 아닙니다. 메이저 독점 소프트웨어는 내부 및 외부 기관에서 감사를 진행할 수 있으며, 외부 보안 연구원도 리버스 엔지니어링 등의 기술을 통해 취약점을 발견할 수 있습니다.

편향된 판단을 내리지 않기 위해선 소프트웨어의 프라이버시 및 보안 수준을 객관적으로 평가하는 것이 중요합니다.

## "신뢰하는 대상을 바꾸면 프라이버시를 강화할 수 있다"

VPN과 같은 솔루션들에 대해 논의할 때 "신뢰하는 대상을 변경한다"는 말이 자주 나옵니다. (VPN은 ISP로부터 VPN 제공자로 신뢰 대상을 바꿉니다) 이는 ISP로부터 브라우징 데이터를 보호하지만, 당신이 선택한 VPN 제공자는 이 브라우징 데이터에 접근할 수 있습니다. 즉, 데이터가 모든 이로부터 보호되는 것이 아닙니다. 따라서:

1. 새로 신뢰할 제공업체를 신중하게 선택해야 합니다.
2. 종단간 암호화와 같은 기타 기술을 같이 이용해서 데이터를 지켜야 합니다. 기존 제공업체 대신 다른 업체를 신뢰하는 것만으로는 데이터 보호라고 보기 어렵습니다.

## "프라이버시를 중점으로 둔 솔루션은 본질적으로 신뢰할 수 있다"

제품 또는 서비스의 개인정보 보호정책과 마케팅에만 집중하게 되면 해당 솔루션들의 약점들을 놓칠 수 있습니다. 솔루션을 찾을 때에는 우선 근본적인 문제가 무엇인지를 파악한 후, 그 문제에 대응하는 기술적인 해결책을 찾는 방향으로 나아가야 합니다. 예시로, 자신의 데이터를 Google에게 넘겨줄 수 있다는 이유로 Google Drive를 피하고 싶을 수 있습니다. The underlying problem in this case is lack of E2EE, so you should make sure that the provider you switch to actually implements E2EE, or use a tool (like [Cryptomator](../encryption.md#cryptomator-cloud)) which provides E2EE on any cloud provider. 프라이버시에 중점을 두었다고 광고하지만 종단간 암호화를 도입하지 않은 제공자는 이 문제의 해결책이 될 수 없습니다. 이는 그저 Google에서 해당 제공자로 신뢰 대상을 변경할 뿐입니다.

The privacy policies and business practices of providers you choose are very important, but should be considered secondary to technical guarantees of your privacy: You shouldn't shift trust to another provider when trusting a provider isn't a requirement at all.

## "복잡할수록 좋다"

간혹 위협 모델을 지나치게 복잡하게 만드는 사람들을 볼 수 있습니다. 이런 솔루션들은 너무 많은 이메일 계정들이나 복잡한 설정과 같은 문제점을 지니고 있을 수 있습니다. The replies are usually answers to "What is the best way to do *X*?"

자신에게 최고인 솔루션은 수십가지의 조건하에서도 작동하는 것을 가리키는 것이 아닙니다. 이런 솔루션들은 대개 현실적으로 사용하기 어렵습니다. 앞서 설명한 것과 같이, 보안과 편의성은 서로 반대되는 관계를 가집니다. Below, we provide some tips:

1. ==행동은 목적을 가지고 이루어져야 합니다.== 최소한의 노력으로 목적을 달성하는 방법을 생각해보세요.
2. ==자신의 의지력에 의존하지 마세요.== 사람은 실패하고, 지치고, 깜박하기 마련입니다. To maintain security, avoid relying on manual conditions and processes that you have to remember.
3. ==Use the right level of protection for what you intend.== We often see recommendations of so-called law-enforcement or subpoena-proof solutions. These often require specialist knowledge and generally aren't what people want. There's no point in building an intricate threat model for anonymity if you can be easily de-anonymized by a simple oversight.

So, how might this look?

One of the clearest threat models is one where people *know who you are* and one where they do not. There will always be situations where you must declare your legal name and there are others where you don't need to.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Tip</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](../cryptocurrency.md#monero). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added a obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
