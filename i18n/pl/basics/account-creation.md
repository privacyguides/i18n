---
meta_title: "Jak prywatnie zakładać konta w Internecie — Privacy Guides"
title: "Zakładanie konta"
icon: 'material/account-plus'
description: Zakładanie kont w sieci to niemal konieczność — wykonaj poniższe kroki, aby upewnić się, że zachowujesz prywatność.
---

Często ludzie rejestrują się w usługach bez zastanowienia. Może to być serwis streamingowy, żeby obejrzeć nowy serial, o którym wszyscy mówią, albo konto, które daje zniżkę w ulubionej sieci fast food. Niezależnie od powodu, warto przemyśleć konsekwencje dla swoich danych — teraz i w przyszłości.

Każda nowa usługa, z której korzystasz, niesie ze sobą ryzyko. Naruszenia danych, ujawnienie informacji o klientach stronom trzecim, dostęp do danych przez nieuczciwych pracowników — to wszystko to realne możliwości, które trzeba brać pod uwagę, podając swoje dane. Musisz mieć pewność, że możesz zaufać danej usłudze, dlatego nie zalecamy przechowywania cennych danych nigdzie indziej niż na najbardziej dojrzałych i sprawdzonych produktach. Zazwyczaj chodzi o usługi oferujące szyfrowanie E2EE i poddane audytowi kryptograficznemu. Audyt zwiększa pewność, że produkt został zaprojektowany bez rażących błędów bezpieczeństwa wynikających z braku doświadczenia twórców.

Usunięcie konta w niektórych usługach też bywa trudne. Czasem możliwe jest [nadpisanie danych](account-deletion.md#overwriting-account-information) powiązanych z kontem, ale w innych przypadkach usługa będzie przechowywać całą historię zmian konta.

## Warunki korzystania z usługi i polityka prywatności

Warunki korzystania z usługi (ToS) to zasady, których zgadzasz się przestrzegać, korzystając z serwisu. W większych usługach te zasady często egzekwowane są przez systemy zautomatyzowane. Czasami takie systemy popełniają błędy. Na przykład możesz zostać zbanowany lub zablokowany na swoim koncie za korzystanie z VPN lub numeru VoIP. Odwoływanie się od takich banów jest często trudne i również przebiega automatycznie, co nie zawsze kończy się sukcesem. To jedna z przyczyn, dla których nie zalecamy używania Gmaila jako przykładowej skrzynki e-mail. Email is crucial for access to other services you might have signed up for.

The Privacy Policy is how the service says they will use your data, and it is worth reading so that you understand how your data will be used. A company or organization might not be legally obligated to follow everything contained in the policy (it depends on the jurisdiction). We would recommend having some idea what your local laws are and what they permit a provider to collect.

We recommend looking for particular terms such as "data collection", "data analysis", "cookies", "ads" or "3rd-party" services. Sometimes you will be able to opt out from data collection or from sharing your data, but it is best to choose a service that respects your privacy from the start.

Keep in mind you're also placing your trust in the company or organization and that they will comply with their own privacy policy.

## Authentication methods

There are usually multiple ways to sign up for an account, each with their own benefits and drawbacks.

### Email and password

The most common way to create a new account is by an email address and password. When using this method, you should use a password manager and follow [best practices](passwords-overview.md) regarding passwords.

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

You can use your password manager to organize other authentication methods too! Just add the new entry and fill the appropriate fields, you can add notes for things like security questions or a backup key.

</div>

You will be responsible for managing your login credentials. For added security, you can set up [MFA](multi-factor-authentication.md) on your accounts.

[Recommended password managers](../passwords.md ""){.md-button}

#### Email aliases

If you don't want to give your real email address to a service, you have the option to use an alias. We describe them in more detail on our email services recommendation page. Essentially, alias services allow you to generate new email addresses that forward all emails to your main address. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign-up process. Those can be filtered automatically based on the alias they are sent to.

Should a service get hacked, you might start receiving phishing or spam emails to the address you used to sign up. Using unique aliases for each service can assist in identifying exactly what service was hacked.

[Recommended email aliasing services](../email-aliasing.md ""){.md-button}

### "Sign in with..." (OAuth)

[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth) is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Whenever you see something along the lines of "Sign in with *provider name*" on a registration form, it's typically using OAuth.

When you sign in with OAuth, it will open a login page with the provider you choose, and your existing account and new account will be connected. Your password won't be shared, but some basic information typically will (you can review it during the login request). This process is needed every time you want to log in to the same account.

The main advantages are:

- **Security**: You don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials because they are stored with the external OAuth provider. Common OAuth providers like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease-of-use**: Multiple accounts are managed by a single login.

But there are disadvantages:

- **Privacy**: The OAuth provider you log in with will know the services you use.
- **Centralization**: If the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth can be especially useful in those situations where you could benefit from deeper integration between services. Our recommendation is to limit using OAuth to only where you need it, and always protect the main account with [MFA](multi-factor-authentication.md).

All the services that use OAuth will be as secure as your underlying OAuth provider's account. For example, if you want to secure an account with a hardware key, but that service doesn't support hardware keys, you can secure the account you use with OAuth with a hardware key instead, and now you essentially have hardware MFA on all your accounts. It is worth noting though that weak authentication on your OAuth provider account means that any account tied to that login will also be weak.

There is an additional danger when using *Sign in with Google*, *Facebook*, or another service, which is that typically the OAuth process allows for *bidirectional* data sharing. For example, logging in to a forum with your Twitter account could grant that forum access to do things on your Twitter account such as post, read your messages, or access other personal data. OAuth providers will typically present you with a list of things you are granting the external service access to, and you should always ensure that you read through that list and don't inadvertently grant the external service access to anything it doesn't require.

Malicious applications, particularly on mobile devices where the application has access to the WebView session used for logging in to the OAuth provider, can also abuse this process by hijacking your session with the OAuth provider and gaining access to your OAuth account through those means. Using the *Sign in with* option with any provider should usually be considered a matter of convenience that you only use with services you trust to not be actively malicious.

### Phone number

We recommend avoiding services that require a phone number for sign up. A phone number can identify you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

You should avoid giving out your real phone number if you can. Some services will allow the use of VoIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

In many cases you will need to provide a number that you can receive SMS or calls from, particularly when shopping internationally, in case there is a problem with your order at border screening. It's common for services to use your number as a verification method; don't let yourself get locked out of an important account because you wanted to be clever and give a fake number!

### Username and password

Some services allow you to register without using an email address and only require you to set a username and password. These services may provide increased anonymity when combined with a VPN or Tor. Keep in mind that for these accounts there will most likely be **no way to recover your account** in the event you forget your username or password.
