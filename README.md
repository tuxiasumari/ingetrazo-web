# IngeTrazo · Landing Page

Sitio web público de **IngeTrazo** — modelador 3D libre para ingeniería y
arquitectura, desarrollado por Ing. Marco Sumari.

URL en producción: **https://ingetrazo.com**

Repo del producto (código fuente, GPL-3.0):
[github.com/tuxiasumari/ingetrazo](https://github.com/tuxiasumari/ingetrazo)

## Stack

HTML + CSS + JS vanilla, sin build step — el mismo patrón que
`ingepresupuestos-web`. Pensado para Cloudflare Pages (deploy automático
con `git push`).

## Probar en local

```bash
cd ~/ingetrazo-web
python3 -m http.server 8765
# abrir http://localhost:8765
```
