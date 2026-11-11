# Encuesta final del proyecto de Maude — versión para Moodle (Campus Virtual) o Google Forms

Curso 2026/27 · Auditoría, Calidad y Fiabilidad Informáticas

---

## Cómo montarla (leer antes de pegar nada)

**1. Actividad y anonimato.** Usa una actividad **Encuesta (Feedback)** del
Campus Virtual con `Registrar nombres de usuario = Anónimo`. No uses
Cuestionario/Quiz: ese guarda intentos identificados.

**2. Es voluntaria y no puntúa.** No hay nota asociada ni tarea de
acreditación: con una encuesta anónima no se puede comprobar quién ha
contestado sin montar una segunda actividad, y no compensa.

**3. Cómo conseguir que la contesten, entonces.** Reserva los últimos 10--15
minutos de la sesión del 17 de diciembre, después de las defensas, y que la
rellenen allí mismo antes de irse. Es lo que de verdad sube la tasa de
respuesta; unas décimas no lo hacen. Con 7 grupos, una encuesta abierta y
voluntaria fuera de clase puede quedarse en la mitad de respuestas, y con esa
n los resultados no sostienen gran cosa.

> Si la pasas en clase, la versión en papel (el PDF) es preferible a la de
> Moodle: sin cuenta ni marca de tiempo, el anonimato del bloque F se ve, no
> hay que creérselo. Recoge en una carpeta y dilo en voz alta: «no las miro
> hasta que estén las actas».

**4. Tipos de pregunta.** En los bloques Likert (C, D, E) usa
**«Opción múltiple (valorada)»** en vez de «Opción múltiple»: escribiendo las
opciones como `1/Totalmente en desacuerdo`, `2/En desacuerdo`… Moodle te
calcula medias directamente y te ahorra el recuento manual.

**5. El bloque de porcentajes (pregunta 6)** no tiene equivalente directo:
móntalo como cinco preguntas numéricas (rango 0–100) o como una sola pregunta
de texto corto. Cinco numéricas se analizan mucho mejor.

**6. Consentimiento.** Los dos párrafos iniciales van como elemento
**«Etiqueta»** al principio. No los quites: el uso de las respuestas en una
publicación necesita que estén informados y que puedan negarse (pregunta 47).
Con n pequeña y respuestas que se publicarán sin agregar, revisa las abiertas
antes de citarlas: una frase puede identificar a su autor aunque no lleve
nombre.

---

## Texto de cabecera (pegar como Etiqueta)

**Antes de empezar.** Esta encuesta es **anónima** y **voluntaria**: no
puntúa, no se sabe quién la ha contestado y no influye en tu nota ni en la de
nadie. Se tarda unos 10 minutos. Este año la asignatura se ha evaluado de una
forma distinta a la habitual, y lo que respondáis aquí es lo único que permite
saber si el cambio ha merecido la pena o hay que deshacerlo. Contestad con
calma y sin adornar nada: una respuesta crítica es más útil que una amable.

**Uso de los datos.** Las respuestas podrán publicarse en un artículo sobre
el rediseño de la asignatura, incluidas respuestas individuales y citas
literales de las preguntas abiertas. No se publicará tu nombre ni ningún dato
que permita identificarte. Si prefieres que tus respuestas no se usen con ese
fin, marca la casilla de la última pregunta.

---

## A. Contexto

**1.** ¿De cuántas personas era tu equipo? · *[opción múltiple, una respuesta]*

```
Dos
Tres
```

**2.** El sistema que modelasteis lo elegisteis: · *[opción múltiple, una respuesta]*

```
De la lista del enunciado
Lo propusimos nosotros
```

**3.** ¿Cuánto conocías ese sistema antes de empezar el proyecto? · *[opción múltiple valorada]*

```
1/Nada
2/Había oído hablar de él
3/Lo había usado o estudiado por encima
4/Lo conocía bien
```

**4.** (Opcional) ¿Qué sistema modelasteis? · *[texto corto, no obligatoria]*

> Añade como texto de ayuda: «Puedes dejarlo en blanco: si tu equipo fue
> el único que eligió ese sistema, responder aquí permite identificarlo
> (aunque no a ti dentro de él).»

---

## B. Dedicación

**5.** Aproximadamente, ¿cuántas horas en total dedicaste al proyecto fuera de clase? · *[opción múltiple valorada]*

```
1/Menos de 10
2/10-19
3/20-29
4/30-39
5/40 o más
```

**6.** ¿Qué porcentaje de ese tiempo dedicaste a cada tarea? (debería sumar 100) · *[cinco preguntas numéricas, 0–100]*

```
6a. Entender el sistema real (documentación, artículos, código)
6b. Escribir y depurar la especificación en Maude
6c. Formular y verificar las propiedades (search, LTL)
6d. Mutaciones
6e. Redactar la memoria y preparar la defensa
```

