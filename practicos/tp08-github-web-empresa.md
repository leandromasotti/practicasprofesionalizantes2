# TP8 — Trabajo colaborativo con GitHub: web de una empresa

> **Unidad:** [13 — Gestión de la Configuración del Software](../unidades/13-gestion-de-configuracion/)
> **Modalidad:** grupal, 3 a 4 integrantes, con responsabilidad individual asignada
> **Entregable:** repositorio en GitHub más informe de trabajo
> **Puntaje:** 100 puntos

---

## Objetivo

Aprender a trabajar en equipo bajo control de versiones, construyendo la web de una empresa ficticia.

Es el único práctico del año con producto de software. Su objeto no es la web: es el **mecanismo de trabajo colaborativo** que la unidad 13 desarrolla como marco.

---

## Preparación

### Paso 1 — Crear el repositorio

> Lo hace **un solo integrante**: el Team Leader.

1. Ingresar a GitHub.
2. **New repository**.
3. Nombre: `empresa-web-grupoX`.
4. Visibilidad: **público**.
5. **Create repository**.

**Agregar a los compañeros:** Settings → Collaborators → agregar a todos los integrantes.

### Paso 2 — Estructura inicial

El Team Leader crea los archivos base y hace el primer commit:

```
index.html
about.html
contact.html
styles.css
README.md
```

Mensaje del primer commit: `Crea la estructura inicial del proyecto`.

El **README.md** debe indicar: nombre de la empresa, integrantes del grupo y quién es responsable de cada página.

### Paso 3 — Clonar

> Lo hacen **todos** los integrantes.

```bash
git clone <URL_DEL_REPOSITORIO>
cd empresa-web-grupoX
```

---

## Desarrollo

### Paso 4 — Crear la rama propia

Cada integrante trabaja **en su propia rama**:

```bash
git checkout -b feature/home
git checkout -b feature/about
git checkout -b feature/contact
git checkout -b feature/estilos
```

### Paso 5 — Desarrollar su parte

| Responsable | Archivo | Requisitos mínimos |
|---|---|---|
| Home | `index.html` | Nombre de la empresa, una imagen, menú de navegación |
| About | `about.html` | Historia de la empresa, misión o descripción |
| Contact | `contact.html` | Formulario con nombre, correo y mensaje |
| Estilos | `styles.css` | Hoja de estilos común a las tres páginas |

> Si el grupo es de tres, el responsable de estilos se reparte entre los tres o se suma a una de las páginas.

### Paso 6 — Registrar cambios

Cada vez que avancen:

```bash
git add .
git commit -m "Descripcion clara de lo que se hizo"
```

Ejemplos de mensajes correctos:

- `Agrega el encabezado y el menu de navegacion a la home`
- `Crea la seccion de historia de la empresa`
- `Agrega el formulario de contacto con validacion de correo`

### Paso 7 — Subir la rama

```bash
git push origin feature/home
```

### Paso 8 — Pull request

1. Ir al repositorio en GitHub.
2. **Compare & pull request**.
3. Escribir una descripción de qué se hizo.
4. **Create pull request**.

### Paso 9 — Revisión e integración

> La revisión la hace **otro integrante**, no el autor.

El revisor deja al menos un comentario en el pull request: una observación, una sugerencia o una aprobación fundamentada.

El Team Leader integra a la rama principal con **Merge**.

### Paso 10 — Resolver conflictos

Si aparece un conflicto:

1. Leer el mensaje: Git indica el archivo y las líneas.
2. Abrir el archivo y ver ambas versiones marcadas.
3. Decidir qué queda: una, la otra, o una combinación.
4. Borrar las marcas del conflicto.
5. Confirmar con un commit.

> Un conflicto no es un error. Es Git avisando que hay una decisión que una persona tiene que tomar.

---

## Cierre

### Paso 11 — Resultado

El proyecto terminado debe tener:

- navegación funcionando entre las tres páginas;
- diseño aplicado desde la hoja de estilos común;
- contenido completo en cada página.

### Paso 12 — Línea base

El Team Leader crea una **etiqueta** sobre el commit final:

```bash
git tag -a v1.0 -m "Version entregada del TP8"
git push origin v1.0
```

Esto es una línea base, en el sentido de la Unidad 13: una versión revisada y aprobada, identificada.

---

## Informe de trabajo

Además del repositorio, entreguen un informe de una página con:

| Punto | Contenido |
|---|---|
| Enlace al repositorio | URL |
| Reparto | Quién hizo cada parte |
| Conflictos | Si hubo, cuáles y cómo se resolvieron |
| Problemas | Qué dificultades aparecieron |
| Aprendizaje | Qué harían distinto la próxima vez |

---

## Reglas

| | Regla |
|---|---|
| ❌ | **No trabajar directamente en la rama principal** |
| ❌ | **No sobrescribir el trabajo de un compañero** |
| ❌ | **No fusionar sin revisión** de otro integrante |
| ✅ | Commits chicos y frecuentes |
| ✅ | Mensajes de commit descriptivos |
| ✅ | Avisar al equipo qué se está haciendo |
| ✅ | Probar la página antes de subir |

---

## Criterios de evaluación

| Criterio | Puntos |
|---|---|
| **Repositorio** creado, público, con todos los integrantes como colaboradores | 5 |
| **README** con integrantes y responsabilidades | 5 |
| **Una rama por integrante**, con nombre descriptivo | 10 |
| **Ningún commit directo** a la rama principal | 15 |
| **Commits chicos y frecuentes** — mínimo cuatro por integrante | 10 |
| **Mensajes de commit** que expliquen qué cambió | 15 |
| **Pull requests** — uno por integrante, con descripción | 10 |
| **Revisión cruzada** — cada PR revisado por otro integrante, con comentario | 10 |
| **Producto** — tres páginas con navegación y estilos aplicados | 10 |
| **Etiqueta de línea base** creada | 5 |
| **Informe** con reparto, conflictos y aprendizaje | 5 |
| **Total** | **100** |

---

## Lo que baja la nota

| Situación | Descuento |
|---|---|
| Commits directos a la rama principal | −5 cada uno |
| Un solo integrante con commits (los demás no participaron) | −30 |
| Mensajes de commit como "cambios", "arreglos", "subo lo de hoy", "final" | −3 cada uno |
| Un único commit gigante por integrante | −8 cada uno |
| Pull request fusionado por su propio autor sin revisión | −5 cada uno |
| Pull request sin descripción | −3 cada uno |
| Archivos versionados con nombres tipo `index_final_v2.html` | −5 |
| Sin etiqueta de línea base | −5 |
| Sin informe | −5 |

---

## Recomendaciones

- Instalen Git antes de la clase: [git-scm.com](https://git-scm.com/)
- Glosario de comandos: [Atlassian — Glosario de Git](https://www.atlassian.com/es/git/glossary)
- Libro completo y gratuito en español: [Pro Git](https://git-scm.com/book/es/v2)
- Hagan `git pull` **antes** de empezar a trabajar cada vez. La mayoría de los conflictos se evitan así.
- Un commit por cambio conceptual. Si el mensaje necesita la palabra "y", probablemente sean dos commits.
- El historial del repositorio es parte de la entrega. Se evalúa **cómo trabajaron**, no solo qué entregaron.
- Provoquen un conflicto a propósito y resuélvanlo. Es mejor aprender a resolverlo en un ejercicio que en un proyecto real.
