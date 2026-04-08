# PANDAMIEN — ANEXO H
## Diseño detallado de la criatura v01
### Derivado del GDD Maestro v06, del Plan de Acción Maestro v05, del Anexo I v01, del Anexo J v01, del Anexo K v01, del Anexo M v01 y del authored de ciclos 1–8

---

## 0. Estado del anexo

Este anexo abre el **Diseño detallado de la criatura** del proyecto.

Su función no es cerrar un “monstruo final” estático, ni diseñar una criatura como enemigo tradicional, ni producir sólo un model sheet bonito. Su función es fijar a la criatura como un **sistema de gestación, organización corporal, temperamento y lenguaje** que:

- nace de decisiones, omisiones, respuestas y contenciones del jugador,
- se alimenta de zonas concretas del apartamento,
- aprende de vínculos humanos, TV, exterioridad y puerta,
- cambia su sociabilidad, agresividad, intimidad y gramática verbal según el historial,
- y deja **espacio escalable** para mecánicas authored o momentos concretos sin romper el canon.

Este anexo responde a una verdad central ya cerrada por el proyecto:

**la criatura será de una manera u otra dependiendo de nuestras decisiones y acciones.**

Eso no significa que “todo valga” ni que haya una combinatoria infinita incontrolable. Significa que el sistema debe producir una criatura:
- variable,
- coherente,
- trazable,
- legible,
- y lo bastante modular como para permitir diferencias reales entre partidas y, a la vez, momentos authored memorables.

---

## 1. Confirmación de principio

Sí: **no te equivocas**.

La criatura **debe** definirse mediante:
- reglas de creación,
- variables acumulativas,
- relaciones entre zonas, vínculos y residuos,
- y estados emergentes que dependan del historial del jugador.

Y también **debe** dejar espacio para:
- mecánicas concretas,
- escenas authored,
- set-pieces puntuales,
- pequeñas excepciones controladas,
- o interacciones especiales según ciclo, umbral o final.

Dicho en limpio:
- **base sistémica obligatoria**,
- **capa authored escalable por encima**.

Si no hacemos eso, pasan dos desastres:
1. o la criatura se vuelve genérica y siempre igual;
2. o el juego se convierte en un caos imposible de producir y balancear.

Este anexo evita ambas cosas.

---

## 2. Principios maestros de diseño de criatura

## 2.1. La criatura no aparece: se organiza
No “spawnea”. No “entra”. No “sale de un susto”.  
Se organiza lentamente a partir de:
- residuos,
- focos no contenidos,
- presión relacional,
- hábitos de evitación,
- y aprendizajes robados al jugador.

## 2.2. La criatura no es una skin
No basta con cambiarle “la forma visual”.  
Una criatura diferente debe notarse en:
- cuerpo,
- sonido,
- trato,
- lenguaje,
- timing,
- relación con la puerta,
- respuesta al jugador,
- y final posible.

## 2.3. La criatura no es libre del sistema
Aunque sea variable, no puede romper la lógica del juego:
- nace del apartamento,
- depende del historial,
- y siempre refleja deuda encarnada.

## 2.4. La criatura es una síntesis
Su resultado depende de cuatro planos que se cruzan:
1. **plano material** — qué zonas y residuos la alimentan,
2. **plano relacional** — de qué voces y tratos aprende,
3. **plano conductual** — cómo la modelan evitación, confrontación y contención,
4. **plano authored** — momentos concretos que el diseño quiera subrayar.

## 2.5. Regla de trazabilidad
Toda manifestación relevante de criatura debe poder explicarse hacia atrás por:
- una zona,
- una deuda,
- una función corporal,
- un patrón de decisión,
- o una mezcla justificada de ellos.

## 2.6. Regla de incompletitud
La criatura puede estar más o menos formada, pero nunca debe sentirse como una “ficha cerrada” demasiado pronto. Su verdad final se paga tarde.

## 2.7. Regla de espacio authored
Habrá huecos previstos para:
- eventos singulares,
- respuestas especiales,
- cortes de ritmo,
- mecánicas de cercanía,
- momentos de escucha,
- momentos de puerta,
- y variantes de confrontación final.

