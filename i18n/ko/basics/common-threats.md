---
title: "일반적인 위협"
icon: 'material/eye-outline'
description: 위협 모델은 개개인마다 다르지만, 이 사이트의 방문자 대부분이 관심을 가질 사항입니다.
---

전반적으로, Privacy Guides의 권장 목록은 대부분의 사람들에게 적용되는 [위협](threat-modeling.md) 혹은 목표로 분류됩니다. 여러분이 사용하는 툴 및 서비스는 여러분의 목표에 따라 달라지며, ==이러한 위협 가능성에 대한 관심도는 사람마다 다를 수 있습니다.== 혹시나 여기에 정리되지 않은 종류의 위협을 겪고 있더라도 상관 없습니다! 핵심은 '사용하기로 선택한 툴의 장단점을 이해하는 것' 입니다. 모든 위협으로부터 여러분을 완벽히 보호할 수 있는 툴은 존재하지 않기 때문입니다.

- <span class="pg-purple">:material-incognito: 익명성</span> - 온라인 활동에서 실제 신원을 보호하여, *여러분의* 신원을 밝혀내려는 사람들로부터 여러분을 보호합니다.
- <span class="pg-red">:material-target-account: 표적 공격</span> - *당신의* 데이터나 기기에 세부적으로 접근하려는 해커 및 그 외 악의적인 상대로부터 보호합니다.
- <span class="pg-orange">:material-bug-outline: 수동적 공격</span> - 멀웨어, 데이터 유출 등 다수의 사람을 한꺼번에 대상으로 삼는 공격으로부터 보호합니다.
- <span class="pg-teal">:material-server-network: 서비스 제공자</span> - (여러분의 데이터를 서버에서 읽을 수 없도록 하는 E2EE 등을 이용하여) 서비스 제공자로부터 여러분의 데이터를 보호합니다.
- <span class="pg-blue">:material-eye-outline: 대중 감시</span> - 여러분의 활동을 추적하기 위해 협력하는 정부 기관, 단체, 웹사이트, 서비스로부터 보호합니다.
- <span class="pg-brown">:material-account-cash: 감시 자본주의</span> - Google, Facebook 등의 거대 광고 네트워크 및 기타 수많은 제3자 데이터 수집 업체로부터 여러분을 보호합니다.
- <span class="pg-green">:material-account-search: 공개 노출</span> - 여러분에 대한 정보를 (검색 엔진이나 일반 대중이) 온라인에서 접근하는 것을 제한합니다.
- <span class="pg-blue-gray">:material-close-outline: 검열</span> - 정보 접근을 제한하는 검열을 회피하고, 온라인상에서 자신의 주장이 검열되는 것을 방지합니다.

대응해야 할 위협의 우선 순위는 개인의 관심도에 따라 바뀔 수 있습니다. 예를 들어, 중요한 데이터에 접근할 수 있는 소프트웨어 개발자가 가장 신경쓰는 위협은 <span class="pg-red">:material-target-account: 표적 공격</span>일 테지만, 개인 데이터를 <span class="pg-blue">:material-eye-outline: 대중 감시</span> 프로그램들로부터 보호하고 싶은 의향 또한 가지고 있을 수도 있습니다. 마찬가지로, 대부분의 사람들이 가장 우려하는 위협은 개인 데이터의 <span class="pg-green">:material-account-search: 공개 노출</span>일 테지만, 기기 감염 멀웨어 등의 <span class="pg-orange">:material-bug-outline: 수동적 공격</span> 보안 문제 또한 주의해야 합니다.

## 익명성 vs 프라이버시

<span class="pg-purple">:material-incognito: 익명성(Anonymity)</span>

익명성은 프라이버시와 혼동되는 경우가 많지만, 서로 다른 개념입니다. '프라이버시'는 여러분의 데이터가 사용 및 공유되는 방식을 여러분이 선택할 권리를 의미하고, '익명성'은 온라인 활동을 실제 신원과 완전히 분리하는 것을 의미합니다.

