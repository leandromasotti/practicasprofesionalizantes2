# Unidad 12
# Gestión del riesgo y plan de RSGR

> "Un riesgo que se conoce y no se comunica deja de ser un riesgo del proyecto y pasa a ser una responsabilidad de quien lo calló."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Distinguir un riesgo de un problema.
- Identificar riesgos técnicos, de proyecto, de negocio y de personal.
- Proyectar el riesgo estimando probabilidad e impacto.
- Construir y priorizar una matriz de riesgos.
- Elaborar un **plan de RSGR**: reducción, supervisión y gestión del riesgo.
- Definir planes de contingencia.
- Realizar el seguimiento de riesgos durante el proyecto.

---

# Riesgo y problema

La distinción es simple y determinante:

| | Riesgo | Problema |
|---|---|---|
| **Cuándo ocurre** | Todavía no ocurrió | Ya ocurrió |
| **Qué se hace** | Se anticipa | Se resuelve |
| **Cuándo se actúa** | Antes | Después |
| **Costo de actuar** | Bajo | Alto |

> Un riesgo es un problema que todavía no pasó. Un problema es un riesgo que no se gestionó.

La gestión del riesgo consiste en pensar antes lo que otros piensan después.

## Los dos componentes

Todo riesgo tiene dos:

- **Probabilidad** — qué tan posible es que ocurra.
- **Impacto** — qué consecuencia tendría si ocurriera.

Un riesgo con probabilidad alta e impacto despreciable no merece atención. Uno con probabilidad baja e impacto catastrófico, sí.

---

# Identificación de riesgos

## Las cuatro categorías

### Riesgos técnicos

Relativos a la construcción del sistema.

- Tecnología que el equipo no domina.
- Integración con un sistema del que no hay documentación.
- Requerimiento sin solución técnica conocida.
- Rendimiento que puede no alcanzar lo pedido.
- Calidad de los datos existentes.

### Riesgos de proyecto

Relativos a la conducción: plazos, recursos, alcance.

- Estimación subestimada.
- Alcance que crece sin control.
- Recursos que no llegan cuando hacen falta.
- Dependencias externas que no se cumplen.
- Plazo impuesto sin fundamento.

### Riesgos de negocio

Relativos a que el sistema sirva para lo que se pensó.

- Que el sistema se construya y nadie lo use.
- Que el problema cambie antes de la entrega.
- Que la organización pierda el interés o el financiamiento.
- Que aparezca normativa que lo invalide.
- Que el beneficio esperado no se materialice.

### Riesgos de personal

Relativos a las personas.

- Ausencia o renuncia de alguien clave.
- Conocimiento concentrado en una sola persona.
- Falta de disponibilidad del referente de la organización.
- Equipo con habilidades insuficientes.
- Rotación durante el proyecto.

## Cómo identificarlos

| Técnica | Cómo funciona |
|---|---|
| **Lista de comprobación** | Recorrer las cuatro categorías con preguntas fijas |
| **Revisión de supuestos** | Cada supuesto del documento de alcance es un riesgo si no se cumple |
| **Experiencia anterior** | Qué salió mal en proyectos parecidos |
| **Consulta al equipo** | Preguntar qué es lo que más le preocupa a cada uno |
| **Análisis del diagnóstico** | Las debilidades y amenazas del FODA de la Unidad 4 son fuente directa de riesgos |

> Las dos últimas son las más productivas y las más baratas. Los supuestos declarados en el alcance y el cuadrante de amenazas del FODA ya son, literalmente, una lista de riesgos.

## Cómo enunciar un riesgo

Un riesgo mal enunciado no se puede gestionar.

| ❌ Vago | ✅ Enunciado correctamente |
|---|---|
| "Problemas con los datos" | "Que los datos de socios tengan más del 20 % de registros incompletos y la migración requiera limpieza manual" |
| "Falta de tiempo" | "Que el referente de la organización no disponga de las 4 horas semanales acordadas y las validaciones se demoren" |
| "Riesgo técnico" | "Que el sistema contable no permita importar el archivo de cobranzas en el formato que genera nuestro sistema" |

La forma útil es: **"Que ocurra X, y como consecuencia Y"**.

---

# Proyección del riesgo

Proyectar es estimar probabilidad e impacto para poder priorizar.

## Escala de probabilidad

