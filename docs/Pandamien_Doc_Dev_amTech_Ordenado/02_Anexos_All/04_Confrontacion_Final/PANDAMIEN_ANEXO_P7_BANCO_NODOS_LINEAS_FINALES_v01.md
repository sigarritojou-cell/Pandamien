# PANDAMIEN — ANEXO P.7
## Banco de nodos finales y líneas exactas v01
### Derivado del GDD Maestro v06, del Plan de Acción Maestro v05, del Anexo P v01, del Anexo P.1 v02, del Anexo P.2 v01, del Anexo P.3 v01, del Anexo P.4 v01 y del Anexo P.6 v01

---

## 0. Estado del anexo

Este documento abre el banco de **nodos finales authored** y de **líneas exactas** para la confrontación final.

Si:
- el **Anexo P** definía la arquitectura del final,
- el **Anexo P.1** fijaba los perfiles de confrontación,
- el **Anexo P.2** fijaba verbos y respuestas,
- el **Anexo P.3** fijaba familias de cierre,
- el **Anexo P.4** fijaba staging e imágenes,
- y el **Anexo P.6** convertía todo eso en árbol implementable,

este anexo baja por fin a lo más delicado:
- nodos concretos,
- líneas de criatura,
- líneas o pseudo-líneas del jugador,
- respuestas reactivas,
- remates exactos,
- y pequeñas unidades de escritura ya listas para iterar o montar.

No pretende todavía escribir todas las escenas finales completas de todas las combinaciones.  
Sí deja cerrado un **banco reutilizable y modular** para construirlas sin improvisar como borrachos con un rotulador.

---

## 1. Principio rector

Las líneas finales de PANDAMIEN deben cumplir cuatro reglas:

1. **Ser hijas del historial**, no frases guays puestas al final.
2. **Decir poco pero herir mucho**.
3. **Poder sonar en boca de criatura**, no de guionista luciéndose.
4. **Estar siempre apoyadas por cuerpo, espacio o silencio**.

Regla maestra:
**ninguna línea final larga debe explicar el juego.**
La criatura devuelve:
- deuda,
- trato,
- ritmo,
- costumbre,
- miedo,
- necesidad,
- o lectura torcida.

No hace conferencia.

---

## 2. Tipos de nodo final

## 2.1. Nodo de reconocimiento
Primera devolución clara de que la criatura ya no es sólo presión:
- te nombra,
- te espera,
- te conoce,
- o te corrige.

## 2.2. Nodo de invitación
La criatura abre trato:
- pide,
- llama,
- pregunta,
- insinúa,
- o sólo deja sitio verbal.

## 2.3. Nodo de juicio
La criatura devuelve medida:
- mentira,
- retraso,
- evasión,
- patrón,
- negación.

## 2.4. Nodo de cuerpo
La criatura devuelve:
- latido,
- respiración,
- humedad,
- hambre,
- peso,
- tactilidad.

## 2.5. Nodo de umbral
La criatura habla o actúa desde:
- rendija,
- marco,
- pasillo,
- puerta principal,
- espera de borde.

## 2.6. Nodo de decisión
Unidad authored donde el jugador queda forzado a:
- admitir,
- negar,
- abrir,
- contener,
- retirarse,
- o sostener escucha.

## 2.7. Nodo de remate
No abre más trato.  
Clava:
- la imagen final,
- la frase final,
- o el silencio final.

---

## 3. Formato recomendado de nodo

```yaml
node_id: "P7_NODE_EXAMPLE_01"
profile_main: "P05"
closure_bias: "C02"
node_family: "judgment"
space_focus: ["hallway", "sealed_door"]
creature_mode: "voice_reasonable"
player_inputs:
  - "respond"
  - "admit"
  - "deny"
  - "silence"
creature_line: "No era falta de palabras."
player_response_seeds:
  respond:
    - "¿Y entonces qué era?"
  admit:
    - "Lo sé."
  deny:
    - "No sabes nada."
  silence:
    - "[silencio]"
effects:
  truth_depth: +1
  denial_depth: 0
  creature_clarity: +1
notes: "La criatura no explica; devuelve patrón."
```

---

