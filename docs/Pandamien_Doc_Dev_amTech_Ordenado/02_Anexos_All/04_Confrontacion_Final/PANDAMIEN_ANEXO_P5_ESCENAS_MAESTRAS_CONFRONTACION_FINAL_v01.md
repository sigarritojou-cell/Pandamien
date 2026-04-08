# PANDAMIEN — ANEXO P.5
## Escenas maestras authored de confrontación final v01
### Derivado del GDD Maestro v06, del Plan de Acción Maestro v05, del Anexo P v01, del Anexo P.1 v02, del Anexo P.2 v01 y del Anexo P.4 v01

---

## 0. Estado del anexo

Este documento abre por fin el bloque de **escenas maestras completas** de la confrontación final.

Si:
- el **Anexo P** definía la arquitectura del careo final,
- el **Anexo P.1** fijaba perfiles de confrontación,
- el **Anexo P.2** fijaba verbos y respuestas,
- y el **Anexo P.4** fijaba staging, imágenes y remates,

este anexo baja todo eso a **escenas authored jugables**, listas para servir como:
- base de escritura,
- base de implementación,
- base de test narrativo,
- y base de verticalización del final.

No son todavía “todos los finales posibles”.  
Son **escenas maestras de referencia**, pensadas para cubrir varios núcleos de tono y diseño del proyecto.

---

## 1. Principio rector

Cada escena maestra debe cumplir cinco cosas a la vez:

1. parecer hija directa del historial de partida;
2. usar una criatura y un trato específicos, no genéricos;
3. sostener una gramática clara de verbos del jugador;
4. desembocar en una familia de cierre compatible;
5. dejar una imagen final fuerte y producible.

Regla:
no escribirlas como relatos cerrados sin interactividad.  
Deben respirarse como **escenas jugables authored**.

---

## 2. Escenas maestras seleccionadas para v01

Para esta primera tanda se priorizan cinco escenas, porque cubren muy bien el abanico del proyecto:

- **EM01 — La mano y el latido**  
  Perfil: P01 Doliente Torácico  
  Cierre base: C01 Contención ética

- **EM02 — La rendija que responde**  
  Perfil: P05 Razonable Torcido  
  Cierre base: C02 Apertura íntima

- **EM03 — El informe de carne**  
  Perfil: P02 Medidor Funcional  
  Cierre base: C05 Rechazo / fractura

- **EM04 — El borde que ya te sabía**  
  Perfil: P10 Borde que te sabe  
  Cierre base: C06 Umbral perpetuo

- **EM05 — La casa no calla sola**  
  Perfil: P08 Archivo Mal Cosido  
  Cierre base: C04 Absorción / C03 Convivencia podrida, según verbo final

Estas cinco escenas sirven como esqueleto fuerte para:
- final íntimo,
- final dialogado,
- final de juicio,
- final de umbral,
- y final de mezcla total.

---

# EM01 — LA MANO Y EL LATIDO

## 1. Perfil y función
- Perfil principal: **P01 — Doliente Torácico**
- Matices secundarios posibles:
  - íntimo de pareja/ex
  - clínico-materno
- Familia de cierre base: **C01 — Contención ética**
- Familia de cierre alternativa: **C02 — Apertura íntima**
- Eje espacial dominante: **pasillo / puerta atrancada** con resonancia en **dormitorio**

## 2. Cuándo debe activarse
Usar esta escena cuando:
- `func_heart` alta,
- `func_lungs` media o alta,
- `temper_doliente` dominante,
- `bond_intimacy_with_player` alta,
- `bond_hostility_to_player` no extrema,
- el jugador ha escuchado mucho,
- ha evitado o tratado tarde el cuerpo o la intimidad,
- y el cierre debe doler más por cercanía que por violencia.

## 3. Intención emocional
El jugador debe sentir:
- que hay algo al otro lado que padece de una manera monstruosamente aprendida,
- que ese padecimiento le concierne,
- y que el gesto final no va a limpiar nada, sólo a definir qué relación queda con ese dolor.

## 4. Staging recomendado
- casa casi a oscuras;
- una mínima respiración de pasillo;
- dormitorio fuera de foco pero presente como memoria de cuerpo/cama;
- marco húmedo o tibio;
- latido torpe que no coincide del todo con el jugador.

