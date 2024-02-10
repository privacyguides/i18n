---
title: "Client Email"
icon: material/email-open
description: Questi client di posta elettronica rispettano la privacy e supportano la crittografia OpenPGP.
cover: email-clients.webp
---

Il nostro elenco di consigli contiene i client email che supportano sia [OpenPGP](encryption.md#openpgp) che l'autenticazione forte, come [Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth). OAuth consente di utilizzare l'[autenticazione a più fattori](basics/multi-factor-authentication.md) e di prevenire il furto del profilo.

<details class="warning" markdown>
<summary>L'email non fornisce la forward secrecy</summary>

Quando si utilizza una tecnologia di crittografia end-to-end (E2EE) come OpenPGP, le e-mail avranno ancora [alcuni metadati](email.md#email-metadata-overview) non crittografati nell'intestazione dell'e-mail.

OpenPGP non supporta inoltre la [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), il che significa che se la tua chiave privata o quella del destinatario viene rubata, tutti i messaggi precedenti crittografati con essa saranno esposti: [Come posso proteggere le mie chiavi private?](basics/email-security.md) Considera la possibilità di utilizzare un mezzo di comunicazione che garantisca la forward secrecy:

[Comunicazione in tempo reale](real-time-communication.md ""){.md-button}

</details>

## Multipiattaforma

### Thunderbird

<div class="admonition recommendation" markdown>

![Logo di Thunderbird](assets/img/email-clients/thunderbird.svg){ align=right }

**Thunderbird** è un client email, newsgroup, feed di notizie e chat (XMPP, IRC, Twitter) gratuito, open source e multipiattaforma, sviluppato dalla community di Thunderbird e precedentemente dalla Mozilla Foundation.

[:octicons-home-16: Homepage](https://www.thunderbird.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.mozilla.org/privacy/thunderbird){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title=Documentazione}
[:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-windows11: Windows](https://www.thunderbird.net)
- [:simple-apple: macOS](https://www.thunderbird.net)
- [:simple-linux: Linux](https://www.thunderbird.net)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

</details>

</div>

#### Configurazione consigliata

Consigliamo di modificare alcune di queste impostazioni per rendere Thunderbird un po' più privato.

Queste opzioni si trovano in :material-menu: → **Impostazioni** → **Privacy e Sicurezza**.

##### Contenuti Web

- [ ] Rimuovi la spunta da **Ricorda siti web e link visitati**
- [ ] Rimuovi la spunta da **Accetta i cookie dai siti**

##### Telemetria

- [ ] Rimuovi la spunta da **Consenti a Thunderbird di inviare a Mozilla dati tecnici e d'interazione**

#### Thunderbird-user.js (avanzato)

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js), è una serie di opzioni di configurazione che mira a disabilitare quante più funzionalità di navigazione web possibili su Thunderbird, per poter ridurre la superficie e mantenere la privacy. Alcune delle modifiche provengono dal [progetto Arkenfox](https://github.com/arkenfox/user.js).

## Specifiche della Piattaforma

### Apple Mail (macOS)

<div class="admonition recommendation" markdown>

![Logo di Apple Mail](assets/img/email-clients/applemail.png){ align=right }

**Apple Mail** è incluso in macOS ed è estendibile per supportare OpenPGP con [GPG Suite](encryption.md#gpg-suite), che aggiunge la possibilità di inviare email crittografate in PGP.

[:octicons-home-16: Home](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.apple.com/legal/privacy/en-ww/){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://support.apple.com/mail){ .card-link title=Documentazione}

</details>

</div>

Apple Mail può caricare i contenuti da remoto in background o bloccarli interamente e nascondere l'indirizzo IP di mittenti su [macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) e [iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios).

### Canary Mail (iOS)

<div class="admonition recommendation" markdown>

![Logo di Canary Mail](assets/img/email-clients/canarymail.svg){ align=right }

**Canary Mail** è un client email a pagamento progettato per semplificare la crittografia end-to-end con funzionaalità di sicurezza come il blocco biometrico dell'app.

[:octicons-home-16: Homepage](https://canarymail.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://canarymail.io/privacy.html){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://canarymail.zendesk.com/){ .card-link title=Documentazione}

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.canarymail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1236045954)
- [:simple-windows11: Windows](https://canarymail.io/downloads.html)

</details>

</div>

<details class="warning" markdown>
<summary>Avviso</summary>

Canary Mail ha rilasciato soltanto di recente un client per Windows e Android, sebbene non crediamo sia altrettanto stabile, quanto le controparti per iOS e Mac.

</details>

Canary Mail è closed-source. Lo consigliamo a causa di alcune scelte per i client email su iOS, che supportano l'E2EE PGP.

### FairEmail (Android)

<div class="admonition recommendation" markdown>

![Logo di FairEmail ](assets/img/email-clients/fairemail.svg){ align=right }

**FairEmail** è un'app di email minimale e open source che utilizza gli standard apeerti (IMAP, SMTP, OpenPGP), con un basso consumo di dati e batteria.

[:octicons-home-16: Homepage](https://email.faircode.eu){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://email.faircode.eu/donate/){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
- [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

</details>

</div>

### GNOME Evolution (GNOME)

<div class="admonition recommendation" markdown>

![Logo di Evolution](assets/img/email-clients/evolution.svg){ align=right }

**Evolution** è un'applicazione per la gestione delle informazioni personali che fornisce funzionalità integrate di email, calendario e rubrica. Evolution dispone di un'ampia [documentazione](https://help.gnome.org/users/evolution/stable/) per aiutarti a iniziare.

[:octicons-home-16: Homepage](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
[:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://help.gnome.org/users/evolution/stable/){ .card-link title=Documentazione}
[:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution/){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://www.gnome.org/donate/){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

</details>

</div>

### K-9 Mail (Android)

<div class="admonition recommendation" markdown>

![Logo di K-9 Mail](assets/img/email-clients/k9mail.svg){ align=right }

**K-9 Mail** è un'applicazione indipendente di email che supporta le caselle POP3 e IMAP, ma supporta soltanto le email push per IMAP.

In futuro, K-9 Mail sarà il client [ufficiale](https://k9mail.app/2022/06/13/K-9-Mail-and-Thunderbird.html) di Thunderbird per Android.

[:octicons-home-16: Homepage](https://k9mail.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://k9mail.app/privacy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://docs.k9mail.app/){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/thundernest/k-9){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://k9mail.app/contribute){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
- [:simple-github: GitHub](https://github.com/thundernest/k-9/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Rispondendo a qualcuno in una mailing list, l'opzione "rispondi" potrebbe includere anche la mailing list stessa. Per maggiori informazioni visita il ticket [#3738 di thundernest/k-9](https://github.com/thundernest/k-9/issues/3738).

</div>

### Kontact (KDE)

<div class="admonition recommendation" markdown>

![Logo di Kontact](assets/img/email-clients/kontact.svg){ align=right }

**Kontact** è un'applicazione di gestione delle informazioni personali (PIM), dal progetto [KDE](https://dke.org). Fornisce un client email, rubrica, un'agenda e un client RSS.

[:octicons-home-16: Homepage](https://kontact.kde.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://kontact.kde.org/users/){ .card-link title=Documentazione}
[:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://kde.org/community/donations/){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-linux: Linux](https://kontact.kde.org/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

</details>

</div>

### Mailvelope (Browser)

<div class="admonition recommendation" markdown>

![Logo di Mailvelope](assets/img/email-clients/mailvelope.svg){ align=right }

**Mailvelope** è un'estensione del browser che consente lo scambio di email crittografate secondo lo standard di crittografia OpenPGP.

[:octicons-home-16: Homepage](https://www.mailvelope.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.mailvelope.com/en/privacy-policy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://mailvelope.com/faq){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

</details>

</div>

### NeoMutt (CLI)

<div class="admonition recommendation" markdown>

![Logo di NeoMutt](assets/img/email-clients/mutt.svg){ align=right }

**NeoMutt** è un lettore di email a riga di comando (MUA) open source per Linux e BSD. È una biforcazione di [Mutt](https://it.wikipedia.org/wiki/Mutt) con funzionalità aggiuntive.

NeoMutt è un client basato su testo con una curva d'apprendimento molto rapida. Tuttavia, è molto personalizzabile.

[:octicons-home-16: Homepage](https://neomutt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://neomutt.org/guide/){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="Codice sorgente"}
[:octicons-heart-16:](https://www.paypal.com/paypalme/russon/){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-apple: macOS](https://neomutt.org/distro)
- [:simple-linux: Linux](https://neomutt.org/distro)

</details>

</div>

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

<div class="admonition example" markdown>
<p class="admonition-title">Questa sezione è nuova</p>

Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

</div>

### Requisiti minimi

- Le applicazioni sviluppate per sistemi operativi open source devono essere open source.
- Non devono raccogliere telemetria, o deve disporre di un metodo facile per disabilitare tutta la telemetria.
- Deve supportare la crittografia dei messaggi OpenPGP.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Dovrebbe essere open source.
- Dovrebbe essere multipiattaforma.
- Non dovrebbe raccogliere alcuna telemetria di default.
- Deve supportare OpenPGP nativamente, cioè senza estensioni.
- Dovrebbe supportare l'archiviazione locale delle email crittografate, OpenPGP.
