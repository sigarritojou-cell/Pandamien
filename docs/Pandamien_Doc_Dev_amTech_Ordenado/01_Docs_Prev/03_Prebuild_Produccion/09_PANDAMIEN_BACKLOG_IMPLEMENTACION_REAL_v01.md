# PANDAMIEN — Backlog real de implementación v01

## Estado
Este backlog traduce el estado actual del proyecto a trabajo montable de verdad: épicas, tareas, dependencias, orden de ataque y criterio de cierre.

## Supuestos de build
- Se construye un **MVP fuerte** antes que el juego completo.
- El primer corte jugable demuestra: apartamento P0, TV P0, umbral P0, contaminación P0, criatura MVP y final MVP.
- El recorrido implementado prioritario cubre **C01–C06** y desemboca en **4 rutas finales MVP**.
- C07–C08, perfiles extra y cierres C03/C04 quedan en cola de fase 2 salvo que sobre pulmón.

## Milestones
- **M0** — Fundación técnica y contrato canónico
- **M1** — Apartamento core y sistemas base
- **M2** — Vertical slice inicial — C01–C02
- **M3** — Vertical slice cuerpo/intimidad — C03–C04
- **M4** — Vertical slice umbral/semántica — C05–C06
- **M5** — Final MVP
- **M6** — Hardening y build interna

## Criterio de prioridad
- **P0**: bloquea MVP.
- **P1**: mejora mucho el MVP, pero no lo impide.
- **P2**: juego completo / fase 2.

## Orden recomendado de ataque
1. Contrato de datos y normalización.
2. Apartamento + puerta + contaminación + móvil + TV + exterior.
3. Integración authored C01–C06.
4. Snapshot y selector de final.
5. 4 rutas MVP del final.
6. Hardening y build interna.

## M0 — Fundación técnica y contrato canónico
### BLG-001 — Congelar contrato de variables P0 usando Q.4 y limpiar nombres legacy en runtime/data
- **Epic:** Canon & Data
- **Prioridad:** P0
- **Owner sugerido:** Sistemas + Continuidad
- **Dependencias:** -
- **Definition of Done:** Existe lista oficial de variables runtime; prefijos y nombres canónicos usados en código y datos.

### BLG-002 — Definir schema de datos para ciclos, nodos, TV, exterior, contaminación y final
- **Epic:** Canon & Data
- **Prioridad:** P0
- **Owner sugerido:** Gameplay Engineer
- **Dependencias:** BLG-001
- **Definition of Done:** Schemas versionados; validación básica; datos de ejemplo cargan sin errores.

### BLG-003 — Definir IDs únicos para ciclos, beats, nodos, triggers, líneas TV y finales
- **Epic:** Canon & Data
- **Prioridad:** P0
- **Owner sugerido:** Continuidad + Tech
- **Dependencias:** BLG-001
- **Definition of Done:** No hay colisiones de ID; convención documentada.

### BLG-004 — Crear panel debug de variables, zonas, vínculos y final selectors
- **Epic:** Canon & Data
- **Prioridad:** P0
- **Owner sugerido:** Tech
- **Dependencias:** BLG-002
- **Definition of Done:** Se pueden inspeccionar y forzar variables clave sin recompilar.

### BLG-005 — Diseñar savegame/profile state mínimo
- **Epic:** Canon & Data
- **Prioridad:** P0
- **Owner sugerido:** Tech
- **Dependencias:** BLG-002
- **Definition of Done:** Persisten progreso de ciclo, estado de zonas, vínculos, TV, criatura y flags de final.

### BLG-006 — Normalizar C/D/E bajo Biblia B y Q.4 para C01–C06
- **Epic:** Normalización
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Continuidad
- **Dependencias:** BLG-001, BLG-003
- **Definition of Done:** C01–C06 usan tono y nombres estables; redundancias marcadas o corregidas.

### BLG-007 — Traducir tablas legacy de efectos a variables canónicas runtime
- **Epic:** Normalización
- **Prioridad:** P0
- **Owner sugerido:** Sistemas
- **Dependencias:** BLG-001, BLG-006
- **Definition of Done:** Mapa legacy→canónico cerrado y usable por implementación.

### BLG-008 — Preparar pipeline simple de ingestión authored (Markdown/JSON manual) para nodos y beats
- **Epic:** Pipeline
- **Prioridad:** P1
- **Owner sugerido:** Tech + Narrativa
- **Dependencias:** BLG-002, BLG-003
- **Definition of Done:** Se pueden importar/actualizar datos authored sin tocar código núcleo.

