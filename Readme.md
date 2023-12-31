# <h1 align=center> **Análisis del Mercado de Telecomunicaciones Argentino** </h1>

# <h1 align=center>**`Análisis descriptivo, situación actual y propuesta de oportunidades de crecimiento en el sector de internet`**</h1>

# **Autor: Cristian Biava**

## **Propuesta de trabajo**</h2>

La propuesta es estudiar la evolución y el comportamiento de los servicios de telecomunicación a nivel nacional. Particularmente, enfocado en el mercado de internet. 

La finalidad es identificar oportunidades de crecimiento y poder plantear soluciones personalizadas a los posibles usuarios.

La propuesta incluye:

**`Extracción de datos a traves de un API:`**
Los datos se extrajeron en formato .csv desde la pagina oficial de ['ENACOM'](https://datosabiertos.enacom.gob.ar/dashboards/20000/acceso-a-internet/) (Ente Nacional de Comunicaciones), institución encargada de promover la inclusión digital en todo el país.
Para esto se hizo uso de la API de la página.

* Tecnologías y librerías utilizadas: Python, Request, Pandas, os


**`ETL y EDA de los datos originales:`** 
Se realizó un análisis exploratorio de los datos, enfocado en el sector de internet, donde se obtuvieron conclusiones en cuanto a la evolución del número de usuarios y las tecnologías más frecuentes.

Así mismo, se detectaron regiones con oportunidades de crecimiento que podrían ser aprovechadas por empresas proveedoras del servicio.

* Tecnologías y librerías utilizadas: Python, Pandas, Matplotlib

**`Desarrollo de un Dashboard interactivo:`** Se desarrolló un dashboard interactivo cuyo propósito es navegar en las diferentes opciones que presentan los Datasets y evaluar distintos escenarios.

* Tecnologías utilizadas: Power BI, Lenguaje DAX, Inclusión de datos a Power BI a través de Python.


## **Trabajo realizado**</h2>

# **`Extracción de datos`**</h3>

Haciendo uso de la librería requests y de la clave de autenticación provista por la página de ENACOM, se desacargaron 16 archivos .csv relacionados con el sector de internet y 14 datasets con información complementaria de otros sectores.

Los mismos se guardaron en la carpeta Datasets de este proyecto.

Más detalles: ['Extracción de datasets.ipynb'](https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Extracci%C3%B3n%20de%20datasets.ipynb)

# **`ETL y EDA de los datos originales`**</h3>

El análisis del sistema de telecomunicaciones se realizó haciendo foco en el sector de Servicios de Internet, con el objetivo de detectar posibles oportunidades de crecimiento. Haciendo hincapié también, en sus características particulares y la evolución de sus tendencias con la finalidad de plantear soluciones de calidad a los potenciales clientes.

Las preguntas que propone responder este análisis son las siguientes:

1) ¿En qué provicias se pueden encontrar oportunidades de inserción temprana en el mercado?

2) ¿Con qué tipo de servicio sería más conveniente ingresar? ¿Cuál es la tendencia en estos distritos? ¿Cuál es la tendencia en los mercados más avanzados?

3) ¿Qué tecnologías se encuentran en uso en los mercados con oportunidad de crecimiento? ¿Cómo es la situación en las regiones más avanzadas?

4) ¿Cuál es la perspectiva de crecimiento a nivel ingresos en el sector?

A continuación, se mencionan las principales conclusiones.

### **Accesos a internet**

Un análisis en la cantidad de accesos por cada 100 hogares evidencia que un crecimiento en los últimos 8 años que duplicó la cantidad de hogares conectados al servicio (del 35% en 2014 al 70% en 2022).

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Cantidad%20de%20Accesos%20por%20cada%20100%20hogares_Evoluci%C3%B3n%20por%20trimestre.png><p>

Es importante destacar que el 70% de los hogares ya cuenta con conexión a internet. Un porcentaje relativamente alto que haría pensar que ya es tarde para entrar cómo proveedor del servicio.

Sin embargo, analisis más minucioso a nivel provincial revela que hay distritos con una accesibilidad por debajo del 40% (al 3° trimestre del año 2022), lo cual podría suponer una buena oportunidad de incursionar en estos mercados en una etapa relativamente temprana.

Estas provincias son: Santa Cruz, Formosa, Chaco, Santiago Del Estero y Corrientes. Destacar también que, salvo Santa Cruz, el resto son provincias muy cercanas con lo que se podría simplificar la expansión interprovincial del servicio.

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Cantidad%20de%20Accesos%20por%20cada%20100%20hogares_Por%20Provincia.png><p>

Si se considera la evolución en estas provicias a lo largo del tiempo, se puede ver que los hogares con acceso a internet están en plena expansión.

En Chaco y Corrientes aumentó al doble. En el caso de Formosa y Santiago Del Estero, más del 400%.

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Cantidad%20de%20Accesos%20por%20cada%20100%20hogares_Por%20Provincias%20de%20interes.png><p>

### **Calidad del servicio**

A nivel nacional, el estudio sobre los datos de velocidades señala una tendencia hacia velocidades cada vez mayores (+30 Mbps).

En contrapartida, velocidades por debajo de 30 Mbps son cada vez menos aceptadas por el mercado.

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Cantidad%20de%20accesos%20por%20Velocidad_Evoluci%C3%B3n%20por%20trimestre.png><p>

