# PANDAMIEN — Lista de assets P0/P1 por disciplina v01

## Objetivo
Lista de assets realmente necesarios para arrancar build MVP, separados por disciplina y prioridad.

## Regla de lectura
- **P0**: entra sí o sí en el MVP.
- **P1**: entra si el calendario no se parte la crisma.

## Entorno
### AST-001 — Layout canónico del apartamento
- **Prioridad:** P0
- **Descripción:** Whitebox/bloqueo final con salón, dormitorio, baño, cocina, entrada, pasillo y balcón/ventana principal.
- **Depende de:** -
- **Definition of Done:** Se recorre completo y soporta loop C01–C06.

### AST-002 — Puerta atrancada + marco
- **Prioridad:** P0
- **Descripción:** Modelo base, colocación final y relación clara con pasillo.
- **Depende de:** AST-001
- **Definition of Done:** La puerta existe como foco espacial central y encaja con interacción base.

### AST-003 — Puerta principal + rellano sugerido
- **Prioridad:** P0
- **Descripción:** Puerta funcional, marco, felpudo y lectura del borde.
- **Depende de:** AST-001
- **Definition of Done:** Se soportan mirilla, sonido y eventos de umbral P0.

### AST-004 — Baño funcional
- **Prioridad:** P0
- **Descripción:** Espacio base con espejo, lavabo, ducha/WC y puntos de lectura corporal.
- **Depende de:** AST-001
- **Definition of Done:** Baño soporta C03 y contaminación P0.

### AST-005 — Dormitorio funcional
- **Prioridad:** P0
- **Descripción:** Cama, circulación, zona íntima y lectura de descanso/herida.
- **Depende de:** AST-001
- **Definition of Done:** Dormitorio soporta C03–C04 y finales íntimos.

### AST-006 — Salón funcional
- **Prioridad:** P0
- **Descripción:** TV, sofá/asiento principal, mesa y zona de trabajo básica.
- **Depende de:** AST-001
- **Definition of Done:** Salón soporta TV, C01–C02 y C06.

### AST-007 — Cocina funcional mínima
- **Prioridad:** P0
- **Descripción:** Nevera, fregadero, superficie de apoyo y lectura de rutina.
- **Depende de:** AST-001
- **Definition of Done:** Cocina soporta banalidad, hambre y abandono.

### AST-008 — Pasillo jugable
- **Prioridad:** P0
- **Descripción:** Compresión espacial, tránsito y foco de puerta.
- **Depende de:** AST-001
- **Definition of Done:** Pasillo sostiene C05–C06 y finales de borde.

### AST-009 — Ventana/balcón principal
- **Prioridad:** P0
- **Descripción:** Sistema visual y espacial básico de exterioridad.
- **Depende de:** AST-001
- **Definition of Done:** Permite aire, exposición y eco exterior.

## Tech Art
### AST-010 — Sistema de contaminación por zonas
- **Prioridad:** P0
- **Descripción:** Swaps/overlays para baño, dormitorio, salón y entrada/pasillo.
- **Depende de:** AST-001
- **Definition of Done:** Hay 3 niveles legibles por zona.

### AST-011 — Estados materiales del marco
- **Prioridad:** P0
- **Descripción:** 3–4 estados visibles del marco/puerta sellada.
- **Depende de:** AST-002
- **Definition of Done:** Cambios son legibles y ligados a variables.

### AST-012 — Contaminación fina por zona
- **Prioridad:** P1
- **Descripción:** Variantes extra por materialidad húmeda/orgánica/funcional.
- **Depende de:** AST-010
- **Definition of Done:** Hay más riqueza sin romper coherencia.

## Interacción
### AST-013 — Móvil diegético
- **Prioridad:** P0
- **Descripción:** Contenedor de mensajes, audios, llamadas e historial.
- **Depende de:** AST-006
- **Definition of Done:** Se puede resolver authored básico.

### AST-014 — Mirilla funcional
- **Prioridad:** P0
- **Descripción:** Entrada a lectura de umbral.
- **Depende de:** AST-003
- **Definition of Done:** Se activa, devuelve feedback y condiciona eventos.

