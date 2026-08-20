# Unidad 15
# Entrega, entrenamiento y mantenimiento

> "El día que el sistema entra en producción no termina el proyecto: empieza la etapa más larga y más cara del ciclo de vida."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Planificar la entrega y la puesta en producción de un sistema.
- Diseñar el entrenamiento de los usuarios y la transferencia de conocimiento.
- Comprender el mantenimiento como etapa del ciclo de vida.
- Distinguir los cuatro tipos de mantenimiento.
- Aplicar métricas de mantenimiento.
- Reconocer el peso del mantenimiento en el costo total del sistema.

---

# La entrega

## Qué es poner en producción

Poner en producción es que el sistema pase a ser **el sistema que la organización usa** para trabajar.

Es un cambio en la organización, no un evento técnico. Y por eso falla por razones que no son técnicas.

## Qué incluye una entrega

| Componente | Contenido |
|---|---|
| **Sistema instalado** | Funcionando en el ambiente definitivo |
| **Datos migrados** | La información anterior, cargada y verificada |
| **Documentación** | Manual de usuario, documentación técnica, informe final |
| **Capacitación** | Realizada antes de la puesta en producción |
| **Soporte inicial** | Acompañamiento durante los primeros días |
| **Transferencia** | A quien vaya a mantener el sistema |

Una entrega que solo incluye el primer punto no es una entrega: es una instalación.

## Estrategias de puesta en producción

| Estrategia | Cómo funciona | Riesgo |
|---|---|---|
| **Directa** | El sistema viejo se apaga y el nuevo arranca | Alto: si algo falla, no hay a dónde volver |
| **En paralelo** | Ambos sistemas funcionan a la vez durante un período | Bajo, pero duplica el trabajo del usuario |
| **Por etapas** | Se van habilitando módulos de a uno | Bajo, pero la transición dura más |
| **Piloto** | Se arranca con un sector o un grupo reducido | Bajo, y permite corregir antes de extender |

Para el sistema del club, la estrategia razonable es **en paralelo durante dos semanas**: es el mecanismo de contingencia del riesgo R6 que definimos en la Unidad 12.

## La migración de datos

Es la parte de la entrega que más problemas produce y la que peor se estima.

| Paso | Qué se hace |
|---|---|
| 1 | Auditar la calidad de los datos existentes |
| 2 | Definir las reglas de transformación |
| 3 | Limpiar y normalizar |
| 4 | Migrar a un ambiente de prueba |
| 5 | **Verificar** contra el origen |
| 6 | Migrar a producción |
| 7 | Verificar de nuevo |

El paso 5 es el que se omite. Migrar sin verificar significa que la organización descubre los errores usando el sistema, y con datos ya operativos.

> El riesgo R1 de la Unidad 12 —datos de socios incompletos— es exactamente este problema, anticipado con nueve meses de antelación.

## Criterios de aceptación

La entrega se acepta o se rechaza contra los **criterios de aceptación** definidos en el documento de alcance de la Unidad 5.

Si esos criterios no se escribieron, la aceptación se convierte en una negociación sobre impresiones, y la organización siempre encuentra algo que falta.

---

# Entrenamiento

## Por qué es parte del proyecto

De la Unidad 9: la **viabilidad operativa** es la dimensión que más proyectos técnicamente correctos hace fracasar.

El entrenamiento es el instrumento principal para asegurarla. Un sistema que los usuarios no saben usar no está entregado.

## Cuándo capacitar

**Antes de la puesta en producción.** No después.

Capacitar después significa que durante los primeros días —los que definen si el sistema se adopta o se rechaza— la gente usa un sistema que no entiende. La primera impresión de un sistema difícil no se revierte con una capacitación posterior.

## Cómo diseñar la capacitación

Aplica el análisis del destinatario de la Unidad 2: hay públicos distintos y necesitan cosas distintas.

| Público | Qué necesita | Formato |
|---|---|---|
| **Usuario operativo** | Cómo hacer su trabajo cotidiano con el sistema | Práctica guiada sobre su propio puesto |
| **Usuario ocasional** | Cómo hacer las dos o tres cosas que hace | Guía rápida de una página |
| **Responsable / supervisor** | Cómo obtener información y controlar | Recorrido por los reportes |
| **Quien mantendrá el sistema** | Cómo está construido y cómo se interviene | Documentación técnica y sesión de transferencia |

## Qué funciona y qué no

