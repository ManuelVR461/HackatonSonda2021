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

