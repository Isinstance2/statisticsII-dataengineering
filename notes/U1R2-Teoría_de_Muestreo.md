# Muestreo

El **muestreo** es una técnica de investigación que consiste en seleccionar un grupo de elementos (muestra) de una población con el objetivo de obtener información sobre ella sin necesidad de analizar todos sus elementos.

La idea principal es que la **muestra sea lo más representativa posible de la población**, de manera que las conclusiones obtenidas puedan inferirse con un nivel de confianza aceptable al resto de la población.

> **En Ingeniería de Datos**, el muestreo es una práctica muy común. Cuando trabajamos con millones de registros, analizar toda la información puede ser costoso en tiempo y recursos. Por ello, se utilizan muestras representativas para realizar análisis exploratorios, validar modelos o probar pipelines antes de ejecutarlos sobre el conjunto completo de datos.

---

# Espacio Muestral

El **espacio muestral** es el conjunto de todos los posibles resultados que pueden obtenerse al realizar un experimento aleatorio.

Por ejemplo, al lanzar un dado de seis caras:

```text
S = {1, 2, 3, 4, 5, 6}
```

Cada uno de esos valores representa un posible resultado del experimento.

---

# Tipos de Muestreo

Existen dos grandes categorías:

- Muestreo Probabilístico.
- Muestreo No Probabilístico.

---

# Muestreo No Probabilístico

En este tipo de muestreo, **no todos los elementos de la población tienen la misma probabilidad de ser seleccionados**.

La selección depende del criterio, experiencia o conveniencia del investigador, por lo que existe una mayor posibilidad de introducir sesgos.

Algunos ejemplos son:

- Muestreo por conveniencia.
- Muestreo por cuotas.
- Muestreo intencional.
- Muestreo por bola de nieve.

> Debido a que la selección no es completamente aleatoria, no siempre se puede garantizar que la muestra represente correctamente a toda la población.

---

# Muestreo Probabilístico

En el muestreo probabilístico, **todos los elementos de la población tienen una probabilidad conocida de ser seleccionados**.

Gracias a ello es posible aplicar métodos estadísticos para estimar el comportamiento de la población con un nivel de confianza determinado.

Algunos métodos probabilísticos son:

- Muestreo aleatorio simple.
- Muestreo sistemático.
- Muestreo estratificado.
- Muestreo por conglomerados.

> En proyectos de análisis de datos e Ingeniería de Datos, este tipo de muestreo suele ser el preferido cuando se busca obtener resultados representativos y minimizar el sesgo.

---

# Muestreo sin Reposición

En ocasiones, una vez que un elemento ha sido seleccionado para formar parte de la muestra, **ya no puede volver a ser seleccionado**.

A esto se le conoce como **muestreo sin reposición** (o sin reemplazo).

En este caso, cada elemento solo puede aparecer una vez dentro de la muestra.

## Ejemplo

Un laboratorio farmacéutico desea comprobar si un lote de pastillas de aspirina contiene la dosis correcta del principio activo.

Para ello:

1. Selecciona una pastilla.
2. La disuelve para realizar el análisis químico.
3. Obtiene los resultados.

Como la pastilla fue destruida durante el proceso, **no puede volver a formar parte de la población**.

Por ello, este es un ejemplo de **muestreo sin reposición**.

> Este tipo de muestreo es muy común cuando analizar una observación implica modificarla o eliminarla.

---

# Muestreo con Reposición

En el muestreo con reposición ocurre lo contrario.

Después de seleccionar un elemento, este **se devuelve nuevamente a la población** antes de realizar la siguiente selección.

Como consecuencia, **un mismo elemento puede ser seleccionado varias veces**.

## Ejemplo

Imaginemos una tómbola con **100 esferas numeradas**.

1. Se extrae una esfera y sale el número **42**.
2. Se registra el resultado.
3. La esfera **42** se devuelve nuevamente a la tómbola.
4. Se mezclan todas las esferas.
5. Se realiza una nueva extracción.

En la segunda extracción, el número **42** tiene exactamente la misma probabilidad de volver a salir que cualquier otro número.

Esto ocurre porque la población nunca cambia de tamaño: después de cada extracción, todos los elementos vuelven a estar disponibles.

> En simulaciones computacionales y técnicas como el **Bootstrap**, es muy común utilizar muestreo con reposición para generar múltiples muestras a partir de un mismo conjunto de datos.

---

# Aplicación en Ingeniería de Datos

En Ingeniería de Datos, el muestreo es una herramienta fundamental para trabajar de forma eficiente con grandes volúmenes de información.

Algunos ejemplos de su uso son:

- Realizar **Análisis Exploratorio de Datos (EDA)** sin procesar millones de registros.
- Validar la calidad de los datos antes de ejecutar un pipeline completo.
- Probar consultas SQL sobre una muestra antes de ejecutarlas en producción.
- Entrenar y evaluar modelos de Machine Learning utilizando conjuntos de entrenamiento y prueba.
- Reducir tiempos de procesamiento durante el desarrollo de soluciones de datos.

El objetivo es obtener información representativa reduciendo el costo computacional y el tiempo de procesamiento.
