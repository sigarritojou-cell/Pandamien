# PANDAMIEN — ANEXO P.6
## Árbol authored base de confrontación final v01
### Derivado del GDD Maestro v06, del Plan de Acción Maestro v05, del Anexo H v01, del Anexo P v01, del Anexo P.1 v02, del Anexo P.2 v01, del Anexo P.3 v01 y del Anexo P.5 v01

---

## 0. Estado del anexo

Este documento convierte la confrontación final en un **árbol authored base implementable**.

Si:
- el **Anexo P** definía la arquitectura general,
- el **Anexo P.1** fijaba perfiles de confrontación,
- el **Anexo P.2** fijaba verbos y respuestas,
- el **Anexo P.3** fijaba familias de cierre,
- y el **Anexo P.5** proponía escenas maestras,

este anexo responde a la pregunta de producción real:

**¿Cómo se estructura la confrontación final como árbol jugable con nodos, condiciones, locks, transiciones y cierres compatibles?**

Su función es fijar:
- la arquitectura nodal mínima del final,
- qué variables lee,
- cómo se selecciona escena maestra y perfil principal,
- qué nodos son obligatorios,
- qué nodos son contextuales,
- qué locks y thresholds gobiernan la ramificación,
- y cómo desemboca cada rama en una familia de cierre.

No pretende cerrar aquí todos los diálogos definitivos.  
Sí deja el final preparado para:
- diseño narrativo fino,
- implementación,
- prototipado,
- test de variantes,
- y futura escritura de líneas finales exactas.

---

## 1. Principio rector

La confrontación final de PANDAMIEN no debe funcionar como:
- un menú de endings,
- un combate en fases,
- ni un árbol de diálogo clásico con colores morales.

Debe funcionar como un **árbol de presión y trato** donde:
- el perfil de criatura condiciona qué clase de escena se activa,
- el jugador usa pocos verbos muy pesados,
- y la rama final emerge de la combinación entre historial acumulado y decisión final.

La regla maestra es:

**Un árbol pequeño, denso y reversible al principio; irreversible al final.**

---

## 2. Entradas sistémicas obligatorias

Antes de entrar al árbol final, el sistema debe calcular estas lecturas:

## 2.1. Lectura de perfil principal
`final_profile_main`
Valores posibles:
- P01 Doliente Torácico
- P02 Medidor Funcional
- P03 Observador de Umbral
- P04 Hambriento Parlanchín
- P05 Razonable Torcido
- P06 Súplica de Marco
- P07 Rencor de Trayecto
- P08 Archivo Mal Cosido
- P09 Cuidado Intrusivo
- P10 Borde que te sabe

## 2.2. Lectura de matiz secundario
`final_profile_tint`
Valores posibles:
- none
- tv_editorial
- exterioridad
- intimo_pareja_ex
- clinico_materno

## 2.3. Lectura de familia de escena maestra
`final_scene_master`
Valores base v01:
- EM01 La mano y el latido
- EM02 La rendija que responde
- EM03 El informe de carne
- EM04 El borde que ya te sabía
- EM05 La casa no calla sola

## 2.4. Lectura de familia de cierre preferente
`final_closure_family_preferred`
Valores:
- C01 Contención ética
- C02 Apertura íntima
- C03 Convivencia podrida
- C04 Absorción
- C05 Rechazo / fractura
- C06 Umbral perpetuo

## 2.5. Variables de umbral
- `door_pressure`
- `frame_reactivity`
- `threshold_intelligence`
- `release_threshold`

## 2.6. Variables de vínculo final con la criatura
- `bond_intimacy_with_player`
- `bond_hostility_to_player`
- `bond_trust_to_player`
- `bond_dependence_on_player`

## 2.7. Variables verbales
- `lang_capacity`
- `lang_coherence`
- `lang_mix_index`
- `lang_addressivity`
- `lang_memory_depth`

---

## 3. Arquitectura general del árbol

La confrontación final se compone de seis capas nodales:

1. **Nodo de entrada**
2. **Nodo de reconocimiento**
3. **Nodo de trato inicial**
4. **Nodo de presión/verdad**
5. **Nodo irreversible**
6. **Nodo de cierre**

Cada capa puede tener:
- un nodo obligatorio,
- uno o dos nodos variantes,
- y transiciones condicionadas por perfil, verbo o threshold.

---

## 4. Variables temporales de escena

Durante el árbol final se usan variables de escena acumulativas.

## 4.1. `final_listen_depth`
Sube cuando el jugador:
- escucha,
- calla con intención,
- se queda,
- o se aproxima sin cortar la escena.

