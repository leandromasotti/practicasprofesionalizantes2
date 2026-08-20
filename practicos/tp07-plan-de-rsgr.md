# TP7 — Plan de RSGR y matriz de riesgos

> **Unidad:** [12 — Gestión del riesgo](../unidades/12-riesgo-y-rsgr/)
> **Modalidad:** grupal, 3 a 4 integrantes
> **Entregable:** matriz de riesgos y plan de RSGR
> **Puntaje:** 100 puntos

---

## Objetivo

Identificar y proyectar los riesgos del proyecto, y elaborar el plan de Reducción, Supervisión y Gestión del Riesgo de los más expuestos.

---

## Consigna

### Parte A — Identificación

Identifiquen un mínimo de **ocho riesgos**, con **al menos dos por categoría**:

| Categoría | Relativos a |
|---|---|
| **Técnicos** | La construcción del sistema |
| **De proyecto** | Plazos, recursos, alcance |
| **De negocio** | Que el sistema sirva para lo que se pensó |
| **De personal** | Las personas |

Para cada riesgo, indiquen **de dónde salió**:

- del cuadrante de amenazas o debilidades del FODA del TP1;
- de los supuestos declarados en el alcance del TP2;
- de las dependencias externas del cronograma del TP6;
- de experiencia previa;
- de consulta al equipo.

> Los supuestos del alcance y el cuadrante de amenazas del FODA ya son, literalmente, una lista de riesgos. Si no aparece ninguno de ahí, es que no se los revisó.

### Parte B — Enunciado

Reescriban cada riesgo en la forma:

> **"Que ocurra X, y como consecuencia Y."**

| ❌ Vago | ✅ Enunciado correctamente |
|---|---|
| "Problemas con los datos" | "Que los datos de socios tengan más del 20 % de registros incompletos y la migración requiera limpieza manual" |
| "Falta de tiempo" | "Que el referente no disponga de las 4 horas semanales acordadas y las validaciones se demoren" |

Un riesgo mal enunciado no se puede supervisar ni mitigar.

### Parte C — Proyección

Asignen probabilidad e impacto con las escalas de la unidad:

| Probabilidad | Valor | | Impacto | Valor |
|---|---|---|---|---|
| Muy baja | 10 % | | Catastrófico | 4 |
| Baja | 30 % | | Crítico | 3 |
| Media | 50 % | | Marginal | 2 |
| Alta | 70 % | | Despreciable | 1 |
| Muy alta | 90 % | | | |

Calculen la **exposición** y ordenen la matriz por ese valor:

```
Exposición = Probabilidad × Impacto
```

Cuando puedan, cuantifiquen el impacto en **días de atraso** o en **dinero**. La exposición queda en las mismas unidades y se vuelve mucho más útil para decidir.

### Parte D — Matriz gráfica

Ubiquen los ocho riesgos en la matriz de probabilidad por impacto:

| | Despreciable | Marginal | Crítico | Catastrófico |
|---|---|---|---|---|
| **Muy alta** | | | | |
| **Alta** | | | | |
| **Media** | | | | |
| **Baja** | | | | |
| **Muy baja** | | | | |

### Parte E — Plan de RSGR

Para los **cuatro riesgos de mayor exposición**, completen la ficha:

| Campo | Contenido |
|---|---|
| **Riesgo** | Enunciado completo |
| **Probabilidad × Impacto** | Con la exposición resultante |
| **Estrategia** | Evitar · Mitigar · Transferir · Aceptar |
| **Reducción** | Qué se hace antes, y en qué momento del proyecto |
| **Supervisión** | Qué indicador se observa, con **umbral** y **frecuencia** |
| **Contingencia** | Qué se hace concretamente si ocurre |
| **Responsable** | Una sola persona |

**El indicador de supervisión es obligatorio y debe tener umbral.** Sin umbral, nadie sabe cuándo activar la contingencia.

