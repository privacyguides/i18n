---
title: Configuración de las Directivas de Grupo
description: Una guía rápida para configurar las Directivas de Grupo para que Windows respete un poco más la privacidad.
---

Aparte de modificar el propio registro, el **Editor de Directivas de Grupo Local** es la forma más potente de cambiar muchos aspectos del sistema sin instalar herramientas de terceros. Para cambiar estos ajustes se requiere la [Edición Pro](index.md#windows-editions) o superior.

Estos ajustes deben establecerse en una nueva instalación de Windows. Configurarlos en tu instalación existente debería funcionar, pero puede introducir un comportamiento impredecible y lo haces bajo tu propio riesgo.

Todas estas configuraciones tienen una explicación adjunta en el Editor de Directivas de Grupo que explica exactamente lo que hacen, normalmente con gran detalle. Por favor, presta atención a esas descripciones cuando hagas cambios, para que sepas exactamente lo que estamos recomendando aquí. También hemos explicado algunas de nuestras opciones aquí siempre que la explicación incluida con Windows sea inadecuada.

## Planitllas Administrativas

Puedes encontrar esta configuración abriendo `gpedit.msc` y navegando a **Directiva Equipo Local** > **Configuración del Equipo** > **Plantillas Administrativas** en la barra lateral izquierda. Los encabezados de esta página corresponden a carpetas/subcarpetas dentro de Plantillas Administrativas, y las viñetas corresponden a directivas individuales.

Para cambiar cualquier directiva de grupo, haz doble clic en ella y selecciona Habilitada o Deshabilitada en la parte superior de la ventana que aparece en función de las recomendaciones siguientes. Algunas directivas de grupo tienen parámetros adicionales que pueden configurarse, y si ese es el caso, los parámetros apropiados también se indican a continuación.

### Sistema

#### Device Guard

- Activar la Seguridad Basada en la Virtualización: \*_Habilitada_
  - Nivel de Seguridad de la Plataforma: **Arranque Seguro y Protección de DMA**
  - Configuración de Inicio Seguro: **Habilitada**

#### Administración de Comunicaciones de Internet

- Desactivar el Programa para la Mejora de la Experiencia del Usuario de Windows: **Habilitada**
- Desactivar el Informe de Errores de Windows: **Habilitada**
- Desactivar el Programa para la Mejora de la Experiencia del Usuario de Windows Messenger: **Habilitada**

Ten en cuenta que al deshabilitar el Programa para la Mejora de la Experiencia del Usuario de Windows también se deshabilitan algunas otras funciones de seguimiento que también se pueden controlar individualmente con la Directiva de Grupo. No las enumeramos todas aquí ni las desactivamos porque este ajuste lo cubre.

#### Directivas del Sistema Operativo

- Permitir el Historial del Portapapeles: **Deshabilitada**
- Permitir la Sincronización del Portapapeles entre Dispositivos: **Deshabilitada**
- Habilita la Fuente de Actividades: **Deshabilitada**
- Permitir la Publicación de las Actividades del Usuario: **Deshabilitada**
- Permitir la Carga de Actividades del Usuario: **Deshabilitada**

#### Perfiles de usuario

- Desactivar el Identificador de Publicidad: **Habilitada**

### Componentes de Windows

#### Directivas de Reproducción Automática

Reproducción Automática y Ejecución Automática son funciones que permiten a Windows ejecutar un script o realizar alguna otra tarea cuando un dispositivo está conectado, a veces evitando las medidas de seguridad que implican el consentimiento del usuario. Esto podría permitir a dispositivos no fiables ejecutar código malicioso sin tu conocimiento. Es una buena práctica de seguridad desactivar estas funciones y abrir los archivos de los discos externos manualmente.

- Desactivar Reproducción Automática: **Habilitada**
- Deshabilitar Reproducción Automática para Dispositivos que no son de Volumen: **Habilitada**
- Establece el Comportamiento Predeterminado para Ejecución Automática: **Habilitada**
  - Comportamiento Predeterminado de Ejecución Automática: **No Ejecutar Ningún Comando de Ejecución Automática**

#### Cifrado de Unidad BitLocker

Es posible que desees volver a cifrar la unidad del sistema operativo después de cambiar estos ajustes.

- Elija Método de Cifrado e Intensidad de Cifrado de Unidad (Windows Vista, Windows Server 2008, Windows 7): **Habilitada**
  - Seleccione el método de cifrado: **AES-256**

Establecer la intensidad de cifrado para la política de Windows 7 todavía aplica esa intensidad a las nuevas versiones de Windows.

##### Unidades del Sistema Operativo

- Requiere Autenticación Adicional al Iniciar: **Habilitada**
- Permitir los PIN Mejorados para el Inicio: **Habilitada**

A pesar de los nombres de estas directivas, esto no _requiere_ que hagas nada por defecto, pero desbloqueará la _opción_ de tener una configuración más compleja (como requerir un PIN al inicio además del TPM) en el asistente de configuración de Bitlocker.

#### Contenido de la Nube

- Desactivar el Contenido Optimizado en la Nube: **Habilitada**
- Desactivar el Contenido de Estado de Cuentas de Consumidor en la nube: **Habilitada**
- No Mostrar Recomendaciones de Windows: **Habilitada**
- Desactivar Experiencias del Consumidor de Microsoft: **Habilitada**

#### Interfaz de Usuario de Credenciales

- Requerir Ruta de Acceso de Confianza para la Entrada de Credenciales: **Habilitada**
- Impedir el Uso de Preguntas de Seguridad en las Cuentas Locales: **Habilitada**

#### Recopilación de Datos y Compilaciones Preliminares

- Permitir Telemetría: **Habilitada**
  - Opciones: **Requerido** (Edición Pro); o
  - Options: **Diagnostic data off** (Enterprise or Education Edition)
- Limit Diagnostic Log Collection: **Enabled**
- Limit Dump Collection: **Enabled**
- Limitar los Datos de Diagnóstico de Nivel Mejorado al Valor Mínimo Requerido por Windows Analytics: **Habilitada**
  - Opciones: **Deshabilitar la Recopilación de Análisis de Windows**
- No Volver a Mostrar Notificaciones de Comentarios: **Habilitada**

#### File Explorer

- Turn off account-based insights, recent, favorite, and recommended files in File Explorer: **Enabled**

#### MDM

- Disable MDM Enrollment: **Enabled**

#### OneDrive

- Save documents to OneDrive by default: **Disabled**
- Prevent OneDrive from generating network traffic until the user signs in to OneDrive: **Enabled**
- Prevent the usage of OneDrive for file storage: **Enabled**

This last setting disables OneDrive on your system; make sure to change it to **Disabled** if you use OneDrive.

#### Push To Install

- Turn off Push To Install service: **Enabled**

#### Buscar

- Allow Cortana: **Disabled**
- Don't search the web or display web results in Search: **Enabled**
- Set what information is shared in Search: **Enabled**
  - Type of information: **Anonymous info**

#### Sync your settings

- Do not sync: **Enabled**

#### Text input

- Improve inking and typing recognition: **Disabled**

#### Windows Error Reporting

- Do not send additional data: **Enabled**
- Consent > Configure Default consent: **Enabled**
  - Consent level: **Always ask before sending data**
