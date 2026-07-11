# algoritmos-q1
Pseudocódigo y Algoritmos Q1 - Ingenieria en Sistemas - Universida Uk

## Contenido
- Unidad 1: Introducción a los algoritmos
- Unidad 2: Estructuras de decisión
- Unidad 3: Estructuras de ciclos (PARA, MIENTRAS, HACER-MIENTRAS)
- Unidad 4: Arreglos y matrices

## Herramientas
Pseudocódigo en español neutro, sin lenguaje de programación especifico.

## Autor
Luis Manuel Rodriguez Martinez - Q1 2026

# Evaluación Semana 2 - Algoritmos
## pseudocódigo Muestra el control de stock de una tienda Online

##ALGORITMO ControlStockProductos

VARIABLES
    N              : ENTERO
    i              : ENTERO
    stock          : ARREGLO[N] DE ENTERO
    stockTotal     : ENTERO
    valorValido    : ENTERO
    hayProductoCero: LOGICO
    posicionCero   : ENTERO
INICIO
 ESCRIBIR "Ingrese la cantidad de productos (N):"
 LEER N
 // --- Carga y Validación de arreglo ---

 PARA i ← 1 HASTA N HACER
        valorValido ← 0
        MIENTRAS valorValido = 0 HACER
            ESCRIBIR "Ingrese el stock del producto ", i, ": "
            LEER stock[i]
            SI stock[i] >= 0 ENTONCES
                valorValido ← 1
            SINO
                ESCRIBIR "Valor inválido. El stock no puede ser negativo."
            FIN SI
        FIN MIENTRAS
    FIN PARA
  
   // --- Inicialización de acumuladores ---
    stockTotal      ← 0
    hayProductoCero ← FALSO
    posicionCero    ← 0 
 
  //--- Recorrido del arreglo ---
  
  PARA i ← 1 HASTA N HACER
    stockTotal ← stockTotal + stock[i]
     SI stock[i] = 0 Y hayProductoCero = FALSO ENTONCES
            hayProductoCero ← VERDADERO
            posicionCero    ← i
        FIN SI
    FIN PARA

// --- resultados y calculos ---

ESCRIBIR "Stock total disponible:", stockTotal

SI hayProductoCero = VERDADERO ENTONCES
 ESCRIBIR "Se encontro un producto con stck 0 en la posicion:", posicionCero
SINO
 ESCRIBIR "No hay productos con stock 0"

 FIN

 ##Diagrama de flujo
 ![diagrama de flujo](diagrama-control-stock.png)
    
    
    

 
    
