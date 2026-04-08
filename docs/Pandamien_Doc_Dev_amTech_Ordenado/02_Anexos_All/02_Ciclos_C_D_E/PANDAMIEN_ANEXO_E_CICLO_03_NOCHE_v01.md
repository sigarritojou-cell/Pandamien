# PANDAMIEN — ANEXO E
## Ficha real de noche — Ciclo 3: El cuerpo entra en juego
### Derivada del GDD Maestro v03, del Anexo M v01, del Anexo I v01, de la ficha de día C03 y de los pilotos nocturnos de los ciclos 1 y 2

---

## 0. Intención de la noche

La tercera noche no debe “subir el volumen” de manera torpe. Debe cambiar la naturaleza de la cercanía. Si en la primera noche la casa respondió y en la segunda aprendió mejor a devolver, en la tercera empieza a respirar contigo de forma obscena. El monstruo sigue sin exhibirse, pero la puerta ya no parece sólo una máquina de ruidos. Parece albergar un cuerpo que ha empezado a entender el aire, la humedad, el pecho y la intimidad del descanso.

La función dramática de esta noche es:

- traducir la deuda corporal del día en una presencia más íntima y más orgánica,
- desplazar la puerta desde la articulación defectuosa hacia la respiración y el cuerpo blando,
- dejar claro que atender o no atender el cuerpo cambia la textura del horror,
- llevar la TV a suggestion clínica o tranquilizadora,
- y cerrar el ciclo con una verdad incómoda: el apartamento no sólo escucha lo que dices; escucha cómo respiras.

---

## 1. Ficha oficial

```yaml
cycle_id: "C03"
cycle_title: "El cuerpo entra en juego"
night_theme: "la casa ya sabe algo de tu aire"

inherited_from_day:
  unresolved_relation: "cuidado rechazado o aceptado a medias con Madre; editor como vergüenza de fondo; posible herida íntima activada por Pareja/Ex"
  unresolved_zone: "baño o dormitorio, según la contención fallida o incompleta"
  unresolved_choice: "se atendió el cuerpo demasiado tarde, se mintió sobre él o se sacrificó para seguir funcionando"
  tv_seed: "suggestion con tono clínico, tranquilizador o de descanso blando"

night_entry_state:
  apartment_tension_level: "medium"
  active_zones:
    - "pasillo"
    - "baño o dormitorio, según foco dominante"
    - "salón residual si el trabajo siguió empapándolo todo"
  tv_state: "suggestion tendiendo a clínico / calmante"
  stability_bias: "la realidad aún es legible, pero la sensación de cuerpo observado o acompañado sin permiso se vuelve difícil de racionalizar"

ambient_progression:
  phase_1: "al bajar la actividad, el piso parece más húmedo o más cargado de presencia física: tuberías, tejidos, cama, espejo, respiración propia, nevera al fondo"
  phase_2: "el pasillo absorbe mejor el silencio y la puerta atrancada ya no pesa sólo como objeto; pesa como caja torácica torpe o como pulmón mal cerrado"
  phase_3: "se produce un retorno más íntimo: respiración húmeda, exhalación irregular, roce de membrana, latido blando o pausa demasiado humana detrás de la madera"

relational_return:
  main_echo_source: "Madre / cuerpo"
  secondary_echo_source: "Pareja/Ex o Editor, según historial del día"
  form: "door + apartment + bedroom"
  distortion_type: "cuidado convertido en respiración sin permiso, descanso transformado en vigilancia íntima o vergüenza funcional mezclada con fatiga corporal"
  emotional_effect: "el jugador entiende que la casa ha aprendido no sólo una voz o un ritmo, sino una forma de habitar el cuerpo"

door_behavior:
  material_state: "marco más húmedo, madera con cansancio orgánico, posible sombra de condensación o textura que parece sudor de pared"
  sound_bank_primary: "respiración irregular, exhalación pegada, roce de materia húmeda o latido torpe"
  sound_bank_secondary: "pequeño golpe de peso blando, tela o membrana, pausa afectiva rara si la intimidad fue activada"
  pressure_level: "medium"
  player_proximity_response: "al acercarse, el ritmo puede acompasarse mal con el jugador, cortarse de golpe o quedarse demasiado quieto, como si estuviera escuchando también"
  frame_reactivity: "tocar o acercar la mano al marco puede dar sensación térmica, vibración blanda o humedad más presente"

creature_activity:
  dominant_function: "piel / mucosa / pecho / respiración"
  secondary_function: "corazón temprano si dormitorio quedó peor; garganta residual si el trabajo siguió colonizando fondo"
  temperament_bias: "doliente tendiendo a suplicante o íntimo"
  manifestation_rules:
    - "nada plenamente visible"
    - "debe sentirse como un cuerpo que no domina aún su anatomía, pero ya no suena abstracto"
    - "si dominó el baño, el retorno debe oler a humedad, mucosa, piel o respiración pegada"
    - "si dominó el dormitorio, el retorno debe sugerir pecho, latido o presencia tumbada / cansada"
    - "si Pareja/Ex quedó activa, puede colarse una pausa afectiva que vuelva la noche más íntima"
    - "si Editor quedó muy mal, la respiración puede incluir un ritmo cortado, como de tarea interrumpida o esfuerzo que no descansa"

apartment_events:
  - zone: "Baño"
    condition: "si quedó como foco principal"
    event: "el espejo devuelve una presencia de cansancio más densa; la humedad tarda demasiado en disiparse; una gota o junta parece tener ritmo"
    interpretation_space: "realismo sucio antes que sobrenatural frontal"
  - zone: "Dormitorio"
    condition: "si quedó como foco principal o si Pareja/Ex se activó"
    event: "la cama parece más hundida, el aire menos renovado, la tela más consciente del cuerpo"
    interpretation_space: "la intimidad del descanso se vuelve escenario"
  - zone: "Pasillo"
    event: "el trayecto a la puerta parece más estrecho y más respirado; caminarlo da la impresión de entrar en el pecho del piso"
    interpretation_space: "no casa encantada; órgano doméstico"
  - zone: "Salón"
    condition: "si el editor siguió vivo como deuda fuerte"
    event: "portátil o TV dejan un residuo funcional tardío que ahora suena más cruel por contraste con el agotamiento corporal"
    interpretation_space: "la utilidad no desaparece; se incrusta"

night_actions_available:
  - action: "acercarse a la puerta y escuchar la respiración"
    cost: "sube threat_intimacy, baja estabilidad y fija una relación mucho más íntima con la criatura"
    possible_outcome: "el jugador confirma que la puerta ya no sólo articula; también acompasa mal la vida del apartamento"
  - action: "pasar por baño o dormitorio y revisar el foco corporal"
    cost: "obliga a mirar el residuo del día de frente"
    possible_outcome: "obtiene lectura más clara del origen del retorno nocturno"
  - action: "intervenir mínimamente en la zona no contenida"
    cost: "llega tardísimo y sólo desplaza una textura del horror a otra"
    possible_outcome: "menos humedad directa, más latido; o menos pecho, más roce de pasillo"
  - action: "medicarse o retirarse temprano"
    cost: "corta la exposición, sube avoidance o dependencia del corte"
    possible_outcome: "la noche se encoge, pero el cuerpo no queda resuelto"
  - action: "ignorar la puerta y acostarse"
    cost: "sube avoidance y permite crecimiento fuera de escena"
    possible_outcome: "el ciclo siguiente arranca con un cansancio menos neutro"

micro_containment_if_any:
  is_available: true
  action: "colgar la toalla, secar una gota, cambiar la sábana o ventilar unos minutos"
  cost: "es un gesto triste, tardío y parcial; obliga a elegir si tocar el residuo o la puerta"
  effect: "amortigua una superficie del problema, pero no detiene la noche; sólo modifica si vuelve más por humedad, por pecho o por latido"

closure_options:
  sleep: "aceptar que el piso ya ha interiorizado el cuerpo y retirarse con una intimidad insoportable instalada"
  medication: "recortar la exposición directa a la respiración de la puerta, reforzando el pacto de evitación"
  stay_awake: "dejar que escuchar se convierta casi en acompañamiento mutuo"
  threshold_action: "tocar el marco, apoyar la frente, hablar bajo o quedarse quieto demasiado tiempo junto a la madera"

persistence_out:
  relation_shift: "Madre deja de ser sólo voz externa de cuidado; su lógica corporal ya respira dentro del piso"
  zone_shift: "baño o dormitorio pasan de degradados a focos muy personales"
  tv_shift: "suggestion clínica queda consolidada"
  creature_shift: "la criatura gana organicidad íntima: piel, respiración, pecho o latido temprano"
  door_shift: "la puerta entra en una fase más corporal y menos puramente sonora"
  emotional_truth_learned: "lo que no se atiende del cuerpo no desaparece: cambia de habitación y aprende a respirar"
```

