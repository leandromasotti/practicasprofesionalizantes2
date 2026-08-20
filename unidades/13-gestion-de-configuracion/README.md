# Unidad 13
# Gestión de la Configuración del Software

> "Están haciendo un trabajo en grupo. Uno borra algo importante, otro tiene otra versión. ¿Qué pasa?"

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Explicar qué problema resuelve la Gestión de la Configuración del Software.
- Identificar los elementos de configuración de un proyecto.
- Comprender qué es una línea base y cómo se establece.
- Aplicar el procedimiento de gestión del cambio.
- Utilizar Git y GitHub para el control de versiones y el trabajo colaborativo.
- Realizar una auditoría de configuración.

> Git es la herramienta. La Gestión de la Configuración es el marco. Esta unidad enseña el marco y usa la herramienta.

---

# El problema

Un equipo de cuatro personas trabaja sobre el mismo proyecto.

Al cabo de dos semanas:

- hay tres versiones del documento de alcance y nadie sabe cuál es la vigente;
- alguien sobrescribió el trabajo de otro;
- el archivo se llama `alcance_final_v3_corregido_ESTE_SI.docx`;
- una funcionalidad que andaba dejó de andar y nadie sabe qué cambió;
- el cliente aprobó una versión que ya no existe.

Ninguno de estos problemas es técnico. Todos son de **configuración**.

---

# Qué es la Gestión de la Configuración del Software

La **GCS** es el conjunto de actividades destinadas a **identificar, controlar y auditar** los productos de un proyecto a lo largo de su ciclo de vida.

Responde cuatro preguntas que un proyecto debe poder contestar en cualquier momento:

| Pregunta | Actividad de GCS |
|---|---|
| ¿Qué elementos componen el producto? | Identificación de la configuración |
| ¿Cuál es la versión vigente de cada uno? | Control de versiones |
| ¿Quién cambió qué, cuándo y por qué? | Control de cambios |
| ¿Lo entregado es lo aprobado? | Auditoría de la configuración |

Un proyecto que no puede responder estas cuatro preguntas no está bajo control, independientemente de cuán bien funcione el software.

---

# Elementos de configuración

Un **elemento de configuración** es cualquier producto del proyecto que debe estar bajo control.

No es solo código:

| Categoría | Ejemplos |
|---|---|
| **Documentos de análisis** | Informe de diagnóstico, documento de alcance, especificación de requerimientos |
| **Documentos de gestión** | Plan de proyecto, cronograma, matriz de riesgos, informe de viabilidad |
| **Modelos** | Diagrama de clases, modelo de datos, diagramas de proceso |
| **Código** | Fuentes, scripts de base de datos, configuración |
| **Pruebas** | Casos de prueba, datos de prueba, resultados |
| **Documentación de usuario** | Manuales, material de capacitación |

> En esta materia, la mayoría de los elementos de configuración **no son código**. Son documentos e informes técnicos. Y necesitan el mismo control.

---

# La línea base

Una **línea base** es una versión de un elemento —o de un conjunto de elementos— que ha sido **formalmente revisada y aprobada**, y que a partir de ese momento solo puede modificarse mediante el procedimiento de gestión del cambio.

## Para qué sirve

Establece un punto de referencia estable. Sin línea base:

- no se sabe respecto de qué se está cambiando;
- el cliente aprueba algo que sigue cambiando;
- no se puede volver a un estado conocido.

## Cómo se establece

| Paso | Qué se hace |
|---|---|
| 1 | El elemento se completa |
| 2 | Se revisa formalmente |
| 3 | Se aprueba, y queda registrado quién aprobó y cuándo |
| 4 | Se identifica con una versión |
| 5 | Queda congelado: cambia solo por gestión del cambio |

## Líneas base típicas de un proyecto

| Línea base | Contenido | Momento |
|---|---|---|
| **Funcional** | Documento de alcance aprobado | Después de la Unidad 5 |
| **De diseño** | Modelo de datos y diagrama de clases aprobados | Después de la Unidad 16 |
| **De producto** | Sistema y documentación entregados | En la entrega |