| Nivel | Descripción | Valor |
|---|---|---|
| Muy baja | Improbable pero posible | 10 % |
| Baja | Podría ocurrir | 30 % |
| Media | Es posible que ocurra | 50 % |
| Alta | Probablemente ocurra | 70 % |
| Muy alta | Casi seguro | 90 % |

## Escala de impacto

| Nivel | Descripción | Valor |
|---|---|---|
| **Catastrófico** | El proyecto no puede continuar | 4 |
| **Crítico** | Afecta gravemente plazo, costo o alcance | 3 |
| **Marginal** | Produce molestias manejables | 2 |
| **Despreciable** | Efecto mínimo | 1 |

## Exposición al riesgo

La priorización se hace por **exposición**:

```
Exposición = Probabilidad × Impacto
```

Cuando el impacto se puede cuantificar en dinero o en días, la exposición queda en las mismas unidades y se vuelve mucho más útil para decidir.

```
Exposición = Probabilidad × Costo del impacto
```

*Ejemplo:* un riesgo con 30 % de probabilidad y un impacto de 15 días de atraso tiene una exposición de 4,5 días. Si mitigarlo cuesta 2 días de trabajo, conviene mitigarlo.

> Ese es el criterio de decisión: **mitigar cuando el costo de mitigar es menor que la exposición**.

---

# La matriz de riesgos

## Caso: Club Deportivo San Martín

| # | Riesgo | Cat. | Prob. | Imp. | Expos. | Prioridad |
|---|---|---|---|---|---|---|
| R1 | Que los datos de socios tengan más del 20 % de registros incompletos y requieran limpieza manual | Técnico | 70 % | 3 | 2,10 | **Alta** |
| R2 | Que el referente no disponga de las 4 h semanales y las validaciones se demoren | Personal | 50 % | 3 | 1,50 | **Alta** |
| R3 | Que el conocimiento del circuito administrativo esté solo en la administrativa y ella se ausente | Personal | 30 % | 4 | 1,20 | **Alta** |
| R4 | Que el sistema contable no acepte el formato de importación | Técnico | 50 % | 2 | 1,00 | Media |
| R5 | Que la comisión directiva pida funcionalidad nueva durante el proyecto | Proyecto | 70 % | 2 | 1,40 | **Alta** |
| R6 | Que el personal no adopte el sistema y siga usando el cuaderno | Negocio | 30 % | 4 | 1,20 | **Alta** |
| R7 | Que el servidor no esté provisto en la semana 4 | Proyecto | 30 % | 2 | 0,60 | Media |
| R8 | Que cambie la comisión directiva y se pierda el apoyo al proyecto | Negocio | 10 % | 4 | 0,40 | Baja |

## Lectura de la matriz

**R1 es el riesgo mayor** y viene directamente del diagnóstico: sabemos que los registros están en papel y se consolidan a mano.

**R3 y R6 tienen probabilidad baja pero impacto catastrófico.** No se pueden ignorar por ser poco probables.

**R8 tiene la exposición más baja** pero conviene dejarlo registrado: si se acerca una elección en el club, su probabilidad cambia.

## Representación gráfica

| | Despreciable | Marginal | Crítico | Catastrófico |
|---|---|---|---|---|
| **Muy alta** | | | | |
| **Alta** | | R5 | R1 | |
| **Media** | | R4 | R2 | |
| **Baja** | | R7 | | R3, R6 |
| **Muy baja** | | | | R8 |

El cuadrante superior derecho es la zona de atención prioritaria. El inferior izquierdo, la de riesgos que solo se registran.

---

# El plan de RSGR

**RSGR** son las siglas de **Reducción, Supervisión y Gestión del Riesgo**.

Es el documento donde se define, para cada riesgo relevante, qué se hace antes, durante y después.

## Las tres partes

### Reducción — antes de que ocurra

Acciones para bajar la probabilidad o el impacto.

### Supervisión — durante el proyecto

Qué indicador se observa para saber si el riesgo se está materializando, y con qué frecuencia.

### Gestión — si ocurre

El plan de contingencia: qué se hace concretamente.

## Las cuatro estrategias de respuesta

| Estrategia | Qué significa | Cuándo se usa |
|---|---|---|
| **Evitar** | Cambiar el plan para que el riesgo no aplique | Cuando la exposición es inaceptable y hay alternativa |
| **Mitigar** | Reducir probabilidad o impacto | La más frecuente |
| **Transferir** | Pasar el riesgo a un tercero: seguro, contrato, proveedor | Cuando otro lo maneja mejor |
| **Aceptar** | No hacer nada, pero saberlo y registrarlo | Cuando mitigar cuesta más que la exposición |

