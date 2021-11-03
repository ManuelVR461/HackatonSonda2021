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




