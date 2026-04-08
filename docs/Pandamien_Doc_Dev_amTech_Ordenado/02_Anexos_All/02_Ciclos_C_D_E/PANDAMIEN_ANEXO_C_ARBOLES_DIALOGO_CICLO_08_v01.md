# PANDAMIEN — ANEXO C
## Árboles de diálogo y ecos — Ciclo 8: Resolución
### Derivado del GDD Maestro v04, Anexo M v01, Anexo A v01, Anexo I v01, Anexo D C08 y Anexo E C08

---

## 0. Propósito del documento

Este documento abre el trabajo authored del **Ciclo 8 — Resolución**.

Su función no es escribir un final como cinemática cerrada, sino volver operativa la lógica ya fijada por el corpus:

- la **criatura** toma la presión activa como suma viva del historial,
- la **puerta atrancada** deja de ser sólo interfaz de retorno y se vuelve lugar de confrontación dialogada,
- **Madre, Editor, Amigo, Pareja/Ex y TV** sobreviven como material de tono dentro del encuentro,
- el **apartamento completo** funciona como cuerpo testigo,
- y la resolución final no limpia ni explica del todo: **devuelve**.

La regla maestra aquí debe ser más estricta que nunca:

**cada nodo importante debe alterar la postura del jugador, el tono del umbral y la cualidad relacional de la criatura; si sólo "da lore", está muerto.**

---

## 1. Criterios de escritura del Ciclo 8

### 1.1. Tono
El tono de C08 no es épico ni confesional. Es de reconocimiento sucio. El jugador llega ya sin coartadas limpias y la criatura tampoco puede hablar como una persona entera.

### 1.2. Función del ciclo
- convertir la puerta en diálogo,
- fijar la postura ética del jugador ante lo engendrado,
- devolver la cualidad del trato acumulado,
- abrir categorías de cierre compatibles con el canon,
- y evitar tanto el boss final como la chapa expositiva.

### 1.3. Regla de respuesta
La criatura debe responder a:
- distancia,
- tono,
- si el jugador abre o no,
- si habla primero o escucha primero,
- y al tipo de historial dominante.

### 1.4. Regla de herencia
Las palabras de la criatura no salen de la nada. Deben salir de:
- madre,
- editor,
- amigo,
- pareja/ex,
- TV,
- y de los residuos de cada zona.

---

## 2. Árbol 01 — Umbral / primer contacto con la puerta

### 2.1. Intención
El primer árbol no es aún la conversación plena. Es el momento en que el jugador fija su **postura**. La puerta ya puede responder; la cuestión es cómo se entra en relación con ella.

### 2.2. Nodo principal

```yaml
node_id: "C08_THRESHOLD_MAIN_01"
character: "Puerta atrancada / Umbral"
phase: "night"
context: "Primer momento de quietud total frente al marco. El jugador ya ha llegado al final del trayecto y la casa escucha en serio."
text: "Hay una respiración que no termina de ser ajena. Una pausa. Después, algo parecido a una voz que no se atreve todavía a existir del todo."
subtext: "ya has llegado / ya no puedes fingir que esto era sólo una puerta"
location_bias: "hallway -> sealed_door"
related_zone: "hall"
recurrence_type: "main"
player_options:
  - option_id: "C08_THRESHOLD_MAIN_01_A"
    label: "Hablar primero, sin abrir: 'Estoy aquí.'"
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
      creature_growth: 0
      door_pressure: +1
      creature_temperament: "soften_or_listen"
      zone_contamination_hall: +1
    unlocks: ["C08_CREATURE_REPLY_01"]
    locks: []
    next_node: "C08_CREATURE_REPLY_01"
  - option_id: "C08_THRESHOLD_MAIN_01_B"
    label: "Escuchar en silencio, pegado al marco"
    tone: "delay"
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
      creature_growth: 0
      door_pressure: +1
      creature_temperament: "absorption_risk"
      zone_contamination_hall: +1
    unlocks: ["C08_CREATURE_REPLY_01"]
    locks: []
    next_node: "C08_CREATURE_REPLY_01"
  - option_id: "C08_THRESHOLD_MAIN_01_C"
    label: "Intentar contener o bloquear antes de escuchar"
    tone: "evasiva"
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
      door_pressure: +2
      creature_temperament: "harden"
      zone_contamination_hall: +2
    unlocks: ["C08_CREATURE_REPLY_02"]
    locks: []
    next_node: "C08_CREATURE_REPLY_02"
  - option_id: "C08_THRESHOLD_MAIN_01_D"
    label: "Abrir de golpe"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +2
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: -2
      threat_intimacy: +2
      creature_growth: 0
      door_pressure: +2
      creature_temperament: "immediate_manifest"
      zone_contamination_hall: +2
    unlocks: ["C08_CREATURE_FACE_01"]
    locks: []
    next_node: "C08_CREATURE_FACE_01"
echoes:
  tv:
    - "el silencio sustituye mejor a la TV que cualquier frase"
  night:
    - "todo el piso parece contener la respiración"
  exterior:
    - "afuera deja de importar como fuente de sentido"
notes: "La postura importa más que la valentía abstracta."
```

