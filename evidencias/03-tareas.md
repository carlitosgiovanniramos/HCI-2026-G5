# Tareas de la prueba · Usability Test Dashboard 2.0

**Responsable de este documento:** Henry Lagua
**Acceso:** https://hci-proyecto-hazel.vercel.app/ → botón "Entrar como evaluador de demostración"

El moderador lee cada tarea **tal como está escrita**. No explica dónde hacer clic.

| ID | Escenario que se le lee al usuario | Meta | Tiempo máximo | Criterio de éxito | Uso |
|---|---|---|---|---|---|
| T1 | "Entre al sistema como evaluador de demostración y dígame cuál es la tasa de éxito de la prueba 'Portal Académico'." | 60 s | 2 min | Dice el valor de la tabla de respuestas | Exposición |
| T2 | "Cree una prueba llamada 'Sistema de biblioteca' con una tarea y llegue a la guía de moderación." | 4 min | 8 min | La prueba existe con una tarea y el usuario ve la guía de moderación | **Pilotaje** |
| T3 | "Registre una observación y aplique la sugerencia de la IA." | 3 min | 6 min | La observación queda registrada en la prueba 'Sistema de biblioteca' y la sugerencia se aplicó | **Pilotaje** |
| T4 | "Complete la síntesis, finalice la prueba y genere el Sprint Backlog." | 3 min | 6 min | La prueba figura como finalizada y se ve el Sprint Backlog generado | **Pilotaje** |
| T5 | "En el Sprint 4 del tablero SCRUM, cuente las tareas en 'Terminado' y dígame quién tiene el 'Generador de informe formal PDF'." | 3 min | 6 min | Dice la cuenta y el responsable de la tabla de respuestas | Exposición |
| T6 | "Consulte cuánto mejoró la tasa de éxito en Antes/Después." | 60 s | 2 min | Dice el valor de la tabla de respuestas | Exposición |

**Orden del pilotaje:** T2 → T3 → T4. T3 y T4 dependen de la prueba creada en T2, por eso no se pueden cambiar de orden.

**Justificación:** las tareas recorren el flujo central del Dashboard (acceder, crear, observar, sintetizar y consultar resultados) y combinan tareas de **búsqueda de información** (T1, T5 y T6) con tareas de **creación y edición** (T2, T3 y T4).

## Respuestas correctas (T1, T5 y T6)
Se verifican en el Dashboard **el mismo día de la sesión**, después del reinicio, porque todos los usuarios de demostración comparten los mismos datos.

| Tarea | Respuesta correcta | Verificado el | Por |
|---|---|---|---|
| T1 · Tasa de éxito de "Portal Académico de Matrícula UTA" | **75 %** (pestaña Resultados) | 10/11/2026 | Carlos Ramos |
| T5 · Tareas en "Terminado" del Sprint 4 | **8** (Tablero SCRUM → Sprint 4) | 10/11/2026 | Carlos Ramos |
| T5 · Responsable del "Generador de informe formal PDF con indicadores KPI" (RF.EXP.02) | **Melany Cevallos** | 10/11/2026 | Carlos Ramos |
| T6 · Mejora de la tasa de éxito en Antes/Después | **+36 puntos: de 58 % (versión 1.0) a 94 % (versión 2.0)**. La pantalla lo muestra como "+36% Mejora" | 10/11/2026 | Carlos Ramos |

**Respuestas aceptadas en T6:** "36 %", "+36", "36 puntos" o "de 58 a 94". Ojo: son 36 **puntos porcentuales**, no un 36 % relativo (la mejora relativa sería del 62 %).

Henry vuelve a comprobar estos valores el día del pilotaje y el día de la exposición.

**Estado inicial del Dashboard (para comprobar el reinicio):** en Resultados, "Pruebas realizadas: 1" (solo "Portal Académico de Matrícula UTA", 21/9/2026) y "Planificadas: 0". En el Sprint 4: Por hacer 0, En progreso 0, En revisión 0, Terminado 8. Si después del reinicio no se ve exactamente esto, algo quedó del participante anterior.

## Pista permitida
- **Texto exacto (el mismo para todas las tareas):** "Vuelva a leer la tarea y revise las opciones que tiene en pantalla."
- **Cuándo se da:** solo si el usuario la pide o si pasa **1 minuto sin avanzar**.
- **Cuántas veces:** una vez por tarea.
- **Efecto:** si el usuario completa la tarea después de la pista, se registra *Con ayuda* y no cuenta como éxito.
- **Prohibido:** señalar la pantalla, nombrar botones o menús, o decir "casi" o "por ahí".

## Reinicio entre participantes
**Por qué hace falta:** el botón "Entrar como evaluador de demostración" usa **un solo usuario fijo** y un solo proyecto. Lo que crea un participante lo ve el siguiente, y lo vería la clase el 17/11.

Lo hace el soporte técnico (Henry) al terminar cada sesión:
1. En el Dashboard, eliminar la prueba "Sistema de biblioteca" (botón **Eliminar** → **Sí, eliminar**).
2. Comprobar que no quedó ninguna otra prueba ni tarea nueva creada durante la sesión. Si quedó, eliminarla.
3. Cerrar sesión desde la aplicación. Esto también borra el borrador guardado en el navegador.
4. Cerrar la ventana y abrir una **ventana de incógnito nueva** de Chrome para el siguiente participante.
5. Volver a comprobar que las respuestas de T1, T5 y T6 no cambiaron.

**Riesgo detectado en T6:** la pantalla Antes/Después tiene dos partes: la matriz fija del estudio (58 % → 94 %) y una comparación "calculada en vivo". La parte en vivo solo aparece cuando hay **dos o más pruebas con observaciones**. Hoy hay una sola, así que muestra el mensaje "Se necesitan al menos dos planes de prueba…". Si la prueba "Sistema de biblioteca" (creada en T2, con la observación de T3) **no se elimina**, aparecerá una segunda comparación con otros números y T6 se volverá ambigua para la clase.

## Comprobación antes del pilotaje (ensayo interno)
Antes de recibir a P1, el grupo hace una vez T2 → T3 → T4 completo y después:
- vuelve a revisar T1, T5 y T6, para comprobar que generar el Sprint Backlog (T4) no cambia esas respuestas;
- aplica el reinicio y verifica que el Dashboard vuelve al estado inicial.

Si algo cambia, se anota en la sección 12 del [plan](01-plan-de-evaluacion.md) como ajuste del protocolo.
