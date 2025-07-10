---
meta_title: "Why Email Isn't the Best Choice for Privacy and Security - Privacy Guides"
title: Email Security
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

Az e-mail alapértelmezetten nem biztonságos kommunikációs forma. Az e-mailek biztonságát javíthatod olyan eszközökkel, mint az OpenPGP, amely végpontok közötti titkosítást ad az üzeneteidhez, bár az OpenPGP-nek is vannak hátrányai más üzenetküldő alkalmazások titkosításához képest.

Ezért az e-mailt leginkább tranzakciós üzenetek fogadására érdemes használni (például értesítések, megerősítő e-mailek, jelszó-visszaállítások stb.), nem pedig személyes kommunikációra.

## E-mail titkosítási áttekintés

A különböző e-mail szolgáltatók közötti e-mailekhez a végpontok közötti titkosítás szabványos módja az OpenPGP használata. Az OpenPGP szabványnak többféle megvalósítása létezik, a legelterjedtebbek a [GnuPG](../encryption.md#gnu-privacy-guard) és az [OpenPGP.js](https://openpgpjs.org).

Még ha OpenPGP-t használsz is, az nem támogatja a [ forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy)-t, vagyis az előre irányuló titkosságot, ami azt jelenti, hogy ha a te vagy a címzett privát kulcsa valaha kiszivárog, az összes korábbi, ezzel titkosított üzenet is visszafejthetővé válik. Személyes üzenetküldéshez ezért inkább olyan [azonnali üzenetküldő alkalmazásokat](../real-time-communication.md) ajánlunk, amelyek előre irányuló titkosságot használnak, mert ezek biztonságosabbak, mint az e-mail.

Létezik egy másik, üzleti körökben népszerű szabvány is, az [S/MIME](https://en.wikipedia.org/wiki/S/MIME), de ez tanúsítványt igényel egy [hitelesítésszolgáltatótól](https://en.wikipedia.org/wiki/Certificate_authority) (CA), amiért gyakran éves díjat is kell fizetni. Bizonyos esetekben használhatóbb, mint a PGP, mivel olyan népszerű/elterjedt e-mail alkalmazások is támogatják, mint az Apple Mail, a [Google Workspace](https://support.google.com/a/topic/9061730) és az [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). Azonban az S/MIME sem oldja meg az előre irányuló titkosság hiányát, és nem is különösebben biztonságosabb a PGP-nél.

## Mi az a Web Key Directory szabvány?

A [Web Key Directory](https://wiki.gnupg.org/WKD) (WKD) lehetővé teszi az e-mail kliensek számára, hogy más szolgáltatók postafiókjaihoz tartozó OpenPGP kulcsokat automatikusan megtaláljanak. A WKD-t támogató kliensek a címzett domainje alapján kérik le a kulcsot. Például, ha írsz a `jonah@privacyguides.org` címre, az e-mail kliensed elkéri a `privacyguides.org`-tól Jonah OpenPGP kulcsát, és ha a `privacyguides.org` rendelkezik a fiók kulcsával, akkor az üzeneted automatikusan titkosítva lesz.

Az [általunk ajánlott, WKD-t támogató e-mail kliensek](../email-clients.md) mellett néhány webmail szolgáltató is támogatja a WKD-t. Az, hogy *a te kulcsod* elérhető-e mások számára WKD-n keresztül, az a domained beállításaitól függ. Ha olyan [e-mail szolgáltatót](../email.md#openpgp-compatible-services) használsz, mint a Proton Mail vagy a Mailbox.org, ők automatikusan megoszthatják az OpenPGP kulcsodat.

Ha saját domaint használsz, a WKD-t külön kell beállítanod. Ha te kezeled a domain nevet, akkor a WKD-t szolgáltatótól függetlenül beállíthatod. Ennek egyik egyszerű módja a `keys.openpgp.org` ["WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" funkciójának használata: állíts be egy CNAME rekordot a domained `openpgpkey` aldomainjére, amely a `wkd.keys.openpgp.org` címre mutat, majd töltsd fel a kulcsodat a [keys.openpgp.org](https://keys.openpgp.org) oldalra. Alternatív megoldásként [saját szerveren is hosztolhatod a WKD-t](https://wiki.gnupg.org/WKDHosting).

Ha olyan szolgáltató megosztott domainjét használod, amely nem támogatja a WKD-t, például a `@gmail.com`-ot, akkor ezen a módon nem tudod megosztani OpenPGP-kulcsodat másokkal.

### Melyik e-mail kliensek támogatják a végpontok közötti titkosítást?

Az olyan e-mail szolgáltatók, amelyek lehetővé teszik a szabványos hozzáférési protokollok, például az IMAP és az SMTP használatát, az [általunk ajánlott e-mail kliensek](../email-clients.md) bármelyikével használhatók. Azonban ha a hitelesítés csak jelszóval történik, és nincs [OAuth](account-creation.md#sign-in-with-oauth) vagy köztes alkalmazás, akkor a biztonság csökkenhet, mivel a [többfaktoros hitelesítés](multi-factor-authentication.md) nem lehetséges.

### Hogyan védhetem meg a privát kulcsaimat?

Egy intelligens kártya (például a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) vagy a [Nitrokey](../security-keys.md#nitrokey)) úgy működik, hogy fogad egy titkosított e-mail üzenetet egy eszközről (telefonról, táblagépről, számítógépről stb.), amelyen egy e-mail vagy webmail kliens fut. Az üzenetet ezután az intelligens kártya visszafejti, majd a dekódolt tartalmat visszaküldi az eszköznek.

Ez azért előnyös, mert a visszafejtés az intelligens kártyán történik, így a privát kulcs nem kerül ki a kártyáról, és nem lesz kitéve egy esetlegesen fertőzött eszköznek.

## E-mail metaadatok áttekintése

Az e-mail metaadatok az e-mail [üzenet fejlécében](https://en.wikipedia.org/wiki/Email#Message_header) vannak tárolva, és tartalmaznak néhány látható fejlécet is, amelyeket ismerhetsz, mint például a `címzett`, a `küldő`, a `másolati címzettek`, a `dátum` és a `tárgy`. Sok e-mailes alkalmazás és szolgáltató olyan rejtett fejléceket is alkalmaz, amelyek számos adatot elárulhatnak a fiókoddal kapcsolatban.

Az ügyfélszoftverek az e-mail metaadatokat használhatják arra, hogy megmutassák, kitől és mikor érkezett az üzenet. A szerverek az e-mail metaadatait felhasználhatják annak meghatározására, hogy hová kell továbbítani az üzenetet, valamint [más célokra](https://en.wikipedia.org/wiki/Email#Message_header) is, amelyek nem mindig átláthatók.

### Ki láthatja az e-mail metaadatokat?

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Sometimes email servers will also use third-party services to protect against spam, which generally also have access to your messages.

### Why Can't Metadata be E2EE?

Email metadata is crucial to the most basic functionality of email (where it came from, and where it has to go). E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
