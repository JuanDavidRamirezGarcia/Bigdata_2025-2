# Bigdata_2025-2

## Trabajo realizado por Juan David Ramírez García

## Grupo_9: Trabajo individual

## IUDigital de Antioquia

## Evidencia de aprendizaje 1: Creación de una base de datos analítica

Esta evidencia de aprendizaje tiene como objetivo diseñar y construir una base de datos analítica a partir de una fuente de datos consultada en Kaggle.
Para este ejercicio se escogieron datos relacionados con pacientes que han sufrido cáncer de pulmón, como tipo de tratamiento que han recibido, historial médico y demográfico.

**Problemática** : El cáncer de pulmón es la principal causa de muerte por cáncer del mundo, con más diagnósticos y personas fallecidas anualmente. Afecta principalmente a poblaciones vulnerables como los fumadores, exfumadores, diabéticos y personas mayores de 70 años. Asimismo, como familiares de enfermos y los sistemas de salud que tienen una gran carga financiera en la lucha contra la enfermedad. Por lo tanto, el análisis de este problema es vital para encontrar factores y tendencias que puedan ayudar a detectar esta enfermedad en una fase temprana, ya que su detención tardía es la causa fundamental de su mortalidad.

Dataset: Este dataset fue organizado y construido para propósitos educativos y no como una herramienta de predicción de cáncer de pulmón. La idea es poder encontrar patrones y tendencias en los pacientes, y su evolución en los tratamientos aplicados que faciliten un diagnóstico temprano de esta problemática mediante modelos de machine learning y análisis exploratorio de datos.

Este es el link kagle para acceder a más información del data set: https://www.kaggle.com/datasets/khwaishsaxena/lung-cancer-dataset/data

**Variables relevantes encontrada en el dataset**:

* id: Identificador único de cada paciente.
* age: La edad de los pacientes en el momento en que fueron diagnosticados.
* gender: género de los pacientes. Ejemplo male y female.
* country: País donde vive el paciente.
* diagnosis_date: Fecha en la cual el paciente fue diagnosticado con cáncer de pulmón.
* cancer_stage: Fase en la que se encuentra el cáncer al momento del diagnóstico. Ejemplo Stage I, Stage II, Stage III, Stage IV.
* family_history: Indica si hay historia de cáncer en la familia. Ejemplo yes y no.
* smoking_status: Indica si el paciente es fumador.Ejemplo: current smoker, former smoker, never smoked, passive smoker.
* bmi: Índice de masa corporal del paciente cuando fue diagnosticado.
* cholesterol_level: Indica el valor del nivel de colesterol del paciente.
* hypertension: Indica si el paciente tiene hipertensión alta. Ejemplo yes, no.
* asthma: Indicada si el paciente tiene asma.Ejemplo yes, no.
* cirrhosis: Indica si el paciente tiene cirrosis en el hígado.Ejemplo yes, no.
* other_cancer: Indica si el paciente tiene otro tipo de cáncer además del diagnóstico de pulmon. Ejemplo yes, no.
* treatment_type: El tipo de tratamiento que el paciente ha recibido. Ejemplo surgery, chemotherapy, radiation, combined.
* end_treatment_date: La fecha en la que el paciente ha terminado su tratamiento o ha muerto.
* survived: Indica si el paciente sobrevivió. Ejemplo yes, no.

## Estructura y desarrollo de la actividad

* Modelado de datos:
  * En la carpeta docs/ se encuentra el modelo entidad-relación (ER) creado desde dos herramientas diferentes y diseñado para representar las relaciones entre las entidades principales del proyecto (pacientes, diagnósticos, tratamientos, etc.).

*  Creación y carga de la base de datos:
   En la carpeta src/bigdata/ se desarrolló el archivo actividad_1.ipynb, donde se implementaron los scripts SQL para:

    * Crear la base de datos cancer_db.db.
    * Definir las tablas y relaciones según el modelo ER.
    *  Insertar datos de prueba y realizar validaciones iniciales.

* Desarrollo en Databricks:
El archivo Actividad_1_databricks.ipynb contiene el trabajo realizado desde el entorno de Databricks, donde se replicó el mismo trabajo usando Spark, creación de la base de datos analítica y ejecución de consultas.
Este notebook replica y amplía parte del trabajo hecho en el entorno local de GitHub.

