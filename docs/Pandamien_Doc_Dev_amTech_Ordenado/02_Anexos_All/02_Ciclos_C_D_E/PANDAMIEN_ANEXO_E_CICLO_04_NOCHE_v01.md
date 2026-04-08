# PANDAMIEN — ANEXO E
## Ficha real de noche — Ciclo 4: La herida íntima
### Derivada del GDD Maestro v03, del Anexo M v01, del Anexo I v01, de la ficha de día C04 y de los pilotos nocturnos de los ciclos 1, 2 y 3

---

## 0. Intención de la noche

La cuarta noche no debe hacerse “más monstruosa” por añadir músculo sonoro sin cabeza. Debe volverse más sentimental en el peor sentido de la palabra: más íntima, más torpe, más pegada al pecho, a la súplica y a la posibilidad obscena de que algo detrás de la puerta esté empezando a sentir a su manera. Si en la primera noche la casa respondió, en la segunda articuló mejor y en la tercera respiró con el jugador, en la cuarta empieza a parecer que padece.

La función dramática de esta noche es:

- devolver la herida íntima del día como presencia torácica, afectiva y casi suplicante,
- confirmar que la puerta ya puede alojar no sólo función corporal, sino una emoción monstruosamente aprendida,
- contaminar dormitorio, balcón y pasillo con un latido o una voz emocional fallida,
- llevar la TV a suggestion sentimental o a manipulación blanda,
- y cerrar el ciclo con una verdad incómoda: lo íntimo mal resuelto no se queda en memoria; busca cuerpo.

---

## 1. Ficha oficial

```yaml
cycle_id: "C04"
cycle_title: "La herida íntima"
night_theme: "la casa ya padece mal el afecto"

inherited_from_day:
  unresolved_relation: "pareja/ex activada y no resuelta; madre y editor como tensiones cruzadas de fondo"
  unresolved_zone: "dormitorio o balcón, según la contención fallida o insuficiente"
  unresolved_choice: "se abrió la herida, se dejó a medias o se intentó cerrar sin atravesarla"
  tv_seed: "suggestion sentimental mezclándose con manipulación leve"

night_entry_state:
  apartment_tension_level: "medium_to_high"
  active_zones:
    - "pasillo"
    - "dormitorio o balcón, según foco dominante"
    - "salón residual si la TV o el editor siguen contaminando"
  tv_state: "suggestion sentimental tendiendo a manipulación blanda"
  stability_bias: "la realidad sigue siendo legible, pero la casa ya parece demasiado capaz de acompañar mal lo íntimo"

ambient_progression:
  phase_1: "el apartamento baja a un silencio con pecho: tejidos, cama, cristal del balcón, nevera lejana, televisión residual y una respiración propia que ya no parece del todo privada"
  phase_2: "el pasillo concentra más gravedad emocional; la puerta atrancada no pesa sólo como órgano, sino como alguien que ha empezado a esperar"
  phase_3: "se produce un retorno más afectivo y más jodido: latido torpe, exhalación suplicante, sílaba emocional rota, roce de pecho contra madera o pausa demasiado humana"

relational_return:
  main_echo_source: "Pareja/Ex"
  secondary_echo_source: "Madre o Editor, según historial del día"
  form: "door + bedroom + balcony"
  distortion_type: "intimidad convertida en latido sin cuerpo, voz emocional mal aprendida, pausa afectiva vigilante o súplica torpe"
  emotional_effect: "el jugador entiende que la criatura no sólo sabe respirar; empieza a saber echar de menos, reclamar o dolerse de forma monstruosamente parcial"

door_behavior:
  material_state: "marco húmedo pero más tenso; la madera parece menos pared y más caja torácica; la rendija o el entorno del marco acumulan sensación de aire retenido"
  sound_bank_primary: "latido blando, exhalación suplicante, sílaba emocional rota o respiración con pena"
  sound_bank_secondary: "golpe de pecho sin fuerza, tela o membrana, pausa demasiado atenta, arrastre mínimo si el pasillo heredó peso"
  pressure_level: "medium"
  player_proximity_response: "al acercarse, el sonido puede acompasarse mal, detenerse como si escuchara, o intentar una frase que no llega a nacer limpia"
  frame_reactivity: "apoyarse, tocar o hablar cerca del marco puede devolver calor de pared, vibración torácica o una pausa que se vuelve insoportable"

creature_activity:
  dominant_function: "corazón / pecho / voz emocional / súplica"
  secondary_function: "pulmones si el balcón quedó peor; humedad residual si C03 sigue heredado; ritmo cortado si el editor contaminó el clima"
  temperament_bias: "doliente tendiendo a suplicante"
  manifestation_rules:
    - "nada plenamente visible"
    - "debe sentirse como una emoción aprendida por un cuerpo que no tiene todavía el idioma ni la forma correctos"
    - "si dominó el dormitorio, el retorno debe sugerir pecho, latido, cama, espera o herida sentida"
    - "si dominó el balcón, el retorno debe añadir aire, llamada hacia fuera o exhalación expuesta"
    - "si la pareja/ex fue dejada en visto o esquivada, la súplica pesa más"
    - "si se abrió la herida y se respondió con verdad, el retorno puede ser menos rencoroso y más tristemente íntimo"
    - "si el editor apareció cortando el día, puede colarse un ritmo feo de utilidad o vergüenza dentro del pecho"

apartment_events:
  - zone: "Dormitorio"
    condition: "si quedó como foco principal"
    event: "la cama parece más hundida, más habitada o más reciente de lo que debería; el móvil o un objeto íntimo pesan demasiado en la oscuridad"
    interpretation_space: "intimidad contaminada, no fantasma romántico"
  - zone: "Balcón"
    condition: "si quedó como foco principal"
    event: "el cristal, la puerta o el aire del balcón parecen guardar una exhalación que no coincide del todo con el exterior"
    interpretation_space: "el afuera repite el adentro sin aclararlo"
  - zone: "Pasillo"
    event: "caminar hacia la puerta se siente como ir hacia el pecho del piso y no hacia una habitación cualquiera"
    interpretation_space: "órgano doméstico, no truco de mansión encantada"
  - zone: "Salón"
    condition: "si la TV o el editor quedaron muy activos"
    event: "una línea tardía de TV, un brillo residual o un aparato que tarda demasiado en callarse"
    interpretation_space: "lo funcional y lo sentimental empiezan a mezclarse mal"

night_actions_available:
  - action: "acercarse a la puerta y escuchar el latido o la súplica"
    cost: "sube threat_intimacy, baja estabilidad y vuelve la relación con la criatura mucho más personal"
    possible_outcome: "el jugador confirma que la puerta ya no sólo alberga una función, sino una forma de padecer"
  - action: "revisar dormitorio o balcón y enfrentarse al foco íntimo"
    cost: "obliga a mirar el residuo emocional del día de frente"
    possible_outcome: "obtiene lectura más clara del origen del retorno nocturno"
  - action: "intervenir mínimamente el foco no contenido"
    cost: "llega tardísimo y sólo desplaza la textura de la noche"
    possible_outcome: "menos súplica directa, más latido; menos latido, más exhalación de balcón"
  - action: "hablarle a la puerta o quedarse demasiado tiempo junto al marco"
    cost: "aumenta door_pressure y amenaza con enseñar trato directo a la criatura"
    possible_outcome: "se siembra futura imitación emocional más clara"
  - action: "medicarse, dormirse o retirarse"
    cost: "recorta exposición pero refuerza avoidance o dependencia del corte"
    possible_outcome: "la noche se encoge sin quedar resuelta"

micro_containment_if_any:
  is_available: true
  action: "guardar el objeto íntimo, apartar el móvil, ventilar un minuto, cerrar o abrir el balcón con intención, estirar la sábana"
  cost: "es un gesto ridículo y doloroso; obliga a decidir si se toca el residuo o la puerta"
  effect: "amortigua una superficie del problema, pero no detiene el aprendizaje afectivo de la casa"

closure_options:
  sleep: "aceptar que el piso ya sabe guardar el afecto mal y retirarse con una pena demasiado concreta instalada"
  medication: "rebajar exposición a la noche a costa de dejar la herida sin lenguaje propio"
  stay_awake: "dejar que la escucha se convierta casi en acompañamiento mutuo y monstruoso"
  threshold_action: "tocar el marco, apoyar el pecho, quedarse quieto o hablar bajo hacia la madera"

persistence_out:
  relation_shift: "la pareja/ex deja de ser sólo contacto humano y pasa a formar parte de la gramática emocional del piso"
  zone_shift: "dormitorio o balcón pasan a foco íntimo contaminado de alta carga"
  tv_shift: "la suggestion sentimental queda preparada para volverse manipulación más clara"
  creature_shift: "la criatura gana corazón, pecho, voz emocional o súplica más legible"
  door_shift: "la puerta entra en una fase afectiva y torácica, no sólo orgánica"
  emotional_truth_learned: "lo íntimo no desaparece por aplazarlo: aprende a latir detrás de una puerta"
```