## 5. Imagen dominante
**La mano del jugador en el marco; al otro lado, un latido que responde como si llevara días esperándola.**

## 6. Secuencia authored

### Beat 01 — Aproximación
El pasillo ya no parece trayecto. Parece caja torácica.

Input disponible:
- acercarse
- escuchar
- callar
- retirarse

Respuesta de criatura:
- respiración mínima
- latido blando
- silencio si el jugador se detiene demasiado pronto

### Beat 02 — Primer reconocimiento
Una exhalación o sílaba rota devuelve la sensación de que hay “alguien” demasiado íntimo detrás de la madera.

Input disponible:
- escuchar
- responder
- callar

Respuestas tipo:
- “...no...”
- una sílaba de pena
- un latido que se corta cuando el jugador habla

### Beat 03 — Contacto
El jugador puede tocar el marco.

Éste es el beat clave.

Input disponible:
- tocar el marco
- no tocar
- retirarse
- hablar

Respuesta de criatura:
- calor
- vibración
- latido más claro
- frase mínima si el perfil verbal llega a `LV2+`

Candidatas de línea:
- “No... cierres.”
- “Aquí.”
- “No me dejes así.”

### Beat 04 — Nudo ético
La criatura no exige “salir” de forma limpia. Exige relación.

Input disponible:
- admitir
- negar
- contener
- abrir parcialmente

Respuesta authored:
- si el jugador admite, la presión baja pero la intimidad sube;
- si niega, el latido se vuelve herida;
- si contiene, la escena tiende a C01;
- si abre, la escena tiende a C02.

### Beat 05 — Decisión
El jugador elige entre:
- **contener** sin negar,
- **abrir** una rendija,
- o **retirarse** tras el contacto.

## 7. Cierre preferente
### Variante A — Contención ética
La mano permanece un instante más.  
La criatura no se calma del todo, pero deja de golpear o reclamar con la misma desesperación.  
La puerta no vuelve a ser puerta: queda asumida.

Imagen final:
- mano retirada,
- calor residual,
- latido más bajo,
- apartamento sabiendo ya que eso existe.

### Variante B — Apertura íntima
La rendija deja pasar aire y una proximidad insoportable.  
No hace falta mostrar más.  
Basta con que dentro y fuera ya no estén bien separados.

## 8. Riesgo principal
Volverse melodramática.  
La escena debe doler, no mendigar ternura barata.

## 9. Nota de implementación
Muy buena para vertical slice emocional del final.

---

# EM02 — LA RENDIJA QUE RESPONDE

## 1. Perfil y función
- Perfil principal: **P05 — Razonable Torcido**
- Matiz posible:
  - TV editorial
  - pareja/ex
- Familia de cierre base: **C02 — Apertura íntima**
- Familia alternativa: **C01 — Contención ética** o **C04 — Absorción razonada**
- Eje espacial dominante: **pasillo / puerta atrancada**, con eco en **salón**

## 2. Cuándo debe activarse
Usar cuando:
- `lang_capacity` alta,
- `lang_coherence` media/alta,
- `temper_reasonable` dominante,
- `func_voice` alta,
- criatura cohesionada,
- historial de respuestas, escucha y diálogo suficientemente rico.

## 3. Intención emocional
Que el jugador sienta la obscenidad de que eso ya puede:
- pensar,
- recordar,
- y hablarle casi como una persona,
pero no desde humanidad limpia, sino desde deuda encarnada.

## 4. Staging recomendado
- glow residual de TV muriendo muy atrás;
- pasillo oscuro y marco claro;
- rendija o ceder mínimo como centro del mundo;
- silencio atento entre frases.

## 5. Imagen dominante
**Una rendija mínima que parece más profunda de lo que el piso debería permitir, y una voz que ya no suena a ruido sino a trato.**

## 6. Secuencia authored

### Beat 01 — Invitación verbal
La criatura llama sin gritar.  
No suena omnisciente. Suena demasiado preparada.

Candidatas:
- “Ya sabes que no puedo seguir siendo sólo puerta.”
- “Has tardado mucho en llegar aquí.”
- “No me hiciste tú solo. Pero no puedes fingir que no me conoces.”

