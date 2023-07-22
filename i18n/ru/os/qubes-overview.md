---
title: "Обзор Qubes"
icon: simple/qubesos
description: Qubes - это операционная система, построенная на изоляции приложений в виртуальных машинах для обеспечения повышенной безопасности.
---

[**Qubes OS**](../desktop.md#qubes-os) is an open-source operating system which uses the [Xen](https://en.wikipedia.org/wiki/Xen) hypervisor to provide strong security for desktop computing through isolated virtual machines. Каждая ВМ называется *Qube*, и вы можете назначить каждому Qube уровень доверия в зависимости от его назначения. As Qubes OS provides security by using isolation, and only permitting actions on a per-case basis, it is the opposite of [badness enumeration](https://www.ranum.com/security/computer_security/editorials/dumb/).

## Как работает Qubes OS?

Qubes использует [компартментализацию(разделение)](https://www.qubes-os.org/intro/) для обеспечения безопасности системы. Qubes создаются на основе шаблонов, по умолчанию Fedora, Debian и [Whonix](../desktop.md#whonix). Qubes OS также позволяет создавать [одноразовые](https://www.qubes-os.org/doc/how-to-use-disposables/) виртуальные машины.

![Архитектура Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Qubes Architecture, Credit: What is Qubes OS Intro</figcaption>

Каждое приложение Qubes имеет [цветную рамку](https://www.qubes-os.org/screenshots/), которая помогает вам понять, в какой виртуальной машине оно запущено. Например, вы можете использовать определенный цвет для банковского браузера, а другой цвет - для общего ненадежного браузера.

![Цветная рамка](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Qubes window borders, Credit: Qubes Screenshots</figcaption>

## Почему мне стоит использовать Qubes?

Qubes OS полезна, если ваша [модель угроз](../basics/threat-modeling.md) требует сильного разделения и безопасности, например, если вы думаете, что будете открывать недоверенные файлы из недоверенных источников. Типичная причина использования Qubes OS - открытие документов из неизвестных источников.

Qubes OS использует ВМ [Dom0](https://wiki.xenproject.org/wiki/Dom0) Xen (т.е. "AdminVM") для управления другими гостевыми ВМ или Qubes на хостовой ОС. Другие ВМ отображают отдельные окна приложений в среде рабочего стола Dom0. Это позволяет вам выделять окна цветом в зависимости от уровня доверия и запускать приложения, которые могут взаимодействовать друг с другом с очень детальным контролем.

### Копирование и вставка текста

Вы можете [копировать и вставлять текст](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/), используя `qvm-copy-to-vm` или приведенные ниже инструкции:

1. Нажмите **Ctrl+C**, чтобы сообщить ВМ, в которой вы находитесь, что вы хотите что-то скопировать.
2. Нажмите **Ctrl+Shift+C**, чтобы указать ВМ сделать этот буфер доступным для глобального буфера обмена.
3. Нажмите **Ctrl+Shift+V** в ВМ назначения, чтобы сделать доступным глобальный буфер обмена.
4. Нажмите **Ctrl+V** в целевой ВМ, чтобы вставить содержимое в буфер.

### Обмен файлами

Для копирования и вставки файлов и каталогов (папок) из одной ВМ в другую можно воспользоваться опцией **Copy to Other AppVM...** или **Move to Other AppVM...**. Разница в том, что опция **Move** удалит исходный файл. Любой из этих вариантов защитит ваш буфер обмена от утечки к другим Qubes. Это более безопасно, чем передача файлов по воздуху, поскольку компьютер с передачей по воздуху все равно будет вынужден парсить разделы или файловые системы. Этого не требуется при использовании системы копирования между несколькими Qubes.

??? info "AppVMs или qubes не имеют собственных файловых систем"

    Вы можете [копировать и перемещать файлы](https://www.qubes-os.org/doc/how-to-copy-and-move-files/) между Qubes. При этом изменения вносятся не сразу и могут быть легко отменены в случае аварии.

### Взаимодействие между ВМ

[Фреймворк qrexec](https://www.qubes-os.org/doc/qrexec/) является основной частью Qubes, которая позволяет виртуальным машинам взаимодействовать между доменами. Он построен на базе библиотеки Xen *vchan*, которая обеспечивает изоляцию [с помощью политик](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## Дополнительные советы

Для получения дополнительной информации мы рекомендуем вам обратиться к обширной документации Qubes OS, расположенной на сайте [Qubes OS Website](https://www.qubes-os.org/doc/). Офлайн копии можно загрузить из [репозитория документации](https://github.com/QubesOS/qubes-doc) Qubes OS.

- Фонд открытых технологий: [*Пожалуй, самая безопасная операционная система в мире*](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/)
- J. Rutkowska: [*Программная компартментализация против физического разделения*](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf)
- J. Rutkowska: [*Разделение моей цифровой жизни по доменам безопасности*](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html)
- Qubes OS: [*Связанные статьи*](https://www.qubes-os.org/news/categories/#articles)
