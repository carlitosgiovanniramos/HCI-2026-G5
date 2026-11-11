# Plan de evaluación · APE 6, Fases 1 y 2

**Grupo 5 · Interacción Persona-Ordenador · UTA · Paralelo 5A**
**Prototipo evaluado:** CaféU (https://false-wired-67481015.figma.site · copia local en [`prototipos/prototipo.html`](../prototipos/prototipo.html))
**Responsable de este documento:** Carlos Ramos

## 0. Alcance del Grupo 5
Según la matriz de la asignatura, al G5 (5A) le corresponden las **Fases 1 y 2 del APE 6**:

| Fase | Qué incluye | Responsable |
|---|---|---|
| 1. Planificación | Contexto, objetivos, participantes, tareas, métricas, ética y registro | **G5** (este documento y los archivos 02 a 05) |
| 2. Pilotaje | Ensayo del protocolo con participantes reales y ajuste del plan | **G5** (carpeta `resultados/`) |
| 3. Aplicación y análisis | Aplicar y comparar métodos, triangular, matriz de hallazgos y severidad | G6 |
| 4. Cierre | Backlog priorizado, criterios técnicos y conclusiones finales | G6 |

**Por qué CaféU:** la matriz pide evaluar el prototipo del proyecto. La cadena de los APE es: **APE 4** (prototipo de CaféU en Figma) → **APE 5** (paso del prototipo a HTML) → **APE 6** (evaluación de ese prototipo con usuarios). Ver Issue #9.

## 1. Contexto
**CaféU** es un prototipo de aplicación web móvil para que los estudiantes **pidan en la cafetería universitaria antes de llegar** y recojan su pedido sin hacer fila. El flujo es:

**Inicio → Menú** (buscador y filtros Todo, Bebidas y Comida) **→ Detalle del producto** (cantidad y "Agregar al pedido") **→ Mi pedido** (cambiar cantidad, "Quitar" y "Confirmar pedido") **→ Pedido confirmado** (número de pedido).

En el APE 4 se probó la versión v3 de CaféU con dos participantes (P01 y P02), en tareas parecidas que tomaron entre 17 y 26 segundos. La versión que se evalúa ahora es la **publicada en Figma Make**, que no incluye el pago simulado ni la confirmación al quitar productos de la v3.

El prototipo funciona: navega, calcula totales y genera el número de pedido (**verificación**: ¿construimos bien el producto?). Falta comprobar si un estudiante que no lo diseñó puede usarlo sin ayuda (**validación**: ¿construimos el producto correcto?).

## 2. Objetivos
**General:** planificar y pilotear una evaluación de usabilidad del prototipo CaféU con estudiantes que no participaron en su diseño, combinando la evaluación heurística de Nielsen con la prueba con usuarios.

**Específicos de la evaluación (Fase 1):**
1. Definir tareas, métricas y reglas que permitan medir eficacia (tasa de éxito), eficiencia (tiempo y errores) y satisfacción (SUS), según ISO 9241-11.
2. Preparar los instrumentos: consentimiento, tareas, hoja de observación, cuestionario SUS y guía del pilotaje.

**Específicos del pilotaje (Fase 2):**
3. Comprobar que las seis tareas (T1 a T6) se entienden sin explicaciones adicionales, incluidas las que hará la clase.
4. Comprobar que las metas de tiempo son realistas.
5. Comprobar que la hoja de observación permite registrar todo lo que ocurre.
6. Registrar los ajustes al protocolo (versión 1 → versión 2) y los hallazgos preliminares que se entregan al G6.

**Pregunta de evaluación:** ¿en qué medida el prototipo CaféU permite a un estudiante nuevo armar, modificar y confirmar un pedido con eficacia, eficiencia y satisfacción, y qué problemas lo impiden?

## 3. Métodos
| Método | Tipo | Qué aporta | Quién lo aplica |
|---|---|---|---|
| Evaluación heurística (10 heurísticas de Nielsen) | Analítico (expertos) | Problemas previstos y el principio violado | Cada integrante del G5 por separado (Issue #6) |
| Prueba de usabilidad con pensamiento en voz alta | Empírico (usuarios) | Problemas confirmados y métricas | Participantes externos (pilotaje) y la clase (exposición) |

La combinación de ambos permite triangular: un problema que aparece en los dos métodos tiene más evidencia. La triangulación completa la realiza el G6.

## 4. Participantes del pilotaje
- **Perfil:** estudiantes universitarios que usan la cafetería y no participaron en el diseño de CaféU.
- **Número:** 3 participantes (P1, P2 y P3).
- **Identificación:** solo códigos P1, P2 y P3. No hay nombres en ningún archivo del repositorio.
- **Criterios de exclusión:** haber diseñado CaféU, haber participado en la prueba del APE 4 (P01 y P02) o conocer de antemano las tareas.
- **Limitación declarada:** con 3 participantes las métricas son descriptivas, no estadísticas. Sirven para validar el protocolo y detectar problemas evidentes, no para generalizar.

## 5. Tareas y metas
Ver [03-tareas.md](03-tareas.md).

| Momento | Tareas | Quién las hace |
|---|---|---|
| Pilotaje (antes del 17/11) | T1 → T6: consultar (T1), armar, modificar y confirmar un pedido (T2 a T4) y consultar (T5 y T6) | P1, P2 y P3 |
| Exposición (17/11) | T1, T5 y T6 (consultar información) | Un compañero en la demostración en vivo y los demás grupos en la actividad de clase |

Al principio el pilotaje usaba solo T2, T3 y T4. Como CaféU no comparte datos entre usuarios, el 10/11/2026 se amplió a las seis tareas para validar también las que hará la clase.

## 6. Métricas y definiciones
| Métrica | Dimensión (ISO 9241-11) | Cómo se calcula |
|---|---|---|
| Tasa de éxito por tarea | Eficacia | (participantes con "Sí" / participantes que intentaron la tarea) × 100 |
| Tiempo en tarea | Eficiencia | mm:ss desde que el moderador termina de leer la tarea hasta que el usuario la completa o abandona. Se reporta la mediana |
| Errores | Eficacia y eficiencia | Conteo de errores críticos y no críticos por tarea |
| SUS | Satisfacción | 10 ítems. Impares: valor − 1. Pares: 5 − valor. Suma × 2,5 = puntaje de 0 a 100 (referencia: 68) |

**Reglas fijadas antes de la prueba:**
- **Éxito:** *Sí* = la completa sin ayuda. *Con ayuda* = la completa después de la pista permitida. *No* = no la completa o abandona. Solo "Sí" cuenta como éxito.
- **Error:** acción que no acerca al resultado esperado (por ejemplo, entrar a un producto equivocado o buscar sin resultados). Es *crítico* si impide completar la tarea y *no crítico* si el usuario se recupera solo.
- **Tiempo máximo:** el doble de la meta (T1, T2, T3 y T5: 2 min; T4 y T6: 3 min). Al superarlo, el moderador termina la tarea y registra "No".

## 7. Roles
Los roles cambian según el momento, porque en el pilotaje el usuario **no puede** ser un integrante del G5.

| Rol | Responsabilidad | Pilotaje | Exposición (17/11) |
|---|---|---|---|
| Moderador | Lee las tareas y conduce la sesión sin guiar | Carlos Ramos | Carlos Ramos |
| Usuario | Hace las tareas pensando en voz alta | P1, P2 y P3 (externos) | Henry Lagua (demostración del método) |
| Registro de métricas | Cronometra y anota éxito, tiempo y errores | Melany Cevallos | Melany Cevallos |
| Observador | Anota frases, dudas, fricciones y posibles heurísticas | Allison Cobos | Allison Cobos |
| Soporte técnico | Recarga el prototipo entre participantes y controla la grabación | Henry Lagua | — |

**Regla del moderador:** no ayudar ni sugerir dónde tocar. Solo puede dar la pista permitida definida en [03-tareas.md](03-tareas.md).

## 8. Procedimiento de cada sesión (unos 20 minutos)
1. Bienvenida: "se evalúa la aplicación, no a usted" (1 min).
2. Lectura del consentimiento ([02-consentimiento-informado.md](02-consentimiento-informado.md)) y aceptación verbal; se pregunta si acepta la grabación de pantalla (2 min).
3. El prototipo ya está abierto en la pantalla **Inicio** con el pedido vacío.
4. Tareas T1 a T6 en orden, con registro en la hoja ([04-hoja-de-observacion.md](04-hoja-de-observacion.md)) (7 min como meta, hasta 14 como máximo).
5. Cuestionario SUS (3 min).
6. Cierre: "¿qué fue lo más confuso y qué funcionó mejor?" (2 min).
7. Reinicio del prototipo antes del siguiente participante (ver [05-guia-del-pilotaje.md](05-guia-del-pilotaje.md)).

## 9. Entorno
- **Equipo:** laptop Lenovo LOQ (modelo 83JC) con Windows 11, la misma para los 3 participantes.
- **Navegador:** Google Chrome 157, en una ventana de incógnito.
- **Prototipo:** https://false-wired-67481015.figma.site. En pantallas grandes se muestra dentro de un marco de celular de 390 × 844 px. Respaldo sin cambios: [`prototipos/prototipo.html`](../prototipos/prototipo.html).
- **Resolución de la laptop:** 1536 × 864 px (resolución efectiva con el escalado de Windows).
- **Conexión:** internet necesario (las imágenes de los productos se cargan en línea). Se anota cualquier caída.
- **Cronómetro:** el del celular de la persona de registro de métricas.
- **Grabación de pantalla:** solo si el participante la acepta. Se graba **solo la pantalla, sin cámara ni audio**, con la Xbox Game Bar de Windows (Win + Alt + R). Los videos **no se suben a GitHub**: se guardan en una carpeta privada del grupo y se usan solo para revisar tiempos y errores.

## 10. Ética
- La participación es voluntaria y se puede abandonar en cualquier momento sin consecuencia.
- Los datos se anonimizan con los códigos P1, P2 y P3. No se publican nombres, firmas, rostros ni voces en GitHub.
- Se evalúa la aplicación, no a la persona.
- El prototipo no pide datos personales ni pagos reales.

## 11. Criterios para dar por validado el protocolo
Al terminar el pilotaje se revisa cada criterio. Si alguno falla, se ajusta el protocolo y se anota en la sección 12.

| Criterio | Se cumple si… |
|---|---|
| Comprensión de las tareas | Ningún participante pide que se le repita o explique la tarea |
| Metas de tiempo | Al menos 2 de 3 participantes terminan cada tarea antes del tiempo máximo |
| Hoja de observación | Registro y observación pudieron anotar todo sin quedarse atrás |
| Estabilidad técnica | No hubo fallos del prototipo ni de la conexión que obligaran a repetir una tarea |
| Duración de la sesión | La sesión completa duró 20 minutos o menos |

## 12. Resultados del pilotaje y ajustes (se llena después de las sesiones)
Los datos se registran en `resultados/` y el resumen va aquí. No se inventan datos.

| Qué se observó | Ajuste al protocolo (v1 → v2) |
|---|---|
| Ensayo previo (10/11, 20:44): solo T1 se cronometró en vivo; los demás tiempos se estimaron | Esa corrida no cuenta como dato. Todos los tiempos se toman en vivo con cronómetro, desde que termina la lectura de la tarea |
| P1 no pertenece al perfil (mayor de 50 años, poca experiencia con apps) | Se conservan sus datos y se reportan aparte. P2 y P3 deben cumplir el perfil (estudiantes) |
| En T3 con P1 se dio una pista distinta de la permitida ("fíjese dentro del detalle del producto") | Llevar la pista escrita en la hoja y leerla textual. Si se da otra, registrarlo como desviación |
| Solo P1 pidió repetir T2 y T4 (T4 tiene tres pasos); P2 y P3 no | Mantener las consignas. En la v2, tener la tarea también escrita en una tarjeta para quien la pida |
| Duración: P1 22 min, P2 16 min, P3 14 min | Se mantienen los 20 min anunciados; solo P1 los superó |
| Ninguno de los tres confirmó ser estudiante universitario (P2 no lo registró; P3 tiene 12 años) | Preguntar y anotar el perfil antes de empezar. Aplicar el criterio de inclusión antes de la sesión, no después |
| P3 es menor de edad (participó con autorización de su madre o padre) | En la v2 se excluyen menores: no pertenecen al público de CaféU y el consentimiento no los contempla |
| En P2 y P3 cronometraron varios integrantes | Designar una sola persona para el cronómetro |
| Los tres dijeron que "no sale aviso" al agregar, aunque el aviso existe y dura 2,2 s | Se registra como "no percibido". Antes del 17/11 el grupo verifica en pantalla cuándo y dónde aparece |

Resultados completos en [`resultados/resumen-pilotaje.md`](../resultados/resumen-pilotaje.md).

**Hallazgos preliminares para el G6:** se listan en `resultados/` con la tarea, la evidencia y la heurística posiblemente violada. El G6 les asigna la severidad final (1 cosmético a 4 crítico) y construye el backlog.

## 13. Cronograma
| Fecha | Actividad |
|---|---|
| 10/11/2026 | Plan, consentimiento, tareas, hoja de observación y guía (Fase 1) |
| 11/11/2026 – 12/11/2026 | Ensayo interno del protocolo con el prototipo |
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
| Sin internet no cargan las imágenes | Probar la conexión antes; el flujo funciona igual sin imágenes y se anota |
| Un participante conoce CaféU | Aplicar los criterios de exclusión antes de empezar |
| El pedido de un participante queda en pantalla | Recargar la página entre sesiones (ver [05-guia-del-pilotaje.md](05-guia-del-pilotaje.md)) |