예를 들자면, 내부 고발자나 언론인은 완전한 익명성을 요구하는 극단적인 위협 모델이 필요합니다. 무엇을 하는지, 어떤 데이터를 가지고 있는지를 숨기고, 악의적인 상대나 정부로부터의 해킹을 막을 뿐만 아니라, '자신이 누구인지'도 완전히 숨겨야 합니다. 익명성, 프라이버시, 보안을 위해서라면 어떤 편의성도 포기할 수 있을 겁니다. 목숨이 달렸을 테니까요. 대부분의 사람들은 이렇게까지 할 필요는 없습니다.

## 보안, 프라이버시

<span class="pg-orange">:material-bug-outline: 수동적 공격(Passive Attacks)</span>

보안, 프라이버시도 자주 혼동됩니다. 프라이버시를 지키기 위해서는 보안이 필요하기 때문입니다. 프라이버시 중점적으로 설계된 서비스라 하여도 해당 서비스의 보안이 취약해 어떤 공격자가 손쉽게 데이터를 유출 및 악용할 수 있다면 무용지물입니다. 하지만, 반대로 뛰어난 보안에 프라이버시가 항상 뒤따라오는 것은 아닙니다. 완벽한 예시로 Google이 있습니다. Google은 업계 최고의 보안 전문가를 고용해 인프라를 보호하여 보안 사고가 거의 발생하지 않았습니다. Google이 제공하는 서비스의 보안은 매우 안전하지만, Google 무료 서비스(Gmail, YouTube 등)에서 자신의 데이터가 비공개라고 생각하는 사람은 거의 없습니다.

애플리케이션 보안 측면에서는, 일반적으로 우리는 사용하는 소프트웨어가 악성 소프트웨어인지 혹은 언젠가 악성 소프트웨어가 될지는 알지 못합니다(때로는 알 방법이 없습니다). 아무리 믿을 만한 개발자라 해도, 훗날에 악용될 수 있는 심각한 취약점이 존재하지 않을 거라는 보장은 일반적으로 없습니다.

악성 소프트웨어가 일으킬 *수도 있는* 피해를 최소화하려면 구획화를 이용한 보안을 적용해야합니다. 작업 종류마다 다른 컴퓨터를 사용하거나, 애플리케이션을 연관 그룹별로 분류해 가상 머신에서 사용하거나, 애플리케이션 샌드박스 격리 및 필수 접근 제어 기능에 특화된 보안 운영체제를 사용하는 등의 방법이 있습니다.