## 4. Banco de líneas por perfil

A continuación se proponen bancos de líneas exactas o casi exactas por perfil principal.  
No todas deben usarse juntas.  
Están pensadas como munición authored.

---

# P01 — DOLIENTE TORÁCICO

## 4.1. Tono
- íntimo
- doliente
- cercano
- poco verbal pero muy cargado
- jamás cursi

## 4.2. Nodos de reconocimiento

### P7_P01_REC_01
**Criatura:** “Aquí.”  
Uso:
- cercanía inicial
- si el jugador escucha

### P7_P01_REC_02
**Criatura:** “No... cierres.”  
Uso:
- primer reconocimiento con súplica
- mejor con `LV1–LV2`

### P7_P01_REC_03
**Criatura:** “Ya me oyes.”  
Uso:
- si el jugador ha escuchado mucho durante la partida

## 4.3. Nodos de invitación

### P7_P01_INV_01
**Criatura:** “Pon la mano.”  
Uso:
- si el marco responde al tacto
- muy bueno para EM01

### P7_P01_INV_02
**Criatura:** “No hace falta abrir del todo.”  
Uso:
- apertura parcial
- cierre C01 o C02

### P7_P01_INV_03
**Criatura:** “Sólo no te vayas todavía.”  
Uso:
- si la criatura es más suplicante que hostil

## 4.4. Nodos de dolor / cuerpo

### P7_P01_BODY_01
**Criatura:** “Me has dejado latiendo aquí.”  
Uso:
- si heart muy alta
- admisión posible

### P7_P01_BODY_02
**Criatura:** “No sabía parar.”  
Uso:
- si el jugador cuidó tarde
- tono doliente no acusatorio

### P7_P01_BODY_03
**Criatura:** “Cuando tú callabas, yo seguía.”  
Uso:
- mezcla de cuerpo + silencio histórico

## 4.5. Nodos de decisión

### P7_P01_DEC_01
**Criatura:** “Dímelo de frente.”  
Inputs mejores:
- admitir
- negar
- callar

### P7_P01_DEC_02
**Criatura:** “Si abres, no vuelvas a llamarme sólo puerta.”  
Inputs mejores:
- abrir
- contener
- retirarse

## 4.6. Remates

### P7_P01_END_01
**Criatura:** “Ahora sí.”  
Uso:
- C01 o C02 muy íntimos

### P7_P01_END_02
**Criatura:** “No me cierres como si no me hubieras oído.”  
Uso:
- si el jugador intenta contención negadora

### P7_P01_END_03
**[Silencio + latido que se acompasa mal]**
Uso:
- finales sin gran frase
- muy PANDAMIEN

---

# P02 — MEDIDOR FUNCIONAL

## 4.1. Tono
- preciso
- frío
- seco
- casi profesional
- más jodido cuanto menos teatral

## 4.2. Nodos de reconocimiento

### P7_P02_REC_01
**Criatura:** “Necesito una respuesta clara.”  
Uso:
- arranque muy fuerte
- eco del editor

### P7_P02_REC_02
**Criatura:** “Ya vas tarde incluso para esto.”  
Uso:
- si hostilidad alta

### P7_P02_REC_03
**Criatura:** “No me dejes en el aire otra vez.”  
Uso:
- si patrón de delay/ghosting muy fuerte

## 4.3. Nodos de juicio

### P7_P02_JUD_01
**Criatura:** “No era falta de tiempo.”  
Uso:
- nodo de verdad
- muy bueno si el jugador admite

### P7_P02_JUD_02
**Criatura:** “Era costumbre.”  
Uso:
- devolución de patrón de evitación

### P7_P02_JUD_03
**Criatura:** “Siempre pedías un rato más.”  
Uso:
- eco directo de aplazamiento

### P7_P02_JUD_04
**Criatura:** “No llegabas. Lo ibas dejando.”  
Uso:
- si negación fuerte pero la criatura tiene claridad verbal

## 4.4. Nodos de decisión

### P7_P02_DEC_01
**Criatura:** “Dilo ahora.”  
Inputs:
- responder
- admitir
- negar
- callar