Eso no rompe el sistema.  
Lo usa.

---

## 3. Rol dramático de la criatura

La criatura cumple cinco funciones a la vez:

1. **Inventario corporal de lo no atendido**  
   Es la forma encarnada de la deuda.

2. **Respuesta del apartamento**  
   El piso la organiza y la esconde.

3. **Archivo humano deformado**  
   Aprende del jugador, de sus vínculos y de sus dispositivos.

4. **Interlocutor final potencial**  
   No sólo ataca o aparece: puede tratar, pedir, imitar, exigir o devolver.

5. **Motor de relectura ética**  
   Permite que el final no sea “ganar o perder”, sino leer el historial de la partida como cuerpo.

---

## 4. Estructura general del sistema de criatura

La criatura se define mediante **capas**.

## 4.1. Capa A — Cuerpo material
Responde a qué zonas han sido más contaminadas y cómo.

## 4.2. Capa B — Funciones corporales
Define qué puede hacer o insinuar:
- respirar,
- mirar,
- arrastrarse,
- sostenerse,
- latir,
- articular sonido,
- ensayar sintaxis,
- reclamar contacto,
- presionar el marco,
- ocupar espacio.

## 4.3. Capa C — Temperamento
Define cómo trata al jugador:
- doliente,
- imitativo,
- famélico,
- rencoroso,
- suplicante,
- furioso,
- razonable torcido,
- íntimo intrusivo.

## 4.4. Capa D — Gramática verbal
Define:
- si habla,
- cuánto habla,
- cómo mezcla voces,
- cuánta claridad tiene,
- y qué tipo de interacción dialogada puede sostener.

## 4.5. Capa E — Estado relacional hacia el jugador
Define si la criatura:
- busca,
- acusa,
- pide,
- seduce,
- mide,
- espera,
- castiga,
- convive,
- o negocia.

## 4.6. Capa F — Hooks authored
Slots reservados para:
- eventos especiales,
- mecánicas concretas,
- escenas de fuerte identidad,
- o variaciones de confrontación.

---

## 5. Variables maestras de criatura

Estas variables gobiernan el sistema. No tienen por qué mostrarse al jugador.

## 5.1. Variables de crecimiento corporal

### `creature_mass`
Cuánta entidad física total ha acumulado la criatura.

Uso:
- presión general,
- sensación de presencia,
- densidad sonora,
- capacidad de ocupar el marco.

### `creature_cohesion`
Qué tan organizada está su anatomía.

Baja cohesión:
- masa torpe,
- función aislada,
- ruido sin coordinación.

Alta cohesión:
- combinación de funciones,
- timing,
- presencia más articulada,
- mejor capacidad de trato final.

### `creature_visibility_index`
Qué tan cerca está de pasar de “presencia tras puerta” a “cuerpo asumible”.

Uso:
- staging,
- revelaciones parciales,
- silueta,
- transición al final.

---

## 5.2. Variables funcionales / anatómicas

Cada una puede crecer de 0 a 5 internamente.

### `func_voice`
Asociada a:
- salón,
- editor,
- TV,
- evasión verbal,
- mentira funcional,
- no-respuestas.

Permite:
- sílaba,
- frase rota,
- imitación,
- diálogo parcial.

### `func_eyes`
Asociada a:
- entrada,
- pasillo,
- mirilla,
- ventana,
- vigilancia,
- lectura compulsiva del borde.

Permite:
- orientación,
- mirada,
- foco,
- timing de escucha.

### `func_legs`
Asociada a:
- pasillo,
- trayecto,
- empuje,
- desplazamiento,
- ansiedad de borde,
- presión acumulada.

Permite:
- arrastre,
- golpe de peso,
- amenaza de movimiento,
- embestida final o aproximación.

### `func_stomach`
Asociada a:
- cocina,
- abandono funcional,
- hambre/no hambre,
- banalidad anestesiante,
- digestión de residuos.

Permite:
- gorgoteo,
- bilis,
- masticación,
- hambre afectiva o instrumental.

### `func_skin`
Asociada a:
- baño,
- humedad,
- higiene aplazada,
- costra,
- cuerpo descuidado.