---

## 2. Notas de dirección

### 2.1. Regla de progreso
La noche 3 no debe ser más ruidosa que la 2. Debe ser más cercana. El salto no es de volumen; es de intimidad.

### 2.2. Regla de lectura
El jugador debe salir de esta noche pensando que el piso ha dejado de responder a decisiones abstractas y ha empezado a responder al cuerpo mismo: su cansancio, su humedad, su aire y su necesidad de corte.

### 2.3. Regla anatómica
Si dominó el baño, la puerta devuelve humedad, mucosa y respiración. Si dominó el dormitorio, devuelve pecho, latido o presencia tumbada. Si la pareja/ex entró con fuerza, la pausa afectiva se mezcla con lo corporal. Si el editor siguió muy vivo, la respiración puede sonar trabajosa, cortada o medida.

### 2.4. Función emocional
La casa no sólo aprende lenguaje. Aprende intimidad fisiológica. Y eso da más asco y más pena a la vez.

---

## 3. Persistencia recomendada hacia Ciclo 4

- La pareja/ex queda perfectamente posicionada para tomar más peso en el siguiente ciclo si se ha mezclado con dormitorio, balcón o descanso.
- La madre debe quedar menos episódica y más interiorizada: ya no llama sólo desde fuera, ya está en la gramática del cuerpo del piso.
- El editor no desaparece, pero se hunde en vergüenza interna y deuda somatizada.
- El amigo puede reaparecer como alivio casi obsceno por contraste con una noche demasiado íntima.
- La puerta entra en una fase donde el monstruo ya no sólo ensaya funciones: empieza a parecer un cuerpo desgraciado.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **tercera ficha real de noche** del proyecto. Demuestra que PANDAMIEN puede volver más íntimo el horror sin inflarlo, manteniendo el principio central: la criatura no salta a escena, se aprende desde el residuo.
