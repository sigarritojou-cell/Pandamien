
# PANDAMIEN — ANEXO D
## Ficha real de día — Ciclo 7: Doble vínculo imposible
### Derivada del GDD Maestro v04, del Anexo M v01, del Anexo A v01, del Anexo I v01 y de los pilotos authored de los ciclos 1–6

---

## 0. Intención del día

El séptimo día no debe sentirse como “más cosas pasando”, sino como el momento en que el sistema por fin te arrincona sin escapatoria limpia. Ya no basta con gestionar mal, aplazar o repartir la podredumbre con elegancia triste: ahora dos presiones legítimas e incompatibles se pisan la garganta y obligan a sacrificar algo que importa.

Para esta versión authored del ciclo se fija como combinación principal **Madre + Editor**. No porque sea la única posible dentro del canon, sino porque es la que mejor convierte la lógica del proyecto en una crueldad humana nítida: el cuerpo pide atención real y el mundo útil exige rendimiento en el mismo tramo de aire. Responder a una cosa mutila la otra.

La función dramática del día es:

- superponer dos sistemas incompatibles de forma inequívoca,
- obligar al jugador a elegir qué pérdida acepta cargar,
- hacer que el salón, el baño y el pasillo entren en guerra por el centro del piso,
- convertir la TV en aparato de confrontación y no sólo de suggestion/manipulation,
- dejar a pareja/ex y amigo como presencias reales pero no dominantes,
- fijar una zona claramente sacrificada,
- y preparar una noche donde la criatura ya no sólo devuelva mezcla o mirada, sino **temperamento dominante**.

---

## 1. Ficha oficial

