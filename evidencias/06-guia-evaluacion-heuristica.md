# Guía para la evaluación heurística individual · Prototipo CaféU

**Issue:** #6 · **Responsables:** los 4 integrantes, **cada uno por separado**
**Prototipo:** https://false-wired-67481015.figma.site (o [`prototipos/prototipo.html`](../prototipos/prototipo.html))
**Tiempo estimado:** 15 minutos

## Reglas
1. Hazlo **solo**. No mires las respuestas de tus compañeros hasta que todos terminen: la evaluación heurística vale porque cada evaluador revisa de forma independiente.
2. Para cada pregunta, **haz la prueba en el prototipo** (no respondas de memoria).
3. Responde **Sí** o **No** y, si encuentras un problema, escribe en una línea qué viste y su severidad.
4. Envía tus respuestas para pasarlas a `resultados/heuristica-<tu-nombre>.md` y súbelas **desde tu propia cuenta**.

## Severidad (solo si hay problema)
| Valor | Significa |
|---|---|
| 1 · Cosmético | Se ve mal o raro, pero no molesta para hacer la tarea |
| 2 · Menor | Molesta o hace dudar, pero el usuario lo resuelve solo |
| 3 · Mayor | Provoca errores o demoras importantes |
| 4 · Crítico | Impide terminar la tarea |

## Las 21 preguntas

| # | Heurística | Prueba esto en CaféU | Pregunta |
|---|---|---|---|
| 1 | 1 · Visibilidad del estado | Agrega un producto desde su detalle | ¿Ves claramente que el producto se agregó? |
| 2 | 1 · Visibilidad del estado | Mira el botón "Mi pedido" mientras agregas | ¿Muestra siempre cuántos productos llevas? |
| 3 | 1 · Visibilidad del estado | En Menú, toca el filtro "Comida" | ¿Queda claro qué filtro está activo y cuántos productos se muestran? |
| 4 | 1 · Visibilidad del estado | Confirma un pedido | ¿Queda claro que el pedido se envió? |
| 5 | 2 · Mundo real | Recorre el menú y el detalle | ¿Los nombres, precios y botones se entienden sin explicación? |
| 6 | 2 · Mundo real | Lee el horario en Inicio | ¿Cualquier persona entiende "7:00 – 19:00"? |
| 7 | 3 · Control y libertad | Agrega algo y navega entre Inicio, Menú y Mi pedido | ¿Puedes volver atrás sin perder tu pedido? |
| 8 | 3 · Control y libertad | En Mi pedido, toca "Quitar" | Si lo quitaste por error, ¿puedes deshacerlo? |
| 9 | 3 · Control y libertad | Confirma un pedido | Después de confirmar, ¿puedes cancelarlo o modificarlo? |
| 10 | 4 · Consistencia | Compara los botones de volver de cada pantalla | ¿Se ven y funcionan de la misma forma? |
| 11 | 4 · Consistencia | Compara los botones principales | ¿Tienen el mismo estilo en todas las pantallas? |
| 12 | 5 · Prevención de errores | En Mi pedido, toca "Quitar" | ¿Pide confirmación antes de borrar? |
| 13 | 5 · Prevención de errores | Toca "Confirmar pedido" | ¿Te pide revisar o confirmar antes de enviarlo? |
| 14 | 5 · Prevención de errores | Con el pedido vacío, ve a Mi pedido | ¿Se puede confirmar un pedido vacío? |
| 15 | 6 · Reconocer antes que recordar | En la lista del Menú | ¿Puedes agregar un producto sin entrar a su detalle? |
| 16 | 6 · Reconocer antes que recordar | En el detalle de un producto | ¿El selector de cantidad (− / +) se ve fácilmente? |
| 17 | 7 · Flexibilidad y eficiencia | En el buscador escribe **sanduche** (sin tilde) | ¿Encuentra el sánduche? |
| 18 | 7 · Flexibilidad y eficiencia | Busca atajos | ¿Hay formas rápidas de llegar a lo que buscas (filtros, buscador, "Ver pedido")? |
| 19 | 8 · Diseño estético y minimalista | Mira todas las pantallas | ¿Hay textos demasiado pequeños o información que sobra? |
| 20 | 9 · Recuperarse de errores | Busca **pizza** | ¿El mensaje explica qué pasó y qué hacer? |
| 21 | 10 · Ayuda y documentación | Revisa Inicio, Mi pedido y la confirmación | ¿Se explica cómo y dónde se paga y se recoge el pedido? |

## Formato para enviar las respuestas

```
Evaluador: (tu nombre)
Fecha:
Dispositivo y navegador:

1: Sí / No — (si hay problema: qué viste) — severidad: _
2: ...
...
21: ...

Otros problemas que encontraste (fuera de las preguntas):
```

## Después
Cuando los cuatro terminen, se comparan las listas: los problemas que encontró más de un evaluador, y los que además aparecieron en el pilotaje ([`resultados/resumen-pilotaje.md`](../resultados/resumen-pilotaje.md)), son la evidencia más fuerte para el G6.
