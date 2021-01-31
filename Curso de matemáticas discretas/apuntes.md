# Matemáticas discretas
La lógica es aquello con lo que tomamos decisiones, tiene sentido, es coherente.
- Las propocisiones son enunciados que pueden tomar el valor de verdadero o falso.
- Las preguntas, las ordenes, los deseos **NO** se toman como proposiciones.

Con esto podemos hacer relaciones, por ejemplo, si yo digo "Plabo es ingeniero" y "Los ingenieros son aburridos" y ambas proposiciones son verdaderas, puedo concluir que Pablo es aburrido.

Tenemos 2 tipos de proposiciones:
- Simples (formadas por solo 1)
- Compuestas (formadas por 2 o más)

Las proposiciones se suelen representar con las letras: p,q,r,s,t.


Podemos usar conectores lógicos para darle un sentido a estas proposiciones.

Para calcular la cantidad de valores que salen de cada proposicion, hay que usar 2^n.

La tabla de verdad sirve para evaluar una composición compuesta.

- Y (Conjunción): Para que se cumpla el valor de verdadero, TODAS las proposiciones deben ser verdaderas. Se representa  *p^q*
- O (Disyunción débil): Para que se cumpla el valor de verdadero, solamente basta con que 1 proposición sea verdadera. Se representa *pVq*
- O ... o (Disyunción fuerte): Aquí SOLAMENTE 1 proposición debe ser verdadera para tener el resultado de verdadero. Se presenta *pΔq*
- Si ... entonces (Condicional): Aquí solamente tendremos un resultado de falso si el antecedente es verdadero y el consecuente es falso. Se presenta *p -> q*
- ... si y solo si ... (Bicondicional): Obtendremos el valor verdadero cuando ambas proposiciones tengan el mismo valor. Se representa *p <-> q*
- No (Negación): Invierte el valor de la proposición. Se representa *~p*

## Conjuntos
Colección de elementos con características en común.
Se agrupan entre llaves {} y no importa el orden de elementos ni importa si se repiten. Solo importan los elementos en sí.
### Conjuntos por extensión
Expresarlos tal cual.
### Conjuntos por compresión
Describirlos.
### Cardinalidad
Se expresa con '#A' o '|A|' para indicar la cantidad de elementos.
### Subconjunto
Un conjunto dentro de otro.

### Conjuntos especiales
- φ = Conjunto nulo o vacío
- Conjunto unitario : solo hay 1 elemento
- Conjunto universal: Uno que se comprende los demás conjuntos

⋃ Unión = Tomar los elementos de ambos conjuntos, sin repetirlos
⋂ Intersección = Tomar en cuenta sólo los elementos comunes de ambos conjuntos
– Resta: Quitar los elementos que se tienen en común. A-B es quitar de A los comunes que tiene con B. B-A es quitar de B los comunes en que tiene con A.
∈ Pertenencia
∉ No es un elemento de
⊂ Subconjunto estricto
⊃ Superconjunto estricto
|A| Cardinalidad
'#A' Cardinalidad
Cª Complemento: Los elementos que le faltan al conjunto para llegar a ser el conjunto universal

## Grafos
- Vértices: nodos.
El grado de un vértice se mide por la cantidad de aristas que este tiene.
- Aristas: líneas que conectan los nodos.
- Cadena: suceción de aristas.
- Camino: no se pueden repetir los nodos ni las artistas.
- Ciclo: solamente se repite el vértice con el que comenzamos y ese debe ser con el que terminamos.
- Cadena cerrada: se pueden repetir vértices.
- Grafo conexo: todos los vértices están conectados con aristas.
- Grafo NO conexo: no todos los grafos están conectados.

### Caminos eulerianos y ciclos eulerianos
No podemos repetir las aristas
- Cadena euleriana: No más de 2 vértices con grado impar.
- Ciclo euleriano: Todos los vértices con grado par.

