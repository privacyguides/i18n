---
meta_title: "How to Create Internet Accounts Privately - Privacy Guides"
title: "Account Creation"
icon: 'material/account-plus'
description: Creating accounts online is practically an internet necessity, take these steps to make sure you stay private.
---

사람들은 별다른 생각 없이 서비스에 가입할 때가 많습니다. 남들이 이야기하는 새로 나온 드라마를 상영하는 스트리밍 서비스에 가입하기도 하고, 자주 가는 음식 프랜차이즈에서 할인 혜택을 받으려고 가입하기도 합니다. 어떤 경우든, 현재 및 향후 여러분의 데이터에 미치는 영향을 고려해야 합니다.

새로 사용하는 모든 서비스에는 위험성이 뒤따릅니다. 어딘가에 정보를 제공할 때에는 데이터 유출, 제3자에게 고객 정보 공개, 불량 직원의 데이터 접근 등 다양한 가능성을 고려해야 합니다. 그러니 믿을만한, 즉 가장 성숙하고 실전에서 검증된 서비스 이외에는 여러분의 소중한 데이터를 저장하지 않을 것을 권장드립니다. 믿을 만한 서비스는 일반적으로 E2EE를 제공하고 암호화 감사를 거친 서비스를 의미합니다. 보안 감사는 미숙한 개발자에 의해 생겼을지도 모르는 확연한 보안 문제가 없게 제품이 설계되었음을 보장합니다.