## M1 — Apartamento core y sistemas base
### BLG-010 — Montar whitebox final del apartamento con layout canónico jugable
- **Epic:** Apartamento Core
- **Prioridad:** P0
- **Owner sugerido:** Entorno
- **Dependencias:** BLG-002
- **Definition of Done:** Se recorren salón, dormitorio, baño, cocina, entrada, pasillo y balcón/ventana principal.

### BLG-011 — Implementar navegación, colisiones y puntos de interacción base
- **Epic:** Apartamento Core
- **Prioridad:** P0
- **Owner sugerido:** Gameplay Engineer
- **Dependencias:** BLG-010
- **Definition of Done:** Jugador puede mirar, acercarse, activar, escuchar y usar puntos clave sin bloqueo.

### BLG-012 — Crear presets de iluminación día/tarde/noche/TV residual
- **Epic:** Apartamento Core
- **Prioridad:** P0
- **Owner sugerido:** Lighting
- **Dependencias:** BLG-010
- **Definition of Done:** Cambios de franja temporal legibles y consistentes con tono.

### BLG-013 — Montar audio espacial base del piso
- **Epic:** Apartamento Core
- **Prioridad:** P0
- **Owner sugerido:** Audio
- **Dependencias:** BLG-010
- **Definition of Done:** Nevera, tuberías, tejidos, patio/rellano y ambiente general funcionan por zona y franja.

### BLG-014 — Implementar props P0: cama, móvil, TV, sofá, mesa, espejo, lavabo/ducha/WC, nevera/fregadero, puerta principal, felpudo, medicación, 2 props íntimos, 2 de trabajo
- **Epic:** Props P0
- **Prioridad:** P0
- **Owner sugerido:** Entorno + Interacción
- **Dependencias:** BLG-010, BLG-011
- **Definition of Done:** Todos los props P0 existen y tienen lectura/interacción básica.

### BLG-015 — Implementar puerta atrancada + marco como sistema interactivo base
- **Epic:** Puerta Sellada
- **Prioridad:** P0
- **Owner sugerido:** Gameplay Engineer + Entorno
- **Dependencias:** BLG-010, BLG-011
- **Definition of Done:** Puerta tiene presencia, distancia, escucha y estados básicos de reactividad.

### BLG-016 — Crear 3–4 estados materiales P0 de marco/puerta
- **Epic:** Puerta Sellada
- **Prioridad:** P0
- **Owner sugerido:** Art + Tech Art
- **Dependencias:** BLG-015
- **Definition of Done:** Swaps/overlays funcionan y son legibles.

### BLG-017 — Implementar sistema base de contaminación por zonas con 3 niveles legibles
- **Epic:** Contaminación
- **Prioridad:** P0
- **Owner sugerido:** Tech Art + Systems
- **Dependencias:** BLG-010, BLG-011, BLG-007
- **Definition of Done:** Baño, dormitorio, salón y entrada/pasillo cambian de estado por variables.

### BLG-018 — Implementar contención parcial P0 (1 acción por ciclo/foco)
- **Epic:** Contaminación
- **Prioridad:** P0
- **Owner sugerido:** Gameplay Engineer
- **Dependencias:** BLG-017
- **Definition of Done:** Jugador puede contener un foco y el sistema desplaza o amortigua consecuencias sin anularlas.

### BLG-019 — Implementar gestor de transición día → noche → cierre → persistencia
- **Epic:** Transiciones
- **Prioridad:** P0
- **Owner sugerido:** Systems + Tech
- **Dependencias:** BLG-005, BLG-017
- **Definition of Done:** El loop avanza y persiste estado sin romper authored.

### BLG-020 — Implementar UI diegética mínima de móvil/mensajes/llamadas/audios
- **Epic:** Móvil & Comms
- **Prioridad:** P0
- **Owner sugerido:** UI Diegética + Tech
- **Dependencias:** BLG-011, BLG-005
- **Definition of Done:** Se pueden mostrar beats authored con respuesta directa/evasiva/delay/silence.

### BLG-021 — Implementar runner de nodos de diálogo y ecos
- **Epic:** Authored Runtime
- **Prioridad:** P0
- **Owner sugerido:** Gameplay Engineer
- **Dependencias:** BLG-002, BLG-020
- **Definition of Done:** Carga nodos authored, presenta opciones y aplica efectos.