Permite:
- membrana,
- mucosa,
- tejido,
- sudor de pared,
- cercanía blanda repulsiva.

### `func_heart`
Asociada a:
- dormitorio,
- pareja/ex,
- pecho,
- herida íntima,
- espera,
- afecto deformado.

Permite:
- latido,
- súplica,
- espera,
- dolor torácico,
- intimidad monstruosa.

### `func_lungs`
Asociada a:
- balcón,
- aire,
- exposición,
- respiración,
- contagio,
- cuerpo social.

Permite:
- exhalación,
- respiración de rellano,
- expansión del marco,
- relación entre dentro y fuera.

### `func_hands` (opcional / escalable)
Asociada a:
- contención,
- manipulación material,
- tocar marco,
- arrastre de objetos,
- rastro en puerta o props.

Permite:
- marcas,
- presión digital,
- tactilidad authored,
- microinteracción avanzada.

Regla:
- no es obligatoria en MVP,
- pero queda reservada como variable escalable.

---

## 5.3. Variables de temperamento

### `temper_doliente`
Tendencia a:
- quejido,
- pena,
- cuerpo vencido,
- dolor sin teatralidad.

### `temper_imitative`
Tendencia a:
- copiar ritmos,
- repetir tonos,
- ensayar lenguaje,
- devolver frases.

### `temper_famished`
Tendencia a:
- hambre,
- bilis,
- consumo,
- necesidad sin educación.

### `temper_resentful`
Tendencia a:
- medir,
- recordar omisiones,
- cortar,
- acusar,
- devolver con mala leche fría.

### `temper_supplicant`
Tendencia a:
- pedir,
- esperar,
- reclamar sin atacar frontalmente,
- pegarse emocionalmente.

### `temper_furious`
Tendencia a:
- presión física,
- golpe,
- brusquedad,
- agresividad explícita.

### `temper_reasonable`
Tendencia a:
- hablar con lógica aparente,
- negociar,
- usar lenguaje casi humano,
- argumentar.

Regla:
- esta variable no hace “buena” a la criatura.
- Sólo la vuelve más capaz de interlocución coherente.

---

## 5.4. Variables de vínculo con el jugador

### `bond_intimacy_with_player`
Cuánto sabe la criatura de la intimidad del jugador.

Sube con:
- pareja/ex,
- dormitorio,
- balcón,
- escucha,
- quedarse despierto,
- hablarle a la puerta.

### `bond_dependence_on_player`
Cuánto parece necesitar al jugador como fuente, espejo o resolución.

Sube con:
- cuidado ambiguo,
- proximidad repetida,
- escucha insistente,
- contenciones tardías,
- trato compasivo.

### `bond_hostility_to_player`
Cuánta agresividad directa o recriminación ha acumulado.

Sube con:
- evitación sostenida,
- silencios crueles,
- abandono repetido,
- negación del borde,
- rechazo sistemático.

### `bond_trust_to_player`
No es “amistad”.  
Es posibilidad de trato no inmediatamente violento.

Sube con:
- confrontación honesta,
- escucha,
- respuestas directas,
- cuidado no performativo,
- contención asumida aunque sea parcial.

Baja con:
- mentira repetida,
- manipulación,
- aplazamiento crónico,
- ver sin actuar,
- usar la TV como sustituto constante.

---

## 5.5. Variables de lenguaje

### `lang_capacity`
Capacidad de articular unidades comprensibles.

### `lang_coherence`
Capacidad de mantener una línea, no sólo restos.

### `lang_mix_index`
Nivel de mezcla entre voces humanas, TV y exterioridad.

### `lang_addressivity`
Capacidad de dirigirse al jugador como “tú”, nombrarlo o interpelarlo.

### `lang_memory_depth`
Capacidad de usar material viejo de la partida, no sólo el residuo del último ciclo.

---

## 5.6. Variables de staging y puerta

### `door_pressure`
Cuánta presión puede ejercer sobre el marco.

### `frame_reactivity`
Cuánto responde el marco al jugador:
- calor,
- vibración,
- humedad,
- pausa,
- cambio de timbre.

