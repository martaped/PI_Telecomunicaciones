# [Análisis de Datos para importante Empresa de Telecomunicaciones](#presentacion-info) 
## [Con énfasis en la distribución de accesos de Fibra Optica y ADSL](#presentacion-info) 


1. [Presentación Personal](#presentacion-info)

2. [Introducción](#Comentarios-introductorios)

3. [Análisis Exploratorio de Datos](#ETL-EDA)

4. [Inclusión de Dataset adicional geográfico para Penetración de Internet](#ETL_penetracionI.ipynb)

5. [Transformacón para Ingresos por Tecnología](#IngresosYaccesos.ipynb)

6. [KPIs y Conclusiones](#Conclusiones)

7. [Link al Dashboard en Power BI](#Conclusiones)

    https://app.powerbi.com/view?r=eyJrIjoiNjY0ZjRmMDItNTNiYi00OTExLThkMWEtNDZjMzY3MDEzZTBkIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9



![Image text](data/Telecomunicaciones.webp)


## Presentación Personal
***
<p align="justify">
  
Soy **Marta Inés Pedriel**, licenciada en Análisis de Sistemas, Master en Administración de Servicios de Salud. Con experiencia en programación y análisis. En la actualidad me desarrolo como profesora de Matemática de Media y de Progamación y Estructuras de datos en Media.
Estoy culminando también la carrera de Ciencia de Datos en SoyHenry a los fines de actualizarme en el manejo de las nuevas tecnologías y requerimientos del mercado.


## Introducción
*** 

He sido contratada por una **Empresa de Telecomunicaciones**, la cual quiere conocer el comportamiento de los accesos a Internet a nivel nacional, dentro de la Republica Argentina. He decidido analizar el comportamiento de los accesos a Internet en todo el país.
La principal actividad de la empresa es brindar acceso a internet en Fibra óptica o ADSL,  siendo los pilares fundamentales de nuestra empresa.
Debi explorar y entender el panorama general de los servicios de comunicación,pero también debí considerar el comportamiento asociado al resto de los servicios de comunicación, con el fin de orientar a la empresa en oportunidades de crecimiento y mejoras de servicio.

Como parte de mi contribución a este equipo, he iniciado un proyecto integral para comprender el comportamiento de los accesos a Internet a nivel nacional, cuyo resultado cúlmine es un ** Dashboard interactivo en Power Bi. **

## Objetivo del Proyecto:

Analizar el comportamiento de los accesos a Internet en todo el país.
Centrarse en los servicios de Fibra Óptica y ADSL, siendo los pilares fundamentales de nuestra empresa.
Explorar y entender el panorama general de los servicios de comunicación en busca de oportunidades de crecimiento y mejoras de servicio.

## Fuentes de Datos:

<div class=text-justify> Cuento con la API de Enacom - Ente Nacional de Comunicaciones de Argentina -para tomar información al respecto https://datosabiertos.enacom.gob.ar/home - A pesar de las dificultades, he obtenido datos cruciales de acceso a Internet. Estos datos, formato CSV, nos brindaron información detallada sobre la utilización y distribución de servicios.

Se descargaron los datos en csv, por fallas en la api. Dichos archivos fueron numerados del 01 al 16 para no confundir los mismos.

Dataset de Ubicación de Localidades del Gobierno Argentino: ademas para completar la información he tomado la ubicación de localidades del dataset de servicios normalizados de Gobierno argentino https://datos.gob.ar/ar/dataset/jgm-servicio-normalizacion-datos-geograficos/archivo/jgm_8.14
Con ello he complementado con datos geográficos para un análisis más completo.

## Análisis Exploratorio de Datos

Lo primero que realice es una visualización total de la información aportada por la pagina de Enacom respecto a la conectvidad a internet. 
Mediante un notebook de Visual Estudio en:

### python EDA.ipynb 

En este EDA puedes observar un ETL mas EDA , recorrido por todas las tablas, transformaciones de datos y Graficos. Con los comentarios pertinentes asociados a lectura de datos, transformaciones y gráficos.

Pude descargar los archivos cvs en dataframes a los fines de observar, limpiar y analizar los mismos. Para luego cruzar datos y quedarme con los mas convenientes.
Primero decidi evaluar el que mayor cantidad de información aporta, o sea con localidades, provincias y los diversos tipos de conectividades.

Luego decidi numerar los csv que son 16 a los fines de no confundir tablas que contienen en muchos casos datos similares. 
Hice la lectura de los archivos csv, su análisis de datos, mediante recuento de datos y graficos, ademas de la eliminación de nulos y columnas innecesarias.

Se observa que la información esta discriminada por Año Trimestre, con lo cual no hay detalle de dias y fechas excactas. A los fines practicos y para el desarrollo de los KPI en power Bi decidi agregar fecha a algunas de las tablas.



## Incluyo Dataset adicional geográfico para observar la Penetración de Internet

Es específico para ver la penetracion de internet en forma geografica por Provincia y localidad, para ello utilice información aportada por el gobierno, indicada en Fuente de Datos de este readme.

Se realizo el merge de la data de las localidades con su latitud y longitud. Para ello he tenido que transformar y normalizar nombres de provincia y localidades.
### ETL_penetracionI.ipynb


## Transformación de datos para ver los Ingresos por Tecnología

En este Notebook se cruzan los datos de accesos por tecnologia de Internet fijo por trimestre y los ingresos por Trimestre.

### IngresosYaccesos.ipynb

## Análisis y Conclusión: Accesos y Fibra Óptica

Se propone un **KPI orientado** a aumentar los accesos por cada 100 habitantes  en un 2%* trimestre a trimestre. Sin embargo, se observa una variabilidad en el cumplimiento del objetivo, con la mayoría de los trimestres sin alcanzar la meta, aunque en algunos casos se ha superado ampliamente, llegando incluso al 8%.

En particular, el crecimiento ambicioso del 5% trimestral - marcado con un **KPI para la Fibra Óptica** ha tenido resultados positivos en pocas ocasiones. Este indicador señala áreas de oportunidad para mejorar la expansión de la conectividad en dicha tecnología.

## [**Conclusiones**](#presentacion-info)

A partir del Analisis de Datos y el Dashboard asociados se puede concluir:

### [**Conectividad en Crecimiento**](#presentacion-info)

A pesar de la variabilidad en el cumplimiento trimestral, la conectividad muestra una tendencia general creciente.

### [**Diferencias Regionales**](#presentacion-info)

Se identifican disparidades significativas entre provincias, destacándose Capital Federal, Buenos Aires y Córdoba como líderes en conectividad. Sin embargo, hay muchas provincias con una baja cantidad de accesos, señalando áreas clave para mejorar.

### [**Desafíos en Fibra Óptica:**](#presentacion-info)

Aunque hay un crecimiento en el uso de Fibra Óptica en los últimos años, se evidencia la necesidad de un enfoque más específico para cumplir con el ambicioso objetivo del 5% trimestral.

### [**Oportunidades de Crecimiento:**](#presentacion-info)

Se sugiere que la empresa de tecnología centre sus esfuerzos en conectar  localidades con una ausencia notable de Fibra Óptica. Este enfoque estratégico podría aprovechar al máximo el potencial de crecimiento en áreas aún no atendidas.
Este análisis proporciona una base sólida para tomar decisiones informadas y desarrollar estrategias que impulsen la expansión y mejora de la conectividad, alineadas con los objetivos específicos de la empresa.</p>







***
Lista de las tecnologias usada en este proyecto:
* [Visual Estudio Code]
* [Python]: Version 3.10.10
* [Power Bi for Desktop]