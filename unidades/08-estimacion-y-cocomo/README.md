# Unidad 8
# Estimación y modelos empíricos

> "Una estimación no es una promesa. Presentarla como promesa es el origen de la mayoría de los proyectos incumplidos."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Comprender la estimación como aproximación fundamentada y no como predicción exacta.
- Aplicar técnicas de descomposición.
- Estimar por juicio experto, analogía y tres valores.
- **Aplicar el modelo COCOMO** en sus tres modos y calcular esfuerzo y duración.
- Explicar por qué fallan las estimaciones.
- Registrar el desvío entre estimado y real como insumo de mejora.
- Reconocer la dimensión ética de la estimación.

---

# Qué es estimar

**Estimar** es predecir el esfuerzo, el tiempo o el costo que demandará un trabajo, a partir de la información disponible en ese momento.

Tres propiedades que definen una estimación profesional:

| Propiedad | Significa |
|---|---|
| Es **aproximada** | No es un dato exacto y no debe presentarse como tal |
| Es **fundamentada** | Se apoya en un método, no en una impresión |
| Es **revisable** | Se actualiza cuando aparece información nueva |

La diferencia entre una estimación y una adivinanza no está en el número: está en **poder explicar cómo se llegó a él**.

## Estimación, compromiso y objetivo

Tres cosas que se confunden permanentemente:

| | Qué es | Quién lo fija |
|---|---|---|
| **Estimación** | Cuánto creemos que va a costar | El equipo técnico |
| **Objetivo** | Cuándo la organización querría tenerlo | La organización |
| **Compromiso** | Qué fecha se asume formalmente | Se negocia, con la estimación sobre la mesa |

El error más costoso del rol consiste en dejar que el objetivo reemplace a la estimación. Cuando la organización dice "lo necesito en tres meses" y el equipo responde "entonces son tres meses", no hubo estimación: hubo obediencia.

---

# Técnicas de descomposición

No se puede estimar lo que no se entiende. Y no se entiende lo que es demasiado grande.

**Descomponer** consiste en partir el trabajo hasta llegar a unidades estimables.

Una tarea es estimable cuando cumple tres condiciones:

- se entiende con claridad qué hay que hacer;
- tiene un responsable identificable;
- alguien puede decir cuánto le llevaría, con fundamento.

## Ejemplo

| ❌ No estimable | ✅ Descompuesto y estimable |
|---|---|
| "Hacer el módulo de socios" | Diseñar el modelo de datos de socios · Construir el alta y modificación · Construir la búsqueda · Construir la baja lógica · Validar reglas de negocio · Probar con datos reales · Documentar |

Siete tareas estimables reemplazan a una imposible de estimar.

## Por qué mejora la precisión

Cuando se estima un total de una sola vez, el error se aplica entero al total.

Cuando se estima por partes, los errores individuales se compensan parcialmente: algunos sobran, otros faltan. El total resulta más cercano.

> Regla práctica: si una tarea dura más que el período de control del proyecto, hay que descomponerla más. Con control semanal, ninguna tarea debería estimarse en más de una semana.

## Lo que la descomposición suele olvidar

Estas tareas existen siempre y casi nunca se estiman:

- revisión y corrección;
- validación con el cliente;
- reuniones y coordinación;
- espera de respuestas de terceros;
- documentación;
- pruebas y corrección de lo que aparece en las pruebas;
- puesta en producción.

Un plan que solo estima el trabajo de construcción subestima el proyecto entre un 30 % y un 50 %.

---

# Técnicas de estimación

## Juicio experto

Se consulta a alguien que ya hizo un trabajo similar.

**Ventaja:** rápido y, con experiencia real disponible, razonablemente bueno.
**Límite:** depende de que ese experto exista y de que el trabajo sea efectivamente comparable.

## Estimación por analogía

Se compara con un trabajo anterior del que se conoce el esfuerzo real.