---

## 2. Notas de dirección

### 2.1. Regla de progreso
La noche 4 no debe ser “más grande” que la 3. Debe ser más doliente y más personal. El salto es de afecto deformado, no de decibelios.

### 2.2. Regla de lectura
El jugador debe salir de esta noche con la sensación de que la criatura ya no sólo aprende cuerpo, sino una forma muy mala y muy triste de querer, reclamar o pedir. Eso es más inquietante que un rugido, y bastante más miserable.

### 2.3. Regla anatómica
Si dominó el dormitorio, la puerta devuelve corazón, pecho, pausa, cama y voz herida. Si dominó el balcón, mete aire, llamada, exhalación y exposición. Si el baño heredado sigue cargado, lo íntimo se vuelve húmedo y más físico. Si el editor contaminó el clima, el pecho puede sonar medido, cortado o vergonzosamente útil.

### 2.4. Función emocional
La casa no sólo ha aprendido a respirar con el jugador. Ha aprendido a dolerse mal con él.

---

## 3. Persistencia recomendada hacia Ciclo 5

- La pareja/ex debe quedar plenamente posicionada como eco persistente de alta carga aunque el siguiente ciclo cambie de presión activa.
- La madre puede reaparecer como cuidado que entra todavía peor cuando el pecho ya está demasiado ocupado.
- El amigo debe poder funcionar como contraste casi obsceno frente a una noche sentimentalmente monstruosa.
- El editor queda listo para volver como cuchillo funcional en medio de otro tipo de presión.
- La puerta debe estar preparada para que el exterior del siguiente ciclo ya no sea sólo “fuera”, sino un espejo o una provocación para lo que late dentro.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **cuarta ficha real de noche** del proyecto. Cierra la lógica del ciclo donde la herida íntima se devuelve como corazón, pecho, voz emocional y súplica, sin convertir el horror en melodrama ornamental ni en espectáculo de feria.

La norma final del ciclo es sencilla:

**cuando el afecto no encuentra salida, busca caja torácica.**
