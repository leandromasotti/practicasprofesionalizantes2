# Unidad 9
# Viabilidad y costos del proyecto

> "El trabajo más valioso de un analista es, algunas veces, explicarle a una organización por qué no conviene hacer el proyecto que le pidió."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Explicar qué significa que un proyecto sea viable.
- Analizar las cinco dimensiones de la viabilidad.
- Elaborar un estudio de viabilidad como entregable previo a la decisión.
- Construir la estructura de costos de un proyecto de software.
- Distinguir costo directo, indirecto y costo de oportunidad.
- Calcular relación costo-beneficio y retorno de la inversión.
- Presentar la evaluación a quien decide.

> Esta unidad desarrolla la capacidad profesional **C3** que fija la resolución: *"analizar la viabilidad y costos del proyecto"*.

---

# El problema inicial

Una organización quiere hacer un proyecto. El equipo lo estimó: 32 persona-mes, 9 meses.

Falta la pregunta más importante:

**¿Conviene hacerlo?**

Un proyecto puede ser técnicamente posible y a la vez inconveniente: porque cuesta más que el problema que resuelve, porque la organización no puede sostenerlo, porque para cuando esté listo el problema habrá cambiado, o porque no está permitido.

Determinar eso es el objeto de esta unidad.

---

# Qué significa que un proyecto sea viable

Viable no es lo mismo que posible.

**Posible** es que se pueda construir. **Viable** es que se pueda construir *y* que tenga sentido hacerlo en esta organización, con estos recursos y en este momento.

Un proyecto es viable cuando las cinco dimensiones dan resultado favorable. Basta que una falle para que el proyecto no deba avanzar como está planteado.

---

# Las cinco dimensiones de la viabilidad

## Viabilidad técnica

> ¿Se puede construir con la tecnología y el conocimiento disponibles?

Qué se analiza:

- ¿El equipo tiene las habilidades necesarias, o hay que adquirirlas?
- ¿La tecnología requerida existe, está madura y es accesible?
- ¿La infraestructura de la organización lo soporta?
- ¿Hay que integrarse con sistemas existentes? ¿Es posible?
- ¿Hay algún requerimiento que no se sabe cómo resolver?

*Señal de alerta:* que la respuesta a "cómo haríamos esto" sea "ya lo vamos a ver".

## Viabilidad operativa

> ¿La organización va a poder usarlo?

Es la dimensión que más proyectos técnicamente correctos hace fracasar.

Qué se analiza:

- ¿Los usuarios tienen la capacidad de operar el sistema?
- ¿El sistema se adapta a cómo trabaja la organización, o exige que cambie?
- ¿Hay resistencia al cambio? ¿De quién y por qué?
- ¿Quién va a mantener el sistema cuando el proyecto termine?
- ¿La organización puede sostener la carga de datos que el sistema requiere?

*Señal de alerta:* que el sistema resuelva un problema de la dirección creando trabajo nuevo para quien opera.

## Viabilidad económica

> ¿El beneficio justifica el costo?

Qué se analiza:

- ¿Cuánto cuesta el proyecto, completo?
- ¿Cuánto cuesta mantenerlo después?
- ¿Qué beneficio produce, medido en dinero o en tiempo ahorrado?
- ¿En cuánto tiempo se recupera la inversión?
- ¿La organización tiene el dinero disponible cuando hay que gastarlo?

## Viabilidad temporal

> ¿Se puede tener a tiempo?

Qué se analiza:

- ¿Existe una fecha límite real? ¿De dónde viene?
- ¿La duración estimada entra en ese plazo?
- ¿Qué pasa si se entrega después? ¿El valor se pierde o solo se demora?
- ¿Se puede entregar por etapas para que lo importante llegue a tiempo?

*Distinción útil:* una fecha impuesta por una temporada deportiva o un cierre contable es real. Una fecha impuesta porque "quedaría bien tenerlo para fin de año" es negociable.

