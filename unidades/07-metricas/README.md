# Unidad 7
# Métricas del proceso y del proyecto

> "Lo que no se mide no se puede controlar. Lo que se mide mal se controla peor que si no se midiera."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Explicar para qué se mide en un proyecto de software.
- Distinguir métricas del proceso de métricas del proyecto.
- Aplicar métricas orientadas al tamaño y reconocer sus límites.
- **Calcular puntos función** sobre un caso concreto.
- Comprender las métricas orientadas a casos de uso.
- Recopilar, calcular y evaluar métricas.
- Interpretar desvíos y reconocer el riesgo de gestionar para el indicador.

> **Articulación.** El tratamiento estadístico de los datos recopilados —promedios, dispersión, tendencias— corresponde a **Estadística**, cursada en paralelo.

---

# Para qué se mide

Un proyecto sin métricas se conduce por impresiones.

> "¿Cómo vamos?"
>
> "Bien, bastante avanzado."

Esa respuesta no permite decidir nada. No dice si hay que pedir más tiempo, sumar gente o recortar alcance.

Medir sirve para cuatro cosas concretas:

| Propósito | Qué permite |
|---|---|
| **Comprender** | Saber cuánto trabajo hay realmente |
| **Controlar** | Detectar desvíos mientras hay margen para corregirlos |
| **Mejorar** | Aprender de un proyecto para estimar mejor el siguiente |
| **Comunicar** | Informar el estado con datos verificables en lugar de percepciones |

---

# Clasificación de las métricas

## Métricas del proceso

Se recopilan **a lo largo de muchos proyectos y durante períodos largos**, y sirven para mejorar la forma de trabajar de la organización.

No se usan para controlar el proyecto en curso: se usan para que el próximo salga mejor.

*Ejemplos:* productividad promedio de la organización, tasa de defectos por punto función, tiempo promedio de corrección de un error, porcentaje de proyectos entregados en fecha.

## Métricas del proyecto

Se recopilan **dentro de un proyecto** y sirven para conducirlo.

Tienen dos usos: evaluar el estado actual y ajustar las estimaciones de lo que falta.

*Ejemplos:* tareas completadas sobre planificadas, esfuerzo consumido, desvío de cronograma, defectos abiertos, cambios de alcance solicitados.

## La diferencia importa

| | Proceso | Proyecto |
|---|---|---|
| **Horizonte** | Varios proyectos, años | Un proyecto |
| **Para qué** | Mejorar cómo trabaja la organización | Controlar y ajustar este proyecto |
| **Quién la usa** | La dirección | El líder de proyecto |
| **Cuándo se evalúa** | Al cerrar proyectos | Durante el proyecto |

Usar una métrica de proceso para evaluar a una persona en un proyecto es uno de los errores más dañinos que puede cometer una organización: convierte el instrumento de mejora en un instrumento de control personal, y a partir de ahí los datos dejan de ser confiables.

---

# Métricas orientadas al tamaño

Miden el tamaño del producto en **líneas de código** (LDC, o KLDC para miles).

A partir del tamaño se derivan indicadores:

| Métrica derivada | Cálculo |
|---|---|
| Productividad | KLDC / persona-mes |
| Calidad | defectos / KLDC |
| Costo unitario | $ / KLDC |
| Densidad de documentación | páginas de documentación / KLDC |

## Ventajas

- Fácil de medir: se cuenta automáticamente.
- Disponible en cualquier proyecto ya construido.
- Útil para comparar proyectos de la misma organización y el mismo lenguaje.

## Límites

- **Depende del lenguaje.** La misma funcionalidad requiere muchas más líneas en un lenguaje que en otro.
- **Penaliza el buen código.** Un desarrollador que resuelve algo en 20 líneas aparece como menos productivo que uno que necesita 200.
- **No sirve para estimar al inicio**, porque en la etapa de análisis nadie sabe cuántas líneas va a tener el sistema.
- **Es fácil de inflar** si se la usa para evaluar personas.

