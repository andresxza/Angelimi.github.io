---
name: "Carta para Angeli"
description: "Un folio editorial para desplegar una carta personal, escena por escena."
colors:
  paper: "#1c201b"
  paper-soft: "#252a23"
  paper-raised: "#2d322a"
  ground: "#10120f"
  ink: "#f2eee4"
  accent: "#d97b6d"
  accent-action: "#733a33"
  olive: "#a1ae89"
  olive-action: "#526143"
  rule: "#4b5146"
typography:
  display:
    fontFamily: "Instrument Serif, Georgia, serif"
    fontSize: "clamp(3.2rem, 7vw, 5.3rem)"
    fontWeight: 400
    lineHeight: 0.9
  body:
    fontFamily: "DM Sans, system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
  reading:
    fontFamily: "Libre Baskerville, Georgia, serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.8
rounded:
  square: "0px"
  seal: "50%"
spacing:
  page-edge: "12px"
  scene-gutter: "clamp(28px, 6vw, 84px)"
  section-gap: "12px"
components:
  button-primary:
    backgroundColor: "{colors.olive-action}"
    textColor: "{colors.ink}"
    rounded: "{rounded.square}"
    padding: "10px 18px"
    height: "44px"
  button-primary-hover:
    backgroundColor: "{colors.accent-action}"
    textColor: "{colors.ink}"
  chapter-current:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.paper}"
    rounded: "{rounded.square}"
    width: "36px"
    height: "34px"
---

# Design System: Carta para Angeli

## Overview

**Creative North Star: "El folio que se despliega en la penumbra."**

La carta se siente como un pequeño objeto editorial: hojas de carbón cálido, texto marfil y acentos apagados de terracota y oliva. La oscuridad acompaña la intimidad de una sorpresa personal sin competir con las palabras ni con las fotografías.

Cada escena conserva la lógica de una página del mismo folleto. Una guía numerada en el margen orienta la lectura; el sobre y su sello marcan el momento de entrada. En pantallas estrechas, la portada se convierte en una secuencia vertical.

**Key Characteristics:**
- Papel carbón mate, reglas finas y superficies planas con contraste alto.
- Serif editorial para nombres y títulos; sans legible para controles.
- Terracota y oliva usados como señales, no como fondos decorativos.
- Animación abundante en aperturas, giros, revelados y respuestas al toque; sin bucles ambientales.

## Colors

El carbón cálido, el texto marfil y dos acentos moderados mantienen el tono íntimo y editorial.

### Primary
- **Terracota** (`accent`): sello, pliegue del sobre y acciones que deben atraer la mirada.
- **Oliva claro** (`olive`): navegación, texto de apoyo y detalles florales.
- **Oliva profundo** (`olive-action`): botones principales con texto marfil.

### Neutral
- **Papel** (`paper`): hojas de carbón y superficies de lectura.
- **Fondo** (`ground`): espacio exterior alrededor de cada hoja.
- **Tinta** (`ink`): texto marfil principal.
- **Regla** (`rule`): bordes y divisiones discretas.

**The Accent-Sparing Rule.** Reserva los acentos para acciones y detalles narrativos; no conviertas una escena completa en una superficie de color. El texto secundario conserva contraste legible sobre las superficies oscuras.

## Typography

**Display Font:** Instrument Serif (Georgia, serif)  
**Body Font:** DM Sans (system-ui, sans-serif)  
**Reading Font:** Libre Baskerville (Georgia, serif)

**Character:** La serif aporta el ritmo de una carta impresa; la sans mantiene controles y navegación directos. Libre Baskerville da a los pasajes largos una textura de lectura distinta sin cambiar la voz de la carta.

### Hierarchy
- **Display** (400, `clamp(3.2rem, 7vw, 5.3rem)`, 0.9): nombre de la portada.
- **Headline** (400, `clamp(2.5rem, 5.6vw, 5rem)`, 0.95): títulos de escena.
- **Body** (400, 16px, 1.6): texto de interfaz y explicación breve.
- **Reading** (400, 1rem, 1.8): pasajes y carta.
- **Label** (500, 0.78rem): índice, pequeñas indicaciones y etiquetas.

**The Two-Voice Rule.** Usa Instrument Serif para los momentos principales y DM Sans para la interfaz; no añadas otra fuente de exhibición.

## Layout

La página se lee como una sucesión de hojas en un contenedor desplazable, con un número de escena en el margen izquierdo y un marco centrado. En escritorio, la portada reparte el espacio entre nombre y sobre a la izquierda y una fotografía a la derecha. A 640px o menos, título, fotografía y sobre se apilan en ese orden. Mantén iguales los márgenes de cada escena y deja que el contenido respire dentro de la hoja.

## Elevation & Depth

La profundidad se expresa mediante el borde del papel, la superposición física del sobre y una sombra suave bajo ese objeto. Las demás superficies permanecen planas; no uses halos, resplandores ni sombras duras como decoración.

**The Flat-By-Default Rule.** Reserva la sombra para separar el sobre abierto del papel; el resto de la jerarquía se construye con espacio, contraste y tipografía.

## Shapes

Predominan las esquinas cuadradas y los contornos finos. El sello es el único círculo deliberado; conserva la geometría del pliegue para que el sobre se lea como papel doblado y no como una tarjeta de aplicación.

## Components

### Buttons
- **Shape:** rectangular, sin radio.
- **Primary:** fondo oliva profundo, texto marfil y área táctil de al menos 44px.
- **Hover / Focus:** el fondo pasa a terracota profunda; el foco usa un contorno visible y separado.

### Cards / Containers
- **Background:** papel dentro de la hoja; fondo neutro fuera.
- **Border:** regla fina, sin paneles anidados ni esquinas redondeadas.
- **Shadow Strategy:** plana por defecto; la sombra suave se limita a elementos físicos como el sobre.

### Navigation
- **Style:** índice vertical de escenas, alineado al margen izquierdo.
- **State:** la escena activa se distingue con el acento y texto claro; las demás quedan discretas y legibles.
- **Mobile:** mantiene el margen lateral y no cubre el contenido de la portada.

### Signature Component: Sealed Envelope
El sobre usa una base oliva profunda, un pliegue terracota y un sello circular. Al activarlo, la tarjeta interior sube y muestra el nombre de la destinataria; conserva esa secuencia y el control accesible.

### Motion
Las transiciones dan respuesta a las acciones: entrada inicial de portada, pliegues de los sobres, giro de fotos, apertura del abanico, crecimiento de flores, parpadeo al tocar los ojos, escritura de la carta y celebración del regalo. Las partículas solo aparecen tras una interacción y se detienen al terminar. No hay flotación, pulso ni brillo en bucle; `prefers-reduced-motion` elimina el desplazamiento animado y mantiene el contenido visible.

## Do's and Don'ts

### Do:
- **Do** mantener el nombre, las fotografías y la carta como protagonistas de cada escena.
- **Do** reutilizar los tokens carbón, marfil, terracota y oliva en todos los capítulos.
- **Do** conservar el orden de título, fotografía y sobre en la portada móvil.

### Don't:
- **Don't** añadir brillos, gradientes ornamentales o efectos de luz al carbón mate.
- **Don't** redondear las hojas ni convertir las escenas en una cuadrícula de tarjetas.
- **Don't** introducir colores o tipografías de exhibición nuevos sin una dirección aprobada.
