# Unidad 5
# El alcance del proyecto y las 4P

> "Un proyecto sin alcance definido no se termina: se abandona."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Definir el alcance de un proyecto indicando qué hará y qué no hará.
- Reconocer y corregir enunciados ambiguos.
- Redactar un documento de alcance que funcione como acuerdo con la organización.
- Analizar un proyecto con el marco de las 4P.
- Gestionar un pedido de cambio de alcance.

---

# El problema inicial

Dos equipos reciben el mismo encargo: *"un sistema para administrar el club"*.

Al cabo de tres meses, uno entregó registro de socios y control de cuotas. El otro entregó registro de socios, cuotas, turnos de canchas, carnets con código de barras y una aplicación para celulares.

Los dos cumplieron el encargo. El encargo era el problema.

**El alcance es lo que convierte un encargo en un proyecto.**

---

# Qué define el alcance

El alcance establece los límites del proyecto. Responde dos preguntas, y la segunda es tan importante como la primera:

- **¿Qué va a hacer el sistema?**
- **¿Qué NO va a hacer?**

La segunda pregunta es la que evita los conflictos. Lo que no está escrito como excluido, el cliente lo supone incluido.

## Características de un buen alcance

La consigna de la cátedra fija cuatro criterios:

| Criterio | Significa |
|---|---|
| **Claridad** | Se entiende sin necesidad de explicación oral |
| **Precisión** | No admite dos interpretaciones |
| **Límites** | Dice explícitamente qué queda afuera |
| **Lenguaje técnico simple** | Comprensible para el cliente, sin perder exactitud |

---

# La ambigüedad

Una frase ambigua en un documento de alcance es una discusión postergada.

## Ejemplos y corrección

| ❌ Ambiguo | Por qué | ✅ Preciso |
|---|---|---|
| "El sistema debe ser rápido" | No dice en qué operación ni comparado con qué | "La consulta de estado de cuenta debe responder en menos de 3 segundos con 50 usuarios simultáneos" |
| "El sistema avisará los vencimientos" | No dice a quién, por qué medio ni cuándo | "El sistema enviará un correo al socio 7 días antes del vencimiento de la cuota" |
| "Se podrán generar reportes" | No dice cuáles ni con qué datos | "El sistema generará tres reportes: socios con deuda, cobranza mensual y asistencia por actividad" |
| "El sistema será fácil de usar" | No es verificable | "Un usuario administrativo podrá registrar un socio nuevo sin consultar el manual, tras una capacitación de 30 minutos" |
| "Se integrará con el sistema contable" | No dice qué se integra ni en qué dirección | "El sistema exportará mensualmente un archivo CSV de cobranzas con el formato que requiere el sistema contable actual" |

## Las palabras que anticipan ambigüedad

Cuando aparecen estas palabras en un documento de alcance, conviene detenerse:

**rápido · fácil · amigable · flexible · eficiente · adecuado · óptimo · varios · algunos · etcétera · entre otros · si es necesario · en lo posible**

Ninguna es verificable. Todas van a significar cosas distintas para el cliente y para el equipo.

## La prueba de verificabilidad

Un enunciado de alcance está bien redactado si se puede responder esta pregunta:

> **¿Cómo verificaríamos, el día de la entrega, si esto se cumplió o no?**

Si no hay una forma objetiva de responderla, el enunciado hay que reescribirlo.

---

# El documento de alcance

## Qué contiene

| Sección | Contenido |
|---|---|
| **Objetivo** | Qué problema resuelve el proyecto, en una o dos oraciones |
| **Alcance incluido** | Funcionalidades y entregables comprometidos, enunciados de forma verificable |
| **Alcance excluido** | Lo que explícitamente NO forma parte |
| **Usuarios** | Quiénes van a usar el sistema y con qué rol |
| **Supuestos** | Lo que se asume verdadero y que, si cambia, altera el proyecto |
| **Restricciones** | Límites de tiempo, presupuesto, tecnología o normativa |
| **Entregables** | Productos concretos que se van a entregar |
| **Criterios de aceptación** | Cómo se va a verificar que está terminado |

## El apartado de exclusiones

Es el que más conflictos evita y el que más se omite.

Ejemplo, para el sistema del club:

> **No forma parte de este proyecto:**
>
> - la migración del histórico de pagos anterior a 2024;
> - la aplicación para teléfonos celulares;
> - la integración automática con el sistema contable;
> - la emisión de carnets con código de barras;
> - la capacitación del personal más allá de una jornada de 4 horas.

Nada impide que esas cosas se hagan después. Lo que el documento establece es que **no están incluidas en este acuerdo**.

## Los supuestos

Un supuesto es algo que el proyecto da por cierto sin controlarlo.

> - La organización designará un referente disponible al menos 4 horas semanales.
> - Los datos actuales de socios están completos en un 90 %.
> - El servidor será provisto por la organización antes de la semana 4.

