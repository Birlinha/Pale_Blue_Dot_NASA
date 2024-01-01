# NASA | DrivenData.org
## El Pálido Punto Azul - *Pale Blue Dot*

Este desafío propuesto por DrivenData, en conjunto con la NASA y NASA Tournament Labs - *NTL*
Es un desafío cuyo objetivo apunta a alcanzar los Objetivos de Desarrollo Sostenible - *ODS*
Los objetivos en foco son: Hambre Cero, Agua Limpia y Saneamiento, y Cambio Climático

Como analista de datos, científico o científico ciudadano, debes crear visuales intrigantes que ayuden a los formuladores de políticas - *policymakers* a tomar decisiones.

Atención: Es necesario utilizar datos públicos sobre Estados Unidos en tu estudio. Verifica los conjuntos de datos disponibles en su totalidad en: [Pale Blue Dot](https://www.drivendata.org/competitions/256/pale-blue-dot/)

## Cómo hacer un proyecto como este (*pero diferente*)

Para construir tu proyecto, debes prestar atención a los siguientes 3 puntos (no necesariamente en orden, y puede ser cíclico):

- Lluvia de ideas
  - Comprensión del problema
  - Construcción de posibles soluciones
  - Vinculación entre datos disponibles y problemas por resolver
- Datos
  - Descarga de datos
  - Comprensión de los datos
  - Transformación de los datos
- Visualización / Resolución del problema
  - Construcción de gráficos
  - Validación de los datos y del gráfico construido
  - Pregunta: ¿Este gráfico resuelve el problema propuesto en la fase de Lluvia de ideas/Datos? Si no, regresar a donde sea necesario

En este caso, vamos a saltar la fase de lluvia de ideas para entrenarnos en un caso específico:
  Precipitación sobre hielo en Alaska

Al preguntarle a ChatGPT cuáles podrían ser los casos de uso para un conjunto de datos destinado a comprender el índice de precipitación sobre hielo en Alaska, respondió:

> Este conjunto de datos sobre la frecuencia y distribución de lluvia sobre la nieve durante las estaciones frías en Alaska entre 2003 y 2016 tiene varias aplicaciones interesantes. Aquí hay algunos casos de uso potenciales:
> 
> Predicción de Riesgo de Inundaciones: Utiliza patrones de lluvia sobre la nieve para prever el riesgo de inundaciones durante el derretimiento de la nieve en primavera. Esto podría ser crucial para comunidades y autoridades locales que deseen prepararse para eventos de inundación.
> 
> Impacto en la Vida Silvestre: Analiza cómo la lluvia sobre la nieve afecta la ecología y el comportamiento de la vida silvestre en Alaska. Esto puede ayudar a biólogos y conservacionistas a entender mejor cómo el cambio climático está influyendo en las poblaciones animales en la región.
> 
> Agricultura y Recursos Hídricos: Estudia cómo la lluvia sobre la nieve afecta los niveles de agua disponibles para la agricultura y otras actividades humanas. Esto podría ser crucial para la planificación de recursos hídricos y la gestión agrícola en la región.
> 
> Modelado de Cambio Climático: Utiliza estos datos para validar y mejorar modelos climáticos que intentan predecir cambios futuros en el patrón de lluvia sobre la nieve. Esto puede ayudar a entender mejor los cambios climáticos globales y sus impactos regionales.
> 
> Planificación de Infraestructura: Comprende cómo la lluvia sobre la nieve afecta la infraestructura, como carreteras, edificios y redes de energía, para planificar mejor la construcción y el mantenimiento en regiones afectadas.
> 
> La razón por la que estos casos de uso son relevantes es que la lluvia sobre la nieve puede tener efectos significativos en varios aspectos de la vida y operaciones humanas en Alaska. Comprender estos patrones puede ser fundamental para la adaptación al cambio climático y la mitigación de los riesgos asociados.

Por lo tanto, vamos a utilizar la lluvia de ideas realizada por nuestro compañero y estudiar al menos uno de estos temas.

En la fase de datos, necesitamos descargar los datos relevantes para nuestro análisis.

En este caso, al hacer clic aquí, podemos ver los [datos sobre precipitación en Alaska de 2003 a 2016](https://search.earthdata.nasa.gov/search/granules?portal=idn&p=C2162145449-ORNL_CLOUD&pg%5B0%5D%5Bv%5D=f&pg%5B0%5D%5Bgsk%5D=-start_date&fi=MODIS&as%5Bscience_keywords%5D%5B0%5D=Atmosphere%3APrecipitation&tl=1703557365.73%213%21%21&fst0=Atmosphere&fsm0=Precipitation)

Recuerda, es necesario registrarse en el sistema del sitio web antes de tener acceso para ver la información y descargarla.
Una vez que hayas registrado tu cuenta, descargar un archivo es tan simple como encontrarlo y hacer clic en un botón "descargar" o "descargar todo" -> y recibirás una lista de URL para hacer clic y descargar, una por una.

Suponiendo que has descargado el archivo, el último paso necesario sería abrir el archivo ["ALASKA_rain_on_snow.ipynb"](https://github.com/Birlinha/Pale_Blue_Dot_NASA/blob/main/ALASKA_rain_on_snow.ipynb) y hacer clic en el botón en la parte superior "Abrir en Colab"

Dentro del Notebook, que es el nombre dado a este intérprete de código, necesitarás abrir la pestaña a la izquierda, donde hay un ícono de una carpeta.

Dentro de esa carpeta, haz clic en cargar y sube el archivo de imagen .tif descargado del conjunto de datos de precipitación de Alaska.

Después de eso, simplemente copia el nombre del archivo e introdúcelo en el código, reemplazando el nombre ABoVE.Rain-On-Snow.2003_Water_Year_Ah000-001v000-001.001.10212018 (1).tif con el nombre de tu archivo.

Al ejecutar todo el cuaderno, pedirá tu permiso para acceder a Google Drive y almacenar el archivo allí, dentro de una carpeta llamada rain_on_snow_NA
