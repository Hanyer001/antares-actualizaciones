# Antares — Distribución y actualizaciones

Repositorio oficial de distribución de **Antares para Windows y Android**. Su finalidad es alojar los instaladores y los archivos que utiliza la aplicación para comprobar y descargar nuevas versiones.

El código fuente de la aplicación se mantiene en el [repositorio Antares](https://github.com/Hanyer001/Antares). Este repositorio corresponde al canal de distribución, cuya disponibilidad pública permite acceder a las descargas sin una cuenta de GitHub.

## Descarga oficial

**[Consultar y descargar la última versión estable](https://github.com/Hanyer001/antares-actualizaciones/releases/latest)**

Cada publicación incluye las notas de la versión y los archivos necesarios para su instalación. Las versiones anteriores permanecen disponibles en el [historial de publicaciones](https://github.com/Hanyer001/antares-actualizaciones/releases).

### Versión 0.3.3

La versión estable **0.3.3** incorpora listas de Spotify de más de 100 canciones, álbumes completos en orden y una vista de artista compacta: cinco principales con continuación habitual y el botón **Solo este artista** para su catálogo en la cola. El instalador ocupa 25,7 MB (25,656,066 bytes).

### Android 0.3.3 Beta 1

[Descargar Antares para Android](https://github.com/Hanyer001/antares-actualizaciones/releases/download/android-v0.3.3-beta.1/Antares-Android.apk) · [Notas e instalación](https://github.com/Hanyer001/antares-actualizaciones/releases/tag/android-v0.3.3-beta.1). Android 7.0+, ARM de 32 y 64 bits. Paquete público `com.hanyer.antares`, firmado con la clave privada de distribución. Las próximas versiones públicas conservan identificador y firma; se instalan encima sin desinstalar.

Preview puede coexistir. Exporta una copia completa desde Ajustes → Tus datos en Preview y restáurala en Antares para migrar la biblioteca.

La release Android está marcada **Pre-release** y no reemplaza la última estable de Windows. `android-latest.json` es un manifiesto separado, preparado para un futuro aviso dentro de Android; la app todavía no lo consulta. El `latest.json` de Windows no cambia.


**[Descargar Antares 0.3.3](https://github.com/Hanyer001/antares-actualizaciones/releases/download/v0.3.3/Antares-Setup.exe)** · [Notas y archivos de esta versión](https://github.com/Hanyer001/antares-actualizaciones/releases/tag/v0.3.3)

### Requisitos

- Windows 10 o Windows 11 de 64 bits.
- Conexión a Internet para comprobar y descargar actualizaciones.

La instalación se realiza para el usuario actual y no requiere permisos de administrador.

## Instalación y actualización manual

1. Acceda a la última versión estable mediante el enlace de descarga oficial.
2. En la sección **Assets**, descargue `Antares-Setup.exe` o `Antares_<versión>_x64-setup.exe`. Ambos contienen el mismo instalador.
3. Ejecute el instalador y siga sus instrucciones.

Para actualizar una instalación existente, ejecute el nuevo instalador sobre la versión anterior, sin desinstalarla previamente. La biblioteca, las listas, el historial y las preferencias se almacenan fuera de la carpeta de instalación y se conservan durante la actualización.

Como respaldo adicional, la aplicación permite exportar una copia completa desde **Ajustes → Tus datos**.

## Actualizaciones desde la aplicación

El actualizador integrado está disponible desde **Antares 0.3.0**. Cuando la opción **Ajustes → Sistema → Avisar de versiones nuevas** está activada, la aplicación consulta este canal:

- Al iniciar Antares.
- Cada seis horas mientras la aplicación permanece abierta.

También es posible realizar una comprobación manual mediante **Buscar versión nueva**.

Si existe una versión superior a la instalada, Antares muestra un aviso. La descarga y la instalación requieren la confirmación del usuario. Antes de instalar el paquete, la aplicación verifica su firma y, al completar la actualización, se reinicia.

Los avisos se muestran al comprobar el canal; no se envían con la aplicación cerrada. Una instalación anterior que no incluya el actualizador debe actualizarse manualmente una vez para recibir las siguientes versiones desde la aplicación.

## Archivos de cada publicación

| Archivo | Finalidad |
| --- | --- |
| `Antares_<versión>_x64-setup.exe` | Instalador de Antares para Windows de 64 bits. Se utiliza tanto para nuevas instalaciones como para actualizaciones manuales. |
| `Antares-Setup.exe` | Copia idéntica con nombre fijo para el enlace de descarga de la página. |
| `latest.json` | Manifiesto que consulta el actualizador. Contiene la versión, las notas, la dirección del instalador y su firma de verificación. |

Para instalar Antares solo es necesario descargar el archivo `.exe`. El manifiesto `latest.json` está destinado al uso de la aplicación y no requiere intervención del usuario.

## Verificación y seguridad

Antares comprueba la firma del instalador con la clave pública incorporada en la aplicación. Esta comprobación permite detectar modificaciones del paquete y verificar que fue firmado con la clave correspondiente.

La firma incluida en `latest.json` es pública y puede distribuirse junto con el instalador. **La clave privada de firma, sus contraseñas y las credenciales de GitHub no deben publicarse en este repositorio ni adjuntarse a una versión.**

Esta verificación corresponde al sistema de actualizaciones de Antares; no equivale a un certificado de firma de código de Windows.

## Publicación de nuevas versiones

La persona responsable de una publicación debe:

1. Actualizar el número de versión de la aplicación y comprobar los cambios.
2. Generar el instalador y su manifiesto utilizando la clave de firma correspondiente al canal existente.
3. Crear una publicación con la etiqueta `vX.Y.Z` y describir los cambios de la versión.
4. Adjuntar `Antares_<versión>_x64-setup.exe`, su copia `Antares-Setup.exe` y el archivo `latest.json` generado para ese mismo paquete.
5. Publicar la versión como estable y marcarla como **Latest**.
6. Comprobar que el manifiesto y el instalador pueden descargarse desde sus direcciones públicas.

El manifiesto debe indicar una versión superior a la instalada y apuntar al instalador correcto. Las publicaciones en borrador o marcadas como **Pre-release** no deben utilizarse para distribuir actualizaciones del canal estable.

Subir cambios al repositorio del código fuente no distribuye una actualización. Para que los usuarios puedan recibirla, es necesario publicar el instalador firmado y su manifiesto en este canal.

Consulte la [guía de publicación](https://github.com/Hanyer001/Antares/blob/main/docs/releases.md) para conocer el procedimiento de preparación de los archivos.

## Documentación y soporte

- [Sitio web de Antares](https://hanyer001.github.io/Pagina-Antares/)
- [Código fuente y documentación](https://github.com/Hanyer001/Antares)
- [Reportar un problema](https://github.com/Hanyer001/Antares/issues)

Al informar un problema de instalación o actualización, indique la versión de Antares, la versión de Windows y el mensaje de error, si existe. Omita contraseñas, tokens y cualquier otra información privada.
