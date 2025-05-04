---
title: "よくある誤解"
icon: 'material/robot-confused'
description: プライバシーは単純ではないテーマであり、マーケティング上の主張や他の嘘の情報に巻き込まれやすい。
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: オープンソースソフトウェアは本質的に安全ですか？
        acceptedAnswer:
          "@type": Answer
          text: |
            ソースコードが入手可能かどうかやライセンスは本質的にはソフトウェアのセキュリティに影響を与えるものではありません。 オープンソースソフトウェアはプロプラエタリソフトウェアよりも潜在的には安全ですが、絶対的な保証はありません。 ソフトウェアを評価する際には、各ツールの評価や安全性を個別に判断する必要があります。
      - 
        "@type": Question
        name: 他のプロバイダーへの信頼の移行によりプライバシーは向上しますか？
        acceptedAnswer:
          "@type": Answer
          text: |
            VPNのようなソリューション（信頼をISPからVPNプロバイダーに移す）について議論が行われる際、「信頼の移行」について話すことが多いです。 ISPからブラウジングデータは保護される一方で、VPNプロバイダーからはブラウジングデータにアクセスできます：すべての関係者に対して完全に安全を確保できるわけではありません。
      - 
        "@type": Question
        name: プライバシー重視のソリューションは本来的に信頼できますか？
        acceptedAnswer:
          "@type": Answer
          text: |
            ツールのプライバシーポリシーやマーケティングだけに注目し過ぎるとその弱点が見えなくなります。 よりプライバシーを重視した解決策を探している場合、根本的な問題を見極め、技術的な解決策を見つける必要があります。 例えば、GoogleがすべてのデータにアクセスできるGoogle Driveの利用をやめたいとしましょう。 この場合の根本的な問題はエンドツーエンド暗号化がないことで、乗り換えるプロバイダーに実際にエンドツーエンド暗号化が実装されているか確認するか、どのクラウドサービスプロバイダーでもエンドツーエンド暗号化ができる（Cryptomatorのような）ツールを使用する必要があります。 （エンドツーエンド暗号化がない）「プライバシー重視」のプロバイダーに乗り換えても問題は解決しません：単にGoogleからそのプロバイダーに信頼の移行をしただけです。
      - 
        "@type": Question
        name: 脅威モデルが複雑であるべき程度
        acceptedAnswer:
          "@type": Answer
          text: |
            複雑すぎるプライバシーの脅威モデルを説明する人もよくいます。 多くの場合、その解決策は多くのメールアカウントを使うことや不確定要素を含む複雑なセットアップが含まれています。 これは大抵の場合、「Xを行うベストな方法は何か？」という質問に対する回答です。
            「ベスト」な解決策をを見つけることは、必ずしも、たくさんの条件がある絶対に確実な解決策を求めるということではありません。そのようなものは実際に運用することは難しいことが多いです。 先に述べたように、セキュリティは利便性を犠牲にします。
---

## 「オープンソースソフトウェアは常に安全である」もしくは「オープンソースソフトウェアはプロプライエタリソフトウェアよりも安全である」

この神話は多くの先入観から生じているものですが、ソースコードが入手可能かどうかやライセンスは本質的にセキュリティに影響を与えるものではありません。 ==オープンソースソフトウェアはプロプライエタリソフトウェアよりも*潜在的には*安全ですが、絶対的な保証はありません。==ソフトウェアを評価する際には、各ツールの評価や安全性を個別に判断する必要があります。

オープンソースソフトウェアは第三者による監査が*可能*であり、プロプライエタリソフトウェアよりも潜在的な脆弱性について透明性が高いことが多いです。 またコードを確認し、疑わしい機能を自分で無効にすることもできます。 ただし、*自分でしない限り*、特に小規模なソフトウェアプロジェクトでは、コードが評価されているという保証はありません。 オープンな開発プロセスは[:material-package-variant-closed-remove:サプライチェーン攻撃](common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}のような新たな脆弱性を含めることに悪用される場合もあります。詳細は[一般的な脅威](common-threats.md)を参照してください。[^1]

