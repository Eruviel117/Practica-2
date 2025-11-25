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
- **Hoja 1:** Imagen 1 - Matriz Original (30x30)
- **Hoja 2:** Imagen 2 - Matriz Original (30x30)
- **Hoja 3:** Imagen 3 - Matriz Original (30x30)
- **Hoja 4:** Imagen 4 - Matriz Original (30x30)
- **Hoja 5:** Imagen 5 - Matriz Original (30x30)

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


Dimensiones: 5 filas x 5 columnas




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



