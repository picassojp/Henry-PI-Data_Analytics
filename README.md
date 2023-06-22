<p align=center><img src=https://www.abatic.es/wp-content/uploads/2018/02/MOOC.png width="500px"><p>

# <h1 align=center>**`Proyecto Individual: Análisis de Datos de Plataformas MOOC`**</h1>


Este repositorio es un proyecto individual cuyo objetivo es la generación de indicadores claves de rendimiento (KPI, por sus siglas en inglés) para el negocio de cursos de tipo MOOC. Inicialmente, se procesaron los datos de plataformas reconocidas que ofrecen este tipo de cursos para luego desarrollar un análisis exploratorio con la intención de descubrir información de utilidad. Posteriormente, se diseño un _dashboard_ para presentar la métricas necesarias para el seguimiento de los KPIs propuestos. El preprocesamiento y análisis se desarrollo con librerías de lenguaje Python. El tablero se generó mediante el programa _Power BI_. Este proyecto fue desarrollado durante la etapa de Labs del _bootcamp_ de Henry. A continuación, se describen cada una de las etapas en las que se organizó el proyecto.

**`Fuentes de datos`**

Los conjuntos de datos se encuentran disponibles en esta carpeta de [Google Drive](https://drive.google.com/drive/folders/1dx1scrL8qucZNLqYr2nHYN5e5F3RoBUx?usp=drive_link), separados en originales (sin transformaciones) y los resultantes del preprocesamiento.

**`Preprocesamiento`**

Se realizaron algunas transformaciones a los datasets originales tales como:

+ Se eliminaron las filas integralmente duplicadas en todos los datasets.

+ Se mapearon las variables correspondientes a idioma y grupo temático de cada curso para reemplazarlas por su traducción al español.

+ Los formatos de variables como número de inscriptos, precio del curso y fecha de lanzamiento se modificaron. 

+ Se separaron los datos de la columna de instructores para facilitar el agrupamiento.

+ Los datasets de la plataforma **`Coursera`** fueron combinados a partir del campo **`course_id`** para contar con la cantidad de reseñas como estimador de la cantidad de inscriptos en cada curso. También se combinaron los datasets de la plataforma **`Udemy`** para contar con los instructores de cada curso; la combinación también se realizó en base al campo **`course_id`**.

Estas tareas se realizaron en una [Jupyter Notebook](https://github.com/picassojp/Henry-PI-Data_Analytics/blob/54a9704eaaa2731f737748d842f21e95fc463582/Henry_PI_DA.ipynb) en el entorno de Google Colab. Se utilizaron librerías como Pandas, Numpy, Seaborn, Matplotlib.pyplot y Scikit-learn.

**`Análisis exploratorio de los datos`**: _(Exploratory Data Analysis-EDA)_

Para cada plataforma se realizó un análisis individual ya que diferían en las variables disponibles. Como primera aproximación a los datos se realizó un resumen estadístico con medidas de tendencia central. Se analizaron las distribuciones de variables relevantes para el desarrollo de los KPIs como **`idioma`**, **`precio`**, **`nivel del curso`** y **`rating`** respecto al nivel de venta, el cual se estimó con las variables relativas a cantidad de inscriptos por curso. También se analizaron variables como **`fecha de lanzamiento`**, **`instructor`** e **`institución`**. A fin de detectar variables importantes para la predicción del número de inscriptos, se desarrollo un modelo de _Random Forest_ y se presentaron las variables más importantes para el modelo. También se analizaron las nubes de palabras de los campos **`título`** , **`resumen`** y **`descripción`**.
Los hallazgos de este análisis se utilizaron para el posterior desarrollo del _dashboard_ y KPIs asociados.


Este EDA se puede consultar en la sección 3 de la [Jupyter Notebook](https://github.com/picassojp/Henry-PI-Data_Analytics/blob/54a9704eaaa2731f737748d842f21e95fc463582/Henry_PI_DA.ipynb). Se utilizaron librerías como Pandas, Numpy, Seaborn, Matplotlib.pyplot y Wordcloud.

**`Dashboard`**

Los KPIs diseñados y el seguimiento de las métricas asociadas se realizó mediante el _software_ dedicado a _Business Intelligence_ de Microsoft, _Power BI_. La facilidad para realizar análisis complejos y crear visualizaciones interactivas junto con la interfaz de usuario cómoda para la creación de reportes atractivos lo vuelve un software muy conveniente para esta etapa del proyecto.

El _dashboard_ se encuentra disponible como archivo de [_Power BI_](https://github.com/picassojp/Henry-PI-Data_Analytics/blob/54a9704eaaa2731f737748d842f21e95fc463582/dash_board.pbix).

**`Mantenimiento`**
Este proyecto es mantenido por Juan Pablo Picasso. Si tienes alguna pregunta o encuentras algún problema, por favor, [contactame](https://www.linkedin.com/in/picassojp).