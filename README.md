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

![image](https://user-images.githubusercontent.com/40529168/139966002-cfb04c9c-aca0-4a26-af8d-bf04e7494bcc.png)

![image](https://user-images.githubusercontent.com/40529168/139966020-be222f6b-24d8-4dc3-a52c-1ef774a80ed3.png)

![image](https://user-images.githubusercontent.com/40529168/139966027-2fc98306-a20d-4765-ac32-9c062239e74a.png)

![image](https://user-images.githubusercontent.com/40529168/139966035-f7958e61-d893-4a6c-afea-ac702aea3f80.png)

![image](https://user-images.githubusercontent.com/40529168/139966128-d7adc06a-5d06-4a8b-a0dd-32a994799ebd.png)

![image](https://user-images.githubusercontent.com/40529168/139966153-961bdaaa-8a3d-45b6-b728-f575b62276fc.png)

![image](https://user-images.githubusercontent.com/40529168/139966166-aa186ff7-dc13-4f02-9b2f-903b8ca5c7c0.png)

![image](https://user-images.githubusercontent.com/40529168/139966186-f2f622c4-be4c-4c29-9399-ee1bd44e0e92.png)

![image](https://user-images.githubusercontent.com/40529168/139966200-d76ca2da-a8bb-4859-abf1-d3ef236047f1.png)

![image](https://user-images.githubusercontent.com/40529168/139966238-ed390cd2-f685-4684-b128-05e732019942.png)

Como se aprecia en el gráfico de torta, los datos indican que está balanceado, ya que no se visualiza una inclinación a alguna de las alternativas, con una proporción muy similar entre Fugados y No Fugados lo que nos permitirá entrenar el modelo de manera eficaz.

![image](https://user-images.githubusercontent.com/40529168/139966295-e3563ecc-543f-4229-b747-34dd8fe8f930.png)

![image](https://user-images.githubusercontent.com/40529168/139966339-978d8a5d-68d4-45a6-b8f9-64d22dc940bf.png)

![image](https://user-images.githubusercontent.com/40529168/139966354-82b9cf8f-5f2f-485a-b96b-b0d0688c137f.png)

Buscamos inconsistencias para la variable Edad.

![image](https://user-images.githubusercontent.com/40529168/139966393-bfacd1a6-c010-46a5-bce7-a5ca15b78e55.png)

![image](https://user-images.githubusercontent.com/40529168/139966408-06f80e79-337c-4af0-9075-3f645c2351db.png)

Dados los resultados anteriores, se encontraron registros que podrían tener algún error de transcripción en la edad, por lo que procedemos a calcular la moda de la variable y actualizar dichos registros con el resultado obtenido.

![image](https://user-images.githubusercontent.com/40529168/139966443-d4717ff2-4c73-4105-afbe-02f7c00736a7.png)

![image](https://user-images.githubusercontent.com/40529168/139966457-e77e74ae-1aa8-441f-9711-c2277119fbdb.png)

A continuación se realiza el análisis de las variables con el test de Kolmogorov-Smirnof de manera de revisar la distribución de las variables.

![image](https://user-images.githubusercontent.com/40529168/139966473-47639e7a-840a-4eaf-b017-908691ba8b64.png)

![image](https://user-images.githubusercontent.com/40529168/139966899-4da83bdb-ce8e-4f16-b7f9-a356deffbd6d.png)

![image](https://user-images.githubusercontent.com/40529168/139966943-e86b6433-5644-40e2-81cb-3156a576fbd3.png)

![image](https://user-images.githubusercontent.com/40529168/139967018-38dbdd1f-d37f-4ae0-ba5d-4daa42f8c704.png)

![image](https://user-images.githubusercontent.com/40529168/139967195-2194cae1-6b8e-4caf-b0bc-3e70f6fa7443.png)

![image](https://user-images.githubusercontent.com/40529168/139967122-0a9c5940-e1f6-4bb6-880c-125b575b9121.png)

![image](https://user-images.githubusercontent.com/40529168/139967386-d015e51b-86ae-48e4-9781-7313f8c9f603.png)

![image](https://user-images.githubusercontent.com/40529168/139967401-430e02e1-ffdf-49d1-a6f9-e03db0dabfd2.png)

![image](https://user-images.githubusercontent.com/40529168/139967453-9136f447-edac-4b55-8fea-b23025a08cb8.png)

![image](https://user-images.githubusercontent.com/40529168/139967463-422d48d0-6173-4797-b03a-fa64852af5b4.png)

![image](https://user-images.githubusercontent.com/40529168/139968987-5883472d-5e8f-4cac-af6e-be40c5860d7b.png)

La base de datos sin las columnas descartadas se puede ver a continuación:

![image](https://user-images.githubusercontent.com/40529168/139969041-8f81f2b5-e1b5-45bd-9296-bf3dfcbb02e3.png)

![image](https://user-images.githubusercontent.com/40529168/139969090-e92f7676-1838-4e45-ac57-4dd3919cc453.png)

Dentro de las variables categóricas, existen tres de ellas a las cuales se aplicará un tratamiento especial para agrupar la cantidad existente y así minimizar los sesgos por dispersión que pudieran existir; estás variables son CIUDAD, COD_COM y COD_OFIC.

![image](https://user-images.githubusercontent.com/40529168/139969123-909ec503-67d0-46c4-b608-f28f116adc73.png)

![image](https://user-images.githubusercontent.com/40529168/139969145-1e199eb2-17f5-4fed-9837-b4744e143f7b.png)

![image](https://user-images.githubusercontent.com/40529168/139969181-ffb77746-9dce-49b8-a797-db596680966d.png)

![image](https://user-images.githubusercontent.com/40529168/139969206-8e546528-a726-470d-b41c-60bf9ad75132.png)

![image](https://user-images.githubusercontent.com/40529168/139969223-6818975f-39e6-4632-adc2-30426d2cfebf.png)

![image](https://user-images.githubusercontent.com/40529168/139969241-517e70eb-10a2-42e1-b56d-df0e3e14fe57.png)

![image](https://user-images.githubusercontent.com/40529168/139969256-d7f433e5-d12f-40c3-9e14-294db1b32e78.png)

![image](https://user-images.githubusercontent.com/40529168/139969321-fdcb2ccb-54ab-4546-9b50-121f79ab6a4d.png)

![image](https://user-images.githubusercontent.com/40529168/139969350-84733846-ad73-4645-baa1-aa110ff5b129.png)

![image](https://user-images.githubusercontent.com/40529168/139969384-19e724a6-b060-4d29-be5e-b4a6cda88af1.png)

![image](https://user-images.githubusercontent.com/40529168/139969412-f2ee7d32-a78e-4346-a49c-77d5609f9438.png)

![image](https://user-images.githubusercontent.com/40529168/139969449-66074329-bf00-45cc-9f81-4b8581685606.png)

Al revisar los gráficos, nuestras primeras impresiones sobre los clientes que tienden a fugarse:
-	Poseen estudios universitarios.
-	Son casados.
-	Son hombres.
-	No tienen seguro de desgravamen.

En cambio, los más fieles (no se fugan):
-	Poseen estudios técnicos.
-	Son solteros o viudos.
-	Son mujeres.

![image](https://user-images.githubusercontent.com/40529168/139969484-90cfa59b-f77d-4eba-a5a3-a23dc9bae1f7.png)

![image](https://user-images.githubusercontent.com/40529168/139969503-f81407f0-51c4-4013-a6c8-4e9fe15308ae.png)

Al realizar la impresión de un gráfico de dispersión, la librería (Pandas) gráfica primero los datos de los clientes Fugados (rojo) para luego sobreponer los datos de los clientes No Fugados (verde), por tanto, para entender mejor la idea se disponen ambos gráficos donde el segundo muestra la impresión invertida.

![image](https://user-images.githubusercontent.com/40529168/139969578-00130538-ea70-4ad4-b8e3-0536d18c1783.png)

![image](https://user-images.githubusercontent.com/40529168/139969648-bcfd669e-5e60-4bb4-a74a-67de5f85cfc1.png)

Según el mapa de correlación de la base de datos, todas las variables se pueden considerar para el entrenamiento, ya que ninguna explica otra.

Luego de culminada la limpieza de los datos, procedemos a realizar el escalamiento de estos para normalizarlos en una distribución entre cero (0) y uno (1).

![image](https://user-images.githubusercontent.com/40529168/139969685-2db718e5-70de-432c-b6a5-d757b5bf8517.png)

![image](https://user-images.githubusercontent.com/40529168/139969727-671d80cb-4a7b-4b4e-a662-2a81f6d16ea3.png)


## MINERÍA DE DATOS

Comenzamos realizando el proceso de entrenamiento donde tomaremos 80% de los registros y los dividimos en una validación cruzada de 4 partes, mientras el 20% restante lo tomamos para el test final del entrenamiento.

![image](https://user-images.githubusercontent.com/40529168/139969752-6df37f03-35e7-4324-aaeb-1f4025c99987.png)

![image](https://user-images.githubusercontent.com/40529168/139969806-307f13dd-1121-4909-8967-717ab7f2a4d5.png)

Para el siguiente paso hemos seleccionado los modelos de machine learning que vamos a aplicar:

-	K vecinos más cercanos (KNN)
-	Árbol de decisión (TREE)
-	Regresión logística (LOG)
-	Máquina de vectores de soporte (SVC)
-	Gaussian Naive Bayes (NBC)
-	Gradiente descenso estocástico (SGD)
-	Clasificador Ramdom Forest (RF)
-	Red neuronal (RNN)

# ***K Vecinos más cercanos (KNN)***

![image](https://user-images.githubusercontent.com/40529168/139969865-b299b84b-5013-4b99-aaf1-a684b981ba94.png)

![image](https://user-images.githubusercontent.com/40529168/139969893-4e7dedc3-2821-4a32-a15a-fd44241d20b8.png)


# ***Árbol de decisión (TREE)***

![image](https://user-images.githubusercontent.com/40529168/139969932-8c125f05-761f-4da6-97ad-32f5e2df92ba.png)

![image](https://user-images.githubusercontent.com/40529168/139969965-f11767be-9dc8-4eaf-8366-3f5f27b8f7ee.png)


# ***Regresión logística (LOG)***

![image](https://user-images.githubusercontent.com/40529168/139970004-0ca71f06-359b-42f5-b788-134c728445f6.png)

![image](https://user-images.githubusercontent.com/40529168/139970034-d51941ce-a536-41b5-9206-d6c72b5b0cf1.png)


# ***Máquina de vectores de soporte (SVC)***

![image](https://user-images.githubusercontent.com/40529168/139970071-f8af05d4-4430-4531-bcbf-9a26138c3a23.png)

![image](https://user-images.githubusercontent.com/40529168/139970088-88e0edd8-8893-4f4d-b021-96e483f91229.png)


# ***Gaussian Naive Bayes (NBC)***

![image](https://user-images.githubusercontent.com/40529168/139970110-8bc0212d-550a-4208-a05c-a793f66adda7.png)

![image](https://user-images.githubusercontent.com/40529168/139970127-b8835671-d0d9-45d8-866c-c33fc99bbd80.png)


# ***Gradiente descenso estocástico (SGD)***

![image](https://user-images.githubusercontent.com/40529168/139970161-a086b620-1bd9-482e-99fa-89b3f4b7f948.png)

![image](https://user-images.githubusercontent.com/40529168/139970185-96660889-9093-435d-900d-d7e040a1c08c.png)


# ***Clasificador Ramdom Forest (RF)***

![image](https://user-images.githubusercontent.com/40529168/139970205-8d3fdd67-cbd3-4192-b4dd-6f9b8ed4cf65.png)

![image](https://user-images.githubusercontent.com/40529168/139970235-79815b8a-3c04-42fb-8ebc-3b15e8145ad0.png)


# ***Red neuronal (RNN)***

![image](https://user-images.githubusercontent.com/40529168/139970264-080dda29-d500-4e41-ac36-214aa199fa72.png)

![image](https://user-images.githubusercontent.com/40529168/139970298-afc70c0a-fdde-47ad-b2d5-9083f836dab9.png)

![image](https://user-images.githubusercontent.com/40529168/139970313-00db8f48-de8d-4f13-999a-3370702b9353.png)

![image](https://user-images.githubusercontent.com/40529168/139970334-3f89e912-556c-45cd-9547-975641d73290.png)

![image](https://user-images.githubusercontent.com/40529168/139970347-0590843c-a751-4f16-8277-ea2f8c0c222a.png)


Luego de analizar los distintos métodos, verificamos la curva ROC:

![image](https://user-images.githubusercontent.com/40529168/139970377-8f55fc64-0153-4d6c-8d6c-971c00afd6d6.png)

![image](https://user-images.githubusercontent.com/40529168/139970398-c5d0fadc-25f3-47f0-bd4f-2b5a182001d4.png)

![image](https://user-images.githubusercontent.com/40529168/139970425-a9b47474-2f32-4b87-9032-a1aed97ac5d6.png)

![image](https://user-images.githubusercontent.com/40529168/139970451-1d1e392d-4510-43de-a7d7-d7c584282374.png)



## INTERPRETACIÓN Y EVALUACIÓN

Luego de haber seleccionado un modelo con los datos de entrenamiento, se realizan los mismos pasos de limpieza y escalamiento para los datos de evaluación hasta tener el mismo esquema de datainput necesaria para los modelos.

![image](https://user-images.githubusercontent.com/40529168/139970482-2b1f506c-2d13-4a25-a072-570a3a3c686b.png)

![image](https://user-images.githubusercontent.com/40529168/139970501-52ed2daf-4dde-4abb-a2db-b046b202ab6b.png)

![image](https://user-images.githubusercontent.com/40529168/139970513-4c00fa50-4901-4c51-ab62-9a9431d64530.png)

![image](https://user-images.githubusercontent.com/40529168/139970530-d56a5f5b-4313-4e76-b785-27aa1391d230.png)


Se realiza el mismo proceso de limpieza y conversión de variables que se utilizó para el entrenamiento.

El siguiente paso es utilizar estos datos y someterlos al modelo Ramdom Forest, ya que este fue el cual nos dio un mejor resultado.

![image](https://user-images.githubusercontent.com/40529168/139970567-b4772299-be49-4044-a6fe-5c901d6d9f73.png)

![image](https://user-images.githubusercontent.com/40529168/139970599-7dea5260-c6a8-469f-b624-1bcbb28442cf.png)

![image](https://user-images.githubusercontent.com/40529168/139970631-90ad5f57-1913-4f4f-a153-0a8bb8f5ff59.png)

![image](https://user-images.githubusercontent.com/40529168/139970648-a12f39a4-608f-46fa-b683-93056fd084a1.png)

![image](https://user-images.githubusercontent.com/40529168/139970661-9ffccb0d-781c-4f15-86ac-02d27357e86a.png)

![image](https://user-images.githubusercontent.com/40529168/139970708-21f78d56-48b7-4b73-b3a8-f47e6c79479d.png)

![image](https://user-images.githubusercontent.com/40529168/139970730-918ba0d5-da15-4376-b394-ae7b018a482e.png)

![image](https://user-images.githubusercontent.com/40529168/139970758-a8ad7ef8-5fc6-4eec-947a-30cdfed5f48c.png)

![image](https://user-images.githubusercontent.com/40529168/139970782-96aa7bef-5a35-47f7-8a2f-ebf2af55e661.png)