## Viabilidad legal

> ¿Está permitido?

Qué se analiza:

- ¿Hay normativa aplicable al tratamiento de los datos involucrados?
- ¿Se manejan datos personales o sensibles?
- ¿Hay obligaciones de conservación o de auditoría?
- ¿Las licencias del software a utilizar permiten este uso?
- ¿La propiedad de lo que se construye está definida por escrito?

*Señal de alerta:* un sistema que registra datos de salud, datos de menores o datos financieros y nadie preguntó qué normativa aplica.

---

# El estudio de viabilidad

El estudio de viabilidad es un **entregable previo a la decisión de avanzar**.

Su función no es aprobar el proyecto: es darle a quien decide la información para decidir.

## Estructura

| Sección | Contenido |
|---|---|
| **Situación actual** | El diagnóstico, resumido |
| **Proyecto propuesto** | Qué se haría, en dos párrafos |
| **Viabilidad técnica** | Análisis y conclusión |
| **Viabilidad operativa** | Análisis y conclusión |
| **Viabilidad económica** | Costos, beneficios y retorno |
| **Viabilidad temporal** | Plazo y consecuencia de no cumplirlo |
| **Viabilidad legal** | Normativa aplicable y cumplimiento |
| **Riesgos principales** | Los tres o cuatro que más pesan |
| **Alternativas** | Al menos dos, incluyendo no hacer nada |
| **Recomendación** | Qué conviene hacer y por qué |

## La alternativa de no hacer nada

Todo estudio de viabilidad debe incluir esta alternativa, con su costo.

No hacer nada **también tiene costo**: el problema sigue produciendo pérdidas. Cuantificarlo es lo que le da sentido a comparar.

> Si el costo de no hacer nada es menor que el del proyecto, la recomendación profesional es no hacer el proyecto.

---

# Estructura de costos

Los costos de un proyecto de software se agrupan en cinco categorías. Las tres últimas son las que se olvidan.

## Recursos humanos

Es habitualmente el componente mayor, entre el 60 % y el 80 % del total.

Se calcula a partir de la estimación de esfuerzo:

```
Costo de RRHH = esfuerzo (persona-mes) × costo del persona-mes
```

El costo del persona-mes incluye el salario más las cargas sociales, no solo el salario.

## Infraestructura

- Servidores o servicio de alojamiento.
- Equipamiento nuevo si hace falta.
- Conectividad.
- Respaldos.

Conviene distinguir el costo **de una vez** del costo **mensual**, porque el segundo continúa después del proyecto.

## Licencias

- Sistemas operativos y bases de datos.
- Herramientas de desarrollo.
- Servicios de terceros con costo por uso.

## Capacitación

- Del equipo, si necesita adquirir conocimiento.
- **De los usuarios de la organización**, que es la que siempre se omite.

Un sistema entregado sin capacitación produce un sistema que no se usa.

## Mantenimiento

El costo que continúa cuando el proyecto termina.

Sobre el ciclo de vida completo de un sistema, el mantenimiento suele **superar** el costo de la construcción inicial.

> Presentar un costo de proyecto sin el costo de mantenimiento es informar la mitad del número.

---

# Tipos de costo

## Costo directo

Atribuible al proyecto de manera inequívoca: las horas del equipo, el servidor comprado para este sistema, la licencia adquirida.

## Costo indirecto

Recursos que el proyecto consume pero comparte con el resto de la organización: espacio, electricidad, administración, la porción de tiempo de quien supervisa varios proyectos.

Se imputan por algún criterio de reparto, que hay que explicitar.

## Costo de oportunidad

Es el concepto que más se ignora y el que más pesa en una decisión.

> El costo de oportunidad es **el valor de lo que se deja de hacer** por hacer esto.

Si el equipo dedica nueve meses a este proyecto, no hace los otros dos que estaban en la lista. Ese es un costo real, aunque no aparezca en ninguna factura.

