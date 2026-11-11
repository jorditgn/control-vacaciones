# Control de vacaciones

Aplicación web instalable (PWA) para apuntar las vacaciones de cada trabajador:
días laborables y naturales, justificante para firmar y resumen anual en PDF.

- **Dirección:** <https://jorditgn.github.io/control-vacaciones/>
- **Tecnología:** un único `index.html` (HTML, CSS y JavaScript sin compilar),
  `sw.js` para funcionar sin conexión, jsPDF 2.5.1 + jspdf-autotable 3.8.2 en `vendor/`.
- **Datos:** sólo en el dispositivo. IndexedDB `control-vacaciones` (un único
  documento JSON) con espejo en `localStorage['vacaciones-copia-seguridad']`.
- **Publicación:** GitHub Pages desde la rama `main`, carpeta raíz.

Comparte dominio con `diario-trabajos` y `control-horas`; por eso usa nombres
propios de base de datos, clave de `localStorage`, prefijo de caché
(`vacaciones-`) y fichero de copia (`vacaciones-copia-FECHA.txt`).

Para publicar un cambio: subir `VERSION` en `sw.js` **y** en `index.html`.

Manual de uso: [LEEME.txt](LEEME.txt).
