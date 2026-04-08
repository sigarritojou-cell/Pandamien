# PANDAMIEN — ANEXO E
## Ficha real de noche — Ciclo 2: Primera deuda clara
### Derivada del GDD Maestro v03, del Anexo M v01, de la ficha de día C02 y del piloto nocturno del Ciclo 1

---

## 0. Intención de la noche

La segunda noche ya no puede apoyarse sólo en la sorpresa mínima de “algo ha sonado”. Esa promesa ya fue pagada en miniatura al final del primer ciclo. Ahora toca una variación más precisa: la puerta no sólo responde, empieza a responder mejor.

No debe haber espectáculo todavía. Pero sí un salto cualitativo pequeño y jodido: el ruido ya no parece sólo materia torpe, sino una tentativa defectuosa de función. Si el día estuvo dominado por deuda laboral, la noche debe insinuar garganta, sílaba, golpe seco o ritmo cortante. Si el jugador protegió el salón pero dejó podrir cocina u otra zona, la respuesta debe desplazarse sin desaparecer.

La función dramática de esta noche es:

- convertir la deuda del día en un retorno más legible,
- confirmar que la puerta aprende con el historial,
- contaminar la frontera entre ruido funcional y presencia intencional,
- dejar que la TV dé un paso hacia suggestion,
- y cerrar el ciclo con una criatura todavía pequeña pero ya menos abstracta.

---

## 1. Ficha oficial

```yaml
cycle_id: "C02"
cycle_title: "Primera deuda clara"
night_theme: "la casa ya articula mejor lo que devuelve"

inherited_from_day:
  unresolved_relation: "deuda clara con editor, o cruce entre editor y pareja/ex si la intimidad fue tocada"
  unresolved_zone: "salón o cocina, según foco no contenido"
  unresolved_choice: "se protegió una cosa dejando fermentar otra, o se sostuvo la apariencia de control sin resolver nada"
  tv_seed: "comfort contaminado hacia suggestion con tono de rutina funcional"

night_entry_state:
  apartment_tension_level: "medium"
  active_zones:
    - "pasillo"
    - "salón o cocina, según contaminación no contenida"
    - "dormitorio como eco secundario si la pareja/ex dejó herida activa"
  tv_state: "suggestion inicial"
  stability_bias: "la realidad sigue siendo legible, pero el jugador ya no concede inocencia automática a los ruidos del piso"

ambient_progression:
  phase_1: "la casa baja de estímulo, pero el silencio ya no es neutro; la nevera, el roce del cableado, el portátil cerrado o la TV en residual tienen demasiado contorno"
  phase_2: "el salón conserva una presión muda y el pasillo parece más consciente del trayecto; la puerta atrancada pesa aunque no emita de inmediato"
  phase_3: "se produce un retorno más definido: golpe seco, sílaba mínima, exhalación rara o roce con ritmo funcional fallido"

relational_return:
  main_echo_source: "Editor"
  secondary_echo_source: "Pareja/Ex o Madre, según historial del día"
  form: "door + apartment"
  distortion_type: "presión de rendimiento convertida en garganta defectuosa, intento de llamada corporal o mandato vuelto materia"
  emotional_effect: "el jugador entiende que no sólo ha dejado algo sin hacer; ha enseñado a la casa una forma de hablar"

door_behavior:
  material_state: "marco más húmedo o más tenso que en C01; la madera parece menos cansada y más presionada desde dentro"
  sound_bank_primary: "golpe seco con intención, sílaba rota o respiración cortada con ritmo de frase fallida"
  sound_bank_secondary: "zumbido sordo, roce de masa contra marco o pequeño arrastre si el pasillo ha ganado peso"
  pressure_level: "low_to_medium"
  player_proximity_response: "al acercarse, el sonido puede cortar justo antes de volverse comprensible, o repetir sólo un fragmento demasiado torpe para ser mensaje limpio"

creature_activity:
  dominant_function: "garganta / voz latente más articulada o función desplazada según foco alternativo"
  secondary_function: "hambre difusa si cocina quedó peor; respiración húmeda si baño heredado sigue cargado"
  temperament_bias: "neutro tendiendo a imitativo o doliente"
  manifestation_rules:
    - "nada plenamente coordinado"
    - "debe sentirse como un cuerpo intentando usar un mecanismo que todavía no domina"
    - "si el salón quedó peor, el retorno debe oler a voz, trabajo, sílaba o frase abortada"
    - "si la cocina quedó peor, el retorno debe inclinarse a gorgoteo, bilis o masticación leve"
    - "si la pareja/ex se activó, puede colarse una cadencia emocional en la respiración o en la pausa del sonido"

apartment_events:
  - zone: "Salón"
    event: "la TV o el portátil parecen emitir un residuo de presencia funcional: brillo que tarda en morir, sonido mínimo de sistema, frase tardía demasiado oportunista"
    interpretation_space: "puede ser aparato residual o continuidad perversa del tono del editor"
  - zone: "Pasillo"
    event: "el trayecto hacia la puerta parece más largo, más estrecho o más absorbente que en C01"
    interpretation_space: "no sobrenatural obvio; percepción cansada con fundamento inquietante"
  - zone: "Cocina"
    condition: "si quedó como foco principal"
    event: "olor mínimo agrio, goteo más presente o silencio de nevera demasiado atento"
    interpretation_space: "la casa parece digerir mal"
  - zone: "Dormitorio"
    condition: "si la pareja/ex se activó"
    event: "el móvil, una foto o la cama arrastran una quietud cargada; no domina la noche, pero la vuelve más íntima"
    interpretation_space: "lo íntimo ya tiene eco aunque no mande"

night_actions_available:
  - action: "acercarse a la puerta y escuchar"
    cost: "sube tensión y amenaza con fijar mejor la intimidad con la criatura"
    possible_outcome: "el jugador confirma un patrón más articulado que en C01 sin obtener lenguaje limpio"
  - action: "revisar salón/portátil/TV"
    cost: "puede reforzar suggestion y retrasar la escucha directa"
    possible_outcome: "obtiene contaminación cruzada entre discurso funcional y presencia"
  - action: "intervenir mínimamente la zona no contenida"
    cost: "llega tarde y mueve el residuo, no lo anula"
    possible_outcome: "desplaza la textura del retorno, quizá de voz a hambre o de golpe a exhalación"
  - action: "ignorar la puerta y cerrar la noche"
    cost: "sube avoidance y deja que la criatura gane terreno sin mirada"
    possible_outcome: "la mañana siguiente arranca con más sospecha incorporada"

micro_containment_if_any:
  is_available: true
  action: "cerrar portátil, retirar taza/plato, vaciar pequeño resto de cocina o secar un detalle heredado"
  cost: "es demasiado poco y demasiado tarde; obliga a elegir entre escuchar o seguir fingiendo gestión"
  effect: "amortigua una superficie del piso pero no cancela la evolución de la puerta"

closure_options:
  sleep: "aceptar que la deuda del día ya tiene eco material y pasar al ciclo siguiente con cansancio menos inocente"
  medication: "recortar exposición directa a la noche, pero reforzar corte y evitación"
  stay_awake: "dejar que la escucha se vuelva relación, no sólo evento"
  threshold_action: "tocar el marco, hablarle al silencio, quedarse demasiado tiempo en el pasillo o revisar la rendija sin obtener premio claro"

persistence_out:
  relation_shift: "el editor deja de ser sólo personaje funcional y pasa a integrarse en la gramática del piso"
  zone_shift: "el salón o la cocina pasan de degradados a focos más característicos"
  tv_shift: "suggestion queda oficialmente activa"
  creature_shift: "la criatura registra una primera mejora en capacidad expresiva o de digestión, según el foco dominante"
  door_shift: "la puerta ya no sólo pesa; ya devuelve patrones"
  emotional_truth_learned: "lo dejado sin resolver no vuelve igual; vuelve aprendido"
```

