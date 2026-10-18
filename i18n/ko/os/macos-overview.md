---
title: macOS 개요
icon: material/apple-finder
description: macOS는 애플의 하드웨어와 함께 작동하여 강력한 보안을 제공하는 애플의 데스크톱 운영 체제입니다.
---

**macOS**는 애플이 맥 컴퓨터용으로 개발한 유닉스 운영 체제입니다. macOS에서 프라이버시를 강화하려면 원격 측정 기능을 비활성화하고 기존 프라이버시 및 보안 설정을 강화하면 됩니다.

구형 인텔 기반 맥과 해킨토시는 macOS가 제공하는 모든 보안 기능을 지원하지 않습니다. 데이터 보안을 강화하려면 [애플 실리콘](https://support.apple.com/HT211814)을 탑재한 최신 맥을 사용할 것을 권장합니다.

## 프라이버시 참고 사항 { #privacy-notes }

macOS에는 고려해야 할 몇 가지 주목할 만한 프라이버시 문제가 있습니다. 이는 애플의 다른 앱이나 서비스가 아닌 운영 체제 자체와 관련된 것입니다.

### 활성화 잠금 { #activation-lock }

새로 구매한 애플 실리콘 기기는 인터넷 연결 없이도 설정할 수 있습니다. 하지만 맥을 복구하거나 재설정하려면 분실 또는 도난 기기의 활성화 잠금 데이터베이스를 확인하기 위해 애플 서버에 인터넷으로 연결해야 **합니다**.

### 앱 인증서 폐기 확인 { #app-revocation-checks }

macOS는 앱을 열 때 해당 앱에 알려진 멀웨어가 포함되어 있는지, 개발자의 서명 인증서가 폐기되었는지 온라인으로 확인합니다.

애플의 OCSP 서비스는 HTTPS 암호화를 사용하므로, 여러분이 어떤 앱을 여는지는 애플만 볼 수 있습니다. 애플은 이 서비스의 로깅 정책에 대한 [정보를 게시](https://support.apple.com/HT202491)했습니다. 또한 사람들이 이 온라인 확인을 거부할 수 있는 메커니즘을 추가하겠다고 [약속](http://lapcatsoftware.com/articles/2024/8/3.html)했지만, 아직 macOS에 추가되지 않았습니다.

이 확인은 비교적 쉽게 수동으로 [거부할 수 있지만](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private), macOS의 인증서 폐기 확인으로 인해 심각하게 노출될 상황이 아니라면 그렇게 하지 않을 것을 권장합니다. 이 확인은 침해된 앱의 실행을 차단하는 중요한 역할을 하기 때문입니다.

## 권장 설정 { #recommended-configuration }

맥을 처음 설정할 때 만든 계정은 관리자 계정이며, 일반 사용자 계정보다 높은 권한을 가집니다. macOS에는 멀웨어나 기타 프로그램이 관리자 권한을 남용하지 못하게 하는 여러 보호 기능이 있으므로, 일반적으로 이 계정을 사용해도 안전합니다.

하지만 `sudo` 같은 보호 유틸리티에서 [과거에 익스플로잇이 발견된 적](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass)이 있습니다. 실행하는 프로그램이 관리자 권한을 남용할 가능성을 피하고 싶다면, 일상적인 작업에 사용할 두 번째 일반 사용자 계정을 만드는 것을 고려해 볼 수 있습니다. 이렇게 하면 앱이 관리자 권한을 필요로 할 때마다 자격 증명을 요구하므로, 이를 더 분명히 알 수 있다는 장점도 있습니다.

두 번째 계정을 사용한다면 macOS 로그인 화면에서 원래 관리자 계정으로 로그인할 필요는 사실상 없습니다. 일반 사용자로 관리자 권한이 필요한 작업을 할 때는 시스템이 인증을 요청하며, 이때 일반 사용자 상태에서 일회성으로 관리자 자격 증명을 입력할 수 있습니다. 로그인 화면에 계정이 하나만 보이기를 원한다면 관리자 계정을 숨기는 방법에 대한 애플의 [안내](https://support.apple.com/HT203998)를 참고하세요.

### 아이클라우드 { #icloud }

아이클라우드 같은 애플 서비스를 사용하면 대부분의 정보가 애플 서버에 저장되며, 기본적으로 *애플이 접근할 수 있는* 키로 보호됩니다. 애플은 이를 [표준 데이터 보호](https://support.apple.com/en-us/102651)라고 부릅니다.

따라서 아이클라우드를 사용한다면 [**고급 데이터 보호**를 활성화](https://support.apple.com/HT212520)해야 합니다. 고급 데이터 보호는 거의 모든 아이클라우드 데이터를 애플 서버가 아닌 여러분의 기기에 저장된 키로 암호화(종단 간 암호화)하므로, 데이터 유출이 발생해도 아이클라우드 데이터가 안전하며 애플로부터도 숨겨집니다.

아이클라우드를 활성화하지 않고 앱 스토어에서 앱을 설치하고 싶다면, **시스템 설정** 대신 앱 스토어에서 애플 계정에 로그인하면 됩니다.

### 시스템 설정 { #system-settings }

시스템을 강화하기 위해 확인하거나 변경해야 할 내장 설정이 많이 있습니다. **시스템 설정** 앱을 여세요:

#### Bluetooth

- [ ] **Bluetooth** 끄기(현재 사용 중이 아닌 경우)

#### 네트워크 { #network }

**Wi-Fi** 또는 **이더넷** 중 무엇을 사용하는지(초록색 점과 "연결됨"이라는 문구로 표시됨)에 따라 해당 아이콘을 클릭하세요.

네트워크 이름 옆의 "세부사항" 버튼을 클릭하세요:

- [x] **비공개 Wi-Fi 주소**에서 **순환** 선택

- [x] **IP 주소 추적 제한** 켜기

##### 방화벽 { #firewall }

방화벽은 원치 않는 네트워크 연결을 차단합니다. 방화벽 설정이 엄격할수록 맥은 더 안전해집니다. 하지만 일부 서비스가 차단될 수 있습니다. 사용하는 서비스를 차단하지 않는 범위에서 최대한 엄격하게 방화벽을 구성해야 합니다.

- [x] **방화벽** 켜기

**옵션** 버튼을 클릭하세요:

- [x] **들어오는 연결 모두 차단** 켜기

이 구성이 너무 엄격하다면 다시 돌아와 선택을 해제할 수 있습니다. 하지만 앱이 들어오는 연결을 요청하면 macOS는 일반적으로 해당 앱의 연결을 허용할지 묻습니다.

#### 일반 { #general }

기본적으로 기기 이름은 "[여러분의 이름]의 iMac" 같은 형식입니다. 이 이름은 [네트워크에 공개적으로 브로드캐스트](https://support.apple.com/guide/mac-help/change-computers-local-hostname-mac-mchlp2322/26/mac/26#:~:text=The%20local%20hostname%2C%20or%20local%20network%20name%2C%20is%20displayed%20at%20the%20bottom%20of%20the%20Sharing%20settings%20window.%20It%20identifies%20your%20Mac%20to%20Bonjour%2Dcompatible%20services.)되므로, 기기 이름을 "Mac"처럼 일반적인 이름으로 바꾸는 것이 좋습니다.

**정보**를 클릭하고 **이름** 필드에 원하는 기기 이름을 입력하세요.

##### 소프트웨어 업데이트 { #software-updates }

맥에 최신 보안 수정 사항이 적용되도록 사용 가능한 모든 업데이트를 자동으로 설치해야 합니다.

**자동 업데이트** 옆의 작은 :material-information-outline: 아이콘을 클릭하세요:

- [x] **사용 가능한 경우 새로운 업데이트 다운로드** 켜기

- [x] **macOS 업데이트 설치** 켜기

- [x] **보안 응답 및 시스템 파일 설치** 켜기

#### Apple Intelligence 및 Siri

macOS에서 이 기능을 사용하지 않는다면 비활성화해야 합니다:

- [ ] **Apple Intelligence** 끄기
- [ ] **Siri** 끄기

**[애플 인텔리전스](https://apple.com/legal/privacy/data/en/intelligence-engine)**는 기기가 지원하는 경우에만 사용할 수 있습니다. 애플 인텔리전스는 기기 내 처리와, 기기가 제공할 수 있는 것보다 더 많은 처리 능력이 필요한 작업을 위한 [프라이빗 클라우드 컴퓨트](https://security.apple.com/blog/private-cloud-compute)를 함께 사용합니다.

애플 인텔리전스를 통해 전송된 모든 데이터에 대한 보고서를 보려면 **개인정보 보호 및 보안** → **Apple Intelligence 보고서**로 이동하여 **활동 내보내기**를 누르면, 설정에 따라 최근 15분 또는 7일간의 활동을 확인할 수 있습니다. 기기의 앱이 최근 접근한 권한을 보여 주는 **앱 개인정보 보호 리포트**와 마찬가지로, Apple Intelligence 보고서는 애플 인텔리전스를 사용하는 동안 애플 서버로 전송되는 내용을 보여 줍니다.

기본적으로 ChatGPT 통합은 비활성화되어 있습니다. 더 이상 ChatGPT 통합을 원하지 않는다면 **ChatGPT**로 이동하세요:

- [ ] **ChatGPT 사용** 끄기

ChatGPT 통합을 켜 둔다면 매번 확인을 요청하도록 설정할 수도 있습니다:

- [x] **요청 확인** 켜기

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

ChatGPT로 보내는 모든 요청은 ChatGPT 서버로 전송되며, 애플 인텔리전스와 달리 기기 내 처리나 PCC가 없습니다.

</div>

#### 개인정보 보호 및 보안 { #privacy-security }

애플리케이션이 권한을 요청할 때마다 여기에 표시됩니다. 어떤 애플리케이션에 특정 권한을 허용하거나 거부할지 결정할 수 있습니다.

##### 위치 서비스 { #location-services }

앱별로 위치 서비스를 개별적으로 허용할 수 있습니다. 앱이 위치를 사용할 필요가 없다면 위치 서비스를 완전히 끄는 것이 프라이버시를 가장 잘 보호하는 선택입니다.

- [ ] **위치 서비스** 끄기

##### 분석 및 향상 { #analytics-improvements }

애플 및 앱 개발자와 분석 데이터를 공유할지 결정하세요.

##### Apple 광고 { #apple-advertising }

사용 내역에 기반한 개인 맞춤형 광고를 원하는지 결정하세요.

- [ ] **개인 맞춤형 광고** 끄기

##### FileVault

Secure Enclave(애플 T2 보안 칩, 애플 실리콘)가 있는 최신 기기에서는 데이터가 항상 암호화되어 있지만, 기기가 변조를 감지하지 못하면 하드웨어 키로 자동 복호화됩니다. [FileVault](../encryption.md#filevault)를 활성화하면 데이터를 복호화하는 데 비밀번호가 추가로 필요하므로, 특히 전원이 꺼져 있을 때나 전원을 켠 후 처음 로그인하기 전에 보안이 크게 향상됩니다.

구형 인텔 기반 맥 컴퓨터에서는 FileVault가 기본으로 제공되는 유일한 디스크 암호화 방식이므로 항상 활성화해야 합니다.

- [x] **켜기** 클릭

##### 차단 모드 { #lockdown-mode }

**[차단 모드](https://support.apple.com/guide/mac-help/lock-mac-targeted-a-cyberattack-ibrw66f4e191/mac)**는 보안을 강화하기 위해 일부 기능을 비활성화합니다. 일부 앱이나 기능은 차단 모드가 꺼져 있을 때와 다르게 작동합니다. 예를 들어 차단 모드를 활성화하면 사파리에서 자바스크립트 Just-In-Time([JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers)) 컴파일과 [웹어셈블리](https://developer.mozilla.org/docs/WebAssembly)가 비활성화됩니다. 차단 모드를 활성화한 뒤 일상적인 사용에 큰 영향이 있는지 확인해 볼 것을 권장합니다.

- [x] **켜기** 클릭

### MAC 주소 무작위화 { #mac-address-randomization }

macOS는 네트워크에 연결되지 않은 상태에서 [와이파이 검색을 수행](https://support.apple.com/guide/security/privacy-features-connecting-wireless-networks-secb9cb3140c/web)할 때 무작위 MAC 주소를 사용합니다.

네트워크 간, 그리고 같은 네트워크에서 시간에 따른 추적을 막기 위해 네트워크마다 [MAC 주소를 무작위화](https://support.apple.com/en-us/102509)하고 주기적으로 바꾸도록 설정할 수 있습니다.

**시스템 설정** → **네트워크** → **Wi-Fi** → **세부사항**으로 이동하여, 연결된 네트워크에 대해 고정되지만 고유한 주소를 원한다면 **비공개 Wi-Fi 주소**를 **고정**으로, 시간이 지나면서 바뀌기를 원한다면 **순환**으로 설정하세요.

연결된 네트워크에 브로드캐스트되는 또 다른 기기 식별자인 호스트 이름도 변경하는 것을 고려해 보세요. **시스템 설정** → **일반** → **공유**에서 호스트 이름을 "MacBook Air", "Laptop", "John's MacBook Pro", "iPhone"처럼 일반적인 이름으로 설정할 수 있습니다.

## 보안 보호 기능 { #security-protections }

macOS는 서로 다른 특성을 지닌 여러 계층의 소프트웨어 및 하드웨어 기반 보호 기능에 의존하는 심층 방어를 사용합니다. 이를 통해 한 계층에서 문제가 생겨도 시스템 전체의 보안이 침해되지 않도록 합니다.

### 소프트웨어 보안 { #software-security }

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

macOS에서는 베타 업데이트를 설치할 수 있습니다. 베타 업데이트는 불안정하며, 테스트 목적이기 때문에 [추가 원격 측정](https://beta.apple.com/privacy)이 포함될 수 있습니다. 따라서 일반적으로 베타 소프트웨어는 피할 것을 권장합니다.

</div>

#### 서명된 시스템 볼륨 { #signed-system-volume }

macOS의 시스템 구성 요소는 읽기 전용 [서명된 시스템 볼륨](https://support.apple.com/guide/security/signed-system-volume-security-secd698747c9/web)으로 보호되므로, 여러분이나 멀웨어 모두 중요한 시스템 파일을 변경할 수 없습니다.

시스템 볼륨은 실행 중에 검증되며, 애플의 유효한 암호화 서명이 없는 데이터는 거부됩니다.

#### 시스템 무결성 보호 { #system-integrity-protection }

macOS는 재정의할 수 없는 특정 보안 제한을 설정합니다. 이를 [강제적 접근 제어](https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/1/web/1)라고 하며, macOS의 샌드박스, 자녀 보호 기능, [시스템 무결성 보호](https://support.apple.com/en-us/102149)의 기반이 됩니다.

시스템 무결성 보호는 중요한 파일 위치를 읽기 전용으로 만들어 악성 코드에 의한 수정을 막습니다. 이는 커널이 메모리 내에서 수정되지 않도록 하는 하드웨어 기반 커널 무결성 보호에 더해 적용됩니다.

#### 애플리케이션 보안 { #application-security }

##### 앱 샌드박스 { #app-sandbox }

macOS에서 앱의 샌드박스 적용 여부는 개발자가 앱에 서명할 때 결정합니다. [앱 샌드박스](https://developer.apple.com/documentation/xcode/configuring-the-macos-app-sandbox)는 앱이 악용될 경우 악의적인 행위자가 접근할 수 있는 범위를 제한하여, 실행하는 앱의 취약점으로부터 보호합니다. 앱 샌드박스*만으로는* 악의적인 개발자의 [:material-package-variant-closed-remove: 공급망 공격](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}을 막을 수 없습니다. 이를 위해서는 [앱 스토어](https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/1/web/1#:~:text=All%20apps%20from%20the%20App%20Store%20are%20sandboxed%20to%20restrict%20access%20to%20data%20stored%20by%20other%20apps.)처럼 개발자가 아닌 다른 주체가 샌드박싱을 강제해야 합니다.

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

공식 앱 스토어 외부에서 다운로드한 소프트웨어는 샌드박스 적용이 필수가 아닙니다. 위협 모델에서 [:material-bug-outline: 수동적 공격](../basics/common-threats.md#security-and-privacy){ .pg-orange } 방어를 우선시한다면, 앱 스토어 외부에서 다운로드한 소프트웨어가 샌드박스 처리되어 있는지 확인해 볼 수 있습니다. 샌드박스 적용 여부는 개발자가 *직접 선택*하기 때문입니다.

</div>

앱이 앱 샌드박스를 사용하는지 확인하는 방법은 몇 가지가 있습니다:

[활성 상태 보기](https://developer.apple.com/documentation/security/protecting-user-data-with-app-sandbox#Verify-that-your-app-uses-App-Sandbox)를 사용하여 이미 실행 중인 앱이 샌드박스 처리되어 있는지 확인할 수 있습니다.

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

앱의 프로세스 하나가 샌드박스 처리되어 있다고 해서 모든 프로세스가 그런 것은 아닙니다.

</div>

또는 터미널에서 다음 명령을 실행하여 앱을 실행하기 전에 확인할 수 있습니다:

``` zsh
codesign -dvvv --entitlements - <앱 경로>
```

앱이 샌드박스 처리되어 있다면 다음과 같은 출력이 표시됩니다:

``` zsh
    [Key] com.apple.security.app-sandbox
    [Value]
        [Bool] true
```

실행하려는 앱이 샌드박스 처리되어 있지 않다면 가상 머신이나 별도의 기기 같은 [구획화](../basics/common-threats.md#security-and-privacy) 방법을 사용하거나, 샌드박스 처리된 비슷한 앱을 사용하거나, 샌드박스 처리되지 않은 앱을 아예 사용하지 않을 수 있습니다.

##### 강화된 런타임 { #hardened-runtime }

[강화된 런타임](https://developer.apple.com/documentation/security/hardened_runtime)은 특정 종류의 익스플로잇을 막는 앱용 추가 보호 기능입니다. JIT 같은 특정 기능을 비활성화하여 익스플로잇에 대한 앱의 보안을 향상합니다.

다음 명령으로 앱이 강화된 런타임을 사용하는지 확인할 수 있습니다:

``` zsh
codesign -dv <앱 경로>
```

강화된 런타임이 활성화되어 있다면 `flags=0x10000(runtime)`이 표시됩니다. `runtime` 출력은 강화된 런타임이 활성화되어 있다는 뜻입니다. 다른 플래그가 있을 수도 있지만, 여기서 확인해야 할 것은 runtime 플래그입니다.

활성 상태 보기에서 "제한됨" 열을 활성화할 수 있는데, 이는 프로그램이 macOS의 [동적 링커](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html)를 통해 코드를 주입하는 것을 막는 플래그입니다. 이상적으로는 "예"로 표시되어야 합니다.

##### 바이러스 백신 { #antivirus }

macOS에는 두 가지 형태의 [멀웨어 방어](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/1/web/1) 기능이 내장되어 있습니다:

1. 처음부터 멀웨어가 실행되지 않도록 하는 보호는 앱 스토어 앱의 경우 앱 스토어 심사 과정을 통해, 그 외의 경우 *공증*(*게이트키퍼*의 일부)을 통해 제공됩니다. 공증은 서드파티 앱이 실행되기 전에 애플이 알려진 멀웨어를 검사하는 과정입니다. 앱은 개발자가 애플로부터 받은 키로 서명해야 합니다. 이를 통해 실제 개발자가 만든 소프트웨어를 실행하고 있음을 보장합니다. 또한 공증을 받으려면 개발자가 앱에 강화된 런타임을 활성화해야 하며, 이를 통해 익스플로잇 방법이 제한됩니다.
2. 기타 멀웨어에 대한 보호와 시스템에 이미 있는 멀웨어의 제거는 macOS에 내장된 보다 전통적인 백신 소프트웨어인 *XProtect*가 담당합니다.

서드파티 백신 소프트웨어는 설치하지 않을 것을 권장합니다. 서드파티 앱에 대한 애플의 제한 때문에 어차피 제대로 작동하는 데 필요한 시스템 수준 접근 권한을 갖지 못하는 경우가 많고, 이들이 요구하는 높은 수준의 접근 권한을 부여하면 오히려 컴퓨터의 보안과 프라이버시에 더 큰 위험이 되는 경우가 많기 때문입니다.

##### 백업 { #backups }

macOS에는 [타임 머신](https://support.apple.com/HT201250)이라는 자동 백업 소프트웨어가 내장되어 있어, 파일이 손상되거나 삭제될 경우를 대비해 외장 드라이브나 네트워크 드라이브에 [암호화된 백업](https://support.apple.com/guide/mac-help/keep-your-time-machine-backup-disk-secure-mh21241/mac)을 만들 수 있습니다.

### 하드웨어 보안 { #hardware-security }

최신 보안 부팅, 하드웨어 수준의 익스플로잇 완화, OS 무결성 검사, 파일 기반 암호화 등 macOS의 많은 최신 보안 기능은 애플 실리콘에 의존하며, 애플의 최신 하드웨어가 항상 [최고의 보안](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1)을 제공합니다. 구형 인텔 기반 맥 컴퓨터나 해킨토시가 아닌 애플 실리콘 사용만 권장합니다.

이러한 최신 보안 기능 중 일부는 애플 T2 보안 칩이 탑재된 구형 인텔 기반 맥 컴퓨터에서도 사용할 수 있지만, 이 칩은 보안을 침해할 수 있는 *checkm8* 익스플로잇에 취약합니다.

키보드 같은 블루투스 액세서리를 사용한다면 macOS가 펌웨어를 [자동으로 업데이트](https://support.apple.com/en-us/120303#:~:text=Firmware%20updates%20are%20automatically%20delivered%20in%20the%20background%20while%20the%20Magic%20Keyboard%20is%20actively%20paired%20to%20a%20device%20running%20macOS%2C%20iOS%2C%20iPadOS%2C%20or%20tvOS.)해 주는 애플 정품을 사용할 것을 권장합니다. 서드파티 액세서리를 사용해도 괜찮지만, 정기적으로 펌웨어 업데이트를 설치하는 것을 잊지 마세요.

애플의 SoC는 보안 기능을 기능이 제한된 전용 하드웨어에 맡김으로써 [공격 표면을 최소화](https://support.apple.com/en-vn/guide/security/secf020d1074/web#:~:text=Security%2Dfocused%20hardware%20follows%20the%20principle%20of%20supporting%20limited%20and%20discretely%20defined%20functions%20to%20minimize%20attack%20surface.)하는 데 중점을 둡니다.

#### 부트 ROM { #boot-rom }

macOS는 부팅 시 애플의 공식 소프트웨어만 실행되도록 허용하여 멀웨어의 지속성을 막는데, 이를 [보안 부팅](https://support.apple.com/en-vn/guide/security/secac71d5623/1/web/1)이라고 합니다. 맥 컴퓨터는 [칩 제조 과정에서 기록되는](https://support.apple.com/en-vn/guide/security/secf020d1074/1/web/1#:~:text=which%20is%20laid%20down%20during%20Apple%20SoC%20fabrication) SoC의 소량 읽기 전용 메모리인 [부트 ROM](https://support.apple.com/en-vn/guide/security/aside/sec5240db956/1/web/1)으로 이를 검증합니다.

부트 ROM은 하드웨어 신뢰 루트를 구성합니다. 부트 ROM은 변경할 수 없으므로 멀웨어가 부팅 과정을 변조할 수 없습니다. 맥이 부팅될 때 가장 먼저 실행되는 것이 부트 ROM이며, 신뢰 체인의 첫 번째 고리를 형성합니다.

맥 컴퓨터는 *완전한 보안*, *낮은 보안*, *허용 보안*의 [세 가지 보안 모드](https://support.apple.com/guide/deployment/startup-security-dep5810e849c/web#dep32fb404e1)로 부팅하도록 구성할 수 있으며, 기본 설정은 완전한 보안입니다. 이상적으로는 완전한 보안 모드를 사용하고, 보안 모드를 낮추도록 강제하는 **[커널 확장 프로그램](https://support.apple.com/guide/deployment/system-extensions-in-macos-depa5fb8376f/web#dep51e097f45)** 같은 것은 피해야 합니다. 완전한 보안 모드를 사용하고 있는지 [확인](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac)하세요.

#### Secure Enclave

**[Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/web)**는 애플 실리콘 기기에 내장된 보안 칩으로, 저장 데이터용 암호화 키와 Face ID 및 Touch ID 데이터를 생성하고 저장하는 역할을 합니다. 자체적인 [별도의 부트 ROM](https://support.apple.com/en-vn/guide/security/sec59b0b31ff/web#sec43006c49f)을 가지고 있습니다.

Secure Enclave는 기기의 보안 허브라고 생각할 수 있습니다. AES 암호화 엔진과 암호화 키를 안전하게 저장하는 메커니즘을 갖추고 있으며, 시스템의 나머지 부분과 분리되어 있어 메인 프로세서가 침해되더라도 안전하게 유지됩니다.

#### Touch ID

애플의 Touch ID 기능을 사용하면 생체 인식으로 기기의 잠금을 안전하게 해제할 수 있습니다.

생체 데이터는 [기기 밖으로 절대 나가지 않으며](https://www.apple.com/legal/privacy/data/en/touch-id/#:~:text=Touch%C2%A0ID%20data%20does%20not%20leave%20your%20device%2C%20and%20is%20never%20backed%20up%20to%20iCloud%20or%20anywhere%20else.), Secure Enclave에만 저장됩니다.

#### 하드웨어 마이크 연결 해제 { #hardware-microphone-disconnect }

애플 실리콘이나 T2 칩이 탑재된 모든 노트북은 덮개를 닫을 때마다 내장 마이크를 [하드웨어적으로 연결 해제](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web)합니다. 즉, 운영 체제가 침해되더라도 공격자가 맥의 마이크로 소리를 엿들을 방법이 없습니다.

카메라는 덮개를 닫으면 어차피 시야가 가려지므로 하드웨어 연결 해제 기능이 없다는 점에 유의하세요.

#### 안전한 카메라 표시등 { #secure-camera-indicator }

맥의 내장 카메라는 카메라 표시등이 [함께 켜지지 않고는](https://support.apple.com/en-us/102177#:~:text=The%20camera%20is%20engineered%20so%20that%20it%20can’t%20activate%20without%20the%20camera%20indicator%20light%20also%20turning%20on.%20This%20is%20how%20you%20can%20tell%20if%20your%20camera%20is%20on.) 카메라가 켜질 수 없도록 설계되어 있습니다.

#### 주변 프로세서 보안 { #peripheral-processor-security }

컴퓨터에는 메인 CPU 외에도 네트워킹, 그래픽, 전원 관리 등을 처리하는 [내장 프로세서](https://support.apple.com/en-vn/guide/security/seca500d4f2b/1/web/1)가 있습니다. 이러한 프로세서는 보안이 불충분하여 침해될 수 있으므로, 애플은 자사 하드웨어에서 이러한 프로세서의 필요성을 최소화하려고 노력합니다.

이러한 프로세서를 사용해야 할 때 애플은 공급업체와 협력하여 해당 프로세서가 다음을 충족하도록 합니다:

- 시동 시 메인 CPU로부터 검증된 펌웨어를 실행
- 자체 보안 부팅 체인 보유
- 최소 암호화 기준 준수
- 알려진 결함 펌웨어가 제대로 폐기되도록 보장
- 디버그 인터페이스 비활성화
- 애플의 암호화 키로 서명

#### 직접 메모리 접근 보호 { #direct-memory-access-protections }

애플 실리콘은 [직접 메모리 접근](https://support.apple.com/guide/security/direct-memory-access-protections-seca4960c2b5/1/web/1)이 필요한 각 구성 요소를 분리합니다. 예를 들어 썬더볼트 포트는 커널용으로 지정된 메모리에 접근할 수 없습니다.

#### 터미널 보안 키보드 입력 { #terminal-secure-keyboard-entry }

[보안 키보드 입력](https://support.apple.com/guide/terminal/use-secure-keyboard-entry-trml109/mac)을 활성화하면 다른 앱이 터미널에서 입력하는 내용을 감지하지 못하게 할 수 있습니다.