一方で、プロプライエタリソフトウェアは透明性には欠けますが、安全ではないということではありません。 大規模なプロプライエタリソフトウェアは、内部監査や第三者機関による監査を実施することができますし、独立したセキュリティ研究者はリバースエンジニアリングなどの手法で脆弱性を発見することもできます。

偏った判断をしないために、使っているソフトウェアのプライバシーとセキュリティの基準を評価することが*極めて重要*です。

## 「信頼の移行によりプライバシーを向上させることができる」

VPNのようなソリューション（信頼をISPからVPNプロバイダーに移す）について議論が行われる際、「信頼の移行」について話すことが多いです。 *特に*ISPからブラウジングデータは保護される一方で、VPNプロバイダーからはブラウジングデータにアクセスできます：すべての関係者に対して完全に安全を確保できるわけではありません。 つまり：

1. 信頼の移行先のプロバイダーを選ぶには注意が必要である。
2. データを完全に保護するにはエンドツーエンド暗号化のような技術を使うべきである。 単にあるプロバイダーを信頼せず、他のプロバイダーを信頼するだけではデータの安全性は確保できません。

## 「プライバシー重視のソリューションは本質的に信頼できる」

ツールのプライバシーポリシーやマーケティングだけに注目し過ぎるとその弱点が見えなくなります。 よりプライバシーを重視した解決策を探している場合、根本的な問題を見極め、技術的な解決策を見つける必要があります。 例えば、GoogleがすべてのデータにアクセスできるGoogle Driveの利用をやめたいとしましょう。 この場合の根本的な問題はエンドツーエンド暗号化がないことで、乗り換えるプロバイダーに実際にエンドツーエンド暗号化が実装されているか確認するか、どのクラウドサービスプロバイダーでもエンドツーエンド暗号化ができる（[Cryptomator](../encryption.md#cryptomator-cloud)のような）ツールを使用する必要があります。 （エンドツーエンド暗号化がない）「プライバシー重視」のプロバイダーに乗り換えても問題は解決しません：単にGoogleからそのプロバイダーに信頼の移行をしただけです。

選んだプロバイダーのプライバシーポリシーとビジネスは非常に重要ですが、プライバシーの技術的保証に次ぐものと考える必要があります：全く要件を満たさない別のプロバイダーに信頼の移行をすべきではありません。

## 「複雑であるほうがよい」

複雑すぎるプライバシーの脅威モデルを説明する人もよくいます。 多くの場合、その解決策は多くのメールアカウントを使うことや不確定要素を含む複雑なセットアップが含まれています。 これは大抵の場合、「*X*を行うベストな方法は何か？」という質問に対する回答です。

「ベスト」な解決策をを見つけることは、必ずしも、たくさんの条件がある絶対に確実な解決策を求めるということではありません。そのようなものは実際に運用することは難しいことが多いです。 先に述べたように、セキュリティは利便性を犠牲にします。 以下にヒントを示します：

1. ==行動は特定の目的に合う必要がある：==最小限の行動でやりたいことがどうやったらできるか考えてください。
2. ==人が失敗し得る箇所をなくす：==人は失敗したり、疲れたり、忘れたりします。 セキュリティを維持するために、覚えておく必要のある手動条件や手作業に頼らないようにします。
3. ==意図したものを適切なレベルで保護すること。==いわゆる法の執行や召喚令状を防ぐソリューションの推奨がよくあります。 このようなものは通常、一般人が望むものではなく、専門的な知識を必要とします。 単純な監視によって簡単に匿名化を解除されてしまうのであれば、匿名化のために複雑な脅威モデルを作ることは意味がありません。

So, how might this look?

One of the clearest threat models is one where people *know who you are* and one where they do not. There will always be situations where you must declare your legal name and there are others where you don't need to.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Tip</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](../cryptocurrency.md#monero). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added an obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
