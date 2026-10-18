---
title: "언어 도구"
icon: material/alphabetical-variant
description: 이 언어 도구는 입력한 텍스트를 서버로 보내지 않으며, 오프라인에서 사용하거나 자체 호스팅할 수 있습니다.
cover: language-tools.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

문법·맞춤법·문체 검사기와 번역 서비스에 입력한 텍스트에는 민감한 정보가 담길 수 있으며, 이러한 정보는 서버에 무기한 저장되거나 제3자에게 판매될 수 있습니다. 이 페이지에 소개된 언어 도구는 제출한 텍스트를 서버에 저장하지 않으며, 데이터를 최대한 통제할 수 있도록 자체 호스팅하거나 오프라인에서 사용할 수 있습니다.

## 번역 도구 { #translation-tools }

### 리브레트랜슬레이트 { #libretranslate }

<div class="admonition recommendation" markdown>

![리브레트랜슬레이트 로고](assets/img/language-tools/libretranslate.png){ align=right }

**리브레트랜슬레이트**는 자유 오픈 소스 기계 번역 웹 인터페이스이자 API 서버입니다. 번역에는 백엔드에서 [아르고스 트랜슬레이트](https://github.com/argosopentech/argos-translate) 모델을 사용합니다.

[:octicons-home-16: 홈페이지](https://libretranslate.com){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/LibreTranslate/LibreTranslate#mirrors){ .card-link title="공개 인스턴스" }
[:octicons-code-16:](https://github.com/LibreTranslate/LibreTranslate){ .card-link title="소스 코드" }

</div>

여러 공개 인스턴스를 통해 리브레트랜슬레이트를 사용할 수 있으며, 그중 일부는 [토르](tor.md) 어니언 서비스나 [I2P](alternative-networks.md#i2p-the-invisible-internet-project) 이프사이트를 제공합니다. 번역을 위해 제출하는 텍스트를 최대한 통제하고 싶다면 소프트웨어를 직접 호스팅할 수도 있습니다.

프라이버시 가이드는 자체 호스팅한 리브레트랜슬레이트 인스턴스를 사용해 [포럼](https://discuss.privacyguides.net)의 게시물을 여러 언어로 자동 번역하고 있습니다.

프라이버시 가이드는 깃허브 저장소 구성에서 VSCode 확장 프로그램을 사용하여 웹사이트와 기사의 문법 및 맞춤법 오류를 찾고 있습니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

- 오픈 소스여야 합니다.
- 완전히 오프라인으로 작동해야 합니다.
