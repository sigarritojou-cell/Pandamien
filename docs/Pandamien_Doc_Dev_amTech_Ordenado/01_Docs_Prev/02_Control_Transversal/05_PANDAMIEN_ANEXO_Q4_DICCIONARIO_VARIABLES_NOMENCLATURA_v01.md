# PANDAMIEN — ANEXO Q.4
## Diccionario unificado de variables y nomenclatura v01
### Derivado del GDD Maestro v07, del Plan de Acción Maestro v06, del Anexo H v01, del bloque P–P.8 y de la Auditoría total v01

---

## 0. Estado del documento

Este documento abre el **Diccionario unificado de variables y nomenclatura** del proyecto.

Su función no es añadir diseño nuevo.  
Su función es impedir que el proyecto se parta por dentro porque:
- una misma idea reciba tres nombres,
- dos variables parecidas hagan trabajos casi idénticos,
- una familia cambie de prefijo según el anexo,
- o una palabra narrativa se use como si fuera una variable técnica.

Este anexo fija:

- convención oficial de nombres,
- familias de variables,
- distinción entre variables maestras y variables locales,
- equivalencias y términos prohibidos,
- mapeo entre lenguaje narrativo y lenguaje de implementación,
- y reglas para crear nuevas variables sin infectar el corpus con barro técnico.

---

## 1. Principio rector

En PANDAMIEN, una variable no es sólo una cifra.  
Es una promesa de diseño.

Si una variable existe, debe cumplir estas cuatro condiciones:

1. **nombra una cosa real del sistema**;
2. **no pisa otra variable ya existente**;
3. **puede leerse con claridad en authored e implementación**;
4. **sirve a producción**, no sólo a pensamiento abstracto.

Regla maestra:
**pocas familias, nombres limpios, semántica estable.**

---

## 2. Convención oficial de nombres

## 2.1. Idioma de variables
Las variables técnicas canónicas se fijan en **inglés simple**.

Razón:
- mayor limpieza para implementación,
- mejor consistencia con pseudológica,
- menos riesgo de duplicar nombres entre documentos narrativos y técnicos.

## 2.2. Idioma documental
La explicación, función y notas de diseño siguen en **español**.

## 2.3. Formato general
Usar siempre:
- minúsculas,
- snake_case,
- sin guiones,
- sin abreviaturas oscuras,
- sin nombres poéticos.

### Correcto
- `bond_intimacy_with_player`
- `door_pressure`
- `lang_mix_index`

### Incorrecto
- `intimidadJugador`
- `doorPressure`
- `mixSem`
- `vibraPuerta`

## 2.4. Regla de prefijos por familia
Toda variable debe pertenecer a una familia identificable por prefijo o dominio claro.

Familias oficiales:
- `creature_*`
- `func_*`
- `temper_*`
- `bond_*`
- `lang_*`
- `door_*`
- `frame_*`
- `threshold_*`
- `zone_*`
- `rel_*`
- `tv_*`
- `ext_*`
- `final_*`

## 2.5. Regla de singularidad
No crear dos variables para la misma idea con dos nombres distintos.

Ejemplo:
- si existe `bond_hostility_to_player`, no crear `player_hostility_from_creature` salvo necesidad real y diferenciada.

---

## 3. Tipos de variables del proyecto

Se distinguen cuatro tipos.

## 3.1. Variables maestras persistentes
Son las que viven a lo largo de la partida y definen estado profundo.

Ejemplos:
- criatura,
- vínculo,
- lenguaje,
- puerta,
- zonas,
- TV,
- exterioridad.

## 3.2. Variables authored de ciclo
Sirven para authored de día/noche/ciclos, pero no tienen por qué almacenarse como sistema global si no hace falta.

Ejemplos:
- peso de una presencia en un ciclo concreto,
- semilla de eco,
- foco de noche,
- bias de una escena.

## 3.3. Variables locales de confrontación
Nacen en el final y mueren en el final.

Ejemplos:
- `final_listen_depth`
- `final_contact_depth`

## 3.4. Flags y locks
No miden intensidad.  
Permiten o impiden rutas, assets o comportamientos.

Ejemplos:
- `lock_absorption`
- `lock_full_dialogue`

---

## 4. Familias maestras de variables

---

# 4.A. Familia de criatura

## 4.A.1. Variables globales de cuerpo
### `creature_mass`
Cuánta entidad física total ha acumulado la criatura.

### `creature_cohesion`
Cuánto se ha organizado su anatomía y su lógica corporal.

### `creature_visibility_index`
Qué tan cerca está de ser legible como cuerpo asumible.

## 4.A.2. Regla
Estas tres variables son estructurales.  
No sustituirlas por metáforas narrativas tipo:
- “presencia”,
- “densidad emocional”,
- “bicho_total”.

