---
title: "Strumenti di produttività"
icon: material/file-sign
description: La maggior parte delle suite per ufficio online non supportano la crittografia end-to-end, il che significa che il provider del cloud ha accesso a tutto ciò che fai.
---

La maggior parte delle suite per ufficio online non supportano la crittografia end-to-end, il che significa che il provider del cloud ha accesso a tutto ciò che fai. L'informativa sulla privacy potrebbe proteggere legalmente i tuoi diritti, ma non fornisce vincoli tecnici di accesso.

## Suite per ufficio

### LibreOffice

!!! recommendation

    ![Logo Nextcloud](assets/img/productivity/nextcloud.svg){ align=right }
    
    **Nextcloud** è una suite di software gratuiti e open-source client-server per la creazione di servizi di file hosting su un server privato controllato dall'utente.
    
    [:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Politica sulla Privacy" }
    [:octicons-info-16:](https://nextcloud.com/support/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Codice Sorgente" }
    [:octicons-heart-16:](https://nextcloud.com/contribute/){ .card-link title=Contribuisci }
    
    ??? download
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
        - [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
        - [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
        - [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
        - [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/www/nextcloud)

!!! attenzione

    Sconsigliamo di utilizzare l'[App E2EE](https://apps.nextcloud.com/apps/end_to_end_encryption) per Nextcloud, in quanto potrebbe causare la perdita di dati; è altamente sperimentale e non soddisfa i criteri di qualità. [:octicons-home-16: Pagina principale](https://www.onlyoffice.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://help.onlyoffice.com/products/files/doceditor.aspx?fileid=5048502&doc=SXhWMEVzSEYxNlVVaXJJeUVtS0kyYk14YWdXTEFUQmRWL250NllHNUFGbz0_IjUwNDg1MDIi0){ .card-link title="Informativa sulla privacy" }
    [:octicons-info-16:](https://helpcenter.onlyoffice.com/userguides.aspx){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/ONLYOFFICE){ .card-link title="Codice sorgente" }
    
    ???

### OnlyOffice

!!! recommendation

    ![Logo CryptPad](assets/img/productivity/cryptpad.svg){ align=right }
    
    **CryptPad** è un'alternativa privata e di design ai più diffusi strumenti per l'ufficio. Tutti i contenuti di questo servizio web sono criptati end-to-end e possono essere condivisi facilmente con altri utenti.
    
    [:octicons-home-16: Pagina principale](https://cryptpad.fr){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE/){ .card-link title="Informativa sulla privacy" }
    [:octicons-info-16:](https://docs.cryptpad.fr/){ .card-link title=Documentazione}
    [:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Codice sorgente" }
    [:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=Contribuisci }

### Criteri

**Si noti che non siamo affiliati a nessuno dei progetti che raccomandiamo.** Oltre ai [ nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari che ci consentono di fornire raccomandazioni obiettive. Ti consigliamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le vostre ricerche per assicurarvi che sia la scelta giusta per voi.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire criteri ben definiti per ogni sezione del nostro sito, e questo potrebbe essere soggetto a modifiche. Se avete domande sui nostri criteri, vi preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e non date per scontato che non abbiamo preso in considerazione qualcosa nel formulare le nostre raccomandazioni se non è elencato qui. Sono molti i fattori presi in considerazione e discussi quando consigliamo un progetto, e stiamo lavorando per documentare ogni singolo fattore.

In general, we define collaboration platforms as full-fledged suites which could reasonably act as a replacement to collaboration platforms like Google Drive.

- Open-source.
- Makes files accessible via WebDAV unless it is impossible due to E2EE.
- Has sync clients for Linux, macOS, and Windows.
- Supports document and spreadsheet editing.
- Supports real-time document collaboration.
- Supports exporting documents to standard document formats (e.g. ODF).

#### Caso migliore

KeePassXC memorizza i suoi dati di esportazione come file [CSV](https://en.wikipedia.org/wiki/Comma-separated_values). Ciò può comportare la perdita di dati se si importa questo file in un altro gestore di password.

- Should store files in a conventional filesystem.
- Should support TOTP or FIDO2 multi-factor authentication support, or Passkey logins.

## Servizi di paste

### PrivateBin

!!! recommendation

    ![LibreOffice logo](assets/img/productivity/libreoffice.svg){ align=right }
    
    **LibreOffice** is a free and open-source office suite with extensive functionality.
    
    [:octicons-home-16: Homepage](https://www.libreoffice.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.libreoffice.org/about-us/privacy/privacy-policy-en/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://documentation.libreoffice.org/en/english-documentation/){ .card-link title=Documentation}
    [:octicons-code-16:](https://www.libreoffice.org/about-us/source-code){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.libreoffice.org/donate/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://www.libreoffice.org/download/android-and-ios/)
        - [:simple-appstore: App Store](https://www.libreoffice.org/download/android-and-ios/)
        - [:simple-windows11: Windows](https://www.libreoffice.org/download/download/)
        - [:simple-apple: macOS](https://www.libreoffice.org/download/download/)
        - [:simple-linux: Linux](https://www.libreoffice.org/download/download/)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.libreoffice.LibreOffice)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/editors/libreoffice/)

### OnlyOffice

!!! recommendation

    ![OnlyOffice logo](assets/img/productivity/onlyoffice.svg){ align=right }
    
    **OnlyOffice** is a cloud-based free and open-source office suite with extensive functionality, including integration with Nextcloud.
    
    [:octicons-home-16: Homepage](https://www.onlyoffice.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://help.onlyoffice.com/products/files/doceditor.aspx?fileid=5048502&doc=SXhWMEVzSEYxNlVVaXJJeUVtS0kyYk14YWdXTEFUQmRWL250NllHNUFGbz0_IjUwNDg1MDIi0){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://helpcenter.onlyoffice.com/userguides.aspx){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/ONLYOFFICE){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onlyoffice.documents)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id944896972)
        - [:simple-windows11: Windows](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-apple: macOS](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-linux: Linux](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.onlyoffice.desktopeditors)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/www/onlyoffice-documentserver/)

### Criteri

**Si noti che non siamo affiliati a nessuno dei progetti che raccomandiamo.** Oltre ai [ nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari che ci consentono di fornire raccomandazioni obiettive. Ti consigliamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le vostre ricerche per assicurarvi che sia la scelta giusta per voi.

!!! esempio "Questa sezione è nuova"

    Stiamo lavorando per stabilire criteri ben definiti per ogni sezione del nostro sito, e questo potrebbe essere soggetto a modifiche. Se avete domande sui nostri criteri, vi preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e non date per scontato che non abbiamo preso in considerazione qualcosa nel formulare le nostre raccomandazioni se non è elencato qui. Sono molti i fattori presi in considerazione e discussi quando consigliamo un progetto, e stiamo lavorando per documentare ogni singolo fattore.

In general, we define office suites as applications which could reasonably act as a replacement for Microsoft Word for most needs.

- Deve essere multi-piattaforma.
- Deve essere un software open-source.
- Must function offline.
- Must support editing documents, spreadsheets, and slideshows.
- Must export files to standard document formats.

## Paste services

### PrivateBin

!!! recommendation

    ![PrivateBin logo](assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** is a minimalist, open-source online pastebin where the server has zero knowledge of pasted data. Data is encrypted/decrypted in the browser using 256-bit AES. It is the improved version of ZeroBin. There is a [list of instances](https://privatebin.info/directory/).
    
    [:octicons-home-16: Homepage](https://privatebin.info){ .md-button .md-button--primary }
    [:octicons-server-16:](https://privatebin.info/directory/){ .card-link title="Public Instances"}
    [:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/wiki/FAQ){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Source Code" }
