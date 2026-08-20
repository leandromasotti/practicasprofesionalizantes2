# Unidad 17
# Documentación técnica y el informe técnico

> "La documentación no es lo que se escribe al final del proyecto. Es lo que permite que el proyecto exista para alguien más que quien lo hizo."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Decidir qué documentar, para quién y con qué nivel de detalle.
- Distinguir los cuatro tipos de documento y elegir el adecuado.
- **Redactar un informe técnico** con su estructura completa.
- Registrar decisiones técnicas con su fundamento.
- Producir documentación como texto versionable.
- Mantener la documentación actualizada.
- Armar el informe final del proyecto integrador.

> El **informe técnico** es el entregable que la resolución señala como característico de este módulo: *"los estudiantes deberán documentar las acciones a partir de la elaboración de informes técnicos"*. Esta unidad lo formaliza, pero se practicó en cada entrega del año.

---

# El problema de la documentación

La documentación tiene mala fama por buenas razones. Casi siempre se hace mal:

- se escribe al final, cuando nadie recuerda por qué se decidió lo que se decidió;
- se escribe para cumplir, no para que alguien la lea;
- describe lo obvio y omite lo que hace falta;
- queda desactualizada en semanas;
- nadie la abre.

El problema no es que documentar sea inútil. Es que **documentar sin destinatario** es inútil.

## Las dos preguntas previas

Antes de escribir una línea:

1. **¿Quién va a leer esto?**
2. **¿Qué tiene que poder hacer después de leerlo?**

Si no hay respuesta a las dos, no hay que escribir el documento. No porque documentar sea malo, sino porque un documento sin destinatario es trabajo que nadie va a usar y que además habrá que mantener.

> Es el mismo análisis del destinatario de la Unidad 2, aplicado a la escritura técnica.

---

# Qué documentar

## El criterio

Se documenta lo que **no se puede recuperar de otra forma**.

| Se documenta | No hace falta documentar |
|---|---|
| Por qué se tomó una decisión | Qué hace el código, si el código es legible |
| Lo que el sistema no hace y por qué | Lo que se ve en la pantalla |
| Las reglas de negocio y su fuente | Lo que se puede deducir en dos minutos |
| Los supuestos y las restricciones | Lo que va a cambiar la semana que viene |
| Los defectos conocidos | |
| Los puntos frágiles | |

La asimetría es notable: **el por qué no se puede reconstruir; el qué, casi siempre sí**.

Dentro de seis meses, cualquiera puede leer el código y ver qué hace. Nadie puede reconstruir por qué se eligió eso en lugar de la alternativa, si no quedó escrito.

## Con qué nivel de detalle

El nivel de detalle lo determina el destinatario, no el autor.

| Destinatario | Nivel |
|---|---|
| Dirección de la organización | Conclusiones, costos, riesgos, decisiones a tomar |
| Usuario final | Cómo hacer su tarea, paso a paso |
| Quien mantendrá el sistema | Estructura, decisiones de diseño, puntos frágiles |
| Auditoría | Trazabilidad, aprobaciones, evidencia |
| Equipo actual | Acuerdos, convenciones, pendientes |

---

# Los cuatro tipos de documento

Existe un marco —**Diátaxis**— que ordena la documentación técnica en cuatro tipos según dos ejes: si sirve para *aprender* o para *trabajar*, y si es *práctico* o *teórico*.

| Tipo | Responde a | El lector está… |
|---|---|---|
| **Tutorial** | "Enseñame a usar esto" | Aprendiendo, guiado paso a paso |
| **Guía práctica** | "Cómo hago tal cosa" | Trabajando, con un objetivo concreto |
| **Referencia** | "Cuáles son los datos exactos" | Consultando un dato preciso |
| **Explicación** | "Por qué funciona así" | Entendiendo el contexto |

## Por qué la distinción importa

Porque **mezclarlos arruina los cuatro**.

| Mezcla | Resultado |
|---|---|
| Tutorial con explicaciones de fondo | El principiante se pierde |
| Referencia con tutorial | Quien busca un dato tiene que leer una lección |
| Guía práctica con teoría | Quien tiene una tarea urgente no encuentra el paso |
| Explicación con pasos | Queda un documento que no enseña ni explica |

