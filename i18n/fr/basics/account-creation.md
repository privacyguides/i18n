---
meta_title: "Comment créer des comptes internet de façon privée - Privacy Guides"
title: "Création de compte"
icon: 'material/account-plus'
description: La création de comptes en ligne est pratiquement une nécessité sur internet, prenez ces mesures pour vous assurer de rester privé.
---

Souvent, les gens s'inscrivent à des services sans réfléchir. Il s'agit peut-être d'un service de streaming qui vous permet de regarder la nouvelle émission dont tout le monde parle, ou d'un compte qui vous permet de bénéficier d'une réduction dans votre fast-food préféré. Quoi qu'il en soit, vous devez tenir compte des implications pour vos données, maintenant et plus tard.

Chaque nouveau service que vous utilisez comporte des risques. Les fuites de données, la divulgation d'informations sur les clients à des tiers, l'accès à des données par des employés véreux sont autant de possibilités qui doivent être envisagées avant de founir vos informations. Vous devez être sûr que vous pouvez faire confiance au service, c'est pourquoi nous ne recommandons pas de stocker des données précieuses sur autre chose que les produits les plus matures et les plus éprouvés. Il s'agit généralement de services qui fournissent E2EE et qui ont fait l'objet d'un audit cryptographique. Un audit renforce l'assurance que le produit a été conçu sans problèmes de sécurité flagrants causés par un développeur inexpérimenté.