---

## 3. Árbol 02 — Criatura / primera respuesta verbal

### 3.1. Intención
La criatura debe responder como archivo vivo mal cosido. No puede aún soltar un monólogo limpio. Tiene que tantear al jugador con devolución de tono, deuda y forma de trato.

### 3.2. Nodo de respuesta inicial

```yaml
node_id: "C08_CREATURE_REPLY_01"
character: "Criatura"
phase: "night"
context: "El jugador ha hablado primero o ha escuchado con cercanía."
text: "La voz llega rota, como si probara una garganta prestada: '...aquí... ya... estabas...'"
subtext: "te reconozco / te he estado aprendiendo / quiero saber con qué vienes"
location_bias: "sealed_door"
related_zone: "hall"
recurrence_type: "main"
player_options:
  - option_id: "C08_CREATURE_REPLY_01_A"
    label: "'No sé qué eres, pero sé que vienes de aquí.'"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      guilt_noise: +1
      threat_intimacy: +2
      stability: -1
      creature_temperament: "reasoning_path"
      zone_contamination_hall: +1
    unlocks: ["C08_CREATURE_DIALOGUE_01"]
    locks: []
    next_node: "C08_CREATURE_DIALOGUE_01"
  - option_id: "C08_CREATURE_REPLY_01_B"
    label: "'Te oigo. Habla.'"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      loneliness_index: -1
      threat_intimacy: +2
      stability: -1
      creature_temperament: "listening_path"
      zone_contamination_hall: +1
    unlocks: ["C08_CREATURE_DIALOGUE_01"]
    locks: []
    next_node: "C08_CREATURE_DIALOGUE_01"
  - option_id: "C08_CREATURE_REPLY_01_C"
    label: "'No me vengas con mi voz.'"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: +1
      guilt_noise: +1
      threat_intimacy: +1
      stability: -1
      creature_temperament: "defensive_path"
      zone_contamination_hall: +1
    unlocks: ["C08_CREATURE_DIALOGUE_02"]
    locks: []
    next_node: "C08_CREATURE_DIALOGUE_02"
  - option_id: "C08_CREATURE_REPLY_01_D"
    label: "Quedarse callado"
    tone: "silence"
    effects:
      avoidance: +1
      confrontation: 0
      guilt_noise: +2
      loneliness_index: +1
      threat_intimacy: +2
      stability: -1
      creature_temperament: "absorption_path"
      zone_contamination_hall: +1
    unlocks: ["C08_CREATURE_DIALOGUE_03"]
    locks: []
    next_node: "C08_CREATURE_DIALOGUE_03"
notes: "La primera respuesta debe oler al historial dominante: cuidado, medición, banalidad rota o herida íntima."
```

### 3.3. Variante endurecida