Aceptar un riesgo **es** una decisión de gestión, siempre que sea explícita y esté documentada. Lo que no es aceptable es ignorarlo.

---

## Plan de RSGR del caso

### R1 — Datos de socios incompletos

| | |
|---|---|
| **Probabilidad × Impacto** | 70 % × 3 = 2,10 |
| **Estrategia** | Mitigar |
| **Reducción** | Auditar una muestra de 100 fichas en la semana 1, antes de diseñar la migración. Con el porcentaje real de incompletitud, dimensionar el trabajo de limpieza y ajustar la estimación. |
| **Supervisión** | Porcentaje de registros validados por semana durante la migración. Umbral de alerta: menos de 100 registros validados por semana. |
| **Contingencia** | Migrar solo los socios activos —unos 300 de 800— y dejar el histórico para una segunda etapa. Reduce el trabajo un 60 % conservando la funcionalidad operativa. |
| **Responsable** | Analista |

### R2 — Referente sin disponibilidad

| | |
|---|---|
| **Probabilidad × Impacto** | 50 % × 3 = 1,50 |
| **Estrategia** | Mitigar |
| **Reducción** | Acordar por escrito con la comisión directiva la designación del referente y sus 4 horas semanales, con día y horario fijos, antes de iniciar. |
| **Supervisión** | Registro de horas efectivas de reunión por semana. Alerta: dos semanas consecutivas por debajo de 2 horas. |
| **Contingencia** | Escalar a la comisión directiva por escrito, con el listado de decisiones pendientes y su impacto en el cronograma. |
| **Responsable** | Líder de proyecto |

### R3 — Conocimiento concentrado en una persona

| | |
|---|---|
| **Probabilidad × Impacto** | 30 % × 4 = 1,20 |
| **Estrategia** | Mitigar |
| **Reducción** | Documentar el circuito administrativo completo en la semana 2, validado por escrito. Entrevistar además a un segundo empleado. |
| **Supervisión** | Estado del documento de circuito administrativo: completo y validado, sí o no. |
| **Contingencia** | Trabajar con el documento validado y consultar a la comisión directiva las decisiones que el documento no cubra. |
| **Responsable** | Analista |

### R6 — El personal no adopta el sistema

| | |
|---|---|
| **Probabilidad × Impacto** | 30 % × 4 = 1,20 |
| **Estrategia** | Mitigar |
| **Reducción** | Involucrar a la administrativa en el diseño de las pantallas desde el inicio. Capacitación antes de la puesta en producción, no después. Período de uso en paralelo de dos semanas. |
| **Supervisión** | Cantidad de operaciones registradas en el sistema por semana tras la puesta en producción. Alerta: menos del 70 % de las operaciones esperadas. |
| **Contingencia** | Sesiones de acompañamiento en el puesto de trabajo y ajuste de las pantallas que generan rechazo. |
| **Responsable** | Analista |

### R5 — Pedidos de funcionalidad nueva

| | |
|---|---|
| **Probabilidad × Impacto** | 70 % × 2 = 1,40 |
| **Estrategia** | Mitigar |
| **Reducción** | Aplicar el procedimiento de gestión de cambios de la Unidad 5: registrar todo pedido, evaluar impacto e informarlo antes de aceptar. |
| **Supervisión** | Cantidad de pedidos registrados y esfuerzo acumulado que representan. |
| **Contingencia** | Presentar a la comisión la suma acumulada de los pedidos con su impacto en plazo, para que priorice. |
| **Responsable** | Líder de proyecto |

### R8 — Cambio de comisión directiva

| | |
|---|---|
| **Probabilidad × Impacto** | 10 % × 4 = 0,40 |
| **Estrategia** | **Aceptar** |
| **Fundamento** | La exposición es baja y no hay acción de mitigación al alcance del equipo. Se registra y se revisa si se convoca a elecciones. |
| **Supervisión** | Convocatoria a elecciones en el club. |
| **Responsable** | Líder de proyecto |

---

# Seguimiento de riesgos

Un plan de RSGR escrito al inicio y nunca revisado no sirve de nada.

## Qué se revisa en cada corte de control

