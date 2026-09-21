
# Tarea 1 - Programación Web Avanzada

## Identificación

**Estudiante:** Tatiana Solis Quesada
**Carné:** 207490238
**Curso:** SOFT-12 - Programación Web Avanzada
**Sección:** SCV2
**Docente:** Álvaro Cordero Peña
**Tarea:** Tarea 1 - HTML5 y CSS3
**Fecha de entrega:** 20 de septiembre de 2026

---

## Descripción del proyecto

Este proyecto corresponde a la Tarea 1 del curso Programación Web Avanzada.

El objetivo es desarrollar dos interfaces web utilizando únicamente HTML5 y CSS3, aplicando estructura semántica, accesibilidad, modelo de caja, posicionamiento, Flexbox, CSS Grid, diseño mobile first, media queries, unidades relativas y variables CSS.

Los dos casos fueron desarrollados como soluciones visualmente diferentes según las necesidades de cada contexto.

- **Caso 1:** centro de control de una expedición científica.
- **Caso 2:** panel de consulta para un festival cultural.

El primer caso prioriza la visualización simultánea de información operativa, mientras que el segundo prioriza una consulta sencilla desde dispositivos móviles.

---

# Caso 1 - Centro de Control de Expedición Científica

## Descripción

El primer caso consiste en un centro de control para una expedición científica realizada en un área protegida de Costa Rica.

La interfaz funciona como un dashboard que permite consultar de forma simultánea:

- Resumen general de operaciones.
- Misiones científicas.
- Equipos de investigación.
- Alertas operativas.
- Próximas actividades.

Se incluyeron cinco misiones con información sobre equipo responsable, ubicación, horario, prioridad y estado.

También se presentan cuatro equipos científicos:

- Biología.
- Hidrología.
- Meteorología.
- Geología.

Las alertas utilizan diferentes niveles de importancia y combinan información textual con elementos visuales, evitando que su significado dependa únicamente del color.

## Decisiones de diseño del caso 1

El caso 1 fue diseñado como un centro de control en el que es importante observar varias categorías de información simultáneamente.

En teléfonos, el contenido se presenta principalmente en una sola columna para mantener la legibilidad. En tabletas comienza a distribuirse en dos columnas y, en escritorio, CSS Grid permite organizar las secciones principales en distintas zonas del dashboard.

La jerarquía visual permite diferenciar indicadores, misiones, equipos, alertas y agenda sin depender únicamente del color.

El encabezado utiliza posicionamiento `sticky` para mantener disponibles el nombre de la expedición y la navegación mientras el usuario consulta el dashboard. El nivel de apilamiento se controla mediante `z-index`.

Flexbox se utiliza en problemas de distribución unidimensional, mientras que CSS Grid se utiliza para las estructuras bidimensionales y la reorganización general del contenido.

---

# Caso 2 - Festival Cultural Raíces 2026

## Descripción

El segundo caso consiste en una interfaz pública para consultar la programación del Festival Cultural Raíces 2026.

La información se divide en:

- Actividades que ocurren en este momento.
- Programación de próximas actividades.
- Programación por escenarios.
- Cambios de programación.
- Servicios disponibles.

La sección **Ahora** recibe mayor importancia visual porque contiene la información más relevante para una persona que se encuentra consultando el festival durante el evento.

Cada actividad que se encuentra en curso presenta su horario, nombre, tipo, escenario y estado.

La programación de próximas actividades incluye hora, nombre, escenario y categoría.

La programación por escenarios se organiza en cuatro espacios principales:

- Escenario Central.
- Teatro.
- Zona Cultural.
- Zona Familiar.

Los horarios utilizan el elemento semántico `time`, permitiendo representar adecuadamente la información temporal.

## Decisiones de diseño del caso 2

El caso 2 fue diseñado con un enfoque de consulta móvil.

A diferencia del centro de control del caso 1, esta interfaz prioriza inicialmente una lectura vertical sencilla. Conforme aumenta el ancho disponible, las actividades, escenarios y servicios se distribuyen en más columnas.

El encabezado presenta el nombre del festival, fecha, ubicación y horario general para que la información principal esté disponible desde el inicio de la página.

La navegación permite acceder rápidamente a las secciones Ahora, Programación, Escenarios, Servicios e Información.

El encabezado y la navegación permanecen disponibles mediante posicionamiento `sticky`.

CSS Grid se utiliza principalmente en la programación por escenarios y en otras agrupaciones que requieren una distribución bidimensional.

Flexbox se emplea para estructuras unidimensionales como la navegación y distintos componentes de programación.

El resultado busca que la consulta sea rápida en teléfono y aproveche progresivamente el espacio adicional disponible en tableta y escritorio.

---

# HTML semántico y organización del contenido

Los dos casos utilizan elementos semánticos de HTML5 según el significado del contenido.

Entre los elementos utilizados se encuentran:

- `header` para los encabezados principales.
- `nav` para la navegación.
- `main` para el contenido principal.
- `section` para agrupar áreas temáticas.
- `article` para contenidos independientes.
- `footer` para la información final.
- `time` para representar horarios cuando corresponde.

