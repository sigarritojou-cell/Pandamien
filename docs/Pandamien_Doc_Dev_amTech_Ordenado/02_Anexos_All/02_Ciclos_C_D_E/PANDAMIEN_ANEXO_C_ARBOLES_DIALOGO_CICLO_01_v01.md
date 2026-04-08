# PANDAMIEN — ANEXO C
## Primeros árboles de diálogo y ecos — Ciclo 1: Reconocimiento
### Derivado del GDD Maestro v03, Anexo M v01, Anexo D C01 y Anexo E C01

---

## 0. Propósito del documento

Este anexo abre el trabajo authored real de diálogo para el **Ciclo 1 — Reconocimiento**.

No pretende cerrar todavía todas las variantes del ciclo, sino fijar una primera gramática jugable y emocional de cómo deben funcionar:

- los nodos principales de relación,
- la respuesta directa / evasiva / diferida / silencio,
- los ecos en TV, noche y apartamento,
- la trazabilidad entre vínculo, foco espacial y criatura,
- y el tono cotidiano degradado propio del arranque.

La regla maestra de este anexo es sencilla:

**cada nodo importante debe mover vínculo, apartamento y promesa de criatura al menos en dos de esas tres capas, idealmente en las tres.**

---

## 1. Criterios de escritura del Ciclo 1

### 1.1. Tono
El tono del primer ciclo debe ser de normalidad fatigada. Nada entra como gran escena de horror. Todo debe parecer doméstico, ligeramente triste, algo cargado, pero aún racionalizable.

### 1.2. Función del ciclo
- instalar la rutina,
- fijar la deuda inicial con el editor,
- dejar que la madre entre ya como discurso de cuerpo y obediencia,
- usar al amigo como falsa normalidad,
- mantener a la pareja/ex como ausencia con masa específica,
- y preparar que la noche devuelva algo mínimo detrás de la puerta.

### 1.3. Regla de eco
Todos los nodos relevantes deben sembrar al menos uno de estos retornos:
- eco de TV,
- eco nocturno,
- eco de zona,
- eco de puerta.

---

## 2. Árbol 01 — Madre / llamada corta de media mañana

### 2.1. Intención
La madre no entra como villana ni como simple cuidadora. Entra como mezcla de ternura, costumbre y control blando. Su llamada debe pesar en baño y dormitorio, y dejar abierta la posibilidad de que lo corporal vuelva de noche como respiración húmeda, cansancio o sensación de cuerpo vigilado.

### 2.2. Nodo principal

```yaml
node_id: "C01_MADRE_MAIN_01"
character: "Madre"
phase: "day"
context: "Media mañana. El jugador lleva un rato en el piso, aún sin asentarse del todo."
text: "¿Estabas durmiendo todavía? Tienes voz rara. Has desayunado algo o sigues como siempre."
subtext: "te cuido / te vigilo / no confío del todo en que te cuides solo"
location_bias: "dormitorio -> baño"
related_zone: "bathroom"
recurrence_type: "main"
player_options:
  - option_id: "C01_MADRE_MAIN_01_A"
    label: "Sí, sí. Estoy bien, no empieces."
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bedroom: 0
      zone_contamination_living: 0
      zone_contamination_hall: 0
      zone_contamination_kitchen: 0
      zone_contamination_bathroom: +1
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C01_MADRE_FOLLOWUP_01"]
    locks: []
    next_node: "C01_MADRE_FOLLOWUP_01"
  - option_id: "C01_MADRE_MAIN_01_B"
    label: "He dormido regular. Luego me arreglo."
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_living: 0
      zone_contamination_hall: 0
      zone_contamination_kitchen: 0
      zone_contamination_bathroom: +1
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C01_MADRE_FOLLOWUP_02"]
    locks: []
    next_node: "C01_MADRE_FOLLOWUP_02"
  - option_id: "C01_MADRE_MAIN_01_C"
    label: "Te llamo luego, mamá."
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: 0
      zone_contamination_living: 0
      zone_contamination_hall: 0
      zone_contamination_kitchen: 0
      zone_contamination_bathroom: +1
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C01_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C01_MADRE_MAIN_01_D"
    label: "No coger / dejar sonar"
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
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_living: 0
      zone_contamination_hall: 0
      zone_contamination_kitchen: 0
      zone_contamination_bathroom: +2
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C01_MADRE_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "tono clínico suave"
    - "frases sobre descanso, rutina o cuidarse"
  night:
    - "si el baño queda peor: respiración húmeda o roce blando tras la puerta"
    - "si el dormitorio queda peor: sensación de cuerpo cansado escuchado por la casa"
  exterior:
    - "rellano silencioso con bolsa, medicamento o eco de pasos domésticos"
notes: "El objetivo no es discutir fuerte; es instalar deuda corporal y vigilancia íntima."
```

