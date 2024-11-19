# Telecom-Data-Analysis

## Introducción

El objetivo de este **análisis exploratorio de datos (EDA)** es examinar el estado actual del sector de telecomunicaciones en Argentina. A través de la investigación de métricas clave y tendencias, este análisis busca brindar una visión profunda de la estructura, desempeño y desafíos del sector.

Como fuentes de datos se utilizarán tres Datasets de dos fuentes distintas, los cuales se encuentran de la siguiente manera:

[ENACOM:](https://indicadores.enacom.gob.ar/datos-abiertos)

- **Internet.xlsx:** Consiste en una serie de tablas con datos relativos al uso de internet en las distintas provincias argentinas.
- **mapa_conectividad.xlsx:** Tabla donde se incluyen todas las provincias, partidos y localidades argentinas con su respectiva población, ubicación geográfica y tipo de tecnologías de telecomunicaciones que se encuentran soportadas.

[OECD:](https://data-explorer.oecd.org/)

- **Broaband.csv:** Total de suscripciones a redes móviles y fijas dentro de los países pertenecientes a la OECD.

## Insights

### Accesos por Provincia

Como podemos observar en el gráfico, la provincia de **Buenos Aires** es la que mayor número de accesos tiene con casi **5 Millones**, por otro lado las provincias de **Caba, Córdoba y Santa fe** son las que superan el **millón de accesos**, y el **resto de las provincias** no sobrepasan los **500 mil accesos**.

En este gráfico se puede deducir que la mayoría de las provincias argentinas cuentan con muy pocos accesos en comparación de las cuatro antes mencionadas, derivado de esto es necesario analizar el total de población de estas provincias para así comprobar si este fenómeno se debe a la densidad de población o existe una brecha tecnológica muy grande entre las provincias argentinas.

![Accesos por Provincia.](/assets/img/Accesos%20por%20Provincia.png)

### Evolucion Trimestral de la Cantidad de Accesos por Tecnologia

Como podemos apreciar en esta gráfica, el uso de **Cablemodem** es la tecnología de acceso a internet **más popular** desde el segundo Trimestre del 2017, a su vez otro punto importante a destacar es como **el ADSL ha dejado de ser usado para nuevos accesos** desde ese mismo trimestre y su uso ha ido disminuyendo paulatinamente a lo largo de los trimestres.

Un último punto que podemos apreciar desde el **cuarto trimestre del 2021**, la **Fibra óptica** ha ido en **aumento** y el Cablemodem no registra grandes cambios en la cantidad de nuevos accesos, por lo que podríamos deducir que la **Fibra óptica podría llegar a ser la nueva tecnologia mas usada en los próximos años** y el Cablemodem empezaría a dejar de ser usado como ha sucedido con el ADSL.

![Evolucion Trimestral de la Cantidad de Accesos por Tecnologia](/assets/img/Evolucion%20Trimestral%20de%20la%20Cantidad%20de%20Accesos%20por%20Tecnologia.png)

### Accesos por cada 100 habitantes en paises de latinoamerica y la media de la OCDE

Como podemos observar en este gráfico la cantidad de accesos por cada 100 habitantes en Argentina sobrepasa ligeramente la cantidad de accesos de los países latinoamericanos pertenecientes al OCDE, pero aun se encuentra muy por debajo de la media de la OCDE.

![Accesos por cada 100 habitantes en paises de latinoamerica y la media de la OCDE](/assets/img/Accesos%20por%20cada%20100%20habitantes%20en%20paises%20de%20latinoamerica%20y%20la%20media%20de%20la%20OCDE.png)

## KPIs

De acuerdo a los datos previamente analizados se presentan tres KPIs que ayudarán a medir de una forma SMART el avance del sector de telecomunicaciones en Argentina.

### 1. Aumentar en un 2% el acceso al servicio de internet para el próximo trimestre, cada 100 habitante, por provincia.

*KPI = ((NuevoAcceso - AccesoActual) / AccesoActual) * 100*

Donde:

- **Nuevo acceso** se refiere al número de habitantes con acceso a Internet después del próximo trimestre.
- **Acceso actual** se refiere al número de habitantes con acceso a Internet en el trimestre actual.

### 2. Superar en un 15% los accesos al servicio de internet por cada 100 habitantes, con respecto a la media de la OCDE en cada trimestre.

*KPI = ((MediaOCDE - AccesoActual) / AccesoActual) * 100*

Donde:

- **MediaOCDE** se refiere a al media del número de habitantes con acceso a Internet de los paises dentro de la OCDE de cada trimestre.
- **Acceso actual** se refiere al número de habitantes con acceso a Internet en el trimestre actual.

### 3. Migrar en un 5% trimestral, los accesos a Internet con tecnologia de cobre a Fibra Optica.

*KPI = (AccesosCobreAnterior - AccesosCobre) / (AccesosCobre + AccesosFibra) * 100*

Donde:

- **AccesosCobreAnterior** se refiere a la cantidad de accesos a internet con tecnologias ADSL y Cablemodem del trimestre anterior.
- **AccesosCobre** se refiere a la cantidad de accesos a internet con tecnologias ADSL y Cablemodem del trimestre actual.
- **AccesosFibra** se refiere a la cantidad de accesos a internet con Fibra optica del trimestre aactual.
