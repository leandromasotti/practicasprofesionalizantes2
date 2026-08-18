# Unidad 4
# Diagnóstico organizacional: FODA y técnicas de análisis

> "Un médico que receta antes de examinar comete mala praxis. Un analista que propone un sistema antes de diagnosticar la organización hace exactamente lo mismo, con la diferencia de que nadie lo denuncia."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Comprender qué es un diagnóstico organizacional y por qué antecede a toda propuesta.
- Distinguir un síntoma de un problema y de su causa.
- Aplicar técnicas de diagnóstico: observación, relevamiento documental y análisis de procesos.
- Construir una matriz FODA sobre una organización real.
- Cruzar la matriz para derivar líneas de acción.
- **Identificar oportunidades de proyecto** a partir del diagnóstico y fundamentarlas.

> **Articulación.** Ingeniería en Software I desarrolla las técnicas de elicitación de requisitos —entrevistas, cuestionarios, JAD, brainstorming—. Aquí no se estudian esas técnicas sino lo que viene antes: comprender la organización como un todo para poder decidir **qué** proyecto vale la pena.

---

# El problema inicial

Una organización llama a un analista y le dice qué necesita.

> "Necesitamos un sistema de gestión."

Es tentador tomar ese enunciado como punto de partida y empezar a relevar requerimientos.

Sería un error.

Lo que la organización expresa es **lo que cree que necesita**, y esa creencia ya contiene una solución. Antes de aceptarla hay que verificar dos cosas:

- si el problema que se quiere resolver es realmente el que están nombrando;
- si un sistema es la respuesta adecuada a ese problema.

A veces lo es. Muchas veces el problema es un proceso mal diseñado, y automatizar un proceso malo produce un proceso malo más rápido.

El **diagnóstico organizacional** es el trabajo que permite responder esas dos preguntas.

---

# Qué es un diagnóstico organizacional

Diagnosticar consiste en estudiar cómo funciona efectivamente una organización para identificar problemas, oportunidades de mejora y necesidades de información.

No es lo mismo que relevar requerimientos.

| | Diagnóstico | Relevamiento de requerimientos |
|---|---|---|
| **Pregunta** | ¿Qué le pasa a esta organización? | ¿Qué debe hacer el sistema? |
| **Momento** | Antes de decidir el proyecto | Después de decidirlo |
| **Alcance** | La organización | El sistema |
| **Resultado** | Oportunidades de proyecto | Especificación |

El diagnóstico produce la materia prima de una decisión: **qué conviene hacer**, y si conviene hacer algo.

---

# Síntoma, problema y causa

Esta distinción es la herramienta conceptual central de la unidad.

- **Síntoma:** lo que se observa y molesta.
- **Problema:** la disfunción que produce ese síntoma.
- **Causa:** el origen de esa disfunción.

Un ejemplo:

| | |
|---|---|
| **Síntoma** | "Los socios se quejan de que les cobran cuotas que ya pagaron." |
| **Problema** | No existe un registro confiable y único de pagos. |
| **Causa** | Cada cobrador anota en su propio cuaderno y las planillas se consolidan una vez por mes, a mano. |

Si el analista trabaja sobre el síntoma, construirá un sistema de reclamos.

Si trabaja sobre el problema, construirá un registro único de pagos.

Si trabaja sobre la causa, quizá descubra que el problema se resuelve cambiando el momento de consolidación, y que el sistema es más chico de lo que parecía —o innecesario—.

> Una regla práctica: ante un síntoma, preguntar "¿por qué ocurre?" tres o cuatro veces seguidas. La respuesta que ya no admite otro "por qué" suele estar cerca de la causa.

---

# Técnicas de diagnóstico

## Observación

Mirar cómo se trabaja realmente, en el lugar donde se trabaja.

Es la técnica que más contradicciones revela, porque **lo que se hace rara vez coincide con lo que se dice que se hace**.

Qué observar:

- Cuánto tarda cada tarea en la práctica.
- Qué pasos se saltean respecto del procedimiento oficial.
- Qué anotaciones informales existen: cuadernos, planillas propias, mensajes.
- Dónde se acumula trabajo y dónde se espera.
- Qué tareas se rehacen.

> Los sistemas paralelos —la planilla personal que alguien mantiene "por las dudas"— son la evidencia más valiosa de un diagnóstico. Indican exactamente dónde el sistema oficial no responde.

---

## Relevamiento documental

Estudiar lo que la organización ya produce y conserva.

- Formularios y planillas en uso.
- Reglamentos, procedimientos y manuales.
- Informes que se elaboran periódicamente.
- Registros contables y de facturación.
- Normativa que la organización debe cumplir.

