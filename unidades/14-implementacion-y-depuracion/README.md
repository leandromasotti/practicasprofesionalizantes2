# Unidad 14
# Implementación, estándares y depuración

> "El código se escribe una vez y se lee cien. Escribirlo para que se entienda no es una cortesía: es la decisión económica correcta."

---

# Objetivos de aprendizaje

Al finalizar esta unidad el estudiante será capaz de:

- Ubicar la etapa de implementación dentro del proyecto.
- Comprender qué son los estándares de programación y por qué una organización los adopta.
- Reconocer las pautas de programación que hacen mantenible un sistema.
- Distinguir error, defecto y falla.
- Aplicar un proceso de depuración con estrategia.
- Registrar y hacer seguimiento de defectos.

> **Articulación.** Algoritmos y Estructuras de Datos II desarrolla las técnicas de testing —pruebas de unidad, integración, aceptación, TDD— y de refactoring. Aquí se aborda la implementación desde la conducción del proyecto: qué exige la organización, cómo se ordena el trabajo y cómo se gestionan los defectos.

---

# La implementación dentro del proyecto

De la Unidad 10 sabemos que la construcción representa entre el 30 % y el 40 % del esfuerzo del proyecto: es la etapa más grande, pero no es la mayoría.

Lo que la distingue no es su tamaño sino su **visibilidad**. Es la etapa donde el proyecto empieza a producir algo que se puede ver, y donde las decisiones tomadas antes se vuelven costosas de cambiar.

## Qué se decide antes de escribir código

| Decisión | Consecuencia de no tomarla |
|---|---|
| Estándares de codificación | Cada integrante escribe distinto y el resultado es ilegible |
| Convenciones de nombres | Nadie encuentra nada |
| Estructura del proyecto | Los archivos terminan donde cayeron |
| Procedimiento de revisión | Los defectos llegan a producción |
| Qué se prueba y quién | Se prueba lo que a cada uno le parece |
| Cómo se registra un defecto | Los defectos se pierden en conversaciones |

Estas decisiones son parte de la planificación, no de la construcción. Tomarlas a mitad de camino cuesta reescribir lo hecho.

---

# Estándares de programación y procedimientos

Un **estándar de programación** es un conjunto de reglas acordadas sobre cómo se escribe el código en una organización.

## Qué cubre

| Aspecto | Ejemplo de regla |
|---|---|
| Nombres | Las variables en minúscula separadas por guion bajo; las clases con inicial mayúscula |
| Indentación y formato | Cuatro espacios, líneas de hasta 100 caracteres |
| Comentarios | Se comenta el por qué, no el qué |
| Longitud | Una función no debería exceder una pantalla |
| Manejo de errores | Toda operación que puede fallar tiene su tratamiento |
| Estructura de archivos | Dónde va cada tipo de archivo |
| Registro | Qué se registra en el log y con qué nivel |

## Por qué una organización los adopta

No es una cuestión estética. Son cuatro razones económicas:

**1. El código se lee mucho más de lo que se escribe.** Cada minuto ahorrado en escritura a costa de legibilidad se paga muchas veces al leerlo.

**2. La gente rota.** El sistema va a ser mantenido por personas que no lo escribieron. Un estándar hace que el código sea familiar aunque sea ajeno.

**3. La revisión se vuelve posible.** Revisar código que cada uno escribe a su manera consume el doble de tiempo, porque hay que entender el estilo antes de entender la lógica.

**4. Los defectos se detectan antes.** Un código uniforme hace que lo anómalo se destaque.

## Qué pierde una organización sin estándares

- Cada módulo requiere aprender el estilo de quien lo escribió.
- El costo de mantenimiento crece con cada persona que pasó por el sistema.
- La incorporación de alguien nuevo tarda mucho más.
- Las revisiones se vuelven discusiones de estilo en lugar de discusiones de fondo.

> Cualquier estándar razonable aplicado de forma consistente es mejor que el mejor estándar aplicado a medias. Lo que produce el beneficio es la uniformidad, no la elección particular de reglas.

---

# Pautas para la programación

## Legibilidad

| Pauta | Por qué |
|---|---|
| Nombres que describen la intención | `dias_hasta_vencimiento` en lugar de `d` |
| Funciones que hacen una sola cosa | Se entienden, se prueban y se reutilizan |
| Evitar la anidación profunda | Tres niveles ya es difícil de seguir |
| Constantes con nombre en lugar de números sueltos | `DIAS_DE_GRACIA = 10` en lugar de `10` repartido en el código |
| Comentar el por qué, no el qué | El código dice qué hace; el comentario, por qué se hizo así |

