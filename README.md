# Fundamentos de Algebra

# Ejercicios de Álgebra Lineal — Determinantes y Aplicaciones

## Información del Estudiante
- **Nombre:** Euruviel Márquez Martínez  
- **Matrícula:**  SW2509018
- **Grupo:** 1C 
- **Carrera:** TSW  
- **Cuatrimestre:** Primero  
- **Profesor:** Jorge Javier Pedrozo Romero  



---

## Ejercicio 1: Determinantes 2×2

A continuación se calculan los determinantes de las siguientes matrices:

$$
\mathbf{A} =
\begin{pmatrix}
5 & 2 \\
3 & 1 \\
\end{pmatrix}
\qquad
\mathbf{B} =
\begin{pmatrix}
-1 & 4 \\
2 & -8 \\
\end{pmatrix}
\qquad
\mathbf{C} =
\begin{pmatrix}
6 & 9 \\
2 & 3 \\
\end{pmatrix}
\qquad
\mathbf{D} =
\begin{pmatrix}
0 & 5 \\
-5 & 0 \\
\end{pmatrix}
$$

## ✅ **Ejercicio 1.1 – Determinante de la matriz A**

### **Enunciado**

Calcular el determinante de:

$$ **A** =
\begin{pmatrix}
5 & 3 \\
2 & 1 \\
\end{pmatrix}
$$

### **Respuesta**

det(A)=-1


### **Procedimiento**

1. Multiplicar la diagonal principal:

   * (5 * 1 = 5)
2. Multiplicar la diagonal secundaria:

   * (2 * 3 = 6)
3. Aplicar la fórmula del determinante:

   * (5 - 6 = -1)

---

## ✅ **Ejercicio 1.2 – Determinante de la matriz B**

### **Enunciado**

$$ **B** =
\begin{pmatrix}
-1 & 4 \\
2 & -8 \\
\end{pmatrix}
$$

### **Respuesta**

det(B)=0


### **Procedimiento**

1. Diagonal principal:

   * ((-1)(-8)=8)
2. Diagonal secundaria:

   * (4 * 2 = 8)
3. Restar:

   * (8 - 8 = 0)


---

## ✅ **Ejercicio 1.3 – Determinante de la matriz C**

### **Enunciado**

$$ **C** =
\begin{pmatrix}
6 & 9 \\
2 & 3 \\
\end{pmatrix}
$$



### **Respuesta**

det(C)=0


### **Procedimiento**

1. Diagonal principal:

   * (6 * 3 = 18)
2. Diagonal secundaria:

   * (9 * 2 = 18)
3. Restar:

   * (18 - 18 = 0)

---

## ✅ **Ejercicio 1.4 – Determinante de la matriz D**

### **Enunciado**

$$ **D** =
\begin{pmatrix}
0 & 5 \\
-5 & 0 \\
\end{pmatrix}
$$

### **Respuesta**

det(D)=25


### **Procedimiento**

1. Diagonal principal:

   * (0  * 0 = 0)
2. Diagonal secundaria:

   * (5  (-5) = -25)
3. Restar:

   * (0 - (-25) = 25)





---

## Ejercicio 2: Regla de Sarrus (3×3)

Calcular los determinantes usando la **Regla de Sarrus** para las matrices:

$$
\mathbf{E} =
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 4 \\
5 & 6 & 0 \\
\end{pmatrix}
\qquad
\mathbf{F} =
\begin{pmatrix}
2 & -1 & 3 \\
1 & 4 & 0 \\
3 & 2 & -2 \\
\end{pmatrix}
$$



### Ejercicio 2.1 — Matriz **E** (Sarrus)

#### Procedimiento Sarrus
Escribir las dos primeras columnas a la derecha y multiplicar las diagonales:

Diagonales positivas:
- (1 * 1 * 0 = 0)
- (2 * 4 * 5 = 40)
- (3 * 0 * 6 = 0)  
Suma positivas = (0 + 40 + 0 = 40)