Ejemplo concreto: la administrativa del club dedicará 4 horas semanales durante 9 meses a acompañar el proyecto. Son 144 horas que no dedica a su trabajo habitual. Eso es costo del proyecto.

---

# Análisis costo-beneficio

## Cuantificar el beneficio

El beneficio de un sistema administrativo casi nunca es un ingreso nuevo. Suele ser una de estas tres cosas:

| Tipo de beneficio | Cómo se cuantifica |
|---|---|
| **Tiempo ahorrado** | Horas de trabajo liberadas × costo de la hora |
| **Pérdida evitada** | Monto que hoy se pierde por errores, olvidos o morosidad |
| **Ingreso posibilitado** | Capacidad de atender más operaciones con la misma estructura |

Los beneficios intangibles —mejor imagen, mayor satisfacción, menos estrés— existen y deben mencionarse, pero **no se suman al cálculo**. Se informan aparte, para que quien decide los pondere.

## Ejemplo: Club Deportivo San Martín

### Costos

| Concepto | Tipo | Monto |
|---|---|---|
| Desarrollo: 32,6 persona-mes × $200.000 | Directo, una vez | $6.520.000 |
| Servidor y alojamiento, año 1 | Directo, mensual | $360.000 |
| Capacitación de usuarios: 8 horas | Directo, una vez | $120.000 |
| Tiempo de la administrativa: 144 h | Oportunidad | $720.000 |
| **Total primer año** | | **$7.720.000** |
| Mantenimiento anual estimado (18 % del desarrollo) | Recurrente | $1.173.600 |

### Beneficios anuales

| Concepto | Cálculo | Monto |
|---|---|---|
| Tiempo administrativo liberado | 10 h/semana × 48 semanas × $5.000 | $2.400.000 |
| Morosidad recuperada por control de cuotas | 3 % de $40.000.000 de cuotas anuales | $1.200.000 |
| Pérdidas por errores de cobro evitadas | Estimado sobre reclamos del último año | $400.000 |
| **Total anual** | | **$4.000.000** |

### Retorno de la inversión

```
Beneficio neto anual = 4.000.000 − 1.173.600 = $2.826.400

Período de recupero = 7.720.000 / 2.826.400 = 2,73 años
```

### Interpretación

El proyecto se recupera en aproximadamente **2 años y 9 meses** y a partir de allí produce un beneficio neto de unos 2,8 millones anuales.

¿Es aceptable? Depende de la organización. Para un club con vida institucional larga, un recupero a tres años es razonable. Para un emprendimiento que no sabe si va a existir en dos años, no lo es.

> Un número de recupero no se interpreta solo: se interpreta contra el horizonte de la organización.

---

# Presentar la evaluación a quien decide

Un estudio de viabilidad se escribe para alguien que **no es técnico** y que tiene que decidir.

## Reglas

**1. La recomendación va primero.** Quien decide lee la conclusión y después, si le interesa, el fundamento. Un informe que hace esperar la conclusión hasta la página seis no se lee.

**2. Los números con su supuesto al lado.** "Ahorro de $2.400.000 anuales, suponiendo que se liberan 10 horas semanales de trabajo administrativo" es verificable. El número solo, no.

**3. Alternativas, no un solo camino.** Como mínimo: el proyecto completo, una versión reducida, y no hacer nada.

**4. La incertidumbre declarada.** Si el beneficio depende de un supuesto frágil, hay que decirlo.

## Estructura de una página

> **Recomendación:** avanzar con el proyecto en dos etapas.
>
> **Por qué:** el control de cuotas resuelve el 70 % de la pérdida actual y se recupera en 14 meses. La gestión de actividades puede esperar.
>
> **Costo etapa 1:** $4.100.000. **Recupero:** 14 meses.
>
> **Alternativas:** proyecto completo ($7.720.000, recupero 2,7 años) · no hacer nada (pérdida anual estimada de $4.000.000).
>
> **Riesgo principal:** si la organización no asigna las 4 horas semanales de referente, el plazo se extiende un 30 %.
>
> **Supuesto crítico:** que la morosidad recuperable sea del 3 %. Si fuera del 1 %, el recupero pasa a 20 meses.

