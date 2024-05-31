---
title: "Autenticadores de Múltiples Factores"
icon: 'material/two-factor-authentication'
description: Estas herramientas te ayudan a proteger tus cuentas de Internet con la autenticación multifactor sin enviar tus secretos a terceros.
cover: multi-factor-authentication.webp
---

## Llaves de Seguridad

### YubiKey

<div class="admonition recommendation" markdown>

![YubiKeys](assets/img/multi-factor-authentication/yubikey.png)

Las **YubiKeys** están entre las llaves de seguridad más populares. Algunos modelos de YubiKey tienen una amplia gama de características, como: autenticación [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 y WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP), [TOTP y HOTP](https://developers.yubico.com/OATH).

Una de las ventajas de la YubiKey es que una llave puede hacer casi todo (YubiKey 5) lo que se podría esperar de una llave de seguridad. Te animamos a que hagas el [cuestionario](https://yubico.com/quiz) antes de comprar para asegurarte de que tomas la decisión correcta.

[:octicons-home-16: Página Principal](https://yubico.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentación}

</details>

</div>

La [tabla de comparación](https://yubico.com/store/compare) muestra las características y cómo se comparan las YubiKeys. Le recomendamos que seleccione las llaves de las YubiKey 5 Series.

Las YubiKeys se pueden programar utilizando [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) o [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). Para gestionar los códigos TOTP, puedes utilizar [Yubico Authenticator](https://yubico.com/products/yubico-authenticator). Todos los clientes de Yubico son de código abierto.

Para los modelos que soportan HOTP y TOTP, hay 2 ranuras en la interfaz OTP que pueden utilizarse para HOTP y 32 ranuras para almacenar secretos TOTP. Estos secretos se almacenan cifrados en la llave y nunca se exponen a los dispositivos a los que se conectan. Una vez que se ha proporcionado una semilla (secreto compartido) a Yubico Authenticator, éste sólo proporcionará los códigos de seis dígitos, pero nunca la semilla. Este modelo de seguridad ayuda a limitar lo que un atacante puede hacer si compromete uno de los dispositivos que ejecutan Yubico Authenticator y hace que la YubiKey sea resistente a un atacante físico.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El firmware de YubiKey no es de código abierto y no se puede actualizar. Si desea características en versiones de firmware más nuevas, o si hay una vulnerabilidad en la versión de firmware que está utilizando, tendría que comprar una nueva llave.

</div>

### Nitrokey

<div class="admonition recommendation" markdown>

![Nitrokey](assets/img/multi-factor-authentication/nitrokey.jpg){ align=right }

**Nitrokey** tiene una clave de seguridad capaz de [FIDO2 y WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) llamada **Nitrokey FIDO2**. Para obtener compatibilidad con PGP, deberá adquirir una de sus otras llaves, como la **Nitrokey Start**, la **Nitrokey Pro 2** o la **Nitrokey Storage 2**.

[:octicons-home-16: Página Principal](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title=Documentación}

</details>

</div>

La [tabla de comparación](https://nitrokey.com/#comparison) muestra las características y cómo se comparan los modelos de las Nitrokey. La **Nitrokey 3** listada tendrá un conjunto de características combinadas.

Los modelos de Nitrokey se pueden configurar usando la [aplicación de Nitrokey](https://nitrokey.com/download).

Para los modelos que admiten HOTP y TOTP, hay 3 ranuras para HOTP y 15 para TOTP. Algunas Nitrokeys pueden actuar como administrador de contraseñas. Pueden almacenar 16 credenciales diferentes y cifrarlas utilizando la misma contraseña que la interfaz OpenPGP.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Aunque las Nitrokeys no revelan los secretos HOTP/TOTP al dispositivo al que están conectadas, el almacenamiento HOTP y TOTP **no** está cifrado y es vulnerable a ataques físicos. Si desea almacenar secretos HOTP o TOTP, le recomendamos encarecidamente que utilice una YubiKey en su lugar.

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El restablecimiento de la interfaz OpenPGP en una Nitrokey también hará la base de datos de contraseñas [inaccessible](https://docs.nitrokey.com/pro/linux/factory-reset).

</div>

La Nitrokey Pro 2, la Nitrokey Storage 2 y la próxima Nitrokey 3 admiten la verificación de la integridad del sistema para portátiles con el firmware [Coreboot](https://coreboot.org) + [Heads](https://osresearch.net).

El firmware de Nitrokey es de código abierto, a diferencia del de YubiKey. El firmware de los modelos NitroKey modernos (excepto el de la **NitroKey Pro 2**) se puede actualizar.

### Criterios

**Por favor, tenga en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de decidir utilizar un proyecto y realizar su propia investigación para asegurarse de que es la elección ideal para usted.

#### Requisitos Mínimos

- Debe utilizar módulos de seguridad de hardware de alta calidad y resistentes a la manipulación.
- Debe ser compatible con la última especificación FIDO2.
- No debe permitir la extracción de claves privadas.
- Los dispositivos que cuesten más de 35$ deben soportar el manejo de OpenPGP y S/MIME.

#### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Debe estar disponible en formato USB-C.
- Debe estar disponible con NFC.
- Debe soportar el almacenamiento de secretos TOTP.
- Debe soportar actualizaciones seguras de firmware.

## Aplicaciones de Autenticación

Las Aplicaciones de Autenticación implementan un estándar de seguridad adoptado por el Grupo de Trabajo de Ingeniería de Internet (IETF) llamado **Contraseñas de un solo uso basadas en el tiempo** o **TOTP**. Se trata de un método en el que los sitios web comparten un secreto con usted que es utilizado por su aplicación de autenticación para generar un código de seis dígitos (normalmente) basado en la hora actual, que introduce al iniciar sesión para que el sitio web lo compruebe. Normalmente, estos códigos se regeneran cada 30 segundos, y una vez que se genera uno nuevo, el anterior queda inutilizado. Incluso si un pirata informático consigue un código de seis dígitos, no hay forma de que invierta ese código para obtener el secreto original ni de que pueda predecir cuáles serán los códigos futuros.

Recomendamos encarecidamente que utilice aplicaciones TOTP para móviles en lugar de alternativas de escritorio, ya que Android e iOS tienen mejor seguridad y aislamiento de aplicaciones que la mayoría de los sistemas operativos de escritorio.

### Ente Auth

<div class="admonition recommendation" markdown>

![Ente Auth logo](assets/img/multi-factor-authentication/ente-auth.png){ align=right }

**Ente Auth** is a free and open-source app which stores and generates TOTP tokens. Esta permite utilizar una cuenta en línea para realizar copias de seguridad y sincronizar sus tokens entre sus dispositivos (y accesarlos por medio de una interfaz web) de una manera secura y cifrada de extremo a extremo. También se puede utilizar sin conexión a Internet en un único dispositivo sin la necesidad de una cuenta.

[:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.ente.io/auth){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

### Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** es una aplicación gratuita y de código abierto para gestionar sus tokens para la verificación de 2 pasos de sus servicios en línea. Aegis Authenticator funciona completamente sin conexión/localmente, pero incluye una opción para exportar sus tokens para respaldarlos, a diferencia de otras alternativas.

[:octicons-home-16: Página Principal](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

<!-- markdownlint-disable-next-line -->
### Criterios

**Por favor, tenga en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de decidir utilizar un proyecto y realizar su propia investigación para asegurarse de que es la elección ideal para usted.

- El código fuente debe estar a disposición del público.
- No debe requerir conexión a Internet.
- No debe sincronizarse con un servicio de sincronización/copia de seguridad en la nube de terceros.
    - Es aceptable el soporte de sincronización E2EE** Opcional** con herramientas nativas del sistema operativo, por ejemplo, sincronización cifrada a través de iCloud.
