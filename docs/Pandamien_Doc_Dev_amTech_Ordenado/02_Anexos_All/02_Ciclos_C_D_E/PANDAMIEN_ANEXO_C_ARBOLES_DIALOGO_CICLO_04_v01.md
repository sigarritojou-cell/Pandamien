# PANDAMIEN — ANEXO C
## Árboles de diálogo y ecos — Ciclo 4: La herida íntima
### Derivado del GDD Maestro v03, Anexo M v01, Anexo A v01, Anexo I v01, Anexo D C04 y Anexo E C04

---

## 0. Propósito del documento

Este documento abre el trabajo authored del **Ciclo 4 — La herida íntima**.

Su función no es montar una subtrama romántica con luces cálidas y postureo de videoclip. Su función es volver operativa la lógica ya fijada por el corpus:

- la **pareja/ex** toma la presión activa del ciclo,
- el **dormitorio** y el **balcón** pasan a ser zonas dominantes de contaminación afectiva,
- la **madre** y el **amigo** siguen vivos como continuidad real,
- el **editor** persiste como amenaza funcional de fondo,
- la **TV** ya puede parasitar lenguaje íntimo,
- y la **puerta** deja de sonar sólo orgánica para empezar a sonar doliente, torácica y emocionalmente torcida.

La regla maestra aquí sigue siendo la misma:

**cada nodo importante debe tensionar, como mínimo, dos de estas capas — vínculo, apartamento, criatura/puerta — y, cuando pueda, las tres.**

---

## 1. Criterios de escritura del Ciclo 4

### 1.1. Tono
El tono del ciclo 4 no es de reconciliación, ni de confesión bonita, ni de escena de “por fin hablamos”. Es de intimidad mala, retrasada y demasiado material.

### 1.2. Función del ciclo
- dejar que la pareja/ex domine sin volverse decorativa,
- incrustar la herida en dormitorio y balcón,
- mantener a madre y amigo como ritmos que cruzan la jornada,
- dejar al editor como cuchillo fino de fondo,
- y preparar una noche donde la puerta ya parezca tener corazón, pecho o súplica.

### 1.3. Regla de presión
La pareja/ex toma la presión activa, pero el día tiene que seguir oliendo a vida real: cuidado corporal que entra mal, banalidad que salva y molesta, utilidad que no desaparece y una casa que va tragándoselo todo.

### 1.4. Regla de eco
Todos los nodos relevantes del ciclo 4 deben sembrar al menos uno de estos retornos:
- eco de TV sentimental o manipulador,
- eco nocturno de latido, pecho, pausa afectiva o súplica,
- eco de zona en dormitorio, balcón o salón,
- eco de puerta como voz emocional fallida.

---

## 2. Árbol 01 — Pareja / Ex / llamada o mensaje largo que abre la presión del ciclo

### 2.1. Intención
La pareja/ex debe dominar el ciclo sin robarle espesor al piso. No entra para explicar el pasado; entra para demostrar que el pasado sigue ocupando cama, aire y barandilla.

### 2.2. Nodo principal

```yaml
node_id: "C04_EX_MAIN_01"
character: "Pareja/Ex"
phase: "day"
context: "Primera tarde o momento de reposo malo en dormitorio. El cuerpo ya viene tocado del ciclo anterior."
text: "No sé si tendría que haberte escrito, pero llevo un rato dándole vueltas y prefiero hacerlo a seguir hablando sola."
subtext: "vuelvo / sigo aquí / no sé cerrar esto / tampoco te dejo salir limpio"
location_bias: "bedroom -> balcony"
related_zone: "bedroom"
recurrence_type: "main"
player_options:
  - option_id: "C04_EX_MAIN_01_A"
    label: "Responder con verdad corta y abrir la puerta de la conversación"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: -1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +1
      zone_contamination_bedroom: +2
      zone_contamination_balcony: +1
    unlocks: ["C04_EX_FOLLOWUP_01"]
    locks: []
    next_node: "C04_EX_FOLLOWUP_01"
  - option_id: "C04_EX_MAIN_01_B"
    label: "Responder ambiguo, sin cerrar ni abrir del todo"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_bedroom: +2
      zone_contamination_balcony: +1
    unlocks: ["C04_EX_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C04_EX_MAIN_01_C"
    label: "Abrir, leer y dejarlo suspendido"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +1
      zone_contamination_bedroom: +2
      zone_contamination_balcony: +1
    unlocks: ["C04_EX_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C04_EX_MAIN_01_D"
    label: "No contestar o dejar en visto"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: +2
      guilt_noise: +2
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +2
      zone_contamination_bedroom: +2
      zone_contamination_balcony: +1
    unlocks: ["C04_EX_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "frase melodramática fuera de lugar"
    - "consejo sentimental demasiado oportuno"
  night:
    - "latido blando"
    - "pausa afectiva rara"
    - "súplica o voz emocional rota si se deja en visto"
  exterior:
    - "balcón ajeno, pareja vecina, luz íntima que duele por contraste"
notes: "La pareja/ex aquí no debe pedir explicación completa. Debe abrir una grieta que el piso pueda quedarse."
```

