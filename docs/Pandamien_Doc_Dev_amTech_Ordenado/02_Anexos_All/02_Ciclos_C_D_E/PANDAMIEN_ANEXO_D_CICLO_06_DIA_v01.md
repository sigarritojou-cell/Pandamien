# PANDAMIEN — ANEXO D
## Ficha real de día — Ciclo 6: Colonización semántica
### Derivada del GDD Maestro v03, del Anexo M v01, del Anexo A v01, del Anexo I v01 y de los pilotos authored de los ciclos 1–5

---

## 0. Intención del día

El sexto día no debe sentirse como “el día raro” en el que todo se vuelve surrealista porque sí. Debe sentirse como el día en que el lenguaje del piso deja de pertenecer a compartimentos estancos. La madre ya no habla sólo como madre. El editor ya no aprieta sólo como trabajo. La pareja/ex ya no duele sólo en dormitorio o balcón. El amigo ya no alivia limpio. Y la televisión ya no acompaña: empieza a organizar, doblar, editorializar y coser trozos de todas esas voces hasta que el protagonista ya no sabe del todo si lo que oye sigue viniendo de fuera o de la digestión del apartamento.

La función dramática del día es:

- desplazar la presión activa desde un vínculo concreto hacia la colonización semántica,
- hacer que la TV tome una posición de pseudo-centro interpretativo,
- permitir que madre, amigo, editor y pareja/ex sigan vivos a la vez como material mezclable,
- contaminar sobre todo salón y pasillo, con goteo hacia dormitorio y cocina,
- ofrecer una contención que ya no sea sólo física, sino también de corte de cadena interpretativa,
- y preparar una noche donde la puerta no sólo mire o respire, sino que intente decir.

---

## 1. Ficha oficial

