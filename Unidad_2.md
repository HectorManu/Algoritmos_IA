# Resolución de problemas mediante búsquedas

## ¿ Qué son lso agentes resolventes? 

Es un resolvente de problemas es un agente inteligente que puede elegir un objetivo y tratar de satisfacerlo. 

- UN OBJETIVO ES UN CONJUTNO DE ESTADOS DEL MUNDO QUE SATIFACEN EXACTMENTE EL OBJETIVO 
- FORMMULACIÓN DEL PROBLEMA 
- Busqueda- la secuencia de acciónes de toda la gama el tiene que hacer el proceso para encontrar la secuencia posible de acciones 
- Solución
  - Secuencia de acciones que va a dar como resultado de un algoritmo de busqueda 
- Ejecución 
  - aplicar el resultado del algoritmo 


## componentes de problema 
- Estado inicial 
  - Es el estado de donde el agente inicial de búsqueda d ela solución 
- Acciones
  - Es lo que el agente puede realizar en el estado actual 
- Función osucesor 
  - dado en un estado particular x, devuelve un conjunto de pares ordenados acción, sucesor donde <br> cada acción es una de las acciones legaes en el estado x, <br> cada sucesor es un estado que puede alcanzarse desde x, <br> aplicando la acción.
- Espacio de estados
  - Conjunto de todos los estados alcanzables desde el estado inicial
  - **¿cuál es mi espacio de estados?**

par qué sirven los algoritmos de búsqueda
- por amplitud 
- preferente por profundidad 
- costo uniforme
- primero en profundidad con profundidad iterativa
- profundidad limitada
- bidireccional


1. Ejemplo 1 
El juego de las 8 fichas
- **Estado** : ubicación de cada número en las 9 cuadros
- estado inical : cuaalquier estado
- estado objetivo: cualquier estado
- acciones: mover el blanco a la izquierda, derecha arriba o abajo
- Prueba objetivo:¿Estoy en el estado objetivo?
- costo de camino: s1 por cad amovimiento


2. Ejemplo 2 
El recorrido de mapas
- Estado: cada estado está represenetado por una ciudad del mapa de rumania
- Estado inicial: cualquier estado
- Estado objetivos: cualquier estado
- acciones: viajar de uan ciudad a otra o que esté indicada en el mapa
- Prueba objetivo: ¿Estoy en el estado objetivo?
- costo de camino: Distancia entre una ciudad y otra

**HAY QUE PONER EL ESPACIO DE ESTADOS**

3. Ejemplo 3
Mundo de la aspiradora
condiciones iniciales
- estado: en este mudno hay dos posible ubicaciones A o B <br> en ellas puede o no haber mugre. El agente aspiradores ase encuenta cuaklqueir 

**TAREA hacer el espacio de estados completo**

nodo frontera- nodos no explorados que aún no se ve si se puden expandir 

nodos hojas: al grupo de nodos queya fueron expandidos y no tiene hijos o sucesores

La estrategias de búsqueda se evaluarán bajo 4 criterios:
1. Completitud ¿la estrategia garantiza eoncontrar una solución, si es que eésta existe?
2. Complejidad temporal: ¿Cuánto tiempo se necesitará para encontrar una solución?
3. complejidad espacial: ¿cuánta memoria se neceisita para efectuar la búsqueda?
4. Optimo: ¿con estas estrategias se encontrará una solución de las más alta calidad, en cadso de que existan varias soluciones


en el proyecto final se resolverá el mismo problema pero con diferente algoritmo 


### Búsqueda peferente por amplitud

amplitud o por anchura

Este método de búsqueda primer toma en cuenta todas las rutas de longitud 1, luego las de longitud 2, etc. 

En caso de habe rsolución, la encuentrará, si son varias soluciones, este tipo de búsqueda encontrará primero el nodo destino (estado meta) más próximo. 

en este utilizan un nodo fifo es decir que el primero que va a expandir es el primero que llego. primeor genera cada nodo hijo por cada nivel del árbol 

# 14/09/2023



Búsqueda preferente por profundidad

Este método de búsqueda consiste en encontrar un camino cuyos nodos han sido seleccionados de acuerdo a un criterio sni fundamento. 

Algoritmo búsqueda preferente por profundidaad 

Localizar nodo raíz 

Búsqueda prefernte por profundidad 

Sóslo si la búsqueda conduce a un **callejón sin salida** (un nodo sin meta que no tiene expansión), se revierte la búsqueda (ir a un nivel antterior) y se expanden 


# exposición de la busqueda bidireccional 

1. nodo: estado del problema en un momento dato hay tres tipos 
2. nodo inicial 
3. objetivo 
4. transición 

árbol de expansión subconjunto de aristas de un grafo conexo en quee conct todos los vértices que se genera en la búsqueda del nodo . 

Objetivo 

Reducción del espacio de búsqueda 
Mejor eficiencia 
Garantizar uan solución óptima 
Identificar rutas más cortaas 

Ventajas 
- Se necesita conocer el estado objetivo de manerra explícita 
- Se necesita de operadores inversos para genera lsos estaods predecesores de un lado ( significa que no avanza hacia delante si no que necesitas saber de donde vienes )
- Recuperación de información más completa.

Desventajas

- Mayor coste computacional 
- Requerimientos de datos invertidos adicionales. (como se ocupaon dos busquedas se tiene que tner dos busquedas)
- Pérdida de eficiencia(no en todos los casos se necesita este algoritmo )

Problema 

- Ir desde el nodo 1 hasta el nodo 7 solo pudiendo trnsitar por los arcos definidos en la imagen 

- Ir desde el nodo 7 hasta el nodo 1 solo pudiendo transitar de forma inversa por los arcos definidos en la imagen 


Esto se resuelve con dos listas inicial y una lista final es decir 2 árboles.  