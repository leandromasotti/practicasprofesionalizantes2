# Unidad 11
# Planificación organizativa del equipo

> "Un proyecto de software no fracasa por falta de tecnología. Fracasa por cómo se organizó la gente que lo hizo."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Comprender la planificación organizativa como parte de la planificación del proyecto.
- Reconocer las estructuras de equipo y elegir una según el contexto.
- Asignar roles y responsabilidades de forma inequívoca.
- Explicar la relación entre tamaño del equipo, comunicación y productividad.
- Organizar la coordinación entre equipos.
- Identificar el lugar del analista en la conducción.

---

# Por qué el Personal es la primera de las 4P

En la Unidad 5 vimos que las 4P empiezan por **Personal**, y dijimos que el orden no es casual.

La razón es que es el factor que más determina el resultado y el que menos se planifica.

Un equipo bien organizado con tecnología modesta entrega. Un equipo desorganizado con la mejor tecnología disponible, no.

Pero mientras la tecnología se discute en detalle, la organización del equipo se resuelve con una frase: *"nos repartimos las tareas"*.

Esta unidad es sobre lo que hay que decidir en lugar de esa frase.

---

# Qué se planifica

La **planificación organizativa** responde cinco preguntas:

| Pregunta | Decisión |
|---|---|
| ¿Cuánta gente hace falta y cuándo? | Dimensionamiento |
| ¿Cómo se estructura el equipo? | Estructura |
| ¿Quién hace qué y de qué responde? | Roles |
| ¿Cómo se comunican? | Canales y rutinas |
| ¿Quién decide cuando hay que decidir? | Autoridad |

La última es la que más conflictos evita y la que más se omite.

---

# Dimensionamiento

De la Unidad 8: el proyecto del club requiere 32,6 persona-mes en 9,4 meses, lo que da unas 3,5 personas.

Ese número es un **promedio**, no una constante. La cantidad de gente necesaria varía a lo largo del proyecto.

| Etapa | Perfil predominante | Cantidad |
|---|---|---|
| Análisis | Analista | 1 – 2 |
| Diseño | Analista y arquitecto | 2 |
| Construcción | Desarrolladores | 3 – 4 |
| Pruebas | Desarrolladores y usuarios | 2 – 3 |
| Entrega y capacitación | Analista | 1 – 2 |

Planificar una dotación constante de 3,5 personas produce dos problemas simultáneos: gente sin trabajo al inicio y falta de gente en el pico de construcción.

> El perfil del equipo también cambia. Un proyecto no necesita las mismas habilidades en el mes 1 que en el mes 6.

---

# Estructuras de equipo

## Equipo con líder designado

Una persona conduce, asigna tareas y responde por el resultado.

**Cuándo conviene:** proyectos con plazos ajustados, equipos con poca experiencia, cuando hace falta una decisión rápida y única.

**Riesgo:** el líder se convierte en cuello de botella; si no está, nadie decide.

## Equipo democrático

Las decisiones se toman en conjunto. No hay una autoridad única.

**Cuándo conviene:** equipos chicos de personas con experiencia comparable, problemas donde el diseño se beneficia de discusión.

**Riesgo:** decisiones lentas y, en el peor caso, decisiones que nadie tomó.

## Equipo por especialidad

Cada integrante es responsable de un área: base de datos, interfaz, integraciones, pruebas.

**Cuándo conviene:** sistemas con partes técnicamente muy distintas.

**Riesgo:** dependencia crítica de cada persona. Si el responsable de base de datos falta dos semanas, esa parte se detiene.

## Equipo por funcionalidad

Cada subgrupo se hace cargo de una funcionalidad completa, de punta a punta.

**Cuándo conviene:** sistemas divisibles en módulos con poco acoplamiento.

**Riesgo:** decisiones técnicas divergentes entre subgrupos, que aparecen al integrar.

## Cómo elegir

| Contexto | Estructura sugerida |
|---|---|
| Equipo con experiencia dispar, plazo ajustado | Líder designado |
| Equipo chico y experimentado | Democrático |
| Partes técnicamente heterogéneas | Por especialidad |
| Módulos independientes, equipo mediano | Por funcionalidad |
| Proyecto académico de 3 a 4 integrantes | Líder rotativo por etapa |

