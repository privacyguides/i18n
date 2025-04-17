---
meta_title: "Cómo Crear Cuentas de Internet Privadas - Privacy Guides"
title: "Creación de Cuenta"
icon: 'material/account-plus'
description: Crear cuentas en línea es prácticamente una necesidad en Internet, sigue estos pasos para asegurarte de mantener tu privacidad.
---

A menudo la gente se inscribe en servicios sin pensar. Maybe it's a streaming service to watch that new show everyone's talking about, or an account that gives you a discount for your favorite fast food place. Sea cual sea el caso, debes tener en cuenta las implicaciones que tednrá para tus datos ahora y más adelante.

Hay riesgos asociados con cada nuevo servicio que utilices. Las filtraciones de datos, la revelación de información de clientes a terceros o el acceso a datos por parte de empleados deshonestos son posibilidades que deben tenerse en cuenta a la hora de facilitar tu información. Tienes que estar seguro de que puedes confiar en el servicio, por eso no recomendamos almacenar datos valiosos en nada, excepto en los productos más maduros y que han sido puestos profundamente a prueba. Por lo general, se trata de servicios que ofrecen E2EE y han sido sometidos a una auditoría criptográfica. Una auditoría aumenta las garantías de que el producto se diseñó sin problemas de seguridad notorios causados por un desarrollador inexperto.