---

# La dimensión ética

## Informar que un proyecto no es viable

Es la situación más incómoda del rol: la organización quiere el proyecto, ya lo anunció internamente, y el análisis dice que no conviene.

Callar es más fácil. El proyecto avanza, se factura, y el problema aparece dos años después.

**La decisión profesional:** presentar el análisis completo, con la recomendación negativa fundamentada, y ofrecer la alternativa viable si existe.

## Inflar los beneficios para que el número cierre

Ajustar los supuestos hasta que el retorno resulte atractivo es la forma más común de falsear un estudio de viabilidad, y la más difícil de detectar.

**La decisión profesional:** declarar cada supuesto y su fuente, y mostrar cómo cambia el resultado si el supuesto no se cumple.

## Omitir el costo de mantenimiento

Presentar solo el costo de construcción hace ver el proyecto más barato de lo que es. La organización descubre el costo real cuando ya lo tiene instalado.

**La decisión profesional:** informar el costo del ciclo de vida completo.

---

# Errores frecuentes

- **Confundir posible con viable.**
- **Analizar solo la viabilidad técnica**, que es la que menos proyectos hace fracasar.
- **Omitir la viabilidad operativa**, y entregar un sistema que nadie usa.
- **No preguntar por la normativa** cuando hay datos personales o sensibles.
- **Olvidar el costo de mantenimiento.**
- **Olvidar la capacitación de los usuarios.**
- **Ignorar el costo de oportunidad.**
- **Sumar beneficios intangibles** al cálculo económico.
- **No incluir la alternativa de no hacer nada.**
- **Presentar el estudio en lenguaje técnico** a quien tiene que decidir.

---

# Buenas prácticas

✔ Analizar las cinco dimensiones, no solo la técnica.

✔ Cuantificar el costo de no hacer nada.

✔ Informar el costo del ciclo de vida completo, no solo la construcción.

✔ Declarar cada supuesto con su fuente.

✔ Mostrar cómo cambia el resultado si un supuesto falla.

✔ Poner la recomendación al principio.

✔ Presentar siempre al menos tres alternativas.

✔ Informar la inviabilidad cuando existe.

---

# Caso de estudio

## El proyecto que no conviene

Una biblioteca popular con 400 socios y dos empleados quiere un sistema completo de gestión: préstamos, socios, catálogo, reservas en línea y aplicación para celulares.

Datos relevados:

- El catálogo tiene 6.000 títulos, hoy en fichas de cartón.
- Se registran unos 20 préstamos por día.
- La morosidad en devoluciones es del 8 %, sin consecuencia económica.
- La biblioteca se financia con una cuota social de bajo monto y un subsidio municipal.
- El presupuesto disponible para el proyecto es de $1.500.000.
- Los dos empleados tienen más de 60 años y poca experiencia con computadoras.
- No hay nadie que pueda mantener un sistema después de la entrega.
- Existe software libre de gestión bibliotecaria, ya usado por otras bibliotecas populares.

### Para analizar

1. Evalúe las cinco dimensiones de viabilidad. ¿Cuáles fallan?
2. ¿Cuál es el beneficio económico real de este proyecto? ¿Se puede cuantificar?
3. ¿Cuál es el costo de no hacer nada?
4. ¿Qué peso tiene aquí la viabilidad operativa?
5. La existencia de software libre ya probado, ¿cómo cambia el análisis?
6. Redacte la recomendación en cinco líneas, dirigida a la comisión directiva.
7. Si la comisión ya anunció a los socios que va a tener sistema nuevo, ¿cambia su recomendación? ¿Cambia cómo la comunica?

---

# Aplicación profesional

Cada grupo entrega el **informe de viabilidad y costos** de su proyecto.

