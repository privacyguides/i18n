---
title: "Pastebins"
icon: material/content-paste
description: These tools allow you to have full control of any pasted data you share to other parties.
cover: pastebins.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

[**Pastebins**](https://en.wikipedia.org/wiki/Pastebin) are online services most commonly used to share large blocks of code in a convenient and efficient manner. The pastebins listed here employ client-side encryption and password protection for pasted content; both of these features prevent the website or server operator from reading or accessing the contents of any paste.

## PrivateBin

<div class="admonition recommendation" markdown>

![PrivateBin logo](assets/img/pastebins/privatebin.svg){ align=right }

**PrivateBin** is a minimalist, open-source, online pastebin where the server has zero knowledge of pasted data. Данные шифруются/дешифруются в браузере с помощью 256-битного AES. Это улучшенная версия ZeroBin.

[:octicons-home-16: Homepage](https://privatebin.info){ .md-button .md-button--primary }
[:octicons-server-16:](https://privatebin.info/directory){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/wiki/FAQ){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Source Code" }

</div>

## Paaster

<div class="admonition recommendation" markdown>

![Paaster logo](assets/img/pastebins/paaster.svg){ align=right }

**Paaster** is a secure and user-friendly pastebin application that prioritizes privacy and simplicity. With end-to-end encryption and paste history, Paaster ensures that your pasted code remains confidential and accessible.

[:octicons-home-16: Homepage](https://paaster.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://paaster.io/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/WardPearce/paaster#security){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/WardPearce/paaster){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/WardPearce){ .card-link title="Contribute" }

</div>

## Критерии

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

### Минимальные требования к сервисам

- Исходный код проекта должен быть открыт.
- Must implement "zero-trust" E2EE.
- Должен поддерживать файлы, защищенные паролем.

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Should have a published audit from a reputable, independent third party.
