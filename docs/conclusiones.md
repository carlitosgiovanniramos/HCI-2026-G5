# Conclusiones · APE 6, Fases 1 y 2 · Prototipo CaféU

Basadas en el [plan de evaluación](../evidencias/01-plan-de-evaluacion.md), el [resumen del pilotaje](../resultados/resumen-pilotaje.md) (6 participantes en dos rondas) y la [evaluación heurística consolidada](../resultados/heuristica-consolidado.md) (4 evaluadores).

## 1. Respuesta a la pregunta inicial
¿Una interfaz que funciona técnicamente puede ser una mala interfaz?

**Sí, y CaféU lo demuestra.** El aviso "Producto agregado al pedido" existe en el código y se ejecuta durante 2,2 segundos cada vez que se agrega un producto: el prototipo **pasa la verificación**. Sin embargo, **ninguno de los 6 participantes lo percibió**, porque al terminar la animación el aviso queda desplazado y cortado en el borde derecho de la pantalla: el prototipo **falla en la validación**. El defecto solo se descubrió al observar usuarios reales; las pruebas técnicas del equipo no lo habrían detectado.

## 2. Respuesta a la pregunta de evaluación
¿En qué medida el prototipo CaféU permite a un estudiante nuevo armar, modificar y confirmar un pedido con eficacia, eficiencia y satisfacción, y qué problemas lo impiden?

Con estudiantes universitarios del perfil (ronda 2: P4, P5 y P6):

| Dimensión (ISO 9241-11) | Resultado | Lectura |
|---|---|---|
| Eficacia | 18 de 18 tareas completadas sin ayuda (100 %) | Alta |
| Eficiencia | Medianas de 5 a 23 s por tarea, todas muy por debajo de la meta; 1 error no crítico | Alta |
| Satisfacción | SUS medio de 90,8 (90,0 · 95,0 · 87,5), sobre la referencia de 68 | Alta |

CaféU permite completar el flujo de pedido con eficacia, eficiencia y satisfacción altas para su público. Lo que lo impide o lo dificulta no es completar las tareas, sino **saber qué pasó**: la principal debilidad es la **visibilidad del estado del sistema** (heurística 1), seguida del selector de cantidad poco visible.

Con usuarios fuera del perfil (ronda 1), el rendimiento bajó: P1, mayor de 50 años y con poca experiencia con aplicaciones, concentró 6 de los 7 errores, los tiempos sobre la meta y el único SUS bajo (50,0). Indica que la usabilidad de CaféU depende de la experiencia previa del usuario.

## 3. Principales hallazgos

| N.º | Hallazgo | Evidencia | Heurística |
|---|---|---|---|
| 1 | No se percibe la confirmación al agregar un producto (el aviso queda cortado a la derecha) | 4/4 evaluadores · 6/6 usuarios · causa verificada en el código | 1 · Visibilidad del estado |
| 2 | El selector de cantidad (−/+) se nota poco; se agrega el producto dos veces en lugar de usar "+" | 3/4 evaluadores · 3/6 usuarios | 6 · Reconocer antes que recordar |
| 3 | "Quitar" borra sin confirmar y sin opción de deshacer | 4/4 evaluadores · 0/6 usuarios | 3 · Control y libertad · 5 · Prevención de errores |
| 4 | El buscador no encuentra palabras sin tilde ("sanduche") | 4/4 evaluadores · 0/6 usuarios (nadie usó el buscador) | 7 · Flexibilidad |
| 5 | Textos pequeños y horario en formato de 24 horas | 4/4 y 3/4 evaluadores · 2/6 usuarios (fuera del perfil) | 2 · Mundo real · 8 · Diseño |
| 6 | Botones para volver al menú con nombres y posiciones distintas | 4/4 evaluadores · 0/6 usuarios | 4 · Consistencia |
| 7 | No se explica dónde está la cafetería, cuánto tarda el pedido ni cómo se paga | 4/4 evaluadores · 0/6 usuarios | 10 · Ayuda |

**Lo que funciona bien:** la pantalla de confirmación con el número de pedido grande, los filtros Comida/Bebidas, el flujo corto, los precios siempre visibles, la navegación inferior y el mensaje de búsqueda sin resultados.

## 4. Comparación entre métodos

### 4.1 Hallazgos detectados por ambos métodos
- **Sin confirmación visible al agregar** (4/4 evaluadores y 6/6 usuarios): la evidencia más fuerte del estudio.
- **Selector de cantidad poco visible** (3/4 y 3/6).
- **Texto pequeño y horario en 24 horas** (4/4 y 2/6, aunque solo en usuarios fuera del perfil).
- **"7 productos" confunde al contar una categoría** (1/4 y 2/6).

### 4.2 Hallazgos detectados solo en la evaluación heurística
- "Quitar" sin confirmación ni deshacer.
- Buscador sensible a las tildes.
- Botones para volver con nombres distintos.
- Falta de información sobre pago, retiro y tiempo de preparación.

