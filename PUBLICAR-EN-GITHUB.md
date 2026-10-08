# Cómo publicar la invitación en GitHub Pages

Con esta guía la invitación queda en una dirección corta y bonita:

**`https://TU-USUARIO.github.io/edison-y-milena/`**

(`TU-USUARIO` será tu nombre de usuario de GitHub). Es gratis y no necesitas instalar nada: todo se hace desde el navegador.

GitHub está en inglés. En esta guía los botones aparecen **en negrita y con su nombre exacto en inglés**, y al lado se explica qué hacen.

> **Antes de empezar (importante):** en Apps Script debes haber publicado una **Nueva versión** con el `Code.gs` y el `Index.html` nuevos
> (ver la sección "Dirección bonita con GitHub Pages" de `invitacion-apps-script\COMO-PUBLICAR.md`).
> Si no lo haces, Google no deja mostrar la invitación dentro de esta página: los invitados verán la pantalla de carga
> y, a los pocos segundos, el botón **Abrir la invitación**. Ese botón funciona, pero se pierde la dirección bonita.

---

## Paso 1. Crea tu cuenta de GitHub (si no tienes)

1. Entra a [github.com](https://github.com) y pulsa **Sign up** (registrarse), arriba a la derecha.
2. Escribe tu correo, una contraseña y un **Username** (nombre de usuario).
   - El usuario forma parte de la dirección de la invitación. Elige uno corto, fácil de dictar y sin tildes,
     por ejemplo `edisonymilena`. Solo se permiten letras, números y guiones.
3. Pulsa **Continue** / **Create account** y escribe el código que te llega al correo.
4. Si te hace preguntas de bienvenida, puedes saltarlas (**Skip personalization**).

## Paso 2. Crea el repositorio `edison-y-milena`

Un "repositorio" es la carpeta donde GitHub guarda los archivos de la página.

1. Arriba a la derecha pulsa el botón **+** y elige **New repository** (nuevo repositorio).
2. En **Repository name** escribe exactamente: `edison-y-milena`
   (en minúsculas y con guiones; este nombre aparece en la dirección).
3. En la visibilidad elige **Public** (público).
   GitHub Pages es gratis solo con repositorios públicos. No te preocupes: en estos archivos no hay datos privados;
   las confirmaciones de los invitados siguen guardándose en tu hoja de Google.
4. Deja lo demás como está (sin README, sin .gitignore, sin licencia).
5. Pulsa el botón verde **Create repository**.

## Paso 3. Sube los archivos

1. En la página del repositorio recién creado, busca el enlace **uploading an existing file** (subir un archivo existente),
   en el recuadro "Quick setup". Si en cambio ves un botón **Add file**, pulsa **Add file → Upload files**.
2. En tu computador abre la carpeta `github-pages` (está en `VIDEO BODA MILENA\github-pages`).
3. Entra a la carpeta, selecciona **todo su contenido** con **Ctrl + A** y arrástralo al recuadro de GitHub que dice
   *Drag files here to add them to your repository*.
   - Arrastra los **archivos**, no la carpeta `github-pages` completa: `index.html` tiene que quedar en la raíz del repositorio,
     no dentro de una subcarpeta.
   - Deben aparecer en la lista: `index.html`, `404.html`, `vista-previa.jpg`, `icono.svg`, `apple-touch-icon.png`,
     `.nojekyll`, `README.md` y esta guía.
4. Abajo, en **Commit changes**, deja el mensaje que trae ("Add files via upload"), revisa que esté marcada la opción
   **Commit directly to the `main` branch** y pulsa el botón verde **Commit changes** (guardar los cambios).

### Sobre el archivo `.nojekyll`

Es un archivo vacío cuyo nombre empieza con punto. Le dice a GitHub que publique los archivos tal cual, sin procesarlos.

- Al terminar la subida, revisa que `.nojekyll` aparezca en la lista de archivos del repositorio.
- **Si no lo ves en tu carpeta**: algunos sistemas (sobre todo Mac) esconden los archivos que empiezan con punto.
  En Windows 11 puedes mostrarlos así: en el Explorador de archivos, **Ver → Mostrar → Elementos ocultos**.
- **Si no se subió**, créalo desde la web:
  1. En el repositorio pulsa **Add file → Create new file**.
  2. En la casilla del nombre (*Name your file...*) escribe `.nojekyll` (con el punto al principio).
  3. Deja el contenido vacío. Si GitHub no te deja guardarlo vacío, escribe cualquier palabra: funciona igual.
  4. Pulsa **Commit changes...** y, en la ventana que aparece, otra vez **Commit changes**.
- Tranquilidad: aun sin `.nojekyll` la invitación funciona; solo tarda un poco más en publicarse.

## Paso 4. Activa GitHub Pages

1. En el repositorio, pulsa la pestaña **Settings** (configuración, con un ícono de engranaje), arriba a la derecha.
2. En el menú de la izquierda, en la sección *Code and automation*, pulsa **Pages**.
3. En **Build and deployment** → **Source**, elige **Deploy from a branch** (publicar desde una rama).
4. En **Branch**, elige **main** y, al lado, la carpeta **/ (root)**.
5. Pulsa **Save** (guardar).

## Paso 5. Espera 1 o 2 minutos y abre la dirección

1. Espera un par de minutos y recarga la página de **Settings → Pages**.
2. Arriba aparecerá: *Your site is live at `https://tu-usuario.github.io/edison-y-milena/`*, con el botón **Visit site**.
3. Ábrela: primero sale la pantalla de carga (nombres y sello) y luego el sobre de la invitación.
4. Si ves un error 404, espera unos minutos más (la primera vez puede tardar hasta 10). El avance se ve en la pestaña
   **Actions**: cuando "pages build and deployment" tenga un visto verde ✓, ya está publicada.

## Paso 6. Pon tu usuario en `index.html` (para la foto de WhatsApp)

WhatsApp necesita la dirección completa de la foto de vista previa. Hay que cambiar `TU-USUARIO` por tu usuario
**en tres líneas** de `index.html`.

1. En el repositorio, pulsa el archivo **index.html**.
2. Pulsa el **lápiz** (*Edit this file*, editar este archivo), arriba a la derecha del contenido.
3. Busca este comentario (está cerca del principio; puedes usar **Ctrl + F** dentro del editor):
   ```
   <!-- Cambia TU-USUARIO por tu usuario de GitHub -->
   ```
4. En las tres líneas de abajo (`og:url`, `og:image` y `twitter:image`) cambia `TU-USUARIO` por tu usuario **en minúsculas**.
   Por ejemplo, si tu usuario es `EdisonYMilena`, quedaría:
   ```
   <meta property="og:url" content="https://edisonymilena.github.io/edison-y-milena/">
   <meta property="og:image" content="https://edisonymilena.github.io/edison-y-milena/vista-previa.jpg">
   <meta name="twitter:image" content="https://edisonymilena.github.io/edison-y-milena/vista-previa.jpg">
   ```
   No cambies nada más: deja las comillas, las barras `/` y el resto del texto.
5. Pulsa el botón verde **Commit changes...** (arriba a la derecha) y, en la ventana que aparece, otra vez **Commit changes**.
6. Espera 1 minuto a que se vuelva a publicar.
7. Comprueba que la foto existe abriendo `https://tu-usuario.github.io/edison-y-milena/vista-previa.jpg`.

## Paso 7. Pon la dirección bonita también en Apps Script

Para que el botón **Compartir por WhatsApp** de la invitación use esta dirección, sigue el punto 3 de la sección
"Dirección bonita con GitHub Pages" de `invitacion-apps-script\COMO-PUBLICAR.md`
(cambiar `URL_INVITACION` en `Code.gs` y publicar otra **Nueva versión**).

**Recuerda:** cada vez que cambies algo en Apps Script, publica una **Nueva versión** de la misma implementación
(**Implementar → Gestionar implementaciones → lápiz Editar → Versión: Nueva versión → Implementar**).
Si no, el iframe queda bloqueado y saldrá el botón **Abrir la invitación**.

## Paso 8. Comparte

Comparte esta dirección: `https://tu-usuario.github.io/edison-y-milena/`

Al pegarla en WhatsApp, **espera a que aparezca la vista previa con la foto** antes de enviar el mensaje.

---

## Cómo hacer que WhatsApp actualice la vista previa

WhatsApp guarda la vista previa de cada enlace durante un tiempo. Si la compartiste antes de cambiar `TU-USUARIO`
(o cambiaste la foto) y sigue saliendo sin foto o con la vieja:

1. Comparte el enlace con un agregado al final, por ejemplo `https://tu-usuario.github.io/edison-y-milena/?v=2`
   (la próxima vez `?v=3`, etc.). Para WhatsApp es un enlace nuevo, así que vuelve a leer la foto; la invitación es la misma.
2. Borra el mensaje a medio escribir, vuelve a pegar el enlace y espera unos segundos a que cargue la vista previa.
3. Para revisar qué ve un servicio de mensajería, pega la dirección en el
   [Depurador de Facebook](https://developers.facebook.com/tools/debug/) y pulsa **Debug** y luego **Scrape Again**.
   Debe mostrar el título "Edison & Milena · Nuestra boda" y la foto.

## Solución de problemas

**Sale "404 · There isn't a GitHub Pages site here" recién publicado**
- Espera unos minutos (la primera publicación puede tardar hasta 10) y recarga.
- Revisa en **Settings → Pages** que diga *Your site is live* y que la fuente sea **main** y **/ (root)**.
- Revisa que el repositorio se llame exactamente `edison-y-milena` y que la dirección termine en `/edison-y-milena/`.
- Revisa que `index.html` esté en la página principal del repositorio y no dentro de una carpeta. Si quedó dentro de
  `github-pages/`, vuelve a subir los archivos sueltos (Paso 3) y borra la carpeta.
- Revisa que el repositorio sea **Public** (en **Settings → General**, al final, *Danger Zone → Change visibility*).

**La vista previa de WhatsApp sale sin foto**
- Revisa el Paso 6: las tres líneas deben tener tu usuario real, en minúsculas, sin `TU-USUARIO`.
- Abre `https://tu-usuario.github.io/edison-y-milena/vista-previa.jpg`: si no se ve la foto, la dirección está mal escrita
  o la imagen no se subió.
- Después de corregir, usa el truco de `?v=2` (arriba).

**La invitación no aparece y sale el botón "Abrir la invitación"**
- Casi siempre es porque falta publicar la **Nueva versión** en Apps Script con el `Code.gs` nuevo. Sin ella, Google
  no deja mostrar la invitación dentro de otra página.
- Revisa en Apps Script que la implementación tenga **Ejecutar como: Yo** y **Quién tiene acceso: Cualquier usuario**.
- Con internet muy lento el botón puede salir aunque todo esté bien: a los 8 segundos aparece discreto abajo y,
  si la invitación termina de cargar, el botón se va solo. El botón siempre abre la invitación, así que nadie se queda sin verla.

**La invitación pide iniciar sesión con Google**
- La implementación de Apps Script está en "Cualquier usuario con cuenta de Google" o el dominio restringe compartir.
  Cámbiala a **Cualquier usuario** (ver la sección de Google Workspace en `COMO-PUBLICAR.md`).

**Hice un cambio y no se ve**
- Los cambios en GitHub tardan 1 o 2 minutos en publicarse; recarga la página.
- Los cambios en Apps Script solo se ven después de publicar una **Nueva versión**.

**Cambió la URL `/exec` de Apps Script** (por ejemplo, porque se creó una implementación nueva)
- Edita `index.html` con el lápiz y cambia la dirección en **dos lugares**: la constante `URL_APP` (dentro del `<script>`,
  al final del archivo) y el enlace dentro de `<noscript>`. Luego **Commit changes**.

**Quiero probar antes de compartir**
- Abre la dirección en tu celular con datos móviles (no solo con el wifi de la casa), toca el sello y verifica que suene la música.
- Envíate el enlace a ti mismo por WhatsApp para ver la vista previa.
