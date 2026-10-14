---
meta_title: "이메일이 프라이버시, 보안 면에서 최선의 선택이 아닌 이유 - 프라이버시 가이드"
title: 이메일 보안
icon: material/email
description: 이메일은 기술적으로 원래 여러 가지 면에서 안전하지 않습니다. 따라서 강한 프라이버시를 위한 좋은 옵션은 아닙니다.
---

기본적으로, 이메일은 안전하지 않은 통신 형식입니다. OpenPGP(메시지에 종단 간 암호화 적용) 등을 이용해 이메일 보안을 개선할 수는 있지만, OpenPGP 또한 다른 메신저 애플리케이션의 암호화에 비교하면 많은 문제점이 있으며, 이메일 시스템 설계상 기술적으로 암호화가 불가능한 일부 이메일 데이터도 존재합니다.

따라서, 이메일은 다른 사람과 통신하는 용도로는 사용하지 않고, 가입한 온라인 서비스에서 보내는 사무 관련 이메일(알림, 인증 메일, 비밀번호 초기화 등) 수신 용도로 사용하는 것이 가장 좋습니다.

## 이메일 암호화 개요

서로 다른 이메일 제공 업체 간의 이메일에 E2EE를 적용하는 표준 방법은 OpenPGP를 사용하는 것입니다. OpenPGP 표준에는 여러 구현체가 존재하며, [GnuPG](../encryption.md#gnu-privacy-guard)와 [OpenPGP.js](https://openpgpjs.org)가 가장 널리 쓰이고 있습니다.

OpenPGP를 사용하더라도 [순방향 비밀성(Forward secrecy)](https://en.wikipedia.org/wiki/Forward_secrecy)을 지원하지 않으므로, 본인 혹은 수신자의 개인 키가 도난당할 경우 해당 키로 암호화된 이전 메시지가 전부 노출됩니다. 따라서, 개인 간 의사소통에는 이메일보다는 순방향 비밀성이 구현된 [메신저](../real-time-communication.md)를 이용하실 것을 권장드립니다.

비즈니스에서 널리 사용되는 [S/MIME](https://en.wikipedia.org/wiki/S/MIME) 같은 표준도 있으나, S/MIME는 [인증 기관](https://en.wikipedia.org/wiki/Certificate_authority)(모든 인증 기관이 S/MIME 인증서를 발급하진 않습니다)에서 발급한 인증서가 필요합니다. 어떤 경우에는 PGP보다 사용하기 더 편리합니다. Apple Mail, [구글 워크스페이스](https://support.google.com/a/topic/9061730), [Outlook과](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480) 같은 대중적이고 주류인 이메일 애플리케이션에서 지원되기 때문입니다.  그러나 S/MIME는 순방향 기밀성(forward secrecy)이 부족하다는 문제를 해결하지 못하며, PGP보다 특별히 더 안전하다고 할 수 없습니다.

## Web Key Directory(WKD) 표준이란 무엇인가요?

[WKD(Web Key Directory)](https://wiki.gnupg.org/WKD) 표준을 통해 이메일 클라이언트는 다른 제공업체에서 호스팅되는 메일함의 OpenPGP 키도 찾을 수 있습니다. WKD를 지원하는 이메일 클라이언트는 수신자의 서버에 이메일 주소의 도메인 이름을 기반으로 키를 요청합니다. 예를 들어, `jonah@privacyguides.org으로` 이메일을 보낸다면, 사용자의 이메일 클라이언트가 `privacyguides.org에` 조나(Jonah)의 OpenPGP 키를 요청하게 되고, `privacyguides.org에` 해당 계정의 키가 있다면 사용자의 메시지는 자동으로 암호화됩니다.

WKD를 지원하는 [당사가 추천하는 이메일 클라이언트](../email-clients.md) 외에도, 일부 웹메일 제공업체에서도 WKD를 지원합니다. *사용자 자신의* 키가 다른 사람들이 사용할 수 있도록 WKD에 게시되는지는 도메인 구성에 따라 달라집니다. Proton Mail이나 Mailbox Mail과 같이 WKD를 지원하는 [이메일 서비스를](../email.md#openpgp-compatible-services) 이용한다면, 해당 서비스에서 사용자의 OpenPGP 키를 자사 도메인에 대리 게시해 줄 수 있습니다.

개인 도메인같은 맞춤 도메인을 사용하는 경우, WKD를 별도로 설정해야 합니다. 도메인 네임을 직접 관리하고 있다면, 이메일 서비스 제공업체와 관계없이 WKD를 설정할 수 있습니다. 이를 쉽게 구현하는 방법 중 하나는`keys.openpgp.org` 서버의[“「WKD 서비스」(WKD as a Service)”](https://keys.openpgp.org/about/usage#wkd-as-a-service) 기능을 이용하는 것입니다. 도메인의 `openpgpkey` 하위 도메인이 `wkd.keys.openpgp.org를` 가리키도록 CNAME 레코드를 설정한 다음, [keys.openpgp.org에](https://keys.openpgp.org) 공개 키를 업로드하면 됩니다. 또는, [본인의 웹 서버에서 WKD를 직접 호스팅할](https://wiki.gnupg.org/WKDHosting) 수도 있습니다.

`@gmail.com과` 같이 WKD를 지원하지 않는 제공업체의 공유 도메인을 사용하는 경우, 이 방법을 통해 다른 사람과 OpenPGP 키 공유는 어렵습니다.

### E2EE 지원 이메일 클라이언트는 무엇인가요?

IMAP, SMTP 등 표준 접속 프로토콜을 사용할 수 있는 이메일 제공 업체는 [권장 이메일 클라이언트](../email-clients.md)와 함께 사용할 수 있습니다. 인증 방법에 따라서, 이메일 제공 업체/클라이언트가 OATH를 지원하지 않거나 브리지 서비스를 지원하지 않는 경우, 단순 비밀번호 인증으로는 [다중 인증](multi-factor-authentication.md)이 어려워 보안이 저하될 수 있습니다.

### 개인 키를 어떻게 보호해야 하나요?

스마트카드([YubiKey](https://support.yubico.com/hc/en-us/articles/360013790259-Using-Your-YubiKey-with-OpenPGP), [Nitrokey](https://www.nitrokey.com) 등)는 이메일/웹메일 클라이언트를 실행하는 장치(휴대폰, 태블릿, 컴퓨터 등)로부터 암호화된 이메일 메시지를 받아 동작합니다. 암호화된 메일 내용은 스마트카드에서 복호화되며, 복호화된 내용이 스마트카드로부터 기기로 전달됩니다.

스마트카드에서 복호화가 진행되므로 기기의 보안이 손상됐을 경우에도 개인 키가 노출되는 것을 방지할 수 있습니다.

## 이메일 메타데이터 개요

이메일 메타데이터는 이메일 메시지의 [메시지 헤더](https://en.wikipedia.org/wiki/Email#Message_header)에 저장됩니다. 이메일 메타데이터에는 여러분이 봐왔을 `To`(받는사람), `From`(보낸사람), `Cc`(참조), `Date`(보낸 날짜), `Subject`(제목) 등이 포함됩니다. 이외에도 여러 숨겨진 헤더가 이메일 클라이언트 및 제공 업체로부터 추가되며, 이러한 정보는 여러분의 계정에 대한 정보를 노출시킬 수 있습니다.

클라이언트 소프트웨어는 이메일 메타데이터를 사용해 메시지의 발신자와 수신 시간을 표시할 수 있습니다. 서버는 항상 투명하지만은 않은 [다른 목적지](https://en.wikipedia.org/wiki/Email#Message_header) 중 어디에 이메일을 보내야 할지 결정하는 데에 메타데이터를 활용할 수 있습니다.

### 이메일 메타데이터는 누가 볼 수 있나요?

이메일 메타데이터는 [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS)(기회적 TLS)를 통해 외부 관찰자로부터 보호되지만, 여전히 이메일 클라이언트 소프트웨어(또는 웹메일)와 발신자에서 수신자까지 메시지를 전달하는 중계 서버(이메일 제공업체 포함)가 볼 수 있습니다. 이메일 서버 중에는 스팸 차단 목적으로 타사 서비스를 사용하기도 하는데, 보통 이런 타사 서비스도 여러분의 메시지에 접근할 수 있습니다.

### 메타데이터는 종단 간 암호화를 적용할 수 없나요?

이메일 메타데이터는 이메일의 가장 기본적인 기능(어디에서 왔는지, 어디로 가야하는지 등)에 매우 중요한 역할을 합니다. E2EE(종단 간 암호화)는 원래 표준 이메일 프로토콜에 내장되어 있지 않았으며, 대신 OpenPGP와 같은 추가 소프트웨어가 필요했습니다. OpenPGP 메시지는 여전히 기존 이메일 제공업체와 호환되어야 하기 때문에, 통신 당사자를 식별하는 데 필요한 일부 이메일 메타데이터를 암호화할 수 없습니다. 즉, OpenPGP를 사용하더라도 외부 관찰자는 이메일을 주고받는 상대, 이메일을 보낸 시간 등 메시지에 관한 많은 정보를 볼 수 있습니다.
