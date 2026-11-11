# Guía del día del pilotaje · APE 6, Fase 2

**Grupo 5 · Interacción Persona-Ordenador · UTA · Paralelo 5A**
**Prototipo:** CaféU · https://false-wired-67481015.figma.site
**Issue:** #5 · **Responsables:** los 4 integrantes

Esta guía convierte el [plan](01-plan-de-evaluacion.md) en pasos concretos para que cualquier grupo pueda repetir el pilotaje con su propio prototipo.

## 1. Antes del día (checklist)
- [ ] **3 participantes confirmados:** estudiantes que no diseñaron CaféU, que no participaron en la prueba del APE 4 y que no conocen las tareas. Se les asigna P1, P2 y P3 en orden de llegada.
- [ ] **Lugar tranquilo** con una mesa y tres sillas detrás del participante (moderador al lado, registro y observación detrás).
- [ ] **Laptop Lenovo LOQ** cargada, con Chrome 157 e internet probado.
- [ ] **Celular con cronómetro** (Melany).
- [ ] **3 copias** de la hoja por participante ([04-hoja-de-observacion.md](04-hoja-de-observacion.md)), impresas o en OneNote.
- [ ] **Consentimiento** ([02-consentimiento-informado.md](02-consentimiento-informado.md)) y **tareas** ([03-tareas.md](03-tareas.md)) a la mano del moderador.
- [ ] **Ensayo interno** hecho (sección 2).

## 2. Ensayo interno (20 min antes, no genera datos)
1. Un integrante hace T2 → T3 → T4 completo. **Sus datos no cuentan**: solo sirve para probar el flujo.
2. Comprobar que T4 termina en "¡Pedido confirmado!" con **#CU-104** y **$3,00**.
3. Recargar la página (F5) y comprobar el estado inicial (sección 5).
4. Si algo no funciona, anotarlo en la sección 12 del plan como ajuste del protocolo.

## 3. Roles durante la sesión
| Rol | Quién | Qué hace |
|---|---|---|
| Moderador | Carlos | Lee el guion y las tareas palabra por palabra. No ayuda |
| Registro de métricas | Melany | Cronometra y llena la tabla de tareas |
| Observador | Allison | Anota frases textuales y la posible heurística |
| Soporte técnico | Henry | Deja el prototipo en el estado inicial, controla la grabación y recarga entre participantes |

## 4. Una sesión paso a paso (unos 15 min)
**Estado inicial:** Henry abrió https://false-wired-67481015.figma.site en una ventana de incógnito de Chrome. Se ve la pantalla **Inicio** ("Pide antes de llegar") y el botón **"Mi pedido"** marca **0**.

| Paso | Quién | Qué se dice o hace |
|---|---|---|
| 1. Bienvenida | Moderador | "Gracias por ayudarnos. Vamos a probar una aplicación, no a evaluarte a ti." |
| 2. Consentimiento | Moderador | Lee el texto de [02-consentimiento-informado.md](02-consentimiento-informado.md). Si acepta, marca su código y si acepta grabación |
| 3. Grabación | Soporte | Solo si aceptó: Win + Alt + R (solo pantalla, sin audio) |
| 4. Pensar en voz alta | Moderador | "Mientras trabajas, di en voz alta lo que piensas, lo que buscas y lo que te sorprende." |
| 5. T2 | Moderador / registro | "Agrega un sánduche de queso a tu pedido." **El cronómetro arranca al terminar de leer** y se detiene cuando lo logra o abandona |
| 6. T3 | Moderador / registro | "Agrega también dos cafés americanos." Igual que T2 |
| 7. T4 | Moderador / registro | "Ya no quieres el sánduche. Quítalo, confirma tu pedido y dime tu número de pedido." Igual que T2 |
| 8. SUS | Participante | Responde los 10 ítems solo, sin que nadie mire |
| 9. Cierre | Moderador | "¿Qué fue lo más confuso? ¿Qué funcionó mejor?" |
| 10. Agradecer | Moderador | Sin comentar su desempeño |

**Cuándo termina cada tarea (detener el cronómetro):**
- **T2:** el sánduche de queso ya está en el pedido (aparece el aviso "Producto agregado al pedido" o "Mi pedido" marca 1).
- **T3:** el pedido tiene 1 sánduche y 2 cafés americanos ("Mi pedido" marca 3).
- **T4:** el participante dice el número de pedido en la pantalla "¡Pedido confirmado!".

Si dice "ya terminé" pero no cumple el criterio, **no lo corrijas**: detén el cronómetro y anota lo que pasó.

**Lo que el moderador SÍ puede decir:**
- Si el participante se queda callado: "¿Qué estás pensando?" (es un recordatorio, **no** cuenta como pista).
- La pista permitida, una vez por tarea: "Vuelve a leer la tarea y revisa las opciones que tienes en pantalla." → se registra *Con ayuda*.
- Al superar el tiempo máximo (T2 y T3: 2 min; T4: 3 min): "Gracias, pasemos a la siguiente." → se registra *No*.
- Si pregunta "¿así está bien?": "Haz lo que harías normalmente."

**Lo que NO puede decir:** nombres de botones o pantallas ("Menú", "Mi pedido", "Quitar", "Confirmar"), "casi", "por ahí", "muy bien", ni señalar la pantalla.

## 5. Entre participantes: reinicio (Henry, 1 min)
1. Detener la grabación, si la hubo.
2. Recargar la página (**F5**).
3. Comprobar el estado inicial: pantalla **Inicio** y "Mi pedido" en **0**.

El grupo llena la sección "Revisión del protocolo" de la hoja mientras tanto.

## 6. Después de las 3 sesiones
1. Revisar que ninguna hoja tenga nombres, solo P1, P2 y P3.
2. Transcribir cada hoja a `resultados/P1.md`, `resultados/P2.md` y `resultados/P3.md`, con los datos tal cual (sin redondear ni corregir).
3. Calcular el resumen del pilotaje y el SUS de cada participante.
4. Llenar la sección 12 del plan con lo observado y los ajustes (versión 1 → versión 2).
5. Los videos se guardan en la carpeta privada del grupo y **no se suben a GitHub**.

## 7. Tiempo total estimado
| Bloque | Duración |
|---|---|
| Ensayo interno | 20 min |
| 3 sesiones × 15 min | 45 min |
| Reinicios | 3 min |
| **Total** | **algo más de 1 hora** |