```yaml
cycle_id: "C07"
cycle_title: "Doble vínculo imposible"
day_theme: "no puedes sostener las dos cosas"
act_phase: "Acto III tardío / borde de Acto IV"

presence_base:
  - character: "Madre"
    format: "llamada insistente, audio o mensaje que apunta a cuerpo, comida, medicación o crisis física real"
    tone: "preocupación cansada, control blando, amor con urgencia verdadera"
    purpose: "arrastrar el día al cuerpo, al baño, al dormitorio y al miedo de caída real"
  - character: "Editor"
    format: "mensaje claro + intento de llamada + deadline no prorrogable"
    tone: "preciso, medidor, profesional, cortante sin histeria"
    purpose: "exigir definición funcional justo cuando el cuerpo o el cuidado ya no admiten aplazamiento"
  - character: "Amigo"
    format: "audio breve, llamada perdida o mensaje de compañía que llega mal"
    tone: "cercano, banal, mal sincronizado"
    purpose: "recordar que incluso el alivio entra tarde y puede empeorar la saturación"
  - character: "Pareja/Ex"
    format: "historial reactivado, mensaje suspendido o eco íntimo mínimo"
    tone: "suave por fuera, corrosivo por dentro"
    purpose: "hacer que la decisión entre cuerpo y rendimiento también roce intimidad y verdad personal"

pressure_active:
  primary_system_or_character: "Madre + Editor"
  format: "colisión de llamada/mensaje corporal urgente con deadline funcional inmediata"
  urgency: "high"
  decision_core: "atender el cuerpo o sostener la entrega; responder a una presión deja sangrando la otra"

persistent_echoes:
  - source: "TV"
    form: "confrontational: frases sobre responsabilidad, no dejar esperando, cuidarse tarde y pagar lo aplazado"
    effect: "ya no acompaña ni sugiere; acusa, ordena y cose los dos frentes"
  - source: "Pareja/Ex"
    form: "historial reabierto, mensaje sin cerrar o eco de frase íntima que hace más obscena la elección"
    effect: "dormitorio y balcón conservan una herida secundaria que vuelve la decisión menos abstracta"
  - source: "Amigo"
    form: "ruido social o intento de apoyo torpemente extemporáneo"
    effect: "ofrece una tercera salida falsa: flotar un rato más"
  - source: "Puerta atrancada"
    form: "peso casi organizado al fondo del pasillo"
    effect: "el jugador siente que cualquier sacrificio va directo a alimentar carácter, no sólo cuerpo"

entry_state:
  player_body_state: "agotamiento sostenido, peor sueño, cuerpo funcional sólo por orgullo o inercia, sensación de descomposición organizada"
  apartment_state_summary: "salón y pasillo siguen cargados de lenguaje y medición; baño y dormitorio reclaman deuda corporal; la casa ya no parece pedir atención, parece exigir una pérdida"
  tv_state: "confrontational"
  weather_or_exterior_bias: "afuera existe como presión de calendario y testigo mudo, no como promesa"

relational_beats:
  - beat_id: "C07_D_B01"
    trigger_window: "mañana media o primer tramo útil del día"
    source: "Madre"
    format: "llamada o audio con urgencia real"
    short_description: "algo del cuerpo ya no admite frase de cortesía: mareo, comida sin tomar, medicación ignorada, ducha no hecha, voz realmente mala o cansancio que ya asusta"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "baño y dormitorio reclaman centralidad dramática"
      - "si se acepta el cuidado, el cuerpo gana margen pero el trabajo queda más expuesto"
      - "si se evita, la deuda corporal deja de ser sólo tristeza y pasa a insulto material"
  - beat_id: "C07_D_B02"
    trigger_window: "inmediatamente después o en el mismo tramo de respiración"
    source: "Editor"
    format: "mensaje seco + llamada breve o ultimátum"
    short_description: "la entrega o definición ya no admite anestesia elegante. El editor no ruge: delimita"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "salón, mesa y pasillo se vuelven herramientas de presión"
      - "si se atiende al editor, el cuerpo se convierte en residuo sacrificado"
      - "si se le deja colgado, la vergüenza funcional se vuelve casi física"
  - beat_id: "C07_D_B03"
    trigger_window: "tramo medio, cuando la elección ya está hecha o aplazada"
    source: "Amigo"
    format: "audio breve o llamada perdida"
    short_description: "entra tarde con intención de alivio, pero ya no puede salvar nada; sólo evidencia que la vida social también existe y no cabe"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "cocina y salón reciben una falsa salida"
      - "si el jugador se refugia aquí, se fija una tercera forma de cobardía: no decidir"
  - beat_id: "C07_D_B04"
    trigger_window: "tarde media o final, después del sacrificio principal"
    source: "Pareja/Ex"
    format: "mensaje mínimo, historial reabierto o eco"
    short_description: "no abre una nueva trama: sólo hace que la pérdida del día tenga alguien mirando desde dentro"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "dormitorio y balcón guardan memoria moral del sacrificio"
      - "si se responde, el jugador verbaliza lo que ha dejado morir"
      - "si se evita, la intimidad queda lista para volver como reproche deformado"

contamination:
  primary_focus:
    zone: "Zona sacrificada"
    material_form: "depende del sacrificio dominante: baño con humedad, espejo y ropa pegada si se abandonó el cuerpo; salón con restos de trabajo, TV, portátil y tiempo podrido si se abandonó la entrega"
    emotional_cause: "colisión entre cuidado y rendimiento; imposibilidad de atender ambos frentes"
    escalation_if_ignored: "ya no crece sólo función anatómica; se fija carácter de criatura"
  secondary_focus:
    zone: "Pasillo"
    material_form: "aire más denso, trayecto más hostil, puerta atrancada demasiado presente, sensación de tránsito condenatorio"
    emotional_cause: "el pasillo absorbe la decisión y la traduce en vector hacia la puerta"
    escalation_if_ignored: "la noche se vuelve juicio espacial y no sólo retorno sensorial"

containment_offer:
  is_available: true
  action: "intervención significativa pero excluyente: recomponer mínimamente el cuerpo (ducha, comida, medicación, ventilar baño) o sostener un gesto funcional real (sentarse, responder, entregar, ordenar el frente de trabajo)"
  location: "baño/dormitorio o salón, nunca ambos"
  time_cost: "alto"
  emotional_cost: "hacer una cosa deja a la otra explícitamente a la intemperie"
  outcome_logic:
    - "si se contiene el cuerpo, baja degradación física inmediata pero suben deuda laboral, vergüenza funcional y posible rencor"
    - "si se contiene lo funcional, baja la exposición con editor pero suben daño íntimo, respiración mala y sensación de autoabandono"
    - "si no se contiene nada, la criatura fija un temperamento más caótico, mezclado y hostil"

tv_behavior:
  mode: "confrontational"
  dominant_material:
    - "responsabilidad"
    - "no dejar a nadie esperando"
    - "cuidarse cuando ya es tarde"
    - "pagar lo que se ha dejado sin resolver"
  parasitic_targets:
    - "madre"
    - "editor"
    - "pareja/ex en residuo"
  note: "La TV no tiene que gritar. Tiene que unir las dos presiones con una obscenidad insoportable."

zone_bias:
  primary: "zona sacrificada"
  secondary: "pasillo"
  tertiary: "la zona del frente no elegido, que queda vibrando como deuda"

creature_learning:
  dominant_shift: "temperamento dominante"
  branches:
    if_body_sacrificed:
      likely_temperament:
        - "furioso"
        - "rencoroso"
      learned_logic: "la utilidad vale más que la carne"
    if_work_sacrificed:
      likely_temperament:
        - "doliente"
        - "suplicante"
      learned_logic: "el cuerpo cae y pide amparo"
    if_both_avoided:
      likely_temperament:
        - "imitativo"
        - "famélico"
      learned_logic: "nada se sostiene; todo se rumia y se roba"
  note: "El ciclo no decide por completo el monstruo, pero fija con fuerza el sesgo principal."

cycle_truth: "La tragedia no está en elegir mal; está en que la estructura ya no permite una elección limpia."
```

