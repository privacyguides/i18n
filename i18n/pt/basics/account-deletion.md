---
title: "Eliminação de Contas"
icon: 'material/account-remove'
description: É fácil acumular um grande número de contas na Internet. Eis algumas dicas sobre como reduzir a sua coleção.
---

Com o passar do tempo, pode ser fácil acumular uma série de contas em linha, muitas das quais podem já não ser utilizadas. A eliminação destas contas não utilizadas é um passo importante para recuperar a sua privacidade, uma vez que as contas inativas são vulneráveis a violações de dados. Uma violação de dados ocorre quando a segurança de um serviço é comprometida e as informações protegidas são visualizadas, transmitidas ou roubadas por pessoas não autorizadas. Infelizmente, as violações de dados são [demasiado comuns](https://haveibeenpwned.com/PwnedWebsites) atualmente, pelo que praticar uma boa higiene digital é a melhor forma de minimizar o impacto tido na sua vida. O objetivo deste guia é ajudá-lo a navegar pelo processo incómodo de eliminação de contas, muitas vezes dificultado pelo [design enganador](https://www.deceptive.design/), para melhorar a sua presença online.

## Encontrar Contas Antigas

### Gestor de Palavras-Passe

Se tiver um gestor de palavras-passe que tenha utilizado durante toda a sua vida digital, esta parte será muito fácil. Muitas vezes, incluem funcionalidades incorporadas para detetar se as suas credenciais foram expostas numa violação de dados — como o Relatório de violação de dados [da Bitwarden](https://bitwarden.com/blog/have-you-been-pwned/).

<figure markdown>
  ![Funcionalidade do Relatório de Violação de Dados da Bitwarden](../assets/img/account-deletion/exposed_passwords.png)
</figure>

Mesmo que nunca tenha utilizado explicitamente um gestor de palavras-passe, é provável que já o tenha feito no seu navegador ou no seu telemóvel sem se aperceber. Por exemplo: [Gestor de Palavras-Passe da Google](https://support.mozilla.org/kb/password-manager-remember-delete-edit-logins), [Gestor de Palavras-Passe da Google](https://passwords.google.com/intro) e [Gestor de Palavras-Passe da Google](https://support.microsoft.com/en-us/microsoft-edge/save-or-forget-passwords-in-microsoft-edge-b4beecb0-f2a8-1ca0-f26f-9ec247a3f336).

As plataformas de ambiente de trabalho também têm frequentemente um gestor de palavras-passe que pode ajudá-lo a recuperar palavras-passe esquecidas:

- [Gestor de Credenciais](https://support.microsoft.com/en-us/windows/accessing-credential-manager-1b5c916a-6a16-889f-8581-fc16e8165ac0) Windows
- [Palavras-passe](https://support.apple.com/en-us/HT211145) macOS
- [Palavras-passe](https://support.apple.com/en-us/HT211146) iOS
- Linux, Gnome Keyring, que pode ser acedido através de [Seahorse](https://wiki.gnome.org/Apps/Seahorse) ou [KDE Wallet Manager](https://userbase.kde.org /KDE_Wallet_Manager)

### Correio eletrónico

Se não utilizou um gestor de palavras-passe no passado ou se pensa que tem contas que nunca foram adicionadas ao seu gestor de palavras-passe, outra opção é pesquisar a(s) conta(s) de correio eletrónico em que pensa ter-se registado. No seu cliente de correio eletrónico, procure palavras-chave como "verificar" ou "bem-vindo." Quase sempre que cria uma conta em linha, o serviço envia uma ligação de verificação ou uma mensagem introdutória para o seu correio eletrónico. Esta pode ser uma boa forma de encontrar contas antigas e esquecidas.

## Eliminar Contas Antigas

### Iniciar Sessão

Para eliminar as contas antigas, tem de se certificar primeiro de que pode iniciar sessão nas mesmas. Mais uma vez, se a conta estava no seu gestor de palavras-passe, este passo é fácil. Caso contrário, pode tentar adivinhar a sua palavra-passe. Caso contrário, normalmente existem opções para recuperar o acesso à sua conta, normalmente disponíveis através de uma ligação "esqueci-me da palavra-passe" na página de início de sessão. Também pode ser possível que as contas que abandonou já tenham sido eliminadas — por vezes, os serviços eliminam todas as contas antigas.

Ao tentar recuperar o acesso, se o sítio web devolver uma mensagem de erro a indicar que o endereço de correio eletrónico não está associado a uma conta, ou se nunca receber uma ligação de reposição após várias tentativas, então não tem uma conta com esse endereço de correio eletrónico e deve tentar um endereço diferente. Se não conseguir descobrir qual o endereço de correio eletrónico que utilizou, ou se já não tiver acesso a esse correio eletrónico, pode tentar contactar o apoio ao cliente do serviço. Infelizmente, não existe nenhuma garantia de que conseguirá recuperar o acesso à sua conta.

### RGPD (somente residentes no EEE)

Os residentes do EEE têm direitos adicionais relativamente à eliminação de dados especificados em [Artigo 17](https://www.gdpr.org/regulation/article-17.html) do RGPD. Se for aplicável ao seu caso, leia a política de privacidade de um determinado serviço para obter informações sobre como exercer o seu direito ao apagamento. A leitura da política de privacidade pode revelar-se importante, uma vez que alguns serviços têm uma opção "Eliminar conta" que apenas desativa a sua conta e, para uma verdadeira eliminação, tem de tomar medidas adicionais. Sometimes actual deletion may involve filling out surveys, emailing the data protection officer of the service or even proving your residence in the EEA. If you plan to go this way, do **not** overwrite account information—your identity as an EEA resident may be required. Note that the location of the service does not matter; GDPR applies to anyone serving European users. If the service does not respect your right to erasure, you can contact your national [Data Protection Authority](https://ec.europa.eu/info/law/law-topic/data-protection/reform/rights-citizens/redress/what-should-i-do-if-i-think-my-personal-data-protection-rights-havent-been-respected_en) and you may be entitled to monetary compensation.

### Overwriting Account information

In some situations where you plan to abandon an account, it may make sense to overwrite the account information with fake data. Once you've made sure you can log in, change all the information in your account to falsified information. The reason for this is that many sites will retain information you previously had even after account deletion. The hope is that they will overwrite the previous information with the newest data you entered. However, there is no guarantee that there won't be backups with the prior information.

For the account email, either create a new alternate email account via your provider of choice or create an alias using an [email aliasing service](../email.md#email-aliasing-services). You can then delete your alternate email address once you are done. We recommend against using temporary email providers, as oftentimes it is possible to reactivate temporary emails.

### Delete

You can check [JustDeleteMe](https://justdeleteme.xyz) for instructions on deleting the account for a specific service. Some sites will graciously have a "Delete Account" option, while others will go as far as to force you to speak with a support agent. The deletion process can vary from site to site, with account deletion being impossible on some.

For services that don't allow account deletion, the best thing to do is falsify all your information as previously mentioned and strengthen account security. To do so, enable [MFA](multi-factor-authentication.md) and any extra security features offered. As well, change the password to a randomly-generated one that is the maximum allowed size (a [password manager](../passwords.md) can be useful for this).

If you're satisfied that all information you care about is removed, you can safely forget about this account. If not, it might be a good idea to keep the credentials stored with your other passwords and occasionally re-login to reset the password.

Even when you are able to delete an account, there is no guarantee that all your information will be removed. In fact, some companies are required by law to keep certain information, particularly when related to financial transactions. It's mostly out of your control what happens to your data when it comes to websites and cloud services.

## Avoid New Accounts

As the old saying goes, "an ounce of prevention is worth a pound of cure." Whenever you feel tempted to sign up for a new account, ask yourself, "Do I really need this? Can I accomplish what I need to without an account?" It can often be much harder to delete an account than to create one. And even after deleting or changing the info on your account, there might be a cached version from a third-party—like the [Internet Archive](https://archive.org/). Avoid the temptation when you're able to—your future self will thank you!
