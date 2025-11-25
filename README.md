# Manipulación de Imágenes con Operaciones Matriciales en Excel

## Información del Estudiante
- **Nombre:** Euruviel Márquez Martínez  
- **Matrícula:**  SW2509018
- **Grupo:** 1C 
- **Carrera:** TSW  
- **Cuatrimestre:** Primero  
- **Profesor:** Jorge Javier Pedrozo Romero  

##  Descripción del Proyecto

Este README documenta las matrices contenidas en el archivo algebra  y los pasos para reproducir dibujo con las matrices 



---


## Estructura del Archivo

El archivo contiene **14 hojas de cálculo** organizadas de la siguiente manera:


###  Hojas Base (10 hojas)

#### Matrices Originales (5 hojas)
- **Hoja 1:** Jefe maestro 1 - Matriz Original (30x30)
- **Hoja 2:** Spiderma - Matriz Original (30x30)
- **Hoja 3:** gato - Matriz Original (30x30)
- **Hoja 4:** koala- Matriz Original (30x30)
- **Hoja 5:** ballena - Matriz Original (30x30)

Cada matriz contiene valores numéricos entre 0 y 1 que representan un dibujo tipo pixel art con escala de grises:
- **Valor 1:** La celda se colorea de negro (píxel completamente activo)
- **Valor 0:** La celda se colorea de blanco (píxel inactivo)
- **Valores intermedios (0.2, 0.5, 0.7, etc.):** La celda se colorea en tonos de gris

- 
##Matrices 

Hoja: JEFE MAESTRO

Dimensiones: 10 filas x 5 columnas
```txt
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z AA AB AC AD
 1   . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
 2   . . . 1 1 1 1 1 1 1 1 1 1 . . . . . . . . . . . . . . . . .
 3   . . 1 1 1 1 1 1 1 1 1 1 1 1 . . . . . . . . . . . . . . . .
 4   . 1 1 1 1 1 1 1 1 1 1 1 1 1 1 . . . . . . . . . . . . . . .
 5   1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 . . . . . . . . . . . . . .
 6   1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 . . . . . . . . . . . . . .
 7   1 1 1 0 0 0 1 1 0 0 0 1 1 1 1 . . . . . . . . . . . . . . .
 8   1 1 1 0 0 0 1 1 0 0 0 1 1 1 1 . . . . . . . . . . . . . . .
 9   1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 . . . . . . . . . . . . . . .
10   1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 . . . . . . . . . . . . . . .
11   1 1 0 0 1 1 1 1 1 1 0 0 1 1 . . . . . . . . . . . . . . . .
12   1 1 1 0 0 0 0 0 0 0 0 0 1 1 1 . . . . . . . . . . . . . . .
13   . 1 1 1 0 0 0 0 0 0 0 0 1 1 1 . . . . . . . . . . . . . . .
14   . 1 1 1 1 1 1 1 1 1 1 1 1 . . . . . . . . . . . . . . . . .
15   . . 1 1 1 1 1 1 1 1 1 1 . . . . . . . . . . . . . . . . . .
16   . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
17   . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
```


Hoja: Spideman

Dimensiones: 8 filas x 4 columnas

```txt
0   0   0   1   1   1   1   1   0   0   0   0   0   0
0   0   1   0.5 0.5 0.5 0.5 0.5 1   0   0   0   0   0
0   1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 1   0   0   0   0
0   1   1   0.5 0.5 0.5 0.5 0.5 1   1   0   0   0   0
0   1   0   1   0.5 0.5 0.5 1   0   1   0   0   0   0
0   1   0   0   1   0.5 1   0   0   1   0   0   0   0
0   1   0   0   1   0.5 1   0   0   1   0   0   0   0
0   0   1   1   0.5 0.5 0.5 1   1   0   0   0   0   0
0   1   0.5 1   1   1   1   1   0.5 1   0   0   0   0
1   0.5 0.8 0.5 0.5 1   0.5 0.5 0.8 0.5 1   0   0   0
1   0.5 1   0.5 1   0.5 1   0.5 1   0.5 1   0   0   0
0   1   1   0.8 0.5 0.5 0.5 0.8 1   1   0   0   0   0
0   0   1   0.8 0.8 0.8 0.8 0.8 1   0   0   0   0   0
0   0   1   0.5 0.5 1   0.5 0.5 1   0   0   0   0   0
0   0   0   1   1   0   1   1   0   0   0   0   0   0

```
---