> Las líneas de código miden el esfuerzo de construcción, no el valor entregado. Son útiles como dato histórico y peligrosas como objetivo.

---

# Métricas orientadas a la función: puntos función

Los **puntos función (PF)** miden el tamaño del sistema por su **funcionalidad**, no por su implementación.

Su ventaja decisiva: **se pueden calcular en la etapa de análisis**, cuando todavía no existe una línea de código. Por eso son la métrica que sirve para estimar.

## Los cinco parámetros del dominio de información

| Parámetro | Qué se cuenta |
|---|---|
| **Entradas de usuario** | Datos distintos que el usuario aporta al sistema |
| **Salidas de usuario** | Informes, pantallas y mensajes que el sistema produce |
| **Consultas de usuario** | Interacciones en línea que producen una respuesta inmediata sin actualizar datos |
| **Archivos lógicos internos** | Agrupamientos lógicos de datos que el sistema mantiene |
| **Interfaces externas** | Archivos o datos que se intercambian con otros sistemas |

## Factores de ponderación

Cada parámetro se cuenta y se clasifica según su complejidad.

| Parámetro | Simple | Medio | Complejo |
|---|---|---|---|
| Entradas de usuario | 3 | 4 | 6 |
| Salidas de usuario | 4 | 5 | 7 |
| Consultas de usuario | 3 | 4 | 6 |
| Archivos lógicos internos | 7 | 10 | 15 |
| Interfaces externas | 5 | 7 | 10 |

La suma de cuenta × peso da la **cuenta total**.

## El factor de ajuste

La cuenta total se corrige según catorce **factores de complejidad**, cada uno valorado de **0** (sin influencia) a **5** (esencial):

1. ¿Requiere el sistema copias de seguridad y recuperación confiables?
2. ¿Se requieren comunicaciones de datos especializadas?
3. ¿Existen funciones de procesamiento distribuido?
4. ¿Es crítico el rendimiento?
5. ¿Se ejecutará en un entorno operativo existente y fuertemente utilizado?
6. ¿Requiere entrada de datos interactiva?
7. ¿La entrada interactiva requiere transacciones sobre múltiples pantallas u operaciones?
8. ¿Se actualizan los archivos maestros de forma interactiva?
9. ¿Son complejas las entradas, salidas, archivos o consultas?
10. ¿Es complejo el procesamiento interno?
11. ¿Se diseñó el código para ser reutilizable?
12. ¿Están incluidas la conversión y la instalación en el diseño?
13. ¿Se diseñó el sistema para soportar múltiples instalaciones en distintas organizaciones?
14. ¿Se diseñó la aplicación para facilitar los cambios y el uso por parte del usuario?

## La fórmula

```
PF = cuenta total × [ 0,65 + 0,01 × Σ Fi ]
```

Como cada uno de los 14 factores va de 0 a 5, la sumatoria va de 0 a 70, y el multiplicador queda entre **0,65** y **1,35**.

Es decir: el ajuste por complejidad puede reducir el tamaño hasta un 35 % o aumentarlo hasta un 35 %.

---

## Cálculo completo: Club Deportivo San Martín

Sistema de registro de socios, control de cuotas y gestión de actividades.

### Paso 1 — Contar y ponderar

| Parámetro | Cuenta | Complejidad | Peso | Subtotal |
|---|---|---|---|---|
| Entradas de usuario | 8 | Media | 4 | 32 |
| Salidas de usuario | 5 | Media | 5 | 25 |
| Consultas de usuario | 6 | Simple | 3 | 18 |
| Archivos lógicos internos | 4 | Media | 10 | 40 |
| Interfaces externas | 1 | Simple | 5 | 5 |
| | | | **Cuenta total** | **120** |

*Detalle de lo contado:*

- **Entradas (8):** alta de socio, modificación de socio, registro de pago, alta de actividad, inscripción a actividad, baja de socio, alta de usuario, registro de cuota mensual.
- **Salidas (5):** listado de socios con deuda, recibo de pago, informe de cobranza mensual, listado de inscriptos por actividad, estado de cuenta del socio.
- **Consultas (6):** buscar socio, consultar estado de cuenta, consultar cupo de actividad, consultar pagos de un socio, consultar actividades vigentes, consultar socios por actividad.
- **Archivos lógicos (4):** socios, pagos, actividades, inscripciones.
- **Interfaz externa (1):** exportación mensual al sistema contable.

