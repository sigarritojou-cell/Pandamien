# PANDAMIEN — ANEXO D
## Ficha real de día — Ciclo 8: Resolución
### Derivada del GDD Maestro v04, del Anexo M v01, del Anexo A v01, del Anexo I v01 y de los pilotos authored de los ciclos 1–7

---

## 0. Intención del día

El octavo día no debe sentirse como “el capítulo final” subrayado con rotulador rojo. Debe sentirse como el día en que ya no queda distancia funcional suficiente entre el jugador, el piso y la puerta. La casa no está más espectacular: está más decidida. El jugador tampoco está “listo” en un sentido heroico; está arrinconado por el historial completo.

La presión activa ya no pertenece a un solo vínculo. Pertenece a la **criatura como suma viva del historial**, y al modo en que ese historial se ha repartido por el piso. Madre, editor, amigo, pareja/ex y TV no desaparecen: vuelven como últimas líneas de fuerza, residuos, llamadas tardías, mensajes no del todo contestados o frases robadas por el apartamento. Pero el centro del día es otro: **qué hace el jugador cuando ya no puede seguir tratando la puerta atrancada como un borde administrativo del piso**.

La función dramática del día es:

- convertir la puerta atrancada en la presión activa inequívoca del ciclo,
- hacer que todo el apartamento lea ya como antesala de confrontación,
- devolver el historial completo a través de presencia base residual de todos los vínculos,
- ofrecer una última preparación material y ética del umbral,
- cerrar el frente de “seguir gestionando” para abrir el frente de “responder”,
- y preparar una noche donde la criatura por fin pueda ser confrontada mediante diálogo y conducta, no sólo padecida.

---

## 1. Ficha oficial

