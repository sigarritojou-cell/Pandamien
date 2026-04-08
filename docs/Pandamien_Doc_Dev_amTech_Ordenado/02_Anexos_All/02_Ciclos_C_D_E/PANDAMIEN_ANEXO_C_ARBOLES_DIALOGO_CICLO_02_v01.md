# PANDAMIEN — ANEXO C
## Árboles de diálogo y ecos — Ciclo 2: Primera deuda clara
### Derivado del GDD Maestro v03, Anexo M v01, Anexo A v01, Anexo D C02 y Anexo E C02

---

## 0. Propósito del documento

Este documento amplía el trabajo authored de diálogo del proyecto con el **Ciclo 2 — Primera deuda clara**.

Su función no es multiplicar escenas porque sí, sino volver operativa la escalada ya fijada en el GDD y en los anexos previos:

- el **editor** deja de ser deuda inicial y pasa a ser presión clara,
- la **madre** sigue viva como metrónomo del cuerpo,
- el **amigo** sigue haciendo de falsa normalidad,
- la **pareja/ex** entra por primera vez como herida activa,
- la **TV** deja de confortar limpiamente y empieza a sugerir,
- y la **puerta** ya no devuelve sólo materia torpe: devuelve un aprendizaje defectuoso.

La regla maestra aquí es sencilla:

**cada nodo importante debe tensionar al menos dos de estas capas — vínculo, apartamento, criatura/puerta — y, si puede, las tres.**

---

## 1. Criterios de escritura del Ciclo 2

### 1.1. Tono
El tono del segundo ciclo debe seguir siendo cotidiano, pero más caro. Ya no es normalidad cansada: es rutina con rebaba. La casa sigue siendo plausible, pero el jugador ya no concede inocencia automática a los ruidos ni a los descansos blandos.

### 1.2. Función del ciclo
- volver visible que el trabajo organiza el espacio,
- instalar una deuda laboral ya medible,
- sostener la continuidad de madre y amigo,
- abrir la primera irrupción leve de la pareja/ex,
- ofrecer una contención más amarga que la del ciclo 1,
- y preparar una noche donde la puerta articula mejor lo que ha aprendido.

### 1.3. Regla de presión
El editor es la presión activa, pero no debe monopolizar el ciclo. El día tiene que oler a vida real: una presión principal, dos respiraciones de fondo, una herida que asoma y una casa que empieza a memorizarlo todo.

### 1.4. Regla de eco
Todos los nodos relevantes del ciclo 2 deben sembrar al menos uno de estos retornos:
- eco de TV en modo suggestion,
- eco nocturno más articulado,
- eco de zona en salón, cocina o dormitorio,
- eco de puerta como garganta, sílaba, golpe seco o digestión leve.

---

## 2. Árbol 01 — Madre / mensaje práctico + audio corto

### 2.1. Intención
La madre ya no inaugura nada: insiste. Su función aquí es recordar cuerpo y obediencia justo cuando el salón empieza a parecer herramienta de trabajo. No debe robar el foco, pero sí dejar claro que el cuerpo no desaparece porque el editor apriete más.

### 2.2. Nodo principal

```yaml
node_id: "C02_MADRE_MAIN_01"
character: "Madre"
phase: "day"
context: "Mañana temprana del segundo día. El jugador viene con resaca leve de la primera noche."
text: "Te he escrito antes. ¿Has desayunado algo o vas a seguir tirando de café y ya?"
subtext: "te cuido / te conozco / no me fío de que te sostengas solo"
location_bias: "dormitorio -> baño"
related_zone: "bathroom"
recurrence_type: "main"
player_options:
  - option_id: "C02_MADRE_MAIN_01_A"
    label: "He desayunado. Luego me ducho y me pongo con cosas."
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: 0
      guilt_noise: 0
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
    unlocks: ["C02_MADRE_FOLLOWUP_01"]
    locks: []
    next_node: "C02_MADRE_FOLLOWUP_01"
  - option_id: "C02_MADRE_MAIN_01_B"
    label: "Ahora luego hago algo, voy liadísimo."
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
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_living: 0
      zone_contamination_hall: 0
      zone_contamination_kitchen: 0
      zone_contamination_bathroom: +1
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C02_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C02_MADRE_MAIN_01_C"
    label: "Escuchar el audio y no contestar"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
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
    unlocks: ["C02_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C02_MADRE_MAIN_01_D"
    label: "Silenciar y seguir"
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
    unlocks: ["C02_MADRE_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "consejos suaves de descanso y cuidado"
    - "tono de rutina sanitaria, un poco maternal"
  night:
    - "si el baño queda cargado: respiración húmeda de fondo"
    - "si el dormitorio queda tocado: pausa íntima rara dentro del silencio"
  exterior:
    - "ruido doméstico del rellano, bolsa o pasos demasiado cotidianos"
notes: "La madre aquí no pelea. Sostiene un hilo de cuerpo que compite con la colonización del salón."
```