### P7_P02_DEC_02
**Criatura:** “Aunque sea para decir que no.”  
Inputs:
- admitir
- negar
- abrir
- contener

## 4.5. Remates

### P7_P02_END_01
**Criatura:** “Ahora ya no puedes dejarlo para luego.”  
Uso:
- fractura o apertura hostil

### P7_P02_END_02
**Criatura:** “Eso era.”  
Uso:
- si el jugador por fin admite

### P7_P02_END_03
**[Golpe seco en marco + silencio]**
Uso:
- C05 muy duro
- sin frase larga

---

# P03 — OBSERVADOR DE UMBRAL

## 4.1. Tono
- mínimo
- vigilante
- más espacial que verbal
- orientado

## 4.2. Nodos de reconocimiento

### P7_P03_REC_01
**Criatura:** “Ya.”  
Uso:
- pausa orientada
- casi nada de palabra

### P7_P03_REC_02
**Criatura:** “Siempre paras aquí.”  
Uso:
- si mucha conducta de borde

### P7_P03_REC_03
**[Silencio atento, como si la criatura acabara de corregir su foco]**
Uso:
- `LV0`
- muy bueno para EM04

## 4.3. Nodos de umbral

### P7_P03_THR_01
**Criatura:** “No sabes cruzar.”  
Uso:
- si el jugador mira mucho pero actúa poco

### P7_P03_THR_02
**Criatura:** “Ni entrar ni irte.”  
Uso:
- ambivalencia alta

### P7_P03_THR_03
**Criatura:** “Otra vez aquí.”  
Uso:
- perfil de repetición de pasillo

## 4.4. Nodos de decisión

### P7_P03_DEC_01
**Criatura:** “Acércate o no.”  
Inputs:
- acercarse
- retirarse
- callar

### P7_P03_DEC_02
**Criatura:** “No hace falta que mires más.”  
Inputs:
- tocar
- abrir
- seguir escuchando

## 4.5. Remates

### P7_P03_END_01
**[El pasillo sigue pesando aunque la criatura ya no diga nada]**
Uso:
- C06
- C05

### P7_P03_END_02
**Criatura:** “Eso haces siempre.”  
Uso:
- si el jugador repite patrón del borde en el final

---

# P04 — HAMBRIENTO PARLANCHÍN

## 4.1. Tono
- pegajoso
- banal podrido
- necesitado
- socialmente obsceno

## 4.2. Nodos de reconocimiento

### P7_P04_REC_01
**Criatura:** “No te vayas ahora, joder.”  
Uso:
- necesidad + cercanía

### P7_P04_REC_02
**Criatura:** “Habla otra vez.”  
Uso:
- si el jugador responde mínimo

### P7_P04_REC_03
**Criatura:** “No sé si quiero que me digas algo o que te quedes.”  
Uso:
- hambre + compañía

## 4.3. Nodos de hambre / mezcla

### P7_P04_BODY_01
**Criatura:** “Aquí dentro todo seguía pidiendo.”  
Uso:
- stomach alta

### P7_P04_BODY_02
**Criatura:** “Lo dejabas sonar todo.”  
Uso:
- TV + amigo + cocina

### P7_P04_BODY_03
**Criatura:** “No sabía si era hambre o compañía.”  
Uso:
- remate muy pandamien

## 4.4. Remates

### P7_P04_END_01
**Criatura:** “Quédate un poco más.”  
Uso:
- convivencia podrida

### P7_P04_END_02
**[Una frase banal vuelve detrás del marco como si hubiera aprendido a tener hambre]**
Uso:
- remate sin explicar

---

# P05 — RAZONABLE TORCIDO

## 4.1. Tono
- lógico
- persuasivo
- íntimamente insoportable
- nunca demasiado limpio

## 4.2. Nodos de reconocimiento

### P7_P05_REC_01
**Criatura:** “Ya sabes que esto no puede seguir siendo sólo una puerta.”  
Uso:
- arranque fuerte de EM02

### P7_P05_REC_02
**Criatura:** “Has llegado hasta aquí para no poder seguir fingiendo.”  
Uso:
- si el jugador escucha y se acerca

### P7_P05_REC_03
**Criatura:** “No te estoy pidiendo tanto.”  
Uso:
- ambigüedad moral

