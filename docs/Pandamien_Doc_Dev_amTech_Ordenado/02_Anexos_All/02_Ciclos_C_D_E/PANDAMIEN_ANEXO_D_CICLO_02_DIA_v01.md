# PANDAMIEN — ANEXO D
## Ficha real de día — Ciclo 2: Primera deuda clara
### Derivada del GDD Maestro v03, del Anexo M v01 y del piloto authored del Ciclo 1

---

## 0. Intención del día

El segundo día no debe sentirse como un capítulo nuevo, sino como una costura mal curada del anterior. La primera noche ya ha dejado una devolución mínima tras la puerta. No ha cambiado el mundo de forma espectacular, pero sí ha roto algo muy delicado: la tranquilidad con la que el protagonista podía llamar “normal” a los ruidos del piso.

Este día tiene que demostrar que la deuda no sólo existe: organiza el tiempo, ocupa el salón, contamina el lenguaje y vuelve más caro cualquier gesto de cuidado menor. La presión activa sigue siendo laboral, pero ya no entra como presentación; entra como repetición con filo.

La función dramática del día es:

- volver visible que el trabajo coloniza el espacio,
- instalar la primera deuda clara, ya no sólo insinuada,
- dejar que madre y amigo sigan vivos como ritmos del encierro,
- sembrar la primera irrupción leve de la pareja/ex,
- ofrecer una contención más tensa que la del ciclo 1,
- y preparar una noche en la que la puerta ya no suene “casi por casualidad”, sino como una respuesta más nítida al residuo acumulado.

---

## 1. Ficha oficial

