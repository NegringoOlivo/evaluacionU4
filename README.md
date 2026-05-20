# 🚀 Evaluación Unidad 4: Organización de datos

### 💧 Ejercicio 1: Optimización de Riego por Sectores Agrícolas
> **Objetivo:** Combinar el recorrido de una matriz con la consulta de un vector para generar nuevos conjuntos de datos. 🚜

* 🌱 **Descripción:** Tienes una matriz `H` de `4x5` que representa el porcentaje de humedad actual en diferentes sectores de un campo. Las filas representan el tipo de cultivo (4 cultivos) y las columnas representan las parcelas (5 parcelas). Además, tienes un vector `R` de tamaño `4` que contiene el *porcentaje de humedad requerido* (ideal) para cada uno de los 4 cultivos.
* 🎯 **Tu Reto:**
    1. 🔍 **Cálculo de Déficit:** Compara la humedad actual de cada parcela (matriz `H`) con la humedad requerida para ese cultivo (vector `R`).
    2. 🛠️ **Nueva Matriz:** Genera una nueva matriz `D` de `4x5` que contenga únicamente el déficit de humedad (cuánto porcentaje falta para llegar al ideal). Si la parcela ya tiene la humedad ideal o la supera, el déficit debe ser `0`.
    3. 📊 **Vector de Consumo:** Crea un nuevo vector `C` de tamaño `4` que almacene la **suma total del déficit por fila** (esto representará la cantidad total de agua a inyectar en la línea de riego de cada cultivo).
    4. 🖥️ Imprime la matriz de déficit `D` y el vector de consumo `C` con un formato limpio.

---


### 📦 Ejercicio 2: Trazabilidad en la Cadena de Suministro (Registros)
> **Objetivo:** Diseñar un registro (Struct / Clase / Record) aplicando conceptos de protección de datos (Mutabilidad vs. Inmutabilidad). 🔒🔓

* 🏭 **Descripción:** En un sistema ERP, la información de un lote de producto no debe poder alterarse por completo una vez registrada. Algunos datos son inmutables (históricos/origen) y otros son mutables (estado actual).
* 🎯 **Tu Reto:**
    1. 🏗️ **Diseño del Registro:** Crea la estructura de datos para un `LoteAgroindustrial` que contenga las siguientes propiedades:
        * 🔒 **Inmutables (No pueden cambiar una vez creados):** `id_lote` (Ej. "L-2026-05"), `fecha_cosecha` (Ej. "20-May-2026"), `parcela_origen`.
        * 🔓 **Mutables (Pueden actualizarse):** `temperatura_actual` (Ej. 18.5), `estado_logistico` (Ej. "En Almacén", "En Tránsito", "Entregado").
    2. 🧪 **Simulación de Vida del Lote:**
        * Instancia (crea) un registro válido con datos iniciales.
        * Escribe el código para simular que el lote fue cargado a un camión: actualiza su `estado_logistico` a "En Tránsito" y su `temperatura_actual` a 22.0.
        * 🛑 **La Prueba de Fuego:** Agrega una línea de código donde intentes modificar deliberadamente el `id_lote` o la `fecha_cosecha`. Añade un comentario en tu código explicando por qué el lenguaje de programación arrojaría un error (o cómo implementarías la inmutabilidad si el lenguaje no la fuerza por defecto, por ejemplo usando `const`, tuplas, o getters sin setters).
    3. 🖨️ **Reporte:** Imprime el estado final del registro mostrando qué datos cambiaron y cuáles permanecieron intactos.

