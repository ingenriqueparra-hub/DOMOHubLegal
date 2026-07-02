# DOMOHubLegal — sitio estático

Versión estática y ligera del sitio (home + 3 artículos de blog), lista para
publicar en **GitHub Pages**. Es autocontenida: incluye solo el HTML y los
assets (CSS, JS, imágenes) realmente usados por esas páginas.

## Contenido

```
index.html                          # Página principal
el-caso-del-esquirolaje-tecnologico/          # Blog 1
la-contratacion-temporal-de-los-docentes-universitarios/   # Blog 2
la-delimitacion-.../                # Blog 3
wp-content/  wp-includes/           # Solo los assets referenciados
.nojekyll                           # Evita el procesado Jekyll de GitHub
```

Peso total: ~4.7 MB (el sitio WordPress original pesaba ~340 MB).

## Publicar en GitHub Pages

Todas las rutas son **relativas**, así que el sitio funciona igual servido desde
la raíz del dominio (`usuario.github.io`), desde una subruta de proyecto
(`usuario.github.io/repo/`) o desde una subcarpeta local.

Pasos:
1. Sube el **contenido** de esta carpeta `web/` al repositorio.
2. En **Settings → Pages**, selecciona la rama y la carpeta raíz (`/`).
3. Espera al despliegue y abre la URL.

## Probar en local

```bash
cd web
python -m http.server 8000
# abre http://localhost:8000
```

## Notas

- Las fuentes se cargan desde Google Fonts (requiere conexión a internet).
- Los enlaces a comentarios (`#respond`) y feeds RSS (`/feed/`) no tienen
  equivalente estático y no son funcionales (el resto de la navegación sí).
- Los formularios (WhatsApp/contacto) apuntan al sitio original; al ser estático
  no procesan datos en el servidor.
