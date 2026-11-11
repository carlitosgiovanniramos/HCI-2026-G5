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

**Cierre sugerido:** CaféU funciona: navega, calcula totales y genera el número de pedido (verificación). Al terminar el laboratorio, retomar la pregunta y responderla con la evidencia obtenida en la validación con estudiantes nuevos: [COMPLETAR después del pilotaje: hallazgo concreto que ilustre la respuesta].

---

## 2. Preguntas técnicas probables del grupo QA/UX retador

### T1. ¿Cuántos usuarios probaron y por qué es suficiente?

**Respuesta sugerida:** en el pilotaje probamos con 3 participantes (P1, P2 y P3). Nuestro estudio es **formativo** y, además, es un **pilotaje**: busca validar el protocolo y descubrir problemas, no certificar estadísticamente el prototipo CaféU. Según Nielsen y Landauer (1993), alrededor de cinco usuarios bastan para detectar la mayoría de los problemas frecuentes en este tipo de estudio. Reconocemos dos límites. Primero, Faulkner (2003) mostró una alta variabilidad entre muestras pequeñas. Segundo, nuestras métricas cuantitativas son **descriptivas** y no generalizables; un estudio sumativo requeriría alrededor de 20 participantes. Por eso no afirmamos porcentajes poblacionales y combinamos la prueba con una evaluación heurística, que no depende del tamaño de la muestra de usuarios.

**Evidencia a mostrar:** 3 estudiantes que no diseñaron CaféU ni participaron en la prueba del APE 4; [COMPLETAR después del pilotaje: problemas que se repitieron entre participantes].

### T2. ¿Por qué eligieron la evaluación heurística y la prueba con usuarios, y no otros métodos?

**Respuesta sugerida:** porque se complementan. La heurística es un método **analítico**: cubre toda la interfaz y explica qué principio se viola. La prueba con usuarios es un método **empírico**: confirma si el problema afecta a usuarios reales y mide su impacto. Otros métodos tienen requisitos que no se ajustan a nuestro alcance. El A/B testing requiere dos versiones en producción y mucho tráfico. El eye tracking requiere equipo especializado. El recorrido cognitivo se centra en la facilidad de aprendizaje de flujos concretos, que la prueba con usuarios ya cubre de forma empírica.

### T3. ¿Cómo calcularon el SUS y cómo lo interpretan con tan pocos participantes?

**Respuesta sugerida:** aplicamos el procedimiento estándar de Brooke (1996): impares = puntaje − 1; pares = 5 − puntaje; suma × 2,5, con un rango de 0 a 100. El puntaje no es un porcentaje. Lo comparamos con el promedio de referencia de aproximadamente 68 (Sauro y Lewis, 2016). Tullis y Stetson (2004) reportan que el SUS se estabiliza con alrededor de 12–14 participantes; con nuestra muestra lo interpretamos como un indicador y no como una medida concluyente.

**Evidencia a mostrar:** [COMPLETAR después del pilotaje: puntaje SUS de P1, P2 y P3 y promedio]. Versión usada: traducción del grupo a partir de Brooke (1996); la versión validada en español es la de Sevilla-González et al. (2020).

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
1. **Frecuencia:** [COMPLETAR: x de n participantes lo experimentaron].
2. **Impacto:** [COMPLETAR: efecto en tasa de éxito, tiempo o errores; p. ej., si impidió completar la tarea].
3. **Principio violado:** [COMPLETAR: heurística de Nielsen] y su consistencia con lo observado.

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

## 5. Registro de preguntas recibidas el día de la exposición

| # | Tipo (técnica / objeción / debate) | Pregunta recibida | Respuesta del grupo | Integrante que respondió |
|---|---|---|---|---|
| 1 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] |
| 2 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] |
| 3 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] |
