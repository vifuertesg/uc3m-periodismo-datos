# PRÁCTICA 3&4. MI HISTORIA DE PERIODISMO DE DATOS
Para esta actividad, he realizado un gráfico a través de unos datos que he recolectado de la página web de Eurostat ([La oficina Europea de Estadística](https://ec.europa.eu/eurostat)). Dichos datos recogen las edades estimadas con las que los jóvenes de la Unión Europea se "independizan", o más concretamente, dejan atrás sus hogares familiares. Este archivo de datos está construido basándose en parámetros tales como el sexo,la procedencia geográfica y la fecha (en años, desde el 2000 hasta el 2020). A continuación, expondré los gráficos y explicaré detalladamente el proceso de creación que he seguido. 
## GRÁFICOS CREADOS CON DATAWRAPPER
[Gráfico 1](https://github.com/vifuertesg/uc3m-periodismo-datos/blob/main/Img/Gra%CC%81fico%20UE.png): ***Media de edad con la que los jóvenes de la UE abandonan el hogar familiar***

La razón por la cual he querido construir este gráfico radica en la creciente popularidad y, en mi opinión, importancia de este tema. Nos encontramos en un contexto nacional marcado por una elevada tasa de desempleo juvenil, dato que los medios de comunicación, las redes sociales o un probable 50% de nuestras conversaciones sobre este temido e incierto futuro no deja de recordarnos. Ahora bien, el desempleo juvenil está directamente relacionado con la tardía tendencia que tienen los jóvenes españoles a dejar sus hogares familiares y vivir de manera plenamente independiente. Por este motivo he querido diseñar esta visualización, porque así podremos ver que estamos entre los diez últimos, y que esto es un problema. 

En este gráfico he querido centrarme en la totalidad de la población de cada zona geográfica, prescindiendo de las diferenciaciones de género, ya que consideraba que de haberlas incluido, el gráfico iba a quedar extremadamente recargado y esto podría perjudicar el dinamismo y el fácil entendimiento del mismo. También he querido prescindir de todos los datos que no sean actuales, por actuales me refiero a todos menos a los del año 2019. Las razones por la que he escogido este año y no el 2020 son dos: para poder ofrecer también los datos del Reino Unido y para poder mostrar la realidad prepandémica.

## PROCESO DE CREACIÓN
### ORGANIZACIÓN, LIMPIEZA Y SELECCIÓN DE DATOS
Para llevar a cabo este proceso, me he servido de **OpenRefine** y de diversos archivos que también proporcionaba *Eurostat*, para poder interpretar los datos y así poder organizarlos y seleccionar los que fueron objeto de mi estudio. 
1) ANTES DE CREAR EL PROYECTO TENEMOS QUE SEPARAR LAS COLUMNAS POR TABULACIONES, NO POR COMAS.
1) ELIMINAR TODAS LAS COLUMNAS QUE HAGAN REFERENCIA A LOS AÑOS MENOS LAS DE 2019 (ÉPOCA PRECOVID Y ADEMÁS ASÍ PODER METER A UK EN LA LISTA TAMBIEN) - DESD TODO - EDITAR COLUMNAS -REORDENAR/QUITAR COLUMNAS
2) Dividir la columna con el nombre:unit,sex,geo\time usando la coma como separador. De tal forma que ahora tendremos cuatro columnas.
3) Eliminamos la primera, ya que es irrelevante AVG(Average,media).
4) las siguientes las renombramos, de tal forma que tenemos sex y geo
5) FILTRO DE TEXTO ESCRIBIR T, en la columna sex Y ASÍ TENER LOS DATOS de la totalidad de la población, con independencia del sexo

7) eliminar las celdas que hacen referencia a datos de la union europea en su totalidad. Son cuatro: EA19, EU 15, EU27_2020, EU28 (FILTRO DE TEXTO INVERTIDO - PRIMERO DE EU Y LUEGO DE EA)
8) REORGANIZAMOS LAS COLUMNAS DE TAL FORMA QUE QUEDEN DE IZQ A dercha (geo - sex - 2019), contraemos la columna de sex para que visualmente quede mejor 

### DATAWRAPPER
