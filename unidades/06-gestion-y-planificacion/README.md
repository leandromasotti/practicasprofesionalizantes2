# Unidad 6
# Gestión y planificación. El plan de proyecto

> "Un proyecto sin plan no es un proyecto: es una serie de urgencias encadenadas."

> Las secciones de **métricas** y **estimación** de esta unidad son introductorias. Se desarrollan en profundidad en la Unidad 7 (clasificación de métricas, métricas orientadas al tamaño, a la función y a casos de uso) y en la Unidad 8 (técnicas de descomposición y modelos empíricos como COCOMO).

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Comprender qué significa gestionar un proyecto de software.
- Distinguir entre planificar y ejecutar.
- Diferenciar con precisión un hito de un entregable.
- Elaborar un plan de proyecto simple pero completo.
- Estimar el esfuerzo necesario para realizar una tarea.
- Interpretar métricas básicas de seguimiento.
- Reconocer por qué los planes se desvían y cómo reaccionar ante ello.

---

# El problema inicial

Imaginemos que un grupo recibe el encargo de desarrollar un sistema.

El equipo está motivado y quiere empezar cuanto antes.

Entonces surgen dos preguntas que parecen simples:

- ¿Cómo organizamos el trabajo?
- ¿Qué pasa si no planificamos?

La segunda pregunta suele responderse sola con el tiempo.

Sin planificación aparecen situaciones muy reconocibles:

- dos personas hacen la misma tarea;
- nadie hace una tarea porque todos suponían que la hacía otro;
- se descubre a último momento que falta algo importante;
- la entrega se realiza apurada y de mala calidad;
- nadie sabe cuánto se avanzó realmente.

Planificar no elimina los problemas.

Planificar permite detectarlos a tiempo.

---

# ¿Qué es la gestión de proyectos?

Gestionar un proyecto consiste en conducirlo desde su inicio hasta su cierre, tomando decisiones para que los objetivos se cumplan dentro de los recursos disponibles.

Comprende cuatro actividades permanentes:

## Organizar el trabajo

Dividir el proyecto en tareas comprensibles y manejables.

---

## Asignar tareas

Definir quién hace cada cosa y con qué plazo.

---

## Controlar avances

Verificar periódicamente qué se completó y qué no.

---

## Ajustar el plan

Modificar la planificación cuando la realidad se aparta de lo previsto.

---

Estas cuatro actividades no ocurren una sola vez al comienzo.

Se repiten durante todo el proyecto.

Un plan que no se actualiza deja de ser un plan y se convierte en un documento histórico.

---

# Planificar es decidir antes de empezar

Planificar consiste en tomar, por anticipado, las decisiones que de otro modo se tomarían apuradas y en el peor momento.

Planificar implica definir:

- **Qué tareas** componen el proyecto.
- **En qué orden** deben realizarse.
- **Cuánto tiempo** llevará cada una.
- **Quién** es responsable de cada una.
- **Qué se entrega** y **cuándo**.

Conviene insistir en una idea:

Planificar no es adivinar el futuro.

Es construir una referencia contra la cual comparar la realidad.

Cuando la realidad se aparta de esa referencia, el equipo se entera temprano y puede reaccionar.

Sin referencia, la desviación se descubre el día de la entrega.

---

# Hitos

Un **hito** es un momento significativo del proyecto.

Marca un punto de control en el tiempo: algo importante acaba de ocurrir o debe ocurrir.

Un hito no tiene duración. Es una fecha.

Ejemplos de hitos:

- Inicio del proyecto.
- Aprobación del documento de alcance por parte del cliente.
- Cierre del relevamiento.
- Aprobación del diseño.
- Entrega final.
- Presentación ante el cliente.

Los hitos permiten responder una pregunta muy concreta: *¿estamos donde deberíamos estar?*

---

# Entregables

Un **entregable** es un producto concreto que el proyecto genera y que alguien recibe.

A diferencia del hito, el entregable se puede abrir, leer, ejecutar o revisar.

