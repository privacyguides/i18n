---
meta_title: "Comment créer des comptes internet de façon privée - Privacy Guides"
title: "Création de compte"
icon: 'material/account-plus'
description: La création de comptes en ligne est pratiquement une nécessité sur internet, prenez ces mesures pour vous assurer de rester privé.
---

Souvent, les gens s'inscrivent à des services sans réfléchir. Maybe it's a streaming service to watch that new show everyone's talking about, or an account that gives you a discount for your favorite fast food place. Quoi qu'il en soit, vous devez tenir compte des implications pour vos données, maintenant et plus tard.

Chaque nouveau service que vous utilisez comporte des risques. Les fuites de données, la divulgation d'informations sur les clients à des tiers, l'accès à des données par des employés véreux sont autant de possibilités qui doivent être envisagées avant de founir vos informations. Vous devez être sûr que vous pouvez faire confiance au service, c'est pourquoi nous ne recommandons pas de stocker des données précieuses sur autre chose que les produits les plus matures et les plus éprouvés. Il s'agit généralement de services qui fournissent E2EE et qui ont fait l'objet d'un audit cryptographique. Un audit renforce l'assurance que le produit a été conçu sans problèmes de sécurité flagrants causés par un développeur inexpérimenté.

Il peut également être difficile de supprimer les comptes sur certains services. Il est parfois possible [d'écraser les données](account-deletion.md#overwriting-account-information) associées à un compte, mais dans d'autres cas, le service conservera un historique complet des modifications apportées au compte.

## Conditions Générales d'Utilisation & Politique de Confidentialité

Les CGU sont les règles que vous acceptez de suivre lorsque vous utilisez le service. Dans les grands services, ces règles sont souvent appliquées par des systèmes automatisés. Parfois, ces systèmes automatisés peuvent faire des erreurs. For example, you may be banned or locked out of your account on some services for using a VPN or VoIP number. Il est souvent difficile de faire appel de ces interdictions, et cela implique également une procédure automatisée, qui n'aboutit pas toujours. C'est l'une des raisons pour lesquelles nous ne suggérons pas d'utiliser Gmail pour la messagerie électronique, par exemple. L'e-mail est essentiel pour accéder à d'autres services auxquels vous avez peut-être souscrit.

The Privacy Policy is how the service says they will use your data, and it is worth reading so that you understand how your data will be used. Une entreprise ou une organisation peut ne pas être légalement obligée de suivre tout ce qui est contenu dans la politique (cela dépend de la juridiction). Nous vous recommandons d'avoir une idée de la législation locale et de ce qu'elle autorise un prestataire à collecter.

Nous vous recommandons de rechercher des termes particuliers tels que "collecte de données", "analyse de données", "cookies", "annonces", "publicité" ou services "tiers". Sometimes you will be able to opt out from data collection or from sharing your data, but it is best to choose a service that respects your privacy from the start.

Vous faites également confiance à l'entreprise ou à l'organisation pour se conformer à sa propre politique de confidentialité.

## Méthodes d'authentification

Il existe généralement plusieurs façons de créer un compte, chacune ayant ses propres avantages et inconvénients.

### E-mail et mot de passe

Le moyen le plus courant de créer un nouveau compte est d'utiliser une adresse e-mail et un mot de passe. Lorsque vous utilisez cette méthode, vous devriez utiliser un gestionnaire de mots de passe et suivre les [bonnes pratiques](passwords-overview.md) concernant les mots de passe.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Vous pouvez également utiliser votre gestionnaire de mots de passe pour gérer d'autres méthodes d'authentification ! Il suffit d'ajouter la nouvelle entrée et de remplir les champs appropriés. Vous pouvez ajouter des notes pour des choses comme des questions de sécurité ou une clé de secours.

</div>

Vous serez responsable de la gestion de vos identifiants de connexion. Pour plus de sécurité, vous pouvez configurer [MFA](multi-factor-authentication.md) sur vos comptes.

[Gestionnaires de mots de passe recommandés](../passwords.md ""){.md-button}

#### Alias d'e-mail

Si vous ne voulez pas donner votre véritable adresse e-mail à un service, vous avez la possibilité d'utiliser un alias. We describe them in more detail on our email services recommendation page. Essentiellement, les services d'alias vous permettent de créer de nouvelles adresses e-mail qui transmettent tous les courriers à votre adresse principale. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign-up process. Ceux-ci peuvent être filtrés automatiquement en fonction de l'alias auquel ils sont envoyés.

Si un service est piraté, vous pouvez commencer à recevoir des e-mails d'hameçonnage ou de spam à l'adresse que vous avez utilisée pour vous inscrire. L'utilisation d'alias uniques pour chaque service peut aider à identifier exactement quel service a été piraté.

[Services d'alias d'e-mail recommandés](../email-aliasing.md ""){.md-button}

### "Se connecter avec..." (OAuth)

[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth) is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Chaque fois que vous voyez quelque chose du type "Se connecter avec *nom du fournisseur*" sur un formulaire d'inscription, c'est généralement qu'il utilise OAuth.

Lorsque vous vous connectez avec OAuth, une page de connexion s'ouvre avec le fournisseur que vous avez choisi, et votre compte existant et votre nouveau compte seront connectés. Votre mot de passe ne sera pas communiqué, mais certaines informations de base le seront généralement (vous pouvez les consulter lors de la demande de connexion). Ce processus est nécessaire chaque fois que vous voulez vous connecter au même compte.

Les principaux avantages sont les suivants :

- **Security**: You don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials because they are stored with the external OAuth provider. Common OAuth providers like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease-of-use**: Multiple accounts are managed by a single login.

Mais il y a des inconvénients :

- **Privacy**: The OAuth provider you log in with will know the services you use.
- **Centralization**: If the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

L'OAuth peut être particulièrement utile dans les situations où vous pourriez bénéficier d'une intégration plus poussée entre les services. Nous recommandons de limiter l'utilisation d'OAuth aux seuls cas où vous en avez besoin et de toujours protéger le compte principal à l'aide de [MFA](multi-factor-authentication.md).

Tous les services qui utilisent OAuth seront aussi sûrs que le compte de votre fournisseur OAuth sous-jacent. Par exemple, si vous souhaitez sécuriser un compte avec une clé matérielle, mais que ce service ne prend pas en charge les clés matérielles, vous pouvez sécuriser le compte que vous utilisez avec OAuth avec une clé matérielle à la place, et vous disposez alors d'une MFA matérielle sur tous vos comptes. Il convient toutefois de noter qu'une authentification faible sur votre compte de fournisseur OAuth signifie que tout compte lié à cette connexion sera également faiblement sécurisé.

L'utilisation de *Se connecter avec Google*, *Facebook*, ou d'un autre service présente un danger supplémentaire qui est que le processus OAuth permet généralement un partage *bidirectionnel* des données. Par exemple, le fait de vous connecter à un forum avec votre compte Twitter pourrait permettre à ce forum de faire des choses sur votre compte Twitter, comme poster, lire vos messages ou accéder à d'autres données personnelles. Les fournisseurs OAuth vous présenteront généralement une liste des éléments auxquels vous accordez l'accès au service externe, et vous devez toujours veiller à lire cette liste et à ne pas accorder par inadvertance au service externe l'accès à des éléments dont il n'a pas besoin.

Des applications malveillantes, en particulier sur les appareils mobiles où l'application a accès à la session WebView utilisée pour se connecter au fournisseur OAuth, peuvent également abuser de ce processus en détournant votre session avec le fournisseur OAuth et en accédant à votre compte OAuth par ce biais. L'utilisation de l'option *Se connecter avec* avec n'importe quel fournisseur doit généralement être considérée comme une question de commodité que vous n'utilisez qu'avec des services dont vous êtes sûrs qu'ils ne sont pas activement malveillants.

### Numéro de téléphone

Nous vous recommandons d'éviter les services qui exigent un numéro de téléphone pour l'inscription. A phone number can identify you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

Vous devriez éviter de donner votre vrai numéro de téléphone si vous le pouvez. Some services will allow the use of VoIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

Dans de nombreux cas, vous devrez fournir un numéro à partir duquel vous pourrez recevoir des SMS ou des appels, en particulier lorsque vous effectuez des achats à l'étranger, au cas où votre commande rencontrerait un problème lors du contrôle aux frontières. Il est courant que les services utilisent votre numéro comme méthode de vérification ; ne vous faites pas bloquer un compte important parce que vous avez voulu être malin et donner un faux numéro !

### Nom d'utilisateur et mot de passe

Certains services vous permettent de vous inscrire sans utiliser d'adresse électronique et vous demandent seulement de définir un nom d'utilisateur et un mot de passe. Ces services peuvent offrir un anonymat accru lorsqu'ils sont associés à un VPN ou à Tor. Gardez à l'esprit que pour ces comptes, il n'y aura très probablement **aucun moyen de récupérer votre compte** au cas où vous oublieriez votre nom d'utilisateur ou votre mot de passe.