> El documento de alcance aprobado por la comisión directiva **es** una línea base. A partir de ahí, todo cambio pasa por el procedimiento.

---

# Gestión del cambio

Es el mecanismo que permite modificar una línea base sin perder el control.

## El procedimiento

| Paso | Qué se hace | Quién |
|---|---|---|
| 1. **Solicitud** | Se registra el pedido por escrito: qué, quién lo pide, por qué | Quien lo pide |
| 2. **Evaluación de impacto** | Qué elementos afecta, cuánto esfuerzo, qué efecto en plazo y costo | Equipo técnico |
| 3. **Informe** | Se comunica el impacto a quien pidió el cambio | Analista |
| 4. **Decisión** | Se aprueba o se rechaza, con el impacto sobre la mesa | La organización |
| 5. **Incorporación** | Se aplica el cambio a los elementos afectados | Equipo técnico |
| 6. **Nueva línea base** | Se aprueba la nueva versión y se registra | Analista y organización |

Este procedimiento es el mismo que vimos para cambios de alcance en la Unidad 5. La diferencia es que aquí se aplica a **todos** los elementos de configuración, no solo al alcance.

## El registro de cambios

| # | Fecha | Solicita | Cambio | Impacto | Decisión |
|---|---|---|---|---|---|
| C1 | 12/09 | Comisión | Agregar campo "grupo sanguíneo" al socio | 4 h | Aprobado |
| C2 | 20/09 | Comisión | Reporte de asistencia por profesor | 16 h, +2 días al plazo | Aprobado |
| C3 | 28/09 | Administrativa | Poder anular un pago registrado | 12 h, afecta modelo de datos | Aprobado |
| C4 | 05/10 | Comisión | Aplicación para celulares | 240 h, +6 semanas | **Rechazado** — pasa a segunda etapa |

Esta tabla es la que permite responder, al final del proyecto, por qué se entregó dos semanas más tarde de lo planificado.

Sin ella, el atraso parece incompetencia. Con ella, es la consecuencia documentada de tres cambios aprobados por el cliente.

---

# Control de versiones con Git

## Qué es Git

**Git** es un sistema de control de versiones distribuido. Guarda la historia completa de cambios de un conjunto de archivos, permite volver a cualquier estado anterior y permite que varias personas trabajen en paralelo sin sobrescribirse.

**GitHub** es una plataforma que aloja repositorios Git y agrega herramientas de colaboración: revisión de cambios, discusión y gestión de tareas.

| | |
|---|---|
| **Git** | El historial de cambios |
| **GitHub** | El lugar donde ese historial se comparte |

## Conceptos

| Concepto | Qué es |
|---|---|
| **Repositorio** | El proyecto con toda su historia |
| **Commit** | Un cambio confirmado, con autor, fecha y descripción |
| **Rama** (*branch*) | Una línea de trabajo paralela |
| **Fusión** (*merge*) | Incorporar una rama a otra |
| **Clonar** | Traer una copia completa del repositorio |
| **Push** | Subir los commits locales al repositorio remoto |
| **Pull** | Traer los cambios del remoto |
| **Pull request** | Pedido de revisión antes de fusionar |
| **Conflicto** | Dos cambios sobre la misma línea, que hay que resolver |

## Comandos básicos

```bash
# Traer el repositorio por primera vez
git clone <url-del-repositorio>

# Ver el estado del trabajo
git status

# Crear una rama y cambiarse a ella
git checkout -b nombre-de-la-rama

# Registrar cambios
git add .
git commit -m "Descripcion clara de lo que se hizo"

# Subir la rama al remoto
git push origin nombre-de-la-rama

# Traer los cambios de los demás
git pull

# Ver la historia
git log --oneline
```

## Cómo se corresponde con la GCS

