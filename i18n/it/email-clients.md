---
title: "Client Email"
icon: material/email-open
description: Questi client email rispettano la privacy e supportano la crittografia OpenPGP.
cover: email-clients.png
---

Il nostro elenco di raccomandazioni contiene client di posta elettronica che supportano sia [OpenPGP](encryption.md#openpgp) che l'autenticazione forte come [Open Authorization (OAuth)](https://it.wikipedia.org/wiki/OAuth). OAuth consente di utilizzare l'[autenticazione a più fattori](basics/multi-factor-authentication.md) e di prevenire il furto di account.

??? warning "L'e-mail non fornisce la segretezza dell'inoltro"

    Quando si utilizza una tecnologia di crittografia end-to-end (E2EE) come OpenPGP, le e-mail avranno ancora [alcuni metadati](email.md#email-metadata-overview) non crittografati nell'intestazione dell'e-mail.
    
    OpenPGP non supporta inoltre la [forward secrecy](https://it.wikipedia.org/wiki/Forward_secrecy), il che significa che se la chiave privata del destinatario o dell'utente viene rubata, tutti i messaggi precedenti crittografati con essa saranno esposti: [come proteggo le mie chiavi private?](basics/email-security.md) Considera l'utilizzo di un mezzo che garantisca la segretezza in avanti (forward secrecy):
    
    [Comunicazione in tempo reale](real-time-communication.md){ .md-button }

## Multipiattaforma

### Thunderbird

!!! recommendation

    ![Thunderbird logo](assets/img/email-clients/thunderbird.svg){ align=right }
    
    **Thunderbird** è un client di posta elettronica, newsgroup, news feed e chat (XMPP, IRC, Twitter) gratuito, open-source e multipiattaforma, sviluppato dalla comunità Thunderbird e precedentemente dalla Mozilla Foundation.
    
    [:octicons-home-16: Pagina principale](https://www.thunderbird.net){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/thunderbird){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title=Documentazione}
    [:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Codice sorgente" }
    
    ??? downloads "Scaricare"
    
        - [:simple-windows11: Windows](https://www.thunderbird.net)
        - [:simple-apple: macOS](https://www.thunderbird.net)
        - [:simple-linux: Linux](https://www.thunderbird.net)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

#### Configurazione consigliata

Si consiglia di modificare alcune di queste impostazioni per rendere Thunderbird un po' più privato.

Queste opzioni si trovano in :material-menu: → **Impostazioni** → **Privacy e sicurezza**.

##### Contenuto Web

- [ ] Deseleziona **Ricorda siti web e link visitati**
- [ ] Deseleziona  **Accetta i cookie dai siti**

##### Telemetria

- [ ] Deseleziona  **Consenti a Thunderbird di inviare a Mozilla dati tecnici e di interazione**

#### Thunderbird-user.js (avanzato)

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js), è un insieme di opzioni di configurazione che mira a disabilitare il maggior numero possibile di funzioni di navigazione web all'interno di Thunderbird, al fine di ridurre la superficie e mantenere la privacy. Alcune modifiche sono state prese dal [progetto Arkenfox](https://github.com/arkenfox/user.js).

## Specifiche alla piattaforma

### Apple Mail (macOS)

!!! recommendation

    ![Apple Mail logo](assets/img/email-clients/applemail.png){ align=right }
    
    **Apple Mail** è incluso in macOS e può essere esteso per avere il supporto OpenPGP con [GPG Suite](encryption.md#gpg-suite), che aggiunge la possibilità di inviare e-mail crittografate.
    
    [:octicons-home-16: Pagina Principale](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/legal/privacy/en-ww/){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://support.apple.com/mail){ .card-link title=Documentazione}

Apple Mail ha la possibilità di caricare contenuti in remoto in background o di bloccarli completamente nascondendo il tuo indirizzo IP dai mittenti su [macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) e [iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios).

### Canary Mail (iOS)

!!! recommendation

    ![Canary Mail logo](assets/img/email-clients/canarymail.svg){ align=right }
    
    **Canary Mail** è un client di posta elettronica a pagamento progettato per rendere perfetta la crittografia end-to-end con funzioni di sicurezza come il blocco biometrico dell'app.
    
    [:octicons-home-16: Pagina principale](https://canarymail.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://canarymail.io/privacy.html){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://canarymail.zendesk.com/){ .card-link title=Documentazione}
    
    ??? downloads "Scaricare"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.canarymail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1236045954)
        - [:simple-windows11: Windows](https://canarymail.io/downloads.html)

!!! warning "Attenzione"

    Canary Mail ha rilasciato solo di recente un client per Windows e Android, anche se non crediamo che siano stabili come le loro controparti per iOS e Mac.

Canary Mail è closed-source. Lo consigliamo a causa della scarsa scelta di client email su iOS che supportano la E2EE PGP.

### FairEmail (Android)

!!! recommendation

    ![logo FairEmail ](assets/img/email-clients/fairemail.svg){ align=right }
    
    **FairEmail** è un'applicazione di posta elettronica minimale e open-source, che utilizza standard aperti (IMAP, SMTP, OpenPGP) con un basso consumo di dati e batteria.
    
    [:octicons-home-16: Pagina principale](https://email.faircode.eu){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://email.faircode.eu/donate/){ .card-link title=Contribuisci }
    
    ??? downloads "Scaricare"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
        - [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

### GNOME Evolution (GNOME)

!!! recommendation

    ![Evolution logo](assets/img/email-clients/evolution.svg){ align=right }
    
    **Evolution** è un'applicazione per la gestione delle informazioni personali che fornisce funzionalità integrate di posta, calendario e rubrica. Evolution dispone di un'ampia [documentazione](https://help.gnome.org/users/evolution/stable/) per aiutarti a iniziare.
    
    [:octicons-home-16: Pagina principale](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://help.gnome.org/users/evolution/stable/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution/){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://www.gnome.org/donate/){ .card-link title=Contribuisci }
    
    ??? downloads "Scaricare"
    
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

### K-9 Mail (Android)

!!! recommendation

    ![K-9 Mail logo](assets/img/email-clients/k9mail.svg){ align=right }
    
    **K-9 Mail** è un'applicazione di posta elettronica indipendente che supporta sia le caselle POP3 che IMAP, ma supporta solo la posta push per IMAP.
    
    In futuro, K-9 Mail sarà il client [ufficiale](https://k9mail.app/2022/06/13/K-9-Mail-and-Thunderbird.html) di Thunderbird per Android.
    
    [:octicons-home-16: Pagina principale](https://k9mail.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://k9mail.app/privacy){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://docs.k9mail.app/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/k9mail/k-9){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://k9mail.app/contribute){ .card-link title=Contribuisci }
    
    ??? downloads "Scaricare"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
        - [:simple-github: GitHub](https://github.com/k9mail/k-9/releases)

!!! warning "Attenzione"

    ![Kontact logo](assets/img/email-clients/kontact.svg){ align=right }
    
    **Kontact** è un'applicazione di gestione delle informazioni personali (PIM, personal information manager) del progetto [KDE](https://kde.org). Offre un client di posta, una rubrica, un'agenda e un client RSS.

### Kontact (KDE)

!!! recommendation

    ![Logo Kontact](assets/img/email-clients/kontact.svg){ align=right }
    
    **Kontact** è un'applicazione di gestione delle informazioni personali (PIM) del progetto [KDE](https://kde.org). Offre un client email, una rubrica, un'agenda e un client RSS.
    
    [:octicons-home-16: Pagina Principale](https://kontact.kde.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://kontact.kde.org/users/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://kde.org/community/donations/){ .card-link title=Contribuisci }
    
    ??? downloads "Scaricare"
    
        - [:simple-linux: Linux](https://kontact.kde.org/download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

### Mailvelope (Browser)

!!! recommendation

    ![Logo Mailvelope](assets/img/email-clients/mailvelope.svg){ align=right }
    
    **Mailvelope** è un'estensione del browser che consente lo scambio di e-mail crittografate secondo lo standard di crittografia OpenPGP.
    
    [:octicons-home-16: Pagina Principale](https://www.mailvelope.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mailvelope.com/en/privacy-policy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://mailvelope.com/faq){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="Codice Sorgente" }
    
    ??? downloads "Scaricare"
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

### NeoMutt (CLI)

!!! recommendation

    ![NeoMutt logo](assets/img/email-clients/mutt.svg){ align=right }
    
    **NeoMutt** è un lettore di posta elettronica a riga di comando open-source (or MUA) per Linux e BSD. È un fork di [Mutt](https://it.wikipedia.org/wiki/Mutt) con funzionalità aggiuntive.
    
    NeoMutt è un client basato sul testo che ha una curva di apprendimento molto ripida. Tuttavia, è molto personalizzabile.
    
    [:octicons-home-16: Pagina Principale](https://neomutt.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://neomutt.org/guide/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://www.paypal.com/paypalme/russon/){ .card-link title=Contribuisci }
    
    ??? downloads "Scaricare"
    
        - [:simple-apple: macOS](https://neomutt.org/distro)
        - [:simple-linux: Linux](https://neomutt.org/distro)

## Criteri

**Si noti che non siamo affiliati a nessuno dei progetti che raccomandiamo.** Oltre ai [ nostri criteri standard ](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari che ci consentono di fornire raccomandazioni oggettive. Ti consigliamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che sia la scelta giusta per te.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire criteri definiti per ogni sezione del nostro sito, e questo potrebbe essere soggetto a modifiche. Se avete domande sui nostri criteri, vi preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e non date per scontato che non abbiamo preso in considerazione qualcosa nel formulare le nostre raccomandazioni se non è elencato qui. Sono molti i fattori presi in considerazione e discussi quando consigliamo un progetto, e stiamo lavorando per documentare ogni singolo fattore.

### Requisiti minimi

- Le applicazioni sviluppate per sistemi operativi open-source devono essere open-source.
- Non deve raccogliere la telemetria o deve avere un modo semplice per disabilitare tutta la telemetria.
- Deve supportare la crittografia dei messaggi OpenPGP.

### Criteri Ottimali

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. Le nostre raccomandazioni potrebbero non includere tutte o alcune di queste funzionalità, ma quelle che le includono potrebbero avere una posizione più alta rispetto ad altre in questa pagina.

- Dovrebbe essere open-source.
- Dovrebbe essere multipiattaforma.
- Non dovrebbe raccogliere alcuna telemetria per impostazione predefinita.
- Deve supportare OpenPGP in modo nativo, cioè senza estensioni.
- Dovrebbe supportare l'archiviazione locale delle e-mail crittografate OpenPGP.