### `threshold_intelligence`
Capacidad de usar:
- puerta atrancada,
- pasillo,
- puerta principal,
- mirilla,
- ventana,
- balcón
como sistema coordinado.

### `release_threshold`
Condición interna para pasar del estado “tras la puerta” a confrontación/apertura/resolución.

---

## 6. Fuentes de alimentación del sistema

La criatura no crece en abstracto. Se alimenta de entradas concretas.

## 6.1. Por zonas
Cada zona alimenta una o varias funciones:
- salón → voz, mezcla, medición, masa útil
- baño → piel, mucosa, humedad, respiración íntima
- dormitorio → corazón, pecho, súplica, intimidad
- cocina → hambre, bilis, digestión, parloteo banal
- pasillo → orientación, presión, desplazamiento
- entrada → ojos, vigilancia, umbral, timing
- balcón → pulmones, exposición, aire, caída posible
- ventana → mirada social, eco exterior, lectura torcida

## 6.2. Por vínculos
- madre → cuidado, clínica blanda, cuerpo, obediencia, respiración
- editor → voz cortante, medición, exigencia, vergüenza funcional
- amigo → banalidad, ruido, charla, hambre difusa, falsa compañía
- pareja/ex → corazón, súplica, memoria íntima, pecho, pausa afectiva
- TV → sintaxis, manipulación, editorialización, mezcla de voces
- exterioridad → ojos, orientación, foco, vigilancia, exposición

## 6.3. Por patrón de conducta
- evasión
- confrontación
- silencio
- mentira
- escucha
- contención
- exposición
- uso narcótico de TV
- revisar sin responder
- mirar umbrales sin actuar

## 6.4. Por gestión material
- limpiar tarde,
- limpiar una zona dejando otra,
- contener sólo superficie,
- sostener desorden funcional,
- aplazar cuerpo,
- saturar salón,
- abandonar cocina,
- dejar húmedo baño,
- sobrecargar dormitorio con memoria u objeto.

---

## 7. Reglas de creación de criatura

## 7.1. Regla de semilla dominante
En cada ciclo, una o dos semillas dominan según:
- foco de contaminación principal,
- presión activa,
- y zona más sacrificada.

## 7.2. Regla de mezcla heredada
Nada nuevo borra lo anterior.  
Cada ciclo añade:
- función,
- matiz,
- tono,
- o reorientación.

## 7.3. Regla de coherencia interna
Si la criatura tiene mucha voz pero poca cohesión corporal:
- hablará peor,
- se escuchará más que se sentirá.

Si tiene mucha masa y poca sintaxis:
- presionará más que dialogará.

Si tiene mucho corazón y mucha intimidad:
- no será “amable”; será más íntimamente insoportable.

## 7.4. Regla de contención desviada
La contención no sólo reduce crecimiento. También puede:
- desplazarlo de una zona a otra,
- cambiar su temperamento,
- o retrasar la forma visible pero no la deuda relacional.

## 7.5. Regla de trato acumulado
El modo en que el jugador trata a:
- sus vínculos,
- el cuerpo,
- la puerta,
- el exterior,
- la TV,
- y las contenciones
moldea el **cómo** de la criatura, no sólo el **cuánto**.

## 7.6. Regla de authored override suave
Se permiten momentos concretos authored que subrayen:
- una función,
- una respuesta,
- una forma de interacción,
- un rasgo visual,
- una frase,
- un gesto de marco,
siempre que no contradigan las variables acumuladas.

---

## 8. Modelo de ensamblaje de criatura

La criatura final puede entenderse como:

**CRIATURA = (Cuerpo material) + (Funciones dominantes) + (Temperamento dominante) + (Gramática verbal) + (Vínculo hacia jugador) + (Momento authored final)**

### Ejemplo A
- salón muy contaminado,
- editor evitado,
- TV absorbida,
- muchas mentiras,
- poco cuidado real.

Resultado probable:
- mucha voz,
- buena sintaxis rota,
- rencor medidor,
- presión coordinada,
- trato frío o evaluativo.

### Ejemplo B
- baño y dormitorio mal sostenidos,
- madre evitada,
- pareja/ex dejada en visto,
- mucho insomnio y escucha.

