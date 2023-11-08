
<p align='center'>
<img src ="https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png"height=150>
<p>
<p align='center'>
<img src = "https://i.imgur.com/0DozeX4.png"height=150> 
<p>
<p align= 'center'>
<img src = "https://i.imgur.com/BeCdvVA.jpg" height=100>
<p>
<h1 align='left'>
 <b>PROYECTO INDIVIDUAL Nº2 - AInsight Data Analytics Company (Gerardo José Cortijo Regalo-Dataft16)</b>
</h1>


## <font color='orange'>Contexto:</font>

Las telecomunicaciones se refieren a la transmisión de información a través de medios electrónicos, como la telefonía, la televisión, la radio y, más recientemente, el internet. Estos medios de comunicación permiten la transmisión de información entre personas, organizaciones y dispositivos a largas distancias.

El internet, por su parte, es una red global de computadoras interconectadas que permite el intercambio de información en tiempo real. Desde su creación, ha tenido un impacto significativo en la vida de las personas, transformando la manera en que nos comunicamos, trabajamos, aprendemos y nos entretenemos.

La industria de las telecomunicaciones ha jugado un papel vital en nuestra sociedad, facilitando la información a escala internacional y permitiendo la comunicación continua incluso en medio de una pandemia mundial. La transferencia de datos y comunicación se realiza en su mayoría a través de internet, líneas telefónicas fijas, telefonía móvil, y en casi cualquier lugar del mundo. 

