## Proyecto de Análisis del Servicio de Internet Fijo en Localidades Argentinas

Proyecto de análisis realizado para una empresa prestadora de servicios de telecomunicaciones. El objetivo del proyecto es reconocer el estado del sector a nivel nacional, considerando la actividad principal de la empresa, que es brindar acceso a internet fijo. Con esta información, se busca orientar a la empresa para identificar oportunidades de crecimiento y potenciales clientes. Se utilizan conjuntos de datos públicos proporcionados por ENACOM e INDEC.

### Archivos y Carpetas en el Repositorio
El repositorio contiene los siguientes archivos y carpetas:

EDA-xtreme.ipynb: Jupyter Notebook que contiene el análisis exploratorio de datos (EDA). En este notebook, se documentan los pasos realizados para el análisis, se presentan gráficos y se incluyen conclusiones. También se construyen tres KPIs importantes para el análisis requerido.

/Dataset: Contiene todos los datasets que fueron necesarios para el análisis, los cuales están listados en el apartado "Datasets utilizados".

### Descripción del Proyecto

El presente proyecto emplea herramientas de análisis de datos en Python, tales como pandas, numpy y matplotlib, para investigar el estado del servicio de internet fijo en distintas localidades del territorio argentino.

### Datasets utilizados

Los datasets utilizados en el análisis son los siguientes:
1. `Accesos_Internet_fijo_por_velocidad_bajada_y_localidad.csv`: Contiene información de la cantidad de accesos a internet fijo por velocidad a nivel de localidad.
2. `Conectividad_al_servicio_Internet.csv`: Proporciona información de población y coordenadas geográficas de las localidades.
3. `Accesos_Internet_fijo_por_tecnología_y_localidad.csv`: Contiene información de la cantidad de accesos a internet fijo por tecnología a nivel de localidad.
4. `cnphv2022_resultados_provisionales.xlsx`: Datos del Censo Nacional de Población, Hogares y Viviendas 2022 con información de viviendas y población desagregados por jurisdicción y departamento, partido o comuna.


### Proceso de análisis

Este análisis se enfoca en evaluar el servicio de internet fijo en Argentina, para lo cual se han definido tres KPIs para medir el rendimiento del servicio en diferentes aspectos.

KPI 1: Localidades con una población > 1000 hab. con alto grado de insatisfacción de su servicio de internet fijo.
Se obtiene el total de accesos por localidad y el porcentaje de accesos con una velocidad menor a 10Mbps y menor a 25Mbps. El criterio para determinar que una localidad tiene "alto grado de insatisfacción" es:
- Porcentaje de accesos > 15%, con velocidad < 10Mbps.
- Población > 1000 habitantes.

KPI 2: Partidos con cantidad de viviendas > 10000 y una penetración de internet fijo < 70%.
Se calcula el porcentaje de penetración de internet fijo a nivel de partidos con los datos de accesos del ENACOM y la información de viviendas del último censo obtenida del INDEC. 
El criterio para indicar que un partido cumple con este indicador es:
- Porcentaje de accesos respecto a la cantidad de viviendas < 70%.
- Cantidad de viviendas > 10000. 

KPI 3: Localidades con una población > 1000 hab. con penetración de FO < 50%.
Se calcula el porcentaje de utilización de fibra óptica (FO) como medio de acceso a internet fijo y como tecnología top para brindar este servicio.
El criterio para determinar que una localidad cumple con este indicador es:
- Porcentaje de accesos por fibra óptica respecto al total de accesos < 50%.
- Población > 1000 habitantes.

En resumen, los tres KPIs presentados en el análisis están enfocados en identificar localidades y partidos con problemas en la calidad y penetración del servicio de internet fijo en Argentina. Cada KPI considera diferentes aspectos del servicio y proporciona información valiosa para tomar decisiones y mejorar la calidad de conexión a internet en esas áreas.

### Resultados

El análisis permite identificar:

- Que un 44% de las localidades de Argentina con una población mayor a 1000 habitantes, presentarían un alto grado de insatisfacción con el servicio de internet fijo al tener una velocidad menor a 10Mbps, que es lo mínimo requerido para una navegación básica.

- Que, además, un 4.5% más de localidades, presentarían un grado medio de insatisfacción con el servicio de internet fijo al tener una velocidad menor a 25Mbps (pero mayor a 10Mbps), que es lo recomendado para teletrabajo y streaming.

El análisis también permite identificar los partidos de Argentina con una cantidad de viviendas mayor a 10,000 que presentan una penetración de internet fijo inferior al 70%, los cuales representan el 46% del total de partidos.

Y finalmente, que el porcentaje de utilización de fibra óptica como medio de acceso a internet fijo es del 21%, una tasa cercana al promedio de la región (Latam) del 25%, pero muy baja si la comparamos con el referente de la región, que es Chile, con una tasa de entre 50-60%.

Estos resultados son de gran relevancia para visualizar la gran brecha de mercado en el acceso a internet fijo en diversas regiones del país, y sobretodo identificar dónde está la oportunidad de crecimiento y de adherencia de clientes nuevos.

