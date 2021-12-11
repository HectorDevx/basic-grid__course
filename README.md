# CSS Grid Básico

- Grilla
- Columnas (Columns)
- Filas (Row)

## Conceptos

Contenedor: El elemento que se va a convertir en una grilla.
Item: Elementos dentro del contenedor.
Líneas: Elementos que limitan o dividen las filas y columnas de una grilla.
Celda: Unidad mínima a tener dentro de una grilla.
Grupos de celdas: Tracks (Horizontales) y Áreas (Horizontales y verticales).

## Propiedades del contenedor

Crear una grilla, definir su cantidad de columnas y filas y el espaci oentre ellas.

- Display grid:
- Grid-template:
- Gaps:
- Grid-auto:

## Propiedades de alineación

### Propiedades de los items.

Las declaramos en el contenedor y nos ayudan a alinear los items que están dentro del contenedor.

- Justify-items
- Align-items
- Place-items

Justify: Nos ayudan a alinear en el espacio horizontal.
Align: Alineación vertical.
Place: Una mezcla de horizontal y vertical.

### Propiedades de alineación del contenedor.

Son las que ajustan la grilla completa al espacio que tiene disponible. Como un bloque.

- Justify-content
- Align-content
- Place-content

### Propiedades de alineación del item.

Se le dan directamente a los items.

- Justify-self
- Align-self
- Place-self

## Propiedades de ubicación

- grid-column-start
- grid-column-end
- grid-column

- grid-row-start
- grid-row-end
- grid-row

- grid-area. Donde inicia y termina en columna y en fila.

## Funciones especiales

- minmax: Ayuda a declarar el tamaño mínimo y máximo para el ancho y alto de una celda, sin depender del contenido que tengamos en ella. `grid-template-columns: minmax(30px, 300px) 200px minmax(20px, 250x);`

- repeat: Se usa cuando todas las colimnas o filas tienen el mismo ancho y evitar tepetir el tamaño de columnas.
  `grid-template-rows: repeat(3, auto);`

## Keywords especiales

- fr: Es una unidad de medida especial de css grid para darle ancho o alto a filas y columnas. 1fr representa una fracción del total de columnas o filas. `grid-template-columns: repeat(4, 1fr);`
- min-content: Ajusta el ancho de la celda lo mínimo posible sin romper su contenido. Crea saltos de línea donde es posible. `grid-template-columns: 1fr 3fr min-content 2fr`
- max-content: Ajusta el ancho de la celda lo máximo posible para mostrar su contenido. Puede provocar overflow. `grid-template-columns: 1fr 3fr max-content 2fr`
- auto-fill: Agrega columnas "fantasma" que rellenan el espacio del contenedor. `grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));`
  auto-fill y auto-fit ayudan a la grilla a ocupar el 100% del espacio disponible.
- auto-fit: Las columnas se expanden hasta llenar el 100% del espacio disponible. `grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));`
  auto-fill y auto-fit ayudan a la grilla a ocupar el 100% del espacio disponible.
