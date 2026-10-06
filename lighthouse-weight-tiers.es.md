> Traducción comunitaria (borrador) — Política P2-002 de NTARI, Difusión Multilingüe Global. Fuente: lighthouse-weight-tiers.md (original en inglés, instantánea del 2026-10-05). Borrador comunitario asistido por máquina, pendiente de revisión por mantenedores regionales conforme a P2-002 §3.1. Las especificaciones técnicas centrales permanecen en inglés conforme a §2.2.
>
> ¿Encontraste un error en esta traducción? Tu corrección es una contribución
> bienvenida y valorada: haz un fork del repositorio y abre un pull request en
> https://github.com/NTARI-RAND/lighthouse.

> **Precedencia.** El original en inglés es normativo. Esta traducción se ofrece para la lectura, no para la interpretación: donde difiera de `lighthouse-weight-tiers.md`, rige el inglés. Las palabras clave normativas (MUST, MUST NOT, SHOULD, SHOULD NOT, MAY), los nombres de campos, las etiquetas y los identificadores se mantienen en inglés porque constituyen el contrato de conformidad.

# Niveles de Peso de Lighthouse — Especificación en Borrador

Se rige por Janus-Facing Architecture (Arquitectura de Doble Faz). Un nivel es un **hecho estructural sobre la corroboración**, nunca un veredicto sobre la verdad. Los niveles se cuentan en **unidades de hubs independientes**: el hub, no la cuenta, es la unidad de conteo, con la independencia leída estructuralmente y los hubs bajo control común excluidos. Las definiciones de nivel son **política, no mecanismo** — viven como datos de política comparables por diff y se consignan en el registro atestiguado con entradas de registro de cambios en lenguaje llano, de modo que "¿qué reglas de nivel estaban en vigor cuando esto se renderizó?" siempre tiene una respuesta atestiguada. Todo renderizado que muestra un nivel porta un recibo: qué replicaciones, qué hubs, qué distribución de concordancia, qué versión de la política de niveles. Las afirmaciones de conocimiento y sus replicaciones son **relaciones tipadas**, distintas de las señales de comercio y de resolución de disputas; ningún lector puede difuminarlas.

---

## T0 — Anclado (Anchored)

Una afirmación de conocimiento existe en el registro atestiguado como una tripleta vinculada — **afirmación de hecho, procedimiento, resultado** — consignada por un declarante de buena reputación, en un hub, bajo la disciplina ordinaria de la capa de registro: de solo adición, atestiguada de forma independiente, monotónica. El ancla consigna **solo hechos estructurales y referencias**: los hashes de contenido de los tres artefactos, un tipo de afirmación, un identificador de versión del procedimiento, una marca de tiempo, una referencia seudónima del declarante, una referencia del hub. Los artefactos en sí — el procedimiento escrito, los datos — entran al bien común de contribuciones bajo AGPL, direccionados por contenido y servidos por los hubs; el libro mayor guarda los hashes.

- El anclaje está condicionado por el pacto: la reputación decide **si** una cuenta puede anclar, nunca cuánto ni con cuánta visibilidad.
- La existencia es el piso, nunca evidencia. Un lector puede inferir que esta afirmación, con este procedimiento, existía en este momento, proveniente de una cuenta que entonces tenía buena reputación. Un lector NO puede inferir revisión, plausibilidad ni verdad.
- Toda ancla es interpelable. Cualquiera puede anclar una impugnación que la referencie; el silencio del declarante acumula dwell (tiempo de permanencia) — un hecho legible, nunca uno resuelto automáticamente.
- Un artefacto que deja de ser recuperable no borra el ancla; la afirmación se renderiza como artefacto-oscuro (artifact-dark), otro hecho legible.
- Un incumplimiento posterior del pacto por parte de un declarante **anota sus anclas, nunca las borra**. Un fabricador puede haber dicho algo cierto; las replicaciones de sus afirmaciones se sostienen sobre su propio historial.

Superficie de manipulación: acuñación masiva. Defensa: T0 no dimensiona nada, toda ancla es una exposición interpelable bajo el pacto, y un hub puede limitar la tasa de anclaje como política local y publicada.

## T1 — Citado (Cited)

Otras anclas referencian la afirmación. Las citas son **aristas tipadas** — extends (amplía), uses-procedure (usa el procedimiento), disputes (disputa), mentions (menciona) — y los tipos de arista son datos de política. La citación renderiza el **grafo de descubrimiento**: es la manera en que las afirmaciones se encuentran, se exploran y se impugnan entre hubs.