| ❌ | ✅ |
|---|---|
| "Controlar el avance de la migración" | "Registros validados por semana. Alerta si son menos de 100" |
| "Estar atentos a la disponibilidad del referente" | "Horas efectivas de reunión por semana. Alerta si hay dos semanas consecutivas por debajo de 2 h" |

### Parte F — Riesgos aceptados

Si aceptan algún riesgo, fundamenten **por qué** y describan **cómo lo informarían** a la organización.

Aceptar un riesgo es una decisión de gestión válida. Aceptarlo sin informarlo no lo es: la decisión de aceptar un riesgo del negocio le corresponde a la organización, no al equipo técnico.

### Parte G — Análisis costo-mitigación

Elijan un riesgo y estimen el **costo de mitigarlo** en horas o en dinero.

Compárenlo con su exposición y concluyan si conviene mitigarlo.

> El criterio es: **mitigar cuando el costo de mitigar es menor que la exposición.**

### Parte H — Revisión

En el corte de control siguiente, revisen la matriz y entreguen la revisión:

| Pregunta | Qué registrar |
|---|---|
| ¿Cambió alguna probabilidad? | Recalcular y reordenar |
| ¿Algún indicador cruzó su umbral? | Qué se hizo |
| ¿Aparecieron riesgos nuevos? | Incorporarlos |
| ¿Algún riesgo se cerró? | Si fue porque la mitigación funcionó o porque nunca fue un riesgo real |
| ¿Alguno se materializó? | Qué falló en la anticipación |

---

## Criterios de evaluación

| Criterio | Puntos |
|---|---|
| **Ocho riesgos**, con al menos dos por categoría | 15 |
| **Trazabilidad del origen** — al menos tres derivados del FODA, los supuestos o las dependencias externas | 10 |
| **Enunciado** en la forma "que ocurra X, y como consecuencia Y" | 15 |
| **Proyección** con las escalas, exposición calculada y matriz ordenada | 10 |
| **Impacto cuantificado** en días o dinero en al menos tres riesgos | 5 |
| **Matriz gráfica** completa | 5 |
| **Fichas de RSGR** — cuatro completas con los siete campos | 20 |
| **Indicadores de supervisión** con umbral y frecuencia | 10 |
| **Riesgos aceptados** fundamentados, con cómo se informan | 5 |
| **Análisis costo-mitigación** de un riesgo | 5 |
| **Total** | **100** |

---

## Lo que baja la nota

| Situación | Descuento |
|---|---|
| Riesgos vagos, sin la forma "que ocurra X, y como consecuencia Y" | −4 cada uno |
| Menos de dos riesgos en alguna categoría | −5 por categoría |
| Ningún riesgo de negocio | −10 |
| Confundir riesgo con problema (describir algo que ya ocurrió) | −5 cada caso |
| Indicador de supervisión sin umbral | −4 cada uno |
| Confundir reducción con contingencia | −5 cada ficha |
| Riesgo aceptado sin fundamento ni plan de comunicación | −5 |
| Ignorar riesgos de probabilidad baja e impacto catastrófico | −8 |
| Matriz que contiene solo riesgos menores | −10 |

---

## Recomendaciones

- Empiecen por releer los supuestos del TP2. Cada supuesto que no se cumpla **es** un riesgo, y ya los tienen escritos.
- Las dependencias externas del TP6 son la fuente más directa de riesgos de proyecto.
- Un riesgo de probabilidad baja e impacto catastrófico no se puede ignorar por ser poco probable. Es el caso que más daño hace cuando ocurre.
- La diferencia entre reducción y contingencia: la reducción es lo que se hace **antes** para que no ocurra o para que duela menos; la contingencia es lo que se hace **si ocurre**.
- Los riesgos de negocio son los que más proyectos inutilizan y los que menos se identifican. Pregúntense: ¿qué pasaría si construimos esto perfectamente y nadie lo usa?
- Un informe de riesgos que solo contiene riesgos menores no es tranquilizador: es un informe que no se hizo.
