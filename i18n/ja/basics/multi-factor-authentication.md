---
title: "多要素認証"
icon: 'material/two-factor-authentication'
description: 多要素認証はオンラインアカウントを保護するためのセキュリティの仕組みで、強力な仕組みのものもあります。
---

**多要素認証**（**MFA**）はユーザー名（もしくはEメール）とパスワードを入力することに加え、追加の手順を必要とするセキュリティの仕組みです。 最も一般的な方法はSMSやアプリから一時的なコードを受け取るものです。

通常、ハッカー（または敵対者）はパスワードが分かれば、そのアカウントにアクセスできるようになります。 ハッカーが多要素認証で保護されたアカウントにアクセスするには、パスワード（あなたが*知っている*もの)と、携帯電話のような所有しているデバイス（あなたが*持っている*もの）の両方を必要とします。

多要素認証のセキュリティは様々ですが、攻撃者が多要素認証の仕組みにアクセスしにくいほど、よいという前提に基づいています。 多要素認証の手法としては（弱いものから強いもの順に）SMS、メールでのコード、アプリのプッシュ通知、TOTP、Yubico OTPやFIDOが挙げられます。

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

[FIDO](https://en.wikipedia.org/wiki/FIDO_Alliance)には多くの標準規格があり、最初にU2F、後にウェブ標準の[WebAuthn](https://en.wikipedia.org/wiki/WebAuthn)を含む[FIDO2](https://en.wikipedia.org/wiki/FIDO2_Project)が策定されました。

U2FとFIDO2は[Client to Authenticator Protocol](https://en.wikipedia.org/wiki/Client_to_Authenticator_Protocol)で、セキュリティーキーとラップトップや携帯電話のようなコンピューター間のプロトコルです。 ログインしようとしているウェブサイト（「Relaying Party」）との認証に使われているコンポーネントであるWebAuthnを補完しています。

WebAuthnは最も安全でプライベートな二要素認証の方法です。 認証の使い勝手はYubico OTPと似ていますが、キーはワンタイムパスワードを出力せず、第三者のサーバーで検証もしません。 その代わり、認証には[公開鍵暗号](https://en.wikipedia.org/wiki/Public-key_cryptography)を用います。

<figure markdown>
  ![FIDO](../assets/img/multi-factor-authentication/fido.png)
</figure>

アカウント作成時にサーバーに公開鍵を送り、ログインする際にサービス側は秘密鍵でデータに「署名」するよう要求します。 利点はサービス側にパスワードが保存されておらず、敵対者は盗むものがないことです。

以下のプレゼンテーションではパスワード認証の歴史、危険性（パスワードの再利用など）、FIDOと[WebAuthn](https://webauthn.guide)標準について説明しています：

- [How FIDO2 and WebAuthn Stop Account Takeovers](https://youtu.be/aMo4ZlWznao) <small>(YouTube)</small>

FIDO2とWebAuthnは他の多要素認証の方法よりも安全性とプライバシー面で優れています。

通常、ウェブサービスでは[W3C勧告](https://en.wikipedia.org/wiki/World_Wide_Web_Consortium#W3C_recommendation_(REC))の一部であるWebAuthnとともに使用されます。 公開鍵認証を使用し、認証時にオリジンネーム（通常はドメイン名）を含むため、Yubico OTPやTOTPで使われるような共有シークレットよりも安全です。 認証はサービスが偽物ではなく本物であることを確認するのに役立つため、フィッシング詐欺から保護します。

Yubico OTPとは異なり、WebAuthnは公開IDを使わないため、異なるウェブサイト間でキーを識別することが**できません**。 また、認証に第三者のクラウドサーバーを使用することもありません。 全ての通信は、キーとログインしているウェブサイト間で完結します。 また、FIDOはセッションの再利用やキーの複製を防ぐため、使用時に増やすカウンターを使っています。

ウェブサイトやサービスがWebAuthnの認証に対応している場合、他の多要素認証よりもWebAuthnを使うことを強く推奨します。

## 一般的な推奨事項

一般的には以下のように推奨しています：

### どの方法を使うべきか？

多要素認証を設定する際、使用する最も弱い認証方法と同じ安全性になってしまうことに留意してください。 つまり、利用できる最も強力な多要素認証のみを使うことが重要です。 例えば、TOTPをすでに使っている場合、メールやSMS多要素認証は無効にする必要があります。 もし、FIDO2/WebAuthnをすでに使っている場合、そのアカウントではYubico OTPやTOTPを使うべきではありません。

### バックアップ

多要素認証は常にバックアップしておく必要があります。 ハードウェアセキュリティーキーは紛失したり、盗まれたり、または時間の経過とともに動かなくなったりします。 アカウントにアクセスできるハードウェアセキュリティーキーは1つだけではなく、2つ持つことを推奨します。

認証アプリでTOTPを使う際、リカバリーキーやアプリ自体をバックアップするか、「共有シークレット」を他の携帯電話のアプリか暗号化されたコンテナ（[VeraCrypt](../encryption.md#veracrypt-disk)など）にコピーしてください。

### 初期設定

セキュリティーキーを購入する際、デフォルトの認証情報を変更し、キーのパスワード保護を設定し、タッチ認証に対応している場合は有効にすることが重要です。 YubiKeyのような製品には複数のインターフェースがあり、個別に認証が設定されています。そのため、各インターフェースごとに調べ、保護の設定をする必要があります。

### 電子メールとSMS

多要素認証にメールを使う必要がある場合、メールアカウント自体が適切な多要素認証で保護されていることを確認してください。

SMS多要素認証を使う場合、[SIMスワップ詐欺](https://en.wikipedia.org/wiki/SIM_swap_scam)を避けるために、アカウントにアクセスせずに電話番号を新しいSIMカードに切り替えないキャリアを使うか、同様のセキュリティがあるプロバイダーの専用のVoIP番号を使用してください。

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
