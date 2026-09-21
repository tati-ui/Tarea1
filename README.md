
# Tarea 1 - ProgramaciÃ³n Web Avanzada

## IdentificaciÃ³n

**Estudiante:** Tatiana Solis Quesada
**CarnÃ©:** 207490238
**Curso:** SOFT-12 - ProgramaciÃ³n Web Avanzada
**SecciÃ³n:** SCV2
**Docente:** Ãlvaro Cordero PeÃ±a
**Tarea:** Tarea 1 - HTML5 y CSS3
**Fecha de entrega:** 20 de septiembre de 2026

---

## DescripciÃ³n del proyecto

Este proyecto corresponde a la Tarea 1 del curso ProgramaciÃ³n Web Avanzada.

El objetivo es desarrollar dos interfaces web utilizando Ãºnicamente HTML5 y CSS3, aplicando estructura semÃ¡ntica, accesibilidad, modelo de caja, posicionamiento, Flexbox, CSS Grid, diseÃ±o mobile first, media queries, unidades relativas y variables CSS.

Los dos casos fueron desarrollados como soluciones visualmente diferentes segÃºn las necesidades de cada contexto.

- **Caso 1:** centro de control de una expediciÃ³n cientÃ­fica.
- **Caso 2:** panel de consulta para un festival cultural.

El primer caso prioriza la visualizaciÃ³n simultÃ¡nea de informaciÃ³n operativa, mientras que el segundo prioriza una consulta sencilla desde dispositivos mÃ³viles.

---

# Caso 1 - Centro de Control de ExpediciÃ³n CientÃ­fica

## DescripciÃ³n

El primer caso consiste en un centro de control para una expediciÃ³n cientÃ­fica realizada en un Ã¡rea protegida de Costa Rica.

La interfaz funciona como un dashboard que permite consultar de forma simultÃ¡nea:

- Resumen general de operaciones.
- Misiones cientÃ­ficas.
- Equipos de investigaciÃ³n.
- Alertas operativas.
- PrÃ³ximas actividades.

Se incluyeron cinco misiones con informaciÃ³n sobre equipo responsable, ubicaciÃ³n, horario, prioridad y estado.

TambiÃ©n se presentan cuatro equipos cientÃ­ficos:

- BiologÃ­a.
- HidrologÃ­a.
- MeteorologÃ­a.
- GeologÃ­a.

Las alertas utilizan diferentes niveles de importancia y combinan informaciÃ³n textual con elementos visuales, evitando que su significado dependa Ãºnicamente del color.

## Decisiones de diseÃ±o del caso 1

El caso 1 fue diseÃ±ado como un centro de control en el que es importante observar varias categorÃ­as de informaciÃ³n simultÃ¡neamente.

En telÃ©fonos, el contenido se presenta principalmente en una sola columna para mantener la legibilidad. En tabletas comienza a distribuirse en dos columnas y, en escritorio, CSS Grid permite organizar las secciones principales en distintas zonas del dashboard.

La jerarquÃ­a visual permite diferenciar indicadores, misiones, equipos, alertas y agenda sin depender Ãºnicamente del color.

El encabezado utiliza posicionamiento `sticky` para mantener disponibles el nombre de la expediciÃ³n y la navegaciÃ³n mientras el usuario consulta el dashboard. El nivel de apilamiento se controla mediante `z-index`.

Flexbox se utiliza en problemas de distribuciÃ³n unidimensional, mientras que CSS Grid se utiliza para las estructuras bidimensionales y la reorganizaciÃ³n general del contenido.

---

# Caso 2 - Festival Cultural RaÃ­ces 2026

## DescripciÃ³n

El segundo caso consiste en una interfaz pÃºblica para consultar la programaciÃ³n del Festival Cultural RaÃ­ces 2026.

La informaciÃ³n se divide en:

- Actividades que ocurren en este momento.
- ProgramaciÃ³n de prÃ³ximas actividades.
- ProgramaciÃ³n por escenarios.
- Cambios de programaciÃ³n.
- Servicios disponibles.

La secciÃ³n **Ahora** recibe mayor importancia visual porque contiene la informaciÃ³n mÃ¡s relevante para una persona que se encuentra consultando el festival durante el evento.

Cada actividad que se encuentra en curso presenta su horario, nombre, tipo, escenario y estado.

La programaciÃ³n de prÃ³ximas actividades incluye hora, nombre, escenario y categorÃ­a.

La programaciÃ³n por escenarios se organiza en cuatro espacios principales:

- Escenario Central.
- Teatro.
- Zona Cultural.
- Zona Familiar.

Los horarios utilizan el elemento semÃ¡ntico `time`, permitiendo representar adecuadamente la informaciÃ³n temporal.

## Decisiones de diseÃ±o del caso 2

El caso 2 fue diseÃ±ado con un enfoque de consulta mÃ³vil.

A diferencia del centro de control del caso 1, esta interfaz prioriza inicialmente una lectura vertical sencilla. Conforme aumenta el ancho disponible, las actividades, escenarios y servicios se distribuyen en mÃ¡s columnas.

El encabezado presenta el nombre del festival, fecha, ubicaciÃ³n y horario general para que la informaciÃ³n principal estÃ© disponible desde el inicio de la pÃ¡gina.

La navegaciÃ³n permite acceder rÃ¡pidamente a las secciones Ahora, ProgramaciÃ³n, Escenarios, Servicios e InformaciÃ³n.

El encabezado y la navegaciÃ³n permanecen disponibles mediante posicionamiento `sticky`.

CSS Grid se utiliza principalmente en la programaciÃ³n por escenarios y en otras agrupaciones que requieren una distribuciÃ³n bidimensional.

Flexbox se emplea para estructuras unidimensionales como la navegaciÃ³n y distintos componentes de programaciÃ³n.

El resultado busca que la consulta sea rÃ¡pida en telÃ©fono y aproveche progresivamente el espacio adicional disponible en tableta y escritorio.

---

# HTML semÃ¡ntico y organizaciÃ³n del contenido

Los dos casos utilizan elementos semÃ¡nticos de HTML5 segÃºn el significado del contenido.

Entre los elementos utilizados se encuentran:

- `header` para los encabezados principales.
- `nav` para la navegaciÃ³n.
- `main` para el contenido principal.
- `section` para agrupar Ã¡reas temÃ¡ticas.
- `article` para contenidos independientes.
- `footer` para la informaciÃ³n final.
- `time` para representar horarios cuando corresponde.

Se mantiene una jerarquÃ­a lÃ³gica de encabezados:

- `h1` identifica la interfaz.
- `h2` identifica las secciones principales.
- `h3` identifica contenidos internos como actividades, misiones, equipos, escenarios o servicios.

Esta estructura permite comprender la organizaciÃ³n general del contenido incluso sin aplicar CSS.

---

# Accesibilidad

Se aplicaron diferentes principios bÃ¡sicos de accesibilidad.

Los documentos utilizan `lang="es"` para identificar el idioma del contenido.

La navegaciÃ³n utiliza enlaces comprensibles y se incorporaron estados de foco visibles para facilitar la navegaciÃ³n mediante teclado.

Los estados, prioridades y alertas no dependen exclusivamente del color. TambiÃ©n utilizan texto para comunicar su significado.

Se mantuvo una jerarquÃ­a coherente de encabezados y se buscaron niveles adecuados de contraste entre texto y fondo.

En el caso 1 se incorporÃ³ ademÃ¡s la media query `prefers-reduced-motion`, que elimina el desplazamiento suave cuando el usuario tiene configurada una preferencia de movimiento reducido.

No se utilizaron imÃ¡genes informativas que requieran texto alternativo en las interfaces actuales.

---

# Modelo de caja

Se utiliza `box-sizing: border-box` para facilitar el control de las dimensiones de los elementos.

Los mÃ¡rgenes, rellenos, bordes y espacios se organizan mediante valores reutilizables y variables CSS.

TambiÃ©n se establecieron lÃ­mites de ancho para evitar que el contenido se extienda excesivamente en pantallas grandes.

Los componentes fueron diseÃ±ados para adaptarse al espacio disponible y evitar desbordamientos horizontales accidentales.

---

# Posicionamiento

El posicionamiento se utiliza Ãºnicamente cuando responde a una necesidad concreta y no como sustituto de Flexbox o CSS Grid.

Los encabezados utilizan `position: sticky` para conservar la navegaciÃ³n durante el desplazamiento de la pÃ¡gina.

TambiÃ©n se controla el nivel de apilamiento mediante `z-index`, evitando conflictos entre el encabezado y el resto del contenido.

Esta decisiÃ³n permite mantener disponibles los principales controles de navegaciÃ³n sin alterar el flujo general de los documentos.

---

# Flexbox

Flexbox se utiliza para resolver distribuciones unidimensionales.

Entre sus aplicaciones se encuentran:

- NavegaciÃ³n.
- AlineaciÃ³n de elementos.
- DistribuciÃ³n de informaciÃ³n dentro de componentes.
- OrganizaciÃ³n de actividades y programaciÃ³n.
- Manejo de direcciÃ³n, separaciÃ³n y envoltura de elementos.

Su uso complementa a CSS Grid y evita depender de mÃ¡rgenes arbitrarios para construir el layout.

---

# CSS Grid

CSS Grid se utiliza para las estructuras bidimensionales de ambos casos.

En el caso 1 permite transformar el centro de control desde una distribuciÃ³n vertical para telÃ©fonos hasta una estructura de varias zonas en escritorio.

En el caso 2 se utiliza principalmente para organizar la programaciÃ³n por escenarios y otras agrupaciones de contenido que aumentan su cantidad de columnas conforme existe mÃ¡s espacio disponible.

Las columnas y Ã¡reas cambian segÃºn el ancho de la pantalla, permitiendo que cada interfaz responda a su contexto.

---

# DiseÃ±o mobile first

Los estilos base fueron construidos para pantallas pequeÃ±as.

A partir de esa base, las interfaces se amplÃ­an progresivamente mediante media queries.

En telÃ©fono se prioriza una lectura principalmente vertical.

En tableta se incorporan nuevas columnas cuando existe espacio suficiente.

En escritorio se aprovecha el ancho disponible para mostrar mÃ¡s informaciÃ³n simultÃ¡neamente y reorganizar las secciones principales.

Este enfoque evita construir primero una interfaz de escritorio para posteriormente intentar reducirla.

---

# Media queries y breakpoints

Se utilizaron principalmente dos puntos de ruptura:

- `601px`: transiciÃ³n aproximada de telÃ©fono a tableta.
- `1024px`: transiciÃ³n hacia una distribuciÃ³n de escritorio.

Estos breakpoints no se utilizan Ãºnicamente para aumentar tamaÃ±os. TambiÃ©n producen transformaciones reales en la distribuciÃ³n.

En el caso 1 cambian las columnas y las zonas ocupadas por las diferentes secciones del centro de control.

En el caso 2 aumenta la cantidad de columnas disponibles para actividades, escenarios y servicios, y el contenido principal aprovecha de manera diferente el espacio disponible en escritorio.

---

# Unidades relativas

Se utilizaron unidades relativas segÃºn las necesidades de cada propiedad.

Entre ellas:

- `rem` para tamaÃ±os y espacios.
- `%` para dimensiones relativas.
- `fr` para distribuir columnas de CSS Grid.
- `clamp()` para permitir tamaÃ±os flexibles dentro de lÃ­mites controlados.

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
- Anchos mÃ¡ximos.
- Estados y prioridades cuando corresponde.

De esta manera, el sistema visual puede modificarse globalmente sin repetir valores innecesariamente.

---

# Cascada, especificidad y organizaciÃ³n del CSS

El CSS se organizÃ³ utilizando selectores comprensibles y clases reutilizables.

Se evitÃ³ depender de `!important` para resolver conflictos de estilos.

Los estilos base se definen primero y posteriormente las media queries amplÃ­an o modifican Ãºnicamente las propiedades necesarias.

Esto permite aprovechar la cascada y mantener una especificidad controlada.

---

# Diferencias entre los dos casos

Aunque ambos proyectos utilizan HTML5 y CSS3, fueron diseÃ±ados para resolver problemas distintos.

El **caso 1** funciona como un centro de control. Su objetivo es permitir la visualizaciÃ³n simultÃ¡nea de informaciÃ³n relacionada con misiones, equipos, alertas, indicadores y agenda.

El **caso 2** funciona como una herramienta pÃºblica de consulta. Su diseÃ±o prioriza la informaciÃ³n inmediata del festival y una navegaciÃ³n sencilla desde dispositivos mÃ³viles.

Por esta razÃ³n, las diferencias no se limitan a colores o textos: tambiÃ©n cambia la jerarquÃ­a visual, la distribuciÃ³n del contenido y la forma en que las interfaces evolucionan segÃºn el ancho disponible.

---

# Estructura del proyecto

```text
tarea1/
â”œâ”€â”€ caso1/
â”‚   â”œâ”€â”€ css/
â”‚   â”‚   â””â”€â”€ estilos.css
â”‚   â”œâ”€â”€ img/
â”‚   â””â”€â”€ index.html
â”œâ”€â”€ caso2/
â”‚   â”œâ”€â”€ css/
â”‚   â”‚   â””â”€â”€ estilos.css
â”‚   â”œâ”€â”€ img/
â”‚   â””â”€â”€ index.html
â””â”€â”€ README.md
```