También puede ser difícil eliminar las cuentas en algunos servicios. En ocasiones, [sobrescribir los datos](account-deletion.md#overwriting-account-information) asociados a una cuenta puede ser posible, pero en otros casos el servicio guardará un historial completo de los cambios realizados en la cuenta.

## Términos del servicio y Política de privacidad

Los ToS (Términos del Servicio) son las normas que usted se compromete a respetar al utilizar el servicio. En los servicios más grandes, estas normas suelen aplicarse mediante sistemas automatizados. A veces, estos sistemas automatizados pueden cometer errores. For example, you may be banned or locked out of your account on some services for using a VPN or VoIP number. Recurrir estos bloqueos suele ser difícil, y además implica un proceso automatizado que no siempre funciona bien. Esta es una de las razones por las que no sugerimos utilizar Gmail para el correo electrónico, por ejemplo. El correo electrónico es crucial para acceder a otros servicios a los que estés inscrito.

The Privacy Policy is how the service says they will use your data, and it is worth reading so that you understand how your data will be used. Una empresa u organización puede no estar legalmente obligada a seguir todo lo que contiene la política (depende de la jurisdicción). Te recomendamos que tengas una idea de cuál es tu legislación local y qué le permite recopilar a un proveedor.

Te recomendamos que busques términos concretos como "recopilación de datos", "análisis de datos", "cookies", "anuncios" o servicios de "terceros". Sometimes you will be able to opt out from data collection or from sharing your data, but it is best to choose a service that respects your privacy from the start.

Ten en cuenta que también estás depositando tu confianza en la empresa u organización y en que cumplirán su propia política de privacidad.

## Métodos de autenticación

Usualmente hay varias maneras para registrarse, cada una tiene sus propias ventajas y desventajas.

### Correo electrónico y contraseña

La manera más común de crear una nueva cuenta es utilizando una dirección de correo electrónico y una contraseña. Cuando se utiliza este método, se debe utilizar un gestor de contraseñas y seguir las [mejores prácticas](passwords-overview.md) respecto a las contraseñas.

<div class="admonition tip" markdown>
<p class="admonition-title">Consejo</p>

¡También puedes usar un gestor de contraseñas para organizar otros métodos de autenticación! Solo añade la nueva entrada y completa los espacios apropiados, puedes agregar notas para cosas como las preguntas de seguridad o una llave de respaldo.

</div>

Usted es responsable de gestionar sus credenciales de ingreso. Para mayor seguridad, se puede configurar la [autenticación multifactor](multi-factor-authentication.md) en las cuentas.

[Gestores de contraseñas recomendados](../passwords.md ""){.md-button}

#### Alias de correo electrónico

Si no se quiere utilizar una dirección real de correo electrónico en un servicio, se cuenta con la opción de utilizar un alias. We describe them in more detail on our email services recommendation page. Básicamente, los servicios de alias permiten generar nuevas direcciones de correo que reenvían todos los correos a la dirección principal. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign-up process. Estos pueden ser filtrados automáticamente basándose en el alias al que son enviados.

Si un servicio es hackeado, puede que usted comience a recibir correos engañosos o basura en la dirección que utilizó para registrarse. Al utilizar un único alias para cada servicio, se puede identificar cual servicio fue hackeado.

[Servicios recomendados de alias de correo electrónico](../email-aliasing.md ""){.md-button}

### "Iniciar sesión con..." (OAuth)

[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth) is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Cuando veas algo parecido a "Iniciar sesión con *nombre del proveedor*" en un formulario de registro, normalmente está utilizando OAuth.

Cuando inicies sesión con OAuth, se abrirá una página de inicio de sesión con el proveedor que elijas, y tu cuenta existente y la nueva estarán conectadas. Tu contraseña no se compartirá, pero sí algunos datos básicos (puedes revisarlos durante la solicitud de acceso). Este proceso es necesario cada vez que quieres iniciar sesión en la misma cuenta.

Las principales ventajas son:

- **Security**: You don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials because they are stored with the external OAuth provider. Common OAuth providers like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease-of-use**: Multiple accounts are managed by a single login.

Pero hay desventajas:

- **Privacy**: The OAuth provider you log in with will know the services you use.
- **Centralization**: If the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth puede ser especialmente útil en aquellas situaciones en las que podrías beneficiarte de una integración más profunda entre servicios. Nuestra recomendación es limitar el uso de OAuth solamente donde lo necesites, y proteger siempre la cuenta principal con [MFA](multi-factor-authentication.md).

Todos los servicios que utilicen OAuth serán tan seguros como la cuenta de tu proveedor de OAuth subyacente. Por ejemplo, si quieres proteger una cuenta con una llave de hardware, pero ese servicio no admite llaves de hardware, puedes proteger la cuenta que utilizas con OAuth con una llave de hardware en su lugar, y ahora básicamente tienes MFA por hardware en todas tus cuentas. Vale la pena señalar, sin embargo, que una autenticación débil en su cuenta de proveedor de OAuth significa que cualquier cuenta vinculada a ese inicio de sesión también será débil.

Existe un peligro adicional cuando se utiliza *Iniciar sesión con Google*, *Facebook*, u otro servicio, y es que normalmente el proceso OAuth permite una compartición de datos *bidireccional*. Por ejemplo, iniciar sesión en un foro con tu cuenta de Twitter podría conceder a ese foro acceso para hacer cosas en tu cuenta de Twitter como publicar, leer tus mensajes o acceder a otros datos personales. Los proveedores de OAuth normalmente te presentarán una lista de cosas a las que estás concediendo acceso al servicio externo, y siempre debes asegurarte de que lees esa lista y no concedes inadvertidamente al servicio externo acceso a algo que no necesita.

Las aplicaciones maliciosas, especialmente en dispositivos móviles en los que la aplicación tiene acceso a la sesión WebView utilizada para iniciar sesión en el proveedor OAuth, también pueden abusar de este proceso secuestrando tu sesión con el proveedor OAuth y obteniendo acceso a tu cuenta OAuth a través de esos medios. El uso de la opción *Iniciar sesión con* con cualquier proveedor debe considerarse normalmente una cuestión de comodidad que solo se utiliza con servicios en los que se confía que no son activamente maliciosos.

### Número de teléfono

Recomendamos evitar los servicios que exigen un número de teléfono para darse de alta. Un número de teléfono puede identificarte a través de múltiples servicios y, dependiendo de los acuerdos de intercambio de datos, esto hará que tu uso sea más fácil de rastrear, especialmente si uno de esos servicios es violado, ya que el número de teléfono a menudo **no** está cifrado.

Si puedes, evita dar tu número de teléfono real. Some services will allow the use of VoIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

En muchos casos, tendrás que facilitar un número desde el que puedas recibir SMS o llamadas, sobre todo cuando hagas compras internacionales, por si hay algún problema con tu pedido en el control fronterizo. Es habitual que los servicios utilicen tu número como método de verificación; ¡no dejes que te bloqueen una cuenta importante por haber querido pasarte de listo y dar un número falso!

### Nombre de usuario y contraseña

Algunos servicios permiten registrarse sin utilizar una dirección de correo electrónico y sólo exigen que establezcas un nombre de usuario y una contraseña. Estos servicios pueden proporcionar un mayor anonimato cuando se combinan con una VPN o Tor. Ten en cuenta que para estas cuentas lo más probable es que no haya **ninguna forma de recuperar tu cuenta** en caso de que olvides tu nombre de usuario o contraseña.
