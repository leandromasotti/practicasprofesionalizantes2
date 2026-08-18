# Planificación de la cursada

Esta carpeta contiene la planificación concreta de cada ciclo lectivo.

---

## Cómo está organizada la documentación

La cátedra separa deliberadamente dos cosas que suelen mezclarse:

| Documento | Responde a | Estabilidad |
|---|---|---|
| [**Programa**](../programa/) | **Qué** se enseña: unidades, contenidos, bibliografía, evaluación | Estable entre ciclos |
| **Planificación anual** (esta carpeta) | **Cuándo** se enseña: calendario, feriados, hitos, entregas | Se rehace cada año |

El motivo es práctico: los contenidos de la materia cambian poco de un año a otro, pero el calendario cambia siempre —arranca otro día, los feriados caen distinto, el receso se corre—.

Al mantenerlos separados, planificar un ciclo nuevo no obliga a reescribir el programa, y actualizar el programa no invalida los calendarios anteriores.

---

## Ciclos lectivos

| Ciclo | Planificación | Estado |
|---|---|---|
| 2026 | [2026.md](2026.md) | En curso |

---

## Cómo planificar un ciclo nuevo

Procedimiento a seguir al comenzar cada año.

### 1. Obtener las fechas institucionales

Se necesitan cinco datos:

- fecha de inicio de clases;
- fecha de finalización;
- días de la semana en que se dicta;
- período de receso invernal;
- período de mesas de examen.

### 2. Verificar los feriados

Los feriados nacionales que suelen caer en día de clase:

| Feriado | Fecha | Tipo |
|---|---|---|
| Memoria, Verdad y Justicia | 24/03 | Fijo |
| Malvinas | 02/04 | Fijo |
| Día del Trabajador | 01/05 | Fijo |
| Revolución de Mayo | 25/05 | Fijo |
| Paso a la Inmortalidad de Belgrano | 20/06 | Fijo |
| Día de la Independencia | 09/07 | Fijo |
| Paso a la Inmortalidad de San Martín | 3.er lunes de agosto | Trasladable |
| Respeto a la Diversidad Cultural | 12/10, se traslada a lunes | Trasladable |
| Soberanía Nacional | 4.º lunes de noviembre | Trasladable |

A esto hay que sumarle los asuetos institucionales y los puentes turísticos, que se definen por decreto cada año.

### 3. Cerrar el presupuesto horario — **antes** de asignar contenidos

La resolución fija **128 horas reloj** para el módulo. No es una referencia: es una obligación que el cronograma debe cerrar.

Este paso va **antes** de repartir las unidades, no después. Si se asignan contenidos primero y las horas se verifican al final, el desvío aparece cuando ya no hay margen para corregirlo.

Dos reglas que la experiencia de 2026 dejó asentadas:

- **Se cuentan encuentros, no semanas.** Cada feriado en día de clase elimina un encuentro y sus horas. Contar semanas y multiplicar por dos sobrestima la carga.
- **La duración del encuentro se toma del horario institucional**, no se estima. Hay que saber si se expresa en horas reloj o cátedra, y de cuántos minutos.

El siguiente comando calcula el presupuesto completo:

