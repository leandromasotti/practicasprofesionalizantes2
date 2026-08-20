# Unidad 2
# Comunicación y ética profesional

> "Un analista pasa gran parte de su tiempo explicando cuestiones técnicas a personas que no son técnicas. Es exactamente la misma habilidad que se necesita para explicar qué es una computadora a un chico de seis años."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Reconocer la comunicación como competencia profesional central del analista.
- Analizar al destinatario antes de comunicar.
- Adaptar lenguaje y nivel de detalle según a quién se dirige.
- Traducir entre el lenguaje del dominio y el lenguaje técnico.
- Comunicar atrasos, desvíos y malas noticias de forma profesional.
- Identificar los dilemas éticos habituales del rol y fundamentar una decisión frente a ellos.

> **Ejes transversales.** Esta unidad desarrolla de forma explícita dos de los tres ejes que la resolución exige integrar de manera continua en toda la carrera: **comunicación** y **ética profesional**. Ambos se retoman en el resto de las unidades y se evalúan en cada entrega.

---

# Por qué la comunicación es contenido de esta materia

Podría parecer que la comunicación es una habilidad personal, no un contenido técnico.

Pero la resolución la define como eje transversal de la carrera, con una precisión que conviene leer completa:

> "Resulta necesario que los profesionales del nivel superior puedan desarrollar estrategias comunicativas en distintos soportes y medios de comunicación a lo largo de toda la formación, con el fin de interpretar necesidades, gestionar proyectos adecuadamente, comunicar conclusiones y resultados […] atendiendo a los objetivos, a los destinatarios, al contenido, al soporte y a la finalidad comunicacional prevista en cada caso."

Hay una razón práctica detrás. El trabajo del analista consiste en producir y transmitir información:

- releva necesidades **escuchando**;
- documenta requerimientos **escribiendo**;
- explica soluciones **presentando**;
- capacita usuarios **enseñando**;
- defiende propuestas **argumentando**;
- informa desvíos **comunicando malas noticias**.

Un analista que comprende perfectamente un problema pero no logra explicarlo produce el mismo resultado que uno que no lo comprendió.

---

# Análisis del destinatario

Antes de comunicar hay que responder tres preguntas:

1. **¿Quién va a recibir esto?**
2. **¿Qué necesita hacer con la información?**
3. **¿Qué sabe y qué no sabe?**

No es lo mismo hablar con:

| Destinatario | Le interesa | Le sobra |
|---|---|---|
| Un programador | Cómo se implementa, qué restricciones hay | La justificación de negocio |
| Un gerente | Costo, plazo, riesgo, beneficio | El detalle técnico |
| Un usuario final | Cómo cambia su trabajo cotidiano | La arquitectura |
| Un auditor | Trazabilidad, cumplimiento, evidencia | Las decisiones de diseño |
| Un docente de nivel inicial | Qué van a hacer los chicos y en cuánto tiempo | Los conceptos de informática |

El error típico no es usar palabras difíciles: es **dar información que al destinatario no le sirve para nada**, y omitir la que necesita para decidir.

## El mismo hecho, tres versiones

Situación: el proyecto se va a atrasar tres semanas porque la base de datos heredada tiene datos inconsistentes.

**Al equipo técnico**

> "Los datos de la tabla de socios tienen documentos duplicados y fechas en tres formatos distintos. Antes de migrar hay que escribir un script de normalización y validar caso por caso los registros que no se resuelvan automáticamente."

**A la dirección**

> "Encontramos que los datos actuales de socios tienen inconsistencias que hay que corregir antes de cargarlos al sistema nuevo. Si los migramos como están, el sistema va a arrastrar errores de cobro. Corregirlos suma tres semanas al plazo. La alternativa es migrar solo los socios activos y dejar el histórico para una segunda etapa."

**Al usuario administrativo**

> "Vamos a necesitar tu ayuda para revisar unos 200 registros de socios donde los datos no están claros. Serían unas dos horas por día durante una semana. Sin eso, el sistema nuevo podría cobrarle mal a esos socios."

Los tres mensajes describen el mismo hecho. Ninguno miente. Cada uno le da a su destinatario **lo que necesita para actuar**.

---

# Traducción entre lenguajes

El cliente habla el lenguaje de su actividad. El equipo técnico necesita precisión.

| El cliente dice | El analista debe averiguar |
|---|---|
| "Necesito saber qué socios están al día" | ¿Al día significa sin deuda alguna, o con la última cuota paga? ¿Cuenta el mes en curso? |
| "Quiero que me avise cuando venza una vacuna" | ¿Avisar a quién, por qué medio, cuántos días antes? |
| "El sistema tiene que ser rápido" | ¿Rápido en qué operación? ¿Comparado con qué? ¿Cuántos usuarios simultáneos? |
| "Que sea fácil de usar" | ¿Fácil para quién? ¿Qué tarea tiene que poder hacer sin ayuda? |

