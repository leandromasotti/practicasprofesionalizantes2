# Unidad 3
# Metodologías tradicionales y ágiles

> "No existe la metodología correcta. Existe la metodología adecuada para este proyecto, en esta organización, con este equipo y en este momento."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Comprender qué es el ciclo de vida del software y por qué toda organización adopta uno.
- Distinguir las metodologías tradicionales de las ágiles.
- Reconocer el modelo en cascada, los modelos incrementales y los evolutivos.
- Identificar los valores y principios del Manifiesto Ágil.
- Describir los roles, eventos y artefactos de Scrum.
- **Evaluar** qué metodología resulta adecuada para un proyecto dado y fundamentar esa elección.

> **Articulación.** Ingeniería en Software I desarrolla los modelos de proceso desde la teoría del desarrollo. Aquí el enfoque es el del analista frente a una organización: qué metodología conviene adoptar, qué exige de la organización, y qué señales indican que la elegida no está funcionando.

---

# El problema inicial

Una organización aprueba un proyecto y aparece de inmediato una pregunta que suele responderse por costumbre en lugar de por análisis:

**¿Cómo vamos a trabajar?**

Muchas veces la respuesta es "como siempre". Otras veces es "de forma ágil", sin que nadie pueda explicar qué significa eso más allá de hacer reuniones de pie.

Ninguna de las dos es una decisión: son inercias.

Elegir una metodología es una decisión de proyecto, con consecuencias sobre los plazos, el presupuesto, la relación con el cliente y el ánimo del equipo.

Y como toda decisión de proyecto, el analista debe poder fundamentarla.

---

# El ciclo de vida del software

Todo sistema atraviesa una serie de etapas desde que se concibe hasta que se retira.

Ese recorrido se denomina **ciclo de vida del software**.

Las etapas típicas son:

- **Análisis** — comprender el problema y relevar necesidades.
- **Diseño** — decidir cómo será la solución.
- **Implementación** — construirla.
- **Pruebas** — verificar que funciona.
- **Entrega** — ponerla en producción.
- **Mantenimiento** — corregirla y hacerla evolucionar.

Todas las metodologías atraviesan estas etapas.

La diferencia no está en **cuáles** son las etapas, sino en **cómo se ordenan y cuántas veces se recorren**.

Esa es la distinción de fondo de esta unidad.

---

# Metodologías tradicionales

Las metodologías tradicionales se apoyan en una premisa: **es posible saber al comienzo qué hay que construir**.

Si esa premisa se cumple, conviene planificar en detalle antes de empezar y después ejecutar el plan.

Sus rasgos característicos:

- Planificación extensa y anticipada.
- Etapas secuenciales.
- Documentación exhaustiva.
- Requerimientos definidos y aprobados al inicio.
- El cambio se trata como una excepción que hay que controlar.

---

## El modelo en cascada

Es el modelo tradicional por excelencia.

Cada etapa comienza cuando la anterior terminó y fue aprobada. El nombre viene de la imagen: el trabajo cae de una etapa a la siguiente y no vuelve a subir.

| Orden | Etapa | Condición para avanzar |
|---|---|---|
| 1 | Análisis | Requerimientos aprobados |
| 2 | Diseño | Diseño aprobado |
| 3 | Implementación | Construcción terminada |
| 4 | Pruebas | Pruebas superadas |
| 5 | Entrega | Sistema en producción |
| 6 | Mantenimiento | — |

### Cuándo funciona bien

- Los requerimientos son estables y están claros desde el inicio.
- El dominio es conocido y la organización ya hizo proyectos similares.
- Existen exigencias contractuales, regulatorias o de auditoría que obligan a documentar y aprobar cada etapa.
- El costo de equivocarse en producción es muy alto.

### Sus límites

- El cliente recién ve el sistema al final.
- Un error de comprensión en el análisis se arrastra por todo el proyecto y se descubre tarde.
- Absorbe mal los cambios: modificar algo aprobado obliga a rehacer etapas.
- El valor se entrega todo junto, al final. Si el proyecto se cancela antes, no queda nada utilizable.

> El modelo en cascada suele presentarse como obsoleto. No lo es. Es inadecuado cuando los requerimientos son inciertos —que es la situación más común—, pero sigue siendo la mejor opción en proyectos con requerimientos estables y fuertes exigencias de documentación.

---

# Modelos intermedios

Entre la cascada pura y los métodos ágiles existen modelos que conservan la planificación pero rompen la secuencia única.