### Paso 2 — Factor de ajuste

Valorados los catorce factores para este sistema, la sumatoria resulta **Σ Fi = 32**.

Es un valor intermedio, coherente con un sistema administrativo sin exigencias de rendimiento crítico ni procesamiento distribuido.

```
Factor = 0,65 + 0,01 × 32 = 0,97
```

### Paso 3 — Puntos función

```
PF = 120 × 0,97 = 116,4  ≈  116 puntos función
```

### Paso 4 — Métricas derivadas

Si la organización sabe, por su historia, que produce **10 PF por persona-mes**:

| Indicador | Cálculo | Resultado |
|---|---|---|
| Esfuerzo estimado | 116 PF ÷ 10 PF/persona-mes | ≈ 12 persona-mes |
| Costo, a $200.000 el persona-mes | 12 × 200.000 | $2.400.000 |
| Costo por punto función | 2.400.000 ÷ 116 | ≈ $20.700 |
| Defectos esperados, a 0,3 def/PF | 116 × 0,3 | ≈ 35 defectos |

Este es el mecanismo completo: del análisis funcional al esfuerzo, al costo y a la calidad esperada, **sin haber escrito código**.

> El dato de productividad (10 PF por persona-mes) es una métrica **del proceso**: sale del histórico de la organización. Sin histórico, hay que usar valores de referencia de la industria y declarar explícitamente que la estimación tiene mayor incertidumbre.

---

# Métricas orientadas a casos de uso

Cuando el sistema se especifica con casos de uso, se puede dimensionar directamente sobre ellos.

El procedimiento es análogo al de puntos función:

**1. Ponderar los actores.**

| Tipo de actor | Descripción | Peso |
|---|---|---|
| Simple | Otro sistema con interfaz definida | 1 |
| Medio | Otro sistema por protocolo, o persona con interfaz de texto | 2 |
| Complejo | Persona con interfaz gráfica | 3 |

**2. Ponderar los casos de uso** según la cantidad de transacciones que contienen.

| Tipo de caso de uso | Transacciones | Peso |
|---|---|---|
| Simple | hasta 3 | 5 |
| Medio | de 4 a 7 | 10 |
| Complejo | más de 7 | 15 |

**3. Sumar** el peso de actores y el de casos de uso para obtener los puntos de caso de uso sin ajustar, y aplicar después factores de complejidad técnica y de entorno.

## Ventaja y límite

La ventaja es que aprovecha la especificación que el equipo ya produjo, sin trabajo adicional de conteo.

El límite es que **depende de cómo se escribieron los casos de uso**: si un equipo escribe casos de uso muy grandes y otro los escribe finos, los tamaños medidos no son comparables.

---

# Recopilación, cálculo y evaluación

Medir es un proceso con tres etapas, y las tres se hacen mal con frecuencia.

## Recopilación

- Definir **antes** qué se va a medir y con qué frecuencia.
- Registrar en el momento, no reconstruir de memoria al cierre.
- Usar la misma definición siempre. Si "tarea completada" significa una cosa en marzo y otra en septiembre, la serie no sirve.
- Que registrar sea barato. Una métrica que cuesta más de un minuto por día se deja de registrar en dos semanas.

## Cálculo

- Aplicar la fórmula de manera consistente.
- Registrar el dato crudo además del indicador, para poder recalcular.
- No promediar promedios.

## Evaluación

Un número solo no dice nada. Un número necesita **referencia**:

| Tipo de referencia | Ejemplo |
|---|---|
| Contra el plan | 12 tareas completadas de 20 planificadas |
| Contra el período anterior | 8 defectos este mes, 14 el anterior |
| Contra el histórico de la organización | productividad 10 PF/persona-mes, promedio histórico 12 |
| Contra el tiempo transcurrido | 60 % del trabajo con 70 % del tiempo consumido |

