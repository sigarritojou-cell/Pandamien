# PANDAMIEN — ANEXO D
## Ficha real de día — Ciclo 4: La herida íntima
### Derivada del GDD Maestro v03, del Anexo M v01, del Anexo A v01, del Anexo I v01 y de los pilotos authored de los ciclos 1, 2 y 3

---

## 0. Intención del día

El cuarto día no debe sentirse como “el capítulo romántico” del juego. Debe sentirse como el momento en que la intimidad deja de ser una aguja ocasional y se convierte en la presión activa del ciclo. El cuerpo ya ha sido puesto en primer plano por el ciclo anterior; ahora esa carne cansada recibe una llamada, un audio, un mensaje largo o una reapertura de historial que no entra en un vacío limpio, sino en una casa ya húmeda, ya atenta y ya capaz de devolver afecto deformado.

La función dramática del día es:

- hacer que la pareja/ex tome la presión activa sin secuestrar el tejido de vida cotidiana,
- contaminar dormitorio y balcón con memoria, deseo, ambigüedad y reparación imposible,
- mantener a madre y amigo como ritmos reales del encierro,
- dejar al editor como amenaza funcional de fondo, capaz de envenenar el clima con una sola irrupción breve,
- ofrecer una contención más afectiva y más desagradable que las anteriores,
- y preparar una noche donde la puerta ya no sólo respire o roce, sino que empiece a latir, suplicar o hablar emocionalmente mal.

---

## 1. Ficha oficial

