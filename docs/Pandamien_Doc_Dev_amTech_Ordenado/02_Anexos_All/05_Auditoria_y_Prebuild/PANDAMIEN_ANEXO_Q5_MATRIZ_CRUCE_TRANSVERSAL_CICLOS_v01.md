# PANDAMIEN — ANEXO Q.5
## Matriz de cruce transversal por ciclos v01
### Derivada del GDD Maestro v07, del Plan de Acción Maestro v06, del Anexo F v01, del Anexo G v01, del Anexo H v01, del bloque P–P.8, de la Auditoría total v01 y del Diccionario unificado de variables v01

---

## 0. Estado del documento

Este documento abre la **Matriz de cruce transversal por ciclos**.

Su función no es volver a escribir los ciclos 1–8.  
Su función es comprobar, ordenar y dejar visible **cómo se cosen realmente** en cada ciclo estos cuatro bloques mayores del proyecto:

- **TV**
- **Exterioridad**
- **Criatura**
- **Confrontación final**

Hasta ahora esos bloques ya existen y están bastante bien definidos por separado.  
Lo que necesitábamos aquí era una herramienta para revisar, ciclo a ciclo:

- qué entra por cada canal,
- qué aprende el apartamento,
- qué roba la criatura,
- qué se prepara para el final,
- y qué riesgo de contradicción o sobrecarga hay.

Este documento es, por tanto, un puente entre:
- authored por ciclos,
- sistemas transversales,
- y prioridades de implementación.

---

## 1. Principio rector

Cada ciclo de PANDAMIEN debe empujar simultáneamente cuatro cosas:

1. **la relación del jugador con el piso**
2. **la lectura del afuera / del borde**
3. **la formación de la criatura**
4. **la futura inteligibilidad del careo final**

Si un ciclo está bien authored pero no deja residuo útil para esos cuatro ejes, entonces está bonito pero no trabaja lo suficiente.

Regla maestra:
**ningún ciclo debe sentirse aislado del monstruo final, aunque el monstruo aún no pueda hablar ni mostrarse claramente.**

---

## 2. Cómo leer esta matriz

Cada ciclo se revisa con estos campos:

- **Presión activa**
- **TV: función del ciclo**
- **Exterioridad: función del ciclo**
- **Criatura: aprendizaje / crecimiento**
- **Confrontación final: semilla o preparación**
- **Zonas dominantes**
- **Variables clave sugeridas**
- **Riesgo de integración**
- **Acción correctiva si hace falta**

---

## 3. Matriz transversal

---

# C01 — Reconocimiento

## Presión activa
Rutina, primer editor, base cotidiana, puerta todavía “doméstica”.

## TV
### Función del ciclo
- acompañamiento,
- anestesia blanda,
- primer comfort,
- ligereza funcional.

### Lo que siembra
- costumbre de fondo,
- dependencia suave,
- primer derecho de la TV a ocupar silencio.

## Exterioridad
### Función del ciclo
- clima social de encierro,
- vida vecinal de fondo,
- sirena o aplauso posibles,
- mundo existente pero lejano.

### Lo que siembra
- el piso no está solo,
- el afuera no es libre, sólo distante.

## Criatura
### Aprendizaje / crecimiento
- casi nada visible,
- primera resonancia tras puerta,
- respuesta torpe,
- primer signo de que algo puede estar organizándose.

### Funciones probables
- pre-voz
- peso abstracto

## Confrontación final
### Semilla
- la puerta como promesa,
- la escucha como primer verbo moral.

## Zonas dominantes
- salón
- pasillo
- puerta atrancada como detalle

## Variables clave sugeridas
- `tv_influence`
- `rel_editor_intensity`
- `zone_living_contamination`
- `door_pressure`

## Riesgo de integración
Bajo.

## Acción correctiva
Ninguna gruesa.  
Sólo cuidar que el primer ciclo ya huela a retorno futuro sin forzarlo.

---

# C02 — Primera deuda clara

## Presión activa
Trabajo, respuesta, tiempo, deuda funcional.

## TV
### Función del ciclo
- compañía de fondo que tapa responsabilidad,
- comfort virando a suggestion.

### Lo que siembra
- anestesia funcional,
- capacidad de la TV para no parecer inocente del todo.

## Exterioridad
### Función del ciclo
- borde utilitario:
  - paquete,
  - timbre,
  - rellano,
  - vida práctica.

### Lo que siembra
- entrada y pasillo como zonas de lectura.

## Criatura
### Aprendizaje / crecimiento
- primer tono de voz o función ligada a trabajo/respuesta,
- presión todavía poco corporal.