```yaml
cycle_id: "C06"
cycle_title: "Colonización semántica"
day_theme: "las voces ya no conservan sus fronteras"
act_phase: "Acto III — Convergencia"

presence_base:
  - character: "Madre"
    format: "mensaje o audio breve de cuidado que ya suena contaminable"
    tone: "cercano, práctico, pero demasiado reconocible dentro del resto del ruido"
    purpose: "aportar gramática corporal y cuidado que la TV y la criatura puedan parasitar"
  - character: "Amigo"
    format: "cadena corta de mensajes, audio banal o llamada fugaz"
    tone: "ligero, callejero, un poco absurdo"
    purpose: "aportar ruido social, broma y cháchara deformable"
  - character: "Pareja/Ex"
    format: "mensaje o historial reactivado de baja intensidad pero alta carga"
    tone: "íntimo, ambiguo, suave por fuera y corrosivo por dentro"
    purpose: "aportar material afectivo que pueda mezclarse con otras voces"

pressure_active:
  primary_system_or_character: "TV / lenguaje contaminado / mezcla de ecos"
  format: "TV activa, línea residual, llamada/mensaje cruzado, audio diegético que entra mal, secuencia de ecos demasiado oportunos"
  urgency: "medium_high"
  decision_core: "seguir escuchando, cortar la fuente, apagar la TV, responder a una de las voces y dejar las demás fermentar, o intentar ordenar el ruido sin lograr limpieza real"

persistent_echoes:
  - source: "Editor"
    form: "mensaje seco, deadline reactivada o silencio evaluativo que reaparece en el peor momento"
    effect: "añade medición, utilidad y vergüenza funcional al magma general"
  - source: "Madre"
    form: "eco de cuidado o rutina práctica"
    effect: "tiñe el ruido de cuerpo, descanso, obediencia y clínica blanda"
  - source: "Amigo"
    form: "broma, audio, frase banal o tono de conversación ligera"
    effect: "aporta parloteo, ligereza falsa y ruido que tapa"
  - source: "Pareja/Ex"
    form: "frase suspendida, historial, mensaje ambiguo o memoria reactiva"
    effect: "inyecta herida, pecho, deseo y reparación imposible"
  - source: "Puerta atrancada"
    form: "recuerdo de mirada, pecho y trayecto ya aprendidos"
    effect: "el pasillo se vuelve la línea por la que todas las voces podrían terminar volviendo material"

entry_state:
  player_body_state: "cansancio mezclado con saturación verbal; ya no pesa sólo el cuerpo ni sólo la deuda, pesa el exceso de sentido"
  apartment_state_summary: "salón y pasillo funcionan como eje de mezcla; la TV ha dejado de ser compañía inocente y el dormitorio ya no protege de la contaminación del resto"
  tv_state: "suggestion avanzada entrando en manipulation"
  weather_or_exterior_bias: "afuera existe, pero el protagonismo ya no está en ver más, sino en interpretar peor"

relational_beats:
  - beat_id: "C06_D_B01"
    trigger_window: "mañana media o primer momento de encendido de TV / estancia larga en salón"
    source: "TV"
    format: "línea demasiado oportuna, programa magazine/tertulia, presentador/a o voz que roba tono de otros vínculos"
    short_description: "la TV ya no sólo comenta; parece anticipar, completar o deformar lo que el jugador acaba de leer o dejar sin responder"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "salón y pasillo se vuelven eje principal de semántica contaminada"
      - "si el jugador se queda escuchando, sube mezcla de voces y futura capacidad imitativa de criatura"
      - "si corta la TV, baja una capa de ruido pero sube la crudeza del silencio del piso"
  - beat_id: "C06_D_B02"
    trigger_window: "después del primer arrastre semántico o cuando el jugador revisa el móvil"
    source: "Editor"
    format: "mensaje breve, preciso y medidor"
    short_description: "su irrupción no domina el día, pero añade una línea de utilidad que la TV o el pasillo pueden robar enseguida"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "salón mantiene deuda funcional dentro del ruido general"
      - "si se ignora, la criatura gana material de voz cortante y rencor semántico"
  - beat_id: "C06_D_B03"
    trigger_window: "mediodía o tarde temprana"
    source: "Madre"
    format: "audio o mensaje breve"
    short_description: "aparece con cuidado práctico que ya no entra como hilo separado, sino como frase susceptible de ser tragada por TV o puerta"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "baño y dormitorio siguen vivos, pero ya conectados con salón por contaminación de lenguaje"
      - "si se evita, el cuidado se vuelve más fácil de parasitar"
  - beat_id: "C06_D_B04"
    trigger_window: "tarde media"
    source: "Amigo"
    format: "audio corto, broma, cadena ligera"
    short_description: "la banalidad ya no cae limpia; puede aliviar o resultar grotesca por exceso de mezcla con lo demás"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "cocina y salón pueden llenarse de parloteo o quedar más vacíos por contraste"
      - "si se usa como refugio, la TV gana tono de entretenimiento anestésico"
  - beat_id: "C06_D_B05"
    trigger_window: "quietud mala en dormitorio, balcón o incluso en salón tras saturación"
    source: "Pareja/Ex"
    format: "mensaje corto, releer historial o frase suspendida"
    short_description: "la intimidad ya no manda el ciclo, pero sigue pinchando el tejido justo cuando el lenguaje general ya está roto"
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "dormitorio y balcón permanecen cargados como fuentes secundarias de pecho y voz herida"
      - "si se abre aquí, la mezcla sentimental se vuelve más peligrosa para la noche"

contamination:
  primary_focus:
    zone: "Salón"
    material_form: "TV encendida demasiado tiempo, brillo residual, portátil, mando, taza olvidada, papeles, cableado, mesa o sofá convertidos en interfaz de consumo y espera"
    emotional_cause: "anestesia, búsqueda de relato, necesidad de compañía, incapacidad de cortar la cadena de interpretación"
    escalation_if_ignored: "la criatura gana voz más articulada, imitación, frase abortada, rencor verbal o parloteo podrido"
  secondary_focus:
    zone: "Pasillo"
    material_form: "trayecto más tenso, sombra con dirección, marco y pared que parecen retener eco verbal, longitud subjetiva del pasillo más agresiva"
    emotional_cause: "todo termina orientándose hacia la puerta; el piso organiza sentido alrededor de la espera"
    escalation_if_ignored: "la noche devuelve frase rota, imitación o llamada fallida con dirección clara"
  inherited_focus_optional:
    zone: "Dormitorio o cocina"
    condition: "si herida íntima o banalidad evasiva quedaron muy activas"
    effect: "aportan tono emocional o hambre/ruido a la mezcla general, pero no deben robar el eje salón-pasillo"

containment_offer:
  is_available: true
  action: "apagar la TV, cortar una cadena de mensajes, cerrar portátil, despejar el frente de salón o romper la secuencia de escucha continua"
  location: "salón o pasillo, una sola intervención significativa"
  time_cost: "rompe acompañamiento, deja solo al jugador con el silencio o con una deuda relacional"
  relational_cost: "si se corta un frente, otro vínculo queda abierto o reaparece por otra vía"
  systemic_benefit: "reduce la mezcla más obvia y frena la vía más directa hacia voz/imitación de criatura"
  systemic_risk: "la contención no limpia el ruido ya tragado; sólo le cambia de canal y puede empujarlo hacia puerta o pasillo"

tv_material:
  baseline_content: "magazine, tertulia, informativo blando o entretenimiento donde las frases parecen dialogar demasiado con lo que el jugador vive"
  parasitic_line_pool:
    - "todo el mundo necesita que le contesten"
    - "hay cosas que se dejan para luego y luego ya no vuelven igual"
    - "lo importante es no perder el hilo"
    - "si no puedes con todo, al menos di algo"

exterior_material:
  window_event: "una figura, una luz o un gesto exterior parecen responder más al relato que al mundo; nunca prueba limpia"
  peephole_event: "el rellano ofrece casi nada, pero la falta de información ya parece una frase"
  balcony_event: "el aire no despeja; deja al jugador más mezclado con sus propias interpretaciones"

day_closing_debt:
  unresolved_relation: "quedan varias voces abiertas a la vez; el problema ya no es una sola deuda, sino no saber cortar ninguna sin coste"
  unresolved_zone: "salón o pasillo, según se haya intentado contener superficie o trayecto"
  unresolved_truth: "el piso ya no sólo devuelve residuo material; empieza a montar sintaxis"
```