Un formulario dice mucho: qué datos la organización considera importantes, cuáles pide dos veces y cuáles nadie completa nunca.

---

## Análisis de procesos

Reconstruir la secuencia real de pasos de una actividad, con sus responsables, sus tiempos y sus puntos de decisión.

Preguntas que guían el análisis:

- ¿Dónde empieza y dónde termina el proceso?
- ¿Quién interviene en cada paso?
- ¿Qué información se necesita y de dónde sale?
- ¿Dónde se demora?
- ¿Qué pasos no agregan valor?
- ¿Qué ocurre cuando algo sale mal?

---

## Indicadores

Cuando existen datos, conviene usarlos: cantidad de operaciones por período, tiempos promedio, tasa de error, reclamos recibidos.

Un diagnóstico apoyado en números es mucho más difícil de discutir que uno apoyado en impresiones.

> Articula con **Estadística**, cursada en paralelo, para el tratamiento de los datos relevados.

---

# El análisis FODA

FODA es una herramienta de diagnóstico que ordena la situación de una organización en cuatro cuadrantes, según dos ejes: **origen** (interno o externo) y **signo** (favorable o desfavorable).

| | **Favorable** | **Desfavorable** |
|---|---|---|
| **Interno** — la organización controla | **F** — Fortalezas | **D** — Debilidades |
| **Externo** — la organización no controla | **O** — Oportunidades | **A** — Amenazas |

En inglés se la conoce como **SWOT**.

## Los cuatro cuadrantes

### Fortalezas

Capacidades propias que la organización posee y puede aprovechar.

*Ejemplos:* personal con experiencia, buena reputación, equipamiento disponible, procesos ya ordenados, respaldo económico.

### Debilidades

Carencias propias que la limitan.

*Ejemplos:* registros en papel, dependencia de una sola persona, ausencia de control de pagos, personal sin capacitación, procesos no documentados.

### Oportunidades

Circunstancias externas que podría aprovechar.

*Ejemplos:* una línea de financiamiento disponible, crecimiento de la demanda, tecnología que bajó de precio, un cambio normativo favorable.

### Amenazas

Circunstancias externas que podrían perjudicarla.

*Ejemplos:* competencia nueva, aumento de costos, exigencias regulatorias más estrictas, dependencia de un proveedor único.

---

## La regla que define el eje interno/externo

La confusión más común es ubicar en el cuadrante equivocado.

El criterio es uno solo:

> **¿La organización puede modificarlo por decisión propia?**
>
> Si sí, es interno: fortaleza o debilidad.
>
> Si no, es externo: oportunidad o amenaza.

Ejemplos que suelen ubicarse mal:

| Elemento | Cuadrante correcto | Por qué |
|---|---|---|
| "El personal no sabe usar computadoras" | Debilidad | La organización puede capacitarlo |
| "Los socios cada vez pagan más tarde" | Amenaza | Depende de los socios, no de la organización |
| "Tenemos buena ubicación" | Fortaleza | Es un recurso propio |
| "Apareció un competidor con app propia" | Amenaza | Externo y no controlable |
| "No tenemos presupuesto" | Debilidad | Es una condición interna |

---

## Cómo construir la matriz

**1. Definir el alcance.** Una matriz FODA de "la organización entera" suele quedar genérica e inútil. Conviene acotarla: la gestión administrativa, la atención al socio, el área de cobranzas.

**2. Relevar antes de clasificar.** La matriz se llena con lo observado, no con lo imaginado.

**3. Enunciar con precisión.** Cada punto debe ser verificable.

| ❌ Vago | ✅ Preciso |
|---|---|
| "Mala organización" | "No existe un registro único de pagos: cada cobrador lleva su propio cuaderno" |
| "Poco personal" | "Una sola persona administra socios, cuotas y actividades" |
| "Tecnología" | "Se dispone de tres computadoras y conexión estable, sin uso sistemático" |

**4. Priorizar.** No todos los puntos pesan igual. Conviene marcar los tres o cuatro determinantes de cada cuadrante.

**5. Validar con la organización.** Un diagnóstico que la organización no reconoce como propio no sirve para decidir nada.

---

## El cruce de la matriz

Una matriz FODA por sí sola es una lista. Lo que la convierte en herramienta de decisión es **cruzarla**.

| | **Oportunidades** | **Amenazas** |
|---|---|---|
| **Fortalezas** | **FO** — Usar fortalezas para aprovechar oportunidades | **FA** — Usar fortalezas para defenderse de amenazas |
| **Debilidades** | **DO** — Superar debilidades aprovechando oportunidades | **DA** — Reducir debilidades para no sucumbir ante amenazas |

Cada casilla del cruce sugiere líneas de acción, y **de ahí salen las oportunidades de proyecto**.

