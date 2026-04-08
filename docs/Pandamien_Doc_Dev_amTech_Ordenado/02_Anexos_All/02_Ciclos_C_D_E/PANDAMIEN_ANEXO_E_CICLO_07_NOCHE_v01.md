
# PANDAMIEN — ANEXO E
## Ficha real de noche — Ciclo 7: Doble vínculo imposible
### Derivada del GDD Maestro v04, del Anexo M v01, del Anexo I v01, de la ficha de día C07 y de los pilotos nocturnos de los ciclos 1–6

---

## 0. Intención de la noche

La séptima noche no debe limitarse a “subir intensidad”. Tiene que **dictar sentencia**. Si en C06 la casa ensayaba sintaxis, aquí ensaya trato. Ya no devuelve sólo restos mezclados: devuelve una manera de colocarse frente al jugador. Lo decisivo no es si suena más fuerte, sino si se nota que detrás de la madera hay algo que ya ha decidido cómo mirarte, cómo esperarte y cómo apretarte.

La función dramática de esta noche es:

- traducir el sacrificio del día en una presencia casi organizada,
- hacer que la puerta deje de parecer sólo un órgano y se vuelva casi postura,
- fijar el **temperamento dominante** de la criatura según el historial inmediato y acumulado,
- convertir pasillo, zona sacrificada y salón/baño en un pequeño tribunal doméstico,
- llevar la TV a confrontational pleno o a silencio acusatorio,
- y cerrar el ciclo con una verdad durísima: la casa ya no sólo recuerda lo que dejaste pudrir; **ha decidido qué hacer contigo**.

---

## 1. Ficha oficial

```yaml
cycle_id: "C07"
cycle_title: "Doble vínculo imposible"
night_theme: "la casa ya toma partido"

inherited_from_day:
  unresolved_relation: "colisión no resuelta entre Madre y Editor; pareja/ex y amigo como eco moral secundario"
  unresolved_zone: "la zona sacrificada del día"
  unresolved_choice: "se eligió cuerpo o trabajo, o se traicionaron ambos por aplazamiento"
  tv_seed: "confrontational, acusatorio, editorialmente cruel"

night_entry_state:
  apartment_tension_level: "very_high"
  active_zones:
    - "pasillo"
    - "puerta atrancada"
    - "zona sacrificada"
    - "salón o baño según la pérdida dominante"
  tv_state: "confrontational o silencio residual demasiado consciente"
  stability_bias: "la realidad sigue siendo reconocible, pero el jugador ya no puede fingir que la casa responde de forma neutra"

ambient_progression:
  phase_1: "el apartamento baja el ruido normal y deja sólo aquello que acusa: respiración propia, reloj, aparato residual, tubería, tejido, nevera, madera"
  phase_2: "el pasillo concentra no sólo atención sino criterio; caminar hacia la puerta parece ir hacia una versión monstruosa de la decisión tomada"
  phase_3: "se produce un retorno casi organizado: ritmo de espera, golpe con intención, frase fallida ya no meramente imitativa, respiración que juzga o suplica según temperamento"

relational_return:
  main_echo_source: "sacrificio del día"
  secondary_echo_source: "TV confrontational + uno de los vínculos heridos"
  form: "door + hallway + sacrificed_zone"
  distortion_type: "el cuidado, la utilidad o la mentira reaparecen como forma de trato monstruoso"
  emotional_effect: "el jugador entiende que el monstruo ya no sólo sabe hablar mal; sabe posicionarse ante él"

door_behavior:
  material_state: "marco tenso, humedad y presión más organizadas, madera menos hinchada y más a punto de ceder por empuje interno sostenido"
  sound_bank_primary: "golpe medido, pausa evaluativa, exhalación con intención, intento de frase breve, roce de peso que se recoloca"
  sound_bank_secondary: "latido seco, respiración cortada, pequeña sílaba, raspado del marco o arrastre mínimo con voluntad"
  pressure_level: "high"
  player_proximity_response: "al acercarse, la puerta puede callarse como quien espera respuesta, devolver un golpe si el jugador habla, o repetir sólo el tono más cruel de la decisión tomada"
  frame_reactivity: "tocar el marco puede dar vibración organizada, calor, humedad o una sensación de cuerpo al otro lado que ya sabe dónde apoyarse"

creature_activity:
  dominant_function: "temperamento dominante + voz/pecho/presión coordinada"
  secondary_function: "depende de historial: garganta verbal, respiración, ojos u orientación residuales"
  temperament_bias:
    if_body_sacrificed:
      primary: "furioso o rencoroso"
      manifestation: "golpe medido, evaluación hostil, respiración contenida con mala leche"
    if_work_sacrificed:
      primary: "doliente o suplicante"
      manifestation: "latido triste, frase rota que pide o espera, presión menos violenta pero más insoportable"
    if_both_avoided:
      primary: "imitativo o famélico"
      manifestation: "voz mal cosida, hambre verbal, mezcla de registros, presencia pegajosa y falsa"
  manifestation_rules:
    - "no frase larga limpia"
    - "debe sentirse como una conducta, no sólo como un ruido"
    - "si se sacrificó el cuerpo, el retorno debe oler a resentimiento contra la carne abandonada"
    - "si se sacrificó el trabajo, el retorno puede sonar a espera triste, evaluación doliente o exigencia fallida"
    - "si se sacrificó la verdad, el retorno debe mezclar tonos sin honestidad posible"
    - "la puerta aguanta a duras penas: todavía no se paga la promesa final, pero ya cruje como si supiera que se acerca"

apartment_events:
  - zone: "Pasillo"
    event: "deja de sentirse sólo estrecho; parece una línea de juicio. Caminarlo es ponerse delante de lo que se ha decidido."
    interpretation_space: "órgano moral del piso, no corredor encantado"
  - zone: "Zona sacrificada"
    event: "la materialidad acusa recibo con demasiada claridad: baño pegajoso, espejo hostil, cama mala, o salón convertido en mesa de derrota"
    interpretation_space: "la zona no se vuelve mágica; se vuelve indiscutible"
  - zone: "Salón"
    condition: "si se sacrificó trabajo o si el editor quedó abierto"
    event: "portátil, TV o reloj parecen sostener una presencia acusatoria incluso apagados"
    interpretation_space: "lo útil ya no es neutro ni muerto"
  - zone: "Baño/Dormitorio"
    condition: "si se sacrificó el cuerpo o si madre quedó herida"
    event: "humedad, tela, cama, espejo o olor parecen guardar la forma de una caída que no se atendió"
    interpretation_space: "intimidad corporal degradada antes que horror explícito"
  - zone: "TV"
    condition: "si se dejó activa o si el jugador la usó de refugio"
    event: "una frase tardía, un corte de emisión o un silencio de plató cae justo cuando la puerta parece escuchar"
    interpretation_space: "el acompañamiento se ha convertido en acusación editorial"

night_actions_available:
  - action: "acercarse a la puerta y escuchar sin hablar"
    cost: "sube intimidad de amenaza y puede fijar mejor el temperamento de la criatura"
    possible_outcome: "el jugador reconoce si lo que hay detrás está doliente, rencoroso, imitativo o famélico"
  - action: "hablarle a la puerta"
    cost: "enseña más del tono del jugador a la criatura y prepara con más fuerza la confrontación final"
    possible_outcome: "la puerta devuelve un golpe, una pausa o un resto verbal con intención"
  - action: "revisar la zona sacrificada"
    cost: "obliga a ver la pérdida material que se ha aceptado"
    possible_outcome: "aparece una oportunidad mínima de contención tardía que ya no salva el ciclo, sólo matiza el trato nocturno"
  - action: "buscar anestesia en TV, medicación o cama"
    cost: "reduce exposición inmediata pero refuerza avoidance, dependencia del corte o derrota"
    possible_outcome: "el jugador llega al cierre con menos roce directo y más deuda"

micro_containment_if_any:
  is_available: true
  action: "gesto tardío de reparación en la zona sacrificada"
  cost: "altísimo en verdad moral y casi inútil en eficacia"
  effect: "no cancela la noche; sólo puede desplazar el temperamento de la criatura de furia a rencor, de súplica a tristeza o de hambre a imitación"
  note: "La contención aquí ya no trata de crecimiento, sino de modulación de trato."

closure_options:
  sleep: "aceptar que la pérdida ya tiene voz y pasar al último día con una relación monstruosa casi definida"
  medication: "recortar exposición, reforzando quizá la sensación de cuerpo administrado y de corte artificial"
  stay_awake: "sostener el juicio del pasillo y llegar más abierto al ciclo final"
  threshold_action: "quedarse cerca de la puerta, tocar el marco, hablar o no apartarse del sitio"

persistence_out:
  relation_shift: "la relación con madre o editor queda ya definitivamente torcida por el tipo de sacrificio realizado; pareja/ex y amigo absorben residuo moral del día"
  zone_shift: "la zona sacrificada entra al ciclo final como prueba material del historial"
  creature_shift: "el temperamento dominante queda casi fijado para la confrontación"
  tv_shift: "la TV puede callar más en C08 o hablar sólo como respiración acusatoria de fondo"
  global_truth: "el monstruo ya no es sólo acumulación; es carácter aprendido"

cycle_truth: "Cuando ya no se puede sostener todo, la forma de perder se convierte en personalidad del horror."
```