## 4.2. `final_contact_depth`
Sube cuando el jugador:
- toca el marco,
- se acerca,
- abre o cede,
- o sostiene tacto.

## 4.3. `final_truth_depth`
Sube cuando el jugador:
- admite,
- responde directo,
- deja de mentir,
- reconoce vínculo o deuda.

## 4.4. `final_denial_depth`
Sube cuando el jugador:
- niega,
- corta,
- se retira,
- responde defensivo,
- o intenta reinstalar ficción de no-vínculo.

## 4.5. `final_irreversibility`
Sube cuando el jugador:
- abre,
- cede,
- toca demasiado,
- cruza cierta cercanía,
- o activa una escena authored fuerte.

## 4.6. `final_creature_clarity`
Sube cuando la criatura:
- articula mejor,
- se hace más legible,
- o usa memoria del historial con mayor precisión.

---

## 5. Reglas de selección de escena maestra

## 5.1. Prioridad de escenas base v01

### EM01 — La mano y el latido
Se selecciona si:
- `func_heart` dominante,
- `temper_doliente` dominante,
- `bond_intimacy_with_player` alto,
- hostilidad no extrema.

### EM02 — La rendija que responde
Se selecciona si:
- `temper_reasonable` dominante,
- `lang_capacity` alta,
- `func_voice` alta,
- `creature_cohesion` alta.

### EM03 — El informe de carne
Se selecciona si:
- `temper_resentful` dominante,
- editor/trabajo muy altos,
- `func_voice` alta,
- hostilidad alta.

### EM04 — El borde que ya te sabía
Se selecciona si:
- `threshold_intelligence` muy alta,
- `func_eyes` alta,
- umbral dominante,
- ambivalencia alta.

### EM05 — La casa no calla sola
Se selecciona si:
- `lang_mix_index` alta,
- varios vínculos muy activos,
- TV importante,
- mezcla verbal marcada.

## 5.2. Regla de desempate
Si dos escenas empatan:
1. gana la que mejor exprese el perfil principal;
2. si siguen empatadas, gana la que mejor use el eje espacial dominante;
3. si aún empatan, priorizar la escena más específica y menos genérica.

---

## 6. Esqueleto nodal mínimo

## 6.1. Nodo N00 — Entrada al umbral
Función:
- colocar al jugador en la escena,
- fijar espacio,
- activar tono dominante,
- cargar el borde sin decidir aún trato.

Obligatorio:
- sí

Inputs disponibles:
- escuchar
- acercarse
- callar
- retirarse

Salidas:
- N10 Reconocimiento corporal
- N11 Reconocimiento verbal
- N12 Reconocimiento de borde

Selección:
- según perfil y `lang_capacity`

---

## 6.2. Nodo N10 / N11 / N12 — Reconocimiento

### N10 — Reconocimiento corporal
Mejor para:
- P01
- P06
- P09

Señales:
- respiración,
- latido,
- calor,
- marco vivo.

### N11 — Reconocimiento verbal
Mejor para:
- P02
- P05
- P08

Señales:
- frase rota,
- llamada clara,
- línea devuelta.

### N12 — Reconocimiento de borde
Mejor para:
- P03
- P07
- P10

Señales:
- pausa,
- foco,
- peso del pasillo,
- corrección de timing.

Salidas:
- N20 Trato inicial
- N21 Trato evasivo
- N22 Trato de espera

---

## 6.3. Nodo N20 / N21 / N22 — Trato inicial

### N20 — Trato inicial abierto
Se activa si el jugador:
- escucha
- responde
- admite
- se acerca sin cortar

### N21 — Trato inicial evasivo
Se activa si el jugador:
- calla
- responde mínimo
- duda
- retira un poco

### N22 — Trato inicial hostil / borde
Se activa si el jugador:
- niega
- se retira
- corta
- responde defensivo

Salidas:
- N30 Presión de verdad
- N31 Presión de cuerpo
- N32 Presión de juicio
- N33 Presión de umbral

Selección según perfil principal.

---

## 6.4. Nodo N30 / N31 / N32 / N33 — Presión principal

### N30 — Presión de verdad
Perfiles ideales:
- P05
- P08
- P02
- P01

Función:
- hacer que la criatura use memoria, deuda o verdad no dicha.

### N31 — Presión de cuerpo
Perfiles ideales:
- P01
- P06
- P09
- P04

Función:
- empujar contacto, latido, hambre, tactilidad o respiración.

### N32 — Presión de juicio
Perfiles ideales:
- P02
- P05
- P07