- Los conteos de citas MUST NOT entrar en el peso, en la clasificación con fines de recompensa ni en la elegibilidad — **permanentemente**, no a la espera de nada. Las citas son, y seguirán siendo, casi gratuitas de acuñar; una señal que no cuesta nada no puede ponderar nada.
- Una arista *disputes* es de primera clase y se renderiza junto a *extends*. El grafo nunca compensa una con otra.
- Las superficies de descubrimiento MUST renderizar la procedencia — quién cita, desde qué hub — de modo que un anillo de citas sea legible como una forma. El escaneo de lo demasiado limpio lee los subgrafos cerrados como material de señalamiento; un señalamiento es insumo de impugnación, nunca una eliminación.

Un lector puede inferir atención y conectividad. Un lector NO puede inferir corroboración. La citación encuentra afirmaciones; nunca las confirma.

## T2 — Replicado en el mismo hub (Replicated in-hub)

Una cuenta distinta de la del declarante, registrada en el **propio hub del declarante**, ejecutó una versión específica del procedimiento y ancló una **replicación**: referencia a la versión del procedimiento, el hash de su propio resultado y su **declaración de concordancia** — consistente (consistent), inconsistente (inconsistent) o no concluyente (inconclusive) — que es su propia afirmación interpelable, impugnable como cualquier ancla.

- Todas las replicaciones dentro del mismo hub **colapsan en una sola unidad-hub** sin importar el número de cuentas. El colapso es la defensa contra Sybil: las cuentas títere no compran nada, y la métrica se sostiene sin ninguna detección de controladores.
- Las cuentas propias del declarante quedan excluidas; donde el control común de cuentas es estructuralmente visible, también se excluye — pero es la regla de colapso, no la detección, la que porta la garantía.
- T2 aporta estructura y renderizado, nunca elegibilidad. Su función es la rampa de acceso: demuestra que el procedimiento es **ejecutable por manos distintas de las de su autor**, y saca a la luz los defectos de procedimiento a bajo costo, antes de invertir esfuerzo entre hubs.

Un lector puede inferir ejecutabilidad e interés local. Un lector NO puede inferir confirmación independiente — un hub compartido significa equipo compartido, gravedad social compartida, puntos ciegos compartidos.

## T3 — Replicado entre hubs (Replicated cross-hub)

Existen replicaciones ancladas desde hubs **estructuralmente independientes** del hub del declarante. El nivel porta un conteo en unidades-hub — el número de hubs independientes distintos con al menos una replicación anclada — mantenido **por categoría de concordancia**: "consistente en cuatro hubs, inconsistente en uno" se publica exactamente así, permanentemente. Esta es la regla de no promediar aplicada al conocimiento.

- La independencia se lee estructuralmente a nivel de hub: control distinto par a par. Operador común, controlador común, matriz administrativa compartida — excluidos. **Las diez sucursales de un sistema bibliotecario de condado son una sola unidad.**
- La relación de testigo no es una relación de control. Los hubs que contrafirman mutuamente sus checkpoints siguen siendo corroboradores independientes; de lo contrario, los socios de federación nunca podrían corroborarse entre sí, y las redes pequeñas se estrangularían al nacer.
- Un hub es una unidad contable solo mientras su propio registro esté honestamente atestiguado — dos o más testigos independientes, ninguno de ellos con las claves del propio hub. Las replicaciones de un hub nuevo operan bajo la **etiqueta de suplencia** (stand-in) hasta que su atestiguamiento sea real: reconocimiento escalonado, exactamente como en la capa de gobernanza.
- La replicación real se dispersa. Una concordancia demasiado perfecta entre hubs supuestamente independientes es en sí misma material de señalamiento para el escaneo — la firma del comercio ficticio (wash trade) traducida al conocimiento.
- Una inconsistencia sin respuesta acumula dwell sobre la afirmación original — legible, nunca una degradación automática.

Superficie de manipulación: hubs acuñados, ya que AGPL significa que cualquiera puede levantar uno. Defensa: el estatus de unidad se gana estructuralmente — registro atestiguado, exclusión por control, suplencia hasta federarse — de modo que un hub falso cuesta lo que cuesta un hub real.

## T4 — Atestado (Attested)

Un hub ancla, bajo su propia clave institucional, una **atestación de ocurrencia**: esta versión del procedimiento se ejecutó en estas instalaciones, en esta fecha, en esta sesión, por esta referencia de cuenta. **Ocurrencia, nunca verdad** — el hub atesta el evento que alojó directamente, no el hallazgo. El resultado y la declaración de concordancia del replicador siguen siendo su propia ancla, separada y vinculada.