En comparación con la media mundial, Argentina está a la vanguardia en el desarrollo de las telecomunicaciones, teniendo para el 2020 un total de [62,12 millones de conexiones](https://www.datosmundial.com/america/argentina/telecomunicacion.php). 


## <font color='orange'>Limpieza de datos</font>

*Comencé por descargar todos los archivos xlsx obligatorios de la página de ENACOM, creando un archivo ipynb para realizar primero una limpieza detallada de cada base de datos y su posterior edicion (Orden de columnas, tipo para cada columna,eliminación de nulos y reemplazo de valores erróneos)*

Una vez tenemos nuestro pd.read para cada base de datos, se comenzó realizando una vista de cada uno , para observar los tipos de dato por columna y así poder tenerlos bien definidos.

Como primera medida mi objetivo fué detectar valores nulos, faltantes o duplicados, los cuales no son relevantes para la investigacion que estamos llevando a cabo, permitiendo de ésta manera lograr un mejor desempeño en nuestro *EDA*

Detecté muy pocas incongruencias en los datos, pocos nulos, no había valores duplicados, algunos valores faltantes que se reemplazaron, encontré columnas que me parecieron poco acertivas para la investigación (Como lo es período en algunas tablas), Período nos demarcaba "ene-abr-2014", el cual corresponde a las columnas ya organizadas "Año" y "Trimestre" por lo tanto decidí eliminar Período

Uno de los mayores inconvenientes surgió en los accesos por velocidad, el cual tenia columnas con varios rangos de diferentes velocidades de internet, conteniendo dentro varias filas con el valor "-0", decidí modificarlo de manera óptima reemplazando su valor al correspondiente y cambiar su tipo a entero para una mejor lectura de los mismos.

Para la base de datos *"internet ingresos"* elegí redondear los ingresos a dos decimales, ya que había demasiados y resultarían en una complejidad de lectura a futuro.

Una vez finalizada la examinación de cada base de datos, decidí pasar los datos que me servirían para enfocarme en el KPI a .csv, y tenerlos separados en su carpeta correspondiente para su posterior utilización.




# <font color='lightgreen'>***Librerías utilizadas para la limpieza de los datos***</font>

***pandas*** para la lectura de cada archivo
***Warnings*** para ignorar las alertas de warning al ejecutar los códigos

# <font color='red'>***ACLARACIÓN:***</font>
*Se utilizó la extensión ***"Data Wrangler"*** instalada en visual studio code para el reemplazo de valores incorrectos en las bases de datos explicadas anteriormente (accesos por velocidad por loc, y sin rangos),sumando tambien la revisión en ésta extension para corroborar la precision de nuestros datos*
*Además, se realizo la limpieza de los datasets originales dentro de un archivo ipynb llamado "Limpieza_datos.ipynb" el cual se encuentra déntro de el actual repositorio





Una vez realizado el análisis, selección y limpieza de datos relevantes para nuestro EDA, transformamos nuestros archivos previamente seleccionados y los transformamos en ".csv"

En primera instancia, tuve problemas con la decisión sobre la elección de los datos, por lo tanto mi proyecto se enfocó en realizar el KPI solicitado, por lo cual decidí utilizar 6 bases de datos relacionadas, las cuales son los Accesos a internet en general, por diferentes contextos (velocidad, hogares,etc)

### <font color='Orange'>***Rol a desarrollar:***</font>

En este contexto, un ente regulador de operadoras de internet nos encarga la realización de un **análisis** completo que permita reconocer el comportamiento de este sector a nivel nacional. Considere que la principal actividad de la empresa es brindar **acceso a internet**, pero también es importante considerar el comportamiento asociado al resto de los servicios de comunicación, con el fin de orientar al ente contratista brindar una buena calidad de sus servicios, identificar oportunidades de crecimiento y poder plantear soluciones personalizadas a sus operadoras.


# <font color='lightgreen'>***Análisis exploratorio de datos[EDA]***</font>

![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/Im%C3%A1genesEDA-PowerBI/accesos_100_hogares.png?raw=true)
![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/Im%C3%A1genesEDA-PowerBI/Accesos_a_lo_largo_de_los_a%C3%B1os.png?raw=true)


## <font color='Orange'>***Principales Observaciones a tener en cuenta:***</font>

**Comparación entre Provincias:** El gráfico ofrece una comparación rápida y sencilla del acceso a Internet entre las distintas provincias. Esto facilita la identificación de aquellas con mayor y menor acceso a la web, lo que puede ser valioso para la toma de decisiones estratégicas.

**Tendencias a lo Largo del Tiempo:** Los colores de las barras revelan tendencias de acceso a Internet a lo largo del tiempo en cada provincia. Esto puede ayudar a determinar si el acceso está en aumento, disminución o se mantiene constante.

**Variaciones Estacionales:** La diversidad de colores para cada trimestre posibilita la detección de variaciones estacionales en el acceso a Internet. Esta información es fundamental para la planificación de iniciativas de mejora del servicio.

## <font color='Orange'>***Consideraciones finales:***</font>

Es esencial recordar que este gráfico es una herramienta valiosa para la identificación de tendencias y comparaciones. No obstante, para una comprensión más profunda de los factores que influyen en estas tendencias, se requeriría un análisis más detallado.

 <font color='yellow'>***En resumen:***</font> Este gráfico proporciona una representación clara y concisa del acceso a Internet en diferentes provincias a lo largo del tiempo. Es una herramienta valiosa para la toma de decisiones y la planificación estratégica, facilitando la visualización de tendencias y comparaciones de manera efectiva.




# <font color='Lightgreen'>*Conexiones a internet por provincia*</font>
![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/Im%C3%A1genesEDA-PowerBI/accesos_a_lo_largo_de_los_a%C3%B1os_prov.png?raw=true)






El gráfico generado proporciona una **visión** clara y concisa de la evolución de la conectividad a internet en diferentes provincias a lo largo de los años. Este gráfico de líneas muestra la cantidad de accesos a internet por cada 100 hogares, permitiendo una comparación directa entre las provincias.

Cada provincia se representa con una línea de color único(algunos repetidos), lo que facilita la identificación y comparación de las tendencias a lo largo del tiempo. La leyenda situada a la derecha del gráfico proporciona una referencia rápida para identificar cada provincia por su color correspondiente.
Aunque tengamos colores repetidos, no es un dato que se suponga "relevante" para la investigación, ya que estamos analizando outliers y patrones de tendencias

## <font color='Orange'>Ejes del gráfico</font>
El eje horizontal (X) del gráfico representa el paso del tiempo, mostrando los años en orden cronológico. El eje vertical (Y) muestra la cantidad de accesos a internet por cada 100 hogares, lo que permite una evaluación cuantitativa de la conectividad a internet.

## <font color='orange'>Resumen / Observaciones</font>

En resumen, este gráfico proporciona una representación visual efectiva de la evolución de la conectividad a internet en diferentes provincias a lo largo de los años, permitiendo a los espectadores identificar rápidamente las tendencias y hacer comparaciones entre las provincias.

*A su vez, podemos observar la notoria diferencia entre Capital Federal y las demás provincias que se encuentran dentro de un "rango promedio" de accesos a internet*

*Tambien podemos observar, gracias al gráfico de líneas, que hay una constante tendencia hacia aumentar la cantidad de accesos a internet fijo por cada 100 hogares, aunque en algunas provincias sea más leve que en otras esta curva, todas van en aumento*



 <font color='red'>Nota:</font> Aunque tengamos algunos colores repetidos en las líneas, no es un dato que se suponga *"relevante"* para la investigación, ya que estamos analizando outliers y patrones de tendencias


# ***<font color='lightgreen'>Gráficos evolutivos de Acceso a Banda Ancha Fija por Provincias:</font>***


![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/Im%C3%A1genesEDA-PowerBI/Banda_ancha_por_provincia.png?raw=true)
![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/Im%C3%A1genesEDA-PowerBI/Evolucion_banda_ancha_provincias.png?raw=true)

Dentro de los gráficos que representan el "Acceso a Banda Ancha Fija por Provincia"(gráficos superiores), se muestra una comparación de la cantidad de accesos a Internet a través de la tecnología de "Banda Ancha Fija" en diferentes provincias. Cada barra horizontal corresponde a una provincia específica, y su largo representa el número de accesos de Banda Ancha Fija en esa provincia.

Las barras de error se utilizan para mostrar la variabilidad en los datos, lo que nos ayuda a comprender cuánto varían los valores de acceso a Banda Ancha Fija en cada provincia.

*Este gráfico nos permite visualizar las diferencias en la adopción de la tecnología de Banda Ancha Fija entre las provincias, lo que puede ser útil para identificar áreas donde esta tecnología es más utilizada y áreas donde es menos común.*

Ambos gráficos proporcionan una representación visual de la distribución de accesos a Internet por provincia, lo que puede ser valioso para tomar decisiones informadas en el ámbito de las telecomunicaciones y la infraestructura de Internet.

**<font color='red'>Observación:</font>** Podemos **observar**, viendo los gráficos, que Buenos Aires junto con Capital Federal, Córdobba y Santa Fe son las provincias que poseen más acceso a banda ancha fija a lo largo de los años.


# ***<font color='lightgreen'>Migración de Dial Up a otras tecnologías:</font>***
 
![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/Im%C3%A1genesEDA-PowerBI/evolucion_dial_up.png?raw=true)

**<font color='lightgreen'>Observación:</font>** *Podemos notar en el gráfico que se observa arriba, la evolución, o "migración" de las provincias respecto al dial up y las nuevas tecnologías a lo largo de los años,pero...***¿A qué se debe ésto?.**

La conexión "dial-up" es una tecnología de acceso a Internet que fue ampliamente utilizada en las décadas de 1990 y principios de 2000. El término "dial-up" se deriva de la forma en que se establece la conexión, a través de la marcación de un número telefónico utilizando un módem. Aquí hay una descripción básica de cómo funciona:

**<font color='lightblue'>Módem:</font>** *Un módem (abreviatura de "modulador-demodulador") es un dispositivo que se conecta a una computadora y a una línea telefónica. Transforma las señales digitales de la computadora en señales analógicas que pueden viajar a través de la red telefónica.*

**<font color='lightblue'>Marcación:</font>** *Cuando una computadora con un módem quiere conectarse a Internet, marca un número telefónico específico de un proveedor de servicios de Internet (ISP). Este número se conoce como "número de acceso" del ISP.*

**<font color='lightblue'>Establecimiento de la conexión:</font>** *El módem realiza una serie de sonidos conocidos como "apretón de manos" con el módem del ISP. Estos sonidos permiten que los dos módems se comuniquen y establezcan una conexión.*

**<font color='lightblue'>Conexión a Internet:</font>** Una vez que se ha establecido la conexión, la computadora puede enviar y recibir datos a través de la línea telefónica. Sin embargo, las velocidades de transmisión de datos en una conexión dial-up son bastante lentas en comparación con las conexiones modernas de banda ancha, generalmente limitadas a velocidades de 56 kbps o menos.

**<font color='lightblue'>Facturación por tiempo:</font>** En muchos casos, las conexiones dial-up se facturaban por tiempo, lo que significaba que los usuarios pagaban por la cantidad de tiempo que pasaban en línea, lo que fomentaba la moderación en el uso de Internet.

Aunque las conexiones dial-up fueron ampliamente utilizadas en su momento, han sido en gran medida reemplazadas por tecnologías de banda ancha más rápidas y eficientes, como DSL, cable, fibra óptica y conexiones inalámbricas. Las conexiones dial-up tenían la desventaja de ser lentas y ocupar la línea telefónica, por lo que no permitían realizar llamadas telefónicas simultáneas. A medida que las velocidades de Internet y las opciones de conectividad mejoraron, las conexiones dial-up se volvieron menos comunes y obsoletas.

 ## ***La siguiente imagen tiene como objetivo contextualizar lo anteriormente mencionado para nuestro gráfico:***

![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/Im%C3%A1genesEDA-PowerBI/Archivo_Enacom.png?raw=true)



# <font color='lightgreen'>***Accesos por Tecnología a lo largo de los años***</font>

![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/Im%C3%A1genesEDA-PowerBI/evolucion_diferentes_tec.png?raw=true)
![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/Im%C3%A1genesEDA-PowerBI/Acceso_tecnologias.png?raw=true)

En el siguiente gráfico de líneas y de barras, podemos notar una evolución constante en búsqueda y establecimiento de nuevas tecnologías, las más utilizadas en éstos dias son "Cablemodem" y "Fibra óptica" siendo éstas las más rapidas a la hora de establecer una correcta conectividad para el usuario, en la sección "Otros", logramos detectar una pendiente negativa, la cual nos indica que tecnologías como "Dial up" por ejemplo, entraron en desuso a partir del 2016, decayendo fuertemente luego de 2018, junto con quizá otras tecnologías igual de obsoletas, las tecnologías como ADSL y Wireless no han tenido mucha evolución positiva o negativa hasta el momento, lo cual implicaría una revisión acerca de éstas tecnologías.

Como es de público conocimiento, la tecnología avanza a pasos agigantados, cada vez son más las compañias, pequeñas empresas, comercios y emprendedores que, desde la pandemia del COVID, lograron expandir el negocio a través de las redes (ya que en esos tiempos era muy limitado el contacto humano), ésta búsqueda de expansión las llevo a una evolución tecnologica en cuanto a los accesos a internet, como podemos denotar en el gráfico, sumando a ésto que la mayoría de trabajadores presenciales tuvieron que pasar a ser trabajadores remotos 


# <font color='lightgreen'>***Evolución de ingresos de diferentes operadores de red a lo largo de los años:***</font>
![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/Im%C3%A1genesEDA-PowerBI/Evolucion_ingresos.png?raw=true)

El gráfico muestra la evolución de los ingresos (en miles de pesos) por trimestre a lo largo del tiempo. Los datos se presentan como una serie temporal, con los trimestres en el eje x y los ingresos en el eje y.

La línea en el gráfico representa la tendencia de los ingresos a lo largo del tiempo. Se puede observar que la línea tiene una pendiente generalmente positiva, lo que indica que los ingresos han estado aumentando a lo largo del tiempo.

Un punto de inflexión notable en el gráfico ocurre alrededor de 2019, donde la línea comienza a subir a un ritmo más rápido. Esto sugiere que hubo un "despegue" en los ingresos en este punto, con un crecimiento acelerado desde entonces.

Es importante destacar que, aunque la tendencia general es positiva, también hay fluctuaciones de un trimestre a otro. Estas fluctuaciones podrían deberse a una variedad de factores, como las condiciones del mercado, las estrategias de la empresa o los eventos estacionales.

En resumen, el gráfico muestra una tendencia positiva en los ingresos a lo largo del tiempo, con un crecimiento particularmente fuerte a partir de 2019. Sin embargo, también destaca la importancia de considerar las fluctuaciones trimestrales al interpretar estos datos.

*En conjunto*, estos gráficos indican un progreso continuo en la infraestructura de Internet y en la adopción de tecnologías más avanzadas en Argentina a partir de 2019. Esto puede tener un impacto positivo en el acceso a la información, la comunicación y el desarrollo económico en el país. Es importante seguir monitoreando estas tendencias para garantizar que la conectividad a Internet siga siendo accesible y eficiente para todos los ciudadanos.

# <font color='lightgreen'>***Conclusión***</font>
En conclusión, gracias a los graficos proporcionados y a los datos que los crearon, podemos deducir en general una curva positiva para el avance en cuanto a la conectividad a internet dentro de la Argentina, aunque se denota una inconsistencia dentro de la equidad sobre los accesos a ciertas tecnologias, puedo que esto esté directa o indirectamente relacionado a planes políticos, densidad de población y/o demanda por provincia debido a la densidad poblacional, hay bastantes factores a tener en cuenta, el principal que se observa al principio, es la notoria diferencia entre capital federal(buenos aires), y las demás provincias para las relaciones en accesos a tecnologia, por ejemplo, muchas provincias aún cuentan con elevados valores de "Dial up", un tipo de conexion a internet "arcaica" por así decirlo, la media de provincias que tienen una red deficiente varía en cuanto mas nos alejamos de capital federal, las provincias de el sur tienen menos calidad de internet y acceso a él.

Otro de los datos a añadir es la eficiente y rápida transformación de la tecnologías a una mejor calidad de acceso, "Dial up" decayó bastante en el contexto social de el "COVID-19", ésto debe suceder por la misma cuarentena que hizo que la gente utilice más sus conexiones a internet, sobretodo para estar al tanto de la situación social vivida en ese momento, se dejó denotar que hubo planes de contencion en las redes y su acceso a ellas(adjunto imagenes debajo) 

![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/fotosENACOM/25mar2020.png?raw=true)

![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/fotosENACOM/24mar2020.png?raw=true)
![Descripción de la imagen](https://github.com/Gerard175dnb/AInsights_PIDA/blob/main/Im%C3%A1genes/fotosENACOM/Comparativo20_21.jpg?raw=true)


# <font color='lightgreen'>***Informe de análisis en powerBi***</font>
En este informe, describiré los pasos que seguí en Power BI para crear gráficos comparativos que muestran la cantidad de accesos a Internet cada 100 hogares por provincia. El objetivo de este análisis es identificar las diferencias en la disponibilidad de Internet en las diferentes provincias.


# <font color='lightgreen'>***KPI número 1 solicitado(incremento del 2% de accesos por hogar por trimestre)***</font>
Para el siguiente KPI, nos solicitan realizar una comparativa de trimestres (trimestre actual vs trimestre siguiente) en la cual debemos denotar un incremento del 2% en el siguiente trimestre, basándonos en los accesos cada 100 hogares, la fórmula realizada es la siguiente:

##  <font color='cyan'>***Calendario***</font>

Realicé una nueva medida aparte llamada calendario (date) con la cual puedo enlazar los primedios de mis KPI por fecha(año,trimestre,mes,etc)
*Calendario = CALENDAR(DATE(2014,1,1),DATE(2022, 12, 31))*
## <font color='cyan'>***Fecha***</font>
Se realizó una medida en la cual especificamos las fechas en base a los trimestres, mes 9 corresponde al trimestre 3, mes 12 al trimestre 4 y así sucesivamente.

## <font color='cyan'>***Acceso actual(trimestre seleccionado)***</font>
Realizamos la medida "Nuevo acceso = AVERAGE(Acceso_hogares[Accesos por cada 100 hogares])" la cual tomará un promedio entre los accesos
## <font color='cyan'>***Acceso anterior***</font>
Realizamos la medida "Acceso anterior = CALCULATE([Nuevo acceso],PREVIOUSQUARTER(calendario[Date]))" la cual tomará en comparativa el trimestre seleccionado con el trimestre anterior, logrando asi observar el índice de rendimiento

## <font color='cyan'>***Objetivo***</font>
Realizamos la medida objetivo, la cual es : "KPIobjetivo = ([Nuevo acceso]/[Acceso anterior]) - 1", logrando obtener el promedio de nuestro indice de rendimiento

## <font color='cyan'>***Destino***</font>
Realizamos la medida destino, la cual es "Destino = 0.02" para mostrar el rendimiento del 2% sobre la comparativa de trimestres, esperando observar graficamente si se cumple o no con lo solicitado 


# <font color='lightgreen'>***KPI número 2(Posible incremento del 15% en la tecnología "Fibra óptica")***</font>

Para el KPI que creé, investigué las tablas armadas y observé que podría ser viable un aumento del 15% en el acceso a la tecnologia "fibra optica" anual, lo cual voy a detallar a continuacion los pasos que realice:

## <font color='yellow'>***Velocidad nueva**</font>
Realizamos la medida "*Velocidad nueva = AVERAGE(historico_velocidad_internet[Mbps (Media de bajada)])*" la cual tomará un promedio entre las velocidades

## <font color='yellow'>***Velocidad anterior**</font>
Realice la medida "*Velocidad anterior = CALCULATE([Velocidad nueva],PREVIOUSQUARTER(calendario[Date]))*"
para obtener la comparativa entre la velocidad anterior y la nueva velocidad



## <font color='yellow'>***Objetivo**</font>
Realizamos la medida objetivo, la cual es : "*Objetivo = ([Velocidad nueva]/[Velocidad anterior]) - 1*", logrando obtener el promedio de nuestro indice de rendimiento para la fibra optica 

## <font color='yellow'>***Destino**</font>
Realizamos la medida destino, la cual es "VelocidadObjetivo = 0.15" para mostrar el posible rendimiento del 15% sobre la comparativa de trimestres, esperando observar graficamente si se cumple o no con lo solicitado 


¡Gracias por leer este informe!

Gerardo José Cortijo Regalo - Henry DataFT16