| ❌ | ✅ |
|---|---|
| Explicar todas las funciones del sistema | Enseñar las tareas que la persona hace |
| Una sesión larga única | Sesiones cortas, con práctica entre ellas |
| Capacitar con datos de ejemplo | Capacitar con datos reales de la organización |
| Manual de 60 páginas | Guía rápida de una página, más el manual como referencia |
| El capacitador maneja la computadora | El usuario maneja la computadora |

> El último punto es determinante. Una persona que vio hacer algo no aprendió a hacerlo.

## Transferencia de conocimiento

Cuando el proyecto termina, el equipo se va. Alguien tiene que poder mantener el sistema.

La transferencia incluye:

- documentación técnica actualizada;
- acceso al repositorio y a las credenciales;
- explicación de las decisiones de diseño y su fundamento;
- registro de los defectos conocidos y no corregidos;
- lista de los puntos frágiles del sistema.

Los dos últimos son los que nunca se transfieren, y son los que la persona que hereda el sistema más necesita.

> Entregar un sistema sin transferir a quién lo mantiene es dejar a la organización con un activo que no puede sostener. En la Unidad 9, ese fue el punto que hizo inviable el proyecto de la biblioteca.

---

# El mantenimiento

## El dato que cambia la perspectiva

Sobre el ciclo de vida completo de un sistema, el mantenimiento suele consumir **entre el 60 % y el 80 % del costo total**.

Es decir: construir el sistema es la parte menor del gasto.

| Etapa | Proporción del costo total del ciclo de vida |
|---|---|
| Desarrollo inicial | 20 – 40 % |
| Mantenimiento | 60 – 80 % |

Esto tiene dos consecuencias inmediatas:

1. **Un presupuesto que solo contempla el desarrollo informa menos de la mitad del costo real.** Es lo que vimos en la Unidad 9.
2. **Las decisiones que facilitan el mantenimiento tienen un retorno mucho mayor que las que aceleran el desarrollo.** Es lo que justifica los estándares de la Unidad 14.

## Evolución del software

Un sistema en uso cambia siempre, por razones que no son defectos:

- la organización cambia sus procesos;
- aparece normativa nueva;
- crece el volumen de operaciones;
- cambia la tecnología del entorno;
- los usuarios descubren necesidades que no habían planteado.

> Un sistema que no cambia es un sistema que nadie usa.

---

# Los cuatro tipos de mantenimiento

| Tipo | Qué resuelve | Se origina en |
|---|---|---|
| **Correctivo** | Defectos | Fallas detectadas |
| **Adaptativo** | Cambios del entorno | Normativa, tecnología, integraciones |
| **Perfectivo** | Mejoras y funcionalidad nueva | Pedidos de los usuarios |
| **Preventivo** | Deterioro de la mantenibilidad | Iniciativa del equipo técnico |

## Correctivo

Corrige defectos que se manifestaron en uso.

*Ejemplo:* el cálculo de deuda no considera los pagos parciales.

Es el que la organización espera y el único que suele estar previsto. Sin embargo, es **el menor de los cuatro** en volumen: representa alrededor del 20 % del esfuerzo de mantenimiento.

## Adaptativo

Adapta el sistema a cambios de su entorno, sin agregar funcionalidad.

*Ejemplo:* el sistema contable cambió el formato de importación y hay que ajustar la exportación.

Es inevitable y no depende de la calidad del sistema. Depende del mundo.

## Perfectivo

Agrega funcionalidad o mejora la existente a pedido de los usuarios.

*Ejemplo:* que el listado de morosos se pueda filtrar por actividad.

**Es el mayor de los cuatro**, entre el 50 % y el 60 % del esfuerzo de mantenimiento. Y es una buena señal: significa que el sistema se usa y que los usuarios quieren más.

## Preventivo

Mejora la estructura interna del sistema para que siga siendo mantenible, sin cambiar lo que hace.

*Ejemplo:* reorganizar el módulo de pagos, que se volvió difícil de modificar tras seis cambios sucesivos.

Es el que nunca se aprueba, porque desde afuera **no se ve nada**. Y es el que evita que el sistema llegue a un estado en el que cualquier cambio es riesgoso.

> Argumentar el mantenimiento preventivo ante una organización es una tarea de comunicación, no técnica: hay que explicar en términos de costo futuro algo que hoy no produce ningún cambio visible.

## Proporciones de referencia

| Tipo | Proporción del esfuerzo de mantenimiento |
|---|---|
| Perfectivo | 50 – 60 % |
| Adaptativo | 20 – 25 % |
| Correctivo | ~20 % |
| Preventivo | ~5 % |

El dato relevante: **la mayor parte del mantenimiento no es arreglar cosas rotas**. Es hacer evolucionar un sistema que funciona.

