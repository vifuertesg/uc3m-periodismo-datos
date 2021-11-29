## ORGANIZACIÓN, LIMPIEZA Y SELECCIÓN DE DATOS
Para llevar a cabo este proceso, me he servido de OpenRefine
para saber lo que significa cada datos me he apoyado en los documentos de los que dispone eurostat para poder analizar sus datos.
1) ANTES DE CREAR EL PROYECTO TENEMOS QUE SEPARAR LAS COLUMNAS POR TABULACIONES, NO POR COMAS.
1) ELIMINAR TODAS LAS COLUMNAS QUE HAGAN REFERENCIA A LOS AÑOS MENOS LAS DE 2019 (ÉPOCA PRECOVID Y ADEMÁS ASÍ PODER METER A UK EN LA LISTA TAMBIEN) - DESD TODO - EDITAR COLUMNAS -REORDENAR/QUITAR COLUMNAS
2) Dividir la columna con el nombre:unit,sex,geo\time usando la coma como separador. De tal forma que ahora tendremos cuatro columnas.
3) Eliminamos la primera, ya que es irrelevante AVG(Average,media).
4) las siguientes las renombramos, de tal forma que tenemos sex y geo
5) FILTRO DE TEXTO ESCRIBIR T, en la columna sex Y ASÍ TENER LOS DATOS de la totalidad de la población, con independencia del sexo

7) eliminar las celdas que hacen referencia a datos de la union europea en su totalidad. Son cuatro: EA19, EU 15, EU27_2020, EU28 (FILTRO DE TEXTO INVERTIDO - PRIMERO DE EU Y LUEGO DE EA)
8) REORGANIZAMOS LAS COLUMNAS DE TAL FORMA QUE QUEDEN DE IZQ A dercha (geo - sex - 2019), contraemos la columna de sex para que visualmente quede mejor 
9) 
