# TP2-LDD-2C-2023 - Armado de modelos sobre el `fashion-mnist` dataset
## 2do Trabajo Practico de la materia Laboratorio de Datos

Este trabajo consistio en analiza en una primera instancia como se distribuian los datos e identificar cuales eran los atributos mas valiosos entre las distintas clases para asi poder hacer una mejor prediccion.

Luego armamos un modelo de clasificacion KNN el cual separa entre remeras y pantalones entrenandolo con solo 4 pixeles de cada muestra del 80% del dataset.

Tambien armamos un modelo de Arbol de Clasficacion el cual clasifica entre todos los tipos de prendas usando todos los pixeles de cada muestra.

Las bibliotecas que utilizamos son:

`pandas`,`numpy`,`matplotlib.pyplot`,`seaborn`,`sklearn.neighbors`.

El archivo `TP2-fashionMNIST-Consigna.pdf` es la consigna del trabajo practico del cual tenemos las preguntas que organizan el TP.

El archivo `TP2_Informe.pdf` es nuestro informe donde detallamos los pasos hechos y las decisiones tomadas, ademas de tener graficos sobre el dataset y los modelos, y las conclusiones obtenidas.

El repositorio no cuenta con el dataset por cuestiones de peso ya que el mismo cuenta con 60000 muestras de 785 columnas, para descargarlo clickea [aca](https://www.kaggle.com/datasets/zalando-research/fashionmnist). Tambien en el mismo link se encuentra el dataset de testeo compuesto por otras 10000 muestras que usamos para testear los modelos una vez entrenados y calibrados

# Requisitos:
1. Instalar Python >= 3.8
2. Instalar las bibliotecas mencionadas (Se recomienda usar Anaconda/Miniconda)
3. Instalar las extenciones de Python y Jupyter Notebook
4. Descargar los datasets necesarios [(aca)](https://www.kaggle.com/datasets/zalando-research/fashionmnist)

# Informacion del Dataset
Extraido de [Kaggle](https://www.kaggle.com/datasets/zalando-research/fashionmnist)

1. Each training and test example is assigned to one of the following labels:

      - 0 T-shirt/top
      - 1 Trouser
      - 2 Pullover
      - 3 Dress
      - 4 Coat
      - 5 Sandal
      - 6 Shirt
      - 7 Sneaker
      - 8 Bag
      - 9 Ankle boot

3. Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total.
4. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker.
5. This pixel-value is an integer between 0 and 255.
6. The training and test data sets have 785 columns.
7. The first column consists of the class labels (see above), and represents the article of clothing.
8. The rest of the columns contain the pixel-values of the associated image.

# Funciones armadas:
   - `mostrarImagen`: Devuelve una imagen dentro de la clase seleccionada
   - `imagenPromedio`: Devuelve la imagen promedio de una clase
   - `graficoDistribucionDeClase`: Nos devuelve un mapeo de frecuencias de cuales c
   - `validacionCruzada`: Realiza una validacion cruzada con un modelo dado realizando *k* pliegues en el set de entrenamiento, devuelve los scores obtenidos
   - `testarModelo`: Recibe un modelo y un dataset y realiza un training y realiza una prediccion para devolvernos el puntaje obtenido
   - `calibrarModelo`: Recibe un modelo sin hiperparametros seleccionados y un data set y nos devuelve los hiperparametros mas optimos con el puntaje obtenido