```yaml
cycle_id: "C04"
cycle_title: "La herida íntima"
day_theme: "lo que estaba ausente ya pide habitación"
act_phase: "Acto II — Colonización íntima"

presence_base:
  - character: "Madre"
    format: "mensaje corto, llamada breve o audio de cuidado que entra en mal momento"
    tone: "preocupado, corporal, algo cansado"
    purpose: "recordar que el cuerpo sigue reclamando atención incluso dentro de la crisis íntima"
  - character: "Amigo"
    format: "mensaje banal, audio ligero o comentario fuera de tempo"
    tone: "cercano, bromista, torpemente salvador"
    purpose: "mantener una falsa normalidad que por contraste duele más"

pressure_active:
  primary_system_or_character: "Pareja/Ex"
  format: "llamada difícil, audio cargado, mensaje largo o historial reabierto con intención"
  urgency: "medium_high"
  decision_core: "abrir la intimidad, defenderse, aplazar, dejar en visto o refugiarse en una respuesta mínima que no cierre nada"

persistent_echoes:
  - source: "Editor"
    form: "notificación breve, recordatorio seco o silencio funcional que corta el clima"
    effect: "el trabajo ya no domina, pero sigue presente como amenaza de utilidad incrustada"
  - source: "Madre"
    form: "eco corporal, cuidado que interrumpe o frase que recuerda sueño/comida/medicación"
    effect: "evita que el ciclo se convierta en pura escena sentimental"
  - source: "TV"
    form: "suggestion parasitando lenguaje íntimo, melodrama suave o consejo ridículamente oportuno"
    effect: "vuelve borrosa la frontera entre intimidad real y sentimentalización tóxica"
  - source: "Puerta atrancada"
    form: "peso latente en el pasillo, ya asociado a pecho y respiración"
    effect: "la casa parece esperar algo del jugador cuando el dormitorio y el balcón se cargan"

entry_state:
  player_body_state: "fatiga arrastrada, pecho algo tomado, energía emocional más frágil que física, necesidad de evasión y de contacto a la vez"
  apartment_state_summary: "el dormitorio ya no es refugio limpio; el balcón empieza a sentirse como umbral íntimo; el salón conserva deudas viejas y la TV acompaña demasiado"
  tv_state: "suggestion con deriva sentimental y clínica"
  weather_or_exterior_bias: "luz más caída, aire posible desde balcón pero sin promesa real de alivio"

relational_beats:
  - beat_id: "C04_D_B01"
    trigger_window: "mañana tardía o primera tarde, cuando el jugador entra en dormitorio o reposa un momento"
    source: "Pareja/Ex"
    format: "mensaje largo, audio o llamada difícil"
    short_description: "abre una intimidad que no llega en el momento correcto; puede sonar vulnerable, ambigua, enfadada o demasiado suave, pero siempre deja claro que hay una habitación emocional sin cerrar"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "dormitorio y balcón pasan a primer plano dramático"
      - "si se responde con verdad, sube threat_intimacy y la herida queda oficialmente abierta"
      - "si se esquiva o se deja en visto, crecen silencio cargado, pecho doliente y futura súplica de criatura"
  - beat_id: "C04_D_B02"
    trigger_window: "después del primer impacto íntimo o cuando el jugador intenta recomponerse"
    source: "Madre"
    format: "mensaje breve o llamada corta"
    short_description: "pregunta algo pequeño del cuerpo o del día, y por eso mismo corta o agrava el clima; recuerda que el protagonista sigue teniendo carne, hambre y sueño mientras se le abre la herida"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "baño y dormitorio quedan ligados"
      - "si entra mal, el cuidado suena intrusivo; si entra bien, agrava la fragilidad"
  - beat_id: "C04_D_B03"
    trigger_window: "mitad o final de tarde"
    source: "Amigo"
    format: "audio absurdo, chiste, mensaje ligero o invitación a una llamada sin solemnidad"
    short_description: "ofrece una salida banal y casi obscena por contraste con lo íntimo recién abierto"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "salón y cocina recuperan o pierden calor humano"
      - "si el jugador se refugia aquí, la intimidad no desaparece: fermenta"
  - beat_id: "C04_D_B04"
    trigger_window: "cuando el clima ya está cargado o al acercarse al cierre del día"
    source: "Editor"
    format: "mensaje seco o recordatorio cortante"
    short_description: "no toma el control del día, pero lo envenena con una irrupción funcional que deja claro que la herida íntima no suspende la maquinaria"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "el salón se mantiene como deuda latente"
      - "si aparece justo después de la pareja/ex, mezcla vergüenza funcional con pecho y resentimiento"

contamination:
  primary_focus:
    zone: "Dormitorio"
    material_form: "cama más hundida, sábana arrugada con marca demasiado viva, ropa acumulada, vaso o móvil como reliquia, olor a habitación cerrada, objeto compartido o reaparecido"
    emotional_cause: "intimidad suspendida, deseo mal digerido, duelo blando, rumiación, historial reabierto"
    escalation_if_ignored: "la criatura gana corazón, pecho, voz herida o súplica; la noche puede devolver latido, pausa afectiva o frase emocional torcida"
  secondary_focus:
    zone: "Balcón"
    material_form: "ceniza, colilla, tela húmeda, luz de fuera que entra demasiado, barandilla o puerta corredera cargadas de respiración y espera"
    emotional_cause: "tentación de aire, necesidad de distancia, mirar fuera para no mirar dentro"
    escalation_if_ignored: "puede sembrar pulmones, exposición y una cualidad de llamada o exhalación hacia afuera"
  inherited_focus_optional:
    zone: "Baño"
    condition: "si C03 dejó cuerpo muy mal contenido"
    effect: "sigue como humedad de fondo y vuelve lo íntimo más pegajoso, más corporal y menos abstracto"

containment_offer:
  is_available: true
  action: "recomponer mínimamente la cama / guardar un objeto íntimo / cerrar el historial y apartar el móvil / salir al balcón sólo para retirar un resto o abrir/cerrar con intención"
  location: "dormitorio o balcón, una sola intervención significativa"
  time_cost: "obliga a interrumpir la rumiación o a sostener la herida de frente"
  relational_cost: "si contienes la intimidad, alguien queda sin respuesta; si no la contienes, la casa se la queda entera"
  systemic_benefit: "amortigua la vía más directa hacia corazón, pecho, voz emocional o súplica"
  systemic_risk: "puede sentirse como negación, como ritual ridículo o como cierre falso; no cura, sólo desplaza el tono del retorno nocturno"

medication_offer:
  is_available: true
  action: "plantearse medicación, corte o descanso anticipado"
  dramatic_meaning: "apagar el pecho antes de que hable demasiado"
  systemic_risk: "si se usa para no atravesar la herida, aumenta avoidance y deja la noche más contenida pero más suplicante"

tv_material:
  baseline_content: "programa o película tibia, magazine sentimental, voces de compañía que parecen entender demasiado"
  parasitic_line_pool:
    - "hay cosas que una nunca termina de cerrar"
    - "a veces una llamada cambia el día entero"
    - "no todo lo que vuelve merece abrirse"

exterior_material:
  window_event: "pareja o figura en balcón ajeno, luz vecina demasiado íntima, escena mínima de convivencia ajena"
  peephole_event: "sin peso central; el umbral principal del ciclo es emocional más que vecinal"
  balcony_event: "el balcón puede funcionar como respiración falsa, fuga mínima o teatro de una llamada que no se sostiene dentro"

day_closing_debt:
  unresolved_relation: "la pareja/ex debe quedar claramente activada; madre y amigo siguen vivos; el editor deja un veneno fino en el fondo"
  unresolved_zone: "dormitorio o balcón, según qué se haya dejado sin contener"
  unresolved_truth: "la intimidad no vuelve como recuerdo limpio; vuelve como material pegajoso que quiere casa"

handoff_to_transition:
  light_shift_meaning: "la tarde cae sobre la cama, el móvil, la puerta del balcón y las superficies donde uno se queda demasiado tiempo"
  sound_shift_meaning: "el apartamento empieza a recoger la vibración afectiva del día"
  first_door_hint: "la puerta atrancada ya no parece sólo respirada; parece guardar algo que ha empezado a tener pecho o pena"
```

