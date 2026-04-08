# PANDAMIEN — ANEXO D
## Ficha real de día — Ciclo 1: Reconocimiento
### Derivada del GDD Maestro v03 y del Anexo M v01

---

## 0. Intención del día

El primer día no debe parecer “el día del horror”, sino el día en que la vida ya viene torcida pero todavía conserva una apariencia de gestión cotidiana. El jugador entra en una rutina gastada: hay mensajes, una exigencia laboral que parece razonable, la madre ya vive en el borde de lo invasivo sin resultar todavía insoportable, el amigo ocupa espacio como ruido y refugio, y la pareja/ex sólo existe como ausencia sedimentada.

La función dramática del día es muy concreta:

- instalar la rutina,
- presentar la deuda inicial,
- sugerir que el piso ya arrastra desgaste,
- abrir la primera oportunidad de contención precaria,
- y dejar una deuda pequeña pero suficiente para que la noche tenga una primera devolución física detrás de la puerta.

---

## 1. Ficha oficial

```yaml
cycle_id: "C01"
cycle_title: "Reconocimiento"
day_theme: "todavía parece gestionable"
act_phase: "Acto I — Rutina contaminada"

presence_base:
  - character: "Madre"
    format: "llamada corta a media mañana"
    tone: "cuidado con borde de control"
    purpose: "anclar el cuerpo del protagonista al discurso de cuidado/obediencia"
  - character: "Amigo"
    format: "cadena de mensajes banales y un audio breve"
    tone: "ligero, bromista, pandémico, un poco pesado"
    purpose: "normalizar el encierro y ofrecer una vía de evasión aparentemente inocua"

pressure_active:
  primary_system_or_character: "Editor"
  format: "mensaje inicial + llamada breve o intento de llamada"
  urgency: "medium"
  decision_core: "responder con disposición, excusarse, aplazar o ignorar para sostener la sensación de control"

persistent_echoes:
  - source: "Pareja/Ex"
    form: "nombre en historial y foto antigua no abierta del todo"
    effect: "ocupa dormitorio y memoria sin pedir aún escena explícita"
  - source: "TV"
    form: "programación de comfort"
    effect: "acompaña y adormece el conflicto, deja flotando discurso de normalidad"

entry_state:
  player_body_state: "cansancio leve, aseo dudoso, hambre imprecisa, sensación de arrastre pero aún funcional"
  apartment_state_summary: "piso creíble y vivido; hay vaso olvidado en salón, humedad pequeña en baño o cocina y una sensación de aire usado"
  tv_state: "comfort"
  weather_or_exterior_bias: "luz de día plana; el exterior parece real pero distante, aún no amenaza"

relational_beats:
  - beat_id: "C01_D_B01"
    trigger_window: "primer tramo de mañana"
    source: "Madre"
    format: "llamada"
    short_description: "pregunta si ha dormido, si ha tomado algo, si debería arreglarse un poco; mezcla ternura con vigilancia"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "baño y dormitorio quedan teñidos por discurso corporal"
      - "si se evita, sube deuda blanda y se prepara humedad/respiración nocturna"
  - beat_id: "C01_D_B02"
    trigger_window: "después de sentarse en salón o junto al portátil"
    source: "Editor"
    format: "mensaje + posible llamada breve"
    short_description: "instala una entrega o revisión razonable pero cargada de tono evaluativo"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "salón queda ligado a productividad, reloj y deuda"
      - "si se responde evasivo o se ignora, se fortalece la semilla de voz/garganta"
  - beat_id: "C01_D_B03"
    trigger_window: "tramo medio o tarde temprana"
    source: "Amigo"
    format: "cadena de mensajes + audio corto"
    short_description: "manda una tontería, comenta algo del encierro o propone videollamada absurda sin urgencia real"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "salón y cocina ganan calor banal o ruido de fondo"
      - "si el jugador se refugia demasiado aquí, la TV y la pasividad se vuelven más cómodas"
  - beat_id: "C01_D_B04"
    trigger_window: "momento de quietud en dormitorio"
    source: "Pareja/Ex"
    format: "historial no abierto / foto antigua / nombre visible"
    short_description: "no hay contacto directo; sólo la prueba de una intimidad ya instalada en la casa"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "el dormitorio deja de ser neutro"
      - "la herida existe antes de hablar"

contamination:
  primary_focus:
    zone: "Salón"
    material_form: "vaso abandonado, cenicero o taza reseca junto al sofá/mesa; polvo de TV y sensación de aire quieto"
    emotional_cause: "evasión funcional, presión laboral sin asumir y anestesia cotidiana"
    escalation_if_ignored: "la zona se densifica y la criatura gana latencia de voz o masa informe ligada al salón"
  secondary_focus:
    zone: "Baño"
    material_form: "junta con humedad negra incipiente, toalla húmeda demasiado tiempo o espejo salpicado no atendido"
    emotional_cause: "descuido corporal suave, cansancio y control materno interiorizado"
    escalation_if_ignored: "la noche puede devolver humedad, respiración o una textura orgánica mínima"

containment_offer:
  is_available: true
  action: "retirar el vaso/taza y despejar la mesa o rascar una junta pequeña del baño"
  location: "salón o baño, pero sólo una opción significativa"
  time_cost: "consume la ventana cómoda entre la presión del editor y el refugio banal del amigo"
  relational_cost: "puede implicar dejar un mensaje sin responder o cortar la falsa normalidad televisiva"
  systemic_benefit: "reduce el crecimiento más obvio del foco elegido y desplaza la sensación de control hacia el jugador"
  systemic_risk: "si se contiene una zona, la otra queda libre para fermentar y la noche no desaparece, sólo cambia de tono"

tv_material:
  baseline_content: "magazine o tertulia de confort pandémico, voces que acompañan sin decir nada verdaderamente útil"
  parasitic_line_pool:
    - "hoy conviene tomárselo con calma"
    - "ya habrá tiempo para ponerse al día"

exterior_material:
  window_event: "vecino o figura a distancia con rutina ambigua pero aún creíble; nada amenaza, sólo observa el tiempo detenido"
  peephole_event: "silencio en el rellano o ruido lejano de bolsa/pasos; mirar ofrece poco contexto"
  balcony_event: "no recomendado aún como escena central; puede existir sólo como tentación de aire"

day_closing_debt:
  unresolved_relation: "el editor queda instalado como deuda suave y la madre puede quedar ligeramente herida o invasiva según respuesta"
  unresolved_zone: "salón o baño, según qué foco haya quedado sin contener"
  unresolved_truth: "la vida ya estaba torcida antes de empezar; no se inaugura hoy, sólo se reconoce"

handoff_to_transition:
  light_shift_meaning: "la tarde no trae épica, sólo cansancio y una pequeña bajada de temperatura emocional"
  sound_shift_meaning: "la casa suena más presente cuando bajan los estímulos del móvil"
  first_door_hint: "al pasar por el pasillo, la puerta atrancada puede parecer más húmeda o más densa que esta mañana, aunque todavía parezca una paranoia leve"
```

