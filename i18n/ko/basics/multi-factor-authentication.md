---
title: "다중 인증"
icon: 'material/two-factor-authentication'
description: MFA is a critical security mechanism for securing your online accounts, but some methods are stronger than others.
---

**다중 인증**(**MFA**, Multi-Factor Authentication)은 사용자 이름(혹은 이메일)과 비밀번호 입력 외에도 추가 단계를 거치는 보안 방식입니다. 가장 흔히 볼 수 있는 예시로는 문자 메시지나 앱으로 받는 시간 제한 인증 코드가 대표적입니다.

보통, 해커/공격자가 여러분의 비밀번호를 알아내는 순간 해당 계정은 뚫립니다. 하지만 해당 계정이 MFA를 사용하고 있다면, 해커는 (여러분의 *머릿속에* 있는) 비밀번호 뿐만 아니라 (여러분의 *손에* 들려있는 휴대폰 등) 기기 또한 탈취해야 합니다.

MFA 방식마다 보안성은 각각 다르지만, 기본적으로는 '공격자가 여러분이 사용하는 MFA 방식에 접근하기 어려운' 방식일수록 더 뛰어나다고 할 수 있습니다. MFA 종류로는(취약한 방식부터 갈수록 강력한 순으로) SMS, 이메일, 앱 푸시 알림, TOTP, Yubico OTP, FIDO 등이 있습니다.

## MFA 방식 비교

### SMS/이메일 MFA