```yaml
node_id: "C08_CREATURE_REPLY_02"
character: "Criatura"
phase: "night"
context: "El jugador intenta contener o bloquear antes de escuchar."
text: "Al otro lado no hay súplica inmediata. Hay una pausa de cálculo. Luego: 'Otra vez.'"
subtext: "ya sé lo que haces con lo que te incomoda / me has enseñado bien"
location_bias: "sealed_door"
related_zone: "hall"
recurrence_type: "variant"
player_options:
  - option_id: "C08_CREATURE_REPLY_02_A"
    label: "'No voy a dejar que salgas así.'"
    tone: "direct"
    effects:
      confrontation: +1
      guilt_noise: +1
      threat_intimacy: +1
      creature_temperament: "containment_path"
      door_pressure: +1
    unlocks: ["C08_CREATURE_DIALOGUE_02"]
    locks: []
    next_node: "C08_CREATURE_DIALOGUE_02"
  - option_id: "C08_CREATURE_REPLY_02_B"
    label: "Aflojar la contención y escuchar"
    tone: "delay"
    effects:
      avoidance: 0
      confrontation: +1
      threat_intimacy: +2
      creature_temperament: "listening_path"
    unlocks: ["C08_CREATURE_DIALOGUE_01"]
    locks: []
    next_node: "C08_CREATURE_DIALOGUE_01"
  - option_id: "C08_CREATURE_REPLY_02_C"
    label: "Insistir en sellar"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      guilt_noise: +2
      creature_temperament: "hostile_path"
      door_pressure: +2
    unlocks: ["C08_ENDING_CONTAINMENT_01", "C08_ENDING_RUPTURE_01"]
    locks: []
    next_node: "END"
```

---

## 4. Árbol 03 — Criatura / conversación principal

### 4.1. Intención
Aquí la criatura debe devolver la cualidad del trato: si el jugador ha sido más honesto, escucha; si ha sido evasivo, la criatura roba; si ha sido cruel, mide o invade; si ha sido doliente, suplica o duele.

### 4.2. Nodo de conversación abierta

```yaml
node_id: "C08_CREATURE_DIALOGUE_01"
character: "Criatura"
phase: "night"
context: "Se ha abierto un intercambio menos defensivo."
text: "'No me hiciste de una vez. Me fuiste dejando. Aquí. En todo.'"
subtext: "no vengo de fuera / soy la organización de tus residuos"
location_bias: "sealed_door -> threshold"
related_zone: "hall"
recurrence_type: "main"
player_options:
  - option_id: "C08_CREATURE_DIALOGUE_01_A"
    label: "'Lo sé.'"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +2
      guilt_noise: +1
      loneliness_index: -1
      threat_intimacy: +2
      creature_temperament: "soften_or_clarify"
    unlocks: ["C08_ENDING_OPEN_DIALOGUE_01", "C08_ENDING_COEXISTENCE_01"]
    locks: []
    next_node: "END"
  - option_id: "C08_CREATURE_DIALOGUE_01_B"
    label: "'No eres sólo mío.'"
    tone: "direct"
    effects:
      confrontation: +1
      guilt_noise: 0
      threat_intimacy: +1
      creature_temperament: "reasoning_path"
    unlocks: ["C08_ENDING_CONTAINMENT_01", "C08_ENDING_OPEN_DIALOGUE_01"]
    locks: []
    next_node: "END"
  - option_id: "C08_CREATURE_DIALOGUE_01_C"
    label: "'No puedo con todo esto.'"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      guilt_noise: +1
      loneliness_index: -1
      threat_intimacy: +2
      creature_temperament: "doliente_path"
    unlocks: ["C08_ENDING_COEXISTENCE_01", "C08_ENDING_ABSORPTION_01"]
    locks: []
    next_node: "END"
  - option_id: "C08_CREATURE_DIALOGUE_01_D"
    label: "Abrir el umbral y aceptar verla mejor"
    tone: "direct"
    effects:
      confrontation: +2
      stability: -2
      threat_intimacy: +3
      creature_temperament: "full_manifest"
    unlocks: ["C08_CREATURE_FACE_01"]
    locks: []
    next_node: "C08_CREATURE_FACE_01"
```

