# 📚 Semana 9 – Algoritmos Voraces

**Referencia**:  
Brassard, G., & Bratley, P. (2006). *Fundamentals of Algorithmics*. Prentice Hall.

---

## 🧠 ¿Qué es un algoritmo voraz?

Un **algoritmo voraz (greedy algorithm)** es una estrategia de diseño que construye una solución paso a paso, eligiendo en cada paso la opción **localmente óptima**, con la esperanza de alcanzar una **solución global óptima**.

> ⚠️ No todos los problemas se pueden resolver correctamente con algoritmos voraces, pero en algunos casos específicos, esta técnica garantiza una solución óptima.

---

## 🎯 Características clave

- ✅ Toma decisiones locales óptimas.
- 🔒 Las decisiones son irrevocables.
- ❌ No utiliza backtracking.
- ⚡ Alta eficiencia y simplicidad en implementación.

---

## ✅ Condiciones necesarias para aplicar el método voraz

1. **Subestructura óptima**: Una solución óptima del problema contiene soluciones óptimas de sus subproblemas.
2. **Propiedad de elección voraz**: Siempre existe una elección local óptima que conduce a una solución global óptima.

---

## 🧪 Ejemplos clásicos

### 1. Cambio de monedas
- Objetivo: Dar cambio con la menor cantidad de monedas.
- Solo funciona en sistemas monetarios bien diseñados (ej., no siempre funciona en monedas de {1, 3, 4}).

### 2. Problema de la mochila fraccionaria
- Se permiten fracciones de objetos.
- Estrategia: Tomar primero los objetos con mayor relación valor/peso.
- Garantiza solución óptima.

### 3. Árbol de expansión mínima
- **Algoritmos**: Kruskal y Prim.
- Conectan todos los nodos de un grafo con el menor costo.
- Ambos aplican el enfoque voraz.

### 4. Codificación de Huffman
- Codifica símbolos con frecuencias distintas usando árboles binarios.
- Los más frecuentes reciben códigos más cortos.
- Se basa en una estrategia voraz eficiente.

---

## 🛠️ Esquema general de un algoritmo voraz

```java
1. Inicializar una solución vacía.
2. Mientras no se haya construido una solución completa:
   a. Seleccionar el mejor candidato disponible.
   b. Verificar si puede formar parte de la solución.
   c. Añadir el candidato a la solución.
```

---------------------------------------------------------------------------------------------------------------------------------------------

![Semana9](https://github.com/user-attachments/assets/4d81eb19-4e21-4f65-b658-ec188117e4cc)
![semana91](https://github.com/user-attachments/assets/478592cf-32e2-4510-9586-3ebc71620fea)


