# PANDAMIEN — ANEXO C
## Árboles de diálogo y ecos — Ciclo 6: Colonización semántica
### Derivado del GDD Maestro v03, Anexo M v01, Anexo A v01, Anexo I v01, Anexo D C06 y Anexo E C06

---

## 0. Propósito del documento

Este documento abre el trabajo authored del **Ciclo 6 — Colonización semántica**.

Su función no es inflar el guion con escenas “raras”, sino volver operativa la deriva ya fijada por el corpus:

- la **TV** pasa a presión activa del ciclo,
- los vínculos dejan de sentirse como líneas paralelas y empiezan a mezclarse,
- el **editor** añade medición y vergüenza al magma general,
- la **madre** aporta gramática corporal y clínica blanda,
- el **amigo** aporta banalidad, charla y ruido acompañante,
- la **pareja/ex** sigue clavando una astilla afectiva dentro de la mezcla,
- y la **puerta** ya no sólo devuelve función, mirada o pecho: empieza a devolver **sintaxis defectuosa**.

La regla maestra aquí sigue siendo la misma:

**cada nodo importante debe tensionar, como mínimo, dos de estas capas — vínculo, apartamento, criatura/puerta — y, cuando pueda, las tres.**

---

## 1. Criterios de escritura del Ciclo 6

### 1.1. Tono
El tono de C06 no es de locura explosiva. Es de contaminación interpretativa. Todo sigue siendo reconocible, pero ya no atribuible con seguridad.

### 1.2. Función del ciclo
- convertir la TV en pseudo-centro de relato y manipulación,
- mantener a todos los vínculos vivos como material mezclable,
- consolidar salón y pasillo como eje de sintaxis contaminada,
- preparar una noche donde la puerta ya intente responder,
- y demostrar que el apartamento ha empezado a pensar con restos de voces humanas.

### 1.3. Regla de presión
La TV manda, pero no porque “hable más alto”, sino porque organiza mejor. El resto de voces siguen entrando, pero ya pueden parecer subtítulos de algo que el piso está montando.

### 1.4. Regla de eco
Todos los nodos relevantes del ciclo 6 deben sembrar al menos uno de estos retornos:
- eco de TV en modo manipulation,
- eco nocturno de frase rota, llamada fallida o tono mezclado,
- eco de zona en salón o pasillo,
- eco de puerta como voz mal cosida.

---

## 2. Árbol 01 — TV / línea demasiado oportuna

### 2.1. Intención
La TV toma aquí la presión activa del ciclo. No debe sonar mágica ni omnisciente. Debe sonar como un aparato que ha aprendido demasiado del clima del piso y editorializa con una puntería obscena.

### 2.2. Nodo principal

```yaml
node_id: "C06_TV_MAIN_01"
character: "TV"
phase: "day"
context: "Mañana media o primer tramo largo en salón. El jugador lleva ya varios ciclos usando la TV como compañía, fondo o narcótico."
text: "Hay veces en que no hace falta decir mucho. Basta con no dejar a nadie esperando al otro lado."
subtext: "te acompaño / te leo / te reorganizo las culpas / ya no eres tú quien interpreta primero"
location_bias: "living_room -> hallway"
related_zone: "living"
recurrence_type: "main"
player_options:
  - option_id: "C06_TV_MAIN_01_A"
    label: "Quedarse escuchando y dejar que siga"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: +1
      guilt_noise: +1
      loneliness_index: -1
      tv_influence: +2
      editor_pressure: +1
      stability: -1
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_living: +2
      zone_contamination_hall: +1
    unlocks: ["C06_TV_FOLLOWUP_01"]
    locks: []
    next_node: "C06_TV_FOLLOWUP_01"
  - option_id: "C06_TV_MAIN_01_B"
    label: "Bajar volumen sin apagar"
    tone: "evasiva"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: +1
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: +1
      zone_contamination_living: +2
      zone_contamination_hall: +1
    unlocks: ["C06_TV_RESIDUAL_ECHO_01"]
    locks: []
    next_node: "END"
  - option_id: "C06_TV_MAIN_01_C"
    label: "Apagarla de golpe"
    tone: "delay"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: 0
      guilt_noise: 0
      loneliness_index: +1
      tv_influence: -1
      editor_pressure: 0
      stability: -1
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: +1
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: ["C06_TV_ABRUPT_SILENCE_01"]
    locks: []
    next_node: "END"
  - option_id: "C06_TV_MAIN_01_D"
    label: "Seguir mirando el móvil con la tele de fondo"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
      loneliness_index: 0
      tv_influence: +2
      editor_pressure: +1
      stability: -1
      threat_intimacy: 0
      creature_growth: +2
      door_pressure: +1
      zone_contamination_living: +3
      zone_contamination_hall: +1
    unlocks: ["C06_TV_RESIDUAL_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "la siguiente línea ya no parece comentario, sino continuación"
  night:
    - "frase rota, llamada fallida, tono robado a varios vínculos"
  exterior:
    - "afuera se vuelve menos informativo y más escenográfico"
notes: "La TV no sabe la verdad; sabe reorganizar los residuos del jugador mejor que él."
```

