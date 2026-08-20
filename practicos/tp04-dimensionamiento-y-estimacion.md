# TP4 — Dimensionamiento y estimación: puntos función y COCOMO

> **Unidades:** [7 — Métricas](../unidades/07-metricas/) · [8 — Estimación y modelos empíricos](../unidades/08-estimacion-y-cocomo/)
> **Modalidad:** grupal, 3 a 4 integrantes
> **Entregable:** informe técnico de dimensionamiento y estimación
> **Puntaje:** 100 puntos

---

## Objetivo

Dimensionar el sistema propuesto mediante **puntos función**, estimar su esfuerzo por dos métodos independientes —descomposición y **COCOMO**— y explicar la diferencia entre ambos resultados.

Es el práctico con mayor contenido de cálculo del año. Todos los cálculos deben mostrarse paso a paso.

---

## Consigna

### Parte A — Conteo del dominio de información

Identifiquen y **detallen** los cinco parámetros de su sistema. No alcanza con la cantidad: hay que listar cada elemento.

| Parámetro | Qué se cuenta |
|---|---|
| Entradas de usuario | Datos distintos que el usuario aporta |
| Salidas de usuario | Informes, pantallas y mensajes que produce |
| Consultas de usuario | Interacciones que devuelven respuesta sin actualizar datos |
| Archivos lógicos internos | Agrupamientos de datos que el sistema mantiene |
| Interfaces externas | Datos que se intercambian con otros sistemas |

### Parte B — Ponderación

Clasifiquen cada parámetro como **simple, medio o complejo** y justifiquen la clasificación en una línea.

| Parámetro | Simple | Medio | Complejo |
|---|---|---|---|
| Entradas de usuario | 3 | 4 | 6 |
| Salidas de usuario | 4 | 5 | 7 |
| Consultas de usuario | 3 | 4 | 6 |
| Archivos lógicos internos | 7 | 10 | 15 |
| Interfaces externas | 5 | 7 | 10 |

Calculen la **cuenta total** como suma de cuenta × peso.

### Parte C — Factores de complejidad

Valoren los **catorce factores** de 0 (sin influencia) a 5 (esencial), en una tabla.

Justifiquen los **tres que puntuaron más alto** y los **dos que puntuaron en cero**.

### Parte D — Puntos función

```
PF = cuenta total × [ 0,65 + 0,01 × Σ Fi ]
```

Muestren: la cuenta total, la sumatoria de Fi, el factor resultante y el PF final.

Verifiquen que el factor esté entre 0,65 y 1,35. Si no lo está, hay un error de cálculo.

### Parte E — Métricas derivadas

A partir de los PF, y declarando el valor de productividad que usan y de dónde lo tomaron:

| Indicador | Cálculo |
|---|---|
| Esfuerzo estimado | PF ÷ productividad (PF por persona-mes) |
| Costo | esfuerzo × costo del persona-mes |
| Costo por punto función | costo ÷ PF |
| Defectos esperados | PF × tasa de defectos por PF |

> Si no tienen histórico propio de productividad, usen un valor de referencia de la industria y **declaren explícitamente** que la estimación tiene mayor incertidumbre por ese motivo.

### Parte F — Estimación por descomposición

Recuperen la estimación de tres valores del TP3 y actualícenla con lo que aprendieron desde entonces.

Presenten el total en persona-mes, convirtiendo desde horas con el criterio que usen (y declarándolo).

### Parte G — COCOMO

**1. Tamaño.** Convertir PF a KLDC, declarando el factor de conversión y el lenguaje supuesto.

**2. Modo.** Elegir entre orgánico, semiacoplado o empotrado, **justificando** con las características del proyecto.

| Modo | Esfuerzo (persona-mes) | Duración (meses) |
|---|---|---|
| Orgánico | E = 2,4 × (KLDC)^1,05 | D = 2,5 × E^0,38 |
| Semiacoplado | E = 3,0 × (KLDC)^1,12 | D = 2,5 × E^0,35 |
| Empotrado | E = 3,6 × (KLDC)^1,20 | D = 2,5 × E^0,32 |

**3. Cálculo.** Esfuerzo, duración y cantidad de personas (E ÷ D), paso a paso.

**4. Comparación de modos.** Calculen los tres modos para su tamaño y presenten la tabla comparativa. Comenten qué cambia y qué no.

### Parte H — Contraste

Comparen el total por descomposición con el de COCOMO.

Si difieren en **más del 30 %**, expliquen a qué lo atribuyen. Opciones habituales: tareas olvidadas en la descomposición, modo mal elegido, factor de conversión PF→LDC inadecuado, productividad supuesta que no corresponde.

> Ninguna técnica se usa sola. Estimar por dos métodos y explicar la diferencia es la práctica profesional; que coincidan no es el objetivo.

### Parte I — Informe a la organización

Redacten el resultado como lo presentarían al referente:

- **en rango**, no como número único;
- en lenguaje no técnico;
- con los supuestos que lo sostienen declarados;
- indicando qué haría cambiar la estimación.

### Parte J — Métricas de seguimiento

Presenten el estado actual de las tres métricas definidas en el TP3, cada una **con su referencia**.

---

## Criterios de evaluación

| Criterio | Puntos |
|---|---|
| **Conteo detallado** — cinco parámetros con cada elemento listado | 15 |
| **Ponderación** justificada | 10 |
| **Catorce factores** valorados, con justificación de los extremos | 10 |
| **Cálculo de PF** correcto y mostrado paso a paso | 15 |
| **Métricas derivadas** con la productividad declarada y su fuente | 5 |
| **Estimación por descomposición** actualizada | 10 |
| **COCOMO** — modo justificado y cálculo correcto paso a paso | 15 |
| **Comparación de los tres modos** con su comentario | 5 |
| **Contraste** entre métodos, con explicación de la diferencia | 10 |
| **Informe a la organización** — en rango, con supuestos, en lenguaje adecuado | 5 |
| **Total** | **100** |

---

## Lo que baja la nota

| Situación | Descuento |
|---|---|
| Conteo sin detalle, solo cantidades | −10 |
| Factor de ajuste fuera del rango 0,65 – 1,35 | −10 (error de cálculo) |
| Cálculos presentados sin mostrar los pasos | −5 cada uno |
| Modo de COCOMO sin justificar | −8 |
| Usar productividad de la industria sin declararlo | −5 |
| Factor de conversión PF→LDC sin declarar el lenguaje | −5 |
| No contrastar los dos métodos | −10 |
| Presentar la estimación como número único a la organización | −5 |
| Confundir esfuerzo con duración | −5 |

---

## Recomendaciones

- El error de cálculo más común es olvidar que Σ Fi va de 0 a 70, con lo que el factor queda entre 0,65 y 1,35. Si les da 2,3, revisen.
- Al elegir el modo de COCOMO recuerden que es **la variable más sensible del cálculo**: el mismo tamaño cuesta más del doble en modo empotrado que en orgánico.
- Los exponentes son mayores que 1 en los tres modos. Eso significa que duplicar el tamaño más que duplica el esfuerzo, y es por qué agregar gente a un proyecto atrasado lo atrasa más.
- Si su descomposición da mucho menos que COCOMO, revisen primero las tareas no constructivas. Es la causa más frecuente.
- La honestidad de los supuestos se evalúa. Declarar "usamos productividad de referencia porque no tenemos histórico propio" suma; ocultarlo, resta.
