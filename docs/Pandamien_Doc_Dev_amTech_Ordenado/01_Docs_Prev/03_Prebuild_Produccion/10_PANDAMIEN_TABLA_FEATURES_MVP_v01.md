# PANDAMIEN — Tabla de features MVP v01

## Qué es esto
Traducción del backlog a **features de producción** con estimación grosera por disciplina, prioridad y criterio de aceptación.

## Leyenda
- **Tamaño**: S / M / L / XL
- **P0**: entra sí o sí en MVP
- **P1**: entra si no rompe calendario

## Resumen rápido
- Features totales: **35**
- Features P0: **33**
- Features P1: **2**
- Ruta de corte: **C01–C06 + 4 finales MVP**

## Agrupación por bloques
### Fundación técnica
- **FEAT-001** — Core state & save (L, P0)
- **FEAT-002** — Debug & telemetry panel (M, P0)
- **FEAT-012** — Diegetic phone (L, P0)
- **FEAT-013** — Authored node runner (L, P0)
- **FEAT-014** — Cross-effects runtime (L, P0)

### Apartamento y sistemas base
- **FEAT-003** — Apartment whitebox final (L, P0)
- **FEAT-004** — Interaction base (L, P0)
- **FEAT-005** — Lighting presets (M, P0)
- **FEAT-006** — Apartment soundscape (L, P0)
- **FEAT-007** — Props P0 (L, P0)
- **FEAT-008** — Sealed door system (L, P0)
- **FEAT-009** — Zone contamination (L, P0)
- **FEAT-010** — Partial containment (M, P0)
- **FEAT-011** — Day-night loop (L, P0)

### TV / Exterior / Criatura
- **FEAT-015** — TV runtime P0 (L, P0)
- **FEAT-016** — Exterior & threshold P0 (L, P0)
- **FEAT-017** — Creature runtime core (M, P0)
- **FEAT-018** — Creature manifestation grammar (L, P0)
- **FEAT-022** — TV library MVP (L, P0)
- **FEAT-023** — Exterior events MVP (M, P1)

### Ciclos MVP
- **FEAT-019** — Cycles C01-C02 (L, P0)
- **FEAT-020** — Cycles C03-C04 (L, P0)
- **FEAT-021** — Cycles C05-C06 (XL, P0)

### Final MVP
- **FEAT-024** — Snapshot & final selector (M, P0)
- **FEAT-025** — Final local variables & locks (M, P0)
- **FEAT-026** — Final Route A P01→C01 (M, P0)
- **FEAT-027** — Final Route B P05→C02 (M, P0)
- **FEAT-028** — Final Route C P02→C05 (M, P0)
- **FEAT-029** — Final Route D P10→C06 (M, P0)
- **FEAT-030** — Final staging pack (M, P0)
- **FEAT-031** — Canonical final lines pack (S, P1)

### Hardening
- **FEAT-032** — Save/load hardening (M, P0)
- **FEAT-033** — Performance & stability pass (M, P0)
- **FEAT-034** — Route QA matrix (M, P0)
- **FEAT-035** — Vertical slice internal build (L, P0)

## Tabla completa
### FEAT-001 — Core state & save
- **Descripción:** Estado persistente de partida, variables P0, guardado/carga y perfil de progreso.
- **Disciplinas:** Tech, Systems
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** -
- **Aceptación:** Se guarda y restaura progreso de ciclos, zonas, vínculos, TV, criatura y flags de final.

### FEAT-002 — Debug & telemetry panel
- **Descripción:** Panel debug para variables, zonas, final selectors y triggers authored.
- **Disciplinas:** Tech, Systems, QA
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-001
- **Aceptación:** Permite inspeccionar/forzar estado y acelerar test de rutas.

### FEAT-003 — Apartment whitebox final
- **Descripción:** Layout jugable del apartamento con circulación canónica.
- **Disciplinas:** Environment, Tech
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** -
- **Aceptación:** Salón, dormitorio, baño, cocina, entrada, pasillo y balcón/ventana se recorren completos.

### FEAT-004 — Interaction base
- **Descripción:** Mirar, escuchar, activar, tocar, usar puntos de interacción y navegación estable.
- **Disciplinas:** Gameplay, Tech
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-003
- **Aceptación:** El jugador puede recorrer e interactuar sin bloqueos ni fricción accidental.

### FEAT-005 — Lighting presets
- **Descripción:** Presets de luz para día, tarde, noche y glow residual de TV.
- **Disciplinas:** Lighting, Environment
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-003
- **Aceptación:** Cambios temporales y climáticos son legibles y consistentes.

### FEAT-006 — Apartment soundscape
- **Descripción:** Audio espacial base del piso, patio, rellano, electrodomésticos y tejidos.
- **Disciplinas:** Audio, Tech
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-003
- **Aceptación:** El piso suena vivo y localizado por zonas/franjas.

