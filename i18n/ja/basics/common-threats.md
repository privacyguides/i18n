---
title: "一般的な脅威"
icon: 'material/eye-outline'
description: 脅威モデルは個々人によりますが、このサイトの閲覧者が気にしていることが含まれます。
---

一般的にいえば、推奨するものは多くの人に当てはまる[脅威](threat-modeling.md)や目標に分類することができます。 ==この可能性のうち、どれも心配していないかもしれませんし、一つ、２つ以上、もしくは全てに関心があるかもしれませんが、==使うツールやサービスは目標によります。 このカテゴリ以外の脅威に関心があるかもしれませんが、問題ありません！ 重要なのは、選んだツールの利点と欠点を理解することです。なぜならすべての脅威から保護するようなものは実際ないからです。

<span class="pg-purple">:material-incognito:**匿名性**</span>
:

オンライン上の活動を実際の身元から保護し、*あなたの*身元を特定しようとする人から守ります。

<span class="pg-red">:material-target-account:**標的型攻撃**</span>
:

*あなたの*データやデバイスを対象にアクセスしようとするハッカーや悪意のある者から守ります。

<span class="pg-viridian">:material-package-variant-closed-remove:**サプライチェーン攻撃**</span>
:

典型的な<span class="pg-red">:material-target-account:標的型攻撃</span>の一つで、正常なソフトウェアに直接もしくはサードパーティの依存関係の脆弱性やエクスプトイトを伝って行われる攻撃です。

<span class="pg-orange">:material-bug-outline:**パッシブ攻撃**</span>
:

マルウェア、データ漏洩など一度に多数の人を対象に行われる攻撃から守ります。

<span class="pg-teal">:material-server-network:**サービスプロバイダー**</span>
:

サービスの提供者からデータを守ります（例えば、エンドツーエンド暗号化によって、サーバーでデータを読み取ることができなくなります）。

<span class="pg-blue">:material-eye-outline:**監視社会**</span>
:

政府の機関・組織・ウェブサイトや活動を追跡することに協力するサービスから守ります。

<span class="pg-brown">:material-account-cash:**監視資本主義**</span>
:

GoogleやFacebookのような巨大な広告ネットワークやその他多数のサードパーティのデータ収集者から守ります。

<span class="pg-green">:material-account-search:**秘密の暴露**</span>
:

検索エンジンに対し、もしくは一般公開されている、オンライン上の情報へのアクセスに制限します。

<span class="pg-blue-gray">:material-close-outline:**検閲**</span>
:

オンライン上で発言する際、情報や自身に対する検閲を避けます。

懸念によりますが、脅威の中には他よりも重要だと思うものがあるかもしれません。 例えば、貴重なもしくは重要なデータにアクセスできるソフトウェア開発者は主に<span class="pg-viridian">:material-package-variant-closed-remove:サプライチェーン攻撃</span>や<span class="pg-red">:material-target-account:標的型攻撃</span>に関心を持つかもしれません。 また、<span class="pg-blue">:material-eye-outline:監視社会</span>のプログラムに巻き込まれないよう個人のデータを守りたいと思うでしょう。 同様に、多くの人は主に個人データの<span class="pg-green">:material-account-search:秘密の暴露</span>は気にしているかもしれませんが、デバイスがマルウェアに感染するなどの<span class="pg-orange">:material-bug-outline:パッシブ攻撃</span>のようなセキュリティの問題にも注意を向ける必要があります。

## 匿名性とプライバシーの比較

<span class="pg-purple">:material-incognito: 匿名性</span>

匿名性はしばしばプライバシーと混同されますが、それらは異なる概念です。 プライバシーは個人のデータがどのように使われ、共有されるかを選択するのに対し、匿名性は実際の身元とオンライン上での活動を完全に切り離すことです。

例えば、内部告発者やジャーナリストの脅威モデルは完全な匿名性が必要となる極端なものになるでしょう。 何をしているか、どんなデータを持っているかを隠し、悪意ある者や政府からハッキングされていないことだけではなく、誰であるかを完全に隠すことです。 命がかかっているため、匿名性、プライバシー、セキュリティを守るためであればどんな利便性も犠牲にするでしょう。 ほとんどの人はそこまでする必要はありません。

## セキュリティーとプライバシー

<span class="pg-orange">:material-bug-outline: パッシブ攻撃</span>

