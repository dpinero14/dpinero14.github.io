# dpinero14.github.io

La página de entrada de **Sur Analytics**: los laboratorios abiertos de datos sobre
hidrocarburos y minería, con el enlace a cada repositorio, a la página que se puede
abrir y a la lista de correo.

Se publica sola en <https://dpinero14.github.io> con GitHub Pages desde la rama `main`.

## Qué hay acá

| Archivo | Qué es |
|---|---|
| `index.html` | La página entera: estilos, contenido y el formulario de suscripción. Sin dependencias ni build. |
| `img/*.jpg` | Miniaturas de cada laboratorio, a 900 px de ancho. Salen de un cuadro de los videos o de una figura del repo. |

## Cómo se cambia

- **Sumar un laboratorio:** copiar un bloque `<article class="lab">` en `index.html`,
  cambiar número, título, texto y enlaces, y poner la miniatura en `img/`.
- **La lista de correo:** el `<iframe>` de la sección `#lista` apunta a
  `https://suranalytics.substack.com/embed`. Si la publicación de Substack usa otro
  subdominio, se cambia esa línea y listo.
- **Las miniaturas** se regeneran con el script `make_thumbs.py` (queda fuera del repo,
  en el scratchpad de trabajo): toma un cuadro del video de cada laboratorio con ffmpeg,
  lo lleva a 900 px y lo guarda como JPEG progresivo.

## Reglas

Las mismas que en el resto de la serie: datos públicos, código abierto, sin datos ni
rutas locales en lo que se publica, textos en castellano y nada de métricas infladas.
