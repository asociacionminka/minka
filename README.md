# Asociación Minka (Salta) — Formación en inclusión

Sitio estático (HTML + CSS + JS, sin frameworks) para presentar la misión, los dos cursos
y el acceso al aula virtual en MilAulas.

## Estructura

```
index.html        contenido de la página
styles.css        estilos (la paleta está en :root, arriba de todo)
script.js         menú móvil y año del pie
assets/           logo, favicon, fotos
.nojekyll         evita que GitHub Pages procese el sitio con Jekyll
```

## Qué falta completar

Los textos son de ejemplo: revisar misión, cursos (nombres, horas, semanas) y "Quiénes somos" con la información real. Además:

- [x] Link al aula virtual: https://minka.milaulas.com/login/index.php
- [x] Logo: `assets/logo-marca.svg` (personitas, header y favicon) y `assets/logo-completo.jpg`.
- [ ] Foto del equipo → `assets/equipo.jpg` y reemplazar el `.photo-placeholder` en "Quiénes somos".
- [ ] Foto de portada (`assets/hero.jpg`): reemplazarla por una versión con licencia de uso y mayor resolución (ideal ≥ 1200 px de ancho).
- [ ] Correo y teléfono reales (los actuales son de ejemplo).

## Ver la página en local

```powershell
python -m http.server 5510
```

Abrir http://localhost:5510

## Publicar en GitHub Pages

1. Crear un repositorio nuevo en GitHub (por ejemplo `mision-docente`), **público**.
2. Desde esta carpeta:
   ```powershell
   git init
   git add .
   git commit -m "Primera versión de la página"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/mision-docente.git
   git push -u origin main
   ```
3. En GitHub: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.
4. En uno o dos minutos queda online en `https://TU-USUARIO.github.io/mision-docente/`.

Cada `git push` posterior actualiza la página automáticamente.

## Accesibilidad

- Enlace "Saltar al contenido", navegación por teclado y foco visible.
- Respeta `prefers-reduced-motion`.
- Los enlaces que abren otra pestaña lo anuncian a lectores de pantalla.
