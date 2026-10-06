# Marco teórico: evaluación y validación de interfaces

## 1. Evaluación y validación de interfaces

### 1.1 Usabilidad

La norma ISO 9241-11:2018 define la usabilidad como el grado en que un sistema, producto o servicio puede ser usado por usuarios específicos para lograr objetivos específicos con **eficacia**, **eficiencia** y **satisfacción** en un **contexto de uso** específico.

- **Eficacia:** precisión y completitud con que el usuario logra sus objetivos.
- **Eficiencia:** recursos invertidos (tiempo, esfuerzo) en relación con el resultado obtenido.
- **Satisfacción:** respuestas físicas, cognitivas y emocionales del usuario frente al uso.

La definición es relativa: una interfaz no es usable en abstracto, sino para ciertos usuarios, ciertas tareas y cierto contexto. En este proyecto los usuarios son estudiantes de la UTA, las tareas son actividades académicas frecuentes en el aula virtual y el contexto se describe en el README.

### 1.2 Verificación vs. validación

Boehm (1984) resume la diferencia con dos preguntas:

- **Verificación:** ¿estamos construyendo el producto correctamente? (cumple su especificación técnica)
- **Validación:** ¿estamos construyendo el producto correcto? (sirve a las necesidades reales de sus usuarios)

Una interfaz puede superar la verificación (no tiene fallos y hace lo que dice la especificación) y aun así fracasar en la validación (los usuarios no logran sus objetivos o lo hacen con errores, demoras y frustración). Esta distinción sustenta la pregunta inicial de la exposición.

### 1.3 Evaluación formativa vs. sumativa

- **Formativa:** se realiza para descubrir problemas y orientar mejoras. Su producto principal son hallazgos cualitativos.
- **Sumativa:** se realiza para medir o certificar el nivel de usabilidad, a menudo comparándolo con un criterio o con otro sistema. Su producto principal son métricas con validez estadística.

Este proyecto es principalmente **formativo**. Las métricas se usan para describir y respaldar los hallazgos, no para certificar estadísticamente la plataforma.

### 1.4 Métodos analíticos vs. empíricos

- **Analíticos o de inspección:** evaluadores examinan la interfaz con criterios predefinidos, sin usuarios finales. Ejemplos: evaluación heurística, recorrido cognitivo.
- **Empíricos:** se observa a usuarios reales que interactúan con la interfaz. Ejemplos: prueba de usabilidad, A/B testing.

Los métodos analíticos **predicen** problemas; los empíricos los **observan**.

---

## 2. Métricas de usabilidad

| Métrica | Dimensión ISO | Definición | Cálculo | Consideraciones |
|---|---|---|---|---|
| Tasa de éxito | Eficacia | Proporción de intentos en que el usuario completa la tarea según un criterio de éxito definido de antemano. | (tareas completadas / tareas intentadas) × 100 | Definir el criterio de éxito antes de la prueba. Con muestras pequeñas conviene reportar un intervalo de confianza; Sauro y Lewis (2016) recomiendan el intervalo de Wald ajustado. |
| Tiempo en tarea | Eficiencia | Tiempo desde que el usuario inicia la tarea hasta que la completa o la abandona. | Mediana o media geométrica por tarea | Los tiempos suelen tener una distribución sesgada; con muestras pequeñas, Sauro y Lewis (2016) recomiendan la media geométrica. Hay que decidir de antemano si se incluyen los tiempos de las tareas fallidas. El protocolo de pensamiento en voz alta tiende a alargar los tiempos. |
| Errores | Eficacia / eficiencia | Acción incorrecta o desviación de la ruta que conduce al objetivo. | Conteo por tarea y por participante | Definir operacionalmente qué cuenta como error antes de la prueba. Distinguir los errores **críticos** (impiden completar la tarea) de los **no críticos** (el usuario se recupera). |
| Satisfacción (SUS) | Satisfacción | Percepción global de usabilidad medida con el System Usability Scale. | Ver 2.1 | Mide la percepción, no el desempeño, y puede divergir de las métricas objetivas. |

### 2.1 System Usability Scale (SUS)

El SUS (Brooke, 1996) es un cuestionario de 10 ítems con escala Likert de 5 puntos (1 = totalmente en desacuerdo, 5 = totalmente de acuerdo). Los ítems impares tienen redacción positiva y los pares, negativa.

**Cálculo:**
1. Ítems impares: puntaje del ítem − 1.
2. Ítems pares: 5 − puntaje del ítem.
3. Sumar los 10 valores resultantes (rango 0–40).
4. Multiplicar la suma por 2,5 (rango 0–100).

**Interpretación:**
- El puntaje **no es un porcentaje**. Un SUS de 68 no significa "68 % usable".
- El promedio de referencia reportado en la literatura es de aproximadamente **68** (Sauro y Lewis, 2016). Bangor, Kortum y Miller (2009) proponen además una escala adjetiva (p. ej., "aceptable", "bueno", "excelente") para facilitar la interpretación.
- Tullis y Stetson (2004) observaron que el SUS produce resultados consistentes con muestras relativamente pequeñas (alrededor de 12–14 participantes). Con menos participantes, el puntaje debe interpretarse como indicativo.
- Si se aplica una versión en español, debe declararse su fuente: [COMPLETAR].

