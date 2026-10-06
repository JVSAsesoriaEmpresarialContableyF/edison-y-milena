# Edison & Milena · Nuestra boda

Dirección bonita de la invitación digital de la boda de Edison y Milena (sábado 12 de diciembre de 2026, Sogamoso).

La invitación de verdad es una aplicación web de Google Apps Script. Esta página de GitHub Pages
(`https://TU-USUARIO.github.io/edison-y-milena/`) la muestra a pantalla completa dentro de un marco,
con una pantalla de carga mientras abre, y pone la foto y el texto que aparecen al compartir el enlace por WhatsApp.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La página: pantalla de carga, la invitación a pantalla completa y los datos para compartir. |
| `vista-previa.jpg` | La imagen que muestra WhatsApp al compartir el enlace (1200 × 630). |
| `icono.svg`, `apple-touch-icon.png` | El sello E&M de la pestaña del navegador y del acceso directo en el celular. |
| `404.html` | Si alguien escribe mal la dirección, lo lleva a la invitación. |
| `.nojekyll` | Le dice a GitHub que publique los archivos tal cual. |
| `PUBLICAR-EN-GITHUB.md` | Guía paso a paso para publicar. |

## Cómo se actualiza

- **Cambios en la invitación** (textos, fotos, música): se hacen en Apps Script y se publican como
  **Nueva versión** de la misma implementación (Implementar → Gestionar implementaciones → lápiz → Versión: Nueva versión).
  La dirección `/exec` no cambia, así que aquí no hay que tocar nada.
- **Si cambia la dirección `/exec`** (por ejemplo, si se crea una implementación nueva): en `index.html`
  cambia la constante `URL_APP` y también el enlace dentro de `<noscript>`.
- **Otra imagen para WhatsApp**: reemplaza `vista-previa.jpg` por otra de 1200 × 630 y menos de 300 KB, con el mismo nombre.
- **Tu usuario de GitHub**: en `index.html`, cambia `TU-USUARIO` en las tres líneas que están debajo del comentario
  `<!-- Cambia TU-USUARIO por tu usuario de GitHub -->`.
- Para probar en el computador: `python -m http.server 8790` dentro de esta carpeta y abrir `http://localhost:8790/`.
  Con `?app=http://localhost:8766/Index.html` carga una copia local de la invitación (solo se aceptan `localhost` o `script.google.com`).