## 4.3. Nodos de verdad / trato

### P7_P05_TRUTH_01
**Criatura:** “No era que no supieras. Era que podías dejarlo para después.”  
Uso:
- verdad ética
- muy buena línea

### P7_P05_TRUTH_02
**Criatura:** “Lo llamabas cansancio cuando todavía podías apartar la mirada.”  
Uso:
- cuerpo + negación

### P7_P05_TRUTH_03
**Criatura:** “No me hiciste de golpe. Eso sería demasiado fácil.”  
Uso:
- reconocimiento monstruoso sin exposición total

### P7_P05_TRUTH_04
**Criatura:** “Con que me mires de frente una vez ya cambia todo.”  
Uso:
- antes de apertura o admisión

## 4.4. Nodos de decisión

### P7_P05_DEC_01
**Criatura:** “Dime si vas a seguir llamándome mentira.”  
Inputs:
- admitir
- negar
- callar

### P7_P05_DEC_02
**Criatura:** “No tienes que abrir del todo. Pero sí decidir.”  
Inputs:
- abrir
- contener
- retirarse

## 4.5. Remates

### P7_P05_END_01
**Criatura:** “Ahora ya sabes dónde poner el cuerpo.”  
Uso:
- contención ética

### P7_P05_END_02
**Criatura:** “Entonces abre.”  
Uso:
- apertura íntima
- muy peligrosa, usar con bisturí

### P7_P05_END_03
**[Silencio corto; luego una exhalación que suena a acuerdo demasiado caro]**
Uso:
- cierre más fino que verbal

---

# P06 — SÚPLICA DE MARCO

## 4.1. Tono
- muy dependiente
- muy de borde
- poca palabra
- mucha espera

## 4.2. Nodos de reconocimiento

### P7_P06_REC_01
**Criatura:** “No te vayas.”  
Uso:
- sencillo y durísimo si el contexto lo sostiene

### P7_P06_REC_02
**Criatura:** “Aquí.”  
Uso:
- llamada mínima de marco

### P7_P06_REC_03
**[Calor en la madera antes que frase]**
Uso:
- perfil bajo verbal

## 4.3. Nodos de súplica

### P7_P06_SUP_01
**Criatura:** “Sólo quédate.”  
Uso:
- dependencia alta

### P7_P06_SUP_02
**Criatura:** “No sabía pedirlo mejor.”  
Uso:
- dolor + borde
- línea potentísima

### P7_P06_SUP_03
**Criatura:** “No te estaba persiguiendo. Te estaba esperando.”  
Uso:
- final de umbral o contención

## 4.4. Remates

### P7_P06_END_01
**[Mano + calor + silencio]**
Uso:
- C01
- C06

### P7_P06_END_02
**Criatura:** “Ya.”  
Uso:
- remate mínimo, muy seco y muy fuerte

---

# P07 — RENCOR DE TRAYECTO

## 4.1. Tono
- duro
- corto
- físico
- sin florituras

## 4.2. Nodos de reconocimiento

### P7_P07_REC_01
**Criatura:** “Ahora no corras.”  
Uso:
- si el jugador retrocede

### P7_P07_REC_02
**Criatura:** “Demasiado tarde.”  
Uso:
- hostilidad alta
- apertura violenta o fractura

### P7_P07_REC_03
**[Golpe de peso sin frase]**
Uso:
- `LV0–LV1`

## 4.3. Nodos de presión

### P7_P07_JUD_01
**Criatura:** “Ni una vez te quedaste del todo.”  
Uso:
- borde + culpa

### P7_P07_JUD_02
**Criatura:** “Siempre querías salida.”  
Uso:
- si mucha mirada al exterior / mucha huida

## 4.4. Remates

### P7_P07_END_01
**[El pasillo deja de ser tuyo]**
Uso:
- remate físico sin frase

### P7_P07_END_02
**Criatura:** “Pues ahora sí.”  
Uso:
- absorción brusca o fractura

---

# P08 — ARCHIVO MAL COSIDO

## 4.1. Tono
- híbrido
- preciso en el caos
- mezclado
- no carnavalesco