Hoja: Gato

Dimensiones: 12 filas x 3 columnas
```txt

0   0   0   0   0   0   0   0   0   0   0   0   0    0    0    0   0
0   0   1   1   1   0   0   0   0   0   1   1   1    0    0    0   0
0   0   1   0.3 0.3 1   0   0   0   1   0.8 0.8 1    0    0    0   0
0   0   1   0.3 0.3 0.3 1   1   1   0.8 0.8 0.8 1    0    0    0   0
0   0   1   0.3 0.3 0.3 0   0   0.8 0.8 0.8 0.8 1    0    0    0   0
0   1   0.3 0.3 0.3 0.3 0   0   0.8 0.8 0.8 0.8 0.8  1    0    0   0
0   1   0.3 0.3 1   0   0   0   0.8 0.8 1   0.8 0.8  1    0    0   0
0   1   0.3 0   1   0   0   0   0.8 0.8 1   0.8 0.8  1    0    0   0
0   1   0   0   0   0   1   0   0.8 0.8 0.8 0.8 1    0    0    0   0
0   0   1   1   0   0   0   0   0   0   0   1   1    0    0    0   0
0   0   0   0   1   0   0   0   0   0   1   0   0    0    0    0   0
0   0   0   0   1   0   0   0   0.2 0.2 1   0   0    0    1    0   0
0   0   0   0   1   0.8 0   0   0.2 0.2 1   0   0    1    0    1   0
0   0   0   1   0.8 0.8 0   0   0.2 0.2 0.2 1   0    1    0    1   0
0   0   0   1   0.8 0.8 1   0   1   0.2 0.2 1   1    0.8  0.8  1   0
0   0   0   1   0.8 0.8 1   0   1   0.2 0.2 1   0.2  0.8  1    0   0
0   0   0   0   11  11  11  11  11  11  11  11  11   11   0    0   0
0   0   0   0   0   0   0   0   0   0   0   0   0    0    0    0   0
```

---

Hoja: koala

Dimensiones: 6 filas x 6 columnas
```txt

0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
0   0   0   0.8 0.8 0.8 0   0.8 0.8 0.8 0.8 0.8 0.8 0.8 0   0.8 0.8 0.8 0   0   0
0   0   0.8 0.3 0.3 0.3 0.8 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.8 0.3 0.3 0.3 0.8 0   0
0   0.8 0.3 0.3 0.3 0.8 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.8 0.3 0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.8 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.8 0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.8 0.3 0.3 0.3 0.3 0.3 1   0.3 0.3 0.3 0.3 0.3 0.8 0.3 0.3 0.8 0
0   0   0.8 0.8 0.3 0.3 1   0.3 0.3 1   1   1   0.3 0.3 1   0.3 0.3 0.8 0.8 0   0
0   0   0   0.8 0.3 0.3 1   0.3 0.3 1   1   1   0.3 0.3 1   0.3 0.3 0.8 0   0   0
0   0   0   0.8 0.3 0.3 0.3 0.3 0.3 1   1   1   0.3 0.3 0.3 0.3 0.3 0.8 0   0   0
0   0   0   0.8 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.8 0   0   0
0   0   0   0   0.8 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0.8 0   0   0   0
0   0   0   0   0   0.8 0.8 0.8 0.8 0.8 0.8 0.8 0.8 0.8 0.8 0.8 0   0   0   0   0
0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
```


