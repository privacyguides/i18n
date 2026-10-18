---
title: 이메일 서버
meta_title: "이메일 자체 호스팅 - 프라이버시 가이드"
icon: material/email
description: 기술적인 지식이 있는 독자라면 이메일을 직접 자체 호스팅하여 데이터를 최대한 통제함으로써 프라이버시를 추가로 보장받을 수 있습니다.
cover: email.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-server-network: 서비스 제공업체](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

숙련된 시스템 관리자라면 자신만의 **이메일 서버**를 구축하는 것을 고려해 볼 수 있습니다. 메일 서버는 보안을 유지하고 메일 전송의 안정성을 확보하기 위해 지속적인 관심과 유지 관리가 필요합니다. 아래의 "올인원" 솔루션 외에도, 보다 수동적인 방식을 다루는 몇 가지 글을 골라 두었습니다:

- [OpenSMTPD, Dovecot, Rspamd로 메일 서버 구축하기](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [나만의 메일 서버를 운영하는 방법](https://www.c0ffee.net/blog/mail-server-guide) (2017년 8월)

## 스톨워트 { #stalwart }

<div class="admonition recommendation" markdown>

![스톨워트 로고](../assets/img/self-hosting/stalwart.svg){ align=right }

**스톨워트**는 러스트로 작성된 비교적 새로운 메일 서버로, 표준 IMAP, POP3, SMTP 외에 JMAP도 지원합니다. 다양한 구성 옵션을 제공하면서도 보안과 기능 모두 매우 합리적인 기본 설정을 갖추고 있어 바로 사용하기 쉽습니다. TOTP 2FA를 지원하는 웹 기반 관리 기능을 제공하며, 공개 PGP 키를 입력하면 수신되는 **모든** 메시지를 암호화할 수 있습니다.

[:octicons-home-16: 홈페이지](https://stalw.art){ .md-button .md-button--primary }
[:octicons-info-16:](https://stalw.art/docs/get-started){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/stalwartlabs){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://github.com/sponsors/stalwartlabs){ .card-link title="후원하기" }

</div>

스톨워트의 [PGP 구현](https://stalw.art/docs/encryption/overview)은 프라이버시 가이드가 추천하는 자체 호스팅 솔루션 중 유일한 것으로, 메시지를 암호화하여 저장하는 메일 서버를 직접 운영할 수 있어 이메일에 대한 무단 접근 위험을 줄여 줍니다. 도메인에 웹 키 디렉터리(WKD)도 추가로 구성하고 (썬더버드처럼) 발신 메일에 PGP와 WKD를 지원하는 이메일 클라이언트를 사용한다면, 모든 [프로톤 메일](../email.md#proton-mail) 사용자와 자체 호스팅 환경에서 E2EE 호환성을 확보하는 가장 쉬운 방법입니다.

스톨워트에는 통합 웹메일이 **없으므로**, [전용 이메일 클라이언트](../email-clients.md)와 함께 사용하거나 넥스트클라우드의 메일 앱 같은 자체 호스팅용 오픈 소스 웹메일을 찾아야 합니다.

_프라이버시 가이&#xB4DC;_&#xC5D0;서도 내부 이메일에 스톨워트를 사용하고 있습니다.

## 메일카우 { #mailcow }

<div class="admonition recommendation" markdown>

![메일카우 로고](../assets/img/self-hosting/mailcow.svg){ align=right }

**메일카우**는 리눅스 경험이 있는 분들에게 적합한 고급 메일 서버입니다. DKIM을 지원하는 메일 서버, 바이러스 및 스팸 모니터링, SOGo를 통한 웹메일 및 ActiveSync, 2FA를 지원하는 웹 기반 관리 등 필요한 모든 것을 도커 컨테이너 하나에 담고 있습니다.

[:octicons-home-16: 홈페이지](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="후원하기" }

</div>

## 메일인어박스 { #mail-in-a-box }

<div class="admonition recommendation" markdown>

![메일인어박스 로고](../assets/img/self-hosting/mail-in-a-box.svg){ align=right }

**메일인어박스**는 우분투에 메일 서버를 배포하는 자동화된 설치 스크립트입니다. 사람들이 자신만의 메일 서버를 더 쉽게 구축할 수 있도록 하는 것이 목표입니다.

[:octicons-home-16: 홈페이지](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="소스 코드" }

</div>