Ejemplos de entregables:

- Documento de alcance.
- Informe de relevamiento.
- Diagrama de clases UML.
- Cronograma del proyecto.
- Prototipo del sistema.
- Manual de usuario.
- Presentación final.

---

# La diferencia entre hito y entregable

Esta distinción se confunde con mucha frecuencia, así que conviene fijarla con claridad.

| | Hito | Entregable |
|---|---|---|
| **Qué es** | Un momento clave | Un producto concreto |
| **Tiene duración** | No, es una fecha | No aplica: es una cosa |
| **Se puede tocar** | No | Sí |
| **Ejemplo** | "Aprobación del alcance" | "Documento de alcance" |

Una forma sencilla de recordarlo:

> El entregable es **lo que se entrega**.
>
> El hito es **el momento en que se entrega**.

Ambos suelen aparecer juntos: la entrega del documento de alcance (entregable) da lugar al hito "alcance aprobado".

Pero no siempre coinciden. El inicio del proyecto es un hito y no produce ningún entregable.

---

# El plan de proyecto

El plan de proyecto es el documento que organiza todo el trabajo.

No necesita ser extenso. Necesita ser **usable**.

Un plan de proyecto debe incluir:

- **Objetivo** — qué se busca lograr.
- **Alcance** — qué incluye y qué no incluye el proyecto.
- **Tareas** — el trabajo descompuesto en unidades manejables.
- **Cronograma** — cuándo se hace cada tarea.
- **Hitos** — los puntos de control.
- **Entregables** — los productos a generar.
- **Responsables** — quién responde por cada tarea.
- **Recursos** — con qué se cuenta.

Un plan que nadie lee no sirve.

Un plan que no se actualiza, tampoco.

---

# Un ejemplo mínimo de planificación

Un proyecto corto de cuatro semanas podría organizarse así:

| Semana | Foco | Entregable | Hito |
|---|---|---|---|
| 1 | Alcance | Documento de alcance v1 | Alcance aprobado |
| 2 | Análisis | Informe de requerimientos | Relevamiento cerrado |
| 3 | Diseño | Diagrama de clases UML | Diseño aprobado |
| 4 | Entrega | Presentación final | Entrega final |

Obsérvese que cada semana produce **algo**.

Esta es una característica de una buena planificación: el avance es visible y verificable, no una sensación.

Si al final de la semana 2 no existe el informe de requerimientos, el equipo sabe con certeza que está atrasado. No hace falta discutirlo.

---

# Descomponer el trabajo

Antes de estimar hay que descomponer.

Una tarea como "hacer el sistema" es imposible de estimar y de controlar.

Descomponer consiste en partirla hasta llegar a tareas que cumplan tres condiciones:

- se entiende con claridad qué hay que hacer;
- tiene un responsable identificable;
- se puede estimar con cierta confianza.

Por ejemplo, en lugar de "relevamiento":

- Preparar el guion de la entrevista.
- Entrevistar al presidente del club.
- Entrevistar al administrativo.
- Redactar el informe de relevamiento.
- Validar el informe con el cliente.

Cinco tareas estimables reemplazan a una tarea imposible de estimar.

Una regla práctica: si una tarea dura más que el período de control del proyecto (por ejemplo, más de una semana), probablemente convenga descomponerla más.

---

# Estimación

**Estimar** consiste en predecir cuánto esfuerzo o cuánto tiempo demandará una tarea.

Una estimación no es un dato exacto.

Es una aproximación fundamentada.

Esta distinción es importante, porque una estimación se comunica de forma muy distinta a un dato cierto.

## Técnicas habituales

### Juicio experto

Se consulta a alguien que ya realizó una tarea similar.

Es rápido y suele ser razonablemente bueno, pero depende de la experiencia disponible en el equipo.

---

### Estimación por analogía

Se compara con una tarea parecida ya realizada.

*"El informe de relevamiento del proyecto anterior nos llevó tres días; este es algo más chico, calculamos dos."*