> La última fila es la recomendada para el proyecto integrador: cada integrante conduce una etapa, y así todos ejercen el rol de conducción al menos una vez.

---

# Roles y responsabilidades

Un rol no es una tarea. Un rol es **un conjunto de responsabilidades y la autoridad para cumplirlas**.

## Roles típicos

| Rol | Responsabilidad | Autoridad |
|---|---|---|
| Líder de proyecto | Que el proyecto cumpla alcance, plazo y calidad | Asignar tareas, negociar con el cliente |
| Analista | Que el problema esté bien comprendido y documentado | Definir requerimientos, validar con el cliente |
| Desarrollador | Que lo construido funcione y sea mantenible | Decidir la implementación |
| Responsable de pruebas | Que los defectos se detecten antes de la entrega | Rechazar una entrega que no pasa las pruebas |
| Referente de la organización | Que el equipo tenga la información y las decisiones que necesita | Decidir sobre el negocio |

El último rol es del lado del cliente, no del equipo, y es imprescindible. Un proyecto sin referente designado en la organización toma decisiones de negocio por su cuenta.

## La asignación inequívoca

> Una tarea de todos es una tarea de nadie.

Cada tarea debe tener **un** responsable. Puede haber varias personas trabajando en ella, pero una sola responde.

| ❌ | ✅ |
|---|---|
| "El documento de alcance lo hacemos entre todos" | "Redacta Ana; revisan Bruno y Carla; aprueba Ana antes de enviarlo" |
| "Las pruebas las hace el equipo" | "Diego es responsable de pruebas; cada uno prueba lo que no construyó" |

## Matriz de asignación

Una forma compacta de dejarlo por escrito:

| Tarea | Responsable | Participan | Aprueba |
|---|---|---|---|
| Informe de diagnóstico | Ana | Bruno, Carla, Diego | Ana |
| Documento de alcance | Bruno | Ana | Cliente |
| Modelo de datos | Carla | Diego | Bruno |
| Estimación | Ana | todos | Ana |
| Cronograma | Diego | Ana | Ana |
| Informe de viabilidad | Bruno | Carla | Ana |

Una sola columna de "Responsable" por fila, siempre con un solo nombre.

---

# Tamaño del equipo y comunicación

## El problema de los canales

En un equipo de **n** personas, la cantidad de canales de comunicación posibles es:

```
canales = n × (n − 1) / 2
```

| Personas | Canales |
|---|---|
| 2 | 1 |
| 3 | 3 |
| 4 | 6 |
| 5 | 10 |
| 8 | 28 |
| 12 | 66 |
| 20 | 190 |

La cantidad de gente crece de forma lineal; la comunicación necesaria, de forma cuadrática.

## La consecuencia

Cada canal consume tiempo: coordinar, informar, resolver malentendidos, alinear decisiones.

A partir de cierto tamaño, **agregar una persona reduce la productividad del equipo**: el esfuerzo de coordinación que introduce es mayor que el trabajo que aporta.

Esto es lo que formalizan los exponentes mayores que 1 de COCOMO, que vimos en la Unidad 8. Ahora sabemos de dónde vienen.

## Las dos consecuencias prácticas

**1. Agregar gente a un proyecto atrasado lo atrasa más.** El nuevo integrante no es productivo de inmediato y consume tiempo de quien ya estaba para ponerse al día.

**2. Los equipos grandes se dividen.** La respuesta correcta a un proyecto grande no es un equipo de veinte personas, sino cuatro equipos de cinco con interfaces definidas entre ellos.

> Regla de referencia: equipos de entre 3 y 7 personas. Por debajo hay poca capacidad; por encima, la coordinación empieza a dominar.

---

# Coordinación entre equipos

Cuando hay más de un equipo, la coordinación se vuelve un trabajo en sí mismo.

## Mecanismos