セキュリティとプライバシーはよく混同されます。プライバシーを確保するにはセキュリティが必要です：たとえ設計上はプライバシーが確保されているツールを使っていても、個人のデータを公開しようとする攻撃者が簡単に攻撃できるのであれば、意味がありません。 ただし、この逆は必ずしも正しいわけではありません：世界で最もセキュアなサービスはプライバシーがある*とは限りません*。 最もよい例はGoogleにデータを託すことです。インフラを保護するために業界トップのセキュリティ専門家を雇っており、Googleの規模を考えれば、セキュリティインシデントはほとんど起きていません。 Googleのサービスは非常に安全ではありますが、Googleの一般消費者向けの無料サービス（Gmail, YouTubeなど）で自分のデータのプライバシーがあると考える人はほとんどいないでしょう。

アプリケーションのセキュリティに関して、通常はそのソフトウェアが悪意のあるものか、あるいは悪意のあるものになるかは分かりません（知ることすらできないこともあります）。 たとえ信頼のできる開発者が関わっていたとしても、重大な脆弱性がなく、悪用されないという保証はありません。

悪意のあるソフトウェアの影響を最小限に抑え*うる*ためには、区画化によるセキュリティを採用することです。 例えば、ジョブごとにコンピューターを使い分けたり、関連するアプリケーションのグループごとに仮想マシンを分けたり、アプリケーションのサンドボックスや強制的なアクセス制御を重視したセキュアなOSを使ったりすることが挙げられます。

<div class="admonition tip" markdown>
<p class="admonition-title">ヒント</p>

一般的にモバイルOSはデスクトップOSよりもアプリケーションサンドボックス機能が優れています：アプリケーションはルートアクセスを取得できず、システムリソースへのアクセスは許可が必要です。