### 2.3. Follow-up mínimo

```yaml
node_id: "C06_TV_FOLLOWUP_01"
character: "TV"
phase: "day"
context: "El jugador se ha quedado escuchando y ha concedido protagonismo a la emisión."
text: "Lo peor no es el silencio. Lo peor es cuando cada uno cree estar oyendo otra cosa."
subtext: "ya te estoy enseñando cómo va a hablar la casa esta noche"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "followup"
player_options:
  - option_id: "C06_TV_FOLLOWUP_01_A"
    label: "Seguir escuchando"
    tone: "direct"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: -1
      tv_influence: +1
      editor_pressure: 0
      stability: -1
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: +1
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C06_TV_FOLLOWUP_01_B"
    label: "Apagar"
    tone: "evasive"
    effects:
      avoidance: 0
      confrontation: +1
      social_debt: 0
      guilt_noise: 0
      loneliness_index: +1
      tv_influence: -1
      editor_pressure: 0
      stability: -1
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: +1
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: ["C06_TV_ABRUPT_SILENCE_01"]
    locks: []
    next_node: "END"
```

---

## 3. Árbol 02 — Editor / precisión cortante dentro del magma

### 3.1. Intención
El editor aquí no domina. Pincha. Su función es aportar medición, utilidad y vergüenza a una mezcla que, sin él, podría volverse demasiado atmosférica y poco cruel.

### 3.2. Nodo principal

```yaml
node_id: "C06_EDITOR_MAIN_01"
character: "Editor"
phase: "day"
context: "Media mañana o primer hueco después de haber dejado a la TV ocupar demasiado espacio."
text: "Necesito una respuesta clara hoy. Aunque sea para decirme que no llegas."
subtext: "ordena esto / deja de flotar / tu indefinición ya cuesta"
location_bias: "living_room -> hall"
related_zone: "living"
recurrence_type: "main"
player_options:
  - option_id: "C06_EDITOR_MAIN_01_A"
    label: "No llego. Luego te explico."
    tone: "direct"
    effects:
      avoidance: -1
      confrontation: +1
      social_debt: 0
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: +1
      stability: 0
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: ["C06_EDITOR_FOLLOWUP_01"]
    locks: []
    next_node: "C06_EDITOR_FOLLOWUP_01"
  - option_id: "C06_EDITOR_MAIN_01_B"
    label: "Sí, sí, te digo en un rato"
    tone: "evasive"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
      loneliness_index: 0
      tv_influence: +1
      editor_pressure: +1
      stability: -1
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: +1
      zone_contamination_living: +2
      zone_contamination_hall: +1
    unlocks: ["C06_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C06_EDITOR_MAIN_01_C"
    label: "Abrir y dejarlo en visto"
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
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: +1
      zone_contamination_living: +2
      zone_contamination_hall: +1
    unlocks: ["C06_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C06_EDITOR_MAIN_01_D"
    label: "Ignorar y seguir con la TV o con otra voz"
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
      creature_growth: +2
      door_pressure: +1
      zone_contamination_living: +3
      zone_contamination_hall: +1
    unlocks: ["C06_EDITOR_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "organizarse, contestar, definirse"
  night:
    - "corte verbal, urgencia rítmica, evaluación torcida"
  exterior:
    - "medición del tiempo ajeno, ventanas encendidas a destiempo"
notes: "La violencia aquí es sintáctica y administrativa. Muy poco volumen, mucha diana."
```

### 3.3. Follow-up mínimo

```yaml
node_id: "C06_EDITOR_FOLLOWUP_01"
character: "Editor"
phase: "day"
context: "El jugador ha dicho una verdad corta."
text: "Vale. Pero dímelo tú, no me obligues a adivinarlo."
subtext: "la falta de respuesta ya es una forma de trabajo que me desplazas"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "followup"
player_options:
  - option_id: "C06_EDITOR_FOLLOWUP_01_A"
    label: "Entendido."
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
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C06_EDITOR_FOLLOWUP_01_B"
    label: "Sí."
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
      door_pressure: 0
      zone_contamination_living: +1
    unlocks: ["C06_EDITOR_INSIST_01"]
    locks: []
    next_node: "END"
```