Así mismo, un zoom en las provincias detectadas con potencial de crecimiento, muestra la misma tendencia en Chaco y Corrientes, en donde se observa un salto pronunciado en la cantidad de accesos a velocidades altas durante el año 2019, pasando de menos de 10.000 accesos a más de 50.000 el caso de Corrientes y más de 80.000 para Chaco en 2022 (línea rosa +30Mbps).

Sin embargo, en Formosa y Santiago Del Estero aún no se dio esa explosión y continúan predominando las velocidades bajas (línea verde +1 Mbps - 6 Mbps).

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Cantidad%20de%20accesos%20por%20Velocidad_Chaco.png><p>


<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Cantidad%20de%20accesos%20por%20Velocidad_Corrientes.png><p>


<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Cantidad%20de%20accesos%20por%20Velocidad_Santiago.png><p>


<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Cantidad%20de%20accesos%20por%20Velocidad_Formosa.png><p>


### **Tecnologías**

En línea con lo anterior, el uso de tecnologías de Cable Modem (línea naranja) y Fibra Óptica (línea verde), asociadas a las altas velocidades, va en aumento.

En el caso de la Fibra Óptica se demuestra un aumento significativo de las curva de crecimiento a partir del 2019. Esto guarda relación con lo examinado en el apartado anterior.

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Tecnolog%C3%ADas_Evoluci%C3%B3n%20por%20trimestre.png><p>

El que sigue es un cuadro comparativo de las tecnologías y los rangos de velocidad que proveen, que se agrega a este informe a modo de referencia.

| Tecnología      | Velocidad (Mbps)            |
| --------------- | --------------------------- |
| ADSL            | 2-24 Mbps                   |
| Cablemódem      | 10-1000 Mbps                |
| Fibra óptica    | 100-1000 Mbps (o más)       |
| Wireless        | 1-100 Mbps                  |

Si indagamos la situación en las provincias al 3° trimestre del año 2022, en aquellas con mayor penetración, la alta velocidad es ampliamente dominante (Cable modem, en naranja. Fibra Óptica, en verde).

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Tecnolog%C3%ADas_Por%20Provincias.png><p>

Posando la lupa en las provincias con potencial de crecimiento, se evidencia que el uso de la tecnología ADSL (Líena Azul. Para velocidades inferiores a 24), que predominaba el mercado hasta el año 2019, está sufriendo un gran descenso. Por el contrario, el Cable Modem (línea naranja) y la Fibra Óptica (línea verde) tomaron relevancia desde entonces.

Es de notar, además, que en Formosa la adopción de mejores tecnologías tiene un retraso respecto del resto puesto que el salto importante de estas se da recién en 2022.

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Tecnolog%C3%ADas_Chaco.png><p>

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Tecnolog%C3%ADas_Corrientes.png><p>

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Tecnolog%C3%ADas_Santiago.png><p>

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Tecnolog%C3%ADas_Formosa.png><p>

### **Ingresos**

Es obvio que los ingresos en el sector de internet van en constante y pronunciado aumento, también influenciado por el avance a nivel mundial de tendencias, tecnologías y estilos de vida vinculados con el servicio de internet.

<p align=center><img src=https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Imagenes/Ingresos.png><p>

Más detalles: ['ETL y EDA.ipynb'](https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/ETL%20y%20EDA.ipynb)

# **`Resumen y conclusión`**</h3>

Retomando la propuesta de este análisis:

Se evaluaron 3 indicadores que respondieron a las siguientes preguntas:

### **Penetración de mercado**

¿En qué provincias se pueden encontrar oportunidades de inserción temprana en el mercado?

Las provincias de Corrientes, Formosa, Chaco y Santiago del Estero se presentan como mercados interesantes para una inserción relativamente temprana, puesto que el porcentaje de penetración (menos del 50%) está muy por debajo de la media nacional (70%)

### **Calidad del servicio: Velocidad**

¿Con es la tendencia en cuanto a velocidad en estas provincias? ¿Y en las más avanzadas?

La evolución de la calidad del servicio hacia velocidades cada vez mayores se evidencia, en general, en todas las provincias del país. Se observa una tendencia al uso de velocidades superiores a 30 Mbps.

Sin embargo, en Formosa y Santiago del Estero aún no se dio esa explosión. Hecho que puede ser aprovechado al momento de incursionar en estos mercados.

### **Tecnologías en uso**

¿Qué tecnologías hacen posible la expansión de esas tendencias? ¿Y cómo están evolucionando en las distintas provincias?


En cuanto a las tecnologías utilizadas, la tendencia se correlaciona con las velocidades demandadas por el mercado. El cablemodem y la fibra óptica están desplazando a las tecnologías de menor calidad.

Particularmente, en Formosa la adopción de cablemodem y fibra óptica presenta un delay en el tiempo respecto al resto de las provincias.


### **CONCLUSIÓN:**

Formosa podría ser un buen distrito para aprovechar su potencial de crecimiento, teniendo en cuenta también, la posibilidad de expandir el servicio a provincias limítrofes que, si bien están un poco más avanzadas, aún tienen una penetración de mercado muy por debajo de la media nacional.




# **`Desarrollo de Dashboard interactivo`**</h3>

En línea con este análisis se desarrolló un Dashboard dinámico en Power BI en donde se definieron como KPIs:

1) Penetración de Mercado.

2) Calidad del servicio: velocidad.

3) Tecnologías en uso.

Más detalles: ['Dashboard_Análisis del mercado de telecomunicaciones'](https://github.com/Crichu/Analisis_del_Mercado_de_Internet_en_Argentina/blob/main/Dashboard%20_%20An%C3%A1lisis%20del%20mercado%20de%20telecomunicaciones.pbix)
