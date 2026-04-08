# PANDAMIEN — Mapa de dependencias entre sistemas v01

## Objetivo
Hacer visible qué sistemas bloquean a cuáles y en qué orden conviene coserlos.

## Nodos maestros
- Core State Runtime
- Apartment Whitebox
- Interaction Base
- Zone Contamination
- Sealed Door System
- TV Runtime
- Exterior & Threshold P0
- Creature Runtime Core
- Creature Manifestation Grammar
- Authored Node Runner
- Cross-Effects Runtime
- Authored Cycles C01–C06
- Final Snapshot & Selector
- Final Local Variables & Locks
- Final Routes MVP
- Final Staging Pack
- Vertical Slice Internal Build

## Dependencias clave de lectura rápida
1. **Core State Runtime** bloquea casi todo.
2. **Apartment Whitebox** bloquea interacción, audio, luz, puerta y contaminación.
3. **Cross-Effects Runtime** es la bisagra real entre authored y sistema.
4. **Exterior & Threshold P0** es imprescindible para C05–C06 y para la ruta final P10→C06.
5. **Sealed Door System + Creature Manifestation Grammar** son el cuello de botella del horror y del final.

## Tabla de dependencias
- **Core State Runtime** → **Day-Night Loop** (hard) — Sin estado persistente no hay loop jugable.
- **Core State Runtime** → **Authored Node Runner** (hard) — Los nodos necesitan leer/escribir variables.
- **Core State Runtime** → **TV Runtime** (hard) — La TV necesita estado, ciclo y flags.
- **Core State Runtime** → **Creature Runtime Core** (hard) — La criatura nace de variables persistentes.
- **Core State Runtime** → **Final Snapshot & Selector** (hard) — El final depende del histórico consolidado.
- **Apartment Whitebox** → **Interaction Base** (hard) — No hay interacción sin espacio jugable.
- **Apartment Whitebox** → **Lighting Presets** (hard) — La luz se monta sobre el layout final.
- **Apartment Whitebox** → **Apartment Soundscape** (hard) — El audio espacial necesita zonas y volúmenes.
- **Apartment Whitebox** → **Zone Contamination** (hard) — La degradación necesita superficies/zonas.
- **Apartment Whitebox** → **Sealed Door System** (hard) — La puerta sellada depende del pasillo y su colocación.
- **Interaction Base** → **Diegetic Phone** (hard) — El móvil necesita navegación y puntos de uso.
- **Interaction Base** → **TV Runtime** (hard) — Encendido/apagado y foco visual requieren interacción.
- **Interaction Base** → **Exterior & Threshold P0** (hard) — Mirilla/ventana/balcón necesitan input básico.
- **Interaction Base** → **Sealed Door System** (hard) — Escuchar, tocar y acercarse son verbos base.
- **Zone Contamination** → **Partial Containment** (hard) — No se contiene lo que no existe en estado.
- **Zone Contamination** → **Authored Cycles C03-C06** (soft) — Estos ciclos lucen mucho peor sin degradación visible.
- **Sealed Door System** → **Creature Manifestation Grammar** (hard) — La manifestación vuelve a través de puerta/marco.
- **Creature Runtime Core** → **Creature Manifestation Grammar** (hard) — El audio/retorno debe leer funciones y temperamentos.
- **Authored Node Runner** → **Cross-Effects Runtime** (hard) — Las opciones authored necesitan aplicar huellas.
- **Cross-Effects Runtime** → **Creature Runtime Core** (hard) — Las decisiones alimentan criatura.
- **Cross-Effects Runtime** → **Zone Contamination** (hard) — Las decisiones tiñen zonas.
- **Cross-Effects Runtime** → **TV Runtime** (hard) — Las decisiones mueven influencia y estado de TV.
- **Cross-Effects Runtime** → **Exterior & Threshold P0** (soft) — Las decisiones pueden alterar presión/ambigüedad de borde.
- **TV Runtime** → **TV Library MVP** (hard) — Sin líneas/familias de programa la TV está hueca.
- **Exterior & Threshold P0** → **Exterior Events MVP** (hard) — Los eventos authored necesitan sistema de borde.
- **Authored Cycles C01-C02** → **TV Library MVP** (soft) — La TV necesita saber en qué ciclo/estado está.
- **Authored Cycles C03-C04** → **Creature Manifestation Grammar** (soft) — Cuerpo e intimidad afinan respiración/latido.
- **Authored Cycles C05-C06** → **Exterior Events MVP** (soft) — Umbral y colonización semántica piden más riqueza de borde.
- **Authored Cycles C05-C06** → **Final Snapshot & Selector** (hard) — Sin C05–C06 el final queda cojo y poco merecido.
- **TV Runtime** → **Authored Cycles C01-C06** (hard) — La TV es actor del recorrido, no postproducción.
- **Exterior & Threshold P0** → **Authored Cycles C05-C06** (hard) — Sin borde jugable C05–C06 no existen de verdad.
- **Creature Manifestation Grammar** → **Authored Cycles Noche** (hard) — Las noches necesitan retorno de puerta.
- **Authored Cycles C01-C06** → **Final Snapshot & Selector** (hard) — El final se nutre del historial de juego.
- **Final Snapshot & Selector** → **Final Local Variables & Locks** (hard) — Primero se perfila, luego se modula la escena.
- **Final Local Variables & Locks** → **Final Route A P01→C01** (hard) — La ruta necesita contadores y locks.
- **Final Local Variables & Locks** → **Final Route B P05→C02** (hard) — La ruta necesita contadores y locks.
- **Final Local Variables & Locks** → **Final Route C P02→C05** (hard) — La ruta necesita contadores y locks.
- **Final Local Variables & Locks** → **Final Route D P10→C06** (hard) — La ruta necesita contadores y locks.
- **Sealed Door System** → **Final Routes MVP** (hard) — Todas las rutas se juegan en relación con el marco.
- **Creature Manifestation Grammar** → **Final Routes MVP** (hard) — La cualidad de criatura debe leerse en final.
- **Exterior & Threshold P0** → **Final Route D P10→C06** (hard) — El borde/umbral es columna de esa ruta.
- **Lighting Presets** → **Final Staging Pack** (hard) — Los finales dependen de luz/foco/temperatura.
- **Apartment Soundscape** → **Final Staging Pack** (hard) — Sin sonido no existe el remate del final.
- **Final Routes MVP** → **Canonical Final Lines Pack** (soft) — Primero funciona la escena, luego se congela el texto.
- **Final Staging Pack** → **Vertical Slice Internal Build** (hard) — La build debe enseñar imagen y cualidad sonora final.
- **Save/Load Hardening** → **Vertical Slice Internal Build** (hard) — No hay slice estable sin persistencia.
- **Performance & Stability Pass** → **Vertical Slice Internal Build** (hard) — La build debe ser jugable, no sólo conceptualmente correcta.
- **Route QA Matrix** → **Vertical Slice Internal Build** (hard) — Sin QA el slice no es enseñable al equipo.

## Orden de ensamblaje recomendado
### Fase A — Bloqueantes puros
- Core State Runtime
- Apartment Whitebox
- Interaction Base

### Fase B — Piso que ya responde
- Lighting Presets
- Apartment Soundscape
- Props P0
- Sealed Door System
- Zone Contamination

### Fase C — Sistemas que convierten authored en estado
- Diegetic Phone
- Authored Node Runner
- Cross-Effects Runtime
- TV Runtime
- Exterior & Threshold P0
- Creature Runtime Core
- Creature Manifestation Grammar

### Fase D — Contenido MVP
- Authored C01–C06
- TV Library MVP
- Exterior Events MVP

### Fase E — Final MVP
- Final Snapshot & Selector
- Final Local Variables & Locks
- Rutas A/B/C/D
- Final Staging Pack

### Fase F — Hardening
- Save/Load
- Performance
- QA Matrix
- Vertical Slice Internal Build

## Nota
Si una de estas bisagras falla, el resto del juego no se rompe por falta de ideas: se rompe por montaje malo. Este mapa está para evitar justo esa gilipollez técnica.