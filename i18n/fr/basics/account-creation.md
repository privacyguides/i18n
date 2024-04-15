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

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Vous pouvez également utiliser votre gestionnaire de mots de passe pour gérer d'autres méthodes d'authentification ! Il suffit d'ajouter la nouvelle entrée et de remplir les champs appropriés. Vous pouvez ajouter des notes pour des choses comme des questions de sécurité ou une clé de secours.

</div>

Vous serez responsable de la gestion de vos identifiants de connexion. Pour plus de sécurité, vous pouvez configurer [MFA](multi-factor-authentication.md) sur vos comptes.

[Gestionnaires de mots de passe recommandés](../passwords.md ""){.md-button}

#### Alias d'e-mail

Si vous ne voulez pas donner votre véritable adresse e-mail à un service, vous avez la possibilité d'utiliser un alias. Nous les avons décrits plus en détail sur notre page de recommandation des services d'e-mail. Essentiellement, les services d'alias vous permettent de créer de nouvelles adresses e-mail qui transmettent tous les courriers à votre adresse principale. Cela peut permettre d'éviter le pistage entre les services et vous aider à gérer les e-mail de marketing qui accompagnent parfois le processus d'inscription. Ceux-ci peuvent être filtrés automatiquement en fonction de l'alias auquel ils sont envoyés.

Si un service est piraté, vous pouvez commencer à recevoir des e-mails d'hameçonnage ou de spam à l'adresse que vous avez utilisée pour vous inscrire. L'utilisation d'alias uniques pour chaque service peut aider à identifier exactement quel service a été piraté.

[Services d'alias d'e-mail recommandés](../email-aliasing.md ""){.md-button}

### "Se connecter avec..." (OAuth)

OAuth est un protocole d'authentification qui vous permet de vous inscrire à un service sans partager beaucoup d'informations avec le fournisseur de services, le cas échéant, en utilisant un compte existant que vous avez avec un autre service à la place. Chaque fois que vous voyez quelque chose du type "Se connecter avec *nom du fournisseur*" sur un formulaire d'inscription, c'est généralement qu'il utilise OAuth.

Lorsque vous vous connectez avec OAuth, une page de connexion s'ouvre avec le fournisseur que vous avez choisi, et votre compte existant et votre nouveau compte seront connectés. Votre mot de passe ne sera pas communiqué, mais certaines informations de base le seront généralement (vous pouvez les consulter lors de la demande de connexion). Ce processus est nécessaire chaque fois que vous voulez vous connecter au même compte.

Les principaux avantages sont les suivants :

- **Sécurité** : vous n'avez pas à vous fier aux pratiques de sécurité du service auquel vous vous connectez lorsqu'il s'agit de stocker vos identifiants de connexion, car ils sont stockés chez le fournisseur OAuth externe, qui, lorsqu'il s'agit de services comme Apple et Google, suit généralement les meilleures pratiques de sécurité, audite en permanence ses systèmes d'authentification et ne stocke pas les identifiants de manière inappropriée (par exemple en texte clair).
- **Facilité d'utilisation** : plusieurs comptes sont gérés par un seul login.

Mais il y a des inconvénients :

- **Vie privée** : le fournisseur OAuth avec lequel vous vous connectez connaîtra les services que vous utilisez.
- **Centralisation** : si le compte que vous utilisez pour OAuth est compromis ou si vous n'êtes pas en mesure de vous y connecter, tous les autres comptes qui y sont connectés sont affectés.

L'OAuth peut être particulièrement utile dans les situations où vous pourriez bénéficier d'une intégration plus poussée entre les services. Nous recommandons de limiter l'utilisation d'OAuth aux seuls cas où vous en avez besoin et de toujours protéger le compte principal à l'aide de [MFA](multi-factor-authentication.md).

Tous les services qui utilisent OAuth seront aussi sûrs que le compte de votre fournisseur OAuth sous-jacent. Par exemple, si vous souhaitez sécuriser un compte avec une clé matérielle, mais que ce service ne prend pas en charge les clés matérielles, vous pouvez sécuriser le compte que vous utilisez avec OAuth avec une clé matérielle à la place, et vous disposez alors d'une MFA matérielle sur tous vos comptes. Il convient toutefois de noter qu'une authentification faible sur votre compte de fournisseur OAuth signifie que tout compte lié à cette connexion sera également faiblement sécurisé.

L'utilisation de *Se connecter avec Google*, *Facebook*, ou d'un autre service présente un danger supplémentaire qui est que le processus OAuth permet généralement un partage *bidirectionnel* des données. Par exemple, le fait de vous connecter à un forum avec votre compte Twitter pourrait permettre à ce forum de faire des choses sur votre compte Twitter, comme poster, lire vos messages ou accéder à d'autres données personnelles. Les fournisseurs OAuth vous présenteront généralement une liste des éléments auxquels vous accordez l'accès au service externe, et vous devez toujours veiller à lire cette liste et à ne pas accorder par inadvertance au service externe l'accès à des éléments dont il n'a pas besoin.

Des applications malveillantes, en particulier sur les appareils mobiles où l'application a accès à la session WebView utilisée pour se connecter au fournisseur OAuth, peuvent également abuser de ce processus en détournant votre session avec le fournisseur OAuth et en accédant à votre compte OAuth par ce biais. L'utilisation de l'option *Se connecter avec* avec n'importe quel fournisseur doit généralement être considérée comme une question de commodité que vous n'utilisez qu'avec des services dont vous êtes sûrs qu'ils ne sont pas activement malveillants.

### Numéro de téléphone

Nous vous recommandons d'éviter les services qui exigent un numéro de téléphone pour l'inscription. Un numéro de téléphone peut vous identifier auprès de plusieurs services et, en fonction des accords de partage des données, cela rendra votre navigation plus facile à suivre, en particulier si l'un de ces services a une fuite, car le numéro de téléphone est souvent **non** chiffré.

Vous devriez éviter de donner votre vrai numéro de téléphone si vous le pouvez. Certains services autorisent l'utilisation de numéros VOIP, mais ceux-ci déclenchent souvent des systèmes de détection des fraudes, entraînant le blocage du compte, ce que nous ne recommandons pas pour les comptes importants.

Dans de nombreux cas, vous devrez fournir un numéro à partir duquel vous pourrez recevoir des SMS ou des appels, en particulier lorsque vous effectuez des achats à l'étranger, au cas où votre commande rencontrerait un problème lors du contrôle aux frontières. Il est courant que les services utilisent votre numéro comme méthode de vérification ; ne vous faites pas bloquer un compte important parce que vous avez voulu être malin et donner un faux numéro !

### Nom d'utilisateur et mot de passe

Certains services vous permettent de vous inscrire sans utiliser d'adresse électronique et vous demandent seulement de définir un nom d'utilisateur et un mot de passe. Ces services peuvent offrir un anonymat accru lorsqu'ils sont associés à un VPN ou à Tor. Gardez à l'esprit que pour ces comptes, il n'y aura très probablement **aucun moyen de récupérer votre compte** au cas où vous oublieriez votre nom d'utilisateur ou votre mot de passe.
