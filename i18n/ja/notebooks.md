---
title: "ノート"
icon: material/notebook-edit-outline
description: These encrypted note-taking apps let you keep track of your notes without giving them to a third-party.
cover: notebooks.webp
---

第三者による閲覧を防止しながら、メモや日記を保存できます。

現在、Evernote、Google Keep、Microsoft OneNoteなどを使用している場合は、ここに掲載されたエンドツーエンド暗号化対応のアプリケーションに移行することをおすすめします。

## クラウドベース

### Standard Notes

<div class="admonition recommendation" markdown>

![Standard Notesのロゴ](assets/img/notebooks/standard-notes.svg){ align=right }

**Standard Notes**はどこでも簡単にメモを取れる、シンプルかつプライベートなノートアプリです。 すべてのプラットフォームでエンドツーエンド暗号化を使用し、テーマやカスタムエディターによる強力なデスクトップ環境を提供します。 また、[独立した監査](https://standardnotes.com/help/2/has-standard-notes-completed-a-third-party-security-audit)も受けています。

[:octicons-home-16: Homepage](https://standardnotes.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://standardnotes.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://standardnotes.com/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/standardnotes){ .card-link title="Source Code" }
[:octicons-heart-16:](https://standardnotes.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.standardnotes)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1285392450)
- [:simple-github: GitHub](https://github.com/standardnotes/app/releases)
- [:simple-windows11: Windows](https://standardnotes.com)
- [:simple-apple: macOS](https://standardnotes.com)
- [:simple-linux: Linux](https://standardnotes.com)
- [:octicons-globe-16: Web](https://app.standardnotes.com)

</details>

</div>

Standard Notes has [joined Proton AG](https://standardnotes.com/blog/joining-forces-with-proton) as of April 10, 2024.

### Notesnook

<div class="admonition recommendation" markdown>

![Notesnook logo](assets/img/notebooks/notesnook.svg){ align=right }

**Notesnook** is a free (as in speech) & open-source note-taking app focused on user privacy & ease of use. 外出先でメモを取るための強力な同期機能を備えており、すべてのプラットフォームでエンドツーエンドの暗号化を行います。 You can easily import your notes from Evernote, OneNote & a lot of other apps using their [official importer](https://importer.notesnook.com).

[:octicons-home-16: Homepage](https://notesnook.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://notesnook.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.notesnook.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/streetwriters/notesnook){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/streetwriters/notesnook/blob/master/CONTRIBUTING.md){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.streetwriters.notesnook)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1544027013)
- [:simple-github: GitHub](https://github.com/streetwriters/notesnook/releases)
- [:simple-windows11: Windows](https://notesnook.com/downloads)
- [:simple-apple: macOS](https://notesnook.com/downloads)
- [:simple-linux: Linux](https://notesnook.com/downloads)
- [:simple-firefoxbrowser: Firefox](https://notesnook.com/notesnook-web-clipper)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/notesnook-web-clipper/kljhpemdlcnjohmfmkogahelkcidieaj)

</details>

</div>

Notesnook only allows local note encryption with the [private vault](https://help.notesnook.com/lock-notes-with-private-vault) feature on their pro plan, otherwise your notes are not stored encrypted on your device. Your notes are always encrypted before being synced to their servers with keys which only you have access to.

### Joplin

<div class="admonition recommendation" markdown>

![Joplinのロゴ](assets/img/notebooks/joplin.svg){ align=right }

**Joplin**は、ノートやタグを管理し大量のMarkdownノートを扱える、フリー、オープンソース、フル機能のノートおよびToDoアプリケーションです。 エンドツーエンド暗号化対応で、NextcloudやDropboxなどを通じて同期できます。 また、Evernoteやプレーンテキストノートを簡単にインポートできます。

[:octicons-home-16: Homepage](https://joplinapp.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://joplinapp.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://joplinapp.org/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/laurent22/joplin){ .card-link title="Source Code" }
[:octicons-heart-16:](https://joplinapp.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.cozic.joplin)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1315599797)
- [:simple-github: GitHub](https://github.com/laurent22/joplin-android/releases)
- [:simple-windows11: Windows](https://joplinapp.org/#desktop-applications)
- [:simple-apple: macOS](https://joplinapp.org/#desktop-applications)
- [:simple-linux: Linux](https://joplinapp.org/#desktop-applications)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/joplin-web-clipper)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/joplin-web-clipper/alofnhikmmkdbbbgpnglcpdollgjjfek)

</details>

</div>

Joplin does not [support](https://github.com/laurent22/joplin/issues/289) password/PIN protection for the application itself or individual notes and notebooks. ただし、データはマスターキーを使用した暗号化により転送中および同期先では常に保護されます。 Since January 2023, Joplin [supports biometrics](https://github.com/laurent22/joplin/commit/f10d9f75b055d84416053fab7e35438f598753e9) app lock for Android and iOS.

### Cryptee

<div class="admonition recommendation" markdown>

![Cryptee ロゴ](./assets/img/notebooks/cryptee.svg#only-light){ align=right }
![Cryptee ロゴ](./assets/img/notebooks/cryptee-dark.svg#only-dark){ align=right }

**Cryptee**は、オープンソースでウェブベースの、端末間暗号化に対応したドキュメントエディターおよび写真ストレージのアプリケーションです。 CrypteeはPWAであり、それぞれのプラットフォームのネイティブアプリを必要とせず、最新のすべてのデバイスでシームレスに動作します。

[:octicons-home-16: Homepage](https://crypt.ee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://crypt.ee/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://crypt.ee/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/cryptee){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-globe-16: PWA](https://crypt.ee/download)

</details>

</div>

Crypteeは100MBのストレージを無料で提供しています。さらに必要な場合は有料オプションを利用できます。 サインアップには電子メールやその他の個人情報は必要ありません。

## ローカルノート

### Org-mode

<div class="admonition recommendation" markdown>

![Org-mode logo](assets/img/notebooks/org-mode.svg){ align=right }

**Org-mode** is a [major mode](https://gnu.org/software/emacs/manual/html_node/elisp/Major-Modes.html) for GNU Emacs. Org-modeを使うと、高速かつ効果的なプレーンテキスト システムにより、メモの保存、ToDoリストの管理、プロジェクトの計画、およびドキュメントの作成を行うことができます。 [ファイル同期](file-sharing.md#file-sync)ツールを使うと同期が可能です。

[:octicons-home-16: ホームページ](https://orgmode.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://orgmode.org/manuals.html){ .card-link title=文書 }
[:octicons-code-16:](https://git.savannah.gnu.org/cgit/emacs/org-mode.git){ .card-link title="ソースコード" }
[:octicons-heart-16:](https://liberapay.com/bzg){ .card-link title=貢献 }

</details>

</div>

## 規準

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる規準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

- クライアントはオープンソースであること。
- クラウド同期機能がエンドツーエンド暗号化であること。
- 文書を標準的な形式でエクスポートできること。

### 満たされることが望ましい基準

- ローカルバックアップ/同期機能は、暗号化に対応すべきである。
- クラウドベースのプラットフォームは、文書共有に対応すべきである。
