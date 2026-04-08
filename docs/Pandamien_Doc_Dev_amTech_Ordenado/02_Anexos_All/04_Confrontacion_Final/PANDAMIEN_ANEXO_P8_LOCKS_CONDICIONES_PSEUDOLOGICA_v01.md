# PANDAMIEN — ANEXO P.8
## Locks, condiciones y pseudológica de implementación final v01
### Derivado del GDD Maestro v06, del Plan de Acción Maestro v05, del Anexo H v01, del Anexo P v01, del Anexo P.1 v02, del Anexo P.2 v01, del Anexo P.3 v01, del Anexo P.6 v01 y del Anexo P.7 v01

---

## 0. Estado del anexo

Este documento cierra el bloque técnico-autoral base de la confrontación final.

Si:
- el **Anexo P** definía la arquitectura del careo final,
- el **Anexo P.1** fijaba perfiles,
- el **Anexo P.2** fijaba verbos y respuestas,
- el **Anexo P.3** fijaba familias de cierre,
- el **Anexo P.6** fijaba el árbol base implementable,
- y el **Anexo P.7** fijaba nodos y líneas exactas,

este anexo responde a la pregunta de implementación real:

**¿Qué locks, condiciones, thresholds y reglas de montaje necesita el final para funcionar como sistema authored controlado y no como una masa informe de ramas imposibles?**

Su función es fijar:
- condiciones de entrada al bloque final,
- orden de evaluación,
- locks duros y blandos,
- thresholds mínimos,
- reglas de selección de perfil/escena/cierre,
- pseudológica base de runtime,
- prioridades de implementación,
- y criterios de test.

No sustituye a los otros anexos del bloque final.  
Los vuelve montables.

---

## 1. Principio rector

La confrontación final debe sentirse variable, pero no arbitraria.

Eso exige tres cosas:

1. **pocas lecturas maestras, bien definidas**;
2. **locks claros**, para que no todos los finales estén abiertos siempre;
3. **orden fijo de evaluación**, para que el sistema no se contradiga.

Regla central:
**primero se lee qué criatura hay; luego cómo trata al jugador; luego qué hace el jugador en el final; y sólo entonces se fija el cierre.**

No al revés.

---

## 2. Pipeline de evaluación final

El bloque final debe evaluarse en este orden:

### Etapa 01 — Snapshot de partida
Congelar variables relevantes al entrar al final.

### Etapa 02 — Lectura de criatura
Determinar:
- perfil principal,
- matiz secundario,
- familia verbal,
- eje espacial dominante.

### Etapa 03 — Selección de escena maestra
Asignar una escena base de confrontación.

### Etapa 04 — Aplicación de locks
Cerrar rutas incompatibles antes de arrancar el árbol.

### Etapa 05 — Ejecución del árbol final
Leer verbos, acumular variables de escena y conducir a nodo irreversible.

### Etapa 06 — Selección de cierre
Fijar familia de cierre según:
- perfil,
- verbo duro dominante,
- truth/denial/contact/irreversibility,
- locks activos.

### Etapa 07 — Remate authored
Seleccionar:
- staging,
- imagen final,
- frase o silencio,
- estado del apartamento post-cierre.

---

## 3. Snapshot de partida obligatorio

Antes de cargar la confrontación final, el sistema debe guardar en una estructura inmutable los valores relevantes.

## 3.1. Snapshot mínimo recomendado

```yaml
final_snapshot:
  creature:
    mass: 0
    cohesion: 0
    visibility_index: 0
    func_voice: 0
    func_eyes: 0
    func_legs: 0
    func_stomach: 0
    func_skin: 0
    func_heart: 0
    func_lungs: 0
    temper_doliente: 0
    temper_imitative: 0
    temper_famished: 0
    temper_resentful: 0
    temper_supplicant: 0
    temper_furious: 0
    temper_reasonable: 0
  bond:
    intimacy: 0
    hostility: 0
    trust: 0
    dependence: 0
  language:
    capacity: 0
    coherence: 0
    mix_index: 0
    addressivity: 0
    memory_depth: 0
  threshold:
    door_pressure: 0
    frame_reactivity: 0
    threshold_intelligence: 0
    release_threshold: 0
  play_history:
    avoidance_total: 0
    confrontation_total: 0
    lies_total: 0
    silences_total: 0
    listen_total: 0
    care_total: 0
    containment_total: 0
    tv_dependence_total: 0
    edge_fixation_total: 0
  dominant_spaces:
    living: 0
    hallway: 0
    entry: 0
    bedroom: 0
    bathroom: 0
    kitchen: 0
    balcony: 0
    window: 0
  dominant_relations:
    mother: 0
    editor: 0
    friend: 0
    ex_partner: 0
    tv: 0
    exteriority: 0
```