Función:
- devolver medida, retraso, mentira o patrón de daño.

### N33 — Presión de umbral
Perfiles ideales:
- P03
- P07
- P10

Función:
- convertir el borde en decisión real.

Salidas:
- N40 Nodo de contacto
- N41 Nodo de admisión/negación
- N42 Nodo de apertura potencial
- N43 Nodo de contención potencial

---

## 6.5. Nodo N40 / N41 / N42 / N43 — Nudo de jugador

### N40 — Contacto
Inputs dominantes:
- tocar el marco
- acercarse
- sostener tacto
- abrir parcial

### N41 — Verdad
Inputs dominantes:
- admitir
- negar
- responder directo
- responder defensivo

### N42 — Apertura
Inputs dominantes:
- abrir
- ceder
- no retirar la mano
- mantener rendija

### N43 — Contención
Inputs dominantes:
- contener
- escuchar
- callar con cuidado
- sostener sin abrir

Salidas:
- N50 Irreversible de apertura
- N51 Irreversible de contención
- N52 Irreversible de fractura
- N53 Irreversible de suspensión
- N54 Irreversible de absorción

---

## 6.6. Nodo irreversible

Este nodo fija el cierre.  
A partir de aquí ya no se debe volver a ramas blandas.

### N50 — Irreversible de apertura
Empuja:
- C02
- C04

### N51 — Irreversible de contención
Empuja:
- C01
- C03

### N52 — Irreversible de fractura
Empuja:
- C05

### N53 — Irreversible de suspensión
Empuja:
- C06

### N54 — Irreversible de absorción
Empuja:
- C04
- C03 en algunas versiones mixtas

Salidas:
- N90 Cierre final

---

## 6.7. Nodo N90 — Cierre
Función:
- staging final,
- línea o silencio final,
- imagen final,
- estado del apartamento,
- persistencia ética de la relación.

---

## 7. Esquema de transiciones base

```yaml
N00:
  on_listen: [N10, N11, N12]
  on_approach: [N10, N11, N12]
  on_silence: [N10, N12]
  on_retreat: [N12]

N10:
  on_listen: N20
  on_touch_frame: N40
  on_silence: N21
  on_retreat: N22

N11:
  on_respond: N20
  on_admit: N41
  on_deny: N41
  on_silence: N21
  on_retreat: N22

N12:
  on_listen: N22
  on_approach: N20
  on_retreat: N21
  on_touch_frame: N40

N20:
  to_pressure:
    - N30
    - N31
    - N32
    - N33

N21:
  to_pressure:
    - N30
    - N31
    - N33

N22:
  to_pressure:
    - N32
    - N33

N30:
  on_admit: N41
  on_respond: N41
  on_touch_frame: N40
  on_open: N42
  on_contain: N43

N31:
  on_touch_frame: N40
  on_admit: N41
  on_open: N42
  on_contain: N43
  on_retreat: N52

N32:
  on_deny: N52
  on_admit: N41
  on_respond: N41
  on_contain: N43
  on_open: N50

N33:
  on_approach: N40
  on_open: N42
  on_contain: N43
  on_silence: N53
  on_retreat: N52

N40:
  if_contact_depth_high_and_open: N50
  if_contact_depth_high_and_contain: N51
  if_contact_depth_high_and_no_decision: N53
  if_contact_depth_extreme_and_profile_absorption: N54

N41:
  if_truth_depth_high_and_admit: N51
  if_truth_depth_high_and_open: N50
  if_denial_depth_high: N52
  if_mix_and_intimacy_extreme: N54

N42:
  if_profile_allows_opening: N50
  if_profile_absorption_and_irreversibility_high: N54
  if_opening_as_break: N52

N43:
  if_profile_accepts_containment: N51
  if_profile_rejects_containment_and_hostility_high: N52
  if_profile_threshold_and_no_resolution: N53
```

---

## 8. Locks y thresholds

## 8.1. Locks principales

### `LOCK_OPENING_FORBIDDEN`
Se activa si:
- masa/cohesión demasiado bajas para que abrir tenga sentido authored,
- o el perfil es demasiado de borde aún.

Efecto:
- “abrir” no aparece o aparece como intento fallido no determinante.

### `LOCK_FULL_DIALOGUE`
Se activa si:
- `lang_capacity` baja,
- `lang_coherence` muy baja.

Efecto:
- el árbol se apoya más en cuerpo, gesto y silencio.

### `LOCK_COMPASSION_PATH`
Se activa si:
- hostilidad extrema,
- confianza casi nula,
- mentira y negación muy altas.