```yaml
cycle_id: "C02"
cycle_title: "Primera deuda clara"
day_theme: "la presión ya ordena la casa"
act_phase: "Acto I — Rutina contaminada acercándose a colonización"

presence_base:
  - character: "Madre"
    format: "mensaje temprano + posible audio corto"
    tone: "práctico, cuidador, ligeramente intrusivo"
    purpose: "recordar cuerpo, sueño, comida y obediencia doméstica justo cuando el trabajo empieza a ocuparlo todo"
  - character: "Amigo"
    format: "mensajes dispersos durante el día + audio banal"
    tone: "ligero, algo insistente, cómico en apariencia"
    purpose: "ofrecer refugio blando y mantener viva la falsa normalidad"

pressure_active:
  primary_system_or_character: "Editor"
  format: "cadena de mensajes + llamada breve o intento de llamada + deadline explícita"
  urgency: "medium_high"
  decision_core: "responder comprometido, vender excusa, aplazar de forma torpe o esquivar para conservar una sensación falsa de control"

persistent_echoes:
  - source: "Pareja/Ex"
    form: "primer mensaje ambiguo, aparentemente menor, que entra cuando el día ya está cargado"
    effect: "abre una línea íntima que no domina el ciclo pero deja el dormitorio y el balcón menos inocentes"
  - source: "TV"
    form: "comfort contaminándose hacia suggestion"
    effect: "normaliza cansancio, aplazamiento y discurso de productividad blanda"
  - source: "Puerta atrancada"
    form: "recuerdo corporal de la noche anterior"
    effect: "el pasillo pesa un poco más aunque durante el día no ocurra nada frontal"

entry_state:
  player_body_state: "cansancio más pegado, sueño irregular, cuerpo funcional pero menos convincente, leve resaca emocional de la noche anterior"
  apartment_state_summary: "el salón se siente más ocupado por trabajo y por restos; el baño o la cocina conservan la huella del foco no contenido del ciclo 1"
  tv_state: "comfort infectándose hacia suggestion"
  weather_or_exterior_bias: "luz plana tirando a sucia; afuera sigue pareciendo real, pero el piso ya no filtra igual"

relational_beats:
  - beat_id: "C02_D_B01"
    trigger_window: "mañana temprana"
    source: "Madre"
    format: "mensaje + posible audio"
    short_description: "pregunta si ha desayunado, dormido o tomado algo; el cuidado ya no cae sobre vacío, cae sobre un jugador que viene de oír la casa"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "baño y dormitorio se vuelven a teñir de cuerpo y cumplimiento"
      - "si se ignora, la humedad y la respiración ganan terreno como retorno posible nocturno"
      - "si se responde directo, baja algo la culpa filial pero sube la sensación de obediencia vigilada"
  - beat_id: "C02_D_B02"
    trigger_window: "mañana media o al abrir portátil / sentarse en salón"
    source: "Editor"
    format: "mensaje seco + deadline concreta + llamada breve si no hay respuesta clara"
    short_description: "la tarea ya no es abstracta; ahora tiene forma, hora y tono evaluativo. El editor no grita, pero obliga a que el salón deje de ser salón"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "salón, mesa, portátil, reloj y pasillo se cargan de utilidad y vergüenza funcional"
      - "si se aplaza o se miente, suben deuda, presión verbal y probabilidad de retorno nocturno de garganta/sílaba/golpe seco"
      - "si se responde con disposición, se gana tregua laboral pero se refuerza la colonización del salón"
  - beat_id: "C02_D_B03"
    trigger_window: "mediodía o primera tarde"
    source: "Amigo"
    format: "audio banal + cadena breve de mensajes"
    short_description: "trae ruido social de encierro, una tontería compartida o una invitación absurda a videollamada que parece no pedir nada serio"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "cocina y salón ganan calor humano o pasividad, según el tono de la respuesta"
      - "si el jugador se refugia demasiado aquí, la TV queda mejor posicionada para justificar la inacción"
      - "si se corta con brusquedad, queda un pequeño residuo de irritación que puede reaparecer deformado"
  - beat_id: "C02_D_B04"
    trigger_window: "tarde media, idealmente tras saturación laboral"
    source: "Pareja/Ex"
    format: "primer mensaje ambiguo"
    short_description: "no exige escena grande; puede ser una pregunta pequeña, una referencia compartida o una aparición que parece casual y por eso hiere más"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "dormitorio y balcón ganan densidad íntima aunque la escena suceda mirando el móvil en otro lugar"
      - "si se abre y se deja en visto, suben silencio cargado y amenaza íntima futura"
      - "si se responde, la herida queda oficialmente activa para ciclos posteriores"

contamination:
  primary_focus:
    zone: "Salón"
    material_form: "mesa o sofá ocupados por restos de trabajo y descuido: taza reseca, vaso, ceniza, cables, libreta, portátil abierto demasiado tiempo, polvo de TV"
    emotional_cause: "presión laboral asumida a medias, autoengaño productivo, permanencia excesiva frente a la pantalla y dificultad para salir del bucle"
    escalation_if_ignored: "la zona empieza a generar latencia de garganta, sílaba defectuosa, golpe seco o zumbido con intención"
  secondary_focus:
    zone: "Cocina"
    material_form: "plato sin recoger, fregadero leve pero ya cargado, bolsa floja, olor mínimo que todavía podría racionalizarse"
    emotional_cause: "abandono funcional derivado del trabajo, hambre mal gestionada y refugio en rutinas blandas"
    escalation_if_ignored: "puede sembrar hambre, bilis o gorgoteo leve para la noche o los ciclos siguientes"
  inherited_focus_optional:
    zone: "Baño"
    condition: "si el foco secundario del ciclo 1 quedó peor"
    effect: "persiste como humedad de fondo, no domina el día pero condiciona la textura de la noche"

containment_offer:
  is_available: true
  action: "recoger y despejar el frente de trabajo en el salón o vaciar/ordenar el pequeño abandono de cocina"
  location: "salón o cocina, una sola intervención significativa"
  time_cost: "rompe la inercia del trabajo o la falsa pausa de la TV"
  relational_cost: "puede dejar al editor peor atendido o convertir al amigo/pareja-ex en deuda leve"
  systemic_benefit: "contiene la colonización más visible del ciclo y reduce la vía más directa de voz/hambre"
  systemic_risk: "si se protege el salón, la cocina fermenta; si se protege la cocina, el salón queda mejor preparado para que la puerta hable con lenguaje laboral"

tv_material:
  baseline_content: "magazine, tertulia tibia o programa de actualidad ligera con frases de normalización funcional"
  parasitic_line_pool:
    - "hay que seguir con la rutina"
    - "lo importante es no dejarse caer"
    - "todo el mundo va un poco tarde"

exterior_material:
  window_event: "vecino en una rutina repetida o gesto dudoso a distancia; nada sobrenatural, pero sí una sensación de tiempo detenido y vigilancia blanda"
  peephole_event: "ruido de pasos o bolsa fuera de campo; mirar no aclara nada, pero ya no parece del todo inocuo"
  balcony_event: "todavía no como escena central; puede existir como fantasía de aire o descompresión imposible"

day_closing_debt:
  unresolved_relation: "el editor debe quedar más pesado que en el ciclo 1; la pareja/ex puede quedar sembrada como herida leve y la madre puede mantenerse como culpa funcional"
  unresolved_zone: "salón o cocina, según la contención elegida"
  unresolved_truth: "el trabajo no sólo exige tiempo; convierte la casa en instrumento y al jugador en algo utilizable"

handoff_to_transition:
  light_shift_meaning: "la tarde cae sobre objetos demasiado usados, no sobre una escena nueva"
  sound_shift_meaning: "cuando baja el móvil, el salón sigue cargado y el pasillo vuelve a reclamar atención"
  first_door_hint: "la puerta atrancada ya no parece sólo húmeda o pesada; parece esperar a que el ruido del día se retire"
```

