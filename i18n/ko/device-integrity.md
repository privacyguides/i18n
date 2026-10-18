---
title: "기기 무결성"
icon: material/security
description: 이 도구를 사용하여 기기가 침해되었는지 확인할 수 있습니다.
cover: device-integrity.webp
robots: nofollow, max-snippet:-1, max-image-preview:large
---

이 도구를 사용하면 모바일 기기의 무결성을 검증하고, 페가수스, 프레데터, 킹스폰 같은 스파이웨어와 멀웨어에 의한 침해 지표가 있는지 확인할 수 있습니다. 이 페이지는 **모바일 보안**에 중점을 둡니다. 모바일 기기는 일반적으로 잘 알려진 구성의 읽기 전용 시스템을 갖추고 있어, 기존 데스크톱 시스템보다 악의적인 수정을 탐지하기가 더 쉽기 때문입니다. 앞으로 이 페이지에서 다루는 범위를 넓힐 수도 있습니다.

<div class="admonition note" markdown>
<p class="admonition-title">고급 주제입니다</p>

이 도구는 특정 개인에게 유용할 수 있습니다. 대부분의 사람은 신경 쓸 필요가 없는 기능을 제공하며, 효과적으로 사용하려면 보다 깊은 기술 지식이 필요한 경우가 많습니다.

</div>

공개된 침해 지표로 기기를 검사하는 것만으로는 기기가 "깨끗"하고 특정 스파이웨어 도구의 표적이 되지 않았다고 판단하기에 **충분하지 않다**는 점을 이해하는 것이 **매우 중요합니다**. 공개적으로 사용할 수 있는 이러한 검사 도구에만 의존하면 최근의 보안 동향을 놓칠 수 있으며, 잘못된 안도감을 줄 수 있습니다.

## 일반적인 조언 { #general-advice }

최신 모바일 기기에 대한 시스템 수준 익스플로잇의 대부분, 특히 제로 클릭 공격은 비지속적이므로 재부팅 후에는 남아 있거나 자동으로 실행되지 않습니다. 따라서 기기를 정기적으로 재부팅할 것을 강력히 권장합니다. 누구나 최소 일주일에 한 번은 기기를 재부팅할 것을 권장하며, 비지속형 멀웨어가 특히 우려된다면 프라이버시 가이드와 많은 보안 전문가는 매일 재부팅할 것을 권장합니다.

이렇게 하면 공격자가 접근을 유지하기 위해 기기를 주기적으로 다시 감염시켜야 하지만, 불가능한 일은 아니라는 점도 짚어 둡니다. 기기를 재부팅해도 _지속형_ 멀웨어로부터는 보호되지 않지만, 보안 부팅/자체 검사 부팅 같은 최신 보안 기능 덕분에 모바일 기기에서는 지속형 멀웨어가 비교적 드뭅니다.

## 침해 후 대처 정보 및 면책 조항 { #post-compromise-information-disclaimer }

아래 도구 중 하나라도 페가수스, 프레데터, 킹스폰 같은 스파이웨어에 의한 침해 가능성을 나타낸다면 다음 기관에 연락할 것을 권장합니다:

- 인권 운동가, 언론인 또는 시민 사회 단체 소속이라면: [국제앰네스티 보안 연구소](https://securitylab.amnesty.org/contact-us)
- 기업이나 정부 기기가 침해되었다면: 소속 기업, 부서 또는 기관의 해당 보안 담당자
- 관할 지역의 법 집행 기관

**프라이버시 가이드는 이 이상으로 직접 도와드릴 수 없습니다.** [커뮤니티](https://discuss.privacyguides.net) 공간에서 여러분의 구체적인 상황이나 사정에 대해 기꺼이 이야기 나누고 결과를 검토해 드릴 수는 있지만, 이 페이지에 적힌 내용 이상으로 도움을 드리기는 어렵습니다.

이 페이지의 도구는 침해 지표를 탐지할 수만 있을 뿐, 제거하지는 못합니다. 침해되었을까 우려된다면 다음을 권장합니다:

- 기기를 완전히 교체하는 것을 고려하세요
- SIM/eSIM 번호를 변경하는 것을 고려하세요
- 백업에서 복원하지 마세요. 해당 백업도 침해되었을 수 있습니다

이 도구는 기기에서 접근할 수 있는 정보와 공개적으로 접근 가능한 침해 지표를 바탕으로 분석을 제공합니다. 두 가지를 명심하는 것이 중요합니다:

1. 침해 지표는 말 그대로 _지&#xD45C;_&#xC77C; 뿐입니다. 확정적인 결과가 아니며, 때로는 **오탐**일 수 있습니다. 침해 지표가 탐지되었다면 _잠재적_ 위협에 대해 추가로 조사해야 한다는 뜻입니다.
2. 이 도구가 찾는 침해 지표는 위협 연구 기관에서 공개한 것이지만, 모든 지표가 공개되는 것은 아닙니다! 즉, 공개된 어떤 지표로도 탐지되지 않는 스파이웨어에 기기가 감염되어 있다면 이 도구는 **미탐**(거짓 음성) 결과를 보여 줄 수 있습니다. 신뢰할 수 있고 포괄적인 디지털 포렌식 지원과 분류를 위해서는 비공개 지표, 연구, 위협 인텔리전스에 접근할 수 있어야 합니다.

## 외부 검증 도구 { #external-verification-tools }

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

외부 검증 도구는 컴퓨터에서 실행되며 모바일 기기의 포렌식 흔적을 검사하는데, 이는 잠재적인 침해를 식별하는 데 도움이 됩니다.

<div class="admonition danger" markdown>
<p class="admonition-title">위험</p>

공개된 침해 지표만으로는 기기가 "깨끗"하고 특정 스파이웨어 도구의 표적이 되지 않았다고 판단하기에 충분하지 않습니다. 공개 지표에만 의존하면 최근의 포렌식 흔적을 놓칠 수 있으며, 잘못된 안도감을 줄 수 있습니다.

신뢰할 수 있고 포괄적인 디지털 포렌식 지원과 분류를 위해서는 비공개 지표, 연구, 위협 인텔리전스에 접근할 수 있어야 합니다.

시민 사회는 [국제앰네스티 보안 연구소](https://amnesty.org/en/tech)나 [액세스 나우의 디지털 보안 헬프라인](https://accessnow.org/help)을 통해 이러한 지원을 받을 수 있습니다.

</div>

이 도구는 오탐을 일으킬 수 있습니다. 이 도구 중 하나라도 침해 지표를 발견했다면, 실제 위험을 판단하기 위해 더 깊이 조사해야 합니다. 일부 보고는 과거에 방문한 웹사이트로 인한 오탐일 수 있으며, 수년 전의 탐지 결과는 오탐이거나 이전의 (더 이상 활성 상태가 아닌) 침해를 나타낼 가능성이 높습니다.

### 모바일 검증 툴킷 { #mobile-verification-toolkit }

<div class="admonition recommendation" markdown>

![MVT 로고](assets/img/device-integrity/mvt.webp#only-light){ align=right }
![MVT 로고](assets/img/device-integrity/mvt-dark.png#only-dark){ align=right }

**모바일 검증 툴킷**(**MVT**)은 알려진 스파이웨어 캠페인에 의한 표적 공격이나 감염의 잠재적 흔적이 있는지 모바일 기기를 검사하는 과정을 단순화하고 자동화하는 유틸리티 모음입니다. MVT는 국제앰네스티가 개발했으며 [페가수스 프로젝트](https://forbiddenstories.org/about-the-pegasus-project)의 일환으로 2021년에 공개되었습니다.

[:octicons-home-16: 홈페이지](https://mvt.re){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-apple: macOS](https://docs.mvt.re/en/latest/install)
- [:simple-linux: 리눅스](https://docs.mvt.re/en/latest/install)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

MVT를 사용하는 것만으로는 기기가 "깨끗"하고 특정 스파이웨어 도구의 표적이 되지 않았다고 판단하기에 충분하지 않습니다.

</div>

MVT는 iOS 기기를 검사할 때 _가장_ 유용합니다. 안드로이드는 잠재적인 침해를 분류하는 데 유용한 진단 정보를 거의 저장하지 않으므로, `mvt-android`의 기능도 제한적입니다. 반면 암호화된 iOS 아이튠즈 백업에는 기기에 저장된 파일이 충분히 포함되어 있어, 많은 경우 의심스러운 흔적을 탐지할 수 있습니다. 그렇더라도 MVT는 iOS와 안드로이드 분석 모두에 상당히 유용한 도구를 제공합니다.

iOS를 사용하고 있고 고위험군에 속한다면 세 가지를 추가로 제안합니다:

1. 정기적으로(매월) 아이튠즈 백업을 만들어 보관하세요. 이렇게 하면 향후 새로운 위협이 발견되었을 때 MVT로 과거의 감염을 찾아내고 진단할 수 있습니다.

2. _sysdiagnose_ 로그를 자주 생성하고 외부에 백업하세요. 이 로그는 필요한 경우 향후 포렌식 조사관에게 매우 귀중한 데이터가 될 수 있습니다.

   방법은 모델마다 다르지만, 최신 휴대폰에서는 짧은 진동이 느껴질 때까지 _전원_ + _음량 높이기_ + _음량 낮추기_ 버튼을 함께 길게 눌러 생성할 수 있습니다. 몇 분 후, 타임스탬프가 찍힌 _sysdiagnose_ 로그가 **설정** > **개인정보 보호 및 보안** > **분석 및 향상** > **분석 데이터**에 나타납니다.

3. [차단 모드](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode)를 활성화하세요.

기기가 탈옥되어 있다면 MVT로 더 깊이 있는 검사/분석을 수행할 수 있습니다. 무엇을 하는지 정확히 알지 못한다면 **기기를 탈옥하거나 루팅하지 마세요.** 기기를 탈옥하면 상당한 보안 위험에 노출됩니다.

### 아이메이징(iOS) { #imazing-ios }

<div class="admonition recommendation" markdown>

![아이메이징 로고](assets/img/device-integrity/imazing.png){ align=right }

**아이메이징**은 iOS 기기용 무료 스파이웨어 분석 도구를 제공하며, 이 도구는 [MVT](#mobile-verification-toolkit)의 GUI 래퍼 역할을 합니다. 기술 전문가와 포렌식 조사관을 위해 설계된 명령줄 도구인 MVT 자체보다 훨씬 쉽게 실행할 수 있습니다.

[:octicons-home-16: 홈페이지](https://imazing.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title="문서"}

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://imazing.com/download)
- [:simple-apple: macOS](https://imazing.com/download)

</details>

</div>

아이메이징은 다양한 위협 연구자들이 공개한, 공개적으로 접근 가능한 침해 지표가 있는지 [MVT](#mobile-verification-toolkit)로 기기를 검사하는 과정을 자동화하고 대화형으로 안내합니다. MVT에 적용되는 모든 정보와 경고가 이 도구에도 똑같이 적용되므로, 위 섹션의 MVT 관련 참고 사항도 함께 숙지해 두시기 바랍니다.

## 기기 내 검증 { #on-device-verification }

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy){ .pg-orange }

기기와 운영 체제에 변조 흔적이 있는지 확인하고 기기의 신원을 검증하는, 설치해서 사용하는 앱입니다.

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

이러한 앱을 사용하는 것만으로는 기기가 "깨끗"하고 특정 스파이웨어 도구의 표적이 되지 않았다고 판단하기에 충분하지 않습니다.

</div>

### 오디터(안드로이드) { #auditor-android }

<div class="admonition recommendation" markdown>

![오디터 로고](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![오디터 로고](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**오디터**는 하드웨어 보안 기능을 활용하여 기기의 신원과 운영 체제의 무결성을 능동적으로 검증함으로써 기기 무결성 모니터링을 제공하는 앱입니다. 현재는 [지원되는 기기](https://attestation.app/about#device-support)의 그래핀OS 또는 순정 운영 체제에서만 작동합니다.

[:octicons-home-16: 홈페이지](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title="문서"}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
- [:simple-github: 깃허브](https://github.com/GrapheneOS/Auditor/releases)
- [:material-cube-outline: 그래핀OS 앱 스토어](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

오디터는 이 페이지의 다른 도구처럼 검사/분석 도구가 아닙니다. 대신 기기의 하드웨어 기반 키 저장소를 사용하여 기기의 신원을 검증하고, 자체 검사 부팅을 통해 운영 체제 자체가 변조되거나 다운그레이드되지 않았다는 확신을 얻을 수 있게 해 줍니다. 이를 통해 기기 자체에 대해 매우 견고한 무결성 검사를 제공하지만, 기기에서 실행되는 사용자 수준 앱이 악성인지까지 반드시 확인하는 것은 아닙니다.

오디터는 _피감사 기기_(검증받는 기기)와 _감사 기기_(검증을 수행하는 기기), **두 대**의 기기로 증명과 침입 탐지를 수행합니다. 감사 기기는 안드로이드 10 이상의 모든 기기(또는 [그래핀OS](android/distributions.md#grapheneos)가 운영하는 원격 웹 서비스)가 될 수 있지만, 피감사 기기는 특별히 [지원되는 기기](https://attestation.app/about#device-support)여야 합니다. 오디터는 다음과 같이 작동합니다:

- _감사 기&#xAE30;_&#xC640; _피감사 기기_ 간의 [최초 사용 시 신뢰(TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) 모델을 사용하여, 두 기기는 _오디&#xD130;_&#xC758; [하드웨어 기반 키 저장소](https://source.android.com/security/keystore)에 개인 키를 설정합니다.
- _감사 기&#xAE30;_&#xB294; 다른 오디터 앱 인스턴스이거나 [원격 증명 서비스](https://attestation.app)일 수 있습니다.
- _감사 기&#xAE30;_&#xB294; _피감사 기&#xAE30;_&#xC758; 현재 상태와 구성을 기록합니다.
- 페어링이 완료된 후 _피감사 기&#xAE30;_&#xC758; 운영 체제가 변조되면, 감사 기기는 기기 상태와 구성의 변화를 인지하게 됩니다.
- 그러면 변경 사항에 대한 알림을 받게 됩니다.

오디터는 TOFU 모델을 사용하므로 최초 페어링 **이후**의 변경 사항만 효과적으로 탐지할 수 있으며, 페어링 도중이나 이전의 변경 사항은 탐지하지 못할 수 있다는 점에 유의해야 합니다. 하드웨어와 운영 체제가 정품인지 확인하려면, 기기를 설치한 직후 인터넷에 연결하기 전에 [로컬 증명을 수행](https://grapheneos.org/install/web#verifying-installation)하세요.

증명 서비스에는 개인 식별 정보가 전송되지 않습니다. 지속적인 모니터링을 위해 익명 계정으로 가입하고 원격 증명을 활성화할 것을 권장합니다.

[위협 모델](basics/threat-modeling.md)상 증명 서비스로부터 IP 주소를 숨겨야 한다면 [오봇](alternative-networks.md#orbot)이나 [VPN](vpn.md) 사용을 고려해 볼 수 있습니다.
