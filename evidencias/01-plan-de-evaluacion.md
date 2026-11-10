# Plan de evaluación · APE 6, Fases 1 y 2

**Grupo 5 · Interacción Persona-Ordenador · UTA · Paralelo 5A**
**Aplicación evaluada:** Usability Test Dashboard 2.0 (https://hci-proyecto-hazel.vercel.app/)
**Responsable de este documento:** Carlos Ramos

## 0. Alcance del Grupo 5
Según la matriz de la asignatura, al G5 (5A) le corresponden las **Fases 1 y 2 del APE 6**:

| Fase | Qué incluye | Responsable |
|---|---|---|
| 1. Planificación | Contexto, objetivos, participantes, tareas, métricas, ética y registro | **G5** (este documento y los archivos 02 a 04) |
| 2. Pilotaje | Ensayo del protocolo con participantes reales y ajuste del plan | **G5** (carpeta `resultados/`) |
| 3. Aplicación y análisis | Aplicar y comparar métodos, triangular, matriz de hallazgos y severidad | G6 |
| 4. Cierre | Backlog priorizado, criterios técnicos y conclusiones finales | G6 |

## 1. Contexto
El Dashboard 2.0 es una aplicación web para gestionar pruebas de usabilidad. Permite crear pruebas con tareas, acceder a la guía de moderación, registrar observaciones con sugerencias de IA, completar la síntesis, generar un Sprint Backlog, consultar el tablero SCRUM y comparar resultados Antes/Después.

La aplicación pasó las pruebas técnicas del equipo (**verificación**: ¿construimos bien el producto?). Falta comprobar si un evaluador nuevo puede usarla (**validación**: ¿construimos el producto correcto?).

## 2. Objetivos
**General:** planificar y pilotear una evaluación de usabilidad del Dashboard 2.0 con evaluadores nuevos, combinando la evaluación heurística de Nielsen con la prueba con usuarios.

**Específicos de la evaluación (Fase 1):**
1. Definir tareas, métricas y reglas que permitan medir eficacia (tasa de éxito), eficiencia (tiempo y errores) y satisfacción (SUS), según ISO 9241-11.
2. Preparar los instrumentos: consentimiento, tareas, hoja de observación y cuestionario SUS.

**Específicos del pilotaje (Fase 2):**
3. Comprobar que las tareas T2, T3 y T4 se entienden sin explicaciones adicionales.
4. Comprobar que las metas de tiempo son realistas.
5. Comprobar que la hoja de observación permite registrar todo lo que ocurre.
6. Registrar los ajustes al protocolo (versión 1 → versión 2) y los hallazgos preliminares que se entregan al G6.

**Pregunta de evaluación:** ¿en qué medida el Dashboard 2.0 permite a un evaluador nuevo completar sus tareas principales con eficacia, eficiencia y satisfacción, y qué problemas lo impiden?

## 3. Métodos
| Método | Tipo | Qué aporta | Quién lo aplica |
|---|---|---|---|
| Evaluación heurística (10 heurísticas de Nielsen) | Analítico (expertos) | Problemas previstos y el principio violado | Cada integrante del G5 por separado (Issue #6) |
| Prueba de usabilidad con pensamiento en voz alta | Empírico (usuarios) | Problemas confirmados y métricas | Participantes externos (pilotaje) y la clase (exposición) |

La combinación de ambos permite triangular: un problema que aparece en los dos métodos tiene más evidencia. La triangulación completa la realiza el G6.

## 4. Participantes del pilotaje
- **Perfil:** estudiantes de Software que no participaron en el desarrollo del Dashboard 2.0.
- **Número:** 3 participantes (P1, P2 y P3).
- **Identificación:** solo códigos P1, P2 y P3. No hay nombres en ningún archivo del repositorio.
- **Criterio de exclusión:** haber colaborado en el desarrollo del Dashboard 2.0 o conocer de antemano las tareas.
- **Limitación declarada:** con 3 participantes las métricas son descriptivas, no estadísticas. Sirven para validar el protocolo y detectar problemas evidentes, no para generalizar.

## 5. Tareas y metas
Ver [03-tareas.md](03-tareas.md).

| Momento | Tareas | Quién las hace |
|---|---|---|
| Pilotaje (antes del 17/11) | T2 → T3 → T4 | P1, P2 y P3 |
| Exposición (17/11) | T1, T5 y T6 | Un compañero en la demostración en vivo y los demás grupos en la actividad de clase |

## 6. Métricas y definiciones
| Métrica | Dimensión (ISO 9241-11) | Cómo se calcula |
|---|---|---|
| Tasa de éxito por tarea | Eficacia | (participantes con "Sí" / participantes que intentaron la tarea) × 100 |
| Tiempo en tarea | Eficiencia | mm:ss desde que el moderador termina de leer la tarea hasta que el usuario la completa o abandona. Se reporta la mediana |
| Errores | Eficacia y eficiencia | Conteo de errores críticos y no críticos por tarea |
| SUS | Satisfacción | 10 ítems. Impares: valor − 1. Pares: 5 − valor. Suma × 2,5 = puntaje de 0 a 100 (referencia: 68) |

**Reglas fijadas antes de la prueba:**
- **Éxito:** *Sí* = la completa sin ayuda. *Con ayuda* = la completa después de la pista permitida. *No* = no la completa o abandona. Solo "Sí" cuenta como éxito.
- **Error:** acción que no acerca al resultado esperado. Es *crítico* si impide completar la tarea y *no crítico* si el usuario se recupera solo.
- **Tiempo máximo:** si el usuario supera el doble de la meta (T2: 8 min; T3 y T4: 6 min), el moderador termina la tarea y registra "No".

## 7. Roles
Los roles cambian según el momento, porque en el pilotaje el usuario **no puede** ser un integrante del G5.

| Rol | Responsabilidad | Pilotaje | Exposición (17/11) |
|---|---|---|---|
| Moderador | Lee las tareas y conduce la sesión sin guiar | Carlos Ramos | Carlos Ramos |
| Usuario | Hace las tareas pensando en voz alta | P1, P2 y P3 (externos) | Henry Lagua (demostración del método) |
| Registro de métricas | Cronometra y anota éxito, tiempo y errores | Melany Cevallos | Melany Cevallos |
| Observador | Anota frases, dudas, fricciones y posibles heurísticas | Allison Cobos | Allison Cobos |
| Soporte técnico | Reinicia el Dashboard entre participantes y controla la grabación | Henry Lagua | — |

**Regla del moderador:** no ayudar ni sugerir dónde hacer clic. Solo puede dar la pista permitida definida en [03-tareas.md](03-tareas.md).

## 8. Procedimiento de cada sesión (unos 20 minutos)
1. Bienvenida: "se evalúa la aplicación, no a usted" (1 min).
2. Lectura del consentimiento ([02-consentimiento-informado.md](02-consentimiento-informado.md)) y aceptación verbal; se pregunta si acepta la grabación de pantalla (2 min).
3. Entrada al Dashboard con el botón "Entrar como evaluador de demostración".
4. Tareas T2, T3 y T4 en orden, con registro en la hoja ([04-hoja-de-observacion.md](04-hoja-de-observacion.md)) (10 min como meta, hasta 20 como máximo).
5. Cuestionario SUS (3 min).
6. Cierre: "¿qué fue lo más confuso y qué funcionó mejor?" (2 min).
7. Reinicio del Dashboard antes del siguiente participante.

## 9. Entorno
- **Equipo:** laptop Lenovo LOQ (modelo 83JC) con Windows 11, la misma para los 3 participantes.
- **Navegador:** Google Chrome 157, en una ventana nueva sin extensiones visibles.
- **Resolución:** 1536 × 864 px (resolución efectiva con el escalado de Windows).
- **Conexión:** internet de la universidad o del lugar de la sesión. Se anota cualquier caída.
- **Cronómetro:** el del celular de la persona de registro de métricas.
- **Grabación de pantalla:** solo si el participante la acepta. Se graba **solo la pantalla, sin cámara ni audio**, con la Xbox Game Bar de Windows (Win + Alt + R). Los videos **no se suben a GitHub**: se guardan en una carpeta privada del grupo y se usan solo para revisar tiempos y errores.

## 10. Ética
- La participación es voluntaria y se puede abandonar en cualquier momento sin consecuencia.
- Los datos se anonimizan con los códigos P1, P2 y P3. No se publican nombres, firmas, rostros ni voces en GitHub.
- Se evalúa la aplicación, no a la persona.
- La hoja de consentimiento con datos personales, si existe, se guarda fuera del repositorio.

## 11. Criterios para dar por validado el protocolo
Al terminar el pilotaje se revisa cada criterio. Si alguno falla, se ajusta el protocolo y se anota en la sección 12.

| Criterio | Se cumple si… |
|---|---|
| Comprensión de las tareas | Ningún participante pide que se le repita o explique la tarea |
| Metas de tiempo | Al menos 2 de 3 participantes terminan cada tarea antes del tiempo máximo |
| Hoja de observación | Registro y observación pudieron anotar todo sin quedarse atrás |
| Estabilidad técnica | No hubo fallos del servicio que obligaran a repetir una tarea |
| Duración de la sesión | La sesión completa duró 25 minutos o menos |

## 12. Resultados del pilotaje y ajustes (se llena después de las sesiones)
Los datos se registran en `resultados/` y el resumen va aquí. No se inventan datos.

| Qué se observó | Ajuste al protocolo (v1 → v2) |
|---|---|
| | |

**Hallazgos preliminares para el G6:** se listan en `resultados/` con la tarea, la evidencia y la heurística posiblemente violada. El G6 les asigna la severidad final (1 cosmético a 4 crítico) y construye el backlog.

## 13. Cronograma
| Fecha | Actividad |
|---|---|
| 10/11/2026 | Plan, consentimiento, tareas y hoja de observación (Fase 1) |
| 11/11/2026 – 12/11/2026 | Respuestas correctas de T1, T5 y T6 y ensayo interno del protocolo |
| 12/11/2026 – 13/11/2026 | Pilotaje con P1, P2 y P3 (Fase 2) |
| 14/11/2026 – 15/11/2026 | Registro de resultados, evaluación heurística individual y ajustes del protocolo |
| 16/11/2026 | Ensayo de roles y preparación para el grupo QA/UX |
| 17/11/2026 | Exposición en clase (laboratorio de usabilidad) |
| Por confirmar con el docente | Subida del archivo del APE 6 al aula virtual |

## 14. Riesgos
| Riesgo | Mitigación |
|---|---|
| Solo 3 participantes | Declararlo como limitación; las métricas son descriptivas |
| El moderador ayuda sin querer | Guion fijo, pista única definida y ensayo previo |
| Fallo del servicio durante la prueba | Registrar el incidente, reiniciar y repetir la tarea |
| Un participante conoce el Dashboard | Aplicar el criterio de exclusión antes de empezar |
| Datos de un participante quedan en el Dashboard | Reinicio definido en [03-tareas.md](03-tareas.md) entre sesiones |
