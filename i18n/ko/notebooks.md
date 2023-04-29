---
title: "Notebooks"
icon: material/notebook-edit-outline
description: These encrypted note-taking apps let you keep track of your notes without giving them to a third-party.
cover: notebooks.png
---

Keep track of your notes and journalings without giving them to a third-party.

If you are currently using an application like Evernote, Google Keep, or Microsoft OneNote, we suggest you pick an alternative here that supports E2EE.

## Cloud-based

### Joplin

!!! recommendation

    ![Joplin logo](assets/img/notebooks/joplin.svg){ align=right }
    
    **Joplin** is a free, open-source, and fully-featured note-taking and to-do application which can handle a large number of markdown notes organized into notebooks and tags. It offers E2EE and can sync through Nextcloud, Dropbox, and more. It also offers easy import from Evernote and plain-text notes.
    
    [:octicons-home-16: Homepage](https://joplinapp.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://joplinapp.org/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://joplinapp.org/help/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/laurent22/joplin){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://joplinapp.org/donate/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.cozic.joplin)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/joplin/id1315599797)
        - [:simple-github: GitHub](https://github.com/laurent22/joplin-android/releases)
        - [:simple-windows11: Windows](https://joplinapp.org/#desktop-applications)
        - [:simple-apple: macOS](https://joplinapp.org/#desktop-applications)
        - [:simple-linux: Linux](https://joplinapp.org/#desktop-applications)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/joplin-web-clipper/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/joplin-web-clipper/alofnhikmmkdbbbgpnglcpdollgjjfek)

Joplin does not support password/PIN protection for the [application itself or individual notes and notebooks](https://github.com/laurent22/joplin/issues/289). However, your data is still encrypted in transit and at the sync location using your master key. Since January 2023, Joplin supports biometrics app lock for [Android](https://joplinapp.org/changelog_android/#android-v2-10-3-https-github-com-laurent22-joplin-releases-tag-android-v2-10-3-pre-release-2023-01-05t11-29-06z) and [iOS](https://joplinapp.org/changelog_ios/#ios-v12-10-2-https-github-com-laurent22-joplin-releases-tag-ios-v12-10-2-2023-01-20t17-41-13z).

### Standard Notes

!!! recommendation

    ![Standard Notes logo](assets/img/notebooks/standard-notes.svg){ align=right }
    
    **Standard Notes** is a simple and private notes app that makes your notes easy and available everywhere you are. It features E2EE on every platform, and a powerful desktop experience with themes and custom editors. It has also been [independently audited (PDF)](https://s3.amazonaws.com/standard-notes/security/Report-SN-Audit.pdf).
    
    [:octicons-home-16: Homepage](https://standardnotes.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://standardnotes.com/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://standardnotes.com/help){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/standardnotes){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://standardnotes.com/donate){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.standardnotes)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1285392450)
        - [:simple-github: GitHub](https://github.com/standardnotes/app/releases)
        - [:simple-windows11: Windows](https://standardnotes.com)
        - [:simple-apple: macOS](https://standardnotes.com)
        - [:simple-linux: Linux](https://standardnotes.com)
        - [:octicons-globe-16: Web](https://app.standardnotes.com/)

### Cryptee

!!! recommendation

    ![Cryptee logo](./assets/img/notebooks/cryptee.svg#only-light){ align=right }
    ![Cryptee logo](./assets/img/notebooks/cryptee-dark.svg#only-dark){ align=right }
    
    **Cryptee** is an open-source, web-based E2EE document editor and photo storage application. Cryptee is a PWA, which means that it works seamlessly across all modern devices without requiring native apps for each respective platform.
    
    [:octicons-home-16: Homepage](https://crypt.ee){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://crypt.ee/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://crypt.ee/help){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/cryptee){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:octicons-globe-16: PWA](https://crypt.ee/download)

Cryptee offers 100MB of storage for free, with paid options if you need more. Sign-up doesn't require an e-mail or other personally identifiable information.

## Local notebooks

### Org-mode

!!! recommendation

    ![Org-mode logo](assets/img/notebooks/org-mode.svg){ align=right }
    
    **Org-mode** is a [major mode](https://www.gnu.org/software/emacs/manual/html_node/elisp/Major-Modes.html) for GNU Emacs. Org-mode is for keeping notes, maintaining to-do lists, planning projects, and authoring documents with a fast and effective plain-text system. Synchronization is possible with [file synchronization](file-sharing.md#file-sync) tools.
    
    [:octicons-home-16: Homepage](https://orgmode.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://orgmode.org/manuals.html){ .card-link title=Documentation}
    [:octicons-code-16:](https://git.savannah.gnu.org/cgit/emacs/org-mode.git){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://liberapay.com/bzg){ .card-link title=Contribute }

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

!!! example "이 단락은 최근에 만들어졌습니다"

    Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

- Clients must be open-source.
- Any cloud sync functionality must be E2EE.
- Must support exporting documents into a standard format.

### Best Case

- Local backup/sync functionality should support encryption.
- Cloud-based platforms should support document sharing.