La última comparación es la más útil para conducir un proyecto: cruza avance con consumo.

---

# Interpretación de desvíos

Un desvío no es un fracaso: es información.

| Situación | Lectura posible |
|---|---|
| Avance menor que tiempo consumido | Subestimación, o impedimentos no previstos |
| Avance mayor que tiempo consumido | Sobreestimación, o tareas más fáciles primero |
| Muchos defectos y avance rápido | Se está avanzando sacrificando calidad |
| Cero cambios de alcance en meses | Probablemente el cliente no está mirando |
| Todas las tareas al 90 % | Nadie está cerrando nada |

La última fila describe un fenómeno real: cuando el avance se autoinforma en porcentajes, todo tiende a quedar cerca del final sin llegar nunca. La respuesta es medir **tareas terminadas**, no porcentajes de tarea.

---

# El riesgo de gestionar para el indicador

Toda métrica que se convierte en objetivo deja de medir lo que medía.

| Si la métrica es… | El equipo aprende a… |
|---|---|
| Líneas de código escritas | Escribir más líneas de las necesarias |
| Tareas cerradas por semana | Partir las tareas en pedazos más chicos |
| Defectos reportados | Reportar menos defectos |
| Horas trabajadas | Estar más horas, no producir más |
| Porcentaje de avance | Informar avance optimista |

Esto no es mala fe: es la respuesta previsible a cómo se evalúa el trabajo.

## Cómo evitarlo

✔ Usar las métricas para **conducir el proyecto**, no para evaluar personas.

✔ Mirar varias métricas juntas: velocidad y calidad, avance y defectos.

✔ Cambiar el conjunto de métricas cuando dejan de informar.

✔ Explicar al equipo para qué se mide.

> Cuando un equipo entiende que las métricas sirven para pedir más tiempo con fundamento, las registra con honestidad. Cuando sospecha que sirven para evaluarlo, las maquilla.

---

# Errores frecuentes

- **Medir todo lo medible** en lugar de lo que sirve para decidir.
- **Usar métricas del proceso para evaluar personas.**
- **Estimar con líneas de código** en la etapa de análisis, donde el dato no existe.
- **Cambiar la definición de una métrica** a mitad del proyecto.
- **Reportar un número sin referencia.**
- **Medir avance en porcentajes autoinformados.**
- **No registrar el tiempo real**, con lo que se pierde el insumo para mejorar las estimaciones.
- **Presentar como certeza una estimación** basada en productividad de la industria y no de la organización.

---

# Buenas prácticas

✔ Definir las métricas antes de empezar a medir.

✔ Registrar en el momento y con bajo costo.

✔ Contar tareas terminadas, no porcentajes.

✔ Acompañar todo indicador con su referencia.

✔ Guardar el dato crudo además del indicador.

✔ Registrar estimado contra real, siempre.

✔ Declarar la incertidumbre cuando falta histórico propio.

---

# Caso de estudio

## Dos informes del mismo proyecto

Semana 8 de un proyecto de 12 semanas.

**Informe A**

> El proyecto avanza según lo previsto. El equipo está trabajando bien y ya se completó la mayor parte del desarrollo. Estimamos cumplir con la fecha de entrega.

**Informe B**

> Semana 8 de 12 (67 % del tiempo consumido).
>
> Tareas: 14 completadas de 26 planificadas (54 % de avance).
>
> Esfuerzo: 210 horas consumidas de 320 estimadas (66 %).
>
> Defectos: 11 abiertos, 3 de ellos bloqueantes.
>
> Cambios de alcance solicitados: 4, ninguno evaluado formalmente todavía.
>
> Desvío: el avance en tareas (54 %) está 13 puntos por debajo del tiempo consumido (67 %). Proyectado a la fecha de entrega, faltarían aproximadamente 2 semanas.
>
> Alternativas: extender 2 semanas, o dejar el módulo de reportes para una segunda etapa.