### BLG-022 — Implementar motor de aplicación de efectos cruzados a variables y zonas
- **Epic:** Authored Runtime
- **Prioridad:** P0
- **Owner sugerido:** Systems
- **Dependencias:** BLG-007, BLG-021
- **Definition of Done:** Cada opción authored puede tocar vínculo, zona, TV, criatura y puerta.

### BLG-023 — Implementar TV runtime base con estados comfort/suggestion/manipulation/residual
- **Epic:** TV
- **Prioridad:** P0
- **Owner sugerido:** TV Designer + Tech
- **Dependencias:** BLG-011, BLG-012
- **Definition of Done:** La TV puede encenderse/apagarse/cambiar estado y emitir líneas por contexto.

### BLG-024 — Implementar sistema de umbral/exterior P0: mirilla, puerta principal, rellano sugerido, ventana/balcón, soundscape
- **Epic:** Exterior
- **Prioridad:** P0
- **Owner sugerido:** Entorno + Audio + Gameplay
- **Dependencias:** BLG-010, BLG-013, BLG-014
- **Definition of Done:** El borde ya funciona como sistema jugable, no sólo decorado.

### BLG-025 — Implementar estado base de criatura: mass/cohesion/visibility + func_* y temper_* mínimos
- **Epic:** Criatura Core
- **Prioridad:** P0
- **Owner sugerido:** Systems
- **Dependencias:** BLG-007, BLG-022
- **Definition of Done:** Las variables de criatura existen, cambian y pueden leerse en debug.

### BLG-026 — Implementar gramática de manifestación P0 no visible: respiración, golpe, sílaba, latido, silencio atento
- **Epic:** Criatura Core
- **Prioridad:** P0
- **Owner sugerido:** Audio + Experience
- **Dependencias:** BLG-025, BLG-015
- **Definition of Done:** La puerta puede devolver tipos de retorno distintos según estado.

## M2 — Vertical slice inicial — C01–C02
### BLG-100 — Integrar C01 Día authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-020, BLG-021, BLG-022
- **Definition of Done:** C01 día se juega completo con madre, amigo, editor y eco de ex.

### BLG-101 — Integrar C01 Noche authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-019, BLG-015, BLG-026, BLG-100
- **Definition of Done:** C01 noche devuelve primer signo tras puerta y cierra ciclo.

### BLG-102 — Integrar C02 Día authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-100, BLG-021, BLG-022
- **Definition of Done:** Trabajo coloniza salón y pareja/ex entra leve sin romper loop.

### BLG-103 — Integrar C02 Noche authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-101, BLG-026, BLG-102
- **Definition of Done:** Puerta articula mejor garganta/sílaba/golpe seco.

### BLG-104 — Cargar biblioteca TV P0 para C01–C02
- **Epic:** TV MVP
- **Prioridad:** P0
- **Owner sugerido:** TV Designer
- **Dependencias:** BLG-023, BLG-100, BLG-102
- **Definition of Done:** TV acompaña y empieza a suggestion con líneas aprobadas.

### BLG-105 — Implementar fenómenos authored P0 de exterior para C01–C02
- **Epic:** Exterior MVP
- **Prioridad:** P1
- **Owner sugerido:** Exterioridad + Audio
- **Dependencias:** BLG-024, BLG-100, BLG-102
- **Definition of Done:** Paquete, pasos, luz vecina y rellano básico sincronizan con ciclo.

## M3 — Vertical slice cuerpo/intimidad — C03–C04
### BLG-110 — Integrar C03 Día authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-103, BLG-017, BLG-018
- **Definition of Done:** Cuerpo toma el foco; madre/medicación pesan; baño/dormitorio mandan.

### BLG-111 — Integrar C03 Noche authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-110, BLG-026
- **Definition of Done:** Puerta respira/cuerpo blando/pecho con reactividad térmica o vibración.

### BLG-112 — Integrar C04 Día authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-111, BLG-021
- **Definition of Done:** Pareja/ex toma presión activa y contamina dormitorio/balcón.

### BLG-113 — Integrar C04 Noche authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-112, BLG-026
- **Definition of Done:** Puerta late/suplica y el piso padece mal el afecto.