### 4.3. Nodo defensivo / hostil

```yaml
node_id: "C08_CREATURE_DIALOGUE_02"
character: "Criatura"
phase: "night"
context: "El jugador entra a la defensiva o intenta negarle legitimidad."
text: "'Entonces dime qué hice yo sola.'"
subtext: "si me niegas, tendrás que negar también todo lo demás"
location_bias: "threshold"
related_zone: "hall"
recurrence_type: "variant"
player_options:
  - option_id: "C08_CREATURE_DIALOGUE_02_A"
    label: "'No dijiste nada. Fui yo dejándolo todo ahí.'"
    tone: "direct"
    effects:
      confrontation: +2
      guilt_noise: +1
      threat_intimacy: +2
      creature_temperament: "soften"
    unlocks: ["C08_ENDING_OPEN_DIALOGUE_01", "C08_ENDING_CONTAINMENT_01"]
    locks: []
    next_node: "END"
  - option_id: "C08_CREATURE_DIALOGUE_02_B"
    label: "'No voy a darte razón.'"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: +1
      guilt_noise: +1
      creature_temperament: "harden"
      door_pressure: +1
    unlocks: ["C08_ENDING_RUPTURE_01", "C08_ENDING_CONTAINMENT_01"]
    locks: []
    next_node: "END"
  - option_id: "C08_CREATURE_DIALOGUE_02_C"
    label: "Callar y sostener la mirada/pausa"
    tone: "silence"
    effects:
      avoidance: 0
      confrontation: +1
      threat_intimacy: +2
      creature_temperament: "mirror_path"
    unlocks: ["C08_ENDING_ABSORPTION_01", "C08_ENDING_COEXISTENCE_01"]
    locks: []
    next_node: "END"
```

### 4.4. Nodo de absorción por exceso de escucha

```yaml
node_id: "C08_CREATURE_DIALOGUE_03"
character: "Criatura"
phase: "night"
context: "El jugador escucha demasiado y deja que la criatura gane la iniciativa semántica."
text: "La voz no pregunta primero. Ocupa hueco. 'Ya me oías antes. Sólo que entonces te salía llamarlo casa.'"
subtext: "si me dejas todo el espacio, hablaré con todo"
location_bias: "hall -> whole_apartment"
related_zone: "hall"
recurrence_type: "variant"
player_options:
  - option_id: "C08_CREATURE_DIALOGUE_03_A"
    label: "Responder por fin"
    tone: "direct"
    effects:
      confrontation: +1
      threat_intimacy: +2
      creature_temperament: "recover_dialogue"
    unlocks: ["C08_CREATURE_DIALOGUE_01"]
    locks: []
    next_node: "C08_CREATURE_DIALOGUE_01"
  - option_id: "C08_CREATURE_DIALOGUE_03_B"
    label: "Abrir y dejar que el encuentro ocurra"
    tone: "delay"
    effects:
      avoidance: 0
      confrontation: +1
      stability: -2
      threat_intimacy: +3
      creature_temperament: "absorption_path"
    unlocks: ["C08_ENDING_ABSORPTION_01", "C08_ENDING_COEXISTENCE_01"]
    locks: []
    next_node: "END"
  - option_id: "C08_CREATURE_DIALOGUE_03_C"
    label: "Retroceder e intentar bloquear tarde"
    tone: "evasiva"
    effects:
      avoidance: +2
      guilt_noise: +2
      creature_temperament: "hostile_path"
      door_pressure: +2
    unlocks: ["C08_ENDING_RUPTURE_01", "C08_ENDING_CONTAINMENT_01"]
    locks: []
    next_node: "END"
```

---

## 5. Árbol 04 — Criatura visible / umbral abierto

### 5.1. Intención
No hace falta describir modelo definitivo. Lo authored aquí debe fijar la lógica del encuentro visible: cuerpo coherente con historial, lenguaje incompleto y reacción al tono del jugador.

