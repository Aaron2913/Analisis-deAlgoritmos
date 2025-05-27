# Semana 7: Notación Asintótica  
**Referencia: Brassard & Bratley, 2006 – Fundamentos de Algoritmia, Tema 3**

---

## 🔸 ¿Qué es la Notación Asintótica?

La **notación asintótica** describe el comportamiento del tiempo de ejecución de un algoritmo cuando el tamaño de entrada **tiende a infinito**. Es una herramienta fundamental para **comparar algoritmos** sin depender de la implementación o hardware.

---

## 🔹 Objetivos principales

- Representar el **orden de crecimiento** del tiempo de ejecución.
- Enfocarse en el **comportamiento a gran escala** (no en detalles finos).
- Ignorar constantes y términos de orden inferior.

---

## 🔹 Tipos de Notación

| Notación     | Significado    | Interpretación                                        |
|--------------|----------------|-------------------------------------------------------|
| **O(f(n))**  | Cota superior  | El algoritmo no tarda más que f(n) en el peor caso   |
| **Ω(f(n))**  | Cota inferior  | El algoritmo tarda al menos f(n) en el mejor caso    |
| **Θ(f(n))**  | Cota ajustada  | El tiempo de ejecución está acotado por f(n) arriba y abajo |

> *Brassard & Bratley enfatizan la comprensión intuitiva y visual de estas cotas.*

---

## 🔸 Ejemplos prácticos

### 1. Suma de los primeros n enteros:
```java
s := 0
for i := 1 to n do
  s := s + i

⏱ Tiempo: O(n) → ejecución lineal
```
2. Doble bucle anidado:
```java
for i := 1 to n do
  for j := 1 to n do
    hacer algo
⏱ Tiempo: O(n²) → crecimiento cuadrático
```
3. Búsqueda binaria:

buscar elemento en lista ordenada

⏱ Tiempo: O(log n) → muy eficiente en entradas grandes
🔸 Comparación de funciones de crecimiento
| Función      | Crecimiento |
| ------------ | ----------- |
| constante    | O(1)        |
| logarítmica  | O(log n)    |
| lineal       | O(n)        |
| linealítmica | O(n log n)  |
| cuadrática   | O(n²)       |
| cúbica       | O(n³)       |
| exponencial  | O(2ⁿ)       |

## Conclusión:
La notación asintótica permite clasificar algoritmos según su eficiencia.
Es crucial para el diseño y selección de algoritmos en problemas reales.
Brassard & Bratley presentan estos conceptos de forma intuitiva y gradual, facilitando la comprensión incluso para quienes se inician en el tema.
