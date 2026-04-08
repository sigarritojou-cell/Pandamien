# PANDAMIEN — ANEXO D
## Ficha real de día — Ciclo 3: El cuerpo entra en juego
### Derivada del GDD Maestro v03, del Anexo M v01, del Anexo A v01, del Anexo I v01 y de los pilotos authored de los ciclos 1 y 2

---

## 0. Intención del día

El tercer día debe sentirse como una factura física. El trabajo no desaparece, la pareja/ex ya ha dejado una aguja clavada y el amigo sigue ofreciendo una falsa normalidad respirable, pero la presión activa deja de estar fuera y se mete en la carne. El protagonista ya no puede fingir del todo que el cuerpo es el vehículo silencioso de la trama. El cuerpo es una escena.

La función dramática del día es:

- desplazar el foco de la productividad al cuerpo como archivo y como límite,
- hacer que madre/medicación ganen peso sin convertir la jornada en sermón sanitario,
- dejar que la pareja/ex empiece a entrar en el tejido diario justo cuando peor sienta,
- mantener al editor vivo como deuda de fondo que no concede tregua limpia,
- tensar baño y dormitorio como zonas principales de desgaste,
- ofrecer una contención más íntima y más desagradable,
- y preparar una noche en la que la puerta ya no sólo articule una función: la incorpore al ritmo del aire y del pecho.

---

## 1. Ficha oficial

