---
meta_title: "Как создавать аккаунты в интернете конфиденциально - Privacy Guides"
title: "Создание аккаунтов"
icon: 'material/account-plus'
description: Создание аккаунтов в интернете является, практически, необходимостью, предпримите следующие шаги, чтобы сохранить вашу конфиденциальность.
---

Часто люди регистрируются на сайтах, не задумываясь. Возможно, это стриминг, позволяющий смотреть новое шоу, о котором все говорят, или аккаунт, предоставляющий скидку в любимом заведении быстрого питания. В любом случае вы должны рассмотреть сегодняшние и последующие последствия для ваших данных.

Определённые риски связаны с каждой новой услугой, которой вы пользуетесь. Утечки данных; раскрытие информации о клиенте третьим лицам; недобросовестные сотрудники, получившие доступ к данным - все это возможности, которые необходимо учитывать при передаче информации. Вы должны быть уверены, что можете доверять сервису, поэтому мы не рекомендуем хранить ценные данные ни на чем, кроме самых совершенных и проверенных в боях продуктов. Обычно это означает сервисы, предоставляющие E2EE и прошедшие криптографический аудит. Аудит повышает уверенность в том, что продукт был разработан без проблем безопасности, вызванных неопытностью разработчиков.

Также может быть сложно удалить учетные записи в некоторых сервисах. Иногда возможна [перезапись данных](account-deletion.md#overwriting-account-information), связанных с учетной записью, но в остальных случаях служба будет хранить всю историю изменений учетной записи.

## Условия использования & Политика конфиденциальности

Условия использования - это правила использования сервиса, с которыми вы соглашаетесь. В крупных сервисах за соблюдением этих правил часто следят автоматизированные системы. Иногда эти автоматизированные системы могут допускать ошибки. Например, вас могут забанить или заблокировать ваш аккаунт в некоторых сервисах за использование VPN или номера VOIP. Обжаловать такие запреты часто бывает сложно, к тому же этот процесс автоматизирован и не всегда успешен. Это одна из причин, по которой мы не советуем использовать Gmail для электронной почты. Электронная почта имеет критическое значение для доступа к другим сервисам, на которые вы, возможно, подписались.

Политика конфиденциальности - это то, как сервис заявляет, что будет использовать ваши данные, и ее стоит прочитать, чтобы вы понимали, как будут использоваться ваши данные. Компания или организация может не быть юридически обязана следовать всему, что содержится в этой политике (это зависит от юрисдикции). Мы рекомендуем иметь представление о местных законах и о том, какие данные о вас они позволяют собирать провайдеру.

Мы рекомендуем искать конкретные термины, такие как "сбор данных", "анализ данных", "cookies", "реклама" или "сторонние" услуги. Иногда вы можете отказаться от сбора данных или от обмена информацией, но лучше всего выбирать сервис, который с самого начала уважает вашу конфиденциальность.

Помните, что вы также доверяете компании или организации и уверены, что они будут соблюдать собственную политику конфиденциальности.

## Методы аутентификации

Обычно существует несколько способов регистрации аккаунтов, каждый из которых имеет свои преимущества и недостатки.

### Электронная почта и пароль

Самый распространенный способ создания новой учетной записи - это адрес электронной почты и пароль. При использовании этого метода следует использовать менеджер паролей и следовать [лучшим практикам](passwords-overview.md) при выборе паролей.

!!! tip "Совет"

    Вы можете использовать свой менеджер паролей также и для организации других методов аутентификации! Просто добавьте новую запись и заполните соответствующие поля, вы можете добавить примечания для таких вещей, как вопросы безопасности или резервный код.

Вы будете ответственны за управление своими данными для входа в систему. Для дополнительной безопасности вы можете настроить [МФА](multi-factor-authentication.md) в своих аккаунтах.

[Рекомендуемые менеджеры паролей](../passwords.md ""){.md-button}

#### Псевдонимы электронной почты

If you don't want to give your real email address to a service, you have the option to use an alias. We described them in more detail on our email services recommendation page. Essentially, alias services allow you to generate new email addresses that forward all emails to your main address. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign up process. Those can be filtered automatically based on the alias they are sent to.

Should a service get hacked, you might start receiving phishing or spam emails to the address you used to sign up. Using unique aliases for each service can assist in identifying exactly what service was hacked.

[Рекомендуемые провайдеры псевдонимов электронной почты](../email.md#email-aliasing-services ""){.md-button}

### "Войти с помощью..." (OAuth)

OAuth is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Whenever you see something along the lines of "Sign in with *provider name*" on a registration form, it's typically using OAuth.

When you sign in with OAuth, it will open a login page with the provider you choose, and your existing account and new account will be connected. Your password won't be shared, but some basic information typically will (you can review it during the login request). This process is needed every time you want to log in to the same account.

Основными преимуществами являются:

- **Безопасность**: нет риска быть подверженным [утечке данных](https://en.wikipedia.org/wiki/Data_breach), поскольку сайт не хранит ваши учетные данные.
- **Простота использования**: управление несколькими учетными записями осуществляется с помощью одного логина.

Но есть и недостатки:

- **Конфиденциальность**: провайдер OAuth, с помощью которого вы входите в систему, будет знать, какими услугами вы пользуетесь.
- **Централизация**: если учетная запись, которую вы используете для OAuth, скомпрометирована или вы не можете войти в нее, все остальные учетные записи, подключенные к ней, будут также недоступны.

Аутентификация OAuth может быть особенно полезна в тех ситуациях, когда вы можете выиграть от более тесной интеграции между сервисами. Наша рекомендация - ограничить использование OAuth только там, где это необходимо, и всегда защищать основной аккаунт с помощью [МФА](multi-factor-authentication.md).

Все сервисы, использующие OAuth, будут безопасны настолько, насколько безопасна ваша основная учетная запись. Например, если вы хотите защитить учетную запись аппаратным ключом, но сервис не поддерживает аппаратные ключи, вы можете защитить учетную запись, используемую с помощью OAuth, аппаратным ключом, и теперь у вас есть аппаратная МФА для всех ваших учетных записей. Однако стоит отметить, что слабая аутентификация в учетной записи поставщика OAuth означает, что любая учетная запись, привязанная к этому логину, также будет слабой.

### Номер телефона

We recommend avoiding services that require a phone number for sign up. A phone number can identity you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

You should avoid giving out your real phone number if you can. Some services will allow the use of VOIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

In many cases you will need to provide a number that you can receive SMS or calls from, particularly when shopping internationally, in case there is a problem with your order at border screening. It's common for services to use your number as a verification method; don't let yourself get locked out of an important account because you wanted to be clever and give a fake number!

### Имя пользователя и пароль

Some services allow you to register without using an email address and only require you to set a username and password. These services may provide increased anonymity when combined with a VPN or Tor. Keep in mind that for these accounts there will most likely be **no way to recover your account** in the event you forget your username or password.
