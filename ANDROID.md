# Antares Android 0.3.3 Beta 1

Primera distribución pública para Android, basada en la interfaz y las funciones de Preview 10.

- Reproducción nativa, servicio multimedia y controles de la pantalla de bloqueo.
- Playlists, favoritos, carpetas, importación, cola y letras.
- Recomendaciones musicales, búsqueda con caché y mejor selección de audio.
- Interfaz táctil compacta, diseños predefinidos, doce fuentes locales y ajustes explicados.
- Personalización, perfiles, usuarios, copias completas y ahorro de batería.

## Instalación

Android 7.0 o posterior; ARM de 32 o 64 bits. Descarga `Antares-Android.apk` y abre el archivo; Android puede pedir autorización al navegador para instalar aplicaciones.

La edición pública se llama **Antares**, utiliza `com.hanyer.antares` y está firmada con la clave privada de distribución. La aplicación Preview usa otro identificador y puede coexistir. Para migrar, en Preview abre **Ajustes → Tus datos → Exportar copia completa**; instala Antares y usa **Restaurar archivo…** en la misma sección. Conserva la aplicación anterior hasta comprobar tu biblioteca.

Las próximas versiones públicas utilizarán el mismo identificador y certificado, con un código de versión creciente. Instálalas encima, sin desinstalar, para conservar los datos.

## Validación y alcance

172 pruebas JavaScript y 50 comprobaciones de interfaz de Preview 10; nueve categorías de ajustes verificadas en cuatro tamaños móviles. APK público optimizado, firmado y comprobado. No se ha probado en teléfono físico ni se ha medido batería; se publica en canal Beta.

El aviso de actualizaciones dentro de Android aún no está implementado. Las versiones se distribuyen en GitHub Releases y la página oficial. `android-latest.json` prepara un manifiesto separado para un futuro aviso en la app; el actualizador de Windows conserva su canal.