Si un supuesto no se cumple, el alcance o el plazo cambian. Declararlos por escrito convierte un futuro reclamo en una conversación prevista.

## El alcance como acuerdo

Un documento de alcance no es documentación interna: es un **acuerdo con la organización**.

Por eso tiene que estar escrito en un lenguaje que el cliente pueda leer y aprobar, y tiene que estar efectivamente aprobado. Un alcance que el cliente nunca leyó no protege a nadie.

---

# Las 4P del proyecto

Definir el alcance responde *qué* se va a hacer. Falta el resto.

Las **4P** son un marco de análisis que ordena las cuatro dimensiones de todo proyecto de software.

| P | Dimensión | Pregunta central |
|---|---|---|
| 👥 **Personal** | Quiénes | ¿Quiénes trabajan, con qué roles y qué habilidades? |
| 🧩 **Producto** | Qué | ¿Qué se va a construir y qué lo caracteriza? |
| ⚙️ **Proceso** | Cómo | ¿Cómo se va a trabajar? ¿Con qué metodología? |
| 📁 **Proyecto** | Cuándo y con qué | ¿Cuánto tiempo hay, qué recursos y qué entregas? |

## Personal

Es la primera por una razón: es el factor que más influye en el resultado y el que más se subestima.

- ¿Quiénes integran el equipo?
- ¿Qué rol cumple cada uno y de qué responde?
- ¿Qué habilidades tiene el equipo y cuáles le faltan?
- ¿Quién es el referente en la organización y cuánta disponibilidad tiene?
- ¿Quién toma las decisiones cuando hay que decidir?

> Se desarrolla en la **Unidad 11 — Planificación organizativa del equipo**.

## Producto

- ¿Qué se va a construir?
- ¿Qué funciones cumple y para quién?
- ¿Qué lo distingue de lo que la organización ya tiene?
- ¿Qué tamaño y complejidad tiene?

> El dimensionamiento del producto se trabaja en la **Unidad 7 — Métricas**.

## Proceso

- ¿Metodología tradicional, ágil o híbrida?
- ¿Cómo se organiza el trabajo en el tiempo?
- ¿Cómo se validan los avances con la organización?
- ¿Cómo se tratan los cambios?

> La elección y su fundamentación se trabajaron en la **Unidad 3 — Metodologías**.

## Proyecto

- ¿Cuánto tiempo hay?
- ¿Qué recursos están disponibles?
- ¿Qué entregas y en qué fechas?
- ¿Cómo se controla el avance?

> Se desarrolla en las **Unidades 6 y 10**.

## Por qué el marco funciona

Las 4P obligan a mirar lo que se suele pasar por alto.

Un equipo que solo pensó el **Producto** tiene una buena idea sin forma de construirla. Uno que solo pensó el **Proyecto** tiene un cronograma que nadie puede cumplir. Uno que ignoró el **Personal** asigna tareas a personas que no tienen la habilidad ni el tiempo.

> Para hacer un sistema no alcanza con tener una buena idea.

---

# Gestión de cambios de alcance

El alcance se define al inicio, pero el proyecto ocurre después. Los pedidos de cambio son inevitables.

Lo que distingue un proyecto bien conducido no es la ausencia de cambios, sino tener un **procedimiento** para tratarlos.

## Procedimiento

| Paso | Qué se hace |
|---|---|
| 1. Registrar | El pedido se documenta por escrito, con quién lo pide y por qué |
| 2. Evaluar impacto | Qué efecto tiene sobre plazo, esfuerzo, costo y sobre lo ya construido |
| 3. Informar | Se comunica el impacto a quien pidió el cambio |
| 4. Decidir | La organización decide con el impacto sobre la mesa |
| 5. Actualizar | Si se aprueba, se actualiza el documento de alcance y el plan |

El paso 3 es el que se saltea. Aceptar un cambio sin informar su impacto es cargarlo al plazo original, y el plazo original se incumple.

## El deslizamiento del alcance

Ningún proyecto se desborda por un cambio grande. Se desborda por veinte cambios chicos que nadie registró.

> "Ya que estás, agregale un campo."
>
> "Sería bueno que también muestre el total."
>
> "Una pantallita más y quedamos."

Cada uno parece menor. Sumados explican la mayoría de los proyectos que no llegan.

La defensa no es negarse: es **registrar y evaluar cada pedido**, aunque sea chico. Cuando el cliente ve la suma acumulada, prioriza.

---

# Errores frecuentes

- **No escribir el apartado de exclusiones.**
- **Usar palabras no verificables** y descubrir su significado el día de la entrega.
- **No declarar los supuestos.**
- **Redactar el alcance en lenguaje técnico** que el cliente no puede leer ni aprobar.
- **No hacer aprobar el documento.**
- **Aceptar cambios sin evaluar el impacto.**
- **Analizar solo el Producto** y dar por resueltas las otras tres P.
- **Confundir alcance con lista de deseos:** todo lo que se enuncia hay que construirlo.

