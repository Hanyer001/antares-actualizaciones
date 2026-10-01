# Antares · Actualizaciones

Canal de distribución de Antares para Windows. Aquí se publican los instaladores y el manifiesto que consulta el actualizador de la aplicación.

## Descargar e instalar

1. Abre la [última versión](https://github.com/Hanyer001/antares-actualizaciones/releases/latest).
2. Descarga el archivo `Antares_<versión>_x64-setup.exe`.
3. Ejecuta el instalador. También sirve para una instalación nueva.

Las listas, el historial y los ajustes se guardan fuera de la instalación. Para actualizar, instala encima de la versión existente.

## Avisos de nuevas versiones

Antares 0.3.0 incluye el actualizador. Con **Ajustes → Sistema → Avisar de versiones nuevas** activado, comprueba el canal al abrirse y cada seis horas mientras permanece abierta. También puedes usar **Buscar versión nueva**.

Cuando hay una versión superior, muestra un aviso y permite descargarla e instalarla después de confirmar. Antes de instalar, verifica la firma del paquete. Una instalación anterior sin actualizador necesita instalar esta versión manualmente una vez.

## Publicar la próxima versión

1. Aumentar la versión de la aplicación y preparar el instalador con la misma clave de firma.
2. Crear una release estable con la etiqueta `vX.Y.Z`.
3. Adjuntar el instalador y su `latest.json`, generado para ese mismo archivo.
4. Publicarla como la versión más reciente. Una release en borrador o preliminar no debe usarse como canal estable.

El manifiesto contiene la versión, las novedades, la URL y una firma pública de verificación. Las claves privadas y sus contraseñas se conservan fuera de GitHub.

Subir cambios al código fuente no distribuye una actualización: hay que publicar los archivos de la release. Los avisos llegan al comprobar el canal, no con la aplicación cerrada.

## Código y documentación

- [Código de Antares](https://github.com/Hanyer001/Antares)
- [Guía de publicación](https://github.com/Hanyer001/Antares/blob/main/docs/releases.md)
- [Reportar un problema](https://github.com/Hanyer001/Antares/issues)
