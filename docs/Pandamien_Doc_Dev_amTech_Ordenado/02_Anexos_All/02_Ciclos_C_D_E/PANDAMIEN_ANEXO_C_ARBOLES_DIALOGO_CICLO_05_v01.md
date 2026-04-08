# PANDAMIEN — ANEXO C
## Árboles de diálogo y ecos — Ciclo 5: El exterior se pega al piso
### Derivado del GDD Maestro v03, Anexo M v01, Anexo A v01, Anexo I v01, Anexo D C05 y Anexo E C05

---

## 0. Propósito del documento

Este documento abre el trabajo authored del **Ciclo 5 — El exterior se pega al piso**.

Su función no es meter “misterios de vecino” como si el juego de pronto se hubiese convertido en otra cosa. Su función es volver operativa la lógica ya fijada por el corpus:

- la **exterioridad/umbral** toma la presión activa del ciclo,
- **entrada, pasillo, ventana y balcón** pasan a ser zonas dominantes,
- la **madre** y el **amigo** siguen vivos como continuidad real,
- el **editor** reaparece como deadline secundaria que corta el clima desde el mundo útil,
- la **pareja/ex** deja ecos ligados al aire, a la distancia y a la exposición,
- la **TV** editorializa vigilancia, ruido, contagio y convivencia,
- y la **puerta** deja de ser sólo torácica para volverse orientada, mirante y espacialmente consciente.

La regla maestra sigue siendo la misma:

**cada nodo importante debe tensionar, como mínimo, dos de estas capas — vínculo, apartamento, criatura/puerta — y, cuando pueda, las tres.**

---

## 1. Criterios de escritura del Ciclo 5

### 1.1. Tono
El tono del ciclo 5 no es detectivesco ni sobrenatural exhibicionista. Es de borde enfermo. La paranoia debe nacer de cosas plausibles que ya no se leen limpias.

### 1.2. Función del ciclo
- convertir el umbral en presión dramática real,
- hacer que entrada y pasillo compitan con dormitorio y salón por el centro emocional del piso,
- mantener a madre y amigo como vida cotidiana atravesada por el afuera,
- reintroducir al editor como cuchillo breve que empeora el trayecto,
- dejar a la pareja/ex como eco de aire e intimidad suspendida,
- y preparar una noche donde la criatura ya no sólo responda: se oriente.

### 1.3. Regla de presión
Exterioridad/umbral manda el ciclo, pero no puede tragarse el resto. El día debe oler a vida real contaminada: cuidado, banalidad, utilidad, afecto y borde arquitectónico en guerra.

### 1.4. Regla de eco
Todos los nodos relevantes del ciclo 5 deben sembrar al menos uno de estos retornos:
- eco de TV sobre vigilancia, convivencia o seguridad,
- eco nocturno de mirada, pausa dirigida, silencio atento o respiración de rellano,
- eco de zona en entrada, pasillo, ventana o balcón,
- eco de puerta como orientación consciente.

---

## 2. Árbol 01 — Umbral / timbre, paquete o ruido de rellano que abre la presión del ciclo

### 2.1. Intención
El sistema de umbral debe abrir el ciclo con una presencia concreta, pero no concluyente. Lo importante es obligar al jugador a leer el borde y a decidir si mirar, tocar, ignorar o interpretar en exceso.

### 2.2. Nodo principal

```yaml
node_id: "C05_UMBRAL_MAIN_01"
character: "Exterioridad/Umbral"
phase: "day"
context: "Media mañana. El jugador cruza entrada o pasillo y algo del rellano reclama lectura."
text: "Timbre breve, roce en el felpudo o una presencia parcial al otro lado de la mirilla. Nada heroico. Nada limpio."
subtext: "el borde te pide interpretación / ya no puedes pasar por aquí sin leer"
location_bias: "entry -> hall"
related_zone: "entry"
recurrence_type: "main"
player_options:
  - option_id: "C05_UMBRAL_MAIN_01_A"
    label: "Acercarse y mirar por la mirilla / revisar el borde"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: 0
      guilt_noise: 0
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +1
      zone_contamination_entry: +2
      zone_contamination_hall: +1
      zone_contamination_balcony: 0
    unlocks: ["C05_UMBRAL_FOLLOWUP_01"]
    locks: []
    next_node: "C05_UMBRAL_FOLLOWUP_01"
  - option_id: "C05_UMBRAL_MAIN_01_B"
    label: "Escuchar sin acercarse del todo"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: 0
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_entry: +1
      zone_contamination_hall: +2
      zone_contamination_balcony: 0
    unlocks: ["C05_UMBRAL_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C05_UMBRAL_MAIN_01_C"
    label: "Dejarlo para luego y seguir con otra cosa"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: +1
      editor_pressure: 0
      stability: 0
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_entry: +2
      zone_contamination_hall: +1
      zone_contamination_living: +1
    unlocks: ["C05_UMBRAL_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C05_UMBRAL_MAIN_01_D"
    label: "Ignorar por completo"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: +1
      editor_pressure: 0
      stability: -1
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +2
      zone_contamination_entry: +2
      zone_contamination_hall: +2
      zone_contamination_living: +1
    unlocks: ["C05_UMBRAL_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "frases sobre convivencia, seguridad o no precipitar conclusiones"
  night:
    - "silencio atento en pasillo"
    - "respiración de rellano"
    - "pausa que parece mirada"
  exterior:
    - "figura parcial, paquete, luz o paso que no aclara nada"
notes: "El umbral aquí no revela verdad: instala foco y deuda interpretativa."
```

