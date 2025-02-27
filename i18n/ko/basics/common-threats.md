---
title: "일반적인 위협"
icon: 'material/eye-outline'
description: 위협 모델은 개개인마다 다르지만, 이 사이트의 방문자 대부분이 관심을 가질 사항입니다.
---

전반적으로, Privacy Guides의 권장 목록은 대부분의 사람들에게 적용되는 [위협](threat-modeling.md) 혹은 목표로 분류됩니다. 여러분이 사용하는 툴 및 서비스는 여러분의 목표에 따라 달라지며, ==이러한 위협 가능성에 대한 관심도는 사람마다 다를 수 있습니다.== You may have specific threats outside these categories as well, which is perfectly fine! 핵심은 '사용하기로 선택한 툴의 장단점을 이해하는 것' 입니다. 모든 위협으로부터 여러분을 완벽히 보호할 수 있는 툴은 존재하지 않기 때문입니다.

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

대응해야 할 위협의 우선 순위는 개인의 관심도에 따라 바뀔 수 있습니다. For example, a software developer with access to valuable or critical data may be primarily concerned with <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span> and <span class="pg-red">:material-target-account: Targeted Attacks</span>. They will likely still want to protect their personal data from being swept up in <span class="pg-blue">:material-eye-outline: Mass Surveillance</span> programs. 마찬가지로, 대부분의 사람들이 가장 우려하는 위협은 개인 데이터의 <span class="pg-green">:material-account-search: 공개 노출</span>일 테지만, 기기 감염 멀웨어 등의 <span class="pg-orange">:material-bug-outline: 수동적 공격</span> 보안 문제 또한 주의해야 합니다.

## 익명성 vs 프라이버시

<span class="pg-purple">:material-incognito: 익명성(Anonymity)</span>

익명성은 프라이버시와 혼동되는 경우가 많지만, 서로 다른 개념입니다. '프라이버시'는 여러분의 데이터가 사용 및 공유되는 방식을 여러분이 선택할 권리를 의미하고, '익명성'은 온라인 활동을 실제 신원과 완전히 분리하는 것을 의미합니다.

예를 들자면, 내부 고발자나 언론인은 완전한 익명성을 요구하는 극단적인 위협 모델이 필요합니다. 무엇을 하는지, 어떤 데이터를 가지고 있는지를 숨기고, 악의적인 상대나 정부로부터의 해킹을 막을 뿐만 아니라, '자신이 누구인지'도 완전히 숨겨야 합니다. 익명성, 프라이버시, 보안을 위해서라면 어떤 편의성도 포기할 수 있을 겁니다. 목숨이 달렸을 테니까요. 대부분의 사람들은 이렇게까지 할 필요는 없습니다.

## 보안, 프라이버시

<span class="pg-orange">:material-bug-outline: 수동적 공격(Passive Attacks)</span>

보안, 프라이버시도 자주 혼동됩니다. 프라이버시를 지키기 위해서는 보안이 필요하기 때문입니다. 프라이버시 중점적으로 설계된 서비스라 하여도 해당 서비스의 보안이 취약해 어떤 공격자가 손쉽게 데이터를 유출 및 악용할 수 있다면 무용지물입니다. 하지만, 반대로 뛰어난 보안에 프라이버시가 항상 뒤따라오는 것은 아닙니다. 완벽한 예시로 Google이 있습니다. Google은 업계 최고의 보안 전문가를 고용해 인프라를 보호하여 보안 사고가 거의 발생하지 않았습니다. Google이 제공하는 서비스의 보안은 매우 안전하지만, Google 무료 서비스(Gmail, YouTube 등)에서 자신의 데이터가 비공개라고 생각하는 사람은 거의 없습니다.

애플리케이션 보안 측면에서는, 일반적으로 우리는 사용하는 소프트웨어가 악성 소프트웨어인지 혹은 언젠가 악성 소프트웨어가 될지는 알지 못합니다(때로는 알 방법이 없습니다). 아무리 믿을 만한 개발자라 해도, 훗날에 악용될 수 있는 심각한 취약점이 존재하지 않을 거라는 보장은 일반적으로 없습니다.

악성 소프트웨어가 일으킬 *수도 있는* 피해를 최소화하려면 구획화를 이용한 보안을 적용해야합니다. 작업 종류마다 다른 컴퓨터를 사용하거나, 애플리케이션을 연관 그룹별로 분류해 가상 머신에서 사용하거나, 애플리케이션 샌드박스 격리 및 필수 접근 제어 기능에 특화된 보안 운영체제를 사용하는 등의 방법이 있습니다.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