## 4.2. Nodos de reconocimiento

### P7_P08_REC_01
**Criatura:** “No era sólo una llamada.”  
Uso:
- mezcla de vínculos
- muy buena apertura de EM05

### P7_P08_REC_02
**Criatura:** “No era sólo cansancio.”  
Uso:
- cuerpo + trabajo + negación

### P7_P08_REC_03
**Criatura:** “No era sólo una puerta.”  
Uso:
- una de las mejores líneas de mezcla del bloque

## 4.3. Nodos de mezcla

### P7_P08_MIX_01
**Criatura:** “Tú también me oías por partes.”  
Uso:
- mezcla de voces + historial

### P7_P08_MIX_02
**Criatura:** “Primero fui ruido. Luego ya me fuiste dejando nombre.”  
Uso:
- evolución de criatura
- muy pandamien

### P7_P08_MIX_03
**Criatura:** “No sabías a quién estabas dejando en visto.”  
Uso:
- brutal si el historial lo sostiene

### P7_P08_MIX_04
**Criatura:** “La casa no callaba sola.”  
Uso:
- línea madre del perfil
- puede ser remate brutal

## 4.4. Nodos de decisión

### P7_P08_DEC_01
**Criatura:** “Ahora dime qué haces con todo esto.”  
Inputs:
- admitir
- negar
- contener
- abrir

### P7_P08_DEC_02
**Criatura:** “No me ordenes ahora.”  
Inputs:
- contener
- negar
- responder

## 4.5. Remates

### P7_P08_END_01
**Criatura:** “Ya no hace falta que sepas de quién era cada voz.”  
Uso:
- absorción

### P7_P08_END_02
**[TV residual + frase doméstica irreconociblemente tuya]**
Uso:
- convivencia podrida

---

# P09 — CUIDADO INTRUSIVO

## 4.1. Tono
- corporal
- húmedo
- preocupado sin permiso
- tristemente invasivo

## 4.2. Nodos de reconocimiento

### P7_P09_REC_01
**Criatura:** “Te ibas dejando.”  
Uso:
- madre/cuerpo altos

### P7_P09_REC_02
**Criatura:** “No querías que te vieran así.”  
Uso:
- baño/dormitorio potentes

### P7_P09_REC_03
**Criatura:** “Yo sí me quedé mirándolo.”  
Uso:
- terror íntimo muy fino

## 4.3. Nodos de cuerpo / cuidado

### P7_P09_BODY_01
**Criatura:** “No era sólo humedad.”  
Uso:
- skin alta

### P7_P09_BODY_02
**Criatura:** “Te seguí respirando aquí.”  
Uso:
- lungs/skin
- muy bueno para marco

### P7_P09_BODY_03
**Criatura:** “No sabía cuidarte mejor.”  
Uso:
- línea potentísima, con mucho riesgo si se usa sin contexto

## 4.4. Remates

### P7_P09_END_01
**[Respiración cerca del marco como si quisiera cubrirte]**
Uso:
- convivencia o contención

### P7_P09_END_02
**Criatura:** “Ahora sí descansa.”  
Uso:
- sólo si el contexto lo sostiene de forma oscurísima

---

# P10 — BORDE QUE TE SABE

## 4.1. Tono
- sobrio
- atento
- muy de patrón y umbral
- casi arquitectónico

## 4.2. Nodos de reconocimiento

### P7_P10_REC_01
**Criatura:** “Sabía que volverías aquí.”  
Uso:
- EM04
- borde fuerte

### P7_P10_REC_02
**Criatura:** “Siempre paras en el mismo sitio antes de decidir.”  
Uso:
- lectura de hábito

### P7_P10_REC_03
**Criatura:** “No me estabas mirando a mí. Te estabas mirando desde aquí.”  
Uso:
- brutal para final pandamien puro

## 4.3. Nodos de umbral / lectura

### P7_P10_THR_01
**Criatura:** “No hace falta que abras para cruzar.”  
Uso:
- C06 o C02

### P7_P10_THR_02
**Criatura:** “Yo aprendí antes que tú por dónde ibas a volver.”  
Uso:
- umbral inteligente