## El comentario útil

| ❌ Redundante | ✅ Útil |
|---|---|
| `// suma uno al contador` | `// El vencimiento se cuenta desde el dia 10 por reglamento del club, art. 14` |
| `// recorre la lista` | `// Se recorre en orden inverso porque los pagos parciales se imputan al periodo mas antiguo` |

Un comentario que repite el código envejece mal: el código cambia y el comentario queda mintiendo.

## Revisión entre pares

Es la práctica de control de calidad con mejor relación costo-beneficio que existe.

| | |
|---|---|
| **Qué es** | Otra persona lee el cambio antes de que se integre |
| **Cuánto cuesta** | Minutos |
| **Qué detecta** | Defectos, decisiones discutibles, código difícil de mantener |
| **Beneficio adicional** | Distribuye el conocimiento del sistema, lo que mitiga el riesgo de dependencia de una sola persona |

Se implementa con los pull requests de la Unidad 13.

> Una regla que funciona: nadie prueba ni revisa lo que escribió.

---

# Error, defecto y falla

Tres términos que se usan como sinónimos y designan cosas distintas.

| Término | Qué es | Dónde ocurre |
|---|---|---|
| **Error** | La equivocación humana | En la persona |
| **Defecto** | La consecuencia de esa equivocación en el producto | En el código o el documento |
| **Falla** | La manifestación del defecto durante la ejecución | En el uso |

## Ejemplo

| | |
|---|---|
| **Error** | El programador entendió que la cuota vence a los 30 días |
| **Defecto** | El código calcula el vencimiento sumando 30 días en lugar de tomar el día 10 del mes siguiente |
| **Falla** | Un socio recibe un aviso de deuda que no corresponde |

## Por qué importa la distinción

Porque cada nivel se ataca de manera distinta:

- La **falla** se corrige atendiendo el caso.
- El **defecto** se corrige cambiando el código.
- El **error** se previene mejorando la comunicación del requerimiento.

Un equipo que solo corrige fallas corrige el mismo problema muchas veces. Uno que llega al error deja de producir esa clase de defecto.

> Es la misma cadena síntoma-problema-causa de la Unidad 4, aplicada al software.

Además: **un defecto puede existir sin producir falla**, si nadie ejecuta ese camino. Eso no significa que no esté.

---

# La depuración

**Depurar** es el proceso de localizar y corregir la causa de una falla.

Es distinto de probar: las pruebas **detectan** que algo está mal; la depuración **encuentra por qué**.

## El proceso

| Paso | Qué se hace |
|---|---|
| 1. **Reproducir** | Conseguir que la falla ocurra de forma consistente |
| 2. **Acotar** | Reducir el caso al mínimo que todavía falla |
| 3. **Hipotetizar** | Formular una explicación concreta y verificable |
| 4. **Verificar** | Probar la hipótesis, no suponerla |
| 5. **Corregir** | Cambiar la causa, no el síntoma |
| 6. **Verificar la corrección** | Confirmar que la falla desapareció |
| 7. **Verificar que no rompió otra cosa** | Volver a probar lo que ya funcionaba |

El paso 1 es el que se saltea, y sin él todo lo demás es adivinar. **Una falla que no se puede reproducir no se puede corregir con certeza**: solo se puede corregir con esperanza.

El paso 7 es el que se olvida. Una corrección que introduce dos defectos nuevos es peor que la falla original.

## Estrategias

| Estrategia | Cómo funciona | Cuándo conviene |
|---|---|---|
| **Búsqueda binaria** | Partir el espacio del problema en dos y determinar en qué mitad está | Cuando el recorrido es largo |
| **Vuelta atrás** | Partir del punto de la falla y retroceder | Cuando la falla es localizada |
| **Comparación de versiones** | Buscar qué cambió desde la última versión que funcionaba | Cuando algo dejó de funcionar |
| **Eliminación de causas** | Listar las causas posibles y descartarlas de a una | Cuando hay varias hipótesis |

La tercera es la más rápida y depende directamente de tener buen control de versiones. Con un historial de commits chicos y bien descritos, encontrar el cambio que introdujo la falla toma minutos. Con doce commits llamados "avances", toma días.

> Es un beneficio concreto de la Unidad 13 que se cobra en esta.

## Errores al depurar

- **Corregir el síntoma.** Agregar una validación que oculta la falla en lugar de arreglar el cálculo.
- **Cambiar cosas sin hipótesis**, hasta que "deja de fallar". Nunca se supo por qué fallaba, así que va a volver.
- **No verificar la corrección.**
- **No volver a probar el resto.**
- **Corregir sin registrar** qué se corrigió, con lo que se pierde la información.