```yaml
cycle_id: "C03"
cycle_title: "El cuerpo entra en juego"
day_theme: "ya no basta con seguir; el cuerpo reclama su deuda"
act_phase: "Acto I tardío rozando Acto II"

presence_base:
  - character: "Madre"
    format: "llamada más larga o audio más personal + posible insistencia sobre comer, ducharse, medicación o abrir la ventana"
    tone: "cuidado real mezclado con control, miedo y costumbre"
    purpose: "arrastrar la jornada hacia el cuerpo, el baño, el dormitorio y la obediencia práctica"
  - character: "Amigo"
    format: "mensaje o audio breve de banalidad que contrasta con el estado físico"
    tone: "ligero, cercano, algo inoportuno sin querer"
    purpose: "recordar que la vida social sigue intentando colarse incluso cuando el cuerpo ya no da"
  - character: "Pareja/Ex"
    format: "mensaje pequeño o eco relacional que entra en mal momento"
    tone: "íntimo, ambivalente, casi suave por fuera y punzante por dentro"
    purpose: "hacer que la intimidad no espere a estar cómoda para aparecer"

pressure_active:
  primary_system_or_character: "Madre / cuerpo / medicación"
  format: "llamada, audio o cadena breve de insistencia práctica"
  urgency: "medium_high"
  decision_core: "aceptar cuidado, mentir sobre el estado corporal, aplazar una acción básica o cortar para seguir funcionando"

persistent_echoes:
  - source: "Editor"
    form: "recordatorio de fondo, mensaje seco o silencio cargado después del retraso anterior"
    effect: "el trabajo ya no manda la jornada, pero sigue incrustado como vergüenza interna y deuda pendiente"
  - source: "Pareja/Ex"
    form: "mensaje que entra cuando el cuerpo ya va tarde"
    effect: "dormitorio y balcón se vuelven más personales incluso sin escena principal"
  - source: "TV"
    form: "suggestion con deriva clínica, descanso, normalización del agotamiento o autocuidado banalizado"
    effect: "vuelve ambiguo el límite entre atenderse y anestesiarse"
  - source: "Puerta atrancada"
    form: "recuerdo físico de la segunda noche"
    effect: "el pasillo ya no es sólo trayecto; es la línea por la que el piso parece escuchar el cuerpo"

entry_state:
  player_body_state: "sueño peor, hambre irregular, aseo aplazado, pesadez en pecho o cabeza, energía de mentira"
  apartment_state_summary: "baño y dormitorio pesan más; el salón sigue cargado de trabajo residual, pero ya no monopoliza la sensación central del día"
  tv_state: "suggestion tirando a clínico-tranquilizadora"
  weather_or_exterior_bias: "luz más blanca o desvaída; afuera parece ventilación posible, no alivio verdadero"

relational_beats:
  - beat_id: "C03_D_B01"
    trigger_window: "mañana temprana o media mañana, antes de haber recompuesto el cuerpo"
    source: "Madre"
    format: "llamada larga o audio insistente"
    short_description: "pregunta si ha dormido, si se ha duchado, si ha comido, si se ha tomado algo; el tono ya lee fatiga real, no pereza abstracta"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "baño y dormitorio ganan centralidad plena"
      - "si se evita, el cuerpo pasa de problema funcional a deuda íntima"
      - "si se acepta demasiado, sube la sensación de obediencia vigilada y dependencia del corte"
  - beat_id: "C03_D_B02"
    trigger_window: "después del primer contacto con madre o cuando el jugador intenta arrancar la mañana"
    source: "Editor"
    format: "mensaje de fondo, breve pero pesado"
    short_description: "no toma el control del día, pero recuerda que la deuda laboral sigue viva y que el cuerpo no da inmunidad moral"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "salón sigue infectado como deuda latente"
      - "si se responde mal, el cuerpo y el trabajo chocan y se prepara vergüenza más somática"
  - beat_id: "C03_D_B03"
    trigger_window: "mediodía o primera tarde, cuando el jugador ya arrastra cansancio"
    source: "Amigo"
    format: "mensaje breve o audio con tontería"
    short_description: "aparece con ruido social ligero, lo bastante vivo como para dar alivio y lo bastante fuera de tempo como para doler un poco"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "cocina y salón pueden recuperar calor banal o volverse más vacíos por contraste"
      - "si el jugador se refugia demasiado, la fatiga se enmascara y el cuerpo se cobra luego la ocultación"
  - beat_id: "C03_D_B04"
    trigger_window: "tarde media o momento de quietud mala en dormitorio / baño / balcón"
    source: "Pareja/Ex"
    format: "mensaje pequeño, audio corto o eco íntimo que entra cuando menos espacio hay"
    short_description: "la intimidad llega justo cuando el cuerpo ya no tiene margen; no secuestra el ciclo, pero deja marca en pecho, cama, respiración o balcón"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "dormitorio y balcón se vuelven más densos"
      - "si se abre la herida ahora, el descanso posterior se vuelve peor y la noche más íntima"

contamination:
  primary_focus:
    zone: "Baño"
    material_form: "toalla húmeda demasiado tiempo, junta oscurecida, espejo salpicado, olor cerrado, superficie pegajosa o goteo mínimo que ya no parece inocente"
    emotional_cause: "descuido corporal, cansancio acumulado, aplazamiento de lo básico y lectura materna incrustada en la propia cabeza"
    escalation_if_ignored: "la criatura gana piel, mucosa, respiración húmeda o un pecho todavía incompleto pero más sensible"
  secondary_focus:
    zone: "Dormitorio"
    material_form: "cama hundida, ropa a medio caer, lado de mesilla cargado, vaso olvidado, aire sin renovar, marca tenue en sábana o almohada"
    emotional_cause: "agotamiento, deseo de desaparecer, intimidad suspendida, uso del dormitorio como refugio que ya no repara"
    escalation_if_ignored: "la noche puede devolver latido blando, peso de pecho, respiración de sueño o pausa íntima demasiado consciente"
  inherited_focus_optional:
    zone: "Salón"
    condition: "si el jugador dejó muy mal el ciclo 2"
    effect: "la deuda laboral sigue adherida como ruido de fondo, pero no debe robar la jornada"

containment_offer:
  is_available: true
  action: "ducharse o asearse de forma mínima y real, cambiar la toalla o ventilar / recomponer cama y abrir dormitorio"
  location: "baño o dormitorio, una sola intervención significativa"
  time_cost: "rompe la falsa continuidad funcional del día y puede dejar mensajes, trabajo o intimidad en suspensión"
  relational_cost: "si se contiene el cuerpo, alguien queda esperando; si no se contiene, el cuerpo aprende a esperar demasiado"
  systemic_benefit: "amortigua la vía más directa hacia piel, mucosa, pecho o respiración húmeda"
  systemic_risk: "la contención puede sentirse invasiva, insuficiente, obediente o demasiado tardía; no limpia el día, sólo modifica la textura de la deuda"

medication_offer:
  is_available: true
  action: "tomar medicación o plantearse tomarla antes del cierre nocturno"
  dramatic_meaning: "alivio, corte, obediencia, pacto temporal con el cuerpo o con la madre"
  systemic_risk: "si se usa demasiado pronto, desplaza la tensión del cuerpo a la evitación y deja la noche menos directa pero más doliente"

tv_material:
  baseline_content: "programa de fondo, magazine o voces blandas que recomiendan cuidarse, seguir la rutina o no venirse abajo"
  parasitic_line_pool:
    - "hay días en que el cuerpo también pide tregua"
    - "lo importante es no dejarse del todo"
    - "descansar también es necesario"

exterior_material:
  window_event: "vecino ventilando, ropa tendida, alguien tosiendo lejos o escena mínima de cuidado ajeno"
  peephole_event: "rellano quieto con resonancia doméstica; nada grande, pero todo demasiado cercano"
  balcony_event: "la tentación de salir un segundo a coger aire aparece como falsa promesa; el aire no arregla la saturación"

day_closing_debt:
  unresolved_relation: "la madre queda mejor o peor colocada según se acepte o rechace el cuidado; el editor sigue de fondo; la pareja/ex puede quedar oficialmente metida bajo la piel"
  unresolved_zone: "baño o dormitorio, según qué se haya dejado pudrir"
  unresolved_truth: "el cuerpo no es un contexto de la trama; es el lugar donde la trama empieza a cobrarse"

handoff_to_transition:
  light_shift_meaning: "la tarde cae sobre superficies usadas por el cuerpo, no sobre tareas abstractas"
  sound_shift_meaning: "el piso respira más cuando el jugador deja de moverse; los ruidos ya parecen internos"
  first_door_hint: "la puerta atrancada no parece simplemente más tensa: parece acompasar mal el aire del apartamento"
```

