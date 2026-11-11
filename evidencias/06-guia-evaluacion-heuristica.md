# Guía para la evaluación heurística individual · Prototipo CaféU

**Issue:** #6 · **Responsables:** los 4 integrantes, **cada uno por separado**
**Prototipo:** https://false-wired-67481015.figma.site (o [`prototipos/prototipo.html`](../prototipos/prototipo.html))
**Tiempo estimado:** 10 minutos

## Reglas
1. Hazlo **solo**. No mires las respuestas de tus compañeros hasta que todos terminen: la evaluación heurística vale porque cada evaluador revisa de forma independiente.
2. Para cada pregunta, **haz la prueba en el prototipo** (no respondas de memoria).
3. Responde **Sí** o **No** y explica en una línea qué viste.
4. Las respuestas se pasan a `resultados/heuristica-<nombre>.md`.

## Las 10 preguntas (una por heurística de Nielsen)

| # | Heurística | Prueba esto en CaféU | Pregunta |
|---|---|---|---|
| 1 | 1 · Visibilidad del estado del sistema | Agrega un producto desde su detalle | ¿Ves claramente que el producto se agregó? |
| 2 | 2 · Coincidencia con el mundo real | Lee el horario en Inicio | ¿Cualquier persona entiende "7:00 – 19:00"? |
| 3 | 3 · Control y libertad del usuario | En Mi pedido, toca "Quitar" | Si lo quitaste por error, ¿puedes deshacerlo? |
| 4 | 4 · Consistencia y estándares | Compara los botones de volver de cada pantalla | ¿Se ven y funcionan de la misma forma? |
| 5 | 5 · Prevención de errores | En Mi pedido, toca "Quitar" | ¿Pide confirmación antes de borrar? |
| 6 | 6 · Reconocer antes que recordar | En el detalle de un producto | ¿El selector de cantidad (− / +) se ve fácilmente? |
| 7 | 7 · Flexibilidad y eficiencia de uso | En el buscador escribe **sanduche** (sin tilde) | ¿Encuentra el sánduche? |
| 8 | 8 · Diseño estético y minimalista | Mira todas las pantallas | ¿Hay textos demasiado pequeños o información que sobra? |
| 9 | 9 · Ayudar a recuperarse de errores | Busca **pizza** | ¿El mensaje explica qué pasó y qué hacer? |
| 10 | 10 · Ayuda y documentación | Revisa Inicio, Mi pedido y la confirmación | ¿Se explica cómo y dónde se paga y se recoge el pedido? |

## Formato para enviar las respuestas

```
Evaluador: (tu nombre)
Fecha:

1: Sí / No — qué viste
2: ...
...
10: ...
```

## Después
Se comparan las cuatro listas entre sí y con el pilotaje ([`resultados/resumen-pilotaje.md`](../resultados/resumen-pilotaje.md)). Un problema que encuentran varios evaluadores **y** que también aparece con usuarios tiene la evidencia más fuerte. La consolidación está en [`resultados/heuristica-consolidado.md`](../resultados/heuristica-consolidado.md).