## 4.A.3. Términos narrativos equivalentes
- masa
- cohesión
- visibilidad / legibilidad corporal

---

# 4.B. Familia de funciones corporales

## Variables oficiales
- `func_voice`
- `func_eyes`
- `func_legs`
- `func_stomach`
- `func_skin`
- `func_heart`
- `func_lungs`
- `func_hands` (escalable / opcional)

## Regla
Estas variables nombran **capacidades anatómico-funcionales** de criatura.

No son:
- zonas,
- emociones,
- ni estilos de escena.

## Prohibiciones
No crear duplicados del tipo:
- `voice_level`
- `heart_presence`
- `breath_growth`
si ya estamos midiendo eso dentro de la familia `func_*`.

## Términos narrativos equivalentes
- voz
- ojos / foco
- piernas / trayecto
- estómago / hambre
- piel / membrana
- corazón / pecho
- pulmones / aire
- manos / tactilidad

---

# 4.C. Familia de temperamento

## Variables oficiales
- `temper_doliente`
- `temper_imitative`
- `temper_famished`
- `temper_resentful`
- `temper_supplicant`
- `temper_furious`
- `temper_reasonable`

## Regla
Temperamento = **cómo trata la criatura**, no qué puede hacer corporalmente.

## Prohibiciones
No mezclar temperamento con función.

Incorrecto:
- “latido suplicante” como variable.
Correcto:
- `func_heart` + `temper_supplicant`

---

# 4.D. Familia de vínculo con el jugador

## Variables oficiales
- `bond_intimacy_with_player`
- `bond_dependence_on_player`
- `bond_hostility_to_player`
- `bond_trust_to_player`

## Regla
Bond = relación específica criatura ↔ jugador.

No usar `intimacy`, `trust`, `hostility` sueltos salvo dentro de estructura local muy controlada.

## Términos narrativos equivalentes
- intimidad
- dependencia
- hostilidad
- confianza relativa

---

# 4.E. Familia de lenguaje

## Variables oficiales
- `lang_capacity`
- `lang_coherence`
- `lang_mix_index`
- `lang_addressivity`
- `lang_memory_depth`

## Regla
Estas variables miden capacidad verbal/semántica de criatura o sistema final.

## Diferencia interna
- `lang_capacity` = cuánto puede articular
- `lang_coherence` = cuánto puede sostener línea
- `lang_mix_index` = cuánto mezcla voces
- `lang_addressivity` = cuánto se dirige a ti
- `lang_memory_depth` = cuánta memoria vieja puede devolver

## Prohibiciones
No usar indistintamente:
- “claridad verbal”,
- “coherencia”,
- “capacidad de hablar”,
como si fueran lo mismo.

---

# 4.F. Familia de puerta, marco y umbral

## Variables oficiales
- `door_pressure`
- `frame_reactivity`
- `threshold_intelligence`
- `release_threshold`

## Regla
Estas variables miden el eje:
- puerta atrancada,
- marco,
- comportamiento del borde,
- posibilidad de cruce.

## Distinción clave
- `door_pressure` = presión ejercida o acumulada en el umbral
- `frame_reactivity` = cuánto responde el marco al jugador
- `threshold_intelligence` = inteligencia de uso del borde
- `release_threshold` = umbral de salida / confrontación / cruce

## Prohibiciones
No confundir:
- puerta,
- umbral,
- pasillo,
- borde,
como si fueran siempre la misma cosa.

---

# 4.G. Familia de zonas del apartamento

## Variables oficiales recomendadas
- `zone_living_contamination`
- `zone_hallway_contamination`
- `zone_entry_contamination`
- `zone_bedroom_contamination`
- `zone_bathroom_contamination`
- `zone_kitchen_contamination`
- `zone_balcony_contamination`
- `zone_window_contamination`

## Regla
Usar siempre formato:
`zone_<zona>_contamination`

## Prohibiciones
No alternar con:
- `contamination_bedroom`
- `bedroom_state`
- `zone_contamination_bedroom`
en el mismo nivel de sistema.

### Decisión canónica
Para documentación futura, priorizar:
`zone_bedroom_contamination`
y equivalentes.

## Nota
En corpus previo existen rastros del patrón invertido `zone_contamination_bedroom`.  
Esta auditoría decide migrar al patrón:
`zone_<zona>_contamination`

---

# 4.H. Familia de relaciones humanas

## Variables oficiales recomendadas
- `rel_mother_intensity`
- `rel_editor_intensity`
- `rel_friend_intensity`
- `rel_ex_partner_intensity`

Escalables adicionales:
- `rel_mother_debt`
- `rel_editor_debt`
- `rel_friend_noise`
- `rel_ex_partner_wound`