---

## 3. Las 10 heurísticas de Nielsen

Nielsen y Molich (1990) propusieron la evaluación heurística, y Nielsen (1994) refinó el conjunto de heurísticas a partir del análisis factorial de 249 problemas de usabilidad.

| # | Heurística | Descripción | Ejemplo de pregunta guía (genérica para un aula virtual) |
|---|---|---|---|
| 1 | Visibilidad del estado del sistema | El sistema mantiene informado al usuario sobre lo que ocurre, con retroalimentación oportuna. | ¿El estudiante sabe si una acción que realizó se completó correctamente? |
| 2 | Coincidencia entre el sistema y el mundo real | Usa el lenguaje y los conceptos del usuario, no jerga técnica, y sigue convenciones del mundo real. | ¿Los términos de la interfaz corresponden a los que usa un estudiante? |
| 3 | Control y libertad del usuario | Ofrece "salidas de emergencia" claras para deshacer o abandonar acciones no deseadas. | ¿Puede cancelar o corregir una acción sin perder trabajo? |
| 4 | Consistencia y estándares | Elementos iguales se ven y se comportan igual, y se siguen las convenciones de la plataforma y de la industria. | ¿La estructura y los controles son coherentes entre secciones o cursos? |
| 5 | Prevención de errores | Evitar que el error ocurra es mejor que un buen mensaje de error: se eliminan las condiciones propensas a error o se pide confirmación. | ¿Se advierte antes de una acción irreversible? |
| 6 | Reconocer antes que recordar | Se minimiza la carga de memoria haciendo visibles los elementos, las acciones y las opciones. | ¿La interfaz muestra la información o el usuario debe recordar dónde estaba? |
| 7 | Flexibilidad y eficiencia de uso | Ofrece aceleradores para usuarios expertos sin perjudicar a los novatos. | ¿Hay accesos directos a lo que se usa con más frecuencia? |
| 8 | Diseño estético y minimalista | No incluye información irrelevante; cada elemento extra compite con el relevante. | ¿La información prioritaria se distingue de la secundaria? |
| 9 | Ayudar a reconocer, diagnosticar y recuperarse de errores | Los mensajes de error usan lenguaje claro, indican el problema y sugieren una solución. | ¿El mensaje de error explica qué pasó y qué hacer? |
| 10 | Ayuda y documentación | Si se necesita ayuda, es fácil de encontrar, está centrada en la tarea y ofrece pasos concretos. | ¿Existe ayuda accesible en el punto donde se necesita? |

---

## 4. Escala de severidad

Nielsen (1995) propone calificar la severidad de cada problema según tres factores:

- **Frecuencia:** ¿es común o raro? En la prueba con usuarios se expresa como la proporción de participantes afectados (x/n).
- **Impacto:** ¿el usuario puede superarlo fácilmente o le impide avanzar?
- **Persistencia:** ¿se supera una vez o molesta repetidamente aunque el usuario ya lo conozca?

La escala original va de 0 a 4 (0 = no es un problema de usabilidad). Este proyecto usa los niveles 1–4:

| Nivel | Valor | Criterio operativo | Prioridad |
|---|---|---|---|
| Cosmético | 1 | No afecta la realización de la tarea; es un detalle visual o de redacción. | Corregir si hay recursos disponibles. |
| Menor | 2 | Causa vacilación, demora leve o errores de los que el usuario se recupera solo. | Baja. |
| Mayor | 3 | Causa errores significativos o demoras importantes, requiere ayuda externa o hace que algunos usuarios no completen la tarea. | Alta. |
| Crítico | 4 | Impide completar una tarea clave o puede tener consecuencias graves para el estudiante. | Imperativo corregir. |

Para reducir la subjetividad:
1. Cada evaluador asigna la severidad por separado, sin conocer las calificaciones de los demás.
2. Se consolida por promedio o por consenso argumentado.
3. Cada calificación se vincula a su evidencia: la heurística violada y, cuando existe, la observación en la prueba con usuarios.

---

## 5. Métodos de evaluación elegidos

### 5.1 Evaluación heurística de Nielsen

**Qué es:** un método de inspección en el que varios evaluadores examinan la interfaz por separado contra las 10 heurísticas y registran cada violación con su ubicación, la heurística afectada y la severidad.

**Número de evaluadores:** Nielsen reporta que un solo evaluador encuentra en promedio alrededor del 35 % de los problemas y que con cinco evaluadores se llega aproximadamente al 75 %. Por eso se recomiendan de 3 a 5 evaluadores que trabajen por separado.

**Fortalezas:** rápida, de bajo costo, no requiere usuarios y cubre toda la interfaz, incluidas zonas que las tareas de la prueba no recorren.