> "El informe de relevamiento del proyecto de la veterinaria nos llevó 22 horas. Este es algo más chico: estimamos 18."

**Requisito:** tener registro del esfuerzo real de proyectos anteriores. Sin histórico, no hay analogía posible.

## Estimación por tres valores

Para cada tarea se estiman tres escenarios:

- **Optimista (O)** — todo sale bien.
- **Más probable (M)** — el escenario realista.
- **Pesimista (P)** — aparecen complicaciones.

El valor esperado se calcula como:

```
E = (O + 4M + P) / 6
```

El peso 4 sobre el valor más probable refleja que ese escenario es el más frecuente. Y el hecho de que el pesimista pese lo mismo que el optimista reconoce algo que la experiencia confirma: **las complicaciones son más frecuentes que los aciertos inesperados**.

### Ejemplo

| Tarea | O | M | P | E = (O+4M+P)/6 |
|---|---|---|---|---|
| Diseñar modelo de datos | 4 h | 6 h | 12 h | 6,7 h |
| Construir alta de socio | 6 h | 8 h | 16 h | 9,0 h |
| Validar reglas de negocio | 3 h | 6 h | 15 h | 7,0 h |
| **Total** | **13 h** | **20 h** | **43 h** | **22,7 h** |

Obsérvese que el total esperado (22,7 h) está más cerca del más probable que del promedio simple entre optimista y pesimista (28 h). La fórmula corrige el sesgo.

> Sobre esta técnica se construye el método **PERT**, que se desarrolla en la Unidad 10.

## La medida de la incertidumbre

La distancia entre el optimista y el pesimista **es información**.

| Tarea | O | P | Diferencia | Lectura |
|---|---|---|---|---|
| A | 6 h | 8 h | 2 h | Bien comprendida |
| B | 4 h | 40 h | 36 h | No se entiende el trabajo |

La tarea B no necesita una estimación mejor: necesita que alguien averigüe qué hay que hacer antes de estimarla.

---

# Modelos empíricos: COCOMO

Los modelos empíricos calculan el esfuerzo a partir del **tamaño estimado del producto**, usando fórmulas derivadas de datos históricos de muchos proyectos reales.

**COCOMO** (*Constructive Cost Model*) es el más conocido. Fue construido por Barry Boehm a partir del análisis de decenas de proyectos.

## Los tres modos

COCOMO clasifica los proyectos en tres modos según su complejidad y sus restricciones.

| Modo | Características | Ejemplo |
|---|---|---|
| **Orgánico** | Equipo pequeño, dominio conocido, requisitos flexibles, poca rigidez | Sistema administrativo para un club |
| **Semiacoplado** | Complejidad y rigidez intermedias, equipo con experiencia mixta | Sistema de facturación con integraciones |
| **Empotrado** | Restricciones fuertes de hardware, normativa o tiempo real | Software de control de un equipo médico |

## Las fórmulas del modelo básico

El **esfuerzo** se expresa en persona-mes y el **tamaño** en KLDC (miles de líneas de código).

| Modo | Esfuerzo (persona-mes) | Duración (meses) |
|---|---|---|
| Orgánico | E = 2,4 × (KLDC)^1,05 | D = 2,5 × E^0,38 |
| Semiacoplado | E = 3,0 × (KLDC)^1,12 | D = 2,5 × E^0,35 |
| Empotrado | E = 3,6 × (KLDC)^1,20 | D = 2,5 × E^0,32 |

Y la cantidad de personas se deriva:

```
Personas = E / D
```

## Lo que dicen los exponentes

El exponente del esfuerzo es **mayor que 1** en los tres modos.

Eso significa que el esfuerzo crece **más rápido** que el tamaño: duplicar el tamaño del sistema más que duplica el esfuerzo.

La razón es la comunicación. Un sistema más grande necesita más gente, y más gente necesita coordinarse entre sí, lo que consume esfuerzo que no produce producto.

> Esta es la formalización matemática de algo conocido: **agregar gente a un proyecto atrasado lo atrasa más**.

