---
title: Обзор macOS
icon: material/apple-finder
description: macOS — это настольная операционная система Apple, которая работает с их оборудованием для обеспечения высокого уровня безопасности.
---

**macOS** — это Unix-операционная система, разработанная Apple для их компьютеров Mac. Для повышения приватности в macOS вы можете отключить функции телеметрии и усилить существующие настройки приватности и безопасности.

Старые Mac на базе Intel и Hackintosh не поддерживают все функции безопасности, которые предлагает macOS. Для повышения безопасности данных мы рекомендуем использовать более новый Mac с [Apple Silicon](https://support.apple.com/HT211814).

## Примечания о приватности

Существует несколько заметных проблем с приватностью в macOS, которые вам следует учитывать. Они относятся к самой операционной системе, а не к другим приложениям и службам Apple.

### Блокировка активации

Совершенно новые устройства Apple Silicon можно настроить без подключения к интернету. Однако восстановление или сброс Mac **потребует** подключения к интернету для соединения с серверами Apple, чтобы проверить устройство по базе данных Блокировки активации утерянных или украденных устройств.

### Проверка отзыва приложений

macOS выполняет онлайн-проверки при открытии приложения, чтобы убедиться, что приложение не содержит известного вредоносного ПО, и что сертификат разработчика не отозван.

Сервис OCSP от Apple использует шифрование HTTPS, поэтому только они могут видеть, какие приложения вы открываете. Они [опубликовали информацию](https://support.apple.com/HT202491) о своей политике ведения журналов для этой службы. Кроме того, они [обещали](http://lapcatsoftware.com/articles/2024/8/3.html) добавить механизм для отказа от этой онлайн-проверки, но это ещё не было добавлено в macOS.

Хотя вы [можете](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private) вручную отказаться от этой проверки относительно легко, мы рекомендуем не делать этого, если только вы не будете серьезно скомпрометированы проверками отзыва, выполняемыми macOS, поскольку они играют важную роль в обеспечении блокировки скомпрометированных приложений.

## Рекомендованные настройки

Первая учётная запись, создаваемая при настройке Mac, получает административные права, превосходящие привилегии стандартного пользователя. macOS имеет ряд защитных механизмов, которые предотвращают злоупотребление вашими привилегиями Администратора вредоносным ПО и другими программами, поэтому обычно безопасно использовать эту учетную запись.

Однако эксплойты в защитных утилитах, таких как `sudo`, были [обнаружены в прошлом](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass). Для повседневной работы рекомендуется создать отдельную Стандартную учетную запись, что поможет избежать злоупотребления административными привилегиями. Это имеет дополнительное преимущество, делая более очевидным, когда приложению требуется доступ администратора, поскольку оно будет запрашивать учётные данные каждый раз.

Если вы используете вторую учётную запись, не обязательно когда-либо входить в свою исходную учетную запись Администратора с экрана входа в macOS. Когда вы выполняете действие как Стандартный пользователь, требующее разрешений Администратора, система должна запросить аутентификацию, где вы можете ввести свои учётные данные Администратора как Стандартный пользователь на разовой основе. Apple предоставляет [руководство](https://support.apple.com/HT203998) по скрытию вашей учетной записи Администратора, если вы предпочитаете видеть только одну учетную запись на экране входа.

### iCloud

Когда вы используете службы Apple, такие, как iCloud, большая часть вашей информации хранится на их серверах и защищена ключами, *к которым Apple имеет доступ* по умолчанию. Это называется [Стандартной защитой данных](https://support.apple.com/en-us/102651) по терминологии Apple.

Поэтому, если вы используете iCloud, вам следует [включить **Расширенную защиту данных**](https://support.apple.com/HT212520). Это шифрует почти все ваши данные iCloud с помощью ключей, хранящихся на ваших устройствах (сквозное шифрование), а не на серверах Apple, так что ваши данные iCloud защищены в случае утечки данных и в целом скрыты от Apple.

Если вы хотите иметь возможность устанавливать приложения из App Store, но не хотите включать iCloud, вы можете войти в свою учетную запись Apple из App Store вместо **Системных настроек**.

### Системные настройки

Существует ряд встроенных настроек, которые вы должны подтвердить или изменить для усиления вашей системы. Откройте приложение **"Настройки** ":

#### Bluetooth

- [ ] Отключите **Bluetooth** (если вы не используете его в данный момент)

#### Сеть

В зависимости от того, используете ли вы **Wi-Fi** или **Ethernet** (обозначается зеленой точкой и словом "подключено"), нажмите на соответствующий значок.

Нажмите кнопку "Подробнее" рядом с именем вашей сети:

- [x] Выберите **Ротация адреса** в разделе **Частный адрес Wi-Fi**

- [x] Включите **Ограничение трекинга по IP-адресу**

##### Брандмауэр

Ваш брандмауэр блокирует нежелательные сетевые подключения. Чем строже настройки вашего брандмауэра, тем безопаснее ваш Mac. Однако некоторые службы будут заблокированы. Вам следует настроить брандмауэр так, чтобы он был максимально строгим, не блокируя при этом службы, которые вы используете.

- [x] Включите **Брандмауэр**

Нажмите кнопку **Параметры**:

- [x] Включите **Блокировать все входящие подключения**

Если эта конфигурация слишком строгая, вы можете вернуться и снять этот флажок. Однако macOS обычно предложит вам разрешить входящие подключения для приложения, если приложение запрашивает это.

#### Основные

По умолчанию имя вашего устройства будет что-то вроде "iMac [вашего имени]". Поскольку это имя [публично транслируется в вашей сети](https://support.apple.com/guide/mac-help/change-computers-local-hostname-mac-mchlp2322/26/mac/26#:~:text=The%20local%20hostname%2C%20or%20local%20network%20name%2C%20is%20displayed%20at%20the%20bottom%20of%20the%20Sharing%20settings%20window.%20It%20identifies%20your%20Mac%20to%20Bonjour%2Dcompatible%20services.), вы захотите изменить имя устройства на что-то общее, например "Mac".

Нажмите на **Описание** и введите желаемое имя устройства в поле **Имя**.

##### Обновление ПО

Вы должны автоматически устанавливать все доступные обновления, чтобы убедиться, что ваш Mac имеет последние исправления безопасности.

Нажмите на небольшой значок :material-information-outline: рядом с **Автообновление**:

- [x] Включите **Загружать обновления, если они доступны**

- [x] Включите **Устанавливать обновления macOS**

- [x] Включите **Устанавливать системные файлы и обновления системы безопасности**

#### Apple Intelligence и Siri

Если вы не используете эти функции в macOS, вам следует отключить их:

- [ ] Отключите **Apple Intelligence**
- [ ] Отключите **Siri**

**[Apple Intelligence](https://apple.com/legal/privacy/data/en/intelligence-engine)** доступен только если ваше устройство поддерживает его. Apple Intelligence использует комбинацию обработки на устройстве и их [Private Cloud Compute](https://security.apple.com/blog/private-cloud-compute) для задач, которые требуют больше вычислительной мощности, чем может предоставить ваше устройство.

Чтобы увидеть отчет обо всех данных, отправленных через Apple Intelligence, вы можете перейти в **Конфиденциальность и безопасность** → **Отчет Apple Intelligence** и нажать **Экспорт активности**, чтобы увидеть активность за последние 15 минут или 7 дней, в зависимости от ваших настроек. Подобно **Отчету о конфиденциальности приложений**, который показывает вам недавно используемые разрешения приложениями на вашем телефоне, Отчет Apple Intelligence аналогично показывает, что отправляется на серверы Apple при использовании Apple Intelligence.

По умолчанию интеграция с ChatGPT отключена. Если вы больше не хотите использовать интеграцию с ChatGPT, вы можете перейти в **ChatGPT**:

- [ ] Отключите **Использовать ChatGPT**

Вы также можете настроить запрос подтверждения каждый раз, если оставляете интеграцию с ChatGPT включенной:

- [x] Включите **Подтверждать запросы**

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Любой запрос, сделанный с помощью ChatGPT, будет отправлен на серверы ChatGPT, без обработки на устройстве и без PCC, как в случае с Apple Intelligence.

</div>

#### Приватность и защита

Когда приложение запрашивает разрешение, оно отобразится здесь. Вы можете решить, каким приложениям вы хотите разрешить или запретить определенные разрешения.

##### Службы геолокации

Вы можете разрешать службы геолокации для каждого приложения отдельно. Если вам не нужно, чтобы приложения использовали ваше местоположение, полное отключение служб геолокации является наиболее приватным вариантом.

- [ ] Отключите **Службы геолокации**

##### Аналитика и улучшения

Решите, хотите ли вы делиться аналитическими данными с Apple и разработчиками приложений.

##### Реклама от Apple

Решите, хотите ли вы получать персонализированную рекламу на основе вашего использования.

- [ ] Отключите **Контекстную рекламу**

##### FileVault

На современных устройствах с Secure Enclave (чип безопасности Apple T2, Apple Silicon) ваши данные всегда зашифрованы, но автоматически расшифровываются аппаратным ключом, если ваше устройство не обнаруживает, что оно было взломано. Включение [FileVault](../encryption.md#filevault) дополнительно требует вашего пароля для расшифровки ваших данных, значительно повышая безопасность, особенно при выключенном питании или перед первым входом после включения.

На старых компьютерах Mac на базе Intel FileVault — единственная форма шифрования диска, доступная по умолчанию, и она всегда должна быть включена.

- [x] Нажмите **Включить**

##### Режим блокировки

**[Режим блокировки](https://support.apple.com/guide/mac-help/lock-mac-targeted-a-cyberattack-ibrw66f4e191/mac)** отключает некоторые функции для повышения безопасности. Некоторые приложения или функции не будут работать так же, как при его отключении. Например, компиляция Javascript Just-In-Time ([JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers)) и [WebAssembly](https://developer.mozilla.org/docs/WebAssembly) отключены в Safari при включенном режиме блокировки. Мы рекомендуем включить режим блокировки и проверить, влияет ли это существенно на повседневное использование.

- [x] Нажмите **Включить**

### Рандомизация MAC-адресов

macOS использует случайный MAC-адрес при [выполнении сканирования Wi-Fi](https://support.apple.com/guide/security/privacy-features-connecting-wireless-networks-secb9cb3140c/web), когда устройство не подключено к сети.

Вы можете настроить [случайный MAC-адрес](https://support.apple.com/en-us/102509) для каждой сети с периодической ротацией, чтобы предотвратить отслеживание между сетями и в одной и той же сети с течением времени.

Перейдите в **Системные настройки** → **Сеть** → **Wi-Fi** → **Подробнее** и установите **Частный адрес Wi-Fi** на **Статический адрес**, если вы хотите иметь фиксированный, но уникальный адрес для сети, к которой вы подключены, или **Ротация адреса**, если вы хотите, чтобы он менялся со временем.

Рассмотрите возможность изменения имени хоста — идентификатора, транслируемого в вашей сети. Вы можете установить имя хоста на что-то общее, например "MacBook Air", "Ноутбук", "MacBook Pro Ивана" или "iPhone" в **Системные настройки** → **Основные** → **Общий доступ**.

## Защитные механизмы

macOS использует многоуровневую защиту, полагаясь на несколько слоев программных и аппаратных средств защиты с различными свойствами. Это гарантирует, что сбой в одном слое не компрометирует общую безопасность системы.

### Программная безопасность

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

macOS позволяет устанавливать бета-обновления. Они нестабильны и могут содержать [дополнительную телеметрию](https://beta.apple.com/privacy) , поскольку предназначены для тестирования. Из-за этого мы рекомендуем вам в целом избегать бета-программного обеспечения.

</div>

#### Подписанный системный том

Системные компоненты macOS защищены в доступном только для чтения [подписанном системном томе](https://support.apple.com/guide/security/signed-system-volume-security-secd698747c9/web), что означает, что ни вы, ни вредоносное ПО не можете изменять важные системные файлы.

Системный том проверяется во время работы, и любые данные, не подписанные действительной криптографической подписью от Apple, будут отклонены.

#### Защита целостности системы

macOS устанавливает определенные ограничения безопасности, которые нельзя обойти. Они называются [Обязательными средствами контроля доступа](https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/1/web/1) и формируют основу песочницы, родительского контроля и [Защиты целостности системы](https://support.apple.com/en-us/102149) в macOS.

Защита целостности системы делает критически важные местоположения файлов доступными только для чтения, чтобы защитить их от изменений вредоносным кодом. Это дополняет аппаратную защиту целостности ядра, которая предотвращает модификацию ядра в памяти.

#### Безопасность приложений

##### Песочница приложений

В macOS то, находится ли приложение в песочнице, определяется разработчиком при его подписании. [Песочница приложений](https://developer.apple.com/documentation/xcode/configuring-the-macos-app-sandbox) защищает от уязвимостей в запускаемых приложениях, ограничивая то, к чему злоумышленник может получить доступ в случае эксплуатации приложения. Песочница приложений *сама по себе* не может защитить от [:material-package-variant-closed-remove: Атак цепочки поставок](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} со стороны злонамеренных разработчиков. Для этого песочница должна контролироваться кем-то другим, кроме самого разработчика, как это происходит в [App Store](https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/1/web/1#:~:text=All%20apps%20from%20the%20App%20Store%20are%20sandboxed%20to%20restrict%20access%20to%20data%20stored%20by%20other%20apps.).

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Программное обеспечение, загруженное из-за пределов официального App Store, не обязано находиться в песочнице. Если ваша модель угроз приоритезирует защиту от :material-bug-outline: Пассивных атак(../basics/common-threats.md#security-and-privacy){ .pg-orange }, то вам, возможно, стоит проверить, находится ли программное обеспечение, загружаемое вами вне App Store, в песочнице, что зависит от разработчика, который должен включить эту опцию.

</div>

Вы можете проверить, использует ли приложение песочницу, несколькими способами:

Вы можете проверить, находятся ли уже запущенные приложения в песочнице, используя [Мониторинг активности](https://developer.apple.com/documentation/security/protecting-user-data-with-app-sandbox#Verify-that-your-app-uses-App-Sandbox).

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

То, что один из процессов приложения находится в песочнице, не означает, что все они там находятся.

</div>

В качестве альтернативы, вы можете проверить приложения перед их запуском, выполнив следующую команду в терминале:

``` zsh
codesign -dvvv --entitlements - <путь к вашему приложению>
```

Если приложение находится в песочнице, вы должны увидеть следующий вывод:

``` zsh
    [Key] com.apple.security.app-sandbox
    [Value]
        [Bool] true
```

Если вы обнаружите, что приложение, которое вы хотите запустить, не находится в песочнице, то вы можете использовать методы [компартментализации](../basics/common-threats.md#security-and-privacy), такие как виртуальные машины или отдельные устройства, использовать аналогичное приложение, которое находится в песочнице, или полностью отказаться от использования приложения, не находящегося в песочнице.

##### Hardened Runtime

The [Hardened Runtime](https://developer.apple.com/documentation/security/hardened_runtime) — это дополнительная форма защиты приложений, которая предотвращает определенные классы эксплойтов. Она повышает безопасность приложений от эксплуатации, отключая определенные функции, такие как JIT.

Вы можете проверить, использует ли приложение Hardened Runtime, с помощью этой команды:

``` zsh
codesign -dv <путь к вашему приложению>
```

Если Hardened Runtime включена, вы увидите `flags=0x10000(runtime)`. Вывод `runtime` означает, Hardened Runtime включена. Могут быть и другие флаги, но флаг runtime — это то, что мы ищем здесь.

Вы можете включить столбец в Мониторинге системы под названием "Ограничено", который является флагом, предотвращающим внедрение кода программами через [динамический компоновщик](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html) macOS. В идеале, здесь должно быть указано "Да".

##### Антивирус

macOS поставляется с двумя формами [защиты от вредоносного ПО](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/1/web/1):

1. Защита от запуска вредоносного ПО в первую очередь обеспечивается процессом проверки App Store для приложений из App Store или *Нотаризацией* (часть *Gatekeeper*), процессом, при котором сторонние приложения сканируются на наличие известного вредоносного ПО компанией Apple, прежде чем им разрешается запуск. Приложения должны быть подписаны разработчиками с использованием ключа, предоставленного им Apple. Это гарантирует, что вы запускаете программное обеспечение от настоящих разработчиков. Нотаризация также требует, чтобы разработчики включали усиленное время выполнения для своих приложений, что ограничивает методы эксплуатации.
2. Protection against other malware and remediation from existing malware on your system is provided by *XProtect*, a more traditional antivirus software built-in to macOS.

We recommend against installing third-party antivirus software as they typically do not have the system-level access required to properly function anyway, because of Apple's limitations on third-party apps, and because granting the high levels of access they do ask for often poses an even greater security and privacy risk to your computer.

##### Резервное копирование

macOS comes with automatic backup software called [Time Machine](https://support.apple.com/HT201250), so you can create [encrypted backups](https://support.apple.com/guide/mac-help/keep-your-time-machine-backup-disk-secure-mh21241/mac) to an external drive or a network drive in the event of corrupted/deleted files.

### Hardware Security

Many modern security features in macOS—such as modern Secure Boot, hardware-level exploit mitigation, OS integrity checks, and file-based encryption—rely on Apple Silicon, and Apple's newer hardware always has the [best security](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). We only encourage the use of Apple Silicon, and not older Intel-based Mac computers or Hackintoshes.

Some of these modern security features are available on older Intel-based Mac computers with the Apple T2 Security Chip, but that chip is susceptible to the *checkm8* exploit which could compromise its security.

If you use Bluetooth accessories such as a keyboard, we recommend that you use official Apple ones as their firmware will [automatically be updated](https://support.apple.com/en-us/120303#:~:text=Firmware%20updates%20are%20automatically%20delivered%20in%20the%20background%20while%20the%20Magic%20Keyboard%20is%20actively%20paired%20to%20a%20device%20running%20macOS%2C%20iOS%2C%20iPadOS%2C%20or%20tvOS.) for you by macOS. Using third party accessories is fine, but you should remember to install firmware updates for them regularly.

Apple's SoCs focus on [minimizing attack surface](https://support.apple.com/en-vn/guide/security/secf020d1074/web#:~:text=Security%2Dfocused%20hardware%20follows%20the%20principle%20of%20supporting%20limited%20and%20discretely%20defined%20functions%20to%20minimize%20attack%20surface.) by relegating security functions to dedicated hardware with limited functionality.

#### Boot ROM

macOS prevents malware persistence by only allowing official Apple software to run at boot time; this is known as [secure boot](https://support.apple.com/en-vn/guide/security/secac71d5623/1/web/1). Mac computers verify this with a bit of read-only memory on the SoC called the [boot ROM](https://support.apple.com/en-vn/guide/security/aside/sec5240db956/1/web/1), which is [laid down during the manufacturing of the chip](https://support.apple.com/en-vn/guide/security/secf020d1074/1/web/1#:~:text=which%20is%20laid%20down%20during%20Apple%20SoC%20fabrication).

The boot ROM forms the hardware root of trust. This ensures that malware cannot tamper with the boot process, since the boot ROM is immutable. When your Mac boots up, the boot ROM is the first thing that runs, forming the first link in the chain of trust.

Mac computers can be configured to boot in [three security modes](https://support.apple.com/guide/deployment/startup-security-dep5810e849c/web#dep32fb404e1): *Full Security*, *Reduced Security*, and *Permissive Security*, with the default setting being Full Security. You should ideally be using Full Security mode and avoid things like **[kernel extensions](https://support.apple.com/guide/deployment/system-extensions-in-macos-depa5fb8376f/web#dep51e097f45)** that force you to lower your security mode. Make sure to [check](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) that you're using Full Security mode.

#### Secure Enclave

The **[Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/web)** is a security chip built into devices with Apple Silicon which is responsible for storing and generating encryption keys for data at rest as well as Face ID and Touch ID data. It contains its own [separate boot ROM](https://support.apple.com/en-vn/guide/security/sec59b0b31ff/web#sec43006c49f).

You can think of the Secure Enclave as your device's security hub: it has an AES encryption engine and a mechanism to securely store your encryption keys, and it's separated from the rest of the system, so even if the main processor is compromised, it should still be safe.

#### Touch ID

Apple's Touch ID feature allows you to securely unlock your devices using biometrics.

Your biometric data [never leaves your device](https://www.apple.com/legal/privacy/data/en/touch-id/#:~:text=Touch%C2%A0ID%20data%20does%20not%20leave%20your%20device%2C%20and%20is%20never%20backed%20up%20to%20iCloud%20or%20anywhere%20else.); it's stored only in the Secure Enclave.

#### Hardware Microphone Disconnect

All laptops with Apple Silicon or the T2 chip feature a [hardware disconnect](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web) for the built-in microphone whenever the lid is closed. This means that there is no way for an attacker to listen to your Mac's microphone even if the operating system is compromised.

Note that the camera does not have a hardware disconnect, since its view is obscured when the lid is closed anyway.

#### Secure Camera Indicator

The built-in camera in a Mac is designed so that the camera can't turn on without the camera indicator light [also turning on](https://support.apple.com/en-us/102177#:~:text=The%20camera%20is%20engineered%20so%20that%20it%20can’t%20activate%20without%20the%20camera%20indicator%20light%20also%20turning%20on.%20This%20is%20how%20you%20can%20tell%20if%20your%20camera%20is%20on.).

#### Peripheral Processor Security

Computers have [built-in processors](https://support.apple.com/en-vn/guide/security/seca500d4f2b/1/web/1) other than the main CPU that handle things like networking, graphics, power management, etc. These processors can have insufficient security and become compromised, therefore Apple tries to minimize the need for these processors in their hardware.

When it is necessary to use one of these processors, Apple works with the vendor to ensure that the processor

- runs verified firmware from the primary CPU on startup
- has its own Secure Boot chain
- follows minimum cryptographic standards
- ensures known bad firmware is properly revoked
- has its debug interfaces disabled
- is signed with Apple's cryptographic keys

#### Direct Memory Access Protections

Apple Silicon separates each component that requires [direct memory access](https://support.apple.com/guide/security/direct-memory-access-protections-seca4960c2b5/1/web/1). For example, a Thunderbolt port can't access memory designated for the kernel.

#### Terminal Secure Keyboard Entry

Enable [Secure Keyboard Entry](https://support.apple.com/guide/terminal/use-secure-keyboard-entry-trml109/mac) to prevent other apps from detecting what you type in the terminal.