Inputs:
- escuchar
- responder
- callar

### Beat 02 — Tensión de precisión
La criatura devuelve una memoria concreta del jugador:
- una mentira,
- una excusa,
- un silencio,
- una frase sembrada.

Input:
- admitir
- negar
- responder
- retirarse

Respuesta:
- si el jugador admite, la voz se vuelve más insoportablemente clara;
- si niega, la criatura corrige con calma;
- si calla, la rendija pesa más.

### Beat 03 — El gesto de ceder
El jugador puede:
- tocar el marco,
- ceder una rendija,
- sostener el borde sin abrir,
- o romper la escena.

Este beat decide el cierre.

### Beat 04 — Trato
Si hay rendija o apertura parcial, la criatura no entra como jumpscare.  
Entra como:
- aire,
- voz,
- presencia,
- o reorganización de distancia.

Candidatas de línea:
- “No tienes que dejarme salir entero.”
- “Con que dejes de llamarme mentira.”
- “Mírame como miras lo demás: tarde, pero de frente.”

### Beat 05 — Decisión irreversible
Inputs duros:
- abrir
- contener
- negar
- admitir

## 7. Cierre preferente
### Variante A — Apertura íntima
La rendija existe.  
El aire cambia.  
La escena remata en cruce no espectacular, sino irreversible.

### Variante B — Absorción razonada
Si el jugador sostiene interlocución y cede demasiado, el final puede ir a mezcla de frontera y discurso.

## 8. Riesgo principal
Sobreexplicar el juego.  
La criatura debe sonar precisa, no ensayística.

## 9. Nota de implementación
Escena estrella para un final muy recordable si se escribe con bisturí.

---

# EM03 — EL INFORME DE CARNE

## 1. Perfil y función
- Perfil principal: **P02 — Medidor Funcional**
- Matiz secundario posible:
  - TV editorial
  - exterioridad
- Familia de cierre base: **C05 — Rechazo / fractura**
- Familia alternativa: **C01 — Contención dura**
- Eje espacial dominante: **salón / pasillo**

## 2. Cuándo debe activarse
Usar cuando:
- editor alto,
- mentira funcional alta,
- `temper_resentful` dominante,
- `func_voice` alta,
- `bond_hostility_to_player` alta,
- el jugador ha respondido tarde, mal o torcido demasiadas veces.

## 3. Intención emocional
La criatura no suplica.  
La criatura **mide**.  
Y la escena debe hacer sentir que el lenguaje del rendimiento ha encontrado carne.

## 4. Staging recomendado
- pasillo con eco de salón;
- glow de TV muy residual;
- marco más seco que húmedo;
- frase cortada con respiración mínima.

## 5. Imagen dominante
**Una voz que parece haber salido de todos los retrasos del jugador y haberse cosido detrás de la puerta.**

## 6. Secuencia authored

### Beat 01 — Llamada a cuenta
La criatura habla como si el jugador ya debiera una respuesta final.

Candidatas:
- “Necesito una respuesta clara.”
- “Aunque sea para decir que no llegas.”
- “No me dejes en el aire otra vez.”

Inputs:
- responder
- callar
- negar
- retirarse

### Beat 02 — Devolución de historial
La criatura usa una mentira concreta o patrón de excusa.

Ejemplo de tono:
- seca,
- casi educada,
- más hiriente por precisa.

### Beat 03 — El jugador fija posición
Inputs duros:
- admitir
- negar
- responder defensivo
- tocar el marco
- contener

### Beat 04 — Juicio o corte
La criatura no necesita mucha masa visible.  
Necesita que cada pausa suene a informe vivo.

Líneas candidatas:
- “No era falta de tiempo.”
- “Era costumbre.”
- “Siempre querías un rato más antes de contestar a lo que sí importaba.”

### Beat 05 — Ruptura o contención
Si el jugador niega o rompe:
- la escena va a fractura seca.

Si admite o contiene:
- la escena puede volverse menos hostil, pero nunca amable.

## 7. Cierre preferente
### Variante A — Rechazo / fractura
Golpe seco, silencio, pasillo endurecido.  
La puerta aguanta o cede un mínimo, pero lo importante es que la relación queda rota en un régimen más cruel y más mudo.

