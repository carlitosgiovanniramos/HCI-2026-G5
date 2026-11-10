# Plan de evaluación · APE 6, Fase 1

**Grupo 5 · Interacción Persona-Ordenador · UTA · Paralelo 5A**
**Aplicación evaluada:** Usability Test Dashboard 2.0 (https://hci-proyecto-hazel.vercel.app/)
**Responsable de este documento:** Carlos Ramos

## 1. Contexto
El Dashboard 2.0 es una aplicación web para gestionar pruebas de usabilidad: crear pruebas con tareas, acceder a la guía de moderación, registrar observaciones con sugerencias de IA, completar la síntesis, generar un Sprint Backlog, consultar el tablero SCRUM y comparar resultados Antes/Después. Pasó las pruebas técnicas del equipo (verificación). Falta validar si un evaluador nuevo puede usarlo (validación).

## 2. Objetivos
**General:** evaluar la usabilidad del Dashboard 2.0 con evaluadores nuevos mediante evaluación heurística de Nielsen y prueba con usuarios.

**Específicos:**
1. Medir eficacia (tasa de éxito), eficiencia (tiempo y errores) y satisfacción (SUS).
2. Detectar problemas de usabilidad y clasificarlos por severidad.
3. Contrastar los hallazgos de ambos métodos (triangulación).
4. Convertir los hallazgos priorizados en un backlog de Issues.

**Pregunta de evaluación:** ¿en qué medida el Dashboard 2.0 permite a un evaluador nuevo completar sus tareas principales con eficacia, eficiencia y satisfacción, y qué problemas lo impiden?

## 3. Métodos
| Método | Tipo | Qué aporta |
|---|---|---|
| Evaluación heurística (10 heurísticas de Nielsen) | Analítico | Problemas previstos y el principio violado |
| Prueba de usabilidad con pensamiento en voz alta | Empírico | Problemas confirmados y métricas |

## 4. Participantes
- **Perfil:** estudiantes de Software que no participaron en el desarrollo del Dashboard.
- **Número:** [COMPLETAR: mínimo 3 para el piloto; ideal 5].
- **Identificación:** P1, P2, P3... sin nombres en ningún archivo del repositorio.
- **Criterio de exclusión:** haber colaborado en el desarrollo del Dashboard 2.0.

## 5. Tareas y metas
Ver [03-tareas.md](03-tareas.md). El piloto usa T2, T3 y T4. La demostración en clase usa T1, T5 y T6.

## 6. Métricas y definiciones
| Métrica | Dimensión | Cómo se registra |
|---|---|---|
| Tasa de éxito | Eficacia | (tareas con "Sí" / tareas intentadas) × 100 |
| Tiempo en tarea | Eficiencia | mm:ss desde que el usuario inicia hasta que completa o abandona |
| Errores | Eficacia / eficiencia | Conteo de críticos y no críticos por tarea |
| SUS | Satisfacción | Cuestionario de 10 ítems; puntaje 0-100 (impares −1, pares 5−valor, suma × 2,5) |

**Reglas fijadas antes de la prueba:**
- **Éxito:** *Sí* = sin ayuda; *Con ayuda* = tras una pista; *No* = no completa o abandona. Solo "Sí" cuenta como éxito.
- **Error:** acción que no acerca al resultado esperado. *Crítico* si impide completar la tarea; *no crítico* si el usuario se recupera solo.
- **Tiempo máximo:** si el usuario supera el doble de la meta, el moderador puede dar por terminada la tarea y registrar "No".

## 7. Roles
| Rol | Responsabilidad | Integrante |
|---|---|---|
| Moderador | Presenta las tareas y conduce la sesión sin guiar al usuario | Carlos Ramos |
| Usuario | Realiza las tareas hablando en voz alta | Henry Lagua |
| Registro de métricas | Cronometra y anota éxito, tiempo y errores | Melany Cevallos |
| Observador | Anota dudas, comentarios y fricciones | Allison Cobos |

Los roles pueden rotar para obtener más datos. **Regla del moderador:** no ayudar ni sugerir dónde hacer clic.

## 8. Procedimiento de la sesión
1. Bienvenida y explicación: "se evalúa la aplicación, no a usted" (2 min).
2. Consentimiento informado ([02-consentimiento-informado.md](02-consentimiento-informado.md)) (2 min).
3. Entrada al Dashboard con "Entrar como evaluador de demostración".
4. Tareas en orden, con registro en la hoja ([04-hoja-de-observacion.md](04-hoja-de-observacion.md)).
5. Cuestionario SUS al final.
6. Breve conversación de cierre: ¿qué fue lo más confuso y lo mejor?

## 9. Entorno
- Dispositivo, navegador y resolución: [COMPLETAR]
- Cronómetro: [COMPLETAR]
- Grabación de pantalla: [COMPLETAR: solo con consentimiento explícito]

## 10. Ética
- Participación voluntaria; se puede abandonar en cualquier momento sin consecuencia.
- Datos anonimizados (P1, P2...). No se publican nombres ni firmas en GitHub.
- Se evalúa la aplicación, no a la persona.

## 11. Análisis previsto
1. Calcular métricas por tarea y por participante.
2. Consolidar los hallazgos de la heurística y de la prueba.
3. Asignar severidad (1 cosmético a 4 crítico) con frecuencia, impacto y persistencia.
4. Crear Issues con etiqueta de severidad. El análisis completo lo continúa el G6 (Fases 3 y 4).

## 12. Cronograma
| Fecha | Actividad |
|---|---|
| Hasta 16/11/2026 | Plan, documentos, pilotaje T2-T4, ensayo de roles |
| 17/11/2026 | Exposición en clase (laboratorio de usabilidad) |
| [COMPLETAR] | Subida del archivo del APE al aula virtual |

## 13. Riesgos
| Riesgo | Mitigación |
|---|---|
| Pocos participantes | Declararlo como limitación; las métricas son descriptivas |
| El moderador ayuda sin querer | Guion y ensayo previo |
| Fallo del servicio durante la prueba | Registrar el incidente y repetir la tarea |
