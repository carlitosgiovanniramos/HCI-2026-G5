# HCI-2026-G5 · Evaluación y validación de la usabilidad del Usability Test Dashboard 2.0

**Asignatura:** Interacción Persona-Ordenador. Universidad Técnica de Ambato (UTA), Ecuador
**Carrera / nivel:** Software, quinto nivel, paralelo 5A
**Tema:** G5 · APE 6, Evaluación y validación (Fases 1 y 2: planificación y pilotaje)
**Grupo:** 5
**Docente:** Ing. José Rubén Caiza Caizabuano
**Periodo académico:** Julio 2026 – Diciembre 2026
**Aplicación evaluada:** [Usability Test Dashboard 2.0](https://hci-proyecto-hazel.vercel.app/)

> **Pregunta inicial para la clase:** ¿Una interfaz que funciona técnicamente puede ser una mala interfaz?

---

## Problema

El Usability Test Dashboard 2.0 es la aplicación web de nuestro proyecto para gestionar pruebas de usabilidad: crear una prueba con sus tareas, llegar a la guía de moderación, registrar observaciones con apoyo de IA, completar la síntesis, generar el Sprint Backlog y consultar el tablero SCRUM y la comparación Antes/Después.

El Dashboard 2.0 pasó las pruebas técnicas del propio equipo: carga, guarda y procesa información sin fallos. Pero que funcione no garantiza que un evaluador nuevo pueda usarlo con eficacia, eficiencia y satisfacción. Quienes lo construimos conocemos el flujo de memoria, así que no podemos juzgar su claridad. Sin evidencia de uso, cualquier mejora descansaría en opiniones y no en datos observables.

**Pregunta de evaluación:** ¿En qué medida el Usability Test Dashboard 2.0 permite a un evaluador nuevo completar sus tareas principales con eficacia, eficiencia y satisfacción, y qué problemas lo impiden?

## Objetivo

### Objetivo general

Evaluar la usabilidad del Dashboard 2.0 con evaluadores nuevos (estudiantes de Software), combinando la evaluación heurística de Nielsen con una prueba de usabilidad con usuarios, para identificar los problemas, priorizarlos por severidad y convertirlos en un backlog de mejoras.

### Objetivos específicos

1. Planificar la evaluación (Fase 1): contexto, objetivos, participantes, tareas, métricas, ética y registro.
2. Pilotear las tareas con usuarios (Fase 2) y ajustar el plan según lo observado.
3. Medir la eficacia (tasa de éxito), la eficiencia (tiempo en tarea y errores) y la satisfacción (cuestionario SUS).
4. Inspeccionar la interfaz con las 10 heurísticas de Nielsen y contrastar sus hallazgos con los de la prueba con usuarios (triangulación).
5. Clasificar los problemas por severidad (cosmético, menor, mayor, crítico) y registrarlos como Issues en GitHub.

## Alcance de este grupo dentro del APE 6

| Fase | Contenido | Responsable |
|---|---|---|
| 1. Planificación | Contexto, objetivos, participantes, tareas, métricas, ética, registro | **G5 (este repositorio)** |
| 2. Pilotaje | Prueba de las tareas, hoja de observación, ajustes | **G5 (este repositorio)** |
| 3-4. Análisis y cierre | Aplicación y comparación de métodos, priorización, criterios técnicos | G6 |

## Conceptos HCI utilizados

| Concepto | Uso en este proyecto |
|---|---|
| Usabilidad (ISO 9241-11:2018) | Marco de referencia: eficacia, eficiencia y satisfacción en un contexto de uso específico. |
| Verificación vs. validación | Distinguir entre "el sistema funciona" y "el sistema sirve a sus usuarios" (pregunta inicial). |
| Evaluación formativa | El propósito es encontrar problemas para mejorar, no certificar la aplicación. |
| Métodos analíticos vs. empíricos | Inspección por evaluadores (heurística) frente a observación de usuarios reales (prueba). |
| Heurísticas de Nielsen | Criterios para la inspección experta. |
| Prueba de usabilidad / think-aloud | Observación de usuarios que realizan tareas hablando en voz alta, con roles definidos. |
| Métricas de usabilidad | Tasa de éxito, tiempo en tarea, errores y SUS. |
| Severidad | Priorización por frecuencia, impacto y persistencia. |
| Triangulación | Contraste entre métodos para fortalecer la evidencia de cada hallazgo. |

El desarrollo teórico está en [docs/investigacion.md](docs/investigacion.md).

## Procedimiento

### 1. Definición del alcance

- **Participantes:** evaluadores nuevos, estudiantes de Software que no participaron en el desarrollo del Dashboard. Se anonimizan como P1, P2, P3...
- **Entorno:** [COMPLETAR: equipo, navegador y resolución usados]. Acceso con el botón "Entrar como evaluador de demostración".
- **Tareas** (hoja de registro por tarea: éxito, tiempo, errores, observaciones):

| ID | Tarea | Meta | Se usa en |
|---|---|---|---|
| T1 | Entrar con el acceso de demostración y leer la tasa de éxito de la prueba "Portal Académico" | 60 s | Demo y clase |
| T2 | Crear la prueba "Sistema de biblioteca" con una tarea y llegar a la guía de moderación | 4 min | Piloto |
| T3 | Registrar una observación y aplicar la sugerencia de la IA | 3 min | Piloto |
| T4 | Completar la síntesis, finalizar la prueba y generar el Sprint Backlog | 3 min | Piloto |
| T5 | En el Sprint 4 del tablero SCRUM, contar las tareas en "Terminado" y decir quién tiene el "Generador de informe formal PDF" | 3 min | Demo y clase |
| T6 | Consultar cuánto mejoró la tasa de éxito en Antes/Después | 60 s | Clase |

- **Reglas fijadas antes de la prueba:**
  - *Éxito:* **Sí** (sin ayuda), **Con ayuda** (tras una pista) o **No** (no la completa o la abandona). Solo "Sí" cuenta como éxito.
  - *Error:* acción que no acerca al resultado esperado. **Crítico** si impide completar la tarea; **no crítico** si el usuario se recupera solo.

### 2. Evaluación heurística

Cada evaluador inspecciona el Dashboard por separado con las 10 heurísticas de Nielsen; después se consolidan los hallazgos y se asigna la severidad. Número de evaluadores: [COMPLETAR].

### 3. Prueba de usabilidad con usuarios

- **Participantes:** [COMPLETAR: número].
- **Ética:** consentimiento informado y participación voluntaria; se evalúa la aplicación, no a la persona; datos anonimizados (P1, P2...); sin nombres ni firmas en GitHub.
- **Métricas:** tasa de éxito, tiempo en tarea, errores y SUS (al final de las tareas).
- **Roles del laboratorio:**

| Rol | Responsabilidad | Integrante |
|---|---|---|
| Moderador | Presenta las tareas y conduce la sesión sin guiar al usuario. | Carlos Ramos |
| Usuario | Realiza las tareas en el Dashboard hablando en voz alta. | Henry Lagua |
| Registro de métricas | Cronometra y anota éxito, tiempo y errores de cada tarea. | Melany Cevallos |
| Observador | Anota dudas, comentarios y puntos de fricción. | Allison Cobos |

Regla del moderador: no ayudar ni sugerir dónde hacer clic.

### 4. Análisis y priorización

Consolidar los hallazgos de ambos métodos, asignar la severidad (1 cosmético, 2 menor, 3 mayor, 4 crítico) y relacionar cada hallazgo con su evidencia. Esta fase se completa junto con el G6.

### 5. Backlog de mejoras

Los hallazgos priorizados se registran como Issues de GitHub: [COMPLETAR: enlace a Issues].

## Herramientas

| Herramienta | Propósito |
|---|---|
| Usability Test Dashboard 2.0 (Vercel) | Aplicación evaluada. |
| GitHub (repositorio e Issues) | Documentación del proyecto y backlog de mejoras. |
| Markdown | Redacción de la documentación. |
| Cronómetro [COMPLETAR: cuál] | Medición del tiempo en tarea. |
| Cuestionario SUS [COMPLETAR: formato y versión en español] | Medición de la satisfacción percibida. |
| OneNote | Hoja de registro por tarea durante la clase. |
| Hoja de cálculo [COMPLETAR] | Cálculo de métricas y del puntaje SUS. |
| Grabación de pantalla [COMPLETAR, solo con consentimiento] | Evidencia de las sesiones. |

## Estructura del repositorio

```
HCI-2026-G5/
├── README.md
├── docs/
│   ├── investigacion.md   # Marco teórico y métodos
│   ├── preguntas.md       # Pregunta inicial, preguntas del QA/UX retador y debate
│   └── conclusiones.md    # Conclusiones del laboratorio
├── prototipos/
├── evidencias/            # Plan, consentimiento (anonimizado), tareas, hoja de observación
├── src/
└── resultados/            # Tiempos, errores, capturas del pilotaje
```

## Resultados

> Pendiente: se completan después del pilotaje (Fase 2). No se incluyen datos hasta tener evidencia real.

### Evaluación heurística
[COMPLETAR]

### Prueba de usabilidad (pilotaje T2, T3 y T4)
- Tasa de éxito: [COMPLETAR]
- Tiempo en tarea: [COMPLETAR]
- Errores: [COMPLETAR]
- SUS: [COMPLETAR]

### Hallazgos priorizados por severidad
[COMPLETAR]

### Backlog de mejoras
[COMPLETAR: enlace a Issues]

## Integrantes

| Integrante | Rol en el laboratorio | Aporte al repositorio |
|---|---|---|
| Carlos Ramos | Moderador | [COMPLETAR] |
| Henry Lagua | Usuario | [COMPLETAR] |
| Melany Cevallos | Registro de métricas | [COMPLETAR] |
| Allison Cobos | Observador | [COMPLETAR] |

Los roles rotan durante la sesión para obtener más datos.

## Conclusiones

[COMPLETAR después del pilotaje]

El desarrollo completo estará en [docs/conclusiones.md](docs/conclusiones.md).