---
Hoja: Ballena
Dimensiones: 5 filas x 5 columnas
```txt

0   0   0   0   0   0   0   0   0   0   0   0   0   0   0.5 0   0.5 0   0   0   0   0
0   0   0   0   0   0   0   0   0   0   0   0   0   0.5 0   0.5 0   0.5 0   0   0   0
0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0.5 0   0   0   0   0   0
0   0   0   0   0   0   0   0   0   0   0   0   1   1   1   1   1   1   1   0   0   0
0   0   0   0   0   0   0   0   0   0   1   1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 1   0   0
0   0   0   0   0   0   0   0   0   1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 1   0
0   1   1   0   1   1   0   0   1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 1   0
0   1   0.5 1   0.5 1   0   0   1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 0   0   0.5 0.5 1   0
0   1   0.5 0.5 0.5 1   0   0   1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 0   1   0.5 0.5 1   0
0   0   1   0.5 1   0   0   1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 0.5 1   0
0   0   1   0.5 0.5 1   1   0.5 0.5 0.5 0.5 0.5 0.5 0   0   0   0   0   0   0   1   0
0   0   0   1   0.5 0.5 0.5 0.5 0.5 0   0   0   0   0   0   0   0   0   0   1   0   0
0   0   0   0   1   1   1   1   1   1   11  1   0   1   1   0   0   1   1   0   0   0
0   0   0   0   0   0   0   0   0   0   0   1   1   0   0   1   1   0   0   0   0   0
0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
```

#### Matrices Trasnpuesta (5 hojas)
- **Hoja 1:** Jefe maestro 1 - Matriz Original (30x30)
- **Hoja 2:** Spiderma - Matriz Original (30x30)
- **Hoja 3:** gato - Matriz Original (30x30)
- **Hoja 4:** koala- Matriz Original (30x30)
- **Hoja 5:** ballena - Matriz Original (30x30)

```txt

0 0 0 0 1 1 1 1 1 1 1 1 0 0 0 0 0
0 0 0 1 1 1 1 1 1 1 1 1 1 1 0 0 0
0 0 1 1 1 1 1 1 1 1 0 1 1 1 1 0 0
0 1 1 1 1 1 0 0 1 1 0 0 1 1 1 0 0
0 1 1 1 1 1 0 0 1 1 1 0 0 1 1 0 0
0 1 1 1 1 1 0 0 1 1 1 0 0 1 1 0 0
0 1 1 1 1 1 1 1 1 1 1 0 0 1 1 0 0
0 1 1 1 1 1 1 1 1 1 1 0 0 1 1 0 0
0 1 1 1 1 1 0 0 1 1 0 0 0 1 1 0 0
0 1 1 1 1 1 0 0 1 1 0 0 0 1 1 0 0
0 1 1 1 1 1 0 0 1 1 0 0 0 1 1 0 0
0 1 1 1 1 1 1 1 1 1 0 0 0 1 1 0 0
0 1 1 1 1 1 1 1 1 1 1 1 1 1 0 0 0
0 0 1 1 1 1 1 1 1 1 0 1 1 1 0 0 0
0 0 0 1 1 1 1 1 1 1 1 1 0 0 0 0 0
0 0 0 0 1 1 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
...
```


```txt


0   0   0   0   0   0   0   0   0   1   1   0   0   0   0
0   0   1   1   1   1   1   0   1   0.5 0.5 1   0   0   0
0   1   0.5 1   0   0   0   1   0.5 0.8 1   1   1   1   0
1   0.5 0.5 0.5 1   0   0   1   1   0.5 0.5 0.8 0.8 0.5 1
1   0.5 0.5 0.5 0.5 1   1   0.5 1   0.5 1   0.5 0.8 0.5 1
1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 1   1   0.5 0.5 0.8 1   0
1   0.5 0.5 0.5 0.5 1   1   0.5 1   0.5 1   0.5 0.8 0.5 1
1   0.5 0.5 0.5 1   0   0   1   1   0.5 0.5 0.8 0.8 0.5 1
0   1   0.5 1   0   0   0   1   0.5 0.8 1   1   1   1   0
0   0   1   1   1   1   1   0   1   0.5 0.5 1   0   0   0
0   0   0   0   0   0   0   0   0   1   1   0   0   0   0
0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
```


