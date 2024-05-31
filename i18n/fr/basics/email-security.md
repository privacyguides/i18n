---
meta_title: "Pourquoi l'e-mail n'est pas le meilleur choix en matière de protection de la vie privée et de sécurité - Privacy Guides"
title: Sécurité des e-mails
icon: material/email
description: L'e-mail est intrinsèquement peu sûr à bien des égards, et voici quelques-unes des raisons pour lesquelles il n'est pas notre premier choix en matière de communications sécurisées.
---

L'e-mail est une forme de communication non sécurisée par défaut. Vous pouvez améliorer la sécurité de vos e-mails avec des outils tels que OpenPGP, qui ajoute un chiffrement de bout en bout à vos messages, mais OpenPGP présente toujours un certain nombre d'inconvénients par rapport au chiffrement dans d'autres applications de messagerie, et certaines données d'e-mail ne peuvent jamais être chiffrées de manière inhérente en raison de la manière dont l'e-mail est conçu.

Par conséquent, il est préférable d'utiliser l'e-mail pour recevoir des e-mails transactionnels (notifications, e-mails de vérification, réinitialisation de mot de passe, etc.) provenant des services auxquels vous vous inscrivez en ligne, et non pour communiquer avec d'autres personnes.

## Aperçu du chiffrement des e-mails