### BLG-114 — Añadir props íntimos y estados P1 para dormitorio/balcón/baño
- **Epic:** Art & Audio
- **Prioridad:** P1
- **Owner sugerido:** Art + Audio
- **Dependencias:** BLG-014, BLG-017, BLG-112
- **Definition of Done:** Dormitorio, balcón y baño tienen riqueza suficiente para intimidad/cuerpo.

### BLG-115 — Cargar biblioteca TV P0/P1 para C03–C04
- **Epic:** TV MVP
- **Prioridad:** P0
- **Owner sugerido:** TV Designer
- **Dependencias:** BLG-023, BLG-110, BLG-112
- **Definition of Done:** TV suggestion clínica/sentimental funciona sin sonar mágica.

## M4 — Vertical slice umbral/semántica — C05–C06
### BLG-120 — Integrar C05 Día authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-113, BLG-024
- **Definition of Done:** Exterioridad/umbral toma presión activa y entrada/pasillo ganan centralidad.

### BLG-121 — Integrar C05 Noche authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-120, BLG-026
- **Definition of Done:** La casa enfoca: orientación, pausa dirigida, silencio atento.

### BLG-122 — Integrar C06 Día authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-121, BLG-023
- **Definition of Done:** TV toma presión activa y mezcla voces sin caos ilegible.

### BLG-123 — Integrar C06 Noche authored
- **Epic:** Ciclos MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech
- **Dependencias:** BLG-122, BLG-026
- **Definition of Done:** La puerta ensaya sintaxis defectuosa y contestación rota.

### BLG-124 — Añadir fenómenos authored P1 de umbral y balcón para C05–C06
- **Epic:** Exterior P1
- **Prioridad:** P1
- **Owner sugerido:** Exterioridad + Audio
- **Dependencias:** BLG-024, BLG-120, BLG-122
- **Definition of Done:** Mirilla, paso, conversación amortiguada, luz vecina y aire expuesto tienen suficiente variedad.

### BLG-125 — Cargar biblioteca TV manipulation/residual para C05–C06
- **Epic:** TV P1
- **Prioridad:** P1
- **Owner sugerido:** TV Designer
- **Dependencias:** BLG-023, BLG-122
- **Definition of Done:** La TV editorializa vigilancia y colonización semántica con control de tono.

### BLG-126 — Pasada de coherencia ciclo a ciclo C01–C06 bajo Biblia B
- **Epic:** QA Narrativa
- **Prioridad:** P0
- **Owner sugerido:** Continuidad + QA Narrativa
- **Dependencias:** BLG-100..BLG-123
- **Definition of Done:** Voces, residuos y ecos respetan familias y contaminación verbal.

## M5 — Final MVP
### BLG-200 — Implementar snapshot final y selector de perfil principal MVP
- **Epic:** Final MVP
- **Prioridad:** P0
- **Owner sugerido:** Systems + Tech
- **Dependencias:** BLG-025, BLG-122, BLG-123
- **Definition of Done:** El final lee variables y escoge entre P01/P05/P02/P10.

### BLG-201 — Implementar variables locales de confrontación y locks mínimos
- **Epic:** Final MVP
- **Prioridad:** P0
- **Owner sugerido:** Systems
- **Dependencias:** BLG-200
- **Definition of Done:** listen/contact/truth/denial/irreversibility/etc. funcionan en runtime.

### BLG-202 — Implementar Ruta A: P01 → C01 (La mano y el latido)
- **Epic:** Final MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech + Audio
- **Dependencias:** BLG-200, BLG-201, BLG-015
- **Definition of Done:** Ruta jugable completa con contacto, contención, latido y remate.

### BLG-203 — Implementar Ruta B: P05 → C02 (La rendija que responde)
- **Epic:** Final MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech + Audio
- **Dependencias:** BLG-200, BLG-201, BLG-015
- **Definition of Done:** Ruta jugable completa con diálogo, verdad, rendija y apertura.

### BLG-204 — Implementar Ruta C: P02 → C05 (El informe de carne)
- **Epic:** Final MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech + Audio
- **Dependencias:** BLG-200, BLG-201, BLG-015
- **Definition of Done:** Ruta jugable completa con juicio, negación/fractura y golpe seco.

### BLG-205 — Implementar Ruta D: P10 → C06 (El borde que te sabía)
- **Epic:** Final MVP
- **Prioridad:** P0
- **Owner sugerido:** Narrativa + Tech + Audio
- **Dependencias:** BLG-200, BLG-201, BLG-015, BLG-024
- **Definition of Done:** Ruta jugable completa con espera, borde y silencio atento.

