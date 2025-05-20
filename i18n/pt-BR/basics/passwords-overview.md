---
title: Introdução às senhas
icon: material/form-textbox-password
description: Aqui estão algumas dicas e truques para que você crie senhas mais seguras e garanta a segurança de suas contas.
---

Senhas são um elemento essencial no dia a dia de nossas vidas digitais. We use them to protect our accounts, our devices, and our secrets. Embora seja na maioria das vezes a única barreira entre nossos dados pessoais e um indivíduo mal intencionado (hacker, golpista, etc.) acabamos por não pensar muito em nossas senhas. Isso leva ao comportamento comum das pessoas em utilizar senhas que são facilmente adivinháveis ou forçadas (através de um software malicioso, por exemplo).

## Práticas recomendadas

### Use **apenas uma ** senha para cada serviço.

Imagine this: You sign up for an account with the same e-mail and password on multiple online services. Se um desses provedores de serviço for malicioso ou ocorrer um vazamento de dados que expõe sua senha em um formato não encriptado (protegido), tudo que um hacker/golpista precisaria era testar sua combinação de e-mail e senha em diversos serviços populares até que o mesmo consiga um acerto. Nesse caso, não interessa o o quão "forte" é uma senha, pois o hacker ou golpista já tem posse dela.

Isso é chamado de [credential stuffing](https://en.wikipedia.org/wiki/Credential_stuffing) e é uma das maneiras mais comuns pelas quais suas contas podem ser comprometidas por agentes mal-intencionados. Para evitar essas situações é necessário certificar-se que você não **reutiliza** nenhuma senha.

### Utilize senhas geradas aleatoreamente (por ferramentas confiáveis)

Você nunca deve confiar em si mesmo para criar uma boa senha. Nós recomendamos que você use senhas  [geradas aleatoramente](#passwords) ou com tecnologia diceware. Estas estarão providas com a entropia suficiente para proteger você, suas contas virtuais e seus dispositivos.

Todos os nossos [gerenciadores de senhas recomendados](../passwords.md) incluem um gerador de senhas integrado.

### Rotação de senhas

Evite alterar as senhas que realmente precisa lembrar (como a senha mestra de seu gerenciador de senhas), a menos que tenha **motivos para acreditar que ela tenha sido comprometida**, pois alterá-la com muita frequência tem risco de você esquecê-la.

Ao se tratar de senhas que você não precisa lembrar (como as senhas armazenadas no gerenciador de senhas), se o seu [gerenciador de riscos](threat-modeling.md) exigir isso, recomendamos que você **examine** suas contas mais importantes (especialmente as contas que não usam autenticação multifator 2FA) e altere a senha delas a cada **dois meses**, caso tenham sido comprometidas em algum vazamento de dados que ainda não foi divulgado. A maioria dos gerenciadores de senha permite que você configure uma data de expiração para determinadas senhas, facilitando a tarefa da rotação de senhas.

<div class="admonition tip" markdown>
<p class="admonition-title">Verificando violações de dados</p>

Se o seu gerenciador de senhas permitir a verificação de contas e senhas comprometidas, certifique-se de fazer isso **e altere imediatamente** qualquer senha que possa ter sido exposta em um vazamento de dados. Você também pode acompanhar o feed [Have I Been Pwned's Latest Breaches](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) com a ajuda de um [agregador de notícias ou cliente RSS](../news-aggregators.md) para obter informações sobre os vazamentos de dados mais recentes.

</div>

## Criando senhas fortes

### Senhas

Vários serviços exigem certos critérios para as senhas de suas contas. Alguns destes podem incluir um número mínimo e/ou máximo de caracteres bem como a inclusão de caracteres especiais ou capitalizados. É recomendado que se use o gerador de senhas contido em seu gerenciador de senhas de preferência. Isso permite uma maior praticidade ao gerar novas senhas que cumprem com os critérios (quantidade de caracteres, letras maiúscula e minúscula, caracteres especiais, etc.) exigidos em cada serviço.

Se você precisar de uma senha que possa memorizar, recomendamos uma [frase Diceware](#diceware-passphrases).

### Frases Diceware

Diceware é um método de criação de senhas e palavras-passe que são fáceis de se lembrar porém difíceis de se adivinhar

As frases Diceware são boas opção quando você precisa memorizar ou inserir manualmente suas credenciais, tal como para a senha mestra do seu gerenciador de senhas ou a senha de proteção do seu dispositivo.

Um exemplo de uma frase secreta de dados é o `fastness reluctant squishy seventeen shown pencil`.

Para gerar frases diceware usando um dado real, siga esses passos:

<div class="admonition Note" markdown>
<p class="admonition-title">Observação:</p>

Essas instruções pressupõem que você esteja usando [a grande lista de palavras da EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) para gerar a frase secreta, o que requer cinco lançamentos de dados por palavra. Outras listas de palavras podem exigir mais ou menos rolagens por palavra e podem exigir uma quantidade diferente de palavras para obter a mesma entropia.

</div>

1. Jogue um dado de seis lados cinco vezes, anotando o número após cada jogada.

2. Por exemplo, digamos que você tenha tirado `2-5-2-6-6`. Procure na [grande lista de palavras da EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) a palavra que corresponde a `25266`.

3. Você encontrará a palavra `encrypt (criptografar`). Anote essa palavra.

4. Repita esse processo até que a frase secreta tenha o número de palavras necessárias, separadas por um espaço.

<div class="admonition warning" markdown>
<p class="admonition-title">Importante</p>

Você não deve **rolar** as palavras até obter uma combinação de palavras que lhe agrade. O processo deve ser completamente aleatório.

</div>

If you don't have access to or would prefer to not use real dice, you can use your password manager's built-in password generator, as most of them have the option to generate diceware passphrases in addition to regular passwords. We recommend setting the generated passphrase length to at least 6 words.

We also recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. Caso você prefira também existem [listas de palavras em diferentes idiomas](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline).

<details class="note" markdown>
<summary>Explicação da entropia e da força das frases diceware</summary>

Para demonstrar a força das frases diceware, usaremos a frasede sete palavras mencionada anteriormente`(viewable fastness reluctant squishy seventeen shown pencil`) e [a grande lista de palavras da EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) como exemplo.

One metric to determine the strength of a diceware passphrase is how much entropy it has. The entropy per word in a diceware passphrase is calculated as <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> and the overall entropy of the passphrase is calculated as: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Therefore, each word in the aforementioned list results in ~12.9 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), and a seven word passphrase derived from it has ~90.47 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, or in our case, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

On average, it takes trying 50% of all the possible combinations to guess your phrase. With that in mind, even if your adversary is capable of ~1,000,000,000,000 guesses per second, it would still take them ~27,255,689 years to guess your passphrase. That is the case even if the following things are true:

- Your adversary knows that you used the diceware method.
- Your adversary knows the specific word list that you used.
- Your adversary knows how many words your passphrase contains.

</details>

To sum it up, diceware passphrases are your best option when you need something that is both easy to remember *and* exceptionally strong.

## Guardando suas senhas

### Gerenciadores de Senhas

A melhor maneira de guardar suas senhas é utilizando um programa gerenciador de senhas. Esse tipo de software é responsável por armazenar localmente ou em 'nuvem' as senhas que você usa em diversos serviços que tem seu acesso garantido através da senha mestre. Desta maneira, você só precisa lembrar uma senha forte, que lhe permitirá acessar ou fazer o preenchimento automático de suas demais senhas.

Existem várias opções boas quando se trata de gerenciadores de senhas, ambas opções locais e baseadas 'na nuvem'. Escolha uma de nossas recomendações de gerenciadores de senhas e utilize-os a fim de produzir senhas mais fortes para suas contas. We recommend securing your password manager with a [diceware passphrase](#diceware-passphrases) comprised of at least seven words.

[Lista de gerenciadores de senhas recomendados.](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Não coloque suas senhas e tokens TOTP no mesmo gerenciador de senhas</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

Storing your TOTP tokens in the same place as your passwords, while convenient, reduces the accounts to a single factor in the event that an adversary gains access to your password manager.

Furthermore, we do not recommend storing single-use recovery codes in your password manager. Those should be stored separately such as in an encrypted container on an offline storage device.

</div>

### Backups

É de extrema importância armazenar backups <0>criptografados</0> de todas as suas senhas em mais de um dispositivo (pendrive, cartão de memória, etc.) ou em um provedor confiável de armazenamento em nuvem. Isso pode ajudá-lo a acessar suas senhas se algo acontecer com seu dispositivo principal ou com o serviço que você está usando.