Se mantiene una jerarquía lógica de encabezados:

- `h1` identifica la interfaz.
- `h2` identifica las secciones principales.
- `h3` identifica contenidos internos como actividades, misiones, equipos, escenarios o servicios.

Esta estructura permite comprender la organización general del contenido incluso sin aplicar CSS.

---

# Accesibilidad

Se aplicaron diferentes principios básicos de accesibilidad.

Los documentos utilizan `lang="es"` para identificar el idioma del contenido.

La navegación utiliza enlaces comprensibles y se incorporaron estados de foco visibles para facilitar la navegación mediante teclado.

Los estados, prioridades y alertas no dependen exclusivamente del color. También utilizan texto para comunicar su significado.

Se mantuvo una jerarquía coherente de encabezados y se buscaron niveles adecuados de contraste entre texto y fondo.

En el caso 1 se incorporó además la media query `prefers-reduced-motion`, que elimina el desplazamiento suave cuando el usuario tiene configurada una preferencia de movimiento reducido.

No se utilizaron imágenes informativas que requieran texto alternativo en las interfaces actuales.

---

# Modelo de caja

Se utiliza `box-sizing: border-box` para facilitar el control de las dimensiones de los elementos.

Los márgenes, rellenos, bordes y espacios se organizan mediante valores reutilizables y variables CSS.

También se establecieron límites de ancho para evitar que el contenido se extienda excesivamente en pantallas grandes.

Los componentes fueron diseñados para adaptarse al espacio disponible y evitar desbordamientos horizontales accidentales.

---

# Posicionamiento

El posicionamiento se utiliza únicamente cuando responde a una necesidad concreta y no como sustituto de Flexbox o CSS Grid.

Los encabezados utilizan `position: sticky` para conservar la navegación durante el desplazamiento de la página.

También se controla el nivel de apilamiento mediante `z-index`, evitando conflictos entre el encabezado y el resto del contenido.

Esta decisión permite mantener disponibles los principales controles de navegación sin alterar el flujo general de los documentos.

---

# Flexbox

Flexbox se utiliza para resolver distribuciones unidimensionales.

Entre sus aplicaciones se encuentran:

- Navegación.
- Alineación de elementos.
- Distribución de información dentro de componentes.
- Organización de actividades y programación.
- Manejo de dirección, separación y envoltura de elementos.

Su uso complementa a CSS Grid y evita depender de márgenes arbitrarios para construir el layout.

---

# CSS Grid

CSS Grid se utiliza para las estructuras bidimensionales de ambos casos.

En el caso 1 permite transformar el centro de control desde una distribución vertical para teléfonos hasta una estructura de varias zonas en escritorio.

En el caso 2 se utiliza principalmente para organizar la programación por escenarios y otras agrupaciones de contenido que aumentan su cantidad de columnas conforme existe más espacio disponible.

Las columnas y áreas cambian según el ancho de la pantalla, permitiendo que cada interfaz responda a su contexto.

---

# Diseño mobile first

Los estilos base fueron construidos para pantallas pequeñas.

A partir de esa base, las interfaces se amplían progresivamente mediante media queries.

En teléfono se prioriza una lectura principalmente vertical.

En tableta se incorporan nuevas columnas cuando existe espacio suficiente.

En escritorio se aprovecha el ancho disponible para mostrar más información simultáneamente y reorganizar las secciones principales.

Este enfoque evita construir primero una interfaz de escritorio para posteriormente intentar reducirla.

---

# Media queries y breakpoints

Se utilizaron principalmente dos puntos de ruptura:

- `601px`: transición aproximada de teléfono a tableta.
- `1024px`: transición hacia una distribución de escritorio.

Estos breakpoints no se utilizan únicamente para aumentar tamaños. También producen transformaciones reales en la distribución.

En el caso 1 cambian las columnas y las zonas ocupadas por las diferentes secciones del centro de control.

En el caso 2 aumenta la cantidad de columnas disponibles para actividades, escenarios y servicios, y el contenido principal aprovecha de manera diferente el espacio disponible en escritorio.

---

# Unidades relativas

Se utilizaron unidades relativas según las necesidades de cada propiedad.

Entre ellas:

- `rem` para tamaños y espacios.
- `%` para dimensiones relativas.
- `fr` para distribuir columnas de CSS Grid.
- `clamp()` para permitir tamaños flexibles dentro de límites controlados.

Esto permite que las interfaces mantengan flexibilidad en diferentes dimensiones de pantalla.

---

# Variables CSS

Los dos casos utilizan variables declaradas en `:root`.

Las variables permiten centralizar valores relacionados con:

- Colores.
- Espaciados.
- Bordes.
- Radios.
- Sombras.
- Anchos máximos.
- Estados y prioridades cuando corresponde.

De esta manera, el sistema visual puede modificarse globalmente sin repetir valores innecesariamente.

---

# Cascada, especificidad y organización del CSS