Efecto:
- reduce acceso a cierres de contención ética tierna o apertura íntima amable.

### `LOCK_ABSORPTION_PATH`
Se activa si:
- irreversibilidad no suficiente,
- poca mezcla o poca intimidad.

Efecto:
- impide C04 aunque el jugador abra.

### `LOCK_PERPETUAL_THRESHOLD`
Se activa si:
- el jugador ya ha cruzado demasiado claramente,
- o la escena exige resolución más dura.

Efecto:
- impide C06.

## 8.2. Thresholds principales

### `THR_LISTEN_HIGH`
Se alcanza cuando:
- `final_listen_depth >= 2`

### `THR_TRUTH_HIGH`
Se alcanza cuando:
- `final_truth_depth >= 2`

### `THR_DENIAL_HIGH`
Se alcanza cuando:
- `final_denial_depth >= 2`

### `THR_CONTACT_HIGH`
Se alcanza cuando:
- `final_contact_depth >= 2`

### `THR_IRREVERSIBLE`
Se alcanza cuando:
- `final_irreversibility >= 2`

### `THR_CREATURE_CLEAR`
Se alcanza cuando:
- `final_creature_clarity >= 2`

---

## 9. Árboles base por escena maestra

A continuación se proponen esqueletos concretos para las cinco escenas maestras de v01.

---

# 9.1. Árbol base EM01 — La mano y el latido

```yaml
scene_id: "EM01"
profile_main: "P01"
entry_node: "N00"
flow:
  - N00 -> N10
  - N10 -> [N20, N21, N22]
  - N20 -> N31
  - N21 -> N31
  - N22 -> [N32, N33]
  - N31 -> [N40, N41, N43]
  - N40 -> [N50, N51, N53]
  - N41 -> [N51, N52]
  - N43 -> [N51, N53]
preferred_closures:
  - C01
  - C02
  - C06
```

Regla authored:
- si el jugador toca el marco y luego contiene/admite, priorizar **C01**.
- si toca y abre con intimidad alta, priorizar **C02**.
- si escucha mucho pero no cruza, priorizar **C06**.

---

# 9.2. Árbol base EM02 — La rendija que responde

```yaml
scene_id: "EM02"
profile_main: "P05"
entry_node: "N00"
flow:
  - N00 -> N11
  - N11 -> [N20, N21, N22]
  - N20 -> N30
  - N21 -> [N30, N32]
  - N22 -> N32
  - N30 -> [N41, N42, N43]
  - N32 -> [N41, N52]
  - N42 -> [N50, N54]
  - N43 -> [N51, N52]
preferred_closures:
  - C02
  - C01
  - C04
  - C05
```

Regla authored:
- si el jugador responde/admite y luego abre parcial, priorizar **C02**.
- si admite y contiene, priorizar **C01**.
- si abre con irreversibilidad alta y perfil verbal alto, habilitar **C04**.
- si niega con perfil hostil, caer a **C05**.

---

# 9.3. Árbol base EM03 — El informe de carne

```yaml
scene_id: "EM03"
profile_main: "P02"
entry_node: "N00"
flow:
  - N00 -> N11
  - N11 -> [N20, N21, N22]
  - N20 -> N32
  - N21 -> N32
  - N22 -> N32
  - N32 -> [N41, N43, N52]
  - N41 -> [N51, N52]
  - N43 -> [N51, N52]
preferred_closures:
  - C05
  - C01
  - C02
```

Regla authored:
- la negación pesa muchísimo.
- si el jugador niega o corta, priorizar **C05**.
- si admite sin abrir, puede ir a **C01** dura.
- si abre desde hostilidad o culpa, puede ir a **C02** hostil.

---

# 9.4. Árbol base EM04 — El borde que ya te sabía

```yaml
scene_id: "EM04"
profile_main: "P10"
entry_node: "N00"
flow:
  - N00 -> N12
  - N12 -> [N20, N21, N22]
  - N20 -> N33
  - N21 -> N33
  - N22 -> N33
  - N33 -> [N40, N42, N43, N53]
  - N40 -> [N50, N53]
  - N42 -> [N50, N54]
  - N43 -> [N51, N53]
preferred_closures:
  - C06
  - C02
  - C01
  - C04
```

Regla authored:
- si el jugador escucha, se acerca y no decide, priorizar **C06**.
- si toca y luego contiene, priorizar **C01** de borde.
- si abre con umbral muy alto, priorizar **C02** o **C04** según irreversibilidad.

---

# 9.5. Árbol base EM05 — La casa no calla sola