---

## 4. Árbol 03 — Madre / cuidado fácilmente parasitable

### 4.1. Intención
La madre sigue entrando, pero ahora una frase suya puede sonar ya como semilla perfecta para que la TV o la puerta la mastiquen luego.

### 4.2. Nodo principal

```yaml
node_id: "C06_MADRE_MAIN_01"
character: "Madre"
phase: "day"
context: "Después de una secuencia de ruido o justo cuando el jugador intenta recomponerse."
text: "Aunque no tengas ganas, come algo y descansa un poco. Se te nota cuando vas arrastrándote."
subtext: "te cuido / te ordeno / tu cuerpo me sigue hablando aunque tú no quieras"
location_bias: "bathroom -> bedroom"
related_zone: "bathroom"
recurrence_type: "main"
player_options:
  - option_id: "C06_MADRE_MAIN_01_A"
    label: "Vale, luego corto un poco"
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
      threat_intimacy: +1
      creature_growth: 0
      door_pressure: 0
      zone_contamination_bathroom: +1
      zone_contamination_bedroom: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C06_MADRE_MAIN_01_B"
    label: "Ahora no puedo"
    tone: "evasive"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: 0
      tv_influence: +1
      editor_pressure: +1
      stability: 0
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bathroom: +1
      zone_contamination_bedroom: +1
    unlocks: ["C06_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C06_MADRE_MAIN_01_C"
    label: "Escuchar y no responder"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +2
      loneliness_index: 0
      tv_influence: +1
      editor_pressure: 0
      stability: -1
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bathroom: +1
      zone_contamination_bedroom: +1
    unlocks: ["C06_MADRE_INSIST_01"]
    locks: []
    next_node: "END"
  - option_id: "C06_MADRE_MAIN_01_D"
    label: "Silenciar"
    tone: "silence"
    effects:
      avoidance: +2
      confrontation: 0
      social_debt: +2
      guilt_noise: +2
      loneliness_index: +1
      tv_influence: +1
      editor_pressure: 0
      stability: -1
      threat_intimacy: +1
      creature_growth: +1
      door_pressure: 0
      zone_contamination_bathroom: +1
      zone_contamination_bedroom: +1
    unlocks: ["C06_MADRE_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "autocuidado, descanso, orden, cuidado blando"
  night:
    - "frase clínica rota, respiración que parece consejo"
  exterior:
    - "doméstico sin alivio"
notes: "La madre aquí aporta gramática corporal a la mezcla; no lleva el volante, pero deja palabras pegajosas."
```

---

## 5. Árbol 04 — Amigo / banalidad que ya puede sonar deforme

### 5.1. Intención
El amigo debe seguir siendo amigo. Pero su ruido ya no cae limpio: puede volverse casi grotesco por contexto o acabar dándole material de parloteo a la criatura.

### 5.2. Nodo principal

```yaml
node_id: "C06_AMIGO_MAIN_01"
character: "Amigo"
phase: "day"
context: "Tarde media, cuando el jugador está saturado de voces más serias o más pesadas."
text: "Te juro que ya hablo solo hasta cuando cierro el grifo. Esto acaba y me diagnostican nevera."
subtext: "vente aquí / ríete un segundo / no mires demasiado lo demás"
location_bias: "kitchen -> living_room"
related_zone: "kitchen"
recurrence_type: "main"
player_options:
  - option_id: "C06_AMIGO_MAIN_01_A"
    label: "Seguirle la broma"
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
      threat_intimacy: 0
      creature_growth: 0
      door_pressure: 0
      zone_contamination_kitchen: +1
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C06_AMIGO_MAIN_01_B"
    label: "Responder corto, sin entrar"
    tone: "evasive"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: 0
      loneliness_index: 0
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_kitchen: +1
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C06_AMIGO_MAIN_01_C"
    label: "Dejarlo en leído"
    tone: "delay"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +1
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: 0
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_kitchen: +1
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C06_AMIGO_MAIN_01_D"
    label: "Ignorarlo y seguir absorbiendo ruido"
    tone: "silence"
    effects:
      avoidance: +1
      confrontation: 0
      social_debt: +2
      guilt_noise: +1
      loneliness_index: +1
      tv_influence: +1
      editor_pressure: 0
      stability: 0
      threat_intimacy: 0
      creature_growth: +1
      door_pressure: 0
      zone_contamination_kitchen: +1
      zone_contamination_living: +1
    unlocks: ["C06_AMIGO_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "entretenimiento, cháchara, humor sin centro"
  night:
    - "parloteo hueco, banalidad podrida, masticación verbal"
  exterior:
    - "vida ajena que parece seguir hablando sin ti"
notes: "El amigo aquí puede aliviar mucho o dejar un ruido tristísimo. Las dos cosas sirven."
```