!!! tip "도움말"

    일반적으로 모바일 운영 체제는 데스크톱 운영 체제보다 애플리케이션 샌드박스 기능이 뛰어납니다. 모바일 운영체제에서는 앱이 루트 권한을 얻을 수 없고, 시스템 리소스에 접근하려면 권한이 필요합니다.
    
    데스크톱 운영 체제는 보통 적절한 샌드박스 기능 면에서 뒤처집니다. ChromeOS는 Android와 유사한 샌드박스 기능을 제공하며, macOS는 전체 시스템 권한 제어 기능을 제공합니다(개발자는 애플리케이션의 샌드박스를 적용 여부를 선택할 수 있습니다). 하지만 이러한 운영 체제는 식별 정보를 각 OEM에 전송합니다. Linux는 대체로 시스템 공급 업체에 정보를 보내지 않지만, 취약점 및 악성 앱으로부터의 보호 기능은 미흡합니다. 이 문제는 [Qubes OS](../../desktop/#qubes-os) 등, 가상 머신/컨테이너를 적극적으로 사용하도록 특화된 배포판에서는 완화될 수 있습니다.

<span class="pg-red">:material-target-account: 표적 공격(Targeted Attacks)</span>

특정 인물을 대상으로 하는 표적 공격은 더욱 대응하기 어렵습니다. 흔한 예시로는 이메일을 통한 악성 문서 전송, 브라우저 및 운영 체제 등의 취약점 악용, 물리적 공격 등이 있습니다. 표적 공격이 우려된다면, 보다 고급 위협 완화 전략이 필요합니다.

!!! tip "도움말"

    **웹 브라우저**, **이메일 클라이언트**, **오피스 애플리케이션**은 설계상 외부에서 전송된 신뢰할 수 없는 코드를 실행하도록 되어있습니다. 여러 가상 머신을 사용해 이러한 애플리케이션을 호스트 시스템과 분리하는 것은 애플리케이션 취약점으로부터 시스템의 다른 영역이 손상될 가능성을 줄이는 방법 중 하나입니다. 이런 격리 작업을 편리하게 만들어주는 기술로는 Qubes OS/Microsoft Defender Application Guard 등이 있습니다.

**물리적 공격**이 우려된다면 Android, iOS, macOS, [Windows(TPM 사용)](https://docs.microsoft.com/en-us/windows/security/information-protection/secure-the-windows-10-boot-process) 등 보안 부팅이 구현된 운영 체제를 사용해야 합니다. 또한 드라이브를 암호화하고, 운영 체제에서 TPM/Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1)/[Element](https://developers.google.com/android/security/android-ready-se)를 이용해 암호 입력 시도를 제한해야 합니다. 대부분의 데스크톱 운영체제는 사용자별 데이터를 암호화하지 않으므로, 신뢰하지 않는 사람과 컴퓨터를 공유하지 말아야 합니다.

## 서비스 제공 업체로부터의 프라이버시

<span class="pg-teal">:material-server-network: 서비스 제공자/제공 업체(Service Providers)</span>

우리는 사실상 모든 것이 인터넷에 연결된 세상에 살고 있습니다. '비공개' 메시지, 이메일, 소셜 상호 작용은 보통 어딘가의 서버에 저장됩니다. 일반적으로, 여러분이 누군가에게 메시지를 보내면 해당 메시지는 서버에 저장되고, 여러분의 친구가 메시지를 읽으려 할 때 서버에서 메시지를 보여줍니다.

이 방식의 명백한 문제점은 서비스 제공자(혹은 서버에 침투한 해커)가 언제든지 마음대로 여러분의 대화를 여러분 몰래 살펴볼 수 있다는 것입니다. SMS 문자 메시지, Telegram, Discord 등 일반적인 서비스의 대부분이 가지고 있는 문제입니다.

다행히, 송신자와 수신자 간의 통신을 서버로 전송하기 전에 암호화하는 E2EE를 적용하면 이러한 문제를 완화할 수 있습니다. 서비스 제공 업체가 양측 당사자의 개인 키에 접근하지 못한다는 가정 하에, 메시지의 기밀성이 보장됩니다.

!!! note "웹 기반 암호화에 대한 참고 사항"

    실질적으로 모든 E2EE 구현체가 동일한 유효성을 갖는 것은 아닙니다. [Signal](../real-time-communication.md#signal) 같은 애플리케이션은 기기에서 네이티브로 실행되며, 여러번 설치하더라도 언제나 완벽히 동일한 애플리케이션이 설치됩니다. 서비스 제공 업체가 여러분의 개인 키를 탈취하기 위해 [백도어](https://ko.wikipedia.org/wiki/%EB%B0%B1%EB%8F%84%EC%96%B4)를 도입하더라도, 차후에 [리버스 엔지니어링](https://ko.wikipedia.org/wiki/%EC%97%AD%EA%B3%B5%ED%95%99)을 통해 탐지될 수 있습니다.
    
    반면, Proton Mail 웹메일이나 Bitwarden **웹 보관함** 같은 웹 기반 E2EE 구현체의 경우, 서버에서 동적으로 제공하는 자바스크립트 코드에 암호화 처리를 의존합니다. 악성 서버는 사용자를 표적으로 삼아 악성 자바스크립트 코드를 전송해 암호화 키를 탈취 가능하며, 이 경우 사용자는 이를 알아차리기 매우 어렵습니다. 만약 사용자가 공격을 알아차리더라도 제공 업체의 책임을 입증하기란 매우 어렵습니다. 서버에서 사람마다 웹 클라이언트를 다르게 제공하는 것이 가능하기 때문입니다.
    
    따라서, 가능하면 웹 클라이언트 대신 네이티브 애플리케이션을 사용해야 합니다.

E2EE를 적용하더라도 여전히 서비스 제공 업체는 (일반적으로 보호되지 않는) **메타데이터**에 기반하여 여러분의 정보를 수집하고 프로파일링할 수 있습니다. 서비스 제공 업체는 여러분의 메시지를 읽을 수는 없지만, 여러분이 누구와 대화하는지, 얼마나 자주 메시지를 주고받는지, 주로 언제 활동하는지 등 중요한 정보를 관찰 가능합니다. 메타데이터에도 보호가 적용되는 경우는 매우 드뭅니다. 만약 여러분의 [위협 모델](threat-modeling.md)이 메타데이터 보호 또한 필요로 한다면, 사용하는 소프트웨어의 기술 문서를 주의 깊게 확인하여 메타데이터 최소화 혹은 보호가 존재하는지 살펴봐야 합니다.

## 대중 감시 프로그램

<span class="pg-blue">:material-eye-outline: 대중 감시(Mass Surveillance)</span>

'대중 감시'는 전체(혹은 상당한 부분의) 인구의 '행동, 다양한 활동 혹은 정보'를 모니터링하는 전방위적 노력을 뜻합니다.[^1] [2013년 에드워드 스노든이 폭로한 정부 프로그램](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)) 등을 가리키는 경우가 많습니다. 하지만, 기업이 정부 기관 대신 수행하거나, 기업 자체가 주도적으로 수행하기도 합니다.

!!! abstract "감시 지도"

    감시 방법과, 미국의 특정 도시에서 어떻게 감시 체계를 운용하는지 자세히 알고 싶다면 [Electronic Frontier Foundation](https://www.eff.org/)의 [Atlas of Surveillance](https://atlasofsurveillance.org/)를 살펴보세요.
    
    프랑스의 경우, 비영리 단체인 La Quadrature du Net에서 운영하는 [Technolopolice website](https://technopolice.fr/villes/)를 살펴볼 수 있습니다.

정부는 테러 대응 및 범죄 예방에 필요한 수단으로 대중 감시 프로그램을 정당화하는 경우가 많습니다. 하지만 이는 분명한 인권 침해일 뿐만 아니라, 대중 감시는 소수 집단과 정치적 반체제 인사 등의 대상을 집중적으로 표적삼는 데에 가장 자주 사용됩니다.

!!! quote "ACLU: [*9.11 사건의 프라이버시 교훈: 대중 감시는 앞으로 나아갈 길이 아닙니다*](https://www.aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward)"

    정보 당국은 에드워드 스노든의 정부 프로그램([PRISM](https://en.wikipedia.org/wiki/PRISM), [Upstream](https://en.wikipedia.org/wiki/Upstream_collection) 등) 폭로에 직면하여, NSA가 수년간 사실상 모든 미국인의 전화 통화 기록(누가 누구랑 통화하는지, 언제 통화하는지, 얼마나 오래 통화하는지)을 비밀리에 수집해 왔음을 인정했습니다. NSA가 이러한 정보를 매일 수집할 경우, 어떤 사람이 목사, 낙태 시술자, 중독 상담사, 자살 예방 상담사와 전화했는지 등 사람들의 삶과 관계성에 대해 극도로 민감한 정보를 파악할 수 있습니다.

미국에서 대중 감시가 증가하고 있음에도 불구하고, 정부는 215조항과 같은 대중 감시 프로그램이 실제 범죄나 테러 음모를 저지하는 데 있어 '고유한 가치가 거의 없다'라는 사실을 발견했으며, 대부분의 노력은 FBI의 표적 감시 프로그램과 중복되는 것으로 나타났습니다.[^2]

온라인상에서 여러분은 다양한 방법을 통해 추적당할 수 있습니다.

- 여러분의 IP 주소
- 브라우저 쿠키
- 여러분이 웹사이트에 제출한 데이터
- 여러분의 브라우저/기기 핑거프린트
- 결제 수단 연관성

\[이 목록뿐만이 아닙니다].

대중 감시 프로그램을 우려하는 경우, 온라인 신원을 구별해 활동하거나, 다른 사용자 사이에 섞여들거나, 가능한 선에서 식별 정보를 최소화하는 등의 전략을 이용할 수 있습니다.

<span class="pg-brown">:material-account-cash: 감시 자본주의(Surveillance Capitalism)</span>

> 감시 자본주의는 이윤 창출을 주요 목적으로 하여 개인 데이터를 수집하고 상품화하는 데 중점을 둔 경제 시스템입니다.[^3]

대중 사이에서, 사기업의 추적 및 감시에 대한 우려는 점점 더 커지고 있습니다. Pervasive 광고 네트워크는(Google, Facebook이 운영하는 광고가 이에 해당) 해당 업체의 사이트뿐만 아니라 인터넷 전반에 퍼져서 여러분의 행동을 추적하고 있습니다. 콘텐츠 차단기 등의 툴을 써서 광고 네트워크 요청을 제한하고, 서비스의 프라이버시 정책을 꼼꼼히 읽으면 (추적을 완전히 방지할 수는 없지만) 기본적인 적들을 피하는 데에 도움이 됩니다.[^4]

Additionally, even companies outside of the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. You can't automatically assume your data is safe just because the service you're using doesn't fall within the typical AdTech or tracking business model. The strongest protection against corporate data collection is to encrypt or obfuscate your data whenever possible, making it difficult for different providers to correlate data with each other and build a profile on you.

## 정보 공개 제한

<span class="pg-green">:material-account-search: 공개 노출(Public Exposure)</span>

The best way to keep your data private is simply not making it public in the first place. Deleting unwanted information you find about yourself online is one of the best first steps you can take to regain your privacy.

- [View our guide on account deletion :material-arrow-right-drop-circle:](account-deletion.md)

On sites where you do share information, checking the privacy settings of your account to limit how widely that data is spread is very important. For example, enable "private mode" on your accounts if given the option: This ensures that your account isn't being indexed by search engines, and that it can't be viewed without your permission.

If you've already submitted your real information to sites which shouldn't have it, consider using disinformation tactics, like submitting fictitious information related to that online identity. This makes your real information indistinguishable from the false information.

## 검열 회피

<span class="pg-blue-gray">:material-close-outline: 검열(Censorship)</span>

Censorship online can be carried out (to varying degrees) by actors including totalitarian governments, network administrators, and service providers. These efforts to control communication and restrict access to information will always be incompatible with the human right to Freedom of Expression.[^5]

Censorship on corporate platforms is increasingly common, as platforms like Twitter and Facebook give in to public demand, market pressures, and pressures from government agencies. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://www.nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

People concerned with the threat of censorship can use technologies like [Tor](../advanced/tor-overview.md) to circumvent it, and support censorship-resistant communication platforms like [Matrix](../real-time-communication.md#element), which doesn't have a centralized account authority that can close accounts arbitrarily.

!!! tip "도움말"

    While evading censorship itself can be easy, hiding the fact that you are doing it can be very problematic.
    
    You should consider which aspects of the network your adversary can observe, and whether you have plausible deniability for your actions. For example, using [encrypted DNS](../advanced/dns-overview.md#what-is-encrypted-dns) can help you bypass rudimentary, DNS-based censorship systems, but it can't truly hide what you are visiting from your ISP. A VPN or Tor can help hide what you are visiting from network administrators, but can't hide that you're using those networks in the first place. Pluggable transports (such as Obfs4proxy, Meek, or Shadowsocks) can help you evade firewalls that block common VPN protocols or Tor, but your circumvention attempts can still be detected by methods like probing or [deep packet inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection).

You must always consider the risks of trying to bypass censorship, the potential consequences, and how sophisticated your adversary may be. You should be cautious with your software selection, and have a backup plan in case you are caught.

[^1]: Wikipedia: [*Mass Surveillance*](https://en.wikipedia.org/wiki/Mass_surveillance) and [*Surveillance*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: 미국 프라이버시 및 시민 자유 감독 위원회: [*215조항에 따라 수행된 전화 통화 기록 프로그램에 대한 보고서*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://www.ranum.com/security/computer_security/editorials/dumb/)" (or, "listing all the bad things that we know about"), as many adblockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. You should also employ other mitigation techniques.
[^5]: UN: [*세계 인권 선언*](https://www.un.org/en/about-us/universal-declaration-of-human-rights)
