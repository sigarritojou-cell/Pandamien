# PANDAMIEN — ANEXO E
## Ficha real de noche — Ciclo 5: El exterior se pega al piso
### Derivada del GDD Maestro v03, del Anexo M v01, del Anexo I v01, de la ficha de día C05 y de los pilotos nocturnos de los ciclos 1–4

---

## 0. Intención de la noche

La quinta noche no debe convertirse en “evento de pasillo” ni en casa encantada con vecino demoníaco. El progreso correcto es otro: si en C03 la puerta respiraba y en C04 dolía, en C05 **mira**. No hace falta mostrar un ojo. Basta con que el jugador deje de sentir el pasillo como un simple trayecto y empiece a sentirlo como una línea de visión.

La función dramática de esta noche es:

- traducir la presión del umbral en una presencia más orientada y consciente,
- hacer que puerta atrancada, puerta principal, mirilla y ventana parezcan formar un único sistema respiratorio-ocular del piso,
- confirmar que lo exterior no trae verdad limpia, sino dirección, foco y vigilancia,
- llevar la TV a suggestion editorial claramente torcida o a manipulación blanda,
- y cerrar el ciclo con una verdad nueva: la casa no sólo te devuelve; **te enfoca**.

---

## 1. Ficha oficial

```yaml
cycle_id: "C05"
cycle_title: "El exterior se pega al piso"
night_theme: "la casa ya sabe por dónde mirarte"

inherited_from_day:
  unresolved_relation: "umbral no resuelto; posible deadline secundaria del Editor; inquietud de Madre; eco íntimo de Pareja/Ex desde balcón o ventana"
  unresolved_zone: "entrada/pasillo o ventana/balcón, según la contención fallida o desplazada"
  unresolved_choice: "se miró demasiado sin actuar, se ignoró el borde o se selló un frente dejando el otro libre"
  tv_seed: "suggestion editorial sobre vigilancia, seguridad, contagio o ruido"

night_entry_state:
  apartment_tension_level: "medium_high"
  active_zones:
    - "pasillo"
    - "entrada"
    - "ventana o balcón, según foco dominante"
    - "salón residual si la TV o el editor siguieron activos"
  tv_state: "suggestion avanzada tendiendo a manipulación blanda"
  stability_bias: "la realidad aún es legible, pero el jugador ya no puede separar del todo mirar de ser mirado"

ambient_progression:
  phase_1: "al bajar el ruido del día, el rellano, el patio y las luces vecinas parecen demasiado sincronizados con la respiración del piso"
  phase_2: "el pasillo se siente más largo y más dirigido; la puerta principal y la atrancada parecen compartir atención en vez de mero peso"
  phase_3: "se produce un retorno orientado: silencio expectante, roce que se detiene al ser escuchado, respiración de rellano, golpe mínimo con cálculo o pausa que parece mirada"

relational_return:
  main_echo_source: "Exterioridad / umbral"
  secondary_echo_source: "Editor o Pareja/Ex, según historial del día"
  form: "door + entry + hallway + window"
  distortion_type: "vigilancia exterior convertida en orientación consciente, mirada sin ojo explícito o atención que se organiza dentro del piso"
  emotional_effect: "el jugador entiende que la casa ya no sólo reacciona a lo que deja pudrir: también aprende dónde apuntar"

door_behavior:
  material_state: "marco con humedad más vertical, madera menos blanda y más tensa, sensación de dirección en la presión"
  sound_bank_primary: "silencio demasiado atento, roce cortado, respiración de rellano, pequeño golpe con timing preciso"
  sound_bank_secondary: "arrastre mínimo, pausa larga, vibración puntual cerca del marco o rendija"
  pressure_level: "medium"
  player_proximity_response: "al acercarse, el retorno puede detenerse justo antes de ser localizable, como si la criatura estuviera corrigiendo su orientación"
  frame_reactivity: "mirilla y marco principal contagian la lectura del pasillo; tocar un borde puede hacer más presente el otro"

creature_activity:
  dominant_function: "ojos / atención dirigida / orientación"
  secondary_function: "piernas tempranas o inmovilidad consciente; pecho residual si C04 sigue muy vivo"
  temperament_bias: "rencoroso tendiendo a imitativo, o vigilante doliente según historial"
  manifestation_rules:
    - "nada visible del todo"
    - "debe sentirse como una presencia que sabe ya colocar su atención, aunque aún no domine el cuerpo completo"
    - "si dominó entrada/pasillo, el retorno debe ser de mirada sin ojo, trayecto observado y pausa dirigida"
    - "si dominó ventana/balcón, debe haber aire expectante, exposición y sensación de foco desde fuera-dentro"
    - "si el editor reapareció fuerte, la orientación puede sentirse evaluativa, casi de medición"
    - "si la pareja/ex quedó activa, la mirada puede sonar más íntima y menos puramente paranoica"

apartment_events:
  - zone: "Entrada"
    condition: "si quedó como foco principal"
    event: "el felpudo, la rendija o el pomo parecen tener una presencia demasiado puntual; no cambia mucho materialmente, pero cambia cómo se lee"
    interpretation_space: "cotidiano contaminado antes que fenómeno directo"
  - zone: "Pasillo"
    event: "caminarlo da la sensación de entrar en una línea de visión; la oscuridad no tapa, encuadra"
    interpretation_space: "la tensión nace de orientación, no de volumen"
  - zone: "Ventana"
    condition: "si quedó como foco principal"
    event: "luz vecina, cortina o figura parcial parecen responder al momento equivocado"
    interpretation_space: "nunca prueba limpia; siempre provocación"
  - zone: "Balcón"
    condition: "si Pareja/Ex o exterioridad se mezclaron con fuerza"
    event: "el aire no despeja; deja la impresión de una atención suspendida sobre la barandilla"
    interpretation_space: "exposición como intimidad enferma"
  - zone: "Salón"
    condition: "si TV/editor siguen fuertes"
    event: "la TV deja una frase tardía sobre seguridad o convivencia, o el portátil suena a sistema pendiente justo cuando el pasillo pide otra cosa"
    interpretation_space: "lo funcional y lo paranoico ya conviven"

night_actions_available:
  - action: "acercarse a la puerta principal o a la mirilla"
    cost: "sube threat_intimacy y orienta mejor a la criatura hacia el jugador"
    possible_outcome: "obtiene confirmación parcial de que el umbral ya no es neutro, pero no verdad objetiva del exterior"
  - action: "cruzar el pasillo hacia la puerta atrancada y escuchar"
    cost: "convierte el trayecto en vínculo; baja estabilidad"
    possible_outcome: "la puerta devuelve atención más que sonido bruto"
  - action: "asomarse a ventana o balcón"
    cost: "exposición emocional y perceptiva; puede reactivar eco de Pareja/Ex o sensación de vida ajena insoportable"
    possible_outcome: "obtiene un patrón exterior ambiguo que empeora la lectura del interior"
  - action: "intervenir mínimamente en entrada o ventana"
    cost: "llega tarde y sólo mueve el borde infectado"
    possible_outcome: "menos presión en un umbral, más presencia en el otro"
  - action: "ignorar todos los umbrales y retirarse"
    cost: "sube avoidance y permite que la orientación de la criatura se asiente sin mirada del jugador"
    possible_outcome: "el siguiente ciclo arranca con más mezcla y menos inocencia espacial"

micro_containment_if_any:
  is_available: true
  action: "retirar paquete/bolsa, limpiar felpudo o cerrar/ajustar ventana/cortina"
  cost: "es un gesto tardío, pequeño y casi supersticioso; obliga a elegir qué borde tocar"
  effect: "disminuye un eco directo del umbral elegido, pero desplaza la atención de la noche hacia el otro frente o hacia el pasillo"

closure_options:
  sleep: "aceptar que el piso ya ha aprendido a orientarse hacia ti y retirarse con la sensación de haber sido enfocado"
  medication: "recortar la exposición directa a los umbrales a costa de reforzar evitación y corte perceptivo"
  stay_awake: "dejar que el pasillo, la mirilla y la puerta se conviertan en un triángulo de escucha"
  threshold_action: "mirar por la mirilla, tocar el pomo, apoyar la mano en el marco o quedarse quieto en mitad del pasillo"

persistence_out:
  relation_shift: "el exterior deja de ser rumor y pasa a sistema activo dentro del lenguaje del piso"
  zone_shift: "entrada/pasillo o ventana/balcón pasan de degradados a focos umbral claramente enfermos"
  tv_shift: "suggestion editorial queda lista para contaminarse hacia manipulación abierta"
  creature_shift: "la criatura gana orientación, atención dirigida y capacidad de esperar"
  door_shift: "la puerta ya no sólo devuelve cuerpo; devuelve foco"
  emotional_truth_learned: "cuando no sabes si algo te mira, el piso termina aprendiendo a hacerlo por ello"
```

