# Fundamentos de Algebra - Practica 1

## Información del Estudiante
- **Nombre:** Euruviel Márquez Martínez  
- **Matrícula:**  SW2509018
- **Grupo:** 1C 
- **Carrera:** TSW  
- **Cuatrimestre:** Primero  
- **Profesor:** Jorge Javier Pedrozo Romero  

##  Descripción del Proyecto

Este repositorio contiene mi solución a la práctica de **Fundamentos de Programación**, donde implemento funciones en JavaScript para resolver problemas de álgebra básica, preparándome para trabajar con operaciones matriciales más complejas.


## **Ejercicio 1: Determinante de una matriz 2×2**

Dada la matriz:

[ A = \begin{pmatrix} a & b \ c & d \end{pmatrix} ]
El determinante se calcula como:

[ \det(A) = ad - bc ]

---

## **Ejercicio 2: Suma, resta y multiplicación de matrices**

Dadas las matrices:
[
A = \begin{pmatrix} 2 & 1 \ 1 & 3 \end{pmatrix}, \quad
B = \begin{pmatrix} 1 & 2 \ 3 & 1 \end{pmatrix}
]

### **A + B**

Se suman elemento a elemento:
[
A + B = \begin{pmatrix} 3 & 3 \ 4 & 4 \end{pmatrix}
]

### **A − B**

[
A - B = \begin{pmatrix} 1 & -1 \ -2 & 2 \end{pmatrix}
]

### **Multiplicación AB**

[
AB = \begin{pmatrix}
(2)(1) + (1)(3) & (2)(2) + (1)(1) \
(1)(1) + (3)(3) & (1)(2) + (3)(1)
\end{pmatrix}
= \begin{pmatrix} 5 & 5 \ 10 & 5 \end{pmatrix}
]

---

## **Ejercicio 3: Determinante de AB, A y B**

### **Determinante de A**

[
\det(A) = (2)(3) - (1)(1) = 6 - 1 = 5
]

### **Determinante de B**

[
\det(B) = (1)(1) - (2)(3) = 1 - 6 = -5
]

### **Determinante de AB**

Usando la matriz calculada:
[
AB = \begin{pmatrix} 5 & 5 \ 10 & 5 \end{pmatrix}
]
[
\det(AB) = (5)(5) - (5)(10) = 25 - 50 = -25
]

### **Verificación de la propiedad**

[
\det(AB) = \det(A)\cdot\det(B)
]
[
-25 = (5)(-5)
]
✔ **Propiedad verificada**

---

---

## 📄 Licencia

Este proyecto es parte de las actividades académicas del **Tecnológico de Software** y está bajo la licencia MIT.

---