---

# Métricas del mantenimiento

| Métrica | Qué informa |
|---|---|
| Tiempo medio de respuesta | Cuánto tarda en atenderse un pedido |
| Tiempo medio de resolución | Cuánto tarda en resolverse |
| Cantidad de pedidos por tipo | Distribución entre los cuatro tipos |
| Esfuerzo por tipo | Dónde se consume el tiempo |
| Tasa de reapertura | Correcciones que no corrigieron |
| Costo de mantenimiento anual | Como porcentaje del desarrollo inicial |
| Cantidad de módulos tocados por cambio | Indicador de acoplamiento |

## Las dos que dan la alerta temprana

**Tasa de reapertura alta** indica que se está corrigiendo el síntoma y no la causa. Es la misma señal de la Unidad 14.

**Cantidad de módulos tocados por cambio, en aumento**, indica que el sistema se está volviendo difícil de modificar. Cuando un cambio chico obliga a tocar seis módulos, el sistema está pidiendo mantenimiento preventivo.

> Estas métricas son del proceso, en el sentido de la Unidad 7: se acumulan a lo largo de años y sirven para decidir cuándo conviene rehacer un sistema en lugar de seguir manteniéndolo.

## Cuándo conviene reemplazar en lugar de mantener

Señales:

- el costo anual de mantenimiento se acerca al de reconstruir;
- cada cambio introduce defectos nuevos;
- nadie en la organización entiende partes del sistema;
- la tecnología ya no tiene soporte;
- el sistema impide cambios que la organización necesita hacer.

Determinar esto es un análisis de viabilidad, con las herramientas de la Unidad 9.

---

# Errores frecuentes

- **Confundir instalar con entregar.**
- **Capacitar después** de la puesta en producción.
- **Migrar datos sin verificar** contra el origen.
- **Puesta en producción directa** sin posibilidad de volver atrás.
- **No definir criterios de aceptación**, y negociar la aceptación sobre impresiones.
- **No transferir** a quien va a mantener el sistema.
- **No informar los defectos conocidos** en la transferencia.
- **Presupuestar solo el desarrollo** y omitir el mantenimiento.
- **Suponer que el mantenimiento es corregir errores**, cuando la mayor parte es evolución.
- **No hacer nunca mantenimiento preventivo**, hasta que cualquier cambio se vuelve riesgoso.

---

# Buenas prácticas

✔ Planificar la entrega como un cambio en la organización, no como un evento técnico.

✔ Capacitar antes de la puesta en producción.

✔ Que el usuario maneje la computadora durante la capacitación.

✔ Verificar la migración contra el origen, dos veces.

✔ Elegir una estrategia de puesta en producción que permita volver atrás.

✔ Transferir incluyendo los defectos conocidos y los puntos frágiles.

✔ Informar el costo del ciclo de vida completo.

✔ Registrar el mantenimiento por tipo, para saber dónde se consume el esfuerzo.

✔ Argumentar el mantenimiento preventivo en términos de costo futuro.

---

# Caso de estudio

## Tres años después

El sistema del Club Deportivo San Martín se entregó hace tres años. Datos del período:

| Año | Pedidos correctivos | Adaptativos | Perfectivos | Preventivos | Esfuerzo total |
|---|---|---|---|---|---|
| 1 | 34 | 3 | 12 | 0 | 180 h |
| 2 | 18 | 5 | 26 | 0 | 240 h |
| 3 | 22 | 4 | 31 | 0 | 380 h |

Datos adicionales:

- El desarrollo inicial costó 32,6 persona-mes.
- La cantidad de módulos tocados por cambio pasó de 1,3 en el año 1 a 3,8 en el año 3.
- La tasa de reapertura pasó del 8 % al 24 %.
- Dos de los cuatro desarrolladores originales ya no están.
- La documentación técnica no se actualizó desde la entrega.
- El club creció de 800 a 1.400 socios.

### Para analizar

1. ¿Qué tipo de mantenimiento predomina? ¿Es una buena o una mala señal?
2. ¿Por qué el esfuerzo total creció un 111 % entre el año 1 y el año 3, si la cantidad de pedidos creció solo un 22 %?
3. ¿Qué indican los módulos tocados por cambio pasando de 1,3 a 3,8?
4. ¿Qué indica la tasa de reapertura del 24 %?
5. La columna de mantenimiento preventivo tiene ceros los tres años. ¿Qué relación tiene con las dos preguntas anteriores?
6. Calcule el costo de mantenimiento del año 3 como porcentaje del desarrollo inicial. ¿Es sostenible?
7. ¿Qué efecto tuvo que la documentación no se actualizara y que se fueran dos desarrolladores?
8. Redacte, en cinco líneas y en lenguaje no técnico, la recomendación que le haría a la comisión directiva.