## 3.2. Regla de congelación
Una vez empieza el final, este snapshot ya no cambia.  
Lo que cambia durante la escena son variables locales de confrontación.

---

## 4. Cálculo de perfil principal y matiz secundario

## 4.1. Perfil principal
Se calcula ponderando:
- función dominante de criatura,
- temperamento dominante,
- capacidad verbal,
- vínculo con jugador,
- eje espacial dominante.

## 4.2. Pseudológica base

```pseudo
if heart high and doliente high and intimacy high and hostility not extreme:
    profile_main = P01

elif voice high and resentful high and editor/history_delay high:
    profile_main = P02

elif eyes high and threshold_intelligence high and edge_fixation high:
    profile_main = P03 or P10
    if addressivity medium_or_high:
        profile_main = P10
    else:
        profile_main = P03

elif stomach high and famished high:
    profile_main = P04

elif voice high and cohesion high and reasonable high and lang_capacity high:
    profile_main = P05

elif dependence high and supplicant high and frame_reactivity medium_or_high:
    profile_main = P06

elif legs high and hostility high and (furious high or resentful high):
    profile_main = P07

elif mix_index high and memory_depth high and voice high:
    profile_main = P08

elif skin high and lungs medium_or_high and mother/body history high:
    profile_main = P09
```

## 4.3. Matiz secundario
Se calcula después del perfil principal.

```pseudo
if tv dominance high and mix_index medium_or_high:
    profile_tint = tv_editorial
elif exteriority dominance high or entry/hallway/window very high:
    profile_tint = exteriority
elif bedroom/balcony high and ex_partner dominance high:
    profile_tint = intimo_pareja_ex
elif bathroom/body high and mother dominance high:
    profile_tint = clinico_materno
else:
    profile_tint = none
```

## 4.4. Regla de desempate
Si dos perfiles empatan:
1. gana el más sostenido por función corporal;
2. luego el más sostenido por temperamento;
3. luego el más sostenido por eje espacial;
4. si siguen empatados, elegir el más específico y menos genérico.

---

## 5. Selección de escena maestra

## 5.1. Tabla base

- P01, P06, P09 → **EM01**
- P05 → **EM02**
- P02 → **EM03**
- P03, P10 → **EM04**
- P08, P04 → **EM05**

## 5.2. Excepciones controladas
- P05 con hostilidad muy alta puede usar estructura parcial de **EM03**.
- P10 con apertura alta puede tomar staging parcial de **EM02**.
- P04 con dependencia muy alta puede teñirse con ritmos de **EM01**.
- P08 con juicio muy alto puede injertar nodos de **EM03**.

Regla:
No cambiar escena maestra completa por capricho.  
Sólo contaminarla.

---

## 6. Variables locales de confrontación

Estas variables nacen a 0 y se modifican durante la escena.

```yaml
final_scene_state:
  listen_depth: 0
  contact_depth: 0
  truth_depth: 0
  denial_depth: 0
  irreversibility: 0
  creature_clarity: 0
  opening_commitment: 0
  containment_commitment: 0
  fracture_pressure: 0
  suspension_pressure: 0
```

## 6.1. Regla de lectura
No usar más de 10 variables locales.  
La escena tiene que ser legible.

## 6.2. Regla de feedback
Cada cambio de estas variables debe sentirse en:
- voz,
- marco,
- aire,
- pasillo,
- o disponibilidad de opciones.

---

## 7. Locks duros

Los locks duros bloquean rutas completas.

## 7.1. `LOCK_FULL_OPENING`
Bloquea apertura fuerte si:
- `release_threshold` bajo,
- `creature_mass` muy baja,
- `creature_cohesion` muy baja.

Razón:
no tendría sentido authored abrir “demasiado” si la criatura aún no soporta esa escena.

## 7.2. `LOCK_FULL_DIALOGUE`
Bloquea diálogo extendido si:
- `lang_capacity <= 1`
- o `lang_coherence` muy baja.

Efecto:
las respuestas se apoyan en:
- gesto,
- aire,
- ritmo,
- sílabas,
- golpe,
- latido.

## 7.3. `LOCK_COMPASSIONATE_CONTAINMENT`
Bloquea la versión más tierna de C01 si:
- `bond_hostility` muy alta,
- `bond_trust` casi nula,
- `lies_total` muy alta,
- `denial_total` muy alta.

Efecto:
puede haber contención, pero no dulce ni reconciliadora.

## 7.4. `LOCK_ABSORPTION`
Bloquea C04 si:
- `irreversibility < 2`
- y `contact_depth < 2`
- y `intimacy` no es alta
- y `mass/cohesion` no la sostienen.

## 7.5. `LOCK_PERPETUAL_THRESHOLD`
Bloquea C06 si:
- el jugador ya abrió de forma material fuerte,
- o ya activó irreversibilidad muy alta incompatible con suspensión.

