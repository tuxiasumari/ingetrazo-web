# IngeTrazo · Landing Page

Sitio web público de **IngeTrazo** (https://ingetrazo.com) — modelador 3D
libre para ingeniería y arquitectura. Hermano visual de
`~/ingepresupuestos-web` (ingepresupuestos.com): mismo stack, misma
estructura, mismas convenciones. **Ante la duda, el CLAUDE.md de aquel repo
es la referencia extendida.**

Repo del producto: `~/ingetrazo/` → github.com/tuxiasumari/ingetrazo (GPL-3.0).

## Stack (idéntico al hermano)

- HTML + CSS + JS vanilla, **sin build step**. Inter vía Google Fonts.
- Hosting objetivo: Cloudflare Pages (ver `COMO-PUBLICAR.md`).
- `script.js`: versión desde **GitHub Releases API** (no R2 como el hermano),
  menú móvil, scroll reveal, lightbox, botón copiar.
- SEO: JSON-LD (SoftwareApplication + FAQPage — espejados con el HTML del
  FAQ), canonical, OG/Twitter (`images/og-banner.jpg` 1200×630), sitemap,
  robots. `_headers` con CSP (lista blanca: fonts + api.github.com).

## Identidad visual

Sistema de la familia Inge[X] con **acento por producto**:

- IngeTrazo = **Blueberry `#3689E6`** (`--accent`); IngePresupuestos = naranja.
- El naranja aparece SOLO en la sección puente «Del modelo al presupuesto».
- Secciones coloreadas: BIM = gradiente azul (la tesis), Terreno = lime suave
  `#F2F9EC`, puente = `--orange-soft`.
- Resto idéntico al hermano: header slate-700, impact slate-900, screenshots
  grandes alternando lado, español neutro (tuteo), "Ing. Marco Sumari".

## Screenshots (`images/screenshots/`)

Todas REALES, generadas por script contra la app en GL
(`QT_QPA_PLATFORM=xcb` + captura con `import -window` de ImageMagick —
`QWidget.grab()` NO captura el overlay QPainter del viewport):

- `principal.jpeg` — hero (copiada de `~/ingetrazo/docs/images/viewport.png`,
  recortada la franja inferior).
- `modelado.jpeg` — recorte del viewport del hero.
- `bim.jpeg` — casita taggeada + panel BIM con metrados (script scratch
  `shot_bim.py`; los números del panel se verificaron correctos).
- `terreno.jpeg` — terreno 3D del valle del Colca (Yanque) con Esri satelital.
- `import-sketchup.jpeg` — "Proyecto vivero.dae" real importado (314 grupos).

OG banner: `.cover-build/og.html` + Chromium headless (snap: solo escribe
dentro de $HOME) → `images/og-banner.jpg`.

## Decisiones (no revertir sin discutir)

- Sin frameworks, sin trackers, sin cookies banner.
- Descarga: hoy apunta a GitHub (código fuente + 3 comandos); cuando existan
  binarios (v0.2+), convertir a cards por SO como el hermano.
- **No publicar sin aprobación de Marco** — iterar local con
  `python3 -m http.server 8765`.

## Contacto

Ing. Marco Sumari · ing.sumari@gmail.com · WhatsApp +51 998 839 090