### Caminos y ciclos hamiltonianos
No podemos repetir los vértices
- Camino hamiltoniano: Grado(u) + Grado(v) <= n-1; donde "n" es el total de vértices; y (u) y (v) son 2 vértices. SIN EMBARGO, aunque esta condición no se cumpla, no podemos afirmar que el camino NO es hamiltoniano.
- Ciclo hamiltoniano: Terminamos donde empezamos sin repetir vértices.
Si hay camino PERO NO hay ciclo, NO es grafo hamiltoniano.
Si 1 vértice tiene peso de 1, no es ciclo hamiltoniano.

### Matriz de adyaciencia
En las columnas y filas tendremos los nodos. Aquí podremos representar los grafos en una tabla.
De igual manera, con la información de esta tabla podremos crear grafos.
Si hay varias vértices las indicaremos con un número para expresar su cantidad.

### Matriz de incidencia
En las columnas tendremos las aristas y las filas los vértices. En esta matriz solamente tomamos en cuenta si existen conexiones o no, por lo que usamos 1 y 0.

### Grafo dirigido = matriz asimétrica

### Grafo no dirigido = matriz simétrica

En la matriz de adyacencia asimétrica, si sumamos las filas de cada nodo nos dirá la cantidad de conexiones que inciden en el nodo, y si miramos las columna nos dirá sobre que nodo inciden los nodos.

## Árboles
### Nivel y altura de un árbol
El nodo raíz tiene nivel 0.

### Subárboles
Un árbol pequeño dentro del árbol general.

### Vértice terminal
Es el vértice que no tiene un hijo, también llamados hojas.

### Vértices internos
Son los vértices que tienen hijos y no es el raíz.

### Árbol de expansión mínimo
Escoger las aristas con menos peso, empezando con un vértice cualquiera. No se deben presentar ciclos.
Después hacemos el árbol con vértice raíz, sumamos los pesos de cada nivel y obtenemos el valor de
árbol de expansión mínimo.

### Árbol binario
Es una estructura recursiva.
Es un árbol en el cual cada vértice tiene como máximo 2 hijos. Se llama hijo izquierdo e hijo derecho.
- Árbol binario completo: o el nodo tiene 2 hijos o no tienen hijos.
- Árbol binario lleno: lo mismo que el completo PERO todos los nodos llegan al mismo nivel.
- Árbol degenerado: está todo feo y no parece un árbol.

### Recorrido de árboles
- Preorden: Raíz, Izquierda, Derecha
- Inorden: Izquierda, Raíz, Derecha
- Posorden: Izquierda, Derecha, Raíz

### Expresiones aritméticas
- Los vértices terminales son operados (números).
- Los vértices internos son los operadores.
- La raíz SIEMPRE debe ser un operador y es el que tiene más relevancia.
- Prioridad de operadores: Parentésis, raices y exponentes, multiplicación y división y finalmente suma y resta.

## Algoritmo de Prim
Encontrar el coste mínimo de conectar todos los puntos
No se deben formar ciclos.

## Algoritmo de Dijkstra
Encontrar la ruta óptima de un punto con otro.

## Algoritmo de Kruskal
Encontrar la ruta óptima, empezando con la conexión de menor coste y hay que conectar todos los puntos.
No se deben formar ciclos.

## Algoritmo de Fleury
Nos permite encontrar un ciclo euleriano. Hay que agregar nuevos circuitos cerrados con nuevas conexiones.
Hay que visitar las aristas 1 sola vez. La cantidad de veces que aparece un vértice debe ser la mitad de su grado, esto solo no aplica para el nodo inicial.

## Algoritmo de flujo máximo
Pasos:
1. Direccionar los flujos e iniciar en ceros.
2. Obtener trayectorias buscando el mayor flujo.
3. Escoger el menor flujo de la trayectoria, esto es la arista de menor valor dentro de tu camino que seleccionaste.
4. Actualizar el gráfico con las capacidades mínimas, ósea, restando el valor de la arista del anterior paso a cada una de las aristas del camino.
5. Buscar nueva trayectoria o camina en aumento y repetir hasta que no existan más.