| Pregunta | Acción |
|---|---|
| ¿Cambió la probabilidad de algún riesgo? | Recalcular exposición y reordenar |
| ¿Algún indicador de supervisión cruzó su umbral? | Activar la contingencia |
| ¿Aparecieron riesgos nuevos? | Incorporarlos a la matriz |
| ¿Algún riesgo dejó de aplicar? | Cerrarlo, dejando registro |
| ¿Algún riesgo se materializó? | Pasó a ser problema: se gestiona y se registra qué falló en la anticipación |

## Los riesgos cerrados también informan

Cuando un riesgo se cierra sin haberse materializado, conviene anotar por qué: si fue porque la mitigación funcionó o porque nunca fue un riesgo real.

Esa distinción, acumulada entre proyectos, mejora la identificación futura. Es una **métrica del proceso**, en el sentido de la Unidad 7.

---

# La dimensión ética

## El riesgo conocido y no comunicado

Es el caso más grave de esta unidad.

Un analista detecta un riesgo con impacto crítico y no lo informa: porque complica la aprobación del proyecto, porque preocuparía al cliente, o porque espera que no ocurra.

Si el riesgo se materializa, la organización sufre una consecuencia que podría haber previsto y decidido.

**La decisión profesional:** todo riesgo identificado con impacto crítico o catastrófico se informa, incluso cuando su probabilidad es baja y aunque comprometa la aprobación del proyecto.

## Registrar un riesgo como aceptado sin decirlo

Aceptar un riesgo es legítimo. Aceptarlo **sin informar a la organización** no lo es, porque la decisión de aceptar un riesgo del negocio le corresponde a la organización, no al equipo técnico.

## Subestimar la probabilidad para que el proyecto cierre

Es el equivalente, en riesgos, de estimar por debajo. Ajustar las probabilidades hasta que la matriz se vea aceptable falsea el instrumento.

> Un informe de riesgos que solo contiene riesgos menores no es un informe tranquilizador: es un informe que no se hizo.

---

# Errores frecuentes

- **Confundir riesgo con problema**, y gestionar solo lo que ya pasó.
- **Enunciar riesgos vagos** que no se pueden supervisar ni mitigar.
- **Ignorar riesgos de probabilidad baja e impacto catastrófico.**
- **No revisar la matriz** durante el proyecto.
- **No definir indicador de supervisión**, con lo que nadie sabe cuándo activar la contingencia.
- **Confundir mitigación con contingencia**: la primera es antes, la segunda es después.
- **Aceptar riesgos de forma implícita**, sin registrarlo ni informarlo.
- **Omitir los riesgos de negocio**, que son los que más proyectos inutilizan.
- **No usar el FODA ni los supuestos del alcance** como fuente de riesgos.

---

# Buenas prácticas

✔ Enunciar cada riesgo como "que ocurra X, y como consecuencia Y".

✔ Derivar riesgos de los supuestos del alcance y del FODA.

✔ Cuantificar el impacto en días o en dinero cuando sea posible.

✔ Mitigar cuando el costo de mitigar es menor que la exposición.

✔ Definir un indicador de supervisión por riesgo, con umbral.

✔ Revisar la matriz en cada corte de control.

✔ Documentar los riesgos aceptados y comunicarlos.

✔ Informar todo riesgo de impacto crítico o catastrófico.

---

# Caso de estudio

## El riesgo que nadie quiso ver

Un equipo desarrolló durante siete meses un sistema de turnos para un centro médico. En la puesta en producción, el sistema funcionó correctamente.

Tres meses después, el centro seguía usando la agenda de papel.

Del relevamiento posterior surgió que:

- El sistema requería que las recepcionistas cargaran el turno mientras hablaban por teléfono con el paciente.
- La carga tomaba unos 90 segundos; anotar en la agenda tomaba 15.
- Nadie había medido cuánto tardaba el proceso anterior.
- La capacitación se dio una semana después de la puesta en producción.
- Durante el proyecto, el referente había sido el administrador del centro, que nunca atendió un teléfono.
- Dos recepcionistas habían planteado su preocupación en una reunión; quedó registrado como "resistencia al cambio".

### Para analizar

1. ¿Qué riesgo se materializó? Enúncielo correctamente y clasifíquelo por categoría.
2. ¿Cuál habría sido su probabilidad e impacto si se lo hubiera identificado al inicio?
3. ¿Qué acción de reducción lo habría evitado, y en qué momento del proyecto?
4. ¿Qué indicador de supervisión habría detectado el problema antes de los tres meses?
5. ¿Qué error se cometió al interpretar el planteo de las recepcionistas?
6. ¿Qué relación tiene este caso con la viabilidad operativa de la Unidad 9?
7. ¿Qué error de elección de referente se cometió, y qué dice al respecto la Unidad 11?

