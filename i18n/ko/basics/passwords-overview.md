---
title: 비밀번호 소개
icon: material/form-textbox-password
description: 가장 강력한 비밀번호를 만들고 계정을 안전하게 지키는 데 도움이 되는 몇 가지 팁과 요령입니다.
---

비밀번호는 일상적인 디지털 생활에서 필수적인 요소입니다. 우리는 비밀번호로 계정, 기기, 그리고 비밀을 보호합니다. 비밀번호는 우리의 개인 정보를 노리는 공격자와 우리 사이를 가로막는 유일한 수단인 경우가 많은데도, 사람들은 비밀번호에 그다지 신경을 쓰지 않아 쉽게 추측하거나 무차별 대입 공격으로 알아낼 수 있는 비밀번호를 사용하는 경우가 많습니다.

## 모범 사례 { #best-practices }

### 모든 서비스마다 서로 다른 비밀번호 사용하기 { #use-unique-passwords-for-every-service }

이런 상황을 생각해 보세요. 여러 온라인 서비스에 같은 이메일과 비밀번호로 가입했다고 가정합시다. 그중 한 서비스 제공업체가 악의적이거나, 해당 서비스에서 데이터 유출이 발생해 비밀번호가 암호화되지 않은 형태로 노출된다면, 악의적인 행위자는 성공할 때까지 여러 인기 서비스에 해당 이메일과 비밀번호 조합을 시도해 보기만 하면 됩니다. 이미 비밀번호를 손에 넣었으므로 그 비밀번호가 얼마나 강력한지는 상관없습니다.