La méthode standard pour ajouter du E2EE aux e-mails entre différents fournisseurs d'e-mails est d'utiliser OpenPGP. Il existe différentes implémentations de la norme OpenPGP, les plus courantes étant [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard) et [OpenPGP.js](https://openpgpjs.org).

Il existe une autre norme populaire auprès des entreprises, appelée [S/MIME](https://en.wikipedia.org/wiki/S/MIME), mais elle nécessite un certificat émis par une [Autorité de Certification](https://en.wikipedia.org/wiki/Certificate_authority) (toutes ne délivrent pas de certificats S/MIME). Elle est prise en charge par [Google Workplace](https://support.google.com/a/topic/9061730) et [Outlook sur le web ou Exchange Server 2016, 2019](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480).

Même si vous utilisez OpenPGP, il ne prend pas en charge la [confidentialité persistante](https://en.wikipedia.org/wiki/Forward_secrecy), ce qui signifie que si votre clé privée ou celle du destinataire est volée, tous les messages précédents chiffrés avec cette clé seront exposés. C'est pourquoi nous recommandons, dans la mesure du possible, les [messageries instantanées](../real-time-communication.md) qui mettent en œuvre la confidentialité persistante par rapport aux e-mails pour les communications de personne à personne.

## Qu'est-ce que la norme Web Key Directory ?

La norme Web Key Directory (WKD) permet aux clients d'e-mail de découvrir la clé OpenPGP d'autres boîtes mails, même celles qui sont hébergées chez un autre fournisseur. Les clients d'e-mail qui prennent en charge le WKD demandent au serveur du destinataire une clé basée sur le nom de domaine de l'adresse e-mail. Par exemple, si vous envoyez un e-mail à `jonah@privacyguides.org`, votre client d'e-mail demandera à `privacyguides.org` la clé OpenPGP de Jonah, et si `privacyguides.org` dispose d'une clé pour ce compte, votre message sera automatiquement chiffré.

Outre les [clients d'e-mail que nous recommandons](../email-clients.md) et qui prennent en charge le WKD, certains fournisseurs d'e-mail avec interface web prennent également en charge le WKD. Le fait que *votre propre clé* soit publiée sur le WKD pour que d'autres puissent l'utiliser dépend de la configuration de votre domaine. Si vous utilisez un [fournisseur d'e-mail](../email.md#openpgp-compatible-services) qui prend en charge le WKD, tel que Proton Mail ou Mailbox.org, il peut publier votre clé OpenPGP sur son domaine pour vous.

Si vous utilisez votre propre domaine personnalisé, vous devrez configurer le WKD séparément. Si vous contrôlez votre nom de domaine, vous pouvez configurer le WKD quel que soit votre fournisseur d'e-mail. Une façon simple de le faire est d'utiliser la fonction "[WKD en tant que Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" de keys.openpgp.org, en définissant un enregistrement CNAME sur le sous-domaine `openpgpkey` de votre domaine pointé vers `wkd.keys.openpgp.org`, puis en envoyant votre clé sur [keys.openpgp.org](https://keys.openpgp.org). Vous pouvez également [héberger vous-même le WKD sur votre propre serveur web](https://wiki.gnupg.org/WKDHosting).

Si vous utilisez un domaine partagé d'un fournisseur qui ne prend pas en charge le WKD, comme @gmail.com, vous ne pourrez pas partager votre clé OpenPGP avec d'autres personnes via cette méthode.

### Quels clients d'e-mail supportent le E2EE ?

Les fournisseurs d'e-mail qui vous permettent d'utiliser les protocoles d'accès standard comme IMAP et SMTP peuvent être utilisés avec n'importe lequel des [clients d'e-mail que nous recommandons](../email-clients.md). En fonction de la méthode d'authentification, cela peut entraîner une diminution de la sécurité si le fournisseur ou le client d'e-mail ne prend pas en charge OATH ou une application passerelle, car [l'authentification multi-facteurs](/basics/multi-factor-authentication/) n'est pas possible avec l'authentification par mot de passe simple.

### Comment puis-je protéger mes clés privées ?

A smartcard (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../multi-factor-authentication.md#nitrokey) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. Le message est ensuite déchiffré par la carte à puce et le contenu déchiffré est renvoyé à l'appareil.

Il est préférable que le déchiffrement ait lieu sur la carte à puce afin d'éviter d'exposer votre clé privée à un dispositif compromis.

## Aperçu des métadonnées des e-mails

Les métadonnées des e-mails sont stockées dans [l'en-tête de message](https://en.wikipedia.org/wiki/Email#Message_header) de l'e-mail et comprennent certains en-têtes visibles que vous avez peut-être vus, tels que : `À`, `De`, `Cc`, `Date`, `Sujet`. Il existe également un certain nombre d'en-têtes cachés inclus par de nombreux clients et fournisseurs d'e-mail qui peuvent révéler des informations sur votre compte.

Le logiciel client peut utiliser les métadonnées de l'e-mail pour montrer de qui provient un message et à quelle heure il a été reçu. Les serveurs peuvent l'utiliser pour déterminer où un e-mail doit être envoyé, parmi [d'autres objectifs](https://en.wikipedia.org/wiki/Email#Message_header) qui ne sont pas toujours transparents.

### Qui peut voir les métadonnées des e-mails ?

Les métadonnées des emails sont protégées des observateurs extérieurs par le protocole [TLS Opportuniste](https://en.wikipedia.org/wiki/Opportunistic_TLS). Elles peuvent néanmoins être vues par votre logiciel client e-mail (ou interface d'e-mail web) et par tout serveur relayant le message de votre part à ses destinataires, y compris votre fournisseur d'e-mail. Parfois, les serveurs d'e-mail font également appel à des services tiers pour se protéger des spams, qui ont généralement aussi accès à vos messages.

### Pourquoi les métadonnées ne peuvent-elles pas être E2EE?

Les métadonnées des e-mails sont essentielles à la fonctionnalité la plus élémentaire d'un e-mail (d'où il vient et où il doit aller). À l'origine, le E2EE n'était pas intégré dans les protocoles d'e-mails, mais nécessitait un logiciel complémentaire comme OpenPGP. Comme les messages OpenPGP doivent toujours fonctionner avec les fournisseurs d'e-mail traditionnels, il ne peut pas chiffrer les métadonnées de l'e-mail, mais seulement le corps du message lui-même. Cela signifie que, même en utilisant OpenPGP, des observateurs extérieurs peuvent voir de nombreuses informations sur vos messages, comme l'identité de l'expéditeur, l'objet du message, le moment de l'envoi, etc.