La traducción tiene dos direcciones. También hay que devolver al cliente, en su lenguaje, lo que el equipo técnico plantea.

## Confirmar lo comprendido

Una práctica que evita la mayoría de los malentendidos: **devolver lo entendido con las propias palabras y pedir confirmación**.

> "Déjame ver si entendí: querés que el sistema le envíe un correo al dueño de la mascota siete días antes de que se venza la vacuna, y que si no responde, le vuelva a avisar el día del vencimiento. ¿Es así?"

Es una sola frase y elimina semanas de trabajo mal orientado.

---

# Comunicar malas noticias

Todo proyecto produce malas noticias: atrasos, sobrecostos, funcionalidades que no se pueden hacer como se prometió.

La forma de comunicarlas distingue a un profesional.

## Cuatro reglas

**1. Temprano.** Una mala noticia comunicada a tiempo es un problema a resolver. La misma noticia comunicada tarde es un engaño descubierto.

**2. Con la causa.** No alcanza con decir que hay atraso: hay que explicar por qué.

**3. Con alternativas.** Nunca llevar solo el problema. Llevar dos o tres cursos de acción con sus consecuencias.

**4. Sin adornos.** Los eufemismos no reducen la mala noticia, solo hacen que el destinatario tarde más en entenderla.

## Comparación

| ❌ Mal | ✅ Bien |
|---|---|
| "Estamos teniendo algunas complicaciones menores" | "Vamos tres semanas atrasados" |
| "Se está avanzando" | "Completamos 12 de 20 tareas; el 60 % del trabajo con el 70 % del tiempo consumido" |
| "Se va a poder hacer" | "Se puede hacer si extendemos el plazo dos semanas, o si sacamos el módulo de reportes del alcance" |
| Callar hasta la entrega | Informar en la reunión siguiente a la detección |

---

# Ética profesional

La resolución establece que la formación ética debe desplazar el énfasis *"depositado en lo normativo, instrumental y técnico hacia la creatividad y el compromiso en la toma de decisiones"*.

Es decir: no se trata de memorizar un código de conducta, sino de poder decidir bien cuando la decisión correcta tiene costo.

## Los dilemas habituales del rol

### Estimar por debajo para ganar el proyecto

La organización tiene un presupuesto y el analista sabe que el trabajo cuesta más.

Ajustar la estimación a lo que el cliente quiere escuchar consigue el contrato y garantiza el conflicto.

*La decisión profesional:* informar la estimación real y, si el presupuesto no alcanza, proponer un alcance menor que sí sea viable.

### Ocultar un atraso esperando recuperarlo

Es el dilema más frecuente y el más costoso. Casi nunca se recupera, y el atraso se descubre cuando ya no hay margen.

*La decisión profesional:* informar el desvío en cuanto se detecta.

### Comprometer un plazo que se sabe inviable

Aceptar una fecha imposible para evitar una conversación incómoda traslada el problema a todo el equipo y termina en un incumplimiento.

*La decisión profesional:* dejar constancia por escrito de la inviabilidad, con el fundamento, y proponer la fecha que sí se puede sostener.

### Usar información de la organización

Durante el relevamiento el analista accede a información sensible: datos de personas, información contable, prácticas internas.

*La decisión profesional:* usarla solo para el proyecto, no divulgarla, no llevarla a otro cliente, y no conservarla al terminar.

### Recomendar lo que conviene al proveedor

Si la solución más rentable para quien la vende no es la mejor para la organización, hay un conflicto de interés.

*La decisión profesional:* explicitar el conflicto y fundamentar la recomendación en el interés de la organización.

---

## Responsabilidad sobre lo que se documenta

Un documento técnico firmado por un analista es una afirmación profesional.

Quien lo firma responde por:

- que lo que dice sea verificable;
- que las estimaciones estén fundamentadas y no ajustadas a conveniencia;
- que los riesgos conocidos estén declarados;
- que lo que no se sabe figure como incertidumbre y no se presente como certeza.

> Un informe que omite un riesgo conocido no es un informe incompleto: es un informe que induce a error a quien decide.

---

# Errores frecuentes

- **Usar el mismo lenguaje con todos los destinatarios.**
- **Confundir hablar simple con hablar impreciso.** Simplificar es elegir qué decir, no decir cosas vagas.
- **Suponer que el cliente entendió** porque no preguntó nada.
- **Documentar para cubrirse** en lugar de para que alguien lo lea.
- **Guardar la mala noticia** para el próximo informe.
- **Llevar el problema sin alternativas.**
- **Aceptar un compromiso inviable** para no tener una conversación difícil.

---

# Buenas prácticas

✔ Analizar al destinatario antes de escribir o hablar.

✔ Devolver lo comprendido y pedir confirmación.

✔ Comunicar los desvíos apenas se detectan.

✔ Llevar siempre alternativas con sus consecuencias.