### Funciones probables
- `func_voice` temprano
- eco de ritmo cortado

## Confrontación final
### Semilla
- futura criatura capaz de medir, pedir respuesta o devolver tardanza.

## Zonas dominantes
- salón
- entrada
- pasillo

## Variables clave sugeridas
- `rel_editor_intensity`
- `tv_influence`
- `zone_entry_contamination`
- `zone_hallway_contamination`
- `func_voice`

## Riesgo de integración
Medio-bajo.

## Acción correctiva
Vigilar que lo funcional no tape del todo la promesa orgánica.

---

# C03 — El cuerpo entra en juego

## Presión activa
Madre / cuerpo / descanso / baño y dormitorio.

## TV
### Función del ciclo
- suggestion clínica,
- cuidado empaquetado,
- descanso mal entendido.

### Lo que siembra
- TV roba a madre y al cuerpo.

## Exterioridad
### Función del ciclo
- pandemia,
- contagio,
- respiración social,
- ambulancia,
- vecino tosiendo,
- aire.

### Lo que siembra
- pulmones,
- cuerpo social,
- exposición del aire.

## Criatura
### Aprendizaje / crecimiento
- respiración,
- piel,
- humedad,
- pecho temprano.

### Funciones probables
- `func_skin`
- `func_lungs`
- `func_heart` embrionario

## Confrontación final
### Semilla
- criaturas dolientes, suplicantes o corporales se empiezan a volver posibles.

## Zonas dominantes
- baño
- dormitorio
- pasillo

## Variables clave sugeridas
- `rel_mother_intensity`
- `zone_bathroom_contamination`
- `zone_bedroom_contamination`
- `func_skin`
- `func_lungs`

## Riesgo de integración
Bajo.

## Acción correctiva
Sólo cuidar que el cuerpo no se quede aislado del resto del sistema y que ya deje residuo verbal reutilizable.

---

# C04 — La herida íntima

## Presión activa
Pareja/ex, dormitorio, balcón, pecho, memoria a medias.

## TV
### Función del ciclo
- suggestion sentimental,
- consejo emocional obsceno,
- melodrama empaquetado.

### Lo que siembra
- futura contaminación afectiva en TV y criatura.

## Exterioridad
### Función del ciclo
- balcón y ventana como exposición íntima,
- pareja vecina,
- luz ajena,
- aire que duele.

### Lo que siembra
- exterioridad ya no sólo paranoica: también íntima.

## Criatura
### Aprendizaje / crecimiento
- corazón,
- latido,
- súplica,
- pausa afectiva,
- dolor torácico.

### Funciones probables
- `func_heart`
- `temper_doliente`
- `temper_supplicant`

## Confrontación final
### Semilla
- perfil P01 y familia de apertura íntima / contención ética / convivencia podrida.

## Zonas dominantes
- dormitorio
- balcón
- pasillo

## Variables clave sugeridas
- `rel_ex_partner_intensity`
- `zone_bedroom_contamination`
- `zone_balcony_contamination`
- `func_heart`
- `bond_intimacy_with_player`

## Riesgo de integración
Medio.

## Acción correctiva
Asegurar que la herida íntima deja frases, pausas y ritmos que después puedan reaparecer en P.7 sin sonar metidas con calzador.

---

# C05 — El exterior se pega al piso

## Presión activa
Umbral, mirilla, puerta principal, rellano, ventana, balcón.

## TV
### Función del ciclo
- suggestion editorial sobre vigilancia, ruido, convivencia, seguridad.

### Lo que siembra
- lectura mediada del afuera,
- legitimación del foco paranoico.

## Exterioridad
### Función del ciclo
- contagio interpretativo,
- borde enfermo,
- vigilancia,
- exposición.

### Lo que siembra
- entrada/pasillo/ventana/balcón como órganos narrativos.

## Criatura
### Aprendizaje / crecimiento
- ojos,
- orientación,
- atención dirigida,
- foco de trayecto.

### Funciones probables
- `func_eyes`
- `threshold_intelligence`
- `temper_imitative` o `temper_resentful`

## Confrontación final
### Semilla
- perfiles P03 y P10,
- finales de umbral, borde, foco y suspensión.

## Zonas dominantes
- entrada
- pasillo
- ventana
- balcón

## Variables clave sugeridas
- `ext_pressure`
- `ext_vigilance_bias`
- `zone_entry_contamination`
- `zone_hallway_contamination`
- `func_eyes`
- `threshold_intelligence`

