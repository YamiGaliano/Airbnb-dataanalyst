# Airbnb-dataanalyst
Documentación Proyecto
Data Analytics 
 ____________

Proyecto: Airbnb - CABA

Integrantes: 
Yamila Galiano 
Comisión CH: 43510
Octubre- 2022

Contenido

1 - Introducción.

2 - Descripción de la temática de los datos.

3 - Tipos de análisis.

4 - Alcance. 

5 - Usuario final y nivel de aplicación.

6 - Herramientas utilizadas. 

7 - Datasets.

8 - Glosario.

9 - Diagrama de entidad-relación.

10 - Listado de tablas.

11 - Segmentación elegida. 

12 - Conclusión. 

 ____________

1 - Introducción

Airbnb puede considerarse hoy en día la cadena hotelera más grande y está revolucionando la industria del turismo en todo el mundo.
Airbnb se convirtió en un popular mercado de alquileres en línea y una aplicación móvil que conecta a los anfitriones y huéspedes que buscan un alojamiento alternativo con alojamiento a corto plazo y actividades relacionadas con el turismo.
La compañía ha revolucionado el turismo mundial y está impulsando la competencia con los hoteles tradicionales, al ofrecer una excelente alternativa al servicio de los hoteles caros y de baja calidad.

Ciudad de Buenos Aires
En Buenos Aires, la ciudad podría observar un boom desde 2011, año en que Airbnb aterrizó en Argentina. Más de 900.000 viajeros se alojaron en ubicaciones de Airbnb dentro de Argentina en 2018 y las cifras siguen aumentando a lo largo de los años.
Una búsqueda rápida de ubicaciones de Airbnb en Buenos Aires y sus alrededores arroja cientos de lugares donde los viajeros pueden quedarse.

En el presente trabajo quisimos abordar el crecimiento de los alojamientos de esta zona en particular para abordarlo con más detalles y encontrar tendencias o patrones en toda la información. 



2 - Descripción de la temática de los datos. 

En el presente trabajo, se obtuvieron los datos de los alojamientos temporarios ofrecidos en la Ciudad de Buenos Aires de la plataforma de Airbnb, en Inside Airbnb. Inside es un conjunto de herramientas y datos independientes, no comerciales, que permiten a la comunidad explorar cómo se utiliza Airbnb en ciudades de todo el mundo.
En particular, se tuvieron en cuenta las características propias de anfitriones (“Host”), su validación en dicha plataforma (“Verification”), las propiedades a alquilar (“Property”), los tipos de alojamientos que se ofertan (“Type room”), el barrio en el que se ubican (“Neighborhood”), los servicios que ofrecen (“Services”) y otras variables relativas al puntaje (“Score”) y las reseñas que reciben de parte de los usuarios (“Review”).
A partir del tipo del modelo denominado “Entidad-Relación” se estructuró y organizó la base de datos escogida en sus respectivas tablas, las cuales se encuentran divididas en solapas. 

3 - Tipos de análisis seleccionado.
Descriptivo 
Con base en la pregunta ¿Cuáles son los alojamientos disponibles en CABA según AIRBNB? Se describen los patrones claves en los datos existentes, lo que permite observar la situación actual de las plazas ofrecidas por la plataforma en la Ciudad de Buenos Aires. 
Además, entendemos que la presente base de datos permitirá reflejar si hubo aumento en la cantidad de alojamientos disponibles en CABA, según los registros de años anteriores. Con ello, examinar si el eventual crecimiento guarda relación con la problemática existente en torno a los alquileres en la Ciudad. También podremos detectar posibles concentraciones en ciertos sectores de la ciudad como su precio promedio. 

Demás tipos de análisis:
Diagnósticos
A partir de ciertos hitos y momentos donde se cambiaron las leyes de alquiler en alojamientos de larga estadía, podremos validar si se condice con el crecimiento de alquileres temporales. 
Predictivos
Validando la concentración por barrios o zonas de la ciudad, podremos detectar un patrón de zonas de turistas y una tasa de crecimiento promedio. 
Prescriptivos
Esta información podría generar posibles acciones de la ciudad para brindar mayor seguridad y limpieza en dichas zonas, así como activar un comercio mayor. 

4 - Alcance
El dashboard planea ser parte de un análisis táctico y en parte estratégico para el sector turístico. 
Táctico, para que los interesados puedan obtener información que impulsen a tomar medidas y proyectar el crecimiento que demande la cantidad de alojamientos cumpliendo con las expectativas de los huéspedes. 
Estratégico para analizar si esto puede desencadenar mayores zonas de comercios o nuevos negocios. 

5 - Usuario final y nivel de aplicación
El usuario final corresponde al sector de turismo, ya sean arrendadores o analistas del sector turístico. En el mismo podrá obtener información relevante para mejorar sus hospedajes y tener en cuenta cual es el funcionamiento actual del sector turístico. 