SMS나 이메일로 OTP 코드를 받는 방식은 MFA를 통한 계정 보호 방법 중 취약한 편에 속합니다. 여러분의 기기에 직접 물리적으로 접근하지 않고도 [전화번호를 탈취](https://en.wikipedia.org/wiki/SIM_swap_scam)하거나 이메일 계정에 접근할 수 있는 방법은 다양하기 때문에, MFA의 장점인 '내 *손에 들려있으니* 남이 몰래 빼앗을 수 없다'라는 점이 퇴색됩니다. 공격자가 여러분의 이메일에 접근 가능한 경우, 해당 접근 권한을 이용해 비밀번호를 재설정 후 인증 코드를 받고 계정의 전체 접근 권한을 얻을 수 있습니다.

### 푸시 알림

푸시 알림 MFA는 계정의 새로운 로그인 확인을 요청하는 메시지가 휴대폰 앱으로 전송되는 방식입니다. 푸시 알림 MFA 방식은 SMS/이메일보다 훨씬 뛰어납니다. 공격자가 이미 해당 계정에 로그인된 기기를 가지고 있지 않은 이상, 여러분의 기기 중 하나를 손상시키지 않고서는 푸시 알림을 받을 수 없기 때문입니다.

하지만 사람은 누구나 실수를 할 수 있고, 실수로 로그인을 승인할 위험성이 존재합니다. 일반적으로 푸시 알림 로그인 인증은 여러분의 *모든* 기기로 한꺼번에 전송되므로, 사용하는 기기가 많아질수록 MFA 코드의 철저한 관리는 어려워집니다.

푸시 알림 MFA의 보안성은 앱의 품질, 서버 구성 요소, 앱 개발자의 신뢰도에 따라 달라집니다. Installing an app may also require you to accept invasive privileges that grant access to other data on your device. An individual app also requires that you have a specific app for each service which may not require a password to open, unlike a good TOTP generator app.

### TOTP(시간 기반 일회용 비밀번호)

TOTP(시간 기반 일회용 비밀번호, Time-based One-time Password)는 널리 쓰이는 MFA 방식 중 하나입니다. 일반적으로 TOTP 설정은 사용하고자 하는 서비스에서 [QR 코드](https://ko.wikipedia.org/wiki/QR_%EC%BD%94%EB%93%9C)를 스캔하여 '[공유 비밀(Shared Secret)](https://en.wikipedia.org/wiki/Shared_secret)'을 설정하는 방식으로 이루어집니다. 공유 비밀은 인증 앱의 데이터 내부에서 보호되며, 간혹 비밀번호로 보호되는 경우도 있습니다.

The time-limited code is then derived from the shared secret and the current time. As the code is only valid for a short time, without access to the shared secret, an adversary cannot generate new codes.

TOTP를 지원하는 하드웨어 보안 키를 가지고 계실 경우, '공유 비밀'을 해당 하드웨어 보안 키에 저장하실 것을 권장드립니다. YubiKey 등의 하드웨어 보안 키는 '공유 비밀'을 추출하거나 복사하는 것을 어렵게 만들기 위해서 개발되었습니다. 또한, TOTP 앱이 설치된 휴대폰과 달리 YubiKey는 인터넷에 연결되어 있지 않기 때문에 더 안전합니다.

[WebAuthn](#fido-fast-identity-online)과 달리, TOTP는 [피싱](https://ko.wikipedia.org/wiki/%ED%94%BC%EC%8B%B1) 혹은 재사용 공격으로부터 보호하는 기능을 제공하지 않습니다. 만약 공격자가 여러분의 유효 코드를 탈취해낸다면, 공격자는 해당 코드가 만료될 때까지(보통 60초) 몇 번이고 사용할 수 있습니다.

공격자는 어떤 서비스의 공식 웹사이트를 흉내낸 웹사이트를 만들어서 여러분이 사용자 이름, 비밀번호, 현재 TOTP 코드를 제출하도록 유도할 수도 있습니다. 만약 여러분이 이를 제출할 경우, 공격자는 해당 자격 증명 내용을 이용해 실제 서비스에 로그인하여 계정을 탈취할 수 있습니다.

TOTP는 완벽하지는 않습니다. 하지만 대부분의 사람들에게 있어서 충분히 안전하며, [하드웨어 보안 키](../multi-factor-authentication.md#hardware-security-keys)가 지원되지 않는 경우에는 [인증 앱](../multi-factor-authentication.md#authenticator-apps)도 여전히 훌륭한 선택지입니다.

### 하드웨어 보안 키

Yubikey는 변조 방지 Solid-State 칩에 데이터를 저장합니다. 변조 방지 칩은 포렌식 연구실을 동원하고 고가의 공정을 거치지 않는 이상 비파괴적 접근이 [불가능합니다](https://security.stackexchange.com/a/245772).

하드웨어 보안 키는 보통 여러 기능을 가지고 있으며 다양한 인증 방식을 제공합니다. Below are the most common ones.

#### Yubico OTP

Yubico OTP는 일반적으로 하드웨어 보안 키로 구현되는 인증 프로토콜입니다. Yubico OTP를 사용하면 공개 ID, 개인 ID, 비밀 키가 생성되고 Yubico OTP 서버로 업로드됩니다.

웹사이트에 로그인하려면 보안 키를 물리적으로 터치하기만 하면 됩니다. 보안 키는 키보드 에뮬레이터처럼 작동하여 비밀번호 필드에 일회용 비밀번호를 출력합니다.

서비스는 유효성 검사를 위해 Yubico OTP 서버로 일회용 비밀번호를 전달합니다. 카운터는 키, Yubico 유효성 검사 서버 양측 모두에서 증가합니다. OTP는 한 번만 사용할 수 있으며, 인증에 성공하면 카운터가 증가함으로써 OTP 재사용을 방지합니다. Yubico에서 [ 자세히 설명한 문서](https://developers.yubico.com/OTP/OTPs_Explained.html)를 참고하세요.

<figure markdown>
  ![Yubico OTP](../assets/img/multi-factor-authentication/yubico-otp.png)
</figure>

Yubico OTP는 TOTP와 비교했을 때 몇 가지 장단점이 있습니다.

Yubico 유효성 검사 서버는 클라우드 기반 서비스입니다. 따라서 사용자는 그저 Yubico 측에서 데이터를 안전하게 저장하고, 사용자를 프로파일링하지 않을 것이라 믿고 있어야 합니다. 또한, Yubico OTP와 연결된 공개 ID는 모든 웹사이트에서 재사용되므로 제3자가 여러분을 프로파일링하는 수단으로 쓰일 수 있습니다. TOTP와 마찬가지로, Yubico OTP에서 피싱 방지 기능은 제공하지 않습니다.

여러분의 위협 모델에 따라, '웹사이트마다 서로 다른 신원을 사용하고자 하는 경우'에는 여러 사이트에서 동일한 하드웨어 보안 키로 Yubico OTP를 사용해서는 **안 됩니다**. 각 보안 키는 고유한 공개 ID를 갖기 때문입니다.

#### FIDO(Fast IDentity Online)

[FIDO](https://ko.wikipedia.org/wiki/FIDO_%EC%96%BC%EB%9D%BC%EC%9D%B4%EC%96%B8%EC%8A%A4)에는 여러 표준이 포함되어 있습니다. U2F가 먼저 추가되었고, 이후에는 [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) 웹 표준을 포함하는 [FIDO2](https://en.wikipedia.org/wiki/FIDO2_Project)가 추가되었습니다.

U2F and FIDO2 refer to the [Client to Authenticator Protocol](https://en.wikipedia.org/wiki/Client_to_Authenticator_Protocol), which is the protocol between the security key and the computer, such as a laptop or phone. It complements WebAuthn which is the component used to authenticate with the website (the "Relying Party") you're trying to log in on.

WebAuthn is the most secure and private form of second factor authentication. While the authentication experience is similar to Yubico OTP, the key does not print out a one-time password and validate with a third-party server. Instead, it uses [public key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) for authentication.

<figure markdown>
  ![FIDO](../assets/img/multi-factor-authentication/fido.png)
</figure>

When you create an account, the public key is sent to the service, then when you log in, the service will require you to "sign" some data with your private key. The benefit of this is that no password data is ever stored by the service, so there is nothing for an adversary to steal.

This presentation discusses the history of password authentication, the pitfalls (such as password reuse), and discussion of FIDO2 and [WebAuthn](https://webauthn.guide) standards.

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/aMo4ZlWznao?local=true" title="How FIDO2 and WebAuthn Stop Account Takeovers" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

FIDO2 and WebAuthn have superior security and privacy properties when compared to any MFA methods.

Typically for web services it is used with WebAuthn which is a part of the [W3C recommendations](https://en.wikipedia.org/wiki/World_Wide_Web_Consortium#W3C_recommendation_(REC)). It uses public key authentication and is more secure than shared secrets used in Yubico OTP and TOTP methods, as it includes the origin name (usually, the domain name) during authentication. Attestation is provided to protect you from phishing attacks, as it helps you to determine that you are using the authentic service and not a fake copy.

Unlike Yubico OTP, WebAuthn does not use any public ID, so the key is **not** identifiable across different websites. It also does not use any third-party cloud server for authentication. All communication is completed between the key and the website you are logging into. FIDO also uses a counter which is incremented upon use in order to prevent session reuse and cloned keys.

If a website or service supports WebAuthn for the authentication, it is highly recommended that you use it over any other form of MFA.

## General Recommendations

We have these general recommendations:

### 어떤 MFA 방식을 사용해야 하나요?

When configuring your MFA method, keep in mind that it is only as secure as your weakest authentication method you use. This means it is important that you only use the best MFA method available. 예를 들어, TOTP를 이미 사용하고 있다면 SMS/이메일 MFA를 비활성화해야 합니다. FIDO/WebAuthn을 이미 사용 중인 경우라면 해당 계정에서 Yubico OTP/TOTP를 사용해서는 안 됩니다.

### 백업

You should always have backups for your MFA method. 하드웨어 보안 키는 세월이 지나며 분실, 도난, 혹은 단순 고장이 발생할 수 있습니다. 계정 접근 권한이 동일한 하드웨어 보안 키를 (예비용을 포함해) 두 개씩 마련해야 합니다.

TOTP 인증 앱을 사용하는 경우, 복구 키 혹은 앱 자체를 백업하거나, 다른 휴대폰에 설치한 앱이나 (VeraCrypt 등을 이용한) 별도 암호화 저장소에 '공유 비밀 키(Shared Secret Key)'를 복사해둬야 합니다.

### 초기 설정

보안 키를 구매했다면, 기본 자격 증명 변경, 보안 키 비밀번호 보호 설정, (지원하는 경우) 터치식 인증 확인 활성화를 진행해야 합니다. Products such as the YubiKey have multiple interfaces with separate credentials for each one of them, so you should go over each interface and set up protection as well.

### Email and SMS

If you have to use email for MFA, make sure that the email account itself is secured with a proper MFA method.

If you use SMS MFA, use a carrier who will not switch your phone number to a new SIM card without account access, or use a dedicated VoIP number from a provider with similar security to avoid a [SIM swap attack](https://en.wikipedia.org/wiki/SIM_swap_scam).

[MFA tools we recommend](../multi-factor-authentication.md ""){.md-button}

## More Places to Set Up MFA

Beyond just securing your website logins, multi-factor authentication can be used to secure your local logins, SSH keys or even password databases as well.

### Windows

Yubico has a dedicated [Credential Provider](https://docs.microsoft.com/en-us/windows/win32/secauthn/credential-providers-in-windows) that adds Challenge-Response authentication for the username + password login flow for local Windows accounts. If you have a YubiKey with Challenge-Response authentication support, take a look at the [Yubico Login for Windows Configuration Guide](https://support.yubico.com/hc/en-us/articles/360013708460-Yubico-Login-for-Windows-Configuration-Guide), which will allow you to set up MFA on your Windows computer.

### macOS

macOS has [native support](https://support.apple.com/guide/deployment/intro-to-smart-card-integration-depd0b888248/web) for authentication with smart cards (PIV). If you have a smartcard or a hardware security key that supports the PIV interface such as the YubiKey, we recommend that you follow your smartcard/hardware security vendor's documentation and set up second factor authentication for your macOS computer.

Yubico have a guide [Using Your YubiKey as a Smart Card in macOS](https://support.yubico.com/hc/en-us/articles/360016649059) which can help you set up your YubiKey on macOS.

After your smartcard/security key is set up, we recommend running this command in the Terminal:

```text
sudo defaults write /Library/Preferences/com.apple.loginwindow DisableFDEAutoLogin -bool YES
```

The command will prevent an adversary from bypassing MFA when the computer boots.

### Linux

!!! warning "경고"

    If the hostname of your system changes (such as due to DHCP), you would be unable to login. It is vital that you set up a proper hostname for your computer before following this guide.

The `pam_u2f` module on Linux can provide two-factor authentication for logging in on most popular Linux distributions. If you have a hardware security key that supports U2F, you can set up MFA authentication for your login. Yubico has a guide [Ubuntu Linux Login Guide - U2F](https://support.yubico.com/hc/en-us/articles/360016649099-Ubuntu-Linux-Login-Guide-U2F) which should work on any distribution. The package manager commands—such as `apt-get`—and package names may however differ. This guide does **not** apply to Qubes OS.

### Qubes OS

Qubes OS has support for Challenge-Response authentication with YubiKeys. If you have a YubiKey with Challenge-Response authentication support, take a look at the Qubes OS [YubiKey documentation](https://www.qubes-os.org/doc/yubikey/) if you want to set up MFA on Qubes OS.

### SSH

#### 하드웨어 보안 키

SSH MFA could be set up using multiple different authentication methods that are popular with hardware security keys. We recommend that you check out Yubico's [documentation](https://developers.yubico.com/SSH/) on how to set this up.

#### TOTP(시간 기반 일회용 비밀번호)

SSH MFA can also be set up using TOTP. DigitalOcean has provided a tutorial [How To Set Up Multi-Factor Authentication for SSH on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-set-up-multi-factor-authentication-for-ssh-on-ubuntu-20-04). Most things should be the same regardless of distribution, however the package manager commands—such as `apt-get`—and package names may differ.

### KeePass (KeePassXC)

KeePass and KeePassXC databases can be secured using Challenge-Response or HOTP as a second-factor authentication. Yubico has provided a document for KeePass [Using Your YubiKey with KeePass](https://support.yubico.com/hc/en-us/articles/360013779759-Using-Your-YubiKey-with-KeePass) and there is also one on the [KeePassXC](https://keepassxc.org/docs/#faq-yubikey-2fa) website.
