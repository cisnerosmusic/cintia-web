# cintia-web

Sitio personal de **Cintia Becerra**, maestra de piano en Miami.

🌐 **Live:** [cintiamusic.com](https://cintiamusic.com)

## Sobre el sitio

Una sola página, bilingüe (ES/EN), pensada como carta de presentación profesional. Tipografía editorial, paleta cálida, cero dependencias pesadas y ningún dominio de terceros en la carga.

## Stack

- HTML estático con CSS y JavaScript en un único archivo. Sin frameworks, sin build step, sin npm.
- Tipografía auto-hospedada en `fonts/`: Cormorant Garamond (redonda e itálica) e Inter, en `woff2` con subset latino, `font-display: swap` y `preload`. No se llama a Google Fonts.
- Toggle ES/EN con detección automática del idioma del navegador y persistencia en `localStorage`.
- JSON-LD `Person` schema, `canonical`, `hreflang` y Open Graph con imagen propia (`og-image.png`, 1200x630).
- Contraste AA verificado.
- `llms.txt` para crawlers de modelos de lenguaje (Claude, ChatGPT, Perplexity, etc.).
- Desplegado en GitHub Pages con HTTPS forzado y dominio propio.

## Estructura

```
cintia-web/
├── index.html                          Sitio completo (HTML, CSS y JS en un archivo)
├── fonts/                              Tipografías auto-hospedadas
│   ├── cormorant-garamond.woff2
│   ├── cormorant-garamond-italic.woff2
│   └── inter.woff2
├── og-image.png                        Imagen para redes sociales (1200x630)
├── robots.txt                          Permite indexación de buscadores y crawlers de IA
├── sitemap.xml                         Mapa del sitio para buscadores
├── llms.txt                            Resumen estructurado para modelos de lenguaje
├── humans.txt                          Créditos y guiño humano
├── google85530d12f607d7f9.html         Verificación de Google Search Console (no borrar)
├── .nojekyll                           Evita el procesamiento de Jekyll en GitHub Pages
├── CNAME                               Dominio personalizado: cintiamusic.com
└── README.md
```

## Peso

La primera carga son `index.html` (22 KB) más las tres tipografías (110 KB): unos 132 KB en total, sin peticiones a dominios externos. `og-image.png` solo lo descargan los rastreadores de redes sociales.

## Desarrollo local

No hay build. Para previsualizar:

```bash
# Opción 1: abrir directamente
start index.html

# Opción 2: servidor local con Python (recomendado, las fuentes se sirven bien)
python -m http.server 8000
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

- **Google Search Console:** propiedad verificada por archivo HTML en la raíz (`google85530d12f607d7f9.html`). Google exige que ese archivo siga accesible, así que no se borra ni se renombra.
- **Sitemap:** enviar o reenviar `https://cintiamusic.com/sitemap.xml` desde Search Console tras cambios de contenido, y actualizar el `lastmod` cuando el contenido cambie de verdad.
- **Bing Webmaster Tools:** se puede importar la propiedad directamente desde Search Console.
- **Crawlers de IA:** verificar que `https://cintiamusic.com/llms.txt` siga accesible.

## Créditos

Desarrollado por [Index01](https://index01.net) para Cintia.

## Licencia

Contenido y diseño © Cintia Becerra. Todos los derechos reservados.