---

### Descomposición

Se estima cada subtarea y se suman los resultados.

Suele ser más precisa que estimar el total de una sola vez.

---

### Estimación por tres valores

Para cada tarea se estiman tres escenarios:

- **Optimista (O):** todo sale bien.
- **Más probable (M):** el escenario realista.
- **Pesimista (P):** aparecen complicaciones.

El valor esperado se calcula como:

```
Estimación = (O + 4M + P) / 6
```

Esta técnica reconoce algo que la experiencia confirma: los problemas son más frecuentes que los aciertos inesperados.

Sobre esta idea se construye el método PERT, que veremos en la próxima unidad.

---

# Por qué las estimaciones fallan

Las estimaciones se equivocan casi siempre, y por razones bastante previsibles:

- Se estima el trabajo ideal, sin interrupciones ni reuniones.
- Se olvidan tareas que no son "hacer" sino revisar, corregir y validar.
- Se subestima el tiempo de coordinación entre personas.
- Se estima con optimismo para conformar al cliente.
- No se contempla el tiempo de espera por respuestas de terceros.

Un equipo maduro no aspira a estimar perfecto.

Aspira a **estimar, medir el desvío y aprender de él**.

Registrar cuánto se estimó y cuánto llevó realmente es la forma más efectiva de mejorar las estimaciones futuras.

---

# Métricas

Una **métrica** es un dato que permite medir algo del proyecto de manera objetiva.

Las métricas convierten impresiones en información.

No es lo mismo decir *"vamos bien"* que decir *"completamos 12 de 20 tareas y llevamos consumido el 55 % del tiempo previsto"*.

## Métricas básicas de seguimiento

- Cantidad de tareas planificadas.
- Cantidad de tareas completadas.
- Porcentaje de avance.
- Tiempo estimado versus tiempo real.
- Cantidad de tareas atrasadas.
- Cantidad de cambios solicitados por el cliente.
- Cantidad de errores detectados.

## Para qué sirven

- Detectar desvíos a tiempo.
- Fundamentar decisiones con datos y no con percepciones.
- Comunicar el estado del proyecto al cliente de forma verificable.
- Mejorar la planificación de proyectos futuros.

Una advertencia: la métrica es una herramienta de diagnóstico, no un fin en sí mismo.

Un equipo que trabaja para que los números luzcan bien deja de trabajar para el proyecto.

---

# Caso de estudio

## Club Deportivo San Martín

Retomamos el caso de la Unidad 2.

El club decidió avanzar con la informatización de sus procesos y el equipo debe planificar un proyecto de **ocho semanas**.

El alcance acordado incluye:

- registro de socios;
- control de cuotas;
- gestión de actividades deportivas.

Una planificación posible:

| Semana | Tareas principales | Entregable | Hito |
|---|---|---|---|
| 1 | Entrevistas con presidente y administración | Informe de relevamiento | Relevamiento cerrado |
| 2 | Definición y validación del alcance | Documento de alcance | Alcance aprobado |
| 3 | Análisis de requerimientos | Listado de requerimientos | — |
| 4 | Modelado del sistema | Diagrama de clases UML | Diseño aprobado |
| 5-6 | Construcción del prototipo | Prototipo navegable | — |
| 7 | Pruebas con usuarios del club | Informe de pruebas | Prototipo validado |
| 8 | Documentación y presentación | Manual e informe final | Entrega final |

Preguntas para analizar el plan:

- ¿Qué ocurre si el presidente del club no está disponible durante la semana 1?
- ¿Qué tareas podrían realizarse en paralelo?
- ¿Cuál es la tarea cuyo atraso arrastraría a todas las demás?
- ¿Qué entregable convendría validar antes con el cliente para reducir el riesgo?

Estas preguntas son exactamente las que se hace un analista al revisar una planificación.

---

# Errores frecuentes

