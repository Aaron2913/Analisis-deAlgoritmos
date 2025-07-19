# 📚 Semana 11 – Divide y Vencerás (Divide-and-Conquer)

**Referencias:**
- Brassard, G., & Bratley, P. (2006). *Fundamentals of Algorithmics*. Prentice Hall.
- Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2022). *Introduction to Algorithms*. 4.ª edición. MIT Press.

---

## 🧠 ¿Qué es Divide y vencerás?

**Divide y vencerás (Divide-and-Conquer)** es una técnica fundamental para el diseño de algoritmos. Su principio básico consiste en:

1. **Dividir**: Descomponer el problema en subproblemas más pequeños del mismo tipo.
2. **Vencer (Conquistar)**: Resolver los subproblemas de forma recursiva.
3. **Combinar**: Unir las soluciones de los subproblemas para formar la solución final.

> Esta técnica es ideal para problemas que tienen una estructura recursiva natural y permite reducir la complejidad comparado con enfoques iterativos o de fuerza bruta.

---

## 🔧 Esquema general

```plaintext
function DivideYVenceras(problema):
    si el problema es suficientemente pequeño entonces
        resolver directamente
    sino
        dividir el problema en subproblemas
        resolver recursivamente los subproblemas
        combinar las soluciones
```
📦 Ejemplos clásicos
📍 Ordenamiento por mezcla (Merge Sort)

    -Divide el arreglo en dos mitades.
    -Ordena recursivamente cada mitad.
    -Combina las mitades ordenadas.

Complejidad: O(n log n)
📍 Ordenamiento rápido (Quick Sort)

    -Selecciona un pivote.
    -Divide el arreglo en elementos menores y mayores que el pivote.
    -Ordena recursivamente los subconjuntos.

Complejidad promedio: O(n log n)
Peor caso: O(n²)
📍 Multiplicación rápida de enteros (Karatsuba)

    -Divide los números grandes en mitades.
    -Aplica tres multiplicaciones recursivas.
    -Combina con desplazamientos de base (potencias de 10).

Complejidad: O(n^log₂3) ≈ O(n^1.585)
📍 Búsqueda binaria

    -Divide el arreglo a la mitad.
    -Decide en qué mitad continuar la búsqueda.

Complejidad: O(log n)
⏱️ Análisis de complejidad

Muchos algoritmos de tipo divide y vencerás se expresan mediante relaciones de recurrencia. Ejemplo:

T(n) = 2T(n/2) + O(n)  ⟹  T(n) = O(n log n)

Se puede resolver usando:

    -Árboles de recurrencia
    -Master Theorem (Teorema maestro)

📘 Teorema Maestro (Cormen et al., 2022)

Se usa para resolver recurrencias de la forma:

T(n) = a·T(n/b) + f(n)

Donde:

    -a ≥ 1, número de subproblemas.
    -b > 1, factor de reducción de tamaño.
    -f(n), costo para dividir y combinar.
  -----------------------------------------------------------------
  ![Imagen de WhatsApp 2025-07-19 a las 15 53 23_afd778f7](https://github.com/user-attachments/assets/b5f088e1-ff74-4430-8cdc-266463f09bb7)

  ![Imagen de WhatsApp 2025-07-19 a las 15 53 24_9cf4f928](https://github.com/user-attachments/assets/3d7cd949-672e-47b3-ac17-ff94418df563)