### 2.3. Follow-up e insistencia

```yaml
node_id: "C04_EX_FOLLOWUP_01"
character: "Pareja/Ex"
phase: "day"
context: "El jugador ha abierto la conversación con algo de verdad."
text: "Ya. Es que hay días que parece que todo lo que dejamos a medias se queda aquí esperando también."
subtext: "te nombro sin cerrar / convierto la memoria en presencia"
location_bias: "bedroom"
related_zone: "bedroom"
recurrence_type: "followup"
player_options:
  - option_id: "C04_EX_FOLLOWUP_01_A"
    label: "Seguir entrando"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: -1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +1
      zone_contamination_bedroom: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C04_EX_FOLLOWUP_01_B"
    label: "Cortar con una frase corta"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_bedroom: +1
    unlocks: ["C04_EX_INSIST_01"]
    locks: []
    next_node: "END"
```

```yaml
node_id: "C04_EX_INSIST_01"
character: "Pareja/Ex"
phase: "day"
context: "Si se ha aplazado o dejado en suspenso."
text: "No hace falta que me contestes ahora. Sólo… no lo leas como si no hubiese pasado nada."
subtext: "te dejo espacio / te lo lleno igual"
location_bias: "bedroom -> balcony"
related_zone: "balcony"
recurrence_type: "insistence"
player_options:
  - option_id: "C04_EX_INSIST_01_A"
    label: "Mandar una respuesta mínima"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: +1
      zone_contamination_balcony: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C04_EX_INSIST_01_B"
    label: "No responder"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: +2
      guilt_noise: +2
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +2
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: ["C04_EX_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 3. Árbol 02 — Madre / cuidado que entra peor cuando el pecho ya va cargado

### 3.1. Intención
La madre aquí ya no manda el ciclo, pero debe cruzarlo como una mano que llega cuando menos hueco hay. Puede salvar o invadir, y a veces las dos cosas a la vez.

### 3.2. Nodo principal

```yaml
node_id: "C04_MADRE_MAIN_01"
character: "Madre"
phase: "day"
context: "Después de la irrupción íntima o en un momento donde el jugador intenta recomponerse."
text: "¿Has comido algo por lo menos? Tienes días en que se te nota desde aquí, aunque no te vea."
subtext: "te leo el cuerpo / me sigues preocupando / llego cuando molesto más"
location_bias: "bedroom -> bathroom"
related_zone: "bathroom"
recurrence_type: "main"
player_options:
  - option_id: "C04_MADRE_MAIN_01_A"
    label: "Responder con cansancio pero sin cortar"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bathroom: +1
      zone_contamination_bedroom: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C04_MADRE_MAIN_01_B"
    label: "Quitarle importancia"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bathroom: +1
    unlocks: ["C04_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C04_MADRE_MAIN_01_C"
    label: "Posponer"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bathroom: +1
    unlocks: ["C04_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C04_MADRE_MAIN_01_D"
    label: "Silenciar"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: +2
      guilt_noise: +2
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bathroom: +1
      zone_contamination_bedroom: +1
    unlocks: ["C04_MADRE_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "rutina de autocuidado en tono casi insultantemente oportuno"
  night:
    - "si baño heredado pesa: humedad dentro de un latido"
    - "si el dormitorio domina: cuidado intrusivo dentro de la súplica"
  exterior:
    - "domesticidad ajena o cuidado de vecindad que raspa"
notes: "La madre aquí no compite con la pareja/ex: agrava la mezcla entre pecho y cuerpo."
```

---

## 4. Árbol 03 — Amigo / banalidad que ahora duele por contraste

### 4.1. Intención
El amigo sigue vivo y eso es importante. Pero su banalidad, en este ciclo, debe funcionar como alivio o como violencia involuntaria por contraste.

### 4.2. Nodo principal

```yaml
node_id: "C04_AMIGO_MAIN_01"
character: "Amigo"
phase: "day"
context: "Mitad o final de tarde, cuando el jugador ya viene tocado por la herida íntima."
text: "Te iba a mandar una tontería, pero por tu cara de silencio igual la tontería hoy soy yo."
subtext: "te veo un poco / sigo entrando ligero / no sé si te salvo o te toco los cojones"
location_bias: "living_room -> kitchen"
related_zone: "living"
recurrence_type: "main"
player_options:
  - option_id: "C04_AMIGO_MAIN_01_A"
    label: "Responder y dejarse arrastrar un rato"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: 0
      social_debt: -1
      guilt_noise: -1
      loneliness_index: -1
      tv_influence: +1
      editor_pressure: 0
      stability: 0
      threat_intimacy: -1
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
      zone_contamination_kitchen: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C04_AMIGO_MAIN_01_B"
    label: "Responder seco"
    tone: "evasiva"
    effects:
      avoidance: 0
      confrontation: 0
      social_debt: +1
      guilt_noise: 0
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C04_AMIGO_MAIN_01_C"
    label: "Dejarlo para luego"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: 0
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: ["C04_AMIGO_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
  - option_id: "C04_AMIGO_MAIN_01_D"
    label: "Ignorar"
    tone: "silence"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: 0
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: 0
    unlocks: ["C04_AMIGO_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "frase de compañía barata"
    - "humor flojo que tapa demasiado"
  night:
    - "si el jugador se refugia aquí, la súplica nocturna duele más por contraste"
  exterior:
    - "vida ajena ligera que parece insultante desde dentro"
notes: "El amigo no deja de ser humano aquí. Precisamente por eso puede doler más."
```

---

## 5. Árbol 04 — Editor / cuchillo fino de fondo

### 5.1. Intención
El editor aquí no debe tomar mando. Debe atravesar el clima con un recordatorio funcional que mezcle utilidad y herida.

### 5.2. Nodo principal

```yaml
node_id: "C04_EDITOR_MAIN_01"
character: "Editor"
phase: "day"
context: "Final de tarde o momento de saturación afectiva."
text: "Cuando puedas, necesito saber si cuento contigo mañana. No me dejes colgado otra vez."
subtext: "la maquinaria sigue / tu pecho no suspende el calendario"
location_bias: "living_room -> hall"
related_zone: "living"
recurrence_type: "main"
player_options:
  - option_id: "C04_EDITOR_MAIN_01_A"
    label: "Responder con una mínima verdad funcional"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: +1
      stability: -1
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C04_EDITOR_MAIN_01_B"
    label: "Escurrir el bulto"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: +1
      stability: 0
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: +1
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C04_EDITOR_MAIN_01_C"
    label: "Ignorar"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: +2
      guilt_noise: +2
      loneliness_index: +1
      tv_influence: +1
      editor_pressure: +2
      stability: -1
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: +1
      zone_contamination_living: +2
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
echoes:
  tv:
    - "frase funcional dentro de un contenido sentimental"
  night:
    - "pecho con ritmo feo, cortado o utilitario"
  exterior:
    - "luces de trabajo o rutina ajena que no espera a nadie"
notes: "La gracia es que el editor aquí no arrasa: pudre el borde."
```

---

## 6. Pool de TV contaminada — suggestion sentimental hacia manipulación blanda

```yaml
node_id: "C04_TV_ECHO_POOL_01"
character: "TV"
phase: "day_to_night"
context: "Salón activo o residual, especialmente tras interacción con Pareja/Ex"
text_pool:
  - "Hay vínculos que una no corta; sólo cambia de habitación."
  - "Lo peor no es que alguien vuelva. Lo peor es que vuelva cuando ya no queda sitio."
  - "A veces una llamada no arregla nada. Sólo mueve el aire."
subtext: "yo convierto tu intimidad en guión barato / te doy frases para no pensar / también te infecto el pecho"
related_zone: "living"
recurrence_type: "contaminated_echo"
effects:
  tv_influence: +1
  threat_intimacy: +1
  zone_contamination_living: +1
  creature_growth: +1
notes: "La TV aquí no debe sonar brillante ni cínica. Debe sonar demasiado disponible para el drama ajeno."
```

---

## 7. Retorno de puerta / noche — corazón, pecho y súplica mal aprendida

```yaml
node_id: "C04_PUERTA_RETURN_01"
character: "Puerta/Criatura"
phase: "night"
context: "Tras el cierre del día. Dormitorio o balcón han quedado tocados, y el pasillo concentra la devolución."
text: "No hay frase limpia. Hay un latido torpe, una exhalación que parece pedir algo y una sílaba emocional mal nacida que no llega a ser palabra."
subtext: "he aprendido tu intimidad mal / ya no sólo respiro / también padezco"
location_bias: "hall -> sealed_door"
related_zone: "hall"
recurrence_type: "night_echo"
player_options:
  - option_id: "C04_PUERTA_RETURN_01_A"
    label: "Acercarse y escuchar"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +2
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C04_PUERTA_RETURN_01_B"
    label: "Hablarle al marco o quedarse demasiado tiempo"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +2
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C04_PUERTA_RETURN_01_C"
    label: "Retirarse sin mirar más"
    tone: "silence"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C04_PUERTA_RETURN_01_D"
    label: "Dormir o medicarse"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
notes: "La textura exacta depende del foco dominante: dormitorio -> pecho/latido/voz herida; balcón -> exhalación expuesta; editor de fondo -> ritmo cortado; madre heredada -> humedad corporal dentro de la súplica."
```

---

## 8. Mapa rápido de IDs y funciones

| ID | Fuente | Tipo | Zona | Función principal |
|---|---|---|---|---|
| C04_EX_MAIN_01 | Pareja/Ex | Main | Dormitorio/Balcón | Abrir la herida íntima como presión activa |
| C04_EX_INSIST_01 | Pareja/Ex | Insistence | Dormitorio/Balcón | Sostener silencio cargado y amenaza afectiva |
| C04_MADRE_MAIN_01 | Madre | Main | Dormitorio/Baño | Cruzar la herida con cuerpo y cuidado |
| C04_AMIGO_MAIN_01 | Amigo | Main | Salón/Cocina | Ofrecer banalidad que salva o raspa |
| C04_EDITOR_MAIN_01 | Editor | Main | Salón/Pasillo | Envenenar el clima con utilidad persistente |
| C04_TV_ECHO_POOL_01 | TV | Contaminated Echo | Salón | Parasitar lenguaje íntimo |
| C04_PUERTA_RETURN_01 | Puerta/Criatura | Night Echo | Pasillo | Devolver corazón, pecho o súplica |

---

## 9. Validaciones para pasar a siguientes ciclos

Antes de abrir el Ciclo 5, este documento debe dejar claras estas cuatro cosas:

1. La **pareja/ex** ya puede dominar un ciclo sin volverse melodrama ornamental.  
2. El **dormitorio** y el **balcón** ya funcionan como zonas íntimas contaminables de verdad.  
3. La **puerta** ya no sólo parece albergar un cuerpo: empieza a parecer albergar afecto deformado.  
4. El **editor**, la **madre** y el **amigo** pueden seguir cruzando la jornada sin romper la presión activa de la herida íntima.

Si una de estas cuatro patas falla, el Ciclo 5 entrará cojo y el exterior no tendrá carne suficiente que reflejar.

---

## 10. Veredicto de cierre

Este anexo queda aprobado como **cuarta capa authored de árboles de diálogo del proyecto**. No agota el Ciclo 4, pero deja fijados:

- la pareja/ex como presión activa legítima,
- el dormitorio y el balcón como órganos íntimos del sistema,
- la madre como cuidado que ya no entra limpio,
- el amigo como alivio que puede doler,
- el editor como cuchillo de fondo,
- la TV en suggestion sentimental rozando manipulación,
- y la puerta como aparato de corazón, pecho y súplica.

La norma final del ciclo es sencilla:

**la herida íntima no pide explicación; pide caja torácica.**
