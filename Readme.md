<h2 align='center' style="font-weight:light; text-align:justify; margin-left: 80px; margin-right: 100px;">
<div align="center">
  <h2>Proyecto Individual Nº 2: DATA ANALYTICS</h2>
</div>

<h1 align='center'>
<img src="IoT & Minería.png" width="1000"> 

<h2 align='center' style="font-weight:light; text-align:justify; margin-left: 80px; margin-right: 100px;">
<div align="center">
<h2>Análisis de Factibilidad para inversiones en el rubro Minero</h2>
</div>


# Introducción:
<h3>
En este laboratorio individual de <em>Data Analytics</em> (DA), asumiré el rol de un <em>Analista de Datos</em> pertenciente a la empresa tecnológica <strong>IoT InnOvaTions.</strong>(empresa ficticia) <br>
<h4 align='center'>
<img src="Logo IoT 2.png" width="100"></h4>
<h3>
Basándome en la información provista por el <strong>ENACOM</strong> más la generada a partir de los datos disponibles en el sitio web de la <strong>Cámara Argentina de Minería</strong> se buscará orientar a la empresa para identificar la mejor oportunidad de inversión en un nuevo rubro.


# Archivos y Carpetas en el Repositorio
<h3>
<p> El repositorio contiene los siguientes archivos y carpetas:<br>
<ul><li>Lab02_EDA.ipynb: Jupyter Notebook que contiene el análisis exploratorio de datos (EDA). Se documentan los pasos realizados para el análisis, se presentan gráficos y se incluyen algunas conclusiones a partir de los mismos.</li><br>
<li>Informe_proyecto_IoTMinero.pbix: Daxhboard con las visualizaciones calve que permiten orientar en la toma de decisiones para las posibles inversiones. Se presentan allí 3 KPIs que permitirán realizar la evaluación del análisis.</li><br>
<li>/Dataset: contiene los archivos que fueron utilizados para el análisis tanto del EDA como para su posterior aprovechamiento en el Dasboard.</li></ul><br>

# Descripción del Proyecto:
<h3> <strong><p> IoT InnOvaTions</strong> es una empresa especializada en integrar y ofrecer soluciones IoT llave en mano, con experiencia en distintos rubros (industria automtotriz, empresas alimenticias, sistema de salud, entre otros).<br><p>
<p> Se me ha encomendado realizar un análisis de factibilidad para la apertura de una nueva división dentro de la empresa con el objetivo de incursionar en el rubro de las empresas mineras. Esta nueva división se identificará con el nombre de <em><strong>SmartMine</em></strong>
<h4 align='center'>
<img src="logo SmartMine con texto.png" width="120"></h4>
<h3><p> Para este fin se cuenta con información obtenida desde el <strong>ENACOM</strong>, el cual proporciona datos referentes al alcance de la tecnología disponible en Argentina para el rubro telecomunicaciones en general, el grado de cobertura por localidades y nivel de población, y también información referida al tipo de tecnología disponible para el acceso a internet, contemplando la velocidad de acceso.
<p> Para investigar el grado de factibilidad de incursionar en el rubro minero, se focalizó el análisis sobre 4 provincias de la región oeste de Argentina, en donde se desarrolla mayormente esta actividad. Las provincias seleccionadas fueron <strong>Catamarca</strong>, <strong>Mendoza</strong>, <strong>Neuquén</strong>, y <strong>San Juan</strong>. Esta información fue recolectada a partir de los registros públicos de la <strong>Cámara Argentina de Minería</strong>, de donde se extrajeron los datos de los proyectos mineros presentes en las provincias mencionadas. Estos datos permitieron crear un dataset en donde se colocó el nombre de cada proyecto, la provincia en la que se encuentra ubicado, y los minerales que se explotan en dichos yacimientos. Para poder contar con la ubicación geográfica de los mismos (latitud y longitud) ser recurrió a <strong>Google Earth</strong>, información que también se incorporó al dataset mencionado.
<p> Con respecto a la implementación de soluciones IoT en el campo minero, sólo focalizaré el análisis en 3 segmentos de velocidad.
<ul><li> El primero, para funciones de registro de sensores para monitoreo ambiental. En este caso, dependiendo de la cantidad de sensores y de la frecuencia de actualización de los datos de ubicación y estado, los rangos de ancho de banda pueden ir desde unos pocos kbps hasta 5Mbps.</li><br>
<li>El segundo estaría orientado al monitoreo remoto y gestión de equipamiento, en donde se requiere un ancho de banda medio a alto (de 5Mbps hasta 20 Mbps).</li><br>
<li>El tercer y último segmento estaría destinado a aplicaciones de gestión de activos y logística, como seguimiento en tiempo real de vehículos, equipos y materiales. Para estas aplicaciones es necesario contar con un ancho de banda alto, que puede ir desde 20Mbps hasta 100 Mbps, dependiendo del número de dispositivos rastreados y la frecuencia de actualización de ubicación y estado.</li></ul><br>
<p>Considerando estos 3 segmentos, podemos clasificar las distintas tecnologías de acceso a internet de acuerdo a los rangos de ancho de banda (<em>BW</em>):
<ul><li><strong>Registro de Sensores y Monitoreo Ambiental</strong>: ADSL, con un BW menor a 5Mbps</li><br>
<li><strong>Monitoreo Remoto y Gestión de Equipamiento</strong>: 3G, 4G, Wireless (conexión punto a punto con antenas), con un BW de 5Mbbps hasta 20 Mbps</li><br>
<li><strong>Gestión de Activos y Logística (seguimiento en tiempo real de vehículos, equipos y materiales)</strong>: 4G, Fibra Óptica, Satelital, con un BW de 20Mbps hasta 100 Mbps</li></ul><br>
<p>La propuesta de inversión se tomará considerando tres factores (KPIs):
<ol><li><strong>Volumen de Mercado:</strong> para que la incursión en este nuevo rubro se considere justificable, se ha considerado cubrir al menos la mitad más uno de los proyectos disponibles en la región evaluada. Para los números actuales que se cuenta con 13 proyectos activos en la región, lo deseable sería cubrir al menos 7 de estos proyectos.</li><br>
<li><strong>Conectividad Disponible:</strong> con el objeto de aprovechar al máximo los recursos tecnológicos instalados, se evaluará también la conectividad disponibles en las poblaciones y localidades más cercanas a cada uno de los proyectos mineros. Se fijo como valor mínimo, un total de ocho (8) conexiones o accesos.</li><br>
<li><strong>Costo Obras:</strong> debido a que el emplazamiento de los proyectos mineros se encuentran por lo general alejados de las poblaciones, se considerará la distancia a la localidad más cercana que cuente con conectividad. Este valor de la distancia servirá como indicador del volumen de obras que debrán llevarse a cabo para poder implementar el trabajo. Entre otras tareas se pueden mencionar obras de tendido de cables o fibras, montaje de antes y obras civiles asociadas. También permitirá dimensionar los costos vinculados a la cantidad de metros necesarios de cable o fibra, y a la capacidad de los equipos de transmisión. La distancia máxima considerada como óptima para esta primera incursión en el rubro minero no deberá superar los 720km, contemplando la suma de las distancias entre cada proyecto analizado y la población más cercana al mismo.</li></ol><br>
<p>Para la decisión final se espera que al menos dos (2) de los tres (3) KPIs sean alcanzados.
<p>Una vez definido esto, se determinará, considerando el tipo de tecnología disponible en la proximidad del proyecto, qué servicio se podrá empezar a ensayar para su posterior implementación.

</h3>"# Lab02_Data-Analytics" 
