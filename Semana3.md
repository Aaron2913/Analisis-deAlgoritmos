# Semana 3 : Designing Algorithms  
**Referencia: Cormen et al., 2022 – Introduction to Algorithms**

---

##  ¿Qué significa diseñar un algoritmo?

Diseñar un algoritmo implica encontrar una **solución paso a paso** para resolver un problema, de forma que sea **correcta**, **eficiente** y **comprensible**. En esta sección, Cormen presenta los fundamentos del diseño algorítmico, destacando la importancia de la creatividad, el análisis y la estructura en la resolución de problemas computacionales.

---

##  Principales conceptos

### 1. Estrategias de diseño

- **Dividir y vencer (Divide and Conquer):**  
  Divide el problema en subproblemas más pequeños, resuélvelos de forma recursiva y combina sus soluciones.

- **Algoritmos voraces (Greedy):**  
  En cada paso, toma la decisión óptima local esperando llegar a una solución global óptima.

- **Programación dinámica:**  
  Resuelve subproblemas y guarda sus soluciones para evitar cálculos repetidos.

- **Fuerza bruta y búsqueda exhaustiva:**  
  Prueba todas las posibilidades posibles (efectivo solo en problemas pequeños).

### 2. Consideraciones clave

- **Corrección:**  
  Demostrar que el algoritmo produce la salida correcta para toda entrada válida.

- **Eficiencia:**  
  Evaluar el tiempo y espacio requeridos (normalmente con notación asintótica).

- **Claridad y mantenibilidad:**  
  El algoritmo debe ser comprensible, modular y fácil de adaptar.

### 3. Proceso iterativo

El diseño de algoritmos no es un proceso lineal, sino **iterativo**:
1. Entender el problema.
2. Proponer una solución inicial.
3. Refinarla con pruebas y análisis.
4. Optimizarla si es necesario.

---

##  Ejemplo incluido en el texto

Cormen et al. utilizan ejemplos concretos (como el problema del **ordenamiento**) para mostrar cómo elegir un enfoque algorítmico adecuado y justificarlo con análisis teóricos y prácticos.

---
## Codigo MergeSort
```java
public class MergeSort {

    // Método para mezclar (merge) dos subarreglos de A[]
    // El primer subarreglo es A[p..q]
    // El segundo subarreglo es A[q+1..r]
    public static void merge(int[] A, int p, int q, int r) {
        int nL = q - p + 1; // longitud del subarreglo izquierdo
        int nR = r - q;     // longitud del subarreglo derecho

        // Crear arreglos temporales para L[] y R[]
        int[] L = new int[nL];
        int[] R = new int[nR];

        // Copiar datos a los arreglos temporales L[] y R[]
        for (int i = 0; i < nL; i++) {
            L[i] = A[p + i];
        }
        for (int j = 0; j < nR; j++) {
            R[j] = A[q + 1 + j];
        }

        // Mezclar los arreglos temporales de nuevo en A[p..r]
        int i = 0; // Índice inicial para L[]
        int j = 0; // Índice inicial para R[]
        int k = p; // Índice inicial para A[]

        while (i < nL && j < nR) {
            if (L[i] <= R[j]) {
                A[k] = L[i];
                i++;
            } else {
                A[k] = R[j];
                j++;
            }
            k++;
        }

        // Copiar los elementos restantes de L[], si hay alguno
        while (i < nL) {
            A[k] = L[i];
            i++;
            k++;
        }

        // Copiar los elementos restantes de R[], si hay alguno
        while (j < nR) {
            A[k] = R[j];
            j++;
            k++;
        }
    }
}
```
![semana3_1](https://github.com/user-attachments/assets/ddc19714-081b-4f0b-b687-20a63def931a)
![semana3](https://github.com/user-attachments/assets/b9b69d23-4409-4ccf-ac48-ef0f4d11bc44)



