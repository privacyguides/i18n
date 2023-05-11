---
meta_title: "Cómo Crear Cuentas de Internet Privadas - Privacy Guides"
title: "Creación de cuenta"
icon: 'material/account-plus'
description: Crear cuentas en línea es prácticamente una necesidad en Internet, sigue estos pasos para asegurarte de mantener tu privacidad.
---

A menudo la gente se inscribe en servicios sin pensar. Tal vez sea un servicio de streaming para que puedas ver ese nuevo show del que todo el mundo habla, o una cuenta que te da un descuento para tu lugar de comida rápida favorito. Sea cual sea el caso, debes tener en cuenta las implicaciones que tednrá para tus datos ahora y más adelante.

Hay riesgos asociados con cada nuevo servicio que utilices. Las filtraciones de datos, la revelación de información de clientes a terceros o el acceso a datos por parte de empleados deshonestos son posibilidades que deben tenerse en cuenta a la hora de facilitar tu información. Tienes que estar seguro de que puedes confiar en el servicio, por eso no recomendamos almacenar datos valiosos en nada, excepto en los productos más maduros y que han sido puestos profundamente a prueba. Por lo general, se trata de servicios que ofrecen E2EE y han sido sometidos a una auditoría criptográfica. Una auditoría aumenta las garantías de que el producto se diseñó sin problemas de seguridad notorios causados por un desarrollador inexperto.