## Modelo incremental

El sistema se construye por partes.

Cada incremento atraviesa todas las etapas y agrega funcionalidad utilizable al producto anterior.

La organización recibe algo que funciona mucho antes del final.

*Ejemplo:* primero el registro de socios, después el control de cuotas, después la gestión de actividades.

---

## Modelo evolutivo

Se construye una versión inicial y se la refina sucesivamente a partir de la retroalimentación recibida.

Es apropiado cuando ni siquiera el cliente sabe con precisión qué necesita.

---

## Prototipado

Se construye una versión reducida y descartable con el único objetivo de **comprender el requerimiento**.

El prototipo no es el sistema: es una herramienta de análisis.

Sirve especialmente cuando el cliente no logra explicar lo que quiere pero puede reconocerlo cuando lo ve.

> Riesgo clásico: que el cliente vea el prototipo y pida ponerlo en producción. Un prototipo se construye para ser descartado, y esa condición debe estar acordada por escrito antes de mostrarlo.

---

# Metodologías ágiles

Las metodologías ágiles parten de la premisa opuesta: **no es posible saber al comienzo todo lo que hay que construir**.

Si el conocimiento se va adquiriendo durante el proyecto, conviene trabajar en ciclos cortos, entregar seguido y ajustar el rumbo con lo aprendido.

Sus rasgos característicos:

- Iteraciones breves y de duración fija.
- Entregas frecuentes de software funcionando.
- Colaboración permanente con el cliente.
- Adaptación al cambio como norma, no como excepción.
- Equipos pequeños y autoorganizados.

---

## El Manifiesto Ágil

En 2001, diecisiete profesionales publicaron un documento breve que ordenó estas ideas.

Sus **cuatro valores**:

> **Individuos e interacciones** sobre procesos y herramientas.
>
> **Software funcionando** sobre documentación extensiva.
>
> **Colaboración con el cliente** sobre negociación contractual.
>
> **Respuesta ante el cambio** sobre seguir un plan.

El manifiesto agrega una aclaración que suele omitirse y que es la parte más importante:

> "Esto es, aunque valoramos los elementos de la derecha, **valoramos más los de la izquierda**."

No dice que la documentación no sirva. Dice que, ante un conflicto entre ambos, se prioriza el de la izquierda.

Esta distinción importa: buena parte de las malas implementaciones de agilidad consisten en leer la columna derecha como si estuviera prohibida.

Al manifiesto lo acompañan **doce principios**, entre ellos la entrega temprana y continua de valor, la aceptación de cambios incluso en etapas tardías, y la reflexión periódica del equipo sobre su propia forma de trabajar.

---

## Scrum

Scrum es el marco de trabajo ágil más difundido en la industria.

No es una metodología completa: es una estructura mínima de roles, eventos y artefactos sobre la que cada organización construye su forma de trabajar.

El trabajo se organiza en **Sprints**: iteraciones de duración fija, habitualmente de dos a cuatro semanas, al final de las cuales debe existir un incremento de producto utilizable.

### Roles

| Rol | Responsabilidad |
|---|---|
| **Product Owner** | Representa al cliente y a los usuarios. Define y prioriza qué se construye y en qué orden. |
| **Scrum Master** | Facilita el proceso, remueve impedimentos y protege al equipo. No es un jefe. |
| **Equipo de desarrollo** | Construye el producto. Es autoorganizado: decide cómo hacer el trabajo. |

### Eventos

| Evento | Propósito |
|---|---|
| **Sprint Planning** | Definir qué se hará en el sprint que comienza. |
| **Daily Scrum** | Reunión breve y diaria para sincronizar el trabajo y detectar impedimentos. |
| **Sprint Review** | Mostrar el incremento al cliente y recibir retroalimentación. |
| **Sprint Retrospective** | Revisar cómo trabajó el equipo y acordar mejoras. |

### Artefactos

| Artefacto | Qué es |
|---|---|
| **Product Backlog** | Lista priorizada de todo lo que el producto podría necesitar. |
| **Sprint Backlog** | Lo que el equipo se comprometió a hacer en el sprint actual. |
| **Incremento** | El producto utilizable que resulta al cierre del sprint. |

> La Daily Scrum es una reunión de sincronización entre pares, no un informe de avance a un superior. Cuando se convierte en lo segundo deja de cumplir su función, y el equipo empieza a maquillar el estado real del trabajo.

---

# Comparación