Este paso es el que distingue un FODA hecho como trámite de uno que efectivamente orienta una decisión.

---

# Del diagnóstico a la oportunidad de proyecto

El diagnóstico no termina en la matriz. Termina en una recomendación.

El recorrido completo:

1. **Síntomas observados** → lo que molesta.
2. **Problemas identificados** → qué disfunción los produce.
3. **Causas** → por qué ocurre.
4. **Matriz FODA** → situación de la organización.
5. **Cruce** → líneas de acción posibles.
6. **Oportunidades de proyecto** → qué se podría hacer.
7. **Recomendación fundamentada** → qué conviene hacer primero, y por qué.

Para priorizar entre varias oportunidades, tres preguntas:

- ¿Cuál resuelve el problema de mayor impacto?
- ¿Cuál es viable con los recursos de la organización?
- ¿Cuál produce resultados visibles más pronto?

La tercera importa más de lo que parece: un primer resultado visible sostiene el apoyo de la organización para lo que sigue.

> La viabilidad se analiza en profundidad en la **Unidad 9**. Aquí alcanza con una evaluación preliminar.

---

# Errores frecuentes

- **Diagnosticar con la solución ya decidida.** Si el analista llega convencido de que hace falta un sistema, encontrará evidencia de que hace falta un sistema.
- **Confundir síntoma con problema**, y construir sobre el síntoma.
- **Aceptar el enunciado del cliente sin verificarlo.**
- **Llenar la matriz FODA con generalidades** que servirían para cualquier organización.
- **Confundir el eje interno con el externo.**
- **Armar la matriz y no cruzarla**, con lo que queda en una lista decorativa.
- **Diagnosticar sin hablar con quien hace el trabajo.** La dirección describe el proceso oficial; el personal conoce el real.
- **Presentar el diagnóstico como una lista de defectos.** Un diagnóstico que solo señala fallas genera resistencia y se desestima.

---

# Buenas prácticas

✔ Observar el trabajo real antes de preguntar por él.

✔ Preguntar "¿por qué?" hasta llegar a la causa.

✔ Enunciar cada punto de forma verificable.

✔ Apoyar el diagnóstico en datos siempre que existan.

✔ Cruzar la matriz para derivar líneas de acción.

✔ Validar el diagnóstico con la organización antes de proponer.

✔ Reconocer las fortalezas, no solo las carencias.

---

# Caso de estudio

## Club Deportivo San Martín

Retomamos el caso de la Unidad 1, ahora desde el diagnóstico.

### Lo relevado

Durante dos visitas al club se observó y documentó:

- Los socios se registran en fichas de papel guardadas en un fichero.
- Las cuotas se cobran en efectivo en la sede; el cobrador anota en un cuaderno.
- Una vez por mes, la administrativa transcribe el cuaderno a una planilla de Excel.
- Las actividades deportivas se organizan en planillas separadas, una por disciplina.
- No hay sistema de turnos: los profesores anotan en papel.
- La administrativa es la única persona que conoce el circuito completo.
- El club tiene tres computadoras y conexión estable.
- La comisión directiva aprobó un presupuesto acotado para modernizarse.
- En el barrio abrió un gimnasio con aplicación de reservas propia.
- La cantidad de socios creció un 30 % en dos años.

### Matriz FODA

| | Favorable | Desfavorable |
|---|---|---|
| **Interno** | **Fortalezas**<br>• Equipamiento disponible sin uso sistemático<br>• Presupuesto aprobado para modernización<br>• Personal con conocimiento profundo del circuito | **Debilidades**<br>• Registro de socios y cobros en papel<br>• Consolidación manual y mensual de pagos<br>• Dependencia de una sola persona<br>• Sin sistema de turnos |
| **Externo** | **Oportunidades**<br>• Crecimiento sostenido de socios<br>• Tecnología accesible y de bajo costo | **Amenazas**<br>• Competencia con aplicación propia<br>• Riesgo de perder socios por errores de cobro |

### Cruce

| | Oportunidades | Amenazas |
|---|---|---|
| **Fortalezas** | **FO:** aprovechar el equipamiento y el presupuesto para acompañar el crecimiento de socios con un registro digital | **FA:** usar el conocimiento del circuito para digitalizar sin perder el detalle operativo que hoy sostiene el club |
| **Debilidades** | **DO:** reemplazar el registro en papel aprovechando que la tecnología es accesible | **DA:** eliminar la consolidación mensual manual, que es la causa directa del riesgo de errores de cobro |

### Para analizar

