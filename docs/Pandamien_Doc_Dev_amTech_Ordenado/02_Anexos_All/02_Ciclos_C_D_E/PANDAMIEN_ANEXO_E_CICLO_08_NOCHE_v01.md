# PANDAMIEN — ANEXO E
## Ficha real de noche — Ciclo 8: Resolución
### Derivada del GDD Maestro v04, del Anexo M v01, del Anexo I v01, de la ficha de día C08 y de los pilotos nocturnos de los ciclos 1–7

---

## 0. Intención de la noche

La octava noche no debe funcionar como “jefe final” ni como gran revelación explicativa. Debe funcionar como **devolución ética y corporal**. Si en la primera noche la casa respondió, en la segunda articuló mejor, en la tercera respiró, en la cuarta padeció, en la quinta miró, en la sexta ensayó sintaxis y en la séptima fijó temperamento, en la octava por fin **dialoga y actúa según lo que ha aprendido del jugador**.

La criatura no debe volverse de pronto completamente humana ni completamente monstruosa. Debe mantenerse en ese punto indecente donde resulta legible y al mismo tiempo insoportable: reconoce tonos, devuelve ritmos, intenta pedir, medir, juzgar, suplicar o invadir según historial; pero sigue siendo una forma viva mal cosida, nacida del piso y de la deuda.

La función dramática de esta noche es:

- pagar la promesa total de la puerta atrancada,
- permitir una confrontación dialogada real con la criatura,
- hacer que el tono de la criatura refleje trato acumulado y no moralina abstracta,
- convertir el apartamento completo en testigo y cuerpo de la confrontación,
- ofrecer salidas compatibles con el canon: contención, apertura, convivencia precaria, absorción, ruptura o escucha radical,
- y cerrar el ciclo sin limpieza total, dejando una resolución coherente con el historial del jugador.

---

## 1. Ficha oficial