デスクトップOSは適切なサンドボックス化では遅れています。 ChromeOSにはAndroidと同じようなサンドボックス機能があり、macOSには完全なシステムの権限制御があります（開発者はアプリケーションのサンドボックス化を選ぶことができます）。 ただし、識別情報をOEM元に送信します。 Linuxはシステムベンダーに情報を送らないことが多いですが、エクスプロイトや悪意のあるアプリからの保護は不十分です。 [QubesOS](../desktop.md#qubes-os)のような仮想マシンやコンテナを多用する特別なディストリビューションを使えば影響は軽減されます。

</div>

## Attacks against Specific Individuals

<span class="pg-red">:material-target-account: Targeted Attacks</span>

Targeted attacks against a specific person are more problematic to deal with. Common attacks include sending malicious documents via email, exploiting vulnerabilities (e.g. in browsers and operating systems), and physical attacks. If this is a concern for you, you should employ more advanced threat mitigation strategies.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

By design, **web browsers**, **email clients**, and **office applications** typically run untrusted code, sent to you from third parties. Running multiple virtual machines—to separate applications like these from your host system, as well as each other—is one technique you can use to mitigate the chance of an exploit in these applications compromising the rest of your system. For example, technologies like Qubes OS or Microsoft Defender Application Guard on Windows provide convenient methods to do this.

</div>

If you are concerned about **physical attacks** you should use an operating system with a secure verified boot implementation, such as Android, iOS, macOS, or [Windows (with TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). You should also make sure that your drive is encrypted, and that the operating system uses a TPM or Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) or [Element](https://developers.google.com/android/security/android-ready-se) to rate limit attempts to enter the encryption passphrase. You should avoid sharing your computer with people you don't trust, because most desktop operating systems don't encrypt data separately per-user.

## Attacks against Certain Organizations

<span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>

Supply chain attacks are frequently a form of <span class="pg-red">:material-target-account: Targeted Attack</span> towards businesses, governments, and activists, although they can end up compromising the public at large as well.

<div class="admonition example" markdown>
<p class="admonition-title">Example</p>

A notable example of this occurred in 2017 when M.E.Doc, a popular accounting software in Ukraine, was infected with the *NotPetya* virus, subsequently infecting people who downloaded that software with ransomware. NotPetya itself was a ransomware attack which impacted 2000+ companies in various countries, and was based on the *EternalBlue* exploit developed by the NSA to attack Windows computers over the network.

</div>

There are few ways in which this type of attack might be carried out:

1. A contributor or employee might first work their way into a position of power within a project or organization, and then abuse that position by adding malicious code.
2. A developer may be coerced by an outside party to add malicious code.
3. An individual or group might identify a third party software dependency (also known as a library) and work to infiltrate it with the above two methods, knowing that it will be used by "downstream" software developers.

These sorts of attacks can require a lot of time and preparation to perform and are risky because they can be detected, particularly in open source projects if they are popular and have outside interest. Unfortunately they're also one of the most dangerous as they are very hard to mitigate entirely. We would encourage readers to only use software which has a good reputation and makes an effort to reduce risk by:

1. Only adopting popular software that has been around for a while. The more interest in a project, the greater likelihood that external parties will notice malicious changes. A malicious actor will also need to spend more time gaining community trust with meaningful contributions.
2. Finding software which releases binaries with widely-used, trusted build infrastructure platforms, as opposed to developer workstations or self-hosted servers. Some systems like GitHub Actions let you inspect the build script that runs publicly for extra confidence. This lessens the likelihood that malware on a developer's machine could infect their packages, and gives confidence that the binaries produced are in fact produced correctly.
3. Looking for code signing on individual source code commits and releases, which creates an auditable trail of who did what. For example: Was the malicious code in the software repository? Which developer added it? Was it added during the build process?
4. Checking whether the source code has meaningful commit messages (such as [conventional commits](https://conventionalcommits.org)) which explain what each change is supposed to accomplish. Clear messages can make it easier for outsiders to the project to verify, audit, and find bugs.
5. Noting the number of contributors or maintainers a program has. A lone developer may be more susceptible to being coerced into adding malicious code by an external party, or to negligently enabling undesirable behavior. This may very well mean software developed by "Big Tech" has more scrutiny than a lone developer who doesn't answer to anyone.

## Privacy from Service Providers

<span class="pg-teal">:material-server-network: Service Providers</span>

We live in a world where almost everything is connected to the internet. Our "private" messages, emails, and social interactions are typically stored on a server, somewhere. Generally, when you send someone a message it's stored on a server, and when your friend wants to read the message the server will show it to them.

The obvious problem with this is that the service provider (or a hacker who has compromised the server) can access your conversations whenever and however they want, without you ever knowing. This applies to many common services, like SMS messaging, Telegram, and Discord.

Thankfully, E2EE can alleviate this issue by encrypting communications between you and your desired recipients before they are even sent to the server. The confidentiality of your messages is guaranteed, assuming the service provider doesn't have access to the private keys of either party.

<div class="admonition note" markdown>
<p class="admonition-title">Note on Web-based Encryption</p>

In practice, the effectiveness of different E2EE implementations varies. Applications, such as [Signal](../real-time-communication.md#signal), run natively on your device, and every copy of the application is the same across different installations. If the service provider were to introduce a [backdoor](https://en.wikipedia.org/wiki/Backdoor_(computing)) in their application—in an attempt to steal your private keys—it could later be detected with [reverse engineering](https://en.wikipedia.org/wiki/Reverse_engineering).

On the other hand, web-based E2EE implementations, such as Proton Mail's web app or Bitwarden's *Web Vault*, rely on the server dynamically serving JavaScript code to the browser to handle cryptography. A malicious server can target you and send you malicious JavaScript code to steal your encryption key (and it would be extremely hard to notice). Because the server can choose to serve different web clients to different people—even if you noticed the attack—it would be incredibly hard to prove the provider's guilt.

Therefore, you should use native applications over web clients whenever possible.

</div>

Even with E2EE, service providers can still profile you based on **metadata**, which typically isn't protected. While the service provider can't read your messages, they can still observe important things, such as whom you're talking to, how often you message them, and when you're typically active. Protection of metadata is fairly uncommon, and—if it's within your [threat model](threat-modeling.md)—you should pay close attention to the technical documentation of the software you're using to see if there's any metadata minimization or protection at all.

## 大量監視プログラム

<span class="pg-blue">:material-eye-outline: Mass Surveillance</span>

Mass surveillance is the intricate effort to monitor the "behavior, many activities, or information" of an entire (or substantial fraction of a) population.[^1] It often refers to government programs, such as the ones [disclosed by Edward Snowden in 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). However, it can also be carried out by corporations, either on behalf of government agencies or by their own initiative.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France, you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

Governments often justify mass surveillance programs as necessary means to combat terrorism and prevent crime. However, as breaches of human rights, they're most often used to disproportionately target minority groups and political dissidents, among others.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

In the face of Edward Snowden's disclosures of government programs such as [PRISM](https://en.wikipedia.org/wiki/PRISM) and [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), intelligence officials also admitted that the NSA had for years been secretly collecting records about virtually every American’s phone calls — who’s calling whom, when those calls are made, and how long they last. This kind of information, when amassed by the NSA day after day, can reveal incredibly sensitive details about people’s lives and associations, such as whether they have called a pastor, an abortion provider, an addiction counselor, or a suicide hotline.

</div>

Despite growing mass surveillance in the United States, the government has found that mass surveillance programs like Section 215 have had "little unique value" with respect to stopping actual crimes or terrorist plots, with efforts largely duplicating the FBI's own targeted surveillance programs.[^2]

Online, you can be tracked via a variety of methods, including but not limited to:

- あなたのIPアドレス
- ブラウザーのクッキー
- The data you submit to websites
- Your browser or device fingerprint
- Payment method correlation

If you're concerned about mass surveillance programs, you can use strategies like compartmentalizing your online identities, blending in with other users, or, whenever possible, simply avoiding giving out identifying information.

## Surveillance as a Business Model

<span class="pg-brown">:material-account-cash: Surveillance Capitalism</span>

> Surveillance capitalism is an economic system centered around the capture and commodification of personal data for the core purpose of profit-making.[^3]

For many people, tracking and surveillance by private corporations is a growing concern. Pervasive ad networks, such as those operated by Google and Facebook, span the internet far beyond just the sites they control, tracking your actions along the way. Using tools like content blockers to limit network requests to their servers, and reading the privacy policies of the services you use can help you avoid many basic adversaries (although it can't completely prevent tracking).[^4]

Additionally, even companies outside the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. You can't automatically assume your data is safe just because the service you're using doesn't fall within the typical AdTech or tracking business model. The strongest protection against corporate data collection is to encrypt or obfuscate your data whenever possible, making it difficult for different providers to correlate data with each other and build a profile on you.

## Limiting Public Information

<span class="pg-green">:material-account-search: Public Exposure</span>

The best way to keep your data private is simply not making it public in the first place. Deleting unwanted information you find about yourself online is one of the best first steps you can take to regain your privacy.

- [アカウント削除に関するガイド :material-arrow-right-drop-circle: を表示](account-deletion.md)

On sites where you do share information, checking the privacy settings of your account to limit how widely that data is spread is very important. For example, enable "private mode" on your accounts if given the option: This ensures that your account isn't being indexed by search engines, and that it can't be viewed without your permission.

If you've already submitted your real information to sites which shouldn't have it, consider using disinformation tactics, like submitting fictitious information related to that online identity. This makes your real information indistinguishable from the false information.

## 検閲の回避

<span class="pg-blue-gray">:material-close-outline: 検閲</span>

Censorship online can be carried out (to varying degrees) by actors including totalitarian governments, network administrators, and service providers. These efforts to control communication and restrict access to information will always be incompatible with the human right to Freedom of Expression.[^5]

Censorship on corporate platforms is increasingly common, as platforms like Twitter and Facebook give in to public demand, market pressures, and pressures from government agencies. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

People concerned with the threat of censorship can use technologies like [Tor](../advanced/tor-overview.md) to circumvent it, and support censorship-resistant communication platforms like [Matrix](../real-time-communication.md#element), which doesn't have a centralized account authority that can close accounts arbitrarily.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

While evading censorship itself can be easy, hiding the fact that you are doing it can be very problematic.

You should consider which aspects of the network your adversary can observe, and whether you have plausible deniability for your actions. For example, using [encrypted DNS](../advanced/dns-overview.md#what-is-encrypted-dns) can help you bypass rudimentary, DNS-based censorship systems, but it can't truly hide what you are visiting from your ISP. A VPN or Tor can help hide what you are visiting from network administrators, but can't hide that you're using those networks in the first place. Pluggable transports (such as Obfs4proxy, Meek, or Shadowsocks) can help you evade firewalls that block common VPN protocols or Tor, but your circumvention attempts can still be detected by methods like probing or [deep packet inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection).

</div>

You must always consider the risks of trying to bypass censorship, the potential consequences, and how sophisticated your adversary may be. You should be cautious with your software selection, and have a backup plan in case you are caught.

[^1]: Wikipedia: [*Mass Surveillance*](https://en.wikipedia.org/wiki/Mass_surveillance) and [*Surveillance*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: United States Privacy and Civil Liberties Oversight Board: [*Report on the Telephone Records Program Conducted under Section 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. You should also employ other mitigation techniques.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