> El manual de 60 páginas que nadie lee suele ser los cuatro tipos mezclados en un solo archivo.

## Aplicado a un proyecto de software

| Documento | Tipo |
|---|---|
| Guía rápida del usuario operativo | Guía práctica |
| Material de capacitación | Tutorial |
| Manual de usuario completo | Referencia |
| Documento de decisiones de diseño | Explicación |
| Informe de viabilidad | Explicación |
| Especificación de requerimientos | Referencia |

---

# El informe técnico

Es el formato central de esta materia. Un informe técnico presenta un **análisis** y llega a una **conclusión fundamentada**, dirigido a alguien que tiene que decidir.

No es una descripción de lo que se hizo. Es un argumento.

## Estructura

| Sección | Contenido | Extensión |
|---|---|---|
| **1. Objeto** | Qué se analizó y por qué | 1 párrafo |
| **2. Conclusión y recomendación** | La respuesta, al principio | 1 párrafo |
| **3. Alcance del análisis** | Qué se incluyó y qué quedó afuera | Breve |
| **4. Metodología** | Cómo se obtuvo la información | Breve |
| **5. Desarrollo** | El análisis, con los datos | El cuerpo |
| **6. Supuestos** | Lo que se dio por cierto | Lista |
| **7. Limitaciones** | Qué no se pudo verificar | Lista |
| **8. Alternativas** | Los cursos de acción posibles | Tabla |
| **9. Recomendación fundamentada** | Qué conviene hacer y por qué | 1-2 párrafos |
| **10. Anexos** | Datos, planillas, cálculos | Lo que haga falta |

## La conclusión va segunda, no última

Es la regla que más cambia la utilidad de un informe.

Quien decide lee la conclusión, y después —si le interesa o si duda— busca el fundamento. Un informe que reserva la conclusión para la última página obliga a leer todo o a no leer nada.

> Un informe técnico no es una novela policial. El final va al principio.

## Las secciones que se omiten y hacen la diferencia

**Supuestos.** Todo análisis se apoya en cosas que se dieron por ciertas. Declararlas permite que el lector evalúe la solidez de la conclusión, y que el análisis se pueda revisar si un supuesto cambia.

**Limitaciones.** Lo que no se pudo verificar. Omitirlas convierte una conclusión provisoria en una afirmación categórica.

**Alternativas.** Un informe con un solo curso de acción no informa una decisión: la impone.

## Cómo se escribe

| ❌ | ✅ |
|---|---|
| "Se considera que el sistema podría eventualmente presentar dificultades" | "El sistema no soporta más de 50 usuarios simultáneos; el club espera 200 en temporada" |
| "Se realizaron diversas tareas de relevamiento" | "Se entrevistó al presidente y a la administrativa, y se observó el cobro de cuotas durante dos jornadas" |
| "Los costos serían significativos" | "El costo es de $7.720.000, un 15 % por encima del presupuesto disponible" |
| "Se recomienda avanzar" | "Se recomienda avanzar con la etapa 1, que resuelve el 70 % de la pérdida actual y se recupera en 14 meses" |

Tres reglas:

1. **Afirmaciones verificables**, no impresiones.
2. **Números con su supuesto** al lado.
3. **Sin condicional evasivo.** El condicional se usa para hipótesis, no para no comprometerse.

---

# Registro de decisiones técnicas

Es la documentación con mejor relación entre esfuerzo y valor, y la que casi nadie hace.

## Formato

Una ficha corta por decisión:

| Campo | Contenido |
|---|---|
| **Decisión** | Qué se decidió |
| **Fecha** | Cuándo |
| **Contexto** | Qué problema había que resolver |
| **Alternativas consideradas** | Qué otras opciones había |
| **Fundamento** | Por qué se eligió esta |
| **Consecuencias** | Qué implica, incluido lo que se resigna |
| **Estado** | Vigente, revisada, revertida |

## Ejemplo