6 - Herramientas utilizadas
Google sheet: Para el análisis y limpieza del dataset obtenido en un archivo .csv. 
Diagrams.net: Para realizar el diagrama de entidad-relación. 
Power BI Desktop: Para realizar análisis, transformación de datos y creación de dashboard. 
Canva: Para generar un fondo uniforme. 
Flaticon: Para obtener los iconos de la presentación.

7 - Datasets
Se adjunta el documento Google Sheet con las bases de datos organizadas y estructuradas utilizadas en el presente trabajo. [Link](https://docs.google.com/spreadsheets/d/1DLnzgi4OBxwn829iCos0RBuRm0Cu1bZnsaszOw5Eorc/edit#gid=1957361665) 
Dicha información ha sido extraída de la web [Inside Airbnb](http://insideairbnb.com/get-the-data/) en un archivo .csv para su posterior transformación en excel.
Se quitaron datos irrelevantes para este análisis como imágenes del perfil del arrendatario, links a la publicación, imágenes de la propiedad, entre otros. 


8 - Glosario
El glosario se encuentra detallado en el siguiente archivo google [sheet](https://docs.google.com/spreadsheets/d/1Q0idI-ocnhI4YVn-CneGdNz-TG-ZXyaHLLYlZGoBlOI/edit?usp=sharing). 

9 - Diagrama de entidad-relación
Para validar el diagrama entidad-relación con mayor detalle, ingresar al siguiente [link](https://app.diagrams.net/#G1Aw_zkfK7jWzXIkkYMf6TpYqWmxOCrP9K).

10 - Listado de tablas
Host:
Esta tabla contiene los datos del propietario como su id, nombre, ubicación, tipo de host, tiempo de respuesta, cantidad de propiedades y su fecha de alta en la plataforma. Clave PK: host_id.
Verification:
Esta tabla contiene las verificaciones realizadas por el host/propietario de identidad, email, teléfono y mail de trabajo. Clave PK: id_verification. Clave FK: host_id. 
Property: 
Esta tabla contiene información de la propiedad como la ubicación, baños, habitaciones, precio, entre otros. Clave PK: id_property. Clave FK: host_id, id_room.
Type_room:
Esta tabla contiene el tipo de habitación de la propiedad: Entire places, Private rooms y Shared rooms. Clave PK: id_room.
Neighborhood:
Detalle del barrio en donde se encuentra ubicada la propiedad. Clave PK: id_neighbourdhood. Clave FK: id_property. 
Score:
Puntuación de la propiedad en distintos aspectos: checkin, comunicación, limpieza, ubicación, costo-beneficio y veracidad. Clave PK: id_score. Clave FK: id_property.
Review: 
Cantidad de comentarios que tiene una propiedad, por parte de sus huéspedes. Clave PK: id_review. Clave FK: id_property. 
Services:
Tabla con la descripción de los servicios disponibles en la propiedad. Clave PK: id_services. Clave FK: id_property. 
Más detalle en el siguiente [link](https://docs.google.com/spreadsheets/d/1DLnzgi4OBxwn829iCos0RBuRm0Cu1bZnsaszOw5Eorc/edit#gid=1957361665). 


11 - Segmentación elegida 
La segmentación elegida en todos los gráficos es por:
Tipo de propiedad.
Barrio. 
Luego en algunos casos especiales se seleccionó filtros como:
Tipo de divisa/moneda. 
Puntuación de la propiedad.
Período de tiempo - Año. 

12 - Conclusión
Como conclusión podemos decir que se han obtenido datos relevantes en el análisis del dashboard tales como:
El tipo de propiedad u hospedaje más ofrecido y por ende más solicitado es de un ‘Entire home/apt’, el cual dispone de un lugar solo para el huésped, sin compartir espacios comunes. 
Palermo es el barrio con más concentración de hospedajes, por lo que se puede impulsar un crecimiento de negocios en el área. 
Los precios más altos y como era de esperarse, se ofrecen en Puerto Madero, por lo que podemos delimitar la clase monetaria de huéspedes que puede recibir dicha zona a la hora de plantear nuevos negocios u nuevos hospedajes.  
Hasta el día de la fecha el año que más registros de anfitriones ha tenido es el 2016, pero lo más drástico a tener en cuenta fue la cantidad de anfitriones por debajo del promedio que se registraron en la pandemia y como esto tuvo un efecto en la oferta de hospedaje. Este dato se encuentra repuntando en el año 2022.
Los servicios más requeridos y ofrecidos son el Wifi. Ya que estamos en un era moderna que genera la demanda de cantidad de megas en el servicio, es importante que los anfitriones tengan en cuenta que calidad de servicio van a contratar y ofrecer. 
Por último consideramos que Buenos Aires tiene un crecimiento mucho mayor esperado y con los valores y detalles mencionados podemos proyectar ese crecimiento de la mejor manera posible. 