```yaml
node_id: "C08_CREATURE_FACE_01"
character: "Criatura"
phase: "night"
context: "El umbral se abre lo suficiente para que la criatura deje de ser sólo voz o marco."
text: "No hay revelación limpia. Hay una forma que reúne demasiado bien cosas que el jugador reconoce de la casa, del cuerpo y de su manera de tratar el mundo."
subtext: "por fin me miras sin la coartada de la madera"
location_bias: "sealed_room -> threshold"
related_zone: "sealed_door"
recurrence_type: "manifestation"
player_options:
  - option_id: "C08_CREATURE_FACE_01_A"
    label: "No apartar la vista"
    tone: "direct"
    effects:
      confrontation: +2
      threat_intimacy: +2
      stability: -2
      creature_temperament: "clarify"
    unlocks: ["C08_ENDING_OPEN_DIALOGUE_01", "C08_ENDING_COEXISTENCE_01"]
    locks: []
    next_node: "END"
  - option_id: "C08_CREATURE_FACE_01_B"
    label: "Intentar contener sin negar"
    tone: "direct"
    effects:
      confrontation: +1
      guilt_noise: +1
      threat_intimacy: +1
      creature_temperament: "contained_but_alive"
    unlocks: ["C08_ENDING_CONTAINMENT_01"]
    locks: []
    next_node: "END"
  - option_id: "C08_CREATURE_FACE_01_C"
    label: "Romper el encuentro"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: +1
      guilt_noise: +2
      creature_temperament: "hostile_path"
    unlocks: ["C08_ENDING_RUPTURE_01"]
    locks: []
    next_node: "END"
  - option_id: "C08_CREATURE_FACE_01_D"
    label: "Ceder proximidad"
    tone: "silence"
    effects:
      avoidance: 0
      confrontation: 0
      loneliness_index: -1
      threat_intimacy: +3
      creature_temperament: "absorption_path"
    unlocks: ["C08_ENDING_ABSORPTION_01", "C08_ENDING_COEXISTENCE_01"]
    locks: []
    next_node: "END"
```

---

## 6. Categorías de cierre authored

### 6.1. `C08_ENDING_CONTAINMENT_01`
Contención amarga. El jugador no destruye lo engendrado, pero le da un marco, un límite o una forma de coexistencia no expansiva. Funciona mejor con más honestidad y más cuidado tardío que negado.

### 6.2. `C08_ENDING_OPEN_DIALOGUE_01`
Apertura dialogada. El jugador sostiene palabra y reconocimiento. No limpia el daño, pero deja una resolución más legible, menos vengativa y más ética.

### 6.3. `C08_ENDING_COEXISTENCE_01`
Convivencia indecente. No hay cierre limpio; hay aceptación de que la grieta sigue en casa, quizá más tranquila, quizá sólo más nombrada.

### 6.4. `C08_ENDING_ABSORPTION_01`
Absorción. El jugador deja caer demasiada distancia o el monstruo ya la había disuelto. Puede ser íntimo, triste o terrorífico, pero nunca debe sentirse aleatorio.

### 6.5. `C08_ENDING_RUPTURE_01`
Ruptura hostil. El jugador intenta cortar, negar o violentar el encuentro. No es game over clásico; es una resolución más sucia, más reactiva y con resto duro en el piso.

---

## 7. Notas de dirección

- La criatura no gana por hablar más, sino por hablar **demasiado parecido** a cómo el mundo se le fue quedando dentro.
- El jugador no gana por abrir, sino por la manera en que abre, escucha, contiene o responde.
- Ningún final debe absolver por completo al jugador ni condenarlo con moralina de colegio.
- La habitación sellada debe pagar su promesa sin dejar de ser organismo y símbolo a la vez.

---

## 8. Cierre de diseño

El Ciclo 8 no termina con una revelación. Termina con una **relación estabilizada de una forma u otra**. La criatura final no es “el monstruo del piso”: es el modo en que el piso, el cuerpo y los vínculos han terminado aprendiendo a devolverse la palabra.