---

## 2. Gramática de temperamento resultante

### 2.1. Si dominó la pérdida del cuerpo
La criatura debe sentirse:
- más dura,
- más cortante,
- menos suplicante,
- más rencorosa o furiosa.

Señales:
- golpes medidos,
- respiración contenida,
- pausa seca,
- menos pecho doliente y más mala leche organizada.

### 2.2. Si dominó la pérdida funcional / laboral
La criatura debe sentirse:
- más doliente,
- más evaluativa,
- más triste que explosiva,
- más suplicante o decepcionada.

Señales:
- frase rota que casi pide,
- latido cansado,
- espera prolongada,
- menos rabia pura y más herida consciente.

### 2.3. Si dominó la huida / mentira / aplazamiento general
La criatura debe sentirse:
- más imitativa,
- más pegajosa,
- más hambrienta de voz,
- menos estable en su trato.

Señales:
- mezcla de tonos,
- banalidad podrida,
- llamada fallida,
- hambre verbal,
- presencia que no acaba de decidir si pide, acusa o mastica.

---

## 3. Validaciones para pasar al Ciclo 8

Antes de abrir la resolución, este documento debe dejar claras estas cuatro cosas:

1. La criatura **ya tiene modo de tratar** al jugador, no sólo anatomía.
2. Hay una **zona sacrificial** materialmente legible para el cierre.
3. La **TV** ya puede retirarse parcialmente sin perder función, porque su trabajo está hecho.
4. El jugador llega al último ciclo sabiendo que la puerta ya no contiene “algo”, sino **una forma de relación**.

Si una de estas cuatro patas falla, la resolución entrará floja o demasiado expositiva.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **séptima capa authored de noche del proyecto**. No cierra todavía la promesa mayor de la puerta, pero sí deja fijado el punto exacto donde la criatura pasa de archivo monstruoso a **temperamento reconocible**. El siguiente ciclo ya no podrá tratarla como mera presencia: tendrá que tratarla como interlocutor en ciernes.
