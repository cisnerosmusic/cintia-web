# cintia-web

Sitio personal de **Cintia Becerra**, maestra de piano en Miami.

🌐 **Live:** [cintiamusic.com](https://cintiamusic.com)

## Sobre el sitio

Una página simple, bilingüe (ES/EN) y sin imágenes, pensada como carta de presentación profesional. Tipografía editorial, paleta cálida, cero dependencias pesadas.

## Stack

- HTML estático con CSS y JavaScript en un solo archivo.
- Sin frameworks, sin build step, sin npm.
- Tipografía: Cormorant Garamond + Inter (Google Fonts).
- Toggle ES/EN con detección automática del idioma del navegador y persistencia en `localStorage`.
- JSON-LD `Person` schema para SEO.
- Desplegado en GitHub Pages.

## Estructura

```
cintia-web/
├── index.html      Sitio completo (HTML, CSS y JS en un archivo)
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

Configuración de `cintiamusic.com` en el registrador del dominio:

| Tipo  | Host  | Valor                        |
|-------|-------|------------------------------|
| A     | @     | 185.199.108.153              |
| A     | @     | 185.199.109.153              |
| A     | @     | 185.199.110.153              |
| A     | @     | 185.199.111.153              |
| CNAME | www   | cisnerosmusic.github.io      |

Después del primer despliegue con el dominio personalizado, activar **Enforce HTTPS** en `Settings → Pages` (puede tardar 24 horas en estar disponible).

## Licencia

Contenido y diseño © Cintia Becerra. Todos los derechos reservados.
