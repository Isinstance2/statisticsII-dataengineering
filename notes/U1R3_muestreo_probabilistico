# Muestreo Aleatorio Simple

Es el método de muestreo probabilístico más sencillo. Consiste en seleccionar individuos directamente de la población de forma completamente aleatoria, garantizando que **todos tengan la misma probabilidad de ser elegidos**.

## Paso 1 - Numerar la población

Asigne un número único a cada uno de los individuos que forman parte de la población.

Ejemplo:

```text
1  → Ana
2  → Luis
3  → María
...
1000 → Carlos
```

---

## Paso 2 - Seleccionar la muestra aleatoriamente

Utilice un método de selección aleatoria como:

- Tómbolas.
- Tablas de números aleatorios.
- Generadores de números aleatorios.
- Software estadístico o Python (`random`, `numpy`, `pandas.sample()`).

Se seleccionan los individuos hasta completar el tamaño de muestra deseado.

---

## Limitación

Aunque es uno de los métodos más fáciles de comprender, **pierde practicidad cuando la población es muy grande**, ya que requiere disponer de una lista completa de todos los elementos.

> **En Ingeniería de Datos**, este tipo de muestreo es muy útil para obtener una muestra representativa de un dataset antes de realizar un análisis exploratorio o probar un algoritmo de Machine Learning.

---

# Muestreo Estratificado

Este método consiste en dividir primero la población en grupos llamados **estratos**, donde los individuos de cada grupo comparten características similares relacionadas con la variable que se desea estudiar.

El objetivo es garantizar que todos los grupos importantes de la población estén representados en la muestra.

## Fase I - Preparación

### Paso 1 - Estratificar la población

Se divide la población utilizando una característica relevante.

Algunos ejemplos:

- Sexo.
- Edad.
- Provincia.
- Nivel educativo.
- Rango salarial.

Cada estrato debe ser lo más homogéneo posible.

---

### Paso 2 - Asignar una cuota

Se determina cuántos individuos serán seleccionados de cada estrato.

---

### Paso 3 - Seleccionar los individuos

Dentro de cada estrato se aplica un método de muestreo probabilístico, generalmente un muestreo aleatorio simple.

---

## Fase II - Cálculo de cuotas

Dependiendo del objetivo del estudio existen dos formas de asignar las cuotas.

### Opción A - Asignación Proporcional

La muestra mantiene exactamente la misma distribución que la población.

**Ejemplo**

Si la población está compuesta por:

- 55 % mujeres
- 45 % hombres

La muestra deberá conservar esos mismos porcentajes.

---

### Opción B - Asignación Óptima

Se asignan más individuos a aquellos estratos que presentan mayor variabilidad.

Este método produce estimaciones más precisas, pero requiere conocer previamente el comportamiento estadístico de la población.

> **En Ingeniería de Datos**, este tipo de muestreo es útil cuando queremos asegurar que todas las categorías importantes de un dataset estén representadas, evitando que clases minoritarias desaparezcan durante el entrenamiento de modelos.

---

# Muestreo Sistemático

Este método selecciona individuos utilizando un intervalo fijo (**k**) dentro de una lista previamente ordenada.

La selección comienza desde un punto de inicio elegido aleatoriamente.

## Paso 1 - Definir las variables

- **N** → Tamaño de la población.
- **n** → Tamaño de la muestra.
- **k** → Intervalo de selección.

Se calcula mediante:

```text
k = N / n
```

---

## Paso 2 - Elegir el arranque aleatorio

Se selecciona un número al azar entre **1** y **k**.

Ese será el primer elemento de la muestra.

---

## Paso 3 - Aplicar el intervalo

A partir del primer elemento, se continúa seleccionando cada **k** posiciones.

**Ejemplo**

Si:

```text
N = 10000
n = 500

k = 20
```

y el inicio aleatorio es:

```text
8
```

La muestra será:

```text
8
28
48
68
88
108
...
```

hasta completar la muestra.

> **En Ingeniería de Datos**, este método es muy utilizado para obtener muestras rápidas de registros ordenados cronológicamente, como logs, transacciones o eventos de sensores.