```txt
0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
0   0   0   0   0   1   1   1   1   0   0   0   0   0   0   0   0   0
0   1   1   1   1   0.3 0.3 0.3 0   1   0   0   0   0   0   0   0   0
0   1   0.3 0.3 0.3 0.3 0.3 0   0   1   0   0   0   1   1   1   0   0
0   1   0.3 0.3 0.3 0.3 1   1   1   0   1   1   1   0.8 0.8 0.8 11  0
0   0   1   1   1   0   0   0   0   0   0   0   0   0.8 0.8 0.8 11  0
0   0   0   1   0   0   0   0   1   0   0   0   0   0   1   1   11  0
0   0   0   1   0   0.8 0   0   0   0   0   0   0   0.2 0.2 0.2 11  0
0   0   0   1   0   0.8 0   0.8 0.8 0   0   0.2 0.2 0.2 0.2 1   11  0
0   0   1   0.8 0.8 0.8 0.8 0.8 0.8 0   0   0.2 0.2 0.2 0.2 1   11  0
0   1   0.8 0.8 0.8 0.8 1   1   0.8 0   1   1   1   0.2 0.2 0.2 11  0
0   1   1   1   0.8 0.8 0.8 0.8 0.8 1   0   0.8 0.8 1   1   1   11  0
1   0.8 1   1   1   0.8 0.8 0.8 1   1   0   0.8 0.8 1   1   1   11  0
1   0.8 0.8 1   1   0.8 1   1   1   0   0   0.2 0.2 1   1   1   11  0
1   0.8 0.8 1   1   0.8 0.8 0.2 0.2 0.2 0.2 1   1   1   1   1   11  0
1   0.8 0.8 1   1   0.8 0.8 0.2 0.2 0.2 0.2 1   1   1   1   1   11  0
0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0   0



```



```txt
0   0   0   0   0   0   0   0   0   0   0   0   0
0   0   0   0.8 0.8 0.8 0   0   0   0   0   0   0
0   0   0.8 0.3 0.3 0.3 0.8 0.8 0   0   0   0   0
0   0.8 0.3 0.3 0.3 0.8 0.3 0.8 0.8 0.8 0.8 0.8 0
0   0.8 0.3 0.8 0.3 0.3 0.3 0.3 0.3 0.3 0.8 0   0
0   0.8 0.3 0.8 0.3 0.3 0.3 0.3 0.3 0.3 0.3 0   0
0   0.8 0.3 0.3 0.3 1   1   1   1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 0.3 0.3 0.3 1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 0.3 0.3 0.3 1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 1   1   1   1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 1   1   1   1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 1   1   1   1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 0.3 0.3 0.3 1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 0.3 0.3 0.3 1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 0.3 0.3 0.3 1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 0.3 0.3 0.3 1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 0.3 0.3 0.3 1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 0.3 0.3 0.3 1   0.3 0.3 0.8 0
0   0.8 0.3 0.3 0.3 0.3 0.3 0.8 0   0   0   0   0
0   0   0.8 0.8 0.8 0.8 0.8 0.8 0   0   0   0   0
0   0   0   0   0   0   0   0   0   0   0   0   0



```