## 7.6. `LOCK_HARD_FRACTURE`
Bloquea C05 fuerte si:
- hostilidad no suficiente,
- vínculo demasiado íntimo y dependiente,
- criatura claramente más doliente que agresiva,
- y el jugador no ha negado ni roto de forma clara.

---

## 8. Locks blandos

No bloquean totalmente; reducen probabilidad o mueven el tono.

## 8.1. `SOFTLOCK_TV_EDITORIAL`
Si activo:
- aumentar líneas de discurso organizado,
- staging con glow residual,
- y posibilidades de frase más medida.

## 8.2. `SOFTLOCK_EX_INTIMATE`
Si activo:
- subir peso de dormitorio/balcón,
- pecho, espera, aire, herida.

## 8.3. `SOFTLOCK_MOTHER_CLINICAL`
Si activo:
- subir cuerpo, baño, descanso, respiración, humedad, cuidado invasivo.

## 8.4. `SOFTLOCK_EDGE_PARANOIA`
Si activo:
- priorizar pasillo, orientación, espera, mirada, silencio atento.

---

## 9. Thresholds mínimos para familias de cierre

## 9.1. C01 — Contención ética
Requiere:
- `containment_commitment >= 1`
- `truth_depth >= 1` o `listen_depth >= 2`
- no tener `LOCK_COMPASSIONATE_CONTAINMENT` si se quiere la variante más íntima

## 9.2. C02 — Apertura íntima
Requiere:
- `opening_commitment >= 1`
- `irreversibility >= 2`
- no tener `LOCK_FULL_OPENING`

## 9.3. C03 — Convivencia podrida
Requiere:
- `containment_commitment >= 1`
- `opening_commitment <= 1`
- `suspension_pressure >= 1`
- vínculo mixto, no limpio

## 9.4. C04 — Absorción
Requiere:
- `irreversibility >= 2`
- `contact_depth >= 2` o `truth_depth >= 2`
- no tener `LOCK_ABSORPTION`

## 9.5. C05 — Rechazo / fractura
Requiere:
- `denial_depth >= 2` o `fracture_pressure >= 2`
- hostilidad media/alta
- no tener `LOCK_HARD_FRACTURE`

## 9.6. C06 — Umbral perpetuo
Requiere:
- `listen_depth >= 2`
- `opening_commitment == 0`
- `containment_commitment <= 1`
- `suspension_pressure >= 2`
- no tener `LOCK_PERPETUAL_THRESHOLD`

---

## 10. Modificación de variables por verbo

## 10.1. Escuchar
```yaml
listen_depth: +1
creature_clarity: +1 if profile verbal medium_or_high else 0
suspension_pressure: +1 if no hard decision yet
```

## 10.2. Responder
```yaml
truth_depth: +1 if direct
denial_depth: +1 if evasive/defensive
creature_clarity: +1
```

## 10.3. Callar
```yaml
listen_depth: +1 if held with intention
denial_depth: +1 if used as avoidance
suspension_pressure: +1
```

## 10.4. Acercarse
```yaml
contact_depth: +1
irreversibility: +1 if repeated
```

## 10.5. Retirarse
```yaml
denial_depth: +1
fracture_pressure: +1 if profile hostile
suspension_pressure: +1 if player keeps listening
```

## 10.6. Tocar el marco
```yaml
contact_depth: +2
irreversibility: +1
creature_clarity: +1
```

## 10.7. Abrir / ceder
```yaml
opening_commitment: +2
irreversibility: +2
contact_depth: +1
```

## 10.8. Contener
```yaml
containment_commitment: +2
truth_depth: +1 if non-denying containment
fracture_pressure: +1 if profile rejects containment
```

## 10.9. Negar
```yaml
denial_depth: +2
fracture_pressure: +1
```

## 10.10. Admitir
```yaml
truth_depth: +2
creature_clarity: +1
opening_commitment: +1 if admission paired with approach/opening
containment_commitment: +1 if admission paired with containment
```

---

## 11. Selector de cierre final

## 11.1. Orden de evaluación
Evaluar las familias de cierre en este orden:

1. ¿Se ha activado absorción fuerte?
2. ¿Se ha activado fractura fuerte?
3. ¿Se ha activado apertura?
4. ¿Se ha activado contención?
5. ¿Se ha activado convivencia?
6. ¿Queda umbral perpetuo?

Razón:
- absorción y fractura son más irreversibles;
- apertura y contención estructuran decisiones claras;
- convivencia y umbral perpetuo funcionan mejor como residuo de patrón.

## 11.2. Pseudológica base

