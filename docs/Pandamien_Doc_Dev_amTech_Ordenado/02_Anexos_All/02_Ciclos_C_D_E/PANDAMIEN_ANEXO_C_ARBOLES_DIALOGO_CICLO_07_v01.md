
# PANDAMIEN — ANEXO C
## Árboles de diálogo y ecos — Ciclo 7: Doble vínculo imposible
### Derivado del GDD Maestro v04, Anexo M v01, Anexo A v01, Anexo I v01, Anexo D C07 y Anexo E C07

---

## 0. Propósito del documento

Este documento abre el trabajo authored del **Ciclo 7 — Doble vínculo imposible**.

Su función no es apilar más estímulos ni convertir el proyecto en un festival de desgracias mecánicas. Su función es volver operativa la lógica ya fijada por el canon:

- **todos los vínculos** siguen vivos,
- la **presión activa** es una **colisión de sistemas incompatibles**,
- para esta versión principal se fija la combinación **Madre + Editor**,
- la **TV** entra en modo **confrontational**,
- la **puerta** ya casi organiza el piso,
- y el resultado del ciclo no es sólo crecimiento: es **fijación del temperamento dominante de la criatura**.

La regla maestra aquí sigue siendo la misma, pero más cabrona que nunca:

**cada nodo importante debe mover vínculo, apartamento y criatura/puerta al menos en dos de esas tres capas, y en este ciclo lo ideal es que toque las tres.**

---

## 1. Criterios de escritura del Ciclo 7

### 1.1. Tono
El tono de C07 no es histérico. Es cruel. La crueldad nace de que ambas presiones tienen legitimidad humana y no admiten conciliación limpia.

### 1.2. Función del ciclo
- obligar a sacrificar algo inequívoco,
- dejar una zona claramente perdida o seriamente empeorada,
- fijar el sesgo dominante del monstruo,
- preparar la resolución con una criatura que ya no sea sólo archivo, sino trato.

### 1.3. Regla de presión
La combinación principal de este authored es **Madre + Editor**, pero deben seguir respirando:
- **Amigo** como salida falsa o alivio tardío,
- **Pareja/Ex** como eco íntimo que hace más obscena la pérdida,
- **TV** como aparato confrontational que cose las dos exigencias,
- **Puerta** como retorno casi organizado.

### 1.4. Regla de eco
Todos los nodos relevantes del ciclo 7 deben sembrar al menos uno de estos retornos:
- eco de TV confrontational,
- eco de puerta como conducta, no sólo sonido,
- eco de zona sacrificada,
- eco nocturno de temperamento dominante.

---

## 2. Árbol 01 — Madre / urgencia corporal real

### 2.1. Intención
La madre toma aquí una urgencia distinta: ya no sólo cuida o controla; detecta una caída real. Su presencia debe sonar a amor cansado, costumbre de sostén y derecho viejo sobre el cuerpo del protagonista.

### 2.2. Nodo principal

```yaml
node_id: "C07_MADRE_MAIN_01"
character: "Madre"
phase: "day"
context: "Mañana media. El jugador ya está gastado antes de empezar y el cuerpo no entra hoy como sugerencia."
text: "No me digas que estás bien porque no te creo. Tienes una voz horrible. ¿Has comido algo? ¿Te has tomado lo que te tocaba?"
subtext: "te cuido / te conozco / ya no puedo leer esto como simple cansancio"
location_bias: "bathroom -> bedroom"
related_zone: "bathroom"
recurrence_type: "main"
player_options:
  - option_id: "C07_MADRE_MAIN_01_A"
    label: "Decir la verdad corta: 'Estoy hecho polvo. Ahora hago algo.'"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: -1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: +1
      stability: -1
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: 0
      creature_temperament: "doliente_seed"
      zone_contamination_bathroom: +1
      zone_contamination_bedroom: +1
    unlocks: ["C07_MADRE_FOLLOWUP_01", "C07_EDITOR_COLLISION_01"]
    locks: []
    next_node: "C07_EDITOR_COLLISION_01"
  - option_id: "C07_MADRE_MAIN_01_B"
    label: "Mentir: 'Estoy bien, voy liado nada más.'"
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
      creature_temperament: "rencor_seed"
      zone_contamination_bathroom: +2
      zone_contamination_bedroom: +1
    unlocks: ["C07_MADRE_INSIST_01", "C07_EDITOR_COLLISION_01"]
    locks: []
    next_node: "C07_EDITOR_COLLISION_01"
  - option_id: "C07_MADRE_MAIN_01_C"
    label: "Cortar: 'Luego te llamo.'"
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
      creature_temperament: "imitative_seed"
      zone_contamination_bathroom: +1
      zone_contamination_bedroom: +1
    unlocks: ["C07_MADRE_INSIST_01", "C07_EDITOR_COLLISION_01"]
    locks: []
    next_node: "C07_EDITOR_COLLISION_01"
  - option_id: "C07_MADRE_MAIN_01_D"
    label: "Silenciar o no coger"
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
      creature_temperament: "furious_seed"
      zone_contamination_bathroom: +2
      zone_contamination_bedroom: +1
    unlocks: ["C07_MADRE_ABSENCE_ECHO_01", "C07_EDITOR_COLLISION_01"]
    locks: []
    next_node: "C07_EDITOR_COLLISION_01"
echoes:
  tv:
    - "frases sobre no dejarse"
    - "cuidado dicho como reproche"
  night:
    - "si el cuerpo queda sacrificado: rencor contra la carne abandonada"
    - "si se acepta el cuidado: criatura más doliente o suplicante"
  exterior:
    - "silencio doméstico que parece juzgar"
notes: "La madre no debe sonar como melodrama. Debe sonar como una verdad incómoda que llega cuando ya no hay margen."
```

