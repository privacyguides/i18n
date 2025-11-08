---
meta_title: "Recommended Search Engines: Anonymous Alternatives to Google - Privacy Guides"
title: מנועי חיפוש
icon: material/search-web
description: Use privacy-respecting search engines which don't build an advertising profile based on your searches.
cover: search-engines.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: קפיטליזם מעקב](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Use a **search engine** that doesn't build an advertising profile based on your searches.

## ספקים מומלצים

The recommendations here do not collect personally identifying information (PII) based on each service's privacy policy. אין **ערובה לכך** שמדיניות פרטיות זו תכובד.

Consider using a [VPN](vpn.md) or [Tor](tor.md) if your threat model requires hiding your IP address from the search provider.

| Provider                     | Search Index                                                                                                                                                                  | Tor Hidden Service            | Logging / Privacy Policy | Country of Operation |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- | ------------------------ | -------------------- |
| [חיפוש Brave](#brave-search) | [Independent](https://brave.com/search-independence)                                                                                                                          | :material-check:{ .pg-green } | Anonymized[^1]           | United States        |
| [DuckDuckGo](#duckduckgo)    | [Bing](https://help.duckduckgo.com/results/sources)                                                                                                                           | :material-check:{ .pg-green } | Anonymized[^2]           | United States        |
| [Startpage](#startpage)      | [Google and Bing](https://support.startpage.com/hc/articles/4522435533844-What-is-the-relationship-between-Startpage-and-your-search-partners-like-Google-and-Microsoft-Bing) | :material-check:{ .pg-green } | Anonymized[^3]           | Netherlands          |

### חיפוש Brave

<div class="admonition recommendation" markdown>

![Brave Search logo](assets/img/search-engines/brave-search.svg){ align=right }

**Brave Search** is a search engine developed by Brave. It includes unique features such as [Discussions](https://search.brave.com/help/discussions), which highlights conversation-focused results such as forum posts.

Brave Search is the default search engine for the [Brave Browser](desktop-browsers.md#brave).

[:octicons-home-16: Homepage](https://search.brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://search.brave.com/help){ .card-link title="Documentation" }

</div>

If you use Brave Search while logged in to a Premium account, there is a risk of Brave correlating search queries with your account.

We recommend you disable [Anonymous usage metrics](https://search.brave.com/help/usage-metrics) as it is enabled by default and can be disabled within settings.

### DuckDuckGo

<div class="admonition recommendation" markdown>

![DuckDuckGo לוגו](assets/img/search-engines/duckduckgo.svg){ align=right }

**DuckDuckGo** היא אחת האפשרויות היותר מיינסטרים במנועי חיפוש פרטיים. Notable DuckDuckGo search features include [bangs](https://duckduckgo.com/bang) and a variety of [instant answers](https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features). The search engine uses numerous [sources](https://help.duckduckgo.com/results/sources) other than Bing for instant answers and other non-primary results.

DuckDuckGo is the default search engine for the [Tor Browser](tor.md#tor-browser) and is one of the few available options on Apple’s [Safari](mobile-browsers.md#safari-ios) browser.

[:octicons-home-16: Homepage](https://duckduckgo.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.duckduckgo.com){ .card-link title="Documentation" }

</div>

DuckDuckGo offers two [other versions](https://help.duckduckgo.com/features/non-javascript) of their search engine, both of which do not require JavaScript. עם זאת, גרסאות אלו חסרות תכונות. These versions can also be used in conjunction with their Tor hidden address by appending [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) or [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) for the respective version.

### Startpage

<div class="admonition recommendation" markdown>

![Startpage logo](assets/img/search-engines/startpage.svg#only-light){ align=right }
![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }

**Startpage** is a private search engine. One of Startpage's unique features is the [Anonymous View](https://startpage.com/en/anonymous-view), which puts forth efforts to standardize user activity to make it more difficult to be uniquely identified. The feature can be useful for hiding [some](https://support.startpage.com/hc/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) network and browser properties. שלא כמו שהשם מרמז, אין להסתמך על התכונה לאנונימיות. אם אתה מחפש אנונימיות, השתמש במקום זאת ב [Tor Browser]( tor.md#tor - browser).

[:octicons-home-16: Homepage](https://startpage.com){ .md-button .md-button--primary }
[:simple-torbrowser:](http://startpagel6srwcjlue4zgq3zevrujfaow726kjytqbbjyrswwmjzcqd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://startpage.com/en/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.startpage.com/hc/categories/4481917470356-Startpage-Search-Engine){ .card-link title="Documentation" }

</div>

בעלת המניות הרוב של Startpage היא System1 שהיא חברת adtech. אנחנו לא מאמינים שזו בעיה מכיוון שיש להם [מדיניות פרטיות](https://system1.com/terms/privacy-policy) נפרדת באופן מובהק. The Privacy Guides team reached out to Startpage [back in 2020](https://blog.privacyguides.org/2020/05/03/relisting-startpage) to clear up any concerns with System1's sizeable investment into the service, and we were satisfied with the answers we received.

Startpage previously placed limitations on VPN and [Tor](tor.md) users, but they recently created an [official](https://support.startpage.com/hc/en-us/articles/24786602537364-Startpage-s-Tor-onion-service) Tor hidden service, and as of April 2024 we have no longer noticed extra roadblocks for Tor or [VPN](vpn.md) users.

## Metasearch Engines

A [metasearch engine](https://en.wikipedia.org/wiki/Metasearch_engine) aggregates the results of other search engines, such as the ones recommended above, while not storing any information itself.

### SearXNG

<div class="admonition recommendation" markdown>

![SearXNG logo](assets/img/search-engines/searxng.svg){ align=right }

**SearXNG** is an open-source, self-hostable, metasearch engine. זהו מזלג מתוחזק פעיל של [SearX](https://github.com/searx/searx).

[:octicons-home-16: Homepage](https://searxng.org){ .md-button .md-button--primary }
[:octicons-server-16:](https://searx.space){ .card-link title="Public Instances" }
[:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="Source Code" }

</div>

SearXNG הוא פרוקסי בינך לבין מנועי החיפוש שמהם הוא צובר. שאילתות החיפוש שלך עדיין יישלחו למנועי החיפוש שמהם SearXNG מקבל את תוצאותיו.

בעת אירוח עצמי, חשוב שאנשים אחרים ישתמשו במקרה שלך כדי שהשאילתות ישתלבו. עליכם להיזהר היכן וכיצד אתם מארחים את SearXNG, מכיוון שאנשים שמחפשים תוכן לא חוקי בהפצה שלכם עלולים למשוך תשומת לב לא רצויה מהרשויות.

כאשר אתה משתמש בהפצה של SearXNG, הקפד לקרוא את מדיניות הפרטיות שלהם. מאחר שמופעי SearXNG עשויים להשתנות על ידי בעליהם, הם לא בהכרח משקפים את מדיניות הפרטיות שלהם. חלק מהמקרים מופעלים כשירות Tor מוסתר, אשר עשוי להעניק פרטיות מסוימת כל עוד שאילתות החיפוש שלך אינן מכילות PII.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

### דרישות מינימליות

- Must not collect PII per their privacy policy.
- Must not require users to create an account with them.

### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- צריך להיות מבוסס על תוכנת קוד פתוח.
- אין לחסום את כתובות ה - IP של צומת היציאה של Tor.

[^1]: Brave Search collects aggregated usage metrics, which includes the OS and the user agent. However, they do not collect PII. To serve [anonymous local results](https://search.brave.com/help/anonymous-local-results), IP addresses are temporarily processed, but are not retained.

    Brave Search: [*Brave Search privacy notice*](https://search.brave.com/help/privacy-policy) [^2]: DuckDuckGo **does** log your searches for product improvement purposes, but not your IP address or any other PII.

    DuckDuckGo Privacy Policy: [*We don't track you.*](https://duckduckgo.com/privacy) [^3]: Startpage logs details such as operating system, user agent, and language. They do not log your IP address, search queries, or other PII.

    Our Privacy Policy: [*How we have implemented truly anonymous analytics*](https://startpage.com/en/privacy-policy#section-4)
