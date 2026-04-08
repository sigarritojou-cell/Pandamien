# PANDAMIEN — ANEXO E
## Ficha real de noche — Ciclo 6: Colonización semántica
### Derivada del GDD Maestro v03, del Anexo M v01, del Anexo I v01, de la ficha de día C06 y de los pilotos nocturnos de los ciclos 1–5

---

## 0. Intención de la noche

La sexta noche no debe hacerse “más grande”. Debe hacerse más habladora de la peor manera posible. Si en C03 la puerta respiraba, en C04 parecía padecer y en C05 enfocaba, en C06 **ensaya sintaxis**. Todavía no habla limpio. Y justamente por eso da más dentera: porque el jugador percibe que detrás de la madera ya no hay sólo función, mirada o pecho, sino una forma defectuosa de hilar tonos, palabras rotas, medias frases, ritmos ajenos y restos de conversación que el piso ha ido rumiando durante días.

La función dramática de esta noche es:

- traducir la mezcla semántica del día en una presencia verbal más legible y más obscena,
- confirmar que la criatura ya no sólo imita voces sueltas: intenta organizarlas,
- contaminar puerta, TV, salón y pasillo con fraseo roto, llamada fallida, pausa escuchante o masticación verbal,
- reducir todavía más la frontera entre acompañamiento mediático y habla monstruosa,
- y cerrar el ciclo con una verdad nueva: la casa ya no sólo te respira y te mira; empieza a **contestarte mal**.

---

## 1. Ficha oficial

```yaml
cycle_id: "C06"
cycle_title: "Colonización semántica"
night_theme: "la casa ya ensaya decir"

inherited_from_day:
  unresolved_relation: "varias deudas abiertas a la vez; ninguna voz queda limpia"
  unresolved_zone: "salón o pasillo, con goteo a dormitorio o cocina según historial"
  unresolved_choice: "se escuchó demasiado, se cortó tarde o se intentó ordenar un ruido que ya estaba dentro"
  tv_seed: "manipulation inicial a partir de suggestion semántica"

night_entry_state:
  apartment_tension_level: "high"
  active_zones:
    - "pasillo"
    - "salón"
    - "puerta atrancada"
    - "dormitorio o cocina como resonancia secundaria"
  tv_state: "manipulation blanda con restos de suggestion"
  stability_bias: "la realidad sigue siendo legible, pero atribuir ya no sirve; el jugador oye cosas reconocibles sin poder devolverlas a un origen estable"

ambient_progression:
  phase_1: "al bajar el ruido del día, la TV residual, el portátil, los tejidos del salón y el pasillo parecen formar una sola corriente de fondo"
  phase_2: "la puerta atrancada concentra el lenguaje tragado: silencios con intención, respiración que parece preparar frase, roce como toma de aire"
  phase_3: "se produce un retorno verbal defectuoso: sílaba emocional, fragmento reconocible, llamada sin dueño claro, frase cortada o mezcla breve de tonos que no debería existir"

relational_return:
  main_echo_source: "TV / mezcla de vínculos"
  secondary_echo_source: "Editor, Madre, Pareja/Ex o Amigo según el patrón dominante del día"
  form: "door + tv + hallway + living_room"
  distortion_type: "frases robadas, sintaxis fallida, llamada corporal, humor hueco, cuidado intrusivo y utilidad medida mezclados en una sola emisión imperfecta"
  emotional_effect: "el jugador entiende que la criatura ya no sólo devuelve residuo: empieza a devolver interpretación"

door_behavior:
  material_state: "marco menos húmedo y más tenso, como si la presión interna ya no fuera sólo de masa o pecho sino de organización"
  sound_bank_primary: "sílaba rota, fragmento de frase, exhalación que parece preparar palabra, tono robado que se corta"
  sound_bank_secondary: "masticación verbal, roce seco, pausa atenta, pequeño golpe con intención de marcar ritmo"
  pressure_level: "medium_high"
  player_proximity_response: "al acercarse, la puerta puede callarse justo antes de decir algo o repetir sólo un resto insoportable, como si estuviera corrigiendo el ensayo"
  frame_reactivity: "escuchar pegado al marco aumenta legibilidad, pero también amenaza con enseñar mejor la voz del jugador a la criatura"

creature_activity:
  dominant_function: "voz / imitación / sintaxis defectuosa"
  secondary_function: "ojos y atención dirigida heredados de C05; pecho o corazón residuales según historial afectivo"
  temperament_bias: "imitativo tendiendo a rencoroso o suplicante según trato acumulado"
  manifestation_rules:
    - "nada de frase limpia larga"
    - "debe sentirse como lenguaje aprendido por digestión, no por comprensión estable"
    - "si dominó editor, el retorno debe oler a medición, urgencia, corte o evaluación"
    - "si dominó madre, debe colarse cuidado clínico, descanso, orden o lectura corporal"
    - "si dominó amigo, puede aparecer chiste vacío, banalidad podrida o parloteo sin centro"
    - "si dominó pareja/ex, una palabra o pausa afectiva puede torcer toda la mezcla"
    - "la criatura no habla todavía como personaje pleno; habla como archivo mal cosido"

apartment_events:
  - zone: "Salón"
    condition: "si quedó como foco principal"
    event: "la TV deja una línea tardía demasiado íntima, o un brillo residual coincide con una media frase tras la puerta"
    interpretation_space: "ya no puede saberse bien qué inició qué"
  - zone: "Pasillo"
    event: "el trayecto a la puerta parece una frase que el jugador debe terminar con el cuerpo"
    interpretation_space: "órgano lingüístico, no corredor encantado"
  - zone: "Dormitorio"
    condition: "si pareja/ex o madre siguieron resonando"
    event: "el móvil, la cama o el silencio del cuarto conservan una palabra no dicha que la puerta parece recoger después"
    interpretation_space: "la intimidad ya alimenta la sintaxis monstruosa"
  - zone: "Cocina"
    condition: "si amigo o abandono funcional pesaron mucho"
    event: "una nevera, un fregadero o un plato parecen emitir compañía hueca o digestión de fondo"
    interpretation_space: "humor, hambre y palabra pueden parecer la misma cosa"
  - zone: "Entrada / umbral"
    condition: "si el jugador ha insistido mucho en mirar o escuchar bordes"
    event: "puerta principal y puerta atrancada parecen repartirse la atención del piso"
    interpretation_space: "la casa habla por varias bocas, pero mastica en una"

night_actions_available:
  - action: "acercarse a la puerta y escuchar la frase rota"
    cost: "sube threat_intimacy, baja estabilidad y acelera la capacidad imitativa de criatura"
    possible_outcome: "el jugador confirma que la puerta ya no sólo ensaya ruido: ensaya respuesta"
  - action: "apagar definitivamente la TV o cortar la fuente de salón"
    cost: "el silencio posterior es más cruel y deja el retorno de la puerta más desnudo"
    possible_outcome: "baja contaminación mediática superficial, sube crudeza de la presencia"
  - action: "permanecer en el pasillo esperando otra emisión"
    cost: "convierte la escucha en relación y vuelve el trayecto parte del ritual"
    possible_outcome: "el jugador obtiene más legibilidad verbal, pero cede más intimidad"
  - action: "hablarle a la puerta"
    cost: "altísimo riesgo de enseñar tono, ritmo y trato directo"
    possible_outcome: "siembra respuesta futura más clara y hace más viable un final dialogado muy personal"
  - action: "ignorar, medicarse o retirarse"
    cost: "sube avoidance y deja que la sintaxis de la criatura madure fuera de escena"
    possible_outcome: "el siguiente día arranca con menos inocencia verbal y más mezcla incrustada"

micro_containment_if_any:
  is_available: true
  action: "apagar TV, cerrar portátil, retirar objeto del salón que sostiene el frente semántico o cortar una cadena relacional abierta"
  cost: "es parcial, llega tarde y nunca silencia todo a la vez"
  effect: "amortigua una vía de mezcla pero fortalece otra: menos eco mediático, más puerta; menos puerta aparente, más residuo en dormitorio o cocina"

closure_options:
  sleep: "aceptar que el piso ya tiene una forma tosca de lenguaje propio y pasar al siguiente día con una atención rota"
  medication: "recortar exposición y volver más borroso el retorno, pero reforzar el corte como dependencia"
  stay_awake: "empujar la escucha hasta convertirla en vínculo más que en evento"
  threshold_action: "escuchar, tocar el marco, apagar la TV a destiempo o hablarle a la nada para medir si algo contesta"

persistence_out:
  relation_shift: "las voces quedan menos separables y el jugador empieza a anticipar mezcla antes de que ocurra"
  zone_shift: "salón y pasillo quedan establecidos como eje de sintaxis contaminada"
  tv_shift: "manipulation gana legitimidad y puede actuar casi como comentarista de deudas"
  creature_shift: "la criatura obtiene imitación y fraseo defectuoso como capacidad estable"
  door_shift: "la puerta ya no es sólo promesa de cuerpo; es promesa de interlocución monstruosa"
  emotional_truth_learned: "el apartamento ya no devuelve sólo presencia: devuelve respuesta"
```

