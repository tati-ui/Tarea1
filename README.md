# tarea 1 - programación web avanzada

## identificación

**estudiante:** tatiana solis quesada  
**carné:** 207490238  
**curso:** soft-12 - programación web avanzada  
**tarea:** tarea 1 - html5 y css3  

---

## descripción del proyecto

este proyecto corresponde a la tarea 1 del curso programación web avanzada.

el objetivo es desarrollar dos interfaces web utilizando html5 y css3, aplicando estructura semántica, accesibilidad, box model, posicionamiento, flexbox, css grid, diseño mobile first, media queries, unidades relativas y variables css.

los dos casos fueron desarrollados como soluciones visualmente diferentes de acuerdo con las necesidades de cada contexto.

---

# caso 1 - centro de control de expedición científica

el primer caso consiste en un centro de control para una expedición científica realizada en un área protegida de costa rica.

la interfaz funciona como un dashboard que permite consultar de forma simultánea información relacionada con:

- resumen general de operaciones.
- misiones científicas.
- equipos de investigación.
- alertas operativas.
- próximas actividades.

se incluyeron cinco misiones con información sobre equipo responsable, ubicación, horario, prioridad y estado.

también se presentan cuatro equipos científicos: biología, hidrología, meteorología y geología.

las alertas utilizan diferentes niveles de importancia y combinan información textual con elementos visuales, evitando que el significado dependa únicamente del color.

---

## decisiones de diseño del caso 1

### estructura semántica

se utilizaron elementos semánticos de html5 como `header`, `nav`, `main`, `section`, `article`, `footer` y `time`.

la jerarquía de encabezados comienza con un único `h1` para identificar la expedición. cada sección principal utiliza `h2` y los componentes internos utilizan `h3`.

esto permite mantener una estructura lógica y facilita la comprensión del documento.

### css grid

css grid se utiliza para construir la estructura principal del centro de control y para organizar las tarjetas.

en teléfono la interfaz utiliza principalmente una columna.

en tablet el contenido comienza a distribuirse en dos columnas.

en escritorio se utiliza una estructura multizona mediante `grid-template-areas`, permitiendo mostrar simultáneamente misiones, equipos, alertas y agenda.

### flexbox

flexbox se utiliza para problemas de distribución unidimensional.

por ejemplo, se utiliza en la navegación, en la organización horizontal del encabezado en escritorio y dentro de componentes específicos.

### position

se utiliza `position: sticky` en el encabezado para mantener disponible la navegación mientras el usuario consulta el centro de control.

se utiliza `z-index` de forma controlada para mantener el encabezado sobre el contenido sin utilizar posicionamiento como sustituto de grid o flexbox.

también se utiliza `scroll-margin-top` para evitar que el encabezado sticky cubra los títulos cuando se utilizan los enlaces internos.

### accesibilidad

la interfaz utiliza `lang="es"` y una jerarquía lógica de encabezados.

los enlaces de navegación cuentan con estados de foco visibles para facilitar la navegación mediante teclado.

los estados, prioridades y niveles de alerta se indican mediante texto. el color se utiliza únicamente como apoyo visual y no como única forma de transmitir información.

---

# caso 2 - festival cultural raíces 2026

el segundo caso corresponde a un panel de consulta para el festival cultural raíces 2026.

a diferencia del centro de control científico, esta interfaz fue diseñada pensando principalmente en una consulta rápida desde dispositivos móviles.

la interfaz incluye:

- actividades que están ocurriendo en este momento.
- próximas actividades.
- cuatro espacios del festival.
- cambios de programación.
- servicios disponibles para los visitantes.

la sección "ahora" tiene una prioridad visual mayor para permitir que el usuario identifique rápidamente las actividades que se encuentran en desarrollo.

---

## decisiones de diseño del caso 2

### mobile first

el caso 2 fue desarrollado siguiendo un enfoque mobile first.

los estilos base corresponden a pantallas pequeñas y posteriormente se agregan media queries con `min-width` para reorganizar la interfaz en tablet y escritorio.

esto permite priorizar la información más importante en teléfonos y aprovechar progresivamente el espacio disponible en pantallas mayores.

### css grid

grid se utiliza para organizar componentes como los espacios, servicios y la estructura general del contenido.

el número de columnas cambia según el ancho disponible.

en escritorio la estructura principal se reorganiza para mostrar distintas secciones simultáneamente.

### flexbox

flexbox se utiliza en la navegación y en la programación de actividades.

esto permite distribuir elementos en una dimensión y controlar propiedades como dirección, separación y alineación.

### position

se utiliza `position: sticky` en el encabezado para mantener visible la información principal y la navegación durante el desplazamiento.

se utiliza `z-index` de forma controlada para mantener el encabezado sobre el contenido.

el uso de `position` responde a una necesidad de navegación y no sustituye los sistemas principales de layout como grid o flexbox.

también se utiliza `scroll-margin-top` para evitar que el encabezado sticky cubra los títulos de las secciones cuando se utilizan los enlaces internos.

### diferenciación visual

