# Análisis geoespacial del sistema sanitario de Madrid

## Descripción

Esta segunda parte del proyecto amplía el análisis inicial
del sistema sanitario de Madrid incorporando una dimensión
geográfica y poblacional.

El objetivo es analizar cómo se distribuyen los centros
sanitarios entre los diferentes distritos de Madrid y
estudiar su cobertura en relación con la población.

Para ello, se combinan los datos de los centros sanitarios
con información geográfica de los distritos y datos de
población, aplicando técnicas de análisis geoespacial
con Python.

## Objetivos

El análisis busca responder principalmente a las siguientes
preguntas:

- ¿Cómo se distribuyen los centros sanitarios entre
  los diferentes distritos de Madrid?

- ¿Qué distritos concentran un mayor número de centros?

- ¿Qué distritos presentan una mayor cobertura sanitaria
  en relación con su población?

- ¿Existen diferencias territoriales en la distribución
  relativa de los centros sanitarios?

- ¿Cómo puede representarse espacialmente esta información
  mediante mapas?

## Tecnologías utilizadas

- Python

- Pandas

- GeoPandas

- Shapely

- Matplotlib

## Proceso de análisis

1. Carga de los datos de los centros sanitarios.

2. Creación de las geometrías a partir de las coordenadas
   geográficas de los centros.

3. Carga de la cartografía de los distritos de Madrid.

4. Comprobación y adaptación de los sistemas de referencia
   de coordenadas (CRS).

5. Realización de una unión espacial (Spatial Join)
   entre los centros sanitarios y los distritos.

6. Análisis del número de centros sanitarios por distrito.

7. Carga y preparación de los datos de población.

8. Agrupación de la población por distrito.

9. Integración de los datos de centros sanitarios
   y población.

10. Cálculo del número de centros por cada
    10.000 habitantes.

11. Representación cartográfica de la cobertura sanitaria.

12. Comparación de los distritos según su cobertura
    respecto a la media.

13. Identificación de los distritos con mayor y menor
    cobertura relativa.

14. Elaboración de conclusiones.

## Principales resultados

El conjunto analizado contiene **277 centros sanitarios**
distribuidos entre los **21 distritos de Madrid**.

En términos absolutos, **Fuencarral - El Pardo** presenta
el mayor número de centros, con **22**, seguido de
**Salamanca**, con 21, y de **Latina** y **Chamberí**,
con 20 centros cada uno.

Por el contrario, **Barajas** presenta el menor número
de centros, con 4, seguido de **Moratalaz**, con 5,
y **Vicálvaro**, con 6.

Sin embargo, el número absoluto de centros no permite
comparar de forma adecuada la cobertura sanitaria entre
distritos, ya que la población es diferente en cada uno.

Por este motivo, se ha calculado un indicador basado en
el número de centros sanitarios por cada 10.000 habitantes.

Los resultados muestran que **Moncloa - Aravaca** presenta
la mayor cobertura relativa, con **1,50 centros por cada
10.000 habitantes**.

Le siguen **Salamanca**, con 1,43, y **Chamberí**, con 1,41
centros por cada 10.000 habitantes.

En el extremo contrario se encuentra **Carabanchel**, con
**0,47 centros por cada 10.000 habitantes**, seguido de
**Moratalaz**, con 0,53, y **Villa de Vallecas**, con 0,55.

Estos resultados muestran que disponer de un mayor número
de centros no implica necesariamente una mayor cobertura
relativa.

La incorporación de los datos de población permite obtener
una visión más equilibrada de la distribución territorial
de los servicios sanitarios.

## Visualización

La información geográfica se representa mediante mapas
realizados con GeoPandas y Matplotlib.

La cartografía permite visualizar la distribución de los
centros sanitarios y analizar las diferencias de cobertura
entre los distintos distritos de Madrid.

El mapa de cobertura representa el número de centros
sanitarios por cada 10.000 habitantes en cada distrito.

## Conclusiones

El análisis geoespacial permite complementar el estudio
realizado en la primera parte del proyecto incorporando
la dimensión territorial y poblacional.

El uso conjunto de Pandas, GeoPandas, Shapely y Matplotlib
permite integrar diferentes fuentes de información, realizar
operaciones espaciales, construir indicadores y representar
los resultados mediante mapas.

Los resultados muestran diferencias en la cobertura relativa
de los servicios sanitarios entre los distintos distritos.

No obstante, el indicador utilizado representa únicamente
la relación entre el número de centros y la población, por
lo que no permite medir directamente la calidad, capacidad,
demanda o accesibilidad real de los servicios sanitarios.

Como posible ampliación del análisis, podrían incorporarse
variables como la distancia a los centros, la accesibilidad
mediante transporte público, la población por grupos de edad,
la capacidad de los centros o la demanda sanitaria.

Estas variables permitirían realizar en el futuro un análisis
más completo de la accesibilidad y cobertura del sistema
sanitario de Madrid.