## Riesgo de integración
Medio-alto.

## Acción correctiva
Cruzar fino con P.4–P.8 para que el final de umbral no parezca salido de la nada, sino ganado aquí.

---

# C06 — Colonización semántica

## Presión activa
TV, mezcla de voces, sintaxis contaminada, salón/pasillo.

## TV
### Función del ciclo
- pseudo-centro interpretativo,
- manipulation,
- editorialización de todo.

### Lo que siembra
- la TV ya no comenta: organiza.

## Exterioridad
### Función del ciclo
- pasa a segundo plano directo,
- pero su lectura ya queda contaminada por discurso.

### Lo que siembra
- el afuera ya no se interpreta limpio.

## Criatura
### Aprendizaje / crecimiento
- voz,
- mezcla,
- sintaxis defectuosa,
- llamada fallida.

### Funciones probables
- `func_voice`
- `lang_capacity`
- `lang_mix_index`
- `lang_memory_depth`

## Confrontación final
### Semilla
- perfiles P05, P08 y parte de P02.
- posibilidad de criatura que ya no sólo devuelve, sino que interpreta.

## Zonas dominantes
- salón
- pasillo
- puerta atrancada

## Variables clave sugeridas
- `tv_manipulation_level`
- `lang_capacity`
- `lang_coherence`
- `lang_mix_index`
- `zone_living_contamination`
- `zone_hallway_contamination`

## Riesgo de integración
Alto.

## Acción correctiva
Aquí es donde más hace falta la Biblia de diálogos y el diccionario de variables.  
Este ciclo puede ser glorioso o una sopa si no se controla.

---

# C07 — Doble vínculo imposible

## Presión activa
Superposición de demandas incompatibles.

## TV
### Función del ciclo
- subrayar, empujar, cortar, editorializar presión simultánea.

## Exterioridad
### Función del ciclo
- competir con móvil, vínculo, cuerpo o deadline.
- el afuera se vuelve una urgencia más dentro del nudo.

## Criatura
### Aprendizaje / crecimiento
- fija temperamento dominante,
- aprende del sacrificio real del jugador.

### Funciones probables
- depende de historial, pero aquí se estabiliza:
  - rencor,
  - súplica,
  - juicio,
  - hambre,
  - o foco.

## Confrontación final
### Semilla
- define más claramente familia de cierre probable:
  - apertura,
  - contención,
  - fractura,
  - umbral perpetuo,
  - absorción.

## Zonas dominantes
- variables según partida, pero el pasillo debe estar muy vivo

## Variables clave sugeridas
- `bond_hostility_to_player`
- `bond_trust_to_player`
- `bond_dependence_on_player`
- `temper_*` dominante
- `door_pressure`

## Riesgo de integración
Medio-alto.

## Acción correctiva
Asegurar que C07 no sea sólo “muchas cosas a la vez”, sino el ciclo que fija con claridad el trato final.

---

# C08 — Resolución

## Presión activa
La criatura y el umbral ya exigen relación definida.

## TV
### Función del ciclo
- residual o eco,
- nunca protagonista.

## Exterioridad
### Función del ciclo
- espejo final,
- silencio del edificio,
- respiración del borde,
- apoyo de suspensión o cruce.

## Criatura
### Aprendizaje / crecimiento
- no aprende tanto nuevo aquí: devuelve lo aprendido.

## Confrontación final
### Semilla
- aquí ya no es semilla: aquí se paga la promesa completa.

## Zonas dominantes
- pasillo
- puerta atrancada
- y zona secundaria según perfil:
  - dormitorio,
  - salón,
  - balcón,
  - entrada

## Variables clave sugeridas
- `final_*`
- snapshot completo del estado acumulado

## Riesgo de integración
Bajo, si todo lo anterior está bien cosido.
Muy alto, si lo anterior no lo está.

## Acción correctiva
No meter soluciones nuevas aquí.  
Sólo devolución.

---

## 4. Lectura transversal por sistemas

# 4.A. TV a través de los ciclos
- C01: comfort
- C02: comfort -> suggestion
- C03: suggestion clínica
- C04: suggestion sentimental
- C05: suggestion editorial
- C06: manipulation
- C07: manipulation de presión cruzada
- C08: residual_confrontation

## Dictamen
Coherente.  
No necesita rediseño, sino vigilancia fina de tono.

---

# 4.B. Exterioridad a través de los ciclos
- C01: telón social
- C02: borde utilitario
- C03: aire/cuerpo/pandemia
- C04: intimidad a distancia
- C05: foco enfermo del umbral
- C06: material ya contaminado por discurso
- C07: urgencia cruzada
- C08: espejo final

