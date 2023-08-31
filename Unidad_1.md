# 21/08/2023

identificar y docuemta el agente, qué realiza , sensores, percepciones actuadores y acciones 

Identificar: ***Una impresora 3d gigante constructura de casas*** 

## Documentar el agente qué realiza: 

El agente construye estructuras 

Sensores: 

- Camaras

- Teclado

- Raton

Percepciones: 

- Percibe la forma en la cual va dejando todo el material que va poniendo encima de otro material 
- 

Actuadores: 

- Su expulsador de material para la construcción de casas atravez de su cabezal
- manguera de material 


Acciones: 

- Son sus motores de expulsión y motoroes que le permiten movimientos elaborados para la creción de una estructura deseada



## Elabora la función del agente en forma de tabla 



Percepciones | Acción 
--- | ---
Detecta un render a realizar,da clic para empezar | Empieza a construirlo 
Detecta un render a realizar, valida que haya material para hacelo | Nada
Detecta que no hay render a realizar, da clic a empezar | Nada
Detecta que un render a realizar, valida que hay material para hacelo y le dan clic para empezar | Empieza a constuirlo 
No queda suficiente material | Deja de construir 

## Agente racional 

Un agente racional es aquel que hace lo correcto. 

Cada elemtnon de la tabla que define la función del agente se tendriá que rellnear correctamente . 

Lo correcto = resultado mejor

Medir el éxito 

como regla general, es mejor diseñar medida que utilidad  de acuerdo con lo que se quiere para el entorno, más que de acuerdo con cómo se cree que el agente debe comportarse. 

## Racionalidad

1. La medida de rendimeinto qe define el criterio de éxito 
2. El conocmiento del medio en el que habita acoumulado por el agente 
3. Las accioens que el agente puede llevar a cabo
4. La secuencia de percepciones del agente hasta este momento 


EN cada posible secuencia de percepciones, un agente racionald eberá emprender aquellla acción qe suspuestamente maximice su medida de rendimeinto, casándose en las evidencias aportadas por la secuencia de percepcioens y en el conocmiento que el agente mantiene almacenado . 

## Tarea 

Elaborar en PowerPoint una narración del tema de agente inteligente (que incluya los conceptos de agente inteligente, racionalidad, rendimiento, aprendizaje y autonomía) en forma de PECHAKUCHA



# 24/08/2023

## Entorno de trabajo 

Las medidas de rendimiento, el entrno, los actuadores y sensores del agente, todo ello forma lo que se llama el **entnrno de trabajo**, para cuya denominación se utiliza el acrónimo **REAS** (Rendimiento, Entorno, Actuadores, Sensores).

## Arquitectura 

El trabajo de la IA es diseñar el programa del agente que implemente la función del agente que proyecta las percepciones en las acciones.

Se asume que este programa se ejecutará en algún tipo de computador con sensores físicos y actuadores, lo cual se conoce como **arquietctura:**

> **Agente = arquiectura + programa**

La arquitectura hace que 
- Las percepciones de los sensores estén disponibles para el programa 
- ejecuta los programas 
- Se encarga de que los acutadores pongan en marcha las acciones generadas


## Actividad 

Del vídeo que analizaste y docuemtnaste de la Era de I.A., identifica y agrega eal docuemtno el REA:
el agente, medidas de rendmiento, entorno y arquitectura.

Agente | Medida de rendimientos | Entorno | Actuadores  | Sensores | Percepcion
--- | --- | --- | --- | --- | ---
Impresora 3d gigante | La optimización de material para no desperdiciar tanto material<br>Hacer de forma correcta del renderizado<br>Seguro <br> Rápido | Medio ambiente hostil de otro planeta<br>Suelo rugoso | Brazo de expulsión de material | Sensores de temperatura <br> Cámara <br> Teclado y Mouse | Percibe a través del de temperatura si el material aún es maleable para seguir construyendo <br> Con la cámara percibe si la forma que está siguiento es correcta <br> 


# 31/08/2023 

**Tipos de agentes**

1. Agentes reactivos simples

- Estos agentes seleccionan las acciones sobre la base de las percepciones actuales, ignorando el resto de las percepciones históricas.
  - Ejemplo 1 
    - El agente del mundo de la aspiradora


 >**función** AGENTE-ASPIRADORA-REACTIVO([*localización*,*estado*])**devuelve** una acción. <br>
 **si** *estado* = *Sucio* **Entonces devolver** *Aspirar*<br>
 **de otra forma, si** *localización* = *A* **entonces devolver** *Derecha*<br>
 **de otra forma, si** *localización* = *B* **entonces devolver** *Izquierda*



> Por lo visto este agente presenta una condición en la cual se le puede colocar una condición 


> Se basan en la regla **condición-acción**

- Ejemplo 2
  - **Si** el-coche-que-circula-delante-está-frenando **entonces** iniciar-frenada

```prolog


función AGENTE-REACTIVO-SIMPLE(percepción) devuelve una acción
    estático: reglas, un conjunto de reaglas condición-acción

    estado <- INTERPRETAR-ENTREADA(percepción)
    regla <- REGLA-COINCIDENCIA(estado,reglas)
    acción <- REGLA-ACCIÓN[regla]
    devolver acción
```

2. Agentes reactivos basados en modelos

3. Agentes basados en obejtivos 

4. Agentes basados en utilidad



**Tipos de entornos**

Agente inidividual vs multiagente

Totalmente observales vs parcialmlente observables

Determinista vs Estocástico

Epsódico vs secuencia

Estático vs Dinámico
Exponer el entorno y un ejemplo de cada uno 

Documentar la investigación que incluya 

- Definición de un tipo de entorno 
  - Estático
    - Un entorno estático es un conjunto de condiciones y circunstancias en el que un agente interactúa, y estas condiciones no cambian por sí mismas durante la interacción del agente.
  - Dinámico
    - Un entorno dinámico es un conjunto de condiciones y circunstancias que pueden cambiar durante la interacción de un agente, lo que requiere que el agente sea capaz de ajustar su comportamiento para tomar decisiones óptimas.

- Ejemplo de agentes
  
  - Estático 
    - **Calculadora**

Agente | Medida de rendimientos | Entorno | Actuadores  | Sensores 
--- | --- | --- | --- | --- 
Calculadora | Rápidez al realizar cálculos <br> Cálculos correctos | Salones de clase <br> Laboratorios <br> Comercios | Pantalla | Teclas <br> Procesador


   - Dinámico
      - **Coche autónomo**

Agente | Medida de rendimientos | Entorno | Actuadores  | Sensores 
--- | --- | --- | --- | --- 
Coche autónomo | Precisión con la que reconoce autos y personas <br>  | Calles <br> Carretera <br> Estacionamientos <br> Chochera | Llantas <br> Motor <br> | Cámaras <br> Volante  
