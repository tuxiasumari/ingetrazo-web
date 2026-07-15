# Cómo publicar ingetrazo.com

El sitio es estático (HTML/CSS/JS, sin build). El camino recomendado es el
mismo de ingepresupuestos.com: **Cloudflare Pages**.

## Primera vez (una sola vez)

1. Crear un repo en GitHub (p. ej. `tuxiasumari/ingetrazo-web`) y pushear
   este directorio:

   ```bash
   cd ~/ingetrazo-web
   git remote add origin git@github.com:tuxiasumari/ingetrazo-web.git
   git push -u origin main
   ```

2. En el dashboard de Cloudflare → **Workers & Pages → Create → Pages →
   Connect to Git** → elegir el repo. Build command: *(vacío)*.
   Output directory: `/`.

3. En **Custom domains** de ese proyecto Pages, agregar `ingetrazo.com`
   (y `www.ingetrazo.com`). Cloudflare configura el DNS solo si el dominio
   ya está en la cuenta; si lo compraste en otro registrador, apuntar los
   nameservers a Cloudflare primero.

## Cada cambio después

```bash
git add . && git commit -m "..." && git push
# ~30 segundos y queda live
```

## Checklist post-publicación

- [ ] Verificar OG banner: compartir la URL en WhatsApp/Facebook
      (si sale caché vieja: Facebook Sharing Debugger → Scrape Again).
- [ ] `https://ingetrazo.com/robots.txt` y `/sitemap.xml` responden.
- [ ] Registrar en Google Search Console.
- [ ] Activar Cloudflare Web Analytics (sin cookies) si se desea.
