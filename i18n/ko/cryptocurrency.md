---
meta_title: "프라이버시를 보호하는 암호화폐 블록체인 - 프라이버시 가이드"
description: 대부분의 암호화폐와 달리, 다음 암호화폐는 기본적으로 거래 프라이버시를 제공합니다. 모네로는 거래 정보를 난독화하는 데 프라이버시 가이드가 가장 추천하는 선택지입니다.
title: 암호화폐
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-eye-outline: 대규모 감시](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: 검열](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

온라인 결제는 프라이버시에 있어 가장 큰 난제 중 하나입니다. 다음 암호화폐는 기본적으로 거래 프라이버시를 제공합니다(대부분의 암호화폐는 이를 보장하지 **않습니다**). 단, 프라이버시를 지키며 효과적으로 결제하는 방법을 충분히 이해하고 있어야 합니다. 무언가를 구매하기 전에 먼저 결제 개요 글을 읽어 볼 것을 강력히 권장합니다:

[프라이버시를 지키며 결제하기 :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">위험</p>

전부는 아니더라도 대부분의 암호화폐 프로젝트는 사기입니다. 신뢰할 수 있는 프로젝트하고만 신중하게 거래하세요.

</div>

## 모네로 { #monero }

<div class="admonition recommendation" markdown>

![모네로 로고](assets/img/cryptocurrency/monero.svg){ align=right }

**모네로**는 거래를 난독화하는 프라이버시 강화 기술이 적용된 블록체인을 사용하여 [:material-incognito: 익명성](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }을 달성합니다. 모든 모네로 거래는 별도의 번거로운 절차 없이도 거래 금액, 송수신 주소, 자금 출처를 숨기므로, 암호화폐 초보자에게 이상적인 선택입니다.

[:octicons-home-16: 홈페이지](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title="문서"}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title="후원하기" }

</details>

</div>

모네로를 사용하면 외부 관찰자는 모네로를 거래하는 주소, 거래 금액, 주소 잔액, 거래 내역을 알아낼 수 없습니다.

<details class="info" markdown>
<summary>대규모 감시에 대한 모네로의 회복력</summary>

2021년 8월, 사이퍼트레이스는 정부 기관을 위한 향상된 모네로 추적 기능을 [발표](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing)했습니다. 공개된 게시물에 따르면 미국 재무부 산하 금융범죄단속네트워크(FinCEN)는 2022년 말 사이퍼트레이스의 "모네로 모듈"에 대한 [라이선스를 취득](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view)했습니다.

모네로의 거래 그래프 프라이버시는 상대적으로 작은 링 서명으로 인해 제한적이며, 특히 표적 공격에 취약합니다. 일부 보안 연구자들은 모네로의 프라이버시 기능에 [의문을 제기](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy)했으며, 과거에 여러 심각한 취약점이 발견되어 패치된 적도 있으므로 사이퍼트레이스 같은 조직의 주장이 전혀 불가능한 것은 아닙니다. 비트코인 등에 대해 존재하는 것과 같은 모네로 대규모 감시 도구가 존재할 가능성은 낮지만, 추적 도구가 표적 수사에 도움이 되는 것은 확실합니다.

결론적으로 모네로는 프라이버시 친화적인 암호화폐 중 가장 유력한 후보이지만, 그 프라이버시 주장은 어느 쪽으로도 확실하게 입증된 바 **없습니다**. 모네로가 항상 적절한 프라이버시를 제공할 만큼 공격에 충분히 강한지 평가하려면 더 많은 시간과 연구가 필요합니다.

</details>

### 모네로 지갑 { #monero-wallets }

최적의 프라이버시를 위해 [뷰 키](https://getmonero.org/resources/moneropedia/viewkey.html)가 기기에 그대로 남아 있는 자체 보관형 지갑을 사용하세요. 이렇게 하면 여러분만 자금을 사용하고 입출금 거래를 볼 수 있습니다. 수탁형 지갑을 사용하면 제공업체가 여러분이 하는 **모든 것**을 볼 수 있으며, 제공업체가 뷰 키를 보관하는 "경량" 지갑을 사용하면 제공업체가 여러분이 하는 거의 모든 것을 볼 수 있습니다(자금을 사용할 수는 없지만). 뷰 키가 기기 밖으로 나가지 않는 자체 보관형 지갑으로는 다음이 있습니다:

- [공식 모네로 클라이언트](https://getmonero.org/downloads)(데스크톱)
- [케이크 월렛](https://cakewallet.com)(iOS, 안드로이드, 데스크톱)
    - 케이크 월렛은 여러 암호화폐를 지원합니다. 모네로 전용 iOS 및 안드로이드용 케이크 월렛은 [Monero.com](https://monero.com)에서 받을 수 있습니다.
- [페더 월렛](https://featherwallet.org)(데스크톱)
- [모네루조](https://monerujo.io)(안드로이드)

### 모네로 노드 { #monero-nodes }

(자체 보관형 지갑을 사용하더라도) 최대한의 프라이버시를 원한다면 [CLI 지갑](https://getmonero.org/downloads/#cli)에 포함된 [모네로 데몬](https://docs.getmonero.org/interacting/monerod-reference)이라는 자신만의 모네로 노드를 운영해야 합니다. 다른 사람의 노드를 사용하면 연결하는 IP 주소, 지갑을 동기화하는 시각, 지갑에서 보내는 거래(해당 거래의 다른 세부 정보는 제외) 같은 일부 정보가 노드 운영자에게 노출됩니다. 또는 [토르](alternative-networks.md#tor), [I2P](alternative-networks.md#i2p-the-invisible-internet-project), [VPN](vpn.md)을 통해 다른 사람의 모네로 노드에 연결할 수도 있습니다.

### 모네로 구매하기 { #buying-monero }

[모네로를 얻기 위한 일반적인 팁](advanced/payments.md#acquisition ""){.md-button}

모네로를 사고팔 수 있는 중앙화 거래소(CEX)와 P2P 마켓플레이스는 많이 있습니다. 그중 일부는 자금 세탁 방지 규정을 준수하기 위해 신원 확인(KYC)을 요구합니다. 하지만 모네로의 프라이버시 기능 덕분에 판매자가 알 수 있는 것은 여러분이 모네로를 샀다는 *사실*뿐이며, (거래소를 떠난 후) 얼마를 보유하고 있는지나 어디에 사용하는지는 알 수 없습니다. 모네로를 구매할 수 있는 신뢰할 만한 곳으로는 다음이 있습니다:

- [크라켄](https://kraken.com): 잘 알려진 중앙화 거래소입니다. 가입과 KYC가 필수입니다. 카드 결제와 계좌 이체를 지원합니다. 구매한 모네로를 크라켄 플랫폼에 그대로 두지 말고, 구매 후 자체 보관형 지갑으로 출금하세요. 크라켄이 운영되는 모든 관할 지역에서 모네로를 구매할 수 있는 것은 아닙니다.[^1]
- [케이크 월렛](https://cakewallet.com): 모네로와 기타 암호화폐를 위한 자체 보관형 크로스 플랫폼 지갑입니다. ([가디어리언](https://guardarian.com)이나 [DFX](https://dfx.swiss) 같은 서드파티 제공업체를 통해) 카드 결제나 계좌 이체로 앱에서 바로 모네로를 구매할 수 있습니다.[^2] KYC는 대개 필요하지 않지만, 국가와 구매 금액에 따라 달라집니다. 모네로를 직접 구매할 수 없는 국가에서는 케이크 월렛 안의 제공업체를 통해 먼저 비트코인, 비트코인 캐시, 라이트코인 같은 다른 암호화폐를 구매한 다음, 앱 안에서 모네로로 교환할 수도 있습니다.
    - [Monero.com](https://monero.com)은 앱을 다운로드하지 않고도 모네로와 기타 암호화폐를 구매할 수 있는 관련 웹사이트입니다. 자금은 여러분이 선택한 지갑 주소로 바로 전송됩니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

- 암호화폐는 기본적으로 비공개/추적 불가능한 거래를 제공해야 합니다.

<div class="admonition tip" markdown>
<p class="admonition-title">중요 고지 사항</p>

이 내용은 법률 또는 금융 자문이 아닙니다. 프라이버시 가이드는 불법 행위를 지지하거나 장려하지 않으며, 기업의 서비스 이용 약관을 위반하는 어떠한 행위도 지지하거나 장려하지 않습니다. 이러한 추천이 여러분의 관할 지역에서 합법적이고 이용 가능한지 전문가에게 확인하세요. [모든 고지 사항 보기](about/notices.md).

</div>

[^1]: 크라켄이 모네로 구매를 허용하지 **않는** 국가에 대한 최신 정보는 다음 페이지를 참고하세요: [Where is Kraken licensed or regulated?](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) 및 [Support for Monero (XMR) in Europe](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe).
[^2]: 케이크 월렛과 Monero.com이 (서드파티 제공업체를 통한) 모네로 직접 구매**만** 허용하는 국가에 대한 최신 정보는 다음 페이지를 참고하세요: [Which countries are served by DFX?](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) 및 [What are the supported countries/regions? (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