---

# Buenas prácticas

✔ Escribir qué queda afuera con el mismo cuidado que qué queda adentro.

✔ Aplicar la prueba de verificabilidad a cada enunciado.

✔ Declarar los supuestos por escrito.

✔ Hacer que el cliente lea y apruebe el documento.

✔ Registrar todo pedido de cambio, aunque parezca menor.

✔ Informar el impacto antes de aceptar un cambio.

✔ Analizar el proyecto con las cuatro P, no con una.

---

# Caso de estudio

## Revisión de un documento de alcance

Un equipo presentó este documento de alcance para el Club Deportivo San Martín.

> **Objetivo:** mejorar la gestión del club.
>
> **Alcance:** el sistema permitirá administrar socios, cobrar cuotas de forma eficiente, gestionar las actividades deportivas y generar reportes. Será fácil de usar y rápido. Se integrará con los sistemas existentes. Podrá usarse desde cualquier dispositivo.
>
> **Entregables:** el sistema funcionando.

### Para trabajar

1. Identifiquen todas las frases ambiguas. Hay al menos siete.
2. Reescriban cada una de forma verificable.
3. ¿Qué secciones obligatorias faltan?
4. Redacten el apartado de exclusiones que este documento debería tener.
5. Enuncien tres supuestos razonables para este proyecto.
6. ¿Qué conflicto concreto puede producir la frase "se integrará con los sistemas existentes"?

### Análisis con las 4P

Con los datos del diagnóstico de la Unidad 4, completen las cuatro dimensiones para este proyecto. Señalen qué información falta relevar en cada una.

---

# Aplicación profesional

Cada grupo entrega el **documento de alcance** de su proyecto y su **análisis con las 4P**.

El documento se revisa en dos instancias:

1. **Versión 1** — se redacta y se entrega.
2. **Revisión** — se detectan frases ambiguas y se reescriben. La versión 2 es la que se aprueba.

Esta doble instancia es deliberada: casi ningún documento de alcance sale bien la primera vez, y detectar la propia ambigüedad es la competencia que la actividad busca desarrollar.

El alcance aprobado es la base del plan de proyecto de la Unidad 6 y de la estimación de las Unidades 7 y 8.

---

# Resumen

En esta unidad aprendimos que:

- El alcance convierte un encargo en un proyecto, y debe decir tanto qué se hará como qué no.
- Un buen alcance es claro, preciso, con límites y en lenguaje técnico simple.
- Toda frase de alcance debe pasar la prueba de verificabilidad.
- Las palabras como "rápido", "fácil" o "flexible" anticipan conflicto.
- Los supuestos declarados convierten un futuro reclamo en una conversación prevista.
- El documento de alcance es un acuerdo, no documentación interna: hay que hacerlo aprobar.
- Las 4P —Personal, Producto, Proceso, Proyecto— ordenan las cuatro dimensiones del proyecto.
- Los cambios de alcance no se evitan: se registran, se evalúan y se informan antes de aceptarlos.

---

# Actividad práctica

## Documento de alcance y 4P

**Parte A — Documento de alcance**

Redacten el documento de alcance de su proyecto, con las ocho secciones. Requisitos:

- mínimo cinco enunciados de alcance incluido, todos verificables;
- mínimo cinco exclusiones explícitas;
- mínimo tres supuestos;
- criterios de aceptación para cada entregable.

**Parte B — Autorrevisión**

Sobre su propio documento: subrayen toda palabra no verificable y reescriban esos enunciados. Entreguen ambas versiones.

**Parte C — Análisis 4P**

Analicen el proyecto con las cuatro P. Para cada una, indiquen qué saben y qué necesitan averiguar.

**Formato de entrega:** documento, cuadro o presentación.

---

# Preguntas de repaso

1. ¿Por qué el apartado de exclusiones es tan importante como el de inclusiones?

2. Enuncie la prueba de verificabilidad y aplíquela a la frase "el sistema será confiable".

3. ¿Qué es un supuesto y para qué sirve declararlo?

4. ¿Por qué el documento de alcance debe estar en lenguaje que el cliente pueda leer?

5. Nombre las 4P e indique la pregunta central de cada una.

6. ¿Por qué el Personal es la primera de las 4P?

7. ¿Cuál es el paso que se saltea con más frecuencia al gestionar un cambio de alcance, y qué consecuencia tiene?

8. ¿Cómo se produce el deslizamiento del alcance y cómo se lo contiene?

---

# Bibliografía

- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Capítulo sobre las 4P y gestión del alcance.
- Sommerville, I. *Ingeniería del Software.* Capítulo sobre ingeniería de requerimientos.
- Project Management Institute. [*Guía PMBOK*](https://www.pmi.org/standards/pmbok). Área de Gestión del Alcance. _(acceso pago)_

---

**Fin de la Unidad 5**