### 2.3. Follow-ups mínimos

```yaml
node_id: "C01_MADRE_FOLLOWUP_01"
character: "Madre"
phase: "day"
context: "La respuesta ha sido directa, con defensa leve."
text: "Yo no empiezo nada, hijo. Te lo digo porque luego te vienes abajo y ya está."
subtext: "te conozco / te reduzco / te sigo cuidando"
location_bias: "bathroom"
related_zone: "bathroom"
recurrence_type: "followup"
player_options:
  - option_id: "C01_MADRE_FOLLOWUP_01_A"
    label: "Vale. Luego te digo algo."
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: 0
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bathroom: 0
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C01_MADRE_FOLLOWUP_01_B"
    label: "Sí, claro."
    tone: "evasive"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bathroom: +1
    unlocks: ["C01_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
```

```yaml
node_id: "C01_MADRE_INSIST_01"
character: "Madre"
phase: "day"
context: "Si se ha pospuesto o cortado la llamada."
text: "Cuando puedas me dices algo, aunque sea un mensaje."
subtext: "no te suelto / quedas en deuda"
location_bias: "dormitorio"
related_zone: "bedroom"
recurrence_type: "insistence"
player_options:
  - option_id: "C01_MADRE_INSIST_01_A"
    label: "Responder con un emoji o un 'sí'"
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
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bedroom: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C01_MADRE_INSIST_01_B"
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
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_bathroom: +1
    unlocks: ["C01_MADRE_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 3. Árbol 02 — Editor / deuda inicial de productividad

### 3.1. Intención
El editor es la primera presión activa del juego. No debe sonar a supervillano laboral de cómic, sino a exigencia razonable con filo. Su función es colonizar el salón con utilidad, reloj y autoexigencia, y sembrar la voz latente de la criatura.

### 3.2. Nodo principal

```yaml
node_id: "C01_EDITOR_MAIN_01"
character: "Editor"
phase: "day"
context: "Primer tramo útil del día. El jugador ya ha podido mirar el móvil o acercarse a la mesa/salón."
text: "Necesito que me digas cómo llevas lo de hoy. Aunque sea una línea."
subtext: "rendir también es existir / te estoy midiendo"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "main"
player_options:
  - option_id: "C01_EDITOR_MAIN_01_A"
    label: "Voy justo, pero te lo saco."
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: -1
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bedroom: 0
      zone_contamination_living: +1
      zone_contamination_hall: 0
      zone_contamination_kitchen: 0
      zone_contamination_bathroom: 0
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C01_EDITOR_FOLLOWUP_01"]
    locks: []
    next_node: "C01_EDITOR_FOLLOWUP_01"
  - option_id: "C01_EDITOR_MAIN_01_B"
    label: "Se me ha torcido la mañana. Luego te digo algo mejor."
    tone: "evasive"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: +1
      stability: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: 0
      zone_contamination_living: +2
      zone_contamination_hall: 0
      zone_contamination_kitchen: 0
      zone_contamination_bathroom: 0
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C01_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C01_EDITOR_MAIN_01_C"
    label: "Abrir y dejar sin contestar"
    tone: "delay"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
      loneliness_index: 0
      tv_influence: +1
      editor_pressure: +2
      stability: -1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: 0
      zone_contamination_living: +2
      zone_contamination_hall: 0
      zone_contamination_kitchen: +1
      zone_contamination_bathroom: 0
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C01_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C01_EDITOR_MAIN_01_D"
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
      creature_growth: +2
      door_pressure: +1
      zone_contamination_bedroom: 0
      zone_contamination_living: +3
      zone_contamination_hall: 0
      zone_contamination_kitchen: +1
      zone_contamination_bathroom: 0
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C01_EDITOR_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "frases de rendimiento amable"
    - "normalización de ir tarde, pero sin parar nunca"
  night:
    - "si el salón queda peor: gemido vocal o golpe seco con resonancia funcional"
    - "zumbido de aparato o madera que parece querer articular algo"
  exterior:
    - "luces vecinas o reflejos sincronizados con el horario"
