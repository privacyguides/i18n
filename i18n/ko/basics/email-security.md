---
meta_title: "이메일이 프라이버시, 보안 면에서 최선의 선택이 아닌 이유 - Privacy Guides"
title: 이메일 보안
icon: material/email
description: 이메일은 태생적으로 여러 가지 면에서 안전하지 않습니다. 따라서 안전한 통신을 위한 최선의 선택은 아닙니다.
---

기본적으로, 이메일은 안전하지 않은 통신 형식입니다. OpenPGP(메시지에 종단 간 암호화 적용) 등을 이용해 이메일 보안을 개선할 수는 있지만, OpenPGP 또한 다른 메신저 애플리케이션의 암호화에 비교하면 여러 문제점이 있으며, 이메일 시스템 설계상 암호화가 불가능한 일부 이메일 데이터도 존재합니다.

따라서, 이메일은 다른 사람과 통신하는 용도로는 사용하지 않고, 가입한 온라인 서비스에서 보내는 사무 관련 이메일(알림, 인증 메일, 비밀번호 초기화 등) 수신 용도로 사용하는 것이 가장 좋습니다.

## 이메일 암호화 개요

서로 다른 이메일 제공 업체 간의 이메일에 E2EE를 적용하는 표준 방법은 OpenPGP를 사용하는 것입니다. OpenPGP 표준에는 여러 구현체가 존재하며, [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard)와 [OpenPGP.js](https://openpgpjs.org)가 보편적입니다.

비즈니스에서 널리 사용되는 [S/MIME](https://en.wikipedia.org/wiki/S/MIME) 표준도 있으나, S/MIME는 [인증 기관](https://en.wikipedia.org/wiki/Certificate_authority)(모든 인증 기관이 S/MIME 인증서를 발급하지는 않습니다)에서 발급한 인증서가 필요합니다. S/MIME는 [Google Workplace](https://support.google.com/a/topic/9061730?hl=en&ref_topic=9061731), [웹용 Outlook 또는 Exchange Server 2016, 2019](https://support.office.com/en-us/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480)에서 지원됩니다.

OpenPGP를 사용하더라도 [순방향 비밀성(Forward secrecy)](https://en.wikipedia.org/wiki/Forward_secrecy)을 지원하지 않으므로, 본인 혹은 수신자의 개인 키가 도난당할 경우 해당 키로 암호화된 이전 메시지가 전부 노출됩니다. 따라서, 개인 간 의사소통에는 이메일보다는 순방향 비밀성이 구현된 [메신저](../real-time-communication.md)를 이용하실 것을 권장드립니다.

### E2EE 지원 이메일 클라이언트는 무엇인가요?

IMAP, SMTP 등 표준 접속 프로토콜을 사용할 수 있는 이메일 제공 업체는 [권장 이메일 클라이언트](../email-clients.md)와 함께 사용할 수 있습니다. 인증 방법에 따라서, 이메일 제공 업체/클라이언트가 OATH를 지원하지 않거나 브리지 애플리케이션을 지원하지 않는 경우, 단순 비밀번호 인증으로는 [다중 인증](multi-factor-authentication.md)이 불가능하므로 보안이 저하될 수 있습니다.

### 개인 키를 어떻게 보호해야 하나요?

스마트카드([YubiKey](https://support.yubico.com/hc/en-us/articles/360013790259-Using-Your-YubiKey-with-OpenPGP), [Nitrokey](https://www.nitrokey.com) 등)는 기기(스마트폰, 태블릿, PC 등)에서 실행하는 이메일/웹메일 클라이언트가 암호화된 메일을 수신했을 때 작동합니다. 암호화된 메일 내용은 스마트카드에서 복호화되며, 복호화된 내용이 스마트카드로부터 기기로 전달됩니다.

스마트카드에서 복호화를 수행함으로써, 기기의 보안이 손상됐을 경우에도 개인 키가 노출되는 것을 방지할 수 있습니다.

## 이메일 메타데이터 개요

이메일 메타데이터는 이메일 메시지의 [메시지 헤더](https://en.wikipedia.org/wiki/Email#Message_header)에 저장됩니다. 이메일 메타데이터에는 여러분이 봐왔을 `To`(받는사람), `From`(보낸사람), `Cc`(참조), `Date`(보낸 날짜), `Subject`(제목) 등이 포함됩니다. 이외에도 여러 숨겨진 헤더가 이메일 클라이언트 및 제공 업체로부터 추가되며, 이러한 정보는 여러분의 계정에 대한 정보를 노출시킬 수 있습니다.

클라이언트 소프트웨어는 이메일 메타데이터를 사용해 메시지의 발신자와 수신 시간을 표시할 수 있습니다. 서버는 항상 투명하지만은 않은 [다른 목적지](https://en.wikipedia.org/wiki/Email#Message_header) 중 어디에 이메일을 보내야 할지 결정하는 데에 메타데이터를 활용할 수 있습니다.

### 이메일 메타데이터는 누가 볼 수 있나요?

이메일 메타데이터는 [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS)를 통해 외부 관찰자로부터 보호됩니다. 하지만 여러분이 사용하는 이메일 클라이언트 소프트웨어나 웹메일은 메타데이터를 볼 수 있습니다. 또한 여러분의 이메일 제공 업체를 포함한, 여러분과 상대 수신자 사이의 모든 메시지 전달 서버 역시 메타데이터를 볼 수 있습니다. 이메일 서버 중에는 스팸 차단 목적으로 타사 서비스를 사용하기도 하는데, 보통 이런 타사 서비스도 여러분의 메시지에 접근할 수 있습니다.

### 메타데이터는 종단 간 암호화를 적용할 수 없나요?

이메일 메타데이터는 이메일의 가장 기본적인 기능(어디에서 왔는지, 어디로 가야하는지 등)에 매우 중요한 역할을 합니다. 이메일 프로토콜에는 본래 E2EE가 내장되지 않았기 때문에, OpenPGP 등의 애드온 소프트웨어가 필요합니다. 그러나 OpenPGP 메시지는 여전히 기존 이메일 제공 업체와도 작동해야 합니다. 따라서 메시지 본문은 암호화할 수 있으나, 메타데이터는 암호화할 수 없습니다. 따라서, OpenPGP를 사용하더라도 외부 관찰자는 이메일 수신자, 제목, 이메일 작성 시간 등 여러 정보를 볼 수 있습니다.
