---
title: "多要素認証"
icon: 'material/two-factor-authentication'
description: 多要素認証はオンラインアカウントを保護するためのセキュリティの仕組みで、強力な仕組みのものもあります。
---

**多要素認証**（**MFA**）はユーザー名（もしくはEメール）とパスワードを入力することに加え、追加の手順を必要とするセキュリティの仕組みです。 最も一般的な方法はSMSやアプリから一時的なコードを受け取るものです。

通常、ハッカー（または敵対者）はパスワードが分かれば、そのアカウントにアクセスできるようになります。 ハッカーが多要素認証で保護されたアカウントにアクセスするには、パスワード（あなたが*知っている*もの)と、携帯電話のような所有しているデバイス（あなたが*持っている*もの）の両方を必要とします。

多要素認証のセキュリティは様々ですが、攻撃者が多要素認証の仕組みにアクセスしにくいほど、よいという前提に基づいています。 他要素認証の手法としては（弱いものから強いもの順に）SMS、メールでのコード、アプリのプッシュ通知、TOTP、Yubico OTPやFIDOが挙げられます。

## 多要素認証の方法の比較

### SMSまたはEメール多要素認証

OTPコードをSMSもしくはメールで受信することは、多要素認証でアカウントを保護する弱い方法です。 メールやSMSでコードを受け取ることは「あなたが*持っている*もの」という条件が損なわれてしまいます。ハッカーは[電話番号を奪う](https://en.wikipedia.org/wiki/SIM_swap_scam)ことが可能であり、デバイスに物理的にアクセスすることなくメールにはアクセス可能だからです。 不正にメールにアクセスすることができれば、パスワードをリセットしたり、認証コードを受け取ったり、あなたのアカウントにフルアクセスすることができてしまいます。

### プッシュ通知

プッシュ通知の多要素認証は、新しいログインを確認するよう携帯電話のアプリにメッセージが送られるものです。 この方法はSMSやメールよりもはるかに優れています。攻撃者はすでにログインされたデバイスを持っていなければプッシュ通知を受け取ることはできず、まずはデバイスを攻撃する必要があります。

間違いを犯す可能性はあり、誤ってログイン試行を許可してしまうリスクもあります。 プッシュ通知によるログイン認証は*全ての*デバイスに送られることが多く、複数のデバイスがある場合はより広くアクセスできるようになってしまいます。

プッシュ通知多要素認証のセキュリティはアプリとサーバーコンポーネントの両方の品質、そして開発者の信頼性によります。 アプリケーションをインストールするには、デバイス上の他のデータへのアクセスを許可する必要があるかもしれません。 よいTOTP生成アプリとは異なり、開くのにパスワードを必要とせず、サービスごとにアプリが必要になることがあります。

### タイムベースドワンタイムパスワード(TOTP)

TOTPは、最も一般的なMFAの形式の一つです。 TOTPを設定する際、一般的には利用するサービスとの「[共有シークレット](https://en.wikipedia.org/wiki/Shared_secret)」を確立するため[QRコード](https://en.wikipedia.org/wiki/QR_code)をスキャンする必要があります。 共有シークレットは認証アプリのデータの中に保護され、パスワードによって保護されることもあります。

時間制限のあるコードは共有シークレットと現在時刻から生成されます。 コードは短時間のみ有効であり、共有シークレットにアクセスできなければ、敵対者は新たなコードを生成することはできません。

TOTPに対応したハードウェアセキュリティキー（[Yubico Authenticator](https://yubico.com/products/yubico-authenticator)に対応したYubiKeyなど）を持っている場合は、ハードウェアに「共有シークレット」を保存することを推奨します。 YubiKeyのようなハードウェアは「共有シークレット」の抽出やコピーが困難になることを意図して開発されています。 また、YubiKeyは携帯電話のTOTPアプリとは異なり、インターネットに接続しません。

[WebAuthn](#fido-fast-identity-online)とは異なり、TOTPは[フィッシング](https://en.wikipedia.org/wiki/Phishing)や反射攻撃からの保護はできません。 もし敵対者があなたから有効なコードを入手したら、有効期限（通常は60秒）が切れるまで何度でも使用することができます。

敵対者が公式サービスを似せたウェブサイトを立ち上げ、ユーザー名、パスワードと現在のTOTPコードをだまし取ろうとする可能性があります。 もし、敵対者が記録された認証情報を使えば、実際にサービスにログインし、アカウントを乗っ取ることができるかもしれません。

完璧ではありませんが、TOTPはほとんどの人にとって十分安全であり、[ハードウェアセキュリティーキー](../security-keys.md)が[認証アプリ](../multi-factor-authentication.md)に対応していない場合、依然としてよい選択肢です。

### ハードウェアのセキュリティキー

YubiKeyは耐タンパー性ソリッドステートチップにデータを保存しており、費用がかかる手順と法科学研究所なしには非破壊での[アクセスは不可能](https://security.stackexchange.com/a/245772)です。

ハードウェアセキュリティーキーは一般的に多機能であり、多くの認証方法に対応しています。 以下のものは最も一般的なものです。

#### Yubico OTP

Yubico OTPはハードウェアセキュリティーキーに実装される認証プロトコルです。 Yubico OTPを使う場合、キーは公開ID、秘密IDと秘密鍵を生成し、Yubico OTPサーバーにアップロードします。

ウェブサイトにログインする際には、セキュリティーキーに物理的にタッチするだけで済みます。 セキュリティーキーはキーボードをエミュレートし、パスワード欄にワンタイムパスワードを入力します。

検証のためにワンタイムパスワードをYubico OTPサーバーに送信します。 キーとYubico検証サーバーの両方でカウンターが増えます。 OTPは一度しか使うことはできず、認証が成功すると、OTPの再利用を防ぐためにカウンターが増えます。 Yubicoはこのプロセスの[詳細なドキュメント](https://developers.yubico.com/OTP/OTPs_Explained.html)を提供しています。

<figure markdown>
  ![Yubico OTP](../assets/img/multi-factor-authentication/yubico-otp.png)
</figure>

Yubico OTPはTOTPと比べて利点と欠点があります。

Yubico検証サーバーはクラウドベースのサービスでありデータが安全に保存され、プロファイリングされていないとYubicoを信頼する必要があります。 Yubico OTPに関連付けられた公開IDはあらゆるウェブサイトで再利用され、第三者がプロファイリングする手段になる可能性があります。 TOTPと同じく、Yubico OTPにはフィッシング耐性はありません。

それぞれのウェブサイトで異なるIDが必要となる脅威モデルの場合、公開IDは各セキュリティキーで固有であるため、そのウェブサイトに同じハードウェアセキュリティーキーでYubico OTPは使用**しないでください**。

#### FIDO (Fast IDentity Online)

[FIDO](https://en.wikipedia.org/wiki/FIDO_Alliance) includes a number of standards, first there was U2F and then later [FIDO2](https://en.wikipedia.org/wiki/FIDO2_Project) which includes the web standard [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn).

U2F and FIDO2 refer to the [Client to Authenticator Protocol](https://en.wikipedia.org/wiki/Client_to_Authenticator_Protocol), which is the protocol between the security key and the computer, such as a laptop or phone. It complements WebAuthn which is the component used to authenticate with the website (the "Relying Party") you're trying to log in on.

WebAuthn is the most secure and private form of second factor authentication. While the authentication experience is similar to Yubico OTP, the key does not print out a one-time password and validate with a third-party server. Instead, it uses [public key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) for authentication.

<figure markdown>
  ![FIDO](../assets/img/multi-factor-authentication/fido.png)
</figure>

When you create an account, the public key is sent to the service, then when you log in, the service will require you to "sign" some data with your private key. The benefit of this is that no password data is ever stored by the service, so there is nothing for an adversary to steal.

This presentation discusses the history of password authentication, the pitfalls (such as password reuse), and the standards for FIDO2 and [WebAuthn](https://webauthn.guide):

- [How FIDO2 and WebAuthn Stop Account Takeovers](https://youtu.be/aMo4ZlWznao) <small>(YouTube)</small>

FIDO2 and WebAuthn have superior security and privacy properties when compared to any MFA methods.

Typically, for web services it is used with WebAuthn which is a part of the [W3C recommendations](https://en.wikipedia.org/wiki/World_Wide_Web_Consortium#W3C_recommendation_(REC)). It uses public key authentication and is more secure than shared secrets used in Yubico OTP and TOTP methods, as it includes the origin name (usually, the domain name) during authentication. Attestation is provided to protect you from phishing attacks, as it helps you to determine that you are using the authentic service and not a fake copy.

Unlike Yubico OTP, WebAuthn does not use any public ID, so the key is **not** identifiable across different websites. It also does not use any third-party cloud server for authentication. All communication is completed between the key and the website you are logging into. FIDO also uses a counter which is incremented upon use in order to prevent session reuse and cloned keys.

If a website or service supports WebAuthn for the authentication, it is highly recommended that you use it over any other form of MFA.

## 一般的な推奨事項

We have these general recommendations:

### Which Method Should I Use?

When configuring your MFA method, keep in mind that it is only as secure as your weakest authentication method you use. This means it is important that you only use the best MFA method available. For instance, if you are already using TOTP, you should disable email and SMS MFA. If you are already using FIDO2/WebAuthn, you should not be using Yubico OTP or TOTP on your account.

### バックアップ

You should always have backups for your MFA method. Hardware security keys can get lost, stolen or simply stop working over time. It is recommended that you have a pair of hardware security keys with the same access to your accounts instead of just one.

When using TOTP with an authenticator app, be sure to back up your recovery keys or the app itself, or copy the "shared secrets" to another instance of the app on a different phone or to an encrypted container (e.g. [VeraCrypt](../encryption.md#veracrypt-disk)).

### 初期設定

When buying a security key, it is important that you change the default credentials, set up password protection for the key, and enable touch confirmation if your key supports it. Products such as the YubiKey have multiple interfaces with separate credentials for each one of them, so you should go over each interface and set up protection as well.

### 電子メールとSMS

If you have to use email for MFA, make sure that the email account itself is secured with a proper MFA method.

If you use SMS MFA, use a carrier who will not switch your phone number to a new SIM card without account access, or use a dedicated VoIP number from a provider with similar security to avoid a [SIM swap attack](https://en.wikipedia.org/wiki/SIM_swap_scam).

[推奨するMFAツール](../multi-factor-authentication.md ""){.md-button}

## More Places to Set Up MFA

Beyond just securing your website logins, multifactor authentication can be used to secure your local logins, SSH keys or even password databases as well.

### macOS

macOS has [native support](https://support.apple.com/guide/deployment/intro-to-smart-card-integration-depd0b888248/web) for authentication with smart cards (PIV). If you have a smart card or a hardware security key that supports the PIV interface such as the YubiKey, we recommend that you follow your smart card or hardware security vendor's documentation and set up second factor authentication for your macOS computer.

Yubico have a guide [Using Your YubiKey as a Smart Card in macOS](https://support.yubico.com/hc/articles/360016649059) which can help you set up your YubiKey on macOS.

After your smart card/security key is set up, we recommend running this command in the Terminal:

```text
sudo defaults write /Library/Preferences/com.apple.loginwindow DisableFDEAutoLogin -bool YES
```

The command will prevent an adversary from bypassing MFA when the computer boots.

### Linux

<div class="admonition warning" markdown>
<p class="admonition-title">注意</p>

If the hostname of your system changes (such as due to DHCP), you would be unable to login. It is vital that you set up a proper hostname for your computer before following this guide.

</div>

The `pam_u2f` module on Linux can provide two-factor authentication for logging in on most popular Linux distributions. If you have a hardware security key that supports U2F, you can set up MFA authentication for your login. Yubico has a guide [Ubuntu Linux Login Guide - U2F](https://support.yubico.com/hc/articles/360016649099-Ubuntu-Linux-Login-Guide-U2F) which should work on any distribution. The package manager commands—such as `apt-get`—and package names may however differ. This guide does **not** apply to Qubes OS.

### Qubes OS

Qubes OS has support for Challenge-Response authentication with YubiKeys. If you have a YubiKey with Challenge-Response authentication support, take a look at the Qubes OS [YubiKey documentation](https://qubes-os.org/doc/yubikey) if you want to set up MFA on Qubes OS.

### SSH

#### ハードウェアセキュリティ

SSH MFA could be set up using multiple different authentication methods that are popular with hardware security keys. We recommend that you check out Yubico's [documentation](https://developers.yubico.com/SSH) on how to set this up.

#### TOTP

SSH MFA can also be set up using TOTP. DigitalOcean has provided a tutorial [How To Set Up Multi-Factor Authentication for SSH on Ubuntu 20.04](https://digitalocean.com/community/tutorials/how-to-set-up-multi-factor-authentication-for-ssh-on-ubuntu-20-04). Most things should be the same regardless of distribution, however the package manager commands—such as `apt-get`—and package names may differ.

### KeePass（およびKeePassXC）

KeePass and KeePassXC databases can be secured using HOTP or Challenge-Response as a second-factor of authentication. Yubico has provided a document for KeePass [Using Your YubiKey with KeePass](https://support.yubico.com/hc/articles/360013779759-Using-Your-YubiKey-with-KeePass) and there is also one on the [KeePassXC](https://keepassxc.org/docs/#faq-yubikey-2fa) website.