- Planificar únicamente el desarrollo y olvidar el relevamiento, las pruebas y la documentación.
- Confundir hitos con entregables.
- Definir tareas tan grandes que resultan imposibles de estimar y de controlar.
- Estimar en función de la fecha deseada por el cliente en lugar del trabajo real.
- No asignar responsables: una tarea de todos es una tarea de nadie.
- Elaborar el plan al inicio y no volver a mirarlo nunca.
- Ocultar los atrasos con la esperanza de recuperarlos más adelante.

---

# Buenas prácticas

✔ Descomponer el trabajo antes de estimarlo.

✔ Asignar un único responsable por tarea.

✔ Definir entregables concretos y verificables.

✔ Revisar el plan periódicamente, no solo al final.

✔ Registrar el tiempo real para mejorar estimaciones futuras.

✔ Comunicar los desvíos apenas se detectan.

✔ Dejar margen: ninguna planificación se cumple al minuto.

---

# Aplicación profesional

Durante el proyecto integrador cada grupo deberá elaborar y mantener su propio plan de proyecto.

Ese plan será revisado en distintos momentos de la cursada.

No se evaluará únicamente que el plan exista, sino que:

- se haya actualizado a lo largo del tiempo;
- refleje lo que efectivamente ocurrió;
- permita explicar los desvíos con fundamento.

Un plan que se mantuvo idéntico de principio a fin, en un proyecto donde todo cambió, es una señal de que nadie lo utilizó.

---

# Resumen

En esta unidad aprendimos que:

- Gestionar un proyecto implica organizar, asignar, controlar y ajustar de manera permanente.
- Planificar es decidir antes de empezar y construir una referencia para medir el avance.
- Un hito es un momento clave; un entregable es un producto concreto.
- El plan de proyecto organiza tareas, tiempos, responsables, hitos y entregables.
- Estimar es aproximar de manera fundamentada, no adivinar.
- Las métricas convierten impresiones en información verificable.
- Un plan sirve mientras se mantiene actualizado.

---

# Actividad práctica

## Planificando el proyecto integrador

En los mismos grupos de trabajo del proyecto integrador:

**1. Descomposición**

Dividan su proyecto en un mínimo de diez tareas concretas. Cada tarea debe tener un verbo y un resultado observable.

**2. Hitos y entregables**

Definan al menos cuatro hitos y cuatro entregables. Preséntenlos en una tabla y verifiquen que ninguno esté clasificado en la columna equivocada.

**3. Estimación**

Estimen cada tarea usando la técnica de tres valores. Calculen el valor esperado e indiquen cuál fue la tarea más difícil de estimar y por qué.

**4. Responsables**

Asignen un único responsable a cada tarea.

**5. Métricas**

Definan tres métricas con las que van a controlar el avance del proyecto e indiquen con qué frecuencia las van a medir.

**Formato de entrega:** documento o planilla, una a dos páginas.

**Importante:** conserven esta planificación. Al finalizar la cursada van a compararla con lo que realmente ocurrió.

---

# Preguntas de repaso

1. ¿Cuál es la diferencia entre un hito y un entregable? Dé un ejemplo de cada uno.

2. ¿Por qué se dice que planificar no consiste en adivinar el futuro?

3. ¿Qué elementos debe contener un plan de proyecto?

4. ¿Por qué conviene descomponer una tarea antes de estimarla?

5. ¿Qué información aporta comparar el tiempo estimado con el tiempo real?

6. Mencione tres razones por las cuales una estimación puede fallar.

7. ¿Qué riesgo existe cuando un equipo trabaja para mejorar sus métricas en lugar de trabajar para el proyecto?

---

# Bibliografía

- Pressman, Roger. *Ingeniería del Software: Un enfoque práctico.* Capítulos sobre gestión de proyectos, métricas y estimación.
- Sommerville, Ian. *Ingeniería del Software.* Capítulo sobre planificación de proyectos.
- Project Management Institute (PMI). *Guía PMBOK.* Áreas de conocimiento de Alcance, Cronograma y Costos.

---

**Fin de la Unidad 6**
