---
title: "Fildelning och synkronisering"
icon: material/share-variant
description: Upptäck hur du kan dela dina filer privat mellan dina enheter, med vänner och familj eller anonymt på nätet.
cover: file-sharing.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Tjänsteleverantörer](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Upptäck hur du kan dela dina filer privat mellan dina enheter, med vänner och familj eller anonymt på nätet.

## Fildelningsprogram

If you have already use [Proton Drive](cloud.md#proton-drive)[^1] or have a [Bitwarden](passwords.md#bitwarden) Premium[^2] subscription, consider using the file sharing capabilities that they each offer, both of which use end-to-end encryption. Otherwise, the standalone options listed here ensure that the files you share are not read by a remote server.

### Skicka

<div class="admonition recommendation" markdown>

![Send logo](assets/img/file-sharing-sync/send.svg){ align=right }

**Send** är en gren av Mozillas nedlagda service Firefox Send som låter dig dela filer till andra med en länk. Filerna krypteras på din enhet så att de inte kan läsas av servern, och de kan också skyddas med lösenord. The maintainer of Send hosts a [public instance](https://send.vis.ee). Du kan använda andra offentliga instanser, eller du kan vara värd för Skicka själv.

[:octicons-home-16: Startsida](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://cryptomator.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/timvisee/send#readme/){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Källkod" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee/){ .card-link title=Contribute }

</details>

</div>

Send kan användas via webbgränssnittet eller via [ffsend](https://github.com/timvisee/ffsend) CLI. Om du känner till kommandoraden och skickar filer ofta rekommenderar vi att du använder CLI-klienten för att undvika JavaScript-baserad kryptering. Du kan ange flaggan `- värd` för att använda en specifik server:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![OnionShare logo](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** is an open-source tool that lets you securely and [:material-incognito: anonymously](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } share a file of any size. Det fungerar genom att starta en webbserver som är tillgänglig som en Tor onion-tjänst, med en oigenkännlig URL som du kan dela med mottagarna för att ladda ner eller skicka filer.

[:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)

</details>

</div>

OnionShare provides the option to connect via [Tor bridges](https://docs.onionshare.org/2.6.2/en/tor.html#automatic-censorship-circumvention) to circumvent [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

### Kriterier

**Observera att vi inte är knutna till något av de projekt som vi rekommenderar.** Förutom [våra standardkriterier](about/criteria.md)har vi utvecklat en tydlig uppsättning krav som gör det möjligt för oss att ge objektiva rekommendationer. Vi föreslår att du bekantar dig med den här listan innan du väljer att använda ett projekt, och att du gör din egen forskning för att se till att det är rätt val för dig.

- Får inte lagra dekrypterade data på en fjärrserver.
- Måste vara programvara med öppen källkod.
- Måste antingen ha klienter för Linux, macOS och Windows eller ha ett webbgränssnitt.

## FreedomBox

<div class="admonition recommendation" markdown>

![FreedomBox-logotyp](assets/img/file-sharing-sync/freedombox.svg){ align=right }

**FreedomBox** är ett operativsystem som är utformat för att köras på en [single-board computer (SBC)] (https://en.wikipedia.org/wiki/Single-board_computer). Syftet är att göra det enkelt att konfigurera serverprogram som du kanske vill vara värd för själv.

[:octicons-home-16: Homepage](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=Documentation}
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Source Code" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title=Contribute }

</details>

</div>

## Filsynkronisering

### Nextcloud (klient-server)

<div class="admonition recommendation" markdown>

![Nextcloud logo](assets/img/document-collaboration/nextcloud.svg){ align=right }

**Nextcloud** is a suite of free and open-source client-server software for creating your own file hosting services on a private server you control.

[:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Varning</p>

Vi rekommenderar inte att du använder [E2EE App](https://apps.nextcloud.com/apps/end_to_end_encryption) för Nextcloud eftersom det kan leda till dataförluster; det är mycket experimentellt och inte av produktionskvalitet.

</div>

### Synkronisering (P2P)

<div class="admonition recommendation" markdown>

![Synkronisera logotyp](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing** är ett verktyg för kontinuerlig filsynkronisering med öppen källkod. Det används för att synkronisera filer mellan två eller flera enheter över det lokala nätverket eller internet. Synkronisering använder inte en centraliserad server; den använder [Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html #bep-v1) för att överföra data mellan enheter. All data krypteras med TLS.

[:octicons-home-16: Homepage](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="Source Code" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nutomic.syncthingandroid)
- [:fontawesome-brands-windows: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

### Kriterier

**Observera att vi inte är knutna till något av de projekt som vi rekommenderar.** Förutom [våra standardkriterier](about/criteria.md)har vi utvecklat en tydlig uppsättning krav som gör det möjligt för oss att ge objektiva rekommendationer. Vi föreslår att du bekantar dig med den här listan innan du väljer att använda ett projekt, och att du gör din egen forskning för att se till att det är rätt val för dig.

#### Minimikrav

- Får inte kräva en fjärr-/molnserver från tredje part.
- Måste vara programvara med öppen källkod.
- Måste antingen ha klienter för Linux, macOS och Windows eller ha ett webbgränssnitt.

#### Bästa fall

Våra kriterier för bästa fall representerar vad vi skulle vilja se av det perfekta projektet i denna kategori. Våra rekommendationer kanske inte innehåller alla eller några av dessa funktioner, men de som gör det kan vara högre rankade än andra på den här sidan.

- Should have mobile clients for iOS and Android which at least support document previews.
- Should support photo backups from iOS and Android, and optionally support file/folder sync on Android.

[^1]: Proton Drive allows you to [share files or folders](https://proton.me/support/drive-shareable-link) by generating a shareable public link or sending a unique link to a designated email address. Public links can be protected with a password, set to expire, and completely revoked, while links shared via email can have custom permissions and be similarly revoked. Per Proton Drive's [privacy policy](https://proton.me/drive/privacy-policy), file contents, file and folder names, and thumbnail previews are end-to-end encrypted.
[^2]: With a [premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) subscription, [Bitwarden Send](https://bitwarden.com/products/send) allows you to share files and text securely with [end-to-end encryption](https://bitwarden.com/help/send-encryption). A [password](https://bitwarden.com/help/send-privacy/#send-passwords) can be required along with the Send link. Bitwarden Send also features [automatic deletion](https://bitwarden.com/help/send-lifespan).