## Regla
La familia `rel_*` mide peso sistémico de cada vínculo durante la partida.

## Nota
No todo authored de relaciones necesita variable global.  
Pero cuando la necesite, usar prefijo `rel_`.

---

# 4.I. Familia TV

## Variables oficiales recomendadas
- `tv_influence`
- `tv_state`
- `tv_editorial_bias`
- `tv_manipulation_level`

## Estados canónicos de `tv_state`
- `comfort`
- `suggestion`
- `manipulation`
- `residual_confrontation`

## Regla
No usar “tele”, “tv_mode”, “screen_state”, “broadcast_state” indistintamente.  
Si es estado general, usar `tv_state`.

---

# 4.J. Familia de exterioridad

## Variables oficiales recomendadas
- `ext_pressure`
- `ext_ambiguity`
- `ext_vigilance_bias`
- `ext_social_noise`

## Regla
Exterioridad no es sólo ventana o mirilla.  
Es el conjunto de:
- rellano,
- puerta principal,
- patio,
- luces,
- balcón,
- calle,
- voces parciales.

---

# 4.K. Familia de confrontación final

## Variables locales oficiales
- `final_listen_depth`
- `final_contact_depth`
- `final_truth_depth`
- `final_denial_depth`
- `final_irreversibility`
- `final_creature_clarity`
- `final_opening_commitment`
- `final_containment_commitment`
- `final_fracture_pressure`
- `final_suspension_pressure`

## Regla
Estas variables sólo viven durante el bloque final.

## Prohibiciones
No reaprovecharlas como variables globales del juego.

---

## 5. Diccionario de términos narrativos → técnicos

| Término narrativo | Término técnico canónico |
|---|---|
| masa de criatura | `creature_mass` |
| cohesión del monstruo | `creature_cohesion` |
| legibilidad corporal | `creature_visibility_index` |
| voz de criatura | `func_voice` |
| mirada / foco | `func_eyes` |
| trayecto / piernas | `func_legs` |
| hambre / digestión | `func_stomach` |
| piel / membrana | `func_skin` |
| pecho / corazón | `func_heart` |
| aire / pulmones | `func_lungs` |
| hostilidad de criatura | `bond_hostility_to_player` o `temper_resentful` / `temper_furious` según contexto |
| intimidad con criatura | `bond_intimacy_with_player` |
| confianza | `bond_trust_to_player` |
| dependencia | `bond_dependence_on_player` |
| capacidad de hablar | `lang_capacity` |
| coherencia verbal | `lang_coherence` |
| mezcla de voces | `lang_mix_index` |
| dirección al jugador | `lang_addressivity` |
| memoria verbal | `lang_memory_depth` |
| presión de puerta | `door_pressure` |
| reactividad del marco | `frame_reactivity` |
| inteligencia de umbral | `threshold_intelligence` |
| umbral de cruce | `release_threshold` |
| contaminación de dormitorio | `zone_bedroom_contamination` |
| contaminación de baño | `zone_bathroom_contamination` |
| presión TV | `tv_influence` / `tv_manipulation_level` según caso |
| presión exterior | `ext_pressure` |
| escucha final | `final_listen_depth` |
| contacto final | `final_contact_depth` |
| verdad final | `final_truth_depth` |
| negación final | `final_denial_depth` |

---

## 6. Términos ambiguos que deben restringirse

## 6.1. “Presión”
Problema:
se usa para demasiadas cosas.

### Uso permitido
Sólo con apellido o contexto claro:
- presión de puerta,
- presión de editor,
- presión de final,
- presión de fractura.

### Uso prohibido
Decir sólo “sube la presión” sin especificar cuál.

---

## 6.2. “Amenaza íntima”
Problema:
demasiado narrativo para implementación.

### Decisión
Mantenerlo como lenguaje de lectura narrativa, no como variable técnica.

Si hace falta medirlo, descomponer en:
- `bond_intimacy_with_player`
- `temper_supplicant` / `temper_doliente`
- `func_heart`
- `func_lungs`

---

## 6.3. “Estabilidad”
Problema:
puede sonar a cordura, salud mental o equilibrio sistémico.

### Decisión
Restringir muchísimo su uso.
Si aparece en authored granular, debe migrarse luego a variables concretas de:
- vínculo,
- cuerpo,
- contaminación,
- o final.

No usar `stability` como gran variable maestra del proyecto.

---

## 6.4. “Creature growth”
Problema:
es demasiado general.

### Decisión
Sólo usarlo como comentario de diseño o atajo temporal en tablas gruesas.
Para sistema real, traducirlo a:
- `creature_mass`
- `creature_cohesion`
- función dominante correspondiente.