---

# Aplicación profesional

Cada grupo entrega el **plan de RSGR** de su proyecto:

- matriz de riesgos con un mínimo de ocho riesgos, al menos dos por cada una de las cuatro categorías;
- cada riesgo enunciado en la forma "que ocurra X, y como consecuencia Y";
- probabilidad, impacto y exposición de cada uno;
- para los cuatro de mayor exposición, el plan completo: estrategia, reducción, indicador de supervisión con umbral, contingencia y responsable;
- los riesgos aceptados, con su fundamento explícito;
- indicación de qué riesgos derivan del FODA de la Unidad 4 y qué riesgos derivan de los supuestos del alcance de la Unidad 5.

La matriz se revisa en el corte de control siguiente, y esa revisión también se entrega.

---

# Resumen

En esta unidad aprendimos que:

- Un riesgo es un problema que todavía no pasó; un problema es un riesgo que no se gestionó.
- Todo riesgo tiene probabilidad e impacto, y se prioriza por su producto: la exposición.
- Las cuatro categorías son técnicos, de proyecto, de negocio y de personal.
- Los supuestos del alcance y el cuadrante de amenazas del FODA ya son una lista de riesgos.
- Un riesgo mal enunciado no se puede gestionar: la forma útil es "que ocurra X, y como consecuencia Y".
- Conviene mitigar cuando el costo de mitigar es menor que la exposición.
- RSGR define, para cada riesgo, la reducción antes, la supervisión durante y la contingencia después.
- Las cuatro estrategias son evitar, mitigar, transferir y aceptar.
- Aceptar un riesgo es una decisión de gestión válida, siempre que sea explícita, documentada e informada.
- Un riesgo conocido y no comunicado deja de ser un riesgo del proyecto y pasa a ser responsabilidad de quien lo calló.

---

# Actividad práctica

## Plan de RSGR

**1. Identificación**

Identifiquen un mínimo de ocho riesgos de su proyecto, al menos dos por categoría. Indiquen de dónde salió cada uno: FODA, supuestos del alcance, experiencia o consulta al equipo.

**2. Enunciado**

Reescriban cada riesgo en la forma "que ocurra X, y como consecuencia Y".

**3. Proyección**

Asignen probabilidad e impacto con las escalas de la unidad. Calculen la exposición y ordenen.

**4. Matriz gráfica**

Ubiquen los riesgos en la matriz de probabilidad por impacto.

**5. Plan de RSGR**

Para los cuatro de mayor exposición, completen: estrategia, acciones de reducción con su momento, indicador de supervisión con umbral y frecuencia, plan de contingencia y responsable.

**6. Riesgos aceptados**

Si aceptan algún riesgo, fundamenten por qué y cómo lo informarían a la organización.

**7. Análisis costo-mitigación**

Elijan un riesgo y estimen el costo de mitigarlo. Compárelo con su exposición y concluya si conviene mitigarlo.

**Formato de entrega:** informe técnico con la matriz y las fichas de RSGR.

---

# Preguntas de repaso

1. ¿Cuál es la diferencia entre un riesgo y un problema?

2. Nombre las cuatro categorías de riesgo con un ejemplo de cada una.

3. ¿Por qué un riesgo de probabilidad baja e impacto catastrófico no puede ignorarse?

4. Escriba la fórmula de exposición al riesgo y explique para qué sirve.

5. ¿Cuál es el criterio para decidir si conviene mitigar un riesgo?

6. ¿Qué significan las tres letras de RSGR?

7. ¿Qué diferencia hay entre una acción de reducción y un plan de contingencia?

8. Nombre las cuatro estrategias de respuesta e indique cuándo se usa cada una.

9. ¿En qué condiciones aceptar un riesgo es una decisión profesional válida?

10. ¿Por qué un informe de riesgos que solo contiene riesgos menores es un informe que no se hizo?

---

# Bibliografía

- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Capítulo sobre gestión del riesgo y el plan RSGR.
- Sommerville, I. *Ingeniería del Software.* Sección sobre gestión de riesgos.
- [SEI (Carnegie Mellon) — Risk Management](https://www.sei.cmu.edu/our-work/risk-management/)
- Project Management Institute. [*Guía PMBOK*](https://www.pmi.org/standards/pmbok). Área de Gestión de los Riesgos. _(acceso pago)_

---

**Fin de la Unidad 12**
