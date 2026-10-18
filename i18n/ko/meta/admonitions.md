---
title: 안내 상자
description: 웹사이트 기여자를 위한 안내 상자 작성 가이드입니다.
---

**안내 상자**(admonition, "콜아웃"이라고도 함)는 글쓴이가 문서의 흐름을 방해하지 않고 글에 부가 내용을 넣을 수 있는 도구입니다.

<div class="admonition example" markdown>
<p class="admonition-title">안내 상자 예시</p>

안내 상자의 예시입니다. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</div>

<details class="example" markdown>
<summary>접을 수 있는 안내 상자 예시</summary>

접을 수 있는 안내 상자의 예시입니다. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</details>

## 형식 { #formatting }

페이지에 안내 상자를 추가하려면 다음 코드를 사용하세요:

```markdown title="Admonition"
<div class="admonition TYPE" markdown>
<p class="admonition-title">TITLE</p>

ENCLOSED TEXT

</div>
```

```markdown title="Collapsible Admonition"
<details class="TYPE" markdown>
<summary>TITLE</summary>

ENCLOSED TEXT

</details>
```

`TITLE`은 반드시 지정해야 합니다. 특정 제목을 원하지 않는다면 `TYPE`(아래 참조)과 같은 텍스트를 첫 글자만 대문자로 써서 지정할 수 있습니다(예: `Note`). `ENCLOSED TEXT`는 마크다운 형식으로 작성해야 합니다.

### 일반 유형 { #regular-types }

위 예시의 `TYPE`을 다음 중 하나로 바꾸세요:

#### `note`

<div class="admonition note" markdown>
<p class="admonition-title">참고</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `abstract`

<div class="admonition abstract" markdown>
<p class="admonition-title">요약</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `info`

<div class="admonition info" markdown>
<p class="admonition-title">정보</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `tip`

<div class="admonition tip" markdown>
<p class="admonition-title">팁</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `success`

<div class="admonition success" markdown>
<p class="admonition-title">성공</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `question`

<div class="admonition question" markdown>
<p class="admonition-title">질문</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `warning`

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `failure`

<div class="admonition failure" markdown>
<p class="admonition-title">실패</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `danger`

<div class="admonition danger" markdown>
<p class="admonition-title">위험</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `bug`

<div class="admonition bug" markdown>
<p class="admonition-title">버그</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `example`

<div class="admonition example" markdown>
<p class="admonition-title">예시</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `quote`

<div class="admonition quote" markdown>
<p class="admonition-title">인용</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

### 특수 유형 { #special-types }

#### `recommendation`

이 형식은 추천 카드를 만드는 데 사용됩니다. 특히 `<p class="admonition-title">` 요소가 없다는 점이 다릅니다.

```markdown title="Recommendation Card"
<div class="admonition recommendation" markdown>

![PhotoPrism logo](assets/img/self-hosting/photoprism.svg){ align=right }

**PhotoPrism** is a self-hostable platform for managing photos. It supports album syncing and sharing as well as a variety of other [features](https://photoprism.app/features). It does not include end-to-end encryption, so it's best hosted on a server that you trust and is under your control.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

</div>
```

<div class="result" markdown>

<div class="admonition recommendation" markdown>

![포토프리즘 로고](../assets/img/self-hosting/photoprism.svg){ align=right }

**포토프리즘**은 사진을 관리하는 자체 호스팅 가능한 플랫폼입니다. 앨범 동기화 및 공유는 물론 다양한 [기능](https://photoprism.app/features)을 지원합니다. 종단 간 암호화를 지원하지 않으므로, 신뢰할 수 있고 직접 관리하는 서버에서 호스팅하는 것이 가장 좋습니다.

[:octicons-home-16: 홈페이지](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="소스 코드" }

</div>

</div>

#### `downloads`

다운로드 링크가 담긴 섹션을 만드는 데 사용되는 특수한 유형의 접을 수 있는 안내 상자입니다. 위 예시처럼 추천 카드 안에서만 사용됩니다.

```markdown title="Downloads Section"
<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>
```

<div class="result" markdown>

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id979659905)
- [:simple-github: 깃허브](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: 윈도우](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: 리눅스](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: 웹](https://mail.proton.me)

</details>

</div>

## 이전 형식 { #old-format }

사이트 곳곳에서 다음 예시와 같은 형식의 안내 상자를 볼 수 있습니다:

```markdown title="Admonition"
!!! note

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<div class="admonition note" markdown>
<p class="admonition-title">참고</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</div>

</div>

```markdown title="Collapsible Admonition"
??? example "Custom Title"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<details class="example" markdown>
<summary>사용자 지정 제목</summary>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</details>

</div>

**이 형식은 앞으로 더 이상 사용되지 않습니다**. 크라우딘에서 사용하는 번역 소프트웨어의 최신 버전과 호환되지 않기 때문입니다. 사이트에 새 페이지를 추가할 때는 HTML 기반의 새 형식만 사용해야 합니다.

이전 형식의 안내 상자를 서둘러 새 형식으로 변환할 필요는 없습니다. 현재 이 형식을 사용하는 페이지도 계속 정상적으로 작동하지만, 사이트를 꾸준히 업데이트하면서 점차 위의 HTML 기반 새 형식으로 바꿔 나갈 예정입니다.