```bash
python - <<'PY'
import datetime as dt
from fractions import Fraction as F

# ── Parámetros del ciclo ──────────────────────────────────────────
INICIO   = dt.date(2026, 3, 30)    # ← ajustar
FIN      = dt.date(2026, 11, 20)   # ← ajustar
DIAS     = [0, 1]                  # 0=lunes … 6=domingo
OBJETIVO = F(128)                  # horas reloj que fija la resolución
DURACION = F(2)                    # horas reloj por encuentro. F(9,4) = 2 h 15 min

RECESOS = [                                              # ← ajustar
    (dt.date(2026, 7, 20), dt.date(2026, 7, 31)),        # receso invernal
    (dt.date(2026, 8, 3),  dt.date(2026, 8, 14)),        # mesas de examen
]
FERIADOS = {                                             # ← ajustar
    dt.date(2026, 5, 25), dt.date(2026, 8, 17), dt.date(2026, 10, 12),
}
# ──────────────────────────────────────────────────────────────────

def en_receso(f): return any(a <= f <= b for a, b in RECESOS)
def hm(x):
    m = int(round(float(x) * 60)); return f"{m//60} h {m%60:02d} min"

sem = nom = efec = 0
cur = INICIO - dt.timedelta(days=INICIO.weekday())
while cur <= FIN:
    fechas = [cur + dt.timedelta(days=d) for d in DIAS]
    fechas = [f for f in fechas if INICIO <= f <= FIN and not en_receso(f)]
    if fechas:
        sem += 1
        marcas = []
        for f in fechas:
            nom += 1
            if f in FERIADOS:
                marcas.append(f.strftime('%d/%m') + ' FERIADO')
            else:
                efec += 1; marcas.append(f.strftime('%d/%m'))
        print(f"Semana {sem:2d}: " + "  ".join(marcas))
    cur += dt.timedelta(days=7)

total = DURACION * efec
desvio = total - OBJETIVO
print(f"\nSemanas de clase      : {sem}")
print(f"Encuentros nominales  : {nom}")
print(f"Encuentros efectivos  : {efec}   (perdidos por feriado: {nom - efec})")
print(f"\nA {hm(DURACION)} por encuentro  ->  {hm(total)} de {hm(OBJETIVO)}")
if desvio < 0:
    print(f"  DEFICIT de {hm(-desvio)}  ({float(-desvio/OBJETIVO)*100:.1f} %)")
    print(f"  Encuentros faltantes a esta duracion: {float(-desvio/DURACION):.1f}")
    print(f"  Duracion necesaria por encuentro    : {hm(OBJETIVO/efec)}")
elif desvio > 0:
    print(f"  EXCEDENTE de {hm(desvio)}")
else:
    print("  EXACTO")
PY
```

Si el resultado arroja déficit, hay que resolverlo antes de continuar. Los mecanismos disponibles, en orden de preferencia:

1. **Jornadas de práctica en la organización.** Es el mecanismo más consistente con el módulo: la resolución define entornos formativos en organizaciones reales, de modo que una jornada de relevamiento en terreno es carga horaria del espacio.
2. **Ajustar la duración del encuentro**, si el horario institucional lo permite.
3. **Recuperar los encuentros perdidos por feriado** con clases adicionales.

> No corresponde compensar con tutorías: esa cláusula de la resolución pertenece a Prácticas Profesionalizantes III, no a este módulo.

### 4. Asignar unidades a semanas

Partir de la carga en semanas que el [programa](../programa/) asigna a cada unidad y ajustarla a las semanas disponibles.

Si sobran semanas, ampliar el tiempo de taller sobre el proyecto integrador.
Si faltan, aplicar el criterio de ajuste documentado en la planificación del ciclo.

### 5. Definir hitos y entregas

Cada unidad que habilita una entrega del proyecto integrador debe tener su fecha fijada desde el inicio del ciclo, no sobre la marcha.

### 6. Reservar margen

Asignar el 100 % de las semanas no deja lugar para imprevistos. Conviene dejar una semana libre por cuatrimestre o, como mínimo, dejar escrito de antemano qué se recorta si hay que recortar.

El margen tiene una implicancia horaria: una semana perdida son dos encuentros menos, y por lo tanto horas que salen del presupuesto. Si el ciclo cierra las 128 horas justo, cualquier suspensión de clases lo deja en falta. Conviene planificar con un **excedente de entre 2 y 4 horas**.

### 7. Registrar las horas durante el ciclo

Llevar el acumulado de horas efectivamente dictadas, no solo de contenidos. Una clase suspendida por paro o por acto institucional descuenta horas del presupuesto y hay que verlo cuando ocurre, no en noviembre.

### 8. Cerrar el ciclo

Al finalizar el año, completar el registro de desvíos, verificar el total de horas dictadas contra las 128 y anotar en el programa qué conviene cambiar para el ciclo siguiente.

---

## Plantilla

Para iniciar un ciclo nuevo, copiar [`plantilla.md`](plantilla.md) como `AAAA.md` y completarlo.
