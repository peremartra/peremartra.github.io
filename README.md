# Pere Martra - Personal Site V2

Landing page limpio con foto, links sociales, y layout de 2 columnas (Formación | Consultoría).

## Setup Rápido

### 1. Añadir tu foto
Coloca tu foto de perfil en: `assets/images/profile.jpg`
- Formato: JPG o PNG
- Tamaño recomendado: 400x400px mínimo (se mostrará como círculo de 180px)

### 2. Editar información personal
Edita `_config.yml`:
```yaml
author:
  email: tu-email-real@example.com

github_username: peremartra
linkedin_username: tu-username-linkedin
twitter_username: tu-username-twitter  # opcional
```

### 3. Subir a GitHub

**Opción A - Via Web:**
1. Crea repo `peremartra.github.io`
2. Arrastra TODOS los archivos
3. Commit

**Opción B - Via Terminal:**
```bash
cd peremartra-site-v2
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/peremartra/peremartra.github.io.git
git push -u origin main
```

### 4. Activar GitHub Pages
Settings → Pages → Source: main → / (root) → Save

Espera 2 minutos → https://peremartra.github.io

## Estructura del Contenido

Todo el contenido está en `index.md`:
- Descripción principal (después del `---`)
- `formation:` → Columna izquierda (libros, master, repos)
- `consulting:` → Columna derecha (training, research partnership)

## Personalización

### Cambiar contenido
Edita `index.md` - usa Markdown normal:
- `**texto**` = negrita
- `[texto](url)` = link
- `### Título` = subtítulo

### Cambiar colores
Edita `assets/css/style.css`:
- `#0066cc` = color de links y acentos (línea ~76, ~105, etc)
- `#1a1a1a` = color de títulos
- `#fafafa` = fondo de columnas

### Cambiar tamaños
En `style.css`:
- `.hero-photo img` → tamaño de foto (línea ~38)
- `.hero-content h1` → tamaño nombre (línea ~44)
- `.two-columns` → gap entre columnas (línea ~103)

## Preview Local (Opcional)

```bash
bundle install
bundle exec jekyll serve
# http://localhost:4000
```

## Lo que hace este diseño:

✅ Hero grande con foto circular  
✅ Nombre prominente con links sociales al lado  
✅ Descripción + current work limpios  
✅ 2 columnas para Formación vs Consultoría  
✅ Responsive (mobile-friendly)  
✅ Zero JavaScript (solo HTML/CSS)  
✅ Font Awesome para iconos sociales  

## Diferencias vs V1:

- ❌ Sin páginas separadas (research, training, contact)
- ❌ Sin menú de navegación
- ✅ TODO en una página
- ✅ Menos contenido, más impacto visual
- ✅ Layout de 2 columnas
- ✅ Foto prominente

## Custom Domain (Después)

Settings → Pages → Custom domain → `peremartra.com`

## Troubleshooting

**Foto no aparece:**
- Verifica que el archivo esté en `assets/images/profile.jpg`
- Nombres de archivo case-sensitive en Linux

**Iconos sociales no aparecen:**
- Font Awesome se carga desde CDN (requiere internet)
- Si falla, verifica que el link CDN esté actualizado

**Columnas se ven raras:**
- En móvil, las columnas se apilan (es normal)
- En desktop, deben estar lado a lado

## Próximos Pasos

1. [ ] Añade tu foto
2. [ ] Edita _config.yml con tus datos
3. [ ] Revisa contenido en index.md
4. [ ] Sube a GitHub
5. [ ] Testea en móvil

---

**Este diseño prioriza:**
- Impacto visual inmediato (foto + nombre)
- Menos texto, más estructura
- Facilidad de edición (todo en 1 archivo)
- Zero mantenimiento