**7.** Comparado con lo que esperabas al leer el enunciado, la carga de trabajo real fue: · *[opción múltiple valorada]*

```
1/Mucho menor
2/Menor
3/La esperada
4/Mayor
5/Mucho mayor
```

---

## C. Aprendizaje percibido

> Etiqueta previa: «Indica tu grado de acuerdo con cada afirmación.»
> Las siete preguntas usan la misma escala *[opción múltiple valorada]*:
> `1/Totalmente en desacuerdo` · `2/En desacuerdo` ·
> `3/Ni de acuerdo ni en desacuerdo` · `4/De acuerdo` ·
> `5/Totalmente de acuerdo`

```
8.  El proyecto me hizo conectar ideas de la asignatura con conocimientos de otras asignaturas.
9.  Tuve que analizar en profundidad una idea o un mecanismo, no solo aplicar una receta.
10. He aprendido algo que cambió mi forma de entender cómo funcionan los sistemas concurrentes reales.
11. Ahora sé decidir mejor cuándo algo debe ser una ecuación y cuándo una regla.
12. Ahora entiendo mejor qué garantiza y qué no garantiza una verificación formal.
13. Sabría aplicar lo aprendido a un sistema distinto del que modeló mi equipo.
14. Decidir cómo representar el sistema (qué tipos y constructores usar, qué es estado y qué es mensaje) me costó más que escribir las ecuaciones y las reglas.
```

---

## D. Implicación con el proyecto

> Etiqueta previa: «Para cada frase, indica en qué medida te describe.»
> Las ocho preguntas usan la misma escala *[opción múltiple valorada]*:
> `1/No me describe nada` · `2/Me describe poco` ·
> `3/Me describe bastante` · `4/Me describe totalmente`

```
15. En las sesiones dedicadas al proyecto trabajaba concentrado.
16. Dediqué al proyecto más esfuerzo del mínimo necesario para aprobarlo.
17. Disfruté trabajando en el proyecto.
18. Cuando algo no salía, me apetecía insistir hasta entender por qué.
19. El proyecto me pareció aburrido.                       [ítem inverso]
20. Me limité a hacer lo justo para cumplir con el enunciado.   [ítem inverso]
21. He hablado del proyecto con gente de fuera de la asignatura.
22. Me quedé con ganas de seguir mejorando el modelo después de la entrega.
```

**Ojo al analizar:** los ítems 19 y 20 son inversos (miden *desafección*, no
implicación). Con la escala de 4 puntos hay que recodificarlos como `5 − x`
antes de promediarlos con los demás, o bien reportarlos por separado.

---

## E. Comparación con las prácticas cortas del principio de curso

> Etiqueta previa: «Antes del proyecto hicisteis tres prácticas cortas de
> Maude en esta misma asignatura, que no contaban para la nota. Comparado con
> aquellas prácticas, el proyecto me resultó…»
> Las cinco preguntas usan la misma escala *[opción múltiple valorada]*:
> `1/Mucho menos` · `2/Algo menos` · `3/Igual` · `4/Algo más` · `5/Mucho más`

```
23. ...interesante
24. ...exigente
25. ...útil para aprender Maude de verdad
26. ...relacionado con lo que espero hacer profesionalmente
27. ...exigente en cuanto a entender el sistema ANTES de poder escribir código
```

**28.** Si pudieras elegir el formato de evaluación de la asignatura, preferirías: · *[opción múltiple, una respuesta]*

```
Solo prácticas cortas como las del principio de curso
Solo un proyecto en equipo como este
Las dos cosas, como este año
Me da igual
```

---

## F. Asistentes de IA y el MCP para Maude

> Etiqueta previa: «El uso de asistentes de IA en este proyecto estaba
> **permitido**, y el MCP para Maude recomendado, así que aquí no se trata de
> detectar nada: interesa saber
> cómo os han funcionado y, sobre todo, si el MCP para Maude aporta algo que
> un asistente genérico no dé. El bloque es anónimo, como el resto.»

**29.** ¿Con qué frecuencia usaste algún asistente durante el proyecto? · *[opción múltiple valorada]*

```
1/Nunca
2/Puntualmente
3/Con frecuencia
4/Casi continuamente
```

**30.** ¿Cuáles? · *[opción múltiple, VARIAS respuestas]*

```
ChatGPT
Claude
Copilot
Gemini
Otro
```

**31.** ¿Para qué los usaste? · *[opción múltiple, VARIAS respuestas]*

```
Entender el sistema real que íbamos a modelar
Consultar sintaxis de Maude
Explicar mensajes de error del intérprete
Escribir ecuaciones o reglas concretas
Escribir la especificación entera o casi entera
Formular las propiedades (search, LTL)
Interpretar la salida del model checker
Proponer las mutaciones
Redactar partes de la memoria
Otros
```