---

## 2. Notas de dirección

### 2.1. Tono
Nada debe entrar con espectáculo. Este día necesita la vulgaridad del encierro: mensajes reales, incomodidades pequeñas, una televisión que acompaña demasiado, una exigencia laboral que aún puede racionalizarse y un apartamento que no asusta pero tampoco descansa.

### 2.2. Jerarquía jugable
La presión activa es el editor, pero no debe monopolizar el día. La madre y el amigo deben dejar claro, desde ya, que las relaciones viven en continuidad y no por bloques.

### 2.3. Función de la pareja/ex
Todavía no entra en escena. Sólo debe sentirse como un hueco con peso específico en el dormitorio.

### 2.4. Contención
La contención del ciclo 1 no debe sentirse heroica. Debe sentirse mezquina, mínima y casi ridícula, pero decisiva: ordenar un vaso o rascar una junta es ya elegir qué podredumbre atrasas.

---

## 3. Salidas sistémicas recomendadas

### Si el jugador prioriza al editor
- baja algo la deuda laboral inmediata,
- pero el salón queda colonizado por utilidad y autoexigencia,
- y la TV puede hablar con tono funcional al cierre del día.

### Si el jugador prioriza a la madre
- el cuerpo y baño/dormitorio ganan centralidad,
- se amortigua la culpa filial,
- pero el editor queda peor colocado en suspensión.

### Si el jugador se refugia en el amigo/TV
- gana una falsa sensación de normalidad,
- sube la pasividad,
- y el foco del salón se vuelve más apto para voz latente.

### Si el jugador contiene una zona
- no “gana” el día,
- sólo mueve el residuo a otro sitio y modifica la textura de la primera noche.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **primera ficha real de día** del proyecto. Su función no es impresionar: es demostrar que el modelo de continuidad relacional, foco contaminante, contención limitada y puerta gestante ya puede producir un día jugable coherente sin romper el tono.
