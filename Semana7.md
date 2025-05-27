# Semana 7: Notación Asintótica  
**Referencia: Brassard & Bratley, 2006 – Fundamentos de Algoritmia, Tema 3**

---

## ¿Qué es la Notación Asintótica?

La **notación asintótica** describe el comportamiento del tiempo de ejecución de un algoritmo cuando el tamaño de entrada **tiende a infinito**. Es una herramienta fundamental para **comparar algoritmos** sin depender de la implementación o hardware.

---

## Objetivos principales

- Representar el **orden de crecimiento** del tiempo de ejecución.
- Enfocarse en el **comportamiento a gran escala** (no en detalles finos).
- Ignorar constantes y términos de orden inferior.

---

## Tipos de Notación

| Notación     | Significado    | Interpretación                                        |
|--------------|----------------|-------------------------------------------------------|
| **O(f(n))**  | Cota superior  | El algoritmo no tarda más que f(n) en el peor caso   |
| **Ω(f(n))**  | Cota inferior  | El algoritmo tarda al menos f(n) en el mejor caso    |
| **Θ(f(n))**  | Cota ajustada  | El tiempo de ejecución está acotado por f(n) arriba y abajo |

> *Brassard & Bratley enfatizan la comprensión intuitiva y visual de estas cotas.*

---

## Ejemplos prácticos

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
Comparación de funciones de crecimiento
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

---
![Captura de pantalla 2025-05-27 134340](https://github.com/user-attachments/assets/0034c953-72cc-4255-b4a8-b69ccfb486b2)
---
## Codigo de Fibonacci
```java
public class FibonacciIterativo {
    public static int fibonacci(int n) {
        if (n <= 1) return n;
        int a = 0, b = 1, temp;
        for (int i = 2; i <= n; i++) {
            temp = a + b;
            a = b;
            b = temp;
        }
        return b;
    }

    public static void main(String[] args) {
        int n = 10;
        System.out.println("Fibonacci de " + n + " es: " + fibonacci(n));
    }
}
```
---
![semana7](https://github.com/user-attachments/assets/8bf67256-7c45-459b-9ff4-b09f5f0f6cc8)