notes: "El editor no debe gritar. Debe invadir con exactitud y medir."
```

### 3.3. Follow-up e insistencia

```yaml
node_id: "C01_EDITOR_FOLLOWUP_01"
character: "Editor"
phase: "day"
context: "El jugador ha respondido de frente."
text: "Vale. No necesito perfecto. Necesito saber que estás ahí."
subtext: "la presencia sólo cuenta si produce"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "followup"
player_options:
  - option_id: "C01_EDITOR_FOLLOWUP_01_A"
    label: "Estoy."
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: 0
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: -1
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C01_EDITOR_FOLLOWUP_01_B"
    label: "Sí, sí."
    tone: "evasive"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: +1
      stability: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: ["C01_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
```

```yaml
node_id: "C01_EDITOR_INSIST_01"
character: "Editor"
phase: "day"
context: "Si se ha dejado en visto o se ha aplazado."
text: "Cuando lo tengas, aunque sea a medias, me lo mandas."
subtext: "no desaparezcas / el retraso también habla"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "insistence"
player_options:
  - option_id: "C01_EDITOR_INSIST_01_A"
    label: "Contestar con algo mínimo"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: +1
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C01_EDITOR_INSIST_01_B"
    label: "No contestar"
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
      creature_growth: +1
      door_pressure: +1
      zone_contamination_living: +2
    unlocks: ["C01_EDITOR_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 4. Árbol 03 — Amigo / ruido banal y falsa normalidad

### 4.1. Intención
El amigo no viene a “hacer avanzar la trama” de manera obvia. Viene a demostrar que la evasión agradable también deja residuo. Debe calentar salón y cocina, y competir con la presión del editor sin parecer dramáticamente equivalente.

### 4.2. Nodo principal

```yaml
node_id: "C01_AMIGO_MAIN_01"
character: "Amigo"
phase: "day"
context: "Mitad del día o tarde temprana. El jugador lleva ya alguna deuda encima."
text: "Hermano, te mando esto porque me estoy volviendo gilipollas encerrado. Escúchalo y me dices si soy yo o el mundo."
subtext: "ven a refugiarte aquí / no pienses demasiado / acompáñame en la idiotez"
location_bias: "living_room -> kitchen"
related_zone: "kitchen"
recurrence_type: "main"
player_options:
  - option_id: "C01_AMIGO_MAIN_01_A"
    label: "Entrar al juego y responderle"
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
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bedroom: 0
      zone_contamination_living: +1
      zone_contamination_hall: 0
      zone_contamination_kitchen: +1
      zone_contamination_bathroom: 0
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C01_AMIGO_FOLLOWUP_01"]
    locks: []
    next_node: "C01_AMIGO_FOLLOWUP_01"
  - option_id: "C01_AMIGO_MAIN_01_B"
    label: "Responder a medias, sin entrar del todo"
    tone: "evasive"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: 0
      loneliness_index: 0
      tv_influence: +1
      editor_pressure: 0
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
      zone_contamination_kitchen: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C01_AMIGO_MAIN_01_C"
    label: "Dejar el audio para luego"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: 0
      loneliness_index: +1
      tv_influence: +1
      editor_pressure: 0
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
      zone_contamination_kitchen: 0
    unlocks: ["C01_AMIGO_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C01_AMIGO_MAIN_01_D"
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
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: 0
      zone_contamination_kitchen: 0
    unlocks: ["C01_AMIGO_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "tono de magazine absurdo o entretenimiento blandito"
    - "voz de compañía que normaliza estar perdiendo el tiempo"
  night:
    - "si el jugador se refugió aquí demasiado: salón más blando, más pasivo, más apto para voz latente"
  exterior:
    - "ruido lejano de vecinos como falsa comunidad"
notes: "El amigo no debe parecer accesorio. Su banalidad tiene que ser cálida y sospechosa a la vez."
```

---

## 5. Árbol 04 — Pareja / Ex como ausencia significativa

### 5.1. Intención
En el Ciclo 1 la pareja/ex no entra aún como escena directa. Debe existir como hueco con peso, ocupando dormitorio y memoria. No se escribe todavía conversación principal: se escribe la **ausencia significativa**.

### 5.2. Nodo de ausencia

```yaml
node_id: "C01_EX_ABSENCE_01"
character: "Pareja/Ex"
phase: "day"
context: "Quietud en dormitorio. El jugador abre galería, historial o se cruza con un objeto que remite a esa persona."
text: "No hay mensaje nuevo. Sólo un nombre, una foto vieja o una conversación detenida."
subtext: "esto sigue aquí aunque nadie hable"
location_bias: "bedroom"
related_zone: "bedroom"
recurrence_type: "absence_echo"
player_options:
  - option_id: "C01_EX_ABSENCE_01_A"
    label: "Mirar un poco más"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: 0
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C01_EX_ABSENCE_01_B"
    label: "Cerrar rápido"
    tone: "evasive"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: 0
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C01_EX_ABSENCE_01_C"
    label: "Dejarlo abierto en silencio"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: +2
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C01_EX_ABSENCE_01_D"
    label: "Cambiar de habitación"
    tone: "silence"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: 0
    unlocks: []
    locks: []
    next_node: "END"
echoes:
  tv:
    - "línea sentimental demasiado neutra"
    - "música o frase que parece tocar una costra sin abrirla"
  night:
    - "dormitorio menos inocente"
    - "la criatura aún no roba esta voz, pero empieza a hacer sitio"
  exterior:
    - "balcón o ventana con carga íntima futura, todavía leve"
notes: "La ausencia debe pesar. No debe sonar a truco para posponer contenido."
```

---

## 6. Nodos de eco contaminado para TV y noche

### 6.1. TV — comfort parasitario temprano

```yaml
node_id: "C01_TV_ECHO_POOL_01"
character: "TV"
phase: "transition"
context: "Tras las decisiones del día, con el piso ya más silencioso."
text: "La TV no da una pista sobrenatural. Devuelve frases que podrían ser casuales, pero que llegan demasiado pegadas a las decisiones del jugador."
subtext: "acompaño / justifico / adormezco"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "contaminated_echo"
player_options:
  - option_id: "C01_TV_ECHO_POOL_01_A"
    label: "Dejarla de fondo"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: -1
      tv_influence: +2
      editor_pressure: 0
      stability: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C01_TV_ECHO_POOL_01_B"
    label: "Apagarla"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: 0
      loneliness_index: +1
      tv_influence: -1
      editor_pressure: 0
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: 0
    unlocks: []
    locks: []
    next_node: "END"
notes: "Pool abierto de líneas: 'ya habrá tiempo', 'lo importante es descansar', 'no conviene exigirse demasiado hoy'."
```

### 6.2. Noche — retorno mínimo de la puerta

```yaml
node_id: "C01_PUERTA_RETURN_01"
character: "Puerta/Criatura"
phase: "night"
context: "Cierre de la primera noche."
text: "Un gemido torpe, una fricción, o un golpe pequeño desde detrás de la puerta atrancada."
subtext: "la casa ha aprendido una sílaba de tu día"
location_bias: "hall"
related_zone: "hall"
recurrence_type: "contaminated_echo"
player_options:
  - option_id: "C01_PUERTA_RETURN_01_A"
    label: "Acercarse y escuchar"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C01_PUERTA_RETURN_01_B"
    label: "No mirar más"
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
      creature_growth: +1
      door_pressure: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
notes: "La textura exacta depende del residuo dominante: editor -> garganta/golpe seco; madre -> humedad/respiración."
```

---

## 7. Mapa rápido de IDs y funciones

| ID | Fuente | Tipo | Zona | Función principal |
|---|---|---|---|---|
| C01_MADRE_MAIN_01 | Madre | Main | Baño/Dormitorio | Instalar deuda corporal |
| C01_MADRE_INSIST_01 | Madre | Insistence | Dormitorio | Mantener culpa blanda |
| C01_EDITOR_MAIN_01 | Editor | Main | Salón | Instalar deuda productiva |
| C01_EDITOR_INSIST_01 | Editor | Insistence | Salón | Medir retraso y presión |
| C01_AMIGO_MAIN_01 | Amigo | Main | Salón/Cocina | Ofrecer refugio banal |
| C01_EX_ABSENCE_01 | Pareja/Ex | Absence Echo | Dormitorio | Dar peso a la herida latente |
| C01_TV_ECHO_POOL_01 | TV | Contaminated Echo | Salón | Justificar evasión |
| C01_PUERTA_RETURN_01 | Puerta/Criatura | Night Echo | Pasillo | Devolver el residuo del día |

---

## 8. Veredicto de cierre

Este anexo queda aprobado como **primer núcleo de árboles authored del proyecto**. No agota el Ciclo 1, pero ya permite:

- escribir el primer día con opciones reales,
- sembrar ecos en TV y noche,
- cruzar vínculo, apartamento y criatura,
- y fijar un estándar de IDs, tono y trazabilidad para el resto del guion.

El siguiente paso natural tras este documento es doble:

1. ampliar el **Anexo C** con las ramas de seguimiento del **Ciclo 2**,
2. y abrir el **Anexo I — tabla de efectos cruzados ampliada** para que toda esta mugre preciosa no se nos vuelva barro sin sistema.