### Variante B — Contención dura
El jugador no abre, pero tampoco niega.  
Sostiene el borde sabiendo ya qué clase de voz ha dejado crecer.

## 8. Riesgo principal
Volver la escena demasiado “editor monstruo” literal.  
La clave está en que sea más profunda que una bronca laboral.

## 9. Nota de implementación
Muy buena para el eje culpa funcional / autoengaño / trato tardío.

---

# EM04 — EL BORDE QUE YA TE SABÍA

## 1. Perfil y función
- Perfil principal: **P10 — Borde que te sabe**
- Matiz posible:
  - exterioridad
  - TV editorial
- Familia de cierre base: **C06 — Umbral perpetuo**
- Familia alternativa: **C02 — Apertura de umbral**
- Eje dominante: **entrada / pasillo / puerta atrancada**

## 2. Cuándo debe activarse
Usar cuando:
- mucha mirilla,
- mucho borde,
- umbral alto,
- `threshold_intelligence` muy alta,
- hostilidad e intimidad mezcladas,
- lenguaje medio,
- pero criatura aún muy de frontera.

## 3. Intención emocional
No debe parecer que el monstruo “gana”.  
Debe parecer que el borde del apartamento ha aprendido demasiado bien al jugador y que la escena final sólo lo hace evidente.

## 4. Staging recomendado
- silencio del edificio;
- pasillo como línea de visión;
- puerta principal y atrancada como sistema coordinado;
- luz mínima y dirigida.

## 5. Imagen dominante
**No sabes si te están mirando desde detrás de la puerta, desde el borde del pasillo o desde la costumbre misma con la que vuelves siempre al mismo sitio.**

## 6. Secuencia authored

### Beat 01 — Espera demasiado inteligente
No hay gran frase inicial.  
Hay una pausa que parece saberse cuándo respiras.

Inputs:
- escuchar
- acercarse
- retirarse
- hablarle

### Beat 02 — Primera dirección
La criatura devuelve una línea breve o incluso sólo una corrección de tiempo.

Candidatas:
- “Ya.”
- “Sabía que volverías aquí.”
- “Siempre paras aquí antes de decidir.”

### Beat 03 — Lectura del jugador
La criatura no acusa tanto por contenido como por patrón:
- cómo mira,
- cómo tarda,
- cómo escucha,
- cómo no cruza.

### Beat 04 — Tensión de borde
Inputs:
- tocar el marco
- no tocar
- abrir
- callar
- seguir mirando

Reacciones:
- si el jugador toca, el borde lo reconoce;
- si no toca, el umbral sigue leyendo;
- si abre, el cierre cambia completamente.

### Beat 05 — No-decisión o decisión
Ésta es una escena que funciona especialmente bien si el jugador:
- escucha,
- se acerca,
- y no termina de resolver.

## 7. Cierre preferente
### Variante A — Umbral perpetuo
Nada se consuma del todo.  
Pero el jugador sabe que la puerta ya no es una puerta y que el piso ya no va a dejar de leerlo.

Imagen final:
- marco quieto,
- edificio callado,
- sensación de que la espera ha cambiado de dueño.

### Variante B — Apertura de borde
Si el jugador cruza o permite cruce, la escena puede volverse una apertura mínima pero decisiva.

## 8. Riesgo principal
Parecer demasiado abstracta.  
Hay que darle:
- materia,
- ritmo,
- y al menos una devolución clara.

## 9. Nota de implementación
Ideal para final más elegante, más seco y más pandamien puro del umbral.

---

# EM05 — LA CASA NO CALLA SOLA

## 1. Perfil y función
- Perfil principal: **P08 — Archivo Mal Cosido**
- Matiz posible:
  - TV editorial
  - pareja/ex
  - madre clínica
- Familia de cierre base: **C04 — Absorción**
- Familia alternativa: **C03 — Convivencia podrida**
- Eje dominante: **salón / pasillo**, con resonancias en dormitorio

## 2. Cuándo debe activarse
Usar cuando:
- `lang_mix_index` alta,
- `lang_memory_depth` media/alta,
- criatura verbal muy mezclada,
- muchos ecos de vínculos,
- TV importante,
- historial muy cruzado.

