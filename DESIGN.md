---
name: ORBITA - Laboratorio de misiones espaciales
description: Interfaz espacial táctica y educativa para simulación y diseño de misiones espaciales (Space Apps)
colors:
  bg: "#101a22"
  panel: "#17242d"
  panel-2: "#1d2c36"
  line: "#344650"
  text: "#edf3ed"
  muted: "#a9b8b8"
  lime: "#d8f36a"
  cyan: "#68d6d1"
  orange: "#ffb36b"
  red: "#ff7777"
  green: "#9fdf9f"
typography:
  display:
    fontFamily: "Trebuchet MS, Verdana, sans-serif"
    fontSize: "2.2rem"
    fontWeight: 700
    lineHeight: 1.15
  body:
    fontFamily: "Trebuchet MS, Verdana, sans-serif"
    fontSize: "15px"
    lineHeight: 1.5
  telemetry:
    fontFamily: "Consolas, monospace"
    fontSize: "14px"
    fontWeight: 700
rounded:
  sm: "8px"
  md: "10px"
  lg: "14px"
  full: "9999px"
spacing:
  xs: "6px"
  sm: "10px"
  md: "18px"
  lg: "24px"
components:
  button-primary:
    backgroundColor: "{colors.lime}"
    textColor: "#152019"
    rounded: "{rounded.sm}"
    padding: "9px 13px"
  button-primary-hover:
    backgroundColor: "#e5ff83"
  button-secondary:
    backgroundColor: "{colors.panel-2}"
    textColor: "{colors.text}"
    rounded: "{rounded.sm}"
---

## Overview
ORBITA es una experiencia de simulación y diseño de misiones espaciales 2D inspirada en consolas de telemetría de la NASA y JPL. Su atmósfera visual transmite precisión científica, tecnología espacial y accesibilidad educativa.

## Colors
- **Superficie y Fondo**:
  - `bg` (`#101a22`): Espacio profundo, tono base de alta inmersión.
  - `panel` (`#17242d`): Contenedores principales de etapas y módulos.
  - `panel-2` (`#1d2c36`): Tarjetas interactivas y áreas de selección.
  - `line` (`#344650`): Bordes sutiles con contraste estructural definido.
- **Texto**:
  - `text` (`#edf3ed`): Blanco suave con alta legibilidad sobre fondos oscuros (contraste > 7:1).
  - `muted` (`#a9b8b8`): Metadatos, etiquetas secundarias y explicaciones.
- **Acentos y Semántica**:
  - `lime` (`#d8f36a`): Color primario de acción, confirmación y estados activos.
  - `cyan` (`#68d6d1`): Enlaces, telemetría orbital y foco secundario.
  - `orange` (`#ffb36b`): Alertas de recursos y límites operacionales.
  - `red` (`#ff7777`): Fallos críticos, consumo excesivo o alertas de aborto.
  - `green` (`#9fdf9f`): Parámetros óptimos y validaciones correctas.

## Typography
- **Jerarquía**:
  - Títulos principales (`clamp(25px, 3vw, 38px)`): Enérgicos, compactos (`letter-spacing: -0.035em`).
  - Encabezados de sección (21px - 23px): Claros, con espaciado superior balanceado.
  - Texto de cuerpo (14px - 15px): Lectura fluida sin fatiga visual.
  - Metadatos y etiquetas (12px - 13px): Legibles sin caer en micro-texto anti-patrón.
  - Telemetría (`Consolas, monospace`): Números con espaciado tabular (`font-variant-numeric: tabular-nums`).

## Layout
- Estructura de cabecera fija (*topbar*) con desenfoque de fondo (*backdrop-filter: blur(14px)*).
- Distribución en 2 columnas: Columna principal fluida para las etapas de la misión + panel lateral adhesivo (*sticky*) de telemetría de recursos.
- Navegación por etapas en cinta de pasos táctiles (*step-nav*).
- Diseño responsivo con puntos de ruptura a 1050px, 760px y 480px.

## Elevation & Depth
- Elevaciones limpias sin destellos artificiales: sombras suaves con dispersión amplia (`0 16px 42px #050b10a6`).
- Gradientes sutiles en paneles (`linear-gradient(145deg, #192832 0%, #17242d 55%)`).
- Bordes finos de 1px en `#344650` para definir la arquitectura espacial sin recargar.

## Shapes
- Radios consistentes de 8px a 14px según el tamaño del contenedor.
- Indicadores de estado en píldoras circulares (`status-chip`).
- Barras de progreso de recursos cilíndricas (`meter`).

## Components
- **Botones**: Altura mínima accesible (>= 42px) con estados de foco visibles (`outline: 3px solid var(--lime)`).
- **Tarjetas de Selección**: Feedback táctil en `:hover` (`transform: translateY(-2px)`) y selección en borde lima 2px con fondo resaltado.
- **Superficies del Navegador**: Barra de desplazamiento y selección de texto tematizadas con los tonos de la paleta.

## Do's and Don'ts
- **DO**: Mantener los números y cifras en `Consolas` con `tabular-nums` para evitar saltos de línea al actualizar telemetría.
- **DO**: Asegurar que todo texto secundario mantenga al menos 12px de tamaño para legibilidad en pantallas de alta densidad.
- **DON'T**: Usar degradados decorativos de texto o sombras duras sin desenfoque.
- **DON'T**: Anidar tarjetas dentro de tarjetas de forma redundante.