### FEAT-007 — Props P0
- **Descripción:** Props imprescindibles: cama, móvil, TV, sofá, mesa, espejo, lavabo/ducha/WC, nevera/fregadero, puerta principal, medicación, props íntimos y de trabajo.
- **Disciplinas:** Environment, Interaction
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-003, FEAT-004
- **Aceptación:** Todos los props P0 existen y soportan lectura/interacción básica.

### FEAT-008 — Sealed door system
- **Descripción:** Puerta atrancada + marco con estados materiales y reactividad básica.
- **Disciplinas:** Gameplay, Environment, Tech Art
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-003, FEAT-004
- **Aceptación:** La puerta ya funciona como sistema, no como decorado.

### FEAT-009 — Zone contamination
- **Descripción:** Estados de contaminación por zonas con 3 niveles legibles y swaps/overlays.
- **Disciplinas:** Tech Art, Systems, Environment
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-003, FEAT-007
- **Aceptación:** Baño, dormitorio, salón y entrada/pasillo cambian según variables.

### FEAT-010 — Partial containment
- **Descripción:** Acción de contención/limpieza parcial por foco con coste y desplazamiento de consecuencia.
- **Disciplinas:** Gameplay, Systems, Narrative
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-009
- **Aceptación:** El jugador contiene una cosa y deja otra fermentar.

### FEAT-011 — Day-night loop
- **Descripción:** Gestor de transición día → noche → cierre → persistencia.
- **Disciplinas:** Systems, Tech
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-001, FEAT-009
- **Aceptación:** El loop avanza de forma fiable entre ciclos.

### FEAT-012 — Diegetic phone
- **Descripción:** UI diegética de móvil para mensajes, audios, llamadas, historial y respuestas.
- **Disciplinas:** UI Diegética, Tech, Gameplay
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-004, FEAT-001
- **Aceptación:** Se pueden disparar y resolver beats relacionales authored.

### FEAT-013 — Authored node runner
- **Descripción:** Runner de nodos de diálogo, ecos y beats authored.
- **Disciplinas:** Gameplay, Tech, Narrative Systems
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-012
- **Aceptación:** Carga datos authored y resuelve opciones/efectos.

### FEAT-014 — Cross-effects runtime
- **Descripción:** Aplicación runtime de efectos cruzados entre vínculo, zona, TV, criatura, puerta y exterior.
- **Disciplinas:** Systems, Tech
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-013, FEAT-001
- **Aceptación:** Toda decisión authored deja huella sistémica trazable.

### FEAT-015 — TV runtime P0
- **Descripción:** Televisión con estados comfort/suggestion/manipulation/residual y control básico de reproducción.
- **Disciplinas:** TV Design, Tech, Audio
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-004, FEAT-005
- **Aceptación:** La TV acompaña, sugiere y manipula según estado/ciclo.

### FEAT-016 — Exterior & threshold P0
- **Descripción:** Mirilla, puerta principal, rellano sugerido, ventana/balcón y soundscape de borde.
- **Disciplinas:** Environment, Audio, Gameplay
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-003, FEAT-006, FEAT-007
- **Aceptación:** El umbral ya puede ser jugado, escuchado y leído.

### FEAT-017 — Creature runtime core
- **Descripción:** Variables core de criatura: mass/cohesion/visibility + func_* y temper_* mínimos.
- **Disciplinas:** Systems, Tech
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-001, FEAT-014
- **Aceptación:** La criatura existe en sistema y puede perfilarse.

### FEAT-018 — Creature manifestation grammar
- **Descripción:** Respiración, golpe, sílaba, latido, silencio atento y reactividad de marco.
- **Disciplinas:** Audio, Experience, Gameplay
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-008, FEAT-017
- **Aceptación:** La criatura devuelve tipos de presencia distintos sin mostrarse del todo.

### FEAT-019 — Cycles C01-C02
- **Descripción:** Integración authored jugable de C01 y C02 completos.
- **Disciplinas:** Narrative, Tech, Systems
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-011, FEAT-013, FEAT-014, FEAT-015, FEAT-018
- **Aceptación:** Primer vertical slice funcional del loop cotidiano → noche.

### FEAT-020 — Cycles C03-C04
- **Descripción:** Integración authored jugable de C03 y C04 completos.
- **Disciplinas:** Narrative, Tech, Systems, Audio
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-019
- **Aceptación:** Cuerpo e intimidad ya pesan y devuelven puerta orgánica/torácica.

### FEAT-021 — Cycles C05-C06
- **Descripción:** Integración authored jugable de C05 y C06 completos.
- **Disciplinas:** Narrative, Tech, Systems, Audio
- **Tamaño:** XL
- **Prioridad:** P0
- **Depende de:** FEAT-020, FEAT-016, FEAT-015
- **Aceptación:** Umbral y colonización semántica funcionan con claridad.

### FEAT-022 — TV library MVP
- **Descripción:** Carga de librería TV para C01–C06 por estados y familias de programa.
- **Disciplinas:** TV Design, Writing, Audio
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-015, FEAT-019, FEAT-020, FEAT-021
- **Aceptación:** La TV tiene suficiente texto/tono para sostener 6 ciclos.