Este informe tiene una particularidad: es el único entregable del año que puede concluir que **el proyecto no debe hacerse**. Y esa conclusión, si está fundamentada, se evalúa igual de bien que la contraria.

Contenido requerido:

- análisis de las cinco dimensiones, cada una con su conclusión;
- estructura de costos completa, incluyendo mantenimiento, capacitación y costo de oportunidad;
- cuantificación del beneficio con los supuestos declarados;
- cálculo del período de recupero;
- costo de no hacer nada;
- tres alternativas;
- recomendación de una página, en lenguaje no técnico.

La segunda **jornada de práctica en la organización** se dedica al relevamiento de costos y recursos que este informe necesita.

---

# Resumen

En esta unidad aprendimos que:

- Posible y viable no son lo mismo: viable incluye que tenga sentido hacerlo aquí y ahora.
- Las cinco dimensiones son técnica, operativa, económica, temporal y legal; basta que una falle.
- La viabilidad operativa es la que más proyectos técnicamente correctos hace fracasar.
- El estudio de viabilidad es un entregable previo a la decisión, y su función es informar, no aprobar.
- La alternativa de no hacer nada tiene costo y hay que cuantificarla.
- Los costos que se olvidan son capacitación, mantenimiento y costo de oportunidad.
- El mantenimiento suele superar el costo de construcción sobre el ciclo de vida completo.
- Los beneficios intangibles se informan, no se suman.
- Un período de recupero se interpreta contra el horizonte de la organización.
- Informar que un proyecto no es viable es parte del trabajo, no una falla del analista.

---

# Actividad práctica

## Informe de viabilidad y costos

**1. Las cinco dimensiones**

Analicen cada dimensión para su proyecto. Para cada una: qué evaluaron, qué encontraron y una conclusión de una línea.

**2. Estructura de costos**

Construyan la tabla completa de costos, distinguiendo una vez / recurrente y directo / indirecto / oportunidad. Partan de la estimación de esfuerzo de la Unidad 8.

**3. Beneficios**

Cuantifiquen los beneficios. Cada monto debe ir con el supuesto y la fuente del dato. Listen aparte los intangibles.

**4. Retorno**

Calculen el beneficio neto anual y el período de recupero. Muestren el cálculo.

**5. Análisis de sensibilidad**

Elijan el supuesto más frágil. Recalculen el recupero si ese supuesto se cumple a la mitad.

**6. Alternativas y recomendación**

Presenten tres alternativas, una de ellas no hacer nada, y una recomendación de una página en lenguaje no técnico, con la conclusión al principio.

**Formato de entrega:** informe técnico con las planillas de cálculo, más la página de recomendación como documento separado.

---

# Preguntas de repaso

1. ¿Qué diferencia hay entre un proyecto posible y un proyecto viable?

2. Nombre las cinco dimensiones de la viabilidad y la pregunta central de cada una.

3. ¿Por qué la viabilidad operativa hace fracasar proyectos técnicamente correctos?

4. ¿Cómo se distingue una fecha límite real de una negociable?

5. ¿Por qué todo estudio de viabilidad debe incluir la alternativa de no hacer nada?

6. Explique el costo de oportunidad con un ejemplo del proyecto de su grupo.

7. ¿Por qué los beneficios intangibles no se suman al cálculo económico?

8. ¿Por qué presentar un costo de proyecto sin el mantenimiento es informar la mitad del número?

9. ¿Contra qué se interpreta un período de recupero?

10. ¿Qué hace un analista cuando el proyecto que la organización quiere no es viable?

---

# Bibliografía

- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Sección sobre estimación de costos y análisis de viabilidad.
- Sommerville, I. *Ingeniería del Software.* Sección sobre estudio de viabilidad.
- Project Management Institute. [*Guía PMBOK*](https://www.pmi.org/standards/pmbok). Área de Gestión de los Costos. _(acceso pago)_

---

**Fin de la Unidad 9**
