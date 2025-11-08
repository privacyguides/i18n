---
title: Social network
icon: material/account-supervisor-circle-outline
description: Trova un nuovo social network che non ficchi il naso nei tuoi dati o che monetizzi il tuo profilo.
cover: social-networks.webp
---

<small>Protezione dalle seguenti minacce:</small>

- [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }
- [:material-account-cash: Capitalismo della Sorveglianza](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Questi **social network** che rispettano la privacy ti consentono di partecipare alle comunità online senza fornire informazioni personali come nome e cognome, numero di telefono e altri dati comunemente richiesti dalle aziende tecnologiche.

Un problema crescente nelle piattaforme di social media è la censura, in due forme diverse. In primo luogo, spesso acconsentono a richieste di censura illegittime, sia da parte di governi malintenzionati che delle loro politiche interne. In secondo luogo, spesso richiedono account per accedere a contenuti tagliati fuori, che altrimenti verrebbero pubblicati liberamente sull'internet aperto; ciò censura di fatto le attività di navigazione degli utenti attenti alla privacy che non sono in grado di pagare il costo di apertura di un account su queste reti.

I social network che raccomandiamo risolvono il problema della censura operando su un protocollo di social networking aperto e decentralizzato. Essi inoltre non richiedono un account solamente per visualizzare i contenuti disponibili pubblicamente.

Dovresti tenere in considerazione che i social network **non** sono adatti per le comunicazioni private o sensibili. Per chattare direttamente con gli altri, dovresti utilizzare uno dei [software di messaggistica istantanea](real-time-communication.md) consigliati, con una forte crittografia end-to-end e di utilizzare i messaggi diretti sui social media solamente per instaurare una chat con i tuoi contatti su una piattaforma più privata e sicura.

## Decentralizzazione

I social network decentralizzati sono costruiti su un'architettura che è fondamentalmente differente dalle piattaforme di social media mainstream, ma è molto simile alla struttura sottostante alle email. Invece di aprire un account per un singolo servizio unificato come faresti per Facebook o Discord, puoi scegliere un server pubblico e indipendente a cui unirti. Il server su cui ti unisci può comunicare e scoprire gli altri server; questo aspetto della decentralizzazione è noto anche come _federazione_.

Un beneficio significativo di questo modello decentralizzato è che non c'è un'autorità centrale che può censurare il tuo account attraverso l'intera rete, ma è possibile che il tuo account venga bannato o silenziato da un singolo server.

In questo modello decentralizzato ogni server è un'entità legale a sé stante, con una propria informativa sulla privacy, termini di utilizzo, team di amministrazione e moderatori. Mentre molti di questi server sono molto _meno_ restrittivi e più rispettosi della privacy rispetto alle piattaforme di social media tradizionali, alcuni possono essere molto _più_ restrittivi o potenzialmente _peggiori_ per la tua privacy. In genere, il software su cui si basa il social network non fa discriminazioni tra questi amministratori né pone limitazioni ai loro poteri.

## Resistenza alla Censura

Mentre la censura nei social network decentralizzati non esiste a livello della rete, è possibile sperimentare la censura a livello del server a seconda dell'amministratore del server. Gli amministratori hanno il potere di _defederarsi_ da altri server, il che porta a limitare i contenuti che puoi visualizzare e le persone con cui puoi interagire.

Se sei molto preoccupato per un server esistente che censura i tuoi contenuti, i contenuti a tua disposizione o altri server, in genere hai due opzioni:

1. **Ospita tu stesso il software del social network.** Questo approccio ti dà esattamente la stessa resistenza alla censura che qualsiasi altro sito web che puoi ospitare tu stesso, il quale è abbastanza alto.

2. **Usa un servizio di hosting gestito.** Non abbiamo alcuna raccomandazione specifica, ma ci sono una varietà di servizi di hosting che creeranno un server nuovo di zecca su un tuo dominio (o occasionalmente un sottodominio del loro dominio, ma non ti consigliamo questa opzione a meno che la registrazione del proprio dominio presenti un onere eccessivo per la tua privacy).

   In genere, i provider di hosting si occupano della parte _tecnica_ del tuo server, ma lasciano completamente a te la parte di _moderazione_. Per la maggior parte delle persone questo rappresenta un approccio migliore rispetto al self-hosting, in quanto si può beneficiare di un maggiore controllo sul proprio server senza preoccuparsi di problemi tecnici o vulnerabilità di sicurezza non risolte.

   Prima di registrarti dovresti esaminare attentamente le condizioni di servizio del tuo provider di hosting e l'informativa degli utilizzi accettabili. Queste sono spesso molto più ampie delle normali regole di server hosted e hanno molta meno probabilità di essere applicate senza ricorso, ma possono comunque essere restrittive in modi indesiderati.

## Mastodon

<div class="admonition recommendation" markdown>

![Logo di Mastodon](assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** è un social network basato su protocolli web aperti e su software libero e open source. Utilizza il protocollo **:simple-activitypub: ActivityPub** che è decentralizzato come le email: gli utenti possono esistere su server diversi o persino piattaforme diverse, ma ancora comunicare tra di loro.

[:octicons-home-16: Pagina Principale](https://joinmastodon.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.joinmastodon.org){ .card-link title="Documentazione" }

</div>

Esistono molte piattaforme software che utilizzano ActivityPub come protocollo di backend per il social network, questo significa che possono dialogare con altri server anche quando questi eseguono software diversi. Ad esempio, PeerTube è un software di pubblicazione video che utilizza ActivityPub, il che significa che è possibile seguire i canali su PeerTube con un altro account PeerTube, _o_ con un account Mastodon, perché anche Mastodon utilizza ActivityPub.

Abbiamo scelto di consigliare Mastodon rispetto ad altri software ActivityPub come social media pricipale per questi motivi:

1. Mastodon ha una solida storia di aggiornamenti di sicurezza. Nelle poche circostanze in cui sono state riscontrate gravi vulnerabilità di sicurezza, coordinano il rilascio delle patch in modo rapido e pulito. Storicamente hanno riportato queste patch di sicurezza anche nelle versioni più vecchie. Questo rende più facile per gli host di server meno esperti, che potrebbero non sentirsi a proprio agio nell'aggiornare subito alle ultime versioni, mantenere le loro istanze sicure. Mastodon dispone anche di un sistema di notifica degli aggiornamenti integrato nell'interfaccia web, che rende molto più probabile che gli amministratori dei server siano a conoscenza delle patch di sicurezza critiche disponibili per la loro istanza.

2. Mastodon è ampiamente utilizzabile con la maggior parte dei tipi di contenuto. Pur essendo principalmente una piattaforma di microblogging, Mastodon gestisce facilmente post più lunghi, post con immagini, post con video e la maggior parte degli altri post che si possono incontrare quando si seguono utenti ActivityPub che non sono su Mastodon. Questo rende il tuo account Mastodon un "hub centrale" ideale per seguire chiunque indipendentemente dalla piattaforma che hanno scelto di utilizzare. Al contrario, se utilizzassi solo un account PeerTube, potresti _solo_ seguire altri canali video, ad esempio.

3. Mastodon dispone di controlli sulla privacy abbastanza completi. Ha molte funzionalità integrate che ti permettono di limitare come e quando i tuoi dati sono condivisi, alcune delle quali copriremo qui sotto. Inoltre, sviluppano le nuove funzionalità tenendo conto della privacy. Ad esempio, mentre altri software ActivityPub hanno implementato rapidamente i "post di citazione" limitandosi a gestire i link ad altri post con un modo di incorporamento leggermente diverso, Mastodon sta [sviluppando](https://blog.joinmastodon.org/2025/02/bringing-quote-posts-to-mastodon) una funzione di post di citazione che ti darà un controllo più preciso quando il tuo post viene citato.

### Choosing an Instance

To benefit the most from Mastodon, it is critical to choose a server, or "instance," which is well aligned with the type of content you want to post or read about. We do not currently recommend any specific instances, but you may find advice within our communities. We recommend avoiding _mastodon.social_ and _mastodon.online_ because they are operated by the same company which develops Mastodon itself. From the perspective of decentralization, it is better in the long term to separate software developers and server hosts so that no one party can exert too much control over the network as a whole.

### Recommended Privacy Settings

From Mastodon's web interface, click the **Administration** link in the right sidebar. Within the administration control panel, you'll find these sections in the left sidebar:

#### Public Profile

There are a number of privacy controls under the **privacy and reach** tab here. Most notably, pay attention to these:

- [ ] **Automatically accept new followers**: You should consider unchecking this box to have a private profile. This will allow you to review who can follow your account before accepting them.

  In contrast to most social media platforms, if you have a private profile you still have the _option_ to publish posts which are publicly visible to non-followers and can still be boosted by non-followers. Therefore, unchecking this box is the only way to have the _choice_ to publish to either the entire world or a select group of people.

- [ ] **Show follows and followers on profile**: You should uncheck this box to hide your social graph from the public. It is fairly uncommon for the list of people you follow to have some genuine benefit to others, but that information can present a risk to you.

- [ ] **Display from which app you sent a post**: You should uncheck this box to prevent revealing information about your personal computing setup to others unnecessarily.

The other privacy controls on this page should be read through, but we would stress that they are **not** technical controls—they are merely requests that you make to others. For example, if you choose to hide your profile from search engines on this page, **nothing** is actually stopping a search engine from reading your profile. You are merely requesting search engine indexes not publish your content to their users.

You will likely still wish to make these requests because they can practically reduce your digital footprint. However, they should not be _relied_ upon. The only effective way to hide your posts from search engines and others is to post with non-public (followers only) visibility settings _and_ limit who can follow your account.

#### Preferences

You should change your **posting privacy** setting from public to: **Followers-only - Only show to followers**.

Note that this only changes your default settings to prevent accidental over-sharing. You can always adjust your visibility level when composing a new post.

#### Automated post deletion

- [x] Check the **Automatically delete old posts** box.

The default settings here are fine, and will delete any posts you make after 2 weeks, unless you favorite (star) them. This gives you an easy way to control which posts stick around forever, and which ones are only ephemeral. Many settings about how long and when posts are kept can be adjusted here to suit your own needs, however.

It is very rare for social media posts older than a few weeks to be read or relevant to others. These older posts are often ignored because they are challenging to deal with in bulk, but they can build a fairly comprehensive profile about you over time. You should always strive to publish content ephemerally by default, and only keep posts around for longer than that very intentionally.

### Posting Content

When publishing a new post, you will have the option to choose from one of these visibility settings:

- **Public**, which publishes your content to anyone on the internet.
- **Quiet public**, which you should consider equivalent to publicly posting! This is not a technical guarantee, but merely a request you are making to other servers to hide your post from some feeds.
- **Followers**, which publishes your content only to your followers. If you did not follow our recommendation of restricting your followers, you should consider this equivalent to publicly posting!
- **Specific people**, which only shares the post with people who are specifically mentioned within the post. This is Mastodon's version of direct messages, but should never be relied on for private communications as we covered earlier since Mastodon has no E2EE.

If you used our recommended configuration settings above, you should be posting to **Followers** by default, and only posting to **Public** on an intentional and case-by-case basis.

## Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/social-networks/element.svg){ align=right }

**Element** is the flagship client for the **:simple-matrix: [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im)** protocol, an [open standard](https://spec.matrix.org/latest) that enables decentralized communication by way of federated chat rooms. Users can exist on different homeservers but still communicate with each other.

[:octicons-home-16: Homepage](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

<details class="downloads" markdown><summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.element.android.x)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1631335820)
- [:simple-github: GitHub](https://github.com/element-hq/element-x-android/releases)
- [:fontawesome-brands-windows: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-browser-16: Web](https://app.element.io)

</details>

</div>

### Choosing a Homeserver

To benefit the most from Matrix, it is critical to choose a homeserver which is well aligned with the subject(s) you want to chat about. We do not currently recommend any specific homeservers, but you may find advice within our communities or third-party resources like [_joinmatrix.org_](https://servers.joinmatrix.org). We recommend avoiding _matrix.org_ because they are operated by the same company which develops Matrix itself. From the perspective of decentralization, it is better in the long term to separate software developers and server hosts so that no one party can exert too much control over the network as a whole.

### Recommended Privacy Settings

From Element's web or desktop app, go to :gear: → **All settings** to find these sections:

#### Sessions

By default, when you log in to Element on a new device, the session name will be automatically populated with the Matrix client and platform you used for login. This information may be visible to other users depending on the Matrix client they use.

To prevent revealing information about your personal device to others unnecessarily, consider emptying the session name; this will change the session name to the randomly generated alphanumeric Session ID instead.

#### Preferences

- [ ] Uncheck **Send read receipts**
- [ ] Uncheck **Send typing notifications**

You should uncheck these options to reduce the exposure of metadata to other users when chatting in a public room.

#### Voice & Video

- [ ] Uncheck **Allow Peer-to-Peer for 1:1 calls**
- [ ] Uncheck **Allow fallback call assist server (turn.matrix.org)**

If you do decide to use Element for one-to-one communication, we recommend unchecking these settings to prevent the exposure of your IP address to the other party.

#### Security & Privacy

##### Manage integrations (scalar.vector.im)

A Matrix integration manager connects Matrix to third-party services such as bots, bridges, and other enhancements. Element collects information to provide these services to those using an integration manager; you can review its detailed [Privacy Notice](https://element.io/integration-manager-privacy-notice) for the exact information Element collects and the ways it uses such information.

As an end user on a public homeserver, you can consider unchecking the **Enable the integration manager** option, which does not affect the visibility of bots or other third-party services. As a homeserver administrator, consider whether the additional parties with which you share your data are worth the extra functionality.

##### Sessions

- [ ] (Optional) Uncheck **Record the client name, version, and url to recognize sessions for easily in session manager**

Unchecking this option may make it more diffcult to discern your active sessions if you logged in to your Matrix account on multiple devices.

#### Crittografia

- [x] (Optional) Check **In encrypted rooms, only send messages to verified users**

With this setting enabled, unverified users (i.e., those who have not used the **Verify User** function) and unverified devices of verified users will not receive your messages in a room with encryption enabled. This may limit the messages you can view and the people you can interact with.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto che consigliamo.** Oltre ai nostri [criteri standard](about/criteria.md), abbiamo sviluppato un chiaro insieme di requisiti per consentirci di fornire dei consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

- Must be free and open-source software.
- Must use a federated protocol to communicate with other instances of the social networking software.
- Must not have non-technical restrictions on who can be federated with.
- Must be usable within a standard [web browser](desktop-browsers.md).
- Must make public content accessible to visitors without an account.
- Must allow you to limit who can follow your profile.
- Must allow you to post content visible only to your followers.
- Must support modern web application security standards/features (including [multifactor authentication](multi-factor-authentication.md)).