| Mecanismo | Para qué |
|---|---|
| **Interfaces definidas** | Que cada equipo sepa qué le entrega al otro y en qué formato |
| **Referente por equipo** | Un punto de contacto, en lugar de todos con todos |
| **Reunión de sincronización** | Corta, periódica y solo entre referentes |
| **Repositorio compartido** | Que el estado del trabajo sea visible sin preguntar |
| **Acuerdos técnicos comunes** | Convenciones que evitan divergencia |

El primer mecanismo es el determinante. **La mayoría de los problemas de integración son problemas de interfaz no acordada**, no problemas técnicos.

## Reducir canales con referentes

Cuatro equipos de cinco personas: si todos hablaran con todos, serían 190 canales. Con un referente por equipo, la coordinación entre equipos son 6 canales, y dentro de cada equipo, 10.

Total: 46 canales en lugar de 190.

Esa reducción es el propósito de la estructura.

---

# El analista en la conducción

El analista no siempre es el líder del proyecto, pero casi siempre cumple un papel de conducción, por una razón estructural: **es quien tiene la visión completa**.

Conoce el problema del cliente, el alcance acordado, el plan, los riesgos y el estado del trabajo.

## Sus responsabilidades de conducción

- Que el equipo entienda **por qué** se hace lo que se hace, no solo qué hay que hacer.
- Que la información del cliente llegue completa al equipo, y a la inversa.
- Que los desvíos se detecten y se comuniquen.
- Que las decisiones queden registradas.
- Que nadie quede bloqueado esperando algo que se puede resolver.

## Lo que no le corresponde

- Decidir la implementación técnica, que es del desarrollador.
- Decidir sobre el negocio, que es del referente de la organización.
- Evaluar personas con las métricas del proyecto, como vimos en la Unidad 7.

> Conducir no es decidir todo. Conducir es asegurar que cada decisión la tome quien corresponde, con la información necesaria y a tiempo.

---

# Errores frecuentes

- **Resolver la organización con "nos repartimos las tareas".**
- **Planificar una dotación constante** en lugar de una que varíe por etapa.
- **No designar responsable único** por tarea.
- **No definir quién decide** cuando hay desacuerdo.
- **No pedir un referente en la organización**, y decidir sobre el negocio por cuenta propia.
- **Agregar gente a un proyecto atrasado.**
- **Armar equipos grandes** en lugar de varios equipos chicos con interfaces.
- **No acordar las interfaces entre equipos**, y descubrir el problema al integrar.
- **Confundir conducir con decidir todo.**

---

# Buenas prácticas

✔ Elegir la estructura de equipo según el contexto, y dejarla escrita.

✔ Dimensionar por etapa, no con un promedio.

✔ Un responsable único por tarea, siempre.

✔ Definir explícitamente quién decide en cada tipo de decisión.

✔ Exigir un referente designado en la organización, con disponibilidad acordada.

✔ Mantener los equipos entre 3 y 7 personas.

✔ Acordar las interfaces antes de que los equipos empiecen a trabajar.

✔ Registrar las decisiones y quién las tomó.

---

# Caso de estudio

## El proyecto de cuatro y el proyecto de doce

**Proyecto A.** Cuatro personas, sistema del club, 9 meses. Todas con experiencia similar. Trabajan en el mismo lugar dos veces por semana.

**Proyecto B.** Doce personas, sistema para una cadena de gimnasios con 8 sedes, 14 meses. Tres son analistas, seis desarrolladores, dos de pruebas y una de infraestructura. Trabajan de forma remota en tres ciudades.

### Para analizar

1. Calcule la cantidad de canales de comunicación de cada proyecto.
2. ¿Qué estructura de equipo recomendaría para cada uno? Fundamente.
3. Para el proyecto B, proponga una división en subequipos e indique las interfaces entre ellos.
4. ¿Cuántos canales quedan en el proyecto B con su propuesta? Compare con el total inicial.
5. En el proyecto B, ¿quién decide cuando dos subequipos discrepan sobre una decisión técnica compartida?
6. El proyecto B se atrasa dos meses. La dirección propone sumar cuatro personas. ¿Qué responde y por qué?
7. En el proyecto A, ¿qué pasa si la persona que hace el modelo de datos se ausenta tres semanas? ¿Cómo se lo previene?