---

## 2. Notas de dirección

### 2.1. Tono
Este día no va de enfermedad clínica, ni de castigo moral, ni de simbolismo con megáfono. Va de saturación. El cuerpo ya no sostiene la ficción de rutina con la misma elegancia miserable que en C01 y C02.

### 2.2. Jerarquía jugable
La madre es la presión activa, pero no como gran bronca. Tiene que pesar porque ve demasiado, porque pregunta cosas pequeñas y porque obliga al jugador a decidir si se atiende o si sigue arrastrándose con dignidad podrida.

### 2.3. Función del editor
El editor no desaparece. Se vuelve peor: ya no empuja sólo desde fuera, sino como vergüenza interiorizada. Es ruido de fondo en el pecho del día.

### 2.4. Función de la pareja/ex
Aquí entra ya en el tejido cotidiano, pero todavía sin tomar el trono. Su fuerza está en aparecer cuando el cuerpo no tiene sitio para sentir algo más y, aun así, lo siente.

### 2.5. Contención
La contención del ciclo 3 debe sentirse íntima y casi humillante. Ducharse, cambiar una toalla o ventilar la cama son acciones mínimas, pero dramáticamente enormes. No ordenan la casa: impiden que el cuerpo se vuelva una incubadora más descarada.

---

## 3. Salidas sistémicas recomendadas

### Si el jugador acepta el cuidado de la madre
- baja algo la deuda corporal inmediata,
- pero sube la sensación de obediencia y vigilancia,
- la criatura puede tender menos a mucosa y más a latido íntimo o cuidado intrusivo,
- y la noche puede volverse menos húmeda pero más cercana.

### Si el jugador miente sobre su estado corporal
- suben avoidance, guilt_noise y amenaza íntima,
- el baño gana derecho a pudrirse con mala leche,
- y la puerta puede devolver respiración húmeda, roce de membrana o cansancio hecho sonido.

### Si el jugador prioriza trabajo sobre cuerpo
- el editor queda “atendido” sólo en apariencia,
- pero el cuerpo se cobra luego el aplazamiento,
- y la deuda laboral se mezcla mejor con vergüenza física.

### Si el jugador se refugia en banalidad
- el amigo y la TV amortiguan el día un rato,
- pero convierten el cuerpo en residuo sin palabra,
- y la noche gana posibilidades de retorno más pasivo, blando o doliente.

### Si el jugador atiende a la pareja/ex en mal momento
- el dormitorio y el pecho se abren antes de tiempo,
- la intimidad pesa más en la noche,
- y la criatura gana una primera mezcla entre respiración y herida.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **tercera ficha real de día** del proyecto. Demuestra que PANDAMIEN puede desplazar la presión del sistema laboral al cuerpo sin perder continuidad relacional ni caer en subrayado clínico.
