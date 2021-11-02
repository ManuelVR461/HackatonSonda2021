## DESAFIO SONDA HACKATHON 2021

# 3OMEGA

INTEGRANTES:
- DANIEL VERDUGO.
- MANUEL RAMIREZ.
- RAFAEL ALVAREZ.

Una entidad financiera es todo negocio que funcione como intermediario en el mercado financiero. El ejemplo más claro de estos son los bancos donde las personas naturales y jurídicas pueden salvaguardar su dinero, realizar compras de acciones, pedir distintos tipos de créditos, etc.

Para este desafío, se deben analizar los datos proporcionados de una entidad financiera para saber el porqué está teniendo una tasa de fuga considerable y que acciones se deben tomar para que dicha tasa se reduzca.

Para la realización del proyecto, se utiliza el proceso KDD (Proceso de Descubrimiento del Conocimiento). Para realizar la selección, procesamiento, muestreo y transformación de datos, en una base de datos a la cual se aplicarán procesos de minería de datos, terminado esto se elegirá el mejor método de predicción y así lograr definir las políticas comerciales que ayuden a resolver el problema.

Como objetivo principal se debe desarrollar un modelo predictivo, con el cual se podrán identificar a los clientes con mayor riesgo de fuga, para así definir nuevas políticas comerciales que permitan retener a dichos clientes.

Para cumplir con lo anterior se realizará lo siguiente:

-	Realizar la detección y corrección de incongruencias o errores en la base de datos.
-	Generar indicadores a partir de los datos para encontrar nuevas variables para optimizar el desempeño predictivo.
-	Crear un análisis descriptivo y gráfico de los datos.
-	Construir modelos predictivos para encontrar la mejor solución al problema.
 
La base de datos en estudio está representada de la siguiente manera:

|Variable|Descripción|Tipo de dato|
|--------|------------------|-------------|
|ID|Identificador del cliente|Entero|
|Genero	|Genero del cliente	|Objeto|
|Renta	|Resta en pesos	|Entero|
|Edad	|Edad en años	|Flotante|
|NIV_Educ	|Nivel educacional	|Objeto|
|E_Civil	|Estado civil	|Objeto|
|COD_Ofi	|Código de oficina	|Entero|
|COD_Com	|Código de la comuna	|Objeto|
|Ciudad	|Ciudad de la oficina	|Objeto|
|D_Marzo	|Deuda de Marzo	|Entero|
|D_Abril	|Deuda de Abril	|Entero|
|D_Mayo	|Deuda de Mayo	|Entero|
|D_Junio	|Deuda de Junio	|Entero|
|D_Julio	|Deuda de Julio	|Entero|
|D_Agosto	|Deuda de Agosto	|Entero|
|D_Setptiembre	|Deuda de Septiembre	|Entero|
|M_Moroso	|Meses en mora	|Entero|
|Monto	|Monto preaprobado	|Entero|
|Seguro	|Seguro de desgravamen	|Objeto|
|Fuga	|Variable objetivo	|Objeto|

La muestra otorgada para la realización de este desafío es de 2294 registros, asociados tanto a clientes actuales como a aquellos que ya se fugaron de la entidad financiera.

### SELECCIÓN, PREPROCESAMIENTO Y TRANSFORMACIÓN DE DATOS

Como primer paso en nuestro proceso realizamos la importación de las librerías y extensiones de Python que nos ayudarán en el manejo de vectores y matrices multidimensionales, y la manipulación, el análisis y la visualización de datos.

![image](https://user-images.githubusercontent.com/40529168/139965447-0aec8ea7-a9cd-42e0-a776-af7475f140e1.png)

Luego exportamos la base de datos de entrenamiento.

![image](https://user-images.githubusercontent.com/40529168/139965481-83011780-81dc-458b-a81d-11c1936a47aa.png)

![image](https://user-images.githubusercontent.com/40529168/139965499-ccab21d5-61e4-4a22-a455-014f500388a3.png)

Eliminamos las variables innecesarias y evaluamos los tipos de variables con las que nos quedaremos.

![image](https://user-images.githubusercontent.com/40529168/139965526-ccbe53d1-d5df-4f1d-ba1f-2ef77983dcce.png)

![h](https://user-images.githubusercontent.com/40529168/139965821-932970b7-be99-4632-8ce1-bcf1afa107fd.png)

Detectamos las columnas categóricas para su posterior tratamiento.

![image](https://user-images.githubusercontent.com/40529168/139965848-7f0cc1f9-9a27-4250-9183-6d9316e12bab.png)

![image](https://user-images.githubusercontent.com/40529168/139965863-949e2464-d1d1-470c-9d30-1802bb6d8018.png)

![image](https://user-images.githubusercontent.com/40529168/139965904-0da229d2-e6a0-4809-af2e-8a7827686400.png)