### AST-015 — Puntos de interacción base
- **Prioridad:** P0
- **Descripción:** TV, puerta sellada, puerta principal, props P0, cama, espejo.
- **Depende de:** AST-001
- **Definition of Done:** Todos los puntos críticos son interactuables.

### AST-016 — Interacciones de contención adicionales
- **Prioridad:** P1
- **Descripción:** Variantes de limpiar/contener/retirar en zonas extra.
- **Depende de:** AST-010
- **Definition of Done:** Se amplía sin duplicar mecánicas.

## Props
### AST-017 — TV física
- **Prioridad:** P0
- **Descripción:** Pantalla, mueble/soporte y presencia visual coherente.
- **Depende de:** AST-006
- **Definition of Done:** La TV se integra física y sonoramente.

### AST-018 — Cama
- **Prioridad:** P0
- **Descripción:** Prop central de descanso/intimidad.
- **Depende de:** AST-005
- **Definition of Done:** Soporta lectura de C03–C04.

### AST-019 — Espejo de baño
- **Prioridad:** P0
- **Descripción:** Lectura corporal y foco de vulnerabilidad.
- **Depende de:** AST-004
- **Definition of Done:** Se usa como punto de lectura y eco.

### AST-020 — Mesa/superficie de trabajo
- **Prioridad:** P0
- **Descripción:** Soporte de portátil o trabajo residual.
- **Depende de:** AST-006
- **Definition of Done:** Hace legible la deuda funcional.

### AST-021 — Medicación/objeto corporal
- **Prioridad:** P0
- **Descripción:** Prop de cuerpo/cuidado.
- **Depende de:** AST-004
- **Definition of Done:** Se integra con C03.

### AST-022 — 2 props íntimos
- **Prioridad:** P0
- **Descripción:** Objetos personales de dormitorio/relación.
- **Depende de:** AST-005
- **Definition of Done:** Dejan huella emocional sin exceso de lore.

### AST-023 — 2 props de trabajo
- **Prioridad:** P0
- **Descripción:** Objetos funcionales ligados a editor/deuda.
- **Depende de:** AST-006
- **Definition of Done:** Refuerzan la colonización laboral del salón.

### AST-024 — Props de balcón/pareja-ex
- **Prioridad:** P1
- **Descripción:** Detalle material de intimidad y exposición.
- **Depende de:** AST-009, AST-022
- **Definition of Done:** Enriquecen C04 sin ser bloqueantes.

### AST-025 — Props de umbral/exterior
- **Prioridad:** P1
- **Descripción:** Paquete, bolsa, nota o equivalente authored.
- **Depende de:** AST-003
- **Definition of Done:** Exterior gana concreción sin inflarse.

## Audio
### AST-026 — Soundscape del apartamento
- **Prioridad:** P0
- **Descripción:** Nevera, tuberías, tejidos, electricidad, vacío doméstico.
- **Depende de:** AST-001
- **Definition of Done:** El piso suena vivo y localizado.

### AST-027 — Soundscape de rellano/patio/calle
- **Prioridad:** P0
- **Descripción:** Pasos, voces, luces, ambulancia, rumor vecinal.
- **Depende de:** AST-003, AST-009
- **Definition of Done:** El exterior existe sin sobrerrepresentarse.

### AST-028 — Banco criatura P0
- **Prioridad:** P0
- **Descripción:** Respiración, latido, golpe seco, sílaba rota, silencio atento.
- **Depende de:** AST-002
- **Definition of Done:** La puerta devuelve gramática no visible.

### AST-029 — Banco TV P0
- **Prioridad:** P0
- **Descripción:** Comfort, suggestion, manipulation, residual.
- **Depende de:** AST-017
- **Definition of Done:** La TV ya funciona por estados.

### AST-030 — Banco exterior authored ampliado
- **Prioridad:** P1
- **Descripción:** Voces amortiguadas, paquete, sombra, aire expuesto, barandilla.
- **Depende de:** AST-027
- **Definition of Done:** C05–C06 ganan variedad.