이를 [크리덴셜 스터핑](https://en.wikipedia.org/wiki/Credential_stuffing)이라고 하며, 악의적인 행위자가 계정을 탈취하는 가장 흔한 방법 중 하나입니다. 이를 방지하려면 절대 비밀번호를 재사용하지 마세요.

### 무작위로 생성된 비밀번호 사용하기 { #use-randomly-generated-passwords }

==좋은 비밀번호를 스스로 떠올리는 방식에 **절대** 의존해서는 안 됩니다.== 계정과 기기를 보호하려면 충분한 엔트로피를 가진 [무작위로 생성된 비밀번호](#passwords)나 [다이스웨어 패스프레이즈](#diceware-passphrases)를 사용하는 것을 권장합니다.

프라이버시 가이드가 [추천하는 비밀번호 관리자](../passwords.md)는 모두 비밀번호 생성기를 내장하고 있습니다.

### 비밀번호 주기적으로 변경하기 { #rotating-passwords }

비밀번호 관리자의 마스터 비밀번호처럼 기억해야 하는 비밀번호는 유출되었다고 의심할 만한 이유가 없다면 너무 자주 변경하지 않는 것이 좋습니다. 너무 자주 바꾸면 잊어버릴 위험이 있기 때문입니다.

비밀번호 관리자에 저장된 비밀번호처럼 기억할 필요가 없는 비밀번호의 경우, [위협 모델](threat-modeling.md)상 필요하다면 아직 공개되지 않은 데이터 유출로 이미 유출되었을 가능성에 대비하여 중요한 계정(특히 다중 인증을 사용하지 않는 계정)의 비밀번호를 몇 달마다 변경하는 것을 권장합니다. 대부분의 비밀번호 관리자에서는 비밀번호 만료일을 설정할 수 있어 더 쉽게 관리할 수 있습니다.

<div class="admonition tip" markdown>
<p class="admonition-title">데이터 유출 확인하기</p>

비밀번호 관리자에서 유출된 비밀번호 확인 기능을 제공하는 경우, 반드시 해당 기능을 사용해 데이터 유출로 인해 노출됐을 가능성이 있는 비밀번호는 즉시 변경하세요. 또는 [뉴스 애그리게이터](../news-aggregators.md)를 이용해 [Have I Been Pwned의 최신 유출 사고 피드](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches)를 구독할 수도 있습니다.

</div>

## 강력한 비밀번호 만들기 { #creating-strong-passwords }

### 비밀번호 { #passwords }

많은 서비스는 최소/최대 길이나 (사용할 수 있다면) 사용 가능한 특수 문자 등 비밀번호에 일정한 조건을 둡니다. 비밀번호 관리자에 내장된 비밀번호 생성기를 사용하여 대문자, 소문자, 숫자, 특수 문자를 포함해 서비스가 허용하는 한 최대한 길고 복잡한 비밀번호를 만들어야 합니다.

기억해야 하는 비밀번호가 필요하다면 [다이스웨어 패스프레이즈](#diceware-passphrases)를 권장합니다.

### 다이스웨어 패스프레이즈 { #diceware-passphrases }

다이스웨어는 기억하기 쉬우면서도 추측하기는 어려운 패스프레이즈를 만드는 방법입니다.

다이스웨어 패스프레이즈는 비밀번호 관리자의 마스터 비밀번호나 기기 암호화 비밀번호 등 직접 머릿속에 외워둬야 하거나 수동으로 입력해야 하는 비밀번호에 유용합니다.

다이스웨어 패스프레이즈의 예시는 `viewable fastness reluctant squishy seventeen shown pencil`입니다.

실물 주사위를 사용해 다이스웨어 패스프레이즈를 생성하는 방법은 다음과 같습니다:

<div class="admonition Note" markdown>
<p class="admonition-title">참고</p>

이 안내는 패스프레이즈 생성에 [EFF의 대형 단어 목록](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)을 사용한다고 가정하며, 이 목록은 단어 하나당 주사위를 다섯 번 굴려야 합니다. 다른 단어 목록은 단어 하나당 주사위를 굴리는 횟수가 더 많거나 적을 수 있으며, 같은 엔트로피를 얻는 데 필요한 단어 수도 다를 수 있습니다.

</div>

1. 6면체 주사위를 다섯 번 굴리고, 굴릴 때마다 나온 숫자를 적습니다.

2. 예를 들어 `2-5-2-6-6`이 나왔다고 해 봅시다. [EFF의 대형 단어 목록](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)에서 `25266`에 해당하는 단어를 찾습니다.

3. `encrypt`라는 단어가 나옵니다. 이 단어를 적어 둡니다.

4. 패스프레이즈에 필요한 만큼의 단어가 모일 때까지 이 과정을 반복하며, 각 단어는 공백으로 구분합니다.

<div class="admonition warning" markdown>
<p class="admonition-title">중요</p>

마음에 드는 단어 조합이 나올 때까지 주사위를 다시 굴려서는 **안 됩니다**. 이 과정은 완전히 무작위여야 합니다.

</div>

실물 주사위가 없거나 사용하고 싶지 않다면 비밀번호 관리자에 내장된 비밀번호 생성기를 사용할 수 있습니다. 대부분은 일반 비밀번호 외에 다이스웨어 패스프레이즈를 생성하는 옵션도 제공합니다. 생성할 패스프레이즈 길이는 최소 6단어로 설정할 것을 권장합니다.

또한 다이스웨어 패스프레이즈를 생성할 때는 [EFF의 대형 단어 목록](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)을 사용할 것을 권장합니다. 원래 목록과 보안성은 똑같으면서 더 기억하기 쉬운 단어로 구성되어 있기 때문입니다. 패스프레이즈를 영어로 만들고 싶지 않다면 [다른 언어의 단어 목록](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline)도 있습니다.

<details class="note" markdown>
<summary>다이스웨어 패스프레이즈의 엔트로피와 강도에 대한 설명</summary>

다이스웨어 패스프레이즈가 얼마나 강력한지 보여 드리기 위해, 앞서 언급한 7단어 패스프레이즈(`viewable fastness reluctant squishy seventeen shown pencil`)와 [EFF의 대형 단어 목록](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)을 예로 들어 보겠습니다.

다이스웨어 패스프레이즈의 강도를 판단하는 지표 중 하나는 엔트로피가 얼마나 되는지입니다. 다이스웨어 패스프레이즈의 단어당 엔트로피는 다음과 같이 계산되고, <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> 패스프레이즈 전체의 엔트로피는 다음과 같이 계산됩니다: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

따라서 앞서 언급한 목록의 각 단어는 약 12.9비트의 엔트로피를 가지며(<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), 이 목록으로 만든 7단어 패스프레이즈는 약 90.47비트의 엔트로피를 가집니다(<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

[EFF의 대형 단어 목록](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)에는 7776개의 고유한 단어가 있습니다. 가능한 패스프레이즈의 개수는 간단히 다음과 같이 계산할 수 있습니다: <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, 이 예시에서는 <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

이를 실감 나게 표현하자면, [EFF의 대형 단어 목록](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)을 사용한 7단어 패스프레이즈는 약 1,719,070,799,748,422,500,000,000,000개의 가능한 패스프레이즈 중 하나입니다.

평균적으로 패스프레이즈를 알아맞히려면 가능한 모든 조합의 50%를 시도해야 합니다. 이를 고려하면 공격자가 초당 약 1,000,000,000,000번 추측할 수 있다고 해도, 여러분의 패스프레이즈를 알아맞히는 데 약 27,255,689년이 걸립니다. 이는 다음 사항이 모두 사실이라고 해도 마찬가지입니다:

- 공격자가 여러분이 다이스웨어 방식을 사용했다는 것을 알고 있습니다.
- 공격자가 여러분이 사용한 단어 목록을 알고 있습니다.
- 공격자가 여러분의 패스프레이즈가 몇 개의 단어로 이루어져 있는지 알고 있습니다.

</details>

요약하자면, 기억하기 쉬우면서*도* 매우 강력한 것이 필요할 때 다이스웨어 패스프레이즈는 최선의 선택입니다.

## 비밀번호 저장하기 { #storing-passwords }

### 비밀번호 관리자 { #password-managers }

비밀번호를 저장하는 가장 좋은 방법은 비밀번호 관리자를 사용하는 것입니다. 비밀번호 관리자를 사용하면 비밀번호를 파일이나 클라우드에 저장하고 하나의 마스터 비밀번호로 보호할 수 있습니다. 이렇게 하면 강력한 비밀번호 하나만 기억하면 나머지 모든 비밀번호에 접근할 수 있습니다.

클라우드 기반과 로컬 기반 모두 훌륭한 선택지가 많습니다. 추천 비밀번호 관리자 중 하나를 선택하여 모든 계정에 강력한 비밀번호를 설정하세요. 비밀번호 관리자는 최소 7단어로 구성된 [다이스웨어 패스프레이즈](#diceware-passphrases)로 보호할 것을 권장합니다.

[추천 비밀번호 관리자 목록](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">비밀번호와 TOTP 토큰을 같은 비밀번호 관리자에 보관하지 마세요</p>

[다중 인증용 TOTP 코드](multi-factor-authentication.md#time-based-one-time-password-totp)를 사용할 때는 TOTP 코드를 [별도의 앱](../multi-factor-authentication.md)에 보관하는 것이 가장 안전한 방법입니다.

TOTP 토큰을 비밀번호와 같은 곳에 저장하면 편리하지만, 공격자가 비밀번호 관리자에 접근하게 되면 계정 보호가 단일 인증 요소로 줄어들게 됩니다.

또한 일회용 복구 코드를 비밀번호 관리자에 저장하는 것도 권장하지 않습니다. 이러한 정보는 오프라인 저장 장치의 암호화 컨테이너 등에 별도로 보관해야 합니다.

</div>

### 백업 { #backups }

비밀번호의 [암호화된](../encryption.md) 백업을 여러 저장 장치나 클라우드 스토리지 제공업체에 보관해야 합니다. 이렇게 하면 주 기기나 사용 중인 서비스에 문제가 생기더라도 비밀번호에 접근할 수 있습니다.
