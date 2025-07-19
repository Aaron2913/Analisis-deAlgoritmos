# 📚 Semana 14 – Algoritmos Probabilistas

**Referencia**:  
Brassard, G., & Bratley, P. (2006). *Fundamentals of Algorithmics*. Prentice Hall.

---

## 🎲 ¿Qué son los algoritmos probabilistas?

Un **algoritmo probabilista** es aquel que **usa números aleatorios** para tomar decisiones durante su ejecución. La salida o el rendimiento del algoritmo puede **variar entre ejecuciones**, incluso con la misma entrada.

Se utilizan especialmente cuando:
- No se conoce un algoritmo determinista eficiente.
- La solución aproximada o con alta probabilidad de éxito es aceptable.
- Se busca simplicidad o rapidez.

---

## 🧪 Tipos de algoritmos probabilistas

### 1. **Algoritmos de Monte Carlo**
- Devuelven una **respuesta probablemente correcta**, con un pequeño margen de error.
- Son rápidos, pero **no garantizan exactitud**.
- **Ejemplo**: Prueba de primalidad de Miller-Rabin.

```plaintext
P(correcta) ≥ 1 - ε
```
2. Algoritmos de Las Vegas
    Siempre devuelven la respuesta correcta, pero el tiempo de ejecución es aleatorio.
    La variabilidad está en el rendimiento, no en la corrección.
    Ejemplo: Randomized QuickSort.

P(error) = 0, pero tiempo es variable.

💡 Ejemplos clásicos

📍 Miller-Rabin (Monte Carlo)

    Prueba si un número es primo con alta probabilidad.
    Es ampliamente usado en criptografía.
    
📍 QuickSort aleatorizado (Las Vegas)

    Selecciona el pivote al azar para evitar el peor caso.
    Esperanza de tiempo: O(n log n)

📍 Algoritmo de Freivalds

    Verifica si A·B = C en matrices usando vectores aleatorios.
    Verificación rápida con alta probabilidad de certeza.

⏱️ Ventajas

    Frecuentemente más simples y rápidos que sus contrapartes deterministas.
    Muy útiles para problemas intratables o de gran tamaño.
    Permiten técnicas aproximadas en contextos donde la exactitud no es esencial.

⚠️ Desventajas

    No garantizan resultados exactos (en el caso Monte Carlo).
    Su análisis puede ser más complejo (requiere teoría de probabilidad).
    No siempre es fácil estimar el número de repeticiones necesarias para obtener una probabilidad aceptable.

📌 Aplicaciones comunes
    Criptografía (generación de claves, primalidad)
    Aprendizaje automático (inicialización, muestreo)
    Simulación de sistemas complejos (Monte Carlo)
    Verificación de propiedades algebraicas y numéricas
-----------------------------------------------------------------------------------
![Imagen de WhatsApp 2025-07-19 a las 16 06 23_7048da89](https://github.com/user-attachments/assets/8c828952-a415-4b50-92f1-8a05f2d1d457)
![Imagen de WhatsApp 2025-07-19 a las 16 06 24_61fda246](https://github.com/user-attachments/assets/a8d50483-9a64-49e6-b585-b96b19d8c595)
![Imagen de WhatsApp 2025-07-19 a las 16 06 24_9660f35f](https://github.com/user-attachments/assets/d5a000d9-8fa7-4b6e-bdbb-b09044c0179a)
![Imagen de WhatsApp 2025-07-19 a las 16 06 24_25c6468f](https://github.com/user-attachments/assets/2e758abd-1c9e-4eae-b8b6-6289583e40cc)
![Imagen de WhatsApp 2025-07-19 a las 16 06 24_f0ff2169](https://github.com/user-attachments/assets/75ab80b8-4dec-4050-9de5-4bb4b459a5a4)
![Imagen de WhatsApp 2025-07-19 a las 16 06 24_de394dae](https://github.com/user-attachments/assets/52ded238-88c7-48c4-b9e2-78297541fb6b)









