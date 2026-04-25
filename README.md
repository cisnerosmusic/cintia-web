# cintia-web

Sitio personal de **Cintia Becerra**, maestra de piano en Miami.

🌐 **Live:** [cintiamusic.com](https://cintiamusic.com)

## Sobre el sitio

Una página simple y bilingüe (ES/EN), pensada como carta de presentación profesional. Tipografía editorial, paleta cálida, cero dependencias pesadas. El contenido visible se sostiene en tipografía y un ornamento musical en SVG; las imágenes se reservan para Open Graph (previsualización al compartir el link en redes y mensajería).

## Stack

- HTML estático con CSS y JavaScript en un solo archivo.
- Sin frameworks, sin build step, sin npm.
- Tipografía: Cormorant Garamond + Inter (Google Fonts).
- Toggle ES/EN con detección automática del idioma del navegador y persistencia en `localStorage`.
- JSON-LD `Person` schema para SEO.
- `hreflang` para indicar idiomas alternativos a buscadores.
- `llms.txt` para crawlers de modelos de lenguaje (Claude, ChatGPT, Perplexity, etc.).
- Desplegado en GitHub Pages con HTTPS forzado.

## Estructura

```
cintia-web/
├── index.html      Sitio completo (HTML, CSS y JS en un archivo)
├── og-image.png    Tarjeta Open Graph (1200x630) para previsualización al compartir
├── robots.txt      Permite indexación de buscadores y crawlers de IA
├── sitemap.xml     Mapa del sitio para buscadores
├── llms.txt        Resumen estructurado para modelos de lenguaje
├── humans.txt      Créditos y guiño humano
├── .nojekyll       Evita el procesamiento de Jekyll en GitHub Pages
├── CNAME           Dominio personalizado: cintiamusic.com
└── README.md
```

## Desarrollo local

No hay build. Para previsualizar:

```bash
# Opción 1: abrir directamente
open index.html

# Opción 2: servidor local con Python
python3 -m http.server 8000
# luego abrir http://localhost:8000
```

## Despliegue

GitHub Pages está configurado en `Settings → Pages`, sirviendo desde la rama `main`, carpeta raíz.

Cualquier push a `main` actualiza el sitio en vivo en aproximadamente un minuto.

## DNS

Configuración de `cintiamusic.com` en GoDaddy:

| Tipo  | Host  | Valor                        |
|-------|-------|------------------------------|
| A     | @     | 185.199.108.153              |
| A     | @     | 185.199.109.153              |
| A     | @     | 185.199.110.153              |
| A     | @     | 185.199.111.153              |
| CNAME | www   | cisnerosmusic.github.io      |

## SEO y discoverability

Tras el primer despliegue completo:

- Indexar manualmente en [Google Search Console](https://search.google.com/search-console) añadiendo la propiedad `cintiamusic.com` y enviando el sitemap.
- Indexar en [Bing Webmaster Tools](https://www.bing.com/webmasters).
- Verificar que `llms.txt` sea accesible en `https://cintiamusic.com/llms.txt` para los crawlers de IA.

## Licencia

Contenido y diseño © Cintia Becerra. Todos los derechos reservados.
