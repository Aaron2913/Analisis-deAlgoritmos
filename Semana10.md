# 📚 Semana 10 – Algoritmos Voraces  
## Subtema 6.4: Grafos – Caminos mínimos

**Referencia**:  
Brassard, G., & Bratley, P. (2006). *Fundamentals of Algorithmics*. Prentice Hall.

---

## 🗺️ ¿Qué es el problema de caminos mínimos?

Dado un **grafo ponderado** (con pesos en las aristas), el problema de **caminos mínimos** consiste en encontrar el camino de **costo mínimo** entre un nodo origen y los demás nodos del grafo.

Existen variantes:

- Camino mínimo desde un nodo a todos los demás (problema de fuente única).
- Camino mínimo entre todos los pares de nodos.

Este subtema se enfoca en la solución **voraz** para el problema de **fuente única**, con el algoritmo de **Dijkstra**.

---

## 🧠 Algoritmo de Dijkstra

### ✔️ Supuestos
- El grafo es **dirigido o no dirigido**.
- Los pesos son **no negativos**.

### 🚀 Idea principal
Construir un conjunto de nodos con distancia conocida mínima desde el origen, expandiéndolo de forma **voraz**: siempre se elige el nodo más cercano aún no procesado.

---

## 🛠️ Esquema del algoritmo de Dijkstra

```plaintext
1. Inicializar la distancia de todos los nodos como ∞, excepto el origen (0).
2. Marcar todos los nodos como no visitados.
3. Mientras haya nodos no visitados:
   a. Seleccionar el nodo no visitado con menor distancia actual.
   b. Marcarlo como visitado.
   c. Actualizar las distancias de sus vecinos si se mejora el camino actual.
```
### Ejemplo
```plaintext
A --1--> B --2--> C
 \       |
  \--4--> D --1--> C
```
Camino más corto desde A:

    A → B → C (costo 1 + 2 = 3)

    A → D → C = 4 + 1 = 5 → No óptimo
  # 🔧 Pseudocódigo del Algoritmo de Dijkstra

```plaintext
Entrada:
    - Grafo G = (V, E), con pesos positivos en las aristas
    - Nodo origen s ∈ V

Salida:
    - dist[v]: distancia mínima desde s hasta cada nodo v ∈ V
    - prev[v]: nodo anterior en el camino mínimo desde s hasta v

Procedimiento Dijkstra(G, s):
    para cada nodo v en V hacer:
        dist[v] ← ∞
        prev[v] ← indefinido
    dist[s] ← 0

    Q ← conjunto de todos los nodos en V

    mientras Q no esté vacío hacer:
        u ← nodo en Q con menor dist[u]
        eliminar u de Q

        para cada vecino v de u:
            si (u, v) ∈ E entonces:
                alt ← dist[u] + peso(u, v)
                si alt < dist[v] entonces:
                    dist[v] ← alt
                    prev[v] ← u

    retornar dist, prev
```
--------------------------------------------------------------------------------------------------------------------------------------------
![Imagen de WhatsApp 2025-07-19 a las 15 43 35_28c02788](https://github.com/user-attachments/assets/46da5e53-7927-4146-a269-4d93dce915df)

![Imagen de WhatsApp 2025-07-19 a las 15 43 35_a1d92edc](https://github.com/user-attachments/assets/ce7b6abb-d404-4b1c-80d8-8df65876ad54)