| | Tradicional | Ágil |
|---|---|---|
| **Premisa** | Se puede saber todo al inicio | El conocimiento se construye durante el proyecto |
| **Planificación** | Detallada y anticipada | Continua y por iteraciones |
| **Entregas** | Una, al final | Frecuentes y parciales |
| **Cambios** | Excepción a controlar | Norma esperada |
| **Documentación** | Exhaustiva | La necesaria |
| **Cliente** | Al inicio y al final | Presente durante todo el proyecto |
| **Visibilidad del avance** | Baja hasta el final | Alta y permanente |
| **Contrato** | Alcance cerrado | Alcance evolutivo |

---

# Cómo elegir: criterios de decisión

Esta es la competencia que la unidad busca desarrollar. No se trata de saber qué es Scrum, sino de decidir si corresponde usarlo.

| Pregunta sobre el proyecto | Inclina hacia tradicional | Inclina hacia ágil |
|---|---|---|
| ¿Los requerimientos están claros y estables? | Sí | No |
| ¿El dominio es conocido para el equipo? | Sí | No |
| ¿Hay exigencias regulatorias o de auditoría? | Sí | No |
| ¿El cliente puede participar de forma continua? | No | Sí |
| ¿Se necesita entregar valor temprano? | No | Sí |
| ¿El contrato fija alcance y precio cerrados? | Sí | No |
| ¿El equipo es pequeño y comparte espacio de trabajo? | Indistinto | Sí |
| ¿El costo de un error en producción es crítico? | Sí | No |

Ninguna respuesta decide por sí sola. El analista pondera el conjunto y **fundamenta** la elección.

## La restricción que se suele ignorar

Una metodología ágil requiere que el cliente esté disponible de manera continua.

Si la organización no puede o no quiere asignar a alguien con capacidad de decisión durante todo el proyecto, adoptar Scrum produce un resultado peor que la cascada: iteraciones que terminan sin validación y decisiones tomadas por el equipo técnico sobre asuntos que no le corresponden.

Antes de proponer una metodología ágil hay que verificar que la organización pueda sostenerla.

## Enfoques híbridos

En la práctica muchas organizaciones combinan: relevamiento y definición de alcance con enfoque tradicional, construcción con iteraciones.

No es una contradicción. Es una respuesta razonable cuando el contrato exige un alcance cerrado pero la construcción se beneficia de entregas frecuentes.

---

# Errores frecuentes

- **Adoptar una metodología por moda**, sin analizar si el contexto la sostiene.
- **Llamar ágil a la ausencia de planificación.** Ágil no significa improvisar: significa planificar de otra manera y con más frecuencia.
- **Usar cascada con requerimientos inciertos**, y descubrir en la entrega que se construyó otra cosa.
- **Implementar los eventos de Scrum vaciados de su propósito**: dailies que son informes de avance, retrospectivas que nunca cambian nada, sprints que cierran sin incremento utilizable.
- **Prometer agilidad con un contrato de alcance cerrado.** Son incompatibles, y el conflicto aparece con el primer cambio de requerimiento.
- **Cambiar de metodología a mitad del proyecto** sin evaluar el costo de la transición.

---

# Buenas prácticas

✔ Analizar el contexto antes de elegir la metodología.

✔ Verificar que la organización pueda sostener lo que la metodología exige.

✔ Dejar por escrito la metodología elegida y su fundamentación.

✔ Acordar con el cliente cómo se tratarán los cambios, cualquiera sea el enfoque.

✔ Adaptar el marco al proyecto y no al revés.

✔ Revisar periódicamente si la metodología elegida está funcionando.

---

# Caso de estudio

## Dos organizaciones, dos decisiones

### Caso A — Clínica Santa Elena

Una clínica necesita un sistema de historia clínica electrónica.

Datos del contexto:

- La normativa sanitaria fija con precisión qué datos deben registrarse y conservarse.
- El sistema será auditado por el organismo de control.
- Un error en el registro de una medicación puede tener consecuencias graves.
- La dirección aprobó un presupuesto cerrado.
- El personal médico tiene muy poca disponibilidad para reuniones.

### Caso B — Emprendimiento de reparto

Una empresa de reparto quiere una aplicación para coordinar pedidos.

Datos del contexto:

- El negocio está en formación y el modelo cambia mes a mes.
- Los fundadores trabajan en la misma oficina que el equipo y están disponibles todo el tiempo.
- Necesitan salir al mercado lo antes posible, aunque sea con funcionalidad mínima.
- No hay exigencias regulatorias relevantes.
- El presupuesto se ajusta a medida que el negocio crece.

