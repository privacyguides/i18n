---
meta_title: "How to Create Internet Accounts Privately - Privacy Guides"
title: "계정 생성"
icon: 'material/account-plus'
description: Creating accounts online is practically an internet necessity, take these steps to make sure you stay private.
---

사람들은 별다른 생각 없이 서비스에 가입할 때가 많습니다. 남들이 이야기하는 새로 나온 드라마를 상영하는 스트리밍 서비스에 가입하기도 하고, 자주 가는 음식 프랜차이즈에서 할인 혜택을 받으려고 가입하기도 합니다. 어떤 경우든, 현재 및 향후 여러분의 데이터에 미치는 영향을 고려해야 합니다.

새로 사용하는 모든 서비스에는 위험성이 뒤따릅니다. 어딘가에 정보를 제공할 때에는 데이터 유출, 제3자에게 고객 정보 공개, 불량 직원의 데이터 접근 등 다양한 가능성을 고려해야 합니다. 그러니 믿을만한, 즉 가장 성숙하고 실전에서 검증된 서비스 이외에는 여러분의 소중한 데이터를 저장하지 않을 것을 권장드립니다. 믿을 만한 서비스는 일반적으로 E2EE를 제공하고 암호화 감사를 거친 서비스를 의미합니다. 보안 감사는 미숙한 개발자에 의해 생겼을지도 모르는 확연한 보안 문제가 없게 제품이 설계되었음을 보장합니다.

일부 서비스의 경우, 계정 삭제가 쉽지 않을 수 있습니다. 계정 관련 데이터를 [덮어씌우는 것](account-deletion.md#overwriting-account-information)은 가능한 경우도 있지만, 서비스에서 계정 데이터의 변경 기록을 보관하는 경우도 있습니다.

## Terms of Service & Privacy Policy

'이용 약관'은 여러분이 어떤 서비스를 이용할 때 동의해야 하는 규칙입니다. With larger services these rules are often enforced by automated systems. Sometimes these automated systems can make mistakes. 예를 들어, 일부 서비스에서는 VPN/VoIP 번호를 사용한다는 이유로 계정이 차단되거나 잠길 수 있습니다. Appealing such bans is often difficult, and involves an automated process too, which isn't always successful. This would be one of the reasons why we wouldn't suggest using Gmail for email as an example. Email is crucial for access to other services you might have signed up for.

The Privacy Policy is how the service says they will use your data and it is worth reading so that you understand how your data will be used. A company or organization might not be legally obligated to follow everything contained in the policy (it depends on the jurisdiction). We would recommend having some idea what your local laws are and what they permit a provider to collect.

We recommend looking for particular terms such as "data collection", "data analysis", "cookies", "ads" or "3rd-party" services. Sometimes you will be able to opt-out from data collection or from sharing your data, but it is best to choose a service that respects your privacy from the start.

Keep in mind you're also placing your trust in the company or organization and that they will comply with their own privacy policy.

## Authentication methods

There are usually multiple ways to sign up for an account, each with their own benefits and drawbacks.

### Email and password

The most common way to create a new account is by an email address and password. When using this method, you should use a password manager and follow [best practices](passwords-overview.md) regarding passwords.

!!! tip "도움말"

    You can use your password manager to organize other authentication methods too! Just add the new entry and fill the appropriate fields, you can add notes for things like security questions or a backup key.

You will be responsible for managing your login credentials. For added security, you can set up [MFA](multi-factor-authentication.md) on your accounts.

[권장 비밀번호 관리자](../passwords.md ""){.md-button}

#### 이메일 별칭

If you don't want to give your real email address to a service, you have the option to use an alias. We described them in more detail on our email services recommendation page. Essentially, alias services allow you to generate new email addresses that forward all emails to your main address. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign up process. Those can be filtered automatically based on the alias they are sent to.

Should a service get hacked, you might start receiving phishing or spam emails to the address you used to sign up. Using unique aliases for each service can assist in identifying exactly what service was hacked.

[권장 이메일 별칭 서비스](../email.md#email-aliasing-services ""){.md-button}

### Single sign-on

!!! note

    We are discussing Single sign-on for personal use, not enterprise users.

Single sign-on (SSO) is an authentication method that allows you to register for a service without sharing much information, if any. Whenever you see something along the lines of "Sign-in with *provider name*" on a registration form it's SSO.

When you choose single sign-on in a website, it will prompt your SSO provider login page and after that your account will be connected. Your password won't be shared but some basic information will (you can review it during the login request). This process is needed every time you want to log in to the same account.

주요 장점은 다음과 같습니다:

- **보안**: 웹사이트에 여러분의 자격 증명이 저장되지 않으므로, [데이터 유출](https://en.wikipedia.org/wiki/Data_breach) 위험성이 없습니다.
- **사용 편의성**: 하나의 로그인으로 여러 계정을 관리할 수 있습니다.

단점은 다음과 같습니다:

- **프라이버시**: SSO 제공 업체는 사용자가 어떤 서비스를 사용하는지 알 수 있습니다.
- **중앙 집중화**: SSO 계정이 손상되거나 로그인할 수 없는 경우, 해당 계정에 연결된 계정도 전부 영향을 받습니다.

SSO can be especially useful in those situations where you could benefit from deeper integration between services. For example, one of those services may offer SSO for the others. Our recommendation is to limit SSO to only where you need it and protect the main account with [MFA](multi-factor-authentication.md).

All services that use SSO will be as secure as your SSO account. For example, if you want to secure an account with a hardware key but that service doesn't support hardware keys, you can secure your SSO account with a hardware key and now you essentially have hardware MFA on all your accounts. It is worth noting though that weak authentication on your SSO account means that any account tied to that login will also be weak.

### 전화번호

전화번호 입력이 필수적인 서비스를 가입하는 것은 피하는 것이 좋습니다. A phone number can identity you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

You should avoid giving out your real phone number if you can. Some services will allow the use of VOIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

In many cases you will need to provide a number that you can receive SMS or calls from, particularly when shopping internationally, in case there is a problem with your order at border screening. It's common for services to use your number as a verification method; don't let yourself get locked out of an important account because you wanted to be clever and give a fake number!

### Username and password

Some services allow you to register without using an email address and only require you to set a username and password. These services may provide increased anonymity when combined with a VPN or Tor. Keep in mind that for these accounts there will most likely be **no way to recover your account** in the event you forget your username or password.