Il peut également être difficile de supprimer les comptes sur certains services. Il est parfois possible [d'écraser les données](account-deletion.md#overwriting-account-information) associées à un compte, mais dans d'autres cas, le service conservera un historique complet des modifications apportées au compte.

## Conditions Générales d'Utilisation & Politique de Confidentialité

Les CGU sont les règles que vous acceptez de suivre lorsque vous utilisez le service. Dans les grands services, ces règles sont souvent appliquées par des systèmes automatisés. Parfois, ces systèmes automatisés peuvent faire des erreurs. Par exemple, vous pouvez être banni ou bloqué de votre compte sur certains services pour avoir utilisé un VPN ou numéro VOIP. Il est souvent difficile de faire appel de ces interdictions, et cela implique également une procédure automatisée, qui n'aboutit pas toujours. C'est l'une des raisons pour lesquelles nous ne suggérons pas d'utiliser Gmail pour la messagerie électronique, par exemple. L'e-mail est essentiel pour accéder à d'autres services auxquels vous avez peut-être souscrit.

La Politique de Confidentialité est la manière dont le service indique qu'il utilisera vos données. Elle mérite d'être lue pour que vous compreniez comment vos données seront utilisées. Une entreprise ou une organisation peut ne pas être légalement obligée de suivre tout ce qui est contenu dans la politique (cela dépend de la juridiction). Nous vous recommandons d'avoir une idée de la législation locale et de ce qu'elle autorise un prestataire à collecter.

Nous vous recommandons de rechercher des termes particuliers tels que "collecte de données", "analyse de données", "cookies", "annonces", "publicité" ou services "tiers". Parfois, vous aurez la possibilité de refuser la collecte ou le partage de vos données, mais il est préférable de choisir un service qui respecte votre vie privée dès le départ.

Vous faites également confiance à l'entreprise ou à l'organisation pour se conformer à sa propre politique de confidentialité.

## Méthodes d'authentification

Il existe généralement plusieurs façons de créer un compte, chacune ayant ses propres avantages et inconvénients.

### E-mail et mot de passe

Le moyen le plus courant de créer un nouveau compte est d'utiliser une adresse e-mail et un mot de passe. Lorsque vous utilisez cette méthode, vous devriez utiliser un gestionnaire de mots de passe et suivre les [bonnes pratiques](passwords-overview.md) concernant les mots de passe.

!!! tip "Conseil"

    You can use your password manager to organize other authentication methods too! Just add the new entry and fill the appropriate fields, you can add notes for things like security questions or a backup key.

Vous serez responsable de la gestion de vos identifiants de connexion. Pour plus de sécurité, vous pouvez configurer [MFA](multi-factor-authentication.md) sur vos comptes.

[Gestionnaires de mots de passe recommandés](../passwords.md ""){.md-button}

#### Alias d'e-mail

Si vous ne voulez pas donner votre véritable adresse e-mail à un service, vous avez la possibilité d'utiliser un alias. Nous les avons décrits plus en détail sur notre page de recommandation des services d'e-mail. Essentiellement, les services d'alias vous permettent de créer de nouvelles adresses e-mail qui transmettent tous les courriers à votre adresse principale. Cela peut permettre d'éviter le pistage entre les services et vous aider à gérer les e-mail de marketing qui accompagnent parfois le processus d'inscription. Ceux-ci peuvent être filtrés automatiquement en fonction de l'alias auquel ils sont envoyés.

Si un service est piraté, vous pouvez commencer à recevoir des e-mails d'hameçonnage ou de spam à l'adresse que vous avez utilisée pour vous inscrire. L'utilisation d'alias uniques pour chaque service peut aider à identifier exactement quel service a été piraté.

[Services d'alias d'e-mail recommandés](../email.md#email-aliasing-services ""){.md-button}

### "Sign in with..." (OAuth)

OAuth is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Whenever you see something along the lines of "Sign in with *provider name*" on a registration form, it's typically using OAuth.

When you sign in with OAuth, it will open a login page with the provider you choose, and your existing account and new account will be connected. Your password won't be shared, but some basic information typically will (you can review it during the login request). Ce processus est nécessaire chaque fois que vous voulez vous connecter au même compte.

Les principaux avantages sont les suivants :

- **Sécurité**: aucun risque d'être impliqué dans une [fuite de données](https://fr.wikipedia.org/wiki/Violation_de_donn%C3%A9es) car le site ne stocke pas vos informations d'identification.
- **Facilité d'utilisation**: plusieurs comptes sont gérés par un seul login.

Mais il y a des inconvénients :

- **Privacy**: the OAuth provider you log in with will know the services you use.
- **Centralization**: if the account you use for OAuth is compromised or you aren't able to login to it, all other accounts connected to it are affected.

OAuth authentication can be especially useful in those situations where you could benefit from deeper integration between services. Our recommendation is to limit using OAuth to only where you need it, and always protect the main account with [MFA](multi-factor-authentication.md).

All the services that use OAuth will be as secure as your underlying provider's account. For example, if you want to secure an account with a hardware key, but that service doesn't support hardware keys, you can secure the account you use with OAuth with a hardware key instead, and now you essentially have hardware MFA on all your accounts. It is worth noting though that weak authentication on your OAuth provider account means that any account tied to that login will also be weak.

### Numéro de téléphone

Nous vous recommandons d'éviter les services qui exigent un numéro de téléphone pour l'inscription. Un numéro de téléphone peut vous identifier auprès de plusieurs services et, en fonction des accords de partage des données, cela rendra votre navigation plus facile à suivre, en particulier si l'un de ces services a une fuite, car le numéro de téléphone est souvent **non** chiffré.

Vous devriez éviter de donner votre vrai numéro de téléphone si vous le pouvez. Certains services autorisent l'utilisation de numéros VOIP, mais ceux-ci déclenchent souvent des systèmes de détection des fraudes, entraînant le blocage du compte, ce que nous ne recommandons pas pour les comptes importants.

Dans de nombreux cas, vous devrez fournir un numéro à partir duquel vous pourrez recevoir des SMS ou des appels, en particulier lorsque vous effectuez des achats à l'étranger, au cas où votre commande rencontrerait un problème lors du contrôle aux frontières. Il est courant que les services utilisent votre numéro comme méthode de vérification ; ne vous faites pas bloquer un compte important parce que vous avez voulu être malin et donner un faux numéro !

### Nom d'utilisateur et mot de passe

Certains services vous permettent de vous inscrire sans utiliser d'adresse électronique et vous demandent seulement de définir un nom d'utilisateur et un mot de passe. Ces services peuvent offrir un anonymat accru lorsqu'ils sont associés à un VPN ou à Tor. Gardez à l'esprit que pour ces comptes, il n'y aura très probablement **aucun moyen de récupérer votre compte** au cas où vous oublieriez votre nom d'utilisateur ou votre mot de passe.
