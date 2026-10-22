# Teleprompter Selfie

App web de un solo archivo (`index.html`, sin librerías) para grabar video desde Safari en iPhone mientras lees un guion sobre la cámara. **El texto no aparece en el video grabado.**

## Uso

1. Abre la página por HTTPS en Safari y pulsa **Activar cámara** (acepta cámara y micrófono).
2. Escribe o pega tu guion en el cuadro. Arrástralo desde la barra superior del cuadro para moverlo.
3. Botón **⚙︎**: opacidad del fondo (0–100 %), tamaño de letra (16–48 px), velocidad de desplazamiento y cámara **Selfie / Normal**.
4. **⇋** voltea la vista previa (solo la vista previa; el video sale sin voltear). **▶︎** inicia/pausa el desplazamiento. **Aa** muestra/oculta el texto sin detener la grabación.
5. Botón rojo: grabar / detener. Al detener puedes **Descargar** o **Grabar de nuevo**.

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
