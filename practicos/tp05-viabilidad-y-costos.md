# TP5 — Informe de viabilidad y costos

> **Unidad:** [9 — Viabilidad y costos del proyecto](../unidades/09-viabilidad-y-costos/)
> **Modalidad:** grupal, 3 a 4 integrantes
> **Entregable:** informe técnico de viabilidad, más una página de recomendación
> **Puntaje:** 100 puntos

---

## Objetivo

Determinar si el proyecto propuesto es viable y cuánto cuesta, y producir la recomendación fundamentada que la organización necesita para decidir.

> Este es el único entregable del año que **puede concluir que el proyecto no debe hacerse**. Si esa conclusión está bien fundamentada, se evalúa igual de bien que la contraria.

---

## Consigna

### Parte A — Las cinco dimensiones

Analicen cada dimensión. Para cada una: **qué evaluaron**, **qué encontraron** y una **conclusión de una línea**.

| Dimensión | Pregunta central | Mínimo a verificar |
|---|---|---|
| **Técnica** | ¿Se puede construir? | Habilidades del equipo, tecnología, infraestructura, integraciones |
| **Operativa** | ¿La organización va a poder usarlo? | Capacidad de los usuarios, adaptación al proceso, resistencia, quién lo mantendrá |
| **Económica** | ¿El beneficio justifica el costo? | Costo total, costo de mantenimiento, beneficio, recupero |
| **Temporal** | ¿Se puede tener a tiempo? | Si la fecha límite es real o negociable, y qué pasa si se entrega después |
| **Legal** | ¿Está permitido? | Normativa sobre los datos involucrados, datos personales o sensibles, licencias, propiedad de lo construido |

> La **operativa** es la que más proyectos técnicamente correctos hace fracasar. No la traten como un formalismo.

### Parte B — Estructura de costos

Construyan la tabla completa, partiendo del esfuerzo estimado en el TP4.

Cinco categorías obligatorias:

| Categoría | No olvidar |
|---|---|
| Recursos humanos | Costo del persona-mes con cargas, no solo salario |
| Infraestructura | Distinguir costo de una vez del mensual |
| Licencias | Incluidos servicios de terceros con costo por uso |
| **Capacitación** | De los usuarios de la organización, no solo del equipo |
| **Mantenimiento** | El costo anual que continúa cuando el proyecto termina |

Clasifiquen además cada ítem como **directo**, **indirecto** o **de oportunidad**.

**Obligatorio:** incluyan al menos un **costo de oportunidad** cuantificado. Por ejemplo, las horas que el referente de la organización dedica al proyecto y no a su trabajo habitual.

### Parte C — Beneficios

Cuantifiquen los beneficios. Cada monto debe ir con **el supuesto y la fuente del dato**.

| Tipo de beneficio | Cómo se cuantifica |
|---|---|
| Tiempo ahorrado | Horas liberadas × costo de la hora |
| Pérdida evitada | Monto que hoy se pierde por errores, olvidos o morosidad |
| Ingreso posibilitado | Capacidad de atender más operaciones con la misma estructura |

Los beneficios **intangibles** —imagen, satisfacción, menos estrés— se listan **aparte** y no se suman al cálculo.

### Parte D — Retorno

```
Beneficio neto anual = beneficio anual − mantenimiento anual

Período de recupero = costo total inicial / beneficio neto anual
```

Interpreten el resultado **contra el horizonte de la organización**: un recupero a tres años es razonable para una institución de vida larga y no lo es para un emprendimiento que no sabe si va a existir en dos.

### Parte E — Costo de no hacer nada

Cuantifiquen la alternativa de **no hacer el proyecto**.

No hacer nada también tiene costo: el problema sigue produciendo pérdidas. Sin este número, no hay con qué comparar.

### Parte F — Análisis de sensibilidad

Identifiquen el **supuesto más frágil** de su análisis.

Recalculen el período de recupero suponiendo que ese supuesto se cumple **a la mitad**. Indiquen si la recomendación cambia.

### Parte G — Alternativas

Presenten **tres alternativas** en una tabla comparativa. Una de ellas debe ser no hacer nada.

| Alternativa | Costo | Recupero | Qué resuelve | Qué deja sin resolver |
|---|---|---|---|---|

### Parte H — Recomendación

**Una página, documento separado**, dirigida a quien decide en la organización.

Estructura obligatoria:

1. **Recomendación** — al principio, en una oración.
2. **Por qué** — el fundamento en dos o tres líneas.
3. **Costo y recupero** de la opción recomendada.
4. **Alternativas** con su número.
5. **Riesgo principal.**
6. **Supuesto crítico** y qué pasa si no se cumple.

Reglas de redacción:

- afirmaciones verificables, no impresiones;
- números con su supuesto al lado;
- sin condicional evasivo.

---

## Criterios de evaluación

| Criterio | Puntos |
|---|---|
| **Cinco dimensiones** analizadas, con qué se evaluó y conclusión por dimensión | 20 |
| **Viabilidad operativa** — tratada con profundidad, no como formalismo | 10 |
| **Estructura de costos** — cinco categorías completas | 15 |
| **Capacitación y mantenimiento** incluidos | 5 |
| **Costo de oportunidad** cuantificado | 5 |
| **Beneficios** con supuesto y fuente por cada monto | 10 |
| **Intangibles** listados aparte, sin sumarse | 5 |
| **Retorno** calculado e interpretado contra el horizonte de la organización | 10 |
| **Costo de no hacer nada** cuantificado | 5 |
| **Análisis de sensibilidad** del supuesto más frágil | 5 |
| **Tres alternativas** comparadas | 5 |
| **Recomendación** de una página, con la conclusión al principio | 5 |
| **Total** | **100** |

---

## Lo que baja la nota

| Situación | Descuento |
|---|---|
| Analizar solo la viabilidad técnica | −20 |
| Omitir el costo de mantenimiento | −10 |
| Omitir la capacitación de usuarios | −5 |
| Sumar beneficios intangibles al cálculo económico | −8 |
| Montos sin supuesto ni fuente | −3 cada uno |
| No incluir la alternativa de no hacer nada | −8 |
| Recomendación con la conclusión al final | −5 |
| Uso de condicional evasivo ("podría eventualmente presentar dificultades") | −3 cada caso |
| No preguntar por la normativa cuando hay datos personales o sensibles | −10 |
| Ajustar los supuestos hasta que el retorno resulte atractivo | −20 |

---

## Recomendaciones

- Posible y viable no son lo mismo. Un proyecto puede construirse perfectamente y no convenir.
- Para la viabilidad operativa, la pregunta que más revela es: **¿este sistema resuelve un problema de la dirección creando trabajo nuevo para quien opera?** Si la respuesta es sí, hay un problema grave.
- Presentar un costo de proyecto sin el mantenimiento es informar la mitad del número.
- El costo de oportunidad no aparece en ninguna factura y suele pesar más que varios ítems que sí aparecen.
- La segunda **jornada de práctica en la organización** está destinada al relevamiento de costos y recursos de este informe. Vayan con la lista de datos que necesitan.
- Si el análisis concluye que el proyecto no es viable, dígalo. Informar la inviabilidad es parte del trabajo del analista, no una falla.