---

# Registro y seguimiento de defectos

Un defecto que no se registra se olvida o se descubre en producción.

## Qué registra una ficha de defecto

| Campo | Contenido |
|---|---|
| Identificador | Número único |
| Descripción | Qué se observa |
| Pasos para reproducir | La secuencia exacta |
| Resultado esperado | Qué debería pasar |
| Resultado obtenido | Qué pasa |
| Severidad | Impacto en el uso |
| Prioridad | Urgencia de la corrección |
| Estado | Abierto, en corrección, corregido, verificado, cerrado |
| Responsable | Quién lo corrige |
| Versión | Dónde se detectó y dónde se corrigió |

## Severidad y prioridad no son lo mismo

| | Qué mide | Quién la fija |
|---|---|---|
| **Severidad** | Cuán grave es la consecuencia | Quien reporta |
| **Prioridad** | Cuán urgente es corregirlo | Quien conduce el proyecto |

Un defecto de severidad alta y prioridad baja es posible: un cálculo grave que solo ocurre en un caso que se da una vez al año.

Uno de severidad baja y prioridad alta también: un error de ortografía en la pantalla principal, el día antes de la presentación al cliente.

## Escala de severidad

| Nivel | Descripción |
|---|---|
| **Bloqueante** | Impide seguir usando el sistema |
| **Grave** | Funcionalidad importante no sirve, o hay datos incorrectos |
| **Moderado** | Molesta pero hay forma de seguir |
| **Leve** | Cosmético o menor |

## Métricas de defectos

| Métrica | Qué informa |
|---|---|
| Defectos abiertos | Deuda de calidad pendiente |
| Defectos por semana | Si la calidad mejora o empeora |
| Tiempo promedio de corrección | Capacidad de respuesta |
| Defectos reabiertos | Correcciones que no corrigieron |
| Defectos por etapa de detección | Cuánto antes se detectan |

La última es la más valiosa. **Un defecto detectado en el análisis cuesta una fracción de lo que cuesta el mismo defecto detectado en producción.** Medir dónde se detectan indica si conviene invertir más en revisión temprana.

Y la penúltima es la señal de alerta: una tasa alta de defectos reabiertos indica que se está corrigiendo el síntoma.

> Estas son métricas del proyecto y del proceso, en el sentido de la Unidad 7. Y aplica la misma advertencia: si se usa "defectos reportados" para evaluar personas, se reportan menos defectos.

---

# Errores frecuentes

- **Empezar a construir sin acordar estándares.**
- **Comentar qué hace el código** en lugar de por qué.
- **Confundir error, defecto y falla**, y corregir solo el nivel visible.
- **Depurar sin reproducir primero.**
- **Cambiar código sin hipótesis** hasta que la falla desaparece.
- **No volver a probar** después de corregir.
- **Confundir severidad con prioridad.**
- **No registrar los defectos**, y gestionarlos por conversación.
- **Que cada uno pruebe lo que escribió.**
- **Recortar la revisión** cuando el cronograma aprieta.

---

# Buenas prácticas

✔ Acordar estándares antes de escribir la primera línea.

✔ Preferir la uniformidad a la elección particular de reglas.

✔ Nombres que describan la intención.

✔ Comentar el por qué.

✔ Revisión entre pares de todo cambio.

✔ Nadie prueba ni revisa lo que escribió.

✔ Reproducir antes de depurar.

✔ Corregir la causa, no el síntoma.

✔ Registrar todo defecto con pasos para reproducir.

✔ Medir en qué etapa se detectan los defectos.

---

# Caso de estudio

## La corrección que no corrigió

Reporte recibido: *"A algunos socios el sistema les muestra deuda cuando están al día."*

Lo que hizo el equipo:

1. Revisaron el caso del socio que reclamó.
2. Encontraron que tenía un pago registrado dos veces.
3. Borraron el pago duplicado.
4. El socio dejó de aparecer con deuda.
5. Cerraron el defecto como corregido.

Tres semanas después llegaron once reclamos iguales.

Datos adicionales:

- El pago duplicado se produce cuando la administrativa presiona "Guardar" dos veces porque el sistema tarda en responder.
- El cálculo de deuda considera solo el último pago registrado por período, no la suma.
- No existe validación de pago duplicado.
- No hay ficha de defecto: el caso se resolvió por WhatsApp.

### Para analizar