---

## 6.5. “Door pressure” vs “door reactivity”
Problema:
a veces se mezclan.

### Decisión
- `door_pressure` = empuje/peso/presión acumulada
- `frame_reactivity` = respuesta al jugador
No son intercambiables.

---

## 7. Variables candidatas a migración o limpieza

A partir de la revisión del corpus, estas familias suelen aparecer de forma inestable y deben normalizarse:

## 7.1. Variables de authored de ciclos
Rastros problemáticos:
- `avoidance`
- `confrontation`
- `social_debt`
- `guilt_noise`
- `loneliness_index`
- `threat_intimacy`
- `stability`

### Decisión
Se aceptan como **variables de authored local** en fichas antiguas, pero no como nomenclatura maestra final de implementación.

### Acción
En futuras pasadas, mapearlas a familias más limpias:
- vínculo,
- criatura,
- zonas,
- TV,
- exterior,
- final.

## 7.2. Variables de contaminación de zonas
Rastro inconsistente:
- `zone_contamination_bedroom`
- `zone_bedroom_contamination`

### Decisión
Canónica:
- `zone_bedroom_contamination`

Migrar resto a ese patrón.

---

## 8. Reglas para crear nuevas variables

Antes de crear una variable nueva, responder:

1. ¿Esta idea ya existe con otro nombre?
2. ¿Es maestra, local o authored puntual?
3. ¿Necesita de verdad vivir en sistema o basta con nota narrativa?
4. ¿Puede derivarse de dos variables ya existentes?
5. ¿Su prefijo deja claro su dominio?
6. ¿Su nombre aguanta bien en pseudocódigo y en documentación?

Si falla dos de estas preguntas, no crearla todavía.

---

## 9. Formato de ficha de variable canónica

```yaml
variable_name: "bond_intimacy_with_player"
family: "bond"
type: "persistent_master"
range: "0-5"
description: "Mide cuánto sabe la criatura de la intimidad del jugador y cuánta cercanía afectiva ha acumulado hacia él."
narrative_reading: "Intimidad monstruosa, conocimiento del pecho, dormitorio, herida y espera."
used_by:
  - "creature profile selection"
  - "final confrontation profile"
  - "closure selection"
do_not_confuse_with:
  - "bond_trust_to_player"
  - "temper_supplicant"
  - "func_heart"
```

---

## 10. Matriz rápida de uso por bloques

### Ciclos día/noche authored
Priorizar:
- `rel_*`
- `zone_*`
- `tv_*`
- `ext_*`
- comentarios authored locales

### Criatura
Priorizar:
- `creature_*`
- `func_*`
- `temper_*`
- `bond_*`
- `lang_*`

### Puerta / umbral
Priorizar:
- `door_*`
- `frame_*`
- `threshold_*`

### Confrontación final
Priorizar:
- `final_*`
- snapshot de criaturas/vínculos/lenguaje/umbral

---

## 11. Decisiones canónicas fuertes de esta primera pasada

1. El patrón oficial de zonas será:
   - `zone_<zona>_contamination`
2. `stability` deja de ser variable maestra recomendable.
3. `threat_intimacy` se mantiene sólo como lectura authored temporal, no como variable final deseable.
4. `creature_growth` no debe sobrevivir como variable gruesa si ya puede descomponerse.
5. `tv_state` queda fijado con:
   - `comfort`
   - `suggestion`
   - `manipulation`
   - `residual_confrontation`
6. El final usa sólo familia `final_*` para sus contadores locales.
7. La familia de relaciones humanas se nombra `rel_*`.
8. La familia de exterioridad se nombra `ext_*`.

---

## 12. Acciones derivadas inmediatas

Después de este diccionario, los movimientos sanos son:

1. revisar **Anexo C / D / E** y marcar variables authored antiguas que necesiten traducción;
2. revisar **P.6 / P.8** para asegurar consistencia plena con este diccionario;
3. abrir la **Q.5 — Matriz de cruce transversal por ciclos** usando ya esta nomenclatura;
4. después, abrir **Q.2 — Asset map y prioridades** con nombres limpios.

---

## 13. Cierre de dirección

Aquí no estamos escribiendo poesía.  
Estamos evitando que dentro de tres meses el proyecto hable de:
- hostilidad,
- rencor,
- presión,
- mirada,
- vínculo,
- borde,
- apertura,
- contacto
como si fueran lo mismo según le venga bien a cada documento.

Si este diccionario funciona, el proyecto gana algo muy poco sexy pero jodidamente valioso:

**deja de balbucear técnicamente.**

Y cuando una bestia como PANDAMIEN deja de balbucear por dentro, todo lo demás empieza a respirar mejor.
