# Semana 6: Análisis de las Estructuras de Control  
**Referencia: Brassard & Bratley, 2000 – Fundamentos de Algoritmia, sección 4.2 (págs. 111–117)**

---

## 🔸 4.2 Análisis de las Estructuras de Control

### 🎯 Objetivo del análisis
Evaluar el **tiempo de ejecución** de las estructuras de control básicas (secuencias, condicionales, bucles) como parte fundamental del análisis algorítmico.

---

## 🔹 Estructuras de Control y su Costo

### 1. **Secuencias**
- Si se ejecutan varias instrucciones una detrás de otra, el tiempo total es la **suma** de los tiempos individuales.
- Ejemplo:
  ```java
  a := b + c     // O(1)
  d := a * 2     // O(1)
  Total: O(1 + 1) = O(1)
### 2. **Condicionales (if-then-else)**

    El costo depende del camino tomado durante la ejecución.

    Se analiza usando el peor caso (generalmente).

    Ejemplo:
```java
    if (x > 0) then
      x := x - 1      // O(1)
    else
      x := x + 1      // O(1)

    ⏱ Total: máximo entre las ramas → O(1)
```
### 3. **Bucles (loops)**

    El análisis se basa en la cantidad de iteraciones.

    Se multiplican las operaciones del cuerpo por el número de veces que se ejecutan.

    Ejemplo:
```java
    for i := 1 to n do
      a := a + 1      // O(1)

    ⏱ Total: n × O(1) = O(n)
```
---
### **Observaciones clave:**

    El análisis no depende del lenguaje de programación, sino de la estructura lógica del algoritmo.
    Se prioriza el orden de crecimiento (ver Notación Asintótica en semanas anteriores).
    En estructuras anidadas, el análisis se realiza desde dentro hacia afuera.

---
### **Conclusión**

El análisis de estructuras de control permite:

    Estimar la complejidad algorítmica paso a paso.
    Prever cómo el algoritmo escalará con entradas más grandes.
    Fundar una base sólida para el análisis de algoritmos completos.
