---
title: Impostazioni dei criteri di gruppo
description: A quick guide to configuring Group Policy to make Windows a bit more privacy respecting.
---

Outside modifying the registry itself, the **Local Group Policy Editor** is the most powerful way to change many aspects of your system without installing third-party tools. La modifica di queste impostazioni richiede [Pro Edition](index.md#windows-editions) o superiore.

These settings should be set on a brand-new installation of Windows. Setting them on your existing installation should work, but may introduce unpredictable behavior and is done at your own risk.

Tutte queste impostazioni sono accompagnate da una spiegazione nell'editor dei Criteri di gruppo che ne illustra esattamente le funzioni, di solito in modo molto dettagliato. Prestate attenzione a queste descrizioni mentre apportate le modifiche, in modo da sapere esattamente cosa vi stiamo raccomandando. Abbiamo anche spiegato alcune delle nostre scelte qui di seguito, quando la spiegazione inclusa in Windows è inadeguata.

## Modelli amministrativi

È possibile trovare queste impostazioni aprendo `gpedit.msc` e navigando in **Politica locale del computer** > **Configurazione del computer** > **Modelli amministrativi** nella barra laterale sinistra. Le intestazioni di questa pagina corrispondono alle cartelle/sottocartelle dei Modelli amministrativi, mentre i punti elenco corrispondono ai singoli criteri.

Per modificare un criterio di gruppo, fare doppio clic su di esso e selezionare Abilitato o Disabilitato nella parte superiore della finestra visualizzata, in base alle raccomandazioni riportate di seguito. Alcuni criteri di gruppo prevedono impostazioni aggiuntive che possono essere configurate; in questo caso, le impostazioni appropriate sono indicate anche di seguito.

### Sistema

#### Device Guard

- Attiva Sicurezza Basata Sulla Virtualizzazione: **Abilitato**
  - Livello di sicurezza della piattaforma: **Avvio sicuro e protezione DMA**
  - Configurazione Secure Launch: **Abilitato**

#### Gestione delle comunicazioni Internet

- Disattiva il programma di miglioramento dell'esperienza clienti di Windows: **Abilitato**
- Disattiva segnalazione errori di Windows: **Abilitato**
- Disattiva il programma di miglioramento dell'esperienza dei clienti di Windows Messenger: **Abilitato**

Si noti che la disabilitazione del programma di miglioramento dell'esperienza cliente di Windows disabilita anche alcune altre funzionalità di tracciamento che possono essere controllate individualmente anche con Criteri di gruppo. Non li elenchiamo tutti qui e non li disabilitiamo perché questa impostazione li copre.

#### Politiche del sistema operativo

- Permetti Cronologia Appunti: **Disabilitato**
- Consenti la sincronizzazione degli appunti tra i dispositivi: **Disabilitato**
- Abilita Feed Attività: **Disabilitato**
- Consenti la pubblicazione delle attività dell'utente: **Disabilitato**
- Consenti il caricamento delle attività dell'utente: **Disabilitato**

#### Profili Utente

- Disattiva l'ID pubblicitario: **Abilitato**

### Componenti di Windows

#### Politiche di AutoPlay

AutoRun e AutoPlay sono funzioni che consentono a Windows di eseguire uno script o qualche altra attività quando un dispositivo è connesso, talvolta evitando le misure di sicurezza che prevedono il consenso dell'utente. Ciò potrebbe consentire a dispositivi non affidabili di eseguire codice dannoso a tua insaputa. È una buona pratica di sicurezza disabilitare queste funzioni e aprire manualmente i file sui dischi esterni.

- Disattiva AutoPlay: **Abilitato**
- Disabilita Autoplay per dispositivi senza volume: **Abilitato**
- Imposta il comportamento predefinito per AutoRun: **Abilitato**
  - Comportamento AutoRun predefinito: **Non eseguire alcun comando AutoRun**

#### Crittografia unità BitLocker

Si potrebbe desiderare di ri-crittografare l'unità del sistema operativo dopo aver modificato queste impostazioni.

- Scegli il metodo di crittografia dell'unità e la forza della cifratura (Windows Vista, Windows Server 2008, Windows 7): **Abilitato**
  - Seleziona il metodo di cifratura: **AES-256**

Impostare la forza di cifratura per il criterio di Windows 7 continua ad applicare tale forza alle versioni più recenti di Windows.

##### Unità del Sistema Operativo

- Richiedi un'autenticazione aggiuntiva all'avvio: **Abilitato**
- Permetti i PIN migliorati per l'avvio: **Abilitato**

Despite the names of these policies, this doesn't _require_ you to do anything by default, but it will unlock the _option_ to have a more complex setup (such as requiring a PIN at startup in addition to the TPM) in the BitLocker setup wizard.

#### Contenuto cloud

- Disattiva il contenuto ottimizzato nel cloud: **Abilitato**
- Disattiva il contenuto dello stato dell'account del cloud consumer: **Abilitato**
- Non mostrare i suggerimenti di Windows: **Abilitato**
- Disattiva le esperienze dei consumatori Microsoft: **Abilitato**

#### Interfaccia Credenziale Utente

- Richiede un percorso attendibile per la voce credenziale: **Abilitato**
- Impedisci l'uso delle domande di sicurezza per gli account locali: **Abilitato**

#### Raccolta dati e anteprima Builds

- Permetti Dati Diagnostici: **Abilitato**
  - Opzioni: **Invia i dati diagnostici richiesti** (edizione Pro); oppure
  - Opzioni: **Dati diagnostici disattivati** (Edizione Enterprise o Education)
- Limita la raccolta dei registri diagnostici: **Abilitato**
- Limitae la raccolta di dump: **Abilitato**
- Limita i dati diagnostici opzionali per Desktop Analytics: **Abilitato**
  - Opzioni: **Disabilita la raccolta di Desktop Analytics**
- Non mostrare le notifiche di feedback: **Abilitato**

#### File Explorer

- Disattivare gli approfondimenti basati sull'account, i file recenti, preferiti e consigliati in Esplora file: **Abilitato**

#### MDM

- Disattivare l'iscrizione MDM: **Abilitato**

#### OneDrive

- Salva i documenti in OneDrive per impostazione predefinita: **Disabilitato**
- Impedire a OneDrive di generare traffico di rete finché l'utente non accede a OneDrive: **Abilitato**
- Impedire l'uso di OneDrive per l'archiviazione dei file: **Abilitato**

Quest'ultima impostazione disabilita OneDrive sul sistema; assicuratevi di cambiarla in **Disabilitato** se utilizzate OneDrive.

#### Push To Install

- Disattivare il servizio Push To Install: **Abilitato**

#### Ricerca

- Consenti Cortana: **Disabilitato**
- Non cercare sul web e non visualizzare i risultati web in Ricerca: **Abilitato**
- Imposta quali informazioni sono condivise in Ricerca: **Abilitato**
  - Tipo di informazioni: **Informazioni anonime**

#### Sincronizza le impostazioni

- Non sincronizzare: **Abilitato**

#### Inserimento testo

- Migliora il riconoscimento della scrittura e della digitazione: **Disabilitato**

#### Segnalazione degli errori di Windows

- Non inviare dati aggiuntivi: **Abilitato**
- Consenso > Configura consenso predefinito: **Abilitato**
  - Livello di consenso: **Chiedere sempre prima di inviare i dati**