**32.** ¿Usaste el MCP para Maude (Harold)? · *[opción múltiple valorada]*

```
1/No lo instalé
2/Lo instalé pero apenas lo usé
3/Lo usé a veces
4/Lo usé habitualmente
```

**33.** Si no lo usaste, ¿por qué? · *[texto corto, no obligatoria]*

> En Moodle puedes poner las preguntas 34–38 dentro de una **dependencia** de
> la 32 («mostrar solo si la respuesta es distinta de *No lo instalé*»), para
> que quien no lo usó no tenga que pasar por ellas.

**34.** Instalarlo y ponerlo en marcha fue sencillo: · *[valorada, 1 (nada) – 5 (mucho)]*

**35.** Los diagnósticos que devuelve sobre la especificación me resultaron útiles: · *[valorada, 1 (nada) – 5 (mucho)]*

**36.** Con el MCP, el asistente generaba código Maude más correcto que sin él: · *[valorada, 1 (nada) – 5 (mucho), más `0/No lo puedo comparar`]*

**37.** ¿En qué situaciones te resultó más útil el MCP? · *[texto largo]*

**38.** ¿Qué le falta al MCP o qué le cambiarías? · *[texto largo]*

**39.** Del código Maude que te generó un asistente, ¿cuánto tuviste que rehacer o corregir? · *[opción múltiple valorada]*

```
0/No usé asistentes para el código
1/Nada o casi nada
2/Poco
3/Bastante
4/Casi todo
```

**40.** ¿Entendías todo el código que entregasteis, viniera de donde viniera? · *[opción múltiple valorada]*

```
4/Sí, todo
3/Casi todo
2/Había partes que no acababa de entender
1/Bastantes partes no las entendía
```

**41.** ¿Probasteis a pedirle a un asistente el proyecto entero a partir del enunciado, a ver qué salía? · *[opción múltiple, una respuesta]*

```
No lo probamos
Sí, y no dio nada aprovechable
Sí, y dio algo que hubo que rehacer casi entero
Sí, y funcionó razonablemente bien
```

**42.** Comparado con las prácticas cortas del principio de curso, resolver este proyecto con ayuda de una IA me pareció: · *[opción múltiple valorada]*

```
1/Mucho más fácil
2/Más fácil
3/Igual
4/Más difícil
5/Mucho más difícil
```

**43.** ¿Qué es lo que peor hacen los asistentes en Maude? · *[texto largo]*

---

## G. Para terminar

**44.** ¿Qué es lo mejor del proyecto? ¿Qué mantendrías? · *[texto largo]*

**45.** ¿Qué es lo peor? ¿Qué cambiarías? · *[texto largo]*

**46.** ¿Qué consejo le darías a alguien que empiece este proyecto el curso que viene? · *[texto largo]*

**47.** · *[opción múltiple, una respuesta]*

```
No quiero que mis respuestas se usen en una publicación sobre el diseño de la asignatura.
Sí autorizo ese uso.
```

> En el PDF esta última es una casilla suelta (pregunta 46). En Moodle conviene
> convertirla en dos opciones explícitas y **obligatoria**, para que quien no
> autorice quede registrado sin ambigüedad. Por eso aquí hay 47 preguntas y en
> el PDF 46; el resto de la numeración coincide salvo por la pregunta 33, que
> en el PDF va incrustada en la 32 (el «si no lo usaste, indica por qué»).

---

## Cómo se conectan estas preguntas con el artículo

El artículo es Riesco y Rodríguez-Hortalá, *Modeling Real Systems in Maude:
Making the Declarative Decisions the Assignment* (TFPIE 2027). Las secciones
que se citan abajo son las suyas.

| Afirmación del artículo | Preguntas que la miden |
|---|---|
| Los estudiantes dedican tiempo real al proyecto, y la carga es proporcionada (Sección 7) | 5, 6, 7 |
| El proyecto enseña más que las prácticas cortas | 8–13, 25 |
| Diseñar la representación es la parte difícil (Sección 5) | 11, 14 |
| El rediseño aumenta la implicación | 15–22, 23, 28 |
| La autenticidad del sistema importa | 3, 26 |
| Cómo se usan los asistentes cuando se permiten | 29, 30, 31 |
| El proyecto resiste el atajo con IA | 27, 39–43 |
| El MCP aporta algo sobre un asistente genérico | 32, 34–38 |

El bloque C está adaptado de los ítems de aprendizaje profundo del NSSE y el
bloque D de la escala *Engagement vs. Disaffection with Learning*; son las dos
fuentes que usan Chang et al. (2024), así
que los resultados serán directamente comparables con los suyos. La escala de
4 puntos del bloque D («no me describe nada» … «me describe totalmente») es la
de la validación española de esa escala (Aza et al., HEAd'23,
doi:10.4995/HEAd23.2023.16152).
