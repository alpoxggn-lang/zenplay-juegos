# ZenPlay Juegos

Aplicación Android de prueba para móvil, tablet, Android TV y Fire TV con Fire OS. El funcionamiento en equipos físicos varía según el dispositivo y el núcleo.

## Descargar

**Enlace fijo para Downloader:** [ZenGame.apk](https://github.com/alpoxggn-lang/zenplay-juegos/releases/latest/download/ZenGame.apk).

El enlace no contiene el número de versión. Cada nueva release marcada como `latest` debe incluir la APK actual con el nombre exacto `ZenGame.apk` para conservarlo. El archivo es idéntico a la APK con nombre de versión.

La APK y el código editable se publican en [Releases](https://github.com/alpoxggn-lang/zenplay-juegos/releases/latest).

- `ZenPlay-0.3.1-prueba.apk`: aplicación de prueba.
- `ZenPlay-0.3.1-codigo.zip`: proyecto Android editable y avisos de licencias.
- `ZenPlay-0.3.1-fuentes-terceros.zip`: fuentes archivadas de componentes nativos y su inventario.
- `zenplay-update.json`: versión, tamaño y SHA-256 que consulta el actualizador.

Para conservar biblioteca y ajustes, instalar sobre la app anterior usando la misma firma. La 0.3.0 necesita una instalación manual de la 0.3.1 para incorporar el actualizador. Después, la app detecta las siguientes versiones públicas al abrirse o volver al primer plano, con un intervalo mínimo de seis horas entre intentos. También puede comprobarse desde Ajustes. La descarga se solicita desde el aviso y Android confirma la instalación.

## Funciones

- Acceso con cuentas de cliente del panel ZenPlay Negocio.
- Catálogos externos, biblioteca y favoritos.
- Núcleos de emulación incluidos, con compatibilidad y requisitos según cada sistema.
- Controles táctiles configurables y detección de mandos reconocidos por Android.
- Interfaz adaptable; modo TV con navegación superior horizontal.
- Pantalla del juego con tamaño del 50 al 200 %, posición vertical y preferencias guardadas.
- Portadas estáticas y GIF.

## Código y licencias

El código editable está en el ZIP de cada versión; el árbol principal de este repositorio sirve como canal de distribución y documentación. El frontend propio usa GPL-3.0-or-later y cada componente conserva su licencia. Los avisos e inventarios están incluidos en los archivos de código y fuentes de terceros.

Las fuentes archivadas son snapshots de referencia: no se ha verificado su correspondencia exacta con los binarios nightly de los núcleos. Algunas licencias restringen uso comercial. Esta publicación no certifica una distribución comercial ni que todos los motores funcionen en todos los equipos. Se mantienen 11 bibliotecas con alineación ELF inferior a 16 KB. La firma actual es de desarrollo.

No se incluyen ROMs o BIOS comerciales, cuentas, sesiones ni claves de firma. Los catálogos son servicios externos y sus enlaces e imágenes pueden cambiar. La descarga o el acceso a un catálogo no concede derechos sobre su contenido.

## Publicar una actualización

1. Aumentar `versionCode`, actualizar `versionName` y compilar usando la misma clave privada de firma.
2. Comprobar las pruebas, la APK y las condiciones de distribución de cada componente.
3. Crear un borrador de release con una etiqueta de versión y adjuntar la APK, el código y los archivos de fuentes correspondientes. Adjuntar también una copia idéntica de la APK llamada exactamente `ZenGame.apk`, con mayúsculas y minúsculas tal como aparecen, para mantener el enlace fijo de Downloader.
4. Adjuntar `zenplay-update.json` con `packageName`, `versionCode`, `versionName`, `apkUrl`, `sha256`, `size`, `minSdk` y `notes`. El enlace debe corresponder a la etiqueta y al nombre real de la APK en este repositorio.
5. Publicar como la última versión (`latest`) cuando todos los archivos estén completos. Los borradores y pre-releases no se ofrecen en el canal actual.

Nunca adjuntar sesiones, bases de datos de clientes, contraseñas, tokens ni claves privadas de firma.
