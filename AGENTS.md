# Reglas de Diseño y Marca — Landing Alto Zañartu

Estas reglas deben aplicarse de forma consistente en todas las secciones de la landing page de **Alto Zañartu** (Constructora Vector).

## 1. Paleta de Colores Oficial
- **Amarillo principal de marca (Botones y acentos)**: `#E29E05` (hover en un tono más claro `#e5b75c`).
- **Tinta principal (Textos y títulos)**: `#000000`.
- **Gris secundario (Subtítulos, eyebrows y textos de apoyo)**: `#666666`.
- **Superficie / Fondo claro**: `#EFEFEF` y `#FFFFFF`.

## 2. Tipografía Local
- **Títulos y encabezados (`.section-title`)**: `'Roboto Condensed', sans-serif` (archivos locales en `fuentes/Roboto condensada/`).
  - Respetar el uso de minúsculas/tipo oración en subtítulos o bajadas de titular cuando se indique (no forzar `text-transform: uppercase` en todo el título si lleva dos partes).
  - No incluir punto final (`.`) al terminar los títulos de sección.
- **Cuerpo, párrafos, formularios y navegación (`.section-copy`, `.section-nav`)**: `'Work Sans', sans-serif` (archivos locales en `fuentes/Work_Sans/`).

## 3. Botones, Bordes (`border-radius`) e Iconografía
- **Bordes redondeados consistentes**:
  - Botones y píldoras de navegación: `border-radius: 999px` (`--radius-pill`).
  - Tarjetas y contenedores (como formularios): `border-radius: 22px` (`--radius-card`).
  - Campos de entrada (`input`, `select`, `textarea`): `border-radius: 12px` (`--radius-input`).
- **Botones limpios**:
  - Usar color de fondo `#E29E05`, hover `#e5b75c` y texto `#000000`.
  - **PROHIBIDO** incluir iconos, flechas SVG, emojis o elementos decorativos dentro de los botones; usar únicamente texto plano.

## 4. Limpieza Visual, Etiquetas y Formularios
- **Eyebrows / Tags sobre títulos**: Mostrar únicamente como texto plano limpio (`color: #666666`), sin fondos de color, sin bordes laterales ni cajas contenedoras.
- **Formularios**:
  - Contenedores ligeros y de alta transparencia (ej. `background: rgba(255, 255, 255, 0.38)` con `backdrop-filter: blur(8px)`) cuando estén sobre imagen o video para no tapar el fondo.
  - Etiquetas (`<label>`) siempre en peso regular (`font-weight: 400`).