| | |
|---|---|
| **Decisión** | Migrar solo los socios activos; el histórico anterior a 2024 queda fuera del alcance |
| **Fecha** | 15/09/2026 |
| **Contexto** | La auditoría de la semana 1 encontró un 34 % de fichas con datos incompletos. Migrar todo requeriría unas 120 horas de limpieza manual |
| **Alternativas** | (a) Migrar todo con limpieza manual: +120 h, +3 semanas. (b) Migrar todo sin limpiar: arrastra errores de cobro. (c) Migrar solo activos: 300 de 800 fichas |
| **Fundamento** | La opción (c) conserva la funcionalidad operativa completa y elimina el riesgo de errores de cobro, con un costo de 40 h. El histórico se puede incorporar después sin rehacer nada |
| **Consecuencias** | El club no podrá consultar pagos anteriores a 2024 desde el sistema. Las fichas de papel se conservan como respaldo |
| **Estado** | Vigente |

## Por qué vale la pena

Dentro de un año alguien va a preguntar por qué el sistema no tiene el histórico. Sin esta ficha, la respuesta es "no sé, se hizo así". Con la ficha, la respuesta es un fundamento que se puede revisar y, si el contexto cambió, revertir con conocimiento.

> Una decisión sin registro no es una decisión: es una característica sin explicación.

---

# Documentación como texto versionable

## El principio

La documentación es un **elemento de configuración**, en el sentido de la Unidad 13. Debe estar en el mismo repositorio, con el mismo control de versiones, y cambiar en el mismo commit que lo que documenta.

## Por qué en texto

| Documento binario | Documento en texto |
|---|---|
| No se puede ver qué cambió entre versiones | El historial muestra cada cambio línea por línea |
| Requiere una aplicación específica | Se edita con cualquier editor |
| Se versiona con nombres de archivo | Se versiona con el control de versiones |
| Se separa del código y se desactualiza | Cambia junto con lo que documenta |

## Formatos

| Formato | Para qué |
|---|---|
| **Markdown** | Todo documento de texto |
| **Mermaid** | Diagramas, cronogramas, modelos |
| **CSV** | Datos tabulares |

## La regla que evita la desactualización

> **Un cambio que modifica el comportamiento y no actualiza la documentación está incompleto.**

Aplicada en la revisión entre pares de la Unidad 13, funciona: quien revisa un pull request verifica que la documentación acompañe. Es el único mecanismo que mantiene la documentación viva, porque no depende de que alguien se acuerde después.

---

# Mantenimiento de la documentación

## Documentación desactualizada es peor que ninguna

Un sistema sin documentación obliga a averiguar. Uno con documentación equivocada hace tomar decisiones sobre información falsa, con la confianza de estar informado.

En el caso de la Unidad 15, el manual describía tres pantallas que ya no existían. El efecto sobre un usuario nuevo es peor que no haber tenido manual.

## Cómo se mantiene

✔ La documentación cambia en el mismo commit que el cambio que la afecta.

✔ La revisión entre pares verifica que acompañe.

✔ Se documenta poco y se mantiene, en lugar de documentar mucho y abandonarlo.

✔ Se borra lo que ya no aplica. Un documento obsoleto se elimina, no se deja "por si acaso".

✔ Cada documento tiene fecha de última revisión.

> Menos documentación mantenida vale más que mucha documentación desactualizada. Es una decisión de alcance, y se toma igual que cualquier otra.

---

# El informe final del proyecto integrador

Es el entregable que integra todo el año.

## Estructura

| Sección | Contenido | De qué unidad viene |
|---|---|---|
| **Resumen ejecutivo** | Una página: qué se analizó, qué se concluyó, qué se recomienda | — |
| **1. La organización** | Qué hace, cómo funciona, qué releva | 1, 2 |
| **2. Diagnóstico** | Síntomas, problemas, causas, matriz FODA y su cruce | 4 |
| **3. Proyecto propuesto** | Alcance, exclusiones, supuestos, análisis 4P | 5 |
| **4. Metodología** | Elegida y fundamentada | 3 |
| **5. Dimensionamiento** | Puntos función y métricas definidas | 7 |
| **6. Estimación** | Descomposición, tres valores, COCOMO, contraste | 8 |
| **7. Viabilidad y costos** | Cinco dimensiones, costos, beneficios, recupero | 9 |
| **8. Plan de proyecto** | Tareas, hitos, entregas | 6 |
| **9. Cronograma** | Gantt, PERT, camino crítico | 10 |
| **10. Organización del equipo** | Estructura, roles, matriz de asignación | 11 |
| **11. Riesgos** | Matriz y plan de RSGR | 12 |
| **12. Modelo del dominio** | Diagrama de clases y preguntas pendientes | 16 |
| **13. Gestión de configuración** | Líneas base, registro de cambios, auditoría | 13 |
| **14. Plan de entrega y mantenimiento** | Puesta en producción, capacitación, mantenimiento | 15 |
| **15. Registro de decisiones** | Fichas de las decisiones tomadas | 17 |
| **16. Desvíos** | Qué se planificó, qué ocurrió, por qué | 6, 7 |
| **17. Conclusiones** | Qué se aprendió | — |
| **Anexos** | Planillas, cálculos, evidencia | — |

