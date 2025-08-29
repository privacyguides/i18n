---
title: Configuración de las Directivas de Grupo
description: Una guía rápida para configurar las Directivas de Grupo para que Windows respete un poco más la privacidad.
---

Aparte de modificar el propio registro, el **Editor de Directivas de Grupo Local** es la forma más potente de cambiar muchos aspectos del sistema sin necesidad de instalar herramientas de terceros. Para cambiar estos ajustes se requiere la [Edición Pro](index.md#windows-editions) o superior.

Estos ajustes deben establecerse en una instalación de Windows completamente nueva. Configurarlos en tu instalación existente debería funcionar, pero podría introducir comportamientos impredecibles y lo haces bajo tu propia responsabilidad.

Todas estas configuraciones tienen una explicación adjunta en el Editor de Directivas de Grupo que explica exactamente lo que hacen, normalmente con gran detalle. Por favor, presta atención a esas descripciones cuando hagas cambios, para que sepas exactamente lo que estamos recomendando aquí. También hemos explicado algunas de nuestras opciones aquí siempre que la explicación incluida con Windows sea inadecuada.

## Plantillas Administrativas

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

A pesar de los nombres de estas directivas, esto no _requiere_ que hagas nada por defecto, pero desbloqueará la _opción_ de tener una configuración más compleja (como requerir un PIN al inicio además del TPM) en el asistente de configuración de BitLocker.

#### Contenido de la Nube

- Desactivar el Contenido Optimizado en la Nube: **Habilitada**
- Desactivar el Contenido de Estado de Cuentas de Consumidor en la nube: **Habilitada**
- No Mostrar Recomendaciones de Windows: **Habilitada**
- Desactivar Experiencias del Consumidor de Microsoft: **Habilitada**

#### Interfaz de Usuario de Credenciales

- Requerir Ruta de Acceso de Confianza para la Entrada de Credenciales: **Habilitada**
- Impedir el Uso de Preguntas de Seguridad en las Cuentas Locales: **Habilitada**

#### Recopilación de Datos y Versiones Preliminares

- Permitir Datos de Diagnóstico: **Habilitada**
  - Opciones: **Enviar Datos de Diagnóstico Necesarios** (Edición Pro); o
  - Opciones: **Datos de Diagnóstico Desactivados** (Edición Enterprise o Education)
- Limitar Recopilación de Registros de Diagnóstico: **Habilitada**
- Limitarn Recopilación de Volcados: **Habilitada**
- Limitar los Datos de Diagnóstico Opcionales para el Análisis de Escritorio: **Habilitada**
  - Opciones: **Desactivar la Colección de Análisis de Escritorio**
- No Volver a Mostrar Notificaciones de Comentarios: **Habilitada**

#### Explorador de Archivos

- Desactivar la Información Basada en Cuentas, los Archivos Recientes, Favoritos y Recomendados en Explorador de Archivos: **Habilitada**

#### MDM

- Deshabilitar la Inscripción de MDM: **Habilitada**

#### OneDrive

- Guardar Documentos en OneDrive de Forma Predeterminada: **Deshabilitada**
- Impedir que se Está Generando el Tráfico de Red Hasta que el Usuario Inicia Sesión en OneDrive OneDrive: **Habilitada**
- Impedir el Uso de OneDrive para Almacenar Archivos: **Habilitada**

Este último ajuste desactiva OneDrive en tu sistema; asegúrate de cambiarlo a **Deshabilitada** si utilizas OneDrive.

#### Insertar para Instalar

- Desactivar el Servicio Inesrtar para Instalar: **Habilitada**

#### Buscar

- Permitir el Uso de Cortana: **Deshabilitada**
- No buscar en Internet o Mostrar Resultados de Internet en Search: **Habilitada**
- Definir Qué Información se Comparte en Search: **Habilitada**
  - Tipo de información: **Información anónima**

#### Sincronizar la Configuración

- No Sincronizar: **Habilitada**

#### Entrada de Texto

- Mejorar el Reconocimiento de la Escritura y la Entrada Manuscrita: **Deshabilitada**

#### Informes de Errores de Windows

- No Enviar Datos Adicionales: **Habilitada**
- Consentimiento > Configurar Consentimiento Predeterminado: **Habilitada**
  - Nivel de consentimiento: **Preguntar siempre antes de enviar datos**
