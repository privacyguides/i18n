---
title: "Tor Network"
icon: simple/torproject
description: Protect your internet browsing from prying eyes by using the Tor network, a secure network which circumvents censorship.
---

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

Das **Tor** Netzwerk besteht aus von freiwillig betriebenen Servern, die es ermöglichen, kostenlos die eigene Privatsphäre und Sicherheit im Internet zu verbessern. Einzelpersonen und Organisationen können auch Informationen über das Tor-Netzwerk mit ".onion versteckten Diensten" austauschen, ohne ihre Privatsphäre zu gefährden. Da der Tor-Verkehr schwer zu blockieren und zurückzuverfolgen ist, ist Tor ein effektives Werkzeug zur Zensur Umgehung.

[:octicons-home-16:](https://www.torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation}
[:octicons-code-16:](https://gitweb.torproject.org/tor.git){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

Tor funktioniert, indem es deinen Internetverkehr über diese von Freiwilligen betriebenen Server leitet, anstatt eine direkte Verbindung zu der Website herzustellen, die du besuchen willst. Dadurch wird verschleiert, woher der Datenverkehr kommt, und kein Server im Verbindungspfad ist in der Lage, den vollständigen Pfad zu sehen, woher der Datenverkehr kommt und wohin er geht, was bedeutet, dass selbst die Server, die du für die Verbindung verwendest, deiner Anonymität nichts anhaben können.

[Detailed Tor Overview :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Verbinden mit Tor

There are a variety of ways to connect to the Tor network from your device, the most commonly used being the **Tor Browser**, a fork of Firefox designed for anonymous browsing for desktop computers and Android. In addition to the apps listed below, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser.

### Tor Browser

!!! recommendation

    ![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }
    
    **Tor Browser** is the choice if you need anonymity, as it provides you with access to the Tor network and bridges, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*.
    
    [:octicons-home-16: Homepage](https://www.torproject.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
    [:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation }
    [:octicons-code-16:](https://gitweb.torproject.org/tor-browser.git/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
        - [:simple-android: Android](https://www.torproject.org/download/#android)
        - [:simple-windows11: Windows](https://www.torproject.org/download/)
        - [:simple-apple: macOS](https://www.torproject.org/download/)
        - [:simple-linux: Linux](https://www.torproject.org/download/)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/security/tor)

!!! danger

    You should **never** install any additional extensions on Tor Browser or edit `about:config` settings, including the ones we suggest for Firefox. Browser extensions and non-standard settings make you stand out from others on the Tor network, thus making your browser easier to [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting).

The Tor Browser is designed to prevent fingerprinting, or identifying you based on your browser configuration. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings/).

### Orbot

!!! recommendation

    ![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }
    
    **Orbot** is a free Tor VPN for smartphones which routes traffic from any app on your device through the Tor network.
    
    [:octicons-home-16: Homepage](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

We previously recommended enabling the *Isolate Destination Address* preference in Orbot settings. While this setting can theoretically improve privacy by enforcing the use of a different circuit for each IP address you connect to, it doesn't provide a practical advantage for most applications (especially web browsing), can come with a significant performance penalty, and increases the load on the Tor network. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

!!! tip "Tips for Android"

    Orbot can proxy individual apps if they support SOCKS or HTTP proxying. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.
    
    Orbot is often outdated on the Guardian Project's [F-Droid repository](https://guardianproject.info/fdroid) and [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), so consider downloading directly from the [GitHub repository](https://github.com/guardianproject/orbot/releases) instead.
    
    All versions are signed using the same signature so they should be compatible with each other.

## Relays and Bridges

### Snowflake

!!! recommendation

    ![Snowflake logo](assets/img/browsers/snowflake.svg#only-light){ align=right }
    ![Snowflake logo](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }
    
    **Snowflake** allows you to donate bandwidth to the Tor Project by operating a "Snowflake proxy" within your browser.
    
    People who are censored can use Snowflake proxies to connect to the Tor network. Snowflake is a great way to contribute to the network even if you don't have the technical know-how to run a Tor relay or bridge.
    
    [:octicons-home-16: Homepage](https://snowflake.torproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitweb.torproject.org/pluggable-transports/snowflake.git/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-US/firefox/addon/torproject-snowflake/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/snowflake/mafpmfcccpbjnhfhjnllmmalhifmlcie)
        - [:octicons-browser-16: Web](https://snowflake.torproject.org/embed "Leave this page open to be a Snowflake proxy")

??? tip "Embedded Snowflake"

    You can enable Snowflake in your browser by clicking the switch below and ==leaving this page open==. You can also install Snowflake as a browser extension to have it always run while your browser is open, however adding third-party extensions can increase your attack surface.
    
    <center><iframe src="https://snowflake.torproject.org/embed.html" width="320" height="240" frameborder="0" scrolling="no"></iframe></center>
    <small>If the embed does not appear for you, ensure you are not blocking the third-party frame from `torproject.org`. Alternatively, visit [this page](https://snowflake.torproject.org/embed.html).</small>

Snowflake does not increase your privacy in any way, nor is it used to connect to the Tor network within your personal browser. However, if your internet connection is uncensored, you should consider running it to help people in censored networks achieve better privacy themselves. There is no need to worry about which websites people are accessing through your proxy—their visible browsing IP address will match their Tor exit node, not yours.

Running a Snowflake proxy is low-risk, even moreso than running a Tor relay or bridge which are already not particularly risky endeavours. However, it does still proxy traffic through your network which can be impactful in some ways, especially if your network is bandwidth-limited. Make sure you understand [how Snowflake works](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) before deciding whether to run a proxy.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://www.whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
