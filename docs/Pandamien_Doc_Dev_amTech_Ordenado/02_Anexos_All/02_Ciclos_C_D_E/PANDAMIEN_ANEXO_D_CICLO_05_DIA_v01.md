# PANDAMIEN — ANEXO D
## Ficha real de día — Ciclo 5: El exterior se pega al piso
### Derivada del GDD Maestro v03, del Anexo M v01, del Anexo A v01, del Anexo I v01 y de los pilotos authored de los ciclos 1–4

---

## 0. Intención del día

El quinto día debe sentirse como una infección de frontera. Hasta ahora el apartamento había absorbido mensajes, cuerpo, trabajo e intimidad y los había devuelto desde dentro. En este ciclo ocurre algo más jodido: el afuera deja de ser simple telón ambiguo y empieza a pegarse a los bordes del piso como si encontrara por fin por dónde entrar.

La presión activa no es “salir fuera”, porque el juego no abandona el apartamento. La presión activa es **vivir el umbral como zona enferma**: la mirilla, la puerta principal, el rellano, la ventana, el balcón, un paquete, una sombra, una luz vecina que parece mirar de vuelta. Lo importante no es descubrir una verdad exterior. Lo importante es que lo exterior ya no se comporta como información: se comporta como contagio interpretativo.

La función dramática del día es:

- romper la falsa frontera entre dentro y fuera,
- hacer que entrada, pasillo, ventana y balcón ganen peso como órganos del apartamento,
- mantener a madre y amigo como continuidad cotidiana mientras el umbral se vuelve más caro,
- dejar a la pareja/ex como eco íntimo que reaparece justo cuando mirar fuera abre memoria,
- reintroducir al editor como deadline secundaria que corta el clima y demuestra que el mundo útil no ha desaparecido,
- ofrecer una contención que ya no es sólo doméstica, sino también de exposición,
- y preparar una noche en la que la criatura ya no sólo respire o suplique: **mire**.

---

## 1. Ficha oficial