1. Identifique el error, el defecto y la falla de este caso.
2. ¿Qué nivel corrigió el equipo? ¿Por qué volvieron los reclamos?
3. ¿Cuántos defectos distintos hay realmente en esta situación? Enúncielos.
4. ¿Qué pasos del proceso de depuración se omitieron?
5. Redacte la ficha de defecto que debería haberse abierto, con todos sus campos.
6. Asigne severidad y prioridad a cada defecto identificado, y justifique.
7. ¿Qué habría detectado este problema antes de que llegara a producción?
8. ¿Qué métrica de defectos habría dado la alerta a las tres semanas?

---

# Aplicación profesional

Cada grupo entrega:

- el **acuerdo de estándares** de su proyecto: convenciones de nombres, formato, comentarios y estructura de archivos, en una página;
- el **procedimiento de revisión** adoptado: quién revisa qué y en qué momento;
- el **registro de defectos** del proyecto, con al menos cinco fichas completas;
- la **métrica de etapa de detección**: en qué etapa se detectó cada defecto.

Para el proyecto integrador de esta materia, que produce fundamentalmente documentos, los estándares aplican igual: convenciones de nombres de archivo, formato de los informes, y revisión entre pares antes de entregar.

---

# Resumen

En esta unidad aprendimos que:

- Las decisiones sobre estándares y procedimientos son parte de la planificación, no de la construcción.
- Los estándares se adoptan por razones económicas: el código se lee mucho más de lo que se escribe y la gente rota.
- La uniformidad produce más beneficio que la elección particular de reglas.
- El comentario útil explica el por qué; el que repite el código envejece mintiendo.
- La revisión entre pares es el control de calidad con mejor relación costo-beneficio, y además distribuye conocimiento.
- Error, defecto y falla son cosas distintas y se atacan de manera distinta.
- Un equipo que solo corrige fallas corrige el mismo problema muchas veces.
- La depuración empieza por reproducir; sin eso, es adivinar.
- La comparación de versiones es la estrategia más rápida y depende de tener buen control de versiones.
- Severidad y prioridad son independientes.
- La métrica más valiosa es en qué etapa se detectan los defectos, porque el costo de corregir crece con la etapa.

---

# Actividad práctica

## Estándares y gestión de defectos

**1. Acuerdo de estándares**

Redacten el estándar de su grupo, cubriendo al menos: nombres de archivos, estructura de carpetas, formato de los documentos, convenciones de redacción y, si hay código, convenciones de codificación. Máximo una página.

**2. Procedimiento de revisión**

Definan quién revisa qué, en qué momento y con qué criterio de aprobación. Debe cumplir la regla de que nadie revise lo propio.

**3. Análisis de la cadena**

Tomen un defecto real detectado en su proyecto —puede ser un error en un documento— e identifiquen el error, el defecto y la falla. Indiquen qué haría falta para prevenir el error, no solo corregir el defecto.

**4. Fichas de defecto**

Abran cinco fichas de defecto completas sobre su proyecto, con todos los campos, incluyendo pasos para reproducir.

**5. Severidad y prioridad**

Asignen severidad y prioridad a cada ficha, con una línea de justificación. Debe haber al menos un caso donde severidad y prioridad no coincidan.

**6. Etapa de detección**

Para cada defecto, indiquen en qué etapa se detectó y en qué etapa se introdujo. Calculen cuántos se detectaron en la misma etapa en que se introdujeron.

**Formato de entrega:** informe técnico con el estándar como anexo.

---

# Preguntas de repaso

1. ¿Qué decisiones deben tomarse antes de empezar a construir, y por qué son parte de la planificación?

2. Enuncie las cuatro razones económicas por las que una organización adopta estándares.

3. ¿Por qué la uniformidad importa más que la elección particular de reglas?

4. ¿Qué distingue un comentario útil de uno redundante?

5. Explique la diferencia entre error, defecto y falla con un ejemplo propio.

6. ¿Por qué un equipo que solo corrige fallas corrige el mismo problema muchas veces?

7. ¿Puede existir un defecto sin falla? Justifique.

8. ¿Por qué el primer paso de la depuración es reproducir?

9. ¿De qué depende que la estrategia de comparación de versiones sea rápida?

10. Dé un ejemplo de defecto con severidad alta y prioridad baja, y otro al revés.

11. ¿Por qué la métrica de etapa de detección es la más valiosa?

---

# Bibliografía

- Pressman, R. *Ingeniería del Software: Un enfoque práctico.* Capítulos sobre implementación, técnicas de prueba y depuración.
- Sommerville, I. *Ingeniería del Software.* Capítulo sobre verificación y validación.
- [Refactoring Guru — Código con olor](https://refactoring.guru/es/refactoring/smells)
- [Markdown Guide](https://www.markdownguide.org/) — para las convenciones de documentación del proyecto.

---

**Fin de la Unidad 14**