Resultado probable:
- pecho,
- respiración,
- latido,
- súplica íntima,
- criatura más doliente y pegajosa.

### Ejemplo C
- entrada/pasillo/ventana dominantes,
- mucha mirilla,
- mucho borde no resuelto,
- deadlines cortando clima,
- TV editorial.

Resultado probable:
- ojos,
- orientación,
- timing,
- presión de trayecto,
- criatura que enfoca, espera y mide.

### Ejemplo D
- cocina abandonada,
- amigo usado como narcótico,
- TV de fondo constante,
- contenciones siempre desplazadas.

Resultado probable:
- hambre difusa,
- gorgoteo,
- parloteo banal,
- compañía hueca,
- asco social.

---

## 9. Arquetipos resultantes de referencia

Estos no son criaturas cerradas, sino **familias de resultado**.

## 9.1. El Doliente Torácico
Dominantes:
- heart,
- lungs,
- skin,
- temper_doliente,
- temper_supplicant.

Se siente como:
- presencia pegada,
- latido mal aprendido,
- súplica,
- espera,
- intimidad sin permiso.

## 9.2. El Medidor Funcional
Dominantes:
- voice,
- eyes,
- cohesion,
- temper_resentful,
- temper_reasonable.

Se siente como:
- evaluación,
- precisión,
- frases cortadas,
- vergüenza hecha cuerpo,
- trato casi profesional y por eso obsceno.

## 9.3. El Observador de Umbral
Dominantes:
- eyes,
- legs,
- threshold_intelligence,
- temper_imitative o temper_resentful.

Se siente como:
- foco,
- línea de visión,
- corrección de timing,
- espera en pasillo,
- borde que piensa.

## 9.4. El Hambriento Parlanchín
Dominantes:
- stomach,
- voice,
- temper_famished,
- temper_imitative.

Se siente como:
- digestión de voces,
- gorgoteo,
- chiste muerto,
- falsa compañía,
- necesidad pegajosa.

## 9.5. El Razonable Torcido
Dominantes:
- lang_capacity alta,
- lang_coherence media/alta,
- bond_trust moderado,
- temper_reasonable + rencor o súplica.

Se siente como:
- interlocutor final posible,
- casi humano,
- precisamente peor por eso.

---

## 10. Reglas de interacción con la criatura

## 10.1. Antes de la confrontación final
La interacción principal ocurre mediante:
- escucha,
- proximidad,
- toque de marco,
- habla a puerta,
- retirada,
- sostener la escucha,
- cortar la escucha,
- mirar umbral relacionado,
- decidir contención o abandono.

## 10.2. Interacción final base
La confrontación final debe poder soportar:
- diálogo,
- silencio,
- escucha,
- contención,
- apertura,
- resistencia,
- aceptación,
- negociación,
- absorción,
- o convivencia fallida.

## 10.3. Regla de compatibilidad
No todos los finales usan las mismas mecánicas exactamente igual.  
El sistema debe permitir:
- módulos comunes,
- variaciones según criatura,
- momentos authored concretos,
- y cierres distintos compatibles con historial.

---

## 11. Espacio y escalabilidad para mecánicas o momentos concretos

Aquí está la parte clave que pedías: dejar hueco para añadir cosas sin romper el sistema.

## 11.1. Slots de momento authored por función dominante
Cada función puede habilitar momentos concretos:

### Voz
- frase casi clara detrás de la puerta,
- llamada fallida,
- repetición de una línea de TV,
- eco del jugador.

### Ojos
- pausa que sigue tu movimiento,
- mirilla contaminada,
- ventana que parece devolverte la mirada.

### Piernas
- cambio en peso del pasillo,
- embestida corta de marco,
- arrastre concreto.

### Estómago
- cocina que “digiere”,
- masticación verbal,
- olor/sabor/asco authored.

### Piel
- humedad táctil,
- temperatura de marco,
- membrana en pared,
- tela pegada.

### Corazón
- latido sincronizado,
- súplica,
- pausa afectiva,
- espera de cama o dormitorio.

### Pulmones
- exhalación en puerta,
- aire del balcón que responde,
- respiración del rellano.

