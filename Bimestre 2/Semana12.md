# 📚 Semana 12 – Ordenación por Fusión (Merge Sort)

**Referencia**:  
Brassard, G., & Bratley, P. (2006). *Fundamentals of Algorithmics*. Prentice Hall.  
Cormen, T. H. et al. (2022). *Introduction to Algorithms*. 4ª edición. MIT Press.

---

## 🧠 ¿Qué es Merge Sort?

**Merge Sort** (Ordenación por fusión) es un algoritmo de ordenamiento basado en la técnica de **Divide y Vencerás**.  
Divide un arreglo en mitades, las ordena recursivamente y luego las combina (funde) en una única lista ordenada.

---

## 🔧 Esquema general (Divide y vencerás)

```plaintext
MergeSort(A):
    si longitud(A) ≤ 1:
        retornar A
    dividir A en dos mitades: izquierda y derecha
    izquierda_ordenada = MergeSort(izquierda)
    derecha_ordenada = MergeSort(derecha)
    retornar Merge(izquierda_ordenada, derecha_ordenada)
```
🛠️ Pseudocódigo
```plaintext
procedure MergeSort(A, inicio, fin):
    si inicio < fin:
        medio ← (inicio + fin) / 2
        MergeSort(A, inicio, medio)
        MergeSort(A, medio + 1, fin)
        Merge(A, inicio, medio, fin)

procedure Merge(A, inicio, medio, fin):
    n1 ← medio - inicio + 1
    n2 ← fin - medio
    crear arreglos temporales L[1...n1], R[1...n2]

    copiar A[inicio...medio] en L
    copiar A[medio+1...fin] en R

    i ← 1, j ← 1, k ← inicio
    mientras i ≤ n1 y j ≤ n2:
        si L[i] ≤ R[j]:
            A[k] ← L[i]
            i ← i + 1
        sino:
            A[k] ← R[j]
            j ← j + 1
        k ← k + 1

    copiar elementos restantes de L (si hay)
    copiar elementos restantes de R (si hay)
```
--------------------------------------------------------------------------------------------------------
![Imagen de WhatsApp 2025-07-19 a las 15 58 43_df2c73af](https://github.com/user-attachments/assets/43a718dc-b8d3-4c73-8a7a-39c79fad829c)
![Imagen de WhatsApp 2025-07-19 a las 15 58 44_964481e0](https://github.com/user-attachments/assets/4491c03d-6b28-43da-8b07-b18713497d33)