### Para analizar

1. ¿Qué metodología recomendaría para cada caso? Fundamente con al menos tres criterios de la tabla de decisión.
2. ¿Qué riesgo concreto aparecería si se aplicara Scrum en el caso A?
3. ¿Qué riesgo concreto aparecería si se aplicara cascada en el caso B?
4. ¿Existe alguna combinación híbrida que mejore alguno de los dos casos?
5. ¿Qué pregunta adicional le haría a cada organización antes de decidir?

Estas son exactamente las preguntas que un analista responde en un informe técnico de recomendación metodológica.

---

# Aplicación profesional

Durante el proyecto integrador cada grupo deberá **elegir y fundamentar** la metodología de trabajo de su propio proyecto.

No alcanza con nombrarla. La entrega debe indicar:

- qué metodología se adopta;
- qué características del proyecto y de la organización justifican esa elección;
- qué exige esa metodología de la organización, y si la organización puede sostenerlo;
- qué se hará si aparece un cambio de requerimiento;
- qué señales indicarían que la elección no está funcionando.

Esa fundamentación se retoma en la Unidad 5, al definir el **Proceso** dentro de las 4P.

---

# Resumen

En esta unidad aprendimos que:

- El ciclo de vida del software describe las etapas por las que atraviesa todo sistema; las metodologías se diferencian en cómo las ordenan y cuántas veces las recorren.
- Las metodologías tradicionales suponen requerimientos estables y planifican por anticipado.
- El modelo en cascada no está obsoleto: es inadecuado para requerimientos inciertos, pero apropiado cuando hay estabilidad y exigencias de auditoría.
- Los modelos incremental, evolutivo y de prototipado ocupan posiciones intermedias.
- Las metodologías ágiles suponen conocimiento incompleto y trabajan en ciclos cortos con entregas frecuentes.
- El Manifiesto Ágil prioriza cuatro valores sin negar sus opuestos.
- Scrum aporta una estructura mínima de roles, eventos y artefactos.
- La elección de la metodología es una decisión fundamentada del analista, no una preferencia ni una moda.

---

# Actividad práctica

## Recomendación metodológica

En los grupos del proyecto integrador.

**1. Análisis del contexto**

Respondan las ocho preguntas de la tabla de criterios aplicadas a **su** proyecto y a **su** organización. Justifiquen cada respuesta en una línea.

**2. Recomendación**

Elijan una metodología y fundamenten la elección en un párrafo, citando los criterios que más pesaron.

**3. Condiciones**

Indiquen qué necesitan de la organización para que esa metodología funcione. Sean concretos: quién debe estar disponible, con qué frecuencia y con qué capacidad de decisión.

**4. Plan de cambios**

Describan cómo se tratará un cambio de requerimiento bajo la metodología elegida.

**5. Señales de alerta**

Definan tres señales observables que indicarían que la metodología no está funcionando.

**Formato de entrega:** informe técnico de una a dos páginas.

---

# Preguntas de repaso

1. ¿Qué diferencia de fondo separa a una metodología tradicional de una ágil?

2. ¿En qué situaciones el modelo en cascada sigue siendo la mejor opción?

3. ¿Qué diferencia hay entre un modelo incremental y uno evolutivo?

4. ¿Para qué sirve un prototipo y cuál es el riesgo de construirlo?

5. ¿Por qué el Manifiesto Ágil aclara que también valora los elementos de la derecha?

6. Mencione los tres roles de Scrum e indique la responsabilidad de cada uno.

7. ¿Qué requisito de la organización debe verificarse antes de proponer una metodología ágil?

8. ¿Por qué son incompatibles un contrato de alcance cerrado y un enfoque ágil?

---

# Bibliografía

- [Manifiesto por el Desarrollo Ágil de Software](https://agilemanifesto.org/iso/es/manifesto.html) — versión en español, con sus doce principios
- [The Scrum Guide](https://scrumguides.org/) · [Descargas en español](https://scrumguides.org/download.html)
- [Atlassian — Guía de Scrum](https://www.atlassian.com/es/agile/scrum)
- [Microsoft Learn — ¿Qué es Agile?](https://learn.microsoft.com/es-es/devops/plan/what-is-agile)
- Sommerville, I. *Ingeniería del Software.* Capítulos sobre procesos del software y desarrollo ágil.
- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Capítulos sobre modelos de proceso.

---

**Fin de la Unidad 3**