```yaml
cycle_id: "C08"
cycle_title: "Resolución"
day_theme: "ya no puedes dejar la puerta para luego"
act_phase: "Acto IV — Umbral y devolución"

presence_base:
  - character: "Madre"
    format: "mensaje, audio o llamada breve que insiste en cuerpo, cuidado o miedo a que el jugador se esté rompiendo"
    tone: "íntimo, cansado, real"
    purpose: "recordar que la confrontación final también pasa por el cuerpo y por la forma de habitarlo"
  - character: "Editor"
    format: "mensaje de cierre, reproche final, silencio evaluativo o notificación seca"
    tone: "funcional, cortante, más cansado que violento"
    purpose: "devolver el rastro de utilidad, deuda y vergüenza con el que el jugador ha entrenado a la criatura"
  - character: "Amigo"
    format: "mensaje de compañía, audio extraño o banalidad que ya entra casi como eco"
    tone: "cercano, torpe, humanamente insuficiente"
    purpose: "recordar que la compañía también pudo ser refugio o anestesia"
  - character: "Pareja/Ex"
    format: "historial reabierto, mensaje mínimo o silencio afectivo con peso"
    tone: "íntimo, herido, suspendido"
    purpose: "dejar que la confrontación final también pase por intimidad y pérdida"
  - character: "TV"
    format: "línea residual, continuidad obscena, programa que parece despedirse o dictar"
    tone: "ya casi sin máscara"
    purpose: "funcionar como coro parasitario del historial"

pressure_active:
  primary_system_or_character: "Criatura / puerta atrancada / historial total"
  format: "signos diurnos inequívocos en el marco, el pasillo, el aire y el retorno de voces"
  urgency: "high"
  decision_core: "preparar el umbral, seguir aplazando un poco más, intentar contener desde fuera, hablar primero, o abrir una vía hacia confrontación/absorción/convivencia/ruptura"

persistent_echoes:
  - source: "Madre"
    form: "cuidado que llega cuando ya no puede ordenar el día"
    effect: "vuelve más carnal la decisión final"
  - source: "Editor"
    form: "deuda residual o cierre funcional"
    effect: "introduce medición, culpa y trato instrumental en la voz del final"
  - source: "Amigo"
    form: "compañía banal o tono de normalidad que ya no cabe"
    effect: "recuerda que parte del horror creció también a la sombra del ruido cómodo"
  - source: "Pareja/Ex"
    form: "silencio íntimo, frase reabierta o memoria activa"
    effect: "convierte la confrontación en herida personal y no sólo en problema espacial"
  - source: "TV"
    form: "residuo manipulador o sentencia cotidiana demasiado oportuna"
    effect: "hace de comentarista final del historial"

entry_state:
  player_body_state: "agotado, muy poroso, más claro en intención que en energía; el cuerpo ya no permite neutralidad"
  apartment_state_summary: "el piso completo funciona como antesala del umbral; ninguna zona queda inocente, pero una o dos dominan según historial de sacrificios"
  tv_state: "confrontational o residual manipulador"
  weather_or_exterior_bias: "afuera apenas importa como información; sólo pesa como contraste, salida imposible o testigo lejano"

relational_beats:
  - beat_id: "C08_D_B01"
    trigger_window: "mañana media o primer momento de mirar/evitar el pasillo"
    source: "Puerta atrancada / apartamento"
    format: "signo diurno inequívoco: marco cedido, humedad organizada, frase abortada, latido o presión física demasiado consciente"
    short_description: "por primera vez el umbral no puede leerse como rareza nocturna. El día mismo confirma que algo detrás ya no está sólo creciendo: está esperando respuesta."
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "el pasillo y la puerta atrancada pasan a ser centro total"
      - "cualquier aplazamiento ya no protege, sólo agrava el modo en que la criatura interpreta la relación"
      - "si el jugador se acerca o habla, empieza a fijarse el tono de confrontación final"
  - beat_id: "C08_D_B02"
    trigger_window: "tras el primer signo diurno o durante el intento de recomposición"
    source: "Madre / cuerpo"
    format: "mensaje, audio o llamada corta"
    short_description: "pregunta si está bien, si ha dormido, si ha comido o si le pasa algo. Lo cotidiano se vuelve insoportable porque llega justo cuando la casa ya no cabe en una explicación práctica."
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "baño, dormitorio y cuerpo vuelven a entrar en la resolución"
      - "según respuesta, la confrontación final tenderá más a amparo/súplica o a intrusión/culpa"
  - beat_id: "C08_D_B03"
    trigger_window: "tramo medio, cuando el jugador intenta ordenar restos del día o del piso"
    source: "TV / historial mezclado"
    format: "línea residual, continuidad obscena, presentador/a que roba tono ajeno o frase de compañía que ya no acompaña"
    short_description: "la TV ya no introduce un tema; remezcla el historial y le quita al jugador la prioridad de interpretación."
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "salón y pasillo quedan cosidos semánticamente al umbral"
      - "si se deja encendida, sube mezcla y capacidad de la criatura para devolver frases"
      - "si se apaga, baja el ruido pero el silencio del piso gana una crudeza brutal"
  - beat_id: "C08_D_B04"
    trigger_window: "tarde o momento previo a preparar la noche"
    source: "Último eco dominante del historial (Editor / Amigo / Pareja/Ex según partida)"
    format: "mensaje breve, historial, llamada perdida o audio reescuchado"
    short_description: "una última línea humana reabre el tono con el que el jugador ha tratado al mundo: exigencia, banalidad, intimidad o cuidado."
    player_options:
      - direct
      - evasive
      - delay
      - silence
    main_effects:
      - "fija el sesgo relacional principal del diálogo final"
      - "si se afronta, el jugador llega menos negado pero más expuesto"
      - "si se esquiva, la criatura hereda mejor el residuo"

contamination:
  primary_focus:
    zone: "Puerta atrancada / pasillo"
    material_form: "marco más cedido, humedad organizada, hendiduras, madera menos doméstica, aire retenido, presión térmica o frase abortada en el borde"
    emotional_cause: "historial total de omisiones, respuestas, sacrificios y formas de trato"
    escalation_if_ignored: "ya no crece sólo anatomía; se endurece la lectura que la criatura hace del jugador"
  secondary_focus:
    zone: "Zona dominante según historial"
    material_form: "salón medido, baño saturado, dormitorio doliente, entrada vigilante, cocina digestiva o balcón expuesto"
    emotional_cause: "la resolución final no nace del pasillo solo; nace del modo en que el piso entero ha sido repartido"
    escalation_if_ignored: "vuelve el diálogo final más unilateral, más hostil o más confuso"

containment_offer:
  is_available: true
  action: "última preparación del umbral o del cuerpo: despejar el pasillo, cerrar/apagar la TV, comer algo, lavarse la cara, retirar un residuo, coger un objeto-signo, abrir una ventana, guardar el móvil o llevarlo consigo"
  location: "pasillo/puerta, baño/dormitorio o salón"
  time_cost: "medium_high"
  emotional_cost: "todo gesto ya parece ceremonial; no arregla, sólo define cómo llegas"
  outcome_logic:
    - "si el jugador ordena el umbral, gana legibilidad y algo de agencia para confrontar"
    - "si atiende el cuerpo, llega menos roto pero más íntimamente expuesto"
    - "si apaga TV/móvil, baja manipulación externa pero sube desnudez del encuentro"
    - "si no hace nada, la resolución tenderá a absorción caótica o a hostilidad menos negociable"

pre_threshold_actions:
  - action: "hablarle a la puerta sin abrir"
    purpose: "medir respuesta y sembrar el tono del diálogo final"
  - action: "apoyar la mano en el marco"
    purpose: "aceptar que el umbral ya es cuerpo compartido"
  - action: "recoger un objeto vincular"
    purpose: "llevar al encuentro un sesgo humano explícito"
  - action: "quitar una obstrucción del pasillo"
    purpose: "decidir si el encuentro será contención o invitación"

cycle_truth: "La resolución no consiste en derrotar algo que estaba fuera de la vida del jugador, sino en responder por fin a aquello que su vida ha terminado de organizar."
```

