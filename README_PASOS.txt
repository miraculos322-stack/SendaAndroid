SENDA — PROYECTO ANDROID (VERSIÓN INICIAL)
==========================================

Esta carpeta contiene un proyecto Android que puede compilarse en la nube.
No incluye un APK ya compilado. El APK debe generarse mediante GitHub Actions.

FUNCIONES DE ESTA BASE
- Interfaz móvil SENDA con pestañas Inicio, Buses, Rutas, Guardián y Accesibilidad.
- Mapa real integrado Leaflet + teselas de OpenStreetMap.
- Solicitud de ubicación solo cuando el usuario la pide.
- Búsqueda puntual de lugares usando Nominatim.
- Consulta de paradas cartografiadas cercanas mediante Overpass.
- Selección de parada en el mapa y distancia aproximada.
- Planificador que ubica origen/destino, sin fingir que eso equivale a una ruta de bus.
- Aviso manual del Modo Guardián.
- Reportes guardados localmente en el dispositivo.

LIMITACIONES IMPORTANTES
- No hay APK compilado/verificado en este ZIP.
- Mapa y consultas requieren conexión a internet.
- Las paradas son datos cartografiados, no una lista oficial garantizada.
- No se muestran buses en vivo, llegadas, líneas, ocupación ni transbordos porque aún no se conectó una fuente oficial autorizada.
- Los reportes se quedan en el dispositivo; no se comparten con la comunidad.
- Modo Guardián no realiza seguimiento continuo ni envía alertas automáticas.
- Nominatim y Overpass son servicios comunitarios con límites de uso; no deben recibir tráfico intensivo. Para una publicación real conviene añadir backend, caché y un proveedor de geocodificación adecuado.
- Leaflet se carga desde CDN; el mapa puede no abrir si la red bloquea el CDN.
- Antes de distribuir públicamente, revisar licencias, privacidad, pruebas y políticas de servicios externos.

CÓMO GENERAR EL APK DESDE EL CELULAR
1. Descarga y extrae este ZIP en el teléfono.
2. En GitHub crea un repositorio vacío llamado SendaAndroid.
3. Sube el CONTENIDO extraído, conservando las carpetas y el archivo .github/workflows/build-apk.yml.
4. Abre la pestaña Actions del repositorio y el flujo “Build Senda APK”.
5. Pulsa Run workflow si no inició automáticamente.
6. Cuando termine correctamente, abre la ejecución y descarga el artefacto “Senda-debug-apk”.
7. Extrae ese ZIP y abre app-debug.apk para instalarlo en Android.

Si la compilación falla, comparte el mensaje de error o una captura para corregirlo.
