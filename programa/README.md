# Programa de la materia

> **Prácticas Profesionalizantes II** · Módulo del Campo de las Prácticas Profesionalizantes
> Tecnicatura Superior en Análisis de Sistemas · 2.º año
> **Carga horaria oficial: 128 horas reloj** · 30 semanas de clase

Este documento define **qué se enseña** en la materia: fundamentación, capacidades profesionales, unidades, contenidos, bibliografía y régimen de evaluación.

Es el documento estable de la cátedra: se mantiene de un ciclo lectivo a otro y se revisa al cierre de cada año.

El **cuándo** se enseña cada cosa vive en [`planificacion/`](../planificacion/), con un archivo por ciclo lectivo.

---

## Marco normativo

El programa se ajusta al diseño curricular aprobado por la **Resolución TSAS 6790/19** de la Dirección General de Cultura y Educación de la Provincia de Buenos Aires.

| | |
|---|---|
| Carrera | Tecnicatura Superior en Análisis de Sistemas |
| Familia profesional | Sistemas Informáticos · Variante diversificada |
| Carga horaria de la carrera | 1856 horas |
| Título | Analista de Sistemas |
| **Este módulo** | Prácticas Profesionalizantes II · 2.º año · **128 horas reloj** |
| **Correlativas para cursar** | Algoritmos y Estructuras de Datos I · Prácticas Profesionalizantes I |

