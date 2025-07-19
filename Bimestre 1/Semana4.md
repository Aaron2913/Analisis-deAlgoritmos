# Semana 4: Análisis de Tiempos de Ejecución y Notación Asintótica

**Referencias:**
- Cormen et al., 2022 – *Introduction to Algorithms*, Capítulo 3: *Characterizing Running Times*
- Brassard & Bratley, 2006 – *Fundamentos de Algoritmia*, Sección: *Notación Asintótica*

---

## Cormen et al. – Characterizing Running Times

### Objetivo
Entender cómo se mide y compara el rendimiento de algoritmos a gran escala, usando funciones matemáticas que representan su tiempo de ejecución.

- **Tiempo de ejecución**: se mide en función del tamaño de la entrada (*n*).
- **Función de crecimiento**: no se interesa en tiempos exactos, sino en cómo escala el algoritmo.
- **Caso peor, promedio y mejor caso**: se distinguen según el tipo de entrada.
- Introducción a la **notación asintótica**:
  - **O grande (O(n))**: cota superior
  - **Ω (Omega)**: cota inferior
  - **Θ (Theta)**: cota ajustada (exacta)
- **Comparación de funciones**: crecimiento lineal vs. logarítmico, polinomial vs. exponencial, etc.

### Ejemplo:
Un algoritmo de búsqueda secuencial tiene tiempo O(n), mientras que uno de búsqueda binaria tiene O(log n).

---

## Brassard & Bratley – Notación Asintótica

### Enfoque
Introducir de manera más intuitiva cómo expresar el rendimiento de algoritmos sin centrarse en detalles de implementación o constantes.

### Puntos clave:
- Uso de analogías y ejemplos sencillos para explicar los conceptos.
- **Notación O** como herramienta para ignorar constantes y enfocarse en la "forma" del crecimiento.
- No se enfatizan tanto las pruebas formales como en Cormen, sino el **entendimiento práctico**.
- Se da especial atención a que la notación asintótica ayuda a **comparar algoritmos**, incluso sin implementarlos.

### Ejemplo visual:
Comparación entre algoritmos de ordenamiento por inserción (O(n²)) y mergesort (O(n log n)) usando gráficos e intuición.

---

## Comparación General

| Aspecto                | Cormen et al. (2022)                        | Brassard & Bratley (2006)               |
|------------------------|---------------------------------------------|-----------------------------------------|
| Enfoque                | Matemático, riguroso y formal               | Intuitivo, pedagógico                   |
| Profundidad            | Alta: analiza todos los casos y demostraciones | Media: se enfoca en conceptos prácticos |
| Presentación de O, Ω, Θ| Formal con definiciones precisas           | Intuitiva y aplicada                    |
| Público objetivo       | Estudiantes con bases matemáticas           | Principiantes en algoritmos             |

---
### Taller Semana 4 :


![semana4](https://github.com/user-attachments/assets/4e5767f0-0ca5-48af-972d-c4582ca029b9)