---

# Aplicación profesional

Cada grupo entrega el **plan de entrega, entrenamiento y mantenimiento** de su proyecto:

- estrategia de puesta en producción elegida, con su fundamentación y su plan de vuelta atrás;
- plan de migración de datos, con los pasos de verificación;
- criterios de aceptación, tomados del documento de alcance de la Unidad 5;
- plan de capacitación, con un apartado por tipo de público;
- plan de transferencia, incluyendo qué documentación se entrega y a quién;
- estimación del costo anual de mantenimiento y su composición esperada por tipo;
- métricas de mantenimiento que se propondrían a la organización.

Este plan cierra el análisis de costos de la Unidad 9: sin el costo de mantenimiento, ese informe estaba incompleto.

---

# Resumen

En esta unidad aprendimos que:

- Poner en producción es un cambio en la organización, no un evento técnico.
- Una entrega incluye sistema, datos, documentación, capacitación, soporte y transferencia.
- La migración de datos requiere verificación contra el origen, y es el paso que se omite.
- La capacitación va antes de la puesta en producción, no después.
- En la capacitación, la computadora la maneja el usuario.
- La transferencia debe incluir los defectos conocidos y los puntos frágiles.
- El mantenimiento consume entre el 60 % y el 80 % del costo del ciclo de vida.
- Los cuatro tipos son correctivo, adaptativo, perfectivo y preventivo.
- El perfectivo es el mayor: la mayor parte del mantenimiento es evolución, no reparación.
- El preventivo es el que nunca se aprueba porque no se ve, y el que evita que el sistema se vuelva inmodificable.
- La tasa de reapertura y los módulos tocados por cambio son las alertas tempranas del deterioro.

---

# Actividad práctica

## Plan de entrega y mantenimiento

**1. Estrategia de puesta en producción**

Elijan una de las cuatro estrategias, fundamenten y describan el plan de vuelta atrás si algo falla.

**2. Migración**

Describan los siete pasos aplicados a los datos de su organización. Indiquen cómo van a verificar y contra qué.

**3. Criterios de aceptación**

Recuperen los criterios del documento de alcance. Si no eran verificables, reescríbanlos ahora.

**4. Plan de capacitación**

Para cada tipo de público de su organización: qué necesita aprender, en qué formato, cuánto tiempo y en qué momento.

**5. Guía rápida**

Redacten la guía rápida de una página para el usuario operativo. Debe cubrir solo las tareas que esa persona hace.

**6. Plan de transferencia**

Definan qué se entrega, a quién y en qué instancia. Incluyan el registro de defectos conocidos y la lista de puntos frágiles del proyecto.

**7. Costo de mantenimiento**

Estimen el costo anual de mantenimiento y su composición por tipo. Incorpórenlo al informe de viabilidad de la Unidad 9 y recalculen el período de recupero.

**Formato de entrega:** informe técnico, con la guía rápida como anexo separado.

---

# Preguntas de repaso

1. ¿Por qué poner en producción es un cambio organizacional y no un evento técnico?

2. Nombre los seis componentes de una entrega completa.

3. Compare las cuatro estrategias de puesta en producción por su riesgo.

4. ¿Cuál es el paso de la migración de datos que más se omite y qué consecuencia tiene?

5. ¿Por qué la capacitación debe darse antes de la puesta en producción?

6. ¿Por qué en la capacitación la computadora la debe manejar el usuario?

7. ¿Qué dos elementos de la transferencia nunca se transfieren y por qué son los más necesarios?

8. ¿Qué proporción del costo del ciclo de vida corresponde al mantenimiento, y qué dos consecuencias tiene?

9. Nombre los cuatro tipos de mantenimiento y ordénelos por volumen de esfuerzo.

10. ¿Por qué el mantenimiento preventivo es el que nunca se aprueba?

11. ¿Qué indica un aumento en la cantidad de módulos tocados por cambio?

---

# Bibliografía

- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Capítulos sobre mantenimiento y reingeniería.
- Sommerville, I. *Ingeniería del Software.* Capítulo sobre evolución del software.
- [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) — registro de cambios entre versiones entregadas.
- [Write the Docs — Guía de documentación](https://www.writethedocs.org/guide/) — para el material de capacitación y transferencia.

---

**Fin de la Unidad 15**