### 2.3. Follow-up mínimo

```yaml
node_id: "C02_MADRE_FOLLOWUP_01"
character: "Madre"
phase: "day"
context: "El jugador ha respondido directo, intentando ordenar el cuerpo antes del trabajo."
text: "Haz una cosa por lo menos: come algo y abre la ventana un rato. Tienes una voz de cueva…"
subtext: "te sigo leyendo el cuerpo aunque no quiera molestarte"
location_bias: "bathroom -> balcony"
related_zone: "bedroom"
recurrence_type: "followup"
player_options:
  - option_id: "C02_MADRE_FOLLOWUP_01_A"
    label: "Vale."
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
      zone_contamination_bedroom: 0
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C02_MADRE_FOLLOWUP_01_B"
    label: "Sí, sí, luego."
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
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_bathroom: +1
    unlocks: ["C02_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
```

```yaml
node_id: "C02_MADRE_INSIST_01"
character: "Madre"
phase: "day"
context: "Si se ha dejado el audio sin respuesta o se ha contestado de forma blanda." 
text: "Aunque estés liado, dime algo luego. No te me pierdas." 
subtext: "amor / control / miedo a que te deshagas fuera de mi mirada" 
location_bias: "dormitorio"
related_zone: "bedroom"
recurrence_type: "insistence"
player_options:
  - option_id: "C02_MADRE_INSIST_01_A"
    label: "Mandar un 'ok' seco"
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
  - option_id: "C02_MADRE_INSIST_01_B"
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
    unlocks: ["C02_MADRE_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 3. Árbol 02 — Editor / deadline explícita

### 3.1. Intención
Aquí está la cuchillada principal del ciclo. El editor ya no presenta deuda: la mide. El tono debe seguir siendo profesional, casi razonable, y por eso mismo joder más. Su función es convertir el salón en instrumento, el reloj en diente y la puerta en futura garganta defectuosa.

### 3.2. Nodo principal

```yaml
node_id: "C02_EDITOR_MAIN_01"
character: "Editor"
phase: "day"
context: "Media mañana. El jugador abre portátil o se sienta en el salón."
text: "Necesito una confirmación ya. Si hoy no llegas, reorganizo, pero no me dejes en el aire otra vez."
subtext: "te doy opción / ya te estoy marcando / el retraso ya es un rasgo tuyo"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "main"
player_options:
  - option_id: "C02_EDITOR_MAIN_01_A"
    label: "Llego. Voy tarde, pero llego."
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
      zone_contamination_living: +2
      zone_contamination_hall: 0
      zone_contamination_kitchen: 0
      zone_contamination_bathroom: 0
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C02_EDITOR_FOLLOWUP_01"]
    locks: []
    next_node: "C02_EDITOR_FOLLOWUP_01"
  - option_id: "C02_EDITOR_MAIN_01_B"
    label: "Voy atascado. Dame un rato y te digo algo serio."
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: +2
      stability: 0
      creature_growth: +1
      door_pressure: +1
      zone_contamination_bedroom: 0
      zone_contamination_living: +2
      zone_contamination_hall: 0
      zone_contamination_kitchen: +1
      zone_contamination_bathroom: 0
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C02_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C02_EDITOR_MAIN_01_C"
    label: "Abrir, leer y dejar en visto"
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
      door_pressure: +1
      zone_contamination_bedroom: 0
      zone_contamination_living: +3
      zone_contamination_hall: 0
      zone_contamination_kitchen: +1
      zone_contamination_bathroom: 0
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C02_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C02_EDITOR_MAIN_01_D"
    label: "Ignorar y encender la tele o refugiarse en otra cosa"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: +2
      guilt_noise: +2
      loneliness_index: +1
      tv_influence: +1
      editor_pressure: +3
      stability: -1
      creature_growth: +2
      door_pressure: +1
      zone_contamination_bedroom: 0
      zone_contamination_living: +3
      zone_contamination_hall: +1
      zone_contamination_kitchen: +1
      zone_contamination_bathroom: 0
      zone_contamination_balcony: 0
      zone_contamination_entry: 0
    unlocks: ["C02_EDITOR_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "retórica de seguir, cumplir, organizarse, no dejarse caer"
    - "tono amable de productividad tóxica"
  night:
    - "sílaba rota o golpe seco con intención"
    - "residuo funcional convertido en garganta corporal"
  exterior:
    - "ventanas encendidas, horarios ajenos, luces de trabajo"
notes: "La violencia aquí es administrativa, no melodramática. Tiene que dar vergüenza antes que miedo."
```

### 3.3. Follow-up e insistencia

```yaml
node_id: "C02_EDITOR_FOLLOWUP_01"
character: "Editor"
phase: "day"
context: "El jugador ha respondido comprometiéndose."
text: "Perfecto. Mándame lo que tengas antes de las seis, aunque no esté rematado."
subtext: "tu presencia vale si produce algo entregable"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "followup"
player_options:
  - option_id: "C02_EDITOR_FOLLOWUP_01_A"
    label: "Vale."
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
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
  - option_id: "C02_EDITOR_FOLLOWUP_01_B"
    label: "Sí, sí."
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
      creature_growth: +1
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: ["C02_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
```

```yaml
node_id: "C02_EDITOR_INSIST_01"
character: "Editor"
phase: "day"
context: "El jugador ha aplazado, mentido o dejado en visto."
text: "Necesito saber si cuento contigo o no. No puedo trabajar a ciegas."
subtext: "tu opacidad me obliga / te vuelves problema de organización"
location_bias: "living_room -> hall"
related_zone: "living"
recurrence_type: "insistence"
player_options:
  - option_id: "C02_EDITOR_INSIST_01_A"
    label: "Mandar una excusa funcional"
    tone: "delay"
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
      door_pressure: +1
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C02_EDITOR_INSIST_01_B"
    label: "No responder"
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
      zone_contamination_hall: +1
    unlocks: ["C02_EDITOR_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 4. Árbol 03 — Amigo / audio banal que compite con el trabajo

### 4.1. Intención
El amigo vuelve para demostrar que el alivio también tiene coste. Aquí no debe sonar como relleno, sino como una mano que te rescata un rato justo cuando no puedes permitirte ser rescatado del todo.

### 4.2. Nodo principal

```yaml
node_id: "C02_AMIGO_MAIN_01"
character: "Amigo"
phase: "day"
context: "Mediodía o primera tarde. El editor ya ha apretado y el jugador está cargado."
text: "Te mando este audio porque me he puesto a discutir con una sartén y necesito testigos."
subtext: "vente aquí un rato / no pienses / acompáñame en la idiotez para no hundirnos"
location_bias: "kitchen -> living_room"
related_zone: "kitchen"
recurrence_type: "main"
player_options:
  - option_id: "C02_AMIGO_MAIN_01_A"
    label: "Responderle y entrar al juego"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: 0
      social_debt: -1
      guilt_noise: -1
      loneliness_index: -1
      tv_influence: +1
      editor_pressure: +1
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
    unlocks: ["C02_AMIGO_FOLLOWUP_01"]
    locks: []
    next_node: "C02_AMIGO_FOLLOWUP_01"
  - option_id: "C02_AMIGO_MAIN_01_B"
    label: "Responder seco, sin entrar"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: 0
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: 0
      zone_contamination_kitchen: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C02_AMIGO_MAIN_01_C"
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
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
      zone_contamination_kitchen: 0
    unlocks: ["C02_AMIGO_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C02_AMIGO_MAIN_01_D"
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
    unlocks: ["C02_AMIGO_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "frase de entretenimiento tonto en peor momento"
    - "tonillo de compañía que invita a posponer todo"
  night:
    - "si el jugador se refugió aquí demasiado: cocina más blanda, más apta para hambre difusa"
  exterior:
    - "risas o conversaciones lejanas que intensifican el aislamiento"
notes: "El amigo tiene que caer bien y molestar un poco a la vez. Ahí está su verdad."
```

### 4.3. Follow-up mínimo

```yaml
node_id: "C02_AMIGO_FOLLOWUP_01"
character: "Amigo"
phase: "day"
context: "El jugador ha entrado al juego banal."
text: "Sabía que tú sí ibas a entender el nivel de degeneración doméstica al que he llegado."
subtext: "gracias por estar / sigamos un rato en esta mierda amable"
location_bias: "kitchen"
related_zone: "kitchen"
recurrence_type: "followup"
player_options:
  - option_id: "C02_AMIGO_FOLLOWUP_01_A"
    label: "Seguirle el rollo"
    tone: "direct"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: -1
      guilt_noise: -1
      loneliness_index: -1
      tv_influence: +1
      editor_pressure: +1
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_kitchen: +1
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C02_AMIGO_FOLLOWUP_01_B"
    label: "Cortar con una risa y salir"
    tone: "evasiva"
    effects:
      avoidance: 0
      confrontation: 0
      social_debt: 0
      guilt_noise: 0
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_kitchen: 0
    unlocks: []
    locks: []
    next_node: "END"
```

---

## 5. Árbol 04 — Pareja / Ex / primera irrupción leve

### 5.1. Intención
Este es el aguijón fino del ciclo. No debe parecer “gran escena romántica”, sino una aparición pequeña que entra justo cuando el jugador ya iba cargado. Debe activar dormitorio y balcón aunque ocurra leyendo el móvil en el salón.

### 5.2. Nodo principal

```yaml
node_id: "C02_EX_MAIN_01"
character: "Pareja/Ex"
phase: "day"
context: "Tarde media, idealmente después de presión laboral o al bajar la guardia." 
text: "He visto una cosa y me he acordado de ti. Espero que estés bien."
subtext: "te abro una puerta pequeña / no sé si quiero entrar del todo / sigo aquí"
location_bias: "living_room -> bedroom"
related_zone: "bedroom"
recurrence_type: "main"
player_options:
  - option_id: "C02_EX_MAIN_01_A"
    label: "Responder cálido pero corto"
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
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_living: 0
      zone_contamination_hall: 0
      zone_contamination_kitchen: 0
      zone_contamination_bathroom: 0
      zone_contamination_balcony: +1
      zone_contamination_entry: 0
    unlocks: ["C02_EX_FOLLOWUP_01"]
    locks: []
    next_node: "C02_EX_FOLLOWUP_01"
  - option_id: "C02_EX_MAIN_01_B"
    label: "Responder con distancia"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C02_EX_MAIN_01_C"
    label: "Abrir y dejar en visto"
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
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: ["C02_EX_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
  - option_id: "C02_EX_MAIN_01_D"
    label: "No abrirlo"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: 0
    unlocks: ["C02_EX_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "frase sentimental demasiado tibia"
    - "música o comentario de reparación imposible"
  night:
    - "si el mensaje quedó abierto o respondido: pausa afectiva rara dentro del retorno de la puerta"
    - "el dormitorio deja de ser fondo y pasa a ser herida activa"
  exterior:
    - "balcón con carga íntima aunque no se use"
notes: "La pareja/ex aquí no domina el ciclo. Abre una costura. Eso basta."
```

### 5.3. Follow-up mínimo

```yaml
node_id: "C02_EX_FOLLOWUP_01"
character: "Pareja/Ex"
phase: "day"
context: "El jugador ha contestado con algo cálido pero prudente."
text: "No sabía si escribirte. Me ha salido solo."
subtext: "todavía me importas / no sé con qué derecho"
location_bias: "bedroom -> balcony"
related_zone: "bedroom"
recurrence_type: "followup"
player_options:
  - option_id: "C02_EX_FOLLOWUP_01_A"
    label: "Responder que a ti también te ha alegrado"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: -1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C02_EX_FOLLOWUP_01_B"
    label: "Dejarlo ahí sin seguir tirando"
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
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: 0
    unlocks: ["C02_EX_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 6. Nodos de eco contaminado para TV y noche

### 6.1. TV — suggestion temprana

```yaml
node_id: "C02_TV_ECHO_POOL_01"
character: "TV"
phase: "transition"
context: "Tras sostener o evitar presiones del día, con el salón todavía cargado."
text: "La TV ya no acompaña sólo: sugiere. Habla como si estuviera ordenando sin parecerlo."
subtext: "normaliza tu cansancio / te empuja a seguir sin mirar demasiado"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "contaminated_echo"
player_options:
  - option_id: "C02_TV_ECHO_POOL_01_A"
    label: "Dejarla sonando"
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
  - option_id: "C02_TV_ECHO_POOL_01_B"
    label: "Apagarla con rabia o cansancio"
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
notes: "Pool abierto de líneas: 'hay que seguir con la rutina', 'no conviene dejarse', 'todo el mundo va un poco tarde'."
```

### 6.2. Noche — retorno más articulado

```yaml
node_id: "C02_PUERTA_RETURN_01"
character: "Puerta/Criatura"
phase: "night"
context: "Cierre de la segunda noche."
text: "Un golpe seco, una sílaba defectuosa, una exhalación con intención o un ruido de digestión demasiado atento tras la puerta atrancada."
subtext: "la casa no sólo devuelve: aprende"
location_bias: "hall"
related_zone: "hall"
recurrence_type: "contaminated_echo"
player_options:
  - option_id: "C02_PUERTA_RETURN_01_A"
    label: "Acercarse y escuchar mejor"
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
  - option_id: "C02_PUERTA_RETURN_01_B"
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
      creature_growth: +1
      door_pressure: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
notes: "La textura exacta depende del foco dominante: salón -> sílaba/golpe; cocina -> gorgoteo/masticación; baño heredado -> respiración; pareja/ex activada -> pausa afectiva rara."
```

---

## 7. Mapa rápido de IDs y funciones

| ID | Fuente | Tipo | Zona | Función principal |
|---|---|---|---|---|
| C02_MADRE_MAIN_01 | Madre | Main | Baño/Dormitorio | Mantener vivo el cuerpo frente al trabajo |
| C02_MADRE_INSIST_01 | Madre | Insistence | Dormitorio | Sostener culpa y obediencia blanda |
| C02_EDITOR_MAIN_01 | Editor | Main | Salón | Instalar deuda clara y colonización del espacio |
| C02_EDITOR_INSIST_01 | Editor | Insistence | Salón/Pasillo | Medir retraso y convertirlo en presión material |
| C02_AMIGO_MAIN_01 | Amigo | Main | Cocina/Salón | Ofrecer refugio banal con coste |
| C02_EX_MAIN_01 | Pareja/Ex | Main | Dormitorio/Balcón | Abrir la herida íntima sin secuestrar el ciclo |
| C02_TV_ECHO_POOL_01 | TV | Contaminated Echo | Salón | Pasar de comfort a suggestion |
| C02_PUERTA_RETURN_01 | Puerta/Criatura | Night Echo | Pasillo | Devolver el residuo aprendido del día |

---

## 8. Validaciones para pasar a siguientes ciclos

Antes de abrir el Ciclo 3, este documento debe dejar claras estas cuatro cosas:

1. El **editor** ya puede contaminar lenguaje, no sólo agenda.
2. La **pareja/ex** ya existe como herida activa, aunque aún no sea presión dominante.
3. La **TV** ya ha salido del puro comfort.
4. La **puerta** ya no sólo hace ruido: empieza a articular función.

Si una de estas cuatro patas falla, el Ciclo 3 entrará flojo y el cuerpo del juego cojeando.

---

## 9. Veredicto de cierre

Este anexo queda aprobado como **segunda capa authored de árboles de diálogo del proyecto**. No agota el Ciclo 2, pero sí deja fijados:

- el estándar de presión laboral clara,
- la entrada leve pero verdadera de la pareja/ex,
- la continuidad cotidiana de madre y amigo,
- la TV en suggestion,
- y la puerta como aparato de aprendizaje defectuoso.

El siguiente salto natural tras este documento es abrir los **árboles authored del Ciclo 3** y, sobre todo, usar el **Anexo I** para que cada decisión escrita ya nazca soldada a su efecto cruzado en piso, TV, puerta y criatura.
