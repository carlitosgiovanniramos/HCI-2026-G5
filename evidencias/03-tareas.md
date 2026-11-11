# Tareas de la prueba · Prototipo CaféU

**Responsable de este documento:** Henry Lagua
**Prototipo:** https://false-wired-67481015.figma.site (respaldo: [`prototipos/prototipo.html`](../prototipos/prototipo.html))

El moderador lee cada tarea **tal como está escrita**. No explica dónde tocar.

| ID | Escenario que se le lee al usuario | Meta | Tiempo máximo | Criterio de éxito | Uso |
|---|---|---|---|---|---|
| T1 | "¿En qué horario atiende la cafetería?" | 60 s | 2 min | Dice "lunes a viernes, de 7:00 a 19:00" | **Pilotaje** y exposición |
| T2 | "Agrega un sánduche de queso a tu pedido." | 60 s | 2 min | "Mi pedido" contiene 1 Sánduche de queso | **Pilotaje** |
| T3 | "Agrega también dos cafés americanos." | 60 s | 2 min | "Mi pedido" contiene 1 Sánduche de queso y 2 Café americano (total $5,75) | **Pilotaje** |
| T4 | "Ya no quieres el sánduche. Quítalo, confirma tu pedido y dime tu número de pedido." | 90 s | 3 min | Se ve "¡Pedido confirmado!" con 2 Café americano ($3,00) y el usuario dice **#CU-104** | **Pilotaje** |
| T5 | "¿Cuántos productos de comida ofrece la cafetería?" | 60 s | 2 min | Dice **3** | **Pilotaje** y exposición |
| T6 | "¿Cuánto pagarías por 3 croissants?" | 90 s | 3 min | Dice **$5,25** | **Pilotaje** y exposición |

**Orden del pilotaje:** T1 → T2 → T3 → T4 → T5 → T6. T1 se responde desde la pantalla Inicio, donde empieza la sesión. T3 y T4 parten del pedido que dejó la tarea anterior. T5 y T6 van después de confirmar, para no alterar el número #CU-104 de T4.

**Cambio respecto a la primera versión:** al principio el pilotaje usaba solo T2, T3 y T4, porque en el Dashboard 2.0 los datos eran compartidos y las tareas de consulta se reservaban para la clase. CaféU guarda los datos solo en el navegador, así que el 10/11/2026 se decidió pilotear las seis: así las tareas que hará la clase también se prueban antes (Issue #9).

**Justificación:**
- Las tareas del pilotaje recorren el flujo central de CaféU: **armar** un pedido (T2), **modificarlo** agregando productos (T3), **quitar** un producto y **confirmar** (T4).
- T1, T5 y T6 son de **consulta**: son cortas, no dependen unas de otras y cada grupo de la clase puede hacerlas en su propio celular o laptop. En el pilotaje se aplican también, para validarlas antes de usarlas con la clase.
- **Metas:** en el APE 4, P01 y P02 hicieron tareas parecidas en la versión v3 en 17 a 26 s. Las metas de 60 a 90 s dan margen a un usuario nuevo; el pilotaje comprueba si son realistas.

## Respuestas correctas
Salen del contenido fijo del prototipo (código fuente y pantallas publicadas), así que no cambian entre sesiones.

| Tarea | Respuesta correcta | Dónde está en el prototipo |
|---|---|---|
| T1 | **Lunes a viernes · 7:00 – 19:00** | Pantalla Inicio, recuadro "Horario de atención" |
| T3 | Pedido de **$5,75** (2,75 + 2 × 1,50) | Mi pedido → Total |
| T4 | **#CU-104** y total **$3,00** | Pantalla "¡Pedido confirmado!" → "Número de pedido". Es #CU-104 solo si es el primer pedido desde que se cargó la página |
| T5 | **3** (Sánduche de queso, Croissant y Empanada de pollo) | Menú → filtro "Comida" → "3 productos" |
| T6 | **$5,25** (3 × $1,75) | Menú → Croissant → cantidad 3 → "Agregar al pedido · $5.25" |

**Respuestas aceptadas:** T1 también vale "de 7 a 7 entre semana". T6 también vale "5,25" o "cinco veinticinco". En T4 el número debe ser exacto.

## Pista permitida
- **Texto exacto (el mismo para todas las tareas):** "Vuelve a leer la tarea y revisa las opciones que tienes en pantalla."
- **Cuándo se da:** solo si el usuario la pide o si pasan **30 segundos sin avanzar**.
- **Cuántas veces:** una vez por tarea.
- **Efecto:** si el usuario completa la tarea después de la pista, se registra *Con ayuda* y no cuenta como éxito.
- **Prohibido:** señalar la pantalla, nombrar botones o pantallas ("Menú", "Mi pedido", "Quitar"), o decir "casi" o "por ahí".

## Reinicio entre participantes
El prototipo guarda el pedido **solo en la memoria del navegador**. Al recargar la página todo vuelve al estado inicial y el número de pedido vuelve a #CU-104.

Lo hace el soporte técnico (Henry) al terminar cada sesión:
1. Detener la grabación, si la hubo.
2. Recargar la página (**F5**).
3. Comprobar el **estado inicial**: pantalla **Inicio**, botón "Mi pedido" con **0** y ningún aviso en pantalla.

**Por qué es obligatorio:** si no se recarga, el siguiente participante vería el pedido anterior y en T4 obtendría #CU-105 en lugar de #CU-104.

## Comprobación antes del pilotaje (ensayo interno)
Antes de recibir a P1, el grupo hace una vez T2 → T3 → T4 completo y después:
- comprueba que T4 da **#CU-104** y $3,00;
- recarga la página y verifica que el prototipo vuelve al estado inicial;
- revisa que las imágenes cargan (si no cargan, se anota: el flujo funciona igual).

Si algo no funciona, se anota en la sección 12 del [plan](01-plan-de-evaluacion.md) como ajuste del protocolo.