---

## 2. Notas de dirección

### 2.1. Tono
Este día debe doler más que asustar. La presión íntima tiene que ser reconocible, sórdida, cotidiana y profundamente material. Nada de escena de amor plastificada. Nada de melodrama de anuncio.

### 2.2. Jerarquía jugable
La pareja/ex toma presión activa, sí, pero el ciclo no puede convertirse en teatro de una sola voz. Madre y amigo deben seguir cruzando la jornada, y el editor debe poder meter un cuchillo pequeño sin secuestrar el día.

### 2.3. Función del dormitorio
El dormitorio no es sólo escenario romántico ni lugar de descanso. Es almacén de pecho, cama, sudor, historial, objeto y repetición mental. Debe sentirse como zona íntima degradada, no como set decorativo.

### 2.4. Función del balcón
El balcón no salva. El balcón expone. Es un borde donde el aire puede parecer suficiente durante diez segundos y luego dejar más claro que no lo era.

### 2.5. Regla anatómica
Si domina el dormitorio, la criatura se inclina hacia corazón, pecho, voz herida o súplica. Si domina el balcón, añade exposición, pulmones y una forma de llamar hacia fuera o desde fuera. Si el baño heredado sigue pesado, lo íntimo se vuelve más húmedo y corporal.

### 2.6. Función emocional
La herida íntima no debe sentirse como subtrama. Debe sentirse como una habitación de la casa que el jugador llevaba años intentando no abrir y que ahora se ha quedado sin cerrojo.

---

## 3. Persistencia recomendada hacia Ciclo 5

- La pareja/ex debe quedar ya lo bastante incrustada como para seguir contaminando dormitorio, balcón, TV y noches aunque no domine todos los ciclos.
- La madre tiene que seguir viva como cuidado que entra peor cuando el pecho ya va cargado.
- El amigo puede funcionar como alivio obsceno o como prueba de que la vida banal continúa incluso cuando uno no puede seguirla.
- El editor queda como cuchillo fino, listo para reaparecer cuando el exterior empiece a apretar.
- La puerta debe estar preparada para devolver corazón, pecho, súplica o voz emocional mal formada.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **cuarta ficha real de día** del proyecto. Cierra la lógica del ciclo en que la pareja/ex toma presión activa y asegura que la herida íntima no nazca aislada del cuerpo, de la casa y de la criatura.

La norma final del ciclo es sencilla:

**la intimidad no vuelve para explicarse; vuelve para pedir sitio.**