---

# Aplicación profesional

Cada grupo entrega la **planificación organizativa** de su proyecto:

- estructura de equipo elegida, con su fundamentación;
- dimensionamiento por etapa;
- matriz de asignación de tareas, con responsable único por fila;
- definición de quién decide en cada tipo de decisión: técnica, de alcance, de negocio;
- referente solicitado a la organización, con la disponibilidad que se necesita;
- rutinas de comunicación: qué reuniones, con qué frecuencia y para qué.

Esta planificación se combina con el cronograma de la Unidad 10: la asignación de personas a tareas es lo que permite verificar si el plan es ejecutable con la gente disponible.

---

# Resumen

En esta unidad aprendimos que:

- El Personal es la primera de las 4P porque es el factor que más determina el resultado y el que menos se planifica.
- La planificación organizativa decide dimensionamiento, estructura, roles, comunicación y autoridad.
- La cantidad de gente necesaria varía por etapa: planificar un promedio produce faltantes y sobrantes.
- Las estructuras de equipo tienen contextos de aplicación distintos y riesgos propios.
- Un rol es un conjunto de responsabilidades más la autoridad para cumplirlas.
- Cada tarea debe tener un responsable único; una tarea de todos es una tarea de nadie.
- Los canales de comunicación crecen como n(n−1)/2, de forma cuadrática.
- A partir de cierto tamaño, agregar una persona reduce la productividad del equipo.
- La respuesta a un proyecto grande son varios equipos chicos con interfaces definidas.
- Conducir no es decidir todo: es asegurar que cada decisión la tome quien corresponde.

---

# Actividad práctica

## Planificación organizativa

**1. Estructura**

Elijan la estructura de equipo de su grupo y fundamenten en un párrafo por qué es la adecuada para su proyecto.

**2. Dimensionamiento**

Indiquen, para cada etapa de su cronograma, cuántas personas y con qué perfil hacen falta.

**3. Matriz de asignación**

Completen la matriz para todas las entregas del proyecto: tarea, responsable único, participantes y quién aprueba.

**4. Autoridad**

Definan quién decide en tres tipos de decisión: técnica, de alcance y de negocio. Indiquen qué se hace si el responsable no está disponible.

**5. Canales**

Calculen los canales de comunicación de su equipo. Definan las rutinas de comunicación que van a sostener: qué reuniones, cuándo y con qué objetivo.

**6. Referente**

Redacten el pedido de referente a la organización: qué necesitan de esa persona, cuántas horas y con qué capacidad de decisión.

**7. Riesgo de dependencia**

Identifiquen la tarea con mayor dependencia de una sola persona y propongan cómo reducir ese riesgo.

**Formato de entrega:** informe técnico de dos páginas con las tablas.

---

# Preguntas de repaso

1. ¿Por qué el Personal es la primera de las 4P?

2. ¿Cuáles son las cinco preguntas que responde la planificación organizativa?

3. ¿Por qué planificar una dotación constante produce problemas?

4. Nombre dos estructuras de equipo, su contexto de aplicación y su riesgo principal.

5. ¿Qué diferencia hay entre un rol y una tarea?

6. ¿Por qué cada tarea debe tener un responsable único?

7. Escriba la fórmula de canales de comunicación y calcúlela para un equipo de 6 personas.

8. ¿Por qué agregar gente a un proyecto atrasado lo atrasa más?

9. ¿Cuál es la respuesta correcta a un proyecto que requiere veinte personas?

10. ¿Qué significa que conducir no es decidir todo?

---

# Bibliografía

- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Capítulo sobre el personal del proyecto y estructuras de equipo.
- Sommerville, I. *Ingeniería del Software.* Capítulo sobre gestión de personal y trabajo en equipo.
- Project Management Institute. [*Guía PMBOK*](https://www.pmi.org/standards/pmbok). Área de Gestión de los Recursos. _(acceso pago)_

---

**Fin de la Unidad 11**
