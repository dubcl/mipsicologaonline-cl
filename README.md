# mipsicologaonline-cl

Landing page para una psicóloga clínica, construida con [Hugo](https://gohugo.io/).
Sitio estático, de una sola página, con diseño responsivo y paleta cálida y serena.

## Requisitos

- [Hugo](https://gohugo.io/installation/) (extended o standard) — probado con `v0.163.1`.

```bash
brew install hugo   # macOS
```

## Desarrollo local

```bash
hugo server -D
```

Abre http://localhost:1313 en el navegador. El sitio se recarga solo al guardar cambios.

## Compilar para producción

```bash
hugo --minify
```

El sitio final queda en `public/`, listo para subir a cualquier hosting estático
(Netlify, Cloudflare Pages, GitHub Pages, etc.).

## Cómo personalizar

Casi todo el contenido se edita sin tocar HTML:

| Qué cambiar | Dónde |
|---|---|
| Nombre, profesión, email, enlaces de agenda (Clinifica/Doctoralia), redes sociales | `hugo.toml` → `[params]` |
| Texto "Sobre mí", servicios, pasos y preguntas frecuentes | `content/_index.md` |
| Foto de perfil | reemplaza `static/images/profile.svg` por tu imagen (ej. `profile.jpg`) y actualiza `profileImage` en `hugo.toml` |
| Colores y estilos | `static/css/style.css` (variables `:root`) |

> ⚠️ Los datos de ejemplo (nombre, número de registro, teléfono) son ficticios.
> Reemplázalos por los reales antes de publicar.

## Estructura

```
hugo.toml                 # configuración y datos de contacto
content/_index.md         # contenido de las secciones
layouts/
  _default/baseof.html    # plantilla base
  index.html              # secciones de la home
  partials/               # head, header, footer
static/
  css/style.css           # estilos
  images/profile.svg      # foto (placeholder)
  favicon.svg
```