## Iluminación
### AST-031 — Presets día/tarde/noche
- **Prioridad:** P0
- **Descripción:** Lectura temporal y emocional por franja.
- **Depende de:** AST-001
- **Definition of Done:** El tiempo del piso se siente.

### AST-032 — Glow residual TV
- **Prioridad:** P0
- **Descripción:** Contamina salón/pasillo sin dominarlo todo.
- **Depende de:** AST-017
- **Definition of Done:** La TV deja rastro incluso apagada o residual.

### AST-033 — Lectura de pasillo/puerta
- **Prioridad:** P0
- **Descripción:** Control de foco en umbral y finales.
- **Depende de:** AST-002, AST-008
- **Definition of Done:** Pasillo y puerta tienen peso dramático.

### AST-034 — Presets finos por ciclo
- **Prioridad:** P1
- **Descripción:** Matices por C03–C06.
- **Depende de:** AST-031
- **Definition of Done:** Los ciclos se distinguen mejor sin rediseño completo.

## Narrativa/Contenido
### AST-035 — Biblioteca TV C01–C06
- **Prioridad:** P0
- **Descripción:** Líneas suficientes por estados y ciclos.
- **Depende de:** AST-029
- **Definition of Done:** La TV sostiene 6 ciclos sin repetición grosera.

### AST-036 — Authored C01–C06
- **Prioridad:** P0
- **Descripción:** Nodos, ecos y fichas integradas.
- **Depende de:** AST-013, AST-015
- **Definition of Done:** C01–C06 se juegan completos.

### AST-037 — Banco final MVP
- **Prioridad:** P0
- **Descripción:** Líneas/remates de P01/P05/P02/P10.
- **Depende de:** AST-028
- **Definition of Done:** Las 4 rutas finales distinguen voz y cierre.

### AST-038 — Refuerzo authored exterior
- **Prioridad:** P1
- **Descripción:** Eventos P1 de umbral/balcón/ventana.
- **Depende de:** AST-030, AST-036
- **Definition of Done:** Exterior gana densidad sin creep.

## Sistemas
### AST-039 — Variables core runtime
- **Prioridad:** P0
- **Descripción:** Persistencia de vínculo, TV, exterior, contaminación, criatura y final.
- **Depende de:** -
- **Definition of Done:** El runtime ya puede leer y escribir estado canónico.

### AST-040 — Selector de perfil final MVP
- **Prioridad:** P0
- **Descripción:** P01/P05/P02/P10.
- **Depende de:** AST-039, AST-036
- **Definition of Done:** El juego puede elegir la ruta final correcta.

### AST-041 — Sistema de loop día/noche
- **Prioridad:** P0
- **Descripción:** Transición, cierre y persistencia.
- **Depende de:** AST-039
- **Definition of Done:** El slice C01–C06 es jugable como secuencia real.

### AST-042 — Herramientas QA/debug
- **Prioridad:** P1
- **Descripción:** Forzado de estados, saltos de ciclo y selector de final.
- **Depende de:** AST-039
- **Definition of Done:** QA puede testear sin tortura manual.

## Corte recomendado
### P0 absolutos
- Apartamento canónico.
- Puerta atrancada y puerta principal.
- Contaminación por zonas.
- Móvil diegético.
- Mirilla.
- Soundscape del piso y del rellano.
- Banco criatura P0.
- Presets de luz.
- Biblioteca TV C01–C06.
- Authored C01–C06.
- Selector de final MVP.

### P1 prudentes
- Contaminación fina por zona.
- Props de balcón/pareja-ex.
- Props de umbral/exterior.
- Banco exterior authored ampliado.
- Presets finos por ciclo.
- Refuerzo authored exterior.
- Herramientas QA/debug más cómodas.

## Nota
Aquí no está todo lo bonito. Está lo que hace falta para que el juego tenga esqueleto, carne y voz sin ponerse barroco antes de tiempo.