## La sección 16 es la que más se evalúa

El registro de desvíos entre lo planificado y lo ocurrido es la sección que demuestra si el grupo usó su plan o solo lo escribió.

Un informe donde el plan inicial coincide exactamente con lo ejecutado, en un proyecto de ocho meses, indica una de dos cosas: que se reescribió el plan al final, o que nunca se lo miró.

> Un desvío bien explicado se evalúa mejor que un plan supuestamente perfecto.

---

# Errores frecuentes

- **Documentar sin destinatario.**
- **Documentar el qué y omitir el por qué**, que es lo único irrecuperable.
- **Mezclar los cuatro tipos de documento** en un solo archivo.
- **Poner la conclusión al final** del informe técnico.
- **Omitir supuestos y limitaciones.**
- **Presentar un solo curso de acción.**
- **Usar el condicional evasivo** para no comprometerse.
- **No registrar las decisiones** ni su fundamento.
- **Entregar documentos binarios** fuera del control de versiones.
- **Dejar documentación obsoleta** "por si acaso".
- **Documentar todo al final**, cuando nadie recuerda los fundamentos.

---

# Buenas prácticas

✔ Definir destinatario y propósito antes de escribir.

✔ Documentar el por qué; el qué se recupera del producto.

✔ Un tipo de documento por archivo.

✔ La conclusión al principio.

✔ Declarar supuestos y limitaciones.

✔ Presentar al menos tres alternativas.

✔ Afirmaciones verificables y números con su supuesto.

✔ Registrar cada decisión con su fundamento y sus consecuencias.

✔ Documentación en texto, en el repositorio, cambiando junto con lo que documenta.

✔ Poco y mantenido, antes que mucho y abandonado.

---

# Caso de estudio

## Dos informes de viabilidad

Los dos analizan el mismo proyecto. Los dos recomiendan avanzar.

**Informe A** — 24 páginas.

> Comienza con la historia de la organización, sigue con un capítulo sobre la evolución de los sistemas de gestión, describe la metodología de relevamiento en detalle, presenta ocho páginas de datos relevados, analiza la viabilidad técnica en profundidad, y en la página 23 concluye: *"En virtud de lo expuesto, se considera que el proyecto resultaría viable y se recomendaría su realización."*

**Informe B** — 4 páginas.

> **Objeto:** evaluar la viabilidad del sistema de gestión de socios y cuotas.
>
> **Recomendación:** avanzar en dos etapas. La etapa 1 —socios y cuotas— resuelve el 70 % de la pérdida actual, cuesta $4.100.000 y se recupera en 14 meses.
>
> **Supuesto crítico:** que la morosidad recuperable sea del 3 % anual. Si fuera del 1 %, el recupero pasa a 20 meses y la recomendación se mantiene.
>
> **Limitación:** no se pudo verificar la calidad de los datos históricos; se auditó una muestra de 100 de 800 fichas.
>
> **Alternativas:** proyecto completo ($7.720.000, recupero 2,7 años) · dos etapas (recomendada) · no hacer nada (pérdida anual estimada $4.000.000).
>
> *(Sigue el desarrollo, y los datos completos en anexo.)*

### Para analizar

1. ¿Cuál de los dos informes permite decidir? ¿Por qué?
2. Identifique en el informe A tres problemas de redacción de los que la unidad enumera.
3. ¿Qué información contiene B que A no contiene?
4. El informe A tiene más trabajo invertido. ¿Por qué eso no lo hace mejor?
5. ¿Qué le agregaría al informe B?
6. Reescriba la conclusión del informe A aplicando las tres reglas de redacción.
7. ¿Dónde debería ir, en el informe B, el contenido de las ocho páginas de datos relevados del informe A?

