---
title: "Tor 개요"
icon: 'simple/torproject'
description: Tor는 무료로 이용 가능한 탈중앙화 네트워크입니다. 최대한 프라이버시를 보호하면서 인터넷을 이용할 수 있도록 설계되었습니다.
---

Tor는 무료로 이용 가능한 탈중앙화 네트워크입니다. 최대한 프라이버시를 보호하면서 인터넷을 이용할 수 있도록 설계되었습니다. Tor 네트워크를 올바르게 사용하면 비공개 및 익명 웹 탐색과 커뮤니케이션이 가능합니다.

## Clearnet 서비스 경로 구축 방식

클리어넷(Clearnet) 서비스란, 모든 브라우저로 접근 가능한 웹사이트(예시: [privacyguides.org](https://www.privacyguides.org))를 말합니다. 클리어넷 서비스의 동의어로 '표면 웹(Surface Web)'이 쓰이기도 합니다. Tor는 '노드'(혹은 '릴레이')라고 하는 자원 봉사 운영 서버 수천 개로 구성된 네트워크를 통해 트래픽을 라우팅하여, 웹사이트를 익명으로 연결할 수 있도록 합니다.

여러분이 [Tor에 연결할](../tor.md) 때마다 3개의 노드가 선택되어 인터넷 연결 경로를 구축합니다. 이 경로를 '우회로(Circuit)'라고 합니다.

<figure markdown>
  ![여러분의 기기가 목적지 웹사이트에 도달하기까지 거쳐가는 입구 노드, 중간 노드, 출구 노드를 나타내는 Tor 경로](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![여러분의 기기가 목적지 웹사이트에 도달하기까지 거쳐가는 입구 노드, 중간 노드, 출구 노드를 나타내는 Tor 경로](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Tor 우회 경로</figcaption>
</figure>

노드는 각각 다른 역할을 가지고 있습니다.

### 입구 노드

입구 노드(Entry Node)는 Tor 클라이언트가 연결되는 첫 번째 노드입니다. 진입 노드/가드 노드(Guard Node)라고 불리기도 합니다. 입구 노드는 사용자의 IP 주소를 볼 수 있으나, 사용자가 어디에 연결하는지는 알 수 없습니다.

다른 노드와 달리, Tor 클라이언트는 여러분을 특정 공격으로부터 보호하기 위해 무작위로 입구 노드를 선택하여 2~3개월간 해당 노드를 유지합니다.

### 중간 노드

중간 노드(Middle Node)는 Tor 클라이언트가 연결되는 두 번째 노드입니다. 중간 노드는 트래픽이 어디서 왔는지, 즉 어떤 입구 노드에서 왔는지, 그리고 다음으로는 어떤 노드로 가는지 알 수 있습니다. 중간 노드는 사용자의 IP 주소 혹은 사용자가 연결하고자 하는 도메인은 알 수 없습니다.

중간 노드는 우회로를 새로 생성할 때마다 사용 가능한 모든 Tor 노드 중에서 무작위로 선택됩니다.

### 출구 노드

출구 노드(Exit Node)는 웹 트래픽이 Tor 네트워크를 벗어나, 사용자가 원하는 목적지로 전달되는 지점입니다. 출구 노드는 사용자의 IP 주소를 볼 수 없으나, 어떤 사이트에 연결하고 있는지는 알 수 있습니다.

출구 노드는 출구 릴레이 플래그로 실행된 모든 사용 가능한 Tor 노드 중에서 무작위로 선택됩니다.

## Onion 서비스 경로 구축 방식

'Onion 서비스'('Hidden 서비스'라고도 불립니다)는 Tor 브라우저로만 접근 가능한 웹사이트입니다. Onion 서비스 도메인은 랜덤으로 생성된 긴 문자열로 되어있으며, `.onion`으로 끝납니다.

Tor에서 Onion 서비스로의 연결은 클리어넷 서비스 연결과 매우 유사하게 작동하지만, 트래픽은 목적지 서버에 도달하기 전에 총 **6개**의 노드를 거쳐 라우팅됩니다. 단, 앞선 내용과 마찬가지로 *사용자의 익명성*에 기여하는 노드는 이 중 3개 뿐이며, 나머지 노드 3개는 *Onion 서비스의 익명성*을 보호합니다. 즉, Tor 브라우저가 사용자의 IP와 주소를 숨기는 것과 동일한 방식으로 웹사이트의 실제 IP와 주소를 숨깁니다.

<figure style="width:100%" markdown>
  ![3개의 Tor 노드에 더해 웹사이트 신원을 숨기는 3개의 Tor 노드를 추가로 거쳐가는 트래픽을 나타내는 Tor 경로](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![3개의 Tor 노드에 더해 웹사이트 신원을 숨기는 3개의 Tor 노드를 추가로 거쳐가는 트래픽을 나타내는 Tor 경로](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Onion 서비스 Tor 우회 경로 <span class="pg-blue">파란색</span> 테두리 내 노드는 사용자 브라우저에 해당하며, <span class="pg-red">빨간색</span> 테두리 내 노드는 서버에 해당합니다. 이리하여 서버의 신원은 노출되지 않습니다.</figcaption>
</figure>

## 암호화

Tor는 각 패킷(전송되는 데이터 덩어리)을 출구, 중간, 입구 노드 순서대로 키를 3 번 암호화합니다.

Tor 우회로가 구축되고 나면 데이터 전송은 다음과 같이 이루어집니다:

1. 먼저, 패킷이 입구 노드에 도착하면 첫 번째 암호화 레이어가 제거됩니다. 입구 노드는 해당 암호화 패킷에서 중간 노드 주소가 포함된 또 다른 암호화 패킷을 찾습니다. 이후, 입구 노드는 중간 노드로 패킷을 전송합니다.

2. 다음으로, 중간 노드가 입구 노드로부터 패킷을 수신하면 마찬가지로 키를 이용해 암호화 레이어를 제거합니다. 이번에는 출구 노드 주소가 포함된 암호화 패킷을 찾습니다. 이후, 중간 노드는 출구 노드로 패킷을 전송합니다.

3. 마지막으로, 출구 노드가 패킷을 수신하면 해당 키로 마지막 암호화 레이어를 제거합니다. 출구 노드는 목적지 주소를 확인하고 해당 주소로 패킷을 전송합니다.

다음은 이 과정을 다이어그램으로 나타낸 것입니다. 각 노드는 해당 노드의 암호화 레이어를 제거하며, 목적지 서버가 데이터를 반환할 경우 이와 동일한 과정이 정반대로 진행됩니다. 예를 들어, 출구 노드는 사용자가 누구인지는 알 수 없으나 어떤 노드에서 전송해왔는지는 알고 있으므로 자체 암호화 레이어를 추가하여 전송합니다.

<figure markdown>
  ![Tor 암호화](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor 암호화](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Tor 네트워크를 통한 데이터 송수신</figcaption>
</figure>

Tor를 이용하면 단일 주체에게 전체 경로를 노출하지 않고도 서버에 연결 가능합니다. 입구 노드는 사용자가 누구인지는 알지만 목적지는 알 수 없고, 중간 노드는 사용자와 목적지 모두 알 수 없으며, 출구 노드는 목적지는 알지만 사용자가 누구인지는 알 수 없습니다. 최종 연결이 생성되는 지점은 출구 노드이므로, 목적지 서버는 사용자의 IP 주소를 절대 알 수 없습니다.

## 주의 사항

Tor는 강력한 프라이버시를 보장하지만, 완벽하지는 않습니다:

- 전 세계 대부분의 네트워크 트래픽을 수동적으로 감시하는 능력과 자금을 갖춘 공격자는 고급 트래픽 분석을 통해 Tor 사용자의 익명성을 무효화할 수 있습니다. 또한, Tor는 사용자가 자신의 실수로 신원 정보를 노출하는 것으로부터 보호하지는 못합니다.
- Tor 출구 노드가 직접 트래픽을 모니터링하고 있을 수도 있습니다. 즉, 일반 HTTP 트래픽 등 암호화되지 않은 트래픽은 기록, 모니터링될 수 있습니다. 암호화되지 않은 트래픽에 개인 식별 정보가 포함된 경우 해당 출구 노드로 사용자의 익명성을 무효화할 수 있습니다. 따라서, Tor에서 HTTPS를 사용할 것을 권장합니다.

웹 탐색 용도로 Tor를 이용하고자 하실 경우, 핑거프린팅을 방지하도록 설계된 **공식** Tor 브라우저만 사용하실 것을 권장드립니다.

- [Tor 브라우저 :material-arrow-right-drop-circle:](../tor.md#tor-browser)

## 추가 자료

- [Tor 브라우저 사용자 설명서](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: 우회로의 첫 번째 릴레이는 'Entry Guard' 혹은 'Guard'라고 합니다. 알려진 익명성 침해 공격으로부터 보호하기 위해, 우회로에서 첫 번째 릴레이로 2~3개월간 유지되는 빠르고 안정적인 릴레이입니다. 우회로의 나머지 경로는 새로운 웹사이트를 방문할 때마다 변경되며, 이러한 릴레이가 모두 모여 Tor의 완벽한 프라이버시 보호를 제공합니다. 보다 자세한 가드 릴레이 작동 방식 설명은 [이 블로그 포스트](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters)와 [이 논문](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf)을 참고해 주세요. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2/))

[^2]: '릴레이 플래그'란 우회로 위치(Guard, Exit, BadExit 등), 우회로 속성(Fast, Stable 등), 역할(Authority, HSDir 등) 같은 릴레이의 특수 자격을 말합니다. 이는 Directory Authority에 의해 할당되며, Directory Protocol 사양에 추가로 정의되어 있습니다. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