---

## Cálculo completo: Club Deportivo San Martín

### Paso 1 — Tamaño estimado

De la Unidad 7: **116 puntos función**.

Con un factor de conversión de aproximadamente 100 líneas por punto función para el lenguaje elegido:

```
116 PF × 100 LDC/PF = 11.600 LDC ≈ 12 KLDC
```

### Paso 2 — Modo

Equipo chico, dominio administrativo conocido, sin restricciones de tiempo real ni normativa estricta: **modo orgánico**.

### Paso 3 — Esfuerzo

```
E = 2,4 × (12)^1,05

12^1,05 = 13,588

E = 2,4 × 13,588 = 32,6 persona-mes
```

### Paso 4 — Duración

```
D = 2,5 × (32,6)^0,38

32,6^0,38 = 3,759

D = 2,5 × 3,759 = 9,4 meses
```

### Paso 5 — Equipo

```
Personas = 32,6 / 9,4 = 3,5 personas
```

### Resultado

| | |
|---|---|
| Tamaño | 12 KLDC (116 PF) |
| Esfuerzo | 32,6 persona-mes |
| Duración | 9,4 meses |
| Equipo | 3 a 4 personas |

### Comparación entre modos

El mismo tamaño de 12 KLDC, según el modo:

| Modo | Esfuerzo | Duración | Personas |
|---|---|---|---|
| Orgánico | 32,6 p-mes | 9,4 meses | 3,5 |
| Semiacoplado | 48,5 p-mes | 9,7 meses | 5,0 |
| Empotrado | 71,0 p-mes | 9,8 meses | 7,3 |

El mismo sistema cuesta **más del doble** en modo empotrado que en orgánico. La duración casi no cambia; lo que cambia es la cantidad de gente necesaria.

Elegir bien el modo es, por lo tanto, la decisión más determinante del cálculo.

---

## Límites de COCOMO

- **Depende de estimar KLDC**, que en la etapa de análisis es en sí mismo una estimación. Se arrastra la incertidumbre del paso anterior.
- **La conversión de PF a LDC depende del lenguaje** y del estilo, y los factores de referencia son promedios de la industria.
- **Fue calibrado con proyectos de otra época** y de otro tipo de organización.
- **No contempla** herramientas modernas, reutilización masiva de componentes ni frameworks.

## Entonces, ¿para qué usarlo?

Por dos razones prácticas:

1. **Como contraste.** Si la estimación por descomposición del equipo da 8 persona-mes y COCOMO da 32, hay algo que revisar. Puede estar mal COCOMO o puede estar mal la descomposición, pero la discrepancia obliga a mirar.
2. **Como orden de magnitud fundamentado**, en un momento en el que no hay ningún otro dato disponible.

> Ninguna técnica de estimación se usa sola. La práctica profesional consiste en estimar por dos métodos independientes y explicar la diferencia.

---

# Por qué fallan las estimaciones

| Causa | Cómo se manifiesta |
|---|---|
| Se estima el trabajo ideal | Sin interrupciones, reuniones ni cambios de contexto |
| Se olvidan tareas no constructivas | Revisión, validación, documentación, pruebas |
| Se subestima la coordinación | Más gente implica más comunicación |
| Optimismo sistemático | Se estima el escenario en que todo sale bien |
| Presión sobre el estimador | Se ajusta el número a lo que se quiere escuchar |
| No se contempla la espera | Respuestas de terceros, aprobaciones, provisión de recursos |
| Falta de histórico propio | Se usan valores de la industria como si fueran propios |

## El registro estimado contra real

Es la práctica que más mejora las estimaciones futuras, y la que menos se hace.

| Tarea | Estimado | Real | Desvío |
|---|---|---|---|
| Diseñar modelo de datos | 6,7 h | 9 h | +34 % |
| Construir alta de socio | 9,0 h | 8 h | −11 % |
| Validar reglas de negocio | 7,0 h | 18 h | +157 % |

