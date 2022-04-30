# U1 Activity NLP

author: Miquel Antoni Llambías Cabot

## How to run

1. Install python
2. Install python dependencies. Install dependencies with `pip install requirements.txt`
3. download `OpinRankDatasetWithJudgments.zip` from [OpinRank](https://github.com/kavgan/OpinRank/tree/master) and unzip it into `/data` directory
    - Download: `curl https://github.com/kavgan/OpinRank/raw/master/OpinRankDatasetWithJudgments.zip -o "data/OpinRankDatasetWithJudgments.zip"`
    - Unzip [windows + 7zip]: `7z x -y "data/OpinRankDatasetWithJudgments.zip" -odata`
    - Unzip [mac]: `unzip "data/OpinRankDatasetWithJudgments.zip"`

## Objetivo

Queremos analizar el dataset de opiniones, [OpinRank](https://github.com/kavgan/OpinRank/tree/master) y responder a las siguientes cuestiones:

1. ¿Qué partes de una habitación son las más mencionadas?
2. ¿Qué servicios pueden detectarse por cada hotel?
3. ¿Qué lugares y qué porcentaje de revisiones sobre cada ciudad mencionan otras ciudades, regiones o puntos de interés turístico?
    - ¿en Las Vegas se menciona el Gran Cañón del Colorado?

## Desarrollo

Se ha realizado el análisis entorno a las librerías de `ipyparallel`, `pandas`, `nltk` y `spacy`.

La librería de `ipyparallel` permite hacer uso de multithreading para aprovechar mejor la potencia de cálculo de nuestro ordenador o uso de un cluster.

La librería de `pandas` permite manejar los datos como tablas y a hacer los gráficos.

Las librerías de `nltk` y `spacy` son los procesadores de lenguaje natural. En los dos primeros apartados se ha usado `nltk` y `spacy` en el último. Se ha usado `nltk` y su wordnet para realizar búsquedas de palabras dada una definición muy concreta. En el primer apartado, lista de habitaciones y en el segundo, lista de servicios.
Spacy por otro lado, permite etiquetar palabras por significado, sin necesidad de que sea algo muy concreto. En nuestro caso, ubicaciones.

## Resultado

Los resultados de cada apartado se pueden encontrar en formato CSV como `resultado_apartado_1.csv`, `resultado_apartado_2.csv` y `resultado_apartado_3.csv`. O como html para ver el proceso y código utilizado paso a paso.
