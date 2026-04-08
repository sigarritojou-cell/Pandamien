# PANDAMIEN — ANEXO C
## Árboles de diálogo y ecos — Ciclo 3: El cuerpo entra en juego
### Derivado del GDD Maestro v03, Anexo M v01, Anexo A v01, Anexo I v01, Anexo D C03 y Anexo E C03

---

## 0. Propósito del documento

Este documento abre el trabajo authored del **Ciclo 3 — El cuerpo entra en juego**.

Su función no es inflar el guion por inercia, sino volver operativa la deriva ya fijada por el corpus:

- la **madre** pasa a presión activa del ciclo,
- el **cuerpo** deja de ser contexto y se vuelve material dramático,
- el **editor** persiste como deuda latente y vergüenza funcional,
- el **amigo** sigue ofreciendo falsa normalidad,
- la **pareja/ex** entra en el tejido cotidiano justo cuando peor sienta,
- la **TV** se vuelve más clínica o tranquilizadora,
- y la **puerta** responde con organicidad íntima: respiración, humedad, pecho o latido.

La regla maestra aquí sigue siendo la misma:

**cada nodo importante debe tensionar, como mínimo, dos de estas capas — vínculo, apartamento, criatura/puerta — y, cuando sea posible, las tres.**

---

## 1. Criterios de escritura del Ciclo 3

### 1.1. Tono
El tono del ciclo 3 no es de “gran horror corporal”. Es de saturación. Todo sigue siendo verosímil, reconocible y pequeño, pero ya no cabe leerlo como simple cansancio neutral.

### 1.2. Función del ciclo
- poner al cuerpo en primer plano,
- hacer que madre y medicación pesen sin convertirse en exposición médica,
- dejar al editor como deuda interna, no sólo externa,
- mantener al amigo vivo como respiración banal,
- permitir que la pareja/ex entre donde menos espacio emocional queda,
- y preparar una noche donde la criatura ya se sienta más orgánica que abstracta.

### 1.3. Regla de presión
La madre/cuerpo es la presión activa, pero el ciclo debe conservar tejido de vida: trabajo pendiente, mensajes pequeños, intimidad incómoda y televisión que sugiere descanso o corte.

### 1.4. Regla de eco
Todos los nodos relevantes del ciclo 3 deben sembrar al menos uno de estos retornos:
- eco de TV clínico o tranquilizador,
- eco nocturno de respiración, humedad, pecho o latido,
- eco de zona en baño, dormitorio o pasillo,
- eco de puerta más íntimo y más corporal.

---

## 2. Árbol 01 — Madre / llamada larga o audio de cuidado insistente

### 2.1. Intención
La madre toma aquí la presión activa. No porque grite más, sino porque su lectura del cuerpo se vuelve demasiado exacta. Tiene que pesar como mezcla de amor, miedo, costumbre y derecho viejo sobre el cuerpo del protagonista.

### 2.2. Nodo principal

```yaml
node_id: "C03_MADRE_MAIN_01"
character: "Madre"
phase: "day"
context: "Mañana media. El jugador aún no ha recompuesto del todo cuerpo ni piso."
text: "No tienes buena voz. ¿Has dormido algo o has vuelto a pasar la noche fatal? Dime la verdad, por favor."
subtext: "te cuido / te leo / no te creo del todo / tu cuerpo sigue entrando en mi jurisdicción"
location_bias: "dormitorio -> baño"
related_zone: "bathroom"
recurrence_type: "main"
player_options:
  - option_id: "C03_MADRE_MAIN_01_A"
    label: "He dormido mal, pero estoy tirando."
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
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_bathroom: +1
    unlocks: ["C03_MADRE_FOLLOWUP_01"]
    locks: []
    next_node: "C03_MADRE_FOLLOWUP_01"
  - option_id: "C03_MADRE_MAIN_01_B"
    label: "Estoy bien, sólo voy liado."
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
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_bathroom: +2
    unlocks: ["C03_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C03_MADRE_MAIN_01_C"
    label: "Escuchar y decir que luego hablas"
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
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_bathroom: +1
    unlocks: ["C03_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C03_MADRE_MAIN_01_D"
    label: "No coger o silenciar"
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
      zone_contamination_bedroom: +1
      zone_contamination_bathroom: +2
    unlocks: ["C03_MADRE_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "consejos de descanso, comida o autocuidado"
    - "tono clínico suave o casi maternal"
  night:
    - "respiración húmeda"
    - "presencia de pecho o cuidado intrusivo detrás de la puerta"
  exterior:
    - "eco doméstico de rellano, medicación o cuidado ajeno"
notes: "La madre no aprieta como amenaza externa; aprieta porque sabe leer el cuerpo cuando el jugador ya no quiere leerse."
```