---

# Muestreo por Estadios Múltiples (Multietápico)

Este método se utiliza cuando no se dispone de una lista completa de la población o cuando acceder directamente a todos los individuos resulta costoso o poco práctico.

En lugar de seleccionar directamente a los individuos, la población se divide en varios niveles jerárquicos y la selección se realiza por etapas.

Es como un embudo.

```text
País
│
├── Provincia
│
├── Municipio
│
├── Escuela
│
└── Profesor
```

No sería práctico recorrer todo un país buscando profesores directamente.

En su lugar:

1. Se seleccionan provincias.
2. Luego municipios.
3. Después escuelas.
4. Finalmente profesores.

Cada etapa puede utilizar cualquiera de los métodos probabilísticos vistos anteriormente.

> **En Ingeniería de Datos**, esta estrategia es similar a procesar datos jerárquicamente: primero seleccionar regiones, luego centros de datos, después servidores y finalmente los registros que serán analizados.

---

# Muestreo por Conglomerados

En este método la población ya se encuentra dividida de forma natural en grupos llamados **conglomerados**.

En lugar de seleccionar individuos, se seleccionan algunos conglomerados completos.

Posteriormente se estudian todos los elementos pertenecientes a esos conglomerados.

## Ejemplo

Supongamos que queremos estudiar profesores.

Las escuelas representan los conglomerados.

```text
Escuela A

• Profesor
• Profesor
• Profesor

--------------------

Escuela B

• Profesor
• Profesor
• Profesor
```

Si existen 100 escuelas y seleccionamos únicamente 10, se estudiarán todos los profesores pertenecientes a esas escuelas.

A diferencia del muestreo multietápico, normalmente **no es necesario seguir subdividiendo la población**.

> En algunos diseños puede seleccionarse únicamente una parte de los individuos de cada conglomerado. A este procedimiento se le conoce como **muestreo bietápico**.

> **En Ingeniería de Datos**, un conglomerado puede representar una sucursal, un centro de datos, una región o un servidor completo. En lugar de analizar toda la infraestructura, se seleccionan algunos conglomerados para reducir costos y tiempos de procesamiento.

---

# Comparación de los Métodos de Muestreo

| Método | ¿Cómo selecciona? | ¿Cuándo utilizarlo? | Ventajas | Desventajas |
|---------|-------------------|---------------------|----------|-------------|
| **Aleatorio Simple** | Selecciona individuos completamente al azar. | Cuando existe una lista completa de la población. | Fácil de entender e implementar. | Poco práctico en poblaciones muy grandes. |
| **Estratificado** | Divide la población en grupos homogéneos y toma una muestra de cada uno. | Cuando existen grupos importantes que deben estar representados. | Mayor precisión y representatividad. | Requiere conocer previamente la composición de la población. |
| **Sistemático** | Selecciona cada **k** elementos a partir de un inicio aleatorio. | Cuando la población ya está ordenada. | Muy rápido y sencillo. | Puede generar sesgos si existe un patrón en el orden de los datos. |
| **Conglomerados** | Selecciona grupos completos de individuos. | Cuando la población ya está agrupada naturalmente. | Reduce costos y facilita la recolección de datos. | Menor precisión si los conglomerados no representan bien a la población. |
| **Estadios Múltiples** | Realiza varias selecciones sucesivas (grupos, subgrupos e individuos). | Cuando la población es muy grande o difícil de acceder. | Muy eficiente para estudios nacionales o poblaciones distribuidas. | Su diseño y análisis estadístico son más complejos. |

---

# Relación con Ingeniería de Datos

En proyectos de Ingeniería de Datos es común trabajar con millones o incluso miles de millones de registros. Analizar toda la información no siempre es viable, por lo que el muestreo permite reducir el volumen de datos sin perder representatividad.

Algunas aplicaciones incluyen:

- Análisis Exploratorio de Datos (EDA).
- Validación de la calidad de datos.
- Pruebas de pipelines antes de ejecutarlos en producción.
- Entrenamiento y validación de modelos de Machine Learning.
- Reducción de costos computacionales y tiempos de procesamiento.
