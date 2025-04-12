---
meta_title: "Pourquoi l'e-mail n'est pas le meilleur choix en matière de protection de la vie privée et de sécurité - Privacy Guides"
title: Sécurité des e-mails
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

L'e-mail est une forme de communication non sécurisée par défaut. You can improve your email security with tools such as OpenPGP, which add End-to-End Encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

Par conséquent, il est préférable d'utiliser l'e-mail pour recevoir des e-mails transactionnels (notifications, e-mails de vérification, réinitialisation de mot de passe, etc.) provenant des services auxquels vous vous inscrivez en ligne, et non pour communiquer avec d'autres personnes.

## Aperçu du chiffrement des e-mails

La méthode standard pour ajouter du E2EE aux e-mails entre différents fournisseurs d'e-mails est d'utiliser OpenPGP. Il existe différentes implémentations de la norme OpenPGP, les plus courantes étant [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard) et [OpenPGP.js](https://openpgpjs.org).

Même si vous utilisez OpenPGP, il ne prend pas en charge la [confidentialité persistante](https://en.wikipedia.org/wiki/Forward_secrecy), ce qui signifie que si votre clé privée ou celle du destinataire est volée, tous les messages précédents chiffrés avec cette clé seront exposés. C'est pourquoi nous recommandons, dans la mesure du possible, les [messageries instantanées](../real-time-communication.md) qui mettent en œuvre la confidentialité persistante par rapport aux e-mails pour les communications de personne à personne.

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however, it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## Qu'est-ce que la norme Web Key Directory ?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Les clients d'e-mail qui prennent en charge le WKD demandent au serveur du destinataire une clé basée sur le nom de domaine de l'adresse e-mail. Par exemple, si vous envoyez un e-mail à `jonah@privacyguides.org`, votre client d'e-mail demandera à `privacyguides.org` la clé OpenPGP de Jonah, et si `privacyguides.org` dispose d'une clé pour ce compte, votre message sera automatiquement chiffré.

Outre les [clients d'e-mail que nous recommandons](../email-clients.md) et qui prennent en charge le WKD, certains fournisseurs d'e-mail avec interface web prennent également en charge le WKD. Le fait que *votre propre clé* soit publiée sur le WKD pour que d'autres puissent l'utiliser dépend de la configuration de votre domaine. Si vous utilisez un [fournisseur d'e-mail](../email.md#openpgp-compatible-services) qui prend en charge le WKD, tel que Proton Mail ou Mailbox.org, il peut publier votre clé OpenPGP sur son domaine pour vous.

Si vous utilisez votre propre domaine personnalisé, vous devrez configurer le WKD séparément. Si vous contrôlez votre nom de domaine, vous pouvez configurer le WKD quel que soit votre fournisseur d'e-mail. Une façon simple de le faire est d'utiliser la fonction "[WKD en tant que Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" de keys.openpgp.org, en définissant un enregistrement CNAME sur le sous-domaine `openpgpkey` de votre domaine pointé vers `wkd.keys.openpgp.org`, puis en envoyant votre clé sur [keys.openpgp.org](https://keys.openpgp.org). Vous pouvez également [héberger vous-même le WKD sur votre propre serveur web](https://wiki.gnupg.org/WKDHosting).

Si vous utilisez un domaine partagé d'un fournisseur qui ne prend pas en charge le WKD, comme @gmail.com, vous ne pourrez pas partager votre clé OpenPGP avec d'autres personnes via cette méthode.

### Quels clients d'e-mail supportent le E2EE ?

Les fournisseurs d'e-mail qui vous permettent d'utiliser les protocoles d'accès standard comme IMAP et SMTP peuvent être utilisés avec n'importe lequel des [clients d'e-mail que nous recommandons](../email-clients.md). Depending on the authentication method, this may lead to the decrease security if either the provider or the email client does not support OATH or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### Comment puis-je protéger mes clés privées ?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Aperçu des métadonnées des e-mails

Les métadonnées des e-mails sont stockées dans [l'en-tête de message](https://en.wikipedia.org/wiki/Email#Message_header) de l'e-mail et comprennent certains en-têtes visibles que vous avez peut-être vus, tels que : `À`, `De`, `Cc`, `Date`, `Sujet`. Il existe également un certain nombre d'en-têtes cachés inclus par de nombreux clients et fournisseurs d'e-mail qui peuvent révéler des informations sur votre compte.

Le logiciel client peut utiliser les métadonnées de l'e-mail pour montrer de qui provient un message et à quelle heure il a été reçu. Les serveurs peuvent l'utiliser pour déterminer où un e-mail doit être envoyé, parmi [d'autres objectifs](https://en.wikipedia.org/wiki/Email#Message_header) qui ne sont pas toujours transparents.

### Qui peut voir les métadonnées des e-mails ?

Les métadonnées des emails sont protégées des observateurs extérieurs par le protocole [TLS Opportuniste](https://en.wikipedia.org/wiki/Opportunistic_TLS). Elles peuvent néanmoins être vues par votre logiciel client e-mail (ou interface d'e-mail web) et par tout serveur relayant le message de votre part à ses destinataires, y compris votre fournisseur d'e-mail. Parfois, les serveurs d'e-mail font également appel à des services tiers pour se protéger des spams, qui ont généralement aussi accès à vos messages.

### Pourquoi les métadonnées ne peuvent-elles pas être E2EE?

Les métadonnées des e-mails sont essentielles à la fonctionnalité la plus élémentaire d'un e-mail (d'où il vient et où il doit aller). À l'origine, le E2EE n'était pas intégré dans les protocoles d'e-mails, mais nécessitait un logiciel complémentaire comme OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