| Concepto de GCS | Cómo se realiza en Git |
|---|---|
| Elemento de configuración | Archivo del repositorio |
| Versión | Commit |
| Historia de cambios | `git log` |
| Línea base | Etiqueta (*tag*) sobre un commit |
| Solicitud de cambio | Issue |
| Evaluación y aprobación | Pull request con revisión |
| Trazabilidad | Autor, fecha y mensaje de cada commit |

Git no reemplaza el procedimiento de gestión del cambio: lo **soporta**. Un equipo puede usar Git y no tener gestión de configuración, si nadie revisa, nadie aprueba y nadie establece líneas base.

---

# Trabajo colaborativo

## Flujo con ramas por funcionalidad

| Paso | Acción |
|---|---|
| 1 | Cada integrante crea su rama: `feature/modulo-socios` |
| 2 | Trabaja en su rama, con commits frecuentes y chicos |
| 3 | Sube la rama al remoto |
| 4 | Abre un pull request |
| 5 | Otro integrante revisa |
| 6 | Se fusiona a la rama principal |

## Las reglas

| Regla | Por qué |
|---|---|
| ❌ **No trabajar directamente en la rama principal** | La principal debe estar siempre en estado utilizable |
| ❌ **No sobrescribir el trabajo de otro** | Se resuelve con ramas y revisión, no avisando por mensaje |
| ✅ **Commits chicos y frecuentes** | Un commit gigante es imposible de revisar y de revertir |
| ✅ **Mensajes descriptivos** | "Correcciones" no dice nada en seis meses |
| ✅ **Revisar antes de fusionar** | Es la instancia de control de calidad más barata que existe |
| ✅ **Avisar al equipo qué se está haciendo** | Evita que dos personas toquen lo mismo |

## Mensajes de commit

| ❌ | ✅ |
|---|---|
| `cambios` | `Agrega validacion de documento duplicado en alta de socio` |
| `arreglos` | `Corrige el calculo de deuda cuando el socio tiene pagos parciales` |
| `subo lo de hoy` | `Documenta el circuito de cobranza relevado el 12/09` |
| `final` | `Aprueba la linea base del documento de alcance v2` |

Un mensaje de commit describe **qué cambió y por qué**, no cuándo se hizo.

## Resolución de conflictos

Un conflicto aparece cuando dos personas modificaron la misma línea del mismo archivo.

| Paso | Qué hacer |
|---|---|
| 1 | Leer el mensaje: Git indica el archivo y las líneas |
| 2 | Abrir el archivo y ver ambas versiones marcadas |
| 3 | Decidir qué queda: una, la otra, o una combinación |
| 4 | Borrar las marcas del conflicto |
| 5 | Confirmar la resolución con un commit |

Un conflicto no es un error: es Git avisando que hay una decisión que una persona tiene que tomar.

---

# Auditoría de la configuración

La auditoría verifica que **lo que se entrega es lo que se aprobó**.

## Auditoría de configuración funcional

Verifica que el producto cumple lo especificado en la línea base funcional.

> ¿Cada requerimiento del documento de alcance aprobado está implementado y probado?

## Auditoría de configuración física

Verifica que todos los elementos que deben entregarse están presentes, completos y en la versión correcta.

> ¿Están el código, los scripts, los manuales, los modelos y los informes? ¿Son las versiones aprobadas?

## Lista de verificación

| Verificación |
|---|
| ¿El cambio se realizó según el procedimiento? |
| ¿Está aprobado y registrado quién lo aprobó? |
| ¿Se actualizaron todos los elementos afectados, incluida la documentación? |
| ¿Se estableció la nueva línea base? |
| ¿Los elementos entregados coinciden con las versiones aprobadas? |
| ¿Cada requerimiento del alcance tiene su implementación y su prueba? |

> El punto que más falla es el tercero: se cambia el código y no se actualiza la documentación. Al mes, la documentación describe un sistema que no existe.

---

# El repositorio como documentación viva

