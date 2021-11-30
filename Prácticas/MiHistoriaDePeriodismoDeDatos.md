# PRÁCTICA 3&4. MI HISTORIA DE PERIODISMO DE DATOS
Para esta actividad, he realizado un gráfico a través de unos datos que he recolectado de la página web de Eurostat ([La oficina Europea de Estadística](https://ec.europa.eu/eurostat)). Dichos datos recogen las edades estimadas con las que los jóvenes de la Unión Europea se "independizan", o más concretamente, dejan atrás sus hogares familiares. Este archivo de datos está construido basándose en parámetros tales como el sexo,la procedencia geográfica y la fecha (en años, desde el 2000 hasta el 2020). A continuación, expondré los gráficos y explicaré detalladamente el proceso de creación que he seguido. 
## GRÁFICOS CREADOS CON DATAWRAPPER
[Gráfico 1](https://github.com/vifuertesg/uc3m-periodismo-datos/blob/main/Img/Gra%CC%81fico%20UE.png): ***Media de edad con la que los jóvenes de la UE abandonan el hogar familiar***

La razón por la cual he querido construir este gráfico radica en la creciente popularidad y, en mi opinión, importancia de este tema. Nos encontramos en un contexto nacional marcado por una elevada tasa de desempleo juvenil, dato que los medios de comunicación, las redes sociales o un probable 50% de nuestras conversaciones sobre este temido e incierto futuro no deja de recordarnos. Ahora bien, el desempleo juvenil está directamente relacionado con la tardía tendencia que tienen los jóvenes españoles a dejar sus hogares familiares y vivir de manera plenamente independiente. Por este motivo he querido diseñar esta visualización, porque así podremos ver que estamos entre los diez últimos, y que esto es un problema. 

En este gráfico he querido centrarme en la totalidad de la población de cada zona geográfica, prescindiendo de las diferenciaciones de género, ya que consideraba que de haberlas incluido, el gráfico iba a quedar extremadamente recargado y esto podría perjudicar el dinamismo y el fácil entendimiento del mismo. También he querido prescindir de todos los datos que no sean actuales, por actuales me refiero a todos menos a los del año 2019. Las razones por la que he escogido este año y no el 2020 son dos: para poder ofrecer también los datos del Reino Unido y para poder mostrar la realidad prepandémica.

## PROCESO DE CREACIÓN
### ORGANIZACIÓN, LIMPIEZA Y SELECCIÓN DE DATOS
Para llevar a cabo este proceso, me he servido de **OpenRefine** y me he apoyado en diversos archivos que también proporcionaba *Eurostat*, para poder interpretar los datos y así poder organizarlos y seleccionar posteriorme con OpenRefine. El archivo con los datos que he utilizado lo podeís encontrar [aquí](https://github.com/vifuertesg/uc3m-periodismo-datos/tree/main/data). Pasos seguidos en OpenRefine:
1) Antes de crear el proyecto, he separado las columnas por tabulaciones y no por comas. 
2) He eliminado todas las columnas relacionadas con los años menos la que corresponde a 2019. Procedimiento: Columna TODO - EDITAR COLUMNAS -REORDENAR/QUITAR COLUMNAS
3) He dividido la columna con el nombre:unit,sex,geo\time usando la coma como separador. De tal forma que pasé a tener cuatro nuevas columnas. Procedimiento: columna UNIT,SEX,GEO\TIME - EDITAR COLUMNA - DIVIDIR EN VARIAS COLUMNAS
4) Eliminé la primera (la que se encuentra más a la izquierda), ya que es irrelevante, todos los datos son: AVG(Average,media).
5) Las dos columnas siguientes las renombré, para que me fuera más sencillo trabajar con ellas. De izq a derecha, los nuevos nombres: SEX (datos de género) Y GEO (datos de la región geográfica).
6) Para prescindir de los datos que diferencian el género de los jóvenes, utilicé un FILTRO DE TEXTO (T=totalidad), en la columna sex. Así solo se quedaron los datos que hacen referencia a la totalidad de la población, con independencia del sexo
7) También eliminé las celdas que hacen referencia a datos de la union europea en su totalidad y poder trabajar con los datos únicamente d elos países. Las celdas que eliminé fueron cuatro: EA19, EU 15, EU27_2020, EU28 (Procedimiento: FILTRO DE TEXTO INVERTIDO - PRIMERO DE EU Y LUEGO DE EA).
8) REORGANIZAMOS LAS COLUMNAS de tal forma que queden de izquierda a derecha (geo - sex - 2019) y trasnformamos las celdas de la columna 2019 en números (procedimiento: columna 2019 - EDITAR CELDAS - TRANSFORMACIONES COMUNES - A NÚMERO).
9) Exportamos en formato excel (.xls).


| **ANTES** | **DESPUÉS** |
| ------------- | ------------- |
| ![ant](https://github.com/vifuertesg/uc3m-periodismo-datos/blob/main/Img/ANTES.png)  | ![desp](https://github.com/vifuertesg/uc3m-periodismo-datos/blob/main/Img/DESPUE%CC%81S.png)  |


### DATAWRAPPER
Lo único que me gustaría resaltar de este procedimiento son 3 puntos: 
- La modificación manual que he llevado a cabo de las siglas de las regiones geográficas (ES-España, FR-Francia, MK-Macedonia...) con el objetivo de facilitar el entendimiento del gráfico. 
- También he cuidado mucho los colores de la barras para que se pueda ver con más claridad las diferencias entre países, siendo Suecia el más claro con una media de 18 años de edad y Montenegro el más oscuro con una media de 33 años. Aquí también pretendía relacionar la claridad del color con el progreso y los tonos más oscuros, con el "hundimiento". 
- Por último me gustaría comentar que los datos númericos estaban escritos con decimales, pero a la hora de realizar el gráfico he prescindido de ellos (sin embargo la longitud de las barras nos puede ofrecer una idea de por dónde van los tiros).