```pseudo
if not LOCK_ABSORPTION and irreversibility >= 2 and contact_depth >= 2 and (
    profile_main in [P05, P08, P10, P07, P04] or truth_depth >= 2
):
    closure = C04

elif not LOCK_HARD_FRACTURE and (denial_depth >= 2 or fracture_pressure >= 2) and hostility medium_or_high:
    closure = C05

elif not LOCK_FULL_OPENING and opening_commitment >= 2:
    closure = C02

elif containment_commitment >= 2 and truth_depth >= 1:
    if mixed_dependency_or_domestic_pattern_high:
        closure = C03
    else:
        closure = C01

elif not LOCK_PERPETUAL_THRESHOLD and suspension_pressure >= 2 and opening_commitment == 0:
    closure = C06

else:
    # fallback controlado
    if profile_main in [P01, P06, P09]:
        closure = C01
    elif profile_main in [P03, P10]:
        closure = C06
    elif profile_main in [P02, P07]:
        closure = C05
    else:
        closure = C03
```

---

## 12. Selector de remate authored

Una vez fijado el cierre, seleccionar:

1. staging final,
2. imagen final,
3. dominante sonora,
4. frase o silencio final,
5. estado del apartamento.

## 12.1. Regla de selección
- primero manda el cierre,
- luego el perfil principal,
- luego el matiz secundario.

## 12.2. Ejemplo

```pseudo
if closure == C01 and profile_main == P01:
    staging = "A"
    final_image = "I01"
    final_sound = "heartbeat_breath"
    final_line = choose(P7_P01_END_01, P7_P01_END_03)

elif closure == C02 and profile_main == P05:
    staging = "C"
    final_image = "I02"
    final_sound = "breath_gap"
    final_line = choose(P7_P05_END_02, silence_short_costly)

elif closure == C05 and profile_main == P02:
    staging = "F"
    final_image = "I05_or_I09"
    final_sound = "dry_hit"
    final_line = choose(P7_P02_END_01, P7_P02_END_03)

elif closure == C06 and profile_main == P10:
    staging = "B_or_C"
    final_image = "I04"
    final_sound = "attentive_silence"
    final_line = choose(P7_P10_END_01, P7_P10_END_02)
```

---

## 13. Criterios de test del bloque final

## 13.1. Test de coherencia
Preguntas:
- ¿La criatura final parece hija de la partida?
- ¿El cierre parece merecido?
- ¿La escena usa bien el espacio?
- ¿La frase final no explica de más?

## 13.2. Test de diferencia perceptible
Entre dos partidas distintas, comprobar:
- perfil diferente,
- staging diferente,
- tono diferente,
- remate diferente.

## 13.3. Test de no caos
Comprobar que:
- no se mezclan demasiados perfiles,
- no se abren demasiadas rutas simultáneas,
- y el jugador no siente arbitrariedad gratuita.

## 13.4. Test de peso del verbo
Verificar que:
- tocar el marco no vale lo mismo que escuchar,
- negar no vale lo mismo que callar,
- abrir cambia de verdad la escena,
- y contener no se siente como opción burocrática.

## 13.5. Test de respiración de escena
Verificar que el final:
- no va demasiado deprisa,
- no se ahoga en texto,
- y permite que aire, marco, pasillo y silencio hagan trabajo.

---

## 14. Prioridad de implementación

## 14.1. MVP mínimo fuerte
Implementar primero:

- P01 + C01
- P05 + C02
- P02 + C05
- P10 + C06

Con:
- 1 escena maestra cada una,
- 1 ruta principal,
- 1 ruta alternativa,
- 1 frase/remate fuerte,
- 1 silencio fuerte.

## 14.2. Escalado posterior
Añadir después:
- P08 + C04
- P06 + C03
- P07 + C05/C04
- matices secundarios más finos
- hooks authored especiales

---

## 15. Qué hacer tras P.8

Después de este documento, el bloque final ya no necesita mucho más para estar listo de cara a canon.

Los movimientos naturales serían:
1. **Consolidación nueva del maestro**  
   para subir F, G, H y P–P.8 al cuerpo canónico.

2. **Auditoría transversal**  
   para revisar contradicciones, huecos, exceso de ramas y nomenclatura.

3. **Paquete de implementación**  
   si se quiere ya convertir esto en tareas de producción.

---

## 16. Cierre de dirección

Con P.8, el final deja de ser literatura de diseño y se convierte en:
- lógica,
- montaje,
- limitación,
- y posibilidad real de build.

Y eso es importante, porque PANDAMIEN no se puede permitir un final que dependa del entusiasmo del último día.  
Tiene que depender de una estructura que aguante el peso de todo lo que hemos estado criando detrás de la puerta.

Si este anexo está bien, el final ya no será “a ver cómo lo resolvemos luego”.  
Será una bestia atada con cadena corta, lista para que la soltemos justo lo suficiente.
