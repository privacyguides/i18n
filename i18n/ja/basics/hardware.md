---
title: ハードウェアを選ぶ
icon: material/chip
description: ソフトウェアだけが全てではありません。プライバシーを守るために日常的に使うハードウェアのツールについて学びましょう。
---

プライバシーについて議論する際、ハードウェアはソフトウェアほど考慮されていないことが多いです。 ハードウェアはプライバシーを設定するもう一つの基礎であると考えるべきです。

## コンピューターを選ぶ

デバイスの内部では全てのデジタルデータを処理し、保存しています。 デバイスはメーカーや開発者によってセキュリティアップデートを受け続けることができるようサポートされていることが重要です。

### ハードウェアセキュリティプログラム

「ハードウェアセキュリティプログラム」のあるデバイスもあります。ハードウェアを設計する際のベストプラクティスや推奨に関するベンダー間の協力によって成り立っています。例えば以下のものが挙げられます：

- [WindowsのセキュアコアPC](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure-11) は、マイクロソフトによって定められた高いセキュリティ基準を満たすものです。 Windowsのユーザーだけではなく、 他のOSのユーザーも[DMA保護](https://learn.microsoft.com/en-us/windows/security/information-protection/kernel-dma-protection-for-thunderbolt) やMicrosoftの証明書を完全に信用しないようにする機能を利用することができます。
- [Android Ready SE](https://developers.google.com/android/security/android-ready-se) はデバイスが[ベストプラクティス](https://source.android.com/docs/security/best-practices/hardware)に従い、暗号化キーなどのために耐タンパ性のあるストレージが含まれていることを保証するベンダー間の協力によるものです。
- Apple SoC上で動作するmacOSは他のOSでは利用できない[ハードウェアセキュリティ](../os/macos-overview.md#hardware-security)を活用しています。
- [ChromeOSのセキュリティ](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper)はChromebook上で実行する際に[hardware root-of-trust](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper/#hardware-root-of-trust-and-verified-boot)のようなハードウェアの機能を使うことができるため、最も強力なものとなります。

上記のOSを使っていなくても、プログラムに参加しているメーカーはハードウェアセキュリティやアップデートに関するベストプラクティスに従っていることを示している可能性があります。

### プリインストールOS

Macや特別なLinuxマシンを買わない限り、新しいコンピューターにはほとんどの場合、Windowsがプリインストールされています。 ドライブを消去し、選んだOSを新たにインストールすること（Windowsを再インストールすることも）はよい考えです。 ハードウェアベンダーと怪しいソフトウェアベンダーとの契約により、デフォルトのWindowsにはあらかじめロードするように設定されたブロートウェア、[アドウェア](https://bleepingcomputer.com/news/technology/lenovo-gets-a-slap-on-the-wrist-for-superfish-adware-scandal)や[マルウェア](https://zdnet.com/article/dell-poweredge-motherboards-ship-with-malware)があることが多いです。

### ファームウェアの更新

ハードウェアにはセキュリティ上の問題が発見されることがあり、ファームウェアアップデートによりパッチが適用されます。

マザーボードからストレージデバイスに至るまで、コンピューターのほぼ全てのコンポーネントは動作するのにファームウェアが必要です。 全てのコンポーネントが完全にサポートされていることが理想的です。 Appleのデバイス、Chromebook、ほとんどのAndroid端末、Microsoft Surfaceはデバイスがサポートされている限り、ファームウェアアップデートがあります。

自作PCの場合は、マザーボードのファームウェアはOEMのウェブサイトからダウンロードし、手動でアップデートする必要があるかもしれません。 Linuxの場合、ビルトインの[`pwupd`](https://fwupd.org)を使い、マザーボードで利用可能なファームウェアアップデートを確認、適用することを検討してください。

### TPM/セキュア暗号プロセッサー

ほとんどのコンピューターや携帯電話にはTPM（もしくは同様のセキュア暗号プロセッサー）が搭載されており、暗号鍵を安全に保存し、その他セキュリティ関連の機能を処理します。 もし、このような機能がないマシンを使っているのであれば、機能のある新しいコンピューターを購入するほうがよいでしょう。 デスクトップ・サーバーのマザーボードの中にはTPMを搭載した小型のアクセサリーボードをつけることができる「TPMヘッダー」があるものもあります。

<div class="admonition Note" markdown>
<p class="admonition-title">メモ</p>

仮想TPMはサイドチャネル攻撃の影響を受けやすく、外部TPMは攻撃者がハードウェアにアクセスできる場合、マザーボード上のCPUから分離されているため、[スニッフィング](https://pulsesecurity.co.nz/articles/TPM-sniffing)に脆弱です。 セキュアプロセッサーをCPU自体に内蔵することが解決策であり、AppleのチップやMicrosoftの[Pluton](https://microsoft.com/en-us/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs)が例として挙げられます。

</div>

### 生体認証

多くのデバイスには指紋読取や顔認証の機能が搭載されています。 とても便利ですが、完璧ではなく、失敗することもあります。 その場合、ほとんどデバイスはPINやパスワードにフォールバックします。つまり、パスワードと同程度のセキュリティであるということです。

生体認証はパスワードの入力を見られることを防ぐことができるため、脅威モデルにショルダーサーフィンがあるなら、生体認証はよい選択肢です。

ほとんどの顔認証の実装では携帯電話を見る必要があり、比較的近い距離でのみ動作するため、誰かが同意なしに携帯電話のロックを解除するために携帯電話を向けることを心配し過ぎる必要はありません。 必要であれば、携帯電話がロックされているときに生体認証を無効にすることもできます。 iOSでは、FaceIDに対応したモデルで、サイドボタンと音量ボタンを3秒間長押しして、FaceIDを無効にできます。 Androidでは、電源ボタンを押して、メニューのロックダウンを選択します。

<div class="admonition warning" markdown>
<p class="admonition-title">注意</p>

デバイスによっては安全な顔認証のための適切なハードウェアがないものもあります。 顔認証には主なタイプとして2Dと3Dの二種類があります。 3D顔認証ではドットプロジェクターを使用し、顔の3D深度マップを作成します。 デバイスにこの機能があることを確認してください。

</div>

Androidでは生体認証の[生体認証クラス](https://source.android.com/docs/security/features/biometric/measure#biometric-classes)が定められており、生体認証を有効にする前に、デバイスがクラス3であることを確認してください。

### デバイスの暗号化

デバイスが[暗号化](../encryption.md)されている場合、最初に暗号化鍵やロックスクリーンのパスワードを入力する前、（単にスリープ状態になっているのではなく）完全に電源がオフになっているときにデータは最も安全な状態です。 携帯電話では、セキュリティが高い状態を「Before First Unlock」（BFU）と呼び、再起動・電源オン後に正しいパスワードを入力した状態を「After First Unlock」（AFU）と呼びます。 AFUはBFUに比べ、デジタルフォレンジックツールやその他の攻撃に対してかなり安全性が低くなります。 そのため、敵対者によるデバイスへの物理的なアクセスを懸念する場合、使っていないときは完全に電源を切る必要があります。

現実的ではないかもしれないため、その価値があるか検討してください。いずれにせよ、強力な暗号鍵を使っていれば、AFUでも多くの脅威には有効です。

## 外付けのハードウェア

内部コンポーネントだけでは対抗できない脅威もあります。 状況によるところが大きいため、脅威モデルに本当に必要であるか評価してください。

### ハードウェアセキュリティ

ハードウェアキーは強力な暗号技術を使って、デバイスやアカウントの認証を行うデバイスです。 ハードウェアキーはコピーできず、物理的に所持している場合にのみアクセスできる方法でアカウントを保護するため、多くのリモート攻撃を排除できます。

[推奨するハードウェアキー :material-arrow-right-drop-circle:](../security-keys.md){ .md-button .md-button--primary } [ハードウェアキーの詳細 :material-arrow-right-drop-circle:](multi-factor-authentication.md#hardware-security-keys){ .md-button }

### カメラ/マイク

OSの権限管理をそもそも信用しない場合、物理的にカメラに光が届かないようにカメラブロックを購入することも一つの方法です。 また、カメラが内蔵されていないデバイスを購入し、使っていないときには取り外すことができる外付けのカメラを使うことも一つの方法です。 カメラブロッカー付きのものやカメラを電源から物理的に切り離すハードウェアスイッチのあるカメラもあります。

<div class="admonition warning" markdown>
<p class="admonition-title">注意</p>

ノートパソコンに合っていて、蓋を閉めたときにダメージを与えないカメラカバーを買うようにしてください。 カメラを覆うと、明るさの自動調整や顔認証機能の妨げになります。

</div>

マイクのアクセスについては、多くの場合、OSの権限管理を信用する必要があります。 もしくはマイクが内蔵されていないデバイスを購入し、使っていないときには外すことができる外付けのマイクを使ってください。 [MacBookやiPad](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web)のように蓋をしめるとマイクがハードウェア的に切断されるデバイスもあります。

多くのコンピューターにはカメラやマイクを無効にするオプションがBIOSにあります。 無効にすると、起動したシステム上にデバイスとして表示されなくなります。

### プライバシースクリーン

プライバシースクリーンはスクリーン上にフィルムを貼り、ある角度でのみスクリーンが見えるようにするものです。 脅威モデルにスクリーンを覗き見することがある場合はよいですが、誰でも視野角を変えるだけでスクリーンを見ることができるため、確実なものではありません。

### デッドマンスイッチ

デッドマンスイッチは人間の操作なしに機械の動作を停止させるものです。 もとは安全対策が目的のものですが、不在時に電子機器をロックすることにも当てはめることができます。

スクリーンの前に座っていないときに、自動的にロックがかかるよう[検知](https://support.microsoft.com/en-us/windows/managing-presence-sensing-settings-in-windows-11-82285c93-440c-4e15-9081-c9e38c1290bb)するノートパソコンもあります。 コンピューターがこの機能に対応しているか、OSの設定を確認してください。

[BusKill](https://buskill.in)のようなケーブルが切断されたときにコンピューターをロックまたは消去するケーブルもあります。

### アンチインターディクション・悪意あるメイド攻撃

手元にデバイスが届く前の標的型攻撃を防ぐ最善の方法は、送り届けてもらうのではなく、実店舗でデバイスを購入することです。

デバイスがセキュアブート・ベリファイドブートに対応しているか確認し、有効にしてください。 可能な限り、デバイスを放置しないようにしてください。

## Secure your Network

### Compartmentalization

Many solutions exist that allow you to separate what you're doing on a computer, such as virtual machines and sandboxing. However, the best compartmentalization is physical separation. This is useful especially for situations where certain software requires you to bypass security features in your OS, such as with anti-cheat software bundled with many games.

For gaming, it may be useful to designate one machine as your "gaming" machine and only use it for that one task. Keep it on a separate VLAN. This may require the use of a managed switch and a router that supports segregated networks.

Most consumer routers allow you to do this by enabling a separate "guest" network that can't talk to your main network. All untrusted devices can go here, including IoT devices like your smart fridge, thermostat, TV, etc.

### Minimalism

As the saying goes, "less is more". The fewer devices you have connected to your network, the less potential attack surface you'll have and the less work it will be to make sure they all stay up-to-date.

You may find it useful to go around your home and make a list of every connected device you have to help you keep track.

### Routers

Your router handles all your network traffic and acts as your first line of defense between you and the open internet.

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

A lot of routers come with storage to put your files on so you can access them from any computer on your network. We recommend you don't use networking devices for things other than networking. In the event your router was compromised, your files would also be compromised.

</div>

The most important thing to think about with routers is keeping them up-to-date. Many modern routers will automatically install updates, but many others won't. You should check on your router's settings page for this option. That page can usually be accessed by typing `192.168.1.1` or `192.168.0.1` into the URL bar of any browser assuming you're on the same network. You can also check in the network settings of your OS for "router" or "gateway".

If your router does not support automatic updates, you will need to go to the manufacturer's site to download the updates and apply them manually.

Many consumer-grade routers aren't supported for very long. If your router isn't supported by the manufacturer anymore, you can check if it's supported by [FOSS firmware](../router.md). You can also buy routers that come with FOSS firmware installed by default; these tend to be supported longer than most routers.

Some ISPs provide a combined router/modem. It can be beneficial for security to purchase a separate router and set your ISP router/modem into modem-only mode. This way, even when your ISP-provided router is no longer getting updates, you can still get security updates and patches. It also means any problems that affect your modem won't affect your router and vice versa.