### BLG-206 — Implementar staging/audio/luz P0 para las 4 rutas finales
- **Epic:** Final MVP
- **Prioridad:** P0
- **Owner sugerido:** Experience + Lighting + Audio
- **Dependencias:** BLG-202, BLG-203, BLG-204, BLG-205
- **Definition of Done:** Cada ruta tiene imagen dominante, cualidad sonora y remate distinguibles.

### BLG-207 — Integrar selector de cierre MVP limitado a C01/C02/C05/C06
- **Epic:** Final MVP
- **Prioridad:** P0
- **Owner sugerido:** Systems
- **Dependencias:** BLG-201
- **Definition of Done:** No se cuelan C03/C04; selección es coherente y depurable.

### BLG-208 — Pulir y fijar líneas/remates MVP canónicos
- **Epic:** Final MVP
- **Prioridad:** P1
- **Owner sugerido:** Narrativa + Continuidad
- **Dependencias:** BLG-202, BLG-203, BLG-204, BLG-205
- **Definition of Done:** Banco de líneas P0 congelado para build MVP.

## M6 — Hardening y build interna
### BLG-300 — Implementar guardado/carga estable de progreso hasta final MVP
- **Epic:** Hardening
- **Prioridad:** P0
- **Owner sugerido:** Tech
- **Dependencias:** BLG-005, BLG-123, BLG-207
- **Definition of Done:** Se puede salir y volver sin corromper estado.

### BLG-301 — Pasada de performance y estabilidad del apartamento + TV + audio + puerta
- **Epic:** Hardening
- **Prioridad:** P0
- **Owner sugerido:** Tech + QA
- **Dependencias:** BLG-123, BLG-206
- **Definition of Done:** FPS/estabilidad aceptables en escenas base y finales.

### BLG-302 — Matriz de test de rutas: 4 perfiles × 4 cierres MVP válidos
- **Epic:** Hardening
- **Prioridad:** P0
- **Owner sugerido:** QA Narrativa + Systems
- **Dependencias:** BLG-207
- **Definition of Done:** Hay casos de prueba y bugs clasificados por selector, nodos y remates.

### BLG-303 — Pasada de consistencia de variables y nomenclatura en código/datos
- **Epic:** Hardening
- **Prioridad:** P0
- **Owner sugerido:** Sistemas + Continuidad
- **Dependencias:** BLG-300
- **Definition of Done:** No quedan nombres legacy peligrosos.

### BLG-304 — Build vertical slice interna: C01–C06 + salto controlado a final MVP
- **Epic:** Hardening
- **Prioridad:** P0
- **Owner sugerido:** Producción + Tech
- **Dependencias:** BLG-123, BLG-206, BLG-300
- **Definition of Done:** Existe build jugable interna que demuestra loop completo y 4 finales MVP.

### BLG-305 — Preparar cola post-MVP: C03/C04 finales, perfiles P03/P04/P06/P07/P08/P09, C07–C08 authored fino, assets P2
- **Epic:** Fase 2
- **Prioridad:** P2
- **Owner sugerido:** Producción
- **Dependencias:** BLG-304
- **Definition of Done:** Post-MVP priorizado sin contaminar el MVP base.

## Corte oficial de MVP
### Entra sí o sí
- Apartamento canónico P0.
- TV runtime P0 con estados base.
- Umbral/exterior P0.
- Contaminación/contención P0.
- Criatura MVP no plenamente visible.
- C01–C06 implementados.
- Final MVP con rutas A/B/C/D.

### Se aplaza
- Perfiles finales P03/P04/P06/P07/P08/P09.
- Cierres C03 y C04.
- Microvariaciones de contaminación por prop.
- Exterior demasiado visible o demasiado rico.
- Combinatoria anatómica completa de criatura.

## Riesgos vigilados
- Creep de assets en exterior y criatura.
- Barro de variantes en final.
- Legacy variables sin migrar.
- TV demasiado débil o demasiado mágica.
- C05/C06 perdiendo claridad por exceso de ruido.

## Entregables inmediatos que salen de este backlog
- Tabla de features MVP.
- Lista de assets P0/P1.
- Rutas finales MVP con dependencias reales.
- Mapa de sistemas bloqueantes.
- Build interna vertical slice.

## Nota de dirección
Este backlog está hecho para montar la bestia sin que se convierta en barro: primero lo que sostiene el pecho del juego, luego lo que le pone joyitas.
