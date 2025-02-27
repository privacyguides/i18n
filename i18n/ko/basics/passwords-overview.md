---
title: "Introduction to Passwords"
icon: 'material/form-textbox-password'
description: These are some tips and tricks on how to create the strongest passwords and keep your accounts secure.
---

'비밀번호'는 우리의 일상 디지털 생활에 있어서 필수적인 요소입니다. 우리는 비밀번호를 통해 계정, 기기, 개인 정보를 보호합니다. 간혹 비밀번호는 우리의 개인 정보를 노리는 공격자와 우리 사이의 유일한 방어 수단임에도 불구하고, 사람들은 비밀번호의 중요성을 심각하게 생각하지 않아 쉽게 추측되거나 무차별 대입 공격에 취약한 비밀번호를 사용하는 경우가 흔합니다.

## 모범 사례

### 모든 서비스마다 서로 다른 비밀번호 사용하기

여러분이 여러 온라인 서비스에 똑같은 이메일, 비밀번호로 가입했다고 가정해봅시다. 서비스 제공 업체 중 하나가 악의적이거나, 해당 서비스에서 데이터 유출 사고가 발생해 비밀번호가 암호화되지 않은 형식으로 노출될 경우, 악의적인 공격자는 여러 유명 서비스에서 해당 이메일과 비밀번호 조합을 시도해 성공할 때까지 기다리기만 하면 됩니다. 비밀번호를 이미 알아낸 상태이기 때문에, 비밀번호가 얼마나 강력한지는 중요하지 않습니다.

