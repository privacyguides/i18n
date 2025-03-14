---
title: "통신 네트워크 유형"
icon: 'material/transit-connection-variant'
description: 메신저 애플리케이션에서 보편적으로 사용되는 몇 가지 네트워크 구조에 대한 개요입니다.
---

사람들 간에 메시지를 전달할 때 일반적으로 쓰이는 네트워크의 구조는 여러 유형이 있습니다. 네트워크 유형마다 프라이버시 면에서 각각 다른 장단점이 존재하므로, 어떤 유형의 애플리케이션을 사용할지는 여러분의 [위협 모델](../basics/threat-modeling.md)을 고려하여 결정하는 것이 좋습니다.

[Recommended Instant Messengers](../real-time-communication.md ""){.md-button} [:material-movie-open-play-outline: Video: It's time to stop using SMS](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why/ ""){.md-button}

## 중앙 집중형 네트워크

![중앙 집중형 네트워크 다이어그램](../assets/img/layout/network-centralized.svg){ align=left }

중앙 집중형(Centralized) 메신저는 모든 참가자가 하나의 서버 혹은 하나의 단체가 관리하는 서버 네트워크를 이용합니다.

일부 자체 호스팅 지원 메신저에서는 직접 서버를 설정할 수 있는 경우도 있습니다. 자체 호스팅을 하는 경우에는 메타데이터(누가 누구와 대화하는지에 대한 데이터) 접근 제한이나 사용 기록을 저장하지 않는 등 추가적인 프라이버시 이점을 얻는 것이 가능하다는 장점이 있습니다. 자체 호스팅 중앙 집중형 메신저는 고립되어 있으며, 모든 사람은 서로 통신하려면 동일한 서버에 있어야 합니다.

**장점:**

- 새로운 기능이나 수정 사항이 더 빠르게 구현될 수 있습니다.
- 사용하기 쉽고 연락처를 찾기도 쉽습니다.
- 중앙 집중형 소프트웨어는 프로그래밍하기 더 쉽기 때문에, 가장 성숙하고 안정적인 기능 생태계를 갖추고 있습니다.
- 신뢰할 수 있는 자체 호스팅 서버가 있다면, 프라이버시 문제는 완화할 수 있습니다.

**단점:**

- [접근이나 제어가 제한적](https://drewdevault.com/2018/08/08/Signal.html)일 수 있습니다. 예시는 다음과 같습니다:
- 더 자유로운 커스텀이나 더 나은 사용 경험을 제공 가능한 제3자 클라이언트를 중앙 집중형 네트워크에 연결하는 것이 [금지됩니다](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165). 이는 이용 약관에 정의되어 있는 경우가 많습니다.
- 외부 개발자를 위한 문서가 부실하거나 아예 없습니다.
- The [ownership](https://web.archive.org/web/20210729191953/https://blog.privacytools.io/delisting-wire), privacy policy, and operations of the service can change easily when a single entity controls it, potentially compromising the service later on.
- 자체 호스팅을 하기 위해서는 서비스 구축에 대한 노력과 지식이 필요합니다.

## 연합형 네트워크

![연합형 네트워크 다이어그램](../assets/img/layout/network-decentralized.svg){ align=left }

연합형(Federated) 메신저는 서로 간에 대화할 수 있는 여러 개의 독립적이고 분산된 서버를 이용합니다(이메일이 연합형 메신저의 대표적인 예시입니다). 연합 방식에서는 어떤 시스템 관리자가 자신의 서버를 통제하면서도 더 큰 통신 네트워크의 일부가 되는 것이 가능합니다.

자체 호스팅하는 경우, 해당 연합형 서버의 구성원은 다른 서버의 구성원을 찾아내고 통신할 수 있습니다. 단, 서버 연합 네트워크에 참여하지 않고 비공개로 유지하는 것도 가능합니다(업무용 서버 등이 대표적입니다).

**장점:**

- 자체 서버를 운영하는 경우 자신의 데이터에 대한 통제력이 향상됩니다.
- 여러 '공개' 서버 중 원하는 서버를 고르는 것으로 데이터 신뢰 대상을 취사선택 가능합니다.
- 네이티브, 커스텀, 사용 경험 면에서 더 뛰어난 제3자 클라이언트를 사용할 수 있도록 허용하는 경우가 많습니다.
- Server software can be verified that it matches public source code, assuming you have access to the server, or you trust the person who does (e.g., a family member).

**단점:**

- 어떤 새로운 기능이 추가되려면 해당 기능이 네트워크상의 모든 서버에서 작동해야 합니다. 즉, 기능의 표준화와 테스트를 거쳐야 하므로 새로운 기능의 추가는 쉽지 않습니다.
- 앞선 이유와 마찬가지로, 메시지 삭제나 오프라인 상태에서의 메시지 전달 등의 기능이 중앙 집중형 플랫폼에 비해 부족하거나, 불완전하거나, 예상치 못한 방식으로 작동할 수 있습니다.
- 일부 메타데이터가 유출될 가능성이 존재합니다(E2EE가 적용될 경우 실제 메시지 내용은 알 수 없지만, '누가 누구랑 대화하고 있는지'는 알 수 있습니다).
- 연합형 서버를 사용하려면 일반적으로 해당 서버의 관리자를 신뢰해야 합니다. 하지만 서버 관리자가 '보안 전문가'일 것이란 보장은 없습니다. 단순히 취미로 운영할 수도 있으며, 사용자 데이터 처리 방침/서비스 약관/프라이버시 정책 등의 표준 문서를 제공하지 않을 수 있습니다.
- 중재되지 않는 어뷰징이 일어나거나 일반적인 규칙을 위반하는 다른 서버를 여러분의 서버 관리자가 차단하기도 합니다. 이 경우 해당 서버의 구성원과는 소통하기 어려워집니다.

## P2P 네트워크

![P2P 다이어그램](../assets/img/layout/network-distributed.svg){ align=left }

P2P 메신저는 [분산형(Distributed) 네트워크](https://en.wikipedia.org/wiki/Distributed_networking)에 노드로서 연결되어 제3자 서버 없이 수신자에게 메시지를 전달합니다.

클라이언트(피어)는 일반적으로 [분산 컴퓨팅](https://en.wikipedia.org/wiki/Distributed_computing) 네트워크를 이용해 서로를 찾아냅니다. 예시로는 [토렌트](https://ko.wikipedia.org/wiki/%EB%B9%84%ED%8A%B8%ED%86%A0%EB%A0%8C%ED%8A%B8), [IPFS](https://ko.wikipedia.org/wiki/InterPlanetary_File_System)에서 사용하는 [분산 해시 테이블](https://ko.wikipedia.org/wiki/%EB%B6%84%EC%82%B0_%ED%95%B4%EC%8B%9C_%ED%85%8C%EC%9D%B4%EB%B8%94)(DHT)이 있습니다. Another approach is proximity based networks, where a connection is established over Wi-Fi or Bluetooth (for example, Briar or the [Scuttlebutt](https://scuttlebutt.nz) social network protocol).

피어가 이러한 방법을 통해 연락 상대로 연결되는 경로를 찾아내면 서로 직접 연결이 이루어집니다. 메시지에는 일반적으로 암호화가 적용되나, 관찰자는 발신자/수신자의 위치와 신원을 유추할 수 있습니다.

P2P 네트워크는 피어가 서로 직접 통신하므로 서버를 사용하지 않고, 따라서 자체 호스팅은 불가능합니다. 하지만 사용자 검색, 오프라인 메시지 전달 등 일부 추가 서비스는 중앙 집중형 서버에 의존하는 경우도 있으며, 이러한 서비스는 자체 호스팅의 이점이 존재합니다.

**장점:**

- 제3자에게 노출되는 정보를 최소화합니다.
- 최신 P2P 플랫폼은 E2EE를 기본적으로 구현하고 있습니다. 중앙 집중형/연합형 모델과 달리, 잠재적으로 사용자의 통신을 가로채고 해독할 여지가 있는 서버가 아예 존재하지 않습니다.

**단점:**

- 일반적으로 기능이 부족합니다.
- 메시지를 주고받으려면 대화 발신자/수신자가 모두 온라인 상태여야 합니다. 단, 이 문제는 클라이언트에 따라 상대방이 온라인 상태가 될 때까지 메시지를 로컬에 저장한 채로 기다렸다가 전송하는 등의 방식을 이용해 어느 정도 완화하기도 합니다.
- 일반적으로 모바일 기기의 배터리 소모량이 높아집니다. 상대가 온라인 상태인지를 파악하기 위해서 클라이언트가 분산형 네트워크에 계속 연결되어 있어야 하기 때문입니다.
- 메시지 삭제 등의 일반적인 메신저 기능이 구현되어 있지 않거나, 구현이 불완전할 수 있습니다.
- [VPN](../vpn.md)이나 [Tor](../tor.md) 등의 소프트웨어와 함께 사용하지 않을 경우, 자신이나 대화 상대의 IP 주소가 노출될 수 있습니다. 많은 국가에서는 어떤 형태로든 대규모 감시 혹은 메타데이터 수집을 진행하고 있습니다.

## 익명 라우팅

![익명 라우팅 다이어그램](../assets/img/layout/network-anonymous-routing.svg){ align=left }

[익명 라우팅](https://doi.org/10.1007/978-1-4419-5906-5_628)을 사용하는 메신저는 발신자, 수신자의 신원 혹은 통신 흔적을 드러내지 않습니다. 이상적으로는, 메신저는 이 세 가지(발신자 신원, 수신자 신원, 통신 흔적) 모두를 숨길 수 있어야 합니다.

There are [many](https://doi.org/10.1145/3182658) ways to implement anonymous routing. 대표적인 방법으로는 [Onion 라우팅](https://en.wikipedia.org/wiki/Onion_routing)([Tor](tor-overview.md))이 존재합니다. 각 메시지의 발신자나 수신자뿐만 아니라 각 노드의 위치를 숨기는 가상 [오버레이 네트워크](https://en.wikipedia.org/wiki/Overlay_network)를 통해 암호화 메시지를 주고받습니다. 발신자와 수신자는 직접적으로 상호작용하지 않고 비밀 랑데부 노드를 통해서만 만나기 때문에 IP 주소나 실제 위치는 노출되지 않습니다. 노드는 메시지를 복호화하거나 최종 목적지를 알 수 없으며, 수신자만이 해독 가능합니다. 각 중개 노드는 메시지를 다음에는 어디로 보낼지를 나타내는 부분만 해독 가능하며 그 외에는 여전히 암호화가 적용되어 있습니다. 그리고 이 과정은 수신자에게 도달해 완전히 복호화될 때까지 반복됩니다. 'Onion(양파) 레이어'라는 명칭은 이러한 작동 방식에서 유래되었습니다.

Self-hosting a node in an anonymous routing network does not provide the host with additional privacy benefits, but rather contributes to the whole network's resilience against identification attacks for everyone's benefit.

**장점:**

- 제3자에게 노출되는 정보를 최소화합니다.
- 당사자 중 한명이 오프라인 상태이더라도 분산형 방식으로 메시지를 전달할 수 있습니다.

**단점:**

- 메시지 전달 속도가 느립니다.
- 네트워크의 느린 속도로 인해 전송 가능한 미디어 유형이 제한됩니다. 실질적으로 텍스트만 가능합니다.
- 무작위 라우팅으로 노드를 선정하는 경우, 일부 노드는 발신자와 수신자로부터 매우 멀리 떨어져 있을 수 있습니다. 이 경우 지연 시간이 길어지거나 노드 중 하나가 오프라인 상태가 되면 메시지 전송에 실패할 수도 있습니다.
- 암호화 개인 키를 생성하고 안전하게 백업하는 방법을 알아야 하므로, 사용 난이도가 높은 편입니다.
- 여타 분산형 플랫폼과 마찬가지로 중앙 집중형 플랫폼에 비해 새로운 기능이 추가되는 과정이 복잡합니다. 오프라인 메시지 전달이나 메시지 삭제 등의 기능이 부족하거나, 불완전할 수 있습니다.