```yaml
cycle_id: "C08"
cycle_title: "Resolución"
night_theme: "por fin te devuelve la palabra"

inherited_from_day:
  unresolved_relation: "historial total condensado en una o dos deudas dominantes"
  unresolved_zone: "pasillo/puerta + la zona más sacrificada de la partida"
  unresolved_choice: "cómo se ha preparado el umbral: cuidado, orden, negación, escucha, violencia, apertura o aplazamiento residual"
  tv_seed: "confrontational residual o silencio ya incapaz de ocultar nada"

night_entry_state:
  apartment_tension_level: "max_but_intimate"
  active_zones:
    - "pasillo"
    - "puerta atrancada"
    - "zona dominante del historial"
    - "salón o dormitorio como coro secundario"
  tv_state: "apagada, residual o ya absorbida semánticamente por la casa"
  stability_bias: "la realidad deja de servir como refugio interpretativo; no se rompe del todo, pero ya no protege"

ambient_progression:
  phase_1: "el apartamento baja a una quietud demasiado organizada; cada zona parece esperar un gesto del jugador"
  phase_2: "el pasillo se convierte en un eje de atención total; la puerta ya no pesa como obstáculo sino como presencia recíproca"
  phase_3: "se inicia el contacto: respiración, frase rota, silencio escuchante o primer intercambio verbal defectuoso"
  phase_4: "umbral de decisión: abrir, contener, hablar desde fuera, ceder, sostener, dejar entrar, romper o absorber"
  phase_5: "resolución según trato acumulado y postura final del jugador"

relational_return:
  main_echo_source: "Criatura como mezcla del historial"
  secondary_echo_source: "vínculo dominante de la partida"
  form: "door + apartment + dialogue"
  distortion_type: "devolución verbal, corporal y ética del trato acumulado"
  emotional_effect: "el jugador comprende que la criatura no está improvisando un papel; está usando el idioma que se le enseñó"

threshold_state:
  can_open: true
  can_listen_without_opening: true
  can_attempt_containment: true
  can_speak_first: true
  can_refuse_and_absorb_consequences: true
  note: "La noche no obliga a una única vía, pero todas deben ser irreversibles en tono."

door_behavior:
  material_state: "marco cediendo o ya semiabierto según historial; humedad, tensión, aire retenido y textura demasiado orgánica"
  sound_bank_primary: "frase rota, respiración, latido, pausa escuchante, tono robado o petición defectuosa"
  sound_bank_secondary: "golpe de peso, arrastre coordinado, roce de pecho, masticación verbal o silencio que se comporta como réplica"
  pressure_level: "decisive"
  player_proximity_response: "la criatura responde al tono, a la distancia y a la postura del jugador; no sólo a la acción binaria de abrir/no abrir"
  frame_reactivity: "tocar, apoyar la frente, hablar o intentar bloquear el marco altera cómo la criatura devuelve presencia"

creature_activity:
  dominant_function: "voz dialogada + anatomía dominante según historial"
  secondary_function: "temperamento dominante fijado en C07 + residuos de todos los actos anteriores"
  temperament_branches:
    sociable_reasonable:
      conditions: "más confrontación honesta, más escucha, menos abandono cruel, contención menos evasiva"
      return_style: "pregunta, mide, pide, acusa con lógica triste, busca reconocimiento"
    doliente_suplicante:
      conditions: "más cuidado a medias, más culpa íntima, más cuerpo sacrificado con vergüenza"
      return_style: "pide amparo, nombra faltas, busca proximidad, duele más que amenaza"
    imitativo_famelico:
      conditions: "mucha mezcla, mucho ruido, mucha evasión y mucha TV/móvil en sustitución de vínculo"
      return_style: "repite, mastica, hace collage de voces, busca seguir tragando lenguaje y presencia"
    rencoroso_furioso:
      conditions: "abandono duro, negación continuada, sacrificio del cuerpo o del otro sin asumirlo"
      return_style: "mide, acusa, invade, empuja, usa frases como cuchillos rotos"
  manifestation_rules:
    - "nada de discurso largo limpio"
    - "la criatura debe sonar y moverse como alguien/algo que ha aprendido a hablar desde el residuo"
    - "la anatomía visible o insinuada debe corresponderse con zonas y funciones realmente alimentadas"
    - "si el jugador habla primero, importa tanto el tono como el contenido"
    - "la confrontación no es resolver un puzzle; es sostener una relación límite"

apartment_events:
  - zone: "Pasillo"
    event: "ya no es trayecto: es el lugar donde el piso obliga al jugador a tomar posición"
    interpretation_space: "juicio espacial, no pasadizo encantado"
  - zone: "Puerta atrancada"
    event: "se comporta como boca, pecho, ojo o frontera ética según el momento"
    interpretation_space: "umbral vivo"
  - zone: "Salón"
    condition: "si TV y editor fueron muy fuertes"
    event: "pantalla residual, brillo muerto, frase tardía o silencio utilitario que todavía pincha"
    interpretation_space: "el mundo funcional mira sin ayudar"
  - zone: "Dormitorio"
    condition: "si pareja/ex y madre fueron dominantes"
    event: "cama, móvil o tela siguen pesando como vida no resuelta"
    interpretation_space: "la intimidad asiste al juicio"
  - zone: "Baño"
    condition: "si el cuerpo fue gran deuda"
    event: "humedad, espejo o toalla devuelven cuerpo y vergüenza"
    interpretation_space: "la carne no quedó fuera de la conversación"

night_actions_available:
  - action: "hablarle a la puerta sin abrir"
    cost: "permite medir, pero también entrega tono y vulnerabilidad"
    possible_outcome: "la criatura responde desde el marco con más o menos legibilidad"
  - action: "abrir el umbral"
    cost: "no hay vuelta atrás simbólica"
    possible_outcome: "la confrontación se vuelve más corporal y más comprometida"
  - action: "intentar contener o bloquear"
    cost: "puede endurecer el temperamento del encuentro"
    possible_outcome: "abre vías de contención precaria o de ruptura hostil"
  - action: "escuchar hasta el límite"
    cost: "sube amenaza íntima y absorción"
    possible_outcome: "más verdad, menos distancia"
  - action: "llevar un objeto-signo al umbral"
    cost: "expone una relación dominante"
    possible_outcome: "modifica el sesgo del diálogo final"

final_route_categories:
  containment:
    tone: "aceptar que no se destruye, pero se encuadra"
    emotional_core: "responsabilidad amarga"
  opening_dialogue:
    tone: "entrar en conversación plena o casi plena"
    emotional_core: "devolución ética"
  coexistence:
    tone: "no resolución limpia; pacto indecente"
    emotional_core: "vivir con la grieta"
  absorption:
    tone: "dejar que el piso/yo/monstruo se mezclen"
    emotional_core: "ya no había frontera que salvar"
  rupture:
    tone: "acto violento o desesperado sin limpieza moral"
    emotional_core: "rechazo tardío con coste"

closure_truth: "El final no decide si el monstruo tenía razón. Decide si el jugador puede por fin mirarlo como algo que también le pertenece."
```