Un repositorio bien mantenido responde por sí solo preguntas que de otro modo requieren preguntarle a alguien:

| Pregunta | Dónde está la respuesta |
|---|---|
| ¿Cuál es la versión vigente? | La rama principal |
| ¿Qué se cambió la semana pasada? | El historial |
| ¿Por qué se tomó esta decisión? | El mensaje del commit y el pull request |
| ¿Quién trabajó en qué? | El historial por autor |
| ¿Qué está aprobado? | Las etiquetas de línea base |
| ¿Qué está pendiente? | Los issues abiertos |

## El README

Es la puerta de entrada. Un repositorio sin README obliga a cada persona nueva a preguntar de qué se trata.

Debe contener, como mínimo: qué es el proyecto, cómo está organizado, cómo se trabaja en él y a quién preguntarle.

> Este repositorio de la cátedra es un ejemplo aplicado de lo que la unidad enseña: los elementos de configuración son documentos, cada cambio queda en el historial con su fundamento, y el README es el punto de entrada.

---

# Errores frecuentes

- **Creer que GCS es control de versiones de código.** Los documentos son elementos de configuración.
- **No establecer líneas base**, con lo que no se sabe respecto de qué se cambia.
- **Aceptar cambios sin registrarlos.**
- **Trabajar directamente en la rama principal.**
- **Commits gigantes** que mezclan cinco cambios distintos.
- **Mensajes de commit sin información.**
- **Fusionar sin revisión.**
- **Cambiar el código y no actualizar la documentación.**
- **No auditar antes de entregar**, y entregar una versión que no es la aprobada.
- **Versionar archivos con nombres como `_final_v3`** en lugar de usar el control de versiones.

---

# Buenas prácticas

✔ Poner bajo control todos los elementos, no solo el código.

✔ Establecer líneas base con aprobación registrada.

✔ Registrar cada solicitud de cambio, aunque sea chica.

✔ Informar el impacto antes de aceptar un cambio.

✔ Una rama por funcionalidad, nunca trabajar en la principal.

✔ Commits chicos con mensajes que expliquen el por qué.

✔ Revisión entre pares antes de fusionar.

✔ Actualizar la documentación en el mismo cambio que el código.

✔ Auditar la configuración antes de entregar.

---

# Caso de estudio

## El proyecto sin línea base

Un equipo entregó un sistema de gestión. En la reunión de aceptación, la organización rechazó la entrega.

Los hechos:

- El documento de alcance se había enviado por correo en marzo y el cliente respondió "está bien".
- En abril se agregaron dos funcionalidades pedidas verbalmente en una reunión.
- En mayo se quitó una funcionalidad porque "el cliente dijo que no la usaba".
- El manual de usuario describe tres pantallas que ya no existen.
- Nadie sabe si el reporte de morosos se pidió o el equipo lo agregó por su cuenta.
- El cliente afirma que el sistema debía emitir carnets. El equipo afirma que nunca se pidió.
- El repositorio tiene 12 commits, todos con el mensaje "avances".

### Para analizar

1. ¿Qué línea base faltó establecer, y en qué momento?
2. ¿Cómo se habría resuelto la discusión sobre los carnets con GCS aplicada?
3. ¿Qué paso del procedimiento de gestión del cambio se omitió en abril y en mayo?
4. ¿Qué revela el manual que describe pantallas inexistentes?
5. ¿Qué auditoría habría detectado el problema antes de la reunión de aceptación?
6. ¿Qué información se perdió por los 12 commits con mensaje "avances"?
7. Escriba los mensajes de commit que ese equipo debería haber usado, si el trabajo hubiera sido el que describe el caso.

---

# Aplicación profesional

Cada grupo mantiene su proyecto en un **repositorio bajo gestión de configuración**, y entrega:

- el repositorio con todos los elementos de configuración, no solo código;
- un README que explique el proyecto y cómo está organizado;
- las líneas base establecidas, identificadas con etiquetas;
- el registro de cambios, con impacto y decisión de cada uno;
- evidencia de trabajo con ramas y revisión entre pares;
- una auditoría de configuración antes de la entrega final, con su lista de verificación completada.

Se evalúa la trazabilidad: que a partir del repositorio se pueda reconstruir qué se hizo, cuándo, quién y por qué.

---

# Resumen

En esta unidad aprendimos que:

- La GCS permite responder qué compone el producto, cuál es la versión vigente, quién cambió qué y si lo entregado es lo aprobado.
- Los elementos de configuración incluyen documentos, modelos, pruebas y manuales, no solo código.
- Una línea base es una versión revisada y aprobada, que solo cambia por procedimiento.
- El documento de alcance aprobado es una línea base.
- La gestión del cambio tiene seis pasos, y el que se saltea es informar el impacto antes de decidir.
- El registro de cambios es lo que permite explicar un atraso con fundamento.
- Git soporta la GCS pero no la reemplaza: sin revisión ni líneas base, no hay gestión de configuración.
- Los commits deben ser chicos y sus mensajes explicar el por qué.
- Un conflicto es Git avisando que hay una decisión humana pendiente.
- La auditoría verifica que lo entregado sea lo aprobado, y el punto que más falla es la documentación desactualizada.

---

# Actividad práctica

## Puesta bajo configuración

**1. Inventario**

Listen todos los elementos de configuración de su proyecto, clasificados por categoría. Deben ser al menos diez, y la mayoría no deben ser código.

**2. Repositorio**

Pongan el proyecto en un repositorio con README. El README debe permitir que alguien externo entienda de qué se trata sin preguntar.

**3. Línea base**

Establezcan la línea base funcional: el documento de alcance aprobado, identificado con etiqueta y con registro de quién lo aprobó y cuándo.

**4. Trabajo con ramas**

Cada integrante trabaja en su propia rama y abre al menos un pull request, revisado por otro integrante. Debe quedar evidencia de la revisión.

**5. Registro de cambios**

Armen la tabla de registro de cambios con los pedidos recibidos hasta ahora, su impacto y su decisión.

**6. Mensajes**

Revisen sus commits. Reescriban tres mensajes que no cumplan la regla de explicar qué cambió y por qué.

**7. Auditoría**

Completen la lista de verificación de auditoría sobre el estado actual del proyecto. Indiquen qué encontraron mal.

**Formato de entrega:** enlace al repositorio más un informe técnico de una página con el resultado de la auditoría.

---

# Preguntas de repaso

1. ¿Cuáles son las cuatro preguntas que la GCS permite responder?

2. ¿Por qué un documento de alcance es un elemento de configuración?

3. ¿Qué es una línea base y qué la distingue de una versión cualquiera?

4. Enuncie los seis pasos de la gestión del cambio.

5. ¿Cuál es el paso que se omite con más frecuencia, y qué consecuencia tiene?

6. ¿Para qué sirve el registro de cambios al final de un proyecto?

7. ¿Cuál es la diferencia entre Git y GitHub?

8. ¿Por qué un equipo puede usar Git y no tener gestión de configuración?

9. ¿Por qué no se debe trabajar directamente en la rama principal?

10. ¿Qué verifica una auditoría de configuración funcional y qué verifica una física?

---

# Bibliografía

- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Capítulo sobre gestión de la configuración del software.
- Sommerville, I. *Ingeniería del Software.* Capítulo sobre gestión de configuraciones.
- [Pro Git — Chacon & Straub](https://git-scm.com/book/es/v2) — libro completo y gratuito en español
- [Documentación oficial de GitHub en español](https://docs.github.com/es) · [Primeros pasos](https://docs.github.com/es/get-started/start-your-journey) · [Pull requests](https://docs.github.com/es/pull-requests)
- [Atlassian — Glosario de Git](https://www.atlassian.com/es/git/glossary)
- [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/)

---

**Fin de la Unidad 13**
