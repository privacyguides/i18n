---
meta_title: "이메일이 프라이버시와 보안에 최선의 선택이 아닌 이유 - 프라이버시 가이드"
title: 이메일 보안
icon: material/email
description: 이메일은 여러 면에서 안전하지 않으며, 이 페이지에서는 이메일이 안전한 통신 수단으로 최선의 선택이 아닌 몇 가지 이유를 설명합니다.
---

이메일은 기본적으로 안전하지 않은 통신 수단입니다. 메시지에 종단 간 암호화를 적용하는 OpenPGP 같은 도구로 이메일 보안을 개선할 수는 있지만, OpenPGP는 다른 메신저 애플리케이션의 암호화에 비해 여전히 여러 단점이 있습니다.

따라서 이메일은 다른 사람과 소통하는 용도보다는 가입한 온라인 서비스에서 보내는 트랜잭션 이메일(알림, 인증 메일, 비밀번호 재설정 등)을 받는 용도로 사용하는 것이 가장 좋습니다.

## 이메일 암호화 개요 { #email-encryption-overview }

서로 다른 이메일 제공업체 간 이메일에 E2EE를 적용하는 표준 방법은 OpenPGP를 사용하는 것입니다. OpenPGP 표준에는 여러 구현체가 존재하며, [GnuPG](../encryption.md#gnu-privacy-guard)와 [OpenPGP.js](https://openpgpjs.org)가 가장 널리 쓰이고 있습니다.

OpenPGP를 사용하더라도 [순방향 비밀성](https://en.wikipedia.org/wiki/Forward_secrecy)은 지원되지 않습니다. 즉, 여러분이나 수신자의 개인 키가 도난당하면 그 키로 암호화된 이전 메시지가 모두 노출됩니다. 그렇기 때문에 개인 간 소통에는 가능하면 이메일보다 순방향 비밀성을 구현한 [메신저](../real-time-communication.md)를 사용할 것을 권장합니다.

기업에서 널리 사용되는 [S/MIME](https://en.wikipedia.org/wiki/S/MIME)이라는 또 다른 표준도 있지만, [인증 기관](https://en.wikipedia.org/wiki/Certificate_authority)에서 발급한 인증서가 필요합니다(모든 인증 기관이 S/MIME 인증서를 발급하는 것은 아니며, 대개 매년 비용을 지불해야 합니다). 경우에 따라서는 애플 메일, [구글 워크스페이스](https://support.google.com/a/topic/9061730), [아웃룩](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480) 같은 대중적인 이메일 애플리케이션에서 지원되기 때문에 PGP보다 사용하기 편리합니다. 하지만 S/MIME도 순방향 비밀성이 없다는 문제를 해결하지 못하며, PGP보다 특별히 더 안전한 것도 아닙니다.

## 웹 키 디렉터리 표준이란 무엇인가요? { #what-is-the-web-key-directory-standard }

[웹 키 디렉터리(WKD)](https://wiki.gnupg.org/WKD) 표준을 사용하면 이메일 클라이언트가 다른 제공업체에서 호스팅되는 메일함이라도 해당 메일함의 OpenPGP 키를 찾을 수 있습니다. WKD를 지원하는 이메일 클라이언트는 수신자의 서버에 이메일 주소의 도메인 이름을 기반으로 키를 요청합니다. 예를 들어 `jonah@privacyguides.org`로 이메일을 보내면 이메일 클라이언트는 `privacyguides.org`에 조나의 OpenPGP 키를 요청하고, `privacyguides.org`에 해당 계정의 키가 있다면 메시지가 자동으로 암호화됩니다.

WKD를 지원하는 [추천 이메일 클라이언트](../email-clients.md) 외에도 일부 웹메일 제공업체도 WKD를 지원합니다. *여러분 자신의* 키가 다른 사람이 사용할 수 있도록 WKD에 게시되는지는 도메인 구성에 따라 달라집니다. 프로톤 메일이나 메일박스 메일처럼 WKD를 지원하는 [이메일 제공업체](../email.md#openpgp-compatible-services)를 사용한다면, 해당 업체가 자사 도메인에 여러분의 OpenPGP 키를 대신 게시해 줄 수 있습니다.

자신의 사용자 지정 도메인을 사용한다면 WKD를 별도로 구성해야 합니다. 도메인 이름을 직접 관리하고 있다면 이메일 제공업체와 관계없이 WKD를 설정할 수 있습니다. 이를 쉽게 하는 방법 중 하나는 `keys.openpgp.org` 서버의 "[서비스형 WKD(WKD as a Service)](https://keys.openpgp.org/about/usage#wkd-as-a-service)" 기능을 사용하는 것입니다. 도메인의 `openpgpkey` 하위 도메인에 `wkd.keys.openpgp.org`를 가리키는 CNAME 레코드를 설정한 다음, [keys.openpgp.org](https://keys.openpgp.org)에 키를 업로드하면 됩니다. 또는, [본인의 웹 서버에서 WKD를 직접 호스팅할](https://wiki.gnupg.org/WKDHosting) 수도 있습니다.

`@gmail.com`처럼 WKD를 지원하지 않는 제공업체의 공유 도메인을 사용한다면, 이 방법으로는 다른 사람과 OpenPGP 키를 공유할 수 없습니다.

### 어떤 이메일 클라이언트가 E2EE를 지원하나요? { #what-email-clients-support-e2ee }

IMAP, SMTP 같은 표준 접속 프로토콜을 사용할 수 있는 이메일 제공업체는 [추천 이메일 클라이언트](../email-clients.md) 중 어느 것과도 함께 사용할 수 있습니다. 인증 방식에 따라, 제공업체나 이메일 클라이언트가 [OAuth](account-creation.md#sign-in-with-oauth)나 브리지 애플리케이션을 지원하지 않으면 보안이 저하될 수 있습니다. 단순 비밀번호 인증으로는 [다중 인증](multi-factor-authentication.md)을 사용할 수 없기 때문입니다.

### 개인 키를 어떻게 보호해야 하나요? { #how-do-i-protect-my-private-keys }

스마트 카드([유비키](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP)나 [니트로키](../security-keys.md#nitrokey) 등)는 이메일/웹메일 클라이언트를 실행하는 기기(휴대폰, 태블릿, 컴퓨터 등)로부터 암호화된 이메일 메시지를 받아 작동합니다. 그러면 스마트 카드가 메시지를 복호화하고, 복호화된 내용을 기기로 다시 보냅니다.

복호화가 스마트 카드에서 이루어지므로, 침해된 기기에 개인 키가 노출될 가능성을 피할 수 있다는 장점이 있습니다.

## 이메일 메타데이터 개요 { #email-metadata-overview }

이메일 메타데이터는 이메일 메시지의 [메시지 헤더](https://en.wikipedia.org/wiki/Email#Message_header)에 저장되며, `To`(받는 사람), `From`(보낸 사람), `Cc`(참조), `Date`(날짜), `Subject`(제목)처럼 여러분이 본 적이 있을 법한 표시되는 헤더가 포함됩니다. 또한 많은 이메일 클라이언트와 제공업체가 추가하는 여러 숨겨진 헤더도 있으며, 이를 통해 여러분의 계정에 대한 정보가 드러날 수 있습니다.

클라이언트 소프트웨어는 이메일 메타데이터를 사용해 메시지의 발신자와 수신 시간을 표시할 수 있습니다. 서버는 메타데이터를 이메일 메시지를 어디로 보내야 하는지 결정하는 데 사용하며, 항상 투명하게 공개되지는 않는 [다른 목적](https://en.wikipedia.org/wiki/Email#Message_header)으로도 사용할 수 있습니다.

### 이메일 메타데이터는 누가 볼 수 있나요? { #who-can-view-email-metadata }

이메일 메타데이터는 [기회적 TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS)를 통해 외부 관찰자로부터 보호되지만, 이메일 클라이언트 소프트웨어(또는 웹메일)와 이메일 제공업체를 포함해 여러분에게서 수신자에게 메시지를 중계하는 모든 서버는 여전히 메타데이터를 볼 수 있습니다. 이메일 서버는 스팸 방지를 위해 제3자 서비스를 이용하기도 하는데, 이러한 서비스도 일반적으로 여러분의 메시지에 접근할 수 있습니다.

### 메타데이터는 왜 E2EE를 적용할 수 없나요? { #why-cant-metadata-be-e2ee }

이메일 메타데이터는 이메일의 가장 기본적인 기능(어디에서 왔고 어디로 가야 하는지)에 반드시 필요합니다. E2EE는 원래 표준 이메일 프로토콜에 내장되어 있지 않았기 때문에, OpenPGP 같은 추가 소프트웨어가 필요합니다. OpenPGP 메시지는 여전히 기존 이메일 제공업체와 호환되어야 하기 때문에, 통신 당사자를 식별하는 데 필요한 일부 이메일 메타데이터를 암호화할 수 없습니다. 즉, OpenPGP를 사용하더라도 외부 관찰자는 이메일을 주고받는 상대, 이메일을 보낸 시간 등 메시지에 관한 많은 정보를 볼 수 있습니다.
