<h1 align='center'>
 <b>PROYECTO INDIVIDUAL Nº2 - Telecomunicaciones</b>
</h1>
 
<div>
<p>El concepto de telecomunicación abarca todas las formas de comunicación a distancia. Podemos hallar hoy en día numerosas tecnologías, desde la radio, televisión, telefonía, GPS, redes informáticas e Internet.</p>
<p>El internet, por su parte, es una red global de dispositivos interconectados que permite el intercambio de información en tiempo real. Desde su creación, ha tenido un impacto significativo en la vida de las personas, transformando la manera en que nos comunicamos, trabajamos, aprendemos y nos entretenemos.</p>
<p>Desde 1997 hasta 2013, dos tecnologías fueron predominantes en el mercado local: el cablemódem y el ADSL. En Argentina, la red de banda ancha abarca casi la totalidad del país en sus diversas modalidades. En la actualidad, la conexión por Fibra Óptica se convirtió en la segunda tecnología elegida.</p>
</div>

<div>
<p>En este proyecto voy a desarrollar un análisis completo de este sector a nivel nacional con datos provistos de ENACOM.</p>
<p>Voy a trabajar bajo el rol de Data Analyst para una empresa prestadora de <b>servicios de internet</b>.</p>
</div>


<div>
<h2>EDA</h2>
<p>Realicé un análisis de 10 datasets que rondan entre los años 2014 y 2022: 'banda-ancha-provincia.csv', 'banda-ancha-trimestral.csv', 'conectividad-localidad.csv', 'internet-penetracion.csv', 'mbps-provincia.csv', 'rangos-velocidad-prov.csv', 'tecnologia-localidad.csv', 'tecnologia-pronvicia.csv', 'velocidad-localidad.csv', 'velocidad-provincia.csv'. Se pueden visualizar la carpeta [datasets](https://github.com/rebbc/PI_DA/tree/main/datasets) </p>
<p>Utilicé las librerías Pandas para poder explorar las tablas y, MatPlotLib y Seaborn para realizar gráficos.</p>
<p>Me encontré con columnas vacías y filas con datos nulos y outliers, que decidí eliminar. También modifiqué tipos de datos para que puedan ser tomados en cuenta en el análisis. En otros casos, solo tomé columnas específicas para representar.</p>
<p>Profundicé en el acceso a internet por provincia, para ver su evolución en el tiempo y luego poder trabajar con el KPI propuesto.</p>
<p>Investigué sobre el uso de tecnologías, ya que, desde la última década se está implementando la Fibra Óptica, que ofrece a los usuarios un servicio más rápido. Por lo tanto, los datos sobre la velocidad nos pueden brindar información sobre tipos de conexión antiguas.</p>
<p>Para la creación del segundo KPI, analicé y utilicé el dataset 'denuncias-reclamos-2023.csv', también obtenido de la página de ENACOM. Este archivo nos provee la cantidad de reclamos por tipo, dividido por mes.</p>
<p>Para la creación del tercer KPI, analicé y utilicé el dataset 'conexion-fibra-optica.csv', obtenido de la página ARSAT (Empresa Argentina de Soluciones Satelitales S.A.). Este archivo nos muestra la cantidad de puntos de conexión o nodos de la fibra óptica.</p>

<p></p>
</div>

<h2>KPI's</h2>
<div>
<p>1- Se propuso el siguiente KPI: Aumentar en un 2% el acceso al servicio de internet para el próximo trimestre, cada 100 hogares, por provincia.</p>
<p>Para su realización utilicé el dataset '01-internet-acceso.csv', en el que podemos ver el acceso a internet cada 100 hogares, por provincia, dividido por año y trimestre.
El objetivo es aumentar el 2% el acceso a internet. 

<p>La formula del KPI es: ((Nuevo acceso - Acceso actual) / Acceso actual) * 100 </p>
Donde:

- "Nuevo acceso" se refiere al número de hogares con acceso a Internet después del próximo trimestre.
- "Acceso actual" se refiere al número de hogares con acceso a Internet en el trimestre actual.
<p>Se creó la columna "Nuevo acceso" para poder evaluar al KPI.</p>

<p>Ejemplo de uso:</p>
<b>KPI = ((510 - 500) / 500) * 100 = 2%</b>
</div>
<br><br>
<div>
<p>2- Si bien no nos encontramos analizando áreas de atención al cliente, sabemos que el hecho de que haya problemas en el servicio, influye en la pérdida de clientes. "Es decir, el rendimiento de la calidad tiene un efecto positivo sobre la satisfacción del cliente.
(Sandvik y Duhan, 1996)." - Fuente: https://core.ac.uk/download/pdf/161254117.pdf</p>

<p>Por lo tanto, propongo el siguiente KPI: Disminuir un 3% los reclamos por problemas técnicos para el mes siguiente.</p>
La fórmula del KPI es: ((RTecnicos Mes Actual - RTecnicos Mes Anterior)/(RTecnicos Mes Anterior) * 100
Donde:

- "RTecnicos Mes Actual" es la cantidad de reclamos por problemas técnicos del mes siguiente. 
- "RTecnicos Mes Anterior" es la cantidad de reclamos por problemas técnicos del mes anterior.


<p>Ejemplo de uso:</p>
<b>KPI = ((720-743)/743)*100 = -3%</b>
<p>Este KPI nos permitiría implementar mejoras en el servicio, ya sea para detectar fallas técnicas masivas y para prevenir la pérdida de clientes.</p>
</div>

<p>3- Como podemos ver en la sección "Tecnologías por Provincia", entre 2020 y 2021, el acceso a la fibra óptica aumentó un 22%. En este KPI, vamos a buscar aproximarnos a un incremento de puntos de conexión del 20% anual para cada provincia. Los puntos de conexión de fibra óptica son parte de la infraestructura de red, y desde estos puntos, la conexión se distribuye a través de tecnologías adicionales para llegar a los hogares individuales.</p>

<p>La fórmula del KPI es: ((Puntos2023 - Puntos2022) / Puntos2022) * 100</p>
Donde:

- "Puntos 2022" es la suma a nivel nacional de los puntos de conexión para el año analizado.
- "Puntos 2023" es la suma a nivel nacional de los puntos de conexión esperados para el año siguiente.


<p>Si bien no tenemos aún los datos del 2023, este KPI nos propone conseguir o superar los objetivos para cada provincia.</p>

<h2>CONCLUSIONES</h2>
<p>La conectividad a Internet es un factor indispensable para el crecimiento económico y la igualdad de oportunidades para todos los habitantes. Para ello, necesitamos seguir ampliando la infraestrutura y lograr una mejora en nuestros servicios. En relación a los datos analizados, se logró incrementar el acceso a Internet a nivel nacional en los últimos años, y desde la aparición de la Fibra Óptica, muchas tecnologías quedaron en desuso, ya que, la fibra puede brindarnos conexiones más estables y rápidas.</p>
<p>Sabemos que la detección de problemas es un punto de partida para encontrar oportunidades de mejora, por eso, incluí la sección de Reclamos para poder localizar y analizar aquellas provincias donde hay más inconvenientes y poder resolver cuestiones de infraestructura, ya sea la necesidad de expansión de accesos a las residencias o el mantenimiento de los existentes.</p>

<h3>Bibliografía:</h3>
<p>

- https://www.argentina.gob.ar/jefatura/innovacion-publica/telecomunicaciones-y-conectividad/conectar/despliegue-de-la-refefo
- https://datos.arsat.com.ar/dataset/puntos-de-conexion-refefo 
- https://viapais.com.ar/argentina/181153-la-banda-ancha-en-la-argentina-cumple-20-anos-su-historia/'
- https://win.pe/blog/diferencias-fibra-optica-y-cable-coaxial/
- https://core.ac.uk/download/pdf/161254117.pdf

</p>