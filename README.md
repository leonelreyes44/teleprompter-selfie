# Teleprompter Selfie

App web de un solo archivo (`index.html`, sin librerías) para grabar video desde Safari en iPhone mientras lees un guion sobre la cámara. **El texto no aparece en el video grabado.**

## Uso

1. Abre la página por HTTPS en Safari y pulsa **Activar cámara** (acepta cámara y micrófono).
2. Escribe o pega tu guion en el cuadro. Arrástralo desde la barra superior del cuadro para moverlo.
3. Botón **⚙︎**: panel de ajustes (también se arrastra y tiene su propia opacidad): opacidad del panel y del texto (0–100 %), tamaño de letra (16–48 px), velocidad de desplazamiento, cámara **Selfie / Normal** y **Video grabado en espejo** (sí/no). Muestra además la duración estimada del desplazamiento.
4. Cambia el tamaño del cuadro de texto con el tirador de su esquina inferior derecha.
5. **⇋** voltea solo la vista previa. **▶︎** inicia/pausa el desplazamiento (si mueves el texto con el dedo, continúa desde donde lo sueltes). **Aa** muestra/oculta el texto sin detener la grabación. El chip **⏱** del cuadro indica el tiempo restante estimado.
6. Botón rojo: grabar / detener. Al detener puedes **Descargar** o **Grabar de nuevo**.

Texto y ajustes se guardan en `localStorage` (si no está disponible, la app sigue funcionando).

## Despliegue

Sitio estático: importa el repositorio en Vercel (sin framework ni build).

## Limitaciones conocidas (Safari iOS)

- Requiere HTTPS y iOS 14.3+ para `MediaRecorder`.
- Se graba en MP4 si Safari lo soporta; si no, WebM o un mensaje de error.
- La pantalla puede bloquearse en grabaciones largas; mantén el iPhone activo.
- Si cambias de app o bloqueas el teléfono, Safari puede pausar la cámara.
- La descarga abre el diálogo de Safari ("Descargas"); también puedes guardar desde el reproductor (Compartir → Guardar video).
- Cambiar de cámara vuelve a pedir el stream y puede mostrar un parpadeo.