---

## 2. Notas de dirección

### 2.1. Regla de frase
La frase rota tiene que doler más que una frase limpia. Si se entiende del todo, se vuelve truco. Si no se reconoce nada, se vuelve ruido. El punto bueno es la comprensión casi completa que se pudre justo antes de cerrarse.

### 2.2. Regla de mezcla vocal
La mezcla de voces no debe sonar a efecto digital de tres pistas a la vez. Debe parecer un origen único lleno de restos humanos mal metabolizados.

### 2.3. Regla de TV
La TV ya puede ser abiertamente oportunista, pero no omnipotente. Sigue siendo un aparato diegético contaminado, no un dios narrador.

### 2.4. Función emocional
La noche de C06 debe dejar al jugador con la sensación insoportable de que el piso empieza a tratarle como si ya hubiera conversación en curso.

---

## 3. Persistencia recomendada hacia Ciclo 7

- El siguiente ciclo puede superponer dos presiones incompatibles porque la criatura ya tiene material para devolver ambas a la vez.
- La TV queda lista para robar líneas completas, no sólo tonos o temas.
- La puerta está preparada para una fase donde la palabra y la agresividad puedan convivir.
- El pasillo queda consolidado como órgano de tránsito verbal, no sólo físico.
- El final dialogado gana densidad: la criatura ya no será sólo presencia íntima, sino interlocutor deformado.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **sexta ficha real de noche** del proyecto. Demuestra que PANDAMIEN puede acercarse a la palabra sin romper su misterio central: la criatura no explica, no monologa y no pontifica; **ensaya contestar** con la basura humana que ha ido aprendiendo a tragos.
