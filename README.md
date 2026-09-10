# Tónico Y&M — Landing Page

Landing page de la tienda oficial **Tónico Y&M** (cuidado botánico y dermatológico), generada con [Google Stitch](https://stitch.withgoogle.com/) y exportada como HTML estático con Tailwind CSS (vía CDN).

## Estructura del proyecto

```
.
├── index.html            # Página completa de la landing (única página del sitio)
├── assets/
│   └── images/
│       └── logotipo.png  # Logo del sitio, servido localmente (ver nota abajo)
├── docs/
│   ├── DESIGN.md         # Sistema de diseño (paleta de colores, tipografías) usado en Stitch
│   └── previews/         # Capturas de referencia generadas por Stitch durante el diseño
└── README.md
```

> La mayoría de las imágenes de la página (`index.html`) se cargan desde una CDN externa (`lh3.googleusercontent.com/aida-public/...`), pública y estable. El **logotipo** es la excepción: la exportación original de Stitch usaba una URL privada de sesión (`.../aida/...`, sin "-public") que deja de funcionar para cualquiera fuera de esa sesión, por eso se sirve localmente desde `assets/images/logotipo.png`. Las imágenes en `docs/previews/` son solo referencias visuales del proceso de diseño en Stitch, no assets consumidos por la página.

## Ejecutar en local

No requiere instalación de dependencias: es un único archivo HTML. Basta con servirlo con cualquier servidor estático, por ejemplo:

```bash
# Con Python 3
python -m http.server 8000

# o con Node (npx)
npx serve .
```

Luego abre [http://localhost:8000](http://localhost:8000) en el navegador.

También puedes abrir `index.html` directamente con doble clic, aunque servirlo por HTTP evita posibles restricciones del navegador con recursos externos.