La tercera fila es el hallazgo valioso: si "validar reglas de negocio" se subestima sistemáticamente, la organización aprende a multiplicar por 2,5 ese tipo de tarea.

Un equipo maduro no aspira a estimar perfecto. Aspira a **conocer su propio sesgo**.

---

# La dimensión ética de la estimación

Aquí la ética profesional no es un tema abstracto: aparece en un número.

## Estimar por debajo para ganar el trabajo

La organización tiene un presupuesto y la estimación lo excede.

Bajar el número consigue el contrato y garantiza el conflicto: el proyecto se va a atrasar, se va a recortar en calidad, o va a terminar en discusión.

**La decisión profesional:** informar la estimación real y proponer un alcance menor que sí entre en el presupuesto.

## Aceptar la fecha que fija el cliente

Cuando la organización pone la fecha y el equipo asiente sin recalcular, no hay estimación.

**La decisión profesional:** presentar la estimación, mostrar la brecha, y ofrecer las alternativas: más plazo, menos alcance o más recursos. La decisión es de la organización, pero tomada con la información sobre la mesa.

## Presentar una estimación como certeza

Una estimación con alta incertidumbre presentada como número único induce a error.

**La decisión profesional:** informar el rango. "Entre 8 y 12 meses, con 9,4 como valor esperado" es más honesto y más útil que "9,4 meses".

> Quien firma una estimación responde por su fundamento. Una estimación deliberadamente baja no es un error de cálculo: es una afirmación falsa hecha por conveniencia.

---

# Errores frecuentes

- **Estimar sin descomponer.**
- **Estimar solo la construcción** y omitir revisión, validación y documentación.
- **Confundir estimación con compromiso.**
- **Dejar que el objetivo de la organización reemplace la estimación.**
- **Usar un solo método** y no contrastar.
- **No registrar el tiempo real**, perdiendo el insumo de mejora.
- **Presentar un número único** cuando la incertidumbre es alta.
- **Elegir mal el modo de COCOMO**, que es la variable más sensible del cálculo.
- **Estimar una tarea que nadie entiende** en lugar de averiguar primero qué hay que hacer.

---

# Buenas prácticas

✔ Descomponer antes de estimar.

✔ Incluir las tareas no constructivas.

✔ Estimar por dos métodos independientes y explicar la diferencia.

✔ Usar tres valores cuando la incertidumbre es relevante.

✔ Tratar la distancia optimista-pesimista como medida de lo que no se sabe.

✔ Informar rangos, no números únicos.

✔ Registrar estimado contra real, siempre.

✔ Distinguir con claridad estimación, objetivo y compromiso.

---

# Caso de estudio

## La reunión de presupuesto

El equipo estimó el sistema del club por descomposición: **28 persona-mes**. COCOMO en modo orgánico dio **32,6**. El equipo informa un rango de 28 a 33.

En la reunión, la comisión directiva plantea:

> "Nosotros tenemos presupuesto para 18 persona-mes y necesitamos el sistema andando para el inicio de la temporada, en 6 meses."

### Para analizar

1. ¿Cuál es la brecha entre lo estimado y lo disponible, en esfuerzo y en plazo?
2. ¿Qué haría la salida cómoda en esa reunión? ¿Qué consecuencia tendría?
3. Proponga tres alternativas concretas para presentar a la comisión, con su consecuencia cada una.
4. Si se recorta alcance, ¿qué recortaría primero y con qué criterio? Use el diagnóstico de la Unidad 4.
5. ¿Cómo redactaría, en dos oraciones y en lenguaje no técnico, la respuesta a la comisión?
6. Si la comisión insiste en las 18 persona-mes sin recortar alcance, ¿qué deja usted por escrito?

---

# Aplicación profesional

Cada grupo entrega la **estimación de esfuerzo** de su proyecto, que debe contener:

- la descomposición del trabajo en tareas estimables;
- la estimación por tres valores de cada tarea, con el valor esperado;
- el cálculo de COCOMO a partir de los puntos función de la Unidad 7, con el modo elegido y su justificación;
- la comparación entre ambos métodos y la explicación de la diferencia;
- el rango informado y no un número único;
- la planilla de registro estimado contra real, para completar durante el proyecto.

Esta estimación es el insumo directo del análisis de costos de la **Unidad 9** y del cronograma de la **Unidad 10**.

---

# Resumen

En esta unidad aprendimos que:

- Estimar es aproximar de forma fundamentada y revisable, no predecir con exactitud.
- Estimación, objetivo y compromiso son tres cosas distintas, y confundirlas es el error más costoso del rol.
- No se puede estimar lo que no se descompuso.
- Las tareas no constructivas se olvidan siempre y explican entre el 30 % y el 50 % del esfuerzo.
- La fórmula de tres valores es E = (O + 4M + P) / 6, y la distancia entre O y P mide la incertidumbre.
- COCOMO calcula esfuerzo y duración a partir del tamaño, con tres modos según complejidad y rigidez.
- Los exponentes mayores que 1 formalizan que el esfuerzo crece más rápido que el tamaño.
- COCOMO se usa como contraste y como orden de magnitud, no como verdad.
- Registrar estimado contra real es lo que permite conocer el propio sesgo.
- Una estimación deliberadamente baja es una afirmación falsa, no un error de cálculo.

---

# Actividad práctica

## Estimación del proyecto

**1. Descomposición**

Descompongan su proyecto en un mínimo de quince tareas estimables. Incluyan explícitamente al menos tres tareas no constructivas.

**2. Tres valores**

Estimen cada tarea con optimista, más probable y pesimista. Calculen el valor esperado y el total.

**3. Análisis de incertidumbre**

Identifiquen las tres tareas con mayor distancia entre optimista y pesimista. Para cada una, indiquen qué habría que averiguar para reducir esa distancia.

**4. COCOMO**

A partir de los puntos función de la Unidad 7, estimen KLDC, elijan el modo justificándolo, y calculen esfuerzo, duración y cantidad de personas. Muestren el cálculo paso a paso.

**5. Contraste**

Comparen el total por descomposición con el resultado de COCOMO. Si difieren en más del 30 %, expliquen a qué lo atribuyen.

**6. Informe**

Redacten el resultado como lo presentarían a la organización: en rango, en lenguaje no técnico, y con la aclaración de qué supuestos lo sostienen.

**Formato de entrega:** informe técnico con las planillas de cálculo.

---

# Preguntas de repaso

1. ¿Qué distingue una estimación de una adivinanza?

2. Explique la diferencia entre estimación, objetivo y compromiso.

3. ¿Por qué estimar por descomposición es más preciso que estimar el total de una vez?

4. Nombre cuatro tareas que la descomposición suele olvidar.

5. Escriba la fórmula de tres valores y explique por qué el más probable pesa 4.

6. ¿Qué información aporta la distancia entre el optimista y el pesimista?

7. ¿Cuáles son los tres modos de COCOMO y qué los distingue?

8. ¿Por qué el exponente del esfuerzo en COCOMO es mayor que 1, y qué consecuencia práctica tiene?

9. Mencione dos límites de COCOMO y explique para qué conviene usarlo igual.

10. ¿Por qué una estimación deliberadamente baja es una falta ética y no un error técnico?

---

# Bibliografía

- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Capítulo sobre estimación, técnicas de descomposición y modelos empíricos.
- Sommerville, I. *Ingeniería del Software.* Sección sobre estimación de costos.
- [Atlassian — Estimación en gestión de proyectos](https://www.atlassian.com/es/agile/project-management/estimation)
- Project Management Institute. [*Guía PMBOK*](https://www.pmi.org/standards/pmbok). Área de Gestión de los Costos. _(acceso pago)_

---

**Fin de la Unidad 8**