---

## 2. Secuencia de presión recomendada

1. **Entrada del cuerpo**. La madre o el síntoma abren el día antes de que el jugador pueda convencerse de que hoy sí funcionará.
2. **Entrada del mundo útil**. El editor cae sin pedir perdón y vuelve incompatible cualquier intento de recomposición lenta.
3. **Falsa tercera vía**. Amigo, TV o una microtarea ofrecen una forma de no decidir todavía.
4. **Sacrificio explícito**. El jugador atiende un frente, parchea ambos o huye de los dos.
5. **Resonancia íntima**. Pareja/ex o un eco privado devuelven el peso moral de la pérdida.
6. **Pasillo como juicio**. El piso acusa recibo antes de que llegue la noche.

---

## 3. Regla authored de sacrificio

Este ciclo debe dejar una de estas tres huellas bien visibles:

### 3.1. Sacrificio del cuerpo
- baño degradado,
- dormitorio con ropa/cama/aire peor,
- voz más frágil,
- criatura sesgada a furia rencorosa o a vergüenza que muerde.

### 3.2. Sacrificio del trabajo
- salón convertido en fracaso visible,
- portátil/mesa/reloj como restos acusatorios,
- editor más frío o casi administrativo,
- criatura sesgada a dolor, súplica o evaluación doliente.

### 3.3. Sacrificio de la verdad
- se responde a todos mintiendo o aplazando,
- no hay frente claramente atendido,
- el piso entero se vuelve más sospechoso,
- criatura sesgada a imitación, hambre verbal y resentimiento mezclado.

---

## 4. Validaciones para pasar a la noche

Antes de cerrar el día, el ciclo debe dejar claras estas cuatro cosas:

1. El jugador **ha sacrificado algo inequívoco**.
2. Hay una **zona claramente peor** por esa decisión.
3. La **TV** ya no acompaña: confronta.
4. La criatura no sólo ha crecido: **ha aprendido cómo tratar al jugador**.

Si una de esas cuatro patas falla, la noche de C07 entrará floja y el ciclo perderá el colmillo.

---

## 5. Veredicto de cierre

Esta ficha queda aprobada como **séptima capa authored de día del proyecto**. No agota todas las combinaciones posibles del ciclo 7 dentro del canon, pero sí fija una versión principal, clara y cruel del **doble vínculo imposible**, apoyada en la colisión entre **madre/cuerpo** y **editor/rendimiento**, con **TV confrontational**, **pasillo judicial** y **temperamento de criatura** en fase de fijación.