---

## 2. Notas de dirección

### 2.1. Regla de mezcla
La mezcla no debe sonar a collage chulo ni a videoclip de horror. Debe sonar a realidad demasiado contaminada: frases que llegan bien pero significan mal, tonos que se pegan, ecos que no son del todo atribuibles.

### 2.2. Regla de TV
La TV tiene que parecer inteligente sin volverse literalmente omnisciente. Lo importante no es que “sepa”, sino que robe, recombine y editorialice.

### 2.3. Regla de piso
El salón ya no es sólo lugar de trabajo o pasividad. Es aparato digestivo del lenguaje. El pasillo ya no es sólo trayecto. Es sintaxis física hacia la puerta.

### 2.4. Función emocional
El horror aquí nace de sentir que ya no controlas del todo qué voz pertenece a qué deuda. El jugador empieza a sospechar que el apartamento piensa con sobras humanas.

---

## 3. Persistencia recomendada hacia Ciclo 7

- La TV deja de ser apoyo ambiguo para convertirse en agente claro de mezcla y manipulación.
- La criatura queda posicionada para pasar de imitación defectuosa a presión verbal más dirigida.
- El pasillo gana carácter de órgano de traducción entre relaciones y puerta.
- El siguiente ciclo debe poder superponer presiones incompatibles sin necesidad de inventar una amenaza nueva.
- La gramática del final dialogado gana suelo: la criatura ya tiene material lingüístico bastante amplio como para responder mal, reclamar mal o pedir mal.

---

## 4. Veredicto de cierre

Esta ficha queda aprobada como **sexta ficha real de día** del proyecto. Demuestra que PANDAMIEN puede entrar en la contaminación semántica sin romper su principio central: el horror no llega por espectáculo, sino porque el piso ya sabe usar lo humano como idioma.