La [correspondencia unidad por unidad con los ejes de contenido oficiales](#correspondencia-con-la-resolución-679019) está al final de este documento.

### Sobre la carga horaria

Las **128 horas reloj** son una obligación normativa que el cronograma de cada ciclo debe cerrar, no una referencia orientativa.

Dos precisiones que condicionan la planificación anual:

- El cómputo se hace sobre **encuentros efectivos**, no sobre semanas: cada feriado que cae en día de clase elimina un encuentro y sus horas.
- La resolución **no habilita** compensar el déficit con tutorías en este módulo. Esa cláusula corresponde a Prácticas Profesionalizantes III. Para PP II solo prevé *"coordinación, orientación y supervisión del docente a cargo"*.

Cuando el calendario no alcanza, el mecanismo de cierre coherente con el módulo son las **jornadas de práctica en la organización**: la resolución define entornos formativos en organizaciones reales, de modo que una jornada de relevamiento en terreno es carga horaria del espacio.

El presupuesto horario se cierra **antes** de asignar contenidos a semanas. El procedimiento está en [`planificacion/`](../planificacion/#3-cerrar-el-presupuesto-horario--antes-de-asignar-contenidos).

---

## Fundamentación

El Campo de las Prácticas Profesionalizantes está destinado, según la resolución, a *"posibilitar la integración y contrastación de los saberes construidos en la formación de los campos descriptos, y garantizar la articulación teoría-práctica […] a través del acercamiento de los estudiantes a situaciones reales de trabajo"*.

Dentro de ese campo, Prácticas Profesionalizantes II tiene un objeto preciso: **el análisis y la evaluación de proyectos reales en organizaciones**.

La resolución establece que las prácticas se desarrollan *"a partir del trabajo con proyecto en organizaciones (públicas o privadas) o sistemas de información como organización"*, y que *"los estudiantes deberán documentar las acciones a partir de la elaboración de informes técnicos"*.

De allí se desprenden los tres rasgos que estructuran la materia:

1. **El objeto es el proyecto**, no la tecnología. Se estudia cómo se concibe, se dimensiona, se valora y se conduce un proyecto dentro de una organización.
2. **El ámbito es real.** Una organización concreta, o un sistema de información tratado como organización.
3. **El entregable característico es el informe técnico.** Toda práctica se documenta.

El módulo recupera los saberes de **Sistemas y Organizaciones** y **Prácticas Profesionalizantes I** (1.º año), y articula con **Ingeniería en Software I**, **Estadística**, **Sistemas Operativos** y **Algoritmos y Estructuras de Datos II**, cursadas en paralelo.

### Delimitación con las materias del mismo año

Para evitar superposiciones, el programa deja fuera de su desarrollo los contenidos que el diseño curricular asigna a otros espacios:

| Contenido | Espacio curricular al que corresponde | Tratamiento en esta materia |
|---|---|---|
| Elicitación de requisitos, entrevistas, JAD, IEEE 830 | Ingeniería en Software I | Se aplica, no se enseña |
| POO, diagrama de clases, relaciones UML, catálogo de patrones de diseño, refactoring | Algoritmos y Estructuras de Datos II | Se articula en la Unidad 16, aplicado al proyecto |
| Perfil profesional y rol del analista | Prácticas Profesionalizantes I | Se recupera en la Unidad 1 |

---

## Capacidades profesionales

Las que fija la resolución para este módulo. Se espera que al finalizar el cursado los estudiantes sean capaces de:

| | Capacidad | Unidades |
|---|---|---|
| C1 | Conocer aspectos y características de los proyectos que se desarrollan en las organizaciones | 1, 3, 5 |
| C2 | Analizar y evaluar los proyectos de las organizaciones | 4, 7, 9 |
| C3 | Analizar la viabilidad y costos del proyecto | 9 |
| C4 | Elaborar informes técnicos sobre el análisis del proyecto | 17, y transversal a todas las entregas |
| C5 | Reconocer el rol del analista de sistemas en relación a la gestión de un proyecto en la organización | 1, 2, 11 |

---

## Ejes transversales

La resolución define tres ejes que *"deberán ser integrados en forma continua al desarrollo de la propuesta formativa"* de toda la carrera. No son unidades: atraviesan todas.

### Relación entre avances tecnológicos y las organizaciones

Cada unidad se plantea desde el efecto que la tecnología produce sobre la organización que la adopta, no desde la tecnología en sí.

### Ética profesional

La resolución pide *"el desplazamiento del énfasis depositado en lo normativo, instrumental y técnico hacia la creatividad y el compromiso en la toma de decisiones"*.

Se trabaja en situaciones concretas que aparecen a lo largo del año: estimar por debajo para ganar un proyecto, ocultar un atraso, documentar de forma incompleta, comprometer un plazo que se sabe inviable, usar datos de una organización sin autorización. Tiene tratamiento explícito en la Unidad 2 y se retoma en las Unidades 8, 9 y 12.

### Comunicación

*"Deberá ser trabajada de manera transversal […] atendiendo a los objetivos, a los destinatarios, al contenido, al soporte y a la finalidad comunicacional prevista en cada caso."*

Tiene tratamiento explícito en la Unidad 2 y se evalúa en cada entrega y en la defensa final.

---

## Organización

Cinco módulos, diecisiete unidades, 30 semanas.

| Módulo | Eje | Unidades | Semanas |
|---|---|---|---|
| **I** | El analista, la organización y el proyecto | 1 – 3 | 4 |
| **II** | Diagnóstico y definición del proyecto | 4 – 6 | 5 |
| **III** | Medición, estimación y viabilidad | 7 – 9 | 5 |
| **IV** | Planificación y riesgo | 10 – 12 | 5 |
| **V** | Configuración, implementación y cierre | 13 – 17 | 8 |
| — | Evaluación y defensa | — | 3 |
| | | **17 unidades** | **30** |

La materia abre con una clase de **presentación** ([`unidades/00-presentacion/`](../unidades/00-presentacion/)), que no constituye una unidad de contenido.

---

# Módulo I — El analista, la organización y el proyecto

## Unidad 1 — El analista de sistemas y el proyecto en la organización

**Duración:** 1 semana · **Material:** [`unidades/01-el-analista-y-el-proyecto/`](../unidades/01-el-analista-y-el-proyecto/) · **Capacidades:** C1, C5

Recuperación de Prácticas Profesionalizantes I, orientada al objeto de esta materia.

### Contenidos

- El rol del analista y su lugar en el equipo interdisciplinario _(recuperación de PP I)_.
- El analista como puente entre la organización y el equipo técnico.
- Qué es un proyecto dentro de una organización: objetivo, alcance, usuarios, recursos, tiempo y entregables.
- Tipos de proyectos que las organizaciones desarrollan.
- Por qué fracasan los proyectos: comenzar a construir antes de comprender el problema.

### Bibliografía

- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Capítulo sobre gestión de proyectos.
- Sommerville, I. *Ingeniería del Software.* Capítulo introductorio.
- [SWEBOK — Software Engineering Body of Knowledge](https://www.computer.org/education/bodies-of-knowledge/software-engineering)

---

## Unidad 2 — Comunicación y ética profesional

**Duración:** 1 semana · **Capacidades:** C4, C5 · **Ejes transversales:** comunicación, ética

### Contenidos

- La comunicación como competencia profesional central.
- Análisis del destinatario: no es lo mismo hablar con un programador, un gerente, un médico o un docente.
- Adaptación del lenguaje y del nivel de detalle.
- Traducción entre el lenguaje del dominio y el lenguaje técnico.
- Comunicación de malas noticias: atrasos, desvíos y cambios de alcance.
- Ética profesional en la toma de decisiones: compromisos inviables, estimaciones deliberadamente bajas, uso de información de la organización, confidencialidad.
- Responsabilidad del analista sobre lo que documenta y lo que firma.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Capítulo sobre comunicación con el cliente.
- [Write the Docs — Guía de comunicación técnica](https://www.writethedocs.org/guide/)
- [ACM Code of Ethics and Professional Conduct](https://www.acm.org/code-of-ethics)

---

## Unidad 3 — Metodologías tradicionales y ágiles

**Duración:** 2 semanas · **Material:** [`unidades/03-metodologias/`](../unidades/03-metodologias/) · **Capacidades:** C1

### Contenidos

- El ciclo de vida del software.
- Metodologías tradicionales: planificación extensa, etapas secuenciales, modelo en cascada.
- Modelos incrementales y evolutivos. Prototipado.
- Metodologías ágiles: iteraciones, entregas frecuentes, adaptación al cambio.
- El Manifiesto Ágil y sus principios.
- Scrum: roles, eventos y artefactos.
- Criterios para elegir una metodología según el contexto de la organización.

### Bibliografía

- [Manifiesto por el Desarrollo Ágil de Software](https://agilemanifesto.org/iso/es/manifesto.html) — versión en español
- [The Scrum Guide](https://scrumguides.org/) · [Descargas en español](https://scrumguides.org/download.html)
- [Atlassian — Guía de Scrum](https://www.atlassian.com/es/agile/scrum)
- [Microsoft Learn — ¿Qué es Agile?](https://learn.microsoft.com/es-es/devops/plan/what-is-agile)
- Sommerville, I. *Ingeniería del Software.* Capítulos sobre procesos y desarrollo ágil.

---

# Módulo II — Diagnóstico y definición del proyecto

## Unidad 4 — Diagnóstico organizacional: FODA y técnicas de análisis

**Duración:** 1 semana · **Capacidades:** C2

### Contenidos

- Qué es un diagnóstico organizacional y para qué sirve antes de proponer una solución.
- Técnicas de diagnóstico: observación, relevamiento documental, análisis de procesos.
- **Análisis FODA:** fortalezas, oportunidades, debilidades y amenazas.
- Construcción de una matriz FODA sobre una organización real.
- Del diagnóstico a la identificación de oportunidades de proyecto.
- Errores frecuentes: confundir síntoma con problema, y diagnosticar con la solución ya decidida.

### Bibliografía

- Sommerville, I. *Ingeniería del Software.* Capítulo sobre sistemas socio-técnicos y su contexto organizacional.
- Pressman, R. *Ingeniería del Software.* Sección sobre análisis del dominio del problema.

---

## Unidad 5 — El alcance del proyecto y las 4P

**Duración:** 2 semanas · **Capacidades:** C1, C2

### Contenidos

- Qué define el alcance: qué hará y qué **no** hará el sistema.
- Características de un buen alcance: claridad, precisión, límites y lenguaje técnico simple.
- Detección y corrección de frases ambiguas.
- El documento de alcance como entregable y como acuerdo con la organización.
- Las 4P del proyecto:
  - **Personal** — quiénes trabajan, roles y habilidades.
  - **Producto** — qué se va a construir y qué lo caracteriza.
  - **Proceso** — cómo se va a trabajar, metodología elegida.
  - **Proyecto** — organización general, tiempos y recursos.
- Gestión de cambios de alcance.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Capítulo sobre las 4P.
- Project Management Institute. [*Guía PMBOK*](https://www.pmi.org/standards/pmbok). Área de Gestión del Alcance. _(acceso pago)_

---

## Unidad 6 — Gestión y planificación. El plan de proyecto

**Duración:** 2 semanas · **Material:** [`unidades/06-gestion-y-planificacion/`](../unidades/06-gestion-y-planificacion/) · **Capacidades:** C1, C5

### Contenidos

- Gestión de proyectos: organizar, asignar, controlar y ajustar.
- Planificar como decidir por anticipado.
- Hitos y entregas: definición y diferencia.
- El plan de proyecto y sus componentes.
- Descomposición del trabajo en tareas estimables.
- Introducción a métricas y estimación _(se desarrollan en las Unidades 7 y 8)_.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Capítulos sobre gestión de proyectos.
- Sommerville, I. *Ingeniería del Software.* Capítulo sobre planificación de proyectos.
- Project Management Institute. [*Guía PMBOK*](https://www.pmi.org/standards/pmbok). Áreas de Cronograma y Costos. _(acceso pago)_

---

# Módulo III — Medición, estimación y viabilidad

## Unidad 7 — Métricas del proceso y del proyecto

**Duración:** 2 semanas · **Capacidades:** C2

### Contenidos

- Para qué se mide: convertir impresiones en información verificable.
- **Clasificación de las métricas.**
- **Métricas del proceso** y **métricas del proyecto**: qué mide cada una y para quién.
- **Métricas orientadas al tamaño:** líneas de código, sus usos y sus límites.
- **Métricas orientadas a la función:** puntos función, factores de complejidad, cálculo.
- **Métricas orientadas a casos de uso.**
- **Recopilación, cálculo y evaluación de métricas.**
- Interpretación de desvíos.
- Riesgo de gestionar para mejorar el indicador en lugar de para mejorar el proyecto.

> Articula con **Estadística** (2.º año) para el tratamiento de los datos recopilados.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Capítulos sobre métricas del proceso y del proyecto, y métricas orientadas a la función.
- Sommerville, I. *Ingeniería del Software.* Sección sobre medición del software.
- [IFPUG — International Function Point Users Group](https://www.ifpug.org/)

---

## Unidad 8 — Estimación y modelos empíricos

**Duración:** 1 semana · **Capacidades:** C2, C3 · **Eje transversal:** ética

### Contenidos

- Estimar: predecir esfuerzo de forma fundamentada, no adivinar.
- **Técnicas de descomposición.**
- Juicio experto y estimación por analogía.
- Estimación por tres valores: optimista, más probable y pesimista.
- **Modelos empíricos: COCOMO.** Modos orgánico, semiacoplado y empotrado. Cálculo de esfuerzo y duración.
- Por qué fallan las estimaciones.
- Registro del desvío entre estimación y tiempo real como insumo de mejora.
- Dimensión ética: la estimación ajustada a la fecha deseada en lugar del trabajo real.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Capítulo sobre estimación, técnicas de descomposición y modelos empíricos.
- [Atlassian — Estimación en gestión de proyectos](https://www.atlassian.com/es/agile/project-management/estimation)

---

## Unidad 9 — Viabilidad y costos del proyecto

**Duración:** 2 semanas · **Capacidades:** C2, C3 · **Eje transversal:** ética

### Contenidos

- Qué significa que un proyecto sea viable.
- Dimensiones de la viabilidad: técnica, operativa, económica, temporal y legal.
- Estudio de viabilidad como entregable previo a la decisión de avanzar.
- Estructura de costos de un proyecto de software: recursos humanos, infraestructura, licencias, capacitación, mantenimiento.
- Costo directo e indirecto. Costo de oportunidad.
- Relación costo-beneficio. Retorno de la inversión.
- Presentación de la evaluación de viabilidad a quien decide.
- Dimensión ética: informar la inviabilidad de un proyecto que la organización quiere realizar.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Sección sobre estimación de costos y análisis de viabilidad.
- Sommerville, I. *Ingeniería del Software.* Sección sobre estudio de viabilidad.
- Project Management Institute. [*Guía PMBOK*](https://www.pmi.org/standards/pmbok). Área de Gestión de los Costos. _(acceso pago)_

---

# Módulo IV — Planificación y riesgo

## Unidad 10 — Planificación temporal: Gantt y PERT

**Duración:** 2 semanas · **Capacidades:** C1, C2

### Contenidos

- **Calendarización del proyecto.**
- **Distribución del esfuerzo** a lo largo del ciclo de vida.
- Dependencias entre tareas. Tareas secuenciales y paralelas.
- **Redes de tareas.**
- **Diagrama de Gantt:** barras, hitos y dependencias.
- **Método PERT:** red de actividades, estimación por tres valores.
- **Camino crítico** y holgura.
- **Seguimiento de la planificación:** avance real contra avance previsto.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Capítulo sobre planificación temporal y seguimiento.
- [Atlassian — Diagramas de Gantt](https://www.atlassian.com/es/agile/project-management/gantt-chart)
- [IBM — ¿Qué es un diagrama de Gantt?](https://www.ibm.com/think/topics/gantt-chart)
- [Mermaid — Diagramas de Gantt como texto versionable](https://mermaid.js.org/)

---

## Unidad 11 — Planificación organizativa del equipo

**Duración:** 1 semana · **Capacidades:** C5

### Contenidos

- **Planificación organizativa del equipo y del proyecto.**
- Estructuras de equipo y criterios para elegirlas.
- Asignación de roles y responsabilidades.
- Relación entre tamaño del equipo, comunicación y productividad.
- Coordinación entre equipos.
- El analista en la conducción del equipo.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Capítulo sobre el personal del proyecto y estructuras de equipo.
- Sommerville, I. *Ingeniería del Software.* Capítulo sobre gestión de personal.

---

## Unidad 12 — Gestión del riesgo y plan de RSGR

**Duración:** 2 semanas · **Capacidades:** C2 · **Eje transversal:** ética

### Contenidos

- Qué es un riesgo y en qué se diferencia de un problema.
- **Identificación de riesgos:** técnicos, de proyecto, de negocio y de personal.
- **Proyección del riesgo:** probabilidad e impacto.
- Matriz de riesgos y priorización.
- **Reducción, supervisión y gestión del riesgo.** El **plan de RSGR**.
- **Planes de contingencia.**
- Seguimiento de riesgos durante el proyecto.
- Dimensión ética: el riesgo conocido y no comunicado.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Capítulo sobre gestión del riesgo y el plan RSGR.
- Sommerville, I. *Ingeniería del Software.* Sección sobre gestión de riesgos.
- [SEI (Carnegie Mellon) — Risk Management](https://www.sei.cmu.edu/our-work/risk-management/)

---

# Módulo V — Configuración, implementación y cierre

## Unidad 13 — Gestión de la Configuración del Software

**Duración:** 2 semanas · **Capacidades:** C1, C4

### Contenidos

- Qué es la **Gestión de la Configuración del Software (GCS)** y qué problema resuelve.
- Elementos de configuración.
- **Línea base:** definición, establecimiento y aprobación.
- **Gestión del cambio:** solicitud, evaluación de impacto, aprobación e incorporación.
- **Control de versiones.** Git como herramienta: repositorio, commit, rama, fusión, historial.
- Trabajo colaborativo: ramas por funcionalidad, revisión entre pares, resolución de conflictos.
- **Auditoría de la configuración.**
- El repositorio como documentación viva del proyecto.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Capítulo sobre gestión de la configuración del software.
- [Pro Git — Chacon & Straub](https://git-scm.com/book/es/v2) — libro completo y gratuito en español
- [Documentación oficial de GitHub en español](https://docs.github.com/es) · [Pull requests](https://docs.github.com/es/pull-requests)
- [Atlassian — Glosario de Git](https://www.atlassian.com/es/git/glossary)
- [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/)

---

## Unidad 14 — Implementación, estándares y depuración

**Duración:** 1 semana · **Capacidades:** C1

### Contenidos

- La etapa de implementación dentro del proyecto.
- **Estándares de programación y procedimientos.**
- **Pautas para la programación:** legibilidad, convenciones, revisión.
- Por qué una organización adopta estándares y qué pierde si no lo hace.
- **La depuración:** proceso, estrategias y corrección del error.
- Distinción entre error, defecto y falla.
- Registro y seguimiento de defectos.

> Articula con **Algoritmos y Estructuras de Datos II**, que desarrolla las técnicas de testing y refactoring.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Capítulos sobre implementación y depuración.
- Sommerville, I. *Ingeniería del Software.* Sección sobre verificación y validación.

---

## Unidad 15 — Entrega, entrenamiento y mantenimiento

**Duración:** 2 semanas · **Capacidades:** C1, C4

### Contenidos

- **Entrega** del sistema a la organización. Puesta en producción.
- **Entrenamiento:** capacitación de usuarios y transferencia de conocimiento.
- **Mantenimiento y evolución del software.**
- **Tipos de mantenimiento:** correctivo, adaptativo, perfectivo y preventivo.
- **Métricas del mantenimiento.**
- **Técnicas y herramientas para el mantenimiento.**
- El costo del mantenimiento en el ciclo de vida total del sistema.

### Bibliografía

- Pressman, R. *Ingeniería del Software.* Capítulos sobre mantenimiento y evolución del software.
- Sommerville, I. *Ingeniería del Software.* Capítulo sobre evolución del software.

---

## Unidad 16 — Modelado del proyecto con UML

**Duración:** 1 semana · **Capacidades:** C4

Unidad de **articulación** con Algoritmos y Estructuras de Datos II, que es donde se enseña el modelado orientado a objetos. Aquí se aplica al proyecto propio, sin desarrollar la teoría.

### Contenidos

- UML como lenguaje para comunicar el diseño a la organización y al equipo.
- Lectura e interpretación de un diagrama de clases.
- Aplicación al proyecto: identificar las entidades del dominio relevado.
- Diagramas como texto versionable, integrados a la gestión de configuración.

### Bibliografía

- [OMG — Especificación oficial de UML](https://www.omg.org/spec/UML/)
- [PlantUML en español](https://plantuml.com/es/) · [Mermaid](https://mermaid.js.org/)
- Sommerville, I. *Ingeniería del Software.* Capítulo sobre modelado de sistemas.

---

## Unidad 17 — Documentación técnica y el informe técnico

**Duración:** 2 semanas · **Capacidades:** C4

El informe técnico es el entregable que la resolución señala como característico de este módulo. Se trabaja en esta unidad y se practica en cada entrega del año.

### Contenidos

- Qué documentar, para quién y con qué nivel de detalle.
- Tipos de documento: tutorial, guía práctica, referencia y explicación.
- **El informe técnico:** estructura, destinatario, fundamentación de conclusiones y recomendaciones.
- Documentación de requerimientos, de diseño y de usuario.
- Registro de decisiones técnicas y su fundamentación.
- Documentación como texto versionable, integrada a la gestión de configuración.
- Mantenimiento de la documentación.
- Armado del informe final del proyecto integrador.

### Bibliografía

- [Diátaxis — Marco para estructurar documentación técnica](https://diataxis.fr/)
- [Write the Docs — Guía de documentación](https://www.writethedocs.org/guide/)
- [Markdown Guide](https://www.markdownguide.org/)
- Sommerville, I. *Ingeniería del Software.* Sección sobre documentación.

---

# Proyecto integrador

El proyecto integrador atraviesa toda la cursada y articula las diecisiete unidades.

Conforme a la resolución, el trabajo se desarrolla sobre **una organización real** —pública o privada— o sobre un **sistema de información tratado como organización**, y se documenta mediante **informes técnicos**.

Cada grupo funciona como una consultora informática. El docente asume alternativamente los roles de cliente, líder de proyecto, consultor, director y revisor técnico.

## Entregas

| Entrega | Unidad que la habilita |
|---|---|
| Informe de relevamiento de la organización | 1 – 2 |
| Diagnóstico organizacional con matriz FODA | 4 |
| Documento de alcance y análisis con las 4P | 5 |
| Plan de proyecto con hitos y entregas | 6 |
| Informe de métricas del proyecto | 7 |
| Estimación de esfuerzo con COCOMO | 8 |
| **Informe de viabilidad y costos** | 9 |
| Cronograma con Gantt, PERT y camino crítico | 10 |
| Plan de RSGR y matriz de riesgos | 12 |
| Repositorio del proyecto bajo GCS | 13 |
| Plan de entrega, entrenamiento y mantenimiento | 15 |
| Modelado UML del dominio | 16 |
| **Informe técnico final** | 17 |
| Presentación y defensa oral | — |

Los antecedentes y entregas de ciclos anteriores se conservan en [`proyecto-integrador/`](../proyecto-integrador/).

---

# Régimen de evaluación

## Instancias

| Instancia | Cantidad | Descripción |
|---|---|---|
| Exámenes escritos | 2 por año | Uno por cuatrimestre, con dos temas equivalentes |
| Trabajos prácticos | Según ciclo | Entrega grupal documentada |
| Proyecto integrador | Continuo | Evaluado por avances y en la defensa final |

## Estructura del examen escrito

| | |
|---|---|
| Duración | 60 minutos |
| Puntaje total | 100 puntos |
| Parte A — opción múltiple | 48 puntos (12 preguntas × 4) |
| Parte B — resolución de un caso | 52 puntos |
| Aprobación | 60 / 100 |

## Escala de calificación

| Puntaje | Nota | Resultado |
|---|---|---|
| 90 – 100 | 10 | Sobresaliente |
| 75 – 89 | 8 – 9 | Muy bueno |
| 60 – 74 | 6 – 7 | Aprobado |
| Menos de 60 | — | Desaprobado |

## Criterios de evaluación del proyecto integrador

- Coherencia entre diagnóstico, alcance, plan y resultado obtenido.
- Fundamentación de la viabilidad y los costos propuestos.
- Calidad y pertinencia de los informes técnicos producidos.
- Capacidad de fundamentar las decisiones tomadas.
- Adecuación del lenguaje al destinatario.
- Evidencia de trabajo colaborativo real, verificable en el repositorio.
- Honestidad en el registro de desvíos y dificultades.

---

# Correspondencia con la Resolución 6790/19

Cada eje de contenido del módulo oficial y la unidad que lo desarrolla.

| Eje de contenido oficial | Unidad |
|---|---|
| Metodologías tradicionales y ágiles | 3 |
| Gestión de proyectos. Conceptos | 6 |
| El problema de las 4 "P" (personal, producto, proceso, proyecto) | 5 |
| Actividades de gestión, planificación del proyecto, hitos y entregas | 6 |
| El plan de proyecto | 6 |
| Métricas y estimaciones | 7, 8 |
| Técnicas de diagnóstico. FODA | 4 |
| Clasificación de las métricas. Métricas del proceso y del proyecto | 7 |
| Métricas orientadas al tamaño, a la función, a casos de uso | 7 |
| Recopilación, cálculo y evaluación de métricas | 7 |
| Estimación de proyectos. Técnicas de descomposición | 8 |
| Modelos empíricos (COCOMO) | 8 |
| Planificación temporal: calendarización, distribución del esfuerzo, redes de tareas, seguimiento | 10 |
| Métodos PERT, Gantt | 10 |
| Planificación organizativa: del equipo y del proyecto | 11 |
| Gestión del riesgo: identificación, proyección, impacto, reducción, supervisión y gestión | 12 |
| Planes de contingencia. El plan de RSGR | 12 |
| GCS. Gestión de la configuración del software: línea base, gestión del cambio, control de versiones, auditoría | 13 |
| Implementación. Estándares de programación y procedimientos. Pautas para la programación | 14 |
| La depuración: proceso, estrategia, corrección del error | 14 |
| Entrega. Entrenamiento | 15 |
| Mantenimiento. Evolución del software. Tipos: correctivo, adaptativo, perfectivo, preventivo | 15 |
| Métricas del mantenimiento, técnicas y herramientas | 15 |
| Documentación | 17 |

Además, la capacidad profesional *"analizar la viabilidad y costos del proyecto"* se desarrolla en la **Unidad 9**, que no tiene un eje de contenido propio en la resolución pero es exigible por corresponder a una capacidad declarada.

---

# Bibliografía general

## Libros

- Pressman, Roger S. *Ingeniería del Software: Un enfoque práctico.* McGraw-Hill. — Referencia principal de la materia.
- Sommerville, Ian. *Ingeniería del Software.* Pearson.
- Project Management Institute. [*Guía de los Fundamentos para la Dirección de Proyectos (Guía PMBOK)*](https://www.pmi.org/standards/pmbok). _(acceso pago)_

## Recursos en línea

| Recurso | Tema |
|---|---|
| [Manifiesto Ágil (español)](https://agilemanifesto.org/iso/es/manifesto.html) | Metodologías ágiles |
| [The Scrum Guide](https://scrumguides.org/) | Scrum |
| [Atlassian — Scrum](https://www.atlassian.com/es/agile/scrum) · [Estimación](https://www.atlassian.com/es/agile/project-management/estimation) · [Gantt](https://www.atlassian.com/es/agile/project-management/gantt-chart) | Gestión de proyectos |
| [IBM — Diagrama de Gantt](https://www.ibm.com/think/topics/gantt-chart) | Planificación temporal |
| [IFPUG](https://www.ifpug.org/) | Puntos función |
| [SEI — Risk Management](https://www.sei.cmu.edu/our-work/risk-management/) | Gestión de riesgos |
| [Pro Git (español, gratuito)](https://git-scm.com/book/es/v2) | Control de versiones |
| [Documentación de GitHub (español)](https://docs.github.com/es) · [Glosario Atlassian](https://www.atlassian.com/es/git/glossary) | Git y GitHub |
| [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) | Gestión del cambio |
| [OMG — UML](https://www.omg.org/spec/UML/) · [PlantUML](https://plantuml.com/es/) · [Mermaid](https://mermaid.js.org/) | Modelado |
| [Diátaxis](https://diataxis.fr/) · [Write the Docs](https://www.writethedocs.org/guide/) · [Markdown Guide](https://www.markdownguide.org/) | Documentación |
| [ACM Code of Ethics](https://www.acm.org/code-of-ethics) | Ética profesional |
| [SWEBOK](https://www.computer.org/education/bodies-of-knowledge/software-engineering) | Cuerpo de conocimiento |

---

## Control de versiones del programa

| Ciclo | Cambios |
|---|---|
| 2026 — v1 | Versión inicial del programa formalizado. |
| 2026 — v2 | Reajuste completo tras la validación contra la Resolución TSAS 6790/19. Se incorporan FODA, clasificación de métricas, COCOMO, viabilidad y costos, planificación organizativa, GCS como marco, implementación y depuración, entrega, entrenamiento y mantenimiento, y el eje transversal de ética profesional. POO y patrones de diseño se retiran por corresponder a Algoritmos y Estructuras de Datos II; UML queda como unidad de articulación aplicada al proyecto. |

Al cierre de cada ciclo lectivo conviene registrar aquí qué se modificó y por qué.