일반적으로 모바일 운영 체제는 데스크톱 운영 체제보다 애플리케이션 샌드박스 기능이 뛰어납니다. 모바일 운영체제에서는 앱이 루트 권한을 얻을 수 없고, 시스템 리소스에 접근하려면 권한이 필요합니다.

데스크톱 운영 체제는 보통 적절한 샌드박스 기능 면에서 뒤처집니다. ChromeOS has similar sandboxing capabilities to Android, and macOS has full system permission control (and developers can opt in to sandboxing for applications). 하지만 이러한 운영 체제는 식별 정보를 각 OEM에 전송합니다. Linux는 대체로 시스템 공급 업체에 정보를 보내지 않지만, 취약점 및 악성 앱으로부터의 보호 기능은 미흡합니다. This can be mitigated somewhat with specialized distributions which make significant use of virtual machines or containers, such as [Qubes OS](../desktop.md#qubes-os).

</div>

## Attacks against Specific Individuals

<span class="pg-red">:material-target-account: 표적 공격(Targeted Attacks)</span>

특정 인물을 대상으로 하는 표적 공격은 더욱 대응하기 어렵습니다. 흔한 예시로는 이메일을 통한 악성 문서 전송, 브라우저 및 운영 체제 등의 취약점 악용, 물리적 공격 등이 있습니다. 표적 공격이 우려된다면, 보다 고급 위협 완화 전략이 필요합니다.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

**웹 브라우저**, **이메일 클라이언트**, **오피스 애플리케이션**은 설계상 외부에서 전송된 신뢰할 수 없는 코드를 실행하도록 되어있습니다. 여러 가상 머신을 사용해 이러한 애플리케이션을 호스트 시스템과 분리하는 것은 애플리케이션 취약점으로부터 시스템의 다른 영역이 손상될 가능성을 줄이는 방법 중 하나입니다. 이런 격리 작업을 편리하게 만들어주는 기술로는 Qubes OS/Microsoft Defender Application Guard 등이 있습니다.

</div>

If you are concerned about **physical attacks** you should use an operating system with a secure verified boot implementation, such as Android, iOS, macOS, or [Windows (with TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). 또한 드라이브를 암호화하고, 운영 체제에서 TPM/Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1)/[Element](https://developers.google.com/android/security/android-ready-se)를 이용해 암호 입력 시도를 제한해야 합니다. 대부분의 데스크톱 운영체제는 사용자별 데이터를 암호화하지 않으므로, 신뢰하지 않는 사람과 컴퓨터를 공유하지 말아야 합니다.

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

<span class="pg-teal">:material-server-network: 서비스 제공자/제공 업체(Service Providers)</span>

우리는 사실상 모든 것이 인터넷에 연결된 세상에 살고 있습니다. '비공개' 메시지, 이메일, 소셜 상호 작용은 보통 어딘가의 서버에 저장됩니다. 일반적으로, 여러분이 누군가에게 메시지를 보내면 해당 메시지는 서버에 저장되고, 여러분의 친구가 메시지를 읽으려 할 때 서버에서 메시지를 보여줍니다.

이 방식의 명백한 문제점은 서비스 제공자(혹은 서버에 침투한 해커)가 언제든지 마음대로 여러분의 대화를 여러분 몰래 살펴볼 수 있다는 것입니다. SMS 문자 메시지, Telegram, Discord 등 일반적인 서비스의 대부분이 가지고 있는 문제입니다.

다행히, 송신자와 수신자 간의 통신을 서버로 전송하기 전에 암호화하는 E2EE를 적용하면 이러한 문제를 완화할 수 있습니다. 서비스 제공 업체가 양측 당사자의 개인 키에 접근하지 못한다는 가정 하에, 메시지의 기밀성이 보장됩니다.

<div class="admonition note" markdown>
<p class="admonition-title">Note on Web-based Encryption</p>

실질적으로 모든 E2EE 구현체가 동일한 유효성을 갖는 것은 아닙니다. [Signal](../real-time-communication.md#signal) 같은 애플리케이션은 기기에서 네이티브로 실행되며, 여러번 설치하더라도 언제나 완벽히 동일한 애플리케이션이 설치됩니다. 서비스 제공 업체가 여러분의 개인 키를 탈취하기 위해 [백도어](https://ko.wikipedia.org/wiki/%EB%B0%B1%EB%8F%84%EC%96%B4)를 도입하더라도, 차후에 [리버스 엔지니어링](https://ko.wikipedia.org/wiki/%EC%97%AD%EA%B3%B5%ED%95%99)을 통해 탐지될 수 있습니다.

On the other hand, web-based E2EE implementations, such as Proton Mail's web app or Bitwarden's *Web Vault*, rely on the server dynamically serving JavaScript code to the browser to handle cryptography. 악성 서버는 사용자를 표적으로 삼아 악성 자바스크립트 코드를 전송해 암호화 키를 탈취 가능하며, 이 경우 사용자는 이를 알아차리기 매우 어렵습니다. 만약 사용자가 공격을 알아차리더라도 제공 업체의 책임을 입증하기란 매우 어렵습니다. 서버에서 사람마다 웹 클라이언트를 다르게 제공하는 것이 가능하기 때문입니다.

따라서, 가능하면 웹 클라이언트 대신 네이티브 애플리케이션을 사용해야 합니다.

</div>

E2EE를 적용하더라도 여전히 서비스 제공 업체는 (일반적으로 보호되지 않는) **메타데이터**에 기반하여 여러분의 정보를 수집하고 프로파일링할 수 있습니다. While the service provider can't read your messages, they can still observe important things, such as whom you're talking to, how often you message them, and when you're typically active. 메타데이터에도 보호가 적용되는 경우는 매우 드뭅니다. 만약 여러분의 [위협 모델](threat-modeling.md)이 메타데이터 보호 또한 필요로 한다면, 사용하는 소프트웨어의 기술 문서를 주의 깊게 확인하여 메타데이터 최소화 혹은 보호가 존재하는지 살펴봐야 합니다.

## 대중 감시 프로그램

<span class="pg-blue">:material-eye-outline: 대중 감시(Mass Surveillance)</span>

'대중 감시'는 전체(혹은 상당한 부분의) 인구의 '행동, 다양한 활동 혹은 정보'를 모니터링하는 전방위적 노력을 뜻합니다.[^1] [2013년 에드워드 스노든이 폭로한 정부 프로그램](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)) 등을 가리키는 경우가 많습니다. 하지만, 기업이 정부 기관 대신 수행하거나, 기업 자체가 주도적으로 수행하기도 합니다.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France, you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

정부는 테러 대응 및 범죄 예방에 필요한 수단으로 대중 감시 프로그램을 정당화하는 경우가 많습니다. However, as breaches of human rights, they're most often used to disproportionately target minority groups and political dissidents, among others.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

In the face of Edward Snowden's disclosures of government programs such as [PRISM](https://en.wikipedia.org/wiki/PRISM) and [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), intelligence officials also admitted that the NSA had for years been secretly collecting records about virtually every American’s phone calls — who’s calling whom, when those calls are made, and how long they last. NSA가 이러한 정보를 매일 수집할 경우, 어떤 사람이 목사, 낙태 시술자, 중독 상담사, 자살 예방 상담사와 전화했는지 등 사람들의 삶과 관계성에 대해 극도로 민감한 정보를 파악할 수 있습니다.

</div>

미국에서 대중 감시가 증가하고 있음에도 불구하고, 정부는 215조항과 같은 대중 감시 프로그램이 실제 범죄나 테러 음모를 저지하는 데 있어 '고유한 가치가 거의 없다'라는 사실을 발견했으며, 대부분의 노력은 FBI의 표적 감시 프로그램과 중복되는 것으로 나타났습니다.[^2]

Online, you can be tracked via a variety of methods, including but not limited to:

- 여러분의 IP 주소
- 브라우저 쿠키
- 여러분이 웹사이트에 제출한 데이터
- 여러분의 브라우저/기기 핑거프린트
- 결제 수단 연관성

If you're concerned about mass surveillance programs, you can use strategies like compartmentalizing your online identities, blending in with other users, or, whenever possible, simply avoiding giving out identifying information.

## Surveillance as a Business Model

<span class="pg-brown">:material-account-cash: 감시 자본주의(Surveillance Capitalism)</span>

> 감시 자본주의는 이윤 창출을 주요 목적으로 하여 개인 데이터를 수집하고 상품화하는 데 중점을 둔 경제 시스템입니다.[^3]

대중 사이에서, 사기업의 추적 및 감시에 대한 우려는 점점 더 커지고 있습니다. Pervasive 광고 네트워크는(Google, Facebook이 운영하는 광고가 이에 해당) 해당 업체의 사이트뿐만 아니라 인터넷 전반에 퍼져서 여러분의 행동을 추적하고 있습니다. 콘텐츠 차단기 등의 툴을 써서 광고 네트워크 요청을 제한하고, 서비스의 프라이버시 정책을 꼼꼼히 읽으면 (추적을 완전히 방지할 수는 없지만) 기본적인 적들을 피하는 데에 도움이 됩니다.[^4]

Additionally, even companies outside the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. 여러분이 사용 중인 서비스가 일반적인 AdTech/추적 비즈니스 모델에 속하지 않는다고 해서 여러분의 데이터가 안전하다고 할 수는 없습니다. 기업 데이터 수집을 방어하는 가장 강력한 방법은 가능한 한 여러분의 데이터를 암호화하거나 난독화하는 것입니다. 업체들 사이에서 데이터의 상관성을 알아내기 어려워지기 때문에, 여러분에 대한 프로필을 구축하기 어려워집니다.

## 정보 공개 제한

<span class="pg-green">:material-account-search: 공개 노출(Public Exposure)</span>

여러분의 데이터를 남들로부터 지키는 가장 좋은 방법은, 애초에 데이터를 공개하지 않는 것입니다. '온라인에서 자신에 대한 원치 않는 정보를 삭제하기'는 자신의 프라이버시를 되찾기 위한 가장 훌륭한 첫걸음입니다.

- [계정 삭제 가이드 살펴보기 :material-arrow-right-drop-circle:](account-deletion.md)

정보를 공유하는 사이트에서는 반드시 계정 개인정보 보호 설정을 확인하여 데이터가 원치 않게 널리 퍼지지 않도록 해야 합니다. 예를 들어, 가능하면 계정에서 '비공개 모드' 같은 옵션을 활성화해야 합니다. 계정 비공개 모드를 활성화하면 여러분의 계정이 검색 엔진에 잡히지 않고 여러분 허락 없이 계정을 살펴볼 수 없습니다.

실제 정보를 제공해서는 안 되는 사이트에 이미 실제 정보를 제출했다면, 해당 온라인 신원에 관련된 허위 정보를 제출하는 등의 전략을 사용할 수 있습니다. 이렇게 하면 가짜 정보와 여러분에 대한 실제 정보를 구별할 수 없습니다.

## 검열 회피

<span class="pg-blue-gray">:material-close-outline: 검열(Censorship)</span>

'온라인 검열'은 전체주의 정부, 네트워크 관리자, 서비스 제공 업체 등 다양한 주체에 의해 (그 정도 또한 다양하게) 이루어질 수 있습니다. 의사소통을 통제하고 정보 접근을 제한하는 '검열'은 표현의 자유 인권과 절대 양립할 수 없습니다.[^5]

Twitter, Facebook 같은 플랫폼이 대중의 요구, 시장의 압력, 정부 기관의 압력에 굴복하면서, 기업 플랫폼에서의 검열은 점점 보편화되고 있습니다. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

검열 위협이 우려될 경우, [Tor](../advanced/tor-overview.md) 등의 기술을 사용해 검열을 우회할 수 있으며, [Matrix](../real-time-communication.md#element) 처럼 중앙 집중식 계정 시스템이 없는(플랫폼이 독단적으로 누군가의 계정을 차단할 수 없는) 검열 방지 통신 플랫폼을 지원할 수 있습니다.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

'검열 회피' 자체는 어렵지 않습니다. 하지만 여러분이 검열을 회피하고 있다는 사실을 감추는 것은 매우 문제가 될 수 있습니다.

여러분의 적대자가 가진 네트워크 감시 능력은 어느정도인지, 여러분 스스로 자신의 검열 회피 행동에 대해 타당한 구실을 가지고 있는지를 고려해야 합니다. 예를 들어, [암호화 DNS](../advanced/dns-overview.md#what-is-encrypted-dns)를 사용하면 기초적인 DNS 기반 검열 시스템을 우회할 수 있지만, 방문 중인 사이트가 ISP에 노출되는 것을 숨길 수는 없습니다. VPN/Tor를 사용하면 네트워크 관리자로부터 여러분이 어떤 사이트를 방문하는지 숨길 수 있지만, VPN/Tor 네트워크를 사용 중이라는 것 자체는 숨길 수 없습니다. (Obfs4proxy, Meek, Shadowsocks 등) Pluggable transports로는 일반적인 VPN/Tor 프로토콜 차단 방화벽을 우회할 수는 있지만, 프로빙(Probing)이나 [심층 패킷 검사(Deep Packet Inspection)](https://en.wikipedia.org/wiki/Deep_packet_inspection) 같은 방법을 사용하면 우회 시도를 탐지할 수 있습니다.

</div>

검열을 우회할 경우 발생할 수 있는 위험 및 결과, 적대자의 능력을 항상 고려해야 합니다. 사용할 소프트웨어를 신중하게 선택하고, 적발될 경우를 대비한 백업 계획을 세워야 합니다.

[^1]: Wikipedia: [*Mass Surveillance*](https://en.wikipedia.org/wiki/Mass_surveillance) and [*Surveillance*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: 미국 프라이버시 및 시민 자유 감독 위원회: [*215조항에 따라 수행된 전화 통화 기록 프로그램에 대한 보고서*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. 다른 완화 기술도 추가로 사용해야 합니다.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
