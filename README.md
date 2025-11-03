# Bigdata_2025-2

## Evidencia de aprendizaje 1: Creación de una base de datos analítica

Esta evidencia de aprendizaje tiene como objetivo diseñar y construir una base de datos analítica a partir de una fuente de datos consultada en Kaggle.
Para este ejercicio se escogieron datos relacionados con pacientes que han sufrido cáncer de pulmón, como tipo de tratamiento que han recibido, historial médico y demográfico.

**Problemática** : El cáncer de pulmón es la principal causa de muerte por cáncer del mundo, con más diagnósticos y personas fallecidas anualmente. Afecta principalmente a poblaciones vulnerables como los fumadores, ex fumadores, diabéticos y personas mayores de 70 años. Asimismo, como familiares de enfermos y los sistemas de salud que tienen una gran carga financiera en la lucha contra la enfermedad. Por lo tanto, el análisis de este problema es vital para encontrar factores y tendencias que puedan ayudar a detectar esta enfermedad en una fase temprana, ya que su detención tardía es la causa fundamental de su mortalidad.

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
  


