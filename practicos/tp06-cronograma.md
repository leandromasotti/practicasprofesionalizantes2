# TP6 — Cronograma: Gantt, PERT y camino crítico

> **Unidad:** [10 — Planificación temporal](../unidades/10-gantt-y-pert/)
> **Modalidad:** grupal, 3 a 4 integrantes
> **Entregable:** cronograma con red de tareas, cálculo PERT y diagrama de Gantt
> **Puntaje:** 100 puntos

---

## Objetivo

Construir el cronograma del proyecto, calcular el camino crítico y la holgura de cada tarea, y usar esos resultados para tomar decisiones de asignación.

---

## Consigna

### Parte A — Tabla de tareas

A partir de la descomposición del TP3 y la estimación del TP4, armen la tabla con un mínimo de **doce tareas**:

| Tarea | Descripción | Predecesoras | Duración |
|---|---|---|---|

La duración se expresa en días o semanas, no en persona-mes: es **duración**, no esfuerzo.

> Recuerden la distinción: un trabajo de 32 persona-mes no se hace en 1 mes con 32 personas.

### Parte B — Distribución del esfuerzo

Verifiquen que su cronograma distribuya el esfuerzo entre **todas** las etapas, no solo la construcción.

| Etapa | Referencia | El suyo |
|---|---|---|
| Análisis y requerimientos | 15 – 20 % | |
| Diseño | 15 – 20 % | |
| Construcción | 30 – 40 % | |
| Pruebas e integración | 20 – 30 % | |
| Entrega y capacitación | 5 – 10 % | |

Si su construcción supera el 50 %, revisen: probablemente falten tareas de las otras etapas.

### Parte C — Dependencias

Clasifiquen cada dependencia:

| Tipo | Descripción |
|---|---|
| **Obligatoria** | Impuesta por la naturaleza del trabajo |
| **De recurso** | La misma persona no puede hacer dos tareas a la vez |
| **Externa** | Depende de un tercero |

**Listen aparte todas las dependencias externas**, con responsable y fecha comprometida. Son las que más atrasos producen y las que menos se planifican.

### Parte D — Red de tareas

Dibujen la red. Se admite hecha a mano, en herramienta gráfica o en Mermaid.

### Parte E — Cálculo PERT

Completen la tabla con los cuatro tiempos y la holgura:

| Tarea | Pred. | Dur. | ES | EF | LS | LF | Holgura | Crítica |
|---|---|---|---|---|---|---|---|---|

**Muestren los dos recorridos:**

*Hacia adelante* — desde el inicio:
```
ES = el mayor EF de sus predecesoras   (0 si no tiene)
EF = ES + duración
```

*Hacia atrás* — desde el final:
```
LF = el menor LS de sus sucesoras   (duración del proyecto si no tiene)
LS = LF − duración
Holgura = LS − ES
```

### Parte F — Camino crítico

Identifiquen la secuencia de tareas con **holgura cero** y la duración del proyecto.

**Verificación obligatoria:** la suma de las duraciones del camino crítico debe coincidir con la duración total calculada. Si no coincide, hay un error en los recorridos.

Informen además:

- la suma de todas las duraciones;
- el ahorro obtenido por paralelismo.

### Parte G — Diagrama de Gantt

Construyan el Gantt **distinguiendo el camino crítico**.

Se valora que esté escrito en formato de texto versionable —Mermaid— en lugar de entregado como imagen.

### Parte H — Análisis y decisiones

Respondan, usando su propia tabla:

1. ¿Cuál es la tarea con **más holgura**? ¿Para qué la usarían?
2. ¿Cuál está **casi crítica** (holgura de 1 o 2)? ¿Qué riesgo implica?
3. Si tuvieran que **acortar el proyecto un 20 %**, ¿sobre qué tareas actuarían y por qué?
4. Si aceleraran una tarea con holgura, ¿qué efecto tendría en la fecha de entrega?
5. ¿Qué pasa con el camino crítico si su tarea casi crítica se atrasa tres días? Recalculen.

> La pregunta 5 es la que más se equivoca. El camino crítico **cambia** durante el proyecto, y por eso se recalcula en cada corte de control.

---

## Criterios de evaluación

| Criterio | Puntos |
|---|---|
| **Tabla de tareas** — doce mínimo, con predecesoras y duraciones | 10 |
| **Distribución del esfuerzo** verificada entre las cinco etapas | 10 |
| **Dependencias** clasificadas por tipo | 5 |
| **Dependencias externas** listadas con responsable y fecha | 10 |
| **Red de tareas** correcta y legible | 10 |
| **Recorrido hacia adelante** — ES y EF correctos, mostrados | 10 |
| **Recorrido hacia atrás** — LS y LF correctos, mostrados | 10 |
| **Holguras** calculadas correctamente | 5 |
| **Camino crítico** identificado, con la verificación de la suma | 10 |
| **Gantt** con el camino crítico distinguido | 10 |
| **Análisis** — cinco preguntas respondidas con la propia tabla | 10 |
| **Total** | **100** |

---

## Lo que baja la nota

| Situación | Descuento |
|---|---|
| Confundir esfuerzo con duración | −10 |
| Construcción por encima del 50 % del cronograma | −8 |
| No listar las dependencias externas | −10 |
| Recorridos sin mostrar el cálculo | −5 cada uno |
| Suma del camino crítico que no coincide con la duración total | −10 (error de cálculo) |
| Camino crítico con tareas de holgura distinta de cero | −10 |
| Proponer acortar el proyecto actuando sobre tareas con holgura | −8 |
| Gantt entregado como imagen sin el texto fuente | −5 |
| Gantt hecho sin el análisis PERT previo | −15 |

---

## Recomendaciones

- Empiecen por la red y después el Gantt. Un Gantt sin PERT previo es un dibujo lindo sin fundamento.
- En el recorrido hacia adelante se toma el **mayor** EF porque la tarea no puede empezar hasta que terminen **todas** sus predecesoras. En el de atrás se toma el **menor** LS porque debe terminar antes de que necesite empezar **la más urgente** de sus sucesoras.
- Verifiquen siempre la suma del camino crítico. Es el control más rápido de que los recorridos están bien.
- La holgura no es un margen para relajarse: es el recurso que permite reasignar gente cuando algo crítico se atrasa.
- Las dependencias externas son el punto ciego de casi todos los cronogramas. Si su proyecto depende de que la organización provea un dato, un acceso o una aprobación, eso es una tarea con responsable y fecha.
