---
meta_title: "Empfohlene Suchmaschinen: Anonyme Google-Alternativen - Privacy Guides"
title: "Suchmaschinen"
icon: material/search-web
description: Diese Privatsphäre respektierenden Suchmaschinen erstellen kein Werbeprofil auf der Grundlage deiner Suchanfragen.
cover: search-engines.webp
---

Verwende eine Suchmaschine, die kein Werbeprofil auf Grundlage deiner Suchanfragen erstellt.

Die hier gegebenen Empfehlungen beruhen auf den Datenschutzbestimmungen der einzelnen Dienste. Es gibt **keine Garantie**, dass diese Datenschutzbestimmungen auch eingehalten werden.

Erwäge die Verwendung eines [VPN](vpn.md) oder [Tor](https://www.torproject.org/), wenn dein Bedrohungsmodell das Verbergen deiner IP-Adresse vor dem Suchanbieter erfordert.

## Brave Search

!!! recommendation

    ![Brave Search logo](assets/img/search-engines/brave-search.svg){ align=right }
    
    **Brave Search** wird von Brave entwickelt und liefert hauptsächlich Ergebnisse aus seinem eigenen, unabhängigen Index. Der Index ist für die Google-Suche optimiert und kann daher im Vergleich zu anderen Alternativen möglicherweise kontextgenauere Ergebnisse liefern.
    
    Brave Search verfügt über einzigartige Funktionen, wie etwa Diskussionen, die auf Konversationen ausgerichtete Ergebnisse wie Forenbeiträge hervorheben.
    
    Wir emfehlen dir, [Anonyme Nutzungsstatistiken](https://search.brave.com/help/usage-metrics) zu deaktivieren, da sie standardmäßig aktiviert sind und in den Einstellungen deaktiviert werden können.
    
    [:octicons-home-16: Homepage](https://search.brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="Datenschutzbestimmungen" }
    [:octicons-info-16:](https://search.brave.com/help){ .card-link title=Dokumentation}

Brave Search hat seinen Sitz in den Vereinigten Staaten. Die [Datenschutzbestimmungen](https://search.brave.com/help/privacy-policy) besagen, dass aggregierte Nutzungsdaten gesammelt werden, zu denen auch das verwendete Betriebssystem und der verwendete Browser gehören; es werden jedoch keine personenbezogenen Daten erfasst. IP-Adressen werden temporär verarbeitet, aber nicht gespeichert.

## DuckDuckGo

!!! recommendation

    ![DuckDuckGo logo](assets/img/search-engines/duckduckgo.svg){ align=right }
    
    **DuckDuckGo** ist eine der gängigeren Optionen für private Suchmaschinen. Zu den erwähnenswerten Suchfunktionen von DuckDuckGo gehören [Bangs](https://duckduckgo.com/bang) und zahlreiche [Sofortantworten](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features/). Die Suchmaschine stützt sich auf die kommerzielle Bing-API, um die meisten Ergebnisse zu liefern, nutzt aber auch zahlreiche [andere Quellen](https://help.duckduckgo.com/results/sources/) für Sofortantworten und andere nicht primäre Ergebnisse.
    
    DuckDuckGo ist die Standardsuchmaschine für den Tor-Browser und eine der wenigen verfügbaren Optionen für den Safari-Browser von Apple.
    
    [:octicons-home-16: Homepage](https://duckduckgo.com){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="Datenschutzbestimmungen" }
    [:octicons-info-16:](https://help.duckduckgo.com/){ .card-link title=Dokumentation}

DuckDuckGo hat seinen Sitz in den Vereinigten Staaten. Ihre [Datenschutzbestimmungen](https://duckduckgo.com/privacy) besagen, dass sie deine Suchanfragen zum Zwecke der Produktverbesserung **protokollieren**, aber weder deine IP-Adresse noch andere personenbezogene Daten speichern.

DuckDuckGo bietet zwei [andere Versionen](https://help.duckduckgo.com/features/non-javascript/) ihrer Suchmaschine an, für die beide kein JavaScript benötigt wird. Allerdings fehlen diesen Versionen einige Funktionen. Diese Versionen können auch in Verbindung mit ihrer [Tor-Onion-Adresse](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/) verwendet werden, indem man [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) oder [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) für die jeweilige Version anfügt.

## SearXNG

!!! recommendation

    ![SearXNG logo](assets/img/search-engines/searxng.svg){ align=right }
    
    **SearXNG** ist eine quelloffene, selbstständig hostbare Metasuchmaschine, die die Ergebnisse anderer Suchmaschinen zusammenfasst, ohne selbst Informationen zu speichern. Es ist ein aktiv betreuter Fork von [SearX](https://github.com/searx/searx).
    
    [:octicons-home-16: Homepage](https://searxng.org){ .md-button .md-button--primary }
    [:octicons-server-16:](https://searx.space/){ .card-link title="Öffentliche Instanzen"}
    [:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="Source Code" }

SearXNG ist ein Proxy zwischen dir und den Suchmaschinen, die es zusammenfasst. Deine Suchanfragen werden weiterhin an die Suchmaschinen gesendet, von denen SearXNG seine Ergebnisse bezieht.

Wenn du selbst hostest, ist es wichtig, dass deine Instanz auch von anderen Personen genutzt wird, damit sich die Suchanfragen vermischen können. Du solltest vorsichtig sein, wo und wie du SearXNG hostest, da Leute, die auf deiner Instanz nach illegalen Inhalten suchen, unerwünschte Aufmerksamkeit der Behörden auf sich ziehen könnten.

Wenn du eine SearXNG-Instanz verwendest, beachte unbedingt deren Datenschutzbestimmungen. Da SearXNG-Instanzen von ihren Eigentümern geändert werden können, spiegeln sie nicht unbedingt deren Datenschutzpolitik wider. Einige Instanzen laufen als versteckter Tor-Dienst, der ein gewisses Maß an Privatsphäre gewährleistet, solange deine Suchanfragen keine personenbezogenen Daten enthalten.

## Startpage

!!! recommendation

    ![Startpage logo](assets/img/search-engines/startpage.svg#only-light){ align=right }
    ![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }
    
    **Startpage** ist eine private Suchmaschine, die dafür bekannt ist, dass sie Suchergebnisse von [Google und Bing](https://support.startpage.com/hc/en-us/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing-) liefert.  Eine der einzigartigen Funktionen von Startpage ist die [Anonyme Ansicht](https://www.startpage.com/de/anonymous-view/), die sich bemüht, die Benutzeraktivitäten zu standardisieren, um eine eindeutige Identifizierung zu erschweren. Die Funktion kann nützlich sein, um [einige](https://support.startpage.com/hc/de/articles/4455540212116-Der-Anonyme-Ansicht-Proxy-Technische-Details) Netzwerk- und Browsereigenschaften zu verbergen. Anders als der Name vermuten lässt, sollte man sich jedoch nicht auf diese Funktion verlassen, um anonym zu bleiben. Wenn du Anonymität suchst, verwende stattdessen den [Tor Browser](tor.md#tor-browser).
    
    [:octicons-home-16: Homepage](https://www.startpage.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.startpage.com/en/privacy-policy){ .card-link title="Datenschutzbestimmungen" }
    [:octicons-info-16:](https://support.startpage.com/hc/en-us/categories/4481917470356-Startpage-Search-Engine){ .card-link title=Dokumentation}

!!! warning "Warnung"

    Startpage beschränkt regelmäßig den Zugang zu seinem Dienst auf bestimmten IP-Adressen, wie IPs, die für VPNs oder Tor reserviert sind. [DuckDuckGo](#duckduckgo) und [Brave Search](#brave-search) sind freundlichere Optionen, wenn dein Bedrohungsmodell das Verbergen deiner IP-Adresse vor dem Suchanbieter erfordert.

Startpage hat seinen Sitz in den Niederlanden. Laut ihren [Datenschutzbestimmungen](https://www.startpage.com/de/privacy-policy/) protokollieren sie Details wie das Betriebssystem, den Browsertyp und die Sprache. Sie protokollieren weder die IP-Adresse noch Suchanfragen oder andere personenbezogene Daten.

Der Mehrheitsaktionär von Startpage ist System1, ein Werbeunternehmen. Wir glauben nicht, dass dies ein Problem ist, da sie gesonderte <a href="https://system1.com/terms/privacy-policy"]>Datenschutzbestimmungen</a> haben. Das Privacy Guides Team hat sich bereits [im Jahr 2020](https://web.archive.org/web/20210118031008/https://blog.privacytools.io/relisting-startpage/) an Startpage gewandt, um etwaige Bedenken hinsichtlich der beträchtlichen Investition von System1 in den Dienst auszuräumen. Wir waren mit den Antworten, die wir erhielten, zufrieden.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

!!! example "Dieser Abschnitt ist neu"

    Wir arbeiten daran, für jeden Bereich unserer Website genaue Kriterien festzulegen, die sich möglicherweise noch ändern werden. Wenn du irgendwelche Fragen zu unseren Kriterien hast, frage bitte [in unserem Forum](https://discuss.privacyguides.net/latest) und gehe nicht davon aus, dass wir etwas bei unseren Empfehlungen nicht berücksichtigt haben, nur weil es hier nicht aufgeführt ist. Es gibt viele Faktoren, die berücksichtigt und diskutiert werden, wenn wir ein Projekt empfehlen, und die Dokumentation jedes einzelnen Faktors ist ein laufender Prozess.

### Mindestanforderungen

- Darf keine persönlich identifizierbaren Informationen gemäß ihrer Datenschutzrichtlinie sammeln.
- Sie dürfen den Nutzern nicht erlauben, ein Konto bei ihnen anzulegen.

### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Merkmale, aber diejenigen, die sie enthalten, werden möglicherweise höher eingestuft als andere auf dieser Seite.

- Sollte auf Open-Source-Software basieren.
- Sollte keine IP-Adressen von Tor-Ausgangsknoten blockieren.
