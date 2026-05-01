# Bar El Jardín — Landing Page

Página web de una sola sección (single-page) para el **Bar El Jardín**, un bar de tapas y cervecería de barrio en Viloira, Ourense.

> Av. de Elena Quiroga, 14 · 32315 Viloira (Ourense)

---

## Cómo abrir el proyecto

1. Descomprime el ZIP.
2. Abre la carpeta `bar-el-jardin` en **VS Code** (`File → Open Folder...`).
3. Para verla en el navegador:
   - Doble clic en `index.html` (se abrirá con el navegador por defecto), **o**
   - Instala la extensión **Live Server** en VS Code, haz clic derecho sobre `index.html` y elige **"Open with Live Server"**. Esto recarga la página automáticamente al guardar cambios.

No hay dependencias, ni `npm install`, ni build. Es **HTML + CSS + JS plano** en un solo archivo.

---

## Estructura

```
bar-el-jardin/
├── index.html      # Toda la web: HTML, CSS y JS embebidos
└── README.md       # Este archivo
```

---

## Cómo personalizar

Toda la web está en `index.html`. Las zonas más útiles para tocar:

### 1. Colores y tipografía
Al principio del `<style>` hay un bloque `:root` con las variables de color (verdes bosque, maderas, dorado, terracotta, cremas). Cambia ahí los hex y se actualiza toda la página.

### 2. Textos
Edita directamente el HTML. Las secciones están comentadas:
- `HERO` — frase grande de portada
- `ABOUT` — "Tu rincón verde en Viloira"
- `HIGHLIGHTS` — las 2 tarjetas (terraza y cocina)
- `HOURS` — horarios
- `LOCATION` — dirección y mapa
- `FOOTER`

### 3. Horario
Busca `<ul class="hours__list">` y cambia los días/horas. Recuerda actualizar también el bloque **Schema.org** (JSON-LD en el `<head>`) para que Google muestre los horarios correctos en la búsqueda.

### 4. Mapa
El mapa es un **SVG ilustrado** que se ve siempre, sin depender de iframes. Toda la tarjeta es un enlace que abre Google Maps en una pestaña nueva con la dirección del bar.

### 5. SEO
En el `<head>` están:
- Meta tags Open Graph (cuando se comparta el enlace en WhatsApp/Facebook)
- JSON-LD `BarOrPub` con dirección, teléfono (vacío — añádelo si quieres) y horario
- `theme-color` para el color del navegador móvil

---

## Próximos pasos sugeridos

- Añadir fotos reales de la terraza y de los platos (sustituir el SVG ilustrado del bloque `about__visual` por `<img src="...">`).
- Añadir teléfono real en el JSON-LD (`telephone`) y un botón "Llamar".
- Subir a un dominio. Opciones gratis: Netlify, Vercel, GitHub Pages, Cloudflare Pages — solo arrastras la carpeta y queda online en segundos.

---

## Licencia

Uso libre para el Bar El Jardín. Hecho con cariño.
