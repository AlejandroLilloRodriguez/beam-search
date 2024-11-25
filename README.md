# Beam Search
This is a little research on Beam Search, an heuristic search algorithm used for NLP, Robotics, Game AI ...

Beam Search es un algoritmo de busqueda heurística que trata de encontrar la solución mas probable de un conjunto de nodos. 
Este algoritmo, expande los nodos que tienen mayor probabilidad . Se suele ultilizar en modelos secuenciales, donde el orden importa.

Beam Search, comienza en un nodo inicial, en dicho nodo genera todos sus hijos posibles . A cada hijo se le asigna un valor heurístico y seleccciona los N mejores. A partir de este paso, se repite la secuencia hasta seleccionar el camino con la mayor puntuación global. 

¿Entonces, que hay de difrenete con la busqueda Naive Search ?.

Naive Search , a dieferencia del algoritmo Beam Search , realiza una expansión *completa* de los nodos , en cambio en el algoritmo Beam Search realizabamos la expansión sobre aquellos nodos que tuvieran el mejor valor heurístico o *beam width*. Esto garantiza encontrar la solución óptima, sin embargo el espacio de búsqueda crece exponencialmente en algunos casos. 
Pongamos un ejemplo concreto :

Imaginemos que estamos programando un traductor con un algoritmo de busqueda Naive Search , cualquier lenguaje , mismamente el español tiene miles de palabras en su vocabulario . Como consecuencia , a la hora de buscar la traducción de dichas palabras , expandería todos los nodos existentes dando lugar a un tiempo de computación exagerado y formando combinaciones y no necesitan ser consideradas.