이를 [크리덴셜 스터핑(Credential stuffing)](https://en.wikipedia.org/wiki/Credential_stuffing)이라 하며, 악의적인 공격자가 계정을 탈취하는 굉장히 흔한 방법 중 하나입니다. 이를 방지하려면 비밀번호를 재사용하지 말아야 합니다.

### 무작위로 생성된 비밀번호 사용하기

==좋은 비밀번호를 만들고자 한다면, **절대** 스스로에게 의존해서는 안 됩니다.== 계정 및 기기를 보호할 만큼 충분한 엔트로피를 갖춘 비밀번호를 만들려면 [랜덤 생성된 패스워드](#passwords)나 [Diceware 패스프레이즈](#diceware-passphrases) 방식을 사용하실 것을 권장드립니다.

저희가 [권장하는 비밀번호 관리자](../passwords.md)는 전부 비밀번호 생성기를 내장하고 있습니다.

### 비밀번호 변경

비밀번호 관리자의 마스터 비밀번호처럼 머릿속에 외워둬야 하는 비밀번호는 유출이 발생했다고 판단되지 않는 한 자주 변경하지 않는 편이 좋습니다. 잊어버릴 위험성이 높아지기 때문입니다.

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multifactor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. 대부분의 비밀번호 관리자는 비밀번호 만료일 설정 기능을 제공하기 때문에 더욱 관리하기 쉽습니다.

<div class="admonition tip" markdown>
<p class="admonition-title">Checking for data breaches</p>

비밀번호 관리자에서 유출된 비밀번호 확인 기능을 제공하는 경우, 반드시 해당 기능을 사용해 데이터 유출로 인해 노출됐을 가능성이 있는 비밀번호는 즉시 변경하세요. 혹은 [뉴스 애그리게이터](../news-aggregators.md)를 이용해 [내가 겪은 최근 유출 사례(Have I Been Pwned's Latest Breaches feed)](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches)를 팔로우 해두는 방법도 있습니다.

</div>

## 강력한 비밀번호 만들기

### 패스워드

많은 서비스는 최소/최대 길이, 사용 가능한 특수 문자 등 패스워드(Password)에 특정 제한이 존재합니다. 비밀번호 관리자에 내장된 비밀번호 생성기를 사용해 해당 서비스에서 허용되는 한도 내에서 최대한 길고 복잡한(대문자, 소문자, 숫자, 특수 문자를 포함한) 패스워드를 만들어야 합니다.

외워두어야 하는 비밀번호의 경우, [Diceware 패스프레이즈](#diceware-passphrases) 방식으로 생성할 것을 권장합니다.

### Diceware 패스프레이즈

다이스웨어(Diceware) 방식을 사용하면 기억하기 쉬우면서도 추측하기는 어려운 패스프레이즈(Passphrase)를 만들 수 있습니다.

다이스웨어 패스프레이즈는 비밀번호 관리자의 마스터 비밀번호나 기기 암호화 비밀번호 등 직접 머릿속에 외워둬야 하거나 수동으로 입력해야 하는 비밀번호에 유용합니다.

다이스웨어 패스프레이즈의 예시는 이와 같습니다. `viewable fastness reluctant squishy seventeen shown pencil`

실물 주사위를 사용해 다이스웨어 패스프레이즈를 생성하는 방법은 다음과 같습니다:

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

These instructions assume that you are using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other word lists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

</div>

1. 6면체 주사위를 5번 굴려서 각 주사위를 굴릴 때마다 숫자를 적습니다.

2. 예를 들어, `2-5-2-6-6`가 나왔다고 가정해 보겠습니다. Look through the [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. `encrypt` 단어를 찾았습니다. 이 단어를 받아 적습니다.

4. 원하는 개수의 단어를 얻을 때까지 이 과정을 반복하고, 각 단어는 공백으로 구분합니다.

<div class="admonition warning" markdown>
<p class="admonition-title">Important</p>

단어 조합이 마음에 들지 않는다는 이유로 단어를 다시 선택해서는 **안 됩니다**. 패스프레이즈 생성 과정은 완전히 랜덤으로 진행되어야 합니다.

</div>

실물 주사위가 없거나 사용하고 싶지 않은 경우, 비밀번호 관리자에 내장된 비밀번호 생성기를 사용하면 됩니다. 대부분의 비밀번호 관리자는 일반적인 패스워드 방식뿐만 아니라 다이스웨어 패스프레이즈도 지원합니다.

We recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [word lists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

<details class="note" markdown>
<summary>Explanation of entropy and strength of diceware passphrases</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

One metric to determine the strength of a diceware passphrase is how much entropy it has. The entropy per word in a diceware passphrase is calculated as <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> and the overall entropy of the passphrase is calculated as: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Therefore, each word in the aforementioned list results in ~12.9 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), and a seven word passphrase derived from it has ~90.47 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, or in our case, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

평균적으로, 누군가의 패스프레이즈를 알아맞히려면 가능한 모든 조합의 50%를 시도해야만 합니다. 이 점을 고려하여 계산해보면 공격자가 만약 초당 1,000,000,000,000번 시도한다고 가정해도 여러분의 패스프레이즈를 알아맞히는 데에는 27,255,689년이 걸립니다. 심지어 이는 다음 조건을 충족하는 경우의 이야기입니다:

- 여러분이 다이스웨어 방식을 사용했다는 점을 공격자가 알고 있습니다.
- Your adversary knows the specific word list that you used.
- 여러분의 패스프레이즈 단어 개수를 공격자가 알고 있습니다.

</details>

요약하자면, 기억하기 쉬우면서*도* 매우 강력한 비밀번호가 필요할 경우에는 다이스웨어 패스프레이즈가 최선의 선택입니다.

## 비밀번호 저장

### 비밀번호 관리자

비밀번호를 저장하는 가장 좋은 방법은 비밀번호 관리자를 사용하는 것입니다. 파일이나 클라우드에 비밀번호들을 저장하고 마스터 비밀번호 하나로 보호할 수 있습니다. 이로써, 강력한 비밀번호 하나만 외워두면 모든 비밀번호를 관리할 수 있습니다.

클라우드 기반, 로컬 기반 각각 훌륭한 선택지가 여럿 있습니다. 권장 비밀번호 관리자 중 하나를 선택해 모든 계정의 비밀번호를 강력하게 설정하세요. 비밀번호 관리자 마스터 비밀번호는 [다이스웨어 패스프레이즈](#diceware-passphrases)를 사용하여 7개 단어 이상으로 구성할 것을 권장드립니다.

[권장 비밀번호 관리자 목록](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Don't place your passwords and TOTP tokens inside the same password manager</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

TOTP 토큰과 비밀번호를 한 곳에서 관리하면 편리하지만, 만약 공격자가 여러분의 비밀번호 관리자에 접근 가능할 경우 다중 인증은 무용지물이 됩니다.

일회용 복구 코드 또한 비밀번호 관리자에 저장하지 말 것을 권장드립니다. 이러한 정보는 오프라인 저장 장치의 암호화 컨테이너 등에 별도로 보관해야 합니다.

</div>

### 백업

비밀번호를 [암호화하여](../encryption.md) 백업하고 여러 저장 장치 혹은 클라우드 서비스에 저장해야 합니다. 이렇게 함으로써 주로 사용하는 기기나 이용하는 서비스에 문제가 생기더라도 자신의 비밀번호에 접근할 수 있습니다.
