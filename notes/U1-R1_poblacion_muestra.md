# Unidad 1 - Población y Muestra

## 🎯 Objetivos de aprendizaje

Al finalizar esta unidad seré capaz de:

- Comprender la diferencia entre población y muestra.
- Identificar los distintos tipos de población.
- Comprender qué es una unidad de muestreo y un marco muestral.
- Explicar por qué el muestreo es una herramienta fundamental en Estadística.
- Relacionar estos conceptos con problemas reales de Ingeniería de Datos.

---

# Elemento

## Definición

Es el objeto o individuo sobre el cual se realizan las observaciones o mediciones.

## En mis palabras

Todo estudio estadístico comienza observando elementos individuales. Estos pueden ser personas, productos, clientes, transacciones, sensores o cualquier objeto de interés.

## 💻 Perspectiva de Ingeniería de Datos

En Ingeniería de Datos un elemento normalmente corresponde a **un registro (fila)** dentro de una base de datos.

### Ejemplos

- Un cliente.
- Una compra.
- Una factura.
- Un sensor IoT.
- Un evento registrado por una aplicación.

---

# Población

## Definición

Es el conjunto completo de elementos sobre el cual se desea obtener información o realizar inferencias.

## En mis palabras

La población representa el universo completo del estudio.

Idealmente se analizaría toda la población, pero en la mayoría de los casos esto resulta costoso, lento o simplemente imposible.

Por esta razón se utiliza una muestra.

## Tipos de población

### Población Diana

Es el grupo ideal al cual se desean aplicar los resultados del estudio.

### Población Base

Es el conjunto de elementos que cumplen las características necesarias para formar parte del estudio.

### Población Muestreada

Es la parte de la población que realmente puede ser seleccionada.

### Muestra Estudiada

Es el subconjunto cuyos datos fueron finalmente observados y analizados.

## 💻 Perspectiva de Ingeniería de Datos

En un proyecto de datos, la población normalmente corresponde al conjunto completo de registros almacenados.

### Ejemplos

| Empresa | Población |
|----------|-----------|
| Netflix | Todos los usuarios |
| Amazon | Todas las compras |
| Spotify | Todas las reproducciones |
| Uber | Todos los viajes |
| Banco | Todas las transacciones |

---

# Unidad de Muestreo

## Definición

Es cada uno de los elementos individuales que pueden ser seleccionados para formar parte de una muestra.

## 💻 Perspectiva de Ingeniería de Datos

Generalmente corresponde a una fila dentro de una tabla.

Ejemplo:

Cliente #10542

o

Pedido #845923

---

# Marco Muestral

## Definición

Es la lista, base de datos o conjunto de elementos disponibles desde donde realmente se seleccionará la muestra.

## En mis palabras

Es la fuente de datos que contiene todas las unidades de muestreo disponibles.

## 💻 Perspectiva de Ingeniería de Datos

El marco muestral puede ser:

- Una tabla SQL.
- Un archivo CSV.
- Un DataFrame de Pandas.
- Una tabla de BigQuery.
- Un Data Lake.
- Un Data Warehouse.

---

# ¿Por qué es importante el muestreo?

Muchas organizaciones generan millones o incluso miles de millones de registros diariamente.

Procesar toda esa información cada vez que se necesita hacer un análisis puede consumir mucho tiempo y recursos computacionales.

Por ello se utilizan muestras representativas que permiten obtener conclusiones confiables reduciendo significativamente el tiempo de procesamiento.

---

# 💡 Aplicación en Ingeniería de Datos

Imaginemos que trabajamos como Data Engineers en Spotify.

Spotify registra miles de millones de reproducciones diariamente.

Si un analista quiere estudiar el comportamiento de los usuarios, analizar todos los registros puede ser innecesario para una primera exploración.

En lugar de ello, se selecciona una muestra representativa.

Si esa muestra fue obtenida correctamente, permitirá estimar el comportamiento de toda la población utilizando muchos menos recursos computacionales.

Este mismo principio se aplica en empresas como Netflix, Amazon, Google y Uber para realizar análisis exploratorios, validar datos y probar modelos antes de ejecutarlos sobre grandes volúmenes de información.

---

# 🐍 Vista previa de la implementación en Python

En el notebook de esta unidad se desarrollará lo siguiente:

- Generar una población sintética de clientes.
- Extraer muestras aleatorias de distintos tamaños.
- Comparar la media poblacional con la media muestral.
- Visualizar cómo cambia la precisión conforme aumenta el tamaño de la muestra.
- Analizar por qué una muestra bien seleccionada puede representar adecuadamente a toda la población.

---

# 📌 Conclusiones

- La población representa el conjunto completo de elementos de interés.
- La muestra es un subconjunto de la población.
- Un buen muestreo permite obtener conclusiones confiables sobre toda la población.
- En Ingeniería de Datos, el muestreo es una herramienta esencial para trabajar de forma eficiente con grandes volúmenes de datos.