El CSS se organizó utilizando selectores comprensibles y clases reutilizables.

Se evitó depender de `!important` para resolver conflictos de estilos.

Los estilos base se definen primero y posteriormente las media queries amplían o modifican únicamente las propiedades necesarias.

Esto permite aprovechar la cascada y mantener una especificidad controlada.

---

# Diferencias entre los dos casos

Aunque ambos proyectos utilizan HTML5 y CSS3, fueron diseñados para resolver problemas distintos.

El **caso 1** funciona como un centro de control. Su objetivo es permitir la visualización simultánea de información relacionada con misiones, equipos, alertas, indicadores y agenda.

El **caso 2** funciona como una herramienta pública de consulta. Su diseño prioriza la información inmediata del festival y una navegación sencilla desde dispositivos móviles.

Por esta razón, las diferencias no se limitan a colores o textos: también cambia la jerarquía visual, la distribución del contenido y la forma en que las interfaces evolucionan según el ancho disponible.

---

# Estructura del proyecto

```text
tarea1/
├── caso1/
│   ├── css/
│   │   └── estilos.css
│   ├── img/
│   └── index.html
├── caso2/
│   ├── css/
│   │   └── estilos.css
│   ├── img/
│   └── index.html
└── README.md
```

---

# Instrucciones para abrir el proyecto

1. Descargar o clonar el repositorio.
2. Abrir la carpeta `tarea1`.
3. Para visualizar el centro de control, abrir `caso1/index.html` en un navegador web.
4. Para visualizar el festival cultural, abrir `caso2/index.html` en un navegador web.
5. No se requieren dependencias, servidores ni librerías externas para ejecutar el proyecto.

---

# Historial de commits

La siguiente tabla registra el desarrollo progresivo del proyecto y corresponde al historial de Git existente antes de la actualización final de requisitos y documentación.

| # | Fecha | Hash | Mensaje | Caso | Cambio realizado |
|---:|---|---|---|---|---|
| 1 | 2026-09-19 | `073fd75` | crea estructura inicial del proyecto | Ambos | Creación de la estructura inicial de carpetas y archivos del proyecto. |
| 2 | 2026-09-19 | `412740e` | agrega contenido y estilos base del caso 1 | Caso 1 | Incorporación del contenido y los estilos iniciales del centro de control. |
| 3 | 2026-09-19 | `7085585` | implementa diseño responsive y accesibilidad del caso 1 | Caso 1 | Implementación del comportamiento responsive y mejoras de accesibilidad. |
| 4 | 2026-09-20 | `24f72bf` | crea interfaz responsive del festival cultural | Caso 2 | Desarrollo inicial de la interfaz responsive del festival cultural. |
| 5 | 2026-09-20 | `446d860` | mejora posicionamiento y navegacion del caso 2 | Caso 2 | Mejoras de posicionamiento y navegación de la interfaz del festival. |
| 6 | 2026-09-20 | `038c365` | mejora accesibilidad y estados visuales del caso 1 | Caso 1 | Mejora de accesibilidad y comunicación de estados visuales. |
| 7 | 2026-09-20 | `5f8d702` | Documenta Estructura y Decisiones de Diseño | Ambos | Incorporación de la estructura del proyecto y las decisiones de diseño al README. |
| 8 | 2026-09-20 | `a83dedd` | Update README.md | Ambos | Actualización de la documentación general del proyecto. |
| 9 | 2026-09-20 | `256b14a` | Update README.md | Ambos | Ampliación de la documentación incluida en el README. |
| 10 | 2026-09-20 | `0442aef` | corrige redaccion y documentacion del proyecto | Ambos | Corrección de redacción y documentación general. |
| 11 | 2026-09-20 | `40c218a` | mejora accesibilidad de movimiento del caso 1 | Caso 1 | Incorporación de soporte para preferencias de movimiento reducido. |
| 12 | 2026-09-20 | `b559cb8` | mejora semantica de horarios del caso 2 | Caso 2 | Incorporación de elementos `time` en los horarios de las actividades del festival. |
| 13 | 2026-09-20 | `4ee89ee` | # Tarea 1 - Programación Web Avanzada | Ambos | Actualización general de la documentación del proyecto. |
| 14 | 2026-09-20 | `d8a8456` | completa documentacion final del proyecto | Ambos | Consolidación de la documentación final y del historial del proyecto. |

Para consultar y verificar el historial directamente desde Git se puede utilizar:

```bash
git --no-pager log --date=short --pretty=format:"| %ad | %h | %s |"
```

---

# Conclusión

El proyecto aplica los contenidos principales estudiados en HTML5 y CSS3 mediante dos soluciones diferentes.

El centro de control prioriza la visualización simultánea y organizada de información operativa, mientras que el festival cultural prioriza la consulta móvil y el acceso rápido a la programación.

Ambas interfaces utilizan estructura semántica, accesibilidad básica, modelo de caja, posicionamiento, Flexbox, CSS Grid, diseño mobile first, media queries, unidades relativas y variables CSS.
