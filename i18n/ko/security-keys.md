---
title: 보안 키
icon: material/key-chain
description: 이 보안 키는 이를 지원하는 계정에 대해 피싱에 면역인 인증 방식을 제공합니다.
cover: multi-factor-authentication.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy){ .pg-orange }

물리적 **보안 키**는 온라인 계정에 매우 강력한 보호 계층을 더해 줍니다. [인증 앱](multi-factor-authentication.md)과 비교해 [FIDO2](basics/multi-factor-authentication.md#fido-fast-identity-online) 보안 키 프로토콜은 피싱에 면역이며, 키 자체를 물리적으로 소지하지 않고는 침해할 수 없습니다. 많은 서비스가 계정 보호를 위한 다중 인증 옵션으로 FIDO2/WebAuthn을 지원하며, 일부 서비스는 비밀번호 없는 인증을 통해 보안 키를 강력한 단일 인증 요소로 사용할 수 있게 해 줍니다.

## 유비코 시큐리티 키 { #yubico-security-key }

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![유비코 시큐리티 키 시리즈](assets/img/security-keys/yubico-security-key.webp){ width="315" }
</figure>

**유비코 시큐리티 키** 시리즈는 FIDO 레벨 2 인증[^1]을 받은 하드웨어 보안 키 중 가장 가성비가 좋은 제품입니다. FIDO2/WebAuthn과 FIDO U2F(Universal 2nd Factor)를 지원하며, 보안 키를 2차 인증 요소로 지원하는 대부분의 서비스와 많은 비밀번호 관리자에서 별도 설정 없이 바로 작동합니다.

[:octicons-home-16: 홈페이지](https://yubico.com/products/security-key){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="문서" }

</details>

</div>

이 키는 USB-C와 USB-A 버전으로 모두 제공되며, 두 버전 모두 모바일 기기에서 사용할 수 있도록 NFC를 지원합니다.

이 키는 기본적인 FIDO2 기능만 제공하지만, 대부분의 사람에게는 이것으로 충분합니다. 시큐리티 키 시리즈에 **없는** 주요 기능은 다음과 같습니다:

- [유비코 오센티케이터](https://yubico.com/products/yubico-authenticator)
- CCID 스마트 카드 지원(PIV 호환)
- OpenPGP

이러한 기능이 필요하다면 상위 제품인 [유비키](#yubikey) 시리즈를 고려해 보세요.

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

유비코 시큐리티 키의 펌웨어는 업데이트할 수 없습니다. 최신 펌웨어 버전의 기능이 필요하거나 사용 중인 펌웨어 버전에 취약점이 있다면 새 키를 구매해야 합니다.

</div>

## 유비키 { #yubikey }

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![유비키](assets/img/security-keys/yubikey.png){ width="400" }
</figure>

유비코의 **유비키** 시리즈는 FIDO 레벨 2 인증[^1]을 받은 가장 인기 있는 보안 키 중 하나입니다. **유비키 5 시리즈**는 FIDO2/WebAuthn, FIDO U2F, [TOTP 및 HOTP](https://developers.yubico.com/OATH) 인증, [개인 신원 확인(PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP) 등 다양한 기능을 갖추고 있습니다.

[:octicons-home-16: 홈페이지](https://yubico.com/products/yubikey-5-overview){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="문서" }

</details>

</div>

[비교표](https://yubico.com/store/compare)에서 유비키 제품끼리, 그리고 유비코의 [시큐리티 키](#yubico-security-key) 시리즈와 기능 및 기타 사양을 비교할 수 있습니다. 유비키 시리즈의 장점 중 하나는 키 하나로 하드웨어 보안 키에 기대할 수 있는 거의 모든 기능을 사용할 수 있다는 것입니다. 자신에게 맞는 보안 키를 고를 수 있도록 구매하기 전에 [퀴즈](https://yubico.com/quiz)를 풀어 볼 것을 권장합니다.

유비키는 [유비키 매니저](https://yubico.com/support/download/yubikey-manager)나 [유비키 퍼스널라이제이션 툴](https://yubico.com/support/download/yubikey-personalization-tools)로 설정할 수 있습니다. TOTP 코드를 관리하려면 [유비코 오센티케이터](https://yubico.com/products/yubico-authenticator)를 사용할 수 있습니다. 유비코의 모든 클라이언트는 오픈 소스입니다.

[HOTP와 TOTP를 지원하는](https://support.yubico.com/hc/articles/360013790319-How-many-accounts-can-I-register-my-YubiKey-with) 모델의 경우, 비밀 정보는 키에 암호화되어 저장되며 키를 연결한 기기에 절대 노출되지 않습니다. 시드(공유 비밀)를 유비코 오센티케이터에 입력하면 6자리 코드만 제공할 뿐 시드는 절대 내보내지 않습니다. 이러한 보안 모델은 공격자가 유비코 오센티케이터를 실행하는 기기 중 하나를 침해하더라도 할 수 있는 일을 제한하며, 유비키를 물리적 공격자에게도 강하게 만들어 줍니다.

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

유비키의 펌웨어는 업데이트할 수 없습니다. 최신 펌웨어 버전의 기능이 필요하거나 사용 중인 펌웨어 버전에 취약점이 있다면 새 키를 구매해야 합니다.

</div>

## 니트로키 { #nitrokey }

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![니트로키](assets/img/security-keys/nitrokey.jpg){ width="300" }
</figure>

**니트로키**에는 FIDO2/WebAuthn과 FIDO U2F를 지원하는 가성비 좋은 보안 키인 **니트로키 패스키**가 있습니다. PIV, OpenPGP, TOTP 및 HOTP 인증 같은 기능을 지원받으려면 **니트로키 3** 같은 다른 키를 구매해야 합니다. 현재 [FIDO 레벨 1 인증](https://nitrokey.com/news/2024/nitrokey-3a-mini-receives-official-fido2-certification)을 받은 제품은 **니트로키 3A 미니**뿐입니다.

[:octicons-home-16: 홈페이지](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title="문서" }

</details>

</div>

[비교표](https://nitrokey.com/products/nitrokeys#:~:text=The%20Nitrokey%20Family)에서 여러 니트로키 모델의 기능 및 기타 사양을 비교할 수 있습니다. 니트로키에서 사용할 수 있는 기능에 대한 자세한 내용은 니트로키 [문서](https://docs.nitrokey.com/nitrokeys/features)를 참고하세요.

니트로키 모델은 [니트로키 앱](https://nitrokey.com/download)으로 설정할 수 있습니다.

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

니트로키 3부터는 HOTP와 TOTP 비밀 정보가 저장 시 추가로 암호화됩니다. 니트로키 프로 2나 니트로키 스토리지 2 같은 구형 니트로키 기기는 OTP 비밀 정보를 저장 시 암호화하지 않았으므로, 이러한 기기의 OTP 비밀 정보는 물리적 공격에 취약할 수 있습니다.

</div>

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

### 최소 요구 사항 { #minimum-requirements }

- 고품질의 변조 방지 하드웨어 보안 모듈을 사용해야 합니다.
- 최신 FIDO2 사양을 지원해야 합니다.
- 개인 키 추출을 허용해서는 안 됩니다.
- 35달러가 넘는 기기는 OpenPGP와 S/MIME 처리를 지원해야 합니다.

### 우대 사항 { #best-case }

우대 사항은 이 카테고리에서 완벽한 프로젝트라면 갖추었으면 하는 사항을 나타냅니다. 추천 항목에 이 기능 중 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- USB-C 폼 팩터로 제공되는 것이 좋습니다.
- NFC를 지원하는 제품이 있는 것이 좋습니다.
- TOTP 비밀 정보 저장을 지원하는 것이 좋습니다.
- 안전한 펌웨어 업데이트를 지원하는 것이 좋습니다.

[^1]: 일부 정부나 기관에서는 레벨 2 인증을 받은 키를 요구할 수 있지만, 대부분의 사람은 이 차이를 신경 쓸 필요가 없습니다.