Diagonales negativas:
- (3 * 1 * 5 = 15)
- (1 * 4 * 6 = 24)
- (2 * 0 * 0 = 0)  
Suma negativas = \(15 + 24 + 0 = 39\)

Resultado:

det E = 40 - 39 = 1


---

### Ejercicio 2.2 — Matriz **F** (Sarrus)

#### Procedimiento Sarrus
Diagonales positivas:
- (2 * 4 * (-2) = -16)
- ((-1) * 0 * 3 = 0)
- (3 * 1 * 2 = 6)  
Suma positivas = (-16 + 0 + 6 = -10)

Diagonales negativas:
- (3 * 4 * 3 = 36)
- (2 * 0 * 2 = 0\)
- ((-1) * 1 * (-2) = 2)  
Suma negativas = (36 + 0 + 2 = 38)

Resultado:

det F = (-10) - 38 = -48

---

## Ejercicio 3: Método de cofactores (3×3)

Calcular por expansión de cofactores:

$$
\mathbf{G} =
\begin{pmatrix}
1 & 0 & 2 \\
-1 & 3 & 1 \\
2 & 0 & 1 \\
\end{pmatrix}
$$

### **Respuesta**

**det(G) = 9**

### **Procedimiento (Cofactores)**


1. sacamos las matrices de deaca elemento :

2. primer matrices 

$$ **1** =
\begin{pmatrix}
3 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

det= 3

3. Segunda matrices 

$$ **-0** =
\begin{pmatrix}
-1 & 1 \\
2 & 1 \\
\end{pmatrix}
$$

det = 0


4. Tercer matriz 


$$ **2** =
\begin{pmatrix}
-1 & 3 \\
2 & 1 \\
\end{pmatrix}
$$

det = -12 

5. Determinante el determinante total :

det = 3 + 0 + (-12)


Resultado final:
**det(G) = 9**


---

## Ejercicio 4: Verificar propiedades del determinante

Dadas las matrices:

$$
\mathbf{A} =
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix}
\qquad
\mathbf{B} =
\begin{pmatrix}
1 & 2 \\
3 & 1 \\
\end{pmatrix}
$$

Se verifican:

* det(AB) = det(A) × det(B)
* det(Aᵀ) = det(A)

### **Cálculos**

1. det(A) = (2·3) − (1·1) = 5
2. det(B) = (1·1) − (2·3) = -5
3. Producto AB =

```
[  5   5 ]
[ 10   5 ]
```

4. det(AB) = (5·5) − (5·10) = -25

### **Verificación**

* det(A)·det(B) = 5 × (-5) = -25 ✓
* Aᵀ = A → det(Aᵀ) = 5 = det(A) ✓


---

## Ejercicio 5: Aplicación geométrica (área)

Datos:
u = (3, 2)
v = (1, 4)

Se forma la matriz cuyas columnas son los vectores:


$$ **M** =
\begin{pmatrix}
3 & 2 \\
1 & 4 \\
\end{pmatrix}
$$

### **a) Área del paralelogramo**

```
det(M) = (3·4) − (1·2) = 12 − 2 = **10**
```

\Área = |10| = **10 unidades²**

### **b) ¿Cambia el área si se intercambian los vectores?**


$$ **M'** =
\begin{pmatrix}
1 & 4 \\
3 & 2 \\
\end{pmatrix}
$$


det(M') = (1·2) − (3·4) = 2 − 12 = -10

\Área = |−10| = **10** (no cambia)

### **c) Signo del determinante**

* Positivo → orientación antihoraria
* Negativo → orientación horaria

El signo afecta la orientación, **no el área**.

El área siempre se toma como el valor absoluto del determinante.

---

## Conclusión general
- Se aplicaron técnicas fundamentales: fórmula 2×2, Regla de Sarrus (3×3) y expansión por cofactores.  
- Verificamos propiedades algebraicas (multiplicativa y transposición).  
- Vimos la conexión geométrica del determinante con el área y la orientación.

---


