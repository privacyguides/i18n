---
title: "애플리케이션 받기"
description: 구글 플레이 서비스를 거치지 않고 안드로이드에서 애플리케이션을 받을 수 있는 방법으로 다음을 권장합니다.
---

구글 플레이 서비스를 거치지 않고도, 심지어 플레이 스토어에서도 프라이버시를 지키며 안드로이드 앱을 받을 수 있는 방법은 많습니다. 안드로이드에서 애플리케이션을 받는 방법으로 다음을 권장하며, 우선순위 순으로 정리했습니다.

## 옵테이니엄 { #obtainium }

<div class="admonition recommendation" markdown>

![옵테이니엄 로고](../assets/img/android/obtainium.svg){ align=right }

**옵테이니엄**은 앱을 중앙화된 앱 스토어/저장소가 아닌 개발자의 자체 릴리스 페이지(예: 깃허브, 깃랩, 개발자 웹사이트 등)에서 직접 설치하고 업데이트할 수 있게 해 주는 앱 관리자입니다. 안드로이드 12 이상에서는 백그라운드 자동 업데이트를 지원합니다.

[:octicons-repo-16: 저장소](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-github: 깃허브](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

옵테이니엄을 사용하면 매우 다양한 출처에서 APK 설치 파일을 다운로드할 수 있으며, 해당 출처와 앱이 신뢰할 수 있는 정식 출처와 앱인지 확인하는 것은 사용자의 몫입니다. 예를 들어 옵테이니엄으로 [시그널의 APK 배포 페이지](https://signal.org/android/apk)에서 시그널을 설치하는 것은 문제가 없겠지만, 앱토이드나 APKPure 같은 서드파티 APK 저장소에서 설치하는 것은 추가적인 위험을 초래할 수 있습니다. 악성 _업데이&#xD2B8;_&#xB97C; 설치할 위험은 상대적으로 낮은데, 안드로이드가 앱 업데이트를 설치하기 전에 해당 업데이트가 휴대폰에 이미 설치된 앱과 동일한 개발자에 의해 서명되었는지 자체적으로 확인하기 때문입니다.

## 그래핀OS 앱 스토어 { #grapheneos-app-store }

그래핀OS의 앱 스토어는 [깃허브](https://github.com/GrapheneOS/Apps/releases)에서 받을 수 있습니다. 안드로이드 12 이상을 지원하며, 앱 스토어 자체도 스스로 업데이트할 수 있습니다. 이 앱 스토어에서는 [오디터](../device-integrity.md#auditor-android), [카메라](general-apps.md#secure-camera), [PDF 뷰어](general-apps.md#secure-pdf-viewer) 등 그래핀OS 프로젝트에서 개발한 독립형 애플리케이션을 받을 수 있습니다. 이러한 애플리케이션이 필요하다면 플레이 스토어 대신 그래핀OS 앱 스토어에서 받는 것을 강력히 권장합니다. 그래핀OS 앱 스토어의 앱은 구글이 접근할 수 없는 그래핀OS 프로젝트 자체 서명으로 서명되어 있기 때문입니다.

## 오로라 스토어 { #aurora-store }

구글 플레이 스토어는 로그인에 구글 계정이 필요하므로 프라이버시 측면에서 바람직하지 않습니다. 오로라 스토어 같은 대체 클라이언트를 사용하면 이 문제를 피할 수 있습니다.

<div class="admonition recommendation" markdown>

![오로라 스토어 로고](../assets/img/android/aurora-store.webp){ align=right }

**오로라 스토어**는 앱을 다운로드할 때 구글 계정, 구글 플레이 서비스, microG가 필요하지 않은 구글 플레이 스토어 클라이언트입니다.

[:octicons-home-16: 홈페이지](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="개인정보 처리방침" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-gitlab: 깃랩](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

오로라 스토어의 익명 계정 기능으로는 유료 앱을 다운로드할 수 없습니다. 구매한 앱을 다운로드하려면 선택적으로 오로라 스토어에서 구글 계정으로 로그인할 수 있지만, 이 경우 구글이 사용자가 설치한 앱 목록에 접근할 수 있게 됩니다. 그렇더라도 기기에 정식 구글 플레이 클라이언트와 구글 플레이 서비스 또는 microG를 설치하지 않아도 된다는 이점은 여전히 누릴 수 있습니다.

## RSS 알림을 활용한 수동 설치 { #manually-with-rss-notifications }

깃허브나 깃랩 같은 플랫폼에서 배포되는 앱이라면, [뉴스 애그리게이터](../news-aggregators.md)에 RSS 피드를 추가하여 새 릴리스를 추적할 수 있습니다.

![RSS APK](../assets/img/android/rss-apk-light.png#only-light) ![RSS APK](../assets/img/android/rss-apk-dark.png#only-dark) ![APK 변경 사항](../assets/img/android/rss-changes-light.png#only-light) ![APK 변경 사항](../assets/img/android/rss-changes-dark.png#only-dark)

### 깃허브 { #github }

깃허브에서는 [시큐어 카메라](general-apps.md#secure-camera)를 예로 들면, 해당 앱의 [릴리스 페이지](https://github.com/GrapheneOS/Camera/releases)로 이동한 뒤 URL 끝에 `.atom`을 추가하면 됩니다:

`https://github.com/GrapheneOS/Camera/releases.atom`

### 깃랩 { #gitlab }

깃랩에서는 [오로라 스토어](#aurora-store)를 예로 들면, 해당 앱의 [프로젝트 저장소](https://gitlab.com/AuroraOSS/AuroraStore)로 이동한 뒤 URL 끝에 `/-/tags?format=atom`을 추가하면 됩니다:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

### APK 지문 확인하기 { #verifying-apk-fingerprints }

APK 파일을 직접 다운로드하여 수동으로 설치하는 경우, 안드로이드 [build-tools](https://developer.android.com/studio/releases/build-tools)에 포함된 [`apksigner`](https://developer.android.com/studio/command-line/apksigner) 도구로 서명을 확인할 수 있습니다.

1. [자바 JDK](https://oracle.com/java/technologies/downloads)를 설치합니다.

2. [안드로이드 스튜디오 명령줄 도구](https://developer.android.com/studio#command-tools)를 다운로드합니다.

3. 다운로드한 압축 파일을 해제합니다:

   ```bash
   unzip commandlinetools-*.zip
   cd cmdline-tools
   ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
   ```

4. 서명 확인 명령을 실행합니다:

   ```bash
   ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
   ```

5. 출력된 해시를 다른 출처의 값과 비교합니다. 시그널처럼 일부 개발자는 웹사이트에 [지문을 공개](https://signal.org/android/apk)하고 있습니다.

   ```bash
   Signer #1 certificate DN: CN=GrapheneOS
   Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
   Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
   Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
   ```

## F-Droid

![F-Droid 로고](../assets/img/android/f-droid.svg){ align=right width=120px }

\==F-Droid는 위의 방법으로 받을 수 없는 앱을 받는 용도로만 권장합니다.== F-Droid는 특히 프라이버시 커뮤니티에서 구글 플레이의 대안으로 자주 추천됩니다. 서드파티 저장소를 추가할 수 있어 구글의 폐쇄형 생태계에 갇히지 않아도 된다는 점이 인기의 요인입니다. 또한 F-Droid는 일부 애플리케이션에 대해 [재현 가능한 빌드](https://f-droid.org/en/docs/Reproducible_Builds)를 제공하며, 자유 오픈 소스 소프트웨어에 전념하고 있습니다. 하지만 F-Droid가 패키지를 빌드하고, 서명하고, 배포하는 방식에는 보안과 관련된 몇 가지 단점이 있습니다:

앱을 빌드하는 과정 때문에 _공식_ F-Droid 저장소의 앱은 업데이트가 늦어지는 경우가 많습니다. 또한 F-Droid 관리자는 패키지 ID를 재사용하면서 자체 키로 앱에 서명하는데, 이는 F-Droid 팀에 절대적인 신뢰를 부여하는 것이므로 바람직하지 않습니다. 게다가 공식 F-Droid 저장소에 앱이 등록되기 위한 요건은 구글 플레이 같은 다른 앱 스토어보다 덜 엄격하기 때문에, F-Droid에는 오래되었거나 유지 관리되지 않거나 더 이상 [최신 보안 기준](https://developer.android.com/google/play/requirements/target-sdk)을 충족하지 않는 앱이 훨씬 많은 편입니다.

[이지온드로이드](https://apt.izzysoft.de/fdroid) 같은 다른 인기 있는 F-Droid 서드파티 저장소는 이러한 우려를 일부 해소해 줍니다. 이지온드로이드 저장소는 코드 호스팅 플랫폼(깃허브, 깃랩 등)에서 빌드를 직접 가져오므로 개발자 자체 저장소 다음으로 가장 좋은 선택지입니다. 또한 수백 개의 애플리케이션에 대해 [재현 가능한 빌드](https://android.izzysoft.de/articles/named/iod-rbs-mirrors-clients)를 제공하며, 개발자가 서명한 APK의 재현 가능성을 검증하는 개발자들도 두고 있습니다. 아울러 이지온드로이드 팀은 저장소에 등록된 앱을 대상으로 [추가 보안 검사](https://android.izzysoft.de/articles/named/iod-scan-apkchecks)를 수행하며, 이는 대개 앱의 프라이버시 개선을 위한 팀과 앱 개발자 간의 [논의](https://github.com/gouravkhunger/QuotesApp/issues/22)로 이어집니다. 단, [특정 상황](https://gitlab.com/IzzyOnDroid/repo#are-apps-removed-from-the-repo--and-when-does-that-happen)에서는 앱이 이지온드로이드 저장소에서 삭제될 수 있다는 점에 유의하세요.

[F-Droid](https://f-droid.org/en/packages)와 [이지온드로이드](https://apt.izzysoft.de/fdroid) 저장소에는 수많은 앱이 있으므로, 오픈 소스 앱을 검색하고 발견하는 곳으로 유용하게 활용할 수 있습니다. 이렇게 찾은 앱은 플레이 스토어나 오로라 스토어 등 다른 경로를 통하거나 개발자에게서 APK를 직접 받아 설치하면 됩니다. 이 방법으로 새 앱을 찾을 때는 신중하게 판단해야 하며, 앱이 얼마나 자주 업데이트되는지도 꼭 살펴봐야 합니다. 오래된 앱은 지원이 종료된 라이브러리 등에 의존할 수 있어 잠재적인 보안 위험이 될 수 있습니다.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

드물게 F-Droid를 통해서만 받을 수 있는 앱도 있습니다. 그런 앱이 꼭 필요하다면 기존 F-Droid 앱 대신 최신 [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) 클라이언트를 사용해 받는 것을 권장합니다. F-Droid Basic은 기능이 축소되어 있어 공격 표면이 줄어들기 때문입니다.

</div>
