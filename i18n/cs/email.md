---
meta_title: "Doporučení na šifrované soukromé e-maily – Privacy Guides"
title: E-mailové služby
icon: material/email
description: Tito poskytovatelé e-mailu jsou skvělí pro bezpečné uchovávání e-mailů, a mnozí z nich nabízejí interoperabilní OpenPGP šifrování s ostatními poskytovateli.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Chrání před těmito hrozbami:</small>

- [:material-server-network: Poskytovatelé služeb](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

E-mail je prakticky nezbytný pro používání jakékoliv online služby, ale nedoporučujeme jej pro osobní konverzace. Namísto e-mailu zvažte možnost kontaktování pomocí chatovacích služeb, které podporují dopřednou bezpečnost.

[Doporučené messengery](real-time-communication.md ""){.md-button}

## Doporučení poskytovatelé

Pro všechno ostatní doporučujeme různé e-mailové poskytovatele, kteří mají udržitelný byznys model a vestavěné funkce pro zachování bezpečnosti a soukromí. Přečtěte si náš [úplný seznam kritérií](#criteria) pro více informací.

| Poskytovatel                  | OpenPGP / WKD                          | IMAP / SMTP                                                     | Zero-Access šifrování                                  | Anonymní platební metody                               |
| ----------------------------- | -------------------------------------- | --------------------------------------------------------------- | ------------------------------------------------------ | ------------------------------------------------------ |
| [Proton Mail](#proton-mail)   | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Pouze placené tarify | :material-check:{ .pg-green }                          | Hotovost                                               |
| [Mailbox Mail](#mailbox-mail) | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                   | :material-information-outline:{ .pg-blue } Pouze maily | Hotovost                                               |
| [Tuta](#tuta)                 | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                          | :material-check:{ .pg-green }                          | Monero <br>Hotovost prostřednictvím třetí strany |

Můžete navíc, nebo místo, zvážit používání kromě zmíněných e-mailových poskytovatelů i používání dedikované [služby pro e-mailové aliasy](email-aliasing.md#recommended-providers) pro ochranu vašeho soukromí. Tyto služby vám mimo jiné mohou pomoct chránit vaši pravou adresu před spamem, zabránit marketingovým týmům v korelování mezi jednotlivými účty a šifrovat všechny příchozí zprávy pomocí PGP.

- [Více informací](email-aliasing.md)

## Služby kompatibilní s OpenPGP

Tito poskytovatelé nativně podporují OpenPGP (de)šifrování a [standard Web Key Directory (WKD)](basics/email-security.md#what-is-the-web-key-directory-standard), který umožňuje posílání koncově šifrovaných e-mailů bez ohledu na poskytovatele. Například uživatel Proton Mailu může poslat koncově šifrovanou zprávu uživateli Mailbox Mail, nebo může přijímat notifikace šifrované pomocí OpenPGP z internetových služeb, které to podporují.

<div class="grid cards" markdown>

- ![logo Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](#proton-mail)
- ![logo Mailbox mail](assets/img/email/mailbox-mail.svg){ .twemoji } [Mailbox Mail](#mailbox-mail)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Varování</p>

I při používání E2EE technologie, jako je OpenPGP, budou vaše e-maily přesto obsahovat některá metadata, která nebudou šifrovaná v hlavičce e-mailu, obvykle včetně předmětu. Přečtěte si více o [e-mailových metadatech](basics/email-security.md#email-metadata-overview).

OpenPGP také nepodporuje dopřednou bezpečnost, což znamená, že pokud někdo jiný získá soukromý klíč, ať už váš, nebo protistrany, všechny vaše předchozí šifrované zprávy budou odhaleny.

- [Jak mohu ochránit své soukromé klíče?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![logo Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** je e-mailová služba se zaměřením na soukromí, šifrování, bezpečnost a snadné používání. Fungují od roku 2013. Proton AG sídlí ve švýcarské Ženevě.

Tarif Proton Free obsahuje 500 MB úložiště pro e-mail, které můžete zdarma rozšířit až na 1 GB.

[:octicons-home-16: Hlavní stránka](https://proton.me/cs/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion stránka" }
[:octicons-eye-16:](https://proton.me/cs/legal/privacy){ .card-link title="Zásady ochrany osobních údajů" }
[:octicons-info-16:](https://proton.me/support/cs/mail){ .card-link title="Podpora" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Zdrojový kód" }

<details class="downloads" markdown>
<summary>Ke stažení</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Bezplatné účty mají některá omezení, např. nemohou vyhledávat v textu zpráv nebo nemají přístup k [Proton Mail Bridge](https://proton.me/mail/bridge), který je nutný pro používání s [doporučenými desktopovými e-mailovými klienty](email-clients.md) (např. s Thunderbirdem). Placené účty zahrnují funkce, jako je např. Proton Mail Bridge, dodatečné úložiště nebo podpora vlastních domén. Pokud máte tarif Proton Unlimited nebo jakýkoliv Proton tarif pro více uživatelů, získáte také [SimpleLogin](email-aliasing.md#simplelogin) Premium zdarma.

[Osvědčení](https://proton.me/blog/security-audit-all-proton-apps) bylo uděleno aplikacím Proton Mail 9. října 2021 firmou [Securitum](https://research.securitum.com).

Proton Mail generuje interní hlášení o pádech, které ale **nejsou** sdílené se třetími stranami. Můžete je ve webové aplikaci zakázat následovně: :gear: → **Všechna nastavení** → **Účet** → **Bezpečnost a soukromí** → **Soukromí a sběr dat**.

#### :material-check:{ .pg-green } Vlastní domény a aliasy

Uživatelé placených tarifů Proton Mailu mohou používat vlastní domény se službou nebo [univerzální](https://proton.me/support/catch-all) adresu. Proton Mail také podporuje [sub-adresování](https://proton.me/support/creating-aliases), což je užitečné pro lidi, kteří si nechtějí kupovat doménu.

#### :material-check:{ .pg-green } Soukromé platební metody

Proton Mail kromě běžných plateb kreditní či debetní kartou [přijímá](https://proton.me/support/payment-options) také [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), PayPal a dokonce i **hotovost** zaslanou poštou.

#### :material-check:{ .pg-green } Zabezpečení účtu

Proton Mail podporuje [dvoufaktorové ověřování](https://proton.me/support/two-factor-authentication-2fa) pomocí TOTP a [hardwarové bezpečnostní klíče](https://proton.me/support/2fa-security-key) pomocí standardů FIDO2 a U2F. Používání hardwarových bezpečnostních klíčů nejprve vyžaduje nastavení TOTP dvoufaktorového ověření.

#### :material-check:{ .pg-green } Zabezpečení dat

Proton Mail má [zero-access šifrování](https://proton.me/blog/zero-access-encryption) pro uložená data e-mailů a [kalendářů](https://proton.me/news/protoncalendar-security-model). K datům zabezpečeným zero-access šifrováním můžete přistupovat jenom vy.

Určité informace uložené v [Kontaktech](https://proton.me/support/proton-contacts), např. zobrazovaná jména nebo e-mailové adresy, nejsou zabezpečené zero-access šifrováním. Pole kontaktu, která podporují zero-access šifrování, např. telefonní čísla, jsou označené ikonou zámku.

#### :material-check:{ .pg-green } Šifrování e-malu

Proton Mail má [integrované OpenPGP šifrování](https://proton.me/support/how-to-use-pgp) ve svém webmailu. E-maily posílané ostatním účtům Proton Mailu jsou automaticky šifrované a šifrování na adresy mimo Proton Mail OpenPGP klíčem lze jednoduše povolit v nastavení vašeho účtu. Proton také podporuje automatické zjišťování externích klíčů pomocí WKD. To znamená, že e-maily poslané jiným poskytovatelům, kteří používají WKD, budou také automaticky šifrované pomocí OpenPGP bez nutnosti vyměňovat si veřejné OpenPGP klíče s vašimi kontakty. Také vám umožňují [šifrovat zprávy adresátům mimo Proton Mail bez OpenPGP](https://proton.me/support/password-protected-emails), aniž by si museli zakládat Proton Mail účet.

Proton Mail také zveřejňuje veřejné klíče Proton účtů přes HTTP z jejich WKD. To umožňuje lidem, kteří nepoužívají Proton Mail, snadno najít OpenPGP klíče Proton Mail účtů jednoduše pro E2EE mezi různými poskytovateli. To ale platí pouze pro e-mailové adresy ve vlastních doménách Protonu, např. `@proton.me`. Pokud používáte vlastní doménu, je potřeba [nastavit WKD](basics/email-security.md#what-is-the-web-key-directory-standard) zvlášť.

#### :material-information-outline:{ .pg-blue } Ukončení účtu

Pokud máte placený tarif a [nezaplatíte](https://proton.me/support/delinquency) do 14 dnů, nebudete moci přistupovat ke svým datům. Po 30 dnech se váš účet omezí a nebude přijímat příchozí e-maily. Toto období vám bude stále účtováno. Proton [odstraní neaktivní bezplatné účty](https://proton.me/support/inactive-accounts) po jednom roce. **Nemůžete** znovu použít e-mailovou adresu deaktivovaného účtu.

#### :material-information-outline:{ .pg-blue } Dodatečné funkce

Tarif Proton Mail [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) vám kromě několika vlastních domén, neomezených skrytých e-mailových aliasů a 500 GB úložiště navíc umožňuje přístup k prémiovým funkcím ostatních služeb Protonu.

### Mailbox Mail

<div class="admonition recommendation" markdown>

![logo Mailbox Mail](assets/img/email/mailbox-mail.svg){ align=right }

**Mailbox Mail** je e-mailová služba zaměřená na bezpečnost, je bez reklam a je poháněná 100% ekologickou energií. Fungují od roku 2014. Mailbox Mail sídlí v německém Berlíně.

Účty mají 2 GB úložiště, které může být podle potřeby rozšířeno.

[:octicons-home-16: Hlavní stránka](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Zásady ochrany osobních údajů" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Dokumentace" }

<details class="downloads" markdown>
<summary>Ke stažení</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Vlastní domény a aliasy

Mailbox Mail vám umožňuje používat vlastní doménu a podporuje [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) adresy. Mailbox Mail také podporuje [sub-adresování](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), což je užitečné pro ty, kteří si nechtějí kupovat doménu.

#### :material-check:{ .pg-green } Soukromé platební metody

Mailbox Mail nepřijímá žádné kryptoměny, jelikož jejich platební brána BitPay v Německu přerušila svou činnost. Přijímají ale **hotovost** poštou, **hotovostní** platba na bankovní účet, bankovní převod, kreditní karty, PayPal a pár brán specifických pro Německo: Paydirekt a Sofortüberweisung.

#### :material-check:{ .pg-green } Zabezpečení účtu

Mailbox Mail podporuje [dvoufaktorové ověřování](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) jen pro svůj webmail. Můžete použít buď TOTP nebo [YubiKey](security-keys.md#yubikey) přes [YubiCloud](https://yubico.com/products/services-software/yubicloud). Webové standardy, jako je např. [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), nejsou zatím podporovány.

#### :material-information-outline:{ .pg-blue } Zabezpečení dat

Mailbox Mail umožňuje šifrování příchozí pošty pomocí jejich [šifrovaných schránek](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Nové zprávy, které obdržíte, budou automaticky zašifrované pomocí vašeho veřejného klíče.

[Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), softwarová platforma používaná Mailbox Mail, nicméně [nepodporuje](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) šifrování vašich kontaktů a kalendáře. Pro tato data může být vhodnější jiná, [oddělená služba](calendar.md).

#### :material-check:{ .pg-green } Šifrování e-malu

Mailbox Mail má [integrované šifrování](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) v jejich webmailu, které zjednodušuje posílání zpráv lidem s veřejnými OpenPGP klíči. Také umožňuje [vzdáleným příjemcům dešifrovat e-mail](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) na serverech Mailbox Mail. Tato funkce je užitečná v případě, že vzdálený příjemnce nemá OpenPGP a nemůže dešifrovat kopii e-mailu v jeho vlastní schránce.

Mailbox Mail také podporuje zjišťování veřejných klíču skrz HTTP z jejich WKD. To umožňuje lidem mimo Mailbox Mail najít OpenPGP klíče Mailbox. org účtů jednoduše pro E2EE mezi různými poskytovateli. To ale platí pouze pro e-mailové adresy ve vlastních doménách Mailbox Mail, jako je např. `@mailbox.org`. Pokud používáte vlastní doménu, je potřeba [nastavit WKD](basics/email-security.md#what-is-the-web-key-directory-standard) zvlášť.

#### :material-information-outline:{ .pg-blue } Ukončení účtu

Váš účet bude nastaven jako omezený, jakmile skončí vaše smlouva. Následně bude nenávratně smazaný po [30 dnech](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Dodatečné funkce

Můžete přistupovat ke svému Mailbox Mail účtu pomocí IMAP/SMTP skrz jejich [.onion službu](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Přes .onion službu ale nemůžete přistupovat k jejich webmail rozhraní a může docházet k chybám s TLS certifikátem.

Všechny účtu obsahují omezené cloudové úložiště, které [lze šifrovat](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox Mail také nabízí alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), který vynucuje TLS šifrování na spojení mezi poštovními servery, jinak se zpráva vůbec neodešle. Mailbox Mail také podporuje [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) kromě standardních přístupových protokolů, jako je IMAP nebo POP3.

Mailbox Mail má službu digitálního dědictví ve všech tarifech. Můžete si vybrat, která data budou poskytnuta vašim dědičům v případě, že o ně požádají a poskytnou vaši závěť. Případně můžete určit osobu podle jména a adresy.

## Více poskytovatelů

Tito poskytovatelé ukládají vaše e-maily pomocí zero-knowledge šifrování, které je skvělou možností pro zabezpečení vašich uložených e-mailů. Nepodporují však interoperabilní šifrovací standardy pro E2EE komunikaci napříč různými poskytovateli.

<div class="grid cards" markdown>

- ![logo Tuta](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![logo Tuta](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![logo Tuta](assets/img/email/tuta.svg#only-light){ align=right }
![logo Tuta](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (dříve *Tutanota*) je e-mailová služba se zaměřením na bezpečnost a soukromí prostřednictvím šifrování. Tuta působí od roku 2011 a sídlí v německém Hanoveru.

Bezplatné účty zahrnují 1 GB úložiště.

[:octicons-home-16: Domovská stránka](https://tuta.com/cs){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/cs/privacy){ .card-link title="Soukromí" }
[:octicons-info-16:](https://tuta.com/cs/support){ .card-link title="Podpora" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Zdrojový kód" }
[:octicons-heart-16:](https://tuta.com/cs/community){ .card-link title="Přispějte" }

<details class="downloads" markdown>
<summary>Ke stažení</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/cs#download)
- [:simple-apple: macOS](https://tuta.com/cs#download)
- [:simple-linux: Linux](https://tuta.com/cs#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta nepodporuje [IMAP protokol](https://tuta.com/support#imap) ani používání [e-mailových klientů](email-clients.md) třetích stran, a ani nemůžete přidat [externí e-mailové účtu](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) do aplikace Tuta. V současnosti není podporován ani [import e-mailů](https://github.com/tutao/tutanota/issues/630), což se [má však změnit](https://tuta.com/blog/kickoff-import). E-maily lze exportovat [jednotlivě nebo hromadně](https://tuta.com/support#generalMail) pro jednotlivé složky, což může být nemotorné, pokud máte více složek.

#### :material-check:{ .pg-green } Vlastní domény a aliasy

Placené Tuta účty mohou používat buď 15 nebo 30 aliasů v závislosti na jejich tarifu, a neomezené množství aliasů na [vlastních doménách](https://tuta.com/support#custom-domain). Tuta neumožňuje [sub-adresování (plusové adresy)](https://tuta.com/support#plus), ale můžete použít [univerzální](https://tuta.com/support#settings-global) adresu s vlastní doménou.

#### :material-information-outline:{ .pg-blue } Soukromé platební metody

Tuta přijímá pouze platební karty a PayPal. Přes [**kryptoměny**](cryptocurrency.md) lze ale zakoupit dárkové karty díky [spolupráci](https://tuta.com/support/#cryptocurrency) s ProxyStore.

#### :material-check:{ .pg-green } Zabezpečení účtu

Tuta podporuje [dvoufaktorové oveřování](https://tuta.com/support#2fa) pomocí TOTP nebo U2F.

#### :material-check:{ .pg-green } Zabezpečení dat

Tuta má [zero-access šifrování v klidu](https://tuta.com/support#what-encrypted) pro vaše e-maily, [kontakty v adresáři](https://tuta.com/support#encrypted-address-book) i [kalendáře](https://tuta.com/support#calendar). To znamená, že zprávy a jiná data uložená na vašem účtu můžete číst pouze vy.

#### :material-information-outline:{ .pg-blue } Šifrování e-mailů

Tuta [nepoužívá OpenPGP](https://tuta.com/support/#pgp). Tuta účtu mohou přijímat šifrované e-maily od účtů nepocházejících od Tuty pouze tehdy, když jsou odeslány přes [dočasnou Tuta schránku](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Ukončení účtu

Tuta [odstraní neaktivní bezplatné účty](https://tuta.com/support#inactive-accounts) po šesti měsících. Pokud zaplatíte, můžete znovu použít deaktivovaný bezplatný účet.

#### :material-information-outline:{ .pg-blue } Dodatečné funkce

Tuta nabízí firemní verzi [Tuty pro neziskové organizace](https://tuta.com/blog/secure-email-for-non-profit) buď zadarmo, nebo s výraznou slevou.

## Kritéria

**Upozorňujeme, že nespolupracujeme s žádným z poskytovatelů, které doporučujeme.** Kromě [našich standardních kritérií](about/criteria.md) jsme vypracovali jasný seznam požadavků pro každého e-mailového poskytovatele, který by si přál být doporučený, včetně zavedení osvědčených postupů v odvětví, moderních technologií a dalších. Doporučujeme, abyste se seznámili s tímto seznamem před tím, než se rozhodnete pro některého e-mailového poskytovatele, a také se sami přesvědčili, že daný e-mailový poskytovatel je správná volba pro vás.

### Technologie

Tyto funkce považujeme za důležité pro to, aby byla služba bezpečná a optimální. Měli byste brát v potaz, jestli daný poskytovatel má funkce, které potřebujete.

**Naprosté minimum:**

- Musí šifrovat data e-mailového účtu v klidu zero-access šifrováním.
- Musí být schopen exportovat e-maily jako [Mbox](https://en.wikipedia.org/wiki/Mbox) nebo jednotlivé .EML v normě [RFC5322](https://datatracker.ietf.org/doc/rfc5322).
- Umožňovat uživatelům používat jejich vlastní [domény](https://en.wikipedia.org/wiki/Domain_name). Vlastní domény jsou pro uživatele důležité, protože jim umožňují zachovávat nezávislost na službě, ať už z důvodu jejího úpadku nebo převzetí jinou společností, která nepovažuje soukromí za prioritu.
- Musí fungovat na vlastní infrastruktuře, tzn. že nesmí běžet na e-mailových službách třetích stran.

**Nejlepší případ:**

- Měla by šifrovat všechna data účtu (kontakty, kalendáře atd.) v klidu pomocí zero-access šifrování.
- Měla by pro jednoduchost poskytovat webmail s integrovaným E2EE/PGP šifrováním.
- Měla by podporovat WKD, aby bylo možné lépe nalézat veřejné OpenPGP klíče přes HTTP. Uživatelé GnuPG mohou získat klíč tímto příkazem: `gpg --locate-key uzivatel@priklad.cz`.
- Podporuje dočasné schránky pro externí uživatele. To je užitečné, pokud chcete poslat zašifrovaný e-mail, aniž byste odeslali skutečnou kopii příjemci. Tyto e-maily mají obvykle omezenou životnost a jsou následně smazány. Také nevyžadují od příjemce nastavování jakékoliv kryptografie, např. OpenPGP.
- Měla by podporovat [sub-adresování](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Měla by umožňovat uživatelům používat jejich vlastní [domény](https://en.wikipedia.org/wiki/Domain_name). Vlastní domény jsou pro uživatele důležité, protože jim umožňují zachovávat nezávislost na službě, ať už z důvodu jejího úpadku nebo převzetí jinou společností, která nepovažuje soukromí za prioritu.
- Funkce catch-all a aliasy pro ty, kteří chtějí používat svoje domény.
- Měla by používat standardní protokoly pro přístup k e-mailu, jako je IMAP, SMTP nebo [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standardní přístupové protokoly zajišťují, že si zákazníci mohou snadno stáhnout všechny svoje e-maily, kdyby se rozhodli změnit poskytovatele.
- Služby poskytovatele e-mailu by měly být dostupné přes [onion službu](https://en.wikipedia.org/wiki/.onion).

### Soukromí

Preferujeme, aby námi doporučení poskytovatelé shromažďovali co nejméně dat.

**Naprosté minimum:**

- Musí chránit IP adresu odesílatele, což může zahrnovat její odstranění v `Received` poli v hlavičce.
- Nesmí vyžadovat osobní údaje (personally identifiable information, PII) kromě uživatelského jména a hesla.
- Zásady ochrany osobních údajů musí splňovat požadavky definované GDPR.

**Nejlepší případ:**

- Měla by přijímat [anonymní platební metody](advanced/payments.md) ([kryptoměny](cryptocurrency.md), hotovost, dárkové poukazy atp.)
- Měla by být umístěna v jurisdikci se silnou právní ochranou e-mailového soukromí.

### Bezpečnost

E-mailové servery pracují s velkým množstvím citlivých dat. Očekáváme, že poskytovatelé implementují v odvětví osvědčené postupy, aby ochránili své zákazníky.

**Naprosté minimum:**

- Ochrana webmailu pomocí 2FA, např. [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access šifrování, které staví na šifrování v klidu. Poskytovatel nemá k dispozici dešifrovací klíče k datům, které jsou u něj uložené. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) support.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- A valid [MTA-STS](https://tools.ietf.org/html/rfc8461) and [TLS-RPT](https://tools.ietf.org/html/rfc8460) policy.
- Valid [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Valid [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) and [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) submission, assuming SMTP is used.
- Website security standards such as:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) if loading things from external domains.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Best Case:**

- Should support hardware authentication, i.e. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- Bug-bounty programs and/or a coordinated vulnerability-disclosure process.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Trust

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**Minimum to Qualify:**

- Public-facing leadership or ownership.

**Best Case:**

- Frequent transparency reports.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Minimum to Qualify:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Best Case:**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Additional Functionality

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