### FEAT-023 — Exterior events MVP
- **Descripción:** Paquete de fenómenos authored P0/P1 de exterior para C01–C06.
- **Disciplinas:** Exterioridad, Audio, Narrative
- **Tamaño:** M
- **Prioridad:** P1
- **Depende de:** FEAT-016, FEAT-019, FEAT-021
- **Aceptación:** Paquetes, pasos, luces, voces amortiguadas y aire expuesto tienen variedad suficiente.

### FEAT-024 — Snapshot & final selector
- **Descripción:** Snapshot de partida y selección de perfil final MVP.
- **Disciplinas:** Systems, Tech
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-017, FEAT-021
- **Aceptación:** El juego elige entre P01/P05/P02/P10 con lógica depurable.

### FEAT-025 — Final local variables & locks
- **Descripción:** Contadores locales del final y locks mínimos.
- **Disciplinas:** Systems, Tech
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-024
- **Aceptación:** El final reacciona a verbos duros y estados acumulados.

### FEAT-026 — Final Route A P01→C01
- **Descripción:** Ruta íntima de contención ética.
- **Disciplinas:** Narrative, Gameplay, Audio, Lighting
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-024, FEAT-025, FEAT-008, FEAT-018
- **Aceptación:** Se juega completa con mano, calor, latido y remate.

### FEAT-027 — Final Route B P05→C02
- **Descripción:** Ruta dialogada de apertura íntima.
- **Disciplinas:** Narrative, Gameplay, Audio, Lighting
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-024, FEAT-025, FEAT-008, FEAT-018
- **Aceptación:** Se juega completa con verdad, rendija y exhalación.

### FEAT-028 — Final Route C P02→C05
- **Descripción:** Ruta de juicio y fractura.
- **Disciplinas:** Narrative, Gameplay, Audio, Lighting
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-024, FEAT-025, FEAT-008, FEAT-018
- **Aceptación:** Se juega completa con juicio, negación y golpe seco.

### FEAT-029 — Final Route D P10→C06
- **Descripción:** Ruta de borde y umbral perpetuo.
- **Disciplinas:** Narrative, Gameplay, Audio, Lighting
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-024, FEAT-025, FEAT-008, FEAT-016, FEAT-018
- **Aceptación:** Se juega completa con espera, borde y silencio atento.

### FEAT-030 — Final staging pack
- **Descripción:** Staging, audio y luz P0 para las 4 rutas finales.
- **Disciplinas:** Experience, Audio, Lighting
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-026, FEAT-027, FEAT-028, FEAT-029
- **Aceptación:** Cada ruta final se distingue por imagen y cualidad sonora.

### FEAT-031 — Canonical final lines pack
- **Descripción:** Banco congelado de líneas/remates MVP.
- **Disciplinas:** Writing, Continuity
- **Tamaño:** S
- **Prioridad:** P1
- **Depende de:** FEAT-026, FEAT-027, FEAT-028, FEAT-029
- **Aceptación:** Las líneas P0 quedan fijadas para build y QA.

### FEAT-032 — Save/load hardening
- **Descripción:** Persistencia estable hasta final MVP.
- **Disciplinas:** Tech, QA
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-030
- **Aceptación:** No se corrompe estado entre sesiones.

### FEAT-033 — Performance & stability pass
- **Descripción:** Optimización base del apartamento + TV + audio + puerta.
- **Disciplinas:** Tech, QA
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-021, FEAT-030
- **Aceptación:** Rinde de forma aceptable en slice interna.

### FEAT-034 — Route QA matrix
- **Descripción:** Matriz de pruebas de ciclos y 4 finales MVP.
- **Disciplinas:** QA Narrativa, Systems
- **Tamaño:** M
- **Prioridad:** P0
- **Depende de:** FEAT-030
- **Aceptación:** Casos de prueba y bugs por selector, ruta y estado.

### FEAT-035 — Vertical slice internal build
- **Descripción:** Build interna jugable C01–C06 + 4 finales MVP.
- **Disciplinas:** Production, Tech, QA
- **Tamaño:** L
- **Prioridad:** P0
- **Depende de:** FEAT-032, FEAT-033, FEAT-034
- **Aceptación:** Existe build interna coherente y enseñable al equipo.

## Corte oficial recomendable
### MVP base
- FEAT-001 a FEAT-022
- FEAT-024 a FEAT-030
- FEAT-032 a FEAT-035

### P1 si respira el calendario
- FEAT-023 — Exterior events MVP
- FEAT-031 — Canonical final lines pack

## Lectura honesta de pasos que quedan
### Para cerrar prebuild documental-técnico
Quedan **3 pasos gordos**:
1. Lista de assets P0/P1 por disciplina.
2. Mapa de dependencias entre sistemas.
3. Primer sprint plan de implementación.

### Para poder arrancar producción sin hacer más biblia
Quedan **2 pasos**:
1. Aprobación de este corte de features.
2. Pasarlo a sprint/backlog ejecutable por disciplina.

## Nota de dirección
Aquí ya no estamos soñando. Aquí estamos eligiendo qué músculos se cosen primero para que la bestia ande antes de querer que baile.
