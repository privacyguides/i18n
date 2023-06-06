---
title: "Strumenti per la produttività"
icon: material/file-sign
description: La maggior parte delle suite per ufficio online non supportano la crittografia end-to-end, il che significa che il provider del cloud ha accesso a tutto ciò che fai.
cover: productivity.png
---

La maggior parte delle suite per ufficio online non supportano la crittografia end-to-end, il che significa che il provider del cloud ha accesso a tutto ciò che fai. L'informativa sulla privacy potrebbe proteggere legalmente i tuoi diritti, ma non fornisce vincoli tecnici di accesso.

## Suite per ufficio

### LibreOffice

!!! recommendation

    ![Logo Nextcloud](assets/img/productivity/nextcloud.svg){ align=right }
    
    **Nextcloud** è una suite di software gratuiti e open-source client-server per la creazione di servizi di file hosting su un server privato controllato dall'utente.
    
    [:octicons-home-16: Pagina Principale](https://nextcloud.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://nextcloud.com/support/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://nextcloud.com/contribute/){ .card-link title=Contribuisci }
    
    ??? downloads "Scaricare"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
        - [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
        - [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
        - [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
        - [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/www/nextcloud)

!!! danger "Attenzione"

    Sconsigliamo di utilizzare l'[App E2EE](https://apps.nextcloud.com/apps/end_to_end_encryption) per Nextcloud, in quanto potrebbe causare la perdita di dati; è altamente sperimentale e non soddisfa i criteri di qualità. Per questo motivo, non consigliamo i provider Nextcloud di terze parti.

### OnlyOffice

!!! recommendation

    ![Logo CryptPad](assets/img/productivity/cryptpad.svg){ align=right }
    
    **CryptPad** è un'alternativa privata e di design ai più diffusi strumenti per l'ufficio. Tutti i contenuti di questo servizio web sono criptati end-to-end e possono essere condivisi facilmente con altri utenti.
    
    [:octicons-home-16: Pagina Principale](https://cryptpad.fr){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE/){ .card-link title="Politica sulla privacy" }
    [:octicons-info-16:](https://docs.cryptpad.fr/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=Contribuisci }

### Criteri

**Si noti che non siamo affiliati a nessuno dei progetti che raccomandiamo.** Oltre ai [ nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari che ci consentono di fornire raccomandazioni obiettive. Ti consigliamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le vostre ricerche per assicurarvi che sia la scelta giusta per voi.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire criteri ben definiti per ogni sezione del nostro sito, e questo potrebbe essere soggetto a modifiche. Se avete domande sui nostri criteri, vi preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e non date per scontato che non abbiamo preso in considerazione qualcosa nel formulare le nostre raccomandazioni se non è elencato qui. Sono molti i fattori presi in considerazione e discussi quando consigliamo un progetto, e stiamo lavorando per documentare ogni singolo fattore.

In generale, definiamo le piattaforme di collaborazione come suite complete che possono facilmente sostituire piattaforme di collaborazione come Google Drive.

- Open-source.
- Rende i file accessibili tramite WebDAV, a meno che non sia impossibile a causa dell'E2EE.
- Dispone di client di sincronizzazione per Linux, macOS e Windows.
- Supporta la modifica dei documenti e fogli di calcolo.
- Supporta la collaborazione in tempo reale sui documenti.
- Supporta l'esportazione di documenti in formati standard (ad esempio ODF).

#### Caso migliore

KeePassXC memorizza i suoi dati di esportazione come file [CSV](https://en.wikipedia.org/wiki/Comma-separated_values). Ciò può comportare la perdita di dati se si importa questo file in un altro gestore di password.

- Dovrebbe memorizzare i file in un filesystem convenzionale.
- Dovrebbe supportare l'autenticazione a più fattori TOTP o FIDO2, o i login con Passkey.

## Servizi di paste

### PrivateBin

!!! recommendation

    ![Logo LibreOffice](assets/img/productivity/libreoffice.svg){ align=right }
    
    **LibreOffice** è una suite per ufficio gratuita e open-source con diverse funzionalità.
    
    [:octicons-home-16: Pagina Principale](https://www.libreoffice.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.libreoffice.org/about-us/privacy/privacy-policy-en/){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://documentation.libreoffice.org/it/documentazione-in-italiano/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://it.libreoffice.org/chi-siamo/codice-sorgente/){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://it.libreoffice.org/donazioni/){ .card-link title=Contribuisci }
    
    ??? download
    
        - [:simple-googleplay: Google Play](https://www.libreoffice.org/download/android-and-ios/)
        - [:simple-appstore: App Store](https://www.libreoffice.org/download/android-and-ios/)
        - [:simple-windows11: Windows](https://www.libreoffice.org/download/download/)
        - [:simple-apple: macOS](https://www.libreoffice.org/download/download/)
        - [:simple-linux: Linux](https://www.libreoffice.org/download/download/)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.libreoffice.LibreOffice)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/editors/libreoffice/)

### OnlyOffice

!!! recommendation

    ![Logo OnlyOffice](assets/img/productivity/onlyoffice.svg){ align=right }
    
    **OnlyOffice** è una suite per ufficio gratuita e open-source basata su cloud con diverse funzionalità, tra cui l'integrazione con Nextcloud.
    
    [:octicons-home-16: Pagina Principale](https://www.onlyoffice.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://help.onlyoffice.com/products/files/doceditor.aspx?fileid=5048502&doc=SXhWMEVzSEYxNlVVaXJJeUVtS0kyYk14YWdXTEFUQmRWL250NllHNUFGbz0_IjUwNDg1MDIi0){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://helpcenter.onlyoffice.com/userguides.aspx){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/ONLYOFFICE){ .card-link title="Codice Sorgente" }
    
    ??? download
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onlyoffice.documents)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id944896972)
        - [:simple-windows11: Windows](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-apple: macOS](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-linux: Linux](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.onlyoffice.desktopeditors)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/www/onlyoffice-documentserver/)

### Criteri

**Si noti che non siamo affiliati a nessuno dei progetti che raccomandiamo.** Oltre ai [ nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari che ci consentono di fornire raccomandazioni obiettive. Ti consigliamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le vostre ricerche per assicurarvi che sia la scelta giusta per voi.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire criteri ben definiti per ogni sezione del nostro sito, e questo potrebbe essere soggetto a modifiche. Se avete domande sui nostri criteri, vi preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e non date per scontato che non abbiamo preso in considerazione qualcosa nel formulare le nostre raccomandazioni se non è elencato qui. Sono molti i fattori presi in considerazione e discussi quando consigliamo un progetto, e stiamo lavorando per documentare ogni singolo fattore.

In generale, definiamo suite per ufficio le applicazioni che possono facilmente sostituire Microsoft Word per la maggior parte delle esigenze.

- Deve essere multi-piattaforma.
- Deve essere un software open-source.
- Deve funzionare offline.
- Deve supportare la modifica dei documenti, fogli di calcolo e presentazioni.
- Deve esportare i file in formati documenti standard.

## Servizi Paste

### PrivateBin

!!! recommendation

    ![logo PrivateBin](assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** è un pastebin online minimalista e open-source in cui il server non ha alcuna conoscenza dei dati incollati. I dati vengono criptati/decriptati nel browser utilizzando AES a 256 bit. È la versione migliorata di ZeroBin. Esiste un [elenco di istanze](https://privatebin.info/directory/).
    
    [:octicons-home-16: Pagina Principale](https://privatebin.info){ .md-button .md-button--primary }
    [:octicons-server-16:](https://privatebin.info/directory/){ .card-link title="Istanze pubbliche"}
    [:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/wiki/FAQ){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Codice Sorgente" }

### Criteri

**Si noti che non siamo affiliati a nessuno dei progetti che raccomandiamo.** Oltre ai [ nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari che ci consentono di fornire raccomandazioni obiettive. Ti consigliamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le vostre ricerche per assicurarvi che sia la scelta giusta per voi.

!!! example "Questa sezione è nuova"

    Stiamo lavorando per stabilire criteri ben definiti per ogni sezione del nostro sito, e questo potrebbe essere soggetto a modifiche. Se avete domande sui nostri criteri, vi preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e non date per scontato che non abbiamo preso in considerazione qualcosa nel formulare le nostre raccomandazioni se non è elencato qui. Sono molti i fattori presi in considerazione e discussi quando consigliamo un progetto, e stiamo lavorando per documentare ogni singolo fattore.

#### Requisiti minimi

- Devono essere open-source.
- Deve implementare la crittografia end-to-end "zero-trust".
- Deve supportare i file protetti da password.


#### Caso migliore

KeePassXC memorizza i suoi dati di esportazione come file [CSV](https://en.wikipedia.org/wiki/Comma-separated_values). Ciò può comportare la perdita di dati se si importa questo file in un altro gestore di password.

- Dovrebbe avere un audit pubblicato da un ente di terze parti affidabile e indipendente.
