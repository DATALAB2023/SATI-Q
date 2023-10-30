![LOGO DATATHON BA 2023 ICO](https://github.com/DATALAB2023/SATI-Q/assets/148904526/6fee3fe3-f7a3-469f-99a0-766d3895b986)

# ![LOGO CUADRADO SATIQ ICO](https://github.com/DATALAB2023/SATI-Q/assets/148904526/d67eeb09-d63c-40d3-87d2-71c903c134c1) DESAFIO DATATHON: SATI-Q 
*SATI-Q 20 AÑOS: Analicemos juntos 2 décadas de datos de cuidados intensivos en Argentina*

## DESCRIPCIÓN:📊
En este desafío, exploraremos el potencial de la Ciencia de Datos y la Inteligencia Artificial como herramientas para identificar el perfil epidemiológico y detectar oportunidades de mejora en la calidad de atención de pacientes, adultos y pediátricos, internados en Unidades de Cuidado Intensivo en Argentina.
 
## OBJETIVO DEL DESAFÍO:🏆
El principal objetivo es reconocer el valor de la información generada durante los procesos de atención de los pacientes en Cuidados Intensivos y la importancia del análisis de registros de datos estandarizados y multicéntricos para generar conocimiento. Para lograrlo, se espera que los participantes puedan responder a una pregunta de investigación relevante. Como ejemplos de puntos de partida, pero no limitantes, compartimos las siguientes preguntas Inspiradoras:

+ ¿Cuál es la evolución de los pacientes  adolescentes / adultos jóvenes en UCI o UCIP? (Menores de 20 años en UCI vs. Mayores de 14 años en UCIP)
+ ¿Cómo son los pacientes que requieren Cuidados Intermedios o tercer nivel post UCI o UCIP?  
+ ¿Es el reingreso a la UCI- UCIP un factor pronóstico de mala evolución? ¿ Cuáles son sus factores de riesgo?
+ ¿El género es un factor que afecta los resultados en UCIP / UCI?
+ ¿Por Qué una mujer joven requiere Cuidados Intensivos? ¿Son distintas las causas de ingresos a las de los hombres?
+ Uso de dispositivos en UCI y UCIP: ¿Existen diferencias entre  el grado de invasión de niños y adultos críticamente enfermos?
+ Mortalidad en pacientes de bajo riesgo en UCI / UCIP : perfil epidemiológico, factores de riesgo , predicción
+ Tiempo entre ingreso al hospital e ingreso a Cuidados Intensivos : ¿influye en la mortalidad en UCI- UCIP?
+ Guardia vs Sala : ¿la procedencia afecta la evolución de los pacientes en UCI / UCIP?
+ ¿Podemos predecir la infección asociada a dispositivos en el paciente crítico?

## CONTEXTO:📚
El Programa de Calidad SATI- Q es una **red multicéntrica de registro prospectivo y permanente de indicadores de calidad (Quality Benchmarking) en Unidades de Cuidados Intensivos de Argentina**, llevado adelante por la Sociedad Argentina de Terapia Intensiva (SATI). Las Unidades participan enviando voluntariamente sus registros en forma anónima y estandarizada. También disponen de un soporte informático de distribución libre, el Software SATI-Q, que permite el uso integrado a la práctica asistencial y la generación de informes personalizables. 
> Para mas información: https://www.satiq.net.ar/
  
Los datos que forman parte de este desafío son una muestra anonimizada y curada de la base de pacientes adultos y pediátricos de SATI-Q

## PRERREQUISITOS: :hammer_and_wrench:
Todos los miembros del equipo deben haber firmado [el acuerdo de confidencialidad y uso de datos:](https://forms.gle/GqhdWrTAu9a9hVhi7)
  
Para el análisis de los datos se recomienda utilizar alguna de las siguientes plataformas:
+ R-STUDIO:  https://posit.co/download/rstudio-desktop/
+ Visual Code: https://code.visualstudio.com/
+ Google Collab: https://colab.research.google.com/?hl=es

## PRESENTACIÓN DE RESULTADOS:
	**REVISAR ESTA SECCION**
Generar una presentación de no mas de 5 diapositivas, 5 minutos.
INTRODUCCION, PREGUNTA, RESULTADOS
Compartir códigos fuentes utilizados

## ESTRUCTURA DE DATOS
La base de datos SATI-Q (adultos y pediátrica) está compuesta de 2 tipos de tablas: 
+ 1-tablas que contienen datos de los episodios de internaciones
+ 2-tablas que contienen códigos internos
Las distintas tablas con datos están relacionadas por **3 campos claves: TIPODNI, DNI, FECING.**
Estos campos identifican unívocamente al paciente y su internación en todo el sistema.

## REPOSITORIO DE DATOS
A los fines de este desafío se ponen a disposición las tablas que contienen datos en formato CSV (texto separado por comas). Aquellas que contienen códigos internos, además del formato CSV, se pueden consultar en los respectivos diccionarios de datos.

> [REPOSITORIO DE DATOS:](https://drive.google.com/drive/folders/1fTmRTHRpsRGUnIxlkTB1AN3tbH9kLnMQ?usp=drive_link)

Dentro de este *REPOSITORIO*, se disponen de dos carpetas que incluyen las tablas para utilizar en este Desafío: **SATIQ-ADULTOS y SATIQ-PEDIATRICOS**. Allí mismo también encontrará el diccionario de datos, dentro de su respectiva carpeta.

### ÍNDICE RÁPIDO DE TABLAS EN SATI-Q

A continuación presentamos la descripción de cada tabla / archivo CSV del *DESAFIO SATI-Q*, incluyendo los códigos internos relacionados. Estos códigos internos se presentan en tambien en su respectiva carpeta y además están referenciados dentro del diccionario de datos.

| Tablas de Datos  | Descripción | Códigos internos |
| ------------- | ------------- | :-------------: |
| **FIVARAPA**  | Tabla principal para todos los pacientes (adultos y pediátricos). Contiene un resúmen de la evolución del paciente, datos demográficos, procedencia, uso de dispositivos, estadía y resultados. Cada fila / registro representa a una única internación. Además almacena el Puntaje APACHE II en los pacientes adultos. | *FIVARAPA_PATOLOGIA (SOLO ADULTOS), FIVARAPA_CATKNAUS (SOLO ADULTOS), FIVARAPA_COMORBIL (SOLO ADULTOS), FIVARAPA_TIPO, FIVARAPA_PROCEDENCIA, FIVARAPA_RESTRAT*|
| **FIMOTINGP**  | Contiene la categoría diagnóstica presentada al ingreso de la UCI. Se permite una sola categoría por ingreso |  |
| **FIMOTINGD**  | Contiene todos los diagnósticos presentes al ingreso de la UCIP. Se puede registrar uno o más por internación. Contiene el Diagnostico Principal (un registro por episodio), los Antecedentes (pueden haber varios registros por episodio) y Otros Diagnosticos al Ingreso (tambien pueden haber varios registros por episodio). | **(SOLO PEDIÁTRICOS)** |
| **FIMOTINGD_PRINCIPAL**  | Contiene todos los diagnósticos *PRINCIPALES* presentes al ingreso de la UCIP. Un registro por episodio. | **(SOLO ADULTOS)** |
| **FIMOTINGD_DIAGNOSTICO)**  | Contiene todos los diagnósticos *SECUNDARIOS* presentes al ingreso de la UCIP. Pueden haber varios registros por episodio. | **(SOLO ADULTOS)** |
| **FIMOTINGD_ANTECEDENTES)**  | Contiene todos los *ANTECEDENTES* presentes al ingreso de la UCIP. Pueden haber varios registros por episodio | **(SOLO ADULTOS)** |
| **FIPRACTICAFOLEY**  | Contiene datos referentes a las sondas vesicales que el paciente tuvo colocadas durante su internación en la UCI. Puede registrarse más de un episodio de sondaje vesical por paciente |  |
| **FIPRACTICAARM**  | Contiene datos referentes a los episodios de ventilación mecánica o apoyo respiratorio que recibió el paciente en la UCI. Incluye ventilación mecánica invasiva, no invasiva y CAFO. Se registra una fila por cada episodio de ventilación mecánica. | *ARM_COMPL, ARM_MOTIVO, ARM_UTIL* |
| **FIPROC**  | Contiene los procedimientos que se realizaron al paciente durante su internación en la UCIP. Puede registrarse más de un procedimiento por paciente, lo cual generará varias filas para el mismo registro de internación. | Content Cell |
| **FIMOTINGP**  | Motivos de Ingreso (tanto adultos como pediátricos)  | Content Cell |
| **FIMOTINGP**  | Motivos de Ingreso (tanto adultos como pediátricos)  | Content Cell |
| **FIMOTINGP**  | Motivos de Ingreso (tanto adultos como pediátricos)  | Content Cell |
| **FIMOTINGP**  | Motivos de Ingreso (tanto adultos como pediátricos)  | Content Cell |
| **FIMOTINGP**  | Motivos de Ingreso (tanto adultos como pediátricos)  | Content Cell |
| **FIMOTINGP**  | Motivos de Ingreso (tanto adultos como pediátricos)  | Content Cell |