1. Identifique un síntoma, su problema y su causa entre lo relevado.
2. ¿Cuál de las cuatro líneas del cruce atacaría primero? Fundamente con las tres preguntas de priorización.
3. La dependencia de una sola persona, ¿se resuelve con un sistema? ¿Qué más haría falta?
4. ¿Qué dato le pediría al club que no figura en lo relevado?
5. ¿Qué ocurriría si el club informatizara los turnos sin tocar el registro de pagos?

---

# Aplicación profesional

Esta unidad habilita la **primera jornada de práctica en la organización** del ciclo.

La jornada no es una visita: es trabajo de campo con un objetivo definido.

Antes de ir, cada grupo debe llevar preparado:

- qué va a observar y en qué parte del proceso;
- qué documentación va a solicitar;
- con quién necesita hablar, además de la dirección;
- qué datos cuantitativos va a intentar obtener;
- cómo va a registrar lo relevado.

Después de la jornada, el grupo produce su **informe de diagnóstico** con la matriz FODA, su cruce y las oportunidades de proyecto identificadas.

Ese informe es el insumo del documento de alcance de la Unidad 5: no se puede definir el alcance de un proyecto que todavía no se decidió cuál es.

---

# Resumen

En esta unidad aprendimos que:

- El diagnóstico organizacional antecede al relevamiento de requerimientos y responde una pregunta distinta: qué conviene hacer, y si conviene hacer algo.
- Lo que el cliente enuncia como necesidad ya contiene una solución, y esa solución debe verificarse.
- Síntoma, problema y causa son cosas distintas; trabajar sobre el síntoma produce sistemas que no resuelven nada.
- Las técnicas de diagnóstico son la observación, el relevamiento documental, el análisis de procesos y los indicadores.
- La observación revela las contradicciones entre el trabajo declarado y el trabajo real.
- FODA ordena la situación según origen y signo; el criterio del eje es si la organización puede modificarlo por decisión propia.
- Una matriz sin cruzar es una lista: el cruce FO, DO, FA y DA es lo que produce líneas de acción.
- El diagnóstico termina en una recomendación fundamentada, no en una matriz.

---

# Actividad práctica

## Diagnóstico de la organización

En los grupos del proyecto integrador, sobre la organización elegida.

**1. Síntomas, problemas y causas**

Documenten tres síntomas observados. Para cada uno, identifiquen el problema que lo produce y su causa probable. Usen la pregunta "¿por qué?" al menos tres veces en cada cadena.

**2. Técnicas aplicadas**

Indiquen qué técnicas de diagnóstico usaron y qué obtuvo cada una. Si hubo diferencias entre lo que les contaron y lo que observaron, regístrenlas: son el hallazgo más valioso.

**3. Matriz FODA**

Construyan la matriz con un alcance acotado y explicitado. Mínimo tres puntos por cuadrante, todos enunciados de forma verificable.

**4. Cruce**

Completen las cuatro casillas FO, DO, FA y DA con al menos una línea de acción cada una.

**5. Oportunidades de proyecto**

Deriven dos o tres oportunidades y prioricen una, fundamentando con las tres preguntas de priorización.

**6. Recomendación**

Cierren con un párrafo dirigido a la dirección de la organización, en lenguaje no técnico, explicando qué recomiendan hacer primero y por qué.

**Formato de entrega:** informe técnico de dos a tres páginas, con la matriz en formato de tabla.

---

# Preguntas de repaso

1. ¿En qué se diferencia un diagnóstico organizacional de un relevamiento de requerimientos?

2. ¿Por qué no conviene aceptar sin verificar el enunciado de necesidad del cliente?

3. Explique la diferencia entre síntoma, problema y causa con un ejemplo propio.

4. ¿Por qué la observación revela cosas que la entrevista no revela?

5. ¿Cuál es el criterio para decidir si un elemento del FODA es interno o externo?

6. ¿Qué aporta el cruce de la matriz que la matriz sola no aporta?

7. ¿Por qué conviene priorizar una oportunidad que produzca resultados visibles pronto?

8. ¿Qué riesgo tiene presentar un diagnóstico compuesto únicamente por debilidades?

---

# Bibliografía

- Sommerville, I. *Ingeniería del Software.* Capítulo sobre sistemas socio-técnicos y su contexto organizacional.
- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Sección sobre análisis del dominio del problema.
- [Asana — Análisis FODA: qué es y cómo hacerlo](https://asana.com/es/resources/swot-analysis)
- [Atlassian — Análisis FODA](https://www.atlassian.com/es/work-management/strategic-planning/swot-analysis)
- [Investopedia — SWOT Analysis](https://www.investopedia.com/terms/s/swot.asp)
- [MindTools — SWOT Analysis](https://www.mindtools.com/amtbj63/swot-analysis)

---

**Fin de la Unidad 4**
