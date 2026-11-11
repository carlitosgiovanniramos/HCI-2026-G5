# HCI-2026-G5 · Evaluación y validación de la usabilidad del prototipo CaféU

**Asignatura:** Interacción Persona-Ordenador. Universidad Técnica de Ambato (UTA), Ecuador
**Carrera / nivel:** Software, quinto nivel, paralelo 5A
**Tema:** G5 · APE 6, Evaluación y validación (Fases 1 y 2: planificación y pilotaje)
**Grupo:** 5
**Docente:** Ing. José Rubén Caiza Caizabuano
**Periodo académico:** Julio 2026 – Diciembre 2026
**Prototipo evaluado:** [CaféU](https://false-wired-67481015.figma.site) · copia local en [`prototipos/prototipo.html`](prototipos/prototipo.html)

> **Pregunta inicial para la clase:** ¿Una interfaz que funciona técnicamente puede ser una mala interfaz?

---

## Problema

**CaféU** es el prototipo de aplicación web móvil del grupo para que los estudiantes **pidan en la cafetería universitaria antes de llegar** y recojan su pedido sin hacer fila. Se construyó en el APE 4 (prototipo en Figma) y es la base del APE 5 (paso a HTML).

El prototipo funciona: navega entre pantallas, calcula los totales y genera un número de pedido. Pero que funcione no garantiza que un estudiante que no lo diseñó pueda usarlo con eficacia, eficiencia y satisfacción. Quienes lo diseñamos conocemos el flujo de memoria, así que no podemos juzgar su claridad. Sin evidencia de uso, cualquier mejora descansaría en opiniones y no en datos observables.

**Pregunta de evaluación:** ¿En qué medida el prototipo CaféU permite a un estudiante nuevo armar, modificar y confirmar un pedido con eficacia, eficiencia y satisfacción, y qué problemas lo impiden?

### Por qué se evalúa CaféU

La matriz de la asignatura encadena los APE sobre el mismo proyecto:

| APE | Qué se hizo |
|---|---|
| APE 4 | Prototipo de CaféU (wireframes y prototipo navegable en Figma) |
| APE 5 | Paso del prototipo a una interfaz web (HTML/CSS) |
| **APE 6** | **Evaluación del prototipo con usuarios** (este repositorio) |

El cambio desde el Usability Test Dashboard 2.0 está documentado en el Issue #9.

## Objetivo

### Objetivo general

Planificar y pilotear una evaluación de usabilidad del prototipo CaféU con estudiantes que no participaron en su diseño, combinando la evaluación heurística de Nielsen con una prueba de usabilidad con usuarios.

### Objetivos específicos

1. Planificar la evaluación (Fase 1): contexto, objetivos, participantes, tareas, métricas, ética y registro.
2. Pilotear las tareas con usuarios (Fase 2) y ajustar el plan según lo observado.
3. Medir la eficacia (tasa de éxito), la eficiencia (tiempo en tarea y errores) y la satisfacción (cuestionario SUS).
4. Inspeccionar la interfaz con las 10 heurísticas de Nielsen y entregar al G6 los hallazgos preliminares para su triangulación y priorización.

## Alcance de este grupo dentro del APE 6

| Fase | Contenido | Responsable |
|---|---|---|
| 1. Planificación | Contexto, objetivos, participantes, tareas, métricas, ética, registro | **G5 (este repositorio)** |
| 2. Pilotaje | Prueba de las tareas, hoja de observación, ajustes | **G5 (este repositorio)** |
| 3-4. Análisis y cierre | Aplicación y comparación de métodos, severidad, backlog, criterios técnicos | G6 |

## Conceptos HCI utilizados

| Concepto | Uso en este proyecto |
|---|---|
| Usabilidad (ISO 9241-11:2018) | Marco de referencia: eficacia, eficiencia y satisfacción en un contexto de uso específico. |
| Verificación vs. validación | Distinguir entre "el prototipo funciona" y "el prototipo sirve a sus usuarios" (pregunta inicial). |
| Evaluación formativa | El propósito es encontrar problemas para mejorar, no certificar el prototipo. |
| Métodos analíticos vs. empíricos | Inspección por evaluadores (heurística) frente a observación de usuarios reales (prueba). |
| Heurísticas de Nielsen | Criterios para la inspección experta. |
| Prueba de usabilidad / think-aloud | Observación de usuarios que realizan tareas hablando en voz alta, con roles definidos. |
| Pilotaje | Ensayo del protocolo con participantes reales para ajustar tareas, tiempos e instrumentos antes de la evaluación completa. |
| Métricas de usabilidad | Tasa de éxito, tiempo en tarea, errores y SUS. |
| Severidad | Priorización por frecuencia, impacto y persistencia. |
| Triangulación | Contraste entre métodos para fortalecer la evidencia de cada hallazgo. |

El desarrollo teórico está en [docs/investigacion.md](docs/investigacion.md).

## Procedimiento

Los documentos completos están en [`evidencias/`](evidencias/):

| N.º | Documento | Responsable |
|---|---|---|
| 01 | [Plan de evaluación](evidencias/01-plan-de-evaluacion.md) | Carlos Ramos |
| 02 | [Consentimiento informado](evidencias/02-consentimiento-informado.md) | Allison Cobos |
| 03 | [Tareas y respuestas correctas](evidencias/03-tareas.md) | Henry Lagua |
| 04 | [Hoja de observación y SUS](evidencias/04-hoja-de-observacion.md) | Melany Cevallos |
| 05 | [Guía del día del pilotaje](evidencias/05-guia-del-pilotaje.md) | Carlos Ramos |

### 1. Definición del alcance

- **Participantes del pilotaje:** 3 estudiantes (P1, P2 y P3) que no diseñaron CaféU ni participaron en la prueba del APE 4.
- **Entorno:** laptop Lenovo LOQ con Windows 11 y Chrome 157 (1536 × 864 px); el prototipo se muestra en un marco de celular de 390 × 844 px.
- **Tareas:**

| ID | Tarea | Meta | Se usa en |
|---|---|---|---|
| T1 | Decir en qué horario atiende la cafetería | 60 s | Pilotaje y exposición |
| T2 | Agregar un sánduche de queso al pedido | 60 s | Pilotaje |
| T3 | Agregar también dos cafés americanos | 60 s | Pilotaje |
| T4 | Quitar el sánduche, confirmar el pedido y decir el número de pedido | 90 s | Pilotaje |
| T5 | Decir cuántos productos de comida ofrece la cafetería | 60 s | Pilotaje y exposición |
| T6 | Decir cuánto se pagaría por 3 croissants | 90 s | Pilotaje y exposición |

- **Reglas fijadas antes de la prueba:**
  - *Éxito:* **Sí** (sin ayuda), **Con ayuda** (tras la pista) o **No** (no la completa, la abandona o supera el doble de la meta). Solo "Sí" cuenta como éxito.
  - *Error:* acción que no acerca al resultado esperado. **Crítico** si impide completar la tarea; **no crítico** si el usuario se recupera solo.

### 2. Evaluación heurística

Cada integrante inspecciona CaféU por separado con las 10 heurísticas de Nielsen (4 evaluadores, Issue #6). Los hallazgos se entregan al G6 para consolidarlos y asignar la severidad.

### 3. Prueba de usabilidad con usuarios (pilotaje)

- **Participantes:** 3 (P1, P2 y P3).
- **Ética:** consentimiento verbal y voluntario; se evalúa la aplicación, no a la persona; datos anonimizados; sin nombres, firmas, rostros ni voces en GitHub.
- **Métricas:** tasa de éxito, tiempo en tarea (mediana), errores y SUS al final.
- **Roles:**

| Rol | Pilotaje | Exposición (17/11) |
|---|---|---|
| Moderador | Carlos Ramos | Melany Cevallos |
| Usuario | Participantes externos (P1 a P6) | Allison Cobos (demostración) |
| Registro de métricas | Melany Cevallos | Carlos Ramos |
| Observador | Allison Cobos | Henry Lagua |
| Soporte técnico | Henry Lagua | — |

Regla del moderador: no ayudar ni sugerir dónde tocar.

### 4. Análisis, priorización y backlog

Lo realiza el G6 (Fases 3 y 4) a partir de los datos del pilotaje y de las evaluaciones heurísticas de este repositorio.

## Herramientas

| Herramienta | Propósito |
|---|---|
| Figma Make | Prototipo evaluado (CaféU) |
| Google Chrome 157 | Navegador de las sesiones |
| GitHub (repositorio e Issues) | Documentación, reparto de tareas y trazabilidad |
| Markdown | Redacción de la documentación |
| Cronómetro del celular | Medición del tiempo en tarea |
| Cuestionario SUS (Brooke, 1996; traducción del grupo) | Medición de la satisfacción percibida |
| OneNote o papel | Hoja de registro durante las sesiones |
| Xbox Game Bar de Windows | Grabación de pantalla, solo con consentimiento y sin subirla a GitHub |

## Entregables

| Entregable | Archivo |
|---|---|
| Informe del APE 6 (formato UTA) | [Word](docs/APE6_Informe_G5_CafeU.docx) · [PDF](docs/APE6_Informe_G5_CafeU.pdf) |
| Guía de réplica de la Fase 1 (planificación) para los demás grupos | [Word](docs/APE6_Guia_Fase1_Planificacion.docx) · [PDF](docs/APE6_Guia_Fase1_Planificacion.pdf) |
| Guía de réplica de la Fase 2 (pilotaje) para los demás grupos | [Word](docs/APE6_Guia_Fase2_Pilotaje.docx) · [PDF](docs/APE6_Guia_Fase2_Pilotaje.pdf) |
| Presentación de la exposición | [presentacion-G5-CafeU.pptx](docs/presentacion-G5-CafeU.pptx) |
| Guion de la exposición y del ensayo | [guion-exposicion.md](docs/guion-exposicion.md) |
| Preguntas del G5 para G1 y G4 | [preguntas.md](docs/preguntas.md), sección 5 |

## Estructura del repositorio

```
HCI-2026-G5/
├── README.md
├── docs/
│   ├── investigacion.md   # Marco teórico y métodos
│   ├── preguntas.md       # Pregunta inicial, preguntas del QA/UX retador y debate
│   └── conclusiones.md    # Conclusiones del laboratorio
├── prototipos/
│   └── prototipo.html     # Prototipo CaféU en un solo archivo
├── evidencias/            # Plan, consentimiento, tareas, hoja de observación y guía del pilotaje
├── src/
└── resultados/            # Datos del pilotaje (P1, P2 y P3) y evaluaciones heurísticas
```

## Resultados

> Pendiente: se completan después del pilotaje (Fase 2). No se incluyen datos hasta tener evidencia real.

### Prueba de usabilidad (pilotaje T1 a T6)
Dos rondas el 10/11/2026. Resumen completo en [resultados/resumen-pilotaje.md](resultados/resumen-pilotaje.md).

**Ronda 2 · principal** ([P4](resultados/P4.md), [P5](resultados/P5.md) y [P6](resultados/P6.md): estudiantes universitarios que no conocían CaféU):
- **Tasa de éxito:** 18 de 18 tareas (100 %), sin pistas.
- **Tiempo en tarea (mediana):** T1 5 s · T2 13 s · T3 19 s · T4 23 s · T5 9 s · T6 15 s.
- **Errores:** 0 críticos y 1 no crítico.
- **SUS:** 90,0 · 95,0 · 87,5 (media 90,8).

**Ronda 1 · inicial** ([P1](resultados/P1.md), [P2](resultados/P2.md) y [P3](resultados/P3.md): no cumplían el perfil): 17 de 18 tareas con éxito y SUS medio 79,2. Sirvió para ajustar el protocolo.

**Hallazgo principal:** 6 de 6 participantes no percibieron la confirmación al agregar un producto. El aviso existe, pero queda desplazado y cortado en el borde derecho de la pantalla.

### Evaluación heurística
Pendiente (Issue #6).

### Ajustes al protocolo
Pendiente (sección 12 del [plan](evidencias/01-plan-de-evaluacion.md)).

## Integrantes

| Integrante | GitHub | Rol en el laboratorio | Aporte al repositorio |
|---|---|---|---|
| Carlos Ramos | @carlitosgiovanniramos | Moderador (pilotaje) / registro de métricas (exposición) | Plan de evaluación, guía del pilotaje y prototipo |
| Henry Lagua | @Hlagua | Soporte técnico (pilotaje) / observador (exposición) | Tareas y respuestas correctas |
| Melany Cevallos | @SalyC15 | Registro de métricas (pilotaje) / moderadora (exposición) | Hoja de observación y SUS |
| Allison Cobos | @Itsuna18 | Observadora (pilotaje) / usuaria (exposición) | Consentimiento informado |

## Conclusiones

1. **Una interfaz que funciona puede ser una mala interfaz:** el aviso de confirmación de CaféU existe y se ejecuta, pero 6 de 6 usuarios no lo vieron porque queda cortado en el borde de la pantalla.
2. **CaféU es eficaz, eficiente y satisfactorio para su público** (18 de 18 tareas, SUS 90,8), pero su principal debilidad es la visibilidad del estado del sistema.
3. **Los dos métodos se complementan:** 4 problemas confirmados por ambos y 4 que solo vio la heurística, como el buscador sin tildes, que nadie usó en las pruebas.
4. **El pilotaje validó el protocolo:** la ronda 1 reveló fallas de perfil, pista y cronometraje; la ronda 2 cumplió los cinco criterios.

Desarrollo completo en [docs/conclusiones.md](docs/conclusiones.md).