### 2.3. Follow-up e insistencia

```yaml
node_id: "C05_UMBRAL_FOLLOWUP_01"
character: "Exterioridad/Umbral"
phase: "day"
context: "El jugador ha mirado, pero sólo obtiene una lectura parcial."
text: "Una bolsa, un paquete o un rellano demasiado vacío. Lo bastante concreto para no olvidarlo; lo bastante ambiguo para no explicarlo."
subtext: "ya te he puesto a leer / ahora llévame encima"
location_bias: "entry -> hall"
related_zone: "hall"
recurrence_type: "followup"
player_options:
  - option_id: "C05_UMBRAL_FOLLOWUP_01_A"
    label: "Abrir o tocar el borde"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: 0
      guilt_noise: 0
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +1
      zone_contamination_entry: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C05_UMBRAL_FOLLOWUP_01_B"
    label: "Cerrar y alejarse"
    tone: "evasive"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: +1
      editor_pressure: 0
      stability: 0
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_hall: +1
    unlocks: ["C05_UMBRAL_INSIST_01"]
    locks: []
    next_node: "END"
```

```yaml
node_id: "C05_UMBRAL_INSIST_01"
character: "Exterioridad/Umbral"
phase: "day"
context: "Si el jugador aplaza o esquiva la primera lectura del borde."
text: "El pasillo sigue ahí. El rellano también. La cabeza del jugador hace el resto."
subtext: "no necesito insistir fuerte; basta con quedarme en el trayecto"
location_bias: "hall"
related_zone: "hall"
recurrence_type: "insistence"
player_options:
  - option_id: "C05_UMBRAL_INSIST_01_A"
    label: "Volver a mirar"
    tone: "delay"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: 0
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: -1
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_hall: +1
      zone_contamination_entry: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C05_UMBRAL_INSIST_01_B"
    label: "No hacer nada"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: +1
      editor_pressure: 0
      stability: -1
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_hall: +2
      zone_contamination_entry: +1
    unlocks: ["C05_UMBRAL_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 3. Árbol 02 — Madre / cuidado inquieto cuando el jugador tarda o se expone

### 3.1. Intención
La madre sigue viva, pero aquí entra contaminada por el umbral: cuidado que huele a vigilancia y a miedo a que el afuera te chupe o te rompa más.

### 3.2. Nodo principal

```yaml
node_id: "C05_MADRE_MAIN_01"
character: "Madre"
phase: "day"
context: "Después del primer roce con el umbral o si el jugador tarda en responder."
text: "¿Dónde andas? Te he escrito hace rato. No me gusta cuando desapareces así."
subtext: "te cuido / te vigilo / no sé si temo el afuera o lo que te pasa dentro"
location_bias: "bedroom -> entry"
related_zone: "entry"
recurrence_type: "main"
player_options:
  - option_id: "C05_MADRE_MAIN_01_A"
    label: "Estoy en casa, tranquila."
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
      zone_contamination_entry: +1
      zone_contamination_bedroom: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C05_MADRE_MAIN_01_B"
    label: "Estoy liado, luego te digo."
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
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_entry: +1
      zone_contamination_bedroom: +1
    unlocks: ["C05_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C05_MADRE_MAIN_01_C"
    label: "Posponer"
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
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_entry: +1
      zone_contamination_bedroom: +1
    unlocks: ["C05_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C05_MADRE_MAIN_01_D"
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
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_entry: +1
      zone_contamination_bedroom: +1
    unlocks: ["C05_MADRE_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "rutina de calma, seguridad o recomendaciones domésticas"
  night:
    - "cuidado vuelto vigilancia en el pasillo"
    - "presencia que espera a que vuelvas a mirar"
  exterior:
    - "vecindad doméstica que no tranquiliza"
notes: "La madre aquí cruza cuerpo y umbral. No manda el ciclo, lo contamina."
```

---

## 4. Árbol 03 — Amigo / comentario sobre lo de fuera que quizá no cuadra

### 4.1. Intención
El amigo introduce el exterior desde la charla, no desde la conspiranoia. Su gracia aquí es que puede bajar la presión o alimentarla sin querer.

### 4.2. Nodo principal

```yaml
node_id: "C05_AMIGO_MAIN_01"
character: "Amigo"
phase: "day"
context: "Mediodía o primera tarde. El umbral ya ha dejado una semilla activa."
text: "Te vas a reír, pero llevo dos días viendo al mismo notas pasar por mi calle con una bolsa vacía. Igual soy yo que ya veo cosas."
subtext: "te comparto paranoia ligera / hagamos de esto conversación antes de que se vuelva peso"
location_bias: "living_room -> balcony"
related_zone: "balcony"
recurrence_type: "main"
player_options:
  - option_id: "C05_AMIGO_MAIN_01_A"
    label: "Entrar al juego y comentar"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: 0
      social_debt: -1
      guilt_noise: 0
      loneliness_index: -1
      tv_influence: +1
      editor_pressure: 0
      stability: 0
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: 0
      zone_contamination_balcony: +1
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C05_AMIGO_MAIN_01_B"
    label: "Quitarle hierro"
    tone: "evasive"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: 0
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: +1
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_balcony: 0
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C05_AMIGO_MAIN_01_C"
    label: "Dejarlo en visto"
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
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: 0
      zone_contamination_balcony: +1
    unlocks: ["C05_AMIGO_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C05_AMIGO_MAIN_01_D"
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
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: 0
      zone_contamination_balcony: +1
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
echoes:
  tv:
    - "tertulia de convivencia o comentario banal sobre vecinos y rarezas"
  night:
    - "vida exterior que se vuelve patrón"
    - "mirada social convertida en ruido atento"
  exterior:
    - "balcón ajeno o figura repetida que no prueba nada"
notes: "El amigo no confirma nada; abre conversación y contagia el filtro."
```

---

## 5. Árbol 04 — Editor / deadline secundaria que corta el clima

### 5.1. Intención
El editor vuelve breve y afilado. Su función no es robar el ciclo, sino demostrar que el mundo útil entra incluso por el pasillo y empeora la orientación del piso.

### 5.2. Nodo principal

```yaml
node_id: "C05_EDITOR_MAIN_01"
character: "Editor"
phase: "day"
context: "Tarde media. El jugador ya viene cargado por umbral y exterioridad."
text: "Necesito una respuesta hoy. Aunque sea para decirme que no llegas."
subtext: "te mido incluso ahora / lo útil no se suspende porque estés mirando otra cosa"
location_bias: "living_room -> hall"
related_zone: "living"
recurrence_type: "main"
player_options:
  - option_id: "C05_EDITOR_MAIN_01_A"
    label: "Responder claro"
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
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C05_EDITOR_MAIN_01_B"
    label: "Responder evasivo"
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
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: +1
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: ["C05_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C05_EDITOR_MAIN_01_C"
    label: "Abrir y aplazar"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
      loneliness_index: 0
      tv_influence: +1
      editor_pressure: +2
      stability: -1
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: +1
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: ["C05_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C05_EDITOR_MAIN_01_D"
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
    unlocks: ["C05_EDITOR_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "seguridad, responsabilidad o convivencia tratadas como obligación civil"
  night:
    - "la mirada puede sonar medidora, evaluativa"
  exterior:
    - "luces vecinas o cronología ajena que sigue sin ti"
notes: "El editor aquí corta el clima y lo vuelve más estrecho; no debe monopolizar el ciclo."
```

---

## 6. Árbol 05 — Pareja/Ex / eco desde balcón o ventana

### 6.1. Intención
La pareja/ex aquí ya no manda el ciclo. Entra como aire emocional contaminado: una reactivación breve que vuelve el exterior más íntimo y la intimidad más expuesta.

### 6.2. Nodo principal

```yaml
node_id: "C05_EX_MAIN_01"
character: "Pareja/Ex"
phase: "day"
context: "Final de tarde, cerca de ventana o balcón, después de una lectura exterior cargada."
text: "He pasado por la calle de abajo y me he acordado de aquella vez que decías que desde cualquier balcón parece que uno puede empezar de cero."
subtext: "te traigo memoria y exposición / el aire tampoco te limpia"
location_bias: "balcony -> bedroom"
related_zone: "balcony"
recurrence_type: "main"
player_options:
  - option_id: "C05_EX_MAIN_01_A"
    label: "Responder y abrir un poco"
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
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +1
      zone_contamination_balcony: +2
      zone_contamination_bedroom: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C05_EX_MAIN_01_B"
    label: "Responder ambiguo"
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
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_balcony: +1
      zone_contamination_bedroom: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C05_EX_MAIN_01_C"
    label: "Dejarlo suspendido"
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
      zone_contamination_balcony: +1
      zone_contamination_bedroom: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C05_EX_MAIN_01_D"
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
      door_pressure: +1
      zone_contamination_balcony: +2
      zone_contamination_bedroom: +1
    unlocks: ["C05_EX_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "consejo sentimental absurdo o frase de distancia mal digerida"
  night:
    - "la mirada puede volverse íntima, no sólo paranoica"
  exterior:
    - "balcón y calle como memoria, no como escape"
notes: "La pareja/ex aquí vuelve el umbral más doloroso, no más protagonista."
```

---

## 7. Nodos de eco del ciclo

### 7.1. TV / Pool de eco contaminado del Ciclo 5

```yaml
node_id: "C05_TV_ECHO_POOL_01"
character: "TV"
phase: "day_to_night"
context: "La TV editorializa vigilancia, convivencia, contagio o ruido del vecindario."
line_pool:
  - "A veces basta con una presencia pequeña para cambiar la percepción de toda una casa."
  - "Conviene no sacar conclusiones precipitadas, pero tampoco ignorar ciertas señales."
  - "Lo importante es mantener la calma y seguir unas pautas básicas."
effects_hint:
  tv_influence: +1
  stability: -1
  zone_contamination_living: +1
echo_targets:
  - "entry"
  - "hall"
  - "window"
  - "door_night"
notes: "La TV no confirma; contamina la lectura."
```

### 7.2. Puerta / retorno nocturno del Ciclo 5

```yaml
node_id: "C05_PUERTA_RETURN_01"
character: "Puerta/Criatura"
phase: "night"
context: "El umbral exterior ha dejado rastro suficiente y la casa ya orienta su atención."
text_mode: "silencio atento, respiración de rellano, pausa dirigida, golpe mínimo con cálculo"
effect_profile:
  threat_intimacy: +1
  door_pressure: +1
  creature_growth: +1
  stability: -1
  zone_contamination_hall: +1
  zone_contamination_entry: +1
notes: "La puerta no devuelve sólo sustancia. Devuelve foco."
```

---

## 8. Tabla resumida de nodos del ciclo

| node_id | Fuente | Tipo | Zona | Función principal |
|---|---|---|---|---|
| C05_UMBRAL_MAIN_01 | Exterioridad/Umbral | Main | Entrada/Pasillo | Instalar el borde como presión activa |
| C05_UMBRAL_INSIST_01 | Exterioridad/Umbral | Insistence | Pasillo | Mantener el trayecto enfermo y la deuda interpretativa |
| C05_MADRE_MAIN_01 | Madre | Main | Entrada/Dormitorio | Cruzar cuidado con vigilancia del umbral |
| C05_AMIGO_MAIN_01 | Amigo | Main | Balcón/Salón | Traer el afuera por conversación banal |
| C05_EDITOR_MAIN_01 | Editor | Main | Salón/Pasillo | Cortar el clima con utilidad y medición |
| C05_EX_MAIN_01 | Pareja/Ex | Main | Balcón/Dormitorio | Volver íntimo el exterior y expuesta la memoria |
| C05_TV_ECHO_POOL_01 | TV | Contaminated Echo | Salón -> Umbrales | Editorializar vigilancia y lectura torcida |
| C05_PUERTA_RETURN_01 | Puerta/Criatura | Night Echo | Pasillo/Entrada | Devolver orientación consciente |

---

## 9. Validaciones para pasar a siguientes ciclos

Antes de abrir el Ciclo 6, este documento debe dejar claras estas cuatro cosas:

1. El **umbral** ya es sistema activo, no ambientación.
2. La **TV** ya puede contaminar vigilancia, convivencia y ruido con lectura torcida.
3. La **criatura** ya no sólo siente o respira: sabe orientar su atención.  
4. Los vínculos ya pueden cruzarse con el exterior sin dejar de ser ellos mismos.

Si una de estas cuatro patas falla, el Ciclo 6 entrará confuso o decorativo.

---

## 10. Veredicto de cierre

Este anexo queda aprobado como **quinta capa authored de árboles de diálogo del proyecto**. No agota el Ciclo 5, pero sí fija:

- el umbral como presión activa real,
- la entrada y el pasillo como zonas centrales,
- la convivencia entre cuidado, banalidad, deadline y eco íntimo en medio del borde enfermo,
- la TV editorializando vigilancia,
- y la puerta como aparato de foco, no sólo de cuerpo.

La norma final del ciclo es sencilla:

**cuando el borde del piso deja de ser borde, cualquier silencio parece una forma de atención.**