---

## 2. Notas de dirección

### 2.1. Tono
Este día debe sentirse un punto más apretado que el ciclo 1, pero no todavía abiertamente siniestro. La violencia del ciclo es laboral, doméstica y casi administrativa. Tiene que dar asco por reconocible.

### 2.2. Jerarquía jugable
El editor es la presión activa, sí, pero el día no puede volverse monográfico. Madre y amigo siguen vivos para sostener el realismo relacional, y la pareja/ex entra sólo como aguja fina, no como martillo sentimental.

### 2.3. Función de la pareja/ex
No debe secuestrar la escena. Su función es abrir una fisura nueva justo cuando el jugador ya estaba saturado con otra cosa. La clave no es intensidad, sino momento de entrada.

### 2.4. Contención
La contención del ciclo 2 ya tiene que sentirse más amarga que la del ciclo 1. No es “ordenar un vaso”. Es decidir si el salón deja de ser un altar de utilidad o si la cocina deja de ser el estómago olvidado de la casa.

### 2.5. Relación con el ciclo 1
El sonido de la primera noche no se comenta de forma explícita. Su efecto debe vivirse como resaca de atención: el protagonista cruza el pasillo o se sienta en el salón sabiendo ya que el piso podría devolver algo.

---

## 3. Salidas sistémicas recomendadas

### Si el jugador prioriza al editor
- gana una tregua relativa de deuda inmediata,
- pero el salón queda más colonizado por lógica de rendimiento,
- la TV puede volverse más funcional y cruel,
- y la criatura se orienta mejor hacia voz, mandíbula o presión coordinada.

### Si el jugador contiene el salón
- se frena la vía más directa de voz latente,
- pero la cocina gana riesgo de hambre, gorgoteo o bilis,
- y el trabajo se desplaza del espacio a la culpa interna.

### Si el jugador contiene la cocina
- reduce la degradación orgánica inmediata,
- pero deja que el salón quede más infectado de tiempo, utilidad y discurso,
- lo que fortalece la posibilidad de sílaba, golpe seco o frase rota.

### Si el jugador atiende a la pareja/ex
- la intimidad entra en juego antes,
- el dormitorio deja de ser fondo y empieza a pedir cuentas,
- y la noche puede recoger ese hilo aunque el foco principal del ciclo siga siendo laboral.

### Si el jugador se deja mecer por amigo + TV
- la presión no desaparece,
- sólo se ablanda lo suficiente para pudrir mejor,
- y el residuo del día se vuelve más traicionero porque parece menos grave de lo que es.

---

## 4. Persistencia recomendada hacia Ciclo 2 — Noche

- El salón debe llegar a la noche con carga principal si el editor fue evitado, mentido o atendido sólo de forma funcional.
- La cocina debe llegar cargada si el jugador sostuvo el trabajo pero dejó el cuerpo en piloto automático.
- La pareja/ex queda oficialmente sembrada si hubo apertura, respuesta o visto no digerido.
- La TV debe poder pasar de comfort infectado a suggestion más visible.
- La puerta ya tiene derecho a sonar como algo que aprende un poco mejor a usar lo que el jugador dejó suelto.

---

## 5. Veredicto de cierre

Esta ficha queda aprobada como **segunda ficha real de día** del proyecto. Su función es demostrar que la continuidad relacional no fragmenta el diseño, sino que le da vida mientras el sistema de deuda, contaminación y criatura gana precisión.