---

## 2. Notas de dirección

### 2.1. Regla de progreso
La noche 5 no debe sonar más fuerte que la 4. Debe sonar más precisa espacialmente. El salto no es de monstruosidad, sino de **dirección**.

### 2.2. Regla de lectura
El jugador debe salir de esta noche pensando que el apartamento ya ha incorporado el umbral como órgano. El borde no separa; enfoca.

### 2.3. Regla anatómica
Si dominó entrada/pasillo, la puerta devuelve mirada, orientación, silencio atento y trayectoria. Si dominó ventana/balcón, devuelve aire expuesto, foco a distancia y sensación de marco. Si el editor entró fuerte, la mirada mide. Si la pareja/ex contaminó, la exposición se vuelve íntima.

### 2.4. Función emocional
La casa no sólo respira contigo ni sólo se duele contigo. Empieza a **seguirte con atención**. Y eso hace el encierro más estrecho.

---

## 3. Persistencia recomendada hacia Ciclo 6

- La TV queda perfectamente posicionada para apropiarse de vigilancia, vecindad, intimidad y utilidad en una misma pasta verbal.
- Madre y amigo deben poder reaparecer ya contaminados por lectura exterior, no sólo por sus troncos originales.
- El editor puede volver como fórmula incrustada en el clima de control y medición.
- La pareja/ex queda lista para reaparecer como frase íntima robada en balcón, ventana o puerta.
- La puerta entra en fase de criatura que no sólo siente ni mira: empieza a **entender sintaxis de atención**, base necesaria para la colonización semántica de C06.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **quinta ficha real de noche** del proyecto. Cierra la lógica del ciclo donde el umbral deja de ser borde y pasa a ser órgano de atención del apartamento.

La norma final del ciclo es sencilla:

**cuando el afuera no puede entrar limpio, se queda en el marco y aprende a mirar desde allí.**