```yaml
scene_id: "EM05"
profile_main: "P08"
entry_node: "N00"
flow:
  - N00 -> N11
  - N11 -> [N20, N21]
  - N20 -> N30
  - N21 -> [N30, N32]
  - N30 -> [N41, N42, N43]
  - N32 -> [N41, N52]
  - N42 -> [N50, N54]
  - N43 -> [N51, N54]
preferred_closures:
  - C04
  - C03
  - C01
  - C05
```

Regla authored:
- si el jugador admite y cede, activar **C04**.
- si contiene sin negar del todo, activar **C03**.
- si niega agresivamente, activar **C05** con mezcla verbal residual.

---

## 10. Nodos authored mínimos obligatorios

Para MVP del final, cada ruta implementada debe contener al menos:

1. **1 nodo de reconocimiento**
2. **1 nodo de presión**
3. **1 nodo de verbo duro**
4. **1 nodo irreversible**
5. **1 nodo de imagen/sonido final**

No hace falta que todos los finales tengan muchísimos nodos.  
La densidad importa más que la cantidad.

---

## 11. Formato recomendado de nodo authored

```yaml
node_id: "P6_NODE_EXAMPLE_01"
scene_master: "EM02"
profile_main: "P05"
closure_bias: "C02"
node_type: "pressure_truth"
space_focus: ["hallway", "sealed_door"]
creature_mode: "voice_reasonable"
trigger_conditions:
  - "lang_capacity >= 3"
  - "final_truth_depth >= 1"
  - "final_denial_depth <= 1"
player_inputs:
  - "respond"
  - "admit"
  - "deny"
  - "silence"
text_seed: "La criatura devuelve una frase precisa pero incompleta."
effects:
  final_listen_depth: 0
  final_truth_depth: +1
  final_denial_depth: 0
  final_irreversibility: 0
  final_creature_clarity: +1
locks_applied: []
transitions:
  on_respond: "P6_NODE_EXAMPLE_02"
  on_admit: "P6_NODE_EXAMPLE_03"
  on_deny: "P6_NODE_EXAMPLE_04"
  on_silence: "P6_NODE_EXAMPLE_05"
```

---

## 12. Reglas de escritura del árbol

## 12.1. Regla de un gesto dominante por nodo
Cada nodo debe tener:
- una acción del jugador dominante,
- una respuesta dominante de criatura,
- y una sensación dominante.

## 12.2. Regla de no saturación verbal
Si el perfil no lo soporta, la criatura debe responder:
- con aire,
- peso,
- latido,
- timing,
- tacto,
- o silencio.

## 12.3. Regla de continuidad espacial
El espacio no puede cambiar de forma arbitraria entre nodos.  
Cada transición debe sentirse como desplazamiento real dentro del régimen del apartamento.

## 12.4. Regla de consecuencia acumulativa
Los verbos del jugador en el final deben notarse enseguida:
- en la voz,
- en el marco,
- en el pasillo,
- en la proximidad,
- o en la familia de cierre a la que ya se está inclinando la escena.

---

## 13. Prioridad de implementación

## 13.1. MVP recomendado
Implementar primero estas ramas completas:

- **EM01 → C01**
- **EM02 → C02**
- **EM03 → C05**
- **EM04 → C06**

Porque cubren:
- contención íntima,
- apertura dialogada,
- fractura dura,
- y suspensión de umbral.

## 13.2. Escalado posterior
Añadir después:
- EM05 → C04
- EM05 → C03
- EM02 → C04
- EM01 → C02

---

## 14. Qué falta después de P.6

Una vez exista este árbol base, lo siguiente ya no es estructural grueso, sino:
- escritura nodal fina,
- líneas finales exactas,
- staging implementado,
- y consolidación canónica.

Documentos naturales siguientes:
- **P.7 — Banco de nodos finales y líneas exactas**
- **P.8 — Locks, condiciones y pseudológica de implementación**
- o consolidación directa si decidimos que ya hay suficiente para subir al maestro.

---

## 15. Cierre de dirección

Con este anexo, la confrontación final deja de ser “una buena idea muy bien escrita” y se convierte por fin en:
- un árbol,
- un sistema,
- una máquina de trato,
- y una estructura implementable.

Eso era lo importante.

Que al llegar a la puerta final no tengamos sólo un discurso bonito,  
sino una arquitectura capaz de sostener la peor verdad del juego:

**que el monstruo no sólo depende de lo que has hecho, sino también de cómo eliges tratarlo cuando por fin ya no puedes seguir llamándolo sólo puerta.**