### 2.3. Follow-up e insistencia

```yaml
node_id: "C07_MADRE_FOLLOWUP_01"
character: "Madre"
phase: "day"
context: "El jugador ha admitido algo de caída."
text: "Entonces deja lo que estés haciendo cinco minutos y arréglate mínimamente. No puedes seguir así."
subtext: "te doy una orden porque ya no sé ayudarte de forma neutra"
location_bias: "bathroom"
related_zone: "bathroom"
recurrence_type: "followup"
player_options:
  - option_id: "C07_MADRE_FOLLOWUP_01_A"
    label: "Vale, lo hago."
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: -1
      guilt_noise: 0
      stability: +0
      editor_pressure: +1
      creature_temperament: "doliente_seed"
      zone_contamination_bathroom: -1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_MADRE_FOLLOWUP_01_B"
    label: "Ahora no puedo."
    tone: "evasiva"
    effects:
      avoidance: +1
      social_debt: +1
      guilt_noise: +1
      editor_pressure: +1
      creature_growth: +1
      creature_temperament: "rencor_seed"
      zone_contamination_bathroom: +1
    unlocks: ["C07_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
```

```yaml
node_id: "C07_MADRE_INSIST_01"
character: "Madre"
phase: "day"
context: "Si se ha aplazado, mentido o ignorado."
text: "Haz lo que quieras, pero no me vuelvas a decir esta noche que estabas fatal y no has hecho ni lo mínimo."
subtext: "amor agotado / reproche preventivo / ya te estoy oyendo caer"
location_bias: "bedroom"
related_zone: "bedroom"
recurrence_type: "insistence"
player_options:
  - option_id: "C07_MADRE_INSIST_01_A"
    label: "Mandar un 'sí, ya'"
    tone: "delay"
    effects:
      avoidance: +1
      guilt_noise: +1
      creature_temperament: "imitative_seed"
      zone_contamination_bedroom: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_MADRE_INSIST_01_B"
    label: "No responder"
    tone: "silence"
    effects:
      avoidance: +2
      social_debt: +2
      guilt_noise: +2
      stability: -1
      creature_growth: +1
      creature_temperament: "furious_seed"
      zone_contamination_bedroom: +1
      zone_contamination_bathroom: +1
    unlocks: ["C07_MADRE_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 3. Árbol 02 — Editor / colisión no prorrogable

### 3.1. Intención
El editor aquí no “reaparece”: cae como una guillotina normal, razonable y tardía. Su trabajo no es sonar monstruoso, sino hacer incompatible la urgencia corporal con la exigencia útil.

### 3.2. Nodo principal

```yaml
node_id: "C07_EDITOR_COLLISION_01"
character: "Editor"
phase: "day"
context: "En el mismo tramo del día en que la madre o el cuerpo ya han reclamado prioridad."
text: "Necesito que me digas esto ya. Si no lo saco hoy, me revientas la planificación. No me sirve otra respuesta en el aire."
subtext: "tu cuerpo no cancela el mundo / decide algo y págalo"
location_bias: "living_room -> hall"
related_zone: "living"
recurrence_type: "main"
player_options:
  - option_id: "C07_EDITOR_COLLISION_01_A"
    label: "Responder claro: 'Hoy no llego. Te lo digo ya.'"
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: +1
      guilt_noise: +1
      tv_influence: +1
      editor_pressure: +2
      stability: -1
      creature_growth: +0
      door_pressure: +1
      creature_temperament: "doliente_seed"
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: ["C07_EDITOR_FOLLOWUP_01"]
    locks: []
    next_node: "C07_EDITOR_FOLLOWUP_01"
  - option_id: "C07_EDITOR_COLLISION_01_B"
    label: "Prometer que llegas aunque no sea verdad"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
      tv_influence: +1
      editor_pressure: +2
      stability: -1
      creature_growth: +1
      door_pressure: +1
      creature_temperament: "rencor_seed"
      zone_contamination_living: +2
      zone_contamination_hall: +1
    unlocks: ["C07_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C07_EDITOR_COLLISION_01_C"
    label: "Abrir y dejar flotando"
    tone: "delay"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
      tv_influence: +1
      editor_pressure: +2
      stability: -1
      creature_growth: +1
      door_pressure: +1
      creature_temperament: "imitative_seed"
      zone_contamination_living: +2
      zone_contamination_hall: +1
    unlocks: ["C07_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C07_EDITOR_COLLISION_01_D"
    label: "No responder"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: +2
      guilt_noise: +2
      tv_influence: +1
      editor_pressure: +3
      stability: -1
      creature_growth: +1
      door_pressure: +2
      creature_temperament: "furious_seed"
      zone_contamination_living: +2
      zone_contamination_hall: +1
    unlocks: ["C07_EDITOR_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "responsabilidad"
    - "pagar el retraso"
    - "no dejar colgado a nadie"
  night:
    - "si se miente: criatura más rencorosa"
    - "si se corta limpio: criatura más triste o evaluativa"
    - "si se deja en visto: golpe medido o espera hostil"
  exterior:
    - "horario del mundo útil como acusación muda"
notes: "Aquí nace la incompatibilidad central. No hay que gritarla: basta con que quede materialmente imposible."
```

### 3.3. Follow-up e insistencia

```yaml
node_id: "C07_EDITOR_FOLLOWUP_01"
character: "Editor"
phase: "day"
context: "El jugador ha elegido claridad aunque le haga daño."
text: "Vale. Gracias por decírmelo ya. Pero necesito que entiendas el agujero que me dejas."
subtext: "la claridad no perdona / sólo ordena la herida"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "followup"
player_options:
  - option_id: "C07_EDITOR_FOLLOWUP_01_A"
    label: "Asumirlo y cortar"
    tone: "direct"
    effects:
      confrontation: +1
      guilt_noise: +1
      editor_pressure: +1
      creature_temperament: "doliente_seed"
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_EDITOR_FOLLOWUP_01_B"
    label: "Intentar justificarse más"
    tone: "evasive"
    effects:
      avoidance: +1
      guilt_noise: +2
      editor_pressure: +1
      creature_temperament: "imitative_seed"
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
```

```yaml
node_id: "C07_EDITOR_INSIST_01"
character: "Editor"
phase: "day"
context: "Si se ha prometido, aplazado o dejado en el aire."
text: "No me dejes otra vez esperando una respuesta que sabes que tienes que dar."
subtext: "ya te mido por cómo retrasas / no por lo que haces"
location_bias: "living_room -> hall"
related_zone: "hall"
recurrence_type: "insistence"
player_options:
  - option_id: "C07_EDITOR_INSIST_01_A"
    label: "Responder con un 'voy'"
    tone: "delay"
    effects:
      avoidance: +1
      guilt_noise: +1
      editor_pressure: +1
      creature_temperament: "rencor_seed"
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_EDITOR_INSIST_01_B"
    label: "Seguir sin contestar"
    tone: "silence"
    effects:
      avoidance: +2
      social_debt: +2
      guilt_noise: +2
      editor_pressure: +2
      creature_growth: +1
      door_pressure: +1
      creature_temperament: "furious_seed"
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: ["C07_EDITOR_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 4. Árbol 03 — Amigo / falsa tercera salida

### 4.1. Intención
El amigo aquí no salva ni domina. Ofrece esa posibilidad mugrienta de flotar un rato más para no elegir.

### 4.2. Nodo principal

```yaml
node_id: "C07_AMIGO_MAIN_01"
character: "Amigo"
phase: "day"
context: "Mitad del día. El choque principal ya ha ocurrido o está ocurriendo."
text: "¿Estás vivo o qué? Te iba a mandar una tontería pero me ha dado la sensación de que no era momento."
subtext: "quiero entrar sin molestar / entro igual / te ofrezco una rendija de aire raro"
location_bias: "kitchen -> living_room"
related_zone: "kitchen"
recurrence_type: "main"
player_options:
  - option_id: "C07_AMIGO_MAIN_01_A"
    label: "Contestar corto y sincero"
    tone: "direct"
    effects:
      loneliness_index: -1
      confrontation: +1
      creature_temperament: "doliente_seed"
      zone_contamination_kitchen: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_AMIGO_MAIN_01_B"
    label: "Refugiarse un rato en la cháchara"
    tone: "evasive"
    effects:
      avoidance: +1
      tv_influence: +1
      guilt_noise: +1
      creature_growth: +1
      creature_temperament: "imitative_seed"
      zone_contamination_kitchen: +1
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_AMIGO_MAIN_01_C"
    label: "No contestar"
    tone: "silence"
    effects:
      avoidance: +1
      loneliness_index: +1
      social_debt: +1
      creature_temperament: "rencor_seed"
      zone_contamination_kitchen: +1
    unlocks: []
    locks: []
    next_node: "END"
```

---

## 5. Árbol 04 — Pareja/Ex / eco moral de la pérdida

### 5.1. Intención
La pareja/ex aquí no abre la presión principal. Sólo hace que lo sacrificado tenga alguien mirando desde dentro de la casa.

### 5.2. Nodo principal

```yaml
node_id: "C07_EX_MAIN_01"
character: "Pareja/Ex"
phase: "day"
context: "Tarde media o final. El sacrificio principal ya dejó poso."
text: "Lo de hoy te lo estoy leyendo en la cara aunque no te esté viendo. No sé por qué, pero lo noto."
subtext: "te sigo conociendo / lo que eliges deja forma / sigo entrando donde más duele"
location_bias: "bedroom -> balcony"
related_zone: "bedroom"
recurrence_type: "main"
player_options:
  - option_id: "C07_EX_MAIN_01_A"
    label: "Abrirse un poco"
    tone: "direct"
    effects:
      confrontation: +1
      threat_intimacy: +2
      loneliness_index: -1
      creature_temperament: "suplicante_seed"
      zone_contamination_bedroom: +1
      door_pressure: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_EX_MAIN_01_B"
    label: "Responder ambiguo"
    tone: "evasive"
    effects:
      avoidance: +1
      guilt_noise: +1
      threat_intimacy: +1
      creature_temperament: "imitative_seed"
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_EX_MAIN_01_C"
    label: "Dejar en visto"
    tone: "silence"
    effects:
      avoidance: +2
      guilt_noise: +2
      loneliness_index: +1
      threat_intimacy: +2
      creature_temperament: "rencor_seed"
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
      door_pressure: +1
    unlocks: []
    locks: []
    next_node: "END"
echoes:
  night:
    - "si se deja en visto: la puerta puede suplicar o resentirse peor"
  tv:
    - "frase sentimental usada como cuchillo, no como consuelo"
notes: "La pareja/ex aquí mide daño, no roba estructura."
```

---

## 6. Pool contaminado — TV confrontational

```yaml
node_id: "C07_TV_ECHO_POOL_01"
character: "TV"
phase: "day"
context: "Después de la colisión principal o como hilo de fondo que ya no deja anestesiarse."
text_options:
  - "A veces no elegir ya es una forma de decidir contra alguien."
  - "Lo peor no es llegar tarde. Lo peor es llegar cuando ya no sirve."
  - "Cuidarse tarde también cuenta como abandono."
  - "No se puede sostener todo. La pregunta es qué está dispuesto a dejar caer."
subtext: "te editorializo la culpa / te coso las dos presiones / te convierto la casa en veredicto"
location_bias: "living_room -> hallway"
related_zone: "living"
recurrence_type: "contaminated_echo"
player_options:
  - option_id: "C07_TV_ECHO_POOL_01_A"
    label: "Dejarla puesta"
    tone: "direct"
    effects:
      tv_influence: +2
      creature_growth: +1
      door_pressure: +1
      creature_temperament: "imitative_seed"
      zone_contamination_living: +2
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_TV_ECHO_POOL_01_B"
    label: "Bajar volumen"
    tone: "evasive"
    effects:
      avoidance: +1
      tv_influence: +1
      creature_growth: +1
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_TV_ECHO_POOL_01_C"
    label: "Apagarla de golpe"
    tone: "delay"
    effects:
      confrontation: +1
      tv_influence: -1
      stability: -1
      door_pressure: +1
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: ["C07_TV_ABRUPT_SILENCE_01"]
    locks: []
    next_node: "END"
notes: "La TV aquí ya no acompaña; dicta. Si calla, el piso suena peor."
```

---

## 7. Eco nocturno principal — Puerta / temperamento fijándose

```yaml
node_id: "C07_PUERTA_RETURN_01"
character: "Puerta/Criatura"
phase: "night"
context: "Noche del ciclo 7. La decisión del día ya ha sido traducida al pasillo."
text: "No hay frase limpia. Hay conducta: un golpe con intención, una espera, una respiración que ya parece saber si pedir, medir o morder."
subtext: "ya no sólo existo / ya sé cómo tratarte"
location_bias: "hallway -> locked_door"
related_zone: "hall"
recurrence_type: "night_echo"
player_options:
  - option_id: "C07_PUERTA_RETURN_01_A"
    label: "Acercarse y escuchar"
    tone: "direct"
    effects:
      confrontation: +1
      threat_intimacy: +2
      door_pressure: +2
      creature_growth: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_PUERTA_RETURN_01_B"
    label: "Hablarle"
    tone: "direct"
    effects:
      confrontation: +1
      threat_intimacy: +2
      door_pressure: +2
      creature_growth: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C07_PUERTA_RETURN_01_C"
    label: "Retirarse sin acercarse más"
    tone: "silence"
    effects:
      avoidance: +1
      guilt_noise: +1
      door_pressure: +1
      creature_growth: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
notes: "La textura concreta depende del sacrificio dominante: cuerpo -> hostilidad rencorosa; trabajo -> súplica doliente; mentira general -> imitación hambrienta."
```

---

## 8. Mapa rápido de IDs y funciones

| ID | Fuente | Tipo | Zona | Función principal |
|---|---|---|---|---|
| C07_MADRE_MAIN_01 | Madre | Main | Baño/Dormitorio | Abrir urgencia corporal real |
| C07_MADRE_INSIST_01 | Madre | Insistence | Dormitorio | Convertir cuidado en reproche anticipado |
| C07_EDITOR_COLLISION_01 | Editor | Main | Salón/Pasillo | Hacer incompatible cuerpo y rendimiento |
| C07_EDITOR_INSIST_01 | Editor | Insistence | Salón/Pasillo | Medir retraso y endurecer deuda |
| C07_AMIGO_MAIN_01 | Amigo | Main | Cocina/Salón | Ofrecer falsa tercera salida |
| C07_EX_MAIN_01 | Pareja/Ex | Main | Dormitorio/Balcón | Devolver el peso moral del sacrificio |
| C07_TV_ECHO_POOL_01 | TV | Contaminated Echo | Salón/Pasillo | Editorializar la incompatibilidad |
| C07_PUERTA_RETURN_01 | Puerta/Criatura | Night Echo | Pasillo | Fijar el temperamento dominante |

---

## 9. Validaciones para pasar al Ciclo 8

Antes de abrir la resolución, este documento debe dejar claras estas cuatro cosas:

1. El jugador **ha tenido que perder algo de forma inequívoca**.
2. La criatura **ya puede tratar** al jugador según el sacrificio hecho.
3. La **TV** ha completado su función de pseudo-centro interpretativo y puede empezar a retirarse.
4. La puerta ya no devuelve sólo ruido o sintaxis: devuelve **posición moral monstruosa**.

Si una de estas cuatro patas falla, el ciclo final entrará decorativo o demasiado explicativo.

---

## 10. Veredicto de cierre

Este anexo queda aprobado como **séptima capa authored de árboles de diálogo del proyecto**. No agota todas las combinaciones posibles del ciclo 7 dentro del canon, pero sí fija una versión principal, robusta y cruel del **doble vínculo imposible**. Deja cerrados:

- el choque entre cuerpo y rendimiento,
- la zona sacrificada como prueba material,
- la TV en confrontational pleno,
- la pareja/ex y el amigo como ecos morales que no sobran,
- y, sobre todo, la criatura como **temperamento en ciernes**, no ya como simple suma de residuos.
