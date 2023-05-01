# (NLP) Predicción y visualización de palabras basadas en el contexto con PCA(Principal Component Analysis)

## Word2vec
Wor2vec es una red neuronal de dos capas que procesa texto "vectorizando" palabras. Su entrada es un corpus de texto y su salida es un conjunto de vectores; vectores de características que representan palabras en este corpus. Aunque Word2vec no es una red neuronal profunda, transforma el texto en una forma numérica que las redes neuronales profundas pueden entender.

Word2vec es un método para calcular representaciones vectoriales de palabras y fue desarrollado por un equipo de investigadores de Google dirigido por Tomas Mikolov. Google aloja una versión de código abierto de Word2vec lanzada bajo una licencia Apache 2.0. En 2014, Mikolov dejó Google por Facebook y, en mayo de 2015, a Google se le otorgó una patente para el método, que no revoca la licencia de Apache bajo la cual se haya publicado.

Aquí está el papel original -> https://arxiv.org/pdf/1301.3781.pdf

Las aplicaciones de Word2vec van más allá del análisis de oraciones. También se puede aplicar a genes, códigos, me gusta en redes sociales, listas de producción, gráficos de redes sociales y otras series verbales o simbólicas en las que se pueden discernir patrones.

¿Por qué? Como las palabras son solo estados discretos, al igual que otros datos mencionados anteriormente, simplemente estamos buscando las probabilidades de transición entre estos estados, es decir, la probabilidad de que ocurran simultáneamente. Entonces gene2vec, line2vec y follower2vec son posibles.

El propósito y la utilidad de Word2vec es agrupar vectores de palabras similares en un espacio vectorial. Es decir, detecta similitudes matemáticamente. Word2vec crea matrices que son representaciones numéricas distribuidas de características de palabras, características como el contexto de palabras individuales. Lo hace sin intervención humana.


Con suficientes datos y contexto, Word2vec puede hacer conjeturas muy precisas sobre el significado de una palabra en función del contexto. Estos supuestos se pueden utilizar para establecer la asociación de una palabra con otras palabras (por ejemplo, hombre es niño y mujer es niña) o para agrupar documentos y clasificarlos por tema. Estas agrupaciones pueden formar la base de la investigación, el análisis de sentimientos y las recomendaciones en diversos campos, como la investigación científica, la extracción de documentos, el comercio electrónico y la gestión de relaciones con los clientes.

El resultado de la red neuronal de Word2vec es un vocabulario en el que cada elemento tiene un vector adjunto, que puede introducirse en una red de aprendizaje profundo o simplemente consultarse para detectar relaciones entre palabras.

Midiendo la semejanza del coseno, ninguna semejanza se expresaría como un ángulo de 90 grados, mientras que la semejanza total de 1 es un ángulo de 0 grados, es decir, la palabra Suecia es igual a la palabra Suecia, mientras que la palabra Noruega tiene una distancia de cossen de 0.760124 de la palabra Suecia, por ejemplo.

## Semejanza de Coseno
Entre las diferentes métricas de distancia, la similitud del coseno es más intuitiva y más utilizada en Word2vec. Es un producto normalizado de 2 vectores y esta relación define el ángulo entre ellos. Dos vectores con la misma orientación tienen una similitud de coseno de 1, dos vectores a 90° tienen una similitud de 0 y dos vectores diametralmente opuestos tienen una similitud de -1, independientemente de su magnitud.

Dado que las palabras están representadas por vectores, la tarea de encontrar palabras similares o diferentes se vuelve más fácil. Cualquier combinación de vectores da como resultado un nuevo vector y se pueden usar distancias de coseno u otras medidas de similitud. Así resolveremos la famosa ecuación que define a Word2vec:

***rei-homem+mulher=rainha*** 

