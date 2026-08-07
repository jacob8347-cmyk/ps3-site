# PS3 Static Site Template (Homebrew & Temas)

Plantilla pensada para navegadores limitados (PS3). Provee:
- Interfaz pública (`index.html`) que carga `manifest.json`.
- Carpeta `files/` para subir paquetes, temas, imágenes.
- Página de administración (`admin.html`) que usa la GitHub REST API para subir archivos y actualizar `manifest.json`.

IMPORTANTE — legales
- No uses este repositorio para distribuir material con copyright sin permiso.
- Yo no puedo ayudar a distribuir juegos comerciales pirateados.

Instrucciones rápidas
1. Crea un repositorio en GitHub (por ejemplo `owner/ps3-site`) y sube estos archivos.
2. En Settings -> Pages, habilita GitHub Pages desde la rama `main` (o la rama por defecto). La web estará disponible en `https://<owner>.github.io/<repo>/`.
3. Para subir archivos desde `admin.html`:
   - Crea un Personal Access Token (Settings -> Developer settings -> Personal access tokens) con scope `repo` (o `public_repo` si el repo es público).
   - Abre `admin.html`, introduce `owner/repo` y el token, usa el formulario para subir archivos.
   - El admin subirá el archivo a `files/<nombre>` y añadirá/editará `manifest.json`.

Límites y notas técnicas
- GitHub limita archivos individuales a 100 MB vía push normal. Si necesitas archivos más grandes usa Git LFS o un host externo (CDN, storage público).
- Pegar un token en admin.html implica riesgo si usas un equipo compartido; guarda el token en un lugar seguro y revócalo si lo expones.
- El navegador de PS3 es limitado: evita scripts pesados, comprueba enlaces directos con `raw.githubusercontent.com`.

Si quieres que yo suba todo directamente a tu cuenta, pásame:
- El owner/repo exacto (ej: `jacob8347-cmyk/ps3-site`) y confirma que el repositorio ya existe.
- Confirma que quieres que yo haga el push (yo NO crearé nuevos repositorios; el repo debe existir).