---

## 2. Notas de dirección

### 2.1. Regla de progreso
La noche 2 no debe ser “más grande”; debe ser más precisa. El horror mejora su caligrafía, no su volumen.

### 2.2. Regla de lectura
El jugador no debe preguntarse sólo si ha oído algo, sino qué demonios acaba de aprender ese algo de su día. La clave es pasar de la pura sospecha a la sospecha con forma.

### 2.3. Regla anatómica
Si el salón fue sacrificado, la puerta se inclina hacia voz, sílaba, golpe cortante o pseudo llamada. Si la cocina fue sacrificada, aparece digestión, bilis o hambre pobre. Si persiste el baño, humedad. Si se activó ex/pareja, entra una pausa afectiva rara.

### 2.4. Función emocional
La casa no revela un monstruo. Revela aprendizaje. Eso es peor.

---

## 3. Persistencia recomendada hacia Ciclo 3

- La madre queda mejor posicionada para ganar presión activa en el siguiente ciclo si el cuerpo fue postergado frente al trabajo.
- El editor sigue vivo, pero debería empezar a mezclarse mejor con vergüenza interna y no presentarse sólo como evento externo.
- La pareja/ex debe quedar oficialmente sembrada si apareció en el día, aunque todavía no tome el control.
- El amigo puede reaparecer como falsa normalidad al día siguiente, precisamente para tensar por contraste el cuerpo ya cansado.
- La puerta entra en fase donde la articulación defectuosa ya es canon jugable, no sólo intuición literaria.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **segunda ficha real de noche** del proyecto. Demuestra que la escalada puede hacerse por precisión, cadencia y contaminación cruzada, sin romper la intimidad ni adelantar de forma torpe la criatura.
