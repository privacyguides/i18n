---
meta_title: "How to Create Internet Accounts Privately - Privacy Guides"
title: "Account Creation"
icon: 'material/account-plus'
description: Creating accounts online is practically an internet necessity, take these steps to make sure you stay private.
---

Muitas vezes, as pessoas inscrevem-se em serviços sem pensar. Maybe it's a streaming service to watch that new show everyone's talking about, or an account that gives you a discount for your favorite fast food place. Seja qual for o caso, deve considerar as implicações para os seus dados agora e mais tarde.

Há riscos associados a cada novo serviço que utiliza. Violações de dados; divulgação de informações de clientes a terceiros; acesso de funcionários desonestos aos dados; todas estas são possibilidades que devem ser tidas em conta ao se divulgarem informações. É necessário ter a certeza de que pode confiar no serviço, razão pela qual não recomendamos o armazenamento de dados valiosos em nada que não seja os produtos mais maduros e testados. Isto significa, normalmente, serviços que fornecem E2EE e que foram submetidos a uma auditoria criptográfica. Uma auditoria aumenta a garantia de que o produto foi concebido sem problemas de segurança evidentes causados por um programador inexperiente.

Também pode ser difícil apagar as contas em alguns serviços. Por vezes, [substituir os dados](account-deletion.md#overwriting-account-information) associados a uma conta é possível, mas noutros casos o serviço manterá um histórico completo das alterações à conta.

## Termos de Serviço e Política de Privacidade

Os ToS são as regras que aceita seguir quando utiliza o serviço. Nos serviços de maior dimensão, estas regras são frequentemente aplicadas por sistemas automatizados. Por vezes, estes sistemas automatizados podem cometer erros. For example, you may be banned or locked out of your account on some services for using a VPN or VoIP number. O recurso a estas proibições é muitas vezes difícil e envolve também um processo automatizado, que nem sempre é bem-sucedido. Esta é uma das razões pelas quais não sugerimos a utilização do Gmail para correio eletrónico, por exemplo. O correio eletrónico é crucial para o acesso a outros serviços em que se tenha inscrito.

The Privacy Policy is how the service says they will use your data, and it is worth reading so that you understand how your data will be used. Uma empresa ou organização pode não ser legalmente obrigada a seguir tudo o que está contido na política (depende da jurisdição). Recomendamos que tenha uma ideia das leis locais e do que estas permitem que um fornecedor recolha.

Recomendamos que procure termos específicos como "recolha de dados", "análise de dados", "cookies", "anúncios" ou serviços "de terceiros". Sometimes you will be able to opt out from data collection or from sharing your data, but it is best to choose a service that respects your privacy from the start.

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

Se não quiser fornecer o seu verdadeiro endereço de correio eletrónico a um serviço, tem a opção de utilizar um pseudónimo. We describe them in more detail on our email services recommendation page. Essencialmente, os serviços de alias permitem-lhe gerar novos endereços de correio eletrónico que reencaminham todas as mensagens para o seu endereço principal. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign-up process. Estes podem ser filtrados automaticamente com base no pseudónimo para o qual são enviados.

Se um serviço for comprometido, pode começar a receber mensagens eletrónicas de phishing ou spam no endereço que utilizou para se registar. A utilização de aliases únicos para cada serviço pode ajudar a identificar exatamente qual o serviço comprometido.

[Serviços de aliasing de correio eletrónico recomendados](../email-aliasing.md ""){.md-button}

### "Iniciar a sessão com..." (OAuth)

[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth) is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Sempre que vir algo como "Inicie sessão com o nome do fornecedor **" num formulário de registo, normalmente utiliza o OAuth.

Quando iniciar sessão com o OAuth, será aberta uma página de início de sessão com o fornecedor que escolher, e a sua conta existente e a nova conta serão ligadas. A sua palavra-passe não será partilhada, mas algumas informações básicas serão normalmente partilhadas (pode revê-las durante o pedido de início de sessão). Este processo é necessário sempre que se pretende iniciar sessão na mesma conta.

As principais vantagens são:

- **Security**: You don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials because they are stored with the external OAuth provider. Common OAuth providers like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease-of-use**: Multiple accounts are managed by a single login.

Mas há desvantagens:

- **Privacy**: The OAuth provider you log in with will know the services you use.
- **Centralization**: If the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth can be especially useful in those situations where you could benefit from deeper integration between services. A nossa recomendação é limitar a utilização do OAuth apenas onde for necessário e proteger sempre a conta principal com [MFA](multi-factor-authentication.md).

All the services that use OAuth will be as secure as your underlying OAuth provider's account. Por exemplo, se quiser proteger uma conta com uma chave de hardware, mas esse serviço não suportar chaves de hardware, pode proteger a conta que utiliza com o OAuth com uma chave de hardware, e agora tem essencialmente MFA de hardware em todas as suas contas. No entanto, vale a pena notar que uma autenticação fraca na sua conta de fornecedor OAuth significa que qualquer conta associada a esse início de sessão também será fraca.

There is an additional danger when using *Sign in with Google*, *Facebook*, or another service, which is that typically the OAuth process allows for *bidirectional* data sharing. For example, logging in to a forum with your Twitter account could grant that forum access to do things on your Twitter account such as post, read your messages, or access other personal data. OAuth providers will typically present you with a list of things you are granting the external service access to, and you should always ensure that you read through that list and don't inadvertently grant the external service access to anything it doesn't require.

Malicious applications, particularly on mobile devices where the application has access to the WebView session used for logging in to the OAuth provider, can also abuse this process by hijacking your session with the OAuth provider and gaining access to your OAuth account through those means. Using the *Sign in with* option with any provider should usually be considered a matter of convenience that you only use with services you trust to not be actively malicious.

### Número de telemóvel

Recomendamos que evite serviços que exijam um número de telefone para se registar. A phone number can identify you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

Se possível, deve evitar dar o seu número de telefone verdadeiro. Some services will allow the use of VoIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

Em muitos casos, é necessário fornecer um número a partir do qual possa receber SMS ou chamadas, especialmente em compras internacionais, para o caso de haver um problema com a sua encomenda no controlo fronteiriço. É comum os serviços utilizarem o seu número como método de verificação; não se deixe bloquear numa conta importante porque quis ser esperto e dar um número falso!

### Nome de utilizador e palavra-passe

Alguns serviços permitem-lhe registar-se sem utilizar um endereço de correio eletrónico e apenas lhe exigem a definição de um nome de utilizador e de uma palavra-passe. Estes serviços podem proporcionar um maior anonimato quando combinados com uma VPN ou Tor. Tenha em atenção que, para estas contas, é muito provável que não haja **forma de recuperar a sua conta** caso se esqueça do seu nome de utilizador ou palavra-passe.