### Para analizar

1. ¿Qué decisiones permite tomar el informe B que el A no permite?
2. ¿Qué señal de alerta contiene el informe B además del atraso?
3. ¿Por qué el informe A no es necesariamente mentiroso, pero sí inútil?
4. ¿Qué métrica agregaría al informe B?
5. Si usted fuera la dirección de la organización, ¿qué preguntaría después de leer el informe B?

---

# Aplicación profesional

Cada grupo entrega el **informe de métricas** de su proyecto, que incluye:

- el cálculo de **puntos función** del sistema propuesto, con el detalle de lo contado y la valoración de los catorce factores;
- las métricas de proyecto definidas para el seguimiento, con su definición precisa y su frecuencia de medición;
- el estado actual de cada métrica con su referencia;
- la interpretación de los desvíos, si los hay.

El cálculo de puntos función es el insumo directo de la estimación de esfuerzo de la **Unidad 8** y del análisis de costos de la **Unidad 9**.

---

# Resumen

En esta unidad aprendimos que:

- Se mide para comprender, controlar, mejorar y comunicar.
- Las métricas del proceso mejoran la organización a lo largo de años; las del proyecto conducen el proyecto en curso.
- Las líneas de código son fáciles de medir, dependen del lenguaje y no sirven para estimar al inicio.
- Los puntos función miden funcionalidad y se pueden calcular en la etapa de análisis: son la métrica que permite estimar.
- La fórmula es PF = cuenta total × (0,65 + 0,01 × Σ Fi), con un ajuste de entre 0,65 y 1,35.
- Las métricas de casos de uso aprovechan la especificación existente pero dependen de cómo se la escribió.
- Un número sin referencia no informa nada.
- Toda métrica convertida en objetivo deja de medir lo que medía.

---

# Actividad práctica

## Dimensionamiento del proyecto

**1. Conteo**

Identifiquen y listen los cinco parámetros del dominio de información de su sistema. Detallen cada elemento contado, no solo la cantidad.

**2. Ponderación**

Clasifiquen cada parámetro como simple, medio o complejo, justificando la clasificación en una línea.

**3. Factores de complejidad**

Valoren los catorce factores de 0 a 5 para su sistema. Justifiquen los tres que puntuaron más alto.

**4. Cálculo**

Calculen la cuenta total, el factor de ajuste y los puntos función. Muestren el cálculo.

**5. Métricas de seguimiento**

Definan cuatro métricas de proyecto. Para cada una: nombre, definición precisa, cómo se obtiene el dato, frecuencia y contra qué se compara.

**6. Análisis crítico**

Para cada métrica definida, indiquen qué comportamiento indeseado podría inducir si se la convirtiera en objetivo.

**Formato de entrega:** informe técnico con las tablas de cálculo.

---

# Preguntas de repaso

1. ¿Cuáles son los cuatro propósitos de medir en un proyecto?

2. ¿Qué diferencia hay entre una métrica del proceso y una del proyecto?

3. ¿Por qué las líneas de código no sirven para estimar en la etapa de análisis?

4. ¿Qué ventaja decisiva tienen los puntos función sobre las líneas de código?

5. Enuncie los cinco parámetros del dominio de información.

6. ¿Entre qué valores puede variar el factor de ajuste de los puntos función, y por qué?

7. ¿De qué depende la comparabilidad de las métricas orientadas a casos de uso?

8. ¿Por qué medir avance en porcentajes autoinformados produce tareas eternamente al 90 %?

9. Dé un ejemplo propio de una métrica que, convertida en objetivo, induzca un comportamiento indeseado.

---

# Bibliografía

- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Capítulos sobre métricas del proceso y del proyecto, y métricas orientadas a la función.
- Sommerville, I. *Ingeniería del Software.* Sección sobre medición del software.
- [IFPUG — International Function Point Users Group](https://www.ifpug.org/)
- Project Management Institute. [*Guía PMBOK*](https://www.pmi.org/standards/pmbok). _(acceso pago)_

---

**Fin de la Unidad 7**