---

# Instrucciones para abrir el proyecto

1. Descargar o clonar el repositorio.
2. Abrir la carpeta `tarea1`.
3. Para visualizar el centro de control, abrir `caso1/index.html` en un navegador web.
4. Para visualizar el festival cultural, abrir `caso2/index.html` en un navegador web.
5. No se requieren dependencias, servidores ni librerÃ­as externas para ejecutar el proyecto.

---

# Historial de commits

La siguiente tabla registra el desarrollo progresivo del proyecto y corresponde al historial de Git existente antes de la actualizaciÃ³n final de requisitos y documentaciÃ³n.

| # | Fecha | Hash | Mensaje | Caso | Cambio realizado |
|---:|---|---|---|---|---|
| 1 | 2026-09-19 | `073fd75` | crea estructura inicial del proyecto | Ambos | CreaciÃ³n de la estructura inicial de carpetas y archivos del proyecto. |
| 2 | 2026-09-19 | `412740e` | agrega contenido y estilos base del caso 1 | Caso 1 | IncorporaciÃ³n del contenido y los estilos iniciales del centro de control. |
| 3 | 2026-09-19 | `7085585` | implementa diseÃ±o responsive y accesibilidad del caso 1 | Caso 1 | ImplementaciÃ³n del comportamiento responsive y mejoras de accesibilidad. |
| 4 | 2026-09-20 | `24f72bf` | crea interfaz responsive del festival cultural | Caso 2 | Desarrollo inicial de la interfaz responsive del festival cultural. |
| 5 | 2026-09-20 | `446d860` | mejora posicionamiento y navegacion del caso 2 | Caso 2 | Mejoras de posicionamiento y navegaciÃ³n de la interfaz del festival. |
| 6 | 2026-09-20 | `038c365` | mejora accesibilidad y estados visuales del caso 1 | Caso 1 | Mejora de accesibilidad y comunicaciÃ³n de estados visuales. |
| 7 | 2026-09-20 | `5f8d702` | Documenta Estructura y Decisiones de DiseÃ±o | Ambos | IncorporaciÃ³n de la estructura del proyecto y las decisiones de diseÃ±o al README. |
| 8 | 2026-09-20 | `a83dedd` | Update README.md | Ambos | ActualizaciÃ³n de la documentaciÃ³n general del proyecto. |
| 9 | 2026-09-20 | `256b14a` | Update README.md | Ambos | AmpliaciÃ³n de la documentaciÃ³n incluida en el README. |
| 10 | 2026-09-20 | `0442aef` | corrige redaccion y documentacion del proyecto | Ambos | CorrecciÃ³n de redacciÃ³n y documentaciÃ³n general. |
| 11 | 2026-09-20 | `40c218a` | mejora accesibilidad de movimiento del caso 1 | Caso 1 | IncorporaciÃ³n de soporte para preferencias de movimiento reducido. |
| 12 | 2026-09-20 | `b559cb8` | mejora semantica de horarios del caso 2 | Caso 2 | IncorporaciÃ³n de elementos `time` en los horarios de las actividades del festival. |
| 13 | 2026-09-20 | `4ee89ee` | # Tarea 1 - ProgramaciÃ³n Web Avanzada | Ambos | ActualizaciÃ³n general de la documentaciÃ³n del proyecto. |
| 14 | 2026-09-20 | `d8a8456` | completa documentacion final del proyecto | Ambos | ConsolidaciÃ³n de la documentaciÃ³n final y del historial del proyecto. |

Para consultar y verificar el historial directamente desde Git se puede utilizar:

```bash
git --no-pager log --date=short --pretty=format:"| %ad | %h | %s |"
```

---

# ConclusiÃ³n

El proyecto aplica los contenidos principales estudiados en HTML5 y CSS3 mediante dos soluciones diferentes.

El centro de control prioriza la visualizaciÃ³n simultÃ¡nea y organizada de informaciÃ³n operativa, mientras que el festival cultural prioriza la consulta mÃ³vil y el acceso rÃ¡pido a la programaciÃ³n.

Ambas interfaces utilizan estructura semÃ¡ntica, accesibilidad bÃ¡sica, modelo de caja, posicionamiento, Flexbox, CSS Grid, diseÃ±o mobile first, media queries, unidades relativas y variables CSS.