---

## 2. Secuencia de presión recomendada

1. **Confirmación diurna del umbral**. La puerta o el pasillo ya devuelven presencia en pleno día.
2. **Última irrupción del cuerpo**. Madre o cuerpo recuerdan que la resolución también es corporal.
3. **Última contaminación interpretativa**. TV o móvil mezclan el historial.
4. **Último eco humano dominante**. Una voz concreta fija el tono emocional de la noche.
5. **Preparación del umbral**. El jugador decide cómo llega: sucio, ordenado, anestesiado, expuesto, armado con palabra u oculto tras silencio.
6. **Cierre del día**. Ya no se cierra para seguir gestionando; se cierra para entrar en la resolución.

---

## 3. Reglas de dirección para el día

### 3.1. No épica de final
Nada de “ahora sí, ahora empieza lo importante”. Lo importante lleva ahí desde el principio; ahora se vuelve inaplazable.

### 3.2. Todo debe oler a historial
Cada gesto del día tiene que recordar que la criatura final no es un giro nuevo, sino una coagulación del juego entero.

### 3.3. El umbral ya manda, pero el piso entero responde
No se trata de pasillo versus resto de zonas; se trata de un apartamento completo empujando hacia la puerta.

### 3.4. La última preparación importa moralmente
La forma en que el jugador ordena, evita, apaga, recoge, se cuida o habla antes de la noche debe alterar el tono del encuentro final.

---

## 4. Notas de continuidad

- Si el monstruo viene muy **doliente / suplicante**, el día debe permitir una llegada más íntima, menos militar y más cargada de cuidado o vergüenza.
- Si viene muy **rencoroso / furioso**, el pasillo y el marco deben sentirse más tensos, menos negociables y más deudores del sacrificio de C07.
- Si viene muy **imitativo / famélico**, el día debe dejar más mezcla, más TV, más móvil y más residuos verbales abiertos.
- El encuentro final no debe sentirse como un salto de género; debe sentirse como la consecuencia más lógica y más indecente del juego.

---

## 5. Cierre de diseño

El octavo día no remata una trama. **Remata una relación**: la relación entre el jugador y aquello que ha ido engendrando al tratar al piso, al cuerpo y a los demás como podía, como quería o como le salía de los cojones cuando ya no podía más.