---

## 6. Árbol 05 — Pareja / Ex / astilla íntima dentro del magma

### 6.1. Intención
La pareja/ex ya no lleva el volante del ciclo, pero una sola frase suya puede torcer la mezcla entera y convertirla en algo mucho más personal.

### 6.2. Nodo principal

```yaml
node_id: "C06_EX_MAIN_01"
character: "Pareja/Ex"
phase: "day"
context: "Momento de quietud mala o relectura accidental de algo pendiente."
text: "No sé qué me ha dado por escribirte justo ahora. Supongo que hay días que se queda todo demasiado cerca."
subtext: "vuelvo poco / vuelvo justo / sigo teniendo llave en el aire del cuarto"
location_bias: "bedroom -> balcony"
related_zone: "bedroom"
recurrence_type: "main"
player_options:
  - option_id: "C06_EX_MAIN_01_A"
    label: "Abrir la herida un poco"
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
      zone_contamination_balcony: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C06_EX_MAIN_01_B"
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
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C06_EX_MAIN_01_C"
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
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C06_EX_MAIN_01_D"
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
      zone_contamination_bedroom: +1
      zone_contamination_balcony: +1
    unlocks: ["C06_EX_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
echoes:
  tv:
    - "romanticismo barato, reparación imposible"
  night:
    - "una pausa afectiva puede torcer toda la mezcla verbal"
  exterior:
    - "balcón, luz íntima, aire que no despeja"
notes: "Aquí la pareja/ex no hace gran escena. Hace daño de precisión."
```

---

## 7. Nodos de eco y ausencia recomendados

```yaml
node_id: "C06_TV_ABRUPT_SILENCE_01"
character: "TV"
phase: "transition"
context: "La TV se apaga de golpe."
text: "El silencio que deja no limpia nada; sólo adelanta la puerta."
subtext: "has cortado una boca, no el hambre de hablar"
location_bias: "living_room -> hallway"
related_zone: "hall"
recurrence_type: "echo"
player_options:
  - option_id: "C06_TV_ABRUPT_SILENCE_01_A"
    label: "Quedarse quieto"
    tone: "direct"
    effects:
      confrontation: +1
      threat_intimacy: +1
      stability: -1
      door_pressure: +1
      zone_contamination_hall: +1
    unlocks: []
    locks: []
    next_node: "END"
```

```yaml
node_id: "C06_EDITOR_INSIST_01"
character: "Editor"
phase: "day"
context: "Tras evasión o visto."
text: "Aunque sea un no, necesito una frase."
subtext: "tu silencio ya me obliga a hablar por ti"
location_bias: "living_room"
related_zone: "living"
recurrence_type: "insistence"
player_options:
  - option_id: "C06_EDITOR_INSIST_01_A"
    label: "Mandar un 'no llego'"
    tone: "direct"
    effects:
      confrontation: +1
      editor_pressure: 0
      guilt_noise: +1
      zone_contamination_living: +1
    unlocks: []
    locks: []
    next_node: "END"
  - option_id: "C06_EDITOR_INSIST_01_B"
    label: "No responder"
    tone: "silence"
    effects:
      avoidance: +2
      editor_pressure: +2
      guilt_noise: +2
      creature_growth: +1
      door_pressure: +1
      zone_contamination_living: +1
      zone_contamination_hall: +1
    unlocks: ["C06_EDITOR_ABSENCE_ECHO_01"]
    locks: []
    next_node: "END"
```

---

## 8. Validación del ciclo

### 8.1. Validación narrativa
C06 queda aprobado si el jugador siente que varias voces siguen siendo reconocibles pero ninguna vuelve limpia.

### 8.2. Validación sistémica
C06 queda aprobado si:
- salón y pasillo ganan centralidad semántica,
- la TV sube de suggestion a manipulation,
- la criatura gana imitación y fraseo defectuoso,
- y la noche puede devolver palabras rotas sin convertirse aún en conversación plena.

### 8.3. Validación experiencial
El jugador debe salir del ciclo pensando algo muy concreto:
**la casa ya no sólo sabe devolverme cosas; empieza a responderme usando restos de todos.**

---

## 9. Veredicto de cierre

Este anexo queda aprobado como **sexto árbol authored** del proyecto. Demuestra que PANDAMIEN puede acercarse a la palabra sin matar el misterio: la criatura todavía no conversa; **improvisa una respuesta con pedazos de vida humana mal digerida**.