- Una atestación falsa es un incumplimiento del pacto por parte del propio hub — adjudicable, leído como estructura, que alimenta la lectura de conducta del operador que rige la reputación del hub. La atestación tiene dientes porque detrás de ella está la reputación de una institución.
- Se cuenta en unidades-hub como T3: muchas ejecuciones atestadas en un mismo hub son una sola unidad. El conteo de ejecuciones se renderiza como detalle y no dimensiona nada.
- **La atestación es un servicio, nunca un permiso.** Un hub puede negarse a alojar o atestar cualquier procedimiento — la programación, la supervisión y el deber de cuidado ordinario son política local del hub, publicada — y una afirmación rechazada no pierde nada en otra parte: se ancla en T0, recorre el grafo en T1, se corrobora entre hubs en T3. El cuidado ordinario de la sede hace el trabajo de seguridad sin que ningún centro se convierta en autoridad de verdad o de contenido.
- Un hub MUST NOT atestar ejecuciones de cuentas bajo su propio control — su operador, su personal actuando como el hub. En este nivel, el empleo es una relación de control; una unidad autoatestada es el zorro contando gallinas: cuenta cero y porta la etiqueta.
- El costo de acuñación del nivel es **cuerpos y tardes** — lineal en hubs, sin economías de escala. Esa linealidad, no ninguna verificación de identidad, es la economía de Sybil.

Un lector puede inferir que instituciones independientes comprometieron su reputación en que el evento ocurrió. Un lector NO puede inferir que el resultado sea correcto — solo que falsificarlo ahora le cuesta a instituciones reales tardes reales, multiplicadas.

---

## Disciplinas que rigen a través de los niveles

- **Vinculación de versiones.** Una replicación se vincula a la versión del procedimiento que ejecutó. Un procedimiento refinado es un ancla nueva que cita a la antigua; el peso se acumula por versión, con la cadena visible. De lo contrario, el peso se reúne sobre la v1 mientras la v2 se publica discretamente por debajo de ella.
- **La concordancia es dato; el incumplimiento es conducta.** Una replicación inconsistente es un hecho de concordancia, no una acusación, y jamás se encauza como reclamo de daño. Solo la conducta — la fabricación, la tergiversación de lo que se ejecutó, una atestación falsa — entra al canal de reclamos del pacto. **El desacuerdo nunca es incumplimiento.** Mantener separados los dos canales es lo que impide que los reclamos de daño se conviertan en el arma de la disputa científica.
- **Elegibilidad, nunca dimensionamiento.** El estatus de nivel condiciona si una afirmación es elegible para el flujo de entrada de la economía; el umbral — T3 o superior, o solo T4 en la activación — es política gobernada, no definición de nivel. El dimensionamiento de los pagos pertenece al intercambio real que financia, el cual carga con la fricción comercial que los niveles no pueden cargar.
- **Sin renderizado colapsado.** Sin puntaje único, sin estrellas, sin insignia de "verificado". Un nivel se renderiza con su recibo: las replicaciones, los hubs, la distribución de concordancia, la versión de la política en vigor.

## Solicitudes que deben rechazarse o señalarse

- *"Muestra el puntaje general de la afirmación."* → Reconstruye el promedio que el pacto prohíbe. Publica la distribución.
- *"Mejora la clasificación según el conteo de citas."* → T1 no dimensiona nada, permanentemente.
- *"Deja que el hub ateste las ejecuciones de su propio personal."* → Autoatestación con el disfraz de una clave institucional.
- *"Deja que los hubs cobren por una colocación más rápida o de nivel superior."* → Reputación vendida. La programación de atestaciones es política del hub; el estatus de nivel nunca se puede comprar.
- *"Degrada automáticamente ante una replicación inconsistente."* → La concordancia es dato. Renderízala; nunca la adjudiques por reloj ni por conteo.
- *"Marca la afirmación como verificada en T4."* → La autoridad de verdad con un abrigo más bonito. Ocurrencia, nunca verdad.
- *"Incorpora la reputación comercial al peso del conocimiento."* → Difumina las relaciones tipadas. Un buen comerciante no es por ello un buen declarante.

## Residuo nombrado

Exclusión geográfica: las comunidades sin hub participante no pueden alcanzar T4, y alcanzan T3 solo mediante registro a distancia — una brecha que debe resolverse con diseño (jornadas itinerantes de atestación, acuerdos con hubs asociados), nunca aceptarse en silencio. Arranque en frío: los conteos escasos de hubs al principio significan corroboración escasa; las etiquetas de suplencia portan la honestidad hasta que la federación se densifique. Los anillos de colusión de humanos reales que abarcan varios hubs siguen siendo posibles a costo lineal; son fraude — territorio del pacto — y cada caso adjudicado es un incumplimiento que nunca se diluye en un promedio.