---

# Aplicación profesional

Cada grupo entrega el **informe final del proyecto integrador**, con la estructura de diecisiete secciones.

Además:

- el **registro de decisiones** del proyecto, con un mínimo de seis fichas completas;
- toda la documentación en el repositorio, en formato de texto versionable;
- la **guía rápida** del usuario operativo, de una página.

El informe se defiende oralmente. En la defensa se evalúa la capacidad de explicar las decisiones a un interlocutor no técnico y de sostenerlas cuando se las cuestiona.

> Con esta unidad se cierra el recorrido del año. El informe final no es un documento nuevo: es la integración de los quince entregables producidos desde marzo.

---

# Resumen

En esta unidad aprendimos que:

- Documentar sin destinatario es trabajo que nadie usará y que habrá que mantener.
- Se documenta lo que no se puede recuperar de otra forma: el por qué, no el qué.
- Los cuatro tipos de documento —tutorial, guía práctica, referencia y explicación— se arruinan al mezclarse.
- Un informe técnico es un argumento con una conclusión fundamentada, no una descripción de lo hecho.
- La conclusión va al principio.
- Supuestos, limitaciones y alternativas son las secciones que se omiten y las que hacen la diferencia.
- El condicional evasivo se usa para no comprometerse, y en un informe técnico no corresponde.
- Una decisión sin registro es una característica sin explicación.
- La documentación es un elemento de configuración y cambia en el mismo commit que lo que documenta.
- Documentación desactualizada es peor que ninguna.
- Menos documentación mantenida vale más que mucha abandonada.
- En el informe final, la sección de desvíos es la que demuestra si el plan se usó.

---

# Actividad práctica

## Informe final y registro de decisiones

**1. Registro de decisiones**

Completen seis fichas de decisión del proyecto, con contexto, alternativas, fundamento y consecuencias. Al menos una debe corresponder a una decisión que hoy revertirían.

**2. Auditoría de tipos**

Revisen la documentación que produjeron durante el año. Clasifiquen cada documento en uno de los cuatro tipos. Identifiquen los que mezclan tipos y propongan cómo separarlos.

**3. Informe final**

Armen el informe con las diecisiete secciones. El resumen ejecutivo debe ser autosuficiente: quien lea solo esa página tiene que poder decidir.

**4. Sección de desvíos**

Comparen el plan de la Unidad 6 con lo que efectivamente ocurrió. Para cada desvío: qué se planificó, qué pasó, por qué, y qué harían distinto.

**5. Guía rápida**

Redacten la guía rápida del usuario operativo, de una página, en formato de guía práctica.

**6. Verificación**

Verifiquen que toda la documentación esté en el repositorio, en texto, y que ningún documento describa algo que ya no es así.

**Formato de entrega:** informe final en el repositorio, más resumen ejecutivo y guía rápida como documentos separados.

---

# Preguntas de repaso

1. ¿Cuáles son las dos preguntas que hay que responder antes de escribir un documento?

2. ¿Por qué se documenta el por qué y no el qué?

3. Nombre los cuatro tipos de documento y a qué pregunta responde cada uno.

4. ¿Qué ocurre cuando se mezclan los cuatro tipos en un solo archivo?

5. ¿Por qué la conclusión de un informe técnico va al principio?

6. ¿Qué aportan las secciones de supuestos y limitaciones?

7. ¿Por qué un informe con un solo curso de acción no informa una decisión?

8. Reescriba de forma verificable: "el sistema podría presentar algunas dificultades de rendimiento".

9. ¿Por qué una decisión sin registro es una característica sin explicación?

10. ¿Por qué la documentación desactualizada es peor que la ausencia de documentación?

11. ¿Qué demuestra la sección de desvíos del informe final?

---

# Bibliografía

- [Diátaxis — Marco para estructurar documentación técnica](https://diataxis.fr/)
- [Write the Docs — Guía de documentación](https://www.writethedocs.org/guide/)
- [Markdown Guide](https://www.markdownguide.org/)
- [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/)
- Sommerville, I. *Ingeniería del Software.* Sección sobre documentación del software.
- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Secciones sobre documentación de requerimientos y de diseño.

---

**Fin de la Unidad 17**
