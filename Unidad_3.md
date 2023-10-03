# 

* Comprender los conceptos básicos de lso algoritmso de búsqueda preferente de lo mejor d
* Elaborar el árbol de búsqueda avara 
* Entender el aogoritmo de búsqueda de costo uniforme 
* Obtener el árbol de búsque dal algormit de una aplicación mapa de Rumania 
* Comprender el algoritmo búsqueda A*


## Búsqueda preferente por lo mejor 

Función de evaluacion: 
Es una función qeue produce un número que sirve para represntar lo deseable que seriá la expasión de un nodo. 

Por ejemplo, el costo de ruta *g* (algoritmo de búsqueda por costo unirofme) es una función de evaluación. 

Cuando los nodos se ordenan de manera tal que se expande primero aquel con mejro evaluación, entonces se trtata de una estrategia denomiada **búsqueda preferente opr lo mejor**.

Ejemplo: Búsqueda de costo uniforme 

El nombre "búsqueda preferente por lo mejor" es respetable,pero impreciso. Al fin y al cabo, si en verdad fuese posible expader desde un principio el mejor nodo, en realidad no se trataris que búsqueda .

1. Expandir el nodo más cecano a la meta(búsqueda avara)
2. Correspondiente a la ruta de la resolución menos costosa (A*)

## Búsquda avara

Esta estrategia sconsiste en , el nodo cuyo estado se consider ser el más cercano al estado meta es el que siempre se expande primero
La función se que utilia para calcular tales estimados de costo se conoce como función herurística, generalmente simbolizada por la legra h. 

Hérístico: Técnica de la indagación y del descubrimiento. RAE

h(N)= costo estimado de la ruta más barata que une el estado del nodo n con un estado meta. 

Aquella búsqueda prefernete por lo mejro que utiliza h para escoger cuál es el siguietne nodo que se va a expander es denomiando **búsqueda avara**. 

### Ejemplo

Desde el punto de vista formal, h puede se cualqueir función El único requisito es que h(N) = 0 cuando n es el estado meta. 


La función heurística h puede ser: 
para el juego de las ocho fichas: 
h(N) = el núermode fichas desscolocadas ( comparadas con la configuación meta o el estado meta)

## Búsqueda A*

Eslte algoritmo convina dos algoritmos

**f(n)= g(n) + h(n)**

g(n)= el costo de la ruta que va del nodo de partida al nodo n

h(n)= es el costo estimado de la rut amás barata que va dle nodo n a la meta 

f(n) = costo estmaido de la solución más barata pasando por n.

Aqui se usan ambos números por ejemplo la heuristiaca de línea recta en lso arcos adjayuentes enca da espacio. 

Ejemplo búsqueda A* 

Es una combinación entre las de distancia euclidiana y una hamming 

ahroa se suman dos distancias



