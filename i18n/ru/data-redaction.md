---
meta_title: "Удаление ПД с помощью инструментов удаления метаданных и редактирования данных - Privacy Guides"
title: "Редактирование данных и метаданных"
icon: material/tag-remove
description: Используйте эти инструменты для удаления метаданных, таких как местоположение GPS и другой идентифицирующей информации, с фотографий и файлов, которыми вы делитесь.
cover: data-redaction.png
---

Когда вы делитесь с кем-то файлами, то не забудьте удалить связанные с ними метаданные. Файлы изображений обычно содержат [данные EXIF](https://ru.wikipedia.org/wiki/Exif). Иногда фотографии даже содержат ваши GPS координаты в метаданных файла.

## Для компьютеров

### MAT2

!!! recommendation

    ![Логотип MAT2](assets/img/data-redaction/mat2.svg){ align=right }
    
    **MAT2** - это бесплатное программное обеспечение, которое позволяет удалять метаданные из изображений, аудио, торрентов и документов. Оно предоставляет как инструмент командной строки, так и графический интерфейс пользователя через [расширение для Nautilus](https://0xacab.org/jvoisin/mat2/-/tree/master/nautilus) (файловый менеджер по умолчанию в [GNOME](https://www.gnome.org)), и [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin) (файловый менеджер по умолчанию в [KDE](https://kde.org)).
    
    В Linux существует сторонний графический инструмент [Metadata Cleaner](https://gitlab.com/rmnvgr/metadata-cleaner) на базе MAT2, который [доступен на Flathub](https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner).
    
    [:octicons-repo-16: Репозиторий](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
    [:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title=Документация}
    [:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-windows11: Windows](https://pypi.org/project/mat2)
        - [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
        - [:simple-linux: Linux](https://pypi.org/project/mat2)
        - [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

## Для телефонов

### ExifEraser (Android)

!!! recommendation

    ![Логотип ExifEraser](assets/img/data-redaction/exiferaser.svg){ align=right }
    
    **ExifEraser** - это современное приложение, не требующее разрешений, для удаления метаданных изображений для Android.
    
    В настоящее время он поддерживает файлы JPEG, PNG и WebP.
    
    [:octicons-repo-16: Репозиторий](https://github.com/Tommy-Geenexus/exif-eraser){ .md-button .md-button--primary }
    [:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
        - [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
        - [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

Удаляемые метаданные зависят от типа файла изображения:

* **JPEG**: ICC Профиль, Exif, Photoshop Image Resources и XMP/ExtendedXMP будут удалены, если они существуют.
* **PNG**: ICC Profile, Exif и XMP будут удалены, если они существуют.
* **WebP**: ICC Profile, Exif и XMP будут удалены, если они существуют.

После обработки изображений ExifEraser предоставляет вам полный отчет о том, что именно было удалено с каждого изображения.

Приложение предлагает несколько способов удаления метаданных с изображений. А именно:

* С помощью ExifEraser можно поделиться изображением из другого приложения.
* В самом приложении можно выбрать одно изображение, несколько изображений сразу или даже целый каталог.
* В нем есть опция "Камера", которая использует приложение камеры вашей операционной системы для создания фотографии, а затем удаляет из нее метаданные.
* Он позволяет перетаскивать фотографии из другого приложения в ExifEraser, когда они оба открыты в режиме разделенного экрана.
* Наконец, он позволяет вставить изображение из буфера обмена.

### Metapho (iOS)

!!! recommendation

    ![Логотип Metapho](assets/img/data-redaction/metapho.jpg){ align=right }
    
    **Metapho** - это простая и чистая программа для просмотра метаданных фотографии, таких как дата, имя файла, размер, модель камеры, выдержка и местоположение.
    
    [:octicons-home-16: Домашняя страница](https://zininworks.com/metapho){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://zininworks.com/privacy/){ .card-link title="Политика конфиденциальности" }
    
    ??? downloads "Скачать"
    
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/metapho/id914457352)

### PrivacyBlur

!!! recommendation

    ![Логотип PrivacyBlur](assets/img/data-redaction/privacyblur.svg){ align=right }
    
    **PrivacyBlur** - это бесплатное приложение, которое позволяет размыть чувствительные части фотографий перед тем, как поделиться ими в интернете.
    
    [:octicons-home-16: Домашняя страница](https://privacyblur.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://privacyblur.app/privacy.html){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://github.com/MATHEMA-GmbH/privacyblur#readme){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/MATHEMA-GmbH/privacyblur){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.mathema.privacyblur)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/privacyblur/id1536274106)

!!! warning "Осторожно"

    Вы **никогда** не должны использовать размытие для редактирования [текста на изображениях] (https://bishopfox.com/blog/unredacter-tool-never-pixelation). Если вы хотите скрыть текст на изображении, закройте текст черным квадратом. Для этого мы предлагаем такие приложения, как [Pocket Paint](https://github.com/Catrobat/Paintroid).

## Для командной строки

### ExifTool

!!! recommendation

    ![Логотип ExifTool](assets/img/data-redaction/exiftool.png){ align=right }
    
    **ExifTool** - это оригинальная библиотека perl и приложение командной строки для чтения, записи и редактирования метаинформации (Exif, IPTC, XMP и др.) в самых разных форматах файлов (JPEG, TIFF, PNG, PDF, RAW и др.).
    
    Он часто является компонентом других приложений для удаления Exif и находится в репозиториях большинства дистрибутивов Linux.
    
    [:octicons-home-16: Домашняя страница](https://exiftool.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-windows11: Windows](https://exiftool.org)
        - [:simple-apple: macOS](https://exiftool.org)
        - [:simple-linux: Linux](https://exiftool.org)

!!! example "Удаление данных из каталога файлов"

    ```bash
    exiftool -all= *.file_extension
    ```

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

!!! example "Это новый раздел"

    Мы всё еще работаем над установлением критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у вас есть вопросы по поводу наших критериев, пожалуйста, [задавайте их на нашем форуме](https://discuss.privacyguides.net/latest). Если какой-то критерий здесь не указан, это не значит, что мы его не учли. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

- Приложения, разработанные для операционных систем с открытым исходным кодом, должны быть с открытым исходным кодом.
- Приложения должны быть бесплатными и не должны содержать рекламы или других ограничений.
