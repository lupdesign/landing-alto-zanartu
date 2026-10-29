# Reglas de Diseño y Marca — Landing Alto Zañartu

Estas reglas deben aplicarse de forma consistente en todas las secciones y versiones de la landing page de **Alto Zañartu** (Constructora Vector / Comercializa OneKey).

## 1. Paleta de Colores Oficial
- **Amarillo principal de marca (Botones y acentos)**: `#E29E05` (hover en un tono más claro `#e5b75c`).
- **Fondo amarillo claro (Sección FAQ / acentos suaves)**: `#FAF1DA`.
- **Tinta principal (Textos y títulos)**: `#000000`.
- **Gris secundario (Subtítulos, eyebrows y textos de apoyo)**: `#666666`.
- **Superficie / Fondo claro**: `#EFEFEF` y `#FFFFFF`.

## 2. Tipografía Local y Escala de Títulos
- **Títulos y encabezados (`.section-title`)**: `'Roboto Condensed', sans-serif` (archivos locales en `fuentes/Roboto condensada/`).
  - Respetar el uso de minúsculas/tipo oración en subtítulos o bajadas de titular cuando se indique, destacando en **MAYÚSCULAS** la(s) palabra(s) clave de cada título de sección (ej. `ALTO ZAÑARTU`, `LA FLORIDA`, `UN ACTIVO INMOBILIARIO`, `ESPACIOS`, `BOUTIQUE`, `SIMPLE`, `DUDAS`, `CONECTIVIDAD & PLUSVALÍA`, `INVIERTE`).
  - **Escala unificada de títulos de sección** (excepto el Hero): `font-size: clamp(2.15rem, 3.8vw, 3.25rem); font-weight: 700; line-height: 1.06; letter-spacing: -0.015em;`.
  - No incluir punto final (`.`) ni dos puntos (`:`) innecesarios al terminar los títulos de sección.
- **Cuerpo, párrafos, formularios y navegación (`.section-copy`, `.section-nav`)**: `'Work Sans', sans-serif` (archivos locales en `fuentes/Work_Sans/`).

## 3. Botones, Bordes (`border-radius`) e Iconografía
- **Bordes redondeados consistentes**:
  - Botones y píldoras de navegación: `border-radius: 999px` (`--radius-pill`).
  - Tarjetas y contenedores (como formularios): `border-radius: 22px` (`--radius-card`).
  - Campos de entrada (`input`, `select`, `textarea`): `border-radius: 12px` (`--radius-input`).
- **Botones limpios**:
  - Usar color de fondo `#E29E05`, hover `#e5b75c` y texto `#000000`.
  - **PROHIBIDO** incluir iconos, flechas SVG, emojis o elementos decorativos dentro de los botones de acción; usar únicamente texto plano.
  - Los botones redondos de control de carrusel (como las flechas de Tipologías) también usan fondo `#E29E05` y hover `#e5b75c`.

## 4. Limpieza Visual, Etiquetas y Formularios
- **Eyebrows / Tags sobre títulos**: Mostrar únicamente como texto plano limpio (`color: #666666`), sin fondos de color, sin bordes laterales ni cajas contenedoras.
- **Formularios**:
  - Contenedores ligeros y de alta transparencia (ej. `background: rgba(255, 255, 255, 0.38)` con `backdrop-filter: blur(8px)`) cuando estén sobre imagen o video para no tapar el fondo.
  - Etiquetas (`<label>`) siempre en peso regular (`font-weight: 400`).

## 5. Arquitectura de Componentes y Secciones (Referencia `index.html`)
1. **Header fijo (`#siteHeader`)**:
   - Debe ubicarse siempre en la raíz de `<body>` (fuera de `.hero-frame`) con `z-index: 9999` para mantenerse por encima de todas las secciones.
   - Muestra `assets/logos/logotipo.svg` arriba y cambia suavemente a `assets/logos/ISOTIPO.svg` (sin máscara ni contenedor) al hacer scroll (`height: 57px` en escritorio, `36px`/`47px` en móvil).
2. **Sección Tipologías (`#tipologias`)**:
   - Columna izquierda con indicador numérico lineal `1 2 3 4` (sin círculos amarillos), título, introducción, lista de características separadas por líneas horizontales, bloque de precio y botón de descarga de `Brochure.pdf`.
   - Columna derecha con carrusel de 4 tipologías (`D1 isometrico.jpg` a `D4 isometrico.jpg`) que avanza de 2 en 2, subtítulo `2D2B` en `Roboto Condensed` y tabla inferior con `Sup. Total` y `Sup. Útil`.
3. **Sección Galería (`#espacios`)**:
   - Carrusel con la imagen activa centrada dejando ver parte de la foto anterior a la izquierda y la siguiente a la derecha (*peek* con clones en los extremos), y controles mediante cuadros de miniaturas ubicados **debajo** de la imagen principal (nunca superpuestos).
4. **Sección Terminaciones (`#terminaciones`)**:
   - Título y párrafo ubicados arriba de la imagen vertical (`media/carrusel/render_16.jpg`, sin franjas superpuestas), e imagen igualada en altura al bloque derecho de `DETALLE DE TERMINACIONES`.
   - Acordeón exclusivo (`<details name="...">`, solo 1 abierto a la vez, iniciando con `Pisos` abierto), con iconos SVG de `36px`–`38px` en color `#E29E05` sin círculo contenedor ni animación, títulos de fila en peso regular (`400`), indicador `+` en negro (`#000000`) y `−` en gris claro (`#C2C2C2`) sin círculo.
5. **Sección Ubicación (`#ubicacion`)**:
   - Fondo blanco (`#FFFFFF`), columna izquierda con título en 3 líneas arriba y párrafo + botón abajo; columna derecha con el mapa (`media/mapa unicacion proyecto.png` / `.svg`) grande y libre (sin contenedor ni máscara); fila inferior de 3 columnas sin iconos con la descripción debajo de cada subtítulo.
6. **Sección Proceso de Compra (`#proceso`)**:
   - Grilla de 3 columnas × 2 filas con número grande arriba, línea divisoria horizontal, subtítulo y descripción alineados con `subgrid`, y elevación suave en hover (`translateY(-6px)`).
7. **Sección Preguntas Frecuentes (`#faq`)**:
   - Fondo en tono claro del amarillo principal (`#FAF1DA`) con tarjetas redondeadas individuales.
8. **Sección CTA Final (`#cta-final`) y Footer (`.site-footer`)**:
   - CTA Final con imagen `media/carrusel/render_8.jpg`, overlay negro translúcido, título en `#E29E05` y botón hacia `#contacto`.
   - Footer en fondo blanco (`#FFFFFF`), logos de Alto Zañartu (`assets/logos/logotipo.svg`), Constructora Vector (`media/logo vector .svg`) y OneKey (`media/logo onekey.svg` alineado a la izquierda con `COMERCIALIZA`), datos de contacto, texto monumental `ALTO ZAÑARTU` a todo el ancho (`cqi`) y barra de copyright.