## Herramientas utilizadas

* Python (Jupyter / Databricks Notebooks).
* SQLite para la creación de la base de datos.
* Draw.io y dbdiagram.io para el modelado entidad-relación.
* GitHub para la gestión del código y documentación.

## Conclusiones:

* Se creó la base de datos analítica abarcando desde su diseño, generación y modelado de nuevas tablas y el código y buenas prácticas para su implementación.
* Se comprendió la importancia de organizar los datos para lograr una mejor gestión, legibilidad y mantenimiento al crear una base de datos.
Por ejemplo, al dividir una tabla grande en varias tablas relacionadas, se evita la redundancia de información, se mejora la consistencia de los datos y se facilita la realización de consultas analíticas más eficientes.
* El uso de Databricks permitió ejecutar y probar consultas en un entorno de análisis en la nube.
* El uso de GitHub facilitó el trabajo colaborativo, el control de versiones y la trazabilidad de cada fase del proyecto.
  
## Evidencia de aprendizaje 2: procesamiento de datos en una infraestructura cloud

## Antecedentes de la evidencia de aprendizaje 2

Se ha venido trabajando con un conjunto de datos consultado en Kaggle sobre pacientes que padecen cáncer de pulmón y que participan en un tratamiento contra la enfermedad. En la primera actividad se construyó una base de datos analítica usando herramientas como Spark para todo el proceso de carga de datos, creación de tablas y limpieza de la información.

Para esta segunda evidencia de aprendizaje, la idea es replicar el mismo proceso, pero ahora desde la nube utilizando sentencias SQL y empleando Databricks como herramienta principal. Esto incluye la creación del esquema necesario y todos los componentes que permitan ejecutar el flujo completo de procesamiento.

## Objetivo de la actividad

Para esta segunda evidencia de aprendizaje, la idea es replicar el mismo proceso, pero ahora desde la nube utilizando sentencias SQL y empleando Databricks como herramienta principal. Esto incluye la creación del esquema necesario y todos los componentes que permitan ejecutar el flujo completo de procesamiento.

## Estructura y desarrollo de la actividad

El desarrollo de la actividad se realizó en estos paso:

1. Diseño de esquema en el que se almaceno los datos
2. Configuración y documentación del enterno de trabajo en Databricks
3. Creación del ctatalogo, esquemas y tablas con SQL
4. Validación de cosnultas: Metadatos, descripción ,select y Group By
5. Análisis de ventajas y desventajas entre SQL Y SPARK

**Estructura**

* En la carpeta docs/ se encuentra el esquema de almacenamiento de datos esquema.drawio
*  En la carpeta src/bigdata/ se cargo el notebook de la segundo actividad realizado en Databricks Actividad_2.ipynb

## Herramientas utilizadas

* Databricks Notebooks: actividad_2.ipynb
* SQL: para la creación de catálogo, esquemas y tablas
* Draw.io y dbdiagram.io: para realizar el esquema de la arquitecura
* GitHub para la gestión del código y documentación.

## ventajas y desventajas

## Tabla Comparativa

| Propósito | SQL  | Propósito | Spark |
|----------------------------|----------------------|-----------------------------|----------------------------------|
| Facilidad de uso           | SQL es más fácil de usar porque todo es declarativo y directo, y tiene una lógica más sencilla. | Escalabilidad | Noto que Spark tiene una mayor capacidad para trabajar con grandes volúmenes de datos distribuidos. |
| Expresividad declarativa   | Me parece que SQL permite expresar consultas complejas con pocas líneas y la sintaxis es más sencilla. | APIs ricas (DataFrame/RDD)       |  Spark es muy versátil gen cuanto a sus APIs, que permiten transformaciones avanzadas. |
| Integración con BI         | Considero que SQL se integra mucho mejor con herramientas de BI tradicionales. | UDFs y funciones personalizadas  | Siento que Spark facilita mucho más el uso de UDFs en Python para lógica compleja. |
| Limitaciones en pipelines  | En mi experiencia, SQL se queda corto cuando necesito pipelines muy complejos. | MLlib | Veo que Spark es una herramienta fuerte para el trabajo con modelos de ML, en cambio, SQL su fuerte es organizar información de manera lógica. |
| Limitaciones con UDFs      | Percibo que las UDFs en SQL dependen demasiado del motor y pueden ser restrictivas. | Curva de aprendizaje y tuning | creo que la curva de aprendizaje en spark es mucho más inclinada por las múltiples funcionalidades e integraciones que la herramienta posee. |


