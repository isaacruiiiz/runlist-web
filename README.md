# Web de Runlist

Web estática alojada en Cloudflare Pages: portada, privacidad, borrado de cuenta
y la página de los enlaces de invitación (`/i/CODIGO`).

Sin compilación ni dependencias: lo que hay en esta carpeta es lo que se publica.

## Publicar

Cada cambio que se sube a la rama `main` se publica solo en Cloudflare Pages.

## Pendiente antes de publicar la app

- `privacidad.html`: rellenar `[NOMBRE Y APELLIDOS]` y `[REGIÓN DE LOS SERVIDORES DE SUPABASE]`.
- `.well-known/apple-app-site-association`: sustituir `TEAM_ID.BUNDLE_ID` (cuenta de desarrollador de Apple).
- `.well-known/assetlinks.json`: sustituir `ANDROID_PACKAGE_NAME` y `SHA256_FINGERPRINT` (firma de la app de Android).

## Estructura

- `index.html` — portada
- `privacidad.html`, `borrar-cuenta.html` — páginas legales
- `invitacion.html` — destino de `/i/*` (ver `_redirects`)
- `_headers` — cabeceras de seguridad y tipo de contenido de la verificación de Apple
- `assets/` — estilos, tipografía Outfit servida desde la propia web, iconos e imagen para compartir