## Dictamen
Muy potente.
Éste es uno de los mejores arcos sistémicos del proyecto.

---

# 4.C. Criatura a través de los ciclos
- C01: respuesta torpe
- C02: ritmo / voz temprana
- C03: piel / pulmones / cuerpo
- C04: corazón / pecho / súplica
- C05: ojos / orientación
- C06: voz / sintaxis
- C07: fijación de temperamento
- C08: devolución final

## Dictamen
Excelente arco.
Es de las espinas dorsales más claras del proyecto.

## Riesgo
No de diseño, sino de asset scope y priorización.

---

# 4.D. Preparación de la confrontación final
- C01: escuchar
- C02: responder / retrasar
- C03: cuerpo
- C04: intimidad
- C05: umbral
- C06: lenguaje
- C07: trato irreversible
- C08: pago total

## Dictamen
Muy bien cosido en abstracto.

## Riesgo
Todavía falta traducir esta limpieza a:
- asset map,
- MVP selection,
- rutas mínimas de build.

---

## 5. Hallazgos principales

## 5.1. Hallazgo 01
El arco **TV → criatura verbal → confrontación final** está muy bien pensado, pero necesita control fino de tono para no inflarse.

## 5.2. Hallazgo 02
El arco **exterioridad → ojos/umbral → finales de borde** es uno de los más sólidos del proyecto y debe protegerse como pilar.

## 5.3. Hallazgo 03
Los ciclos 4, 5 y 6 son el triángulo más delicado:
- intimidad,
- borde,
- sintaxis.

Si esa tríada se cose bien, el final cae por su propio peso.

## 5.4. Hallazgo 04
C07 es el ciclo más fácil de estropear por exceso.  
Debe ser punto de fijación, no de barro.

## 5.5. Hallazgo 05
La confrontación final ya está bien preparada a nivel semántico y sistémico.  
Lo que falta es selección y montaje, no idea.

---

## 6. Riesgos detectados ciclo a ciclo

### C01
Riesgo: demasiado limpio.
Control: sembrar puerta y TV sin subrayar.

### C02
Riesgo: que el trabajo tape el monstruo.
Control: mantener residuo de umbral.

### C03
Riesgo: que el cuerpo quede aislado del resto.
Control: dejar residuo verbal y de TV.

### C04
Riesgo: melodrama.
Control: mantener materialidad y deuda.

### C05
Riesgo: thriller de vecinos.
Control: recordar que el exterior infecta, no informa.

### C06
Riesgo: sopa semántica.
Control: Biblia de diálogos + selección.

### C07
Riesgo: sobreacumulación.
Control: un conflicto dominante, no cuatro al mismo volumen.

### C08
Riesgo: final explicativo.
Control: devolver, no explicar.

---

## 7. Acciones derivadas inmediatas

## 7.1. Acción A
Usar esta matriz para revisar authored satélite de C / D / E y marcar:
- residuos fuertes que merece conservar,
- redundancias,
- puntos donde TV/exterior/criatura/final aún no se notan suficiente.

## 7.2. Acción B
Abrir **Q.2 — Asset map y prioridades de producción** con esta matriz ya como guía.

## 7.3. Acción C
Abrir **Q.3 — Paquete MVP del final** usando especialmente los hallazgos sobre:
- C04,
- C05,
- C06,
- C07,
- C08.

---

## 8. Dictamen final de esta matriz

El proyecto no está deshilachado por ciclos.  
Al contrario: el recorrido 1–8 aguanta bastante bien como espina dorsal de:
- contaminación,
- criatura,
- TV,
- exterioridad,
- y devolución final.

La buena noticia es ésa.

La mala —o la cabrona— es otra:
como el armazón ya está bien, ahora no hay excusa para dejarlo fofo en producción.

Ahora toca:
- seleccionar,
- recortar,
- priorizar,
- y traducir esta belleza húmeda a build sin que se nos desmaye por exceso de amor al detalle.

---

## 9. Cierre de dirección

Si esta matriz sirve de verdad, entonces cada ciclo dejará de ser “un episodio del juego” y pasará a sentirse como lo que en realidad es:

**una fase concreta del aprendizaje del piso.**

No sólo aprendizaje del monstruo.  
Aprendizaje del piso entero:
- cómo escuchar,
- cómo mirar,
- cómo doler,
- cómo hablar,
- y cómo devolverte al final algo que llevaba ensayando desde el primer día.