los dos casos utilizan soluciones visuales diferentes.

el caso 1 utiliza una apariencia asociada con un centro de control científico y prioriza la visualización simultánea de información operativa.

el caso 2 utiliza una identidad más cálida y cultural, priorizando la consulta rápida de actividades desde dispositivos móviles.

---

# diseño responsive

el proyecto utiliza un enfoque mobile first.

se utilizaron como referencias principales los siguientes puntos de cambio:

- teléfono: estilos base hasta 600 px.
- tablet: desde 601 px.
- escritorio: desde 1024 px.

las media queries no se utilizan únicamente para aumentar tamaños. también modifican la distribución y el número de columnas del contenido.

los diseños fueron revisados aproximadamente en 375 px, 768 px y 1440 px para comprobar su comportamiento en teléfono, tablet y escritorio.

---

# box model

se utiliza:

```css
* {
    box-sizing: border-box;
}
```

esto permite que el ancho de los componentes incluya correctamente `padding` y bordes, facilitando el control de las dimensiones.

las tarjetas utilizan de manera consistente propiedades como `padding`, `border`, `margin`, `gap` y `border-radius`.

también se utilizan reglas como `min-width: 0` y `minmax(0, 1fr)` para reducir el riesgo de desbordamientos dentro de grid.

---

# cascada y especificidad

las hojas de estilo fueron organizadas por bloques funcionales.

se utilizan principalmente clases reutilizables y selectores simples.

se evitó el uso de `!important` y se mantuvo una especificidad controlada para aprovechar correctamente la cascada de css.

las media queries aparecen después de los estilos base y modifican las propiedades necesarias para cada tamaño de pantalla.

---

# unidades relativas

se utilizan unidades relativas como:

- `rem` para tamaños, espacios, bordes y anchos máximos.
- `em` en componentes pequeños como las etiquetas de estado.
- `%` para dimensiones relativas.
- `fr` para la distribución de columnas mediante css grid.
- `clamp()` para adaptar algunos tamaños tipográficos.

esto permite que las interfaces se adapten mejor a diferentes tamaños de pantalla.

---

# variables css

ambos casos utilizan variables definidas dentro de `:root`.

las variables permiten centralizar valores relacionados con:

- colores.
- fondos.
- texto.
- espacios.
- bordes.
- radios.
- sombras.
- anchos máximos.

esto permite mantener un sistema visual consistente y facilita modificaciones posteriores.

---

# estructura del proyecto

```text
tarea1/
│
├── caso1/
│   ├── css/
│   │   └── estilos.css
│   ├── img/
│   └── index.html
│
├── caso2/
│   ├── css/
│   │   └── estilos.css
│   ├── img/
│   └── index.html
│
└── README.md
```

---

# instrucciones para abrir el proyecto

1. descargar o clonar el repositorio.
2. abrir la carpeta del proyecto en visual studio code.
3. ingresar a la carpeta `caso1` o `caso2`.
4. abrir el archivo `index.html` correspondiente en un navegador web.
5. opcionalmente se puede utilizar una extensión como live server para visualizar los cambios durante el desarrollo.

el proyecto utiliza únicamente html5 y css3, por lo que no requiere instalación de dependencias.

---

# historial de desarrollo

el proyecto fue desarrollado mediante commits progresivos para registrar diferentes etapas del trabajo.

| n.º | fecha | hash | mensaje | caso | cambio realizado |
|---:|---|---|---|---|---|
| 1 | 2026-09-19 | `073fd75` | crea estructura inicial del proyecto | general | creación de la estructura inicial de carpetas y archivos |
| 2 | 2026-09-19 | `412740e` | agrega contenido y estilos base del caso 1 | caso 1 | incorporación de la estructura y estilos iniciales del centro de control |
| 3 | 2026-09-19 | `7085585` | implementa diseño responsive y accesibilidad del caso 1 | caso 1 | incorporación de adaptabilidad responsive y mejoras de accesibilidad |
| 4 | 2026-09-20 | `24f72bf` | crea interfaz responsive del festival cultural | caso 2 | desarrollo de la interfaz mobile first del festival |
| 5 | 2026-09-20 | `446d860` | mejora posicionamiento y navegacion del caso 2 | caso 2 | ajustes de posicionamiento y navegación |
| 6 | 2026-09-20 | `038c365` | mejora accesibilidad y estados visuales del caso 1 | caso 1 | incorporación de estados, prioridades y mejoras visuales y de accesibilidad |

> esta tabla documenta los commits existentes antes de la incorporación inicial de este readme. el historial completo y actualizado puede consultarse directamente mediante git.

---

# conclusión

el proyecto aplica los conceptos principales estudiados en html5 y css3 mediante dos interfaces con objetivos diferentes.

el centro de control científico prioriza la visualización simultánea de información operativa, mientras que el festival cultural prioriza una consulta rápida desde dispositivos móviles.

en ambos casos se aplican estructura semántica, accesibilidad, box model, flexbox, css grid, posicionamiento, diseño responsive, media queries, unidades relativas y variables css.