## Conclusiones:

* A través de la actividad se logró comprender mejor cómo replicar un flujo completo de procesamiento de datos usando únicamente SQL en un entorno en la nube, evidenciando las diferencias y similitudes respecto al proceso realizado previamente con Spark.

* Se pudo validar la importancia de definir un esquema de almacenamiento adecuado en Databricks, ya que esto facilita la organización, consulta y manejo del dataset Lung_cancer dentro de un entorno distribuido.

* Trabajar con SQL en Databricks permite mantener un enfoque declarativo y estructurado, lo cual hace más sencillo interpretar y verificar cada etapa del procesamiento, especialmente en tareas como creación de tablas, limpieza y validación de datos.

* La actividad permitió reforzar los conceptos de arquitectura y las herramientas necesarias para desplegar un flujo analítico en la nube, destacando la importancia de combinar una buena planificación del esquema con la ejecución adecuada de las sentencias SQL.

* Finalmente, al comparar el uso de Spark con SQL durante este ejercicio, pude identificar que Spark ofrece mayor flexibilidad y potencia para procesar grandes volúmenes de datos y construir pipelines complejos , mientras que SQL aporta claridad y simplicidad en la definición del procesamiento. Esta comparación me permitió entender cómo ambas herramientas se complementan y cuándo resulta más conveniente utilizar cada una según las necesidades del análisis.

## Evidencia de aprendizaje 3: proyecto integrador

## Objetivo de la actividad

Poner en práctica las técnicas de limpieza y transformación de datos con herramientas como Spark o SQL en el conjunto de datos que hemos estado trabajando durante todo el curso
En mi caso el data set de pacientes diagnosticados con cáncer de pulmón. Asimismo, visualizar aspectos importantes de nuestros datos con librerías como Matplotlib y Seaborn, además implementar técnicas de buenas prácticas cuando trabajamos con datos en Databricks.

## Nuevos archivos
* Actividad_3_JuanDaRamirez: donde se desarrolló todo el código y puntos del proyecto integrador.
* Video_proyecto_integrador: donde se explicó y se sustentó lo realizado en la actividad.

### Enlace del video: 
https://youtu.be/NHIEr-0LWNY

## Guón de la explicación del video: 

1. **Transformaciones de Fecha :** Del módulo de funciones de Pyspark llamado F se transformó de tipo String a Date las columnas “giagnosis_date” y “end_treatment” de la tabla Historial, usando la instrucción `F.to_date()`. Asimismo, de estas columnas se calcularon nuevas columnas como el año, mes y día de diagnóstico y de fin de tratamiento con las instrucciones: `F.year, F.month y F.day of month`.

2. **Resumen mensual :** Con el módulo de funciones creamos dos tablas para mostrar el resumen de pacientes diagnosticados y que terminaron el tratamiento. Se calcularon nuevas columnas como el número de pacientes diagnosticados y número de pacientes que terminaron el tratamiento mensualmente, usando `F.count`; el promedio de niveles de colesterol con `F.avg` y número de pacientes en estadio IV de cáncer a la hora del diagnóstico y al terminar el tratamiento.

3. **Limpieza antes y después :** De la tabla pacientes y usando el módulo de funciones se hizo limpieza de datos como borrar espacios al inicio y al final, y convertir letras mayúsculas a minúsculas de la columna smoking_status con instrucciones `F.lower` y `F.trim`. Asimismo, de datos nulos y negativos de la variable Edad con condicionales e instrucciones como: 
`(F.col("age").isNull()) | (F.col("age") < 0)`.


**Visualizaciónes**
 
4. Se usó la librería **Matplotlib** para visualizar cómo se distribuyen los tipos de fumadores en el año de su diagnóstico a través de un gráfico de barras usando la instrucción .plot(kind=bar,…)

5.	Se usó la librería **Seaborn** para visualizar el estado del paciente al finalizar el tratamiento con el método `sns.barplot()`.

  
