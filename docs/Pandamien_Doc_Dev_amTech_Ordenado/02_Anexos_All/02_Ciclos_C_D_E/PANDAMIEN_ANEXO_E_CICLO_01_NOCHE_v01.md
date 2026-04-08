# PANDAMIEN — ANEXO E
## Ficha real de noche — Ciclo 1: Reconocimiento
### Derivada del GDD Maestro v03 y de la ficha de día C01

---

## 0. Intención de la noche

La primera noche no debe “destapar el horror” como un telón de feria. Debe devolver, de manera vergonzosamente pequeña, el residuo del día. La casa baja de volumen social y sube de presencia. El jugador ya no está ocupado gestionando mensajes; ahora escucha el piso.

La función dramática de esta noche es:

- traducir una deuda diurna en gesto material,
- dejar claro que la puerta atrancada no es decorado,
- insinuar que la criatura no aparece: aprende a existir,
- y cerrar el ciclo con una prueba mínima pero inolvidable de crecimiento.

---

## 1. Ficha oficial

```yaml
cycle_id: "C01"
cycle_title: "Reconocimiento"
night_theme: "algo pequeño ha empezado"

inherited_from_day:
  unresolved_relation: "deuda suave con editor o madre, según lo no sostenido"
  unresolved_zone: "salón o baño"
  unresolved_choice: "se eligió atender una presión y dejar otra fermentando"
  tv_seed: "comfort con frases de normalización y descanso"

night_entry_state:
  apartment_tension_level: "low to medium"
  active_zones:
    - "pasillo"
    - "salón o baño, según contaminación no contenida"
  tv_state: "comfort contaminándose hacia suggestion"
  stability_bias: "todavía funcional, pero más porosa al silencio del apartamento"

ambient_progression:
  phase_1: "la casa parece ordinaria pero demasiado audible: nevera, tuberías, roce de tejidos, televisión bajita o apagada del todo"
  phase_2: "el pasillo gana espesor; una zona del piso reclama mirada y la puerta atrancada pesa sin llamar la atención de forma frontal"
  phase_3: "se produce el primer retorno mínimo: gemido, golpe torpe o fricción desde la puerta"

relational_return:
  main_echo_source: "Editor o Madre"
  form: "door"
  distortion_type: "presión funcional convertida en sonido corporal o cuidado convertido en respiración húmeda"
  emotional_effect: "el jugador entiende que el apartamento no olvida del todo lo que ha dejado sin cerrar"

door_behavior:
  material_state: "marco apenas más hinchado, humedad insinuada, madera que parece ceder por cansancio más que por fuerza monstruosa"
  sound_bank_primary: "gemido breve o golpe torpe"
  sound_bank_secondary: "roce pequeño, crujido húmedo o una respiración casi imaginaria si el baño quedó peor"
  pressure_level: "incipient"
  player_proximity_response: "al acercarse, el sonido cesa o cambia de textura; no hay confirmación limpia, sólo sospecha muy concreta"

creature_activity:
  dominant_function: "voz latente o masa informe con respiración mínima"
  temperament_bias: "neutro tendiendo a doliente"
  manifestation_rules:
    - "nada coordinado ni espectacular"
    - "el sonido debe parecer el ensayo torpe de un cuerpo que todavía no sabe usarse"
    - "si el salón quedó peor, el retorno debe sugerir garganta/voz"
    - "si el baño quedó peor, debe sugerir humedad/pecho/respiración"

apartment_events:
  - zone: "Salón"
    event: "la TV emite una línea tardía, residual o ambigua, o refleja luz enfermiza un segundo de más"
    interpretation_space: "puede ser pura coincidencia o una continuidad demasiado íntima del discurso diurno"
  - zone: "Pasillo"
    event: "la oscuridad no es total, pero el tramo hacia la puerta parece más largo y absorbente"
    interpretation_space: "no debe sentirse sobrenatural obvio; debe sentirse como una percepción cansada con fundamento dudoso"

night_actions_available:
  - action: "acercarse a la puerta y escuchar"
    cost: "sube tensión, reduce distancia psicológica y compromete el cierre seguro de la noche"
    possible_outcome: "obtiene confirmación parcial de que ha sonado algo y deja sembrada la promesa"
  - action: "ignorar la puerta y cerrar la noche"
    cost: "sube avoidance y deja la sospecha sin elaborar"
    possible_outcome: "el jugador duerme o se retira con una verdad no mirada"

micro_containment_if_any:
  is_available: true
  action: "pequeña intervención menor en la zona no contenida durante el día: apartar el vaso, secar una gota, colgar la toalla"
  cost: "llega tarde, es parcial y puede hacer que el retorno de la puerta se desplace en vez de desaparecer"
  effect: "amortigua textura de una zona pero no cancela el primer signo tras la puerta"

closure_options:
  sleep: "aceptar que el piso guarda algo sin nombre y pasar al siguiente día con una incomodidad instalada"
  medication: "recortar algo de exposición, pero reforzar evitación o dependencia del corte"
  stay_awake: "prolongar la escucha y aumentar la intimidad con la puerta"
  threshold_action: "mirar el pasillo una vez más, tocar el marco o hablarle a la nada sin respuesta clara"

persistence_out:
  relation_shift: "la deuda ignorada no explota todavía, pero ya tiene eco sensible"
  zone_shift: "la zona no contenida pasa de descuidada a degradada o queda marcada como foco recurrente"
  tv_shift: "comfort queda levemente infectado por suggestion"
  creature_shift: "se registra el primer crecimiento audible; la criatura deja de ser hipótesis abstracta"
  door_shift: "la puerta gana peso dramático real"
  emotional_truth_learned: "la casa devuelve aunque sea en pequeño; nada ignorado desaparece del todo"
```

---

## 2. Notas de dirección

### 2.1. Regla de tamaño
La noche debe cerrar con algo pequeño. Nada de festival. El primer sonido tras la puerta tiene que ser casi miserable: un gemido torpe, una fricción, un golpe sin destreza. Eso lo hace más íntimo y más insoportable.

### 2.2. Regla de lectura
El jugador debe poder dudar un instante, pero no tanto como para que el evento se vuelva trivial. La duda no es “¿ha pasado algo?” sino “¿de verdad acaba de pasar tan poco y aun así me ha cambiado la casa?”

### 2.3. Regla anatómica
Si el salón fue sacrificado, la noche inclina hacia voz. Si el baño fue sacrificado, inclina hacia respiración húmeda. La ficha ya nace conectada al sistema anatómico del GDD.

### 2.4. Función emocional
El piso no ataca todavía. Responde.

---

## 3. Persistencia recomendada hacia Ciclo 2

- El editor queda mejor posicionado como presión activa de la siguiente jornada si fue evitado.
- La madre deja un poso más corporal si fue ignorada o respondida con culpa.
- El amigo puede reaparecer como falsa normalidad al día siguiente.
- La pareja/ex sigue ausente, pero el dormitorio ya no es completamente inocente.
- La puerta entra oficialmente en la gramática del juego como promesa física cumplida en miniatura.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **primera ficha real de noche** del proyecto. Demuestra que el sistema ya puede pasar del principio abstracto al retorno jugable sin inflar el tono ni volver literal demasiado pronto la criatura.