```yaml
cycle_id: "C05"
cycle_title: "El exterior se pega al piso"
day_theme: "lo de fuera ya no queda fuera"
act_phase: "Acto II — Colonización del umbral"

presence_base:
  - character: "Madre"
    format: "mensaje inquieto + posible llamada corta si el jugador tarda demasiado en responder"
    tone: "cuidador, preocupado, algo controlador"
    purpose: "recordar que exponerse demasiado o desaparecer de la rutina también tiene coste corporal y filial"
  - character: "Amigo"
    format: "comentario, audio o cadena breve sobre algo visto/oído fuera que quizá no cuadra"
    tone: "ligero, curioso, un poco nervioso sin admitirlo"
    purpose: "introducir el afuera desde la banalidad y la charla, no desde la épica del misterio"
  - character: "Pareja/Ex"
    format: "eco breve, mensaje reabierto o recuerdo activado al mirar ventana/balcón"
    tone: "íntimo, suspendido, ligado al aire y a la distancia"
    purpose: "hacer que el umbral no sólo active paranoia, sino también memoria"

pressure_active:
  primary_system_or_character: "Exterioridad / umbral"
  format: "paquete o llamada al timbre / ruido de rellano / sombra en mirilla / patrón insistente en ventana o balcón"
  urgency: "medium_high"
  decision_core: "acercarse, mirar, ignorar, escuchar sin actuar, exponerse un poco o sellar el borde para seguir fingiendo control"

persistent_echoes:
  - source: "Editor"
    form: "deadline secundaria o mensaje seco que reaparece en mal momento"
    effect: "corta el clima y recuerda que el mundo funcional sigue exigiendo incluso cuando el umbral ya está enfermo"
  - source: "TV"
    form: "suggestion editorializada sobre vigilancia, vecinos, contagio, seguridad o ruido urbano"
    effect: "vuelve dudoso si el peligro viene de fuera o del relato que se construye sobre lo de fuera"
  - source: "Pareja/Ex"
    form: "eco desde balcón o ventana; mensaje que reabre aire íntimo"
    effect: "la exposición al exterior arrastra también afecto y memoria"
  - source: "Puerta atrancada"
    form: "recuerdo somático de la noche 4"
    effect: "el jugador ya no camina hacia la puerta principal sin sentir que otra puerta escucha desde dentro"

entry_state:
  player_body_state: "cansancio útil, hipervigilancia leve, cuerpo menos devastado que en C03 pero más alerta y peor descansado"
  apartment_state_summary: "el dormitorio y el cuerpo siguen tocados por C04, pero ahora entrada y pasillo empiezan a competir por el centro emocional del piso"
  tv_state: "suggestion editorial tirando a manipulación blanda"
  weather_or_exterior_bias: "luz incierta, más contrastada o más sucia; el afuera parece especialmente interpretable"

relational_beats:
  - beat_id: "C05_D_B01"
    trigger_window: "mañana media o primer paso por entrada/pasillo"
    source: "Exterioridad"
    format: "ruido de rellano, paquete dudoso, llamada al timbre o sombra en mirilla"
    short_description: "algo del umbral exige lectura. No hay gran revelación, pero sí una forma demasiado concreta de presencia ajena o de objeto dejado."
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "entrada y pasillo ganan centralidad"
      - "si se mira sin actuar, suben amenaza íntima, orientación y sensación de estar siendo observado"
      - "si se ignora, el umbral fermenta y la noche puede devolver ojos, inmovilidad o respiración de rellano"
  - beat_id: "C05_D_B02"
    trigger_window: "tras el primer estímulo de umbral o al pasar por el salón con la TV encendida"
    source: "Madre"
    format: "mensaje inquieto o llamada corta"
    short_description: "pregunta dónde anda, si está bien, por qué tarda en responder; el cuidado se mezcla ahora con temor al afuera y con lectura de desorden"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "baño/dormitorio siguen vivos, pero entrada y pasillo se cargan de vigilancia filial"
      - "si se evita, la casa puede devolver cuidado vuelto control desde el umbral"
  - beat_id: "C05_D_B03"
    trigger_window: "mediodía o primera tarde"
    source: "Amigo"
    format: "audio corto o mensajes sobre algo visto fuera, vecino raro, paquete o ruido"
    short_description: "trae el exterior por la vía de la charla banal: quizá ha visto algo parecido desde su balcón, quizá se ríe de una paranoia, quizá la alimenta sin querer"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "ventana, balcón y cocina/salón ganan rumor social"
      - "si el jugador se engancha demasiado, el afuera se vuelve conversación antes que realidad"
  - beat_id: "C05_D_B04"
    trigger_window: "tarde media, cuando el día ya va cargado y el umbral ha dejado poso"
    source: "Editor"
    format: "mensaje seco o llamada breve"
    short_description: "reaparece con una deadline secundaria o una exigencia corta que cae como cuchillo fuera de sitio"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "salón sigue colonizado como deuda latente"
      - "si se combina con umbral no resuelto, el pasillo se vuelve trayecto de utilidad y amenaza"
  - beat_id: "C05_D_B05"
    trigger_window: "cerca de ventana o balcón, al final de la tarde"
    source: "Pareja/Ex"
    format: "eco corto, mensaje reabierto o recuerdo activado"
    short_description: "la intimidad reaparece ligada al aire, a la distancia o a una visión exterior concreta; no manda el ciclo, pero le da profundidad"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "balcón y dormitorio quedan reactivados"
      - "si se deja en suspensión, el exterior se vuelve más emocional y la noche más torcida"

contamination:
  primary_focus:
    zone: "Entrada / Pasillo"
    material_form: "felpudo húmedo, bolsa dejada demasiado tiempo, marco con marca oscura, polvo raro en zócalo, rendija demasiado viva, cadena o pomo con tacto sospechoso"
    emotional_cause: "hipervigilancia, lectura obsesiva del umbral, exposición sin digestión y mezcla entre amenaza exterior y deuda interior"
    escalation_if_ignored: "la criatura gana ojos, orientación, inmovilidad consciente o atención dirigida"
  secondary_focus:
    zone: "Ventana / Balcón"
    material_form: "cristal sucio que devuelve una imagen rara, cortina pegada, barandilla demasiado fría, ceniza o resto mínimo, aire que parece estancarse donde no debería"
    emotional_cause: "buscar fuera una verdad que el piso ya contamina, aire íntimo reactivado por memoria o por paranoia"
    escalation_if_ignored: "la noche puede devolver mirada, pausa expectante, exposición respirada o silencio demasiado inteligente"
  inherited_focus_optional:
    zone: "Dormitorio"
    condition: "si C04 quedó muy cargado"
    effect: "la intimidad sigue viva, pero ya no domina; se mezcla con el aire y con la distancia"

containment_offer:
  is_available: true
  action: "retirar el paquete o bolsa, limpiar/ordenar el frente de entrada o cerrar/regular ventana y balcón de forma significativa"
  location: "entrada-pasillo o ventana-balcón, una sola intervención con peso"
  time_cost: "obliga a elegir entre mirar más, responder a alguien o cortar la escalada del umbral"
  relational_cost: "puede dejar a madre/editor/pareja-ex en suspensión justo cuando el afuera está tirando"
  systemic_benefit: "reduce la vía más directa hacia ojos, orientación y presión de mirada"
  systemic_risk: "sellar un borde fortalece el otro; ordenar entrada puede cargar ventana/balcón, y cerrar balcón puede pudrir más el pasillo"

tv_material:
  baseline_content: "tertulia, noticias tibias o magazine de actualidad con tono de vigilancia social, convivencia, seguridad, vecinos, contagio o ruido"
  parasitic_line_pool:
    - "conviene no sacar conclusiones precipitadas"
    - "lo importante es mantener la calma y seguir las pautas"
    - "a veces una cosa pequeña en el rellano basta para alterar todo el día"

exterior_material:
  window_event: "patrón repetido en ventana vecina, figura quieta demasiado tiempo, luz que se enciende cuando no debería o alguien que parece mirar sin estar claramente mirando"
  peephole_event: "paquete, bolsa, sombra parcial, sonido de respiración dudosa o paso que se detiene demasiado cerca"
  balcony_event: "aire que no alivia, vecino demasiado presente o recuerdo íntimo ligado a la distancia"
  entry_event: "timbre breve, golpe pequeño, roce en el felpudo o silencio demasiado espeso"

day_closing_debt:
  unresolved_relation: "el umbral debe quedar por delante del resto, pero editor o madre pueden haber dejado cuchilla de fondo y la pareja/ex un eco suspendido"
  unresolved_zone: "entrada/pasillo o ventana/balcón, según la contención elegida"
  unresolved_truth: "lo externo no entra como verdad, sino como interpretación contagiosa que el piso utiliza para reorganizarse"

handoff_to_transition:
  light_shift_meaning: "la tarde cae sobre bordes y reflejos: cristal, mirilla, rendija, barandilla, pomo, sombra"
  sound_shift_meaning: "cuando baja el ruido del día, el rellano, el patio y el pasillo parecen hablar entre sí"
  first_door_hint: "al cruzar el pasillo, el jugador puede sentir que la puerta atrancada y la puerta principal comparten ahora una misma respiración torcida"
```

