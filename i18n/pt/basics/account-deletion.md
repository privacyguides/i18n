---
title: Eliminação de Contas
icon: material/account-remove
description: It's easy to accumulate a large number of internet accounts. Here are some tips on how to prune your collection.
---

Com o passar do tempo, pode ser fácil acumular uma série de contas em linha, muitas das quais podem já não ser utilizadas. A eliminação destas contas não utilizadas é um passo importante para recuperar a sua privacidade, uma vez que as contas inativas são vulneráveis a violações de dados. A data breach occurs when a service's security is compromised and protected information is viewed, transmitted, or stolen by unauthorized actors. Infelizmente, as violações de dados são [demasiado comuns](https://haveibeenpwned.com/PwnedWebsites) atualmente, pelo que praticar uma boa higiene digital é a melhor forma de minimizar o impacto tido na sua vida. The goal of this guide then is to help navigate you through the irksome process of account deletion, often made difficult by [deceptive design](https://deceptive.design), for the betterment of your online presence.

## Encontrar Contas Antigas

### Gestor de Palavras-Passe

Se tiver um gestor de palavras-passe que tenha utilizado durante toda a sua vida digital, esta parte será muito fácil. Oftentimes, they include built-in functionality for detecting if your credentials were exposed in a data breach—such as Bitwarden's [Data Breach Report](https://bitwarden.com/blog/have-you-been-pwned).

<figure markdown>
  ![Funcionalidade do Relatório de Violação de Dados da Bitwarden](../assets/img/account-deletion/exposed_passwords.png)
</figure>

Even if you haven't explicitly used a password manager before, there's a chance you've used the one in your browser ([Firefox](https://support.mozilla.org/kb/password-manager-remember-delete-edit-logins), [Chrome](https://passwords.google.com/intro), [Edge](https://support.microsoft.com/microsoft-edge/save-or-forget-passwords-in-microsoft-edge-b4beecb0-f2a8-1ca0-f26f-9ec247a3f336)) or your phone ([Google](https://passwords.google.com/intro) on stock Android, [Passwords](https://support.apple.com/HT211146) on iOS) without even realizing it.

As plataformas de ambiente de trabalho também têm frequentemente um gestor de palavras-passe que pode ajudá-lo a recuperar palavras-passe esquecidas:

- Windows: [Credential Manager](https://support.microsoft.com/windows/accessing-credential-manager-1b5c916a-6a16-889f-8581-fc16e8165ac0)
- macOS: [Passwords](https://support.apple.com/HT211145)
- Linux: Gnome Keyring (accessed through [Seahorse](https://gitlab.gnome.org/GNOME/seahorse#seahorse)) or [KDE Wallet Manager](https://userbase.kde.org/KDE_Wallet_Manager)

### Correio eletrónico

If you didn't use a password manager in the past, or you think you have accounts that were never added to your password manager, another option is to search the email account(s) that you believe you signed up on. No seu cliente de correio eletrónico, procure palavras-chave como "verificar" ou "bem-vindo." Quase sempre que cria uma conta em linha, o serviço envia uma ligação de verificação ou uma mensagem introdutória para o seu correio eletrónico. Esta pode ser uma boa forma de encontrar contas antigas e esquecidas.

## Eliminar Contas Antigas

### Iniciar Sessão

Para eliminar as contas antigas, tem de se certificar primeiro de que pode iniciar sessão nas mesmas. Mais uma vez, se a conta estava no seu gestor de palavras-passe, este passo é fácil. Caso contrário, pode tentar adivinhar a sua palavra-passe. Caso contrário, normalmente existem opções para recuperar o acesso à sua conta, normalmente disponíveis através de uma ligação "esqueci-me da palavra-passe" na página de início de sessão. Também pode ser possível que as contas que abandonou já tenham sido eliminadas — por vezes, os serviços eliminam todas as contas antigas.

Ao tentar recuperar o acesso, se o sítio web devolver uma mensagem de erro a indicar que o endereço de correio eletrónico não está associado a uma conta, ou se nunca receber uma ligação de reposição após várias tentativas, então não tem uma conta com esse endereço de correio eletrónico e deve tentar um endereço diferente. Se não conseguir descobrir qual o endereço de correio eletrónico que utilizou, ou se já não tiver acesso a esse correio eletrónico, pode tentar contactar o apoio ao cliente do serviço. Infelizmente, não existe nenhuma garantia de que conseguirá recuperar o acesso à sua conta.

### RGPD (somente residentes no EEE)

Residents of the EEA have additional rights regarding data erasure specified in [Article 17](https://gdpr-info.eu/art-17-gdpr) of the GDPR. Se for aplicável ao seu caso, leia a política de privacidade de um determinado serviço para obter informações sobre como exercer o seu direito ao apagamento. A leitura da política de privacidade pode revelar-se importante, uma vez que alguns serviços têm uma opção "Eliminar conta" que apenas desativa a sua conta e, para uma verdadeira eliminação, tem de tomar medidas adicionais. Por vezes, a eliminação efetiva pode implicar o preenchimento de inquéritos, o envio de uma mensagem de correio eletrónico ao responsável pela proteção de dados do serviço ou mesmo a prova da sua residência no EEE. Se pretender seguir este caminho, **não** substitua as informações da conta — a sua identidade como residente no EEE pode ser exigida. Note-se que a localização do serviço não é importante; o RGPD aplica-se a todos os que servem utilizadores europeus. If the service does not respect your right to erasure, you can contact your national [Data Protection Authority](https://ec.europa.eu/info/law/law-topic/data-protection/reform/rights-citizens/redress/what-should-i-do-if-i-think-my-personal-data-protection-rights-havent-been-respected_en) and may be entitled to monetary compensation.

### Subscrever Informações da Conta

Em algumas situações em que planeia abandonar uma conta, pode fazer sentido substituir as informações da conta por dados falsos. Após se certificar de que pode iniciar sessão, altere todas as informações da sua conta para informações falsificadas. A razão para isto é que muitos sítios conservam as informações que tinha anteriormente, mesmo após a eliminação da conta. O objetivo é substituir as informações anteriores pelos dados mais recentes que introduziu. No entanto, não há garantia de que não existam cópias de segurança das informações anteriores.

For the account email, either create a new alternate email account via your provider of choice or create an alias using an [email aliasing service](../email-aliasing.md). Pode então apagar o seu endereço de correio eletrónico alternativo quando tiver terminado. Não recomendamos utilizar fornecedores de correio eletrónico temporários, uma vez que, muitas vezes, é possível reativar correio eletrónico temporário.

### Apagar

Pode consultar [JustDeleteMe](https://justdeleteme.xyz) para obter instruções sobre como eliminar a conta de um serviço específico. Alguns sítios web têm a opção "Eliminar conta", enquanto outros obrigam-no a falar com um agente de apoio. O processo de eliminação pode variar de sítio web para sítio web, sendo a eliminação da conta impossível em alguns.

Para os serviços que não permitem a eliminação da conta, a melhor coisa a fazer é falsificar todas as suas informações, como mencionado anteriormente, e reforçar a segurança da conta. Para o fazer, ative [MFA](multi-factor-authentication.md) e quaisquer funcionalidades de segurança adicionais oferecidas. Além disso, altere a palavra-passe para uma palavra-passe gerada aleatoriamente com o tamanho máximo permitido (um [gestor de palavras-passe](../passwords.md) pode ser útil para este efeito).

Se estiver convencido de que todas as informações que lhe interessam foram removidas, pode esquecer esta conta com segurança. Caso contrário, pode ser uma boa ideia manter as credenciais guardadas com as suas outras palavras-passe e, ocasionalmente, voltar a iniciar sessão para redefinir a palavra-passe.

Mesmo quando é possível eliminar uma conta, não há garantia de que todas as suas informações sejam removidas. De facto, algumas empresas são obrigadas por lei a conservar determinadas informações, nomeadamente quando estão relacionadas com transações financeiras. Na maioria das vezes, o que acontece aos seus dados está fora do seu controlo quando se trata de sítios web e serviços em nuvem.

## Evitar Contas Novas

Como diz o velho ditado, "mais vale um grama de prevenção do que um quilo de cura." Sempre que se sentir tentado a inscrever-se numa nova conta, pergunte a si próprio: "Preciso mesmo disto? Posso fazer o que preciso sem uma conta?" Muitas vezes, pode ser muito mais difícil apagar uma conta do que criar uma. And even after deleting or changing the info on your account, there might be a cached version from a third-party—like the [Internet Archive](https://archive.org). Evite a tentação quando puder — o seu futuro o agradecer-lhe-á!
