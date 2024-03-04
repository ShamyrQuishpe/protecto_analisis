# protecto_analisis
Como primer paso en el codigo importamos la libreria pandas, usamos el archivo csv "gamesPR.csv" y le
realizamos un encoding a utf-08, lo transformamos a dataset, vemos los tipos de datos que se estan 
usando, luego contabilizamos los datos para poder limpiarlos. Como observamos este archivo la
categoria rating esta en ingles muy importante a tener en cuenta. ahora transformo todos los tipos de
datos a string  y remplazo los precios a "0.00".
Ahora en cuanto a las fechas solo mantengo el año, dropeo 3 filas que no analizaremos

Y ahora si, la cereza del pastel el webscrapping para ello importamos el webdriver de la libreria
de selenium y tambien bs4 de BeautifulSoup. Esto nos permitirá navegar en toda la página para poder
tomar todos los datos necesarios, definimos nuestro contendor del html de la pagina que es el iterable,
genero unos arreglos y un diccionario, y iteramos en los demas contenedores para tener titulos,
precios, windows, macs, linux, fechas, ratings, porcentajes, reseñas y el id respectivo de cada juego
Luego genero diferentes for que me permiten extraer dichos datos. Finalmente estos arreglos los
guardamos en un diccionario. Lo transformamos a un DatFrame con pandas y empezamos la limpieza de datos

La idea es igualar los datos del primer dataset y del que creamos del webscrapping entonces creamos
un diccionario que contiene las traducciones en español que recibimos en el webscrapping y las
cambiamos en el dataframe del webscrapping. Despues de la limpieza definimos los tipos de datos
Numericos como numericos y strings como strings.

Finalmente, concatenamos los dos datasets y los subimos a MYSQL que es la base de datos en donde
subire mis datos, desde MYSQL los extraré y subire a nuestro DataLake en MongoDB Atlas.


