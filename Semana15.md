# 📚 Semana 15 – Algoritmos Probabilistas (Parte 2)

**Referencia**:  
Brassard, G., & Bratley, P. (2006). *Fundamentals of Algorithmics*. Prentice Hall.

---

## 🎲 Profundización: Algoritmos probabilistas

Los **algoritmos probabilistas** introducen aleatoriedad como parte del proceso de cálculo. En esta semana se profundiza en su análisis, en el uso de funciones de probabilidad, errores controlados, repetición y estructuras matemáticas subyacentes.

---

## 🧠 Principios fundamentales

### 🔁 Repetición para aumentar la confianza
Los algoritmos Monte Carlo pueden repetirse múltiples veces para aumentar la **probabilidad de éxito**.

```plaintext
Probabilidad de éxito con k repeticiones:
P = 1 - (error por ejecución)^k
Ejemplo: si el error por ejecución es 1/4, tras 5 repeticiones:
P = 1 - (1/4)^5 ≈ 0.999
```
📐 Análisis probabilístico

Para evaluar un algoritmo probabilista se consideran:

    Esperanza matemática (esperado) del tiempo de ejecución.
    Varianza para medir fluctuaciones.
    Probabilidad de error y cómo se controla.
    Distribuciones discretas (uniforme, binomial) para modelar entradas o decisiones aleatorias.

🔎 Casos detallados
📍 Miller-Rabin – Prueba de primalidad

    Dado un número impar n > 3, se prueba si es primo con alta probabilidad.
    Requiere selección aleatoria de testigos.
    Puede identificar compuestos con probabilidad ≥ 3/4 por ejecución.

📍 Algoritmo de Freivalds – Verificación matricial

    Dado A, B, C, verifica si A·B = C en O(n²) tiempo.
    Genera un vector aleatorio r, compara A·(B·r) con C·r.
    Si los resultados difieren, garantiza que A·B ≠ C.

📍 QuickSort aleatorizado

    Selección aleatoria del pivote mejora el rendimiento promedio.
    Tiempo esperado: O(n log n) sin importar el orden de entrada.