---

## 2. Gramática de confrontación recomendada

### 2.1. Regla de postura
La criatura debe reaccionar a la **postura** del jugador:
- acercarse con escucha,
- acercarse con rabia,
- abrir con culpa,
- abrir con necesidad de acabar,
- no abrir pero sostener palabra,
- no abrir y seguir negando.

### 2.2. Regla de trato devuelto
La criatura debe ser tan:
- sociable,
- razonable,
- manipuladora,
- imitativa,
- famélica,
- doliente,
- rencorosa,
- o violenta,
como el historial permita.

### 2.3. Regla de cuerpo coherente
Si la criatura ha ganado más:
- **voz**: el final tendrá más fraseo y medición.
- **pecho/corazón**: más súplica, latido y duelo.
- **ojos/orientación**: más pausa, mirada y cálculo.
- **hambre/bilis**: más masticación, digestión y ruido obsceno.
- **piel/mucosa**: más humedad, roce y cercanía invasiva.

### 2.4. Regla de no explicación total
La criatura puede revelar sentido, pero no debe resolverlo todo con un monólogo de notario mal cagado. El final tiene que dejar misterio suficiente para seguir siendo organismo, no powerpoint.

---

## 3. Desencadenantes de cierre

### 3.1. Si el jugador habla primero con honestidad
La criatura tenderá más a:
- responder con pregunta,
- pedir reconocimiento,
- doler antes que empujar,
- o aceptar contención amarga.

### 3.2. Si el jugador abre desde la negación o la violencia
La criatura tenderá más a:
- medir,
- empujar,
- repetir reproches,
- o fijar una resolución más hostil y menos negociable.

### 3.3. Si el jugador escucha demasiado sin actuar
La criatura tenderá más a:
- absorber tono,
- imponerse semánticamente,
- o arrastrar al jugador hacia coexistencia o absorción.

### 3.4. Si el jugador llega cuidado y ordenado
El encuentro gana legibilidad, pero también intimidad. No facilita “ganar”; facilita ver mejor la relación.

### 3.5. Si el jugador llega roto, anestesiado o saturado
El final tiende más a collage, violencia, confusión o cesión de agencia.

---

## 4. Notas de dirección

- El final debe doler más por **reconocimiento** que por susto.
- La criatura no es el enemigo final de una historia clásica; es la forma final del conflicto.
- La habitación sellada debe sentirse como culminación del apartamento, no como mapa secreto de otro juego.
- Ninguna resolución debe dejar el piso completamente limpio. El canon prohíbe esa mentira.

---

## 5. Cierre de diseño

La octava noche convierte la puerta atrancada en lo que siempre fue: **una conversación aplazada hasta adquirir cuerpo**.