**Limitaciones:**
- Puede producir **falsos positivos**, es decir, problemas previstos que los usuarios reales no experimentan.
- Está sujeta al **efecto evaluador** (Hertzum y Jacobsen, 2001): distintos evaluadores detectan problemas distintos y califican la severidad de forma diferente.
- Su calidad depende de la experiencia de los evaluadores.

### 5.2 Prueba de usabilidad con usuarios

**Qué es:** un método empírico en el que participantes representativos realizan tareas reales mientras se observa su comportamiento y se registran métricas. Puede incluir el protocolo de **pensamiento en voz alta**, en el que el participante verbaliza lo que piensa mientras trabaja (Rubin y Chisnell, 2008).

**Número de participantes:** según el modelo de Nielsen y Landauer (1993), cinco usuarios detectan aproximadamente el 85 % de los problemas de una interfaz en un estudio **formativo** y **cualitativo**, bajo el supuesto de que cada usuario encuentra en promedio el 31 % de los problemas. Este supuesto ha sido cuestionado: Faulkner (2003) mostró una alta variabilidad entre muestras de cinco usuarios. Para estudios **cuantitativos** con métricas comparables se requieren muestras mayores (Nielsen recomienda alrededor de 20).

**Fortalezas:** ofrece evidencia directa del comportamiento real; permite medir eficacia, eficiencia y satisfacción; revela problemas que los expertos no anticipan.

**Limitaciones:**
- Las tareas definidas acotan lo que se observa.
- El entorno de laboratorio y la presencia de observadores pueden alterar el comportamiento.
- Con muestras pequeñas, las métricas son descriptivas y no generalizables.

### 5.3 Por qué los dos métodos se complementan

| Aspecto | Evaluación heurística | Prueba con usuarios |
|---|---|---|
| Fuente de evidencia | Juicio experto con criterios | Comportamiento observado |
| Tipo de resultado | Problemas previstos | Problemas confirmados y métricas |
| Cobertura | Toda la interfaz | Solo las tareas probadas |
| Riesgo principal | Falsos positivos | Problemas fuera del alcance de las tareas |
| Explica el "por qué" | Sí (principio violado) | Parcialmente (lo que el usuario dice y hace) |

La combinación permite **triangular** la evidencia:

- **Hallazgo detectado por ambos métodos:** evidencia más fuerte. La heurística explica el principio violado y la prueba demuestra el impacto real.
- **Hallazgo solo heurístico:** es un problema potencial. Su severidad se justifica por el principio violado y debe declararse que no fue observado.
- **Hallazgo solo en la prueba con usuarios:** es un problema real que la inspección no anticipó. Se analiza qué heurística, si alguna, lo explica.

Así, la heurística aporta el **diagnóstico** y la prueba con usuarios aporta la **evidencia de impacto**. Juntas permiten defender la severidad de cada hallazgo con datos y principios, no con opiniones.

---

## Referencias

- Bangor, A., Kortum, P. y Miller, J. (2009). Determining what individual SUS scores mean: Adding an adjective rating scale. *Journal of Usability Studies, 4*(3), 114–123.
- Boehm, B. W. (1984). Verifying and validating software requirements and design specifications. *IEEE Software, 1*(1), 75–88.
- Brooke, J. (1996). SUS: A "quick and dirty" usability scale. En P. W. Jordan, B. Thomas, B. A. Weerdmeester y I. L. McClelland (Eds.), *Usability Evaluation in Industry* (pp. 189–194). Taylor & Francis.
- Faulkner, L. (2003). Beyond the five-user assumption: Benefits of increased sample sizes in usability testing. *Behavior Research Methods, Instruments, & Computers, 35*(3), 379–383.
- Hertzum, M. y Jacobsen, N. E. (2001). The evaluator effect: A chilling fact about usability evaluation methods. *International Journal of Human-Computer Interaction, 13*(4), 421–443.
- ISO 9241-11:2018. *Ergonomics of human-system interaction — Part 11: Usability: Definitions and concepts.*
- Nielsen, J. (1993). *Usability Engineering.* Academic Press.
- Nielsen, J. (1994). Enhancing the explanatory power of usability heuristics. *Proceedings of CHI '94*, 152–158.
- Nielsen, J. (1995). *Severity ratings for usability problems.* Nielsen Norman Group.
- Nielsen, J. y Landauer, T. K. (1993). A mathematical model of the finding of usability problems. *Proceedings of INTERCHI '93*, 206–213.
- Nielsen, J. y Molich, R. (1990). Heuristic evaluation of user interfaces. *Proceedings of CHI '90*, 249–256.
- Rubin, J. y Chisnell, D. (2008). *Handbook of Usability Testing* (2.ª ed.). Wiley.
- Sauro, J. y Lewis, J. R. (2016). *Quantifying the User Experience: Practical Statistics for User Research* (2.ª ed.). Morgan Kaufmann.
- Tullis, T. S. y Stetson, J. N. (2004). A comparison of questionnaires for assessing website usability. *Usability Professionals Association Conference.*