## 11.2. Slots de mecánica escalable
Se reservan huecos para implementar después, si conviene:

### M1 — Escucha prolongada
Mini-mecánica de sostener cercanía sin ver.

### M2 — Lectura de textura de marco
Feedback táctil/sonoro al tocar puerta.

### M3 — Hablarle a la puerta
Sistema simple de interpelación con eco variable.

### M4 — Aperturas parciales controladas
No abrir del todo, pero sí ceder o intervenir.

### M5 — Contención avanzada
Intervenciones materiales más específicas según zona/función.

### M6 — Respuesta de criatura a objetos concretos
Props narrativos con reacción especial authored.

### M7 — Interacción con balcón/ventana en paralelo
Cruzar criatura interior con borde exterior.

Regla:
- estas mecánicas quedan **reservadas**, no obligatorias para MVP.
- el anexo las contempla para no cerrar el sistema demasiado pronto.

## 11.3. Slots de escena singular
Se permiten escenas concretas que no dependan sólo de la suma bruta de variables, siempre que usen un trigger legítimo.

Ejemplos:
- una sola palabra muy específica en una partida concreta,
- un latido acompasado en una noche muy íntima,
- una corrección del timing en pasillo,
- una reacción única a un objeto clave.

Requisito:
- cada escena singular debe declarar qué variables la habilitan.

---

## 12. Reglas de balance y producción

## 12.1. No diseñar 500 criaturas distintas
Diseñamos:
- un sistema base,
- unas familias de resultado,
- unos thresholds,
- y unas variantes authored.

## 12.2. Diferencia perceptible, no caos infinito
Las partidas deben producir diferencias reales en:
- tono,
- trato,
- lenguaje,
- foco corporal,
- staging,
- final,
pero no una explosión inmantenible.

## 12.3. MVP recomendado
Para vertical slice / primera implementación, basta con soportar:
- 4 funciones dominantes principales visibles,
- 4 temperamentos principales,
- 3 perfiles de lenguaje,
- 3 perfiles de trato final,
- y 2 o 3 momentos authored singulares.

## 12.4. Escalado posterior
Juego completo puede ampliar:
- manos,
- microinteracciones,
- reactividad a props,
- ramas de confrontación,
- y combinaciones más finas.

---

## 13. Variables mínimas recomendadas para implementación

### Núcleo obligatorio
- creature_mass
- creature_cohesion
- func_voice
- func_eyes
- func_stomach
- func_skin
- func_heart
- func_lungs
- temper_doliente
- temper_imitative
- temper_resentful
- temper_supplicant
- bond_intimacy_with_player
- bond_hostility_to_player
- bond_trust_to_player
- lang_capacity
- lang_coherence
- lang_mix_index
- door_pressure
- threshold_intelligence

### Núcleo ampliable
- func_legs
- func_hands
- temper_famished
- temper_furious
- temper_reasonable
- bond_dependence_on_player
- lang_memory_depth
- lang_addressivity
- frame_reactivity
- release_threshold

---

## 14. Puente con la confrontación final

La confrontación final debe usar este anexo como columna vertebral.

La criatura final no se define por:
- “fase 1, fase 2, fase 3”
ni por
- “boss pattern”.

Se define por:
- qué cuerpo ha conseguido organizar,
- qué voz puede sostener,
- qué temperamento domina,
- cuánto confía, odia o necesita al jugador,
- y qué historia quiere devolverle.

Por eso el diseño del final debe leer directamente:
- funciones dominantes,
- temperamento dominante,
- perfil de lenguaje,
- perfil vincular,
- y thresholds authored alcanzados.

---

## 15. Cierre de dirección

La criatura no es un premio ni un castigo.  
Es una **contabilidad obscena**.

No sale de la habitación porque sí.  
Sale, si sale, porque el jugador ha ayudado a organizarle un cuerpo.

No habla porque sea inteligente.  
Habla porque ha tragado demasiadas voces.

No será siempre igual.  
Y precisamente por eso tiene que obedecer reglas más claras que el hambre.

El monstruo final no debe sentirse diseñado desde fuera.  
Debe sentirse **merecido desde dentro**.
