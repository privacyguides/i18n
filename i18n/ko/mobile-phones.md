---
title: 휴대폰
icon: material/cellphone-check
description: 이 모바일 기기는 커스텀 안드로이드 운영 체제를 위한 최고의 하드웨어 보안 지원을 제공합니다.
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: 휴대폰 추천
    url: "./"
  - "@context": http://schema.org
    "@type": Product
    name: Pixel
    brand:
      "@type": Brand
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://en.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Review
      author:
        "@type": Organization
        name: Privacy Guides
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy){ .pg-orange }

대부분의 **휴대폰**은 OEM으로부터 짧거나 제한된 기간 동안만 보안 업데이트를 받습니다. 지원 기간이 끝난 기기는 더 이상 펌웨어나 드라이버 보안 업데이트를 받지 못하므로 안전하다고 볼 수 **없습니다**.

여기에 소개된 모바일 기기는 보안 업데이트가 보장되는 기간이 길며, 안드로이드 보안 모델을 위반하지 않고 커스텀 운영 체제를 설치할 수 있습니다.

[추천 안드로이드 배포판 :material-arrow-right-drop-circle:](android/distributions.md){ .md-button .md-button--primary } [안드로이드 보안 자세히 알아보기 :material-arrow-right-drop-circle:](os/android-overview.md#security-protections){ .md-button }

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

(그래핀OS의 "확장 지원" 기기 같은) 지원이 종료된 기기는 OEM이 지원을 중단했기 때문에 완전한 보안 패치(펌웨어 업데이트)를 받지 못합니다. 이러한 기기는 어떤 소프트웨어를 설치하든 완전히 안전하다고 볼 수 없습니다.

</div>

## 일반적인 구매 조언 { #general-purchasing-advice }

기기를 구매할 때는 가능한 한 최신 기기를 구입할 것을 권장합니다. 모바일 기기의 소프트웨어와 펌웨어는 제한된 기간 동안만 지원되므로, 새 기기를 사면 그 기간을 최대한 늘릴 수 있습니다.

이동통신사에서 판매하는 휴대폰은 피하세요. 이러한 휴대폰은 **부트로더가 잠겨** 있고 [OEM 잠금 해제](https://source.android.com/devices/bootloader/locking_unlocking)를 지원하지 않는 경우가 많습니다. 이러한 휴대폰 변형 모델에는 어떤 종류의 대체 안드로이드 배포판도 설치할 수 없습니다.

온라인 마켓플레이스에서 중고 휴대폰을 구매할 때는 매우 **주의**해야 합니다. 항상 판매자의 평판을 확인하세요. 도난당한 기기라면 [IMEI 데이터베이스](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database)에 등록되어 있을 가능성이 있습니다. 이전 소유자의 활동과 연관될 위험도 있습니다.

안드로이드 기기와 운영 체제 호환성에 관한 몇 가지 추가 팁은 다음과 같습니다:

- 지원 종료일에 도달했거나 가까운 기기는 구매하지 마세요. 추가 펌웨어 업데이트는 제조업체가 제공해야 합니다.
- 리니지OS나 /e/ OS가 미리 설치된 휴대폰이나, 적절한 [자체 검사 부팅](https://source.android.com/security/verifiedboot) 지원과 펌웨어 업데이트가 없는 안드로이드 휴대폰은 구매하지 마세요. 이러한 기기는 변조되었는지 확인할 방법도 없습니다.
- 요컨대 여기에 소개되지 않은 기기라면 그만한 이유가 있을 가능성이 높습니다. 자세한 내용은 [포럼](https://discuss.privacyguides.net)을 확인해 보세요!

## 구글 픽셀 { #google-pixel }

구글 픽셀 휴대폰은 프라이버시 가이드가 구매를 추천하는 **유일한** 기기입니다. 픽셀 휴대폰은 서드파티 운영 체제에 대한 적절한 AVB 지원과 Secure Element 역할을 하는 구글의 맞춤형 [타이탄](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) 보안 칩 덕분에, 현재 시중의 다른 어떤 안드로이드 기기보다 강력한 하드웨어 보안을 갖추고 있습니다.

<div class="admonition recommendation" markdown>

![구글 픽셀 6](assets/img/android/google-pixel.png){ align=right }

**구글 픽셀** 기기는 보안이 뛰어나기로 유명하며, 커스텀 운영 체제를 설치해도 [자체 검사 부팅](https://source.android.com/security/verifiedboot)을 제대로 지원합니다.

**픽셀 8**과 **8 프로**부터 픽셀 기기는 최소 7년간의 보안 업데이트가 보장되므로, 경쟁 OEM이 일반적으로 제공하는 2~5년보다 훨씬 오래 사용할 수 있습니다.

[:material-shopping: 스토어](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

### 하드웨어 보안 { #hardware-security }

타이탄 M2 같은 Secure Element는 "신뢰할 수 있는" 프로그램을 실행하는 데 쓰이지 않고 비밀 저장, 하드웨어 증명, 속도 제한에만 사용되므로, 대부분의 다른 휴대폰이 사용하는 프로세서의 신뢰 실행 환경(TEE)보다 기능이 제한적입니다. Secure Element가 없는 휴대폰은 이러한 기능을 _모두_ TEE로 처리해야 하므로 공격 표면이 더 넓어집니다.

구글 픽셀 휴대폰은 다른 많은 휴대폰과 달리 [오픈 소스](https://source.android.com/security/trusty#whyTrusty)인 트러스티라는 TEE OS를 사용합니다.

픽셀 8 시리즈 이후 모델은 메모리 손상 버그를 통한 익스플로잇 발생 가능성을 대폭 낮춰 주는 하드웨어 보안 강화 기능인 ARM의 메모리 태깅 확장([MTE](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension))을 지원합니다. 순정 픽셀 OS에서는 구글의 고급 보호 프로그램이나 개발자 옵션을 통해 지원되는 앱에 MTE를 활성화할 수 있지만, 사용성이 상당히 제한적입니다. 프라이버시 가이드가 추천하는 대체 안드로이드 OS인 [그래핀OS](android/distributions.md#grapheneos)는 MTE 구현을 통해 사용성과 적용 범위를 크게 향상합니다.

### 구글 픽셀 구매하기 { #buying-a-google-pixel }

구글 픽셀 구매에 관한 몇 가지 추가 팁은 다음과 같습니다:

- 픽셀 기기를 저렴하게 구매하고 싶다면, 다음 플래그십 모델이 출시된 직후에 "**a**" 모델을 구입할 것을 권장합니다. 구글이 재고를 정리하려고 하기 때문에 보통 할인을 받을 수 있습니다.
- 오프라인 매장에서 제공하는 최저가 보상 옵션이나 특가 행사를 고려해 보세요.
- 여러분이 사는 나라의 온라인 커뮤니티 특가 정보 사이트를 살펴보세요. 좋은 할인 소식을 알려 줄 수 있습니다.
- 구글은 각 기기의 [지원 주기](https://support.google.com/nexus/answer/4457705)를 보여 주는 목록을 제공합니다. 기기의 하루당 가격은 다음과 같이 계산할 수 있습니다: <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext>비용</mtext> <mrow> <mtext>지원 종료일</mtext> <mo>−</mo> <mtext>현재 날짜</mtext> </mrow> </mfrac> </math>
  , 즉 기기를 오래 사용할수록 하루당 비용이 낮아집니다.
- 여러분의 지역에서 픽셀을 구할 수 없다면 [니트로폰](https://shop.nitrokey.com/shop)을 전 세계로 배송받을 수 있습니다.

그래핀OS의 [웹 설치 프로그램](https://grapheneos.org/install/web)을 사용하면 픽셀 휴대폰에 그래핀OS를 쉽게 설치할 수 있습니다. 직접 설치하기가 부담스럽고 약간의 추가 비용을 낼 의향이 있다면, 평판이 좋은 [니트로키](https://nitrokey.com/about)사의 그래핀OS가 사전 설치된 [니트로폰](https://shop.nitrokey.com/shop)을 살펴보세요.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

- 프라이버시 가이드가 추천하는 커스텀 운영 체제 중 하나 이상을 지원해야 합니다.
- 현재 매장에서 새 제품으로 판매되고 있어야 합니다.
- 최소 5년간 보안 업데이트를 받아야 합니다.
- 전용 Secure Element 하드웨어를 갖추고 있어야 합니다.
