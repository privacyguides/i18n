---
meta_title: "How to Create Internet Accounts Privately - Privacy Guides"
title: "Account Creation"
icon: 'material/account-plus'
description: Creating accounts online is practically an internet necessity, take these steps to make sure you stay private.
---

Muitas vezes, as pessoas inscrevem-se em serviços sem pensar. Talvez seja um serviço de streaming para poder ver aquela nova série de que todos falam, ou uma conta que lhe dá um desconto no seu restaurante de fast food favorito. Seja qual for o caso, deve considerar as implicações para os seus dados agora e mais tarde.

Há riscos associados a cada novo serviço que utiliza. Violações de dados; divulgação de informações de clientes a terceiros; acesso de funcionários desonestos aos dados; todas estas são possibilidades que devem ser tidas em conta ao se divulgarem informações. É necessário ter a certeza de que pode confiar no serviço, razão pela qual não recomendamos o armazenamento de dados valiosos em nada que não seja os produtos mais maduros e testados. Isto significa, normalmente, serviços que fornecem E2EE e que foram submetidos a uma auditoria criptográfica. Uma auditoria aumenta a garantia de que o produto foi concebido sem problemas de segurança evidentes causados por um programador inexperiente.

Também pode ser difícil apagar as contas em alguns serviços. Por vezes, [substituir os dados](account-deletion.md#overwriting-account-information) associados a uma conta é possível, mas noutros casos o serviço manterá um histórico completo das alterações à conta.

## Termos de Serviço e Política de Privacidade

Os ToS são as regras que aceita seguir quando utiliza o serviço. Nos serviços de maior dimensão, estas regras são frequentemente aplicadas por sistemas automatizados. Por vezes, estes sistemas automatizados podem cometer erros. Por exemplo, pode ser banido ou bloqueado da sua conta em alguns serviços por utilizar uma VPN, ou VOIP. O recurso a estas proibições é muitas vezes difícil e envolve também um processo automatizado, que nem sempre é bem-sucedido. Esta é uma das razões pelas quais não sugerimos a utilização do Gmail para correio eletrónico, por exemplo. O correio eletrónico é crucial para o acesso a outros serviços em que se tenha inscrito.

A Política de Privacidade é como o serviço diz que irá utilizar os seus dados e vale a pena lê-la para compreender como os seus dados serão utilizados. Uma empresa ou organização pode não ser legalmente obrigada a seguir tudo o que está contido na política (depende da jurisdição). Recomendamos que tenha uma ideia das leis locais e do que estas permitem que um fornecedor recolha.

Recomendamos que procure termos específicos como "recolha de dados", "análise de dados", "cookies", "anúncios" ou serviços "de terceiros". Por vezes, pode optar por não participar na recolha de dados ou na partilha dos seus dados, mas é melhor escolher um serviço que respeite a sua privacidade desde o início.

Não se esqueça de que também está a depositar a sua confiança na empresa ou organização e que esta irá cumprir a sua própria política de privacidade.

## Métodos de autenticação

Normalmente, existem várias formas de registar uma conta, cada uma com as suas próprias vantagens e desvantagens.

### Correio eletrónico + palavra-passe

A forma mais comum de criar uma nova conta é por um endereço de correio eletrónico e de uma palavra-passe. Ao utilizar este método, deve utilizar um gestor de palavras-passe e seguir as [melhores práticas](passwords-overview.md) relativamente a palavras-passe.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Também pode utilizar o seu gestor de palavra-passes para organizar outros métodos de autenticação! Basta adicionar a nova entrada e preencher os campos adequados, pode adicionar notas para coisas como perguntas de segurança ou uma chave de segurança.

</div>

Será responsável pela gestão das suas credenciais de início de sessão. Para maior segurança, pode configurar [MFA](multi-factor-authentication.md) nas suas contas.

[Gestores de palavras-passe recomendados](../passwords.md ""){.md-button}

#### Aliases de correio eletrónico

Se não quiser fornecer o seu verdadeiro endereço de correio eletrónico a um serviço, tem a opção de utilizar um pseudónimo. Descrevemos los com mais pormenor na nossa página de recomendações de serviços de correio eletrónico. Essencialmente, os serviços de alias permitem-lhe gerar novos endereços de correio eletrónico que reencaminham todas as mensagens para o seu endereço principal. Isto pode ajudar a evitar o rastreio entre serviços e ajudá-lo a gerir as mensagens eletrónicas de marketing que, por vezes, acompanham o processo de registo. Estes podem ser filtrados automaticamente com base no pseudónimo para o qual são enviados.

Se um serviço for comprometido, pode começar a receber mensagens eletrónicas de phishing ou spam no endereço que utilizou para se registar. A utilização de aliases únicos para cada serviço pode ajudar a identificar exatamente qual o serviço comprometido.

[Serviços de aliasing de correio eletrónico recomendados](../email-aliasing.md ""){.md-button}

### "Iniciar a sessão com..." (OAuth)

A OAuth é um protocolo de autenticação que permite registar-se num serviço sem partilhar muitas informações com o fornecedor do serviço, se for caso disso, utilizando uma conta existente noutro serviço. Sempre que vir algo como "Inicie sessão com o nome do fornecedor **" num formulário de registo, normalmente utiliza o OAuth.

Quando iniciar sessão com o OAuth, será aberta uma página de início de sessão com o fornecedor que escolher, e a sua conta existente e a nova conta serão ligadas. A sua palavra-passe não será partilhada, mas algumas informações básicas serão normalmente partilhadas (pode revê-las durante o pedido de início de sessão). Este processo é necessário sempre que se pretende iniciar sessão na mesma conta.

As principais vantagens são:

- **Security**: you don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials, because they are stored with the external OAuth provider, which when it comes to services like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Facilidade de utilização**: várias contas são geridas por um único início de sessão.

Mas há desvantagens:

- **Privacidade**: o fornecedor OAuth com o qual inicia sessão conhecerá os serviços que utiliza.
- **Centralization**: if the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth can be especially useful in those situations where you could benefit from deeper integration between services. A nossa recomendação é limitar a utilização do OAuth apenas onde for necessário e proteger sempre a conta principal com [MFA](multi-factor-authentication.md).

All the services that use OAuth will be as secure as your underlying OAuth provider's account. Por exemplo, se quiser proteger uma conta com uma chave de hardware, mas esse serviço não suportar chaves de hardware, pode proteger a conta que utiliza com o OAuth com uma chave de hardware, e agora tem essencialmente MFA de hardware em todas as suas contas. No entanto, vale a pena notar que uma autenticação fraca na sua conta de fornecedor OAuth significa que qualquer conta associada a esse início de sessão também será fraca.

There is an additional danger when using *Sign in with Google*, *Facebook*, or another service, which is that typically the OAuth process allows for *bidirectional* data sharing. For example, logging in to a forum with your Twitter account could grant that forum access to do things on your Twitter account such as post, read your messages, or access other personal data. OAuth providers will typically present you with a list of things you are granting the external service access to, and you should always ensure that you read through that list and don't inadvertently grant the external service access to anything it doesn't require.

Malicious applications, particularly on mobile devices where the application has access to the WebView session used for logging in to the OAuth provider, can also abuse this process by hijacking your session with the OAuth provider and gaining access to your OAuth account through those means. Using the *Sign in with* option with any provider should usually be considered a matter of convenience that you only use with services you trust to not be actively malicious.

### Número de telemóvel

Recomendamos que evite serviços que exijam um número de telefone para se registar. Um número de telefone pode identificá-lo em vários serviços e, dependendo dos acordos de partilha de dados, facilitará o rastreio da sua utilização, especialmente se um desses serviços for violado, dado que o número de telefone é frequentemente **e não** encriptado.

Se possível, deve evitar dar o seu número de telefone verdadeiro. Alguns serviços permitem a utilização de números VOIP, no entanto, estes acionam frequentemente sistemas de deteção de fraudes, fazendo com que uma conta seja bloqueada, pelo que não recomendamos a sua utilização para contas importantes.

Em muitos casos, é necessário fornecer um número a partir do qual possa receber SMS ou chamadas, especialmente em compras internacionais, para o caso de haver um problema com a sua encomenda no controlo fronteiriço. É comum os serviços utilizarem o seu número como método de verificação; não se deixe bloquear numa conta importante porque quis ser esperto e dar um número falso!

### Nome de utilizador e palavra-passe

Alguns serviços permitem-lhe registar-se sem utilizar um endereço de correio eletrónico e apenas lhe exigem a definição de um nome de utilizador e de uma palavra-passe. Estes serviços podem proporcionar um maior anonimato quando combinados com uma VPN ou Tor. Tenha em atenção que, para estas contas, é muito provável que não haja **forma de recuperar a sua conta** caso se esqueça do seu nome de utilizador ou palavra-passe.