---

## 2. Notas de dirección

### 2.1. Tono
Este día no va de descubrir un secreto objetivo del exterior. Va de que el jugador ya no puede vivir el umbral como simple borde arquitectónico. La inquietud nace de lo cotidiano mal interpretado con fundamento suficiente.

### 2.2. Jerarquía jugable
La presión activa es exterioridad/umbral, pero el resto de vínculos no desaparece. Madre y amigo deben seguir haciendo de vida real; el editor debe reaparecer como cuchillo breve; la pareja/ex debe dejar aire emocional contaminado.

### 2.3. Regla de lectura
Si el ciclo parece “uno de vecinos raros” y no “uno del apartamento siendo infectado por el borde”, está mal enfocado.

### 2.4. Regla anatómica
La entrada y el pasillo alimentan ojos, orientación e inmovilidad consciente. La ventana y el balcón añaden aire, exposición y sensación de ser visto. Si queda demasiado activo el dormitorio heredado, la mirada se vuelve íntima, no sólo paranoica.

---

## 3. Persistencia recomendada hacia la noche

- Si se ignoró el umbral, la noche debe devolver silencio mirante, inmovilidad o respiración de rellano.
- Si se miró demasiado por mirilla o ventana sin actuar, sube la sensación de que el apartamento ha aprendido a observar.
- Si el editor reapareció mal, la mirada puede adquirir ritmo de medición o evaluación.
- Si la pareja/ex quedó activa, balcón y ventana deben cargar el exterior de afecto suspendido.
- La TV debe quedar lista para pasar de editorializar vigilancia a sugerir interpretación torcida.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **quinta ficha real de día** del proyecto. Cierra el ciclo donde el exterior deja de ser fondo ambiguo y se vuelve presión contaminante del piso sin abandonar nunca el principio maestro del juego:

**en PANDAMIEN el afuera no se explora: se filtra.**