### 2.3. Follow-up e insistencia

```yaml
node_id: "C03_MADRE_FOLLOWUP_01"
character: "Madre"
phase: "day"
context: "El jugador admite algo de malestar."
text: "Entonces hazme caso una vez: dúchate, come algo y no esperes a estar hecho polvo."
subtext: "te doy una orden que se disfraza de cuidado"
location_bias: "bathroom"
related_zone: "bathroom"
recurrence_type: "followup"
player_options:
  - option_id: "C03_MADRE_FOLLOWUP_01_A"
    label: "Vale, lo hago."
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: -1
      guilt_noise: 0
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bathroom: -1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C03_MADRE_FOLLOWUP_01_B"
    label: "Sí, ahora luego."
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
      zone_contamination_bedroom: +1
    unlocks: ["C03_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
```

```yaml
node_id: "C03_MADRE_INSIST_01"
character: "Madre"
phase: "day"
context: "Si se ha aplazado o ignorado el cuidado."
text: "Luego no me digas que te encontrabas fatal y no hiciste ni lo mínimo."
subtext: "amor cansado / reproche preventivo / yo ya veía esto venir"
location_bias: "bedroom"
related_zone: "bedroom"
recurrence_type: "insistence"
player_options:
  - option_id: "C03_MADRE_INSIST_01_A"
    label: "Mandar un 'sí, ya'"
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
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bedroom: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C03_MADRE_INSIST_01_B"
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
      zone_contamination_bedroom: +1
      zone_contamination_bathroom: +1
    unlocks: ["C03_MADRE_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 3. Árbol 02 — Editor / deuda latente que ya vive dentro

### 3.1. Intención
El editor en C03 no manda el día, pero sí mancha su fondo. Su función es demostrar que el trabajo no se fue: se ha vuelto vergüenza interiorizada, mala respiración y sensación de ir tarde incluso dentro del baño.

### 3.2. Nodo principal

```yaml
node_id: "C03_EDITOR_MAIN_01"
character: "Editor"
phase: "day"
context: "Final de mañana o primera tarde. El jugador ya arrastra cuerpo."
text: "Avísame en cuanto sepas si hoy sale algo. Necesito poder contar con ello o enterrarlo."
subtext: "tu retraso ya no es sorpresa; es una variable de trabajo"
location_bias: "living_room -> hall"
related_zone: "living"
recurrence_type: "main"
player_options:
  - option_id: "C03_EDITOR_MAIN_01_A"
    label: "Hoy voy muy justo. Te digo algo en cuanto pueda."
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
    unlocks: ["C03_EDITOR_FOLLOWUP_01"]
    locks: []
    next_node: "C03_EDITOR_FOLLOWUP_01"
  - option_id: "C03_EDITOR_MAIN_01_B"
    label: "Sí, sí, luego te paso algo."
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: +1
      stability: -1
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: ["C03_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C03_EDITOR_MAIN_01_C"
    label: "Abrir y dejarlo flotando"
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
      zone_contamination_living: +2
      zone_contamination_hall: +1
    unlocks: ["C03_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C03_EDITOR_MAIN_01_D"
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
    unlocks: ["C03_EDITOR_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "tono de seguir funcionando aunque no puedas"
    - "productividad mezclada con descanso culpable"
  night:
    - "respiración trabajosa o ritmo cortado dentro del retorno corporal"
  exterior:
    - "ventanas activas o rutinas ajenas que siguen sin ti"
notes: "Aquí el editor debe doler más por cansancio que por agenda."
```

### 3.3. Follow-up mínimo

```yaml
node_id: "C03_EDITOR_FOLLOWUP_01"
character: "Editor"
phase: "day"
context: "El jugador ha respondido sin desaparecer del todo."
text: "Entendido. Sólo no me dejes esperando otra vez sin una línea."
subtext: "lo mínimo exigible sigue siendo disponibilidad"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "followup"
player_options:
  - option_id: "C03_EDITOR_FOLLOWUP_01_A"
    label: "No te dejo tirado."
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
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C03_EDITOR_FOLLOWUP_01_B"
    label: "Sí."
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
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: ["C03_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
```

---

## 4. Árbol 03 — Amigo / banalidad que choca con la fatiga

### 4.1. Intención
El amigo tiene que seguir vivo, pero su tono ya no cae igual. Lo banal puede aliviar o resultar casi violento por contraste con el cuerpo que se cae a cachos por dentro.

### 4.2. Nodo principal

```yaml
node_id: "C03_AMIGO_MAIN_01"
character: "Amigo"
phase: "day"
context: "Mediodía o tarde temprana, cuando el jugador está cansado y ya ha pasado por el cuerpo o lo ha evitado."
text: "Te juro que acabo de hablarle a la nevera como si fuera una persona. Si esto no se acaba me caso con un electrodoméstico."
subtext: "ven aquí un segundo / no te hundas / hagamos chiste antes de oler lo demás"
location_bias: "kitchen -> living_room"
related_zone: "kitchen"
recurrence_type: "main"
player_options:
  - option_id: "C03_AMIGO_MAIN_01_A"
    label: "Responderle y seguir la broma"
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
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_kitchen: +1
      zone_contamination_living: +1
    unlocks: ["C03_AMIGO_FOLLOWUP_01"]
    locks: []
    next_node: "C03_AMIGO_FOLLOWUP_01"
  - option_id: "C03_AMIGO_MAIN_01_B"
    label: "Responder seco, sin humor"
    tone: "evasiva"
    effects:
      avoidance: 0
      confrontation: 0
      social_debt: +1
      guilt_noise: 0
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_kitchen: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C03_AMIGO_MAIN_01_C"
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
    unlocks: ["C03_AMIGO_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C03_AMIGO_MAIN_01_D"
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
      zone_contamination_kitchen: 0
      zone_contamination_living: 0
    unlocks: ["C03_AMIGO_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "compañía blandita o cháchara que recomienda distraerse"
  night:
    - "si el jugador se refugia aquí, el retorno corporal puede volverse más doliente y menos frontal"
  exterior:
    - "vida ajena a distancia que suena ligera y por eso raspa"
notes: "El amigo tiene que seguir respirando verdad humana, no convertirse en alivio cómico de diseño."
```

---

## 5. Árbol 04 — Pareja / Ex / entrada que pilla al cuerpo sin espacio

### 5.1. Intención
La pareja/ex aquí ya puede entrar con más verdad, pero todavía sin tomar el trono del ciclo. La gracia está en que aparezca cuando el protagonista ya no tiene aire para gestionar nada más.

### 5.2. Nodo principal

```yaml
node_id: "C03_EX_MAIN_01"
character: "Pareja/Ex"
phase: "day"
context: "Tarde media o momento de quietud mala en dormitorio o cerca del balcón."
text: "No sé si hago bien en escribirte hoy. Me he acordado de una cosa tonta y se me ha quedado el cuerpo raro."
subtext: "vuelvo / sigo aquí / te abro intimidad justo cuando no te cabe"
location_bias: "bedroom -> balcony"
related_zone: "bedroom"
recurrence_type: "main"
player_options:
  - option_id: "C03_EX_MAIN_01_A"
    label: "Responder con verdad corta"
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
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: ["C03_EX_FOLLOWUP_01"]
    locks: []
    next_node: "C03_EX_FOLLOWUP_01"
  - option_id: "C03_EX_MAIN_01_B"
    label: "Responder con distancia amable"
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
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C03_EX_MAIN_01_C"
    label: "Abrirlo y dejarlo suspendido"
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
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: ["C03_EX_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
  - option_id: "C03_EX_MAIN_01_D"
    label: "No abrir"
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
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: 0
    unlocks: ["C03_EX_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "frase sentimental tibia, casi obscena por momento"
  night:
    - "pausa afectiva dentro de respiración o pecho"
    - "dormitorio menos neutro, más vivido por ausencia"
  exterior:
    - "balcón con carga íntima incluso sin salir"
notes: "La pareja/ex aquí no secuestra el ciclo: perfora su superficie."
```

### 5.3. Follow-up mínimo

```yaml
node_id: "C03_EX_FOLLOWUP_01"
character: "Pareja/Ex"
phase: "day"
context: "El jugador ha abierto una verdad pequeña."
text: "A mí también. Pensaba que se me había pasado y mira."
subtext: "lo nuestro no está muerto del todo / o no del modo limpio"
location_bias: "bedroom"
related_zone: "bedroom"
recurrence_type: "followup"
player_options:
  - option_id: "C03_EX_FOLLOWUP_01_A"
    label: "Seguir un poco"
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
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C03_EX_FOLLOWUP_01_B"
    label: "Cortar suave"
    tone: "evasive"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bedroom: +1
    unlocks: ["C03_EX_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 6. Árbol 05 — TV / suggestion clínica y tranquila

### 6.1. Intención
La TV en C03 debe dejar de sonar sólo a comodidad. Ahora acompaña, pero recomendando descanso, gestión blanda del cuerpo y aplazamiento con buena conciencia. Es veneno en vaso de agua.

### 6.2. Pool de eco contaminado

```yaml
node_id: "C03_TV_ECHO_POOL_01"
character: "TV"
phase: "day_to_night_transition"
context: "Salón activo o residual; jugador cansado; cuerpo presente como problema"
text_pool:
  - "hay días en los que lo mejor es no forzarse"
  - "cuidarse también es saber parar"
  - "el cuerpo avisa antes de romperse"
  - "a veces lo sensato es tumbarse y dejar pasar"
subtext: "descansa / córtate / no mires demasiado / delega en la pausa"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "contaminated_echo"
player_options:
  - option_id: "C03_TV_ECHO_POOL_01_A"
    label: "Dejar la TV puesta"
    tone: "silence"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: 0
      loneliness_index: -1
      tv_influence: +2
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C03_TV_ECHO_POOL_01_B"
    label: "Apagarla"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: -1
      editor_pressure: 0
      stability: -1
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: 0
    unlocks: []
    locks: []
    next_node: "END"
notes: "La TV no cura ni empeora de forma lineal; sesga la interpretación de lo corporal."
```

---

## 7. Árbol 06 — Puerta / retorno nocturno corporal

### 7.1. Intención
La puerta en C03 debe devolver organicidad íntima. No frase todavía, no gran despliegue: respiración, humedad, pecho, pausa demasiado viva.

### 7.2. Nodo nocturno

```yaml
node_id: "C03_PUERTA_RETURN_01"
character: "Puerta/Criatura"
phase: "night"
context: "Noche avanzada. El jugador se acerca al pasillo o decide escuchar."
text: "No hay lenguaje limpio. Hay un ritmo húmedo, una exhalación rara o una presencia blanda detrás de la madera, como si al otro lado alguien ensayara descansar mal."
subtext: "el piso ha aprendido tu cuerpo / la deuda ya respira"
location_bias: "hall -> sealed_door"
related_zone: "hall"
recurrence_type: "night_echo"
player_options:
  - option_id: "C03_PUERTA_RETURN_01_A"
    label: "Acercarse y escuchar más"
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
      threat_intimacy: +2
      creature_growth: +1
      door_pressure: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C03_PUERTA_RETURN_01_B"
    label: "Quedarse quieto sin acercarse más"
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
      creature_growth: +1
      door_pressure: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C03_PUERTA_RETURN_01_C"
    label: "Tocar el marco"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: +2
      loneliness_index: +1
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
  - option_id: "C03_PUERTA_RETURN_01_D"
    label: "Irse a la cama o medicarse"
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
notes: "La textura exacta depende del foco dominante: baño -> humedad/mucosa/aire; dormitorio -> pecho/latido/pausa; editor latente -> respiración trabajosa; pareja/ex activa -> pausa íntima rara."
```

---

## 8. Mapa rápido de IDs y funciones

| ID | Fuente | Tipo | Zona | Función principal |
|---|---|---|---|---|
| C03_MADRE_MAIN_01 | Madre | Main | Baño/Dormitorio | Volver el cuerpo el centro del día |
| C03_MADRE_INSIST_01 | Madre | Insistence | Dormitorio | Mantener culpa corporal y obediencia blanda |
| C03_EDITOR_MAIN_01 | Editor | Main | Salón/Pasillo | Mantener deuda laboral como vergüenza de fondo |
| C03_AMIGO_MAIN_01 | Amigo | Main | Cocina/Salón | Ofrecer alivio banal en mal momento |
| C03_EX_MAIN_01 | Pareja/Ex | Main | Dormitorio/Balcón | Abrir intimidad dentro de la fatiga |
| C03_TV_ECHO_POOL_01 | TV | Contaminated Echo | Salón | Sesgar el cuerpo hacia pausa, corte o anestesia |
| C03_PUERTA_RETURN_01 | Puerta/Criatura | Night Echo | Pasillo | Devolver respiración, pecho o humedad orgánica |

---

## 9. Validaciones para pasar a siguientes ciclos

Antes de abrir el Ciclo 4, este documento debe dejar claras estas cuatro cosas:

1. La **madre** ya puede dominar un ciclo sin convertirse en personaje episódico ni sermón.
2. El **cuerpo** ya funciona como fuente primaria de contaminación y retorno.
3. La **pareja/ex** ya está lo bastante metida en el tejido diario como para poder tomar presión activa más adelante.
4. La **puerta** ya no sólo articula función; ya parece albergar un cuerpo desgraciado.

Si una de estas cuatro patas falla, el Ciclo 4 entrará decorativo, blandito y sin la mala leche íntima que necesita.

---

## 10. Veredicto de cierre

Este anexo queda aprobado como **tercera capa authored de árboles de diálogo del proyecto**. No agota el Ciclo 3, pero deja fijados:

- el cuerpo como archivo dramático,
- la madre como presión activa legítima,
- el editor como deuda interiorizada,
- el amigo como falsa normalidad todavía viva,
- la pareja/ex como aguja íntima ya incrustada,
- la TV en suggestion clínica,
- y la puerta como aparato de respiración y pecho, no sólo de ruido.
