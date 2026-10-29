# Roymar

Landing en HTML5, CSS3 y JavaScript vanilla. Abrir `index.html` con Live Server. Sin instalación ni compilación. Repositorio: https://github.com/pabloldl/roymar . Se mantiene `noindex, nofollow`; no se ha configurado un despliegue.

## Archivos

- `index.html`: contenido, navegación, ubicación y metadatos. Una única etiqueta `noindex, nofollow`.
- `styles.css`: identidad, responsive, foco visible y movimiento reducido.
- `script.js`: gestión de foco al navegar a los destinos internos. Navegación directa, sin menú desplegable.
- `assets/favicon.svg`: monograma de la identidad propuesta.
- `assets/verduras.webp`, `assets/pan.webp`, `assets/patatas.webp`: fotografías locales WebP. `mesa.webp` queda sin utilizar tras la corrección fotográfica.
- `.gitignore`: exclusión de archivos locales y carpeta de pruebas `.qa/`.
- `.qa/server.cjs`, `.qa/check.cjs`: herramientas de comprobación sin dependencias, no necesarias para Live Server.
- `.qa/results.json`, `.qa/view-375.png`, `.qa/view-1440.png`: resultados y capturas de revisión.

## Dirección del rediseño

Escaparate gráfico en azul tinta, amarillo mantequilla y blanco roto, con acento teja. Rotulación condensada de gran formato, módulos unidos por líneas y fotografía de pan integrada en la portada. Después: apuntes visuales de alimentación, presentación breve del comercio y cierre con la dirección protagonista. En móvil, el escaparate conserva dos columnas y el módulo de ubicación pasa a una franja horizontal; las fotografías editoriales permanecen en dos columnas. Sin tarjetas flotantes, degradados ni apariciones al hacer scroll. El rótulo tiene una única animación breve, desactivada con movimiento reducido. Se conservan las fotografías locales y el `.gitignore`.

## Fotografías y licencia

Fuente: Unsplash. Licencia consultada el 29 de octubre de 2026: https://unsplash.com/license . Permite descarga y uso comercial; no permite revender imágenes sin modificación significativa ni crear un servicio competidor con ellas.

Se descargaron con conversión WebP, ancho máximo 1400 px y calidad 78–82. Son composiciones ilustrativas, no fotografías del local ni un catálogo confirmado.

| Archivo | Contenido | Fuente descargada |
| --- | --- | --- |
| `assets/verduras.webp` | Cesta de verduras, por leonie wise | https://images.unsplash.com/photo-1418669112725-fb499fb61127?auto=format&fit=crop&w=1400&h=953&q=78&fm=webp |
| `assets/pan.webp` | Panes y espigas | https://images.unsplash.com/photo-1509440159596-0249088772ff?auto=format&fit=crop&w=1400&q=82&fm=webp |
| `assets/patatas.webp` | Detalle de patatas | https://images.unsplash.com/photo-1518977676601-b53f82aba655?auto=format&fit=crop&w=1400&q=82&fm=webp |

## Datos y límites

Corrección fotográfica: solo se sustituyó el plato preparado (`mesa.webp`) por una cesta de verduras (`verduras.webp`, 1400 × 953, 157274 bytes), más adecuada para ilustrar una compra cotidiana. Fuente y licencia comercial gratuita verificadas: https://unsplash.com/photos/NLU117HCVuc y https://unsplash.com/license . Se conservaron pan y patatas. En el HTML solo cambiaron la ruta y el texto alternativo de esa imagen; dimensiones, lazy loading y textos visibles se mantienen. CSS y JavaScript permanecen idénticos. Comprobaciones repetidas a 375, 768, 1440 y 1920 px, con capturas revisadas en móvil y escritorio.

Nombre, actividad y dirección proceden del encargo: Roymar, tienda de alimentación, Avenida Diputación, 5, 11670 El Bosque, Cádiz, España. No se han añadido teléfono, WhatsApp, correo, horarios, redes sociales, servicios, precios, reseñas ni surtido no confirmado.

Pendientes de confirmar si se desea ampliar la web: horarios, contacto oficial, productos disponibles, fotografías reales e identidad oficial. La identidad actual es una propuesta de diseño.

## Verificación realizada

Comprobaciones repetidas tras el rediseño en Chrome headless: 375, 768, 1440 y 1920 px; sin scroll horizontal, tres imágenes cargadas, anclas válidas, una etiqueta robots, sin enlaces telefónicos, sin errores de JavaScript ni recursos con error HTTP. Navegación directa visible en móvil. Foco sobre el destino al activar el enlace de ubicación comprobado. Movimiento reducido y desactivación de la animación tipográfica comprobados. Sintaxis de JavaScript comprobada con `node --check`. Capturas revisadas a 375 y 1440 px; evidencias actualizadas en `.qa/`.

El enlace de Google Maps utiliza la dirección proporcionada y el formato de búsqueda con `api=1`; no se verificó una ruta ni un marcador exacto en el servicio externo. Safari/iPhone no se ha ejecutado y requiere comprobación en dispositivo real. No se han realizado commits, pushes ni despliegues.

Para repetir las comprobaciones técnicas: ejecutar `node .qa/server.cjs`, iniciar Chrome headless con depuración remota en puerto 9248 y ejecutar `node .qa/check.cjs`. El comprobador cierra la instancia de Chrome conectada al terminar.
