# Semana 5: Notación Asintótica  
**Referencia: Brassard & Bratley, 2006 – Fundamentos de Algoritmia**

---

##  Tema 3: Notación Asintótica

### Propósito
La notación asintótica permite **expresar el crecimiento del tiempo de ejecución** de un algoritmo sin importar los detalles de implementación ni las constantes menores.

---

## ¿Por qué se usa?
- Para comparar algoritmos **independientemente del hardware**.
- Para enfocarse en el comportamiento del algoritmo cuando el **tamaño de entrada crece** (caso más importante en análisis de eficiencia).
- Para evitar depender de medidas exactas, centrándose solo en el **orden de crecimiento**.

---

## Tipos de Notación

| Notación | Significado | Interpretación práctica |
|----------|-------------|--------------------------|
| O(f(n))  | Cota superior | El algoritmo **no es peor** que f(n) en el peor caso |
| Ω(f(n))  | Cota inferior | El algoritmo **no es mejor** que f(n) en el mejor caso |
| Θ(f(n))  | Cota ajustada | El algoritmo es **exactamente del orden** de f(n) |

> Bassard & Bratley priorizan **la intuición visual y conceptual** sobre la formalidad matemática, a diferencia de Cormen.

---

## Ejemplo didáctico:

Supongamos que una operación dentro de un algoritmo se repite proporcionalmente a:

- n veces → **O(n)** (lineal)
- n² veces → **O(n²)** (cuadrático)
- log n veces → **O(log n)** (logarítmico)

### Ejemplo práctico:
> Ordenamiento por inserción: O(n²)  
> Merge Sort: O(n log n)

---
![semana 5](https://github.com/user-attachments/assets/e978e638-f786-483d-84a7-2a9f476e803e)



---

