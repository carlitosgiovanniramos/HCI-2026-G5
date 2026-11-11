# Evaluación heurística consolidada y triangulación · Prototipo CaféU

**Fecha:** 10/11/2026 · **Evaluadores:** 4 integrantes del G5, por separado
[E1 Carlos Ramos](heuristica-carlos.md) · [E2 Henry Lagua](heuristica-henry.md) · [E3 Melany Cevallos](heuristica-melany.md) · [E4 Allison Cobos](heuristica-alison.md)
**Método:** 10 preguntas, una por heurística de Nielsen ([guía](../evidencias/06-guia-evaluacion-heuristica.md)), sobre la versión publicada antes de la corrección del Issue #10.

## 1. Problemas detectados por los evaluadores

| N.º | Problema | Heurística | Evaluadores que lo detectaron |
|---|---|---|---|
| HE-1 | Al agregar un producto no se percibe ninguna confirmación; solo cambia el contador | 1 · Visibilidad | **4/4** |
| HE-2 | "Quitar" borra el producto sin opción de deshacer | 3 · Control y libertad | **4/4** |
| HE-3 | Los botones para volver al menú tienen nombres y posiciones distintas ("Menú", "Seguir comprando", "Volver al menú") | 4 · Consistencia | **4/4** |
| HE-4 | "Quitar" no pide confirmación antes de borrar | 5 · Prevención de errores | **4/4** |
| HE-5 | El buscador no reconoce palabras sin tilde ("sanduche" no encuentra "Sánduche de queso") | 7 · Flexibilidad | **4/4** |
| HE-6 | No se explica dónde está la cafetería, cuánto tarda el pedido ni cómo se paga | 10 · Ayuda | **4/4** |
| HE-7 | Textos pequeños (etiquetas de categoría de 10 px, contador de 11 px, horario) | 8 · Diseño | **4/4** |
| HE-8 | El selector de cantidad (− / +) tiene poco énfasis o se percibe pequeño | 6 · Reconocer | **3/4** (E1, E2, E4) |
| HE-9 | El horario en formato de 24 horas ("19:00") puede confundir | 2 · Mundo real | **3/4** (E2, E3, E4; E1 dijo que debe pensarlo) |

**Lo que los evaluadores valoraron bien:** el mensaje de búsqueda sin resultados ("No encontramos productos" + "Limpiar búsqueda"), evaluado positivamente por 4/4 (heurística 9).

## 2. Triangulación con el pilotaje

Se cruza cada problema con lo observado en las seis sesiones del pilotaje ([resumen](resumen-pilotaje.md)). Ronda 2 = P4 a P6 (perfil del plan); ronda 1 = P1 a P3.

| Problema | Heurística (4 evaluadores) | Usuarios (6 participantes) | Clasificación |
|---|---|---|---|
| HE-1 · Sin confirmación al agregar | 4/4 | **6/6** (3/3 en la ronda 2) | **Confirmado por ambos métodos** · Corregido en `prototipos/prototipo.html` (Issue #10) |
| HE-8 · Selector de cantidad poco visible | 3/4 | **3/6** agregaron dos veces en lugar de usar "+" (P1, P3 y P4); P4: "el '+' se nota poco" | **Confirmado por ambos métodos** |
| HE-7 y HE-9 · Textos pequeños y horario de 24 h | 4/4 y 3/4 | **2/6** (P1: "la letra está un poquito chiquita"; P3: "Diecinueve... ah, las siete") · 0/3 en la ronda 2 | **Confirmado por ambos métodos**, solo en perfiles fuera del público objetivo |
| HE-2 y HE-4 · "Quitar" sin confirmación ni deshacer | 4/4 | 1/6 dudó entre "Quitar" y la cantidad (P1); nadie borró por error | **Solo heurística (potencial):** las tareas no provocaron el error |
| HE-5 · Buscador sensible a tildes | 4/4 | **0/6:** ningún participante usó el buscador, todos usaron los filtros | **Solo heurística (potencial):** el problema existe, pero las tareas no lo recorrieron |
| HE-3 · Botones de volver inconsistentes | 4/4 | 0/6 | **Solo heurística (potencial)** |
| HE-6 · Falta información de pago y retiro | 4/4 | 0/6 (las tareas no lo pedían) | **Solo heurística (potencial)** |
| "7 productos" confunde al contar una categoría | 1/4 (E3, en otra pregunta de la guía original) | **2/6** (P1 dijo 7; P5 lo comentó) | **Confirmado por ambos métodos** (débil en la heurística) |
| El nombre "Café americano" genera duda | 0/4 | 1/6 (P3) | **Solo usuarios** |

### Cómo leer la tabla
- **Confirmado por ambos métodos:** la evidencia más fuerte. Los evaluadores lo previeron y los usuarios lo sufrieron.
- **Solo heurística:** problema potencial. Existe en el prototipo, pero no afectó a los participantes en estas tareas. No se descarta: el buscador sin tildes no se observó porque **nadie lo usó**, no porque funcione bien.
- **Solo usuarios:** problema real que la inspección no anticipó.

## 3. Verificación contra el prototipo

Al contrastar las respuestas de la guía original (21 preguntas) con el código del prototipo se encontraron dos diferencias. Ilustran el **efecto evaluador**, que justifica usar varios evaluadores y contrastarlos con usuarios:

1. **Pedido vacío:** los evaluadores indicaron que "Confirmar pedido" se veía igual y debía desactivarse. En el prototipo el botón **sí está desactivado** (se muestra en gris y no responde). El problema válido es que **no explica por qué** está desactivado.
2. **Botón "Agregar al pedido":** se reportó como naranja y consistente con los demás botones principales. En el prototipo es **café oscuro**, mientras que "Ver menú" y "Confirmar pedido" son naranjas. Es una inconsistencia (heurística 4) que **ningún evaluador detectó**.

Estas dos preguntas quedaron fuera de la guía final de 10 preguntas.

## 4. Entrega al G6
Los problemas de las secciones 2 y 3 pasan al G6 (Fases 3 y 4) para asignar la severidad final (1 a 4) y construir el backlog priorizado. Los evaluadores no asignaron una severidad numérica individual, salvo E2 en HE-2 ("severidad media").