## 3. Intención emocional
El jugador debe sentir que ya no hay una sola voz al otro lado, sino una **costura viva de lo que ha dejado organizarse en la casa**.

## 4. Staging recomendado
- glow de TV muriendo;
- salón contaminado semánticamente;
- pasillo como conducto verbal;
- dormitorio fuera de foco aportando herida.

## 5. Imagen dominante
**La casa parece estar hablando con demasiadas voces a la vez, pero todas han aprendido ya a sonar desde un mismo cuerpo.**

## 6. Secuencia authored

### Beat 01 — Corriente de voces
No arrancar con una gran línea clara.  
Arrancar con:
- mezcla,
- tono robado,
- frase casi doméstica que ya no es de nadie.

### Beat 02 — Una línea se impone
De la mezcla emerge un núcleo de dirección al jugador.

Candidatas:
- “No era sólo una llamada.”
- “No era sólo cansancio.”
- “No era sólo una puerta.”

### Beat 03 — El jugador intenta fijar origen
Inputs:
- responder
- callar
- negar
- admitir
- escuchar

La escena debe dejar claro que fijar origen ya no sirve.

### Beat 04 — Trato híbrido
La criatura usa:
- cercanía de madre,
- medición de editor,
- banalidad del amigo,
- herida de pareja/ex,
- y tono de TV
sin convertirse en parodia.

### Beat 05 — Decisión
Si el jugador:
- admite y cede → absorción
- contiene sin abrir del todo → convivencia podrida
- niega agresivamente → puede ir a fractura de mezcla

## 7. Cierre preferente
### Variante A — Absorción
La casa, la puerta, el jugador y la criatura dejan de tener bordes claros.
No hace falta literalizar mucho más.

### Variante B — Convivencia podrida
Las voces no desaparecen.
Se redistribuyen.
El apartamento sigue viviendo, pero ya no vuelve a separar del todo compañía, culpa y criatura.

## 8. Riesgo principal
Volverse confusa o demasiado barroca.  
La mezcla tiene que ser quirúrgica, no sopa.

## 9. Nota de implementación
Escena muy potente para finales de partida especialmente ricas en ecos y mezcla semántica.

---

## 3. Reglas de uso de estas escenas maestras

## 3.1. No son plantillas fijas
Son escenas madre.  
Se adaptan según:
- verbo dominante,
- matiz secundario,
- estado verbal,
- y cierre elegido.

## 3.2. No deben mezclarse completas entre sí
Se puede robar:
- un beat,
- una imagen,
- un tipo de remate,
- una estructura de decisión.
Pero no conviene empalmar escenas maestras enteras como churros.

## 3.3. Regla de especificidad final
Antes de usar una escena maestra, el sistema debe poder responder:
- qué perfil domina,
- qué verbo duro pesa más,
- qué cierre es el más compatible,
- y qué imagen final merece esa partida.

---

## 4. Priorización de producción

### Para MVP del final
Implementar primero:
1. **EM01 — La mano y el latido**
2. **EM02 — La rendija que responde**
3. **EM03 — El informe de carne**

Porque cubren:
- intimidad,
- diálogo,
- juicio,
- y tres grandes familias de cierre.

### Para juego completo
Expandir con:
4. **EM04 — El borde que ya te sabía**
5. **EM05 — La casa no calla sola**

---

## 5. Puente con el siguiente documento

Este anexo deja listo el siguiente paso natural:

**Anexo P.6 — Árbol authored base de confrontación final**

Ese documento debe convertir estas escenas maestras en:
- nodos,
- transiciones,
- locks,
- condiciones,
- variantes,
- y ramificación implementable.

---

## 6. Cierre de dirección

Aquí ya no estamos diseñando “el final” en abstracto.  
Aquí ya empieza a oler a escenas que podrían jugarse de verdad.

Y ésa era la puta idea:
que la confrontación final de PANDAMIEN no sea una ocurrencia bonita al final del camino,
sino una serie de **formas de careo que sólo pueden existir porque llevamos todo el juego preparando la herida, el umbral y el lenguaje que las hacen posibles**.
