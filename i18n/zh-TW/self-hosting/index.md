---
title: 自行架設
meta_title: "自行架設軟體與服務 - Privacy Guides"
description: 對於技術能力較高的讀者，自行架設軟體與服務可最大限度地管控您的資料，提供更多的隱私保護。
cover: router.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務供應商](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

**自行架設**軟體和服務可以掌握數位主權，特別是獨立於產品開發商或廠商控制的雲端伺服器，以達到更高層級的隱私保護。 自行架設的意思是指，在您自己的硬體上架設管理應用程式和資料。

自行架設自己的解決方案，需要有進階的技術知識，並且能深入了解相關的風險。 當您成為自己資料的主人（可能也包含別人的資料），就要負起原本可能沒有的責任。 錯誤地自行架設隱私權軟體，可能會讓您的情況比使用有提供端對端加密的服務供應商還遭，所以如果您還不熟悉怎麼做，建議避免。

## :material-dns: DNS 過濾

<div class="grid cards" markdown>

- ![AdGuard Home 圖示](../assets/img/self-hosting/adguard-home.svg){ .twemoji loading=lazy } [AdGuard Home](dns-filtering.md#adguard-home)
- ![Pi-Hole 圖示](../assets/img/self-hosting/pi-hole.svg){ .twemoji loading=lazy } [Pi-Hole](dns-filtering.md#pi-hole)

</div>

[更多資訊 :material-arrow-right-drop-circle:](dns-filtering.md)

## :material-email: 電子郵件伺服器

<div class="grid cards" markdown>

- ![Stalwart 圖示](../assets/img/self-hosting/stalwart.svg){ .twemoji loading=lazy } [Stalwart](email-servers.md#stalwart)
- ![Mailcow 圖示](../assets/img/self-hosting/mailcow.svg){ .twemoji loading=lazy } [Mailcow](email-servers.md#mailcow)
- ![Mail-in-a-Box 圖示](../assets/img/self-hosting/mail-in-a-box.svg){ .twemoji loading=lazy } [Mail-in-a-Box](email-servers.md#mail-in-a-box)

</div>

[更多資訊 :material-arrow-right-drop-circle:](email-servers.md)

## :material-file-multiple-outline: 檔案管理

<div class="grid cards" markdown>

- ![PhotoPrism 圖示](../assets/img/self-hosting/photoprism.svg){ .twemoji loading=lazy } [PhotoPrism](file-management.md#photoprism)
- ![FreedomBox 圖示](../assets/img/self-hosting/freedombox.svg){ .twemoji loading=lazy } [FreedomBox](file-management.md#freedombox)
- ![Nextcloud 圖示](../assets/img/self-hosting/nextcloud.svg){ .twemoji loading=lazy } [Nextcloud](file-management.md#nextcloud)

</div>

[更多資訊 :material-arrow-right-drop-circle:](file-management.md)

## :material-form-textbox-password: 密碼管理

### Vaultwarden

<div class="admonition recommendation" markdown>

![Vaultwarden 圖示](../assets/img/self-hosting/vaultwarden.svg#only-light){ align=right }
![Vaultwarden 圖示](../assets/img/self-hosting/vaultwarden-dark.svg#only-dark){ align=right }

**Vaultwarden** 是一套使用 Rust 寫成的 [Bitwarden](../passwords.md#bitwarden) 同步伺服器的替代品，並相容於 Bitwarden 官方的客戶端，非常適合在架設資源需求繁重的[官方服務](https://github.com/bitwarden/server)可能不太理想的情況下，來自行架設。

[:octicons-repo-16: 程式庫](https://github.com/dani-garcia/vaultwarden#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="原始碼" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title="捐款" }

</div>

## :material-account-supervisor-circle-outline: 社群網路

自行架設自己的社群網路軟體，可以幫助規避公共伺服器的管理員或管理團隊潛在的[伺服器層級審查](../social-networks.md#censorship-resistance)。

### Mastodon

<div class="admonition recommendation" markdown>

![Mastodon 圖示](../assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** 是基於開放網路通訊協定和自由及開放原始碼軟體的社交網路。 他使用分散式的 **:simple-activitypub: ActivityPub** 通訊協定。

[:octicons-home-16:](https://joinmastodon.org){ .card-link title="首頁" }
[:octicons-info-16:](https://docs.joinmastodon.org/admin/prerequisites){ .card-link title="管理文件" }

</div>

Mastodon 可[與 Tor 網路整合](https://docs.joinmastodon.org/admin/optional/tor)，以應付更極端的、甚至您的主機供應商也受到審查的情況，但這可能會限制只能讓也整合 Tor 的其他伺服器才能存取您的內容（與其他大多數隱藏服務一樣）。

Mastodon 從龐大且活躍的自行架設社群中獲益良多，其管理方式也有非常全面的說明文件。 雖然許多其他 ActivityPub 平台可能需要豐富的技術知識才能執行和排除故障，但 Mastodon 擁有非常穩定且經過測試的版本，一般來說，任何人只要會使用 Linux 命令列並遵循他們的逐步教學，就可以安全無虞地執行它。

### Element

<div class="admonition recommendation" markdown>

![Element 圖示](../assets/img/social-networks/element.svg){ align=right }

**Element** 是 **:simple-matrix: Matrix** 通訊協定的旗艦級用戶端，此開放式標準可透過聯合聊天室的方式實現分散式通訊。

[:octicons-home-16:](https://element.io){ .card-link title="首頁" }
[:octicons-info-16:](https://element-hq.github.io/synapse/latest){ .card-link title="管理文件" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="原始碼" }

</div>

## :material-flip-to-front: 前端

自行架設您自己的網頁前端，可幫助您避開高流量、公共主機上可能遇到的流量限制。 自我架設時，讓其他人也使用您的主機，讓您融入其中也很重要。 您應該謹慎處理託管的地點和方式，因為其他人如何使用將會影響到您的託管。

<div class="grid cards" markdown>

- ![Redlib 圖示](../assets/img/frontends/redlib.svg){ .lg .middle .twemoji } [**Redlib (Reddit)**](../frontends.md#redlib)

  ---

  [:octicons-info-16:](https://github.com/redlib-org/redlib#deployment){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="原始碼" }

- ![ProxiTok 圖示](../assets/img/frontends/proxitok.svg){ .lg .middle .twemoji } [**ProxiTok (TikTok)**](../frontends.md#proxitok)

  ---

  [:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki/Self-hosting){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="原始碼" }

- ![Invidious 圖示](../assets/img/frontends/invidious.svg#only-light){ .twemoji }![Invidious logo](../assets/img/frontends/invidious-dark.svg#only-dark){ .twemoji } [**Invidious (YouTube)**](../frontends.md#invidious)

  ---

  [:octicons-home-16:](https://invidious.io){ .card-link title="首頁" }
  [:octicons-info-16:](https://docs.invidious.io/installation){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="原始碼" }

- ![Piped 圖示](../assets/img/frontends/piped.svg){ .twemoji } [**Piped (YouTube)**](../frontends.md#piped)

  ---

  [:octicons-info-16:](https://docs.piped.video/docs/self-hosting){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="原始碼" }

</div>

## 更多工具…

本站其他分類的工具推薦清單，也有自行架設的選項，所以只要在閱讀文章之後對自行架設有把握，就可以自行架設。

<div class="grid cards" markdown>

- ![Peergos 圖示](../assets/img/cloud/peergos.svg){ .twemoji } [**Peergos**](../cloud.md#peergos)

  ---

  [:octicons-home-16:](https://peergos.org){ .card-link title="首頁" }
  [:octicons-info-16:](https://github.com/peergos/peergos#usage---running-locally-to-log-in-to-another-instance){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="原始碼" }

- ![Addy.io 圖示](../assets/img/email-aliasing/addy.svg){ .twemoji } [**Addy.io**](../email-aliasing.md#addyio)

  ---

  [:octicons-home-16:](https://addy.io){ .card-link title="首頁" }
  [:octicons-info-16:](https://addy.io/self-hosting){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="原始碼" }

- ![SimpleLogin 圖示](../assets/img/email-aliasing/simplelogin.svg){ .twemoji } [**SimpleLogin**](../email-aliasing.md#simplelogin)

  ---

  [:octicons-home-16:](https://addy.io){ .card-link title="首頁" }
  [:octicons-info-16:](https://github.com/simple-login/app#prerequisites){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/simple-login){ .card-link title="原始碼" }

- ![Ente 圖示](../assets/img/photo-management/ente.svg){ .twemoji } [**Ente Photos**](../photo-management.md#ente-photos)

  ---

  [:octicons-home-16:](https://ente.io){ .card-link title="首頁" }
  [:octicons-info-16:](https://help.ente.io/self-hosting){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="原始碼" }

- ![CryptPad 圖示](../assets/img/document-collaboration/cryptpad.svg){ .twemoji } [**CryptPad**](../document-collaboration.md#cryptpad)

  ---

  [:octicons-home-16:](https://cryptpad.fr){ .card-link title="首頁" }
  [:octicons-info-16:](https://docs.cryptpad.org/en/admin_guide/index.html){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="原始碼" }

- ![Send 圖示](../assets/img/file-sharing-sync/send.svg){ .twemoji } [**Send**](../file-sharing.md#send)

  ---

  [:octicons-home-16:](https://send.vis.ee){ .card-link title="首頁" }
  [:octicons-info-16:](https://github.com/timvisee/send/blob/master/docs/deployment.md){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="原始碼" }

- ![LibreTranslate 圖示](../assets/img/language-tools/libretranslate.png){ .twemoji } [**LibreTranslate**](../language-tools.md#libretranslate)

  ---

  [:octicons-home-16:](https://libretranslate.com){ .card-link title="首頁" }
  [:octicons-info-16:](https://docs.libretranslate.com){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/LibreTranslate/LibreTranslate){ .card-link title="原始碼" }

- ![Miniflux 圖示](../assets/img/news-aggregators/miniflux.svg#only-light){ .twemoji }![Miniflux 圖示](../assets/img/news-aggregators/miniflux-dark.svg#only-dark){ .twemoji } [**Miniflux**](../news-aggregators.md#miniflux)

  ---

  [:octicons-home-16:](https://miniflux.app){ .card-link title="首頁" }
  [:octicons-info-16:](https://miniflux.app/docs/index.html#administration-guide){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/miniflux/v2){ .card-link title="原始碼" }

- ![Standard Notes 圖示](../assets/img/notebooks/standard-notes.svg){ .twemoji } [**Standard Notes**](../notebooks.md#standard-notes)

  ---

  [:octicons-home-16:](https://standardnotes.com){ .card-link title="首頁" }
  [:octicons-info-16:](https://standardnotes.com/help/47/can-i-self-host-standard-notes){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/standardnotes){ .card-link title="原始碼" }

- ![PrivateBin 圖示](../assets/img/pastebins/privatebin.svg){ .twemoji } [**PrivateBin**](../pastebins.md#privatebin)

  ---

  [:octicons-home-16:](https://privatebin.info){ .card-link title="首頁" }
  [:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/blob/master/doc/Installation.md){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="原始碼" }

- ![Paaster 圖示](../assets/img/pastebins/paaster.svg){ .twemoji } [**Paaster**](../pastebins.md#paaster)

  ---

  [:octicons-home-16:](https://paaster.io){ .card-link title="首頁" }
  [:octicons-info-16:](https://github.com/WardPearce/paaster#deployment){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/WardPearce/paaster){ .card-link title="原始碼" }

- ![SimpleX Chat 圖示](../assets/img/messengers/simplex.svg){ .twemoji } [**SimpleX Chat**](../real-time-communication.md#simplex-chat)

  ---

  [:octicons-home-16:](https://simplex.chat){ .card-link title="首頁" }
  [:octicons-info-16:](https://simplex.chat/docs/server.html){ .card-link title="管理文件" }
  [:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="原始碼" }

</div>