```txt
0   0   0   0   0   0   0   0   0   0   0   0   0   0   0
0   0   0   0   0   0   1   1   1   0   0   0   0   0   0
0   0   0   0   0   0   1   0.5 0.5 1   1   0   0   0   0
0   0   0   0   0   0   0   1   0.5 0.5 0.5 1   0.5 0   0
0   0   0   0   0   0   1   0.5 0.5 1   0.5 0.5 1   0   0
0   0   0   0   0   0   1   1   1   0   1   1   0   0   0
0   0   0   0   0   0   0   0   0   0   1   1   1   0   0
0   0   0   0   0   0   0   0   0   1   1   0   1   0   0
0   0   0   0   1   1   1   1   1   0.5 0.5 0   1   0   0
0   0   0   0   1   0   0   0   0   0.5 0.5 0   1   0   0
0   0   0   0   0.5 0.5 0.5 0.5 0.5 0.5 0.5 0   11  0   0
0   0   0   0   0.5 0.5 0.5 0.5 0.5 0.5 0.5 0   1   1   0
0   0   0   1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 0   0   0   0
0   0.5 0   1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 0   1   0   0
0.5 0.5 0.5 1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 0   1   0   0
0   0   0.5 1   0.5 0.5 0.5 0   0   0.5 0.5 0   0   1   0
0.5 0.5 0.5 1   0.5 0.5 0.5 0   1   0.5 0.5 0   0   1   0
0   0.5 0   1   0.5 0.5 0.5 0   1   0.5 0.5 0   1   0   0
0   0   0   1   0.5 0.5 0.5 0.5 0.5 0.5 0.5 0   1   0   0
0   0   0   0   1   1   1   1   1   1   0   1   0   0   0
0   0   0   0   0   1   1   1   1   1   1   0   0   0   0
0   0   0   0   0   0   0   0   0   0   0   0   0   0   0



```




# 1. Hoja: Multiplicación Escalar (Imagen × Escalar)
La **multiplicación escalar** consiste en multiplicar todos los valores de la matriz por un número constante, por ejemplo, aumentar o disminuir la intensidad de los colores.

Supongamos que tu matriz original está en el rango **A1:N20** y el escalar está en la celda **P1**.

1. En una hoja nueva, selecciona un rango con las mismas dimensiones que la matriz.
2. En la primera celda (por ejemplo, **A1**), escribe:

```
=A1 * $P$1
```

3. Arrastra la fórmula hacia la derecha y hacia abajo.



INSERTAR IMAGEN 





# 🟩 2. Hoja: Suma de Matrices (Imagen A + Imagen B)
Esta operación combina dos imágenes pixeladas sumando sus valores numéricos.

## ✔️ Requisitos
- Ambas matrices deben tener **las mismas dimensiones**.

## ✔️ Fórmula
Si la primera imagen está en la hoja A en **A1:N20** y la segunda en la hoja B en el mismo rango:

En la nueva hoja, en la celda **A1** escribe:

```
=HojaA!A1 + HojaB!A1
```

Arrastra hacia toda la matriz.


INSERTAR IMAGEN 







#  3. Hoja: Resta de Matrices (Imagen A − Imagen B)
La resta permite comparar o extraer diferencias entre dos imágenes.

## ✔️ Fórmula
En la celda **A1** de la hoja correspondiente escribe:

```
=HojaA!A1 - HojaB!A1
```

Luego arrastra en toda la matriz.




INSERTAR IMAGEN 




# 🟨 4. Hoja: Composición de Matrices (c₁A + c₂B)
La composición mezcla dos imágenes mediante la suma ponderada de cada una con un escalar.

## ✔️ Preparación
Coloca:
- El escalar **c₁** en la celda **P1**
- El escalar **c₂** en la celda **Q1**

## ✔️ Fórmula general
Si la matriz A está en HojaA!A1:N20 y la matriz B en HojaB!A1:N20, en la nueva hoja escribe en **A1**:

```
=HojaA!A1 * $P$1 + HojaB!A1 * $Q$1
```

Arrastra para llenar toda la matriz.

---















## Técnica de Formato Condicional

Para replicar el efecto visual del pixel art con escala de grises en nuevas hojas:

### Opción 1: Formato Condicional con Escala de Color

1. Selecciona el rango de 30×30 (por ejemplo, A1:AD30)
2. Ve a Inicio > Formato condicional > Escalas de color
3. Selecciona una escala de 3 colores:
   - Valor mínimo (0): Blanco
   - Punto medio (0.5): Gris
   - Valor máximo (1): Negro
4. Excel aplicará automáticamente todos los tonos intermedios


---

## Autor
Euruviel Marquez Martinez 



