# Preguntas: exposición, defensa y debate

## 1. Pregunta inicial para la clase

> **¿Una interfaz que funciona técnicamente puede ser una mala interfaz?**

**Propósito:** activar la distinción entre **verificación** (el sistema cumple su especificación) y **validación** (el sistema permite a sus usuarios lograr sus objetivos).

**Respuesta argumentada:** sí. Que una interfaz "funcione" solo demuestra que cumple su especificación técnica. La usabilidad, según ISO 9241-11, se mide por la eficacia, la eficiencia y la satisfacción de usuarios concretos en un contexto concreto. Un sistema sin fallos técnicos puede hacer que el usuario:
- no encuentre una función que sí existe (problema de eficacia);
- tarde demasiado o cometa errores evitables (problema de eficiencia);
- termine la tarea con frustración o inseguridad (problema de satisfacción).

**Ejemplos para la discusión:**
- Un formulario que valida correctamente los datos, pero borra todos los campos cuando muestra un error.
- Un botón que ejecuta bien su acción, pero cuya etiqueta no describe lo que hace.
- Un sistema que guarda correctamente una acción, pero no muestra ninguna confirmación, por lo que el usuario la repite.

**Cierre sugerido:** CaféU funciona: navega, calcula totales y genera el número de pedido (verificación). Al terminar el laboratorio, retomar la pregunta y responderla con la evidencia: el aviso "Producto agregado al pedido" **existe y se ejecuta**, pero **6 de 6 participantes no lo vieron** porque quedaba desplazado y cortado en el borde derecho. Funciona técnicamente y aun así falla en usabilidad (corregido en el Issue #10).

---

## 2. Preguntas técnicas que nos pueden hacer (docente o clase)

### T1. ¿Cuántos usuarios probaron y por qué es suficiente?

**Respuesta sugerida:** en el pilotaje probamos con 3 participantes (P1, P2 y P3). Nuestro estudio es **formativo** y, además, es un **pilotaje**: busca validar el protocolo y descubrir problemas, no certificar estadísticamente el prototipo CaféU. Según Nielsen y Landauer (1993), alrededor de cinco usuarios bastan para detectar la mayoría de los problemas frecuentes en este tipo de estudio. Reconocemos dos límites. Primero, Faulkner (2003) mostró una alta variabilidad entre muestras pequeñas. Segundo, nuestras métricas cuantitativas son **descriptivas** y no generalizables; un estudio sumativo requeriría alrededor de 20 participantes. Por eso no afirmamos porcentajes poblacionales y combinamos la prueba con una evaluación heurística, que no depende del tamaño de la muestra de usuarios.

**Evidencia a mostrar:** dos rondas de 3 participantes. La ronda 2 (P4 a P6) son estudiantes universitarios que no conocían CaféU; la ronda 1 no cumplía el perfil y sirvió para ajustar el protocolo. El problema del aviso al agregar se repitió en **6 de 6** participantes y el uso de "Agregar" dos veces en lugar de "+" en **3 de 6**.

### T2. ¿Por qué eligieron la evaluación heurística y la prueba con usuarios, y no otros métodos?

**Respuesta sugerida:** porque se complementan. La heurística es un método **analítico**: cubre toda la interfaz y explica qué principio se viola. La prueba con usuarios es un método **empírico**: confirma si el problema afecta a usuarios reales y mide su impacto. Otros métodos tienen requisitos que no se ajustan a nuestro alcance. El A/B testing requiere dos versiones en producción y mucho tráfico. El eye tracking requiere equipo especializado. El recorrido cognitivo se centra en la facilidad de aprendizaje de flujos concretos, que la prueba con usuarios ya cubre de forma empírica.

### T3. ¿Cómo calcularon el SUS y cómo lo interpretan con tan pocos participantes?

**Respuesta sugerida:** aplicamos el procedimiento estándar de Brooke (1996): impares = puntaje − 1; pares = 5 − puntaje; suma × 2,5, con un rango de 0 a 100. El puntaje no es un porcentaje. Lo comparamos con el promedio de referencia de aproximadamente 68 (Sauro y Lewis, 2016). Tullis y Stetson (2004) reportan que el SUS se estabiliza con alrededor de 12–14 participantes; con nuestra muestra lo interpretamos como un indicador y no como una medida concluyente.

**Evidencia a mostrar:** ronda 2: 90,0 · 95,0 · 87,5 (media 90,8). Ronda 1: 50,0 · 95,0 · 92,5 (media 79,2). El SUS de 50 de P1 (mayor de 50 años, poca experiencia con apps) muestra por qué no se debe mezclar perfiles sin declararlo. Versión usada: traducción del grupo a partir de Brooke (1996); la versión validada en español es la de Sevilla-González et al. (2020).

### T4. ¿Cómo definieron qué es "éxito" y qué es "error"?

**Respuesta sugerida:** los definimos **antes** de la prueba para no ajustarlos a los resultados. **Éxito:** cada tarea tiene un estado final observable (por ejemplo, en T4 se ve "¡Pedido confirmado!" con 2 cafés por $3,00 y el usuario dice #CU-104), y solo cuenta si lo logra sin ayuda; ver [03-tareas.md](../evidencias/03-tareas.md). **Error:** toda acción que no acerca al resultado esperado, como entrar a un producto equivocado o buscar sin resultados. Distinguimos los errores críticos (impiden completar la tarea) de los no críticos (el usuario se recupera).

### T5. Si usaron pensamiento en voz alta, ¿eso no altera el tiempo en tarea?

**Respuesta sugerida:** sí, verbalizar tiende a alargar los tiempos. Lo usamos **en todas las sesiones por igual**, así que los tiempos son comparables entre participantes, pero no con un uso real en la cafetería. Lo declaramos como limitación y por eso las metas (60 a 90 s) dejan margen frente a los 17 a 26 s observados en el APE 4.

### T6. ¿La severidad no es subjetiva?

**Respuesta sugerida:** la severidad implica juicio; por eso la sistematizamos. (1) Usamos criterios explícitos de frecuencia, impacto y persistencia (Nielsen, 1995). (2) Cada evaluador calificó por separado antes de consolidar, para reducir el efecto evaluador (Hertzum y Jacobsen, 2001). (3) Cada calificación está vinculada a su evidencia: la heurística violada y, cuando existe, la proporción de usuarios afectados y el efecto observado en las métricas.

### T7. ¿Cómo saben que las tareas son representativas del uso real?

**Respuesta sugerida:** las seis tareas cubren lo que un estudiante hace en CaféU: consultar información (horario en T1, productos por categoría en T5, precio por cantidad en T6) y armar, modificar y confirmar un pedido (T2, T3 y T4). El pilotaje aplica las seis: T2 a T4 son el recorrido central (y se parecen a las que se probaron en el APE 4 con la versión v3, lo que permite comparar), y T1, T5 y T6 son las que hará la clase, así que también se validan antes. Reconocemos que la prueba solo observa lo que las tareas recorren; por eso la evaluación heurística amplía la cobertura al resto de la interfaz.

### T9. ¿Por qué evaluaron CaféU y no el Usability Test Dashboard 2.0?

**Respuesta sugerida:** porque la matriz pide evaluar **el prototipo** del proyecto, y la cadena de los APE es APE 4 (prototipo de CaféU en Figma) → APE 5 (paso a HTML) → APE 6 (evaluación de ese prototipo con usuarios). Al revisar los APE anteriores corregimos el rumbo y lo dejamos documentado en el Issue #9. Eso también es parte del método: validar que evaluamos el objeto correcto antes de recoger datos.

### T10. ¿Por qué no presentan el backlog priorizado?

**Respuesta sugerida:** porque al G5 le corresponden las Fases 1 y 2 (planificación y pilotaje). La severidad final, la triangulación y el backlog priorizado son las Fases 3 y 4, que construye el G6 con nuestros datos y nuestras evaluaciones heurísticas.

### T8. Si la heurística y los usuarios no coinciden, ¿a quién le creen?

**Respuesta sugerida:** a ninguno de forma automática; clasificamos la evidencia. Un hallazgo confirmado por ambos métodos tiene la evidencia más fuerte. Un hallazgo solo heurístico se presenta como problema potencial, y declaramos que no se observó en usuarios. Un hallazgo solo observado en usuarios es un problema real que la inspección no anticipó. Esta triangulación evita tanto los falsos positivos de la inspección como la cobertura limitada de la prueba.

---

## 3. Objeciones probables y respuestas sugeridas

### O1. "¿Qué evidencia tienen de que este problema es realmente grave?"

**Respuesta sugerida:** la severidad no es una opinión; se sustenta en tres elementos verificables:
1. **Frecuencia:** el aviso al agregar no lo percibieron **6 de 6** participantes, y **4 de 4** evaluadores lo marcaron.
2. **Impacto:** no impidió completar la tarea (por eso no es crítico), pero generó duda ("¿Y ahora cómo sé que ya se puso?") y en P1 una verificación extra en "Mi pedido".
3. **Principio violado:** heurística 1, visibilidad del estado del sistema, y es consistente con lo observado: los usuarios se guiaron solo por el contador.

Si un problema no tiene evidencia de usuarios, lo declaramos como potencial y su severidad se justifica únicamente por la heurística.

### O2. "Los participantes son compañeros de clase; la muestra está sesgada."

**Respuesta sugerida:** los participantes son estudiantes que no diseñaron CaféU ni participaron en la prueba del APE 4, por lo que no conocen el flujo de memoria como el equipo. Además, son usuarios reales del contexto: estudiantes que usan la cafetería universitaria. Reconocemos que comparten carrera y nivel de experiencia con nosotros, así que los resultados no se generalizan a otros perfiles. Lo declaramos como limitación y proponemos ampliar la muestra a otras carreras o a docentes.

### O3. "Ustedes no son expertos en usabilidad; la evaluación heurística no es válida."

**Respuesta sugerida:** la experiencia de los evaluadores sí afecta la cantidad de problemas detectados. Por eso (1) usamos varios evaluadores que trabajaron por separado, (2) aplicamos criterios definidos en lugar de impresiones y (3) contrastamos los hallazgos con la prueba con usuarios, que no depende de la experiencia de los evaluadores.

### O4. "En un laboratorio la gente no se comporta como en la vida real."

**Respuesta sugerida:** es una limitación conocida de la prueba de usabilidad; la presencia de observadores puede alterar el comportamiento. Para mitigarla, el moderador no ayuda durante las tareas (solo una pista definida de antemano), las tareas se plantean como situaciones reales de la cafetería y se usa el prototipo publicado y navegable, no imágenes estáticas. Aun así, es un prototipo y no hay pago ni retiro reales; lo declaramos en las limitaciones.

### O5. "Eso es cuestión de gusto, no un problema de usabilidad."

**Respuesta sugerida:** no reportamos preferencias. Un hallazgo entra en el backlog solo si se relaciona con una heurística o con un efecto observable en las métricas. Los problemas puramente estéticos sin impacto en la tarea se clasifican como cosméticos.

### O6. "Nosotros lo usamos sin problema; si funciona, no hay nada que corregir."

**Respuesta sugerida:** quien construye una interfaz la conoce de memoria y no puede juzgar su claridad. Que el equipo la use sin problema no demuestra que un evaluador nuevo pueda hacerlo. Esa es la diferencia entre verificación y validación. Además, la costumbre oculta costos de eficiencia (tiempo, errores) que solo aparecen con usuarios nuevos, y la **persistencia** es un factor de severidad: un problema que sigue molestando incluso a usuarios que ya lo conocen es más grave, no menos.

### O7. "¿Para qué sirve el backlog si ustedes mismos pueden corregir todo?"

**Respuesta sugerida:** porque los recursos del equipo son limitados y no todo se corrige a la vez. El backlog documenta cada problema con su severidad y su evidencia de forma trazable, y permite decidir qué corregir primero (los críticos y mayores) y qué dejar para después (los cosméticos). Cada hallazgo queda como Issue de GitHub, con responsable y estado.

---

## 4. Preguntas para el debate con la clase

1. Si una interfaz obtiene un buen puntaje SUS pero una baja tasa de éxito, ¿es usable? ¿Qué métrica pesa más y por qué?
2. ¿Puede un problema "cosmético" volverse grave si afecta a miles de estudiantes todos los días?
3. ¿Quién debería decidir la severidad de un problema: los evaluadores, los usuarios o los datos?
4. ¿Es ético evaluar una aplicación con participantes sin su consentimiento informado? ¿Qué hicimos nosotros para cuidarlo?
5. ¿Qué diferencia hay entre "el usuario se equivocó" y "la interfaz indujo el error"?
6. ¿Qué cambiaría en los resultados si los participantes fueran estudiantes de primer semestre en lugar de estudiantes avanzados?

---

## 5. Preguntas del G5 como grupo QA/UX retador (a G1 y G4)

Cada pregunta trae la **respuesta esperada** (lo que debería contener una buena respuesta) y una **repregunta** por si la respuesta es débil. Todas piden evidencia, no opiniones.

### Al G1 · Emoción y experiencia de usuario (curva emocional, momentos de verdad y mejoras)

**Técnica 1 · Pregunta:** "¿Cómo midieron la emoción en cada touchpoint de la curva? ¿La reportó el usuario, por ejemplo con una escala, o la estimó el equipo? ¿Con cuántos usuarios?"
- **Respuesta esperada:** la emoción la **reportaron usuarios reales** en cada touchpoint con un instrumento definido (escala de 1 a 5, caritas o la escala SAM), más lo que se observó o dijeron en voz alta. Indican cuántos usuarios participaron y aclaran que, si fueron pocos, la curva es indicativa.
- **Respuesta débil:** "la curva la hicimos según lo que creemos que siente el usuario".
- **Repregunta:** "Entonces la curva es una hipótesis del equipo. ¿Qué dato de un usuario real respalda el punto más bajo de la curva?"

**Técnica 2 · Pregunta:** "¿Qué criterio usaron para decidir que un touchpoint es un **momento de verdad** y no un punto más de la curva?"
- **Respuesta esperada:** un momento de verdad es el punto donde el usuario **decide si confía, continúa o abandona** (por ejemplo, el pago o la confirmación del pedido). Lo identificaron por su impacto en la decisión y por la variación emocional (los picos o caídas más fuertes), no solo por ser un paso del flujo.
- **Respuesta débil:** "son los pasos más importantes".
- **Repregunta:** "¿Qué pasa con el usuario si ese momento sale mal: abandona, se equivoca o pide ayuda? ¿Lo observaron?"

**Objeción:** "Ustedes muestran una curva de 'después' con emociones más positivas. Pero si esa curva la construyó el mismo equipo que diseñó la mejora, es una **predicción**, no una evidencia. ¿Volvieron a probar la versión mejorada con usuarios reales?"
- **Respuesta esperada:** reconocen la diferencia entre **predicción y evidencia**. Lo ideal es que hayan repetido la prueba con usuarios en la versión mejorada y comparen la misma métrica antes y después. Si no lo hicieron, lo declaran como limitación y proponen esa prueba como siguiente paso.
- **Respuesta débil:** "se ve claramente que la nueva versión es mejor".
- **Repregunta:** "¿Con qué métrica compararían el antes y el después para demostrarlo: tiempo, errores, satisfacción?"

### Al G4 · Implementación de interfaces web y móviles (HTML5/CSS, responsive, mobile first)

**Técnica 1 · Pregunta:** "¿Cómo comprobaron que la interfaz es responsive? ¿Solo con capturas en DevTools, o midieron algo concreto, como que no haya desplazamiento horizontal en 320, 360, 768 y 1366 px?"
- **Respuesta esperada:** usaron un **criterio medible**: en cada ancho, `document.documentElement.scrollWidth` es igual a `innerWidth` (0 px de desborde), según el criterio WCAG 1.4.10 (Reflow). Muestran capturas de cada ancho con la medición y explican el punto de quiebre (por ejemplo, 48rem) con mobile first.
- **Respuesta débil:** "lo vimos en el celular y se veía bien".
- **Repregunta:** "¿Cómo sabría otra persona, sin mirar sus capturas, que en 320 px no hay desplazamiento horizontal?"

**Técnica 2 · Pregunta:** "¿Qué criterios de accesibilidad aplicaron (contraste mínimo de 4,5:1, botones de al menos 44 px, navegación con teclado y foco visible) y cómo verificaron cada uno?"
- **Respuesta esperada:** nombran criterios WCAG concretos y cómo los comprobaron: contraste 1.4.3 calculado con una herramienta; tamaño de objetivos táctiles de al menos 44 × 44 px; operación con teclado (2.1.1) recorriendo la pantalla solo con Tab, Enter y Esc; foco visible (2.4.7); HTML semántico y `role="status"` para los mensajes.
- **Respuesta débil:** "usamos colores con buen contraste".
- **Repregunta:** "¿Cuál es la relación de contraste de su texto secundario y con qué la midieron?"

**Objeción:** "Que la interfaz se adapte a todas las pantallas demuestra **verificación**: funciona. Pero no demuestra **validación**. ¿Probaron con usuarios en un celular real si pueden completar la tarea sin ayuda? Sin eso no pueden afirmar que es usable."
- **Respuesta esperada:** aceptan la distinción: lo responsive y accesible es necesario, pero no suficiente. Lo ideal es que muestren una observación con usuarios (tarea, éxito, tiempo y dificultades) en el ancho móvil. Si no la hicieron, lo declaran como limitación y la proponen como siguiente paso.
- **Respuesta débil:** "si se ve bien en todas las pantallas, es usable".
- **Repregunta:** "Nosotros encontramos un aviso que funcionaba en el código, pero que 6 de 6 usuarios no vieron. ¿Cómo descartan que a ustedes les pase lo mismo?"

### Reparto sugerido
| Pregunta | Quién la hace |
|---|---|
| G1 · Técnica 1 | Henry Lagua |
| G1 · Técnica 2 | Melany Cevallos |
| G1 · Objeción | Carlos Ramos |
| G4 · Técnica 1 | Allison Cobos |
| G4 · Técnica 2 | Henry Lagua |
| G4 · Objeción | Melany Cevallos |

## 6. Registro de preguntas el día de la exposición

| # | Tipo (técnica / objeción / debate) | Pregunta recibida | Respuesta del grupo | Integrante que respondió |
|---|---|---|---|---|
| 1 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] |
| 2 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] |
| 3 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] |