Son **problemas potenciales**: existen en el prototipo, pero las tareas no llevaron a los usuarios a sufrirlos. No significa que no importen: el fallo de las tildes no apareció porque **nadie usó el buscador**, no porque funcione bien.

### 4.3 Hallazgos detectados solo en la prueba con usuarios
- Duda con el nombre "Café americano" ("¿es el negrito?").
- En la lista del menú se busca un botón "Agregar" que no existe (P1).
- Duda entre "Quitar" y los botones de cantidad (P1).

### 4.4 Qué aportó cada método
La heurística **amplió la cobertura** a partes que las tareas no recorren; la prueba con usuarios **confirmó el impacto real** y reveló la causa del problema principal. Además, al contrastar las respuestas de los evaluadores con el código se encontraron dos diferencias (el botón de confirmar sí se desactiva con el pedido vacío, y "Agregar al pedido" no tiene el color de los demás botones principales), que muestran el **efecto evaluador** y justifican usar varios evaluadores.

## 5. Priorización y backlog de mejoras
La severidad final y el backlog priorizado corresponden al **Grupo 6** (Fases 3 y 4), con estos datos. Como propuesta de entrada para ese análisis:

1. **Aviso de confirmación** (confirmado por ambos métodos, 6/6): **ya corregido** en `prototipos/prototipo.html` (Issue #10); falta aplicarlo en Figma Make.
2. **Selector de cantidad** (ambos métodos, 3/6).
3. **"Quitar" sin confirmar ni deshacer** y **buscador sin tildes** (solo heurística, 4/4): verificar primero con una tarea que obligue a usarlos.

## 6. Limitaciones del estudio
1. **Muestra pequeña:** 3 participantes por ronda; las métricas son descriptivas, no generalizables.
2. **Ronda 1 fuera del perfil:** incluyó a una persona mayor de 50 años, una persona sin perfil registrado y un menor de 12 años (con autorización de su madre o padre); se reporta aparte.
3. **Efecto techo:** en la ronda 2 todas las tareas se completaron muy por debajo de la meta; las metas (60 a 90 s) resultaron holgadas para usuarios con experiencia.
4. **Pensamiento en voz alta:** alarga los tiempos por igual en todas las sesiones.
5. **Evaluadores no expertos:** los cuatro evaluadores heurísticos son estudiantes; se compensó con varios evaluadores y con la triangulación.
6. **Prototipo:** no hay pago ni retiro reales, y la versión evaluada es la publicada en Figma Make.

## 7. Retroalimentación del grupo QA/UX
En esta exposición el G5 actúa como grupo QA/UX de G1 y G4, con 2 preguntas técnicas y 1 objeción para cada grupo ([preguntas.md](preguntas.md), sección 5). Lo que respondan y lo que se pregunte al G5 se registra el 17/11/2026 en la sección 6 de [preguntas.md](preguntas.md).

## 8. Lecciones aprendidas
1. **Validar el objeto antes de los datos.** Empezamos evaluando el Usability Test Dashboard 2.0 y corregimos a CaféU al revisar la cadena de los APE (Issue #9). Evaluar el objeto equivocado invalida todo lo demás.
2. **El criterio de inclusión se aplica antes de la sesión, no después.** La ronda 1 tuvo que repetirse porque no se preguntó el perfil al inicio.
3. **Un tiempo estimado no es un dato.** El ensayo con tiempos estimados no se contó; solo valen los tiempos tomados en vivo.
4. **La pista debe ser única y textual.** Una pista distinta orienta al usuario y cambia el resultado de la tarea.
5. **Un problema no observado no es un problema descartado.** El buscador sin tildes demuestra por qué se necesitan dos métodos.

## 9. Criterios técnicos para mejorar los métodos
- Definir por escrito, antes de probar, el éxito, el error, la pista, el tiempo máximo y el reinicio de cada tarea.
- Incluir al menos una tarea por cada función crítica (por ejemplo, una que obligue a usar el buscador) para que la prueba con usuarios cubra lo que la heurística prevé.
- Designar una sola persona para el cronómetro y otra para las frases textuales.
- Pedir a cada evaluador heurístico una severidad numérica (1 a 4) por problema, para facilitar la consolidación.
- Contrastar los hallazgos con el prototipo o el código antes de reportarlos, para separar los problemas reales de los errores del evaluador.

## 10. Trabajo futuro
1. Aplicar la corrección del aviso en Figma Make y **repetir la prueba** para comprobar que el problema se resolvió (nueva validación).
2. Ampliar la muestra a **5 o más estudiantes** y agregar una tarea con el buscador.
3. Que el **Grupo 6** asigne la severidad final, construya el backlog priorizado y compare los métodos en las Fases 3 y 4.
4. Considerar a usuarios con poca experiencia (como P1) si CaféU se abre a docentes y personal de la universidad.