También puede ser difícil eliminar las cuentas en algunos servicios. En ocasiones, [sobrescribir los datos](account-deletion.md#overwriting-account-information) asociados a una cuenta puede ser posible, pero en otros casos el servicio guardará un historial completo de los cambios realizados en la cuenta.

## Términos del servicio y Política de privacidad

Los ToS (Términos del Servicio) son las normas que usted se compromete a respetar al utilizar el servicio. En los servicios más grandes, estas normas suelen aplicarse mediante sistemas automatizados. A veces, estos sistemas automatizados pueden cometer errores. Por ejemplo, pueden expulsarte o bloquearte la cuenta en algunos servicios por utilizar una VPN o un número VOIP. Recurrir estos bloqueos suele ser difícil, y además implica un proceso automatizado que no siempre funciona bien. Esta es una de las razones por las que no sugerimos utilizar Gmail para el correo electrónico, por ejemplo. El correo electrónico es crucial para acceder a otros servicios a los que estés inscrito.

La Política de Privacidad es la forma en que el servicio dice que utilizará tus datos y vale la pena leerla para que entiendas cómo se utilizarán tus datos. Una empresa u organización puede no estar legalmente obligada a seguir todo lo que contiene la política (depende de la jurisdicción). Te recomendamos que tengas una idea de cuál es tu legislación local y qué le permite recopilar a un proveedor.

Te recomendamos que busques términos concretos como "recopilación de datos", "análisis de datos", "cookies", "anuncios" o servicios de "terceros". A veces podrás optar por no participar en la recopilación de datos o no compartirlos, pero lo mejor es elegir un servicio que respete tu privacidad desde el principio.

Ten en cuenta que también estás depositando tu confianza en la empresa u organización y en que cumplirán su propia política de privacidad.

## Métodos de autenticación

Usualmente hay varias maneras para registrarse, cada una tiene sus propias ventajas y desventajas.

### Correo electrónico y contraseña

La manera más común de crear una nueva cuenta es utilizando una dirección de correo electrónico y una contraseña. Cuando se utiliza este método, se debe utilizar un gestor de contraseñas y seguir las [mejores prácticas](passwords-overview.md) respecto a las contraseñas.

!!! tip "Consejo"

    ¡También puedes usar un gestor de contraseñas para organizar otros métodos de autenticación! Solo añade la nueva entrada y completa los espacios apropiados, puedes agregar notas para cosas como las preguntas de seguridad o una llave de respaldo.

Usted es responsable de gestionar sus credenciales de ingreso. Para mayor seguridad, se puede configurar la [autenticación multifactor](multi-factor-authentication.md) en las cuentas.

[Gestores de contraseñas recomendados](../passwords.md ""){.md-button}

#### Alias de correo electrónico

Si no se quiere utilizar una dirección real de correo electrónico en un servicio, se cuenta con la opción de utilizar un alias. Estos los describimos con mayores detalles en nuestra página con recomendaciones de servicios de correo electrónico. Básicamente, los servicios de alias permiten generar nuevas direcciones de correo que reenvían todos los correos a la dirección principal. Esto puede ayudar a prevenir el rastreo a través de múltiples servicios y ayudar a gestionar los correos de mercadeo que algunas veces vienen con el proceso de registro. Estos pueden ser filtrados automáticamente basándose en el alias al que son enviados.

Si un servicio es hackeado, puede que usted comience a recibir correos engañosos o basura en la dirección que utilizó para registrarse. Al utilizar un único alias para cada servicio, se puede identificar cual servicio fue hackeado.

[Servicios recomendados de alias de correo electrónico](../email.md#email-aliasing-services ""){.md-button}

### "Iniciar sesión con..." (OAuth)

OAuth es un protocolo de autenticación que te permite registrarte en un servicio sin compartir mucha información con el proveedor del servicio, o incluso nada de información, utilizando en su lugar una cuenta existente que tengas con otro servicio. Cuando veas algo parecido a "Iniciar sesión con *nombre del proveedor*" en un formulario de registro, normalmente está utilizando OAuth.

Cuando inicies sesión con OAuth, se abrirá una página de inicio de sesión con el proveedor que elijas, y tu cuenta existente y la nueva estarán conectadas. Tu contraseña no se compartirá, pero sí algunos datos básicos (puedes revisarlos durante la solicitud de acceso). Este proceso es necesario cada vez que quieres iniciar sesión en la misma cuenta.

Las principales ventajas son:

- **Seguridad**: no hay riesgo de verse implicado en una [violación de datos ](https://en.wikipedia.org/wiki/Data_breach) porque el sitio web no almacena tus credenciales.
- **Facilidad de uso**: varias cuentas se gestionan con un solo inicio de sesión.

Pero hay desventajas:

- **Privacidad**: el proveedor de OAuth con el que te conectes sabrá los servicios que utilizas.
- **Centralización**: si la cuenta que utilizas para OAuth se ve comprometida o no puedes iniciar sesión en ella, todas las demás cuentas conectadas a ella se verán afectadas.

La autenticación OAuth puede ser especialmente útil en situaciones en las que podrías beneficiarte de una integración más profunda entre servicios. Nuestra recomendación es limitar el uso de OAuth solamente donde lo necesites, y proteger siempre la cuenta principal con [MFA](multi-factor-authentication.md).

Todos los servicios que utilicen OAuth serán tan seguros como la cuenta de tu proveedor subyacente. Por ejemplo, si quieres proteger una cuenta con una llave de hardware, pero ese servicio no admite llaves de hardware, puedes proteger la cuenta que utilizas con OAuth con una llave de hardware en su lugar, y ahora básicamente tienes MFA por hardware en todas tus cuentas. Vale la pena señalar, sin embargo, que una autenticación débil en su cuenta de proveedor de OAuth significa que cualquier cuenta vinculada a ese inicio de sesión también será débil.

### Número de teléfono

Recomendamos evitar los servicios que exigen un número de teléfono para darse de alta. Un número de teléfono puede identificarte en múltiples servicios y, dependiendo de los acuerdos de intercambio de datos, esto hará que su uso sea más fácil de rastrear, sobre todo si uno de esos servicios es violado, ya que el número de teléfono **no** suele estar encriptado.

Si puedes, evita dar tu número de teléfono real. Algunos servicios permiten el uso de números VOIP, pero a menudo activan los sistemas de detección de fraude y provocan el bloqueo de la cuenta, por lo que no lo recomendamos para cuentas importantes.

En muchos casos, tendrás que facilitar un número desde el que puedas recibir SMS o llamadas, sobre todo cuando hagas compras internacionales, por si hay algún problema con tu pedido en el control fronterizo. Es habitual que los servicios utilicen tu número como método de verificación; ¡no dejes que te bloqueen una cuenta importante por haber querido pasarte de listo y dar un número falso!

### Nombre de usuario y contraseña

Algunos servicios permiten registrarse sin utilizar una dirección de correo electrónico y sólo exigen que establezcas un nombre de usuario y una contraseña. Estos servicios pueden proporcionar un mayor anonimato cuando se combinan con una VPN o Tor. Ten en cuenta que para estas cuentas lo más probable es que no haya **ninguna forma de recuperar tu cuenta** en caso de que olvides tu nombre de usuario o contraseña.