일부 서비스의 경우, 계정 삭제가 쉽지 않을 수 있습니다. 계정 관련 데이터를 [덮어씌우는 것](account-deletion.md#overwriting-account-information)은 가능한 경우도 있지만, 서비스에서 계정 데이터의 변경 기록을 보관하는 경우도 있습니다.

## 서비스 이용 약관 & 개인정보 보호 정책(프라이버시 정책)

'이용 약관'은 여러분이 어떤 서비스를 이용할 때 동의해야 하는 규칙입니다. 대규모 서비스에서는 이용 약관 규칙을 자동화된 시스템과 운용하는 경우가 많습니다. 그리고 자동화 시스템에서는 간혹 실수가 발생하기도 합니다. 예를 들어, 일부 서비스에서는 VPN/VoIP 번호를 사용한다는 이유로 계정이 차단되거나 잠길 수 있습니다. 이런 제한 조치에 대한 이의 제기는 어려운 경우가 많고 자동화된 과정을 거쳐야 하므로, 항상 성공적이진 않습니다. 이는 Privacy Guides에서 Gmail 이메일 서비스 사용을 권장드리지 않는 이유 중 하나이기도 합니다. 이메일은 여러분이 가입한 다른 서비스에 접근하기 위한 매우 중요한 역할을 맡고 있습니다.

개인정보 보호 정책은 서비스에서 여러분의 데이터를 어떻게 이용할지 명시한 것으로, 여러분은 자신의 데이터가 어떻게 쓰일지 이해하기 위해 읽어보는 것이 좋습니다. 회사/조직은 정책 내 모든 내용을 따르도록 법적으로 강제되지는 않을 수 있습니다(관할권에 따라 달라집니다). 제공 업체가 수집 가능한 데이터의 범위와 현지 법률을 어느 정도는 파악해 두는 것이 좋습니다.

살펴봐야 할 주요 용어는 '데이터 수집(Data Collection)', '데이터 분석(Data Analysis)', '쿠키(Cookies)', '광고(Ads)', '제3자/타사(3rd-Party)' 등이 있습니다. 데이터 수집/공유를 거부할 수 있는 경우도 있지만, 가장 좋은 방법은 처음부터 프라이버시를 존중하는 서비스를 선택하는 것입니다.

또한, 여러분은 해당 서비스 회사/조직이 개인정보 처리 방침을 올바르게 준수할 것이라고 믿고 있을 뿐임을 명심해야 합니다.

## 인증 방법

계정 가입 방법은 일반적으로 여러 가지가 있으며, 각각 장단점이 있습니다.

### 이메일 주소와 비밀번호

새로운 계정을 생성할 때는 이메일 주소와 비밀번호를 사용하는 것이 가장 일반적입니다. 이 경우, 비밀번호 관리자를 사용해야 하며 비밀번호 관련 [모범 사례](passwords-overview.md)를 따라야 합니다.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

다른 인증 방법도 비밀번호 관리자에서 관리할 수 있습니다! 새 항목을 추가하고 적절한 필드를 채우면 보안 질문, 백업 키 등 관련 메모를 추가할 수 있습니다.

</div>

로그인 자격 증명의 관리 책임은 자기 자신에게 있습니다. 보안을 강화하려면 계정에 [MFA](multi-factor-authentication.md)를 설정하세요.

[권장 비밀번호 관리자](../passwords.md ""){.md-button}

#### 이메일 별칭

실제 이메일 주소를 서비스에 노출하지 않고자 하는 경우 이메일 별칭을 사용할 수 있습니다. (이메일 별칭 관련 자세한 내용은 이메일 서비스 권장 목록 페이지를 참고하세요.) 이메일 별칭 서비스를 사용하면 주요 이메일 주소로 모든 이메일이 전달되는 새로운 이메일 주소를 만들 수 있습니다. 서비스 간 추적을 방지하고, 가입 과정에서 따라온 마케팅 이메일을 관리하는 데에 유용합니다. 어떤 별칭으로 보내졌는지에 따라 자동으로 분류되기 때문입니다.

서비스가 해킹당할 경우, 가입한 이메일 주소로 피싱/스팸 메일이 올 수 있습니다. 서비스마다 고유한 별칭을 사용하면 어떤 서비스가 해킹당했는지 식별 가능합니다.

[권장 이메일 별칭 서비스](../email.md#email-aliasing-services ""){.md-button}

### '~ (으)로 로그인' (OAuth)

OAuth는 가입하려는 서비스 제공 업체와 많은 정보를 공유하지 않고도, 다른 서비스에서 이미 사용 중이던 기존 계정을 이용해서 서비스에 가입할 수 있는 인증 프로토콜입니다. 가입 시에 '*제공 업체* (으)로 로그인' 문구로 표시되는 방식이 OAuth를 사용하는 것입니다.

Oauth 로그인을 선택할 경우, OAuth 제공 업체의 로그인 페이지를 거쳐 계정이 연결됩니다. 여러분의 비밀번호는 공유되지 않지만, 보통 일부 기본 정보(로그인 과정에서 검토 가능합니다)는 공유됩니다. 이 과정은 해당 계정에 로그인할 때마다 필요합니다.

주요 장점은 다음과 같습니다:

- **Security**: you don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials, because they are stored with the external OAuth provider, which when it comes to services like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **사용 편의성**: 하나의 로그인으로 여러 계정을 관리할 수 있습니다.

단점은 다음과 같습니다:

- **프라이버시**: OAuth 제공 업체는 사용자가 어떤 서비스를 사용하는지 알 수 있습니다.
- **Centralization**: if the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth can be especially useful in those situations where you could benefit from deeper integration between services. 되도록 OAuth는 필요한 경우에만 사용하고, 주요 계정은 [MFA](multi-factor-authentication.md)로 보호할 것을 권장드립니다.

All the services that use OAuth will be as secure as your underlying OAuth provider's account. 예를 들어, 하드웨어 키를 사용해 계정을 보호하고 싶은데 해당 서비스는 하드웨어 키를 지원하지 않는 경우, OAuth 계정을 하드웨어 키로 보호하면 결과적으로 모든 계정을 하드웨어 키로 보호하는 효과를 얻습니다. 하지만 동시에, OAuth 계정 인증이 취약할 경우에는 해당 계정에 연결된 모든 계정의 인증 또한 취약해진다는 점을 명심해야합니다.

There is an additional danger when using *Sign in with Google*, *Facebook*, or another service, which is that typically the OAuth process allows for *bidirectional* data sharing. For example, logging in to a forum with your Twitter account could grant that forum access to do things on your Twitter account such as post, read your messages, or access other personal data. OAuth providers will typically present you with a list of things you are granting the external service access to, and you should always ensure that you read through that list and don't inadvertently grant the external service access to anything it doesn't require.

Malicious applications, particularly on mobile devices where the application has access to the WebView session used for logging in to the OAuth provider, can also abuse this process by hijacking your session with the OAuth provider and gaining access to your OAuth account through those means. Using the *Sign in with* option with any provider should usually be considered a matter of convenience that you only use with services you trust to not be actively malicious.

### 전화번호

전화번호 입력이 필수적인 서비스를 가입하는 것은 피하는 것이 좋습니다. 전화번호를 이용하면 여러 서비스에서 사용자를 식별할 수 있으며, 서비스끼리 데이터를 공유하는 경우에는 사용자 추적 또한 간단해집니다. 특히, 어떤 서비스에서 데이터 유출이 발생하는 경우, 전화번호는 암호화되지 **않은** 채로 유출되는 경우가 많기 때문에 더욱 문제가 커집니다.

가능하다면, 실제 전화번호를 제공하지 않는 것이 좋습니다. VoIP 번호를 사용할 수 있는 일부 서비스도 있지만, 사기 탐지 시스템에 의해 계정이 잠기는 경우가 많기 때문에 중요한 계정에 VoIP 번호를 사용하는 것은 권장드리지 않습니다.

대부분의 경우, 문자나 전화를 실제로 받을 수 있는 번호를 제공해야 합니다. 대표적으로 해외 직구 시에는 세관에서 문제가 발생할 경우를 대비해야 합니다. 서비스에서는 전화번호가 인증 수단의 역할을 하는 것이 일반적이니, 교묘하게 가짜 번호를 입력했다가 중요 계정이 차단되는 일이 없도록 주의하세요!

### 사용자 이름과 비밀번호

일부 서비스는 이메일 주소도 사용하지 않고 사용자 이름과 비밀번호만으로 가입할 수 있습니다. 이러한 서비스는 VPN이나 Tor를 함께 사용하면 익명성이 더욱 강화됩니다. 단, 이런 계정은 사용자 이름이나 비밀번호를 잊어버리면 **계정을 복구할 방법이 없을** 가능성이 높습니다.