### P7_P10_THR_03
**Criatura:** “El borde también se acostumbra.”  
Uso:
- línea seca muy buena

## 4.4. Nodos de decisión

### P7_P10_DEC_01
**Criatura:** “Acércate o sigue haciéndote el pasillo.”  
Inputs:
- acercarse
- callar
- retirarse

### P7_P10_DEC_02
**Criatura:** “Si tocas, ya no vuelves a no saberlo.”  
Inputs:
- tocar
- abrir
- retirar mano

## 4.5. Remates

### P7_P10_END_01
**[Silencio atento: el borde ya no te espera, te conoce]**
Uso:
- C06

### P7_P10_END_02
**Criatura:** “Ya.”  
Uso:
- remate mínimo devastador

### P7_P10_END_03
**Criatura:** “Ahora ya eres de aquí también.”  
Uso:
- absorción de umbral, sólo si se gana de verdad

---

## 5. Banco de pseudo-respuestas del jugador

No son líneas definitivas del protagonista, sino semillas de tono.

## 5.1. Respuesta directa
- “Lo sé.”
- “No sé qué quieres que te diga.”
- “Ya estoy aquí.”
- “No te estoy evitando ahora.”

## 5.2. Respuesta evasiva
- “No es tan simple.”
- “No era así.”
- “No me hagas esto.”
- “No sé.”

## 5.3. Admisión
- “Te dejé crecer.”
- “Lo fui dejando.”
- “Te oía.”
- “No quería mirarte.”

## 5.4. Negación
- “No eres eso.”
- “No tienes nada que ver conmigo.”
- “No me hables como si me conocieras.”
- “No.”

## 5.5. Silencio
- “[se queda]”
- “[retira la mano]”
- “[no contesta]”
- “[respira]”

---

## 6. Nodos listos para MVP fuerte

Para una primera versión muy sólida, recomiendo usar ya estos:

### MVP_P7_01
**P01 / EM01 / C01**
- “Pon la mano.”
- “No me cierres como si no me hubieras oído.”
- remate: latido + silencio

### MVP_P7_02
**P05 / EM02 / C02**
- “No me hiciste de golpe.”
- “No tienes que abrir del todo. Pero sí decidir.”
- remate: rendija + exhalación

### MVP_P7_03
**P02 / EM03 / C05**
- “No era falta de tiempo.”
- “Era costumbre.”
- remate: golpe seco + silencio

### MVP_P7_04
**P10 / EM04 / C06**
- “Sabía que volverías aquí.”
- “No hace falta que abras para cruzar.”
- remate: silencio del borde

---

## 7. Reglas de combinación

## 7.1. No apilar demasiadas líneas memorables juntas
Una escena buena no necesita seis frases de póster.  
Con una o dos bien puestas, sobra.

## 7.2. Regla de apoyo físico
Toda línea fuerte debe ir apoyada por:
- aire,
- latido,
- pausa,
- peso,
- marco,
- glow de TV,
- cama,
- o pasillo.

## 7.3. Regla de tono por perfil
- P01, P06, P09 → más cuerpo que discurso
- P02, P05 → más precisión verbal
- P03, P07, P10 → más borde que parloteo
- P04, P08 → más mezcla, pero con control

## 7.4. Regla anti-lore
Ninguna línea debe contestar:
- qué es exactamente la criatura,
- cómo funciona el piso,
- o una explicación cerrada del sistema.

---

## 8. Qué falta después de P.7

Tras este banco de nodos y líneas, lo siguiente natural es:

**P.8 — Locks, condiciones y pseudológica de implementación final**

Ahí tocaría:
- convertir este banco en reglas ejecutables,
- fijar prioridades de implementación,
- y dejar el bloque final listo para consolidación canónica.

---

## 9. Cierre de dirección

Aquí ya empieza la parte donde el juego puede romperse por exceso o quedarse tieso por miedo.

Las líneas finales de PANDAMIEN tienen que sonar como si llevaran todo el juego esperando detrás de la puerta.  
No como si las hubiéramos escrito ayer para quedar de listos.

Cuando funcionen, no parecerán “buenas frases”.  
Parecerán **verdades malas que la casa llevaba ensayando demasiado tiempo**.