✔ Dejar por escrito las decisiones y su fundamento.

✔ Declarar la incertidumbre como incertidumbre.

✔ Tratar la información de la organización como confidencial por defecto.

---

# Caso de estudio

## El taller para nivel inicial

Una institución educativa encarga a la consultora el diseño de un taller tecnológico para chicos de nivel inicial y primario.

El encargo pone la competencia comunicativa en su caso extremo: hay que explicar algoritmos, condicionales y redes a un destinatario de cinco años, sin perder la precisión del concepto.

Además exige comunicación en tres direcciones distintas:

| Destinatario | Qué hay que comunicarle |
|---|---|
| La dirección de la institución | Qué se va a hacer, en cuánto tiempo, con qué materiales y qué se espera que los chicos aprendan |
| Las docentes de sala | Cómo se organiza la actividad, qué rol cumplen ellas, cómo se maneja el grupo |
| Los chicos | La consigna del juego, en su lenguaje |

### Para analizar

1. ¿Qué cambia entre el documento para la dirección y la consigna para los chicos, además del vocabulario?
2. ¿Cómo explicaría "algoritmo" a un chico de cinco años sin usar la palabra?
3. Si el taller requiere más materiales de los previstos, ¿cómo lo comunicaría a la dirección?
4. ¿Qué información de la institución consideraría confidencial?
5. Si al ensayar descubren que la actividad no funciona como esperaban, ¿lo informan o lo ajustan en silencio?

> La entrega [El Gran Circuito Tecnológico Desconectado](../../proyecto-integrador/ejemplos/2026-gran-circuito-tecnologico-desconectado.md) resuelve este encargo. Sirve como referencia de cómo se documenta una propuesta para tres audiencias a la vez.

---

# Aplicación profesional

La comunicación y la ética se evalúan en **todas** las entregas del proyecto integrador, no en una en particular.

En cada entrega se observa:

- si el documento está dirigido a un destinatario identificable;
- si el nivel de detalle es el adecuado para ese destinatario;
- si las estimaciones y los riesgos están declarados con honestidad;
- si los desvíos figuran en lugar de estar disimulados.

En la defensa final se evalúa además la capacidad de explicar las decisiones a un interlocutor no técnico y de sostenerlas cuando se las cuestiona.

---

# Resumen

En esta unidad aprendimos que:

- La comunicación es un eje transversal de la carrera y una competencia técnica del rol, no un rasgo de personalidad.
- Antes de comunicar hay que analizar al destinatario: qué necesita hacer con la información y qué sabe.
- Simplificar es elegir qué decir, no decir cosas imprecisas.
- La traducción entre el lenguaje del dominio y el técnico va en las dos direcciones.
- Confirmar lo comprendido evita la mayoría de los malentendidos.
- Las malas noticias se comunican temprano, con su causa y con alternativas.
- Los dilemas éticos del rol aparecen en la estimación, en el reporte de avance, en el compromiso de plazos y en el manejo de información.
- Quien firma un documento técnico responde por lo que afirma y por lo que omite.

---

# Actividad práctica

## Tres audiencias, un mismo hecho

**1. Análisis de destinatarios**

Elijan una decisión técnica de su proyecto. Identifiquen tres destinatarios distintos y, para cada uno, qué necesita hacer con la información.

**2. Tres versiones**

Redacten el mismo contenido tres veces, una por destinatario. Máximo un párrafo cada una.

**3. Mala noticia**

Redacten la comunicación de un atraso de dos semanas en su proyecto, dirigida a la dirección de la organización. Debe incluir causa, impacto y al menos dos alternativas con sus consecuencias.

**4. Dilema ético**

Elijan uno de los cinco dilemas de la unidad. Describan cómo podría aparecer concretamente en su proyecto, qué haría la salida cómoda y qué haría la decisión profesional. Fundamenten.

**Formato de entrega:** documento de una a dos páginas.

---

# Preguntas de repaso

1. ¿Por qué la comunicación se considera contenido de esta materia y no una habilidad personal?

2. ¿Qué tres preguntas hay que responder antes de comunicar algo?

3. ¿Cuál es la diferencia entre simplificar y ser impreciso?

4. Enuncie las cuatro reglas para comunicar una mala noticia.

5. ¿Por qué ocultar un atraso esperando recuperarlo es una mala decisión, además de una falta ética?

6. ¿De qué responde un analista que firma un informe técnico?

7. ¿Por qué un informe que omite un riesgo conocido induce a error?

---

# Bibliografía

- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Capítulo sobre comunicación con el cliente.
- [Write the Docs — Guía de documentación y comunicación técnica](https://www.writethedocs.org/guide/)
- [ACM Code of Ethics and Professional Conduct](https://www.acm.org/code-of-ethics)
- Resolución TSAS 6790/19 — Eje transversal de Comunicación y Eje transversal de Ética Profesional.

---

**Fin de la Unidad 2**
